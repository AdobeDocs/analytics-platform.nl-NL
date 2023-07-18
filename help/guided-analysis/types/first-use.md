---
title: Weergave voor eerste gebruik
description: Meet het effect van het gebruik van de eerste functie op sleutelindicatoren.
feature: Guided Analysis
source-git-commit: 4121c199e4a5050d84f57c69d7fb1d7b05007fcd
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# [!UICONTROL First use] weergave

De **[!UICONTROL First use]** de mening toont een vergelijking van hoe de belangrijkste indicatoren vóór en na een gebruiker een producteigenschap voor het eerst gebruikten. De horizontale as van dit rapport is een relatief tijdinterval voor en na de gebeurtenis, terwijl de verticale as de gewenste toetsindicatoren meet. Een verticale bar in het midden van de grafiek vertegenwoordigt dag 0 voor wanneer een eigenschap voor het eerst door een bepaalde gebruiker wordt gebruikt. Omdat de gebruikers niet altijd eigenschappen op de zelfde dag goedkeuren en uw rollouts kunnen over verscheidene dagen gebeuren, zal dag 0 iets anders voor elke individuele gebruiker betekenen.

Zie de [!UICONTROL First use] weergave in actie

>[!VIDEO](https://video.tv.adobe.com/v/3421661/?learn=on)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Nieuwe functieanalyse**: Als u een nieuwe functie binnen uw product start, kunt u vergelijken hoe belangrijke indicatoren die voor en na gebruikers voor het eerst aan die nieuwe functie werden blootgesteld, werden uitgevoerd.
* **Gefaseerde rollouts**: Aangezien de analyse zoekt naar het eerste gebruik van de functie in plaats van naar een vaste datum, is deze weergave vooral handig als u de functies over een bepaalde periode geleidelijk wilt implementeren.
* **Analyse van nieuwe productversie**: Als u een nieuwe versie van uw product lanceert, kunt u vergelijken hoe zeer belangrijke indicatoren vóór en nadat de gebruikers aan die nieuwe versie voor het eerst werden blootgesteld. Selecteer &quot;om het even welke gebeurtenis&quot;als uw eerste-gebruiksgebeurtenis en filter het aan uw bezit van het Aantal van de Versie.
* **Verbeteringen voor bestaande functies**: Als u verbeteringen aan een bestaande eigenschap binnen uw product aanbrengt, kunt u vergelijken hoe zeer belangrijke indicatoren vóór en nadat de gebruikers aan die nieuwe verbeteringen voor het eerst werden blootgesteld. U kunt deze analyse op een paar manieren uitvoeren afhankelijk van uw eigenschapinstrumentatie. 1) Selecteer een gebeurtenis die de verbetering als uw eerste-gebruikgebeurtenis vertegenwoordigt, en/of 2) selecteer de datum toen de veranderingen begonnen uit te rollen, en/of 3) segmenteer de analyse aan de groep mensen blootgesteld aan de verbeteringen.
* **Doeltreffendheid van campagnes**: Wanneer een gebruiker van een bepaalde campagne door klikt, kunt u vergelijken hoe de zeer belangrijke indicatoren vóór en na de gebruiker met die campagne uitvoerden.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Key indicators]**: De gebeurtenissen die u per gebruiker wilt meten. Elke geselecteerde toetsindicator wordt weergegeven als een gekleurde lijn. Aan de tabel wordt een rij toegevoegd die de gebeurtenis vertegenwoordigt. U kunt maximaal drie gebeurtenissen opnemen.
* **[!UICONTROL Factors]**: Dit standpunt kent twee factoren:
   * **[!UICONTROL Date]**: Hoe ver terug u wilt beginnen zoekend de eerste tijd gebruikgebeurtenis om voorgekomen te zijn.
   * **[!UICONTROL Event]**: De gebeurtenis die u voor eerste gebruik van wilt zoeken, om de analyse te centreren.
* **[!UICONTROL People]**: Het segment dat u wilt meten. Het geselecteerde segment filtert uw gegevens om zich slechts op de individuen te concentreren die uw segmentcriteria aanpassen.

## Diagraminstellingen

De weergave Eerste gebruik biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Metric]**: De metrische waarde die u wilt meten. Opties omvatten [!UICONTROL Events per user], [!UICONTROL Events], [!UICONTROL Sessions], en [!UICONTROL Users].
* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. U kunt onder andere Lijn kiezen.

## Datumbereik

Datumselecties in de effectanalyse werken anders dan andere analysetypen, aangezien de analyse rond de in de queryrail gespecificeerde datum draait. De volgende opties zijn beschikbaar:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Geldige opties zijn [!UICONTROL Daily], [!UICONTROL Weekly], [!UICONTROL Monthly], en [!UICONTROL Quarterly]. Het wijzigen van het interval heeft invloed op de opties die beschikbaar zijn voor de periode Voor en Na.
* **[!UICONTROL Before and after period]**: De hoeveelheid tijd die voor en na de eerste gebruiksgebeurtenis moet worden geanalyseerd die in de querytrack is opgegeven. Welke opties beschikbaar zijn, is afhankelijk van de [!UICONTROL Interval] selectie.
