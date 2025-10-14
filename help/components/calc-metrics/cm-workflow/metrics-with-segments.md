---
description: Leer hoe te op individuele metriek te segmenteren die u toestaat om metrische vergelijkingen binnen de zelfde visualisatie te maken.
title: Gesegmenteerde cijfers
feature: Calculated Metrics
exl-id: 37cc93df-9f51-42b3-918f-ed5864991621
source-git-commit: c209341400bf4e0c00719075f0fc82f81ca9dbb4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Gesegmenteerde metriek

In de [&#x200B; Berekende metrische bouwer &#x200B;](cm-build-metrics.md#definition-builder), kunt u segmenten binnen uw metrische definitie toepassen. Het toepassen van segmenten is nuttig als u metriek voor een ondergroep van uw gegevens in uw analyse wilt gebruiken.

>[!NOTE]
>
>De definities van het segment worden bijgewerkt door de [&#x200B; bouwer van het Segment &#x200B;](/help/components/segments/seg-builder.md). Als u een verandering in een segment aanbrengt, wordt het segment automatisch bijgewerkt overal het wordt gebruikt, met inbegrip van als het segment deel van een berekende metrische definitie uitmaakt.
>

Je wilt meetgegevens vergelijken voor Duitse mensen die interageren met je merk versus mensen buiten Duitsland. U kunt dus vragen beantwoorden zoals:

1. Hoeveel Duitse versus internationale mensen bezoeken uw meest [&#x200B; populaire pagina&#39;s &#x200B;](#popular-pages).
1. Hoeveel Duitse versus internationale mensen in [&#x200B; totaal &#x200B;](#totals) online met uw merk deze maand hebben gecommuniceerd.
1. Wat zijn de [&#x200B; percentages &#x200B;](#percentages) van Duitsers en internationale mensen die uw populaire pagina&#39;s hebben bezocht?

Zie de volgende secties om te illustreren hoe u deze vragen kunt beantwoorden met gesegmenteerde meetgegevens. In voorkomend geval wordt verwezen naar meer gedetailleerde documentatie.

## Populaire pagina&#39;s

1. [&#x200B; creeer berekende metrisch &#x200B;](cm-workflow.md) van een project van Workspace, genoemd `German people`.
1. Van binnen de [&#x200B; Berekende metrische bouwer &#x200B;](cm-build-metrics.md), [&#x200B; creeer een segment &#x200B;](/help/components/segments/seg-builder.md), getiteld `Germany`, dat het gebied van het Land van CRM van uw gegevens van CRM gebruikt om te bepalen waar een persoon van komt.

   >[!TIP]
   >
   >In de Berekende metrische bouwer, kunt u een segment tot stand brengen direct gebruikend het paneel van Componenten.
   >   

   Je segment zou er zo kunnen uitzien.

   ![&#x200B; Segment Duitsland &#x200B;](assets/filter-germany.png)

1. Terug in de Berekende metrische bouwer, gebruik het segment om berekende metrisch bij te werken.

   ![&#x200B; Berekende metrisch Duitsland &#x200B;](assets/calculated-metric-germany.png)

Herhaal bovenstaande stappen voor de internationale versie van de berekende metrische waarde.

1. Maak een berekende metrische waarde van het Workspace-project met de naam `International people` .
1. Van binnen de Berekende metrische bouwer, creeer een segment, genoemd `Not Germany`, dat het gebied van het Land van CRM van uw gegevens van CRM gebruikt om te bepalen waar een persoon uit komt.

   Uw segment zou moeten kijken als.

   ![&#x200B; Segment Duitsland &#x200B;](assets/filter-not-germany.png)

1. Terug in de Berekende metrische bouwer, gebruik het segment om berekende metrisch bij te werken.

   ![&#x200B; Berekende metrisch Duitsland &#x200B;](assets/calculated-metric-notgermany.png)


1. Maak een project in Analysis Workspace, waar je kijkt naar pagina&#39;s die door Duitse en internationale mensen worden bezocht.

   ![&#x200B; de lijstvisualisatie van de Freeform van Workspace die Duits vs. Internationale mensen toont &#x200B;](assets/workspace-german-vs-international.png)


## Totalen

1. Creeer twee nieuwe berekende metriek die op het Grote Totaal wordt gebaseerd. Open elk van de eerder gemaakte segmenten, wijzig de naam van het segment, stel de **[!UICONTROL Metric type]** for **[!UICONTROL People]** to **[!UICONTROL Grand Total]** in en gebruik **[!UICONTROL Save As]** om het segment op te slaan met de nieuwe naam. Bijvoorbeeld:

   ![&#x200B; Totale metrisch voor Duitsland &#x200B;](assets/calculated-metric-germany-total.png)

1. Voeg een nieuwe tabelvisualisatie voor vrije vorm toe aan uw Workspace-project en geef het totaal aantal pagina&#39;s voor deze maand weer.

   ![&#x200B; de lijstvisualisatie van de Freeform van Workspace die Duits vs. Internationale totale mensen toont &#x200B;](assets/workspace-german-vs-international-totals.png)


## Percentage

1. Creeer twee nieuwe berekende metriek die een percentage van de berekende metriek berekenen u vroeger creeerde.

   ![&#x200B; de lijstvisualisatie van Workspace Freeform die Duits vs. Internationaal totaal personenpercentage &#x200B;](assets/calculated-metric-germany-total-percentage.png) toont


1. Werk uw Workspace-project bij.

   ![&#x200B; de lijstvisualisatie van de Freeform van Workspace die Duits vs. Internationale totale mensen toont &#x200B;](assets/workspace-german-vs-international-totals-percentage.png)



>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; gebruiken gesegmenteerd berekend metrisch als implementationless metrisch &#x200B;](https://video.tv.adobe.com/v/25407?quality=12&learn=on){target="_blank"} voor een demo video.

{{videoaa}}

>[!ENDSHADEBOX]

