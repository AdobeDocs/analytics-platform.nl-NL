---
title: Componenten van Content Analytics
description: Bijzonderheden over de specifieke componenten voor de analyse van inhoud, zoals afmetingen, (berekende) meetwaarden en afgeleide velden
solution: Customer Journey Analytics
feature: Content Analytics
role: User
hide: true
hidefromtoc: true
exl-id: 79bf235a-6f6e-4b04-bcd8-1ff884536648
source-git-commit: 62491fcbf37961d33be92d209e5710bf9696c223
workflow-type: tm+mt
source-wordcount: '1390'
ht-degree: 1%

---

# Componenten van Content Analytics

>[!WARNING]
>
>Dit artikel is een voorlopige niet-officiële ontwerpversie van een toekomstige definitieve versie en maakt deel uit van de documentatie van Content Analytics. Alle inhoud kan worden gewijzigd en er kunnen geen wettelijke verplichtingen uit de huidige versie van dit artikel worden afgeleid.
>

{{release-limited-testing}}

Met Content Analytics worden de volgende categorieën componenten (afmetingen, (berekende) waarden, afgeleide velden) toegevoegd aan de reeds beschikbare componenten in Customer Journey Analytics:

* [Metagegevens ervaren](#experience-metadata)
* [Ervingkenmerken](#experience-attributes)
* [Gebeurtenissen van Experience](#experience-events)
* [Metagegevens van element](#asset-metadata)
* [Elementkenmerken](#asset-attributes)
* [Assets-gebeurtenissen](#asset-events)
* [Berekende cijfers](#calculated-metrics)

In de lijsten hieronder, ![ geproduceerde AI ](/help/assets/icons/AI.svg) wijst op een AI/ML geproduceerde waarde.

## Metagegevens ervaren

| Titel | Beschrijving | Type | Instellingen |
|---|---|---|---|
| Experience Channel | Kanaal voor de ervaring. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Ervaar Source | Source URL of the experience. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Ervaring-id | Unieke id voor de ervaring. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Naam van ervaring | Naam voor de ervaring. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Beschrijving van ervaring | Beschrijving van de ervaring. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Experience Thumbnail URL | URL voor de miniatuur van de ervaring. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Ervaar de Horizontale Diepte van het Percentage | Kwantificeerbare waarde van de horizontale percentagediepte van de ervaring. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Ervaar de verticale percentagediepte | Kwantificeerbare waarde van de verticale percentagediepte van de ervaring. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Ervaar de horizontale pixeldiepte | Kwantificeerbare waarde van de horizontale pixeldiepte van de ervaring. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Ervaar verticale pixeldiepte | Kwantificeerbare waarde van de verticale pixeldiepte van de ervaring. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |

{style="table-layout:fixed"}



## Ervingkenmerken

| Titel | Beschrijving | Type | Instellingen |
|---|---|---|---|
| Ervaar leesbaarheid | ![ AI produceerde ](/help/assets/icons/AI.svg) Readability score voor de ervaring. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Ervaar trefwoorden | ![ AI produceerde ](/help/assets/icons/AI.svg) Sleutelwoorden voor de ervaring. | Dimension <br> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Ervaar Persusiestrategieën | ![ AI produceerde ](/help/assets/icons/AI.svg) strategieën van de Uitdrukking die in de bepaalde ervaring aanwezig zijn. De mogelijke waarden zijn: Sociale identiteit, Sociale Bewijs, Autoriteit, Betrouwheid, Voetbal in de deur, Overkomende Reacantie, Wederkerigheid, Anchoring en Vergelijking, Sociale Effect, Schoolheid, en Anthropomorisme. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Ervaar verhalen | ![ AI produceerde ](/help/assets/icons/AI.svg) Narratives die de ervaring bouwt op relevantie van het de meningspunt van een teller wordt gebaseerd. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Ervaring met tinten | ![ AI produceerde ](/help/assets/icons/AI.svg) Tonen die de ervaring voortbouwt die op relevantie van het de meningspunt van een teller wordt gebaseerd | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Geniet van marketing | ![ AI produceerde ](/help/assets/icons/AI.svg) de emotie die in de lezer wordt aangehaald wanneer het lezen van de tekst die als deel van de ervaring wordt gebruikt: Urgentie, Exclusiviteit, Aanmoediging, Uitdaging, Curiositeit, Verwezenlijking, Vertrouwen, Eenvoud, en Fascination. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Ervaar het aantal emojis | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal emojis voor de ervaring. | Metrisch | Aantal waarden <br/> Decimaal \| Decimalen: 0 |
| Aantal hashtags ervaren | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal hashtags voor de ervaring. | Metrisch | Aantal waarden <br/> Decimaal \| Decimalen: 0 |
| Aantal waardenreeksen van ervaring | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal zinnen voor de ervaring. | Metrisch | Aantal waarden <br/> Decimaal \| Decimalen: 0 |
| Woordenverhouding woordstop-ervaring | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal eindewoorden voor de ervaring. | Metrisch | Aantal waarden <br/> Decimaal \| Decimalen: 0 |
| Aantal tekstaanhalingstekens ervaren | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal tekstcitaten voor de ervaring. | Metrisch | Aantal waarden <br/> Decimaal \| Decimalen: 0 |
| Aantal woorden beleven | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal woorden voor de ervaring. | Metrisch | Aantal waarden <br/> Decimaal \| Decimalen: 0 |
| Ervaar het aantal woorden per zin | ![ AI produceerde ](/help/assets/icons/AI.svg) Aantal woorden per zin voor de ervaring. | Metrisch | Aantal waarden <br/> Decimaal \| Decimalen: 0 |

{style="table-layout:fixed"}


## Gebeurtenissen van Experience

| Titel | Beschrijving | Type | Instellingen |
|---|---|---|---|
| Weergaven beleven | Kwantificeerbare maat voor het aantal weergaven van de ervaring. | Metrisch | Aantal waarden <br/> Decimaal \| Decimalen: 0 |
| Ervaar klikken | Kwantificeerbare maat voor het aantal klikken op de ervaring. | Metrisch | Aantal waarden <br/> Decimaal \| Decimalen: 0 |

{style="table-layout:fixed"}


## Metagegevens van element

| Titel | Beschrijving | Type | Instellingen |
|---|---|---|---|
| Source-element | Openbare toegankelijke bron-URL voor het element. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Element-id | Unieke id van het element. Het binaire element bepaalt de uniciteit. Als het element binair verandert, verandert identiteitskaart wel. De unieke id kan de URL zijn, maar ook een gemaakte hash. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Elementnaam | Naam van het element. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Elementtype | Type van het element. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| URL van elementminiatuur | URL voor de miniatuur van het element. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| HTML-pad voor element | Samengevoegd HTML-pad voor het element. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Koppelings-URL voor element | Naaste paginanker voor het element. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Breedte van middelenweergave | Weergavebreedte van inhoudselementen. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Hoogte van bedrijfsmiddelenweergave | Hoogte van weergave van inhoudselementen. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Absoluut linkerelement | Content asset absolute left. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Absoluut bovenaan | Absolute top inhoudselement. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Element gemaakt door | Identifier voor het maken van elementen. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Aanmaakdatum van element | Aanmaakdatum van element. | Dimension | Recentste \| Sessie |
| Element laatst bijgewerkt door | Id voor bijwerken van element. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Laatste bijgewerkte datum van element | Datum van update van element. | Dimension | Recentste \| Sessie |

{style="table-layout:fixed"}


## Elementkenmerken

| Titel | Beschrijving | Type | Instellingen |
|---|---|---|---|
| Elementrichting | ![ AI produceerde ](/help/assets/icons/AI.svg) Richtlijn van de activa. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Totale hoeveelheid element | ![ AI produceerde ](/help/assets/icons/AI.svg) Algemene toon van de activa. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Voorgrondkleuren van element | ![ AI produceerde ](/help/assets/icons/AI.svg) Voorgrondkleuren van de activa. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Achtergrondkleur van element | ![ AI produceerde ](/help/assets/icons/AI.svg) Achtergrondkleuren van de activa. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Elementlabels | ![ AI produceerde ](/help/assets/icons/AI.svg) Markeringen voor de activa. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Elementen | ![ AI produceerde ](/help/assets/icons/AI.svg) Scènes voor de activa. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Elementobjecten | ![ AI produceerde ](/help/assets/icons/AI.svg) Voorwerpen van de activa. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Elementfotografie | ![ AI produceerde ](/help/assets/icons/AI.svg) de stijlen van de Fotografie van de activa. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Afbeeldingstype element | ![ AI produceerde ](/help/assets/icons/AI.svg) Type van Beeld van de activa. Mogelijke waarden zijn: foto, schets, verven, digital_cartoon, infographics, graphic_design, collage en software_screenshot. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Elementcameraposities | ![ AI produceerde ](/help/assets/icons/AI.svg) posities van de Camera van de activa. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Middelen cameranabijheid | ![ AI produceerde ](/help/assets/icons/AI.svg) nabijheden van de Camera van de activa. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Categorieën personen | ![ AI produceerde ](/help/assets/icons/AI.svg) categorieën van Mensen voor de activa. Mogelijke waarden zijn: persoon, man, vrouw, sociale groep, menigte, mensen, jongen, meisje en kind. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Dichtheid van visuele elementen | ![ AI produceerde ](/help/assets/icons/AI.svg) Visuele inhoudsdichtheid van de activa. Mogelijke waarden zijn: laag, normaal of hoog. Een lage inhoudsdichtheid betekent dat er een kleine hoeveelheid informatie aanwezig is per oppervlakte-eenheid van de afbeelding. | Dimension | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Asset Visual Attached Spread | ![ AI produceerde ](/help/assets/icons/AI.svg) Visuele aandachtsspreiding van de activa. Mogelijke waarden zijn: laag, normaal of hoog. De spreiding van de aandacht heeft betrekking op de mate waarin de aandacht van een kijker tussen verschillende delen van een beeld wordt verdeeld. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Belichtingsvoorwaarde voor element | ![ AI produceerde ](/help/assets/icons/AI.svg) Verlichtingsvoorwaarde van de activa. Mogelijke waarden zijn: golden hour, blue hour, midday, overcast, night, high key, low key, daylighting, incandescent, fluorescerend, kleurrijk en studio. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |
| Instelling van camera-elementen | ![ AI produceerde ](/help/assets/icons/AI.svg) het plaatsen van de Camera van de activa. Mogelijke waarden zijn: snelle sluitersnelheid, lange belichting. Bokeh-vervaging, bewegingsvervaging, vervaging met kantelen, flash, groothoek, zwart-wit, surrealistisch, dubbele belichting, macro en normale modus. | Dimension <br/> Afgeleid Gebied | \| tonen Geen waarde <br/> Recentste \| Sessie |

{style="table-layout:fixed"}


## Gebeurtenissen van Asset

| Titel | Beschrijving | Type | Instellingen |
|---|---|---|---|
| Elementweergaven | Kwantificeerbare waarde van het aantal weergaven van het actief. | Metrisch | Aantal waarden <br/> Decimaal \| Decimalen: 0 |
| Elementklikken | Kwantificeerbare maatstaf voor het aantal klikken op het actief. | Metrisch | Aantal waarden <br/> Decimaal \| Decimalen: 0 |

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

| Titel | Beschrijving | Type | Instellingen |
|---|---|---|---|
| Middelen klikken-dalingssnelheid | Elementklikken/Elementweergaven | Berekende metrische waarde | |
| ervaringsdoorkliksnelheid | Ervaar klikken/Weergaven ervaren | Berekende metrische waarde | |

{style="table-layout:fixed"}

