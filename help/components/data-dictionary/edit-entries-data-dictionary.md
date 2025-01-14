---
description: Met het gegevenswoordenboek in Analysis Workspace kunnen gebruikers de verschillende componenten in Analysis Workspace, waaronder het beoogde gebruik, die zijn goedgekeurd, duplicaten zijn, catalogiseren en bijhouden, enzovoort.
title: Onderdeelitems bewerken
feature: Components
role: Admin
exl-id: 2d232811-e34a-4667-819c-cbe2a3e72702
source-git-commit: 8c975a37e6772ab3bae1f86c4ccad27ebf0596cc
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# Onderdeelitems bewerken

Customer Journey Analytics-beheerders kunnen componentitems in het gegevenswoordenboek voor een bepaalde gegevensweergave bewerken. Alle aangebrachte wijzigingen zijn zichtbaar voor alle gebruikers van de gegevensweergave.

Een component in het gegevenswoordenboek bewerken:

1. Ga naar het Analysis Workspace-project dat de component bevat die u wilt bewerken.

1. Selecteer het **pictogram van het Woordenboek van Gegevens** in het knooppaneel van Analysis Workspace. (Alternatieve manieren om tot het Woordenboek van Gegevens toegang te hebben worden beschreven in &quot;toegang tot het Woordenboek van Gegevens&quot;in [ het Overzicht van het Woordenboek van Gegevens ](/help/components/data-dictionary/data-dictionary-overview.md).)

   Het venster Gegevenswoordenboek wordt weergegeven.

   {de beheerdermening van het Woordenboek van 0} Gegevens die de Gezondheid van het Woordenboek tonen ](assets/data-dictionary-admin.png)![

1. Controleer of de juiste gegevensweergave is geselecteerd in het keuzemenu. Standaard wordt de gegevensweergave weergegeven waarin u zich al bevindt.

1. (Optioneel) Typ in het zoekveld de naam van de component die u wilt bewerken.

   Het type component kan door zowel kleur als pictogram worden geïdentificeerd. **Dimensionen** ![ het pictogram van het Dimension ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Data_18_N.svg) is oranje, **het pictogram van de Filters** ![ van het Segment ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Segmentation_18_N.svg) is blauw, **waaiers van de Datum** ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg) het de waaierpictogram van 10} Datum is paars, en **Metriek** ![ metrisch pictogram 15} is groen. ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Event_18_N.svg) Het pictogram van de Adobe wijst op of een berekend metrisch malplaatje of een filtermalplaatje, en het pictogram van de calculator ![ Calculator ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calculator_18_N.svg) op berekende metrisch die door een beheerder Analytics in uw organisatie werd gecreeerd.

1. (Facultatief) selecteer het **pictogram van de Filter ![ van het Woordenboek van de Filter van de Filter ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg), dan om het even welke volgende filteropties om de lijst van componenten te filtreren:**

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **Goedgekeurd**] | Alleen componenten tonen die zijn gemarkeerd als goedgekeurd door een beheerder. |
   | [!UICONTROL **Favorieten**] | Alleen componenten tonen die zich in de lijst Favorieten bevinden. Voor informatie over het toevoegen van componenten aan uw lijst van favorieten, zie [ Overzicht van Componenten ](/help/components/overview.md). |
   | [!UICONTROL **Dimensies**] | Alleen componenten weergeven die Dimensionen zijn. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) |
   | [!UICONTROL **Cijfers**] | Alleen componenten weergeven die Metrisch zijn. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) |
   | [!UICONTROL **Filters**] | Alleen componenten weergeven die filters zijn. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) <!--this is Filters in Customer Journey Analytics--> |
   | [!UICONTROL **waaiers van de Datum**] | Alleen componenten tonen die Datumbereik hebben. (Deze optie is ook beschikbaar in het [!UICONTROL **Snelle filters**] lusje wanneer u eerst tot het Woordenboek van Gegevens toegang hebt.) |
   | [!UICONTROL **toon allen**] | Alle componenten tonen. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Niet goedgekeurd**] | Alleen componenten tonen die nog niet zijn gemarkeerd als goedgekeurd door een beheerder. Als beheerder, is dit nuttig wanneer het identificeren van componenten die uw overzicht en goedkeuring vereisen. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Ontbrekende Beschrijving**] | Alleen componenten weergeven die nog geen beschrijving hebben in het veld Beschrijving. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **toon duplicaten**] | Alleen componenten weergeven die dezelfde naam of dezelfde beschrijving hebben als een andere component in de geselecteerde gegevensweergave. Dit geldt ook voor componenten die u maakt en de componenten die door de Adobe worden geleverd. Namen of beschrijvingen moeten exact overeenkomen om als duplicaten te kunnen worden weergegeven. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Geen recente gegevens**] | Alleen componenten weergeven die de afgelopen 90 dagen geen gegevens hebben verzameld. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **die door Adobe**] wordt gecreeerd <!-- I don't see this option--> | Alleen componenten weergeven die zijn gemaakt door Adobe. Componenten die door een beheerder of een andere gebruiker in uw organisatie zijn gemaakt, worden niet weergegeven. |

   {style="table-layout:auto"}

1. (Facultatief) selecteer het **pictogram van de Soort ![ de componenten van de Soort pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SortOrderDown_18_N.svg), dan om het even welke volgende filteropties om de lijst van componenten te sorteren:**

{{components-sort-options}}

1. Selecteer in de lijst met componenten de component die u wilt bewerken.

1. Selecteer **uitgeven** pictogram ![ Woordenboek van Gegevens geeft pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Edit_18_N.svg) naast de componentennaam uit.

