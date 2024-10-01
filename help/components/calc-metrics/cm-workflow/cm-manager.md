---
description: Met de functie Berekende metrische elementen kunt u bestanden delen, filteren, labelen, goedkeuren, kopiëren, verwijderen en markeren als favorieten.
title: Berekende metrische manager
feature: Calculated Metrics
exl-id: 8b257ecc-a596-4b34-ac26-eda16835f1ba
source-git-commit: e07197325e992cd85b852899c2f7cef60637f532
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---

# Berekende waarden beheren

U kunt berekende metriek delen, filteren, labelen, goedkeuren, hernoemen, kopiëren, verwijderen, exporteren en berekende metriek markeren als favoriet vanuit een centrale beheerinterface van [!UICONTROL Calculated metrics] . Berekende waarden beheren:


* Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer vervolgens **[!UICONTROL Calculated metrics]** .


## Het berekende manager van metriek

Het Berekende manager van metriek heeft de volgende interfaceelementen:


![ de interface van Filters ](assets/calculated-metrics-manager.png)

### Filterlijst

In de lijst met filters ➊ worden alle berekende metriek weergegeven die u bezit of die met u hebt gedeeld. De lijst heeft de volgende kolommen:

<!-- I think this table incorrectly talks about quick calculated metrics -->

| Kolom | Beschrijving |
| --- | --- | 
| ![ StarOutline ](/help/assets/icons/StarOutline.svg) | Selecteer om ![ Ster ](/help/assets/icons/Star.svg) of niet-gunst ![ StarOutline ](/help/assets/icons/StarOutline.svg) te begunstigen berekende metrisch. Zie [ Metrisch berekend Teken als favoriet ](/help/components/filters/filters-favorite.md) |
| **[!UICONTROL Title and description]** | Om berekende metrisch uit te geven, selecteer de titelverbinding, die [ Berekende metriek bouwer ](cm-build-metrics.md) opent. Een gedeelde berekende metrische waarde wordt vermeld met ![ Aandeel ](/help/assets/icons/ShareLight.svg). |
| **[!UICONTROL Data view]** | De gegevensweergaven waarop deze berekende metrische waarde van toepassing is. |
| **[!UICONTROL Owner]** | Eigenaar van de berekende metrische waarde. Als gebruiker ziet u alleen de annotaties die u hebt of de annotaties die met u worden gedeeld. |
| **[!UICONTROL Tags]** | Hier worden de codes voor deze berekende metrische waarde weergegeven. |
| **[!UICONTROL Shared with]** | Hiermee geeft u aan met hoeveel personen of groepen u de berekende metrische waarde hebt gedeeld. Selecteer deze optie om het dialoogvenster **[!UICONTROL Share Calculated metric]** te openen. Zie [ Aandeel berekende metriek ](cm-sharing.md) voor meer informatie. |
| **[!UICONTROL Date modified]** | De datum en de tijd dat berekende metrisch het laatst werd gewijzigd. |
| **[!UICONTROL Used in]** | Hiermee kunt u zien waar berekende metriek momenteel worden gebruikt en hoe vaak deze in elk gebied worden gebruikt. <p>Bijvoorbeeld, als berekende metrisch in 40 projecten en 2 alarm wordt gebruikt, dan toont de waarde van deze kolom als [!UICONTROL **42 componenten**]. <p>Selecteer de waarde in deze kolom om de uitsplitsing te zien van waar de berekende metriek (bijvoorbeeld, [!UICONTROL **Projecten (40)**] worden gebruikt, [!UICONTROL **Mobiele Scorecards (2)**]). Bovendien kunt u de lijst van punten bekijken waar de berekende metriek worden gebruikt. Bijvoorbeeld, zie zo de lijst van projecten waar zij worden gebruikt, selecteer de [!UICONTROL **Projecten (40)**] verbinding.</p><p>Elk van de volgende gebieden toont het aantal instanties van berekende metriek die in dat gebied worden gebruikt:</p> <ul><li>[!UICONTROL **Projecten**]<p>Bevat berekende metriek die [ in de berekende metrische bouwer ](/help/components/calc-metrics/cm-workflow/cm-build-metrics.md) werden gecreeerd en voor alle projecten beschikbaar zijn.</p></li><li>[!UICONTROL **Ad hoc componenten**]<p>Bevat berekende metriek die [ als snelle berekende metriek ](/help/components/apply-create-metrics.md#create-calculated-metrics-for-a-single-project) werden gecreeerd en beschikbaar slechts binnen één enkel project zijn.</p></li><li>[!UICONTROL **Geplande projecten**]</li><li>[!UICONTROL **Mobiele Scorecards**]</li><li>[!UICONTROL **Annotaties**]</li><li>[!UICONTROL **Report Builder**]<p>Als u deze optie selecteert, wordt een CSV-bestand gedownload met de volgende kolommen gegevens:</p><ul><li>Naam Report Builder</li><li>Laatst geopend</li><li>Laatst geopende IMS-gebruikersnaam</li><li>Laatst geopende gebruikersnaam</li></ul></li></ul><p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd.</p><p>Houd rekening met het volgende wanneer u deze kolom weergeeft:</p><ul><li>Deze informatie is alleen beschikbaar voor systeembeheerders.</li><li>[!UICONTROL **Gebruikt in**] kolom toont niet door gebrek. Gebruik ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om de vertoning van deze kolom te vormen.</li><li>Deze informatie omvat geen gebruik van de API of Data Warehouse.</li><li>Als er geen gegevens in deze kolom voor een bepaalde component zijn maar het heeft a [!UICONTROL **laatst gebruikte**] datum, zou de component in een analyse kunnen worden gebruikt zonder worden bewaard.</li><li>Gebruiksgegevens zijn beschikbaar vanaf september 2023.</li></ul><p>U kunt het [ Woordenboek van Gegevens ](/help/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie gebruiken om u spoor van te houden en beter te begrijpen hoe de componenten in uw organisatie worden gebruikt.</p> |
| **[!UICONTROL Last Used]** | Wanneer de berekende metrische waarde het laatst werd gebruikt. |

{style="table-layout:auto"}

Gebruik ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om te specificeren welke kolommen u wilt tonen.

### Actiebalk

U kunt op filters actie ondernemen met de ➋ van de actiebalk. De actiebalk bevat de volgende handelingen:

| Handeling | Beschrijving |
|---|---|
| ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add]** | Voeg een andere berekende metriek toe, gebruikend [ Berekende metrische bouwer ](cm-build-metrics.md). |
| ![ Onderzoek ](/help/assets/icons/Search.svg) [!UICONTROL *Onderzoek door titel*] | Wanneer er geen berekende metrisch is geselecteerd in de lijst, zoekt u naar filters met dit zoekveld. |
| ![ Etiket ](/help/assets/icons/Label.svg) **[!UICONTROL Tag]** | Label de geselecteerde berekende metriek. Selecteer in het dialoogvenster **[!UICONTROL Tag Calculated metric]** de labels voor de geselecteerde berekende metrische waarde of hef de selectie hiervan op. Selecteer **[!UICONTROL Save]** om de labels voor de geselecteerde berekende metriek op te slaan. Zie [ Markering berekende metriek ](cm-tagging.md) voor meer informatie. |
| ![ Aandeel ](/help/assets/icons/ShareLight.svg) **[!UICONTROL Share]** | Deel de geselecteerde berekende metriek. In de **[!UICONTROL Share Calculated metrics]** dialoog, kunt u ![ Onderzoek ](/help/assets/icons/Search.svg) *individuen of groepen van het Onderzoek* of u kunt selecteren **[!UICONTROL Organization]** of **[!UICONTROL Groups]**. Selecteer **[!UICONTROL Save]** om deeldetails voor de geselecteerde berekende metriek op te slaan. Zie [ Aandeel berekende metriek ](cm-sharing.md) voor meer informatie. |
| ![ Schrapping ](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** | Verwijder de geselecteerde berekende metriek. U wordt gevraagd om een bevestiging. |
| ![ geef ](/help/assets/icons/Edit.svg) **[!UICONTROL Rename]** uit | Wijzig de naam van één geselecteerde berekende metrische waarde. Als deze optie is geselecteerd, kunt u de naam van de berekende metrische waarde inline wijzigen. |
| ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL Approve]** | Goedkeuren van de geselecteerde berekende metriek. Zie [ berekende metriek goedkeuren ](cm-approving.md). |
| ![ Exemplaar ](/help/assets/icons/Copy.svg) **[!UICONTROL Copy]** | Kopieer de geselecteerde berekende metriek. Nieuwe berekende metriek worden gemaakt met dezelfde naam en hetzelfde achtervoegsel `(Copy)` |
| ![ FileCSV ](/help/assets/icons/FileCSV.svg) **[!UICONTROL Export to CSV]** | Exporteer de berekende metriek naar een `Calculated  metric List.csv` -bestand. |

