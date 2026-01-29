---
title: Datumbereiknamen gebruiken om te filteren
description: Gebruik datumbereiknamen om het gebruik van hoofdletters en kleine letters voor de BI-extensie in verschillende BI-gereedschappen in Customer Journey Analytics te filteren
solution: Customer Journey Analytics
feature: Data Views
role: User
source-git-commit: 0962f64e9bc0fed89f52191bebe6dd0e14bde61d
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 1%

---

# Namen van datumbereik gebruiken om te filteren

In dit geval wilt u een datumbereik gebruiken dat u in Customer Journey Analytics hebt gedefinieerd om gebeurtenissen (gebeurtenissen) in het laatste jaar te filteren en te rapporteren.

+++ Customer Journey Analytics

Als u een datumbereik wilt rapporteren, stelt u in Customer Journey Analytics een datumbereik in met **[!UICONTROL Title]** `Last Year 2023` .

![&#x200B; de Namen van de Datumwaaier van het Gebruik van Customer Journey Analytics aan filter &#x200B;](../assets/cja-daterange.png)

Vervolgens kunt u dat datumbereik gebruiken in een voorbeelddeelvenster **[!UICONTROL Using Date Range Names To Filter]** voor het gebruik van hoofdletters en kleine letters:

![&#x200B; de Afzonderlijke Waarden van de Telling van Customer Journey Analytics &#x200B;](../assets/cja-using-date-range-filter-names-to-filter.png)

Bedenk hoe het datumbereik dat in de visualisatie van de tabel Freeform is gedefinieerd, het datumbereik overtreft dat op het deelvenster wordt toegepast.

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [&#x200B; een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening &#x200B;](connect-and-validate.md) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL daterangemonth]**.
   1. Selecteer **[!UICONTROL daterangeName]**.
   1. Selecteer **[!UICONTROL sum occurrences]**.

   Er wordt een visualisatie weergegeven **[!UICONTROL Error fetching data for this visual]** .

1. In het deelvenster **[!UICONTROL Filters]** :

   1. Selecteer de **[!UICONTROL daterangeName is (All)]** van **[!UICONTROL Filters on this visual]**.
   1. Selecteer **[!UICONTROL Basic filtering]** als de **[!UICONTROL Filter type]** .
   1. Onder het veld **[!UICONTROL Search]** selecteert u **[!UICONTROL Last Year 2023]** . Dit is de naam van het datumbereik dat in Customer Journey Analytics is gedefinieerd.
   1. Selecteer ![&#x200B; CrossSize75 &#x200B;](/help/assets/icons/CrossSize75.svg) om **[!UICONTROL daterangeName]** uit **[!UICONTROL Columns]** te verwijderen.

   De tabel wordt bijgewerkt met het toegepaste filter **[!UICONTROL daterangeName]** . Je Power BI Desktop moet er hieronder uitzien.

   ![&#x200B; Desktop die van Power BI de Namen van de Waaier van de Datum gebruikt om te filtreren &#x200B;](../assets/uc8-powerbi-final.png)

>[!TAB  Desktop Tableau ]

1. Selecteer de tab **[!UICONTROL Sheet 1]** onderaan om te schakelen van **[!UICONTROL Data source]** . In de weergave **[!UICONTROL Sheet 1]** :
   1. Sleep de vermelding **[!UICONTROL Daterange Name]** uit de lijst **[!UICONTROL Tables]** in de lijst **[!UICONTROL Filters]** .
   1. Controleer in het dialoogvenster **[!UICONTROL Filter \[Daterange Name\]]** of **[!UICONTROL Select from list]** is geselecteerd en selecteer **[!UICONTROL Last Year 2023]** in de lijst. Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Sleep **[!UICONTROL Daterangemonth]** -item uit de **[!UICONTROL Tables]** -lijst en zet de vermelding in het veld naast **[!UICONTROL Rows]** neer. Selecteer **[!UICONTROL Daterangemonth]** en selecteer **[!UICONTROL Month]** . De waarde verandert in **[!UICONTROL MONTH(Daterangemonth)]** .
   1. Sleep **[!UICONTROL Occurrences]** -item uit de **[!UICONTROL Tables]** -lijst en zet de vermelding in het veld naast **[!UICONTROL Columns]** neer. De waarde verandert in **[!UICONTROL SUM(Occurrences)]** .
   1. Selecteer **[!UICONTROL Text Table]** in **[!UICONTROL Show Me]** .
   1. Selecteer **[!UICONTROL Swap Rows and Columns]** op de werkbalk.
   1. Selecteer **[!UICONTROL Fit Width]** in de vervolgkeuzelijst **[!UICONTROL Fit]** .

      Uw Tableau Desktop moet er hieronder uitzien.

      ![&#x200B; de Veelvoudige Rangschikte Filter van de Desktop van Tableau Dimension &#x200B;](../assets/uc8-tableau-final.png)

>[!TAB  Leider ]

1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![&#x200B; Plaatsende &#x200B;](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Name]** in de lijst met velden.
1. Geef het filter **[!UICONTROL Cc Data View Daterange Name]** op als **[!UICONTROL is]** en selecteer **[!UICONTROL Last Year 2023]** in de lijst met waarden.
1. Vanuit het gedeelte **[!UICONTROL ‣ Cc Data View]** in de linkertrack:
   1. Selecteer **[!UICONTROL Daterange Month]** en vervolgens **[!UICONTROL Month]** .
   1. Selecteer **[!UICONTROL Count]** onder **[!UICONTROL MEASURES]** in de linkertrack (onder).
1. Selecteer **[!UICONTROL Run]**.
1. Selecteer **[!UICONTROL ‣ Visualization]**.

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![&#x200B; minder duidelijke telling &#x200B;](../assets/uc8-looker-result.png)


>[!TAB  Jupyter Notitieboekje ]

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   data = %sql SELECT daterangeName FROM cc_data_view;
   style = {'description_width': 'initial'}
   daterange_name = widgets.Dropdown(
      options=[d for d, in data],
      description='Date Range Name:',
      style=style
   )
   display(daterange_name)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![&#x200B; Jupyter de Resultaten van het Notitieboekje &#x200B;](../assets/uc8-jupyter-input.png)

1. Selecteer **[!UICONTROL Fishing Products]** in de vervolgkeuzelijst.

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   import seaborn as sns
   import matplotlib.pyplot as plt
   data = %sql SELECT daterangemonth AS Month, COUNT(*) AS Events \
               FROM cc_data_view \
               WHERE daterangeName = '{daterange_name.value}' \
               GROUP BY 1 \
               ORDER BY Month ASC
   df = data.DataFrame()
   df = df.groupby('Month', as_index=False).sum()
   plt.figure(figsize=(15, 3))
   sns.lineplot(x='Month', y='Events', data=df)
   plt.show()
   display(data)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![&#x200B; Jupyter de Resultaten van het Notitieboekje &#x200B;](../assets/uc8-jupyter-results.png)


>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ` ``{r} ` en ` `` ` ` in een nieuw segment in. Zorg ervoor dat u de juiste naam voor het datumbereik gebruikt. Bijvoorbeeld `Last Year 2023` .

   ```R
   ## Monthly Events for Last Year
   df <- dv %>%
      filter(daterangeName == "Last Year 2023") %>%
      group_by(daterangemonth) %>%
      count() %>%
      arrange(daterangemonth, .by_group = FALSE)
   ggplot(df, aes(x = daterangemonth, y = n)) +
      geom_line(color = "#69b3a2") +
      ylab("Events") +
      xlab("Hour")
   print(df)
   ```

1. Voer het segment uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![&#x200B; Resultaten RStudio &#x200B;](../assets/uc8-rstudio-results.png)

>[!ENDTABS]

+++

