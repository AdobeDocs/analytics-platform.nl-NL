---
title: Overzicht van Customer Journey Analytics
description: Leer hoe u met Customer Journey Analytics Analysis Workspace kunt gebruiken met gegevens van Experience Platform.
exl-id: f4f692c9-5951-4fa2-8e9f-5eeff0f79d10
solution: Customer Journey Analytics
feature: Basics
source-git-commit: 63bfed665e8f60c28442015367083e1529e5a2ea
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 4%

---

# Overzicht van Customer Journey Analytics

Customer Journey Analytics is de volgende generatie Analytics-oplossing van de Adobe waarmee u de kracht van Analysis Workspace kunt gebruiken met gegevens uit Adobe Experience Platform. Het kan onderbreken, filtreren, vragen, en visualiseert jaren&#39; waarde van gegevens, en wordt gecombineerd met de capaciteit van het Platform om allerlei gegevensschema&#39;s en types te houden. Met de **Experience Data Model (XDM)** Gegevens kunnen op uniforme wijze worden weergegeven en geordend, klaar voor combinatie en onderzoek. **Adobe Experience Platform Query Services** staat u toe om SQL-compatibele hulpmiddelen en kaders te gebruiken om al uw gegevens te vragen en te manipuleren.

De architectuur van de Customer Journey Analytics op hoog niveau wordt hier getoond:

![architectuur](assets/cja-architecture.png)

Hier volgt een video-overzicht van de Customer Journey Analytics:

