---
description: De visualisatie van het canvas voor een reis configureren
title: Reiscanvas
feature: Visualizations
role: User
exl-id: 53984934-6fba-4f15-aeeb-d91039260553
source-git-commit: 770320a0b16d26e0755203a3524b000db30cac82
workflow-type: tm+mt
source-wordcount: '6207'
ht-degree: 0%

---

# De visualisatie van het canvas voor een reis configureren

Met de reiscanvasvisualisatie kunt u uitgebreide inzichten analyseren en verkrijgen over de reizen die u aan uw gebruikers en klanten biedt.

![ het canvas van de Reis ](assets/journey-canvas.png)

## Overzicht van het reiscanvas

Zie [ Overzicht van het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md) om meer over het canvas van de Reis te leren, die omvatten:

* Belangrijkste kenmerken

* Potentiële inzichten

* Verschillen tussen het canvas van de Reis en Fallout

* Details over het analyseren van Journey Optimizer-reizen

* En meer

## Beginnen met het maken van een reis canvasvisualisatie

1. Voeg een leeg paneel aan uw project toe, selecteer het [!UICONTROL **Visualisaties**] pictogram in het linkerspoor, dan sleep ![ GraphPathing ](/help/assets/icons/Branch3.svg) [!UICONTROL **het canvas van de Reis**] visualisatie in het paneel.

   of

   Voeg een visualisatie van het canvas van de Reis op om het even welke die manieren toe in [ worden beschreven visualisaties aan een paneel ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel) sectie in [ Overzicht van Visualisaties ](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md) toevoegen.

   ![ de configuratie van het canvas van de Reis ](assets/journey-canvas-configure.png)

