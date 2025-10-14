---
title: Instellingen van component Attributie
description: Hiermee kunt u de standaardattributie voor een metrische waarde instellen.
exl-id: bc7ae6e3-7c9b-4994-97ce-690f3bdcbee5
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: 3c13ae26a9ef48454467fc21b8faaa9e078c7f9f
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Instellingen van component Attributie {#attribution-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_component_metric_attribution"
>title="Attributie"
>abstract="Vorm het standaardattributiemodel dat op metrisch in rapporten wordt toegepast."

<!-- markdownlint-enable MD034 -->


Met Attributie kunt u aanpassen hoe dimensie-items krediet krijgen voor succesgebeurtenissen.

![&#x200B; de meningsvenster van Gegevens die de Vastgestelde attributieoptie benadrukken &#x200B;](../assets/attribution-settings.png)

Bijvoorbeeld:

1. Een persoon op uw site klikt op een koppeling naar een betaalde zoekopdracht naar een van uw productpagina&#39;s. Ze voegen het product aan hun winkelwagentje toe, maar kopen het niet.
2. De volgende dag zien ze een bericht in de sociale media van een van hun vrienden. Ze klikken op de koppeling en voltooien de aankoop.

In sommige rapporten wilt u mogelijk de volgorde toewijzen aan Geavanceerd zoeken. In andere rapporten, zou u de orde aan Sociaal kunnen willen worden toegeschreven. Met kenmerk kunt u dit aspect van rapportage beheren.

## Standaardtoewijzingsmodel van een component instellen

U kunt een standaardattributiemodel voor bepaalde metrisch plaatsen door metrisch het plaatsen in de gegevensmening bij te werken. Als u dit doet, overschrijft u het attributiemodel van de maateenheid op elk moment dat het in Analysis Workspace wordt gebruikt.

>[!NOTE]
>
>Houd rekening met het volgende wanneer u attributie op een metrische waarde inschakelt:
>
>* **wanneer het gebruiken van de component in een rapport met *één enkele afmeting*:** de attributie van de component negeert het toewijzingsmodel wanneer een niet-gebrek attributiemodel wordt gebruikt.
>
>* **wanneer het gebruiken van de component in een rapport met *veelvoudige afmetingen*:** de attributie van de component behoudt het toewijzingsmodel wanneer een niet-gebrek attributiemodel wordt gebruikt.
>
>   De veelvoudige afmetingen zijn beschikbaar slechts wanneer [&#x200B; het uitvoeren van gegevens aan de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md).
>
> Voor meer informatie over toewijzing, zie {de montages van de componenten van 0} Persistence [&#128279;](/help/data-views/component-settings/persistence.md).

Het standaardtoewijzingsmodel van een component bijwerken:

1. Ga naar de gegevensmening die de component bevat waarvan standaardattributiemodel u wilt bijwerken.

1. Selecteer de component en vouw vervolgens de sectie **[!UICONTROL Attribution]** aan de rechterkant van het scherm uit.

   ![&#x200B; de meningsvenster van Gegevens die de Vastgestelde attributieoptie benadrukken &#x200B;](../assets/attribution-settings.png)

1. Selecteer [!UICONTROL **Vastgestelde attributie**], dan selecteren het [&#x200B; attributiemodel &#x200B;](#attribution-models), [&#x200B; container &#x200B;](#container) en [&#x200B; raadplegings &#x200B;](#lookback-window) venster.



1. Selecteer [!UICONTROL **sparen en ga**] verder.

>[!TIP]
>
>Als uw organisatie vereist dat metrisch veelvoudige attributie montages heeft, kunt u één van het volgende doen:
>
> * Kopieer de metrische waarde in de gegevensweergave met elke gewenste attributie-instelling. U kunt dezelfde metrische waarde meerdere keren opnemen in een gegevensweergave, zodat elke meting een andere instelling heeft. Zorg ervoor dat u elke metrisch geschikt etiketteert zodat de analisten het verschil tussen deze metriek begrijpen wanneer het produceren van rapporten.
>
> * Overschrijf de metrische waarde in Analysis Workspace. In de montages van de Kolom van metrische [&#128279;](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md), uitgezochte **[!UICONTROL Use non-default attribution model]** om het de attributiemodel van metrische metrische te veranderen en raadplegingsvenster voor dat specifieke rapport.

## Attributiemodellen {#attribution-models}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataviews_component_attribution_attributionmodels"
>title="Model"
>abstract="Selecteer een attributiemodel voor metrisch."

<!-- markdownlint-enable MD034 -->

{{attribution-models-details}}

## Container

{{attribution-container}}

## Venster Opzoeken

{{attribution-lookback-window}}

## Voorbeeld

{{attribution-example}}