1. Bewerk de volgende informatie over de component:

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **Goedgekeurd**] | <p>Geeft aan dat de component is gecontroleerd en goedgekeurd door de beheerder.</p><p>De beheerders zien een optie aan [!UICONTROL **niet goedkeuren**]. Als u deze optie selecteert, wordt de component gemarkeerd als &quot;Niet goedgekeurd&quot; voor gebruikers.</p> |
   | [!UICONTROL **niet goedgekeurd**] | <p>Geeft aan dat de component nog niet is gereviseerd en goedgekeurd door de beheerder.</p><p>De beheerders zien een optie [!UICONTROL **goedkeuren**]. Als u deze optie selecteert, wordt de component gemarkeerd als &quot;Goedgekeurd&quot; voor gebruikers.</p> |
   | [!UICONTROL **Beschrijving**] | Beschrijft de voorgenomen functie van de component. (Deze informatie wordt toegevoegd door de beheerder van Analytics, zoals die in [ wordt beschreven voeg componentenbeschrijvingen ](/help/components/add-component-descriptions.md) toe.) |
   | [!UICONTROL **vaak gebruikt met**] | <p>Geeft componenten weer die het meest worden gebruikt met de component die u bekijkt.</p><p>Er worden maximaal vijf componenten weergegeven voor de vijf primaire componenttypen: Metrisch, Berekend metrisch, Dimension, Filter en Datumbereik.</p><p>Deze lijst is gebaseerd op gegevens uit de afgelopen 90 dagen. Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>De beheerders kunnen tot de componenten leiden die de gebruikers in deze sectie zien door de gewenste componenten in [!UICONTROL **te selecteren omvatten**] altijd en [!UICONTROL **sluit**] drop-down gebieden altijd uit. Alvorens u de componenten beheert die de gebruikers zien, pas eerst **toe tonen al** filter om ervoor te zorgen u om het even welke componenten ziet die niet met u worden gedeeld die door een andere beheerder zouden kunnen zijn toegevoegd.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p> |
   | [!UICONTROL **Gelijkaardig aan**] | <p>Geeft componenten weer met vergelijkbare namen als de component die u bekijkt.</p><p>Er worden maximaal vijf componenten weergegeven voor de vijf primaire componenttypen: Metrisch, Berekend metrisch, Dimension, Filter en Datumbereik.</p><p>Alleen componenten die u kunt bekijken, worden weergegeven.</p><p>Alle dubbele componenten in de gegevensweergave worden hier weergegeven. De beheerders van Analytics zouden alle dubbele componenten moeten identificeren en verwijderen, zoals die in [ wordt beschreven de gezondheid van het Woordenboek van Gegevens van de Monitor ](/help/components/data-dictionary/monitor-data-dictionary-health.md).</p><p>De beheerders kunnen tot de componenten leiden die de gebruikers in deze sectie zien door de gewenste componenten in [!UICONTROL **te selecteren omvatten**] altijd en [!UICONTROL **sluit**] drop-down gebieden altijd uit. Alvorens u de componenten beheert die de gebruikers zien, pas eerst **toe tonen al** filter om ervoor te zorgen u om het even welke componenten ziet die niet met u worden gedeeld die door een andere beheerder zouden kunnen zijn toegevoegd.<!-- Soon we will make it so any fields that an admin doesn't have access to will be greyed out, and then they can enable the Show all filter to make it editable. --></p><p>**NOTA:** momenteel, **Gelijkaardig aan** sectie omvat slechts componenten u creeert en niet die verstrekt door Adobe. In een toekomstige release worden componenten toegevoegd die door de Adobe worden geleverd.</p> |
   | [!UICONTROL **de verenigbaarheid van het Product**] | Geeft aan waar in de Customer Journey Analytics deze berekende metrische waarde kan worden gebruikt. <p>De mogelijke waarden zijn:</p><ul><li>[!UICONTROL **overal in Customer Journey Analytics**]: Berekende metrisch kan door alle Customer Journey Analytics, met inbegrip van Analysis Workspace, Report Builder, etc. worden gebruikt.</li><li>[!UICONTROL **overal in Customer Journey Analytics (exclusief experimenteren)**]: Berekende metrisch kan door alle Customer Journey Analytics, behalve in het paneel van de Experimentatie worden gebruikt.</li> <p>Voor informatie over de criteria die bepalen of berekende metrisch met experimenteren kan worden gebruikt, zie [ Berekende metriek van het Gebruik in het paneel van de Experimentatie ](/help/analysis-workspace/c-panels/experimentation.md#use-calculated-metrics-in-the-experimentation-panel) in [ het paneel van de Experimentatie ](/help/analysis-workspace/c-panels/experimentation.md).</p></ul> |
   | [!UICONTROL **Markeringen**] | Hiermee worden alle tags weergegeven die op de component zijn toegepast. Gebruikers met beheerdersrechten kunnen tags toevoegen wanneer ze de component bewerken. |
   | [!UICONTROL **Type van Component**] | Hiermee wordt het type component weergegeven dat het is, ongeacht of het een Dimension, Metrisch, Filter of Datumbereik betreft. |
   | [!UICONTROL **die door**] wordt gecreeerd | Geeft de naam weer van de gebruiker die de component heeft gemaakt. |
   | [!UICONTROL **Voorproef**] | Toont een voorproef van hoe de component in Analysis Workspace kijkt. |
   | [!UICONTROL **Datum laatst gewijzigd**] | Hiermee geeft u de dag weer waarop de component voor het laatst is gewijzigd. Deze sectie wordt weergegeven wanneer u Filters, Metriek, Berekende meetgegevens en Datumbereiken weergeeft. |

   {style="table-layout:auto"}

1. Klik **sparen** pictogram ![ Woordenboek van Gegevens sparen pictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_SaveFloppy_18_N.svg) om uw veranderingen te bewaren.
