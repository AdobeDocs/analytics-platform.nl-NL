---
description: Gebruik de stroomvisualisatie in een project van de Werkruimte.
title: Een stroomvisualisatie configureren
feature: Visualizations
role: User, Admin
exl-id: 7055cbc9-19b3-40f0-b8d4-52d241224827
source-git-commit: 5dd25745f3ae872a70f60c53a1340ba59552665d
workflow-type: tm+mt
source-wordcount: '1189'
ht-degree: 1%

---

# Een stroomvisualisatie configureren

Met stroomvisualisaties kunt u de reis begrijpen die voortvloeit uit of leidt tot een specifieke conversiegebeurtenis op uw website of uw app. Het traceert een pad door uw dimensies (en dimensie-items) of metriek. Met stroom kunt u het begin of einde van het pad configureren waarin u bent geïnteresseerd, of alle paden analyseren die door een dimensie- of dimensie-item lopen.

![Nieuwe Flow-interface](assets/new-flow.png)

## Configuratiestappen {#configure}

1. Als u een stroomdiagram wilt maken, voegt u een leeg deelvenster toe aan uw project en klikt u op het pictogram voor visualisatie in de linkertrack. Sleep vervolgens de stroomvisualisatie naar het deelvenster. Of sleep de [!UICONTROL Flow] visualisatie in een bestaand project.

1. Veranker uw stroomvisualisatie met een van de volgende drie opties:

   * [!UICONTROL Starts with] (maateenheden, afmetingen of items), of
   * [!UICONTROL Contains] (afmetingen, of items), of
   * [!UICONTROL Ends with] (maateenheden, afmetingen of items)

   Elk van deze categorieën wordt op het scherm getoond als &quot;dalingsstreek.&quot; U kunt de neerzetzone op drie manieren vullen:

   * Gebruik het keuzemenu om metriek of afmetingen te selecteren.
   * Sleep items vanuit de lijst Afmetingen of Metriek.
   * Gebruik de zoekfunctie om de gewenste metriek of dimensie te zoeken.

   Stel bijvoorbeeld dat u alles wilt traceren wat tot een uitcheckgebeurtenis leidt. U zou een controle-verwante afmeting of metrisch (zoals slepen [!UICONTROL Order exists]) in de **[!UICONTROL Ends with]** dropzone.

1. Als u metrisch kiest, moet u ook verstrekken [!UICONTROL Pathing Dimension], zoals u hier ziet, die u gebruikt om het pad samen te stellen. De standaardwaarde is [!UICONTROL Page].

   ![schilderdimensie](assets/pathing-dim.png)

   >[!IMPORTANT]
   >
   >Berekende metriek kunnen niet in de  **[!UICONTROL Starts with]** of **[!UICONTROL Ends with]** dropzones.

1. (Optioneel) Klik op **[!UICONTROL Show Advanced Settings]** Geavanceerde instellingen configureren:

   ![geavanceerde instellingen](assets/adv-settings.png)

   | Instelling | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Wrap labels]** | Normaal gesproken worden de labels op de Flow-elementen ingekort om de schermruimte op te slaan, maar u kunt het volledige label zichtbaar maken door dit selectievakje in te schakelen.  Standaard = uitgeschakeld. |
   | **[!UICONTROL Include repeat instances]** | Stroomvisualisaties zijn gebaseerd op instanties van een dimensie. Met deze instelling kunt u herhaalde exemplaren, zoals opnieuw laden van pagina&#39;s, opnemen of uitsluiten. Herhalingen kunnen echter niet worden verwijderd uit Flow-visualisaties met multigetaxeerde afmetingen, zoals listVars, listProps, s.product, merchandising Vars, enz. Standaard = uitgeschakeld. |
   | **[!UICONTROL Limit to first/last occurrence]** | Beperk paden tot paden die beginnen/eindigen met de eerste/laatste instantie van een dimensie/item/metrisch. Zie de onderstaande sectie &quot;Voorbeeldscenario voor &#39;beperking tot eerste/laatste voorval&#39;&quot; voor een gedetailleerdere uitleg. |
   | **[!UICONTROL Number of Columns]** | Hiermee bepaalt u hoeveel kolommen u in het stroomdiagram wilt opnemen. |
   | **[!UICONTROL Items expanded per Column]** | Hoeveel punten u in elke kolom wilt. |
   | **[!UICONTROL Flow Container]** | <ul><li>Bezoek</li><li>Bezoeker</li></ul> Hiermee kunt u schakelen tussen Bezoek en Bezoeker om het plakken van bezoekers te analyseren. Met deze instellingen kunt u de betrokkenheid van bezoekers op bezoekersniveau (verschillende bezoeken) begrijpen of de analyse beperken tot één bezoek. |

