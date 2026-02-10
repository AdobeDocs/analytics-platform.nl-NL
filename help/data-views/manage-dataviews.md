---
title: Gegevensweergaven beheren
description: Leer hoe u gegevensweergaven beheert.
solution: Customer Journey Analytics
feature: Data Views
role: Admin
exl-id: c5cf15ab-3eb1-4e6b-93a3-3d89694ca0ea
source-git-commit: c7cf7250f30e2f6023aa7690391aea149ba12eff
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 0%

---

# Gegevensweergaven beheren


Zodra u [ creeerde of uitgegeven één of meerdere gegevensmeningen ](/help/data-views/create-dataview.md) hebt, kunt u hen in **[!UICONTROL Data views]** beheren.

Selecteer **[!UICONTROL Data Management]** > **[!UICONTROL Data views]** in de hoofdmenubalk in Customer Journey Analytics.

De interface **[!UICONTROL Data views]** toont een lijst van alle beschikbare gegevensmeningen.

![ de meningsinterface van Gegevens ](/help/data-views/assets/data-views.png)

De volgende kolommen en pictogrammen zijn beschikbaar in de tabel:

| Kolom of pictogram | Beschrijving |
| --- | --- |
| **[!UICONTROL Name]** | De naam van de gegevensweergave. |
| ![ Informatie ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg) | Om informatie over de gegevensmening te bekijken, selecteer ![ InfoOutline ](/help/assets/icons/InfoOutline.svg) naast de naam van de gegevensmening.<br/> pop-up venster van A toont details over de gegevensmening. |
| ![ Meer ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_More_18_N.svg) | Selecteer ![ Meer ](/help/assets/icons/More.svg) om een contextmenu te openen. U kunt selecteren:<br/>![ geeft ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** uit [ ](#edit-data-views) een gegevensmening uit.<br/>![ Exemplaar ](/help/assets/icons/Copy.svg) **[!UICONTROL Copy]** aan [ kopieert een gegevensmening ](#copy-data-views).<br/>![ Schrapping ](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** aan [ schrap ](#delete-data-views) een gegevensmening.<br/>![ FileCSV ](/help/assets/icons/FileCSV.svg) **[!UICONTROL Export to CSV]** aan [ voer de details van de gegevensmening naar een Csv- dossier ](#export-data-views-to-csv) uit.<br/>![ ProjectAdd ](/help/assets/icons/ProjectAdd.svg) **[!UICONTROL Create project]** [ creeert een nieuw project van Workspace ](#create-project-from-data-views) voor de gegevensmening.<br/>![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Enable for Data Insights Agent]** om een gegevensmening voor Data Insights Agent toe te laten.<br/>![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) **[!UICONTROL Disable for Data Insights Agent]** om een gegevensmening voor Data Insights Agent onbruikbaar te maken. |
| **[!UICONTROL Connection]** | De naam van de verbinding die aan de gegevensweergave is gekoppeld. |
| **[!UICONTROL Sandbox]** | De naam van de sandbox die aan de gegevensweergave is gekoppeld. |
| **[!UICONTROL Owner]** | De eigenaar van de gegevensweergave. |
| **[!UICONTROL Data Insights Agent]** ![ InfoOutline ](/help/assets/icons/InfoOutline.svg) | Wijst erop of [ Data Insights Agent ](/help/data-analysis-ai.md) **[!UICONTROL Enabled]** of **[!UICONTROL Disabled]** voor de gegevensmening is. <br/> Uitgezochte ![ InfoOutline ](/help/assets/icons/InfoOutline.svg) om een pop-up met **[!UICONTROL Data Insights Agent Status]** over uw gegevensmeningen te tonen. <br/>![ gebruik van Data Insights Agent ](/help/data-views/assets/data-views-dia-status.png) |
| **[!UICONTROL Integrations]** | Maak een lijst van integratie met andere oplossingen. Bijvoorbeeld: Adobe Audience Analysis, Content Analytics, Brand Concierge, Journey Optimizer, GenStudio en Usage Analytics. |
| **[!UICONTROL Use in CJA]** | Geef aan of de gegevensweergave wordt gebruikt in Customer Journey Analytics. Deze waarde is alleen **[!UICONTROL Off]** voor gegevensweergaven die automatisch worden gegenereerd als onderdeel van de Adobe Journey Optimizer-integratie. |
| **[!UICONTROL Date created]** | De tijdstempel op het moment dat de gegevensweergave is gemaakt. |
| **[!UICONTROL Last modified]** | De tijdstempel waarop de gegevensweergave voor het laatst is gewijzigd. |

Om te vormen welke kolommen in de lijst te tonen, selecteer ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg). Selecteer in het dialoogvenster **[!UICONTROL Customize table]** de kolommen die u wilt weergeven. Selecteer vervolgens **[!UICONTROL Apply]** .


## Weergaven van zoekgegevens

U kunt snel naar een gegevensmening zoeken gebruikend het ![ vakje van het Onderzoek ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg).

## Gegevensweergaven filteren

Om een filter op de lijst van gegevensmeningen toe te passen, selecteer het ![ pictogram van de Filter ](/help/assets/icons/Filter.svg), dan uitgezocht van de volgende filteropties:

| Filter, optie | Beschrijving |
|---------|----------|
| **[!UICONTROL Connections]** | Alleen gegevensweergaven die zijn gekoppeld aan de verbindingen die u selecteert, worden weergegeven. |
| **[!UICONTROL Owner]** | Alleen gegevensweergaven die eigendom zijn van de personen die u selecteert, worden weergegeven. |
| **[!UICONTROL Sandbox]** | Alleen gegevensweergaven die beschikbaar zijn in de sandboxen die u selecteert, worden weergegeven. |
| **[!UICONTROL Integrations]** | Alleen gegevensweergaven met geselecteerde integratie worden weergegeven. |
| **[!UICONTROL Use in CJA]** | Selecteer **[!UICONTROL On]** om alleen gegevensweergaven weer te geven die zijn ingeschakeld voor gebruik met Customer Journey Analytics. Selecteer **[!UICONTROL Off]** om alleen gegevensweergaven weer te geven die nog niet zijn ingeschakeld voor gebruik met Customer Journey Analytics. |


Selecteer ![ Filter ](/help/assets/icons/Filter.svg) **[!UICONTROL Hide filters]** om de filterruit te verbergen.

## Een gegevensweergave maken

Om [ tot een nieuwe gegevensmening ](/help/data-views/create-dataview.md) te leiden, selecteer **[!UICONTROL Create new data view]**.


## Gegevensweergaven bewerken

Als u [ een gegevensmening ](/help/data-views/create-dataview.md) wilt uitgeven:

1. Selecteer ![ Meer ](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![ uitgeven ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** van het contextmenu.

U kunt ook:

1. Selecteer de rij van de gegevensmening.
1. Selecteer ![ uitgeven ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** van de blauwe actiebar.


## Gegevensweergaven kopiëren

Als u een gegevensweergave wilt kopiëren:

1. Selecteer ![ Meer ](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![ Exemplaar ](/help/assets/icons/Copy.svg) **[!UICONTROL Copy]** van het contextmenu.

U kunt ook:

1. Selecteer een of meer gegevensweergaverijen.
1. Selecteer ![ Exemplaar ](/help/assets/icons/Copy.svg) **[!UICONTROL Copy]** van de blauwe actiebar.

De gegevensweergave wordt gekopieerd en aan de lijst toegevoegd met **[!UICONTROL (Copy)]** aan de naam.


## Gegevensweergaven verwijderen

Als u een gegevensweergave wilt verwijderen:

1. Selecteer ![ Meer ](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![ Schrapping ](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** van het contextmenu.

U kunt ook:

1. Selecteer een of meer gegevensweergaverijen.
1. Selecteer ![ Schrapping ](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** van de blauwe actiebar.

Wanneer u een of meer gegevensweergaven verwijdert, wordt in het deelvenster **[!UICONTROL Delete data view]** aangegeven welke projecten worden beïnvloed.

![ de mening van Gegevens van de Schrapping ](/help/data-views/assets/delete-data-view.png)


* In ➊ **[!UICONTROL Confirmation]** worden de implicaties van het verwijderen van de gegevensweergaven weergegeven.
* Selecteer **[!UICONTROL Delete]** om de gegevensweergaven permanent te verwijderen. Selecteer **[!UICONTROL Cancel]** om te annuleren.


## Gegevensweergaven exporteren naar CSV

U kunt een gegevensweergave exporteren naar een CSV-bestand.

1. Selecteer ![ Meer ](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![ FileCSV ](/help/assets/icons/FileCSV.svg) **[!UICONTROL Export to CSV]** van het contextmenu.

U kunt ook:

1. Selecteer een of meer gegevensweergaverijen.
1. Selecteer ![ FileCSV ](/help/assets/icons/FileCSV.svg) **[!UICONTROL Export to CSV]** van de blauwe actiebar.

Details van de geselecteerde gegevensweergaven worden geëxporteerd naar een CSV-bestand met de naam `Data views List (x).csv` in de map Downloads van uw browser.


## Project maken van gegevensweergaven

U kunt een Workspace-project rechtstreeks maken via de interface voor gegevensweergaven.

1. Selecteer ![ Meer ](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![ ProjectAdd ](/help/assets/icons/ProjectAdd.svg) **[!UICONTROL Create project]** van het contextmenu.

U kunt ook:

1. Selecteer een rij in de gegevensweergave.
1. Selecteer ![ ProjectAdd ](/help/assets/icons/ProjectAdd.svg) **[!UICONTROL Create project]** van de blauwe actiebar.


## Gegevensweergaven in- of uitschakelen voor Data Insights Agent

U kunt een gegevensmening voor [ Data Insights Agent ](/help/data-analysis-ai.md) toelaten of onbruikbaar maken.

1. Selecteer ![ Meer ](/help/assets/icons/More.svg) naast de naam van de gegevensmening.
1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Enable for Data Insights Agent]** of ![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) **[!UICONTROL Disable for Data Insights Agent]** van het contextmenu.

U kunt ook:

1. Selecteer een of meer gegevensweergaverijen die zijn uitgeschakeld of ingeschakeld voor de Data Insights Agent.
1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Enable for Data Insights Agent]** of ![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) **[!UICONTROL Disable for Data Insights Agent]** van de blauwe actiebar.
