---
title: Meerdere afmetingen opnemen in een vrije-vormtabel
description: Leer hoe u meerdere afmetingen opneemt in een vrije-vormtabel
feature: Visualizations
role: User
hide: true
hidefromtoc: true
source-git-commit: ec07eb5dced013eac3d1088f2f49dcea23894395
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 0%

---

# Meerdere dimensiekolommen opnemen in een vrije-vormtabel

{{release-limited-testing}}

U kunt tot 5 afmetingskolommen in een vrije vormlijst omvatten, toestaand u om veelvoudige afmeting punten naast elkaar te bekijken. Elke rij van afmetingspunten doet dienst als één enkel samengevoegd punt.

U kunt filters, het sorteren, de onderverdelingen, en meer op vrije vormlijsten met veelvoudige afmetingskolommen toepassen om een volledigere en douaneanalyse tot stand te brengen.

## Meerdere dimensiekolommen toevoegen

U kunt meerdere dimensiekolommen één voor één of in bulk toevoegen.

1. Maak in Analysis Workspace een vrije-vormtabel.

   Voor meer informatie, zie [ visualisaties aan een paneel ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel) in [ overzicht van Visualisaties ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md) toevoegen.

1. Voeg afmetingen toe aan de vrije-vormlijst. U kunt de afmetingen een voor een toevoegen of u kunt meerdere afmetingen tegelijk toevoegen.

   * Sleep de afmetingen een voor een naar de vrije-vormtabel. Plaats extra afmetingskolommen links of rechts van bestaande afmetingskolommen in de tabel. Een blauwe verticale **[!UICONTROL Add]** lijn geeft aan waar de nieuwe kolom wordt gemaakt.

     ![ belemmering individuele afmetingen ](assets/dimensions-add-individually.png)

   * Selecteer maximaal 5 dimensies in het deelvenstermenu en sleep ze naar de vrije-vormtabel. Dimensies worden van links naar rechts aan de tabel toegevoegd in de volgorde waarin u ze selecteert.

     Om veelvoudige afmetingen te selecteren, houd de ***sleutel van het Bevel*** (op Mac) of de ***sleutel van CTRL*** (op Vensters).

     ![ belemmering veelvoudige afmetingen ](assets/dimensions-add-multiple.png)

## Filtertabellen

U kunt filters op één of meerdere afmetingskolommen in een vrije vormlijst toepassen.

