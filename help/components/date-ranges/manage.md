---
title: Datumbereiken beheren
description: U kunt datumbereiken delen, hernoemen of verwijderen in Analysis Workspace.
feature: Calendar
exl-id: 694758c4-d740-4fd7-9fb0-3ff7f6b25a3d
role: User
source-git-commit: 6a279ac39e6b94200ff93ac1a3796d202e6349c7
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%

---

# Datumbereiken beheren


U kunt datumbereiken en datumbereiken als favorieten delen, filteren, labelen, goedkeuren, kopiëren, delen en verwijderen vanuit een centrale beheerinterface van [!UICONTROL Date ranges] . Datumbereiken beheren:

* Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer vervolgens **[!UICONTROL Date ranges]** .


## Datumbereikbeheer

De manager van de waaiers van de Datum heeft de volgende interface elementen:

![ de waaiers van de Datum interface ](assets/date-ranges-manager.png)

### Lijst met datumbereiken

In de lijst met datumbereiken ➊ worden alle datumbereiken weergegeven. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
| --- | --- | 
| ![ StarOutline ](/help/assets/icons/StarOutline.svg) | Selecteer om ![ Ster ](/help/assets/icons/Star.svg) of niet-gunst ![ StarOutline ](/help/assets/icons/StarOutline.svg) een datumwaaier te begunstigen. |
| **[!UICONTROL Title and description]** | Om de titel en de beschrijving uit te geven, selecteer de titelverbinding, die de [ de waaierbouwer van de Datum ](/help/components/date-ranges/create.md#date-range-builder) opent. |
| **[!UICONTROL Owner]** | De eigenaar van het datumbereik. |
| **[!UICONTROL Tags]** | De labels voor dit datumbereik. |
| **[!UICONTROL Shared with]** | De personen of groepen met wie u het datumbereik hebt gedeeld. Selecteer deze optie om het dialoogvenster **[!UICONTROL Share Date range]** te openen. |
| **[!UICONTROL Date modified]** | Geeft de datum en tijd weer waarop het datumbereik voor het laatst is gewijzigd. |

{style="table-layout:auto"}

Gebruik ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om te specificeren welke kolommen u wilt tonen.

### Actiebalk

U kunt op datumbereiken actie ondernemen met de ➋ van de actiebalk. De actiebalk bevat de volgende handelingen:

| Pictogram | Handeling | Beschrijving |
|:---:|---|---|
| ![ AddCircle ](/help/assets/icons/AddCircle.svg) | **[!UICONTROL Add]** | Voeg een andere datumwaaier toe, gebruikend de [ de waaierbouwer van de Datum ](create.md#date-range-builder). |
| ![ Onderzoek ](/help/assets/icons/Search.svg) | [!UICONTROL *Onderzoek door titel*] | Wanneer er geen datumbereik is geselecteerd in de lijst, zoekt u naar datumbereiken met dit zoekveld. |
| ![ Etiket ](/help/assets/icons/Label.svg) | **[!UICONTROL Tag]** | Label de geselecteerde datumbereiken. Selecteer in het dialoogvenster **[!UICONTROL Tag Date range]** de tags voor de geselecteerde datumbereiken of hef de selectie hiervan op. Selecteer **[!UICONTROL Save]** om de labels voor de geselecteerde datumbereiken op te slaan. |
| ![ Aandeel ](/help/assets/icons/ShareAlt.svg) | **[!UICONTROL Share]** | Deel de geselecteerde datumbereiken. In de **[!UICONTROL Share Date range]** dialoog, kunt u ![ Onderzoek ](/help/assets/icons/Search.svg) *individuen of groepen van het Onderzoek* of u kunt selecteren **[!UICONTROL Organization]** of **[!UICONTROL Groups]**. Selecteer **[!UICONTROL Save]** om de deelgegevens voor de geselecteerde datumbereiken op te slaan. |
| ![ Schrapping ](/help/assets/icons/Delete.svg) | **[!UICONTROL Delete]** | Verwijder de geselecteerde datumbereiken. U wordt gevraagd om een bevestiging. |
| ![ geeft ](/help/assets/icons/Edit.svg) uit | **[!UICONTROL Rename]** | Wijzig de naam van één geselecteerd datumbereik. Als deze optie is geselecteerd, kunt u de naam van het datumbereik inline wijzigen. |
| ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | **[!UICONTROL Approve]** | Geef de geselecteerde datumbereiken goed. |
| ![ Exemplaar ](/help/assets/icons/Copy.svg) | **[!UICONTROL Copy]** | Kopieer de geselecteerde datumbereiken. Nieuwe datumbereiken worden gemaakt met dezelfde naam en hetzelfde achtervoegsel (kopie) |
| ![ FileCSV ](/help/assets/icons/FileCSV.svg) | **[!UICONTROL Export to CSV]** | Exporteer de geselecteerde datumbereiken naar een `Date ranges List.csv` -bestand. |

### Actieve filterbalk

De filterbalk ➌ de actieve filters (indien aanwezig). U kunt een filter snel verwijderen gebruikend ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg). Als er meer dan één filter is opgegeven, gebruikt u **[!UICONTROL Remove all]** om alle filters te verwijderen.

### Deelvenster Filter

U kunt datumbereiken filteren met de ➍ van het linkerdeelvenster van **[!UICONTROL Filter]** . In het filterdeelvenster worden het type filter en het aantal datumbereiken weergegeven die aan het filter voldoen. Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om de vertoning van het filterpaneel van een knevel te voorzien.

De lijst met filters filteren:

1. Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om het paneel van Filters te openen. Als u meer ruimte voor de lijst van Filters nodig hebt, kunt u ![ Filter ](/help/assets/icons/Filter.svg) selecteren opnieuw om het paneel te sluiten.
1. U kunt de datumwaaiers filtreren gebruikend om het even welke beschikbare [ filtersecties ](#filter-sections).

   >[!INFO]
   >
   >*Punten* verwijzen naar de punten van de datumwaaier die in de [ lijst van de waaiers van de Datum ](#date-ranges-list) worden getoond.
   > 

#### Secties filteren

{{tagfiltersection}}
{{ownerfiltersection}}
{{otherfiltersfiltersection}}


De [ lijst van de waaiers van de Datum ](#date-ranges-list) wordt automatisch bijgewerkt gebaseerd op uw filterconfiguratie. U kunt de gevormde filters in de [ Actieve filterbar ](#active-filter-bar) zien.


## Datumbereiken bewerken

U kunt een datumbereik op twee manieren bewerken:

* In een project van Workspace, gebruik het [ pictogram van de Component info ](/help/components/use-components-in-workspace.md#component-info).

* Selecteer in de [[!UICONTROL Date ranges] lijst ](#date-ranges-list) de titel van het datumbereik.

U gebruikt de [ de waaierbouwer van de Datum ](/help/components/date-ranges/create.md#date-range-builder) om de datumwaaier uit te geven.




Gebruik de manager van de datumwaaier om, datumwaaiers te delen anders te noemen of te schrappen. De datummanager bereiken:

1. Login aan [ analytics.adobe.com ](https://analytics.adobe.com) gebruikend uw geloofsbrieven van AdobeID.
1. Ga naar [!UICONTROL Components] > [!UICONTROL Date Ranges].


<!--

## Interface

![Date Ranges with Example range highlighted.](../assets/date-range-ui.png)

The date range manager includes the following options:

* **Add**: Create a new date range. See [create a date range](create.md) for more information.
* **Search by title**: Search for a date range by title. Results are filtered based on text entered here.
* **Filter**: Filter date ranges using the left column. You can filter by custom tag, owner, created by you, your favorites, approved, or shared with you. You can also search for desired filters.
* **Favorite**: Click the ![star](../assets/star.png) icon next to a date range to add it to your favorites.
* **Customize columns**: Click the ![columns](../assets/columns.png) icon to show or hide columns in the date range manager.

Click the checkbox next to one or more date ranges for more options.

* **Tag**: Apply a tag to all selected date ranges. Tags help you organize date ranges, and let you filter them using the left column.
* **Share**: Share a date range to other Experience Cloud users. If you are a product administrator, you can also share to the entire organization or groups. Date ranges that are shared to other users in your organization include a ![shared](../assets/shared.png) icon next to the title.
* **Delete**: Permanently delete the selected date range(s).
* **Rename**: If a single date range is selected, you can change its title.
* **Approve**: If you are a product admin, you can add a stamp of approval to a date range. Approved date ranges inform users in your organization that they are 'official', differentiating them from date ranges created by other users in your organization. Approved date ranges include a ![approved](../assets/approved.png) icon next to the title.
* **Unapprove**: If you are a product admin and select a date range that is already approved, you can unapprove it.
* **Copy**: Create a copy of the selected date range(s). Copying date ranges appends `(Copy)` to the end of the title of the newly copied date range(s).
* **Export to CSV**: Exports all selected date ranges into a CSV file. Columns in the resulting CSV file include all visible columns in the date range manager.
-->