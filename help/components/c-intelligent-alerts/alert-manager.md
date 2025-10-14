---
description: Leer hoe u waarschuwingen beheert.
title: Waarschuwingen beheren
feature: Workspace Basics
role: User, Admin
exl-id: 174c3ebd-a77b-4403-ae9a-bb0cff4bcca6
source-git-commit: 1891f73f4326a178b293e7c3763d0d1dbc000a25
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%

---

# Waarschuwingen beheren


U kunt waarschuwingen filteren, labelen, verwijderen, hernoemen, kopiëren, inschakelen, vernieuwen uitschakelen en exporteren vanuit een centrale beheerinterface van [!UICONTROL Alerts] . Waarschuwingen beheren:

* Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer vervolgens **[!UICONTROL Alerts]** .

De manager van het Alarm is gestructureerd als de [&#x200B; manager van het Segment &#x200B;](/help/components/segments/seg-manage.md) en [&#x200B; Berekende metrische manager &#x200B;](/help/components/calc-metrics/cm-workflow/cm-manager.md).


## Waarschuwingenbeheer

De manager van Alarm heeft de volgende interfaceelementen:

![&#x200B; de interface van Filters &#x200B;](assets/alerts-manager.png)

### Waarschuwingenlijst

In de lijst met waarschuwingen ➊ worden alle waarschuwingen weergegeven die u hebt, de waarschuwingen die betrekking hebben op al uw projecten en de waarschuwingen die met u zijn gedeeld. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
|---|---|
| ![&#x200B; StarOutline &#x200B;](/help/assets/icons/StarOutline.svg) | Selecteer om ![&#x200B; Ster &#x200B;](/help/assets/icons/Star.svg) of niet-gunst ![&#x200B; StarOutline &#x200B;](/help/assets/icons/StarOutline.svg) een alarm te begunstigen. |
| **[!UICONTROL Title and description]** | Om het alarm uit te geven, selecteer de titelverbinding, die de [&#x200B; bouwer van Alarm &#x200B;](alert-builder.md#alert-builder) opent. |
| **[!UICONTROL Type]** | Toont of het alarm een het gegevensalarm van Customer Journey Analytics of een het vraaggebruik van de Server alarm is. |
| **[!UICONTROL Enabled]** | Geeft aan of de waarschuwing is in- of uitgeschakeld. |
| **[!UICONTROL Data view]** | De gegevensweergaven waarop deze waarschuwing van toepassing is. |
| **[!UICONTROL Owner]** | De eigenaar van de waarschuwing. Als niet-beheerder, ziet u slechts alarm u bezit of die die met u worden gedeeld. |
| **[!UICONTROL Tags]** | De tags voor deze waarschuwing. |
| **[!UICONTROL Expiration Date]** | De datum en tijd waarop de waarschuwing is ingesteld op verlopen. |
| **[!UICONTROL Date modified]** | De datum en het tijdstip waarop de waarschuwing voor het laatst is gewijzigd. |

<!-- When "Last used" column is added, add this information as the description: Shows the date when the alert was last used. <p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li></ul> -->

Gebruik ![&#x200B; ColumnSetting &#x200B;](/help/assets/icons/ColumnSetting.svg) om te specificeren welke kolommen u wilt tonen.

### Actiebalk

U kunt actie ondernemen bij waarschuwingen met de actiebalk ➋ . De actiebalk bevat de volgende handelingen:

| Pictogram | Handeling | Beschrijving |
|:---:|---|---|
| ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) | **[!UICONTROL Add]** | Voeg een ander alarm toe, gebruikend de [&#x200B; Waakzame bouwer &#x200B;](alert-builder.md#alert-builder). |
| ![&#x200B; Onderzoek &#x200B;](/help/assets/icons/Search.svg) | [!UICONTROL *Onderzoek door titel*] | Wanneer er geen waarschuwing in de lijst is geselecteerd, zoekt u naar waarschuwingen met dit zoekveld. |
| ![&#x200B; Etiket &#x200B;](/help/assets/icons/Label.svg) | **[!UICONTROL Tag]** | Label de geselecteerde waarschuwingen. Selecteer in het dialoogvenster **[!UICONTROL Tag Alert]** de tags voor de geselecteerde waarschuwingen of hef de selectie hiervan op. Selecteer **[!UICONTROL Save]** om de labels voor de geselecteerde waarschuwingen op te slaan. |
| ![&#x200B; Schrapping &#x200B;](/help/assets/icons/Delete.svg) | **[!UICONTROL Delete]** | Verwijder de geselecteerde waarschuwingen. U wordt gevraagd om een bevestiging. |
| ![&#x200B; geeft &#x200B;](/help/assets/icons/Edit.svg) uit | **[!UICONTROL Rename]** | Wijzig de naam van één geselecteerde waarschuwing. Als deze optie is geselecteerd, kunt u de naam van de waarschuwing inline wijzigen. |
| ![&#x200B; Exemplaar &#x200B;](/help/assets/icons/Copy.svg) | **[!UICONTROL Copy]** | Kopieer de geselecteerde waarschuwing. Nieuwe waarschuwingen worden gemaakt met dezelfde naam en hetzelfde achtervoegsel `(Copy)` . |
| ![&#x200B; CheckmarkCircle &#x200B;](/help/assets/icons/CheckmarkCircle.svg) | **[!UICONTROL Enable]** of **[!UICONTROL Disable]** | Schakel de geselecteerde waarschuwingen in of uit. |
| ![&#x200B; verfrissen zich &#x200B;](/help/assets/icons/Refresh.svg) | **[!UICONTROL Renew]** | Hiermee wordt de vervaldatum van de waarschuwing vernieuwd. De vervaldatum is 1 jaar vanaf de dag waarop u deze optie selecteert, ongeacht de oorspronkelijke vervaldatum. |
| ![&#x200B; FileCSV &#x200B;](/help/assets/icons/FileCSV.svg) | **[!UICONTROL Export to CSV]** | Exporteer de waarschuwingen naar een `Alerts List.csv` -bestand. |


### Actieve filterbalk

De filterbalk ➌ geeft de actieve filters weer die van het filterdeelvenster zijn toegepast op de lijst met waarschuwingen (indien aanwezig). U kunt een filter snel verwijderen gebruikend ![&#x200B; CrossSize75 &#x200B;](/help/assets/icons/CrossSize75.svg). Als er meer dan één filter is opgegeven, kunt u alle filters verwijderen met **[!UICONTROL Remove all]** .


### Deelvenster Filter

U kunt de lijst van alarm filtreren gebruikend het ![&#x200B; Linkerpaneel van de Filter &#x200B;](/help/assets/icons/Filter.svg) **[!UICONTROL Filter]** ➍. In het filterdeelvenster worden het type filter en het aantal waarschuwingen weergegeven die aan het specifieke filter voldoen.


1. Selecteer ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) om het paneel van Filters te openen. Als u meer ruimte voor de lijst van Alarm nodig hebt, kunt u ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) selecteren opnieuw om het paneel te sluiten.
1. Selecteer filters uit een van de beschikbare filtersecties.


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

* Selecteer in de [[!UICONTROL Alert] lijst &#x200B;](#alerts-list) de titel van de waarschuwing.

U gebruikt de [&#x200B; Waakzame bouwer &#x200B;](alert-builder.md#alert-builder) om het alarm uit te geven.

## Een waarschuwing oplossen

Geef Adobe Support het JID-nummer (Job Instance ID) op wanneer u een probleem met een waarschuwing oplost. Het JID-nummer bevindt zich onder aan het e-mailbericht dat u ontvangt.

![&#x200B; Alert e-mail &#x200B;](assets/alerts-email.PNG)
