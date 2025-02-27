---
title: Customer Journey Analytics-overzicht
description: Leer hoe u met Customer Journey Analytics Analysis Workspace kunt gebruiken met gegevens van Experience Platform.
exl-id: f4f692c9-5951-4fa2-8e9f-5eeff0f79d10
solution: Customer Journey Analytics
feature: Basics
role: User, Admin
source-git-commit: 51a6341734163fdd6b994ae9cec53ef034959896
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 2%

---

# Customer Journey Analytics-overzicht

Customer Journey Analytics is Adobe-oplossing voor de volgende generatie Analytics waarmee u de kracht van Analysis Workspace kunt gebruiken met gegevens uit Adobe Experience Platform. Het kan onderbreken, filtreren, vragen, en visualiseert jaren&#39; waarde van gegevens, en wordt gecombineerd met de capaciteit van het Platform om allerlei gegevensschema&#39;s en types te houden. Gebruikend het **Model van de Gegevens van de Ervaring (XDM)**, kunnen de gegevens uniform worden vertegenwoordigd en georganiseerd, klaar voor combinatie en exploratie. **de Dienst van de Vraag van Adobe Experience Platform** staat u toe om SQL-compatibele hulpmiddelen en kaders te gebruiken om al uw gegevens te vragen en te manipuleren.

De Customer Journey Analytics-architectuur op hoog niveau wordt hier getoond:

