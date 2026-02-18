---
title: Een schema voor Customer Journey Analytics maken
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: d686dcdd-08d5-4e8f-8f0d-76c8c7b0427f
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# Een gegevensset maken voor gebruik met Customer Journey Analytics {#upgrade-create-dataset}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-dataset-create"
>title="Een gegevensset maken in Adobe Experience Platform"
>abstract="Een dataset is een plaats waar de verzamelde gegevens verblijven. Maak deze locatie in Adobe Experience Platform.<br><br> Creërend een dataset met een schema in mening neemt slechts een paar notulen."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/data-ingestion/aepwebsdk.md-->

Een dataset is de constructie die de gegevens opslaat en beheert die u in Adobe Experience Platform verzamelt.

Een gegevensset maken:

1. In Adobe Experience Platform selecteert u in de linkertrack **[!UICONTROL Datasets]** within [!UICONTROL DATA MANAGEMENT] .

1. Selecteer **[!UICONTROL Create dataset]**.

   ![&#x200B; creeer dataset &#x200B;](assets/create-dataset.png)

1. Selecteer **[!UICONTROL Create dataset from schema]**.

   ![&#x200B; creeer dataset van schema &#x200B;](assets/create-dataset-from-schema.png)

1. Selecteer het schema dat u eerder hebt gemaakt en selecteer **[!UICONTROL Next]** .

1. Geef uw gegevensset een naam en (optioneel) geef een beschrijving op.

   ![&#x200B; dataset van de Naam &#x200B;](assets/name-your-datatest.png)

1. Selecteer **[!UICONTROL Finish]**.

1. Selecteer de **[!UICONTROL Profile]** schakelaar.

   U wordt ertoe aangezet om de dataset voor profiel toe te laten. Zodra toegelaten, verrijkt de dataset klantenprofielen in real time met zijn opgenomen gegevens.

   >[!IMPORTANT]
   >
   >    U kunt een dataset voor profiel slechts toelaten wanneer het schema, waaraan de dataset voldoet, ook voor profiel wordt toegelaten.

   ![&#x200B; laat schema voor profiel &#x200B;](assets/aepwebsdk-dataset-profile.png) toe

   Zie {de gids UI van de Datasets van 0} [&#x200B; voor veel meer informatie over hoe te bekijken, voorproef, tot stand brengen en een dataset schrappen. &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=nl) U kunt ook leren hoe te om een dataset voor het Profiel van de Klant in real time toe te laten.

{{upgrade-final-step}}
