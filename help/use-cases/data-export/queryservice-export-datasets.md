---
title: Experience Platform Query Service (Data Distiller) en exportgegevenssets
description: Beschrijft hoe te om de Dienst van de Vraag (Gegevens Distiller) en de uitvoer van Dataset te gebruiken om gegevens uit te voeren.
solution: Customer Journey Analytics
feature: Use Cases
role: Admin
exl-id: 14a90758-91eb-4610-8802-1edfdb8b9689
source-git-commit: 20ead546897ad517840f95a5ec4dcd7f830afe8c
workflow-type: tm+mt
source-wordcount: '2638'
ht-degree: 0%

---

# Query-service (Data Distiller) en exportgegevenssets

Dit artikel schetst hoe de combinatie van de Dienst van de Vraag van Experience Platform (Gegevens Distiller) en de uitvoer van Dataset kan worden gebruikt om de volgende [&#x200B; gevallen van het de uitvoergebruik van gegevens uit te voeren &#x200B;](overview.md):

- Gegevensvalidatie
- Data Lake, Data Warehouse of BI tools
- Gereedheid voor kunstmatig slim en machinaal leren.


Adobe Analytics kan deze gebruiksgevallen uitvoeren gebruikend zijn [&#x200B; functionaliteit 0&rbrace; van de Diefstal van Gegevens &lbrace;. &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/export/analytics-data-feed/data-feed-overview) Gegevensfeeds zijn een krachtige manier om onbewerkte gegevens uit Adobe Analytics te halen. In dit artikel wordt beschreven hoe u vergelijkbare onbewerkte gegevens uit Experience Platform kunt ophalen, zodat u de hierboven vermelde gebruiksgevallen kunt implementeren. Indien van toepassing worden de in dit artikel beschreven functies vergeleken met Adobe Analytics Data Feeds om verschillen in gegevens en processen te verduidelijken.

## Inleiding

Het uitvoeren van gegevens gebruikend de Dienst van de Vraag (Gegevens Distiller) en de uitvoer van Dataset bestaat uit:

- het bepalen van a **geplande vraag** die de gegevens voor uw gegevensvoer als 2&rbrace; de outputdataset van de outputdataset ![&#x200B; produceert, gebruikend &#x200B;](../assets/output-dataset.svg) Dienst van de Vraag **.**
- het bepalen van de uitvoer van de a **geplande dataset** die de outputdataset naar een bestemming van de wolkenopslag uitvoert, gebruikend **de uitvoer van de Dataset**.

![&#x200B; voer van Gegevens &#x200B;](../assets/queryservice-export-datasets.svg)


## Vereisten

Zorg ervoor dat u aan alle volgende vereisten voldoet voordat u de functionaliteit gebruikt die in dit gebruiksgeval wordt beschreven:

- Een werkende implementatie die gegevens verzamelt in het gegevensmeer van Experience Platform.
- Toegang tot de gegevensinvoegtoepassing Distiller om te controleren of u batch-query&#39;s mag uitvoeren. Zie [&#x200B; het verpakken van de Dienst van de Vraag &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/packaging) voor meer informatie.
- Toegang tot de functionaliteit voor exportgegevenssets die beschikbaar is wanneer u het Real-Time CDP Prime- of Ultimate-pakket, Adobe Journey Optimizer of Customer Journey Analytics hebt aangeschaft. Zie [&#x200B; datasets van de Uitvoer aan de bestemmingen van de wolkenopslag &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets) voor meer informatie.
- Een of meer geconfigureerde doelen (bijvoorbeeld Amazon S3, Google Cloud Storage) waarnaar u de onbewerkte gegevens van uw gegevensfeed kunt exporteren.


## Query-service

De Dienst van de Vraag van Experience Platform staat u toe om het even welke dataset in het de gegevensmeer van Experience Platform te vragen en zich aan te sluiten alsof het een gegevensbestandlijst is. Vervolgens kunt u de resultaten vastleggen als een nieuwe gegevensset voor verder gebruik in rapportage of voor export.

U kunt het gebruikersinterface van de Dienst van de Vraag [&#x200B; gebruiken, a &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/overview) cliënt die door het protocol PostgresQL [&#x200B; wordt aangesloten, of &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/clients/overview) RESTful APIs [&#x200B; om vragen tot stand te brengen en te plannen die de gegevens voor uw gegevensvoer verzamelen.](https://experienceleague.adobe.com/en/docs/experience-platform/query/api/getting-started)

### Query maken

U kunt alle functionaliteit van standaardANSI SQL voor UITGEZOCHTE verklaringen en andere beperkte bevelen gebruiken om vragen tot stand te brengen en uit te voeren die de gegevens voor uw gegevensvoer produceren. Zie [&#x200B; SQL syntaxis &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/syntax) voor meer informatie. Buiten deze SQL-syntaxis biedt Adobe ondersteuning voor:

- prebuilt [&#x200B; Adobe-defined functies (ADF) &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/adobe-defined-functions) die helpen gemeenschappelijke zaken-gerelateerde taken op gebeurtenisgegevens uitvoeren die in het de gegevensmeer van Experience Platform worden opgeslagen, met inbegrip van functies voor [&#x200B; Sessionisatie &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/components/virtual-report-suites/vrs-mobile-visit-processing) en [&#x200B; Attributie &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/attribution/overview),
- verscheidene ingebouwde [&#x200B; functies van de Vonk SQL &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/spark-sql-functions),
- [&#x200B; meta-gegevens PostgreSQL bevelen &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/metadata),
- [&#x200B; voorbereide verklaringen &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/prepared-statements).

#### Gegevensvoederkolommen

De XDM gebieden die u in uw vraag kunt gebruiken hangen van de schemadefinitie af waarop uw datasets worden gebaseerd. Zorg ervoor u het schema onderaan de dataset begrijpt. Zie voor meer informatie de [&#x200B; gids UI van Datasets &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide).

Om u te helpen om de afbeelding tussen de kolommen van het Gegevensvoer en de gebieden te bepalen XDM, zie [&#x200B; het gebiedstoewijzing van Analytics &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics). Zie ook het [&#x200B; overzicht van Schema&#39;s UI &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/overview#defining-xdm-fields) voor meer informatie over hoe te om middelen XDM, met inbegrip van schema&#39;s, klassen, gebiedsgroepen, en gegevenstypes te beheren.

Bijvoorbeeld, voor het geval u *paginanaam* als deel van uw gegevensvoer wilt gebruiken:

- In de gebruikersinterface van Adobe Analytics Data Feed selecteert u **[!UICONTROL pagename]** als kolom die u wilt toevoegen aan de definitie van de gegevensfeed.
- In de Dienst van de Vraag, omvat u `web.webPageDetails.name` van de `sample_event_dataset_for_website_global_v1_1` dataset (die op het **Schema van de Gebeurtenis van de Steekproef voor Website (Globale v1.1)** ervaringsgebeurtenisschema) in uw vraag wordt gebaseerd. Zie de [&#x200B; groep van het het schemagebied van Details van het Web &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/web-details) voor meer informatie.


#### Identiteiten

In Experience Platform zijn verschillende identiteiten beschikbaar. Zorg er bij het maken van query&#39;s voor dat u de id&#39;s correct opvraagt.


Vaak vindt u identiteiten in een afzonderlijke veldgroep. In een implementatie kan ECID (`ecid`) worden gedefinieerd als onderdeel van een veldgroep met een `core` -object, dat zelf deel uitmaakt van een `identification` -object (bijvoorbeeld: `_sampleorg.identification.core.ecid`). De ECIDs zou verschillend in uw schema&#39;s kunnen worden georganiseerd.

U kunt `identityMap` ook gebruiken om te zoeken naar identiteiten. `identityMap` is van type `Map` en gebruikt a [&#x200B; genestelde gegevensstructuur &#x200B;](#nested-data-structure).

Zie [&#x200B; identiteitsgebieden in UI &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity) voor meer informatie over hoe te om identiteitsgebieden in Experience Platform te bepalen.

Verwijs naar [&#x200B; Primaire herkenningstekens in de gegevens van Analytics &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/analytics#primary-identifiers-in-analytics-data) voor een begrip hoe de identiteiten van Adobe Analytics aan de identiteiten van Experience Platform wanneer het gebruiken van de Analytics bronschakelaar in kaart worden gebracht. Deze toewijzing kan als richtlijn voor vestiging uw identiteiten dienen, zelfs wanneer het gebruiken van niet de analytische bronschakelaar.


#### Gegevens en identificatie op bedrijfsniveau

Op basis van de implementatie worden gegevens op raakniveau die traditioneel in Adobe Analytics worden verzameld, nu opgeslagen als tijdstempelgegevens voor gebeurtenissen in Experience Platform. De volgende lijst wordt gehaald uit [&#x200B; het gebiedstoewijzing van Analytics &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics#generated-mapping-fields) en toont voorbeelden hoe te om niveau-specifieke kolommen van de Invoer van Gegevens van Adobe Analytics met overeenkomstige XDM gebieden in uw vragen in kaart te brengen. De tabel bevat ook voorbeelden van hoe treffers, bezoeken en bezoekers worden geïdentificeerd met behulp van XDM-velden.

| Kolom Gegevensfeed | XDM-veld | Type | Beschrijving |
|---|---|---|---|
| `hitid_high` + `hitid_low` | `_id` | string | Een unieke id om een treffer te identificeren. |
| `hitid_low` | `_id` | string | Wordt gebruikt met `hitid_high` om een treffer uniek te identificeren. |
| `hitid_high` | `_id` | string | Wordt gebruikt met `hitid_high` om een treffer uniek te identificeren. |
| `hit_time_gmt` | `receivedTimestamp` | string | De tijdstempel van de hit, gebaseerd op UNIX®-tijd. |
| `cust_hit_time_gmt` | `timestamp` | string | Dit tijdstempel wordt alleen gebruikt in gegevenssets die geschikt zijn voor tijdstempels. Deze tijdstempel wordt samen met de hit verzonden, op basis van UNIX®-tijd. |
| `visid_high` + `visid_low` | `identityMap` | object | Een unieke id voor een bezoek. |
| `visid_high` + `visid_low` | `endUserIDs._experience.aaid.id` | string | Een unieke id voor een bezoek. |
| `visid_high` | `endUserIDs._experience.aaid.primary` | boolean | Wordt samen met `visid_low` gebruikt om een bezoek op unieke wijze te identificeren. |
| `visid_high` | `endUserIDs._experience.aaid.namespace.code` | string | Wordt samen met `visid_low` gebruikt om een bezoek op unieke wijze te identificeren. |
| `visid_low` | `identityMap` | object | Wordt samen met `visid_high` gebruikt om een bezoek op unieke wijze te identificeren. |
| `cust_visid` | `identityMap` | object | De bezoeker-id van de klant. |
| `cust_visid` | `endUserIDs._experience.aacustomid.id` | object | De bezoeker-id van de klant. |
| `cust_visid` | `endUserIDs._experience.aacustomid.primary` | boolean | De naamruimtecode van de bezoeker-id van de klant. |
| `cust_visid` | `endUserIDs._experience.aacustomid.namespace.code` | string | Wordt gebruikt met `visid_low` om de bezoeker-id van de klant op unieke wijze te identificeren. |
| `geo\_*` | `placeContext.geo.* ` | tekenreeks, getal | Geolocatiegegevens, zoals land, regio, stad en andere |
| `event_list` | `commerce.purchases`, `commerce.productViews`, `commerce.productListOpens`, `commerce.checkouts`, `commerce.productListAdds`, `commerce.productListRemovals`, `commerce.productListViews`, `_experience.analytics.event101to200.*`, ..., `_experience.analytics.event901_1000.*` | string | Standaard handel en douanegebeurtenissen teweeggebracht op de slag. |
| `page_event` | `web.webInteraction.type` | string | Het type hit dat wordt verzonden in de afbeeldingsaanvraag (klik op Standaard, Koppeling downloaden, Koppeling afsluiten of Aangepaste koppeling). |
| `page_event` | `web.webInteraction.linkClicks.value` | getal | Het type hit dat wordt verzonden in de afbeeldingsaanvraag (klik op Standaard, Koppeling downloaden, Koppeling afsluiten of Aangepaste koppeling). |
| `page_event_var_1` | `web.webInteraction.URL` | string | Een variabele die alleen wordt gebruikt in aanvragen voor het bijhouden van koppelingen. Deze variabele bevat de URL van de downloadkoppeling, de afsluitkoppeling of de aangepaste koppeling waarop is geklikt. |
| `page_event_var_2` | `web.webInteraction.name` | string | Een variabele die alleen wordt gebruikt in aanvragen voor het bijhouden van koppelingen. Hier wordt de aangepaste naam van de koppeling weergegeven, als deze is opgegeven. |
| `paid_search` | `search.isPaid` | boolean | Een vlag die wordt geplaatst als de treffer betaalde onderzoeksopsporing aanpast. |
| `ref_type` | `web.webReferrertype` | string | Een numerieke id die het verwijzingstype voor de treffer vertegenwoordigt. |

#### Kolommen na

Adobe Analytics Data Feeds gebruikt het concept kolommen met een voorvoegsel `post_` . Dit zijn kolommen met gegevens na verwerking. Zie [&#x200B; Veelgestelde Veelgestelde vragen van het voer van Gegevens &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/export/analytics-data-feed/df-faq#post) voor meer informatie.

Gegevens die via de Experience Platform Edge Network (Web SDK, Mobile SDK, Server API) in gegevenssets zijn verzameld, hebben geen concept van `post_` -velden. Dientengevolge, `post_` prefixed en *niet* - `post_` vooraf vastgestelde de kolommen van de gegevensvoer aan de zelfde gebieden XDM in kaart brengen. Zowel `page_url` als `post_page_url` gegevensfeed-kolommen worden bijvoorbeeld toegewezen aan hetzelfde `web.webPageDetails.URL` XDM-veld.

Zie [&#x200B; gegevensverwerking over Adobe Analytics en Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/data-processing-comparisons) voor een overzicht van het verschil in verwerking van gegevens vergelijken.

Het kolomtype van de prefix `post_` van gegevens, wanneer verzameld in het gegevenshoop van Experience Platform, vereist echter geavanceerde transformaties alvorens het in een gegeven kan met succes worden gebruikt het gebruikt geval van de gegevensvoer. Het uitvoeren van deze geavanceerde transformaties in uw vragen impliceert het gebruik van [&#x200B; Adobe-bepaalde functies &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/adobe-defined-functions) voor zittingssessie, attributie, en deduplicatie. Zie [&#x200B; Voorbeelden &#x200B;](#examples) op hoe te om deze functies te gebruiken.

#### Zoeken

Als u gegevens uit andere gegevenssets wilt opzoeken, gebruikt u standaard SQL-functionaliteit (`WHERE` -component, `INNER JOIN` , `OUTER JOIN` en andere).

#### Berekeningen

Om berekeningen op gebieden (kolommen) uit te voeren, gebruik de standaardSQL functies (bijvoorbeeld `COUNT(*)`), of [&#x200B; wiskunde en statistische exploitanten en functies &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/spark-sql-functions#math) deel van SQL van de Vonk. Ook, [&#x200B; vensterfuncties &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/adobe-defined-functions#window-functions) verlenen steun om samenvoegingen bij te werken en enige punten voor elke rij in een bevolen ondergroep terug te keren. Zie [&#x200B; Voorbeelden &#x200B;](#examples) op hoe te om deze functies te gebruiken.

#### Geneste gegevensstructuur

De schema&#39;s waarop de datasets worden gebaseerd bevatten vaak complexe gegevenstypen, met inbegrip van geneste gegevensstructuren. Eerder vermeld `identityMap` is een voorbeeld van een geneste gegevensstructuur. Zie hieronder voor een voorbeeld van `identityMap` data.

```json
{
   "identityMap":{
      "FPID":[
         {
            "id":"55613368189701342632255821452918751312",
            "authenticatedState":"ambiguous"
         }
      ],
      "CRM":[
         {
            "id":"2394509340-30453470347",
            "authenticatedState":"authenticated"
         }
      ]
   }
}
```

U kunt [`explode()` of andere functies van Arrays &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/spark-sql-functions#arrays) van SQL van de Vonk gebruiken om aan de gegevens binnen een genestelde gegevensstructuur, bijvoorbeeld te krijgen:

```sql
select explode(identityMap) from demosys_cja_ee_v1_website_global_v1_1 limit 15;
```

U kunt ook naar afzonderlijke elementen verwijzen met puntnotatie. Bijvoorbeeld:

```sql
select identityMap.ecid from demosys_cja_ee_v1_website_global_v1_1 limit 15;
```

Zie [&#x200B; Werkend met genestelde gegevensstructuren in de Dienst van de Vraag &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/nested-data-structures) voor meer informatie.


#### Voorbeelden

Voor vragen:

- die gegevens uit gegevensreeksen in het gegevensmeer van Experience Platform gebruiken;
- tikken op de extra mogelijkheden van Adobe Defined Functions en/of Spark SQL, en
- die vergelijkbare resultaten zouden opleveren als een gelijkwaardige Adobe Analytics-gegevenstoevoer,

zie:

- [&#x200B; verlaten doorbladeren &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/use-cases/abandoned-browse)
- [&#x200B; attributieanalyse &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/use-cases/attribution-analysis)
- [&#x200B; bot het filtreren &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/use-cases/bot-filtering)
- en andere [&#x200B; gesteunde gebruiksgevallen in de gids van de Dienst van de Vraag &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/use-cases/overview).

Hieronder ziet u een voorbeeld waarin u de toewijzing op de juiste wijze kunt toepassen op verschillende sessies. Zo ziet u hoe u

- de laatste 90 dagen gebruiken als terugzoekactie;
- vensterfuncties zoals sessionisatie en / of attributie toepassen, en
- de uitvoer beperken op basis van de `ingest_time` .

  +++ Details

  Om dit te doen, moet je...

   - Gebruik een tabel met verwerkingsstatus, `checkpoint_log` , om de huidige versus de laatste ingangstijd bij te houden. Zie [&#x200B; deze gids &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/incremental-load) voor meer informatie.
   - Schakel het neerzetten van systeemkolommen uit, zodat u `_acp_system_metadata.ingestTime` kunt gebruiken.
   - Gebruik een binnenste `SELECT` om de velden te grijpen die u wilt gebruiken en de gebeurtenissen te beperken tot de terugzoekperiode voor sessionisatie- en/of attributieberekeningen. Bijvoorbeeld 90 dagen.
   - Gebruik een niveau op het volgende niveau `SELECT` om u sessionisatie- en/of attributievensters en andere berekeningen toe te passen.
   - Gebruik `INSERT INTO` in de uitvoertabel om de terugzoekopdracht te beperken tot alleen de gebeurtenissen die zijn gearriveerd sinds de laatste verwerkingstijd. U doet dit door op `_acp_system_metadata.ingestTime ` tegenover de tijd te filtreren laatst die in uw lijst van de verwerkingsstatus wordt opgeslagen.

  **de functies van het venster van de Zitting voorbeeld**

  ```sql
  $$ BEGIN
     -- Disable dropping system columns
     set drop_system_columns=false; 
  
     -- Initialize variables
     SET @last_updated_timestamp = SELECT CURRENT_TIMESTAMP;
  
     -- Get the last processed batch ingestion time
     SET @from_batch_ingestion_time = SELECT coalesce(last_batch_ingestion_time, 'HEAD') 
        FROM checkpoint_log a 
        JOIN (
              SELECT MAX(process_timestamp) AS process_timestamp 
              FROM checkpoint_log
              WHERE process_name = 'data_feed' 
              AND process_status = 'SUCCESSFUL'
        ) b
        ON a.process_timestamp = b.process_timestamp;
  
     -- Get the last batch ingestion time
     SET @to_batch_ingestion_time = SELECT MAX(_acp_system_metadata.ingestTime) 
        FROM events_dataset;
  
     -- Sessionize the data and insert into data_feed.
     INSERT INTO data_feed
     SELECT *
     FROM (
        SELECT
              userIdentity,
              timestamp,
              SESS_TIMEOUT(timestamp, 60 * 30) OVER (
                 PARTITION BY userIdentity
                 ORDER BY timestamp
                 ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW
              ) AS session_data,
              page_name,
              ingest_time
        FROM (
              SELECT
                 userIdentity,
                 timestamp,
                 web.webPageDetails.name AS page_name,
                 _acp_system_metadata.ingestTime AS ingest_time
              FROM events_dataset
              WHERE timestamp >= current_date - 90
        ) AS a
        ORDER BY userIdentity, timestamp ASC
     ) AS b
     WHERE b.ingest_time >= @from_batch_ingestion_time;
  
     -- Update the checkpoint_log table
     INSERT INTO checkpoint_log
     SELECT
        'data_feed' process_name,
        'SUCCESSFUL' process_status,
        cast(@to_batch_ingestion_time AS string) last_batch_ingestion_time,
        cast(@last_updated_timestamp AS TIMESTAMP) process_timestamp
  END
  $$;
  ```

  **de functies van het venster van de Attributie voorbeeld**

  ```sql
  $$ BEGIN
   SET drop_system_columns=false;
  
  -- Initialize variables
   SET @last_updated_timestamp = SELECT CURRENT_TIMESTAMP;
  
  -- Get the last processed batch ingestion time 1718755872325
   SET @from_batch_ingestion_time =
       SELECT coalesce(last_snapshot_id, 'HEAD')
       FROM checkpoint_log a
       JOIN (
           SELECT MAX(process_timestamp) AS process_timestamp
           FROM checkpoint_log
           WHERE process_name = 'data_feed'
           AND process_status = 'SUCCESSFUL'
       ) b
       ON a.process_timestamp = b.process_timestamp;
  
   -- Get the last batch ingestion time 1718758687865
   SET @to_batch_ingestion_time =
       SELECT MAX(_acp_system_metadata.ingestTime)
       FROM demo_data_trey_mcintyre_midvalues;
  
   -- Sessionize the data and insert into new_sessionized_data
   INSERT INTO new_sessionized_data
   SELECT *
   FROM (
       SELECT
           _id,
           timestamp,
           struct(User_Identity,
           cast(SESS_TIMEOUT(timestamp, 60 * 30) OVER (
               PARTITION BY User_Identity
               ORDER BY timestamp
               ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW
           ) as string) AS SessionData,
           to_timestamp(from_unixtime(ingest_time/1000, 'yyyy-MM-dd HH:mm:ss')) AS IngestTime,      
           PageName,
           first_url,
           first_channel_type
             ) as _demosystem5
       FROM (
           SELECT
               _id,
               ENDUSERIDS._EXPERIENCE.MCID.ID as User_Identity,
               timestamp,
               web.webPageDetails.name AS PageName,
              attribution_first_touch(timestamp, '', web.webReferrer.url) OVER (PARTITION BY ENDUSERIDS._EXPERIENCE.MCID.ID ORDER BY timestamp ASC ROWS BETWEEN UNBOUNDED PRECEDING AND UNBOUNDED FOLLOWING).value AS first_url,
              attribution_first_touch(timestamp, '',channel.typeAtSource) OVER (PARTITION BY ENDUSERIDS._EXPERIENCE.MCID.ID ORDER BY timestamp ASC ROWS BETWEEN UNBOUNDED PRECEDING AND UNBOUNDED FOLLOWING).value AS first_channel_type,
               _acp_system_metadata.ingestTime AS ingest_time
           FROM demo_data_trey_mcintyre_midvalues
           WHERE timestamp >= current_date - 90
       )
       ORDER BY User_Identity, timestamp ASC    
   )
   WHERE _demosystem5.IngestTime >= to_timestamp(from_unixtime(@from_batch_ingestion_time/1000, 'yyyy-MM-dd HH:mm:ss'));
  
  -- Update the checkpoint_log table
  INSERT INTO checkpoint_log
  SELECT
     'data_feed' as process_name,
     'SUCCESSFUL' as process_status,
     cast(@to_batch_ingestion_time AS string) as last_snapshot_id,
     cast(@last_updated_timestamp AS timestamp) as process_timestamp;
  
  END
  $$;
  ```

  +++


### Zoekopdracht plannen

U plant de vraag om ervoor te zorgen dat de vraag wordt uitgevoerd en dat de resultaten bij uw aangewezen interval worden geproduceerd.

#### Query-editor gebruiken

U kunt een vraag plannen gebruikend de Redacteur van de Vraag. Wanneer het plannen van de vraag, bepaalt u een outputdataset. Zie [&#x200B; de programma&#39;s van de Vraag &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/query-schedules) voor meer informatie.


#### API voor Query Service gebruiken

Alternatief kunt u RESTful APIs gebruiken om een vraag en een programma voor de vraag te bepalen. Zie de [&#x200B; gids van de Dienst API van de Vraag &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/query/api/getting-started) voor meer informatie.
Verzeker u de outputdataset als deel van het facultatieve `ctasParameters` bezit wanneer het creëren van de vraag ([&#x200B; creeer een vraag &#x200B;](https://developer.adobe.com/experience-platform-apis/references/query-service/#tag/Queries/operation/createQuery)) of wanneer het creëren van het programma voor een vraag ([&#x200B; creeer een geplande vraag &#x200B;](https://developer.adobe.com/experience-platform-apis/references/query-service/#tag/Schedules/operation/createSchedule)).



## Gegevensbestanden exporteren

Zodra u hebt gecreeerd en uw vraag gepland, en de resultaten geverifieerd, kunt u de ruwe datasets aan de bestemmingen van de wolkenopslag dan uitvoeren. Deze uitvoer is in de terminologie van de Doelen van Experience Platform die als de uitvoerbestemmingen van de Dataset wordt bedoeld. Zie [&#x200B; datasets van de Uitvoer aan de bestemmingen van de wolkenopslag &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets) voor een overzicht.

De volgende bestemmingen voor cloudopslag worden ondersteund:

- [&#x200B; Azure Data Lake Storage Gen2 &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2)
- [&#x200B; Gegevens die Zone &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone) aanvoeren
- [&#x200B; Google Cloud Storage &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage)
- [&#x200B; Amazon S3 &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3)
- [&#x200B; Azure Blob &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob)
- [&#x200B; SFTP &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp)


### EXPERIENCE PLATFORM UI

U kunt de uitvoer van uw outputdatasets door Experience Platform UI uitvoeren en plannen. In dit gedeelte worden de desbetreffende stappen beschreven.

#### Doel selecteren

Wanneer u hebt bepaald welke bestemming van de wolkenopslag u de outputdataset aan wilt uitvoeren, [&#x200B; selecteer de bestemming &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#select-destination). Wanneer u nog geen bestemming voor uw aangewezen wolkenopslag hebt gevormd, moet u [&#x200B; een nieuwe bestemmingsverbinding &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/connect-destination) tot stand brengen.

Als deel van het vormen van een bestemming, kunt u

- het bestandstype (JSON of Parquet) definiëren;
- of het resulterende bestand al dan niet moet worden gecomprimeerd, en
- of een manifestbestand al dan niet moet worden opgenomen.


#### Gegevensset selecteren

Wanneer u het doel hebt geselecteerd, moet u in de volgende **[!UICONTROL Select datasets]** stap uw outputdataset van de lijst van datasets selecteren. Als u veelvoudige geplande vragen hebt tot stand gebracht, en u de outputdatasets naar de zelfde bestemming van de wolkenopslag wilt verzenden, kunt u de overeenkomstige outputdatasets selecteren. Zie [&#x200B; selecteren uw datasets &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#select-datasets) voor meer informatie.

#### Gegevensexport voor schema

Tot slot wilt u de uitvoer van uw dataset plannen als deel van de **[!UICONTROL Scheduling]** stap. In die stap kunt u het programma bepalen en of de uitvoer van de outputdataset incrementeel of niet zou moeten zijn. Zie [&#x200B; de datasetuitvoer van het Programma &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#scheduling) voor meer informatie.


#### Slotstappen

[&#x200B; Overzicht &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#review) uw selectie, en wanneer correct, begin uw outputdataset aan de bestemming van de wolkenopslag te exporteren.

U moet [&#x200B; verifiëren &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#verify) een succesvolle gegevensuitvoer. Bij het exporteren van gegevenssets maakt Experience Platform een of meer `.json` - of `.parquet` -bestanden op de opslaglocatie die in uw bestemming is gedefinieerd. Nieuwe bestanden worden naar verwachting op uw opslaglocatie gedeponeerd volgens het exportschema dat u instelt. Experience Platform maakt een mapstructuur op de opslaglocatie die u hebt opgegeven als onderdeel van de geselecteerde bestemming, waar de geëxporteerde bestanden worden opgeslagen. Voor elke exporttijd wordt een nieuwe map gemaakt, volgens het patroon: `folder-name-you-provided/datasetID/exportTime=YYYYMMDDHHMM` . De standaardbestandsnaam wordt willekeurig gegenereerd en zorgt ervoor dat geëxporteerde bestandsnamen uniek zijn.

### Flow Service-API

Alternatief, kunt u de uitvoer van outputdatasets uitvoeren en plannen gebruikend APIs. De betrokken stappen worden gedocumenteerd in [&#x200B; datasets van de Uitvoer door de Dienst API van de Stroom te gebruiken &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets).

#### Aan de slag

Om datasets uit te voeren, verzeker u de [&#x200B; vereiste toestemmingen &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#permissions) hebt. Verifieer ook dat de bestemming waarnaar u uw outputdataset wilt verzenden het uitvoeren van datasets steunt. U moet dan [&#x200B; de waarden voor vereiste en facultatieve kopballen &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#gather-values-headers) verzamelen die u in de API vraag gebruikt. U moet ook [&#x200B; de verbindingsspecificatie en stroom specifieke IDs van de bestemming &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#gather-connection-spec-flow-spec) identificeren u van plan bent datasets naar uit te voeren.

#### In aanmerking komende gegevenssets ophalen

U kunt [&#x200B; een lijst van in aanmerking komende datasets &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#retrieve-list-of-available-datasets) voor de uitvoer terugwinnen en verifiëren of uw outputdataset deel van die lijst gebruikend [`GET /connectionSpecs/{id}/configs` &#x200B;](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Configurations/operation/getDatasets) API uitmaakt.


#### Bronverbinding maken

Daarna moet u [&#x200B; een bronverbinding &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#create-source-connection) voor de outputdataset tot stand brengen, gebruikend zijn unieke identiteitskaart, die u naar de bestemming van de wolkenopslag wilt uitvoeren. U gebruikt [`POST /sourceConnections` &#x200B;](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Source-connections/operation/postSourceConnection) API.

#### Verifiëren voor bestemming (basisverbinding maken)

U moet nu [&#x200B; een basisverbinding &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#create-base-connection) tot stand brengen om de geloofsbrieven aan uw bestemming van de wolkenopslag voor authentiek te verklaren en veilig op te slaan gebruikend [`POST /targetConection` &#x200B;](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/postTargetConnection) API.


#### Exportparameters opgeven

Daarna, moet u [&#x200B; een extra doelverbinding tot stand brengen die de uitvoerparameters &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#create-target-connection) voor uw outputdataset opslaat gebruikend, eens meer, [`POST /targetConection` &#x200B;](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/postTargetConnection) API. Deze exportparameters zijn onder andere locatie, bestandsindeling, compressie en meer.

#### Gegevensstroom instellen

Tot slot [&#x200B; opstelling dataflow &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#create-dataflow) om ervoor te zorgen dat uw outputdataset wordt uitgevoerd naar uw bestemming van de wolkenopslag gebruikend [`POST /flows` &#x200B;](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Dataflows/operation/postFlow) API. In deze stap, kunt u het programma voor de uitvoer bepalen, gebruikend de `scheduleParams` parameter.

#### Gegevensstroom valideren

Om [&#x200B; succesvolle uitvoeringen van uw dataflow &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#get-dataflow-runs) te controleren, gebruik [`GET /runs` &#x200B;](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Dataflow-runs/operation/getFlowRuns) API, die dataflow identiteitskaart als vraagparameter specificeren. Deze gegevensstroom-id is een id die wordt geretourneerd wanneer u de gegevensstroom instelt.

[&#x200B; verifieer &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#verify) een succesvolle gegevensuitvoer. Bij het exporteren van gegevenssets maakt Experience Platform een of meer `.json` - of `.parquet` -bestanden op de opslaglocatie die in uw bestemming is gedefinieerd. Nieuwe bestanden worden naar verwachting op uw opslaglocatie gedeponeerd volgens het exportschema dat u instelt. Experience Platform maakt een mapstructuur op de opslaglocatie die u hebt opgegeven als onderdeel van de geselecteerde bestemming, waar de geëxporteerde bestanden worden opgeslagen. Voor elke exporttijd wordt een nieuwe map gemaakt, volgens het patroon: `folder-name-you-provided/datasetID/exportTime=YYYYMMDDHHMM` . De standaardbestandsnaam wordt willekeurig gegenereerd en zorgt ervoor dat geëxporteerde bestandsnamen uniek zijn.

## Conclusie

Kortom, het emuleren van de functionaliteit Adobe Analytics Data Feed impliceert het instellen van geplande query&#39;s met behulp van Query Service en het gebruik van de resultaten van deze query&#39;s in geplande gegevensset-exportbewerkingen.

>[!IMPORTANT]
>
>Twee planners zijn betrokken in dit gebruiksgeval. Om een behoorlijk werk van de geëmuleerde functionaliteit van de gegevensvoer te waarborgen, zorg ervoor dat de programma&#39;s die in de Dienst van de Vraag en de uitvoer van Gegevens worden gevormd zich niet mengen.
