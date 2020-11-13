---
title: Telefooncentrum en webgegevens importeren
description: Leer hoe te om een dataset tot stand te brengen die de gegevens van het vraagcentrum en van de website verbindt.
translation-type: tm+mt
source-git-commit: 8d2f70ad47dcf9b97808da3a04d32d3412a1f0c8
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---


# Telefooncentrum en webgegevens importeren

Customer Journey Analytics verstrekt het waardevolle en robuuste vermogen om datasets van verschillende bronnen in één enkel project van de Werkruimte te combineren. Gebruik deze gids om te begrijpen hoe uw organisatie gegevens van uw website aan gegevens kan verbinden die uit uw vraagcentrum voortkomen.

## Vereisten

* De belangrijkste component om deze twee reeksen gegevens te combineren is een gemeenschappelijke herkenningsteken tussen elke bron van gegevens. Voorbeelden zijn een klant-id, een gehashte e-mail, aanmeldingsgebruikersnaam of telefoonnummer.
* Toegang tot zowel Adobe Experience Platform als Customer Journey Analytics
* Als uw dataset logboeken van een interactief systeem van de stemreactie omvat, adviseert Adobe verwerking van de gegevens om snelle interactie slechts te omvatten alvorens het in Platform in te voeren.
* Als uw dataset vraaglogboeken omvat, adviseert Adobe het omvatten van de volgende kolommen:
   * De datum/tijd toen de vraag begon
   * Oproepreden
   * Id van callcenter
   * Agent-id van callcenter
   * Duur van de oproep
   * Resultaat van de oproep
   * Kosten van de oproep (indien beschikbaar)
   * Om het even welke extra gegevens van vraagmeta die uw organisatie wil omvatten

## Webgegevens en callcentergegevens importeren in Platform

Beginnen met het importeren van gegevens naar Adobe Experience Platform. Zie [Een schema maken](https://docs.adobe.com/content/help/en/experience-platform/xdm/tutorials/create-schema-ui.html) en [Gegevens invoegen](https://docs.adobe.com/content/help/en/experience-platform/ingestion/home.html) in de documentatie van Adobe Experience Platform.

Als u gegevens importeert in Platform, kunt u met deze tips meer inzicht krijgen in de resulterende rapporten:

* Zorg ervoor dat de herkenningsteken die wordt gebruikt om vraag en Webgegevens samen te verbinden gelijkaardig geformatteerd is.
* Neem de gegevensbron op in elke gegevensset. Neem bijvoorbeeld een `data_source`-kolom op in elk schema en stel de waarde van elke gebeurtenis in op respectievelijk `"Web"` of `"Call center"`. <!--mapper-->

## De persoon-id samenstellen

CJA vereist een gemeenschappelijke herkenningsteken om [gecombineerde dataset](../connections/combined-dataset.md) te produceren.

* Als uw datasets reeds een gemeenschappelijke herkenningsteken op elke gebeurtenis over beide datasets hebben, kunt u deze stap overslaan en te werk gaan om een verbinding tot stand te brengen.
* Als één van uw datasets een gemeenschappelijke herkenningsteken op slechts sommige gebeurtenissen heeft, kunt u gegevens verenigen gebruikend de Analytics van het Kanaal. Zie [Overzicht van de Analytics van het Kanaal](/help/connections/cca/overview.md) voor stappen om CCA voor deze twee datasets toe te laten.

## Verbinding maken in CJA

[Maak een ](/help/connections/create-connection.md) verbinding in CJA.

* Als CCA wordt gebruikt, is een nieuwe gestikte dataset beschikbaar voor u aan gebruik. Gebruik het veld Nieuw gekoppelde id als de persoon-id.
* Anders, kunt u zowel originele Web als vraagcentrum datasets voor gebruik in de verbinding selecteren.

## Een gegevensweergave maken

Nadat u een verbinding hebt gemaakt, kunt u [een gegevensweergave maken](/help/data-views/create-dataview.md) voor gebruik in Analysis Workspace. <!-- page dimension last touch, session persistence -->
<!-- create calls metric using call center reason (requires data views 2.0). any column that triggers once per call -->

## Visualisaties maken

De volgende visualisaties kunnen worden gebruikt om inzichten van uw gestikte dataset te bereiken.

### Gegevensset overlapt

Deze visualisatie helpt u begrijpen hoe goed CCA gegevens samenbrengt.

1. Maak twee filters. De variabele die in deze twee filters wordt gebruikt, is dezelfde hierboven vermelde variabele die de gegevensbron van elke gebeurtenis weerspiegelt. Zie [Een filter maken](/help/components/filters/create-filters.md) voor meer informatie.
   * Persoonscontainer waarin de gegevensset-id gelijk is aan uw webgegevens
   * De container van de persoon waar identiteitskaart van de Dataset uw gegevens van het vraagcentrum evenaart
2. In Analysis Workspace sleept u een [Venn](/help/analysis-workspace/visualizations/venn.md)-visualisatie naar het canvas van de werkruimte.
3. Sleep de twee nieuwe filters naar het gebied **[!UICONTROL Add Filter]** en de metrische waarde Personen naar het gebied **[!UICONTROL Add Metric]**.

De resulterende Venn visualisatie toont het aantal mensen in uw dataset die zowel Web als vraagcentrumgegevens bevatten. Hoe groter de overlapping, des te meer mensen met succes werden vastgezet. De gebieden die niet overlappen vertegenwoordigen mensen die uitsluitend in één dataset of andere verblijven.

### Kenmerkaanroepgebeurtenissen voor webpagina&#39;s

Deze vrije lijst laat u de hoogste pagina&#39;s zien die bijdragen tot de gebeurtenissen van het vraagcentrum. Controleer eerst of de gewenste afmetingen en metriek het juiste toewijzingsmodel hebben:

1. Sleep de dimensie die uw webpaginanamen bevat naar een visualisatie voor vrije-vormtabellen.
1. Vervang metrisch met gewenste metrisch vraagcentrum dat u omzetting wilt meten.
1. Klik op het tandwielpictogram bij de metrische koptekst. Klik op **[!UICONTROL Use non-default attribution model]**.
1. Stel het gewenste [Attributiemodel](/help/data-views/configure-dataviews.md#Attribution-model) in.

Het resulterende rapport toont hoogste metrisch van de gegevens van het vraagcentrum. <!-- Complement with donut visualization -->

<!-- ### Flow between web data and call center

call reason as an exit dimension, web page name for previous pages

### Histogram


### Fallout

step 1: all sessions
step 2: purchase step 1
step 3: call

another good one

step 1: all sessions
step 2: -->

<!--  use target (AB testing) to test new versions of these pages so they reduce calls (using an eVar to determine A/B?)
  filter by specific call reason using workspace dropdowns
  visualize flow of pages > call reason 
-->