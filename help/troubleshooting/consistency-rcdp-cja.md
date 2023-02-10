---
description: Verklaart welke factoren de consistentie van metriek en kijkcijfers van het publiekslidmaatschap tussen Real-time Customer Data Platform (in real time CDP) en CJA beïnvloeden.
title: Consistentie van metriek en het tellen van het publieksenlidmaatschap tussen CDP In real time en CJA
role: Admin
feature: CJA Basics
exl-id: 13d972bc-3d32-414e-a67d-845845381c3e
source-git-commit: 34ee7954329d7dc8520031a977bb83d6e1bf3d3d
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---


# Consistentie van metriek en het tellen van het publieksenlidmaatschap tussen CDP In real time en CJA

In real-world scenario&#39;s, kan de consistentie van metriek en het aantal van het publiekslidmaatschap over Real-time Customer Data Platform (Real-time CDP) en Customer Journey Analytics (CJA) niet worden gewaarborgd. In dit document wordt uitgelegd waarom.

Wanneer het vergelijken van het aantal van het publiekslidmaatschap tussen CDP in real time en CJA, is het belangrijk om in mening de verschillende doelstellingen van deze twee hulpmiddelen te houden. CDP in real time gebruikt gegevens van het klantenprofiel om digitale ervaringen aan individuele consumenten te richten, terwijl CJA wordt ontworpen om gebruikers te helpen patronen in zeer belangrijke bedrijfsmetriek en segmenten begrijpen. Terwijl het publiek dat van CJA aan CDP in real time publiceert een gebruiker van deze hulpmiddelen toestaat om een inzicht gemakkelijk en native &quot;te activeren&quot;, die uit de lessen voordeel halen die in CJA worden verkregen, dienen deze hulpmiddelen niettemin fundamenteel verschillende doeleinden.

## Verschillen in identiteitsconfiguraties

CDP en CJA in realtime hebben vandaag niet dezelfde definitie van een persoon. Real-time CDP vertrouwt volledig op de informatie in [Identiteitsgrafiek](https://experienceleague.adobe.com/docs/platform-learn/tutorials/identities/understanding-identity-and-identity-graphs.html?lang=en) om een samengevoegd profiel te maken.

CJA kan worden geconfigureerd voor gebruik [Kanaaloverschrijdende analyse](/help/cca/overview.md) die herkenningstekens uit datasets in het gegevensmeer haalt en douanelogica toepast om hen samen te verbinden.

In de toekomst zal CJA de Grafiek van de Identiteit kunnen gebruiken.

## Verschillen in configuratie gegevensset

U kunt verkiezen om sommige gegevens in Real-time CDP en wat in CJA te zetten; vaak, verkiezen de klanten om meer historische gegevens in CJA te zetten dan voor CDP in real time relevant is. Andere datasets zouden voor in real time CDP dan voor CJA relevanter kunnen zijn.

## Verschillen in verwerkingsconfiguratie

CJA staat voor uitgebreide gegevenswijziging bij vraagtijd toe, zoals het combineren van gebieden, het splitsen van gebieden uit elkaar, en andere manipulaties zoals omvat/omvat/sluit, substrings, waarde deduplicatie, zittingsbepaling, en rij-vlakke het filtreren.

CDP in real time biedt een verschillende reeks hulpmiddelen van de gegevensmanipulatie aan. Zij is van toepassing [beleid samenvoegen](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/overview.html?lang=en) om te bepalen welke gegevens voorrang krijgen en welke gegevens zullen worden gecombineerd om een verenigde mening van een persoon tot stand te brengen.

## Verschillen in TTL (Tijd aan Levende) en gegevensopname

Zelfs als de datasets in Echt - tijd CDP en CJA het zelfde zijn, kan CDP in real time slechts een zeer beperkt venster van geschiedenis houden. CJA heeft daarentegen waarschijnlijk jaren aan gegevens. Daarnaast:

* CJA en klanten in real time CDP kunnen de vensters van het douanebehoud voor gegevens, onafhankelijk van elkaar plaatsen.

* CDP en CJA in real time hebben verschillende logica voor het opnemen van gegevens. CJA negeert records zonder een persoon-id of tijdstempel en heeft strikte limieten aan het aantal records dat één profiel/persoon kan hebben.

* CDP-klanten in realtime krijgen 7 dagen toegang tot gegevens in het meer, voornamelijk om gegevens over instaptoegang tot profielen en voor ad-hocquery&#39;s te vergemakkelijken.

* Er zijn geen TTLs voor de gegevens in het meer voor klanten CJA. CJA-gebruikers kunnen echter zelf een aangepast retentievenster instellen in CJA wanneer ze een verbinding maken.

* De Opslag van het profiel in Echt - tijd CDP staat voor klant-configureerbare TTLs toe. Klanten kunnen deze TTL wijzigen in wat ze nodig hebben om binnen hun licentierechten te blijven.

## Verschillen in de latentie bij het opnemen van gegevens

CJA heeft nog niet de mogelijkheden in real time van CDP in real time en dientengevolge, omvat CJA het melden wat latentie alvorens de gegevens voor het melden of publieksverwezenlijking beschikbaar zijn. CDP in real time verwerkt gegevens door verschillende systemen die verschillende latentie hebben.
