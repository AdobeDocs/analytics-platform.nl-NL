---
description: De filterontwikkelaar biedt een canvas voor het slepen en neerzetten van metrische Dimensionen, filters en gebeurtenissen om personen te filteren op basis van containerhiërarchische logica, regels en operatoren. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige of complexe filters maken en opslaan waarmee u persoonlijke kenmerken en handelingen kunt identificeren voor bezoeken en gebeurtenissen.
title: Filters maken
feature: Filters
role: User
exl-id: 160021f1-6942-4682-9114-d375307d9912
source-git-commit: 8eb146fccbdbe47df8ca28f7b8dcbce2bf6888fd
workflow-type: tm+mt
source-wordcount: '1402'
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
>title="Gegevensvoorbeeld"
>abstract="Vergelijkt de gegevens van dit filter met gegevens van de gegevensmening. Het voorproefpercentage is gebaseerd op het totale aantal in de gegevensmening van **laatste 90 dagen**.<br><br/> als de voorproef niet laadt, zou uw verbinding nog kunnen terugvullen."

<!-- markdownlint-enable MD034 -->



Het dialoogvenster **[!UICONTROL Filter builder]** wordt gebruikt om nieuwe filters te maken of bestaande filters te bewerken. Het dialoogvenster krijgt de naam **[!UICONTROL New filter]** of **[!UICONTROL Edit filter]** voor filters die u maakt of beheert met [[!UICONTROL Filters] Manager ](/help/components/filters/manage-filters.md) .

>[!BEGINTABS]

>[!TAB  Bouwer van de Filter ]

![ de detailvenster die van de Filter gebieden en opties tonen in de volgende sectie worden beschreven.](assets/filter-builder.png)

>[!TAB  creeer of geef filter ] uit

![ de detailvenster die van de Filter gebieden en opties tonen in de volgende sectie worden beschreven.](assets/create-edit-filter.png)

>[!ENDTABS]

