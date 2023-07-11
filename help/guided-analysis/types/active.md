---
title: Actief
description: Meet de groei van uw gebruikersbasis.
exl-id: 0a300bb2-7620-4e29-a6b5-542476893009
feature: Guided Analysis
source-git-commit: 14c7aa342649afbe9923b0086947e5a0adeefff2
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Actief

{{release-limited-testing}}

De **Actief** view type verstrekt inzicht over de groei en de verwerving van gebruikers over een specifieke periode. De horizontale as is altijd een tijdgranulariteit, terwijl de verticale as altijd een meting van gebruikers is. De gebruikers worden geanalyseerd vanaf het begin van de datumwaaier, verdeeld in vier categorieën:

* **Nieuw**: De gebruiker was actief tijdens het huidige gegevenspunt en is niet in vorige gegevenspunten verschenen. Over &#39;[!UICONTROL New users]&#39; in de legenda van de grafiek om te zien hoe ver het rapport terug kijkt om een nieuwe gebruiker te bepalen. Deze datum wordt dynamisch geselecteerd op basis van de lengte en granulariteit van het datumbereik.
* **Herhalen**: De gebruiker werd weergegeven in het vorige gegevenspunt en het huidige gegevenspunt.
* **Return**: De gebruiker is niet in het onmiddellijk vorige gegevenspunt weergegeven, maar is geen nieuwe gebruiker.
* **Dormant**: De gebruiker werd niet weergegeven in het huidige gegevenspunt, maar wel in het onmiddellijk vorige gegevenspunt. slapende gebruikers tellen niet mee voor het totale aantal actieve gebruikers.

Alle actieve gebruikers (new + repeat + return) worden weergegeven als een tint boven de horizontale as, terwijl alle slapende gebruikers in oranje worden weergegeven onder de horizontale as.

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Bewaren en onderdrukken van gebruikers:** Biedt een duidelijke visualisatie rond periodes van hoog of laag vasthouden van de gebruiker. Als u deze periodes van hoge of lage retentie herkent, kunt u productbeslissingen nemen om een hoge retentie aan te moedigen of om de kans op koorts te minimaliseren.
* **Campagnebeoordeling**: Door een specifieke campagne te bekijken, kunt u niet alleen begrijpen hoeveel verkeer het heeft gegenereerd, maar ook hoe goed de campagne gebruikers heeft geholpen betrokken te blijven.
* **Levenscyclusanalyse van gebruikers**: Door de actieve groei van gebruikers gedurende de hele levenscyclus van de gebruiker te analyseren, kunt u specifieke stadia bepalen waarin de betrokkenheid van de gebruiker afneemt. Als er bijvoorbeeld een hoge mate van slapende gebruikers is voor degenen die zich in een instapfase bevinden, kan dit wijzen op bruikbaarheidsproblemen of op de behoefte aan betere productbegeleiding.

[Screenshot van gebruikerstoename]

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **Gebeurtenissen**: De gebeurtenis die u wilt meten. Aangezien dit weergavetype op gebruiker is, kan een gebruiker de gebeurtenis eenmaal aanraken binnen de granulariteit voor de ingestelde datum die als een actieve gebruiker moet worden geteld. U kunt slechts één gebeurtenis in een query opnemen.
* **Mensen**: Het segment dat u wilt meten. U kunt slechts één segment in een vraag omvatten.

## Diagraminstellingen

Dit weergavetype biedt de volgende diagraminstellingen. U kunt de diagraminstellingen aanpassen in het menu tussen het weergavetype en de kalenderkiezer.

* **Metrisch**: De metrische waarde die u wilt meten. U kunt onder andere het aantal gebruikers en het percentage gebruikers kiezen.
* **Type diagram**: Het type visualisatie dat u wilt gebruiken. U kunt onder andere de opties Gestapelde balk en Gestapeld gebied kiezen.

## Tijdvergelijking toepassen

{{apply-time-comparison}}

## Datumbereik

Het gewenste datumbereik. Deze instelling bestaat uit twee belangrijke onderdelen:

* **Interval**: De granulariteit voor de datum waarin u gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **Datum**: De begin- en einddatum. Voorinstellingen voor datumbereik zijn beschikbaar voor uw gemak of u kunt de kalenderkiezer gebruiken om de exacte gewenste datum in te stellen.
