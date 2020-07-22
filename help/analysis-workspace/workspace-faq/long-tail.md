---
title: Dimensie Lange staart
description: Verklaart de afmetingspost "Lange Staart"en waarom het in rapportering verschijnt.
translation-type: tm+mt
source-git-commit: e32311ce4975107e1b7ca2cb2eaadc2c68a93c92
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---


# Dimensie Lange staart

Als u een dimensie gebruikt die een groot aantal unieke waarden bevat, kunt u soms een waarde zien in het rapporteren van het label &quot;Long Tail&quot;. Deze dimensie-item houdt in dat de CJA-rapportagearchitectuur teveel unieke waarden gebruikt om te verwerken.

## CJA-verwerkingsarchitectuur en unieke waarden

CJA verwerkt rapporten op het tijdstip dat zij in werking worden gesteld, die de gecombineerde dataset aan een aantal servers verdelen. De gegevens per verwerkingsserver worden gegroepeerd door identiteitskaart van de Persoon, betekenend dat één enkele verwerkingsserver alle gegevens voor een bepaalde persoon bevat. Zodra de verwerking is voltooid, stuurt het de subset verwerkte gegevens door naar een aggregatorserver. Alle subsets van verwerkte gegevens worden gecombineerd en geretourneerd in de vorm van een Workspace-rapport.

Als om het even welke individuele server die een ondergroep van gegevens verwerkt meer dan 500.000 unieke afmetingspunten ontmoet, keert het de hoogste 500.000 afmetingspunten van zijn eigen ondergroep terug dan de rest onder &quot;Lange Lang&quot;terugkeert. Het afmetingsitem Lange staart dat in een werkruimterapport wordt weergegeven, is het geaggregeerde totaal van de waarden van elke afzonderlijke verwerkingsserver die de unieke waarden van 500 kB overschrijden.

## Verschillen tussen &#39;Lange liniaal&#39; en &#39;Laag verkeer&#39;

In eerdere versies van Adobe Analytics werd een andere verwerkingsarchitectuur gebruikt. De gegevens werden verwerkt op het moment dat ze werden verzameld. De punten van de afmeting werden geplaatst onder &quot;Laag-Verkeer&quot;nadat een afmeting unieke waarden 500K bereikte, en toepaste agressievere filtratie bij unieke waarden 1M. Het unieke aantal waarden is opnieuw ingesteld aan het begin van elke kalendermaand. de verwerkte gegevens permanent waren; Er was geen manier om bestaande gegevens uit &quot;Laag-Verkeer&quot; te halen.

In CJA, worden de afmetingspunten slechts gezet in &quot;Lange Lang&quot;als een individuele verwerkingsserver meer dan 500K unieke waarden bevat. De verwerkte gegevens zijn niet permanent, wat betekent dat u het &quot;Lange Lusje&quot;afmetingspunt kunt verminderen door uw rapport te wijzigen.

## Het dimensiemenu &#39;Lange staart&#39; verkleinen

Als u het afmetingsitem Lange staart wilt verkleinen, raadt Adobe een van de volgende opties aan:

* Gebruik een segment. Segmenten worden toegepast op het moment dat elke server een subset van gegevens verwerkt. Door het aantal unieke waarden dat ze retourneren te beperken, wordt het item voor de dimensie &#39;Long Tail&#39; kleiner.
* Gebruik een dimensie van de raadplegingsdataset. De dimensies van de dataset van de opzoekopdracht combineren de dimensies van de gebeurtenisdataset, die het aantal unieke teruggekeerde waarden beperken.

Over het geheel genomen is het moeilijk om een rapport te gebruiken dat meer dan 500K unieke dimensiepunten bevat. Als u een segment of een dimensie van de raadplegingsdataset toepast, kunt u de aanwezigheid van &quot;Lang Leren&quot;verminderen terwijl het maken van uw rapport gemakkelijker te verbruiken. Adobe is van plan deze ervaring te verbeteren naarmate CJA verder wordt ontwikkeld.
