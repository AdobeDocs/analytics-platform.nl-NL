---
title: Overzicht van de analyse van de reis van de klant
description: Introductie van de analyse van de reis van de klant
translation-type: tm+mt
source-git-commit: 6f5c3c073069ca7f428d971515342c1a636795e3
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---


# Overzicht van de analyse van de reis van de klant

De Analyse van de Reis van de Klant is een Analytics-capaciteit die u de macht van de Werkruimte van de Analyse met gegevens van het Platform van de Ervaring van Adobe laat gebruiken. Het kan onderbreken, filtreren, vragen, en visualiseert jaren&#39; waarde van gegevens, en wordt gecombineerd met de capaciteit van het Platform om allerlei gegevensschema&#39;s en types te houden. Met behulp van het XDM ( **Experience Data Model)** kunnen gegevens op uniforme wijze worden vertegenwoordigd en geordend, klaar voor combinatie en exploratie. **De Diensten** van de Vraag van de ervaring staat u toe om SQL-compatibele hulpmiddelen en kaders te gebruiken om al uw gegevens te vragen en te manipuleren.

## CJA vergelijken met Traditionele Adobe Analytics

De Analyse van de Reis van de Klant breidt het werkingsgebied van Analytics uit door makkelijk te gebruiken dwars-kanaalmogelijkheden aan te bieden en beperkingen in vorige versies van de Analyse van Adobe te verwijderen. Enkele opmerkelijke verbeteringen zijn:

* **Onbeperkte variabelen en gebeurtenissen**: De concepten eVars, props en gebeurtenissen bestaan niet meer. De gegevens zijn vooral gericht op dimensies en metriek. Gegevenssets kunnen een onbeperkte hoeveelheid unieke afmetingen en metriek hebben.
* **Onbeperkte unieke waarden**: Het Adobe Experience Platform is niet beperkt tot enige unieke beperkingen, zoals de unieke waarden van 500 k in traditionele rapportsuites.
* **Historische gegevens** wijzigen: Met Adobe Experience Platform kunnen gegevens worden verwijderd of gecorrigeerd.
* **Gegevens** uit meerdere rapporten: Bestaande implementaties van meerdere gegevenssets kunnen worden gecombineerd in Platform.

De eerste versie van de analyse van de reis van de Klant omvat veel van de eigenschappen inbegrepen in de Werkruimte van de Analyse. Voor een volledige lijst, zie de eigenschapsteun [van de Analyse van de Reis van de](cja-aa.md)Klant.

## CJA vergelijken met apparaatanalyse

