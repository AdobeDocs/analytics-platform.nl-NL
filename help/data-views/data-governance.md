---
title: Labels en beleid
description: Leer hoe gegevenslabels en beleidsregels die in Adobe Experience Platform zijn gedefinieerd van invloed zijn op gegevensweergaven en -rapporten in Customer Journey Analytics.
exl-id: 1de5070f-a91c-4fe6-addb-a89d59a280b7
feature: Data Views, Data Governance
role: Admin
source-git-commit: 4f1299595077a1756a6ad0c4f5ef5e0247ab4973
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Labels en beleid

Wanneer u een dataset in Experience Platform creeert, kunt u [&#x200B; etiketten van het gegevensgebruik &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference) voor wat of alle elementen in de dataset tot stand brengen. U kunt deze labels en beleidsregels weergeven in Customer Journey Analytics.

De volgende labels zijn van bijzonder belang voor Customer Journey Analytics:

* The `C8` label - **[!UICONTROL No measurement]** . Dit label geeft aan dat gegevens niet kunnen worden gebruikt voor analyses op de websites of apps van uw organisatie.

* The `C12` label - **[!UICONTROL No general data export]** . Schemavelden met het label this way kunnen niet worden geëxporteerd of gedownload van Customer Journey Analytics (via rapportage, export, API, enzovoort)

>[!NOTE]
>
>De etiketten van het gebruik van gegevens worden niet automatisch verspreid aan stitched datasets. Deze kunnen echter handmatig worden toegevoegd.

De etikettering op zich betekent niet dat deze etiketten van het gegevensgebruik worden afgedwongen. Daar wordt beleid voor gebruikt. U kunt uw beleid tot stand brengen gebruikend [&#x200B; Experience Platform UI &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/policies/user-guide) of via de [&#x200B; Dienst API van het Beleid &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/api/overview) in Experience Platform.

Er zijn twee door Adobe gedefinieerde beleidsregels beschikbaar in Experience Platform die van invloed kunnen zijn op Customer Journey Analytics en de rapportage en gegevensexport:

* **[!UICONTROL Restrict usage analytics and user based measurement]** -beleid, met het label `C8` , en
* **[!UICONTROL Restrict data export]** , met het label `C12` .

## Gegevenslabels weergeven in Customer Journey Analytics-gegevensweergaven

De etiketten van gegevens die u of anderen creeerde in Experience Platform worden getoond in drie plaatsen in de gebruikersinterface van gegevensmeningen:

| Locatie | Beschrijving |
| --- | --- |
| De knop Info op een schemaveld | Als u op deze knop klikt, wordt aangegeven welke [!UICONTROL Data Usage Labels] momenteel van toepassing is op een veld:<p>![](assets/data-label-left.png) |
| Rechterspoor onder [&#x200B; montages van de Component &#x200B;](/help/data-views/component-settings/overview.md) | Alle [!UICONTROL Data Usage Labels] worden hier vermeld:<p>![](assets/data-label-right.png) |
| Gegevenslabels toevoegen als kolom | U kunt [!UICONTROL Data Usage Labels] als kolom aan de [!UICONTROL Included Components] kolommen in gegevensmeningen toevoegen. Selecteer gewoon het pictogram van de kolomkiezer en selecteer **[!UICONTROL Data Usage Labels]** :<p>![](assets/data-label-column.png) |

{style="table-layout:auto"}

## Filter op labels voor gegevensbeheer in gegevensweergaven

Selecteer in de editor voor gegevensweergaven het pictogram [!UICONTROL filter] in het linkerspoor en filter de componenten van de gegevensweergaven op **[!UICONTROL Data Governance]** en type **[!UICONTROL Label]** :

![](assets/filter-labels.png)

Klik op **[!UICONTROL Apply]** om te zien aan welke componenten labels zijn gekoppeld.

## Filter op beleid voor gegevensbeheer in gegevensweergaven

U kunt controleren of een beleid (bijvoorbeeld een beleid dat u hebt gemaakt met de naam **[!UICONTROL Enforce Analytics]** ) is ingeschakeld. En of dat beleid het gebruik van bepaalde Customer Journey Analytics-gegevensweergaveelementen voor analyses of gegevensexport blokkeert.

Selecteer nogmaals het pictogram [!UICONTROL filter] in de linkerrails en selecteer **[!UICONTROL Data Governance]** onder **[!UICONTROL Policies]** :

![&#x200B; de Filter omvatte componenten door lijst tonen van Beperkt gebruiksanalyses en gebruiker gebaseerde geselecteerde meting &#x200B;](assets/filter-policies.png)

Klik op **[!UICONTROL Apply]** om te zien welk beleid is ingeschakeld.

## Hoe ingeschakeld beleid invloed heeft op gegevensweergaven

Als één of meerdere beleid met C8 of C12 etiketten wordt aangezet, kunnen die schemacomponenten die bepaalde toegepaste gegevensetiketten hebben niet aan gegevensmeningen worden toegevoegd.

Deze componenten worden grijs weergegeven in de lijst met spoorstaven links [!UICONTROL Schema fields] :

![&#x200B; grijsde uit componenten en het bericht dat van het Beleid beleid op beleid wijzen zijn toegepast op dit gebied dat gebruik van de gegevens beperkt &#x200B;](assets/component-greyed.png)

U kunt ook geen gegevensweergave opslaan waarin velden zijn geblokkeerd.

Wees voorzichtig met het toepassen van labels voor toegang en gegevensbeheer (via beleid) op velden of veldgroepen in Experience Platform, waarvoor al componenten zijn gedefinieerd in de gegevensweergave. Dit dialoogvenster wordt mogelijk weergegeven.

![&#x200B; Schending &#x200B;](assets/violation.png)

U moet eerst de schending oplossen (bijvoorbeeld de componenten uit de gegevensmening verwijderen).


>[!MORELIKETHIS]
>
>[&#x200B; Download gevoelige gegevens &#x200B;](/help/analysis-workspace/export/download-send.md)

>[!MORELIKETHIS]
>
>[&#x200B; wat zijn beperkte etiketten in Report Builder?](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-reportbuilder/restricted-labels)


