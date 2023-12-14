---
title: Customer Journey Analytics Guardrails
description: Meer informatie over de trails, statische limieten, prestatiebewaking, bereikparameters en rechten voor Customer Journey Analytics
solution: Customer Journey Analytics
feature: Administration
role: Admin
hide: true
hidefromtoc: true
source-git-commit: 60c3b05778c8bb097dba691bb591ab50121da6bb
workflow-type: tm+mt
source-wordcount: '1489'
ht-degree: 5%

---


# Customer Journey Analytics Guardrails

Dit document bevat limieten voor verschillende componenten van Customer Journey Analytics. Zie voor instructies, bereikparameters en rechten de [Productbeschrijving voor Customer Journey Analytics](https://helpx.adobe.com/legal/product-descriptions/customer-journey-analytics.html) of de [Productbeschrijving voor Adobe Analytics Add-on: Customer Journey Analytics](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics-addon-customer-journey-analytics.html).

## Limiettypen

Dit document bevat twee typen standaardlimieten:

| Het type Guardrail | Beschrijving |
|----------|---------|
| **Prestatiegerichten (zachte limiet)** | Prestatiegaranties zijn gebruikslimieten die betrekking hebben op het bereik van uw gebruiksgevallen. Als u de prestatiegaranties overschrijdt, kan de prestaties achteruitgaan en de latentie vertragen. Adobe is niet verantwoordelijk voor een dergelijke verslechtering van de prestaties. Klanten die een prestatiegarantie consequent overschrijden, kunnen ervoor kiezen om extra capaciteit te licentiëren om prestatievermindering te voorkomen. |
| **Door het systeem afgedwongen geleiding (harde limiet)** | De in het systeem afgedwongen grails worden afgedwongen door de Customer Journey Analytics UI of API. Dit zijn grenzen die u niet kunt overschrijden aangezien UI en API u zal tegenhouden dit te doen of een fout zal terugkeren. |

{style="table-layout:auto"}

Sommige functies en de bijbehorende waarde voor de limiet zijn afhankelijk van het Customer Journey Analytics-pakket waarop u recht hebt.

>[!NOTE]
>
>De waarden die in dit document worden beschreven, kunnen worden gewijzigd op basis van voortdurende verbeteringen in het product. Kom regelmatig terug voor updates. Als u meer wilt weten over aangepaste limieten, neemt u contact op met uw medewerker van de klantenservice.

## Ad hoc SQL-query&#39;s

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Opnieuw proberen | 90 | Door het systeem afgedwongen guardail | Het maximum aantal seconden voordat de meldingsengine reageert, duurt het te lang om de resultaten te retourneren (mogelijk vanwege andere gelijktijdige andere verzoeken). U kunt opnieuw een aanvraag indienen. | |
| Niet opnieuw proberen | 600 | Door het systeem afgedwongen guardail | Het maximum aantal seconden voordat Ad hoc SQL query&#39;s time-out hebben. Anders vermeld, maximumaantal seconden alvorens de rapporteringsmotoren terug melden dat het verzoek te lang heeft geduurd om resultaten terug te keren en niet opnieuw zou moeten worden geprobeerd aangezien het verzoek nooit resultaten wegens kwesties in het achtergrondproces zal terugkeren. |
| Metrics | 150 | Door het systeem afgedwongen guardail | Maximum aantal metriek in een verzoek. | | |
| Interactieve rijen voor query-uitvoer | 50.000 | Door het systeem afgedwongen guardail | Standaardaantal geretourneerde rijen, tenzij anders aangegeven. | |

{style="table-layout:auto"}

## Analysis Workspace-projecten

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Zichtbare rijen per tabel | 400 | Door het systeem afgedwongen guardail | Maximum aantal zichtbare rijen in om het even welke vrije vormlijst in een project van Analysis Workspace. | ![controleren](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg) | ![controleren](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg) |
| Uitgevoerde rijen per tabel | 50.000 | Door het systeem afgedwongen guardail | Maximumaantal rijen dat per enkele afmeting kan worden geëxporteerd. | ![controleren](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg) |
| Deelvensters per project | 15 | Door het systeem afgedwongen guardail | Maximum aantal [deelvensters](../analysis-workspace/home.md#panels) per project. | ![controleren](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg) |
| Visualisaties per deelvenster | 25 | Door het systeem afgedwongen guardail | Maximum aantal [visualisaties](../analysis-workspace/home.md#visualizations) per deelvenster. | ![controleren](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg) |

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
| Auditiefilters | 20 | Door het systeem afgedwongen guardail | Maximum aantal [filters](../components/filters/filters-overview.md) per publiek. |
| Aantal publieksidentiteiten | 20 miljoen | Door het systeem afgedwongen guardail | Maximumaantal identiteiten per publiek. |
| Vernieuwingsfrequentie publiek | 4 | Door het systeem afgedwongen guardail | Maximale frequentie in uren en [publiek](../components/audiences/audiences-overview.md) kan worden vernieuwd. | |
| Het publiek vernieuwt het terugkijkvenster | 90 | Door het systeem afgedwongen guardail | Maximumaantal dagen voor vernieuwen terugzoekvenster. |
| Vernieuwende vervaldatum van publiek | 13 | Door het systeem afgedwongen guardail | Het maximumaantal maanden dat het publiek kan vernieuwen vanaf de aanmaakdatum. Klanten hebben de mogelijkheid dit met nog eens 13 maanden te verlengen. |
| Aantal verfrissende soorten publiek | 75 100 150 | Door het systeem afgedwongen guardail | Het maximale aantal publiek dat wordt vernieuwd, de waarde is afhankelijk van het pakket. |

{style="table-layout:auto"}

Zie ook Experience Platform [Real-time Customer Data Platform guardrails](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=en).


## Vervaldatum automatische gegevensset

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|:---:|
| Werkorders | 20 | Door het systeem afgedwongen guardail | Maximum aantal automatische gegevensset vervalwerkorders per maand. |

{style="table-layout:auto"}



## Verbindingen, de meningen van Gegevens, Projecten

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Projecten | 2.000 | Door het systeem afgedwongen guardail | Maximumaantal projecten voor een organisatie. |
| Gegevensweergaven | 2.000 | Door het systeem afgedwongen guardail | Maximum aantal [gegevensweergaven](../data-views/data-views.md) voor een organisatie. |
| Gegevensweergaven | 50 | Door het systeem afgedwongen guardail | Maximumaantal gegevensweergaven voor een verbinding |
| Gegevenssets | 100 | Door het systeem afgedwongen guardail | Maximum aantal [gegevenssets](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=en) per verbinding. |
| Verbindingen | 1000 | Door het systeem afgedwongen guardail | Maximum aantal [verbindingen](../connections/overview.md) voor een organisatie. |
| Verbindingstitel | 500 | Maximum aantal tekens voor een verbindingstitel. |
| Metrics | 5.000 | Door het systeem afgedwongen guardail | Maximumaantal metriek in een gegevensweergave |
| Dimensies | 5.000 | Door het systeem afgedwongen guardail | Maximumaantal afmetingen in een gegevensweergave | |
| Titel aantekening | 100 | Door het systeem afgedwongen guardail | Maximum aantal tekens voor een titel van een aantekening. |
| Beschrijving van aantekening | 250 | Door het systeem afgedwongen guardail | Maximumaantal tekens voor een beschrijving van een aantekening. | |
| Schema-velden | 10 | Door het systeem afgedwongen guardail | Maximumaantal schemavelden (exclusief standaardvelden) bij het definiëren van regels voor een [afgeleid veld](../data-views/derived-fields/derived-fields.md). |
| Opzoeken/Profielvelden | 3 | Door het systeem afgedwongen guardail | Maximumaantal velden voor opzoekopdrachten of profielschema&#39;s binnen het maximumaantal schemavelden (exclusief standaardvelden) bij het definiëren van regels voor een afgeleid veld. |
| Afgeleide velden | 100 | Door het systeem afgedwongen guardail | Maximumaantal afgeleide velden per verbinding. |

{style="table-layout:auto"}


## Gegevensoverdrachtlimieten

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Velden | 10.000 | Door het systeem afgedwongen guardail | Maximumaantal eigenschappen of velden per rij in een gegevensset. | | |
| Unieke tekenreeksen | 10 miljoen | Door het systeem afgedwongen guardail | Maximum aantal unieke sleutels per raadplegingsdataset. |
| Rijen | 1 miljoen | Door het systeem afgedwongen guardail | Maximum aantal rijen per unieke persoon-id binnen een verbinding. |
| Rijgrootte | 2 | Prestatiegerichte / door het systeem afgedwongen geleiding | Gemiddelde grootte in kilobytes per rij gegevens die in Customer Journey Analytics worden opgenomen (zachte limiet). Een statische limiet voor de rijgrootte wordt bepaald door instructies voor gegevensinvoer in Experience Platform. |

{style="table-layout:auto"}

Zie ook Experience Platform [Guardrails voor gegevensinname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/guardrails.html?lang=en).


## Gegevenslandingszone

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Gegevenslandingszone per sandbox | 1 | Door het systeem afgedwongen guardail | Maximumaantal landingszones voor gegevens per sandbox. |
| Gegevensopslag | 7 | Door het systeem afgedwongen guardail | Het maximale aantal dagen dat gegevens worden opgeslagen in de gegevenslandingszone voordat ze worden verwijderd. |

{style="table-layout:auto"}


## Veldgebaseerde stitatie

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Vastgelegde gegevenssets | 10 | Door het systeem afgedwongen guardail | Maximum aantal gestippelde datasets per klant, afhankelijk van het pakket. |
| Backfill-gegevens | 60 | Door het systeem afgedwongen guardail | Maximumaantal dagen met back-upgegevens. |

{style="table-layout:auto"}


## Filters en berekende metriek

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Containers per filter | 50 | Door het systeem afgedwongen guardail | Maximumaantal containers per filter. |
| Metrisch per berekende metriek | 25 | Door het systeem afgedwongen guardail | Maximum aantal metriek per berekende metrisch. |
| Metriek en afmetingen per filter | 25 | Door het systeem afgedwongen guardail | Maximumaantal ongelijke meeteenheden en afmetingen per filter. |
| Geneste containers per filter | 10 | Door het systeem afgedwongen guardail | Maximumaantal geneste containers per filter. | ![controleren](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg) |
| Regels per filter | 100 | Door het systeem afgedwongen guardail | Maximumaantal regels per filter. |
| Tekenreeks vergelijkt per dimensie per filter | 100 | Door het systeem afgedwongen guardail | Maximum aantal tekenreeksvergelijkingen per afmeting per filter. |
| Berekende cijfers | 6.000 | Door het systeem afgedwongen guardail | Maximumaantal berekende metriek voor een organisatie. | |
| Filters | 50.000 | Door het systeem afgedwongen guardail | Maximumaantal filters dat u voor een organisatie kunt definiëren. |

{style="table-layout:auto"}


## Mobiele toepassing

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Tegels | 16 | Door het systeem afgedwongen guardail | Maximumaantal tegels per scorecard. |
| Filters | 10 | Door het systeem afgedwongen guardail | Maximumaantal filters per scorecard. |
| Dimensies | 10 | Door het systeem afgedwongen guardail | Maximumaantal dimensies per scorecard. |

{style="table-layout:auto"}

## Report Builder

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Bestandsgrootte werkboek | 5 | Door het systeem afgedwongen guardail | Maximale bestandsgrootte in MB van een gepland werkboek. |
| Gegevensblokken | 1000 | Door het systeem afgedwongen guardail | Maximum aantal [gegevensblokken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-reportbuilder/manage-reportbuilder.html?lang=en) per werkboek. |
| Metrics | 20 | Door het systeem afgedwongen guardail | Maximum aantal metriek per gegevensblok. |
| Datumbereik | 13 | Door het systeem afgedwongen guardail | Het maximum aantal maanden dat een datumbereik kan beslaan per gegevensblok. |  |
| Rijen | 50.000 | Door het systeem afgedwongen guardail | Maximumaantal rijen per gegevensblok. |

{style="table-layout:auto"}


## Volledige tabelexport

| Naam | Waarde | Limiettype | Beschrijving |
|---|--:|---|---|
| Rijen per rapport | 3 miljoen - 150 miljoen | Door het systeem afgedwongen guardail | Maximum aantal rapportrijen per rapport; waarde die op het vergunning gegeven pakket wordt gebaseerd. |
| Uitsplitsingen per tabel | 5 | Door het systeem afgedwongen guardail | Maximumaantal uitsplitsingen per tabel. |
| Metriek per tabel | 5 | Door het systeem afgedwongen guardail | Maximum aantal metriek per lijst. |
| Planningsfrequentie | 1 | Door het systeem afgedwongen guardail | De uitvoer kan één keer (1) per dag of op een langer programma (bijvoorbeeld: eens om de 2 dagen, of wekelijks) worden gepland. |

{style="table-layout:auto"}

## Latenties

>[!NOTE]
>
>De verwerkingstijden hieronder zijn garanties, niet contractuele overeenkomsten van het de dienstniveau (SLAs).  De latentie zal afhankelijk van klantenconfiguratie, gegevensvolumes, en de toepassingen van de consument variëren. Echte verwerkingstijden zullen vaak sneller zijn. Verwijs naar uw contract van de Customer Journey Analytics voor uw specifieke contractvoorwaarden en SLAs. Zie Experience Platform [Guardrails voor gegevensinname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/guardrails.html?lang=en) voor meer informatie .

| Gegevensstroom | Verwachte vertraging |
|---|---|
| Adobe Analytics naar Adobe Analytics-bronaansluiting (A4T ingeschakeld) | &lt; 30 minuten |
| Adobe Analytics-bronaansluiting op realtime klantprofiel (A4T niet ingeschakeld) | &lt; 2 minuten |
| Adobe Analytics-bronaansluiting op realtime klantprofiel (A4T ingeschakeld) | &lt; 30 minuten |
| Gegevens-opname in Data Lake van Edge Network of streaming opname | &lt; 60 minuten |
| Gegevensopname in Data Lake vanaf Adobe Analytics-bronaansluiting | &lt; 90 minuten |
| Gegevensopname in de Customer Journey Analytics van Data Lake | &lt; 90 minuten |
| Adobe Analytics-bronconnectorbackfill van minder dan 10 miljard gebeurtenissen (maximaal 13 maanden historische gegevens) | &lt; 4 weken |
| Publiceren van het publiek naar het profiel van de Klant in real time, met inbegrip van de automatische verwezenlijking van het het stromen segment, en het toestaan van het segment klaar om de gegevens te ontvangen. | staan voor 60 minuten |
| Frequentie vernieuwen voor publiek | Eenmalige vernieuwing: latentie van minder dan 5 minuten.<br/>Vernieuwen elke 4 uur, dagelijks, wekelijks, maandelijks (latentie gaat hand in hand met de vernieuwingsfrequentie) |

{style="table-layout:auto"}

