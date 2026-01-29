---
title: Segmentnamen gebruiken voor segment
description: Gebruik segmentnamen voor segmentgebruik voor de BI-extensie in verschillende BI-gereedschappen in Customer Journey Analytics
solution: Customer Journey Analytics
feature: Data Views
role: User
source-git-commit: 0962f64e9bc0fed89f52191bebe6dd0e14bde61d
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 1%

---

# Segmentnamen gebruiken

In dit geval wilt u een bestaand segment gebruiken voor de categorie visserijproducten die u in Customer Journey Analytics hebt gedefinieerd. Segmenteren en rapporteren over productnamen en voorvallen (gebeurtenissen) in januari 2023.

+++ Customer Journey Analytics

Controleer het segment dat u in Customer Journey Analytics wilt gebruiken.

![&#x200B; Customer Journey Analytics gebruiken de Namen van de Filter &#x200B;](../assets/cja-fishing-products.png)

Vervolgens kunt u dat segment in een voorbeeldvenster van **[!UICONTROL Using Segment Names To Segment]** gebruiken voor het gebruik van hoofdletters en kleine letters:

![&#x200B; de Afzonderlijke Waarden van de Telling van Customer Journey Analytics &#x200B;](../assets/cja-using-filter-names-to-filter.png)

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [&#x200B; een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening &#x200B;](connect-and-validate.md) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL daterange]**.
   1. Selecteer **[!UICONTROL filterName]**.
   1. Selecteer **[!UICONTROL product_name]**.
   1. Selecteer **[!UICONTROL sum occurrences]**.

Er wordt een visualisatie weergegeven **[!UICONTROL Error fetching data for this visual]** .

1. In het deelvenster **[!UICONTROL Filters]** :

   1. Selecteer **[!UICONTROL filterName is (All)]** in **[!UICONTROL Filters on this visual]** .
   1. Selecteer **[!UICONTROL Basic filtering]** als de **[!UICONTROL Filter type]** .
   1. Onder het veld **[!UICONTROL Search]** selecteert u **[!UICONTROL Fishing Products]** . Dit is de naam van het bestaande filter dat in Customer Journey Analytics is gedefinieerd.
   1. Selecteer **[!UICONTROL daterange is (All)]** in **[!UICONTROL Filters on this visual]** .
   1. Selecteer **[!UICONTROL Advanced filtering]** als de **[!UICONTROL Filter type]** .
   1. Definieer het filter naar **[!UICONTROL Show items when the value]** **[!UICONTROL is on or after]** `1/1/2023` **[!UICONTROL And]** **[!UICONTROL is before]** `2/1/2023` .
   1. Selecteer ![&#x200B; CrossSize75 &#x200B;](/help/assets/icons/CrossSize75.svg) om **[!UICONTROL filterName]** uit **[!UICONTROL Columns]** te verwijderen.
   1. Selecteer ![&#x200B; CrossSize75 &#x200B;](/help/assets/icons/CrossSize75.svg) om **[!UICONTROL daterange]** uit **[!UICONTROL Columns]** te verwijderen.

   De tabel wordt bijgewerkt met het toegepaste filter **[!UICONTROL filterName]** . Je Power BI Desktop moet er hieronder uitzien.

   ![&#x200B; Desktop die van Power BI de Namen van de Waaier van de Datum gebruikt om te filtreren &#x200B;](../assets/uc9-powerbi-final.png)


>[!TAB  Desktop Tableau ]

1. Selecteer de tab **[!UICONTROL Sheet 1]** onderaan om te schakelen van **[!UICONTROL Data source]** . In de weergave **[!UICONTROL Sheet 1]** :
   1. Sleep de vermelding **[!UICONTROL Filter Name]** uit de lijst **[!UICONTROL Tables]** in de lijst **[!UICONTROL Filters]** .
   1. Controleer in het dialoogvenster **[!UICONTROL Filter \[Filter Name\]]** of **[!UICONTROL Select from list]** is geselecteerd en selecteer **[!UICONTROL Fishing Products]** in de lijst. Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Sleep **[!UICONTROL Daterange]** -item uit de lijst **[!UICONTROL Tables]** in de **[!UICONTROL Filters]** -lijst.
   1. Selecteer **[!UICONTROL Filter Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer **[!UICONTROL Filter \[Daterang\]]** in het dialoogvenster **[!UICONTROL Range of dates]** en selecteer `01/01/2023` - `01/02/2023` . Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Sleep **[!UICONTROL Product Name]** van de **[!UICONTROL Tables]** lijst aan **[!UICONTROL Rows]**.
   1. Sleep **[!UICONTROL Occurrences]** -item uit de **[!UICONTROL Tables]** -lijst en zet de vermelding in het veld naast **[!UICONTROL Columns]** neer. De waarde verandert in **[!UICONTROL SUM(Occurrences)]** .
   1. Selecteer **[!UICONTROL Text Table]** in **[!UICONTROL Show Me]** .
   1. Selecteer **[!UICONTROL Fit Width]** in de vervolgkeuzelijst **[!UICONTROL Fit]** .

      Uw Tableau Desktop moet er hieronder uitzien.

      ![&#x200B; de Veelvoudige Rangschikte Filter van de Desktop van Tableau Dimension &#x200B;](../assets/uc9-tableau-final.png)

>[!TAB  Leider ]

1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![&#x200B; Plaatsende &#x200B;](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![&#x200B; filter van de Leider &#x200B;](../assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2023/02/01]** .
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** om nog een filter toe te voegen.
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Filter name]** in de lijst met velden.
1. Controleer **[!UICONTROL is]** de selectie voor het filter.
1. Selecteer **[!UICONTROL Fishing Products]** in de lijst met mogelijke waarden.
1. Vanuit het gedeelte **[!UICONTROL ‣ Cc Data View]** in de linkertrack:
   1. Selecteer **[!UICONTROL Product Name]**.
   1. Selecteer **[!UICONTROL Count]** onder **[!UICONTROL MEASURES]** in de linkertrack (onder).
1. Selecteer **[!UICONTROL Run]**.
1. Selecteer **[!UICONTROL ‣ Visualization]**.

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![&#x200B; minder duidelijke telling &#x200B;](../assets/uc9-looker-result.png)



>[!TAB  Jupyter Notitieboekje ]

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   data = %sql SELECT filterName FROM cc_data_view;
   style = {'description_width': 'initial'}
   filter_name = widgets.Dropdown(
      options=[d for d, in data],
      description='Filter Name:',
      style=style
   )
   display(filter_name)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![&#x200B; Jupyter de Resultaten van het Notitieboekje &#x200B;](../assets/uc9-jupyter-input.png)

1. Selecteer **[!UICONTROL Fishing Products]** in de vervolgkeuzelijst.

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   import seaborn as sns
   import matplotlib.pyplot as plt
   data = %sql SELECT product_name AS `Product Name`, COUNT(*) AS Events \
               FROM cc_data_view \
               WHERE daterange BETWEEN '2023-01-01' AND '2023-02-01' \
                  AND filterName = '{filter_name.value}' \
               GROUP BY 1 \
               LIMIT 10;
   df = data.DataFrame()
   df = df.groupby('Product Name', as_index=False).sum()
   plt.figure(figsize=(15, 3))
   sns.barplot(x='Events', y='Product Name', data=df)
   plt.show()
   display(data)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![&#x200B; Jupyter de Resultaten van het Notitieboekje &#x200B;](../assets/uc9-jupyter-results.png)


>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ` ``{r} ` en ` `` ` ` in een nieuw segment in. Controleer of u de juiste filternaam gebruikt. Bijvoorbeeld `Fishing Products` .

   ```R
   ## Dimension filtered by name
   df <- dv %>%
      filter(daterange >= "2023-01-01" & daterange < "2023-02-01" & filterName == "Fishing Products") %>%
      group_by(product_name) %>%
      count() %>%
      arrange(desc(n), .by_group = FALSE)
   print(df)
   ```

1. Voer het segment uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![&#x200B; Resultaten RStudio &#x200B;](../assets/uc9-rstudio-results.png)


>[!ENDTABS]

+++
