---
title: Gegevens invoeren via de Adobe Experience Platform Web SDK
description: Verklaar hoe te om gegevens in Customer Journey Analytics via het Web SDK van Adobe Experience Platform en het Netwerk van de Rand in te voeren
solution: Customer Journey Analytics
feature: Basics
exl-id: 0b595e9e-0dcf-4c70-ac6d-5a2322824328
source-git-commit: c343a729de4cb13473a7acc04e837b5e5f69809b
workflow-type: tm+mt
source-wordcount: '3292'
ht-degree: 0%

---

# Gegevens invoeren via de Adobe Experience Platform Web SDK

In deze handleiding voor snel starten wordt uitgelegd hoe u gegevens voor het bijhouden van websites rechtstreeks in Adobe Experience Platform kunt invoeren met de Adobe Experience Platform Web SDK en Edge Network en deze gegevens vervolgens in de Customer Journey Analytics kunt gebruiken.

Hiervoor moet u:

- **Een schema en gegevensset instellen** in Adobe Experience Platform om het model (schema) te bepalen van de gegevens die u wilt verzamelen en waar te om de gegevens (dataset) daadwerkelijk te verzamelen.

- **Een gegevensstroom instellen** om het Adobe Experience Platform Edge Network te configureren om de verzamelde gegevens te routeren naar de gegevensset die u in Adobe Experience Platform hebt geconfigureerd.

- **Tags gebruiken** om regels en gegevenselementen eenvoudig te configureren op basis van de gegevens in uw gegevenslaag op uw website. Vervolgens zorgt u ervoor dat de gegevens worden verzonden naar de gegevensstroom die op het Adobe Experience Platform Edge-netwerk is geconfigureerd.

- **Implementeren en valideren**. Zorg voor een omgeving waarin u de ontwikkeling van tags kunt doorlopen en publiceer deze live in uw productieomgeving als alles is gevalideerd.

- **Een verbinding instellen** in de Customer Journey Analytics. Deze verbinding zou (minstens) uw dataset van Adobe Experience Platform moeten omvatten.

- **Een gegevensweergave instellen** in Customer Journey Analytics om metriek en afmeting te bepalen die u in Analysis Workspace wilt gebruiken.

- **Een project instellen** in Customer Journey Analytics om uw rapporten en visualisaties te bouwen.

>[!NOTE]
>
> Deze handleiding voor snel starten is een vereenvoudigde gids voor het invoeren van gegevens die van uw site zijn verzameld in Adobe Experience Platform en voor gebruik in Customer Journey Analytics. Het wordt ten zeerste aanbevolen de aanvullende informatie te bestuderen wanneer deze wordt vermeld.


## Een schema en gegevensset instellen

Als u gegevens in Adobe Experience Platform wilt invoeren, moet u eerst definiëren welke gegevens u wilt verzamelen. Alle gegevens die in Adobe Experience Platform worden ingevoerd, moeten voldoen aan een standaard, gedenormaliseerde structuur, zodat deze kan worden herkend en kan worden toegepast door de mogelijkheden en functies op de downstreammarkt. Het Model van Gegevens van de ervaring (XDM) is het standaardkader dat deze structuur in de vorm van schema&#39;s verstrekt.

Zodra u een schema hebt bepaald, gebruikt u één of meerdere datasets om de inzameling van gegevens op te slaan en te beheren. Een dataset is een opslag en beheersconstructie voor een inzameling van gegevens (typisch een lijst) die een schema (kolommen) en gebieden (rijen) bevat.

Alle gegevens die in Adobe Experience Platform worden opgenomen moeten met een vooraf gedefinieerd schema in overeenstemming zijn alvorens het als dataset kan worden voortgeduurd.

### Een schema instellen

U wilt enkele minimale gegevens bijhouden van profielen die uw website bezoeken, zoals paginanaam, identificatie.
U moet eerst een schema definiëren dat deze gegevens modelleert.

Uw schema instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Schemas]** binnen [!UICONTROL DATA MANAGEMENT].

1. Selecteren **[!UICONTROL Create schema]**. .
1. In Uitgezocht een klassenstap van de Create schematovenaar:

   1. Selecteren **[!UICONTROL Experience Event]**.

      ![Een schema maken voor markeringsgebeurtenissen](./assets/create-ee-schema-wizard-step-1.png)

      >[!INFO]
      >
      >    Een schema van de Gebeurtenis van de Ervaring wordt gebruikt om het _gedrag_ van een profiel (zoals scènenaam, drukknop om aan winkelwagentje toe te voegen). Een afzonderlijk profielschema wordt gebruikt om het profiel te modelleren _attributes_ (zoals naam, e-mail, geslacht).

   1. Selecteren **[!UICONTROL Next]**.


