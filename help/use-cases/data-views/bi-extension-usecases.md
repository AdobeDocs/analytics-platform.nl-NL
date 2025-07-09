---
title: Gebruik gevallen voor de extensie BI in Customer Journey Analytics
description: Meerdere gebruiksgevallen die laten zien hoe de BI-extensie in verschillende BI-gereedschappen in Customer Journey Analytics wordt gebruikt
solution: Customer Journey Analytics
feature: Data Views
role: User
exl-id: 3d1e3b79-402d-44ff-86b3-be9fd5494e19
source-git-commit: 4b3effffe944df9aaf473c27acc5b2260acbb753
workflow-type: tm+mt
source-wordcount: '11008'
ht-degree: 0%

---

# Gebruikskwesties voor extensie BI

In dit artikel wordt beschreven hoe u een aantal gebruiksgevallen kunt uitvoeren met de Customer Journey Analytics BI-extensie. In elke gebruikszaak wordt de Customer Journey Analytics-functionaliteit beschreven, gevolgd door details voor elk van de ondersteunde BI-gereedschappen:

* **Desktop van Power BI**. De gebruikte versie is 2.137.1102.0 64-bits (oktober 2024).
* **Desktop van Tableau**. De gebruikte versie is 2024.1.5 (20241.24.0705.0334) 64-bits.
* **Leider**. Online versie 25.0.23, beschikbaar door [ looker.com ](https://looker.com)
* **Jupyter Notitieboekje**. De gebruikte versie is 7.3.2.
* **RStudio**. De gebruikte versie is 2024.12.0, build 467.

De volgende gebruiksgevallen worden gedocumenteerd:

* **verbind**
   * [Weergaven van Connect- en lijstgegevens](#connect-and-validate)

* **Rapport en analyseer**
   * [Dagelijkse trend](#daily-trend)
   * [Uurtrend](#hourly-trend)
   * [Maandelijkse trend](#monthly-trend)
   * [Eén dimensie, gerangschikt](#single-dimension-ranked)
   * [Meerdere dimensies gerangschikt](#multiple-dimension-ranked)
   * [Waarden voor verschillende dimensies tellen](#count-distinct-dimension-values)
   * [Namen van datumbereik gebruiken om te filteren](#use-date-range-names-to-filter)
   * [Segmentnamen gebruiken](#use-segment-names-to-segment)
   * [Dimensiewaarden gebruiken om te segmenteren](#use-dimension-values-to-segment)
   * [Sorteren](#sort)
   * [Limieten](#limits)

* **Begrijp**

   * [Transformaties](#transformations)
   * [Visualisaties](#visualizations)
   * [Caveats](#caveats)

Het **verbindt** gebruiksgeval concentreert zich op hoe te om de hulpmiddelen van BI te verbinden gebruikend de uitbreiding van Customer Journey Analytics BI.

Het **rapport en de analyse** gebruiksgevallen instrueren hoe te om gelijkaardige Customer Journey Analytics visualisaties in de momenteel gesteunde hulpmiddelen van BI te verwezenlijken.

**begrijpt** gebruiksgevallen meer details op verstrekken:

* Transformaties die voorkomen wanneer u een hulpmiddel van BI gebruikt om te melden en te analyseren.
* Overeenkomsten en verschillen in visualisatie tussen Customer Journey Analytics- en BI-gereedschappen.
* Voorzie van elk van de hulpmiddelen van BI u zou moeten op de hoogte zijn.


## Verbinding maken en valideren

Met deze gebruiksaanwijzing stelt u de verbinding van het gereedschap BI naar Customer Journey Analytics in, geeft u de beschikbare gegevensweergaven weer en selecteert u een gegevensweergave die u wilt gebruiken.

+++ Customer Journey Analytics

De instructies verwijzen naar een voorbeeldomgeving met de volgende objecten:

* Gegevensweergave: **[!UICONTROL C&C - Data View]** 🅐 .
* Dimensies: **[!UICONTROL Product Name]** 🅑 en **[!UICONTROL Product Category]** 🅒 .
* Metrisch: **[!UICONTROL Purchase Revenue]** 🅓 en **[!UICONTROL Purchases]** 🅔 .
* Filter: **[!UICONTROL Fishing Products]** 🅕 .

![ de opstelling van de Basis van Customer Journey Analytics ](assets/cja-base.png)

Wanneer u de gebruiksgevallen doorloopt, vervangt u deze voorbeeldobjecten door objecten die geschikt zijn voor uw specifieke omgeving.

+++

+++ BI-gereedschappen

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. Open de vereiste referenties en parameters via de gebruikersinterface van de Experience Platform Query Service.

   1. Navigeer naar uw Experience Platform-sandbox.
   1. Selecteer ![ Vragen ](/help/assets/icons/DataSearch.svg) **[!UICONTROL Queries]** van het linkerspoor.
   1. Selecteer de tab **[!UICONTROL Credentials]** in de interface van **[!UICONTROL Queries]** .
   1. Selecteer `prod:cja` in de vervolgkeuzelijst **[!UICONTROL Database]** .

      ![ de dienstgeloofsbrieven van de Vraag ](assets/queryservice-credentials.png)

1. Start Power BI Desktop.
   1. Selecteer **[!UICONTROL Get data from other sources]** in de hoofdinterface.
   1. In het dialoogvenster **[!UICONTROL Get Data]** :
      ![ gegevensbestand PowerBI PostgreSQL ](assets/powerbi-postgresql.png)
      1. Zoek en selecteer **[!UICONTROL PostgreSQL database]** .
      1. Selecteer **[!UICONTROL Connect]** .
   1. In het dialoogvenster **[!UICONTROL PostgreSQL database]** :
      ![ de Server en montages van het Gegevensbestand van de Desktop PowerBI ](assets/powerbi-serverdatabase.png)
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om de **[!UICONTROL Host]** en **[!UICONTROL Port]** waarden van het paneel van Experience Platform **[!UICONTROL Query]** te kopiëren en te kleven **[!UICONTROL Expiring Credentials]**, die door `:` als waarde voor **[!UICONTROL Server]** wordt gescheiden. Bijvoorbeeld: `examplecompany.platform-query.adobe.io:80` .
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om de **[!UICONTROL Database]** waarde van het Experience Platform **[!UICONTROL Query]** **[!UICONTROL Expiring Credentials]** paneel te kopiëren en te kleven. Voeg `?FLATTEN` toe aan de waarde die u plakt. Bijvoorbeeld `prod:cja?FLATTEN` .
      1. Selecteer **[!UICONTROL DirectQuery]** als de **[!UICONTROL Data connectivity mode]** .
      1. Selecteer **[!UICONTROL OK]** .
   1. In het dialoogvenster **[!UICONTROL PostgreSQL database]** - **[!UICONTROL Database]** :
      ![ Gebruiker en Wachtwoord van de Desktop PowerBI ](assets/powerbi-userpassword.png)
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om de **[!UICONTROL Username]** en **[!UICONTROL Password]** waarden van het Experience Platform **[!UICONTROL Query]** te kopiëren **[!UICONTROL Expiring Credentials]** paneel in **[!UICONTROL User name]** en **[!UICONTROL Password]** gebieden. Als u a [ niet-uitbreidende credentie ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/credentials?lang=en#use-credential-to-connect) gebruikt, gebruik het wachtwoord van uw niet-uitbreidende referentie.
      1. Zorg ervoor dat het vervolgkeuzemenu voor **[!UICONTROL Select which level to apply these settings to]** is ingesteld op de **[!UICONTROL Server]** die u eerder hebt gedefinieerd.
      1. Selecteer **[!UICONTROL Connect]** .
   1. In het dialoogvenster **[!UICONTROL Navigator]** worden de gegevensweergaven opgehaald. Dit kan enige tijd duren. Zodra teruggewonnen, ziet u het volgende in de Desktop van Power BI.
      ![ de Gegevens van de Lading van de Desktop van Power BI ](assets/powerbi-navigator-load.png)
      1. Selecteer **[!UICONTROL public.cc_data_view]** in de lijst in het linkerdeelvenster.
      1. U hebt twee opties:
         1. Selecteer **[!UICONTROL Load]** om door te gaan en de installatie te voltooien.
         1. Selecteer **[!UICONTROL Transform Data]** . Er wordt een dialoogvenster weergegeven waarin u desgewenst transformaties kunt toepassen als onderdeel van de configuratie.
            ![ Gegevens van de Transformatie van de Desktop van Power BI ](assets/powerbi-transform-data.png)
            * Selecteer **[!UICONTROL Close & Apply]** .
   1. Na enige tijd wordt **[!UICONTROL public.cc_data_view]** weergegeven in het deelvenster **[!UICONTROL Data]** . Selecteer ![ ChevronRight ](/help/assets/icons/ChevronRight.svg) om afmetingen en metriek te tonen.
      ![ Gegevens van de Server van de Desktop van Power BI geladen ](assets/powerbi-navigator-loaded.png)


### Naar FLATTEN of niet

Power BI Desktop ondersteunt de volgende scenario&#39;s voor de parameter `FLATTEN` . Zie [ genestelde gegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie afvlakken.

| FLATTEN, parameter | Voorbeeld | Ondersteund | Opmerkingen |
|---|---|:---:|---|
| Geen | `prod:cja` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | |
| `?FLATTEN` | `prod:cja?FLATTEN` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | **geadviseerde optie om te gebruiken!** |
| `%3FFLATTEN` | `prod:cja%3FFLATTEN` | ![ CloseCircle ](/help/assets/icons/CloseCircle.svg) | Fout in weergave Power BI Desktop: **[!UICONTROL We couldn't authenticate with the credentials provided. Please try again.]** |

### Meer informatie

* [Vereisten](/help/data-views/bi-extension.md#prerequisites)
* [ gids van Geloofsbrieven ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/credentials)
* [ verbind Power BI met de Dienst van de Vraag ](https://experienceleague.adobe.com/en/docs/experience-platform/query/clients/power-bi).




>[!TAB  Desktop Tableau ]

1. Open de vereiste referenties en parameters via de gebruikersinterface van de Experience Platform Query Service.

   1. Navigeer naar uw Experience Platform-sandbox.
   1. Selecteer ![ Vragen ](/help/assets/icons/DataSearch.svg) **[!UICONTROL Queries]** van het linkerspoor.
   1. Selecteer de tab **[!UICONTROL Credentials]** in de interface van **[!UICONTROL Queries]** .
   1. Selecteer `prod:cja` in de vervolgkeuzelijst **[!UICONTROL Database]** .

      ![ de dienstgeloofsbrieven van de Vraag ](assets/queryservice-credentials.png)

1. Start Tableau.
   1. Selecteer **[!UICONTROL PostgreSQL]** in de linkertrack onder **[!UICONTROL To a Server]** . Als deze optie niet beschikbaar is, selecteert u **[!UICONTROL More...]** en selecteert u **[!UICONTROL PostgreSQL]** in het menu **[!UICONTROL Installed Connectors]** .
      ![ Verbindingen van Tableau ](assets/tableau-connectors.png)
   1. Ga in het dialoogvenster **[!UICONTROL PostgreSQL]** op het tabblad **[!UICONTROL General]** naar:
      ![ Teken van Tableau binnen dialoog ](assets/tableau-signin.png)
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om **[!UICONTROL Host]** van het paneel van Experience Platform **[!UICONTROL Query]** te kopiëren en te kleven **[!UICONTROL Expiring Credentials]** aan **[!UICONTROL Server]**.
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om **[!UICONTROL Port]** van het paneel van Experience Platform **[!UICONTROL Query]** te kopiëren en te kleven **[!UICONTROL Expiring Credentials]** aan **[!UICONTROL Port]**.
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om **[!UICONTROL Database]** van het paneel van Experience Platform **[!UICONTROL Query]** te kopiëren en te kleven **[!UICONTROL Expiring Credentials]** aan **[!UICONTROL Database]**. Voeg `%3FFLATTEN` toe aan de waarde die u plakt. Bijvoorbeeld: `prod:cja%3FFLATTEN` .
      1. Selecteer **[!UICONTROL Username and Password]** in de vervolgkeuzelijst **[!UICONTROL Authentication]** .
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om **[!UICONTROL Username]** van het paneel van Experience Platform **[!UICONTROL Query]** te kopiëren en te kleven **[!UICONTROL Expiring Credentials]** aan **[!UICONTROL Username]**.
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om **[!UICONTROL Password]** van het paneel van Experience Platform **[!UICONTROL Query]** te kopiëren en te kleven **[!UICONTROL Expiring Credentials]** aan **[!UICONTROL Password]**. Als u a [ niet-uitbreidende credentie ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/credentials?lang=en#use-credential-to-connect) gebruikt, gebruik het wachtwoord van uw niet-uitbreidende referentie.
      1. Controleer of **[!UICONTROL Require SSL]** is ingeschakeld.
      1. Selecteer **[!UICONTROL Sign In]** .

      U ziet een dialoogvenster **[!UICONTROL Progressing Request]** terwijl Tableau Desktop de verbinding valideert.
   1. In het hoofdvenster ziet u op de pagina **[!UICONTROL Data Source]** in het linkervenster:
      * De naam van de verbinding, onder **[!UICONTROL Connections]** .
      * De naam van de database, onder **[!UICONTROL Database]** .
      * Een lijst met tabellen, onder **[!UICONTROL Table]** .
        ![ Verbonden Tableau ](assets/tableau-connected.png)
      1. Sleep het item **[!UICONTROL cc_data_view]** en zet het neer in de hoofdweergave die **[!UICONTROL Drag tables]** hier leest.
   1. In het hoofdvenster worden de details van de gegevensweergave van **[!UICONTROL cc_data_view]** weergegeven.
      ![ Verbonden Tableau ](assets/tableau-validation.png)

### Naar FLATTEN of niet

Tableau Desktop ondersteunt de volgende scenario&#39;s voor de parameter `FLATTEN` . Zie [ genestelde gegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie afvlakken.

| FLATTEN, parameter | Voorbeeld | Ondersteund | Opmerkingen |
|---|---|:---:|---|
| Geen | `prod:cja` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | |
| `?FLATTEN` | `prod:cja?FLATTEN` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | |
| `%3FFLATTEN` | `prod:cja%3FFLATTEN` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | **geadviseerde optie om** te gebruiken. Opmerking: `%3FFLATTEN` is een URL-gecodeerde versie van `?FLATTEN` . |

### Meer informatie

* [Vereisten](/help/data-views/bi-extension.md#prerequisites)
* [ gids van Geloofsbrieven ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/credentials)
* [ verbind de Desktop van Tableau aan de Dienst van de Vraag ](https://experienceleague.adobe.com/en/docs/experience-platform/query/clients/tableau).


>[!TAB  Leider ]

1. Open de vereiste referenties en parameters via de gebruikersinterface van de Experience Platform Query Service.

   1. Navigeer naar uw Experience Platform-sandbox.
   1. Selecteer ![ Vragen ](/help/assets/icons/DataSearch.svg) **[!UICONTROL Queries]** van het linkerspoor.
   1. Selecteer de tab **[!UICONTROL Credentials]** in de interface van **[!UICONTROL Queries]** .
   1. Selecteer `prod:cja` in de vervolgkeuzelijst **[!UICONTROL Database]** .

      ![ de dienstgeloofsbrieven van de Vraag ](assets/queryservice-credentials.png)

1. Aanmelden bij Looker

   1. Selecteer **[!UICONTROL Admin]** in het linkerspoor.
   1. Selecteer **[!UICONTROL Connections]** .
   1. Selecteer **[!UICONTROL Add Connection]** .
   1. In de lus **[!UICONTROL Connect your database to Looker screen]** .

      ![ Leider verbindt met gegevensbestand ](assets/looker-connect.png)

      1. Voer een **[!UICONTROL Name]** in voor uw verbinding, bijvoorbeeld `Example Looker Connection` .
      1. Zorg ervoor dat **[!UICONTROL All Projects]** is geselecteerd als de **[!UICONTROL Connection Scope]** .
      1. Selecteer **[!UICONTROL PostgreSQL 9.5+]** als Dialect.
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om de **[!UICONTROL Host]** waarde van het paneel van Experience Platform **[!UICONTROL Query]** te kopiëren en te kleven **[!UICONTROL Expiring Credentials]**, als waarde voor **[!UICONTROL Host]**. Bijvoorbeeld: `examplecompany.platform-query.adobe.io` .
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om de **[!UICONTROL Port]** waarde van het paneel van Experience Platform **[!UICONTROL Query]** te kopiëren en te kleven **[!UICONTROL Expiring Credentials]**, als waarde voor **[!UICONTROL Port]**. Bijvoorbeeld: `80` .
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om de **[!UICONTROL Database]** waarde van het Experience Platform **[!UICONTROL Query]** **[!UICONTROL Expiring Credentials]** paneel als waarde voor **[!UICONTROL Database]** te kopiëren en te kleven. Voeg `%3FFLATTEN` toe aan de waarde die u plakt. Bijvoorbeeld `prod:cja%3FFLATTEN` .
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om de **[!UICONTROL Username]** waarde van het Experience Platform **[!UICONTROL Query]** **[!UICONTROL Expiring Credentials]** paneel als waarde voor **[!UICONTROL Username]** te kopiëren en te kleven.
      1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om de **[!UICONTROL Password]** waarde van het Experience Platform **[!UICONTROL Query]** **[!UICONTROL Expiring Credentials]** paneel als waarde voor **[!UICONTROL Password]** te kopiëren en te kleven.
      1. Selecteer **[!UICONTROL Expand all]** bij **[!UICONTROL Optional Settings]** .
      1. Stel **[!UICONTROL Max connections]** per knooppunt in op `5` .
      1. Controleer of **[!UICONTROL SSL]** is ingeschakeld.
      1. Selecteer **[!UICONTROL Test]** om de verbinding te testen. U ziet dat een banner boven aan het scherm wordt weergegeven met een bericht als **[!UICONTROL Success, can connect JDBC ....]** .
      1. Selecteer **[!UICONTROL Connect]** om de verbinding tot stand te brengen en op te slaan.
   1. De nieuwe verbinding wordt weergegeven in de interface **[!UICONTROL Connections]** .
   1. Selecteer **←** in **[!UICONTROL Admin]** om naar de hoofdnavigatie in de linkertrack te gaan.
   1. Selecteer **[!UICONTROL Develop]** .
   1. Selecteer **[!UICONTROL Projects]** .
   1. Selecteer **[!UICONTROL New Model]** in projecten LookML.
   1. Om ervoor te zorgen dat u geen invloed hebt op andere gebruikers. Selecteer Modus voor ontwikkeling openen als u hierom wordt gevraagd.
   1. In de **[!UICONTROL Create Model]** -ervaring:
      1. In **[!UICONTROL ➊ Select Database Connection]**:
         1. Selecteer uw databaseverbinding in **[!UICONTROL Select database connection]** . Bijvoorbeeld: **[!UICONTROL example_looker_connection]** .
         1. Geef uw project een naam in **[!UICONTROL Create a new LookML Project for this model]** . Voor `example: example_looker_project` .
         1. Selecteer **[!UICONTROL Next]** .
      1. In **[!UICONTROL ➋ Select Tables]**:
         1. Selecteer **[!UICONTROL public]** en zorg ervoor dat de Customer Journey Analytics-gegevensweergave is geselecteerd. Bijvoorbeeld: ![ SelectBox ](/help/assets/icons/SelectBox.svg) **[!UICONTROL cc_data_view]**.
         1. Selecteer **[!UICONTROL Next]** .
      1. In **[!UICONTROL ➌ Select Primary Keys]**:
         1. Selecteer **[!UICONTROL Next]** .
      1. In **[!UICONTROL ➍ Select Explores to Create]**:
         1. Zorg ervoor dat u de weergave selecteert. Bijvoorbeeld: **[!UICONTROL cc_data_view.view]** .
         1. Selecteer **[!UICONTROL Next]** .
      1. In **[!UICONTROL ➎ Enter Model Name]**:
         1. Geef het model een naam. Bijvoorbeeld: `example_looker_model` .
      1. Selecteer **[!UICONTROL Complete and Explore Data]** .

   U wordt omgeleid naar de **[!UICONTROL Explore]** interface van Looker, klaar om de gegevens te onderzoeken.



### Naar FLATTEN of niet

De markering ondersteunt de volgende scenario&#39;s voor de parameter `FLATTEN` . Zie [ genestelde gegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie afvlakken.

| FLATTEN, parameter | Voorbeeld | Ondersteund | Opmerkingen |
|---|---|:---:|---|
| Geen | `prod:cja` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | |
| `?FLATTEN` | `prod:cja?FLATTEN` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | |
| `%3FFLATTEN` | `prod:cja%3FFLATTEN` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | **geadviseerde optie om** te gebruiken. Opmerking: `%3FFLATTEN` is een URL-gecodeerde versie van `?FLATTEN` . |

### Meer informatie

* [Vereisten](/help/data-views/bi-extension.md#prerequisites)
* [ gids van Geloofsbrieven ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/credentials)


>[!TAB  Jupyter Notitieboekje ]

1. Open de vereiste referenties en parameters via de gebruikersinterface van de Experience Platform Query Service.

   1. Navigeer naar uw Experience Platform-sandbox.
   1. Selecteer ![ Vragen ](/help/assets/icons/DataSearch.svg) **[!UICONTROL Queries]** van het linkerspoor.
   1. Selecteer de tab **[!UICONTROL Credentials]** in de interface van **[!UICONTROL Queries]** .
   1. Selecteer `prod:cja` in de vervolgkeuzelijst **[!UICONTROL Database]** .

      ![ de dienstgeloofsbrieven van de Vraag ](assets/queryservice-credentials.png)

1. Zorg ervoor dat u een speciale virtuele Python-omgeving hebt ingesteld voor het uitvoeren van uw Jupyter-laptopomgeving.
1. Controleer of u de vereiste bibliotheken in uw virtuele omgeving hebt geïnstalleerd:
   * ipython-sql: `pip install ipython-sql`.
   * psycopg2-binary: `pip install psycopg-binary`.
   * sqlalchemy: pip `install sqlalchemy` .

1. Start Jupyter-laptop vanuit uw virtuele omgeving: `jupyter notebook` .
1. Creeer een nieuwe notitieboekje, of download [ deze steekproefnotitieboekje ](assets/BI-Extension.ipynb.zip).
1. Voer in de eerste cel de volgende gegevens in en voer deze uit:

   ```
   %config SqlMagic.style = '_DEPRECATED_DEFAULT'
   ```

1. In een nieuwe cel, ga de config parameters voor uw verbinding in. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om waarden van het Experience Platform **[!UICONTROL Query]** **[!UICONTROL Expiring Credentials]** paneel aan de waarden te kopiëren en te kleven die voor de config parameters worden vereist. Bijvoorbeeld:

   ```
   import ipywidgets as widgets
   from IPython.display import display
   
   config_host = widgets.Text(description='Host:', value='example.platform-query-stage.adobe.io',
                           layout=widgets.Layout(width="600px"))
   display(config_host)
   config_port = widgets.IntText(description='Port:', value=80,
                              layout=widgets.Layout(width="200px"))
   display(config_port)
   config_db = widgets.Text(description='Database:', value='prod:cja',
                         layout=widgets.Layout(width="300px"))
   display(config_db)
   config_username = widgets.Text(description='Username:', value='EC582F955C8A79F70A49420E@AdobeOrg',
                               layout=widgets.Layout(width="600px"))
   display(config_username)
   config_password = widgets.Password(description='Password:', value='***',
                                   layout=widgets.Layout(width="600px"))
   display(config_password)
   ```

1. Voer de cel uit.
1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om het wachtwoord van het Experience Platform **[!UICONTROL Query]** te kopiëren en te kleven **[!UICONTROL Expiring Credentials]** paneel aan het **[!UICONTROL Password]** gebied in Jupyter Notitieboekje.

   ![ Stap 1 van Config van het Notitieboekje van Jupter ](assets/jupyter-config-step1.png)

1. Voer in een nieuwe cel de instructies in om de SQL-extensie, de vereiste bibliotheek en de verbinding met Customer Journey Analytics te laden.

   ```python
   %load_ext sql
   from sqlalchemy import create_engine
   %sql postgresql://{config_username.value}:{config_password.value}@{config_host.value}:{config_port.value}/{config_db.value}?sslmode=require
   ```

   Voer de shell uit. Er wordt geen uitvoer weergegeven, maar de cel moet zonder waarschuwing worden uitgevoerd.

   ![ Stap 4 van Config van het Notitieboekje van de Jupyer 1}](assets/jupyter-config-step2.png)

1. In een nieuwe vraag, ga de verklaringen in om een lijst van beschikbare gegevensmeningen te krijgen die op de verbinding worden gebaseerd.

   ```python
   %%sql
   SELECT n.nspname as "Schema",
      c.relname as "Name",
      CASE c.relkind WHEN 'r' THEN 'table' WHEN 'v' THEN 'view' WHEN 'm' THEN 'materialized view' WHEN 'i' THEN 'index' WHEN 'S' THEN 'sequence' WHEN 's' THEN 'special' WHEN 't' THEN 'TOAST table' WHEN 'f' THEN 'foreign table' WHEN 'p' THEN 'partitioned table' WHEN 'I' THEN 'partitioned index' END as "Type",
      pg_catalog.pg_get_userbyid(c.relowner) as "Owner"
   FROM pg_catalog.pg_class c
   LEFT JOIN pg_catalog.pg_namespace n ON n.oid = c.relnamespace
   WHERE c.relkind IN ('v','')
      AND n.nspname <> 'pg_catalog'
      AND n.nspname !~ '^pg_toast'
      AND n.nspname <> 'information_schema'
      AND pg_catalog.pg_table_is_visible(c.oid)
      AND c.relname NOT LIKE '%test%'
      AND c.relname NOT LIKE '%ajo%'
   ORDER BY 1,2;
   ```

   Voer de shell uit. U zou uitvoersimulator aan het hieronder opgenomen schermschot moeten zien.

   ![ Stap 5 van Config van het Notitieboekje van Jupyter ](assets/jupyter-config-step3.png)

   De **[!UICONTROL cc_data_view]** wordt weergegeven in de lijst met gegevensweergaven.

### Naar FLATTEN of niet

Jupyter-laptop ondersteunt de volgende scenario&#39;s voor de parameter `FLATTEN` . Zie [ genestelde gegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie afvlakken.

| FLATTEN, parameter | Voorbeeld | Ondersteund | Opmerkingen |
|---|---|:---:|---|
| Geen | `prod:cja` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | |
| `?FLATTEN` | `prod:cja?FLATTEN` | ![ CloseCircle ](/help/assets/icons/CloseCircle.svg) | |
| `%3FFLATTEN` | `prod:cja%3FFLATTEN` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | **geadviseerde optie om** te gebruiken. Opmerking: `%3FFLATTEN` is een URL-gecodeerde versie van `?FLATTEN` . |

### Meer informatie

* [Vereisten](/help/data-views/bi-extension.md#prerequisites)
* [ gids van Geloofsbrieven ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/credentials)

>[!TAB  RStudio ]

1. Open de vereiste referenties en parameters via de gebruikersinterface van de Experience Platform Query Service.

   1. Navigeer naar uw Experience Platform-sandbox.
   1. Selecteer ![ Vragen ](/help/assets/icons/DataSearch.svg) **[!UICONTROL Queries]** van het linkerspoor.
   1. Selecteer de tab **[!UICONTROL Credentials]** in de interface van **[!UICONTROL Queries]** .
   1. Selecteer `prod:cja` in de vervolgkeuzelijst **[!UICONTROL Database]** .

      ![ de dienstgeloofsbrieven van de Vraag ](assets/queryservice-credentials.png)

1. Start RStudio.
1. Creeer een nieuw dossier van de Markering R, of download [ dit voorbeeld of markeringsdossier ](assets/BI-Extension.Rmd.zip).
1. Voer in het eerste segment de volgende instructies in tussen ` ```{r} ` en ` ``` ` . Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om waarden van het Experience Platform **[!UICONTROL Query]** **[!UICONTROL Expiring Credentials]** paneel aan de waarden te kopiëren en te kleven die voor de diverse parameters, zoals `host` worden vereist, `dbname`, en `user`. Bijvoorbeeld:

   ```R
   library(rstudioapi)
   library(DBI)
   library(dplyr)
   library(tidyr)
   library(RPostgres)
   library(ggplot2)
   
   host <- rstudioapi::showPrompt(title = "Host", message = "Host", default = "orangestagingco.platform-query-stage.adobe.io")
   dbname <- rstudioapi::showPrompt(title = "Database", message = "Database", default = "prod:cja?FLATTEN")
   user <- rstudioapi::showPrompt(title = "Username", message = "Username", default = "EC582F955C8A79F70A49420E@AdobeOrg")
   password <- rstudioapi::askForPassword(prompt = "Password")
   ```

1. Voer het segment uit. U wordt gevraagd om **[!UICONTROL Host]** , **[!UICONTROL Database]** en **[!UICONTROL User]** . Accepteer gewoon de waarden die u hebt opgegeven als onderdeel van de vorige stap.
1. Gebruik ![ Exemplaar ](/help/assets/icons/Copy.svg) om het wachtwoord van het Experience Platform **[!UICONTROL Query]** **[!UICONTROL Expiring Credentials]** paneel aan de **[!UICONTROL Password]** dialoogherinnering in RStudio te kopiëren en te kleven.

   ![ RStudio config stap 1 ](assets/rstudio-config-step1.png)

1. Maak een nieuw segment en voer de volgende instructies in tussen ` ``` {r} ` en ` ``` ` .

   ```R
   con <- dbConnect(
      RPostgres::Postgres(),
      host = host,
      port = 80,
      dbname = dbname,
      user = user,
      password = password,
      sslmode = 'require'
   )
   ```

1. Voer het segment uit. Er wordt geen uitvoer weergegeven als de verbinding is gelukt.


1. Maak een nieuw segment en voer de volgende instructies in tussen ` ``` {r} ` en ` ``` ` .

   ```R
   views <- dbListTables(con)
   print(views)
   ```

1. Voer het segment uit. U moet `character(0)` zien als de enige uitvoer.


1. Maak een nieuw segment en voer de volgende instructies in tussen ` ``` {r} ` en ` ``` ` .

   ```R
   glimpse(dv)
   ```

1. Voer het segment uit. U zou uitvoersimulator aan het hieronder opgenomen schermschot moeten zien.

   ![ RStudio config stap 2 ](assets/rstudio-config-step2.png)

### Naar FLATTEN of niet

RStudio ondersteunt de volgende scenario&#39;s voor de parameter `FLATTEN` . Zie [ genestelde gegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/query/key-concepts/flatten-nested-data) voor meer informatie afvlakken.

| FLATTEN, parameter | Voorbeeld | Ondersteund | Opmerkingen |
|---|---|:---:|---|
| Geen | `prod:cja` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | |
| `?FLATTEN` | `prod:cja?FLATTEN` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | **geadviseerde optie om** te gebruiken. |
| `%3FFLATTEN` | `prod:cja%3FFLATTEN` | ![ CloseCircle ](/help/assets/icons/CloseCircle.svg) | |

### Meer informatie

* [Vereisten](/help/data-views/bi-extension.md#prerequisites)
* [ gids van Geloofsbrieven ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/credentials)

>[!ENDTABS]

+++


## Dagelijkse trend

In dit geval wilt u een tabel en eenvoudige lijnvisualisatie weergeven met een dagelijkse trend van voorvallen (gebeurtenissen) van 1 januari 2023 tot 31 januari 2023.

+++ Customer Journey Analytics

Een voorbeeldvenster **[!UICONTROL Daily Trend]** voor het hoofdlettergebruik:

![ Customer Journey Analytics het Dagelijkse paneel van de Trend ](assets/cja_daily_trend.png)

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u a [ succesvolle verbinding en kunt gegevensmeningen ](#connect-and-validate) voor het hulpmiddel bevestigen en gebruiken BI waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL daterangeday]** .
   1. Selecteer **[!UICONTROL sum occurrences]** .

   Er wordt een tabel weergegeven met de exemplaren voor de huidige maand. Vergroot de visualisatie voor een betere zichtbaarheid.

1. In het deelvenster **[!UICONTROL Filters]** :

   1. Selecteer de **[!UICONTROL daterangeday is (All)]** van **[!UICONTROL Filters on this visual]**.
   1. Selecteer **[!UICONTROL Advanced filtering]** als de **[!UICONTROL Filter type]** .
   1. Definieer het filter op **[!UICONTROL Show items when the value]** **[!UICONTROL is on or after]** `1/1/2023` **[!UICONTROL And]** **[!UICONTROL is before]** `2/1/2023.` U kunt het kalenderpictogram gebruiken om datums te selecteren en te selecteren.
   1. Selecteer **[!UICONTROL Apply filter]** .

   De tabel wordt bijgewerkt met het toegepaste filter **[!UICONTROL daterangeday]** .

1. Selecteer in het deelvenster **[!UICONTROL Visualizations]** de **[!UICONTROL Line chart]** visualisatie.

   Een lijngrafiekvisualisatie vervangt de lijst terwijl het gebruiken van de zelfde gegevens zoals de lijst. Je Power BI Desktop moet er hieronder uitzien.

   ![ Geval van het Gebruik van de Desktop van Power BI 2 de waaierfilter van de Datum ](assets/uc2-pbi-daterange.png)

1. Op het grafiekvisualisatie van de Lijn:

   1. Selecteer ![ Meer ](/help/assets/icons/More.svg).
   1. Selecteer **[!UICONTROL Show as a table]** in het contextmenu.

   De hoofdweergave wordt bijgewerkt om zowel een lijnvisualisatie als een tabel weer te geven. Je Power BI Desktop moet er hieronder uitzien.

   ![ Geval 2 van het Gebruik van de Desktop van Power BI Def. Dagelijkse Tendvisualisatie ](assets/uc2-pbi-final.png)

>[!TAB  Desktop Tableau ]

1. Selecteer de tab **[!UICONTROL Sheet 1]** onderaan om te schakelen van de weergave **[!UICONTROL Data source]** . In de weergave **[!UICONTROL Sheet 1]** :
   1. Sleep de vermelding **[!UICONTROL Daterange]** uit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet deze op de **[!UICONTROL Filters]** shelf neer.
   1. Selecteer **[!UICONTROL Filters Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer **[!UICONTROL Filter \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of dates]** en geef een punt op van `01/01/2023` - `01/02/2023` .

      ![ de Filter van de Desktop van Tableau ](assets/uc2-tableau-filter.png)

   1. Sleep **[!UICONTROL Daterangeday]** vanuit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet de vermelding in het veld naast **[!UICONTROL Columns]** neer.
      * Selecteer **[!UICONTROL Day]** in de vervolgkeuzelijst **[!UICONTROL Daterangeday]** , zodat de waarde wordt bijgewerkt naar **[!UICONTROL DAY(Daterangeday)]** .
   1. De belemmering en laat vallen **[!UICONTROL Occurrences]** van de **[!UICONTROL Tables (*Namen van de Maatregel *)]**lijst in de **[!UICONTROL Data]**ruit en laat vallen de ingang op het gebied naast **[!UICONTROL Rows]**. De waarde wordt automatisch omgezet in **[!UICONTROL SUM(Occurrences)]**.
   1. Wijzig **[!UICONTROL Standard]** in **[!UICONTROL Entire View]** in het vervolgkeuzemenu **[!UICONTROL Fit]** op de werkbalk.

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Grafiek van de Desktop van Tableau ](assets/uc2-tableau-graph.png)

1. Selecteer **[!UICONTROL Duplicate]** in het contextmenu van de tab **[!UICONTROL Sheet 1]** om een tweede blad te maken.
1. Selecteer **[!UICONTROL Rename]** in het contextmenu van de tab **[!UICONTROL Sheet 1]** om de naam van het werkblad te wijzigen in `Graph` .
1. Selecteer **[!UICONTROL Rename]** in het contextmenu van de tab **[!UICONTROL Sheet 1 (2)]** om de naam van het werkblad te wijzigen in `Data` .
1. Zorg ervoor dat het **[!UICONTROL Data]** -werkblad is geselecteerd. In de weergave **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL Show me]** rechtsboven en selecteer **[!UICONTROL Text table]** (bovenste visualisatie linksboven) om de inhoud van de gegevensweergave te wijzigen in een tabel.
   1. Selecteer **[!UICONTROL Swap Rows and Columns]** op de werkbalk.
   1. Wijzig **[!UICONTROL Standard]** in **[!UICONTROL Entire View]** in het vervolgkeuzemenu **[!UICONTROL Fit]** op de werkbalk.

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Gegevens van de Desktop van Tableau ](assets/uc2-tableau-data.png)

1. Selecteer de tabknop **[!UICONTROL New Dashboard]** (onder) om een nieuwe **[!UICONTROL Dashboard 1]** -weergave te maken. In de weergave **[!UICONTROL Dashboard 1]** :
   1. Sleep en laat vallen het **[!UICONTROL Graph]** blad van **[!UICONTROL Sheets]** plank op de **[!UICONTROL Dashboard 1]** mening die *Dropbladen hier* leest.
   1. Sleep het **[!UICONTROL Data]** -werkblad van de **[!UICONTROL Sheets]** -plank onder het **[!UICONTROL Graph]** -werkblad naar de **[!UICONTROL Dashboard 1]** -weergave.
   1. Selecteer het **[!UICONTROL Data]** -werkblad in de weergave en wijzig **[!UICONTROL Entire View]** in **[!UICONTROL Fix Width]** .

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Dashboard 1 van de Desktop van Tableau ](assets/uc2-tableau-dashboard.png)


>[!TAB  Leider ]

1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![ Plaatsende ](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![ filter van de Leider ](assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2023/02/01]** .
1. Vanaf het gedeelte **[!UICONTROL Cc Data View]** in de linkerspoorstaaf,
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en **[!UICONTROL Date]** in de lijst met **[!UICONTROL DIMENSIONS]** .
   1. Selecteer **[!UICONTROL Count]** onder **[!UICONTROL MEASURES]** in de linkertrack (onder).
1. Selecteer **[!UICONTROL Run]** .
1. Selecteer **[!UICONTROL ‣ Visualization]** om de lijnvisualisatie weer te geven.

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![ Minder resultaat dagelijkse trend ](assets/uc2-looker-result.png)


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

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc2-jupyter-results.png)


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

   ![ Resultaten RStudio ](assets/uc2-rstudio-results.png)

>[!ENDTABS]

+++


## Uurtrend

In dit gebruiksgeval wilt u een tabel en eenvoudige lijnvisualisatie weergeven met een trend per uur van voorkomen(gebeurtenissen) voor 1 januari 2023.

+++ Customer Journey Analytics

Een voorbeeldvenster **[!UICONTROL Hourly Trend]** voor het hoofdlettergebruik:

![ de Uur van de Trend van Customer Journey Analytics visualisaties ](assets/cja_hourly_trend.png)

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [ een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening ](#connect-and-validate) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

![ AlertRed ](/help/assets/icons/AlertRed.svg) Power BI **** begrijpt niet hoe te om datum-tijd gebieden te behandelen, zodat worden de afmetingen zoals **[!UICONTROL daterangehour]** en **[!UICONTROL daterangeminute]** niet gesteund.

>[!TAB  Desktop Tableau ]

1. Selecteer de tab **[!UICONTROL Sheet 1]** onderaan om te schakelen van **[!UICONTROL Data source]** . In de weergave **[!UICONTROL Sheet 1]** :
   1. Sleep de vermelding **[!UICONTROL Daterange]** uit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet deze op de **[!UICONTROL Filters]** shelf neer.
   1. Selecteer **[!UICONTROL Filters Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer **[!UICONTROL Filter \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of dates]** en geef een punt op van `01/01/2023` - `02/01/2023` .

      ![ de Filter van de Desktop van Tableau ](assets/uc3-tableau-filter.png)

   1. Sleep **[!UICONTROL Daterangehour]** vanuit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet de vermelding in het veld naast **[!UICONTROL Columns]** neer.
      * Selecteer **[!UICONTROL More]** > **[!UICONTROL Hours]** in de vervolgkeuzelijst **[!UICONTROL Daterangeday]** , zodat de waarde wordt bijgewerkt naar **[!UICONTROL HOUR(Daterangeday)]** .
   1. De belemmering en laat vallen **[!UICONTROL Occurrences]** van de **[!UICONTROL Tables (*Namen van de Maatregel *)]**lijst in de **[!UICONTROL Data]**ruit en laat vallen de ingang op het gebied naast **[!UICONTROL Rows]**. De waarde wordt automatisch omgezet in **[!UICONTROL SUM(Occurrences)]**.
   1. Wijzig **[!UICONTROL Standard]** in **[!UICONTROL Entire View]** in het vervolgkeuzemenu **[!UICONTROL Fit]** op de werkbalk.

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Grafiek van de Desktop van Tableau ](assets/uc3-tableau-graph.png)

1. Selecteer **[!UICONTROL Duplicate]** in het contextmenu van de tab **[!UICONTROL Sheet 1]** om een tweede blad te maken.
1. Selecteer **[!UICONTROL Rename]** in het contextmenu van de tab **[!UICONTROL Sheet 1]** om de naam van het werkblad te wijzigen in `Graph` .
1. Selecteer **[!UICONTROL Rename]** in het contextmenu van de tab **[!UICONTROL Sheet 1 (2)]** om de naam van het werkblad te wijzigen in `Data` .
1. Zorg ervoor dat het **[!UICONTROL Data]** -werkblad is geselecteerd. In de weergave **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL Show me]** rechtsboven en selecteer **[!UICONTROL Text table]** (bovenste visualisatie linksboven) om de inhoud van de gegevensweergave te wijzigen in een tabel.
   1. Sleep **[!UICONTROL HOUR(Daterangeday)]** van **[!UICONTROL Columns]** naar **[!UICONTROL Rows]** .
   1. Wijzig **[!UICONTROL Standard]** in **[!UICONTROL Entire View]** in het vervolgkeuzemenu **[!UICONTROL Fit]** op de werkbalk.

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Gegevens van de Desktop van Tableau ](assets/uc3-tableau-data.png)

1. Selecteer **[!UICONTROL New Dashboard]** tabknop (onder) om een nieuwe **[!UICONTROL Dashboard 1]** -weergave te maken. In de weergave **[!UICONTROL Dashboard 1]** :
   1. Sleep en laat vallen het **[!UICONTROL Graph]** blad van **[!UICONTROL Sheets]** plank op de **[!UICONTROL Dashboard 1]** mening die *Dropbladen hier* leest.
   1. Sleep het **[!UICONTROL Data]** -werkblad van de **[!UICONTROL Sheets]** -plank onder het **[!UICONTROL Graph]** -werkblad naar de **[!UICONTROL Dashboard 1]** -weergave.
   1. Selecteer het **[!UICONTROL Data]** -werkblad in de weergave en wijzig **[!UICONTROL Entire View]** in **[!UICONTROL Fix Width]** .

      De weergave **[!UICONTROL Dashboard 1]** ziet er hieronder ongeveer zo uit.

      ![ Dashboard 1 van de Desktop van Tableau ](assets/uc3-tableau-dashboard.png)


>[!TAB  Leider ]


1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![ Plaatsende ](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![ filter van de Leider ](assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2023/01/02]** .
1. Vanaf het gedeelte **[!UICONTROL Cc Data View]** in de linkerspoorstaaf,
   1. Selecteer **[!UICONTROL ‣ Daterangehour Date]** en **[!UICONTROL Time]** in de lijst met **[!UICONTROL DIMENSIONS]** .
   1. Selecteer **[!UICONTROL Count]** onder **[!UICONTROL MEASURES]** in de linkertrack (onder).
1. Selecteer **[!UICONTROL Run]** .
1. Selecteer **[!UICONTROL ‣ Visualization]** om de lijnvisualisatie weer te geven.

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![ Minder resultaat dagelijkse trend ](assets/uc3-looker-result.png)


>[!TAB  Jupyter Notitieboekje ]

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   import seaborn as sns
   import matplotlib.pyplot as plt
   data = %sql SELECT daterangehour AS Hour, COUNT(*) AS Events \
               FROM cc_data_view \
               WHERE daterange BETWEEN '2023-01-01' AND '2023-01-02' \
               GROUP BY 1 \
                ORDER BY Hour ASC
   df = data.DataFrame()
   df = df.groupby('Hour', as_index=False).sum()
   plt.figure(figsize=(15, 3))
   sns.lineplot(x='Hour', y='Events', data=df)
   plt.show()
   display(data)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc3-jupyter-results.png)


>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ```{r} ` en ` ``` ` in een nieuw segment in.

   ```R
   ## Hourly Events
   df <- dv %>%
      filter(daterange >= "2023-01-01" & daterange < "2023-01-02") %>%
      group_by(daterangehour) %>%
      count() %>%
      arrange(daterangehour, .by_group = FALSE)
   ggplot(df, aes(x = daterangehour, y = n)) +
      geom_line(color = "#69b3a2") +
      ylab("Events") +
      xlab("Hour")
   print(df)
   ```

1. Voer het segment uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Resultaten RStudio ](assets/uc3-rstudio-results.png)

>[!ENDTABS]

+++


## Maandelijkse trend

In dit gebruiksgeval, wilt u een lijst en eenvoudige lijnvisualisatie tonen die een maandelijkse trend van voorkomen (gebeurtenissen) voor 2023 toont.

+++ Customer Journey Analytics

Een voorbeeldvenster **[!UICONTROL Monthly Trend]** voor het hoofdlettergebruik:

![ Customer Journey Analytics Maandelijkse visualisatie van de Trend ](assets/cja_monthly_trend.png)

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [ een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening ](#connect-and-validate) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL daterangemonth]** .
   1. Selecteer **[!UICONTROL sum occurrences]** .

   Er wordt een tabel weergegeven met de exemplaren voor de huidige maand. Vergroot de visualisatie voor een betere zichtbaarheid.

1. In het deelvenster **[!UICONTROL Filters]** :

   1. Selecteer de **[!UICONTROL daterangemonth is (All)]** van **[!UICONTROL Filters on this visual]**.
   1. Selecteer **[!UICONTROL Advanced filtering]** als de **[!UICONTROL Filter type]** .
   1. Definieer het filter op **[!UICONTROL Show items when the value]** **[!UICONTROL is on or after]** `1/1/2023` **[!UICONTROL And]** **[!UICONTROL is before]** `1/1/2024.` U kunt het kalenderpictogram gebruiken om datums te selecteren en te selecteren.
   1. Selecteer **[!UICONTROL Apply filter]** .

   De tabel wordt bijgewerkt met het toegepaste filter **[!UICONTROL daterangemonth]** .

1. In het deelvenster **[!UICONTROL Visualizations]** :

   1. Selecteer de **[!UICONTROL Line chart]** visualisatie.

   Een lijngrafiekvisualisatie vervangt de lijst terwijl het gebruiken van de zelfde gegevens zoals de lijst. Je Power BI Desktop moet er hieronder uitzien.

   ![ Geval van het Gebruik van de Desktop van Power BI 2 de waaierfilter van de Datum ](assets/uc4-pbi-filter-daterange.png)

1. Op het grafiekvisualisatie van de Lijn:

   1. Selecteer ![ Meer ](/help/assets/icons/More.svg).
   1. Selecteer **[!UICONTROL Show as a table]** in het contextmenu.

   De hoofdweergave wordt bijgewerkt om zowel een lijnvisualisatie als een tabel weer te geven. Je Power BI Desktop moet er hieronder uitzien.

   ![ Geval 2 van het Gebruik van de Desktop van Power BI Def. Dagelijkse Tendvisualisatie ](assets/uc4-pbi-filter-final.png)

>[!TAB  Desktop Tableau ]

1. Selecteer de tab **[!UICONTROL Sheet 1]** onderaan om te schakelen van **[!UICONTROL Data source]** . In de weergave **[!UICONTROL Sheet 1]** :
   1. Sleep de vermelding **[!UICONTROL Daterange]** uit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet deze op de **[!UICONTROL Filters]** shelf neer.
   1. Selecteer **[!UICONTROL Filters Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer **[!UICONTROL Filter \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of dates]** en geef een punt op van `01/01/2023` - `01/01/2024` .

      ![ de Filter van de Desktop van Tableau ](assets/uc4-tableau-filter.png)

   1. Sleep **[!UICONTROL Daterangeday]** vanuit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet de vermelding in het veld naast **[!UICONTROL Columns]** neer.
      * Selecteer **[!UICONTROL MONTH]** in de vervolgkeuzelijst **[!UICONTROL Daterangeday]** , zodat de waarde wordt bijgewerkt naar **[!UICONTROL MONTH(Daterangeday)]** .
   1. De belemmering en laat vallen **[!UICONTROL Occurrences]** van de **[!UICONTROL Tables (*Namen van de Maatregel *)]**lijst in de **[!UICONTROL Data]**ruit en laat vallen de ingang op het gebied naast **[!UICONTROL Rows]**. De waarde wordt automatisch omgezet in **[!UICONTROL SUM(Occurrences)]**.
   1. Wijzig **[!UICONTROL Standard]** in **[!UICONTROL Entire View]** in het vervolgkeuzemenu **[!UICONTROL Fit]** op de werkbalk.

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Grafiek van de Desktop van Tableau ](assets/uc4-tableau-graph.png)

1. Selecteer **[!UICONTROL Duplicate]** in het contextmenu van de tab **[!UICONTROL Sheet 1]** om een tweede blad te maken.
1. Selecteer **[!UICONTROL Rename]** in het contextmenu van de tab **[!UICONTROL Sheet 1]** om de naam van het werkblad te wijzigen in `Graph` .
1. Selecteer **[!UICONTROL Rename]** in het contextmenu van de tab **[!UICONTROL Sheet 1 (2)]** om de naam van het werkblad te wijzigen in `Data` .
1. Zorg ervoor dat het **[!UICONTROL Data]** -werkblad is geselecteerd. In de weergave Gegevens:
   1. Selecteer **[!UICONTROL Show me]** rechtsboven en selecteer **[!UICONTROL Text table]** (bovenste visualisatie linksboven) om de inhoud van de gegevensweergave te wijzigen in een tabel.
   1. Sleep **[!UICONTROL MONTH(Daterangeday)]** van **[!UICONTROL Columns]** naar **[!UICONTROL Rows]** .
   1. Wijzig **[!UICONTROL Standard]** in **[!UICONTROL Entire View]** in het vervolgkeuzemenu **[!UICONTROL Fit]** op de werkbalk.

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Gegevens van de Desktop van Tableau ](assets/uc4-tableau-data.png)

1. Selecteer **[!UICONTROL New Dashboard]** tabknop (onder) om een nieuwe **[!UICONTROL Dashboard 1]** -weergave te maken. In de weergave **[!UICONTROL Dashboard 1]** :
   1. Sleep en laat vallen het **[!UICONTROL Graph]** blad van **[!UICONTROL Sheets]** plank op de **[!UICONTROL Dashboard 1]** mening die *Dropbladen hier* leest.
   1. Sleep het **[!UICONTROL Data]** -werkblad van de **[!UICONTROL Sheets]** -plank onder het **[!UICONTROL Graph]** -werkblad naar de **[!UICONTROL Dashboard 1]** -weergave.
   1. Selecteer het **[!UICONTROL Data]** -werkblad in de weergave en wijzig **[!UICONTROL Entire View]** in **[!UICONTROL Fix Width]** .

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Dashboard 1 van de Desktop van Tableau ](assets/uc4-tableau-dashboard.png)


>[!TAB  Leider ]

1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![ Plaatsende ](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![ filter van de Leider ](assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2024/01/01]** .
1. Vanaf de linkerspoorstaaf **[!UICONTROL Cc Data View]** ,
   1. Selecteer **[!UICONTROL ‣ Daterangemonth Date]** en **[!UICONTROL Month]** in de lijst met **[!UICONTROL DIMENSIONS]** .
   1. Selecteer **[!UICONTROL Count]** onder **[!UICONTROL MEASURES]** in de linkertrack (onder).
1. Selecteer **[!UICONTROL Run]** .
1. Selecteer **[!UICONTROL ‣ Visualization]** om de lijnvisualisatie weer te geven.

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![ Minder resultaat dagelijkse trend ](assets/uc4-looker-result.png)


>[!TAB  Jupyter Notitieboekje ]

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   import seaborn as sns
   import matplotlib.pyplot as plt
   data = %sql SELECT daterangemonth AS Month, COUNT(*) AS Events \
               FROM cc_data_view \
               WHERE daterange BETWEEN '2023-01-01' AND '2024-01-01' \
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

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc4-jupyter-results.png)


>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ```{r} ` en ` ``` ` in een nieuw segment in.

   ```R
   ## Hourly Events
   df <- dv %>%
      filter(daterange >= "2023-01-01" & daterange < "2023-01-02") %>%
      group_by(daterangehour) %>%
      count() %>%
      arrange(daterangehour, .by_group = FALSE)
   ggplot(df, aes(x = daterangehour, y = n)) +
      geom_line(color = "#69b3a2") +
      ylab("Events") +
      xlab("Hour")
   print(df)
   ```

1. Voer het segment uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Resultaten RStudio ](assets/uc4-rstudio-results.png)

>[!ENDTABS]

+++


## Eén dimensie, gerangschikt

In dit gebruiksgeval wilt u een tabel en eenvoudige streepjesvisualisatie weergeven met de aankoop- en aankoopopbrengsten voor productnamen over 2023.

+++ Customer Journey Analytics

Een voorbeeldvenster **[!UICONTROL Single Dimension Ranked]** voor het hoofdlettergebruik:

![ Customer Journey Analytics Enige gerangschikte afmeting visualisatie ](assets/cja-single-dimension-ranked.png)

+++

<!--

+++ BI tools

>[!PREREQUISITES]
>
>Ensure you have validated [a successful connection, can list data views, and use a data view](#connect-and-validate) for the BI tool for which you want to try out this use case. 
>

>[!BEGINTABS]

>[!TAB Power BI Desktop] 

1. In the **[!UICONTROL Data]** pane:
   1. Select **[!UICONTROL daterange]**.
   1. Select **[!UICONTROL product_name]**.
   1. Select **[!UICONTROL sum purchase_revenue]**.
   1. Select **[!UICONTROL sum purchases]**.
   
   You see an empty table displaying only the column headers for the selected element. For better visibility, enlarge the visualization.

1. In the **[!UICONTROL Filters]** pane:

   1. Select the **[!UICONTROL daterange is (All)]** from **[!UICONTROL Filters on this visual]**.
   1. Select **[!UICONTROL Relative date]** as the **[!UICONTROL Filter type]**.
   1. Define the filter to **[!UICONTROL Show items when the value]** **[!UICONTROL is in the last]** `1` **[!UICONTROL calendar years]**.
   1. Select **[!UICONTROL Apply filter]**.
   
   You see the table updated with the applied **[!UICONTROL daterange]** filter.

1. In the **[!UICONTROL Visualization]** pane:

   1. Use ![CrossSize75](/help/assets/icons/CrossSize75.svg) to remove **[!UICONTROL daterange]** from **[!UICONTROL Columns]**.
   1. Drag and drop **[!UICONTROL Sum of purchases_revenue]** underneath **[!UICONTROL Sum of purchases]** in **[!UICONTROL Columns]**.

1. On the Table visualization:
   
   1. Select **[!UICONTROL Sum of purchase_revenue]** to sort the product names in descending purchase revenue order. Your Power BI Desktop should look like below.
   
   ![Power BI Desktop Use Case 5 Table status](assets/uc5-pbi-table.png)

1. In the **[!UICONTROL Filters]** pane:

   1. Select **[!UICONTROL product_name is (All)]**.
   1. Set **[!UICONTROL Filter type]** to **[!UICONTROL Top N]**.
   1. Define the filter to **[!UICONTROL Show items]** **[!UICONTROL Top]** `10` **[!UICONTROL By value]**.
   1. Drag and drop **[!UICONTROL purchase_revenue]** into **[!UICONTROL By value]** **[!UICONTROL Add data fields here]**.
   1. Select **[!UICONTROL Apply filter]**.

   You see the table updated with values for purchase revenue in sync with the Freeform table visualization in Analysis Workspace.

1. In the **[!UICONTROL Visualizations]** pane:

   1. Select the **[!UICONTROL Line and stacked column chart]** visualization. 

   A line and stacked column chart visualization replaces the table while using the same data as the table.

1. Drag and drop **[!UICONTROL purchases]** onto **[!UICONTROL Line y-axis]** in the **[!UICONTROL Visualizations]** pane.

   The line and stacked column chart is updated. Your Power BI Desktop should look like below.

   ![Power BI Desktop Use Case 5 Graph](assets/uc5-pbi-chart.png)

1. On the Line and stacked column chart visualization:

   1. Select ![More](/help/assets/icons/More.svg).
   1. From the context menu, select **[!UICONTROL Show as a table]**.

   The main view is updated to show both a line visualization and a table.

   ![Power BI Desktop Use Case 2 Final Daily Trend visualization](assets/uc5-pbi-final.png)

>[!TAB Tableau Desktop]

1. Select the **[!UICONTROL Sheet 1]** tab at the bottom to switch from **[!UICONTROL Data source]**. In the **[!UICONTROL Sheet 1]** view:
   1. Drag the **[!UICONTROL Daterange]** entry from the **[!UICONTROL Tables]** list in the **[!UICONTROL Data]** pane and drop the entry onto the **[!UICONTROL Filters]** shelf.
   1. In the **[!UICONTROL Filters Field \[Daterange\]]** dialog, select **[!UICONTROL Range of Dates]** and select **[!UICONTROL Next >]**.
   1. In the **[!UICONTROL Filter \[Daterange\]]** dialog, select **[!UICONTROL Range of dates]** and specify a period of `01/01/2023` - `31/12/2023`. Select **[!UICONTROL Apply]** and **[!UICONTROL OK]**.

      ![Tableau Desktop Filter](assets/uc5-tableau-filter.png)

   1. Drag and drop **[!UICONTROL Product Name]** from the **[!UICONTROL Tables]** list in the **[!UICONTROL Data]** pane and drop the entry in the field next to **[!UICONTROL Rows]**.
   1. Drag and drop **[!UICONTROL Purchases]** from the **[!UICONTROL Tables (*Measure Names*)]** list in the **[!UICONTROL Data]** pane and drop the entry in the field next to **[!UICONTROL Rows]**. The value is automatically converted to **[!UICONTROL SUM(Purchases)]**.
   1. Drag and drop **[!UICONTROL Purchase Revenue]** from the **[!UICONTROL Tables (*Measure Names*)]** list in the **[!UICONTROL Data]** pane and drop the entry in the field next to **[!UICONTROL Columns]** and left from **[!UICONTROL SUM(Purchases)]**. The value is automatically converted to **[!UICONTROL SUM(Purchase Revenue)]**.
   1. To order both charts in descending purchase revenue order, hover over the **[!UICONTROL Purchase Revenue]** title and select the sort icon.
   1. To limit the number of entries in the charts, select **[!UICONTROL SUM(Purchase Revenue)]** in **[!UICONTROL Rows]** and from the drop-down menu select **[!UICONTROL Filter]**.
   1. In the **[!UICONTROL Filter \[Purchase Revenue\]]** dialog select **[!UICONTROL Range of values]** and enter appropriate values. For example: `1,000,000` - `2,000,000`. Select **[!UICONTROL Apply]** and **[!UICONTROL OK]**.
   1. To convert the two bar charts to a dual combination chart, select **[!UICONTROL SUM(Purchases)]** in **[!UICONTROL Rows]** and from the drop-down menu, select **[!UICONTROL Dual Axis]**. The bar charts transform into a scatter plot.
   1. To modify the scatter plot to a bar chart:
      1. Select **[!UICONTROL SUM(Purchases)]** in the **[!UICONTROL Marks]** area and select **[!UICONTROL Line]** from the drop-down menu.
      1. Select **[!UICONTROL SUM(Purchase Revenue)]** in the **[!UICONTROL Marks]** area and select **[!UICONTROL Bar]** from the drop-down menu.

   Your Tableau Desktop should look like below.

   ![Tableau Desktop Graph](assets/uc5-tableau-graph.png)

1. Select **[!UICONTROL Duplicate]** from the **[!UICONTROL Sheet 1]** tab context menu to create a second sheet.
1. Select **[!UICONTROL Rename]** from the **[!UICONTROL Sheet 1]** tab context menu to rename the sheet to `Data`.
1. Select **[!UICONTROL Rename]** from the **[!UICONTROL Sheet 1 (2)]** tab context menu to rename the sheet to `Graph`.
1. Ensure that the **[!UICONTROL Data]** sheet is selected.
   1. Select **[!UICONTROL Show me]** at the top right and select **[!UICONTROL Text table]** (upper left top visualization) to modify the content of the two charts to a table.
   1. To order purchase revenue in descending order, hover over **[!UICONTROL Purchase Revenue]** in the table and select ![SortOrderDown](/help/assets/icons/SortOrderDown.svg).
   1. Select **[!UICONTROL Entire View]** from the **[!UICONTROL Fit]** drop-down menu.

   Your Tableau Desktop should look like below.

   ![Tableau Desktop Data](assets/uc5-tableau-data.png)

1. Select **[!UICONTROL New Dashboard]** tab button (at the bottom) to create a new **[!UICONTROL Dashboard 1]** view. In the **[!UICONTROL Dashboard 1]** view:
   1. Drag and drop the **[!UICONTROL Graph]** sheet from the **[!UICONTROL Sheets]** shelf onto the **[!UICONTROL Dashboard 1]** view that reads *Drop sheets here*.
   1. Drag and drop the **[!UICONTROL Data]** sheet from the **[!UICONTROL Sheets]** shelf below the **[!UICONTROL Graph]** sheet onto the **[!UICONTROL Dashboard 1]** view.
   1. Select the **[!UICONTROL Data]** sheet in the view and modify **[!UICONTROL Entire View]** to **[!UICONTROL Fix Width]**.

   Your **[!UICONTROL Dashboard 1]** view should look like below.

   ![Tableau Desktop Dashboard 1](assets/uc5-tableau-dashboard.png)



>[!TAB Looker]

1. In the **[!UICONTROL Explore]** interface of Looker, ensure you do have a clean setup. If not, select ![Setting](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Select **[!UICONTROL + Filter]** underneath **[!UICONTROL Filters]**.
1. In the **[!UICONTROL Add Filter]** dialog:
   1. Select **[!UICONTROL ‣ Cc Data View]**
   1. From the list of fields, select **[!UICONTROL ‣ Daterange Date]** then **[!UICONTROL Daterange Date]**.
      ![Looker filter](assets/uc2-looker-filter.png)
1. Specify the **[!UICONTROL Cc Data View Daterange Date]** filter as **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2024/01/01]**.
1. From the **[!UICONTROL ‣ Cc Data View]** section in the left rail, select **[!UICONTROL Product Name]**.
1. From the **[!UICONTROL ‣ Custom Fields]** section in the left rail:
   1. Select **[!UICONTROL Custom Measure]** from the **[!UICONTROL + Add]** drop-down menu. 
   1. In the **[!UICONTROL Create custom measure]** dialog:
      1. Select **[!UICONTROL Purchase Revenue]** from the **[!UICONTROL Field to measure]** drop-down menu.
      1. Select **[!UICONTROL Sum]** from the **[!UICONTROL Measure type]** drop-down menu.
      1. Enter a custom field name for **[!UICONTROL Name]**. For example: `Purchase Revenue`.
      1. Select the **[!UICONTROL Field details]** tab.
      1. Select **[!UICONTROL Decimals]** from the **[!UICONTROL Format]** drop-down menu and ensure `0` is entered in **[!UICONTROL Decimals]**.
         ![Looker custom metric field](assets/uc5-looker-customfield.png)
      1. Select **[!UICONTROL Save]**.
   1. Select **[!UICONTROL Custom Measure]** once more from the **[!UICONTROL + Add]** drop-down menu. In the **[!UICONTROL Create custom]** measure dialog:
      1. Select **[!UICONTROL Purchases]** from the **[!UICONTROL Field to measure]** drop-down menu.
      1. Select **[!UICONTROL Sum]** from the **[!UICONTROL Measure type]** drop-down menu.
      1. Enter a custom field name for **[!UICONTROL Name]**. For example: `Sum of Purchases`.
      1. Select the **[!UICONTROL Field details]** tab.
      1. Select **[!UICONTROL Decimals]** from the **[!UICONTROL Format]** drop-down menu and ensure `0` is entered in **[!UICONTROL Decimals]**.
      1. Select **[!UICONTROL Save]**.
   1. Both fields are automatically added to the Data view. 
1. Select **[!UICONTROL + Filter]** to add another **[!UICONTROL Filters]** and to limit the data.
1. In the **[!UICONTROL Add Filter]** dialog, select **[!UICONTROL ‣ Custom Fields]**, then **[!UICONTROL Purchase Revenue]**.
1. Make the appropriate selections and enter the proposed values, so the filter reads **[!UICONTROL is between inclusive]** `1000000` **[!UICONTROL AND]** `2000000`.
1. Select **[!UICONTROL Run]**.
1. Select **[!UICONTROL ‣ Visualization]** to display the line visualization.
1. Select **[!UICONTROL Edit]** in **[!UICONTROL Visualization]** to update the visualization. In the popup dialog:
   1. Select the **[!UICONTROL Series]** tab.
   1. Scroll down to see **[!UICONTROL Purchases]** and change the **[!UICONTROL Type]** to **[!UICONTROL Line]**.
   1. Select the **[!UICONTROL Y]** tab.
   1. Drag **[!UICONTROL Purchases]** from the **[!UICONTROL Left 1 ]** container to where it reads **[!UICONTROL *Drag series here to create a new left axis*]**. This action creates a **[!UICONTROL Left 2]** container.
      ![Looker visualization configuration](assets/uc5-looker-visualization.png)
   1. Select ![CrossSize75](/help/assets/icons/CrossSize75.svg) next to **[!UICONTROL Edit]** to hide the popup dialog

You should see a visualization and table similar as shown below.

![Looker result daily trend](assets/uc5-looker-result.png)


>[!TAB Jupyter Notebook]

1. Enter the following statements in a new cell.

   ```python
   import seaborn as sns
   import matplotlib.pyplot as plt
   data = %sql SELECT product_name AS `Product Name`, SUM(purchase_revenue) AS `Purchase Revenue`, SUM(purchases) AS `Purchases` \
               FROM cc_data_view \
               WHERE daterange BETWEEN '2023-01-01' AND '2024-01-01' \
               GROUP BY 1 \
               LIMIT 10;
   df = data.DataFrame()
   df = df.groupby('Product Name', as_index=False).sum()
   plt.figure(figsize=(15, 3))
   sns.barplot(x='Purchase Revenue', y='Product Name', data=df)
   plt.show()
   display(data)
   ```

1. Execute the cell. You should see output similar to the screenshot below.

   ![Jupyter Notebook Results](assets/uc5-jupyter-results.png)


>[!TAB RStudio]

1. Enter the following statements between ` ```{r} ` and ` ``` ` in a new chunk.

   ```R
   library(tidyr)

   ## Single dimension ranked
   df <- dv %>%
      filter(daterange >= "2023-01-01" & daterange < "2024-01-01") %>%
      group_by(product_name) %>%
      summarise(purchase_revenue = sum(purchase_revenue), purchases = sum(purchases)) %>%
      arrange(product_name, .by_group = FALSE)
   dfV <- df %>%
      head(5)
   ggplot(dfV, aes(x = purchase_revenue, y = product_name)) +
      geom_col(position = "dodge") +
      geom_text(aes(label = purchase_revenue), vjust = -0.5)
   print(df)
   ```

1. Run the chunk. You should see output similar to the screenshot below.

   ![RStudio Results](assets/uc5-rstudio-results.png)

>[!ENDTABS]

+++

-->


## Meerdere dimensies gerangschikt

In dit geval wilt u een tabel weergeven die de aankoopopbrengsten en -aankopen voor productnamen in productcategorieën opsplitst in 2023. Bovendien wilt u een aantal visualisaties gebruiken om zowel de distributie van de productcategorie als de bijdragen voor productnamen binnen elke productcategorie te illustreren.

+++ Customer Journey Analytics

Een voorbeeldvenster **[!UICONTROL Multiple Dimension Ranked]** voor het hoofdlettergebruik:

![ Veelvoudige Dimension van Customer Journey Analytics Rangschikte paneel ](assets/cja-multiple-dimension-ranked.png)

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [ een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening ](#connect-and-validate) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. Sleep **[!UICONTROL daterangeday]** van het deelvenster **[!UICONTROL Data]** aan **[!UICONTROL Filters on this page]** om ervoor te zorgen dat het datumbereik van toepassing is op alle visualisaties.
   1. Selecteer de **[!UICONTROL daterangeday is (All)]** van **[!UICONTROL Filters on this page]**.
   1. Selecteer **[!UICONTROL Relative date]** als de **[!UICONTROL Filter type]** .
   1. Definieer het filter naar **[!UICONTROL Show items when the value]** **[!UICONTROL is in the last]** `1` **[!UICONTROL calendar years]** .
   1. Selecteer **[!UICONTROL Apply filter]** .

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL datarangeday]** .
   1. Selecteer **[!UICONTROL product_category]** .
   1. Selecteer **[!UICONTROL product_name]** .
   1. Selecteren **[!UICONTROL sum purchase_revenue]**
   1. Selecteren **[!UICONTROL sum purchases]**

1. Als u het verticale staafdiagram wilt wijzigen in een tabel, zorgt u dat de tabel is geselecteerd en selecteert u **[!UICONTROL Matrix]** in het deelvenster **[!UICONTROL Visualizations]** .
   * Sleep **[!UICONTROL product_name]** vanuit **[!UICONTROL Columns]** en zet het veld onder **[!UICONTROL product_categor] **y neer in **[!UICONTROL Rows]** in het deelvenster **[!UICONTROL Visualization]** .

1. Selecteer **[!UICONTROL product_name is (All)]** in het deelvenster **[!UICONTROL Filters]** om het aantal weergegeven producten in de tabel te beperken.

   1. Selecteer **[!UICONTROL Advanced filtering]** .
   1. Selecteer **[!UICONTROL Filter type]** **[!UICONTROL Top N]** **[!UICONTROL Show items]** **[!UICONTROL Top]** `15` **[!UICONTROL By Value]** .
   1. Sleep **[!UICONTROL purchases]** vanuit het deelvenster **[!UICONTROL Data]** naar het deelvenster **[!UICONTROL Add data fields here]** .
   1. Selecteer **[!UICONTROL Apply filter]** .

1. Als u de leesbaarheid wilt verbeteren, selecteert u **[!UICONTROL View]** in het bovenste menu, selecteert u **[!UICONTROL Page View]** > **[!UICONTROL Actual size]** en wijzigt u de grootte van de tabelvisualisatie.

1. Selecteer **[!UICONTROL +]** op productcategorieniveau om elke categorie in de tabel op te splitsen. Je Power BI Desktop moet er hieronder uitzien.

   ![ de Meerdere Dimensies van de Desktop van Power BI Rangschikte matrixlijst ](assets/uc6-powerbi-data.png)

1. Selecteer **[!UICONTROL Home]** in het bovenste menu en selecteer **[!UICONTROL New visual]** . Een nieuwe visuele wordt toegevoegd aan uw rapport.

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL product_category]** .
   1. Selecteer **[!UICONTROL product_name]** .
   1. Selecteer **[!UICONTROL purchase_revenue]** .

1. Als u de visuele weergave wilt wijzigen, selecteert u het staafdiagram en selecteert u **[!UICONTROL Treemap]** in het deelvenster **[!UICONTROL Visualizations]** .
1. Zorg ervoor dat **[!UICONTROL product_category]** onder **[!UICONTROL Category]** en **[!UICONTROL product_name]** onder **[!UICONTROL Details]** in het deelvenster **[!UICONTROL Visualizations]** wordt weergegeven.

   Je Power BI Desktop moet er hieronder uitzien.

   ![ de Veelvoudige Dimensies van de Desktop van Power BI Rangschikte treemap ](assets/uc6-powerbi-treemap.png)

1. Selecteer **[!UICONTROL Home]** in het bovenste menu en selecteer **[!UICONTROL New visual]** . Een nieuwe visuele wordt toegevoegd aan uw rapport.

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL product_category]** .
   1. Selecteer **[!UICONTROL purchase_revenue]** .
   1. Selecteer **[!UICONTROL purchase]** .

1. In het deelvenster **[!UICONTROL Visualizations]** :
   1. Selecteer **[!UICONTROL Line and stacked column chart]** als u de visualisatie wilt wijzigen.
   1. Sleep **[!UICONTROL sum_of_purchases]** van **[!UICONTROL Column y-axis]** naar **[!UICONTROL Line y-axis]** .

1. Wijzig in het rapport de volgorde van de afzonderlijke visualisaties.

   Je Power BI Desktop moet er hieronder uitzien.

   ![ Veelvoudige Afmetingen van de Desktop van Power BI die definitief worden gerangschikt ](assets/uc6-powerbi-final.png)


>[!TAB  Desktop Tableau ]

1. Selecteer de tab **[!UICONTROL Sheet 1]** onderaan om te schakelen van **[!UICONTROL Data source]** . In de weergave **[!UICONTROL Sheet 1]** :
   1. Sleep de vermelding **[!UICONTROL Daterange]** uit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet deze op de **[!UICONTROL Filters]** shelf neer.
   1. Selecteer **[!UICONTROL Filters Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer in het dialoogvenster **[!UICONTROL Filter \[Daterange\]]** de optie **[!UICONTROL Relative dates]** , selecteer **[!UICONTROL Years]** en geef **[!UICONTROL Previous year]** op. Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ de Veelvoudige Rangschikte Filter van de Desktop van Tableau Dimension ](assets/uc6-tableau-filter.png)

   1. Sleep **[!UICONTROL Product Category]** en zet de muisknop los naast **[!UICONTROL Columns]** .
   1. Sleep **[!UICONTROL Purchase Revenue]** en zet de muisknop los naast **[!UICONTROL Rows]** . De waarde verandert in **[!UICONTROL SUM(Purchase Revenue)]** .
   1. Sleep Aankopen en zet ze neer naast **[!UICONTROL Rows]** . De waarde verandert in **[!UICONTROL SUM(Purchases)]** .
   1. Selecteer **[!UICONTROL SUM(Purchases)]** en selecteer **[!UICONTROL Dual Axis]** in de vervolgkeuzelijst.
   1. Selecteer **[!UICONTROL SUM(Purchases)]** in **[!UICONTROL Marks]** en selecteer **[!UICONTROL Line]** in de vervolgkeuzelijst.
   1. Selecteer **[!UICONTROL SUM(Purchase Revenue)]** in **[!UICONTROL Marks]** en selecteer **[!UICONTROL Bar]** in de vervolgkeuzelijst.
   1. Selecteer **[!UICONTROL Entire View]** in het menu **[!UICONTROL Fit]** .
   1. Selecteer de titel **[!UICONTROL Purchase Revenue]** in het diagram en controleer of de aankoopopbrengsten oplopend zijn.

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ Veelvoudige Afmetingen van de Desktop van Tableau Rangschikte Categorie ](assets/uc6-tableau-category.png)

1. Wijzig de naam van het huidige **[!UICONTROL Sheet 1]** blad in `Category` .
1. Selecteer **[!UICONTROL New Worksheet]** om een nieuw blad te maken en wijzig de naam in `Data` .

   1. Sleep de vermelding **[!UICONTROL Daterange]** uit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet deze op de **[!UICONTROL Filters]** shelf neer.
   1. Selecteer **[!UICONTROL Filters Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer in het dialoogvenster **[!UICONTROL Filter \[Daterange\]]** de optie **[!UICONTROL Relative dates]** , selecteer **[!UICONTROL Years]** en geef **[!UICONTROL Previous year]** op. Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Sleep **[!UICONTROL Purchase Revenue]** van **[!UICONTROL Data]** deelvenster naar **[!UICONTROL Columns]** . De waarde verandert in **[!UICONTROL SUM(Purchase Revenue)]** .
   1. Sleep **[!UICONTROL Purchase]** van **[!UICONTROL Data]** deelvenster naar **[!UICONTROL Columns]** naast **[!UICONTROL Purchase Revenue]** . De waarde verandert in **[!UICONTROL SUM(Purchases)]** .
   1. Sleep **[!UICONTROL Product Category]** van het **[!UICONTROL Data]** deelvenster naar **[!UICONTROL Rows]** .
   1. Sleep **[!UICONTROL Product Name]** van het **[!UICONTROL Data]** deelvenster naar **[!UICONTROL Rows]** , naast **[!UICONTROL Product Category]** .
   1. Als u de twee horizontale balken in een tabel wilt wijzigen, selecteert u **[!UICONTROL Text Table]** in **[!UICONTROL Show Me]** .
   1. Selecteer **[!UICONTROL Purchases]** in **[!UICONTROL Measure Values]** om het aantal producten te beperken. Selecteer **[!UICONTROL Filter]** in het keuzemenu.
   1. Selecteer **[!UICONTROL Filter \[Purchases\]]** in het dialoogvenster **[!UICONTROL At least]** en voer `7000` in. Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Selecteer **[!UICONTROL Fit Width]** in de vervolgkeuzelijst **[!UICONTROL the]** Passend.

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ de Veelvoudige Gegevens van Dimension van de Desktop van Tableau ](assets/uc6-tableau-data.png)

1. Selecteer **[!UICONTROL New worksheet]** om een nieuw blad te maken en de naam ervan te wijzigen in **[!UICONTROL Treemap]** .
   1. Sleep de vermelding **[!UICONTROL Daterange]** uit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet deze op de **[!UICONTROL Filters]** shelf neer.
   1. Selecteer **[!UICONTROL Filters Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer in het dialoogvenster **[!UICONTROL Filter \[Daterange\]]** de optie **[!UICONTROL Relative dates]** , selecteer **[!UICONTROL Years]** en geef **[!UICONTROL Previous year]** op. Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Sleep **[!UICONTROL Purchase Revenue]** van het **[!UICONTROL Data]** deelvenster naar **[!UICONTROL Rows]** . De waarden veranderen in **[!UICONTROL SUM(Purchase Revenue)]** .
   1. Sleep **[!UICONTROL Purchase]** van het **[!UICONTROL Data]** deelvenster naar **[!UICONTROL Rows]** , naast **[!UICONTROL Purchase Revenue]** . De waarde verandert in **[!UICONTROL SUM(Purchases)]** .
   1. Sleep **[!UICONTROL Product Category]** van het **[!UICONTROL Data]** deelvenster naar **[!UICONTROL Columns]** .
   1. Sleep **[!UICONTROL Product Name]** van het **[!UICONTROL Data]** deelvenster naar **[!UICONTROL Columns]** .
   1. Als u de twee verticale staafdiagrammen wilt wijzigen in een driehoek, selecteert u **[!UICONTROL Treemap]** in **[!UICONTROL Show Me]** .
   1. Selecteer **[!UICONTROL Purchases]** in **[!UICONTROL Measure Values]** om het aantal producten te beperken. Selecteer **[!UICONTROL Filter]** in het keuzemenu.
   1. Selecteer **[!UICONTROL Filter \[Purchases\]]** in het dialoogvenster **[!UICONTROL At least]** en voer `7000` in. Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Selecteer **[!UICONTROL Fit Width]** in de vervolgkeuzelijst **[!UICONTROL Fit]** .

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ de Veelvoudige Gegevens van Dimension van de Desktop van Tableau ](assets/uc6-tableau-treemap.png)

1. Selecteer **[!UICONTROL New Dashboard]** tabknop (onder) om een nieuwe **[!UICONTROL Dashboard 1]** -weergave te maken. In de weergave **[!UICONTROL Dashboard 1]** :
   1. Sleep en laat vallen het **[!UICONTROL Category]** blad van **[!UICONTROL Sheets]** plank op de **[!UICONTROL Dashboard 1]** mening die *Dropbladen hier* leest.
   1. Sleep het **[!UICONTROL Treemap]** -werkblad vanuit de **[!UICONTROL Sheets]** -plank onder het **[!UICONTROL Category]** -werkblad in de **[!UICONTROL Dashboard 1]** -weergave.
   1. Sleep het **[!UICONTROL Data]** -werkblad vanuit de **[!UICONTROL Sheets]** -plank onder het **[!UICONTROL Treemap]** -werkblad in de **[!UICONTROL Dashboard 1]** -weergave.
   1. Wijzig de grootte van elk blad in de weergave.

   De weergave **[!UICONTROL Dashboard 1]** ziet er hieronder ongeveer zo uit.

   ![ Dashboard 1 van de Desktop van Tableau ](assets/uc6-tableau-final.png)


>[!TAB  Leider ]

1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![ Plaatsende ](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![ filter van de Leider ](assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2024/01/01]** .
1. Vanuit het gedeelte **[!UICONTROL ‣ Cc Data View]** in de linkertrack:
   1. Selecteer **[!UICONTROL Product Category]** .
   1. Selecteer **[!UICONTROL Product Name]** .
1. Vanuit het gedeelte **[!UICONTROL ‣ Custom Fields]** in de linkertrack:
   1. Selecteer **[!UICONTROL Custom Measure]** in de vervolgkeuzelijst **[!UICONTROL + Add]** .
   1. In het dialoogvenster **[!UICONTROL Create custom measure]** :
      1. Selecteer **[!UICONTROL Purchase Revenue]** in de vervolgkeuzelijst **[!UICONTROL Field to measure]** .
      1. Selecteer **[!UICONTROL Sum]** in de vervolgkeuzelijst **[!UICONTROL Measure type]** .
      1. Voer een aangepaste veldnaam in voor **[!UICONTROL Name]** . Bijvoorbeeld: `Sum of Purchase Revenue` .
      1. Selecteer de tab **[!UICONTROL Field details]** .
      1. Selecteer **[!UICONTROL Decimals]** in de vervolgkeuzelijst **[!UICONTROL Format]** en zorg ervoor dat `0` wordt ingevoerd in **[!UICONTROL Decimals]** .
         ![ Lager aangepast metrisch gebied ](assets/uc5-looker-customfield.png)
      1. Selecteer **[!UICONTROL Save]** .
   1. Selecteer **[!UICONTROL Custom Measure]** nogmaals in de vervolgkeuzelijst **[!UICONTROL + Add]** . In het dialoogvenster **[!UICONTROL Create custom]** -meting:
      1. Selecteer **[!UICONTROL Purchases]** in de vervolgkeuzelijst **[!UICONTROL Field to measure]** .
      1. Selecteer **[!UICONTROL Sum]** in de vervolgkeuzelijst **[!UICONTROL Measure type]** .
      1. Voer een aangepaste veldnaam in voor **[!UICONTROL Name]** . Bijvoorbeeld: `Sum of Purchases` .
      1. Selecteer de tab **[!UICONTROL Field details]** .
      1. Selecteer **[!UICONTROL Decimals]** in de vervolgkeuzelijst **[!UICONTROL Format]** en zorg ervoor dat `0` wordt ingevoerd in **[!UICONTROL Decimals]** .
      1. Selecteer **[!UICONTROL Save]** .
   1. Beide velden worden automatisch toegevoegd aan de gegevensweergave.
1. Selecteer **[!UICONTROL Filters]** in de sectie **[!UICONTROL + Filter]** . In het dialoogvenster **[!UICONTROL Add Filter]** . Selecteer **[!UICONTROL ‣ Custom Fields]** en vervolgens **[!UICONTROL Purchase Revenue]** .
1. Selecteer **[!UICONTROL is >]** en voer `800000` in om de resultaten te beperken.
1. Selecteer **[!UICONTROL Run]** .
1. Selecteer **[!UICONTROL ‣ Visualization]** om de lijnvisualisatie weer te geven.
1. Selecteer **[!UICONTROL Edit]** in **[!UICONTROL Visualization]** om de visualisatie bij te werken. In het dialoogvenster Pop-up:
   1. Selecteer de tab **[!UICONTROL Plot]** .
   1. Schuif omlaag en selecteer **[!UICONTROL Edit Chart Config]** .
   1. Wijzig de JSON in **[!UICONTROL Chart Config (Override)]** zoals in de onderstaande schermafbeelding en selecteer vervolgens **[!UICONTROL Preview]** .

      ![ Laagere virtualisatie config ](assets/uc6-looker-visualization.png)

   1. Selecteer **[!UICONTROL Apply]** .
   1. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) naast **[!UICONTROL Edit]** om de popup dialoog te verbergen

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![ Minder resultaat dagelijkse trend ](assets/uc6-looker-result.png)


>[!TAB  Jupyter Notitieboekje ]

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   import seaborn as sns
   import matplotlib.pyplot as plt
   data = %sql SELECT product_category AS `Product Category`, product_name AS `Product Name`, SUM(purchase_revenue) AS `Purchase Revenue`, SUM(purchases) AS `Purchases` \
               FROM cc_data_view \
               WHERE daterange BETWEEN '2023-01-01' AND '2024-01-01' \
               GROUP BY 1, 2 \
               ORDER BY `Purchase Revenue` DESC \
               LIMIT 10;
   df = data.DataFrame()
   df = df.groupby(['Product Category', 'Product Name'], as_index=False).sum()
   plt.figure(figsize=(8, 8))
   sns.scatterplot(x='Product Category', y='Product Name', size='Purchase Revenue', sizes=(10, 200), hue='Purchases', palette='husl', data=df)
   plt.show()
   display(data)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc6-jupyter-results.png)


>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ```{r} ` en ` ``` ` in een nieuw segment in.

   ```R
   ## Multiple dimensions ranked
   df <- dv %>%
      filter(daterange >= "2023-01-01" & daterange < "2024-01-01") %>%
      group_by(product_category, product_name) %>%
      summarise(purchase_revenue = sum(purchase_revenue), purchases = sum(purchases), .groups = "keep") %>%
      arrange(desc(purchase_revenue), .by_group = FALSE)
   print(df)
   ```

1. Voer het segment uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Resultaten RStudio ](assets/uc6-rstudio-results.png)


>[!ENDTABS]

+++


## Waarden voor verschillende dimensies tellen

In dit geval wilt u het duidelijke aantal productnamen ophalen waarop in januari 2023 is gerapporteerd.

+++ Customer Journey Analytics

Als u een duidelijke telling van productnamen wilt rapporteren, stelt u in Customer Journey Analytics een berekende metrische waarde in met **[!UICONTROL Title]** `Product Name (Count Distinct)` en **[!UICONTROL External Id]** `product_name_count_distinct` .

![ berekende de productnaam van Customer Journey Analytics (Afzonderlijke Telling) metrisch ](assets/cja-calc-metric-distinct-count-product-names.png)

Vervolgens kunt u die metrische waarde gebruiken in een voorbeeldvenster van **[!UICONTROL Count Distinct Dimension Values]** voor het gebruik van hoofdletters en kleine letters:

![ de Afzonderlijke Waarden van de Telling van Customer Journey Analytics ](assets/cja-count-distinct-dimension-values.png)

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [ een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening ](#connect-and-validate) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. Sleep **[!UICONTROL daterangeday]** van het deelvenster **[!UICONTROL Data]** aan **[!UICONTROL Filters]** op deze pagina om ervoor te zorgen dat het datumbereik van toepassing is op alle visualisaties.
   1. Selecteer de **[!UICONTROL daterangeday is (All)]** van **[!UICONTROL Filters on this page]**.
   1. Selecteer **[!UICONTROL Advanced filtering]** als de **[!UICONTROL Filter type]** .
   1. Definieer het filter naar **[!UICONTROL Show items when the value]** **[!UICONTROL is on or after]** `1/1/2023` **[!UICONTROL And]** **[!UICONTROL is before]** `2/1/2023` .
   1. Selecteer **[!UICONTROL Apply filter]** .

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL datarangeday]** .
   1. Selecteer **[!UICONTROL sum cm_product_name_count_distinct]** . Dit is de berekende metrische waarde die in Customer Journey Analytics is gedefinieerd.

1. Als u het verticale staafdiagram wilt wijzigen in een tabel, zorgt u ervoor dat het diagram is geselecteerd en selecteert u **[!UICONTROL Table]** in het deelvenster **[!UICONTROL Visualizations]** .

   Je Power BI Desktop moet er hieronder uitzien.

   ![ de Veelvoudige Lijst van de Telling van Power BI van de Desktop Veelvoudige ](assets/uc7-powerbi-table.png)

1. Selecteer de tabelvisualisatie. Selecteer **[!UICONTROL Copy]** > **[!UICONTROL Copy visual]** in het contextmenu.
1. Plak de visualisatie met **[!UICONTROL ctrl-v]** . De exacte kopie van de visualisatie overlapt de originele versie. Verplaats het naar rechts in het rapportgebied.
1. Selecteer **[!UICONTROL Card]** in **[!UICONTROL Visualizations]** om de gekopieerde visualisatie van een tabel naar een kaart te wijzigen.

   Je Power BI Desktop moet er hieronder uitzien.

   ![ de Veelvoudige Lijst van de Telling van Power BI van de Desktop Veelvoudige ](assets/uc7-powerbi-final.png)

U kunt ook de functie Telling gebruiken, die anders is dan Power BI.

1. Selecteer de **[!UICONTROL product_name]** -dimensie.
1. Pas de functie **[!UICONTROL Count (Distinct)]** toe op de **[!UICONTROL product_name]** dimensie in **[!UICONTROL Columns]** .

   ![ de Telling van Power BI Distinct ](assets/uc7-powerbi-alternative.png)



>[!TAB  Desktop Tableau ]

1. Selecteer de tab **[!UICONTROL Sheet 1]** onderaan om te schakelen van **[!UICONTROL Data source]** . In de weergave **[!UICONTROL Sheet 1]** :
   1. Sleep de vermelding **[!UICONTROL Daterange]** uit de lijst **[!UICONTROL Tables]** in het deelvenster **[!UICONTROL Data]** en zet deze op de **[!UICONTROL Filters]** shelf neer.
   1. Selecteer **[!UICONTROL Filter Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer **[!UICONTROL Filter \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of dates]** en selecteer `01/01/2023` - `31/1/2023` . Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Sleep **[!UICONTROL Cm Product Name Count Distinct]** naar **[!UICONTROL Rows]** . De waarde verandert in **[!UICONTROL SUM(Cm Product Name Count Distinct)]** . Dit veld is de berekende maateenheid die u in Customer Journey Analytics hebt gedefinieerd.
   1. Sleep **[!UICONTROL Daterangeday]** en zet de muisknop los naast **[!UICONTROL Columns]** . Selecteer **[!UICONTROL Daterangeday]** en selecteer **[!UICONTROL Day]** in de vervolgkeuzelijst.
   1. Als u de lijnvisualisatie wilt wijzigen in een tabel, selecteert u **[!UICONTROL Text Table]** in **[!UICONTROL Show Me]** .
   1. Selecteer **[!UICONTROL Swap Rows and Columns]** op de werkbalk.
   1. Selecteer **[!UICONTROL Fit Width]** in de vervolgkeuzelijst **[!UICONTROL Fit]** .

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ de Veelvoudige Rangschikte Filter van de Desktop van Tableau Dimension ](assets/uc7-tableau-data.png)

1. Selecteer **[!UICONTROL Duplicate]** in het contextmenu van de tab **[!UICONTROL Sheet 1]** om een tweede blad te maken.
1. Selecteer **[!UICONTROL Rename]** in het contextmenu van de tab **[!UICONTROL Sheet 1]** om de naam van het werkblad te wijzigen in `Data` .
1. Selecteer **[!UICONTROL Rename]** in het contextmenu van de tab **[!UICONTROL Sheet 1 (2)]** om de naam van het werkblad te wijzigen in `Card` .

1. Controleer of u de weergave **[!UICONTROL Card]** hebt geselecteerd.
1. Selecteer **[!UICONTROL DAY(Daterangeday)]** en selecteer **[!UICONTROL Month]** in de vervolgkeuzelijst. De waarde verandert in **[!UICONTROL MONTH(Daterangeday)]** .
1. Selecteer **[!UICONTROL SUM(Cm Product Name Count Distinct)]** in **[!UICONTROL Marks]** en selecteer **[!UICONTROL Format]** in de vervolgkeuzelijst.
1. Als u de tekengrootte wilt wijzigen, selecteert u in het deelvenster **[!UICONTROL Format SUM(CM Product Name Count Distinct)]** de optie **[!UICONTROL Font]** within **[!UICONTROL Default]** en selecteert u **[!UICONTROL 72]** voor de tekengrootte.
1. Als u het getal wilt uitlijnen, selecteert u **[!UICONTROL Automatic]** naast **[!UICONTROL Alignment]** en stelt u **[!UICONTROL Horizontal]** in op gecentreerd.
1. Als u hele getallen wilt gebruiken, selecteert u **[!UICONTROL 123.456]** naast **[!UICONTROL Numbers]** en selecteert u **[!UICONTROL Number (Custom)]** . Stel **[!UICONTROL Decimal places]** in op `0` .

   Uw Tableau Desktop moet er hieronder uitzien.

   ![ de Veelvoudige Rangschikte Filter van de Desktop van Tableau Dimension ](assets/uc7-tableau-card.png)

1. Selecteer **[!UICONTROL New Dashboard]** tabknop (onder) om een nieuwe **[!UICONTROL Dashboard 1]** -weergave te maken. In de weergave **[!UICONTROL Dashboard 1]** :
   1. Sleep en laat vallen het **[!UICONTROL Card]** blad van **[!UICONTROL Sheets]** plank op de **[!UICONTROL Dashboard 1]** mening die *Dropbladen hier* leest.
   1. Sleep het **[!UICONTROL Data]** -werkblad vanuit de **[!UICONTROL Sheets]** -plank onder het **[!UICONTROL Card]** -werkblad in de **[!UICONTROL Dashboard 1]** -weergave.

   De weergave **[!UICONTROL Dashboard 1]** ziet er hieronder ongeveer zo uit.

   ![ Dashboard 1 van de Desktop van Tableau ](assets/uc7-tableau-final.png)


Alternatief, kunt u de telling verschillende functionaliteit van Desktop gebruiken Tableau.

1. Gebruik **[!UICONTROL Product Name]** in plaats van **[!UICONTROL Cm Product Name Count Distinct]** .
1. Pas **[!UICONTROL Measure]** > **[!UICONTROL Count (Distinct)]** on **[!UICONTROL Product Name]** toe in **[!UICONTROL Marks]** .

   ![ Afzonderlijke Telling van Tableau ](assets/uc7-tableau-alternative.png)


>[!TAB  Leider ]

1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![ Plaatsende ](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![ filter van de Leider ](assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2023/02/01]** .
1. Vanuit het gedeelte **[!UICONTROL ‣ Cc Data View]** in de linkertrack:
   1. Selecteer **[!UICONTROL Daterange Date]** en vervolgens **[!UICONTROL Date]** .
   1. Selecteer **[!UICONTROL Aggregate ‣ Count Distinct]** in het contextmenu **⋮ Meer** in **[!UICONTROL Product Name]** .
      ![ het Contextmenu van de Naam van het Product van de Leider ](assets/uc7-looker-count-distinct.png)
1. Selecteer **[!UICONTROL Run]** .
1. Selecteer **[!UICONTROL ‣ Visualization]** en selecteer 6︎⃣ op de werkbalk om één waardenvisualisatie weer te geven.

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![ minder duidelijke telling ](assets/uc7-looker-result.png)


>[!TAB  Jupyter Notitieboekje ]

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   data = %sql SELECT COUNT(DISTINCT(product_name)) AS `Product Name` \
      FROM cc_data_view \
      WHERE daterange BETWEEN '2023-01-01' AND '2023-02-01';
   display(data)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc7-jupyter-results.png)


>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ```{r} ` en ` ``` ` in een nieuw segment in.

   ```R
   ## Count Distinct
   df <- dv %>%
      filter(daterange >= "2023-01-01" & daterange < "2023-02-01") %>%
      summarise(product_name_count_distinct = n_distinct(product_name))
   print(df)
   ```

1. Voer het segment uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Resultaten RStudio ](assets/uc7-rstudio-results.png)


>[!ENDTABS]

+++


## Namen van datumbereik gebruiken om te filteren

In dit geval wilt u een datumbereik gebruiken dat u in Customer Journey Analytics hebt gedefinieerd om gebeurtenissen (gebeurtenissen) in het laatste jaar te filteren en te rapporteren.

+++ Customer Journey Analytics

Als u een datumbereik wilt rapporteren, stelt u in Customer Journey Analytics een datumbereik in met **[!UICONTROL Title]** `Last Year 2023` .

![ de Namen van de Datumwaaier van het Gebruik van Customer Journey Analytics aan filter ](assets/cja-daterange.png)

Vervolgens kunt u dat datumbereik gebruiken in een voorbeelddeelvenster **[!UICONTROL Using Date Range Names To Filter]** voor het gebruik van hoofdletters en kleine letters:

![ de Afzonderlijke Waarden van de Telling van Customer Journey Analytics ](assets/cja-using-date-range-filter-names-to-filter.png)

Bedenk hoe het datumbereik dat in de visualisatie van de tabel Freeform is gedefinieerd, het datumbereik overtreft dat op het deelvenster wordt toegepast.

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [ een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening ](#connect-and-validate) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL daterangemonth]** .
   1. Selecteer **[!UICONTROL daterangeName]** .
   1. Selecteer **[!UICONTROL sum occurrences]** .

   Er wordt een visualisatie weergegeven **[!UICONTROL Error fetching data for this visual]** .

1. In het deelvenster **[!UICONTROL Filters]** :

   1. Selecteer de **[!UICONTROL daterangeName is (All)]** van **[!UICONTROL Filters on this visual]**.
   1. Selecteer **[!UICONTROL Basic filtering]** als de **[!UICONTROL Filter type]** .
   1. Onder het veld **[!UICONTROL Search]** selecteert u **[!UICONTROL Last Year 2023]** . Dit is de naam van het datumbereik dat in Customer Journey Analytics is gedefinieerd.
   1. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om **[!UICONTROL daterangeName]** uit **[!UICONTROL Columns]** te verwijderen.

   De tabel wordt bijgewerkt met het toegepaste filter **[!UICONTROL daterangeName]** . Je Power BI Desktop moet er hieronder uitzien.

   ![ Desktop die van Power BI de Namen van de Waaier van de Datum gebruikt om te filtreren ](assets/uc8-powerbi-final.png)

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

      ![ de Veelvoudige Rangschikte Filter van de Desktop van Tableau Dimension ](assets/uc8-tableau-final.png)

>[!TAB  Leider ]

1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![ Plaatsende ](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Name]** in de lijst met velden.
1. Geef het filter **[!UICONTROL Cc Data View Daterange Name]** op als **[!UICONTROL is]** en selecteer **[!UICONTROL Last Year 2023]** in de lijst met waarden.
1. Vanuit het gedeelte **[!UICONTROL ‣ Cc Data View]** in de linkertrack:
   1. Selecteer **[!UICONTROL Daterange Month]** en vervolgens **[!UICONTROL Month]** .
   1. Selecteer **[!UICONTROL Count]** onder **[!UICONTROL MEASURES]** in de linkertrack (onder).
1. Selecteer **[!UICONTROL Run]** .
1. Selecteer **[!UICONTROL ‣ Visualization]** .

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![ minder duidelijke telling ](assets/uc8-looker-result.png)


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

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc8-jupyter-input.png)

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

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc8-jupyter-results.png)


>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ```{r} ` en ` ``` ` in een nieuw segment in. Zorg ervoor dat u de juiste naam voor het datumbereik gebruikt. Bijvoorbeeld `Last Year 2023` .

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

   ![ Resultaten RStudio ](assets/uc8-rstudio-results.png)

>[!ENDTABS]

+++



## Segmentnamen gebruiken

In dit geval wilt u een bestaand segment gebruiken voor de categorie visserijproducten die u in Customer Journey Analytics hebt gedefinieerd. Segmenteren en rapporteren over productnamen en voorvallen (gebeurtenissen) in januari 2023.

+++ Customer Journey Analytics

Controleer het segment dat u in Customer Journey Analytics wilt gebruiken.

![ Customer Journey Analytics gebruiken de Namen van de Filter ](assets/cja-fishing-products.png)

Vervolgens kunt u dat segment in een voorbeeldvenster van **[!UICONTROL Using Segment Names To Segment]** gebruiken voor het gebruik van hoofdletters en kleine letters:

![ de Afzonderlijke Waarden van de Telling van Customer Journey Analytics ](assets/cja-using-filter-names-to-filter.png)

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [ een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening ](#connect-and-validate) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL daterange]** .
   1. Selecteer **[!UICONTROL filterName]** .
   1. Selecteer **[!UICONTROL product_name]** .
   1. Selecteer **[!UICONTROL sum occurrences]** .

Er wordt een visualisatie weergegeven **[!UICONTROL Error fetching data for this visual]** .

1. In het deelvenster **[!UICONTROL Filters]** :

   1. Selecteer **[!UICONTROL filterName is (All)]** in **[!UICONTROL Filters on this visual]** .
   1. Selecteer **[!UICONTROL Basic filtering]** als de **[!UICONTROL Filter type]** .
   1. Onder het veld **[!UICONTROL Search]** selecteert u **[!UICONTROL Fishing Products]** . Dit is de naam van het bestaande filter dat in Customer Journey Analytics is gedefinieerd.
   1. Selecteer **[!UICONTROL daterange is (All)]** in **[!UICONTROL Filters on this visual]** .
   1. Selecteer **[!UICONTROL Advanced filtering]** als de **[!UICONTROL Filter type]** .
   1. Definieer het filter naar **[!UICONTROL Show items when the value]** **[!UICONTROL is on or after]** `1/1/2023` **[!UICONTROL And]** **[!UICONTROL is before]** `2/1/2023` .
   1. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om **[!UICONTROL filterName]** uit **[!UICONTROL Columns]** te verwijderen.
   1. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om **[!UICONTROL daterange]** uit **[!UICONTROL Columns]** te verwijderen.

   De tabel wordt bijgewerkt met het toegepaste filter **[!UICONTROL filterName]** . Je Power BI Desktop moet er hieronder uitzien.

   ![ Desktop die van Power BI de Namen van de Waaier van de Datum gebruikt om te filtreren ](assets/uc9-powerbi-final.png)


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

      ![ de Veelvoudige Rangschikte Filter van de Desktop van Tableau Dimension ](assets/uc9-tableau-final.png)

>[!TAB  Leider ]

1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![ Plaatsende ](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![ filter van de Leider ](assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2023/02/01]** .
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** om nog een filter toe te voegen.
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Filter name]** in de lijst met velden.
1. Controleer **[!UICONTROL is]** de selectie voor het filter.
1. Selecteer **[!UICONTROL Fishing Products]** in de lijst met mogelijke waarden.
1. Vanuit het gedeelte **[!UICONTROL ‣ Cc Data View]** in de linkertrack:
   1. Selecteer **[!UICONTROL Product Name]** .
   1. Selecteer **[!UICONTROL Count]** onder **[!UICONTROL MEASURES]** in de linkertrack (onder).
1. Selecteer **[!UICONTROL Run]** .
1. Selecteer **[!UICONTROL ‣ Visualization]** .

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![ minder duidelijke telling ](assets/uc9-looker-result.png)



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

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc9-jupyter-input.png)

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

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc9-jupyter-results.png)


>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ```{r} ` en ` ``` ` in een nieuw segment in. Controleer of u de juiste filternaam gebruikt. Bijvoorbeeld `Fishing Products` .

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

   ![ Resultaten RStudio ](assets/uc9-rstudio-results.png)


>[!ENDTABS]

+++


## Dimensiewaarden gebruiken om te segmenteren

U gebruikt de dynamische **[!UICONTROL Hunting]** waarde voor **[!UICONTROL Product Category]** om producten van de jachtcategorie te segmenteren. U kunt ook voor de BI-gereedschappen die het dynamisch ophalen van productcategoriewaarden niet ondersteunen, een nieuw segment in Customer Journey Analytics maken dat zich segmenteert op producten uit de categorie jachtproducten.
Vervolgens wilt u het nieuwe segment gebruiken om productnamen en voorvallen (voorvallen) te rapporteren voor producten uit de jachtcategorie in januari 2023.

+++ Customer Journey Analytics

Maak een nieuw segment met **[!UICONTROL Title]** `Hunting Products` in Customer Journey Analytics.

![ de Waarden van Dimension van het Gebruik van Customer Journey Analytics aan segment ](assets/cja-hunting-products.png)

Vervolgens kunt u dat segment in een voorbeeldvenster van **[!UICONTROL Using Dimension Values To Filter]** gebruiken voor het gebruik van hoofdletters en kleine letters:

![ de Afzonderlijke Waarden van de Telling van Customer Journey Analytics ](assets/cja-using-dimension-values-to-filter.png)

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [ een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening ](#connect-and-validate) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. Selecteer **[!UICONTROL Home]** in het menu en selecteer vervolgens **[!UICONTROL Refresh]** op de werkbalk. U moet de verbinding vernieuwen om het nieuwe filter op te halen dat u net in Customer Journey Analytics hebt gedefinieerd.

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL daterange]** .
   1. Selecteer **[!UICONTROL product_category]** .
   1. Selecteer **[!UICONTROL product_name]** .
   1. Selecteer **[!UICONTROL sum occurrences]** .

Er wordt een visualisatie weergegeven **[!UICONTROL Error fetching data for this visual]** .

1. In het deelvenster **[!UICONTROL Filters]** :
   1. Selecteer **[!UICONTROL filterName is (All)]** in **[!UICONTROL Filters on this visual]** .
   1. Selecteer **[!UICONTROL Basic filtering]** als de **[!UICONTROL Filter type]** .
   1. Selecteer **[!UICONTROL daterange is (All)]** in **[!UICONTROL Filters on this visual]** .
   1. Selecteer **[!UICONTROL Advanced filtering]** als de **[!UICONTROL Filter type]** .
   1. Definieer het filter naar **[!UICONTROL Show items when the value]** **[!UICONTROL is on or after]** `1/1/2023` **[!UICONTROL And]** **[!UICONTROL is before]** `2/1/2023` .
   1. Selecteer **[!UICONTROL Basic filter]** als de **[!UICONTROL Filter type]** for **[!UICONTROL product_category]** en selecteer **[!UICONTROL Hunting]** in de lijst met mogelijke waarden.
   1. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om **[!UICONTROL filterName]** uit **[!UICONTROL Columns]** te verwijderen.
   1. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om **[!UICONTROL daterange]** uit **[!UICONTROL Columns]** te verwijderen.

   De tabel wordt bijgewerkt met het toegepaste filter **[!UICONTROL product_category]** . Je Power BI Desktop moet er hieronder uitzien.

   ![ Desktop die van Power BI de Namen van de Waaier van de Datum gebruikt om te filtreren ](assets/uc10-powerbi-final.png)



>[!TAB  Desktop Tableau ]

![ AlertRed ](/help/assets/icons/AlertRed.svg) Desktop van Tableau steunt het halen van de dynamische lijst van productcategorieën van Customer Journey Analytics niet. In plaats daarvan wordt in dit geval het nieuwe filter voor **[!UICONTROL Hunting Products]** gebruikt en worden de criteria voor de filternaam gebruikt.

1. Selecteer **[!UICONTROL Data Source]** onder **[!UICONTROL Data]** in de **[!UICONTROL cc_data_view(prod:cja%3FFLATTEN)]** -weergave in het contextmenu op **[!UICONTROL Refresh]** . U moet de verbinding vernieuwen om het nieuwe filter op te halen dat u net in Customer Journey Analytics hebt gedefinieerd.
1. Selecteer de tab **[!UICONTROL Sheet 1]** onderaan om te schakelen van **[!UICONTROL Data source]** . In de weergave **[!UICONTROL Sheet 1]** :
   1. Sleep de vermelding **[!UICONTROL Filter Name]** uit de lijst **[!UICONTROL Tables]** in de lijst **[!UICONTROL Filters]** .
   1. Controleer in het dialoogvenster **[!UICONTROL Filter \[Filter Name\]]** of **[!UICONTROL Select from list]** is geselecteerd en selecteer **[!UICONTROL Hunting Products]** in de lijst. Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Sleep **[!UICONTROL Daterange]** -item uit de lijst **[!UICONTROL Tables]** in de **[!UICONTROL Filters]** -lijst.
   1. Selecteer **[!UICONTROL Filter Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer **[!UICONTROL Filter \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of dates]** en selecteer `01/01/2023` - `1/2/2023` . Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Sleep **[!UICONTROL Product Name]** van de **[!UICONTROL Tables]** lijst aan **[!UICONTROL Rows]**.
   1. Sleep **[!UICONTROL Occurrences]** -item uit de **[!UICONTROL Tables]** -lijst en zet de vermelding in het veld naast **[!UICONTROL Columns]** neer. De waarde verandert in **[!UICONTROL SUM(Occurrences)]** .
   1. Selecteer **[!UICONTROL Text Table]** in **[!UICONTROL Show Me]** .
   1. Selecteer **[!UICONTROL Fit Width]** in de vervolgkeuzelijst **[!UICONTROL Fit]** .

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ de Veelvoudige Rangschikte Filter van de Desktop van Tableau Dimension ](assets/uc10-tableau-final.png)

>[!TAB  Leider ]

1. In de 1. Vernieuw de verbinding in de **[!UICONTROL Explore]** -interface van Looker. Selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) **[!UICONTROL Clear cache and refresh]**.
1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![ Plaatsende ](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![ filter van de Leider ](assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2023/02/01]** .
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** om nog een filter toe te voegen.
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Product Category]** in de lijst met velden.
1. Controleer **[!UICONTROL is]** als de selectie voor het filter.

![ AlertRed ](/help/assets/icons/AlertRed.svg) Lijnen toont niet de lijst van mogelijke waarden voor **[!UICONTROL Product Category]**.

![ minder duidelijke telling ](assets/uc10-looker-result.png)


>[!TAB  Jupyter Notitieboekje ]

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   data = %sql SELECT DISTINCT product_category FROM cc_data_view WHERE daterange BETWEEN '2023-01-01' AND '2024-01-01';
   style = {'description_width': 'initial'}
   category_filter = widgets.Dropdown(
      options=[d for d, in data],
      description='Product Category:',
      style=style
   )
   display(category_filter)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc10-jupyter-input.png)

1. Selecteer **[!UICONTROL Hunting]** in de vervolgkeuzelijst.

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   import seaborn as sns
   import matplotlib.pyplot as plt
   data = %sql SELECT product_name AS `Product Name`, COUNT(*) AS Events \
               FROM cc_data_view \
               WHERE daterange BETWEEN '2023-01-01' AND '2023-02-01' \
               AND product_category = '{category_filter.value}' \
               GROUP BY 1 \
               ORDER BY Events DESC \
               LIMIT 10;
   df = data.DataFrame()
   df = df.groupby('Product Name', as_index=False).sum()
   plt.figure(figsize=(15, 3))
   sns.barplot(x='Events', y='Product Name', data=df)
   plt.show()
   display(data)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc10-jupyter-results.png)


>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ```{r} ` en ` ``` ` in een nieuw segment in. Gebruik de juiste categorie. Bijvoorbeeld `Hunting` .

   ```R
   ## Dimension 1 Filtered by Dimension 2 value
   df <- dv %>%
      filter(daterange >= "2023-01-01" & daterange < "2023-02-01" & product_category == "Hunting") %>%
      group_by(product_name) %>%
      count() %>%
      arrange(desc(n), .by_group = FALSE)
   print(df)
   ```

1. Voer het segment uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Resultaten RStudio ](assets/uc10-rstudio-results.png)

>[!ENDTABS]

+++



## Sorteren

In dit geval wilt u in januari 2023 voor productnamen de aankoopopbrengsten en -aankopen rapporteren, gesorteerd in aflopende inkoopopdracht.

+++ Customer Journey Analytics

Een voorbeeldvenster **[!UICONTROL Sort]** voor het hoofdlettergebruik:

![ het paneel van de Sortering van Customer Journey Analytics ](assets/cja-sort.png)

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [ een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening ](#connect-and-validate) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL daterange]** .
   1. Selecteer **[!UICONTROL product_namr]** .
   1. Selecteer **[!UICONTROL sum purchase_revenue]** .
   1. Selecteer **[!UICONTROL sum purchases]** .

1. In het deelvenster **[!UICONTROL Filters]** :
   1. Selecteer **[!UICONTROL daterange is (All)]** in **[!UICONTROL Filters on this visual]** .
   1. Selecteer **[!UICONTROL Advanced filtering]** als de **[!UICONTROL Filter type]** .
   1. Definieer het filter naar **[!UICONTROL Show items when the value]** **[!UICONTROL is on or after]** `1/1/2023` **[!UICONTROL And]** **[!UICONTROL is before]** `2/1/2023` .

1. In het deelvenster Visualisaties:
   1. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om daterange uit Kolommen te verwijderen.
   1. Sleep **[!UICONTROL Sum of purchase_revenue]** naar de onderkant van **[!UICONTROL Column]** -items.

1. Selecteer in het rapport **[!UICONTROL Sum of purchase_revenue]** om de tabel in aflopende volgorde van aankoop-inkomsten te sorteren.

   Je Power BI Desktop moet er hieronder uitzien.

   ![ Desktop die van Power BI de Namen van de Waaier van de Datum gebruikt om te filtreren ](assets/uc11-powerbi-final.png)

De query die door Power BI Desktop wordt uitgevoerd met de BI-extensie bevat geen `sort` -instructie. Het ontbreken van een instructie `sort` betekent dat de sortering aan de clientzijde wordt uitgevoerd.

```sql
select "_"."product_name",
    "_"."a0",
    "_"."a1"
from 
(
    select "rows"."product_name" as "product_name",
        sum("rows"."purchases") as "a0",
        sum("rows"."purchase_revenue") as "a1"
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
        where "_"."daterange" < date '2023-02-01' and "_"."daterange" >= date '2023-01-01'
    ) "rows"
    group by "product_name"
) "_"
where not "_"."a0" is null or not "_"."a1" is null
limit 1000001
```


>[!TAB  Desktop Tableau ]

1. Selecteer de tab **[!UICONTROL Sheet 1]** onderaan om te schakelen van **[!UICONTROL Data source]** . In de weergave **[!UICONTROL Sheet 1]** :
   1. Sleep **[!UICONTROL Daterange]** -item uit de lijst **[!UICONTROL Tables]** in de **[!UICONTROL Filters]** -lijst.
   1. Selecteer **[!UICONTROL Filter Field \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of Dates]** van **[!UICONTROL Next >]** .
   1. Selecteer **[!UICONTROL Filter \[Daterange\]]** in het dialoogvenster **[!UICONTROL Range of dates]** en selecteer `01/01/2023` - `1/2/2023` . Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .
   1. Sleep **[!UICONTROL Product Name]** uit de lijst **[!UICONTROL Tables]** en zet de vermelding neer in het veld naast **[!UICONTROL Rows]** .
   1. Sleep **[!UICONTROL Purchases]** -item uit de **[!UICONTROL Tables]** -lijst en zet de vermelding in het veld naast **[!UICONTROL Columns]** neer. De waarde verandert in **[!UICONTROL SUM(Purchases)]** .
   1. Sleep **[!UICONTROL Purchase Revenue]** -item uit de **[!UICONTROL Tables]** -lijst en zet de vermelding in het veld naast **[!UICONTROL Columns]** , naast **[!UICONTROL SUM(Purchases)]** . De waarde verandert in **[!UICONTROL SUM(Purchase Revenue)]** .
   1. Selecteer **[!UICONTROL Text Table]** in **[!UICONTROL Show Me]** .
   1. Selecteer **[!UICONTROL Fit Width]** in de vervolgkeuzelijst **[!UICONTROL Fit]** .
   1. Selecteer de kolomkop **[!UICONTROL Purchase Revenue]** en sorteer de tabel in deze kolom in aflopende volgorde.

      Uw Tableau Desktop moet er hieronder uitzien.

      ![ de Soort van de Desktop van Tableau ](assets/uc11-tableau-final.png)

De query die wordt uitgevoerd door Tableau Desktop met de BI-extensie bevat geen `sort` -instructie. Het ontbreken van deze instructie `sort` betekent dat de sortering aan de clientzijde wordt uitgevoerd.

```sql
SELECT CAST("cc_data_view"."product_name" AS TEXT) AS "product_name",
  SUM("cc_data_view"."occurrences") AS "sum:occurrences:ok",
  SUM("cc_data_view"."purchase_revenue") AS "sum:purchase_revenue:ok",
  SUM("cc_data_view"."purchases") AS "sum:purchases:ok"
FROM "public"."cc_data_view" "cc_data_view"
WHERE (("cc_data_view"."daterange" >= (DATE '2023-01-01')) AND ("cc_data_view"."daterange" <= (DATE '2023-02-01')))
GROUP BY 1
```

>[!TAB  Leider ]

1. Vernieuw de verbinding in de **[!UICONTROL Explore]** -interface van Looker. Selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) **[!UICONTROL Clear cache and refresh]**.
1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![ Plaatsende ](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![ filter van de Leider ](assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2023/02/01]** .
1. Selecteer **[!UICONTROL ‣ Cc Data View]** in het gedeelte **[!UICONTROL Product Name]** links in de sectie.
1. Vanuit het gedeelte **[!UICONTROL ‣ Custom Fields]** in de linkertrack:
   1. Selecteer **[!UICONTROL Custom Measure]** in de vervolgkeuzelijst **[!UICONTROL + Add]** .
   1. In het dialoogvenster **[!UICONTROL Create custom measure]** :
      1. Selecteer **[!UICONTROL Purchase Revenue]** in de vervolgkeuzelijst **[!UICONTROL Field to measure]** .
      1. Selecteer **[!UICONTROL Sum]** in de vervolgkeuzelijst **[!UICONTROL Measure type]** .
      1. Voer een aangepaste veldnaam in voor **[!UICONTROL Name]** . Bijvoorbeeld: `Sum of Purchase Revenue` .
      1. Selecteer de tab **[!UICONTROL Field details]** .
      1. Selecteer **[!UICONTROL Decimals]** in de vervolgkeuzelijst **[!UICONTROL Format]** en zorg ervoor dat `0` wordt ingevoerd in **[!UICONTROL Decimals]** .
         ![ Lager aangepast metrisch gebied ](assets/uc5-looker-customfield.png)
      1. Selecteer **[!UICONTROL Save]** .
1. Selecteer **[!UICONTROL ↓]** (**[!UICONTROL Descending, Sort Order: 1]** ) in de kolom **[!UICONTROL Purchase Revenue]** .
1. Selecteer **[!UICONTROL Run]** .
1. Selecteer **[!UICONTROL ‣ Visualization]** .

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![ minder duidelijke telling ](assets/uc11-looker-result.png)


De vraag die door het gebruiken van de uitbreiding van BI wordt geproduceerd van het plukker is met inbegrip van `ORDER BY`, wat impliceert dat de soort door de uitbreiding van het plukker en van BI wordt uitgevoerd.

```sql
-- Looker Query Context '{"user_id":6,"history_slug":"fc83573987b999306eaf6e1a3f2cde70","instance_slug":"71d4667f0b76c0011463658f45c3f7a3"}' 
SELECT
    cc_data_view."product_name"  AS "cc_data_view.product_name",
    COALESCE(SUM(CAST(( cc_data_view."purchase_revenue"  ) AS DOUBLE PRECISION)), 0) AS "purchase_revenue"
FROM
    "public"."cc_data_view" AS "cc_data_view"
WHERE ((( cc_data_view."daterange"  ) >= (DATE_TRUNC('day', DATE '2024-01-31')) AND ( cc_data_view."daterange"  ) < (DATE_TRUNC('day', DATE '2023-02-01'))))
GROUP BY
    1
ORDER BY
    2 DESC
FETCH NEXT 500 ROWS ONLY
```


>[!TAB  Jupyter Notitieboekje ]

1. Voer de volgende instructies in een nieuwe cel in.

   ```python
   data = %sql SELECT product_name AS `Product Name`, SUM(purchase_revenue) AS `Purchase Revenue`, SUM(purchases) AS `Purchases` \
               FROM cc_data_view \
               WHERE daterange BETWEEN '2023-01-01' AND '2023-02-01' \
               GROUP BY 1 \
               ORDER BY `Purchase Revenue` DESC \
               LIMIT 5;
   display(data)
   ```

1. Voer de cel uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc11-jupyter-results.png)

De query wordt uitgevoerd door de BI-extensie zoals gedefinieerd in Jupyter Notebook.


>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ```{r} ` en ` ``` ` in een nieuw segment in.

   ```R
   ## Dimension 1 Sorted
   df <- dv %>%
      filter(daterange >= "2023-01-01" & daterange < "2023-02-01") %>%
      group_by(product_name) %>%
      summarise(purchase_revenue = sum(purchase_revenue), purchases = sum(purchases), .groups = "keep") %>%
      arrange(desc(purchase_revenue), .by_group = FALSE)
   print(df)
   ```

1. Voer het segment uit. U zou output moeten zien gelijkend op het hieronder opgenomen schermschot.

   ![ Resultaten RStudio ](assets/uc11-rstudio-results.png)

De query die wordt gegenereerd door RStudio met de BI-extensie bevat `ORDER BY` . Dit houdt in dat de volgorde wordt toegepast via RStudio en de BI-extensie.

```sql
SELECT
  "product_name",
  SUM("purchase_revenue") AS "purchase_revenue",
  SUM("purchases") AS "purchases"
FROM (
  SELECT "cc_data_view".*
  FROM "cc_data_view"
  WHERE ("daterange" >= '2023-01-01' AND "daterange" < '2023-02-01')
) AS "q01"
GROUP BY "product_name"
ORDER BY "purchase_revenue" DESC
LIMIT 1000
```

>[!ENDTABS]

+++

## Limieten

In dit geval, wilt u over de hoogste 5 voorkomen van productnamen tijdens 2023 rapporteren.

+++ Customer Journey Analytics

Een voorbeeldvenster **[!UICONTROL Limit]** voor het hoofdlettergebruik:

![ het paneel van de Grens van Customer Journey Analytics ](assets/cja-limit.png)

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [ een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening ](#connect-and-validate) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
>

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

1. In het deelvenster **[!UICONTROL Data]** :
   1. Selecteer **[!UICONTROL daterange]** .
   1. Selecteer **[!UICONTROL product_name]** .
   1. Selecteer **[!UICONTROL sum occurrences]** .

1. In het deelvenster **[!UICONTROL Filters]** :
   1. Selecteer **[!UICONTROL daterange is (All)]** in **[!UICONTROL Filters on this visual]** .
   1. Selecteer **[!UICONTROL Relative date]** als de **[!UICONTROL Filter type]** .
   1. Definieer het filter naar **[!UICONTROL Show items when the value]** **[!UICONTROL is in the last]** `1` **[!UICONTROL calendar years]** .
   1. Selecteer **[!UICONTROL Apply filter]** .
   1. Selecteer **[!UICONTROL product_name is (All)]** in **[!UICONTROL Filters on this visual]** .
   1. Selecteer **[!UICONTROL Top N]** als de **[!UICONTROL Filter type]** .
   1. Selecteer **[!UICONTROL Show Items]** **[!UICONTROL Top]** `5` **[!UICONTROL By value]** .
   1. Sleep **[!UICONTROL sum occurrences]** vanuit het deelvenster **[!UICONTROL Data]** en zet het neer op **[!UICONTROL Add data fields here]** .
   1. Selecteer **[!UICONTROL Apply filter]** .

1. In het deelvenster Visualisatie:
   * Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om daterange uit Kolommen te verwijderen.

   Je Power BI Desktop moet er hieronder uitzien.

   ![ Desktop die van Power BI de Namen van de Waaier van de Datum gebruikt om te filtreren ](assets/uc12-powerbi-final.png)

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

         ![ AlertRed ](/help/assets/icons/AlertRed.svg) u merkt dat de lijst verdwijnt. Het selecteren van top 5 productnamen door voorkomen werkt **niet** behoorlijk gebruikend deze filter.
      1. Selecteer **[!UICONTROL Product Name]** in de **[!UICONTROL Filter]** plank en van het drop-down menu uitgezocht **[!UICONTROL Remove]**. De tabel wordt opnieuw weergegeven.
   1. Selecteer **[!UICONTROL SUM(Occurrences)]** in de **[!UICONTROL Marks]** -plank. Selecteer **[!UICONTROL Filter]** in de vervolgkeuzelijst.
      1. Selecteer **[!UICONTROL Filter \[Occurrences\]]** in het dialoogvenster **[!UICONTROL At least]** .
      1. Voer `47.799` in als waarde. Deze waarde zorgt ervoor dat alleen de bovenste 5 items in de tabel worden weergegeven. Selecteer **[!UICONTROL Apply]** en **[!UICONTROL OK]** .

         Uw Tableau Desktop moet er hieronder uitzien.

         ![ Limieten van de Desktop van Tableau ](assets/uc12-tableau-final.png)

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

1. Vernieuw de verbinding in de **[!UICONTROL Explore]** -interface van Looker. Selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) **[!UICONTROL Clear cache and refresh]**.
1. Zorg ervoor dat u in de interface **[!UICONTROL Explore]** van Looker een schone instelling hebt. Als niet, uitgezochte ![ Plaatsende ](/help/assets/icons/Setting.svg) **[!UICONTROL Remove fields and filters]**.
1. Selecteer **[!UICONTROL + Filter]** onder **[!UICONTROL Filters]** .
1. In het dialoogvenster **[!UICONTROL Add Filter]** :
   1. Selecteren **[!UICONTROL ‣ Cc Data View]**
   1. Selecteer **[!UICONTROL ‣ Daterange Date]** en vervolgens **[!UICONTROL Daterange Date]** in de lijst met velden.
      ![ filter van de Leider ](assets/uc2-looker-filter.png)
1. Geef het filter **[!UICONTROL Cc Data View Daterange Date]** op als **[!UICONTROL is in range]** **[!UICONTROL 2023/01/01]** **[!UICONTROL until (before)]** **[!UICONTROL 2024/01/01]** .
1. Vanuit het gedeelte **[!UICONTROL ‣ Cc Data View]** in de linkertrack:
   1. Selecteer **[!UICONTROL Product Name]** .
   1. Selecteer **[!UICONTROL Count]** onder **[!UICONTROL MEASURES]** in de linkertrack (onder).
1. Selecteer **[!UICONTROL ↓]** (**[!UICONTROL Descending, Sort Order: 1]** ) in de kolom **[!UICONTROL Purchase Revenue]** .
1. Selecteer **[!UICONTROL ↓]** (**[!UICONTROL Descending, Sort Order: 1]** ) in de kolom **[!UICONTROL Purchase Revenue]** .
1. Selecteer **[!UICONTROL Run]** .
1. Selecteer **[!UICONTROL ‣ Visualization]** .

U dient een visualisatie en tabel te zien zoals hieronder weergegeven.

![ minder duidelijke telling ](assets/uc12-looker-result.png)

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

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc12-jupyter-results.png)

De query wordt uitgevoerd door de BI-extensie zoals gedefinieerd in Jupyter Notebook.

>[!TAB  RStudio ]

1. Voer de volgende instructies tussen ` ```{r} ` en ` ``` ` in een nieuw segment in.

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

   ![ Resultaten RStudio ](assets/uc12-rstudio-results.png)

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

## Transformaties

U wilt de transformaties van de voorwerpen van Customer Journey Analytics zoals afmetingen, metriek, filters, berekende metriek, en datumwaaiers door de diverse hulpmiddelen van BI begrijpen.

+++ Customer Journey Analytics

In Customer Journey Analytics, bepaalt u in a [ gegevensmening ](/help/data-views/data-views.md), die en hoe de componenten van uw datasets als [ dimensies ](/help/components/dimensions/overview.md) en [ metriek ](/help/components/apply-create-metrics.md) worden blootgesteld. Die definitie van dimensie en metriek wordt blootgesteld aan de hulpmiddelen van BI gebruikend de uitbreiding van BI.
U gebruikt componenten zoals [ Filters ](/help/components/segments/seg-overview.md), [ Berekende metriek ](/help/components/calc-metrics/calc-metr-overview.md), en [ de waaiers van de Datum ](/help/components/date-ranges/overview.md) als deel van uw projecten van Workspace. Deze componenten worden ook blootgesteld aan de hulpmiddelen van BI gebruikend de uitbreiding van BI.

+++

+++ BI-gereedschappen

>[!PREREQUISITES]
>
>Verzeker u [ een succesvolle verbinding, gegevensmeningen, en gebruik een gegevensmening ](#connect-and-validate) voor het hulpmiddel van BI hebt bevestigd waarvoor u dit gebruiksgeval wilt uitproberen.
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
   ![ de Transformatie van de Desktop van Power BI aan Laag ](assets/uc14-powerbi-transformation.png)
1. Selecteer de nieuwe kolom **[!UICONTROL product_name_lower]** in het deelvenster **[!UICONTROL Data]** in plaats van de kolom **[!UICONTROL product_name]** .
1. Selecteer **[!UICONTROL Report as Table]** van ![ Meer ](/help/assets/icons/More.svg) in de lijstvisualisatie.

   Je Power BI Desktop moet er hieronder uitzien.
   ![ Definitieve Transformatie van de Desktop van Power BI ](assets/uc14-powerbi-final.png)

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
      ![ Berekend Gebied van Tableau ](assets/uc14-tableau-calculated-field.png)
   1. Selecteer **[!UICONTROL OK]** .
1. Selecteer het **[!UICONTROL Data]** blad.
   1. Sleep **[!UICONTROL Lowercase Product Name]** van **[!UICONTROL Tables]** en laat vallen de ingang in het gebied naast **[!UICONTROL Rows]**.
   1. Verwijder **[!UICONTROL Product Name]** uit **[!UICONTROL Rows]** .
1. Selecteer **[!UICONTROL Dashboard 1]** weergave.

Uw Tableau Desktop moet er hieronder uitzien.

![ Desktop Tableau na transformatie ](assets/uc14-tableau-final.png)

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
      ![ de transformatievoorbeeld van de Leider ](assets/uc14-looker-transformation.png)
   1. Voer `product name` in als de **[!UICONTROL Name]** .
   1. Selecteer **[!UICONTROL Save]** .

U dient een vergelijkbare tabel te zien zoals hieronder weergegeven.

![ Lager transformatieresultaat ](assets/uc14-looker-result.png)


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

   ![ Jupyter de Resultaten van het Notitieboekje ](assets/uc13-jupyter-results.png)

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

   ![ Resultaten RStudio ](assets/uc13-rstudio-results.png)

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



## Visualisaties

U wilt begrijpen hoe de visualisaties, beschikbaar in Customer Journey Analytics, op dezelfde manier kunnen worden gemaakt met de beschikbare visualisaties in de BI-gereedschappen.

+++ Customer Journey Analytics

Customer Journey Analytics heeft een aantal visualisaties. Zie [ Visualisaties ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md) voor een inleiding en een overzicht van alle mogelijke visualisaties.

+++

+++ BI-gereedschappen

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

### Vergelijking

Voor de meeste Customer Journey Analytics-visualisaties biedt Power BI Desktop vergelijkbare ervaringen. Zie de onderstaande tabel.

| Pictogram | Customer Journey Analytics visualisatie | Power BI Desktop visualisatie |
| :---: | --- | ---| 
| ![ GraphArea ](/help/assets/icons/GraphArea.svg) | [ Gebied ](/help/analysis-workspace/visualizations/area.md) | [ grafiek van het Gebied, gestapelde gebiedsgrafiek en 100% gebiedsgrafiek ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#area-charts-basic-layered-and-stacked) |
| ![ GraphBarVertical ](/help/assets/icons/GraphBarVertical.svg) | [ Bar ](/help/analysis-workspace/visualizations/bar.md) | [ Gegroepeerd kolomgrafiek ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#bar-and-column-charts) |
| ![ GraphBarVertical ](/help/assets/icons/GraphBarVerticalStacked.svg) | [ Gestapelde Bar ](/help/analysis-workspace/visualizations/bar.md) | [ Gestapelde kolomgrafiek en 100% gestapelde kolomgrafiek ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#bar-and-column-charts) |
| ![ GraphBullet ](/help/assets/icons/GraphBullet.svg)</p> | [ Opsommingsteken ](/help/analysis-workspace/visualizations/bullet-graph.md) |  |
| ![ TextNumbered ](/help/assets/icons/TextNumbered.svg) | [ Lijst van de Cohort ](/help/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) |  |
| ![ Combo ](/help/assets/icons/ComboChart.svg) | [ Combo ](/help/analysis-workspace/visualizations/combo-charts.md) | [ Lijn en gestapelde kolomgrafiek en Lijn en gegroepeerde kolomgrafiek ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#combo-charts) |
| ![ GraphDonut ](/help/assets/icons/GraphDonut.svg) | [Cirkeldiagram](/help/analysis-workspace/visualizations/donut.md) | [ grafiek van de Donut ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#doughnut-charts) |
| ![ ConversionFunnel ](/help/assets/icons/ConversionFunnel.svg) | [Uitval](/help/analysis-workspace/visualizations/fallout/fallout-flow.md) | [ Trechter ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#funnel-charts). |
| ![ GraphPathing ](/help/assets/icons/GraphPathing.svg) | [Stroom](/help/analysis-workspace/visualizations/c-flow/flow.md) | Boom ontbinden? |
| ![ ViewTable ](/help/assets/icons/ViewTable.svg)</p> | [Vrije-vormentabel](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) | [ Lijst ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#tables) en [ Matrijs ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#matrix) |
| ![ GraphHistogram ](/help/assets/icons/Histogram.svg) | [Histogram](/help/analysis-workspace/visualizations/histogram.md) |  |
| ![ GraphBarHorizontal ](/help/assets/icons/GraphBarHorizontal.svg) | [ Horizontale bar ](/help/analysis-workspace/visualizations/horizontal-bar.md) | [ Gegroepeerd staafdiagram ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#bar-and-column-charts) |
| ![ GraphBarHorizontalGestapeld ](/help/assets/icons/GraphBarHorizontalStacked.svg) | [ Horizontale gestapelde bar ](/help/analysis-workspace/visualizations/horizontal-bar.md) | [ Gestapeld staafdiagram en 100% gestapeld staafdiagram ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#bar-and-column-charts) |
| ![ Branch3 ](/help/assets/icons/Branch3.svg) | [ het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md) | [ Decomposition boom ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#decomposition-tree) |
| ![ KeyMetrics ](/help/assets/icons/KeyMetrics.svg) | [ Zeer belangrijke metrische samenvatting ](/help/analysis-workspace/visualizations/key-metric.md) |  |
| ![ GraphTrend ](/help/assets/icons/GraphTrend.svg) | [Lijn](/help/analysis-workspace/visualizations/line.md) | [ grafiek van de Lijn ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#line-charts) |
| ![ GraphScatter ](/help/assets/icons/GraphScatter.svg) | [ Spreiding ](/help/analysis-workspace/visualizations/scatterplot.md) | [ Spreidingsgrafiek ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#scatter) |
| ![ PageRule ](/help/assets/icons/PageRule.svg) | [ kopbal van de Sectie ](/help/analysis-workspace/visualizations/section-header.md) | [ doos van de Tekst ](https://learn.microsoft.com/en-us/power-bi/paginated-reports/report-design/textbox/add-move-or-delete-a-text-box-report-builder-and-service) |
| ![ MoveUpDown ](/help/assets/icons/MoveUpDown.svg) | [ Summiere verandering ](/help/analysis-workspace/visualizations/summary-number-change.md) | [ Kaart ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#cards) |
| ![ 123 ](/help/assets/icons/123.svg)</p> | [ Summiere aantal ](/help/analysis-workspace/visualizations/summary-number-change.md) | [ Kaart ](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#cards) |
| ![Tekst](/help/assets/icons/Text.svg) | [Tekst](/help/analysis-workspace/visualizations/text.md) | [ doos van de Tekst ](https://learn.microsoft.com/en-us/power-bi/paginated-reports/report-design/textbox/add-move-or-delete-a-text-box-report-builder-and-service) |
| ![ ModernGridView ](/help/assets/icons/ModernGridView.svg) | [Boomstructuur](/help/analysis-workspace/visualizations/treemap.md)<p> | [Boomstructuur](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-types-for-reports-and-q-and-a#treemaps) |
| ![ Type ](/help/assets/icons/TwoDots.svg) | [Venn](/help/analysis-workspace/visualizations/venn.md) | |


### Boor omlaag

Power BI steunt de wijze van de a [ boor ](https://learn.microsoft.com/en-us/power-bi/consumer/end-user-drill) om diepgaande details op bepaalde visualisaties te onderzoeken. In het onderstaande voorbeeld analyseert u de aankoopopbrengsten voor productcategorieën. In het contextmenu van een balk die een productcategorie voorstelt, kunt u **[!UICONTROL Drill down]** selecteren.

![ Power BI boor neer ](assets/uc15-powerbi-drilldown.png)

Met de optie Omlaag kunt u de visualisatie bijwerken met aankoopopbrengsten voor producten binnen de geselecteerde productcategorie.

![ boor van Power BI omhoog ](assets/uc15-powerbi-drillup.png)

De boor neer resulteert in de volgende SQL vraag die een `WHERE` clausule gebruikt:

```sql
select "_"."product_category" as "c25",
    "_"."product_name" as "c26",
    "_"."a0" as "a0"
from 
(
    select "_"."product_category",
        "_"."product_name",
        "_"."a0"
    from 
    (
        select "_"."product_category",
            "_"."product_name",
            "_"."a0"
        from 
        (
            select "rows"."product_category" as "product_category",
                "rows"."product_name" as "product_name",
                sum("rows"."purchase_revenue") as "a0"
            from 
            (
                select "_"."product_category",
                    "_"."product_name",
                    "_"."purchase_revenue"
                from "public"."cc_data_view" "_"
                where ("_"."daterange" >= date '2023-01-01' and "_"."product_category" = 'Fishing') and "_"."daterange" < date '2024-01-01'
            ) "rows"
            group by "product_category",
                "product_name"
        ) "_"
        where not "_"."a0" is null
    ) "_"
) "_"
order by "_"."product_category",
        "_"."product_name"
limit 1001
```

>[!TAB  Desktop Tableau ]

### Vergelijking

Voor de meeste Customer Journey Analytics-visualisaties biedt Tableau Desktop vergelijkbare ervaringen. Zie de onderstaande tabel.

| Pictogram | Customer Journey Analytics visualisatie | Power BI Desktop visualisatie |
| :---: | --- | ---| 
| ![ GraphArea ](/help/assets/icons/GraphArea.svg) | [ Gebied ](/help/analysis-workspace/visualizations/area.md) | [ Grafiek van het Gebied ](https://help.tableau.com/current/pro/desktop/en-us/qs_area_charts.htm) |
| ![ GraphBarVertical ](/help/assets/icons/GraphBarVertical.svg) | [ Bar ](/help/analysis-workspace/visualizations/bar.md) | [ Grafiek van de Bar ](https://help.tableau.com/current/pro/desktop/en-us/buildexamples_bar.htm) |
| ![ GraphBarVertical ](/help/assets/icons/GraphBarVerticalStacked.svg) | [ Gestapelde Bar ](/help/analysis-workspace/visualizations/bar.md) |  |
| ![ GraphBullet ](/help/assets/icons/GraphBullet.svg)</p> | [ Opsommingsteken ](/help/analysis-workspace/visualizations/bullet-graph.md) | [Grafiek met opsommingstekens](https://help.tableau.com/current/pro/desktop/en-us/qs_bullet_graphs.htm) |
| ![ TextNumbered ](/help/assets/icons/TextNumbered.svg) | [ Lijst van de Cohort ](/help/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) |  |
| ![ Combo ](/help/assets/icons/ComboChart.svg) | [ Combo ](/help/analysis-workspace/visualizations/combo-charts.md) | [ de Grafieken van de Combinatie ](https://help.tableau.com/current/pro/desktop/en-us/qs_combo_charts.htm) |
| ![ GraphDonut ](/help/assets/icons/GraphDonut.svg) | [Cirkeldiagram](/help/analysis-workspace/visualizations/donut.md) | |
| ![ ConversionFunnel ](/help/assets/icons/ConversionFunnel.svg) | [Uitval](/help/analysis-workspace/visualizations/fallout/fallout-flow.md) | |
| ![ GraphPathing ](/help/assets/icons/GraphPathing.svg) | [Stroom](/help/analysis-workspace/visualizations/c-flow/flow.md) |  |
| ![ ViewTable ](/help/assets/icons/ViewTable.svg)</p> | [Vrije-vormentabel](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) | [ Lijst van de Tekst ](https://help.tableau.com/current/pro/desktop/en-us/buildexamples_text.htm) |
| ![ GraphHistogram ](/help/assets/icons/Histogram.svg) | [Histogram](/help/analysis-workspace/visualizations/histogram.md) | [Histogram](https://help.tableau.com/current/pro/desktop/en-us/buildexamples_histogram.htm) |
| ![ GraphBarHorizontal ](/help/assets/icons/GraphBarHorizontal.svg) | [ Horizontale bar ](/help/analysis-workspace/visualizations/horizontal-bar.md) | [ Grafiek van de Bar ](https://help.tableau.com/current/pro/desktop/en-us/buildexamples_bar.htm) |
| ![ GraphBarHorizontalGestapeld ](/help/assets/icons/GraphBarHorizontalStacked.svg) | [ Horizontale gestapelde bar ](/help/analysis-workspace/visualizations/horizontal-bar.md) | [ Grafiek van de Bar ](https://help.tableau.com/current/pro/desktop/en-us/buildexamples_bar.htm) |
| ![ Branch3 ](/help/assets/icons/Branch3.svg) | [ het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md) | |
| ![ KeyMetrics ](/help/assets/icons/KeyMetrics.svg) | [ Zeer belangrijke metrische samenvatting ](/help/analysis-workspace/visualizations/key-metric.md) |  |
| ![ GraphTrend ](/help/assets/icons/GraphTrend.svg) | [Lijn](/help/analysis-workspace/visualizations/line.md) | [ Grafiek van de Lijn ](https://help.tableau.com/current/pro/desktop/en-us/buildexamples_line.htm) |
| ![ GraphScatter ](/help/assets/icons/GraphScatter.svg) | [ Spreiding ](/help/analysis-workspace/visualizations/scatterplot.md) | [ Verstrooiingspal ](https://help.tableau.com/current/pro/desktop/en-us/buildexamples_scatter.htm) |
| ![ PageRule ](/help/assets/icons/PageRule.svg) | [ kopbal van de Sectie ](/help/analysis-workspace/visualizations/section-header.md) |  |
| ![ MoveUpDown ](/help/assets/icons/MoveUpDown.svg) | [ Summiere verandering ](/help/analysis-workspace/visualizations/summary-number-change.md) | |
| ![ 123 ](/help/assets/icons/123.svg)</p> | [ Summiere aantal ](/help/analysis-workspace/visualizations/summary-number-change.md) | |
| ![Tekst](/help/assets/icons/Text.svg) | [Tekst](/help/analysis-workspace/visualizations/text.md) | |
| ![ ModernGridView ](/help/assets/icons/ModernGridView.svg) | [Boomstructuur](/help/analysis-workspace/visualizations/treemap.md)<p> | [Boomstructuur](https://help.tableau.com/current/pro/desktop/en-us/buildexamples_treemap.htm) |
| ![ Type ](/help/assets/icons/TwoDots.svg) | [Venn](/help/analysis-workspace/visualizations/venn.md) | |


### Boor omlaag

Tableau steunt [ boor wijze ](https://learn.microsoft.com/en-us/power-bi/consumer/end-user-drill) door [ hiërarchieën ](https://help.tableau.com/current/pro/desktop/en-us/qs_hierarchies.htm). In het onderstaande voorbeeld maakt u een hiërarchie wanneer u het veld **[!UICONTROL Product Name]** binnen **[!UICONTROL Tables]** selecteert en het boven **[!UICONTROL Product Category]** sleept. Vervolgens kunt u **[!UICONTROL + Drill down]** selecteren in het contextmenu van een balk die een productcategorie voorstelt.

![ boor van Tableau neer ](assets/uc15-tableau-drilldown.png)

Met de optie Omlaag kunt u de visualisatie bijwerken met aankoopopbrengsten voor producten binnen de geselecteerde productcategorie.

![ boor van Tableau omhoog ](assets/uc15-tableau-drillup.png)

De boor neer resulteert in de volgende SQL vraag die een GROUP DOOR clausule gebruikt:

```sql
SELECT CAST("cc_data_view"."product_category" AS TEXT) AS "product_category",
  CAST("cc_data_view"."product_name" AS TEXT) AS "product_name",
  SUM("cc_data_view"."purchase_revenue") AS "sum:purchase_revenue:ok"
FROM "public"."cc_data_view" "cc_data_view"
WHERE (("cc_data_view"."daterange" >= (TIMESTAMP '2023-01-01 00:00:00.000')) AND ("cc_data_view"."daterange" < (TIMESTAMP '2024-01-01 00:00:00.000')))
GROUP BY 1,
  2
```

De vraag beperkt **** niet de resultaten tot de geselecteerde productcategorie; slechts toont visualisatie de geselecteerde productcategorie.

![ boor van Tableau omhoog ](assets/uc15-tableau-drillup2.png)

U kunt ook een dashboard maken voor de boor omlaag, waarbij de ene visuele weergave het resultaat is van de selectie in een andere visuele weergave. In het onderstaande voorbeeld wordt de **[!UICONTROL Product Categories]** visualisatie gebruikt als een filter om de **[!UICONTROL Product Names]** -tabel bij te werken. Dit visualisatiefilter is alleen client en leidt niet tot een extra SQL-query.

![ de visualisatiefilter van Tableau ](assets/uc15-tableau-visualizationfilter.png)


>[!TAB  Leider ]

### Vergelijking

Voor de meeste Customer Journey Analytics-visualisaties biedt Lader vergelijkbare ervaringen. Zie de onderstaande tabel.

| Pictogram | Customer Journey Analytics visualisatie | Power BI Desktop visualisatie |
| :---: | --- | ---| 
| ![ GraphArea ](/help/assets/icons/GraphArea.svg) | [ Gebied ](/help/analysis-workspace/visualizations/area.md) | [ Grafiek van het Gebied ](https://cloud.google.com/looker/docs/area-options) |
| ![ GraphBarVertical ](/help/assets/icons/GraphBarVertical.svg) | [ Bar ](/help/analysis-workspace/visualizations/bar.md) | [ Grafiek van de Bar ](https://cloud.google.com/looker/docs/bar-options) |
| ![ GraphBarVertical ](/help/assets/icons/GraphBarVerticalStacked.svg) | [ Gestapelde Bar ](/help/analysis-workspace/visualizations/bar.md) | [ Grafiek van de Bar ](https://cloud.google.com/looker/docs/bar-options) |
| ![ GraphBullet ](/help/assets/icons/GraphBullet.svg)</p> | [ Opsommingsteken ](/help/analysis-workspace/visualizations/bullet-graph.md) | [Grafiek met opsommingstekens](https://cloud.google.com/looker/docs/bullet-chart) |
| ![ TextNumbered ](/help/assets/icons/TextNumbered.svg) | [ Lijst van de Cohort ](/help/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) |  |
| ![ Combo ](/help/assets/icons/ComboChart.svg) | [ Combo ](/help/analysis-workspace/visualizations/combo-charts.md) | [ Aanpassen visualisaties ](https://cloud.google.com/looker/docs/creating-visualizations#customizing_visualizations_with_chart_settings) |
| ![ GraphDonut ](/help/assets/icons/GraphDonut.svg) | [Cirkeldiagram](/help/analysis-workspace/visualizations/donut.md) | [Cirkeldiagram](https://cloud.google.com/looker/docs/donut-multiples-options) |
| ![ ConversionFunnel ](/help/assets/icons/ConversionFunnel.svg) | [Uitval](/help/analysis-workspace/visualizations/fallout/fallout-flow.md) | [ Trechter ](https://cloud.google.com/looker/docs/funnel-options) |
| ![ GraphPathing ](/help/assets/icons/GraphPathing.svg) | [Stroom](/help/analysis-workspace/visualizations/c-flow/flow.md) | [ Sankey ](https://cloud.google.com/looker/docs/sankey) |
| ![ ViewTable ](/help/assets/icons/ViewTable.svg)</p> | [Vrije-vormentabel](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) | [ Lijst ](https://cloud.google.com/looker/docs/table-options) |
| ![ GraphHistogram ](/help/assets/icons/Histogram.svg) | [Histogram](/help/analysis-workspace/visualizations/histogram.md) | |
| ![ GraphBarHorizontal ](/help/assets/icons/GraphBarHorizontal.svg) | [ Horizontale bar ](/help/analysis-workspace/visualizations/horizontal-bar.md) | [ Grafiek van de Bar ](https://cloud.google.com/looker/docs/bar-options) |
| ![ GraphBarHorizontalGestapeld ](/help/assets/icons/GraphBarHorizontalStacked.svg) | [ Horizontale gestapelde bar ](/help/analysis-workspace/visualizations/horizontal-bar.md) | [ Grafiek van de Bar ](https://cloud.google.com/looker/docs/bar-options) |
| ![ Branch3 ](/help/assets/icons/Branch3.svg) | [ het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md) |  |
| ![ KeyMetrics ](/help/assets/icons/KeyMetrics.svg) | [ Zeer belangrijke metrische samenvatting ](/help/analysis-workspace/visualizations/key-metric.md) |  |
| ![ GraphTrend ](/help/assets/icons/GraphTrend.svg) | [Lijn](/help/analysis-workspace/visualizations/line.md) | [ Grafiek van de Lijn ](https://cloud.google.com/looker/docs/line-options) |
| ![ GraphScatter ](/help/assets/icons/GraphScatter.svg) | [ Spreiding ](/help/analysis-workspace/visualizations/scatterplot.md) | [Spreidingsdiagram](https://cloud.google.com/looker/docs/scatter-options) |
| ![ PageRule ](/help/assets/icons/PageRule.svg) | [ kopbal van de Sectie ](/help/analysis-workspace/visualizations/section-header.md) |  |
| ![ MoveUpDown ](/help/assets/icons/MoveUpDown.svg) | [ Summiere verandering ](/help/analysis-workspace/visualizations/summary-number-change.md) | [ Enige Waarde ](https://cloud.google.com/looker/docs/single-value-options) |
| ![ 123 ](/help/assets/icons/123.svg)</p> | [ Summiere aantal ](/help/analysis-workspace/visualizations/summary-number-change.md) | [ Enige Waarde ](https://cloud.google.com/looker/docs/single-value-options) |
| ![Tekst](/help/assets/icons/Text.svg) | [Tekst](/help/analysis-workspace/visualizations/text.md) | [ Enige Waarde ](https://cloud.google.com/looker/docs/single-value-options) |
| ![ ModernGridView ](/help/assets/icons/ModernGridView.svg) | [Boomstructuur](/help/analysis-workspace/visualizations/treemap.md) | [Boomstructuur](https://cloud.google.com/looker/docs/treemap) |
| ![ Type ](/help/assets/icons/TwoDots.svg) | [ Diagram van de Venn ](/help/analysis-workspace/visualizations/venn.md) | [ Diagram van de Venn ](https://cloud.google.com/looker/docs/venn) |

>[!TAB  Jupyter Notitieboekje ]

Het vergelijken van de visualiseringsmogelijkheden van **matplotlib.pyplot**, de op staat-gebaseerde interface aan matplotlib, is voorbij het doel van dit artikel. Zie voorbeelden hierboven voor inspiratie en [ matplotlib.pyplot ](https://matplotlib.org/3.5.3/api/_as_gen/matplotlib.pyplot.html) documentatie.


>[!TAB  RStudio ]

Het vergelijken van de visualiseringsmogelijkheden van **ggplot2**, is het pakket van de gegevensvisualisatie in R, voorbij het doel van dit artikel. Zie voorbeelden hierboven voor inspiratie en [ gplot2 ](https://ggplot2.tidyverse.org/articles/ggplot2.html) documentatie.

>[!ENDTABS]




+++


## Caveats

Elk van de ondersteunde BI-gereedschappen heeft een aantal bedenkingen bij het werken met de Customer Journey Analytics BI-extensie.

+++ BI-gereedschappen

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

* Filteren van datumbereiken via Power BI Desktop Advanced is exclusief.  Voor uw einddatum, moet u één meer dan de dag selecteren u wilt melden. Bijvoorbeeld **[!UICONTROL is on or after]** `1/1/2023` **[!UICONTROL and before]** `1/2/2023` .
* Power BI Desktop wordt standaard ingesteld op **[!UICONTROL Import]** wanneer u een verbinding maakt. Gebruik **[!UICONTROL Direct Query]** niet.
* Power BI Desktop stelt gegevenstransformaties beschikbaar via Power Query.  De Vraag van de macht werkt hoofdzakelijk met het type van de Invoer verbindingen zodat een vele transformaties die u als datum of koordfuncties toepast een fout werpen die u op een het typeverbinding van de Invoer moet schakelen.  Als u gegevens bij vraagtijd moet omzetten, zou u afgeleide dimensies en metriek moeten gebruiken zodat te hoeven Power BI niet om de transformaties zelf te doen.
* De Desktop van Power BI begrijpt niet hoe te om datum-tijd typekolommen te behandelen zodat worden de **[!UICONTROL daterange*X *]**dimensies zoals **[!UICONTROL daterangehour]**en **[!UICONTROL daterangeminute]**niet gesteund.
* Power BI Desktop probeert standaard meerdere verbindingen te maken met behulp van meer Query Service-sessies.  Ga binnen aan de montages van Power BI voor uw project en maak parallelle vragen onbruikbaar.
* Power BI Desktop sorteert en beperkt alles op de client. De Desktop van Power BI heeft ook verschillende semantiek voor top *X* het filtreren die gebonden waarden omvat. U kunt dus niet dezelfde sortering en beperking maken als in Analysis Workspace.
* Eerdere versies van de Power BI Desktop-release van oktober 2024 breken PostSQL-gegevensbronnen uit. Gebruik de versie die in dit artikel wordt vermeld.

>[!TAB  Desktop Tableau ]

* Het filtreren van de Waaier van de Waaier van de Desktop van Tableau van Daten is exclusief. Voor uw einddatum, moet u één meer dan de dag selecteren u wilt melden.
* Wanneer u standaard een datum- of datum-tijddimensie zoals **[!UICONTROL Daterangemonth]** toevoegt aan de rijen van een blad, plaatst Tableau Desktop het veld in een **[!UICONTROL YEAR()]** -functie.  Om te krijgen wat u wilt, moet u die dimensie selecteren en van het drop-down menu selecteren de datumfunctie u wilt gebruiken.  Wijzig bijvoorbeeld **[!UICONTROL Year]** in **[!UICONTROL Month]** wanneer u **[!UICONTROL Daterangemonth]** wilt gebruiken.
* Het beperken van resultaten tot Top *X* is niet duidelijk in de Desktop van Tableau. U kunt de resultaten expliciet beperken of een berekend veld en de functie **[!UICONTROL INDEX()]** gebruiken.  Het toevoegen van een Hoogste *X* filter aan een afmeting produceert complexe SQL gebruikend binnen-sluit zich aan dat niet wordt gesteund.

>[!TAB  Leider ]

* De laagker heeft een maximumaantal verbindingen per knoop die tussen 5-100 wordt vereist plaatsen.  U kunt deze waarde niet instellen op 1.  Deze instelling houdt in dat een lagere verbinding altijd minimaal 5 van de beschikbare Query Service-sessies gebruikt.
* Met Liniaal kunt u een project maken met een weergave op basis van een Customer Journey Analytics-gegevensweergave. De plukker leidt dan tot een model dat op de afmetingen en metriek wordt gebaseerd, beschikbaar in de mening van Gegevens, gebruikend LookerML.  Deze projectweergave wordt niet automatisch bijgewerkt naar de bron.  Als u wijzigingen aanbrengt of toevoegt aan de afmetingen, metriek, berekende metriek of segmenten van de CJA-gegevensweergave, worden deze wijzigingen niet automatisch weergegeven in Kiezer.  U moet de projectweergave handmatig bijwerken of een nieuw project maken.
* De gebruikerservaring van de kiezer op datum- of datum-tijdvelden zoals **[!UICONTROL Daterange Date]** of **[!UICONTROL Daterangeday Date]** is verwarrend.
* Het datumbereik van Lager is exclusief in plaats van inclusief.  **[!UICONTROL until (before)]** is grijs, zodat u dat aspect kunt missen.  Voor uw einddag, moet u één meer dan de dag selecteren u wilt melden.
* In de viewer worden uw meetgegevens niet automatisch als meetgegevens beschouwd.  Wanneer u metrisch selecteert, door gebrek probeert de Teller metrisch als afmeting in de vraag te behandelen.  Om metriek als metrisch te behandelen, moet u een douanegebied tot stand brengen zoals hierboven geïllustreerd. Als sneltoets kunt u **[!UICONTROL ⋮]** selecteren, **[!UICONTROL Aggregate]** selecteren en vervolgens **[!UICONTROL Sum]** selecteren.

>[!TAB  Jupyter Notitieboekje ]

* Het belangrijkste voorbehoud voor Jupyter Notitieboekje is dat het hulpmiddel geen belemmering-en-dalingsgebruikersinterface zoals andere hulpmiddelen van BI heeft. U kunt goede beelden tot stand brengen, maar u moet code schrijven om dit te verwezenlijken.

>[!TAB  RStudio ]

* De illustratie werkt met een plat schema, dus de optie **[!UICONTROL FLATTEN]** is vereist.
* Het belangrijkste voorbehoud voor RStudio is dat het hulpmiddel geen belemmering-en-dalingsgebruikersinterface zoals andere hulpmiddelen van BI heeft. U kunt goede beelden tot stand brengen, maar u moet code schrijven om dit te verwezenlijken.

>[!ENDTABS]

+++
