---
title: Door de klant beheerde toetsen
description: Leer hoe u door de klant beheerde sleutels voor Customer Journey Analytics instelt.
exl-id: 08ece1cb-22b7-4b8d-be76-5414a810feb6
feature: Privacy
role: Admin
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Door de klant beheerde toetsen

Adobe Customer Journey Analytics biedt de optie voor [Gezondheidsschild](https://www.adobe.com/trust/compliance/hipaa-ready.html) en Privacy &amp; Security Shield-klanten om een Azure Customer Managed Key (CMK) te gebruiken die op de gegevens van uw Customer Journey Analytics moet worden toegepast.  Merk op dat dit proces los staat van [Adobe Experience Platform CMK instellen](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys.html).

>[!NOTE]
>
>Door de klant beheerde toetsen zijn momenteel alleen beschikbaar voor organisaties die de [Gezondheidsschild of privacy- en beveiligingsschild](https://experienceleague.adobe.com/docs/customer-data-management-voices-events/events/governance/healthcare-shield.html?lang=en) invoegtoepassing.

## CMK instellen voor Customer Journey Analytics

Ga als volgt te werk om CMK voor Customer Journey Analytics in te stellen:

1. Zorg ervoor dat u recht hebt op Adobe Customer Journey Analytics CMK door contact op te nemen met het accountteam van uw Adobe.
1. Zorg ervoor dat u in Azure een beheerder met een geprivilegieerde rol bent, zoals Toepassingsbeheerder, Cloud Application Administrator of Global Administrator. [Meer informatie van Microsoft](https://learn.microsoft.com/en-us/azure/active-directory/roles/permissions-reference)
1. Maak een nieuwe Azure Key Vault die alleen met Customer Journey Analytics kan worden gebruikt. [Meer informatie van Microsoft](https://learn.microsoft.com/en-us/azure/key-vault/general/)
1. Bied de Adobe Azure App toegang tot uw sleutel in de sleutelkluis. Dit is de toepassings-id van de Adobe: 251e3919-1940-4296-bb8b-6b9a5e8a4805. [Meer informatie over Microsoft](https://learn.microsoft.com/en-us/azure/storage/common/customer-managed-keys-configure-cross-tenant-existing-account?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json&amp;tabs=powershell-preview%2Cazure-portal#the-customer-grants-the-service-providers-app-access-to-the-key-in-the-key-vault)
1. Maak een Adobe Customer Care-ticket waarvoor CMK-installatie wordt aangevraagd. Neem de Azure URI op in uw ticket. De URI vindt u in het dialoogvenster **Sleutel-id** van uw Azure Key.

   ![Sleutel-id-velden met de URI voor https://cmkoberontest.vault.azure.net](assets/key-identifier.png)

1. De klantenservice van de Adobe zal bevestigen dat de CMK-toepassing op de gegevens van uw Customer Journey Analytics is voltooid.

Alle gegevens die door Platform worden gebruikt, worden in doorvoer en in rust gecodeerd om uw gegevens veilig te houden, met of zonder CMK. Voor informatie over Adobe Experience Platform-codering, [Meer informatie](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=en).
