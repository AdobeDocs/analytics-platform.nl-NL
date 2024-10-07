---
description: Voorbeelden bij het configureren van de visualisatie van een journaal
title: Voorbeelden van canvas voor reizen
feature: Visualizations
role: User
hide: true
hidefromtoc: true
source-git-commit: cbe713c08269fd3cc4e1076181020ff3fdc947b3
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---

# Problemen met reiscanvas oplossen

{{release-limited-testing}}

Met de reiscanvasvisualisatie kunt u uitgebreide inzichten analyseren en verkrijgen over de reizen die u aan uw gebruikers en klanten biedt.

Meer over het canvas van de Reis leren, zie {het overzicht van het 0} canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md) en [ vormen een visualisatie van het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md).[

De volgende informatie kan u helpen onbedoelde resultaten problemen oplossen u zou kunnen zien, zoals knopen die later in de reis komen die een hoger percentage of aantaltelling dan knopen tonen die vroeger in de reis komen.

## Knooppunten met een hoger percentage of een hogere waarde dan vorige knooppunten

Het is mogelijk in het canvas van de Reis voor knopen die later op de reis komen om een hoger percentage of aantaltelling te tonen dan knopen die vroeger in de reis komen.

Met andere woorden, in tegenstelling tot in de visualisaties van de Uitval, die altijd trechter-vormig zijn (met deelname die met elke stap vermindert), kunnen de visualisaties van het canvas van de Reis aan recentere stappen van de reis dan in vorige stappen meer deelnemen.

Dit kan in de volgende scenario&#39;s voorkomen:

* Wanneer het gebruiken van primaire metrisch buiten Mensen of Zittingen

* Wanneer meerdere paden samenkomen in één knooppunt

### De reis gebruikt een primaire metrisch buiten Mensen of Zitting

Omdat het canvas van de Reizen u toestaat om het even welke metrisch als primaire metrisch te gebruiken, kan dit in knopen resulteren die later in de reis komen om een hoger percentage of aantaltelling te tonen dan knopen die vroeger in de reis komen.

![ Weg met knopen met een hoger percentage dan vorige knoop ](assets/journey-canvas-higher-percentage.png)

De reis die in de volgende scenario&#39;s wordt gebruikt wordt gevormd met deze montages:

* **[!UICONTROL Person]** wordt ingesteld als de container

* **[!UICONTROL Event]** is ingesteld als primaire metrisch

#### Scenario 1: Gebruiker A volgt de weg in de eerste zitting. In een volgende sessie heeft de gebruiker een gebeurtenis die alleen overeenkomt met een later knooppunt.

Stel dat gebruiker A de site bezoekt en de reis voltooit (knooppunt 1: &quot;Visit site&quot; > knooppunt 2: &quot;View Product A&quot; > Node 3: &quot;Check out&quot;). Omdat gebruiker A een gebeurtenis had die elke knoop van de reis in orde aanpaste, wordt een gebeurtenis geteld op elke knoop van de reis.

Stel nu dat gebruiker A de site opnieuw bezoekt in een latere sessie. Omdat de Gebruiker A reeds de reis in een vorige zitting door de reis weg te volgen voltooide, betekent dit dat om het even welke tijdGebruiker A een gebeurtenis heeft die om het even welke knoop in reis-zelfs aanpast als Gebruiker A niet de weg van de reis in hun huidige zitting-een gebeurtenis op de relevante knoop in de reis heeft geteld. Bijvoorbeeld, als Gebruiker A controles uit, dan wordt een gebeurtenis geteld op de knoop van de &quot;Controle uit&quot;. Dit kan in een hoger percentage en een aantal op de knoop van de &quot;Controle uit&quot;dan op de voorafgaande knoop, &quot;Product A van de Mening resulteren.&quot;

In dit voorbeeld speelt de containerinstelling van de reis van &quot;Persoon&quot; een kritieke rol bij het bepalen dat de gebeurtenis op het derde knooppunt (&quot;Uitchecken&quot;) wordt geteld in de volgende sessie.

Als de containerinstelling was ingesteld op &quot;Sessie&quot;, zou de gebeurtenis die alleen plaatsvond op het derde knooppunt in het volgende bezoek, niet in de reis zijn geteld, omdat de tijdens de reis getoonde statistieken zouden worden beperkt tot één gedefinieerde sessie voor een bepaalde persoon. Om meer over container te leren plaatsend, zie [ beginnen met de bouw van een visualisatie van het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md#begin-building-a-journey-canvas-visualization) in het artikel [ vormt een visualisatie van het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md)

<!-- The time allotted for users to move along the path is determined by the container setting. Because "Person" is selected as the container setting in this example, people who followed the journey's path in one session (moving from Node 1 to Node 2 and to Node 3) met the criteria of the journey. On any subsequent visits to the site, any event they have that matches any node on the journey is counted on that node. -->

#### Scenario 2: gebruiker B valt buiten de reis

Stel dat gebruiker B de site bezoekt en de reis niet voltooit (de site bezoekt, Product B bekijkt en vervolgens uitcheckt). In dit geval wordt een gebeurtenis geteld voor het beginknooppunt van de reis, &quot;Visit site&quot;, maar wordt een gebeurtenis niet geteld voor de resterende knooppunten en valt gebruiker B buiten de reis. Hoewel Gebruiker B gecontroleerd, wordt een gebeurtenis niet geteld op de derde knoop (&quot;Controle uit&quot;) omdat Gebruiker B de reis door Product A te bekijken niet voltooide alvorens uit te controleren.

Dit komt doordat gebeurtenissen alleen voor elk knooppunt worden geteld wanneer mensen het &#39;uiteindelijke pad&#39; van de reis volgen. Dit betekent dat gebeurtenissen alleen worden geteld als de persoon uiteindelijk van het ene knooppunt naar het andere wordt verplaatst, ongeacht eventuele gebeurtenissen tussen de twee knooppunten.

### De reis heeft veelvoudige wegen die in één enkele knoop samenkomen

Met het canvas Reis kunt u meerdere beginknooppunten in één rit opnemen, wat resulteert in meerdere paden. Deze wegen kunnen in een gemeenschappelijke knoop samenkomen, resulterend in knopen die later in de reis komen die een hoger percentage of aantaltelling tonen dan knopen die vroeger in de reis komen.

![ Een reis met veelvoudige wegen die in één enkele knoop ](assets/journey-canvas-percentage-converge.png) samenkomen

<!--

The journey used in the following scenarios is configured with the following settings:

* **[!UICONTROL Person]** is set as the container

* **[!UICONTROL Event]** is set as the primary metric

#### Scenario 

When a journey contains multiple paths that converge into a single node, the two paths are combined into the single node using the OR operator. This can result in the

-->

### Reispercentages

Hoewel de getallen op elk knooppunt van een rit constant blijven, ongeacht wat er in het veld **[!UICONTROL Percentage value]** is geselecteerd, kunnen de percentages zelf worden gewijzigd.

In de volgende secties ziet u hoe de percentages voor dezelfde rit kunnen worden gewijzigd, afhankelijk van de volgende opties die u in het veld **[!UICONTROL Percentage value]** hebt geselecteerd:

+++Percentage van beginknooppunt

De knooppunten in deze rit bevatten de volgende statistieken wanneer het veld **[!UICONTROL Percentage value]** is ingesteld op **[!UICONTROL Percent of start node]** :

![ Weg met knopen met een hoger percentage dan vorige knoop ](assets/journey-canvas-higher-percentage.png)

| Knooppunt | Statistieken |
|---------|----------|
| Knooppunt 1 - &quot;Bezoek site&quot; | In deze reis waren er 354.147 evenementen op de site binnen het bereik van de rapporteringsdatum, zoals getoond in het beginknooppunt van de reis, &quot;Visit site&quot;. |
| Knooppunt 2 - &quot;Product A bekijken&quot; | Van het totale aantal gebeurtenissen in het beginknooppunt, stemden 14% (48.394) ervan overeen met de criteria van het tweede knooppunt van de reis, &quot;Product A bekijken&quot;. |
| Knooppunt 3 - &quot;Uitchecken&quot; | Van het totale aantal gebeurtenissen dat in het beginknooppunt wordt getoond, voldeed 32% (113.782) van deze gebeurtenissen aan de criteria van het derde knooppunt van de reis, &quot;Check out.&quot; |

+++

+++Percentage van vorige node

De knooppunten in deze rit bevatten de volgende statistieken wanneer het veld **[!UICONTROL Percentage value]** is ingesteld op **[!UICONTROL Percent of previous node]** :

![ Weg met knopen met een hoger percentage dan vorige knoop ](assets/journey-canvas-percentage-previous.png)

| Knooppunt | Statistieken |
|---------|----------|
| Knooppunt 1 - &quot;Bezoek site&quot; | In deze reis waren er 354.147 evenementen op de site binnen het bereik van de rapporteringsdatum, zoals getoond in het beginknooppunt van de reis, &quot;Visit site&quot;. |
| Knooppunt 2 - &quot;Product A bekijken&quot; | Van het totale aantal gebeurtenissen dat in het vorige knooppunt werd getoond, voldeed 14% (48.394) van deze gebeurtenissen aan de criteria van het tweede knooppunt van de reis, &quot;Product A bekijken&quot;. |
| Knooppunt 3 - &quot;Uitchecken&quot; | Van het totale aantal gebeurtenissen dat in het vorige knooppunt werd weergegeven, voldeed meer dan 100% (113.782) aan de criteria van het derde knooppunt van de reis, &quot;Check out.&quot; |

+++

+++ % van totaal

De knooppunten in deze rit bevatten de volgende statistieken wanneer het veld **[!UICONTROL Percentage value]** is ingesteld op **[!UICONTROL Percent of total]** :

![ Weg met knopen met een hoger percentage dan vorige knoop ](assets/journey-canvas-percentage-total.png)

| Knooppunt | Statistieken |
|---------|----------|
| Knooppunt 1 - &quot;Bezoek site&quot; | In deze reis waren er 354.147 evenementen op de site binnen het bereik van de rapporteringsdatum, zoals getoond in het beginknooppunt van de reis, &quot;Visit site&quot;. |
| Knooppunt 2 - &quot;Product A bekijken&quot; | Van het totale aantal gebeurtenissen, kwam minder dan 1% (48.394) van hen overeen met de criteria van het tweede knooppunt van de reis, &quot;Product A bekijken&quot;. |
| Knooppunt 3 - &quot;Uitchecken&quot; | Van het totale aantal gebeurtenissen, kwam 1% (113.782) van hen overeen met de criteria van het derde knooppunt van de reis, &quot;Check out.&quot; |

+++

## Verenigbaarheid tussen de metrische en primaire metrische container

U kunt de container van het canvas van de Reis vormen om Persoon (die metrische Mensen) of Zitting (die metrische Sessies gebruikt) te zijn.

Zorg ervoor u primaire metrisch kiest die met container metrisch compatibel is die momenteel wordt geselecteerd. De meeste metriek zijn compatibel met de containermetriek die beschikbaar zijn. Sommige combinaties van containermeetgegevens en primaire meetwaarden moeten echter worden vermeden.

Bijvoorbeeld, kan het gebruiken van Persoon als container met Zitting als primaire metrisch in onbedoelde resultaten resulteren.

<!--

## Percentages that exceed 100%

The following configurations can result in nodes that show percentages that exceed 100%:

* When the **[!UICONTROL Percentage value]** field is set to **[!UICONTROL Percent of total]** or **[!UICONTROL Percent of start node]**, and a primary metric is selected that results in less data for the start node than on subsequent nodes.

  For example, if Revenue is selected as the primary metric, and no revenue is being realized on the primary metric, then on any node where revenue is being realized will show as exceeding 100%. 

-->
