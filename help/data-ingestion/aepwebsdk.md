---
title: Gegevens invoeren via de Adobe Experience Platform Web SDK
description: Verklaar hoe te om gegevens in Customer Journey Analytics via het Web SDK van Adobe Experience Platform en de Edge Network in te voeren
solution: Customer Journey Analytics
feature: Basics
exl-id: 0b595e9e-0dcf-4c70-ac6d-5a2322824328
role: Admin
source-git-commit: 90d1c51c11f0ab4d7d61b8e115efa8257a985446
workflow-type: tm+mt
source-wordcount: '3218'
ht-degree: 0%

---

# Gegevens verzamelen via de SDK van het web

In deze handleiding voor snel starten wordt uitgelegd hoe u gegevens voor het bijhouden van websites rechtstreeks in Adobe Experience Platform kunt invoeren met de Adobe Experience Platform Web SDK en Edge Network en deze gegevens vervolgens in Customer Journey Analytics kunt gebruiken.

Hiervoor moet u:

- **opstelling een schema en dataset** in Adobe Experience Platform om het model (schema) van de gegevens te bepalen die u wilt verzamelen en waar te om de gegevens (dataset) eigenlijk te verzamelen.

- **opstelling een datastream** om de Edge Network van Adobe Experience Platform te vormen om uw verzamelde gegevens aan de dataset te leiden u in Adobe Experience Platform vormde.

- **Markeringen van het Gebruik** om regels en gegevenselementen tegen de gegevens in uw gegevenslaag op uw website gemakkelijk te vormen. Dan zorg ervoor dat het gegeven wordt verzonden naar de datastream die op de Edge Network van Adobe Experience Platform wordt gevormd.

- **stelt en bevestigt** op. Zorg voor een omgeving waarin u de ontwikkeling van tags kunt doorlopen en publiceer deze live in uw productieomgeving als alles is gevalideerd.

- **opstelling een verbinding** in Customer Journey Analytics. Deze verbinding zou (minstens) uw dataset van Adobe Experience Platform moeten omvatten.

- **opstelling een gegevensmening** in Customer Journey Analytics om metriek en afmeting te bepalen die u in Analysis Workspace wilt gebruiken.

- **opstelling een project** in Customer Journey Analytics om uw rapporten en visualisaties te bouwen.

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

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Schemas]** within [!UICONTROL DATA MANAGEMENT] in het linkerspoor.

1. Selecteer **[!UICONTROL Create schema]** .
.
1. In Uitgezocht een klassenstap van de Create schematovenaar:

   1. Selecteer **[!UICONTROL Experience Event]** .

      ![ creeer een schema dat de Gebeurtenis van de Ervaring benadrukt ](./assets/create-ee-schema-wizard-step-1.png)

      >[!INFO]
      >
      >    Een schema van de Gebeurtenis van de Ervaring wordt gebruikt om het _gedrag_ van een profiel (als scènenaam, drukknop te modelleren om aan wagentje toe te voegen). Een individueel schema van het Profiel wordt gebruikt om de profiel _attributen_ (zoals naam, e-mail, geslacht) te modelleren.

   1. Selecteer **[!UICONTROL Next]** .


1. In het gedeelte [!UICONTROL Name and review step] van de wizard [!UICONTROL Create schema] :

   1. Voer een **[!UICONTROL Schema display name]** in voor uw schema en (optioneel) een **[!UICONTROL Description]** .

      ![ creeer schemavenster dat de Naam toont uw schemagebieden ](./assets/create-ee-schema-wizard-step-2.png)

   1. Selecteer **[!UICONTROL Finish]** .

