---
description: Leer hoe u prognoses in een tabel of in een lijndiagram bekijkt.
title: De prognoses in Analysis Workspace bekijken
feature: Visualizations
role: User
source-git-commit: e52cee369be75785a99798d5acfa9cfc5aba2986
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Prognoses weergeven in Analysis Workspace

U kunt prognoses in een vrije-vormlijst of in een lijngrafiek bekijken.

## Prognoses weergeven in een tabel

U kunt prognoses in een tijdreeksvrije lijst bekijken. Als Voorspelling tonen is ingeschakeld voor tabel Freeform in [gebruikersvoorkeuren](../user-preferences.md), wordt het voorspellen automatisch getoond voor de eerste metrische kolom die aan de lijst wordt toegevoegd. Voor elke andere kolom:

1. Het pictogram voor kolominstellingen selecteren ![Kolominstellingen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg) in de kolomkop zorgt u ervoor dat **[!UICONTROL Show forecast]** wordt geselecteerd in de lijst met opties. Zie voor meer informatie [Kolominstellingen](../visualizations/freeform-table/column-row-settings/column-settings.md).

1. Klik buiten de **[!UICONTROL Column settings]** om de instelling op te slaan en de bijgewerkte tabel weer te geven.

De prognoses zijn als volgt weergegeven:

![Voorspelling weergeven in tabel](assets/show-forecast-table.png)

* De geraamde waarde en het percentage voor elke cel worden weergegeven in **donkergrijs**.
* Om een voorspelde waarde aan te geven, een voorspeld symbool <img src="./assets/forecast.svg" alt="Prognose-symbool" width="20" /> wordt in de rechterbovenhoek van de cel weergegeven.


## Prognoses weergeven in een lijndiagram

Een lijngrafiek is de enige visualisatie die u toestaat om prognoses te bekijken.

1. Het pictogram Instellingen selecteren ![Kolominstellingen](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg) in de visualisatiekoptekst en zorg er vervolgens voor dat **[!UICONTROL Show forecast]** wordt geselecteerd in de lijst met opties.

1. (optioneel) Selecteer **[!UICONTROL Allow forecast to scale Y-axis]**. Deze optie is niet standaard geselecteerd omdat deze soms een minder leesbaar diagram kan weergeven.

1. Klik buiten de **[!UICONTROL Settings]** om het bijgewerkte regeldiagram weer te geven.

De prognoses worden als volgt weergegeven in het lijndiagram:

![Voorspelling weergeven in lijndiagram](assets/show-forecast-linechart.png)

* De huidige waarden voor de metriek in het lijndiagram worden aangegeven door een verticale balk. Als u de cursor boven die verticale lijn houdt, wordt een pop-up weergegeven met de laatste huidige datum.
* De voorspelde waarden voor één of meerdere metriek worden getoond recht van de verticale bar gebruikend gestippelde lijnen. U kunt de muisaanwijzer boven elk gegevenspunt voor een metrische waarde plaatsen. Dit toont een popup met:
   * datum van de prognose
   * voorspelde waarde voor de metrische waarde
   * bovengrens van voorspelde waarde voor de metrische waarde
   * ondergrens van voorspelde waarde voor de metrische waarde
* de schaduw geeft de betrouwbaarheidsmarge van de voorspelling weer .