1. In de [!UICONTROL Name and review step] van de [!UICONTROL Create schema] wizard:

   1. Voer een **[!UICONTROL Schema display name]** voor uw schema en (optioneel) a **[!UICONTROL Description]**.

      ![Schema-venster maken met de naam van de schemavelden](./assets/create-ee-schema-wizard-step-2.png)

   1. Selecteren **[!UICONTROL Finish]**.

1. Op het tabblad Structuur van het voorbeeldschema:

   1. Selecteren **[!UICONTROL + Add]** in [!UICONTROL Field groups].

      ![Veldgroep toevoegen](./assets/add-field-group-button.png)

      Veldgroepen zijn herbruikbare verzamelingen van objecten en kenmerken waarmee u het schema eenvoudig kunt uitbreiden.

   1. In de [!UICONTROL Add fields groups] selecteert u de **[!UICONTROL AEP Web SDK ExperienceEvent]** veldgroep in de lijst.

      ![AEP Web SDK ExperienceEvent-veldgroep](./assets/select-aepwebsdk-experienceevent.png)

      U kunt de voorvertoningsknop selecteren om een voorvertoning weer te geven van de velden die deel uitmaken van deze veldgroep, zoals `web > webPageDetails > name`.

      ![AEP Web SDK ExperienceEvent-veldgroepvoorbeeld](./assets/aepwebsdk-experiencevent-preview.png)

      Selecteren **[!UICONTROL Back]** om de voorvertoning te sluiten.

   1. Selecteren **[!UICONTROL Add field groups]**.

1. Selecteren **[!UICONTROL +]** naast de naam van het schema in het dialoogvenster [!UICONTROL Structure] deelvenster.

   ![Voorbeeld: Veld toevoegen, knop](./assets/example-schema-plus.png)

1. In de [!UICONTROL Field Properties] paneel, enter `Identification` als naam, **[!UICONTROL Identification]** als de [!UICONTROL Display name], selecteert u **[!UICONTROL Object]** als de [!UICONTROL Type] en selecteert u **[!UICONTROL ExperienceEvent Core v2.1]** als de [!UICONTROL Field Group].

   ![Identificatieobject](./assets/identification-field.png)

   Het identificatieobject voegt id-mogelijkheden toe aan uw schema. In uw geval wilt u profielen identificeren die uw site bezoeken met de Experience Cloud-id en het e-mailadres. Er zijn vele andere eigenschappen beschikbaar om de identificatie van uw persoon te volgen (bijvoorbeeld klant identiteitskaart, loyalty identiteitskaart).

   Selecteren **[!UICONTROL Apply]** om dit object aan uw schema toe te voegen.

1. Selecteer de **[!UICONTROL ecid]** veld in het identificatieobject dat u zojuist hebt toegevoegd, en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Primary Identity]** en **[!UICONTROL ECID]** van de [!UICONTROL Identity namespace] in het rechterdeelvenster.

   ![ECID opgeven als identiteit](./assets/specify-identity.png)

   U geeft de Experience Cloud Identity op als de primaire identiteit die de Adobe Experience Platform Identity-service kan gebruiken om het gedrag van profielen te combineren (aan te sluiten) met dezelfde ECID.

   Selecteren **[!UICONTROL Apply]**. U ziet dat er een vingerafdrukpictogram wordt weergegeven in het ecid-kenmerk.

1. Selecteer de **[!UICONTROL email]** veld in het identificatieobject dat u zojuist hebt toegevoegd, en selecteer **[!UICONTROL Identity]** en **[!UICONTROL Email]** van de [!UICONTROL Identity namespace] in de lijst [!UICONTROL Field Properties] deelvenster.

   ![E-mail opgeven als identiteit](./assets/specify-email-identity.png)

   U geeft het e-mailadres op als een andere identiteit die de Adobe Experience Platform Identity-service kan gebruiken om het gedrag van profielen te combineren (naaien).

   Selecteren **[!UICONTROL Apply]**. U ziet dat er een vingerafdrukpictogram wordt weergegeven in het e-mailkenmerk.

   Selecteren **[!UICONTROL Save]**.

