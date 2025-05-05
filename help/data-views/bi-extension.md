---
title: Customer Journey Analytics BI-extensie
description: Leer hoe u Power BI of Tableau Desktop kunt gebruiken om tot gegevensmeningen toegang te hebben gebruikend de uitbreiding van Customer Journey Analytics BI.
solution: Customer Journey Analytics
feature: BI Extension
role: Admin
exl-id: ab7e1f15-ead9-46b7-94b7-f81802f88ff5
source-git-commit: f03c82375a907821c8e3f40b32b4d4200a47323f
workflow-type: tm+mt
source-wordcount: '3188'
ht-degree: 0%

---

# Customer Journey Analytics BI-extensie

{{select-package}}

[!DNL Customer Journey Analytics BI extension] laat SQL toegang tot de [ gegevensmeningen ](./data-views.md) toe die u in Customer Journey Analytics hebt bepaald. Uw gegevensengineers en analisten zouden met Power BI, de Desktop van Tableau, of andere bedrijfsintelligentie en visualisatiehulpmiddelen (die verder als hulpmiddelen worden bedoeld BI) vertrouwd kunnen zijn. Ze kunnen nu rapporten en dashboards maken op basis van dezelfde gegevensweergaven die Customer Journey Analytics-gebruikers gebruiken bij het maken van hun Analysis Workspace-projecten.

