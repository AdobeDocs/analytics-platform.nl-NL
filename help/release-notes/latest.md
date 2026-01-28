---
title: Opmerkingen bij de release van Customer Journey Analytics
description: Aanvullende informatie voor de nieuwste versie van Customer Journey Analytics weergeven
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 3955f7c8da90481610328c0657b33e81ad6c0057
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 2%

---

# Huidige Customer Journey Analytics-releaseopmerkingen (januari 2026)

**Laatste update**: 14 Januari, 2026

Deze releaseopmerkingen hebben betrekking op de releaseperiode januari 2026. De versies van Adobe Customer Journey Analytics werken op a [&#x200B; ononderbroken leveringsmodel &#x200B;](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [&#x200B; Het begin van de Uitvoer &#x200B;](releases.md) | [&#x200B; Algemene Beschikbaarheid &#x200B;](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **analyseert publiek van de datasets van het Profiel van Experience Platform in Customer Journey Analytics** | U kunt nu de gegevens van het publiekslidmaatschap van de datasets van het Profiel van Experience Platform in een verbinding van Customer Journey Analytics opnemen. Soorten publiek wordt beschikbaar als nieuwe afmetingen voor gebruik in Analysis Workspace.<p>Dit wordt mogelijk gemaakt door een nieuwe mogelijkheid in Customer Journey Analytics om XDM object-maps in te voeren, waardoor het mogelijk wordt om Profile AudienceIDs in te voeren.</p><p>Eerder konden alleen eenvoudige XDM-maps in Customer Journey Analytics worden opgenomen.</p><p>Naast het kunnen publieksgegevens als afmetingen aan om het even welk project in Analysis Workspace toevoegen, zijn de volgende nieuwe malplaatjes van Workspace ook beschikbaar:</p><ul><li>Audience Analytics - Overzicht</li><li>Overzicht van goedgekeurd beleid</li></ul><p>Voor meer informatie, zie [&#x200B; de analyse van het publiek overzicht &#x200B;](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/audience-analysis/audience-analysis-overview.html).</p> | donderdag 22 oktober 2025 | woensdag 27 januari 2026 <p> (Oorspronkelijk gepland voor 22 januari 2026)</p> |
| **het verhaal van Gegevens: Produceer diapresentaties van de rapporten van Workspace** | U kunt nu automatisch een diapresentatie genereren (in de .pptx-indeling) die is gebaseerd op een Analysis Workspace-rapport. Workspace detecteert belangrijke inzichten in uw rapport en zet deze om in dia&#39;s die klaar zijn voor belanghebbenden.<p>Deze eigenschap vermindert de tijd en de inspanning die wordt vereist om bevindingen te tonen, uitvoerende verhalen te bouwen, en bedrijfsimpact mee te delen.</p><p>Voor meer informatie, zie [&#x200B; het verhaal van Gegevens: Produceer diapresentaties van de rapporten van Workspace &#x200B;](/help/analysis-workspace/curate-share/generate-slides.md).</p> | donderdag 22 oktober 2025 | donderdag 28 januari 2026 |
| **omvat veelvoudige afmetingskolommen in een vrije vormlijst** | U kunt nu maximaal vijf dimensiekolommen opnemen in een vrije-vormlijst, zodat u meerdere dimensiepunten naast elkaar kunt weergeven. Elke rij van afmetingspunten gedraagt zich als één enkel samengevoegd afmetingspunt.<p>U kunt filters, het sorteren, het breken, en meer op vrije vormlijsten met veelvoudige afmetingskolommen toepassen om een diepere en meer douaneanalyse tot stand te brengen.</p><p>Eerder kon u slechts één dimensiekolom in een vrije-vormlijst opnemen.</p><p>Voor meer informatie, zie [&#x200B; veelvoudige afmetingskolommen in een vrije vormlijst &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table-multidimensions.md) omvatten.</p> | donderdag 28 januari 2026 | donderdag 18 februari 2026 |
| **de lijsten van de Soort door veelvoudige kolommen** | U kunt de gegevens van een vrije-vormlijst door veelvoudige kolommen in Analysis Workspace nu sorteren, of zij dimensies of metriek zijn.<p>Wanneer u gegevens voor meerdere kolommen sorteert, worden de gegevens gesorteerd op basis van de prioriteit die u aan elke kolom toewijst. De prioriteitsnummering wordt weergegeven naast het sorteerpictogram.</p><p>(De verbinding van de Documentatie te volgen.) <!-- For more information, see "Filter and sort freeform tables". (need to move info to this article from "Include multiple dimension columns in a freeform table") --></p> | donderdag 28 januari 2026 | donderdag 18 februari 2026 |
| **combineer gegevensbronnen van veelvoudige organismen IMS** | U kunt nu de Analytics Source Connector gebruiken om meerdere gegevensbronnen van meerdere IMS-organen te combineren. Dit staat organisaties toe om een gecombineerde mening van hun klantengegevens te hebben, zelfs wanneer dat klantengegeven over veelvoudige organisaties IMS wordt verspreid. <p>**Nota:** Deze configuratie is beschikbaar slechts door een verzoek aan de Zorg van de Klant van Adobe voor te leggen.</p>  <p>(Koppeling met documentatie die moet worden gevolgd.)</p> |  | zaterdag 30 januari 2026 |
| **Stitching in verbindingen** | Het heetsproces in Customer Journey Analytics is nu eenvoudiger. In plaats van een dataset te dupliceren en het verbinden op de gedupliceerde dataset toe te passen, wordt nu het stitching gedaan op de opname van gegevens in Customer Journey Analytics, die het vereiste van gedupliceerde datasets en schema&#39;s schrapt. <p>Voorts kunt u [&#x200B; het stitching nu door een bijgewerkte interface van Verbindingen &#x200B;](/help/stitching/use-stitching-ui.md) in werking stellen, in plaats van het moeten het stitching door de Zorg van de Klant van Adobe verzoeken.</p><p> *de eerder meegedeelde versiedata werden uitgesteld wegens extra vereiste inspanningen en het vakantieseizoen. Een gefaseerde uitrol wordt nu gepland om stabiliteit te verzekeren en verstoring tijdens de vakantieperiode te minimaliseren.*</p> | woensdag 28 oktober 2025 | zaterdag 30 januari 2026 |
| **Steun voor gegevensspiegel** | Met steun voor model-gebaseerde schema&#39;s en de functionaliteit van de vangst van veranderingsgegevens (CDC) voor specifieke bronschakelaars in Experience Platform, zal Customer Journey Analytics [&#x200B; functionaliteit van de gegevenspiegel van &#x200B;](/help/data-mirror/data-mirror.md) kunnen steunen [!DNL Snowflake], [!DNL Azure Databricks], en [!DNL Google BigQuery].<p>Neem contact op met uw Adobe-accountteam voor toegang tot de bètaversie.</p> | Beta-release: 24 september 2025 | TBD |
| **Streaming media de diensten: De planningsgegevens van de steun** | U kunt nu geplande gegevens van eerder live streaming media-inhoud uploaden om de viewer eenvoudiger en nauwkeuriger bij te houden.<p>Hieronder volgen voorbeelden van live-inhoud die wordt ondersteund met het uploaden van planningsgegevens:</p><ul><li>SNELLE (Free Ad Supported TV) platforms</li><li>Lokale streams</li><li>Levende sport</li></ul><p>Door planningsgegevens te uploaden, kunt u de viewergegevens bijhouden voor afzonderlijke programma&#39;s die worden uitgevoerd tijdens de tijd die u aangeeft in het uploadbestand. U kunt zelfs kijkersgegevens voor specifieke onderwerpen of programmasegmenten verzamelen.</p><p>Deze mogelijkheden zijn beschikbaar ongeacht de manier waarop u de Verzameling van de Media van de Streaming uitvoerde.</p><p>Eerder, was het moeilijk om een bepaalde zitting aan specifieke programma&#39;s nauwkeurig te verbinden wanneer het analyseren van levende inhoud, en het was niet mogelijk om een bepaalde zitting aan individuele onderwerpen of programmasegmenten te binden.</p><p>Voor meer informatie, zie [&#x200B; planningsgegevens uploaden om levende inhoud &#x200B;](https://experienceleague.adobe.com/en/docs/media-analytics/using/media-use-cases/track-schedule-data) te volgen</p> | donderdag 29 oktober 2025 | Eerste helft van 2026<p>(Oorspronkelijk gepland voor vrijgave op 29 oktober 2025)</p> |

## Oplossingen in Customer Journey Analytics

**Analysis Workspace**: AN-423389, AN-423316, AN-422636, AN-422482, AN-422121, AN-42216, AN-422 406271, AN-406188, AN-405997, AN-405983, AN-40577 96, AN-405033, AN-404893, AN-404871, AN-404842, AN-404713, AN-404502, AN-40435 3, AN-404352, AN-404048, AN-403241, AN-402523, AN-400795, AN-396149, AN-39090, AN-390646, AN-383484, AN-376980, AN-371729, AN-347570, AN-404835
**Componenten**:
**Content Analytics**:
**Geleide analyse**: AN-421274
**Uitvoer**:
**meningen van Gegevens**: AN-421891, AN-404627
**Uitvoering**:
**Report Builder**: AN-422120, AN-421937, AN-406296, AN-402951, AN-399748
**het Melden**:
**Segmentatie**:
**Geplande rapporten**: AN-423087, AN-422686
**Gedeelde metriek en dimensies**:
**Andere**: AN-422946, AN-422775, AN-422273, AN-422100, AN-420045, AN-404891, 90912


## Belangrijke kennisgevingen voor Customer Journey Analytics-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. |  |  |

## Gerelateerde bronnen

* [Opmerkingen bij de vorige Customer Journey Analytics-release voor 2025](/help/release-notes/2025.md)
* [&#x200B; de versienota&#39;s van Adobe Analytics &#x200B;](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
* [&#x200B; het stromen de versienota&#39;s van de Inzameling van Media &#x200B;](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [&#x200B; de versienota&#39;s van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