1. Selecteer het basiselement van uw schema dat de naam van het schema toont, dan selecteer **[!UICONTROL Profile]** switch.

   U wordt gevraagd het schema in te schakelen voor het profiel. Zodra toegelaten, wanneer het gegeven in datasets wordt opgenomen die op dit schema worden gebaseerd, worden die gegevens samengevoegd in het Real-Time Profiel van de Klant.

   Zie [Het schema inschakelen voor gebruik in Real-Time Klantprofiel](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=en#profile) voor meer informatie .

   >[!IMPORTANT]
   >
   >    Nadat u een schema hebt opgeslagen dat is ingeschakeld voor profiel, kan het niet meer worden uitgeschakeld voor profiel.

   ![Schema voor profiel inschakelen](./assets/enable-for-profile.png)

1. Selecteren **[!UICONTROL Save]** om uw schema op te slaan.

U hebt een minimumschema gemaakt dat de gegevens modelleert die u van uw website kunt vastleggen. Met het schema kunnen profielen worden geïdentificeerd aan de hand van de identiteit en het e-mailadres van het Experience Cloud. Door het schema voor profiel in te schakelen, zorgt u ervoor dat gegevens die vanaf uw website zijn vastgelegd, worden toegevoegd aan het realtime-klantprofiel.

Naast gedragsgegevens kunt u ook profielkenmerkgegevens van uw site vastleggen (bijvoorbeeld gegevens over profielen die zijn geabonneerd op een nieuwsbrief).

Als u deze profielgegevens wilt vastleggen, doet u het volgende:

- Maak een schema op basis van de klasse Individueel profiel XDM.

- Voeg de het gebiedsgroep van de Kern van het Profiel v2 aan het schema toe.

- Voeg een identificatieobject toe op basis van de veldgroep Profile Core v2.

- Experience Cloud-id definiëren als primaire id en e-mailadres als id.

- Het schema inschakelen voor profiel

Zie [Schema&#39;s maken en bewerken in de gebruikersinterface](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html) voor meer informatie over het toevoegen en verwijderen van veldgroepen en afzonderlijke velden aan een schema.

### Een gegevensset instellen

Met uw schema, hebt u uw gegevensmodel bepaald. U moet nu de constructie bepalen om die gegevens op te slaan en te beheren, die door datasets wordt gedaan.

Uw gegevensset instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Datasets]** binnen [!UICONTROL DATA MANAGEMENT].

2. Selecteren **[!UICONTROL Create dataset]**.

   ![Gegevensset maken](./assets/create-dataset.png)

3. Selecteren **[!UICONTROL Create dataset from schema]**.

   ![Gegevensset maken van schema](./assets/create-dataset-from-schema.png)

4. Selecteer het eerder gemaakte schema en selecteer **[!UICONTROL Next]**.

5. Geef uw gegevensset een naam en (optioneel) geef een beschrijving op.

   ![Gegevensset naam](./assets/name-your-datatest.png)

6. Selecteren **[!UICONTROL Finish]**.

7. Selecteer de **[!UICONTROL Profile]** switch.

   U wordt ertoe aangezet om de dataset voor profiel toe te laten. Zodra toegelaten, verrijkt de dataset klantenprofielen in real time met zijn opgenomen gegevens.

   >[!IMPORTANT]
   >
   >    U kunt een dataset voor profiel slechts toelaten wanneer het schema, waaraan de dataset voldoet, ook voor profiel wordt toegelaten.

   ![Schema voor profiel inschakelen](./assets/aepwebsdk-dataset-profile.png)

Zie [UI-gids voor gegevensbestanden](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=nl) voor veel meer informatie over hoe te om, voorproef te bekijken, creeer, schrapt een dataset. En hoe te om een dataset voor het Profiel van de Klant in real time toe te laten.

## Een gegevensstroom instellen

Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web van Adobe Experience Platform en Mobiele SDKs. Bij het verzamelen van gegevens met de SDK&#39;s van Adobe Experience Platform worden gegevens verzonden naar het Adobe Experience Platform Edge Network. Het is de gegevensstroom die bepaalt aan welke diensten dat de gegevens door:sturen.

In uw opstelling, wilt u de gegevens die u van de website verzamelt worden verzonden naar uw dataset in Adobe Experience Platform.

Uw gegevensstroom instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform **[!UICONTROL Datastreams]** van [!UICONTROL DATA COLLECTION] in het linkerspoor.

2. Selecteren **[!UICONTROL New Datastream]**.

3. Geef een naam en beschrijf de gegevensstroom. Selecteer uw schema in het menu [!UICONTROL Event Schema] lijst.

   ![Nieuwe DataStream](./assets/new-datastream.png)

4. Selecteren **[!UICONTROL Save]**.

5. Selecteren **[!UICONTROL Add Service]**.

6. In de [!UICONTROL Add Service screen]:

   1. Selecteren **[!UICONTROL Adobe Experience Platform]** van de [!UICONTROL Service] lijst.

   2. Zorgen **[!UICONTROL Enabled]** is geselecteerd.

   3. Selecteer uw gegevensset in het menu [!UICONTROL Event Dataset] lijst.

      ![DataStream AEP-service](./assets/datastream-aep-service.png)

   4. Laat de andere instellingen staan en selecteer **[!UICONTROL Save]** om de gegevensstroom op te slaan.

Uw gegevensstroom is nu geconfigureerd om de gegevens die van uw website zijn verzameld door te sturen naar uw gegevensset in Adobe Experience Platform.

Zie [Overzicht gegevensstromen](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=en) voor meer informatie over hoe te om een gegevensstroom te vormen en hoe te om gevoelige gegevens te behandelen.



## Tags gebruiken

Als u code op uw site wilt implementeren om gegevens daadwerkelijk te verzamelen, gebruikt u de functie Codes in Adobe Experience Platform. Met deze oplossing voor tagbeheer kunt u code naast andere coderingsvereisten implementeren. Tags bieden naadloze integratie met Adobe Experience Platform via de Adobe Experience Platform Web SDK-extensie.

### Uw tag maken

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Tags]** binnen [!UICONTROL DATA COLLECTION].

