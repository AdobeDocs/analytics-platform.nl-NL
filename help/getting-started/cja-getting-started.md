---
title: Klantreisanalyse Aan de slag
description: Analyse van de reis van de klant aan de slag.
translation-type: tm+mt
source-git-commit: 16bca45f2576d3feef8129d558fad6f236852cb9
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---


# Klantreisanalyse Aan de slag

Om de analyse van de Reis van de Klant uit te voeren, moet u deze workflow volgen. Sommige aanvankelijke taken worden uitgevoerd in het Platform van de Ervaring van Adobe, en wat in de Analyse van de Reis van de Klant.

## Vereisten

Klantreisanalyse is beschikbaar voor klanten die

* Adobe Analytics zijn [Selecteer, begin, of Ultimate](https://www.adobe.com/analytics/compare-adobe-analytics-packages.html) klanten, en
* Voorziening voor de [Adobe Experience Platform](https://www.adobe.com/experience-platform.html)en
* De klant heeft de SKU voor de reisanalyse van de klant gekocht

## Werkstroom

| Taak | Details |
|---|---|
| **Stap 1: Krijg uw gegevens in het Platform van de Ervaring van Adobe** | Deze stap, die in het Platform van de Ervaring van Adobe wordt uitgevoerd, impliceert verscheidene substappen:<ul><li>**Stap 1a: Bereid uw gegevensschema voor**: Gebruik [Adobe Experience Data Model (XDM)](https://www.adobe.io/apis/experienceplatform/home/xdm.html) om de gegevens over de klantenervaring te standaardiseren en [schema&#39;s definiëren](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/schema_editor_tutorial/schema_editor_tutorial.md) voor het beheer van de klantenervaring.</li><li>**Stap 1b: Creeer een dataset die op het schema wordt gebaseerd**: De gegevens in Platform bestaan uit gegevensreeksen, zoals e-mailgegevensreeksen, de datasets van CRM, POS gegevensreeksen, de dataset van de Analyse van Adobe, enz. Elke gegevensreeksen bestaat uit een schema en partijen gegevens. U kunt een gegevensset maken [in Experience Platform](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/creating_a_dataset_tutorial/creating_a_dataset_tutorial.md).</li><li>**Stap 1c: Verzamel gegevens in het ervaringsplatform**: Gebruik de uit-van-de-doos Schakelaar van het Platform van de Analyse van Adobe om de traditionele gegevens van de Analyse van Adobe in Platform te brengen. U kunt één bronverbinding per rapportreeks tot stand brengen. Zie [Creeer een bronverbinding met de Analyse van Adobe](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/sources_tutorial/adobe-analytics-ui-tutorial.md) in de documentatie van het Platform van de Ervaring van Adobe. Zodra de verbinding wordt gecreeerd, worden een doelschema en een dataset automatisch gecreeerd om de inkomende gegevens te bevatten. Bovendien vindt gegevensback-vulling plaats en neemt het maximaal 13 maanden historische gegevens in. Wanneer de aanvankelijke opname voltooit, kunt u met te werk gaan `Step 2` om een verbinding tot stand te brengen tussen deze dataset van Analytics en de Analytics van de Reis van de Klant. Of, u kunt andere gegevenstypes via opnemen [Inname van de partij](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/ingest_architectural_overview/ingest_architectural_overview.md),[Streamingopname](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/streaming_ingest/streaming_ingest_overview.md)of via [andere Bronconnectors](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/acp_connectors_overview/acp-connectors-overview.md).</li></ul> |
| **Stap 2: Verbindingen maken tussen platformdatasets en klantreisanalyse** | Een verbinding laat u datasets van het Platform van de Ervaring van Adobe in Werkruimte integreren. om over de datasets van het Platform van de Ervaring te rapporteren, moet u eerst een verbinding tussen datasets in het Platform van de Ervaring en Werkruimte vestigen.<br>Zie [Een verbinding maken](/help/connections/create-connection.md). |
| **Stap 3: Gegevensweergaven maken** | Een gegevensmening is een &quot;gefilterde&quot;mening van de gegevens. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor een bezoekonderbreking, toewijzing, enz. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen.<br>Zie [Een gegevensweergave maken](/help/data-views/create-dataview.md). |
| **Stap 4: Rapport over uw dwars-kanaalgegevens in Werkruimte** | Nadat u verbindingen en gegevensmeningen hebt gecreeerd, analyseer de gegevens u binnen gebruikend de macht en de flexibiliteit van de Werkruimte van de Analyse hebt gebracht.<br>Zie [Basisanalyse uitvoeren](/help/analysis-workspace/perform-basic-analysis.md) en [Uitgebreide analyse uitvoeren](/help/analysis-workspace/perform-adv-analysis.md). |
