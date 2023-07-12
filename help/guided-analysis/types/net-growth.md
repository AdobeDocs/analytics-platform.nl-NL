---
title: Netto groei
description: Wint of verliest u gebruikers?
feature: Guided Analysis
source-git-commit: ab734506a023eacdeeb7c26f31a4361a6b804795
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---

# Netto groei

{{release-limited-testing}}

De **Netto groei** weergavetype biedt inzicht in de snelheid waarmee u gebruikers gedurende een bepaalde periode bereikt of verliest. De horizontale as is een tijdinterval, terwijl de verticale as de meting van de groei is.

Elk gegevenspunt vertegenwoordigt de netto groei, die met de volgende formule wordt berekend:

`([New users] + [Return users]) / [Dormant users]`

Het resultaat van deze formule is een verhouding. Een netto groei van `1` een evenwicht vormt; het product heeft hetzelfde aantal gebruikers gewonnen als het heeft verloren . Een netto groei groter dan `1` een positieve groei vertegenwoordigt; er waren meer nieuwe + terugkeergebruikers dan slapende gebruikers. Evenzo is een nettogroei van minder dan `1` een verlies vertegenwoordigt; er waren meer slapende gebruikers dan nieuwe + terugkeergebruikers.

Vergelijkbaar met de [Actief](active.md) weergavetype, worden gebruikers als volgt gedefinieerd:

* **Nieuw**: De gebruiker was actief tijdens de huidige periode, maar niet eerder. Zie hoe ver de analyse terug kijkt om een nieuwe gebruiker te bepalen door over te hangen &#39;[!UICONTROL New users]in de legenda van het diagram. Het terugkijkbereik wordt dynamisch bepaald op basis van het geselecteerde datumbereik en interval.
* **Return**: De gebruiker was actief in de huidige periode en was niet actief in de onmiddellijk voorgaande periode, maar was voorheen actief op een bepaald punt. Zie hoe ver de analyse terug kijkt om een terugkeergebruiker te bepalen door over te hevelen &#39;[!UICONTROL Return users]in de legenda van het diagram. Het terugkijkbereik wordt dynamisch bepaald op basis van het geselecteerde datumbereik en interval.
* **Dormant**: De gebruiker was actief in de onmiddellijk vorige periode, maar is niet actief in de huidige periode. slapende gebruikers tellen niet mee voor het totale aantal actieve gebruikers.
* Opmerking: Herhalende gebruikers worden niet in deze berekening meegenomen, omdat ze geen winst of verlies van gebruikers vertegenwoordigen.

U kunt onder andere de volgende gevallen gebruiken voor dit weergavetype:

* **Prestatiebeoordeling**: Hiermee kunt u de algemene prestaties van uw product beoordelen in termen van het aanschaffen van nieuwe gebruikers. Door de groeitrends te volgen, kunt u beter begrijpen of uw product gebruikers aantrekt en in een gewenst tempo houdt.
* **Analyse van overname door gebruiker**: Staat u toe om de doeltreffendheid van uw strategieën van de gebruikersverwerving te beoordelen. Door de bronnen van groei van gebruikers te analyseren, zoals zoekmachines, campagnes of andere marketingkanalen, kunt u de belangrijkste bronnen van groei identificeren zodat u bronnen op basis daarvan kunt toewijzen.
* **Churn-analyse**: De netto groei omvat een beperking in zijn formule (slapende gebruikers). U kunt de algemene gezondheid van uw gebruikersbasis in tijd beoordelen. Indien de nettogroei constant onder blijft `1`, geeft het een grote hoeveelheid aandacht die kan leiden tot het implementeren van retentiestrategieën.

![Netto groei](../assets/net-growth.png)

## Query-rail

Met de queryrail kunt u de volgende componenten configureren:

* **Gebeurtenissen**: De gebeurtenis die u wilt meten. Aangezien dit weergavetype op gebruiker is gebaseerd, wordt een gebruiker die binnen de periode eenmaal met de gebeurtenis communiceert, als een actieve gebruiker geteld. U kunt één gebeurtenis in een vraag omvatten.
* **Mensen**: Het segment dat u wilt meten. U kunt één segment in een vraag omvatten.

## Datumbereik

Het gewenste datumbereik voor de analyse. Deze instelling bestaat uit twee componenten:

* **Interval**: De granulariteit voor de datum waarop u de getrineerde gegevens wilt weergeven. Mogelijke geldige opties zijn Uur, Dagelijks, Wekelijks, Maandelijks en Driemaandelijks. Hetzelfde datumbereik kan verschillende intervallen hebben die het aantal gegevenspunten in het diagram en het aantal kolommen in de tabel beïnvloeden. Bijvoorbeeld, zou het bekijken van een analyse die drie dagen met dagelijkse granulariteit overspant slechts drie gegevenspunten tonen, terwijl een analyse die drie dagen met uurgranulariteit overspant 72 gegevenspunten zou tonen.
* **Datum**: De begin- en einddatum. Voorinstellingen voor het verschuivende datumbereik en eerder opgeslagen aangepaste bereiken zijn voor uw gemak beschikbaar, maar u kunt ook de kalenderkiezer gebruiken om een vast datumbereik te kiezen.
