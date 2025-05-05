---
title: Vergelijk gegevensverwerking in Adobe Analytics en Customer Journey Analytics rapportfuncties
description: Begrijp de verschillen in gegevensverwerking voor de diverse rapportfuncties
exl-id: e3deedb2-0171-4fc2-9127-b9543603d4f0
feature: Basics
role: User
source-git-commit: 976f481b6886a4f260f44854a30c47ab0dad7955
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---

# Gegevensverwerking vergelijken in Adobe Analytics en Customer Journey Analytics

U hebt vaak de mogelijkheid nodig om gegevens te verwerken voordat deze nuttig zijn voor rapportage. U kunt die gegevens in verscheidene stadia in de reis verwerken die zich van het verzamelen van gegevens aan het produceren van uw rapport of visualisatie uitstrekken.

In Adobe Analytics vindt de verwerking van gegevens grotendeels direct plaats nadat de gegevens zijn verzameld. De functies zoals de Regels van VISTA, de Regels van de Verwerking, de Verwerkingsregels van Kanalen van de marketing zijn beschikbaar om dit **inzameling-tijd verwerking** te steunen.
De gegevens worden dan opgeslagen en op rapporttijd kunt u extra verwerking toepassen. U kunt bijvoorbeeld de afmetingen splitsen, segmentatie toepassen of een ander attributiemodel selecteren. Dit **rapport-tijd verwerking** gebeurt op de vlucht.

In Adobe Analytics, rapport-tijd vertegenwoordigt de verwerking gewoonlijk een kleinere hoeveelheid verwerking dan wat bij inzameling-tijd gebeurt.

![ de inzameling-tijd van Adobe Analytics verwerking ](../assets/aa-processing.png)

Customer Journey Analytics is daarentegen ontworpen om minimale verwerkingstijd vooraf te vereisen voordat gegevens worden geordend en opgeslagen. De onderliggende architectuur van Customer Journey Analytics wordt ontworpen om met de opgeslagen gegevens in rapport-tijd te werken en biedt zijn krachtige rapport-tijd verwerkingsfunctionaliteit niet alleen in Workspace maar ook, nog belangrijker, door de definitie van [ componenten ](/help/data-views/component-settings/overview.md) en [ afgeleide gebieden ](/help/data-views/derived-fields/derived-fields.md) in uw meningen van Gegevens aan.

![ Customer Journey Analytics rapport-tijd verwerking ](../assets/cja-processing.png)

Kennis van de verschillen in gegevensverwerking voor de verschillende rapportfuncties kan nuttig zijn om te begrijpen welke meetgegevens beschikbaar zijn waar en waarom ze kunnen verschillen.

Bijvoorbeeld, aangezien &quot;bezoeken&quot;als metrisch in Adobe Analytics bij gegevensverwerkingstijd worden bepaald, en &quot;zittingen&quot;als metrisch in Customer Journey Analytics bij rapporttijd wordt berekend, kunnen de twee metriek verschillen gebaseerd op de regels die voor zittingsdefinitie binnen de Customer Journey Analytics gegevensmening worden gebruikt.

Ook, noch bezoeken noch zittingen als metrisch zijn beschikbaar in datasets die door de bron van Analytics schakelaar worden gecreeerd en daarom zou u vereisen om de zitting in uw vraaglogica te bepalen om vergelijkingen te doen.

## Terminologie {#terms}

In de onderstaande tabel wordt de terminologie gedefinieerd voor de verschillende typen verwerkingslogica die op Adobe Analytics en Customer Journey Analytics worden toegepast:

