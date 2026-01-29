---
title: Transformaties
description: Transformaties gebruiken hoofdletters/kleine letters voor de BI-extensie in verschillende BI-gereedschappen in Customer Journey Analytics
solution: Customer Journey Analytics
feature: Data Views
role: User
source-git-commit: 0962f64e9bc0fed89f52191bebe6dd0e14bde61d
workflow-type: tm+mt
source-wordcount: '1473'
ht-degree: 0%

---

# Transformaties


U wilt de transformaties van de voorwerpen van Customer Journey Analytics zoals afmetingen, metriek, filters, berekende metriek, en datumwaaiers door de diverse hulpmiddelen van BI begrijpen.

+++ Customer Journey Analytics

In Customer Journey Analytics, bepaalt u in a [ gegevensmening ](/help/data-views/data-views.md), die en hoe de componenten van uw datasets als [ dimensies ](/help/components/dimensions/overview.md) en [ metriek ](/help/components/apply-create-metrics.md) worden blootgesteld. Die definitie van dimensie en metriek wordt blootgesteld aan de hulpmiddelen van BI gebruikend de uitbreiding van BI.
U gebruikt componenten zoals [ Filters ](/help/components/segments/seg-overview.md), [ Berekende metriek ](/help/components/calc-metrics/calc-metr-overview.md), en [ de waaiers van de Datum ](/help/components/date-ranges/overview.md) als deel van uw projecten van Workspace. Deze componenten worden ook blootgesteld aan de hulpmiddelen van BI gebruikend de uitbreiding van BI.

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [ een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening ](connect-and-validate.md) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

De Customer Journey Analytics-objecten zijn beschikbaar in het deelvenster **[!UICONTROL Data]** en worden opgehaald uit de tabel die u hebt geselecteerd in Power BI Desktop. Bijvoorbeeld **[!UICONTROL public.cc_data_view]** . De naam van de tabel is gelijk aan de externe id die u voor de gegevensweergave in Customer Journey Analytics hebt gedefinieerd. Gegevens worden bijvoorbeeld weergegeven met **[!UICONTROL Title]** `C&C - Data View` en **[!UICONTROL External ID]** `cc_data_view` .

**Afmetingen**
Dimensies van Customer Journey Analytics worden geïdentificeerd door de [!UICONTROL Component ID] . [!UICONTROL Component ID] wordt gedefinieerd in uw Customer Journey Analytics-gegevensweergave. Dimensies **[!UICONTROL Product Name]** in Customer Journey Analytics hebben bijvoorbeeld een [!UICONTROL Component ID] **[!UICONTROL product_name]** . Dit is de naam voor de dimensie in Power BI Desktop.
De datumbereikafmetingen van Customer Journey Analytics, zoals **[!UICONTROL Day]** , **[!UICONTROL Week]** , **[!UICONTROL Month]** en meer, zijn beschikbaar als **[!UICONTROL daterangeday]** , **[!UICONTROL daterangeweek]** , **[!UICONTROL daterangemonth]** en meer.

**Metriek**
Metrische gegevens uit Customer Journey Analytics worden geïdentificeerd door de [!UICONTROL Component ID] . [!UICONTROL Component ID] wordt gedefinieerd in uw Customer Journey Analytics-gegevensweergave. Metrisch **[!UICONTROL Purchase Revenue]** in Customer Journey Analytics heeft bijvoorbeeld een [!UICONTROL Component ID] **[!UICONTROL purchase_revenue]** . Dit is de naam voor de metrische waarde in Power BI Desktop. Een **[!UICONTROL ∑]** geeft metriek aan. Wanneer u metrisch in om het even welke visualisatie gebruikt, wordt metrisch anders genoemd aan **[!UICONTROL Sum of *metrisch *]**.

**Filters**
Filters die u in Customer Journey Analytics definieert, zijn beschikbaar in het veld **[!UICONTROL filterName]** . Wanneer u een **[!UICONTROL filterName]** -veld gebruikt in Power BI Desktop, kunt u opgeven welk filter u wilt gebruiken.

**Berekende metriek**
De berekende metriek die u in Customer Journey Analytics bepaalt worden geïdentificeerd door [!UICONTROL External ID] u voor berekende metrisch hebt bepaald. Berekende metrische waarde **[!UICONTROL Product Name (Count Distinct)]** heeft bijvoorbeeld [!UICONTROL External ID] **[!UICONTROL product_name_count_distinct]** en wordt weergegeven als **[!UICONTROL cm_product_name_count_distinc]**t in Power BI Desktop.

