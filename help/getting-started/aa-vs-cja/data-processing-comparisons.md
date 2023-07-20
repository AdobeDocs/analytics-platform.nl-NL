---
title: Vergelijk gegevensverwerking in Adobe Analytics en Customer Journey Analytics-rapportagefuncties
description: Begrijp de verschillen in gegevensverwerking voor de diverse rapportfuncties
exl-id: e3deedb2-0171-4fc2-9127-b9543603d4f0
feature: Basics
source-git-commit: a49ef8b35b9d5464df2c5409339b33eacb90cd9c
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 4%

---

# Vergelijk gegevensverwerking in Adobe Analytics en Customer Journey Analytics.

U hebt vaak de mogelijkheid nodig om gegevens te verwerken voordat deze nuttig zijn voor rapportage. U kunt die gegevens in verscheidene stadia in de reis verwerken die zich van het verzamelen van gegevens aan het produceren van uw rapport of visualisatie uitstrekken.

In Adobe Analytics vindt de verwerking van gegevens grotendeels direct plaats nadat de gegevens zijn verzameld. De functies zoals de Regels van VISTA, de Regels van de Verwerking, de Verwerkingsregels van de Kanalen van de Marketing zijn beschikbaar om dit te steunen **verwerking van verzameltijd**.
De gegevens worden dan opgeslagen en op rapporttijd kunt u extra verwerking toepassen. U kunt bijvoorbeeld de afmetingen splitsen, segmentatie toepassen of een ander attributiemodel selecteren. Dit **verwerking van rapporttijd** gebeurt ter plekke.

In Adobe Analytics, rapport-tijd vertegenwoordigt de verwerking gewoonlijk een kleinere hoeveelheid verwerking dan wat bij inzameling-tijd gebeurt.

![Adobe Analytics-verwerking van verzameltijd](../assets/aa-processing.png)

Customer Journey Analytics is daarentegen ontworpen om minimale verwerkingstijd vooraf te vereisen voordat gegevens worden geordend en opgeslagen. De onderliggende architectuur van Customer Journey Analytics wordt ontworpen om met de opgeslagen gegevens in rapport-tijd te werken en biedt zijn krachtige rapport-tijd verwerkingsfunctionaliteit niet alleen in Werkruimte maar ook, nog belangrijker, door de definitie van [componenten](/help/data-views/component-settings/overview.md) en [afgeleide velden](/help/data-views/derived-fields/derived-fields.md) in uw gegevensweergaven.

![Customer Journey Analytics rapport-tijd verwerking](../assets/cja-processing.png)

Kennis van de verschillen in gegevensverwerking voor de verschillende rapportfuncties kan nuttig zijn om te begrijpen welke meetgegevens beschikbaar zijn waar en waarom ze kunnen verschillen.

Bijvoorbeeld, aangezien &quot;bezoeken&quot;als metrisch in Adobe Analytics bij gegevensverwerkingstijd worden bepaald, en &quot;zittingen&quot;als metrisch in Customer Journey Analytics bij rapporttijd wordt berekend, kunnen de twee metriek verschillen gebaseerd op de regels die voor zittingsdefinitie binnen de de gegevensmening van Customer Journey Analytics worden gebruikt.

Ook, noch bezoeken noch zittingen als metrisch zijn beschikbaar in datasets die door de bron van Analytics schakelaar worden gecreeerd en daarom zou u vereisen om de zitting in uw vraaglogica te bepalen om vergelijkingen te doen.

## Terminologie {#terms}

In de onderstaande tabel wordt de terminologie gedefinieerd voor de verschillende typen verwerkingslogica die worden toegepast op Adobe Analytics en Customer Journey Analytics:

