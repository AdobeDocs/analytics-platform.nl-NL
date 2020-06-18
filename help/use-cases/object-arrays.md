---
title: CJA gebruiken met arrays van objecten
description: Begrijp hoe CJA over gegevenshiërarchieën rapporteert.
translation-type: tm+mt
source-git-commit: b7cd74f3fe2f0222e78452f58a7c387f6e0c86d2
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# CJA gebruiken met arrays van objecten

Sommige platformschema&#39;s kunnen objectarrays hebben. Een van de meest voorkomende voorbeelden is een winkelwagentje, dat meerdere producten bevat. Elk product heeft een naam, SKU, categorie, prijs, hoeveelheid en andere afmetingen die u wilt bijhouden. Al deze facetten hebben verschillende eisen, maar moeten allen in de zelfde klap passen.

In eerdere versies van Adobe Analytics werd deze functie uitgevoerd met de `products` variabele. Het was een samengevoegde tekenreeks, gescheiden door puntkomma&#39;s (`;`), om facetten van een product te scheiden, terwijl door komma&#39;s (`,`) gescheiden producten. Het was de enige variabele met beperkte ondersteuning van &quot;object arrays&quot;. Variabelen met meerdere waarden, zoals list vars, kunnen het equivalent van arrays ondersteunen, maar ze kunnen &#39;objectarrays&#39; niet ondersteunen. CJA breidt dit concept uit door willekeurig diepe hiërarchieën binnen één enkele rij van gegevens te steunen, een eigenschap niet beschikbaar in om het even welke vorige versie van Adobe Analytics.

## Zelfde raakvoorbeeld

De volgende hit is een JSON-object dat een klant vertegenwoordigt die van een wasmachine en droger is gemaakt.

```json
{
  "ID": "1", 
  "product": [
    {
      "SKU": "1234", 
      "category": "Washing Machines", 
      "name": "LG Washing Machine 2000", 
      "orders": 1, 
      "revenue": 1600, 
      "units": 1,
      "order_id":"abc123", 
      "warranty": [
        {
          "coverage": "full coverage", 
          "length": "2 year", 
          "name": "LG 2000 standard", 
          "orders": 1, 
          "revenue": 200
        }, 
        {
          "coverage": "extended", 
          "length": "1 year", 
          "orders": 1, 
          "revenue": 50, 
          "type": "LG 2000 addon"
        }
      ]
    }, 
    {
      "SKU": "4567", 
      "category": "Dryers", 
      "name": "LG Dryer 2000", 
      "orders": 1, 
      "revenue": 500, 
      "units": 1
    }
  ], 
  "timestamp": 1534219229
}
```

Bij het maken van een gegevensweergave zijn de volgende afmetingen en metrische gegevens beschikbaar (op basis van schema):

* **Dimensies:**
   * ID
   * product: SKU
   * product: name
   * product: order_id
   * product: garantie: dekking
   * product: garantie: length
   * product: garantie: name
   * product: garantie: type
* **Cijfers:**
   * product: orders
   * product: eenheden
   * product: inkomsten
   * product: garantie
   * product: garantie: inkomsten

### Zelfde treffers (rapportagegedrag)

Gebruikend enkel bovengenoemde klap, tonen de volgende lijsten de rapporten van de Werkruimte met één of andere afmeting en metrische combinaties.

| `product : name` | `product : orders` | `product : revenue` |
| --- | --- | --- |
| `LG Washing Machine 2000` | `1` | `1600` |
| `LG Dryer 2000` | `1` | `500` |
| `Total` | `1` | `2100` |

CJA kijkt selectief naar de dimensie en metriek van het voorwerp dat op de lijst wordt gebaseerd.

```diff
{
  "ID": "1", 
+  "product": [
+    {
      "SKU": "1234", 
      "category": "Washing Machines", 
+      "name": "LG Washing Machine 2000", 
+      "orders": 1, 
+      "revenue": 1600, 
      "units": 1,
      "order_id":"abc123", 
      "warranty": [
        {
          "coverage": "full coverage", 
          "length": "2 year", 
          "name": "LG 2000 standard", 
          "orders": 1, 
          "revenue": 200
        }, 
        {
          "coverage": "extended", 
          "length": "1 year", 
          "orders": 1, 
          "revenue": 50, 
          "type": "LG 2000 addon"
        }
      ]
+    }, 
+    {
      "SKU": "4567", 
      "category": "Dryers", 
+      "name": "LG Dryer 2000", 
+      "orders": 1, 
+      "revenue": 500, 
      "units": 1
+    }
+  ], 
+  "timestamp": 1534219229
+}
```

Als u over enkel garantieopbrengst wilde rapporteren, zou uw project gelijkaardig aan het volgende kijken:

| `product : warranty : coverage` | `product : warranty : revenue` |
| --- | --- |
| `full coverage` | `200` |
| `extended` | `50` |
| `Total` | `250` |

CJA kijkt naar deze delen van de hit om het rapport te genereren:

```diff
{
  "ID": "1", 
+  "product": [
+    {
      "SKU": "1234", 
      "category": "Washing Machines", 
      "name": "LG Washing Machine 2000", 
      "orders": 1, 
      "revenue": 1600, 
      "units": 1,
      "order_id":"abc123", 
+      "warranty": [
+        {
+          "coverage": "full coverage", 
          "length": "2 year", 
          "name": "LG 2000 standard", 
          "orders": 1, 
+          "revenue": 200
+        }, 
+        {
+          "coverage": "extended", 
          "length": "1 year", 
          "orders": 1, 
+          "revenue": 50, 
          "type": "LG 2000 addon"
+        }
+      ]
+    }, 
    {
      "SKU": "4567", 
      "category": "Dryers", 
      "name": "LG Dryer 2000", 
      "orders": 1, 
      "revenue": 500, 
      "units": 1
    }
+  ], 
+  "timestamp": 1534219229
+}
```

Aangezien de droger geen garantie bevatte, is deze niet in de tabel opgenomen.

Aangezien u om het even welke afmeting met om het even welke metrisch kunt combineren, toont de volgende lijst hoe de gegevens met niet gespecificeerde afmetingswaarden zouden zijn:

| `product : warranty : name` | `product : orders` | `product : warranty : orders` |
| --- | --- | --- |
| `LG 2000 standard` | `1` | `1` |
| `Unspecified` | `2` | `1` |
| `Total` | `2` | `2` |

Er bestaat een productorder waaraan geen garantienaam is gekoppeld, zodat de waarde van de dimensie aan &#39;Unspecified&#39; wordt toegewezen. Dezelfde situatie geldt ook voor de productgarantiebestelling:

```diff
{
  "ID": "1", 
+  "product": [
+    {
      "SKU": "1234", 
      "category": "Washing Machines", 
      "name": "LG Washing Machine 2000", 
      "orders": 1, 
      "revenue": 1600, 
      "units": 1,
      "order_id":"abc123", 
+      "warranty": [
+        {
          "coverage": "full coverage", 
          "length": "2 year", 
+          "name": "LG 2000 standard", 
+          "orders": 1, 
          "revenue": 200
+        }, 
+        {
          "coverage": "extended", 
          "length": "1 year", 
+          "orders": 1, 
          "revenue": 50, 
          "type": "LG 2000 addon"
+        }
+      ]
+    }, 
+    {
      "SKU": "4567", 
      "category": "Dryers", 
      "name": "LG Dryer 2000", 
+      "orders": 1, 
      "revenue": 500, 
      "units": 1
+    }
+  ], 
+  "timestamp": 1534219229
+}
```
