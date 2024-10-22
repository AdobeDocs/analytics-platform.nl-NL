---
title: Actieve groeianalyse
description: Identificeer wie nieuw, behouden, terugkeren, of slapend is.
exl-id: 53ef7485-9cae-4663-bf61-4eb77c126830
feature: Adobe Product Analytics, Guided Analysis
keywords: productanalyse
role: User
source-git-commit: 7ccc9f28acf08fb49d86005abb7fbb648a1564ce
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# [!UICONTROL Active growth] analyse

De ](/help/assets/icons/PeopleGroup.svg) **[!UICONTROL Active growth]** analyse 0} PeopleGroup verstrekt inzichten in de groei en de verwerving van gebruikers over een specifieke periode. ![ De horizontale as is een tijdinterval, terwijl de verticale as een maat van gebruikers is. Gebruikers worden opgesplitst in vier categorieën:

* **[!UICONTROL New]**: De gebruiker was actief tijdens de huidige periode, maar niet eerder. Zie hoe ver de analyse terugkijkt door de muis boven _[!UICONTROL New users]_te houden in de diagramlegenda. Het terugkijkbereik wordt dynamisch bepaald op basis van het geselecteerde datumbereik en interval.
* **[!UICONTROL Repeat]**: De gebruiker was actief in de huidige en onmiddellijk vorige periode.
* **[!UICONTROL Return]**: De gebruiker was actief in de huidige periode en was niet actief in de onmiddellijk vorige periode, maar was voorheen actief op een bepaald punt. Zie hoe ver de analyse terugkijkt door de muis boven _[!UICONTROL Return users]_te houden in de diagramlegenda. Het terugkijkbereik wordt dynamisch bepaald op basis van het geselecteerde datumbereik en interval.
* **[!UICONTROL Dormant]**: De gebruiker was actief in de onmiddellijk vorige periode, maar is niet actief in de huidige periode. slapende gebruikers tellen niet mee voor het totale aantal actieve gebruikers.

Alle actieve gebruikers (new + repeat + return) worden weergegeven als een tint boven de horizontale as, terwijl alle slapende gebruikers in oranje worden weergegeven onder de horizontale as.


>[!VIDEO](https://video.tv.adobe.com/v/3421667/?learn=on)

## Gebruik hoofdletters

De gevallen van het gebruik voor deze analyse omvatten:

* **het behoud en het koord van de Gebruiker:** verstrekt een duidelijke visualisatie van periodes van hoog of laag gebruikersbehoud. Als u deze periodes van hoge of lage retentie herkent, kunt u productbeslissingen nemen om een hoge retentie aan te moedigen of om de kans op koorts te minimaliseren.
* **de beoordeling van de Campagne**: Het bekijken van een specifieke campagne kan u helpen begrijpen hoeveel verkeer het produceerde, en hoe goed het hielp gebruikers betrokken blijven.
* **de levenscyclusanalyse van de Gebruiker**: Het analyseren van de actieve gebruikerstoename door de gebruikerslevenscyclus kan helpen specifieke stadia identificeren waar de gebruikersbetrokkenheid daalt. Als er bijvoorbeeld een hoge mate van slapende gebruikers is voor personen die zich in een instapfase bevinden, kan dit wijzen op bruikbaarheidsproblemen of op de behoefte aan betere begeleiding in het product.

## Interface

Zie [ Interface ](../overview.md#interface) voor een overzicht van de Geleide analyseinterface. De volgende instellingen gelden specifiek voor deze analyse:

### Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **[!UICONTROL View]**: Schakelaar tussen deze analyse en [ Netto groei ](net-growth.md).
* **[!UICONTROL Events]**: De gebeurtenis die u wilt meten. Aangezien deze analyse op gebruikers is gebaseerd, wordt een gebruiker die binnen de periode eenmaal met de gebeurtenis communiceert, als een actieve gebruiker geteld. U kunt één gebeurtenis in een vraag omvatten.
* **[!UICONTROL Counted as]**: De telmethode die u op de geselecteerde gebeurtenissen wilt toepassen. De opties zijn [!UICONTROL Number of users] en [!UICONTROL Percentage of users] .
* **[!UICONTROL Segments]**: Het segment waarop u gegevens wilt filteren. U kunt één segment in een vraag omvatten.

### Diagraminstellingen

De [!UICONTROL Active growth] -analyse biedt de volgende diagraminstellingen, die kunnen worden aangepast in het menu boven het diagram:

* **[!UICONTROL Chart type]**: Het type visualisatie dat u wilt gebruiken. De opties zijn [!UICONTROL Stacked bar] en [!UICONTROL Stacked area] .

### Tijdvergelijking

{{apply-time-comparison}}

### Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **[!UICONTROL Interval]**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben, die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **[!UICONTROL Date]**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.

<!--
## Example

See below for an example of the analysis.

![Active time compare](../assets/active-growth-compare.png)

-->
