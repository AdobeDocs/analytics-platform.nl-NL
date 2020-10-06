---
title: Aan de slag met Customer Journey Analytics
description: Begrijp de eerste vereisten en het werkschema die worden vereist om Customer Journey Analytics uit te voeren.
translation-type: tm+mt
source-git-commit: 8067bb355934f8f6f1d54776f44abfd853aee231
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---


# Aan de slag met Customer Journey Analytics

Voor het implementeren van Customer Journey Analytics moet u deze workflow volgen. Sommige initiële taken worden uitgevoerd in Adobe Experience Platform en andere in Customer Journey Analytics.

## Vereisten

Customer Journey Analytics is beschikbaar voor klanten die

* Zijn Adobe Analytics [Select, Prime of Ultimate](https://www.adobe.com/analytics/compare-adobe-analytics-packages.html) klanten, en
* zijn ingericht voor de [Adobe Experience Platform](https://www.adobe.com/experience-platform.html), en
* De Customer Journey Analytics SKU hebben aangeschaft

## Workflow

| Taak | Details |
|---|---|
| **Stap 1: Uw gegevens ophalen in Adobe Experience Platform** | Deze stap, uitgevoerd in Adobe Experience Platform, omvat verschillende substappen:<ul><li>**Stap 1a: Gegevensschema voorbereiden**: Gebruiken [Adobe Experience Data Model (XDM)](https://www.adobe.io/apis/experienceplatform/home/xdm.html) om de gegevens van de klantervaring te standaardiseren en [schema&#39;s definiëren](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/schema_editor_tutorial/schema_editor_tutorial.md) voor het beheer van de gebruikerservaring.</li><li>**Stap 1b: Creeer een dataset die op het schema wordt gebaseerd**: Gegevens in Platform bestaan uit gegevenssets, zoals e-mailgegevenssets, CRM-gegevenssets, POS-gegevenssets, de Adobe Analytics-gegevensset, enz. Elke gegevensset bestaat uit een schema en gegevensbatches. U kunt een gegevensset maken [in Experience Platform](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/creating_a_dataset_tutorial/creating_a_dataset_tutorial.md).</li><li>**Stap 1c: Gegevens in Experience Platform opnemen**: Gebruik de uit-van-de-doos Verbinding van het Platform van Adobe Analytics om traditionele gegevens van Adobe Analytics in Platform te brengen. U kunt één bronverbinding per rapportreeks tot stand brengen. Zie [Een bronverbinding maken met Adobe Analytics](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/sources_tutorial/adobe-analytics-ui-tutorial.md) in de documentatie van Adobe Experience Platform. Zodra de verbinding wordt gecreeerd, wordt een doelschema en een dataset automatisch gecreeerd om de inkomende gegevens te bevatten. Bovendien vindt de terugvulling van gegevens plaats en neemt deze tot 13 maanden aan historische gegevens in. Wanneer de eerste inname is voltooid, kunt u doorgaan met `Step 2` om een verbinding tussen deze dataset van Analytics en Customer Journey Analytics tot stand te brengen. Of u kunt andere gegevenstypen invoeren via [Inname in batch](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/ingest_architectural_overview/ingest_architectural_overview.md),[Streaming opname](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/streaming_ingest/streaming_ingest_overview.md), of via [andere bronconnectors](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/acp_connectors_overview/acp-connectors-overview.md).</li></ul> |
| **Stap 2: Verbindingen maken tussen platformgegevenssets en Customer Journey Analytics** | Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over de datasets van het Experience Platform te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en Werkruimte vestigen.<br>Zie [Verbinding maken](/help/connections/create-connection.md). |
| **Stap 3: Gegevensweergaven maken** | Een gegevensweergave is een gefilterde weergave van de gegevens. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, de toewijzing enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen.<br>Zie [Een gegevensweergave maken](/help/data-views/create-dataview.md). |
| **Stap 4: Rapport over uw kanaalgegevens in Workspace** | Nadat u verbindingen en gegevensmeningen hebt gecreeerd, analyseer de gegevens u binnen gebruikend de macht en de flexibiliteit van Analysis Workspace hebt gebracht.<br>Zie [Basisanalyse uitvoeren](/help/analysis-workspace/perform-basic-analysis.md) en [Geavanceerde analyse uitvoeren](/help/analysis-workspace/perform-adv-analysis.md). |