### Actieve filterbalk

De filterbalk ➌ de actieve filters weer die van het filterdeelvenster worden toegepast op de lijst met berekende metriek (indien aanwezig). U kunt een filter snel verwijderen gebruikend ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg). Als er meer dan één filter is opgegeven, kunt u alle filters verwijderen met **[!UICONTROL Remove all]** .

### Deelvenster Filter

U kunt de lijst van berekende metrisch filtreren gebruikend de ![ linker paneel➍ van de Filter ](/help/assets/icons/Filter.svg) **[!UICONTROL Filter]**. In het filterdeelvenster worden het type filter en het aantal berekende metingen weergegeven die het specifieke filter respecteren. Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om de vertoning van het filterpaneel van een knevel te voorzien.

Zie [ Filter de lijst van berekende metriek ](cm-filter.md) voor meer informatie.


<!-- OLD CONTENT 

The Calculated metric manager shows you all the filters you own and that have been shared with you. Admin-level users can see all custom metrics in the organization. This overview presents the user interface and the capabilities of the Calculated metric manager.

![Calculated metrics window showing available filters.](assets/calc-metric-manager.png)

## Access the Calculated metrics manager

1. In Customer Journey Analytics, select [!UICONTROL **Components**] > [!UICONTROL **Calculated metrics**].

