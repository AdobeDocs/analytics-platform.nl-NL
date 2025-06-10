---
description: De Berekende Bouwer van Metriek verstrekt een canvas om Afmetingen, Metriek, Segmenten, en Functies te slepen en te laten vallen om douanemetriek tot stand te brengen die op de logica van de containerhiërarchie, regels, en exploitanten wordt gebaseerd. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige berekende metriek of complexe, berekende metriek bouwen en opslaan.
title: Berekende maatstaven samenstellen
feature: Calculated Metrics
exl-id: 4d03a51d-c676-483c-98e2-d7283e8d71b0
source-git-commit: 38be838fccf896a12da3fbadac50e578081312ba
workflow-type: tm+mt
source-wordcount: '1534'
ht-degree: 0%

---

# Berekende maatstaven samenstellen {#build-metrics}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_productcompatibility"
>title="Productcompatibiliteit"
>abstract="Geeft aan waar in Customer Journey Analytics deze berekende metrische waarde kan worden gebruikt, zoals in Analysis Workspace, Report Builder enzovoort. Sommige berekende metriek kunnen niet met experimenteren worden gebruikt."
>additional-url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation#use-in-experimentation" text="Berekende meetwaarden gebruiken in experimenten"

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_externalid"
>title="Externe id"
>abstract="Het veranderen van Externe identiteitskaart zou kunnen beïnvloeden hoe berekende metrisch in externe bronnen zoals bedrijfsintelligentiegereedschappen verschijnt"

<!-- markdownlint-enable MD034 -->

Customer Journey Analytics biedt een canvas voor het slepen en neerzetten van dimensies, metriek, segmenten en functies om aangepaste metrische gegevens te maken op basis van logica in de containerhiërarchie, regels en operatoren. Met dit geïntegreerde ontwikkelprogramma kunt u eenvoudige of complexe berekende meetgegevens maken en opslaan.

## Beginnen met het bouwen van een berekende metrische waarde

U kunt de berekende metrische bouwer gebruiken om berekende metriek tot stand te brengen of uit te geven. Wanneer gecreeerd op deze manier, zijn de berekende metriek beschikbaar in de componentenlijst en kunnen dan in projecten door uw organisatie worden gebruikt. Alternatief, kunt u snel berekende metrisch tot stand brengen die slechts voor het project beschikbaar is waar het werd gecreeerd, zoals die in [ wordt beschreven creeer berekende metriek voor één enkel project ](/help/components/apply-create-metrics.md#create-calculated-metrics-for-a-single-project) in [ Metriek ](/help/components/apply-create-metrics.md).

Heb toegang tot de berekende metrische bouwer beginnen creërend berekende metrisch die in de componentenlijst beschikbaar is.

1. Heb toegang tot de berekende metrische bouwer op om het even welke volgende manieren:

   * Open in Analysis Workspace een project en selecteer vervolgens **[!UICONTROL Components]** > **[!UICONTROL Create metric]** .
   * In Analysis Workspace, open een project, dan selecteer **plus** pictogram naast de [!UICONTROL **sectie van Metriek**] in de linkerspoorlijn.
   * Ga in [!DNL Customer Journey Analytics] naar **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]** en selecteer vervolgens **[!UICONTROL + Add]** boven aan de pagina Berekende meetgegevens.

