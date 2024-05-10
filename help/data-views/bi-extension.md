---
title: Customer Journey Analytics BI-extensie
description: Leer hoe u de Dienst van de Vraag, Power BI, Tableau, of andere hulpmiddelen kunt gebruiken BI en SQL om tot gegevensmeningen toegang te hebben gebruikend de uitbreiding van Customer Journey Analytics BI.
solution: Customer Journey Analytics
feature: SQL Connector
hide: true
hidefromtoc: true
role: Admin
exl-id: ab7e1f15-ead9-46b7-94b7-f81802f88ff5
source-git-commit: ad7f748fb7aa684d134cf110460a84d1b9ec3895
workflow-type: tm+mt
source-wordcount: '2721'
ht-degree: 0%

---

# Customer Journey Analytics BI-extensie

{{release-limited-testing}}

{{select-package}}

De [!DNL Customer Journey Analytics BI extension] biedt SQL toegang tot de [gegevensweergaven](./data-views.md) die u in Customer Journey Analytics hebt gedefinieerd. Uw gegevensingenieurs en analisten zouden met Power BI, Tableau, of andere bedrijfsintelligentie en visualisatiehulpmiddelen (verder die als hulpmiddelen van BI worden bedoeld) vertrouwd kunnen zijn. Ze kunnen nu rapporten en dashboards maken op basis van dezelfde gegevensweergaven die gebruikers van Customers Journey Analytics gebruiken bij het maken van hun Analysis Workspace-projecten.

