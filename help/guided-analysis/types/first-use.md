---
title: Weergave voor eerste gebruik
description: Meet het effect van het gebruik van de eerste functie op sleutelindicatoren.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
exl-id: 2c512184-2d79-4c41-8229-a09e440179ea
role: User
source-git-commit: 240a17923b55479865affaafb098b56e32d083a3
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 0%

---

# [!UICONTROL First use] weergave

De **[!UICONTROL First use]** de mening toont een vergelijking van hoe de belangrijkste indicatoren vóór en na een gebruiker een producteigenschap voor het eerst gebruikten. De horizontale as van dit rapport is een relatief tijdinterval voor en na de gebeurtenis, terwijl de verticale as de gewenste toetsindicatoren meet. Een verticale bar in het midden van de grafiek vertegenwoordigt dag 0 voor wanneer een eigenschap voor het eerst door een bepaalde gebruiker wordt gebruikt. Omdat de gebruikers niet altijd eigenschappen op de zelfde dag goedkeuren en uw rollouts kunnen over verscheidene dagen gebeuren, kan dag 0 iets betekenen verschillend voor elke individuele gebruiker.

>[!VIDEO](https://video.tv.adobe.com/v/3421661/?learn=on)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Nieuwe functieanalyse**: Als u een nieuwe functie binnen uw product start, kunt u vergelijken hoe belangrijke indicatoren die voor en na gebruikers voor het eerst aan die nieuwe functie werden blootgesteld, werden uitgevoerd.
* **Gefaseerde rollouts**: Omdat in de analyse wordt gezocht naar het eerste gebruik van de functie in plaats van naar een vaste datum, is deze weergave handig als u de uitrol van de functies in de loop van de tijd geleidelijk wilt uitvoeren.
* **Analyse van nieuwe productversie**: Als u een nieuwe versie van uw product start, kunt u vergelijken hoe belangrijke indicatoren die voor en na gebruikers voor het eerst aan die nieuwe versie werden blootgesteld, werden uitgevoerd. Selecteer &quot;om het even welke gebeurtenis&quot;als uw eerste-gebruiksgebeurtenis en filter het aan uw bezit van het Aantal van de Versie.
* **Verbeteringen voor bestaande functies**: Als u verbeteringen aanbrengt aan een bestaande functie in uw product, kunt u vergelijken hoe de belangrijkste indicatoren die vóór en nadat gebruikers voor het eerst aan die nieuwe verbeteringen werden blootgesteld, werden uitgevoerd. U kunt deze analyse op één of meerdere manieren afhankelijk van uw eigenschapinstrumentatie verwezenlijken.
   * Selecteer een gebeurtenis die de verbetering als uw eerste gebruiksgebeurtenis vertegenwoordigt
   * Selecteer de datum waarop de wijzigingen zijn gestart
   * Segmenteer de analyse aan de groep mensen die aan de verbeteringen worden blootgesteld
* **Doeltreffendheid van campagnes**: Wanneer een gebruiker vanaf een bepaalde campagne door klikt, kunt u vergelijken hoe de belangrijkste indicatoren vóór en na de gebruiker met die campagne interactie hadden uitgevoerd.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakel tussen dit weergavetype en [Geen](release.md).
* **[!UICONTROL Key indicators]**: De gebeurtenissen die u per gebruiker wilt meten. Elke geselecteerde toetsindicator wordt weergegeven als een gekleurde lijn. Aan de tabel wordt een rij toegevoegd die de gebeurtenis vertegenwoordigt. U kunt maximaal drie gebeurtenissen opnemen.
* **[!UICONTROL Counted as]**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen. Opties omvatten [!UICONTROL Events per user], [!UICONTROL Events], [!UICONTROL Sessions], en [!UICONTROL Users].
* **[!UICONTROL Factors]**: Er zijn twee factoren voor deze mening:
   * **[!UICONTROL Date]**: Hoe ver terug u wilt beginnen zoekend de eerste tijd gebruikgebeurtenis om voorgekomen te zijn.
   * **[!UICONTROL Event]**: De gebeurtenis waarop u wilt zoeken, om de analyse te centreren.
* **[!UICONTROL Segments]**: Het segment dat u wilt meten. Het geselecteerde segment filtert uw gegevens om zich slechts op de individuen te concentreren die uw segmentcriteria aanpassen. Voor dit weergavetype wordt één segment ondersteund.

## Diagraminstellingen

De weergave Eerste gebruik biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. U kunt onder andere Lijn kiezen.

## Datumbereik

Datumselecties in de effectanalyse werken anders dan andere analysetypen, aangezien de analyse rond de in de queryrail gespecificeerde datum draait. De volgende opties zijn beschikbaar:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Geldige opties zijn [!UICONTROL Daily], [!UICONTROL Weekly], [!UICONTROL Monthly], en [!UICONTROL Quarterly]. Het wijzigen van het interval heeft invloed op de opties die beschikbaar zijn voor de periode Voor en Na.
* **[!UICONTROL Before and after period]**: De hoeveelheid tijd die moet worden geanalyseerd voor en na de gebeurtenis voor het eerste gebruik die is opgegeven in de querytrack. Welke opties beschikbaar zijn, is afhankelijk van de [!UICONTROL Interval] selectie.
