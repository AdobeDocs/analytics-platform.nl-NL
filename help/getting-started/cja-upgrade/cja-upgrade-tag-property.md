---
title: Een eigenschap tag maken en de extensie Web SDK toevoegen
description: Leer hoe u een markeringseigenschap maakt en de extensie Web SDK toevoegt
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 156df830-541d-4c92-9c49-98f346e040a7
source-git-commit: bb87226ee4b9acc433031f41997d403d49f48db3
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Een tag voor uw eigenschap maken {#upgrade-tag-property}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-tag-property"
>title="Een tag-eigenschap maken in de gegevensverzameling van Adobe Experience Platform"
>abstract="Tags zijn de standaardstandaard voor gegevensverzameling. Maak een tag in de Adobe Experience Platform-interface, zodat u de variabelen voor gegevensverzameling op elk gewenst moment kunt bijwerken.<br><br> de verwezenlijking van een markeringsbezit kan in verscheidene kliks worden voltooid, die slechts een paar notulen nemen."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

Met de functie Codes in Adobe Experience Platform kunt u code op uw site implementeren om gegevens te verzamelen. Met deze oplossing voor tagbeheer kunt u code naast andere coderingsvereisten implementeren. Tags bieden naadloze integratie met Adobe Experience Platform via de Adobe Experience Platform Web SDK-extensie.

De volgende informatie beschrijft hoe u een tag voor uw eigenschap kunt maken. Voor supplementaire informatie, zie [ de de markeringsuitbreiding van SDK van het Web ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) in de documentatie van het Experience Platform vormen. De Web SDK omvat [!UICONTROL Adobe Experience Cloud ID Service] native, zodat te hoeven u niet om de de dienstuitbreiding van identiteitskaart aan uw markering toe te voegen.

Een eigenschap is in feite een container die u vult met extensies, regels, gegevenselementen en bibliotheken wanneer u tags op uw site implementeert. Veel mensen maken een eigenschap voor elke website (of groep nauw verwante sites) waar ze dezelfde set tags willen implementeren. Voor meer over eigenschappen, zie [ Eigenschappen ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/admin/companies-and-properties) in de documentatie van de de gegevensinzameling van het Experience Platform.

U kunt als volgt een tag voor uw eigenschap maken:

1. Meld u aan bij experience.adobe.com met uw Adobe ID-referenties.

1. Ga in Adobe Experience Platform naar **[!UICONTROL Data Collection]** > **[!UICONTROL Tags]** .

1. Selecteer **[!UICONTROL New Property]** .

   Geef de tag een naam, selecteer **[!UICONTROL Web]** en voer een domeinnaam in. Selecteer **[!UICONTROL Save]** om door te gaan.

   ![ creeer een bezit ](assets/create-property.png)

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
