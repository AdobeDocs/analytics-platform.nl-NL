---
title: Een schema voor Customer Journey Analytics maken
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: f76d098d-d223-40e4-be81-d28e7581396b
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Een gegevensstroom maken voor gebruik met Customer Journey Analytics {#upgrade-create-datastream}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-datastream-create"
>title="Een gegevensstroom maken in Adobe Experience Platform"
>abstract="Een gegevensstroom is een intermediaire plaats die uw gegevens tot alle gevormde diensten overgaat. Maak deze locatie in Adobe Experience Platform.<br><br> de aanvankelijke verwezenlijking van een gegevensstroom in de interface van het Platform neemt slechts een paar notulen."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/data-ingestion/aepwebsdk.md-->

Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web van Adobe Experience Platform en Mobiele SDKs. Bij het verzamelen van gegevens met de SDK&#39;s van Adobe Experience Platform worden gegevens naar de Adobe Experience Platform Edge Network verzonden. Het is de gegevensstroom die bepaalt aan welke diensten dat de gegevens door:sturen.

In uw opstelling, wilt u de gegevensstroom vormen om de verzamelde gegevens naar uw dataset in Adobe Experience Platform te verzenden.

>[!NOTE]
>
>De volgende stappen zijn alleen vereist voor Adobe Analytics-implementaties met AppMeasurement of de extensie Analytics (tags).
>
>Als in uw Adobe Analytics-implementatie de extensie Web SDK of Web SDK wordt gebruikt, bestaat de gegevensstroom al in uw Adobe Analytics-omgeving.

Uw gegevensstroom instellen:

1. Selecteer in Adobe Experience Platform **[!UICONTROL Datastreams]** in [!UICONTROL DATA COLLECTION] in de linkertrack.

1. Selecteer **[!UICONTROL New Datastream]** .

1. Geef een naam en beschrijf de gegevensstroom. Selecteer het schema in de lijst [!UICONTROL Event Schema] .

   ![ Nieuwe DataStream ](assets/new-datastream.png)

1. Selecteer **[!UICONTROL Save]** .

{{upgrade-final-step}}
