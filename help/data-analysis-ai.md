---
description: Hoe te om de vragen van de gegevensanalyse van de documentatie van de Customer Journey Analytics te stellen
title: AI-assistent voor gegevensanalyse in Customer Journey Analytics
role: User, Admin
solution: Customer Journey Analytics
hidefromtoc: true
hide: true
source-git-commit: 376ad62c3883eef675f9b1df639e8c46ee259229
workflow-type: tm+mt
source-wordcount: '1587'
ht-degree: 0%

---


# AI-assistent voor gegevensanalyse in Customer Journey Analytics - Alpha

De Medewerker van AI van de Analyse van Gegevens is een Generatieve AI gespreksagent die u kan helpen sneller en efficiënt vragen beantwoorden u van uw gegevens van Analysis Workspace in Customer Journey Analytics hebt.

Wanneer u een vraag in AI Medewerker stelt, scant de Medewerker AI door alle componenten in uw gegevensmening, met inbegrip van de verschillende soorten metriek en componenten, en vertaalt uw herinnering in de juiste afmeting, metrisch, en datumwaaier voor uw analyse. In plaats van vertrouwd te moeten zijn met de componenten van de gegevensmening, en dan die componenten te slepen en te laten vallen in de beste combinatie om uw vraag te beantwoorden, kunt u de vraag eenvoudig typen in de Medewerker AI.

![ AI van de Analyse van Gegevens Medewerker ](assets/cja-ai-asst-da.gif)

## Functies binnen bereik versus functies buiten bereik voor de versie van de Alpha

### Functies voor Alpha binnen bereik