De Dienst van de Vraag van Adobe Experience Platform [&#128279;](https://experienceleague.adobe.com/nl/docs/experience-platform/query/home) is de SQL interface aan gegevens beschikbaar in het gegevensmeer van Experience Platform. Als [!DNL Customer Journey Analytics BI extension] ingeschakeld is, wordt de functionaliteit van [!DNL Query Service] uitgebreid om uw Customer Journey Analytics-gegevensweergaven als tabellen of weergaven in een [!DNL Query Service] -sessie te zien. Dit betekent dat hulpprogramma&#39;s voor bedrijfsintelligentie die [!DNL Query Service] als hun PostgresSQL-interface gebruiken, naadloos van deze uitgebreide functionaliteit profiteren.

De belangrijkste voordelen zijn:

* Het is niet nodig om een gelijkwaardige weergave van Customer Journey Analytics-gegevensweergaven opnieuw te maken in het BI-gereedschap zelf. <br/> zie [ meningen van Gegevens ](data-views.md) voor meer informatie over de functionaliteit van gegevensmeningen om te begrijpen wat moet worden ontspannen.
* Meer consistentie in rapportage en analyse tussen BI-instrumenten en Customer Journey Analytics.
* Combineer Customer Journey Analytics-gegevens met andere gegevensbronnen die al beschikbaar zijn in BI-gereedschappen.

## Vereisten

Als u deze functionaliteit wilt gebruiken, kunt u verlopen of niet-verlopen referenties gebruiken om BI-gereedschappen te verbinden met de [!DNL Customer Journey Analytics BI extension] . De [ gids van Referenties ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/ui/credentials) verstrekt meer informatie bij het plaatsen van het verlopen van geloofsbrieven of niet-het verlopen geloofsbrieven.
Hieronder vindt u aanvullende stappen voor het instellen van CJA-machtigingen
<!---   Enable the [!UICONTROL Customer Journey Analytics BI extension] in your Experience Platform organization. -->

### Referenties vervallen

Als u verlopen referenties wilt gebruiken, kunt u:

* Toegang verlenen tot Experience Platform en Customer Journey Analytics.
* Bied productbeheerders toegang tot Customer Journey Analytics, zodat u verbindingen en gegevensweergaven kunt weergeven, bewerken, bijwerken of verwijderen.

U kunt ook:

* Bied toegang tot de gegevensweergaven die u wilt openen.
* Toegang verlenen tot de extensie Customer Journey Analytics BI.

### Niet-uitbreidende referenties

Niet-vervallende referenties gebruiken:

* Niet-vervallende gegevens maken in Experience Platform.
* De toegang van de subsidie tot de niet-vervallende geloofsbrieven door de stappen te volgen die in [ worden vermeld het Verlopen Referenties ](#Expiring-credentials).

Zie [ Controle van de Toegang van de Reis van de Klant ](../technotes/access-control.md) voor meer informatie, specifiek de [ extra toestemmingen van Admin van het Product ](../technotes/access-control.md#product-admin-additional-permissions) en [ de Toestemmingen van Customer Journey Analytics in Admin Console ](../technotes/access-control.md#customer-journey-analytics-permissions-in-admin-console).


## Gebruik

Als u de functie [!DNL Customer Journey Analytics BI extension] wilt gebruiken, kunt u SQL rechtstreeks gebruiken of de slepen en neerzetten-ervaring gebruiken die beschikbaar is in het specifieke gereedschap BI.

### SQL

U kunt de functionaliteit direct in SQL verklaringen gebruiken gebruikend of de Redacteur van de Vraag of een standaard bevel-lijn van PostgresSQL (CLI) cliënt.

+++ Query-editor

In Adobe Experience Platform:

1. Selecteer **[!UICONTROL ** Vragen **]** van **[!UICONTROL **&#x200B; GEGEVENSBEHEER &#x200B;**]** in het linkerspoor.

1. Selecteer ![ creëren Vraag ](assets/Smock_AddCircle_18_N.svg) **[!UICONTROL **&#x200B; vraag &#x200B;**]** creëren.

1. Selecteer de `cja` -database voor uw sandbox in de lijst met databases in de vervolgkeuzelijst **[!UICONTROL Database]** . Bijvoorbeeld `prod:cja` .

1. Om de vraag uit te voeren, typ uw SQL verklaring en selecteer ![ Spel ](assets/Smock_Play_18_N.svg) knoop (of druk `[SHIFT]` + `[ENTER]`).

+++


+++ PostgresSQL CLI

1. Zoek en kopieer uw PostgresSQL-referenties in Adobe Experience Platform:

   1. Selecteer **[!UICONTROL ** Vragen **]** van de linkerspoorlijn (onder **[!UICONTROL **&#x200B; GEGEVENSBEHEER &#x200B;**]**).

   1. Selecteer **[!UICONTROL **&#x200B; Referenties &#x200B;**]** van de hoogste bar.

   1. Selecteer de `cja` -database voor uw sandbox in de lijst met databases in de vervolgkeuzelijst **[!UICONTROL Database]** . Bijvoorbeeld `prod:cja` .

   1. Om het bevelkoord te kopiëren, gebruik ![ Exemplaar ](assets/Smock_Copy_18_N.svg) in de **[!UICONTROL **&#x200B; bevel PSQL &#x200B;**]** sectie.

1. Open een opdracht- of terminalvenster.

1. Als u zich wilt aanmelden en uw query&#39;s wilt uitvoeren, plakt u de opdrachttekenreeks in uw terminal.

+++

Zie de [ gids UI van de Redacteur van de Vraag ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/ui/user-guide) voor meer informatie.


### BI-gereedschappen

Momenteel wordt [!DNL Customer Journey Analytics BI extension] ondersteund en getest voor de hieronder vermelde gereedschappen. Andere hulpmiddelen van BI die de interface PSQL gebruiken zouden ook kunnen werken, maar officieel nog niet gesteund.

+++ Power BI

1. Bekijk de details van uw PostgresSQL geloofsbrieven in Adobe Experience Platform:

   1. Selecteer **[!UICONTROL ** Vragen **]** van de linkerspoorlijn (onder **[!UICONTROL **&#x200B; GEGEVENSBEHEER &#x200B;**]**).

   1. Selecteer **[!UICONTROL **&#x200B; Referenties &#x200B;**]** van de hoogste bar.

   1. Selecteer de `cja` -database voor uw sandbox in de lijst met databases in de vervolgkeuzelijst **[!UICONTROL Database]** . Bijvoorbeeld `prod:cja` .

   1. Gebruik ![ Exemplaar ](assets/Smock_Copy_18_N.svg) om elk van de parameters van de geloofsbrieven van Postgres ([!UICONTROL Host], [!UICONTROL Port], [!UICONTROL Database], [!UICONTROL Username], en anderen) te kopiëren wanneer nodig in Power BI.

1. In Power BI:

   1. In het belangrijkste venster, uitgezochte **[!UICONTROL **&#x200B; krijgt gegevens &#x200B;**]** van de hoogste toolbar.

   1. Selecteer **[!UICONTROL More...]** in het linkerspoor.

   1. In **krijgt het 1&rbrace; scherm van Gegevens &lbrace;, onderzoek naar `PostgresSQL` en selecteer het **[!UICONTROL **gegevensbestand PostgresSQL &#x200B;**]&#x200B;**van de lijst.**

   1. In het **[!UICONTROL **&#x200B; PostgressSQL- gegevensbestand &#x200B;**]** dialoog:

      1. Plak de **&#x200B;**&#x200B;parameter van de Gastheer **&#x200B;**&#x200B;van de Vragen van Experience Platform [!UICONTROL Credentials] op het **[!UICONTROL **&#x200B; de tekstgebied van de Server &#x200B;**]**.

      1. Plak de **&#x200B;**&#x200B;parameter van het Gegevensbestand **&#x200B;**&#x200B;{van de Vragen van Experience Platform [!UICONTROL Credentials] in het **[!UICONTROL **&#x200B; 4} tekstgebied van het Gegevensbestand &lbrace;.**]**

         Voeg `?FLATTEN` aan de **[!UICONTROL **&#x200B; 2&rbrace; parameter van het Gegevensbestand &lbrace;toe, zodat leest het als `prod:cja?FLATTEN` bijvoorbeeld. &#x200B;**]** Zie [ genestelde gegevensstructuren voor gebruik met de hulpmiddelen van derdeBI ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie afvlakken.

      1. Selecteer **[!UICONTROL DirectQuery]** wanneer hierom wordt gevraagd voor de modus **[!UICONTROL Data Connectivity]** .

      1. U wordt gevraagd om **[!UICONTROL Username]** en **[!UICONTROL Password]** . Gebruik de equivalente parameters van Experience Platform Queries [!UICONTROL Credentials] .


   1. Na succesvolle login, verschijnen de lijsten van de de gegevensmening van Customer Journey Analytics in de Navigator van Power BIs **[!UICONTROL **&#x200B; **]**.

   1. Selecteer de lijsten van de gegevensmening die u **[!UICONTROL **&#x200B; Lading &#x200B;**]** wilt gebruiken en selecteren.

   Alle dimensies en metriek die aan een of meer geselecteerde tabellen zijn gekoppeld, worden in het rechterdeelvenster weergegeven en kunnen in uw visualisaties worden gebruikt.

   Zie [ Power BI aan de Dienst van de Vraag ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/clients/power-bi) voor meer informatie verbinden. Zie ook [ de gebruiksgevallen van het de uitbreidingsgebruik van BI ](/help/use-cases/data-views/bi-extension-usecases.md) voor een gedetailleerd voorbeeld.

+++

+++Tableau-desktop

1. Bekijk de details van uw PostgresSQL geloofsbrieven in Adobe Experience Platform:

   1. Selecteer **[!UICONTROL ** Vragen **]** van de linkerspoorlijn (onder **[!UICONTROL **&#x200B; GEGEVENSBEHEER &#x200B;**]**).

   1. Selecteer **[!UICONTROL **&#x200B; Referenties &#x200B;**]** van de hoogste bar.

   1. Selecteer de `cja` -database voor uw sandbox in de lijst met databases in de vervolgkeuzelijst **[!UICONTROL Database]** . Bijvoorbeeld `prod:cja` .

   1. Gebruik ![ Exemplaar ](assets/Smock_Copy_18_N.svg) om elk van de geloofsbrieven van Postgres parameters ([!UICONTROL Host], [!UICONTROL Port], [!UICONTROL Database], [!UICONTROL Username], en anderen) te kopiëren wanneer nodig in de Desktop van Tableau.

1. In Tableau Desktop:

   1. Selecteer **[!UICONTROL ** Meer **]** van **[!UICONTROL **&#x200B; aan een Server &#x200B;**]** in het linkerspoor.

   1. Selecteer **[!UICONTROL **&#x200B; PostgresSQL &#x200B;**]** van de lijst.

   1. In het dialoogvenster [!UICONTROL PostgresSQL] :

      1. Plak de **&#x200B;**&#x200B;parameter van de Gastheer **&#x200B;**&#x200B;van de Vragen van Experience Platform [!UICONTROL Credentials] in het **[!UICONTROL **&#x200B; de tekstgebied van de Server &#x200B;**]**.

      1. Plak de **[!UICONTROL ** Poort **]** parameter van de Vragen van Experience Platform [!UICONTROL Credentials] in het **[!UICONTROL **&#x200B; Poort &#x200B;**]** tekstgebied.

      1. Plak de **&#x200B;**&#x200B;parameter van het Gegevensbestand **&#x200B;**&#x200B;{van de Vragen van Experience Platform [!UICONTROL Credentials] in het **[!UICONTROL **&#x200B; 4} tekstgebied van het Gegevensbestand &lbrace;.**]**

         Voeg `%3FFLATTEN` aan de **[!UICONTROL **&#x200B; 2&rbrace; parameter van het Gegevensbestand &lbrace;toe, zodat leest het als `prod:cja%3FFLATTEN` bijvoorbeeld. &#x200B;**]** Zie [ genestelde gegevensstructuren voor gebruik met de hulpmiddelen van derdeBI ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie afvlakken.

      1. Selecteer **[!UICONTROL ** Gebruikersnaam en Wachtwoord **]** van **[!UICONTROL **&#x200B; Authentificatie &#x200B;**]** lijst.

      1. Plak **[!UICONTROL ** Gebruikersnaam **]** parameter van de Vragen van Experience Platform [!UICONTROL Credentials] in **[!UICONTROL **&#x200B; Gebruikersnaam &#x200B;**]** tekstgebied.

      1. Plak de **[!UICONTROL ** parameter van het Wachtwoord **]** van de Vragen van Experience Platform [!UICONTROL Credentials] in het **[!UICONTROL **&#x200B; 4&rbrace; tekstgebied van het Wachtwoord.**]**

      1. Selecteer het **[!UICONTROL **&#x200B; Teken binnen &#x200B;**]**.

   1. De gegevensmeningen van Customer Journey Analytics verschijnen omhoog als lijsten in de **[!UICONTROL **&#x200B; Lijst &#x200B;**]** lijst.

   1. Sleep de tabellen die u op het canvas wilt gebruiken.

   U kunt nu met de gegevens van de lijsten van de gegevensmening werken om uw rapporten en visualisaties te bouwen.

   Zie [ Connect Tableau aan de Dienst van de Vraag ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/clients/tableau) voor meer informatie. Zie ook [ de gebruiksgevallen van het de uitbreidingsgebruik van BI ](/help/use-cases/data-views/bi-extension-usecases.md) voor een gedetailleerd voorbeeld.

+++

+++ Liniaal

1. Bekijk de details van uw PostgresSQL geloofsbrieven in Adobe Experience Platform:

   1. Selecteer **[!UICONTROL ** Vragen **]** van de linkerspoorlijn (onder **[!UICONTROL **&#x200B; GEGEVENSBEHEER &#x200B;**]**).

   1. Selecteer **[!UICONTROL **&#x200B; Referenties &#x200B;**]** van de hoogste bar.

   1. Selecteer de `cja` -database voor uw sandbox in de lijst met databases in de vervolgkeuzelijst **[!UICONTROL Database]** . Bijvoorbeeld `prod:cja` .

   1. Gebruik ![ Exemplaar ](assets/Smock_Copy_18_N.svg) om elk van de parameters van de geloofsbrieven van Postgres ([!UICONTROL Host], [!UICONTROL Port], [!UICONTROL Database], [!UICONTROL Username], en anderen) te kopiëren wanneer nodig in Leider.

1. Minder:

   1. Selecteer **[!UICONTROL Admin]** in het linkerspoor.
   1. Selecteer **[!UICONTROL Connections]** .
   1. Selecteer **[!UICONTROL Add Connection]** .
   1. Plak in het scherm **[!UICONTROL Connect your database to Looker]** de juiste waarden wanneer u de nieuwe verbinding instelt. Selecteer **[!UICONTROL PostgreSQL 9.5+]** als dialect.
   1. Selecteer **[!UICONTROL Test]** om de verbinding te testen.
   1. Wanneer succesvol, uitgezochte **[!UICONTROL Update]** om uw verbinding te bewaren.

   U kunt nu met de gegevens van de lijsten van de gegevensmening werken om uw rapporten en visualisaties te bouwen.

   Zie [ Drager aan de Dienst van de Vraag ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/clients/looker) voor meer informatie verbinden. Zie ook [ de gebruiksgevallen van het de uitbreidingsgebruik van BI ](/help/use-cases/data-views/bi-extension-usecases.md) voor een gedetailleerd voorbeeld.

+++

+++ Jupyter-notebook

1. Bekijk de details van uw PostgresSQL geloofsbrieven in Adobe Experience Platform:

   1. Selecteer **[!UICONTROL ** Vragen **]** van de linkerspoorlijn (onder **[!UICONTROL **&#x200B; GEGEVENSBEHEER &#x200B;**]**).

   1. Selecteer **[!UICONTROL **&#x200B; Referenties &#x200B;**]** van de hoogste bar.

   1. Selecteer de `cja` -database voor uw sandbox in de lijst met databases in de vervolgkeuzelijst **[!UICONTROL Database]** . Bijvoorbeeld `prod:cja` .

   1. Gebruik ![ Exemplaar ](assets/Smock_Copy_18_N.svg) om elk van de parameters van de geloofsbrieven van Postgres ([!UICONTROL Host], [!UICONTROL Port], [!UICONTROL Database], [!UICONTROL Username], en anderen) te kopiëren wanneer nodig in Notitie Jupyter.

1. In Jupyter-laptop:

   1. Zorg ervoor dat u de vereiste bibliotheken gebruikt.
   1. Gebruik de juiste waarden bij het instellen en uitvoeren van de verbinding.
   1. Test uw verbinding door een relevante query uit te voeren.

   Wanneer succesvol, kunt u met de gegevens werken om uw rapporten en visualisaties te bouwen.

   Zie [ Verbind Jupyter Notitieboekje aan de Dienst van de Vraag ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/clients/jupyter-notebook) voor meer informatie. Zie ook [ de gebruiksgevallen van het de uitbreidingsgebruik van BI ](/help/use-cases/data-views/bi-extension-usecases.md) voor een gedetailleerd voorbeeld.

+++

+++ RStudio

1. Bekijk de details van uw PostgresSQL geloofsbrieven in Adobe Experience Platform:

   1. Selecteer **[!UICONTROL ** Vragen **]** van de linkerspoorlijn (onder **[!UICONTROL **&#x200B; GEGEVENSBEHEER &#x200B;**]**).

   1. Selecteer **[!UICONTROL **&#x200B; Referenties &#x200B;**]** van de hoogste bar.

   1. Selecteer de `cja` -database voor uw sandbox in de lijst met databases in de vervolgkeuzelijst **[!UICONTROL Database]** . Bijvoorbeeld `prod:cja` .

   1. Gebruik ![ Exemplaar ](assets/Smock_Copy_18_N.svg) om elk van de parameters van de geloofsbrieven van Postgres ([!UICONTROL Host], [!UICONTROL Port], [!UICONTROL Database], [!UICONTROL Username], en anderen) te kopiëren wanneer nodig in Notitie Jupyter.

1. In RStudio:

   1. Zorg ervoor dat u de vereiste bibliotheken gebruikt.
   1. Gebruik de juiste waarden bij het instellen en uitvoeren van de verbinding.
   1. Test uw verbinding door een relevante query uit te voeren.

   Wanneer succesvol, kunt u met de gegevens werken om uw rapporten en visualisaties te bouwen.

   Zie [ Connect RStudio aan de Dienst van de Vraag ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/clients/rstudio) voor meer informatie. Zie ook [ BI het gebruiksgevallen van het uitbreidingsgebruik ](/help/use-cases/data-views/bi-extension-usecases.md) voor een gedetailleerd voorbeeld (dat in plaats daarvan het pakket RPostgres gebruikt).

+++

Zie [ cliënten met de Dienst van de Vraag ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/clients/overview) voor een overzicht van en meer informatie over de diverse beschikbare hulpmiddelen verbinden.

Zie [ gevallen van het Gebruik ](/help/use-cases/data-views/bi-extension-usecases.md) op hoe te om een aantal gebruiksgevallen te verwezenlijken gebruikend de uitbreiding van Customer Journey Analytics BI.

## Functionaliteit

Standaard hebben uw gegevensweergaven een tabelveilige naam die is gegenereerd op basis van hun vriendelijke naam. De gegevensweergave met de naam [!UICONTROL My Web Data View] heeft bijvoorbeeld de weergavenaam `my_web_data_view` . U kunt een voorkeursnaam definiëren voor gebruik in uw BI-gereedschap voor de gegevensweergave. Zie [ de meningsmontages van Gegevens ](create-dataview.md#settings) voor meer informatie.

Als u de ID&#39;s van de gegevensweergave wilt gebruiken als tabelnamen, kunt u de optionele instelling `CJA_USE_IDS` toevoegen aan de databasenaam wanneer u verbinding maakt. `prod:cja?CJA_USE_IDS` geeft bijvoorbeeld uw gegevensweergaven weer met namen als `dv_ABC123` .

### Datagovernance

De instellingen voor gegevensbeheer in Customer Journey Analytics zijn overgenomen van Adobe Experience Platform. Dankzij de integratie tussen Customer Journey Analytics en Adobe Experience Platform Data Governance kunnen gevoelige gegevens van Customer Journey Analytics worden geëtiketteerd en kan het privacybeleid worden gehandhaafd.

De etiketten en het beleid van de privacy die op datasets werden gecreeerd die door Experience Platform worden verbruikt kunnen in het werkschema van de gegevensmeningen van Customer Journey Analytics worden aangeschept. Daarom geven gegevens die met [!DNL Customer Journey Analytics BI extension] worden gevraagd, passende waarschuwingen of fouten weer wanneer ze niet voldoen aan de gedefinieerde privacylabels en beleidsregels.

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

Standaard gebruikt het schema van uw gegevensweergaven geneste structuren, net als de oorspronkelijke XDM-schema&#39;s. De integratie ondersteunt ook de optie `FLATTEN` . Met deze optie kunt u afvlakken forceren van het schema voor de gegevensweergaven (en elke andere tabel in de sessie). Het afvlakken staat voor gemakkelijker gebruik in de hulpmiddelen van BI toe die geen gestructureerde schema&#39;s steunen. Zie [ Werkend met genestelde gegevensstructuren in de Dienst van de Vraag ](https://experienceleague.adobe.com/nl/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie.


### Standaardwaarden en beperkingen

De volgende extra standaardwaarden en beperkingen zijn van toepassing wanneer u de extensie BI gebruikt:

* De extensie BI vereist een rijlimiet voor de resultaten van de query. De standaardwaarde is 50, maar u kunt dit overschrijven in SQL met behulp van `LIMIT n` , waarbij `n` 1 - 50000 is.
* De extensie BI vereist een datumbereik om de rijen voor berekeningen te beperken. De standaardwaarde is de laatste 30 dagen, maar u kunt dit in uw SQL `WHERE` -component overschrijven met behulp van de speciale [`timestamp`](#timestamp) - of [`daterange`](#date-range) -kolommen.
* Voor de extensie BI zijn samengevoegde query&#39;s vereist. U kunt SQL niet gebruiken zoals `SELECT * FROM ...` om de ruwe, onderliggende rijen te krijgen. Op een hoog niveau, zouden uw gezamenlijke vragen moeten gebruiken:
   * Selecteer totalen met `SUM` en/of `COUNT` .<br/> Bijvoorbeeld `SELECT SUM(metric1), COUNT(*) FROM ...`
   * Selecteer metriek uitgesplitst op een afmeting. <br/> Bijvoorbeeld, `SELECT dimension1, SUM(metric1), COUNT(*) FROM ... GROUP BY dimension1`
   * Selecteer duidelijke metrische waarden.<br/> Bijvoorbeeld, `SELECT DISTINCT dimension1 FROM ...`

     Zie voor meer details [ Ondersteunde SQL ](#supported-sql).


### Ondersteunde SQL

Zie {SQL van de Dienst van de Vraag 1} voor de volledige verwijzing op welk type van SQL wordt gesteund.[&#128279;](https://experienceleague.adobe.com/nl/docs/experience-platform/query/sql/overview)

Zie de onderstaande tabel voor voorbeelden van de SQL die u kunt gebruiken.

+++ Voorbeelden

<table style="table-layout:auto">
    <thead>
        <tr>
            <th>Patroon</th>
            <th>Voorbeeld</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Schema-detectie </td>
            <td>
                <pre><code>SELECT * FROM dv1 WHERE 1=0</code></pre>
            </td>
        </tr>
        <tr>
            <td>Geschikt of uitgesplitst </td>
            <td>
                <pre><code>SELECT dim1, SUM(metric1) AS m1
FROM dv1
WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02'
GROUP BY dim1</code></pre>
                <pre><code>SELECT dim1, SUM(metric1) AS m1
FROM dv1
WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02' AND
  filterId = '12345'
GROUP BY dim1</code></pre>
                <pre><code>SELECT dim1, SUM(metric1) AS m1
FROM dv1
WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02' AND
  AND (dim2 = 'A' OR dim3 IN ('X', 'Y', 'Z'))
GROUP BY dim1</code></pre>
            </td>
        </tr>
        <tr>
            <td><code>HAVING</code> clausule </td>
            <td>
                <pre><code>SELECT dim1, SUM(metric1) AS m1
FROM dv1
WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02'
GROUP BY dim1
HAVING m1 > 100</code></pre>
            </td>
        </tr>
        <tr>
            <td>Onderscheiden, boven 
dimensiewaarden </td>
            <td>
                <pre><code>SELECT DISTINCT dim1 FROM dv1</code></pre>
                <pre><code>SELECT dim1 AS dv1
FROM dv1
WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02'
GROUP BY dim1</code></pre>
                <pre><code>SELECT dim1 AS dv1
FROM dv1
WHERE `timestamp` >= '2022-01-01' AND `timestamp` < '2022-01-02'
GROUP BY dim1
ORDER BY SUM(metric1)
LIMIT 15</code></pre>
            </td>
        </tr>
        <tr>
            <td>Metrische totalen </td>
            <td>
                <pre><code>SELECT SUM(metric1) AS m1
FROM dv1
WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02'</code></pre>
            </td>
        </tr>
        <tr>
            <td>Meerdere dimensies
uitsplitsingen
en toponderscheidingen </td>
            <td>
                <pre><code>SELECT dim1, dim2, SUM(metric1) AS m1
FROM dv1
WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02'
GROUP BY dim1, dim2</code></pre>
                <pre><code>SELECT dim1, dim2, SUM(metric1) AS m1
FROM dv1
WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02'
GROUP BY 1, 2
ORDER BY 1, 2</code></pre>
                <pre><code>SELECT DISTINCT dim1, dim2
FROM dv1</code></pre>
            </td>
        </tr>
        <tr>
            <td>Subselectie maken:
Aanvullende filters
resultaten </td>
            <td>
                <pre><code>SELECT dim1, m1
FROM (
  SELECT dim1, SUM(metric1) AS m1
  FROM dv1
  WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02'</br>  GROEP OP DIm1
)
WAAR grijs 1 in ('A', 'B')</code></pre>
            </td>
        </tr>
        <tr>
            <td>Subselectie maken:
Doorheen zoeken
gegevensweergaven </td>
            <td>
                <pre><code>SELECT key, SUM(m1) AS total
FROM (
  SELECT dim1 AS key, SUM(metric1) AS m1
  FROM dv1
  WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02'
  GROUP BY dim1
<br>
  UNION
<br>
  SELECT dim2 AS key, SUM(m1) AS m1
  FROM dv2
  WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02'
  GROUP BY dim2
)
GROUP BY key
ORDER BY total</code></pre>
            </td>
        </tr>
        <tr>
            <td>Subselectie maken: 
Gelaagde bron, 
filteren, 
en aggregatie </td>
            <td>Gelaagd met subselecties:
<pre><code>SELECT rows.dim1, SUM(rows.m1) AS total
FROM (
  SELECT _.dim1,_.m1
  FROM (
    SELECT * FROM dv1
    WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02'
  ) _
  WHERE _.dim1 in ('A', 'B', 'C')
) rows
GROUP BY 1
ORDER BY total</code></pre>
Lagen met CTE:
<pre><code>WITH rows AS (
  WITH _ AS (
    SELECT * FROM data_ares
    WHERE `timestamp` BETWEEN '2021-01-01' AND '2021-02-01'
  )
  SELECT _.item, _.units FROM _
  WHERE _.item IS NOT NULL
)
SELECT rows.item, SUM(rows.units) AS units
FROM rows WHERE rows.item in ('A', 'B', 'C')
GROUP BY rows.item</code></pre>
        </td>
        </tr>
        <tr>
            <td>Hiermee selecteert u waar de
metriek komt voor
 of worden gemengd met
de afmetingen </td>
            <td>
                <pre><code>SELECT SUM(metric1) AS m1, dim1
FROM dv1
WHERE `timestamp` BETWEEN '2022-01-01' AND '2022-01-02'
GROUP BY 2</code></pre>
            </td>
        </tr>
    </tbody>
</table>

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

U kunt een `IF` - of `CASE` -component insluiten in de `SUM` - of `COUNT` -functies om extra segmentering toe te voegen die specifiek is voor een geselecteerde metrische waarde. Het toevoegen van deze clausules is gelijkaardig aan het toepassen van een segment op een metrische kolom in een het rapportlijst van Workspace.

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

Het tijdstempelbereik wordt geconverteerd naar een algemeen segment met datumbereik in het RankedRequest.
Het tijdstempelveld kan ook worden gebruikt in datum-/tijdfuncties om de tijdstempel van de gebeurtenis te parseren of af te kappen.

#### Datumbereik

De speciale kolom van `daterange` werkt ongeveer zoals in `timestamp` . Het segmenteren is echter beperkt tot volledige dagen. `daterange` is ook optioneel en heeft dezelfde standaardwaarden voor het bereik als `timestamp` .
Het veld `daterange` kan ook worden gebruikt in datum-/tijdfuncties om de gebeurtenisdatum te parseren of af te kappen.

De speciale kolom van `daterangeName` kan worden gebruikt om uw vraag te segmenteren gebruikend een genoemde datumwaaier zoals `Last Quarter`.

>[!NOTE]
>
>Power BI biedt geen ondersteuning voor `daterange` -meetwaarden die minder dan een dag zijn (uur, 30 minuten, 5 minuten, enzovoort).
>

#### Segment-id

De speciale kolom `filterId` is optioneel en wordt gebruikt om een extern gedefinieerd segment toe te passen op de query. Het toepassen van een extern gedefinieerd segment op een query lijkt op het slepen van een segment in een deelvenster in Workspace. U kunt meerdere segment-id&#39;s gebruiken door ze `AND` te laten omgaan.

Samen met `filterId` kunt u `filterName` gebruiken om de naam van een segment te gebruiken in plaats van de id.

### Indien clausule

De component `WHERE` wordt in drie stappen afgehandeld:

1. Zoek het datumbereik in de speciale velden `timestamp` , `daterange` of `daterangeName` .

1. Zoek om het even welke extern gedefiniëerde `filterId` s of `filterName` s om in het segment te omvatten.

1. Zet de resterende expressies om in ad-hocsegmenten.

De afhandeling wordt uitgevoerd door het eerste niveau van `AND` s in de `WHERE` -component te parseren. Elke `AND` -ed-expressie op het hoogste niveau moet overeenkomen met een van de bovenstaande expressies. Om het even wat dieper dan het eerste niveau van `AND` s, of, als de `WHERE` clausule `OR` op het hoogste niveau gebruikt, wordt behandeld als ad hoc segment.

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

### Dimension-functieondersteuning

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
| [ trekken ](https://spark.apache.org/docs/latest/api/sql/index.html#extract) | ``SELECT EXTRACT(MONTH FROM `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde voor sommige onderdelen van deze functie omdat u het nummer nodig hebt en niet de vriendschappelijke naam.<br/> de gesteunde delen zijn:<br> - Trefwoorden: `YEAR`, `MONTH`, `DAYOFMONTH`, `DAYOFWEEK`, `DAYOFYEAR`, `WEEK`, `QUARTER`, `HOUR`, `MINUTE`.<br/> - Tekenreeksen: `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&#39;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'` of 19&rbrace;.`'MINUTE'` |
| [ Datum (deel) ](https://spark.apache.org/docs/latest/api/sql/index.html#date_part) | ``SELECT DATE_PART('month', `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven. Gebruik de item-id in plaats van de waarde voor sommige onderdelen van deze functie omdat u het nummer nodig hebt en niet de vriendschappelijke naam.<br/> Ondersteunde tekenreeksonderdelen zijn: `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&#39;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'`, of `'MINUTE'` . |
| [ Datum (beknot) ](https://spark.apache.org/docs/latest/api/sql/index.html#date_trunc) | ``SELECT DATE_TRUNC('quarter', `timestamp`)`` | Genereer een dynamische dimensie-id op het veld dat wordt doorgegeven.<br/> Ondersteunde tekenreeksgranulariteit is: `'YEAR'`, `'Y'`, `'MONTH'`, `'M'`, `'DAYOFMONTH'`, `'DAY'`, `'D'`, `'DAYOFWEEK'`, `'DOW'`, `'DAYOFYEAR'`, `'DOY'`, `'WEEK'`, `'WOY`&#39;, `'W'`, `'QUARTER'`, `'QOY'`, `'Q'`, `'HOUR'` of `'MINUTE'` . |

{style="table-layout:auto"}

### Gedeeltelijke ondersteuning

Sommige SQL-functionaliteit wordt slechts gedeeltelijk ondersteund met de BI-extensie en retourneert niet dezelfde resultaten als bij andere databases.  Deze specifieke functionaliteit wordt gebruikt in SQL die door diverse hulpmiddelen van BI wordt geproduceerd, waarvoor de uitbreiding van BI geen nauwkeurige gelijke heeft. Dientengevolge, concentreert de uitbreiding van BI zich op een beperkte implementatie die het minimumgebruik van het hulpmiddel van BI zonder fouten te werpen behandelt. Zie de onderstaande tabel voor meer informatie.

| Functie | Voorbeeld | Details |
|---|---|---|
| MIN() &amp; MAX() | ``MIN(daterange)`` of <br/> ``MAX(daterange)`` | `MIN()` on `timestamp` , `daterange` of een van de `daterangeX` like `daterangeday` retourneert twee jaar geleden. <br/><br/> `MAX()` on `timestamp` , `daterange` of een van de `daterangeX` like `daterangeday` retourneert de huidige datum/tijd.<br/><br/>`MIN()` of `MAX()` op een andere dimensie, metrische waarde of expressie retourneert 0. |

{style="table-layout:auto"}
