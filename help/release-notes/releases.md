---
description: Verklaart de ononderbroken strategie van de eigenschapversie voor Customer Journey Analytics
title: Release-strategie voor Customer Journey Analytics-functies
exl-id: aebe709a-4cc7-4197-86e9-b26ab2874375
feature: Release Notes
source-git-commit: 39e4c17336d3648cbf20cace535668d14510186f
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---

# Release-strategie voor Customer Journey Analytics-functies

De versies van de Customer Journey Analytics werken op een ononderbroken leveringsmodel dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat.

## Releasestrategie

[!UICONTROL Analysis Workspace] maakt gebruik van functiemarkeringen (ook wel &#39;&#39;schakelingen&#39;&#39; genoemd) om de zichtbaarheid van nieuwe functies te bepalen, zodat tests op gecontroleerde schaal vóór volledige release mogelijk zijn. Deze releasestrategie omvat de volgende fasen:

* **Beperkte tests**: Een gefaseerde release begint met het testen door interne gebruikers van de Adobe. Het wordt dan ter beschikking gesteld aan een kleine groep klantenrekeningen om ervoor te zorgen dat de eigenschap aan klantenbehoeften en verwachtingen voldoet.

* **Begin van rollout**: De introductie van een gefaseerde release begint met de beperkte testfase. De release wordt vervolgens in de loop van een paar maanden geschaald van 0% naar 100% beschikbaarheid voor klanten. De gefaseerde uitrol gebeurt op het niveau van de Organisatie van het Experience Cloud, zodat ontvangen alle gemachtigde gebruikers in een organisatie de zelfde ervaring.

* **Algemene beschikbaarheid (GA)**: De functie is beschikbaar voor 100% van de organisaties van Experiencen Cloud met bevoegdheid en de release met functies is voltooid.

Bij elke functierelease kan de tijdlijn variëren van RTP tot GA. Het doel is om versies kort te houden, zodat binnen 2 maanden na het begin van de release (RTP) een functie GA zal zijn.

## Functiemarkeringen

De vlaggen van de eigenschap worden gebruikt om de zichtbaarheid van nieuwe eigenschappen tijdens versie te controleren. Adobe beveelt aan toestemming te verlenen `app.launchdarkly.com` via de firewall van uw organisatie voor een optimale ervaring tijdens releases. Deze markeringen worden verwijderd nadat een functie aan iedereen is vrijgegeven. Zie [Door Customer Journey Analytics gebruikte domeinen](../technotes/domains.md) voor meer informatie .

U kunt op elk gewenst moment de vlaggen van uw actieve functie weergeven **Help > Info over Werkruimte > Markeringen voor actieve functies**.

## Voordelen

De gefaseerde versies laten Adobe toe om het proces van de softwareplaatsing beter te schrapen en ervoor te zorgen de eigenschappen volledig worden versterkt alvorens Algemene Beschikbaarheid. Ook kunnen functies worden vrijgegeven zodra ze beschikbaar zijn, in plaats van zich aan een vast maandelijks releasevenster te houden.

## Veelgestelde vragen

| Vraag | Antwoord |
| --- | --- |
| Kan ik vroege toegang tot een eigenschap vragen? | Nee. Vroegtijdige toegang wordt niet verleend.<br>Als u de concepten van de vroege Analyse wilt testen, moedigen wij u aan om te proberen [Adobe Analytics Labs](https://experienceleague.adobe.com/docs/analytics/analyze/labs.html) om feedback te geven over onze toonaangevende innovaties. |
| Heeft deze releasestrategie invloed op mijn toegang tot functies? | Nee. Zodra een functie GA heeft bereikt, hebt u toegang tot de functie als deze in het pakket Analytics is opgenomen. |
