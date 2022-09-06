---
description: Hiermee kunt u eenvoudig vergelijkingsgegevens visualiseren in Analysis Workspace, zoals bouwvergelijkingen met vorige maand, vorig jaar enzovoort.
title: Visualisatie van combinatiekaarten
feature: Visualizations
role: User, Admin
exl-id: 08e49857-aa58-4527-bdfd-b1663a75a02b
source-git-commit: 5eebcccc45b9760ecc18ec94ca526f2082d089bc
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Combodiagram

>[!NOTE]
>
>Deze functionaliteit is momenteel in [beperkte tests](/help/release-notes/releases.md).

De [!UICONTROL Combo chart] Met visualisatie kunt u snel een vergelijkingsvisualisatie maken zonder eerst een tabel te hoeven maken. U kunt tendensen in uw gegevens in een lijn gemakkelijk bekijken/bar combinatie.

Een [!UICONTROL Combo chart] tot

* Vergelijk de bestellingen van deze week voor bestellingen op hetzelfde tijdstip vorige maand (en vorig jaar) - allemaal binnen een paar klikken.

* Snel meerdere meetgegevens analyseren en vergelijken (zoals [!UICONTROL Unique Visitors] en [!UICONTROL Revenue]) op dezelfde kaart.

* Een metrische waarde analyseren op basis van een functie (zoals [!UICONTROL Cumulative Average]) over een tijdshorizon.

Houd er rekening mee dat u

* Meerdere vergelijkingen in één vergelijking toevoegen [!UICONTROL Combo chart].
* Als u een of meer vergelijkingen toevoegt, moeten deze van hetzelfde type zijn, zoals [!UICONTROL Time comparison].
* U kunt maximaal vijf vergelijkingen maken.
* U kunt maximaal drie filters (segmenten) toepassen op een metrische waarde.

## Een combinatieschema samenstellen

1. Sleep vanuit de vervolgkeuzelijst Visualisaties in de linkertrack de [!UICONTROL Combo chart] visualisatie in een leeg paneel.

   ![](assets/combo-chart-build.png)

1. Selecteer in de vervolgkeuzelijsten een afmeting voor de X-as en een afmeting voor de Y-as.

1. Selecteer het type van [!UICONTROL Line comparison] wilt gebruiken.

   | Vergelijkingstype lijn | Definitie |
   | --- | --- |
   | **[!UICONTROL Time comparison]** | Het meest voorkomende type vergelijking: deze periode wordt bijvoorbeeld vergeleken met 4 weken geleden. Als u [!UICONTROL Time comparison]kiest u een tweede tijdsperiode die u wilt vergelijken.<p>![](assets/combo-time-period.png) |
   | **[!UICONTROL Function]** | U kunt een functie als [!UICONTROL Average] in de vergelijking. Hieronder vindt u een lijst met ondersteunde functies.<p>![](assets/combo-functions.png) |
   | **[!UICONTROL Secondary metric]** | U kunt bijvoorbeeld [!UICONTROL Revenue] naar een andere metrische waarde.<p>![](assets/combo-2metrics.png) |

   {style=&quot;table-layout:auto&quot;}

1. Klik op **[!UICONTROL Build]**.

   De uitvoer ziet er ongeveer als volgt uit:

   ![](assets/combo-output.png)

   De huidige periode wordt getoond in de grafiek van de bar, en de vergelijkingsperiode wordt vertegenwoordigd door de lijngrafiek. De punten op het lijndiagram worden ook wel &quot;balken&quot; genoemd.

## Ondersteunde functies

Als u **[!UICONTROL Function]** als de [!UICONTROL Line comparison type], wordt een functie geretourneerd van de maateenheid die u hebt gekozen.

| -functie | Definitie |
| --- | --- |
| **[!UICONTROL Column Sum]** | Hiermee worden alle numerieke waarden toegevoegd voor een metrische waarde in een kolom (over de elementen van een dimensie) |
| **[!UICONTROL Cumulative Average]** | Retourneert het gemiddelde van de laatste N-rijen. |
| **[!UICONTROL Median]** | Retourneert de mediaan voor een metrische waarde in een kolom. De mediaan is het getal in het midden van een reeks getallen, dat wil zeggen dat de helft van de getallen waarden heeft die groter zijn dan of gelijk zijn aan de mediaan, en de helft kleiner dan of gelijk is aan de mediaan. |
| **[!UICONTROL Cumulative]** | De cumulatieve som van N rijen. |
| **[!UICONTROL Column Maximum]** | Retourneert de grootste waarde in een set dimensieelementen voor een metrische kolom. |
| **[!UICONTROL Mean]** | Retourneert het rekenkundig gemiddelde (of gemiddelde) voor een metrische waarde. |
| **[!UICONTROL Column Minimum]** | Retourneert de laagste waarde in een set dimensieelementen voor een metrische kolom. |

{style=&quot;table-layout:auto&quot;}

Hier is een voorbeeld van het cumulatieve gemiddelde van de metrische inkomsten:

![](assets/combo-cumul-avg.png)

Hier is een voorbeeld van een combo grafiek met zowel Cumulatieve gemiddelde als Gemiddelde functies:

![](assets/combo-two-functions.png)

## Combo Chart-instellingen

Klik op het tandwielpictogram rechtsboven in een keuzelijst met invoervak om de instellingen ervan te wijzigen.

![](assets/combo-settings.png)

| Instelling | Definitie |
| --- | --- |
| **[!UICONTROL Visualization type]** | Hiermee kunt u overschakelen op een ander visualisatietype. |
| **[!UICONTROL Granularity]** | Voor getreneerde visualisaties kunt u de tijdsgranulariteit (dag, week, maand, enz.) wijzigen in deze vervolgkeuzelijst. |
| **[!UICONTROL General]** |  |
| **[!UICONTROL Percentages]** | Hiermee geeft u waarden weer in percentages. |
| **[!UICONTROL Legend visible]** | Hiermee kunt u de gedetailleerde legendetekst voor de visualisatie van Combo-diagrammen verbergen. |
| **[!UICONTROL Limit max items]** | Hiermee verkleint u het aantal items op de X-as. Als u een grote gegevensset hebt, kunt u alleen de eerste 10 items tonen (of een waarde die u kiest). |
| **[!UICONTROL Overlays]** | Streepjes weergeven of verbergen op lijnen. |
| **[!UICONTROL Axis]** |  |
| **[!UICONTROL Display dual axis]** | Is slechts van toepassing als u twee metriek hebt - u kunt een y-as op de linkerzijde (voor één metrisch) en op het recht (voor andere metrisch) hebben. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. De kleur van de twee assen komt overeen met de kleur van de tabel, tenzij er meerdere vergelijkingen zijn. In dat geval is de kleur voor alle vergelijkingen grijs. |
| **[!UICONTROL Normalization]** | Dwingt metriek tot gelijke verhoudingen. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| **[!UICONTROL Show x-axis]** | Geef de x-as weer of verberg deze. |
| **[!UICONTROL Show y-axis]** | Geef de y-as weer of verberg deze. |
| **[!UICONTROL Anchor y-axis at zero]** | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as NON-ZERO ingesteld als de standaardinstelling van het diagram. Als u dit vakje inschakelt, wordt de y-as gedwongen tot nul (en wordt het diagram opnieuw getekend). |

{style=&quot;table-layout:auto&quot;}
