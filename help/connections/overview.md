---
title: Overzicht van verbindingen met Customers Journey Analytics
description: Meer informatie over verbindingen in Customer Journey Analytics.
solution: Customer Journey Analytics
feature: Connections
exl-id: 012371d7-aaef-4018-95ee-5c52083e9d8f
role: Admin
source-git-commit: 2f78905c2a1e94174a52269becc15474baf59f71
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Overzicht van verbindingen

Via verbindingen kunnen Customer Journey Analytics-productbeheerders verbindingen tot stand brengen met verschillende [!DNL Adobe Experience Platform] -gegevensbronnen, zoals gebeurtenis-, opzoekgegevens en profielgegevenssets. Deze verbindingen laten de integratie van gegevens van een Verbinding aan een afgeleide Mening van Gegevens toe. Verbindingen vormen de basis van CJA en worden gemaakt op basis van [!DNL Experience Platform] brondatasets. De toegang tot Verbindingen laat u ook de manager van Verbindingen bekijken, waar u de onderliggende datasets kunt bekijken die omhoog de verbinding maken, evenals kritieke het uitgeven en configuratieselecties maken.

We raden u aan de toegang tot het Connections-beheer te beperken tot een kernbeheergroep. Configuraties op het niveau van de Verbinding hebben contractuele implicaties met betrekking tot volumetoewijzing voor gegevens die in Customer Journey Analytics worden gebracht.

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/35111/?quality=12&learn=on)

## Vereiste machtigingen

Om een Verbinding van de Customer Journey Analytics tot stand te brengen, hebt u de volgende toestemmingen nodig. Voor extra details over toestemmingen, verwijs naar documentatie voor [ Adobe Admin Console ](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-permissions-and-roles.ug.html) en [ de Toestemmingen van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home).

### In Adobe Admin Console:

* Customer Journey Analytics: Productbeheerder
* Adobe Experience Platform: Toegevoegd aan het Profiel van het Product genoemd *AEP-gebrek-Alle-Gebruikers*

### In Adobe Experience Platform-machtigingen:

* Gegevensmodellering: Schema&#39;s weergeven, Schema&#39;s beheren
* gegevensbeheer: gegevenssets weergeven, gegevenssets beheren
* Gegevensinname: Bronnen beheren
* Identity Management: Naamruimten weergeven
* Sandboxen: sandboxen gebruikt in gerelateerde Customer Journey Analytics-verbindingen

>[!IMPORTANT]
>
>U kunt meerdere [!DNL Experience Platform] datasets combineren in één verbinding.
