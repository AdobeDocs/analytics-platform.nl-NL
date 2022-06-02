---
title: Filters maken
description: Begrijp de gebruikersinterface van de filterverwezenlijking.
exl-id: b6a921d5-7dd3-4230-88b8-5f1cd313b791
source-git-commit: 7013237e11cb173d54dcbe236967b49d89810975
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# Filters maken

De Filterbouwer verstrekt een canvas om metriek, afmetingen, filters, en gebeurtenissen te slepen en te laten vallen aan filterbezoekers die op de logica van de containerhiërarchie, regels, en exploitanten worden gebaseerd. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige of complexe filters maken en opslaan waarmee bezoekerskenmerken en handelingen tijdens bezoeken en paginakijken worden geïdentificeerd.

U kunt ogenblikkelijke filters tot stand brengen door om het even welk componententype (afmeting, afmetingpunt, gebeurtenis, metrisch, filter, filtermalplaatje, datumwaaier) in de gebied van de filterdaling bij de bovenkant van een paneel te laten vallen.

Componenttypen worden automatisch omgezet in filters. U kunt ook op het plusteken (+) klikken in het dialoogvenster **[!UICONTROL Add Filter]** dropbox.

Houd er rekening mee dat:

* U **kan** Zet de volgende componenttypen neer in de filterzone: berekende metriek en afmetingen/metriek waarvan u geen filters kunt bouwen.
* Voor volledige afmetingen en gebeurtenissen maakt Analysis Workspace &#39;exists&#39; raakfilters. Voorbeelden: &quot;Druk op de plaats waar eVar1 bestaat&quot; of &quot;druk op de plaats waar event1 bestaat&quot;.
* Als &#39;unspecified&#39; of &#39;none&#39; wordt neergezet in de neerzetzone van het filter, wordt deze automatisch omgezet in een filter &#39;does not exist&#39;, zodat deze correct wordt behandeld.

![](assets/segment-dropzone.png)

>[!NOTE]
>
>Filters die op deze manier worden gemaakt, zijn intern voor het project.

U kunt deze filters openbaar (algemeen) maken door de volgende stappen uit te voeren:

1. Houd de muisaanwijzer boven het filter in de neerzetzone en klik op het pictogram &quot;i&quot;.
1. Klik in het informatievenster dat wordt weergegeven op **[!UICONTROL Make public]**.

   ![](assets/segment-info.png)

## Andere methoden voor het toepassen van filters

Er zijn verschillende andere methoden voor het toepassen van filters op een project:

| Handeling | Beschrijving |
| --- | --- |
| Filter van selectie maken | Maak een inlinefilter. Dit filter is alleen van toepassing op het geopende project en wordt niet opgeslagen als een CJA-filter.<p> 1. Selecteer welke tabelrijen u wilt opnemen in het filter.  2. Klik met de rechtermuisknop op de selectie.  3. Klikken *Filter van selectie maken*. |
| Werkruimte [!UICONTROL Components] > [!UICONTROL New Filter] | Geeft de Filter Builder weer. Zie [Filter Builder](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) voor meer informatie over filteren. |
| Delen > Project delen of Delen > Projectgegevens krommen | In [Curven en delen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html#concept_4A9726927E7C44AFA260E2BB2721AFC6)leert u hoe de filters die u op het project toepast, beschikbaar zijn in een gedeelde analyse voor de ontvanger. |
| Filters gebruiken als afmetingen | Zie onderstaande video: Filters gebruiken als Dimension in Analysis Workspace |

>[!VIDEO](https://video.tv.adobe.com/v/23974)
