---
title: Aan de slag met Customer Journey Analytics
description: Begrijp de eerste vereisten en het werkschema die worden vereist om Customer Journey Analytics uit te voeren.
exl-id: cab218c0-009c-4669-9dfb-f8872a7f066b
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: 117e72c9edd031ac76121299a0cff51f89766271
workflow-type: tm+mt
source-wordcount: '383'
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
| **Stap 1: Als u van Adobe Analytics naar CJA migreert, moet u leren wat u moet doen.** | Zie [Adobe Analytics-rapportenpakket-gegevens gebruiken in Customer Journey Analytics](/help/getting-started/aa-vs-cja/aa-data-in-cja.md). |
| **Stap 2: Andere gegevens ophalen in Adobe Experience Platform** | Deze stap, uitgevoerd in Adobe Experience Platform, omvat verschillende substappen:<ul><li>**Stap 2a: Gegevensschema voorbereiden**: Gebruiken [Adobe Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) om de gegevens van de klantervaring te standaardiseren en [schema&#39;s definiëren](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html) voor het beheer van de gebruikerservaring.</li><li>**Stap 2b: Creeer een dataset die op het schema wordt gebaseerd**: Gegevens in Platform bestaan uit gegevenssets, zoals e-mailgegevenssets, CRM-gegevenssets, POS-gegevenssets, de Adobe Analytics-gegevensset, enz. Elke gegevensset bestaat uit een schema en gegevensbatches. U kunt [een gegevensset maken in Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/create-datasets.html).</li><li>**Stap 2c: Gegevens in Experience Platform opnemen**: Hier hebt u verschillende opties. De weergave van [Gebruiksgevallen voor gegevensinvoer](/help/use-cases/data-ingestion.md) voor meer informatie . |
| **Stap 3: Verbindingen maken tussen platformgegevenssets en Customer Journey Analytics** | Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over de datasets van het Experience Platform te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en Werkruimte vestigen.<br>Zie [Verbinding maken](/help/connections/create-connection.md). |
| **Stap 4: Gegevensweergaven maken** | Een gegevensweergave is een gefilterde weergave van de gegevens. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, de toewijzing enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen.<br>Zie [Een gegevensweergave maken](/help/data-views/create-dataview.md). |
| **Stap 5: Rapport over uw kanaalgegevens in Workspace** | Nadat u verbindingen en gegevensmeningen hebt gecreeerd, analyseer de gegevens u binnen gebruikend de macht en de flexibiliteit van Analysis Workspace hebt gebracht.<br>Zie [Basisanalyse uitvoeren](/help/analysis-workspace/perform-basic-analysis.md) en [Geavanceerde analyse uitvoeren](/help/analysis-workspace/perform-adv-analysis.md). |
