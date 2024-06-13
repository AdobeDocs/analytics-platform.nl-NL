---
title: Labels en beleid
description: Leer hoe de gegevensetiketten en het beleid in Adobe Experience Platform worden bepaald gegevensmeningen en rapportering in Customer Journey Analytics beïnvloeden.
exl-id: 1de5070f-a91c-4fe6-addb-a89d59a280b7
feature: Data Views, Data Governance
role: Admin
source-git-commit: 6526ca2b7caaf64acf29d97c859c3e813d003d2d
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Labels en beleid

Wanneer u een dataset in Experience Platform creeert, kunt u creëren [gegevensgebruikslabels](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference) voor sommige of alle elementen in de gegevensset. U kunt deze labels en beleidsregels weergeven in de Customer Journey Analytics.

De volgende labels zijn van bijzonder belang voor de Customer Journey Analytics:

* De `C8` label - **[!UICONTROL No measurement]**. Dit label geeft aan dat gegevens niet kunnen worden gebruikt voor analyses op de websites of apps van uw organisatie.

* De `C12` label - **[!UICONTROL No general data export]**. Schemavelden met het label this way kunnen niet worden geëxporteerd of gedownload van Customer Journey Analytics (via rapportage, export, API, enzovoort)

>[!NOTE]
>
>De etiketten van het gebruik van gegevens worden niet automatisch verspreid aan stitched datasets. Deze kunnen echter handmatig worden toegevoegd.

De etikettering op zich betekent niet dat deze etiketten van het gegevensgebruik worden afgedwongen. Daar wordt beleid voor gebruikt. U kunt uw beleid maken met de [UI EXPERIENCE PLATFORM](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/policies/user-guide) of via de [Policy Service API](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/api/overview) in Experience Platform.

Twee Adobe-bepaalde beleid zijn beschikbaar in Experience Platform dat in Customer Journey Analytics kan opduiken en rapportering en gegevensuitvoer kan beïnvloeden:

* **[!UICONTROL Restrict usage analytics and user based measurement]** beleid, gebruiken van `C8` het etiket, en
* **[!UICONTROL Restrict data export]** beleid, gebruiken van `C12` label.

## Gegevenslabels weergeven in gegevensweergaven van Customers Journey Analytics

De etiketten van gegevens die u of anderen in Experience Platform worden gecreeerd worden getoond in drie plaatsen in de gebruikersinterface van gegevensmeningen:

| Locatie | Beschrijving |
| --- | --- |
| De knop Info op een schemaveld | Als u op deze knop klikt, wordt aangegeven welke [!UICONTROL Data Usage Labels] momenteel van toepassing op een veld:<p>![](assets/data-label-left.png) |
| Rechterspoor onder [Componentinstellingen](/help/data-views/component-settings/overview.md) | Alle [!UICONTROL Data Usage Labels] worden hier weergegeven:<p>![](assets/data-label-right.png) |
| Gegevenslabels toevoegen als kolom | U kunt [!UICONTROL Data Usage Labels] als een kolom voor de [!UICONTROL Included Components] kolommen in gegevensweergaven. Selecteer gewoon het pictogram van de kolomkiezer en selecteer **[!UICONTROL Data Usage Labels]**:<p>![](assets/data-label-column.png) |

{style="table-layout:auto"}

## Filter op labels voor gegevensbeheer in gegevensweergaven

Selecteer in de editor voor gegevensweergaven de optie [!UICONTROL filter] pictogram in het linkerspoor en filter de componenten van de gegevensmening door **[!UICONTROL Data Governance]** en type **[!UICONTROL Label]**:

![](assets/filter-labels.png)

Klikken **[!UICONTROL Apply]** om te zien welke componenten etiketten hebben in bijlage aan hen.

## Filter op beleid voor gegevensbeheer in gegevensweergaven

U kunt controleren of een beleid (bijvoorbeeld een beleid dat u hebt gemaakt, genaamd **[!UICONTROL Enforce Analytics]**) is ingeschakeld. En of dat beleid het gebruik van bepaalde Customer Journey Analytics gegevensweergaveelementen voor analyses of gegevensexport blokkeert.

Selecteer nogmaals de [!UICONTROL filter] pictogram in de linkerspoorstaaf en onder **[!UICONTROL Data Governance]**, selecteert u **[!UICONTROL Policies]**:

![Filter bevat componenten op lijst met de optie Gebruiksanalyses beperken en op gebruiker gebaseerde metingen geselecteerd](assets/filter-policies.png)

Klikken **[!UICONTROL Apply]** om te zien welk beleid wordt toegelaten.

## Hoe ingeschakeld beleid invloed heeft op gegevensweergaven

Als één of meerdere beleid met C8 of C12 etiketten wordt aangezet, kunnen die schemacomponenten die bepaalde toegepaste gegevensetiketten hebben niet aan gegevensmeningen worden toegevoegd.

Deze onderdelen worden grijs weergegeven in de linkerrails [!UICONTROL Schema fields] lijst:

![Grijsvervormde componenten en het beleidsbericht dat beleid aangeeft zijn toegepast op dit veld waardoor het gebruik van de gegevens wordt beperkt](assets/component-greyed.png)

U kunt ook geen gegevensweergave opslaan waarin velden zijn geblokkeerd.

Wees voorzichtig met het toepassen van labels voor toegang en gegevensbeheer (via beleid) op velden of veldgroepen in Experience Platform, waarvoor u al componenten hebt gedefinieerd in uw gegevensweergave. Dit dialoogvenster wordt mogelijk weergegeven.

![Schending](assets/violation.png)

U moet eerst de schending oplossen (bijvoorbeeld de componenten uit de gegevensmening verwijderen).


>[!MORELIKETHIS]
>
>[Gevoelige gegevens downloaden](/help/analysis-workspace/export/download-send.md)

>[!MORELIKETHIS]
>
>[Wat zijn beperkte etiketten in Report Builder?](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-reportbuilder/restricted-labels)


