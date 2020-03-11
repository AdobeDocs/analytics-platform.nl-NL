---
title: Aan de slag met de analyse van de reis van de klant
description: De Analyse van de Reis van de klant Begonnen.
translation-type: tm+mt
source-git-commit: fb2b5868db69bfff3345abcd69b0b70112fdcf3c

---


# Aan de slag met de analyse van de reis van de klant

Om de Analyse van de Reis van de Klant uit te voeren, moet u deze werkschema volgen. Sommige initiële taken worden uitgevoerd in het Adobe Experience Platform en andere in de Analyse voor reizen van klanten.

| Taak | Waar uitgevoerd | Details |
|---|---|---|
| **Stap 1: Uw gegevens ophalen in het Adobe Experience Platform** | Adobe Experience Platform | Er zijn verschillende manieren om gegevens in te voeren voor zowel streaming- als batchgebruik, waaronder API&#39;s en een grafische interface voor het uploaden van gegevens. Experience Platform kan gegevens ophalen uit bijvoorbeeld:<ul><li>S3-opslag</li><li>Azure Blob Storage</li><li>Kafka Streams</li><li>SFTP-overdrachten</li><li>CSV-bestanden uploaden</li><li>JSON-bestanden uploaden</li></ul> |
| **Stap 2: Gegevensschema voorbereiden** | Adobe Experience Platform | Met [Adobe Experience Data Model (XDM)](https://www.adobe.io/apis/experienceplatform/home/xdm.html) kunt u gegevens voor klantervaring standaardiseren en schema&#39;s definiëren voor het beheer van klantervaring. |
| **Stap 3: Creeer een dataset die op het schema wordt gebaseerd** | Adobe Experience Platform | De gegevens in Platform bestaan uit gegevensreeksen, zoals e-mailgegevensreeksen, de datasets van CRM, POS gegevensreeksen, de dataset van de Analyse van Adobe, enz.. Elke gegevensset bestaat uit een schema en gegevensbatches. U kunt een gegevensset maken [in Experience Platform](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/creating_a_dataset_tutorial/creating_a_dataset_tutorial.md).<br>Hoewel het schema voor datasets die in de Analyse van de Reis van de Klant kunnen worden ingevoerd flexibel is, moet het met sommige basisregels in overeenstemming zijn. U kunt het beste controleren of uw gegevens aan deze vereisten voldoen voordat u ze uploadt naar Platform. (Schema bevat zowel metriek als afmetingen.)<br>Er zijn drie soorten gegevens die compatibel zijn met de Analyse van de Reis van de Klant:<ul><li>**Gebeurtenisgegevens**: Gegevens die gebeurtenissen in de tijd vertegenwoordigen (bv. webbezoeken, interacties, transacties, POS-gegevens, enquêtegegevens, gegevens van de indruk enz.). Dit zijn typisch klikstroomgegevens, met een klant identiteitskaart of een koekjesidentiteitskaart, en een timestamp. Met gebeurtenisgegevens kunt u de gewenste id gebruiken.</li><li>**Gegevens** opzoeken: Deze gegevens worden gebruikt voor het opzoeken van waarden of toetsen in de gebeurtenis- of profielgegevens. U kunt bijvoorbeeld opzoekgegevens uploaden waarmee numerieke id&#39;s in uw gebeurtenisgegevens worden toegewezen aan productnamen.</li><li>**Profielgegevens**: Gegevens die worden toegepast op uw bezoekers, gebruikers of klanten in de gebeurtenisgegevens. Bijvoorbeeld, staat u toe om de gegevens van CRM over uw klanten te uploaden.</li></ul> |
| **Stap 4:Verbindingen maken tussen platformdatasets en de Analyse van de Reis van de Klant** | Klantreisanalyse | Zie Verbinding [maken](/help/connections/create-connection.md). |
| **Stap 5: Gegevensweergaven maken** | Klantreisanalyse | Zie [Een gegevensweergave](/help/data-views/create-dataview.md)maken. |
| **Stap 6: Rapport over uw kanaalgegevens in Workspace** | Klantreisanalyse | Zie [Basisanalyse](/help/projects/perform-basic-analysis.md) uitvoeren en [Geavanceerde analyse](/help/projects/perform-adv-analysis.md)uitvoeren. |

## Vereisten

Klantreisanalyse is beschikbaar voor klanten die

* Zijn Adobe Analytics [Select-, Premier- of Ultimate](https://www.adobe.com/analytics/compare-adobe-analytics-packages.html) -klanten, en
* zijn ingericht voor het [Adobe Experience Platform](https://www.adobe.com/experience-platform.html), en
* De SKU voor de analyse van de reis van de klant hebben aangeschaft

## Gegevensschema voorbereiden

[Een schema maken met de Schema-editor](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/schema_editor_tutorial/schema_editor_tutorial.md)

## Stap 1: Uw gegevens ophalen in het Adobe Experience Platform

Voordat u gegevens van het Experience Platform kunt gebruiken in CJA, moet u die gegevens opnemen in Platform. Er zijn verschillende manieren om dit te doen:

* Gebruik de Adobe Analytics Platform Connector als u bestaande Adobe Analytics-gegevens wilt opnemen.
* Voor het invoeren van andere gegevens gebruikt u indelingen zoals: S3-opslag, Azure Blob-opslag, Kafka-streams, SFTP-overdrachten, CSV-bestandsuploads, JSON-bestandsuploads

### Stap 1a: Breng uw bestaande analysegegevens naar het Adobe Experience Platform

Gebruik de kant-en-klare Adobe Analytics Platform Connector om traditionele Adobe Analytics-gegevens over te brengen naar Platform. U kunt één bronverbinding per rapportreeks tot stand brengen. Zie [Een bronverbinding maken met Adobe Analytics](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/sources_tutorial/adobe-analytics-ui-tutorial.md) in de documentatie van het Adobe Experience Platform.

Zodra de verbinding wordt gecreeerd, wordt een doelschema en een dataset automatisch gecreeerd om de inkomende gegevens te bevatten. Bovendien vindt de terugvulling van gegevens plaats en neemt deze tot 13 maanden aan historische gegevens in. Wanneer de eerste opname is voltooid, kunt u doorgaan `Step 4` om een verbinding tot stand te brengen tussen deze dataset Analytics en de Analytics van de Reis van de Klant.

### Stap 1b: Andere gegevenstypen samenvoegen

[Met Batchopname](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/ingest_architectural_overview/ingest_architectural_overview.md) kunt u gegevens als batchbestanden in Experience Platform opnemen. Batches zijn gegevenseenheden die bestaan uit een of meer bestanden die als één eenheid moeten worden ingevoerd. Als de batches eenmaal zijn opgenomen, bieden ze metagegevens die het aantal records beschrijven dat is opgenomen, evenals eventuele mislukte records en bijbehorende foutberichten. Handmatig geüploade gegevensbestanden, zoals platte CSV-bestanden (toegewezen aan XDM-schema&#39;s) en Parquet-dataframes, moeten met deze methode worden opgenomen.

[Met streaming opname](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/streaming_ingest/streaming_ingest_overview.md) kunt u gegevens van client- en server-side apparaten in real-time naar Experience Platform verzenden.

[Met andere bronconnectors](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/acp_connectors_overview/acp-connectors-overview.md) kunt u gegevens uit externe bronnen invoeren en kunt u inkomende gegevens structureren, labelen en verbeteren met behulp van de platformservices. U kunt gegevens invoeren uit verschillende bronnen, zoals Adobe-toepassingen (Adobe Analytics, Audience Manager, Experience Platform Launch, Target), opslag op basis van de cloud (Azure Blob, Amazon S3, FTP/SFTP, Google Cloud Storage), software van derden en uw CRM (Microsoft Dynamics 365, Salesforce).

## Stap 2: Gegevensschema voorbereiden

bnbnbnbn
