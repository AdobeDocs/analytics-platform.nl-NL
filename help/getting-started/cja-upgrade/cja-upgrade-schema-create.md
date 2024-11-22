---
title: Een schema voor Customer Journey Analytics maken
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 902e5890-f970-4f1a-b091-9c3e51a987db
source-git-commit: 8bcc6b3b2a1e6f75bd0c868f77a375913412f988
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 0%

---

# Creeer een schema XDM om met uw implementatie van SDK van het Web van de Customer Journey Analytics te gebruiken

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

>[!IMPORTANT]
>
>Voordat u begint met het maken van uw XDM-schema, werkt u samen met uw gegevensteam en andere belanghebbenden in uw hele organisatie om het ideale schemaontwerp van uw organisatie voor Customer Journey Analytics en de andere Adobe Experience Platform-toepassingen die u gebruikt, te identificeren. Voor meer informatie, zie [ architect uw schema voor gebruik met Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-architect.md).

Adobe raadt u aan een XDM-schema (Custom Experience Data Model) te maken bij de upgrade naar Customer Journey Analytics. Een douaneschema staat voor een gestroomlijnd schema toe dat aan de behoeften van uw organisatie en de specifieke toepassingen van het Platform wordt aangepast die u gebruikt. Wanneer veranderingen in het schema worden vereist, moet u niet door duizenden ongebruikte gebieden bewegen om het gebied te vinden dat het bijwerken vereist.

## Het schema maken

Het XDM-schema dat u definieert, vertegenwoordigt het model van de gegevens die u in Adobe Experience Platform verzamelt.

Een aangepast schema maken:

<!-- Should we single source this instead of duplicate it? The following steps were copied from: /help/data-ingestion/aepwebsdk.md-->

1. In Adobe Experience Platform selecteert u in de linkertrack **[!UICONTROL Schemas]** within [!UICONTROL DATA MANAGEMENT] .

1. Selecteer **[!UICONTROL Create schema]** .

1. In de stap **[!UICONTROL Select a class]** van de wizard Schema maken:

   1. Selecteer **[!UICONTROL Experience Event]** .

      ![ creeer een schema dat de Gebeurtenis van de Ervaring benadrukt ](assets/create-ee-schema-wizard-step-1.png)

      >[!INFO]
      >
      >    Een schema van de Gebeurtenis van de Ervaring wordt gebruikt om het _gedrag_ van een profiel (als scènenaam, drukknop te modelleren om aan wagentje toe te voegen). Een individueel schema van het Profiel wordt gebruikt om de profiel _attributen_ (zoals naam, e-mail, geslacht) te modelleren.

   1. Selecteer **[!UICONTROL Next]** .


1. In het gedeelte [!UICONTROL Name and review step] van de wizard [!UICONTROL Create schema] :

   1. Voer een **[!UICONTROL Schema display name]** in voor uw schema en (optioneel) een **[!UICONTROL Description]** .

      ![ creeer schemavenster dat de Naam toont uw schemagebieden ](assets/create-ee-schema-wizard-step-2.png)

   1. Selecteer **[!UICONTROL Finish]** .

1. Voeg alle veldgroepen toe die velden bevatten die u in uw schema wilt opnemen.

   Veldgroepen zijn herbruikbare verzamelingen van objecten en kenmerken waarmee u het schema eenvoudig kunt uitbreiden.

   1. Selecteer **[!UICONTROL + Add]** in de sectie **[!UICONTROL Field groups]** .

      ![ voeg gebiedsgroep ](assets/add-field-group-button.png) toe

   1. Selecteer in het dialoogvenster [!UICONTROL Add fields groups] de veldgroep **[!UICONTROL AEP Web SDK ExperienceEvent]** in de lijst.

      ![ AEP Web SDK ExperienceEvent gebiedsgroep ](assets/select-aepwebsdk-experienceevent.png)

      U kunt de voorvertoningsknop selecteren om een voorvertoning weer te geven van de velden die deel uitmaken van deze veldgroep, bijvoorbeeld `web > webPageDetails > name` .

      ![ AEP Web SDK ExperienceEvent gebiedsgroepvoorproef ](assets/aepwebsdk-experiencevent-preview.png)

      Selecteer **[!UICONTROL Back]** om de voorvertoning te sluiten.

   1. (Optioneel) Selecteer eventuele extra veldgroepen die u wilt opnemen.

   1. Selecteer **[!UICONTROL Add field groups]** .

1. (Optioneel) Als u aangepaste velden hebt die u in het schema wilt opnemen, maakt u een aangepaste veldgroep en voegt u de aangepaste velden toe aan de veldgroep.

   1. Selecteer **[!UICONTROL + Add]** in de sectie **[!UICONTROL Field groups]** .

      ![ voeg gebiedsgroep ](assets/add-field-group-button.png) toe

   1. Selecteer **[!UICONTROL Create new field group]** in het dialoogvenster [!UICONTROL Add fields groups] .

   1. Geef een weergavenaam en optionele beschrijving op en selecteer vervolgens **[!UICONTROL Add field groups]** .

