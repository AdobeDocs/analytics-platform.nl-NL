---
title: Overzicht van Customer Journey Analytics
description: Leer hoe u met Customer Journey Analytics Analysis Workspace kunt gebruiken met gegevens van Experience Platform.
exl-id: f4f692c9-5951-4fa2-8e9f-5eeff0f79d10
solution: Customer Journey Analytics
feature: Basics
role: User, Admin
source-git-commit: 4bf8c616965718426efe880865acb0e5054b6a31
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 2%

---

# Overzicht van Customer Journey Analytics

Customer Journey Analytics is de volgende generatie Analytics-oplossing van de Adobe waarmee u de kracht van Analysis Workspace kunt gebruiken met gegevens uit Adobe Experience Platform. Het kan onderbreken, filtreren, vragen, en visualiseert jaren&#39; waarde van gegevens, en wordt gecombineerd met de capaciteit van het Platform om allerlei gegevensschema&#39;s en types te houden. Gebruikend het **Model van de Gegevens van de Ervaring (XDM)**, kunnen de gegevens uniform worden vertegenwoordigd en georganiseerd, klaar voor combinatie en exploratie. **de Dienst van de Vraag van Adobe Experience Platform** staat u toe om SQL-compatibele hulpmiddelen en kaders te gebruiken om al uw gegevens te vragen en te manipuleren.

De architectuur van de Customer Journey Analytics op hoog niveau wordt hier getoond:

