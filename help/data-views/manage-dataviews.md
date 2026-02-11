---
title: Gegevensweergaven beheren
description: Leer hoe u gegevensweergaven beheert.
solution: Customer Journey Analytics
feature: Data Views
role: Admin
exl-id: c5cf15ab-3eb1-4e6b-93a3-3d89694ca0ea
source-git-commit: e65dd6f71c75c06aac078c22ea7d77eed75cd381
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 0%

---

# Gegevensweergaven beheren


Zodra u [&#x200B; creeerde of uitgegeven één of meerdere gegevensmeningen &#x200B;](/help/data-views/create-dataview.md) hebt, kunt u hen in **[!UICONTROL Data views]** beheren.

Selecteer **[!UICONTROL Data Management]** > **[!UICONTROL Data views]** in de hoofdmenubalk in Customer Journey Analytics.

De interface **[!UICONTROL Data views]** toont een lijst van alle beschikbare gegevensmeningen.

![&#x200B; de meningsinterface van Gegevens &#x200B;](/help/data-views/assets/data-views.png)

De volgende kolommen en pictogrammen zijn beschikbaar in de tabel:

| Kolom of pictogram | Beschrijving |
| --- | --- |
| **[!UICONTROL Name]** | De naam van de gegevensweergave. |
| ![&#x200B; Informatie &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) | Om informatie over de gegevensmening te bekijken, selecteer ![&#x200B; InfoOutline &#x200B;](/help/assets/icons/InfoOutline.svg) naast de naam van de gegevensmening.<br/> pop-up venster van A toont details over de gegevensmening. |
| ![&#x200B; Meer &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) | Selecteer ![&#x200B; Meer &#x200B;](/help/assets/icons/More.svg) om een contextmenu te openen. U kunt selecteren:<br/>![&#x200B; geeft &#x200B;](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** uit [&#x200B; &#x200B;](#edit-data-views) een gegevensmening uit.<br/>![&#x200B; Exemplaar &#x200B;](/help/assets/icons/Copy.svg) **[!UICONTROL Copy]** aan [&#x200B; kopieert een gegevensmening &#x200B;](#copy-data-views).<br/>![&#x200B; Schrapping &#x200B;](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** aan [&#x200B; schrap &#x200B;](#delete-data-views) een gegevensmening.<br/>![&#x200B; FileCSV &#x200B;](/help/assets/icons/FileCSV.svg) **[!UICONTROL Export to CSV]** aan [&#x200B; voer de details van de gegevensmening naar een Csv- dossier &#x200B;](#export-data-views-to-csv) uit.<br/>![&#x200B; ProjectAdd &#x200B;](/help/assets/icons/ProjectAdd.svg) **[!UICONTROL Create project]** [&#x200B; creeert een nieuw project van Workspace &#x200B;](#create-project-from-data-views) voor de gegevensmening.<br/>![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL Enable for Data Insights Agent]** om een gegevensmening voor Data Insights Agent toe te laten.<br/>![&#x200B; RemoveCircle &#x200B;](/help/assets/icons/RemoveCircle.svg) **[!UICONTROL Disable for Data Insights Agent]** om een gegevensmening voor Data Insights Agent onbruikbaar te maken. |
| **[!UICONTROL Connection]** | De naam van de verbinding die aan de gegevensweergave is gekoppeld. |
| **[!UICONTROL Sandbox]** | De naam van de sandbox die aan de gegevensweergave is gekoppeld. |
| **[!UICONTROL Owner]** | De eigenaar van de gegevensweergave. |
| **[!UICONTROL Data Insights Agent]** ![&#x200B; InfoOutline &#x200B;](/help/assets/icons/InfoOutline.svg) | Wijst erop of [&#x200B; Data Insights Agent &#x200B;](/help/data-analysis-ai.md) **[!UICONTROL Enabled]** of **[!UICONTROL Disabled]** voor de gegevensmening is. <br/> Uitgezochte ![&#x200B; InfoOutline &#x200B;](/help/assets/icons/InfoOutline.svg) om een pop-up met **[!UICONTROL Data Insights Agent Status]** over uw gegevensmeningen te tonen. <br/>![&#x200B; gebruik van Data Insights Agent &#x200B;](/help/data-views/assets/data-views-dia-status.png) |
| **[!UICONTROL Integrations]** | Maak een lijst van integratie met andere oplossingen. Bijvoorbeeld: Adobe Audience Analysis, Content Analytics, Brand Concierge, Journey Optimizer, GenStudio en Usage Analytics. |
| **[!UICONTROL Use in CJA]** | Geeft aan of de gegevensweergave wordt gebruikt in Customer Journey Analytics. Deze waarde is alleen **[!UICONTROL Off]** voor gegevensweergaven die automatisch worden gegenereerd als onderdeel van de Adobe Journey Optimizer-integratie. |
| **[!UICONTROL Date created]** | De tijdstempel op het moment dat de gegevensweergave is gemaakt. |
| **[!UICONTROL Last modified]** | De tijdstempel waarop de gegevensweergave voor het laatst is gewijzigd. |

Om te vormen welke kolommen in de lijst te tonen, selecteer ![&#x200B; ColumnSetting &#x200B;](/help/assets/icons/ColumnSetting.svg). Selecteer in het dialoogvenster **[!UICONTROL Customize table]** de kolommen die u wilt weergeven. Selecteer vervolgens **[!UICONTROL Apply]** .


## Weergaven van zoekgegevens

U kunt snel naar een gegevensmening zoeken gebruikend het ![&#x200B; vakje van het Onderzoek &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg).

## Gegevensweergaven filteren

Om een filter op de lijst van gegevensmeningen toe te passen, selecteer het ![&#x200B; pictogram van de Filter &#x200B;](/help/assets/icons/Filter.svg), dan uitgezocht van de volgende filteropties:

| Filter, optie | Beschrijving |
|---------|----------|
| **[!UICONTROL Connections]** | Alleen gegevensweergaven die zijn gekoppeld aan de verbindingen die u selecteert, worden weergegeven. |
| **[!UICONTROL Owner]** | Alleen gegevensweergaven die eigendom zijn van de personen die u selecteert, worden weergegeven. |
| **[!UICONTROL Sandbox]** | Alleen gegevensweergaven die beschikbaar zijn in de sandboxen die u selecteert, worden weergegeven. |
| **[!UICONTROL Integrations]** | Alleen gegevensweergaven met geselecteerde integratie worden weergegeven. |
| **[!UICONTROL Use in CJA]** | Selecteer **[!UICONTROL On]** om alleen gegevensweergaven weer te geven die zijn ingeschakeld voor gebruik met Customer Journey Analytics. Selecteer **[!UICONTROL Off]** om alleen gegevensweergaven weer te geven die nog niet zijn ingeschakeld voor gebruik met Customer Journey Analytics. |


Selecteer ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) **[!UICONTROL Hide filters]** om de filterruit te verbergen.

## Een gegevensweergave maken

Om [&#x200B; tot een nieuwe gegevensmening &#x200B;](/help/data-views/create-dataview.md) te leiden, selecteer **[!UICONTROL Create new data view]**.


## Gegevensweergaven bewerken

Als u [&#x200B; een gegevensmening &#x200B;](/help/data-views/create-dataview.md) wilt uitgeven:

1. Selecteer ![&#x200B; Meer &#x200B;](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![&#x200B; uitgeven &#x200B;](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** van het contextmenu.

U kunt ook:

1. Selecteer de rij van de gegevensmening.
1. Selecteer ![&#x200B; uitgeven &#x200B;](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** van de blauwe actiebar.


## Gegevensweergaven kopiëren

Als u een gegevensweergave wilt kopiëren:

1. Selecteer ![&#x200B; Meer &#x200B;](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![&#x200B; Exemplaar &#x200B;](/help/assets/icons/Copy.svg) **[!UICONTROL Copy]** van het contextmenu.

U kunt ook:

1. Selecteer een of meer gegevensweergaverijen.
1. Selecteer ![&#x200B; Exemplaar &#x200B;](/help/assets/icons/Copy.svg) **[!UICONTROL Copy]** van de blauwe actiebar.

De gegevensweergave wordt gekopieerd en aan de lijst toegevoegd met **[!UICONTROL (Copy)]** aan de naam.


## Gegevensweergaven verwijderen

Als u een gegevensweergave wilt verwijderen:

1. Selecteer ![&#x200B; Meer &#x200B;](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![&#x200B; Schrapping &#x200B;](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** van het contextmenu.

U kunt ook:

1. Selecteer een of meer gegevensweergaverijen.
1. Selecteer ![&#x200B; Schrapping &#x200B;](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** van de blauwe actiebar.

Wanneer u een of meer gegevensweergaven verwijdert, wordt in het deelvenster **[!UICONTROL Delete data view]** aangegeven welke projecten worden beïnvloed.

![&#x200B; de mening van Gegevens van de Schrapping &#x200B;](/help/data-views/assets/delete-data-view.png)


* In ➊ **[!UICONTROL Confirmation]** worden de implicaties van het verwijderen van de gegevensweergaven weergegeven.
* Selecteer **[!UICONTROL Delete]** om de gegevensweergaven permanent te verwijderen. Selecteer **[!UICONTROL Cancel]** om te annuleren.


## Gegevensweergaven exporteren naar CSV

U kunt een gegevensweergave exporteren naar een CSV-bestand.

1. Selecteer ![&#x200B; Meer &#x200B;](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![&#x200B; FileCSV &#x200B;](/help/assets/icons/FileCSV.svg) **[!UICONTROL Export to CSV]** van het contextmenu.

U kunt ook:

1. Selecteer een of meer gegevensweergaverijen.
1. Selecteer ![&#x200B; FileCSV &#x200B;](/help/assets/icons/FileCSV.svg) **[!UICONTROL Export to CSV]** van de blauwe actiebar.

Details van de geselecteerde gegevensweergaven worden geëxporteerd naar een CSV-bestand met de naam `Data views List (x).csv` in de map Downloads van uw browser.


## Project maken van gegevensweergaven

U kunt een Workspace-project rechtstreeks maken via de interface voor gegevensweergaven.

1. Selecteer ![&#x200B; Meer &#x200B;](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![&#x200B; ProjectAdd &#x200B;](/help/assets/icons/ProjectAdd.svg) **[!UICONTROL Create project]** van het contextmenu.

U kunt ook:

1. Selecteer een rij in de gegevensweergave.
1. Selecteer ![&#x200B; ProjectAdd &#x200B;](/help/assets/icons/ProjectAdd.svg) **[!UICONTROL Create project]** van de blauwe actiebar.


## Gegevensweergaven in- of uitschakelen voor Data Insights Agent

U kunt een gegevensmening voor [&#x200B; Data Insights Agent &#x200B;](/help/data-analysis-ai.md) toelaten of onbruikbaar maken.

1. Selecteer ![&#x200B; Meer &#x200B;](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL Enable for Data Insights Agent]** of ![&#x200B; RemoveCircle &#x200B;](/help/assets/icons/RemoveCircle.svg) **[!UICONTROL Disable for Data Insights Agent]** van het contextmenu.

U kunt ook:

1. Selecteer een of meer gegevensweergaverijen die zijn uitgeschakeld of ingeschakeld voor de Data Insights Agent.
1. Selecteer ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) **[!UICONTROL Enable for Data Insights Agent]** of ![&#x200B; RemoveCircle &#x200B;](/help/assets/icons/RemoveCircle.svg) **[!UICONTROL Disable for Data Insights Agent]** van de blauwe actiebar.
