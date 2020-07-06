---
description: 'null'
title: Cijferoverzicht en Wijzigingsoverzicht
uuid: 177c1b89-6d98-473d-8447-6b4cdc479565
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 8%

---


# Cijferoverzicht en Wijzigingsoverzicht

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

## Visualisatie overzichtsaantal

* Hiermee selecteert u het totaal van de kolom als er geen cel is geselecteerd.
* Als er één cel is geselecteerd, wordt het overzicht voor die cel weergegeven.
* Als er meer dan één cel is geselecteerd, wordt de eerste geselecteerde cel weergegeven.
* Als de kolom is geselecteerd, wordt de eerste celwaarde in de kolom gekozen.

![](assets/summary-number.png)

## Visualisatie overzichtswijziging

* Als er geen cel is geselecteerd, worden de eerste twee celwaarden in de kolom vergeleken.
* Als er één cel is geselecteerd, wordt 0 weergegeven, omdat de celwaarde dan met zichzelf wordt vergeleken.
* Als twee cellen zijn geselecteerd, wordt de eerste geselecteerde cel als teller en de tweede als noemer genomen.
* Als er meer dan twee cellen zijn geselecteerd, worden alleen de eerste twee ter vergelijking in aanmerking genomen.
* Als een bereik cellen is geselecteerd, wordt het eerste veld vergeleken met de laatste cellen in het bereik.
* Als de kolom wordt geselecteerd, vergelijkt het de eerste waarde met zich, die een verandering van 0 toont.
* De groene en rode kleur van de summiere verandering kan door worden gecontroleerd:
   * [Aangepaste gebeurtenispolariteit](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/success-events/success-event.html).
   * De berekende metrische [tonen de Naar boven gerichte Tendens als](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html) optie.

## Instellingen Samenvattingswijziging {#section_2581AC0107634FB4990AB8347E5897AA}

Klik op het tandwielpictogram naast de visualisatie om de overzichtsinstellingen te configureren:

| Instelling | Definitie |
|--- |--- |
| Percentage | Gebruik percentages in plaats van onbewerkte getallen. |
| Legenda zichtbaar | Hier worden de gebruikte meetgegevens weergegeven. |
| Opties voor samenvattingsnummer: Afkorting | U kunt kiezen uit 0 tot 3 decimalen voor afgekorte waarden. |
| Opties voor overzichtswijziging: Percentage wijziging tonen | Geeft de wijziging in procenten tussen de twee getallen weer. |
| Opties voor overzichtswijziging: Onbewerkt verschil tonen | Geeft het onbewerkte verschil weer tussen de twee getallen. |