1. Geef de volgende basisinformatie op om het canvas Reis te configureren:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **Primaire metrisch**] | Bepaalt metrisch die wordt gebruikt wanneer het berekenen van het percentage en aantalwaarden op elke knoop in de reis.<p>**Nota**: Het werkingsgebied van de gegevens inbegrepen in elk percentage en aantalwaarde wordt bepaald door metrisch die u op het **[!UICONTROL Journey canvas container]** gebied kiest. Als **[!UICONTROL Person]** bijvoorbeeld is ingesteld als container, hebben de statistieken die in de reis worden weergegeven betrekking op meerdere sessies voor een bepaalde persoon. Als **[!UICONTROL Session]** als container wordt geplaatst, dan worden de statistieken die in de reis worden getoond beperkt tot één bepaalde zitting voor een bepaalde persoon.</p><p>Overweeg de volgende voorbeelden van hoe primaire metrisch het percentage en aantalwaarden van elke knoop beïnvloedt:</p><ul><li>Als _Mensen_ primaire metrisch en _Persoon_ de container is, dan slechts die mensen die een gebeurtenis hebben die de criteria van elke opeenvolgende knoop in de reis zich door de reis aanpast. De val komt op een knoop voor wanneer een persoon nooit bij om het even welke directe volgende knopen in de reis aankwam. Ze hebben mogelijk andere acties uitgevoerd op de site, maar ze voldoen niet aan de criteria die zijn gedefinieerd door de knooppunten die onmiddellijk volgen.</li><li>Als _Mensen_ primaire metrische en _Zitting_ de container is, dan slechts die mensen die een gebeurtenis hebben die de criteria van elke knoop in de reis binnen één enkele zittingsbeweging door de reis aanpast. De val komt op een knoop voor wanneer een persoon nooit bij om het even welke directe volgende knopen in de reis binnen één enkele zitting aankwam. Ze hebben mogelijk andere acties uitgevoerd op de site binnen de sessie, maar ze voldoen niet aan de criteria die zijn gedefinieerd door de knooppunten die onmiddellijk volgen.</li></ul> <p>De primaire metrische waarde beïnvloedt de volgende aspecten van de visualisatie van het canvas van de Reis:</p><ul><li>Het totale aantal dat op elke knoop wordt getoond.  <p>Bijvoorbeeld, als de Gebeurtenissen primaire metrisch zijn, toont elke knoop het aantal mensen die een gebeurtenis hadden die de criteria van die knoop (en elke vorige knoop die tot het in de reis leidt) aanpast.</p></li><li>Het percentage dat op elk knooppunt wordt weergegeven. (Nadat de visualisatie is opgebouwd, kunt u het vervolgkeuzemenu **[!UICONTROL Percentage value]** gebruiken om het percentage van het totaal, het percentage van het vorige knooppunt of het percentage van het beginknooppunt weer te geven.)<p>Bijvoorbeeld, als de Gebeurtenissen primaire metrisch zijn, toont elke knoop het percentage mensen die een gebeurtenis hadden die de criteria van die knoop (en elke vorige knoop die tot het in de reis leiden) aanpast.</p></li><li>Wanneer een afmeting aan visualisatie wordt toegevoegd, worden de hoogste 3 knopen van visualisatie toegevoegd, die op primaire metrisch wordt gebaseerd.</li></ul> |
   | [!UICONTROL **Secundaire metrische**] | Bepaalt secundaire metrisch die wordt gebruikt wanneer het berekenen van het percentage en aantalwaarden op elke knoop in de reis. Secundaire metrisch is facultatief. <p>**Nota**: Het werkingsgebied van de gegevens inbegrepen in elk percentage en aantalwaarde wordt bepaald door metrisch die u op het **[!UICONTROL Journey canvas container]** gebied kiest. Als **[!UICONTROL Person]** bijvoorbeeld is ingesteld als container, hebben de statistieken die in de reis worden weergegeven betrekking op meerdere sessies voor een bepaalde persoon. Als **[!UICONTROL Session]** als container wordt geplaatst, dan worden de statistieken die in de reis worden getoond beperkt tot één bepaalde zitting voor een bepaalde persoon.</p><p>Wanneer secundaire metrisch wordt gevormd, beïnvloedt het de volgende aspecten van de het canvasvisualisatie van de Reis:</p><ul><li>Het totale aantal dat op elke knoop onder primaire metrisch wordt getoond. <p>Bijvoorbeeld, als Accounts secundaire metrisch is, wordt het aantal rekeningen getoond op de knoop voor alle mensen die die knoop in de reis bereikten.</p></li><li>Het percentage dat op elke knoop onder primaire metrisch wordt getoond. (Nadat de visualisatie is opgebouwd, kunt u kiezen of het percentage van het totaal of van het beginknooppunt wordt weergegeven.)</li><p>Bijvoorbeeld, als Sessies secundaire metrisch is, toont elke knoop het percentage zittingen die die knoop in de reis (of het percentage van het totaal of van de beginnende knoop) bereikten.</p></li></ul> |
   | [!UICONTROL **reis van Journey Optimizer**]<!-- name? --> | Selecteer de reis van Journey Optimizer die u als basis voor uw analyse in het canvas van de Reis wilt gebruiken. Er zijn reizen met een van de volgende statussen beschikbaar: Live, Gestopt of Voltooid <p>U kunt deze optie ook leeg laten als u een leeg canvas wilt maken waaruit u de analyse in Analysis Workspace wilt opbouwen.</p> <p>Wanneer u een Journey Optimizer-reis analyseert op het canvas Journey, wordt de reis weergegeven met dezelfde volgorde, volgorde en structuur als in Journey Optimizer. Voor meer informatie, zie [ reizen van Journey Optimizer ](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md#analyze-journey-optimizer-journeys) in [ overzicht van het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md) analyseren.</p><p>**Nota**: Deze optie toont slechts wanneer het gegeven van Journey Optimizer in de zelfde gegevensmening wordt ontdekt die in het paneel van Analysis Workspace wordt geselecteerd waar u de visualisatie toevoegt. Voor informatie over het veranderen van de gegevensmening over een paneel in Analysis Workspace, zie [ overzicht van Analysis Workspace ](/help/analysis-workspace/home.md).</p> |

1. (Facultatief) selecteer [!UICONTROL **tonen geavanceerde montages**], dan specificeer de volgende informatie:

   | Veld | Functie |
   |---------|----------|
   | [!UICONTROL **de container van het canvas van de Reis**] | Kies de container waarop u zich gedurende de hele reis wilt concentreren. De container die u kiest, bepaalt het bereik van de gegevens die tijdens de reis worden vastgelegd. Dit beïnvloedt de statistieken die in visualisatie worden getoond. (Als uw containernamen afwijken van de onderstaande standaardnamen, zijn deze aangepast in de gegevensweergave.)<ul><li>**Zitting:** beperkt de statistieken van visualisatie om binnen één enkele bepaalde zitting voor een bepaalde persoon te vallen. Dit betekent dat de aantallen en de percentages die op elke knoop verschijnen (die op de primaire en secundaire metriek gebaseerd zijn) binnen één enkele zitting voor elke persoon moeten voorkomen. Met andere woorden, één persoon kan meerdere keren op één reis vertegenwoordigd zijn.<p>Deze container gebruikt metrische sessies.</p></li><li>**Persoon:** (Gebrek) staat de statistieken van visualisatie toe om veelvoudige zittingen voor een bepaalde persoon te overspannen. Dit betekent dat de aantallen en de percentages die op elke knoop verschijnen (die op de primaire en secundaire metriek gebaseerd zijn) over om het even welk aantal zittingen kunnen voorkomen, zolang de zittingen aan de zelfde persoon behoren. Met andere woorden, één persoon kan slechts één keer op één reis vertegenwoordigd zijn.<p>Deze container gebruikt metrische Mensen.</p></li></ul> |

1. Selecteer [!UICONTROL **Bouwstijl**].

   Als u een Journey Optimizer-reis hebt geselecteerd, wordt de reis weergegeven met dezelfde volgorde, volgorde en structuur als in Journey Optimizer. (Alleen gebruikers met toegang tot de functie Reis optimaliseren kunnen een Journey Optimizer-reis selecteren.)

   <!-- add screen shot -->

   Als u geen reis van Journey Optimizer selecteerde, toont een leeg canvas waar u kunt beginnen knopen aan de reis toe te voegen. (Alleen gebruikers met toegang tot de functie Reis optimaliseren kunnen een Journey Optimizer-reis selecteren.)

   <!-- add screen shot -->

1. Of u een nieuwe analyse van een leeg canvas creeert of u een reis van Journey Optimizer analyseert, kunt u de reis vormen zoals die in [ wordt beschreven vormt visualiseringsmontages ](#configure-visualization-settings).


## Visualisatie-instellingen configureren

Er zijn verschillende configuratieopties beschikbaar in de koptekst van het canvas Journey.

Instellingen configureren voor de visualisatie van het canvas Reis:

1. In Analysis Workspace, open een bestaande visualisatie van het canvas van de Reis, of [ beginnen bouwend nieuwe ](#begin-building-a-journey-canvas-visualization).

   De opties die u toestaan om de het canvasvisualisatie van de Reis te vormen zijn beschikbaar in de kopbal:

   ![ de kopbalopties van het canvas van de Reis ](assets/journey-canvas-header.png)

1. Vorm om het even welke volgende montages die over de bovenkant van visualisatie worden getoond:

   | Instelling | Functie |
   |---------|----------|
   | [!UICONTROL **Procentuele waarde**] | De percentagewaarde die op elke knoop in de reis wordt getoond.<p>![ percentagewaarde ](assets/journey-canvas-percentage.png)</p> <p>Overweeg het volgende wanneer het vormen van de percentagewaarden die op knopen in de reis worden getoond:</p><ul><li>Een percentage wordt getoond op elke knoop voor primaire metrisch. Een percentage wordt ook getoond voor secundaire metrisch als men wordt gevormd. (Voor meer informatie over de primaire en secundaire metrische montages, zie [ beginnen met de bouw van een visualisatie van het canvas van de Reis ](#begin-building-a-journey-canvas-visualization).)</li><li>De percentages omvatten alle mensen of zittingen die in de gegevensmening binnen de de datumwaaier van het paneel inbegrepen zijn. Of _mensen_ of _zittingen_ wordt gebruikt hangt van container af het plaatsen. (Voor meer informatie over het plaatsen van de container, zie [ beginnen met de bouw van een visualisatie van het canvas van de Reis ](#begin-building-a-journey-canvas-visualization).)</li></ul> <p>Kies een van de volgende opties:</p> <ul><li>[!UICONTROL **Percentage van beginknoop**]: Berekent de percentages die op elke knoop met betrekking tot de beginknoop worden getoond. De percentages zijn gebaseerd op primaire en secundaire metrisch die u selecteerde. <p>A _beginknoop_ is een knoop die geen verbonden knopen heeft die het voorafgaan.</p><p>Een reis kan veelvoudige beginknopen bevatten. Nochtans, [!UICONTROL **Percentage van totaal**] wordt gebruikt als de reis 2 of meer beginknopen bevat die tot een gemeenschappelijke knoop leiden. Als u [!UICONTROL **Percentage van beginknoop**] wilt gebruiken, werk de reis bij zodat elke knoop in de reis terug naar één enkele beginknoop kan worden getraceerd.</p></li><li>[!UICONTROL **Percentage van vorige knoop**]: Berekent de percentages die op elke knoop met betrekking tot de vorige knoop worden getoond. De percentages zijn gebaseerd op primaire en secundaire metrisch die u selecteerde.</li><li>[!UICONTROL **Percentage van totaal**]: Berekent de percentages die op elke knoop met betrekking tot alle gegevens in de gegevensmening worden getoond. De percentages zijn gebaseerd op primaire en secundaire metrisch die u selecteerde.</li></ul> |
   | [!UICONTROL **montages van de Pijl**] | De pijlen die tussen knopen in het canvas van de Reis verschijnen kunnen worden gevormd om douanelabels en waarden te tonen. <p>![ pijlmontages ](assets/journey-canvas-arrow-settings.png)</p><p>_de Etiketten_ zijn douanenamen die op pijlen verschijnen. Op een bepaalde pijl wordt slechts één label weergegeven. De etiketten kunnen om het even welke volgend zijn, en worden getoond in deze orde van voorkeur:</p><ol><li>Een douanenaam die van het canvas van de Reis wordt toegevoegd (zoals die in [ wordt beschreven voegt of werkt een etiket op een pijl ](#add-or-update-a-label-on-an-arrow) bij)</li><li>Een Journey Optimizer-label</li><li>Een Journey Optimizer-voorwaarde</li></ol><p>_Waarden_ zijn de aantallen en de percentages die op pijlen verschijnen, en zij wijzen op de mensen of de zittingen die van één knoop aan de volgende knoop in de reis bewogen. (Met andere woorden, degenen die niet in een bepaalde fase uit de reis zijn gevallen.) </p><p>De volgende opties zijn beschikbaar voor reizen die niet uit Journey Optimizer voortkwamen en voor reizen van Journey Optimizer die niet significant zijn gewijzigd in het canvas van de Reizen: (Belangrijke wijzigingen omvatten het toevoegen of verwijderen van knopen, het toevoegen of verwijderen van pijlen, of het veranderen van de componenten van een knoop.)</p><ul><li>[!UICONTROL **Geen etiketten**]: Geen etiketten worden getoond op pijlen in de reis. </br> Deze optie is alleen beschikbaar als de rit is gewijzigd in </li><li>[!UICONTROL **Etiketten slechts**]: De etiketten worden getoond op pijlen in de reis.</li></ul><p>De volgende opties zijn beschikbaar voor Journey Optimizer-reizen die aanzienlijk zijn gewijzigd in Reis canvas: (Belangrijke wijzigingen zijn het toevoegen of verwijderen van knooppunten, het toevoegen of verwijderen van pijlen of het wijzigen van de componenten van een knooppunt.)(**Nota**: Deze optiesvertoning slechts wanneer het gegeven van Journey Optimizer in de zelfde gegevensmening wordt ontdekt die in het paneel van Analysis Workspace wordt geselecteerd waar u de visualisatie toevoegt. Voor informatie over het veranderen van de gegevensmening over een paneel in Analysis Workspace, zie [ overzicht van Analysis Workspace ](/help/analysis-workspace/home.md).)</p><ul><li>[!UICONTROL **Geen etiketten of waarden**]: Geen etiketten of waarden worden getoond op pijlen in de reis.</li><li>[!UICONTROL **Etiketten slechts**]: Slechts worden de etiketten getoond op pijlen in de reis. Waarden worden niet weergegeven.</li><li>[!UICONTROL **Waarden slechts**]: Slechts worden de waarden getoond op pijlen in de reis. Labels worden niet weergegeven.</li><li>[!UICONTROL **Waarden en etiketten**]: Zowel worden de etiketten als de waarden getoond op pijlen in de reis.</li></ul> |
   | [!UICONTROL **toon reserve**] | De gegevens van de reserve tonen een percentage en aantal dat uit elke knoop van de reis valt. Falloutgegevens zijn gebaseerd op de metrische waarde die is gekoppeld aan de containerinstellingen van de reis; ze zijn niet gebaseerd op de primaire of secundaire metrische waarde. <p>![ fallout ](assets/journey-canvas-fallout.png)</p><p>Door gebrek, is de container _Persoon_, zodat metrisch die voor reservegegevens wordt gebruikt _Mensen_ is. Als de container in _Zitting_ wordt veranderd, metrisch gebruikt voor reservegegevens is _Zittingen_, etc.</p><p>Bijvoorbeeld, met _Persoon_ als container die, toont de reserve het percentage en het aantal mensen op elke knoop van de reis die nooit bij om het even welke directe volgende knopen aankwam. Ze hebben mogelijk andere acties uitgevoerd op de site, maar ze voldoen niet aan de criteria die zijn gedefinieerd door de knooppunten die onmiddellijk volgen.</p> <p>Voor meer informatie over het plaatsen van de container van het canvas van de Reis, zie [ beginnen bouwend een visualisatie van het canvas van de Reis ](#begin-building-a-journey-canvas-visualization). |
   | **controles van het Gezoem** | De volgende zoomknoppen zijn beschikbaar in de rechterbovenhoek van het canvas:<ul><li>**Gezoem binnen** ![ zoom in pictogram ](assets/zoom-in-icon.png): Vergroot specifieke gebieden van visualisatie.<p>U kunt ook muisbesturingselementen gebruiken, zoals vastzetten op een trackpad.</p></li><li>**Gezoem uit** ![ zoom uit pictogram ](assets/zoom-out-icon.png): Verkleint visualisatie om meer ruimte op het canvas toe te staan.<p>U kunt ook muisbesturingselementen gebruiken, zoals vastzetten op een trackpad.</p></li><li>**het scherm van de Passendheid** ![ past het het schermpictogram ](assets/fill-screen-icon.png): Past huidige gezoem en pan montages aan om het scherm met volledige visualisatie te vullen.</li></ul><p>Als u wilt pannen over het canvas nadat u hebt in- of uitgezoomd, klikt u met de muis en sleept u naar de gewenste locatie.</p> |

1. Ga met [ verder voeg knopen ](#add-nodes) toe.

## Knooppunten toevoegen

De knopen in een het canvasvisualisatie van de Reis vertegenwoordigen de gebeurtenissen of de acties van een gebruikersreis.

U kunt op de volgende manieren knooppunten maken: door Workspace-componenten van de linkerspoorstaaf naar het canvas te slepen, door Reader toe te staan de bovenste volgende of vorige knooppunten te kiezen op basis van bestaande knooppunten, of door bestaande knooppunten te dupliceren.

### Componenten slepen vanaf de linkerspoorstaaf

1. In Analysis Workspace, open een bestaande visualisatie van het canvas van de Reis, of [ beginnen bouwend nieuwe ](#begin-building-a-journey-canvas-visualization).

1. Sleep metriek, afmetingen, afmetingspunten, segmenten, of datumwaaiers van de linkerspoorstaaf op het canvas. De metriek die op a [ afgeleid gebied ](/help/data-views/derived-fields/derived-fields.md) gebaseerd zijn wordt gesteund. Nochtans, worden de berekende metriek, evenals om het even welke metriek of dimensies die op a [ summiere dataset ](/help/data-views/summary-data.md) gebaseerd zijn niet gesteund.

   U kunt meerdere componenten in de linkertrack selecteren door Shift ingedrukt te houden of door Command (in Mac) of Ctrl (in Windows) ingedrukt te houden.

   De visualisatie wordt als volgt bijgewerkt op basis van de primaire meting (afhankelijk van het componenttype en het gebied van het canvas waar u het plaatst):

   | Componenttype | Plaatsing van onderdeel | Visualisatie-updates nadat het knooppunt is toegevoegd |
   |---------|----------|----------|
   | Metrisch | Leeg gebied van canvas | De knoop toont waar de component werd gelaten vallen, los van om het even welke bestaande knopen. |
   | Metrisch | Een bestaand knooppunt | De component wordt automatisch gecombineerd met het bestaande knooppunt. (Zie [ knopen ](#combine-nodes) voor meer informatie combineren.)</p> |
   | Metrisch | Een pijl tussen 2 bestaande knooppunten | De knoop toont tussen de twee bestaande knopen waar de component werd gelaten vallen en met beide bestaande knopen verbonden. (Zie [ verbind knopen ](#connect-nodes) voor meer informatie.)</p> |
   | Dimension | Leeg gebied van canvas | Er worden 3 knooppunten gemaakt voor de bovenste 3 dimensieitems waar de component is neergezet, zonder verbinding met bestaande knooppunten. (**Nota:** als slechts 1 of 2 knopen tonen, betekent het dat het gegeven voor slechts 1 of 2 van de afmetingspunten beschikbaar is. Als er geen knooppunten worden weergegeven, betekent dit dat er geen gegevens beschikbaar zijn voor de dimensie-items. In dit geval, probeer toevoegend het aan een verschillend punt van de reis, pas de de datumwaaier van de visualisatie aan, of kies een verschillende afmeting.)<p>Houd Shift ingedrukt wanneer u de dimensie op het canvas neerzet om deze toe te voegen als één knooppunt met 3 dimensie-items.</p><p></p> |
   | Dimension | Een bestaand knooppunt | Een mislukking wordt automatisch toegepast op de knoop met top 5 getoonde afmetingspunten.<!--what happens if you hold Shift?--><p>Om de mislukking in een nieuwe vrije lijstvisualisatie te bekijken, selecteer [!UICONTROL **Open in een vrije vormlijst**] verbinding op de knoop.</p> |
   | Dimension | Een pijl die 2 bestaande knopen verbindt | Er worden 3 knooppunten gemaakt voor de bovenste 3 dimensiepunten die de eerste gebeurtenis na het eerste knooppunt volgen (van personen/sessies die uiteindelijk het tweede knooppunt bereiken). De knopen tonen tussen de twee bestaande knopen waar de component werd gelaten vallen en elke knoop wordt verbonden met beide bestaande knopen. (**Nota:** als slechts 1 of 2 knopen tonen, betekent het dat het gegeven voor slechts 1 of 2 van de afmetingspunten beschikbaar is. Als er geen knooppunten worden weergegeven, betekent dit dat er geen gegevens beschikbaar zijn voor de dimensie-items. In dit geval, probeer toevoegend het aan een verschillend punt van de reis, pas de de datumwaaier van de visualisatie aan, of kies een verschillende afmeting.)<p>Houd Shift ingedrukt wanneer u de dimensie op het canvas neerzet om deze toe te voegen als één knooppunt met 3 dimensie-items. (Zie [ verbind knopen ](#connect-nodes) voor meer informatie.)</p> |
   | Dimension-item | Leeg gebied van canvas | De knoop toont waar de component werd gelaten vallen, los van om het even welke bestaande knopen. |
   | Dimension-item | Een bestaand knooppunt | De component wordt automatisch gecombineerd met het bestaande knooppunt. |
   | Dimension-item | Een pijl die 2 bestaande knopen verbindt | De knoop toont tussen de twee bestaande knopen waar de component werd gelaten vallen en met beide bestaande knopen verbonden. (Zie [ verbind knopen ](#connect-nodes) voor meer informatie.)</p> |
   | Filter | Leeg gebied van canvas | Het knooppunt geeft aan waar de component is neergezet zonder verbinding met andere knooppunten.<p>Het aantal en het percentage dat op de knoop verschijnen omvatten het totaal van primaire metrisch, die door het segment wordt gesegmenteerd u selecteerde.</p> <p>Bijvoorbeeld, als de Mensen als primaire metrisch voor de reis wordt geselecteerd, dan het toevoegen van een segment van Vandaag aan een leeg gebied van het canvas toont alle mensen die een gebeurtenis vandaag hadden.</p> |
   | Filter | Een bestaand knooppunt | Past het segment op de bestaande knoop toe. |
   | Filter | Een pijl die 2 knooppunten verbindt | De knoop toont tussen de twee bestaande knopen waar de component werd gelaten vallen en met beide bestaande knopen verbonden. (Zie [ verbind knopen ](#connect-nodes) voor meer informatie.)</p><p>Past het segment op het punt op de weg toe waar de component werd gelaten vallen.</p> |
   | Datumbereik | Leeg gebied van canvas | De knoop toont waar de component werd gelaten vallen, losgemaakt van een andere knopen.<p>Het aantal en het percentage dat op de knoop verschijnen omvatten het totaal van primaire metrisch, die door de datumwaaier wordt gesegmenteerd u selecteerde.</p> <p>Als Personen bijvoorbeeld is geselecteerd als de primaire metrische waarde voor de rit, worden bij het toevoegen van een datumbereik van Deze maand aan een leeg gebied van het canvas alle personen weergegeven die een gebeurtenis hebben gehad tijdens de huidige maand.</p> |
   | Datumbereik | Een bestaand knooppunt | Past het datumbereik toe op het bestaande knooppunt. |
   | Datumbereik | Een pijl die 2 knooppunten verbindt | De knoop toont tussen de twee bestaande knopen waar de component werd gelaten vallen en met beide bestaande knopen verbonden. (Zie [ verbind knopen ](#connect-nodes) voor meer informatie.)</p><p>Past het datumbereik toe op het punt op het pad waar de component is neergezet.</p> |
   | Meerdere componenten | Een leeg gebied van het canvas | **als geen van de componenten afmetingen zijn:**<p>Elke component wordt weergegeven als een afzonderlijk knooppunt waar de componenten zijn neergezet, zonder verbinding met bestaande knooppunten.</p><p>Houd de Shift-toets ingedrukt wanneer u de componenten op het canvas neerzet om ze als één gecombineerd knooppunt toe te voegen. </p><p>**als om het even welke componenten u toevoegt dimensies zijn:**</p><p>Elke component wordt weergegeven als een afzonderlijk knooppunt waar de componenten zijn neergezet, zonder verbinding met bestaande knooppunten.</p><p>Er kan slechts één dimensie tegelijk worden toegevoegd. Wanneer de afmeting wordt toegevoegd, worden 3 knopen gecreeerd voor top 3 afmetingspunten waar de component werd gelaten vallen.</p><p>Houd de Shift-toets ingedrukt wanneer u de componenten op het canvas neerzet om ze als één gecombineerd knooppunt toe te voegen. De top 3 afmetingspunten worden gecombineerd met elke knoop. (Zie [ knopen ](#combine-nodes) voor meer informatie combineren.)</p> |
   | Meerdere componenten | Een bestaand knooppunt | Alle componenten worden gecombineerd met het bestaande knooppunt.<p>Als om het even welke componenten u toevoegt afmetingen zijn, dan worden de top 3 afmetingspunten gecombineerd met de knoop.</p> <p>Er kan slechts één dimensie tegelijk worden toegevoegd.</p> |
   | Meerdere componenten | Een pijl die 2 bestaande knopen verbindt | **als geen van de componenten afmetingen zijn:**<p>Elke component wordt weergegeven als een afzonderlijk knooppunt waar de componenten zijn neergezet en elk knooppunt is verbonden met beide bestaande knooppunten. (Zie [ verbind knopen ](#connect-nodes) voor meer informatie.)</p><p>Houd de Shift-toets ingedrukt wanneer u de componenten op het canvas neerzet om ze als één gecombineerd knooppunt toe te voegen. (De componenten moeten van het zelfde type zijn om in één enkele knoop worden gecombineerd.) (Zie [ knopen ](#combine-nodes) voor meer informatie combineren.)</p><p>**als om het even welke componenten u toevoegt dimensies zijn:**</p><p>Elke component wordt weergegeven als een afzonderlijk knooppunt waar de componenten zijn neergezet en elk knooppunt is verbonden met beide bestaande knooppunten.</p><p>Er kan slechts één dimensie tegelijk worden toegevoegd. Wanneer de dimensie wordt toegevoegd, worden 3 knopen gecreeerd voor top 3 punten van de dimensie die de eerste gebeurtenis na de eerste knoop volgen (van mensen of zittingen die uiteindelijk de tweede knoop bereiken). Elk knooppunt is verbonden met beide bestaande knooppunten. (Zie [ verbind knopen ](#connect-nodes) voor meer informatie.)</p><p>Houd de Shift-toets ingedrukt wanneer u de componenten op het canvas neerzet om ze als één gecombineerd knooppunt toe te voegen. De top 3 afmetingspunten worden gecombineerd met elke knoop, en elke knoop wordt verbonden met beide bestaande knopen. (Zie [ knopen ](#combine-nodes) voor meer informatie combineren.)</p> |

   De knopen tonen als rechthoekig vakje met de volgende informatie:

   * Componentnaam

   * Het componenttype (zoals metrisch of afmeting)

   * Primaire metrische statistieken (totaal en percentage)

   * Secundaire statistieken (totaal en percentage)

   Een pulserend of gloeiend knooppunt geeft aan dat gegevens worden geladen voor dat knooppunt.

1. Herhaal dit proces om door te gaan met het toevoegen van knooppunten om uw reis uit te bouwen.

1. Blijf de reis aanpassen zoals beschreven in de onderstaande secties. U kunt knooppunten verbinden, knooppunten hernoemen, storingen toepassen, publiek maken, tijdbeperkingen toevoegen en nog veel meer.

### Bovenste knooppunten weergeven op basis van bestaande knooppunten

U kunt automatisch de bovenste knooppunten direct weergeven op basis van de knooppunten die zich al op het canvas bevinden. U kunt de bovenste knooppunten toevoegen aan het canvas Journey of deze weergeven in een vrije-vormtabel.

Het canvas van de reis gebruikt primaire metrisch wanneer het bepalen van welke knopen om te tonen.

Deze optie is beschikbaar voor de volgende objecten op het canvas:

* Afzonderlijke knooppunten

* De pijl tussen knooppunten

#### Bovenste knooppunten weergeven na een bestaand knooppunt

U kunt een knoop selecteren en de hoogste afmetingspunten tonen die onmiddellijk na het in de reis komen. U kunt de top 3 afmetingspunten aan het canvas van de Reis als afzonderlijke knopen toevoegen, of u kunt alle hoogste afmetingspunten in een vrije vormlijst bekijken.

1. Klik de knoop met de rechtermuisknop aan waar u de hoogste afmetingspunten wilt tonen die na het in de reis komen.

   De knoop kan geen bestaande knopen hebben die uit het in de reis gaan.

1. Selecteer [!UICONTROL **tonen hoogste knopen na deze knoop**].

1. Selecteer waar u de dimensie-items wilt weergeven:

   * [!UICONTROL **in het canvas van de Reis**]: Voegt top 3 knopen aan het canvas toe die na deze knoop in de reis komen. Elk knooppunt wordt verbonden met het knooppunt dat u hebt geselecteerd als een afzonderlijke vertakking op het canvas.

   * [!UICONTROL **in een lijst Freeform**]: Creeert een vrije lijstvisualisatie die alle hoogste afmetingspunten toont die na deze knoop in de reis komen.

1. Selecteer de gewenste afmeting in de lijst met afmetingen.

   Afhankelijk van wat u in de vorige stap koos, worden top 3 afmetingspunten toegevoegd aan het canvas als 3 afzonderlijke knopen, of alle hoogste afmetingspunten worden getoond in een vrije vormlijst.

#### Bovenste knooppunten weergeven vóór een bestaand knooppunt

U kunt een knoop selecteren en de hoogste afmetingspunten tonen die onmiddellijk vóór het in de reis komen. U kunt de top 3 afmetingspunten aan het canvas van de Reis als afzonderlijke knopen toevoegen, of u kunt alle hoogste afmetingspunten in een vrije vormlijst bekijken.

1. Klik de knoop met de rechtermuisknop aan waar u de hoogste afmetingspunten wilt tonen die vóór het in de reis komen.

   Deze knoop kan geen bestaande knopen hebben die in het in de reis komen.

1. Selecteer [!UICONTROL **tonen hoogste knopen vóór deze knoop**].

1. Selecteer waar u de dimensie-items wilt weergeven:

   * [!UICONTROL **in het canvas van de Reis**]: Voegt top 3 knopen aan het canvas toe die vóór deze knoop in de reis komen. Elk knooppunt wordt verbonden met het knooppunt dat u hebt geselecteerd als een afzonderlijke vertakking op het canvas.

   * [!UICONTROL **in een lijst Freeform**]: Creeert een vrije lijstvisualisatie die alle hoogste afmetingspunten toont die vóór deze knoop in de reis komen.

1. Selecteer de gewenste afmeting in de lijst met afmetingen.

   Afhankelijk van wat u in de vorige stap koos, worden top 3 afmetingspunten toegevoegd aan het canvas als 3 afzonderlijke knopen, of alle hoogste afmetingspunten worden getoond in een vrije vormlijst.

#### Bovenste knooppunten tussen bestaande knooppunten weergeven

U kunt een pijl selecteren en de bovenste dimensie-items tonen die tussen twee bestaande knooppunten in de reis komen. U kunt de top 3 afmetingspunten aan het canvas van de Reis als afzonderlijke knopen toevoegen, of u kunt alle hoogste afmetingspunten in een vrije vormlijst bekijken.

1. Klik met de rechtermuisknop op de pijl tussen de twee knooppunten waar u de bovenste dimensie-items wilt weergeven.

1. Selecteer [!UICONTROL **tonen hoogste knopen tussen deze knopen**].

1. Selecteer waar u de dimensie-items wilt weergeven:

   * [!UICONTROL **in het canvas van de Reis**]: Voegt top 3 knopen aan het canvas toe die tussen de 2 bestaande knopen komen. Elk knooppunt wordt verbonden met de omringende knooppunten als een afzonderlijke vertakking op het canvas.

   * [!UICONTROL **in een lijst Freeform**]: Creeert een vrije lijstvisualisatie die alle hoogste afmetingspunten toont die tussen de 2 bestaande knopen komen.

1. Selecteer de gewenste afmeting in de lijst met afmetingen.

   Afhankelijk van wat u in de vorige stap koos, worden top 3 afmetingspunten toegevoegd aan het canvas als 3 afzonderlijke knopen, of alle hoogste afmetingspunten worden getoond in een vrije vormlijst.

### Dubbele knooppunten

De optie om te dupliceren is beschikbaar voor de volgende objecten op het canvas:

* Afzonderlijke knooppunten

* Meerdere knooppunten

Om knooppunten te dupliceren:

1. Selecteer een of meer knooppunten die u wilt dupliceren.

   Houd Command (in Mac) of Ctrl (in Windows) ingedrukt om meerdere knooppunten te selecteren.

1. Klik met de rechtermuisknop op een van de geselecteerde knooppunten en selecteer vervolgens [!UICONTROL **Dupliceren**] .

## De reis ontwerpen

De volgorde van knooppunten en de verbindingen tussen knooppunten zijn van invloed op de gegevens van het canvas Journey. De reizen zouden de opeenvolging van gebeurtenissen visueel en nauwkeurig moeten weerspiegelen die u wilt melden.

Nadat knooppunten aan het canvas zijn toegevoegd, kunt u deze opnieuw rangschikken, combineren, verbinden en tijdbeperkingen toevoegen.

### Knoppen opnieuw rangschikken

De reizen in het canvas van de Reis bestaan uit een flexibele grafiek van knopen en pijlen die om het even welke combinatie gebeurtenissen, afmetingspunten, en segmenten vertegenwoordigen.

U kunt knooppunten naar het canvas slepen om de gebeurtenissen en omstandigheden van de rit opnieuw te rangschikken.

Terwijl u de volgorde van knooppunten in de rit wijzigt, worden de gegevens dienovereenkomstig bijgewerkt.

### Knooppunten combineren

Een gecombineerd knooppunt in het canvas Journey is een enkel punt in de gebruikersreis (knooppunt) dat 2 of meer componenten bevat die via logica bij elkaar zijn gevoegd.

#### Gecombineerde knooppunten maken

U kunt een van de volgende handelingen uitvoeren om knooppunten te combineren in het canvas Reis:

* Sleep vanaf de linkerrails één component naar een knooppunt op het canvas.

* Sleep vanuit de linkerrails meerdere componenten tegelijk naar een knooppunt op het canvas.

* Sleep vanuit de linkerrails meerdere componenten tegelijk naar een leeg gebied van het canvas terwijl u de Shift-toets ingedrukt houdt.

<!-- * On the canvas, select the nodes that you want to combine, right-click one of the selected nodes, then select **Combine**. Is there a limit on how many you can combine? -->

#### Logica bij het combineren van knooppunten

De logica die op knopen wordt toegepast wanneer zij worden gecombineerd verschilt afhankelijk van welke componententypes u, als volgt combineert:

>[!TIP]
>
>U kunt de logica van een gecombineerde knoop bekijken door de knoop met de rechtermuisknop aan te klikken, dan selecterend [!UICONTROL **creeer segment van knoop**]. De logica wordt getoond in de [!UICONTROL **sectie van de Definitie**].


| Te combineren componenttypen | Gebruikte logica (operator) |
|---------|----------|
| Metrisch + metrisch | Samengevoegd met OR |
| Dimension-item + Dimension-item (vanuit dezelfde bovenliggende dimensie) | Samengevoegd met OR |
| Dimension-item + Dimension-item (van verschillende bovenliggende afmetingen) | Deelnemen met AND |
| Filter + Filter | Deelnemen met AND |
| Dimension + Metrisch, Datumbereik of Filter | Deelnemen met AND |
| Datumbereik + Metrisch, Filter of Dimension | Deelnemen met AND |
| Filter + Metrisch, Datumbereik of Dimension | Deelnemen met AND |

### Verbindingsknooppunten

U kunt knooppunten verbinden die zich al op het canvas bevinden, of u kunt een knooppunt verbinden wanneer u het aan het canvas toevoegt.

U verbindt knopen om de opeenvolging van gebeurtenissen van de reis te bepalen.

#### Pijlen tussen knooppunten

De knopen worden verbonden door een pijl. Zowel de richting van de pijl als de breedte hebben betekenis:

* **Richting**: Wijst op de opeenvolging van gebeurtenissen van de reis

* **Breedte**: Wijst op percentagevolume van één knoop aan een andere

  ![ de richting en de breedte van de Pijl ](assets/journey-canvas-arrow-width.png)

#### Logica wanneer knooppunten worden aangesloten

Wanneer u knopen in het canvas van de Reis verbindt, worden zij verbonden gebruikend de exploitant THEN. Dit is ook gekend als [ opeenvolgend segmenteren ](/help/components/filters/seg-sequential-build.md).

Knooppunten worden verbonden als een &quot;uiteindelijk pad&quot;, wat betekent dat bezoekers worden geteld zolang ze uiteindelijk van de ene naar de andere node gaan, ongeacht gebeurtenissen die zich tussen de twee knooppunten voordoen. De tijd die gebruikers wordt toegewezen om langs het pad te bewegen, wordt bepaald door de containerinstelling. <!-- It can also be controlled by [adding a time constraint](#add-a-time-constraint-between-nodes). -->

U kunt de logica van verbonden knopen bekijken door de knoop met de rechtermuisknop aan te klikken, dan selecterend [!UICONTROL **creeer segment van knoop**]. De logica wordt getoond in de [!UICONTROL **sectie van de Definitie**].

#### Bestaande knooppunten verbinden

De reizen kunnen niet circulair zijn, die terug naar eerder verbonden knopen herhalen.

Om knopen in het canvas van de Reis te verbinden:

1. In een reis canvasvisualisatie, beweegt over de knoop die eerst in de reisopeenvolging komt die u met een andere knoop wilt verbinden.

   Er worden 4 blauwe stippen weergegeven aan elke kant van het geselecteerde knooppunt.

1. Sleep een van de vier blauwe stippen naar een van de vier zijden van het knooppunt waarmee u verbinding wilt maken.

   Er verschijnt een pijl die de twee knooppunten verbindt. Zie [ Pijlen tussen knopen ](#arrows-between-nodes) voor meer informatie.

#### Verbind knopen wanneer het toevoegen van een knoop

Wanneer u een knooppunt aan het canvas toevoegt, kunt u het tussen twee verbonden knooppunten plaatsen. De knoop wordt toegevoegd aan de stroom van de reis tussen de 2 bestaande knopen.

Voor meer informatie, zie [ knopen ](#add-nodes) toevoegen.

<!--

### Add a time constraint between nodes

>[!AVAILABILITY]
>
>This feature is not yet available.

You can set a time constraint between nodes. When a time constraint is in place, people are considered to have fallen out of the journey if they follow the defined journey but take longer than the allotted time period to move between the nodes.

The option to add a time constraint is available for the following objects on the canvas:

* The arrow between nodes

To add a time constraint:

1. In a Journey canvas visualization, right-click the arrow between 2 nodes, then select [!UICONTROL **Add time constraint**].

from Travis: You can set time to be within X amount of time or after X amount of time (those are the only two options I think, but we can check with Brandon). 
1. Choose from the following options: 

-->

## Knooppunten of pijlen beheren

<!--

### Change the color of a node or arrow

>[!AVAILABILITY]
>
>This feature is not yet available.

You can visually customize a journey by changing the color of any node or arrow on the canvas. For example, you could adjust colors to indicate a desirable or undesirable event.

The option to change the color is available for the following objects on the canvas:

* Individual nodes

* The arrow between nodes

To change the color of a node or arrow:

1. In a Journey canvas visualization, right-click the node or arrow whose color you want to change.

1. Select [!UICONTROL **Change color**]. 

1. Select the desired color. 

   The following colors are available: 

-->

### Naam knooppunt wijzigen

Wanneer u een component naar het canvas Journey sleept, wordt een knooppunt gemaakt met dezelfde naam als de componentnaam. U kunt de naam van het knooppunt wijzigen zodat deze beter overeenkomt met de stap van de rit die het knooppunt vertegenwoordigt.

De optie om de naam te wijzigen is beschikbaar voor de volgende objecten op het canvas:

* Afzonderlijke knooppunten

Een knooppunt hernoemen:

1. In een reis canvasvisualisatie, klik de knoop met de rechtermuisknop aan die u wilt anders noemen.

1. Selecteer [!UICONTROL **anders noemen**].

1. Geef een nieuwe naam op en druk op Enter.<!--is that right?-->

### Een label toevoegen of bijwerken op een pijl

De pijlen die tussen knopen in het canvas van de Reis verschijnen kunnen worden gevormd om douanelabels en waarden te tonen.

Labels zijn aangepaste namen die op pijlen worden weergegeven. Op een bepaalde pijl wordt slechts één label weergegeven.

Voor meer informatie over de etiketten en de waarden die op pijlen verschijnen, zie de &quot;montages van de Pijl&quot;in [ visualisatie montages ](#configure-visualization-settings) vormen.

De optie om een label toe te voegen of bij te werken is beschikbaar voor de volgende objecten op het canvas:

* De pijl tussen knooppunten

Een label toevoegen aan een pijl:

1. Klik in een reiscanvasvisualisatie met de rechtermuisknop op de plaats waar u een label wilt toevoegen.

1. Selecteer **[!UICONTROL Add label]** .

1. Geef een naam voor het label op en druk op Enter.

   Als de pijlmontages momenteel worden gevormd om etiketten te verbergen, een berichtvertoningen, die u ertoe aanzetten om etiketten te tonen.

Een bestaand label op een pijl bijwerken:

1. Klik in een reiscanvasvisualisatie met de rechtermuisknop op de plaats waar u een label wilt toevoegen.

1. Selecteer **[!UICONTROL Update label]** .

1. Geef een naam voor het label op en druk op Enter.

   Als de pijlmontages momenteel worden gevormd om etiketten te verbergen, een berichtvertoningen, die u ertoe aanzetten om etiketten te tonen.

### Een uitsplitsing toepassen

De optie om een indeling toe te passen op uw gegevens is beschikbaar voor de volgende objecten op het canvas:

* Afzonderlijke knooppunten

* Meerdere knooppunten

* De pijl tussen knooppunten

* Meerdere pijlen tussen knooppunten

Houd rekening met het volgende wanneer u een indeling toepast:

* Uitsplitsingen worden toegepast op de primaire metrische waarde. De secundaire metrische waarde wordt niet beïnvloed.

* Het toepassen van een uitsplitsing verandert de reis niet. In plaats daarvan toont het gewoon een uitsplitsing van de gegevens voor het knooppunt waar het wordt toegepast.

* Als een knooppunt al een uitsplitsing heeft, wordt de bestaande uitsplitsing vervangen door een nieuwe uitsplitsing.

* De uitsplitsingsgegevens worden bijgewerkt als wijzigingen op een eerder tijdstip in de reis worden aangebracht.

#### Een uitsplitsing toepassen op een of meer knooppunten of pijlen

1. In een reis canvasvisualisatie, selecteer één of meerdere knopen waar u een verdeling wilt toepassen, dan klik één van de geselecteerde knopen met de rechtermuisknop aan.

   of

   Selecteer in een reiscanvasvisualisatie een of meer pijlen tussen twee knooppunten waarop u de splitsing wilt toepassen en klik vervolgens met de rechtermuisknop op een van de geselecteerde pijlen.

   Houd Command (in Mac) of Ctrl (in Windows) ingedrukt om meerdere knooppunten of pijlen te selecteren.

1. Selecteer [!UICONTROL **Uitsplitsing**].

1. Kies waar u de indeling wilt weergeven:

   * [!UICONTROL **in het canvas van de Reis**]

   * [!UICONTROL **in een vrije lijst van de Vorm**]

1. Selecteer de dimensie die u voor de onderverdeling wilt gebruiken.

   Als u verkoos om de uitsplitsing in het canvas van de Reis te bekijken, worden de hoogste 5 afmetingspunten getoond op de knoop. Een optie is beschikbaar op de knoop om de mislukking in een vrije vormlijst te openen.

   Als u ervoor kiest om de uitsplitsing in een vrije-vormtabel weer te geven, worden de bovenste dimensie-items weergegeven in een nieuwe vrije-vormtabel direct boven de visualisatie van het canvas Reis.

#### Een uitsplitsing toepassen op een afzonderlijk knooppunt

U kunt een afmeting van de linkerspoorstaaf naar de knoop op het canvas slepen waar u de breuk wilt toepassen.

Voor meer informatie, zie [ knopen ](#add-nodes) toevoegen.

#### Een storing verwijderen

Een toegepaste indeling verwijderen:

1. Klik met de rechtermuisknop op het knooppunt waarop de splitsing is toegepast.

1. Selecteer **[!UICONTROL Remove breakdown]** .

### Een publiek maken

De optie om een publiek te maken is beschikbaar voor de volgende objecten op het canvas:

* Afzonderlijke knooppunten

* Meerdere knooppunten

* De pijl tussen knooppunten

* Meerdere pijlen tussen knooppunten

Wanneer u een publiek van veelvoudige knopen of pijlen creeert, worden zij aangesloten bij de exploitant OR.

Een publiek maken:

1. In een reis canvasvisualisatie, selecteer één of meerdere knopen waar u een publiek wilt tot stand brengen, dan klik één van de geselecteerde knopen met de rechtermuisknop aan.

   of

   Selecteer in een reiscanvasvisualisatie een of meer pijlen tussen twee knooppunten waar u een publiek wilt maken en klik vervolgens met de rechtermuisknop op een van de geselecteerde pijlen.

   Houd Command (in Mac) of Ctrl (in Windows) ingedrukt om meerdere knooppunten of pijlen te selecteren.

   >[!NOTE]
   >
   >Het publiek kan geen berekende metriek of om het even welke metriek omvatten die op a [ summiere dataset ](/help/data-views/summary-data.md) gebaseerd zijn. Als u probeert om een publiek van om het even welk gebied van het canvas van de Reis tot stand te brengen dat berekende metrisch of metrisch bevat die op een summiere dataset gebaseerd is, zal berekende metrisch niet in de publieksdefinitie worden omvat.

1. Selecteer [!UICONTROL **tot publiek van knoop**] leiden of [!UICONTROL **tot publiek van pijl**].

1. Ga verder creërend en het publiceren van het publiek zoals die in [ wordt beschreven creëren en publiceer publiek ](/help/components/audiences/publish.md).

### Tendelgegevens weergeven

U kunt de trendgegevens weergeven in een lijngrafiek voor objecten op het canvas Reis. <!--, with some prebuilt anomaly detection data (this is the definition in Fallout) -->

De optie voor trendmatige ontwikkeling is beschikbaar voor de volgende objecten op het canvas:

* Afzonderlijke knooppunten

* Meerdere knooppunten

* De pijlen tussen knooppunten

* Meerdere pijlen tussen knooppunten

De trendgegevens bekijken:

1. In een reis canvasvisualisatie, selecteer één of meerdere knopen waarvoor u trendgegevens wilt bekijken, dan klik één van de geselecteerde knopen met de rechtermuisknop aan.

   of

   In een reis canvasvisualisatie, selecteer één of meerdere pijlen tussen 2 knopen waarvoor u trendgegevens wilt bekijken, dan klik één van de geselecteerde pijlen met de rechtermuisknop aan.

   Houd Command (in Mac) of Ctrl (in Windows) ingedrukt om meerdere knooppunten of pijlen te selecteren.

1. Selecteer [!UICONTROL **Trend**].

### Een segment maken op basis van een knooppunt of pijl

U kunt een nieuw segment tot stand brengen dat op een knoop of een pijl binnen een reis wordt gebaseerd. Nadat het segment is gemaakt, kunt u het overal in Analysis Workspace gebruiken.

De filters die van het canvas van de Reis worden gecreeerd gebruiken [ opeenvolgend segmenteren ](/help/components/filters/seg-sequential-build.md). Dit betekent dat het segment de operator THEN gebruikt om de volgorde van gebeurtenissen (de reis) die mensen doorstroomden aan elkaar te koppelen en naar het geselecteerde knooppunt of de geselecteerde pijl te leiden. Alle gebeurtenissen die overeenkomen met het geselecteerde knooppunt of de geselecteerde pijl worden opgenomen in het segment.

Als u een segment maakt dat is gebaseerd op een knooppunt met meerdere paden die erin vloeien, worden alle paden in het segment opgenomen. Afzonderlijke paden worden verbonden met de operator OR.

Een segment maken:

1. Klik in een reiscanvasvisualisatie met de rechtermuisknop op het knooppunt of de pijl die u wilt gebruiken om het segment te maken.

1. Selecteer [!UICONTROL **creeer segment van knoop**] of [!UICONTROL **creeer segment van pijl**].

   De construcder voor filters wordt weergegeven. In de [!UICONTROL **sectie van de Definitie**], wordt de segmentdefinitie gecreeerd gebaseerd op de knoop of de pijl u en zijn context binnen de reis selecteerde.

1. Geef een titel voor het segment op en breng eventuele andere wijzigingen aan. Voor meer informatie over het creëren van een segment, zie [ de bouwer van de Filter ](/help/components/filters/filter-builder.md).

1. Selecteer [!UICONTROL **sparen**] om het segment te bewaren.

### Knooppunten verwijderen

U kunt een of meer knooppunten tegelijk binnen een reis verwijderen. Wanneer u een knoop schrapt die tussen 2 knopen binnen de reis wordt verbonden, worden de 2 resterende knopen direct verbonden.

Om knopen in het canvas van de Reis te schrappen:

1. In een reis canvasvisualisatie, selecteer één of meerdere knopen die u wilt schrappen, dan klik één van de geselecteerde knopen met de rechtermuisknop aan.

1. Selecteer [!UICONTROL **Schrapping**].

### Pijlen tussen knooppunten verwijderen

U kunt een of meer pijlen tegelijk binnen een rit verwijderen. Wanneer u een pijl tussen twee knooppunten verwijdert, hebben de knooppunten geen verbinding meer. Als de pijl deel uitmaakte van een langer pad, wordt de verbinding met het pad verbroken.

Als u pijlen wilt verwijderen tussen knooppunten in het canvas Reis:

1. Selecteer in een reiscanvasvisualisatie een of meer pijlen tussen twee knooppunten die u wilt verwijderen en klik met de rechtermuisknop op een van de geselecteerde pijlen.

1. Selecteer [!UICONTROL **Schrapping**].

## Een reis openen vanuit Journey Optimizer

Als u een reis weergeeft in Journey Optimizer, kunt u deze weergeven op het canvas Journey.

1. Open in Journey Optimizer de reis die u wilt analyseren in Journey canvas.

1. Selecteer [!UICONTROL **Analyseren in CJA**]. <!-- ?? -->
