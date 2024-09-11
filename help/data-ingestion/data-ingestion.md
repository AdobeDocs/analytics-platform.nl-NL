---
title: Overzicht van gegevensinscriptie
description: Begrijp de verschillende manieren dat u gegevens in Customer Journey Analytics kunt opnemen
solution: Customer Journey Analytics
feature: Basics
exl-id: ead96b72-40f1-4ce9-8d91-c8ceea6c4458
role: Admin
source-git-commit: ac1d8a191bbad049ada246937364aeb7f8b275a0
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# Overzicht van gegevensinvoer

Er zijn verschillende opties voor het opnemen van gegevens in de Customer Journey Analytics. Sommigen gaan ervan uit dat u de traditionele Adobe Analytics-gegevens wilt verplaatsen. Sommigen gaan ervan uit dat u gegevens gebruikt die u in Adobe Experience Platform hebt ingevoerd.

>[!IMPORTANT]
>
>In alle scenario&#39;s, worden de gegevens u _in Customer Journey Analytics wilt gebruiken_ eigenlijk ingebed _in Adobe Experience Platform._

Zie de architectuur van de Customer Journey Analytics op hoog niveau vroeger in [ Overzicht ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) wordt getoond:

![ die de architectuur van de Customer Journey Analytics in deze sectie wordt beschreven ](./assets/cja-architecture.png)

De dataset in de architectuur hierboven kan uit diverse bronnen voortkomen:

- partijgegevens,

- streaminggegevens,

- gegevens van een huidige Adobe Analytics-implementatie;

- gegevens van het bijhouden van uw website/mobiele toepassing met de Adobe Experience Platform Web/Mobile SDK;

- gegevens van het bijhouden van een bureaubladtoepassing, consolespel, set-top box of IoT-apparaat met de Adobe Experience Platform Edge Network Server-API, of

- gegevens die afkomstig zijn van een externe gegevensaanbieder waarvoor de Adobe een bronaansluiting biedt.

Je kan veel van deze datasets hebben.

In dit gedeelte van de documentatie vindt u snel handleidingen voor verschillende scenario&#39;s.

## Ingestieprioriteit en latentie

U kunt uw gebeurtenisgegevens binnen 90 minuten in de Customer Journey Analytics opnemen, ongeacht of de gegevens 24 uur, 48 uur of 7 dagen oud zijn.

Merk op dat dit vermogen op het SKU-pakket verschilt uw bedrijf kocht:

- Prioritaire Grondbeginselen van de Ingestie: 24-uur oude gegevens binnen de verwerking van 90 minuten SLT (beschikbaar voor **CJA Stichting** en Uitgezochte CJA **)**

- Prioritaire Intermediate van de Ingestie: 72-uur oude gegevens binnen 90 minuten SLT verwerking (beschikbaar voor **CJA Primeur**)

- Prioritaire Geavanceerde Ingestie: 1 week oude gegevens binnen 90 minuten SLT verwerking (beschikbaar voor **CJA Ultimate**)

## Gegevens van traditionele Adobe Analytics verzamelen en gebruiken

Adobe Analytics is al geïmplementeerd en u wilt deze gegevens in Adobe Experience Platform opnemen en gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in de Customer Journey Analytics.

Zie [ samenvatten en gegevens van traditionele Adobe Analytics ](./analytics.md) voor meer informatie gebruiken.


## Gegevens via de Edge Network invoegen en gebruiken

### De SDK van Adobe Experience Platform Web gebruiken

U wilt uw website analyseren met de technologie van de Adobe, potentieel migrerend van een andere oplossing of begin het gedrag van uw persoon te volgen. U wilt de best practices van de Adobe voor de implementatie volgen. Hierbij worden de SDK&#39;s en Edge Network van Adobe Experience Platform gebruikt om de gegevens in te voeren. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in de Customer Journey Analytics.

Zie [ Samenvatten en gegevens gebruiken via het Web SDK van Adobe Experience Platform ](./aepwebsdk.md) voor meer informatie.

### De Adobe Experience Platform Mobile SDK gebruiken

U wilt uw mobiele app analyseren met behulp van Adobe-technologie, waarbij u mogelijk van een andere oplossing migreert of het gedrag van een persoon in de app vanaf het begin kunt volgen. U wilt de best practices van de Adobe voor de implementatie volgen. Hierbij worden de SDK&#39;s en Edge Network van Adobe Experience Platform gebruikt om de gegevens in te voeren. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in de Customer Journey Analytics.

Zie [ Samenvatten en gegevens gebruiken via Adobe Experience Platform Mobile SDK ](./aepmobilesdk.md) voor meer informatie.

### De Adobe Experience Platform Edge Network Server-API gebruiken

U wilt uw desktoptoepassing analyseren, zoals deze wordt afgespeeld op een spelconsole, het gebruik van een videostreamingtoepassing op een set-top box of uw IoT-apparaat met Adobe-technologie. Mogelijk migreert u van een andere oplossing of volgt u het gedrag van een persoon op deze apparaten vanaf het begin. U wilt de beste praktijken van de Adobe voor implementatie volgen, die de Server APIs en de Edge Network van de Edge Network van Adobe Experience Platform gebruikt, om de gegevens in te voeren. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in de Customer Journey Analytics.

Zie [ samenvatten en gegevens gebruiken via de Server API van de Edge Network van Adobe Experience Platform ](./serverapi.md) voor meer informatie.

## Batchgegevens invoegen en gebruiken

U hebt relevante beschikbare partijgegevens die details verstrekken die u kunnen helpen klantengedrag beter begrijpen en klanteninteractie analyseren. De voorbeelden van dergelijke partijgegevens zijn vlakke dossiers in CSV, JSON, of formaat van het Pakket van een systeem van CRM, loyaliteitstoepassing, of andere oplossing waarvoor de Adobe momenteel geen bronschakelaar verstrekt. Door deze batchgegevens in Adobe Experience Platform te importeren, kunt u deze gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in de Customer Journey Analytics.

Zie [ Samenvatten en gebruikspartijgegevens ](./batch.md) voor meer informatie.

## Streaming gegevens invoegen en gebruiken

U hebt een relevante gegevensbron zoals een systeem van CRM, ERP, of een andere bron die details verstrekt die u kunnen helpen klantengedrag beter begrijpen en klanteninteractie analyseren. Die gegevensbron kan communiceren via HTTP of openbare cloudstreaminginfrastructuur, maar waarvoor de Adobe momenteel geen bronaansluiting biedt. Door deze streaminggegevens in real-time in Adobe Experience Platform te installeren, kunt u deze gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [ Samenvatten en gebruik het stromen gegevens ](./streaming.md) voor meer informatie.

## Gegevens verzamelen en gebruiken met behulp van bronconnectors

U hebt gegevens beschikbaar bij een bron die door een bronschakelaar wordt gesteund. Source-connectors zijn configureerbare configuraties waarmee u gegevens van de Adobe, de toepassing van de eerste partij en van derden in Adobe Experience Platform kunt invoeren. Zie [ Source connectors overzicht ](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html) voor een overzicht van beschikbare bronschakelaars. Met de bronaansluiting kunt u eenvoudig gegevens van de bron in Adobe Experience Platform opnemen en deze vervolgens gebruiken, combineren en analyseren met gegevens van andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [ samenvatten en gegevens gebruiken gebruikend bronschakelaars ](./sources.md) voor meer informatie.
