---
title: Sstitching gebruiken
description: Hoe wordt stitching gebruikt
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
role: Admin
hide: true
hidefromtoc: true
exl-id: 9a1689d9-c1b7-42fe-9682-499e49843f76
source-git-commit: 4bca14492374939cd1ea6508c774720db61a6283
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Sstitching gebruiken

U kunt het stitching op één of meerdere gebeurtenisdatasets toelaten u als deel van uw verbinding hebt gevormd. Het aantal gebeurtenisdatasets dat u voor het stitching kunt toelaten wordt bepaald door het pakket van Customer Journey Analytics u vergunning hebt gegeven.

U kunt het stitching als deel van de [ montages van de dataset ](/help/connections/create-connection.md#dataset-settings) voor een gebeurtenisdataset toelaten wanneer u [ een verbinding ](/help/connections/create-connection.md) creeert of wanneer u [ een verbinding ](/help/connections/manage-connections.md#edit-a-connection) uitgeeft.

U kunt stitching inschakelen in het gedeelte met gebeurtenisgegevens van het dialoogvenster **[!UICONTROL Add datasets]** of **[!UICONTROL Edit dataset]** :

![ Identiteit die opties stitching wanneer u identiteitsstitching ](assets/identity-stitching-ui.png) toelaat

1. Selecteer **[!UICONTROL Enable identity stitching]** .

   Als u het stitching voor een bestaande gebeurtenisdataset toelaat, **[!UICONTROL Change Person ID]** toont de dialoog de implicaties van een verandering van identiteitskaart van de Persoon toe te schrijven aan het gebruik van stitching. Selecteer **[!UICONTROL Continue]** om door te gaan.

   Het dialoogvenster **[!UICONTROL Enable identity stitching]** geeft een overzicht van de gevolgen van het stitching van identiteiten. Selecteer **[!UICONTROL Continue]** om door te gaan.

1. Selecteer een permanente id in het vervolgkeuzemenu **[!UICONTROL Persistent ID]** .

   Als u **[!UICONTROL Identity Map]** selecteert voor de permanente id, moet u een naamruimte selecteren. U hebt twee opties:

   * Schakel **[!UICONTROL Use primary identity namespace]** in om de primaire naamruimte voor identiteit te gebruiken.
   * Selecteer een naamruimte in het vervolgkeuzemenu **[!UICONTROL Namespace]** .

1. Selecteer een persoon-id in het vervolgkeuzemenu **[!UICONTROL Person ID]** .

   Als u **[!UICONTROL Identity Map]** selecteert voor de persoon-id, moet u een naamruimte selecteren. U hebt twee opties:

   * Schakel **[!UICONTROL Use primary identity namespace]** in om de primaire naamruimte voor identiteit te gebruiken.
   * Selecteer een naamruimte in het vervolgkeuzemenu **[!UICONTROL Namespace]** .

   Als u **[!UICONTROL Identity Graph]** selecteert voor de persoon-id, moet u een naamruimte selecteren. Hiervóór wordt een dialoogvenster **[!UICONTROL Change to identity graph]** weergegeven om te controleren of u de identiteitsgrafiek hebt ingesteld voordat u de identiteitsgrafiek voor stitching gebruikt. Selecteer **[!UICONTROL Continue]** om door te gaan.

   * Selecteer een naamruimte in het vervolgkeuzemenu **[!UICONTROL Namespace]** .


1. Selecteer een terugzoekvenster in het keuzemenu **[!UICONTROL Lookback window]** . De opties zijn **[!UICONTROL 1 day]** , **[!UICONTROL 7 days]** , **[!UICONTROL 14 days]** of **[!UICONTROL 30 days]** .
