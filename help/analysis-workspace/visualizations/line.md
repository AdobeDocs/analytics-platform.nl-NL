---
description: Gebruik de lijnvisualisatie om trending (op tijd-gebaseerde) gegevensreeksen af te schilderen
title: Lijn
uuid: 0508ff29-43fe-4f3a-a5f7-051869271b55
translation-type: tm+mt
source-git-commit: afe5b341ea1b442c23561299fbffce59dae45930
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 3%

---


# Lijn

De visualisatie van de Lijn vertegenwoordigt metriek gebruikend een lijn om te tonen hoe de waarden over een periode veranderen. Een lijngrafiek kan slechts worden gebruikt wanneer de tijd als afmeting wordt gebruikt.

![Lijnvisualisatie](assets/line-viz.png)

>[!IMPORTANT]
>
>Sommige de visualiseringsmontages van de Lijn, zoals [!UICONTROL Show trendline], zijn momenteel beperkt getest. [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/landing/an-releases.html)

Klik op het versnellingspictogram rechtsboven in de lijnvisualisatie om toegang te krijgen [**Visualisatie-instellingen**](freeform-analysis-visualizations.md) beschikbaar. De montages worden gecategoriseerd in:

* **Algemeen**: Instellingen die bij visualisatietypen gebruikelijk zijn
* **As**: Instellingen die de x- of y-as van de lijnvisualisatie beïnvloeden
* **Overschrijvingen**: Opties om extra context aan de reeks toe te voegen die in uw lijnvisualisatie wordt getoond.

![Visualisatie-instellingen](assets/viz-settings-modal.png)

## Granulariteit wijzigen

Een granularity drop-down in [visualisatie-instellingen](freeform-analysis-visualizations.md) Hiermee kunt u een trendmatige visualisatie (bv. lijn, balk) van dag tot week en maand wijzigen, enzovoort. granularity wordt ook bijgewerkt in de gegevensbronlijst.

## min of max tonen

onder **[!UICONTROL Visualization Settings]** > **[!UICONTROL Overlays]** > **[!UICONTROL Show min/max]**, kunt u een minimum en maximumwaardeetiket bedekken om de pieken en de dalen in metrisch snel te benadrukken.

![min./max. weergeven](assets/min-max-labels.png)

## Tendlinebedekking tonen

onder **[!UICONTROL Visualization Settings]** > **[!UICONTROL Overlays]** > **[!UICONTROL Show trendline]**, kunt u verkiezen om een regressietrendline aan uw lijnreeks toe te voegen. De rendlines helpen om een duidelijker patroon in de gegevens af te schilderen.

![Lineaire trendlijn](assets/show-linear-trendline.png)

Alle modellen zijn geschikt met de gewone kleinste kwadraten:

| Model | Beschrijving |
|---|---|
| Lineair | Creeert een best-geschikte rechte lijn voor eenvoudige lineaire gegevensreeksen en is nuttig wanneer de gegevens met een constant tarief stijgen of verminderen. Vergelijking: `y = a + b * x` |
| Logaritmisch | Creeert een best-geschikte gebogen lijn en is nuttig wanneer het tarief van verandering in de gegevens snel stijgt of vermindert en dan niveaus uit. Een logaritmische trendline kan negatieve en positieve waarden gebruiken. Vergelijking: `y = a + b * log(x)` |
| Exponent | Creeert een gebogen lijn en is nuttig wanneer de gegevens stijgen of bij constant stijgende tarieven vallen. Deze optie zou niet moeten worden gebruikt als uw gegevens nul of negatieve waarden bevatten. Vergelijking: `y = a + e^(b * x)` |
| Voeding | Creeert een gebogen lijn en is nuttig voor gegevensreeksen die metingen vergelijken die aan een specifiek tarief stijgen. Deze optie zou niet moeten worden gebruikt als uw gegevens nul of negatieve waarden bevatten. Vergelijking: `y = a * x^b` |
| Quadratische | Vindt best-geschikt voor een gegevensreeks die als parabola wordt gevormd (concave naar boven of naar onder). Vergelijking: `y = a + b * x + c * x^2` |
