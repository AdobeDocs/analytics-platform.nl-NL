---
title: Gebrek aan machtigingen
description: Leer hoe u problemen kunt oplossen die het gevolg zijn van een gebrek aan machtigingen
role: Admin
solution: Customer Journey Analytics
feature: Troubleshooting
exl-id: 341123b9-f4d6-4ef7-96f1-789850261b96
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Gebrek aan machtigingen

Customer Journey Analytics werkt niet correct wanneer bepaalde Adobe Experience Platform-machtigingen niet zijn ingesteld.

Als voorbeeld kunt u een [Verbinding](../connections/overview.md) en [Gegevens, weergave](../data-views/data-views.md)wordt mogelijk de volgende foutmelding weergegeven in het dialoogvenster [Componenten](/help/data-views/create-dataview.md#components) sectie:


>[!BEGINSHADEBOX]

*[!UICONTROL Something went wrong retrieving DULE policies. Please verify account permissions, policies, or labels. Message: Forbidden.]*

>[!ENDSHADEBOX]


1. Zorg ervoor dat u het juiste toegangsbeheer hebt:

   * U moet systeem of productbeheerdervoorrechten voor een organisatie hebben die een product van de Experience Platform heeft. Zie [Overzicht van toegangsbeheer](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=en#platform-permissions) voor meer informatie .

   * U moet een gebruiker in het AEP-Standaard-Alle-Gebruikers productprofiel zijn. Vraag uw beheerder als u niet de toestemmingen hebt om zich aan dit profiel toe te voegen. Zie [Toegangsbeheerhiërarchie en -workflow](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=en#access-control-hierarchy-and-workflow) voor meer informatie .


1. Navigeer naar de gebruikersinterface van het Adobe Experience Platform.

1. Selecteren **[!UICONTROL Permissions]** van de linkerspoorstaaf.

1. Selecteren **[!UICONTROL Roles]**.

1. Navigeer in de relevante rol.

1. Selecteren ![Bewerken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) **[!UICONTROL Edit]** om de rol te bewerken.

1. Zorgen **[!UICONTROL Manage Data Usage Policies]** en **[!UICONTROL View Data Usage Policies]** worden toegevoegd aan **[!UICONTROL Data Governance]** container.

1. Selecteren **[!UICONTROL Save]** om de wijzigingen op te slaan
