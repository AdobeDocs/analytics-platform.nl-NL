---
title: Opties voor gegevensinvoer voor Customer Journey Analytics
description: Begrijp de verschillende manieren u gegevens in Customer Journey Analytics kunt opnemen
exl-id: 4a47c587-f48e-4e29-b97f-00c7d7e6972c
solution: Customer Journey Analytics
feature: Use Cases
role: Admin
source-git-commit: 46d799ad2621d83906908a3f60a59a1027c6518c
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 0%

---

# Opties voor gegevensinvoer voor Customer Journey Analytics

U hebt een aantal opties voor het opnemen van gegevens in de Customer Journey Analytics. Sommigen gaan ervan uit dat u de traditionele Adobe Analytics-gegevens wilt verplaatsen. Sommigen gaan ervan uit dat u gegevens rechtstreeks vanuit Adobe Experience Platform invoert. Deze naslaggids bevat stappen op hoog niveau die moeten worden gevolgd, met koppelingen naar gedetailleerdere informatie.

## Gegevens uit traditionele Adobe Analytics verzamelen

Deze workflow maakt gebruik van de bronaansluiting Analytics en is afhankelijk van het feit of u DTM of Launch gebruikt als tagbeheer.

### Via tags in Adobe Experience Platform (voorheen genoemd) [!UICONTROL Launch])

1. [Een gegevenslaag maken](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html), als je dat nog niet hebt gedaan. Een gegevenslaag is een raamwerk van JavaScript-objecten op uw site dat alle variabelenwaarden bevat die in uw implementatie worden gebruikt. Hierdoor kunt u uw implementatie beter beheren en eenvoudiger onderhouden.
1. Gebruiken [Adobe Experience Platform-tags](https://experienceleague.adobe.com/docs/analytics/implementation/launch/overview.html) om code op uw plaats voor gegevensinzameling uit te voeren, als u nog niet hebt. Met deze oplossing voor tagbeheer kunt u de analytische code naast andere vereisten voor codering implementeren. De markeringen bieden integratie met andere oplossingen en producten aan, en laten u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.
1. Een [Adobe Analytics-bronaansluiting](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) in Adobe Experience Platform. Deze bronschakelaar zal uw gegevens van Analytics in Experience Platform in een gestandaardiseerd kader opnemen genoemd [XDM-systeem (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl). Zie ook [Adobe Analytics-rapportsuite gebruiken in Customer Journey Analytics](/help/getting-started/aa-vs-cja/aa-data-in-cja.md).
1. Gebruiken [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer verbindingen en gegevensweergaven te maken die uw rapportage via meerdere kanalen mogelijk maken.

## Gegevens verzamelen via de Adobe Experience Platform Web SDK en het Edge Network

[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) is een JavaScript-bibliotheek aan de clientzijde waarmee klanten van Adobe Experience Cloud via het Adobe Experience Platform Edge Network kunnen communiceren met de verschillende services in het Experience Cloud.

1. [De extensie Adobe Experience Platform Web SDK configureren in tags](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html) gegevens vanuit wegeigenschappen naar de Adobe Experience Cloud verzenden via het Adobe Experience Platform Edge Network.
1. Gebruiken [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer [verbindingen](/help/connections/create-connection.md) en [gegevensweergaven](/help/data-views/data-views.md) die u op de hoogte brengt van uw rapportage via het andere kanaal.

## Ingrepen gegevens met batch-opname en streaming opname

Adobe Experience Platform brengt gegevens uit meerdere bronnen samen om marketers te helpen het gedrag van hun klanten beter te begrijpen. De Ingestie van Gegevens van Adobe Experience Platform vertegenwoordigt de veelvoudige methodes waardoor Platform gegevens uit deze bronnen opneemt, evenals hoe die gegevens binnen het meer van Gegevens voor gebruik door de stroomafwaartse diensten van het Platform worden voortgeduurd.

### Inname in batch

1. Instellen [Batchinname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/batch/overview.html#batch) om u toe te staan om gegevens in Adobe Experience Platform in te voeren als batchbestanden. Gegevens die worden opgenomen kunnen de profielgegevens van een vlak dossier in een systeem van CRM (zoals een parquetdossier), of gegevens zijn die aan een bekend schema in het register van het Model van de Gegevens van de Ervaring (XDM) in overeenstemming zijn.
1. Gebruiken [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer [verbindingen](/help/connections/create-connection.md) en [gegevensweergaven](/help/data-views/data-views.md) die u op de hoogte brengt van uw rapportage via het andere kanaal.

### Streaming opname

1. Instellen [Streaming opname](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html#streaming) om gegevens van client- en serverapparaten in real-time naar het Experience Platform te verzenden.
1. Gebruiken [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer [verbindingen](/help/connections/create-connection.md) en [gegevensweergaven](/help/data-views/data-views.md) die u op de hoogte brengt van uw rapportage via het andere kanaal.

## Gegevens van Googles Analytics opnemen om te analyseren in Customer Journey Analytics

Bekijk deze zelfstudie over hoe u [Gegevens van Googles Analytics analyseren met Customer Journey Analytics](https://experienceleague.adobe.com/docs/platform-learn/comprehensive-technical-tutorial-v22/module12/ex5.html) voor gedetailleerde stappen.

## De Bulk API van de Invoeging van Gegevens van het gebruik om gegevens in Analytics te krijgen, dan wordt opgenomen via de bron van Analytics schakelaar in Experience Platform

1. [Opsommings-API gebruiken](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) om gegevens van verzamelingen op de server naar Adobe Analytics te verzenden. Hiermee kunt u CSV-bestanden met gebeurtenisgegevens verzenden.
1. [Een Adobe Analytics-bronaansluiting maken](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) deze consumentengegevens naar Adobe Experience Platform te brengen.
1. Gebruiken [Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer [verbindingen](/help/connections/create-connection.md) en [gegevensweergaven](/help/data-views/data-views.md) die u op de hoogte brengt van uw rapportage via het andere kanaal.
