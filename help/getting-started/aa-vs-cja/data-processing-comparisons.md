---
title: Gegevensverwerking vergelijken in Adobe Analytics en CJA-rapportagefuncties
description: Begrijp de verschillen in gegevensverwerking voor de diverse rapportfuncties
exl-id: e3deedb2-0171-4fc2-9127-b9543603d4f0
source-git-commit: 80d0b95f3bc3d785d9ca7e4b50aa1bd8440373c2
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 5%

---

# Vergelijk gegevensverwerking in Adobe Analytics en Customer Journey Analytics.

<!--

You often need the ability to process data before it is useful for reporting. You can process that data at several stages in the journey that spans from collecting data to generating your report or visualization.

In Adobe Analytics most of that processing of data occurs immediately after collecting the data. Functionalties like VISTA Rules, Processing Rules, Marketing Channels Processing Rules are available to support this **collection-time processing**. 
The data is then stored and at report time you can apply additional processing. For example, break down dimensions, apply segmentation, or  select a different attribution model. This **report-time processing** happens on the fly. 

In Adobe Analytics, report-time processing commonly represents a smaller amount of processing  than what happens at collection-time.

![Adobe Analytics collection-time processing](../assets/aa-processing.png)

In contrast, Customer Journey Analytics (CJA) is designed to require minimal upfront collection-time processing before data being is organized and stored. The underlying architecture of CJA is more designed to work with the stored data at report-time and offers its powerful report-time processing functionality not only in  Workspace but also, even more importantly, through the definition of components in your Data Views. 

![CJA report-time processing](../assets/cja-processing.png)

-->


Kennis van de verschillen in gegevensverwerking voor de verschillende rapportfuncties kan nuttig zijn om te begrijpen welke meetgegevens beschikbaar zijn waar en waarom ze kunnen verschillen.

Bijvoorbeeld, aangezien &quot;bezoeken&quot;als metrisch in Adobe Analytics bij gegevensverwerkingstijd wordt bepaald, en &quot;zittingen&quot;als metrisch in CJA wordt berekend bij rapporttijd, kunnen de twee metriek verschillen gebaseerd op de regels die voor zittingsdefinitie binnen de CJA gegevensmening worden gebruikt.

Ook, noch bezoeken noch zittingen als metrisch zijn beschikbaar in datasets die door de Bron van Analytics Schakelaar worden gecreeerd en daarom zou u vereisen om de zitting in uw vraaglogica te bepalen om vergelijkingen te doen.

## Terminologie {#terms}

In de onderstaande tabel wordt de terminologie gedefinieerd voor de verschillende typen verwerkingslogica die op Adobe Analytics en CJA worden toegepast:

| Term | Definitie | Notities |
| --- | --- | --- |
| Verwerking van de verzameltijd | Logica die wordt uitgevoerd wanneer gegevens worden verzameld en verwerkt, voordat ze worden opgeslagen voor rapportage- en analysedoeleinden. | Deze logica is &quot;gebaseerd op&quot; historische gegevens en kan over het algemeen niet eenvoudig worden gewijzigd. |
| Verwerking bij rapporttijd | Logica die wordt uitgevoerd op het moment dat een rapport wordt uitgevoerd. | Deze logica kan op een niet-destructieve manier op toekomstige en historische gegevens bij rapportruntime worden toegepast. |
| Logica op bedrijfsniveau | Logica toegepast op rij-voor-rij niveau. | Voorbeelden: Verwerkingsregels, VISTA, bepaalde regels inzake marketingkanalen. |
| Logica op bezoekniveau | Logica toegepast op bezoekniveau. | Voorbeelden: Definitie van bezoek en sessie. |
| Logica op bezoekersniveau | Logica toegepast op bezoekersniveau. | Voorbeeld: Sstitching voor bezoekers over het hele apparaat of het kanaal. |
| Segmentlogica (filter) | Evaluatie van de regels voor het segment hit/visit/bezoeker (event/session/person) (filter). | Voorbeeld: Mensen die rode schoenen kochten. |
| Berekende standaarden | Evaluatie van door de klant gemaakte aangepaste maatstaven die kunnen worden gebaseerd op complexe formules, waaronder segmenten en filters. | Voorbeeld: Aantal mensen die rode schoenen kochten. |
| Attributielogica | Logische berekening van attributie. | Voorbeeld: eVar persistentie. |
| Componentinstellingen | Aanpassingen toepassen op metriek of dimensies, zoals kenmerk, gedrag, indeling en andere | Voorbeeld: waarde bucketing om numerieke waarden te combineren die op een waaier worden gebaseerd |
| Aangepaste velden | De logica is van toepassing op schema of standaardgebieden als deel van het bepalen van componenten in een mening van Gegevens. | Voorbeeld: het creëren van een nieuwe afmeting van het marketing kanaal |

{style="table-layout:auto"}

In de loop der tijd hebben Adobe Analytics en nu Customer Journey Analytics hun flexibiliteit verbeterd door het toestaan van bezoek en bezoekersniveau gegevenslogica om bij rapportruntime worden uitgevoerd.

## Typen gegevensverwerking {#types}

De gegevensverwerkingsstappen die worden uitgevoerd voor Adobe Analytics en CJA en de timing van deze stappen, variëren van functie tot functie Analytics. In de onderstaande tabel vindt u een overzicht van de typen gegevensverwerking voor elke functie Analytics en wanneer de gegevensverwerking wordt toegepast.

