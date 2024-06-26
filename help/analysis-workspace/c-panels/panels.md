---
description: Een deelvenster is een verzameling tabellen en visualisaties
title: Overzicht van deelvensters
feature: Panels
exl-id: be3e34a0-06c1-4200-b965-96084c2912fd
role: User
source-git-commit: 665dcd8edcfae6bbf3239c0812ce70843f2ce07c
workflow-type: tm+mt
source-wordcount: '1392'
ht-degree: 0%

---

# Overzicht van deelvensters

A [!UICONTROL panel] is een verzameling tabellen en visualisaties. U hebt toegang tot deelvensters via het pictogram linksboven in Workspace of via een [leeg deelvenster](/help/analysis-workspace/c-panels/blank-panel.md). Deelvensters zijn handig wanneer u uw projecten wilt ordenen op basis van tijdsperioden, gegevensweergaven of het geval waarin de analyse wordt gebruikt.

## Deelvenstertypen

De volgende deelvenstertypen zijn beschikbaar in Analysis Workspace voor [!UICONTROL Customer Journey Analytics]:

| Vensternaam | Beschrijving |
| --- | --- |
| [Leeg deelvenster](/help/analysis-workspace/c-panels/blank-panel.md) | Kies uit de beschikbare deelvensters en visualisaties om uw analyse te starten. |
| [Deelvenster Snelle inzichten](quickinsight.md) | Snel een vrije-vormlijst en een bijbehorende visualisatie bouwen om inzichten sneller te analyseren en te ontdekken. |
| [Kenmerk, deelvenster](attribution.md) | Vergelijk en visualiseer snel om het even welk aantal attributiemodellen gebruikend om het even welke afmeting en omzettingsmetrisch. |
| [Deelvenster Vrije vorm](freeform-panel.md) | Voer onbeperkte vergelijkingen en onderverdelingen uit, dan voeg visualisaties toe om een rijk gegevensverhaal te vertellen. |
| [Deelvenster voor gelijktijdige mediaviewers](media-concurrent-viewers.md) | Analyseer gelijktijdige viewers in de loop van de tijd met details over de piekconsistentie en de mogelijkheid om af te breken en te vergelijken. |
| [Deelvenster Tijdlijn media afspelen](/help/analysis-workspace/c-panels/media-playback-time-spent.md) | Analyseer de afspeeltijd die u hebt doorgebracht om te begrijpen waar de piekgelijktijdige uitvoering heeft plaatsgevonden of waar een drop-down heeft plaatsgevonden. |

![Het deelvenster Customer Journey Analytics met de beschikbare deelvenstertypen.](assets/panel-overview.png)

[!UICONTROL Quick Insights], [!UICONTROL Blank] en [!UICONTROL Freeform] deelvensters zijn ideale plaatsen om uw analyse te starten, terwijl [!UICONTROL Attribution IQ] leent zich voor geavanceerdere analyses. A `"+"` Deze knop is beschikbaar in projecten, zodat u op elk gewenst moment lege deelvensters kunt toevoegen.

Het standaardbeginvenster is het [!UICONTROL Freeform] , maar u kunt het [leeg deelvenster](/help/analysis-workspace/c-panels/blank-panel.md) ook uw standaardinstelling.

## Kalender {#calendar}

De paneelkalender bepaalt het rapporteringswaaier voor lijsten en visualisaties binnen een paneel.

Opmerking: als een (paarse) datumbereikcomponent wordt gebruikt in een tabel, visualisatie of dropzone van een deelvenster, wordt de deelvensterkalender hierdoor overschreven.

![Het kalendervenster dat het geselecteerde datumbereik weergeeft.](assets/panel-calendar.png)

U kunt een datumbereik op minaniveau toepassen onder de geavanceerde instellingen van uw deelvensterkalender. Als u op een datumwaaier rapporteert die vele dagen overspant, is de begintijd van toepassing op de eerste dag en de eindtijd op de laatste dag in uw waaier.

## Dropzone {#dropzone}

Met de dropzone van het deelvenster kunt u filters en vervolgkeuzefilters toepassen op alle tabellen en visualisaties in een deelvenster. U kunt een of meerdere filters toepassen op een deelvenster.

### Filters

Sleep de filters van de linkerspoorstaaf naar de neerzetzone van het deelvenster om het deelvenster te filteren. Herhaal dit proces om extra filters aan het paneel toe te voegen. Filters worden naast elkaar boven in het deelvenster weergegeven.

![De linkerspoorstaaf toont beschikbare Metriek en de Mobiele metrische Klant sleepte aan de paneeldalingsstreek.](assets/segment-filter.png)