2. Selecteren **[!UICONTROL New Property]**.

   Geef de tag een naam, selecteer **[!UICONTROL Web]** en voert u een domeinnaam in. Selecteren **[!UICONTROL Save]** om door te gaan.

   ![Een eigenschap maken](./assets/create-property.png)

### Uw tag configureren

Nadat u de tag hebt gemaakt, moet u deze configureren met de juiste extensies en gegevenselementen en -regels configureren op basis van de manier waarop u uw site wilt bijhouden en gegevens naar Adobe Experience Platform wilt verzenden.

Selecteer de nieuwe tag in de lijst met [!UICONTROL Tag Properties] om het te openen.


#### **Extensies**

Om ervoor te zorgen dat u gegevens naar Adobe Experience Platform kunt verzenden (via uw gegevensstroom), voegt u de extensie Web SDK van het platform Adobe toe aan uw tag.

U kunt als volgt de extensie Adobe Experience Platform Web SDK maken en configureren:

1. Selecteren **[!UICONTROL Extensions]** in het linkerspoor.

2. Selecteren **[!UICONTROL Catalog]** in de bovenste balk.

3. Zoeken naar of schuiven naar de extensie Adobe Experience Platform Web SDK en Selecteren **[!UICONTROL Install]** om het te installeren.

   <img src="./assets/aepwebsdk-extension.png" width="35%"/>

4. Selecteer uw sandbox en uw eerder gemaakte datastream voor uw [!UICONTROL Production Environment] en (optioneel) [!UICONTROL Staging Environment] en [!UICONTROL Development Environment].

   ![AEP Web SDK-extensieconfiguratie](./assets/aepwebsk-extension-datastreams.png)

   Selecteren **[!UICONTROL Save]**.

Zie [De extensie Adobe Experience Platform Web SDK configureren](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html) voor meer informatie .

U wilt ook opstelling de uitbreiding van de Dienst van identiteitskaart van het Experience Cloud zodat kunt u Experience Cloud ID gemakkelijk gebruiken. De Experience Cloud ID Service identificeert personen in alle Adobe Experience Cloud-oplossingen.

Om de uitbreiding van de Dienst van identiteitskaart van het Experience Cloud te creëren en te vormen:

1. Selecteren **[!UICONTROL Extensions]** in het linkerspoor.

2. Selecteren **[!UICONTROL Catalog]** in de bovenste balk.

3. Zoek naar of rol aan de uitbreiding van de Dienst van identiteitskaart van het Experience Cloud **[!UICONTROL Install]** om het te installeren.

   <img src="./assets/ecid-extension.png" width="35%"/>

4. Laat alle configuraties standaard staan.

