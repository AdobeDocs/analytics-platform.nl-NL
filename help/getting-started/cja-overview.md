---
title: Overzicht van de analyse van de reis van de klant
description: Introductie voor de analyse van klantreizen
translation-type: tm+mt
source-git-commit: 7afdf490d0a63b1286a1a646a487ee96d4b6ed8f

---


# Overzicht van de analyse van de reis van de klant

De Analyse van de Reis van de klant is een vermogen van de Analyse dat u de macht van de Werkruimte van de Analyse met gegevens van het Platform van de Ervaring van Adobe laat gebruiken. Het kan afbreken, filtreren, vragen, en visualiseren de waarde van jaren van gegevens, en wordt gecombineerd met de capaciteit van het Platform om allerlei gegevensschema&#39;s en types te houden. Gebruikend het Model van de Gegevens van de **Ervaring (XDM)**, kunnen de gegevens uniform worden vertegenwoordigd en georganiseerd, klaar voor combinatie en exploratie. **De Diensten** van de Vraag van de ervaring staat u toe om SQL-Compatibele hulpmiddelen en kaders te gebruiken om al uw gegevens te vragen en te manipuleren.

## Het vergelijken van CJA aan de Werkruimte van de Analyse

De Analyse van de Reis van de klant breidt het werkingsgebied van Analytics uit door makkelijk te gebruiken dwars-kanaal mogelijkheden aan te bieden en beperkingen in vorige versies van de Analyse van Adobe te verwijderen. Enkele opmerkelijke verbeteringen zijn:

* **Onbeperkte variabelen en gebeurtenissen**: De concepten eVars, de steunen, en de gebeurtenissen bestaan niet meer. De gegevens zijn hoofdzakelijk geconcentreerd op afmetingen en metriek. De reeksen van gegevens kunnen een onbeperkte hoeveelheid unieke afmetingen en metriek hebben.
* **Onbeperkte uniques**: Het Platform van de Ervaring van Adobe wordt niet beperkt tot om het even welke unieke beperkingen, zoals de unieke waarden 500k in traditionele rapportreeksen.
* **Verander historische gegevens**: Gebruikend het Platform van de Ervaring van Adobe, kunnen de gegevens worden verwijderd of worden verbeterd.
* **Gegevens** van een reeks voor meerdere rapporten: De bestaande implementaties van veelvoudige gegevensreeksen kunnen in Platform worden gecombineerd.

De aanvankelijke versie van de Analyse van de Reis van de Klant omvat veel van de eigenschappen inbegrepen in de Werkruimte van de Analyse. Voor een volledige lijst, zie de de eigenschapsteun [van de Analyse van de Reis van de](cja-aa.md)Klant.

### Wijzigingen in terminologie

Verscheidene eigenschappen in CJA zijn anders genoemd om zich aan de industrienormen aan te passen. Sommige bijgewerkte namen omvatten:

* De segmenten zijn nu genoemd geworden &quot;Filters&quot;
* De virtuele Uitrustingen van het Rapport zijn nu gekend als &quot;Meningen&quot;
* De classificaties zijn nu gekend als &quot;datasets van de Raadpleging&quot;
* De attributen van de klant zijn nu genoemd geworden &quot;datasets van het Profiel&quot;
* De containers van de hak zijn nu gekend als &quot;Gebeurtenis&quot;containers
* De containers van het bezoek zijn nu genoemd geworden &quot;de containers van de Zitting&quot;
* De containers van de bezoeker worden nu gekend als &quot;Person&quot;containers

## Belangrijkste gebruiksscenario&#39;s

De Analyse van de Reis van de klant laat u:

* **Bekijk de klant in een reiscontext**: U kunt gegevens bekijken en analyseren opeenvolgend, die veelvoudige kanalen overspannen. De gegevens van call centre, POS systemen, en online eigenschappen kunnen in één enkele rapporteringsmening worden gecombineerd.
* **Inzichten beschikbaar stellen voor iedereen**: De gegevenstoegang van de democratie en laat meer mensen bedrijfsbesluiten met gegeven-afgeleide inzichten nemen. Iedereen in de organisatie met verantwoordelijkheid voor om het even welk aspect van de klantenervaring kan echte besluiten sneller nemen, die op volledigere gegevens worden gebaseerd.
* **Profiteer van de kracht van de gegevenswetenschap voor uw analisten**: De Analyse van de Reis van de klant laat normale mensen gegevenswetenschap gebruiken om diepe inzichten en analyse te openen.
* **Visualiseer en interactie met uw datasets gebruikend ad hoc rapportering**: De werkruimte kan om het even welke dataset van het Platform van de Ervaring van Adobe gebruiken dat met sommige basisregels in overeenstemming is.
* **Niet-webgegevens** bekijken: De werkruimte is niet meer beperkt tot een rigide definitie van een &quot;hit&quot; of &quot;event&quot;. De schema&#39;s van de douane staan volledige controle over gegevens en definities toe.
* **Voer meer controle uit over uw gegevensmanipulatie**: De gegevens van de verandering u hebt geupload, creeer nieuwe datasets, en voer hen in Werkruimte in. Het Platform van de Ervaring van Adobe verstrekt het vragen van, het halen van, het omzetten van, en het laden van hulpmiddelen door de Dienst van de Vraag van de Cloud van de Ervaring.

