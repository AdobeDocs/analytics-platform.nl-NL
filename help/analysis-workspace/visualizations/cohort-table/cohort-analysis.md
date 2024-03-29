---
title: Wat is Cohort Analysis?
description: Meer informatie over cohortanalyse in Analysis Workspace
feature: Visualizations
exl-id: 3e3a70cd-70ec-4d4d-81c3-7902716d0b01
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Wat is [!UICONTROL Cohort Analysis]?

A *`cohort`* is een groep personen die gemeenschappelijke kenmerken delen over een bepaalde periode. [!UICONTROL Cohort Analysis] is bijvoorbeeld handig als u wilt weten hoe een cohort werkt met een merk. U kunt gemakkelijk veranderingen in tendensen waarnemen, dan dienovereenkomstig antwoorden. (Toelichting van [!UICONTROL Cohort Analysis] zijn beschikbaar op het web, bijvoorbeeld op [Cohortanalyse 101](https://en.wikipedia.org/wiki/Cohort_analysis).)

Na het creëren van een cohortrapport, kunt u zijn componenten (specifieke afmetingen, metriek, en filters) tot stand brengen, dan het cohortrapport met iedereen delen. Zie [Curven en delen](/help/analysis-workspace/curate-share/curate.md).

Voorbeelden van wat u kunt doen met [!UICONTROL Cohort Analysis]:

* Start campagnes die zijn ontworpen om een gewenste actie te stimuleren.
* Het marketingbudget verschuiven op precies het juiste moment in de levenscyclus van de klant.
* Herken wanneer een proefversie of een aanbieding moet worden beëindigd om de waarde te maximaliseren.
* Verbeter ideeën voor het testen A/B op gebieden zoals tarifering, verbeteringspad, etc.

[!UICONTROL Cohort Analysis] is beschikbaar voor alle klanten van de Customer Journey Analytics met toegangsrechten tot [!UICONTROL Analysis Workspace].

[Videozelfstudie Cohortinganalyse](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/cohort-analysis/cohort-analysis-workspace.html) 4:36

>[!IMPORTANT]
>
>[!UICONTROL Cohort Analysis] ondersteunt geen niet-filtreerbare metriek (inclusief berekende metriek), niet-geheelmetriek (zoals Opbrengst), of Voorvallen. Alleen metriek die in filters kan worden gebruikt, kan worden gebruikt in [!UICONTROL Cohort Analysis]en kunnen slechts één voor één worden verhoogd.

## Cohortanalyse-mogelijkheden

Met de volgende mogelijkheden kunt u de cohorten die u maakt, nauwkeurig instellen:

### [!UICONTROL Retention] Tabel

A [!UICONTROL Retention] het cohortrapport geeft personen : elke gegevenscel geeft het onbewerkte aantal en het onbewerkte percentage personen in het cohort aan die de actie in die periode hebben uitgevoerd . U kunt maximaal 3 metriek en maximaal 10 filters opnemen.

![Een rapport van de Rention Cohort waarin de eenheden en het percentage personen in de cohort worden weergegeven.](assets/retention-report.png)

### [!UICONTROL Churn] Tabel

A [!UICONTROL Churn] cohort is het omgekeerde van een retentietabel en geeft de personen weer die in de loop der tijd niet of niet aan de criteria voor terugkeer voor uw cohort voldeden. U kunt maximaal 3 metriek en maximaal 10 filters opnemen.

![Een Churn-tabel met de eenheden en het percentage personen die niet aan de retourcriteria voor een cohort voldeden.](assets/churn-report.png)

### [!UICONTROL Rolling Calculation]

Hiermee kunt u de retentie of het verloop berekenen op basis van de vorige kolom, niet de opgenomen kolom.

![Een rapport van het behoud van de Cohort dat berekeningen toont die op een vorige kolom van gegevens worden gebaseerd.](assets/cohort-rolling-calculation.png)

### [!UICONTROL Latency] Tabel

Hiermee wordt de tijd gemeten die is verstreken vóór en na de opnemingsgebeurtenis. Dit is een uitstekend instrument voor pre- en postanalyse. De **[!UICONTROL Included]** de kolom bevindt zich in het midden van de tabel en de tijdsperiodes voor en na de opnemingsgebeurtenis worden aan beide zijden weergegeven.

![Een Cohort-rapport met de verstreken tijd voor en na een gebeurtenis.](assets/cohort-latency.png)

### [!UICONTROL Custom Dimension] Cohort

Maak cohorten op basis van een geselecteerde afmeting en niet op basis van een tijd, de standaardinstelling. Afmetingen gebruiken zoals [!UICONTROL marketing channel], [!UICONTROL campaign], [!UICONTROL product], [!UICONTROL page], [!UICONTROL region]of een andere dimensie in de Customer Journey Analytics om aan te geven hoe de retentie verandert op basis van de verschillende waarden van deze dimensies.

![Een rapport van de Cohort dat aangepast rapport met geselecteerde dimensies niet de standaardop tijd-gebaseerde cohort toont.](assets/cohort-customizable-cohort-row.png)

Ga voor instructies over het instellen en uitvoeren van een cohortrapport naar [Een rapport Cohortanalyse configureren](/help/analysis-workspace/visualizations/cohort-table/t-cohort.md).
