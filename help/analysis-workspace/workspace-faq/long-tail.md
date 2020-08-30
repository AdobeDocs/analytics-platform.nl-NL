---
title: Object met lange staart
description: Verklaart de afmetingspunt "Lange Lang"en waarom het in rapportering verschijnt.
translation-type: tm+mt
source-git-commit: e32311ce4975107e1b7ca2cb2eaadc2c68a93c92
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---


# Object met lange staart

Als u een afmeting gebruikt die een groot aantal unieke waarden bevat, kunt u soms een waarde zien in het melden van &quot;Lange Lang&quot;. Deze afmetingspost betekent dat het gebruik van de rapporteringsarchitectuur CJA te veel unieke waarden bevat om te verwerken.

## CJA-verwerkingsarchitectuur en unieke waarden

CJA verwerkt rapporten tegelijkertijd zij in werking worden gesteld, verdelend de gecombineerde dataset aan een aantal servers. De gegevens per verwerkingsserver worden gegroepeerd door identiteitskaart van de Persoon, betekenend dat één enkele verwerkingsserver alle gegevens voor een bepaalde persoon bevat. Zodra het verwerking beëindigt, hanteert het zijn ondergroep van verwerkte gegevens aan een aggregatorserver. Alle ondergroepen van verwerkte gegevens worden gecombineerd en in de vorm van een rapport van de Werkruimte teruggekeerd.

Als om het even welke individuele server die een ondergroep van gegevens verwerkt meer dan 500.000 unieke afmetingspunten ontmoet, keert het de hoogste 500.000 afmetingspunten van zijn eigen ondergroep dan de rest onder &quot;Lange Lusje&quot;terug. Het &#39;Long Tail&#39;-element in een werkruimterapport is het geaggregeerde totaal van de waarden van elke afzonderlijke verwerkingsserver die de unieke waarden van 500K overtroffen.

## Verschillen tussen &quot;lange baan&quot; en &quot;laag verkeer&quot;

In vorige versies van de Analyse van Adobe, werd een verschillende verwerkingsarchitectuur gebruikt. De gegevens werden verwerkt op het moment dat ze werden verzameld. De punten van de afmeting werden geplaatst onder &quot;Laag-Verkeer&quot;nadat een afmeting unieke waarden bereikte 500K, en het toegepaste agressievere filtreren bij unieke waarden 1M. De unieke waardetelling werd teruggesteld aan het begin van elke kalendermaand. de verwerkte gegevens waren permanent; er was geen manier om bestaande gegevens uit &quot;Laag-Verkeer&quot; te halen.

In CJA, worden de afmetingspunten slechts gezet in &quot;Lange Lusje&quot;als een individuele verwerkingsserver meer dan 500K unieke waarden bevat. De verwerkte gegevens zijn niet permanent, zo betekent het dat u het punt van de &quot;Lange Lusje&quot;afmeting kunt verminderen door uw rapport te wijzigen.

## Verminder het punt van de &quot;Lange Lusje&quot;afmeting

Als u het de afmetingspunt van het Lange Lusje wilt verminderen, adviseert Adobe om het even welke volgend:

* Gebruik een segment. De segmenten passen tegelijkertijd elke server een ondergroep van gegevens toe. Het beperken van het aantal unieke waarden die zij terugkeren vermindert het de afmetingspunt van de Lange Lusel.
* Gebruik een dimensie van de raadplegingsdataset. De de gegevenssetdimensies van de raadpleging combineren de punten van de gebeurtenisdatasetafmeting, die het aantal unieke teruggekeerde waarden beperken.

Algemeen, is het moeilijk om een rapport te verbruiken dat meer dan 500K unieke afmetingspunten bevat. Als u een segment of een dimensie van de raadplegingsdataset toepast, kunt u de aanwezigheid van &quot;Lange Lang&quot;verminderen terwijl het maken van uw rapport gemakkelijker te verbruiken. Adobe is van plan om deze ervaring te verbeteren aangezien CJA verder wordt ontwikkeld.
