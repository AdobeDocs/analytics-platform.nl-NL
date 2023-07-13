---
title: Weergave voor eerste gebruik
description: Meet het effect van het gebruik van de eerste functie op sleutelindicatoren.
feature: Guided Analysis
source-git-commit: 9fa4b894e69a25b26632a93f00a655eec8e8aa86
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Weergave voor eerste gebruik

{{release-limited-testing}}

De **Eerste gebruik** In de weergave wordt een vergelijking getoond van de manier waarop toetsindicatoren die voor en na een gebruiker een bepaalde gebeurtenis voor het eerst aanraken. De horizontale as van dit rapport is een relatief tijdinterval voor en na de gebeurtenis, terwijl de verticale as de gewenste toetsindicatoren meet. Een verticale balk in het midden van het diagram geeft aan wanneer de gebeurtenis voor een bepaalde gebruiker heeft plaatsgevonden.

![Geen](../assets/first-use.png)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Nieuwe functieanalyse**: Als u een nieuwe functie binnen uw product start, kunt u vergelijken hoe belangrijke indicatoren die voor en na gebruikers voor het eerst aan die nieuwe functie werden blootgesteld, werden uitgevoerd.
* **Doeltreffendheid van campagnes**: Wanneer een gebruiker een bepaalde campagne bekijkt, kunt u vergelijken hoe de belangrijkste indicatoren vóór en nadat de gebruiker zag of met die campagne in wisselwerking stond.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **Belangrijkste indicatoren**: De gebeurtenissen die u per gebruiker wilt meten. Elke geselecteerde toetsindicator wordt weergegeven als een gekleurde lijn. Aan de tabel wordt een rij toegevoegd die de gebeurtenis vertegenwoordigt. U kunt maximaal drie gebeurtenissen opnemen.
* **Factoren**: Dit standpunt kent twee factoren:
   * **Datum**: Hoe ver terug u voor de eerste keer wilt zoeken een gebeurtenis werd geraakt.
   * **Gebeurtenis**: De gebeurtenis die u voor en na het aangeraakt zijn wilt vergelijken.
* **Mensen**: Het segment dat u wilt meten. Het geselecteerde segment filtert uw gegevens om zich slechts op de individuen te concentreren die uw segmentcriteria aanpassen.

## Diagraminstellingen

De weergave Eerste gebruik biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **Metrisch**: De metrische waarde die u wilt meten. Opties omvatten [!UICONTROL Events per user], [!UICONTROL Events], [!UICONTROL Sessions], en [!UICONTROL Users].
* **Type diagram**: Het type visualisatie dat u wilt gebruiken. U kunt onder andere Lijn kiezen.

## Datumbereik

Datumselecties in effectrapporten werken anders dan andere analysetypen, omdat het rapport draait om een bepaalde gebeurtenis die voor het eerst wordt aangeraakt (opgegeven in de queryrail). De volgende opties zijn beschikbaar:

* **Interval**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Geldige opties zijn [!UICONTROL Daily], [!UICONTROL Weekly], [!UICONTROL Monthly], en [!UICONTROL Quarterly]. Het wijzigen van het interval heeft invloed op de opties die beschikbaar zijn voor de periode Voor en Na.
* **Voor en na de periode**: De hoeveelheid tijd die moet worden geanalyseerd voor en na de aanraakgebeurtenis die is opgegeven in de querytrack. Welke opties beschikbaar zijn, is afhankelijk van de [!UICONTROL Interval] selectie.