| Term | Definitie | Notities |
| --- | --- | --- |
| Verwerking van de verzameltijd | Logica die wordt uitgevoerd wanneer gegevens worden verzameld en verwerkt, voordat ze worden opgeslagen voor rapportage- en analysedoeleinden. | Deze logica is &quot;gebaseerd op&quot; historische gegevens en kan over het algemeen niet eenvoudig worden gewijzigd. |
| Verwerking bij rapporttijd | Logica die wordt uitgevoerd op het moment dat een rapport wordt uitgevoerd. | Deze logica kan op een niet-destructieve manier op toekomstige en historische gegevens bij rapportruntime worden toegepast. |
| Logica op bedrijfsniveau | Logica toegepast op rij-voor-rij niveau. | Voorbeelden: Verwerkingsregels, VISTA, bepaalde regels inzake marketingkanalen. |
| Logica op bezoekniveau | Logica toegepast op bezoekniveau. | Voorbeelden: Definitie van bezoek en sessie. |
| Logica op bezoekersniveau | Logica toegepast op persoonniveau. | Voorbeeld: Persoonlijke stitching tussen apparaten en kanalen. |
| Segmentlogica (filter) | Evaluatie van de regels voor het segment gebeurtenis/bezoek/persoon (gebeurtenis/sessie/persoon) (filter). | Voorbeeld: Mensen die rode schoenen kochten. |
| Berekende standaarden | Evaluatie van door de klant gemaakte aangepaste maatstaven die kunnen worden gebaseerd op complexe formules, waaronder segmenten en filters. | Voorbeeld: Aantal mensen die rode schoenen kochten. |
| Attributielogica | Logische berekening van attributie. | Voorbeeld: eVar persistentie. |
| Componentinstellingen | Aanpassingen toepassen op metriek of dimensies, zoals kenmerk, gedrag, indeling en andere | Voorbeeld: waarde bucketing om numerieke waarden te combineren die op een waaier worden gebaseerd |
| Afgeleide velden | De logica is van toepassing op schema of standaardgebieden als deel van het bepalen van componenten in een mening van Gegevens. | Voorbeeld: het creëren van een nieuwe afmeting van het marketing kanaal |

{style="table-layout:auto"}

In de loop der tijd hebben Adobe Analytics en nu Customer Journey Analytics hun flexibiliteit verbeterd door het toestaan van bezoek en persoon-vlakke gegevenslogica om bij rapportruntime worden uitgevoerd.

## Typen gegevensverwerking {#types}

De gegevensverwerkingsstappen die worden uitgevoerd voor Adobe Analytics en Customer Journey Analytics en de timing van deze stappen verschillen van functie tot functie Analytics. In de onderstaande tabel vindt u een overzicht van de typen gegevensverwerking voor elke functie Analytics en wanneer de gegevensverwerking wordt toegepast.

