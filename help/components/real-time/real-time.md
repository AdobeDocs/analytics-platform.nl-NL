---
description: In Customer Journey Analytics kunt u real-time rapportagemogelijkheden gebruiken.
title: Real-Time Reporting Overview
feature: Filters, Segments
hide: true
hidefromtoc: true
role: User
badgePremium: label="Beta"
exl-id: 12fbb760-936d-4e30-958f-764febca5ae7
source-git-commit: edc5e96b8c55f785fd8b2ed04ace1944ecf3947d
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

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

   * Werkt de campagne die je onlangs hebt gelanceerd?
   * Wanneer uw nieuwe productpagina live ging, verzamelt u klantgegevens van de pagina?
   * Gaat uw live media-evenement goed?

Overweeg geen rapportering in real time voor verrichtingen die gebruiksgevallen controleren. Bijvoorbeeld om de vraag te beantwoorden: werkt een site eigenlijk?


## Definitie

Het real-time aspect van real-time rapportering voor Customer Journey Analytics wordt gedefinieerd als gegevens en visualisaties die binnen ongeveer 5 minuten worden bijgewerkt vanaf het moment dat de onderliggende gegevens via de bijbehorende verbinding worden opgenomen.

## Beperkingen

Houd rekening met de volgende beperking voor real-time rapportage:

* Real-time rapportage rapporteert alleen gegevens die beschikbaar zijn over een voortschrijdende periode van 24 uur. De gegevens die deze het rollen periode van 24 uur kruisen zijn niet beschikbaar.
* Attributie, segmentatie, berekende metriek, en meer werken slechts aan de gegevens beschikbaar binnen de rolperiode van 24 uren.
* Real-time rapportage werkt het best op gegevens op gebeurtenis- en sessieniveau en u moet voorzichtig zijn met real-time rapportage voor gegevens op persoonniveau. <!--Need to explain this a bit better --> Aangezien alleen gebeurtenissen vanaf de schuivende periode van 24 uur beschikbaar zijn voor realtime rapporten, is de gebeurtenisgeschiedenis van een persoon ook beperkt tot dit venster. Houd rekening met de voorkeur voor gegevens op gebeurtenis- en sessieniveau wanneer u afmetingen (berekende) kiest. En wanneer u functies zoals onderbrekingen, volgende of vorige, en meer in uw real-time gebruikt verfrist toegelaten paneel.
* U kunt het stitching met real-time rapportering niet combineren. <!-- Do we need to explain this in more detail, why? --> Zoals hierboven vermeld, gaat real-time rapportage over gebeurtenis- en sessieniveau-gegevens en niet zozeer over op personen gebaseerde gegevens.
* Er zijn geen hartslagverzamelde mediummetriek beschikbaar, met uitzondering van media start en media close-metriek. Zo kunt u rapportering in real time nog gebruiken om media gebruiksgeval toe te laten.
