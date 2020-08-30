---
description: Gebruik voorbeelden voor cohortanalyse.
keywords: Analysis Workspace
title: Gebruiksgevallen van cohortanalyse
topic: Reports and analytics
uuid: 5ec46f84-5702-4bc1-a796-874a3abe87c9
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 0%

---


# [!UICONTROL Cohort Analysis] gebruiksgevallen

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Gebruik voorbeelden voor voorbeelden voor [!UICONTROL Cohort Analysis].

## Gebruiksscenario voor service met app

Veronderstel dat u wilt analyseren hoe de gebruikers die uw app installeren met het in tijd in dienst nemen. Installeer het en gebruik het nooit? Gebruiken ze het een tijdje en vallen ze dan weg? Of blijven ze in de loop der tijd betrokken?

U kunt een [!UICONTROL Cohort Analysis]:

**Granulariteit**: Maandelijks, van januari 2015 tot en met juni 2015.

**Inclusiemetrisch**: App Installs.

**Metrisch rendement**: Sessies of lanceringen

Bezoekers tellen niet mee *`engaged`* in de daaropvolgende maanden, tenzij zij een sessie hebben of ten minste de app starten. [!UICONTROL Cohort Analysis] dan zou u patronen in gebruik tonen waar *`App Install`* komt altijd voor op Maand 0. U zou kunnen opmerken dat de gebruiksonderbreking in Maand 2, ongeacht wanneer de gebruikers app installeerden. (Voor degenen die de app in januari 2015 hebben geïnstalleerd, is maand 2 maart 2015. Voor degenen die de app in februari 2015 hebben geïnstalleerd, is maand 2 april 2015, etc.) Met deze analyse kunt u een e-mail of een push-bericht naar alle gebruikers sturen in de tweede maand nadat ze de app hebben geïnstalleerd, zodat ze eraan kunnen herinneren dat ze de app moeten gebruiken.

## Gebruiksscenario voor abonnement

U werkt op Adobe.com en biedt een gratis Creative Cloud-abonnement aan. Het doel is voor gebruikers om van de vrije versie aan de 30 dagproefversie of, uiteindelijk, de betaalde versie te bevorderen.

**Granulariteit**: Maandelijks

**Inclusiemetrisch**: Link downloaden

**Metrisch rendement**: Betaalde creatieve cloud kopen

Dit gebruiken [!UICONTROL Cohort Analysis], kon u bijvoorbeeld zien dat tussen 8% en 10% van de gratis Creative Cloud-gebruikers in de eerste maand na de installatie upgraden, ongeacht wanneer ze zijn geïnstalleerd. 12-15% upgrade in de tweede maand van gebruik. Daarna daalt de verbetering beduidend weg: 4-5% in maand drie, 3-4% in maand vier, en 1-2% in maand vijf.

Erkennend dat u potentiële klanten in maand drie niet moet verliezen, vestigt u opstelling een e-mailcampagne die wordt ontworpen om in het midden van maand drie aan een steekproef van gebruikers uit te gaan, die een coupon $50 aan gebruikers aanbieden die nog niet hebben bevorderd.

Bekijk uw rapport van de cohortanalyse een paar maanden later. Voor cohorten die na de lancering van de campagne zijn gevormd, is de omzetting in betaalde Creative Cloud abonnementen in maand drie gestegen van 4-5% tot 13-14%, resulterend in honderdduizenden dollars per cohort, voor elke maandelijkse cohort die maand drie vanaf dat punt vooruit raakt.

## Complexe Cohort Segmenten gebruiken case

Een belangrijke hotelketen richt veelvoudige klantengroepen voor bevorderingen en sporen tegen prestaties. Om de beste groepen gebruikerscohorten te identificeren die u wilt richten, willen ze zeer specifieke cohortgroepen maken. Het augmented gebruiken [!UICONTROL Inclusion] en [!UICONTROL Return] Criteria binnen [!UICONTROL Cohort] De lijsten, kunnen zij enkel de juiste cohortgroeperingen met veelvoudige metriek en segmenten bepalen om ondermaatse klantengroepen te identificeren om hen met bevorderingen en overeenkomsten te richten om het boeken te verhogen.