| Ondersteunde functie | Beschrijving |
| --- | --- |
| **bouwt en werkt visualisaties** bij | Hiermee genereert u een vrije-vormtabel en de bijbehorende visualisatie (bijvoorbeeld lijn, balk, donut, enz.).<p>Voorbeeld: *wat is de winst over SKUs van Februari aan Mei?* |
| **Ondersteunde visualisatietypen** | <ul><li>Lijn</li><li>Meerdere regels</li><li>Vrije vorm</li><li>Balk</li><li>Donut</li><li>Samenvattingsnummer</li></ul> |
| **uit-van-werkingsgebied snelle opsporing** | Als u een herinnering voorlegt die buiten werkingsgebied, zoals &quot;uitvoert dit project&quot;is, antwoordt de Medewerker door u te laten weten dat de vraag buiten werkingsgebied is. |
| **het Verhelderen van vragen** | Als u een vraag stelt die niet genoeg context voor de Medewerker AI heeft om te antwoorden, of te algemeen is, antwoordt de Medewerker AI met een het verduidelijken vraag en/of voorgestelde opties. Voorbeelden: <p>**Onderdelen**<ul><li>Metrisch: *welke metrische &quot;opbrengst&quot;metrisch u bedoelde?*</li><li>Dimension: *welke van hieronder &quot;gebieden&quot;wilt u zich op concentreren?*</li><li>Filter: *Welke &quot;filter van de Rekening&quot;wilde u toepassen?*</li><li>De Waaier van de datum: *door &quot;vorige maand&quot;, bedoelde u de laatste volledige maand of de laatste 30 dagen?*</li></ul>**punten van het Dimension**: Welke &quot;opslagnaam&quot;bedoelde u? (bijvoorbeeld Winkel #5274, Winkel #2949, enz.) |
| **Multi-draai** | De AI-assistent reageert op een vraag met de context van de voorgaande prompt(s), zodat gebruikers de visualisaties kunnen bijwerken en vervolgvragen kunnen stellen.Voorbeeld: <ul><li>Vraag 1: *de gebeurtenissen van de Trend van Maart.*</li><li>Vraag 2: *toon me de gegevens van Maart aan April in plaats daarvan*</li></ul> |
| **Verifiability** | De verifieerbaarheid en juistheid van gegevens kunnen worden bevestigd via de gegenereerde vrije-vormlijst en gegevensvisualisatie. Bijvoorbeeld, als een gebruiker *de orden van de Trend van de Tendens* vraagt, kunt u bevestigen dat correcte metrische (&quot;orden&quot;) en datumwaaier (&quot;vorige maand&quot;) in het onlangs geproduceerde paneel, gegevensvisualisatie, en vrije vormlijst werden geselecteerd. |
| **Terugkoppeling** | <ul><li>Stompelen omhoog</li><li>Miniatuur omlaag</li><li>Markering</li></ul> |

### Functies voor Alpha buiten bereik

| Niet-ondersteunde functie | Beschrijving |
| --- | --- |
| **overzicht of reactie van binnen-lijn** | De AI-assistent kan niet online reageren in de chatrail met een beknopt antwoord van een gebruiker prompt.Voorbeeld van aanwijzingen die buiten het bereik vallen:<ul><li>*geef me een samenvatting van de inzichten van mijn laatste herinnering.*</li><li>*vat de hoogtepunten van de lijnvisualisatie samen.*</li></ul> |
| **het Verhelderen van vragen** | Het verduidelijken van vragen is beperkt tot componenten en afmetingspunten. De AI-assistent kan geen duidelijkheid verschaffen over gegevensweergaven, visualisaties, granulariteit van gegevens, vergelijking, bereik, enzovoort. Zonder vragen te verduidelijken, blijft de Medewerker aan wat u het meest waarschijnlijk vraagt. Als het een onverwachte visualisatie of gegevensgranulariteit terugkeert, kunt u het multi-draai/updatemogelijkheid dan gebruiken om de visualisatie en de gegevens aan te passen. |
| **de Acties van Workspace / Mogelijkheden** | De AI-assistent kan geen actie ondernemen voor een gebruiker in Workspace, behalve het maken en bijwerken van visualisaties. Het kan bijvoorbeeld het volgende niet doen:<ul><li>Contextafhankelijke knoppen voor handelingen (toevoegen aan diagram, nieuw deelvenster, nieuwe tabel)</li><li>Delen</li><li>Exporteren</li><li>Downloaden</li><li>Gebruikersvoorkeuren beheren</li><li>Curate</li><li>Gegevensweergave beheren</li><li>Analytische dashboards-app</li><li>Attributie</li></ul> |
| **Niet gestaafde visualisatietypen** | <ul><li>Stroom</li><li>Fallout</li><li>Cohortabel</li><li>Gebied, gebied gestapeld</li><li>Stapel gestapeld</li><li>Opsommingsteken</li><li>Combo</li><li>Histogram</li><li>Horizontale balk, horizontale balk gestapeld</li><li>Hoofdmetrische samenvatting</li><li>Spreiding</li><li>Samenvattingswijziging</li><li>Tekst</li><li>Treemap</li><li>Venn</li></ul> |

<!---## Feature access in the Customer Journey Analytics UI

[Do we even need this section for the Alpha?]

The following parameters govern access to the Data Analysis AI Assistant feature:

* **Solution access**: The Data Analysis AI Assistant is available for Customer Journey Analytics Prime and Ultimate customers. It is not available in Adobe Analytics. 

It is also available in Adobe Experience Platform, Adobe Journey Optimizer, Adobe Real-Time CDP and additional Experience Platform apps.

* **Contractual access**: If you are not able to use AI Assistant, please contact your organization's administrator or Adobe Account Representative. Before your organization can use Data Analysis AI Assistant, your must agree to certain GenAI-related legal terms.

* **Permissions**: In the [!UICONTROL Adobe Admin Console], the [!UICONTROL Reporting Tools] **[!UICONTROL AI Assistant: Data Analysis]** permission determines access to this tool. A [product profile admin](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) needs to follow these steps in the [!UICONTROL Admin Console]:
   1. Navigate to **[!UICONTROL Admin Console]** > **[!UICONTROL Products and services]** > **[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Product Profiles]**
   1. Select the title of the product profile for which you want to provide access to [!UICONTROL AI Assistant: Product Knowledge].
   1. In the specific product profile, select **[!UICONTROL Permissions]**.
   1. Select ![Edit](/help/assets/icons/Edit.svg) to edit **[!UICONTROL Reporting Tools]**.
   1. Select ![AddCircle](/help/assets/icons/AddCircle.svg) to add **AI Assistant: Data Analysis** to **[!UICONTROL Included permission items]**.
   
      ![Add permission](assets/ai-assistant-permissions.png).

   1. Select **[!UICONTROL Save]** to save the permissions.

See [Access control](/help/technotes/access-control.md#access-control) for more information.--->

## Toegang tot en gebruik Data Analysis AI Assistant

1. Ga naar [ experience.adobe.com ](https://experience.adobe.com/), en login met uw Adobe ID.

2. Selecteer **Customer Journey Analytics** van het Huis van het Experience Cloud

3. Klik op **[!UICONTROL Blank project]** in de banner boven aan de projectpagina om een nieuw, leeg project te openen.

4. Zorg ervoor dat de geselecteerde gegevensweergave voor het deelvenster de gegevensweergave is die is ingeschakeld voor gebruik door AI Assistant voor het testen van Alpha&#39;s (bereik bij twijfel de weergave in het stapelkanaal van de Alpha).

5. Klik op het AI Assistant-chatpictogram rechtsboven.

   ![ AI Hulp pictogram ](/help/assets/ai-asst-icon.png)

6. Stel in het dialoogvenster **[!UICONTROL Ask about Customer Journey Analytics]** onderaan een vraag over gegevensanalyse in de AI-assistent.

### Voorbeeld 1

Stel bijvoorbeeld dat u geïnteresseerd bent in de orders die uw bedrijf in juli heeft ontvangen.

1. Voer *&quot;Trend orders in Juli.&quot;* in

   ![ AI herinnering ](/help/assets/ai-asst-prompt1.png)

2. De AI-assistent verzamelt nu inzichten door de gegevens in de gegevensweergave te bekijken, inclusief de meetgegevens en componenten. Het vertaalt de herinnering in de juiste afmeting/s, metrisch/s, en gegevenswaaier.

   Zoals u kunt zien, heeft het automatisch een grafiek van de Lijn en een vrije lijst geproduceerd die orden voor Juli tonen.

   ![ Antwoord aan herinnering - lijngrafiek en vrije vormlijst ](/help/assets/ai-asst-result.png)

### Voorbeeld 2

Daarna, wilt u zien hoe uw opbrengst per regio vergelijkt.

1. In het snelle venster, ga *&quot;tonen opbrengst door gebied in.&quot;*

2. De AI Assistant begrijpt op intelligente wijze dat u met &quot;regio&quot; het begrip &quot;klantgebied&quot; bedoelt. Het produceert een staafdiagram dat opbrengst door gebied het best toont:

   ![ Grafiek van de Bar ](/help/assets/ai-asst-result2.png)

### Voorbeeld 3

Naast het begrip van de opbrengsten per regio wilt u ook gegevens voor winst per regio zien. In plaats van het moeten de laatste herinnering opnieuw typen, kunt u de Medewerker van AI vragen om de meest recente visualisatie en vrije vormlijst bij te werken.

1. In het snelle venster, type *&quot;voeg winst toe.&quot;*

2. De grafiek **[!UICONTROL Bar]** verstrekt nog het meest beknopte antwoord, maar de winst metrische is toegevoegd als kolom in de vrije vormlijst:

   ![ Grafiek van de Bar ](/help/assets/ai-asst-result4.png)

### Voorbeeld 4

Laten we tot slot eens kijken naar de inkomsten per productcategorie.

1. In het snelle venster, ga *&quot;Deel van opbrengst door productcategorie in&quot;.*

2. De AI-assistent voor gegevensanalyse gebruikt opnieuw de meest geschikte visualisatie, in dit geval de **[!UICONTROL Donut]** visualisatie, om de vraag te beantwoorden.

   ![Cirkeldiagram](/help/assets/ai-asst-result3.png)

## Voorbeeld van aanwijzingen voor gegevensanalyse

Hier volgen enkele voorbeelden van veelvoorkomende vragen en van de visualisatie van het gebruik van AI Assistent voor het reageren op deze vragen.

| Voorbeeldprompt | Verwachte visualisatie |
| --- | --- |
| Toon me winsten in [ Maand ] | Lijn<p>Het vragen voor een trend of metrisch binnen een bepaalde tijdwaaier door gebrek keert een lijnvisualisatie terug. |
| De orden van de trend in [ Maand ] | Lijn |
| Toon opbrengst door gebied in [ Maand ] | Balk |
| Aandeel van de ontvangsten per productcategorie | Donut |
| Orders per dag van de week, van januari tot mei | Balk |
| Ordenen per geslacht tonen, van maart tot juni | Balk |
| Wat is de winst voor SKU&#39;s van februari tot mei | Balk |
| Ontvangsten door opslagnaam in [ Maand ] | Balk |
| Wat waren mijn top 10 SKUs door winst in [ Maand ]? | Balk |
| Aankoopaandeel per maand van het jaar | Donut |
| Totale winst in [ Maand ] | Samenvattingsnummer<p>Het vragen voor &quot;totaal&quot;van metrisch over een bepaalde tijdwaaier zou een Summiere aantalvisualisatie moeten terugkeren. |


## Aankondiging van aanbevolen procedures

De AI Medewerker verwerkt de context die door elke gebruikersherinnering wordt verstrekt en probeert intelligent met de meest aangewezen visualisatie evenals componenten in een vrije vormlijst te antwoorden. De reactie van de AI Assistant kan echter variëren op basis van de specifieke woorden en uitdrukkingen die worden gebruikt bij een prompt, zodat kleine taalwijzigingen tot verschillende resultaten kunnen leiden. Hieronder wordt beschreven hoe u het beste kunt maken: <ul><li>Wees specifiek: neem exacte termen op (zoals &quot;verkoop vorige maand in Californië&quot;) om de reactie te beperken.</li><li>Gebruik Metriek en filters wissen: wanneer u specifieke maatstaven toevoegt (zoals &quot;Opbrengst&quot;), afmetingen (bijvoorbeeld &quot;Websitenaam&quot;), filters (zoals &quot;iPhone-gebruikers&quot;) en datumbereiken (zoals &quot;Laatste drie maanden&quot;), kan de AI-assistent zich concentreren op de juiste gegevens.</li><li>Rechtstreekse vragen stellen: Rechtstreeks vragen, zoals &quot;Wat is de gemiddelde opbrengst per productcategorie dit jaar?&quot; maakt het voor de AI Assistant gemakkelijker om duidelijke, relevante inzichten te verschaffen.</li></ul>

Controleer de onderstaande voorbeeldtermen en woordgroepen die u kunt gebruiken in aanwijzingen met de Data Analysis AI Assistant in CJA, samen met de soorten reacties die u kunt verwachten. Deze voorbeelden zijn ontworpen om u vertrouwd te maken met de manier waarop specifieke woorden of structuren de uitvoer van de AI Assistant kunnen beïnvloeden, zodat u nauwkeurige en waardevolle inzichten krijgt. Houd er rekening mee dat de AI-assistent gebruikmaakt van Generative AI, zodat de visualisaties of geselecteerde gegevens enigszins kunnen variëren voor verschillende, vergelijkbare aanwijzingen.

| Gewenst resultaat | Voorbeelden van termen en woordgroepen |
| --- | --- |
| Samenvattingsnummer visualisatie | <ul><li>Totaal</li></ul> |
| Componenten vergelijken | <ul><li>Ververgelijken</li><li>VS</li><li>Contrast</li><li>Week tot week</li><li>Maand-over-maand</li><li>Kwart-over-Kwart</li><li>Jaar na jaar</li></ul> |
| Donut Visualization | <ul><li>Verhouding</li><li>Aandeel van</li><li>Distributie</li><li>Percentage</li><li>Bijdrage</li><li>Portion</li><li>Onderdelen</li></ul> |
| Lijnvisualisatie | <ul><li>Trend</li><li>[ Metrisch ] in [ Waaier van de Tijd ]</li></ul> |
| Staafvisualisatie | <ul><li>[ Metrisch ] door [ dimensie ]</li></ul> |

## Alpha testverwachtingen en gevraagde feedback

Na het stellen van elke vraag, herzie zorgvuldig het verstrekte antwoord van de medewerker. Het is cruciaal om de gegenereerde visualisaties uitgebreid te evalueren voordat u feedback geeft. Denk aan het volgende wanneer het evalueren van de reactie van AI Medewerker:

* Chat-spoorwegrespons of -sjabloon: evalueer de tekstreactie van de assistent. Is het antwoord geschikt gezien de context van uw vraag(en)?

* Visualisatie/grafiek: evalueer de visualisatie. Is het de aangewezen/verwachte visualisatie voor uw vraag, of zou u een verschillende visualisatie hebben verwacht?

* Vrije-vormtabel: evalueer de vrije-vormtabel. Zijn de gegevens van de vrije-vormlijst correct? Is het opsplitsen van gegevens op verzoek? Zijn de toegepaste filters die u vroeg of verwachtte?

* Foutbericht/Buiten-bereik: als een algemeen foutbericht wordt weergegeven waarin wordt aangegeven dat de vraag buiten het bereik valt, geef dan feedback of u van mening bent dat het bericht buiten het bereik geschikt is gezien uw vraag. Was uw vraag eigenlijk binnen het bereik?

**voor elke reactie, te geven gelieve duimen omhoog of duimen neer, die op de reactie** worden gebaseerd

Na de duimen omhoog/omlaag selectie, gelieve een selectie voor de relevante multi-uitgezochte doos terugkoppelt. Als u aanvullende feedback wilt geven, voegt u notities toe in het geopende tekstvak.

## Vragen en contact

* Vragen en feedback verzenden op de slack channel van de Alpha: #aep-cja-ai-assistent-testers???


