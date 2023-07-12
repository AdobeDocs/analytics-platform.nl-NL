---
title: Conversietrends
description: Wijzigingen in de conversiesnelheid in de loop der tijd bijhouden.
feature: Guided Analysis
source-git-commit: 84ac8008e4c90250e9f626b8c4d72f20297c14ad
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# Conversietrends

{{release-limited-testing}}

De **Conversietrends** de mening verstrekt een trended visualisatie rond omzettingspercentages in tijd. De horizontale as is een tijdinterval, terwijl de verticale as de omzettingssnelheid vertegenwoordigt. U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Optimalisatie-inspanningen bijhouden**: Na het identificeren van belangrijke knelpunten die u wilt verbeteren het gebruiken [Wrijving](friction.md)kunt u deze weergave gebruiken om te volgen hoe deze optimalisaties de conversiesnelheid in de loop der tijd beïnvloeden.
* **A/B-testevaluatie**: Evalueren van de doeltreffendheid van A/B-tests of -experimenten in de context van een trechter. Door de omrekeningskoersen tussen verschillende variaties te vergelijken, kunt u gemakkelijk bepalen welke tests hogere omrekeningskoersen verstrekken, die tot gegeven-gedreven besluiten leiden waarrond variaties permanent moeten uitvoeren.
* **Campagneevaluatie in de loop der tijd**: De doeltreffendheid van marketingcampagnes in de loop der tijd meten. U kunt een segment maken dat zich richt op gebruikers die een bepaalde campagne hebben aangeraakt, en hun conversietarieven vergelijken met andere campagnes. U kunt de huidige omrekeningskoersen ook vergelijken met vergelijkbare campagnes die in het verleden zijn gevoerd.

![Conversietrends](../assets/conversion-trends.png)

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **Stappen**: De aanraakpunten voor gebeurtenissen die u wilt bijhouden. Elke balk in het diagram vertegenwoordigt een stap. U kunt maximaal tien stappen opnemen.
* **Mensen**: De segmenten die u wilt vergelijken de trechter over. Elk segment dat is geselecteerd, splitst elke stap in meerdere balken. Elke kleur vertegenwoordigt een ander segment. U kunt maximaal drie segmenten opnemen.

## Diagraminstellingen

De weergave Conversietrends biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **Metrisch**: De metrische waarde die u wilt meten. U kunt onder andere sessies en gebruikers kiezen.
* **Type diagram**: Het type visualisatie dat u wilt gebruiken. U kunt onder andere Lijn kiezen.
* **Conversie van**: Hiermee bepaalt u de percentageberekening van stap tot stap. U kunt onder andere de conversie uit de eerste of vorige stap berekenen.

## Tijdvergelijking toepassen

{{apply-time-comparison}}

![Conversietrends tijdvergelijking](../assets/conversion-trends-compare.png)

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **Interval**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **Datum**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
