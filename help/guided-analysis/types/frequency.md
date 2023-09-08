---
title: Frequentieweergave
description: Meet de betrokkenheid per gebruiksfrequentie.
feature: Guided Analysis
keywords: productanalyse
source-git-commit: 1e095720301f3e59e88674d086f5e0de9df88872
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# [!UICONTROL Frequency] weergave

De **[!UICONTROL Frequency]** in deze weergave worden gebeurtenisgegevens gegroepeerd op hoe vaak een gebeurtenis wordt weergegeven. De verticale as van dit rapport bevat emmers die de frequentie van de bekeken gebeurtenis of gebeurtenissen vertegenwoordigen. De horizontale as meet het aantal gebruikers of sessies voor elk emmertje.

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Betrokkenheid**: Volg hoe betrokken gebruikers met om het even welke gebeurtenis zijn. U kunt op een horizontale balk klikken om deze als een segment op te slaan. Segmenten voor onderdelen met een lage betrokkenheid kunnen u helpen bepalen waarom gebruikers niet met de gewenste frequentie op de gebeurtenis reageren. Segmenten voor grote servicemmers kunnen u helpen begrijpen waarom gebruikers vaak met de gebeurtenis werken. Van daar, kunt u andere gebruikers aanmoedigen om gelijkaardig gedrag aan te nemen.
* **Klantenloyaliteit**: Stel de gebeurtenis in op Bestellingen en de metrische waarde op Gebruikers. Met dit rapport kunt u gebruikers groeperen op basis van het aantal keren dat ze een aankoop op uw site hebben gedaan binnen het opgegeven datumbereik.
* **Optimalisatie van ondersteuning**: Het bekijken van dit rapport door het aantal steunvraag of open gevallen kan u inzicht geven waarrond de gebruikers de meeste kwesties ontmoeten. Vervolgens kunt u een segment maken dat zich richt op hun ervaring om te helpen hun problemen te identificeren en op te lossen.
* **Abonnementsdiensten**: Dit rapport is nuttig voor organisaties die abonnementsservices hebben. Gebruikers met een lage betrokkenheid zullen waarschijnlijk vaker terugkeren, zodat u dit rapport kunt bekijken om het gedrag van zeer betrokken gebruikers te analyseren. Als u het gedrag van zeer betrokken gebruikers begrijpt, kan dit hetzelfde gedrag voor weinig betrokken gebruikers aanmoedigen, waardoor het minder waarschijnlijk is dat ze hun abonnement opzeggen.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Events]**: De gebeurtenissen die u wilt meten. Elke geselecteerde gebeurtenis wordt weergegeven als een afzonderlijke grafiek. Aan de tabel wordt een rij toegevoegd die de trended-gebeurtenis vertegenwoordigt. U kunt maximaal vijf gebeurtenissen opnemen.
* **[!UICONTROL People]**: De segmenten die u wilt meten. Elk geselecteerd segment verdubbelt het aantal lijnen in de grafiek en rijen in de lijst. U kunt maximaal vijf segmenten opnemen.

## Diagraminstellingen

De [!UICONTROL Frequency] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Metric]**: De metrische waarde die u wilt meten. Opties omvatten [!UICONTROL Users] en [!UICONTROL Sessions].
* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Opties omvatten [!UICONTROL Horizontal bar] en [!UICONTROL Stacked bar].

## Emmerinstellingen

Bepaalt hoe de gebeurtenis in groepen wordt gecategoriseerd.

* **[!UICONTROL Auto buckets]**: Identificeer automatisch de optimale bucket-grootte op basis van de gegevensdistributie.
* **[!UICONTROL Customized buckets]**: Bepaal hoe het rapport gegevens in emmers groepeert.
   * [!UICONTROL From]: Het eerste emmertje. Frequentie kleiner dan deze waarde wordt niet gerapporteerd.
   * [!UICONTROL To]: De frequentie die groter is dan deze waarde, wordt gegroepeerd in het laatste emmertje.
   * [!UICONTROL Size]: Het emmerinterval.

## Tijdvergelijking toepassen

{{apply-time-comparison}}

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Deze instelling heeft geen invloed op niet-trendweergaven, zoals Frequentie.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
