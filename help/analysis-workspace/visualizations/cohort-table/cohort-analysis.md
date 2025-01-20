---
title: Overzicht van de cohortingtabel
description: Meer informatie over het gebruik van een cohortabel voor cohortanalyse in Analysis Workspace
feature: Visualizations
exl-id: 3e3a70cd-70ec-4d4d-81c3-7902716d0b01
role: User
source-git-commit: 55b312552d32070875714a77e1177bf0da5f9d87
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Overzicht van de cohortingtabel {#cohort-table-overview}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_cohorttable_button"
>title="Cohortingtabel"
>abstract="Maak een cohortvisualisatie om gebruikers te groeperen op basis van de voltooiing van een gebeurtenis en de doorlopende betrokkenheid te analyseren en in de loop van de tijd te verdraaien."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_cohorttable_panel"
>title="Cohortingtabel"
>abstract="Groepeer gebruikers op basis van voltooiing van een gebeurtenis en analyseer vervolgens hun doorlopende betrokkenheid en loop de tijd door.<br/><br/>**Parameters **<br/>**criteria van de Opname**: De componenten die worden gebruikt om uw aanvankelijke bezoekerscohorts te bepalen.<br/>**criteria van de Terugkeer**: De componenten die worden gebruikt om te bepalen als een bezoeker is teruggekeerd."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert de lijst van de Cohort in_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**._<br/>_zie [ Lijst van de Cohort ](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/visualizations/cohort-table/cohort-analysis) voor_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics** versie van dit artikel._

>[!ENDSHADEBOX]


A *cohort* is een groep mensen die gemeenschappelijke kenmerken over een gespecificeerde periode delen. A ![ TextNumbered ](/help/assets/icons/TextNumbered.svg) **[!UICONTROL Cohort table]** visualisatie is nuttig, bijvoorbeeld, wanneer u wilt leren hoe een cohort met een merk in dienst neemt. U kunt gemakkelijk veranderingen in tendensen waarnemen, dan dienovereenkomstig antwoorden. (De Verklaringen van [!UICONTROL Cohort Analysis] zijn beschikbaar op het Web, zoals bij [ Analyse 101 van de Cohort ](https://en.wikipedia.org/wiki/Cohort_analysis).)

Na het creëren van een cohortrapport, kunt u zijn componenten (specifieke afmetingen, metriek, en filters) tot stand brengen, dan het cohortrapport met iedereen delen. Zie [ Kromme en Aandeel ](/help/analysis-workspace/curate-share/curate.md).

Voorbeelden van wat u kunt doen met een [!UICONTROL Cohort table] :

* Start campagnes die zijn ontworpen om een gewenste actie te stimuleren.
* Het marketingbudget verschuiven op precies het juiste moment in de levenscyclus van de klant.
* Bespreek wanneer een proefversie of een aanbieding moet worden beëindigd om de waarde te maximaliseren.
* Verbeter ideeën voor het testen A/B op gebieden zoals tarifering, verbeteringspad, etc.

[!UICONTROL Cohort table] is beschikbaar voor alle klanten van de Customer Journey Analytics met toegangsrechten tot [!UICONTROL Analysis Workspace].

+++ Bekijk een videodemonstratie van de cohorttabel.

>[!VIDEO](https://video.tv.adobe.com/v/23990/?quality=12)

{{videoaa}}

+++

>[!IMPORTANT]
>
>[!UICONTROL Cohort Analysis] biedt geen ondersteuning voor niet-filterbare metriek (inclusief berekende meetwaarden), niet-gehele getallen (zoals Opbrengst) of Voorvallen. Alleen metriek die in filters kan worden gebruikt, kan in [!UICONTROL Cohort Analysis] worden gebruikt en kan slechts één voor één worden verhoogd.

De lijsten van de cohort in Customer Journey Analytics steunen dubbel-gebaseerd (of om het even welk numeriek-gebaseerd) metrisch. Purchase.Value (een dubbele waarde) kan bijvoorbeeld worden gebruikt als een insluitings-/retourmetrisch object. Bovendien zijn alle meetgegevens die via de Analytics Source Connector naar Adobe Experience Platform worden doorgegeven, verdubbelbaar.

## Mogelijkheden voor kleurentabellen

De volgende secties beschrijven de eigenschappen van de Analyse van de Cohort die voor nauwkeurige controle over de cohorts toestaan u bouwt.

Voor meer gedetailleerde informatie over het creëren van een cohort en het runnen van a [!UICONTROL Cohort Analysis] rapport, zie [ een lijst van de Cohort ](/help/analysis-workspace/visualizations/cohort-table/t-cohort.md) vormen.

### [!UICONTROL Retention] table

Een [!UICONTROL Retention] -cohortentabel retourneert personen: elke gegevenscel geeft het onbewerkte aantal en percentage weer van de personen in de cohort die de actie tijdens die periode hebben uitgevoerd. U kunt maximaal 3 metriek en maximaal 10 filters opnemen.

![ het cohort van de Vermindering van A die de eenheden en het percentage van personen in de cohort toont.](assets/retention-report.png)

### [!UICONTROL Churn] table

Een [!UICONTROL Churn] -cohortabel is het omgekeerde van een retentietabel en toont de personen die in de loop der tijd niet of niet aan de retourcriteria voor uw cohort hebben voldaan. U kunt maximaal 3 metriek en maximaal 10 filters opnemen.

![ de lijst van het Koord van A die eenheden en percentage van mensen tonen die niet aan de terugkeercriteria voor een cohort beantwoordden.](assets/churn-report.png)

### [!UICONTROL Rolling Calculation]

U kunt de retentie of het churn berekenen op basis van de vorige kolom, niet de opgenomen kolom, die wordt aangeduid als rolberekening.

![ het bewaarrapport van de Cohort dat berekeningen toont die op een vorige kolom van gegevens worden gebaseerd.](assets/retention-report-rolling.png)

### [!UICONTROL Latency] table

Een latentietabel meet de tijd die is verstreken voor en na de opnemingsgebeurtenis. De latentie meten is een uitstekend hulpmiddel voor pre- en postanalyse. De kolom **[!UICONTROL Included]** bevindt zich in het midden van de tabel en de tijdsperioden vóór en na de gebeurtenis include worden aan beide zijden weergegeven.

![ het rapport van de Cohort van A die de verstreken tijd vóór en na een gebeurtenis tonen.](assets/retention-report-latency.png)

### [!UICONTROL Custom dimension] cohort

U kunt cohorten maken op basis van een geselecteerde afmeting en niet op basis van een tijd (de standaardinstelling). Gebruik afmetingen zoals [!UICONTROL City geo] , [!UICONTROL Marketing channel] , [!UICONTROL campaign] , [!UICONTROL product] , [!UICONTROL page] , [!UICONTROL region] of een andere dimensie om aan te geven hoe de retentie verandert. Gebaseerd op de verschillende waarden van deze afmetingen.

![ het rapport van de Cohort van A die aangepast rapport met geselecteerde dimensies tonen niet de standaardop tijd-gebaseerde cohort.](assets/retention-dimensions.png)

>[!MORELIKETHIS]
>
>[ vorm een lijst van de Cohort ](/help/analysis-workspace/visualizations/cohort-table/t-cohort.md).
>

