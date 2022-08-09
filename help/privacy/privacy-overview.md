---
title: Customer Journey Analytics- en gegevensbeheer
description: Beschrijft hoe het gegevensbeheer in Customer Journey Analytics werkt.
exl-id: ab2b7ff2-c638-4ab4-bc86-d1701bebcb1a
source-git-commit: 2f74c10f821aed421e31ee8e14b854f2a73c11f1
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Customer Journey Analytics- en gegevensbeheer

In het algemeen worden instellingen met betrekking tot gegevensbeheer in Customer Journey Analytics overgenomen van Adobe Experience Platform.

## Data Governance

CJA biedt ondersteuning voor labels en beleidsregels voor gegevensbeheer die zijn ingesteld in Adobe Experience Platform. Zie voor meer informatie [CJA-ondersteuning voor Adobe Experience Platform Data Governance](/help/data-views/data-governance.md).

## GDPR

Customer Journey Analytics zal zich niet rechtstreeks op de centrale dienst van de algemene gegevensbeschermingsverordening (GDPR) abonneren en in plaats daarvan alle wijzigingen in de gegevensset in Experience Platform erven. We zijn afhankelijk van het Platform Data Lake voor het afdwingen van aanvragen voor het verwijderen van GDPR en melden ons wanneer deze zijn voltooid op de Pipeline. Wij luisteren aan Pijpleiding en synchroniseren alle veranderingen in beïnvloede partijen in Customer Journey Analytics voor gebeurtenisdatasets. De datasets van het profiel en van de raadpleging die door GDPR schrappingsverzoeken worden beïnvloed zullen volledig na elke schrappingsverzoek opnieuw worden opgenomen. We kunnen garanderen dat verzoeken om verwijdering binnen 7 dagen na een verwijderingsgebeurtenis in het Data Lake worden uitgevoerd.

## CCPA

De California Consumer Privacy Act (CCPA) verbetert de privacyrechten en consumentenbescherming voor inwoners van Californië in de Verenigde Staten. Deze wet wordt van kracht op 1 januari 2020.
De CCPA biedt de inwoners van Californië nieuwe privacyrechten op het gebied van gegevens, zoals het recht op toegang tot en verwijdering van hun persoonsgegevens, om te weten of hun persoonsgegevens worden verkocht of openbaar gemaakt (en aan wie), en om de verkoop van hun persoonsgegevens te weigeren.
In afwachting van de CCPA zal de Privacy Service verzoeken om niet te mogen verkopen van persoonsgegevens steunen.
