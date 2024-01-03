---
title: Telefooncentrum en webgegevens importeren
description: Leer hoe te om een dataset tot stand te brengen die de gegevens van het vraagcentrum en van de website verbindt.
exl-id: 48546227-029c-4cf9-9b7e-66d547769270
solution: Customer Journey Analytics
feature: Use Cases
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '1124'
ht-degree: 0%

---

# Telefooncentrum en webgegevens importeren

Customer Journey Analytics verstrekt het waardevolle en robuuste vermogen om datasets van verschillende bronnen in één enkel project van de Werkruimte te combineren. In deze handleiding leert u hoe uw organisatie websitegegevens kan combineren met gegevens van callcenter. U kunt bijvoorbeeld begrijpen welke acties een klant neemt, welke inhoud deze bekijkt en welke voorwaarden deze zoekt voordat deze contact opneemt met de klantenondersteuning. U kunt dan de inhoud en de zelfbedieningshulpmiddelen bepalen om te verbeteren zodat kunnen de klanten kwesties zelf beter oplossen zonder het moeten binnen roepen.

## Vereisten

* De belangrijkste component voor het combineren van deze twee gegevenssets is een gemeenschappelijke id tussen elke gegevensbron. Voorbeelden zijn een klant-id, een gehashte e-mail, aanmeldingsgebruikersnaam of telefoonnummer.
* Toegang tot zowel Adobe Experience Platform als Customer Journey Analytics
* Als uw dataset logboeken van een interactief systeem van de stemreactie omvat, adviseert de Adobe verwerking van de gegevens om snelle interactie slechts te omvatten alvorens het in Platform in te voeren.
* Als uw dataset vraaglogboeken omvat, beveelt de Adobe het omvatten van de volgende kolommen aan:
   * De datum/tijd toen de vraag begon
   * Oproepreden
   * Id van callcenter
   * Identiteitskaart van de agent van het Centrum van de vraag
   * Duur van de oproep
   * Resultaat van de oproep
   * Kosten van de oproep (indien beschikbaar)
   * Om het even welke extra gegevens van vraagmeta die uw organisatie wil omvatten

## Web- en callcentgegevens importeren in Platform

Importeer uw gegevens naar Adobe Experience Platform. Zie [Een schema maken](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html) en [Samenvattingsgegevens](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html) in de documentatie van Adobe Experience Platform.

Wanneer het invoeren van gegevens in Platform, kan het volgen van deze uiteinden helpen inzicht in resulterende rapporten verhogen:

* Zorg ervoor dat de herkenningsteken die wordt gebruikt om vraag en Webgegevens samen te verbinden gelijkaardig geformatteerd is.
* Neem de gegevensbron op in elke gegevensset. Neem bijvoorbeeld een `data_source` kolom in elk schema en stel de waarde van elke gebeurtenis in op `"Web"` of `"Call center"`, respectievelijk. <!--mapper-->

## De persoon-id samenstellen

Customer Journey Analytics vereist een gemeenschappelijke id om een [gecombineerde gegevensset](/help/connections/combined-dataset.md).

* Als uw datasets reeds een gemeenschappelijke herkenningsteken op elke gebeurtenis over beide datasets hebben, kunt u deze stap overslaan en te werk gaan om een verbinding tot stand te brengen.
* Als één van uw datasets een gemeenschappelijke herkenningsteken op slechts sommige gebeurtenissen heeft, kunt u gegevens verbinden samen gebruikend [Stiksel](/help/stitching/overview.md) voor stappen om kanaalanalyse voor deze twee datasets toe te laten.

## Verbinding maken in Customer Journey Analytics

[Verbinding maken](/help/connections/create-connection.md) in de Customer Journey Analytics.

* Als CCA wordt gebruikt, is een nieuwe gestikte dataset beschikbaar voor u aan gebruik. Gebruik het veld Nieuw gekoppelde id als de persoon-id.
* Anders, kunt u zowel originele Web als vraagcentrum datasets voor gebruik in de verbinding selecteren.

## Een gegevensweergave maken

Nadat u een verbinding hebt gemaakt, kunt u [Een gegevensweergave maken](/help/data-views/create-dataview.md) voor gebruik in Analysis Workspace. De nuttige componenten omvatten:

* Een pagina-dimensie met laatste aanraking en sessieresistentie. U kunt de metriek van het vraagcentrum met de laatste pagina verbinden die een klant alvorens binnen te roepen bekeken.
* Een vraag metrisch die een het schemagebied van het &quot;centrum van de Vraag&quot;gebruikt om voorkomen te verhogen. Gebruiken [Metrische deduplicatie](/help/data-views/component-settings/metric-deduplication.md) het wordt dus slechts eenmaal per sessie verhoogd.

## Visualisaties maken

De volgende visualisaties kunnen worden gebruikt om inzichten van uw gestikte dataset te bereiken.

### Gegevensset overlapt

Deze visualisatie helpt u begrijpen hoe goed CCA gegevens samenbrengt.

1. Maak twee filters. De variabele die in deze twee filters wordt gebruikt, is dezelfde hierboven vermelde variabele die de gegevensbron van elke gebeurtenis weerspiegelt. Zie [Een filter maken](/help/components/filters/create-filters.md) voor meer informatie .
   * Persoonscontainer waarin de gegevensset-id gelijk is aan uw webgegevens
   * De container van de persoon waar identiteitskaart van de Dataset uw gegevens van het vraagcentrum evenaart
