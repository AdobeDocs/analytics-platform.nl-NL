---
title: Overzicht Customer Journey Analytics-verbindingen
description: Meer informatie over verbindingen in Customer Journey Analytics.
solution: Customer Journey Analytics
feature: Connections
exl-id: 012371d7-aaef-4018-95ee-5c52083e9d8f
role: Admin
source-git-commit: 4f1299595077a1756a6ad0c4f5ef5e0247ab4973
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 1%

---

# Overzicht van verbindingen

Met verbindingen kunnen Customer Journey Analytics-productbeheerders definiëren welke [!DNL &#x200B; Experience Platform] -gegevensbronnen, zoals gebeurtenis, opzoekhandeling, profiel en samenvattingsgegevenssets, worden opgenomen. De verbindingen zijn de stichting van Customer Journey Analytics en bepalen de beschikbaarheid van gegevens (gebieden) die u in a [&#x200B; gegevensmening &#x200B;](/help/data-views/data-views.md) als dimensie of metriek kunt bepalen.

>[!IMPORTANT]
>
>U kunt meerdere [!DNL Experience Platform] datasets combineren in één verbinding.


## Verbindingsworkflow

![&#x200B; het werkschema van Verbindingen &#x200B;](assets/connection-workflow.png)

<!-- Outdated interface 

>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Configuring connections](https://video.tv.adobe.com/v/35111/?quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]

-->

Op een hoog niveau kunt u met de workflow Verbindingen:

| Interface | Beschrijving |
|:---:|---|
| ➊ | [&#x200B; beheer uw verbindingen en algemeen gebruik &#x200B;](manage-connections.md) van Customer Journey Analytics van de manager van Verbindingen. |
| ➋ | [&#x200B; inspecteer de details van een verbinding &#x200B;](manage-connections.md#connection-details), als datasetverslagen die worden opgenomen, overgeslagen, of geschrapt. |
| ➌ | [&#x200B; creeer of geef de configuratie van een verbinding &#x200B;](create-connection.md#create-or-edit-a-connection), als een het rollen gegevensvenster, zandbak om te gebruiken, die datasets deel van de verbinding, en meer uitmaken. |
| ➍ | [&#x200B; voegt datasets aan een verbinding &#x200B;](create-connection.md#add-datasets) toe. Uw verbinding zou minstens één gebeurtenis of summiere dataset moeten hebben maar kan een verscheidenheid van gebeurtenis, profiel, raadpleging, en summiere datasets bevatten. |
| ➎ | [&#x200B; vorm de montages &#x200B;](create-connection.md#dataset-settings) voor datasets die u toevoegt. U kunt bepalen hoe te om verschillende datasets te verbinden die op een gemeenschappelijke op persoon-gebaseerde of [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} op rekening-gebaseerde herkenningsteken worden gebaseerd. |
| ➏ | [&#x200B; geeft de montages voor een bestaande dataset &#x200B;](create-connection.md#edit-a-dataset) uit. U kunt de gegevenssetinstellingen altijd in een later stadium opnieuw bekijken. |



## Toegangsbeheer

De toegang tot het beheer van verbindingen zou tot een kernbeheersgroep moeten worden beperkt. Verbindingsconfiguraties hebben contractuele implicaties met betrekking tot volumetoewijzingen voor gegevens die naar Customer Journey Analytics worden overgebracht.

>[!MORELIKETHIS]
>
>[&#x200B; controle van de Toegang &#x200B;](/help/technotes/access-control.md).

