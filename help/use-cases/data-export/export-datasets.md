---
title: Gegevensbestanden voor exporteren Customer Journey Analytics
description: Beschrijft hoe te om de datasets van de Uitvoer aan file uw gegevens te gebruiken.
solution: Customer Journey Analytics
feature: Use Cases
role: Admin
source-git-commit: 19018e31bb2a46e88a27643fe10c388b40de243e
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 0%

---


# Gegevensbestanden exporteren

In dit artikel wordt beschreven hoe de [!DNL Customer Journey Analytics Export datasets] kan worden gebruikt om het volgende uit te voeren [Gebruiksscenario voor exporteren van gegevens](overview.md):

- Gegevensback-up

## Inleiding

Gegevens exporteren met [!DNL Experience Platform Export datasets] Hiermee kunt u gegevens uit de gegevensweergaven van uw Customer Journey Analytics exporteren naar elke bestemming voor cloudopslag.

![BI-extensie](../assets/export-datasets.svg)

## Meer informatie

U kunt ruwe datasets, van het gegevensmeer in Experience Platform, naar de bestemmingen van de wolkenopslag uitvoeren. Deze uitvoer is in de terminologie van de Doelen van de Experience Platform die als de uitvoerbestemmingen van de Dataset wordt bedoeld. Zie [Gegevenssets exporteren naar cloudopslagbestemmingen](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets) voor een overzicht.

De volgende bestemmingen voor cloudopslag worden ondersteund:

- [Azure Data Lake Storage Gen2](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2)
- [Gegevenslandingszone](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone)
- [Google Cloud Storage](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage)
- [Amazon S3](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#changelog)
- [Azure Blob](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob#changelog)
- [SFTP](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp#changelog)


### UI EXPERIENCE PLATFORM

U kunt de uitvoer van uw datasets uitvoeren en plannen door het Experience Platform UI. In dit gedeelte worden de desbetreffende stappen beschreven.

#### Doel selecteren

Wanneer u de bestemming van de cloudopslag hebt bepaald waarnaar u de dataset wilt exporteren, [selecteer het doel](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#select-destination). Als u nog geen bestemming voor uw voorkeurscloudopslag hebt geconfigureerd, moet u [een nieuwe doelverbinding maken](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/connect-destination).

Als deel van het vormen van een bestemming, kunt u bepalen:

- het bestandstype (JSON of Parquet);
- of het resulterende bestand al dan niet moet worden gecomprimeerd, en
- of een manifestbestand al dan niet moet worden opgenomen.


#### Gegevensset selecteren

Wanneer u het doel hebt geselecteerd, gaat u in de volgende **[!UICONTROL Select datasets]** stap u moet uw dataset van de lijst van datasets selecteren. Als u veelvoudige geplande vragen hebt gecreeerd, en u de datasets naar de zelfde bestemming van de wolkenopslag wilt verzenden, kunt u de overeenkomstige datasets selecteren. Zie [Uw gegevenssets selecteren](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#select-datasets) voor meer informatie .

#### Gegevensexport voor schema

Tot slot wilt u uw datasetuitvoer als deel van plannen **[!UICONTROL Scheduling]** stap. In die stap kunt u het programma bepalen en of de datasetuitvoer al dan niet incrementeel zou moeten zijn. Zie [Gegevensexport voor schema](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#scheduling) voor meer informatie .


#### Slotstappen

[Controleren](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#review) uw selectie, en wanneer correct, begin uw dataset aan de bestemming van de wolkenopslag te exporteren.

Eerst moet u [verifiëren](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#verify) een geslaagde gegevensexport. Bij het exporteren van gegevenssets maakt Experience Platform een of meerdere `.json` of `.parquet` bestanden op de opslaglocatie die in de bestemming is gedefinieerd. Nieuwe bestanden worden naar verwachting op uw opslaglocatie gedeponeerd volgens het exportschema dat u instelt. Experience Platform maakt een mapstructuur op de opslaglocatie die u hebt opgegeven als onderdeel van de geselecteerde bestemming, waar de geëxporteerde bestanden worden opgeslagen. Voor elke exporttijd wordt een nieuwe map gemaakt volgens het patroon: `folder-name-you-provided/datasetID/exportTime=YYYYMMDDHHMM`. De standaardbestandsnaam wordt willekeurig gegenereerd en zorgt ervoor dat geëxporteerde bestandsnamen uniek zijn.

### Flow Service-API

U kunt ook de export van gegevenssets exporteren en plannen met behulp van API&#39;s. De betrokken stappen worden beschreven in [De datasets van de uitvoer door de Dienst API van de Stroom te gebruiken](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets).

#### Aan de slag

Om datasets uit te voeren, zorg ervoor u hebt [vereiste machtigingen](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#permissions). Verifieer ook dat de bestemming waarnaar u uw dataset wilt verzenden het uitvoeren van datasets steunt. U moet [verzamel de waarden voor vereiste en optionele kopteksten](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#gather-values-headers) die u gebruikt in de API-aanroepen. U moet ook [identificeer de verbindingsspecificaties en stroom specificeer IDs van de bestemming](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#gather-connection-spec-flow-spec) u bent van plan datasets naar uit te voeren.

#### In aanmerking komende gegevenssets ophalen

U kunt [een lijst met in aanmerking komende gegevenssets ophalen](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#retrieve-list-of-available-datasets) voor de uitvoer en verifieer of uw dataset deel van die lijst uitmaakt gebruikend [`GET /connectionSpecs/{id}/configs`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Configurations/operation/getDatasets) API.


#### Bronverbinding maken

Vervolgens moet u [een bronverbinding maken](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#create-source-connection) voor de dataset, gebruikend zijn unieke identiteitskaart, die u naar de bestemming van de wolkenopslag wilt uitvoeren. U gebruikt de [`POST /sourceConnections`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Source-connections/operation/postSourceConnection) API.

#### Verifiëren voor bestemming (basisverbinding maken)

U moet nu [een basisverbinding maken](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#create-base-connection) om de gegevens te verifiëren en veilig op te slaan naar de bestemming van de cloudopslag met de [`POST /targetConection`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/postTargetConnection) API.


#### Exportparameters opgeven

Vervolgens moet u [een extra doelverbinding maken waarmee de exportparameters worden opgeslagen](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#create-target-connection) voor uw dataset die, opnieuw gebruikt [`POST /targetConection`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/postTargetConnection) API. Deze exportparameters zijn onder andere locatie, bestandsindeling, compressie en meer.

#### Gegevensstroom instellen

Tot slot [de gegevensstroom instellen](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#create-dataflow) om ervoor te zorgen dat uw gegevensset wordt geëxporteerd naar de bestemming voor cloudopslag met de [`POST /flows`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Dataflows/operation/postFlow) API. In deze stap kunt u het programma voor het exporteren definiëren met de opdracht `scheduleParams` parameter.

#### Gegevensstroom valideren

Naar [controleren succesvolle uitvoeringen van uw gegevensstroom](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/api/export-datasets#get-dataflow-runs), gebruikt u de [`GET /runs`](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Dataflow-runs/operation/getFlowRuns) API, die dataflow ID als vraagparameter specificeert. Deze gegevensstroom-id is een id die wordt geretourneerd wanneer u de gegevensstroom instelt.

[Verifiëren](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets#verify) een geslaagde gegevensexport. Bij het exporteren van gegevenssets maakt Experience Platform een of meerdere `.json` of `.parquet` bestanden op de opslaglocatie die in de bestemming is gedefinieerd. Nieuwe bestanden worden naar verwachting op uw opslaglocatie gedeponeerd volgens het exportschema dat u instelt. Experience Platform maakt een mapstructuur op de opslaglocatie die u hebt opgegeven als onderdeel van de geselecteerde bestemming, waar de geëxporteerde bestanden worden opgeslagen. Voor elke exporttijd wordt een nieuwe map gemaakt volgens het patroon: `folder-name-you-provided/datasetID/exportTime=YYYYMMDDHHMM`. De standaardbestandsnaam wordt willekeurig gegenereerd en zorgt ervoor dat geëxporteerde bestandsnamen uniek zijn.
