---
description: Verklaart welke factoren de consistentie van metriek en kijkcijfers van het publiekslidmaatschap tussen Real-time Customer Data Platform (in real time CDP) en Customer Journey Analytics beïnvloeden.
title: De consistentie van metriek en het aantal van het publiekslidmaatschap tussen CDP In real time en Customer Journey Analytics
role: Admin
feature: Basics
exl-id: 13d972bc-3d32-414e-a67d-845845381c3e
source-git-commit: 46d799ad2621d83906908a3f60a59a1027c6518c
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---


# Consistentie van metriek en het aantal van het publiekslidmaatschap tussen CDP In real time en Adobe Customer Journey Analytics

In real-world scenario&#39;s, kan de consistentie van metriek en het aantal van het publiekslidmaatschap over Real-time Customer Data Platform (Real-time CDP) en Customer Journey Analytics niet worden gewaarborgd. In dit document wordt uitgelegd waarom.

Wanneer het vergelijken van het aantal van het publiekslidmaatschap tussen CDP in real time en Customer Journey Analytics, is het belangrijk om in mening de verschillende doelstellingen van deze twee hulpmiddelen te houden. CDP in real time gebruikt gegevens van het klantenprofiel om digitale ervaringen aan individuele consumenten te richten, terwijl de Customer Journey Analytics wordt ontworpen om gebruikers te helpen patronen in zeer belangrijke bedrijfsmetriek en segmenten begrijpen. Terwijl het publiek dat van Customer Journey Analytics aan in real time CDP publiceert een gebruiker van deze hulpmiddelen toestaat om een inzicht gemakkelijk en native &quot;te activeren&quot;, die uit lessen voordeel halen die in Customer Journey Analytics worden verkregen, dienen deze hulpmiddelen niettemin fundamenteel verschillende doeleinden.

## Verschillen in identiteitsconfiguraties

CDP en Customer Journey Analytics in real time delen niet de zelfde definitie van een persoon vandaag. Real-time CDP vertrouwt volledig op de informatie in [Naamgrafiek](https://experienceleague.adobe.com/docs/platform-learn/tutorials/identities/understanding-identity-and-identity-graphs.html) om een samengevoegd profiel te maken.

Customer Journey Analytics kan worden gevormd om te gebruiken [Stiksel](../stitching/overview.md) die herkenningstekens uit datasets in het gegevensmeer haalt en douanelogica toepast om hen samen te verbinden.

In de toekomst zal Customer Journey Analytics de Grafiek van de Identiteit kunnen gebruiken.

## Verschillen in configuratie gegevensset

U kunt verkiezen om sommige gegevens in real time CDP en wat in Customer Journey Analytics te zetten; vaak, kiezen de klanten om meer historische gegevens in Customer Journey Analytics te zetten dan voor Echt - tijd CDP relevant is. Andere datasets zouden voor Echt - tijd CDP dan voor Customer Journey Analytics relevanter kunnen zijn.

## Verschillen in verwerkingsconfiguratie

Met Customer Journey Analytics kunt u tijdens de query uitgebreide gegevens wijzigen, zoals velden combineren, velden splitsen en andere bewerkingen zoals include/Excludes, substrings, value deduplicatie, sessionization en filter op rijniveau.

CDP in real time biedt een verschillende reeks hulpmiddelen van de gegevensmanipulatie aan. Zij is van toepassing [beleid samenvoegen](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/overview.html) om te bepalen welke gegevens voorrang krijgen en welke gegevens zullen worden gecombineerd om een verenigde mening van een persoon tot stand te brengen.

## Verschillen in TTL (Tijd aan Levende) en gegevensopname

Zelfs als de datasets in Echt - tijd CDP en Customer Journey Analytics het zelfde zijn, kan CDP in real time slechts een zeer beperkt venster van geschiedenis houden. Customer Journey Analytics heeft daarentegen waarschijnlijk jaren aan gegevens. Daarnaast:

* De Customer Journey Analytics en de klanten in real time CDP kunnen de vensters van het douanebehoud voor gegevens, onafhankelijk van elkaar plaatsen.

* CDP en Customer Journey Analytics in real time hebben verschillende logica voor het opnemen van gegevens. Customer Journey Analytics negeert records zonder persoon-id of tijdstempel en heeft strikte limieten aan het aantal records dat één profiel/persoon kan hebben.

* CDP-klanten in realtime krijgen 7 dagen toegang tot gegevens in het meer, voornamelijk om gegevens over instaptoegang tot profielen en voor ad-hocquery&#39;s te vergemakkelijken.

* Er zijn geen TTLs voor de gegevens in het meer voor klanten van de Customer Journey Analytics. Gebruikers van Customers Journey Analytics kunnen echter zelf een aangepast retentievenster in Customer Journey Analytics instellen wanneer ze een verbinding maken.

* De Opslag van het profiel in Echt - tijd CDP staat voor klant-configureerbare TTLs toe. Klanten kunnen deze TTL wijzigen in wat ze nodig hebben om binnen hun licentierechten te blijven.

## Verschillen in de latentie bij het opnemen van gegevens

Customer Journey Analytics heeft nog niet de mogelijkheden in real time van CDP en dientengevolge, omvat de Customer Journey Analytics rapportering één of andere latentie alvorens de gegevens voor het melden of publieksverwezenlijking beschikbaar zijn. CDP in real time verwerkt gegevens door verschillende systemen die verschillende latentie hebben.
