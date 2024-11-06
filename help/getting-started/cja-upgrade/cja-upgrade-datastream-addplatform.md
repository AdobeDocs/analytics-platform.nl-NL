---
title: Een schema voor Customer Journey Analytics maken
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: 33cfff3f675fc03c3444531e8426cb806cdf8559
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---

# Platform toevoegen als service aan uw datastream

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/data-ingestion/aepwebsdk.md-->

Een gegevensstroom zou reeds moeten bestaan alvorens u de stappen in deze sectie voltooit. Wanneer en hoe de gegevensstroom werd gecreeerd hangt van uw implementatie van Adobe Analytics af, als volgt:

* Als uw Adobe Analytics-implementatie gebruikmaakt van de Web SDK of de Web SDK Extension, was de datastream beschikbaar voor uw Adobe Analytics-omgeving, voorafgaand aan het upgradeproces.

* Voor andere implementaties van Adobe Analytics, maakt het creëren van een gegevensstroom deel uit van het verbeteringsproces, zoals die in [ wordt beschreven creeer een gegevensstroom om met Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-datastream.md) te gebruiken.

Met de beschikbare gegevensstroom, moet u Platform als dienst toevoegen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform **[!UICONTROL Datastreams]** in [!UICONTROL DATA COLLECTION] in de linkertrack.

1. Selecteer de gegevensstroom die eerder werd gevormd. <!--true?-->

1. Selecteer **[!UICONTROL Add Service]** .

1. In de lus [!UICONTROL Add Service screen] :

   1. Selecteer **[!UICONTROL Adobe Experience Platform]** in de lijst [!UICONTROL Service] .

   1. Zorg ervoor dat **[!UICONTROL Enabled]** is geselecteerd.

   1. Selecteer de gegevensset in de lijst [!UICONTROL Event Dataset] .

      ![ datastream AEP dienst ](./assets/datastream-aep-service.png)

   1. Laat de andere instellingen staan en selecteer **[!UICONTROL Save]** om de gegevensstroom op te slaan.

   Uw gegevensstroom is nu geconfigureerd om de gegevens die van uw website zijn verzameld door te sturen naar uw gegevensset in Adobe Experience Platform.

   Zie [ Overzicht van gegevensstromen ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html) voor meer informatie over hoe te om een gegevensstroom te vormen en hoe te om gevoelige gegevens te behandelen.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
