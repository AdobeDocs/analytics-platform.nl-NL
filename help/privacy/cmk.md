---
title: Door de klant beheerde toetsen
description: Leer hoe u door klanten beheerde sleutels voor CJA instelt.
source-git-commit: 4894519f618b79a5ca29952df48291c44915adae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Door de klant beheerde toetsen

>[!NOTE]
>
>Deze functionaliteit zal in november 2022 beschikbaar zijn.

Customer Journey Analytics (CJA) biedt de mogelijkheid voor klanten van het gezondheidsschild en privacy- en beveiligingsschild om een Azure Customer Managed Key (CMK) te gebruiken die op uw CJA-gegevens moet worden toegepast.  Dit proces staat los van de Adobe Experience Platform CMK-instelling (koppeling om te volgen).

>[!NOTE]
>
>Door de klant beheerde toetsen zijn momenteel alleen beschikbaar voor organisaties die de [Gezondheidsschild of privacy- en beveiligingsschild](https://experienceleague.adobe.com/docs/blueprints-learn/architecture/vertical-blueprints/healthcare-vertical.html%3Flang%3Den) invoegtoepassing.

Ga als volgt te werk om CMK in te stellen voor CJA:

1. Zorg ervoor dat u recht hebt op CMK door contact op te nemen met uw Adobe-accountteam.
1. Maak een nieuwe Azure Key Vault die alleen met CJA kan worden gebruikt.
1. Steek uw Azure Key Value naar de Azure CJA CMK-app (link naar follow-up).
1. Maak een Adobe Customer Care-ticket voor een aanvraag voor CMK-installatie. Neem de Azure URI op in uw ticket.
1. De klantenservice van Adobe zal bevestigen dat de CMK-toepassing op uw CJA-gegevens is voltooid.
