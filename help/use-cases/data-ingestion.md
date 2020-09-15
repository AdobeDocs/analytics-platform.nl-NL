---
title: Opties voor gegevensinvoer voor Customer Journey Analytics
description: Begrijp de verschillende manieren u gegevens in Customer Journey Analytics kunt opnemen
translation-type: tm+mt
source-git-commit: 4ea06ca1f13255c570ccc9f69cb328d57bf975b2
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---


# Opties voor gegevensinvoer voor Customer Journey Analytics

U hebt een aantal opties voor het opnemen van gegevens in Customer Journey Analytics. Sommigen gaan ervan uit dat u de traditionele Adobe Analytics-gegevens wilt verplaatsen. Sommigen gaan ervan uit dat u gegevens rechtstreeks vanuit Adobe Experience Platform invoert. Deze naslaggids bevat stappen op hoog niveau die moeten worden gevolgd, met koppelingen naar meer gedetailleerde informatie.

## Gegevens uit traditionele Adobe Analytics verzamelen

Deze workflow maakt gebruik van de Adobe Analytics Data Connector en is afhankelijk van het feit of u DTM of Launch gebruikt als tagbeheer.

### Via dynamisch tagbeheer (DTM)

1. [Een gegevenslaag maken](https://docs.adobe.com/content/help/en/analytics/implementation/prepare/data-layer.html), als je dat nog niet hebt gedaan. Een gegevenslaag is een raamwerk van JavaScript-objecten op uw site dat alle variabelenwaarden bevat die in uw implementatie worden gebruikt. Hierdoor kunt u uw implementatie beter beheren en eenvoudiger onderhouden.
1. Gebruiken [DTM](https://docs.adobe.com/content/help/en/analytics/implementation/other/dtm/dtm-implementation-overview.html) om code op uw plaats voor gegevensinzameling uit te voeren, als u nog niet hebt. Het dynamische Beheer van de Markering verstrekt één enkele gegevenslaag die gegevens uit veelvoudige bronnen duwt.
1. Een [Adobe Analytics-bronaansluiting](https://docs.adobe.com/content/help/en/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) in Adobe Experience Platform. Deze bronschakelaar zal uw gegevens van Analytics in Experience Platform in een gestandaardiseerd kader opnemen genoemd [XDM-systeem (Experience Data Model)](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html).
1. Gebruiken [Customer Journey Analytics](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer verbindingen en gegevensweergaven te maken die uw rapportage via meerdere kanalen mogelijk maken.

### Via Launch

1. [Een gegevenslaag maken](https://docs.adobe.com/content/help/en/analytics/implementation/prepare/data-layer.html), als je dat nog niet hebt gedaan. Een gegevenslaag is een raamwerk van JavaScript-objecten op uw site dat alle variabelenwaarden bevat die in uw implementatie worden gebruikt. Hierdoor kunt u uw implementatie beter beheren en eenvoudiger onderhouden.
1. Gebruiken [Adobe Experience Platform Launch](https://docs.adobe.com/content/help/en/analytics/implementation/launch/overview.html) om code op uw plaats voor gegevensinzameling uit te voeren, als u nog niet hebt. Launch is een oplossing voor tagbeheer waarmee u naast andere vereisten voor codering ook analytische code kunt implementeren. De lancering biedt integratie met andere oplossingen en producten aan, en laat u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.
1. Een [Adobe Analytics-bronaansluiting](https://docs.adobe.com/content/help/en/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) in Adobe Experience Platform. Deze bronschakelaar zal uw gegevens van Analytics in Experience Platform in een gestandaardiseerd kader opnemen genoemd [XDM-systeem (Experience Data Model)](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html).
1. Gebruiken [Customer Journey Analytics](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-overview/cja-getting-started.html) om een of meer verbindingen en gegevensweergaven te maken die uw rapportage via meerdere kanalen mogelijk maken.
