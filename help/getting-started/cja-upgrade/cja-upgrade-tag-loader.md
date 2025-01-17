---
title: De ladertag voor de Web SDK-extensie implementeren
description: Leer hoe u de ladertag voor de extensie Web SDK implementeert
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 471ecd60-6e1e-4889-93bd-c654b35d40dc
source-git-commit: cb6a439def7bf0fab1768fdd1c7d909b76b995d6
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# De ladertag voor de Web SDK-extensie implementeren

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

U moet de tag installeren op de website die u wilt bijhouden. Dit houdt in dat code in de kopteksttag van de sjabloon van uw website wordt geplaatst.

In het volgende proces wordt beschreven hoe u de code ophaalt die naar de tag verwijst. Voor supplementaire informatie, zie de [ gidsen van de Implementatie voor markeringen en gebeurtenis door:sturen ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/get-started/implementation-guides) in de documentatie van het Experience Platform.

De code ophalen die naar de tag verwijst:

1. Meld u aan bij experience.adobe.com met uw Adobe ID-referenties.

1. Ga in Adobe Experience Platform naar **[!UICONTROL Data Collection]** > **[!UICONTROL Tags]** .

1. Selecteer op de pagina **[!UICONTROL Tag Properties]** de zojuist gemaakte tag in de lijst met eigenschappen om deze te openen.

1. Selecteer **[!UICONTROL Environments]** in het linkerspoor.

1. Selecteer de juiste installatieknop in de lijst met omgevingen.

   Selecteer in het dialoogvenster [!UICONTROL Web Install Instructions] de knop Kopiëren naast de scriptcode die als volgt moet worden gelezen:

   ```
   <script src="https://assets.adobedtm.com/2a518741ab24/.../launch-...-development.min.js" async></script>>
   ```

   ![ Milieu ](assets/environment.png)

1. Selecteer **[!UICONTROL Close]** .

   In plaats van de code voor de ontwikkelomgeving, zou u een andere omgeving (het opvoeren, de productie) kunnen selecteren die op waar wordt gebaseerd u bezig bent om het Web SDK van Adobe Experience Platform op te stellen.

   Zie [ Milieu&#39;s ](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html?) voor meer informatie.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
