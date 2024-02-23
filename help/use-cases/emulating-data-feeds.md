---
title: Functionaliteit voor gegevensinvoer emuleren
description: Begrijp hoe u Adobe Analytics gegevensvoer met gegevens in Experience Platform kunt simuleren.
solution: Customer Journey Analytics
feature: Use Cases
hide: true
hidefromtoc: true
role: Admin
exl-id: 71dd9e4e-1d71-424b-b984-492a3e39af5f
source-git-commit: 744c8cfc903ed841dd39b29fd3fef68ef2e7b7cb
workflow-type: tm+mt
source-wordcount: '2398'
ht-degree: 0%

---

# Functionaliteit voor gegevensinvoer emuleren

Adobe Analytics-gegevensfeeds zijn een krachtige manier om onbewerkte gegevens uit Adobe Analytics te halen. In dit geval wordt beschreven hoe u vergelijkbare onbewerkte gegevens uit het Experience Platform kunt ophalen, zodat u de gegevens kunt gebruiken op andere platformen, gereedschappen die buiten de Adobe vallen en naar eigen goeddunken van uw organisatie.

## Inleiding

Het emuleren van een Adobe Analytics-gegevensfeed omvat:

* een **geplande query** dat de gegevens voor uw gegevensvoer als outputdataset produceert ![uitvoergegevensset](assets/output-dataset.svg), gebruiken **Query-service**.
* een **geplande gegevensset exporteren** dat de outputdataset naar een bestemming van de wolkenopslag uitvoert, gebruikend **Dataset exporteren**.

![Gegevensfeed](assets/data-feed.svg)


## Vereisten

Zorg ervoor dat u aan alle volgende vereisten voldoet voordat u de functionaliteit gebruikt die in dit gebruiksgeval wordt beschreven:

* Een werkende implementatie die gegevens verzamelt in het gegevensmeer van het Experience Platform.
* Toegang tot de gegevensinvoegtoepassing Distiller om te controleren of u batch-query&#39;s mag uitvoeren. Zie [Query Service verpakken](https://experienceleague.adobe.com/docs/experience-platform/query/packaging.html?lang=en) voor meer informatie .
* Toegang tot de functionaliteit voor het exporteren van gegevenssets die beschikbaar is wanneer u het Real-Time CDP-pakket Premier of Ultimate, Adobe Journey Optimizer of Customer Journey Analytics hebt aangeschaft. Zie [Gegevenssets exporteren naar cloudopslagbestemmingen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en) voor meer informatie .
* Een of meer doelen (bijvoorbeeld: Amazon S3, Google Cloud Storage) geconfigureerd voor het exporteren van de onbewerkte gegevens van uw gegevensfeed.


## Query-service

De Dienst van de Vraag van het Experience Platform staat u toe om het even welke dataset in het meer van de gegevens van het Experience Platform te vragen en zich aan te sluiten alsof het een gegevensbestandlijst is. Vervolgens kunt u de resultaten vastleggen als een nieuwe gegevensset voor verder gebruik in rapportage of voor export.