1. Ga met [ Gebieden van de berekende metrische bouwer ](#areas-of-the-calculated-metrics-builder) verder.

## Gebieden van de berekende metriebouwer

Het dialoogvenster **[!UICONTROL Calculated metric builder]** wordt gebruikt om nieuwe berekende waarden te maken of te bewerken. Het dialoogvenster krijgt de naam **[!UICONTROL New calculated metric]** of **[!UICONTROL Edit calculated metric]** voor metriek die u maakt of beheert via de [[!UICONTROL Calculated metrics] manager ](/help/components/calc-metrics/cm-workflow/cm-manager.md) .

>[!BEGINTABS]

>[!TAB  Berekende metrische bouwer ]

![ Berekend metrisch detailsvenster dat gebieden en opties toont die in de volgende sectie worden beschreven.](assets/calculated-metric-builder.png)

>[!TAB creeer of geef berekend metrisch  uit]

![ Berekend metrisch detailsvenster dat gebieden en opties toont die in de volgende sectie worden beschreven.](assets/create-edit-calculated-metric.png)

>[!ENDTABS]

1. Specificeer de volgende details (![ Vereiste ](/help/assets/icons/Required.svg) wordt vereist):

   | Element | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Data view]** | U kunt de gegevensweergave voor de berekende metrische waarde selecteren.  De berekende metrisch u bepaalt is beschikbaar in de projecten van Workspace die op de geselecteerde gegevensmening worden gebaseerd. |
   | **[!UICONTROL Project-only metric]** | Een infodoos verschijnt bij de bovenkant van deze dialoog wanneer u berekende metrisch uitgeeft die voor één enkel project werd gecreeerd, zoals die in [ wordt beschreven creeer berekende metriek voor één enkel project ](/help/components/apply-create-metrics.md#create-calculated-metrics-for-a-single-project). <p>Als u deze berekende metrische waarde beschikbaar wilt maken voor alle projecten, selecteert u de optie, **[!UICONTROL Make this metric available to all your projects and add it to your component list]**.</p> |
   | **[!UICONTROL Title]** ![ Vereiste ](/help/assets/icons/Required.svg) | Geef de berekende metrische waarde een naam, bijvoorbeeld `Conversion Rate` . |
   | **[!UICONTROL External ID]** ![ Vereiste ](/help/assets/icons/Required.svg) | De naam van berekende metrisch wanneer het gebruiken van een extern hulpmiddel van BI en de uitbreiding van BI. De waarde wordt automatisch gedefinieerd als `undefined_xxx` , tenzij u de waarde overschrijft. |
   | **[!UICONTROL Description]** | Geef een beschrijving voor het segment, bijvoorbeeld `Calculated metric to define the conversion rate.` U hoeft de formule voor de berekende metrische waarde niet te beschrijven omdat de formule al automatisch beschikbaar is in [!UICONTROL Summary] . |
   | **[!UICONTROL Format]** | Selecteer een indeling voor de berekende metrische waarde: u kunt tussen **[!UICONTROL Decimal]** , **[!UICONTROL Time]** , **[!UICONTROL Percent]** en **[!UICONTROL Currency]** selecteren. |
   | **[!UICONTROL Decimal places]** | Geef het aantal decimalen op voor de geselecteerde notatie. Wordt alleen ingeschakeld wanneer de geselecteerde indeling Decimaal, Valuta en Percentage is. |
   | **[!UICONTROL Show upward trend as]** | Geef op of een opwaartse trend van de berekende metrische waarde wordt weergegeven als ▲ **[!UICONTROL Good (Green)]** of als ▼ **[!UICONTROL Bad (Red)]** . |
   | **[!UICONTROL Currency]** | Geef de valuta van de berekende metrische waarde op. Alleen ingeschakeld wanneer de geselecteerde notatie Valuta is. |
   | **[!UICONTROL Tags]** | Organiseer de berekende metrisch door één of meerdere markeringen te creëren of toe te passen. Begin te typen om naar bestaande tags te zoeken die u kunt selecteren. Of druk op **[!UICONTROL ENTER]** om een nieuwe tag toe te voegen. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om een markering te verwijderen. |
   | **[!UICONTROL Preview]** | De voorvertoning geldt voor de laatste 90 dagen en is een manier om te bepalen of u de maateenheid correct hebt gedefinieerd. |
   | **[!UICONTROL Summary]** | Toont een samenvatting van de definitie van berekende metrisch. <br/> bijvoorbeeld: ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Total Orders]** ![ verdeel ](/help/assets/icons/Divide.svg) ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Sessions]**. |
   | **[!UICONTROL Definition]** ![ Vereiste ](/help/assets/icons/Required.svg) | Bepaal uw segment gebruikend de [ bouwer van de Definitie ](#definition-builder). |

1. Om te verifiëren of uw berekende metrische definitie correct is, gebruik constant bijgewerkt **[!UICONTROL Preview]** van de resultaten van berekende metrisch. **[!UICONTROL Preview]** geldt voor de laatste 90 dagen en evalueert continu de definitie van de berekende maateenheid.

   **[!UICONTROL Product compatibility]** wijst erop of berekende metrisch in experimenteren kan worden gebruikt. Mogelijke waarden zijn:
   * **[!UICONTROL Everywhere in Customer Journey Analytics]**: De berekende metrische waarde kan in alle Customer Journey Analytics worden gebruikt.
   * **[!UICONTROL Everywhere in Customer Journey Analytics (excluding experimentation)]**: De berekende metrische waarde kan in alle Customer Journey Analytics worden gebruikt, behalve in het deelvenster Experimentatie.

1. Selecteren:
   * **[!UICONTROL Save]** om de berekende metrische waarde op te slaan.
   * **[!UICONTROL Save As]** om een kopie van de berekende metrische waarde op te slaan.
   * **[!UICONTROL Cancel]** om wijzigingen in de berekende metrische waarde te annuleren of om het maken van een nieuwe berekende metrische waarde te annuleren.


## Definition builder

U gebruikt de bouwer van de Definitie om dimensies, metriek, segmenten, en functies te slepen en te laten vallen om douanemetriek tot stand te brengen die op de logica van de containerhiërarchie, regels, en exploitanten wordt gebaseerd. In die constructie, kunt u standaardmetriek, Adobe bepaalde metriek, berekende metriek, segmenten, dimensies en functies gebruiken. Al deze componenten zijn beschikbaar bij het componentenpaneel in de Berekende metrische bouwer. Bovendien kunt u operatoren en containers in de definitie gebruiken.

![ creeer berekende metrisch ](/help/components/calc-metrics/cm-workflow/assets/create-calculated-metric.gif)

Alleen metriek worden gedefinieerd als afzonderlijke componenten in het **[!UICONTROL Definition]** -gebied. Alle andere componenten worden gedefinieerd als een container, verpakkingsmetriek of andere containers. Zie [ Containers ](#containers) voor meer informatie.

### Metrics

Een metrische waarde toevoegen:

* Sleep een ![ component van Gebeurtenissen ](/help/assets/icons/Event.svg) **[!UICONTROL Metrics]** van het componentenpaneel aan **[!UICONTROL Drag and drop metrics, dimensions, dimension items, segments, and/or functions here]**. U kunt het ![ Onderzoek ](/help/assets/icons/Search.svg) in de componentenbar gebruiken om naar specifieke componenten te zoeken.

Wanneer u berekende metrisch als deel van uw definitie gebruikt, wordt berekende metrisch uitgebreid.

Een metrische waarde wijzigen:

1. Selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) in metrische component in het **[!UICONTROL Definition]** gebied.
1. In het popup dialoogvenster kunt u het type metrisch en een attributiemodel bepalen. Zie [ Metrisch type en Attributie ](m-metric-type-alloc.md).

Een metrische waarde verwijderen:

* Selecteer ![ dicht ](/help/assets/icons/Close.svg) in metrisch.

### Operatoren

Met operatoren kunt u de operator tussen componenten of containers opgeven. Operatoren worden automatisch weergegeven tussen

* twee of meer meeteenheden in een container,
* twee of meer recipiënten in een recipiënt,
* een of meer maateenheden en een of meer containers in een container.

U kunt selecteren:

| Symbool | Operator |
|:---:|---|
| ![ Splitsen ](/help/assets/icons/Divide.svg) | Splitsen (standaard) |
| ![ dicht ](/help/assets/icons/Close.svg) | Vermenigvuldigen |
| ![ verwijder ](/help/assets/icons/Remove.svg) | Aftrekken |
| ![ voeg toe ](/help/assets/icons/Add.svg) | Toevoegen |

### Statisch getal

U kunt een statisch aantal aan uw berekende metrische definitie toevoegen. Een statisch getal toevoegen:

* Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add]** van binnen een container.
* Selecteer **[!UICONTROL Static number]** . Er wordt een container met statische getallen weergegeven.
* Selecteer [!UICONTROL *klik om een waarde*] toe te voegen en een waarde te typen.


