---
title: Content Analytics-componenten
description: Details over de specifieke Content Analytics-componenten, zoals afmetingen, (berekende) meetwaarden en afgeleide velden
solution: Customer Journey Analytics
feature: Content Analytics
role: User
exl-id: 79bf235a-6f6e-4b04-bcd8-1ff884536648
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 1%

---

# Content Analytics-componenten

Content Analytics voegt de volgende categorieën componenten (afmetingen, (berekende) metriek, afgeleide gebieden) aan de reeds beschikbare componenten in Customer Journey Analytics toe:

* [Metagegevens ervaren](#experience-metadata)
* [Ervingkenmerken](#experience-attributes)
* [Gebeurtenissen van Experience](#experience-events)
* [Metagegevens van element](#asset-metadata)
* [Elementkenmerken](#asset-attributes)
* [Assets-gebeurtenissen](#asset-events)
* [Berekende cijfers](#calculated-metrics)

In de lijsten hieronder, ![ geproduceerde AI ](/help/assets/icons/AI.svg) wijst op een AI/ML geproduceerd attribuut/waardepaar.

## Metagegevens ervaren

| Titel | Beschrijving | Type |
|---|---|---|
| Experience Channel | Kanaal voor de ervaring. | Dimension |
| Ervaring-id | Unieke id voor de ervaring. | Dimension |
| Experience Thumbnail URL | URL voor de miniatuur van de ervaring. | Dimension |
| Ervaar de Horizontale Diepte van het Percentage | Kwantificeerbare waarde van de horizontale percentagediepte van de ervaring. | Dimension <br/> Afgeleid Gebied |
| Ervaar de verticale percentagediepte | Kwantificeerbare waarde van de verticale percentagediepte van de ervaring. | Dimension <br/> Afgeleid Gebied |

{style="table-layout:fixed"}



## Ervingkenmerken

| Titel | Beschrijving | Type |
|---|---|---|
| Experience Attributes | ![ AI produceerde ](/help/assets/icons/AI.svg) Volledige lijst van alle namen en waarden van de Attributen van de Ervaring | Dimension <br> Afgeleid Gebied |
| Ervaar leesbaarheid | ![ AI produceerde ](/help/assets/icons/AI.svg) Readability score van de ervaring | Dimension |
| Ervaar trefwoorden | ![ AI produceerde ](/help/assets/icons/AI.svg) Sleutelwoorden voor de ervaring. | Dimension <br> Afgeleid Gebied |
| Ervaar Persusiestrategieën | ![ AI produceerde ](/help/assets/icons/AI.svg) strategieën van de Uitdrukking die in de bepaalde ervaring aanwezig zijn. De mogelijke waarden zijn: Sociale identiteit, Sociale Bewijs, Autoriteit, Betrouwheid, Voetbal in de deur, Overkomende Reacantie, Wederkerigheid, Anchoring en Vergelijking, Sociale Effect, Schoolheid, en Anthropomorisme. | Dimension <br/> Afgeleid Gebied |
| Ervaar verhalen | ![ AI produceerde ](/help/assets/icons/AI.svg) Narratives die de ervaring bouwt op relevantie van het de meningspunt van een teller wordt gebaseerd. | Dimension <br/> Afgeleid Gebied |
| Ervaring met tinten | ![ AI produceerde ](/help/assets/icons/AI.svg) Tonen die de ervaring voortbouwt die op relevantie van het de meningspunt van een teller wordt gebaseerd | Dimension <br/> Afgeleid Gebied |
| Geniet van marketing | ![ AI produceerde ](/help/assets/icons/AI.svg) de emotie die in de lezer wordt aangehaald wanneer het lezen van de tekst die als deel van de ervaring wordt gebruikt: Urgentie, Exclusiviteit, Aanmoediging, Uitdaging, Curiositeit, Verwezenlijking, Vertrouwen, Eenvoud, en Fascination. | Dimension <br/> Afgeleid Gebied |
| Ervaar het aantal emojis | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal emojis voor de ervaring. | Metrisch |
| Aantal hashtags ervaren | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal hashtags voor de ervaring. | Metrisch |
| Aantal waardenreeksen van ervaring | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal zinnen voor de ervaring. | Metrisch |
| Woordenverhouding woordstop-ervaring | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal eindewoorden voor de ervaring. | Metrisch |
| Aantal tekstaanhalingstekens ervaren | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal tekstcitaten voor de ervaring. | Metrisch |
| Aantal woorden beleven | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal woorden voor de ervaring. | Metrisch |
| Ervaar het aantal woorden per zin | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal woorden per zin voor de ervaring. | Metrisch |

{style="table-layout:fixed"}


## Gebeurtenissen van Experience

| Titel | Beschrijving | Type |
|---|---|---|
| Weergaven beleven | Kwantificeerbare maat voor het aantal weergaven van de ervaring. | Metrisch |
| Ervaar klikken | Kwantificeerbare maat voor het aantal klikken op de ervaring. | Metrisch |

{style="table-layout:fixed"}


## Metagegevens van element

| Titel | Beschrijving | Type |
|---|---|---|
| Element-id | Unieke id van het element. Het binaire element bepaalt de uniciteit. Als het element binair verandert, verandert identiteitskaart wel. De unieke id kan de URL zijn, maar ook een gemaakte hash. | Dimension |
| HTML-pad voor element | Samengevoegd HTML-pad voor het element. | Dimension |
| Koppelings-URL voor element | Naaste paginanker voor het element. | Dimension |
| Breedte van middelenweergave | Weergavebreedte van inhoudselementen. | Dimension |
| Hoogte van bedrijfsmiddelenweergave | Hoogte van weergave van inhoudselementen. | Dimension |
| Absoluut linkerelement | Content asset absolute left. | Dimension |
| Absoluut bovenaan | Absolute top inhoudselement. | Dimension |

{style="table-layout:fixed"}


## Elementkenmerken

| Titel | Beschrijving | Type |
|---|---|---|
| Elementkenmerken | ![ AI produceerde ](/help/assets/icons/AI.svg) Volledige lijst van alle de attributennamen en waarden van Activa | Dimension <br> Afgeleid Gebied |
| Elementrichting | ![ AI produceerde ](/help/assets/icons/AI.svg) Richtlijn van de activa. | Dimension <br/> Afgeleid Gebied |
| Totale hoeveelheid element | ![ AI produceerde ](/help/assets/icons/AI.svg) Algemene toon van de activa. | Dimension <br/> Afgeleid Gebied |
| Voorgrondkleuren van element | ![ AI produceerde ](/help/assets/icons/AI.svg) Voorgrondkleuren van de activa. | Dimension <br/> Afgeleid Gebied |
| Achtergrondkleuren van element | ![ AI produceerde ](/help/assets/icons/AI.svg) Achtergrondkleuren van de activa. | Dimension <br/> Afgeleid Gebied |
| Elementlabels | ![ AI produceerde ](/help/assets/icons/AI.svg) Markeringen voor de activa. | Dimension <br/> Afgeleid Gebied |
| Elementen | ![ AI produceerde ](/help/assets/icons/AI.svg) Scènes voor de activa. | Dimension <br/> Afgeleid Gebied |
| Elementobjecten | ![ AI produceerde ](/help/assets/icons/AI.svg) Voorwerpen van de activa. | Dimension <br/> Afgeleid Gebied |
| Elementfotografie | ![ AI produceerde ](/help/assets/icons/AI.svg) de stijlen van de Fotografie van de activa. | Dimension <br/> Afgeleid Gebied |
| Afbeeldingstype element | ![ AI produceerde ](/help/assets/icons/AI.svg) Type van Beeld van de activa. Mogelijke waarden zijn: foto, schets, verven, digital_cartoon, infographics, graphic_design, collage en software_screenshot. | Dimension <br/> Afgeleid Gebied |
| Elementcameraposities | ![ AI produceerde ](/help/assets/icons/AI.svg) posities van de Camera van de activa. | Dimension <br/> Afgeleid Gebied |
| Middelen cameranabijheid | ![ AI produceerde ](/help/assets/icons/AI.svg) nabijheden van de Camera van de activa. | Dimension <br/> Afgeleid Gebied |
| Categorieën personen | ![ AI produceerde ](/help/assets/icons/AI.svg) categorieën van Mensen voor de activa. Mogelijke waarden zijn: persoon, man, vrouw, sociale groep, menigte, mensen, jongen, meisje en kind. | Dimension <br/> Afgeleid Gebied |
| Dichtheid van visuele elementen | ![ AI produceerde ](/help/assets/icons/AI.svg) Visuele inhoudsdichtheid van de activa. Mogelijke waarden zijn: laag, normaal of hoog. Een lage inhoudsdichtheid betekent dat er een kleine hoeveelheid informatie aanwezig is per oppervlakte-eenheid van de afbeelding. | Dimension |
| Asset Visual Attached Spread | ![ AI produceerde ](/help/assets/icons/AI.svg) Visuele aandachtsspreiding van de activa. Mogelijke waarden zijn: laag, normaal of hoog. De spreiding van de aandacht heeft betrekking op de mate waarin de aandacht van een kijker tussen verschillende delen van een beeld wordt verdeeld. | Dimension <br/> Afgeleid Gebied |
| Belichtingsvoorwaarde voor element | ![ AI produceerde ](/help/assets/icons/AI.svg) Verlichtingsvoorwaarde van de activa. Mogelijke waarden zijn: golden hour, blue hour, midday, overcast, night, high key, low key, daylighting, incandescent, fluorescerend, kleurrijk en studio. | Dimension <br/> Afgeleid Gebied |
| Instelling van camera-elementen | ![ AI produceerde ](/help/assets/icons/AI.svg) het plaatsen van de Camera van de activa. Mogelijke waarden zijn: snelle sluitersnelheid, lange belichting. Bokeh-vervaging, bewegingsvervaging, vervaging met kantelen, flash, groothoek, zwart-wit, surrealistisch, dubbele belichting, macro en normale modus. | Dimension <br/> Afgeleid Gebied |

{style="table-layout:fixed"}


## Gebeurtenissen van Asset

| Titel | Beschrijving | Type |
|---|---|---|
| Weergaven van elementen | Kwantificeerbare waarde van het aantal weergaven van het actief. | Metrisch |
| Elementklikken | Kwantificeerbare maatstaf voor het aantal klikken op het actief. | Metrisch |

{style="table-layout:fixed"}


<!--
## Other derived fields

| Title | Description | Type | Settings |
|---|---|---|---|
| Experience Path | Full path to the experience. | Derived Field | |
| Experience Path Root | Root path to the experience. | Derived Field | |
| Asset Location | Location of the asset. | Derived Field | |
| Asset Percenption ID + Asset ID | Combiination of asset perception identifier and asset identifier | Derived Field | |

{style="table-layout:fixed"}
-->

## Berekende cijfers

| Titel | Beschrijving | Type |
|---|---|---|
| Middelen klikken-dalingssnelheid | Elementklikken/Elementweergaven | Berekende metrische waarde |
| ervaringsdoorkliksnelheid | Ervaar de klikken/Ervaar Weergaven | Berekende metrische waarde |

{style="table-layout:fixed"}

