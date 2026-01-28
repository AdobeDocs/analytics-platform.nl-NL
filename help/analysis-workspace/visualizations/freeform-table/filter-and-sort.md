---
description: Leer hoe u vrije-vormtabellen kunt filteren en sorteren in Analysis Workspace.
title: Filter en sorteren
feature: Visualizations
exl-id: 3af637ec-bb6c-49b7-a7b3-e1d310e71101
role: User
source-git-commit: e51dced9ac7886ae8d087ca3b2fc6ac2755c3ac6
workflow-type: tm+mt
source-wordcount: '1538'
ht-degree: 0%

---

# Vrije-vormtabellen filteren en sorteren

Vrije-vormtabellen in Analysis Workspace vormen de basis voor interactieve gegevensanalyse. Als zodanig kunnen ze duizenden rijen informatie bevatten. Het filteren en sorteren van de gegevens kan een essentieel onderdeel zijn van het efficiënt opzoeken van de belangrijkste informatie.

<!--The following video covers filter and sort options in Analysis Workspace, in addition to pagination options:

>[!VIDEO](https://video.tv.adobe.com/v/23968)-->

## Filtertabellen

Met filters in Analysis Workspace kunt u de belangrijkste informatie doornemen.

>[!NOTE]
>
> Alleen items met een dynamische dimensie kunnen worden gefilterd zoals in deze sectie wordt beschreven. Statische dimensie-items kunnen niet worden gefilterd. Voor meer informatie, zie [ Dynamische versus statische afmetingspunten in vrije vormlijsten ](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md).

U kunt verschillende methoden gebruiken om rijen vanuit een vrije-vormtabel te filteren.

* Specifieke rijen uitsluiten van een tabel
* Filters toepassen op een tabel
* publiekssegmenten gebruiken

Ben zeker om te lezen hoe elke methode [ vrije lijsttotalen ](/help/analysis-workspace/visualizations/freeform-table/workspace-totals.md) beïnvloedt.

### Specifieke rijen uitsluiten van een tabel

U kunt specifieke rijen van de lijst zonder de behoefte snel uitsluiten om ![ Filter ](/help/assets/icons/Filter.svg) **[!UICONTROL Filter]** te gebruiken.

>[!NOTE]
>
>Wanneer u rijen uitsluit zoals beschreven in deze sectie, wordt automatisch een [!UICONTROL Always exclude items] regel toegevoegd in het [!UICONTROL Advanced] filterdialoogvenster. U kunt de toegepaste regel bekijken door het ![ pictogram van de Filter ](/help/assets/icons/Filter.svg) van de Filter, toen [**[!UICONTROL Show advanced]**](#apply-a-simple-or-advanced-filter-to-a-table) te selecteren.

Specifieke rijen uitsluiten van een vrije-vormlijst:

1. Beweeg over de rij die u wilt uitsluiten, dan selecteren ![ dicht ](/help/assets/icons/Close.svg).

   Houd de ***sleutel van de Verschuiving*** {om een waaier van rijen te selecteren, of houd de ***3} sleutel van het Bevel (op Mac) of*** CTRL ***(op Vensters) om veelvoudige rijen te selecteren.***

<!--### Right-click > Delete selected rows

Note: this option does not seem to work. AN-338422

1. Select 1 or more rows. 
1. Right-click and select **[!UICONTROL Delete Selected Rows]**. 

   This action will remove the rows from the table and apply a table filter.-->


### Eenvoudige of geavanceerde filters toepassen op een tabel

Gegevens filteren in vrije-vormtabellen:

1. Houd de muisaanwijzer boven de kolom met de gegevens die u wilt filteren. <!--only some types of columns show the filter... Which? Just Dimensions?-->

1. Selecteer ![ Filter ](/help/assets/icons/Filter.svg) **Filter** wanneer het verschijnt.

   ![ vrije lijst die het pictogram van de Filter benadrukt.](assets/table-filter-icon.png)

   De volgende opties zijn beschikbaar in het dialoogvenster **[!UICONTROL Search]** :

   ![ Eenvoudige Filter ](assets/filter-simple.png){width="500"}

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **omvat &quot;Geen waarde&quot;**] | Selecteer deze optie om een **[!UICONTROL No value]** rij in de tabel weer te geven voor gegevens die geen waarde hebben voor de geselecteerde dimensie. Schakel deze optie uit als u de **[!UICONTROL No value]** -rijen wilt verbergen. <!-- Add at multi dim GA: When tables include multiple dimension columns, you can deselect this option to show data only when it applies to each dimension column in the table.--> |
   | [!UICONTROL **woord of uitdrukking van het Onderzoek**] | Geef een woord of woordgroep op waarop u wilt filteren. Alleen rijen die het opgegeven woord of de exacte woordgroep bevatten, worden weergegeven. |


1. (Facultatief) om door verschillende criteria of door veelvoudige criteria te filtreren, uitgezochte [!UICONTROL **toont geavanceerd**].

   De volgende geavanceerde filteropties zijn beschikbaar:

   ![ Eenvoudige Filter ](assets/filter-advanced.png){width=500}

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **omvat &quot;Geen waarde&quot;**] | Selecteer deze optie om een **[!UICONTROL No value]** rij in de tabel weer te geven voor gegevens die geen waarde hebben voor de geselecteerde dimensie. Schakel deze optie uit als u de **[!UICONTROL No value]** -rij wilt verbergen. |
   | [!UICONTROL **Gelijke**] | Kies [!UICONTROL **als alle criteria**] worden voldaan om slechts gegevens te tonen die aan alle criteria voldoen die u specificeert. Deze optie resulteert doorgaans in meer verfijnde gegevens.<br/><br/> kies [!UICONTROL **als om het even welke criteria**] worden voldaan om gegevens te tonen die aan om het even welke filtercriteria voldoen die u specificeert. Deze optie resulteert doorgaans in minder verfijnde gegevens. |
   | [!UICONTROL **Criteria**] | Selecteer een van de volgende filteropties:<br/><ul><li>[!UICONTROL **bevat de uitdrukking**] (gebrek): Slechts gegevens die de nauwkeurige uitdrukking bevatten die u specificeert zijn inbegrepen in de gefiltreerde resultaten. De woorden moeten in de orde zijn die in het [!UICONTROL **wordt gespecificeerd woord of woordgebied van het Onderzoek**].</li><li>[!UICONTROL **bevat om het even welke termijn**]: Slechts gegevens die één of meerdere woorden van de uitdrukking bevatten die u specificeert zijn inbegrepen in de gefiltreerde resultaten. </li><li>[!UICONTROL **bevat alle termijnen**]: Slechts gegevens die alle woorden van de uitdrukking bevatten die u specificeert zijn inbegrepen in de gefiltreerde resultaten. De woorden moeten niet in de orde zijn die in het [!UICONTROL **wordt gespecificeerd woord of woordgebied van het Onderzoek**].</li><li>[!UICONTROL **bevat geen termijn**]: Slechts gegevens die geen van de woorden van de uitdrukking bevatten die u specificeert zijn inbegrepen in de gefiltreerde resultaten. </li><li>[!UICONTROL **bevat niet de uitdrukking**]: Slechts gegevens die niet de nauwkeurige uitdrukking bevatten die u specificeert zijn inbegrepen in de gefiltreerde resultaten. De woorden moeten in de orde zijn die in het [!UICONTROL **wordt gespecificeerd woord of woordgebied van het Onderzoek**].</li><li>[!UICONTROL **evenaart**]: Slechts gegevens die precies de uitdrukking aanpassen die u specificeert is inbegrepen in de gefiltreerde resultaten. </li><li>[!UICONTROL **is niet gelijk**]: Slechts gegevens die niet precies de uitdrukking aanpassen die u specificeert zijn inbegrepen in de gefilterde resultaten. </li><li>[!UICONTROL **begint met**]: Slechts gegevens die met het woord of de nauwkeurige uitdrukking beginnen die u specificeert zijn inbegrepen in de gefiltreerde resultaten. </li><li>[!UICONTROL **eindigt met**]: Slechts gegevens die met het woord of de nauwkeurige uitdrukking beëindigen die u specificeert zijn inbegrepen in de gefiltreerde resultaten. </li></ul>Selecteer ![ toevoegen ](/help/assets/icons/Add.svg) [!UICONTROL **rij**] om veelvoudige filtercriteria toe te voegen. De optie u voor [!UICONTROL **selecteert Gelijke**] bepaalt **[!UICONTROL If all criteria are met]** of **[!UICONTROL If any criteria are met]**. |
   | [!UICONTROL **sluit altijd punten**] uit | Geef de naam op van de items die u wilt uitsluiten van de gefilterde gegevens. |

