---
description: Verklaart welke factoren de consistentie van metriek en kijkcijfers van het publiekslidmaatschap tussen Real-time Customer Data Platform (in real time CDP) en CJA beïnvloeden.
title: Consistentie van metriek en het tellen van het publieksenlidmaatschap tussen CDP In real time en CJA
role: Admin
feature: CJA Basics
exl-id: 13d972bc-3d32-414e-a67d-845845381c3e
source-git-commit: 21d51ababeda7fe188fbd42b57ef3baf76d21774
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---


# Consistentie van metriek en het tellen van het publieksenlidmaatschap tussen CDP In real time en CJA

In real-world scenario&#39;s, kan de consistentie van metriek en het aantal van het publiekslidmaatschap over Real-time Customer Data Platform (Real-time CDP) en Customer Journey Analytics (CJA) niet worden gewaarborgd. In dit document wordt uitgelegd waarom.

## CJA gebruikt nog geen identiteitsgrafiek

CDP en CJA delen niet de zelfde definitie van een persoon vandaag. CJA gebruikt nog niet [Identiteitsgrafiek](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=en) haar definitie van een persoon mede te delen. CDP in real time baseert zich volledig op de informatie in de Grafiek van de Identiteit om een samengevoegd profiel te bouwen.

CJA gebruikt een methode die [Veldgebaseerde plaatsing](/help/connections/cca/overview.md) die herkenningstekens uit datasets in het gegevensmeer haalt en douanelogica toepast om hen samen te verbinden. In de tussenliggende toekomst zal CJA naar verwachting beginnen gebruik te maken van [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=en) de uitvoer naar het gegevens meer, die voor een gedeeld begrip van identiteit over CDP en CJA in real time toestaan.

>[!IMPORTANT]
>
>Als u van de Adobe Experience Platform Identity Service de identiteitsbron van de waarheid maakt voor alle Adobe Experience Platform-toepassingen, worden de meetgegevens niet automatisch consistent in alle toepassingen. Lees verder om te leren waarom.

## Flexibiliteit van toepassingsgegevens

Experience Platform past geen strenge handhaving toe om de gegevens tussen het Profiel van de Klant in real time en het meer van Gegevens te houden. In sommige gevallen worden gegevens gebruikt in [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/profile/profile-overview.html?lang=en) (activering), terwijl anderen buiten de [gegevensmeer](https://business.adobe.com/blog/basics/data-lake) (rapportage- en queryservice).

CDP-klanten in realtime beschikken doorgaans niet over 100% van de gegevens in het Adobe Experience Platform-datumpigment dat in Profile wordt uitgevoerd. Dit is door ontwerp - de klanten zouden gegevens in het meer voor Profiel specifiek moeten toelaten. CJA staat gegevensanalisten toe om vrij te selecteren welke gegevens zij voor analyse van het gegevensmeer willen binnen brengen, onafhankelijk van wat voor CDP in real time wordt toegelaten.

## Toepassingsspecifieke modifiers

CJA staat voor uitgebreide gegevenswijziging bij vraagtijd toe, zoals het combineren van gebieden, het splitsen van gebieden uit elkaar, en andere manipulaties zoals muntomzettingen, waarde deduplicatie, zittingsbepaling, en rij-vlakke het filtreren. Deze mogelijkheden zijn niet beschikbaar voor CDP.

Op dezelfde manier wordt CDP in real time toegepast [beleid samenvoegen](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/overview.html?lang=en) om te bepalen welke gegevens voorrang krijgen en welke gegevens zullen worden gecombineerd om een verenigde mening van een persoon tot stand te brengen. Deze configuraties bevinden zich stevig in de logica van elke toepassing en worden niet gedeeld.

## Leestijd versus schrijven-tijd gedrag

CDP in real time vereist punt-in-tijd profielstitching gebruikend de recentste grafiek van identiteitskaart.

* CDP in real time wordt ontworpen om profielinformatie in real time voor activering samen te stellen.

* Het kan in real time alle veranderingen in de vastgestelde herkenningstekens voor een bepaalde gebruiker aanpassen.

* Het terugkijkvenster wordt gecontroleerd door de segmentdefinitie.

CJA vereist dat gegevens bij schrijftijd worden vastgezet gebruikend de uitvoer van de Grafiek van identiteitskaart.

* CJA past complexe voorverwerkingsstappen toe, zoals indexeren, arceren en groeperen, voordat de gegevens klaar zijn voor analyse.

* De persoon-identificator voor een bepaalde gebruiker is een kritische input voor de fasen van de voorbehandeling; het wijzigen van de identificatiecode van de persoon heeft aanzienlijke opwerkingskosten.

* Het terugkijkvenster wordt gecontroleerd op toepassingsniveau.

## Verschillen in TTL (Tijd aan Levende) en gegevensopname

Zelfs als de datasets in Echt - tijd CDP en CJA het zelfde zijn, kan CDP in real time slechts een zeer beperkt venster van geschiedenis houden. CJA heeft daarentegen waarschijnlijk jaren aan gegevens. Daarnaast:

* CJA en klanten in real time CDP kunnen de vensters van het douanebehoud voor gegevens, onafhankelijk van elkaar plaatsen.

* CDP en CJA in real time hebben verschillende logica voor het opnemen van gegevens. CJA negeert records zonder een persoon-id of tijdstempel en heeft strikte limieten aan het aantal records dat één profiel/persoon kan hebben.

* CDP-klanten in realtime krijgen 7 dagen toegang tot gegevens in het meer, voornamelijk om gegevens over instaptoegang tot profielen en voor ad-hocquery&#39;s te vergemakkelijken.

* Er zijn geen TTLs voor de gegevens in het meer voor klanten CJA. CJA-gebruikers kunnen echter zelf een aangepast retentievenster instellen in CJA wanneer ze een verbinding maken.

* De Opslag van het profiel in Echt - tijd CDP staat voor klant-configureerbare TTLs toe. Klanten kunnen deze TTL wijzigen in wat ze nodig hebben om binnen hun licentierechten te blijven.

## Verschillen in verwerking van GDPR (algemene gegevensbeschermingsverordening)

Gegevensverwerkingslogica voor GDPR en gegevenshygiëne in real-time CDP en data Lake is heel anders. We werken aan één enkele aanpak.

## Verschillen in de latentie bij het opnemen van gegevens

CJA-rapportage bevat enige vertraging voordat gegevens beschikbaar zijn voor rapportage of het creëren van een publiek. CDP in real time verwerkt gegevens door verschillende systemen die verschillende latentie hebben.
