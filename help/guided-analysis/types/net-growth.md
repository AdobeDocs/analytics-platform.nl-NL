---
title: Netto groei
description: Winsten en verliezen van gebruikers in balans brengen.
feature: Guided Analysis
source-git-commit: 84cafd2756a09537c93524ff728ea78b7cbf5c8e
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 0%

---

# Netto groei

{{release-limited-testing}}

De **Netto groei** weergavetype biedt inzicht in de snelheid waarmee u gebruikers gedurende een bepaalde periode verkrijgt of verliest. De horizontale as is altijd een tijdgranulariteit, terwijl de verticale as altijd de meting van de groei is.

Elk gegevenspunt vertegenwoordigt de netto groei van dat gegevenspunt, die gebruikend de volgende formule wordt berekend:

`([New users] + [Return users]) / [Dormant users]`

Vergelijkbaar met de [Actief](active.md) weergavetype, worden gebruikers als volgt gedefinieerd:

* **Nieuw**: De gebruiker was actief tijdens het huidige gegevenspunt en is niet in vorige gegevenspunten verschenen.
* **Return**: De gebruiker is niet in het onmiddellijk vorige gegevenspunt weergegeven, maar is geen nieuwe gebruiker.
* **Dormant**: De gebruiker werd niet weergegeven in het huidige gegevenspunt, maar wel in het onmiddellijk vorige gegevenspunt. slapende gebruikers tellen niet mee voor het totale aantal actieve gebruikers.

**Herhalen** de gebruikers worden niet meegerekend in deze berekening, aangezien zij geen groei of verlies vertegenwoordigen.

Het resultaat van deze formule is een verhouding waarbij uw gebruikersbasis tijdens dat gegevenspunt groeide of kromp. Een netto groei van `1` een equalibrium is; het product heeft hetzelfde aantal gebruikers gewonnen als het heeft verloren . Een netto groei groter dan `1` een positieve groei vertegenwoordigt; er waren meer nieuwe gebruikers/terugkeergebruikers dan slapende gebruikers. Evenzo is een nettogroei van minder dan `1` een verlies van actieve gebruikers vertegenwoordigt; er waren meer slapende gebruikers dan nieuwe gebruikers/terugkeergebruikers.

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Analyse van overname door gebruiker**: Staat u toe om de doeltreffendheid van uw strategieën van de gebruikersverwerving te beoordelen. Door de bronnen van groei van gebruikers te analyseren, zoals zoekmachines, campagnes of andere marketingkanalen, kunt u de belangrijkste bronnen van groei identificeren zodat u bronnen op basis daarvan kunt toewijzen.
* **Prestatiebeoordeling**: Hiermee kunt u de algemene prestaties van uw product beoordelen in termen van het aanschaffen van nieuwe gebruikers. Door de groeitrends te volgen, kunt u beter begrijpen of uw product gebruikers aantrekt en in een gewenst tempo houdt.
* **Churn-analyse**: De netto groei neemt een beperking in zijn formule (slapende gebruikers) op. U kunt de algemene gezondheid van uw gebruikersbasis in tijd beoordelen. Indien de nettogroei constant onder blijft `1`, geeft het een hoge mate van aandacht aan, waardoor u wordt gevraagd de redenen achter het onderzoek te onderzoeken en retentiestrategieën te implementeren.

![Netto groei](../assets/net-growth.png)

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **Gebeurtenissen**: De gebeurtenis die u wilt meten. Aangezien dit weergavetype op gebruiker is gebaseerd, kan een gebruiker de gebeurtenis eenmaal aanraken binnen de granulariteit voor de ingestelde datum om in de netto groei te zijn. U kunt slechts één gebeurtenis in een query opnemen.
* **Mensen**: Het segment dat u wilt meten. U kunt slechts één segment in een vraag omvatten.

## Datumbereik

Het gewenste datumbereik. Deze instelling bestaat uit twee belangrijke onderdelen:

* **Interval**: De granulariteit voor de datum waarin u gegevens wilt weergeven. Mogelijke geldige opties zijn Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **Datum**: De begin- en einddatum. Voorinstellingen voor datumbereik zijn beschikbaar voor uw gemak of u kunt de kalenderkiezer gebruiken om de exacte gewenste datum in te stellen.
