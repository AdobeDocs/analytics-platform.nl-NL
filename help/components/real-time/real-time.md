---
description: In Customer Journey Analytics kunt u real-time rapportagemogelijkheden gebruiken.
title: Real-Time Reporting Overview
feature: Real-time Reporting
role: User
exl-id: 12fbb760-936d-4e30-958f-764febca5ae7
source-git-commit: 59d48b84ddd34ef161ec0b11f023ccccf9b2e892
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 2%

---

# Overzicht van real-time rapportage

Real-time rapportage in Customer Journey Analytics geeft gegevens en visualisaties in een of meer deelvensters in Analysis Workspace in real-time weer en werkt deze bij.

{{ultimate-package}}

>[!TIP]
>
>Als u gerechtigd bent tot het pakket van Ultimate maar niet [&#x200B; in real time ziet verfrissen knevel &#x200B;](use-real-time.md), creeer een kaartje van de klantenzorg om te verzoeken om rapportering in real time voor uw organisatie toe te laten.


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

Overweeg geen rapportering in real time voor verrichtingen die gebruiksgevallen controleren. Bijvoorbeeld om de vraag te beantwoorden of een plaats behoorlijk werkt. Aangezien [&#x200B; reëel-tijd verfrist knevel &#x200B;](use-real-time.md) automatisch na 30 minuten onbruikbaar maakt en het rapport in real time houdt verfrissend, zou u geen rapport in real time als betrouwbare bron voor deze gebruiksgevallen moeten gebruiken.

## Hoe werkt het

Real-time het melden gebruikt een geconsolideerde dataset die volledig van de [&#x200B; geconsolideerde (gecombineerde) dataset &#x200B;](/help/connections/combined-dataset.md) die voor standaardrapportering wordt gebruikt volledig gescheiden is. U gebruikt [&#x200B; in real time verfrist knevel &#x200B;](use-real-time.md) om tussen te schakelen:

* Real-time rapportage over een geconsolideerde dataset die tot 24 uur aan het rollen gegevens bevat.
* Standaard rapportering over de geconsolideerde dataset die tot 13 maanden van het rollen gegevens (of langer in het geval u de Uitgebreide Toevoeging van de Capaciteit van Gegevens hebt vergunning gegeven) bevat.

![&#x200B; Echt - tijd rapporterend &#x200B;](assets/real-time-reporting-latencies.svg){zoomable="yes"}

### Latenties

Hoe u gegevens verzamelt, bepaalt de latentie van real-time rapportage in Customer Journey Analytics. In de bovenstaande afbeelding en de onderstaande tabel worden bij benadering latentie voor verschillende scenario&#39;s voor gegevensverzameling getoond wanneer real-time en (voor vergelijking) standaardrapportage worden gebruikt.

| | Dataverzameling | Real-time rapporteringslatentie <br/> (ongeveer kleiner dan) | Standaardvertraging bij rapportage <br/> (ongeveer kleiner dan) |
|:---:|---|--:|--:|
| 1 | Edge Network SDK/API&#39;s in de Edge Network | 7 minuten | 95 minuten |
| 2 | Streaming connectors | 17 minuten | 105 minuten |
| 3 | Adobe Analytics-bronaansluiting | 17 minuten | 105 minuten |
| 4 | Andere bronschakelaars in de bronschakelaars (met inbegrip van partijgegevens) | 25 uur | 25 uur |

Als een verstoring van de diensten meer dan een half uur voorkomt, de gegevens in real time niet backfill met gegevens wanneer de kwesties worden opgelost. In plaats daarvan worden real-time gegevens opgehaald vanaf het moment dat de services opnieuw beginnen te werken. Tijdens deze periode worden geen gegevens verloren en zijn nog steeds gegevens beschikbaar met behulp van de standaard rapportagefuncties buiten realtime rapportage.

## Beperkingen

Houd rekening met de volgende beperking voor real-time rapportage:

* Real-time rapportage rapporteert alleen gegevens die beschikbaar zijn over een voortschrijdende periode van 24 uur. Gegevens die groter zijn dan   24-uurs oud is niet beschikbaar voor rapportering in real time. Zodra [&#x200B; in real time &#x200B;](use-real-time.md) voor een rapport gehandicapt of automatisch uitgezet verfrist is, zijn alle relevante gegevens beschikbaar eens meer van de [&#x200B; geconsolideerde dataset &#x200B;](/help/connections/combined-dataset.md) typisch gebruikt voor het melden in Customer Journey Analytics.
* Attributie, segmentatie, berekende metriek, en meer werken slechts aan de gegevens beschikbaar binnen de rolperiode van 24 uren. Bijvoorbeeld, omvat het a *bezoekers* segment zeer weinig mensen in een rapport in real time omdat het rapport slechts mensen omvat die veelvoudige tijden in de laatste 24 uren bezochten. Een gelijkaardige beperking is van toepassing wanneer u een rapport in real time over mensen creeert die eerder op een campagne klikten die niet meer actief is.
* Real-time rapportage werkt het best op gegevens op gebeurtenis- en sessieniveau en u moet voorzichtig zijn met real-time rapportage voor gegevens op persoonniveau. Aangezien alleen gebeurtenissen van de schuivende periode van 24 uur beschikbaar zijn voor realtime rapporten, is de gebeurtenisgeschiedenis van een persoon ook beperkt tot dit venster. Denk aan de voorkeur voor gegevens op gebeurtenis- en sessieniveau wanneer u een dimensie en (berekende) metriek selecteert. En wanneer u functies zoals onderbrekingen, volgende of vorige, en meer in uw real-time gebruikt verfrist toegelaten paneel.
* U kunt het stitching met real-time rapportering niet combineren. Real-time rapportage heeft betrekking op gegevens op gebeurtenis- en sessieniveau en is minder relevant voor gegevens op basis van personen.
* Er zijn geen hartslagverzamelde mediummetriek beschikbaar, behalve metingen voor het starten van media en het sluiten van media. Zo, kunt u rapportering in real time nog gebruiken om media gebruiksgeval toe te laten.
* Wanneer u de [&#x200B; download of de uitvoeropties &#x200B;](/help/analysis-workspace/export/download-send.md) gebruikt om een project te downloaden of gegevens van een vrije vormlijst uit te voeren, overweeg het volgende:
   * Een gedownload CSV-project of geëxporteerd CSV-bestand bevat de realtime gegevens die beschikbaar zijn op het moment van downloaden of exporteren.
   * Een gedownload PDF-project bevat niet-real-time gegevens, vergelijkbaar met de gegevens die worden weergegeven wanneer real-time vernieuwing is uitgeschakeld.
