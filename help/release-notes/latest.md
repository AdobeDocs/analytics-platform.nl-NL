---
title: Huidige vrijgavenotities van Customer Journey Analytics
description: Aanvullende informatie voor de nieuwste versie van Customer Journey Analytics weergeven
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: ea699bcacd985d9da1e3895f7770290dc77da537
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 2%

---

# Huidige Customer Journey Analytics-releaseopmerkingen (januari 2026)

**Laatste update**: 14 Januari, 2026

Deze releaseopmerkingen hebben betrekking op de releaseperiode januari 2026. De versies van Adobe Customer Journey Analytics werken op a [&#x200B; ononderbroken leveringsmodel &#x200B;](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [&#x200B; Het begin van de Uitvoer &#x200B;](releases.md) | [&#x200B; Algemene Beschikbaarheid &#x200B;](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Analyseer doelgroepen uit Experience Platform Profile datasets in Customer Journey Analytics** | Je kunt nu lidmaatschapsgegevens van de doelgroep uit Experience Platform Profile-datasets invoeren in een Customer Journey Analytics-verbinding. Doelgroepen worden beschikbaar als nieuwe dimensies voor gebruik in Analysis Workspace.<p>Dit is mogelijk gemaakt door een nieuwe mogelijkheid in Customer Journey Analytics om XDM-objectmaps te importeren, waardoor het mogelijk is om Profile AudienceIDs in te voeren.</p><p>Voorheen konden alleen eenvoudige XDM-kaarten worden opgenomen in Customer Journey Analytics.</p><p>Naast het kunnen publieksgegevens als afmetingen aan om het even welk project in Analysis Workspace toevoegen, zijn de volgende nieuwe malplaatjes van Workspace ook beschikbaar:</p><ul><li>Audience Analytics - Overzicht</li><li>Overzicht van goedgekeurd beleid</li><p><!--For more information, see "Audience analysis overview" (https://experienceleague.corp.adobe.com/docs/analytics-platform/using/cja-dataviews/audience-analysis/audience-analysis-overview.html).-->(Documentatielink volgt.)</p> | donderdag 22 oktober 2025 | vrijdag 22 januari 2026 |
| **Data storytelling: Genereer diapresentaties uit Workspace-rapporten** | U kunt nu automatisch een diapresentatie genereren (in de .pptx-indeling) die is gebaseerd op een Analysis Workspace-rapport. Workspace detecteert belangrijke inzichten in uw rapport en zet deze om in dia&#39;s die klaar zijn voor belanghebbenden.<p>Deze eigenschap vermindert de tijd en de inspanning die wordt vereist om bevindingen te tonen, uitvoerende verhalen te bouwen, en bedrijfsimpact mee te delen.</p><p>(De verbinding van de Documentatie te volgen.) <!--For more information, see [Data storytelling: Generate slide presentations from Workspace reports](/help/analysis-workspace/curate-share/generate-slides.md).--></p> | donderdag 22 oktober 2025 | donderdag 28 januari 2026 |
| **omvat veelvoudige afmetingskolommen in een vrije vormlijst** | U kunt nu maximaal vijf dimensiekolommen opnemen in een vrije-vormlijst, zodat u meerdere dimensiepunten naast elkaar kunt weergeven. Elke rij van afmetingspunten gedraagt zich als één enkel samengevoegd afmetingspunt.<p>U kunt filters, het sorteren, het breken, en meer op vrije vormlijsten met veelvoudige afmetingskolommen toepassen om een diepere en meer douaneanalyse tot stand te brengen.</p><p>Eerder kon u slechts één dimensiekolom in een vrije-vormlijst opnemen.</p><p><!-- For more information, see [Include multiple dimension columns in a freeform table](/help/analysis-workspace/visualizations/freeform-table/freeform-table-multidimensions.md).--> (Koppeling met documentatie die moet worden gevolgd.)</p> | donderdag 28 januari 2026 | donderdag 18 februari 2026 |
| **Sorteer tabellen op meerdere kolommen** | Je kunt nu de gegevens van een vrije tabel sorteren op meerdere kolommen in Analysis Workspace, of het nu dimensies of metrieken zijn.<p>Wanneer u gegevens voor meerdere kolommen sorteert, worden de gegevens gesorteerd op basis van de prioriteit die u aan elke kolom toewijst. De prioriteitsnummering wordt weergegeven naast het sorteerpictogram.</p><p>(De verbinding van de Documentatie te volgen.) <!-- For more information, see "Filter and sort freeform tables". (need to move info to this article from "Include multiple dimension columns in a freeform table") --></p> | donderdag 28 januari 2026 | donderdag 18 februari 2026 |
| **Combineer databronnen van meerdere IMS-organisaties** | Je kunt nu de Analytics Source Connector gebruiken om meerdere databronnen van verschillende IMS-organisaties te combineren. Dit stelt organisaties in staat om een gecombineerd beeld te hebben van hun klantgegevens, zelfs wanneer die klantgegevens verspreid zijn over meerdere IMS-organisaties. <p>**Nota:** Deze configuratie is beschikbaar slechts door een verzoek aan de Zorg van de Klant van Adobe voor te leggen.</p>  <p>(Koppeling met documentatie die moet worden gevolgd.)</p> |  | zaterdag 30 januari 2026 |
| **Stitching in verbindingen** | Het heetsproces in Customer Journey Analytics is nu eenvoudiger. In plaats van een dataset te dupliceren en het verbinden op de gedupliceerde dataset toe te passen, wordt nu het stitching gedaan op de opname van gegevens in Customer Journey Analytics, die het vereiste van gedupliceerde datasets en schema&#39;s schrapt. <p>Bovendien kun je nu [zelf beginnen met stitchen via een bijgewerkte Connections-interface](/help/stitching/use-stitching-ui.md), in plaats van stitching via Adobe Customer Care aan te vragen.</p><p> *De eerder aangekondigde releasedata werden uitgesteld vanwege extra inspanningen en het vakantieseizoen. Er is nu een gefaseerde uitrol gepland om stabiliteit te waarborgen en verstoringen tijdens de feestdagen te minimaliseren.*</p> | woensdag 28 oktober 2025 | zaterdag 30 januari 2026 |
| **Steun voor gegevensspiegel** | Met steun voor model-gebaseerde schema&#39;s en de functionaliteit van de vangst van veranderingsgegevens (CDC) voor specifieke bronschakelaars in Experience Platform, zal Customer Journey Analytics [&#x200B; functionaliteit van de gegevenspiegel van &#x200B;](/help/data-mirror/data-mirror.md) kunnen steunen [!DNL Snowflake], [!DNL Azure Databricks], en [!DNL Google BigQuery].<p>Neem contact op met uw Adobe-accountteam voor toegang tot de bètaversie.</p> | Bèta-release: 24 september 2025 | Nog te bepalen |
| **Streaming mediadiensten: Ondersteun planningsgegevens** | U kunt nu geplande gegevens van eerder live streaming media-inhoud uploaden om de viewer eenvoudiger en nauwkeuriger bij te houden.<p>Hieronder volgen voorbeelden van live-inhoud die wordt ondersteund met het uploaden van planningsgegevens:</p><ul><li>SNELLE (Free Ad Supported TV) platforms</li><li>Lokale streams</li><li>Levende sport</li></ul><p>Door planningsgegevens te uploaden, kunt u de viewergegevens bijhouden voor afzonderlijke programma&#39;s die worden uitgevoerd tijdens de tijd die u aangeeft in het uploadbestand. U kunt zelfs kijkersgegevens voor specifieke onderwerpen of programmasegmenten verzamelen.</p><p>Deze mogelijkheden zijn beschikbaar ongeacht de manier waarop u de Verzameling van de Media van de Streaming uitvoerde.</p><p>Eerder, was het moeilijk om een bepaalde zitting aan specifieke programma&#39;s nauwkeurig te verbinden wanneer het analyseren van levende inhoud, en het was niet mogelijk om een bepaalde zitting aan individuele onderwerpen of programmasegmenten te binden.</p><p>Voor meer informatie, zie [&#x200B; planningsgegevens uploaden om levende inhoud &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/media-use-cases/track-schedule-data) te volgen</p> | donderdag 29 oktober 2025 | Eerste helft van 2026<p>(Oorspronkelijk gepland voor release op 29 oktober 2025)</p> |

## Oplossingen in Customer Journey Analytics

**Analysewerkruimte**: AN-423389, AN-423316, AN-422636, AN-422482, AN-422121, AN-422116, AN-422027, AN-421134, AN-420187, AN-406271, AN-406188, AN-405997, AN-405983, AN-405796, AN-405033, AN-404893, AN-404877, AN-404873, AN-404877, AN-404877 1, AN-404842, AN-404713, AN-404502, AN-404353, AN-404352, AN-404048, AN-403241, AN-402523, AN-400795, AN-396149, AN-390990, AN-390646, AN-383484, AN-376980, AN-371729, AN-347570, AN-404835
**Componenten**:
**Contentanalyse**:
**Geleide analyse**: AN-421274
**Export:**
**Gegevensweergaven**: AN-421891, AN-404627
**Implementatie**:
**Rapportbouwer**: AN-422120, AN-421937, AN-406296, AN-402951, AN-399748
**Verslaggeving**:
**Segmentatie**:
**Geplande rapporten**: AN-423087, AN-422686
**Gedeelde metrics en dimensies**:
**Overig**: AN-422946, AN-422775, AN-422273, AN-422100, AN-420045, AN-404891, AN-390912


## Belangrijke kennisgevingen voor Customer Journey Analytics-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. |  |  |

## Gerelateerde bronnen

* [Vorige Customer Journey Analytics release-notities voor 2025](/help/release-notes/2025.md)
* [Adobe Analytics release-notities](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=nl-NL)
* [&#x200B; het stromen de versienota&#39;s van de Inzameling van Media &#x200B;](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=nl-NL)
* [&#x200B; de versienota&#39;s van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl-NL)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
