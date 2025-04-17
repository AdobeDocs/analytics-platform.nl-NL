---
description: Het segmenteren van individuele metriek staat u toe om metrische vergelijkingen binnen het zelfde rapport te maken.
title: Gesegmenteerde metriek
feature: Calculated Metrics
exl-id: 37cc93df-9f51-42b3-918f-ed5864991621
source-git-commit: 2f87afb9c87b0436ee40cc67a04d99d4f4f10e74
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Gesegmenteerde metriek

In de [ Berekende metrische bouwer ](cm-build-metrics.md#definition-builder), kunt u segmenten binnen uw metrische definitie toepassen. Het toepassen van segmenten is nuttig als u metriek voor een ondergroep van uw gegevens in uw analyse wilt gebruiken.

>[!NOTE]
>
>De definities van het segment worden bijgewerkt door de [ bouwer van het Segment ](/help/components/filters/filter-builder.md). Als u een verandering in een segment aanbrengt, wordt het segment automatisch bijgewerkt overal het wordt gebruikt, met inbegrip van als het segment deel van een berekende metrische definitie uitmaakt.
>

Je wilt meetgegevens vergelijken voor Duitse mensen die interageren met je merk versus mensen buiten Duitsland. U kunt dus vragen beantwoorden zoals:

1. Hoeveel Duitse versus internationale mensen bezoeken uw meest [ populaire pagina&#39;s ](#popular-pages).
1. Hoeveel Duitse versus internationale mensen in [ totaal ](#totals) online met uw merk deze maand hebben gecommuniceerd.
1. Wat zijn de [ percentages ](#percentages) van Duitsers en internationale mensen die uw populaire pagina&#39;s hebben bezocht?

Zie de volgende secties om te illustreren hoe u deze vragen kunt beantwoorden met gesegmenteerde meetgegevens. In voorkomend geval wordt verwezen naar meer gedetailleerde documentatie.

## Populaire pagina&#39;s

1. [ creeer berekende metrisch ](cm-workflow.md) van een project van Workspace, genoemd `German people`.
1. Van binnen de [ Berekende metrische bouwer ](cm-build-metrics.md), [ creeer een segment ](/help/components/filters/filter-builder.md), getiteld `Germany`, dat het gebied van het Land van CRM van uw gegevens van CRM gebruikt om te bepalen waar een persoon van komt.

   >[!TIP]
   >
   >In de Berekende metrische bouwer, kunt u een segment tot stand brengen direct gebruikend het paneel van Componenten.
   >   

   Je segment zou er zo kunnen uitzien.

   ![ Filter Duitsland ](assets/filter-germany.png)

1. Terug in de Berekende metrische bouwer, gebruik het segment om berekende metrisch bij te werken.

   ![ Berekende metrisch Duitsland ](assets/calculated-metric-germany.png)

Herhaal bovenstaande stappen voor de internationale versie van de berekende metrische waarde.

1. Maak een berekende metrische waarde van het Workspace-project met de naam `International people` .
1. Van binnen de Berekende metrische bouwer, creeer een segment, genoemd `Not Germany`, dat het gebied van het Land van CRM van uw gegevens van CRM gebruikt om te bepalen waar een persoon uit komt.

   Uw segment zou moeten kijken als.

   ![ Filter Duitsland ](assets/filter-not-germany.png)

1. Terug in de Berekende metrische bouwer, gebruik het segment om berekende metrisch bij te werken.

   ![ Berekende metrisch Duitsland ](assets/calculated-metric-notgermany.png)


1. Maak een project in Analysis Workspace, waar je kijkt naar pagina&#39;s die door Duitse en internationale mensen worden bezocht.

   ![ de lijstvisualisatie van de Freeform van Workspace die Duits vs. Internationale mensen toont ](assets/workspace-german-vs-international.png)


## Totalen

1. Maak twee nieuwe segmenten op basis van Eindtotaal. Open elk van de eerder gemaakte segmenten, wijzig de naam van het segment, stel de **[!UICONTROL Metric type]** for **[!UICONTROL People]** to **[!UICONTROL Grand Total]** in en gebruik **[!UICONTROL Save As]** om het segment op te slaan met de nieuwe naam. Bijvoorbeeld:

   ![ Totale metrisch voor Duitsland ](assets/calculated-metric-germany-total.png)

1. Voeg een nieuwe tabelvisualisatie voor vrije vorm toe aan uw Workspace-project en geef het totaal aantal pagina&#39;s voor deze maand weer.

   ![ de lijstvisualisatie van de Freeform van Workspace die Duits vs. Internationale totale mensen toont ](assets/workspace-german-vs-international-totals.png)


## Percentage

1. Creeer twee nieuwe berekende metriek die een percentage van de berekende metriek berekenen u vroeger creeerde.

   ![ de lijstvisualisatie van Workspace Freeform die Duits vs. Internationaal totaal personenpercentage ](assets/calculated-metric-germany-total-percentage.png) toont


1. Werk uw Workspace-project bij.

   ![ de lijstvisualisatie van de Freeform van Workspace die Duits vs. Internationale totale mensen toont ](assets/workspace-german-vs-international-totals-percentage.png)



>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ gebruiken gesegmenteerd berekend metrisch als implementationless metrisch ](https://video.tv.adobe.com/v/25407?quality=12&learn=on){target="_blank"} voor een demo video.

{{videoaa}}

>[!ENDSHADEBOX]