1. Op het tabblad Structuur van het voorbeeldschema:

   1. Selecteer **[!UICONTROL + Add]** in [!UICONTROL Field groups] .

      ![ voeg gebiedsgroep ](./assets/add-field-group-button.png) toe

      Veldgroepen zijn herbruikbare verzamelingen van objecten en kenmerken waarmee u het schema eenvoudig kunt uitbreiden.

   1. Selecteer in het dialoogvenster [!UICONTROL Add fields groups] de veldgroep **[!UICONTROL AEP Web SDK ExperienceEvent]** in de lijst.

      ![ AEP Web SDK ExperienceEvent gebiedsgroep ](./assets/select-aepwebsdk-experienceevent.png)

      U kunt de voorvertoningsknop selecteren om een voorvertoning weer te geven van de velden die deel uitmaken van deze veldgroep, bijvoorbeeld `web > webPageDetails > name` .

      ![ AEP Web SDK ExperienceEvent gebiedsgroepvoorproef ](./assets/aepwebsdk-experiencevent-preview.png)

      Selecteer **[!UICONTROL Back]** om de voorvertoning te sluiten.

   1. Selecteer **[!UICONTROL Add field groups]** .

1. Selecteer **[!UICONTROL +]** naast de naam van het schema in het deelvenster [!UICONTROL Structure] .

   ![ het Schema van het Voorbeeld voegt de knoop van het Gebied toe ](./assets/example-schema-plus.png)

