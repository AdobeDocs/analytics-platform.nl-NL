---
title: Overzicht van gegevensinscriptie
description: Begrijp de verschillende manieren waarop u gegevens in Customer Journey Analytics kunt opnemen
solution: Customer Journey Analytics
feature: Basics
exl-id: ead96b72-40f1-4ce9-8d91-c8ceea6c4458
role: Admin
source-git-commit: 8071e8d5e1ab7e9cfc5037d710361a4d10285704
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 0%

---

# Overzicht van gegevensinvoer

Er zijn verschillende opties voor het opnemen van gegevens in Customer Journey Analytics. Sommigen gaan ervan uit dat u de traditionele Adobe Analytics-gegevens wilt verplaatsen. Sommigen gaan ervan uit dat u gegevens gebruikt die u in Adobe Experience Platform hebt ingevoerd.

>[!IMPORTANT]
>
>In alle scenario&#39;s, worden de gegevens u _in Customer Journey Analytics_ wilt gebruiken eigenlijk _opgenomen_ in Adobe Experience Platform.

Zie de architectuur op hoog niveau die van Customer Journey Analytics vroeger in [ wordt getoond Overzicht ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=nl-NL):

![ architectuur van Customer Journey Analytics die in deze sectie wordt beschreven ](./assets/cja-architecture.png)

De dataset in de architectuur hierboven kan uit diverse bronnen voortkomen:

- partijgegevens,

- streaminggegevens,

- gegevens van een huidige Adobe Analytics-implementatie;

- gegevens van het volgen van uw website/mobiele toepassing met Adobe Experience Platform Web/Mobile SDK;

- gegevens van het bijhouden van een bureaubladtoepassing, consolespel, set-top box of IoT-apparaat met de Adobe Experience Platform Edge Network Server-API, of

- gegevens die afkomstig zijn van een externe gegevensaanbieder waarvoor Adobe een bronaansluiting biedt.

Je kan veel van deze datasets hebben.

In dit gedeelte van de documentatie vindt u snel handleidingen voor verschillende scenario&#39;s.

## Ingestieprioriteit en latentie

U kunt uw gebeurtenisgegevens binnen 90 minuten (SLT) in Customer Journey Analytics opnemen, ongeacht of de gegevens 24 uur, 48 uur of 7 dagen oud zijn.

Merk op dat dit vermogen op het SKU-pakket verschilt uw bedrijf kocht:

- Prioritaire Grondbeginselen van de Ingestie: 24-uur oude gegevens binnen de verwerking van 90 minuten SLT (beschikbaar voor **CJA Stichting** en Uitgezochte CJA **)**

- Prioritaire Intermediate van de Ingestie: 72-uur oude gegevens binnen 90 minuten SLT verwerking (beschikbaar voor **CJA Prime**)

- Prioritaire Geavanceerde Ingestie: 1 week oude gegevens binnen 90 minuten SLT verwerking (beschikbaar voor **CJA Ultimate**)

## Gegevens van traditionele Adobe Analytics verzamelen en gebruiken

Adobe Analytics is al geïmplementeerd en u wilt deze gegevens in Adobe Experience Platform opnemen en gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [ samenvatten en gegevens van traditionele Adobe Analytics ](./analytics.md) voor meer informatie gebruiken.


## Gegevens via de Edge Network invoegen en gebruiken

### Adobe Experience Platform Web SDK gebruiken

U wilt uw website analyseren met Adobe-technologie, mogelijk migreren van een andere oplossing of het gedrag van uw persoon volgen. U wilt de best practices van Adobe voor de implementatie volgen, waarbij de SDK&#39;s van Adobe Experience Platform en Edge Network worden gebruikt om de gegevens in te voeren. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [ samenvatten en gegevens gebruiken via het Web SDK van Adobe Experience Platform ](./aepwebsdk.md) voor meer informatie.

### Adobe Experience Platform Mobile SDK gebruiken

U wilt uw mobiele app analyseren met Adobe-technologie, waarbij u mogelijk van een andere oplossing migreert of het gedrag van een persoon in de app vanaf het begin kunt volgen. U wilt de best practices van Adobe voor de implementatie volgen, waarbij de SDK&#39;s van Adobe Experience Platform en Edge Network worden gebruikt om de gegevens in te voeren. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [ Samenvatten en gegevens gebruiken via Adobe Experience Platform Mobile SDK ](./aepmobilesdk.md) voor meer informatie.

### De Adobe Experience Platform Edge Network Server-API gebruiken

U wilt uw desktoptoepassing analyseren, zoals deze wordt afgespeeld op een spelconsole, gebruik van een videostreamingtoepassing op een set-top box of uw IoT-apparaat met Adobe-technologie. Mogelijk migreert u van een andere oplossing of volgt u het gedrag van een persoon op deze apparaten vanaf het begin. U wilt de best practices van Adobe voor de implementatie volgen, waarbij de Adobe Experience Platform Edge Network Server-API&#39;s en Edge Network worden gebruikt, om de gegevens in te voeren. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [ samenvatten en gegevens gebruiken via de Server API van Adobe Experience Platform Edge Network ](./serverapi.md) voor meer informatie.

## Batchgegevens invoegen en gebruiken

U hebt relevante beschikbare partijgegevens die details verstrekken die u kunnen helpen klantengedrag beter begrijpen en klanteninteractie analyseren. Voorbeelden van dergelijke batchgegevens zijn platte bestanden in de indeling CSV, JSON of Parquet van een CRM-systeem, loyaliteitstoepassing of een andere oplossing waarvoor Adobe momenteel geen bronaansluiting biedt. Door deze batchgegevens in Adobe Experience Platform te importeren, kunt u deze gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [ Samenvatten en gebruikspartijgegevens ](./batch.md) voor meer informatie.

## Streaming gegevens invoegen en gebruiken

U hebt een relevante gegevensbron zoals een systeem van CRM, ERP, of een andere bron die details verstrekt die u kunnen helpen klantengedrag beter begrijpen en klanteninteractie analyseren. Die gegevensbron kan communiceren via HTTP- of openbare cloudstreaminginfrastructuur, maar waarvoor Adobe momenteel geen bronaansluiting biedt. Door deze streaminggegevens in real-time in Adobe Experience Platform te installeren, kunt u ze gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [ Samenvatten en gebruik het stromen gegevens ](./streaming.md) voor meer informatie.

## Gegevens verzamelen en gebruiken met behulp van bronconnectors

U hebt gegevens beschikbaar bij een bron die door een bronschakelaar wordt gesteund. Source-connectors zijn configureerbare configuraties waarmee u gegevens van Adobe, eersteklas- en externe toepassingen kunt opnemen in Adobe Experience Platform. Zie [ Source connectors overzicht ](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=nl-NL) voor een overzicht van beschikbare bronschakelaars. Met de bronaansluiting kunt u eenvoudig gegevens van de bron in Adobe Experience Platform opnemen en deze vervolgens gebruiken, combineren en analyseren met gegevens van andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [ samenvatten en gegevens gebruiken gebruikend bronschakelaars ](./sources.md) voor meer informatie.

>[!MORELIKETHIS]
>
>Blog: [ een Dichtere blik bij de Verwerking van Gegevens &amp; Opname in Adobe Customer Journey Analytics ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/a-closer-look-at-data-processing-amp-ingestion-in-adobe-customer/ba-p/665091)

