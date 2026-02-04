---
title: Enable Stitching
description: Leer hoe u stitching inschakelt in de gebruikersinterface voor verbindingen.
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
role: Admin
exl-id: 9a1689d9-c1b7-42fe-9682-499e49843f76
source-git-commit: cbb18e9d0990d5df64995c2dabe8362c7c37bb45
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---

# Sstitching inschakelen

U kunt het stitching op één of meerdere gebeurtenisdatasets toelaten u als deel van uw verbinding hebt gevormd. Het Customer Journey Analytics-pakket waarvoor u een licentie hebt verleend, bepaalt het aantal gebeurtenisdatasets dat u kunt inschakelen voor het naaien.

U laat het stitching als deel van de [&#x200B; montages van de dataset &#x200B;](/help/connections/create-connection.md#dataset-settings) voor een gebeurtenisdataset toe wanneer u [&#x200B; een verbinding &#x200B;](/help/connections/create-connection.md) creeert of wanneer u [&#x200B; een verbinding &#x200B;](/help/connections/manage-connections.md#edit-a-connection) uitgeeft.

## Vereisten

U moet de eerste vereisten voor de het stitching methode controleren en ontmoeten u specificeert: [&#x200B; op gebied-gebaseerd het stitching &#x200B;](fbs.md#prerequisites) of [&#x200B; op grafiek-gebaseerde het stitching &#x200B;](gbs.md#prerequisites).


## Preflight-controles

Als u aan de eerste vereisten voldoet, kunt u sommige preflight controles op de gegevens in de gebeurtenisdataset willen uitvoeren alvorens u identiteitsstitching toelaat:

* Als u XDM schemagebieden voor blijvende identiteitskaart of persoonsidentiteitskaart gaat gebruiken, zorg ervoor dat de identiteiten behoorlijk in het schema voor de gebeurtenisdataset worden duidelijk. [&#x200B; zie het overzicht van Identiteitsnaamruimte &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/identity/features/namespaces).
* Identiteitsdekking voor zowel blijvende identiteitskaart als persoonsidentiteitskaart verifiëren:

   * **Blijvende identiteitskaart**

     Vraag 7 dagen van gegevens waar uw blijvend gebied van identiteitskaart niet ongeldig is en door een vraag van 7 dagen van gegevens voor alle gebeurtenissen in uw dataset verdeelt. Dit percentage zou boven 95% moeten liggen.

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


   * **identiteitskaart van de Persoon**
      * Voor op grafiek-gebaseerde het stitching, zorg ervoor dat de identiteitsgrafiek fragmenten bevat die de waarden van identiteitskaart van uw gekozen blijvende naamruimte van identiteitskaart en persoonsidentiteitskaart verbinden U kon een test in werking stellen door naar de [&#x200B; de grafiekkijker van de Identiteit van Experience Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/identity/features/identity-graph-viewer){target="_blank"} te gaan en de grafiek door sommige waarden van test blijvende identiteitskaart te vragen. Controleer of deze permanente id-waarden zijn gekoppeld aan de waarden van de persoon-id in de grafiek.
      * Voor op gebied-gebaseerde het stitching, vraag 7 dagen van gegevens waar uw persoonidentiteitskaart- gebied niet ongeldig is en door een vraag van 7 dagen van gegevens voor alle gebeurtenissen in uw dataset verdeelt. Dit percentage zou idealiter boven de 5% moeten liggen.

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



## Identiteitsstitatie inschakelen {#enable-identity-stitching}

>[!CONTEXTUALHELP]
>id="connection_changeto_identitygraph"
>title="Wijzigen in identiteitsgrafiek"
>abstract="Zorg ervoor dat u de instellingen van de identiteitsgrafiek hebt voltooid voordat u de identiteitsgrafiek voor stitching gebruikt."
>additional-url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/stitching/gbs" text="Op grafiek gebaseerde stitching"

U kunt stitching inschakelen in het gedeelte met gebeurtenisgegevens van het dialoogvenster **[!UICONTROL Add datasets]** of **[!UICONTROL Edit dataset]** :

![&#x200B; Identiteit die opties stitching wanneer u identiteitsstitching &#x200B;](assets/identity-stitching-ui.png) toelaat

1. Selecteer **[!UICONTROL Enable identity stitching]**.

   Als u het stitching voor een bewaarde gebeurtenisdataset in of onbruikbaar maakt in de verbinding, toont het **[!UICONTROL Change Person ID]** dialoog de implicaties van een verandering van persoonsidentiteitskaart Selecteer **[!UICONTROL Continue]** om door te gaan.

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
   >Zorg ervoor dat u het recht hebt om de identiteitsgrafiek te gebruiken.
   >

   Vóór dat, wordt een **[!UICONTROL Change to identity graph]** dialoog getoond om u de opstelling van de identiteitsgrafiek voor de dataset als deel van de [&#x200B; op grafiek-gebaseerde eerste vereisten &#x200B;](/help/stitching/gbs.md#prerequisites) te verzekeren alvorens u de identiteitsgrafiek voor het stitching gebruikt. Selecteer **[!UICONTROL Continue]** om door te gaan.

   * Selecteer een naamruimte in het vervolgkeuzemenu **[!UICONTROL Namespace]** .


1. Selecteer een opnieuw afspeelvenster in het keuzemenu **[!UICONTROL Replay window]** . De beschikbare opties zijn afhankelijk van het Customer Journey Analytics-pakket waarop u recht hebt.

Zodra u een verbinding opslaat, het stitching proces voor datasets die voor het stitching kicks worden toegelaten wanneer de opname van gegevens voor deze datasets begint.

>[!CAUTION]
>
>Voor datasets die voor het stitching in de interface van Verbindingen worden toegelaten, wordt de backfill status onmiddellijk en verkeerd gemeld als ![&#x200B; Status groene &#x200B;](/help/assets/icons/StatusGreen.svg) **[!UICONTROL _x _voltooide backfills]**&#x200B;voor het aantal voltooide backfills. Gebruik andere manieren om te verifiëren of de gegevens van de gestikte dataset achtergevulde gegevens zijn.
>


## Beperkingen

Boven de [&#x200B; op gebied-gebaseerde het stitching beperkingen &#x200B;](/help/stitching/fbs.md#limitations) en [&#x200B; op grafiek-gebaseerde het stitching beperkingen &#x200B;](/help/stitching/gbs.md#limitations), zijn de volgende beperkingen van toepassing wanneer u het stitching in de interface van Verbindingen toelaat:

* U kunt een gebeurtenisdataset slechts eenmaal aansluiten als deel van één enkele verbinding. U kunt niet de zelfde gebeurtenisdataset meer dan eens bepalen en een afzonderlijke stitching configuratie voor elke instantie gebruiken. Als u verschillende stitching configuraties op de zelfde dataset wilt toepassen, gebruik een afzonderlijke verbinding voor elke configuratie.


## Migratie

Het plaatsen die in de interface van Verbindingen wordt toegelaten kan coëxisteren zonder enige kwesties met verzoek gebaseerd stitching.

Bijvoorbeeld, hebt u Web-based gestitched datasets in het gegevensmeer als resultaat van vroegere of huidige stitching verzoeken. U kunt verankerde gegevens van een vraag-centrum dataset toevoegen gebruikend de interface van Verbindingen om die gegevens met de web-based gegevens te combineren.

Uiteindelijk, zal Adobe uw verzoek gebaseerde verbonden datasets aan het nieuwe stitching in connectiviteitservaring migreren.
