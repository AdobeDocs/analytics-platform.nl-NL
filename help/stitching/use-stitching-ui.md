---
title: Sstitching gebruiken
description: Hoe wordt stitching gebruikt
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
role: Admin
exl-id: 9a1689d9-c1b7-42fe-9682-499e49843f76
badgePremium: label="Beta" type="Informative"
source-git-commit: 0afe57047e2038f1acd9f88a1e7992da9a2819b1
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---

# Sstitching gebruiken

U kunt het stitching op één of meerdere gebeurtenisdatasets toelaten u als deel van uw verbinding hebt gevormd. Het aantal gebeurtenisdatasets dat u voor het stitching kunt toelaten wordt bepaald door het pakket van Customer Journey Analytics u vergunning hebt gegeven.

{{release-limited-testing}}

U kunt het stitching als deel van de [&#x200B; montages van de dataset &#x200B;](/help/connections/create-connection.md#dataset-settings) voor een gebeurtenisdataset toelaten wanneer u [&#x200B; een verbinding &#x200B;](/help/connections/create-connection.md) creeert of wanneer u [&#x200B; een verbinding &#x200B;](/help/connections/manage-connections.md#edit-a-connection) uitgeeft.

## Vereisten

Om het stitching op een gebeurtenisdataset binnen de UI van Verbindingen toe te laten:

* Het schema waarop de dataset is gebaseerd moet hebben bepaald:

   * meerdere velden die zijn geconfigureerd als identiteit, en waarmee u verschillende waarden kunt selecteren voor een blijvende id en een persoon-id.
   * ten minste één veld dat als primaire identiteit is gemarkeerd met een bijbehorende naamruimte voor het geval u Identiteitskaart en de primaire naamruimte voor permanente id- of persoonsidentiteitskaart wilt gebruiken.

* De gebeurtenisdataset moet [&#x200B; voor de dienst van de Identiteit &#x200B;](/help/stitching/faq.md#enable-a-dataset-for-the-identity-service) worden toegelaten voor het geval u de Grafiek van de Identiteit en op grafiek-gebaseerd het stitching wilt gebruiken.


## Preflight-controles

Als u aan de eerste vereisten voldoet, kunt u sommige preflight controles op de gegevens in de gebeurtenisdataset willen uitvoeren alvorens u identiteitsstitching toelaat:

* Zorg ervoor dat de identiteiten correct zijn gemarkeerd in het schema voor de gebeurtenisdataset. [&#x200B; zie het overzicht van Identiteitsnaamruimte &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces).
* Identiteitsdekking voor zowel blijvende identiteitskaart als persoonsidentiteitskaart verifiëren:
   * Persistente ID: query 7 dagen van gegevens waarbij het veld van uw permanente id niet null is en wordt gedeeld door een query van 7 dagen met gegevens voor alle gebeurtenissen in uw dataset. Dit percentage zou boven 95% moeten liggen.

     Voorbeeld van een query die u kunt gebruiken voor verificatie:

     ```sql
     SELECT
       COUNT(*) AS total_events,
       COUNT({PERSISTENT_ID_FIELD}) AS events_with_persistentid,
       ROUND(COUNT({PERSISTENT_ID_FIELD}) / COUNT(*), 2) AS percent_with_persistentid_not_null
     FROM 
       {DATASET_TABLE_NAME}
     WHERE
       TO_TIMESTAMP(timestamp, '{FORMAT_STRING}') >= TIMESTAMP '{START_DATE}'
       AND TO_TIMESTAMP(timestamp, 'FORMAT_STRING') < TIMESTAMP '{END_DATE}';
     ```

     Waarbij:

      * `{PERSISTENT_ID_FIELD}` is het veld voor de persisten-id. Bijvoorbeeld: `identityMap.ecid[0]` .
      * `{DATASET_TABLE_NAME}` is de lijstnaam voor de gebeurtenisdataset.
      * `{FORMAT_STRING}` is de indelingstekenreeks voor het tijdstempelveld. Bijvoorbeeld: `MM/DD/YY HH12:MI AM` .
      * `{START_DATE} ` is de begindatum. Bijvoorbeeld: `2024-01-01 00:00:00` .
      * `{END_DATE}` is de einddatum in standaardformaat. Bijvoorbeeld: `2024-01-08 00:00:00` .


   * Identiteitskaart van de persoon - Vraag 7 dagen van gegevens waar uw gebied van identiteitskaart van uw persoon niet ongeldig is en door een vraag van 7 dagen van gegevens voor alle gebeurtenissen in uw dataset verdeelt. Dit percentage moet boven 5% liggen.

     Voorbeeld van een query die u kunt gebruiken voor verificatie:

     ```sql
     SELECT
       COUNT(*) AS total_events,
       COUNT({PERSON_ID_FIELD}) AS events_with_personid,
       ROUND(COUNT({PERSON_ID_FIELD}) / COUNT(*), 2) AS percent_with_personid_not_null
     FROM 
       {DATASET_TABLE_NAME}
     WHERE
       TO_TIMESTAMP(timestamp, '{FORMAT_STRING}') >= TIMESTAMP '{START_DATE}'
       AND TO_TIMESTAMP(timestamp, 'FORMAT_STRING') < TIMESTAMP '{END_DATE}';
     ```

     Waarbij:

      * `{PERSON_ID_FIELD}` is het veld voor de persoon-id. Bijvoorbeeld: `identityMap.crmId[0]` .
      * `{DATASET_TABLE_NAME}` is de lijstnaam voor de gebeurtenisdataset.
      * `{FORMAT_STRING}` is de indelingstekenreeks voor het tijdstempelveld. Bijvoorbeeld: `MM/DD/YY HH12:MI AM` .
      * `{START_DATE}` is de begindatum. Bijvoorbeeld: `2024-01-01 00:00:00` .
      * `{END_DATE}` is de einddatum in standaardformaat. Bijvoorbeeld: `2024-01-08 00:00:00` .



## Identiteitsstitatie inschakelen

>[!NOTE]
>
>Als **[!UICONTROL Enable identity stitching]** niet beschikbaar in de interface van Verbindingen is, gebruik de [&#x200B; verzoekprocedure om het stitching &#x200B;](/help/stitching/use-stitching.md) op een dataset toe te laten.



U kunt stitching inschakelen in het gedeelte met gebeurtenisgegevens van het dialoogvenster **[!UICONTROL Add datasets]** of **[!UICONTROL Edit dataset]** :

![&#x200B; Identiteit die opties stitching wanneer u identiteitsstitching &#x200B;](assets/identity-stitching-ui.png) toelaat

1. Selecteer **[!UICONTROL Enable identity stitching]**.

   Als u het stitching voor een bestaande gebeurtenisdataset toelaat, **[!UICONTROL Change Person ID]** toont de dialoog de implicaties van een verandering van persoonsidentiteitskaart toe te schrijven aan het gebruik van stitching. Selecteer **[!UICONTROL Continue]** om door te gaan.

   Het dialoogvenster **[!UICONTROL Enable identity stitching]** geeft een overzicht van de gevolgen van het stitching van identiteiten. Selecteer **[!UICONTROL Continue]** om door te gaan.

1. Selecteer een permanente id in het vervolgkeuzemenu **[!UICONTROL Persistent ID]** .

   Als u **[!UICONTROL Identity Map]** selecteert voor de permanente id, moet u een naamruimte selecteren. U hebt twee opties:

   * Schakel **[!UICONTROL Use primary identity namespace]** in om de primaire naamruimte voor identiteit te gebruiken.
   * Selecteer een naamruimte in het vervolgkeuzemenu **[!UICONTROL Namespace]** .

1. Selecteer een persoon-id in het vervolgkeuzemenu **[!UICONTROL Person ID]** .

   Als u **[!UICONTROL Identity Map]** selecteert voor de persoon-id, moet u een naamruimte selecteren. U hebt twee opties:

   * Schakel **[!UICONTROL Use primary identity namespace]** in om de primaire naamruimte voor identiteit te gebruiken.
   * Selecteer een naamruimte in het vervolgkeuzemenu **[!UICONTROL Namespace]** .


   Als u **[!UICONTROL Identity Graph]** voor persoonsidentiteitskaart (om [&#x200B; op grafiek-gebaseerd het stitching &#x200B;](/help/stitching/gbs.md) te gebruiken) selecteert, moet u een namespace selecteren.

   >[!NOTE]
   >
   >U moet het recht hebben om de identiteitsgrafiek te gebruiken.
   >

   Vóór dat, wordt een **[!UICONTROL Change to identity graph]** dialoog getoond om u te verzekeren u de opstelling van de identiteitsgrafiek voor de dataset [&#x200B; gebeëindigd hebt alvorens u de identiteitsgrafiek voor het stitching gebruikt. &#x200B;](/help/stitching/faq.md#enable-a-dataset-for-the-identity-service) Selecteer **[!UICONTROL Continue]** om door te gaan.

   * Selecteer een naamruimte in het vervolgkeuzemenu **[!UICONTROL Namespace]** .


1. Selecteer een terugzoekvenster in het keuzemenu **[!UICONTROL Lookback window]** . Welke opties beschikbaar zijn, is afhankelijk van het Customer Journey Analytics-pakket waarop u recht hebt.

Zodra u sparen een verbinding die datasets bevat die voor identiteit het stitching worden toegelaten, begint het het stitching proces voor elke dataset wanneer de opname van gegevens voor die dataset begint.

## Beperkingen

Boven de [&#x200B; op gebied-gebaseerde het plaatsen beperkingen &#x200B;](/help/stitching/fbs.md#limitations) en [&#x200B; op grafiek-gebaseerde stitchin beperkingen &#x200B;](/help/stitching/gbs.md#limitations), zijn de volgende beperkingen van toepassing wanneer u het stitching in de interface van Verbindingen toelaat:

* U kunt een gebeurtenisdataset slechts eenmaal aansluiten als deel van één enkele verbinding. U kunt niet de zelfde gebeurtenisdataset meer dan één bepalen en een afzonderlijke stitching configuratie voor elke instantie gebruiken. Als u verschillende stitching configuraties op de zelfde dataset wilt toepassen, gebruik een afzonderlijke verbinding voor elke configuratie.

