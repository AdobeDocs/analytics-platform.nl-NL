---
description: Verklaart de ononderbroken strategie van de eigenschapversie voor Customer Journey Analytics
title: Customer Journey Analytics-functiereleases
exl-id: aebe709a-4cc7-4197-86e9-b26ab2874375
source-git-commit: 44a140fdd5069cbe806f694377802215bcf50b31
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 1%

---

# Customer Journey Analytics-functiereleases

De versies van Customer Journey Analytics werken op een ononderbroken leveringsmodel dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat.

## Releasestrategie

[!UICONTROL Analysis Workspace] maakt gebruik van functiemarkeringen (ook wel &#39;&#39;schakelingen&#39;&#39; genoemd) om de zichtbaarheid van nieuwe functies te bepalen, zodat tests op gecontroleerde schaal vóór volledige release mogelijk zijn. Deze releasestrategie omvat de volgende fasen:

* **Begin van rollout**: De introductie van een gefaseerde release begint met beperkte tests door interne Adobe-gebruikers. De release wordt vervolgens in de loop van een paar maanden geschaald van 0% naar 100% beschikbaarheid voor klanten. De gefaseerde uitrol gebeurt op het niveau van de Organisatie van de Experience Cloud, zodat ontvangen alle gemachtigde gebruikers in een organisatie de zelfde ervaring.

* **Algemene beschikbaarheid (GA)**: De functie is beschikbaar voor 100% van de organisaties met bevoegdheid voor Experience Cloud en de release met functies is voltooid.

Bij elke functierelease kan de tijdlijn variëren van RTP tot GA. Het doel is om versies kort te houden, zodat binnen 2 maanden na het begin van de release (RTP) een functie GA zal zijn.

## Functiemarkeringen

De vlaggen van de eigenschap worden gebruikt om de zichtbaarheid van nieuwe eigenschappen tijdens versie te controleren. Adobe raadt u aan `app.launchdarkly.com` op uw firewall [lijst van gewenste personen](https://experienceleague.adobe.com/docs/analytics/technotes/ip-addresses.html) voor een optimale ervaring tijdens de afgifte. Kort nadat GA is bereikt, wordt de vlag verwijderd.

U kunt op elk gewenst moment de vlaggen van uw actieve functie weergeven **Help > Info over Werkruimte > Markeringen voor actieve functies**.

## Voordelen

Met gefaseerde releases kan Adobe het implementatieproces van de software beter schalen en ervoor zorgen dat de functies volledig zijn beveiligd voordat de algemene beschikbaarheid beschikbaar is. Ook kunnen functies worden vrijgegeven zodra ze beschikbaar zijn, in plaats van zich aan een vast maandelijks releasevenster te houden.

## Veelgestelde vragen

| Vraag | Antwoord |
| --- | --- |
| Kan ik vroege toegang tot een eigenschap vragen? | Nee. Vroegtijdige toegang wordt niet verleend.<br>Als u de concepten van de vroege Analyse wilt testen, moedigen wij u aan om te proberen [Adobe Analytics Labs](https://experienceleague.adobe.com/docs/analytics/analyze/labs.html) om feedback te geven over onze toonaangevende innovaties. |
| Heeft deze releasestrategie invloed op mijn toegang tot functies? | Nee. Zodra een functie GA heeft bereikt, hebt u toegang tot de functie als deze in het pakket Analytics is opgenomen. |
