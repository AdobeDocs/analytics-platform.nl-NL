---
title: Labels en beleid
description: Leer hoe gegevenslabels en beleidsregels die in Adobe Experience Platform zijn gedefinieerd van invloed zijn op gegevensweergaven en rapportage in Customer Journey Analytics.
exl-id: 1de5070f-a91c-4fe6-addb-a89d59a280b7
source-git-commit: e7e3affbc710ec4fc8d6b1d14d17feb8c556befc
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# Labels en beleid

Wanneer u een dataset in Experience Platform creeert, kunt u tot stand brengen [gegevensgebruikslabels](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=en) voor sommige of alle elementen in de gegevensset. U kunt deze labels en beleidsregels weergeven in Customer Journey Analytics.

De volgende labels zijn van bijzonder belang voor Customer Journey Analytics:

* De `C8` label - **[!UICONTROL No measurement]**. Dit label geeft aan dat gegevens niet kunnen worden gebruikt voor analyses op de websites of apps van uw organisatie.

* De `C12` label - **[!UICONTROL No General Data Export]**. Schemavelden met het label this way kunnen niet worden geëxporteerd of gedownload van Customer Journey Analytics (via rapportage, export, API, enzovoort)

>[!NOTE]
>
>De etiketten van het gebruik van gegevens worden niet automatisch verspreid aan stitched datasets. Deze kunnen echter handmatig worden toegevoegd.

De etikettering op zich betekent niet dat deze etiketten van het gegevensgebruik worden afgedwongen. Daar wordt beleid voor gebruikt. U kunt uw beleid maken via de [Beleidsservice-API](https://experienceleague.adobe.com/docs/experience-platform/data-governance/api/overview.html?lang=en) in Experience Platform.

Er worden twee door Adobe gedefinieerde beleidsregels opgehaald in Customer Journey Analytics en dit heeft invloed op rapportage en downloaden/delen:

* **[!UICONTROL Enforce Analytics]** beleid
* **[!UICONTROL Enforce Download]** beleid

## Gegevenslabels weergeven in gegevensweergaven Customer Journey Analytics

De etiketten van gegevens die in Experience Platform werden gecreeerd worden getoond in drie plaatsen in het gebruikersinterface van gegevensmeningen:

| Locatie | Beschrijving |
| --- | --- |
| De knop Info op een schemaveld | Als u op deze knop klikt, wordt aangegeven welke [!UICONTROL Data Usage Labels] momenteel van toepassing op een veld:<p>![](assets/data-label-left.png) |
| Rechterspoor onder [Componentinstellingen](/help/data-views/component-settings/overview.md) | Alle [!UICONTROL Data Usage Labels] worden hier weergegeven:<p>![](assets/data-label-right.png) |
| Gegevenslabels toevoegen als kolom | U kunt [!UICONTROL Data Usage Labels] als een kolom voor de [!UICONTROL Included Components] kolommen in gegevensweergaven. Klik gewoon op het pictogram van de kolomkiezer en selecteer **[!UICONTROL Data Usage Labels]**:<p>![](assets/data-label-column.png) |

{style="table-layout:auto"}

## Filter op labels voor gegevensbeheer in gegevensweergaven

Klik in de editor voor gegevensweergaven op de knop [!UICONTROL filter] pictogram in het linkerspoor en filter de componenten van de gegevensmening door **[!UICONTROL Data Governance]** en type **[!UICONTROL Label]**:

![](assets/filter-labels.png)

Klikken **[!UICONTROL Apply]** om te zien welke componenten etiketten hebben in bijlage aan hen.

## Filter op beleid voor gegevensbeheer in gegevensweergaven

U kunt controleren om te zien of wordt een beleid aangezet dat het gebruik van bepaalde Customer Journey Analytics gegevens meningselementen voor analytics of de uitvoer gebruikt.

Klik nogmaals op de knop [!UICONTROL filter] pictogram in de linkerspoorstaaf en onder **[!UICONTROL Data Governance]**, klikt u op **[!UICONTROL Policies]**:

![](assets/filter-policies.png)

Klikken **[!UICONTROL Apply]** om te zien welk beleid wordt toegelaten.

## Hoe ingeschakeld beleid invloed heeft op gegevensweergaven

Als de **[!UICONTROL Enforce Analytics]** of **[!UICONTROL Enforce Download]** het beleid wordt aangezet, die schemacomponenten die bepaalde gegevensetiketten (zoals C8 of C12) verbonden aan hen hebben kunnen niet aan gegevensmeningen worden toegevoegd.

Deze onderdelen worden grijs weergegeven in de linkerrails [!UICONTROL Schema fields] lijst:

![](assets/component-greyed.png)

U kunt ook geen gegevensweergave opslaan waarin velden zijn geblokkeerd.

>[!MORELIKETHIS]
>[Gevoelige gegevens downloaden](/help/analysis-workspace/curate-share/download-send.md)

>[!MORELIKETHIS]
>[Wat zijn beperkte labels in Report Builder?](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-reportbuilder/restricted-labels.html?lang=en)


