---
title: Limieten
description: Beperkt gebruiksgeval voor de extensie BI in verschillende BI-gereedschappen in Customer Journey Analytics
solution: Customer Journey Analytics
feature: Data Views
role: User
source-git-commit: 0962f64e9bc0fed89f52191bebe6dd0e14bde61d
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 1%

---

# Limieten


In dit geval, wilt u over de hoogste 5 voorkomen van productnamen tijdens 2023 rapporteren.

+++ Customer Journey Analytics

Een voorbeeldvenster **[!UICONTROL Limit]** voor het hoofdlettergebruik:

![&#x200B; het paneel van de Grens van Customer Journey Analytics &#x200B;](../assets/cja-limit.png)

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
   1. Selecteer **[!UICONTROL product_name]**.
   1. Selecteer **[!UICONTROL sum occurrences]**.

1. In het deelvenster **[!UICONTROL Filters]** :
   1. Selecteer **[!UICONTROL daterange is (All)]** in **[!UICONTROL Filters on this visual]** .
   1. Selecteer **[!UICONTROL Relative date]** als de **[!UICONTROL Filter type]** .
   1. Definieer het filter naar **[!UICONTROL Show items when the value]** **[!UICONTROL is in the last]** `1` **[!UICONTROL calendar years]** .
   1. Selecteer **[!UICONTROL Apply filter]**.
   1. Selecteer **[!UICONTROL product_name is (All)]** in **[!UICONTROL Filters on this visual]** .
   1. Selecteer **[!UICONTROL Top N]** als de **[!UICONTROL Filter type]** .
   1. Selecteer **[!UICONTROL Show Items]** **[!UICONTROL Top]** `5` **[!UICONTROL By value]** .
   1. Sleep **[!UICONTROL sum occurrences]** vanuit het deelvenster **[!UICONTROL Data]** en zet het neer op **[!UICONTROL Add data fields here]** .
   1. Selecteer **[!UICONTROL Apply filter]**.

1. In het deelvenster Visualisatie:
   * Selecteer ![&#x200B; CrossSize75 &#x200B;](/help/assets/icons/CrossSize75.svg) om daterange uit Kolommen te verwijderen.

   Je Power BI Desktop moet er hieronder uitzien.

   ![&#x200B; Desktop die van Power BI de Namen van de Waaier van de Datum gebruikt om te filtreren &#x200B;](../assets/uc12-powerbi-final.png)

De query die door Power BI Desktop wordt uitgevoerd met de BI-extensie bevat een `limit` -instructie, maar niet de instructie die wordt verwacht. De limiet van de bovenste vijf exemplaren wordt door Power BI Desktop afgedwongen met expliciete resultaten voor de productnaam.

```sql
select "_"."product_name",
    "_"."a0"
from 
(
    select "rows"."product_name" as "product_name",
        sum("rows"."occurrences") as "a0"
    from 
    (
        select "_"."daterangeName",
            "_"."daterange",
            "_"."filterId",
            "_"."filterName",
            "_"."timestamp",
            "_"."affiliate_name",
            "_"."affiliate_url",
            "_"."commerce.order.priceTotal",
            "_"."customer_city",
            "_"."customer_region",
            "_"."daterangeday",
            "_"."daterangefifteenminute",
            "_"."daterangefiveminute",
            "_"."daterangehour",
            "_"."daterangeminute",
            "_"."daterangemonth",
            "_"."daterangequarter",
            "_"."daterangesecond",
            "_"."daterangethirtyminute",
            "_"."daterangeweek",
            "_"."daterangeyear",
            "_"."hitdatetime",
            "_"."page_name",
            "_"."page_url",
            "_"."product_category",
            "_"."product_name",
            "_"."product_short_review",
            "_"."product_subCategory",
            "_"."referrer_url",
            "_"."search_engine",
            "_"."search_keywords",
            "_"."store_city",
            "_"."store_name",
            "_"."store_region",
            "_"."store_type",
            "_"."timepartdayofmonth",
            "_"."timepartdayofweek",
            "_"."timepartdayofyear",
            "_"."timeparthourofday",
            "_"."timepartminuteofhour",
            "_"."timepartmonthofyear",
            "_"."timepartquarterofyear",
            "_"."timepartweekofyear",
            "_"."cm_session_end_rate_defaultmetric",
            "_"."cm_session_person_defaultmetric",
            "_"."cm_session_start_rate_defaultmetric",
            "_"."cm_timespent_person_defaultmetric",
            "_"."cm_timespent_session_defaultmetric",
            "_"."cm_product_name_count_distinct",
            "_"."ad_views",
            "_"."adobe_sessionends",
            "_"."adobe_sessionstarts",
            "_"."adobe_timespent",
            "_"."exchange_buybacks",
            "_"."exchange_cost",
            "_"."exchange_purchases",
            "_"."exchange_revenue",
            "_"."occurrences",
            "_"."page_views",
            "_"."product_quantity",
            "_"."product_reviews",
            "_"."product_views",
            "_"."purchase_revenue",
            "_"."purchases",
            "_"."visitors",
            "_"."visits"
        from "public"."cc_data_view" "_"
        where (("_"."product_name" in ('Saltwater Monofilament Line', 'Pop-Up Beach Tent', 'Instant Pop-Up Tent', 'Envelop Sleeping Bag', 'Waterproof Tackle Bag')) and "_"."daterange" < date '2024-01-01') and "_"."daterange" >= date '2023-01-01'
    ) "rows"
    group by "product_name"
) "_"
where not "_"."a0" is null
limit 1000001
```

>[!TAB  Desktop Tableau ]

1. Selecteer de tab **[!UICONTROL Sheet 1]** onderaan om te schakelen van **[!UICONTROL Data source]** . In de weergave **[!UICONTROL Sheet 1]** :
   1. Sleep **[!UICONTROL Daterange]** -item uit de lijst **[!UICONTROL Tables]** in de **[!UICONTROL Filters]** -lijst.
   1. Selecteer **[!UICONTROL Filter Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer in het dialoogvenster **[!UICONTROL Filter \[Daterange\]]** de optie **[!UICONTROL Relative dates]** , selecteer **[!UICONTROL Years]** en selecteer **[!UICONTROL Previous years]** . Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Sleep **[!UICONTROL Product Name]** van de **[!UICONTROL Tables]** lijst aan **[!UICONTROL Rows]**.
   1. Sleep **[!UICONTROL Occurrences]** -item uit de **[!UICONTROL Tables]** -lijst en zet de vermelding in het veld naast **[!UICONTROL Columns]** neer. De waarde verandert in **[!UICONTROL SUM(Occurrences)]** .
   1. Selecteer **[!UICONTROL Text Table]** in **[!UICONTROL Show Me]** .
   1. Selecteer **[!UICONTROL Fit Width]** in de vervolgkeuzelijst **[!UICONTROL Fit]** .
   1. Selecteer **[!UICONTROL Product Name]** in **[!UICONTROL Rows]** . Selecteer **[!UICONTROL Filter]** in de vervolgkeuzelijst.
      1. Selecteer de tab **[!UICONTROL Filter \[Product Name\]]** in het dialoogvenster **[!UICONTROL Top]** .
      1. Selecteer **[!UICONTROL By field:]** **[!UICONTROL Top]** `5` **[!UICONTROL by Occurrences]** **[!UICONTROL Sum]** .
      1. Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .

         ![&#x200B; AlertRed &#x200B;](/help/assets/icons/AlertRed.svg) u merkt dat de lijst verdwijnt. Het selecteren van top 5 productnamen door voorkomen werkt **niet** behoorlijk gebruikend deze filter.
      1. Selecteer **[!UICONTROL Product Name]** in de **[!UICONTROL Filter]** plank en van het drop-down menu uitgezocht **[!UICONTROL Remove]**. De tabel wordt opnieuw weergegeven.
   1. Selecteer **[!UICONTROL SUM(Occurrences)]** in de **[!UICONTROL Marks]** -plank. Selecteer **[!UICONTROL Filter]** in de vervolgkeuzelijst.
      1. Selecteer **[!UICONTROL Filter \[Occurrences\]]** in het dialoogvenster **[!UICONTROL At least]** .
      1. Voer `47.799` in als waarde. Deze waarde zorgt ervoor dat alleen de bovenste 5 items in de tabel worden weergegeven. Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .

         Uw Tableau Desktop moet er hieronder uitzien.

         ![&#x200B; Limieten van de Desktop van Tableau &#x200B;](../assets/uc12-tableau-final.png)

Zoals hierboven getoond, ontbreekt deze vraag die door Desktop van Tableau wordt uitgevoerd, wanneer het bepalen van Hoogste 5 voorvalenfilter op productnamen, ontbreekt.

```sql
SELECT CAST("cc_data_view"."product_name" AS TEXT) AS "product_name",
  SUM("cc_data_view"."occurrences") AS "sum:occurrences:ok"
FROM "public"."cc_data_view" "cc_data_view"
  INNER JOIN (
  SELECT CAST("cc_data_view"."product_name" AS TEXT) AS "product_name",
    SUM("cc_data_view"."occurrences") AS "$__alias__0"
  FROM "public"."cc_data_view" "cc_data_view"
  GROUP BY 1
  ORDER BY 2 DESC,
    1 ASC
  LIMIT 5
) "t0" ON (CAST("cc_data_view"."product_name" AS TEXT) = "t0"."product_name")
WHERE (("cc_data_view"."daterange" >= (TIMESTAMP '2023-01-01 00:00:00.000')) AND ("cc_data_view"."daterange" < (TIMESTAMP '2024-01-01 00:00:00.000')))
GROUP BY 1
```

De vraag die door Desktop Tableau wordt uitgevoerd, wanneer het bepalen van Hoogste 5 filter op voorkomen, wordt hieronder getoond. De limiet is niet zichtbaar in de query en wordt toegepast op de client.

```sql
SELECT CAST("cc_data_view"."product_name" AS TEXT) AS "product_name",
  SUM("cc_data_view"."occurrences") AS "sum:occurrences:ok"
FROM "public"."cc_data_view" "cc_data_view"
WHERE (("cc_data_view"."daterange" >= (TIMESTAMP '2023-01-01 00:00:00.000')) AND ("cc_data_view"."daterange" < (TIMESTAMP '2024-01-01 00:00:00.000')))
GROUP BY 1
```

>[!TAB  Leider ]

1. Vernieuw de verbinding in de **[!UICONTROL Explore]** -interface van Looker. Selecteer ![&#x200B; Plaatsend &#x200B;](/help/assets/icons/Setting.svg) **[!UICONTROL Clear cache and refresh]**.
1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![&#x200B; Plaatsende &#x200B;](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![&#x200B; filter van de Leider &#x200B;](../assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2024/01/01]** .
1. Vanuit het gedeelte **[!UICONTROL ‣ Cc Data View]** in de linkertrack:
   1. Selecteer **[!UICONTROL Product Name]**.
   1. Selecteer **[!UICONTROL Count]** onder **[!UICONTROL MEASURES]** in de linkertrack (onder).
1. Selecteer **[!UICONTROL ↓]** (**[!UICONTROL Descending, Sort Order: 1]** ) in de kolom **[!UICONTROL Purchase Revenue]** .
1. Selecteer **[!UICONTROL ↓]** (**[!UICONTROL Descending, Sort Order: 1]** ) in de kolom **[!UICONTROL Purchase Revenue]** .
1. Selecteer **[!UICONTROL Run]**.
1. Selecteer **[!UICONTROL ‣ Visualization]**.

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![&#x200B; minder duidelijke telling &#x200B;](../assets/uc12-looker-result.png)

De vraag die door de uitbreiding wordt geproduceerd Loker die van BI gebruikt omvat `FETCH NEXT 5 ROWS ONLY`, wat impliceert dat de grens door Leider en de uitbreiding van BI wordt uitgevoerd.

```sql
-- Looker Query Context '{"user_id":6,"history_slug":"a8f3b1ebd5712413ca1ae695090f70db","instance_slug":"71d4667f0b76c0011463658f45c3f7a3"}' 
SELECT
    cc_data_view."product_name"  AS "cc_data_view.product_name",
    COUNT(*) AS "cc_data_view.count"
FROM
    "public"."cc_data_view" AS "cc_data_view"
WHERE ((( cc_data_view."daterange"  ) >= (DATE_TRUNC('day', DATE '2023-01-31')) AND ( cc_data_view."daterange"  ) < (DATE_TRUNC('day', DATE '2024-01-01'))))
GROUP BY
    1
ORDER BY
    2 DESC
FETCH NEXT 5 ROWS ONLY
```


>[!TAB  Jupyter Notitieboekje ]

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   data = %sql SELECT product_name AS `Product Name`, COUNT(*) AS Events \
               FROM cc_data_view \
               WHERE daterange BETWEEN '2023-01-01' AND '2023-02-01' \
               GROUP BY 1 \
               ORDER BY `Events` DESC \
               LIMIT 5;
   display(data)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![&#x200B; Jupyter de Resultaten van het Notitieboekje &#x200B;](../assets/uc12-jupyter-results.png)

De query wordt uitgevoerd door de BI-extensie zoals gedefinieerd in Jupyter Notebook.

>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ` ``{r} ` en ` `` ` ` in een nieuw segment in.

   ```R
   ## Dimension 1 Limited
   df <- dv %>%
      filter(daterange >= "2023-01-01" & daterange < "2024-01-01") %>%
      group_by(product_name) %>%
      count() %>%
      arrange(desc(n), .by_group = FALSE) %>%
      head(5)
   print(df)
   ```

1. Voer het segment uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![&#x200B; Resultaten RStudio &#x200B;](../assets/uc12-rstudio-results.png)

De query die wordt gegenereerd door RStudio met de BI-extensie bevat `LIMIT 5` . Dit houdt in dat de limiet wordt toegepast via RStudio en de BI-extensie.

```sql
SELECT "product_name", COUNT(*) AS "n"
FROM (
  SELECT "cc_data_view".*
  FROM "cc_data_view"
  WHERE ("daterange" >= '2023-01-01' AND "daterange" < '2024-01-01')
) AS "q01"
GROUP BY "product_name"
ORDER BY "n" DESC
LIMIT 5
```

>[!ENDTABS]

+++
