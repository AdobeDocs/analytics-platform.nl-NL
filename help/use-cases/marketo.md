---
title: B2B-gegevens opnemen in AEP en rapporteren in CJA
description: Leer hoe u Marketo-gegevens kunt overbrengen naar CJA
solution: Customer Journey Analytics
feature: Use Cases
source-git-commit: e18de2563427941f8c227881b46f73c490be218d
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---


# Voeg Marketo B2B-gegevens toe aan AEP en rapporteer deze in CJA

U kunt de nieuwe Marketo B2B-datasets in Adobe Experience Platform (AEP) gebruiken om waardevolle analytische en rapporteringsoplossingen aan B2B-marketers te bieden. Dan rapport over deze datasets in Customer Journey Analytics (CJA.)

## Stap 1: Marketo-brongegevensvelden toewijzen aan hun XDM-doelen

Wijs de [Personen](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/marketo.html?lang=en#persons) en [Activiteiten](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/marketo.html?lang=en#activities) op hun respectieve XDM schema doelgebieden.

## Stap 2: Marketo-gegevens in AEP opnemen

Gebruik de [Marketo Engage-aansluiting](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo.html?lang=en) om B2B-gegevens van Marketo naar Experience Platform te brengen en deze gegevens up-to-date te houden met toepassingen die zijn aangesloten op het Platform.

## Stap 3: Een verbinding met deze gegevensset instellen in CJA

Om over de datasets van de Experience Platform te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en CJA vestigen. Meer informatie vindt u onder [Verbinding maken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en).

## Stap 4: Een of meer gegevensweergaven maken

A [gegevensweergave](/help/data-views/data-views.md) is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van een verbinding te interpreteren. Het specificeert alle afmetingen en metriek beschikbaar in Analysis Workspace - in dit geval, metriek en dimensies specifiek voor Marketo. Het specificeert ook welke kolommen die afmetingen en metriek hun gegevens van verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

## Stap 5: Rapport in Analysis Workspace

Eén gebruiksgeval dat u zou kunnen verkennen, is: Hoeveel webpagina&#39;s hebben we in april-juni 2020 bezocht door leads?

1. Openen [Analysewerkruimte](/help/analysis-workspace/home.md) en maak een nieuw project.

1. Een [filter](/help/components/filters/create-filters.md) voor webpaginaweergaven als volgt - Gebeurtenistype = web.webpagedetails.pageViews:

   ![](assets/marketo-filter.png)

1. Trek in de tabel Vrije vorm het filter dat u hebt gemaakt - Weergaven webpagina&#39;s en trek vervolgens het datumbereik Maand in. Dit geeft u Webpagina bezoeken door lood elke maand:

   ![](assets/marketo-freeform.png)

1. Of trek in de volgende afmetingen: Persoonssleutel of zakelijk e-mailadres. Dit geeft u de Webpagina bezoeken door elke lood:

   ![](assets/marketo-freeform2.png)
