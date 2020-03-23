---
title: Privacyoverzicht van analyse van klantgegevens
description: Beschrijft hoe de privacymontages in de Analyse van de Reis van de Klant werken.
translation-type: tm+mt
source-git-commit: 415a4a7f7d540a0329f973042d1c6a6a285d5b1b

---


# Privacyoverzicht van analyse van klantgegevens

In het algemeen worden privacygerelateerde instellingen in de Klantenreisanalyse overgenomen van het Adobe Experience Platform.

## GDPR

De analyse van de Reis van de klant zal niet direct aan de Algemene Dienst van de Verordening van de Bescherming van Gegevens onderschrijven (GDPR) en zal in plaats daarvan alle veranderingen van dataset erven die in het Platform van de Ervaring worden aangebracht. We zijn afhankelijk van Platform Data Lake om aanvragen voor verwijdering van GDPR af te dwingen en stellen ons op de hoogte wanneer deze zijn voltooid op Pipeline. Wij luisteren aan Pijpleiding en synchroniseren alle veranderingen in beïnvloede partijen in de Analyse van de Reis van de Klant voor gebeurtenisdatasets. De datasets van het profiel en van de raadpleging die door GDPR schrappingsverzoeken worden beïnvloed zullen volledig na elke schrappingsverzoek opnieuw worden opgenomen. We kunnen garanderen dat verzoeken om verwijdering binnen 7 dagen na een verwijderingsgebeurtenis in het Data Lake worden uitgevoerd.

## CCPA

De California Consumer Privacy Act (CCPA) verbetert de privacyrechten en consumentenbescherming voor inwoners van Californië in de Verenigde Staten. Deze wet wordt van kracht op 1 januari 2020.
De CCPA biedt de inwoners van Californië nieuwe privacyrechten op het gebied van gegevens, zoals het recht op toegang tot en verwijdering van hun persoonsgegevens, om te weten of hun persoonsgegevens worden verkocht of openbaar gemaakt (en aan wie), en om de verkoop van hun persoonsgegevens te weigeren.
In afwachting van de CCPA zal de Privacy Service verzoeken om niet te mogen verkopen van persoonsgegevens ondersteunen.