### Containers

U voegt afmetingen, segmenten en functies als containers toe aan een berekende metrische definitie. U kunt ook een algemene container toevoegen. Containers werken als een wiskundige expressie en bepalen de volgorde van bewerkingen. Alles in een container wordt verwerkt vóór de volgende component of container.


#### Segmentcontainer

U gebruikt het concept van een segmentcontainer om metrische a [ gesegmenteerde tot stand te brengen ](metrics-with-segments.md). U kunt een segmentcontainer maken met behulp van een segment of met behulp van een segment dat u maakt op basis van een dimensie.

* Een segmentcontainer toevoegen vanuit een dimensie:

   1. De belemmering en laat vallen a ![ Dimensies ](/help/assets/icons/Dimensions.svg) **[!UICONTROL Dimensions]** component van het componentenpaneel op **[!UICONTROL Drag and drop metrics, dimensions, dimension items, segments, and/or functions here]**. U kunt het ![ Onderzoek ](/help/assets/icons/Search.svg) in de componentenbar gebruiken om naar specifieke componenten te zoeken.
   1. Definieer in de pop-up **[!UICONTROL Create Segment from Dimension]** de voorwaarde voor het segment. Selecteer een waarde in de lijst met operatoren en selecteer een waarde of voer een waarde in. Bijvoorbeeld, **[!UICONTROL Month]** **[!UICONTROL equals]** ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) `Sep 2024`.
   1. Selecteer **[!UICONTROL Done]** . Er wordt een segmentcontainer toegevoegd aan de **[!UICONTROL Definition]** .


