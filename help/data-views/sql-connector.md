---
title: SQL Connector
description: Leer hoe u de Dienst van de Vraag, Power BI en/of Tableau kunt gebruiken om tot de Kijken van Gegevens toegang te hebben gebruikend de SQL Schakelaar.
solution: Customer Journey Analytics
feature: Data Views
hide: true
hidefromtoc: true
badgeCJASQLConnector: label="New Feature" type="Positive"
source-git-commit: 3f1112ebd2a4dfc881ae6cb7bd858901d2f38d69
workflow-type: tm+mt
source-wordcount: '2867'
ht-degree: 0%

---

# SQL Connector

{{release-limited-testing}}

De [!DNL Customer Journey Analytics (CJA) SQL Connector] biedt SQL toegang tot de [gegevensweergaven](./data-views.md) die u in CJA hebt gedefinieerd. Uw gegevensingenieurs en analisten zouden met Power BI, Tableau, of andere bedrijfsintelligentie en visualisatiehulpmiddelen (verder die als hulpmiddelen van BI worden bedoeld) vertrouwd kunnen zijn. Ze kunnen nu rapporten en dashboards maken op basis van dezelfde gegevensweergaven die CJA-gebruikers gebruiken bij het maken van hun Analysis Workspace-projecten.

Adobe Experience Platform [Query-service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=en) is de SQL interface aan gegevens beschikbaar in het gegevens meer van Experience Platform. Met de [!DNL CJA SQL Connector] enabled, de functionaliteit van [!DNL Query Service] is uitgebreid om uw CJA- gegevensmeningen als lijsten of meningen in te zien [!DNL Query Service] sessie. Dientengevolge, bedrijfsintelligentiegereedschappen die gebruiken [!DNL Query Service] als hun interface PostgresSQL naadloos van deze uitgebreide functionaliteit profiteert.

De belangrijkste voordelen zijn:

- Het is niet nodig om een gelijkwaardige vertegenwoordiging van CJA- gegevensmeningen binnen het hulpmiddel van BI zelf opnieuw te maken. <br/>Zie [Gegevens, weergave](data-views.md) voor meer informatie over de functionaliteit van de meningen van Gegevens om te begrijpen wat moet worden ontspannen.<br/>

- Meer consistentie in rapportage en analyse tussen BI-instrumenten en CJA.

- Combineer CJA-gegevens met andere gegevensbronnen die al beschikbaar zijn in BI-gereedschappen.

## Vereisten

Als u deze functionaliteit wilt gebruiken, moet u

- De optie [!UICONTROL CJA SQL Connector] in uw organisatie van het Experience Platform.

- Configureer de functionaliteit voor de relevante productprofielen, gebruikersgroepen en/of individuele gebruikers.<br/>
Gebruikers moeten toegang hebben tot:
   - Query-service Experience Platform,
   - CJA Workspace projecten, en
   - CJA-gegevensweergaven die ze willen gebruiken.

