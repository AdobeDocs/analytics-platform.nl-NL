---
title: Telefooncentrum en webgegevens importeren
description: Leer hoe te om een dataset tot stand te brengen die de gegevens van het vraagcentrum en van de website verbindt.
exl-id: 48546227-029c-4cf9-9b7e-66d547769270
solution: Customer Journey Analytics
feature: Use Cases
role: User
source-git-commit: 9f954709a3dde01b4e01581e34aece07fe0256b1
workflow-type: tm+mt
source-wordcount: '1124'
ht-degree: 0%

---

# Telefooncentrum en webgegevens importeren

Customer Journey Analytics biedt het waardevolle en robuuste vermogen om datasets van verschillende bronnen te combineren tot één Workspace-project. In deze handleiding leert u hoe uw organisatie websitegegevens kan combineren met gegevens van callcenter. U kunt bijvoorbeeld begrijpen welke acties een klant neemt, welke inhoud deze bekijkt en welke voorwaarden deze zoekt voordat deze contact opneemt met de klantenondersteuning. U kunt dan de inhoud en de zelfbedieningshulpmiddelen bepalen om te verbeteren zodat kunnen de klanten kwesties zelf beter oplossen zonder het moeten binnen roepen.

## Vereisten

* De belangrijkste component voor het combineren van deze twee gegevenssets is een gemeenschappelijke id tussen elke gegevensbron. Voorbeelden zijn een klant-id, een gehashte e-mail, aanmeldingsgebruikersnaam of telefoonnummer.
* Toegang tot zowel Adobe Experience Platform als Customer Journey Analytics
* Als uw dataset logboeken van een interactief systeem van de stemreactie omvat, adviseert Adobe verwerking van de gegevens om snelle interactie slechts te omvatten alvorens het in Platform in te voeren.
* Als uw dataset vraaglogboeken omvat, adviseert Adobe het omvatten van de volgende kolommen:
   * De datum/tijd toen de vraag begon
   * Oproepreden
   * Id van callcenter
   * Identiteitskaart van de agent van het Centrum van de vraag
   * Duur van de oproep
   * Resultaat van de oproep
   * Kosten van de oproep (indien beschikbaar)
   * Om het even welke extra gegevens van vraagmeta die uw organisatie wil omvatten

## Web- en callcentgegevens importeren in Platform

Importeer uw gegevens naar Adobe Experience Platform. Zie [ een schema ](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html) en [ Samenvatting gegevens ](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html) in de documentatie van Adobe Experience Platform creëren.

Als u gegevens importeert in Platform, kunt u met de volgende tips insight in resulterende rapporten doen toenemen:

* Zorg ervoor dat de herkenningsteken die wordt gebruikt om vraag en Webgegevens samen te verbinden gelijkaardig geformatteerd is.
* Neem de gegevensbron op in elke gegevensset. Neem bijvoorbeeld een kolom `data_source` op in elk schema en stel de waarde van elke gebeurtenis in op respectievelijk `"Web"` of `"Call center"` . <!--mapper-->

## De persoon-id samenstellen

Customer Journey Analytics vereist een gemeenschappelijke herkenningsteken om a [ gecombineerde dataset ](/help/connections/combined-dataset.md) te produceren.

* Als uw datasets reeds een gemeenschappelijke herkenningsteken op elke gebeurtenis over beide datasets hebben, kunt u deze stap overslaan en te werk gaan om een verbinding tot stand te brengen.
* Als één van beiden van uw datasets een gemeenschappelijk herkenningsteken op slechts sommige gebeurtenissen hebben, kunt u gegevens samen verbinden gebruikend [ Stitching ](/help/stitching/overview.md) voor stappen om kanaalanalyse voor deze twee datasets toe te laten.

## Verbinding maken in Customer Journey Analytics

[ creeer een verbinding ](/help/connections/create-connection.md) in Customer Journey Analytics.

* Als CCA wordt gebruikt, is een nieuwe gestikte dataset beschikbaar voor u aan gebruik. Gebruik het veld Nieuw gekoppelde id als de persoon-id.
* Anders, kunt u zowel originele Web als vraagcentrum datasets voor gebruik in de verbinding selecteren.

## Een gegevensweergave maken

Na het creëren van een verbinding, kunt u [ een gegevensmening ](/help/data-views/create-dataview.md) voor gebruik in Analysis Workspace tot stand brengen. De nuttige componenten omvatten:

* Een pagina-dimensie met laatste aanraking en sessieresistentie. U kunt de metriek van het vraagcentrum met de laatste pagina verbinden die een klant alvorens binnen te roepen bekeken.
* Een vraag metrisch die een het schemagebied van het &quot;centrum van de Vraag&quot;gebruikt om voorkomen te verhogen. Het gebruik [ Metrische deduplicatie ](/help/data-views/component-settings/metric-deduplication.md) zodat verhoogt het slechts eenmaal per zitting.

## Visualisaties maken

De volgende visualisaties kunnen worden gebruikt om inzichten van uw gestikte dataset te bereiken.

### Gegevensset overlapt

Deze visualisatie helpt u begrijpen hoe goed CCA gegevens samenbrengt.

