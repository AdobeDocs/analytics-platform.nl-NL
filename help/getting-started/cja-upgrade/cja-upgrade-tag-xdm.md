---
title: XDM-logica voor gegevensverzameling toevoegen aan uw tag
description: Leer hoe u XDM-logica voor gegevensverzameling aan uw tag kunt toevoegen
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: ccc6df56771cd9f83bbd7a8570e32d7ed63a0ced
workflow-type: tm+mt
source-wordcount: '1071'
ht-degree: 0%

---

# XDM-logica voor gegevensverzameling toevoegen aan uw tag

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

Na [ het creëren van de markering en het toevoegen van de uitbreiding van SDK van het Web ](/help/getting-started/cja-upgrade/cja-upgrade-tag-property.md), moet u het met gegevenselementen en regels vormen, volgens hoe u uw plaats wilt volgen en gegevens verzenden naar Adobe Experience Platform. Nadat u gegevenselementen en regels voor uw markering vormt, kunt u het bouwen en publiceren.

## Gegevenselementen configureren

Gegevenselementen zijn de bouwstenen voor uw gegevenswoordenboek (of gegevenskaart). Gebruik gegevenselementen om gegevens te verzamelen, te organiseren en te leveren over marketing- en advertentietechnologie. U stelt gegevenselementen in uw tag in die worden gelezen van uw gegevenslaag en die kunnen worden gebruikt om gegevens naar Adobe Experience Platform te verzenden.

Er zijn verschillende typen gegevenselementen. Stel eerst een gegevenselement in om de paginanaam vast te leggen die personen op uw site bekijken. Stel vervolgens een gegevenselement in dat verwijst naar de Experience Cloud-id. Definieer ten slotte een XDM-objectelement.

### Gegevenselement paginanaam

Een gegevenselement voor de paginanaam definiëren:

1. Meld u aan bij experience.adobe.com met uw Adobe ID-referenties.

1. Ga in Adobe Experience Platform naar **[!UICONTROL Data Collection]** > **[!UICONTROL Tags]** .

1. Selecteer de nieuwe tag in de lijst met [!UICONTROL Tag Properties] om deze te openen.

1. Selecteer **[!UICONTROL Data Elements]** in het linkerspoor.

1. Selecteer **[!UICONTROL Add Data Element]** .

1. Geef in het dialoogvenster [!UICONTROL Create Data Element] de volgende informatie op:

   * **[!UICONTROL Name]**: De naam van het gegevenselement. Bijvoorbeeld `Page Name` .

   * **[!UICONTROL Extension]**: selecteer **[!UICONTROL Core]** in de lijst.

   * **[!UICONTROL Data Element Type]**: selecteer **[!UICONTROL Page Info]** in de lijst.

   * **[!UICONTROL Attribute]**: selecteer **[!UICONTROL Title]** in de lijst.

     ![ creeer het Element van de Datum gebruikend Info van de Pagina ](assets/create-dataelement-1.png)

     U had ook de waarde van een variabele in uw gegevenslaag kunnen gebruiken, bijvoorbeeld `pageName` en het gegevenstype [!UICONTROL JavaScript Variable] voor gegevenselementen om het gegevenselement te definiëren.

     ![ creeer het Element van Gegevens gebruikend Variabele JavaScript ](assets/create-dataelement-2.png)

1. Selecteer **[!UICONTROL Save]** .

   U wilt nu opstelling een gegevenselement van verwijzingen voorzien van Experience Cloud identiteitskaart die automatisch door het Web SDK van Adobe Experience Platform en beschikbaar door de uitbreiding van de Dienst van identiteitskaart van het Experience Cloud wordt verstrekt.

