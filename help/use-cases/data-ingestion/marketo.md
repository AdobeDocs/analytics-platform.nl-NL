---
title: Rapport over Marketo Engage-gegevens
description: Meer informatie over Marketo Engage-gegevens in Customer Journey Analytics
solution: Customer Journey Analytics
feature: Use Cases
exl-id: ef8a2d08-848b-4072-b400-7b24955a085b
role: Admin
source-git-commit: 9f954709a3dde01b4e01581e34aece07fe0256b1
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Rapport over Marketo Engage-gegevens

U kunt de nieuwe Marketo Engage-datasets in Adobe Experience Platform (Adobe Experience Platform) gebruiken om waardevolle analytische en rapporteringsoplossingen aan B2B-marketers te bieden. Geef vervolgens verslag over deze gegevenssets in Adobe Customer Journey Analytics.

## Stap 1: Wijs Marketo-brongegevensvelden toe aan hun XDM-doelen

Wijs de [ Personen ](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/marketo.html#persons) en [ Activiteiten ](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/marketo.html#activities) voorwerpen aan hun respectieve XDM gebieden van het schemadoel in kaart.

## Stap 2: Marketo-gegevens in Adobe Experience Platform opnemen

Gebruik de [ schakelaar van Marketo Engage ](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo.html) om gegevens van Marketo aan Experience Platform te brengen en dit gegeven bijgewerkt te houden gebruikend Platform-verbonden toepassingen.

## Stap 3: Opstelling een verbinding aan deze dataset in Customer Journey Analytics

Om over de datasets van Experience Platform te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en Customer Journey Analytics vestigen. Zie voor meer informatie [ creeer of geef een verbinding ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) uit.

## Stap 4: Een of meer gegevensweergaven maken

A [ gegevensmening ](/help/data-views/data-views.md) is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van een verbinding te interpreteren. Het specificeert alle afmetingen en metriek beschikbaar in Analysis Workspace - in dit geval, metriek en dimensies specifiek voor Marketo. Het specificeert ook welke kolommen die afmetingen en metriek hun gegevens van verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

## Stap 5: Rapport in Analysis Workspace

Een gebruiksgeval dat u zou kunnen onderzoeken is: hoeveel webpagina-bezoeken door leads hebben we in april-juni 2020 gehad?

1. Open [ Analytics Workspace ](/help/analysis-workspace/home.md) en creeer een nieuw project.
Klanten met B2B/B2P CDP kunnen in Customer Journey Analytics een B2C-analyse uitvoeren. B2B-objecten zijn nog niet beschikbaar.

1. Creeer a [ segment ](/help/components/filters/create-filters.md) voor Web-pagina meningen als volgt - het Type van gebeurtenis = web.webpagedetails.pageViews:

   ![ het venster van de Definitie die Gebeurtenis en Type van Gebeurtenis tonen ](../assets/marketo-filter.png)

1. Trek in het segment u in de Freeform lijst - de Mening van de Web-pagina creeerde, dan trek in de de datumwaaier van de Maand. Dit geeft u Webpagina bezoeken door lood elke maand:

   ![ Vrije lijst die Gebeurtenissen door Maand toont.](../assets/marketo-freeform.png)

1. Of trek in de volgende afmetingen: Person sleutel of Werk-e-mailadres. Dit geeft u de Webpagina bezoeken door elke lood:

   ![ vrije lijst die Gebeurtenissen en workEmail.Address en de Kijken van de Web-pagina toont.](../assets/marketo-freeform2.png)
