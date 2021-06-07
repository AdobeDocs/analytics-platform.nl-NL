---
description: Gebruik voorbeelden van hoofdletters en kleine letters voor cohortanalyse.
keywords: Analysis Workspace
title: Gebruiksgevallen van cohortanalyse
feature: Grondbeginselen van rapporten en analyses
uuid: 5ec46f84-5702-4bc1-a796-874a3abe87c9
exl-id: f559d4b4-b682-4306-b111-22acb26fe0a0
source-git-commit: f74b5e79b6713050869301adb95e2a73705330da
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 0%

---

# [!UICONTROL Cohort Analysis] use cases

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van [Analysis Workspace in traditionele Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Gebruik voorbeelden van hoofdletters en kleine letters voor [!UICONTROL Cohort Analysis].

## Gebruiksscenario voor betrokkenheid van apps

Stel dat u wilt analyseren hoe gebruikers die uw app installeren er na verloop van tijd mee werken. Installeren ze het en gebruiken ze het nooit? Hebben ze het een tijdje gebruikt en vallen ze dan weg? Of blijven ze in de loop der tijd betrokken?

U kunt een [!UICONTROL Cohort Analysis] van zes maanden tot stand brengen:

**Korreligheid**: Maandelijks, van januari 2015 tot en met juni 2015.

**Inclusiemetrisch**: App-installaties.

**Metrisch** retourneren: Sessies of Launches

Bezoekers tellen de volgende maanden niet als *`engaged`* mee, tenzij ze een sessie hebben of de app ten minste starten. [!UICONTROL Cohort Analysis] toont u dan patronen in gebruik waar  *`App Install`* altijd voorkomt op Maand 0. Mogelijk ziet u dat het gebruik in maand 2 wordt onderbroken, ongeacht wanneer gebruikers de app hebben geïnstalleerd. (Voor degenen die de app in januari 2015 hebben geïnstalleerd, is maand 2 maart 2015. Voor degenen die de app in februari 2015 hebben geïnstalleerd, is maand 2 april 2015, enzovoort.) Met deze analyse kunt u een e-mail- of pushbericht naar alle gebruikers sturen tijdens de tweede maand na de installatie van de app om hen eraan te herinneren de app te gebruiken.

## Gebruiksscenario voor abonnement

U werkt op Adobe.com en biedt een gratis Creative Cloud-abonnement aan. Het is de bedoeling dat gebruikers een upgrade uitvoeren van de gratis versie naar de proefversie van 30 dagen of uiteindelijk naar de betaalde versie.

**Korreligheid**: Maandelijks

**Inclusiemetrisch**: Koppeling downloaden

**Metrisch** retourneren: Betaalde Creative Cloud aanschaffen

Met behulp van [!UICONTROL Cohort Analysis] kunt u bijvoorbeeld zien dat tussen 8% en 10% van de gratis Creative Cloud-gebruikers in de eerste maand na de installatie een upgrade uitvoeren, ongeacht wanneer ze zijn geïnstalleerd. 12-15% verbetering in de tweede maand van gebruik. Hierna wordt de upgrade aanzienlijk minder: 4-5% in maand drie, 3-4% in maand vier, en 1-2% in maand vijf.

Erkennend dat u potentiële klanten in maand drie niet moet verliezen, stelde u een e-mailcampagne op die wordt ontworpen om in het midden van maand drie aan een steekproef van gebruikers uit te gaan, die een coupon van $50 aan gebruikers aanbieden die nog niet hebben bevorderd.

Neem een paar maanden later contact op met uw rapport over cohortanalyse. Voor cohorten die na de start van de campagne zijn gevormd, is de conversie naar betaalabonnementen voor Creative Cloud in maand drie gestegen van 4-5% naar 13-14%, wat heeft geresulteerd in honderdduizenden dollars per cohort, voor elke maandelijkse cohort die maand drie van dat punt vooruit raakt.

## Complexe cohortfilters gebruiken hoofdletters

Een belangrijke hotelketen richt veelvoudige klantengroepen voor bevorderingen en sporen tegen prestaties. Om de beste groepen van gebruikerscohorten te identificeren om te richten, willen zij zeer specifieke cohortgroepen tot stand brengen. Met behulp van de gewijzigde [!UICONTROL Inclusion]- en [!UICONTROL Return]-criteria in [!UICONTROL Cohort]-tabellen kunnen ze alleen de juiste cohortgroepen definiëren met meerdere maatstaven en filters om ondermaatse klantengroepen te identificeren, zodat ze zich kunnen richten op promoties en deals om boekingen te verhogen.

## Toepassingsversie adoptie-case

Een groot verzekeringsbedrijf drijft veel klantenbetrokkenheid door het gebruik van zijn mobiele app. Als er echter nieuwe functies aan hun app worden toegevoegd, is het van essentieel belang dat hun klanten een upgrade uitvoeren naar de nieuwste app-versie. Ze kunnen al hun app-versies naast elkaar analyseren en vergelijken met behulp van [!UICONTROL Custom Dimension] Cohort om te zien welke klanten de app-versie als doel hebben. Bovendien kunnen ze zowel de retentie als het churn bijhouden om te zien of bepaalde app-versies klanten in de loop der tijd van het gebruik van de app afhouden. Via mobiele communicatie kunnen ze opnieuw contact opnemen met deze gebruikers om ze te laten upgraden naar de nieuwste versie om te profiteren van hun nieuwste functies.

## Campagne Gebruiksscenario

Een multinational in de media gebruikt gerichte campagnes om gebruikers naar hun verschillende platforms te drijven om betrokkenheid te drijven. Advertentie-uitgaven per platform zijn gebaseerd op betrokkenheid en retentie van klanten. succesvolle campagnes zijn dan ook van cruciaal belang voor het succes van hun bedrijf . Ze gebruiken onze nieuwe [!UICONTROL Custom Dimension] codehortfunctie in Tabellen [!UICONTROL Cohort] om verschillende campagnes naast elkaar te vergelijken om te bepalen welke campagnes het meest effectief zijn in het aanschaffen en behouden van gebruikers om de betrokkenheid te vergroten. Vervolgens kunnen zij vaststellen welke aspecten een campagne succesvol maken en deze toepassen op andere campagnes om de betrokkenheid op hun verschillende platform te vergroten.

## Gebruiksscenario bij starten van product

Een grote apparel detailhandelaar heeft vele specifieke klantenfilters die grote delen van opbrengst voor hun zaken drijven. Elk filter heeft specifieke producten die met het filter in mening worden ontworpen en worden gecreeerd. Bij elke productintroductie willen ze weten hoe het nieuwe product de verkoop aan verschillende cohorten in de loop der tijd heeft gestimuleerd. Met de nieuwe [!UICONTROL Latency Table]-instelling in [!UICONTROL Cohort Analysis] kunnen ze het gedrag en de inkomsten van een bepaald klantfilter voor en na de introductie analyseren. Op basis van deze informatie kunnen zij vaststellen welke producten nieuwe inkomsten genereren en die geen tractie krijgen met klanten.

## Individuele filiaalheid - De meest geliefde gebruikers gebruiken hoofdletters/kleine letters

Een grote luchtvaartmaatschappij haalt het grootste deel van haar succes en inkomsten uit herhaalde en loyale klanten. In veel gevallen zijn hun loyale reizigers het grootste deel van hun inkomsten en het behoud van die klanten van cruciaal belang voor hun succes op lange termijn. Het identificeren van hun meest loyale en verenigbare klanten kan vaak moeilijk zijn. Met de nieuwe [!UICONTROL Rolling Calculation]-instelling in [!UICONTROL Cohort Analysis] konden ze echter loyale klantfilters analyseren en erachter komen welke reizigers maand-op-maand herhaalde kopers waren. Vervolgens konden zij deze reizigers met beloningen en perken voor hun loyaliteit aanspreken. Bovendien, door het type van Cohort van behoud aan churn over te schakelen, konden zij ook identificeren welke klanten niet de maand-over-maand kopers herhaalden en die filters richten met bevorderingen om met hen opnieuw in dienst te nemen en ervoor te zorgen dat zij in de toekomst loyale klanten blijven.
