---
title: Groei van gebruikers
description: Houd de groei van de gebruikersbasis van uw product bij.
source-git-commit: 37699a674a190aa2f28125d5b39bb3c27ac88551
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Groei van gebruikers

{{release-limited-testing}}

De **Groei van gebruikers** [Type analyse](overview.md) geeft inzicht in de groei en verwerving van gebruikers gedurende een specifieke periode. De horizontale as is altijd een tijdgranulariteit, terwijl de verticale as altijd een meting van gebruikers is. De gebruikers worden geanalyseerd vanaf het begin van de datumwaaier, verdeeld in vier categorieën:

* **Nieuw**: Het is de eerste keer dat de gebruiker in het opgegeven datumbereik verschijnt. Het eerste gegevenspunt is altijd 100% nieuwe gebruikers, aangezien de analyse niet buiten het datumbereik kijkt.
* **Herhalen**: De gebruiker werd weergegeven in het vorige gegevenspunt en het huidige gegevenspunt.
* **Return**: De gebruiker is niet in het onmiddellijk vorige gegevenspunt weergegeven, maar is geen nieuwe gebruiker. De gebruikers van de terugkeer kunnen niet in de eerste of tweede gegevenspunten verschijnen, aangezien zij eerst als nieuwe gebruiker dan een slapende gebruiker moeten verschijnen.
* **Dormant**: De gebruiker werd niet weergegeven in het huidige gegevenspunt, maar wel in het onmiddellijk vorige gegevenspunt. slapende gebruikers tellen niet mee voor het totale aantal actieve gebruikers.

Alle actieve gebruikers (new + repeat + return) worden weergegeven als een tint boven de horizontale as, terwijl alle slapende gebruikers in oranje worden weergegeven onder de horizontale as.

De gevallen van het gebruik voor dit analysetype omvatten:

* **Prestatiebeoordeling**: Door de groei van gebruikers kunt u de algemene prestaties van uw product beoordelen in termen van het aanschaffen van nieuwe gebruikers. Door de groeitrends te volgen, kunt u beter begrijpen of uw product gebruikers aantrekt en in een gewenst tempo houdt.
* **Bewaren en onderdrukken van gebruikers:** De groei van de gebruiker zorgt voor een duidelijke visualisatie rond periodes van hoog of laag gebruikersbehoud. Als u deze periodes van hoge of lage retentie herkent, kunt u productbeslissingen nemen om een hoge retentie aan te moedigen of om de kans op koorts te minimaliseren.
* **Campagnebeoordeling**: Door de gebruikerstoename specifiek voor een specifieke campagne te bekijken, kunt u niet alleen begrijpen hoeveel verkeer het produceerde, maar ook hoe goed de campagne gebruikers hielp betrokken te blijven.

[Screenshot van gebruikerstoename]

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **Gebeurtenissen**: De gebeurtenis die u wilt meten. Aangezien dit analysetype op gebruiker is gebaseerd, kan een gebruiker de gebeurtenis eenmaal aanraken binnen de ingestelde datumgranulariteit die als actieve gebruiker moet worden geteld. U kunt slechts één gebeurtenis opnemen.
* **Mensen**: Het segment dat u wilt meten. U kunt slechts één segment opnemen.

## Typen weergeven

De groei van de gebruiker biedt de volgende meningstypes aan. U kunt het weergavetype wijzigen met het keuzemenu linksboven in het diagram.

* **Actief:** Meet de groei van uw gebruikersbasis.

## Diagraminstellingen

De groei van de gebruiker biedt de volgende grafiekmontages aan. U kunt de diagraminstellingen aanpassen in het menu tussen het weergavetype en de kalenderkiezer.

* **Metrisch**: De metrische waarde die u wilt meten. U kunt onder andere het aantal gebruikers en het percentage gebruikers kiezen.
* **Type diagram**: Het type visualisatie dat u wilt gebruiken. U kunt onder andere de opties Gestapelde balk en Gestapeld gebied kiezen.

## Datumbereik

Het gewenste datumbereik. Deze instelling bestaat uit twee belangrijke onderdelen:

* **Interval**: De granulariteit voor de datum waarin u gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **Datum**: De begin- en einddatum. Voorinstellingen voor datumbereik zijn beschikbaar voor uw gemak of u kunt de kalenderkiezer gebruiken om de exacte gewenste datum in te stellen.
