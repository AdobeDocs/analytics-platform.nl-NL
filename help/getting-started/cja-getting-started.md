---
title: Aan de slag met Customer Journey Analytics
description: Aan de slag met Customer Journey Analytics.
translation-type: tm+mt
source-git-commit: 16bca45f2576d3feef8129d558fad6f236852cb9
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---


# Aan de slag met Customer Journey Analytics

Als u Customer Journey Analytics wilt implementeren, moet u deze workflow volgen. Sommige initiële taken worden uitgevoerd in Adobe Experience Platform, en andere in Customer Journey Analytics.

## Vereisten

Customer Journey Analytics is beschikbaar voor klanten die

* Zijn Adobe Analytics- [klanten die het programma selecteren, als eerste of laatste](https://www.adobe.com/analytics/compare-adobe-analytics-packages.html) klant, en
* zijn voorzien voor het [Adobe Experience Platform](https://www.adobe.com/experience-platform.html), en
* Customer Journey Analytics SKU hebben aangeschaft

## Workflow

| Taak | Details |
|---|---|
| **Stap 1: Uw gegevens in Adobe Experience Platform ophalen** | Deze stap, uitgevoerd in Adobe Experience Platform, omvat verscheidene substappen:<ul><li>**Stap 1a: Gegevensschema** voorbereiden: Met [Adobe Experience Data Model (XDM)](https://www.adobe.io/apis/experienceplatform/home/xdm.html) kunt u gegevens voor klantervaring standaardiseren en schema&#39;s [voor het beheer van klantervaring](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/schema_editor_tutorial/schema_editor_tutorial.md) definiëren.</li><li>**Stap 1b: Creeer een dataset die op het schema** wordt gebaseerd: Gegevens in Platform bestaan uit gegevenssets, zoals e-mailgegevenssets, CRM-gegevenssets, POS-gegevenssets, de Adobe Analytics-gegevensset, enz. Elke gegevensset bestaat uit een schema en gegevensbatches. U kunt een gegevensset maken [in het Experience Platform](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/creating_a_dataset_tutorial/creating_a_dataset_tutorial.md).</li><li>**Stap 1c: Gegevens opnemen in Experience Platform**: Gebruik de Adobe Analytics Platform Connector buiten de doos om traditionele gegevens van Adobe Analytics in Platform te brengen. U kunt één bronverbinding per rapportreeks tot stand brengen. Zie [Een bronverbinding maken met Adobe Analytics](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/sources_tutorial/adobe-analytics-ui-tutorial.md) in de documentatie bij het Adobe Experience Platform. Zodra de verbinding wordt gecreeerd, wordt een doelschema en een dataset automatisch gecreeerd om de inkomende gegevens te bevatten. Bovendien vindt de terugvulling van gegevens plaats en neemt deze tot 13 maanden aan historische gegevens in. Wanneer de eerste opname is voltooid, kunt u doorgaan `Step 2` om een verbinding te maken tussen deze Analytics-gegevensset en Customer Journey Analytics. Of u kunt andere gegevenstypen innemen via [Batch](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/ingest_architectural_overview/ingest_architectural_overview.md),[Streaming opname](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/streaming_ingest/streaming_ingest_overview.md)of via [andere Source Connectors](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/acp_connectors_overview/acp-connectors-overview.md).</li></ul> |
| **Stap 2: Verbindingen maken tussen platformgegevenssets en Customer Journey Analytics** | Met een verbinding kunt u gegevenssets van Adobe Experience Platform in Workspace integreren. Om over de datasets van het Experience Platform te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en Werkruimte vestigen.<br>Zie Verbinding [maken](/help/connections/create-connection.md). |
| **Stap 3: Gegevensweergaven maken** | Een gegevensweergave is een gefilterde weergave van de gegevens. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, de toewijzing enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen.<br>Zie [Een gegevensweergave](/help/data-views/create-dataview.md)maken. |
| **Stap 4: Rapport over uw kanaalgegevens in Workspace** | Nadat u verbindingen en gegevensmeningen hebt gecreeerd, analyseer de gegevens u binnen gebruikend de macht en de flexibiliteit van Analysis Workspace hebt gebracht.<br>Zie [Basisanalyse](/help/analysis-workspace/perform-basic-analysis.md) uitvoeren en [Geavanceerde analyse](/help/analysis-workspace/perform-adv-analysis.md)uitvoeren. |
