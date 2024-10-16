---
title: Trechter
description: Vergelijk de conversiesnelheden tussen de stappen.
exl-id: c8b0b71f-8ed3-4aad-a0f8-4d5ad8d7a7bd
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
role: User
source-git-commit: 8592d6d5d4a9d7b8ac6a40963059d386ec5ee804
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# [!UICONTROL Funnel] weergave

De ![ mening ConversionFunnel ](/help/assets/icons/ConversionFunnel.svg)**[!UICONTROL Funnel]**verstrekt een visuele vertegenwoordiging van een kritieke gebruikersreis in uw product. De horizontale as vertegenwoordigt elke stap die een gebruiker moet doorgeven. De verticale as vertegenwoordigt het percentage gebruikers of zittingen bij elke stap. Alle stappen moeten in uiteindelijke volgorde worden uitgevoerd, maar kunnen op elk moment binnen het rapportagevenster plaatsvinden.

>[!VIDEO](https://video.tv.adobe.com/v/3421663/?learn=on)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **analyse van de Omzetting**: U kunt omzettingen in elk stadium van de trechter, zoals een detailhandelcontrole, rekeningsonderbreking, abonnementsstroom, of één of andere andere andere kritieke reis binnen uw productervaring analyseren. Door het aantal gebruikers te volgen die van één stap aan volgende overgaan, kunt u knelpunten identificeren die ongebruikelijke of ongewenste omrekeningskoersen hebben. Deze informatie is nuttig om te begrijpen waar u uw productreis voor directe resultaten kunt verbeteren.
* **de analyse van de Experimentatie**: U kunt omzettingspercentages over een trechter vergelijken die facultatieve stappen of stappen heeft waar een experiment A/B in werking wordt gesteld. Deze informatie kan u helpen bepalen welke variatie van de trechter tot de hoogste omzettingspercentage leidt zodat u meer gebruikers langs die weg kunt aanmoedigen.
* **het In kaart brengen optimalisering**: Optimaliseer het aan boord gaan van uw product proces door gebruikersgedrag rond zeer belangrijke gebeurtenissen te onderzoeken. U kunt aangeven met welke stappen gebruikers worstelen of niet.
* **de goedkeuring en de overeenkomst van de Eigenschap**: Begrijp hoe de gebruikers met specifieke eigenschappen in uw product in wisselwerking staan. Door de progressie van gebruikers te analyseren via aan functies gerelateerde stappen, kunt u de adoptiefrequenties zien en gebieden identificeren waar gebruikers bepaalde functies wellicht niet gebruiken. U kunt deze informatie dan gebruiken om zich op eigenschapverbeteringen te concentreren om adoptiecijfers te verhogen.
* **de kanaaldoeltreffendheid van de Marketing**: Meet de doeltreffendheid van marketing kanalen. U kunt een segment maken dat zich richt op gebruikers die met verschillende marketingkanalen hebben gewerkt, zoals betaalde zoekopdrachten, weergave, natuurlijke zoekopdrachten of Direct zoeken. Vervolgens kunt u hun reizen vergelijken om te zien welk kanaal leidt tot de beste productresultaten.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakelaar tussen dit meningstype en [ tendensen van de Omzetting ](conversion-trends.md).
* **[!UICONTROL Steps]**: De aanraakpunten voor gebeurtenissen die u wilt bijhouden. Elke balk in het diagram vertegenwoordigt een stap. U kunt maximaal tien stappen opnemen.
   * [!UICONTROL Compare]: Elke stap biedt een optie voor het vergelijken van meerdere gebeurtenissen in één treinstel, waardoor een &quot;forked trechter&quot; ontstaat. Met deze functie kunt u de wrijving van twee ritten naast elkaar vergelijken zonder twee aparte analyses te hoeven maken. Het is handig wanneer er stapopties zijn of er een A/B-experiment wordt uitgevoerd in de trechter. Zie [ Kanaal ](https://experienceleague.adobe.com/en/docs/customer-journey-analytics-learn/tutorials/guided-analysis/funnel) in de leerprogramma&#39;s van de Customer Journey Analytics voor een video die verklaart hoe te om trechters te vergelijken.
* **[!UICONTROL Counted as]**: Het bereik dat u op de trechter wilt toepassen. De opties zijn [!UICONTROL Sessions] en [!UICONTROL Users] .
   * [!UICONTROL Sessions]: alle stappen moeten binnen dezelfde sessie plaatsvinden om te worden geteld.
   * [!UICONTROL Users]: alle stappen moeten plaatsvinden binnen het geselecteerde rapportagevenster om te worden geteld.
* **[!UICONTROL Segments]**: De segmenten waarin u de trechter wilt vergelijken. Elk segment dat is geselecteerd, splitst elke stap in meerdere balken. Elke kleur vertegenwoordigt een ander segment. U kunt maximaal drie segmenten opnemen.

## Diagraminstellingen

De wrijvingsweergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Opties zijn [!UICONTROL Steps] .
* **[!UICONTROL Conversion from]** - Hiermee bepaalt u het percentage van de berekening van stap tot stap. U kunt onder andere de conversie van de [!UICONTROL First step] of [!UICONTROL Previous step] berekenen.

## Tijdvergelijking

{{apply-time-comparison}}

![ de tijdvergelijking van de Wrijving ](../assets/friction-compare.png){style="border:1px solid gray"}

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Deze instelling heeft geen invloed op niet-trendweergaven, zoals Wrijving.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