>[!VIDEO](https://video.tv.adobe.com/v/30090/?quality=12)

## Customer Journey Analytics vergelijken met Traditioneel Adobe Analytics

Customer Journey Analytics breidt het bereik van Adobe Analytics uit door eenvoudig kanaalmogelijkheden te gebruiken en beperkingen in eerdere versies van Adobe Analytics te verwijderen. Enkele opmerkelijke verbeteringen zijn:

* **Onbeperkte variabelen en gebeurtenissen**: De concepten eVars, props en gebeurtenissen bestaan niet meer. De gegevens zijn vooral gericht op dimensies en metriek. Datasets kunnen een onbeperkt aantal unieke dimensies en metriek hebben.
* **Onbeperkte unieke waarden**: Adobe Experience Platform is niet beperkt tot enige unieke beperking.
* **Historische gegevens wijzigen**: Met Adobe Experience Platform kunnen gegevens worden verwijderd of gecorrigeerd.
* **Gegevens uit meerdere rapporten**: Bestaande implementaties van meerdere datasets kunnen worden gecombineerd in Platform.

>[!TIP]
>
>Als u Adobe Analytics hebt gebruikt en uw Adobe Analytics-gegevens in de Customer Journey Analytics wilt gebruiken, raadpleegt u [Gegevens van traditionele Adobe Analytics verzamelen en gebruiken](../data-ingestion/analytics.md) snelstartgids als onderdeel van de [Gegevensinname](../data-ingestion/data-ingestion.md) sectie.

De eerste release van Customer Journey Analytics bevat veel van de functies die in Adobe Analytics zijn opgenomen. Zie voor een volledige lijst [Ondersteuning van Customer Journey Analytics-functies](/help/getting-started/aa-vs-cja/cja-aa.md).

## Hoofdgebruik

Met Customer Journey Analytics kunt u:

* **Bekijk de klant in een reiscontext**: U kunt gegevens opeenvolgend bekijken en analyseren, die veelvoudige kanalen overspannen. De gegevens van uw vraagcentrum, POS systemen, en online eigenschappen kunnen in één enkele rapporteringsmening worden gecombineerd.
* **Inzichten voor iedereen beschikbaar maken**: Toegang tot gegevens democratiseren en meer mensen toestaan zakelijke beslissingen te nemen met inzichten op basis van gegevens. Iedereen in de organisatie met verantwoordelijkheid voor om het even welk aspect van de klantenervaring kan echte besluiten sneller maken, die op volledigere gegevens worden gebaseerd.
* **Maak gebruik van de kracht van gegevenswetenschap voor uw analisten**: Customer Journey Analytics laat normale mensen gegevenswetenschap gebruiken om diepgaande inzichten en analyse te ontsluiten.
* **Visualiseren en met uw datasets in wisselwerking staan die op bestelling rapportering gebruiken**: De werkruimte kan om het even welke dataset van Adobe Experience Platform gebruiken die aan sommige basisregels voldoet.
* **Niet-webgegevens weergeven**: De werkruimte is niet langer beperkt tot een starre definitie van een &#39;hit&#39; of &#39;event&#39;. De schema&#39;s van de douane staan volledige controle over gegevens en definities toe.
* **Meer controle over het manipuleren van gegevens**: Wijzig de gegevens die u hebt geüpload, maak gegevenssets en importeer deze naar Workspace. Adobe Experience Platform verstrekt het vragen, het halen, het transformeren, en het laden hulpmiddelen door de Dienst van de Vraag van het Experience Platform.

## Vereisten

Voordat u kunt beginnen met het gebruik van Customer Journey Analytics, moet aan de volgende voorwaarden worden voldaan:

* Uw organisatie heeft een actief contract met Adobe Analytics voor Select, Prime of Ultimate met de Customer Journey Analytics add-on. Als u niet zeker bent welk type van contract u hebt, of niet zeker bent als u de Customer Journey Analytics toe:voegen-op hebt, contacteer uw Team van de Rekening van de Adobe.
* Uw organisatie is ingericht voor Adobe Experience Platform.
* U kunt ook Customer Journey Analytics kopen als een zelfstandig product, zonder dat u Adobe Analytics nodig hebt.

## Toegangsbeheer

Zie de [Toegangsbeheer](/help/admin/cja-access-control.md) onderwerp.

## Terminologie-updates

Verschillende functies in de Customer Journey Analytics hebben in vergelijking met de traditionele Adobe Analytics een andere naam gekregen om zich aan te passen aan de industrienormen. Enkele bijgewerkte terminologie:

* Segmenten worden nu &#39;filters&#39; genoemd.
* Virtuele rapportsets worden nu &#39;gegevensweergaven&#39; genoemd.
* Classificaties worden nu &#39;Gegevensbestanden opzoeken&#39; genoemd.
* Klantkenmerken worden nu &#39;profielgegevenssets&#39; genoemd.
* De containers van de greep zijn nu genoemd geworden &quot;Event&quot;containers.
* Visitecontainers worden nu &#39;Sessie&#39;-containers genoemd.
* Bezoekerscontainers worden nu &#39;Person&#39;-containers genoemd.

## Andere mogelijkheden die op Adobe Experience Platform zijn gebaseerd

Customer Journey Analytics is één van de mogelijkheden van velen die op de Adobe Experience Platform vertrouwen. Met verschillende andere mogelijkheden, die ook op Experience Platform zijn gebaseerd, kunt u optimaal profiteren van uw gegevens.

Met Adobe Experience Platform kunt u klantgegevens en -inhoud van elk systeem centraliseren en standaardiseren en gegevens en computertraining toepassen om het ontwerp en de levering van persoonlijke ervaringen te verbeteren. De gegevens van de klant in het platform worden opgeslagen als datasets, die uit een schema en partijen gegevens bestaan. Zie voor meer informatie over het platform [Overzicht van Adobe Experience Platform-architectuur](https://experienceleague.adobe.com/docs/platform-learn/tutorials/intro-to-platform/basic-architecture.html).

Van de Ingestie van Gegevens aan directe SQL toegang, zijn verscheidene componenten van het Experience Platform centraal aan Customer Journey Analytics en vullen het aan:

* [Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl): Gebruik standaard SQL om gegevens van Adobe Experience Platform op te halen, zoals de gegevens van de oplossing van de Adobe, klant 1st-party gegevens, of een andere gegevens van het Platform. Het is een server-zonder hulpmiddel dat u toestaat om zich bij om het even welke datasets aan te sluiten en de vraagresultaten als nieuwe dataset voor gebruik in rapportering, de Werkruimte van de Wetenschap van Gegevens, of voor opname in de Dienst van het Profiel te vangen. U kunt de Dienst van de Vraag van het Experience Platform gebruiken om gegevensanalysecosystemen te bouwen, die tot een beeld van consumenten over hun diverse interactiekanalen leiden. Deze kanalen zouden de systemen van het Punt-van-Verkoop, Web, Mobiel, systemen van CRM, etc. kunnen omvatten.
* [Klantprofiel in real time](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl):
* [Identiteitsservice](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=nl):
* [Werkruimte voor gegevenswetenschap](https://experienceleague.adobe.com/docs/experience-platform/data-science-workspace/home.html) in &quot;developer&quot; (optie voor ontwikkelaars): u kunt in Adobe Experience Platform gebruik maken van vooraf gebouwde artificiële intelligentie (AI) en computerleermodellen om verschillende punten van de reis van de klant te beïnvloeden. Door verborgen inzichten te negeren, kunt u betere voorspellingen over de klantenreis maken, geadviseerde beste volgende stappen voorstellen, of lastige processen automatiseren.

## Video&#39;s

* Werken met gegevens in Customer Journey Analytics:

  >[!VIDEO](https://video.tv.adobe.com/v/32112/?quality=12)

* Architectuur en integratie van Customer Journey Analytics:

  >[!VIDEO](https://video.tv.adobe.com/v/32483/?quality=12)