1. Maak twee segmenten. De variabele die in deze twee segmenten wordt gebruikt, is dezelfde hierboven vermelde variabele die de gegevensbron van elke gebeurtenis weerspiegelt. Zie [ een segment ](/help/components/filters/create-filters.md) voor meer informatie creëren.
   * Persoonscontainer waarin de gegevensset-id gelijk is aan uw webgegevens
   * De container van de persoon waar identiteitskaart van de Dataset uw gegevens van het vraagcentrum evenaart
2. In Analysis Workspace, sleep de visualisatie van de a [ Venn ](/help/analysis-workspace/visualizations/venn.md) op het werkruimtekanvas.
3. Sleep de twee nieuwe segmenten naar het **[!UICONTROL Add Filter]** -gebied en de metrische waarde Personen naar het **[!UICONTROL Add Metric]** -gebied.

De resulterende Venn visualisatie toont het aantal mensen in uw dataset die zowel Web als vraagcentrumgegevens bevatten. Hoe groter de overlapping, des te meer mensen met succes werden vastgezet. De gebieden die elkaar niet overlappen vertegenwoordigen mensen die uitsluitend in één dataset of andere verblijven.

### Kenmerkaanroepgebeurtenissen voor webpagina&#39;s

Deze vrije lijst laat u de hoogste pagina&#39;s zien die bijdragen aan vraag centrumgebeurtenissen. Controleer eerst of de gewenste afmetingen en metriek het juiste toewijzingsmodel hebben:

1. Sleep de dimensie die uw webpaginanamen bevat naar een visualisatie voor vrije-vormtabellen.
1. Vervang metrisch met gewenste metrisch vraagcentrum dat u wilt meten.
1. Klik op het tandwielpictogram bij de metrische koptekst. Klik op **[!UICONTROL Use non-default attribution model]**.
1. Plaats het gewenste [ model van de Attributie ](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md). Bijvoorbeeld, een model van het Verval van de Tijd met een halfwaardetijd van 15 minuten, en een Venster van de Raadpleging van Zitting. Dit attributiemodel geeft krediet aan de pagina&#39;s die tot de vraag aan uw vraagcentrum leiden.

Het resulterende rapport toont de hoogste pagina&#39;s die vraag aan uw vraagcentrum drijven. <!-- use case behind what we use these pages for -->

<!-- Complement with donut visualization -->

U kunt insight met deze lijst verder verhogen door Vraag door reden of categorie te verdelen.

1. Klik het juiste chevron onder de dimensie van de Reden van de Vraag in de lijst van componenten. Deze actie onthult individuele afmetingswaarden.
2. Sleep de gewenste afmetingswaarde(s) onder metrische &quot;Vraag&quot;, die segmenten die metrisch door elke respectieve vraagreden.
3. Herhaal dit voor elke reden waarom u wilt bellen. Gebruik het segment Alle sessies om het geaggregeerde totaal weer te geven.

<!-- screenshot -->

### Stroomvisualisatie

U kunt insight in krijgen wat een klant probeerde te doen alvorens zij het kanaal van het vraagcentrum gebruikten. Deze stroomvisualisatie helpt u de frequentste reizen begrijpen een klant neemt om uw vraagcentrum te bereiken. Met deze insight kunt u bepalen welke verbeteringen u het meest effectief kunt aanbrengen in uw site, zodat klanten minder vaak kunnen bellen.

1. Klik op het tabblad **[!UICONTROL Visualizations]** aan de linkerkant en sleep een stroomvisualisatie naar het canvas van de werkruimte.
2. Klik op het tabblad **[!UICONTROL Components]** aan de linkerkant en zoek de dimensie &#39;Reden bellen&#39;.
3. Klik op het rechterchevron naast deze dimensie. Deze actie onthult individuele afmetingswaarden.
4. Sleep het gewenste de afmetingspunt van de vraagreden aan de centrumplaats van de stroomvisualisatie.
5. De stroomvisualisatie bevolkt automatisch vorige en volgende vraagredenen. Vervang de vorige vraagreden met de dimensie van de websitepagina.
6. Klik op het tandwielpictogram rechtsboven in de stroomvisualisatie en wijzig de container voor de stroom in **[!UICONTROL Session]** .

### Histogram

Hoeveel klanten hebben één keer geroepen, tweemaal geroepen, of 6+ keer geroepen? Sommige van deze mensen bezoeken nooit de website. Gebruik de histogramvisualisatie om te bepalen hoeveel mensen in elk emmertje vallen. Voor mensen die nooit de website bezoeken, zie hoe wij hen kunnen aanmoedigen om zelf te dienen.

1. Klik op de tab **[!UICONTROL Visualizations]** aan de linkerkant en sleep een histogram visualisatie naar het canvas van de werkruimte.
2. Klik op het tabblad **[!UICONTROL Components]** aan de linkerkant en sleep de metrische aanroepen naar de histogram visualisatie.
3. Klik op **[!UICONTROL Show advanced settings]** in het midden van de visualisatie en pas de gewenste emmers aan.
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

Create a bunch of segments - facets to their business. Segments were used because they didn't have all of these in the same dimension, so they could create everything in this report as a single dimension (really segments)

wanted to understand when someone interacts with a facet, whats the highest percentage of people that abandon that channel to call them. not from volume perspective, but percentage perspective.

use sequential segments, but you lose the ability to use attribution IQ

## What to do when you've found insight -->