### Ad-hocfilters

Niet-filtercomponenten kunnen ook rechtstreeks naar de dropzone worden gesleept om ad-hocfilters te maken, waardoor u tijd en moeite bespaart om naar de Filter Builder te gaan. Filters die op deze manier worden gemaakt, worden automatisch gedefinieerd als filters op gebeurtenisniveau. Deze definitie kan worden gewijzigd door te klikken op het informatiepictogram (i) naast het filter, vervolgens op het pictogram voor het bewerken van de vorm van een potlood en dit te bewerken in de Filter Builder.

Ad hoc filters zijn een type snel filter, en zijn plaatselijk aan het project. Ze komen niet in de linkerspoorstaaf voor als je ze niet openbaar maakt.

Zie voor meer informatie [Snelle filters](/help/components/filters/quick-filters.md).

![Ad hoc filters die openbaar worden gemaakt en in de dalingsstreek worden gelaten vallen.](assets/adhoc-segment-filter.png)

### Statische vervolgkeuzefilters

Met statische vervolgkeuzefilters kunt u op een gecontroleerde manier met de gegevens werken. U kunt bijvoorbeeld een vervolgkeuzefilter toevoegen voor mobiele apparaattypen, zodat u het deelvenster kunt filteren op Tablet, Mobiele telefoon of Computer.

De statische drop-down filters kunnen ook worden gebruikt om vele projecten in te consolideren. Als er bijvoorbeeld veel versies van hetzelfde project met verschillende landfilters zijn toegepast, kunt u alle versies samenvoegen tot één project en een vervolgkeuzelijst Land toevoegen.

![Statische vervolgkeuzefilters die het gemarkeerde filter &quot;Direct&quot; van het Kanaal van de Markt tonen. ](assets/dropdown-filter-intro.png)

#### Statische vervolgkeuzefilters maken

* Voor vervolgkeuzefilters die afmetingselementen gebruiken, selecteert u één afmeting in de linkerrails en zet u deze neer in de dropzone van het deelvenster **terwijl u`[Shift]`**. Dit leidt tot een drop-down filter met alle afmetingspunten die met die afmeting worden geassocieerd.

  Of als u wilt dat het vervolgkeuzefilter alleen bepaalde dimensies bevat die aan een dimensie zijn gekoppeld, klikt u op het pijlpictogram naar rechts naast de gewenste dimensie in de linkertrack. Deze actie stelt alle beschikbare afmetingspunten bloot. Meerdere dimensie-items in deze lijst selecteren met `[Shift + Click]` of `[Ctrl + Click]`en zet ze vervolgens neer in de dropzone van het deelvenster **terwijl u** `[Shift]`.

* Bij vervolgkeuzefilters met één componenttype (bijvoorbeeld alleen dimensies, of alleen filters of alleen metriek) selecteert u meerdere items van hetzelfde type in de linkerrail met `[Shift + Click]` of `[Ctrl + Click]`en zet ze vervolgens neer in de dropzone van het deelvenster **terwijl u`[Shift]`**.

  Er wordt één vervolgkeuzemenu gemaakt met de componenten die u hebt geselecteerd.

* Voor vervolgkeuzefilters met een combinatie van componenttypen (zoals 2 metriek en 3 filters) selecteert u meerdere componenten met `[Shift + Click]` of `[Ctrl + Click]`. De selectie neerzetten in de dropzone van het deelvenster **terwijl u`[Shift]`**. In dit verband worden alle componenttypen behandeld als afzonderlijke vervolgkeuzefilters. Als u bijvoorbeeld zowel metriek- als dimensie-items in uw selectie opneemt, worden twee aparte vervolgkeuzefilters gemaakt: een vervolgkeuzelijst bevat dimensie-items en het andere filter bevat metriek.

  ![Het venster van het Comité met het Mobiele de segmentgebied van de Klant beschikbaar om een statische drop-down filter te laten vallen. ](assets/create-dropdown.png)

Als u met de rechtermuisknop op een vervolgkeuzefilter klikt, kunt u uit de volgende opties kiezen:

* **[!UICONTROL Delete drop-down]**: Hiermee verwijdert u het vervolgkeuzefilter uit het deelvenster.
* **[!UICONTROL Delete label]**: Verwijder de tekst boven een vervolgkeuzefilter. Als u het label wilt wijzigen, selecteert u het potloodpictogram.
* **[!UICONTROL Add label]**: Wanneer u een vervolgkeuzefilter toevoegt aan een project, wordt automatisch een label ingesteld op de naam van de component. Als u het label verwijdert, kunt u het opnieuw toevoegen met deze optie.
* **[!UICONTROL Require selection]**: Er moet een filter op het deelvenster worden ingesteld.

