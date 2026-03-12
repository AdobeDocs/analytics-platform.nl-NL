---
title: Enable Stitching
description: Identiteitsstitching voor gebeurtenisdatasets in Customer Journey Analytics inschakelen. Leer hoe te om blijvende IDs, persoon IDs te vormen, en vensters in de UI van Verbindingen opnieuw te spelen om gegevens te verbinden.
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
role: Admin
exl-id: 9a1689d9-c1b7-42fe-9682-499e49843f76
source-git-commit: c1acbea7e22e42a2f64f71af054abe2dd6082130
workflow-type: tm+mt
source-wordcount: '1732'
ht-degree: 0%

---

# Sstitching inschakelen

U kunt het stitching op één of meerdere gebeurtenisdatasets toelaten u als deel van uw verbinding hebt gevormd. Het Customer Journey Analytics-pakket waarvoor u een licentie hebt verleend, bepaalt het aantal gebeurtenisdatasets dat u kunt inschakelen voor het naaien.

U laat het stitching als deel van de [&#x200B; montages van de dataset &#x200B;](/help/connections/create-connection.md#dataset-settings) voor een gebeurtenisdataset toe wanneer u [&#x200B; een verbinding &#x200B;](/help/connections/create-connection.md) creeert of wanneer u [&#x200B; een verbinding &#x200B;](/help/connections/manage-connections.md#edit-a-connection) uitgeeft.

## Vereisten

U moet de eerste vereisten voor de het stitching methode controleren en ontmoeten u specificeert: [&#x200B; op gebied-gebaseerd het stitching &#x200B;](fbs.md#prerequisites) of [&#x200B; op grafiek-gebaseerde het stitching &#x200B;](gbs.md#prerequisites).


## Preflight-controles

Als u aan de eerste vereisten voldoet, kunt u sommige preflight controles op de gegevens in de gebeurtenisdataset willen uitvoeren alvorens u identiteitsstitching toelaat:

* Als u XDM schemagebieden voor blijvende identiteitskaart of persoonsidentiteitskaart gaat gebruiken, zorg ervoor dat de identiteiten behoorlijk in het schema voor de gebeurtenisdataset worden duidelijk. [&#x200B; zie het overzicht van Identiteitsnaamruimte &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces).
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
      * Voor op grafiek-gebaseerde het stitching, zorg ervoor dat de identiteitsgrafiek fragmenten bevat die de waarden van identiteitskaart van uw gekozen blijvende naamruimte van identiteitskaart en persoonsidentiteitskaart verbinden U kon een test in werking stellen door naar de [&#x200B; de grafiekkijker van de Identiteit van Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-viewer){target="_blank"} te gaan en de grafiek door één of andere steekproef blijvende waarden van identiteitskaart te vragen. Controleer of deze permanente id-waarden zijn gekoppeld aan de waarden van de persoon-id in de grafiek.
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

U kunt identiteit toelaten stitching wanneer u [&#x200B; &#x200B;](/help/connections/create-connection.md#add-datasets) toevoegt of [&#x200B; &#x200B;](/help/connections/create-connection.md#edit-a-dataset) een gebeurtenisdataset in een op persoon-gebaseerde verbinding uitgeeft. Identiteitskoppelen is niet beschikbaar voor op account gebaseerde verbindingen.

>[!CONTEXTUALHELP]
>id="connection_changeto_identitygraph"
>title="Wijzigen in identiteitsgrafiek"
>abstract="Zorg ervoor dat u de instellingen van de identiteitsgrafiek hebt voltooid voordat u de identiteitsgrafiek voor stitching gebruikt."
>additional-url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/stitching/gbs" text="Op grafiek gebaseerde stitching"

>[!CONTEXTUALHELP]
>id="connection_stitching_personid"
>title="Persoon-id"
>abstract="Selecteer een persoon-id (de unieke id van een persoon) in de beschikbare identiteiten. Als uw licentie op grafieken gebaseerde stitching bevat en u wilt die methode gebruiken, selecteert u **[!UICONTROL Identity Graph]** ."

>[!CONTEXTUALHELP]
>id="connection_stitchingmetrics"
>title="Stitching-metriek"
>abstract="De metriek van het plaatsen worden berekend gebruikend een steekproefreeks gegevens, van om het even welke gegevens die in de laatste 7 dagen worden opgenomen.<br> Deze steekproefreeks gegevens verschilt gewoonlijk van de steekproefgegevens die in de **[!UICONTROL Preview]** lijst worden gebruikt."

>[!CONTEXTUALHELP]
>id="connection_stitchingmetrics_gbs_personidcoverage"
>title="ID-dekking persoon"
>abstract="De dekking van de geselecteerde persoon-id die wordt gebruikt voor identificatie tijdens het naaiproces (live en replay).<br/> voor beste stitching resultaten, zou een (blijvende identiteitskaart, persoonidentiteitskaart) verhouding in de identiteitsgrafiek voor elke blijvende identiteitskaart aanwezig moeten zijn."

>[!CONTEXTUALHELP]
>id="connection_stitchingmetrics_fbs_personidcoverage"
>title="ID-dekking persoon"
>abstract="De dekking van de geselecteerde persoon-id die wordt gebruikt voor identificatie tijdens het naaiproces (live en replay).<br/> voor beste stitching resultaten, zou de persoon identiteitskaart (gebruikersinfo) op minstens één gebeurtenis voor elke blijvende identiteitskaart (apparateninfo) moeten worden verzonden."

>[!CONTEXTUALHELP]
>id="connection_stitchingmetrics_persistentidcoverage"
>title="Blijvende ID-dekking"
>abstract="Deze waarde wordt gebruikt voor identificatie tijdens het stitching proces (live en replay), voor het geval dat een ID-waarde van een persoon niet kan worden gedetecteerd. <br/> Gebeurtenissen zonder blijvende identiteitskaart en geen persoonsidentiteitskaart worden gelaten vallen van de gegevens. Voor de beste stitching resultaten, zou een blijvende identiteitskaart op alle gebeurtenissen moeten aanwezig zijn."


>[!CONTEXTUALHELP]
>id="connection_stitchingmetrics_badids"
>title="Ongeldige id&#39;s"
>abstract="Onjuiste id&#39;s zijn id-waarden die de rapportgegevens ernstig beïnvloeden."
>additional-url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/badids" text="Ongeldige id&#39;s"


### Gegevensinstellingen

Als u stitching wilt inschakelen, gaat u naar het gedeelte **[!UICONTROL Datasets settings]** van de gebeurtenissenset van het dialoogvenster **[!UICONTROL Add datasets]** of **[!UICONTROL Edit dataset]** :

![&#x200B; Identiteit die opties stitching wanneer u identiteitsstitching &#x200B;](assets/identity-stitching-ui.png) toelaat

1. Selecteer **[!UICONTROL Enable identity stitching]**.

   Als u het stitching voor een bewaarde gebeurtenisdataset in of onbruikbaar maakt in de verbinding, toont het **[!UICONTROL Change Person ID]** dialoog de implicaties van een verandering van persoonsidentiteitskaart Selecteer **[!UICONTROL Continue]** om door te gaan.

   Het dialoogvenster **[!UICONTROL Enable identity stitching]** geeft een overzicht van de gevolgen van het stitching van identiteiten. Selecteer **[!UICONTROL Continue]** om door te gaan.

1. Selecteer een permanente id in het vervolgkeuzemenu **[!UICONTROL Persistent ID]** .

   Als u **[!UICONTROL Identity Map]** selecteert voor de permanente id, moet u een naamruimte selecteren. U hebt twee opties:

   * Selecteer **[!UICONTROL Use primary identity namespace]** om de naamruimte voor de primaire identiteit te gebruiken.
   * Selecteer een naamruimte in het vervolgkeuzemenu **[!UICONTROL Namespace]** .

1. Selecteer een persoon-id in het vervolgkeuzemenu **[!UICONTROL Person ID]** .

   Als u **[!UICONTROL Identity Map]** selecteert voor de persoon-id, moet u een naamruimte selecteren. U hebt twee opties:

   * Selecteer **[!UICONTROL Use primary identity namespace]** om de naamruimte voor de primaire identiteit te gebruiken.
   * Selecteer een naamruimte in het vervolgkeuzemenu **[!UICONTROL Namespace]** .


   Als u **[!UICONTROL Identity Graph]** voor persoonsidentiteitskaart (om [&#x200B; op grafiek-gebaseerd het stitching &#x200B;](/help/stitching/gbs.md) te gebruiken) selecteert, moet u een namespace selecteren.

   >[!NOTE]
   >
   >Zorg ervoor dat u het recht hebt om de identiteitsgrafiek te gebruiken.
   >

   Vóór dat, wordt een **[!UICONTROL Change to identity graph]** dialoog getoond om te verzekeren u de opstelling van de identiteitsgrafiek voor de dataset hebt gebeëindigd. Deze opstelling maakt deel uit van de [&#x200B; op grafiek-gebaseerde eerste vereisten &#x200B;](/help/stitching/gbs.md#prerequisites) alvorens u de identiteitsgrafiek voor het stitching kunt gebruiken. Selecteer **[!UICONTROL Continue]** om door te gaan.

   * Selecteer een naamruimte in het vervolgkeuzemenu **[!UICONTROL Namespace]** .

1. Selecteer een opnieuw afspeelvenster in het keuzemenu **[!UICONTROL Replay window]** . De beschikbare opties zijn afhankelijk van het Customer Journey Analytics-pakket waarop u recht hebt.

1. Selecteer **[!UICONTROL Next]** om een voorvertoning weer te geven van de gegevensset met gebeurtenissen die aan stitching is onderworpen.


### Voorvertoning gegevensbestanden

>[!AVAILABILITY]
>
>De verbeterde **[!UICONTROL Dataset preview]** interface (inclusief **[!UICONTROL Stitching metrics]** en **[!UICONTROL Bad IDs]** ) die in deze sectie wordt beschreven, bevindt zich in de testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Als deze optie niet beschikbaar is, wordt de voorvertoning van de gegevensset weergegeven als onderdeel van de interface **[!UICONTROL Dataset settings]** . Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het de versieproces van Customer Journey Analytics, zie [&#x200B; de eigenschapversies van Customer Journey Analytics &#x200B;](/help/release-notes/releases.md).
>

Boven op de standaard **[!UICONTROL Datasets preview]** interface, wanneer [&#x200B; toevoegend &#x200B;](/help/connections/create-connection.md#add-datasets) of [&#x200B; het uitgeven &#x200B;](/help/connections/create-connection.md#edit-a-dataset) datasets in een op persoon-gebaseerde verbinding, zijn twee extra informatiepanelen beschikbaar.

>[!NOTE]
>Voor klanten die Customer Journey Analytics op AWS hebben geïmplementeerd, is deze functionaliteit in afwachting van release.
>

![&#x200B; Identiteit die opties stitching wanneer u identiteitsstitching &#x200B;](assets/identity-stitching-ui-preview.png) toelaat

#### Stitching-metriek



**[!UICONTROL Stitching metrics]** wordt berekend aan de hand van een set voorbeeldgegevens, op basis van gegevens die de afgelopen 7 dagen zijn ingevoerd. Deze voorbeeldset met gegevens verschilt gewoonlijk van de voorbeeldgegevens die in de **[!UICONTROL Preview]** -tabel worden gebruikt. Stitching-meetgegevens bevatten gegevens voor:

* **[!UICONTROL Person ID coverage]**: De dekking van de geselecteerde persoon-id die wordt gebruikt voor identificatie tijdens het stitching-proces (live en replay).
   * Voor de beste op veld gebaseerde stitching resultaten, zou een persoonsidentiteitskaart (gebruikersinformatie) op minstens één gebeurtenis voor elke blijvende identiteitskaart (apparateninfo) moeten worden verzonden.
   * Voor de beste op grafiek-gebaseerde het stitching resultaten, zou een (blijvende identiteitskaart, persoonsidentiteitskaart) verhouding in de identiteitsgrafiek voor elke blijvende identiteitskaart aanwezig moeten zijn.

  De dekking van de persoon-id wordt weergegeven als een percentage en vergeleken met wat wordt aanbevolen bij een stabiele ontwikkeling of bij een productie-instelling. Hoe hoger deze dekkingswaarde, hoe beter de stitching-resultaten worden verkregen met de geselecteerde persoon-id.

* **[!UICONTROL Persistent ID coverage]**: deze waarde wordt gebruikt voor identificatie tijdens het koppelingsproces (live en replay), voor het geval dat een ID-waarde van een persoon niet kan worden gedetecteerd. Gebeurtenissen zonder blijvende id en zonder persoon-id worden uit de gegevens verwijderd. Voor de beste stitching resultaten, zou een blijvende identiteitskaart op alle gebeurtenissen moeten aanwezig zijn.

  Persistente ID-dekking wordt weergegeven als een percentage en vergeleken met wat minimaal wordt aanbevolen bij een stabiele ontwikkeling of bij een productie-instelling.


#### Ongeldige id&#39;s

>[!INFO]
>
>Beschadigde id&#39;s worden ook wel BAVID&#39;s genoemd in de Customer Journey Analytics-interface.
> 

In Customer Journey Analytics is een ongeldige id een id:

* met een specifieke waarde van identiteitskaart die van of een blijvende identiteitskaart of een gebied van identiteitskaart van de persoon in stitching-Toegelaten datasets, **en** voortkomt
* is op meer dan één miljoen (1.000.000) gebeurtenissen in de verbindingsgegevens, binnen een maand.

Wanneer een ID-waarde wordt gemarkeerd als een slechte id, worden toekomstige gebeurtenissen die die id-waarde bevatten, verwijderd uit de verbindingsgegevens en niet weergegeven in de rapportage.

Voorbeelden van Gebruiksgevallen van slechte id&#39;s:

* U hebt aangepaste of plaatsaanduidingswaarden in het veld Personen-id (bijvoorbeeld `undefined` ). Dergelijke waarden kunnen ook [&#x200B; het stitching en het melden van gegevenskwaliteit &#x200B;](/help/stitching/faq.md#undefined-person-id-values) beïnvloeden.
* In een op gebied-gebaseerde het stitching configuratie, als de veelvoudige mensen een apparaat delen en het totale aantal overgangen tussen gebruikers overschrijdt 50.000. In dit scenario stopt het koppelingsproces met het gebruik van de ID-gegevens van de persoon voor dat apparaat en wordt in plaats daarvan alleen permanente ID-informatie gebruikt. Dientengevolge, worden alle datasetgebeurtenissen van dat apparaat verzonden naar verbindingsgegevens met de blijvende identiteit van identiteitskaart, met een hoge kans om een Onjuiste situatie te veroorzaken IDs.


>[!NOTE]
>De waarde **[!UICONTROL Stitching metrics]**, inclusief **[!UICONTROL Bad IDs]** , wordt berekend op basis van een beperkte set gegevens. Om Verkeerde aanwezigheid IDs voor een dataset te identificeren u voor het stitching van plan bent te gebruiken, verwijs naar het [&#x200B; Verkeerde technologie IDs &#x200B;](/help/technotes/badids.md).
>


### Opslaan

Zodra u een verbinding opslaat, wordt het het stitching proces voor het stitching van toegelaten datasets begonnen zodra de opname van gegevens voor deze datasets begint.

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
