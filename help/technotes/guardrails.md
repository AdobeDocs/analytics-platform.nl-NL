---
title: Customer Journey Analytics Guardrails
description: Meer informatie over de Guardrails voor Customer Journey Analytics
solution: Customer Journey Analytics
feature: Administration
role: Admin
exl-id: f093ac54-7d31-449b-a441-a65856a1d535
source-git-commit: a80b20eb2e0395445e8f2e7fd0e76e2eef40522a
workflow-type: tm+mt
source-wordcount: '1760'
ht-degree: 5%

---

# Customer Journey Analytics Guardrails

Dit document bevat limieten voor verschillende componenten van Customer Journey Analytics. Voor Guardrails, Scoping Parameters, en Entitlements, zie de [ Beschrijving van het Product voor Customer Journey Analytics ](https://helpx.adobe.com/legal/product-descriptions/customer-journey-analytics.html) of de [ Beschrijving van het Product voor toe:voegen-op Adobe Analytics: Customer Journey Analytics ](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics-addon-customer-journey-analytics.html).

## Limiettypen

Dit document bevat twee typen standaardlimieten:

| Het type Guardrail | Beschrijving |
|----------|---------|
| **Guardrails van Prestaties (zachte grens)** | Prestatiehandleidingen zijn gebruikslimieten die betrekking hebben op het bereik van uw gebruiksgevallen. Bij het overschrijden van de prestatiesGrafieken, kunt u prestatiesdegradatie en latentie ervaren. Adobe is niet verantwoordelijk voor een dergelijke verslechtering van de prestaties. Klanten die een prestatiehandleiding consequent overschrijden, kunnen ervoor kiezen om extra capaciteit in licentie te geven om een verslechtering van de prestaties te voorkomen. |
| **systeem-afgedwongen Guardrails (harde grens)** | Systeem-afgedwongen Guardrails worden afgedwongen door de Customer Journey Analytics UI of API. Dit zijn grenzen die u niet kunt overschrijden aangezien UI en API u verhindert dit te doen of een fout terugkeert. |

{style="table-layout:auto"}

Sommige eigenschappen en hun bijbehorende waarde voor de grens hangen van het Pakket van de Customer Journey Analytics af u aan gemachtigd bent.

>[!NOTE]
>
>De waarden die in dit document worden beschreven, kunnen worden gewijzigd op basis van voortdurende verbeteringen in het product. Controleer regelmatig of er updates zijn. Als u meer wilt weten over aangepaste limieten, neemt u contact op met uw medewerker van de klantenservice.

## Ad-hoc SQL-query&#39;s

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Time-out voor opnieuw proberen | 90 | Door het systeem afgedwongen Guardrail | Het maximum aantal seconden voordat de meldingsengine reageert, duurt het te lang om de resultaten te retourneren (mogelijk vanwege andere gelijktijdige andere verzoeken). U kunt opnieuw een aanvraag indienen. |
| Time-out niet opnieuw proberen | 600 | Door het systeem afgedwongen Guardrail | Maximum aantal seconden voordat Ad hoc SQL time-out opvraagt. Anders vermeld, het maximumaantal seconden alvorens de motoren meldt terug dat het verzoek te lang heeft geduurd om resultaten terug te keren, en zou niet opnieuw moeten worden geprobeerd. De aanvraag retourneert waarschijnlijk nooit resultaten vanwege problemen in het achtergrondproces. |
| Metrics | 150 | Door het systeem afgedwongen Guardrail | Maximum aantal metriek in een verzoek. |
| Interactieve rijen voor query-uitvoer | 50.000 | Door het systeem afgedwongen Guardrail | Standaardaantal geretourneerde rijen, tenzij anders aangegeven. |

{style="table-layout:auto"}

## Analysis Workspace-projecten

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Zichtbare rijen per tabel | 400 | Door het systeem afgedwongen Guardrail | Maximum aantal zichtbare rijen in om het even welke vrije vormlijst in een project van Analysis Workspace. |
| Geëxporteerde rijen per tabel | 50.000 | Door het systeem afgedwongen Guardrail | Maximumaantal rijen dat per enkele afmeting kan worden geëxporteerd. |
| Deelvensters per project | 15 | Door het systeem afgedwongen Guardrail | Maximum aantal [ panelen ](../analysis-workspace/home.md#panels) per project. |
| Visualisaties per deelvenster | 25 | Door het systeem afgedwongen Guardrail | Maximum aantal [ visualisaties ](../analysis-workspace/home.md#visualizations) per paneel. |
| Afgeleide velden per vrije-vormtabel | 5 | Door het systeem afgedwongen Guardrail | Maximum aantal verschillende afgeleide gebieden in één enkele vrije vormlijst. |

{style="table-layout:auto"}

<!--
## Attribution AI

| Name |  Value | Description | PD? |
|---|--:|---|:---:|
| Attribution AI models | 35 | Maximum number of Attribution AI Model per year to analyze the impact of up to an average of 60 independent touchpoints on a specified conversion event.  | ![check](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg)  | 
| Region based iterations | 10 | Maximum number of region-based iterations of each Attribution AI model. | ![check](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg)  | 
| Export Insights batches | 12 | Maximum number of export batches times the number of authorized Attribution AI Insights per year. | ![check](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg) | 

{style="table-layout:auto"}
-->

## Soorten publiek

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Auditiefilters | 20 | Door het systeem afgedwongen Guardrail | Maximum aantal [ filters ](../components/filters/filters-overview.md) per publiek. |
| Aantal identiteiten publiek | 20 miljoen | Door het systeem afgedwongen Guardrail | Maximumaantal identiteiten per publiek. |
| Frequentie van publiek vernieuwen | 4 | Door het systeem afgedwongen Guardrail | Maximale frequentie in uren een [ publiek ](../components/audiences/audiences-overview.md) kan worden verfrist. |
| Venster Opzoeken vernieuwen | 90 | Door het systeem afgedwongen Guardrail | Maximumaantal dagen voor vernieuwen terugzoekvenster. |
| Vernieuwende vervaldatum van het publiek | 13 | Door het systeem afgedwongen Guardrail | Het maximumaantal maanden dat het publiek vanaf de aanmaakdatum mag vernieuwen. Klanten kunnen dit met nog eens 13 maanden verlengen. |
| Aantal verfrissende soorten publiek | 75 150 | Door het systeem afgedwongen Guardrail | Maximumaantal verfrissende doelgroepen. De waarde varieert afhankelijk van het Customer Journey Analytics pakket (zie de Beschrijving van het Product). |

{style="table-layout:auto"}

Zie ook Experience Platform [ Real-time Customer Data Platform Guardrails ](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html).


## Vervaldatum automatische gegevensset

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|:---:|
| Werkorders | 20 | Door het systeem afgedwongen Guardrail | Maximum aantal automatische gegevensset vervalwerkorders per maand. |

{style="table-layout:auto"}



## Verbindingen, de meningen van Gegevens, Projecten

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Projecten | 50.000 | Door het systeem afgedwongen Guardrail | Maximumaantal projecten voor een organisatie. |
| Gegevens weergeven | 2.000 | Door het systeem afgedwongen Guardrail | Maximum aantal [ gegevensmeningen ](../data-views/data-views.md) voor een organisatie. |
| Gegevens weergeven | 500 - 1000 | Door het systeem afgedwongen Guardrail | Maximumaantal gegevensweergaven voor een verbinding. De waarde varieert afhankelijk van het Customer Journey Analytics pakket (zie de Beschrijving van het Product). |
| Gegevenssets | 100 | Door het systeem afgedwongen Guardrail | Maximum aantal [ datasets ](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html) per verbinding. |
| Verbindingen | 1000 | Door het systeem afgedwongen Guardrail | Maximum aantal [ verbindingen ](../connections/overview.md) voor een organisatie. |
| Verbindingstitel | 500 | Door het systeem afgedwongen Guardrail | Maximum aantal tekens voor een verbindingstitel. |
| Metrics | 5.000 | Door het systeem afgedwongen Guardrail | Maximum aantal metriek in een gegevensmening. |
| Dimensies | 5.000 | Door het systeem afgedwongen Guardrail | Maximumaantal afmetingen in een gegevensweergave. |
| Titel aantekening | 100 | Door het systeem afgedwongen Guardrail | Maximum aantal tekens voor een titel van een aantekening. |
| Beschrijving van aantekening | 250 | Door het systeem afgedwongen Guardrail | Maximumaantal tekens voor een beschrijving van een aantekening. |
| Schema-velden | 10 | Door het systeem afgedwongen Guardrail | Maximum aantal schemagebieden (zonder standaardgebieden) wanneer het bepalen van regels voor a [ afgeleid gebied ](../data-views/derived-fields/derived-fields.md). |
| Opzoeken/profielvelden | 3 | Door het systeem afgedwongen Guardrail | Maximumaantal velden voor opzoekopdrachten of profielschema&#39;s binnen het maximumaantal schemavelden (exclusief standaardvelden) bij het definiëren van regels voor een afgeleid veld. |
| Afgeleide velden | 100 - 500 | Door het systeem afgedwongen Guardrail | Maximumaantal afgeleide velden per verbinding. De waarde varieert afhankelijk van het Customer Journey Analytics pakket (zie de Beschrijving van het Product). |

{style="table-layout:auto"}


## Gegevensoverdrachtlimieten

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Velden | 10.000 | Door het systeem afgedwongen Guardrail | Maximumaantal eigenschappen of velden per rij in een gegevensset. |
| Unieke tekenreeksen | 10 miljoen | Door het systeem afgedwongen Guardrail | Maximum aantal unieke sleutels per raadplegingsdataset. |
| Rijen | 1 miljoen | Door het systeem afgedwongen Guardrail | Maximum aantal rijen per unieke persoon-id in een bepaalde maand binnen een verbinding. |
| Rijgrootte | 2 | Prestatiehandleiding / door het systeem afgedwongen geleider | Gemiddelde grootte in kilobytes per rij gegevens die in Customer Journey Analytics worden opgenomen (zachte limiet). Een statische limiet voor de rijgrootte wordt bepaald door de instructies voor het opnemen van gegevens in het Experience Platform. |

{style="table-layout:auto"}

Zie ook Experience Platform [ Guardrails voor de Ingestie van Gegevens ](https://experienceleague.adobe.com/docs/experience-platform/ingestion/guardrails.html).


## Doelgegevens exporteren

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Gegevens exporteren | Totaal toegestane gegevensmeeropslag | Prestatiehandleiding | De klant kan de Uitvoer van de Dataset van de Bestemming gebruiken om de Gegevens van de Klant in het meer van Gegevens tot de Totale Erkende Opslag van Gegevens uit te voeren. |
| Beschikbare gegevensbestanden | Profiel en gebeurtenis | Systeem geforceerde geleider | De datasets van de gebeurtenis, van het Profiel of van de Opzoeken die in de UI van het Experience Platform na het opnemen van of het verzamelen van gegevens door Bronnen, Web SDK, Mobiele SDK, de Verbinding van Gegevens van de Analyse, en Audience Manager worden gecreeerd. |

{style="table-layout:auto"}

Zie ook Experience Platform [ Guardrails van de Uitvoer van de Dataset ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/guardrails#dataset-exports)


## Gegevenslandingszone

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Gegevenslandingszone per sandbox | 1 | Door het systeem afgedwongen Guardrail | Maximumaantal landingszones voor gegevens per sandbox. |
| Gegevensopslag | 7 | Door het systeem afgedwongen Guardrail | Het maximale aantal dagen dat gegevens worden opgeslagen in de gegevenslandingszone voordat ze worden verwijderd. |

{style="table-layout:auto"}


## Veldgebaseerde stitching

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Datasets met titels | 5 - 50 | Door het systeem afgedwongen Guardrail | Maximum aantal gestikte datasets per klant. De waarde varieert afhankelijk van het Customer Journey Analytics pakket (zie de Beschrijving van het Product). |
| Lengte achtergrondvulling | 6 - 25 | Door het systeem afgedwongen Guardrail | Maximumaantal maanden back-upgegevens. De waarde varieert afhankelijk van het Customer Journey Analytics pakket (zie de Beschrijving van het Product). |
| Frequentie voor terugzoeken/opnieuw afspelen | 01-30-7 | Door het systeem afgedwongen Guardrail | Maximum terugkijkvenster in dagen/Replay frequentie. De waarde varieert afhankelijk van het Customer Journey Analytics pakket (zie de Beschrijving van het Product). |

{style="table-layout:auto"}


## Op grafiek gebaseerde stitching

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Datasets met titels | 10 - 50 | Door het systeem afgedwongen Guardrail | Maximum aantal gestikte datasets per klant. De waarde varieert afhankelijk van het Customer Journey Analytics pakket (zie de Beschrijving van het Product). |
| Lengte achtergrondvulling | 13 - 25 | Door het systeem afgedwongen Guardrail | Maximumaantal maanden back-upgegevens. De waarde varieert afhankelijk van het Customer Journey Analytics pakket (zie de Beschrijving van het Product). |
| Frequentie voor terugzoeken/opnieuw afspelen | 01-30-7 | Door het systeem afgedwongen Guardrail | Maximum terugkijkvenster in dagen/Replay frequentie. De waarde varieert afhankelijk van het Customer Journey Analytics pakket (zie de Beschrijving van het Product). |


## Filters en berekende metriek

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Containers per filter | 50 | Door het systeem afgedwongen Guardrail | Maximumaantal containers per filter. |
| Metrisch per berekend metrisch | 25 | Door het systeem afgedwongen Guardrail | Maximum aantal metriek per berekende metrisch. |
| Metriek en Dimensionen per filter | 25 | Door het systeem afgedwongen Guardrail | Maximumaantal unieke metingen en afmetingen per filter. |
| Geneste containers per filter | 10 | Door het systeem afgedwongen Guardrail | Maximumaantal geneste containers per filter. |
| Regels per filter | 100 | Door het systeem afgedwongen Guardrail | Maximumaantal regels per filter. |
| Tekenreeks vergelijkt per Dimension per filter | 100 | Door het systeem afgedwongen Guardrail | Maximum aantal tekenreeksvergelijkingen per afmeting per filter. |
| Berekende standaarden | 6.000 | Door het systeem afgedwongen Guardrail | Maximumaantal berekende metriek voor een organisatie. |
| Filters | 50.000 | Door het systeem afgedwongen Guardrail | Maximumaantal filters dat u voor een organisatie kunt definiëren. |
| API-aanroepen | 120 | Door het systeem afgedwongen Guardrail | API-aanvragen per minuut (12 aanvragen om de 6 seconden). |

{style="table-layout:auto"}


## Mobiele toepassing

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Tegels | 16 | Door het systeem afgedwongen Guardrail | Maximumaantal tegels per scorecard. |
| Filters | 10 | Door het systeem afgedwongen Guardrail | Maximumaantal filters per scorecard. |
| Dimensies | 10 | Door het systeem afgedwongen Guardrail | Maximumaantal dimensies per scorecard. |

{style="table-layout:auto"}

## Report Builder

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Bestandsgrootte werkboek | 5 | Door het systeem afgedwongen Guardrail | Maximale bestandsgrootte in MB van een gepland werkboek. |
| Gegevensblokken | 1000 | Door het systeem afgedwongen Guardrail | Maximum aantal [ gegevensblokken ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-reportbuilder/manage-reportbuilder.html) per werkboek. |
| Metrics | 20 | Door het systeem afgedwongen Guardrail | Maximum aantal metriek per gegevensblok. |
| Datumbereik | 13 | Door het systeem afgedwongen Guardrail | Het maximum aantal maanden dat een datumbereik kan beslaan per gegevensblok. |
| Rijen | 50.000 | Door het systeem afgedwongen Guardrail | Maximumaantal rijen per gegevensblok. |

{style="table-layout:auto"}


## Volledige tabelexport

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Rijen per rapport | 3 miljoen - 300 miljoen | Door het systeem afgedwongen Guardrail | Maximumaantal rapportrijen per rapport. De waarde varieert afhankelijk van het Customer Journey Analytics pakket (zie de Beschrijving van het Product). |
| Uitsplitsingen per tabel | 5 | Door het systeem afgedwongen Guardrail | Maximumaantal uitsplitsingen per tabel. |
| Metrisch per tabel | 5 | Door het systeem afgedwongen Guardrail | Maximum aantal metriek per lijst. |
| Planningsfrequentie | 1 | Door het systeem afgedwongen Guardrail | De uitvoer kan één keer (1) per dag of op een langer programma (bijvoorbeeld: eens om de 2 dagen, of wekelijks) worden gepland. |

{style="table-layout:auto"}

## Latenties

>[!NOTE]
>
>De verwerkingstijden hieronder zijn Guardrails, niet contractuele service level agreements (SLA&#39;s). De latentie is afhankelijk van de configuratie van de klant, de gegevensvolumes en de toepassingen van de consument. Echte verwerkingstijden zijn vaak sneller. Verwijs naar uw contract van de Customer Journey Analytics voor uw specifieke contractvoorwaarden en SLAs. Zie Experience Platform [ Grafieken voor de Ingestie van Gegevens ](https://experienceleague.adobe.com/docs/experience-platform/ingestion/guardrails.html) voor meer informatie.

| Gegevensstroom | Verwachte vertraging |
|---|---|
| Adobe Analytics naar Adobe Analytics Source Connector (A4T ingeschakeld) | &lt; 30 minuten |
| Adobe Analytics Source Connector voor realtime klantprofiel (A4T niet ingeschakeld) | &lt; 2 minuten |
| Adobe Analytics Source Connector voor realtime klantprofiel (A4T ingeschakeld) | &lt; 30 minuten |
| Gegevensinsluiting in Data Lake van Edge Network- of streaming inscriptie | &lt; 60 minuten |
| Gegevensinname in Data Lake vanaf Adobe Analytics Source Connector | &lt; 2,25 uur |
| Gegevensinname in Customer Journey Analytics van Data Lake | &lt; 90 minuten |
| Stitching (facultatieve eigenschap; zie [ Stitching overzicht ](../stitching/overview.md) voor meer informatie) | &lt; 3,25 uur |
| Adobe Analytics Source Connector Backfill van minder dan 10 miljard gebeurtenissen (maximaal 13 maanden historische gegevens) | &lt; 4 weken |
| Publiceren van het publiek aan het Profiel van de Klant in real time, met inbegrip van automatische verwezenlijking van het het stromen segment, en het toestaan van het segment klaar om de gegevens te ontvangen. | staan voor 60 minuten |
| Frequentie vernieuwen voor publiek | Eenmalige vernieuwing: latentie van minder dan 5 minuten.<br/> verfrist zich om de 4 uren, dag, wekelijks, maandelijks (de latentie gaat hand in hand met verfrist tarief). |

{style="table-layout:auto"}
