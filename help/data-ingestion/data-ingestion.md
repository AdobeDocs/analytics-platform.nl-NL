---
title: Overzicht van gegevensinname
description: Begrijp de verschillende manieren u gegevens in Customer Journey Analytics kunt opnemen
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: f910f8e810c5c5d6f4d43aff2b609d8bf6c131ca
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---


# Overzicht van gegevensinname

U hebt een aantal opties voor het opnemen van gegevens in Customer Journey Analytics. Sommigen gaan ervan uit dat u de traditionele Adobe Analytics-gegevens wilt verplaatsen. Sommigen gaan ervan uit dat u gegevens rechtstreeks in Adobe Experience Platform gebruikt.

>[!IMPORTANT]
>
>In alle scenario&#39;s, de gegevens u wilt _gebruiken_ in Customer Journey Analytics is _ingesloten_ in Adobe Experience Platform.


Zie de architectuur op hoog niveau van Customer Journey Analytics die vroeger in wordt getoond [Overzicht](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=en):

![Customer Journey Analytics](./assets/cja-architecture.png)

De dataset in de architectuur hierboven kan uit een verscheidenheid van bronnen voortkomen: batchgegevens, streaminggegevens, gegevens van een huidige Adobe Analytics-implementatie, gegevens van het bijhouden van uw website/mobiele app met de Adobe Experience Platform Web/Mobile SDK of gegevens van een externe gegevensaanbieder waarvoor Adobe een bronaansluiting biedt. Je kan veel van deze datasets hebben.

In dit gedeelte van de documentatie vindt u snel handleidingen voor een aantal scenario&#39;s.

## Gegevens uit traditionele Adobe Analytics verzamelen en gebruiken

Adobe Analytics is al geïmplementeerd en u wilt deze gegevens in Adobe Experience Platform opnemen en gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Gegevens uit traditionele Adobe Analytics verzamelen en gebruiken](./analytics.md) voor meer informatie .

## Gegevens verzamelen en gebruiken via de Adobe Experience Platform Web SDK en het Edge Network

U wilt uw website analyseren met Adobe-technologie, mogelijk migreren van een andere oplossing of het gedrag van uw bezoeker volgen. U wilt de beste praktijken van Adobe voor implementatie volgen, die Adobe Experience Platform SDKs en het Netwerk van de Rand gebruikt, om de gegevens op te nemen. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Gegevens verzamelen en gebruiken via de Adobe Experience Platform Web SDK en het Edge Network](./aepwebsdk.md) voor meer informatie .

## Batchgegevens invoegen en gebruiken

U hebt relevante beschikbare partijgegevens die details verstrekken die u kunnen helpen klantengedrag beter begrijpen en klanteninteractie analyseren. Voorbeelden van dergelijke batchgegevens zijn platte bestanden in CSV-, JSON- of Parquet-indeling van een CRM-systeem, loyaliteitstoepassing of andere oplossing waarvoor Adobe momenteel geen bronaansluiting biedt. Door deze batchgegevens in Adobe Experience Platform te importeren, kunt u deze gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Batchgegevens invoegen en gebruiken](./batch.md) voor meer informatie .

## Streaming gegevens invoegen en gebruiken

U hebt een relevante gegevensbron zoals een systeem van CRM, ERP of een andere bron die details verstrekt die u kunnen helpen klantengedrag beter begrijpen en klanteninteractie analyseren. Die gegevensbron kan communiceren via HTTP- of openbare cloudstreaminginfrastructuur, maar waarvoor Adobe momenteel geen bronaansluiting biedt. Door deze streaminggegevens in real-time in Adobe Experience Platform te installeren, kunt u ze gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Streaming gegevens invoegen en gebruiken](./streaming.md) voor meer informatie .

## Gegevens verzamelen en gebruiken met behulp van bronconnectors

U hebt gegevens beschikbaar bij een bron die door een bronschakelaar wordt gesteund. De bronschakelaars zijn configureerbare configuraties die u toestaan om gegevens van Adobe, eerste-partijtoepassing en derdetoepassing in Adobe Experience Platform in te voeren. Zie [Overzicht van bronconnectors](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=en) voor een overzicht van beschikbare bronschakelaars. Met de bronaansluiting kunt u eenvoudig gegevens van de bron in Adobe Experience Platform opnemen en deze vervolgens gebruiken, combineren en analyseren met gegevens van andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [Gegevens verzamelen en gebruiken met behulp van bronconnectors](./sources.md) voor meer informatie .