1. Selecteer **[!UICONTROL +]** naast de naam van het schema in het deelvenster [!UICONTROL Structure] .

   ![ het Schema van het Voorbeeld voegt de knoop van het Gebied toe ](assets/example-schema-plus.png)

1. Typ in het deelvenster [!UICONTROL Field Properties] `Identification` als de naam, **[!UICONTROL Identification]** als de [!UICONTROL Display name] , selecteer **[!UICONTROL Object]** als de [!UICONTROL Type] en selecteer **[!UICONTROL ExperienceEvent Core v2.1]** als de [!UICONTROL Field Group] .

   >[!NOTE]
   >
   >Als die veldgroep niet beschikbaar is, zoekt u naar een andere veldgroep met identiteitsvelden. Of [ creeer een nieuwe gebiedsgroep ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/field-groups.html) en [ voeg nieuwe identiteitsgebieden ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/fields/identity.html#define-a-identity-field) (als `ecid`, `crmId`, en anderen toe u) aan de gebiedsgroep nodig hebt en selecteer die nieuwe gebiedsgroep.

   ![ Voorwerp van de Identificatie ](assets/identification-field.png)

   Het identificatieobject voegt id-mogelijkheden toe aan uw schema. In uw geval wilt u profielen identificeren die uw site bezoeken met de Experience Cloud-id en het e-mailadres. Er zijn vele andere eigenschappen beschikbaar om de identificatie van uw persoon te volgen (bijvoorbeeld klant identiteitskaart, loyalty identiteitskaart).

   Selecteer **[!UICONTROL Apply]** om dit object aan uw schema toe te voegen.

1. Selecteer het veld **[!UICONTROL ecid]** in het identificatieobject dat u net hebt toegevoegd en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Primary Identity]** en **[!UICONTROL ECID]** in de lijst [!UICONTROL Identity namespace] in het rechterdeelvenster.

   ![ specificeer ECID als identiteit ](./assets/specify-identity.png)

   U geeft de Experience Cloud Identity op als de primaire identiteit die de Adobe Experience Platform Identity-service kan gebruiken om het gedrag van profielen te combineren (aan te sluiten) met dezelfde ECID.

   Selecteer **[!UICONTROL Apply]** . U ziet dat er een vingerafdrukpictogram wordt weergegeven in het ecid-kenmerk.

1. Selecteer het veld **[!UICONTROL email]** in het identificatieobject dat u net hebt toegevoegd en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Email]** in de lijst [!UICONTROL Identity namespace] in het deelvenster [!UICONTROL Field Properties] .

   ![ specificeer e-mail als identiteit ](./assets/specify-email-identity.png)

   U geeft het e-mailadres op als een andere identiteit die de Adobe Experience Platform Identity-service kan gebruiken om het gedrag van profielen te combineren (naaien).

   Selecteer **[!UICONTROL Apply]** . U ziet dat er een vingerafdrukpictogram wordt weergegeven in het e-mailkenmerk.

   Selecteer **[!UICONTROL Save]** .

1. (Optioneel) Als u Customer Journey Analytics wilt integreren met RTCDP, selecteert u het basiselement van het schema met de naam van het schema en selecteert u vervolgens de **[!UICONTROL Profile]** -switch.

   U wordt gevraagd het schema in te schakelen voor het profiel. Zodra toegelaten, wanneer het gegeven in datasets wordt opgenomen die op dit schema worden gebaseerd, worden die gegevens samengevoegd in het Real-Time Profiel van de Klant.

   Zie [ het schema voor gebruik in het Profiel van de Klant in real time ](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#profile) voor meer informatie toelaten.

   >[!IMPORTANT]
   >
   >Nadat u een schema voor profiel hebt ingeschakeld, kan het niet voor profiel worden uitgeschakeld.

   ![ laat schema voor profiel ](./assets/enable-for-profile.png) toe

1. Selecteer **[!UICONTROL Save]** om het schema op te slaan.

   U hebt een minimumschema gemaakt dat de gegevens modelleert die u van uw website kunt vastleggen. Met het schema kunnen profielen worden geïdentificeerd aan de hand van de identiteit en het e-mailadres van het Experience Cloud. Door het schema voor profiel in te schakelen, zorgt u ervoor dat gegevens die vanaf uw website zijn vastgelegd, worden toegevoegd aan het realtime-klantprofiel.

   Naast gedragsgegevens kunt u ook profielkenmerkgegevens van uw site vastleggen (bijvoorbeeld gegevens over profielen die zijn geabonneerd op een nieuwsbrief).

   Als u deze profielgegevens wilt vastleggen, doet u het volgende:

   * Maak een schema op basis van de klasse Individueel profiel XDM.

   * Voeg de het gebiedsgroep van de Kern van het Profiel v2 aan het schema toe.

   * Voeg een identificatieobject toe op basis van de veldgroep Profile Core v2.

   * Experience Cloud-id definiëren als primaire id en e-mailadres als id.

   * Het schema inschakelen voor profiel

   Zie [ schema&#39;s in UI ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html) voor meer informatie creëren en uitgeven bij het toevoegen van en het verwijderen van gebiedsgroepen en individuele gebieden aan een schema.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
