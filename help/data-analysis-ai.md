---
description: Vragen over gegevensanalyse van Customer Journey Analytics-documentatie stellen
title: AI-assistent voor gegevensanalyse in Customer Journey Analytics
role: User, Admin
solution: Customer Journey Analytics
feature: AI Tools
hidefromtoc: true
hide: true
exl-id: 262d5f15-16cb-4851-a769-7dbd205b2f81
source-git-commit: 99f82353e41180a0090e84e58593d63fc5cbe803
workflow-type: tm+mt
source-wordcount: '1633'
ht-degree: 0%

---

# Gegevens visualiseren met de AI Assistant in Customer Journey Analytics

De AI Medewerker in Customer Journey Analytics is een generatieve AI gespreksagent die snel en efficiënt vragen over uw gegevens beantwoordt. In Analysis Workspace worden relevante visualisaties gemaakt aan de hand van componenten uit uw gegevensweergave en met behulp van uw werkelijke gegevens.

Met de AI-assistent voor het beantwoorden van gegevenscentrische vragen in Analysis Workspace kunt u ontelbare uren besparen die u anders handmatig zou kunnen besteden aan het maken van visualisaties in Analysis Workspace en het vertrouwd maken met de componenten van de gegevensweergave.

![ AI van de Analyse van Gegevens Medewerker ](assets/cja-ai-asst-da.gif)

## Functies binnen bereik versus functies buiten bereik voor de Alpha-versie

### Alpha-functies binnen bereik

