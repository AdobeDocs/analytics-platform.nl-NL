---
description: Leer hoe u trended-gegevens voor een vrije-vormentabel in Analysis Workspace bekijkt.
title: Getrafte gegevens voor een vrije-vormlijst weergeven
feature: Freeform Tables
role: User, Admin
source-git-commit: 6ffc02c537a5e0b24edab34c87866d5c8413ae6f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Getrafte gegevens voor een vrije-vormlijst weergeven

U kunt de trend van de gegevens bekijken die in een vrije vormlijst inbegrepen is. Deze trended-gegevens worden weergegeven in de volgende gebieden in Analysis Workspace:

* [Sparklines](#use-sparklines-to-view-trended-data)

* [Lijnvisualisatie](#use-line-visualizations-to-view-trended-data)

## Gebruik sparklines om trendgegevens weer te geven

In de kolomkop van vrije-vormtabellen wordt aangegeven hoe u de lijnen in de metrische kolom maakt.

![&#x200B; sparkline in vrije vormlijst &#x200B;](assets/table-sparkline.png)

De reservekopieën zijn altijd:

* Gedetailleerde gegevens voor alle gegevens in de kolom

* Alle zoekfiltercriteria die worden toegepast op de tabelafmetingen

  Voor meer informatie, zie [&#x200B; Filter en soort &#x200B;](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).

## Lijnvisualisaties gebruiken om trendgegevens weer te geven

[&#x200B; visualisaties van de Lijn &#x200B;](/help/analysis-workspace/visualizations/line.md) tonen de gegevens van de vrije vormlijst zij met worden verbonden.

### Verbind een lijnvisualisatie met een vrije vormlijst

Afhankelijk van hoe en wanneer de lijnvisualisatie aan het project werd toegevoegd, zou het reeds met de gewenste vrije vormlijst kunnen worden verbonden. Gebruik de volgende stappen om het te controleren of manueel te verbinden:

1. Voeg een lijnvisualisatie aan een project van Analysis Workspace toe.

1. Selecteer de punt naast de visualisatienaam, selecteer het **[!UICONTROL Data source]** lusje, dan selecteer de naam van de vrije vormlijst die u met de lijnvisualisatie wilt verbinden.

   ![&#x200B; lijn visualisatie die met vrije vormlijsten &#x200B;](assets/table-line-viz.png) wordt verbonden

### Kies de gegevens die zijn opgenomen in de lijnvisualisatie

De gegevens die in de verbonden lijnvisualisatie zijn opgenomen, variëren afhankelijk van de cel die in de vrije-vormlijst is geselecteerd.

Om een trend van alle gegevens in de vrije vormlijst te bekijken, selecteer de sparkline cel in de vrije vormlijst.

Als de dunne cel is geselecteerd, wordt de cel weergegeven als donkergrijs.

![&#x200B; geselecteerde sparkline &#x200B;](assets/table-sparkline-selected.png)

Als de dunne cel van de verbonden tabel is geselecteerd, worden onder andere de volgende lijnen weergegeven:

* Gedetailleerde gegevens voor alle gegevens in de kolom

* Alle zoekfiltercriteria die worden toegepast op de tabelafmetingen

  Voor meer informatie, zie [&#x200B; Filter en soort &#x200B;](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).

Wanneer de dunne lijn van de verbonden lijst niet wordt geselecteerd, omvatten de lijnvisualisaties:

* Gegevens voor de rij die in de verbonden lijst wordt geselecteerd. Als er geen rij is geselecteerd, worden alleen gegevens voor de eerste afmeting van de verbonden tabel weergegeven.

* Alle zoekfiltercriteria die op de tabelafmetingen worden toegepast, worden genegeerd

  Voor meer informatie, zie [&#x200B; Filter en soort &#x200B;](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).


## Filtercriteria opnemen in de weergave van verbonden lijnen

Voor informatie over wanneer de filtercriteria in verbonden lijnvisualisaties inbegrepen zijn, zie [&#x200B; omvatten filtercriteria in trended gegevens in vonklines en lijnvisualisaties &#x200B;](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md#include-filter-criteria-in-trended-data-in-sparklines-and-line-visualizations)