5. Selecteren **[!UICONTROL Save]**.

#### **Gegevenselementen**

Gegevenselementen zijn de bouwstenen voor uw gegevenswoordenboek (of gegevenskaart). Gebruik gegevenselementen om gegevens te verzamelen, te organiseren en te leveren over marketing- en advertentietechnologie. U stelt gegevenselementen in uw tag in die worden gelezen van uw gegevenslaag en die kunnen worden gebruikt om gegevens naar Adobe Experience Platform te verzenden.

Er zijn verschillende typen gegevenselementen. U stelt eerst een gegevenselement in om de paginanaam vast te leggen die personen op uw site bekijken.

Een gegevenselement voor de paginanaam definiëren:

1. Selecteren **[!UICONTROL Data Elements]** in het linkerspoor.

2. Selecteren **[!UICONTROL Add Data Element]**.

3. In de [!UICONTROL Create Data Element] dialoogvenster:

   - Geef uw gegevenselement bijvoorbeeld een naam `Page Name`.

   - Selecteren **[!UICONTROL Core]** van de [!UICONTROL Extension] lijst.

   - Selecteren **[!UICONTROL Page Info]** van de [!UICONTROL Data Element Type] lijst.

   - Selecteren **[!UICONTROL Title]** van de [!UICONTROL Attribute] lijst.

     ![Datumelement maken met behulp van pagina-info](./assets/create-dataelement-1.png)

     U had de waarde van bijvoorbeeld een variabele in uw gegevenslaag kunnen gebruiken `pageName` en de [!UICONTROL JavaScript Variable] het elementtype van gegevens om het gegevenselement te bepalen.

     ![Gegevenselement maken met JavaScript-variabele](./assets/create-dataelement-2.png)

   - Selecteren **[!UICONTROL Save]**.

U wilt nu opstelling een gegevenselement van verwijzingen voorzien van Experience Cloud identiteitskaart die automatisch door het Web SDK van Adobe Experience Platform en beschikbaar door de uitbreiding van de Dienst van identiteitskaart van het Experience Cloud wordt verstrekt.

Een ECID-gegevenselement definiëren:

1. Selecteren **[!UICONTROL Data Elements]** in het linkerspoor.

2. Selecteren **[!UICONTROL Add Data Element]**.

3. In de [!UICONTROL Create Data Element] dialoogvenster:

   - Geef uw gegevenselement bijvoorbeeld een naam `ECID`.

   - Selecteren **[!UICONTROL Experience Cloud ID Service]** van de [!UICONTROL Extension] lijst.

   - Selecteren **[!UICONTROL ECID]** van de [!UICONTROL Data Element Type] lijst.

     ![ECID-gegevenselement](./assets/ecid-dataelement.png)

   - Selecteren **[!UICONTROL Save]**.

Tot slot wilt u nu om het even welke specifieke gegevenselementen aan het schema in kaart brengen u vroeger bepaalde. U definieert een ander gegevenselement dat een representatie van uw XDM-schema biedt.

Een XDM-objectelement definiëren:

1. Selecteren **[!UICONTROL Data Elements]** in het linkerspoor.

2. Selecteren **[!UICONTROL Add Data Element]**.

3. In de [!UICONTROL Create Data Element] dialoogvenster:

   - Geef uw gegevenselement bijvoorbeeld een naam `XDM - Page View`.

   - Selecteren **[!UICONTROL Adobe Experience Platform Web SDK]** van de [!UICONTROL Extension] lijst.

   - Selecteren **[!UICONTROL XDM Object]** van de [!UICONTROL Data Element Type] lijst.

   - Selecteer de sandbox in het menu [!UICONTROL Sandbox] lijst.

   - Selecteer uw schema in het menu [!UICONTROL Schema] lijst.

   - Wijs de `identification > core > ecid` -kenmerk, gedefinieerd in uw schema, aan het ECID-gegevenselement. Selecteer het cilinderpictogram om het ECID-gegevenselement gemakkelijk te kiezen in de lijst met gegevenselementen.

     ![ECID-gegevenselement kiezen](./assets/pick-ecid-dataelement.png)

     ![ECID-gegevenselement toewijzen](./assets/map-ecid.png)


   - Wijs de `web > webPageDetails > name` -kenmerk, gedefinieerd in uw schema, aan het gegevenselement Paginanaam.

     ![Gegevenselement paginanaam toewijzen](./assets/map-pagename.png)

   - Selecteren **[!UICONTROL Save]**.


