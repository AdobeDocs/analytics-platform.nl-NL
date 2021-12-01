---
title: Opties voor gegevensinvoer voor Customer Journey Analytics
description: Begrijp de verschillende manieren u gegevens in Customer Journey Analytics kunt opnemen
exl-id: 4a47c587-f48e-4e29-b97f-00c7d7e6972c
solution: Customer Journey Analytics
source-git-commit: faaf3d19ed37019ba284b41420628750cdb413b8
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 2%

---

# Opties voor gegevensinvoer voor Customer Journey Analytics

U hebt een aantal opties voor het opnemen van gegevens in Customer Journey Analytics. Sommigen gaan ervan uit dat u de traditionele Adobe Analytics-gegevens wilt verplaatsen. Sommigen gaan ervan uit dat u gegevens rechtstreeks vanuit Adobe Experience Platform invoert. Deze naslaggids bevat stappen op hoog niveau die moeten worden gevolgd, met koppelingen naar meer gedetailleerde informatie.

## Gegevens uit traditionele Adobe Analytics verzamelen

Deze workflow maakt gebruik van de Adobe Analytics Data Connector en is afhankelijk van het feit of u DTM of Launch gebruikt als tagbeheer.

### Via Launch

1. [Een gegevenslaag maken](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html), als je dat nog niet hebt gedaan. Een gegevenslaag is een raamwerk van JavaScript-objecten op uw site dat alle variabelenwaarden bevat die in uw implementatie worden gebruikt. Hierdoor kunt u uw implementatie beter beheren en eenvoudiger onderhouden.
1. Gebruiken [Adobe Experience Platform Launch](https://experienceleague.adobe.com/docs/analytics/implementation/launch/overview.html) om code op uw plaats voor gegevensinzameling uit te voeren, als u nog niet hebt. Launch is een oplossing voor tagbeheer waarmee u naast andere vereisten voor codering ook analytische code kunt implementeren. De lancering biedt integratie met andere oplossingen en producten aan, en laat u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.
1. Een [Adobe Analytics-bronaansluiting](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) in Adobe Experience Platform. Deze bronschakelaar zal uw gegevens van Analytics in Experience Platform in een gestandaardiseerd kader opnemen genoemd [XDM-systeem (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl).
1. Gebruiken [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer verbindingen en gegevensweergaven te maken die uw rapportage via meerdere kanalen mogelijk maken.

## Gegevens verzamelen via de Adobe Experience Platform Web SDK en het Edge Network

[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en) is een JavaScript-bibliotheek aan de clientzijde waarmee klanten van Adobe Experience Cloud via het Adobe Experience Platform Edge Network kunnen communiceren met de verschillende services in de Experience Cloud.

1. [De extensie AEP Web SDK configureren in Launch](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html?lang=en) gegevens vanuit wegeigenschappen naar de Adobe Experience Cloud verzenden via het Adobe Experience Platform Edge Network.
1. Gebruiken [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer verbindingen en gegevensweergaven te maken die uw rapportage via meerdere kanalen mogelijk maken.

## Ingrepen gegevens met batch-opname en streaming opname

Adobe Experience Platform brengt gegevens uit meerdere bronnen samen om marketers te helpen het gedrag van hun klanten beter te begrijpen. De Ingestie van Gegevens van Adobe Experience Platform vertegenwoordigt de veelvoudige methodes waardoor Platform gegevens uit deze bronnen inneemt, evenals hoe die gegevens binnen het meer van Gegevens voor gebruik door de stroomafwaartse diensten van het Platform worden voortgeduurd.

### Inname in batch

1. Instellen [Batchinname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/batch/overview.html?lang=en#batch) om u toe te staan om gegevens in Adobe Experience Platform in te voeren als batchbestanden. Gegevens die worden opgenomen kunnen de profielgegevens van een vlak dossier in een systeem van CRM (zoals een parquetdossier), of gegevens zijn die aan een bekend schema in het register van het Model van de Gegevens van de Ervaring (XDM) in overeenstemming zijn.
1. Gebruiken [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer verbindingen en gegevensweergaven te maken die uw rapportage via meerdere kanalen mogelijk maken.

### Streaming opname

1. Instellen [Streaming opname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=en#streaming) om gegevens van client- en serverapparaten in real-time naar het Experience Platform te verzenden.
1. Gebruiken [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer verbindingen en gegevensweergaven te maken die uw rapportage via meerdere kanalen mogelijk maken.

## Google Analytics-gegevens inbrengen om te analyseren in Customer Journey Analytics

Bekijk deze zelfstudie over hoe u [Gegevens van Google Analytics analyseren met Customer Journey Analytics](https://experienceleague.adobe.com/docs/platform-learn/comprehensive-technical-tutorial/module16/ex5.html?lang=en#objectives) voor gedetailleerde stappen.

## De Bulk API van de Invoeging van Gegevens van het gebruik om gegevens in Analytics te krijgen, dan wordt opgenomen via de Bron van Adobe Schakelaar in Experience Platform

1. [Opsommings-API gebruiken](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) om gegevens van verzamelingen op de server naar Adobe Analytics te verzenden. Hiermee kunt u CSV-bestanden met gebeurtenisgegevens verzenden.
1. [Een Adobe Analytics-bronaansluiting maken](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en) deze consumentengegevens naar Adobe Experience Platform te brengen.
1. Gebruiken [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer verbindingen en gegevensweergaven te maken die uw rapportage via meerdere kanalen mogelijk maken.
