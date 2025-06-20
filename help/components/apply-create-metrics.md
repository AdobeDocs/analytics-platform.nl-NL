---
description: Er zijn twee manieren om metriek in Analysis Workspace te gebruiken.
title: Metrics
feature: Metrics
exl-id: 4edfb5d7-da20-4bd8-8041-387b291daf96
role: User
source-git-commit: ec2fc88372814b01a04d4cc824181222ee55a83d
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# Metrics

Met cijfers kunt u gegevenspunten in Analysis Workspace kwantificeren. Deze worden meestal gebruikt als kolommen in een visualisatie en zijn gekoppeld aan afmetingen.

## Metriek gebruiken in Analysis Workspace

Metriek is flexibel in het gebruik binnen Analysis Workspace. Sleep metrisch aan een lege lijst Freeform om te zien die metrisch over de de datumperiode van het project trended. U kunt metrisch ook slepen wanneer een afmeting aanwezig is om dat metrisch vergeleken bij elk afmetingspunt te zien. Als u een metrische waarde boven op een bestaande metrische koptekst sleept, wordt deze vervangen en als u een metrische waarde naast een koptekst sleept, ziet u beide meetgegevens naast elkaar.

Voor informatie over hoe te om metriek en andere soorten componenten aan Analysis Workspace toe te voegen, zie [ de componenten van het Gebruik in Analysis Workspace ](/help/components/use-components-in-workspace.md).


## Soorten metingen

Adobe biedt verschillende typen maateenheden voor gebruik in Analysis Workspace:


* **Standaard metriek**: Voorbeeld van standaardmetriek zijn Mensen, Zittingen, Gebeurtenissen.

  In tegenstelling tot Adobe Analytics, staat Customer Journey Analytics u toe om standaardmetriek op een flexibele manier binnen het werkingsgebied van een verbinding en een gegevensmening te bepalen.

   * **Mensen**: De metrische Mensen in Customer Journey Analytics is de telling verschillend van Persoon IDs. Afhankelijk van wat u als identiteitskaart van de Persoon wanneer u datasets in uw verbinding vormt, metrische Mensen verschillende dingen kunnen betekenen.
   * **Sessies**: Metrische Sessies in Customer Journey Analytics is wat u als deel van de configuratie van de montages van Sessies in uw gegevensmening bepaalt. Zie [ montages van de Zitting ](/help/data-views/session-settings.md).
   * **Gebeurtenissen**: De metrische Gebeurtenissen in Customer Journey Analytics worden samengesteld van de gebeurtenissen die deel van om het even welke gebeurtenisdataset uitmaken u als deel van uw verbinding hebt gevormd.

  Zie [ Standaardmetriek ](#standard-metrics) voor de volledige lijst van standaardmetriek.

* **Berekende metriek** ![ calculator ](/help/assets/icons/Calculator.svg): Gebruiker-bepaalde metriek die op standaardmetriek, statische aantallen, of algoritmische functies gebaseerd zijn.

* **Berekende metrische malplaatjes** ![ AdobeLogoSmall ](/help/assets/icons/AdobeLogoSmall.svg) : Adobe-bepaalde metriek die zich zo ook aan berekende metriek gedragen. U kunt ze ongewijzigd gebruiken in Workspace-projecten of een kopie opslaan om de logica aan te passen. Zie [ Standaard berekende metriek ](calc-metrics/cm-workflow/../default-calcmetrics.md).

U kunt zien of metrisch wordt goedgekeurd ![ Goedgekeurd pictogram ](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg) of niet. Als u meer details op metrisch wilt, beweegt over metrisch, en selecteert ![ pictogram van Info ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg). Zie [ Info van de Component ](use-components-in-workspace.md#component-info) voor meer informatie.


## Standaardwaarden

De volledige lijst van standaardmetriek in Customer Journey Analytics:
{{standard-metrics}}


## Berekende waarden maken

Met de berekende metriek kunt u eenvoudig configureren hoe de metriek op elkaar betrekking heeft, met behulp van eenvoudige operatoren of statistische functies. Zie [ Berekend metriek overzicht ](/help/components/calc-metrics/calc-metr-overview.md) voor meer informatie.

Er zijn verschillende manieren om berekende metriek te maken. De methode u kiest bepaalt of berekende metrisch van de componentenlijst over alle projecten, of slechts in het project beschikbaar is waar het werd gecreeerd.

### Berekende waarden maken voor alle projecten

U kunt de [ berekende metrische bouwer ](/help/components/calc-metrics/cm-workflow/cm-build-metrics.md) gebruiken [ berekende metriek ](/help/components/calc-metrics/cm-workflow/cm-workflow.md) creëren. Wanneer gecreeerd op deze manier, zijn de berekende metriek beschikbaar in de componentenlijst en kunnen dan in projecten door uw organisatie worden gebruikt.

### Berekende waarden maken voor één project

U kunt snel een metrische berekening tot stand brengen die slechts voor het project beschikbaar is waar het werd gecreeerd.

Om berekende metrisch voor één enkel project tot stand te brengen:

1. Open in Analysis Workspace het project waar u de berekende metrische waarde wilt maken.

1. Klik in een vrije-vormlijst met de rechtermuisknop op de kolomkop van één kolom.

   of

   Selecteer twee kolommen terwijl u Shift ingedrukt houdt en klik vervolgens met de rechtermuisknop op een van de geselecteerde kolommen.

1. Selecteren **[!UICONTROL Create metric from selection]**

   ![ het paneel dat van Workspace creeert van selectie ](assets/create-metric-from-selection.png) benadrukt

1. Als u alleen voor dit project een berekende metrische waarde wilt maken, kiest u een van de beschikbare opties.

   Wanneer u één kolom selecteert, zijn de volgende opties beschikbaar:

   * [!UICONTROL **Gemiddeld**]: Creeert een nieuwe kolom die de gemiddelde waarde in de reeks afmetingselementen voor de kolom toont. Dit gebruikt de [ Mean ](/help/components/calc-metrics/cm-functions.md#mean) functie.

   * [!UICONTROL **Mediaan**]: Creeert een nieuwe kolom die de mediane waarde in de reeks afmetingselementen voor de kolom toont. Dit gebruikt de [ Mediaan ](/help/components/calc-metrics/cm-functions.md#median) functie.

   * [!UICONTROL **Kolom max**]: Creeert een nieuwe kolom die de grootste waarde in de reeks afmetingselementen voor de kolom toont. Dit gebruikt de [ Maximale functie van de Kolom ](/help/components/calc-metrics/cm-functions.md#column-maximum).

   * [!UICONTROL **Kolom min**]: Creeert een nieuwe kolom die de kleinste waarde in de reeks afmetingselementen voor de kolom toont. Dit gebruikt de [ Minimale functie van de Kolom ](/help/components/calc-metrics/cm-functions.md#column-minimum).

   * [!UICONTROL **som van de Kolom**]:Creeert een nieuwe kolom die alle numerieke waarden voor metrisch binnen een kolom (over de elementen van een afmeting) toevoegt. Dit gebruikt de [ functie van de Som van de Kolom ](/help/components/calc-metrics/cm-functions.md#column-sum).

   Wanneer u twee kolommen selecteert, zijn de volgende opties beschikbaar:

   * [!UICONTROL **verdeel**]: Creeert een nieuwe kolom die de waarden van de twee geselecteerde kolommen verdeelt.

   * [!UICONTROL **trekt af**]: Creeert een nieuwe kolom die de waarden van de twee geselecteerde kolommen aftrekt.

   * [!UICONTROL **voegt**] toe: Creeert een nieuwe kolom die de waarden van de twee geselecteerde kolommen toevoegt.

   * [!UICONTROL **vermenigvuldigt**]: Creeert een nieuwe kolom die de waarden van de twee geselecteerde kolommen vermenigvuldigt.

   * [!UICONTROL **de verandering van de Percentage**]: Creeert een nieuwe kolom die de percentageverandering tussen de twee geselecteerde kolommen toont.


## Metrische gegevens vergelijken met verschillende attribuutmodellen

Als u het ene attributiemodel snel wilt vergelijken met het andere voor een metrische waarde, selecteert u **[!UICONTROL Compare attribution models]** in het contextmenu voor een metrische waarde.

![ het paneel dat van Workspace het benadrukken vergelijkt attributiemodellen ](assets/compare-attribution.png)

Met deze sneltoets kunt u het ene attributiemodel vergelijken met het andere zonder dat u het twee keer hoeft te slepen en te configureren.


