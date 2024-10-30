---
title: Een schema voor Customer Journey Analytics maken
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: 711e92db7084592dc562eda3d0dcf33bcb4a62d4
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Een gegevensset maken om met Customer Journey Analytics te gebruiken

>[!NOTE]
>
>Deze documentatie zou na de voltooiing van [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) moeten worden gebruikt.
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige stappen hebt uitgevoerd die dynamisch voor uw organisatie zijn gegenereerd.
>
>Nadat u de stappen op deze pagina voltooit, ga na de verbeteringsstappen voort die dynamisch voor uw organisatie van [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/data-ingestion/aepwebsdk.md-->

Na het creëren van een schema XDM, moet u nu de constructie bepalen om die gegevens op te slaan en te beheren, die in Adobe Experience Platform door een dataset wordt gedaan.

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

1. Ga na de verbeteringsstappen verder die dynamisch voor uw organisatie van [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.