U gebruikt de Dienst van de Vraag [gebruikersinterface](https://experienceleague.adobe.com/docs/experience-platform/query/ui/overview.html?lang=en), [client verbonden via het PostQL-protocol](https://experienceleague.adobe.com/docs/experience-platform/query/clients/overview.html?lang=en), of [RESTful-API&#39;s](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=en) om vragen tot stand te brengen en te plannen die de gegevens voor uw gegevensvoer verzamelen.

### Query maken

U kunt alle functionaliteit van standaardANSI SQL voor UITGEZOCHTE verklaringen en andere beperkte bevelen gebruiken om vragen tot stand te brengen en uit te voeren die de gegevens voor uw gegevensvoer produceren. Zie [SQL-syntaxis](https://experienceleague.adobe.com/docs/experience-platform/query/sql/syntax.html?lang=en) voor meer informatie . Buiten deze SQL-syntaxis ondersteunt Adobe:

* voorgebouwd [Adobe-bepaalde functies (ADF)](https://experienceleague.adobe.com/docs/experience-platform/query/sql/adobe-defined-functions.html?lang=en) die helpen gemeenschappelijke zaken-gerelateerde taken op gebeurtenisgegevens uitvoeren die in de gegevens van het Experience Platform meer worden opgeslagen, met inbegrip van functies voor [Sessionering](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-mobile-visit-processing.html?lang=en) en [Attributie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/overview.html?lang=en),
* meerdere ingebouwde [SQL-functies in Spark](https://experienceleague.adobe.com/docs/experience-platform/query/sql/spark-sql-functions.html?lang=en),
* [Metagegevens, PostgreSQL-opdrachten](https://experienceleague.adobe.com/docs/experience-platform/query/sql/metadata.html?lang=en),
* [voorbereide instructies](https://experienceleague.adobe.com/docs/experience-platform/query/sql/prepared-statements.html?lang=en).

#### Gegevensvoederkolommen

De XDM gebieden die u in uw vraag kunt gebruiken hangen van de schemadefinitie af waarop uw datasets worden gebaseerd. Zorg ervoor u het schema onderaan de dataset begrijpt. Zie de [UI-gids voor gegevensbestanden](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en) voor meer informatie .

Om u te helpen om de afbeelding tussen de kolommen van de Invoer van Gegevens en de gebieden te bepalen XDM, zie [Toewijzing van het veld Analytics](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics.html?lang=en). Zie ook de [Overzicht van de interface Schemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en#defining-xdm-fields) voor meer informatie hoe te om middelen XDM, met inbegrip van schema&#39;s, klassen, gebiedsgroepen, en gegevenstypes te beheren.

Als u bijvoorbeeld *paginanaam* als onderdeel van de gegevensinvoer:

* In de gebruikersinterface van Adobe Analytics Data Feed selecteert u **[!UICONTROL pagename]** als de kolom die moet worden toegevoegd aan de definitie van de gegevensinvoer.
* In de Dienst van de Vraag, omvat u `web.webPageDetails.name` van de `sample_event_dataset_for_website_global_v1_1` dataset (gebaseerd op de **Voorbeeld van gebeurtenisschema voor website (Global v1.1)** ervaringsgebeurtenisschema) in uw query. Zie de [Web Details schema-veldgroep](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/web-details.html?lang=en) voor meer informatie .

<!--
To understand the mapping between Adobe Analytics data feed columns and XDM fields in your experience event dataset and underlying schema, see [Analytics fields mapping](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics.html?lang=en) and [Adobe Analytics ExperienceEvent Full Extension schema field group](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/event/analytics-full-extension.html?lang=en) for more information.

Furthermore, the [automatically collected information by the Experience Platform Web SDK (out of the box)](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/automatic-information.html?lang=en) might be relevant to identify columns for your query.
-->

#### Identiteiten

In Experience Platform zijn verschillende identiteiten beschikbaar. Zorg er bij het maken van query&#39;s voor dat u de id&#39;s correct opvraagt.


Vaak vindt u identiteiten in een afzonderlijke veldgroep. In een implementatie ECID (`ecid`) kan worden gedefinieerd als onderdeel van een veldgroep met een `core` object, dat zelf deel uitmaakt van een `identification` object (bijvoorbeeld: `_sampleorg.identification.core.ecid`). De ECIDs zou verschillend in uw schema&#39;s kunnen worden georganiseerd.

U kunt ook `identityMap` om naar identiteiten te zoeken. Dit object is van het type `Map` en gebruikt een [geneste gegevensstructuur](#nested-data-structure).

Zie [Identiteitsvelden definiëren in de gebruikersinterface](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/fields/identity.html?lang=en) voor meer informatie over het definiëren van identiteitsvelden in Experience Platform.

Zie [Primaire id-id&#39;s in analysegegevens](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=en#primary-identifiers-in-analytics-data) voor meer informatie over de manier waarop Adobe Analytics-identiteiten worden toegewezen aan Experience Platform-id&#39;s wanneer de bronconnector Analytics wordt gebruikt. Dit kan als richtlijn dienen die uw identiteiten plaatst, zelfs wanneer het gebruiken van niet de analytische bronschakelaar.


#### Gegevens en identificatie op bedrijfsniveau

Op basis van de implementatie worden gegevens op raakniveau die traditioneel in Adobe Analytics worden verzameld, nu opgeslagen als tijdstempelgegevens voor gebeurtenissen in Experience Platform. De volgende tabel wordt geëxtraheerd uit [Toewijzing van het veld Analytics](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics.html?lang=en#generated-mapping-fields) en toont voorbeelden hoe te om niveau-specifieke kolommen van de Invoer van Gegevens van Adobe Analytics met overeenkomstige XDM gebieden in uw vragen in kaart te brengen. De tabel bevat ook voorbeelden van hoe treffers, bezoeken en bezoekers worden geïdentificeerd met behulp van XDM-velden.

| Kolom Gegevensfeed | XDM-veld | Type | Beschrijving |
|---|---|---|---|
| `hitid_high` + `hitid_low` | `_id` | string | Een unieke id om een treffer te identificeren. |
| `hitid_low` | `_id` | string | Gebruikt met `hitid_high` om een treffer op unieke wijze te identificeren. |
| `hitid_high` | `_id` | string | Gebruikt met `hitid_high` om een treffer op unieke wijze te identificeren. |
| `hit_time_gmt` | `receivedTimestamp` | string | De tijdstempel van de hit, gebaseerd op UNIX®-tijd. |
| `cust_hit_time_gmt` | `timestamp` | string | Dit wordt slechts gebruikt in timestamp-Toegelaten datasets. Dit is de tijdstempel die met de hit wordt verzonden, op basis van UNIX®-tijd. |
| `visid_high` + `visid_low` | `identityMap` | object | Een unieke id voor een bezoek. |
| `visid_high` + `visid_low` | `endUserIDs._experience.aaid.id` | string | Een unieke id voor een bezoek. |
| `visid_high` | `endUserIDs._experience.aaid.primary` | boolean | Gebruikt met `visid_low` om een bezoek op unieke wijze te identificeren. |
| `visid_high` | `endUserIDs._experience.aaid.namespace.code` | string | Gebruikt met `visid_low` om een bezoek op unieke wijze te identificeren. |
| `visid_low` | `identityMap` | object | Gebruikt met `visid_high` om een bezoek op unieke wijze te identificeren. |
| `cust_visid` | `identityMap` | object | De bezoeker-id van de klant. |
| `cust_visid` | `endUserIDs._experience.aacustomid.id` | object | De bezoeker-id van de klant. |
| `cust_visid` | `endUserIDs._experience.aacustomid.primary` | boolean | De naamruimtecode van de bezoeker-id van de klant. |
| `cust_visid` | `endUserIDs._experience.aacustomid.namespace.code` | string | Gebruikt met `visid_low` om de id van de bezoeker van de klant op unieke wijze te identificeren. |
| `geo\_*` | `placeContext.geo.* ` | tekenreeks, getal | Geolocatiegegevens, zoals land, regio, stad en andere |
| `event_list` | `commerce.purchases`, `commerce.productViews`, `commerce.productListOpens`, `commerce.checkouts`, `commerce.productListAdds`, `commerce.productListRemovals`, `commerce.productListViews`, `_experience.analytics.event101to200.*`, ... `_experience.analytics.event901_1000.*` | string | Standaard handel en douanegebeurtenissen teweeggebracht op de slag. |
| `page_event` | `web.webInteraction.type` | string | Het type hit dat wordt verzonden in de afbeeldingsaanvraag (klik op Standaard, Koppeling downloaden, Koppeling afsluiten of Aangepaste koppeling). |
| `page_event` | `web.webInteraction.linkClicks.value` | getal | Het type hit dat wordt verzonden in de afbeeldingsaanvraag (klik op Standaard, Koppeling downloaden, Koppeling afsluiten of Aangepaste koppeling). |
| `page_event_var_1` | `web.webInteraction.URL` | string | Een variabele die alleen wordt gebruikt in aanvragen voor het bijhouden van koppelingen. Deze variabele bevat de URL van de downloadkoppeling, de afsluitkoppeling of de aangepaste koppeling waarop is geklikt. |
| `page_event_var_2` | `web.webInteraction.name` | string | Een variabele die alleen wordt gebruikt in aanvragen voor het bijhouden van koppelingen. Hier wordt de aangepaste naam van de koppeling weergegeven, als deze is opgegeven. |
| `paid_search` | `search.isPaid` | boolean | Een vlag die wordt geplaatst als de treffer betaalde onderzoeksopsporing aanpast. |
| `ref_type` | `web.webReferrertype` | string | Een numerieke id die het verwijzingstype voor de treffer vertegenwoordigt. |

#### Kolommen na

Adobe Analytics Data Feeds gebruikt het concept kolommen met een `post_` prefix, die kolommen zijn die gegevens bevatten na verwerking. Zie [Veelgestelde vragen over gegevensfeeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/df-faq.html?lang=en#post) voor meer informatie .

De gegevens die in datasets door het Netwerk van de Rand van het Experience Platform worden verzameld (Web SDK, Mobiele SDK, Server API) hebben geen concept `post_` velden. Dientengevolge, `post_` vooraf en *non*-`post_` vooraf ingestelde kolommen voor gegevensinvoer worden toegewezen aan dezelfde XDM-velden. Bijvoorbeeld beide `page_url` en `post_page_url` gegevensvoederkolommen worden toegewezen aan hetzelfde `web.webPageDetails.URL` XDM-veld.

Zie [Gegevensverwerking in Adobe Analytics en Customer Journey Analytics vergelijken](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/data-processing-comparisons.html?lang=en) voor een overzicht van het verschil in gegevensverwerking.

De `post_` het type van prefixkolom van gegevens, wanneer verzameld in het de gegevensmeertje van het Experience Platform, vereist echter geavanceerde transformaties alvorens het met succes in een het inputgebruik van gegevens kan worden gebruikt. Het uitvoeren van deze geavanceerde transformaties in uw vragen impliceert het gebruik van [Adobe-gedefinieerde functies](https://experienceleague.adobe.com/docs/experience-platform/query/sql/adobe-defined-functions.html?lang=en) voor sessionisatie, attributie en deduplicatie. Zie [Voorbeelden](#examples) over het gebruik van deze functies.

#### Zoeken

Om gegevens van andere datasets op te zoeken, gebruikt u standaard SQL functionaliteit (`WHERE` clausule, `INNER JOIN`, `OUTER JOIN`, en andere).

#### Berekeningen

Gebruik de standaard SQL-functies (bijvoorbeeld `COUNT(*)`) of de [wiskunde en statistische diensten](https://experienceleague.adobe.com/docs/experience-platform/query/sql/spark-sql-functions.html?lang=en#math) onderdeel van Spark SQL. Ook, [vensterfuncties](https://experienceleague.adobe.com/docs/experience-platform/query/sql/adobe-defined-functions.html?lang=en#window-functions) bieden ondersteuning voor het bijwerken van aggregaties en het retourneren van afzonderlijke items voor elke rij in een geordende subset. Zie [Voorbeelden](#examples) over het gebruik van deze functies.

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

U kunt de [`explode()` of andere Arrays](https://experienceleague.adobe.com/docs/experience-platform/query/sql/spark-sql-functions.html?lang=en#arrays) van SQL van de Vonk om aan de gegevens binnen een genestelde gegevensstructuur, bijvoorbeeld te krijgen:

```sql
select explode(identityMap) from demosys_cja_ee_v1_website_global_v1_1 limit 15;
```

U kunt ook naar afzonderlijke elementen verwijzen met puntnotatie. Bijvoorbeeld:

```sql
select identityMap.ecid from demosys_cja_ee_v1_website_global_v1_1 limit 15;
```

Zie [Werken met geneste gegevensstructuren in Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/key-concepts/nested-data-structures.html?lang=en) voor meer informatie .


#### Voorbeelden

Voor vragen die gegevens van datasets in het de gegevensmeer van het Experience Platform gebruiken, op de extra mogelijkheden van Adobe bepaalde Functies en/of SQL van de Vonk tikken, en die gelijkaardige resultaten aan een gelijkwaardige gegevenstoevoer van Adobe Analytics zouden leveren, zie

* [verlaten browsers](https://experienceleague.adobe.com/docs/experience-platform/query/use-cases/abandoned-browse.html?lang=en)
* [toewijzingsanalyse](https://experienceleague.adobe.com/docs/experience-platform/query/use-cases/attribution-analysis.html?lang=en)
* [bot filteren](https://experienceleague.adobe.com/docs/experience-platform/query/use-cases/bot-filtering.html?lang=en)
* en andere voorbeelden gebruiken gevallen in de gids van de Dienst van de Vraag.


### Zoekopdracht plannen

U plant de vraag om ervoor te zorgen dat de vraag wordt uitgevoerd en dat de resultaten bij uw aangewezen interval worden geproduceerd.

#### Query-editor gebruiken

U kunt een vraag plannen gebruikend de Redacteur van de Vraag. Wanneer het plannen van de vraag, bepaalt u een outputdataset. Zie [Zoekprogramma&#39;s](https://experienceleague.adobe.com/docs/experience-platform/query/ui/query-schedules.html?lang=en) voor meer informatie .


#### API voor Query Service gebruiken

Alternatief kunt u RESTful APIs gebruiken om een vraag en een programma voor de vraag te bepalen. Zie [API-handleiding voor query-service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=en) voor meer informatie .
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

Om datasets uit te voeren, zorg ervoor u hebt [vereiste machtigingen](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#permissions). Verifieer ook dat de bestemming waarnaar u uw outputdataset wilt verzenden het uitvoeren van datasets steunt. U moet [verzamel de waarden voor vereiste en optionele kopteksten](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#gather-values-headers) die u gebruikt in de API-aanroepen. U moet ook [identificeer de verbindingsspecificaties en stroom specificeer IDs van de bestemming](https://experienceleague.adobe.com/docs/experience-platform/destinations/api/export-datasets.html#gather-connection-spec-flow-spec) u bent van plan datasets naar uit te voeren.

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
