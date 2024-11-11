---
title: Een eigenschap tag maken en de extensie Web SDK toevoegen
description: Leer hoe te om een markeringsbezit tot stand te brengen en de uitbreiding van SDK van het Web toe te voegen
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: ccc6df56771cd9f83bbd7a8570e32d7ed63a0ced
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# De Web SDK-extensie toevoegen aan uw tag

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

Met de functie Codes in Adobe Experience Platform kunt u code op uw site implementeren om gegevens te verzamelen. Met deze oplossing voor tagbeheer kunt u code naast andere coderingsvereisten implementeren. Tags bieden naadloze integratie met Adobe Experience Platform via de Adobe Experience Platform Web SDK-extensie.

De volgende informatie beschrijft hoe te om de uitbreiding van SDK van het Web aan uw markering toe te voegen. Voor supplementaire informatie, zie [ de de markeringsuitbreiding van SDK van het Web ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) in de documentatie van het Experience Platform vormen. De SDK van het Web omvat [!UICONTROL Adobe Experience Cloud ID Service] native, zodat te hoeven u niet om de de dienstuitbreiding van identiteitskaart aan uw markering toe te voegen.

Nadat u [ een markering ](/help/getting-started/cja-upgrade/cja-upgrade-tag-property.md) creeert, moet u het met de uitbreiding van SDK van het Web van Adobe Experience Platform vormen. Op deze manier kunt u gegevens naar Adobe Experience Platform verzenden (via uw gegevensstroom).

U voegt als volgt de extensie SDK voor het web toe aan uw tag:

1. Meld u aan bij experience.adobe.com met uw Adobe ID-referenties.

1. Ga in Adobe Experience Platform naar **[!UICONTROL Data Collection]** > **[!UICONTROL Tags]** .

1. Selecteer de nieuwe tag in de lijst met [!UICONTROL Tag Properties] om deze te openen.

1. Selecteer **[!UICONTROL Extensions]** in het linkerspoor.

1. Selecteer **[!UICONTROL Catalog]** in de bovenste balk.

1. Zoek naar of blader naar **[!UICONTROL Adobe Experience Platform Web SDK extension]**, dan selecteer **[!UICONTROL Install]** om het te installeren.

   <img src="assets/aepwebsdk-extension.png" width="35%"/>

1. Selecteer de sandbox en de eerder gemaakte gegevensstroom voor de [!UICONTROL Production Environment] en (optioneel) [!UICONTROL Staging Environment] en [!UICONTROL Development Environment] .

   ![ de uitbreidingsconfiguratie van SDK van het Web AEP ](assets/aepwebsk-extension-datastreams.png)

1. Selecteer **[!UICONTROL Save]** .

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.