1. Ga met [ ECID gegevenselement ](#ecid-data-element) verder.

### ECID-gegevenselement

Een ECID-gegevenselement definiëren:

1. Meld u aan bij experience.adobe.com met uw Adobe ID-referenties.

1. Ga in Adobe Experience Platform naar **[!UICONTROL Data Collection]** > **[!UICONTROL Tags]** .

1. Selecteer de nieuwe tag in de lijst met [!UICONTROL Tag Properties] om deze te openen.

1. Selecteer **[!UICONTROL Data Elements]** in het linkerspoor.

1. Selecteer **[!UICONTROL Add Data Element]** .

1. Geef in het dialoogvenster [!UICONTROL Create Data Element] de volgende informatie op:

   * **[!UICONTROL Name]**: De naam van het gegevenselement. Bijvoorbeeld `ECID` .

   * **[!UICONTROL Extension]**: selecteer **[!UICONTROL Experience Cloud ID Service]** in de lijst.

   * **[!UICONTROL Data Element Type]**: selecteer **[!UICONTROL ECID]** in de lijst.

     ![ ECID het Element van Gegevens ](assets/ecid-dataelement.png)

1. Selecteer **[!UICONTROL Save]** .

1. Ga met [ XDM objecten gegevenselement ](#xdm-object-data-element) verder.

### XDM-objectgegevenselement

Tot slot wilt u nu om het even welke specifieke gegevenselementen aan het schema in kaart brengen u vroeger bepaalde. U definieert een ander gegevenselement dat een representatie van uw XDM-schema biedt.

Een XDM-objectelement definiëren:

1. Meld u aan bij experience.adobe.com met uw Adobe ID-referenties.

1. Ga in Adobe Experience Platform naar **[!UICONTROL Data Collection]** > **[!UICONTROL Tags]** .

1. Selecteer de nieuwe tag in de lijst met [!UICONTROL Tag Properties] om deze te openen.

1. Selecteer **[!UICONTROL Data Elements]** in het linkerspoor.

1. Selecteer **[!UICONTROL Add Data Element]** .

1. Geef in het dialoogvenster [!UICONTROL Create Data Element] de volgende informatie op:

   * **[!UICONTROL Name]**: De naam van het gegevenselement. Bijvoorbeeld `XDM - Page View` .

   * **[!UICONTROL Extension]**: selecteer **[!UICONTROL Adobe Experience Platform Web SDK]** in de lijst.

   * **[!UICONTROL Data Element Type]**: selecteer **[!UICONTROL XDM Object]** in de lijst.

   * **[!UICONTROL Sandbox]**: selecteer de sandbox in de lijst.

   * **[!UICONTROL Schema]**: selecteer het schema in de lijst.

1. Wijs het kenmerk `identification > core > ecid`, dat in uw schema is gedefinieerd, toe aan het gegevenselement ECID. Selecteer het cilinderpictogram om het ECID-gegevenselement gemakkelijk te kiezen in de lijst met gegevenselementen.

   ![ Uitgezocht ECID het Element van Gegevens ](assets/pick-ecid-dataelement.png)

   ![ het Element van Gegevens van de Kaart ECID ](assets/map-ecid.png)


1. Wijs het kenmerk `web > webPageDetails > name`, dat in uw schema is gedefinieerd, toe aan het gegevenselement Paginanaam.

   ![ het Element van de Gegevens van de Naam van de Pagina van de Kaart ](assets/map-pagename.png)

1. Selecteer **[!UICONTROL Save]** .

1. Ga met [ verder vormen regels ](#configure-rules).

## **vorm regels**

Tags in Adobe Experience Platform volgen een op regels gebaseerd systeem. Zij zoeken gebruikersinteractie en bijbehorende gegevens. Wanneer aan de criteria die in uw regels worden geschetst wordt voldaan, teweegbrengt de regel de uitbreiding, het manuscript, of cliënt-zijcode in werking u identificeerde. U kunt regels gebruiken om gegevens (zoals een voorwerp XDM) naar Adobe Experience Platform te verzenden gebruikend de uitbreiding van SDK van het Web van Adobe Experience Platform.

Een regel definiëren:

>[!NOTE]
>
>De volgende stappen zijn een voorbeeld van het definiëren van een regel die XDM-gegevens met waarden uit andere gegevenselementen naar Adobe Experience Platform verzendt.
>
>U kunt regels op verschillende manieren in uw tag gebruiken om variabelen te bewerken (met behulp van uw gegevenselementen).
>
>Zie [ Regels ](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html) voor meer informatie.

1. Meld u aan bij experience.adobe.com met uw Adobe ID-referenties.

1. Ga in Adobe Experience Platform naar **[!UICONTROL Data Collection]** > **[!UICONTROL Tags]** .

1. Selecteer de nieuwe tag in de lijst met [!UICONTROL Tag Properties] om deze te openen.

1. Selecteer **[!UICONTROL Rules]** in het linkerspoor.

1. Selecteer **[!UICONTROL Create New Rule]** .

1. Geef in het dialoogvenster [!UICONTROL Create Rule] de volgende informatie op:

   * **[!UICONTROL Name]**: De naam van de regel. Bijvoorbeeld `Page View` .

   * **[!UICONTROL Events]**: Selecteer **[!UICONTROL + Add]** . Geef vervolgens in het dialoogvenster [!UICONTROL Event Configuration] de volgende informatie op. Selecteer **[!UICONTROL Keep Changes]** wanneer u klaar bent.

      * **[!UICONTROL Extension]**: selecteer **[!UICONTROL Core]** in de lijst.

      * **[!UICONTROL Event Type]**: selecteer **[!UICONTROL Window Loaded]** in de lijst.

        ![ Regel - de Configuratie van de Gebeurtenis ](assets/event-windowloaded-pageview.png)

   * **[!UICONTROL Actions]**: Selecteer **[!UICONTROL + Add]** . Geef vervolgens in het dialoogvenster [!UICONTROL Action Configuration] de volgende informatie op. Selecteer **[!UICONTROL Keep Changes]** wanneer u klaar bent.

      * **[!UICONTROL Extension]**: selecteer **[!UICONTROL Adobe Experience Platform Web SDK]** in de lijst.

      * **[!UICONTROL Action Type]**: selecteer **[!UICONTROL Send Event]** in de lijst.

      * **[!UICONTROL Type]**: selecteer **[!UICONTROL web.webpagedetails.pageViews]** in de lijst.

      * **[!UICONTROL XDM data]**: Selecteer het cilinderpictogram en selecteer vervolgens **[!UICONTROL XDM - Page View]** in de lijst met gegevenselementen.

        ![ Regel - de Configuratie van de Actie ](assets/action-pageview-xdm.png)

        Uw regel moet er als volgt uitzien:

        ![ creeer Regel ](assets/rule-pageview.png)

1. Selecteer **[!UICONTROL Save]** .

## Uw tag maken en publiceren

Nadat u gegevenselementen en regels hebt gedefinieerd, moet u de tag maken en publiceren. Wanneer u een bibliotheek maakt, moet u deze toewijzen aan een omgeving. De uitbreidingen, de regels, en de gegevenselementen van de bouwstijl worden dan gecompileerd en in het toegewezen milieu geplaatst. Elke omgeving bevat een unieke insluitcode waarmee u de toegewezen build in uw site kunt integreren.

Adobe Experience Platform-tags ondersteunen eenvoudige tot complexe publicatieworkflows die geschikt zijn voor uw implementatie van de Adobe Experience Platform Web SDK. Zie [ het Publiceren overzicht ](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html) voor meer informatie.

Om uw markering te bouwen en te publiceren:

1. Meld u aan bij experience.adobe.com met uw Adobe ID-referenties.

1. Ga in Adobe Experience Platform naar **[!UICONTROL Data Collection]** > **[!UICONTROL Tags]** .

1. Selecteer de nieuwe tag in de lijst met [!UICONTROL Tag Properties] om deze te openen.

1. Selecteer **[!UICONTROL Publishing Flow]** in het linkerspoor.

1. Selecteer **[!UICONTROL Select a working library]** , gevolgd door **[!UICONTROL Add Library…]** .

1. Geef in het dialoogvenster [!UICONTROL Create Library] de volgende informatie op:

   * **[!UICONTROL Name]**: De naam van de bibliotheek.

   * **[!UICONTROL Environment]**: selecteer **[!UICONTROL Development (development)]** in de lijst.

1. Selecteer **[!UICONTROL + Add All Changed Resources]** .

   ![ Publish - creeer Bibliotheek ](assets/create-library-aep.png)

1. Selecteer **[!UICONTROL Save & Build to Development]** .

   Uw tag wordt opgeslagen en gebouwd voor uw ontwikkelomgeving. Een groene stip geeft aan dat uw tag met succes is opgebouwd in uw ontwikkelomgeving.

1. U kunt **[!UICONTROL ...]** selecteren om de bibliotheek opnieuw samen te stellen of de bibliotheek naar een testomgeving of productieomgeving te verplaatsen.

   ![ Publish - bouwt Bibliotheek ](assets/build-library.png)

