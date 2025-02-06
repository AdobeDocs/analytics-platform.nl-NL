---
title: Adobe Analytics-functieondersteuning begrijpen bij upgraden naar Customer Journey Analytics
description: Meer informatie over Adobe Analytics-functieondersteuning bij upgrades naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: 8d14bb23283107402332106df36e8f7898ea5d30
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 1%

---

# Adobe Analytics-functieondersteuning begrijpen bij upgraden naar Customer Journey Analytics {#feature-support-upgrade}

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
>abstract="Een invoegtoepassing voor Adobe Analytics die gespecialiseerd is in het verzamelen van gegevens over media, zoals audio, video of gestreamde inhoud."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Gebruik de informatie op deze pagina wanneer het beantwoorden van vragen in de [ controlelijst van de Customer Journey Analytics verbetering ](https://gigazelle.github.io/cja-ttv/).

In de volgende lijst staan alleen die Adobe Analytics-functies die tijdens het upgradeproces naar Customer Journey Analytics in overweging moeten worden genomen. Voor een uitvoerige lijst die toont welke eigenschappen van Adobe Analytics volledig, gedeeltelijk gesteund, of niet gesteund in Customer Journey Analytics worden gesteund, zie {de eigenschapsteun van de Customer Journey Analytics 0} ](/help/getting-started/aa-vs-cja/cja-aa.md).[

Houd rekening met de volgende Adobe Analytics-functies die u wilt blijven gebruiken wanneer u een upgrade uitvoert naar Customer Journey Analytics:

| Adobe Analytics-functie | Overeenkomende functie in Customer Journey Analytics |
|---------|----------|
| [ Componenten en projecten van Adobe Analytics ](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/build-workspace-project/freeform-overview) | [ Migreer projecten en hun bijbehorende componenten aan Customer Journey Analytics ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration). |
| [ de kaartbedekking van de Activiteit en verbinding het volgen ](https://experienceleague.adobe.com/en/docs/analytics/analyze/activity-map/overview) | Nog niet beschikbaar |
| [ Gegevens van de Classificatie ](https://experienceleague.adobe.com/en/docs/analytics/components/classifications/c-classifications) | De datasets van de opzoekopdracht zijn de methode om gegevens in Customer Journey Analytics te classificeren.<p>[ creeer een raadplegingsdataset voor elke dimensie die classificatiegegevens bevat.](/help/getting-started/cja-upgrade/cja-upgrade-dataset-lookup.md)</p> |
| [ de Kanalen van de Marketing ](https://experienceleague.adobe.com/en/docs/analytics/components/marketing-channels/c-getting-started-mchannel) | Afgeleide velden worden gemaakt in een gegevensweergave. <p>[ creeer een marketing kanaal afgeleid gebied.](/help/getting-started/cja-upgrade/cja-upgrade-marketing-channel.md)</p> |
| [Gegevensfeeds](https://experienceleague.adobe.com/en/docs/analytics/export/analytics-data-feed/data-feed-overview) | De uitvoer van gegevens van de eerste generatie van datasets is beschikbaar door de [ Toegang API van de Gegevens van het Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html) en door [ Doelen van het Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html). Deze opties verstrekken gebeurtenis/rijniveau de uitvoer van alle gegevens die in het meer van Gegevens van het Experience Platform worden verzameld of worden opgenomen. Gegevenskolommen na verwerking zijn niet beschikbaar omdat postkolommen bij vraagtijd worden berekend. Exporteren van postkolommen is beschikbaar via rapportage. |
| [Data Warehouse](https://experienceleague.adobe.com/en/docs/analytics/export/data-warehouse/data-warehouse) | [ de Volledige Uitvoer van de Lijst van de Customer Journey Analytics ](/help/analysis-workspace/export/export-cloud.md) is de evolutie van de rapporten van de Data Warehouse in Adobe Analytics, met vele nieuwe, vaak-gevraagde eigenschappen die niet vandaag in Data Warehouse beschikbaar zijn. |
| [ het stromen gegevens van Media ](https://experienceleague.adobe.com/en/docs/media-analytics/using/media-overview) | Streaming-mediagegevens zijn beschikbaar via de bronaansluiting Analytics als onderdeel van het deelvenster Mediagelijktijdige viewers en het deelvenster Media Playback Time Spent in Workspace. |

