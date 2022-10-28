---
title: Door de klant beheerde toetsen
description: Leer hoe u door klanten beheerde sleutels voor CJA instelt.
hide: true
hidefromtoc: true
source-git-commit: 90521aa7326486b9016321d35191a73ef891a0bc
workflow-type: tm+mt
source-wordcount: '283'
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

## CMK instellen voor CJA

Ga als volgt te werk om CMK in te stellen voor CJA:

1. Zorg ervoor dat u recht hebt op Adobe CJA CMK door contact op te nemen met het team van uw Adobe-account.
1. Zorg ervoor dat u in Azure een beheerder met een geprivilegieerde rol bent, zoals Toepassingsbeheerder, Cloud Application Administrator of Global Administrator. [Meer informatie van Microsoft](https://learn.microsoft.com/en-us/azure/active-directory/roles/permissions-reference)
1. Maak een nieuwe Azure Key Vault die alleen met CJA kan worden gebruikt. [Meer informatie van Microsoft](https://learn.microsoft.com/en-us/azure/key-vault/general/)
1. Bied de Adobe Azure App toegang tot uw sleutel in de sleutelkluis. Dit is de toepassings-id Adobe: 251e3919-1940-4296-bb8b-6b9a5e8a4805. [Meer informatie over Microsoft](https://learn.microsoft.com/en-us/azure/storage/common/customer-managed-keys-configure-cross-tenant-existing-account?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json&amp;tabs=powershell-preview%2Cazure-portal#the-customer-grants-the-service-providers-app-access-to-the-key-in-the-key-vault)
1. Maak een Adobe Customer Care-ticket voor een aanvraag voor CMK-installatie. Neem de Azure URI op in uw ticket. De URI vindt u in het veld Key Identifier van uw Azure-sleutel.
1. De klantenservice van Adobe bevestigt de voltooiing van de CMK-toepassing op uw CJA-gegevens.
