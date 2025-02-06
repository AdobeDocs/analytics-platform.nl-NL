---
title: Een eigenschap tag maken en de extensie Web SDK toevoegen
description: Leer hoe u een markeringseigenschap maakt en de extensie Web SDK toevoegt
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 382d2b00-939a-4fff-be02-7a98d457a455
source-git-commit: bb87226ee4b9acc433031f41997d403d49f48db3
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# De extensie Web SDK toevoegen aan uw tag {#upgrade-tag-extension}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-tag-extension"
>title="De extensie Platform Web SDK toevoegen aan de eigenschap tag"
>abstract="Voeg de extensie Adobe Experience Platform Web SDK toe aan de eigenschap tag. Het toevoegen van de extensie Web SDK aan de eigenschap tag wordt gestroomlijnd en duurt slechts een paar minuten voordat de bewerking is voltooid."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

Met de functie Codes in Adobe Experience Platform kunt u code op uw site implementeren om gegevens te verzamelen. Met deze oplossing voor tagbeheer kunt u code naast andere coderingsvereisten implementeren. Tags bieden naadloze integratie met Adobe Experience Platform via de Adobe Experience Platform Web SDK-extensie.

De volgende informatie beschrijft hoe u de extensie Web SDK aan uw tag kunt toevoegen. Voor supplementaire informatie, zie [ de de markeringsuitbreiding van SDK van het Web ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) in de documentatie van het Experience Platform vormen. De Web SDK omvat [!UICONTROL Adobe Experience Cloud ID Service] native, zodat te hoeven u niet om de de dienstuitbreiding van identiteitskaart aan uw markering toe te voegen.

Nadat u [ een markering ](/help/getting-started/cja-upgrade/cja-upgrade-tag-property.md) creeert, moet u het met de uitbreiding van SDK van het Web van Adobe Experience Platform vormen. Op deze manier kunt u gegevens naar Adobe Experience Platform verzenden (via uw gegevensstroom).

De extensie Web SDK toevoegen aan uw tag:

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
