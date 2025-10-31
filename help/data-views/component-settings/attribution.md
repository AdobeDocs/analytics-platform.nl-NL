---
title: Instellingen van component Attributie
description: Hiermee kunt u de standaardattributie voor een metrische waarde instellen.
exl-id: bc7ae6e3-7c9b-4994-97ce-690f3bdcbee5
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: 2fd79da264d60bb90e1193ead2eee67602404b4c
workflow-type: tm+mt
source-wordcount: '430'
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

Bijvoorbeeld:

1. Een persoon op uw site klikt op een koppeling naar een betaalde zoekopdracht naar een van uw productpagina&#39;s. Ze voegen het product aan hun winkelwagentje toe, maar kopen het niet.
2. De volgende dag zien ze een bericht in de sociale media van een van hun vrienden. Ze klikken op de koppeling en voltooien de aankoop.

In sommige rapporten wilt u mogelijk de volgorde toewijzen aan Geavanceerd zoeken. In andere rapporten, zou u de orde aan Sociaal kunnen willen worden toegeschreven. Met kenmerk kunt u dit aspect van rapportage beheren.

## Het toewijzingsmodel van een component instellen

U kunt het standaardattributiemodel voor een bepaalde component wijzigen door de instelling van de component in de gegevensweergave bij te werken. Als u dit doet, overschrijft u het toewijzingsmodel van de component op elk moment dat het in Analysis Workspace wordt gebruikt.

>[!NOTE]
>
>Houd rekening met het volgende wanneer u een niet-standaard attributiemodel op een metrische waarde inschakelt:
>
>* **wanneer het gebruiken van metrisch in een rapport met *één enkele afmeting*:** de attributie van metrische treedt metrische het toewijzingsmodel met voeten dat op de afmeting wordt geplaatst. Een metrische waarde met een kenmerk &quot;first touch&quot; heeft bijvoorbeeld voorrang op een toewijzing van de &quot;meest recente&quot; dimensie.
>
>* **wanneer het gebruiken van metrisch in een rapport met *veelvoudige afmetingen*:** de attributie van metrische wordt toegepast bovenop het toewijzingsmodel voor elke afmeting. Bijvoorbeeld, wordt metrisch met een &quot;eerste aanraking&quot;attributie toegepast bovenop een &quot;meest recente&quot;afmetingstoewijzing.
>
> Voor meer informatie over toewijzing, zie {de montages van de componenten van 0} Persistence [.](/help/data-views/component-settings/persistence.md)

Het standaardtoewijzingsmodel van een component bijwerken:

1. Ga naar de gegevensmening die de component bevat waarvan standaardattributiemodel u wilt bijwerken.

1. Selecteer de component en vouw vervolgens de sectie **[!UICONTROL Attribution]** aan de rechterkant van het scherm uit.

   ![ de meningsvenster van Gegevens die de Vastgestelde attributieoptie benadrukken ](../assets/attribution-settings.png)

1. Selecteer [!UICONTROL **Vastgestelde attributie**], dan selecteren het [ attributiemodel ](#attribution-models), [ container ](#container) en [ raadplegings ](#lookback-window) venster.



1. Selecteer [!UICONTROL **sparen en ga**] verder.

>[!TIP]
>
>Als uw organisatie vereist dat metrisch veelvoudige attributie montages heeft, kunt u één van het volgende doen:
>
> * Kopieer de metrische waarde in de gegevensweergave met elke gewenste attributie-instelling. U kunt dezelfde metrische waarde meerdere keren opnemen in een gegevensweergave, zodat elke meting een andere instelling heeft. Zorg ervoor dat u elke metrisch geschikt etiketteert zodat de analisten het verschil tussen deze metriek begrijpen wanneer het produceren van rapporten.
>
> * Overschrijf de metrische waarde in Analysis Workspace. In de montages van de Kolom van metrische [ ](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md), uitgezochte **[!UICONTROL Use non-default attribution model]** om het de attributiemodel van metrische metrische te veranderen en raadplegingsvenster voor dat specifieke rapport.

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