2. Sleep in Analysis Workspace een [Venn](/help/analysis-workspace/visualizations/venn.md) visualisatie op het canvas van de werkruimte.
3. Sleep de twee nieuwe filters naar de **[!UICONTROL Add Filter]** en de personenmetrie naar het **[!UICONTROL Add Metric]** gebied.

De resulterende Venn visualisatie toont het aantal mensen in uw dataset die zowel Web als vraagcentrumgegevens bevatten. Hoe groter de overlapping, des te meer mensen met succes werden vastgezet. De gebieden die elkaar niet overlappen vertegenwoordigen mensen die uitsluitend in één dataset of andere verblijven.

### Kenmerkaanroepgebeurtenissen voor webpagina&#39;s

Deze vrije lijst laat u de hoogste pagina&#39;s zien die bijdragen aan vraag centrumgebeurtenissen. Controleer eerst of de gewenste afmetingen en metriek het juiste toewijzingsmodel hebben:

1. Sleep de dimensie die uw webpaginanamen bevat naar een visualisatie voor vrije-vormtabellen.
1. Vervang metrisch met gewenste metrisch vraagcentrum dat u wilt meten.
1. Klik op het tandwielpictogram bij de metrische koptekst. Klik op **[!UICONTROL Use non-default attribution model]**.
1. Stel het gewenste [Attributiemodel](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md). Bijvoorbeeld, een model van het Verval van de Tijd met een halfwaardetijd van 15 minuten, en een Venster van de Raadpleging van Zitting. Dit attributiemodel geeft krediet aan de pagina&#39;s die tot de vraag aan uw vraagcentrum leiden.

Het resulterende rapport toont de hoogste pagina&#39;s die vraag aan uw vraagcentrum drijven. <!-- use case behind what we use these pages for -->

<!-- Complement with donut visualization -->

U kunt inzicht met deze lijst verder verhogen door Vraag door reden of categorie te verdelen.

1. Klik het juiste chevron onder de dimensie van de Reden van de Vraag in de lijst van componenten. Deze actie onthult individuele afmetingswaarden.
2. Sleep de gewenste afmetingswaarde(s) onder metrisch van &quot;Vraag&quot;, die metrisch door elke respectieve vraagreden filtreert.
3. Herhaal dit voor elke reden waarom u wilt bellen. Gebruik het filter &#39;Alle sessies&#39; om het totale totaal weer te geven.

<!-- screenshot -->

### Stroomvisualisatie

U kunt inzicht in krijgen wat een klant probeerde te doen alvorens zij het kanaal van het vraagcentrum gebruikten. Deze stroomvisualisatie helpt u de frequentste reizen begrijpen een klant neemt om uw vraagcentrum te bereiken. Met dit inzicht kunt u de meest effectieve verbeteringen bepalen die u kunt aanbrengen in uw site, zodat klanten minder vaak kunnen inbellen.

1. Klik op de knop **[!UICONTROL Visualizations]** aan de linkerkant en sleep een stroomvisualisatie naar het canvas van de werkruimte.
2. Klik op de knop **[!UICONTROL Components]** op de linkerzijde en bepaal de plaats van de &quot;Reden van de Vraag&quot;afmeting.
3. Klik op het rechterchevron naast deze dimensie. Deze actie onthult individuele afmetingswaarden.
4. Sleep het gewenste de afmetingspunt van de vraagreden aan de centrumplaats van de stroomvisualisatie.
5. De stroomvisualisatie bevolkt automatisch vorige en volgende vraagredenen. Vervang de vorige vraagreden met de dimensie van de websitepagina.
6. Klik op het tandwielpictogram in de rechterbovenhoek van de stroomvisualisatie en wijzig de container voor de stroom in **[!UICONTROL Session]**.

### Histogram

Hoeveel klanten hebben één keer geroepen, tweemaal geroepen, of 6+ keer geroepen? Sommige van deze mensen bezoeken nooit de website. Gebruik de histogramvisualisatie om te bepalen hoeveel mensen in elk emmertje vallen. Voor mensen die nooit de website bezoeken, zie hoe wij hen kunnen aanmoedigen om zelf te dienen.

1. Klik op de knop **[!UICONTROL Visualizations]** aan de linkerkant en sleep een histogramvisualisatie naar het canvas van de werkruimte.
2. Klik op de knop **[!UICONTROL Components]** op de linkerzijde en sleep metrische vraag aan de histogramvisualisatie.
3. Klikken **[!UICONTROL Show advanced settings]** in het midden van de visualisatie en pas de gewenste emmers aan.
4. Klik op **[!UICONTROL Build]**.

<!--
### Web to call, call to web

### Fallout

Fallout sessions - session

All sessions > page views metric > calls metric

All sessions > calls metric > page views

Orrr we could also use dataset ID

step 1: all sessions
step 2: 


### Site sections that result in a call within 30 minutes

Slide 4

Create a bunch of filters - facets to their business. Filters were used because they didn't have all of these in the same dimension, so they could create everything in this report as a single dimension (really filters)

wanted to understand when someone interacts with a facet, whats the highest percentage of people that abandon that channel to call them. not from volume perspective, but percentage perspective.

use sequential filters, but you lose the ability to use attribution IQ

## What to do when you've found insight -->
