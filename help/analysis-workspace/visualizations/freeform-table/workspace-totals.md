---
description: Hoe de totalen van de werkruimte worden berekend.
title: Totalen werkruimte
translation-type: tm+mt
source-git-commit: 8b814137a7c5e2ca96091addb5b4430e2da65329
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 1%

---


# Totalen werkruimte

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

In Freeform-tabellen wordt op elk uitsplitsingsniveau een totale rij weergegeven met twee totalen:

* **[!UICONTROL Grand Total]** (grijs &#39;out of&#39; getal) - dit totaal vertegenwoordigt alle resultaten die zijn verzameld, soms &#39;report suite total&#39; genoemd. Wanneer een segment wordt toegepast op deelvensterniveau of binnen de vrije-vormtabel, wordt dit totaal aangepast aan alle resultaten die overeenkomen met de segmentcriteria.
* **[!UICONTROL Table Total]** (zwart getal) - dit totaal is doorgaans gelijk aan of een subset van het  [!UICONTROL Grand Total]object. Het geeft alle tabelfilters weer die binnen de vrije-vormtabel worden toegepast, inclusief de optie [!UICONTROL Include None].

![](assets/total-row.png)

## Totale instelling weergeven

Onder **[!UICONTROL Column Settings]**, zijn er opties aan **[!UICONTROL Show Totals]** en **[!UICONTROL Show Grand Total]**. Als deze instellingen zijn uitgeschakeld, worden de totalen uit de tabel verwijderd. Dit kan gewenst zijn in gevallen waarin totalen niet zinvol zijn, bijvoorbeeld in bepaalde [Berekende metrische scenario&#39;s](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/calcmetrics-reference/cm-totals.html).

![](assets/column-settings-total.png)

## Statische rijtotaal, instellingen

[Statische ](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md) rowtotalen gedragen zich anders en worden onder  **[!UICONTROL Row Settings]** controle gehouden.

* **[!UICONTROL Show sum of current rows as the total]** - hier ziet u een som van de rijen in de tabel aan de clientzijde, wat betekent dat het totaal geen  **** dubbele meetgegevens bevat, zoals bezoeken of bezoekers.
* **[!UICONTROL Show Grand Total]** - dit toont een bedrag aan serverzijde, wat betekent het totaal metriek zoals bezoeken of bezoekers zal dedupliceren.

![](assets/static-rows.png)

## Veelgestelde vragen

| Vragen | Antwoord |
|---|---|
| Op welke &#39;total&#39; zijn de grijze kolompercentages gebaseerd? | Dit is afhankelijk van de instelling **[!UICONTROL Percentages]** onder **[!UICONTROL Row Settings]**:<ul><li>Percentage berekenen op kolom - Dit is de standaardinstelling. Percentages worden gebaseerd op het totaal van de tabel.</li><li>Percentage berekenen op rij - Percentages worden gebaseerd op het Eindtotaal.</li></ul> |
| Hoe beïnvloedt het plaatsen **[!UICONTROL Include Unspecified (None)]** totalen? | Als **[!UICONTROL Include Unspecified (None)]** het plaatsen wordt ongecontroleerd, zal Geen/Niet gespecificeerde rij worden verwijderd uit de lijst, het Totaal van de Lijst, en zal door aan om het even welke berekende metriek overgaan die [&#39;Total&#39; metrische types](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/calcmetric-workflow/m-metric-type-alloc.html) gebruiken |
| Wanneer de filters van de douanetabel op een vrije vormlijst worden toegepast, doe al mijn berekende metriek en voorwaardelijke het formatteren rekening voor de filter? | Momenteel niet. **[!UICONTROL Include Unspecified (None)]** worden in de berekening opgenomen, maar aangepaste tabelfilters hebben geen invloed op het volgende:<ul><li>Het max/min-bereik van de kolom dat bij voorwaardelijke opmaak wordt gebruikt, wordt door alle gegevens bekeken.</li><li>Berekende metriek die hefboomwerking **[!UICONTROL Grand Total]** metrische types.</li><li>Berekende metriek met functies die over rijen in een vrije-vormlijst - d.w.z. Kolomsom, Kolommaximum, Kolom min, Aantal, Gemiddeld, Mediaan, Percentage, Aantal, Rijen, Standaardafwijking, Variantie, Cumulatief, Cumulatief Gemiddelde, Regressievarianten, T-Score, T-Test, Z-Score, Z-Test berekenen.</li></ul> |
| Wat weerspiegelt het metrische type **[!UICONTROL Grand Total]** in Berekende metriek? | **[!UICONTROL Grand Total]** blijft naar de tabel verwijzen  **[!UICONTROL Grand Total]** en geeft geen filters weer die op een tabel of de tabel zijn toegepast  **[!UICONTROL Table Total]**. |
| Welk totaal wordt getoond wanneer de gegevens of van een vrije vormlijst worden gekopieerd en worden gekleefd of via CSV worden gedownload? | De totale rij geeft alleen de **[!UICONTROL Table Total]** weer en neemt de instelling voor de kolom **[!UICONTROL Show Totals]** in acht. |

