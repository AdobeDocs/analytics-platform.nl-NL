---
title: Overzicht van gegevensinscriptie
description: Begrijp de verschillende manieren waarop u gegevens in Customer Journey Analytics kunt opnemen
solution: Customer Journey Analytics
feature: Basics
exl-id: ead96b72-40f1-4ce9-8d91-c8ceea6c4458
role: Admin
source-git-commit: ec56bc657961b2e4e8318ab14cd676288398462f
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 0%

---

# Overzicht van gegevensinvoer

Er zijn verschillende opties voor het opnemen van gegevens in Customer Journey Analytics. Sommigen gaan ervan uit dat u de traditionele Adobe Analytics-gegevens wilt verplaatsen. Sommigen gaan ervan uit dat u gegevens gebruikt die u in Adobe Experience Platform hebt ingevoerd.

>[!IMPORTANT]
>
>In alle scenario&#39;s, worden de gegevens u _in Customer Journey Analytics_ wilt gebruiken eigenlijk _opgenomen_ in Adobe Experience Platform.


De Customer Journey Analytics-architectuur op hoog niveau wordt hier getoond:

![&#x200B; architectuur van Customer Journey Analytics &#x200B;](/help/getting-started/assets/cja-overview.svg)

Deze architectuur illustreert hoe u met de analyse van de Reis van de Klant kunt:

* Combineer veelvoudige datasets ![&#x200B; Gegevens &#x200B;](/help/assets/icons/Data.svg) in a [&#x200B; verbinding &#x200B;](/help/connections/overview.md).
* Bepaal en vorm dimensies ![&#x200B; Dimensies &#x200B;](/help/assets/icons/Dimensions.svg) en metrieke ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) in a [&#x200B; gegevensmening &#x200B;](/help/data-views/data-views.md), die op de gebieden beschikbaar van de datasets wordt gebaseerd u in uw verbinding bepaalde.
* Bouw rapporten ![&#x200B; ViewTable &#x200B;](/help/assets/icons/ViewTable.svg) en visualisaties (als lijn ![&#x200B; Lijn &#x200B;](/help/assets/icons/GraphTrend.svg) en gebied ![&#x200B; Gebied &#x200B;](/help/assets/icons/GraphAreaStacked.svg)) in [&#x200B; projecten &#x200B;](/help/analysis-workspace/home.md) gebaseerd op de afmetingen en metriek van uw gegevensmeningen.

De datasets in de architectuur kunnen uit diverse bronnen voortkomen:

* partijgegevens,

* streaminggegevens,

* gegevens van een huidige Adobe Analytics-implementatie;

* gegevens van het volgen van uw website/mobiele toepassing met Adobe Experience Platform Web/Mobile SDK;

* gegevens van het bijhouden van een bureaubladtoepassing, consolespel, set-top box of IoT-apparaat met de Adobe Experience Platform Edge Network Server-API, of

* gegevens die afkomstig zijn van een externe gegevensaanbieder waarvoor Adobe een bronaansluiting biedt.

Je kan veel van deze datasets hebben.

In dit gedeelte van de documentatie vindt u snel handleidingen voor verschillende scenario&#39;s.

## Ingestieprioriteit en latentie

U kunt uw gebeurtenisgegevens binnen 90 minuten (SLT) in Customer Journey Analytics opnemen, ongeacht of de gegevens 24 uur, 48 uur of 7 dagen oud zijn.

Merk op dat dit vermogen op het SKU-pakket verschilt uw bedrijf kocht:

* Prioritaire Grondbeginselen van de Ingestie: 24-uur oude gegevens binnen 90 minuten SLT verwerking (beschikbaar voor **de Stichting van CJA** en **Uitgezochte CJA**)

* Prioritaire Intermediate van de Ingestie: 72-uur oude gegevens binnen 90 minuten SLT verwerking (beschikbaar voor **CJA Prime**)

* Prioritaire Geavanceerde Ingestie: 1 week oude gegevens binnen 90 minuten SLT verwerking (beschikbaar voor **CJA Ultimate**)

## Gegevens van traditionele Adobe Analytics verzamelen en gebruiken

Adobe Analytics is al geïmplementeerd en u wilt deze gegevens in Adobe Experience Platform opnemen en gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [&#x200B; samenvatten en gegevens van traditionele Adobe Analytics &#x200B;](./analytics.md) voor meer informatie gebruiken.


## Gegevens via de Edge Network invoegen en gebruiken

### Adobe Experience Platform Web SDK gebruiken

U wilt uw website analyseren met Adobe-technologie, mogelijk migreren van een andere oplossing of het gedrag van uw persoon volgen. U wilt de best practices van Adobe voor de implementatie volgen, waarbij de SDK&#39;s van Adobe Experience Platform en Edge Network worden gebruikt om de gegevens in te voeren. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [&#x200B; samenvatten en gegevens gebruiken via het Web SDK van Adobe Experience Platform &#x200B;](./aepwebsdk.md) voor meer informatie.

### Adobe Experience Platform Mobile SDK gebruiken

U wilt uw mobiele app analyseren met Adobe-technologie, waarbij u mogelijk van een andere oplossing migreert of het gedrag van een persoon in de app vanaf het begin kunt volgen. U wilt de best practices van Adobe voor de implementatie volgen, waarbij de SDK&#39;s van Adobe Experience Platform en Edge Network worden gebruikt om de gegevens in te voeren. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [&#x200B; Samenvatten en gegevens gebruiken via Adobe Experience Platform Mobile SDK &#x200B;](./aepmobilesdk.md) voor meer informatie.

### De Adobe Experience Platform Edge Network Server-API gebruiken

U wilt uw desktoptoepassing analyseren, zoals deze wordt afgespeeld op een spelconsole, gebruik van een videostreamingtoepassing op een set-top box of uw IoT-apparaat met Adobe-technologie. Mogelijk migreert u van een andere oplossing of volgt u het gedrag van een persoon op deze apparaten vanaf het begin. U wilt de best practices van Adobe voor de implementatie volgen, waarbij de Adobe Experience Platform Edge Network Server-API&#39;s en Edge Network worden gebruikt, om de gegevens in te voeren. Vervolgens kunt u de opgenomen gegevens gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [&#x200B; samenvatten en gegevens gebruiken via de Server API van Adobe Experience Platform Edge Network &#x200B;](./serverapi.md) voor meer informatie.

## Batchgegevens invoegen en gebruiken

U hebt relevante beschikbare partijgegevens die details verstrekken die u kunnen helpen klantengedrag beter begrijpen en klanteninteractie analyseren. Voorbeelden van dergelijke batchgegevens zijn platte bestanden in de indeling CSV, JSON of Parquet van een CRM-systeem, loyaliteitstoepassing of een andere oplossing waarvoor Adobe momenteel geen bronaansluiting biedt. Door deze batchgegevens in Adobe Experience Platform te importeren, kunt u deze gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [&#x200B; Samenvatten en gebruikspartijgegevens &#x200B;](./batch.md) voor meer informatie.

## Streaming gegevens invoegen en gebruiken

U hebt een relevante gegevensbron zoals een systeem van CRM, ERP, of een andere bron die details verstrekt die u kunnen helpen klantengedrag beter begrijpen en klanteninteractie analyseren. Die gegevensbron kan communiceren via HTTP- of openbare cloudstreaminginfrastructuur, maar waarvoor Adobe momenteel geen bronaansluiting biedt. Door deze streaminggegevens in real-time in Adobe Experience Platform te installeren, kunt u ze gebruiken, combineren en analyseren met gegevens uit andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [&#x200B; Samenvatten en gebruik het stromen gegevens &#x200B;](./streaming.md) voor meer informatie.

## Gegevens verzamelen en gebruiken met behulp van bronconnectors

U hebt gegevens beschikbaar bij een bron die door een bronschakelaar wordt gesteund. Source-connectors zijn configureerbare configuraties waarmee u gegevens van Adobe, eersteklas- en externe toepassingen kunt opnemen in Adobe Experience Platform. Zie [&#x200B; Source connectors overzicht &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=nl-NL) voor een overzicht van beschikbare bronschakelaars. Met de bronaansluiting kunt u eenvoudig gegevens van de bron in Adobe Experience Platform opnemen en deze vervolgens gebruiken, combineren en analyseren met gegevens van andere kanalen en gegevensbronnen in Customer Journey Analytics.

Zie [&#x200B; samenvatten en gegevens gebruiken gebruikend bronschakelaars &#x200B;](./sources.md) voor meer informatie.

## Ad-hocgegevens invoegen en gebruiken

U hebt ad-hocgegevens beschikbaar die slechts één enkele dataset in Experience Platform vereisen en niet de configuratie van een schema van de Gegevens van de Ervaring van het Model (XDM) vereisen. Dit scenario wordt bedoeld als ad hoc schema. Ad-hocschema&#39;s worden gebruikt in verschillende gegevensinsluitingsworkflows voor Experience Platform, waaronder het innemen van CSV-bestanden en het maken van bepaalde soorten bronverbindingen.

Zie [&#x200B; Samenvatten en ad hoc gegevens gebruiken &#x200B;](./adhoc.md)

>[!MORELIKETHIS]
>
>Blog: [&#x200B; een Dichtere blik bij de Verwerking van Gegevens &amp; Opname in Adobe Customer Journey Analytics &#x200B;](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/a-closer-look-at-data-processing-amp-ingestion-in-adobe-customer/ba-p/665091)

