---
title: Adobe Analytics-functieondersteuning begrijpen bij upgrades naar Customer Journey Analytics
description: Meer informatie over Adobe Analytics-functieondersteuning bij upgrades naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 92053109-f80d-47ab-b011-c28a5411149c
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 1%

---

# Adobe Analytics-functieondersteuning begrijpen bij upgrades naar Customer Journey Analytics {#feature-support-upgrade}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-migrate-projects"
>title="Onderdelen en projecten"
>abstract="De componenten van Adobe Analytics omvatten: Projecten (met hun bijbehorende vrije vormlijsten en visualisaties), segmenten, en berekende metriek."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-activity-map"
>title="Bedekking activiteitenoverzicht en koppeling bijhouden"
>abstract="Een browserextensie waarmee u de gegevens voor het bijhouden van koppelingen kunt zien als een overlay op uw site."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-activity-map-support"
>title="Ondersteuning voor Activity Map-overlay is nog niet beschikbaar"
>abstract="Activity Map-overlayondersteuning is nog niet beschikbaar in Customer Journey Analytics. Het is de bedoeling dat het in de toekomst beschikbaar zal zijn."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-classification"
>title="Classificatiegegevens"
>abstract="Gegevens groeperen of categoriseren als afzonderlijke afmetingen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-marketing-channels"
>title="Marketingkanalen"
>abstract="Maak regels die indelen hoe klanten op uw site aankomen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-data-feeds"
>title="Gegevensfeeds"
>abstract="Exporteer onbewerkte gegevens uit Adobe Analytics voor gebruik in externe gereedschappen en processen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-data-warehouse"
>title="Data Warehouse"
>abstract="Verwerkte gegevens uit Adobe Analytics exporteren in spreadsheetindeling."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-streaming-media"
>title="Streaming mediagegevens"
>abstract="Een invoegtoepassing voor Adobe Analytics en Customer Journey Analytics die gespecialiseerd is in het verzamelen van gegevens over media, zoals audio, video of gestreamde inhoud."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-component-migration"
>title="Projecten en onderdelen migreren"
>abstract="Breng Adobe Analytics-projecten en de bijbehorende onderdelen naar Customer Journey Analytics."

<!-- markdownlint-enable MD034 -->

{{upgrade-note}}

In de volgende lijst staan alleen die Adobe Analytics-functies die tijdens het upgradeproces naar Customer Journey Analytics in overweging moeten worden genomen. Voor een uitvoerige lijst die toont welke eigenschappen van Adobe Analytics volledig, gedeeltelijk gesteund, of niet gesteund in Customer Journey Analytics worden gesteund, zie [ de eigenschapsteun van Customer Journey Analytics ](/help/getting-started/aa-vs-cja/cja-aa.md).

Houd rekening met de volgende Adobe Analytics-functies die u wilt blijven gebruiken wanneer u een upgrade uitvoert naar Customer Journey Analytics:

| Adobe Analytics-functie | Overeenkomende functie in Customer Journey Analytics |
|---------|----------|
| [ Componenten en projecten van Adobe Analytics ](https://experienceleague.adobe.com/nl/docs/analytics/analyze/analysis-workspace/build-workspace-project/freeform-overview) | [ Migreer projecten en hun bijbehorende componenten aan Customer Journey Analytics ](https://experienceleague.adobe.com/nl/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration). |
| [ de kaartbedekking van de Activiteit en verbinding het volgen ](https://experienceleague.adobe.com/nl/docs/analytics/analyze/activity-map/overview) | Nog niet beschikbaar |
| [ Gegevens van de Classificatie ](https://experienceleague.adobe.com/nl/docs/analytics/components/classifications/c-classifications) | Gegevenssets opzoeken zijn de methode voor het classificeren van gegevens in Customer Journey Analytics.<p>[ creeer een raadplegingsdataset voor elke dimensie die classificatiegegevens bevat.](/help/getting-started/cja-upgrade/cja-upgrade-dataset-lookup.md)</p> |
| [ de Kanalen van de Marketing ](https://experienceleague.adobe.com/nl/docs/analytics/components/marketing-channels/c-getting-started-mchannel) | Afgeleide velden worden gemaakt in een gegevensweergave. <p>[ creeer een marketing kanaal afgeleid gebied.](/help/getting-started/cja-upgrade/cja-upgrade-marketing-channel.md)</p> |
| [Gegevensfeeds](https://experienceleague.adobe.com/nl/docs/analytics/export/analytics-data-feed/data-feed-overview) | Experience Platform en Customer Journey Analytics bieden een aantal functies die onafhankelijk of gecombineerd de verschillende uitvoervereisten kunnen oplossen. Deze functies omvatten [ de Toegang API van Gegevens van Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=nl-NL), [ Doelen van Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=nl-NL), [ de Volledige Uitvoer van de Lijst van Customer Journey Analytics ](/help/analysis-workspace/export/export-cloud.md), en [ BI hulpmiddelintegratie ](/help/data-views/bi-extension.md).<p>Voor meer informatie over de uitvoeropties, zie [ de uitvoergebruiksgevallen van Gegevens ](/help/use-cases/data-export/overview.md).</p> |
| [Data Warehouse](https://experienceleague.adobe.com/nl/docs/analytics/export/data-warehouse/data-warehouse) | [ de Volledige Uitvoer van de Lijst van Customer Journey Analytics ](/help/analysis-workspace/export/export-cloud.md) is de evolutie van de rapporten van Data Warehouse in Adobe Analytics, met vele nieuwe, vaak-gevraagde eigenschappen die niet vandaag in Data Warehouse beschikbaar zijn. |
| [ het stromen gegevens van Media ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/media-overview) | Streaming-mediagegevens zijn beschikbaar via de bronaansluiting Analytics als onderdeel van het deelvenster Mediagelijktijdige viewers en het deelvenster Media Playback Time Spent in Workspace. |
