---
title: Overzicht van de reisanalyse van de klant
description: Introductie van de reisanalyse van de klant
translation-type: tm+mt
source-git-commit: 6f5c3c073069ca7f428d971515342c1a636795e3
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---


# Overzicht van de reisanalyse van de klant

De Analyse van de Reis van de klant is een vermogen van de Analyse dat u de macht van de Werkruimte van de Analyse met gegevens van het Platform van de Ervaring van Adobe laat gebruiken. Het kan afbreken, filtreren, vragen, en de waarde van jaren van gegevens visualiseren, en wordt gecombineerd met de capaciteit van het Platform om allerlei gegevensschema&#39;s en types te houden. Het gebruiken van **Het Model van de Gegevens van de ervaring (XDM)**, kunnen de gegevens uniform worden vertegenwoordigd en georganiseerd, klaar voor combinatie en onderzoek. **Experience Query Services** staat u toe om SQL-Compatibele hulpmiddelen en kaders te gebruiken om al uw gegevens te vragen en te manipuleren.

## Het vergelijken van CJA met de Traditionele Analyse van Adobe

De Analyse van de Reis van de klant breidt het werkingsgebied van Analytics uit door makkelijk te gebruiken dwars-kanaalmogelijkheden aan te bieden en beperkingen in vorige versies van de Analyse van Adobe te verwijderen. Enkele opmerkelijke verbeteringen zijn:

* **Onbeperkte variabelen en gebeurtenissen**: De concepten eVars, props, en gebeurtenissen bestaan niet meer. De gegevens zijn hoofdzakelijk geconcentreerd op afmetingen en metriek. De reeksen van gegevens kunnen een onbeperkte hoeveelheid unieke afmetingen en metriek hebben.
* **Onbeperkte unieke waarden**: Het Platform van de Ervaring van Adobe wordt niet beperkt tot om het even welke unieke beperkingen, zoals de unieke waarden 500k in traditionele rapportreeksen.
* **Verander historische gegevens**: Gebruikend het Platform van de Ervaring van Adobe, kunnen de gegevens worden verwijderd of worden verbeterd.
* **Gegevens uit de cross-report-suite**: De bestaande implementaties van veelvoudige gegevensreeksen kunnen in Platform worden gecombineerd.

De aanvankelijke versie van de Analyse van de Reis van de Klant omvat veel van de eigenschappen inbegrepen in de Werkruimte van de Analyse. Voor een volledige lijst, zie [Customer Journey Analytics-functionaliteit](cja-aa.md).

## Het vergelijken van CJA met de Analyse van het Kruisapparaat

