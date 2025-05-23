---
description: Verklaart welke factoren de consistentie van metriek en het aantal van het publiekslidmaatschap tussen het Platform van de Gegevens van de Klant in real time (CDP in real time) en Customer Journey Analytics beïnvloeden.
title: Consistentie van metriek en publiek lidmaatschap
role: Admin
feature: Basics
exl-id: 13d972bc-3d32-414e-a67d-845845381c3e
source-git-commit: 7c906e30d54362713f5013c8661ee523938d4b0f
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---


# Consistentie van metriek en publiek lidmaatschap

In real-time scenario&#39;s, kan de consistentie van metriek en het kijklidmaatschap van het publiek over het Platform van de Gegevens van de Klant in real time (CDP in real time) en Customer Journey Analytics niet worden gewaarborgd. In dit document wordt uitgelegd waarom.

Wanneer het vergelijken van het aantal van het publiekslidmaatschap tussen CDP in real time en Customer Journey Analytics, is het belangrijk om in mening de verschillende doelstellingen van deze twee hulpmiddelen te houden. CDP in real time gebruikt gegevens van het klantenprofiel om digitale ervaringen aan individuele consumenten te richten, terwijl Customer Journey Analytics wordt ontworpen om gebruikers te helpen patronen in zeer belangrijke bedrijfsmetriek en segmenten begrijpen. Terwijl het publiek dat van Customer Journey Analytics aan in real time CDP publiceert een gebruiker van deze hulpmiddelen toestaat om een inzicht gemakkelijk en native &quot;te activeren&quot;, die uit de lessen voordeel halen die in Customer Journey Analytics worden verkregen, dienen deze hulpmiddelen niettemin fundamenteel verschillende doeleinden.

## Verschillen in identiteitsconfiguraties

CDP en Customer Journey Analytics in realtime hebben tegenwoordig niet dezelfde definitie van een persoon. CDP in real time baseert zich volledig op de informatie in de [ Grafiek van de Identiteit ](https://experienceleague.adobe.com/docs/platform-learn/tutorials/identities/understanding-identity-and-identity-graphs.html?lang=nl-NL) om een samengevoegd profiel te bouwen.

Customer Journey Analytics kan worden gevormd om [ Stitching ](../stitching/overview.md) te gebruiken. Als u [ Gebaseerde het Sstitching van het Gebied ](/help/stitching/fbs.md) als het stitching mechanisme gebruikt, specificeert u een herkenningsteken van een dataset in het gegevensmeer om de gegevens in die dataset met het doel te verbinden om de dataset met betere samengevoegde profielen op te heffen. Als u [ Grafiek baseerde het stitching ](/help/stitching/gbs.md) als het stitching mechanisme gebruikt, gebruikt een gelijkaardig proces de identiteitsgrafiek, die op een gespecificeerde identiteit wordt gebaseerd namespace.


## Verschillen in configuratie gegevensset

U kunt verkiezen om sommige gegevens in real time CDP en sommige in Customer Journey Analytics te zetten; vaak, kiezen de klanten om meer historische gegevens in Customer Journey Analytics te zetten dan voor Echt - tijd CDP relevant is. Andere datasets zouden voor in real time CDP dan voor Customer Journey Analytics relevanter kunnen zijn.

## Verschillen in verwerkingsconfiguratie

Customer Journey Analytics staat voor uitgebreide gegevenswijziging bij vraagtijd toe, zoals het combineren van gebieden, het splitsen van gebieden uit elkaar, en andere manipulaties zoals omvat/sluit uit, subkoorden, waarde deduplicatie, zittingsonisatie, en rij-vlakke het filtreren.

CDP in real time biedt een verschillende reeks hulpmiddelen van de gegevensmanipulatie aan. Het past [ samenvoegbeleid ](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/overview.html?lang=nl-NL) toe om te bepalen welke gegevens aan voorrang zullen worden gegeven en welke gegevens zullen worden gecombineerd om een verenigde mening van een persoon tot stand te brengen.

## Verschillen in TTL (Tijd aan Levende) en gegevensopname

Zelfs als de datasets in Echt - tijd CDP en Customer Journey Analytics het zelfde zijn, kan CDP in real time slechts een zeer beperkt venster van geschiedenis houden. Customer Journey Analytics heeft daarentegen waarschijnlijk jaren aan gegevens. Daarnaast:

* Customer Journey Analytics- en Real-time CDP-klanten kunnen aangepaste retentievensters voor gegevens instellen, onafhankelijk van elkaar.

* CDP en Customer Journey Analytics in real time hebben verschillende logica voor het opnemen van gegevens. Customer Journey Analytics negeert records zonder een persoon-id of tijdstempel en heeft strikte limieten aan het aantal records dat één profiel/persoon kan hebben.

* CDP-klanten in realtime krijgen 7 dagen toegang tot gegevens in het meer, voornamelijk om gegevens over instaptoegang tot profielen en voor ad-hocquery&#39;s te vergemakkelijken.

* Er zijn geen TTL&#39;s voor de gegevens in het meer voor klanten van Customer Journey Analytics. Customer Journey Analytics-gebruikers kunnen echter zelf een aangepast retentievenster instellen in Customer Journey Analytics wanneer ze een verbinding maken.

* De Opslag van het profiel in Echt - tijd CDP staat voor klant-configureerbare TTLs toe. Klanten kunnen deze TTL wijzigen in wat ze nodig hebben om binnen hun licentierechten te blijven.

## Verschillen in de latentie bij het opnemen van gegevens

Customer Journey Analytics beschikt nog niet over de real-time mogelijkheden van CDP in real-time en als gevolg hiervan bevat Customer Journey Analytics-rapportage enige vertraging voordat gegevens beschikbaar zijn voor rapportage of het creëren van een publiek. CDP in real time verwerkt gegevens door verschillende systemen die verschillende latentie hebben.