Voor informatie over het filtreren van lijsten, zie {de lijsten van de Filter [ in ](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md#filter-tables) Filter en sorteerlijsten [.](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md)

## Tabellen sorteren {#sort-tables}

<!--At GA, move this section into the "Filter and sort tables" article and replace the current "Sort tables" section. Change the "Filter tables" section above to "Filter and sort tables" and link to the other article. Also add row to Guardrails -->

U kunt de gegevens van een vrije-vormlijst door om het even welke kolommen in Analysis Workspace sorteren, of zij dimensies of metriek zijn.

Standaard worden de afmetingen in oplopende volgorde gesorteerd en worden de cijfers in aflopende volgorde gesorteerd.

### Tabellen sorteren op één kolom

Wanneer u gegevens voor één enkele kolom zoals die in deze sectie wordt beschreven sorteert, wordt om het even welk [ geavanceerd sorteren ](#sort-tables-by-multiple-columns-advanced-sorting) die op de lijst wordt toegepast verwijderd.

Gegevens in tabellen sorteren op één kolom:

1. De muis over de kopbal van de kolom u wilt sorteren, dan de **pictogram van de Soort** Soort ![ selecteren wanneer het verschijnt.](/help/assets/icons/SortOrderDown.svg)

   ![ Soort drop-down menu ](assets/sort-dropdown-menu.png)

1. Selecteer **[!UICONTROL Ascending]** of **[!UICONTROL Descending]** .

   Het sorteerpictogram blijft zichtbaar wanneer het sorteren wordt toegepast op de kolom. Een pijl wijst erop hoe het gegeven wordt gesorteerd (![ Soort ](/help/assets/icons/SortOrderUp.svg) voor het stijgen of ![ Soort ](/help/assets/icons/SortOrderDown.svg) voor het dalen).

### Tabellen sorteren op meerdere kolommen (geavanceerd sorteren)

{{release-limited-testing-section}}

#### Sorteren toepassen op meerdere kolommen

Gegevens in tabellen sorteren op meerdere kolommen:

1. De muis over de kopbal van om het even welke kolom die u wilt sorteren, selecteert dan de **pictogram van de Soort** Soort ![ wanneer het verschijnt.](/help/assets/icons/SortOrderDown.svg)

   ![ Soort drop-down menu ](assets/sort-dropdown-menu.png)

1. Selecteer **[!UICONTROL Advanced sorting]**.

   ![ Geavanceerde sorterende dialoog ](assets/sort-advanced-dialog.png)

1. Voer in het dialoogvenster Geavanceerd sorteren een van de volgende handelingen uit:

   * U kunt kolommen toevoegen die nog niet worden gesorteerd door de knop **[!UICONTROL Add sort column]** te selecteren.

   * Verwijder kolommen die u niet meer wilt sorteren door **te selecteren verwijder** pictogram ![ ](/help/assets/icons/Close.svg) verwijdert.

   * Sleep kolommen hoger of lager in de lijst om de sorteerprioriteit aan te passen.

     Voor meer informatie, zie [ prioriteit van de Soort ](#sort-priority).

   * Wijzig de sorteerwaarde door **[!UICONTROL Ascending]** of **[!UICONTROL Descending]** te selecteren in de vervolgkeuzelijst.

   * Selecteer een andere kolom door de kolomnaam drop-down menu te selecteren.

1. Selecteer **[!UICONTROL Apply]**.

Het sorteerpictogram blijft zichtbaar wanneer het sorteren wordt toegepast op een kolom. Een pijl wijst erop hoe het gegeven wordt gesorteerd (![ Soort ](/help/assets/icons/SortOrderUp.svg) voor het stijgen of ![ Soort ](/help/assets/icons/SortOrderDown.svg) voor het dalen).

![ multi-sort voorbeeld ](assets/dimensions-multiple-sort.png)

#### Sorteerprioriteit

Wanneer u gegevens voor meerdere kolommen sorteert, worden de gegevens gesorteerd op basis van de prioriteit die u aan elke kolom toewijst. De prioritaire nummering wordt getoond naast het de rangschikkingsprioritaire pictogram van het soortpictogram ![ ](assets/sort-priority-icon.png).

De kolom met de primaire prioriteit bepaalt de hoofdorde; de kolom met de secundaire prioriteit beslist de orde wanneer de rijen de zelfde waarde in de primaire kolom hebben; de kolom met de tertiaire prioriteit beslist de orde wanneer de rijen de zelfde waarde in de primaire en secundaire kolommen hebben; etc.

Neem bijvoorbeeld een tabel met de volgende kolommen:

* Dag van de maand (afmeting)

* Uur van de dag (afmeting)

* Gebeurtenissen (metrisch)

U kunt als volgt een sorteerprioriteit aan elke kolom toewijzen:

| Naam kolom (component) | Componenttype | Sorteerprioriteit |
|---------|----------|---------|
| Dag van Maand | Dimension | 1 |
| Uur van de dag | Dimension | 2 |
| Gebeurtenissen | Metrisch | 3 |

Door een sorteerprioriteit toe te wijzen aan elke kolom, kunt u precies bepalen hoe de gegevens in de lijst worden getoond. In dit voorbeeld wordt de informatie eerst gesorteerd op Dag van Maand, vervolgens op Uur van Dag en ten slotte op Gebeurtenissen.

![ multi-sort voorbeeld ](assets/dimensions-multiple-sort.png)

## Kolommen en onderverdelingen met meerdere dimensies

Analysis Workspace biedt de volgende manieren om meerdere afmetingen toe te voegen binnen een vrije-vormtabel:

* Meerdere dimensiekolommen opnemen (zoals beschreven in dit artikel)

* [Uitsplitsingen toevoegen](/help/components/dimensions/t-breakdown-fa.md)

Met beide methoden kunt u dimensies analyseren op basis van andere afmetingen. Er zijn echter belangrijke verschillen en beide methoden kunnen in dezelfde tabel worden gebruikt voor een nog diepere analyse.

### Verschillen tussen dimensiekolommen en uitsplitsingen

Met meerdere dimensiekolommen kunt u:

* Dimensie-items samenvoegen tot afzonderlijke rijen met gegevens in meerdere dimensies.

* Omvat afmetingspunten in samengevoegde rijen slechts wanneer de afmetingspunten op elke afmetingskolom in de lijst van toepassing zijn. Hiertoe deselecteert u met het kolomfilter de instelling **[!UICONTROL Include "No value"]** voor elke dimensiekolom.

  Voor meer informatie, zie [ de lijsten van de Soort door veelvoudige kolommen (het Geavanceerde sorteren) ](#sort-tables-by-multiple-columns-advanced-sorting).

* De gegevens van de soort door veelvoudige afmeting en metrische kolommen om meer aangepaste gegevens te zien.

  Voor meer informatie, zie [ de lijsten van de Soort door veelvoudige kolommen (het Geavanceerde sorteren) ](#sort-tables-by-multiple-columns-advanced-sorting)

Met indelingen kunt u:

* Verdeel een afmetingspunt in de vrije vormlijst door een secundaire afmeting. U kunt tot 200 afmetingspunten voor de secundaire afmeting tonen.

### Onderverdelingen toevoegen aan een tabel met meerdere afmetingskolommen

Wanneer u een uitsplitsing toevoegt aan een tabel met meerdere afmetingskolommen, omvat de uitsplitsing alle afmetingsitems op de rij waar u deze toevoegt.

U kunt een onderbreking toevoegen zoals die in [ wordt beschreven onderbreking dimensies ](/help/components/dimensions/t-breakdown-fa.md).

## Niet-ondersteunde afmetingen {#unsupported}

De volgende dimensiecombinaties worden niet ondersteund en Analysis Workspace verbiedt het toevoegen ervan of toont een foutbericht nadat deze zijn toegevoegd:

* De veelvoudige afmetingen die van gebieden zijn die verschillende [ series van voorwerpen ](/help/use-cases/object-arrays.md) van verwijzingen voorzien die samen in de zelfde vrije vormlijst worden gebruikt.

  Meerdere afmetingen zijn samen toegestaan in dezelfde vrije-vormtabel als ze naar dezelfde array van objecten verwijzen.