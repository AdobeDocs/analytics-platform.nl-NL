---
title: Gegevens van Marketo Engage in Adobe Experience Platform opnemen en in Customer Journey Analytics rapporteren
description: Leer hoe u gegevens van Marketo's Engage in de Customer Journey Analytics kunt plaatsen
solution: Customer Journey Analytics
feature: Use Cases
exl-id: ef8a2d08-848b-4072-b400-7b24955a085b
role: Admin
source-git-commit: bfaf76fa5f225e9aa3153fc4ee10c5be8f3164e7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Gegevens van Marketo Engage in Adobe Experience Platform opnemen en in Customer Journey Analytics rapporteren

U kunt de nieuw beschikbare datasets van het Marketo Engage in Adobe Experience Platform (Adobe Experience Platform) gebruiken om waardevolle analyses en rapporteringsoplossingen aan B2B marketers te verstrekken. Geef vervolgens verslag over deze gegevenssets in Adobe Customer Journey Analytics.

## Stap 1: Wijs Marketo-brongegevensvelden toe aan hun XDM-doelen

Wijs de [Personen](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/marketo.html?lang=en#persons) en [Activiteiten](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/marketo.html?lang=en#activities) objecten naar hun respectieve XDM schema doelgebieden.

## Stap 2: Marketo-gegevens in Adobe Experience Platform opnemen

Gebruik de [Marketo Engage-aansluiting](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo.html?lang=en) om gegevens van Marketo naar Experience Platform te brengen en deze gegevens up-to-date te houden gebruikend Platform-Verbonden toepassingen.

## Stap 3: Opstelling een verbinding aan deze dataset in Customer Journey Analytics

Om over de datasets van het Experience Platform te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en Customer Journey Analytics vestigen. Zie voor meer informatie [Verbinding maken of bewerken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en).

## Stap 4: Een of meer gegevensweergaven maken

A [gegevensweergave](/help/data-views/data-views.md) is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van een verbinding te interpreteren. Het specificeert alle afmetingen en metriek beschikbaar in Analysis Workspace - in dit geval, metriek en dimensies specifiek voor Marketo. Het specificeert ook welke kolommen die afmetingen en metriek hun gegevens van verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

## Stap 5: Rapport in Analysis Workspace

Een gebruiksgeval dat u zou kunnen onderzoeken is: hoeveel webpagina-bezoeken door leads hebben we in april-juni 2020 gehad?

1. Openen [Analysewerkruimte](/help/analysis-workspace/home.md) en maak een nieuw project.
Klanten met B2B/B2P CDP kunnen B2C-stijlanalyse in Customer Journey Analytics uitvoeren. B2B-objecten zijn nog niet beschikbaar.

1. Een [filter](/help/components/filters/create-filters.md) voor webpaginaweergaven als volgt - Gebeurtenistype = web.webpagedetails.pageViews:

   ![Het venster Definitie waarin het type gebeurtenis en gebeurtenis wordt weergegeven](../assets/marketo-filter.png)

1. Trek in de tabel Vrije vorm het filter dat u hebt gemaakt - Weergaven webpagina&#39;s en trek vervolgens het datumbereik Maand in. Dit geeft u Webpagina bezoeken door lood elke maand:

   ![Vrije-vormtabel met gebeurtenissen per maand.](../assets/marketo-freeform.png)

1. Of trek in de volgende afmetingen: Person sleutel of Werk-e-mailadres. Dit geeft u de Webpagina bezoeken door elke lood:

   ![Vrije-vormlijst die Gebeurtenissen en workEmail.Address en de Mening van de Web-pagina toont.](../assets/marketo-freeform2.png)
