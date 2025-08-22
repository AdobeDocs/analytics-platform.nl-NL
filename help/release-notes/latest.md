---
title: Opmerkingen bij de release van Customer Journey Analytics
description: Aanvullende informatie voor de nieuwste versie van Customer Journey Analytics weergeven
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 96fedc9c422b2421e48ff7e41dadcc97a0fe3e6d
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 2%

---

# Huidige Adobe Customer Journey Analytics-releaseopmerkingen (augustus 2025)

**Laatste update**: 14 augustus 2025


Deze releaseopmerkingen hebben betrekking op de periode van 13 augustus tot en met 16 september 2025. De versies van Adobe Customer Journey Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **visualisatie van de Kaart** | De kaartvisualisatie is een visualisatie in Analysis Workspace die u toestaat om een visuele kaart van om het even welke metrisch (met inbegrip van berekende metriek) te bouwen. Het is nuttig om metrische gegevens over verschillende geografische gebieden te identificeren en te vergelijken.<p>Eerder was de kaartvisualisatie alleen beschikbaar in Adobe Analytics.</p><p>De kaartvisualisatie in Customer Journey Analytics bevat de volgende verbeteringen van de kaartvisualisatie in Adobe Analytics:</p><ul><li>Gebruik om het even welk segment van uw gegevensmening als gegevensbron.</li><li>Nauwkeurigheid tot één enkele meter door de afmeting in uw gegevensmening te vormen.</li><li>Met een nieuw selectiegereedschap kunt u een segment, publiek, trend of uitsplitsing maken vanuit elk gebied dat u selecteert in de visualisatie.</li></ul><p>Voor meer informatie, zie [ Kaart ](/help/analysis-workspace/visualizations/map.md).</p> | donderdag 13 augustus 2025 | dinsdag 25 augustus 2025 |
| **B2B malplaatjes** | Als u een licentie aanschaft voor de Customer Journey Analytics B2B edition, zijn de volgende aanvullende B2B-sjablonen nu beschikbaar via de gebruikersinterface van de Adobe-sjablonen: <ul><li>Overzicht van B2B-accountbetrokkenheid</li><li>B2B Overzicht van opportunity Engagement</li><li>B2B Activiteit van kopersgroep</li></ul><p>Voor meer informatie, zie [ B2B malplaatjes ](/help/analysis-workspace/templates/use-templates.md#b2b-templates) in [ malplaatjes van het Gebruik ](/help/analysis-workspace/templates/use-templates.md).</p> |  | zaterdag 15 augustus 2025 |
| **Projecten die als PDFs worden gedownload aan uw werkstation** | Wanneer u een project downloadt als een PDF, wordt de PDF gedownload naar de downloadmap op uw werkstation. <p>Als u eerder een project downloadde als een PDF, werd de PDF gestart op een nieuw browsertabblad met een unieke URL.</p><p>Voor meer informatie, zie [ de projecten en gegevens van de Download ](/help/analysis-workspace/export/download-send.md).</p> |  | dinsdag 25 augustus 2025 |
| **Steun voor adhoc schema&#39;s** | [ Adhoc schema&#39;s ](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/tutorials/ad-hoc) worden gebruikt in diverse werkschema&#39;s van de gegevensopname voor Experience Platform, met inbegrip van het opnemen van CSV- dossiers en het creëren van bepaalde soorten bronverbindingen. <p>Met deze functie wordt ondersteuning geboden voor het gebruik van ad-hocschema&#39;s in Customer Journey Analytics. Als deel van de definitie van een verbinding, kunt u nu een dataset selecteren die op een ad hoc schema wordt gebaseerd en de gegevens in uw gegevensmening en werkruimteprojecten gebruiken.</p> <p>(Koppeling met documentatie die moet worden gevolgd.)</p> |  | vrijdag 28 augustus 2025 |
| **het Uitbreiden van de grens van raadplegingssleutels** | Afhankelijk van uw Customer Journey Analytics-pakket kunt u nu maximaal 1 miljard unieke sleutels in een opzoekgegevensset hebben. <p>Voor meer informatie, zie [ de overdrachtgrenzen van Gegevens ](/help/technotes/guardrails.md#data-transfer-limits) in de [ Guardrails van Customer Journey Analytics ](/help/technotes/guardrails.md) documentatie.</p> |  | zaterdag 29 augustus 2025 |
| **creeer metriek en dimensies die op user-defined kaartgebieden van het schema van het Platform** worden gebaseerd | Door de gebruiker gedefinieerde kaartvelden die u in het Experience Platform-schema definieert, zijn nu beschikbaar voor gebruik in Customer Journey Analytics.<p>U kunt de volgende kaartvelden gebruiken bij het maken van maateenheden en dimensies in Customer Journey Analytics:</p><ul><li>Tekenreeks naar tekenreeks</li><li>Tekenreeks naar geheel getal</li></ul><p>Voor meer informatie, zie [ montages van de Component ](/help/data-views/component-settings/overview.md).</p><p>Voor meer informatie over kaartgebieden in Experience Platform, zie [ kaartgebieden in UI ](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/ui/fields/map) bepalen.</p> |  | Eind augustus 2025 |
| **verwijderde projecten zijn onmiddellijk niet beschikbaar door URL en van geplande leveringen geschrapt** | Projecten die worden verwijderd, worden direct verwijderd uit geplande leveringen en zijn niet meer toegankelijk via de URL.<p>Eerder waren projecten opgenomen in geplande leveringen en konden deze gedurende 60 dagen na het verwijderen worden geopend met hun URL.</p><p>Voor meer informatie over het schrappen van projecten, zie [ Overzicht van Projecten ](/help/analysis-workspace/build-workspace-project/freeform-overview.md).</p> | | Eind augustus 2025 |
| **Echt - tijd rapporterend** | Real-time rapportage in Customer Journey Analytics geeft gegevens en visualisaties in een of meer deelvensters in Analysis Workspace in real-time weer en werkt deze bij.<br/><br/> (Documentatie koppeling naar volgen.) | | 17 september 2025 (oorspronkelijk gepland voor vrijgave op 15 augustus 2025) |
| **Streaming Media: Bijgewerkte gebieden XDM voor het verzamelen van het stromen gegevens van Media in Adobe Experience Platform** | Wanneer het verzamelen van de Gegevens van Media van de Streaming in Adobe Experience Platform, zouden de XDM gebiedspaden onder de rubriek van &quot;Pad van het Gebied XDM&quot;van de Streaming de parameterdocumentatie van Media niet meer moeten worden gebruikt. In plaats daarvan, moeten de klanten die de analytische bronschakelaar uitvoerden om het stromen gegevens van Media in Platform vóór 9 Mei te verzamelen, 2025 hun bestaande configuraties aan mediaReporting gebiedspaden, zoals aangetoond onder de rubriek &quot;het Weg van het Gebied van XDM&quot;van de documentatie van de parameters van Media het Streamen.<p> Deze gebiedspaden worden gevonden op de volgende pagina&#39;s en als &quot;Vervangen&quot;duidelijk: [ Audio en videoparameters ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/audio-video-parameters), [ Advertentieparameters ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/ad-parameters), [ de parameters van het Hoofdstuk ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/chapter-parameters), [ de staatsparameters van de Speler ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/player-state-parameters), en [ de parameters van de Kwaliteit ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/implementation/variables/quality-parameters). (Geen actie wordt vereist voor klanten die de bron van Analytics schakelaar na 9 Mei, 2025 uitvoeren, en reeds mediaReporting XDM wegen gebruiken.)</p><p>Gegevensinvoer op de afgekeurde XDM-veldpaden gaat door tot eind oktober 2025. Na die tijd, zullen de afgekeurde gebiedspaden volledig worden verwijderd en niet meer zichtbaar in het Schema UI van Adobe Experience Platform, en de gegevens zullen worden verzonden slechts gebruikend mediaReporting gebiedspaden.</p><p>Voor meer informatie, zie [ migreren een implementatie van de Verbinding van Analytics Source aan bijgewerkte XDM Streaming Media ](https://experienceleague.adobe.com/nl/docs/media-analytics/using/media-use-cases/xdm-updates/updated-xdm-fields).</p><p>Neem contact op met uw Adobe Consulting Services of accountteam voor ondersteuning van migratie. </p> |  | Oktober 2025 |
| **Stitching in verbindingen** | Vereenvoudigt het stitching van Customer Journey Analytics. In plaats van een dataset te dupliceren en het verbinden op de gedupliceerde dataset toe te passen, wordt nu het stitching gedaan op de opname van gegevens in Customer Journey Analytics, die het vereiste van gedupliceerde datasets en schema&#39;s schrapt. <p>Bovendien in plaats van het moeten het stitching door klantensteun vragen, kunt u het stitching nu van een bijgewerkte UI van Verbindingen in werking stellen.</p><p> *de eerder meegedeelde versiedata worden geduwd toe te schrijven aan extra vereiste inspanningen. De nieuwe releasedata overlappen zich met het vakantieseizoen, dat extra vrijgavebeperkingen introduceert. Een gefaseerde uitrol wordt nu gepland om stabiliteit te verzekeren en verstoring tijdens de vakantieperiode te minimaliseren.*</p> | Eind oktober 2025 | Eind januari 2026 |

## Oplossingen in Customer Journey Analytics

**Analysis Workspace**: AN-389683; AN-389534; AN-389207; AN-389066; AN-388687; AN-388478; AN-387 089; AN-384865; AN-384560; AN-383486; AN-365768; AN-351639
**Componenten**:
**Content Analytics**:
**Geleide Analyse**: AN-384426
**Platform**: AN-384410
**Report Builder**: AN-389336; AN-382775
**het Melden**:
**Segmentatie**:
**Gedeelde metriek en dimensies**:
**Andere**: AN-388222; AN-384898; AN-387169


## Belangrijke kennisgevingen voor Customer Journey Analytics-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. | | |

## Gerelateerde bronnen

* [Opmerkingen bij de vorige Customer Journey Analytics-release voor 2025](/help/release-notes/2025.md)
* [ de versienota&#39;s van Adobe Analytics ](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=nl-NL)
* [ het stromen de versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=nl-NL)
* [ de versienota&#39;s van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl-NL)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
