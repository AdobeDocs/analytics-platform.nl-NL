---
title: Gebruiksweergave
description: Meet de betrokkenheid van de gebruiker in de loop van de tijd.
exl-id: 1d103bd3-3e72-4c82-a534-c896f8433029
feature: Guided Analysis
keywords: productanalyse
source-git-commit: c7a370b4c83ceddcb3ec9542714f768d5562f297
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# [!UICONTROL Usage] weergave

De **[!UICONTROL Usage]** biedt waardevolle inzichten in de prestaties van uw product of het gedrag van uw gebruikers in de loop van de tijd. De horizontale as van dit rapport is een tijdinterval, terwijl de verticale as uw gewenste gebeurtenissen meet.

>[!VIDEO](https://video.tv.adobe.com/v/3421666/?learn=on)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Productprestaties evalueren**: Met trends kunt u de algemene prestaties van uw product gedurende een bepaalde periode beoordelen. Door metriek zoals gebruikersbetrokkenheid, goedkeuring, of omzettingspercentages te analyseren, kunt u identificeren als de prestaties van uw product verbeteren, stagneren, of verminderen.
* **Aanpassing van functies**: Met trends kunt u begrijpen hoe gebruikers nieuwe functies of updates gebruiken die u vrijgeeft. U kunt bepalen welke functies populair zijn en welke functies moeten worden verbeterd. Met deze informatie kunt u gegevensgestuurde beslissingen maken over de functies waarmee u prioriteiten kunt stellen bij uw ontwikkelingsinspanningen.
* **Gebruikersgedrag**: De tendensen kunnen inzicht in gebruikersgedrag in tijd verstrekken. Door specifieke acties te onderzoeken die de gebruikers nemen, kunt u patronen identificeren waar de gebruikers zouden kunnen wegvallen. U kunt vanuit deze weergave inzichten combineren met [Wrijving](friction.md) voor nog meer inzicht in gedrag.
* **A/B-tests en -experimenten**: Als u A/B tests binnen uw product in werking stelt, kunt u Trends gebruiken om te meten welke tests in tijd het meest succesvol zijn.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Events]**: De gebeurtenissen die u wilt meten. Afhankelijk van het diagramtype wordt elke geselecteerde gebeurtenis weergegeven als een gekleurde lijn of een set balken. Aan de tabel wordt een rij toegevoegd die de trended-gebeurtenis vertegenwoordigt. U kunt maximaal vijf gebeurtenissen opnemen.
* **[!UICONTROL People]**: De segmenten die u wilt meten. Elk geselecteerd segment verdubbelt het aantal lijnen in de grafiek en rijen in de lijst. U kunt maximaal vijf segmenten opnemen.

## Diagraminstellingen

De [!UICONTROL Usage] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Metric]**: De metrische waarde die u wilt meten. U kunt onder andere gebeurtenissen, sessies, gebruikers, gebeurtenissen per sessie en gebeurtenissen per gebruiker kiezen.
* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Dit menu bevat de opties Lijn, Staaf, Gestapelde balk en Gestapeld gebied.

## Bedekkingen

Voeg aanvullende gegevens toe aan het diagram.

* **[!UICONTROL Show anomalies]**: Runs [anomaliedetectie](/help/analysis-workspace/virtual-analyst/c-anomaly-detection/anomaly-detection.md) over de trendanalyse. De uiteinden verschijnen als punten die u over voor meer informatie kunt bewegen.

## Tijdvergelijking toepassen

{{apply-time-comparison}}

![Vergelijking van gebruiksduur](../assets/usage-compare.png)

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
