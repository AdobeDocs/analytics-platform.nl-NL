---
title: Door de klant beheerde toetsen
description: Leer hoe u door klanten beheerde sleutels voor CJA instelt.
hide: true
hidefromtoc: true
source-git-commit: ce386f30e344b3921689a8ecc0e6fba0a55137f9
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Door de klant beheerde toetsen

>[!NOTE]
>
>Deze functionaliteit zal in november 2022 beschikbaar zijn.

Customer Journey Analytics (CJA) biedt de optie voor [Gezondheidsschild](https://www.adobe.com/trust/compliance/hipaa-ready.html) en Privacy &amp; Security Shield-klanten gebruiken een Azure Customer Managed Key (CMK) die op uw CJA-gegevens moet worden toegepast.  Merk op dat dit proces los staat van [Adobe Experience Platform CMK instellen](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys.html).

>[!NOTE]
>
>Door de klant beheerde toetsen zijn momenteel alleen beschikbaar voor organisaties die de [Gezondheidsschild of privacy- en beveiligingsschild](https://experienceleague.adobe.com/docs/blueprints-learn/architecture/vertical-blueprints/healthcare-vertical.html%3Flang%3Den) invoegtoepassing.

Ga als volgt te werk om CMK in te stellen voor CJA:

1. Zorg ervoor dat u recht hebt op CMK door contact op te nemen met uw Adobe-accountteam.
1. Maak een nieuwe Azure Key Vault die alleen met CJA kan worden gebruikt.
1. Steek uw Azure Key Value naar de Azure CJA CMK-app (link naar follow-up).
1. Maak een Adobe Customer Care-ticket voor een aanvraag voor CMK-installatie. Neem de Azure URI op in uw ticket.
1. De klantenservice van Adobe zal bevestigen dat de CMK-toepassing op uw CJA-gegevens is voltooid.