#### **Regels**

Tags in Adobe Experience Platform volgen een op regels gebaseerd systeem. Zij zoeken gebruikersinteractie en bijbehorende gegevens. Wanneer aan de criteria die in uw regels worden geschetst wordt voldaan, teweegbrengt de regel de uitbreiding, het manuscript, of cliënt-zijcode in werking u identificeerde. U kunt regels gebruiken om gegevens (zoals een voorwerp XDM) naar Adobe Experience Platform te verzenden gebruikend de uitbreiding van SDK van het Web van Adobe Experience Platform.

Een regel definiëren:

1. Selecteren **[!UICONTROL Rules]** in het linkerspoor.

2. Selecteren **[!UICONTROL Create New Rule]**.

3. In de [!UICONTROL Create Rule] dialoogvenster:

   - Geef de regel een naam, bijvoorbeeld `Page View`.

   - Selecteren **[!UICONTROL + Add]** ondergronds [!UICONTROL Events].

   - In de [!UICONTROL Event Configuration] dialoogvenster:

      - Selecteren **[!UICONTROL Core]** van de [!UICONTROL Extension] lijst.

      - Selecteren **[!UICONTROL Window Loaded]** van de [!UICONTROL Event Type] lijst.

        ![Regel - Gebeurtenisconfiguratie](./assets/event-windowloaded-pageview.png)

      - Selecteren **[!UICONTROL Keep Changes]**.



   - Selecteren **[!UICONTROL + Add]** ondergronds [!UICONTROL Actions].

   - In de [!UICONTROL Action Configuration] dialoogvenster:

      - Selecteren **[!UICONTROL Adobe Experience Platform Web SDK]** van de [!UICONTROL Extension] lijst.

      - Selecteren **[!UICONTROL Send Event]** van de [!UICONTROL Action Type] lijst.

      - Selecteren **[!UICONTROL web.webpagedetails.pageViews]** van de [!UICONTROL Type] lijst.

      - Selecteer het cilinderpictogram naast  [!UICONTROL XDM data] en selecteer **[!UICONTROL XDM - Page View]** in de lijst met gegevenselementen.

     ![Regel - Configuratie van handelingen](./assets/action-pageview-xdm.png)

      - Selecteren **[!UICONTROL Keep Changes]**.

   - Uw regel moet er als volgt uitzien:

     ![Regel maken](assets/rule-pageview.png)

   - Selecteren **[!UICONTROL Save]**.

Het bovenstaande is slechts een voorbeeld van het definiëren van een regel die XDM-gegevens met waarden uit andere gegevenselementen naar Adobe Experience Platform verzendt.

U kunt regels op verschillende manieren in uw tag gebruiken om variabelen te bewerken (met behulp van uw gegevenselementen).

Zie [Regels](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html) voor meer informatie .

### Uw tag maken en publiceren

Nadat u gegevenselementen en regels hebt gedefinieerd, moet u de tag maken en publiceren. Wanneer u een bibliotheek maakt, moet u deze toewijzen aan een omgeving. De uitbreidingen, de regels, en de gegevenselementen van de bouwstijl worden dan gecompileerd en in het toegewezen milieu geplaatst. Elke omgeving bevat een unieke insluitcode waarmee u de toegewezen build in uw site kunt integreren.

Om uw markering te bouwen en te publiceren:

1. Selecteren **[!UICONTROL Publishing Flow]** van de linkerspoorstaaf.

2. Selecteren **[!UICONTROL Select a working library]**, gevolgd door **[!UICONTROL Add Library…]**.

3. In de [!UICONTROL Create Library] dialoogvenster:

   - Geef de bibliotheek een naam.

   - Selecteren **[!UICONTROL Development (development)]** van de [!UICONTROL Environment] lijst.

   - Selecteren **[!UICONTROL + Add All Changed Resources]**.

     ![Publiceren - Bibliotheek maken](./assets/create-library-aep.png)

   - Selecteren **[!UICONTROL Save & Build to Development]**.

   Uw tag wordt opgeslagen en gebouwd voor uw ontwikkelomgeving. Een groene stip geeft aan dat uw tag met succes is opgebouwd in uw ontwikkelomgeving.

4. U kunt **[!UICONTROL ...]** om de bibliotheek opnieuw op te bouwen of de bibliotheek naar een testomgeving of productieomgeving te verplaatsen.

   ![Publiceren - Bibliotheek maken](./assets/build-library.png)

