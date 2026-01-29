---
title: Dagelijkse trend
description: Dagelijkse trendgebruikscase voor de BI-extensie in verschillende BI-gereedschappen in Customer Journey Analytics
solution: Customer Journey Analytics
feature: Data Views
role: User
source-git-commit: 0962f64e9bc0fed89f52191bebe6dd0e14bde61d
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 1%

---

# Dagelijkse trend


In dit geval wilt u een tabel en eenvoudige lijnvisualisatie weergeven met een dagelijkse trend van voorvallen (gebeurtenissen) van 1 januari 2023 tot 31 januari 2023.

+++ Customer Journey Analytics

Een voorbeeldvenster **[!UICONTROL Daily Trend]** voor het hoofdlettergebruik:

![ Customer Journey Analytics het Dagelijkse paneel van de Trend ](../assets/cja_daily_trend.png)

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u a [ succesvolle verbinding en kunt gegevensmeningen ](connect-and-validate.md) voor het hulpmiddel bevestigen en gebruiken BI waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL daterangeday]**.
   1. Selecteer **[!UICONTROL sum occurrences]**.

   Er wordt een tabel weergegeven met de exemplaren voor de huidige maand. Vergroot de visualisatie voor een betere zichtbaarheid.

1. In het deelvenster **[!UICONTROL Filters]** :

   1. Selecteer de **[!UICONTROL daterangeday is (All)]** van **[!UICONTROL Filters on this visual]**.
   1. Selecteer **[!UICONTROL Advanced filtering]** als de **[!UICONTROL Filter type]** .
   1. Definieer het filter op **[!UICONTROL Show items when the value]** **[!UICONTROL is on or after]** `1/1/2023` **[!UICONTROL And]** **[!UICONTROL is before]** `2/1/2023.` U kunt het kalenderpictogram gebruiken om datums te selecteren en te selecteren.
   1. Selecteer **[!UICONTROL Apply filter]**.

   De tabel wordt bijgewerkt met het toegepaste filter **[!UICONTROL daterangeday]** .

1. Selecteer in het deelvenster **[!UICONTROL Visualizations]** de **[!UICONTROL Line chart]** visualisatie.

   Een lijngrafiekvisualisatie vervangt de lijst terwijl het gebruiken van de zelfde gegevens zoals de lijst. Je Power BI Desktop moet er hieronder uitzien.

   ![ Geval van het Gebruik van de Desktop van Power BI 2 de waaierfilter van de Datum ](../assets/uc2-pbi-daterange.png)

1. Op het grafiekvisualisatie van de Lijn:

   1. Selecteer ![ Meer ](/help/assets/icons/More.svg).
   1. Selecteer **[!UICONTROL Show as a table]** in het contextmenu.

   De hoofdweergave wordt bijgewerkt om zowel een lijnvisualisatie als een tabel weer te geven. Je Power BI Desktop moet er hieronder uitzien.

   ![ Geval 2 van het Gebruik van de Desktop van Power BI Def. Dagelijkse Tendvisualisatie ](../assets/uc2-pbi-final.png)

>[!TAB  Desktop Tableau ]

1. Selecteer de tab **[!UICONTROL Sheet 1]** onderaan om te schakelen van de weergave **[!UICONTROL Data source]** . In de weergave **[!UICONTROL Sheet 1]** :
   1. Sleep de vermelding **[!UICONTROL Daterange]** uit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet deze op de **[!UICONTROL Filters]** shelf neer.
   1. Selecteer **[!UICONTROL Filters Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer **[!UICONTROL Filter \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of dates]** en geef een punt op van `01/01/2023` - `01/02/2023` .

      ![ de Filter van de Desktop van Tableau ](../assets/uc2-tableau-filter.png)

   1. Sleep **[!UICONTROL Daterangeday]** vanuit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet de vermelding in het veld naast **[!UICONTROL Columns]** neer.
      * Selecteer **[!UICONTROL Day]** in de vervolgkeuzelijst **[!UICONTROL Daterangeday]** , zodat de waarde wordt bijgewerkt naar **[!UICONTROL DAY(Daterangeday)]** .
   1. De belemmering en laat vallen **[!UICONTROL Occurrences]** van de **[!UICONTROL Tables (*Namen van de Maatregel *)]**lijst in de **[!UICONTROL Data]**ruit en laat vallen de ingang op het gebied naast **[!UICONTROL Rows]**. De waarde wordt automatisch omgezet in **[!UICONTROL SUM(Occurrences)]**.
   1. Wijzig **[!UICONTROL Standard]** in **[!UICONTROL Entire View]** in het vervolgkeuzemenu **[!UICONTROL Fit]** op de werkbalk.

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Grafiek van de Desktop van Tableau ](../assets/uc2-tableau-graph.png)

