---
title: De loader-tag voor de Web SDK-extensie implementeren
description: Leer hoe te om de ladermarkering voor de uitbreiding van SDK van het Web uit te voeren
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: ccc6df56771cd9f83bbd7a8570e32d7ed63a0ced
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# De loader-tag voor de Web SDK-extensie implementeren

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

U moet de tag installeren op de website die u wilt bijhouden. Dit houdt in dat code in de kopteksttag van de sjabloon van uw website wordt geplaatst.

In het volgende proces wordt beschreven hoe u de code ophaalt die naar de tag verwijst. Voor supplementaire informatie, zie de [ gidsen van de Implementatie voor markeringen en gebeurtenis door:sturen ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/get-started/implementation-guides) in de documentatie van het Experience Platform.

De code ophalen die naar de tag verwijst:

1. Selecteer **[!UICONTROL Environments]** in het linkerspoor.

1. Selecteer de juiste installatieknop in de lijst met omgevingen.

   Selecteer in het dialoogvenster [!UICONTROL Web Install Instructions] de knop Kopiëren naast de scriptcode die als volgt moet worden gelezen:

   ```
   <script src="https://assets.adobedtm.com/2a518741ab24/.../launch-...-development.min.js" async></script>>
   ```

   ![ Milieu ](assets/environment.png)

1. Selecteer **[!UICONTROL Close]** .

   In plaats van de code voor het ontwikkelmilieu, zou u een ander milieu (het opvoeren, productie) kunnen selecteren die op waar wordt gebaseerd u in het opstellen van het Web SDK van Adobe Experience Platform bent.

   Zie [ Milieu&#39;s ](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html?) voor meer informatie.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.

