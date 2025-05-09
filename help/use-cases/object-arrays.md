---
title: Arrays van objecten gebruiken
description: Leer hoe de Customer Journey Analytics over gegevenshiërarchieën rapporteert.
exl-id: 59318da7-5408-4a9d-82aa-8bcbec7f7364
solution: Customer Journey Analytics
feature: Use Cases
role: Admin
source-git-commit: aff01f4fc3520d461ca800382cc24d8d948d9cbc
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Arrays van objecten gebruiken

Sommige platformschema&#39;s kunnen objectarrays hebben. Adobe Customer Journey Analytics biedt ondersteuning voor het opnemen en rapporteren van objectarrays binnen gebeurtenis-, lookup- en profielgegevens. Een van de meest voorkomende voorbeelden is een winkelwagentje, dat meerdere producten bevat. Elk product heeft een naam, SKU, categorie, prijs, hoeveelheid en andere afmetingen die u wilt bijhouden. Al deze facetten hebben verschillende eisen, maar moeten allen in de zelfde klap passen.

In eerdere versies van Adobe Analytics werd deze functie uitgevoerd met de variabele `products` . Het was een aaneengeschakelde tekenreeks gescheiden door puntkomma&#39;s (`;`) om facetten van een product te scheiden, terwijl door komma&#39;s (`,`) afgebakende producten. Het was de enige variabele met beperkte ondersteuning van &quot;object arrays&quot;. Variabelen met meerdere waarden, zoals list vars, kunnen het equivalent van arrays ondersteunen, maar ze kunnen &#39;objectarrays&#39; niet ondersteunen. Customer Journey Analytics breidt zich op dit concept uit door willekeurig diepe hiërarchieën binnen één enkele rij van gegevens te steunen, een eigenschap niet beschikbaar in om het even welke vorige versie van Adobe Analytics.

## Zelfde gebeurtenisvoorbeeld

De volgende gebeurtenis is een JSON-object dat staat voor de aankoop door een klant van een wasmachine en droger.

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

* **Dimensionen:**
   * ID
   * product : SKU
   * product : name
   * product : order_id
   * product : garantie : dekking
   * product : warranty : length
   * product : warranty : name
   * product : warranty : type
* **Metriek:**
   * product : bestellingen
   * product : eenheden
   * product : inkomsten
   * product : garantie
   * product : warrant : opbrengst

### Zelfde gebeurtenisvoorbeelden (rapportagegedrag)

Met alleen de bovenstaande gebeurtenis worden in de volgende tabellen Workspace-rapporten met enkele afmetingen en metrische combinaties weergegeven.

| `product : name` | `product : orders` | `product : revenue` |
| --- | --- | --- |
| `LG Washing Machine 2000` | `1` | `1600` |
| `LG Dryer 2000` | `1` | `500` |
| `Total` | `1` | `2100` |

Customer Journey Analytics kijkt selectief naar de dimensie en metriek van het voorwerp dat op de lijst wordt gebaseerd.

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

Customer Journey Analytics bekijkt deze delen van de gebeurtenis om het rapport te produceren:

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

Er bestaat een productorder waaraan geen garantienaam is gekoppeld, zodat het item Dimensie aan &#39;Niet opgegeven&#39; toeschrijft. Dezelfde situatie geldt ook voor de productgarantiebestelling:

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

In Customer Journey Analytics worden metriek met dezelfde naam niet gecombineerd als deze op verschillende objectniveaus staan.

| `product : category` | `product : revenue` | `product : warranty : revenue` |
| --- | --- | --- |
| `Washing Machines` | `1600` | `250` |
| `Dryers` | `500` | `0` |
| `Total` | `2100` | `250` |

U kunt echter wel een berekende maateenheid maken die de gewenste maatstaven combineert:

Berekende metrische &quot;Totale omzet&quot;: `[product : revenue] + [product : warranty : revenue]`

Wanneer u deze berekende metrische waarde toepast, worden de gewenste resultaten weergegeven:

| `product : warranty : name` | `Total revenue (calculated metric)` |
| --- | --- |
| `Washing Machines` | `1850` |
| `Dryers` | `500` |
| `Total` | `2350` |



## Beperkingen

Beperkingen gelden wel voor arrays in gegevens die door Customer Journey Analytics worden gebruikt en die als onderdeel van een schema in Experience Platform zijn gemodelleerd. Zie {de modelgrenzen van 0} Gegevens [&#128279;](https://experienceleague.adobe.com/nl/docs/experience-platform/profile/guardrails#data-model-limits) en [ de formaatgrenzen van Gegevens ](https://experienceleague.adobe.com/nl/docs/experience-platform/profile/guardrails#data-size-limits) in de [ StandaardGidsen voor gegevens en de segmentatie van het Profiel van de Klant in real time ](https://experienceleague.adobe.com/nl/docs/experience-platform/profile/guardrails).

