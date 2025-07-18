---
title: Door de klant beheerde sleutels
description: Leer hoe u door de klant beheerde sleutels voor Customer Journey Analytics instelt.
exl-id: 08ece1cb-22b7-4b8d-be76-5414a810feb6
feature: Privacy
role: Admin
source-git-commit: cdc8d889a05c55d2f4765d0837023d007a5a230d
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Door de klant beheerde sleutels

Adobe Customer Journey Analytics verstrekt de optie voor [ de klanten van het Schild van de Gezondheidszorg ](https://www.adobe.com/trust/compliance/hipaa-ready.html) en van de Privacy &amp; van het Beveiliging om klant-beheerde sleutels (CMK) voor de gegevens van Customer Journey Analytics te gebruiken. Merk op dat dit proces van de [ opstelling van Adobe Experience Platform CMK ](https://experienceleague.adobe.com/nl/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview) gescheiden is. Door de klant beheerde sleutels zijn slechts beschikbaar voor organisaties die het [ toe:voegen-op aanbod van het Schild van de Gezondheidszorg of van de Privacy &amp; van het Beveiliging 1&rbrace; hebben gekocht.](https://experienceleague.adobe.com/nl/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield)

## Door de klant beheerde sleutels instellen voor Customer Journey Analytics in Azure

Voer de volgende stappen uit om CMK voor Customer Journey Analytics in te stellen die wordt uitgevoerd op Azure:

1. Zorg ervoor dat u recht hebt op Adobe Customer Journey Analytics CMK en dat uw organisatie gebruikmaakt van Adobe Experience Platform die in Azure wordt uitgevoerd. U kunt deze rechten controleren door contact op te nemen met uw Adobe-accountteam.
1. Zorg ervoor dat u in Azure een beheerder met een geprivilegieerde rol bent, zoals Toepassingsbeheerder, Cloud Application Administrator of Global Administrator. Zie [ Microsoft Entra ingebouwde rollen ](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference) voor meer informatie.
1. Maak een nieuwe Azure Key Vault die alleen met Customer Journey Analytics kan worden gebruikt. Zie [ Microsoft Azure Key Vault documentatie ](https://learn.microsoft.com/en-us/azure/key-vault/general/) voor meer informatie.
1. Bied de Adobe Azure App toegang tot uw sleutel in de sleutelkluis. U kunt dit op een van de volgende manieren doen:
   * Toestemmingen van de vergunning via vergunningstoestemming via volgende URL: [ https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;client_id=251e3919-1940-4296-bb8b-6b9a5e8a4805&amp;redirect_uri=https://experience.adobe.com&amp;scope=user.read](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&client_id=251e3919-1940-4296-bb8b-6b9a5e8a4805&redirect_uri=https://experience.adobe.com&scope=user.read)

   * Volg de instructies in [ vorm klant-geleide sleutels voor een bestaande rekening ](https://learn.microsoft.com/en-us/azure/storage/common/customer-managed-keys-configure-cross-tenant-existing-account?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json&tabs=powershell-preview%2Cazure-portal#the-customer-grants-the-service-providers-app-access-to-the-key-in-the-key-vault). De Adobe-toepassings-id is:

     **`251e3919-1940-4296-bb8b-6b9a5e8a4805`**

1. Maak een Adobe Customer Care-ticket waarvoor CMK-installatie wordt aangevraagd. Neem de Azure URI op in uw ticket. URI kan op het **Zeer belangrijke Herkenningsteken** gebied van uw Azure sleutel worden gevonden:

   ![ Zeer belangrijke gebieden die van het Herkenningsteken URI voor https://cmkoberontest.vault.azure.net ](assets/key-identifier.png) tonen

1. Adobe Customer Care bevestigt dat de CMK-toepassing op uw Customer Journey Analytics-gegevens is voltooid.

Alle gegevens die door Platform worden gebruikt, worden in doorvoer en in rust gecodeerd om uw gegevens veilig te houden, met of zonder door de klant beheerde sleutels. Voor informatie over de encryptie van Adobe Experience Platform, zie [ encryptie van Gegevens in Adobe Experience Platform ](https://experienceleague.adobe.com/nl/docs/experience-platform/landing/governance-privacy-security/encryption).

## Door klanten beheerde sleutels instellen voor Customer Journey Analytics op Amazon Web Services

>[!AVAILABILITY]
>
>Deze sectie is van toepassing op implementaties van Experience Platform die op Amazon Web Services (AWS) worden uitgevoerd. Experience Platform die op AWS wordt uitgevoerd, is momenteel beschikbaar voor een beperkt aantal klanten. Meer over de gesteunde infrastructuur van Experience Platform leren, zie het [ multi-wolkenoverzicht van Experience Platform ](https://experienceleague.adobe.com/nl/docs/experience-platform/landing/multi-cloud).

Als uw organisatie Adobe Experience Platform gebruikt die op Amazon Web Services wordt uitgevoerd, is CMK al geconfigureerd voor u. Er is geen extra installatie nodig.