![ Customer Journey Analytics architectuur die in deze sectie ](assets/cja-architecture.png) wordt verklaard


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Analyse van de Reis van de Klant: Analytics voor de Bedrijfs van de Ervaring ](https://video.tv.adobe.com/v/30090/?quality=12&learn=on){target="_blank"} voor een introductievideo aan Customer Journey Analytics.

>[!ENDSHADEBOX]


## Customer Journey Analytics vergelijken met Traditioneel Adobe Analytics

Customer Journey Analytics breidt het bereik van Adobe Analytics uit door eenvoudig kanaalmogelijkheden te gebruiken en beperkingen in eerdere versies van Adobe Analytics te verwijderen. Enkele opmerkelijke verbeteringen zijn:

* **Onbeperkte variabelen en gebeurtenissen**: De concepten eVars, steunen, en gebeurtenissen bestaan niet meer. De gegevens zijn vooral gericht op dimensies en metriek. Datasets kunnen een onbeperkt aantal unieke dimensies en metriek hebben.
* **Onbeperkte unieke waarden**: Adobe Experience Platform wordt niet beperkt tot enige unieke beperkingen.
* **Verandering historische gegevens**: Gebruikend Adobe Experience Platform, kunnen de gegevens worden verwijderd of worden verbeterd.
* **dwars-rapport-reeks gegevens**: De bestaande implementaties van veelvoudige datasets kunnen in Platform worden gecombineerd.

>[!TIP]
>
>Als u Adobe Analytics hebt gebruikt en uw gegevens van Adobe Analytics in Customer Journey Analytics wilt gebruiken, zie [ Samenvatten en gegevens van traditionele Adobe Analytics ](../data-ingestion/analytics.md) gebruiken snelle begingids als deel van de [ Ingestie van Gegevens ](../data-ingestion/data-ingestion.md) sectie.

De eerste release van Customer Journey Analytics bevat veel van de functies die in Adobe Analytics zijn opgenomen. Voor een volledige lijst, zie [ de eigenschapsteun van de Customer Journey Analytics ](/help/getting-started/aa-vs-cja/cja-aa.md).

## Hoofdgebruik

Met Customer Journey Analytics kunt u:

* **zie de klant in een reiscontext**: U kunt gegevens bekijken en opeenvolgend analyseren, die veelvoudige kanalen overspannen. De gegevens van uw vraagcentrum, POS systemen, en online eigenschappen kunnen in één enkele rapporteringsmening worden gecombineerd.
* **maak inzichten beschikbaar aan iedereen**: De gegevenstoegang van de democratisering en laat meer mensen bedrijfsbesluiten met gegeven-afgeleide inzichten maken. Iedereen in de organisatie met verantwoordelijkheid voor om het even welk aspect van de klantenervaring kan echte besluiten sneller maken, die op volledigere gegevens worden gebaseerd.
* **benut de macht van gegevenswetenschap voor uw analisten**: Customer Journey Analytics laat normale mensen gegevenswetenschap gebruiken om diepe inzichten en analyse te ontgrendelen.
* **visualiseren en met uw datasets in wisselwerking staan gebruikend op bestelling rapporterend**: Workspace kan om het even welke dataset van Adobe Experience Platform gebruiken die aan sommige basisregels voldoet.
* **niet-Webgegevens van de Mening**: Workspace is niet meer beperkt tot een stijve definitie van &quot;klap&quot;of &quot;gebeurtenis&quot;. De schema&#39;s van de douane staan volledige controle over gegevens en definities toe.
* **Uitvoer grotere controle over uw gegevensmanipulatie**: De gegevens van de verandering die u hebt geupload, leiden datasets, en voeren hen in Workspace in. Adobe Experience Platform verstrekt het vragen, het halen, het transformeren, en het laden hulpmiddelen door de Dienst van de Vraag van het Experience Platform.

## Vereisten

Voordat u kunt beginnen met het gebruik van Customer Journey Analytics, moet aan de volgende voorwaarden worden voldaan:

* Uw organisatie heeft een actief contract met Adobe Analytics for Select, Prime of Ultimate met de Customer Journey Analytics add-on. Als u niet zeker bent welk type van contract u hebt, of niet zeker bent als u de Customer Journey Analytics toe:voegen-op hebt, contacteer uw Team van de Rekening van de Adobe.
* Uw organisatie is ingericht voor Adobe Experience Platform.
* U kunt ook Customer Journey Analytics kopen als een zelfstandig product, zonder dat u Adobe Analytics nodig hebt.

## Toegangsbeheer

Zie [ Controle van de Toegang ](/help/technotes/access-control.md).

## Terminologie-updates

Verschillende functies in de Customer Journey Analytics hebben in vergelijking met de traditionele Adobe Analytics een andere naam gekregen om zich aan te passen aan de industrienormen. Enkele bijgewerkte terminologie:

* Segmenten worden nu &#39;filters&#39; genoemd.
* Virtuele rapportsuites worden nu &#39;gegevensweergaven&#39; genoemd.
* Classificaties worden nu &#39;Gegevensbestanden opzoeken&#39; genoemd.
* Klantkenmerken worden nu &#39;profielgegevenssets&#39; genoemd.
* De containers van de greep zijn nu genoemd geworden &quot;Event&quot;containers.
* Visitecontainers worden nu &#39;Sessie&#39;-containers genoemd.
* Bezoekerscontainers worden nu &#39;Person&#39;-containers genoemd.

## Andere mogelijkheden die op Adobe Experience Platform zijn gebaseerd

Customer Journey Analytics is één van de mogelijkheden van velen die op de Adobe Experience Platform vertrouwen. Met verschillende andere mogelijkheden, die ook op Experience Platform zijn gebaseerd, kunt u optimaal profiteren van uw gegevens.

Met Adobe Experience Platform kunt u klantgegevens en -inhoud van elk systeem centraliseren en standaardiseren en gegevens en computertraining toepassen om het ontwerp en de levering van persoonlijke ervaringen te verbeteren. De gegevens van de klant in het platform worden opgeslagen als datasets, die uit een schema en partijen gegevens bestaan. Voor meer detail op het platform, zie [ het Overzicht van de Architectuur van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/platform-learn/tutorials/intro-to-platform/basic-architecture.html).

Van de Ingestie van Gegevens aan directe SQL toegang, zijn verscheidene componenten van het Experience Platform centraal aan Customer Journey Analytics en vullen het aan:

* [ de Dienst van de Vraag van het Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl): Gebruik standaardSQL om gegevens van Adobe Experience Platform, zoals de gegevens van de oplossing van de Adobe, klant 1st-partijgegevens, of een andere gegevens van het Platform terug te winnen. Het is een serverloos hulpmiddel dat u toestaat om zich bij om het even welke datasets aan te sluiten en de vraagresultaten als nieuwe dataset voor gebruik in het melden van of voor opname in de Dienst van het Profiel te vangen. U kunt de Dienst van de Vraag van het Experience Platform gebruiken om gegevensanalysecosystemen te bouwen, die tot een beeld van consumenten over hun diverse interactiekanalen leiden. Deze kanalen zouden de systemen van het Punt-van-Verkoop, Web, Mobiel, systemen van CRM, etc. kunnen omvatten.
* [ Real-time Profiel van de Klant ](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl):
* [ Dienst van de Identiteit ](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=nl)

## Video&#39;s


>[!BEGINSHADEBOX]

Zie ](/help/assets/icons/VideoCheckedOut.svg) [ Werk 0} VideoCheckedOut met gegevens in Customer Journey Analytics ](https://video.tv.adobe.com/v/32112/?quality=12&learn=on){target="_blank"} voor een inleidende video hoe te met gegevens in Customer Journey Analytics werken.![

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Architectuur en integratie ](https://video.tv.adobe.com/v/32483/?quality=12&learn=on){target="_blank"} voor een inleidende video op de architectuur en de integratie van Customer Journey Analytics.

>[!ENDSHADEBOX]