[Cross-Device Analytics](https://docs.adobe.com/content/help/en/analytics/components/cda/cda-home.html) integreert met de Dienst van de Identiteit van het Platform van de Ervaring van Adobe, gebruikend of de Grafiek Co-op of Privé Grafiek, om te identificeren hoe de digitale apparaten aan mensen in kaart brengen. Het is beschikbaar voor de Ultieme klanten van de Analyse van Adobe.

CJA integreert met de datasets van het Platform van de Ervaring van Adobe en laat kanaalanalyse in de Werkruimte van de Analyse toe. Hoewel CJA nog niet met de Coop of de Privé identiteitsgrafieken integreert, kunt u &quot;uw eigen identiteitskaart&quot;brengen om datasets samen te voegen, en die datasets kunnen voorbij digitale gegevens gaan om zowel online als off-line touchpoints te omvatten. De eerste vereisten van CJA worden behandeld hieronder meer in detail.

## Belangrijkste gebruiksscenario&#39;s

De Analyse van de Reis van de klant laat u:

* **Bekijk de klant in een reiscontext**: U kunt gegevens bekijken en analyseren opeenvolgend, overspannend veelvoudige kanalen. De gegevens van uw call centre, POS systemen, en online eigenschappen kunnen in één enkele rapporteringsmening worden gecombineerd.
* **Iedereen inzichten ter beschikking stellen**: Laat de toegang tot gegevens democratiseren en meer mensen zakelijke beslissingen nemen met op gegevens gebaseerde inzichten. Iedereen in de organisatie met verantwoordelijkheid voor om het even welk aspect van de klantenervaring kan echte besluiten sneller nemen, die op vollediger gegevens worden gebaseerd.
* **Profiteer van de kracht van de gegevenswetenschap voor uw analisten**: De Analyse van de Reis van de klant laat normale mensen gegevenswetenschap gebruiken om diepe inzichten en analyse te openen.
* **Visualiseer en maak met uw datasets interactie aan gebruikend ad hoc rapportering**: De werkruimte kan om het even welke dataset van het Platform van de Ervaring van Adobe gebruiken dat met sommige basisregels in overeenstemming is.
* **Niet-webgegevens bekijken**: De werkruimte is niet meer beperkt tot een starre definitie van een &quot;hit&quot; of &quot;event&quot;. De schema&#39;s van de douane staan volledige controle over gegevens en definities toe.
* **Verbeter de controle over uw gegevensmanipulatie**: De gegevens van de verandering u hebt geupload, creëren nieuwe datasets, en voeren hen in Werkruimte in. Het Platform van de Ervaring van Adobe verstrekt het vragen, het halen, het omzetten, en het laden hulpmiddelen door de Dienst van de Vraag van de Wolk van de Ervaring.

## Vereisten

Alvorens u kunt beginnen de Analyse van de Reis van de Klant te gebruiken, moet aan de volgende eerste vereisten worden voldaan:

* Uw organisatie heeft een actief contract met de Analyse van Adobe voor Uitgezochte, Eerste, of Ultimate met de toe:voegen-op Analyse van de Reis van de Klant. Als u niet zeker weet welk type contract u hebt, of niet zeker weet of u de CJA add-on hebt, neemt u contact op met de accountmanager van uw organisatie.
* Uw organisatie is provisioned voor het Platform van de Ervaring van Adobe.

## Toegangsrechten gebruiker

Om verbindingen tot stand te brengen, voeg datasets, enz. toe, hebt u de volgende toestemmingen in de [Beheerconsole](https://adminconsole.adobe.com/enterprise/):

* Om datasets in het Platform van de Ervaring te beheren, moet u deel van een Profiel van het Product van het Platform uitmaken dat u de toestemming &quot;geeft van de Datasets&quot;beheert. Voor meer informatie, zie [Toegangsbeheer in Adobe Experience Platform](https://www.adobe.io/apis/experienceplatform/home/permissions-and-sandboxes/permissions-and-sandboxes.html#!api-specification/markdown/narrative/technical_overview/access-control/access-control-overview.md).
* Om een verbinding aan een dataset van het Platform tot stand te brengen, moet u deel van een Profiel van het Product van het Platform uitmaken dat u de volgende toestemmingen geeft:
   * Schemas bekijken
   * Datasets bekijken
   * Identiteitsnamen beheren
   * Sandboxes bekijken
* Als u toegang wilt krijgen tot de reisanalyse van de klant of een verbinding wilt maken, moet u in de [Beheerconsole](https://adminconsole.adobe.com/enterprise/).

### Terminologie-updates

Verscheidene eigenschappen in CJA zijn anders genoemd om zich aan de industrienormen te richten. Enkele bijgewerkte namen zijn:

* Segmenten worden nu &quot;Filters&quot; genoemd.
* De virtuele Uitrustingen van het Rapport zijn nu gekend als &quot;Meningen&quot;.
* De classificaties zijn nu genoemd geworden &quot;datasets van de Raadpleging&quot;.
* De attributen van de klant zijn nu genoemd geworden &quot;datasets van het Profiel&quot;.
* De containers van de HAIT zijn nu gekend als &quot;Gebeurtenis&quot;containers.
* De containers van het bezoek zijn nu genoemd geworden &quot;Zitting&quot;containers.
* Visitorcontainers worden nu &quot;Person&quot;-containers genoemd.

## Andere mogelijkheden die op het Platform van de Ervaring van Adobe worden voortgebouwd

De Analyse van de Reis van de klant is één vermogen onder velen die zich op het Platform van de Ervaring van Adobe baseren. Verscheidene andere mogelijkheden, die ook op Platform worden gebouwd, laten u het meeste uit uw gegevens halen.

Het Platform van de Ervaring van Adobe laat u klantengegevens en inhoud van om het even welk systeem centraliseren en standaardiseren en gegevens en machine het leren toepassen om het ontwerp en de levering van gepersonaliseerde ervaringen te verbeteren. De gegevens van de klant in het platform worden opgeslagen als datasets, die uit een schema en partijen gegevens bestaan. Voor meer details op het platform, zie [Overzicht van de architectuur van het Platform van de Ervaring van Adobe](https://www.adobe.io/apis/experienceplatform/home/overview.html).

Van de Opname van Gegevens aan directe SQL toegang, zijn verscheidene componenten van het Platform van de Ervaring centraal aan de Analyse van de Reis van de Klant en handelen samen met het:

* [Query-service](https://www.adobe.io/apis/experienceplatform/home/query-service/sql-reference.html): Standaard SQL van het gebruik om gegevens van het Platform van de Ervaring van Adobe, zoals de oplossingsgegevens van Adobe, klant 1st-partijgegevens, of een andere gegevens van het Platform terug te winnen. Het is een serverloos hulpmiddel dat u toestaat om zich bij om het even welke datasets aan te sluiten en de vraagresultaten als nieuwe dataset voor gebruik in rapportering, de Werkruimte van de Wetenschap van Gegevens, of voor opname in de Dienst van het Profiel te vangen. U kunt de Dienst van de Vraag gebruiken om de ecosystemen van de gegevensanalyse te bouwen, die tot een beeld van consumenten over hun diverse interactiekanalen leiden. Deze kanalen zouden punt-van-verkoop systemen, Web, Mobiel, de systemen van CRM, enz. kunnen omvatten.
* [Real-time klantprofiel](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/unified_profile_architectural_overview/unified_profile_architectural_overview.md):
* [Identiteitsdienst](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/identity_services_architectural_overview/identity_services_architectural_overview.md):
* [Data Science Workspace](https://www.adobe.io/apis/experienceplatform/home/data-science-workspace.html) in de optie &quot;ontwikkelaar&quot;: u kunt prebuilt artificial intelligence (AI) en machine-leert modellen in het Platform van de Ervaring van Adobe gebruiken om diverse punten van de klantenreis te beïnvloeden. Door verborgen inzichten te ondermijnen, kunt u betere voorspellingen over de klantenreis maken, adviseren beste volgende stappen, of omslachtige processen automatiseren.
