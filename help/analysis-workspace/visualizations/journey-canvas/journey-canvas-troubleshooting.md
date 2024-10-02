---
description: Voorbeelden bij het configureren van de visualisatie van een journaal
title: Voorbeelden van canvas voor reizen
feature: Visualizations
role: User
hide: true
hidefromtoc: true
source-git-commit: c79d1174d78c0bfb1c9b082eb93855bdab4283e4
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Problemen met reiscanvas oplossen

{{release-limited-testing}}

Met de reiscanvasvisualisatie kunt u uitgebreide inzichten analyseren en verkrijgen over de reizen die u aan uw gebruikers en klanten biedt.

Meer over het canvas van de Reis leren, zie {het overzicht van het 0} canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md) en [ vormen een visualisatie van het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md).[


## Verenigbaarheid tussen de metrische en primaire metrische container

U kunt de container van het canvas van de Reis vormen om Persoon (die metrische Mensen) of Zitting (die metrische Sessies gebruikt) te zijn.

Wanneer het kiezen van primaire of secundaire metrisch, zorg ervoor u metrisch kiest die met container metrisch compatibel is die momenteel wordt geselecteerd. De meeste metriek zijn compatibel met de containermetriek die beschikbaar zijn. Sommige combinaties van containermeeteenheden en primaire of secundaire meetwaarden moeten echter worden vermeden.

Bijvoorbeeld, als u Persoon als container met Zitting als primaire of secundaire metrisch gebruikt


| Container | Primair of secundair metrisch | Resultaat |
|---------|----------|---------|
| Mensen | Sessie | Deze combinatie kan leiden tot onbedoelde resultaten. Het resultaat van deze combinatie kan specifiek zijn: |
| A2 | B2 | C2 |
| A3 | B3 | C3 |


## Percentage dat groter is dan 100%

De volgende configuraties kunnen in knopen resulteren die percentages tonen die 100% overschrijden:

* Wanneer het veld **[!UICONTROL Percentage value]** is ingesteld op **[!UICONTROL Percent of total]** of **[!UICONTROL Percent of start node]** en er een primaire metrische waarde is geselecteerd die resulteert in minder gegevens voor het beginknooppunt dan voor volgende knooppunten.

  Bijvoorbeeld, als de Inkomsten als primaire metrisch wordt geselecteerd, en geen opbrengst op primaire metrisch wordt gerealiseerd, dan op om het even welk knooppunt waar de opbrengst wordt gerealiseerd zal tonen als groter dan 100%.

## Knooppunten met een hoger percentage of een hogere waarde dan vorige knooppunten

## Nodes die een hoger percentage of een hogere waarde dan voorafgaande knopen hebben

## Knooppunten die later op de reis komen, hebben een hoger percentage of een hogere waarde dan die van vroeger

## Een knooppunt met een hoger percentage of een hogere waarde dan knooppunten die eraan voorafgaan tijdens de rit

## Knooppunten met een hoger percentage of een hogere waarde dan vorige knooppunten

## Knooppunten

## Een hoger percentage of een hogere waarde in volgende knooppunten

## Een reis die geen trechter-vorm heeft

Het is mogelijk in het canvas van de Reis voor knopen die later op de reis komen om een hoger percentage of aantaltelling te tonen dan knopen die vroeger in de reis komen.

Met andere woorden, in tegenstelling tot in de visualisaties van de Uitval, die altijd trechter-vormig zijn (met participatie die met elke stap vermindert), kunnen de visualisaties van het canvas van de Reis hogere participatie aan recentere stappen van de reis hebben.

Overweeg een reis met de volgende kenmerken:

* De rit bevat drie knooppunten: knooppunt A —> knooppunt B —> knooppunt C

* Het veld **[!UICONTROL Percentage value]** wordt ingesteld op **[!UICONTROL Percent of total]**

* **[!UICONTROL Person]** wordt ingesteld als de container

* **[!UICONTROL Event]** is ingesteld als primaire metrisch

In dit scenario, veronderstel een bezoeker Node A, Knoop B, en toen Knoop C bezocht. Elk van deze bezoeken telt als één enkele gebeurtenis op elke knoop, omdat zij in de orde werden bezocht die door de reis wordt bepaald.

Bij een volgend bezoek aan de site bezoekt de bezoeker alleen Node C, wat resulteert in een extra gebeurtenis op Node C.

In dit geval zouden Nodes A en B elk 1 gebeurtenis en 100% tonen, terwijl Node C 2 gebeurtenissen en 200% zou tonen.

Anderzijds, als Zitting als container werd geplaatst, dan zouden de Nodes A, B, en C elk 1 gebeurtenis en 100% tonen, omdat het verdere bezoek aan de plaats waar de bezoeker slechts Node C bezocht niet aan de reisvereisten zou voldoen, omdat Node A en Node B niet voorafgaand aan het bezoeken Node C werden bezocht.