1. Selecteer **[!UICONTROL Apply]** om de gegevens te filteren. Selecteer **[!UICONTROL Clear]** om alle invoer te wissen. Selecteer **[!UICONTROL Cancel]** om het dialoogvenster te annuleren en te sluiten. <br/> een gekleurde ![ Filter ](/help/assets/icons/FilterColored.svg) **pictogram van de Filter** wijst op en toont details wanneer een filter op de lijst wordt toegepast.

### Filtercriteria opnemen in trended-gegevens in sparklines en lijnvisualisaties {#include-filter-criteria}

Alle zoekfiltercriteria die worden toegepast op de tabeldimensie op een vrije-vormtabel, worden altijd opgenomen in de sparklines.

Naast sparklines, kunt u filtercriteria vormen om in verbonden lijnvisualisaties worden omvat. (Filtercriteria worden standaard niet opgenomen in lijnvisualisaties. De visualisaties van de lijn tonen gegevens voor de rij die in de verbonden lijst wordt geselecteerd. Als er geen rij is geselecteerd, worden alleen gegevens voor de eerste afmeting van de verbonden tabel weergegeven.)

Voor meer informatie over sparklines en lijnvisualisaties, zie [ Gedetailleerde gegevens van de Mening voor een vrije vormlijst ](/help/analysis-workspace/visualizations/freeform-table/freeform-table-trended-data.md).

