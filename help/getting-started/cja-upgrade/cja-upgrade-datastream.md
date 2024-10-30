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
source-wordcount: '221'
ht-degree: 0%

---

# Een gegevensstroom maken voor gebruik met Customer Journey Analytics

>[!NOTE]
>
>Deze documentatie zou na de voltooiing van [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) moeten worden gebruikt.
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige stappen hebt uitgevoerd die dynamisch voor uw organisatie zijn gegenereerd.
>
>Nadat u de stappen op deze pagina voltooit, ga na de verbeteringsstappen voort die dynamisch voor uw organisatie van [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/data-ingestion/aepwebsdk.md-->

Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web van Adobe Experience Platform en Mobiele SDKs. Bij het verzamelen van gegevens met de SDK&#39;s van Adobe Experience Platform worden gegevens naar de Adobe Experience Platform-Edge Network verzonden. Het is de gegevensstroom die bepaalt aan welke diensten dat de gegevens door:sturen.

In uw opstelling, wilt u de gegevens die u van de website verzamelt worden verzonden naar uw dataset in Adobe Experience Platform.

Uw gegevensstroom instellen:

1. Selecteer in Adobe Experience Platform **[!UICONTROL Datastreams]** in [!UICONTROL DATA COLLECTION] in de linkertrack.

1. Selecteer **[!UICONTROL New Datastream]** .

1. Geef een naam en beschrijf de gegevensstroom. Selecteer het schema in de lijst [!UICONTROL Event Schema] .

   ![ Nieuwe DataStream ](assets/new-datastream.png)

1. Selecteer **[!UICONTROL Save]** .

1. Ga na de verbeteringsstappen verder die dynamisch voor uw organisatie van [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.

