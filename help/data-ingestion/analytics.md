---
title: Gegevens van traditionele Adobe Analytics verzamelen en gebruiken
description: Uitleggen hoe gegevens uit traditionele Adobe Analytics kunnen worden ingevoerd
solution: Customer Journey Analytics
feature: Basics
exl-id: 5cbfa922-6d6e-453a-9558-abfcfb80449d
role: Admin
source-git-commit: 90d1c51c11f0ab4d7d61b8e115efa8257a985446
workflow-type: tm+mt
source-wordcount: '1081'
ht-degree: 0%

---

# Gegevens van Adobe Analytics invoegen en gebruiken

In deze handleiding voor snel starten wordt uitgelegd hoe u de gegevens die door Adobe Analytics in Customer Journey Analytics zijn verzameld, kunt gebruiken.

>[!PREREQUISITES]
>
>U hebt een Adobe Analytics-licentie en -implementatie op een of meer van uw websites, waarbij u een van de gedocumenteerde implementatiemethoden gebruikt:
>
>- [ voert Analyses uit gebruikend Experience Platform Edge ](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/overview.html)
>
>- [ voert Analyses uit gebruikend de uitbreiding van Adobe Analytics ](https://experienceleague.adobe.com/docs/analytics/implementation/launch/overview.html)
>
>- [ voert Analyses uit gebruikend JavaScript ](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html)

Hiervoor moet u:

- **opstelling een bron van Adobe Analytics schakelaar** in Adobe Experience Platform. De bronschakelaar zorgt ervoor dat uw huidige gegevens van Adobe Analytics in een dataset in Adobe Experience Platform worden opgenomen.

- **opstelling een verbinding** in Customer Journey Analytics. De verbinding moet (ten minste) uw Adobe Experience Platform-gegevensset bevatten.

- **opstelling een gegevensmening** in Customer Journey Analytics om metriek en afmeting te bepalen die u in Analysis Workspace wilt gebruiken.

- **opstelling een project** in Customer Journey Analytics om uw rapporten en visualisaties te bouwen.


>[!NOTE]
>
>Deze snelle startgids is een vereenvoudigde gids over hoe te om gegevens in te voeren, gebruikend de bron van Adobe Analytics schakelaar, en gebruik die gegevens in Customer Journey Analytics. Het wordt ten zeerste aanbevolen de aanvullende informatie te bestuderen wanneer deze wordt vermeld.


## Een Adobe Analytics-bronaansluiting instellen

Met de Adobe Analytics-bronaansluiting kunt u Adobe Analytics-rapportsuite-gegevens naar Adobe Experience Platform overbrengen.

Een Adobe Analytics-bronaansluiting maken:

1. Selecteer **[!UICONTROL Sources]** in de UI Platform (Platform-interface) in de linkertrack.

2. Selecteer **[!UICONTROL Adobe applications]** in de lijst met [!UICONTROL CATEGORIES] .

3. Selecteer **[!UICONTROL Set up]** of **[!UICONTROL Add data]** in de tegel Adobe Analytics.

   ![ het venster van Adobe Experience Platform met Bronnen die samen met de toepassingen van de Adobe worden geselecteerd en benadrukte gegevens toevoegen.](./assets/sources-overview.png)

4. Selecteer **[!UICONTROL Report suite]** . Selecteer in de lijst met rapportsuites de versie die u wilt gebruiken.

   ![ Adobe Experience Platform venster dat de lijst van de Reeksen van het Rapport toont ](./assets/report-suites.png)

   Selecteer **[!UICONTROL Next]** .

5. Selecteer **[!UICONTROL Default schema]** als de [!UICONTROL Target schema] . Adobe Experience Platform leidt automatisch tot het schema en de overeenkomstige dataset om alle standaardgebieden van de geselecteerde het rapportreeks van Adobe Analytics in kaart te brengen.

   ![ Adobe Experience Platform venster met het Standaard geselecteerde schema ](./assets/default-schema.png)

   Selecteer **[!UICONTROL Next]** .

6. Geef de gegevensstroom een naam en (optioneel) geef een beschrijving op.

   ![ Adobe Experience Platform venster die de sectie van het detail Dataflow ](./assets/dataflow-detail.png) benadrukt

   Selecteer **[!UICONTROL Next]** .

7. Controleer de verbinding en selecteer **[!UICONTROL Finish]** .

   ![ Adobe Experience Platform venster die Connect en het type van Gegevens secties voor overzicht benadrukken ](./assets/review.png)


Zodra de verbinding wordt gecreeerd, wordt de dataflow automatisch gecreeerd om een dataset met de gegevens van Adobe Analytics van uw rapportreeks te bevolken. De gegevensstroom neemt tot 13 maanden historische gegevens voor productiestanddozen op. De back-up van niet-productie sandboxen is beperkt tot drie maanden.

Wanneer de eerste opname is voltooid, zijn de gegevens van uw Adobe Analytics-rapportenpakket klaar om door de Customer Journey Analytics te worden gebruikt.

Zie [ een Adobe Analytics bronverbinding in UI ](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) voor een veel uitvoeriger leerprogramma tot stand brengen.


## Een verbinding instellen

Om de gegevens van Adobe Experience Platform in Customer Journey Analytics te gebruiken, creeert u een verbinding die de gegevens omvat die uit vestiging uw schema, dataset, en werkschema voortvloeien.

Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over deze datasets te rapporteren, moet u eerst een verband tussen datasets in Adobe Experience Platform en Workspace vestigen.

Om uw verbinding tot stand te brengen:

1. Selecteer **[!UICONTROL Connections]** in de bovenste navigatie in de gebruikersinterface van de Customer Journey Analytics.

2. Selecteer **[!UICONTROL Create new connection]** .

3. In het [!UICONTROL Untitled connection] -scherm:

   Geef een naam en beschrijf de verbinding in [!UICONTROL Connection Settings] .

   Selecteer de juiste sandbox in de lijst [!UICONTROL Sandbox] in [!UICONTROL Data settings] en selecteer het aantal dagelijkse gebeurtenissen in de lijst [!UICONTROL Average number of daily events] .

   ![ de Montages van de Verbinding ](./assets/cja-connections-1.png)

   Selecteer **[!UICONTROL Add datasets]** .

   In de stap [!UICONTROL Select datasets] in [!UICONTROL Add datasets] :

   - Selecteer automatisch de dataset die door de Adobe Analytics bronschakelaar en een andere dataset wordt gecreeerd die u in uw verbinding wilt omvatten.

     ![ voeg datasetvenster ](./assets/cja-connections-2a.png) toe

   - Selecteer **[!UICONTROL Next]** .

   In de stap [!UICONTROL Datasets settings] in [!UICONTROL Add datasets] :

   - Voor elke gegevensset:

      - Selecteer een [!UICONTROL Person ID] van de beschikbare identiteiten die in de datasetschema&#39;s in Adobe Experience Platform worden bepaald.

      - Selecteer de juiste gegevensbron in de lijst [!UICONTROL Data source type] . Als u **[!UICONTROL Other]** opgeeft, voegt u een beschrijving voor de gegevensbron toe.

      - Stel **[!UICONTROL Import all new data]** en **[!UICONTROL Dataset backfill existing data]** in op basis van uw voorkeuren.

     ![ vorm datasets ](./assets/cja-connections-3a.png)

   - Selecteer **[!UICONTROL Add datasets]** .

   Selecteer **[!UICONTROL Save]** .

Zie [ Overzicht van Verbindingen ](../connections/overview.md) voor meer informatie over om een verbinding tot stand te brengen en te beheren en datasets te selecteren en te combineren.

## Een gegevensweergave instellen

Een gegevensmening is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van een verbinding te interpreteren. Hiermee worden alle afmetingen en metriek opgegeven die beschikbaar zijn in Analysis Workspace en de kolommen waarvan die dimensies en metriek hun gegevens verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

Uw gegevensweergave maken:

1. Selecteer **[!UICONTROL Data views]** in de bovenste navigatie in de gebruikersinterface van de Customer Journey Analytics.

2. Selecteer **[!UICONTROL Create new data view]** .

3. In de stap [!UICONTROL Configure] :

   Selecteer de verbinding in de lijst [!UICONTROL Connection] .

   Naam en (optioneel) beschrijf uw verbinding.

   ![ de mening van Gegevens vormt ](./assets/cja-dataview-1.png)

   Selecteer **[!UICONTROL Save and continue]** .

4. In de stap [!UICONTROL Components] :

   Voeg schemagebieden en/of standaardcomponent toe die u aan de [!UICONTROL METRICS] of [!UICONTROL DIMENSIONS] componentenvakjes wilt omvatten.

   ![ de meningscomponenten van Gegevens ](./assets/cja-dataview-2.png)

   Selecteer **[!UICONTROL Save and continue]** .

5. In de stap [!UICONTROL Settings] :

   ![ de meningsmontages van Gegevens ](./assets/cja-dataview-3.png)

   Laat de instellingen ongewijzigd en selecteer **[!UICONTROL Save and finish]** .

Zie [ overzicht van de meningen van Gegevens ](../data-views/data-views.md) voor meer informatie over om een gegevensmening tot stand te brengen en uit te geven, welke componenten voor u aan gebruik in uw gegevensmening en hoe te filter en zittingsmontages te gebruiken beschikbaar zijn.


## Een project instellen

Analysis Workspace is een flexibel browserprogramma waarmee u snel analyses kunt maken en inzichten kunt delen op basis van uw gegevens. U gebruikt de projecten van Workspace om gegevenscomponenten, lijsten, en visualisaties te combineren om uw analyse te bundelen en met iedereen in uw organisatie te delen.

Uw project maken:

1. Selecteer **[!UICONTROL Projects]** in de bovenste navigatie in de gebruikersinterface van de Customer Journey Analytics.

2. Selecteer **[!UICONTROL Projects]** in de linkernavigatie.

3. Selecteer **[!UICONTROL Create project]** .

   ![ Project van Workspace ](./assets/cja-projects-1.png)

   Selecteer **[!UICONTROL Blank project]** .

   ![ Workspace - Leeg Project ](./assets/cja-projects-2.png)

4. Selecteer de gegevensweergave in de lijst.

   ![ de Uitgezochte mening van Gegevens van Workspace ](./assets/cja-projects-3.png).

5. Als u uw eerste rapport wilt maken, sleept u de afmetingen en metriek op de [!UICONTROL Freeform table] in de [!UICONTROL Panel] . Sleep bijvoorbeeld `Program Points Balance` en `Page View` als metriek en `email` als dimensie om een snel overzicht te krijgen van profielen die uw website hebben bezocht en deel uitmaken van het loyaliteitsprogramma dat loyaliteitspunten verzamelt.

   ![ Workspace - Eerste Rapport ](./assets/cja-projects-5.png)

Zie [ overzicht van Analysis Workspace ](../analysis-workspace/home.md) voor meer informatie over hoe te om projecten tot stand te brengen en uw analyse te bouwen gebruikend componenten, visualisaties, en panelen.


>[!SUCCESS]
>
>U hebt alle stappen uitgevoerd. Om te beginnen wordt de Adobe Analytics-gegevensbronaansluiting ingesteld en de aansluiting voor uw rapportsuite geconfigureerd, worden uw Adobe Analytics-gegevens automatisch geüpload naar Adobe Experience Platform. U hebt een verbinding in Customer Journey Analytics gedefinieerd voor het gebruik van de opgenomen Adobe Analytics-gegevens en andere gegevens. Met de definitie van uw gegevensweergave kunt u opgeven welke dimensie en metriek u wilt gebruiken en ten slotte hebt u uw eerste project gemaakt waarin uw gegevens worden gevisualiseerd en geanalyseerd.