1. Klik op **[!UICONTROL Build]**.

## De stroomuitvoer weergeven en wijzigen {#output}

![stroomuitvoer](assets/flow-output.png)

Een samenvatting van de configuratie van de Stroom verschijnt bij de bovenkant van het diagram. De paden in het diagram zijn proportioneel. Paden met meer activiteit lijken dikker.

Als u verder naar de gegevens wilt gaan, hebt u verschillende opties:

* Het stroomdiagram is interactief. Plaats de muis boven het diagram om de weergegeven details te wijzigen.

* Wanneer u op een knoop in het diagram klikt, verschijnen de details voor die knoop. Klik nogmaals op het knooppunt om het samen te vouwen.

   ![knooppuntdetails](assets/node-details.png)

* U kunt een kolom filteren om alleen bepaalde resultaten weer te geven, zoals inclusief en exclusief, het opgeven van criteria enzovoort.

* Klik op het plusteken (+) aan de linkerkant om een kolom uit te vouwen.

* Met de rechtermuisknop klikt u op de opties die hieronder worden uitgelegd, om de uitvoer verder aan te passen.

* Klik op het potloodpictogram naast het configuratieoverzicht om de flow verder te bewerken of opnieuw samen te stellen met andere opties.

* U kunt uw diagram van de Stroom als deel van het .CSV dossier van een project ook uitvoeren en verder analyseren door te gaan naar **[!UICONTROL Project]** > **[!UICONTROL Download CSV]**.

## Filteren

Boven elke kolom wordt een filter weergegeven wanneer u de muisaanwijzer op de kolom plaatst. Door op het filter te klikken, krijgt u hetzelfde filterdialoogvenster als dat in de tabel Freeform van vandaag bestaat. Dit filter werkt hetzelfde als in de tabel Freeform.

