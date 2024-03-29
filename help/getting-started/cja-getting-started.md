---
title: Aan de slag met Customer Journey Analytics
description: Inzicht in de vereisten en workflow die vereist zijn om Customer Journey Analytics te implementeren.
exl-id: cab218c0-009c-4669-9dfb-f8872a7f066b
solution: Customer Journey Analytics
feature: Basics
role: User
source-git-commit: bfaf76fa5f225e9aa3153fc4ee10c5be8f3164e7
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 2%

---

# Aan de slag met Customer Journey Analytics

Voor het implementeren van Customer Journey Analytics moet u deze workflow volgen. Sommige initiële taken worden uitgevoerd in Adobe Experience Platform en andere in Customer Journey Analytics.

## Vereisten

Customer Journey Analytics is beschikbaar voor klanten die

* zijn ingericht voor [Adobe Experience Platform](https://www.adobe.com/experience-platform.html), en
* De Customer Journey Analytics SKU hebben aangeschaft

## Workflow

| Taak | Details |
| --- | --- |
| **Stap 1: Als u van Adobe Analytics aan Customer Journey Analytics migreert, migreer uw gegevens en repliceer uw projecten.** | Voor informatie over het migreren van gegevens van Adobe Analytics naar Customer Journey Analytics, zie: <ul><li>[Adobe Analytics-rapportsuite gebruiken in Customer Journey Analytics](/help/getting-started/aa-vs-cja/aa-data-in-cja.md)</li><li>[Gegevens van traditionele Adobe Analytics verzamelen en gebruiken](../data-ingestion/analytics.md)</li></ul><p>Voor informatie over het herhalen van uw projecten van Adobe Analytics in Customer Journey Analytics, evenals het in kaart brengen van projectcomponenten van een het rapportreeks van Adobe Analytics aan een de gegevensmening van de Customer Journey Analytics, zie:</p><ul><li>[Componenten en projecten migreren van Adobe Analytics naar Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration.html)</li></ul> |
| **Stap 2: Andere gegevens in Adobe Experience Platform ophalen** | Deze stap, uitgevoerd in Adobe Experience Platform, omvat verschillende substappen:<ul><li>**Stap 2a: Bereid uw gegevensschema voor**: Gebruik [Adobe Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) om de gegevens van de klantervaring te standaardiseren en [schema&#39;s definiëren](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html) voor het beheer van de gebruikerservaring.</li><li>**Stap 2b: Creeer een dataset die op het schema wordt gebaseerd**: De gegevens in Platform bestaan uit gegevenssets, zoals e-mailgegevenssets, CRM-gegevenssets, POS-gegevenssets, de Adobe Analytics-gegevensset, enz. Elke dataset bestaat uit een schema en partijen gegevens. U kunt [een dataset in Experience Platform creëren](https://experienceleague.adobe.com/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/create-datasets.html).</li><li>**Stap 2c: Gegevens opnemen in Experience Platform**: Hier hebt u verschillende opties.</li></ul> |
| **Stap 3: Creeer verbindingen tussen platformdatasets en Customer Journey Analytics** | Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over de datasets van het Experience Platform te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en Werkruimte vestigen.<br>Zie [Verbinding maken of bewerken](/help/connections/create-connection.md). |
| **Stap 4: Gegevensweergaven maken** | Een gegevensweergave is een gefilterde weergave van de gegevens. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, de toewijzing, enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen.<br>Zie [Een gegevensweergave maken](/help/data-views/create-dataview.md). |
| **Stap 5: Rapport over uw kanaalgegevens in Workspace** | Nadat u verbindingen en gegevensmeningen hebt gecreeerd, analyseer de gegevens u binnen gebruikend de macht en de flexibiliteit van Analysis Workspace hebt gebracht.<br>Zie [Basisanalyse uitvoeren](/help/analysis-workspace/perform-basic-analysis.md) en [Geavanceerde analyse uitvoeren](/help/analysis-workspace/perform-adv-analysis.md). |

## Hulplijnen voor snel starten

De [Gegevensinvoer](../data-ingestion/data-ingestion.md) bevat snelle handleidingen voor de bovenstaande workflow. Deze snelstarthulplijnen tonen hoe u gegevens uit verschillende bronnen (waaronder Adobe Analytics) in Adobe Experience Platform kunt invoeren en deze gegevens vervolgens in de Customer Journey Analytics kunt gebruiken.