| Term | Definitie | Notities |
| --- | --- | --- |
| Verwerking van de verzameltijd | Logica die wordt uitgevoerd wanneer gegevens worden verzameld en verwerkt, voordat ze worden opgeslagen voor rapportage- en analysedoeleinden. | Deze logica is &quot;gebaseerd op&quot; historische gegevens en kan over het algemeen niet eenvoudig worden gewijzigd. |
| Verwerking bij rapporttijd | Logica die wordt uitgevoerd op het moment dat een rapport wordt uitgevoerd. | Deze logica kan op een niet-destructieve manier op toekomstige en historische gegevens bij rapportruntime worden toegepast. |
| Logica op bedrijfsniveau | Logica toegepast op rij-voor-rij niveau. | Voorbeelden: verwerkingsregels, VISTA, bepaalde regels voor marketingkanalen. |
| Logica op bezoekniveau | Logica toegepast op bezoekniveau. | Voorbeelden: definitie van bezoek en sessie. |
| Logica op bezoekersniveau | Logica toegepast op persoonniveau. | Voorbeeld: personentching via een ander apparaat/kanaal. |
| Segmentlogica | Evaluatie van de segmentregels voor gebeurtenissen/bezoeken/personen (gebeurtenis/sessie/persoon). | Voorbeeld: Mensen die rode schoenen kochten. |
| Berekende cijfers | Evaluatie van door de klant gemaakte aangepaste maatstaven die op complexe formules kunnen worden gebaseerd, inclusief segmenten. | Voorbeeld: aantal mensen die rode schoenen kochten. |
| Attributielogica | Logische berekening van attributie. | Voorbeeld: eVar persistentie. |
| Componentinstellingen | Aanpassingen toepassen op metriek of dimensies, zoals kenmerk, gedrag, indeling en andere | Voorbeeld: waarde overlapt om numerieke waarden te combineren op basis van een bereik |
| Afgeleide velden | De logica is van toepassing op schema of standaardgebieden als deel van het bepalen van componenten in een mening van Gegevens. | Voorbeeld: een nieuwe dimensie voor een marketingkanaal maken |

{style="table-layout:auto"}

In de loop der tijd hebben Adobe Analytics en nu Customer Journey Analytics hun flexibiliteit verbeterd door het toestaan van bezoek en persoon-vlakke gegevenslogica om bij rapportruntime te worden uitgevoerd.

## Typen gegevensverwerking {#types}

De gegevensverwerkingsstappen die worden uitgevoerd voor Adobe Analytics en Customer Journey Analytics en de timing van deze stappen verschillen van functie tot functie Analytics. In de onderstaande tabel vindt u een overzicht van de typen gegevensverwerking voor elke functie Analytics en wanneer de gegevensverwerking wordt toegepast.

