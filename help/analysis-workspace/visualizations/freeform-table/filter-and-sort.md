---
description: Leer hoe u vrije-vormtabellen kunt filteren en sorteren in Analysis Workspace.
title: Filter en sorteren
feature: Visualizations
exl-id: 3af637ec-bb6c-49b7-a7b3-e1d310e71101
role: User
source-git-commit: a16043f1bb15deba1332ed39438214597647b9b4
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 0%

---

# Filteren en sorteren

Vrije-vormtabellen in Analysis Workspace vormen de basis voor interactieve gegevensanalyse. Als zodanig kunnen ze duizenden rijen informatie bevatten. Het filteren en sorteren van de gegevens kan een essentieel onderdeel zijn van het efficiënt opzoeken van de belangrijkste informatie.

<!--The following video covers filter and sort options in Analysis Workspace, in addition to pagination options:

>[!VIDEO](https://video.tv.adobe.com/v/23968)-->

## Filtertabellen

Met filters in Analysis Workspace kunt u de belangrijkste informatie doornemen.

>[!NOTE]
>
> Alleen items met een dynamische dimensie kunnen worden gefilterd zoals in deze sectie wordt beschreven. Statische dimensie-items kunnen niet worden gefilterd. Voor meer informatie, zie [&#x200B; Dynamische versus statische afmetingspunten in vrije vormlijsten &#x200B;](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md).

U kunt verschillende methoden gebruiken om rijen vanuit een vrije-vormtabel te filteren.

* Specifieke rijen uitsluiten van een tabel
* Filters toepassen op een tabel
* publiekssegmenten gebruiken

Ben zeker om te lezen hoe elke methode [&#x200B; Gratis lijsttotalen &#x200B;](/help/analysis-workspace/visualizations/freeform-table/workspace-totals.md) beïnvloedt.

### Specifieke rijen uitsluiten van een tabel

U kunt specifieke rijen van de lijst zonder de behoefte snel uitsluiten om ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) **[!UICONTROL Filter]** te gebruiken.

>[!NOTE]
>
>Wanneer u rijen uitsluit zoals beschreven in deze sectie, wordt automatisch een [!UICONTROL Always exclude items] regel toegevoegd in het [!UICONTROL Advanced] filterdialoogvenster. U kunt de toegepaste regel bekijken door het ![&#x200B; pictogram van de Filter &#x200B;](/help/assets/icons/Filter.svg) van de Filter, toen [**[!UICONTROL Show advanced]**](#apply-a-simple-or-advanced-filter-to-a-table) te selecteren.

Specifieke rijen uitsluiten van een tabel voor vrije vorm:

1. Beweeg over de rij die u wilt uitsluiten, dan selecteren ![&#x200B; dicht &#x200B;](/help/assets/icons/Close.svg).

   Houd de ***verschuiving*** om een waaier van rijen te selecteren, of houd de ***cmd*** sleutel (op Mac) of de ***ctrl*** sleutel (op Vensters) om veelvoudige rijen te selecteren.

<!--### Right-click > Delete selected rows

Note: this option does not seem to work. AN-338422

1. Select 1 or more rows. 
1. Right-click and select **[!UICONTROL Delete Selected Rows]**. 

   This action will remove the rows from the table and apply a table filter.-->


### Een eenvoudig of geavanceerd filter toepassen op een tabel

Gegevens filteren in Freeform-tabellen:

1. Houd de muisaanwijzer boven de kolom met de gegevens die u wilt filteren. <!--only some types of columns show the filter... Which? Just Dimensions?-->

1. Selecteer ![&#x200B; Filter &#x200B;](/help/assets/icons/Filter.svg) **Filter** wanneer het verschijnt.

   ![&#x200B; vrije lijst die het pictogram van de Filter benadrukt.](assets/table-filter-icon.png)

   De volgende opties zijn beschikbaar in het dialoogvenster **[!UICONTROL Search]** :

   ![&#x200B; Eenvoudige Filter &#x200B;](assets/filter-simple.png){width="500"}

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **omvat &quot;Geen waarde&quot;**] | Selecteer deze optie om een **[!UICONTROL No value]** rij in de tabel weer te geven voor gegevens die geen waarde hebben voor de geselecteerde dimensie. Schakel deze optie uit als u de **[!UICONTROL No value]** -rij wilt verbergen. |
   | [!UICONTROL **woord of uitdrukking van het Onderzoek**] | Geef een woord of woordgroep op waarop u wilt filteren. Alleen rijen die het opgegeven woord of de exacte woordgroep bevatten, worden weergegeven. |


1. (Facultatief) om door verschillende criteria of door veelvoudige criteria te filtreren, uitgezochte [!UICONTROL **toont geavanceerd**].

   De volgende geavanceerde filteropties zijn beschikbaar:

   ![&#x200B; Eenvoudige Filter &#x200B;](assets/filter-advanced.png){width=500}

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **omvat &quot;Geen waarde&quot;**] | Selecteer deze optie om een **[!UICONTROL No value]** rij in de tabel weer te geven voor gegevens die geen waarde hebben voor de geselecteerde dimensie. Schakel deze optie uit als u de **[!UICONTROL No value]** -rij wilt verbergen. |
   | [!UICONTROL **Gelijke**] | Kies [!UICONTROL **als alle criteria**] worden voldaan om slechts gegevens te tonen die aan alle criteria voldoen die u specificeert. Deze optie resulteert doorgaans in meer verfijnde gegevens.<br/><br/> kies [!UICONTROL **als om het even welke criteria**] worden voldaan om gegevens te tonen die aan om het even welke filtercriteria voldoen die u specificeert. Deze optie resulteert doorgaans in minder verfijnde gegevens. |
   | [!UICONTROL **Criteria**] | Selecteer een van de volgende filteropties:<br/><ul><li>[!UICONTROL **bevat de uitdrukking**] (gebrek): Slechts gegevens die de nauwkeurige uitdrukking bevatten die u specificeert zijn inbegrepen in de gefiltreerde resultaten. De woorden moeten in de orde zijn die in het [!UICONTROL **wordt gespecificeerd woord of woordgebied van het Onderzoek**].</li><li>[!UICONTROL **bevat om het even welke termijn**]: Slechts gegevens die één of meerdere woorden van de uitdrukking bevatten die u specificeert zijn inbegrepen in de gefiltreerde resultaten. </li><li>[!UICONTROL **bevat alle termijnen**]: Slechts gegevens die alle woorden van de uitdrukking bevatten die u specificeert zijn inbegrepen in de gefiltreerde resultaten. De woorden moeten niet in de orde zijn die in het [!UICONTROL **wordt gespecificeerd woord of woordgebied van het Onderzoek**].</li><li>[!UICONTROL **bevat geen termijn**]: Slechts gegevens die geen van de woorden van de uitdrukking bevatten die u specificeert zijn inbegrepen in de gefiltreerde resultaten. </li><li>[!UICONTROL **bevat niet de uitdrukking**]: Slechts gegevens die niet de nauwkeurige uitdrukking bevatten die u specificeert zijn inbegrepen in de gefiltreerde resultaten. De woorden moeten in de orde zijn die in het [!UICONTROL **wordt gespecificeerd woord of woordgebied van het Onderzoek**].</li><li>[!UICONTROL **evenaart**]: Slechts gegevens die precies de uitdrukking aanpassen die u specificeert is inbegrepen in de gefiltreerde resultaten. </li><li>[!UICONTROL **is niet gelijk**]: Slechts gegevens die niet precies de uitdrukking aanpassen die u specificeert zijn inbegrepen in de gefilterde resultaten. </li><li>[!UICONTROL **begint met**]: Slechts gegevens die met het woord of de nauwkeurige uitdrukking beginnen die u specificeert zijn inbegrepen in de gefiltreerde resultaten. </li><li>[!UICONTROL **eindigt met**]: Slechts gegevens die met het woord of de nauwkeurige uitdrukking beëindigen die u specificeert zijn inbegrepen in de gefiltreerde resultaten. </li></ul>Selecteer ![&#x200B; toevoegen &#x200B;](/help/assets/icons/Add.svg) [!UICONTROL **rij**] om veelvoudige filtercriteria toe te voegen. De optie u voor [!UICONTROL **selecteert Gelijke**] bepaalt **[!UICONTROL If all criteria are met]** of **[!UICONTROL If any criteria are met]**. |
   | [!UICONTROL **sluit altijd punten**] uit | Geef de naam op van de items die u wilt uitsluiten van de gefilterde gegevens. |

1. Selecteer **[!UICONTROL Apply]** om de gegevens te filteren. Selecteer **[!UICONTROL Clear]** om alle invoer te wissen. Selecteer **[!UICONTROL Cancel]** om het dialoogvenster te annuleren en te sluiten. <br/> een gekleurde ![&#x200B; Filter &#x200B;](/help/assets/icons/FilterColored.svg) **pictogram van de Filter** wijst op en toont details wanneer een filter op de lijst wordt toegepast.

### Filtercriteria opnemen in trended-gegevens in sparklines en lijnvisualisaties {#include-filter-criteria}

Alle zoekfiltercriteria die worden toegepast op de tabeldimensie op een vrije-vormtabel, worden altijd opgenomen in de sparklines.

Naast sparklines, kunt u filtercriteria vormen om in verbonden lijnvisualisaties worden omvat. (Filtercriteria worden standaard niet opgenomen in lijnvisualisaties. De visualisaties van de lijn tonen gegevens voor de rij die in de verbonden lijst wordt geselecteerd. Als er geen rij is geselecteerd, worden alleen gegevens voor de eerste afmeting van de verbonden tabel weergegeven.)

Voor meer informatie over sparklines en lijnvisualisaties, zie [&#x200B; Gedetailleerde gegevens van de Mening voor een vrije vormlijst &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table-trended-data.md).

#### Vorm lijnvisualisaties om filtercriteria te omvatten

1. Selecteer de sparkline in de metrische kolomkop.

   Als de dunne cel is geselecteerd, wordt deze weergegeven als donkergrijs. Dit wijst erop dat de filtercriteria in de verbonden lijnvisualisatie inbegrepen zijn. De filtercriteria worden toegepast als een segment in de kolom. <!--show how to see it? Show what the segment looks like when it's applied? -->

   ![&#x200B; geselecteerde sparkline &#x200B;](assets/table-sparkline-selected.png)

#### Begrijp wanneer de kolomtotalen onnauwkeurig zouden kunnen zijn

De totalen van kolommen zijn mogelijk niet exact in de volgende scenario&#39;s:

* Wanneer de statische componenten in de linkerkolom worden gebruikt en [&#x200B; kolomtotalen worden berekend als som rijen &#x200B;](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)

  Als de rijpunten overlappende gegevens in dit scenario bevatten, zullen de kolomtotalen onnauwkeurig zijn.

  Bijvoorbeeld, als u statische segmenten aan de linkerkolom toevoegt, en dan voegt u Gebruikers als metrisch in de juiste kolom toe, zouden sommige van die gebruikers deel van meer dan één van de statische segmenten kunnen uitmaken. In dit geval dedupliceert Workspace de gebruikers niet voor elk statisch segment. Dit kan resulteren in een hoger aantal gebruikers in totaal, omdat sommige gebruikers meer dan één keer kunnen worden geteld.

* Bij het gebruik van multi-getaxeerde afmetingen

>[!NOTE]
>
>De sparkline- en lijngrafiek weerspiegelen nog steeds de nauwkeurige totalen in deze scenario&#39;s.

### publiekssegmenten gebruiken

Zie [&#x200B; Overzicht van de Segmentatie &#x200B;](/help/components/segments/seg-overview.md) voor meer details.

## Tabellen sorteren

U kunt de gegevens van een lijst Freeform door om het even welke kolom in Analysis Workspace sorteren die of een afmeting of metrisch is. Een pijl geeft aan hoe de gegevens worden gesorteerd (**↓** voor aflopend, of **↑** voor oplopend).

![&#x200B; Sorterend &#x200B;](assets/sorting.gif)
