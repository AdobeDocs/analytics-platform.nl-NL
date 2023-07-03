---
title: Customer Journey Analytics- en gegevensbeheer
description: Beschrijft hoe het gegevensbeheer in Customer Journey Analytics werkt.
exl-id: ab2b7ff2-c638-4ab4-bc86-d1701bebcb1a
feature: Privacy
source-git-commit: edbad9c9d3dc0b48db5334828a18ef652d4a38aa
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 1%

---

# Adobe Customer Journey Analytics en gegevensbeheer

In het algemeen worden instellingen met betrekking tot gegevensbeheer in Customer Journey Analytics overgenomen van Adobe Experience Platform.

## Data Governance

De integratie tussen Adobe Customer Journey Analytics en [Adobe Experience Platform Data Governance](https://experienceleague.adobe.com/docs/experience-platform/data-governance/home.html?lang=en) maakt etikettering van gevoelige Customer Journey Analytics-gegevens en handhaving van het privacybeleid mogelijk.

De etiketten en het beleid van de privacy die op datasets werden gecreeerd die door Experience Platform worden verbruikt kunnen in het werkschema van de de gegevensmeningen van Customer Journey Analytics worden bezocht. Deze labels stoppen of waarschuwen gebruikers die metriek en/of afmetingen van gevoelige velden maken.

Wanneer gegevens uit Customer Journey Analytics worden geëxporteerd (via rapportage, export, API, enz.), worden bovendien waarschuwingen of labels toegevoegd om gebruikers te laten weten dat een rapport gevoelige informatie bevat die op een specifieke manier moet worden behandeld.

Dankzij deze integratie kunt u de compatibiliteit eenvoudiger beheren. Gegevensstewards in uw organisatie kunnen beleid plaatsen om gebruik te beperken. Dit betekent dat uw Customer Journey Analytics-gebruikers gegevens betrouwbaarder kunnen gebruiken, in de wetenschap dat deze voldoen aan het beleid dat wordt gedefinieerd door data stewards.

[Meer informatie](/help/data-views/data-governance.md)

## GDPR

Customer Journey Analytics zal zich niet rechtstreeks op de centrale dienst van de algemene gegevensbeschermingsverordening (GDPR) abonneren en in plaats daarvan alle wijzigingen in de gegevensset in Experience Platform erven. Wij hangen van het meer van Gegevens van het Platform af om GDPR verwijderingsverzoeken af te dwingen en ons op de hoogte te brengen wanneer zij op Pijpleiding zijn voltooid. Wij luisteren aan Pijpleiding en synchroniseren alle veranderingen in beïnvloede partijen in Customer Journey Analytics voor gebeurtenisdatasets. De datasets van het profiel en van de raadpleging die door GDPR schrappingsverzoeken worden beïnvloed zullen volledig na elke schrappingsverzoek opnieuw worden opgenomen. We kunnen garanderen dat verzoeken om verwijdering binnen 7 dagen na een verwijderingsgebeurtenis in het Data Lake worden uitgevoerd.

## CCPA

De California Consumer Privacy Act (CCPA) verbetert de privacyrechten en consumentenbescherming voor inwoners van Californië in de Verenigde Staten. Deze wet werd van kracht op 1 januari 2020.
De CCPA biedt de inwoners van Californië nieuwe privacyrechten op het gebied van gegevens, zoals het recht op toegang tot en verwijdering van hun persoonsgegevens, om te weten of hun persoonsgegevens worden verkocht of openbaar gemaakt (en aan wie), en om de verkoop van hun persoonsgegevens te weigeren.
Overeenkomstig de PPV steunt de Privacy Service verzoeken om zich te onthouden van de verkoop van persoonsgegevens.
