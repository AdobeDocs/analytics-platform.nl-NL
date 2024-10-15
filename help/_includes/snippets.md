---
source-git-commit: a6f543d3b6aab06593d9fa40a5d3d6bbf4aa7c32
workflow-type: tm+mt
source-wordcount: '3955'
ht-degree: 0%

---
# Fragmenten

## Beperkte tests voor releasefase {#release-limited-testing}

>[!AVAILABILITY]
>
>De functionaliteit die in dit artikel wordt beschreven, bevindt zich in de Beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het de versieproces van de Customer Journey Analytics, zie {de eigenschapversies van de Customer Journey Analytics 0} ](/help/release-notes/releases.md).[

## Beperkte testsectie voor releasefase {#release-limited-testing-section}

>[!AVAILABILITY]
>
>De in deze sectie beschreven functionaliteit bevindt zich in de beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het de versieproces van de Customer Journey Analytics, zie {de eigenschapversies van de Customer Journey Analytics 0} ](/help/release-notes/releases.md).[

## Pakket selecteren {#select-package}

>[!NOTE]
>
>U moet het **Uitgezochte** pakket of hoger hebben om de functionaliteit te gebruiken die in deze sectie wordt beschreven. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.

## Primair pakket {#prime-package}

>[!NOTE]
>
>U moet het **Primaire** pakket of hoger hebben om de functionaliteit te gebruiken die in deze sectie wordt beschreven. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.

## Ultieme verpakking {#ultimate-package}

>[!NOTE]
>
>U moet het **Ultieme** pakket hebben om de functionaliteit te gebruiken die in deze sectie wordt beschreven. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.


## Criteria van het filter Gegevenswoordenboek {#dd-filter-criteria}

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

## Componenten gegevenswoordenboek {#dd-component-information}

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

## Sorteeropties voor componenten {#components-sort-options}

| Optie | Functie |
|---------|----------|
| **[!UICONTROL Recommended]** | Sorteer componenten voor elk type (afmeting, metrisch, filter en datumbereik) op basis van hun aanbeveling. Componenten die het vaakst en het laatst door u of anderen in uw organisatie worden gebruikt, worden hoger weergegeven in elke lijst. |
| **[!UICONTROL Last modified]** | Sorteer componenten voor elk type (afmeting, metrisch, filter en datumbereik) op basis van de datum die als laatste is gewijzigd. De componenten die onlangs worden gewijzigd worden getoond hoger in elke lijst. |
| **[!UICONTROL Alphabetical]** | Sorteer componenten voor elk type (afmeting, metrisch, filter en datumbereik) in oplopende alfabetische volgorde. |
| **[!UICONTROL Categorical]** | Sorteer componenten voor elk type (afmeting, metrisch, filter en datumbereik) op basis van hun categorie. Bijvoorbeeld gekromde versus niet-gekromde componenten van de gegevensmening. |

{style="table-layout:auto"}

## Tijdvergelijking {#apply-time-comparison}

U kunt de huidige tijdsperiode vergelijken met een vorige tijdsperiode. Als u een optie in dit menu selecteert, ontvangt elk gegevenspunt een met punten gelijkende kleur. Deze tegenhanger vertegenwoordigt die zelfde metrisch in de geselecteerde vorige datumwaaier. Als u deze optie instelt, verdubbelt u het aantal items in het diagram en de rijen in de tabel.

De beschikbare opties voor tijdvergelijking omvatten de vorige periode, 13 weken vóór, 52 weken vóór en een aangepast datumbereik. Als u Aangepast datumbereik selecteert, worden aanvullende opties weergegeven waarmee u het getal en de granulariteit kunt selecteren. Als u Geen selecteert, wordt de datumvergelijking verwijderd.


## Adobe Analytics voor videodemonstratie {#videoaa}

Deze video demonstreert de functionaliteit met Adobe Analytics. De functionaliteit is echter ook beschikbaar in de Customer Journey Analytics. Houd rekening met de volgende terminologische verschillen.

| Adobe Analytics | Customer Journey Analytics |
|:---:|:---:|
| Segmenten | Filters |
| Bezoeker | Persoon |
| Bezoek | Sessie |
| Actief | Gebeurtenis |


## Deelvenster Filters {#filterspanel}

1. Selecteer ![ Filter ](/help/assets/icons/Filter.svg) om het paneel van Filters te openen. Als u meer ruimte voor de lijst van Filters nodig hebt, kunt u ![ Filter ](/help/assets/icons/Filter.svg) selecteren opnieuw om het paneel te sluiten.
1. Selecteer filters uit een van de beschikbare filtersecties.


## Sectie voor tagfilter {#tagfiltersection}

| Tags | Beschrijving |
|---|---|
| ![ Markeringen ](/help/assets/filter-tag.png){width="300"} | In de sectie **[!UICONTROL Tags]** kunt u filteren op tags. <ul><li>U kunt ](/help/assets/icons/Search.svg) *Codes van het Onderzoek* ![ zoeken {om naar markeringen te zoeken u kunt gebruiken om te filtreren.</li><li>U kunt meerdere tags selecteren. Welke labels beschikbaar zijn, is afhankelijk van de selecties die in andere secties in het filterdeelvenster zijn gemaakt.</li><li>De getallen geven aan:<ul><li>**(1)**: Het aantal geselecteerde markeringen (als één of meerdere markeringen worden geselecteerd).</li><li>**2︎⃣**: Het aantal markeringen beschikbaar voor de punten die uit de huidige filter voortvloeien.</li><li>7︎⃣: Het aantal items dat aan de specifieke tag is gekoppeld.</li></ul></li></ul> |


## Sectie Gegevensweergavefilter {#dataviewfiltersection}

| Gegevens, weergave | Beschrijving |
|---|---|
| ![ de meningen van Gegevens ](/help/assets/filter-dataview.png){width="300"} | In de sectie **[!UICONTROL Data view]** kunt u filteren op gegevensweergaven. <ul><li>U kunt ](/help/assets/icons/Search.svg) *de meningen van Gegevens van het 1} Onderzoek* {zoeken aan onderzoek naar gegevensmeningen u kunt gebruiken om te filtreren.![</li><li>U kunt meerdere gegevensweergaven selecteren. Welke gegevensweergaven beschikbaar zijn, is afhankelijk van de selecties die in andere secties van het filterdeelvenster zijn gemaakt.</li><li>De getallen geven aan:<ul><li>**(2)**: Het aantal geselecteerde gegevensmeningen (als één of meerdere gegevensmeningen worden geselecteerd).</li><li>**3︎⃣**: Het aantal gegevensmeningen beschikbaar voor de punten die uit de huidige filter voortvloeien.</li><li>4︎⃣: Het aantal items dat is gekoppeld aan de specifieke gegevensweergave.</li></ul></li></ul> |

## Ingeschakelde sectie voor statusfilter {#enabledstatusfiltersection}

| Status Ingeschakeld | Beschrijving |
|---|---|
| ![ Toegelaten status ](/help/assets/filter-enabledstatus.png){width="300"} | In de sectie **[!UICONTROL Enabled status]** kunt u filteren op ingeschakelde status. <ul><li>U kunt meerdere statussen selecteren.</li><li>De getallen geven aan:<ul><li>**(2)**: Het aantal geselecteerde statussen (als één of meerdere statussen worden geselecteerd).</li><li>**2︎⃣**: Het aantal statussen beschikbaar voor de punten die uit de huidige filter voortvloeien.</li><li>1︎⃣: Het aantal items dat aan de specifieke status is gekoppeld.</li></ul></li></ul> |

## Sectie Type filter {#typefiltersection}

| Type | Beschrijving |
|---|---|
| ![ Type ](/help/assets/filter-type.png){width="300"} | In de sectie **[!UICONTROL Type]** kunt u filteren op tekst. <ul><li>U kunt meerdere typen selecteren.</li><li>De getallen geven aan:<ul><li>**(2)**: Het aantal geselecteerde types (als één of meerdere types worden geselecteerd).</li><li>**1︎⃣**: Het aantal types beschikbaar voor de punten die uit de huidige filter voortvloeien.</li><li>3︎⃣: Het aantal items dat aan het specifieke type is gekoppeld.</li></ul></li></ul> |

## Sectie voor het filter Eigenaar {#ownerfiltersection}

| Eigenaar | Beschrijving |
|---|---|
| ![ Eigenaars ](/help/assets/filter-owners.png){width="300"} | In de sectie **[!UICONTROL Owner]** kunt u filteren op eigenaars. <ul><li>U kunt ](/help/assets/icons/Search.svg) *Onderzoek Eigenaars* ![ zoeken {om naar eigenaars te zoeken u aan filter kunt gebruiken.</li><li>U kunt meerdere eigenaars selecteren. Welke eigenaars beschikbaar zijn, is afhankelijk van de selecties die in andere secties in het filterdeelvenster zijn gemaakt.</li><li>De getallen geven aan:<ul><li>**(2)**: Het aantal geselecteerde eigenaars (als één of meerdere eigenaars worden geselecteerd).</li><li>**3︎⃣**: Het aantal eigenaars beschikbaar voor de punten die uit de huidige filter voortvloeien.</li><li>4︎⃣: Het aantal items dat aan de specifieke eigenaar is gekoppeld.</li></ul></li></ul> |

## Sectie Overige filters {#otherfiltersfiltersection}

| Overige filters | Beschrijving |
|---|---|
| ![ Andere filters ](/help/assets/filter-other.png){width="300"} | Met de sectie **[!UICONTROL Other filters]** kunt u filteren op een ander vooraf gedefinieerd filter.<ul><li>U kunt een of meer van de volgende opties selecteren:<ul><li> **[!UICONTROL Show all]**</li><li>**[!UICONTROL Shared with me]**</li><li>**[!UICONTROL Mine]**</li><li>**[!UICONTROL Approved]**</li><li>**[!UICONTROL Favorites]**</li></ul> Wat u kunt selecteren hangt van uw rol en toestemmingen af.</li><li>U kunt meerdere filters selecteren. Welke andere filters beschikbaar zijn, is afhankelijk van de selecties die in andere secties van het filterdeelvenster zijn gemaakt.</li><li>De getallen geven aan:<ul><li>**(1)**: Het aantal geselecteerde andere filters (als één of meerdere andere filters worden geselecteerd).</li><li>**5︎⃣**: Het aantal andere filters beschikbaar voor de punten die uit de huidige filter voortvloeien.</li><li>4︎⃣: Het aantal items dat aan het specifieke andere filter is gekoppeld.</li></ul></li></ul> |

## Filtersectie Datumbereik  {#daterangefiltersection}

| Toegepast datumbereik | Beschrijving |
|---|---|
| ![ waaier van de Datum ](/help/assets/filter-daterange.png){width="300"} | In de sectie Toegepast datumbereik kunt u filteren op een datumbereik dat van toepassing is op de items.<ol><li>Selecteer een datumbereik.</li><li>Definieer een datumbereik in de kalenderpop-up of selecteer een van de beschikbare voorinstellingen.<br> Alternatief, kunt u een datumwaaier in de de waaiersectie van de Datum van het paneel van de Filter direct ook specificeren.</li></ol><ul><li>De getallen geven aan:<ul><li>**(1)**: Het aantal gewijzigde datumbereiken dat van standaardvoorinstellingen wordt gewijzigd.</li><li>**5︎⃣**: Het aantal datumwaaiers beschikbaar voor de punten die uit de huidige filter voortvloeien.</li></ul> |


## Attributiemodellen {#attribution-models-details}

Een attributiemodel bepaalt welke afmetingspunten krediet voor metrisch krijgen wanneer de veelvoudige waarden binnen het terugkijkvenster van metrisch worden gezien. Attributiemodellen zijn alleen van toepassing wanneer er meerdere dimensieitems zijn ingesteld in het terugzoekvenster. Als slechts één dimensie-item is ingesteld, krijgt dat dimensie-item 100% krediet, ongeacht het gebruikte attributiemodel.

| Pictogram | Attributiemodel | Definitie |
| :---: | :--- | --- |
| ![ Laatste aanraking ](/help/assets/icons/AttributeLastTouch.svg) | Laatste aanraking | Geeft 100% krediet aan het aanraakpunt dat het laatst voor de conversie optrad. Dit attributiemodel is doorgaans de standaardwaarde voor elke meting waarbij een attributiemodel niet op andere wijze is opgegeven. Organisaties gebruiken dit model doorgaans wanneer de conversietijd relatief kort is, zoals bij het analyseren van interne zoektrefwoorden. |
| ![ eerste aanraking ](/help/assets/icons/AttributeFirstTouch.svg) | Eerste aanraking | Geeft 100% krediet aan het aanraakpunt dat het eerst wordt weergegeven in het terugkijkvenster van de attributie. Organisaties gebruiken dit model doorgaans om inzicht te krijgen in merkbekendheid of aanschaf door klanten. |
| ![ Lineair ](/help/assets/icons/AttributeLinear.svg) | Lineair | Biedt hetzelfde krediet aan elk aanraakpunt dat wordt weergegeven voor een conversie. Dit is handig wanneer conversiecycli langer zijn of een frequentere betrokkenheid van klanten vereisen. Organisaties gebruiken dit toewijzingsmodel doorgaans om de doeltreffendheid van meldingen voor mobiele apps of voor producten op abonnementsbasis te meten. |
| ![Deelname](/help/assets/icons/AttributeParticipation.svg) | Deelname | Biedt 100% krediet aan alle unieke aanraakpunten. Aangezien elk aanraakpunt 100% krediet ontvangt, komt het metrische gegeven meestal uit op meer dan 100%. Als een dimensie-item meerdere afzonderlijke keren vóór een conversie wordt weergegeven, worden de waarden gededupliceerd naar 100%. Dit attributiemodel is ideaal in situaties waarin u wilt begrijpen welke aanraakpunten klanten het meest worden blootgesteld. Mediaorganisaties gebruiken dit model doorgaans om de snelheid van de inhoud te berekenen. De detailhandelorganisaties gebruiken typisch dit model om te begrijpen welke delen van hun plaats aan omzetting kritiek zijn. |
| ![ Zelfde aanraking ](/help/assets/icons/AttributeSameTouch.svg) | Zelfde aanraking | Verleent 100% krediet aan de zelfde gebeurtenis waar de omzetting plaatsvond. Als er geen aanraakpunt plaatsvindt op dezelfde gebeurtenis als bij een conversie, wordt dit punt ingesloten onder &quot;Geen&quot;. Dit attributiemodel wordt soms gelijkgesteld met het hebben van helemaal geen attributiemodel. Het is waardevol in scenario&#39;s waar u geen waarden van andere gebeurtenissen wilt die beïnvloeden hoe metrisch krediet aan afmetingspunten geeft. Product- of ontwerpteams kunnen dit model gebruiken om de doeltreffendheid van een pagina te beoordelen waar conversie plaatsvindt. |
| ![ Vormde U ](/help/assets/icons/AttributeUShaped.svg) | U-vorm | Biedt 40% krediet aan de eerste interactie, 40% aan de laatste interactie, en verdeelt de resterende 20% aan om het even welke aanraakpunten tussenin. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt aan beide een krediet van 50% toegekend. Dit attributiemodel wordt het best gebruikt in scenario&#39;s waar u eerste en laatste interactie het meest waart, maar wil geen extra interacties binnen volledig sluiten. |
| ![ Curve van J ](/help/assets/icons/AttributeJCurve.svg) | J Curve | Geeft 60% krediet aan de laatste interactie, 20% krediet aan de eerste interactie, en verdeelt de resterende 20% aan om het even welke aanraakpunten tussenin. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt 75% aan de laatste interactie besteed en wordt 25% aan de eerste. Net als bij U-Shaped, geeft dit attributiemodel de voorkeur aan de eerste en laatste interacties, maar is het zwaarder van belang voor de laatste interactie. |
| ![ Omgekeerde J ](/help/assets/icons/AttributeInverseJ.svg) | Omgekeerd J | Biedt 60% krediet aan het eerste aanraakpunt, 20% aan het laatste aanraakpunt en verdeelt de resterende 20% aan de tussenliggende aanraakpunten. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt 75% aan de eerste interactie toegekend en wordt 25% aan de laatste toegekend. Net als voor J-Shaped, geeft dit attributiemodel de voorkeur aan de eerste en laatste interacties, maar eerder de eerste interactie. |
| ![ Verval van de Tijd ](/help/assets/icons/AttributeTimeDecay.svg) | Tijdverlies | Volgt een exponentieel verval met een aangepaste parameter voor de halfwaardetijd, waarbij de standaardwaarde 7 dagen is. Het gewicht van elk kanaal is afhankelijk van de hoeveelheid tijd die is verstreken tussen het starten van het aanraakpunt en de uiteindelijke conversie. De formule die wordt gebruikt om krediet te bepalen is `2^(-t/halflife)`, waarbij `t` de hoeveelheid tijd tussen een aanraakpunt en een conversie is. Alle aanraakpunten worden vervolgens genormaliseerd tot 100%. Ideaal voor scenario&#39;s waarin u de toewijzing wilt meten aan de hand van een specifieke en significante gebeurtenis. Hoe langer een conversie plaatsvindt na deze gebeurtenis, hoe minder krediet wordt gegeven. |
| ![Aangepast](/help/assets/icons/AttributeCustom.svg) | Aangepast | Hiermee kunt u de gewichten opgeven die u wilt geven aan het eerste aanraakpunt, het laatste aanraakpunt en de tussenliggende aanraakpunten. De opgegeven waarden worden genormaliseerd naar 100%, zelfs als de ingevoerde aangepaste getallen niet bij 100 komen te liggen. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor interactie met twee aanraakpunten wordt de middelste parameter genegeerd. De eerste en laatste aanraakpunten worden vervolgens genormaliseerd tot 100% en de kredieten worden dienovereenkomstig toegewezen. Dit model is ideaal voor analisten die volledige controle willen hebben over hun attributiemodel en specifieke behoeften hebben waaraan andere attributiemodellen niet voldoen. |
| ![ Algorithmic ](/help/assets/icons/AttributeAlgorithmic.svg) | Algorithmic | Gebruikt statistische technieken om dynamisch de optimale allocatie van krediet voor de geselecteerde maatstaf vast te stellen. Het algoritme dat wordt gebruikt voor attributie is gebaseerd op de Harsanyi Dividend van coöperatieve speltheorie. Het dividend van Harsanyi is een generalisering van de Shapley-waardeoplossing (genoemd naar Lloyd Shapley, een Nobelprijswinnaar) voor het verdelen van krediet onder spelers in een spel met ongelijke bijdragen aan de uitkomst.<br> op een hoog niveau, wordt de attributie berekend als coalitie van spelers waaraan een overschot billijk moet worden verdeeld. De overtollige verdeling van elke coalitie wordt bepaald volgens het overschot dat eerder door elke subcoalitie (of eerder deelnemende dimensie-items) recursief werd gecreeerd. Voor meer details, zie John Harsanyi en de originele documenten van Lloyd Shapley:<br> Shapley, Lloyd S. (1953). Een waarde voor spelletjes van één persoon. *bijdragen aan de Theorie van Spelen, 2 (28)*, 307-317.<br> Harsanyi, John C. (1963). Een vereenvoudigd onderhandelingsmodel voor het on-person coöperatieve spel. *Internationale Economische Controle 4 (2)*, 194-220. |

{style="table-layout:auto"}

## Atributie terugzoekvenster {#attribution-lookback-window}

Een terugzoekvenster is de hoeveelheid tijd die een conversie moet terugkijken om aanraakpunten op te nemen. Als een dimensie-item buiten het terugzoekvenster wordt ingesteld, wordt de waarde niet opgenomen in attributieberekeningen.

* **14 Dagen**: Zoekt file tot 14 dagen vanaf toen de omzetting gebeurde.
* **30 Dagen**: Zoekt file tot 30 dagen vanaf toen de omzetting gebeurde.
* **60 Dagen**: Zoekt file tot 60 dagen vanaf toen de omzetting gebeurde.
* **90 Dagen**: Zoekt file tot 90 dagen vanaf toen de omzetting gebeurde.
* **Zitting**: Zoekt file aan het begin van de zitting waar een omzetting gebeurde. De raadplegingsvensters van de zitting respecteren de gewijzigde [ onderbreking van de Zitting ](/help/data-views/create-dataview.md#session-settings) in een gegevensmening.
* **Persoon (Meldend Venster)**: Zoekt bij alle bezoeken file tot de eerste van de maand van de huidige datumwaaier. Als het bereik van de rapportdatum bijvoorbeeld 15 september tot en met 30 september is, omvat het bereik van de persoonlijke terugzoekdatum 1 september tot en met 30 september. Als u dit terugkijkvenster gebruikt, kunt u soms zien dat de afmetingspunten aan data buiten uw rapporterend venster worden toegeschreven.
* **Tijd van de Douane:** staat u toe om een venster van de douaneterugblik van te plaatsen wanneer een omzetting gebeurde. U kunt het aantal minuten, uren, dagen, weken, maanden of kwartalen opgeven. Bijvoorbeeld, als een omzetting op 20 februari gebeurde, zou een terugkijkvenster van vijf dagen alle afmetingstips van 15 februari tot 20 februari in het attributiemodel evalueren.

## Voorbeeld van kenmerk {#attribution-example}

Bekijk het volgende voorbeeld:

1. Op 15 september arriveert een persoon via een betaalde zoekadvertentie naar uw site en verlaat hij vervolgens.
1. Op 18 september arriveert de persoon opnieuw naar uw site via een link naar sociale media die hij van een vriend heeft gekregen. Ze voegen verschillende artikelen aan hun winkelwagentje toe, maar kopen niets.
1. Op 24 september stuurt uw marketingteam hen een e-mail met een coupon voor sommige objecten in hun winkelwagentje. Ze passen de coupon toe, maar gaan naar verschillende andere sites om te zien of er andere coupons beschikbaar zijn. Ze vinden een andere advertentie via een advertentie en kopen uiteindelijk $50.

Afhankelijk van het terugkijkvenster en het attributiemodel, ontvangen de kanalen verschillende kredieten. Hieronder volgen enkele voorbeelden:

* Gebruikend **eerste aanraking** en venster van de a **zittingsterugblik**, kijkt de attributie slechts het derde bezoek. Tussen e-mail en display was e-mail de eerste, dus e-mail krijgt 100% krediet voor de aankoop van $50.

* Gebruikend **eerste aanraking** en venster van de a **persoonraadpleging**, kijkt de attributie naar alle drie bezoeken. De betaalde zoekopdracht was de eerste, dus krijgt deze 100% krediet voor de aankoop van $50.

* Gebruikend **lineair** en venster van de a **zittingsterugblik**, is het krediet verdeeld tussen e-mail en vertoning. Beide kanalen krijgen elk $25 krediet.
Gebruikend **lineair** en het venster van de a **persoonraadpleging**, wordt het krediet verdeeld tussen betaald onderzoek, sociaal, e-mail, en vertoning. Elk kanaal krijgt $12,50 krediet voor deze aankoop.

* Gebruikend **j-Gegeld** en a **persoon terugkijkvenster**, wordt het krediet verdeeld tussen betaald onderzoek, sociaal, e-mail, en vertoning.

   * 60% krediet wordt gegeven aan vertoning, voor $30.
   * 20% krediet wordt gegeven voor betaalde zoekopdrachten, voor $10.
   * De resterende 20% is verdeeld tussen sociale media en e-mail, wat elk $5 geeft.

* Gebruikend **Verval van de Tijd** en venster van de a **persoonraadpleging**, wordt het krediet verdeeld tussen betaald onderzoek, sociaal, e-mail, en vertoning. De standaardhalfwaardetijd van 7 dagen gebruiken:

   * Tussenruimte van nul dagen tussen aanraakpunt weergeven en conversie. `2^(-0/7) = 1`
   * Ruimte van nul dagen tussen aanraakpunt en conversie via e-mail. `2^(-0/7) = 1`
   * Tussenruimte van zes dagen tussen sociale aanraakpunten en conversie. `2^(-6/7) = 0.552`
   * Tussenruimte van negen dagen tussen betaald aanraakpunt en conversie. `2^(-9/7) = 0.41`
   * Het normaliseren van deze waarden resulteert in het volgende:

      * Weergave: 33,8%, krijgt $16,88
      * E-mail: 33,8% ontvangt $ 16,88
      * Sociaal: 18,6%, $ 9,32
      * Betaalde zoekopdracht: 13,8%, krijgt $6,92

Conversiegebeurtenissen die doorgaans hele getallen bevatten, worden gedeeld als het krediet tot meer dan één kanaal behoort. Als twee kanalen bijvoorbeeld een bijdrage leveren aan een bestelling met behulp van een lineair toewijzingsmodel, krijgen beide kanalen 0,5 van die volgorde. Deze gedeeltelijke metriek worden samengevat over alle mensen dan rond gemaakt aan het dichtstbijzijnde geheel voor rapportering.

## Reisvisualisatievergelijkingen {#journey-visualization-comparisons}

Diverse visualisaties in de analyse van de Reis van de Klant worden ontworpen om de reizen te analyseren u aan uw klanten verstrekt.

Gebruik de volgende informatie om de visualisatie te kiezen die het beste aan uw behoeften voldoet.

| Functie | Reiscanvas | Fallout | Stroom |
|---------|----------|---------|---------|
| **Vooraf bepaalde opeenvolging van pagina&#39;s** | Ja </br> Combineert vooraf bepaalde en verkennende analyse. Het uiteindelijke pad wordt gebruikt wanneer vooraf gedefinieerde knooppunten op het pad worden gebruikt (bezoekers worden meegeteld zolang ze uiteindelijk van het ene vooraf gedefinieerde knooppunt naar het andere gaan). De directe (niet uiteindelijke) volgende knopen kunnen ook worden getoond. | Ja </br> de weg kan een uiteindelijke weg zijn of kan aan volgende aanraakpunt worden beperkt | Nee |
| **Verkennende opeenvolging van pagina&#39;s (ad hoc analyse)** | Ja </br> Combineert vooraf bepaalde en verkennende analyse. Het uiteindelijke pad wordt gebruikt wanneer vooraf gedefinieerde knooppunten op het pad worden gebruikt (bezoekers worden meegeteld zolang ze uiteindelijk van het ene vooraf gedefinieerde knooppunt naar het andere gaan). De directe (niet uiteindelijke) volgende knopen kunnen ook worden getoond. | Beperkt </br> staat u toe om directe reserve in een lijst van de Vrije vorm met de rechtermuisknop aan te klikken en te bekijken. | Ja </br> Verkennende slechts analyse. Altijd binnen één afmetingsinstantie tussen knooppunten. Dit betekent dat elk knooppunt het directe (niet uiteindelijke) volgende aanraakpunt langs het pad weergeeft. |
| **toont waar de mensen weggingen (uit vielen) en door (door vielen) werden voortgezet** | Ja </br> toont voor zowel vooraf bepaalde als verkennende reizen | Ja </br> toont vooraf bepaalde reizen | Ja </br> toont voor verkennende reizen |
| **Lineaire reizen** | Ja | Ja | Nee |
| **niet-lineaire reizen met veelvoudige ingangspunten en wegen** | Ja | Nee | Ja |
| **Primaire metrisch** | Elke metrische waarde, inclusief berekende metriek | Alleen sessie of persoon | Alleen voorkomen (padweergaven) |
| **Secundaire metrische** | Ja<p>Elke metrische waarde, inclusief berekende metriek</p> | Nee | Nee |
| **de steun van de Component in knopen of touchpoints** | Metriek, afmetingsitems, filters en datumbereiken. | Metriek, afmetingsitems, filters en datumbereiken. | Alleen afmetingsitems (behalve het begin- en eindpunt) |
| **vergelijk filters** | Nee | Ja<p>Voer zij aan zij vergelijkingen van twee verschillende filters in het zelfde rapport uit.</p> | Nee |
| **belemmering-en-dalingscomponenteninteractie** | Ja | Ja | Nee |
| **reizen van Adobe Journey Optimizer** | Ja </br> Open reizen van Journey Optimizer voor diepere analyse en aanpassing | Nee | Nee |

{style="table-layout:auto"}
