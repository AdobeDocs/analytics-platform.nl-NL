---
title: Aanbevolen werkwijzen voor kenmerken
description: Wat zijn de beste praktijken rond het beslissen over een attributiemodel?
source-git-commit: 3839639858edbd019ef467ca5fb1791f48864100
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Aanbevolen werkwijzen voor kenmerken

Het kiezen van het juiste toewijzingsmodel voor uw organisatie is afhankelijk van een aantal overwegingen. In dit artikel wordt een methodologie en een aantal algemene best practices besproken.

## Stap 1: Verkennende analyse

>[!NOTE]
>Deze analyse moet plaatsvinden voordat u een attributiemodel kiest.

Deze fase bestaat aanvankelijk uit het begrip van klantengedrag en het bepalen van omzettingsmetriek. Op basis van de conversiemetriek maken gereedschappen zoals [Gegevensfeeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html?lang=en) (voor onbewerkte gegevens) of Analysis Workspace het gemakkelijker om te begrijpen

* Hoeveel klanten raken verschillende marketing kanalen alvorens om te zetten?
* De verhouding/verdeling van deze gedragingen.

Bijvoorbeeld, als 50% van klanten 3 kanalen alvorens om te zetten aanraken, is er om het even welke interactie tussen die 3 kanalen?
Vervolgens kon u een analyse van de bovenste en onderste funnel uitvoeren om uw begrip te vergroten.

### Analyse van de bovenfuntrechter

De analyse van de bovenste funnel analyseert kanalen die worden gebruikt om merk of productbewustzijn te creëren. Het doel van de meeste tv-advertenties is bijvoorbeeld merkbewustzijn. U kunt het attributiemodel [&quot;Tijdverlies&quot; gebruiken](/help/analysis-workspace/attribution/models.md), omdat mensen uw tv-advertentie na verloop van tijd zullen vergeten.

### Analyse van de ondertrechter

In deze analyse is de veronderstelling dat mensen al weten wat je merk is en dat ze zich moeten omzetten. Gebruik e-mail- of pushberichten of Facebook-advertenties.

## Stap 2: Toekenning op basis van regels

Het doel van deze stap is uw hypothesen te bevestigen.

**Voorbeeld 1**

Laten we zeggen dat je hypothese is: &quot;Mijn First-touch kanaal heeft meer invloed op de conversie dan mijn laatste aanraakkanaal. Vervolgens gebruikt u het attributiemodel [&quot;Inverse J-shaped&quot;](/help/analysis-workspace/attribution/models.md) om deze hypothese te testen. Dit model geeft 60% van het krediet aan het eerste aanraakpunt.

**Voorbeeld 2**

Uw hypothese kan zijn: &quot;In onze industrie (zoals de reisindustrie), is het attributievenster 60 of 90 dagen, niet 30 dagen, omdat de klanten veel onderzoek doen alvorens een product te kopen. U zou dan uw [lookback venster](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html?lang=en#lookback-windows) in 90 dagen veranderen.

## Stap 3: Algoritmische toewijzing gebruiken

Omdat het zeer moeilijk is om een groot aantal mogelijke hypothesen en combinaties te bevestigen, kunt u [algoritmische attributie](/help/analysis-workspace/attribution/algorithmic.md) gebruiken om dit werk aan ingebouwde algoritmen te verlaten. Als u al het perfecte attributiemodel hebt gevonden dat al uw vragen beantwoordt en een perfecte pasvorm is, dan hoeft u deze stap duidelijk niet te nemen.

## Andere overwegingen

* Misschien moet je de diensten van een data wetenschapper gebruiken in plaats van alleen op Analysis Workspace te vertrouwen.
* U kunt op onbewerkte gegevens vertrouwen, zoals in gegevensfeeds van Adobe.
* U kunt bijvoorbeeld [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=en) gebruiken als u uw Impressiegegevens wilt overwegen.

