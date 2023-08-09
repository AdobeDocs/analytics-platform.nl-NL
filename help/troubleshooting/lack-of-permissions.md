---
title: Gebrek aan machtigingen
description: Leer hoe u problemen kunt oplossen die het gevolg zijn van een gebrek aan machtigingen
role: Data Engineer, Data Architect, Admin
solution: Customer Journey Analytics
feature: Troubleshooting
source-git-commit: 1905e37b76843a7622af4e874a2d74aceff55384
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Gebrek aan machtigingen

Customer Journey Analytics werkt niet correct wanneer bepaalde Adobe Experience Platform-machtigingen niet zijn ingesteld.

Als voorbeeld kunt u een [Verbinding](../connections/overview.md) en [Gegevens, weergave](../data-views/data-views.md)wordt mogelijk de volgende foutmelding weergegeven in het dialoogvenster [Componenten](/help/data-views/create-dataview.md#components) sectie:


>[!BEGINSHADEBOX]

*[!UICONTROL Something went wrong and we couldn't load schema fields. Please try again.]*

>[!ENDSHADEBOX]


Om deze fout te corrigeren, moet u systeem- of productbeheerdersrechten hebben voor een organisatie die een product van een Experience Platform heeft. Zie [Overzicht van toegangsbeheer](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=en#platform-permissions) voor meer informatie .

1. Ga naar de gebruikersinterface van het Adobe Experience Platform.

1. Selecteren **[!UICONTROL Permissions]** van de linkerspoorstaaf.

1. Selecteren **[!UICONTROL Roles]**.

1. Navigeer in de relevante rol.

1. Selecteren ![Bewerken](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) **[!UICONTROL Edit]** om de rol te bewerken.

1. Zorgen **[!UICONTROL Manage Data Usage Policies]** en **[!UICONTROL View Data Usage Policies]** worden toegevoegd aan **[!UICONTROL Data Governance]** container.

1. Selecteren **[!UICONTROL Save]** om de wijzigingen op te slaan


