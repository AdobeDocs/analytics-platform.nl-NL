---
title: Sstitching gebruiken
description: Hoe wordt stitching gebruikt
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
role: Admin
exl-id: 9a1689d9-c1b7-42fe-9682-499e49843f76
badgePremium: label="Beta" type="Informative"
source-git-commit: 23b890ec6a3266d1ca0621b09264f1d6a2f82645
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---

# Sstitching gebruiken

U kunt het stitching op één of meerdere gebeurtenisdatasets toelaten u als deel van uw verbinding hebt gevormd. Het Customer Journey Analytics-pakket waarvoor u een licentie hebt verleend, bepaalt het aantal gebeurtenisdatasets dat u kunt inschakelen voor het naaien.

{{release-limited-testing}}

U kunt het stitching als deel van de [ montages van de dataset ](/help/connections/create-connection.md#dataset-settings) voor een gebeurtenisdataset toelaten wanneer u [ een verbinding ](/help/connections/create-connection.md) creeert of wanneer u [ een verbinding ](/help/connections/manage-connections.md#edit-a-connection) uitgeeft.

## Vereisten

Om het stitching op een gebeurtenisdataset binnen de UI van Verbindingen toe te laten:

* Het schema waarop de dataset is gebaseerd zou moeten hebben:

   * meerdere velden die zijn geconfigureerd als identiteit, en waarmee u verschillende waarden kunt selecteren voor een blijvende id en een persoon-id.
   * ten minste één veld dat als primaire identiteit is gemarkeerd met een bijbehorende naamruimte voor het geval u Identiteitskaart en de primaire naamruimte voor permanente id- of persoonsidentiteitskaart wilt gebruiken.

* De gebeurtenisdataset moet [ voor de dienst van de Identiteit ](/help/stitching/faq.md#enable-a-dataset-for-the-identity-service) worden toegelaten voor het geval u de Grafiek van de Identiteit en op grafiek-gebaseerd het stitching wilt gebruiken.


## Preflight-controles

Als u aan de eerste vereisten voldoet, kunt u sommige preflight controles op de gegevens in de gebeurtenisdataset willen uitvoeren alvorens u identiteitsstitching toelaat:

* Zorg ervoor dat de identiteiten behoorlijk in het schema voor de gebeurtenisdataset worden gemerkt. [ zie het overzicht van Identiteitsnaamruimte ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces).
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

      * `{PERSISTENT_ID_FIELD}` is het veld voor de permanente id. Bijvoorbeeld: `identityMap.ecid[0]` .
      * `{DATASET_TABLE_NAME}` is de lijstnaam voor de gebeurtenisdataset.
      * `{FORMAT_STRING}` is de indelingstekenreeks voor het tijdstempelveld. Bijvoorbeeld: `MM/DD/YY HH12:MI AM` .
      * `{START_DATE} ` is de begindatum. Bijvoorbeeld: `2024-01-01 00:00:00` .
      * `{END_DATE}` is de einddatum in standaardformaat. Bijvoorbeeld: `2024-01-08 00:00:00` .


   * Identiteitskaart van de persoon - Vraag 7 dagen van gegevens waar uw gebied van identiteitskaart van uw persoon niet ongeldig is en door een vraag van 7 dagen van gegevens voor alle gebeurtenissen in uw dataset verdeelt. Dit percentage moet boven de 5% liggen.

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
>Als **[!UICONTROL Enable identity stitching]** niet beschikbaar in de interface van Verbindingen is, gebruik de [ verzoekprocedure om het stitching ](/help/stitching/use-stitching.md) op een dataset toe te laten.



U kunt stitching inschakelen in het gedeelte met gebeurtenisgegevens van het dialoogvenster **[!UICONTROL Add datasets]** of **[!UICONTROL Edit dataset]** :

![ Identiteit die opties stitching wanneer u identiteitsstitching ](assets/identity-stitching-ui.png) toelaat

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


   Als u **[!UICONTROL Identity Graph]** voor persoonsidentiteitskaart (om [ op grafiek-gebaseerd het stitching ](/help/stitching/gbs.md) te gebruiken) selecteert, moet u een namespace selecteren.

   >[!NOTE]
   >
   >Zorg ervoor dat u het recht hebt om de identiteitsgrafiek te gebruiken.
   >

   Vóór dat, wordt een **[!UICONTROL Change to identity graph]** dialoog getoond om u te verzekeren u de opstelling van de identiteitsgrafiek voor de dataset [ gebeëindigd hebt alvorens u de identiteitsgrafiek voor het stitching gebruikt. ](/help/stitching/faq.md#enable-a-dataset-for-the-identity-service) Selecteer **[!UICONTROL Continue]** om door te gaan.

   * Selecteer een naamruimte in het vervolgkeuzemenu **[!UICONTROL Namespace]** .


1. Selecteer een terugzoekvenster in het keuzemenu **[!UICONTROL Lookback window]** . De beschikbare opties zijn afhankelijk van het Customer Journey Analytics-pakket waarop u recht hebt.

Zodra u sparen een verbinding die datasets bevat die voor identiteit het stitching worden toegelaten, begint het het stitching proces voor elke dataset wanneer de opname van gegevens voor die dataset begint.

## Beperkingen

Boven de [ op gebied-gebaseerde het stitching beperkingen ](/help/stitching/fbs.md#limitations) en [ op grafiek-gebaseerde het stitching beperkingen ](/help/stitching/gbs.md#limitations), zijn de volgende beperkingen van toepassing wanneer u het stitching in de interface van Verbindingen toelaat:

* U kunt een gebeurtenisdataset slechts eenmaal aansluiten als deel van één enkele verbinding. U kunt niet de zelfde gebeurtenisdataset meer dan eens bepalen en een afzonderlijke stitching configuratie voor elke instantie gebruiken. Als u verschillende stitching configuraties op de zelfde dataset wilt toepassen, gebruik een afzonderlijke verbinding voor elke configuratie.