#### Vorm lijnvisualisaties om filtercriteria te omvatten

1. Selecteer de sparkline in de metrische kolomkop.

   Als de dunne cel is geselecteerd, wordt deze weergegeven als donkergrijs. Dit wijst erop dat de filtercriteria in de verbonden lijnvisualisatie inbegrepen zijn. De filtercriteria worden toegepast als een segment in de kolom. <!--show how to see it? Show what the segment looks like when it's applied? -->

   ![ geselecteerde sparkline ](assets/table-sparkline-selected.png)

#### Begrijp wanneer de kolomtotalen onnauwkeurig zouden kunnen zijn

De totalen van kolommen zijn mogelijk niet exact in de volgende scenario&#39;s:

* Wanneer de statische componenten in de linkerkolom worden gebruikt en [ kolomtotalen worden berekend als som rijen ](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)

  Als de rijpunten overlappende gegevens in dit scenario bevatten, zullen de kolomtotalen onnauwkeurig zijn.

  Bijvoorbeeld, als u statische segmenten aan de linkerkolom toevoegt, en dan voegt u Gebruikers als metrisch in de juiste kolom toe, zouden sommige van die gebruikers deel van meer dan één van de statische segmenten kunnen uitmaken. In dit geval dedupliceert Workspace de gebruikers niet voor elk statisch segment. Dit kan resulteren in een hoger aantal gebruikers in totaal, omdat sommige gebruikers meer dan één keer kunnen worden geteld.

* Bij het gebruik van multi-getaxeerde afmetingen

>[!NOTE]
>
>De sparkline- en lijngrafiek weerspiegelen nog steeds de nauwkeurige totalen in deze scenario&#39;s.

### publiekssegmenten gebruiken

Zie [ Overzicht van de Segmentatie ](/help/components/segments/seg-overview.md) voor meer details.

## Tabellen sorteren

In Analysis Workspace kunt u de gegevens van een vrije-vormlijst door om het even welke kolommen sorteren, of zij dimensies of metriek zijn. U kunt zelfs op meerdere kolommen tegelijk sorteren.

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