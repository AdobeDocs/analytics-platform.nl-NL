---
title: Dimensie Lange staart
description: Verklaart de afmetingspost "Lange Staart"en waarom het in rapportering verschijnt.
feature: FAQ
exl-id: 262a219a-315a-4c9b-a400-48cff119d45d
source-git-commit: 5603eef365365cea941ba5b261aeb56e58a84236
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---

# Truncation Warning

Als u een dimensie gebruikt die een groot aantal unieke waarden bevat, verschijnt soms een waarschuwing met de volgende tekst: **[!UICONTROL Results Truncated]**.  Dit betekent dat het gebruik van de rapportagearchitectuur van CJA te veel unieke waarden bevatte om efficiënt te kunnen verwerken en dat de items die het CJA dacht het minst belangrijk waren, werden verwijderd.

## CJA-verwerkingsarchitectuur en unieke waarden

CJA verwerkt rapporten op het tijdstip dat zij in werking worden gesteld, die de gecombineerde dataset aan een aantal servers verdelen. De gegevens per verwerkingsserver worden gegroepeerd door identiteitskaart van de Persoon, betekenend dat één enkele verwerkingsserver alle gegevens voor een bepaalde persoon bevat. Zodra de verwerking is voltooid, stuurt het de subset verwerkte gegevens door naar een aggregatorserver. Alle subsets van verwerkte gegevens worden gecombineerd en geretourneerd in de vorm van een Workspace-rapport.

Als een afzonderlijke server een resultaatset samenvoegt die groter is dan een formaatdrempel, worden de resultaten afgebroken voordat ze worden teruggestuurd.  Dat houdt het netwerkverkeer en de samenvoeging met binnen grenzen om snelle rapportering toe te staan.  Omdat het de resultaten met slechts de mening van het eigen gegeven beknot, is het mogelijk (nochtans onwaarschijnlijk) dat de punten die in Analysis Workspace worden getoond onjuiste metrische waarden hebben.

Hiermee bepaalt u welke items worden verwijderd op basis van de metrische waarde die wordt gebruikt voor sorteren.  Als dit berekende metrisch is, kan het niet duidelijk zijn hoe te om het te sorteren, en zodat kunnen de resultaten minder nauwkeurig zijn.  Wanneer u bijvoorbeeld de inkomsten per bezoeker berekent, worden het totale bedrag aan inkomsten en het totale aantal bezoekers geretourneerd en samengevoegd voordat de afdeling wordt uitgevoerd. Elk knooppunt kiest dus veel items die moeten worden verwijderd zonder echt te weten wat de gevolgen van de resultaten zijn voor het sorteren in zijn geheel.

## Verschillen tussen &#39;Lange liniaal&#39; en &#39;Laag verkeer&#39;

In vorige versies van Analytics werd een andere verwerkingsarchitectuur gebruikt. De gegevens werden verwerkt op het moment dat ze werden verzameld. De punten van Dimension werden geplaatst onder &quot;Laag-Verkeer&quot;nadat een afmeting unieke waarden 500K bereikte, en toepasten agressievere het filtreren bij unieke waarden 1M. Het unieke aantal waarden is opnieuw ingesteld aan het begin van elke kalendermaand. de verwerkte gegevens permanent waren; Er was geen manier om bestaande gegevens uit &quot;Laag-Verkeer&quot; te halen.

In CJA, zijn de afmetingspunten slechts afgebroken als de resultaten van een rapport te groot zijn. De verwerkte gegevens zijn niet permanent, wat betekent dat u de beknotting kunt verminderen of elimineren door uw rapport te wijzigen.

## Het dimensiemenu &#39;Lange staart&#39; verkleinen

Als u de afbreking Lange staart wilt verminderen, raadt Adobe een van de volgende opties aan:

* Een [filter](/help/components/filters/create-filters.md). Filters worden toegepast op het moment dat elke server een subset gegevens verwerkt. Door het aantal unieke waarden dat ze retourneren te beperken, wordt de afbreking &#39;Long Tail&#39; kleiner.
* Gebruik een zoekopdracht.  Als een zoekopdracht wordt gebruikt, worden de items die niet overeenkomen met de zoekopdracht afgekapt, zodat de kans groter is dat de gewenste items worden weergegeven.
* Gebruik een dimensie van de raadplegingsdataset. De dimensies van de dataset van de opzoekopdracht combineren de dimensies van de gebeurtenisdataset, die het aantal unieke teruggekeerde waarden beperken.

Over het algemeen is het moeilijk om een rapport te gebruiken dat te veel unieke dimensie-items bevat. Als u een filter of een dimensie van de raadplegingsdataset toepast, kunt u de &quot;Lange afbreking van het Lusje&quot;verminderen terwijl het maken van uw rapport gemakkelijker te verbruiken.