1. Selecteer **[!UICONTROL Duplicate]** in het contextmenu van de tab **[!UICONTROL Sheet 1]** om een tweede blad te maken.
1. Selecteer **[!UICONTROL Rename]** in het contextmenu van de tab **[!UICONTROL Sheet 1]** om de naam van het werkblad te wijzigen in `Graph` .
1. Selecteer **[!UICONTROL Rename]** in het contextmenu van de tab **[!UICONTROL Sheet 1 (2)]** om de naam van het werkblad te wijzigen in `Data` .
1. Zorg ervoor dat het **[!UICONTROL Data]** -werkblad is geselecteerd. In de weergave **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL Show me]** rechtsboven en selecteer **[!UICONTROL Text table]** (bovenste visualisatie linksboven) om de inhoud van de gegevensweergave te wijzigen in een tabel.
   1. Selecteer **[!UICONTROL Swap Rows and Columns]** op de werkbalk.
   1. Wijzig **[!UICONTROL Standard]** in **[!UICONTROL Entire View]** in het vervolgkeuzemenu **[!UICONTROL Fit]** op de werkbalk.

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Gegevens van de Desktop van Tableau ](../assets/uc2-tableau-data.png)

1. Selecteer de tabknop **[!UICONTROL New Dashboard]** (onder) om een nieuwe **[!UICONTROL Dashboard 1]** -weergave te maken. In de weergave **[!UICONTROL Dashboard 1]** :
   1. Sleep en laat vallen het **[!UICONTROL Graph]** blad van **[!UICONTROL Sheets]** plank op de **[!UICONTROL Dashboard 1]** mening die *Dropbladen hier* leest.
   1. Sleep het **[!UICONTROL Data]** -werkblad van de **[!UICONTROL Sheets]** -plank onder het **[!UICONTROL Graph]** -werkblad naar de **[!UICONTROL Dashboard 1]** -weergave.
   1. Selecteer het **[!UICONTROL Data]** -werkblad in de weergave en wijzig **[!UICONTROL Entire View]** in **[!UICONTROL Fix Width]** .

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Dashboard 1 van de Desktop van Tableau ](../assets/uc2-tableau-dashboard.png)


>[!TAB  Leider ]

1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![ Plaatsende ](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![ filter van de Leider ](../assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2023/02/01]** .
1. Vanaf het gedeelte **[!UICONTROL Cc Data View]** in de linkerspoorstaaf,
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en **[!UICONTROL Date]** in de lijst met **[!UICONTROL DIMENSIONS]** .
   1. Selecteer **[!UICONTROL Count]** onder **[!UICONTROL MEASURES]** in de linkertrack (onder).
1. Selecteer **[!UICONTROL Run]**.
1. Selecteer **[!UICONTROL ‣ Visualization]** om de lijnvisualisatie weer te geven.

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![ Minder resultaat dagelijkse trend ](../assets/uc2-looker-result.png)


>[!TAB  Jupyter Notitieboekje ]

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   import seaborn as sns
   import matplotlib.pyplot as plt
   data = %sql SELECT daterangeday AS Date, COUNT(*) AS Events \
             FROM cc_data_view \
             WHERE daterange BETWEEN '2023-01-01' AND '2023-02-01' \
             GROUP BY 1 \
             ORDER BY Date ASC
   df = data.DataFrame()
   df = df.groupby('Date', as_index=False).sum()
   plt.figure(figsize=(15, 3))
   sns.lineplot(x='Date', y='Events', data=df)
   plt.show()
   display(data)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Jupyter de Resultaten van het Notitieboekje ](../assets/uc2-jupyter-results.png)


>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ```{r} ` en ` ``` ` in een nieuw segment in.

   ```R
   ## Daily Events
   df <- dv %>%
      filter(daterange >= "2023-01-01" & daterange < "2023-02-01") %>%
      group_by(daterangeday) %>%
      count() %>%
      arrange(daterangeday, .by_group = FALSE)
   ggplot(df, aes(x = daterangeday, y = n)) +
      geom_line(color = "#69b3a2") +
      ylab("Events") +
      xlab("Date")
   print(df)
   ```

1. Voer het segment uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Resultaten RStudio ](../assets/uc2-rstudio-results.png)

>[!ENDTABS]

+++
