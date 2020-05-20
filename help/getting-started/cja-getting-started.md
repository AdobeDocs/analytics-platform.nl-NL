---
title: Aan de slag met de analyse van de reis van de klant
description: De Analyse van de Reis van de klant Begonnen.
translation-type: tm+mt
source-git-commit: e30bbae59e11bbf93668ffe072508727f6efdd51
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---


# Aan de slag met de analyse van de reis van de klant

Om de Analyse van de Reis van de Klant uit te voeren, moet u deze werkschema volgen. Sommige initiële taken worden uitgevoerd in het Adobe Experience Platform en andere in de Analyse voor reizen van klanten.

## Vereisten

Klantreisanalyse is beschikbaar voor klanten die

* Zijn Adobe Analytics [Select-, Premier- of Ultimate](https://www.adobe.com/analytics/compare-adobe-analytics-packages.html) -klanten, en
* zijn ingericht voor het [Adobe Experience Platform](https://www.adobe.com/experience-platform.html), en
* De SKU voor de analyse van de reis van de klant hebben aangeschaft

## Workflow

| Taak | Details |
|---|---|---|
| **Stap 1: Uw gegevens ophalen in het Adobe Experience Platform** | Deze stap, uitgevoerd in het Adobe Experience Platform, bestaat uit verschillende substappen:<br>**Stap 1a: Gegevensschema **voorbereiden: Met[Adobe Experience Data Model (XDM)](https://www.adobe.io/apis/experienceplatform/home/xdm.html)kunt u gegevens voor klantervaring standaardiseren en schema&#39;s[voor het beheer van klantervaring](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/schema_editor_tutorial/schema_editor_tutorial.md)definiëren.<br>**Stap 1b: Creeer een dataset die op het schema** wordt gebaseerd: De gegevens in Platform bestaan uit gegevensreeksen, zoals e-mailgegevensreeksen, de datasets van CRM, POS gegevensreeksen, de dataset van de Analyse van Adobe, enz.. Elke gegevensset bestaat uit een schema en gegevensbatches. U kunt een gegevensset maken [in Experience Platform](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/creating_a_dataset_tutorial/creating_a_dataset_tutorial.md).<br>**Stap 1c: Gegevens verzamelen in Experience Platform **: Gebruik de kant-en-klare Adobe Analytics Platform Connector om traditionele Adobe Analytics-gegevens over te brengen naar Platform. U kunt één bronverbinding per rapportreeks tot stand brengen. Zie[Een bronverbinding maken met Adobe Analytics](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/sources_tutorial/adobe-analytics-ui-tutorial.md)in de documentatie van het Adobe Experience Platform. Zodra de verbinding wordt gecreeerd, wordt een doelschema en een dataset automatisch gecreeerd om de inkomende gegevens te bevatten. Bovendien vindt de terugvulling van gegevens plaats en neemt deze tot 13 maanden aan historische gegevens in. Wanneer de eerste opname is voltooid, kunt u doorgaan`Step 2`om een verbinding tot stand te brengen tussen deze dataset Analytics en de Analytics van de Reis van de Klant.<br>Of u kunt andere gegevenstypen innemen via[Batch-inname](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/ingest_architectural_overview/ingest_architectural_overview.md),[Streaming inname](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/streaming_ingest/streaming_ingest_overview.md)of via[andere bronconnectors](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/acp_connectors_overview/acp-connectors-overview.md). |
| **Stap 2: Verbindingen tot stand brengen tussen platformdatasets en de Analyse van de Reis van de Klant** | Met een verbinding kunt u gegevenssets van het Adobe Experience Platform integreren in Workspace. Om over de datasets van het Platform van de Ervaring te rapporteren, moet u eerst een verband tussen datasets in het Platform van de Ervaring en Werkruimte vestigen.<br>Zie Verbinding [maken](/help/connections/create-connection.md). |
| **Stap 3: Gegevensweergaven maken** | Een gegevensweergave is een gefilterde weergave van de gegevens. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, de toewijzing enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen.<br>Zie [Een gegevensweergave](/help/data-views/create-dataview.md)maken. |
| **Stap 4: Rapport over uw kanaalgegevens in Workspace** | Nadat u verbindingen en gegevensmeningen hebt gecreeerd, analyseer de gegevens u binnen gebruikend de macht en de flexibiliteit van de Werkruimte van de Analyse hebt gebracht.<br>Zie [Basisanalyse](/help/projects/perform-basic-analysis.md) uitvoeren en [Geavanceerde analyse](/help/projects/perform-adv-analysis.md)uitvoeren. |