* Als u een segmentcontainer vanuit een segment wilt toevoegen, kunt u:

   * Sleep de component van de a ![ Segmentatie ](/help/assets/icons/Segmentation.svg) **[!UICONTROL Segments]** van het componentenpaneel op **[!UICONTROL Drag and drop metrics, dimensions, dimension items, segments, and/or functions here]**. U kunt het ![ Onderzoek ](/help/assets/icons/Search.svg) in de componentenbar gebruiken om naar specifieke segmenten te zoeken.
Er wordt automatisch een segmentcontainer toegevoegd aan de **[!UICONTROL Definition]** , met de naam van het segment.

   * De belemmering en laat vallen a ![ Segmentatie ](/help/assets/icons/Segmentation.svg) **[!UICONTROL Segment]** component van het componentenpaneel op een generische container. De container wordt gewijzigd in een segmentcontainer.

   * Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add]** van binnen een container:

      1. Selecteer **[!UICONTROL Segment]** . Er wordt een segmentcontainer toegevoegd aan de **[!UICONTROL Definition]** .
      1. In de nieuwe segmentcontainer, selecteer een segment van [!UICONTROL *Uitgezocht..*] drop-down menu.

  >[!TIP]
  >
  >U kunt meer dan één segment aan een container toevoegen.

  De segmenten in de container worden genoemd naar de segmentcomponent. Bijvoorbeeld, ![ Segmentatie ](/help/assets/icons/Segmentation.svg) **[!UICONTROL Web sessions]**. Selecteer ![ InfoOutline ](/help/assets/icons/InfoOutline.svg) om popup met details op het segment te tonen. In popup, uitgezocht ![ geef ](/help/assets/icons/Edit.svg) uit om de segmentdefinitie uit te geven.

Een segment verwijderen uit een container:

* Selecteer ![ dicht ](/help/assets/icons/Close.svg) naast de segmentnaam.

Zie [ Gesegmenteerde metriek ](metrics-with-segments.md) voor meer details en voorbeelden.

#### Functiecontainer

Als u een functiecontainer wilt toevoegen, kunt u het volgende gebruiken:

* Sleep en zet:

   1. De belemmering en laat vallen a ![ component van de Functie ](/help/assets/icons/Effect.svg) **[!UICONTROL Functions]** van het componentenpaneel op **[!UICONTROL Drag and drop metrics, dimensions, dimension items, segments, and/or functions here]**. U kunt het ![ Onderzoek ](/help/assets/icons/Search.svg) in de componentenbar gebruiken om naar specifieke functies te zoeken.
   1. Er wordt automatisch een functienotel toegevoegd aan de **[!UICONTROL Definition]** met de naam van de functie.

* Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add]** van binnen een container:

   1. Selecteer **[!UICONTROL Function]** .
   1. In de container, selecteer een functie van [!UICONTROL *Uitgezocht...*] drop-down menu.

De functievulling krijgt de naam van de functiecomponent. Bijvoorbeeld, ![ Functie ](/help/assets/icons/Effect.svg) **[!UICONTROL SQUARE ROOT (metric)]**. Selecteer ![ InfoOutline ](/help/assets/icons/InfoOutline.svg) om popup met details op de functie te tonen. Selecteer **[!UICONTROL Learn more]** voor meer informatie over de functie.

Zie [ functies van het Gebruik ](cm-using-functions.md) voor details op hoe te om functies te gebruiken en welke functies beschikbaar zijn om berekende metrisch tot stand te brengen.


#### Algemene container

Een algemene container toevoegen:

* Selecteer ![&#128279;](/help/assets/icons/AddCircle.svg) AddCircle **[!UICONTROL Add]** van binnen een container
* Selecteer **[!UICONTROL Container]** . Er wordt een nieuwe lege generieke container toegevoegd aan de **[!UICONTROL Definition]** . U kunt een generische container gebruiken om een hiërarchie in de definitie van uw berekende metrisch te nesten of tot stand te brengen.


#### Een container verwijderen

Om een container te schrappen, selecteer ![ dicht ](/help/assets/icons/Close.svg) op het containerniveau.

>[!MORELIKETHIS]
>
>[Functies gebruiken](cm-using-functions.md)
>&#x200B;>[Segmenten ](/help/components/segments/seg-overview.md)
>

