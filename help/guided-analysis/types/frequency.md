---
title: Frequentieanalyse
description: Meet de betrokkenheid per gebruiksfrequentie.
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
exl-id: 27eaa7c7-f1e1-4cf1-9d59-67ac552eb430
role: User
source-git-commit: 7ccc9f28acf08fb49d86005abb7fbb648a1564ce
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# [!UICONTROL Frequency] analyse

De ](/help/assets/icons/Histogram.svg) **[!UICONTROL Frequency]** analysegroepen van de frequentie ![ frequentie {gebeurtenisgegevens door hoe vaak de gebeurtenissen in uw product voorkomen. De verticale as van deze analyse bevat emmers die de frequentie van de gebeurtenis vertegenwoordigen. De horizontale as meet het aantal gebruikers of sessies voor elk emmertje.

>[!VIDEO](https://video.tv.adobe.com/v/3428089/?learn=on)

## Gebruik hoofdletters

De gevallen van het gebruik voor deze analyse omvatten:

* **Betrokkenheid**: Spoor hoe betrokken gebruikers met om het even welke gebeurtenis in uw product zijn. U kunt op elk gewenst deel van het staafdiagram klikken om het als een segment op te slaan. Segmenten voor onderdelen met een lage betrokkenheid kunnen u helpen bepalen waarom gebruikers niet met de gewenste frequentie op de gebeurtenis reageren. Segmenten voor grote servicemmers kunnen u helpen begrijpen waarom gebruikers vaak met de gebeurtenis werken. Van daar, kunt u andere gebruikers aanmoedigen om gelijkaardig gedrag aan te nemen.
* **loyaliteit van de Klant**: Plaats de gebeurtenis aan Orden en metrisch aan Gebruikers. Met deze analyse kunt u gebruikers groeperen op basis van het aantal keren dat zij een aankoop op uw site hebben gedaan binnen het opgegeven datumbereik.
* **optimalisering van de Steun**: Bekijk het aantal steunvraag of open gevallen door gebruiker om inzicht te krijgen in welke gebruikers de meeste kwesties ontmoeten. Vervolgens kunt u een segment maken dat zich richt op hun ervaring om te helpen hun problemen te identificeren en op te lossen.
* **de diensten van het Abonnement**: De gebruikers met lage overeenkomst zijn waarschijnlijker om te draaien. Als u het gedrag van zeer betrokken gebruikers begrijpt, kan dit hetzelfde gedrag voor weinig betrokken gebruikers aanmoedigen, waardoor het minder waarschijnlijk is dat ze hun abonnement opzeggen.

## Interface

Zie [ Interface ](../overview.md#interface) voor een overzicht van de Geleide analyseinterface. De volgende instellingen gelden specifiek voor deze analyse:

### Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakelaar tussen deze analyse en [ Trends ](trends.md).
* **[!UICONTROL Events]**: De gebeurtenissen die u wilt meten. Elke geselecteerde gebeurtenis wordt weergegeven als een afzonderlijke grafiek. Er wordt een rij die de trended-gebeurtenis vertegenwoordigt, aan de tabel toegevoegd. U kunt maximaal vijf gebeurtenissen opnemen.
* **[!UICONTROL Counted as]**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen. De opties zijn [!UICONTROL Users] , [!UICONTROL Sessions] , [!UICONTROL Percentage of users] en [!UICONTROL Percentage of sessions] . De noemer voor op percentage-gebaseerde metriek in deze analyse is gebruikers of zittingen die de geselecteerde gebeurtenissen, niet alle actieve gebruikers van het product deden.
* **[!UICONTROL Segments]**: De segmenten die u wilt meten. Elk geselecteerd segment verdubbelt het aantal balken in het diagram en de rijen in de tabel. U kunt maximaal vijf segmenten opnemen.

### Diagraminstellingen

De [!UICONTROL Frequency] -analyse biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. De opties zijn [!UICONTROL Horizontal bar] en [!UICONTROL Stacked bar] .

### Emmerinstellingen

Bepaalt hoe de gebeurtenis in groepen (emmers) wordt gecategoriseerd. In de trended lijstmening, worden de gebruikers gespikkeld gebaseerd op frequentie van gebruik in totaal en in elk interval, betekenend 1 kan de gebruiker naar verschillende emmers in verschillende intervallen tellen.

* **[!UICONTROL Auto buckets]**: identificeer automatisch de optimale emmergrootte op basis van de gegevensdistributie.
* **[!UICONTROL Customized buckets]**: pas aan hoe de gegevens in emmers worden gegroepeerd.
   * [!UICONTROL From]: Het eerste emmertje. Frequentie kleiner dan deze waarde wordt niet gerapporteerd.
   * [!UICONTROL To]: Frequentie die groter is dan deze waarde, wordt gegroepeerd in het laatste emmertje.
   * [!UICONTROL Size]: Het emmerinterval.

### Tijdvergelijking

{{apply-time-comparison}}

### Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. In het diagram en de tabel worden standaard samengevoegde gegevens weergegeven, met de optie om de tabel uit te vouwen tot een trendweergave. In de trended-weergave worden gebruikers ingesloten op basis van de gebruikte frequentie in totaal en in elk interval. Dit betekent dat één gebruiker in verschillende intervallen naar verschillende emmers kan tellen.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.


<!--
## Example

See below foran example of the analysis.

![Frequency](../assets/frequency.png)

-->
