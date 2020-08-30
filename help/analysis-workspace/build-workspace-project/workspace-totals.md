---
description: Hoe de totalen van de Werkruimte worden berekend.
title: totalen van werkruimte
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 1%

---


# totalen van werkruimte

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

In de lijsten Freeform, verschijnt een totale rij op elk uitsplitsingsniveau en kan twee totalen tonen:

* **[!UICONTROL Grand Total]** (grijs &#39;out of&#39; nummer) - dit totaal vertegenwoordigt alle treffers die zijn verzameld, soms &#39;report suite total&#39; genoemd. Wanneer een segment of op het paneelniveau of binnen de freeformlijst wordt toegepast, past dit totaal aan om op alle treffers te wijzen die de segmentcriteria aanpassen.
* **[!UICONTROL Table Total]** (zwart getal) - dit totaal is doorgaans gelijk aan of een subset van de [!UICONTROL Grand Total]. Het wijst op om het even welke lijstfilters die binnen de freeform lijst worden toegepast, met inbegrip van [!UICONTROL Include None] optie.

![](assets/total-row.png)

## Totale instellingen weergeven

onder **[!UICONTROL Column Settings]**, er zijn mogelijkheden om **[!UICONTROL Show Totals]** en **[!UICONTROL Show Grand Total]**. Als deze montages ongecontroleerd zijn, zullen de totalen uit de lijst worden verwijderd. Dit kan worden gewenst in gevallen waarin totalen bijvoorbeeld in bepaalde gevallen niet zinvol zijn [Berekende metrische scenario&#39;s](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/calcmetrics-reference/cm-totals.html).

![](assets/column-settings-total.png)

## Statische Rij Totale instellingen

[Statische rij](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/build-workspace-project/column-row-settings/manual-vs-dynamic-rows.html) de totalen gedragen zich verschillend en worden gecontroleerd volgens **[!UICONTROL Row Settings]**.

* **[!UICONTROL Show sum of current rows as the total]** - dit toont een cliënt-zijsom de rijen in de lijst wat betekent het totaal zal **niet** deduplicatie-metingen zoals bezoeken of bezoekers.
* **[!UICONTROL Show Grand Total]** - dit toont een server-zijsom, wat betekent het totaal zal decoduplo metriek zoals bezoeken of bezoekers.

![](assets/static-rows.png)

## Veelgestelde vragen

| Vragen | Antwoord |
|---|---|
| Welk &quot;totaal&quot;zijn de grijze kolompercentages die op worden gebaseerd? | Dit hangt af van de **[!UICONTROL Percentages]** het plaatsen van selectie onder **[!UICONTROL Row Settings]**:<ul><li>Bereken percentages door kolom - dit is het standaard plaatsen. De percentages zullen op het Totaal van de Lijst worden gebaseerd.</li><li>Berekend percentages per rij - Percentages worden gebaseerd op het Grand Total.</li></ul> |
| Hoe doet de **[!UICONTROL Include Unspecified (None)]** het plaatsen van effecttotalen? | Als de **[!UICONTROL Include Unspecified (None)]** het plaatsen is ongecontroleerd, zal niets/de Niet gespecificeerde rij uit de lijst, het Totaal van de Lijst worden verwijderd, en zal door aan om het even welke berekende metriek voeren die gebruiken [&quot;Totaal&quot; metrieke typen](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/calcmetric-workflow/m-metric-type-alloc.html) |
| Wanneer de filters van de douanelijst op een freeform lijst worden toegepast, doe elk van mijn berekende metriek en voorwaardelijke het formatteren rekening voor de filter? | Momenteel niet. **[!UICONTROL Include Unspecified (None)]** zal rekenschap worden gegeven, maar de filters van de douanelijst zullen niet het volgende beïnvloeden:<ul><li>De kolom maximum/minwaaier die het voorwaardelijke formatteren gebruik over alle gegevens zal kijken.</li><li>Berekende maatstaven die hefboomwerking **[!UICONTROL Grand Total]** metrische types.</li><li>Berekende waarden met functies die over rijen in een vrije vormlijst - d.w.z. kolomsom, kolom max, kolom min, telling, gemiddelde, mediaan, percentiel, rij, standaardafwijking, variantie, cumulatief, cumulatief gemiddelde, regressievarianten, T-score, T-test, Z-score, Z-test.</li></ul> |
| In Berekende Metriek, wat doet het **[!UICONTROL Grand Total]** metrisch type reflecteert? | **[!UICONTROL Grand Total]** blijft verwijzen naar de **[!UICONTROL Grand Total]**, en geeft geen filters weer die op een tabel of **[!UICONTROL Table Total]**. |
| Welk totaal wordt getoond wanneer het gegeven of van een freeform lijst wordt gekopieerd en wordt gekleefd of via CSV wordt gedownload? | De totale rij zal op de **[!UICONTROL Table Total]** alleen en met inachtneming van de kolom **[!UICONTROL Show Totals]** instelling. |