[De video bekijken](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/using-panels-to-organize-your-analysis-workspace-projects.html) voor meer informatie over het toevoegen van vervolgkeuzefilters aan uw project.

#### Statische vervolgkeuzefilters gebruiken

Gebruikers kunnen het menu met vervolgkeuzelijsten op de volgende manieren gebruiken om het deelvenster te filteren:

* Pas één filter op het paneel toe door het filter van de drop-down filter te selecteren.

* Pas meerdere filters toe op het deelvenster door meer dan één filter te selecteren in de vervolgkeuzelijst. Het deelvenster wordt gefilterd met geselecteerde filters.

  ![Meerdere filters selecteren](assets/dropdown-filter-multiselect.png)

### Dynamische vervolgkeuzefilters

Met dynamische vervolgkeuzefilters kunt u beschikbare waarden bepalen op basis van gegevens binnen het rapportagebereik van het deelvenster en waarden in andere vervolgkeuzefilters. U kunt bijvoorbeeld twee dynamische vervolgkeuzelijsten maken met de dimensie Landen en Steden. Wanneer u een land selecteert in de vervolgkeuzelijst UICONTROL-landen, wordt de vervolgkeuzelijst Steden dynamisch aangepast zodat alleen de steden in dat land worden weergegeven.

Dit concept is van toepassing op alle dimensies. Alleen dimensie-items die binnen het datumbereik van het deelvenster verschijnen en geselecteerde filters zijn zichtbaar. Items die in statische vervolgkeuzefilters zijn geselecteerd, beïnvloeden de beschikbare waarden in dynamische vervolgkeuzefilters. Het omgekeerde is echter niet waar. Dimension-items die zijn geselecteerd in dynamische vervolgkeuzefilters hebben geen invloed op de beschikbare waarden in statische vervolgkeuzefilters.

Handmatige selectie van dimensie-items is beschikbaar als u verwacht dat een bepaald dimensie-item in de toekomst wordt verzameld. U kunt ook een dynamisch vervolgkeuzefilter wissen, zodat het geen waarde bevat, zodat andere dynamische vervolgkeuzefilters meer waarden kunnen bevatten. Selecteren **[!UICONTROL Reset all]** om de selectie uit alle vervolgkeuzefilters voor dat deelvenster te verwijderen.

Een dynamisch vervolgkeuzemenu maken:

* Eén dimensie naar de dropzone van het deelvenster slepen **terwijl u`[Shift]`**.
* Dynamische vervolgkeuzefilters zijn niet beschikbaar voor metriek, filters of datumbereiken.
* Klik met de rechtermuisknop op een vervolgkeuzefilter en selecteer **[!UICONTROL Delete filter]** om deze te verwijderen.

Als u met de rechtermuisknop op een dynamisch vervolgkeuzefilter klikt, hebt u dezelfde opties als statische vervolgkeuzefilters.

## Klikken met rechtermuisknop {#right-click}

Aanvullende functionaliteit voor een deelvenster is beschikbaar door met de rechtermuisknop op de koptekst van het deelvenster te klikken.

![Klik met de rechtermuisknop op opties voor een koptekst in een deelvenster.](assets/right-click-menu.png)

De volgende instellingen zijn beschikbaar:

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Insert Copied Panel/Visualization] | Hiermee kunt u een gekopieerd deelvenster of een visualisatie plakken (&quot;invoegen&quot;) naar een andere locatie in het project of naar een ander project. |
| [!UICONTROL Copy Panel] | Hiermee kunt u met de rechtermuisknop klikken en een deelvenster kopiëren, zodat u het kunt invoegen op een andere locatie in het project of in een ander project. |
| [!UICONTROL Duplicate Panel] | Hiermee maakt u een exacte kopie van het huidige deelvenster, dat u vervolgens kunt wijzigen. |
| [!UICONTROL Collapse/Expand all Panels] | Hiermee vouwt u alle projectdeelvensters samen en breidt u deze uit. |
| [!UICONTROL Collapse/Expand all Visualizations in Panel] | Hiermee vouwt u alle visualisaties in het huidige deelvenster samen en breidt u deze uit. |
| [!UICONTROL Edit Description] | Voeg (of bewerk) een tekstbeschrijving voor het paneel toe. |
| [!UICONTROL Get Panel Link] | Hiermee kunt u iemand doorsturen naar een specifiek deelvenster binnen een project. Wanneer op de koppeling wordt geklikt, moet de ontvanger zich aanmelden voordat deze wordt omgeleid naar het exacte deelvenster dat is gekoppeld aan. |
