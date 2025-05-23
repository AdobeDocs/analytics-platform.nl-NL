---
description: Vragen over gegevensanalyse van Customer Journey Analytics-documentatie stellen
title: Gegevens visualiseren met de Data Insights Agent in Customer Journey Analytics
role: User, Admin
solution: Customer Journey Analytics
feature: AI Tools
exl-id: 262d5f15-16cb-4851-a769-7dbd205b2f81
source-git-commit: bef00aa251831cdb809a6243b5d5a8e2c0dda9bb
workflow-type: tm+mt
source-wordcount: '1803'
ht-degree: 0%

---

# Gegevens visualiseren met Data Insights Agent in Customer Journey Analytics

{{release-limited-testing}}

>[!AVAILABILITY]
>
>De Agent van Gegevens is beschikbaar aan in aanmerking komende klanten voor een beperkte tijd. De toegang tot de Agent van Gegevens zal op 30 november 2025 beëindigen. Als u de Data Insights Agent zonder onderbreking wilt blijven gebruiken, vraagt u uw Adobe-accountvertegenwoordiger om meer informatie over het in licentie geven van Data Insights Agent.

De Agent van Gegevens, toegankelijk van de Medewerker van AI in Customer Journey Analytics, is een generatieve AI gespreksagent die snel en efficiënt vragen over uw gegevens beantwoordt. In Analysis Workspace worden relevante visualisaties gemaakt aan de hand van componenten uit uw gegevensweergave en met behulp van uw werkelijke gegevens.

Het gebruiken van de Agent van Gegevens om gegeven-centric vragen in Analysis Workspace te beantwoorden kan ontelbare uren besparen die u anders manueel het bouwen van visualisaties in Analysis Workspace zou kunnen doorbrengen en zich met uw componenten van de gegevensmening vertrouwd maken.

![ Agent van de Inzichten van Gegevens binnen de Medewerker AI ](assets/cja-ai-asst-da.gif)

## Functies binnen bereik versus buiten bereik