Adobe Experience Platform-tags ondersteunen eenvoudige tot complexe publicatieworkflows die geschikt zijn voor uw implementatie van de Adobe Experience Platform Web SDK.

Zie [Overzicht van publicatie](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html) voor meer informatie .


### De tagcode ophalen

Tot slot moet u de tag installeren op de website die u wilt bijhouden. Dit houdt in dat code in de kopteksttag van de sjabloon van uw website wordt geplaatst.

De code ophalen die naar de tag verwijst:

1. Selecteren **[!UICONTROL Environments]** in het linkerspoor.

2. Selecteer de juiste installatieknop in de lijst met omgevingen.

   In de [!UICONTROL Web Install Instructions] selecteert u de knop Kopiëren naast de scriptcode die als volgt moet worden gelezen:

   ```
   <script src="https://assets.adobedtm.com/2a518741ab24/.../launch-...-development.min.js" async></script>>
   ```

   ![Omgeving](./assets/environment.png)

3. Selecteren **[!UICONTROL Close]**.

In plaats van de code voor het ontwikkelmilieu, zou u een ander milieu (het opvoeren, productie) kunnen selecteren die op waar wordt gebaseerd u in het opstellen van het Web SDK van Adobe Experience Platform bent.

Zie [Omgevingen](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html?) voor meer informatie .

## Implementeren en valideren

U kunt de code nu implementeren in de ontwikkelingsversie van uw website in het dialoogvenster `<head>` -tag. Wanneer uw website wordt geïmplementeerd, worden gegevens verzameld in Adobe Experience Platform.

Valideer uw implementatie, verbeter het waar nodig, en zodra correct, stel het in uw het opvoeren en productiemilieu gebruikend de het publiceren werkschemafunctie van Markeringen op.

## Een verbinding instellen

Om de gegevens van Adobe Experience Platform in Customer Journey Analytics te gebruiken, creeert u een verbinding die de gegevens omvat die uit vestiging uw schema, dataset, en werkschema voortvloeien.

Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over deze datasets te rapporteren, moet u eerst een verband tussen datasets in Adobe Experience Platform en Werkruimte vestigen.

Om uw verbinding tot stand te brengen:

1. Selecteer in de gebruikersinterface van de Customer Journey Analytics de optie **[!UICONTROL Connections]** in de bovenste navigatie.

2. Selecteren **[!UICONTROL Create new connection]**.

3. In de [!UICONTROL Untitled connection] scherm:

   Geef een naam en beschrijf de verbinding in [!UICONTROL Connection Settings].

   Selecteer de juiste sandbox in het menu [!UICONTROL Sandbox] lijst in [!UICONTROL Data settings] en selecteert u het aantal dagelijkse gebeurtenissen in het menu [!UICONTROL Average number of daily events] lijst.

   ![Verbindingsinstellingen](./assets/cja-connections-1.png)

   Selecteren **[!UICONTROL Add datasets]**.

   In de [!UICONTROL Select datasets] stap in [!UICONTROL Add datasets]:

   - Selecteer de gegevensset die u eerder hebt gemaakt (`Example dataset`) en een andere gegevensset die u wilt opnemen in de verbinding.

     ![Gegevenssets toevoegen](./assets/cja-connections-2b.png)

   - Selecteren **[!UICONTROL Next]**.

   In de [!UICONTROL Datasets settings] stap in [!UICONTROL Add datasets]:

   - Voor elke gegevensset:

      - Selecteer een [!UICONTROL Person ID] uit de beschikbare identiteiten die zijn gedefinieerd in de gegevenssetschema&#39;s in Adobe Experience Platform.

      - Selecteer de juiste gegevensbron in het menu [!UICONTROL Data source type] lijst. Als u **[!UICONTROL Other]** Voeg vervolgens een beschrijving voor uw gegevensbron toe.

      - Set **[!UICONTROL Import all new data]** en **[!UICONTROL Dataset backfill existing data]** volgens uw voorkeuren.

     ![Gegevenssets configureren](./assets/cja-connections-3b.png)

   - Selecteren **[!UICONTROL Add datasets]**.

   Selecteren **[!UICONTROL Save]**.

Zie [Overzicht van verbindingen](../connections/overview.md) voor meer informatie over om een verbinding tot stand te brengen en te beheren en datasets te selecteren en te combineren.

## Een gegevensweergave instellen

