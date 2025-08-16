---
description: In Customer Journey Analytics kunt u real-time rapportagemogelijkheden gebruiken.
title: Real-Time Reporting Overview
feature: Real-time Reporting
hide: true
hidefromtoc: true
role: User
badgePremium: label="Beta"
exl-id: 12fbb760-936d-4e30-958f-764febca5ae7
source-git-commit: b833914e7066fa660f856737d6b8a6392aae2feb
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---

# Overzicht van real-time rapportage

Real-time rapportage in Customer Journey Analytics geeft gegevens en visualisaties in een of meer deelvensters in Analysis Workspace in real-time weer en werkt deze bij.

{{release-limited-testing}}

{{ultimate-package}}

## Gebruik hoofdletters

Deze sectie biedt een overzicht van typische waardevolle en minder waardevolle gebruiksgevallen. En ook informatie wanneer niet om rapportering in real time te overwegen.

* De waardevolste gebruiksgevallen voor real-time rapportering zijn rond grote verkoop, promoties, of productlanceringen.
Als onderdeel van die lancering wilt u weten:

   * Hoe vergelijk de verkoop met je laatste verkoop?
   * Hoe wordt dit product gestart in vergelijking met de laatste productintroductie?
   * Werken uw promoties voor deze belangrijke dag of gebeurtenis eigenlijk?

* Relevante, maar minder waardevolle gebruiksgevallen voor real-time rapportage zijn gevallen waarin validatie wordt gebruikt.
U wilt bijvoorbeeld valideren:

   * Werkt de campagne die u onlangs hebt gelanceerd eigenlijk?
   * Wanneer uw nieuwe productpagina live ging, verzamelt u klantgegevens van de pagina?
   * Gaat uw live media-evenement goed?

Overweeg geen rapportering in real time voor verrichtingen die gebruiksgevallen controleren. Bijvoorbeeld om de vraag te beantwoorden of een plaats behoorlijk werkt. Aangezien [ reëel-tijd verfrist knevel ](use-real-time.md) automatisch na 30 minuten onbruikbaar maakt en het rapport in real time houdt verfrissend, zou u geen rapport in real time als betrouwbare bron voor deze gebruiksgevallen moeten gebruiken.


## Definitie

Het real-time aspect van real-time rapportering voor Customer Journey Analytics wordt gedefinieerd als gegevens en visualisaties die binnen ongeveer 6,5 minuten worden bijgewerkt vanaf het moment dat de onderliggende gegevens door de bijbehorende verbinding worden opgenomen.

Diverse componenten in de opstelling van uw gegevensinzameling bepalen de rapportlatentie in real time.

![ Echt - tijd rapporterend ](assets/real-time-reporting-latencies.svg){zoomable="yes"}

| | Beschrijving | Latentie |
|:---:|---|--:|
| 1 | Gegevens verzameld via Edge Network SDK/API&#39;s in de Edge Network. | &lt; 500 milliseconden |
| 2 | Gegevens die van Edge Network aan de dienst van de gegevensinzameling en bevestiging in de Hub van Experience Platform worden herhaald. | &lt; 5 minuten |
| 3 | Gegevens die door het stromen schakelaars in de dienst van de gegevensinzameling en bevestiging in de Hub van Experience Platform worden verzameld. | &lt; 15 minuten |
| 4 | Gegevens die door Adobe Analytics worden verzameld en door de bron van Analytics schakelaar aan de bronbewerker van schakelaars in de Hub van Experience Platform door:sturen. | &lt; 15 minuten |
| 5 | Gegevens die door andere bronschakelaars in de bronbewerker van schakelaars in de Hub van Experience Platform worden verzameld. | &lt; 24 uur |
| 6 | Gegevens die door de verwerker in real time voor een geconsolideerde dataset voor rapportering in real time worden verwerkt. | &lt; 90 seconden |

## Beperkingen

Houd rekening met de volgende beperking voor real-time rapportage:

* Real-time rapportage rapporteert alleen gegevens die beschikbaar zijn over een voortschrijdende periode van 24 uur. De gegevens die deze het rollen periode van 24 uur kruisen zijn verborgen voor rapportering in real time. Zodra [ reëel-tijd ](use-real-time.md) voor een rapport gehandicapt of automatisch uitgezet verfrist is, zijn alle relevante gegevens voor een rapport beschikbaar opnieuw.
* Attributie, segmentatie, berekende metriek, en meer werken slechts aan de gegevens beschikbaar binnen de rolperiode van 24 uren.
* Real-time rapportage werkt het best op gegevens op gebeurtenis- en sessieniveau en u moet voorzichtig zijn met real-time rapportage voor gegevens op persoonniveau. <!--Need to explain this a bit better --> Aangezien alleen gebeurtenissen vanaf de schuivende periode van 24 uur beschikbaar zijn voor realtime rapporten, is de gebeurtenisgeschiedenis van een persoon ook beperkt tot dit venster. Denk aan de voorkeur voor gegevens op gebeurtenis- en sessieniveau wanneer u een dimensie en (berekende) metriek selecteert. En wanneer u functies zoals onderbrekingen, volgende of vorige, en meer in uw real-time gebruikt verfrist toegelaten paneel.
* U kunt het stitching met real-time rapportering niet combineren. <!-- Do we need to explain this in more detail, why? --> Real-time rapportage heeft betrekking op gegevens op gebeurtenis- en sessieniveau en is minder relevant voor op personen gebaseerde gegevens.
* Er zijn geen hartslagverzamelde mediummetriek beschikbaar, behalve metingen voor het starten van media en het sluiten van media. Zo, kunt u rapportering in real time nog gebruiken om media gebruiksgeval toe te laten.
* Wanneer u de [ download of de uitvoeropties ](/help/analysis-workspace/export/download-send.md) gebruikt om een project te downloaden of gegevens van een vrije vormlijst uit te voeren, overweeg het volgende:
   * Een gedownload CSV-project of geëxporteerd CSV-bestand bevat de realtime gegevens die beschikbaar zijn op het moment van downloaden of exporteren.
   * Een gedownload PDF-project bevat niet-real-time gegevens, vergelijkbaar met de gegevens die worden weergegeven wanneer real-time vernieuwing is uitgeschakeld.
