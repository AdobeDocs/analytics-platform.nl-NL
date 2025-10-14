---
description: Gebruik de lijnvisualisatie om (op tijd-gebaseerde) datasets visualiseren.
title: Lijn
feature: Visualizations
exl-id: b68aa8dc-2c96-4c49-8d3c-d94804aab479
role: User
source-git-commit: a16043f1bb15deba1332ed39438214597647b9b4
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Lijn {#line}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_line_button"
>title="Lijn"
>abstract="Creeer een lijnvisualisatie die toont hoe de waarden over een periode veranderen. Een lijnvisualisatie kan slechts worden gebruikt wanneer de tijd als afmeting wordt gebruikt."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert de visualisatie van de Lijn in_ ![&#x200B; CustomerJourneyAnalytics &#x200B;](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics**._<br/>_zie [&#x200B; Lijn &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/analyze/analysis-workspace/visualizations/line) voor_ ![&#x200B; AdobeAnalytics &#x200B;](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics** versie van dit artikel._

>[!ENDSHADEBOX]


![&#x200B; GraphTrend &#x200B;](/help/assets/icons/GraphTrend.svg) **[!UICONTROL Line]** visualisatie vertegenwoordigt metriek gebruikend een lijn om te tonen hoe de waarden over een periode veranderen. Een lijnvisualisatie kan slechts worden gebruikt wanneer de tijd als afmeting wordt gebruikt.

![&#x200B; visualisatie van de lijn 0&rbrace;](assets/line-viz.png)


## Instellingen

Als deel van de [&#x200B; visualiseringsmontages &#x200B;](freeform-analysis-visualizations.md#settings), zijn de specifieke montages van de lijnvisualisatie beschikbaar.

| Instelling | Beschrijving |
|---|---|
| **[!UICONTROL Granularity]** | Selecteer in het keuzemenu Korreligheid een trendmatige visualisatie van dag naar week, enz. De granulariteit wordt ook bijgewerkt in de gegevensbrontabel. |
| **[!UICONTROL Show min]** <br/>**[!UICONTROL Show max]** | U kunt een label voor de minimum- en maximumwaarde bedekken om de minimum- en maximumwaarden in een metrische waarde te markeren. De min/max-waarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie.<br/>![&#x200B; een bedekking met het minimum en maximumwaardeetiket.](assets/min-max-labels.png) |
| **[!UICONTROL Show trendline]** | U kunt een regressie of bewegende gemiddelde trendline aan uw lijnreeks toevoegen. Met behulp van trendlines wordt een duidelijker patroon in de gegevens weergegeven. Selecteer een model in de lijst als u deze optie hebt geselecteerd. Zie [&#x200B; Modellen &#x200B;](#models) voor een overzicht en een beschrijving van beschikbare modellen.<br/>![&#x200B; Lineaire trendline &#x200B;](assets/show-linear-trendline.png).<p>**TIP:** men adviseert dat de trendlines worden toegepast op gegevens die vandaag (gedeeltelijke gegevens) of toekomstige data niet omvatten. De trendlijn wordt scheefgetrokken door de datum van vandaag of van morgen. Als u echter datums in de toekomst wilt opnemen, verwijdert u nullen uit de gegevens om te voorkomen dat de gegevens gedurende die dagen worden schuingetrokken. Ga naar de gegevensbrontabel van de visualisatie, kies de metrische kolom en schakel vervolgens **[!UICONTROL Column Settings]** > **[!UICONTROL Interpret zero as no value]** in.</p> |

### Modellen

Alle trendlines van het regressiemodel zijn geschikt gebruikend gewone minste vierkanten:

| Model | Beschrijving |
| --- | --- |
| **[!UICONTROL Linear]** | Creeer een best-geschikte rechte lijn voor eenvoudige lineaire datasets en is nuttig wanneer de gegevens met een constante snelheid stijgen of verminderen. Vergelijking: `y = a + b * x` |
| **[!UICONTROL Logarithmic]** | Maak een lijn met een curve die het best past en die nuttig is wanneer de snelheid waarmee de gegevens worden gewijzigd snel toeneemt of afneemt en vervolgens niveaus uit. Een logaritmische trendline kan negatieve en positieve waarden gebruiken. Vergelijking: `y = a + b * log(x)` |
| **[!UICONTROL Exponential]** | Maak een gekromde lijn en is handig wanneer gegevens stijgen of dalen met voortdurend stijgende snelheden. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking: `y = a + e^(b * x)` |
| **[!UICONTROL Power]** | Maak een gekromde lijn en is handig voor gegevenssets die metingen vergelijken die met een specifieke snelheid toenemen. Deze optie mag niet worden gebruikt als de gegevens nul of negatieve waarden bevatten. Vergelijking: `y = a * x^b` |
| **[!UICONTROL Quadratic]** | Zoekt het best-past voor een dataset die als parabola wordt gevormd (naar boven of naar onder bedekken). Vergelijking: `y = a + b * x + c * x^2` |
| **[!UICONTROL Moving average]** | Maak een vloeiende trendline op basis van een set gemiddelden. Bij een voortschrijdend gemiddelde wordt een bepaald aantal gegevenspunten gebruikt (bepaald door uw [!UICONTROL Granularity] -selectie), wordt het gemiddelde genomen en wordt het gemiddelde gebruikt als een punt op de regel. Voorbeelden zijn een voortschrijdend gemiddelde van zeven dagen of een voortschrijdend gemiddelde van vier weken. |

>[!MORELIKETHIS]
>
>[&#x200B; voeg een visualisatie aan een paneel toe &#x200B;](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>&#x200B;>[Visualisatie-instellingen &#x200B;](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>&#x200B;>[Contextmenu Visualisatie &#x200B;](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>

