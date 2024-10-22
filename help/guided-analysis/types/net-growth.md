---
title: Netto-groeianalyse
description: Wint of verliest u gebruikers?
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
exl-id: a4f97458-9934-4a98-8005-fa1ba7831101
role: User
source-git-commit: aff01f4fc3520d461ca800382cc24d8d948d9cbc
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# [!UICONTROL Net growth] analyse

De ](/help/assets/icons/NetGrowth.svg) **[!UICONTROL Net growth]** analyse 0} NetGrowth verstrekt inzichten rond het tarief waarbij u gebruikers over een specifieke periode krijgt of verliest. ![ De horizontale as is een tijdinterval, terwijl de verticale as de meting van de groei is.

Elk gegevenspunt vertegenwoordigt de netto groei, die met de volgende formule wordt berekend:

`([New users] + [Return users]) / [Dormant users]`

Het resultaat van deze formule is een verhouding. Een netto groei van `1` vertegenwoordigt een evenwicht; het product verwierf het zelfde aantal gebruikers het. Een netto groei groter dan `1` vertegenwoordigt een positieve groei; er waren meer nieuwe gebruikers + retourgebruikers dan slapende gebruikers. Evenzo vertegenwoordigt een netto groei onder `1` een verlies; er waren meer slapende gebruikers dan nieuwe + retourgebruikers.

Gelijkaardig aan de [ Actieve ](active-growth.md) analyse, worden de gebruikers bepaald als het volgende:

* **[!UICONTROL New]**: De gebruiker was actief tijdens de huidige periode, maar niet eerder. Zie hoe ver de analyse terug kijkt om een nieuwe gebruiker te bepalen door over &quot;[!UICONTROL New users]&quot;in de grafieklegenda te hangen. Het terugkijkbereik wordt dynamisch bepaald op basis van het geselecteerde datumbereik en interval.
* **[!UICONTROL Return]**: De gebruiker was actief in de huidige periode en was niet actief in de onmiddellijk vorige periode, maar was voorheen actief op een bepaald punt. Zie hoe ver de analyse terug kijkt om een terugkeergebruiker te bepalen door over &quot;[!UICONTROL Return users]&quot;in de grafieklegenda te bewegen. Het terugkijkbereik wordt dynamisch bepaald op basis van het geselecteerde datumbereik en interval.
* **[!UICONTROL Dormant]**: De gebruiker was actief in de onmiddellijk vorige periode, maar is niet actief in de huidige periode. slapende gebruikers tellen niet mee voor het totale aantal actieve gebruikers.

>[!NOTE]
>
>Herhalende gebruikers worden niet in deze berekening meegenomen, omdat ze geen winst of verlies van gebruikers vertegenwoordigen.

>[!VIDEO](https://video.tv.adobe.com/v/3421664/?learn=on)


## Gebruik hoofdletters

De gevallen van het gebruik voor deze analyse omvatten:

* **evaluatie van Prestaties**: Staat u toe om de algemene prestaties van uw product in termen van het verwerven van nieuwe gebruikers te beoordelen. Door de groeitrends te volgen, kunt u beter begrijpen of uw product gebruikers aantrekt en in een gewenst tempo houdt.
* **de acquisitieanalyse van de Gebruiker**: Staat u toe om de doeltreffendheid van uw strategieën van de gebruikersverwerving te beoordelen. Door de bronnen van groei van gebruikers te analyseren, zoals zoekmachines, campagnes of andere marketingkanalen, kunt u de belangrijkste bronnen van groei identificeren zodat u bronnen op basis daarvan kunt toewijzen.
* **de analyse van de Kurn**: De netto groei omvat attributie in zijn formule (slapende gebruikers). U kunt de algemene gezondheid van uw gebruikersbasis in tijd beoordelen. Als de netto groei constant onder `1` is, wijst het op een hoge hoeveelheid nadruk die tot het uitvoeren van behoudstrategieën zou kunnen leiden.

## Interface

Zie [ Interface ](../overview.md#interface) voor een overzicht van de Geleide analyseinterface. De volgende instellingen gelden specifiek voor deze analyse:

### Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakelaar tussen deze analyse en [ Actieve groei ](active-growth.md).
* **[!UICONTROL Events]**: De gebeurtenis die u wilt meten. Aangezien deze analyse op gebruikers is gebaseerd, wordt een gebruiker die binnen de periode eenmaal met de gebeurtenis communiceert, als een actieve gebruiker geteld. U kunt één gebeurtenis in een vraag omvatten.
* **[!UICONTROL Counted as]**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen. De opties zijn [!UICONTROL Number of users] en [!UICONTROL Percentage of users] .
* **[!UICONTROL Segments]**: Het segment dat u wilt meten. U kunt één segment in een vraag omvatten.

### Tijdvergelijking

{{apply-time-comparison}}

### Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.

<!-- 
## Example

See below for an example of the analysis.

![Net growth compare](../assets/net-growth-compare.png)

-->
