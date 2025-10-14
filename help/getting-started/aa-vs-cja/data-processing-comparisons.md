---
title: Vergelijk gegevensverwerking in Adobe Analytics en Customer Journey Analytics rapportfuncties
description: Begrijp de verschillen in gegevensverwerking voor de diverse rapportfuncties
exl-id: e3deedb2-0171-4fc2-9127-b9543603d4f0
feature: Basics
role: User
source-git-commit: 0e9dc47b80db142801a94dcbf31470d99a610949
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 0%

---

# Gegevensverwerking vergelijken in Adobe Analytics en Customer Journey Analytics

U hebt vaak de mogelijkheid nodig om gegevens te verwerken voordat deze nuttig zijn voor rapportage. U kunt die gegevens in verscheidene stadia in de reis verwerken die zich van het verzamelen van gegevens aan het produceren van uw rapport of visualisatie uitstrekken.

In Adobe Analytics vindt de verwerking van gegevens grotendeels direct plaats nadat de gegevens zijn verzameld. De functies zoals de Regels van VISTA, de Regels van de Verwerking, de Verwerkingsregels van Kanalen van de marketing zijn beschikbaar om dit **inzameling-tijd verwerking** te steunen.
De gegevens worden dan opgeslagen en op rapporttijd kunt u extra verwerking toepassen. U kunt bijvoorbeeld de afmetingen splitsen, segmentatie toepassen of een ander attributiemodel selecteren. Dit **rapport-tijd verwerking** gebeurt op de vlucht.

In Adobe Analytics, rapport-tijd vertegenwoordigt de verwerking gewoonlijk een kleinere hoeveelheid verwerking dan wat bij inzameling-tijd gebeurt.

