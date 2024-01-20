---
title: Wrijvingsweergave
description: Vergelijk de conversiesnelheden tussen de stappen.
exl-id: c8b0b71f-8ed3-4aad-a0f8-4d5ad8d7a7bd
feature: Guided Analysis
keywords: productanalyse
role: User
source-git-commit: 486cd26bfacbae0072e14ec078ceca66909ac0ec
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# [!UICONTROL Friction] weergave

De **[!UICONTROL Friction]** de mening verstrekt een visuele vertegenwoordiging van een kritieke gebruikersreis in uw product. De horizontale as vertegenwoordigt elke stap die een gebruiker moet doorgeven. De verticale as vertegenwoordigt het percentage gebruikers of zittingen bij elke stap. Alle stappen moeten in uiteindelijke volgorde worden uitgevoerd, maar kunnen op elk moment binnen het rapportagevenster plaatsvinden.

>[!VIDEO](https://video.tv.adobe.com/v/3421663/?learn=on)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Conversieanalyse**: U kunt omzettingen in elke fase van de trechter analyseren. Door het aantal gebruikers te volgen die van één stap aan volgende overgaan, kunt u knelpunten identificeren die ongebruikelijke of ongewenste omrekeningskoersen hebben. Deze informatie is nuttig om te begrijpen waar u uw product voor directe resultaten kunt verbeteren.
* **Optimalisatie aan boord**: Optimaliseer het instapproces van uw product door het gebruikersgedrag rond belangrijke gebeurtenissen te bekijken. U kunt aangeven met welke stappen gebruikers worstelen of niet.
* **Aanpassing en betrokkenheid van functies**: Begrijp hoe de gebruikers met specifieke eigenschappen in uw product in wisselwerking staan. Door de progressie van gebruikers door eigenschap-verwante stappen te analyseren, kunt u de tarieven van de eigenschapadoptie beoordelen en gebieden identificeren waar de gebruikers bepaalde eigenschappen zouden kunnen verlaten of ondergebruiken. U kunt deze informatie dan gebruiken om zich op eigenschapverbeteringen te concentreren om adoptiecijfers te verhogen.
* **Campagneevaluatie**: De doeltreffendheid van marketingcampagnes meten. U kunt een segment maken dat zich richt op gebruikers die een bepaalde campagne hebben aangeraakt, en hun omzettingsproces vergelijken met andere campagnes of binnen uw product in het algemeen.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakel tussen dit weergavetype en [Conversietrends](conversion-trends.md).
* **[!UICONTROL Steps]**: De aanraakpunten voor gebeurtenissen die u wilt bijhouden. Elke balk in het diagram vertegenwoordigt een stap. U kunt maximaal tien stappen opnemen.
* **[!UICONTROL Counted as]**: Het bereik dat u op de trechter wilt toepassen. Opties omvatten [!UICONTROL Sessions] en [!UICONTROL Users].
   * [!UICONTROL Sessions]: Alle stappen moeten binnen dezelfde sessie plaatsvinden om te worden geteld.
   * [!UICONTROL Users]: Alle stappen moeten plaatsvinden binnen het geselecteerde rapportagevenster om te worden geteld.
* **[!UICONTROL Segments]**: De segmenten die u wilt vergelijken de trechter over. Elk segment dat is geselecteerd, splitst elke stap in meerdere balken. Elke kleur vertegenwoordigt een ander segment. U kunt maximaal drie segmenten opnemen.

## Diagraminstellingen

De wrijvingsweergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Opties omvatten [!UICONTROL Steps].
* **[!UICONTROL Conversion from]**: Hiermee bepaalt u het percentage van de berekening van stap tot stap. U kunt onder andere de conversie van de [!UICONTROL First step] of [!UICONTROL Previous step].

## Tijdvergelijking

{{apply-time-comparison}}

![Vergelijking van wrijvingstijd](../assets/friction-compare.png)

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Deze instelling heeft geen invloed op niet-trendweergaven, zoals Wrijving.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
