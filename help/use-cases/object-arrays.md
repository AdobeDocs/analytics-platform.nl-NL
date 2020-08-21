---
title: Arrays van objecten gebruiken
description: Begrijp hoe CJA over gegevenshiërarchieën rapporteert.
translation-type: tm+mt
source-git-commit: 76cedb931085e8b5b59d7c5c3929bf4b5c010d9d
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 0%

---


# Arrays van objecten gebruiken

Sommige platformschema&#39;s kunnen objecten series hebben. Een van de meest voorkomende voorbeelden zou een winkelwagentje zijn, die meerdere producten bevat. Elk product heeft een naam, SKU, categorie, prijs, hoeveelheid, en een andere afmetingen u wilt volgen. Al deze facetten hebben afzonderlijke vereisten, maar moeten allen in de zelfde klap passen.

In vorige versies van de Analyse van Adobe, werd deze eigenschap verwezenlijkt gebruikend `products` variabele. Het was een aaneengeschakeld koord dat door puntkomma&#39;s wordt gescheiden (`;`) om facetten van een product te scheiden, terwijl komma&#39;s (`,`) afgebakende producten. Het was de enige variabele met beperkte ondersteuning van &quot;object arrays&quot;. Variabelen met meerdere waarden, zoals list vars, kunnen het equivalent van arrays ondersteunen, maar ze kunnen geen &#39;object arrays&#39; ondersteunen. CJA breidt zich op dit concept uit door willekeurig diepe hiërarchieën binnen één enkele rij van gegevens te steunen, een eigenschap niet beschikbaar in om het even welke vorige versie van de Analyse van Adobe.

## Zelfde treffer

De volgende hit is een JSON-object dat staat voor een aankoop door een klant van een wasmachine en droger.

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

Wanneer het creëren van een gegevensmening, zijn de volgende afmetingen en metrisch beschikbaar (gebaseerd op schema):

* **Dimensies:**
   * ID
   * product : SKU
   * product : naam
   * product : order_id
   * product : garantie : dekking
   * product : garantie : lengte
   * product : garantie : naam
   * product : garantie : type
* **Cijfers:**
   * product : orders
   * product : eenheden
   * product : inkomsten
   * product : garantie
   * product : garantie : inkomsten

### Zelfde hit-voorbeelden (rapporteringsgedrag)

Gebruikend enkel de bovengenoemde klap, tonen de volgende lijsten de rapporten van de Werkruimte met één of andere afmeting en metrische combinaties.

| `product : name` | `product : orders` | `product : revenue` |
| --- | --- | --- |
| `LG Washing Machine 2000` | `1` | `1600` |
| `LG Dryer 2000` | `1` | `500` |
| `Total` | `1` | `2100` |

CJA bekijkt selectief de afmeting en de metriek van het voorwerp dat op de lijst wordt gebaseerd.

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

CJA bekijkt deze delen van de klap om het rapport te produceren:

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

Aangezien u om het even welke afmeting met om het even welke metrisch kunt combineren, toont de volgende lijst hoe het gegeven met niet gespecificeerde afmetingspunten zou zijn:

| `product : warranty : name` | `product : orders` | `product : warranty : orders` |
| --- | --- | --- |
| `LG 2000 standard` | `1` | `1` |
| `Unspecified` | `2` | `1` |
| `Total` | `2` | `2` |

Een productorder bestaat zonder een garantienaam die eraan gekoppeld is, zodat wordt de dimensie item toegewezen aan &#39;Niet gespecificeerd&#39;. Dezelfde situatie geldt ook voor de bestelling van de productgarantie:

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

Neem nota van de orden die geen naam verbonden aan hen hebben. Dit zijn de orders toegewezen aan de &quot;Niet-gespecificeerde&quot; dimensie-post.

### Het combineren van metriek

CJA combineert niet natively zo ook genoemde metriek als zij op verschillende objecten niveaus zijn.

| `product : category` | `product : revenue` | `product : warranty : revenue` |
| --- | --- | --- |
| `Washing Machines` | `1600` | `250` |
| `Dryers` | `500` | `0` |
| `Total` | `2100` | `250` |

Nochtans, kunt u berekende metrisch tot stand brengen die de gewenste metriek combineert:

Berekende metrische &quot;totale inkomsten&quot;: `[product : revenue] + [product : warranty : revenue]`

Het toepassen van deze berekende metrische vertoningen de gewenste resultaten:

| `product : warranty : name` | `Total revenue (calculated metric)` |
| --- | --- |
| `Washing Machines` | `1850` |
| `Dryers` | `500` |
| `Total` | `2350` |

## Persistentie-voorbeelden

