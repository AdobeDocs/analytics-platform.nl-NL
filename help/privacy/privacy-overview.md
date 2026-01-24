---
title: Customer Journey Analytics en gegevensbeheer
description: Beschrijft hoe het gegevensbeheer in Customer Journey Analytics werkt.
exl-id: ab2b7ff2-c638-4ab4-bc86-d1701bebcb1a
feature: Privacy
role: Admin
source-git-commit: 40706e3118cbaf7582d8625d307358b16f1836ac
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# Adobe Customer Journey Analytics en gegevensbeheer

In het algemeen worden instellingen met betrekking tot gegevensbeheer in Customer Journey Analytics overgenomen van Adobe Experience Platform.

## Datagovernance

De integratie tussen Adobe Customer Journey Analytics en [&#x200B; het Beheer van Gegevens van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/data-governance/home.html?lang=nl-NL) staat voor etikettering van gevoelige gegevens van Customer Journey Analytics en handhaving van privacybeleid toe.

De etiketten en het beleid van de privacy die op datasets werden gecreeerd die door Experience Platform worden verbruikt kunnen in het werkschema van de gegevensmeningen van Customer Journey Analytics worden aangeschept. Deze labels stoppen of waarschuwen gebruikers die metriek en/of afmetingen van gevoelige velden maken.

Wanneer gegevens uit Customer Journey Analytics worden geëxporteerd (via rapportage, export, API, enz.), worden bovendien waarschuwingen of labels toegevoegd om gebruikers te laten weten dat een rapport gevoelige informatie bevat die op een specifieke manier moet worden behandeld.

Dankzij deze integratie kunt u de compatibiliteit eenvoudiger beheren. Gegevensstewards in uw organisatie kunnen beleid plaatsen om gebruik te beperken. Dit betekent dat uw Customer Journey Analytics-gebruikers gegevens betrouwbaarder kunnen gebruiken, in de wetenschap dat deze in overeenstemming zijn met het beleid dat wordt gedefinieerd door data stewards.

[Meer informatie](/help/data-views/data-governance.md)

## Privacyverzoeken

Adobe behandelt privacyverzoeken in overeenstemming met de toepasselijke lokale en internationale wetgeving.

Omdat Customer Journey Analytics gegevens gebruikt die in Adobe Experience Platform beschikbaar zijn, biedt Adobe [&#x200B; Adobe Experience Platform Privacy Service &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=nl-NL) aan om gegevenstoegang en schrappingsverzoeken voor te leggen. De verzoeken zijn van toepassing op zowel de oorspronkelijke als de opgehaalde gegevensbestanden.

## GDPR

Customer Journey Analytics zal zich niet rechtstreeks op de centrale dienst van de algemene gegevensbeschermingsverordening (GDPR) abonneren en in plaats daarvan alle wijzigingen in de gegevensset die in Experience Platform zijn aangebracht, erven. Customer Journey Analytics is afhankelijk van Platform Data Lake om aanvragen voor verwijdering van GDPR af te dwingen en Customer Journey Analytics op de hoogte te brengen wanneer aanvragen zijn voltooid. Alle veranderingen in beïnvloede partijen in Customer Journey Analytics voor gebeurtenisdatasets worden gesynchroniseerd met de gegevens van het Platform. De datasets van het profiel en van de raadpleging die door GDPR schrappingsverzoeken worden beïnvloed worden volledig opnieuw opgenomen na elk schrappingsverzoek. Verwijderingsverzoeken worden doorgaans binnen 7 dagen na een verwijderingsgebeurtenis in het Data Lake voltooid.

## CCPA

De California Consumer Privacy Act (CCPA) verbetert de privacyrechten en consumentenbescherming voor inwoners van Californië in de Verenigde Staten. Deze wet werd van kracht op 1 januari 2020.
De CCPA biedt de inwoners van Californië nieuwe privacyrechten op het gebied van gegevens, zoals het recht op toegang tot en verwijdering van hun persoonsgegevens, om te weten of hun persoonsgegevens worden verkocht of openbaar gemaakt (en aan wie), en om de verkoop van hun persoonsgegevens te weigeren.
In overeenstemming met de CCPA steunt de Privacy Service verzoeken om zich te onthouden van de verkoop van persoonsgegevens.

>[!MORELIKETHIS]
>
>* [&#x200B; Blog: Hoe te om efficiënt bestuur in Adobe Customer Journey Analytics te handhaven &#x200B;](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/bg-p/adobe-analytics-blogs/page/4?profile.language=nl)
