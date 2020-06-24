---
title: Dimensiewaarde lange staart
description: Verklaart de afmetingswaarde "Lange Staart"en waarom het in rapportering verschijnt.
translation-type: tm+mt
source-git-commit: 8f59697b2bb282a1057267131343229e12dd5111
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---


# Dimensiewaarde lange staart

Als u een dimensie gebruikt die een groot aantal unieke waarden bevat, kunt u soms een waarde zien in het rapporteren van het label &quot;Long Tail&quot;. Deze waarde van de dimensie betekent dat het gebruik van de rapporterende architectuur CJA te veel unieke waarden bevatte om te verwerken.

## CJA-verwerkingsarchitectuur en unieke waarden

CJA verwerkt rapporten op het tijdstip dat zij in werking worden gesteld, die de gecombineerde dataset aan een aantal servers verdelen. De gegevens per verwerkingsserver worden gegroepeerd door identiteitskaart van de Persoon, betekenend dat één enkele verwerkingsserver alle gegevens voor een bepaalde persoon bevat. Zodra de verwerking is voltooid, stuurt het de subset verwerkte gegevens door naar een aggregatorserver. Alle subsets van verwerkte gegevens worden gecombineerd en geretourneerd in de vorm van een Workspace-rapport.

Als een individuele server die een subset van gegevens verwerkt meer dan 500.000 unieke dimensiewaarden ontmoet, keert het de hoogste 500.000 afmetingswaarden van zijn eigen ondergroep terug dan de rest onder &quot;Lange Lang&quot;terug. De waarde van de afmeting &#39;Long Tail&#39; die in een Workspace-rapport wordt gezien, is het geaggregeerde totaal van de waarden van elke afzonderlijke verwerkingsserver die de unieke waarden van 500 kB overschrijden.

## Verschillen tussen &#39;Lange liniaal&#39; en &#39;Laag verkeer&#39;

In eerdere versies van Adobe Analytics werd een andere verwerkingsarchitectuur gebruikt. De gegevens werden verwerkt op het moment dat ze werden verzameld. De waarden van de afmeting werden geplaatst onder &quot;Laag-Verkeer&quot;nadat een afmeting unieke waarden 500K bereikte, en toepasten agressievere het filtreren bij unieke waarden 1M. Het unieke aantal waarden is opnieuw ingesteld aan het begin van elke kalendermaand. de verwerkte gegevens permanent waren; Er was geen manier om bestaande gegevens uit &quot;Laag-Verkeer&quot; te halen.

In CJA worden waarden van dimensies alleen in &#39;Long Tail&#39; geplaatst als een afzonderlijke verwerkingsserver meer dan 500 K unieke waarden bevat. De verwerkte gegevens zijn niet permanent, wat betekent dat u de waarde van de dimensie &quot;Lange staart&quot;kunt verminderen door uw rapport te wijzigen.

## De waarde voor de dimensie &#39;Lange staart&#39; verkleinen

Als u de waarde voor de dimensie &#39;Long Tail&#39; wilt verlagen, raadt Adobe een van de volgende opties aan:

* Gebruik een segment. Segmenten worden toegepast op het moment dat elke server een subset van gegevens verwerkt. Als u het aantal unieke waarden dat ze retourneren, beperkt, wordt de waarde van de &#39;Long Tail&#39;-dimensie verlaagd.
* Gebruik een dimensie van de raadplegingsdataset. De dimensies van de dataset van de opzoekopdracht combineren de dimensies van de gebeurtenisdataset, die het aantal unieke teruggekeerde waarden beperken.

Over het geheel genomen is het moeilijk om een rapport te gebruiken dat meer dan 500K unieke afmetingswaarden bevat. Als u een segment of een dimensie van de raadplegingsdataset toepast, kunt u de aanwezigheid van &quot;Lang Leren&quot;verminderen terwijl het maken van uw rapport gemakkelijker te verbruiken. Adobe is van plan deze ervaring te verbeteren naarmate CJA verder wordt ontwikkeld.