## Voorwaarden

Alvorens u kunt beginnen met het gebruik van de Analyse van de Reis van de Klant, moeten de volgende stappen worden voltooid:

* Uw organisatie heeft een actief contract met de Analyse van Adobe voor Uitgezocht, de Eerste, of de Ultimate met toe:voegen-op de Analyse van de Reis van de Klant. Als u niet zeker weet welk type contract u hebt, of niet zeker bent of u de invoegtoepassing CJA hebt, neemt u contact op met de accountmanager van uw organisatie.
* Uw organisatie is provisioned voor het Platform van de Ervaring van Adobe.

## Toegangsrechten gebruiker

Om verbindingen tot stand te brengen, voeg datasets, enz. toe, hebt u de volgende toestemmingen in de Console [](https://adminconsole.adobe.com/enterprise/)Admin nodig:

* Om datasets in het Platform van de Ervaring te beheren, moet u deel van een Profiel van het Product van het Platform uitmaken dat u de toestemming &quot;geeft van de Datasets&quot;beheert. Voor meer informatie, zie de controle van de [Toegang in het Platform](https://www.adobe.io/apis/experienceplatform/home/permissions-and-sandboxes/permissions-and-sandboxes.html#!api-specification/markdown/narrative/technical_overview/access-control/access-control-overview.md)van de Ervaring van Adobe.
* Om een verbinding aan een dataset van het Platform tot stand te brengen, moet u deel van een Profiel van het Product van het Platform uitmaken dat u de volgende toestemmingen geeft:
   * Schemas bekijken
   * Datasets bekijken
   * Identiteitsnamen beheren
   * Sandboxes bekijken
* Als u toegang wilt krijgen tot de analyse van de reis van de klant of een verbinding wilt maken, moet u in de [beheerconsole](https://adminconsole.adobe.com/enterprise/)ook worden toegevoegd aan een productprofiel voor reisanalyse van de klant.

## Andere mogelijkheden die op het Platform van de Ervaring van Adobe worden voortgebouwd

De Analyse van de Reis van de klant is één vermogen onder velen die zich op het Platform van de Ervaring van Adobe baseren. Verscheidene andere mogelijkheden, die ook op Platform worden gebouwd, laten u het meeste uit uw gegevens krijgen.

Het Platform van de Ervaring van Adobe laat u klantengegevens en inhoud van om het even welk systeem centraliseren en standaardiseren en gegevenswetenschap en machine het leren toepassen om het ontwerp en de levering van gepersonaliseerde ervaringen te verbeteren. De gegevens van de klant in het platform worden opgeslagen als datasets, die uit een schema en partijen gegevens bestaan. Voor meer detail op het platform, zie het Overzicht [van de Architectuur van het Platform van de](https://www.adobe.io/apis/experienceplatform/home/overview.html)Ervaring van Adobe van de Architectuur.

Van de Opname van Gegevens aan directe SQL toegang, zijn verscheidene componenten van het Platform van de Ervaring centraal aan de Analyse van de Reis van de Klant en handelen samen met het:

* [Query-service](https://www.adobe.io/apis/experienceplatform/home/query-service/sql-reference.html): StandaardSQL van het gebruik om gegevens van het Platform van de Ervaring van Adobe, zoals de oplossingsgegevens van Adobe, klant 1st-partijgegevens, of een andere gegevens van het Platform terug te winnen. Het is een serverless hulpmiddel dat u toestaat om zich bij om het even welke datasets aan te sluiten en de vraagresultaten te vangen als nieuwe dataset voor gebruik in rapportering, de Werkruimte van de Wetenschap van Gegevens, of voor opneming in de Dienst van het Profiel. U kunt de Dienst van de Vraag gebruiken om de ecosystemen van de gegevensanalyse te bouwen, die tot een beeld van consumenten over hun diverse interactiekanalen leiden. Deze kanalen kunnen verkooppuntsystemen, Web, Mobiel, de systemen van CRM, enz. omvatten.
* [Real-time klantprofiel](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/unified_profile_architectural_overview/unified_profile_architectural_overview.md):
* [Identiteitsdienst](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/identity_services_architectural_overview/identity_services_architectural_overview.md):
* [De Werkruimte](https://www.adobe.io/apis/experienceplatform/home/data-science-workspace.html) van de Wetenschap van gegevens in &quot;ontwikkelaar&quot;optie: u kunt prebuilt artificial intelligence (AI) en machine-leert modellen in het Platform van de Ervaring van Adobe gebruiken om diverse punten van de klantenreis te beïnvloeden. Door verborgen inzichten te ondermijnen, kunt u betere voorspellingen over de klantenreis maken, geadviseerde beste volgende stappen voorstellen, of lastige processen automatiseren.