![&#x200B; de inzameling-tijd van Adobe Analytics verwerking &#x200B;](../assets/aa-processing.png)

Customer Journey Analytics is daarentegen ontworpen om minimale verwerkingstijd vooraf te vereisen voordat gegevens worden geordend en opgeslagen. De onderliggende architectuur van Customer Journey Analytics wordt ontworpen om met de opgeslagen gegevens in rapport-tijd te werken. Customer Journey Analytics beschikt niet alleen in Analysis Workspace over de krachtige verwerkingsfunctionaliteit voor rapporttijd. De extra rapport-tijd verwerkingsfunctionaliteit is beschikbaar door de definitie van [&#x200B; componenten &#x200B;](/help/data-views/component-settings/overview.md) en [&#x200B; afgeleide gebieden &#x200B;](/help/data-views/derived-fields/derived-fields.md) in uw gegevensmeningen.

![&#x200B; Customer Journey Analytics rapport-tijd verwerking &#x200B;](../assets/cja-processing.png)

Kennis van de verschillen in gegevensverwerking voor de verschillende rapportfuncties kan nuttig zijn om te begrijpen welke meetgegevens beschikbaar zijn waar en waarom ze kunnen verschillen.

Bijvoorbeeld, *bezoeken* wordt bepaald als metrisch in Adobe Analytics bij de tijd van de gegevensverwerking. En *zittingen* wordt berekend als metrisch in Customer Journey Analytics in rapporttijd. Hierdoor kunnen de twee metriek afwijken, afhankelijk van de regels voor de sessiedefinitie in een Customer Journey Analytics-gegevensweergave.

Ook, zijn de bezoeken en de zittingen als metrisch niet beschikbaar in datasets die door de de bronschakelaar van Analytics worden gecreeerd. En daarom zou u de zitting in uw vraaglogica moeten bepalen om vergelijkingen te doen.

## Terminologie {#terms}

In de onderstaande tabel wordt de terminologie gedefinieerd voor de verschillende typen verwerkingslogica die op Adobe Analytics en Customer Journey Analytics worden toegepast:

| Term | Definitie | Notities |
| --- | --- | --- |
| Verwerking van de verzameltijd | Logica die wordt uitgevoerd wanneer gegevens worden verzameld en verwerkt, voordat ze worden opgeslagen voor rapportage- en analysedoeleinden. | Deze logica is &quot;gebaseerd op&quot; historische gegevens en kan over het algemeen niet eenvoudig worden gewijzigd. |
| Verwerking bij rapporttijd | Logica die wordt uitgevoerd op het moment dat een rapport wordt uitgevoerd. | Deze logica kan op een niet-destructieve manier op toekomstige en historische gegevens bij rapportruntime worden toegepast. |
| Logica op bedrijfsniveau | Logica toegepast op rij-voor-rij niveau. | Voorbeelden: verwerkingsregels, VISTA, bepaalde regels voor marketingkanalen. |
| Logica op bezoekniveau | Logica die wordt toegepast op bezoekniveau. | Voorbeelden: definitie van bezoek en sessie. |
| Logica op bezoekersniveau | Logica die wordt toegepast op persoonniveau. | Voorbeeld: personentching via een ander apparaat/kanaal. |
| Segmentlogica | Evaluatie van de segmentregels voor gebeurtenissen/bezoeken/personen (gebeurtenis/sessie/persoon). | Voorbeeld: Mensen die rode schoenen kochten. |
| Berekende cijfers | Evaluatie van klantgerichte metriek. Berekende metriek kan op complexe formules, met inbegrip van segmenten worden gebaseerd. | Bijvoorbeeld het aantal mensen dat rode schoenen heeft gekocht. |
| Attributielogica | Logische berekening van attributie. | Voorbeeld: eVar persistentie. |
| Componentinstellingen | Aanpassingen toepassen op metriek of dimensies, zoals kenmerk, gedrag, indeling en andere | Voorbeeld: waarde overlapt om numerieke waarden te combineren op basis van een bereik |
| Afgeleide velden | De logica die op schema of standaardgebieden als deel van het bepalen van componenten in een mening van Gegevens van toepassing is. | Voorbeeld: een nieuwe dimensie voor een marketingkanaal maken |

{style="table-layout:auto"}

In de loop der tijd hebben Adobe Analytics en nu Customer Journey Analytics hun flexibiliteit verbeterd door het toestaan van bezoek en persoon-vlakke gegevenslogica om bij rapportruntime te worden uitgevoerd.

## Typen gegevensverwerking {#types}

De gegevensverwerkingsstappen die door Adobe Analytics en Customer Journey Analytics worden uitgevoerd en de timing van deze stappen verschillen van functie tot functie. In de onderstaande tabel vindt u een overzicht van de typen gegevensverwerking voor elke functie en wanneer gegevensverwerking wordt toegepast.

| Functie | Toegepast op verwerkingstijd | Toegepast op rapporttijd | Niet beschikbaar | Notities |
| --- | --- | --- | --- | --- |
| [&#x200B; Adobe Analytics &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics) rapporterend <br/> (zonder geavanceerde attributieeigenschappen of virtuele rapportsuites met rapport-tijd verwerking) | <ul><li>[&#x200B; Regels van de Verwerking &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules)</li><li>[VISTA-regels](https://experienceleague.adobe.com/nl/docs/analytics/technotes/terms)</li><li>Het greep-niveau [&#x200B; marketing kanaalregels &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/marketing-channels/c-rules)</li><li>Regels voor marketingkanalen op bezoekniveau (zie opmerking)</li><li>Definitie van bezoek</li><li>Attributielogica</li></ul> | <ul><li>Segmentlogica</li><li>Berekende cijfers</li></ul> | <ul><li>Apparaatanalyse (zie opmerking)</li></ul> | <ul><li>Voor Apparaatanalyse is het gebruik van virtuele rapportsuites met verwerking van de rapporttijd vereist.</li><li>&quot;Bezoek-vlakke marketing kanaalregels&quot;omvatten het volgende: **is Eerste Pagina van Bezoek**, **met voeten treedt laatste-Aanraakkanaal**, en **de Vervalsing van het Kanaal van de Marketing**. (Zie [&#x200B; documentatie &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-usecases/aa-data/marketing-channels).)</li></ul> |
| Adobe Analytics [&#x200B; Data Warehouse &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/export/data-warehouse/data-warehouse) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Definitie van bezoek</li><li>Attributielogica</li></ul> | <ul><li>Segmentlogica</li></ul> | <ul><li>Berekende cijfers</li><li>Apparaatanalyse</li></ul> |     |
| Adobe Analytics [&#x200B; de Evoer van Gegevens &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/export/analytics-data-feed/data-feed-overview) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Definitie van bezoek (bezoekerveld)</li><li>Attributielogica (in postkolommen)</li></ul> |   | <ul><li>Segmentlogica</li><li>Berekende cijfers</li><li>Apparaatanalyse</li></ul> | <ul><li>ID-toewijzingen voor bepaalde kolommen met betrekking tot marketingkanalen in gegevensfeeds worden niet opgenomen in gegevensfeeds. (Zie de [&#x200B; documentatie van de gegevenstoevoer &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference).)</li></ul> |
| Adobe Analytics [&#x200B; Livestream &#x200B;](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) | <ul><li> Verwerkingsregels</li><li>VISTA-regels</li><ul> |   | <ul><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li><li>Naar logica</li><li>Attributielogica</li><li>Segmentlogica</li><li>Berekende cijfers</li><li>Apparaatanalyse</li></ul> |  |
| Adobe Analytics [&#x200B; Geavanceerde attributieeigenschappen &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/analyze/analysis-workspace/attribution/overview) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Definitie van bezoek (zie opmerking)</li><li>Apparaatanalyse (zie opmerking)</li></ul> | <ul><li>Regels voor marketingkanalen op hoog niveau (zie opmerking)</li><li>Regels voor marketingkanalen op bezoekniveau (zie opmerking) Attributielogica</li><li>Segmentlogica</li><li>Berekende cijfers</li></ul> |  | <ul><li>Voor Apparaatanalyse is het gebruik van virtuele rapportsuites met verwerking van de rapporttijd vereist.</li><li>De geavanceerde attributieeigenschappen in de Analyse van de Kern gebruiken marketing kanalen die volledig in rapporttijd (namelijk afgeleide middenwaarden) worden afgeleid.</li><li>De geavanceerde attributieeigenschappen gebruiken een verwerking-tijd bezoekdefinitie behalve wanneer gebruikt in een rapport-tijd verwerkings virtuele rapportreeks.</li></ul> |
| De virtuele het rapportsuites van Adobe Analytics met [&#x200B; rapport-tijd verwerking &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/components/virtual-report-suites/vrs-report-time-processing) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>[&#x200B; dwars-ApparaatAnalytics &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/components/cda/overview)</li></ul> | <ul><li>Definitie van bezoek</li><li>Attributielogica</li><li>Segmentlogica</li><li>Berekende cijfers</li><li>Andere virtuele rapportsuite, verwerkingsinstellingen voor rapporttijd</li></ul> | <ul><li>Regels voor distributiekanalen op hoog niveau</li><li>Regels voor verkoopkanalen op bezoekniveau</li></ul> | <ul><li>Zie Virtuele rapport-tijd verwerking van de rapportreeks [&#x200B; documentatie &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/components/virtual-report-suites/vrs-report-time-processing).</li></ul> |
| [-Gebaseerde dataset van de bron van de Analyse van 0&rbrace; in het gegevensmeer van Adobe Experience Platform](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/connectors/adobe-applications/analytics) | <ul><li>Verwerkingsregels</li><li>VISTA-regels</li><li>Regels voor distributiekanalen op hoog niveau</li><li>Veldgebaseerde stitching (zie opmerking)</li></ul> |   | <ul><li>[&#x200B; bezoek-vlakke marketing kanaalregels &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-usecases/aa-data/marketing-channels)</li><li>Naar logica</li><li>Attributielogica</li><li>Segmentlogica</li></ul> | <ul><li>Pas uw eigen segmentlogica en berekende metriek toe</li><li>Op veld gebaseerde stitching leidt tot een afzonderlijke gestikte dataset naast die die door de bron van Analytics schakelaar wordt gecreeerd.</li></ul> |
| [&#x200B; Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-landing) rapportering | <ul><li>Geïmplementeerd als onderdeel van Adobe Experience Platform-gegevensverzameling</li></ul> | <ul><li>Sessiedefinitie</li><li>[&#x200B; de mening van Gegevens &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-dataviews/data-views) montages<li>Attributielogica</li><li>Berekende cijfers</li><li>Segmentlogica</li></ul> | <ul><li>Regels voor verkoopkanalen op bezoekniveau</li></ul> | <ul><li>Gebruik gebonden datasets om te profiteren van kanaalanalyses.</li></ul> |

{style="table-layout:auto"}
