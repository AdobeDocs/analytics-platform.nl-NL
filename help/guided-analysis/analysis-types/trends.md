---
title: Trends
description: Patronen en wijzigingen in de betrokkenheid van gebruikers zoeken in de loop van de tijd.
exl-id: 1d103bd3-3e72-4c82-a534-c896f8433029
feature: Guided Analysis
source-git-commit: edbad9c9d3dc0b48db5334828a18ef652d4a38aa
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 0%

---

# Trends

{{release-limited-testing}}

De **Trends** [Type analyse](overview.md) biedt waardevol inzicht in de prestaties van uw product of het gedrag van uw gebruikers in de loop van de tijd. De horizontale as van dit rapport is altijd een tijdgranulariteit, terwijl de verticale as uw gewenste gebeurtenissen meet. De gevallen van het gebruik voor dit analysetype omvatten:

* **Productprestaties evalueren**: Met trends kunt u de algemene prestaties van uw product gedurende een bepaalde periode beoordelen. Door metriek zoals gebruikersbetrokkenheid, conversietarieven, of opbrengst te analyseren, kunt u identificeren als de prestaties van uw product verbeteren, stagneren, of verminderen.
* **Aanpassing van functies**: De tendensen staan u toe om te begrijpen hoe de gebruikers nieuwe eigenschappen of updates goedkeuren die u vrijgeeft. U kunt bepalen welke functies populair zijn en welke functies moeten worden verbeterd. Met deze informatie kunt u gegevensgestuurde beslissingen maken over de functies waarmee u prioriteiten kunt stellen bij uw ontwikkelingsinspanningen.
* **Gebruikersgedrag**: De tendensen kunnen inzicht in gebruikersgedrag in tijd verstrekken. Door specifieke acties te onderzoeken die de gebruikers nemen, kunt u patronen identificeren waar de gebruikers zouden kunnen wegvallen. U kunt inzichten van dit analysetype combineren met een [Trechter](funnel.md) voor nog meer inzicht in gedrag.
* **A/B-tests en -experimenten**: Als u A/B tests binnen uw product in werking stelt, kunt u Trends gebruiken om te meten welke tests in tijd het meest succesvol zijn.

[Schermafbeelding van trends]

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **Gebeurtenissen**: De gebeurtenissen die u in uw rapport wilt meten. Elke hier geselecteerde gebeurtenis wordt, afhankelijk van het diagramtype, voorgesteld als een gekleurde lijn of een set balken. Aan de tabel wordt een rij toegevoegd die de trended-gebeurtenis vertegenwoordigt. U kunt maximaal vijf gebeurtenissen opnemen.
* **Mensen**: De segmenten die u in uw rapport wilt meten. Elk segment dat u hier selecteert, verdubbelt het aantal regels in het diagram en de rijen in de tabel. Elke set gebeurtenissen wordt voor elk segment weergegeven. U kunt maximaal vijf segmenten opnemen.

## Typen weergeven

De tendensen bieden de volgende meningstypes aan. U kunt het weergavetype wijzigen met het keuzemenu linksboven in het diagram.

* **Gebruik:** Meet de betrokkenheid van de gebruiker in de loop van de tijd.

## Diagraminstellingen

De tendensen bieden de volgende grafiekmontages aan. U kunt de diagraminstellingen aanpassen in het menu tussen het weergavetype en de kalenderkiezer.

* **Metrisch**: De metrische waarde die u wilt meten. U kunt onder andere gebeurtenissen, sessies, gebruikers, gebeurtenissen per sessie en gebeurtenissen per gebruiker kiezen.
* **Type diagram**: Het type visualisatie dat u wilt gebruiken. Dit menu bevat de opties Lijn, Staaf, Gestapelde balk en Gestapeld gebied.

## Tijdvergelijking toepassen

Trends bieden de mogelijkheid om de huidige tijdsperiode te vergelijken met een vorige tijdsperiode. Als u een optie in dit menu selecteert, krijgt elke lijn een stippellijn met dezelfde kleur. Deze stippellijn vertegenwoordigt dezelfde metrische waarde in het geselecteerde datumbereik. Als u deze optie instelt, verdubbelt u het aantal regels in het diagram en de rijen in de tabel.

De beschikbare opties voor tijdvergelijking omvatten de vorige periode, 13 weken vóór, 52 weken vóór en een aangepast datumbereik. Als u Aangepast datumbereik selecteert, worden aanvullende opties weergegeven waarmee u het getal en de granulariteit kunt selecteren. Als u Geen selecteert, wordt de datumvergelijking verwijderd.

## Datumbereik

Hiermee stelt u het gewenste datumbereik in. Deze instelling bestaat uit twee belangrijke onderdelen:

* **Interval**: De granulariteit voor de datum waarin u gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **Datum**: De begin- en einddatum. Voorinstellingen voor datumbereik zijn beschikbaar voor uw gemak of u kunt de kalenderkiezer gebruiken om de exacte gewenste datum in te stellen.
