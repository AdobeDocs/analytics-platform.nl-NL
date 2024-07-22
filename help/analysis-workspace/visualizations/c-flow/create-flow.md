---
description: Leer hoe u de stroomvisualisatie gebruikt in een Workspace-project.
title: Hoe te om een stroomvisualisatie te vormen
feature: Visualizations
exl-id: 7055cbc9-19b3-40f0-b8d4-52d241224827
role: User
source-git-commit: b196b8c05ba05a3f46d71c10fdcaa2ad8ef0dcd6
workflow-type: tm+mt
source-wordcount: '1483'
ht-degree: 0%

---

# Een stroomvisualisatie configureren

Stroomvisualisaties helpen u de reis te begrijpen die voortvloeit uit of leidt tot een specifieke conversiegebeurtenis op uw website of uw app. Het traceert een pad door uw dimensies (en dimensie-items) of metriek.

Met stroomvisualisaties kunt u het begin of einde van het pad configureren waarin u bent geïnteresseerd, of alle paden analyseren die door een dimensie- of dimensie-item lopen.

![ het de configuratiescherm van de Stroom die Begint met, bevat, en eindigt met gebieden.](assets/new-flow.png)

## Stroomvisualisatie maken {#configure}

1. Voeg een leeg paneel aan uw project toe, selecteer het pictogram Visualisaties in het linkerspoor, dan sleep de [!UICONTROL **Stroom**] visualisatie in het paneel.

   of

   Voeg een visualisatie op om het even welke die manieren toe in &quot;worden beschreven visualisaties aan een paneel&quot;sectie in [ Visualisaties overzicht ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md).

1. Veranker uw stroomvisualisatie met een van de volgende opties:

   * [!UICONTROL **begint met**] (metriek, dimensies, of punten), of
   * [!UICONTROL **bevat**] (afmetingen, of punten), of
   * [!UICONTROL **eindigt met**] (metriek, dimensies, of punten)

   Elk van deze categorieën wordt op het scherm weergegeven als een &quot;dropzone&quot;. U kunt de neerzetzone op drie manieren vullen:

   * Gebruik het keuzemenu om metriek of afmetingen te selecteren.
   * Sleep afmetingen of metriek van de linkerspoorstaaf.
   * Typ de naam van een dimensie of metrisch en selecteer deze wanneer deze in de vervolgkeuzelijst wordt weergegeven.

   >[!IMPORTANT]
   >
   >Berekende metriek kunnen niet worden gebruikt in de velden **[!UICONTROL Starts with]** en **[!UICONTROL Ends with]** .

1. Als u metrisch kiest, moet u ook a [!UICONTROL **het Schilderen Dimension**] verstrekken om als uw weg te gebruiken die aan of uit uw geselecteerde component leiden, zoals hier getoond. Het gebrek is [!UICONTROL **Pagina**].

   ![ De het Schilderen dimensie.](assets/pathing-dim.png)

