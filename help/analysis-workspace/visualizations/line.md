---
description: Gebruik lijnvisualisatie om trended (op tijd-gebaseerde) datasets te schilderen
title: Lijn
feature: Visualizations
exl-id: b68aa8dc-2c96-4c49-8d3c-d94804aab479
role: User
source-git-commit: 30f3e24533ab0e03ee7f819c7f94592776603764
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Lijn

>[!NOTE]
>
>De lijnvisualisatie wordt binnenkort weergegeven [intelligente bijschriften](/help/analysis-workspace/visualizations/intelligent-captions.md).

De visualisatie van de Lijn vertegenwoordigt metriek gebruikend een lijn om te tonen hoe de waarden over een periode veranderen. Een lijngrafiek kan slechts worden gebruikt wanneer de tijd als afmeting wordt gebruikt.

![Lijnvisualisatie](assets/line-viz.png)

Het pictogram Instellingen selecteren ![Instellingen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg) in de hoogste bar van de visualisatie van de Lijn aan toegang [Visualisatie-instellingen](freeform-analysis-visualizations.md) beschikbaar. De instellingen worden gecategoriseerd in:

<img src="./assets/viz-settings-line.png" alt="Visualisatie-instellingen" width="50%" />

* **Algemeen**: Instellingen die veel voorkomen in verschillende visualisatietypen
* **As**: Instellingen die de x- of y-as van de lijnvisualisatie beïnvloeden
* **Bedekkingen**: Opties voor het toevoegen van extra context aan de reeks die in uw lijnvisualisatie wordt getoond.


## Korreligheid wijzigen

Een granulariteit-vervolgkeuzelijst in het dialoogvenster [visualisatie-instellingen](freeform-analysis-visualizations.md) Hiermee kunt u een trendvisualisatie (bijvoorbeeld lijn, balk) van dag naar week wijzigen in maand enz. De granulariteit wordt ook bijgewerkt in de gegevensbrontabel.

## min of max tonen

Onder **[!UICONTROL Visualization Settings]** > **[!UICONTROL Overlays]** > **[!UICONTROL Show min/max]** kunt u een minimum- en maximumwaarde-label bedekken om de pieken en dalen snel in een metrische kleur te markeren. Opmerking: de min/max-waarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie.

![Een bedekking met het label voor de minimum- en maximumwaarde.](assets/min-max-labels.png)

## Trendline-bedekking tonen

Onder **[!UICONTROL Visualization Settings]** > **[!UICONTROL Overlays]** > **[!UICONTROL Show trendline]**, kunt u een regressie of bewegende gemiddelde trendline aan uw lijnreeks toevoegen. Met behulp van trendlines wordt een duidelijker patroon in de gegevens weergegeven.

>[!TIP]
>
>Aanbevolen wordt trendlines toe te passen op gegevens die vandaag (gedeeltelijke gegevens) of toekomstige data niet omvatten, aangezien die de trendline zullen scheeftrekken. Als u echter datums in de toekomst wilt opnemen, verwijdert u nullen uit de gegevens om te voorkomen dat de gegevens gedurende die dagen worden schuingetrokken. Om dit te doen, ga naar de gegevensbronlijst van de visualisatie, kies uw metrische kolom, dan laat toe **[!UICONTROL Column Settings]** > **[!UICONTROL Interpret zero as no value]**.

![Lineaire trendlijn](assets/show-linear-trendline.png)

Alle trendlines van het regressiemodel zijn geschikt gebruikend gewone minste vierkanten:

| Model | Beschrijving |
| --- | --- |
| Lineair | Hiermee maakt u een rechte lijn die het best past bij eenvoudige lineaire gegevenssets. Deze lijn is handig wanneer de gegevens met een constante snelheid worden verhoogd of verlaagd. Vergelijking `y = a + b * x` |
| Logaritmisch | Hiermee maakt u een lijn met een curve die het best past. Deze lijn is handig wanneer de snelheid waarmee de gegevens worden gewijzigd snel toeneemt of afneemt en vervolgens niveaus uit. Een logaritmische trendline kan negatieve en positieve waarden gebruiken. Vergelijking `y = a + b * log(x)` |
| Exponential | Hiermee maakt u een gekromde lijn. Deze lijn is handig wanneer de gegevenssnelheid voortdurend toeneemt of daalt. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking `y = a + e^(b * x)` |
| Voeding | Maakt een gekromde lijn en is handig voor gegevenssets die metingen vergelijken die met een specifieke snelheid toenemen. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking `y = a * x^b` |
| Quadratisch | Zoekt het best-past voor een dataset die als parabola wordt gevormd (naar boven of naar onder bedekken). Vergelijking `y = a + b * x + c * x^2` |
| Gemiddeld verplaatsen | Hiermee maakt u een vloeiende trendline op basis van een set gemiddelden. Ook gekend als voortschrijdend gemiddelde, gebruikt een voortschrijdend gemiddelde een specifiek aantal gegevenspunten (die door uw &quot;Selectie van Punten&quot;worden bepaald), het gemiddelde van hen, en gebruikt het gemiddelde als punt in de lijn. Voorbeelden zijn het voortschrijdende gemiddelde over 7 dagen of het voortschrijdende gemiddelde over 4 weken. |
