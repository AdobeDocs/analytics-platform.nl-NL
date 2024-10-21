---
title: Effectanalyse voor eerste gebruik
description: Meet het effect van het gebruik van de eerste functie op sleutelindicatoren.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
exl-id: 2c512184-2d79-4c41-8229-a09e440179ea
role: User
source-git-commit: ad181b5ba3de1a038c661159a159d234da6c3edf
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# [!UICONTROL First use impact] analyse

De ![ FirstUse ](/help/assets/icons/FirstUse.svg) **[!UICONTROL First use impact]** analyse toont een vergelijking van hoe de zeer belangrijke indicatoren vóór en na een gebruiker een producteigenschap voor het eerst uitvoerden. De horizontale as van dit rapport is een relatief tijdinterval voor en na de gebeurtenis, terwijl de verticale as de gewenste toetsindicatoren meet. Een verticale bar in het midden van de grafiek vertegenwoordigt dag 0 voor wanneer een eigenschap voor het eerst door een bepaalde gebruiker wordt gebruikt. Omdat de gebruikers niet altijd eigenschappen op de zelfde dag goedkeuren en uw rollouts kunnen over verscheidene dagen gebeuren, kan dag 0 iets betekenen verschillend voor elke individuele gebruiker.

+++ Video demo

>[!VIDEO](https://video.tv.adobe.com/v/3421661/?learn=on)

+++

![ Eerste gebruikeffect ](../assets/first-use-impact.png)


## Gebruik hoofdletters

De gevallen van het gebruik voor deze analyse omvatten:

* **Nieuwe eigenschapanalyse**: Als u een nieuwe eigenschap binnen uw product lanceert, kunt u vergelijken hoe zeer belangrijke indicatoren vóór en na gebruikers aan die nieuwe eigenschap voor het eerst werden uitgevoerd.
* **Geleidelijke rollouts**: Omdat de analyse eerste gebruik van de eigenschap eerder dan een vaste datum zoekt, is deze analyse nuttig als u de rollout van uw eigenschappen in tijd faseert.
* **Nieuwe analyse van de productversie**: Als u een nieuwe versie van uw product lanceert, kunt u vergelijken hoe zeer belangrijke indicatoren vóór en na gebruikers aan die nieuwe versie voor het eerst werden blootgesteld. Selecteer &quot;om het even welke gebeurtenis&quot;als uw eerste-gebruiksgebeurtenis en filter het aan uw bezit van het Aantal van de Versie.
* **Bestaande eigenschapverbeteringen**: Als u verbeteringen aan een bestaande eigenschap binnen uw product aanbrengt, kunt u vergelijken hoe zeer belangrijke indicatoren vóór en na gebruikers aan die nieuwe verbeteringen voor het eerst werden uitgevoerd. U kunt deze analyse op één of meerdere manieren afhankelijk van uw eigenschapinstrumentatie verwezenlijken.
   * Selecteer een gebeurtenis die de verbetering als uw eerste gebruiksgebeurtenis vertegenwoordigt
   * Selecteer de datum waarop de wijzigingen zijn gestart
   * Segmenteer de analyse aan de groep mensen die aan de verbeteringen worden blootgesteld
* **doeltreffendheid van de Campagne**: Wanneer een gebruiker door van een bepaalde campagne klikt, kunt u vergelijken hoe de belangrijkste indicatoren vóór en na de gebruiker met die campagne interactie hadden uitgevoerd.

## Interface

Zie [ Interface ](../overview.md#interface) voor een overzicht van de Geleide analyseinterface. De volgende instellingen gelden specifiek voor deze analyse:

### Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakelaar tussen deze analyse en [ Versie ](release-impact.md).
* **[!UICONTROL Key indicators]**: De gebeurtenissen die u per gebruiker wilt meten. Elke geselecteerde toetsindicator wordt weergegeven als een gekleurde lijn. Aan de tabel wordt een rij toegevoegd die de gebeurtenis vertegenwoordigt. U kunt maximaal drie gebeurtenissen opnemen.
* **[!UICONTROL Counted as]**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen. De opties zijn [!UICONTROL Events per user] , [!UICONTROL Events] , [!UICONTROL Sessions] en [!UICONTROL Users] .
* **[!UICONTROL Factors]**: Er zijn twee factoren voor deze analyse:
   * **[!UICONTROL Date]**: Hoe ver u wilt beginnen te zoeken naar de eerste keer dat de gebruiksgebeurtenis heeft plaatsgevonden.
   * **[!UICONTROL Event]**: De gebeurtenis die u wilt zoeken voor het eerste gebruik van, om de analyse te centreren.
* **[!UICONTROL Segments]**: Het segment dat u wilt meten. Het geselecteerde segment filtert uw gegevens om zich slechts op de individuen te concentreren die uw segmentcriteria aanpassen. Voor deze analyse wordt één segment ondersteund.

### Diagraminstellingen

De [!UICONTROL First use impact] -analyse biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. U kunt onder andere Lijn kiezen.

### Datumbereik

Datumselecties in de [!UICONTROL First use impact] -analyse werken anders dan andere analyses, omdat de analyse draait om de datum die is opgegeven in de queryrail. De volgende opties zijn beschikbaar:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Geldige opties zijn [!UICONTROL Daily] , [!UICONTROL Weekly] , [!UICONTROL Monthly] en [!UICONTROL Quarterly] . Het wijzigen van het interval heeft invloed op de opties die beschikbaar zijn voor de periode Voor en Na.
* **[!UICONTROL Before and after period]**: De hoeveelheid tijd die moet worden geanalyseerd voor en na de gebeurtenis voor het eerste gebruik die is opgegeven in de querytrack. Welke opties beschikbaar zijn, is afhankelijk van de selectie van [!UICONTROL Interval] .
