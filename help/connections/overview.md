---
title: Overzicht van Customer Journey Analytics-verbindingen
description: Meer informatie over verbindingen in Customer Journey Analytics.
solution: Customer Journey Analytics
feature: Connections
exl-id: 012371d7-aaef-4018-95ee-5c52083e9d8f
role: Admin
source-git-commit: 836c793ae74185728af03636b0ba3e838f46f05d
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Overzicht van verbindingen

Via verbindingen kunnen Customer Journey Analytics-productbeheerders verbindingen tot stand brengen met verschillende [!DNL &#x200B; Experience Platform] -gegevensbronnen, zoals gebeurtenissen, opzoekacties, profielen en samenvattingsgegevenssets. Deze verbindingen laten de integratie van gegevens van een verbinding aan een afgeleide gegevensmening toe. Verbindingen vormen de basis van Customer Journey Analytics en worden gemaakt op basis van [!DNL Experience Platform] brongegevenssets.

>[!IMPORTANT]
>
>U kunt meerdere [!DNL Experience Platform] datasets combineren in één verbinding.


## Verbindingsworkflow

![ het werkschema van Verbindingen ](assets/connection-workflow.png)

<!-- Outdated interface 

>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Configuring connections](https://video.tv.adobe.com/v/35111/?quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]

-->

Op een hoog niveau kunt u met de workflow Verbindingen:

| Interface | Beschrijving |
|:---:|---|
| ➊ | [ beheer uw verbindingen en algemeen gebruik ](manage-connections.md) van Customer Journey Analytics van de manager van Verbindingen. |
| ➋ | [ inspecteer de details van een verbinding ](manage-connections.md#connection-details), als datasetverslagen die worden opgenomen, overgeslagen, of geschrapt. |
| ➌ | [ creeer of geef de configuratie van een verbinding ](create-connection.md#create-or-edit-a-connection), als een het rollen gegevensvenster, zandbak om te gebruiken, die datasets deel van de verbinding, en meer uitmaken. |
| ➍ | [ voegt datasets aan een verbinding ](create-connection.md#add-datasets) toe. Uw verbinding zou minstens één gebeurtenis of summiere dataset moeten hebben maar kan een verscheidenheid van gebeurtenis, profiel, raadpleging, en summiere datasets bevatten. |
| ➎ | [ vorm de montages ](create-connection.md#dataset-settings) voor datasets die u toevoegt. U kunt bepalen hoe te om verschillende datasets te verbinden die op een gemeenschappelijke op persoon-gebaseerde of [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} op rekening-gebaseerde herkenningsteken worden gebaseerd. |
| ➏ | [ geeft de montages voor een bestaande dataset ](create-connection.md#edit-a-dataset) uit. U kunt de gegevenssetinstellingen altijd in een later stadium opnieuw bekijken. |



## Toegangsbeheer

De toegang tot het beheer van verbindingen zou tot een kernbeheersgroep moeten worden beperkt. Verbindingsconfiguraties hebben contractuele implicaties met betrekking tot volumetoewijzingen voor gegevens die naar Customer Journey Analytics worden overgebracht.

>[!MORELIKETHIS]
>
>[ controle van de Toegang ](/help/technotes/access-control.md).

