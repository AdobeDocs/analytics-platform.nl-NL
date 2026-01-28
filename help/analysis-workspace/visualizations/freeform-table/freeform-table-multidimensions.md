---
title: Meerdere afmetingen opnemen in een vrije-vormtabel
description: Leer hoe u meerdere afmetingen opneemt in een vrije-vormtabel
feature: Visualizations
role: User
source-git-commit: 696bd0db44949162307d8ce7d2debed351a76cd6
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 0%

---

# Meerdere dimensiekolommen opnemen in een vrije-vormtabel

{{release-limited-testing}}

U kunt tot 5 afmetingskolommen in een vrije vormlijst omvatten, toestaand u om veelvoudige afmeting punten naast elkaar te bekijken. Elke rij van afmetingspunten gedraagt zich als één enkel samengevoegd afmetingspunt.

U kunt filters, het sorteren, het breken, en meer op vrije vormlijsten met veelvoudige afmetingskolommen toepassen om een diepere en meer douaneanalyse tot stand te brengen.

## Samengevoegde dimensie-items

Wanneer u [ veelvoudige afmetingskolommen aan een vrije vormlijst ](#add-multiple-dimension-columns) toevoegt, gedraagt elke rij van afmetingspunten zich als één enkel samengevoegd afmetingspunt. Met deze functionaliteit kunt u metrische gegevens bekijken voor specifieke combinaties van dimensies.

Bijvoorbeeld, overweeg een vrije lijst waar de afmetingskolommen _,_ Type van Apparaat _zijn, en_ Dag van Maand _en metrisch is_ Gebeurtenissen _._ De 3 afmetingspunten in de eerste rij van deze lijst worden één enkel samengevoegd afmetingspunt dat aantoont dat er 2.056 gebeurtenissen waren die in Mumbai van mobiele telefoons op de 30e dag van de maand plaatsvonden.

| Dimension: Plaats | Dimension: apparaattype | Dimension: Dag van Maand | Metrisch: gebeurtenissen |
|---------|----------|---------|---------|
| Mumbai | Mobiele telefoon | 30 | 2.056 |
| New York | Tablet | 31 | 1.761 |
| Bangalore | Desktop | 1 | 1.666 |
| Delhi | Mobiele telefoon | 14 | 1.396 |

Hieronder ziet u hoe deze tabel in Analysis Workspace wordt weergegeven:

![ Multidimensionaal voorbeeld ](assets/multi-dim-example.png)

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

1. Bekijk elke rij van de lijst als één enkel afmetingspunt. Voor meer informatie, zie [ Samengevoegde afmetingspunten ](#concatenated-dimension-items).

## Tabellen filteren en sorteren

U kunt het filtreren en het sorteren op kolommen in een vrije vormlijst toepassen. U kunt de gegevens van een vrije-vormlijst door om het even welke kolommen sorteren, of zij dimensies of metriek zijn. U kunt zelfs op meerdere kolommen tegelijk sorteren.

Voor informatie, zie [ Filter en sorteer vrije vormlijsten ](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).

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

* Verdeel een afmetingspunt in de vrije vormlijst door een secundaire afmeting. U kunt tot 400 afmetingspunten voor de secundaire afmeting tonen.

### Onderverdelingen toevoegen aan een tabel met meerdere afmetingskolommen

Wanneer u een verdeling aan een lijst toevoegt die veelvoudige afmetingskolommen heeft, is de verdeling op het samengevoegde afmetingspunt (over alle afmetingskolommen) op de rij van toepassing waar u het toevoegt.

![ multi-sort verdelingsvoorbeeld ](assets/dimensions-multiple-sort-breakdown.png)

Bovendien kunt u meerdere dimensiekolommen binnen een verdeling toevoegen. Elke rij van afmetingspunten binnen de uitsplitsing gedraagt zich ook als één enkel samengevoegd afmetingspunt.

<!-- Add a screenshot of a breakdown with multiple cllumns, then add this sentence: "For example, you can break down the first dimension item in this table by a new concatenated dimension item that shows..." -->

Voor meer informatie over hoe te om een onderverdeling toe te voegen, zie {de afmetingen van 0} Onderbreking [.](/help/components/dimensions/t-breakdown-fa.md)

## Creeer een segment dat op een afmetingspunt wordt gebaseerd dat veelvoudige afmetingskolommen overspant

Wanneer u een segment creeert dat op een afmetingspunt wordt gebaseerd dat veelvoudige afmetingskolommen overspant, is elk afmetingspunt inbegrepen in de segmentdefinitie, met en exploitanten die hen aansluiten.

Voor informatie over het creëren van een segment, zie [ segmenten ](/help/components/segments/seg-create.md) creëren.

## Niet-ondersteunde afmetingen {#unsupported}

De volgende dimensiecombinaties worden niet ondersteund en Analysis Workspace verbiedt het toevoegen ervan of toont een foutbericht nadat deze zijn toegevoegd:

* De veelvoudige afmetingen die van gebieden zijn die verschillende [ series van voorwerpen ](/help/use-cases/object-arrays.md) van verwijzingen voorzien die samen in de zelfde vrije vormlijst worden gebruikt.

  Meerdere afmetingen zijn samen toegestaan in dezelfde vrije-vormtabel als ze naar dezelfde array van objecten verwijzen.

