---
title: Frequentieweergave
description: Meet de betrokkenheid per gebruiksfrequentie.
feature: Guided Analysis
keywords: productanalyse
source-git-commit: 645c7913aea309fc52f5a474050406d5e6cbc0e9
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# [!UICONTROL Frequency] weergave

De **[!UICONTROL Frequency]** Hiermee groepeert u gebeurtenisgegevens op basis van hoe vaak gebeurtenissen in uw product voorkomen. De verticale as van deze weergave bevat emmers die de frequentie van de gebeurtenis aangeven. De horizontale as meet het aantal gebruikers of sessies voor elk emmertje.

![Frequentieschermopname](../assets/frequency-stacked.png)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Betrokkenheid**: Volg hoe betrokken gebruikers met om het even welke gebeurtenis in uw product zijn. U kunt op elk gewenst deel van het staafdiagram klikken om het als een segment op te slaan. Segmenten voor onderdelen met een lage betrokkenheid kunnen u helpen bepalen waarom gebruikers niet met de gewenste frequentie op de gebeurtenis reageren. Segmenten voor grote servicemmers kunnen u helpen begrijpen waarom gebruikers vaak met de gebeurtenis werken. Van daar, kunt u andere gebruikers aanmoedigen om gelijkaardig gedrag aan te nemen.
* **Klantenloyaliteit**: Stel de gebeurtenis in op Bestellingen en de metrische waarde op Gebruikers. In deze weergave kunt u gebruikers groeperen op basis van het aantal keren dat zij een aankoop op uw site hebben gedaan binnen het opgegeven datumbereik.
* **Optimalisatie van ondersteuning**: Bekijk het aantal steunvraag of open gevallen door gebruiker om inzicht te krijgen in welke gebruikers de meeste kwesties ontmoeten. Vervolgens kunt u een segment maken dat zich richt op hun ervaring om te helpen hun problemen te identificeren en op te lossen.
* **Abonnementsdiensten**: Gebruikers met een lage betrokkenheid zullen waarschijnlijk eerder afkappen. Als u het gedrag van zeer betrokken gebruikers begrijpt, kan dit hetzelfde gedrag voor weinig betrokken gebruikers aanmoedigen, waardoor het minder waarschijnlijk is dat ze hun abonnement opzeggen.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL Events]**: De gebeurtenissen die u wilt meten. Elke geselecteerde gebeurtenis wordt weergegeven als een afzonderlijke grafiek. Er wordt een rij die de trended-gebeurtenis vertegenwoordigt, aan de tabel toegevoegd. U kunt maximaal vijf gebeurtenissen opnemen.
* **[!UICONTROL People]**: De segmenten die u wilt meten. Elk geselecteerd segment verdubbelt het aantal balken in het diagram en de rijen in de tabel. U kunt maximaal vijf segmenten opnemen.

## Diagraminstellingen

De [!UICONTROL Frequency] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Metric]**: De metrische waarde die u wilt meten. Opties omvatten [!UICONTROL Users],  [!UICONTROL Sessions],  [!UICONTROL Percentage of users] en  [!UICONTROL Percentage of sessions]. De noemer voor op percentage-gebaseerde metriek in deze mening is gebruikers of zittingen die de geselecteerde gebeurtenissen, niet alle actieve gebruikers van het product deden.
* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Opties omvatten [!UICONTROL Horizontal bar] en [!UICONTROL Stacked bar].

## Emmerinstellingen

Bepaalt hoe de gebeurtenis in groepen wordt gecategoriseerd.

* **[!UICONTROL Auto buckets]**: Identificeer automatisch de optimale bucket-grootte op basis van de gegevensdistributie.
* **[!UICONTROL Customized buckets]**: Pas aan hoe de gegevens in emmers zijn gegroepeerd.
   * [!UICONTROL From]: Het eerste emmertje. Frequentie kleiner dan deze waarde wordt niet gerapporteerd.
   * [!UICONTROL To]: De frequentie die groter is dan deze waarde, wordt gegroepeerd in het laatste emmertje.
   * [!UICONTROL Size]: Het emmerinterval.

## Tijdvergelijking toepassen

{{apply-time-comparison}}

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit van de datum waarop u trendgegevens wilt bekijken. Deze instelling heeft geen invloed op niet-trendweergaven, zoals Frequentie.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.