## App Version Adoption-gebruiksscenario

Een groot verzekeringsbedrijf drijft een hoop klantenbetrokkenheid door het gebruik van zijn mobiele app. Nochtans, aangezien de nieuwe eigenschappen aan hun app worden toegevoegd, is het kritiek dat hun klanten aan de recentste app versie bevorderen. Zij kunnen elk van hun app versies naast elkaar analyseren en vergelijken gebruikend [!UICONTROL Custom Dimension] Cohort om te zien welke klanten op welke app versie aan doel zijn. Bovendien, kunnen zij zowel behoud als kurn volgen om te zien of drijven de specifieke app versies klanten weg van het gebruiken van app in tijd. Door mobiele overseineninspanningen, kunnen zij met deze gebruikers opnieuw in dienst nemen om hen aan de recentste versie te krijgen om uit hun recentste eigenschappen voordeel te halen.

## Campagne Stickiness Use case

Een multinationaal mediabedrijf maakt gebruik van gerichte campagnes om gebruikers naar hun verschillende platforms te sturen om de betrokkenheid te stimuleren. Advertentie-uitgaven per platform zijn gebaseerd op klantenservice en behoud; succesvolle campagnes zijn dan ook van cruciaal belang voor het succes van hun bedrijf . Ze gebruiken onze nieuwe [!UICONTROL Custom Dimension] Cohortfunctie in [!UICONTROL Cohort] Tabellen om verschillende campagnes naast elkaar te vergelijken om te bepalen welke campagnes het meest effectief zijn bij het aanschaffen en behouden van gebruikers om de betrokkenheid te vergroten. Zij kunnen dan identificeren welke aspecten een campagne succesvol maken en het toepassen op andere campagnes om betrokkenheid over hun diverse platform te verhogen.

## Product Gebruiksscenario starten

Een grote kledingdetailhandelaar heeft vele specifieke klantensegmenten die grote delen van opbrengst voor hun zaken drijven. Elk segment heeft specifieke producten die met het segment in mening worden ontworpen en worden gecreeerd. Met elke productlancering, willen zij weten hoe het nieuwe product verkoop aan diverse cohorten in tijd heeft bevorderd. Het nieuwe gebruiken [!UICONTROL Latency Table] instelling in [!UICONTROL Cohort Analysis], kunnen zij het gedrag en de inkomsten van een bepaald klantensegment vóór en na de introductie analyseren. Gebruikend deze informatie, kunnen zij identificeren welke producten nieuwe opbrengst drijven en die geen tractie met klanten krijgen.

## Individuele Stickiness - De meeste Gelofelijke Gebruikers gebruiken case

Een grote luchtvaartmaatschappij haalt het grootste deel van haar succes en inkomsten uit herhaalde en loyale klanten. In veel gevallen vormen hun loyale reizigers de meerderheid van hun inkomsten en is het behouden van die klanten van cruciaal belang voor hun succes op de lange termijn. Het identificeren van hun meest loyale en verenigbare klanten kan vaak moeilijk zijn. Het gebruik van de nieuwe [!UICONTROL Rolling Calculation] instelling in [!UICONTROL Cohort Analysis], konden zij loyale klantensegmenten analyseren en te weten komen welke reizigers maand-over-maand herhaalde kopers waren. Zij konden deze reizigers dan met beloningen en perken voor hun loyaliteit toespreken. Bovendien, door het type van Cohort van behoud aan kurn te schakelen, konden zij ook identificeren welke klanten niet maand-over-maand herhaalde kopers waren en die segmenten met bevorderingen richten om met hen opnieuw in dienst te nemen en te verzekeren zij loyale klanten in de toekomst blijven.