![ architectuur van Customer Journey Analytics die in deze sectie ](assets/cja-architecture.png) wordt verklaard


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Analyse van de Reis van de Klant: Analytics voor de Bedrijfs van de Ervaring ](https://video.tv.adobe.com/v/30090/?quality=12&learn=on){target="_blank"} voor een introductievideo aan Customer Journey Analytics.

>[!ENDSHADEBOX]


## Customer Journey Analytics vergelijken met Traditioneel Adobe Analytics

Customer Journey Analytics breidt het bereik van Adobe Analytics uit door eenvoudig kanaaloverschrijdende mogelijkheden te gebruiken en beperkingen in eerdere versies van Adobe Analytics te verwijderen. Enkele opmerkelijke verbeteringen zijn:

* **Onbeperkte variabelen en gebeurtenissen**: De concepten eVars, steunen, en gebeurtenissen bestaan niet meer. De gegevens zijn vooral gericht op dimensies en metriek. Datasets kunnen een onbeperkt aantal unieke dimensies en metriek hebben.
* **Onbeperkte unieke waarden**: Adobe Experience Platform wordt niet beperkt tot enige unieke beperkingen.
* **Verandering historische gegevens**: Gebruikend Adobe Experience Platform, kunnen de gegevens worden verwijderd of worden verbeterd.
* **dwars-rapport-reeks gegevens**: De bestaande implementaties van veelvoudige datasets kunnen in Platform worden gecombineerd.

>[!TIP]
>
>Als u Adobe Analytics hebt gebruikt en uw gegevens van Adobe Analytics in Customer Journey Analytics wilt gebruiken, zie [ Samenvatting en gebruiksgegevens van traditionele Adobe Analytics ](../data-ingestion/analytics.md) snelle begingids als deel van de [ Ingestie van Gegevens ](../data-ingestion/data-ingestion.md) sectie.

De eerste release van Customer Journey Analytics bevat veel van de functies die in Adobe Analytics zijn opgenomen. Voor een volledige lijst, zie [ de eigenschapsteun van Customer Journey Analytics ](/help/getting-started/aa-vs-cja/cja-aa.md).

## Hoofdgebruik

Met Customer Journey Analytics kunt u:

* **zie de klant in een reiscontext**: U kunt gegevens bekijken en opeenvolgend analyseren, die veelvoudige kanalen overspannen. De gegevens van uw vraagcentrum, POS systemen, en online eigenschappen kunnen in één enkele rapporteringsmening worden gecombineerd.
* **maak inzichten beschikbaar aan iedereen**: De gegevenstoegang van de democratisering en laat meer mensen bedrijfsbesluiten met gegeven-afgeleide inzichten maken. Iedereen in de organisatie met verantwoordelijkheid voor om het even welk aspect van de klantenervaring kan echte besluiten sneller maken, die op volledigere gegevens worden gebaseerd.
* **benut de macht van gegevenswetenschap voor uw analisten**: Customer Journey Analytics laat normale mensen gegevenswetenschap gebruiken om diepe inzichten en analyse te ontgrendelen.
* **visualiseren en met uw datasets in wisselwerking staan gebruikend op bestelling rapporterend**: Workspace kan om het even welke dataset van Adobe Experience Platform gebruiken die aan sommige basisregels voldoet.
* **niet-Webgegevens van de Mening**: Workspace is niet meer beperkt tot een stijve definitie van &quot;klap&quot;of &quot;gebeurtenis&quot;. De schema&#39;s van de douane staan volledige controle over gegevens en definities toe.
* **Uitvoer grotere controle over uw gegevensmanipulatie**: De gegevens van de verandering die u hebt geupload, leiden datasets, en voeren hen in Workspace in. Adobe Experience Platform biedt hulpprogramma&#39;s voor het opvragen, uitpakken, transformeren en laden via de Experience Platform Query Service.

## Vereisten

Voordat u Customer Journey Analytics kunt gaan gebruiken, moet aan de volgende voorwaarden zijn voldaan:

* Uw organisatie heeft een actief contract met Adobe Analytics for Select, Prime of Ultimate met de invoegtoepassing Customer Journey Analytics. Als u niet zeker weet welk type contract u hebt of als u niet zeker weet of u de invoegtoepassing Customer Journey Analytics hebt, neemt u contact op met uw Adobe-accountteam.
* Uw organisatie is ingericht voor Adobe Experience Platform.
* U kunt Customer Journey Analytics ook kopen als een zelfstandig product, zonder dat u Adobe Analytics nodig hebt.

## Toegangsbeheer

Zie [ Controle van de Toegang ](/help/technotes/access-control.md).

## Terminologie-updates

Verschillende functies in Customer Journey Analytics hebben in vergelijking met traditionele Adobe Analytics een andere naam gekregen om zich aan te passen aan de industrienormen. Enkele bijgewerkte terminologie:

* Segmenten worden nu &#39;filters&#39; genoemd.
* Virtuele rapportsuites worden nu &#39;gegevensweergaven&#39; genoemd.
* Classificaties worden nu &#39;Gegevensbestanden opzoeken&#39; genoemd.
* Klantkenmerken worden nu &#39;profielgegevenssets&#39; genoemd.
* De containers van de greep zijn nu genoemd geworden &quot;Event&quot;containers.
* Visitecontainers worden nu &#39;Sessie&#39;-containers genoemd.
* Bezoekerscontainers worden nu &#39;Person&#39;-containers genoemd.

## Andere mogelijkheden die op Adobe Experience Platform zijn gebaseerd

Customer Journey Analytics is één van de vele mogelijkheden die op de Adobe Experience Platform vertrouwen. Met verschillende andere mogelijkheden, die ook op Experience Platform zijn gebaseerd, kunt u optimaal profiteren van uw gegevens.

Met Adobe Experience Platform kunt u klantgegevens en -inhoud van elk systeem centraliseren en standaardiseren en gegevens en computertraining toepassen om het ontwerp en de levering van persoonlijke ervaringen te verbeteren. De gegevens van de klant in het platform worden opgeslagen als datasets, die uit een schema en partijen gegevens bestaan. Voor meer detail op het platform, zie [ het Overzicht van de Architectuur van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/platform-learn/tutorials/intro-to-platform/basic-architecture.html).

Van gegevensverwerking tot directe SQL-toegang, meerdere componenten van de Experience Platform zijn van centraal belang voor Customer Journey Analytics en vullen deze aan:

* [ de Dienst van de Vraag van Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl): Gebruik standaardSQL om gegevens van Adobe Experience Platform, zoals de oplossingsgegevens van Adobe, klant 1st-partijgegevens, of een andere gegevens van het Platform terug te winnen. Het is een serverloos hulpmiddel dat u toestaat om zich bij om het even welke datasets aan te sluiten en de vraagresultaten als nieuwe dataset voor gebruik in het melden van of voor opname in de Dienst van het Profiel te vangen. Met Experience Platform Query Service kunt u gegevensanalysecosystemen maken en zo een beeld van de consument op de verschillende communicatiekanalen creëren. Deze kanalen zouden de systemen van het Punt-van-Verkoop, Web, Mobiel, systemen van CRM, etc. kunnen omvatten.
* [ Real-time Profiel van de Klant ](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl):
* [ Dienst van de Identiteit ](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=nl)

## Video&#39;s

>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Werk met gegevens in Customer Journey Analytics ](https://video.tv.adobe.com/v/32112/?quality=12&learn=on){target="_blank"} voor een inleidende video om met gegevens in Customer Journey Analytics te werken.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Architectuur en integratie ](https://video.tv.adobe.com/v/32483/?quality=12&learn=on){target="_blank"} voor een inleidende video op de architectuur en de integratie van Customer Journey Analytics.

>[!ENDSHADEBOX]

* [ Adobe Customer Journey Analytics Crash Cursus voor Analysts ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/adobe-customer-journey-analytics-crash-course-for-analysts/ba-p/719261)

* [ Optimizing Your Mindset and Adobe Customer Journey Analytics Workflow: De Modellen van het team voor Organisaties van Alle Grootte ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/optimizing-your-mindset-and-adobe-customer-journey-analytics/ba-p/721456)

* [ de Organisatorische Gereedheid van de Bouw: Een Mensen-Eerste Gids aan het Schalen van Adobe Customer Journey Analytics ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/building-organizational-readiness-a-people-first-guide-to/ba-p/723273)