Adobe Experience Platform [Query-service](https://experienceleague.adobe.com/en/docs/experience-platform/query/home) is de SQL interface aan gegevens beschikbaar in het gegevens meer van Experience Platform. Met de [!DNL Customer Journey Analytics BI extension] enabled, de functionaliteit van [!DNL Query Service] is uitgebreid om de gegevensweergaven van uw Customer Journey Analytics weer te geven als tabellen of weergaven in een [!DNL Query Service] sessie. Dientengevolge, bedrijfsintelligentiehulpmiddelen die gebruiken [!DNL Query Service] als hun interface PostgresSQL naadloos van deze uitgebreide functionaliteit profiteert.

De belangrijkste voordelen zijn:

* Het is niet nodig om een gelijkwaardige vertegenwoordiging van de gegevensmeningen van de Customer Journey Analytics binnen het hulpmiddel van BI zelf te ontspannen. <br/>Zie [Gegevensweergaven](data-views.md) voor meer informatie over de functionaliteit van gegevensmeningen om te begrijpen wat moet worden ontspannen.
* Meer consistentie in rapportage en analyse tussen BI-instrumenten en Customer Journey Analytics.
* Combineer de gegevens van de Customer Journey Analytics met andere gegevensbronnen reeds beschikbaar in de hulpmiddelen van BI.

## Vereisten

Als u deze functionaliteit wilt gebruiken, moet u:

<!---   Enable the [!UICONTROL Customer Journey Analytics BI extension] in your Experience Platform organization. -->

* De functionaliteit configureren voor de relevante productprofielen, gebruikersgroepen en/of individuele gebruikers. De toegangsvereisten omvatten:
   * Adobe Experience Platform Query Service
   * Werkruimteprojecten in Customer Journey Analytics
   * Gewenste CJA-gegevensweergaven voor gebruik
   * Toegang tot de extensie BI in de gereedschappen voor gegevensweergave

* Het verlopen van het gebruik op niet-vervallende geloofsbrieven om de hulpmiddelen van BI aan te sluiten [!DNL Customer Journey Analytics BI extension]. De [Referentiegids](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/credentials) verstrekt meer informatie bij het plaatsen van het verlopen van geloofsbrieven of niet-vervallende geloofsbrieven.

Zie [Toegangsbeheer](../technotes/access-control.md) in de sectie Beheer Customer Journey Analytics voor aanvullende informatie.


## Gebruik

Als u de opdracht [!DNL Customer Journey Analytics BI extension] kunt u SQL rechtstreeks gebruiken of de slepen en neerzetten-ervaring gebruiken die beschikbaar is in het specifieke BI-gereedschap.

### SQL

U kunt de functionaliteit direct in SQL verklaringen gebruiken gebruikend of de Redacteur van de Vraag of een standaard bevel-lijn van PostgresSQL (CLI) cliënt.

+++ Query-editor

In Adobe Experience Platform:

1. Selecteren **[!UICONTROL ** Zoekopdrachten **]** van **[!UICONTROL ** GEGEVENSBEHEER **]** in het linkerspoor.

1. Selecteren ![Query maken](assets/Smock_AddCircle_18_N.svg) **[!UICONTROL ** Query maken **]**.

1. Selecteer de `cja` **[!UICONTROL ** Database **]**.

1. Als u de query wilt uitvoeren, typt u de SQL-instructie en selecteert u de ![Afspelen](assets/Smock_Play_18_N.svg) knop (of druk op `[SHIFT]` + `[ENTER]`).

+++


+++ PostgresSQL CLI

1. Zoek en kopieer uw PostgresSQL-referenties in Adobe Experience Platform:

   1. Selecteren **[!UICONTROL ** Zoekopdrachten **]** van de linkerspoorstaaf (onder **[!UICONTROL ** GEGEVENSBEHEER **]**).

   1. Selecteren **[!UICONTROL ** Credentials **]** in de bovenste balk.

   1. Selecteer de `cja` **[!UICONTROL ** Database **]**.

   1. Om het bevelkoord te kopiëren, gebruik ![Kopiëren](assets/Smock_Copy_18_N.svg) in de **[!UICONTROL ** PSQL, opdracht **]** sectie.

1. Open een opdracht- of terminalvenster.

1. Als u zich wilt aanmelden en uw query&#39;s wilt uitvoeren, plakt u de opdrachttekenreeks in uw terminal.

+++

Zie [Handleiding voor de Query Editor](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/user-guide) voor meer informatie .


### BI-gereedschappen

Op dit moment wordt [!DNL Customer Journey Analytics BI extension] wordt alleen ondersteund en getest op Power BI en Tableau. Andere hulpmiddelen van BI die de interface PSQL gebruiken zouden ook kunnen werken, maar officieel nog niet gesteund.

+++ Power BI

1. Bekijk de details van uw PostgresSQL geloofsbrieven in Adobe Experience Platform:

   1. Selecteren **[!UICONTROL ** Zoekopdrachten **]** van de linkerspoorstaaf (onder **[!UICONTROL ** GEGEVENSBEHEER **]**).

   1. Selecteren **[!UICONTROL ** Credentials **]** in de bovenste balk.

   1. Selecteer de `cja` **[!UICONTROL ** Database **]**.

   1. Gebruiken ![Kopiëren](assets/Smock_Copy_18_N.svg) om elk van de parameters van de geloofsbrieven te kopiëren Postgres ([!UICONTROL Host], [!UICONTROL Port], [!UICONTROL Database], [!UICONTROL Username], en andere) indien nodig in de Power BI.

1. In Power BI:

   1. Selecteer in het hoofdvenster **[!UICONTROL ** Gegevens ophalen **]** in de bovenste werkbalk.

   1. Selecteren **[!UICONTROL More...]** in het linkerspoor.

   1. In de **Gegevens ophalen** scherm, zoeken naar `PostgresSQL` en selecteert u de **[!UICONTROL ** PostgresSQL-database **]** in de lijst.

   1. In de **[!UICONTROL ** PostgressSQL-database **]** dialoogvenster:

      1. Plakken **[!UICONTROL ** Host **]** parameter van Experience Platforms [!UICONTROL Credentials] in **[!UICONTROL ** Server **]** tekstveld.

      1. Plakken **[!UICONTROL ** Database **]** parameter van Experience Platforms [!UICONTROL Credentials] in **[!UICONTROL ** Database **]** tekstveld.

         Toevoegen `?FLATTEN` aan de **[!UICONTROL ** Database **]** parameter, zodat het als leest `prod:cja?FLATTEN` bijvoorbeeld. Zie [Geneste gegevensstructuren samenvoegen voor gebruik met BI-gereedschappen van derden](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie .

      1. Wanneer wordt gevraagd om **[!UICONTROL Data Connectivity]** modus, selecteren **[!UICONTROL DirectQuery]**.

      1. U wordt gevraagd **[!UICONTROL Username]** en **[!UICONTROL Password]**. De equivalente parameters van Experience Platforms gebruiken [!UICONTROL Credentials].


   1. Na succesvolle login, verschijnen de lijsten van de de gegevensmening van de Customer Journey Analytics in Power BI **[!UICONTROL ** Navigator **]**.

   1. Selecteer de tabellen in de gegevensweergave die u wilt gebruiken en selecteer **[!UICONTROL ** Laden **]**.

   Alle dimensies en metriek die aan een of meer geselecteerde tabellen zijn gekoppeld, worden in het rechterdeelvenster weergegeven en kunnen in uw visualisaties worden gebruikt.

   Zie [Verbinding maken met Power BI-zoekservice](https://experienceleague.adobe.com/en/docs/experience-platform/query/clients/power-bi) voor meer informatie .

+++

+++Tableau

1. Bekijk de details van uw PostgresSQL geloofsbrieven in Adobe Experience Platform:

   1. Selecteren **[!UICONTROL ** Zoekopdrachten **]** van de linkerspoorstaaf (onder **[!UICONTROL ** GEGEVENSBEHEER **]**).

   1. Selecteren **[!UICONTROL ** Credentials **]** in de bovenste balk.

   1. Selecteer de ` cja` **[!UICONTROL ** Database **]**.

   1. Gebruiken ![Kopiëren](assets/Smock_Copy_18_N.svg) om elk van de parameters van de geloofsbrieven te kopiëren Postgres ([!UICONTROL Host], [!UICONTROL Port], [!UICONTROL Database], [!UICONTROL Username], en andere) indien nodig in Tableau.

1. In Tableau:

   1. Selecteren **[!UICONTROL ** Meer **]** van **[!UICONTROL ** Naar een server **]** in het linkerspoor.

   1. Selecteren **[!UICONTROL ** PostgresSQL **]** in de lijst.

   1. In de [!UICONTROL PostgresSQL] dialoogvenster:

      1. Plakken **[!UICONTROL ** Host **]** parameter van Experience Platforms [!UICONTROL Credentials] in **[!UICONTROL ** Server **]** tekstveld.

      1. Plakken **[!UICONTROL ** Poort **]** parameter van Experience Platforms [!UICONTROL Credentials] in **[!UICONTROL ** Poort **]** tekstveld.

      1. Plakken **[!UICONTROL ** Database **]** parameter van Experience Platforms [!UICONTROL Credentials] in **[!UICONTROL ** Database **]** tekstveld.

         Toevoegen `%3FFLATTEN` aan de **[!UICONTROL ** Database **]** parameter, zodat het als leest `prod:cja%3FFLATTEN` bijvoorbeeld. Zie [Geneste gegevensstructuren samenvoegen voor gebruik met BI-gereedschappen van derden](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie .

      1. Selecteren **[!UICONTROL ** Gebruikersnaam en wachtwoord **]** van **[!UICONTROL ** Verificatie **]** lijst.

      1. Plakken **[!UICONTROL ** Gebruikersnaam **]** parameter van Experience Platforms [!UICONTROL Credentials] in **[!UICONTROL ** Gebruikersnaam **]** tekstveld.

      1. Plakken **[!UICONTROL ** Wachtwoord **]** parameter van Experience Platforms [!UICONTROL Credentials] in **[!UICONTROL ** Wachtwoord **]** tekstveld.

      1. Selecteren **[!UICONTROL ** Aanmelden **]**.

   1. De gegevensweergaven van de Customer Journey Analytics worden weergegeven als tabellen in het dialoogvenster **[!UICONTROL ** Tabel **]** lijst.

   1. Sleep de tabellen die u op het canvas wilt gebruiken.

   U kunt nu met de gegevens van de lijsten van de gegevensmening werken om uw rapporten en visualisaties te bouwen.

   Zie [Connect Tableau naar Query Service](https://experienceleague.adobe.com/en/docs/experience-platform/query/clients/tableau) voor meer informatie .

+++

Zie [Client verbinden met Query-service](https://experienceleague.adobe.com/en/docs/experience-platform/query/clients/overview) voor een overzicht van en meer informatie over de verschillende beschikbare instrumenten.

## Functionaliteit

Standaard hebben uw gegevensweergaven een tabelveilige naam die is gegenereerd op basis van hun vriendelijke naam. De gegevensweergave met de naam [!UICONTROL My Web Data View] heeft de weergavenaam `my_web_data_view`.

Als u de ID&#39;s van de gegevensweergave wilt gebruiken als tabelnamen, kunt u de optionele `CJA_USE_IDS` instellen op de databasenaam wanneer verbinding wordt gemaakt. Bijvoorbeeld: `prod:cja?CJA_USE_IDS` geeft uw gegevensweergaven weer met namen als `dv_ABC123`.

### Gegevensbeheer

De aan gegevensbeheer gerelateerde instellingen in Customer Journey Analytics worden overgenomen van Adobe Experience Platform. Dankzij de integratie tussen Customer Journey Analytics en Adobe Experience Platform Data Governance kunnen gevoelige gegevens van Customers Journey Analytics worden geëtiketteerd en kan het privacybeleid worden gehandhaafd.

De etiketten en het beleid van de privacy die op datasets werden gecreeerd die door Experience Platform worden verbruikt kunnen in het werkschema van de de gegevensmeningen van de Customer Journey Analytics worden bezocht. Daarom wordt aan de hand van de [!DNL Customer Journey Analytics BI extension] passende waarschuwingen of fouten tonen wanneer niet wordt voldaan aan de gedefinieerde privacylabels en beleidsregels.

### Weergaven van gegevens weergeven

In de standaardSQL CLI kunt u van uw meningen een lijst maken gebruikend `\dv`

```sql
prod:all=> \dv
                       List of relations
 Schema |                    Name                    | Type |  Owner             
--------+--------------------------------------------+------+----------
 public | my_web_data_view                           | view | postgres
 public | my_mobile_data_view                        | view | postgres
```

### Geneste in plaats van samengevoegd

Standaard gebruikt het schema van uw gegevensweergaven geneste structuren, net als de oorspronkelijke XDM-schema&#39;s. De integratie ondersteunt ook de `FLATTEN` -optie. Met deze optie kunt u afvlakken forceren van het schema voor de gegevensweergaven (en elke andere tabel in de sessie). Het afvlakken staat voor gemakkelijker gebruik in de hulpmiddelen van BI toe die geen gestructureerde schema&#39;s steunen. Zie [Werken met geneste gegevensstructuren in Query Service](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie .

### Ondersteunde SQL

Zie [SQL-naslagservice](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/overview) voor de volledige verwijzing naar welk type SQL wordt ondersteund.

Zie de onderstaande tabel voor voorbeelden van de SQL die u kunt gebruiken.

+++ Voorbeelden

| Patroon | Voorbeeld |
|---|---|
| Schema-detectie | <pre>SELECTEREN * VANUIT dv1 WAAR 1=0</pre> |
| Uitsplitsing | <pre>DIm1, SUM(metrisch1) SELECTEREN ALS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP OP DIm1</pre><pre>DIm1, SUM(metrisch1) SELECTEREN ALS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot; EN<br/>  filterId = &#39;12345&#39;<br/>GROEP OP DIm1</pre><pre>DIm1, SUM(metrisch1) SELECTEREN ALS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot; EN<br/>  EN (dim2 = &#39;A&#39; OF dim3 IN (&#39;X&#39;, &#39;Y&#39;, &#39;Z&#39;)<br/>GROEP OP DIm1</pre> |
| `HAVING` clausule | <pre>DIm1, SUM(metrisch1) SELECTEREN ALS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP OP DIm1<br/>VAN > 100</pre> |
| Onderscheiden, boven <br/>dimensiewaarden | <pre>DIM1 VERSCHUIVEN VANUIT dv1 SELECTEREN</pre><pre>DIM1 SELECTEREN ALS dv1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP OP DIm1</pre><pre>DIM1 SELECTEREN ALS dv1<br/>VAN dv1<br/>WHERE \&quot;timestamp\&quot; >= &quot;2022-01-01&quot; AND \&quot;timestamp\&quot; &lt; &quot;2022-01-02&quot;<br/>GROEP OP DIm1<br/>ORDER BY SUM(metrisch1)<br/>LIMIET 15</pre> |
| Metrische totalen | <pre>SUM(metrisch1) SELECTEREN ALS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;</pre> |
| Meerdere dimensies<br/>uitsplitsingen<br/>en toponderscheidingen | <pre>SELECTEER dim1, dim2, SUM(metrisch1) AS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP MET DIM1, dim2</pre><pre>SELECTEER dim1, dim2, SUM(metrisch1) AS m1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP MET 1, 2<br/>VOLGORDE MET 1, 2</pre><pre>DIM1 VERSCHUIVEN, dim2 SELECTEREN<br/>VAN dv1</pre> |
| Subselectie maken:<br/>Aanvullende filters<br/>resultaten | <pre>DIM1, m1 SELECTEREN<br/>VAN (<br/>  DIm1, SUM(metrisch1) SELECTEREN ALS m1<br/>  VAN dv1<br/>  WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;</br>  GROEP OP DIm1<br/>)<br/>WAAR grijs 1 in (&#39;A&#39;, &#39;B&#39;)</pre> |
| Subselectie maken:<br/>Doorheen zoeken<br/>gegevensweergaven | <pre>SELECT-toets, SUM(m1) AS totaal<br/>VAN (<br/>  DIm1 AS-toets SELECTEREN, SUM(metrisch1) AS m1<br/>  VAN dv1<br/>  WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>  GROEP OP DIm1<br/><br/>  UNIE<br/><br/>  DIm2 AS-toets SELECTEREN, SUM(m1) AS m1<br/>  FROM dv2<br/>  WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>  GROEP MET DIm2<br/>GROEP OP toets<br/>VOLGORDE PER totaal</pre> |
| Subselectie maken: <br/>Gelaagde bron, <br/>filteren, <br/>en aggregatie | Gelaagd met subselecties:<br><pre>SELECT rows.dim1, SUM(rows.m1) AS total<br/>VAN (<br/>  \_.dim1,\_.m1 SELECTEREN<br/>  VAN (<br/>    SELECTEER \* UIT dv1<br/>    WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>  ) \_<br/>  WHERE \_.dim1 in (&#39;A&#39;, &#39;B&#39;, &#39;C&#39;)<br/>) rijen<br/>GROEP MET 1<br/>VOLGORDE PER totaal</pre><br/>Lagen met CTE:<br/><pre>MET rijen AS (<br/>  MET \_ AS (<br/>    SELECTEREN * UIT data_ares<br/>    WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2021-01-01&quot; EN &quot;2021-02-01&quot;<br/>  )<br/>  SELECTEER \_.item, \_.units UIT \_<br/>  WAAR \_.item NIET NULL IS<br/>)<br/>SELECT rows.item, SUM(rows.units) AS-eenheden<br/>UIT rijen WHERE rows.item in (&#39;A&#39;, &#39;B&#39;, &#39;C&#39;)<br/>GROEP OP rijen.item</pre> |
| Hiermee selecteert u waar de<br/>metriek komt voor<br/> of worden gemengd met<br/>de afmetingen | <pre>SUM(metrisch1) SELECTEREN AS m1, dim1<br/>VAN dv1<br/>WAAR \&quot;tijdstempel\&quot; TUSSEN &quot;2022-01-01&quot; EN &quot;2022-01-02&quot;<br/>GROEP MET 2</pre> |

{style="table-layout:auto"}

+++

### Dimensies

U kunt alle standaard beschikbare afmetingen selecteren of in de gegevensweergave definiëren. U selecteert een dimensie op basis van de id.

### Metrics

De beschikbare meetgegevens zijn:

* Een van de standaard beschikbare meetwaarden;
* Gedefinieerd in de gegevensweergave;
* Berekende meetgegevens die compatibel zijn met de gegevensweergave waartoe de gebruiker toegang heeft.

U selecteert metrisch door zijn identiteitskaart die in a wordt verpakt `SUM(metric)` -expressie, net als bij andere SQL-bronnen.

U kunt het volgende gebruiken:

* `SELECT COUNT(*)` of `COUNT(1)` om de voorvallen metrisch te krijgen.
* `SELECT COUNT(DISTINCT dimension)` of `SELECT APPROX_COUNT_DISTINCT(dimension)` om de ongeveer verschillende waarden van een dimensie te tellen. Zie details in [Afzonderlijke waarden tellen](#counting-distinct-values).
* [Inline-berekeningen](#inline-calculations) metriek op de vlucht combineren en/of wiskunde op hen doen.

#### Afzonderlijke waarden tellen

Door de onderliggende aard van hoe Customer Journey Analytics werkt, is de enige dimensie waarvoor u een exacte telling kunt krijgen, de `adobe_personid` dimensie. De volgende SQL-instructies `SELECT COUNT(DISTINCT adobe_personid)` of `SELECT APPROX_COUNT_DISTINCT(adobe_personid)` Retourneer de waarde van de maatstaf voor standaardpersonen, die het aantal verschillende personen is. Voor andere dimensies, wordt een ongeveer verschillende telling teruggekeerd.

#### Voorwaardelijke metriek

U kunt een `IF` of `CASE` in de `SUM` of `COUNT` functies om extra filtreren toe te voegen die voor geselecteerde metrisch specifiek is. Het toevoegen van deze clausules is gelijkaardig aan het toepassen van een filter op een metrische kolom in een de rapportlijst van de Werkruimte.

Voorbeelden:

```sql
SUM(IF(dim1 = 'X' AND dim2 = 'A', metric1, 0)) AS m1
```

```sql
SUM(CASE WHEN dim1 = 'X' AND dim2 = 'A' THEN metric1 END) AS m1
```

#### Inline-berekeningen

U kunt extra wiskunde op metrische uitdrukkingen toepassen in uw `SELECT` in plaats van dat de wiskunde in berekende metrisch wordt bepaald. In de volgende tabel wordt aangegeven welke typen expressies worden ondersteund.

| Operator of functie | Details |
|---|---|
| `+`, `-`, `*`, `/`, en `%` | Toevoegen, aftrekken, vermenigvuldigen, verdelen en modulair/restant |
| `-X` of `+X` | Het teken wijzigen of een metrische waarde instellen waarbij X de metrische expressie is |
| `PI()` | Constante π |
| `POSITIVE`, `NEGATIVE`, `ABS`, `FLOOR`, `CEIL`, `CEILING`, `EXP`, `LN`, `LOG10`, `LOG1P`, `SQRT`, `CBRT`, `DEGREES`, `RADIANS`, `SIN`, `COS`, `TAN`, `ACOS`, `ASIN`, `ATAN`, `COSH`, `SINH`, en `TANH` | Unaire rekenfuncties |
| `MOD`, `POW`, `POWER`, `ROUND`, `LOG` | Binaire wiskundige functies |

{style="table-layout:auto"}

### Speciale kolommen

#### Tijdstempel

De `timestamp` de speciale kolom wordt gebruikt om de datumwaaiers voor de vraag te verstrekken. Een datumbereik kan worden gedefinieerd met een `BETWEEN` expressie of een paar `timestamp` `>`, `>=`, `<`, `<=` controles `AND`rd samen.
De `timestamp` is optioneel en als geen volledig bereik wordt opgegeven, worden standaardwaarden gebruikt:

* Als er slechts een minimum is opgegeven (`timestamp > X` of ` timestamp >= X`), loopt het bereik van X tot nu.
* Als slechts een maximum wordt verstrekt (`timestamp < X` of `timestamp <= X`), ligt het bereik tussen X min 30 dagen en X.
* Als er niets is opgegeven, ligt het bereik van nu min 30 dagen tot nu.

Het tijdstempelbereik wordt geconverteerd naar een algemeen filter voor het datumbereik in RankedRequest.
Het tijdstempelveld kan ook worden gebruikt in datum-/tijdfuncties om de tijdstempel van de gebeurtenis te parseren of af te kappen.

#### Datumbereik

De `daterange` speciale kolommen, vergelijkbaar met  `timestamp`Het filteren is echter beperkt tot volledige dagen. De `daterange` is ook optioneel en heeft dezelfde standaardwaarden als `timestamp`.
De `daterange` veld kan ook worden gebruikt in datum-/tijdfuncties om de gebeurtenisdatum te parseren of af te kappen.

De `daterangeName` de speciale kolom kan worden gebruikt om uw vraag te filtreren gebruikend een genoemde datumwaaier als `Last Quarter`.

>[!NOTE]
>
>PowerBI biedt geen ondersteuning voor `daterange` metriek die minder dan een dag zijn (uur, 30 minuten, 5 minuten, enz.).


#### Filter-id

De `filterId` speciale kolom is optioneel en wordt gebruikt om een extern gedefinieerd filter toe te passen op de query. Het toepassen van een extern gedefinieerd filter op een query lijkt op het slepen van een filter in een deelvenster in Workspace. Er kunnen meerdere filter-id&#39;s worden opgegeven door `AND`-ing hen.

Samen met `filterId`kunt u `filterName` als u de naam van een filter wilt gebruiken in plaats van de id.

### Indien clausule

De `WHERE` clausule wordt in drie stappen afgehandeld:

1. Het datumbereik zoeken in het menu `timestamp`, `daterange`, of `daterangeName` speciale velden.

1. Extern gedefinieerde zoeken `filterId`s of `filterName`s om in het filtreren op te nemen.

1. Zet de resterende expressies om in ad-hocfilters.

De behandeling wordt uitgevoerd door het eerste niveau van `AND`s in de `WHERE` clausule. Elk hoogste niveau `AND`-ed expression must match one of the above. Iets dieper dan het eerste niveau van `AND`s, of als de `WHERE` componentgebruik `OR`Op het hoogste niveau wordt dit als een ad-hocfilter behandeld.

### Sorteervolgorde

Door gebrek, sorteert de vraag de resultaten door eerste geselecteerde metrisch in dalende orde. U kunt de standaardsorteervolgorde overschrijven door `ORDER BY ... ASC` of `ORDER BY ... DESC`. Als u `ORDER BY`moet u `ORDER BY` op de eerste geselecteerde metrische waarde.

U kunt de volgorde ook spiegelen met `-` (min) vóór de metrische waarde. Beide onderstaande instructies resulteren in dezelfde volgorde:

```sql
ORDER BY metric1 ASC
```

```sql
ORDER BY -metric1 DESC
```

### Algemene functieondersteuning

| Functie | Voorbeeld | Details |
|---|---|---|
| [Gegoten](https://spark.apache.org/docs/latest/api/sql/index.html#cast) | ``CAST(`timestamp` AS STRING)`` of <br/> `` `timestamp`::string `` | Type casting wordt momenteel niet ondersteund, maar er wordt geen fout gegenereerd. De `CAST` functie wordt genegeerd. |
| [Tijdstempel](https://spark.apache.org/docs/latest/api/sql/index.html#timestamp) | `` WHERE `timestamp` >= TIMESTAMP('2022-01-01 00:00:00') AND   `timestamp` < TIMESTAMP('2022-01-02 00:00:00') `` | Een tijdtekenreeks parseren als een tijdstempel voor gebruik in een `WHERE` clausule. |
| [Naar tijdstempel](https://spark.apache.org/docs/latest/api/sql/index.html#to_timestamp) | `` WHERE `timestamp` >= TO_TIMESTAMP('01/01/2022', 'MM/dd/yyyy') AND `timestamp` < TO_TIMESTAMP('01/02/2022', 'MM/dd/yyyy') `` | Een tijdtekenreeks parseren als een tijdstempel voor gebruik in een `WHERE` clausule, optioneel verstrekkend een formaat voor die tijdkoord. |
| [Datum](https://spark.apache.org/docs/latest/api/sql/index.html#date) | `` WHERE `timestamp` >= DATE('2022-01-01') AND `timestamp` < DATE('2022-01-02') `` | Een datumtekenreeks parseren als een tijdstempel voor gebruik in een `WHERE` clausule. |
| [Tot op heden](https://spark.apache.org/docs/latest/api/sql/index.html#to_date) | `` WHERE `timestamp` >= TO_DATE('01/01/2022', 'MM/dd/yyyy') AND `timestamp` < TO_DATE('01/02/2022', 'MM/dd/yyyy') `` | Een datumtekenreeks parseren als een tijdstempel voor gebruik in een `WHERE` -component, optioneel een notatie voor die datumtekenreeks opgeven. |

{style="table-layout:auto"}

### Ondersteuning van Dimension-functies

Deze functies kunnen worden gebruikt voor dimensies in de `SELECT`, `WHERE` clausule, of in voorwaardelijke metriek.

**Reeksfuncties**

| Functie | Voorbeeld | Details |
|---|---|---|
| [Onder](https://spark.apache.org/docs/latest/api/sql/index.html#lower) | ``SELECT LOWER(name) AS lower_name`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |

{style="table-layout:auto"}

**Datum- en tijdfuncties**

| Functie | Voorbeeld | Details |
|---|---|---|
| [Jaar](https://spark.apache.org/docs/latest/api/sql/index.html#year) | ``SELECT YEAR(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [Maand](https://spark.apache.org/docs/latest/api/sql/index.html#month) | ``SELECT MONTH(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [Dag](https://spark.apache.org/docs/latest/api/sql/index.html#day) | ``SELECT DAY(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [Dag van de week](https://spark.apache.org/docs/latest/api/sql/index.html#dayofweek) | ``SELECT DAYOFWEEK(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde omdat u het nummer en niet de vriendschappelijke naam nodig hebt. |
| [Dag van jaar](https://spark.apache.org/docs/latest/api/sql/index.html#dayofyear) | ``SELECT DAYOFYEAR(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [Week](https://spark.apache.org/docs/latest/api/sql/index.html#week) | ``SELECT WEEK(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [Kwart](https://spark.apache.org/docs/latest/api/sql/index.html#quarter) | ``SELECT QUARTER(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [Uur](https://spark.apache.org/docs/latest/api/sql/index.html#hour) | ``SELECT HOUR(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde omdat u het nummer en niet de vriendschappelijke naam nodig hebt. |
| [Minute](https://spark.apache.org/docs/latest/api/sql/index.html#minute) | ``SELECT MINUTE(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [Extraheren](https://spark.apache.org/docs/latest/api/sql/index.html#extract) | ``SELECT EXTRACT(MONTH FROM `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde voor sommige onderdelen van deze functie omdat u het nummer nodig hebt en niet de vriendschappelijke naam.<br/>Ondersteunde onderdelen zijn:<br>- Trefwoorden: `YEAR`, `MONTH`, `DAYOFMONTH`, `DAYOFWEEK`, `DAYOFYEAR`, `WEEK`, `QUARTER`, `HOUR`, `MINUTE`.<br/>- Tekenreeksen:  `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&quot;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'`, of `'MINUTE'`. |
| [Datum (deel)](https://spark.apache.org/docs/latest/api/sql/index.html#date_part) | ``SELECT DATE_PART('month', `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde voor sommige onderdelen van deze functie omdat u het nummer nodig hebt en niet de vriendschappelijke naam.<br/>Ondersteunde tekenreeksonderdelen zijn: `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&quot;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'`, of `'MINUTE'`. |
| [Datum (afgebroken)](https://spark.apache.org/docs/latest/api/sql/index.html#date_trunc) | ``SELECT DATE_TRUNC('quarter', `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven.<br/>Ondersteunde tekenreeksgranulariteiten zijn: `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&quot;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'`, of `'MINUTE'`. |

{style="table-layout:auto"}
