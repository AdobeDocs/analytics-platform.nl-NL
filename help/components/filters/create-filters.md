---
title: Filters maken
description: Begrijp de gebruikersinterface van de filterverwezenlijking.
translation-type: tm+mt
source-git-commit: 0c5bd5ce0b0ba4ba758a1ef1adf5a4a519e9cf8c
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---


# Filters maken

De Filterbouwer verstrekt een canvas om metriek, afmetingen, filters, en gebeurtenissen te slepen en te laten vallen aan filterbezoekers die op de logica van de containerhiërarchie, regels, en exploitanten worden gebaseerd. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige of complexe filters maken en opslaan waarmee bezoekerskenmerken en handelingen tijdens bezoeken en paginakijken worden geïdentificeerd.

U kunt onmiddellijk filters tot stand brengen door om het even welk componententype (afmeting, afmetingpunt, gebeurtenis, metrisch, segment, segmentmalplaatje, datumwaaier) in de gebied van de filterdaling bij de bovenkant van een paneel te laten vallen.

Componenttypen worden automatisch omgezet in filters. U kunt ook op het plusteken (+) klikken in het **[!UICONTROL Add Filter]** vak.

Houd er rekening mee dat:

* U **kunt de volgende componenttypen niet** neerzetten in de filterzone: berekende metriek en afmetingen/metriek waarvan u geen filters kunt bouwen.
* Voor volledige afmetingen en gebeurtenissen maakt Analysis Workspace &#39;exists&#39; raakfilters. Voorbeelden: &quot;Druk op de plaats waar eVar1 bestaat&quot; of &quot;druk op de plaats waar event1 bestaat&quot;.
* Als &#39;unspecified&#39; of &#39;none&#39; wordt neergezet in de neerzetzone van het filter, wordt deze automatisch omgezet in een filter &#39;does not exist&#39;, zodat deze correct wordt behandeld.

![](assets/segment-dropzone.png)

>[!NOTE] Filters die op deze manier worden gemaakt, zijn intern voor het project.

U kunt deze filters openbaar (algemeen) maken door de volgende stappen uit te voeren:

1. Houd de muisaanwijzer boven het filter in de neerzetzone en klik op het pictogram &quot;i&quot;.
1. Klik in het informatievenster dat wordt weergegeven **[!UICONTROL Make public]**.

   ![](assets/segment-info.png)

## Andere methoden voor het toepassen van filters

Er zijn verschillende andere methoden voor het toepassen van filters op een project:

| Handeling | Beschrijving |
|--- |--- |
| Filter van selectie maken | Maak een inlinefilter. Selecteer rijen, klik met de rechtermuisknop op de selectie en maak vervolgens een inlinefilter. Dit filter is alleen van toepassing op het geopende project en wordt niet opgeslagen als een CJA-filter. 1. Selecteer rijen.  2. Klik met de rechtermuisknop op de selectie.  3. Klik op *Filter maken van selectie*. |
| Componenten > Nieuw filter | Geeft de Filter Builder weer. Zie [Filter Builder](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-build.html) voor meer informatie over het filtreren. |
| Delen > Project delen of Delen > Projectgegevens krommen | In [Kromme en Aandeel](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html#concept_4A9726927E7C44AFA260E2BB2721AFC6), leer hoe de filters die u op het project toepast in gedeelde analyse voor de ontvanger beschikbaar zijn. |
| Filters gebruiken als afmetingen | Video: [Segmenten gebruiken als afmetingen in Analysis Workspace](https://www.youtube.com/watch?v=WmSdReKTWto&amp;list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS&amp;index=39) |
