---
description: De filterontwikkelaar biedt een canvas waarin u Metrische afmetingen, filters en gebeurtenissen kunt slepen en neerzetten om personen te filteren op basis van logica in de containerhiërarchie, regels en operatoren. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige of complexe filters maken en opslaan waarmee u persoonlijke kenmerken en handelingen kunt identificeren voor bezoeken en gebeurtenissen.
title: Filters maken
feature: Filters
role: User
exl-id: 160021f1-6942-4682-9114-d375307d9912
source-git-commit: c94e97723a4ed30e675144e02196c93016b13235
workflow-type: tm+mt
source-wordcount: '1466'
ht-degree: 0%

---

# Filters maken {#build-filters}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_filters_createaudience"
>title="Publiek maken"
>abstract="Soorten publiek kan worden gemaakt op basis van een filter en worden gedeeld met de Adobe Experience Platform voor activering."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_filters_datapreview"
>title="Voorbeeld van gegevens"
>abstract="Vergelijkt de gegevens van dit filter met de gegevens van de gegevensweergave. Het voorbeeldpercentage is gebaseerd op het totale aantal in de gegevensweergave van de **afgelopen 90 dagen**.<br><br/>Als het voorbeeld niet wordt geladen, wordt uw verbinding mogelijk nog steeds opgevuld."

<!-- markdownlint-enable MD034 -->



Het **[!UICONTROL Filter builder]** dialoogvenster wordt gebruikt om nieuwe filters te maken of bestaande filters te bewerken. Het dialoogvenster heeft de titel **[!UICONTROL New filter]** of **[!UICONTROL Edit filter]** voor filters die u maakt of beheert vanuit de [[!UICONTROL Filters] manager](/help/components/filters/manage-filters.md).

>[!BEGINTABS]

>[!TAB Filter bouwer]

![Venster met filterdetails met velden en opties die in de volgende sectie worden beschreven.](assets/filter-builder.png)

>[!TAB Filter maken of bewerken]

![Venster met filterdetails met velden en opties die in de volgende sectie worden beschreven.](assets/create-edit-filter.png)

>[!ENDTABS]

1. Geef de volgende gegevens op (![vereist](/help/assets/icons/Required.svg) is vereist):

   | Element | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Data view]** | U kunt de gegevensweergave voor het filter selecteren.  Het filter u bepaalt is beschikbaar als filter op het [ lusje van Montages ](/help/data-views/create-dataview.md#settings-filters) van een gegevensmening. |
   | **[!UICONTROL Project-only filter]** | Een infobox om uit te leggen dat het filter alleen zichtbaar is in het project waar het is gemaakt en dat het filter niet wordt toegevoegd aan uw componentenlijst. Schakel deze **[!UICONTROL Make this filter available to all your projects and add it to your component list]** optie in om die instelling te wijzigen. Dit infovak is alleen zichtbaar wanneer u een [snelfilter](quick-filters.md) maakt en de snelfilterinformatie instelt in een normaal filter met behulp **[!UICONTROL Open builder]** van de [!UICONTROL Quick filter] interface. |
   | **[!UICONTROL Title]**![ Vereist](/help/assets/icons/Required.svg) | Geef het filter een naam, bijvoorbeeld `Last month mobile customers` . |
   | **[!UICONTROL Description]** | Geef een beschrijving voor het filter op, bijvoorbeeld `Filter to define the mobile customers for the last month` . |
   | **[!UICONTROL Tags]** | Organiseer het filter door een of meer tags te maken of toe te passen. Begin te typen om naar bestaande tags te zoeken die u kunt selecteren. Of druk op **[!UICONTROL ENTER]** om een nieuwe tag toe te voegen. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om een markering te verwijderen. |
   | **[!UICONTROL Definition]** ![ Vereiste ](/help/assets/icons/Required.svg) | Definieer uw filter met behulp van de [Definitiebouwer](#definition-builder). |

   {style="table-layout:auto"}

1. Als u wilt controleren of de filterdefinitie correct is, gebruikt u de constant bijgewerkte voorvertoning van de resultaten van het filter in de rechterbovenhoek.
1. Selecteer **[!UICONTROL Create audience from filter]** als u een publiek wilt maken van het filter en het publiek wilt delen met Experience Platform. Zie [ publiek ](/help/components/audiences/publish.md) voor meer informatie creëren en publiceren.
1. Selecteren:
   * **[!UICONTROL Save]** om het filter op te slaan.
   * **[!UICONTROL Save As]** om een kopie van het filter op te slaan.
   * **[!UICONTROL Delete]** om het filter te verwijderen.
   * **[!UICONTROL Cancel]** om eventuele wijzigingen die u in het filter hebt aangebracht te annuleren of het maken van een nieuw filter te annuleren.


## Definitie bouwer

U gebruikt de Definition Builder om uw filterdefinitie samen te stellen. In die constructie gebruik je componenten, containers, operators en logica.

U kunt het type en het werkingsgebied van uw definitie vormen:

1. Om het type van uw definitie te specificeren, specificeer of u de bouwstijl wilt omvatten of definitie uitsluiten. Selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) **[!UICONTROL Options]** en van dropdown knevel **[!UICONTROL Include]** of **[!UICONTROL Exclude]**.
1. Om het werkingsgebied van uw definitie te specificeren, selecteer van **[!UICONTROL Include]** of **[!UICONTROL Exclude]** dropdown of u het werkingsgebied van de definitie **[!UICONTROL Event]** wilt zijn, **[!UICONTROL Session]**, **[!UICONTROL Person]**, **[!UICONTROL Global Account]** [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"}, **[!UICONTROL Account]** [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"}, **[!UICONTROL Opportunity]** [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"}, of **[!UICONTROL Buying Group]** [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"}}

