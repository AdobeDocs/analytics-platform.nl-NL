---
description: Leer hoe u prognoses in een tabel of in een lijndiagram bekijkt.
title: De prognoses in Analysis Workspace bekijken
feature: Visualizations
role: User
exl-id: 4a8b602c-e6aa-4a46-bba9-642387e6af88
source-git-commit: a646d1f35308dc1f1d9f06cf94835534bd8b8da6
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# Prognoses weergeven in Analysis Workspace

U kunt prognoses in een vrije-vormlijst of in een lijngrafiek bekijken.

## Prognoses weergeven in een tabel

U kunt prognoses in een tijdreeksvrije lijst bekijken. Wanneer [!UICONTROL Show forecast] voor de lijst van de Vrije vorm in [ gebruikersvoorkeur ](../user-preferences.md) wordt toegelaten, wordt het voorspellen automatisch getoond voor de eerste metrische kolom die aan de lijst wordt toegevoegd. Voor elke andere kolom:

1. Selecteer het pictogram van kolommontages ![ de montages van de Kolom ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg) in de kolomkopbal, dan zorg ervoor dat **[!UICONTROL Show forecast]** in de lijst van opties wordt geselecteerd. Voor meer informatie, zie [ montages van de Kolom ](../visualizations/freeform-table/column-row-settings/column-settings.md).

1. Klik buiten het menu **[!UICONTROL Column settings]** om de instelling op te slaan en de bijgewerkte tabel weer te geven.

De prognoses zijn als volgt weergegeven:

![ toon prognose in lijst ](assets/show-forecast-table.png)

* De voorspelde waarde en het percentage voor elke cel worden getoond in **donkergrijs**.
* Om op een voorspelde waarde te wijzen, wordt een voorspeld symbool ![ ForecastAnalytics ](/help/assets/icons/ForecastAnalytics.svg) getoond in de hoger-juiste hoek van de cel.


## Prognoses weergeven in een lijndiagram

Een lijngrafiek is de enige visualisatie die u toestaat om prognoses te bekijken.

1. Selecteer de montages van de montagespictogram ![ Kolom ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg) in de visualisatiekopbal, dan zorg ervoor dat **[!UICONTROL Show forecast]** in de lijst van opties wordt geselecteerd.

1. (optioneel) Selecteer **[!UICONTROL Allow forecast to scale Y-axis]** als u wilt dat de prognoses correct worden geschaald. Deze optie is niet standaard geselecteerd omdat deze soms een minder leesbaar diagram kan weergeven.

1. Klik buiten het menu **[!UICONTROL Settings]** om het bijgewerkte regeldiagram weer te geven.

De prognoses worden als volgt weergegeven in het lijndiagram:

![ toon prognose in lijngrafiek ](assets/show-forecast-linechart.png)

* De huidige waarden voor de metriek in het lijndiagram worden aangegeven door een verticale balk. Als u de cursor boven die verticale lijn houdt, wordt een pop-up weergegeven met de laatste huidige datum.
* De voorspelde waarden voor één of meerdere metriek worden getoond recht van de verticale bar gebruikend gestippelde lijnen. U kunt de muisaanwijzer boven elk gegevenspunt voor een metrische waarde plaatsen. Dit toont een popup met:
   * datum van de prognose
   * voorspelde waarde voor de metrische waarde
   * bovengrens van voorspelde waarde voor de metrische waarde
   * ondergrens van voorspelde waarde voor de metrische waarde
* Het schaduwgebied toont de betrouwbaarheidsmarge van de voorspelling.
