---
title: Overzicht van verbindingen met Customers Journey Analytics
description: Meer informatie over verbindingen in Customer Journey Analytics.
solution: Customer Journey Analytics
feature: Connections
exl-id: 012371d7-aaef-4018-95ee-5c52083e9d8f
role: Admin
source-git-commit: 14cdc7bd8817dbf1d7a9950fa6ff62aedff82640
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# Overzicht van verbindingen

De verbindingen staan de beheerders van het het productproduct van de Customer Journey Analytics toe om verbindingen met verschillende AEP gegevensbronnen, zoals gebeurtenis, raadpleging, en profieldatasets te vestigen. Deze verbindingen laten de integratie van gegevens van een Verbinding aan een afgeleide Mening van Gegevens toe. We raden u aan de toegang tot het Connections-beheer te beperken tot een kernbeheergroep. Configuraties op het niveau van de Verbinding hebben contractuele implicaties met betrekking tot volumetoewijzing voor gegevens die in Customer Journey Analytics worden gebracht.
De verbindingen zijn de stichting van CJA en worden gecreeerd van AEP brondatasets. De toegang tot Verbindingen verstrekt ook de capaciteit om de manager van Verbindingen te bekijken, die u de onderliggende datasets laat bekijken die omhoog de verbinding maken, evenals kritieke het uitgeven en configuratieselecties maken.

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/35111/?quality=12&learn=on)

## Vereiste machtigingen

Om een Verbinding van de Customer Journey Analytics tot stand te brengen, hebt u de volgende toestemmingen nodig in [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-permissions-and-roles.ug.html):

Adobe Experience Platform:
* Gegevensmodellering: Schema&#39;s weergeven, Schema&#39;s beheren
* gegevensbeheer: gegevenssets weergeven, gegevenssets beheren
* Gegevensinname: Bronnen beheren
* Identiteitsnaamruimten weergeven

Customer Journey Analytics
* Toegang tot productbeheerder

>[!IMPORTANT]
>
>U kunt meerdere [!DNL Experience Platform] datasets in één enkele verbinding.