U kunt deze instellingen altijd later wijzigen.

### Onderdelen

Een essentieel onderdeel van de constructie van uw filterdefinitie is het gebruik van dimensies, metrische gegevens, bestaande filters en datumbereiken. Al deze componenten zijn beschikbaar via het componentenpaneel in de filterbouwer.

![Begin met het bouwen van een definitie](assets/start-building-filter.gif){width=100%}

Een component toevoegen:

1. Sleep een component van het componentenpaneel naar **[!UICONTROL Drag and drop Metric(s), Filter(s), and/or Dimensions here]**. U kunt de ![zoekfunctie](/help/assets/icons/Search.svg) in de onderdelenbalk gebruiken om naar specifieke onderdelen te zoeken.
1. Geef details voor de component op. Selecteer bijvoorbeeld een waarde uit **[!UICONTROL Select value]**. Of voer een waarde in. Wat en hoe u een of meer waarden kunt opgeven, is afhankelijk van het onderdeel en de operator.
1. Wijzig desgewenst de standaardoperator. Bijvoorbeeld, van **[!UICONTROL equals]** naar **[!UICONTROL equals any of]**. Zie [Operators](operators.md) voor een gedetailleerd overzicht van de beschikbare operators.

Een component bewerken:

* Selecteer een nieuwe operator voor het onderdeel in het vervolgkeuzemenu van de operator.
* Selecteer indien van toepassing een andere waarde voor de operator of geef deze op.
* Als het componenttype een dimensie is, kunt u het attributiemodel definiëren. Zie [ model van de Attributie ](#attribution-models) voor meer informatie.

Een component verwijderen:

* Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) in een component.

### Containers

U kunt meerdere componenten groeperen in een of meer containers en logica definiëren binnen en tussen containers. Met containers kunt u complexe definities voor uw filter maken.

![ voeg een container ](assets/add-container.gif){Width=100%} toe