| Functie | Binnen bereik | Buiten bereik |
| --- | --- | --- |
| **Visualisatietypen** | <ul><li>Lijn</li><li>Meerdere regels</li><li>Vrije-vormtabel</li><li>Balk</li><li>Donut</li><li>Samenvattingsnummer</li></ul> | <ul><li>Stroom</li><li>Fallout</li><li>Cohortabel</li><li>Gebied, gebied gestapeld</li><li>Stapel gestapeld</li><li>Opsommingsteken</li><li>Combo</li><li>Histogram</li><li>Horizontale balk, horizontale balk gestapeld</li><li>Hoofdmetrische samenvatting</li><li>Spreiding</li><li>Samenvattingswijziging</li><li>Tekst</li><li>Treemap</li><li>Venn</li></ul> |
| **de acties van Workspace en agentenmogelijkheden** | <ul><li>Visualisaties maken en bijwerken<p>Hiermee genereert u een vrije-vormtabel en de bijbehorende visualisatie (zoals een lijn, balk, donut, enzovoort).<p>Bijvoorbeeld, *wat is de winst over SKUs van Februari aan Mei?*</p></li><li>Vervolgvragen stellen</li><li>Reageer op een vraag in de context van om het even welke vroegere herinneringen<p>Bijvoorbeeld:</p> <ul><li>Vraag 1: *de gebeurtenissen van de Trend van Maart.*</li><li>Vraag 2: *toon me de gegevens van Maart aan April in plaats daarvan*</li></ul> </li><li>Snelle detectie buiten bereik<p>Als u een herinnering voorlegt die buiten werkingsgebied, zoals *is dit project* uitvoeren, antwoordt de Agent van Gegevens Inzichten door u te informeren dat de vraag buiten werkingsgebied is.</p></li></ul> | <ul><li>Contextafhankelijke knoppen voor handelingen (toevoegen aan diagram, nieuw deelvenster, nieuwe tabel)</li><li>Delen</li><li>Exporteren</li><li>Downloaden</li><li>Gebruikersvoorkeuren beheren</li><li>Curate</li><li>Gegevensweergave beheren</li><li>Analytische dashboards-app</li><li>Attributie</li><li>Samenvatting of reactie online<p>Data Insights Agent kan niet online in de chat rail reageren met een beknopt antwoord van een gebruikersprompt. De voorbeelden van uit-van-werkingsgebied herinneringen zijn, *geven me een samenvatting van de inzichten van mijn laatste herinnering* en *vatten de hoogtepunten van de lijnvisualisatie samen.*</p></li></ul> |
| **het Verhelderen van vragen** | Als u een vraag stelt die niet genoeg context voor de Agent van Gegevens heeft om te antwoorden, of te generiek is, antwoordt de Agent van Gegevens met een het verduidelijken vraag of voorgestelde opties. <p>De volgende verduidelijkende vragen zijn voorbeelden van aan onderdelen gerelateerde vragen:</p><ul><li>Metrisch: *welke metrische &quot;opbrengst&quot;metrisch u bedoelde?*</li><li>Dimension: *welke van de hieronder &quot;gebieden&quot;wilt u zich op concentreren?*</li><li>Segment: *welk &quot;segment van de Rekening&quot;wilde u toepassen?*</li><li>De Waaier van de datum: *door &quot;vorige maand,&quot;bedoelde u de laatste volledige maand of de laatste 30 dagen?*</li></ul><p>De volgende verduidelijking is een voorbeeld van een vraag die verband houdt met dimensie-elementen:</p> <ul><li>Welke &quot;winkelnaam&quot; bedoelde je? (Bijvoorbeeld Winkel #5274, Winkel #2949, enzovoort.)</li></ul> | Het verduidelijken van vragen is beperkt tot componenten en afmetingspunten. De Agent van Gegevens kan geen dingen zoals gegevensmeningen, visualisaties, gegevensgranulariteit, vergelijking, en werkingsgebied verduidelijken. Wanneer het verduidelijken van vragen niet kan worden gebruikt, blijft de agent aan wat u het meest waarschijnlijk vraagt. Als het een onverwachte visualisatie of gegevensgranulariteit terugkeert, kunt u een vervolgvraag stellen of de visualisatie en de gegevens aanpassen. |
| **verifieerbaarheid en correctheid van Gegevens** | De verifieerbaarheid en de correctheid van gegevens kunnen worden bevestigd door de geproduceerde vrije vormlijst en gegevensvisualisatie te bekijken. <p>Bijvoorbeeld, als u de Agent van de Inzichten van Gegevens aan *orden van de Trend* vraagt, kunt u bevestigen dat correcte metrische (&quot;orden&quot;) en datumwaaier (&quot;vorige maand&quot;) in het onlangs geproduceerde paneel, gegevensvisualisatie, en vrije vormlijst werden geselecteerd. | De Data Insights Agent reageert niet door u te informeren welke componenten of visualisaties zijn toegevoegd.</p> |
| **mechanismen van de Terugkoppeling** | <ul><li>Stompelen omhoog</li><li>Miniatuur omlaag</li><li>Markering</li></ul> |  |


## De toegang tot Data Insights Agent in Customer Journey Analytics beheren

De volgende parameters regelen de toegang tot Data Insights Agent in Customer Journey Analytics:

* **de toegang van de Oplossing**: De Agent van Gegevens is beschikbaar voor alle klanten van Customer Journey Analytics als deel van een beperkt toegangsprogramma tot 30 November, 2025. Het is niet beschikbaar in Adobe Analytics.

* **Contractuele toegang**: Als u de Agent van Gegevens van de Inzichten in de Medewerker van AI niet kunt gebruiken, gelieve de beheerder van uw organisatie of het de rekeningsteam van Adobe te contacteren. Voordat uw organisatie Data Insights Agent kan gebruiken, moet u akkoord gaan met bepaalde juridische voorwaarden die betrekking hebben op generatieve AI.

* **Toestemmingen**: De noodzakelijke toestemmingen moeten in [!UICONTROL Adobe Admin Console] worden verleend alvorens de gebruikers tot de Agent van Gegevens kunnen toegang hebben.

  Om toestemmingen te verlenen, moet a [ admin van het productprofiel ](https://helpx.adobe.com/nl/enterprise/using/manage-product-profiles.html) de volgende stappen in [!UICONTROL Admin Console] voltooien:
   1. Selecteer in **[!UICONTROL Admin Console]** de tab **[!UICONTROL Products]** om de pagina **[!UICONTROL All products and services]** weer te geven.
   1. Selecteer **[!UICONTROL Customer Journey Analytics]** .
   1. Selecteer op het tabblad **[!UICONTROL Product Profiles]** de titel van het productprofiel waartoe u toegang wilt verlenen aan [!UICONTROL AI Assistant: Product Knowledge] .
   1. Selecteer in het specifieke productprofiel de tab **[!UICONTROL Permissions]** .

      ![ het lusje van Toestemmingen in Admin Console ](assets/ai-assistant-permissions-tab.png)

   1. In de **[!UICONTROL Reporting Tools]** rij in de verstrekte lijst, uitgezocht geef pictogram uit ![ ](/help/assets/icons/Edit.svg) uitgeeft.
   1. De rol aan of onderzoek naar **[!UICONTROL AI Assistant: Product Knowledge]**, dan selecteert het plus pictogram ![ AddCircle ](/help/assets/icons/AddCircle.svg) naast deze toestemming.

      De machtiging **[!UICONTROL AI Assistant: Product Knowledge]** wordt toegevoegd aan de kolom **[!UICONTROL Included permission items]** .

      ![ voeg toestemming ](assets/ai-assistant-permissions.png) toe.

   1. Selecteer het **[!UICONTROL Data View Tools]** lusje, dan selecteer het plusteken ![ AddCircle ](/help/assets/icons/AddCircle.svg) naast de **[!UICONTROL Data Insights Agent]** toestemming.

      De machtiging **[!UICONTROL Data Insights Agent]** wordt toegevoegd aan de kolom **[!UICONTROL Included permission items]** .

      ![ voeg toestemming ](assets/ai-assistant-permissions-dataviewtools.png) toe.

   1. Selecteer het tabblad **[!UICONTROL Data Views]** om de gegevensweergaven te kiezen die u wilt inschakelen voor Data Insights Agent.

      >[!IMPORTANT]
      >
      >De Data Insights Agent kan verwijzen naar de opgenomen gegevensweergaven ergens op dezelfde dag dat u deze inschakelt in de Admin Console.

   1. Onderzoek naar of rol aan de gegevensmeningen die u wilt toelaten, dan selecteren plus pictogram ![ AddCircle ](/help/assets/icons/AddCircle.svg) naast de naam van elke gegevensmening.

      Elke gegevensweergave die u toevoegt, is zichtbaar in de kolom **[!UICONTROL Included permission items]** .

      ![ voeg toestemming ](assets/ai-assistant-permissions-dataviews.png) toe.

   1. Selecteer **[!UICONTROL Save]** om de machtigingen op te slaan.

  Voor extra informatie over toegangsbeheer, zie [ controle van de Toegang ](/help/technotes/access-control.md#access-control).

## De Agent van de Inzicht van Gegevens van de toegang in AI Medewerker

1. Ga naar [ experience.adobe.com ](https://experience.adobe.com/) en login met uw Adobe ID.

2. Selecteer **Customer Journey Analytics** van het Huis van Experience Cloud.

3. Selecteer **[!UICONTROL Blank project]** in de banner bij de bovenkant van de projectpagina om een nieuw leeg project te openen.

4. Zorg ervoor dat de geselecteerde gegevensmening voor het paneel een gegevensmening is die voor gebruik met de Agent van Gegevens werd toegelaten Inzichten, zoals die in [ wordt beschreven beheert toegang tot de Agent van Gegevens Inzichten in Customer Journey Analytics ](#manage-access-to-data-insights-agent-in-customer-journey-analytics).

5. Selecteer het AI Assistant-chatpictogram rechtsboven op de pagina.

   Als u het praatjepictogram niet ziet, contacteer uw beheerder zodat kunnen zij de volgende eigenschappen in Admin Conole toelaten:

   * Rapportgereedschappen: **[!UICONTROL AI Assistant: Product Knowledge]**

   * Gereedschappen voor gegevensweergave: **[!UICONTROL Data Insights Agent]**

   Voor extra details, zie [ toegang tot de Agent van Gegevens beheren in Customer Journey Analytics ](#manage-access-to-data-insights-agent-in-customer-journey-analytics).

   ![ AI Hulp pictogram ](/help/assets/ai-asst-icon.png)

6. Stel in het dialoogvenster **[!UICONTROL Ask about Customer Journey Analytics]** onder aan de pagina een vraag over gegevensvisualisatie met de Data Insights Agent.

   Zie de volgende voorbeelden voor meer informatie.

### Voorbeeld 1

Stel bijvoorbeeld dat u geïnteresseerd bent in de orders die uw bedrijf in juli heeft ontvangen.

**Herinnering:** ga *&quot;De orden van de Trend in Juli in.&quot;*

![ AI herinnering ](/help/assets/ai-asst-prompt1.png)

**Reactie:** de Agent van Gegevens vangt inzichten door de gegevens in de gegevensmening, met inbegrip van de metriek en de componenten te bekijken. Het vertaalt de herinnering in de juiste afmetingen en metriek binnen de gegevenswaaier.

Zoals u kunt zien, produceerde het automatisch een lijngrafiek en een vrije lijst om orden voor Juli te tonen.

![ Antwoord aan herinnering - lijngrafiek en vrije vormlijst ](/help/assets/ai-asst-result.png)

### Voorbeeld 2

Daarna, wilt u zien hoe uw opbrengst per regio vergelijkt.

**Herinnering:** in het snelle venster, ga *&quot;Show opbrengst door gebied in.&quot;*

**Reactie:** De Agent van Gegevens begrijpt intelligent dat door &quot;gebied,&quot;u &quot;klantengebied&quot;bedoelt.&quot; Het produceert een staafdiagram dat opbrengst door gebied het best toont:

![ Grafiek van de Bar ](/help/assets/ai-asst-result2.png)

### Voorbeeld 3

Naast het begrip van de opbrengsten per regio, wilt u ook gegevens voor winst per regio zien. In plaats van de vorige herinnering te herhalen, kunt u de Agent van Gegevens verzoeken om de meest recente visualisatie en vrijevormlijst bij te werken.

**Herinnering:** in het snelle venster, type *&quot;voeg winst toe.&quot;*

**Reactie:** De **[!UICONTROL Bar]** grafiek verstrekt nog het meest beknopte antwoord, maar de winst metrische is toegevoegd als kolom in de vrije vormlijst:

![ Grafiek van de Bar ](/help/assets/ai-asst-result4.png)

### Voorbeeld 4

Tot slot, kijk de opbrengst per productcategorie.

**Herinnering:** in het snelle venster, ga *&quot;Deel van opbrengst door productcategorie in.&quot;*

**Reactie:** opnieuw, neemt de Agent van Gegevens de meest aangewezen visualisatie, in dit geval de **[!UICONTROL Donut]** visualisatie, om de vraag te beantwoorden.

![Cirkeldiagram](/help/assets/ai-asst-result3.png)

## Voorbeeld van vragen voor gegevensvisualisatie

Hieronder volgen enkele voorbeelden van veelvoorkomende herinneringen en de visualisaties die door Data Insights Agent worden gebruikt om te reageren op deze herinneringen.

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

De Agent van Gegevens verwerkt de context die door elke gebruikersherinnering wordt verstrekt en probeert om intelligent met de meest aangewezen visualisatie en de componenten in een vrije vormlijst te antwoorden.

De reacties kunnen variëren afhankelijk van de specifieke woorden en uitdrukkingen die in de herinnering worden gebruikt, en lichte veranderingen in taal kunnen tot verschillende resultaten leiden.

Houd rekening met de volgende richtlijnen om de beste resultaten te bereiken:

* **ben specifiek:** omvat nauwkeurige termijnen om onderaan de reactie te versmallen. Het volgende is een voorbeeld van een specifieke herinnering: &quot;De verkoop van vorige maand in Californië&quot;

* **gebruik duidelijke metriek, dimensies, en segmenten:** Toevoegend specifieke metriek (zoals &quot;Opbrengst&quot;), dimensies (zoals &quot;Websitenaam&quot;), segmenten (zoals &quot;de gebruikers van iPhone&quot;), en datumwaaiers (zoals &quot;laatste drie maanden&quot;) helpt de Agent van Gegevens zich op de juiste gegevens concentreren.

* **stel directe vragen:** het Begeleidende vragen maakt het voor de Agent van Gegevens direct gemakkelijker om duidelijke, relevante inzichten te verstrekken. Het volgende is een voorbeeld van het stellen van een directe vraag in een vroeg stadium: &quot;Wat is de gemiddelde opbrengst per productcategorie dit jaar?&quot;

Herzie de volgende lijst van voorbeeldtermijnen en uitdrukkingen die u in herinneringen met de Agent van Gegevens kunt gebruiken Inzichten, samen met de soorten reacties kunt verwachten u.

Deze voorbeelden worden ontworpen om u vertrouwd te maken met hoe de specifieke woorden of structuren de output van de Agent van Gegevens kunnen beïnvloeden Insight, die nauwkeurigere en waardevolle inzichten verzekeren. De Agent van de Inzichten van gegevens gebruikt generatieve AI, zodat kunnen de visualisaties of de geselecteerde gegevens lichtjes over gelijkaardige herinneringen variëren.

| Gewenst resultaat | Voorbeelden van termen en woordgroepen |
| --- | --- |
| Visualisatie van overzichtsnummers | <ul><li>Totaal</li></ul> |
| Componenten vergelijken | <ul><li>Ververgelijken</li><li>VS</li><li>Contrast</li><li>Week tot week</li><li>Maand-over-maand</li><li>Kwart-over-Kwart</li><li>Jaar na jaar</li></ul> |
| Donut visualisatie | <ul><li>Verhouding</li><li>Aandeel van</li><li>Distributie</li><li>Percentage</li><li>Bijdrage</li><li>Portion</li><li>Onderdelen</li></ul> |
| Lijnvisualisatie | <ul><li>Trend</li><li>[ Metrisch ] in [ waaier van de Tijd ]</li></ul> |
| Staafvisualisatie | <ul><li>[ Metrisch ] door [ Dimension ]</li></ul> |

<!--

## Beta testing expectations and requested feedback

After posing each question, carefully review the assistant's provided answer. It's crucial to evaluate the generated visualizations comprehensively before providing feedback. 

Consider the following when evaluating a response from Data Insights Agent: 

* Chat rail response or template: Evaluate the textual response provided. Is the response appropriate given the context of your prompt? 

* Visualization/chart: Evaluate the visualization. Is it the appropriate or expected visualization for your question, or would you have expected a different visualization?  

* Freeform table: Evaluate the freeform table. Is the freeform table data correct? Is it breaking down data where requested? Are the applied segments those that you requested or expected? 

* Error Message / Out-of-Scope: If a generic error message is given stating the question is out of scope, provide feedback on whether you think the out-of-scope message is appropriate, given your prompt. Was your prompt actually in scope? 

**For every response, give a thumbs up or thumbs down, based on the response.**

Following the thumbs up or thumbs down selection, please make a selection for the relevant multi-select feedback boxes. If you want to provide additional feedback, add notes in the open text box.

## Questions and Contact

* Send questions and feedback in the Beta Slack channel: #data-insights-agent-in-cja-beta

-->

