---
description: Waarschuwingen maken, bewerken of verwijderen.
title: Aletten beheren
feature: Workspace Basics
role: User, Admin
source-git-commit: 6a279ac39e6b94200ff93ac1a3796d202e6349c7
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Waarschuwingen beheren


U kunt waarschuwingen filteren, labelen, verwijderen, hernoemen, kopiëren, inschakelen, vernieuwen uitschakelen en exporteren vanuit een centrale beheerinterface van [!UICONTROL Alerts] . Waarschuwingen beheren:

* Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer vervolgens **[!UICONTROL Alerts]** .

De manager van het Alarm is zeer gestructureerd zoals de [ manager van de Filter ](/help/components/filters/manage-filters.md) en [ Berekende metrische manager ](/help/components/calc-metrics/cm-workflow/cm-manager.md).


## Waarschuwingenbeheer

De manager van Alarm heeft de volgende interfaceelementen:

![ de interface van Filters ](assets/alerts-manager.png)

### Waarschuwingenlijst

In de lijst met waarschuwingen ➊ alle waarschuwingen worden weergegeven die u hebt, de waarschuwingen die binnen het bereik van al uw projecten vallen en de waarschuwingen die met u zijn gedeeld. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
|---|---|
| ![ StarOutline ](/help/assets/icons/StarOutline.svg) | Selecteer om ![ Ster ](/help/assets/icons/Star.svg) of niet-gunst ![ StarOutline ](/help/assets/icons/StarOutline.svg) een alarm te begunstigen. |
| **[!UICONTROL Title and description]** | Om het alarm uit te geven, selecteer de titelverbinding, die de [ bouwer van Alarm ](alert-builder.md#alert-builder) opent. |
| **[!UICONTROL Type]** | Toont of het alarm een alarm van het de vraaggebruik van de Customer Journey Analytics of een alarm van het de vraaggebruik van de Server is. |
| **[!UICONTROL Enabled]** | Geeft aan of de waarschuwing is in- of uitgeschakeld. |
| **[!UICONTROL Data view]** | De gegevensweergaven waarop deze waarschuwing van toepassing is. |
| **[!UICONTROL Owner]** | De eigenaar van de waarschuwing. Als niet-beheerder, ziet u slechts alarm u bezit of die die met u worden gedeeld. |
| **[!UICONTROL Tags]** | De tags voor deze waarschuwing. |
| **[!UICONTROL Expiration Date]** | De datum en tijd waarop de waarschuwing is ingesteld op verlopen. |
| **[!UICONTROL Date modified]** | De datum en het tijdstip waarop de waarschuwing voor het laatst is gewijzigd. |

<!-- When "Last used" column is added, add this information as the description: Shows the date when the alert was last used. <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li></ul> -->

Gebruik ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om te specificeren welke kolommen u wilt tonen.

### Actiebalk

U kunt actie ondernemen bij waarschuwingen met behulp van de ➋. De actiebalk bevat de volgende handelingen:

| Pictogram | Handeling | Beschrijving |
|:---:|---|---|
| ![ AddCircle ](/help/assets/icons/AddCircle.svg) | **[!UICONTROL Add]** | Voeg een ander alarm toe, gebruikend de [ Waakzame bouwer ](alert-builder.md#alert-builder). |
| ![ Onderzoek ](/help/assets/icons/Search.svg) | [!UICONTROL *Onderzoek door titel*] | Wanneer er geen waarschuwing in de lijst is geselecteerd, zoekt u naar waarschuwingen met dit zoekveld. |
| ![ Etiket ](/help/assets/icons/Label.svg) | **[!UICONTROL Tag]** | Label de geselecteerde waarschuwingen. Selecteer in het dialoogvenster **[!UICONTROL Tag Alert]** de tags voor de geselecteerde waarschuwingen of hef de selectie hiervan op. Selecteer **[!UICONTROL Save]** om de labels voor de geselecteerde waarschuwingen op te slaan. |
| ![ Schrapping ](/help/assets/icons/Delete.svg) | **[!UICONTROL Delete]** | Verwijder de geselecteerde waarschuwingen. U wordt gevraagd om een bevestiging. |
| ![ geeft ](/help/assets/icons/Edit.svg) uit | **[!UICONTROL Rename]** | Wijzig de naam van één geselecteerde waarschuwing. Als deze optie is geselecteerd, kunt u de naam van de waarschuwing inline wijzigen. |
| ![ Exemplaar ](/help/assets/icons/Copy.svg) | **[!UICONTROL Copy]** | Kopieer de geselecteerde waarschuwing. Nieuwe waarschuwingen worden gemaakt met dezelfde naam en hetzelfde achtervoegsel `(Copy)` . |
| ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | **[!UICONTROL Enable]** of **[!UICONTROL Disable]** | Schakel de geselecteerde waarschuwingen in of uit. |
| ![ verfrissen zich ](/help/assets/icons/Refresh.svg) | **[!UICONTROL Renew]** | Hiermee wordt de vervaldatum van de waarschuwing vernieuwd. De vervaldatum is 1 jaar vanaf de dag waarop u deze optie selecteert, ongeacht de oorspronkelijke vervaldatum. |
| ![ FileCSV ](/help/assets/icons/FileCSV.svg) | **[!UICONTROL Export to CSV]** | Exporteer de waarschuwingen naar een `Alerts List.csv` -bestand. |


### Actieve filterbalk

De filterbalk ➌ de actieve filters weer die van het filterdeelvenster zijn toegepast op de lijst met waarschuwingen (indien aanwezig). U kunt een filter snel verwijderen gebruikend ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg). Als er meer dan één filter is opgegeven, kunt u alle filters verwijderen met **[!UICONTROL Remove all]** .


### Deelvenster Filter

U kunt de lijst van alarm filtreren gebruikend de ![ linker paneel➍ van de Filter ](/help/assets/icons/Filter.svg) **[!UICONTROL Filter]**. In het filterdeelvenster worden het type filter en het aantal waarschuwingen weergegeven die aan het specifieke filter voldoen.

{{filterspanel}}


#### Sectie Labels, filter

{{tagfiltersection}}


#### Sectie Gegevensweergavefilter

{{dataviewfiltersection}}


#### Sectie eigenaarfilter

{{ownerfiltersection}}


#### Ingeschakelde sectie voor statusfilter

{{enabledstatusfiltersection}}


#### Sectie Type filter

{{typefiltersection}}


#### Sectie Overige filters

{{otherfiltersfiltersection}}



## Waarschuwingen bewerken

U kunt een waarschuwing bewerken

* Selecteer in de [[!UICONTROL Alert] lijst ](#alerts-list) de titel van de waarschuwing.

U gebruikt de [ Waakzame bouwer ](alert-builder.md#alert-builder) om het alarm uit te geven.

## Een waarschuwing oplossen

Wanneer u een probleem met een waarschuwing oplost, geeft u het JID-nummer (Job Instance ID) op aan de ondersteuning van Adoben. Het JID-nummer bevindt zich onder aan het e-mailbericht dat u ontvangt.

![ Alert e-mail ](assets/alerts-email.PNG)