- Gebruik het verlopen op niet-vervallende geloofsbrieven om de hulpmiddelen van BI met de Schakelaar van CJA te verbinden SQL. Thr [Referentiegids](https://experienceleague.adobe.com/docs/experience-platform/query/ui/credentials.html?lang=en) verstrekt meer informatie bij het plaatsen van het verlopen van geloofsbrieven of niet-vervallende geloofsbrieven.

Zie [Toegangsbeheer](../admin/cja-access-control.md) in de sectie CJA Administration voor aanvullende informatie.


## Gebruik

Als u de opdracht [!DNL CJA SQL Connector] kunt u SQL rechtstreeks gebruiken of de slepen en neerzetten-ervaring gebruiken die beschikbaar is in het specifieke BI-gereedschap.

### SQL

U kunt de functionaliteit direct in SQL verklaringen gebruiken gebruikend of de Redacteur van de Vraag of een standaard bevel-lijn van PostgresSQL (CLI) cliënt.

+++ Query-editor

In de interface van het Experience Platform:

1. Selecteren **[!UICONTROL ** Zoekopdrachten **]** van **[!UICONTROL ** GEGEVENSBEHEER **]** in het linkerspoor.

2. Selecteren ![Query maken](assets/Smock_AddCircle_18_N.svg) **[!UICONTROL ** Query maken **]**.

3. Als u de query wilt uitvoeren, typt u de SQL-instructie en selecteert u de instructie ![Afspelen](assets/Smock_Play_18_N.svg) (of druk op SHIFT + ENTER).

+++


+++ PostgresSQL CLI

1. Zoek in de gebruikersinterface van het Experience Platform uw PostgresSQL-referenties op en kopieer deze.

   1. Selecteren **[!UICONTROL ** Zoekopdrachten **]** van de linkerspoorstaaf (onder **[!UICONTROL ** GEGEVENSBEHEER **]**).

   2. Selecteren **[!UICONTROL ** Credentials **]** in de bovenste balk.

   3. Als u de verbindingstekenreeks wilt kopiëren, gebruikt u ![Kopiëren](assets/Smock_Copy_18_N.svg) in de **[!UICONTROL ** PSQL, opdracht **]** sectie.

2. Open uw PostgresSQL CLI.

3. Om binnen te registreren en te beginnen uw vragen uitvoeren, kleef het verbinden koord in CLI PostgresSQL.

+++

Zie [Handleiding voor de Query Editor](https://experienceleague.adobe.com/docs/experience-platform/query/ui/user-guide.html?lang=en) voor meer informatie .


### BI Tools

De CJA SQL-connector wordt momenteel ondersteund voor Power BI en Tableau.

+++ Power BI

1. In Adobe Experience Platform UI, kijk omhoog de details van uw geloofsbrieven PostgresSQL.

   1. Selecteren **[!UICONTROL ** Zoekopdrachten **]** van de linkerspoorstaaf (onder **[!UICONTROL ** GEGEVENSBEHEER **]**).

   2. Selecteren **[!UICONTROL ** Credentials **]** in de bovenste balk.

   3. Gebruiken ![Kopiëren](assets/Smock_Copy_18_N.svg) om elk van de parameters van de geloofsbrieven te kopiëren Postgres ([!UICONTROL Host], [!UICONTROL Port], [!UICONTROL Database], [!UICONTROL Username], en andere) indien nodig in Power BI.

2. In Power BI:

   1. Selecteer in het hoofdvenster de optie **[!UICONTROL ** Gegevens ophalen **]** in de bovenste werkbalk.

   2. Selecteren **[!UICONTROL ** Meer...**]** in het linkerspoor.

   3. In de **Gegevens ophalen** scherm, zoeken naar `PostgresSQL` en selecteert u de **[!UICONTROL ** PostgresSQL-database **]** in de lijst.

   4. In de **[!UICONTROL ** PostgressSQL-database **]** dialoogvenster:

      1. Plakken **[!UICONTROL ** Host **]** parameter van de Vragen van het Experience Platform [!UICONTROL Credentials] in **[!UICONTROL ** Server **]** tekstveld.

      2. Plakken **[!UICONTROL ** Database **]** parameter van de Vragen van het Experience Platform [!UICONTROL Credentials] in **[!UICONTROL ** Database **]** tekstveld.

         Toevoegen `?FLATTEN` aan de **[!UICONTROL ** Database **]** parameter, zodat het als leest `prod:all?FLATTEN` bijvoorbeeld. Zie [Geneste gegevensstructuren samenvoegen voor gebruik met BI-gereedschappen van derden](https://experienceleague.adobe.com/docs/experience-platform/query/essential-concepts/flatten-nested-data.html?lang=en) voor meer informatie .

      3. Wanneer wordt gevraagd om **[!UICONTROL ** Gegevensconnectiviteit **]** modus, selecteren **[!UICONTROL ** DirectQuery **]** om ervoor te zorgen dat de gegevensstructuren op de juiste wijze worden afgevlakt.

      4. U wordt gevraagd **[!UICONTROL ** Gebruikersnaam **]** en **[!UICONTROL ** Wachtwoord **]**. De equivalente parameters van Experience Platforms gebruiken [!UICONTROL Credentials].
   5. Na succesvolle login, verschijnen de lijsten van de Mening van Gegevens CJA in Power BI **[!UICONTROL ** Navigator **]**. Tabellen met gegevensweergave worden geïdentificeerd aan de hand van `dv_` in hun naam.


   6. Selecteer de tabellen in de gegevensweergave die u wilt gebruiken en selecteer **[!UICONTROL ** Laden **]**.

   Alle dimensies en metriek die aan een of meer geselecteerde tabellen zijn gekoppeld, worden in het rechterdeelvenster weergegeven en kunnen in uw visualisaties worden gebruikt.

   Zie [Verbinding maken met Power BI-zoekservice](https://experienceleague.adobe.com/docs/experience-platform/query/clients/power-bi.html?lang=en) voor meer informatie .

+++

+++Tableau

1. In het Experience Platform UI, kijk omhoog de details van uw geloofsbrieven PostgresSQL.

   1. Selecteren **[!UICONTROL ** Zoekopdrachten **]** van de linkerspoorstaaf (onder **[!UICONTROL ** GEGEVENSBEHEER **]**).

   2. Selecteren **[!UICONTROL ** Credentials **]** in de bovenste balk.

   3. Gebruiken ![Kopiëren](assets/Smock_Copy_18_N.svg) om elk van de parameters van de geloofsbrieven te kopiëren Postgres ([!UICONTROL Host], [!UICONTROL Port], [!UICONTROL Database], [!UICONTROL Username], en andere) indien nodig in Tableau.

2. In Tableau:

   1. Selecteren **[!UICONTROL ** Meer **]** van **[!UICONTROL ** Naar een server **]** in het linkerspoor.

   2. Selecteren **[!UICONTROL ** PostgresSQL **]** in de lijst.

   3. In de [!UICONTROL PostgresSQL] dialoogvenster:

      1. Plakken **[!UICONTROL ** Host **]** parameter van de Vragen van het Experience Platform [!UICONTROL Credentials] in **[!UICONTROL ** Server **]** tekstveld.

      2. Plakken **[!UICONTROL ** Poort **]** parameter van de Vragen van het Experience Platform [!UICONTROL Credentials] in **[!UICONTROL ** Poort **]** tekstveld.

      3. Plakken **[!UICONTROL ** Database **]** parameter van de Vragen van het Experience Platform [!UICONTROL Credentials] in **[!UICONTROL ** Database **]** tekstveld.

         Toevoegen `%3FFLATTEN` aan de **[!UICONTROL ** Database **]** parameter, zodat het als leest `prod:all%3FFLATTEN` bijvoorbeeld. Zie [Geneste gegevensstructuren samenvoegen voor gebruik met BI-gereedschappen van derden](https://experienceleague.adobe.com/docs/experience-platform/query/essential-concepts/flatten-nested-data.html?lang=en) voor meer informatie .

      4. Selecteren **[!UICONTROL ** Gebruikersnaam en wachtwoord **]** van **[!UICONTROL ** Verificatie **]** lijst.

      5. Plakken **[!UICONTROL ** Gebruikersnaam **]** parameter van de Vragen van het Experience Platform [!UICONTROL Credentials] in **[!UICONTROL ** Gebruikersnaam **]** tekstveld.

      6. Plakken **[!UICONTROL ** Wachtwoord **]** parameter van de Vragen van het Experience Platform [!UICONTROL Credentials] in **[!UICONTROL ** Wachtwoord **]** tekstveld.

      7. Selecteren **[!UICONTROL ** Aanmelden **]**.
   4. CJA-gegevensweergaven worden weergegeven als tabellen in het dialoogvenster **[!UICONTROL ** Tabel **]** lijst. Tabellen in de gegevensweergave beginnen met `dv_`.

   5. Sleep de tabellen die u op het canvas wilt gebruiken.

   U kunt nu met de gegevens van de lijsten van de gegevensmening werken om uw rapporten en visualisaties te bouwen.

   Zie [Connect Tableau naar Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/clients/tableau.html?lang=en) voor meer informatie .

+++

Zie [Client verbinden met Query-service](https://experienceleague.adobe.com/docs/experience-platform/query/clients/overview.html?lang=en) voor een overzicht van en meer informatie over de verschillende beschikbare instrumenten.

## Functionaliteit

Standaard hebben uw gegevensweergaven een tabelveilige naam die is gegenereerd op basis van hun vriendelijke naam. De gegevensweergave met de naam [!UICONTROL My Web Data] heeft de weergavenaam `dv_my_web_data`.

Als u de ID&#39;s van de gegevensweergave wilt gebruiken als tabelnamen, kunt u de optionele `CJA_USE_IDS` instellen op de databasenaam wanneer verbinding wordt gemaakt. Bijvoorbeeld: `prod:all?CJA_USE_IDS` toont uw gegevensmeningen met namen als `dv_ABC123`.

### Gegevensbeheer

De instellingen voor gegevensbeheer in Customer Journey Analytics zijn overgenomen van Adobe Experience Platform. De integratie tussen CJA en Adobe Experience Platform Data Governance maakt het mogelijk gevoelige CJA-gegevens te labelen en het privacybeleid te handhaven.

De etiketten en het beleid van de privacy die op datasets werden gecreeerd die door Experience Platform worden verbruikt kunnen in het werkschema van CJA- gegevensmeningen worden rond gekomen. Daarom tonen de gegevens die met de SQL-connector van CJA worden gevraagd de juiste waarschuwingen of fouten wanneer niet wordt voldaan aan de gedefinieerde privacylabels en het gedefinieerde beleid.

### Gegevens weergeven

In de standaardSQL CLI kunt u van uw meningen een lijst maken gebruikend `\dv`

```sql
prod:all=> \dv
                                     List of relations
 Schema |                              Name                              | Type |  Owner             
--------+----------------------------------------------------------------+------+----------
 public | dv_adobe_analytics_spa                                         | view | postgres
 public | dv_adobe_analytics_spa_cja_adobe_users_only_                   | view | postgres
 public | dv_adobe_analytics_spa_cja_customers_only_                     | view | postgres
 public | dv_adobe_analytics_spa_core_aa_only_                           | view | postgres
 public | dv_adobe_analytics_spa_trad_aa_customers_only_                 | view | postgres
 public | dv_cja_audit_logs                                              | view | postgres
 public | dv_cja_connections_ui_prod_analytics_format_                   | view | postgres
 public | dv_cja_for_adobe_spark_usage                                   | view | postgres
 public | dv_cja_new_dimesnions                                          | view | postgres
 public | dv_cja_test_dimensions                                         | view | postgres
 public | dv_cja_usage_account_based_customers_only_                     | view | postgres
 public | dv_combined_trad_aa_apps                                       | view | postgres
 public | dv_customer_journey_analytics_sc_demo_users_                   | view | postgres
```

### Geneste in plaats van samengevoegd

Standaard gebruikt het schema van uw gegevensweergaven geneste structuren, net als de oorspronkelijke XDM-schema&#39;s. De integratie ondersteunt ook de `FLATTEN` optie. Met deze optie kunt u afvlakken forceren van het schema voor de gegevensweergaven (en elke andere tabel in de sessie). Het afvlakken staat voor gemakkelijker gebruik in de hulpmiddelen van BI toe die geen gestructureerde schema&#39;s steunen. Zie [Werken met geneste gegevensstructuren in Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/essential-concepts/flatten-nested-data.html?lang=en) voor meer informatie .

### Ondersteunde SQL

Zie [SQL-naslagservice](https://experienceleague.adobe.com/docs/experience-platform/query/sql/overview.html?lang=en) voor de volledige verwijzing naar welk type SQL wordt ondersteund.

Zie de tabel Patronen hieronder voor een overzicht van patronen en voorbeelden.

+++Patronen

| Patroon | Voorbeeld |
|---|---|
| Schema-detectie | <pre>SELECTEREN * VANUIT dv1 WAAR 1=0</pre> |
| Uitsplitsing | <pre>DIm1, SUM(metrisch1) SELECTEREN ALS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP OP DIm1</pre><pre>DIm1, SUM(metrisch1) SELECTEREN ALS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot; EN<br/>  filterId = &#39;12345&#39;<br/>GROEP OP DIm1</pre><pre>DIm1, SUM(metrisch1) SELECTEREN ALS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot; EN<br/>  EN (dim2 = &#39;A&#39; OF dim3 IN (&#39;X&#39;, &#39;Y&#39;, &#39;Z&#39;)<br/>GROEP OP DIm1</pre> |
| HAVENS | <pre>DIm1, SUM(metrisch1) SELECTEREN ALS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP OP DIm1<br/>MET m1 > 100</pre> |
| Onderscheiden, boven <br/>dimensiewaarden | <pre>DIM1 VERSCHUIVEN VANUIT dv1 SELECTEREN</pre><pre>DIM1 SELECTEREN ALS dv1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP OP DIm1</pre><pre>DIM1 SELECTEREN ALS dv1<br/>VAN dv1<br/>WHERE \&quot;timestamp\&quot; >= &quot;2022-01-01&quot; AND \&quot;timestamp\&quot; &lt; &quot;2022-01-02&quot;<br/>GROEP OP DIm1<br/>ORDER BY SUM(metrisch1)<br/>LIMIET 15</pre> |
| Metrische totalen | <pre>SUM(metrisch1) SELECTEREN ALS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;</pre> |
| Meerdere dimensies<br/>uitsplitsingen<br/>en toponderscheidingen | <pre>SELECTEER dim1, dim2, SUM(metrisch1) AS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP MET DIM1, dim2</pre><pre>SELECTEER dim1, dim2, SUM(metrisch1) AS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP MET 1, 2<br/>VOLGORDE MET 1, 2</pre><pre>DIM1 VERSCHUIVEN, dim2 SELECTEREN<br/>VAN dv1</pre> |
| Subselectie:<br/>Aanvullend resultaat<br/>filteren | <pre>DIM1, m1 SELECTEREN<br/>VAN (<br/>  DIm1, SUM(metrisch1) SELECTEREN ALS m1<br/>  VAN dv1<br/>  WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;</br>  GROEP OP DIm1<br/>)<br/>WAAR grijs 1 in (&#39;A&#39;, &#39;B&#39;)</pre> |
| Subselectie:<br/>Samenvoegen met<br/>dataset niet in<br/>CJA | <pre>SELECT b.key, a.dim1, a.m1<br/>VAN (<br/>  DIm1, SUM(metrisch1) SELECTEREN ALS m1<br/>  VAN dv1<br/>  WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>  GROEP OP DIm1<br/>a)<br/>LEFT JOIN lookups b OP a.dim1 = b.key</pre> |
| Subselectie:<br/>Doorheen zoeken<br/>gegevensweergaven | <pre>SELECT-toets, SUM(m1) AS totaal<br/>VAN (<br/>  DIm1 AS-toets SELECTEREN, SUM(metrisch1) AS m1<br/>  VAN dv1<br/>  WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>  GROEP OP DIm1<br/><br/>  UNIE<br/><br/>  DIm2 AS-toets SELECTEREN, SUM(m1) AS m1<br/>  FROM dv2<br/>  WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>  GROEP MET DIm2<br/>GROEP OP toets<br/>VOLGORDE PER totaal</pre> |
| Subselectie: <br/>Gelaagde bron, <br/>filteren, <br/>en aggregatie | Gelaagd met subselecties:<br><pre>SELECT rows.dim1, SUM(rows.m1) AS total<br/>VAN (<br/>  \_.dim1,\_.m1 SELECTEREN<br/>  VAN (<br/>    \* SELECTEREN VANUIT dv1<br/>    WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>  ) \_<br/>  WHERE \_.dim1 in (&#39;A&#39;, &#39;B&#39;, &#39;C&#39;)<br/>) rijen<br/>GROEP MET 1<br/>VOLGORDE PER totaal</pre><br/>Lagen met CTE:<br/><pre>MET rijen AS (<br/>  MET \_ AS (<br/>    SELECTEREN * UIT data_ares<br/>    WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2021-01-01&quot; EN &quot;2021-02-01&quot;<br/>  )<br/>  SELECTEER _.item, _.units VAN _<br/>  WAAR _.item NIET NULL IS<br/>)<br/>SELECT rows.item, SUM(rows.units) AS-eenheden<br/>UIT rijen WHERE rows.item in (&#39;A&#39;, &#39;B&#39;, &#39;C&#39;)<br/>GROEP OP rijen.item</pre> |
| Hiermee selecteert u waar de<br/>metriek komt voor<br/> of worden gemengd met<br/>de afmetingen | <pre>SUM(metrisch1) SELECTEREN AS m1, dim1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP MET 2</pre> |

{style="table-layout:auto"}

+++

### Dimensies

U kunt alle standaard beschikbare afmetingen selecteren of in de gegevensweergave definiëren. U selecteert een dimensie op basis van de id.

### Metrics

De beschikbare meetgegevens zijn:

- alle standaard beschikbare cijfers;

- gedefinieerd in de gegevensweergave,

- berekende metriek die met de Mening van Gegevens compatibel zijn die de gebruiker toegang tot heeft.

U selecteert metrisch door zijn identiteitskaart die in a wordt verpakt `SUM(metric)` -expressie, net als bij andere SQL-bronnen.

U kunt het volgende gebruiken:

- `SELECT COUNT(*)` of `COUNT(1)` om de voorvallen metrisch te krijgen.

- `SELECT COUNT(DISTINCT dimension)` of `SELECT APPROX_COUNT_DISTINCT(dimension)` om de ongeveer verschillende waarden van een dimensie te tellen. Zie details in [Verschillen tellen](#counting-distincts).

- [Inline berekeningen](#inline-calculations) metriek op de vlucht combineren en/of wiskunde op hen doen.

#### Verschillen tellen

Vanwege de onderliggende aard van de werking van CJA is de enige dimensie waarvoor u een exacte telling kunt krijgen, de `adobe_personid` dimensie. De volgende SQL-instructies `SELECT COUNT(DISTINCT adobe_personid)` of `SELECT APPROX_COUNT_DISTINCT(adobe_personid)` Retourneer de waarde van de maatstaf voor standaardpersonen, die het aantal verschillende personen is. Voor andere dimensies, wordt een ongeveer verschillende telling teruggekeerd.

#### Voorwaardelijke metriek

U kunt een `IF` of `CASE` in de `SUM` of `COUNT` functies om extra filtreren toe te voegen die voor geselecteerde metrisch specifiek is. Het toevoegen van deze clausules is gelijkaardig aan het toepassen van een filter op een metrische kolom in een de rapportlijst van de Werkruimte.

Voorbeelden:

```sql
SUM(IF(dim1 = 'X' AND dim2 = 'A', metric1, 0)) AS m1
```

```sql
SUM(CASE WHEN dim1 = 'X' AND dim2 = 'A' THEN METRIC1 END) AS m1
```

#### Inline berekeningen

U kunt aanvullende metrische expressies toepassen in uw `SELECT` in plaats van dat de wiskunde in berekende metrisch wordt bepaald. In de volgende tabel wordt aangegeven welk type expressies wordt ondersteund.

| Operator of functie | Details |
|---|---|
| `+`, `-`, `*`, `/`, en `%` | Toevoegen, aftrekken, vermenigvuldigen, verdelen en modulair/restant |
| `-X` of `+X` | Het teken wijzigen of een metrische waarde instellen waarbij X de metrische expressie is |
| `PI()` | π, constante |
| `POSITIVE`, `NEGATIVE`, `ABS`, `FLOOR`, `CEIL`, `CEILING`, `EXP`, `LN`, `LOG10`, `LOG1P`, `SQRT`, `CBRT`, `DEGREES`, `RADIANS`, `SIN`, `COS`, `TAN`, `ACOS`, `ASIN`, `ATAN`, `COSH`, `SINH`, en `TANH` | Unaire rekenfuncties |
| `MOD`, `POW`, `POWER`, `ROUND`, `LOG` | Binaire wiskundige functies |

{style="table-layout:auto"}

### Speciale kolommen

**Tijdstempel**

De `timestamp` de speciale kolom wordt gebruikt om de datumwaaiers voor de vraag te verstrekken. Een datumbereik kan worden gedefinieerd met een `BETWEEN` expressie of een paar `timestamp` `>`, `>=`, `<`, `<=` controles `AND`rd samen.
De `timestamp` is optioneel en als geen volledig bereik wordt opgegeven, worden standaardwaarden gebruikt:

- Als er slechts een minimum is opgegeven (`timestamp > X` of ` timestamp >= X`), loopt het bereik van X tot nu.

- Als slechts een maximum wordt verstrekt (`timestamp < X` of `timestamp <= X`), ligt het bereik tussen X-30 dagen en X.

- Als er niets is opgegeven, loopt het bereik van nu tot 30 dagen.

Het tijdstempelbereik wordt geconverteerd naar een algemeen filter voor het datumbereik in RankedRequest.
Het tijdstempelveld kan ook worden gebruikt in Datum-tijdfuncties om de tijdstempel van de gebeurtenis te parseren.

**Datumbereik**

De `daterange` speciale kolommen, vergelijkbaar met  `timestamp`Het filteren is echter beperkt tot volledige dagen. De `daterange` is ook optioneel en heeft dezelfde standaardwaarden als `timestamp`.
De `daterange` U kunt het veld ook gebruiken in Datum-tijdfuncties om de gebeurtenisdatum te parseren.

**filterId**

De `filterId` speciale kolom is optioneel en wordt gebruikt om een extern gedefinieerd filter toe te passen op de query. Het toepassen van een extern gedefinieerd filter op een query lijkt op het slepen van een filter in een deelvenster in Workspace. Er kunnen meerdere filter-id&#39;s worden opgegeven door `AND`-ing hen.

### WHERE Clausule

De WHERE-component wordt in drie stappen afgehandeld:

1. Het datumbereik zoeken in het menu `timestamp` speciaal veld.

2. Zoeken naar extern gedefinieerde items `filterId`s om in het filtreren op te nemen.

3. Zet de resterende expressies om in ad-hocfilters.

De behandeling wordt uitgevoerd door het eerste niveau van `AND`s in de `WHERE` clausule. Elk hoogste niveau `AND`de expressie ed moet overeenkomen met een van de bovenstaande expressies. Iets dieper dan het eerste niveau van `AND`s, of als de `WHERE` componentgebruik `OR`Op het hoogste niveau wordt dit als een ad-hocfilter behandeld.

### VOLGORDE OP

Door gebrek, sorteert de vraag de resultaten door eerste geselecteerde metrisch in dalende orde. U kunt de standaardsorteervolgorde overschrijven door `ORDER BY ... ASC` of `ORDER BY ... DESC`. Als u `ORDER BY`moet u `ORDER BY` op de eerste geselecteerde metrische waarde.

U kunt de volgorde ook spiegelen met `-` (min) vóór de metrische waarde. Beide onderstaande instructies resulteren in dezelfde volgorde:

```sql
ORDER BY metric1 ASC
```

```sql
ORDER BY -metric1 DESC
```

### Algemene functieondersteuning

| -functie | Voorbeeld | Details |
|---|---|---|
| [CAST (kolom AS-type)](https://spark.apache.org/docs/latest/api/sql/index.html#cast) | ``CAST(`timestamp` AS STRING)`` of <br/> `` `timestamp`::string `` | Type casting wordt momenteel niet ondersteund, maar er wordt geen fout gegenereerd. De `CAST` functie wordt genegeerd. |
| [TIMESTAMP(timeString)](https://spark.apache.org/docs/latest/api/sql/index.html#timestamp) | `` WHERE `timestamp` >= TIMESTAMP('2022-01-01 00:00:00') AND   `timestamp` < TIMESTAMP('2022-01-02 00:00:00') `` | Een tijdtekenreeks parseren als een tijdstempel voor gebruik in een `WHERE` clausule. |
| [TO_TIMESTAMP(timeString, formatString)](https://spark.apache.org/docs/latest/api/sql/index.html#to_timestamp) | `` WHERE `timestamp` >= TO_TIMESTAMP('01/01/2022', 'MM/dd/yyyy') AND `timestamp` < TO_TIMESTAMP('01/02/2022', 'MM/dd/yyyy') `` | Een tijdtekenreeks parseren als een tijdstempel voor gebruik in een `WHERE` clausule, optioneel verstrekkend een formaat voor die tijdkoord. |
| [DATE(dateString)](https://spark.apache.org/docs/latest/api/sql/index.html#date) | `` WHERE `timestamp` >= DATE('2022-01-01') AND `timestamp` < DATE('2022-01-02') `` | Een datumtekenreeks parseren als een tijdstempel voor gebruik in een `WHERE` clausule. |
| [TO_DATE(dateString, formatString)](https://spark.apache.org/docs/latest/api/sql/index.html#to_date) | `` WHERE `timestamp` >= TO_DATE('01/01/2022', 'MM/dd/yyyy') AND `timestamp` < TO_DATE('01/02/2022', 'MM/dd/yyyy') `` | Een datumtekenreeks parseren als een tijdstempel voor gebruik in een `WHERE` -component, optioneel een notatie voor die datumtekenreeks opgeven. |

{style="table-layout:auto"}

### Ondersteuning voor Dimension-functies

Deze functies kunnen worden gebruikt voor dimensies in de `SELECT`, `WHERE` clausule, of in voorwaardelijke metriek.

**Reeksfuncties**

| -functie | Voorbeeld | Details |
|---|---|---|
| [LOWER(stringDimension)](https://spark.apache.org/docs/latest/api/sql/index.html#lower) | ``SELECT LOWER(name) AS lower_name`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |

{style="table-layout:auto"}

**Datum- en tijdfuncties**

| -functie | Voorbeeld | Details |
|---|---|---|
| [JAAR (datum of datum-tijd)](https://spark.apache.org/docs/latest/api/sql/index.html#year) | ``SELECT YEAR(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [MONTH(date of date-time)](https://spark.apache.org/docs/latest/api/sql/index.html#month) | ``SELECT MONTH(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [DAY(datum of datum-tijd)](https://spark.apache.org/docs/latest/api/sql/index.html#day) | ``SELECT DAY(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [DAYOFWEEK(datum of datum-tijd)](https://spark.apache.org/docs/latest/api/sql/index.html#dayofweek) | ``SELECT DAYOFWEEK(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde omdat u het nummer en niet de vriendschappelijke naam nodig hebt. |
| [DAYOFYEAR(datum of datum-tijd)](https://spark.apache.org/docs/latest/api/sql/index.html#dayofyear) | ``SELECT DAYOFYEAR(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [WEEK(datum of datum-tijd)](https://spark.apache.org/docs/latest/api/sql/index.html#week) | ``SELECT WEEK(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [QUARTER(datum of datum-tijd)](https://spark.apache.org/docs/latest/api/sql/index.html#quarter) | ``SELECT QUARTER(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [HOUR(datum of datum-tijd)](https://spark.apache.org/docs/latest/api/sql/index.html#hour) | ``SELECT HOUR(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde omdat u het nummer en niet de vriendschappelijke naam nodig hebt. |
| [MINUTE(datum of datum-tijd)](https://spark.apache.org/docs/latest/api/sql/index.html#minute) | ``SELECT MINUTE(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [EXTRACT(onderdeel VAN datum of datum/tijd)](https://spark.apache.org/docs/latest/api/sql/index.html#extract) | ``SELECT EXTRACT(MONTH FROM `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde voor sommige onderdelen van deze functie omdat u het nummer nodig hebt en niet de vriendschappelijke naam.<br/>Ondersteunde onderdelen zijn:<br>- Trefwoorden: `YEAR`, `MONTH`, `DAYOFMONTH`, `DAYOFWEEK`, `DAYOFYEAR`, `WEEK`, `QUARTER`, `HOUR`, `MINUTE`.<br/>- Tekenreeksen:  `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&quot;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'`, of `'MINUTE'`. |
| [DATE_PART(deel, datum of datum-tijd)](https://spark.apache.org/docs/latest/api/sql/index.html#date_part) | ``SELECT DATE_PART('month', `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde voor sommige onderdelen van deze functie omdat u het nummer nodig hebt en niet de vriendschappelijke naam.<br/>Ondersteunde tekenreeksonderdelen zijn: `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&quot;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'`, of `'MINUTE'`. |
| [DATE_TRUNC(granularity, date, or date-time)](https://spark.apache.org/docs/latest/api/sql/index.html#date_trunc) | ``SELECT DATE_TRUNC('quarter', `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven.<br/>Ondersteunde tekenreeksgranulariteiten zijn: `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&quot;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'`, of `'MINUTE'`. |

{style="table-layout:auto"}

