---
description: Leer hoe u componenten in een project in Analysis Workspace kunt gebruiken
title: Componenten in een project gebruiken
feature: Components
role: User
exl-id: 97bdfb9e-a27e-4a6b-b6cc-21a292398037
source-git-commit: c209341400bf4e0c00719075f0fc82f81ca9dbb4
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 0%

---

# Componenten in een project gebruiken

Componenten vormen de feitelijke gegevens van elk project in Analysis Workspace. Componenten bestaan uit afmetingen, metriek, segmenten en datumbereiken. U kunt componenten aan een project toevoegen door hen in visualisaties of panelen te slepen.

Zie het [&#x200B; overzicht van Componenten &#x200B;](/help/components/overview.md) voor meer informatie over de types van componenten die u kunt toevoegen.

>[!TIP]
>
>Voor informatie over elke component, gebruik ![&#x200B; InfoOutline &#x200B;](/help/assets/icons/InfoOutline.svg). Zie [&#x200B; Info van de Component &#x200B;](#component-info) voor meer informatie

## Componenten aan een project toevoegen

1. [&#x200B; creeer een project in Analysis Workspace &#x200B;](/help/analysis-workspace/build-workspace-project/create-projects.md).

1. [&#x200B; voeg een paneel &#x200B;](/help/analysis-workspace/c-panels/panels.md#create-a-panel) toe of [&#x200B; voeg een visualisatie &#x200B;](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel) aan het project in Analysis Workspace toe. Als u een component aan een leeg project toevoegt, wordt een vrije lijstvisualisatie reeds gecreeerd voor u.

1. Selecteer ![&#x200B; Kromme &#x200B;](/help/assets/icons/Curate.svg) **[!UICONTROL Components]** van het knooppaneel. Alle beschikbare componenten worden weergegeven in het linkerdeelvenster. Zie [&#x200B; Interface &#x200B;](/help/analysis-workspace/home.md#interface) voor meer details.

1. Blader naar of zoek naar de component die u wilt toevoegen en sleep deze naar een deelvenster of visualisatie in uw project.

1. U kunt een component naar keuze slepen naar de neerzetzone van het segment in een deelvensterkop. Met dit slepen en neerzetten definieert u de component als een segment en past u het segment toe op alle inhoud in het deelvenster.
Voor informatie over hoe u de sectie van de segmentdaling op een paneel kunt gebruiken om uw paneel te segmenteren, zie [&#x200B; de streek van de Daling &#x200B;](/help/analysis-workspace/c-panels/panels.md#drop-zone) in [&#x200B; Overzicht van Comités &#x200B;](/help/analysis-workspace/c-panels/panels.md).

1. Raadpleeg de volgende secties voor meer informatie:

   * [Afmetingen toevoegen aan een project](#add-dimensions-to-a-project)

   * [Metriek toevoegen aan een project](#add-metrics-to-a-project)

   * [Segmenten toevoegen aan een project](#add-segments-to-a-project)

   * [Datumbereiken toevoegen aan een project](#add-date-ranges-to-a-project)

### Afmetingen toevoegen aan een project

[&#x200B; Afmetingen &#x200B;](/help/components/dimensions/overview.md) zijn variabelen in Customer Journey Analytics die typisch koordwaarden bevatten. In tegenstelling, [&#x200B; metriek &#x200B;](/help/components/calc-metrics/calc-metr-overview.md) bevatten numerieke waarden die aan een afmeting binden. Een basisrapport toont rijen van koordwaarden (afmeting), tegen een kolom van numerieke waarden (metrisch).

1. Begin toevoegend een afmeting aan uw project in Analysis Workspace, zoals die in [&#x200B; wordt beschreven voegt componenten aan een project &#x200B;](#add-components-to-a-project) toe.

1. Kies een van de volgende methoden om afmetingen toe te voegen en het type gegevens te bepalen dat u wilt analyseren:

   ![&#x200B; voeg een afmeting &#x200B;](/help/components/assets/add-dimension.gif) toe

   * Sleep een dimensie naar een visualisatie (zoals een vrije-vormlijst) in Analysis Workspace.

   * Sleep één of meerdere dimensies van het linkerpaneel op de gebied van het segmentdaling om een snel segment tot stand te brengen, zoals die in [&#x200B; wordt beschreven voegt segmenten aan een project &#x200B;](#add-filters-to-a-project) toe.

1. U kunt desgewenst dimensies en dimensie-items in Analysis Workspace opsplitsen met andere componenten. Voor meer informatie, zie [&#x200B; de dimensies van de Onderbreking in Workspace &#x200B;](/help/components/dimensions/t-breakdown-fa.md).

Voor meer informatie over hoe te om afmetingen in Analysis Workspace te gebruiken, zie &lbrace;de afmetingen van de Voorproef [, &#x200B;](/help/components/dimensions/view-dimensions.md) de dimensies van de Onderbreking [, en &#x200B;](/help/components/dimensions/t-breakdown-fa.md) tijd-ontledende dimensies [.](/help/components/dimensions/time-parting-dimensions.md)

### Metriek toevoegen aan een project

Met cijfers kunt u gegevenspunten in Analysis Workspace kwantificeren. Deze worden meestal gebruikt als kolommen in een visualisatie en zijn gekoppeld aan afmetingen.

Om metrisch aan een project in Analysis Workspace toe te voegen:

1. Begin metrisch aan uw project in Analysis Workspace toe te voegen, zoals die in [&#x200B; wordt beschreven voegt componenten aan een project &#x200B;](#add-components-to-a-project) toe.



1. Kies een van de volgende methoden om metrisch toe te voegen in Analysis Workspace:

   ![&#x200B; Toevoegend metrisch &#x200B;](/help/components/assets/add-metric.gif)

   * Sleep metrisch aan de metrische dalingsstreek in een lege lijst Freeform om te zien dat metrisch over de de datumperiode van het project trended.

   * Sleep metrisch wanneer een afmeting aanwezig is om dat metrisch voor elk afmetingspunt te zien.

   * Sleep metrisch bovenop een bestaande metrische kopbal om het te vervangen.

   * Sleep metrisch naast de linkerzijde van juiste kant van een bestaande metrische kopbal om nieuwe metrisch toe te voegen.

   * Sleep metrische boven of onder een bestaande metrische kopbal om metrische overlapping tot stand te brengen.


Voor meer informatie over metriek, zie [&#x200B; Metriek &#x200B;](/help/components/apply-create-metrics.md).

### Segmenten toevoegen aan een project

[&#x200B; Segmenten &#x200B;](/help/components/segments/seg-overview.md) staan u toe om ondergroepen van personen, zittingen of gebeurtenissen te identificeren die op kenmerken of specifieke interactie worden gebaseerd.

U kunt segmenten in Analysis Workspace op de volgende manieren gebruiken:

* Segmenten toevoegen aan een deelvenster
Wanneer u segmenten toevoegt aan een deelvenster, worden de segmenten toegepast op alle inhoud in het deelvenster.
Voor informatie over hoe u de sectie van de segmentdaling op een paneel kunt gebruiken om uw paneel te segmenteren, zie [&#x200B; de streek van de Daling &#x200B;](/help/analysis-workspace/c-panels/panels.md#drop-zone) in [&#x200B; Overzicht van Comités &#x200B;](/help/analysis-workspace/c-panels/panels.md).

* Segmenten toevoegen aan een visualisatie
Wanneer u segmenten aan een kolom in een vrije-vormlijst toevoegt, zijn de segmenten op alle inhoud binnen de lijstkolom van toepassing. U kunt segmenten ook toevoegen als onderdeel van een uitvalvisualisatie.

* Segmenten in componenten gebruiken
Wanneer u componenten zoals [&#x200B; berekende metriek &#x200B;](/help/components/calc-metrics/cm-workflow/metrics-with-segments.md) bepaalt, [&#x200B; annotaties &#x200B;](/help/components/annotations/create-annotations.md#annotation-builder), of zelfs [&#x200B; segmenten &#x200B;](/help/components/segments/seg-builder.md) kunt u segmenten als deel van de definitie gebruiken.


### Datumbereiken toevoegen aan een project

[&#x200B; de waaiers van de Datum &#x200B;](/help/components/date-ranges/overview.md) bepalen het rapporteringstijdkader in Analysis Workspace, en kunnen op één of meerdere panelen binnen een project en ook op sommige visualisaties (zoals de lijst Freeform) worden toegepast.

Elk deelvenster bevat standaard een datumbereik. Er zijn meerdere manieren om een datumbereik voor een deelvenster bij te werken. Een manier om een datumbereik voor een deelvenster in Analysis Workspace bij te werken, is door een component met een datumbereik uit het linkerdeelvenster te slepen:

1. Naar keuze, voeg een datumwaaier aan uw project in Analysis Workspace toe, zoals die in [&#x200B; wordt beschreven voegt componenten aan een project &#x200B;](#add-components-to-a-project) toe.

1. Sleep een datumbereik van het linkerdeelvenster naar:

   * Het huidige datumbereik om het datumbereik voor het deelvenster te wijzigen.

     ![&#x200B; Daling een datumwaaier &#x200B;](assets/add-date-range.gif)

   * Een metrische of afmeting in de visualisatie van een Freeform-tabel. Zie [&#x200B; de datumwaaiers van het Gebruik &#x200B;](/help/components/date-ranges/overview.md#use-date-ranges) voor meer informatie.

Voor meer informatie over hoe te om datumwaaiers in Analysis Workspace te gebruiken en te beheren, zie [&#x200B; overzicht van de waaiers van de Datum &#x200B;](/help/components/date-ranges/overview.md).

## Componentinformatie

U kunt over om het even welke component bewegen om ![&#x200B; Meer info &#x200B;](/help/assets/icons/InfoOutline.svg) te tonen. Als deze optie is geselecteerd, wordt een pop-up weergegeven met aanvullende informatie over de component.

![&#x200B; Info van de Component &#x200B;](assets/component-info.png)

Gebaseerd op uw toegangsbeheer, kunt u:

* Heb toegang tot de ![&#x200B; 2&rbrace; definitie van de Bladwijzer &#x200B;](/help/assets/icons/Bookmark.svg) &lbrace;voor de component.[!UICONTROL Data dictionary]
* Heb toegang ![&#x200B; uitgeeft &#x200B;](/help/assets/icons/Edit.svg) componentenbouwer of gegevensmening waar de component wordt bepaald.