**waaiers van de Datum**
Datumbereiken die u in Customer Journey Analytics definieert, zijn beschikbaar in het veld **[!UICONTROL daterangeName]** . Wanneer u een veld **[!UICONTROL daterangeName]** gebruikt, kunt u opgeven welk datumbereik u wilt gebruiken.

**de transformaties van de Douane**
De Desktop van Power BI verstrekt de functionaliteit van de douanetransformatie gebruikend [ Uitdrukkingen van de Analyse van Gegevens (DAX) ](https://learn.microsoft.com/en-us/dax/dax-overview). Als voorbeeld, wilt u de [ Enige afmeting gerangschikte ](#single-dimension-ranked) gebruiksgeval met productnamen in kleine letters uitvoeren.

1. Selecteer in de rapportweergave de streepjesvisualisatie.
1. Selecteer **[!UICONTROL product_name]** in het venster Gegevens.
1. Selecteer **[!UICONTROL New column]** op de werkbalk.
1. Definieer in de formule-editor een nieuwe kolom met de naam `product_name_lower` , net als `product_name_lower = LOWER('public.cc_data_view[product_name])` .
   ![ de Transformatie van de Desktop van Power BI aan Laag ](../assets/uc14-powerbi-transformation.png)
1. Selecteer de nieuwe kolom **[!UICONTROL product_name_lower]** in het deelvenster **[!UICONTROL Data]** in plaats van de kolom **[!UICONTROL product_name]** .
1. Selecteer **[!UICONTROL Report as Table]** van ![ Meer ](/help/assets/icons/More.svg) in de lijstvisualisatie.

   Je Power BI Desktop moet er hieronder uitzien.
   ![ Definitieve Transformatie van de Desktop van Power BI ](../assets/uc14-powerbi-final.png)

De aangepaste transformatie resulteert in een update van SQL-query&#39;s. Zie het gebruik van de functie `lower` in het volgende SQL-voorbeeld:

```sql
select "_"."product_name_lower",
    "_"."a0",
    "_"."a1"
from 
(
    select "rows"."product_name_lower" as "product_name_lower",
        sum("rows"."purchases") as "a0",
        sum("rows"."purchase_revenue") as "a1"
    from 
    (
        select "_"."daterange" as "daterange",
            "_"."product_name" as "product_name",
            "_"."purchase_revenue" as "purchase_revenue",
            "_"."purchases" as "purchases",
            lower("_"."product_name") as "product_name_lower"
        from 
        (
            select "_"."daterange",
                "_"."product_name",
                "_"."purchase_revenue",
                "_"."purchases"
            from 
            (
                select "daterange",
                    "product_name",
                    "purchase_revenue",
                    "purchases"
                from "public"."cc_data_view" "$Table"
            ) "_"
            where ("_"."daterange" < date '2024-01-01' and "_"."daterange" >= date '2023-01-01') and ("_"."product_name" in ('4G Cellular Trail Camera', '4K Wildlife Trail Camera', 'Wireless Trail Camera', '8-Person Cabin Tent', '20MP No-Glow Trail Camera', 'HD Wildlife Camera', '4-Season Mountaineering Tent', 'Trail Camera', '16MP Trail Camera with Solar Panel', '10-Person Family Tent'))
        ) "_"
    ) "rows"
    group by "product_name_lower"
) "_"
where not "_"."a0" is null or not "_"."a1" is null
limit 1000001
```

>[!TAB  Desktop Tableau ]

De Customer Journey Analytics-objecten zijn beschikbaar in de zijbalk van **[!UICONTROL Data]** wanneer u in een vel werkt. En worden opgehaald uit de tabel die u hebt geselecteerd als onderdeel van de pagina **[!UICONTROL Data source]** in Tableau. Bijvoorbeeld **[!UICONTROL cc_data_view]** . De naam van de tabel is gelijk aan de externe id die u voor de gegevensweergave in Customer Journey Analytics hebt gedefinieerd. Gegevens worden bijvoorbeeld weergegeven met **[!UICONTROL Title]** `C&C - Data View` en **[!UICONTROL External ID]** `cc_data_view` .

**Afmetingen**
Dimensies van Customer Journey Analytics worden geïdentificeerd door de [!UICONTROL Component name] . [!UICONTROL Component name] wordt gedefinieerd in uw Customer Journey Analytics-gegevensweergave. Dimensies **[!UICONTROL Product Name]** in Customer Journey Analytics hebben bijvoorbeeld een [!UICONTROL Component name] **[!UICONTROL Product Name]** . Dit is de naam voor de dimensie in Tableau. Alle afmetingen worden aangegeven met **[!UICONTROL Abc]** .
De datumbereikafmetingen van Customer Journey Analytics, zoals **[!UICONTROL Day]** , **[!UICONTROL Week]** , **[!UICONTROL Month]** en meer, zijn beschikbaar als **[!UICONTROL Daterangeday]** , **[!UICONTROL Daterangeweek]** , **[!UICONTROL Daterangemonth]** en meer. Wanneer u een dimensie van het datumbereik gebruikt, moet u een aangewezen definitie van datum of tijd selecteren om op die dimensie van het datumbereik van het drop-down menu toe te passen. Bijvoorbeeld **[!UICONTROL Year]**, **[!UICONTROL Quarter]**, **[!UICONTROL Month]**, **[!UICONTROL Day]** .

**Metriek**
Metrische gegevens uit Customer Journey Analytics worden geïdentificeerd door de [!UICONTROL Component Name] . [!UICONTROL Component Name] wordt gedefinieerd in uw Customer Journey Analytics-gegevensweergave. Metrisch **[!UICONTROL Purchase Revenue]** in Customer Journey Analytics heeft bijvoorbeeld een [!UICONTROL Component Name] **[!UICONTROL Purchase Revenue]** . Dit is de naam voor de metrische waarde in Tableau. Alle metriek worden geïdentificeerd door **[!UICONTROL #]**. Wanneer u metrisch in om het even welke visualisatie gebruikt, wordt metrisch anders genoemd aan **[!UICONTROL Sum(*metrisch *)]**.

**Filters**
Filters die u in Customer Journey Analytics definieert, zijn beschikbaar in het veld **[!UICONTROL Filter Name]** . Wanneer u een veld **[!UICONTROL Filter Name]** in Tableau gebruikt, kunt u opgeven welk filter u wilt gebruiken.

**Berekende metriek**
De berekende metriek die u in Customer Journey Analytics bepaalt worden geïdentificeerd door [!UICONTROL Title] u voor berekende metrisch hebt bepaald. Berekende metrische waarde **[!UICONTROL Product Name (Count Distinct)]** heeft bijvoorbeeld [!UICONTROL Title] **[!UICONTROL Product Name (Count Distinct)]** en wordt weergegeven als **[!UICONTROL Cm Product Name Count Distinct]** in Tableau.

**waaiers van de Datum**
Datumbereiken die u in Customer Journey Analytics definieert, zijn beschikbaar in het veld **[!UICONTROL Daterange Name]** . Wanneer u een veld **[!UICONTROL Daterange Name]** gebruikt, kunt u opgeven welk datumbereik u wilt gebruiken.

**de transformaties van de Douane**
De Desktop van tableau verstrekt de functionaliteit van de douanetransformatie gebruikend [ Berekende Gebieden ](https://help.tableau.com/current/pro/desktop/en-us/calculations_calculatedfields_create.htm). Als voorbeeld, wilt u de [ Enige afmeting gerangschikte ](#single-dimension-ranked) gebruiksgeval met productnamen in kleine letters uitvoeren.

1. Selecteer **[!UICONTROL Analysis]** > **[!UICONTROL Create Calculated Field]** in het hoofdmenu.
   1. Definieer **[!UICONTROL Lowercase Product Name]** met de functie `LOWER([Product Name])` .
      ![ Berekend Gebied van Tableau ](../assets/uc14-tableau-calculated-field.png)
   1. Selecteer **[!UICONTROL OK]**.
1. Selecteer het **[!UICONTROL Data]** blad.
   1. Sleep **[!UICONTROL Lowercase Product Name]** van **[!UICONTROL Tables]** en laat vallen de ingang in het gebied naast **[!UICONTROL Rows]**.
   1. Verwijder **[!UICONTROL Product Name]** uit **[!UICONTROL Rows]** .
1. Selecteer **[!UICONTROL Dashboard 1]** weergave.

Uw Tableau Desktop moet er hieronder uitzien.

![ Desktop Tableau na transformatie ](../assets/uc14-tableau-final.png)

De aangepaste transformatie resulteert in updates van SQL-query&#39;s. Zie het gebruik van de functie `LOWER` in het volgende SQL-voorbeeld:

```sql
SELECT LOWER(CAST(CAST("cc_data_view"."product_name" AS TEXT) AS TEXT)) AS "Calculation_1562467608097775616",
  SUM("cc_data_view"."purchase_revenue") AS "sum:purchase_revenue:ok",
  SUM("cc_data_view"."purchases") AS "sum:purchases:ok"
FROM "public"."cc_data_view" "cc_data_view"
WHERE (("cc_data_view"."daterange" >= (DATE '2023-01-01')) AND ("cc_data_view"."daterange" <= (DATE '2023-12-31')))
GROUP BY 1
HAVING ((SUM("cc_data_view"."purchase_revenue") >= 999999.99999998999) AND (SUM("cc_data_view"."purchase_revenue") <= 2000000.00000002))
```

>[!TAB  Leider ]

De Customer Journey Analytics-objecten zijn beschikbaar in de **[!UICONTROL Explore]** -interface. En worden teruggewonnen als deel van vestiging uw verbinding, project, en model in Drager. Bijvoorbeeld **[!UICONTROL cc_data_view]** . De naam van de weergave is gelijk aan de externe id die u voor de gegevensweergave in Customer Journey Analytics hebt gedefinieerd. Gegevens worden bijvoorbeeld weergegeven met **[!UICONTROL Title]** `C&C - Data View` en **[!UICONTROL External ID]** `cc_data_view` .

**Afmetingen**
Dimensies van Customer Journey Analytics worden weergegeven als **[!UICONTROL DIMENSION]** in de **[!UICONTROL Cc Data View]** linkerrails. De dimensie wordt gedefinieerd in uw Customer Journey Analytics-gegevensweergave. Dimensies **[!UICONTROL Product Name]** in Customer Journey Analytics hebben bijvoorbeeld een **[!UICONTROL DIMENSION]** **[!UICONTROL Product Name]** . Dit is de naam voor de dimensie in Looker.
De datumbereikafmetingen van Customer Journey Analytics, zoals **[!UICONTROL Day]** , **[!UICONTROL Week]** , **[!UICONTROL Month]** en meer, zijn beschikbaar als **[!UICONTROL Daterangeday Date]** , **[!UICONTROL Daterangeweek Date]** , **[!UICONTROL Daterangemonth Date]** en meer.  Wanneer u een dimensie van het datumbereik gebruikt, moet u een aangewezen definitie van datum of tijd selecteren. Bijvoorbeeld **[!UICONTROL Year]**, **[!UICONTROL Quarter]**, **[!UICONTROL Month]**, **[!UICONTROL Date]** .

**Metriek**
Metrische gegevens uit Customer Journey Analytics worden weergegeven als **[!UICONTROL DIMENSION]** in de **[!UICONTROL Cc Data View]** left rail. Metrisch **[!UICONTROL Purchase Revenue]** in Customer Journey Analytics heeft bijvoorbeeld een **[!UICONTROL DIMENSION]** **[!UICONTROL Purchase Revenue]** . Als u daadwerkelijk als metrisch wilt gebruiken, maakt u een aangepast metingsveld, zoals in de bovenstaande voorbeelden wordt getoond, of gebruikt u de sneltoets voor een dimensie. Selecteer bijvoorbeeld **[!UICONTROL ⋮]** , **[!UICONTROL Aggregate]** en selecteer vervolgens **[!UICONTROL Sum]** .

**Filters**
Filters die u in Customer Journey Analytics definieert, zijn beschikbaar in het veld **[!UICONTROL Filter Name]** . Wanneer u een veld **[!UICONTROL Filter Name]** in Drager gebruikt, kunt u opgeven welk filter u wilt gebruiken.

**Berekende metriek**
De berekende metriek die u in Customer Journey Analytics bepaalt worden geïdentificeerd door [!UICONTROL Title] u voor berekende metrisch hebt bepaald. Berekende metrische waarde **[!UICONTROL Product Name (Count Distinct)]** heeft bijvoorbeeld [!UICONTROL Title] **[!UICONTROL Product Name (Count Distinct)]** en wordt weergegeven als **[!UICONTROL Cm Product Name Count Distinct]** in Looker.

**waaiers van de Datum**
Datumbereiken die u in Customer Journey Analytics definieert, zijn beschikbaar in het veld **[!UICONTROL Daterange Name]** . Wanneer u een veld **[!UICONTROL Daterange Name]** gebruikt, kunt u opgeven welk datumbereik u wilt gebruiken.

**de transformaties van de Douane**
Looker biedt aangepaste transformatiefuncties met behulp van aangepaste veldbuilders, zoals hierboven wordt weergegeven. Als voorbeeld, wilt u de [ Enige afmeting gerangschikte ](#single-dimension-ranked) gebruiksgeval met productnamen in kleine letters uitvoeren.

1. Vanuit het gedeelte **[!UICONTROL ‣ Custom Fields]** in de linkertrack:
   1. Selecteer **[!UICONTROL Custom Dimension]** in de vervolgkeuzelijst **[!UICONTROL + Add]** .
   1. Voer `lower(${cc_data_view.product_name})` in het tekstgebied **[!UICONTROL Expression]** in. Wanneer u `Product Name` begint te typen, krijgt u de juiste syntaxis.
      ![ de transformatievoorbeeld van de Leider ](../assets/uc14-looker-transformation.png)
   1. Voer `product name` in als de **[!UICONTROL Name]** .
   1. Selecteer **[!UICONTROL Save]**.

U dient een vergelijkbare tabel te zien zoals hieronder weergegeven.

![ Lager transformatieresultaat ](../assets/uc14-looker-result.png)


De aangepaste transformatie resulteert in updates van SQL-query&#39;s. Zie het gebruik van de functie `LOWER` in het volgende SQL-voorbeeld:

```sql
SELECT
    LOWER((cc_data_view."product_name")) AS "product_name",
    COALESCE(SUM(CAST(( cc_data_view."purchase_revenue"  ) AS DOUBLE PRECISION)), 0) AS "sum_of_purchase_revenue",
    COALESCE(SUM(CAST(( cc_data_view."purchases"  ) AS DOUBLE PRECISION)), 0) AS "sum_of_purchases"
FROM public.cc_data_view  AS cc_data_view
WHERE ((( cc_data_view."daterange"  ) >= (DATE_TRUNC('day', DATE '2023-01-01')) AND ( cc_data_view."daterange"  ) < (DATE_TRUNC('day', DATE '2024-01-01'))))
GROUP BY
    1
ORDER BY
    2 DESC
FETCH NEXT 500 ROWS ONLY
```

>[!TAB  Jupyter Notitieboekje ]

De Customer Journey Analytics-objecten (afmetingen, metriek, filters, berekende metriek en datumbereiken) zijn beschikbaar als onderdeel van de ingesloten SQL-query&#39;s die u maakt. Zie eerdere voorbeelden.

**de transformaties van de Douane**

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   data = %sql SELECT LOWER(product_category) AS `Product Category`, COUNT(*) AS EVENTS \
               FROM cc_data_view \
               WHERE daterange BETWEEN '2023-01-01' AND '2024-01-01' \
               GROUP BY 1 \
               ORDER BY `Events` DESC \
               LIMIT 5;
   display(data)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Jupyter de Resultaten van het Notitieboekje ](../assets/uc13-jupyter-results.png)

De query wordt uitgevoerd door de BI-extensie zoals gedefinieerd in Jupyter Notebook.

>[!TAB  RStudio ]

De Customer Journey Analytics-componenten (afmetingen, metriek, filters, berekende metriek en datumbereiken) zijn beschikbaar als vergelijkbare benoemde objecten in de R-taal. Raadpleeg de componenten die de component gebruiken Zie eerdere voorbeelden.

**de transformaties van de Douane**

1. Voer de volgende instructies tussen ` ```{r} ` en ` ``` ` in een nieuw segment in.

   ```R
   df <- dv %>%
      filter(daterange >= "2023-01-01" & daterange <= "2024-01-01") %>%
      mutate(d2=lower(product_category)) %>%
      group_by(d2) %>%
      count() %>%
      arrange(d2, .by_group = FALSE)
   print(df)
   ```

1. Voer het segment uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Resultaten RStudio ](../assets/uc13-rstudio-results.png)

De query die wordt gegenereerd door RStudio met de BI-extensie bevat `lower` . Dit houdt in dat de aangepaste transformatie wordt uitgevoerd door RStudio en de BI-extensie.

```sql
SELECT "d2", COUNT(*) AS "n"
FROM (
  SELECT "cc_data_view".*, lower("product_category") AS "d2"
  FROM "cc_data_view"
  WHERE ("daterange" >= '2023-01-01' AND "daterange" <= '2024-01-01')
) AS "q01"
GROUP BY "d2"
ORDER BY "d2"
LIMIT 1000
```

>[!ENDTABS]

+++