1. (Optioneel) Selecteer **[!UICONTROL Show advanced settings]** om een van de volgende opties te configureren:

   ![ Geavanceerde montages met de opties van het Weergave, Aantal kolommen en de container van de Stroom.](assets/adv-settings.png)

   | Instelling | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Wrap labels]** | Normaal gesproken worden de labels op de Flow-elementen ingekort om de schermruimte op te slaan, maar u kunt het volledige label zichtbaar maken door dit selectievakje in te schakelen.  Standaard = uitgeschakeld. |
   | **[!UICONTROL Include repeat instances]** | Stroomvisualisaties zijn gebaseerd op instanties van een dimensie. Met deze instelling kunt u herhaalde exemplaren, zoals opnieuw laden van pagina&#39;s, opnemen of uitsluiten. Herhalingen kunnen echter niet worden verwijderd uit Flow-visualisaties met multigetaxeerde afmetingen, zoals listVars, listProps, s.product, merchandising Vars, enz. <p>Deze optie is standaard uitgeschakeld.</p> |
   | **[!UICONTROL Limit to first/last occurrence]** | Beperk paden tot paden die beginnen/eindigen met de eerste/laatste instantie van een dimensie/item/metrisch. Zie de sectie hieronder, [ scenario van het Voorbeeld voor &quot;grens aan eerste/laatste voorkomen&quot;](#example-scenario-for-limit-to-firstlast-occurrence), voor een meer gedetailleerde verklaring. |
   | **[!UICONTROL Number of columns]** | Het aantal kolommen u in uw diagram van de Stroom wilt. U kunt maximaal vijf kolommen opgeven. |
   | **[!UICONTROL Items expanded per column]** | Het aantal items dat u in elke kolom wilt opnemen. U kunt maximaal tien items opgeven die per kolom worden uitgevouwen. |
   | **[!UICONTROL Flow container]** | <ul><li>Bezoek</li><li>Bezoeker</li></ul> Hiermee kunt u schakelen tussen Bezoek en Bezoeker om het plakken van bezoekers te analyseren. Met deze instellingen kunt u de betrokkenheid van bezoekers op bezoekersniveau (verschillende bezoeken) begrijpen of de analyse beperken tot één bezoek. |

   >[!IMPORTANT]
   >
   >De combinatie van **[!UICONTROL Number of columns]** en **[!UICONTROL Items expanded per column]** bepaalt het aantal onderliggende aanvragen dat vereist is om de flowvisualisatie te maken. Hoe hoger deze getallen, hoe langer het duurt om een visualisatie te renderen.


1. Selecteer **[!UICONTROL Build]** .

>[!INFO]
>
>**Voorbeeld:** veronderstel dat u de weg wilt vinden die de gebruikers zowel aan als van de populairste pagina&#39;s op uw plaats namen.
>
>Om dit te doen, zou u
>
>1. Beginnen met het maken van een stroomvisualisatie zoals hierboven beschreven.
>1. Sleep de [!UICONTROL **dimensie van de Pagina**] in het **[!UICONTROL Contains]** gebied, dan uitgezocht [!UICONTROL **bouwt**].
>1. De stroomvisualisatie bouwt verder met de meest bekeken pagina zichtbaar in het focusknooppunt in het midden van de visualisatie. U ziet ook de bovenste pagina&#39;s die naar die pagina lopen (links van het focusknooppunt) en de bovenliggende pagina&#39;s die uit die pagina lopen (rechts van het focusknooppunt).
>1. Analyseer gegevens in de stroom, zoals die in [ worden beschreven Mening en verander de output van de Stroom ](#view-and-change-the-flow-output).

## De stroomuitvoer weergeven en wijzigen {#output}

![ de outputvoorbeeld van de Stroom die Eindigt met Bezoekingen toont, die afmeting schilderen: Pagina, en de container van de Stroom: Dichters.](assets/flow-output.png)

Een samenvatting van de configuratie van de Stroom verschijnt bij de bovenkant van het diagram. De paden in het diagram zijn proportioneel. Paden met meer activiteit lijken dikker.

Als u verder naar de gegevens wilt gaan, hebt u verschillende opties:

* Het stroomdiagram is interactief. Plaats de muis boven het diagram om de weergegeven details te wijzigen.

* Wanneer u op een knoop in het diagram klikt, verschijnen de details voor die knoop. Klik nogmaals op het knooppunt om het samen te vouwen.

  ![ het interactieve stroomdiagram dat van het Voorbeeld knoop-details toont.](assets/node-details.png)

* U kunt een kolom filteren om alleen bepaalde resultaten weer te geven, zoals inclusief en exclusief, het opgeven van criteria enzovoort.

* Klik op het plusteken (+) links om een kolom uit te vouwen.

* Met de rechtermuisknop klikt u op de opties die hieronder worden uitgelegd, om de uitvoer verder aan te passen.

* Klik op het potloodpictogram naast het configuratieoverzicht om de flow verder te bewerken of opnieuw samen te stellen met andere opties.

* U kunt het stroomdiagram ook exporteren en verder analyseren als onderdeel van het CSV-bestand van een project door naar **[!UICONTROL Project]** > **[!UICONTROL Download CSV]** te gaan.

## Filteren

Boven elke kolom wordt een filter weergegeven wanneer u de muisaanwijzer op de kolom plaatst. Door op het filter te klikken, krijgt u hetzelfde filterdialoogvenster als dat in de tabel Freeform van vandaag bestaat. Dit filter werkt hetzelfde als in de tabel Freeform.

* Gebruik geavanceerde instellingen om bepaalde criteria op te nemen in of uit te sluiten van onze lijst met operatoren.
* Zodra u een punt van de lijst hebt gefiltreerd, zal die specifieke kolom het filtreren weerspiegelen. (Het filter verlaagt het zodat alleen het item wordt weergegeven dat in het filter is toegestaan, of verwijdert alle items behalve het item dat u in het filter wilt gebruiken.
* Alle stroomafwaartse en stroomopwaartse kolommen zouden moeten blijven, zolang er gegevens zijn die in de resterende knopen stromen.
* Nadat het filterpictogram is toegepast, wordt het in blauw weergegeven boven de kolom waarop het filter wordt toegepast.
* Als u een filter wilt verwijderen, klikt u op het filterpictogram om het filtermenu te openen. Verwijder eventueel toegepaste filters en klik op **[!UICONTROL Save]** . De flow moet terugkeren naar de vorige ongefilterde toestand.

## Klikopties met de rechtermuisknop {#right-click}

| Optie | Beschrijving |
|--- |--- |
| [!UICONTROL Focus on this node] | Wijzig de focus in het geselecteerde knooppunt. Het focusknooppunt verschijnt in het midden van het stroomdiagram. |
| [!UICONTROL Start over] | Hiermee gaat u terug naar de constructor van het Freeform-diagram, waar u een nieuw stroomdiagram kunt maken. |
| [!UICONTROL Create filter for this path] | Maak een filter. Dit neemt u in de Bouwer van de Filter, waar u de nieuwe filter kunt vormen. |
| [!UICONTROL Breakdown] | Verdeel de knoop neer door beschikbare Dimensionen, Metriek, of Tijd. |
| [!UICONTROL Filter column] | Dezelfde filteropties worden weergegeven als beschikbaar zijn in de tabel Vrije vorm. Voor meer informatie over de beschikbare opties, zie de sectie &quot;een eenvoudig of geavanceerd filter op een lijst&quot;in [ Filter en sorteerlijsten ](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md) toepassen. |
| [!UICONTROL Exclude item]/[!UICONTROL Restore excluded items] | Hiermee verwijdert u een specifiek knooppunt uit de kolom en maakt u het automatisch als filter boven aan de kolom. Als u het uitgesloten item wilt herstellen, klikt u nogmaals met de rechtermuisknop en selecteert u **[!UICONTROL Restore Excluded Item]** . U kunt het filter ook boven aan de kolom openen en de pillarbox verwijderen met het item dat u zojuist hebt uitgesloten. |
| [!UICONTROL Trend] | Creeer een trended diagram voor de knoop. |
| Volgende kolom tonen/Vorige kolom tonen | Geeft de volgende (rechts) of vorige (links) kolom van de visualisatie aan. |
| Kolom verbergen | Hiermee verbergt u de geselecteerde kolom uit de visualisatie. |
| [!UICONTROL Expand entire column] | Breid een kolom uit om alle knopen te tonen. Standaard worden alleen de bovenste vijf knooppunten weergegeven. |
| publiek maken van selectie | Hiermee maakt u een publiek op basis van de geselecteerde kolom. |
| [!UICONTROL Collapse entire column] | Alle knooppunten in een kolom verbergen. |

## Voorbeeldscenario voor &#39;beperking tot eerste/laatste voorkomen&#39;

Houd er bij het gebruik van deze optie rekening mee dat:

* **[!UICONTROL Limit to first/last occurrence]** telt alleen het eerste/laatste exemplaar in de reeks. Alle andere gevallen van de criteria **[!UICONTROL Starts with]** of **[!UICONTROL Ends with]** worden genegeerd.
* Bij gebruik met een **[!UICONTROL Starts with]** -flow wordt alleen de eerste instantie die aan de begincriteria voldoet, opgenomen.
* Bij gebruik met een **[!UICONTROL Ends with]** -flow wordt alleen de laatste instantie opgenomen die aan de eindcriteria voldoet.
* De gebruikte reeks verschilt op basis van de container. Als u de container **[!UICONTROL Visit]** gebruikt, wordt de reeks gebeurtenissen de sessie. Als u de container **[!UICONTROL Visitor]** gebruikt, zijn alle gebeurtenissen voor een bepaalde gebruiker in het opgegeven datumbereik.
* De optie **[!UICONTROL Limit to first/last occurrence]** kan in de geavanceerde montages worden gevormd wanneer het gebruiken van een Metrisch of Punt van het Dimension in &quot;begint met&quot;of &quot;beëindigt met&quot;gebieden.

Voorbeelden van gebeurtenissen:

Home > Producten > Toevoegen aan winkelwagentje > Producten > Toevoegen aan winkelwagentje > Facturering > Bevestiging bestellen

### Overweeg een stroomanalyse met behulp van de volgende instellingen:

* Beginnen met [!UICONTROL  Add to cart] (item Dimension)
* [!UICONTROL Page] dimensie van het plakken
* [!UICONTROL Visit] container

Als &quot;Beperken tot eerste/laatste voorkomen&quot; is uitgeschakeld, telt deze enkele reeks gebeurtenissen 2 exemplaren van &quot;Toevoegen aan winkelwagentje&quot;.
Verwachte stroomuitvoer:
&quot;Toevoegen aan winkelwagentje&quot; (2) —> &quot;Producten&quot; (1)
-> &quot;Facturering&quot; (1)

Als &quot;Beperking tot eerste/laatste voorkomen&quot; echter is ingeschakeld, wordt alleen de eerste keer dat &quot;Toevoegen aan winkelwagentje&quot; voorkomt in de analyse opgenomen.
Verwachte stroomuitvoer:
&quot;Toevoegen aan winkelwagentje&quot; (1) —> &quot;Producten&quot; (1)

### Bekijk dezelfde serie gebeurtenissen, maar gebruik daarbij de volgende instellingen:

* Eindigt met [!UICONTROL Add to cart] (Dimension-item)
* [!UICONTROL Page] dimensie van het plakken
* [!UICONTROL Visit] container

Als **[!UICONTROL Limit to first/last occurrence]** ** gehandicapt is, dan zou deze enige reeks gebeurtenissen 2 voorkomen van &quot;toevoegen aan Kaart&quot;tellen.
Verwachte stroomuitvoer:
&quot;Producten&quot; (2) &lt;— &quot;Toevoegen aan winkelwagentje&quot; (2)

Nochtans, als **[!UICONTROL Limit to first/last occurrence]** ** wordt toegelaten, slechts zou het laatste voorkomen van [!UICONTROL Add to cart] in de analyse worden omvat.
Verwachte stroomuitvoer:
&quot;Producten&quot; (1) &lt;— &quot;Toevoegen aan winkelwagentje&quot; (1)
