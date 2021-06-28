---
title: Dimensie Lange staart
description: Verklaart de afmetingspost "Lange Staart"en waarom het in rapportering verschijnt.
exl-id: 262a219a-315a-4c9b-a400-48cff119d45d
source-git-commit: 8cee89a8ed656ad6376e64c8327aa7c94a937ce9
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Dimensie Lange staart

Als u een dimensie gebruikt die een groot aantal unieke waarden bevat, kunt u soms een waarde in het melden van geëtiketteerde **[!UICONTROL Long Tail]** zien. Deze dimensie-item houdt in dat de CJA-rapportagearchitectuur teveel unieke waarden gebruikt om te verwerken.

## CJA-verwerkingsarchitectuur en unieke waarden

CJA verwerkt rapporten op het tijdstip dat zij in werking worden gesteld, die de gecombineerde dataset aan een aantal servers verdelen. De gegevens per verwerkingsserver worden gegroepeerd door identiteitskaart van de Persoon, betekenend dat één enkele verwerkingsserver alle gegevens voor een bepaalde persoon bevat. Zodra de verwerking is voltooid, stuurt het de subset verwerkte gegevens door naar een aggregatorserver. Alle subsets van verwerkte gegevens worden gecombineerd en geretourneerd in de vorm van een Workspace-rapport.

Als een individuele server die een subset van gegevens verwerkt meer dan 500.000 unieke afmetingspunten ontmoet, keert het de hoogste 500.000 afmetingspunten van zijn eigen ondergroep terug, dan keert de rest onder &#39;[!UICONTROL Long Tail]&#39; terug. Het &#39;[!UICONTROL Long Tail]&#39; dimensie-item dat in een Workspace-rapport wordt weergegeven, is het geaggregeerde totaal van de waarden van elke afzonderlijke verwerkingsserver die de unieke waarden van 500 kB overschrijden.

## Verschillen tussen &#39;Lange liniaal&#39; en &#39;Laag verkeer&#39;

In vorige versies van Analytics werd een andere verwerkingsarchitectuur gebruikt. De gegevens werden verwerkt op het moment dat ze werden verzameld. De punten van Dimension werden geplaatst onder &quot;Laag-Verkeer&quot;nadat een afmeting unieke waarden 500K bereikte, en toepasten agressievere het filtreren bij unieke waarden 1M. Het unieke aantal waarden is opnieuw ingesteld aan het begin van elke kalendermaand. de verwerkte gegevens permanent waren; Er was geen manier om bestaande gegevens uit &quot;Laag-Verkeer&quot; te halen.

In CJA, worden de afmetingspunten slechts gezet in &quot;Lange Lang&quot;als een individuele verwerkingsserver meer dan 500K unieke waarden bevat. De verwerkte gegevens zijn niet permanent, wat betekent dat u het &quot;Lange Lusje&quot;afmetingspunt kunt verminderen door uw rapport te wijzigen.

## Het dimensiemenu &#39;Lange staart&#39; verkleinen

Als u het afmetingsitem Lange staart wilt verkleinen, raadt Adobe een van de volgende opties aan:

* Gebruik een [filter](/help/components/filters/create-filters.md). Filters worden toegepast op het moment dat elke server een subset gegevens verwerkt. Door het aantal unieke waarden dat ze retourneren te beperken, wordt het item voor de dimensie &#39;Long Tail&#39; kleiner.
* Gebruik een dimensie van de raadplegingsdataset. De dimensies van de dataset van de opzoekopdracht combineren de dimensies van de gebeurtenisdataset, die het aantal unieke teruggekeerde waarden beperken.

Over het geheel genomen is het moeilijk om een rapport te gebruiken dat meer dan 500K unieke dimensiepunten bevat. Als u een filter of een dimensie van de raadplegingsdataset toepast, kunt u de aanwezigheid van &quot;Lang Leren&quot;verminderen terwijl het maken van uw rapport gemakkelijker te verbruiken. Adobe is voornemens deze ervaring te verbeteren naarmate de CJA verder wordt ontwikkeld.
