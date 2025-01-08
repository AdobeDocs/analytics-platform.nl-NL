---
title: Door de klant beheerde sleutels
description: Leer hoe te opstelling klant-geleide sleutels voor Customer Journey Analytics.
exl-id: 08ece1cb-22b7-4b8d-be76-5414a810feb6
feature: Privacy
role: Admin
source-git-commit: dfdb6bc5c190e4de98eaef86e0c8d118327640a6
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Door de klant beheerde sleutels

Adobe Customer Journey Analytics verstrekt de optie voor [ de klanten van het Schild van de Gezondheidszorg ](https://www.adobe.com/trust/compliance/hipaa-ready.html) en van de Privacy &amp; van het Beveiliging om klant-beheerde sleutels (CMK) voor Customer Journey Analytics gegevens te gebruiken. Merk op dat dit proces van de [ opstelling van Adobe Experience Platform CMK ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview) gescheiden is. Door de klant beheerde sleutels zijn slechts beschikbaar voor organisaties die het ](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield) toe:voegen-op aanbod van het Schild van de Gezondheidszorg of van de Privacy &amp; van het Beveiliging 1} hebben gekocht.[

## Door de klant beheerde sleutels instellen voor Customer Journey Analytics in Azure

Voer de volgende stappen uit om CMK in te stellen voor Customer Journey Analytics die wordt uitgevoerd in Azure:

1. Zorg ervoor dat u recht hebt op Adobe Customer Journey Analytics CMK en dat uw organisatie gebruikmaakt van Adobe Experience Platform die in Azure wordt uitgevoerd. U kunt deze rechten controleren door contact op te nemen met het accountteam van de Adobe.
1. Zorg ervoor dat u in Azure een beheerder met een geprivilegieerde rol bent, zoals Toepassingsbeheerder, Cloud Application Administrator of Global Administrator. Zie [ Microsoft Entra ingebouwde rollen ](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference) voor meer informatie.
1. Maak een nieuwe Azure Key Vault die alleen met Customer Journey Analytics kan worden gebruikt. Zie [ Microsoft Azure Key Vault documentatie ](https://learn.microsoft.com/en-us/azure/key-vault/general/) voor meer informatie.
1. Bied de Adobe Azure App toegang tot uw sleutel in de sleutelkluis. Zie [ klant-geleide sleutels voor een bestaande rekening ](https://learn.microsoft.com/en-us/azure/storage/common/customer-managed-keys-configure-cross-tenant-existing-account?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json&amp;tabs=powershell-preview%2Cazure-portal#the-customer-grants-the-service-providers-app-access-to-the-key-in-the-key-vault) voor meer informatie vormen. De toepassings-id van de Adobe is:

   **`251e3919-1940-4296-bb8b-6b9a5e8a4805`**

1. Maak een Adobe Customer Care-ticket waarvoor CMK-installatie wordt aangevraagd. Neem de Azure URI op in uw ticket. URI kan op het **Zeer belangrijke Herkenningsteken** gebied van uw Azure sleutel worden gevonden:

   ![ Zeer belangrijke gebieden die van het Herkenningsteken URI voor https://cmkoberontest.vault.azure.net ](assets/key-identifier.png) tonen

1. De Zorg van de Klant van de Adobe bevestigt de voltooiing van de toepassing CMK op uw gegevens van de Customer Journey Analytics.

Alle gegevens die door Platform worden gebruikt, worden in doorvoer en in rust gecodeerd om uw gegevens veilig te houden, met of zonder door de klant beheerde sleutels. Voor informatie over de encryptie van Adobe Experience Platform, zie [ encryptie van Gegevens in Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/encryption).

## Door klanten beheerde sleutels instellen voor Customer Journey Analytics op Amazon Web Services

>[!AVAILABILITY]
>
>Deze sectie is van toepassing op implementaties van Experience Platform dat op Amazon Web Services (AWS) loopt. Experience Platform dat op AWS wordt uitgevoerd, is momenteel beschikbaar voor een beperkt aantal klanten. Meer over de gesteunde infrastructuur van het Experience Platform leren, zie het [ Experience Platform multi-cloud overzicht ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/multi-cloud).

Als uw organisatie Adobe Experience Platform gebruikt die op Amazon Web Services wordt uitgevoerd, is CMK al geconfigureerd voor u. Er is geen extra installatie nodig.
