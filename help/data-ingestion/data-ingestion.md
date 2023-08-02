---
title: Overzicht van gegevensinscriptie
description: Begrijp de verschillende manieren dat u gegevens in Customer Journey Analytics kunt opnemen
solution: Customer Journey Analytics
feature: Basics
exl-id: ead96b72-40f1-4ce9-8d91-c8ceea6c4458
source-git-commit: 89841edb40f8ac89a3142588fede383b87d246f9
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 0%

---

# Overzicht van gegevensinscriptie

Er zijn verschillende opties voor het opnemen van gegevens in Customer Journey Analytics. Sommigen gaan ervan uit dat u de traditionele Adobe Analytics-gegevens wilt verplaatsen. Sommigen gaan ervan uit dat u gegevens gebruikt die u in Adobe Experience Platform hebt ingevoerd.

>[!IMPORTANT]
>
>In alle scenario&#39;s, de gegevens u wilt _gebruiken_ in Customer Journey Analytics is _ingesloten_ in Adobe Experience Platform.


Zie de architectuur op hoog niveau van Customer Journey Analytics die vroeger in wordt getoond [Overzicht](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=en):

![Customer Journey Analytics](./assets/cja-architecture.png)

De dataset in de architectuur hierboven kan uit diverse bronnen voortkomen:

- partijgegevens,

- streaminggegevens,

- gegevens van een huidige Adobe Analytics-implementatie;

- gegevens van het bijhouden van uw website/mobiele toepassing met de Adobe Experience Platform Web/Mobile SDK;

- gegevens van het bijhouden van een bureaubladtoepassing, consolespel, set-top box of IoT-apparaat met de Adobe Experience Platform Edge Network Server-API, of

- gegevens die afkomstig zijn van een externe gegevensaanbieder waarvoor Adobe een bronaansluiting biedt.

Je kan veel van deze datasets hebben.

In dit gedeelte van de documentatie vindt u snel handleidingen voor verschillende scenario&#39;s.

## Gegevens van traditionele Adobe Analytics verzamelen en gebruiken

Adobe Analytics is al geïmplementeerd en u wilt deze gegevens in Adobe Experience Platform opnemen en gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Gegevens van traditionele Adobe Analytics verzamelen en gebruiken](./analytics.md) voor meer informatie .


## Gegevens verzamelen en gebruiken via Edge Network

### De SDK van Adobe Experience Platform Web gebruiken

U wilt uw website analyseren met Adobe-technologie, mogelijk migreren van een andere oplossing of het gedrag van uw persoon volgen. U wilt de beste praktijken van Adobe voor implementatie volgen, die Adobe Experience Platform SDKs en het Netwerk van de Rand gebruikt, om de gegevens op te nemen. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Gegevens verzamelen en gebruiken via de Adobe Experience Platform Web SDK](./aepwebsdk.md) voor meer informatie .

### De Adobe Experience Platform Mobile SDK gebruiken

U wilt uw mobiele app analyseren met Adobe-technologie, waarbij u mogelijk van een andere oplossing migreert of het gedrag van een persoon in de app vanaf het begin kunt volgen. U wilt de beste praktijken van Adobe voor implementatie volgen, die Adobe Experience Platform SDKs en het Netwerk van de Rand gebruikt, om de gegevens op te nemen. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Gegevens verzamelen en gebruiken via de Adobe Experience Platform Mobile SDK](./aepmobilesdk.md) voor meer informatie .

### De Adobe Experience Platform Edge Network Server-API gebruiken

U wilt uw desktoptoepassing analyseren, zoals deze wordt afgespeeld op een spelconsole, het gebruik van een videostreaming toepassing op een set-top box of uw IoT-apparaat met Adobe-technologie. Mogelijk migreert u van een andere oplossing of volgt u het gedrag van een persoon op deze apparaten vanaf het begin. U wilt de best practices van de API voor Adobe voor de implementatie volgen, die de Adobe Experience Platform Edge Network Server en Edge Network gebruikt om gegevens in te voeren. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Gegevens verzamelen en gebruiken via de Adobe Experience Platform Edge Network Server-API](./serverapi.md) voor meer informatie .

## Batchgegevens invoegen en gebruiken

U hebt relevante beschikbare partijgegevens die details verstrekken die u kunnen helpen klantengedrag beter begrijpen en klanteninteractie analyseren. De voorbeelden van dergelijke partijgegevens zijn vlakke dossiers in CSV, JSON, of het formaat van het Pakket van een systeem van CRM, loyaliteitstoepassing, of andere oplossing waarvoor Adobe momenteel geen bronschakelaar verstrekt. Door deze batchgegevens in Adobe Experience Platform te importeren, kunt u deze gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Batchgegevens invoegen en gebruiken](./batch.md) voor meer informatie .

## Streaming gegevens invoegen en gebruiken

U hebt een relevante gegevensbron zoals een systeem van CRM, ERP, of een andere bron die details verstrekt die u kunnen helpen klantengedrag beter begrijpen en klanteninteractie analyseren. Die gegevensbron kan communiceren via HTTP- of openbare cloudstreaminginfrastructuur, maar waarvoor Adobe momenteel geen bronaansluiting biedt. Door deze streaminggegevens in real-time in Adobe Experience Platform te installeren, kunt u ze gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Streaming gegevens invoegen en gebruiken](./streaming.md) voor meer informatie .

## Gegevens verzamelen en gebruiken met behulp van bronconnectors

U hebt gegevens beschikbaar bij een bron die door een bronschakelaar wordt gesteund. De bronschakelaars zijn configureerbare configuraties die u toestaan om gegevens van Adobe, eerste-partijtoepassing en derdetoepassing in Adobe Experience Platform in te voeren. Zie [Overzicht van bronconnectors](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=en) voor een overzicht van beschikbare bronschakelaars. Met de bronaansluiting kunt u eenvoudig gegevens van de bron in Adobe Experience Platform opnemen en deze vervolgens gebruiken, combineren en analyseren met gegevens van andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Gegevens verzamelen en gebruiken met behulp van bronconnectors](./sources.md) voor meer informatie .