| Ondersteunde functie | Beschrijving |
| --- | --- |
| **bouwt en werkt visualisaties** bij | Hiermee genereert u een vrije-vormtabel en de bijbehorende visualisatie (zoals een lijn, balk, donut, enzovoort).<p>Voorbeeld: *wat is de winst over SKUs van Februari aan Mei?* |
| **Ondersteunde visualisatietypen** | <ul><li>Lijn</li><li>Meerdere regels</li><li>Vrije-vormtabel</li><li>Balk</li><li>Donut</li><li>Samenvattingsnummer</li></ul> |
| **uit-van-werkingsgebied snelle opsporing** | Als u een herinnering voorlegt die buiten werkingsgebied, zoals &quot;uitvoert dit project,&quot;antwoordt de Medewerker door u te laten weten dat de vraag buiten werkingsgebied is. |
| **het Verhelderen van vragen** | Als u een vraag stelt die niet genoeg context voor de Medewerker AI heeft om te antwoorden, of te algemeen is, antwoordt de Medewerker AI met een het verduidelijken vraag of voorgestelde opties. Voorbeelden: <p>**Onderdelen**<ul><li>Metrisch: *welke metrische &quot;opbrengst&quot;metrisch u bedoelde?*</li><li>Dimension: *welke van de hieronder &quot;gebieden&quot;wilt u zich op concentreren?*</li><li>Filter: *Welke &quot;filter van de Rekening&quot;wilde u toepassen?*</li><li>De Waaier van de datum: *door &quot;vorige maand,&quot;bedoelde u de laatste volledige maand of de laatste 30 dagen?*</li></ul>**de punten van Dimension**: Welke &quot;opslagnaam&quot;bedoelde u? (Bijvoorbeeld Winkel #5274, Winkel #2949, enzovoort.) |
| **Multi-draai** | De AI-assistent reageert op een vraag met de context van eerdere vragen, zodat gebruikers de visualisaties kunnen bijwerken en vervolgvragen kunnen stellen. Voorbeeld: <ul><li>Vraag 1: *de gebeurtenissen van de Trend van Maart.*</li><li>Vraag 2: *toon me de gegevens van Maart aan April in plaats daarvan*</li></ul> |
| **Verifiability** | De verifieerbaarheid en juistheid van gegevens kunnen worden bevestigd via de gegenereerde vrije-vormlijst en gegevensvisualisatie. Bijvoorbeeld, als een gebruiker *de orden van de Trend van de Tendens* vraagt, kunt u bevestigen dat correcte metrische (&quot;orden&quot;) en datumwaaier (&quot;vorige maand&quot;) in het onlangs geproduceerde paneel, gegevensvisualisatie, en vrije vormlijst werden geselecteerd. |
| **Terugkoppeling** | <ul><li>Stompelen omhoog</li><li>Miniatuur omlaag</li><li>Markering</li></ul> |

### Alpha-functies buiten bereik

| Niet-ondersteunde functie | Beschrijving |
| --- | --- |
| **overzicht of reactie van binnen-lijn** | De AI-assistent kan niet online reageren in de chatrail met een beknopt antwoord van een gebruikersprompt. Voorbeeld-vragen buiten bereik:<ul><li>*geef me een samenvatting van de inzichten van mijn laatste herinnering.*</li><li>*vat de hoogtepunten van de lijnvisualisatie samen.*</li></ul> |
| **het Verhelderen van vragen** | Het verduidelijken van vragen is beperkt tot componenten en afmetingspunten. De AI-assistent kan geen duidelijkheid verschaffen over zaken als gegevensweergaven, visualisaties, granulariteit van gegevens, vergelijking en bereik. Wanneer het verduidelijken van vragen niet kan worden gebruikt, blijft de Medewerker aan wat u het meest waarschijnlijk vraagt. Als het een onverwachte visualisatie of gegevensgranulariteit terugkeert, kunt u het multi-draai/updatemogelijkheid dan gebruiken om de visualisatie en de gegevens aan te passen. |
| **de acties van Workspace / Mogelijkheden** | De AI-assistent kan geen actie ondernemen voor een gebruiker in Workspace, behalve het maken en bijwerken van visualisaties. Het kan bijvoorbeeld geen van de volgende handelingen uitvoeren:<ul><li>Contextafhankelijke knoppen voor handelingen (toevoegen aan diagram, nieuw deelvenster, nieuwe tabel)</li><li>Delen</li><li>Exporteren</li><li>Downloaden</li><li>Gebruikersvoorkeuren beheren</li><li>Curate</li><li>Gegevensweergave beheren</li><li>Analytische dashboards-app</li><li>Attributie</li></ul> |
| **Niet gestaafde visualisatietypen** | <ul><li>Stroom</li><li>Fallout</li><li>Cohortabel</li><li>Gebied, gebied gestapeld</li><li>Stapel gestapeld</li><li>Opsommingsteken</li><li>Combo</li><li>Histogram</li><li>Horizontale balk, horizontale balk gestapeld</li><li>Hoofdmetrische samenvatting</li><li>Spreiding</li><li>Samenvattingswijziging</li><li>Tekst</li><li>Treemap</li><li>Venn</li></ul> |

<!---## Feature access in the Customer Journey Analytics UI

[Do we even need this section for the Alpha?]

The following parameters govern access to Data visualization in AI Assistant:

* **Solution access**: Data visualization in AI Assistant is available for Customer Journey Analytics Prime and Ultimate customers. It is not available in Adobe Analytics. 

It is also available in Adobe Experience Platform, Adobe Journey Optimizer, Adobe Real-Time CDP and additional Experience Platform apps.

* **Contractual access**: If you are not able to use AI Assistant, please contact your organization's administrator or Adobe Account Representative. Before your organization can use Data visualization in AI Assistant, your must agree to certain GenAI-related legal terms.

* **Permissions**: In the [!UICONTROL Adobe Admin Console], the [!UICONTROL Reporting Tools] **[!UICONTROL AI Assistant: Data visualization]** permission determines access to this tool. A [product profile admin](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) needs to follow these steps in the [!UICONTROL Admin Console]:
   1. Navigate to **[!UICONTROL Admin Console]** > **[!UICONTROL Products and services]** > **[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Product Profiles]**
   1. Select the title of the product profile for which you want to provide access to [!UICONTROL AI Assistant: Product Knowledge].
   1. In the specific product profile, select **[!UICONTROL Permissions]**.
   1. Select ![Edit](/help/assets/icons/Edit.svg) to edit **[!UICONTROL Reporting Tools]**.
   1. Select ![AddCircle](/help/assets/icons/AddCircle.svg) to add **AI Assistant: Data visualization** to **[!UICONTROL Included permission items]**.
   
      ![Add permission](assets/ai-assistant-permissions.png).

   1. Select **[!UICONTROL Save]** to save the permissions.

See [Access control](/help/technotes/access-control.md#access-control) for more information.--->

## Toegang tot en gebruik gegevensvisualisatie in AI Assistant

1. Ga naar [ experience.adobe.com ](https://experience.adobe.com/) en login met uw Adobe ID.

2. Selecteer **Customer Journey Analytics** van het Huis van Experience Cloud.

3. Selecteer **[!UICONTROL Blank project]** in de banner bij de bovenkant van de projectpagina om een nieuw leeg project te openen.

4. Zorg ervoor dat de geselecteerde gegevensweergave voor het deelvenster dezelfde gegevensweergave is als de gegevensweergave die is ingeschakeld voor gebruik met de AI-assistent voor Alpha-tests.

   Neem contact op met het Alpha Slack-kanaal als u het niet zeker weet.

5. Selecteer het AI Assistant-chatpictogram rechtsboven op de pagina.

   Als u het praatjepictogram niet ziet, contacteer uw beheerder zodat kunnen zij de volgende eigenschappen in Admin Conole toelaten:

   * **[!UICONTROL AI Assistant: Product Knowledge]**

   * **[!UICONTROL AI Assistant: Data Analysis]**

   Voor extra details, kunnen de beheerders [ deze instructies ](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/access) zien.

   ![ AI Hulp pictogram ](/help/assets/ai-asst-icon.png)

6. Stel in het dialoogvenster **[!UICONTROL Ask about Customer Journey Analytics]** onder aan de pagina een vraag over gegevensvisualisatie in de AI-assistent.

   Zie de volgende voorbeelden voor meer informatie.

### Voorbeeld 1

Stel bijvoorbeeld dat u geïnteresseerd bent in de orders die uw bedrijf in juli heeft ontvangen.

**Herinnering:** ga *&quot;De orden van de Trend in Juli in.&quot;*

![ AI herinnering ](/help/assets/ai-asst-prompt1.png)

**Reactie:** AI Medewerker verzamelt inzicht door de gegevens in de gegevensmening, met inbegrip van de metriek en de componenten te bekijken. Het vertaalt de herinnering in de juiste afmetingen en metriek binnen de gegevenswaaier.

Zoals u kunt zien, produceerde het automatisch een lijngrafiek en een vrije lijst om orden voor Juli te tonen.

![ Antwoord aan herinnering - lijngrafiek en vrije vormlijst ](/help/assets/ai-asst-result.png)

### Voorbeeld 2

Daarna, wilt u zien hoe uw opbrengst per regio vergelijkt.

**Herinnering:** in het snelle venster, ga *&quot;Show opbrengst door gebied in.&quot;*

**Reactie:** AI Medewerker begrijpt intelligent dat door &quot;gebied,&quot;u &quot;klantengebied&quot;bedoelt.&quot; Het produceert een staafdiagram dat opbrengst door gebied het best toont:

![ Grafiek van de Bar ](/help/assets/ai-asst-result2.png)

### Voorbeeld 3

Naast het begrip van de opbrengsten per regio wilt u ook gegevens voor winst per regio zien. In plaats van de vorige vraag te herhalen, kunt u de AI Medewerker vragen om de meest recente visualisatie en de vrije vormlijst bij te werken.

**Herinnering:** in het snelle venster, type *&quot;voeg winst toe.&quot;*

**Reactie:** De **[!UICONTROL Bar]** grafiek verstrekt nog het meest beknopte antwoord, maar de winst metrische is toegevoegd als kolom in de vrije vormlijst:

![ Grafiek van de Bar ](/help/assets/ai-asst-result4.png)

### Voorbeeld 4

Tot slot, kijk de opbrengst per productcategorie.

**Herinnering:** in het snelle venster, ga *&quot;Deel van opbrengst door productcategorie in.&quot;*

**Reactie:** Opnieuw, neemt de gegevensvisualisatie in AI Medewerker de meest aangewezen visualisatie, in dit geval **[!UICONTROL Donut]** visualisatie, om de vraag te beantwoorden.

![Cirkeldiagram](/help/assets/ai-asst-result3.png)

## Voorbeeld van vragen voor gegevensvisualisatie

Hier volgen enkele voorbeelden van veelvoorkomende herinneringen en de visualisaties die door de AI Assistant worden gebruikt om op deze vragen te reageren.

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

De AI Medewerker verwerkt de context die door elke gebruikersherinnering wordt verstrekt en probeert intelligent met de meest aangewezen visualisatie en de componenten in een vrije vormlijst te antwoorden.

De reacties kunnen variëren afhankelijk van de specifieke woorden en uitdrukkingen die in de herinnering worden gebruikt, en lichte veranderingen in taal kunnen tot verschillende resultaten leiden.

Houd rekening met de volgende richtlijnen om de beste resultaten te bereiken:

* Wees specifiek: neem exacte termen op om de reactie te beperken. Hier volgt een voorbeeld van een specifieke prompt: &quot;De verkoop van vorige maand in Californië&quot;

* Gebruik duidelijke maatstaven en filters: wanneer u specifieke maatstaven (zoals &quot;Opbrengst&quot;), afmetingen (zoals &quot;Websitenaam&quot;), filters (zoals &quot;iPhone-gebruikers&quot;) en datumbereiken (zoals &quot;Laatste drie maanden&quot;) toevoegt, kan de AI-assistent zich op de juiste gegevens concentreren.

* Stel directe vragen: Door vragen rechtstreeks te formuleren maakt u het voor de AI Assistant gemakkelijker om duidelijke en relevante inzichten te verschaffen. Hier volgt een voorbeeld van een directe vraag: &quot;Wat is de gemiddelde opbrengst per productcategorie dit jaar?&quot;

Controleer de volgende lijst van voorbeeldtermijnen en uitdrukkingen die u in herinneringen met gegevensvisualisatie in AI Medewerker kunt gebruiken, samen met de soorten reacties kunt u verwachten.

Deze voorbeelden zijn ontworpen om u vertrouwd te maken met de manier waarop specifieke woorden of structuren de uitvoer van de AI Assistant kunnen beïnvloeden, zodat u nauwkeurige en waardevolle inzichten krijgt. In de AI-assistent wordt gebruikgemaakt van generatieve AI, zodat de visualisatie of de geselecteerde gegevens enigszins kunnen variëren tussen vergelijkbare aanwijzingen.

| Gewenst resultaat | Voorbeelden van termen en woordgroepen |
| --- | --- |
| Visualisatie van overzichtsnummers | <ul><li>Totaal</li></ul> |
| Componenten vergelijken | <ul><li>Ververgelijken</li><li>VS</li><li>Contrast</li><li>Week tot week</li><li>Maand-over-maand</li><li>Kwart-over-Kwart</li><li>Jaar na jaar</li></ul> |
| Donut visualisatie | <ul><li>Verhouding</li><li>Aandeel van</li><li>Distributie</li><li>Percentage</li><li>Bijdrage</li><li>Portion</li><li>Onderdelen</li></ul> |
| Lijnvisualisatie | <ul><li>Trend</li><li>[ Metrisch ] in [ waaier van de Tijd ]</li></ul> |
| Staafvisualisatie | <ul><li>[ Metrisch ] door [ Dimension ]</li></ul> |

## Alpha testverwachtingen en gevraagde feedback

Na het stellen van elke vraag, herzie zorgvuldig het verstrekte antwoord van de medewerker. Het is cruciaal om de gegenereerde visualisaties uitgebreid te evalueren voordat u feedback geeft.

Houd rekening met het volgende wanneer u een reactie van de AI Assistant evalueert:

* Chat-spoorwegrespons of -sjabloon: evalueer de tekstreactie van de assistent. Is het antwoord passend gezien de context van uw vraag?

* Visualisatie/grafiek: evalueer de visualisatie. Is het de aangewezen of verwachte visualisatie voor uw vraag, of zou u een verschillende visualisatie hebben verwacht?

* Vrije-vormtabel: evalueer de vrije-vormtabel. Zijn de gegevens van de vrije-vormlijst correct? Is het opsplitsen van gegevens op verzoek? Zijn de toegepaste filters die u vroeg of verwachtte?

* Foutbericht / Buiten-bereik: als een algemeen foutbericht wordt gegeven waarin wordt aangegeven dat de vraag buiten bereik valt, geef dan feedback of u het bericht buiten bereik geschikt acht, gegeven uw vraag. Was uw vraag eigenlijk binnen bereik?

**voor elke reactie, geef omhoog duimen of duimen neer, die op de reactie wordt gebaseerd.**

Na de duimen omhoog of duim onderaan selectie, te maken gelieve een selectie voor de relevante multi-uitgezochte doos terugkoppelt. Als u aanvullende feedback wilt geven, voegt u notities toe in het geopende tekstvak.

## Vragen en contact

* Stuur vragen en feedback op de Alpha Slack-zender: #cja-Assistant-data-alpha
