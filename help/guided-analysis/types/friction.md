---
title: Wrijvingsweergave
description: Vergelijk de conversiesnelheden tussen de stappen.
exl-id: c8b0b71f-8ed3-4aad-a0f8-4d5ad8d7a7bd
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
role: User
source-git-commit: 63dd68d31a9f2b907419fa660904f1dfdacaa0b8
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# [!UICONTROL Friction] weergave

De **[!UICONTROL Friction]** de mening verstrekt een visuele vertegenwoordiging van een kritieke gebruikersreis in uw product. De horizontale as vertegenwoordigt elke stap die een gebruiker moet doorgeven. De verticale as vertegenwoordigt het percentage gebruikers of zittingen bij elke stap. Alle stappen moeten in uiteindelijke volgorde worden uitgevoerd, maar kunnen op elk moment binnen het rapportagevenster plaatsvinden.

>[!VIDEO](https://video.tv.adobe.com/v/3421663/?learn=on)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Conversieanalyse**: U kunt omzettingen in elke fase van de trechter analyseren, bijvoorbeeld een uitchecking in de detailhandel, accountaanmelding, abonnementsstroom of een andere belangrijke reis binnen uw productervaring. Door het aantal gebruikers te volgen die van één stap aan volgende overgaan, kunt u knelpunten identificeren die ongebruikelijke of ongewenste omrekeningskoersen hebben. Deze informatie is nuttig om te begrijpen waar u uw productreis voor directe resultaten kunt verbeteren.
* **Experimentatieanalyse**: U kunt de conversiesnelheden vergelijken in een trechter met optionele stappen of stappen waarin een A/B-experiment wordt uitgevoerd. Deze informatie kan u helpen bepalen welke variatie van de trechter tot de hoogste omzettingspercentage leidt zodat u meer gebruikers langs die weg kunt aanmoedigen.
* **Optimalisatie aan boord**: Optimaliseer het instapproces van uw product door het gebruikersgedrag rond belangrijke gebeurtenissen te bekijken. U kunt aangeven met welke stappen gebruikers worstelen of niet.
* **Aanpassing en betrokkenheid van functies**: Begrijp hoe de gebruikers met specifieke eigenschappen in uw product in wisselwerking staan. Door de progressie van gebruikers te analyseren via aan functies gerelateerde stappen, kunt u de adoptiefrequenties zien en gebieden identificeren waar gebruikers bepaalde functies wellicht niet gebruiken. U kunt deze informatie dan gebruiken om zich op eigenschapverbeteringen te concentreren om adoptiecijfers te verhogen.
* **Efficiëntie van marketingkanalen**: De doeltreffendheid van de afzetkanalen meten. U kunt een segment creëren dat zich op gebruikers concentreert die met verschillende marketing kanalen (b.v. betaalde onderzoek, vertoning, natuurlijk onderzoek, of direct) interactie hadden, en dan hun reizen vergelijken om te zien welk kanaal tot de beste productresultaten leidt.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakel tussen dit weergavetype en [Conversietrends](conversion-trends.md).
* **[!UICONTROL Steps]**: De aanraakpunten voor gebeurtenissen die u wilt bijhouden. Elke balk in het diagram vertegenwoordigt een stap. U kunt maximaal tien stappen opnemen.
   * [!UICONTROL Compare]: Elke stap biedt een optie voor het vergelijken van meerdere gebeurtenissen in één treinstel, waardoor een &quot;forked trechter&quot; ontstaat. Met deze functie kunt u de wrijving van twee ritten naast elkaar vergelijken zonder twee aparte analyses te hoeven maken. Het is handig wanneer er stapopties zijn of er een A/B-experiment wordt uitgevoerd in de trechter.
* **[!UICONTROL Counted as]**: Het bereik dat u op de trechter wilt toepassen. Opties omvatten [!UICONTROL Sessions] en [!UICONTROL Users].
   * [!UICONTROL Sessions]: Alle stappen moeten binnen dezelfde sessie plaatsvinden om te worden geteld.
   * [!UICONTROL Users]: Alle stappen moeten plaatsvinden binnen het geselecteerde rapportagevenster om te worden geteld.
* **[!UICONTROL Segments]**: De segmenten waar u de trechter doorheen wilt vergelijken. Elk segment dat is geselecteerd, splitst elke stap in meerdere balken. Elke kleur vertegenwoordigt een ander segment. U kunt maximaal drie segmenten opnemen.

## Diagraminstellingen

De wrijvingsweergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Opties omvatten [!UICONTROL Steps].
* **[!UICONTROL Conversion from]**: Hiermee bepaalt u het percentage van de berekening van stap tot stap. U kunt onder andere de conversie van de [!UICONTROL First step] of [!UICONTROL Previous step].

## Tijdvergelijking

{{apply-time-comparison}}

![Vergelijking van wrijvingstijd](../assets/friction-compare.png){style="border:1px solid gray"}

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Deze instelling heeft geen invloed op niet-trendweergaven, zoals Wrijving.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
