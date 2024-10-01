---
title: Filters beheren
description: Leer hoe u filters beheert in Customer Journey Analytics
exl-id: b8869560-0cf1-4e5d-a03c-dfca85d05e66
feature: Filters
role: User
source-git-commit: 97b831d7eee477ee7ef0bf8ae65e6a415d243464
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Filters beheren


U kunt ](filters-share.md) delen, [ filter ](filters-filter.md), [ markering ](filters-tag.md), [ goedkeuren ](filters-approve.md), anders noemen, [ exemplaar ](filters-copy.md), schrappen, de filters van de uitvoer en markeren filters als [ favoriet ](filters-favorite.md) van een centrale [!UICONTROL Filters] beheersinterface. [ Filters beheren:

* Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer vervolgens **[!UICONTROL Filters]** .


>[!NOTE]
>
>De snelle filters die u binnen een specifiek Workspace-project maakt, worden niet weergegeven in de [!UICONTROL Filters] -manager, tenzij u het filter beschikbaar hebt gemaakt voor al uw projecten.
>

## Filterbeheer

De Filtermanager heeft de volgende interface-elementen:

![ de interface van Filters ](assets/filters-manager.png)

### Filterlijst

In de lijst met filters ➊ worden alle filters weergegeven die u hebt, de filters die binnen het bereik van al uw projecten vallen en de filters die met u zijn gedeeld. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
| --- | --- | 
| ![ StarOutline ](/help/assets/icons/StarOutline.svg) | Selecteer om ![ Ster ](/help/assets/icons/Star.svg) of niet-gunst ![ StarOutline ](/help/assets/icons/StarOutline.svg) een filter te begunstigen. Zie [ filter van het Teken als favoriet ](/help/components/filters/filters-favorite.md) |
| **[!UICONTROL Title and description]** | Om de filter uit te geven, selecteer de titelverbinding, die de [ bouwer van Filters ](filter-builder.md) opent. Een gedeeld filter wordt vermeld met ![ Aandeel ](/help/assets/icons/ShareAlt.svg). |
| **[!UICONTROL Data view]** | De gegevensweergaven waarop dit filter van toepassing is. |
| **[!UICONTROL Owner]** | De eigenaar van het filter. Als gebruiker ziet u alleen de filters die u bezit of de annotaties die met u worden gedeeld. |
| **[!UICONTROL Tags]** | De labels voor dit filter. |
| **[!UICONTROL Shared with]** | Hoeveel personen of groepen waarmee u het filter hebt gedeeld. Selecteer deze optie om het dialoogvenster **[!UICONTROL Share Component]** te openen. Zie [ filters van het Aandeel ](filters-share.md) voor meer informatie. |
| **[!UICONTROL Date modified]** | De datum en tijd waarop het filter voor het laatst is gewijzigd. |
| **[!UICONTROL Used in]** | Geef aan waar filters momenteel worden gebruikt en hoeveel keer ze in elk gebied worden gebruikt. <p>Bijvoorbeeld, als de filter in 40 projecten en 2 alarm wordt gebruikt, dan toont de waarde van deze kolom als [!UICONTROL **42 componenten**].</p> <p>Selecteer de waarde in deze kolom om de uitsplitsing te zien van waar de filters (bijvoorbeeld, [!UICONTROL **Projecten (40)**] worden gebruikt, [!UICONTROL **Mobiele Scorecards (2)**]). Bovendien kunt u de lijst met items weergeven waarin de filters worden gebruikt. Bijvoorbeeld, zie zo de lijst van projecten waar zij worden gebruikt, selecteer de [!UICONTROL **Projecten (40)**] verbinding.</p><p>Elk van de volgende gebieden toont het aantal instanties van filters die in dat gebied worden gebruikt:</p>  <ul><li>[!UICONTROL **Projecten**]<p>Bevat filters die [ in de filterbouwer ](/help/components/filters/filter-builder.md#) werden gecreeerd en voor alle projecten beschikbaar zijn.</p></li><li>[!UICONTROL **Ad hoc componenten**]<p>Bevat filters die [ als snelle filters ](/help/components/filters/quick-filters.md) werden gecreeerd en beschikbaar slechts binnen één enkel project zijn.</p></li><li>[!UICONTROL **Geplande projecten**]</li><li>[!UICONTROL **Mobiele Scorecards**]</li><li>[!UICONTROL **Annotaties**]</li><li>[!UICONTROL **Berekende standaarden**]</li><li>[!UICONTROL **Report Builder**]<p>Als u deze optie selecteert, wordt een CSV-bestand gedownload met de volgende kolommen gegevens:</p><ul><li>Naam Report Builder</li><li>Laatst geopend</li><li>Laatst geopende IMS-gebruikersnaam</li><li>Laatst geopende gebruikersnaam</li></ul></li></ul><p>Deze informatie helpt u om te bepalen of een component voor gebruikers in uw organisatie waardevol is, waar de component wordt gebruikt, en of de component moet worden geschrapt of worden gewijzigd.</p><p>Houd rekening met het volgende wanneer u deze kolom weergeeft:</p><ul><li>Deze informatie is alleen beschikbaar voor systeembeheerders.</li><li>[!UICONTROL **Gebruikt in**] kolom toont niet door gebrek. Gebruik ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om de vertoning van deze kolom te vormen.</li><li>Deze informatie omvat geen gebruik van de API of Data Warehouse.</li><li>Als er geen gegevens in deze kolom voor een bepaalde component zijn maar de component a [!UICONTROL **heeft laatst gebruikte**] datum, zou de component in een analyse kunnen worden gebruikt zonder worden bewaard.</li><li>Gebruiksgegevens zijn beschikbaar vanaf september 2023.</li></ul><p>U kunt het [ Woordenboek van Gegevens ](/help/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie gebruiken om u spoor van te houden en beter te begrijpen hoe de componenten in uw organisatie worden gebruikt.</p> |
| **[!UICONTROL Last Used]** | Wanneer het filter voor het laatst is gebruikt. |

{style="table-layout:auto"}

Gebruik ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om te specificeren welke kolommen u wilt tonen.

### Actiebalk

U kunt op filters actie ondernemen met de ➋ van de actiebalk. De actiebalk bevat de volgende handelingen:

| Handeling | Beschrijving |
|---|---|
| ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add]** | Voeg een andere filter toe, gebruikend de [ bouwer van de Filter ](filter-builder.md). |
| ![ Onderzoek ](/help/assets/icons/Search.svg) [!UICONTROL *Onderzoek door titel*] | Wanneer er geen filter in de lijst is geselecteerd, zoekt u naar filters met dit zoekveld. |
| ![ Etiket ](/help/assets/icons/Label.svg) **[!UICONTROL Tag]** | Tags toewijzen aan de geselecteerde filters. Selecteer in het dialoogvenster **[!UICONTROL Tag Filter]** de tags voor de geselecteerde filters of hef de selectie hiervan op. Selecteer **[!UICONTROL Save]** om de labels voor de geselecteerde filters op te slaan. Zie [ de filters van de Markering ](/help/components/filters/filters-tag.md) voor meer informatie. |
| ![ Aandeel ](/help/assets/icons/ShareAlt.svg) **[!UICONTROL Share]** | Deel de geselecteerde filters. In de **[!UICONTROL Share Filter]** dialoog, kunt u ![ Onderzoek ](/help/assets/icons/Search.svg) *individuen of groepen van het Onderzoek* of u kunt selecteren **[!UICONTROL Organization]** of **[!UICONTROL Groups]**. Selecteer **[!UICONTROL Save]** om deeldetails voor de geselecteerde filters op te slaan. Zie [ filters van het Aandeel ](filters-share.md) voor meer informatie. |
| ![ Schrapping ](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** | Verwijder de geselecteerde filters. U wordt gevraagd om een bevestiging. |
| ![ geef ](/help/assets/icons/Edit.svg) **[!UICONTROL Rename]** uit | Wijzig de naam van één geselecteerd filter. Als deze optie is geselecteerd, kunt u de naam van het filter inline wijzigen. |
| ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL Approve]** | De geselecteerde filters goedkeuren. Zie [ filters ](filters-approve.md) voor meer informatie goedkeuren. |
| ![ Exemplaar ](/help/assets/icons/Copy.svg) **[!UICONTROL Copy]** | Kopieer het geselecteerde filter. Nieuwe filters worden gemaakt met dezelfde naam en hetzelfde achtervoegsel `(Copy)` . |
| ![ FileCSV ](/help/assets/icons/FileCSV.svg) **[!UICONTROL Export to CSV]** | De filters exporteren naar een `Filters List.csv` -bestand. |

### Actieve filterbalk

De filterbalk ➌ de actieve filters weer die van het filterdeelvenster op de lijst met filters (indien aanwezig) zijn toegepast. U kunt een filter snel verwijderen gebruikend ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg). Als er meer dan één filter is opgegeven, kunt u alle filters verwijderen met **[!UICONTROL Remove all]** .

### Deelvenster Filter

U kunt de lijst van filters filtreren gebruikend de ![ Linker paneel van de Filter ](/help/assets/icons/Filter.svg) **[!UICONTROL Filter]** ➍. In het filterdeelvenster worden het type filter en het aantal filters weergegeven dat aan het specifieke filter voldoet. Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om de vertoning van het filterpaneel van een knevel te voorzien.

Zie [ de lijst van filters ](filters-filter.md) voor meer informatie filtreren.
