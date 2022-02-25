---
title: Aan de slag met Customer Journey Analytics
description: Begrijp de eerste vereisten en het werkschema die worden vereist om Customer Journey Analytics uit te voeren.
exl-id: cab218c0-009c-4669-9dfb-f8872a7f066b
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: 04ceeb9e9a048a224ea957ad42bc54cbd4b3f249
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 1%

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
| --- | --- |
| **Stap 1: Uw gegevens ophalen in Adobe Experience Platform** | Deze stap, uitgevoerd in Adobe Experience Platform, omvat verschillende substappen:<ul><li>**Stap 1a: Gegevensschema voorbereiden**: Gebruiken [Adobe Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) om de gegevens van de klantervaring te standaardiseren en [schema&#39;s definiëren](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=en) voor het beheer van de gebruikerservaring.</li><li>**Stap 1b: Creeer een dataset die op het schema wordt gebaseerd**: Gegevens in Platform bestaan uit gegevenssets, zoals e-mailgegevenssets, CRM-gegevenssets, POS-gegevenssets, de Adobe Analytics-gegevensset, enz. Elke gegevensset bestaat uit een schema en gegevensbatches. U kunt [een gegevensset maken in Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/create-datasets.html%3Flang%3Dnl).</li><li>**Stap 1c: Gegevens in Experience Platform opnemen**: Gebruik de uit-van-de-doos Verbinding van het Platform van Adobe Analytics om traditionele gegevens van Adobe Analytics in Platform te brengen. U kunt één bronverbinding per rapportreeks tot stand brengen. Zie [Een bronverbinding maken met Adobe Analytics](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en) in de documentatie van Adobe Experience Platform. Zodra de verbinding wordt gecreeerd, wordt een doelschema en een dataset automatisch gecreeerd om de inkomende gegevens te bevatten. Bovendien vindt de terugvulling van gegevens plaats en neemt deze tot 13 maanden aan historische gegevens in. Wanneer de eerste inname is voltooid, kunt u doorgaan met `Step 2` om een verbinding tussen deze dataset van Analytics en Customer Journey Analytics tot stand te brengen. Of u kunt andere gegevenstypen invoeren via [Inname in batch](https://experienceleague.adobe.com/docs/experience-platform/ingestion/batch/overview.html?lang=en),[Streaming opname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=en), of via [andere bronconnectors](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=en).</li></ul> |
| **Stap 2: Verbindingen maken tussen platformgegevenssets en Customer Journey Analytics** | Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over de datasets van het Experience Platform te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en Werkruimte vestigen.<br>Zie [Verbinding maken](/help/connections/create-connection.md). |
| **Stap 3: Gegevensweergaven maken** | Een gegevensweergave is een gefilterde weergave van de gegevens. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, de toewijzing enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen.<br>Zie [Een gegevensweergave maken](/help/data-views/create-dataview.md). |
| **Stap 4: Rapport over uw kanaalgegevens in Workspace** | Nadat u verbindingen en gegevensmeningen hebt gecreeerd, analyseer de gegevens u binnen gebruikend de macht en de flexibiliteit van Analysis Workspace hebt gebracht.<br>Zie [Basisanalyse uitvoeren](/help/analysis-workspace/perform-basic-analysis.md) en [Geavanceerde analyse uitvoeren](/help/analysis-workspace/perform-adv-analysis.md). |
