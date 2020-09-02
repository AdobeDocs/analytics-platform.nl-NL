---
description: Gebruik de lijnvisualisatie om trended (op tijd gebaseerde) gegevenssets weer te geven
title: Lijn
uuid: 0508ff29-43fe-4f3a-a5f7-051869271b55
translation-type: tm+mt
source-git-commit: 4f163e32787a732526511aeda5f6c1e32becb490
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 3%

---


# Lijn

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset wijkt enigszins af van [Analysis Workspace in het traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

De visualisatie van de Lijn vertegenwoordigt metriek gebruikend een lijn om te tonen hoe de waarden over een periode veranderen. Een lijngrafiek kan slechts worden gebruikt wanneer de tijd als afmeting wordt gebruikt.

![Lijnvisualisatie](assets/line-viz.png)

>[!IMPORTANT]
>
>Bepaalde instellingen voor lijnvisualisatie, zoals [!UICONTROL Show trendline], momenteel in beperkte mate worden getest. [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/landing/an-releases.html)

Klik op het tandwielpictogram rechtsboven in de lijnvisualisatie voor toegang [**Visualisatie-instellingen**](freeform-analysis-visualizations.md) beschikbaar. Instellingen worden gecategoriseerd in:

* **Algemeen**: Instellingen die gemeenschappelijk zijn voor verschillende visualisatietypen
* **As**: Instellingen die van invloed zijn op de x- of y-as van de lijnvisualisatie
* **Bedekkingen**: Opties om extra context aan de reeks toe te voegen die in uw lijnvisualisatie wordt getoond.

![Visualisatie-instellingen](assets/viz-settings-modal.png)

## Korreligheid wijzigen

Een granulariteit-vervolgkeuzelijst in het dialoogvenster [visualisatie-instellingen](freeform-analysis-visualizations.md) Hiermee kunt u een trendvisualisatie (bijvoorbeeld lijn, balk) van dag naar week wijzigen in maand enz. De granulariteit wordt ook bijgewerkt in de gegevensbrontabel.

## min of max tonen

Onder **[!UICONTROL Visualization Settings]** > **[!UICONTROL Overlays]** > **[!UICONTROL Show min/max]** kunt u een minimum- en maximumwaarde-label bedekken om de pieken en dalen snel in een metrische kleur te markeren. Opmerking: De min/max-waarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie.

![min/max tonen](assets/min-max-labels.png)

## Trendline-bedekking tonen

Onder **[!UICONTROL Visualization Settings]** > **[!UICONTROL Overlays]** > **[!UICONTROL Show trendline]**, kunt u een regressietriendline toevoegen aan uw lijnreeks. Met behulp van trendlines wordt een duidelijker patroon in de gegevens weergegeven.

![Lineaire trendlijn](assets/show-linear-trendline.png)

Alle modellen zijn geschikt met behulp van de kleinste vierkantjes:

| Model | Beschrijving |
| --- | --- |
| Lineair | Hiermee maakt u een rechte lijn die het best past bij eenvoudige lineaire gegevenssets. Deze lijn is handig wanneer de gegevens met een constante snelheid worden verhoogd of verlaagd. Vergelijking: `y = a + b * x` |
| Logaritmisch | Hiermee maakt u een lijn met een curve die het best past. Deze lijn is handig wanneer de snelheid waarmee de gegevens worden gewijzigd snel toeneemt of afneemt en vervolgens niveaus uit. Een logaritmische trendline kan negatieve en positieve waarden gebruiken. Vergelijking: `y = a + b * log(x)` |
| Exponential | Hiermee maakt u een gekromde lijn. Deze lijn is handig wanneer de gegevenssnelheid voortdurend toeneemt of daalt. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking: `y = a + e^(b * x)` |
| Voeding | Maakt een gekromde lijn en is handig voor gegevenssets die metingen vergelijken die met een specifieke snelheid toenemen. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking: `y = a * x^b` |
| Quadratisch | Vindt het best-past voor een gegevensreeks die als parabool wordt gevormd (naar boven of naar onder bedekken). Vergelijking: `y = a + b * x + c * x^2` |
