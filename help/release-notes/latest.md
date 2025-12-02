---
title: Opmerkingen bij de release van Customer Journey Analytics
description: Aanvullende informatie voor de nieuwste versie van Customer Journey Analytics weergeven
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 2%

---

# Opmerkingen bij de huidige Customer Journey Analytics-release (oktober 2025)

**Laatste update**: 14 oktober 2025

Deze opmerkingen hebben betrekking op de releaseperiode van oktober tot begin november 2025. De versies van Adobe Customer Journey Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **criteria van de Filter inbegrepen in lijnvisualisaties en sparklines** | Alle zoekfiltercriteria die u toepast op een tabelfilter in vrije vorm worden nu altijd opgenomen in de sparklines. Bovendien kunt u de criteria van de onderzoeksfilter in om het even welke verbonden lijnvisualisatie omvatten.<p>U kunt lijnvisualisaties vormen om de criteria van de onderzoeksfilter te omvatten door sparkline in de metrische kolomkopbal van de verbonden lijst te selecteren.</p><p>Eerder waren de criteria van de onderzoeksfilter niet inbegrepen in vonklines of verbonden lijnvisualisaties.</p><p>Voor meer informatie, zie [ trended gegevens van de Mening voor een vrije vormlijst ](/help/analysis-workspace/visualizations/freeform-table/freeform-table-trended-data.md).</p> | | donderdag 15 oktober 2025 |
| **het verhaal van Gegevens: Produceer diapresentaties van de rapporten van Workspace** | U kunt nu automatisch een diapresentatie genereren (in de .pptx-indeling) die is gebaseerd op een Analysis Workspace-rapport. Workspace detecteert belangrijke inzichten in uw rapport en zet deze om in dia&#39;s die klaar zijn voor belanghebbenden.<p>Deze eigenschap vermindert de tijd en de inspanning die wordt vereist om bevindingen te tonen, uitvoerende verhalen te bouwen, en bedrijfsimpact mee te delen.</p><p>Voor meer informatie, zie [ het verhaal van Gegevens: Produceer diapresentaties van de rapporten van Workspace ](/help/analysis-workspace/curate-share/generate-slides.md).</p> | donderdag 22 oktober 2025 | Januari 2026 |
| **Echt - tijd rapporterend** | [ Echt - tijd rapporterend in Customer Journey Analytics ](/help/components/real-time/real-time.md) vertoningen en updates gegevens en visualisaties binnen één of meerdere panelen in Analysis Workspace in echt - tijd. | 18 september 2025 (oorspronkelijk gepland voor vrijgave op 15 augustus 2025) | donderdag 22 oktober 2025 |
| **Steun voor gegevensspiegel** | Met steun voor model-gebaseerde schema&#39;s en de functionaliteit van de vangst van veranderingsgegevens (CDC) voor specifieke bronschakelaars in Experience Platform, zal Customer Journey Analytics [ functionaliteit van de gegevenspiegel van ](/help/data-mirror/data-mirror.md) kunnen steunen [!DNL Snowflake], [!DNL Azure Databricks], en [!DNL Google BigQuery].<p>Neem contact op met uw Adobe-accountteam voor toegang tot de bètaversie.</p> | Beta-release: 24 september 2025 | TBD |
| **Stitching in verbindingen** | Vereenvoudigt het stitching van Customer Journey Analytics. In plaats van een dataset te dupliceren en het verbinden op de gedupliceerde dataset toe te passen, wordt nu het stitching gedaan op de opname van gegevens in Customer Journey Analytics, die het vereiste van gedupliceerde datasets en schema&#39;s schrapt. <p>Voorts in plaats van het moeten het stitching door klantensteun verzoeken, kunt u het stitching van nu [ van een bijgewerkte UI van Verbindingen ](/help/stitching/use-stitching-ui.md) in werking stellen.</p><p> *de eerder meegedeelde versiedata worden geduwd toe te schrijven aan extra vereiste inspanningen. De nieuwe releasedata overlappen zich met het vakantieseizoen, dat extra vrijgavebeperkingen introduceert. Een gefaseerde uitrol wordt nu gepland om stabiliteit te verzekeren en verstoring tijdens de vakantieperiode te minimaliseren.*</p> | woensdag 28 oktober 2025 | vrijdag 30 april 2026 |
| **Streaming media de diensten: De planningsgegevens van de steun** | U kunt nu geplande gegevens van eerder live streaming media-inhoud uploaden om de viewer eenvoudiger en nauwkeuriger bij te houden.<p>Hieronder volgen voorbeelden van live-inhoud die wordt ondersteund met het uploaden van planningsgegevens:</p><ul><li>SNELLE (Free Ad Supported TV) platforms</li><li>Lokale streams</li><li>Levende sport</li></ul><p>Door planningsgegevens te uploaden, kunt u de viewergegevens bijhouden voor afzonderlijke programma&#39;s die worden uitgevoerd tijdens de tijd die u aangeeft in het uploadbestand. U kunt zelfs kijkersgegevens voor specifieke onderwerpen of programmasegmenten verzamelen.</p><p>Deze mogelijkheden zijn beschikbaar ongeacht de manier waarop u de Verzameling van de Media van de Streaming uitvoerde.</p><p>Eerder, was het moeilijk om een bepaalde zitting aan specifieke programma&#39;s nauwkeurig te verbinden wanneer het analyseren van levende inhoud, en het was niet mogelijk om een bepaalde zitting aan individuele onderwerpen of programmasegmenten te binden.</p><p>Voor meer informatie, zie [ planningsgegevens uploaden om levende inhoud ](https://experienceleague.adobe.com/en/docs/media-analytics/using/media-use-cases/track-schedule-data) te volgen</p> | donderdag 29 oktober 2025 | Eerste helft van 2026<p>(Oorspronkelijk gepland voor vrijgave op 29 oktober 2025)</p> |
| **Analytics bronschakelaar: De de rapportreeksen van het Onderzoek in Experience Platform** | Als u een hoog aantal rapportsuites hebt kunt u [ naar de rapportreeks ](/help/data-ingestion/analytics.md#set-up-an-adobe-analytics-source-connector) nu zoeken u met binnen het gegevensbestand van de Schakelaar van Source van de Analyse wilt verbinden. | | vrijdag 30 oktober 2025 |
| **Streaming Media: Bijgewerkte gebieden XDM voor het verzamelen van het stromen gegevens van Media in Adobe Experience Platform** | Wanneer het verzamelen van de Gegevens van Media van de Streaming in Adobe Experience Platform, zouden de XDM gebiedspaden onder de rubriek van &quot;Pad van het Gebied XDM&quot;van de Streaming de parameterdocumentatie van Media niet meer moeten worden gebruikt. In plaats daarvan, moeten de klanten die de analytische bronschakelaar uitvoerden om het stromen gegevens van Media in Platform vóór 9 Mei te verzamelen, 2025 hun bestaande configuraties aan mediaReporting gebiedspaden, zoals aangetoond onder de rubriek &quot;het Weg van het Gebied van XDM&quot;van de documentatie van de parameters van Media het Streamen.<p> Deze gebiedspaden worden gevonden op de volgende pagina&#39;s en als &quot;Vervangen&quot;duidelijk: [ Audio en videoparameters ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/audio-video-parameters), [ Advertentieparameters ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/ad-parameters), [ de parameters van het Hoofdstuk ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/chapter-parameters), [ de staatsparameters van de Speler ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/player-state-parameters), en [ de parameters van de Kwaliteit ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/variables/quality-parameters). (Geen actie wordt vereist voor klanten die de bron van Analytics schakelaar na 9 Mei, 2025 uitvoeren, en reeds mediaReporting XDM wegen gebruiken.)</p><p>Gegevensinvoer op de afgekeurde XDM-veldpaden gaat door tot eind oktober 2025. Na die tijd, zullen de afgekeurde gebiedspaden volledig worden verwijderd en niet meer zichtbaar in het Schema UI van Adobe Experience Platform, en de gegevens zullen worden verzonden slechts gebruikend mediaReporting gebiedspaden.</p><p>Voor meer informatie, zie [ migreren een implementatie van de Verbinding van Analytics Source aan bijgewerkte XDM Streaming Media ](https://experienceleague.adobe.com/en/docs/media-analytics/using/media-use-cases/xdm-updates/updated-xdm-fields).</p><p>Neem contact op met uw Adobe Consulting Services of accountteam voor ondersteuning van migratie. </p> |  | Oktober 2025 |

## Oplossingen in Customer Journey Analytics

**Analysis Workspace**: AN-400507, AN-400265, AN-399209, AN-397146, AN-394992, AN-390795
**Componenten**:
**Content Analytics**:
**de Uitvoer**: AN-399012, AN-388578
**Geleide Analyse**:
**Uitvoering**: AN-397551, AN-397550, AN-397190, AN-396127
**Report Builder**: AN-401127, AN-400618, AN-392971, AN-391692
**het Melden**:
**Segmentatie**:
**Geplande rapporten**:
**Gedeelde metriek en dimensies**:
**Andere**:


## Belangrijke kennisgevingen voor Customer Journey Analytics-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. | | |

## Gerelateerde bronnen

* [Opmerkingen bij de vorige Customer Journey Analytics-release voor 2025](/help/release-notes/2025.md)
* [ de versienota&#39;s van Adobe Analytics ](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
* [ het stromen de versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [ de versienota&#39;s van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