## Available actions in the Calculated metrics manager

In the Calculated metrics manager, you can:

* [Filter calculated metrics](/help/components/calc-metrics/cm-workflow/cm-filter.md)

* [Mark calculated metrics as favorites](/help/components/calc-metrics/cm-workflow/cm-favorite.md)

* [Approve calculated metrics](/help/components/calc-metrics/cm-workflow/cm-approving.md)

* [Tag calculated metrics](/help/components/calc-metrics/cm-workflow/cm-tagging.md)

* [Share calculated metrics](/help/components/calc-metrics/cm-workflow/cm-sharing.md)

* Export a calculated metric to a CSV file. 

* [Copy calculated metrics](/help/components/calc-metrics/cm-workflow/cm-copy.md)

* Delete calculated metrics

## Configure columns

You can configure the information displayed for each calculated metric in the Calculated metrics manager by configuring the columns that are displayed.

To configure the visible columns in the Calculated metrics manager:

1. In Customer Journey Analytics, select the **[!UICONTROL Components]** tab, then select **[!UICONTROL Calculated metrics]**. 

1. In the Calculated metrics manager, select the **Customize columns** icon ![Customize columns icon](assets/customize-columns-icon.png), then select the columns that you want to be displayed in the Calculated metrics manager.

   The following columns are available:

   | Column title  | Description |
   |---|---|
   | Favorites  | Displays star icons next to each calculated metric, allowing you to mark calculated metrics as favorites. For more information, see [Mark calculated metrics as favorites](/help/components/calc-metrics/cm-workflow/cm-favorite.md). |
   | Title and description | These values are provided in the Calculated metric builder. To edit the title and description, select the title link to open the Calculated metric builder.  |
   | Report suite | Indicates in which report suite the metric was last saved.  |
   | Owner | Indicates who owns the custom metric. As a non-admin, you can see only metrics you own or those that were shared with you.  |
   | Tags | Shows tags that were applied to the metric, either by you or by people who shared the calculated metric with you.  |
   | Shared with | Lists individuals or groups (admin only) or All (admin only) that you shared the calculated metric with. <p>When a calculated metric is being shared, a share icon displays next to the calculated metric name.</p>  |
   | Date modified | Indicates the date when the custom metric was last modified.  |
   | Used in | Shows where calculated metrics are currently being used, and how many times they are being used in each area. <p>For example, if the calculated metric is being used in 40 projects and 2 alerts, then the value of this column shows as [!UICONTROL **42 components**]. <p>Select the value in this column to see the breakdown of where the calculated metrics are being used (for example, [!UICONTROL **Projects (40)**], [!UICONTROL **Mobile Scorecards (2)**]). Furthermore, you can view the list of items where the calculated metrics are being used. For example, to see the list of projects where they are being used, select the [!UICONTROL **Projects (40)**] link.</p><p>Each of the following areas shows the number of instances of calculated metrics being used in that area:</p> <ul><li>[!UICONTROL **Projects**]<p>Contains calculated metrics that were [created in the calculated metric builder](/help/components/apply-create-metrics.md#create-calculated-metrics-for-all-projects) and are available for all projects.</p></li><li>[!UICONTROL **Ad hoc components**]<p>Contains calculated metrics that were [created as quick calculated metrics ](/help/components/apply-create-metrics.md#create-calculated-metrics-for-a-single-project) and are available only within a single project.</p></li><li>[!UICONTROL **Scheduled projects**]</li><li>[!UICONTROL **Mobile Scorecards**]</li><li>[!UICONTROL **Annotations**]</li><li>[!UICONTROL **Report Builder**]<p>Selecting this option downloads a CSV file, with the following columns of data:</p><ul><li>Report Builder Name</li><li>Last accessed</li><li>Last accessed IMS User ID</li><li>Last accessed user name</li></ul><p>When viewing information for Report Builder, usage information is available starting in September 2024.</p></li></ul><p>This information can help you determine whether a component is valuable to users in your organization, where it is used, and if it needs to be deleted or modified.</p><p>Consider the following when viewing this column:</p><ul><li>This information is available only to system administrators.</li><li>The [!UICONTROL **Used in**] column does not display by default. [Configure columns](#configure-columns) to display it.</li><li>If a calculated metric includes another calculated metric in its definition, any use of that calculated metric is not shown in the [!UICONTROL **Used in**] column. If a calculated metric is included in the definition of another type of component (such as a filter), then usage is shown in the [!UICONTROL **Used in**] column.</li><li>This information does not include usage from the API or Data Warehouse.</li><li>If there is no data in this column for a given component but it has a [!UICONTROL **Last used**] date, the component might have been used in an analysis without being saved.</li><li>Usage information is available starting in September 2023.</li></ul><p>You can use the [Data Dictionary](/help/components/data-dictionary/data-dictionary-overview.md) along with this information to help you keep track of and better understand how components are being used in your organization.</p> |
   | Last used | Shows the date when the calculated metric was last used in any of the following component types: <ul><li>Calculated metrics</li><li>Projects</li><li>Scheduled projects</li></ul> <p>This information can help you determine whether a component is valuable to users in your organization, or whether it should be deleted.</p><p>Consider the following when viewing this column:</p><ul><li>This information does not include usage from the API, Report Builder, or Data Warehouse.</li><li>For some components, this column might not contain data if the component was last used prior to September 2023.</li><li>This information is available only to system administrators.</li></ul><p>You can use the [Data Dictionary](/help/components/data-dictionary/data-dictionary-overview.md) along with this information to help you keep track of and better understand how components are being used in your organization. |

   {style="table-layout:auto"}

-->