1. Typ in het deelvenster [!UICONTROL Field Properties] `Identification` als de naam, **[!UICONTROL Identification]** als de [!UICONTROL Display name] , selecteer **[!UICONTROL Object]** als de [!UICONTROL Type] en selecteer **[!UICONTROL ExperienceEvent Core v2.1]** als de [!UICONTROL Field Group] .

   >[!NOTE]
   >
   >Als die veldgroep niet beschikbaar is, zoekt u naar een andere veldgroep met identiteitsvelden. Of [ creeer een nieuwe gebiedsgroep ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/field-groups.html) en [ voeg nieuwe identiteitsgebieden ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/fields/identity.html#define-a-identity-field) (als `ecid`, `crmId`, en anderen toe u) aan de gebiedsgroep nodig hebt en selecteer die nieuwe gebiedsgroep.

   ![ Voorwerp van de Identificatie ](./assets/identification-field.png)

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

1. Selecteer het hoofdelement van het schema met de naam van het schema en selecteer vervolgens de **[!UICONTROL Profile]** switch.

   U wordt gevraagd het schema in te schakelen voor het profiel. Zodra toegelaten, wanneer het gegeven in datasets wordt opgenomen die op dit schema worden gebaseerd, worden die gegevens samengevoegd in het Real-Time Profiel van de Klant.

   Zie [ het schema voor gebruik in het Profiel van de Klant in real time ](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#profile) voor meer informatie toelaten.

   >[!IMPORTANT]
   >
   >    Nadat u een schema hebt opgeslagen dat is ingeschakeld voor profiel, kan het niet meer worden uitgeschakeld voor profiel.

   ![ laat schema voor profiel ](./assets/enable-for-profile.png) toe

1. Selecteer **[!UICONTROL Save]** om het schema op te slaan.

U hebt een minimumschema gemaakt dat de gegevens modelleert die u van uw website kunt vastleggen. Met het schema kunnen profielen worden geïdentificeerd aan de hand van de identiteit en het e-mailadres van het Experience Cloud. Door het schema voor profiel in te schakelen, zorgt u ervoor dat gegevens die vanaf uw website zijn vastgelegd, worden toegevoegd aan het realtime-klantprofiel.

Naast gedragsgegevens kunt u ook profielkenmerkgegevens van uw site vastleggen (bijvoorbeeld gegevens over profielen die zijn geabonneerd op een nieuwsbrief).

Als u deze profielgegevens wilt vastleggen, doet u het volgende:

- Maak een schema op basis van de klasse Individueel profiel XDM.

- Voeg de het gebiedsgroep van de Kern van het Profiel v2 aan het schema toe.

- Voeg een identificatieobject toe op basis van de veldgroep Profile Core v2.

- Experience Cloud-id definiëren als primaire id en e-mailadres als id.

- Het schema inschakelen voor profiel

Zie [ schema&#39;s in UI ](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html) voor meer informatie creëren en uitgeven bij het toevoegen van en het verwijderen van gebiedsgroepen en individuele gebieden aan een schema.

### Een gegevensset instellen

Met uw schema, hebt u uw gegevensmodel bepaald. U moet nu de constructie bepalen om die gegevens op te slaan en te beheren, die door datasets wordt gedaan.

Uw gegevensset instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Datasets]** within [!UICONTROL DATA MANAGEMENT] in het linkerspoor.

2. Selecteer **[!UICONTROL Create dataset]** .

   ![ creeer dataset ](./assets/create-dataset.png)

3. Selecteer **[!UICONTROL Create dataset from schema]** .

   ![ creeer dataset van schema ](./assets/create-dataset-from-schema.png)

4. Selecteer het schema dat u eerder hebt gemaakt en selecteer **[!UICONTROL Next]** .

5. Geef uw gegevensset een naam en (optioneel) geef een beschrijving op.

   ![ dataset van de Naam ](./assets/name-your-datatest.png)

6. Selecteer **[!UICONTROL Finish]** .

7. Selecteer de **[!UICONTROL Profile]** schakelaar.

   U wordt ertoe aangezet om de dataset voor profiel toe te laten. Zodra toegelaten, verrijkt de dataset klantenprofielen in real time met zijn opgenomen gegevens.

   >[!IMPORTANT]
   >
   >    U kunt een dataset voor profiel slechts toelaten wanneer het schema, waaraan de dataset voldoet, ook voor profiel wordt toegelaten.

   ![ laat schema voor profiel ](./assets/aepwebsdk-dataset-profile.png) toe

Zie {de gids UI van de Datasets van 0} ](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=nl) voor veel meer informatie over hoe te bekijken, voorproef, tot stand brengen, een dataset schrappen. [ En hoe te om een dataset voor het Profiel van de Klant in real time toe te laten.

## Een gegevensstroom instellen

Een gegevensstroom vertegenwoordigt de server-zijconfiguratie wanneer het uitvoeren van het Web van Adobe Experience Platform en Mobiele SDKs. Bij het verzamelen van gegevens met de SDK&#39;s van Adobe Experience Platform worden gegevens naar de Adobe Experience Platform-Edge Network verzonden. Het is de gegevensstroom die bepaalt aan welke diensten dat de gegevens door:sturen.

In uw opstelling, wilt u de gegevens die u van de website verzamelt worden verzonden naar uw dataset in Adobe Experience Platform.

Uw gegevensstroom instellen:

1. Selecteer in de gebruikersinterface van Adobe Experience Platform **[!UICONTROL Datastreams]** in [!UICONTROL DATA COLLECTION] in de linkertrack.

2. Selecteer **[!UICONTROL New Datastream]** .

3. Geef een naam en beschrijf de gegevensstroom. Selecteer het schema in de lijst [!UICONTROL Event Schema] .

   ![ Nieuwe DataStream ](./assets/new-datastream.png)

4. Selecteer **[!UICONTROL Save]** .

5. Selecteer **[!UICONTROL Add Service]** .

6. In de lus [!UICONTROL Add Service screen] :

   1. Selecteer **[!UICONTROL Adobe Experience Platform]** in de lijst [!UICONTROL Service] .

   2. Zorg ervoor dat **[!UICONTROL Enabled]** is geselecteerd.

   3. Selecteer de gegevensset in de lijst [!UICONTROL Event Dataset] .

      ![ datastream AEP dienst ](./assets/datastream-aep-service.png)

   4. Laat de andere instellingen staan en selecteer **[!UICONTROL Save]** om de gegevensstroom op te slaan.

Uw gegevensstroom is nu geconfigureerd om de gegevens die van uw website zijn verzameld door te sturen naar uw gegevensset in Adobe Experience Platform.

Zie [ Overzicht van gegevensstromen ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html) voor meer informatie over hoe te om een gegevensstroom te vormen en hoe te om gevoelige gegevens te behandelen.



## Tags gebruiken

Als u code op uw site wilt implementeren om gegevens daadwerkelijk te verzamelen, gebruikt u de functie Codes in Adobe Experience Platform. Met deze oplossing voor tagbeheer kunt u code naast andere coderingsvereisten implementeren. Tags bieden naadloze integratie met Adobe Experience Platform via de Adobe Experience Platform Web SDK-extensie.

### Uw tag maken

1. Selecteer in de gebruikersinterface van Adobe Experience Platform de optie **[!UICONTROL Tags]** within [!UICONTROL DATA COLLECTION] in het linkerspoor.

2. Selecteer **[!UICONTROL New Property]** .

   Geef de tag een naam, selecteer **[!UICONTROL Web]** en voer een domeinnaam in. Selecteer **[!UICONTROL Save]** om door te gaan.

   ![ creeer een bezit ](./assets/create-property.png)

### Uw tag configureren

Nadat u de tag hebt gemaakt, moet u deze configureren met de juiste extensies en gegevenselementen en -regels configureren op basis van de manier waarop u uw site wilt bijhouden en gegevens naar Adobe Experience Platform wilt verzenden.

Selecteer de nieuwe tag in de lijst met [!UICONTROL Tag Properties] om deze te openen.


#### **Uitbreidingen**

Om ervoor te zorgen dat u gegevens naar Adobe Experience Platform kunt verzenden (via uw gegevensstroom), voegt u de extensie Web SDK van het platform Adobe toe aan uw tag.

U kunt als volgt de extensie Adobe Experience Platform Web SDK maken en configureren:

1. Selecteer **[!UICONTROL Extensions]** in het linkerspoor.

2. Selecteer **[!UICONTROL Catalog]** in de bovenste balk.

3. Zoek naar of blader naar de extensie van Adobe Experience Platform Web SDK en selecteer **[!UICONTROL Install]** om de extensie te installeren.

   <img src="./assets/aepwebsdk-extension.png" width="35%"/>

4. Selecteer de sandbox en de eerder gemaakte gegevensstroom voor de [!UICONTROL Production Environment] en (optioneel) [!UICONTROL Staging Environment] en [!UICONTROL Development Environment] .

   ![ de uitbreidingsconfiguratie van SDK van het Web AEP ](./assets/aepwebsk-extension-datastreams.png)

   Selecteer **[!UICONTROL Save]** .

Zie [ de uitbreiding van SDK van het Web van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html) voor meer informatie vormen.

De SDK van het Web omvat [!UICONTROL Adobe Experience Cloud ID Service] native, zodat te hoeven u niet om de de dienstuitbreiding van identiteitskaart aan uw markering toe te voegen.

#### **Elementen van Gegevens**

Gegevenselementen zijn de bouwstenen voor uw gegevenswoordenboek (of gegevenskaart). Gebruik gegevenselementen om gegevens te verzamelen, te organiseren en te leveren over marketing- en advertentietechnologie. U stelt gegevenselementen in uw tag in die worden gelezen van uw gegevenslaag en die kunnen worden gebruikt om gegevens naar Adobe Experience Platform te verzenden.

Er zijn verschillende typen gegevenselementen. U stelt eerst een gegevenselement in om de paginanaam vast te leggen die personen op uw site bekijken.

Een gegevenselement voor de paginanaam definiëren:

1. Selecteer **[!UICONTROL Data Elements]** in het linkerspoor.

2. Selecteer **[!UICONTROL Add Data Element]** .

3. In het dialoogvenster [!UICONTROL Create Data Element] :

   - Geef uw gegevenselement een naam, bijvoorbeeld `Page Name` .

   - Selecteer **[!UICONTROL Core]** in de lijst [!UICONTROL Extension] .

   - Selecteer **[!UICONTROL Page Info]** in de lijst [!UICONTROL Data Element Type] .

   - Selecteer **[!UICONTROL Title]** in de lijst [!UICONTROL Attribute] .

     ![ creeer het Element van de Datum gebruikend Info van de Pagina ](./assets/create-dataelement-1.png)

     U had ook de waarde van een variabele in uw gegevenslaag kunnen gebruiken, bijvoorbeeld `pageName` en het gegevenstype [!UICONTROL JavaScript Variable] voor gegevenselementen om het gegevenselement te definiëren.

     ![ creeer het Element van Gegevens gebruikend Variabele JavaScript ](./assets/create-dataelement-2.png)

   - Selecteer **[!UICONTROL Save]** .

U wilt nu opstelling een gegevenselement van verwijzingen voorzien van Experience Cloud identiteitskaart die automatisch door het Web SDK van Adobe Experience Platform en beschikbaar door de uitbreiding van de Dienst van identiteitskaart van het Experience Cloud wordt verstrekt.

Een ECID-gegevenselement definiëren:

1. Selecteer **[!UICONTROL Data Elements]** in het linkerspoor.

2. Selecteer **[!UICONTROL Add Data Element]** .

3. In het dialoogvenster [!UICONTROL Create Data Element] :

   - Geef uw gegevenselement een naam, bijvoorbeeld `ECID` .

   - Selecteer **[!UICONTROL Experience Cloud ID Service]** in de lijst [!UICONTROL Extension] .

   - Selecteer **[!UICONTROL ECID]** in de lijst [!UICONTROL Data Element Type] .

     ![ ECID het Element van Gegevens ](./assets/ecid-dataelement.png)

   - Selecteer **[!UICONTROL Save]** .

Tot slot wilt u nu om het even welke specifieke gegevenselementen aan het schema in kaart brengen u vroeger bepaalde. U definieert een ander gegevenselement dat een representatie van uw XDM-schema biedt.

Een XDM-objectelement definiëren:

1. Selecteer **[!UICONTROL Data Elements]** in het linkerspoor.

2. Selecteer **[!UICONTROL Add Data Element]** .

3. In het dialoogvenster [!UICONTROL Create Data Element] :

   - Geef uw gegevenselement een naam, bijvoorbeeld `XDM - Page View` .

   - Selecteer **[!UICONTROL Adobe Experience Platform Web SDK]** in de lijst [!UICONTROL Extension] .

   - Selecteer **[!UICONTROL XDM Object]** in de lijst [!UICONTROL Data Element Type] .

   - Selecteer de sandbox in de lijst [!UICONTROL Sandbox] .

   - Selecteer het schema in de lijst [!UICONTROL Schema] .

   - Wijs het kenmerk `identification > core > ecid`, dat in uw schema is gedefinieerd, toe aan het gegevenselement ECID. Selecteer het cilinderpictogram om het ECID-gegevenselement gemakkelijk te kiezen in de lijst met gegevenselementen.

     ![ Uitgezocht ECID het Element van Gegevens ](./assets/pick-ecid-dataelement.png)

     ![ het Element van Gegevens van de Kaart ECID ](./assets/map-ecid.png)


   - Wijs het kenmerk `web > webPageDetails > name`, dat in uw schema is gedefinieerd, toe aan het gegevenselement Paginanaam.

     ![ het Element van de Gegevens van de Naam van de Pagina van de Kaart ](./assets/map-pagename.png)

   - Selecteer **[!UICONTROL Save]** .


#### **Regels**

Tags in Adobe Experience Platform volgen een op regels gebaseerd systeem. Zij zoeken gebruikersinteractie en bijbehorende gegevens. Wanneer aan de criteria die in uw regels worden geschetst wordt voldaan, teweegbrengt de regel de uitbreiding, het manuscript, of cliënt-zijcode in werking u identificeerde. U kunt regels gebruiken om gegevens (zoals een voorwerp XDM) naar Adobe Experience Platform te verzenden gebruikend de uitbreiding van SDK van het Web van Adobe Experience Platform.

Een regel definiëren:

1. Selecteer **[!UICONTROL Rules]** in het linkerspoor.

2. Selecteer **[!UICONTROL Create New Rule]** .

3. In het dialoogvenster [!UICONTROL Create Rule] :

   - Geef de regel een naam, bijvoorbeeld `Page View` .

   - Selecteer **[!UICONTROL + Add]** onder [!UICONTROL Events] .

   - In het dialoogvenster [!UICONTROL Event Configuration] :

      - Selecteer **[!UICONTROL Core]** in de lijst [!UICONTROL Extension] .

      - Selecteer **[!UICONTROL Window Loaded]** in de lijst [!UICONTROL Event Type] .

        ![ Regel - de Configuratie van de Gebeurtenis ](./assets/event-windowloaded-pageview.png)

      - Selecteer **[!UICONTROL Keep Changes]** .



   - Selecteer **[!UICONTROL + Add]** onder [!UICONTROL Actions] .

   - In het dialoogvenster [!UICONTROL Action Configuration] :

      - Selecteer **[!UICONTROL Adobe Experience Platform Web SDK]** in de lijst [!UICONTROL Extension] .

      - Selecteer **[!UICONTROL Send Event]** in de lijst [!UICONTROL Action Type] .

      - Selecteer **[!UICONTROL web.webpagedetails.pageViews]** in de lijst [!UICONTROL Type] .

      - Selecteer het cilinderpictogram naast [!UICONTROL XDM data] en selecteer **[!UICONTROL XDM - Page View]** in de lijst met gegevenselementen.

     ![ Regel - de Configuratie van de Actie ](./assets/action-pageview-xdm.png)

      - Selecteer **[!UICONTROL Keep Changes]** .

   - Uw regel moet er als volgt uitzien:

     ![ creeer Regel ](assets/rule-pageview.png)

   - Selecteer **[!UICONTROL Save]** .

Het bovenstaande is slechts een voorbeeld van het definiëren van een regel die XDM-gegevens met waarden uit andere gegevenselementen naar Adobe Experience Platform verzendt.

U kunt regels op verschillende manieren in uw tag gebruiken om variabelen te bewerken (met behulp van uw gegevenselementen).

Zie [ Regels ](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html) voor meer informatie.

### Uw tag maken en Publish

Nadat u gegevenselementen en regels hebt gedefinieerd, moet u de tag maken en publiceren. Wanneer u een bibliotheek maakt, moet u deze toewijzen aan een omgeving. De uitbreidingen, de regels, en de gegevenselementen van de bouwstijl worden dan gecompileerd en in het toegewezen milieu geplaatst. Elke omgeving bevat een unieke insluitcode waarmee u de toegewezen build in uw site kunt integreren.

Om uw markering te bouwen en te publiceren:

1. Selecteer **[!UICONTROL Publishing Flow]** in het linkerspoor.

2. Selecteer **[!UICONTROL Select a working library]** , gevolgd door **[!UICONTROL Add Library…]** .

3. In het dialoogvenster [!UICONTROL Create Library] :

   - Geef de bibliotheek een naam.

   - Selecteer **[!UICONTROL Development (development)]** in de lijst [!UICONTROL Environment] .

   - Selecteer **[!UICONTROL + Add All Changed Resources]** .

     ![ Publish - creeer Bibliotheek ](./assets/create-library-aep.png)

   - Selecteer **[!UICONTROL Save & Build to Development]** .

   Uw tag wordt opgeslagen en gebouwd voor uw ontwikkelomgeving. Een groene stip geeft aan dat uw tag met succes is opgebouwd in uw ontwikkelomgeving.

4. U kunt **[!UICONTROL ...]** selecteren om de bibliotheek opnieuw samen te stellen of de bibliotheek naar een testomgeving of productieomgeving te verplaatsen.

   ![ Publish - bouwt Bibliotheek ](./assets/build-library.png)

Adobe Experience Platform-tags ondersteunen eenvoudige tot complexe publicatieworkflows die geschikt zijn voor uw implementatie van de Adobe Experience Platform Web SDK.

Zie [ het Publiceren overzicht ](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html) voor meer informatie.


### De tagcode ophalen

Tot slot moet u de tag installeren op de website die u wilt bijhouden. Dit houdt in dat code in de kopteksttag van de sjabloon van uw website wordt geplaatst.

De code ophalen die naar de tag verwijst:

1. Selecteer **[!UICONTROL Environments]** in het linkerspoor.

2. Selecteer de juiste installatieknop in de lijst met omgevingen.

   Selecteer in het dialoogvenster [!UICONTROL Web Install Instructions] de knop Kopiëren naast de scriptcode die als volgt moet worden gelezen:

   ```
   <script src="https://assets.adobedtm.com/2a518741ab24/.../launch-...-development.min.js" async></script>>
   ```

   ![ Milieu ](./assets/environment.png)

3. Selecteer **[!UICONTROL Close]** .

In plaats van de code voor het ontwikkelmilieu, zou u een ander milieu (het opvoeren, productie) kunnen selecteren die op waar wordt gebaseerd u in het opstellen van het Web SDK van Adobe Experience Platform bent.

Zie [ Milieu&#39;s ](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/environments/environments.html?) voor meer informatie.

## Implementeren en valideren

U kunt de code nu implementeren in de ontwikkelingsversie van uw website binnen de tag `<head>` . Wanneer uw website wordt geïmplementeerd, worden gegevens verzameld in Adobe Experience Platform.

Valideer uw implementatie, verbeter het waar nodig, en zodra correct, stel het in uw het opvoeren en productiemilieu gebruikend de het publiceren werkschemafunctie van Markeringen op.

## Een verbinding instellen

Om de gegevens van Adobe Experience Platform in Customer Journey Analytics te gebruiken, creeert u een verbinding die de gegevens omvat die uit vestiging uw schema, dataset, en werkschema voortvloeien.

Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over deze datasets te rapporteren, moet u eerst een verband tussen datasets in Adobe Experience Platform en Workspace vestigen.

Om uw verbinding tot stand te brengen:

1. Selecteer **[!UICONTROL Connections]** in de bovenste navigatie in de gebruikersinterface van de Customer Journey Analytics.

2. Selecteer **[!UICONTROL Create new connection]** .

3. In het [!UICONTROL Untitled connection] -scherm:

   Geef een naam en beschrijf de verbinding in [!UICONTROL Connection Settings] .

   Selecteer de juiste sandbox in de lijst [!UICONTROL Sandbox] in [!UICONTROL Data settings] en selecteer het aantal dagelijkse gebeurtenissen in de lijst [!UICONTROL Average number of daily events] .

   ![ de Montages van de Verbinding ](./assets/cja-connections-1.png)

   Selecteer **[!UICONTROL Add datasets]** .

   In de stap [!UICONTROL Select datasets] in [!UICONTROL Add datasets] :

   - Selecteer de dataset die u vroeger (`Example dataset`) creeerde en om het even welke andere dataset u in uw verbinding wilt omvatten.

     ![ voeg datasets ](./assets/cja-connections-2b.png) toe

   - Selecteer **[!UICONTROL Next]** .

   In de stap [!UICONTROL Datasets settings] in [!UICONTROL Add datasets] :

   - Voor elke gegevensset:

      - Selecteer een [!UICONTROL Person ID] van de beschikbare identiteiten die in de datasetschema&#39;s in Adobe Experience Platform worden bepaald.

      - Selecteer de juiste gegevensbron in de lijst [!UICONTROL Data source type] . Als u **[!UICONTROL Other]** opgeeft, voegt u een beschrijving voor de gegevensbron toe.

      - Stel **[!UICONTROL Import all new data]** en **[!UICONTROL Dataset backfill existing data]** in op basis van uw voorkeuren.

     ![ vorm datasets ](./assets/cja-connections-3b.png)

   - Selecteer **[!UICONTROL Add datasets]** .

   Selecteer **[!UICONTROL Save]** .

Zie [ Overzicht van Verbindingen ](../connections/overview.md) voor meer informatie over om een verbinding tot stand te brengen en te beheren en datasets te selecteren en te combineren.

## Een gegevensweergave instellen

Een gegevensmening is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van een verbinding te interpreteren. Hiermee worden alle afmetingen en metriek opgegeven die beschikbaar zijn in Analysis Workspace en de kolommen waarvan die dimensies en metriek hun gegevens verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

Uw gegevensweergave maken:

1. Selecteer **[!UICONTROL Data views]** in de bovenste navigatie in de gebruikersinterface van de Customer Journey Analytics.

2. Selecteer **[!UICONTROL Create new data view]** .

3. In de stap [!UICONTROL Configure] :

   Selecteer de verbinding in de lijst [!UICONTROL Connection] .

   Naam en (optioneel) beschrijf uw verbinding.

   ![ de mening van Gegevens vormt ](./assets/cja-dataview-1.png)

   Selecteer **[!UICONTROL Save and continue]** .

4. In de stap [!UICONTROL Components] :

   Voeg schemagebieden en/of standaardcomponent toe die u aan de [!UICONTROL METRICS] of [!UICONTROL DIMENSIONS] componentenvakjes wilt omvatten.

   ![ de meningscomponenten van Gegevens ](./assets/cja-dataview-2.png)

   Selecteer **[!UICONTROL Save and continue]** .

5. In de stap [!UICONTROL Settings] :

   ![ de meningsmontages van Gegevens ](./assets/cja-dataview-3.png)

   Laat de instellingen ongewijzigd en selecteer **[!UICONTROL Save and finish]** .

Zie [ overzicht van de meningen van Gegevens ](../data-views/data-views.md) voor meer informatie over om een gegevensmening tot stand te brengen en uit te geven, welke componenten voor u aan gebruik in uw gegevensmening en hoe te filter en zittingsmontages te gebruiken beschikbaar zijn.


## Een project instellen

Analysis Workspace is een flexibel browserprogramma waarmee u snel analyses kunt maken en inzichten kunt delen op basis van uw gegevens. U gebruikt de projecten van Workspace om gegevenscomponenten, lijsten, en visualisaties te combineren om uw analyse te bundelen en met iedereen in uw organisatie te delen.

Uw project maken:

1. Selecteer **[!UICONTROL Projects]** in de bovenste navigatie in de gebruikersinterface van de Customer Journey Analytics.

2. Selecteer **[!UICONTROL Projects]** in de linkernavigatie.

3. Selecteer **[!UICONTROL Create project]** .

   ![ Project van Workspace ](./assets/cja-projects-1.png)

   Selecteer **[!UICONTROL Blank project]** .

   ![ Workspace - Leeg Project ](./assets/cja-projects-2.png)

4. Selecteer de gegevensweergave in de lijst.

   ![ de Uitgezochte mening van Gegevens van Workspace ](./assets/cja-projects-3.png).

5. Als u uw eerste rapport wilt maken, sleept u de afmetingen en metriek op de [!UICONTROL Freeform table] in de [!UICONTROL Panel] . Sleep bijvoorbeeld `Program Points Balance` en `Page View` als metriek en `email` als dimensie om een snel overzicht te krijgen van profielen die uw website hebben bezocht en deel uitmaken van het loyaliteitsprogramma dat loyaliteitspunten verzamelt.

   ![ Workspace - Eerste Rapport ](./assets/cja-projects-5.png)

Zie [ overzicht van Analysis Workspace ](../analysis-workspace/home.md) voor meer informatie over hoe te om projecten tot stand te brengen en uw analyse te bouwen gebruikend componenten, visualisaties, en panelen.

>[!SUCCESS]
>
>U hebt alle stappen uitgevoerd. Eerst definieert u welke gegevens u wilt verzamelen (schema) en waar u deze wilt opslaan (dataset) in Adobe Experience Platform. Vervolgens hebt u een gegevensstroom geconfigureerd op de Edge Network om ervoor te zorgen dat gegevens naar die gegevensset kunnen worden doorgestuurd. Vervolgens hebt u de tag gedefinieerd en geïmplementeerd die de extensies (Adobe Experience Platform Web SDK, Experience Cloud ID Service), gegevenselementen en regels bevat voor het vastleggen van gegevens van uw website en het verzenden van die gegevens naar uw gegevensstroom. U hebt een verbinding in Customer Journey Analytics gedefinieerd om uw website-volggegevens en andere gegevens te gebruiken. Met de definitie van uw gegevensweergave kunt u opgeven welke dimensie en metriek u wilt gebruiken en ten slotte hebt u uw eerste project gemaakt waarin uw gegevens worden gevisualiseerd en geanalyseerd.
