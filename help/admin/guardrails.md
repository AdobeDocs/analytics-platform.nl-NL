---
title: Customer Journey Analytics Guardrails
description: Meer informatie over de Guardrails voor Customer Journey Analytics
solution: Customer Journey Analytics
feature: Administration
role: Admin
exl-id: f093ac54-7d31-449b-a441-a65856a1d535
source-git-commit: d6837178bccc1a80130ec3fc282d2b44858d06b1
workflow-type: tm+mt
source-wordcount: '1519'
ht-degree: 5%

---

# Customer Journey Analytics Guardrails

Dit document bevat limieten voor verschillende componenten van Customer Journey Analytics. Zie voor instructies, bereikparameters en rechten de optie [Productbeschrijving voor Customer Journey Analytics](https://helpx.adobe.com/legal/product-descriptions/customer-journey-analytics.html) of de [Productbeschrijving voor Adobe Analytics Add-on: Customer Journey Analytics](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics-addon-customer-journey-analytics.html).

## Limiettypen

Dit document bevat twee typen standaardlimieten:

| Het type Guardrail | Beschrijving |
|----------|---------|
| **Prestatiehulplijnen (zachte limiet)** | Prestatiehandleidingen zijn gebruikslimieten die betrekking hebben op het bereik van uw gebruiksgevallen. Bij het overschrijden van de prestatiesGrafieken, kunt u prestatiesdegradatie en latentie ervaren. Adobe is niet verantwoordelijk voor een dergelijke verslechtering van de prestaties. Klanten die een prestatiehandleiding consequent overschrijden, kunnen ervoor kiezen om extra capaciteit in licentie te geven om een verslechtering van de prestaties te voorkomen. |
| **Door het systeem afgedwongen geleiding (harde limiet)** | Systeem-afgedwongen Guardrails worden afgedwongen door de Customer Journey Analytics UI of API. Dit zijn grenzen die u niet kunt overschrijden aangezien UI en API u verhindert dit te doen of een fout terugkeert. |

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
| Deelvensters per project | 15 | Door het systeem afgedwongen Guardrail | Maximum aantal [deelvensters](../analysis-workspace/home.md#panels) per project. |
| Visualisaties per deelvenster | 25 | Door het systeem afgedwongen Guardrail | Maximum aantal [visualisaties](../analysis-workspace/home.md#visualizations) per deelvenster. |
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
| Auditiefilters | 20 | Door het systeem afgedwongen Guardrail | Maximum aantal [filters](../components/filters/filters-overview.md) per publiek. |
| Aantal publieksidentiteiten | 20 miljoen | Door het systeem afgedwongen Guardrail | Maximumaantal identiteiten per publiek. |
| Frequentie van publiek vernieuwen | 4 | Door het systeem afgedwongen Guardrail | Maximale frequentie in uren en [publiek](../components/audiences/audiences-overview.md) kan worden vernieuwd. |
| Het publiek vernieuwt het terugkijkvenster | 90 | Door het systeem afgedwongen Guardrail | Maximumaantal dagen voor vernieuwen terugzoekvenster. |
| Vernieuwende vervaldatum van het publiek | 13 | Door het systeem afgedwongen Guardrail | Het maximumaantal maanden dat het publiek vanaf de aanmaakdatum mag vernieuwen. Klanten kunnen dit met nog eens 13 maanden verlengen. |
| Aantal verfrissende soorten publiek | 75 100 | Door het systeem afgedwongen Guardrail | Het maximale aantal verfrissende soorten publiek. De waarde hangt af van het pakket (zie Productbeschrijving). |

{style="table-layout:auto"}

Zie ook Experience Platform [Real-time Customer Data Platform Guardrails](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=en).


## Vervaldatum automatische gegevensset

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|:---:|
| Werkorders | 20 | Door het systeem afgedwongen Guardrail | Maximum aantal automatische gegevensset vervalwerkorders per maand. |

{style="table-layout:auto"}



## Verbindingen, de meningen van Gegevens, Projecten

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Projecten | 2.000 | Door het systeem afgedwongen Guardrail | Maximumaantal projecten voor een organisatie. |
| Gegevens weergeven | 2.000 | Door het systeem afgedwongen Guardrail | Maximum aantal [gegevensweergaven](../data-views/data-views.md) voor een organisatie. |
| Gegevens weergeven | 50 | Door het systeem afgedwongen Guardrail | Maximumaantal gegevensweergaven voor een verbinding |
| Gegevenssets | 100 | Door het systeem afgedwongen Guardrail | Maximum aantal [gegevenssets](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=en) per verbinding. |
| Verbindingen | 1000 | Door het systeem afgedwongen Guardrail | Maximum aantal [verbindingen](../connections/overview.md) voor een organisatie. |
| Verbindingstitel | 500 | Door het systeem afgedwongen Guardrail | Maximum aantal tekens voor een verbindingstitel. |
| Metrics | 5.000 | Door het systeem afgedwongen Guardrail | Maximum aantal metriek in een gegevensmening. |
| Dimensies | 5.000 | Door het systeem afgedwongen Guardrail | Maximumaantal afmetingen in een gegevensweergave. |
| Titel aantekening | 100 | Door het systeem afgedwongen Guardrail | Maximum aantal tekens voor een titel van een aantekening. |
| Beschrijving van aantekening | 250 | Door het systeem afgedwongen Guardrail | Maximumaantal tekens voor een beschrijving van een aantekening. |
| Schema-velden | 10 | Door het systeem afgedwongen Guardrail | Maximumaantal schemavelden (exclusief standaardvelden) bij het definiëren van regels voor een [afgeleid veld](../data-views/derived-fields/derived-fields.md). |
| Opzoeken/profielvelden | 3 | Door het systeem afgedwongen Guardrail | Maximumaantal velden voor opzoekopdrachten of profielschema&#39;s binnen het maximumaantal schemavelden (exclusief standaardvelden) bij het definiëren van regels voor een afgeleid veld. |
| Afgeleide velden | 100 | Door het systeem afgedwongen Guardrail | Maximumaantal afgeleide velden per verbinding. |

{style="table-layout:auto"}


## Gegevensoverdrachtlimieten

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Velden | 10.000 | Door het systeem afgedwongen Guardrail | Maximumaantal eigenschappen of velden per rij in een gegevensset. |
| Unieke tekenreeksen | 10 miljoen | Door het systeem afgedwongen Guardrail | Maximum aantal unieke sleutels per raadplegingsdataset. |
| Rijen | 1 miljoen | Door het systeem afgedwongen Guardrail | Maximum aantal rijen per unieke persoon-id binnen een verbinding. |
| Rijgrootte | 2 | Prestatiehandleiding / door het systeem afgedwongen geleider | Gemiddelde grootte in kilobytes per rij gegevens die in Customer Journey Analytics worden opgenomen (zachte limiet). Een statische limiet voor de rijgrootte wordt bepaald door de instructies voor het opnemen van gegevens in het Experience Platform. |

{style="table-layout:auto"}

Zie ook Experience Platform [Guardrails voor gegevensinname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/guardrails.html?lang=en).


## Gegevenslandingszone

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Gegevenslandingszone per sandbox | 1 | Door het systeem afgedwongen Guardrail | Maximumaantal landingszones voor gegevens per sandbox. |
| Gegevensopslag | 7 | Door het systeem afgedwongen Guardrail | Het maximale aantal dagen dat gegevens worden opgeslagen in de gegevenslandingszone voordat ze worden verwijderd. |

{style="table-layout:auto"}


## Veldgebaseerde stitching

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Datasets met titels | 10 | Door het systeem afgedwongen Guardrail | Het maximum aantal gebonden gegevenssets per klant. De waarde hangt af van het toepasselijke pakket Customers Journey Analytics (zie de toepasselijke productbeschrijving). |
| Backfill-gegevens | 60 | Door het systeem afgedwongen Guardrail | Maximumaantal dagen met back-upgegevens. |

{style="table-layout:auto"}


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
| Gegevensblokken | 1000 | Door het systeem afgedwongen Guardrail | Maximum aantal [gegevensblokken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-reportbuilder/manage-reportbuilder.html?lang=en) per werkboek. |
| Metrics | 20 | Door het systeem afgedwongen Guardrail | Maximum aantal metriek per gegevensblok. |
| Datumbereik | 13 | Door het systeem afgedwongen Guardrail | Het maximum aantal maanden dat een datumbereik kan beslaan per gegevensblok. |
| Rijen | 50.000 | Door het systeem afgedwongen Guardrail | Maximumaantal rijen per gegevensblok. |

{style="table-layout:auto"}


## Volledige tabelexport

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Rijen per rapport | 3 miljoen - 300 miljoen | Door het systeem afgedwongen Guardrail | Maximum aantal rapportrijen per rapport; de waarde varieert afhankelijk van het toepasselijke pakket van de Customer Journey Analytics (zie toepasselijke productbeschrijving). |
| Uitsplitsingen per tabel | 5 | Door het systeem afgedwongen Guardrail | Maximumaantal uitsplitsingen per tabel. |
| Metrisch per tabel | 5 | Door het systeem afgedwongen Guardrail | Maximum aantal metriek per lijst. |
| Planningsfrequentie | 1 | Door het systeem afgedwongen Guardrail | De uitvoer kan één keer (1) per dag of op een langer programma (bijvoorbeeld: eens om de 2 dagen, of wekelijks) worden gepland. |

{style="table-layout:auto"}

## Latenties

>[!NOTE]
>
>De verwerkingstijden hieronder zijn Guardrails, niet contractuele service level agreements (SLA&#39;s). De latentie is afhankelijk van de configuratie van de klant, de gegevensvolumes en de toepassingen van de consument. Echte verwerkingstijden zijn vaak sneller. Verwijs naar uw contract van de Customer Journey Analytics voor uw specifieke contractvoorwaarden en SLAs. Zie Experience Platform [Guardrails voor gegevensinname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/Guardrails.html?lang=en) voor meer informatie .

| Gegevensstroom | Verwachte vertraging |
|---|---|
| Adobe Analytics naar Adobe Analytics Source Connector (A4T ingeschakeld) | &lt; 30 minuten |
| Adobe Analytics Source Connector to Real-time Customer Profile (A4T niet ingeschakeld) | &lt; 2 minuten |
| Adobe Analytics Source Connector voor Real-time klantprofiel (A4T ingeschakeld) | &lt; 30 minuten |
| Gegevensinsluiting in Data Lake van Edge Network of Streaming Ingestie | &lt; 60 minuten |
| Gegevensinname in Data Lake van Adobe Analytics Source Connector | &lt; 2,25 uur |
| Gegevensinname in Customer Journey Analytics van Data Lake | &lt; 90 minuten |
| Plaatsen (optionele functie; zie [Overzicht van tekenreeksen](../stitching/overview.md) voor meer informatie ) | &lt; 3,25 uur |
| Adobe Analytics Source Connector Backfill van minder dan 10 miljard gebeurtenissen (maximaal 13 maanden historische gegevens) | &lt; 4 weken |
| Publiceren van het publiek aan het Profiel van de Klant in real time, met inbegrip van automatische verwezenlijking van het het stromen segment, en het toestaan van het segment klaar om de gegevens te ontvangen. | staan voor 60 minuten |
| Frequentie vernieuwen voor publiek | Eenmalige vernieuwing: latentie van minder dan 5 minuten.<br/>Vernieuw elke 4 uur, dagelijks, wekelijks, maandelijks (latentie gaat hand in hand met de vernieuwingsfrequentie). |

{style="table-layout:auto"}
