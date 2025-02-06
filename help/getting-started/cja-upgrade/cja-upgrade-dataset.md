---
title: Een schema voor Customer Journey Analytics maken
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: d686dcdd-08d5-4e8f-8f0d-76c8c7b0427f
source-git-commit: bb87226ee4b9acc433031f41997d403d49f48db3
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Een gegevensset maken om met Customer Journey Analytics te gebruiken {#upgrade-create-dataset}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-dataset-create"
>title="Een gegevensset maken in Adobe Experience Platform"
>abstract="Een dataset is een plaats waar de verzamelde gegevens verblijven. Maak deze locatie in Adobe Experience Platform.<br><br> Creërend een dataset met een schema in mening neemt slechts een paar notulen."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/data-ingestion/aepwebsdk.md-->

Een dataset is de constructie die de gegevens opslaat en beheert die u in Adobe Experience Platform verzamelt.

Een gegevensset maken:

1. In Adobe Experience Platform selecteert u in de linkertrack **[!UICONTROL Datasets]** within [!UICONTROL DATA MANAGEMENT] .

1. Selecteer **[!UICONTROL Create dataset]** .

   ![ creeer dataset ](assets/create-dataset.png)

1. Selecteer **[!UICONTROL Create dataset from schema]** .

   ![ creeer dataset van schema ](assets/create-dataset-from-schema.png)

1. Selecteer het schema dat u eerder hebt gemaakt en selecteer **[!UICONTROL Next]** .

1. Geef uw gegevensset een naam en (optioneel) geef een beschrijving op.

   ![ dataset van de Naam ](assets/name-your-datatest.png)

1. Selecteer **[!UICONTROL Finish]** .

1. Selecteer de **[!UICONTROL Profile]** schakelaar.

   U wordt ertoe aangezet om de dataset voor profiel toe te laten. Zodra toegelaten, verrijkt de dataset klantenprofielen in real time met zijn opgenomen gegevens.

   >[!IMPORTANT]
   >
   >    U kunt een dataset voor profiel slechts toelaten wanneer het schema, waaraan de dataset voldoet, ook voor profiel wordt toegelaten.

   ![ laat schema voor profiel ](assets/aepwebsdk-dataset-profile.png) toe

   Zie {de gids UI van de Datasets van 0} ](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=nl) voor veel meer informatie over hoe te bekijken, voorproef, tot stand brengen en een dataset schrappen. [ U kunt ook leren hoe te om een dataset voor het Profiel van de Klant in real time toe te laten.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