1. Specificeer de volgende details (![ Vereiste ](/help/assets/icons/Required.svg) wordt vereist):

   | Element | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Data view]** | U kunt de gegevensweergave voor het filter selecteren.  Het filter u bepaalt is beschikbaar als filter op het [ lusje van Montages ](/help/data-views/create-dataview.md#settings-filters) van een gegevensmening. |
   | **[!UICONTROL Project-only filter]** | Een informatievak om uit te leggen dat het filter alleen zichtbaar is in het project waar het is gemaakt en dat het filter niet wordt toegevoegd aan de lijst met componenten. Schakel **[!UICONTROL Make this filter available to all your projects and add it to your component list]** in om die instelling te wijzigen. Dit infovakje is slechts zichtbaar wanneer u a [ snelle filter ](quick-filters.md) creeert en de snelle filterinfo een regelmatige filter draait gebruikend **[!UICONTROL Open builder]** van de [!UICONTROL Quick filter] interface. |
   | **[!UICONTROL Title]** ![ Vereiste ](/help/assets/icons/Required.svg) | Geef het filter een naam, bijvoorbeeld `Last month mobile customers` . |
   | **[!UICONTROL Description]** | Geef een beschrijving voor het filter op, bijvoorbeeld `Filter to define the mobile customers for the last month` . |
   | **[!UICONTROL Tags]** | Organiseer het filter door een of meer tags te maken of toe te passen. Begin te typen om naar bestaande tags te zoeken die u kunt selecteren. Of druk op **[!UICONTROL ENTER]** om een nieuwe tag toe te voegen. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om een markering te verwijderen. |
   | **[!UICONTROL Definition]** ![ Vereiste ](/help/assets/icons/Required.svg) | Bepaal uw filter gebruikend de [ bouwer van de Definitie ](#definition-builder). |

   {style="table-layout:auto"}

1. Als u wilt controleren of de filterdefinitie correct is, gebruikt u de constant bijgewerkte voorvertoning van de resultaten van het filter in de rechterbovenhoek.
1. Selecteer **[!UICONTROL Create audience from filter]** om een publiek van het filter te maken en het publiek met Experience Platform te delen. Zie [ publiek ](/help/components/audiences/publish.md) voor meer informatie creëren en publiceren.
1. Selecteren:
   * **[!UICONTROL Save]** om het filter op te slaan.
   * **[!UICONTROL Save As]** om een kopie van het filter op te slaan.
   * **[!UICONTROL Delete]** om het filter te verwijderen.
   * **[!UICONTROL Cancel]** om wijzigingen die u in het filter hebt aangebracht, te annuleren of om het maken van een nieuw filter te annuleren.


## Definition builder

Met de definitieontwikkelaar kunt u de filterdefinitie samenstellen. In die constructie, gebruikt u componenten, containers, exploitanten en logica.

U kunt het type en het werkingsgebied van uw definitie vormen:

1. Om het type van uw definitie te specificeren, specificeer of u de bouwstijl wilt omvatten of definitie uitsluiten. Selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) **[!UICONTROL Options]** en van dropdown knevel **[!UICONTROL Include]** of **[!UICONTROL Exclude]**.
1. Als u het bereik van uw definitie wilt opgeven, selecteert u in het vervolgkeuzemenu **[!UICONTROL Include]** of **[!UICONTROL Exclude]** of het bereik van de definitie **[!UICONTROL Event]** , **[!UICONTROL Session]** of **[!UICONTROL Person]** moet zijn.

U kunt deze instellingen altijd later wijzigen.

### Onderdelen

Een essentieel onderdeel van de constructie van uw filterdefinitie is het gebruik van afmetingen, meetwaarden, bestaande filters en datumbereiken. Al deze componenten zijn beschikbaar bij het componentenpaneel in de Bouwer van de Filter.

![ Begin bouwend een definitie ](assets/start-building-filter.gif) {width=100%}

Een component toevoegen:

1. Sleep een component van het deelvenster Componenten naar **[!UICONTROL Drag and drop Metric(s), Filter(s), and/or Dimensions here]** . U kunt het ![ Onderzoek ](/help/assets/icons/Search.svg) in de componentenbar gebruiken om naar specifieke componenten te zoeken.
1. Geef details voor de component op. Selecteer bijvoorbeeld een waarde in **[!UICONTROL Select value]** . Of voer een waarde in. Wat en hoe u een of meer waarden kunt opgeven, is afhankelijk van de component en de operator.
1. Wijzig desgewenst de standaardoperator. Bijvoorbeeld van **[!UICONTROL equals]** tot **[!UICONTROL equals any of]** . Zie [ Exploitanten ](operators.md) voor een gedetailleerd overzicht van de beschikbare exploitanten.

Een component bewerken:

* Selecteer een nieuwe operator voor de component in het vervolgkeuzemenu van de operator.
* Selecteer indien van toepassing een andere waarde voor de operator of geef deze op.
* Als het componenttype een dimensie is, kunt u het attributiemodel definiëren. Zie [ model van de Attributie ](#attribution-models) voor meer informatie.

Een component verwijderen:

* Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) in een component.

### Containers

U kunt meerdere componenten groeperen in een of meer containers en logica definiëren binnen en tussen containers. Met containers kunt u complexe definities voor uw filter maken.

![ voeg een container ](assets/add-container.gif) toe{Width=100%}

* Om een container toe te voegen, selecteer **[!UICONTROL Add container]** van ![ Plaatsend ](/help/assets/icons/Setting.svg) **[!UICONTROL Options]**.
* Als u een bestaande component aan de container wilt toevoegen, sleept u de component naar de container.
* Als u een andere component aan de container wilt toevoegen, sleept u een component uit het deelvenster met componenten naar de container. Gebruik de blauwe invoeglijn als hulplijn.
* Als u een andere component buiten de container wilt toevoegen, sleept u een component uit het deelvenster met componenten buiten de container, maar binnen de container met de hoofddefinitie. Gebruik de blauwe invoeglijn als hulplijn.
* Als u de logica tussen componenten in een container, tussen containers of tussen een container en een component wilt wijzigen, selecteert u de desbetreffende **[!UICONTROL And]**, **[!UICONTROL Or]**, **[!UICONTROL Then]** . Wanneer u vervolgens selecteert, verandert u het filter in een opeenvolgend filter. Zie [ opeenvolgend filter ](seg-sequential-build.md) voor meer informatie creëren.
* Om het containerniveau te schakelen, selecteer ![ WebPage ](/help/assets/icons/WebPage.svg) **[!UICONTROL Event]**, ![ Bezoek ](/help/assets/icons/Visit.svg) **[!UICONTROL Session]** of ![ Gebruiker ](/help/assets/icons/User.svg) **[!UICONTROL Person]**.

U kunt ![ Plaatsen ](/help/assets/icons/Setting.svg) in een container voor de volgende acties gebruiken:

| Container, actie | Beschrijving |
|---|---|
| **[!UICONTROL Add container]** | Voeg een geneste container toe aan de container. |
| **[!UICONTROL Exclude]** | Sluit het resultaat uit van de container in de filterdefinitie. Een dunne, rode linkerbalk geeft een uitsluitingscontainer aan. |
| **[!UICONTROL Include]** | Neem het resultaat van de container op in de filterdefinitie. Opnemen is de standaardinstelling. Een dunne grijze linkerbalk geeft een include-container aan. |
| **[!UICONTROL Name container]** | Wijzig de naam van de container ten opzichte van de standaardbeschrijving. Typ een naam in het tekstveld. Als u geen invoer opgeeft, wordt de standaardbeschrijving gebruikt. |
| **[!UICONTROL Delete container]** | Verwijder de container uit de definitie. |


## Datumbereiken

U kunt filters bouwen die het rollen datumwaaiers bevatten. U kunt dus vragen beantwoorden over lopende campagnes of evenementen. Bijvoorbeeld, kunt u een filter bouwen dat *iedereen omvat die een online aankoop in de afgelopen 60 dagen* heeft gemaakt.

![ Filter gebruikend het rollen datumwaaier ](assets/filter-rolling-date-range.gif)

+++ Hier is een video over het gebruik van roldatumbereiken in filters

>[!VIDEO](https://video.tv.adobe.com/v/25403/?quality=12)

{{videoaa}}

+++

## Stapelfilters {#stack}

U kunt een filter bouwen gebruikend filters. Wanneer u filters in een filter gebruikt, kunt u het filter optimaliseren en de complexiteit verminderen.

Stel dat u wilt filteren op de combinatie van apparaattype (2) en status VS (50). U kunt 100 filters maken, elk voor de unieke combinatie van apparaattype (mobiele telefoon versus tablet) en de Amerikaanse status. Om de gebruikers van de Californische tablet te krijgen, zou u één van de 100 filters gebruiken:

![ Eenvoudige filter voor CA en tablet ](assets/filter-ca-tablet-single.png)

Of u zou 52 filters kunnen definiëren: 50 filters voor de Amerikaanse staten, één voor mobiele telefoon en één voor tablet. Vervolgens stapelt u de filters om dezelfde resultaten te verkrijgen. Als u de gebruikers van de Californische tablet wilt ophalen, stapelt u twee filters:

![ Gestapelde filter voor CA en tablet ](assets/filter-ca-tablet-stacked.png)


## Attributie {#attribution}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_filters_attribution_repeating"
>title="Herhalend"
>abstract="Bevat varianten en doorlopende waarden voor de dimensie."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_filters_attribution_instance"
>title="Instantie"
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
| **[!UICONTROL Repeating model (default)]** | Instantie en doorlopende waarden voor de dimensie opnemen om kwalificatie te bepalen. |
| **[!UICONTROL Instance]** | Neem alleen instantiewaarden op voor de dimensie om de kwalificatie te bepalen. |
| **[!UICONTROL Non-repeating instance]** | U kunt unieke instantie-waarden (niet-herhalende waarden) voor de dimensie opnemen om de kwalificatie te bepalen. |


![ model van de Attributie op afmeting wanneer het bouwen van een filter ](assets/filter-dimension-attribution.png)

### Voorbeeld

Als onderdeel van een filterdefinitie hebt u de volgende voorwaarde opgegeven: De paginanaam is gelijk aan Vrouwen. Vergelijkbaar met het bovenstaande voorbeeld. U herhaalt deze filterdefinitie met de twee andere attributiemodellen. Dus u hebt drie filters elk met hun eigen attributiemodel:

* Vrouwenpagina - Attributie - Herhaling (standaard)
* Women page - Attribution - Instance
* Vrouwenpagina - Attributie - Niet-herhalende instantie


De lijst verklaart hieronder, voor elk attributiemodel, die de inkomende gebeurtenissen ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) voor die voorwaarde gekwalificeerd zijn.


| De Pagina van vrouwen - Attributie - <br/>*attributiemodel* | Gebeurtenis 1:<br/> de Naam van de Pagina evenaart <br/> Vrouwen | Gebeurtenis 2:<br/> de Naam van de Pagina evenaart <br/> Mannen | Gebeurtenis 3:<br/> de Naam van de Pagina evenaart <br/> Vrouwen | Gebeurtenis 4:<br/> de Naam van de Pagina evenaart <br/> Vrouwen <br/> (voortgeduurd) | Gebeurtenis 5:<br/> de Naam van de Pagina evenaart <br/> Controle | Gebeurtenis 6:<br/> de Naam van de Pagina evenaart <br/> Vrouwen | Gebeurtenis 7:<br/> de Naam van de Pagina evenaart <br/> Huis |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:--:|
| Herhaald (standaard) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) |
| Instantie | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) |
| Niet-herhalende instantie | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ verwijder ](/help/assets/icons/Remove.svg) |

Een voorbeeldrapport over gebeurtenissen die de drie filters gebruiken ziet er als volgt uit:

![ de resultaten van het de attributiemodel van de Filter ](assets/filter-dimension-attribution-results.png)
