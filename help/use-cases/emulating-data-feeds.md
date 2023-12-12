---
title: Functionaliteit voor gegevensinvoer emuleren
description: Begrijp hoe u Adobe Analytics gegevensvoer met gegevens in Experience Platform kunt simuleren.
solution: Customer Journey Analytics
feature: Use Cases
hide: true
hidefromtoc: true
source-git-commit: d6e10a00bf9afb2788f99800e09a7e80fd31e489
workflow-type: tm+mt
source-wordcount: '2103'
ht-degree: 0%

---

# Functionaliteit voor gegevensinvoer emuleren

Adobe Analytics-gegevensfeeds zijn een krachtige manier om onbewerkte gegevens uit Adobe Analytics te halen. Met dit gebruiksgeval wordt beschreven hoe u vergelijkbare soorten onbewerkte gegevens uit het Experience Platform kunt halen en kunt gebruiken op andere platformen buiten de Adobe en naar eigen goeddunken van uw organisatie.

## Vereisten

Zorg ervoor dat u aan alle volgende vereisten voldoet voordat u de functionaliteit gebruikt die in dit gebruiksgeval wordt beschreven:

* Een werkende implementatie die online en off-line gegevens naar het gegevensmeer van het Experience Platform verzendt.
* Toegang tot de Dienst van de Vraag, die als deel van op vorm-gebaseerde toepassingen of de gegevens Distiller toe:voegen-op wordt verpakt. Zie [Query Service verpakken](https://experienceleague.adobe.com/docs/experience-platform/query/packaging.html?lang=en) voor meer informatie .
* Toegang tot de functionaliteit voor het exporteren van gegevenssets, beschikbaar voor klanten die het Real-Time CDP-pakket Premier of Ultimate, Adobe Journey Optimizer of Customer Journey Analytics hebben aangeschaft. Zie [Gegevenssets exporteren naar cloudopslagbestemmingen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en) voor meer informatie .
* Een of meer doelen (bijvoorbeeld: Amazon S3, Google Cloud Storage) geconfigureerd voor het exporteren van de onbewerkte gegevens van uw gegevensfeed.

## Inleiding

Het emuleren van een Adobe Analytics-gegevensfeed omvat:

* een **geplande query** dat de gegevens voor uw gegevensvoer als outputdataset produceert, gebruikend **Query-service**.
* een **geplande gegevensset exporteren** dat de outputdataset naar een bestemming van de wolkenopslag uitvoert, gebruikend **Dataset exporteren**.


![Gegevensfeed](assets/data-feed.svg)


## Query-service

De Dienst van de Vraag van het Experience Platform staat u toe om het even welke dataset in het Meer van Gegevens van het Experience Platform te vragen en zich aan te sluiten alsof het een gegevensbestandlijst is. Vervolgens kunt u de resultaten vastleggen als een nieuwe gegevensset voor verder gebruik in rapportage of voor export.

U gebruikt de Dienst van de Vraag [gebruikersinterface](https://experienceleague.adobe.com/docs/experience-platform/query/ui/overview.html?lang=en), [client verbonden via het PostgresSQL-protocol](https://experienceleague.adobe.com/docs/experience-platform/query/clients/overview.html?lang=en), of [RESTful-API&#39;s](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=en) om vragen tot stand te brengen en te plannen die de gegevens voor uw gegevensvoer verzamelen.

### Query maken

U kunt alle functionaliteit van standaardANSI SQL voor UITGEZOCHTE verklaringen en andere beperkte bevelen gebruiken om de vragen tot stand te brengen en uit te voeren die de gegevens voor uw gegevensvoer produceren. Zie [SQL-syntaxis](https://experienceleague.adobe.com/docs/experience-platform/query/sql/syntax.html?lang=en) voor meer informatie . Buiten deze SQL-syntaxis ondersteunt Adobe:

* voorgebouwd [Adobe-bepaalde functies (ADF)](https://experienceleague.adobe.com/docs/experience-platform/query/sql/adobe-defined-functions.html?lang=en) die helpen gemeenschappelijke zaken-gerelateerde taken op gebeurtenisgegevens uitvoeren die in de gegevens van het Experience Platform meer worden opgeslagen, met inbegrip van functies voor [Sessionering](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-mobile-visit-processing.html?lang=en) en [Attributie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/overview.html?lang=en),
* meerdere ingebouwde [SQL-functies in Spark](https://experienceleague.adobe.com/docs/experience-platform/query/sql/spark-sql-functions.html?lang=en),
* [Metagegevens, PostgreSQL-opdrachten](https://experienceleague.adobe.com/docs/experience-platform/query/sql/metadata.html?lang=en),
* [voorbereide instructies](https://experienceleague.adobe.com/docs/experience-platform/query/sql/prepared-statements.html?lang=en).


#### Voorbeelden

Hieronder staan enkele voorbeelden van query&#39;s die gegevens verzamelen voor uw gegevensfeeds. Deze voorbeelden gebruiken `demo_system_event_dataset_for_website_global_v1_1` als de voorbeeldervaringsgegevensset met gegevens die zijn verzameld bij klanten die met de website communiceren.

+++Top vijf producten

*Wat zijn de vijf belangrijkste producten op de website?*

```sql
select productListItems.name, count(*)
from   demo_system_event_dataset_for_website_global_v1_1
where  eventType = 'commerce.productViews'
group  by productListItems.name
order  by 2 desc
limit 5;
```

+++

+++Trechter voor interactie van het product

*Wat zijn de verschillende productinteracties op de website?*

```sql
select eventType, count(*)
from   demo_system_event_dataset_for_website_global_v1_1
where  eventType is not null
and    eventType <> ''
group  by eventType;
```

+++

+++Wat doen mensen?

*Wat doen de mensen op de plaats alvorens de &quot;Cancel pagina van de Dienst&quot;als derde pagina in een zitting te bereiken?*

Deze vraag gebruikt de Adobe bepaalde Functies `SESS_TIMEOUT` en `NEXT`.

* De `SESS_TIMEOUT()` geeft een overzicht van de met Adobe Analytics gevonden bezoeken. Het voert een gelijkaardige op tijd-gebaseerde groepering uit, maar met klantgerichte parameters.
* `NEXT()` en `PREVIOUS()` helpen u te begrijpen hoe klanten door uw site navigeren.

```sql
SELECT
  webPage,
  webPage_2,
  webPage_3,
  webPage_4,
  count(*) journeys
FROM
  (
      SELECT
        webPage,
        NEXT(webPage, 1, true)
          OVER(PARTITION BY ecid, session.num
                ORDER BY timestamp
                ROWS BETWEEN CURRENT ROW AND UNBOUNDED FOLLOWING).value
          AS webPage_2,
        NEXT(webPage, 2, true)
          OVER(PARTITION BY ecid, session.num
                ORDER BY timestamp
                ROWS BETWEEN CURRENT ROW AND UNBOUNDED FOLLOWING).value
          AS webPage_3,
        NEXT(webPage, 3, true)
           OVER(PARTITION BY ecid, session.num
                ORDER BY timestamp
                ROWS BETWEEN CURRENT ROW AND UNBOUNDED FOLLOWING).value
          AS webPage_4,
        session.depth AS SessionPageDepth
      FROM (
            select a._sampleorg.identification.core.ecid as ecid,
                   a.timestamp,
                   web.webPageDetails.name as webPage,
                    SESS_TIMEOUT(timestamp, 60 * 30)
                       OVER (PARTITION BY a._sampleorg.identification.core.ecid
                             ORDER BY timestamp
                             ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW)
                  AS session
            from   demo_system_event_dataset_for_website_global_v1_1 a
            where  a._sampleorg.identification.core.ecid in (
                select b._sampleorg.identification.core.ecid
                from   demo_system_event_dataset_for_website_global_v1_1 b
                where  b.web.webPageDetails.name = 'Cancel Service'
            )
        )
)
WHERE SessionPageDepth=1
and   webpage_3 = 'Cancel Service'
GROUP BY webPage, webPage_2, webPage_3, webPage_4
ORDER BY journeys DESC
LIMIT 10;
```

+++

+++Hoeveel tijd

*Hoeveel tijd hebt u alvorens een bezoeker het vraagcentrum na het bezoeken van de &quot;Cancel Pagina van de Dienst&quot;roept?*

Om dit soort vraag te beantwoorden, gebruikt u `TIME_BETWEEN_NEXT_MATCH()` Door Adobe gedefinieerde functie. De tijd-tussen vorige of volgende gelijke functies verstrekken een nieuwe dimensie, die de tijd meet die sinds een bepaald incident is verstreken.

```sql
select * from (
       select _sampleorg.identification.core.ecid as ecid,
              web.webPageDetails.name as webPage,
              TIME_BETWEEN_NEXT_MATCH(timestamp, web.webPageDetails.name='Call Start', 'seconds')
              OVER(PARTITION BY _sampleorg.identification.core.ecid
                  ORDER BY timestamp
                  ROWS BETWEEN CURRENT ROW AND UNBOUNDED FOLLOWING)
              AS contact_callcenter_after_seconds
       from   demo_system_event_dataset_for_website_global_v1_1
       where  web.webPageDetails.name in ('Cancel Service', 'Call Start')
) r
where r.webPage = 'Cancel Service'
limit 15;
```

+++

+++Wat is het resultaat?

*Wat is het resultaat van klanten die het callcenter roepen?*

Voor deze query, `demo_system_event_dataset_for_website_global_v1_1` dataset is verbonden met een voorbeeld `demo_system_event_dataset_for_call_center_global_v1_1` dataset die vraagcentruminteractie bevat.

```sql
select distinct r.*,
       c._sampleorg.interactionDetails.core.callCenterAgent.callFeeling,
       c._sampleorg.interactionDetails.core.callCenterAgent.callTopic,
       c._sampleorg.interactionDetails.core.callCenterAgent.callContractCancelled
from (
       select _sampleorg.identification.core.ecid ecid,
              web.webPageDetails.name as webPage,
              TIME_BETWEEN_NEXT_MATCH(timestamp, web.webPageDetails.name='Call Start', 'seconds')
              OVER(PARTITION BY _sampleorg.identification.core.ecid
                  ORDER BY timestamp
                  ROWS BETWEEN CURRENT ROW AND UNBOUNDED FOLLOWING)
              AS contact_callcenter_after_seconds
       from   demo_system_event_dataset_for_website_global_v1_1
       where  web.webPageDetails.name in ('Cancel Service', 'Call Start')
) r
, demo_system_event_dataset_for_call_center_global_v1_1 c
where r.ecid = c._sampleorg.identification.core.ecid
and r.webPage = 'Cancel Service'
and c._sampleorg.interactionDetails.core.callCenterAgent.callContractCancelled IN (true,false)
and c._sampleorg.interactionDetails.core.callCenterAgent.callTopic IN ('contract', 'invoice','complaint','wifi')
limit 15;
```

+++

+++Betrokkenheid bij marketingkanalen (Adobe Analytics-gegevens)

*Wat is de betrokkenheid van de verschillende marketingkanalen voor Italiaans gericht webverkeer?*

In dit voorbeeld wordt de gegevensset gebruikt die automatisch door de Adobe Analytics-bronconnector wordt gemaakt, bijvoorbeeld `demo_data_sample_org_midvalues`.

```sql
select 
    channel.typeAtSource, count(*) 
from 
    demo_data_sample_org_midvalues 
where 
    (channel.typeAtSource IS NOT NULL
and
    web.webPageDetails.URL LIKE '%/it/it/%')
group by 
    channel.typeAtSource
order by 2 desc;
```

+++

Voor nog meer (geavanceerde) steekproefvragen zie [verlaten browsers](https://experienceleague.adobe.com/docs/experience-platform/query/use-cases/abandoned-browse.html?lang=en), [toewijzingsanalyse](https://experienceleague.adobe.com/docs/experience-platform/query/use-cases/attribution-analysis.html?lang=en), [bot filteren](https://experienceleague.adobe.com/docs/experience-platform/query/use-cases/bot-filtering.html?lang=en)en andere voorbeelden in de Guide van de Query-service.


#### Identiteiten

In Experience Platform zijn verschillende identiteiten beschikbaar. Zorg ervoor dat u de identiteiten correct opvraagt. In de bovenstaande voorbeelden wordt ECID gedefinieerd als onderdeel van een kernobject, dat zelf deel uitmaakt van een identificatieobject, en beide toegevoegd aan het schema met behulp van een Experience Event Core-veldgroep (bijvoorbeeld: `_sampleorg.identification.core.ecid`). De ECIDs zou verschillend in uw schema&#39;s kunnen worden georganiseerd.

U kunt ook `identityMap` om naar identiteiten te zoeken. Dit object is van het type `Map` en gebruikt een [geneste gegevensstructuur](#nested-data-structure).

Voor gegevens die via de Adobe Analytics-bronaansluiting worden ingevoerd, zijn mogelijk meerdere identiteiten beschikbaar. De primaire id hangt af van het bestaan van een ECID of een HULP. Zie [Primaire id&#39;s in Adobe Analytics-gegevens](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=en#how-the-analytics-source-treats-identities) en [STEUN, ECID, AACUSTOMID en de bronaansluiting voor Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aaid-ecid-adc.html?lang=en) voor meer informatie

#### Gegevensvoederkolommen

De gebieden (kolommen) u in uw vraag kunt gebruiken hangen van de schemadefinitie af waarop uw datasets worden gebaseerd. Zorg ervoor u het schema onderaan de dataset begrijpt.

In sommige van de [voorbeeldquery&#39;s](#examples) u vroeg om *paginanaam*.

* In de gebruikersinterface van Adobe Analytics Data Feed selecteert u **[!UICONTROL pagename]** als de kolom die moet worden toegevoegd aan de definitie van de gegevensinvoer.
* In de Dienst van de Vraag, omvat u `web.webPageDetails.name` van de `demo_system_event_dataset_for_website_global_v1_1` dataset (gebaseerd op de **Demosysteem - Gebeurtenisschema voor website (Global v1.1)** ervaringsgebeurtenisschema) in uw query. Zie de [Web Details schema-veldgroep](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/web-details.html?lang=en) voor meer informatie .

Om de afbeelding tussen de voormalige gegevenskolommen van Adobe Analytics en gebieden XDM in uw dataset van de ervaringsgebeurtenis en het onderliggende schema te begrijpen, zie [Toewijzing van analytische velden](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics.html?lang=en) en de [Adobe Analytics ExperienceEvent Volledige extensieschema, veldgroep](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/analytics-full-extension.html?lang=en) voor meer informatie .

Voorts zou de informatie die automatisch door het Web SDK van het Experience Platform (uit de doos) wordt verzameld ook relevant kunnen zijn om kolommen voor uw vraag te identificeren. Zie [Automatisch verzamelde gegevens](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/automatic-information.html?lang=en) voor meer informatie .


#### Zoeken

Om gegevens van andere datasets omhoog te kijken, gebruikt u standaardSQL functionaliteit (WAAR clausule, BINNEN VERBINDING, OUTER VERBINDING, en anderen). Zie de [Wat is het resultaat?](#examples) in de voorbeelden.

#### Berekeningen

Als u berekeningen wilt uitvoeren op velden (kolommen), gebruikt u gewoon de standaard SQL-functies (bijvoorbeeld `COUNT(*)` in de [Trechter voor productinteractie](#examples) in de voorbeelden) of de [wiskunde en statistische diensten](https://experienceleague.adobe.com/docs/experience-platform/query/sql/spark-sql-functions.html?lang=en#math) onderdeel van Spark SQL.

#### Geneste gegevensstructuur

De schema&#39;s waarop de datasets zijn gebaseerd bevatten vaak complexe gegevenstypen, waaronder geneste gegevensstructuren. Eerder genoemd `identityMap` Dit is een voorbeeld van een geneste gegevensstructuur. Zie hieronder voor een voorbeeld van `identityMap` gegevens.

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

U kunt de [`explode()` of andere Arrays](https://experienceleague.adobe.com/docs/experience-platform/query/sql/spark-sql-functions.html?lang=en#arrays) van SQL van de Vonk om aan de gegevens binnen een genestelde gegevensstructuur te krijgen.

Bijvoorbeeld:

```sql
select explode(identityMap) from demosys_cja_ee_v1_website_global_v1_1 limit 15;
```

U kunt ook naar afzonderlijke elementen verwijzen met puntnotatie. Bijvoorbeeld:

```sql
select identityMap,ecid from demosys_cja_ee_v1_website_global_v1_1 limit 15;
```

Zie [Werken met geneste gegevensstructuren in Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/key-concepts/nested-data-structures.html?lang=en) voor meer informatie .

### Zoekopdracht plannen

U plant de vraag om ervoor te zorgen dat de vraag wordt uitgevoerd en dat de resultaten bij uw aangewezen interval worden geproduceerd. Wanneer het plannen van de vraag, bepaalt u een outputdataset.

#### Query-editor gebruiken

U kunt een vraag plannen gebruikend de Redacteur van de Vraag. Wanneer het bepalen van een programma voor een vraag, kunt u de outputdataset bepalen. Zie [Zoekprogramma&#39;s](https://experienceleague.adobe.com/docs/experience-platform/query/ui/query-schedules.html?lang=en) voor meer informatie .


#### API voor Query Service gebruiken

Alternatief kunt u RESTful APIs gebruiken om een vraag en een programma voor de vraag te bepalen. Zie [API-handleiding voor query-service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=en_) voor meer informatie .
Zorg ervoor dat u de uitvoergegevensset definieert als onderdeel van de optionele `ctasParameters` eigenschap bij het maken van de query ([Een query maken](https://developer.adobe.com/experience-platform-apis/references/query-service/#tag/Queries/operation/createQuery)) of wanneer het creëren van het programma voor een vraag ([Een geplande query maken](https://developer.adobe.com/experience-platform-apis/references/query-service/#tag/Schedules/operation/createSchedule)).



## Dataset exporteren

Zodra u hebt gecreeerd en uw vraag gepland, en de resultaten in de outputdatasets geverifieerd is in overeenstemming met uw vereisten, kunt u de ruwe datasets aan de bestemmingen van de wolkenopslag dan uitvoeren. Deze uitvoer is in de terminologie van de Doelen van de Experience Platform die als de uitvoerbestemmingen van de Dataset wordt bedoeld. Zie [Gegevenssets exporteren naar cloudopslagbestemmingen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en) voor een overzicht.

De volgende bestemmingen voor cloudopslag worden ondersteund:

* [Azure Data Lake Storage Gen2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html?lang=en)
* [Gegevenslandingszone](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html?lang=en)
* [Google Cloud Storage](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html?lang=en)
* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html?lang=en#changelog)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html?lang=en#changelog)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html?lang=en#changelog)


### UI EXPERIENCE PLATFORM

U kunt de uitvoer van uw outputdatasets door het Experience Platform UI uitvoeren en plannen. In dit gedeelte worden de desbetreffende stappen beschreven.

#### Doel selecteren

Wanneer u hebt bepaald aan welke bestemming van de wolkenopslag u de outputdataset wilt uitvoeren, [selecteer het doel](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en#select-destination). Als u nog geen bestemming voor uw voorkeurscloudopslag hebt geconfigureerd, moet u [een nieuwe doelverbinding maken](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=en).

Als deel van het vormen van een bestemming kunt u het dossiertype (JSON of Parquet) bepalen, of het resulterende dossier al dan niet zou moeten worden gecomprimeerd, en of een duidelijk dossier zou moeten worden omvat of niet.


#### Gegevensset selecteren

Wanneer u het doel hebt geselecteerd, gaat u in de volgende **[!UICONTROL Select datasets]** stap u uw outputdataset van de lijst van datasets moet selecteren. Als u veelvoudige geplande vragen hebt tot stand gebracht, en u de outputdatasets naar de zelfde bestemming van de wolkenopslag wilt verzenden, kunt u de overeenkomstige outputdatasets selecteren. Zie [Uw gegevenssets selecteren](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en#select-datasets) voor meer informatie .

#### Gegevensexport voor schema

Tot slot wilt u uw datasetuitvoer als deel van plannen **[!UICONTROL Scheduling]** stap. In die stap kunt u het programma bepalen en of de uitvoer van de outputdataset incrementeel of niet zou moeten zijn. Zie [Gegevensexport voor schema](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en#scheduling) voor meer informatie .


#### Slotstappen

[Controleren](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en#review) uw selectie en wanneer u de juiste start met het exporteren van uw uitvoergegevensset naar de opslaglocatie van de cloud.

U moet [verifiëren](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en#verify) een geslaagde gegevensexport. Bij het exporteren van gegevenssets maakt Experience Platform een of meerdere `.json` of `.parquet` bestanden op de opslaglocatie die in de bestemming is gedefinieerd. Nieuwe bestanden worden naar verwachting op uw opslaglocatie gedeponeerd volgens het exportschema dat u instelt. Experience Platform maakt een mapstructuur op de opslaglocatie die u hebt opgegeven als onderdeel van de geselecteerde bestemming, waar de geëxporteerde bestanden worden opgeslagen. Voor elke exporttijd wordt een nieuwe map gemaakt volgens het patroon: `folder-name-you-provided/datasetID/exportTime=YYYYMMDDHHMM`. De standaardbestandsnaam wordt willekeurig gegenereerd en zorgt ervoor dat geëxporteerde bestandsnamen uniek zijn.

### Flow Service-API

Alternatief, kunt u de uitvoer van outputdatasets uitvoeren en plannen gebruikend APIs. De betrokken stappen worden beschreven in [De datasets van de uitvoer door de Dienst API van de Stroom te gebruiken](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html).

#### Aan de slag

Zorg ervoor dat u beschikt over [vereiste machtigingen](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#permissions) om datasets uit te voeren en dat de bestemming waarnaar u uw outputdataset wilt verzenden het uitvoeren van datasets steunt. U moet [verzamel de waarden voor vereiste en optionele kopteksten](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#gather-values-headers) u gebruikt in de API-aanroepen, en [identificeer de verbindingsspecificaties en stroom specificeer IDs van de bestemming](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#gather-connection-spec-flow-spec) u bent van plan datasets naar uit te voeren.

#### In aanmerking komende gegevenssets ophalen

U kunt [een lijst met in aanmerking komende gegevenssets ophalen](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#retrieve-list-of-available-datasets) voor de uitvoer en verifieer of uw outputdataset deel van die lijst uitmaakt gebruikend [`GET /connectionSpecs/{id}/configs`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Configurations/operation/getDatasets) API.


#### Bronverbinding maken

Volgende moet u [een bronverbinding maken](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#create-source-connection) voor de outputdataset, gebruikend zijn unieke identiteitskaart, die u naar de bestemming van de wolkenopslag wilt uitvoeren. U gebruikt de [`POST /sourceConnections`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Source-connections/operation/postSourceConnection) API.

#### Verifiëren voor bestemming (basisverbinding maken)

U moet nu [een basisverbinding maken](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#create-base-connection) om de gegevens correct te verifiëren en veilig op te slaan naar de bestemming van de cloudopslag met de [`POST /targetConection`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/postTargetConnection) API.


#### Exportparameters opgeven

Vervolgens moet u [een extra doelverbinding maken die de exportparameters opslaat](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#create-target-connection) voor uw outputdataset die, opnieuw gebruikt [`POST /targetConection`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/postTargetConnection) API. Deze exportparameters zijn onder andere locatie, bestandsindeling, compressie en meer.

#### Gegevensstroom instellen

Tot slot [de gegevensstroom instellen](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#create-dataflow) om ervoor te zorgen dat uw uitvoergegevensset naar de opslagbestemming van de cloud wordt geëxporteerd met de [`POST /flows`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Dataflows/operation/postFlow) API. In deze stap kunt u het programma voor het exporteren definiëren met de opdracht `scheduleParams` parameter.

#### Gegevensstroom valideren

Naar [controleren succesvolle uitvoeringen van uw gegevensstroom](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#get-dataflow-runs), gebruikt u de [`GET /runs`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Dataflow-runs/operation/getFlowRuns) API, die dataflow ID als vraagparameter specificeert. Deze gegevensstroom-id is een id die wordt geretourneerd wanneer u de gegevensstroom instelt.

[Verifiëren](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en#verify) een geslaagde gegevensexport. Bij het exporteren van gegevenssets maakt Experience Platform een of meerdere `.json` of `.parquet` bestanden op de opslaglocatie die in de bestemming is gedefinieerd. Nieuwe bestanden worden naar verwachting op uw opslaglocatie gedeponeerd volgens het exportschema dat u instelt. Experience Platform maakt een mapstructuur op de opslaglocatie die u hebt opgegeven als onderdeel van de geselecteerde bestemming, waar de geëxporteerde bestanden worden opgeslagen. Voor elke exporttijd wordt een nieuwe map gemaakt volgens het patroon: `folder-name-you-provided/datasetID/exportTime=YYYYMMDDHHMM`. De standaardbestandsnaam wordt willekeurig gegenereerd en zorgt ervoor dat geëxporteerde bestandsnamen uniek zijn.

## Conclusie

Kortom, het emuleren van de functionaliteit Adobe Analytics Data Feed impliceert het instellen van geplande query&#39;s met behulp van Query Service en het gebruik van resultaten van deze query&#39;s in geplande gegevensset-exportbewerkingen.

>[!IMPORTANT]
>
>Twee planners zijn betrokken in dit gebruiksgeval. Om een behoorlijk werk van de geëmuleerde functionaliteit van de gegevensvoer te waarborgen, zorg ervoor dat de programma&#39;s die in de Dienst van de Vraag en de uitvoer van Gegevens worden gevormd zich niet mengen.






