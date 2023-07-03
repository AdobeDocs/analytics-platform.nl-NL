---
title: Trechter
description: Gebieden met wrijving identificeren in een reeks stappen.
exl-id: f0ba3f00-bf1f-48db-8b6e-137460abf4f8
feature: Guided Analysis
source-git-commit: edbad9c9d3dc0b48db5334828a18ef652d4a38aa
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Trechter

{{release-limited-testing}}

De **Trechter** [Type analyse](overview.md) biedt een visuele weergave van een kritieke gebruikerstraject in uw product. De horizontale as vertegenwoordigt elke gebeurtenis die een gebruiker in volgorde moet aanraken. De verticale as geeft het percentage weer van de gebruikers of sessies die elke gebeurtenis raakten. Alle aanraakpunten moeten in uiteindelijke volgorde worden uitgevoerd, maar kunnen op elk moment binnen het rapportagevenster plaatsvinden. De gevallen van het gebruik voor dit analysetype omvatten:

* **Conversieanalyse**: Met de trechter kunt u conversies in elke fase van de trechter analyseren. Door het aantal gebruikers te volgen die van één stap aan volgende overgaan, kunt u knelpunten identificeren die ongebruikelijke of ongewenste omzettingspercentages hebben. Deze informatie is nuttig om te begrijpen waar u uw product voor directe resultaten kunt verbeteren.
* **Optimalisatie aan boord**: Trechter is handig om het instapproces van uw product te optimaliseren. Door gebruikersgedrag rond zeer belangrijke gebeurtenissen te onderzoeken, kunt u identificeren welke stappen de gebruikers worstelen met of niet voltooien.
* **Aanpassing en betrokkenheid van functies**: De trechter helpt u begrijpen hoe de gebruikers met specifieke eigenschappen in uw product in wisselwerking staan. Door de progressie van gebruikers door eigenschap-verwante stappen te analyseren, kunt u de tarieven van de eigenschapadoptie beoordelen en gebieden identificeren waar de gebruikers bepaalde eigenschappen zouden kunnen verlaten of ondergebruiken. U kunt deze informatie dan gebruiken om zich op eigenschap of verbeteringen UI te concentreren om adoptietarieven te verhogen.
* **Campagneevaluatie**: Het personeel kan helpen de doeltreffendheid van marketingcampagnes te meten. U kunt een segment maken dat zich richt op gebruikers die een bepaalde campagne hebben aangeraakt, en hun omzettingsproces vergelijken met andere campagnes of binnen uw product in het algemeen.

[Screenshot van de trechter]

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **Stappen**: De aanraakpunten voor gebeurtenissen die u wilt bijhouden. Elke balk in het diagram vertegenwoordigt een stap. U kunt maximaal tien stappen opnemen.
* **Mensen**: De segmenten die u wilt vergelijken de trechter over. Elk segment dat is geselecteerd, splitst elke stap in meerdere balken. Elke kleur vertegenwoordigt een ander segment. U kunt maximaal drie segmenten opnemen.

## Typen weergeven

De trechter biedt de volgende meningstypes aan. U kunt het weergavetype wijzigen met het keuzemenu linksboven in het diagram.

* **Wrijving**: Vergelijk de conversiesnelheden tussen de stappen.

## Diagraminstellingen

De trechter biedt de volgende grafiekmontages aan. U kunt de diagraminstellingen aanpassen in het menu tussen het weergavetype en de kalenderkiezer.

* **Metrisch**: De metrische waarde die u wilt meten. U kunt onder andere sessies en gebruikers kiezen.
* **Type diagram**: Het type visualisatie dat u wilt gebruiken. De enige optie is Stappen.
* **Conversie van**: Hiermee bepaalt u de percentageberekening van stap tot stap. U kunt onder andere de conversie uit de eerste of vorige stap berekenen.

## Datumbereik

De begin- en einddatum. Voorinstellingen voor datumbereik zijn beschikbaar voor uw gemak of u kunt de kalenderkiezer gebruiken om de exacte gewenste datum in te stellen.
