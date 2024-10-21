---
title: Trends-analyse
description: Meet de betrokkenheid van de gebruiker in de loop van de tijd.
exl-id: b632475f-371e-4156-9ffc-b138325aa120
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
role: User
source-git-commit: f71abfb76a22171004a6f2a501c8ec70d8485478
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# [!UICONTROL Trends] analyse

De ![ GraphTrend ](/help/assets/icons/GraphTrend.svg) **[!UICONTROL Trends]** analyse verstrekt waardevol inzicht rond de prestaties van uw product of het gedrag van uw gebruikers in tijd. De horizontale as van dit rapport is een tijdinterval, terwijl de verticale as uw gewenste gebeurtenissen meet.

+++ Video demo

>[!VIDEO](https://video.tv.adobe.com/v/3421666/?learn=on)

+++

![ Trends vergelijken ](../assets/trends-compare.png)

## Gebruik hoofdletters

De gevallen van het gebruik voor deze analyse omvatten:

* **evalueer productprestaties**: De tendensen staan u toe om de algemene prestaties van uw product over een bepaalde periode te beoordelen. Door metriek zoals gebruikersbetrokkenheid, goedkeuring, of omzettingspercentages te analyseren, kunt u identificeren als de prestaties van uw product verbeteren, stagneren, of verminderen.
* **Goedkeuring van de Eigenschap**: De tendensen staan u toe om te begrijpen hoe de gebruikers nieuwe eigenschappen of updates goedkeuren die u vrijgeeft. U kunt bepalen welke functies populair zijn en welke functies moeten worden verbeterd. Met deze informatie kunt u gegevensgestuurde beslissingen maken over de functies waarmee u prioriteiten kunt stellen bij uw ontwikkelingsinspanningen.
* **gebruikersgedrag**: De tendensen kunnen inzicht in gebruikersgedrag in tijd verstrekken. Door specifieke acties te onderzoeken die de gebruikers nemen, kunt u patronen identificeren waar de gebruikers zouden kunnen wegvallen. U kunt inzichten van deze analyse met [ Trechter ](funnel.md) voor nog meer inzicht rond gedrag combineren.
* **het testen A/B en experimenteren**: Als u tests A/B binnen uw product in werking stelt, kunt u Trends gebruiken om te meten welke tests het meest succesvol in tijd zijn.

## Interface

Zie [ Interface ](../overview.md#interface) voor een overzicht van de Geleide analyseinterface. De volgende instellingen gelden specifiek voor deze analyse:

### Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakelaar tussen deze analyse en [ Frequentie ](frequency.md).
* **[!UICONTROL Events & Metrics]**: De gebeurtenissen of metriek die u wilt meten. Elke selectie wordt weergegeven als een diagramreeks en tabelrij. Gebeurtenissen en metriek kunnen niet in de vraag worden gecombineerd; zodra u uw eerste selectie hebt gemaakt, moeten de resterende vraagselecties van het zelfde type zijn. U kunt maximaal vijf selecties opnemen.
* **[!UICONTROL Counted as]**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen. U kunt onder andere gebeurtenissen, sessies, gebruikers, percentage gebruikers, gebeurtenissen per sessie en gebeurtenissen per gebruiker kiezen. Geladen als opties zijn alleen van toepassing op gebeurtenisquery&#39;s en worden verwijderd voor metrische query&#39;s.
* **[!UICONTROL Segments]**: De segmenten die u wilt meten. Elk geselecteerd segment verdubbelt het aantal grafiekreeksen en lijstrijen. U kunt maximaal vijf segmenten opnemen.
* **[!UICONTROL Breakdown property]**: Verdeelt de diagramreeks en tabelrijen door de waarden van de geselecteerde eigenschap. Eén enkele eigenschap voor de indeling wordt ondersteund. De bovenste 20 waarden worden weergegeven in de tabel en er kunnen maximaal tien waarden worden weergegeven in het diagram. U kunt een rij in de grafiek verbergen of blootstellen door het ![ tonen verborgen pictogram ](../assets/hide-in-chart.png) pictogram te schakelen.

### Diagraminstellingen

De [!UICONTROL Trends] -analyse biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Dit menu bevat de opties Lijn, Staaf, Gestapelde balk en Gestapeld gebied.

### Bedekkingen

Voeg aanvullende gegevens toe aan het diagram. Als er meer dan één reeks zichtbaar is op het diagram, worden alleen bedekkingen weergegeven op de muisaanwijzer.

* **[!UICONTROL Anomaly detection]**: Lopen [ anomalieopsporing ](/help/analysis-workspace/c-anomaly-detection/anomaly-detection.md) op de trended analyse. De uiteinden verschijnen als punten die u over voor meer informatie kunt bewegen.
* **[!UICONTROL Trendline overlay]**: voegt een trendline toe aan het diagram, zodat een duidelijker patroon in de gegevens wordt weergegeven.
   * [!UICONTROL Linear]: hiermee maakt u een rechte regressieregel. Dit is het meest geschikt voor eenvoudige lineaire gegevens die met een constante snelheid toenemen of afnemen. Vergelijking: `y = a + b * x`
   * [!UICONTROL Logarithmic]: hiermee maakt u een kromme regressielijn. Het beste voor gegevens die snel stijgen of dalen, dan wordt meer niveau. Vergelijking: `y = a + b * log(x)`
   * [!UICONTROL Moving average]: maakt een vloeiende trendline op basis van een reeks gemiddelden. Ook gekend als voortschrijdend gemiddelde, gebruikt een voortschrijdend gemiddelde een specifiek aantal vorige gegevenspunten (die door uw selectie worden bepaald), gemiddelden, en gebruikt het gemiddelde als punt in de lijn. Voorbeelden zijn het voortschrijdende gemiddelde over zeven dagen of het voortschrijdende gemiddelde over vier weken. De beschikbare opties voor gemiddelde verplaatsing zijn afhankelijk van het geselecteerde interval en datumbereik.

### Tijdvergelijking

{{apply-time-comparison}}


### Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.

