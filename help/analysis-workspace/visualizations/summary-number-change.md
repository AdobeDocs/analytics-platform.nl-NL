---
description: Gebruik het Summiere aantal en de Summiere veranderingsvisualisaties om belangrijke gegevenspunten in een project te tonen.
title: Samenvattingsnummer en samenvattingswijziging
feature: Visualizations
exl-id: 8872fc58-0957-415d-9958-ce564612ce87
role: User
source-git-commit: 639c3d3c349615078c76f8806bcd5bb458b0f6f2
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Samenvattingsnummer en wijziging

>[!BEGINSHADEBOX]

_dit artikel documenteert het Summiere aantal en de Summiere veranderingsvisualisaties in_ ![&#x200B; CustomerJourneyAnalytics &#x200B;](/help/assets/icons/CustomerJourneyAnalytics.svg) _&#x200B;**Customer Journey Analytics**._<br/>_zie [&#x200B; Summiere aantal en Summiere verandering &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/analyze/analysis-workspace/visualizations/summary-number-change) voor_ ![&#x200B; AdobeAnalytics &#x200B;](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics** versie van dit artikel._

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; Summiere aantal en Summiere veranderingsvisualisatie &#x200B;](https://video.tv.adobe.com/v/335564/?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]

## Samenvattingsnummer {#summary-number}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_summarynumber_button"
>title="Samenvattingsnummer"
>abstract="Maak een visualisatie met totalen en subtotalen."

<!-- markdownlint-enable MD034 -->

Gebruik ![&#x200B; vat &#x200B;](/help/assets/icons/123.svg) samen **[!UICONTROL Summary number]** visualisatie om een groot aantal te benadrukken dat in een project belangrijk is. Deze visualisatie gedraagt zich op de volgende manieren, gebruikend de bijbehorende gegevensbron:

* Hiermee selecteert u het totaal van de kolom als er geen cel is geselecteerd.
* Als er één cel is geselecteerd, wordt het overzicht voor die cel weergegeven.
* Als er meer dan één cel is geselecteerd, wordt de eerste geselecteerde cel weergegeven.
* Als de kolom is geselecteerd, wordt de eerste celwaarde in de kolom gekozen.

![&#x200B; Summiere aantalvisualisatie &#x200B;](asses/../assets/summary-number.png)

Als onderdeel van de visualisatie-instellingen zijn specifieke opties voor het overzichtsnummer beschikbaar.

| Optie | Definitie |
|--- |--- |
| **[!UICONTROL Abbreviate value]** | Selecteer **[!UICONTROL Abbreviate value]** om de getalwaarde op een intelligente manier te verkorten. Als deze optie is geselecteerd, voert u een getal in om de hoeveelheid afkorting te definiëren. Bijvoorbeeld:<br/><table><tr><td>**Oorspronkelijke waarde**</td><td>**Afkorting waarde**</td><td>**Resultaat**</td></tr><tr><td>$ 12.011.141,25</td><td>Niet geselecteerd</td><td  align="right">$ 12.011.141,25</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, instellen op `0`</td><td align="right">$ 12 MB</td></tr><tr><td>$ 12.011.141,25</td><td> Geselecteerd, instellen op `1`</td><td  align="right">$ 12,0 MB</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, instellen op `2`</td><td align="right">$ 12,01M</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, instellen op `3`</td><td align="right">$ 12,011M</td></tr></table> |
| **[!UICONTROL Summarize value by]** | Kies of u de maximale, minimale, gemiddelde, mediaan of som voor een selectie gegevens wilt weergeven. |

## Samenvattingswijziging {#summary-change}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_summarychange_button"
>title="Samenvattingswijziging"
>abstract="Maak een visualisatie die de delta (wijziging) tussen twee getallen toont"

<!-- markdownlint-enable MD034 -->


Gebruik ![&#x200B; MoveUpDown &#x200B;](/help/assets/icons/MoveUpDown.svg) **[!UICONTROL Summary Change]** visualisatie om de delta (verandering) tussen twee aantallen te tonen. <!-- This is applicable for AA, not CJA: The green and red color of the Summary Change can be controlled through [custom event polarity](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/success-events/success-event.html?lang=nl-NL) or a calculated metric's [Show Upward Trend As](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html?lang=nl-NL) option.-->

<!--
The green and red color of the Summary Change can be controlled through [custom event polarity](https://experienceleague.adobe.com/docs/analytics/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) or a calculated metric's [Show Upward Trend As](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html?lang=nl-NL) option.
-->

Deze visualisatie werkt op de volgende manieren:

* Als er geen cel is geselecteerd, worden de eerste twee celwaarden in de kolom vergeleken.
* Als er één cel is geselecteerd, wordt 0 weergegeven, omdat de celwaarde dan met zichzelf wordt vergeleken.
* Als twee cellen zijn geselecteerd, wordt de eerste geselecteerde cel als teller en de tweede als noemer genomen.
* Als er meer dan twee cellen zijn geselecteerd, worden alleen de eerste twee ter vergelijking gebruikt.
* Als een bereik cellen is geselecteerd, wordt het eerste veld vergeleken met de laatste cellen in het bereik.
* Als de kolom wordt geselecteerd, vergelijkt het de eerste waarde met zich, die een verandering van 0 toont.


![&#x200B; Summiere verandering visualisatie die de delta tussen twee numbers.s toont &#x200B;](assets/summary-change.png)


Als onderdeel van de visualisatie-instellingen is specifieke **[!UICONTROL Summary change options]** beschikbaar.

| Optie | Definitie |
|--- |--- |
| **[!UICONTROL Show percent change]** | De procentuele wijziging tussen de twee getallen weergeven. |
| **[!UICONTROL Show raw difference]** | Het onbewerkte verschil tussen de twee getallen tonen. Met deze optie kunt u ook waarden afbreken en maximaal drie decimalen weergeven. |
| **[!UICONTROL Abbreviate value]** | Selecteer **[!UICONTROL Abbreviate value]** om de gewijzigde waarde op een intelligente manier af te korting. Als deze optie is geselecteerd, voert u een getal in om de hoeveelheid afkorting te definiëren. Bijvoorbeeld:<br/><table><tr><td>**Oorspronkelijke waarde**</td><td>**Afkorting waarde**</td><td>**Resultaat**</td></tr><tr><td>$ 12.011.141,25</td><td>Niet geselecteerd</td><td  align="right">$ 12.011.141,25</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, instellen op `0`</td><td align="right">$ 12 MB</td></tr><tr><td>$ 12.011.141,25</td><td> Geselecteerd, instellen op `1`</td><td  align="right">$ 12,0 MB</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, instellen op `2`</td><td align="right">$ 12,01M</td></tr><tr><td>$ 12.011.141,25</td><td>Geselecteerd, instellen op `3`</td><td align="right">$ 12,011M</td></tr></table> |

>[!MORELIKETHIS]
>
>[&#x200B; voeg een visualisatie aan een paneel toe &#x200B;](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>&#x200B;>[Visualisatie-instellingen &#x200B;](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>&#x200B;>[Contextmenu Visualisatie &#x200B;](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>