* Om een container toe te voegen, selecteer **[!UICONTROL Add container]** van ![ Plaatsend ](/help/assets/icons/Setting.svg) **[!UICONTROL Options]**.
* Als u een bestaande component aan de container wilt toevoegen, sleept u de component naar de container.
* Als u een andere component aan de container wilt toevoegen, sleept u een component uit het deelvenster met componenten naar de container. Gebruik de blauwe invoeglijn als richtlijn.
* Als u een ander onderdeel buiten de container wilt toevoegen, sleept u een onderdeel van het deelvenster Onderdeel buiten de container, maar binnen de hoofddefinitiecontainer. Gebruik de blauwe invoeglijn als richtlijn.
* Als u de logica tussen componenten in een container, tussen containers of tussen een container en een onderdeel wilt wijzigen, selecteert u de juiste **[!UICONTROL And]**, **[!UICONTROL Or]**, **[!UICONTROL Then]**. Wanneer u Dan selecteert, verandert u het filter in een sequentieel filter. Zie [Sequentieel filter](seg-sequential-build.md) maken voor meer informatie.
* Om het containerniveau te schakelen, selecteer ](/help/assets/icons/Globe.svg) Globe **[!UICONTROL Global Account]** [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B-editie"}, ![ Rekening ](/help/assets/icons/Account.svg) **[!UICONTROL Account]** [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}, ![ Opportunity ](/help/assets/icons/Opportunity.svg) **[!UICONTROL Opportunity]** [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}, ![ BuyingGroup ](/help/assets/icons/BuyingGroup.svg) **[!UICONTROL Buying Group]** [!BADGE  B2B edition 19}, ![ WebPage ](/help/assets/icons/WebPage.svg) **[!UICONTROL Event]**, ![ Bezoek ](/help/assets/icons/Visit.svg) **[!UICONTROL Session]** of ![ Gebruiker ](/help/assets/icons/User.svg) **[!UICONTROL Person]**.![]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}

U kunt Instellingen](/help/assets/icons/Setting.svg) in een container gebruiken ![voor de volgende acties:

| Container actie | Beschrijving |
|---|---|
| **[!UICONTROL Add container]** | Voeg een geneste container toe aan de container. |
| **[!UICONTROL Exclude]** | Sluit het resultaat uit van de container in de filterdefinitie. Een dunne rode linkerbalk geeft een uitsluitingscontainer aan. |
| **[!UICONTROL Include]** | Neem het resultaat van de container op in de filterdefinitie. Opnemen is de standaardinstelling. Een dunne grijze linkerbalk identificeert een include-container. |
| **[!UICONTROL Name container]** | Wijzig de naam van de container vanuit de standaardbeschrijving. Typ een naam in het tekstveld. Als u geen invoer geeft, wordt de standaardbeschrijving gebruikt. |
| **[!UICONTROL Delete container]** | Verwijder de container uit de definitie. |


## Datumbereiken

U kunt filters bouwen die het rollen datumwaaiers bevatten. U bent dus in staat om vragen over lopende campagnes of evenementen te beantwoorden. U kunt bijvoorbeeld een filter maken dat iedereen omvat *die de afgelopen 60 dagen* een online aankoop heeft gedaan.

![Filteren op voortschrijdend datumbereik](assets/filter-rolling-date-range.gif)


>[!BEGINSHADEBOX]

Zie ![VideoUitgecheckt Voortschrijdende](/help/assets/icons/VideoCheckedOut.svg) [datumbereiken in segmenten](https://video.tv.adobe.com/v/25403/?quality=12&learn=on){target="_blank"} voor een demovideo.

>[!ENDSHADEBOX]


## Filters stapelen {#stack}

U kunt een filter bouwen met behulp van filters. Wanneer u filters in een filter gebruikt, kunt u uw filter optimaliseren en de complexiteit verminderen.

Stel je voor dat je wilt filteren op de combinatie van apparaattype (2) en Amerikaanse staten (50). Je kunt 100 filters bouwen, elk voor de unieke combinatie van apparaattype (mobiele telefoon versus tablet) en Amerikaanse staat. Om de Californische tabletgebruikers te krijgen, zou je een van de 100 filters gebruiken:

![Eenvoudig filter voor CA en tablet](assets/filter-ca-tablet-single.png)

Of u kunt 52 filters definiëren: 50 filters voor de Amerikaanse staten, één voor mobiele telefoons en één voor tablets. En stapel vervolgens de filters om dezelfde resultaten te verkrijgen. Als u de gebruikers van de Californische tablet wilt ophalen, stapelt u twee filters:

![Gestapeld filter voor CA en tablet](assets/filter-ca-tablet-stacked.png)


## Attributie {#attribution}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_filters_attribution_repeating"
>title="Herhalende"
>abstract="Bevat instanties en permanente waarden voor de dimensie."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_filters_attribution_instance"
>title="Voorbeeld"
>abstract="Bevat varianten en doorlopende waarden voor de dimensie."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_filters_attribution_nonrepeatinginstance"
>title="Niet-herhalende instantie"
>abstract="Bevat unieke (niet-herhalende) instanties voor de dimensie."

<!-- markdownlint-enable MD034 -->



Wanneer u een afmeting in de filterbouwer gebruikt, hebt u de opties om het attributiemodel voor die afmeting te specificeren. Het toewijzingsmodel dat u selecteert, bepaalt of de gegevens in aanmerking komen voor de voorwaarde die u voor de dimensie-component hebt opgegeven.

Selecteer ![ Vestiging ](/help/assets/icons/Setting.svg) binnen de afmetingscomponent en selecteer één van de modellen van de Attributie van popup:

| Modellen | Beschrijving |
|---|---|
| **[!UICONTROL Repeating model (default)]** | Neem exemplaar- en persistente waarden op voor de dimensie om de kwalificatie te bepalen. |
| **[!UICONTROL Instance]** | Neem alleen instantiewaarden op voor de dimensie om de kwalificatie te bepalen. |
| **[!UICONTROL Non-repeating instance]** | U kunt unieke instantie-waarden (niet-herhalende waarden) voor de dimensie opnemen om de kwalificatie te bepalen. |


![Attributiemodel op dimensie bij het bouwen van een filter](assets/filter-dimension-attribution.png)

### Voorbeeld

Als onderdeel van een filterdefinitie heb je de volgende voorwaarde opgegeven: Paginanaam is gelijk aan Vrouwen. Vergelijkbaar met het voorbeeld hierboven. U herhaalt deze filterdefinitie met behulp van de twee andere attributiemodellen. Je hebt dus drie filters met elk hun eigen attributiemodel:

* Pagina Vrouwen - Toeschrijving - Herhalend (standaard)
* Women page - Attribution - Instance
* Vrouwenpagina - Attributie - Niet-herhalende instantie


De lijst verklaart hieronder, voor elk attributiemodel, die de inkomende gebeurtenissen ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) voor die voorwaarde gekwalificeerd zijn.


| De Pagina van vrouwen - Attributie - <br/>*attributiemodel* | Gebeurtenis 1:<br/> de Naam van de Pagina evenaart <br/> Vrouwen | Gebeurtenis 2:<br/> de Naam van de Pagina evenaart <br/> Mannen | Gebeurtenis 3:<br/> de Naam van de Pagina evenaart <br/> Vrouwen | Gebeurtenis 4:<br/> de Naam van de Pagina evenaart <br/> Vrouwen <br/> (voortgeduurd) | Gebeurtenis 5:<br/> de Naam van de Pagina evenaart <br/> Controle | Gebeurtenis 6:<br/> de Naam van de Pagina evenaart <br/> Vrouwen | Gebeurtenis 7:<br/> de Naam van de Pagina evenaart <br/> Huis |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:--:|
| Herhalend (standaard) | ![Vinkje Cirkel](/help/assets/icons/CheckmarkCircle.svg) | ![Verwijderen](/help/assets/icons/Remove.svg) | ![Vinkje Cirkel](/help/assets/icons/CheckmarkCircle.svg) | ![Vinkje Cirkel](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![Vinkje Cirkel](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) |
| Instantie | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) |
| Niet-herhalende instantie | ![Vinkje Cirkel](/help/assets/icons/CheckmarkCircle.svg) | ![Verwijderen](/help/assets/icons/Remove.svg) | ![Vinkje Cirkel](/help/assets/icons/CheckmarkCircle.svg) | ![Verwijderen](/help/assets/icons/Remove.svg) | ![Verwijderen](/help/assets/icons/Remove.svg) | ![Vinkje Cirkel](/help/assets/icons/CheckmarkCircle.svg) | ![Verwijderen](/help/assets/icons/Remove.svg) |

Een voorbeeldrapport over evenementen met behulp van de drie filters ziet er als volgt uit:

![Resultaten van attributiemodel filteren](assets/filter-dimension-attribution-results.png)
