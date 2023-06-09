---
description: Er zijn twee manieren om metriek in Analysis Workspace te gebruiken.
title: Metrics
feature: Metrics
exl-id: 4edfb5d7-da20-4bd8-8041-387b291daf96
source-git-commit: a9751cad1ba49fe3e8c2c484e34d1725e063c2d4
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 4%

---

# Metrics

Met cijfers kunt u gegevenspunten in Analysis Workspace kwantificeren. Deze worden meestal gebruikt als kolommen in een visualisatie en zijn gekoppeld aan afmetingen.


## Soorten metingen

Adobe biedt verschillende typen maateenheden voor gebruik in Analysis Workspace:

* **Standaardwaarden**: Voorbeeld van standaardmetriek zijn Mensen, Zittingen, Gebeurtenissen.

* **Berekende cijfers** ![Pictogram Berekende metrische waarde](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg): Door de gebruiker gedefinieerde meetwaarden die zijn gebaseerd op standaardmeetwaarden, statische getallen of algoritmische functies.

* **Berekende metrische sjablonen**  <img src="./assets/adobe-logo.svg" width="18"> : Adobe-bepaalde metriek die zich gelijkaardig aan berekende metriek gedragen. U kunt ze ongewijzigd gebruiken in Workspace-projecten of een kopie opslaan om de logica ervan aan te passen.


![Metrische gegevens in de gebruikersinterface](assets/cja-metrics.png)

U kunt zien of metrisch is goedgekeurd ![Goedgekeurd pictogram](https://spectrum.adobe.com/static/icons/ui_18/CheckmarkSize100.svg)  of niet. Als u meer details op metrisch wilt, beweegt zich over metrisch, en selecteert ![Info, pictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_InfoOutline_18_N.svg).


Metriek is flexibel in het gebruik binnen Analysis Workspace. Sleep metrisch aan een lege lijst Freeform om te zien die metrisch over de de datumperiode van het project trended. U kunt metrisch ook slepen wanneer een afmeting aanwezig is om dat metrisch vergeleken bij elk afmetingspunt te zien. Als u een metrische waarde boven op een bestaande metrische koptekst sleept, wordt deze vervangen en als u een metrische waarde naast een koptekst sleept, ziet u beide meetgegevens naast elkaar.

## Berekende standaarden

Met berekende meetwaarden kunt u gemakkelijk zien hoe de meetgegevens op elkaar betrekking hebben met behulp van eenvoudige operatoren of statistische functies. U kunt op verschillende manieren berekende metriek maken:

U kunt **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]**. Hiermee gaat u naar de [Berekende metrische builder](/help/components/calc-metrics/calc-metr-overview.md), waar u aangepaste metriek kunt maken op basis van bestaande metriek.

Om het gemakkelijker te maken om snel berekende metriek tot stand te brengen, **[!UICONTROL Create metric from selection]** is toegevoegd aan het met de rechtermuisknop aanklikken van de kolom in de Lijsten van de Vrije Vorm. Deze optie wordt weergegeven wanneer een of meer cellen met kopteksten zijn geselecteerd.

![Maken van selectie](assets/create-metric-from-selection.png)

[Berekende waarden: Metriek zonder implementatie](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/calculated-metrics/calculated-metrics-implementationless-metrics.html) (3:42)

## Metriek vergelijken met verschillende attributiemodellen

Als u één attributiemodel aan een andere snel en gemakkelijk wilt vergelijken, klik metrisch met de rechtermuisknop aan en selecteer **[!UICONTROL Compare Attribution Models]**:

![Kenmerk vergelijken](assets/compare-attribution.png)

Met deze sneltoets kunt u snel en eenvoudig een attributiemodel vergelijken met een ander attribuut zonder dat u dit model in een metrische modus hoeft te slepen en tweemaal hoeft te configureren.