[Apparaatanalyse](https://docs.adobe.com/content/help/en/analytics/components/cda/cda-home.html) kan worden geïntegreerd met de identiteitsservice van het Adobe Experience Platform, waarbij gebruik wordt gemaakt van de coop-grafiek of de persoonlijke grafiek, om te bepalen hoe digitale apparaten aan mensen worden toegewezen. Deze is beschikbaar voor klanten van Adobe Analytics Ultimate.

CJA integreert met de datasets van het Platform van de Ervaring van Adobe en laat kanaalanalyse in de Werkruimte van de Analyse toe. Hoewel CJA nog niet met de coop of de Privé identiteitsgrafieken integreert, kunt u &quot;uw eigen identiteitskaart&quot;brengen om datasets samen te voegen, en die datasets kunnen voorbij digitale gegevens gaan om zowel online als off-line aanraakpunten te omvatten. CJA-voorwaarden worden hieronder gedetailleerder behandeld.

## Hoofdgebruik

De Analyse van de Reis van de Klant laat u:

* **Raadpleeg de klant in een reiscontext**: U kunt gegevens opeenvolgend bekijken en analyseren, die veelvoudige kanalen overspannen. De gegevens van uw vraagcentrum, POS systemen, en online eigenschappen kunnen in één enkele rapporteringsmening worden gecombineerd.
* **Inzichten voor iedereen** beschikbaar maken: De gegevenstoegang van de democratisering en meer mensen laten bedrijfsbesluiten met gegeven-afgeleide inzichten maken. Iedereen in de organisatie met verantwoordelijkheid voor om het even welk aspect van de klantenervaring kan echte besluiten sneller maken, die op volledigere gegevens worden gebaseerd.
* **Maak gebruik van de kracht van gegevenswetenschap voor uw analisten**: De Analyse van de Reis van de klant laat normale mensen gegevenswetenschap gebruiken om diepe inzichten en analyse te ontsluiten.
* **Visualiseer en interactie met uw datasets gebruikend ad hoc rapportering**: De werkruimte kan om het even welke dataset van het Platform van de Ervaring van Adobe gebruiken die aan sommige basisregels voldoet.
* **Niet-webgegevens** weergeven: De werkruimte is niet langer beperkt tot een starre definitie van een &#39;hit&#39; of &#39;event&#39;. De schema&#39;s van de douane staan volledige controle over gegevens en definities toe.
* **Meer controle over het manipuleren** van gegevens: De gegevens van de verandering u hebt geupload, creeert nieuwe datasets, en voert hen in Werkruimte in. Met de Experience Cloud Query Service beschikt u via het Adobe Experience Platform over het zoeken, uitpakken, transformeren en laden van gereedschappen.

## Vereisten

Voordat u de Analyse van de Reis van de Klant kunt gaan gebruiken, moet aan de volgende voorwaarden worden voldaan:

* Uw organisatie heeft een actief contract met Adobe Analytics voor Select, Prime of Ultimate met de invoegtoepassing voor de analyse van de reis van klanten. Neem contact op met de accountmanager van uw organisatie als u niet zeker weet welk type contract u hebt of als u de CJA-invoegtoepassing hebt.
* Uw organisatie is ingericht voor het Adobe Experience Platform.

## Toegangsrechten gebruiker

Als u verbindingen wilt maken, gegevenssets wilt toevoegen, hebt u de volgende machtigingen nodig in de [beheerconsole](https://adminconsole.adobe.com/enterprise/):

* Om datasets in het Platform van de Ervaring te beheren, moet u deel van een Profiel van het Product van het Platform uitmaken dat u de toestemming &quot;geeft Datasets&quot;te leiden. Zie [Toegangsbeheer in het Adobe Experience Platform](https://www.adobe.io/apis/experienceplatform/home/permissions-and-sandboxes/permissions-and-sandboxes.html#!api-specification/markdown/narrative/technical_overview/access-control/access-control-overview.md)voor meer informatie.
* Om een verbinding aan een dataset van het Platform tot stand te brengen, moet u deel van een Profiel van het Product van het Platform uitmaken dat u de volgende toestemmingen geeft:
   * Schema&#39;s weergeven
   * Gegevensbestanden weergeven
   * Identiteitsnaamruimten beheren
   * Sandboxen weergeven
* Als u toegang wilt krijgen tot de analyse van reizen van klanten of verbinding wilt maken, moet u ook worden toegevoegd aan een productprofiel voor reisanalyse van klanten in de [beheerconsole](https://adminconsole.adobe.com/enterprise/).

### Terminologie-updates

Verschillende functies in CJA zijn hernoemd om overeen te stemmen met industriestandaarden. Enkele bijgewerkte namen zijn:

* Segmenten worden nu &#39;filters&#39; genoemd.
* Virtuele rapportsets worden nu &#39;Weergaven&#39; genoemd.
* Classificaties worden nu &#39;Gegevensbestanden opzoeken&#39; genoemd.
* Klantkenmerken worden nu &#39;profielgegevenssets&#39; genoemd.
* De containers van de greep zijn nu genoemd geworden &quot;Event&quot;containers.
* Visitecontainers worden nu &#39;Sessie&#39;-containers genoemd.
* Bezoekerscontainers worden nu &#39;Person&#39;-containers genoemd.

## Andere mogelijkheden die zijn gebaseerd op het Adobe Experience Platform

De analysemogelijkheden van de Klant zijn één van de vele mogelijkheden die op het Platform van de Ervaring van Adobe vertrouwen. Met verschillende andere mogelijkheden, die ook op Platform zijn gebaseerd, kunt u optimaal profiteren van uw gegevens.

Met het Adobe Experience Platform kunt u klantgegevens en -inhoud uit elk systeem centraliseren en standaardiseren en gegevens en computer learning toepassen om het ontwerp en de levering van persoonlijke ervaringen te verbeteren. De gegevens van de klant in het platform worden opgeslagen als datasets, die uit een schema en partijen gegevens bestaan. Zie Overzicht [van de architectuur van het](https://www.adobe.io/apis/experienceplatform/home/overview.html)Adobe Experience Platform voor meer informatie over het platform.

Van de Ingestie van Gegevens tot directe SQL toegang, zijn verscheidene componenten van het Platform van de Ervaring centraal aan de Analyse van de Reis van de Klant en handelen samen met het:

* [Query-service](https://www.adobe.io/apis/experienceplatform/home/query-service/sql-reference.html): Gebruik standaard-SQL om gegevens op te halen van het Adobe Experience Platform, zoals gegevens over de Adobe-oplossing, gegevens van de klant van de eerste partij of andere gegevens van het Platform. Het is een serverloos hulpmiddel dat u toestaat om zich bij om het even welke datasets aan te sluiten en de vraagresultaten als nieuwe dataset voor gebruik in rapportering, de Werkruimte van de Wetenschap van Gegevens, of voor opname in de Dienst van het Profiel te vangen. U kunt de Dienst van de Vraag gebruiken om gegevensanalysecosystemen te bouwen, die tot een beeld van consumenten over hun diverse interactiekanalen leiden. Deze kanalen zouden de systemen van het Punt-van-verkoop, Web, Mobiel, CRM, enz. kunnen omvatten.
* [Klantprofiel](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/unified_profile_architectural_overview/unified_profile_architectural_overview.md)in realtime:
* [Identiteitsservice](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/identity_services_architectural_overview/identity_services_architectural_overview.md):
* [Data Science Workspace](https://www.adobe.io/apis/experienceplatform/home/data-science-workspace.html) in de optie &quot;developer&quot;: u kunt prebuilt artificiële intelligentie (AI) en machine-leert modellen in het Platform van de Ervaring van Adobe gebruiken om diverse punten van de klantenreis te beïnvloeden. Door verborgen inzichten te negeren, kunt u betere voorspellingen over de klantenreis maken, geadviseerde beste volgende stappen voorstellen, of lastige processen automatiseren.
