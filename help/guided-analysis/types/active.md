---
title: Actieve weergave
description: Identificeer wie nieuw, behouden, terugkeren, of slapend is.
exl-id: 53ef7485-9cae-4663-bf61-4eb77c126830
feature: Guided Analysis
keywords: productanalyse
role: User
source-git-commit: e448f6ddbff2673abbd2920aacf41d4268f3ce07
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# [!UICONTROL Active] weergave

De **Actief** view verschaft inzicht in de groei en de verwerving van gebruikers gedurende een specifieke periode. De horizontale as is een tijdinterval, terwijl de verticale as een maat van gebruikers is. Gebruikers worden opgesplitst in vier categorieën:

* **[!UICONTROL New]**: De gebruiker was actief tijdens de huidige periode, maar niet eerder. Kijk hoe ver de analyse terugkijkt door de muisaanwijzer op &#39;[!UICONTROL New users]in de legenda van het diagram. Het terugkijkbereik wordt dynamisch bepaald op basis van het geselecteerde datumbereik en interval.
* **[!UICONTROL Repeat]**: De gebruiker was actief in de huidige en onmiddellijk vorige periode.
* **[!UICONTROL Return]**: De gebruiker was actief in de huidige periode en was niet actief in de onmiddellijk voorafgaande periode, maar was voorheen actief op een bepaald punt. Kijk hoe ver de analyse terugkijkt door de muisaanwijzer op &#39;[!UICONTROL Return users]in de legenda van het diagram. Het terugkijkbereik wordt dynamisch bepaald op basis van het geselecteerde datumbereik en interval.
* **[!UICONTROL Dormant]**: De gebruiker was actief in de onmiddellijk vorige periode, maar is niet actief in de huidige periode. slapende gebruikers tellen niet mee voor het totale aantal actieve gebruikers.

Alle actieve gebruikers (new + repeat + return) worden weergegeven als een tint boven de horizontale as, terwijl alle slapende gebruikers in oranje worden weergegeven onder de horizontale as.

>[!VIDEO](https://video.tv.adobe.com/v/3421667/?learn=on)

## Gebruik hoofdletters

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Bewaren en onderdrukken van gebruikers:** Biedt een duidelijke visualisatie rond periodes van hoog of laag vasthouden van de gebruiker. Als u deze periodes van hoge of lage retentie herkent, kunt u productbeslissingen nemen om een hoge retentie aan te moedigen of om de kans op koorts te minimaliseren.
* **Campagnebeoordeling**: Het bekijken van een specifieke campagne kan u helpen begrijpen hoeveel verkeer het produceerde, en hoe goed het gebruikers hielp betrokken blijven.
* **Levenscyclusanalyse van gebruikers**: Door de actieve groei van gebruikers gedurende de hele levenscyclus van de gebruiker te analyseren, kunt u specifieke fasen identificeren waarin de betrokkenheid van de gebruiker afneemt. Als er bijvoorbeeld een hoge mate van slapende gebruikers is voor personen die zich in een instapfase bevinden, kan dit wijzen op bruikbaarheidsproblemen of op de behoefte aan betere begeleiding in het product.

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakel tussen dit weergavetype en [Netto groei](net-growth.md).
* **[!UICONTROL Events]**: De gebeurtenis die u wilt meten. Aangezien dit weergavetype op gebruiker is gebaseerd, wordt een gebruiker die binnen de periode eenmaal met de gebeurtenis communiceert, als een actieve gebruiker geteld. U kunt één gebeurtenis in een vraag omvatten.
* **[!UICONTROL Counted as]**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen. Opties omvatten [!UICONTROL Number of users] en [!UICONTROL Percentage of users].
* **[!UICONTROL Segments]**: Het segment waarop u gegevens wilt filteren. U kunt één segment in een vraag omvatten.

## Diagraminstellingen

De [!UICONTROL Active] de weergave biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. Opties omvatten [!UICONTROL Stacked bar] en [!UICONTROL Stacked area].

## Tijdvergelijking

{{apply-time-comparison}}

![Vergelijking van actieve tijd](../assets/active-compare.png)

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
