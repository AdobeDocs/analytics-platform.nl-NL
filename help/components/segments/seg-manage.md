---
title: Segmenten beheren
description: Leer hoe u segmenten beheert in Customer Journey Analytics
exl-id: b8869560-0cf1-4e5d-a03c-dfca85d05e66
feature: Filters, Segments
role: User
source-git-commit: 38be838fccf896a12da3fbadac50e578081312ba
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Segmenten beheren


U kunt ](seg-share.md) delen, [ segment ](seg-filter.md), [ markering ](seg-tag.md), [ goedkeuren ](seg-approve.md), anders noemen, [ exemplaar ](seg-copy.md), schrappen, de segmenten en merken segmenten als [ favoriet ](seg-favorite.md) van een centrale [!UICONTROL Segment] beheersinterface. [ Segmenten beheren:

* Selecteer **[!UICONTROL Components]** in de hoofdinterface en selecteer vervolgens **[!UICONTROL Segments]** .


>[!NOTE]
>
>De snelle segmenten die u binnen een specifiek Workspace-project maakt, worden niet weergegeven in de [!UICONTROL Segment] -manager, tenzij u het segment beschikbaar hebt gemaakt voor al uw projecten.
>

## Segmentbeheer

Segmentbeheer heeft de volgende interface-elementen:

![ interface van het Segment ](assets/filters-manager.png)

### Segmentlijst

In de lijst met segmenten ➊ worden alle segmenten weergegeven die u bezit, de segmenten die binnen het bereik van al uw projecten vallen en de segmenten die met u zijn gedeeld. De lijst heeft de volgende kolommen:

| Kolom | Beschrijving |
| --- | --- | 
| ![ StarOutline ](/help/assets/icons/StarOutline.svg) | Selecteer om ![ Ster ](/help/assets/icons/Star.svg) of niet-gunst ![ StarOutline ](/help/assets/icons/StarOutline.svg) een segment te begunstigen. Zie [ segment van het Teken als favoriet ](/help/components/segments/seg-favorite.md) |
| **[!UICONTROL Title and description]** | Om het segment uit te geven, selecteer de titelverbinding, die de [ bouwer van het Segment ](seg-builder.md) opent. Een gedeeld segment wordt vermeld met ![ Aandeel ](/help/assets/icons/ShareAlt.svg). |
| **[!UICONTROL Data view]** | De gegevensweergaven waarop dit segment van toepassing is. |
| **[!UICONTROL Owner]** | De eigenaar van het segment. Als gebruiker, ziet u slechts de segmenten die u bezit of de annotaties die met u worden gedeeld. |
| **[!UICONTROL Tags]** | De labels voor dit segment. |
| **[!UICONTROL Shared with]** | Hoeveel individuen of groepen u het segment met deelde. Selecteer deze optie om het dialoogvenster **[!UICONTROL Share Component]** te openen. Zie [ de segmenten van het Aandeel ](seg-share.md) voor meer informatie. |
| **[!UICONTROL Date modified]** | De datum en tijd waarop het segment voor het laatst is gewijzigd. |
| **[!UICONTROL Used in]** | Geef aan waar de segmenten momenteel worden gebruikt en hoe vaak deze in elk gebied worden gebruikt. <p>Bijvoorbeeld, als het segment in 40 projecten en 2 alarm wordt gebruikt, dan toont de waarde van deze kolom als [!UICONTROL **42 componenten**].</p> <p>Selecteer de waarde in deze kolom om de uitsplitsing te zien van waar de segmenten (bijvoorbeeld, [!UICONTROL **Projecten (40)**] worden gebruikt, [!UICONTROL **Mobiele Scorecards (2)**]). Bovendien kunt u de lijst met items weergeven waarin de segmenten worden gebruikt. Bijvoorbeeld, zie zo de lijst van projecten waar zij worden gebruikt, selecteer de [!UICONTROL **Projecten (40)**] verbinding.</p><p>Elk van de volgende gebieden toont het aantal instanties van segmenten die in dat gebied worden gebruikt:</p>  <ul><li>[!UICONTROL **Projecten**]<p>Bevat segmenten die [ in de segmentbouwer ](/help/components/segments/seg-builder.md#) werden gecreeerd en voor alle projecten beschikbaar zijn.</p></li><li>[!UICONTROL **Ad hoc componenten**]<p>Bevat segmenten die [ als snelle segmenten ](/help/components/segments/seg-quick.md) werden gecreeerd en beschikbaar slechts binnen één enkel project zijn.</p></li><li>[!UICONTROL **Geplande projecten**]</li><li>[!UICONTROL **Mobiele Scorecards**]</li><li>[!UICONTROL **Annotaties**]</li><li>[!UICONTROL **Berekende standaarden**]</li><li>[!UICONTROL **Report Builder**]<p>Als u deze optie selecteert, wordt een CSV-bestand gedownload met de volgende kolommen gegevens:</p><ul><li>Report Builder-naam</li><li>Laatst geopend</li><li>Laatst geopende IMS-gebruikersnaam</li><li>Laatst geopende gebruikersnaam</li></ul></li></ul><p>Deze informatie helpt u om te bepalen of een component voor gebruikers in uw organisatie waardevol is, waar de component wordt gebruikt, en of de component moet worden geschrapt of worden gewijzigd.</p><p>Houd rekening met het volgende wanneer u deze kolom weergeeft:</p><ul><li>Deze informatie is alleen beschikbaar voor systeembeheerders.</li><li>[!UICONTROL **Gebruikt in**] kolom toont niet door gebrek. Gebruik ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om de vertoning van deze kolom te vormen.</li><li>Deze informatie omvat geen gebruik van de API of de Data Warehouse.</li><li>Als er geen gegevens in deze kolom voor een bepaalde component zijn maar de component a [!UICONTROL **heeft laatst gebruikte**] datum, zou de component in een analyse kunnen worden gebruikt zonder worden bewaard.</li><li>Gebruiksgegevens zijn beschikbaar vanaf september 2023.</li></ul><p>U kunt het [ Woordenboek van Gegevens ](/help/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie gebruiken om u spoor van te houden en beter te begrijpen hoe de componenten in uw organisatie worden gebruikt.</p> |
| **[!UICONTROL Last Used]** | Wanneer het segment voor het laatst is gebruikt. |

Gebruik ![ ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om te specificeren welke kolommen u wilt tonen.

### Actiebalk

U kunt op segmenten actie ondernemen met de actiebalk ➋ . De actiebalk bevat de volgende handelingen:

| Handeling | Beschrijving |
|---|---|
| ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add]** | Voeg een ander segment toe, gebruikend de [ bouwer van het Segment ](seg-builder.md). |
| ![ Onderzoek ](/help/assets/icons/Search.svg) [!UICONTROL *Onderzoek door titel*] | Wanneer er geen segment in de lijst is geselecteerd, zoekt u naar segmenten met dit zoekveld. |
| ![ Etiket ](/help/assets/icons/Label.svg) **[!UICONTROL Tag]** | Tags toewijzen aan de geselecteerde segmenten. Selecteer in het dialoogvenster **[!UICONTROL Tag Segment]** de tags voor de geselecteerde segmenten of hef de selectie hiervan op. Selecteer **[!UICONTROL Save]** om de labels voor de geselecteerde segmenten op te slaan. Zie [ de segmenten van de Markering ](/help/components/segments/seg-tag.md) voor meer informatie. |
| ![ Aandeel ](/help/assets/icons/ShareAlt.svg) **[!UICONTROL Share]** | Deel de geselecteerde segmenten. In de **[!UICONTROL Share Segment]** dialoog, kunt u ![ Onderzoek ](/help/assets/icons/Search.svg) *individuen of groepen van het Onderzoek* of u kunt selecteren **[!UICONTROL Organization]** of **[!UICONTROL Groups]**. Selecteer **[!UICONTROL Save]** om deeldetails voor de geselecteerde segmenten op te slaan. Zie [ de segmenten van het Aandeel ](seg-share.md) voor meer informatie. |
| ![ Schrapping ](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** | Verwijder de geselecteerde segmenten. U wordt gevraagd om een bevestiging. |
| ![ geef ](/help/assets/icons/Edit.svg) **[!UICONTROL Rename]** uit | Wijzig de naam van één geselecteerd segment. Als deze optie is geselecteerd, kunt u de naam van het segment inline wijzigen. |
| ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL Approve]** | Geef de geselecteerde segmenten goed. Zie [ segmenten ](seg-approve.md) voor meer informatie goedkeuren. |
| ![ Exemplaar ](/help/assets/icons/Copy.svg) **[!UICONTROL Copy]** | Kopieer het geselecteerde segment. Nieuwe segmenten worden gemaakt met dezelfde naam en hetzelfde achtervoegsel `(Copy)` . |
| ![ FileCSV ](/help/assets/icons/FileCSV.svg) **[!UICONTROL Export to CSV]** | De segmenten exporteren naar een `Segments List.csv` -bestand. |

### Actieve filterbalk

Op de filterbalk ➌ worden de actieve segmenten weergegeven die van het filterdeelvenster zijn toegepast op de lijst met segmenten (indien aanwezig). U kunt een filter snel verwijderen gebruikend ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg). Als er meerdere filters zijn opgegeven, kunt u alle filters verwijderen met **[!UICONTROL Remove all]** .

### Deelvenster Filter

U kunt de lijst van segmenten filtreren gebruikend ](/help/assets/icons/Filter.svg) **[!UICONTROL Filter]** linkerpaneel van de Filter ![ ➍. In het filterdeelvenster worden het type filter en het aantal segmenten weergegeven dat het specifieke filter toepast. Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om de vertoning van het paneel van de Filter van een knevel te voorzien.

Zie [ de lijst van segmenten ](seg-filter.md) voor meer informatie filtreren.
