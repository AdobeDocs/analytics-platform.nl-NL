---
description: Hoe de totalen van de werkruimte worden berekend.
title: Totalen werkruimte
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 1%

---


# Totalen werkruimte

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

In Freeform-tabellen wordt op elk uitsplitsingsniveau een totale rij weergegeven met twee totalen:

* **[!UICONTROL Grand Total]** (grijs &#39;out of&#39; getal) - dit totaal vertegenwoordigt alle resultaten die zijn verzameld, soms &#39;report suite total&#39; genoemd. Wanneer een segment wordt toegepast op deelvensterniveau of binnen de vrije-vormtabel, wordt dit totaal aangepast aan alle resultaten die overeenkomen met de segmentcriteria.
* **[!UICONTROL Table Total]** (zwart getal) - dit totaal is doorgaans gelijk aan of een subset van het [!UICONTROL Grand Total]object. Het geeft alle tabelfilters weer die binnen de vrije-vormtabel worden toegepast, inclusief de [!UICONTROL Include None] optie.

![](assets/total-row.png)

## Totale instelling weergeven

Onder **[!UICONTROL Column Settings]**, zijn er opties aan **[!UICONTROL Show Totals]** en **[!UICONTROL Show Grand Total]**. Als deze instellingen zijn uitgeschakeld, worden de totalen uit de tabel verwijderd. Dit kan gewenst zijn in gevallen waarin totalen niet zinvol zijn, bijvoorbeeld in bepaalde [berekende metrische scenario](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/calcmetrics-reference/cm-totals.html)&#39;s.

![](assets/column-settings-total.png)

## Statische rijtotaal, instellingen

[De statische rijtotalen](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.html) gedragen zich verschillend, en worden gecontroleerd onder **[!UICONTROL Row Settings]**.

* **[!UICONTROL Show sum of current rows as the total]** - hier ziet u een som van de rijen aan de clientzijde van de tabel, wat betekent dat het totaal **niet** de dubbele meetgegevens zoals bezoeken of bezoekers zal dedupliceren.
* **[!UICONTROL Show Grand Total]** - dit toont een bedrag aan serverzijde, wat betekent het totaal metriek zoals bezoeken of bezoekers zal dedupliceren.

![](assets/static-rows.png)

## Veelgestelde vragen

| Vragen | Antwoord |
|---|---|
| Op welke &#39;total&#39; zijn de grijze kolompercentages gebaseerd? | Dit is afhankelijk van de **[!UICONTROL Percentages]** instelling onder **[!UICONTROL Row Settings]**:<ul><li>Percentage berekenen op kolom - Dit is de standaardinstelling. Percentages worden gebaseerd op het totaal van de tabel.</li><li>Percentage berekenen op rij - Percentages worden gebaseerd op het Eindtotaal.</li></ul> |
| Hoe beïnvloedt de **[!UICONTROL Include Unspecified (None)]** instelling totalen? | Als het **[!UICONTROL Include Unspecified (None)]** plaatsen wordt ongecontroleerd, zal Geen/Niet gespecificeerde rij worden verwijderd uit de lijst, het Totaal van de Lijst, en zal door aan om het even welke berekende metriek gaan die metrische types van [&quot;Totaal&quot;gebruiken](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/calcmetric-workflow/m-metric-type-alloc.html) |
| Wanneer de filters van de douanetabel op een vrije vormlijst worden toegepast, doe al mijn berekende metriek en voorwaardelijke het formatteren rekening voor de filter? | Momenteel niet. **[!UICONTROL Include Unspecified (None)]** worden in de berekening opgenomen, maar aangepaste tabelfilters hebben geen invloed op het volgende:<ul><li>Het max/min-bereik van de kolom dat bij voorwaardelijke opmaak wordt gebruikt, wordt door alle gegevens bekeken.</li><li>Berekende metriek die hefboomwerking **[!UICONTROL Grand Total]** metrische types.</li><li>Berekende metriek met functies die over rijen in een vrije-vormlijst - d.w.z. Kolomsom, Kolommaximum, Kolom min, Aantal, Gemiddeld, Mediaan, Percentage, Aantal, Rijen, Standaardafwijking, Variantie, Cumulatief, Cumulatief Gemiddelde, Regressievarianten, T-Score, T-Test, Z-Score, Z-Test berekenen.</li></ul> |
| Wat weerspiegelt het **[!UICONTROL Grand Total]** metrische type in Berekende Metriek? | **[!UICONTROL Grand Total]** blijft naar de tabel verwijzen **[!UICONTROL Grand Total]** en geeft geen filters weer die op een tabel of de tabel zijn toegepast **[!UICONTROL Table Total]**. |
| Welk totaal wordt getoond wanneer de gegevens of van een vrije vormlijst worden gekopieerd en worden gekleefd of via CSV worden gedownload? | De totale rij geeft de **[!UICONTROL Table Total]** enige waarde weer en neemt de **[!UICONTROL Show Totals]** kolominstelling in acht. |

