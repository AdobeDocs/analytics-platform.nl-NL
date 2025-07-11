---
description: In Customer Journey Analytics kunt u real-time rapportagemogelijkheden gebruiken.
title: Real-Time Reporting Overview
feature: Filters, Segments
hide: true
hidefromtoc: true
role: User
badgePremium: label="Beta"
source-git-commit: 24834f6a1424a885c6f7b3dcf0ad84375e21b462
workflow-type: tm+mt
source-wordcount: '392'
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
   * Hoe is de introductie van dit product te vergelijken met de laatste productintroductie?
   * Werken uw promoties voor deze belangrijke dag of gebeurtenis eigenlijk?

* Relevante, maar minder waardevolle gebruiksgevallen voor echte rapportage zijn gevallen waarin validatie wordt gebruikt.
U wilt bijvoorbeeld valideren:

   * Werkt de campagne-reis, die je onlangs hebt gelanceerd, eigenlijk?
   * Is uw nieuwe productpagina live gegaan en verzamelt u klantgegevens van de pagina?
   * Gaat uw live media-evenement goed?

Overweeg geen rapportering in real time voor verrichtingen die gebruiksgevallen controleren. Bijvoorbeeld om de vraag te beantwoorden of uw plaats eigenlijk werkt?


## Definitie

Het real-time aspect van real-time rapportering voor Customer Journey Analytics wordt gedefinieerd als gegevens en visualisaties die binnen ongeveer 5 minuten worden bijgewerkt vanaf het moment dat de onderliggende gegevens via de bijbehorende verbinding worden opgenomen.

## Beperkingen

Houd rekening met de volgende beperking voor real-time rapportage:

* Real-time rapportage rapporteert alleen gegevens die beschikbaar zijn over een voortschrijdende periode van 24 uur. De gegevens die deze het rollen periode van 24 uur kruisen zijn niet beschikbaar.
* Attributie, segmentatie, berekende metriek, en meer werkt slechts op de gegevens beschikbaar binnen de rolperiode van 24 uren.
* Real-time rapportage werkt het best op gegevens op gebeurtenis- en sessieniveau en u moet voorzichtig zijn met het gebruik van real-time rapportage voor gegevens op persoonniveau. <!--Need to explain this a bit better --> Overweeg de voorkeur voor gegevens op gebeurtenis- en sessieniveau wanneer u afmetingen, (berekende) metriek selecteert. En wanneer u functies zoals storingen, volgende of vorige, en meer in uw real-time gebruikt verfrist toegelaten paneel.
* U kunt het stitching met real-time rapportering niet combineren. <!-- Do we need to explain this in more detail, why? --> Zoals hierboven vermeld, gaat real-time rapportage over gebeurtenis- en sessieniveau-gegevens en niet zozeer over op personen gebaseerde gegevens.
* Er zijn geen hartslagverzamelde mediummetriek beschikbaar, met uitzondering van media start en media close-metriek. Zo kunt u rapportering in real time nog gebruiken om media gebruiksgeval toe te laten.