| Functie | Toegepast op verwerkingstijd | Toegepast op rapporttijd | Niet beschikbaar | Notities |
| --- | --- | --- | --- | --- |
| [ Adobe Analytics ](https://experienceleague.adobe.com/docs/analytics.html?lang=nl-NL) rapporterend <br/> (exclusief Attribution IQ of virtuele rapportsuites met rapport-tijd verwerking) | <ul><li>[ Regels van de Verwerking ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/processing-rules/processing-rules.html?lang=nl-NL)</li><li>[VISTA-regels](https://experienceleague.adobe.com/docs/analytics/technotes/terms.html?lang=nl-NL)</li><li>Het greep-niveau [ marketing kanaalregels ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/marketing-channels/c-rules.html?lang=nl-NL)</li><li>Regels voor marketingkanalen op bezoekniveau (zie opmerking)</li><li>Definitie van bezoek</li><li>Attributielogica</li></ul> | <ul><li>Segmentlogica</li><li>Berekende cijfers</li></ul> | <ul><li>Apparaatanalyse (zie opmerking)</li></ul> | <ul><li>CDA vereist gebruik van virtuele rapportsuites met de verwerking van de rapporttijd.</li><li>&quot;Bezoek-vlakke marketing kanaalregels&quot;omvatten het volgende: **is Eerste Pagina van Bezoek**, **met voeten treedt laatste-Aanraakkanaal**, en **de Vervalsing van het Kanaal van de Marketing**. (Zie [ documentatie ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html?lang=nl-NL).)</li></ul> |
| Adobe Analytics [ Data Warehouse ](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html?lang=nl-NL) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Definitie van bezoek</li><li>Attributielogica</li></ul> | <ul><li>Segmentlogica</li></ul> | <ul><li>Berekende cijfers</li><li>Apparaatanalyse</li></ul> |     |
| Adobe Analytics [ de Evoer van Gegevens ](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html?lang=nl-NL) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Definitie van bezoek (bezoekerveld)</li><li>Attributielogica (in postkolommen)</li></ul> |   | <ul><li>Segmentlogica</li><li>Berekende cijfers</li><li>Apparaatanalyse</li></ul> | <ul><li>ID-toewijzingen voor bepaalde kolommen met betrekking tot marketingkanalen in gegevensfeeds worden niet opgenomen in gegevensfeeds. (Zie de [ documentatie van de gegevenstoevoer ](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=nl-NL).)</li></ul> |
| Adobe Analytics [ Livestream ](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) | <ul><li> Verwerkingsregels</li><li>VISTA-regels</li><ul> |   | <ul><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Naar logica</li><li>Attributielogica</li><li>Segmentlogica</li><li>Berekende cijfers</li><li>Apparaatanalyse</li></ul> |  |
| Adobe Analytics [ Attribution IQ ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/overview.html?lang=nl-NL) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Definitie van bezoek (zie opmerking)</li><li>Apparaatanalyse (zie opmerking)</li></ul> | <ul><li>Regels voor marketingkanalen op hoog niveau (zie opmerking)</li><li>Regels voor marketingkanalen op bezoekniveau (zie opmerking) Attributielogica</li><li>Segmentlogica</li><li>Berekende cijfers</li></ul> |  | <ul><li>CDA vereist gebruik van virtuele rapportsuites met de verwerking van de rapporttijd.</li><li>Attribution IQ in Core Analytics maakt gebruik van marketingkanalen die volledig zijn afgeleid op het moment van het rapport (d.w.z. afgeleide mid-values).</li><li>Attribution IQ gebruikt een definitie van een bezoek tijdens de verwerking, behalve wanneer deze wordt gebruikt in een virtuele rapportsuite tijdens de verwerking.</li></ul> |
| De virtuele het rapportsuites van Adobe Analytics met [ rapport-tijd verwerking ](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html?lang=nl-NL) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>[ dwars-ApparaatAnalytics ](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html?lang=nl-NL)</li></ul> | <ul><li>Definitie van bezoek</li><li>Attributielogica</li><li>Segmentlogica</li><li>Berekende cijfers</li><li>Andere virtuele rapportsuite, verwerkingsinstellingen voor rapporttijd</li></ul> | <ul><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li></ul> | <ul><li>Zie Virtuele rapport-tijd verwerking van de rapportreeks [ documentatie ](https://experienceleague.adobe.com/docs/analytics/components/virtual-report-suites/vrs-report-time-processing.html?lang=nl-NL).</li></ul> |
| [&#128279;](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=nl-NL)-Gebaseerde dataset van de bron van de Analyse van 0&rbrace; in het gegevensmeer van Adobe Experience Platform | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Veldgebaseerde stitching (zie opmerking)</li></ul> |   | <ul><li>[ bezoek-vlakke marketing kanaalregels ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html?lang=nl-NL)</li><li>Naar logica</li><li>Attributielogica</li><li>Segmentlogica</li></ul> | <ul><li>U moet uw eigen segmentlogica en berekende maatstaven toepassen</li><li>Op veld gebaseerde stitching leidt tot een afzonderlijke gestikte dataset naast die die door de bron van Analytics schakelaar wordt gecreeerd.</li></ul> |
| [ Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html?lang=nl-NL) rapportering | <ul><li>Geïmplementeerd als onderdeel van Adobe Experience Platform-gegevensverzameling</li></ul> | <ul><li>Sessiedefinitie</li><li>[ de mening van Gegevens ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views.html?lang=nl-NL) montages<li>Attributielogica</li><li>Berekende cijfers</li><li>Segmentlogica</li></ul> | <ul><li>Regels voor verkoopkanalen op bezoekniveau</li></ul> | <ul><li>Moet gebonden gegevenssets gebruiken om te profiteren van kanaalanalyses.</li></ul> |

{style="table-layout:auto"}