| Functie | Toegepast op verwerkingstijd | Toegepast op rapporttijd | Niet beschikbaar | Notities |
| --- | --- | --- | --- | --- |
| [Core AA](https://experienceleague.adobe.com/docs/analytics.html?lang=en) rapportage<br/>(exclusief Attribution IQ- of virtuele-rapportsuites met verwerking bij de rapporttijd) | <ul><li>[Verwerkingsregels](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html?lang=en)</li><li>[VISTA-regels](https://experienceleague.adobe.com/docs/analytics/technotes/terms.html?lang=en)</li><li>Niveau [regels voor marketingkanalen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/marketing-channels/c-rules.html?lang=en)</li><li>Regels voor marketingkanalen op bezoekniveau (zie opmerking)</li><li>Definitie van bezoek</li><li>Attributielogica</li></ul> | <ul><li>Segmentlogica</li><li>Berekende standaarden</li></ul> | <ul><li>Apparaatanalyse (zie opmerking)</li></ul> | <ul><li>CDA vereist gebruik van virtuele rapportsuites met de verwerking van de rapporttijd.</li><li>De &quot;regels voor marketingkanalen op bezoekniveau&quot; omvatten: **Is de eerste bezoekpagina**, **Laatste aanraakkanaal overschrijven**, en **Vervaldatum marketingkanaal**. (Zie [documentatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html?lang=en).)</li></ul> |
| Core AA [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html?lang=en) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Definitie van bezoek</li><li>Attributielogica</li></ul> | <ul><li>Segmentlogica</li></ul> | <ul><li>Berekende standaarden</li><li>Cross-device Analytics</li></ul> |  |
| Core AA [Gegevensfeeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html?lang=en) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Definitie van bezoek (bezoekerveld)</li><li>Attributielogica (in postkolommen)</li></ul> |  | <ul><li>Segmentlogica</li><li>Berekende standaarden</li><li>Cross-device Analytics</li></ul> | <ul><li>ID-toewijzingen voor bepaalde kolommen met betrekking tot marketingkanalen in gegevensfeeds worden niet opgenomen in gegevensfeeds. (Zie de [gegevensdoorvoerdocumentatie](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=en).)</li></ul> |
| Core AA [Livestream](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) | <ul><li> Verwerkingsregels</li><li>VISTA-regels</li><ul> |  | <ul><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Naar logica</li><li>Attributielogica</li><li>Segmentlogica</li><li>Berekende standaarden</li><li>Cross-device Analytics</li></ul> |  |
| Core AA [Attribution IQ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/overview.html?lang=en) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Definitie van bezoek (zie opmerking)</li><li>Apparaatanalyse (zie opmerking)</li></ul> | <ul><li>Regels voor marketingkanalen op hoog niveau (zie opmerking)</li><li>Regels voor marketingkanalen op bezoekniveau (zie opmerking) Attributielogica</li><li>Segmentlogica</li><li>Berekende standaarden</li></ul> |  | <ul><li>CDA vereist gebruik van virtuele rapportsuites met de verwerking van de rapporttijd.</li><li>Attribution IQ in Core Analytics maakt gebruik van marketingkanalen die volledig zijn afgeleid op het moment van het rapport (d.w.z. afgeleide mid-values).</li><li>Attribution IQ gebruikt een verwerking-tijd bezoekdefinitie behalve wanneer gebruikt in een rapport-tijd verwerking VRS.</li></ul> |
| Core AA virtuele rapportensuites met [rapporttijdverwerking](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html?lang=en) (VRS RTP) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>[Cross-device Analytics](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html?lang=en)</li></ul> | <ul><li>Definitie van bezoek</li><li>Attributielogica</li><li>Segmentlogica</li><li>Berekende standaarden</li><li>Andere VRS RTP-instellingen</li></ul> | <ul><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li></ul> | <ul><li>Zie VRS RTP [documentatie](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html?lang=en).</li></ul> |
| [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=en)gegevensset op basis van AEP-gegevens in het gegevensmeer | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Veldgebaseerde stitching (zie opmerking)</li></ul> |  | <ul><li>[Regels voor verkoopkanalen op bezoekniveau](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html?lang=en)</li><li>Naar logica</li><li>Attributielogica</li><li>Filterlogica</li></ul> | <ul><li>U moet uw eigen filterlogica en berekende meetgegevens toepassen</li><li>Op veld gebaseerde stitching leidt tot een afzonderlijke gestikte dataset naast die gecreeerd door de Bron van Analytics Schakelaar.</li></ul> |
| [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html?lang=en) rapportage | <ul><li>Geïmplementeerd als onderdeel van Adobe Experience Platform-gegevensverzameling</li></ul> | <ul><li>Sessiedefinitie</li><li>[Gegevens, weergave](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views.html?lang=en) instellingen<li>Attributielogica</li><li>Berekende standaarden</li><li>Filterlogica</li></ul> | <ul><li>Regels voor verkoopkanalen op bezoekniveau</li></ul> | <ul><li>Moet een gestikte gegevensset gebruiken om te profiteren van op het veld gebaseerde stitching.</li></ul> |

{style="table-layout:auto"}
