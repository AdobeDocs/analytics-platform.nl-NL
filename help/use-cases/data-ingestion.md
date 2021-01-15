---
title: Opties voor gegevensinvoer voor Customer Journey Analytics
description: Begrijp de verschillende manieren u gegevens in Customer Journey Analytics kunt opnemen
translation-type: tm+mt
source-git-commit: 8a3a868ff4e2fbbcdf83ff7769382c6a92f78ec2
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 1%

---


# Opties voor gegevensinvoer voor Customer Journey Analytics

U hebt een aantal opties voor het opnemen van gegevens in Customer Journey Analytics. Sommigen gaan ervan uit dat u de traditionele Adobe Analytics-gegevens wilt verplaatsen. Sommigen gaan ervan uit dat u gegevens rechtstreeks vanuit Adobe Experience Platform invoert. Deze naslaggids bevat stappen op hoog niveau die moeten worden gevolgd, met koppelingen naar meer gedetailleerde informatie.

## Gegevens uit traditionele Adobe Analytics verzamelen

Deze workflow maakt gebruik van de Adobe Analytics Data Connector en is afhankelijk van het feit of u DTM of Launch gebruikt als tagbeheer.

### Via dynamisch tagbeheer (DTM)

1. [Maak een gegevenslaag](https://docs.adobe.com/content/help/en/analytics/implementation/prepare/data-layer.html) als u dat nog niet hebt gedaan. Een gegevenslaag is een raamwerk van JavaScript-objecten op uw site dat alle variabelenwaarden bevat die in uw implementatie worden gebruikt. Hierdoor kunt u uw implementatie beter beheren en eenvoudiger onderhouden.
1. Gebruik [DTM](https://docs.adobe.com/content/help/en/analytics/implementation/other/dtm/dtm-implementation-overview.html) om code op uw plaats voor gegevensinzameling uit te voeren, als u nog niet hebt. Het dynamische Beheer van de Markering verstrekt één enkele gegevenslaag die gegevens uit veelvoudige bronnen duwt.
1. Maak een [Adobe Analytics-bronconnector](https://docs.adobe.com/content/help/en/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) in Adobe Experience Platform. Deze bronschakelaar zal uw gegevens van Analytics in Experience Platform in een gestandaardiseerd kader opnemen genoemd [Systeem van de Gegevens van de Ervaring (XDM)](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html).
1. Gebruik [Customer Journey Analytics](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-overview/cja-getting-started.html) om één of meerdere verbindingen en gegevensmeningen tot stand te brengen die uw kanaalrapportering zullen informeren.

### Via Launch

1. [Maak een gegevenslaag](https://docs.adobe.com/content/help/en/analytics/implementation/prepare/data-layer.html) als u dat nog niet hebt gedaan. Een gegevenslaag is een raamwerk van JavaScript-objecten op uw site dat alle variabelenwaarden bevat die in uw implementatie worden gebruikt. Hierdoor kunt u uw implementatie beter beheren en eenvoudiger onderhouden.
1. Gebruik [Adobe Experience Platform Launch](https://docs.adobe.com/content/help/en/analytics/implementation/launch/overview.html) om code op uw plaats voor gegevensinzameling uit te voeren, als u nog niet hebt. Launch is een oplossing voor tagbeheer waarmee u naast andere vereisten voor codering ook analytische code kunt implementeren. De lancering biedt integratie met andere oplossingen en producten aan, en laat u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.
1. Maak een [Adobe Analytics-bronconnector](https://docs.adobe.com/content/help/en/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) in Adobe Experience Platform. Deze bronschakelaar zal uw gegevens van Analytics in Experience Platform in een gestandaardiseerd kader opnemen genoemd [Systeem van de Gegevens van de Ervaring (XDM)](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html).
1. Gebruik [Customer Journey Analytics](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-overview/cja-getting-started.html) om één of meerdere verbindingen en gegevensmeningen tot stand te brengen die uw kanaalrapportering zullen informeren.

## Gegevens verzamelen via de Adobe Experience Platform Web SDK en het Edge Network

[Adobe Experience Platform Web ](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en) SDK is een JavaScript-bibliotheek aan de clientzijde waarmee klanten van Adobe Experience Cloud via het Adobe Experience Platform Edge Network kunnen communiceren met de verschillende services in de Experience Cloud.

1. [Configureer de AEP Web SDK-extensie in ](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html?lang=en#configure-the-aep-web-sdk-extension) Launchto en verzend gegevens naar de Adobe Experience Cloud vanuit wegeigenschappen via het Adobe Experience Platform Edge Network.
1. Gebruik [Customer Journey Analytics](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-overview/cja-getting-started.html) om één of meerdere verbindingen en gegevensmeningen tot stand te brengen die uw kanaalrapportering zullen informeren.

## Ingrepen gegevens met batch-opname en streaming opname

Adobe Experience Platform brengt gegevens uit meerdere bronnen samen om marketers te helpen het gedrag van hun klanten beter te begrijpen. De Ingestie van Gegevens van Adobe Experience Platform vertegenwoordigt de veelvoudige methodes waardoor Platform gegevens uit deze bronnen inneemt, evenals hoe die gegevens binnen het meer van Gegevens voor gebruik door de stroomafwaartse diensten van het Platform worden voortgeduurd.

### Inname in batch

1. Stel [Batch-inname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/batch/overview.html?lang=en#batch) in zodat u gegevens als batchbestanden in Adobe Experience Platform kunt invoeren. Gegevens die worden opgenomen kunnen de profielgegevens van een vlak dossier in een systeem van CRM (zoals een parquetdossier), of gegevens zijn die aan een bekend schema in het register van het Model van de Gegevens van de Ervaring (XDM) in overeenstemming zijn.
1. Gebruik [Customer Journey Analytics](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-overview/cja-getting-started.html) om één of meerdere verbindingen en gegevensmeningen tot stand te brengen die uw kanaalrapportering zullen informeren.

### Streaming opname

1. Stel [Streaming opname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=en#streaming) in om gegevens van client- en serverapparaten in real-time naar het Experience Platform te verzenden.
1. Gebruik [Customer Journey Analytics](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-overview/cja-getting-started.html) om één of meerdere verbindingen en gegevensmeningen tot stand te brengen die uw kanaalrapportering zullen informeren.

## Google Analytics-gegevens inbrengen om te analyseren in Customer Journey Analytics

Bekijk deze zelfstudie over het [Analyseren van Google Analytics-gegevens met behulp van Customer Journey Analytics](https://experienceleague.adobe.com/docs/platform-learn/comprehensive-technical-tutorial/module16/ex5.html?lang=en#objectives) voor gedetailleerde stappen.

## De Bulk API van de Invoeging van Gegevens van het gebruik om gegevens in Analytics te krijgen, dan wordt opgenomen via de Bron van Adobe Schakelaar in Experience Platform

1. [Gebruik de ](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) API voor het invoegen van gegevens in bulk om de gegevens van de verzameling op de server naar Adobe Analytics te verzenden. Hiermee kunt u CSV-bestanden met gebeurtenisgegevens verzenden.
1. [Maak een Adobe Analytics-](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en) bronverbinding om deze consumentengegevens over te brengen naar Adobe Experience Platform.
1. Gebruik [Customer Journey Analytics](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-overview/cja-getting-started.html) om één of meerdere verbindingen en gegevensmeningen tot stand te brengen die uw kanaalrapportering zullen informeren.