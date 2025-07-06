---
title: Aanbevolen werkwijzen voor kenmerken
description: Begrijp de beste praktijken om te beslissen welk attributiemodel aan gebruik.
feature: Attribution
exl-id: 92c6039c-f950-4746-8b34-ba18be258c08
source-git-commit: 1b6e1d432bfe4b0574b8ee68bcfa940941f3c36f
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Aanbevolen werkwijzen voor kenmerken

Het kiezen van het juiste toewijzingsmodel voor uw organisatie is afhankelijk van een aantal overwegingen. In dit artikel wordt een methodologie en een aantal algemene best practices besproken:

* [Verkennende analyse](#exploratory-analysis)
* [Op regels gebaseerde kenmerken](#rule-base-attribution)
* [Algoritmische toewijzing gebruiken](#use-algorithmic-attribution)

## Verkennende analyse

>[!NOTE]
>Deze analyse moet plaatsvinden voordat u een attributiemodel kiest.

Deze fase bestaat aanvankelijk uit het begrip van klantengedrag en het bepalen van omzettingsmetriek. Gebaseerd op de omzettingsmetriek, vergemakkelijken de hulpmiddelen zoals [ de Eendelen van Gegevens ](https://experienceleague.adobe.com/en/docs/analytics/export/analytics-data-feed/data-feed-overview) (voor ruwe gegevens) of Analysis Workspace uw begrip van

* Het aantal klanten dat verschillende marketingkanalen aanraakt voordat ze hun producten converteren
* De verhouding/de verdeling van deze gedragingen

Bijvoorbeeld, als 50% van klanten 3 kanalen alvorens om te zetten aanraken, is er om het even welke interactie tussen die 3 kanalen?
Vervolgens zou je boven- en ondertrechter-analyse kunnen uitvoeren om je begrip te vergroten.

### Analyse van de bovenfuntrechter

Analyekanalen van de bovenste funnel worden gebruikt om merkbekendheid of productbekendheid te geven. Het doel van de meeste tv-advertenties is bijvoorbeeld merkbewustzijn. U zou het [ de attributiemodel van het Verval van de Tijd ](/help/analysis-workspace/attribution/models.md) kunnen gebruiken, aangezien de mensen over uw Tv en in tijd zullen vergeten.

### Analyse van de ondertrechter

In de lagerschalen analyse is de veronderstelling dat mensen al weten wat je merk is en dat je ze wilt omzetten. Gebruik e-mail, pushmeldingen of Facebook-advertenties.

## Toekenning op basis van regels

Het doel van deze stap is uw hypothesen te bevestigen.

**Voorbeeld 1**

Veronderstel dat uw hypothese is: &quot;*Mijn eerste-aanrakingskanaal heeft meer invloed op omzetting dan mijn laatste-aanrakingskanaal.*&quot;

In dit geval, zou u dan het [ Omgekeerde J-Vormige attributiemodel ](/help/analysis-workspace/attribution/models.md) gebruiken om deze hypothese te testen. Dit model geeft 60% van het krediet aan het eerste aanraakpunt.

**Voorbeeld 2**

Stel dat uw hypothese als volgt is: *&quot;In een specifieke branche (zoals de reisindustrie), is het attributievenster 60 of 90 dagen, niet 30 dagen, omdat klanten veel onderzoek doen voordat ze een product kopen.*&quot;

In dit geval, zou u uw [ raadplegingsvenster ](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/attribution/models) in 90 dagen veranderen.

## Algoritmische toewijzing gebruiken

Als u nog geen attributiemodel hebt dat bevredigende antwoorden aan al uw vragen verstrekt, kunt u [ algoritmische attributie ](/help/analysis-workspace/attribution/algorithmic.md) gebruiken. Omdat het erg moeilijk is om een groot aantal mogelijke hypothesen en combinaties te valideren, gebruikt algoritmische attributie ingebouwde algoritmen om krediet over dimensie-items toe te wijzen.

## Andere overwegingen

* Misschien moet je de diensten van een data wetenschapper gebruiken in plaats van alleen op Analysis Workspace te vertrouwen.
* U kunt vertrouwen op onbewerkte gegevens, zoals in Adobe-gegevensfeeds.
* Overweeg gebruikend [ Customer Journey Analytics ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/cja-overview), bijvoorbeeld, als u uw impressiegegevens wilt overwegen.
