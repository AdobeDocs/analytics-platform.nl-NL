---
title: Wat is Cohort Analysis?
description: Meer informatie over cohortanalyse in Analysis Workspace
translation-type: tm+mt
source-git-commit: ff1a11a18de0825b6338de98865e3bddeef14f39
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---


# Wat is [!UICONTROL Cohort Analysis]?

A *`cohort`* is een groep personen die gemeenschappelijke kenmerken delen over een bepaalde periode. [!UICONTROL Cohort Analysis] is bijvoorbeeld handig als u wilt weten hoe een cohort werkt met een merk. U kunt gemakkelijk veranderingen in tendensen waarnemen, dan dienovereenkomstig antwoorden. (Toelichting van [!UICONTROL Cohort Analysis] zijn beschikbaar op het web, bijvoorbeeld op [Cohortanalyse 101](https://en.wikipedia.org/wiki/Cohort_analysis).)

Na het creëren van een cohortrapport, kunt u zijn componenten (specifieke dimensies, metriek, en segmenten) tot stand brengen, dan het cohortrapport met iedereen delen. Zie [Curven en delen](/help/analysis-workspace/curate-share/curate.md).

Voorbeelden van wat u kunt doen met [!UICONTROL Cohort Analysis]:

* Start campagnes die zijn ontworpen om een gewenste actie te stimuleren.
* Het marketingbudget verschuiven op precies het juiste moment in de levenscyclus van de klant.
* Herken wanneer een proefversie of een aanbieding moet worden beëindigd om de waarde te maximaliseren.
* Verbeter ideeën voor het testen A/B op gebieden zoals tarifering, verbeteringspad, etc.
* Een [!UICONTROL Cohort Analysis] in een rapport met instructies.

[!UICONTROL Cohort Analysis] is beschikbaar voor alle Adobe Analytics-klanten met toegangsrechten voor [!UICONTROL Analysis Workspace].

[Videozelfstudie Cohortinganalyse](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/cohort-analysis/cohort-analysis-workspace.html) (4:36)

>[!IMPORTANT]
>
>[!UICONTROL Cohort Analysis]
>
>ondersteunt geen niet-segmenteerbare metriek (inclusief berekende metriek), niet-gehele metriek (zoals Opbrengst) of Voorvallen. Alleen metriek die in segmenten kan worden gebruikt, kan worden gebruikt in
>[!UICONTROL Cohort Analysis]en kunnen slechts met één worden verhoogd.

## Cohortanalyse-mogelijkheden

Met de volgende mogelijkheden kunt u de cohorten die u maakt, nauwkeurig instellen:

### [!UICONTROL Retention] Tabel

A [!UICONTROL Retention] het cohort rapport geeft bezoekers terug : in elke gegevenscel worden het onbewerkte aantal en het onbewerkte percentage bezoekers in de cohort weergegeven die de actie in die periode hebben uitgevoerd . U kunt maximaal 3 cijfers en maximaal 10 segmenten opnemen.

![](assets/retention-report.png)

### [!UICONTROL Churn] Tabel

A [!UICONTROL Churn] cohort is het omgekeerde van een retentietabel en toont de bezoekers die in de loop der tijd niet of niet aan de terugkeercriteria voor uw cohort voldeden. U kunt maximaal 3 cijfers en maximaal 10 segmenten opnemen.

![](assets/churn-report.png)

### [!UICONTROL Rolling Calculation]

Hiermee kunt u de retentie of het verloop berekenen op basis van de vorige kolom, niet de opgenomen kolom.

![](assets/cohort-rolling-calculation.png)

### [!UICONTROL Latency] Tabel

Hiermee wordt de tijd gemeten die is verstreken vóór en na de opnemingsgebeurtenis. Dit is een uitstekend instrument voor pre- en postanalyse. De **[!UICONTROL Included]** de kolom bevindt zich in het midden van de tabel en de tijdsperiodes voor en na de opnemingsgebeurtenis worden aan beide zijden weergegeven.

![](assets/cohort-latency.png)

### [!UICONTROL Custom Dimension] Cohort

Maak cohorten op basis van een geselecteerde afmeting en niet op basis van een tijd, de standaardinstelling. Afmetingen gebruiken zoals [!UICONTROL marketing channel], [!UICONTROL campaign], [!UICONTROL product], [!UICONTROL page], [!UICONTROL region]of een andere dimensie in Adobe Analytics om aan te geven hoe de retentie verandert op basis van de verschillende waarden van deze dimensies.

![](assets/cohort-customizable-cohort-row.png)

Ga voor instructies over het instellen en uitvoeren van een cohortrapport naar [Een rapport Cohortanalyse configureren](/help/analysis-workspace/visualizations/cohort-table/t-cohort.md).

