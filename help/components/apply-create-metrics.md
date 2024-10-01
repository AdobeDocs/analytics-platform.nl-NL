---
description: Er zijn twee manieren om metriek in Analysis Workspace te gebruiken.
title: Metrics
feature: Metrics
exl-id: 4edfb5d7-da20-4bd8-8041-387b291daf96
role: User
source-git-commit: 5b441472a21db99728d012c19f12d98f984086f5
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# Metrics

Met cijfers kunt u gegevenspunten in Analysis Workspace kwantificeren. Deze worden meestal gebruikt als kolommen in een visualisatie en zijn gekoppeld aan afmetingen.

## Soorten metingen

De Adobe biedt verscheidene types van metriek voor gebruik in Analysis Workspace aan:


* **Standaard metriek**: Voorbeeld van standaardmetriek zijn Mensen, Zittingen, Gebeurtenissen.

* **Berekende metriek** ![ calculator ](/help/assets/icons/Calculator.svg): Gebruiker-bepaalde metriek die op standaardmetriek, statische aantallen, of algoritmische functies gebaseerd zijn.

* **Berekende metrische malplaatjes** ![ AdobeLogoSmall ](/help/assets/icons/AdobeLogoSmall.svg) : Adobe-bepaalde metriek die zich zo ook aan berekende metriek gedragen. U kunt ze ongewijzigd gebruiken in Workspace-projecten of een kopie opslaan om de logica aan te passen.

U kunt zien of metrisch wordt goedgekeurd ![ Goedgekeurd pictogram ](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg) of niet. Als u meer details op metrisch wilt, beweegt over metrisch, en selecteert ![ pictogram van Info ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg). Zie [ Info van de Component ](use-components-in-workspace.md#component-info) voor meer informatie.



## Metriek gebruiken in Analysis Workspace

Metriek is flexibel in het gebruik binnen Analysis Workspace. Sleep metrisch aan een lege lijst Freeform om te zien die metrisch over de de datumperiode van het project trended. U kunt metrisch ook slepen wanneer een afmeting aanwezig is om dat metrisch vergeleken bij elk afmetingspunt te zien. Als u een metrische waarde boven op een bestaande metrische koptekst sleept, wordt deze vervangen en als u een metrische waarde naast een koptekst sleept, ziet u beide meetgegevens naast elkaar.

Voor informatie over hoe te om metriek en andere soorten componenten aan Analysis Workspace toe te voegen, zie [ de componenten van het Gebruik in Analysis Workspace ](/help/components/use-components-in-workspace.md).

## Berekende cijfers

Met de berekende metriek kunt u eenvoudig configureren hoe de metriek met elkaar verwant is door eenvoudige operatoren of statistische functies te gebruiken. Zie [ Berekend metriek overzicht ](/help/components/calc-metrics/calc-metr-overview.md) voor meer informatie.

<!--

There are several ways to create calculated metrics. See [Create calculated metrics]()

### Create calculated metrics for all projects

You can use the calculated metric builder to create calculated metrics. When created in this way, calculated metrics are available in the component list and can then be used in projects throughout your organization. 

For information about how to access the calculated metrics builder, see [Build metrics](/help/components/calc-metrics/cm-workflow/cm-build-metrics.md).

### Create calculated metrics for a single project

You can create quick calculated metrics that are available only for the project where they were created.

To create a calculated metric for a single project:

1. In Analysis Workspace, open the project where you want to create the calculated metric.

1. In a freeform table, select **[!UICONTROL Create metric from selection]** from the context menu in a column header.

   ![Workspace panel highlighting Create from selection](assets/create-metric-from-selection.png)

1. To create a calculated metric for this project only, choose from the following options:

   * [!UICONTROL **Divide**]
   
   * [!UICONTROL **Subtract**]

   * [!UICONTROL **Add**]

   * [!UICONTROL **Multiply**]

   Or, to open the calculated metric builder and create the calculated metric for all projects, select [!UICONTROL **Open in Calculated Metric Builder**], then continue with [Build metrics](/help/components/calc-metrics/cm-workflow/cm-build-metrics.md).


<!-- This video really shows an AA example using hits, etc.  Not suitable for CJA... >
+++ See the following video on how to create an implementation-less calculated metric from within Analysis Workspace.

[Calculated Metrics: Implementation-less metrics](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/calculated-metrics/calculated-metrics-implementationless-metrics.html) (3:42)


>[!VIDEO](https://video.tv.adobe.com/v/25407/?quality=12)

+++

-->

## Metrische gegevens vergelijken met verschillende attribuutmodellen

Als u één attributiemodel voor metrisch wilt snel en gemakkelijk vergelijken met een ander, uitgezochte **[!UICONTROL Compare attribution models]** van het contextmenu voor metrisch.

![ het paneel dat van Workspace het benadrukken vergelijkt attributiemodellen ](assets/compare-attribution.png)

Met deze sneltoets kunt u snel en eenvoudig attributiemodellen vergelijken.