* Gebruik geavanceerde instellingen om bepaalde criteria op te nemen in of uit te sluiten van onze lijst met operatoren.
* Zodra u een punt van de lijst hebt gefiltreerd, zal die specifieke kolom het filtreren weerspiegelen. (Het filter verlaagt het zodat alleen het item wordt weergegeven dat in het filter is toegestaan, of verwijdert alle items behalve het item dat u in het filter wilt gebruiken.
* Alle stroomafwaartse en stroomopwaartse kolommen zouden moeten blijven, zolang er gegevens zijn die in de resterende knopen stromen.
* Nadat het filterpictogram is toegepast, wordt het in blauw weergegeven boven de kolom waarop het filter wordt toegepast.
* Als u een filter wilt verwijderen, klikt u op het filterpictogram om het filtermenu te openen. Verwijder alle toegepaste filters en klik vervolgens op **[!UICONTROL Save]**. De flow moet terugkeren naar de vorige ongefilterde toestand.

## Klikopties met de rechtermuisknop {#right-click}

| Optie | Beschrijving |
|--- |--- |
| [!UICONTROL Focus on this node] | Wijzig de focus in het geselecteerde knooppunt. Het focusknooppunt verschijnt in het midden van het stroomdiagram. |
| [!UICONTROL Start Over] | Hiermee gaat u terug naar de constructor van het Freeform-diagram, waar u een nieuw stroomdiagram kunt maken. |
| [!UICONTROL Create Segment from this point in flow] | Maak een segment. Dit neemt u in de Bouwer van het Segment, waar u het nieuwe segment kunt vormen. |
| [!UICONTROL Breakdown] | Verdeel de knoop neer door beschikbare Dimension, Metriek, of Tijd. |
| [!UICONTROL Trend] | Creeer een trended diagram voor de knoop. |
| [!UICONTROL Expand entire column] | Vouw een kolom uit om alle knooppunten weer te geven. Standaard worden alleen de bovenste vijf knooppunten weergegeven. |
| [!UICONTROL Collapse entire column] | Alle knooppunten in een kolom verbergen. |
| [!UICONTROL Exclude Item]/[!UICONTROL Restore Excluded Items] | Hiermee verwijdert u een specifiek knooppunt uit de kolom en maakt u het automatisch als filter boven aan de kolom. Als u het uitgesloten item wilt herstellen, klikt u nogmaals met de rechtermuisknop en selecteert u **[!UICONTROL Restore Excluded Item]**. U kunt het filter ook boven aan de kolom openen en de pillarbox verwijderen met het item dat u zojuist hebt uitgesloten. |

## Voorbeeldscenario voor &#39;beperking tot eerste/laatste voorkomen&#39;

Houd er bij het gebruik van deze optie rekening mee dat:

* **[!UICONTROL Limit to first/last occurrence]** alleen het eerste/laatste exemplaar in de reeks telt. Alle andere exemplaren van het **[!UICONTROL Starts with]** of **[!UICONTROL Ends with]** criteria worden genegeerd.
* Indien gebruikt met een **[!UICONTROL Starts with]** stroom, slechts wordt het eerste voorkomen dat de begincriteria aanpast inbegrepen.
* Indien gebruikt met een **[!UICONTROL Ends with]** flow, alleen de laatste instantie die aan de eindcriteria voldoet, wordt opgenomen.
* De gebruikte reeks verschilt op basis van de container. Als u de **[!UICONTROL Visit]** container, de reeks hits zal de sessie zijn. Als u de **[!UICONTROL Visitor]** container, zijn de reeksen klapjes alle klappen voor een bepaalde gebruiker in de verstrekte datumwaaier.
* De **[!UICONTROL Limit to first/last occurrence]** Deze optie kan in de geavanceerde instellingen worden geconfigureerd wanneer u een Metrisch of Dimension-item gebruikt in de velden &quot;Begint met&quot; of &quot;Eindigt met&quot;.

Voorbeeld van een serie hits:

Home > Producten > Toevoegen aan winkelwagentje > Producten > Toevoegen aan winkelwagentje > Facturering > Bevestiging bestellen

### Overweeg een stroomanalyse met de volgende instellingen:

* Beginnen met[!UICONTROL  Add to cart] (Dimension-item)
* [!UICONTROL Page] schilderdimensie
* [!UICONTROL Visit] container

Als &quot;Beperken tot eerste/laatste voorkomen&quot; is uitgeschakeld, telt deze enkele reeks hits 2 exemplaren van &quot;Toevoegen aan winkelwagentje&quot;.
Verwachte stroomuitvoer: &quot;Toevoegen aan winkelwagentje&quot; (2) —> &quot;Producten&quot; (1) -> &quot;Facturering&quot; (1)

Als &quot;Beperking tot eerste/laatste voorkomen&quot; echter is ingeschakeld, wordt alleen de eerste keer dat &quot;Toevoegen aan winkelwagentje&quot; voorkomt in de analyse opgenomen.
Verwachte stroomuitvoer: &quot;Toevoegen aan winkelwagentje&quot; (1) —> &quot;Producten&quot; (1)

### Bekijk dezelfde reeks resultaten, maar gebruik daarbij de volgende instellingen:

* Eindigt met [!UICONTROL Add to cart] (Dimension-item)
* [!UICONTROL Page] schilderdimensie
* [!UICONTROL Visit] container

Indien **[!UICONTROL Limit to first/last occurrence]** is *uitgeschakeld*Deze enkele reeks hits telde 2 exemplaren van &#39;Toevoegen aan winkelwagentje&#39;.
Verwachte stroomuitvoer: &quot;Producten&quot; (2) &lt;— &quot;Toevoegen aan winkelwagentje&quot; (2)

Als **[!UICONTROL Limit to first/last occurrence]** is *enabled*, alleen de laatste keer dat [!UICONTROL Add to cart] in de analyse worden opgenomen.
Verwachte stroomuitvoer: &quot;Producten&quot; (1) &lt;— &quot;Toevoegen aan winkelwagentje&quot; (1)