| Functie | Toegepast op verwerkingstijd | Toegepast op rapporttijd | Niet beschikbaar | Notities |
| --- | --- | --- | --- | --- |
| [Adobe Analytics](https://experienceleague.adobe.com/docs/analytics.html?lang=en) rapportage<br/>(exclusief Attribution IQ- of virtuele-rapportsuites met verwerking bij de rapporttijd) | <ul><li>[Verwerkingsregels](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html?lang=en)</li><li>[VISTA-regels](https://experienceleague.adobe.com/docs/analytics/technotes/terms.html?lang=en)</li><li>Niveau [regels voor marketingkanalen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/marketing-channels/c-rules.html?lang=en)</li><li>Regels voor marketingkanalen op bezoekniveau (zie opmerking)</li><li>Definitie van bezoek</li><li>Attributielogica</li></ul> | <ul><li>Segmentlogica</li><li>Berekende standaarden</li></ul> | <ul><li>Apparaatanalyse (zie opmerking)</li></ul> | <ul><li>CDA vereist gebruik van virtuele rapportsuites met de verwerking van de rapporttijd.</li><li>De &quot;regels voor marketingkanalen op bezoekniveau&quot; omvatten: **Is de eerste bezoekpagina**, **Laatste aanraakkanaal overschrijven**, en **Vervaldatum marketingkanaal**. (Zie [documentatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html?lang=en).)</li></ul> |
| Adobe Analytics [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html?lang=en) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Definitie van bezoek</li><li>Attributielogica</li></ul> | <ul><li>Segmentlogica</li></ul> | <ul><li>Berekende standaarden</li><li>Cross-device Analytics</li></ul> |     |
| Adobe Analytics [Gegevensfeeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html?lang=en) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Definitie van bezoek (bezoekerveld)</li><li>Attributielogica (in postkolommen)</li></ul> |   | <ul><li>Segmentlogica</li><li>Berekende standaarden</li><li>Cross-device Analytics</li></ul> | <ul><li>ID-toewijzingen voor bepaalde kolommen met betrekking tot marketingkanalen in gegevensfeeds worden niet opgenomen in gegevensfeeds. (Zie de [gegevensdoorvoerdocumentatie](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=en).)</li></ul> |
| Adobe Analytics [Livestream](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) | <ul><li> Verwerkingsregels</li><li>VISTA-regels</li><ul> |   | <ul><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Naar logica</li><li>Attributielogica</li><li>Segmentlogica</li><li>Berekende standaarden</li><li>Cross-device Analytics</li></ul> |  |
| Adobe Analytics [Attribution IQ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/overview.html?lang=en) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Definitie van bezoek (zie opmerking)</li><li>Apparaatanalyse (zie opmerking)</li></ul> | <ul><li>Regels voor marketingkanalen op hoog niveau (zie opmerking)</li><li>Regels voor marketingkanalen op bezoekniveau (zie opmerking) Attributielogica</li><li>Segmentlogica</li><li>Berekende standaarden</li></ul> |  | <ul><li>CDA vereist gebruik van virtuele rapportsuites met de verwerking van de rapporttijd.</li><li>Attribution IQ in Core Analytics maakt gebruik van marketingkanalen die volledig zijn afgeleid op het moment van het rapport (d.w.z. afgeleide mid-values).</li><li>Attribution IQ gebruikt een verwerking-tijd bezoekdefinitie behalve wanneer gebruikt in een rapport-tijd verwerking VRS.</li></ul> |
| Adobe Analytics Virtual Report-suites met [rapporttijdverwerking](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html?lang=en) (VRS RTP) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>[Cross-device Analytics](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html?lang=en)</li></ul> | <ul><li>Definitie van bezoek</li><li>Attributielogica</li><li>Segmentlogica</li><li>Berekende standaarden</li><li>Andere VRS RTP-instellingen</li></ul> | <ul><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li></ul> | <ul><li>Zie VRS RTP [documentatie](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html?lang=en).</li></ul> |
| [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=en)Op gegevens gebaseerde dataset in het gegevenspenmeer van Adobe Experience Platform | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Veldgebaseerde stitching (zie opmerking)</li></ul> |   | <ul><li>[Regels voor verkoopkanalen op bezoekniveau](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html?lang=en)</li><li>Naar logica</li><li>Attributielogica</li><li>Filterlogica</li></ul> | <ul><li>U moet uw eigen filterlogica en berekende meetgegevens toepassen</li><li>Op veld gebaseerde stitching leidt tot een afzonderlijke gestikte dataset naast die gecreeerd door de bron van Analytics schakelaar.</li></ul> |
| [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html?lang=en) rapportage | <ul><li>Geïmplementeerd als onderdeel van Adobe Experience Platform-gegevensverzameling</li></ul> | <ul><li>Sessiedefinitie</li><li>[Gegevens, weergave](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views.html?lang=en) instellingen<li>Attributielogica</li><li>Berekende standaarden</li><li>Filterlogica</li></ul> | <ul><li>Regels voor verkoopkanalen op bezoekniveau</li></ul> | <ul><li>Moet gebonden gegevenssets gebruiken om te profiteren van kanaalanalyses.</li></ul> |

{style="table-layout:auto"}
