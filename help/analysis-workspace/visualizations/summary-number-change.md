---
description: Gebruik het Summiere Aantal en de visualisaties van de Verandering om belangrijke gegevenspunten in een project te tonen.
title: Samenvattingsnummer en Samenvattingswijziging
feature: Visualizations
exl-id: 8872fc58-0957-415d-9958-ce564612ce87
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 1%

---

# Samenvattingsnummer en Samenvattingswijziging

## Visualisatie van overzichtsnummers {#summary-number}

Gebruik de Summiere visualisatie van het Aantal om een groot aantal te benadrukken dat in een project belangrijk is. Deze visualisatie werkt op de volgende manieren:

* Hiermee selecteert u het totaal van de kolom als er geen cel is geselecteerd.
* Als er één cel is geselecteerd, wordt het overzicht voor die cel weergegeven.
* Als er meer dan één cel is geselecteerd, wordt de eerste geselecteerde cel weergegeven.
* Als de kolom is geselecteerd, wordt de eerste celwaarde in de kolom gekozen.

Klik op de knop **Visualisatie-instellingen** tandwieltje in de rechterbovenhoek om de Summiere montages van het Aantal te vormen:

| Instelling | Definitie |
|--- |--- |
| Percentage | Geef percentages weer in plaats van onbewerkte getallen. |
| Legenda zichtbaar | De informatie van de vertoning over metrisch getoond. |
| Afkorting | Kies of u waarden wilt afbreken en maximaal 3 decimalen wilt weergeven. |
| Waarde samenvatten met | Kies of u de maximale, minimale, gemiddelde, mediaan of som voor een selectie gegevens wilt weergeven. |

{style="table-layout:auto"}

## Visualisatie overzichtswijziging {#summary-change}

Gebruik de visualisatie van de Overzichtsverandering om de delta (verandering) tussen twee aantallen te tonen. De groene en rode kleur van de Summiere Verandering kan door worden gecontroleerd [polariteit aangepaste gebeurtenis](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/success-events/success-event.html) of een berekende metrieke waarde [Toon Opwaartse trend als](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html) -optie.

Deze visualisatie werkt op de volgende manieren:

* Als er geen cel is geselecteerd, worden de eerste twee celwaarden in de kolom vergeleken.
* Als er één cel is geselecteerd, wordt 0 weergegeven, omdat de celwaarde dan met zichzelf wordt vergeleken.
* Als twee cellen zijn geselecteerd, wordt de eerste geselecteerde cel als teller en de tweede als noemer genomen.
* Als er meer dan twee cellen zijn geselecteerd, worden alleen de eerste twee ter vergelijking gebruikt.
* Als een bereik cellen is geselecteerd, wordt het eerste veld vergeleken met de laatste cellen in het bereik.
* Als de kolom wordt geselecteerd, vergelijkt het de eerste waarde met zich, die een verandering van 0 toont.


![Samenvattingswijziging visualisatie met de delta tussen twee getallen](assets/summary-change.png)


Klik op de knop **Visualisatie-instellingen** Wijs in het hoogste recht aan om de Summiere montages van de Verandering te vormen:

| Instelling | Definitie |
|--- |--- |
| Percentage | Geef percentages weer in plaats van onbewerkte getallen. |
| Legenda zichtbaar | De informatie van de vertoning over metrisch getoond. |
| Percentage wijziging tonen | Geeft de procentuele wijziging tussen de twee getallen weer. |
| Onbewerkt verschil tonen | Geeft het onbewerkte verschil weer tussen de twee getallen. Met deze optie kunt u ook waarden afbreken en maximaal drie decimalen weergeven. |
