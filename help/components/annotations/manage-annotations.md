---
title: Annotaties beheren
description: Annotaties beheren in Workspace.
feature: Components
exl-id: 12f2cc2f-477c-4f16-afdd-b0db84725b32
role: User
source-git-commit: 6a279ac39e6b94200ff93ac1a3796d202e6349c7
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 0%

---

# Annotaties beheren

U kunt annotaties delen, filteren, labelen, goedkeuren, kopiëren, verwijderen en annotaties markeren als favoriet vanuit een centrale beheerinterface van [!UICONTROL Annotations] . Annotaties beheren:

* Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer vervolgens **[!UICONTROL Annotations]** .


>[!NOTE]
>
>De annotaties die u binnen een specifiek Workspace-project maakt, worden niet weergegeven in de [!UICONTROL Annotations] -manager, tenzij u de annotatie beschikbaar hebt gemaakt voor al uw projecten.
>

## Annotatiebeheer

Het annotatiebeheer heeft de volgende interface-elementen:

![ de interface van Annotaties ](assets/annotations-manager.png)

### Lijst met annotaties

In de lijst met annotaties ➊ alle annotaties worden weergegeven die u hebt, de annotaties die zijn toegepast op al uw projecten en de annotaties die met u zijn gedeeld. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
| --- | --- | 
| ![ StarOutline ](/help/assets/icons/StarOutline.svg) | Selecteer om ![ Ster ](/help/assets/icons/Star.svg) of niet-gunst ![ StarOutline ](/help/assets/icons/StarOutline.svg) een aantekening te begunstigen. |
| **[!UICONTROL Title and description]** | Opgegeven in de Annotations Builder. Om de titel en de beschrijving uit te geven, selecteer de titelverbinding - opent de [ bouwer van Annotaties ](/help/components/annotations/create-annotations.md#annotation-builder). Een gedeelde annotatie wordt vermeld met ![ Aandeel ](/help/assets/icons/ShareAlt.svg). |
| **[!UICONTROL Data view]** | De gegevensweergaven waarop deze aantekening van toepassing is. |
| **[!UICONTROL Owner]** | De eigenaar van de aantekening. Als gebruiker ziet u alleen de annotaties die u hebt of de annotaties die met u worden gedeeld. |
| **[!UICONTROL Applied date range]** | De datum of het datumbereik waarop deze aantekening van toepassing is. |
| **[!UICONTROL Tags]** | De codes voor deze aantekening. |
| **[!UICONTROL Shared with]** | De personen of groepen waarmee u de annotatie hebt gedeeld. Selecteer deze optie om het dialoogvenster **[!UICONTROL Share Component]** te openen. |
| **[!UICONTROL Date modified]** | Geeft de datum en tijd weer waarop de annotatie voor het laatst is gewijzigd. |

{style="table-layout:auto"}

Gebruik ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om te specificeren welke kolommen u wilt tonen.

### Actiebalk

U kunt actie ondernemen op annotaties met behulp van het ➋ op de actiebalk. De actiebalk bevat de volgende handelingen:

| Pictogram | Handeling | Beschrijving |
|:--:|---|---|
| ![ AddCircle ](/help/assets/icons/AddCircle.svg) | **[!UICONTROL Add]** | Voeg een andere annotatie toe, gebruikend de [ bouwer van de Annotatie ](create-annotations.md#annotation-builder). |
| ![ Onderzoek ](/help/assets/icons/Search.svg) | [!UICONTROL *Onderzoek door titel*] | Wanneer er geen annotatie is geselecteerd in de lijst, zoekt u naar annotaties met dit zoekveld. |
| ![ Etiket ](/help/assets/icons/Label.svg) | **[!UICONTROL Tag]** | Label de geselecteerde annotaties. Selecteer in het dialoogvenster **[!UICONTROL Tag Component]** de tags voor de geselecteerde annotaties of hef de selectie hiervan op. Selecteer **[!UICONTROL Save]** om de labels voor de geselecteerde annotaties op te slaan. |
| ![ Aandeel ](/help/assets/icons/ShareAlt.svg) | **[!UICONTROL Share]** | Deel de geselecteerde annotaties. In de **[!UICONTROL Share Component]** dialoog, kunt u ![ Onderzoek ](/help/assets/icons/Search.svg) *individuen of groepen van het Onderzoek* of u kunt selecteren **[!UICONTROL Organization]** of **[!UICONTROL Groups]**. Selecteer **[!UICONTROL Save]** om deeldetails voor de geselecteerde annotaties op te slaan. Zie [ Annotaties van het Aandeel ](#share-annotations) voor meer details. |
| ![ Schrapping ](/help/assets/icons/Delete.svg) | **[!UICONTROL Delete]** | Verwijder de geselecteerde annotaties. U wordt gevraagd om een bevestiging. |
| ![ geeft ](/help/assets/icons/Edit.svg) uit | **[!UICONTROL Rename]** | Wijzig de naam van één geselecteerde annotatie. Als deze optie is geselecteerd, kunt u de naam van de annotatie inline wijzigen. |
| ![ Exemplaar ](/help/assets/icons/Copy.svg) | **[!UICONTROL Copy]** | Kopieer de geselecteerde annotaties. Nieuwe annotaties worden gemaakt met dezelfde naam en hetzelfde achtervoegsel (kopie) |
| ![ FileCSV ](/help/assets/icons/FileCSV.svg) | **[!UICONTROL Export to CSV]** | Exporteer de annotaties naar een `Annotations List.csv` -bestand. |

### Actieve filterbalk

De filterbalk ➌ de actieve filters (indien aanwezig). U kunt een filter snel verwijderen gebruikend ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg). Als er meer dan één filter is opgegeven, kunt u alle filters verwijderen met **[!UICONTROL Remove all]** .

### Deelvenster Filter

U kunt annotaties filteren met de ➍ van het linkerdeelvenster van **[!UICONTROL Filter]** . In het filterdeelvenster worden het type filter en het aantal annotaties weergegeven die het filter respecteren. Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om de vertoning van het filterpaneel van een knevel te voorzien.

De lijst met filters filteren:

1. Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om het paneel van Filters te openen. Als u meer ruimte voor de lijst van Filters nodig hebt, kunt u ![ Filter ](/help/assets/icons/Filter.svg) selecteren opnieuw om het paneel te sluiten.
1. U kunt de annotaties filtreren gebruikend om het even welke beschikbare [ filtersecties ](#filter-sections).

   >[!INFO]
   >
   >*Punten* verwijzen naar de annotatie punten die in de [ lijst van Annotaties ](manage-annotations.md#annotations-list) worden getoond.
   > 

#### Secties filteren

{{tagfiltersection}}
{{dataviewfiltersection}}
{{ownerfiltersection}}
{{daterangefiltersection}}
{{otherfiltersfiltersection}}


De [ lijst van Annotaties ](manage-annotations.md#annotations-list) wordt automatisch bijgewerkt gebaseerd op uw filterconfiguratie. U kunt de gevormde filters in de [ Actieve filterbar ](manage-annotations.md#active-filter-bar) zien.


## Annotaties bewerken

U kunt een annotatie op twee manieren bewerken:

* In een project van Workspace, gebruik het [ pictogram van de Component info ](/help/components/use-components-in-workspace.md#component-info).

* Selecteer in de [[!UICONTROL Annotations] lijst ](#annotations-list) de titel van de annotatie.

U gebruikt de [ bouwer van de Annotatie ](/help/components/annotations/create-annotations.md#annotation-builder) om de annotatie uit te geven.

## Annotaties delen

Het volgende is van toepassing wanneer u annotaties deelt of met annotaties werkt die met u worden gedeeld:

* Projectgebonden annotaties in een project dat u met andere gebruikers deelt, worden voor die gebruikers weergegeven. De gebruikers kunnen deze alleen-projectnotities niet bewerken of verwijderen.
* Als u een annotatie opslaat en de annotatie rechtstreeks met een gebruiker deelt, kan die gebruiker de annotatie alleen bewerken en verwijderen als die gebruiker beheerdersrechten heeft.

* Als een project met u wordt gedeeld, verschijnen de annotaties die in dat project worden gecreeerd slechts in dat project. Als een annotatie rechtstreeks met u wordt gedeeld, wordt de annotatie weergegeven in alle projecten waarin die annotatie kan worden weergegeven.

## Aantekeningen en tijdzones

Alle annotaties worden gemaakt met een tijdstempel, maar geen uur- of tijdzonegegevens. Op rapporttijd, wordt de tijdzone van de gegevensmening gebruikt die voor het paneel wordt gevormd.
