---
title: Customer Journey Analytics BI-extensie
description: Leer hoe u Power BI of Tableau kunt gebruiken om tot gegevensmeningen toegang te hebben gebruikend de uitbreiding van Customer Journey Analytics BI.
solution: Customer Journey Analytics
feature: BI Extension
role: Admin
exl-id: ab7e1f15-ead9-46b7-94b7-f81802f88ff5
source-git-commit: 81bde9f61f208fd01b3ba1c3df57609104109800
workflow-type: tm+mt
source-wordcount: '2901'
ht-degree: 0%

---

# Customer Journey Analytics BI-extensie

{{select-package}}

[!DNL Customer Journey Analytics BI extension] laat SQL toegang tot de [ gegevensmeningen ](./data-views.md) toe die u in Customer Journey Analytics hebt bepaald. Uw gegevensingenieurs en analisten zouden met Power BI, Tableau, of andere bedrijfsintelligentie en visualisatiehulpmiddelen (verder die als hulpmiddelen van BI worden bedoeld) vertrouwd kunnen zijn. Ze kunnen nu rapporten en dashboards maken op basis van dezelfde gegevensweergaven die gebruikers van Customers Journey Analytics gebruiken bij het maken van hun Analysis Workspace-projecten.

De Dienst van de Vraag van Adobe Experience Platform [ ](https://experienceleague.adobe.com/en/docs/experience-platform/query/home) is de SQL interface aan gegevens beschikbaar in het gegevensmeer van Experience Platform. Als [!DNL Customer Journey Analytics BI extension] ingeschakeld is, wordt de functionaliteit van [!DNL Query Service] uitgebreid om de gegevensweergaven van uw Customer Journey Analytics als tabellen of weergaven in een [!DNL Query Service] -sessie te zien. Dit betekent dat hulpprogramma&#39;s voor bedrijfsintelligentie die [!DNL Query Service] als hun PostgresSQL-interface gebruiken, naadloos van deze uitgebreide functionaliteit profiteren.

De belangrijkste voordelen zijn:

* Het is niet nodig om een gelijkwaardige vertegenwoordiging van de gegevensmeningen van de Customer Journey Analytics binnen het hulpmiddel van BI zelf te ontspannen. <br/> zie [ meningen van Gegevens ](data-views.md) voor meer informatie over de functionaliteit van gegevensmeningen om te begrijpen wat moet worden ontspannen.
* Meer consistentie in rapportage en analyse tussen BI-instrumenten en Customer Journey Analytics.
* Combineer de gegevens van de Customer Journey Analytics met andere gegevensbronnen reeds beschikbaar in de hulpmiddelen van BI.

## Vereisten

U moet beschikken over:

<!---   Enable the [!UICONTROL Customer Journey Analytics BI extension] in your Experience Platform organization. -->

* Verleende toegang tot Experience Platform en Customer Journey Analytics.
* Beheerders van beperkte producten hebben toegang tot Customer Journey Analytics, zodat u verbindingen en gegevensweergaven kunt weergeven, bewerken, bijwerken of verwijderen.
* Toegang verleend tot de gegevensweergaven die u wilt openen.
* Toegang verleend tot de CJA BI-extensie.
* Gebruik het verlopen van niet-vervallende geloofsbrieven om de hulpmiddelen van BI met [!DNL Customer Journey Analytics BI extension] te verbinden. De [ gids van Referenties ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/credentials) verstrekt meer informatie bij het plaatsen van het verlopen van geloofsbrieven of niet-het verlopen geloofsbrieven.

Zie [ Controle van de Toegang van de Reis van de Klant ](../technotes/access-control.md) voor meer informatie, specifiek de [ extra toestemmingen van Admin van het Product ](../technotes/access-control.md#product-admin-additional-permissions) en [ Toestemmingen van de Customer Journey Analytics in de Admin Console ](../technotes/access-control.md#customer-journey-analytics-permissions-in-admin-console).


## Gebruik

Als u de functie [!DNL Customer Journey Analytics BI extension] wilt gebruiken, kunt u SQL rechtstreeks gebruiken of de slepen en neerzetten-ervaring gebruiken die beschikbaar is in het specifieke gereedschap BI.

### SQL

U kunt de functionaliteit direct in SQL verklaringen gebruiken gebruikend of de Redacteur van de Vraag of een standaard bevel-lijn van PostgresSQL (CLI) cliënt.

+++ Query-editor

In Adobe Experience Platform:

1. Selecteer **[!UICONTROL ** Vragen **]** van **[!UICONTROL ** GEGEVENSBEHEER **]** in het linkerspoor.

1. Selecteer ![ creëren Vraag ](assets/Smock_AddCircle_18_N.svg) **[!UICONTROL ** vraag **]** creëren.

1. Selecteer het `cja` **[!UICONTROL ** Gegevensbestand **]**.

1. Om de vraag uit te voeren, typ uw SQL verklaring en selecteer ![ Spel ](assets/Smock_Play_18_N.svg) knoop (of druk `[SHIFT]` + `[ENTER]`).

+++


+++ PostgresSQL CLI

1. Zoek en kopieer uw PostgresSQL-referenties in Adobe Experience Platform:

   1. Selecteer **[!UICONTROL ** Vragen **]** van de linkerspoorlijn (onder **[!UICONTROL ** GEGEVENSBEHEER **]**).

   1. Selecteer **[!UICONTROL ** Referenties **]** van de hoogste bar.

   1. Selecteer het `cja` **[!UICONTROL ** Gegevensbestand **]**.

   1. Om het bevelkoord te kopiëren, gebruik ![ Exemplaar ](assets/Smock_Copy_18_N.svg) in de **[!UICONTROL ** bevel PSQL **]** sectie.

1. Open een opdracht- of terminalvenster.

1. Als u zich wilt aanmelden en uw query&#39;s wilt uitvoeren, plakt u de opdrachttekenreeks in uw terminal.

+++

Zie de [ gids UI van de Redacteur van de Vraag ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/user-guide) voor meer informatie.


### BI-gereedschappen

Momenteel wordt [!DNL Customer Journey Analytics BI extension] alleen ondersteund en getest op Power BI en Tableau. Andere hulpmiddelen van BI die de interface PSQL gebruiken zouden ook kunnen werken, maar officieel nog niet gesteund.

+++ Power BI

1. Bekijk de details van uw PostgresSQL geloofsbrieven in Adobe Experience Platform:

   1. Selecteer **[!UICONTROL ** Vragen **]** van de linkerspoorlijn (onder **[!UICONTROL ** GEGEVENSBEHEER **]**).

   1. Selecteer **[!UICONTROL ** Referenties **]** van de hoogste bar.

   1. Selecteer het `cja` **[!UICONTROL ** Gegevensbestand **]**.

   1. Gebruik ![ Exemplaar ](assets/Smock_Copy_18_N.svg) om elk van de parameters van de geloofsbrieven van Postgres ([!UICONTROL Host], [!UICONTROL Port], [!UICONTROL Database], [!UICONTROL Username], en anderen) te kopiëren wanneer nodig in Power BI.

1. In Power BI:

   1. In het belangrijkste venster, uitgezochte **[!UICONTROL ** krijgt gegevens **]** van de hoogste toolbar.

   1. Selecteer **[!UICONTROL More...]** in het linkerspoor.

   1. In **krijgt het 1} scherm van Gegevens {, onderzoek naar `PostgresSQL` en selecteer het **[!UICONTROL **gegevensbestand PostgresSQL **]**van de lijst.**

   1. In het **[!UICONTROL ** PostgressSQL- gegevensbestand **]** dialoog:

      1. Plak de **]** parameter van de Gastheer **[!UICONTROL ** van de Vragen van het Experience Platform [!UICONTROL Credentials] op het **[!UICONTROL ** de tekstgebied van de Server **]**.

      1. Plak de **[!UICONTROL ** parameter van het Gegevensbestand **]** van de Vragen van het Experience Platform [!UICONTROL Credentials] in het **[!UICONTROL ** 4} tekstgebied van het Gegevensbestand {.**]**

         Voeg `?FLATTEN` aan de **[!UICONTROL ** 2} parameter van het Gegevensbestand {toe, zodat leest het als `prod:cja?FLATTEN` bijvoorbeeld. **]** Zie [ genestelde gegevensstructuren voor gebruik met de hulpmiddelen van derdeBI ](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie afvlakken.

      1. Selecteer **[!UICONTROL DirectQuery]** wanneer hierom wordt gevraagd voor de modus **[!UICONTROL Data Connectivity]** .

      1. U wordt gevraagd om **[!UICONTROL Username]** en **[!UICONTROL Password]** . Gebruik de equivalente parameters van Experience Platforms query&#39;s [!UICONTROL Credentials] .


   1. Na succesvolle login, verschijnen de lijsten van de de gegevensmening van de Customer Journey Analytics in de Navigator van Power BIs **[!UICONTROL ** **]**.

   1. Selecteer de lijsten van de gegevensmening die u **[!UICONTROL ** Lading **]** wilt gebruiken en selecteren.

   Alle dimensies en metriek die aan een of meer geselecteerde tabellen zijn gekoppeld, worden in het rechterdeelvenster weergegeven en kunnen in uw visualisaties worden gebruikt.

   Zie [ verbinden Power BI met de Dienst van de Vraag ](https://experienceleague.adobe.com/en/docs/experience-platform/query/clients/power-bi) voor meer informatie.

+++

+++Tableau

1. Bekijk de details van uw PostgresSQL geloofsbrieven in Adobe Experience Platform:

   1. Selecteer **[!UICONTROL ** Vragen **]** van de linkerspoorlijn (onder **[!UICONTROL ** GEGEVENSBEHEER **]**).

   1. Selecteer **[!UICONTROL ** Referenties **]** van de hoogste bar.

   1. Selecteer het ` cja` **[!UICONTROL ** Gegevensbestand **]**.

   1. Gebruik ![ Exemplaar ](assets/Smock_Copy_18_N.svg) om elk van de parameters van de geloofsbrieven van Postgres ([!UICONTROL Host], [!UICONTROL Port], [!UICONTROL Database], [!UICONTROL Username], en anderen) te kopiëren wanneer nodig in Tableau.

1. In Tableau:

   1. Selecteer **[!UICONTROL ** Meer **]** van **[!UICONTROL ** aan een Server **]** in het linkerspoor.

   1. Selecteer **[!UICONTROL ** PostgresSQL **]** van de lijst.

   1. In het dialoogvenster [!UICONTROL PostgresSQL] :

      1. Plak de **]** parameter van de Gastheer **[!UICONTROL ** van de Vragen van het Experience Platform [!UICONTROL Credentials] in het **[!UICONTROL ** de tekstgebied van de Server **]**.

      1. Plak de **[!UICONTROL ** Poort **]** parameter van de Vragen van het Experience Platform [!UICONTROL Credentials] in het **[!UICONTROL ** Poort **]** tekstgebied.

      1. Plak de **[!UICONTROL ** parameter van het Gegevensbestand **]** van de Vragen van het Experience Platform [!UICONTROL Credentials] in het **[!UICONTROL ** 4} tekstgebied van het Gegevensbestand {.**]**

         Voeg `%3FFLATTEN` aan de **[!UICONTROL ** 2} parameter van het Gegevensbestand {toe, zodat leest het als `prod:cja%3FFLATTEN` bijvoorbeeld. **]** Zie [ genestelde gegevensstructuren voor gebruik met de hulpmiddelen van derdeBI ](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie afvlakken.

      1. Selecteer **[!UICONTROL ** Gebruikersnaam en Wachtwoord **]** van **[!UICONTROL ** Authentificatie **]** lijst.

      1. Plak **[!UICONTROL ** Gebruikersnaam **]** parameter van de Vragen van het Experience Platform [!UICONTROL Credentials] in **[!UICONTROL ** Gebruikersnaam **]** tekstgebied.

      1. Plak de **[!UICONTROL ** parameter van het Wachtwoord **]** van de Vragen van het Experience Platform [!UICONTROL Credentials] in het **[!UICONTROL ** 4} tekstgebied van het Wachtwoord.**]**

      1. Selecteer het **[!UICONTROL ** Teken binnen **]**.

   1. De de gegevensmeningen van de Customer Journey Analytics tonen omhoog als lijsten in de **[!UICONTROL ** lijst van de Lijst **]**.

   1. Sleep de tabellen die u op het canvas wilt gebruiken.

   U kunt nu met de gegevens van de lijsten van de gegevensmening werken om uw rapporten en visualisaties te bouwen.

   Zie [ Connect Tableau aan de Dienst van de Vraag ](https://experienceleague.adobe.com/en/docs/experience-platform/query/clients/tableau) voor meer informatie.

+++

Zie [ cliënten met de Dienst van de Vraag ](https://experienceleague.adobe.com/en/docs/experience-platform/query/clients/overview) voor een overzicht van en meer informatie over de diverse beschikbare hulpmiddelen verbinden.

## Functionaliteit

Standaard hebben uw gegevensweergaven een tabelveilige naam die is gegenereerd op basis van hun vriendelijke naam. De gegevensweergave met de naam [!UICONTROL My Web Data View] heeft bijvoorbeeld de weergavenaam `my_web_data_view` . U kunt een voorkeursnaam definiëren voor gebruik in uw BI-gereedschap voor de gegevensweergave. Zie [ de meningsmontages van Gegevens ](create-dataview.md#settings) voor meer informatie.

Als u de ID&#39;s van de gegevensweergave wilt gebruiken als tabelnamen, kunt u de optionele instelling `CJA_USE_IDS` toevoegen aan de databasenaam wanneer u verbinding maakt. `prod:cja?CJA_USE_IDS` geeft bijvoorbeeld uw gegevensweergaven weer met namen als `dv_ABC123` .

### Gegevensbeheer

De aan gegevensbeheer gerelateerde instellingen in Customer Journey Analytics worden overgenomen van Adobe Experience Platform. Dankzij de integratie tussen Customer Journey Analytics en Adobe Experience Platform Data Governance kunnen gevoelige gegevens van Customers Journey Analytics worden geëtiketteerd en kan het privacybeleid worden gehandhaafd.

De etiketten en het beleid van de privacy die op datasets werden gecreeerd die door Experience Platform worden verbruikt kunnen in het werkschema van de de gegevensmeningen van de Customer Journey Analytics worden bezocht. Daarom geven gegevens die met [!DNL Customer Journey Analytics BI extension] worden gevraagd, passende waarschuwingen of fouten weer wanneer ze niet voldoen aan de gedefinieerde privacylabels en beleidsregels.

#### Standaardwaarden en beperkingen

Om redenen van gegevensbeheer zijn de volgende aanvullende standaardwaarden en beperkingen van toepassing.

* De extensie BI vereist een rijlimiet voor de resultaten van de query. De standaardwaarde is 50, maar u kunt dit overschrijven in SQL met behulp van `LIMIT n` , waarbij `n` 1 - 50000 is.
* De extensie BI vereist een datumbereik om de rijen voor berekeningen te beperken. De standaardwaarde is de laatste 30 dagen, maar u kunt dit in uw SQL `WHERE` -component overschrijven met behulp van de speciale [`timestamp`](#timestamp) - of [`daterange`](#date-range) -kolommen.
* Voor de extensie BI zijn samengevoegde query&#39;s vereist. U kunt SQL niet gebruiken zoals `SELECT * FROM ...` om de ruwe, onderliggende rijen te krijgen. Op een hoog niveau, zouden uw gezamenlijke vragen moeten gebruiken:
   * Selecteer totalen met `SUM` en/of `COUNT` .<br/> Bijvoorbeeld `SELECT SUM(metric1), COUNT(*) FROM ...`
   * Selecteer metriek uitgesplitst op een afmeting. <br/> Bijvoorbeeld, `SELECT dimension1, SUM(metric1), COUNT(*) FROM ... GROUP BY dimension1`
   * Selecteer duidelijke metrische waarden.<br/> Bijvoorbeeld, `SELECT DISTINCT dimension1 FROM ...`

     Zie voor meer details [ Ondersteunde SQL ](#supported-sql).

### Weergaven van gegevens weergeven

In de standaard PostSQL CLI kunt u uw weergaven weergeven met `\dv`

```sql
prod:all=> \dv
                       List of relations
 Schema |                    Name                    | Type |  Owner             
--------+--------------------------------------------+------+----------
 public | my_web_data_view                           | view | postgres
 public | my_mobile_data_view                        | view | postgres
```

### Geneste in plaats van samengevoegd

Standaard gebruikt het schema van uw gegevensweergaven geneste structuren, net als de oorspronkelijke XDM-schema&#39;s. De integratie ondersteunt ook de optie `FLATTEN` . Met deze optie kunt u afvlakken forceren van het schema voor de gegevensweergaven (en elke andere tabel in de sessie). Het afvlakken staat voor gemakkelijker gebruik in de hulpmiddelen van BI toe die geen gestructureerde schema&#39;s steunen. Zie [ Werkend met genestelde gegevensstructuren in de Dienst van de Vraag ](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie.

### Ondersteunde SQL

Zie {SQL van de Dienst van de Vraag 1} voor de volledige verwijzing op welk type van SQL wordt gesteund.[](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/overview)

Zie de onderstaande tabel voor voorbeelden van de SQL die u kunt gebruiken.

+++ Voorbeelden

| Patroon | Voorbeeld |
|---|---|
| Schema-detectie | <pre>SELECTEREN * VANUIT dv1 WAAR 1=0</pre> |
| Geschikt of uitgesplitst | <pre>SELECTEER dim1, SUM(metrisch1) AS m1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;GROUP DOOR dim1<br/></pre><pre>SELECTEER dim1, SUM(metrisch1) AS m1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;EN <br/> filterId = &quot;12345&quot;<br/> GROUP DOOR dim1</pre><pre>SELECTEER dim1, SUM(metrisch1) ALS m1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;EN <br/> EN (dim2 = &quot;A&quot;OF dim3 IN (&#39;X&#39;, &quot;Y&quot;Z&quot;,&#39;) <br/> GROEP DOOR dim1</pre> |
| `HAVING` component | <pre>SELECTEER dim1, SUM(metrisch1) AS m1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;<br/> GROEP DOOR dim1 <br/> HEBBENDE m1 > 100</pre> |
| Afzonderlijk, hoogste <br/> afmetingswaarden | <pre>DIM1 VERSCHUIVEN VANUIT dv1 SELECTEREN</pre><pre>SELECTEER dim1 AS dv1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;<br/> GROEP DOOR dim1</pre><pre>SELECTEER dim1 AS dv1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot; >= &quot;2022-01-01&quot;EN \ &quot;timestamp\&quot;&lt; &quot;2022-01-02&quot;<br/> GROUP DOOR dim1 <br/> ORDER DOOR SUM(meetnorm1) <br/> LIMIT 1 5</pre> |
| Metrische totalen | <pre>SELECTEER SUM (metrisch1) ALS m1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;</pre> |
| De multi-dimensie <br/> breken <br/> en top-Distts | <pre>SELECTEER dim1, dim2, SUM (metrisch1) AS m1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;<br/> GROEP DOOR dim1, dim2</pre><pre>SELECTEER dim1, dim2, SUM (metrisch1) AS m1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;GROEP DOOR 1, 2 <br/> ORDER DOOR 1, 2<br/></pre><pre>SELECTEER DISTINCT dim1, dim2 <br/> VAN dv1</pre> |
| Subselect:<br/> de extra resultaten van de Filter <br/> | <pre>SELECTEER dim1, m1 <br/> VAN (<br/> SELECTEER dim1, SUM (metrisch1) ALS m1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;</br> GROUP DOOR dim1 <br/>) <br/> WAAR dim1 in (&quot;A&quot;, &quot;B&quot;)</pre> |
| Subselect:<br/> het Vragen over <br/> gegevensmeningen | <pre>SELECTEER sleutel, SUM(m1) ALS totaal <br/> VAN (<br/> SELECTEER dim1 ALS sleutel, SUM(metrisch1) AS m1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;GROUP DOOR m1 <br/><br/> UNION <br/><br/> SELECTEER dim2 ALS sleutel, SUM(m1) AS m1 <br/> VAN dv2 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;<br/> GROEP DOOR dim2 <br/> GROUP sleutel <br/> ORDER DOOR totaal<br/></pre> |
| Subselect: <br/> Gelaagde bron, <br/> het filtreren, <br/> en samenvoeging | Gelaagd gebruikend subselects:<br><pre>SELECT rows.dim1, SUM (rows.m1) ALS totaal <br/> VAN (<br/> SELECT \_.dim1, \_.m1 <br/> VAN (<br/>    SELECTEER \* UIT dv1 <br/>    WAAR \&quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;<br/>) \_ <br/> WAAR \_.dim1 in (&quot;A&quot;, &quot;B&quot;, &quot;C&quot;) <br/>) rijen <br/> GROEP DOOR 1 <br/> ORDER DOOR totaal</pre><br/> Lagen die CTE gebruiken MET:<br/><pre>MET rijen AS (<br/> MET \_ AS (<br/>    SELECT * FROM data_ares <br/>    WAAR \&quot;timestamp\&quot;TUSSEN &quot;2021-01-01&quot;EN &quot;2021-02-01&quot;<br/>) <br/> SELECT \_.item, \_.units VAN \_<br/> WAAR \_.item NIET ONGELDIG <br/> IS) <br/> SELECT rows.item, SUM (rows.units) ALS eenheden <br/> VAN rijen WAAR rows.item in (&quot;A&quot;, &quot;B&quot;, &quot;C&quot;) <br/> GROEP DOOR rows.item</pre> |
| Selecteert waar de <br/> metriek vóór <br/> komen of met <br/> gemengd zijn | <pre>SELECTEER SUM (metrisch1) ALS m1, dim1 <br/> VAN dv1 <br/> WAAR \ &quot;timestamp\&quot;TUSSEN &quot;2022-01-01&quot;EN &quot;2022-01-02&quot;<br/> GROEP DOOR 2</pre> |

{style="table-layout:auto"}

+++

### Dimensies

U kunt alle standaard beschikbare afmetingen selecteren of in de gegevensweergave definiëren. U selecteert een dimensie op basis van de id.

### Metrics

De beschikbare meetgegevens zijn:

* Een van de standaard beschikbare meetwaarden;
* Gedefinieerd in de gegevensweergave;
* Berekende meetgegevens die compatibel zijn met de gegevensweergave waartoe de gebruiker toegang heeft.

U selecteert metrisch op zijn identiteitskaart die in een `SUM(metric)` uitdrukking wordt verpakt enkel zoals u met andere SQL bronnen zou doen.

U kunt het volgende gebruiken:

* `SELECT COUNT(*)` of `COUNT(1)` om de instantie metrisch te maken.
* `SELECT COUNT(DISTINCT dimension)` of `SELECT APPROX_COUNT_DISTINCT(dimension)` om de ongeveer verschillende waarden van een dimensie te tellen. Zie details in [ Tellend verschillende waarden ](#counting-distinct-values).
* [ Inline berekeningen ](#inline-calculations) om metriek op de vlucht te combineren en/of wiskunde op hen te doen.

#### Afzonderlijke waarden tellen

Vanwege de onderliggende aard van hoe Customer Journey Analytics werkt, is de `adobe_personid` -dimensie de enige dimensie waarvoor u een exacte telling kunt krijgen. De volgende SQL-instructies `SELECT COUNT(DISTINCT adobe_personid)` of `SELECT APPROX_COUNT_DISTINCT(adobe_personid)` retourneren de waarde van de maateenheid voor standaardpersonen. Dit is het aantal verschillende personen. Voor andere dimensies, wordt een ongeveer verschillende telling teruggekeerd.

#### Voorwaardelijke metriek

U kunt een `IF` - of `CASE` -component insluiten in de `SUM` - of `COUNT` -functies om aanvullende filters toe te voegen die specifiek zijn voor een geselecteerde metrische waarde. Het toevoegen van deze clausules is gelijkaardig aan het toepassen van een filter op een metrische kolom in een het rapportlijst van Workspace.

Voorbeelden:

```sql
SUM(IF(dim1 = 'X' AND dim2 = 'A', metric1, 0)) AS m1
```

```sql
SUM(CASE WHEN dim1 = 'X' AND dim2 = 'A' THEN metric1 END) AS m1
```

#### Inline-berekeningen

U kunt extra wiskunde op metrische uitdrukkingen in uw `SELECT` toepassen. Deze wiskunde kan in plaats van het bepalen van de wiskunde in berekende metrisch worden gebruikt. In de volgende tabel wordt aangegeven welke typen expressies worden ondersteund.

| Operator of functie | Details |
|---|---|
| `+` , `-` , `*` , `/` en `%` | Toevoegen, aftrekken, vermenigvuldigen, verdelen en modulair/restant |
| `-X` of `+X` | Het teken wijzigen of een metrische waarde instellen waarbij X de metrische expressie is |
| `PI()` | Constante π |
| `POSITIVE`, `NEGATIVE`, `ABS`, `FLOOR`, `CEIL`, `CEILING`, `EXP`, `LN`, `LOG10`, `LOG1P`, `SQRT`, `CBRT`, `DEGREES`, `RADIANS`, `SIN`, `COS`, `TAN`, `ACOS`, `ASIN`, `ATAN` `COSH` , `SINH` en `TANH` | Unaire rekenfuncties |
| `MOD`, `POW`, `POWER`, `ROUND`, `LOG` | Binaire wiskundige functies |

{style="table-layout:auto"}

### Speciale kolommen

#### Tijdstempel

De speciale kolom `timestamp` wordt gebruikt om de datumwaaiers voor de vraag te verstrekken. Een datumbereik kan worden gedefinieerd met een `BETWEEN` -expressie of een paar `timestamp` `>` , `>=` , `<` , `<=` checks `AND` .
`timestamp` is optioneel en als er geen volledig bereik is opgegeven, worden de standaardwaarden gebruikt:

* Als slechts een minimum wordt verstrekt (`timestamp > X` of ` timestamp >= X`), is de waaier van X tot nu.
* Als alleen een max wordt opgegeven (`timestamp < X` of `timestamp <= X` ), loopt het bereik van X min 30 dagen tot X.
* Als er niets is opgegeven, ligt het bereik van nu min 30 dagen tot nu.

Het tijdstempelbereik wordt geconverteerd naar een algemeen filter voor het datumbereik in RankedRequest.
Het tijdstempelveld kan ook worden gebruikt in datum-/tijdfuncties om de tijdstempel van de gebeurtenis te parseren of af te kappen.

#### Datumbereik

De speciale kolom van `daterange` werkt gelijkaardig aan `timestamp`; nochtans is het filtreren beperkt tot volledige dagen. `daterange` is ook optioneel en heeft dezelfde standaardwaarden voor het bereik als `timestamp` .
Het veld `daterange` kan ook worden gebruikt in datum-/tijdfuncties om de gebeurtenisdatum te parseren of af te kappen.

De speciale kolom van `daterangeName` kan worden gebruikt om uw vraag te filtreren gebruikend een genoemde datumwaaier zoals `Last Quarter`.

>[!NOTE]
>
>Power BI biedt geen ondersteuning voor `daterange` -meetwaarden die minder dan een dag zijn (uur, 30 minuten, 5 minuten, enzovoort).
>

#### Filter-id

De speciale kolom `filterId` is optioneel en wordt gebruikt om een extern gedefinieerd filter toe te passen op de query. Het toepassen van een extern gedefinieerd filter op een query lijkt op het slepen van een filter op een deelvenster in Workspace. U kunt meerdere filter-id&#39;s gebruiken door ze `AND` te laten renderen.

Samen met `filterId` kunt u `filterName` gebruiken om de naam van een filter te gebruiken in plaats van de id.

### Indien clausule

De component `WHERE` wordt in drie stappen afgehandeld:

1. Zoek het datumbereik in de speciale velden `timestamp` , `daterange` of `daterangeName` .

1. Zoek om het even welke extern gedefiniëerde `filterId` s of `filterName` s om in het filtreren te omvatten.

1. Zet de resterende expressies om in ad-hocfilters.

De afhandeling wordt uitgevoerd door het eerste niveau van `AND` s in de `WHERE` -component te parseren. Elke `AND` -ed-expressie op het hoogste niveau moet overeenkomen met een van de bovenstaande expressies. Om het even wat dieper dan het eerste niveau van `AND` s, of, als de `WHERE` clausule `OR` op het hoogste niveau gebruikt, wordt behandeld als ad hoc filter.

### Sorteervolgorde

Door gebrek, sorteert de vraag de resultaten door eerste geselecteerde metrisch in dalende orde. U kunt de standaardsorteervolgorde overschrijven door `ORDER BY ... ASC` of `ORDER BY ... DESC` op te geven. Als u `ORDER BY` gebruikt, moet u `ORDER BY` opgeven voor de eerste geselecteerde metrische waarde.

U kunt de volgorde ook spiegelen door `-` (min) vóór de metrische waarde te gebruiken. Beide onderstaande instructies resulteren in dezelfde volgorde:

```sql
ORDER BY metric1 ASC
```

```sql
ORDER BY -metric1 DESC
```

### Algemene functieondersteuning

| Functie | Voorbeeld | Details |
|---|---|---|
| [ Gegoten ](https://spark.apache.org/docs/latest/api/sql/index.html#cast) | ``CAST(`timestamp` AS STRING)`` of <br/> `` `timestamp`::string `` | Type casting wordt momenteel niet ondersteund, maar er wordt geen fout gegenereerd. De functie `CAST` wordt genegeerd. |
| [ Tijdstempel ](https://spark.apache.org/docs/latest/api/sql/index.html#timestamp) | `` WHERE `timestamp` >= TIMESTAMP('2022-01-01 00:00:00') AND   `timestamp` < TIMESTAMP('2022-01-02 00:00:00') `` | Parseer een tijdtekenreeks als een tijdstempel voor gebruik binnen een `WHERE` -component. |
| [ aan timestamp ](https://spark.apache.org/docs/latest/api/sql/index.html#to_timestamp) | `` WHERE `timestamp` >= TO_TIMESTAMP('01/01/2022', 'MM/dd/yyyy') AND `timestamp` < TO_TIMESTAMP('01/02/2022', 'MM/dd/yyyy') `` | Parseer een tijdtekenreeks als een tijdstempel voor gebruik binnen een `WHERE` -component en geef desgewenst een indeling voor die tijdtekenreeks. |
| [ Datum ](https://spark.apache.org/docs/latest/api/sql/index.html#date) | `` WHERE `timestamp` >= DATE('2022-01-01') AND `timestamp` < DATE('2022-01-02') `` | Parseer een datumtekenreeks als een tijdstempel voor gebruik binnen een `WHERE` -component. |
| [ aan datum ](https://spark.apache.org/docs/latest/api/sql/index.html#to_date) | `` WHERE `timestamp` >= TO_DATE('01/01/2022', 'MM/dd/yyyy') AND `timestamp` < TO_DATE('01/02/2022', 'MM/dd/yyyy') `` | Analyseer een datumtekenreeks als een tijdstempel voor gebruik binnen een `WHERE` -component en geef desgewenst een indeling voor die datumtekenreeks. |

{style="table-layout:auto"}

### Ondersteuning van Dimension-functies

Deze functies kunnen worden gebruikt voor afmetingen in de component `SELECT` , `WHERE` of in voorwaardelijke metriek.

**functies van het Koord**

| Functie | Voorbeeld | Details |
|---|---|---|
| [ Lager ](https://spark.apache.org/docs/latest/api/sql/index.html#lower) | ``SELECT LOWER(name) AS lower_name`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |

{style="table-layout:auto"}

**Datum-tijd functies**

| Functie | Voorbeeld | Details |
|---|---|---|
| [ Jaar ](https://spark.apache.org/docs/latest/api/sql/index.html#year) | ``SELECT YEAR(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [ Maand ](https://spark.apache.org/docs/latest/api/sql/index.html#month) | ``SELECT MONTH(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [ Dag ](https://spark.apache.org/docs/latest/api/sql/index.html#day) | ``SELECT DAY(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [ Dag van week ](https://spark.apache.org/docs/latest/api/sql/index.html#dayofweek) | ``SELECT DAYOFWEEK(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde omdat u het nummer en niet de vriendschappelijke naam nodig hebt. |
| [ Dag van jaar ](https://spark.apache.org/docs/latest/api/sql/index.html#dayofyear) | ``SELECT DAYOFYEAR(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [ Week ](https://spark.apache.org/docs/latest/api/sql/index.html#week) | ``SELECT WEEK(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [ Kwartaal ](https://spark.apache.org/docs/latest/api/sql/index.html#quarter) | ``SELECT QUARTER(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [ Uur ](https://spark.apache.org/docs/latest/api/sql/index.html#hour) | ``SELECT HOUR(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde omdat u het nummer en niet de vriendschappelijke naam nodig hebt. |
| [ Minuut ](https://spark.apache.org/docs/latest/api/sql/index.html#minute) | ``SELECT MINUTE(`timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. |
| [ trekken ](https://spark.apache.org/docs/latest/api/sql/index.html#extract) | ``SELECT EXTRACT(MONTH FROM `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde voor sommige onderdelen van deze functie omdat u het nummer nodig hebt en niet de vriendschappelijke naam.<br/> de gesteunde delen zijn:<br> - Trefwoorden: `YEAR`, `MONTH`, `DAYOFMONTH`, `DAYOFWEEK`, `DAYOFYEAR`, `WEEK`, `QUARTER`, `HOUR`, `MINUTE`.<br/> - Tekenreeksen: `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&#39;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'` of 19}.`'MINUTE'` |
| [ Datum (deel) ](https://spark.apache.org/docs/latest/api/sql/index.html#date_part) | ``SELECT DATE_PART('month', `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde voor sommige onderdelen van deze functie omdat u het nummer nodig hebt en niet de vriendschappelijke naam.<br/> Ondersteunde tekenreeksonderdelen zijn: `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&#39;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'`, of `'MINUTE'` . |
| [ Datum (beknot) ](https://spark.apache.org/docs/latest/api/sql/index.html#date_trunc) | ``SELECT DATE_TRUNC('quarter', `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven.<br/> Ondersteunde tekenreeksgranulariteit is: `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&#39;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'` of `'MINUTE'` . |

{style="table-layout:auto"}