Een gegevensmening is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van een verbinding te interpreteren. Hiermee worden alle afmetingen en metriek opgegeven die beschikbaar zijn in Analysis Workspace en de kolommen waarvan die dimensies en metriek hun gegevens verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

Uw gegevensweergave maken:

1. Selecteer in de gebruikersinterface van de Customer Journey Analytics de optie **[!UICONTROL Data views]** in de bovenste navigatie.

2. Selecteren **[!UICONTROL Create new data view]**.

3. In de [!UICONTROL Configure] stap:

   Selecteer uw verbinding van [!UICONTROL Connection] lijst.

   Naam en (optioneel) beschrijf uw verbinding.

   ![Gegevensweergave configureren](./assets/cja-dataview-1.png)

   Selecteren **[!UICONTROL Save and continue]**.

4. In de [!UICONTROL Components] stap:

   Voeg schemagebieden en/of standaardcomponent toe die u aan wilt omvatten [!UICONTROL METRICS] of [!UICONTROL DIMENSIONS] deelvakken.

   ![Componenten van gegevensweergave](./assets/cja-dataview-2.png)

   Selecteren **[!UICONTROL Save and continue]**.

5. In de [!UICONTROL Settings] stap:

   ![Instellingen voor gegevensweergave](./assets/cja-dataview-3.png)

   De instellingen ongewijzigd laten en selecteren **[!UICONTROL Save and finish]**.

Zie [Overzicht van gegevensweergaven](../data-views/data-views.md) voor meer informatie over het maken en bewerken van een gegevensweergave, welke componenten beschikbaar zijn voor u in de gegevensweergave en hoe u filter- en sessieinstellingen kunt gebruiken.


## Een project instellen

Analysis Workspace is een flexibel browserprogramma waarmee u snel analyses kunt maken en inzichten kunt delen op basis van uw gegevens. U gebruikt de projecten van de Werkruimte om gegevenscomponenten, lijsten, en visualisaties te combineren om uw analyse te bundelen en met iedereen in uw organisatie te delen.

Uw project maken:

1. Selecteer in de gebruikersinterface van de Customer Journey Analytics de optie **[!UICONTROL Projects]** in de bovenste navigatie.

2. Selecteren **[!UICONTROL Projects]** in de linkernavigatie.

3. Selecteren **[!UICONTROL Create project]**.

   ![Werkruimteproject](./assets/cja-projects-1.png)

   Selecteren **[!UICONTROL Blank project]**.

   ![Werkruimte - Leeg project](./assets/cja-projects-2.png)

4. Selecteer de gegevensweergave in de lijst.

   ![Werkruimte selecteren, gegevensweergave](./assets/cja-projects-3.png).

5. Als u uw eerste rapport wilt maken, sleept u de afmetingen en metriek naar het [!UICONTROL Freeform table] in de [!UICONTROL Panel]. Als voorbeeld sleept u `Program Points Balance` en `Page View` als metriek en `email` als dimensie voor een snel overzicht van profielen die uw website hebben bezocht en deel uitmaken van het loyaliteitsprogramma dat loyaliteitspunten verzamelt.

   ![Werkruimte - Eerste rapport](./assets/cja-projects-5.png)

Zie [Analysis Workspace-overzicht](../analysis-workspace/home.md) voor meer informatie over hoe te om projecten tot stand te brengen en uw analyse te bouwen gebruikend componenten, visualisaties, en panelen.

>[!SUCCESS]
>
>U hebt alle stappen uitgevoerd. Eerst definieert u welke gegevens u wilt verzamelen (schema) en waar u deze wilt opslaan (dataset) in Adobe Experience Platform. Vervolgens hebt u een gegevensstroom geconfigureerd in het Edge Network om ervoor te zorgen dat gegevens naar die gegevensset kunnen worden doorgestuurd. Vervolgens hebt u de tag gedefinieerd en geïmplementeerd die de extensies (Adobe Experience Platform Web SDK, Experience Cloud ID Service), gegevenselementen en regels bevat voor het vastleggen van gegevens van uw website en het verzenden van die gegevens naar uw gegevensstroom. U hebt een verbinding in Customer Journey Analytics gedefinieerd om uw website-volggegevens en andere gegevens te gebruiken. Met de definitie van uw gegevensweergave kunt u opgeven welke dimensie en metriek u wilt gebruiken en ten slotte hebt u uw eerste project gemaakt waarin uw gegevens worden gevisualiseerd en geanalyseerd.
