---
title: Arrays van objecten gebruiken
description: Begrijp hoe CJA over gegevenshiërarchieën rapporteert.
exl-id: 59318da7-5408-4a9d-82aa-8bcbec7f7364
solution: Customer Journey Analytics
source-git-commit: faaf3d19ed37019ba284b41420628750cdb413b8
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Arrays van objecten gebruiken

Sommige platformschema&#39;s kunnen objectarrays hebben. Een van de meest voorkomende voorbeelden is een winkelwagentje, dat meerdere producten bevat. Elk product heeft een naam, SKU, categorie, prijs, hoeveelheid en andere afmetingen die u wilt bijhouden. Al deze facetten hebben verschillende eisen, maar moeten allen in de zelfde klap passen.

In eerdere versies van Adobe Analytics werd deze functie uitgevoerd met de opdracht `products` variabele. Het was een samengevoegde tekenreeks, gescheiden door puntkomma&#39;s (`;`) om de facetten van een product te scheiden, met komma&#39;s (`,`) afgebakende producten. Het was de enige variabele met beperkte ondersteuning van &quot;object arrays&quot;. Variabelen met meerdere waarden, zoals list vars, kunnen het equivalent van arrays ondersteunen, maar ze kunnen &#39;objectarrays&#39; niet ondersteunen. CJA breidt zich op dit concept uit door willekeurig diepe hiërarchieën binnen één enkele rij van gegevens te steunen, een eigenschap niet beschikbaar in om het even welke vorige versie van Adobe Analytics.

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

Aangezien u om het even welke afmeting met om het even welke metrisch kunt combineren, toont de volgende lijst hoe de gegevens met niet gespecificeerde afmetingspunten zouden:

| `product : warranty : name` | `product : orders` | `product : warranty : orders` |
| --- | --- | --- |
| `LG 2000 standard` | `1` | `1` |
| `Unspecified` | `2` | `1` |
| `Total` | `2` | `2` |

Er bestaat een productorder waaraan geen garantienaam is gekoppeld, zodat het item Dimensie aan &#39;Niet opgegeven&#39; toewijst. Dezelfde situatie geldt ook voor de productgarantiebestelling:

```diff
{
  "ID": "1", 
+  "product": [
+    {
      "SKU": "1234", 
      "category": "Washing Machines", 
      "name": "LG Washing Machine 2000", 
+      "orders": 1, 
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

Let op de bestellingen waaraan geen naam is gekoppeld. Dit zijn de orders die worden toegewezen aan de dimensie-item &#39;Niet gespecificeerd&#39;.

### Metrische gegevens combineren

In CJA worden metriek met dezelfde naam niet native gecombineerd als deze op verschillende objectniveaus staan.

| `product : category` | `product : revenue` | `product : warranty : revenue` |
| --- | --- | --- |
| `Washing Machines` | `1600` | `250` |
| `Dryers` | `500` | `0` |
| `Total` | `2100` | `250` |

U kunt echter wel een berekende maateenheid maken die de gewenste maatstaven combineert:

Berekende metrische &quot;totale inkomsten&quot;: `[product : revenue] + [product : warranty : revenue]`

Wanneer u deze berekende metrische waarde toepast, worden de gewenste resultaten weergegeven:

| `product : warranty : name` | `Total revenue (calculated metric)` |
| --- | --- |
| `Washing Machines` | `1850` |
| `Dryers` | `500` |
| `Total` | `2350` |
