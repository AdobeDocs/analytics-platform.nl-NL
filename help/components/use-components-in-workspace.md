---
description: Leer hoe u componenten aan een project kunt toevoegen in Analysis Workspace
title: Componenten in Analysis Workspace gebruiken
feature: Components
role: User
exl-id: 97bdfb9e-a27e-4a6b-b6cc-21a292398037
source-git-commit: 590a3ddbe988d27341fe96a3fa866960d1641e24
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 0%

---

# Componenten in Analysis Workspace gebruiken

Componenten vormen de feitelijke gegevens van elk project in Analysis Workspace. Componenten bestaan uit afmetingen, metriek, filters en datumbereiken. U kunt componenten aan een project toevoegen door hen in visualisaties of panelen te slepen.

Zie het [ overzicht van Componenten ](/help/components/overview.md) voor meer informatie over de types van componenten die u kunt toevoegen.

>[!TIP]
>
>Voor informatie over elke component, gebruik ![ InfoOutline ](/help/assets/icons/InfoOutline.svg). Zie [ Info van de Component ](#component-info) voor meer informatie

## Componenten aan een project toevoegen

1. [ creeer een project in Analysis Workspace ](/help/analysis-workspace/build-workspace-project/create-projects.md).

1. [ voeg een paneel ](/help/analysis-workspace/c-panels/panels.md#create-a-panel) toe of [ voeg een visualisatie ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel) aan het project in Analysis Workspace toe. Als u een component aan een leeg project toevoegt, wordt een vrije lijstvisualisatie reeds gecreeerd voor u.

1. Selecteer ![ Kromme ](/help/assets/icons/Curate.svg) **[!UICONTROL Components]** van het knooppaneel. Alle beschikbare componenten worden weergegeven in het linkerdeelvenster. Zie [ Interface ](/help/analysis-workspace/home.md#interface) voor meer details.

1. Blader naar of zoek naar de component die u wilt toevoegen en sleep deze naar een deelvenster of visualisatie in uw project.

1. U kunt een component naar keuze naar de filterneerzetzone in een deelvensterkop slepen. Met dit slepen en neerzetten definieert u de component als een filter en past u het filter toe op alle inhoud in het deelvenster.
Voor informatie over hoe u de zone van de filterdaling op een paneel kunt gebruiken om uw paneel te filtreren, zie [ de streek van de Daling ](/help/analysis-workspace/c-panels/panels.md#drop-zone) in [ Overzicht van Comités ](/help/analysis-workspace/c-panels/panels.md).

1. Raadpleeg de volgende secties voor meer informatie:

   * [Afmetingen toevoegen aan een project](#add-dimensions-to-a-project)

   * [Metriek toevoegen aan een project](#add-metrics-to-a-project)

   * [Filters toevoegen aan een project](#add-filters-to-a-project)

   * [Datumbereiken toevoegen aan een project](#add-date-ranges-to-a-project)

### Afmetingen toevoegen aan een project

[ Dimensionen ](/help/components/dimensions/overview.md) zijn variabelen in Customer Journey Analytics die typisch koordwaarden bevatten. In tegenstelling, [ metriek ](/help/components/calc-metrics/calc-metr-overview.md) bevatten numerieke waarden die aan een afmeting binden. Een basisrapport toont rijen van koordwaarden (afmeting), tegen een kolom van numerieke waarden (metrisch).

1. Begin toevoegend een afmeting aan uw project in Analysis Workspace, zoals die in [ wordt beschreven voegt componenten aan een project ](#add-components-to-a-project) toe.

1. Kies een van de volgende methoden om afmetingen toe te voegen en het type gegevens te bepalen dat u wilt analyseren:

   ![ voeg een afmeting ](/help/components/assets/add-dimension.gif) toe

   * Sleep een dimensie naar een visualisatie (zoals een vrije-vormlijst) in Analysis Workspace.

   * Sleep één of meerdere afmetingen van het linkerpaneel op de gebied van de filterdaling om een snelle filter tot stand te brengen, zoals die in [ wordt beschreven voegt filters aan een project ](#add-filters-to-a-project) toe.

1. U kunt desgewenst dimensies en dimensie-items in Analysis Workspace opsplitsen met andere componenten. Voor meer informatie, zie [ de dimensies van de Onderbreking in Workspace ](/help/components/dimensions/t-breakdown-fa.md).

Voor meer informatie over hoe te om afmetingen in Analysis Workspace te gebruiken, zie {de afmetingen van de Voorproef ](/help/components/dimensions/view-dimensions.md), [ de dimensies van de Onderbreking ](/help/components/dimensions/t-breakdown-fa.md), en [ tijd-ontledende dimensies ](/help/components/dimensions/time-parting-dimensions.md).[

### Metriek toevoegen aan een project

Met cijfers kunt u gegevenspunten in Analysis Workspace kwantificeren. Deze worden meestal gebruikt als kolommen in een visualisatie en zijn gekoppeld aan afmetingen.

Om metrisch aan een project in Analysis Workspace toe te voegen:

1. Begin metrisch aan uw project in Analysis Workspace toe te voegen, zoals die in [ wordt beschreven voegt componenten aan een project ](#add-components-to-a-project) toe.



1. Kies een van de volgende methoden om metrisch toe te voegen in Analysis Workspace:

   ![ Toevoegend metrisch ](/help/components/assets/add-metric.gif)

   * Sleep metrisch aan de metrische dalingsstreek in een lege lijst Freeform om te zien dat metrisch over de de datumperiode van het project trended.

   * Sleep metrisch wanneer een afmeting aanwezig is om dat metrisch voor elk afmetingspunt te zien.

   * Sleep metrisch bovenop een bestaande metrische kopbal om het te vervangen.

   * Sleep metrisch naast de linkerzijde van juiste kant van een bestaande metrische kopbal om nieuwe metrisch toe te voegen.

   * Sleep metrische boven of onder een bestaande metrische kopbal om metrische overlapping tot stand te brengen.


Voor meer informatie over metriek, zie [ Metriek ](/help/components/apply-create-metrics.md).

### Filters toevoegen aan een project

[ Filters ](/help/components/filters/filters-overview.md) staan u toe om ondergroepen van personen, zittingen of gebeurtenissen te identificeren die op kenmerken of specifieke interactie worden gebaseerd.

U kunt filters in Analysis Workspace op de volgende manieren gebruiken:

* Filters toevoegen aan een deelvenster
Wanneer u filters toevoegt aan een deelvenster, worden de filters toegepast op alle inhoud in het deelvenster.
Voor informatie over hoe u de zone van de filterdaling op een paneel kunt gebruiken om uw paneel te filtreren, zie [ de streek van de Daling ](/help/analysis-workspace/c-panels/panels.md#drop-zone) in [ Overzicht van Comités ](/help/analysis-workspace/c-panels/panels.md).

* Filters toevoegen aan een visualisatie
Wanneer u filters toevoegt aan een kolom in een vrije-vormlijst, zijn de filters van toepassing op alle inhoud binnen de lijstkolom. U kunt filters ook toevoegen als onderdeel van een fallout-visualisatie.

* Filters gebruiken in componenten
Wanneer u componenten zoals [ berekende metriek ](/help/components/calc-metrics/cm-workflow/metrics-with-segments.md) bepaalt, [ annotaties ](/help/components/annotations/create-annotations.md#annotation-builder), of zelfs [ filters ](/help/components/filters/filter-builder.md) kunt u filters als deel van de definitie gebruiken.


### Datumbereiken toevoegen aan een project

[ de waaiers van de Datum ](/help/components/date-ranges/overview.md) bepalen het rapporteringstijdkader in Analysis Workspace, en kunnen op één of meerdere panelen binnen een project en ook op sommige visualisaties (zoals de lijst Freeform) worden toegepast.

Elk deelvenster bevat standaard een datumbereik. Er zijn meerdere manieren om een datumbereik voor een deelvenster bij te werken. Een manier om een datumbereik voor een deelvenster in Analysis Workspace bij te werken, is door een component met een datumbereik uit het linkerdeelvenster te slepen:

1. Naar keuze, voeg een datumwaaier aan uw project in Analysis Workspace toe, zoals die in [ wordt beschreven voegt componenten aan een project ](#add-components-to-a-project) toe.

1. Sleep een datumbereik van het linkerdeelvenster naar:

   * Het huidige datumbereik om het datumbereik voor het deelvenster te wijzigen.

     ![ Daling een datumwaaier ](assets/add-date-range.gif)

   * Een metrische of afmeting in de visualisatie van een Freeform-tabel. Zie [ gegevenswaaiers van het Gebruik ](/help/components/date-ranges/overview.md#use-date-ranges) voor meer informatie.

Voor meer informatie over hoe te om datumwaaiers in Analysis Workspace te gebruiken en te beheren, zie [ overzicht van de waaiers van de Datum ](/help/components/date-ranges/overview.md).

## Componentinformatie

U kunt over om het even welke component bewegen om ![ Meer info ](/help/assets/icons/InfoOutline.svg) te tonen. Als deze optie is geselecteerd, wordt een pop-up weergegeven met aanvullende informatie over de component.

![ Info van de Component ](assets/component-info.png)

Gebaseerd op uw toegangsbeheer, kunt u:

* Heb toegang tot de ![ 2} definitie van de Bladwijzer ](/help/assets/icons/Bookmark.svg) {voor de component.[!UICONTROL Data dictionary]
* Heb toegang ![ uitgeeft ](/help/assets/icons/Edit.svg) componentenbouwer of gegevensmening waar de component wordt bepaald.
