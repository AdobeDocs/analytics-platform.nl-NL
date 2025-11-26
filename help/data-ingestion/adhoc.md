---
title: Ad-hocgegevens invoegen en gebruiken
description: Uitleggen hoe u ad hoc in Customer Journey Analytics kunt innemen en gebruiken
solution: Customer Journey Analytics
feature: Basics
role: Admin
exl-id: 17b5842f-dc81-481f-8b21-dc90a133adcf
source-git-commit: c9d7a4596a842ab7d949364e3469747d20ca15b4
workflow-type: tm+mt
source-wordcount: '1435'
ht-degree: 1%

---

# Ad-hocgegevens invoegen en gebruiken

In deze snelstartgids wordt uitgelegd hoe u ad-hocgegevens kunt invoeren in Experience Platform en deze gegevens vervolgens kunt gebruiken in Customer Journey Analytics.

Hiervoor moet u:

- **creeer een dataset met een Csv- dossier** in Experience Platform. Deze workflow definieert het model (schema) van de gegevens die u wilt verzamelen en waar u de gegevens (gegevensset) wilt verzamelen.

- **opstelling een verbinding** in Customer Journey Analytics. Deze verbinding moet (ten minste) uw Experience Platform-gegevensset ad hoc bevatten.

- **opstelling een gegevensmening** in Customer Journey Analytics om metriek en afmeting van de gebieden in uw ad hoc gegevens te bepalen die u in Analysis Workspace wilt gebruiken.

- **opstelling een project** in Customer Journey Analytics om uw rapporten en visualisaties te bouwen.



>[!NOTE]
>
>Deze handleiding voor snel starten is een vereenvoudigde handleiding voor het innemen van ad-hocgegevens in Experience Platform en het gebruik van die ad-hocgegevens in Customer Journey Analytics. Het wordt ten zeerste aanbevolen de aanvullende informatie te bestuderen wanneer deze wordt vermeld.


## Een gegevensset maken met een CSV-bestand

Voor dit snelle begin, wilt u een Csv- dossier gebruiken dat raadplegingsgegevens vertegenwoordigt en informatie gelijkend op hieronder getoond bevat.

| _id | tracking_code | ad_group | campagne_naam |
| ---: | :---          | :---        | :---          |
| 1 | abc123 | abc-adgroup | 123 Campagne |
| 2 | def123 | def-adgroup | 123 Campagne |
| 3 | ghi123 | ghi-adgroup | 123 Campagne |
| 4 | abc456 | abc-adgroup | 456 Campagne |
| 5 | def456 | def-adgroup | 456 Campagne |

>[!NOTE]
>
>Gebruik speciale gegevenssets en schema&#39;s voor op records gebaseerde gegevens (opzoeken, profiel). Ad hoc datasets en schema&#39;s zijn minder geschikt en zouden niet voor tijdreeksgegevens (gebeurtenis, samenvatting) moeten worden overwogen.

U hoeft geen XDM-schema voor ad-hocgegevens te maken. Experience Platform ondersteunt een workflow die op basis van de gegevens in het CSV-bestand:

1. Hiermee maakt u automatisch een ad-hocschema. Dat schema voldoet aan de kolommen van het CSV-bestand.
1. Maakt een dataset die de gegevens van het CSV-bestand bevat.

De workflow starten:

1. Selecteer **[!UICONTROL Workflows]** in de Experience Platform-interface in de linkertrack.
1. Selecteer ![&#x200B; DataAdd &#x200B;](/help/assets/icons/DataAdd.svg) **[!UICONTROL Create dataset from CSV file]**.
1. Selecteer **[!UICONTROL Launch]** in het rechterdeelvenster.
1. Kies in de wizard **[!UICONTROL Workflows]** > **[!UICONTROL Create dataset from CSV file]** :
   1. In de stap **[!UICONTROL Configure dataset]** :
      1. Voer een **[!UICONTROL Name]** in voor de gegevensset. Bijvoorbeeld: `Sample Data From CSV` .
      1. Voeg een optionele **[!UICONTROL Description]** toe. Bijvoorbeeld: `Sample data from a CSV file` .
      1. Voeg een of meer optionele **[!UICONTROL Tags]** toe of selecteer een of meer bestaande **[!UICONTROL Tags]** .

         ![&#x200B; vorm ad hoc dataset &#x200B;](assets/adhoc-dataset-configure.png)

      1. Selecteer **[!UICONTROL Next]**.
   1. In de stap **[!UICONTROL Add data]** :
      1. Selecteer **[!UICONTROL Choose Files]** om uw CSV-bestand van uw computer of netwerk te selecteren. U kunt het bestand ook van de locatie op uw computer of netwerk naar **[!UICONTROL Drag and drop files]** slepen. Het bestand wordt geüpload en **[!UICONTROL Sample data]** wordt weergegeven.
      1. Schakel **[!UICONTROL Error diagnostics]** en **[!UICONTROL Enable partial ingestion]** in of uit overeenkomstig uw voorkeuren. Wanneer u **[!UICONTROL Enable Partial ingestion]** gebruikt, kunt u een **[!UICONTROL Error threshold %]** definiëren.

         ![&#x200B; voegt gegevens aan een ad hoc dataset &#x200B;](assets/adhoc-dataset-adddata.png) toe

      1. Selecteer **[!UICONTROL Finish]**.

Nadat de gegevens zijn voorbereid en geüpload, wordt u omgeleid naar **[!UICONTROL Datasets]** in de Experience Platform-interface.<br/> u ziet **[!UICONTROL Dataset activity]** voor uw **[!UICONTROL Sample Data from CSV]** dataset met de status ![&#x200B; StatusOrange &#x200B;](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Processing]**.

![&#x200B; activiteit van de Dataset voor ad hoc gegevens &#x200B;](assets/datasets-dataset-activity.png)

De ad-hocgegevens inspecteren:

1. Selecteer **[!UICONTROL Datasets]** in de Experience Platform-interface in de linkertrack.
1. Selecteer de tab **[!UICONTROL Browse]** in **[!UICONTROL Datasets]** . U zou uw dataset moeten zien vermeld.
1. Selecteer de naam van het schema in de kolom **[!UICONTROL Schema]** . Bijvoorbeeld: **[!UICONTROL Sample Data From CSV…]**

   ![&#x200B; Uitgezochte schema voor ad hoc dataset &#x200B;](assets/adhoc-schema-selection.png)

1. Selecteer de **[!UICONTROL Schema name]** in de pop-up. Bijvoorbeeld: **[!UICONTROL Sample Data From CSV - adhoc schema - XXXXXXXXXXX]** . U wordt omgeleid naar de interface **[!UICONTROL Schemas]** > **[!UICONTROL Sample Data From CSV - adhoc schema - XXXXXXXXXXX]** .

In de interface **[!UICONTROL Schemas]** > **[!UICONTROL Sample Data From CSV - adhoc schema - XXXXXXXXXXX]** :

- Selecteer het naamobject van de bovenste huurder onder **[!UICONTROL Schemas]** > **[!UICONTROL Sample Data From CSV - adhoc schema - XXXXXXXXXXX]** om de velden in het object weer te geven. De velden in het object vertegenwoordigen de structuur van het CSV-bestand. Het schema wordt automatisch gemaakt op basis van het uploaden van de ad-hocgegevens.

  ![&#x200B; Ad hoc schema &#x200B;](dataset/../assets/adhoc-schema.png)

  >[!NOTE]
  >
  >De workflow definieert alle velden in het schema als van het type String. U kunt dit type in een later stadium niet wijzigen. Als u meer flexibiliteit in de definitie van een ad hoc schema nodig hebt, overweeg [&#x200B; gebruikend API om een ad hoc schema &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/tutorials/ad-hoc) tot stand te brengen en dan [&#x200B; te gebruiken creeer dataset van schema &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/catalog/datasets/user-guide#schema) werkschema.
  > 




## Een verbinding instellen

Om de dataset van Experience Platform in Customer Journey Analytics te gebruiken, creeert u een verbinding die de ad hoc dataset die uit het [&#x200B; werkschema &#x200B;](#create-a-dataset-with-a-csv-file) resulteert omvat

Met een verbinding kunt u gegevenssets van Experience Platform integreren in Workspace. Om over deze datasets te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en Workspace vestigen.

Om uw verbinding tot stand te brengen:

1. Selecteer in de gebruikersinterface van Customer Journey Analytics de optie **[!UICONTROL Connections]** (optioneel in **[!UICONTROL Data management]** ) in het bovenste menu.

1. Selecteer **[!UICONTROL Create new connection]**.

1. In het **[!UICONTROL Untitled connection]** -scherm:

   1. Geef een naam en beschrijf de verbinding in **[!UICONTROL Connection Settings]** .

   1. Selecteer de juiste sandbox in de lijst **[!UICONTROL Sandbox]** in **[!UICONTROL Data settings]** en selecteer het aantal dagelijkse gebeurtenissen in de lijst **[!UICONTROL Average number of daily events]** .

      ![&#x200B; de Montages van de Verbinding &#x200B;](./assets/cja-connections-1.png)

   1. Selecteer **[!UICONTROL Add datasets]**.

1. In de stap **[!UICONTROL Select datasets]** in **[!UICONTROL Add datasets]** :

   1. Selecteer de dataset die u vroeger creeerde, bijvoorbeeld **[!UICONTROL Sample Data From CSV]**, en om het even welke andere dataset u in uw verbinding wilt omvatten. De ad-hocgegevenssets hebben de eigenschap **[!UICONTROL Adhoc]** [!UICONTROL Dataset type] .

      ![&#x200B; voeg datasets &#x200B;](./assets/cja-connections-adhoc-2.png) toe

   1. Selecteer **[!UICONTROL Next]**.

1. In de stap **[!UICONTROL Datasets settings]** in **[!UICONTROL Add datasets]** :

   Voor uw ad-hocgegevensset:

   1. Selecteer het type ad-hocgegevensset. Bijvoorbeeld: **[!UICONTROL Lookup]** .
   1. Selecteer een **[!UICONTROL Key]** uit de beschikbare toetsen die in het ad-hocschema zijn gedefinieerd.
   1. Selecteer een **[!UICONTROL Matching key]** in een gebeurtenisgegevensset die u als onderdeel van de verbinding hebt toegevoegd.
   1. Selecteer de juiste gegevensbron in de lijst **[!UICONTROL Data source type]** . Als u **[!UICONTROL Other]** opgeeft, voegt u een beschrijving voor de gegevensbron toe.

   1. Stel **[!UICONTROL Import all new data]** en **[!UICONTROL Dataset backfill existing data]** in op basis van uw voorkeuren.

      ![&#x200B; vorm datasets &#x200B;](./assets/cja-connections-3-adhoc.png)

   1. Selecteer **[!UICONTROL Add datasets]**.

   1. Selecteer **[!UICONTROL Save]**.

Zie [&#x200B; Ad hoc datasetmontages &#x200B;](/help/connections/create-connection.md#adhoc-dataset) voor meer details over de montages beschikbaar voor ad hoc datasets.

>[!IMPORTANT]
>
>Naast de algemene aanbeveling om geen ad hoc datasets en schema&#39;s voor tijdreeksgegevens te gebruiken, kunt u niet het **[!UICONTROL Create dataset from CSV]** werkschema voor tijdreeksgegevens gebruiken. Deze workflow definieert alle velden als velden van het type String die u achteraf niet kunt wijzigen. Wanneer u een op tijdreeksen gebaseerde dataset (gebeurtenis of samenvatting) aan een verbinding toevoegt, vereist dit type van dataset de definitie van minstens één gebied van type DateTime.<br/> als u vereist om ad hoc tijd-reeksen gegevens te gebruiken, overweeg [&#x200B; gebruikend API om een ad hoc schema &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/tutorials/ad-hoc#token_type=bearer&expires_in=43197438) tot stand te brengen en dan [&#x200B; te gebruiken creeer dataset van schema &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/catalog/datasets/user-guide#schema) werkschema.


Nadat u a [&#x200B; verbinding &#x200B;](/help/connections/overview.md) creeert, kunt u diverse beheerstaken, zoals [&#x200B; uitvoeren die en datasets &#x200B;](/help/connections/combined-dataset.md) combineren, [&#x200B; controleren het statuut van de datasets van een verbinding en het statuut van gegevensopname &#x200B;](/help/connections/manage-connections.md), en meer.

## Een gegevensweergave instellen

Een gegevensweergave is een container specifiek voor Customer Journey Analytics waarmee u kunt bepalen hoe gegevens van een verbinding moeten worden geïnterpreteerd. Hiermee worden alle afmetingen en metriek opgegeven die beschikbaar zijn in Analysis Workspace en de kolommen waarvan die dimensies en metriek hun gegevens verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

Uw gegevensweergave maken:

1. Selecteer in de gebruikersinterface van Customer Journey Analytics de optie **[!UICONTROL Data views]** (optioneel in **[!UICONTROL Data management]** ) in het bovenste menu.

1. Selecteer **[!UICONTROL Create new data view]**.

1. In de stap **[!UICONTROL Configure]** :

   1. Selecteer uw [&#x200B; verbinding &#x200B;](#set-up-a-connection) van de **[!UICONTROL Connection]** lijst.

   1. Naam en (optioneel) beschrijf uw verbinding.

      ![&#x200B; de mening van Gegevens vormt &#x200B;](./assets/cja-dataview-1.png)

   1. Selecteer **[!UICONTROL Save and continue]**.

1. In de stap **[!UICONTROL Components]** :

   1. Voeg schemagebieden en/of standaardcomponent toe die u aan de **[!UICONTROL METRICS]** of **[!UICONTROL DIMENSIONS]** componentenvakjes wilt omvatten. Zorg ervoor dat u relevante velden uit de gegevensset toevoegt die de ad-hocgegevens bevat. U kunt als volgt toegang krijgen tot deze velden:

      1. Selecteer **[!UICONTROL Event datasets]**.
      1. Selecteer **[!UICONTROL Adhoc & Relational fields]**.

         ![&#x200B; mening van Gegevens - adhoc componenten &#x200B;](assets/cja-dataview-components-adhoc.png)

      1. Sleep velden van de ad-hocschema&#39;s naar **[!UICONTROL METRICS]** of **[!UICONTROL DIMENSIONS]** .



   1. Naar keuze, gebruik [&#x200B; afgeleide gebieden &#x200B;](/help/data-views/derived-fields/derived-fields.md) om het even welke ad hoc gebieden van hun standaardtype en formaat van het Koord aan een ander type of formaat te wijzigen.

   1. Selecteer **[!UICONTROL Save and continue]**.

1. In de stap **[!UICONTROL Settings]** :

   Laat de instellingen ongewijzigd en selecteer **[!UICONTROL Save and finish]** .

Zie [&#x200B; overzicht van de meningen van Gegevens &#x200B;](../data-views/data-views.md) voor meer informatie over om een gegevensmening tot stand te brengen en uit te geven. En welke componenten beschikbaar voor u in uw gegevensmening en hoe te om segment en zittingsmontages te gebruiken zijn.


## Een project instellen

Analysis Workspace is een flexibel browserprogramma waarmee u snel analyses kunt maken en inzichten kunt delen op basis van uw gegevens. U gebruikt de projecten van Workspace om gegevenscomponenten, lijsten, en visualisaties te combineren om uw analyse te bundelen en met iedereen in uw organisatie te delen.

Uw project maken:

1. Selecteer in de gebruikersinterface van Customer Journey Analytics de optie **[!UICONTROL Projects]** in het bovenste menu.

1. Selecteer **[!UICONTROL Projects]** in de linkernavigatie.

1. Selecteer **[!UICONTROL Create project]**.

1. Selecteer **[!UICONTROL Blank project]**.

1. Selecteer uw [&#x200B; gegevensmening &#x200B;](#set-up-a-data-view) van de lijst.

1. Als u uw eerste rapport wilt maken, sleept u de afmetingen en metriek op de [!UICONTROL Freeform table] in de [!UICONTROL Panel] . Met inbegrip van die metriek of dimensie die op uw ad hoc gegevens gebaseerd zijn.

Zie [&#x200B; overzicht van Analysis Workspace &#x200B;](../analysis-workspace/home.md) voor meer informatie over hoe te om projecten tot stand te brengen en uw analyse te bouwen gebruikend componenten, visualisaties, en panelen.

>[!SUCCESS]
>
>U hebt alle stappen uitgevoerd. U hebt eerst gedefinieerd welke ad-hocgegevens u wilt verzamelen (CSV-bestand). U gebruikte de werkstroom om een ad hoc dataset en schema van dat Csv- dossier tot stand te brengen. U hebt een verbinding in Customer Journey Analytics gedefinieerd voor het gebruik van de ingesloten ad-hocgegevens en andere gegevens. Met de definitie van uw gegevensweergave kunt u opgeven welke dimensie en metriek u wilt gebruiken en ten slotte hebt u uw eerste project gemaakt waarin uw gegevens worden gevisualiseerd en geanalyseerd.
