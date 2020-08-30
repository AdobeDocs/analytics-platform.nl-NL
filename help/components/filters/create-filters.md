---
title: Filters maken
description: Begrijp het gebruikersinterface van de filterverwezenlijking.
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---


# Filters maken

De ontwerper van de Filter verstrekt een canvas om metriek, afmetingen, filters, en gebeurtenissen aan filterbezoekers te slepen en te laten vallen die op de logica van de containerhiërarchie, regels, en exploitanten worden gebaseerd. Dit geïntegreerde ontwikkelingshulpmiddel laat u eenvoudige of complexe filters bouwen en bewaren die bezoekersattributen en acties over bezoeken en paginakijken identificeren.

U kunt onmiddellijke filters tot stand brengen door om het even welk componententype (afmeting, afmetingspunt, gebeurtenis, metrisch, segment, segmentmalplaatje, datumwaaier) in de streek van de filterdaling bij de bovenkant van een paneel te laten vallen.

De types van component worden auto-omgezet in filters. U kunt ook op het &quot;+&quot;-teken klikken in het **[!UICONTROL Add Filter]** druppel.

Vergeet niet dat:

* Jij **niet** laat vallen de volgende componententypes in de filterstreek: berekende metriek en afmetingen/metriek waarvan u geen filters kunt bouwen.
* Voor volledige afmetingen en gebeurtenissen, leidt de Werkruimte van de Analyse tot &quot;bestaat&quot;klapfilters. Voorbeelden: &quot;Plaats waar eVar1 bestaat&quot; of &quot;hit waar event1 bestaat&quot;.
* Als &quot;niet gespecificeerd&quot;of &quot;niets&quot;in de streek van de filterdaling wordt gelaten vallen, wordt het automatisch omgezet in een &quot;niet bestaat&quot;filter zodat het correct wordt behandeld.

![](assets/segment-dropzone.png)

>[!NOTE]
>
>De filters creeerden deze manier zijn intern aan het project.

U kunt verkiezen om deze filters openbaar (globaal) te maken door deze stappen te volgen:

1. Beweeg de filter in de dalingsstreek en klik het &quot;i&quot;pictogram.
1. In het informatiepaneel dat toont, klik **[!UICONTROL Make public]**.

   ![](assets/segment-info.png)

## Andere methoden voor het toepassen van filters

Verscheidene andere methodes bestaan voor het toepassen van filters op een project:

| Actie | Beschrijving |
|--- |--- |
| Filter maken uit selectie | Creeer een gealigneerde filter. Selecteer rijen, klik de selectie met de rechtermuisknop aan, dan creeer een gealigneerde filter. Deze filter is alleen van toepassing op het open project en wordt niet opgeslagen als CJA-filter. 1. Selecteer rijen.  2. Klik met de rechtermuisknop op de selectie.  3. Klik *Filter maken uit selectie*. |
| Componenten > Nieuw filter | Toont de Bouwer van de Filter. Zie [Filter ontwerper](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-build.html) voor meer informatie over het filtreren. |
| Delen > Project delen of delen > Projectgegevens aanpassen | In [Curate en share](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html#concept_4A9726927E7C44AFA260E2BB2721AFC6), leer hoe de filters die u op het project toepast in gedeelde analyse voor de ontvanger beschikbaar zijn. |
| Filters gebruiken als afmetingen | Video: [Het gebruiken van Segmenten als Afmetingen in de Werkruimte van de Analyse](https://www.youtube.com/watch?v=WmSdReKTWto&amp;list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS&amp;index=39) |
