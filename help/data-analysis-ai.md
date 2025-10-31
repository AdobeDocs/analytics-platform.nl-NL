---
description: Vragen stellen over data-analyse van Customer Journey Analytics-documentatie
title: Gegevens visualiseren met de Data Insights Agent in Customer Journey Analytics
role: User, Admin
solution: Customer Journey Analytics
feature: AI Tools
exl-id: 262d5f15-16cb-4851-a769-7dbd205b2f81
source-git-commit: 77f350923bb750bf99fe4080e44968f9a52cd7da
workflow-type: tm+mt
source-wordcount: '2411'
ht-degree: 0%

---

# Gegevens visualiseren met Data Insights Agent

>[!AVAILABILITY]
>
>Data Insights Agent is gedurende een beperkte periode beschikbaar voor in aanmerking komende klanten. De toegang tot Data Insights Agent loopt af op 28 februari 2026. Als u Data Insights Agent zonder onderbreking wilt blijven gebruiken, neemt u contact op met uw Adobe-accountvertegenwoordiger voor meer informatie over licenties voor Data Insights Agent.

Data Insights Agent, toegankelijk van de [&#x200B; Medewerker AI &#x200B;](/help/ai-assistant.md) in Customer Journey Analytics, is een generatieve AI gespreksagent die snel en efficiënt vragen over uw gegevens beantwoordt. In Analysis Workspace worden relevante visualisaties gemaakt aan de hand van componenten uit uw gegevensweergave en met behulp van uw werkelijke gegevens.

Als u Data Insights Agent gebruikt om gegevenscentrische vragen in Analysis Workspace te beantwoorden, bespaart u ontelbare uren die u anders handmatig zou kunnen besteden aan het maken van visualisaties in Analysis Workspace en het vertrouwd maken met de componenten van de gegevensweergave.

![&#x200B; Data Insights Agent binnen de Medewerker AI &#x200B;](assets/cja-ai-asst-da.gif)

## Functies binnen bereik versus buiten bereik

| Functie | Binnen bereik | Buiten bereik |
| --- | --- | --- |
| **Visualisatietypen** | <ul><li>Lijn</li><li>Meerdere regels</li><li>Vrije-vormtabel</li><li>Balk</li><li>Donut</li><li>Samenvattingsnummer</li></ul> | <ul><li>Stroom</li><li>Fallout</li><li>Cohortabel</li><li>Gebied, gebied gestapeld</li><li>Stapel gestapeld</li><li>Opsommingsteken</li><li>Combo</li><li>Histogram</li><li>Horizontale balk, horizontale balk gestapeld</li><li>Hoofdmetrische samenvatting</li><li>Spreiding</li><li>Samenvattingswijziging</li><li>Tekst</li><li>Treemap</li><li>Venn</li><li>Analyse met instructies: Actieve groei, Conversietrends, Betrokkenheid, impact voor eerste gebruik, Frequentie, Trechter, Net groei, impact release, Behoud, Tijdlijn, Trends</li></ul> |
| **de acties van Workspace en agentenmogelijkheden** | <ul><li>Visualisaties maken en bijwerken<p>Hiermee genereert u een vrije-vormtabel en de bijbehorende visualisatie (zoals een lijn, balk, donut, enzovoort).<p>Bijvoorbeeld, *wat is de winst over SKUs van Februari aan Mei?*</p></li><li>Vervolgvragen stellen<p>Reageer op een vraag in de context van om het even welke vroegere herinneringen. Bijvoorbeeld:</p> <ul><li>Vraag 1: *de gebeurtenissen van de Trend van Maart.*</li><li>Vraag 2: *toon me de gegevens van Maart aan April in plaats daarvan*</li></ul> </li><li>Snelle detectie buiten bereik<p>Als u een herinnering voorlegt die buiten werkingsgebied, zoals *is dit project* uitvoeren, antwoordt Data Insights Agent door u te informeren dat de vraag buiten werkingsgebied is.</p></li></ul> | <ul><li>Delen</li><li>Exporteren</li><li>Downloaden</li><li>Gebruikersvoorkeuren beheren</li><li>Gegevensweergave beheren</li><li>Analytische dashboards-app</li><li>Attributie</li><li>Samenvatting of reactie online<p>Data Insights Agent kan niet online in de chatrail reageren met een beknopt antwoord van een gebruikersprompt. De voorbeelden van uit-van-werkingsgebied herinneringen zijn, *geven me een samenvatting van de inzichten van mijn laatste herinnering* en *vatten de hoogtepunten van de lijnvisualisatie samen.*</p></li></ul> |
| **het Verhelderen van vragen** | Als u een vraag stelt die niet genoeg context heeft om Data Insights Agent te beantwoorden, of te algemeen is, beantwoordt Data Insights Agent met een verduidelijkende vraag of voorgestelde opties. <p>De volgende verduidelijkende vragen zijn voorbeelden van aan onderdelen gerelateerde vragen:</p><ul><li>Metrisch: *welke metrische &quot;opbrengst&quot;metrisch u bedoelde?*</li><li>Dimension: *welke van de hieronder &quot;gebieden&quot;wilt u zich op concentreren?*</li><li>Segment: *welk &quot;segment van de Rekening&quot;wilde u toepassen?*</li><li>De Waaier van de datum: *door &quot;vorige maand,&quot;bedoelde u de laatste volledige maand of de laatste 30 dagen?*</li></ul><p>De volgende verduidelijking is een voorbeeld van een vraag die verband houdt met dimensie-elementen:</p> <ul><li>Welke &quot;winkelnaam&quot; bedoelde je? (Bijvoorbeeld Winkel #5274, Winkel #2949, enzovoort.)</li></ul> | Het verduidelijken van vragen is beperkt tot componenten en afmetingspunten. Data Insights Agent kan dingen als gegevensweergaven, visualisaties, granulariteit van gegevens, vergelijking en bereik niet verduidelijken. Wanneer het verduidelijken van vragen niet kan worden gebruikt, blijft de agent aan wat u het meest waarschijnlijk vraagt. Als het een onverwachte visualisatie of gegevensgranulariteit terugkeert, kunt u een vervolgvraag stellen of de visualisatie en de gegevens aanpassen. |
| **verifieerbaarheid en correctheid van Gegevens** | De verifieerbaarheid en de correctheid van gegevens kunnen worden bevestigd door de geproduceerde vrije vormlijst en gegevensvisualisatie te bekijken. <p>Bijvoorbeeld, als u Data Insights Agent vraagt om *de orden van de Trend vorige maand*, kunt u bevestigen dat correcte metrische (&quot;orden&quot;) en datumwaaier (&quot;vorige maand&quot;) in het onlangs geproduceerde paneel, gegevensvisualisatie, en vrije vormlijst werden geselecteerd. | Data Insights Agent reageert niet door u te laten weten welke onderdelen of visualisaties zijn toegevoegd.</p> |
| **mechanismen van de Terugkoppeling** | <ul><li>Stompelen omhoog</li><li>Miniatuur omlaag</li><li>Markering</li></ul> |  |


## Toegang tot Data Insights Agent beheren {#manage-access}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-enable-data-insights-data-view"
>title="Inschakelen voor Data Insights Agent"
>abstract="Deze optie schakelt deze gegevensweergave in voor gebruik met Data Insights Agent. Data Insights Agent is een generatieve AI gespreksagent die van AI Medewerker in Customer Journey Analytics toegankelijk is. Hiermee kunt u snel gegevens analyseren met tekstaanwijzingen. In Analysis Workspace worden relevante visualisaties gemaakt aan de hand van componenten uit uw gegevensweergave en met behulp van uw werkelijke gegevens."

<!-- markdownlint-enable MD034 -->

De volgende parameters regelen de toegang tot Data Insights Agent in Customer Journey Analytics:

* **de toegang van de Oplossing**: Data Insights Agent is beschikbaar voor alle klanten van Customer Journey Analytics als deel van een beperkt toegangsprogramma tot 30 November, 2025. Het is niet beschikbaar in Adobe Analytics.

* **Contractuele toegang**: Als u geen Data Insights Agent in de Medewerker kunt gebruiken AI, gelieve te contacteren de beheerder van uw organisatie of het de rekeningsteam van Adobe. Voordat uw organisatie Data Insights Agent kan gebruiken, moet u akkoord gaan met bepaalde wettelijke voorwaarden die betrekking hebben op generatieve AI.

* **Toestemmingen**: De noodzakelijke toestemmingen moeten in [!UICONTROL Adobe Admin Console] worden verleend alvorens de gebruikers tot Data Insights Agent kunnen toegang hebben.

  Om toestemmingen te verlenen, moet a [&#x200B; admin van het productprofiel &#x200B;](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) de volgende stappen in [!UICONTROL Admin Console] voltooien:
   1. Selecteer in **[!UICONTROL Admin Console]** de tab **[!UICONTROL Products]** om de pagina **[!UICONTROL All products and services]** weer te geven.
   1. Selecteer **[!UICONTROL Customer Journey Analytics]**.
   1. Selecteer op het tabblad **[!UICONTROL Product Profiles]** de titel van het productprofiel waartoe u toegang wilt verlenen aan [!UICONTROL AI Assistant: Product Knowledge] .
   1. Selecteer in het specifieke productprofiel de tab **[!UICONTROL Permissions]** .

      ![&#x200B; het lusje van Toestemmingen in Admin Console &#x200B;](assets/ai-assistant-permissions-tab.png)

   1. In de **[!UICONTROL Reporting Tools]** rij in de verstrekte lijst, uitgezocht geef pictogram uit ![&#x200B; &#x200B;](/help/assets/icons/Edit.svg) uitgeeft.
   1. De rol aan of onderzoek naar **[!UICONTROL AI Assistant: Product Knowledge]**, dan selecteert het plus pictogram ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) naast deze toestemming.
   1. De rol aan of onderzoek naar **[!UICONTROL Data Insights Agent]**, dan selecteert het plus pictogram ![&#x200B; AddCircle &#x200B;](/help/assets/icons/AddCircle.svg) naast deze toestemming.

      De machtiging **[!UICONTROL AI Assistant: Product Knowledge]** en **[!UICONTROL Data Insights Agent]** worden toegevoegd aan de kolom **[!UICONTROL Included permission items]** .

      ![&#x200B; voeg toestemming &#x200B;](assets/ai-assistant-permissions.png) toe.

   1. Selecteer **[!UICONTROL Save]** om de machtigingen op te slaan.

  Voor extra informatie over toegangsbeheer, zie [&#x200B; controle van de Toegang &#x200B;](/help/technotes/access-control.md#access-control).

* **de toegang van de mening van Gegevens**: De meningen van gegevens moeten voor Data Insights Agent worden toegelaten.

  >[!IMPORTANT]
  >
  >Houd rekening met het volgende wanneer u gegevensweergaven inschakelt:
  >* U kunt maximaal 50 gegevensweergaven inschakelen per IMS-organisatie. Als u meer dan 50 gegevensweergaven inschakelt voor alle productprofielen voor een bepaalde organisatie, gebruikt de Data Insights Agent de 50 meest gebruikte gegevensweergaven.
  >* De Data Insights Agent kan verwijzen naar de opgenomen gegevensweergaven op een tijdstip op dezelfde dag dat u ze inschakelt.

  Gegevens weergeven voor Data Insights Agent:

   1. Selecteer in Customer Journey Analytics **[!UICONTROL Data Management]** > **[!UICONTROL Data views]** .

   1. Selecteer een of meer gegevensweergaven die u voor Data Insights Agent wilt inschakelen en selecteer vervolgens **[!UICONTROL Enable for Data Insights Agent]** .

      ![&#x200B; laat gegevensmeningen voor Data Insights Agent &#x200B;](assets/data-view-enable-dia.png) toe

  U kunt als volgt het aantal gegevensweergaven weergeven dat voor Data Insights Agent is ingeschakeld in uw IMS-organisatie:

   1. Selecteer in Customer Journey Analytics **[!UICONTROL Data Management]** > **[!UICONTROL Data views]** .

   1. Selecteer het infopictogram boven aan de kolom **[!UICONTROL Data Insights Agent]** .

      ![&#x200B; Data Insights Agent- infopictogram &#x200B;](assets/data-insights-agent-tooltip.png)

## Data Insights Agent openen in de AI-assistent

1. Ga naar [&#x200B; experience.adobe.com &#x200B;](https://experience.adobe.com/) en login met uw Adobe ID.

2. Selecteer **Customer Journey Analytics** van het Huis van Experience Cloud.

3. Selecteer **[!UICONTROL Blank project]** in de banner bij de bovenkant van de projectpagina om een nieuw leeg project te openen.

4. Zorg ervoor dat de geselecteerde gegevensmening voor het paneel een gegevensmening is die voor gebruik met Data Insights Agent werd toegelaten, zoals die in [&#x200B; wordt beschreven beheert toegang tot Data Insights Agent in Customer Journey Analytics &#x200B;](#manage-access-to-data-insights-agent-in-customer-journey-analytics).

5. Selecteer het AI Assistant-chatpictogram rechtsboven op de pagina.

   Als u het praatjepictogram niet ziet, contacteer uw beheerder zodat kunnen zij de volgende eigenschappen in Admin Conole toelaten:

   * Rapportgereedschappen: **[!UICONTROL AI Assistant: Product Knowledge]**

   * Gereedschappen voor gegevensweergave: **[!UICONTROL Data Insights Agent]**

   Voor extra details, zie [&#x200B; toegang tot Data Insights Agent in Customer Journey Analytics beheren &#x200B;](#manage-access-to-data-insights-agent-in-customer-journey-analytics).

   ![&#x200B; AI Hulp pictogram &#x200B;](/help/assets/ai-asst-icon.png)

6. Stel in het dialoogvenster **[!UICONTROL Ask about Customer Journey Analytics]** onder aan de pagina een vraag over gegevensvisualisatie met Data Insights Agent.

   Zie de volgende voorbeelden voor meer informatie.

### Voorbeeld 1

Stel bijvoorbeeld dat u geïnteresseerd bent in de orders die uw bedrijf in juli heeft ontvangen.

**Herinnering:** ga *&quot;De orden van de Trend in Juli in.&quot;*

![&#x200B; AI herinnering &#x200B;](/help/assets/ai-asst-prompt1.png)

**Reactie:** Data Insights Agent verzamelt inzichten door de gegevens in de gegevensmening, met inbegrip van de metriek en de componenten te bekijken. Het vertaalt de herinnering in de juiste afmetingen en metriek binnen de gegevenswaaier.

Zoals u kunt zien, produceerde het automatisch een lijngrafiek en een vrije lijst om orden voor Juli te tonen.

![&#x200B; Antwoord aan herinnering - lijngrafiek en vrije vormlijst &#x200B;](/help/assets/ai-asst-result.png)

### Voorbeeld 2

Daarna, wilt u zien hoe uw opbrengst per regio vergelijkt.

**Herinnering:** in het snelle venster, ga *&quot;Show opbrengst door gebied in.&quot;*

**Reactie:** Data Insights Agent begrijpt intelligent dat door &quot;gebied,&quot;u &quot;klantengebied&quot;bedoelt.&quot; Het produceert een staafdiagram dat opbrengst door gebied het best toont:

![&#x200B; Grafiek van de Bar &#x200B;](/help/assets/ai-asst-result2.png)

### Voorbeeld 3

Naast het begrip van de opbrengsten per regio, wilt u ook gegevens voor winst per regio zien. In plaats van de vorige vraag te herhalen, kunt u Data Insights Agent vragen om de meest recente visualisatie- en vrije-vormtabel bij te werken.

**Herinnering:** in het snelle venster, type *&quot;voeg winst toe.&quot;*

**Reactie:** De **[!UICONTROL Bar]** grafiek verstrekt nog het meest beknopte antwoord, maar de winst metrische is toegevoegd als kolom in de vrije vormlijst:

![&#x200B; Grafiek van de Bar &#x200B;](/help/assets/ai-asst-result4.png)

### Voorbeeld 4

Tot slot, kijk de opbrengst per productcategorie.

**Herinnering:** in het snelle venster, ga *&quot;Deel van opbrengst door productcategorie in.&quot;*

**Reactie:** opnieuw, neemt Data Insights Agent de meest aangewezen visualisatie, in dit geval de **[!UICONTROL Donut]** visualisatie, aan om de vraag te beantwoorden.

![Cirkeldiagram](/help/assets/ai-asst-result3.png)

## Data Insights Agent openen in Experience Cloud-toepassingen

Adobe Experience Platform Agent Orchestrator biedt u toegang tot de functionaliteit van Data Insights Agent in meerdere Adobe Experience Cloud-toepassingen, zoals Adobe Journey Optimizer en Real-Time CDP.

Agent Orchestrator interpreteert uw verzoek, bepaalt welke gespecialiseerde agenten nodig zijn, en organiseert hen om de juiste reactie te leveren. Het houdt van context over multi-draai interactie bij, zodat kunt u op vroegere vragen natuurlijk voortbouwen.

Voor meer informatie, zie [&#x200B; Adobe Experience Platform Agent Orchestrator &#x200B;](http://www.adobe.com/go/agent-orchestrator-home).

## Voorbeeld van vragen voor gegevensvisualisatie

Hieronder volgen enkele voorbeelden van veelvoorkomende vragen en de visualisaties die Data Insights Agent gebruikt om op deze vragen te reageren.

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

Data Insights Agent verwerkt de context die door elke gebruikersherinnering wordt verstrekt en probeert intelligent met de meest aangewezen visualisatie en de componenten in een vrije vormlijst te antwoorden.

De reacties kunnen variëren afhankelijk van de specifieke woorden en uitdrukkingen die in de herinnering worden gebruikt, en lichte veranderingen in taal kunnen tot verschillende resultaten leiden.

Houd rekening met de volgende richtlijnen om de beste resultaten te bereiken:

* **ben specifiek:** omvat nauwkeurige termijnen om onderaan de reactie te versmallen. Het volgende is een voorbeeld van een specifieke herinnering: &quot;De verkoop van vorige maand in Californië&quot;

* **gebruik duidelijke metriek, dimensies, en segmenten:** Toevoegend specifieke metriek (zoals &quot;Opbrengst&quot;), dimensies (zoals &quot;Websitenaam&quot;), segmenten (zoals &quot;gebruikers van iPhone&quot;), en datumwaaiers (zoals &quot;laatste drie maanden&quot;) helpt Data Insights Agent zich op de juiste gegevens concentreren.

* **stel directe vragen:** het Begrippen van vragen maakt het voor Data Insights Agent direct gemakkelijker om duidelijke, relevante inzichten te verstrekken. Het volgende is een voorbeeld van het stellen van een directe vraag in een vroeg stadium: &quot;Wat is de gemiddelde opbrengst per productcategorie dit jaar?&quot;

Bekijk de volgende voorbeeldlijst van termen en uitdrukkingen die u in herinneringen met Data Insights Agent, samen met de soorten reacties kunt gebruiken u kunt verwachten.

Deze voorbeelden worden ontworpen om u vertrouwd te maken met hoe de specifieke woorden of structuren de output van de Agent van Gegevens kunnen beïnvloeden Insight, die nauwkeurigere en waardevolle inzichten verzekeren. Data Insights Agent gebruikt generatieve AI, zodat de visualisaties of de geselecteerde gegevens door gelijkaardige herinneringen lichtjes kunnen variëren.

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


## Best practices voor configuratie

Hieronder volgen de beste werkwijzen voor uw configuratie van Customer Journey Analytics (gegevensmening, berekende metriek, segmenten, en meer) om ervoor te zorgen dat Data Insights Agent van de correcte componenten kan de plaats bepalen en schonere antwoorden terugkeren zonder u voor extra informatie te moeten vragen.

* **Saldo welke componenten u** nodig hebt. Voeg niet alle gebieden van uw datasets als metriek of afmetingscomponenten aan uw gegevensmening toe. Vooral degenen die u zeker niet zult gebruiken in uw analyse. Anderzijds moet u zich niet strikt beperken tot de velden die u voor uw analyse nodig hebt. Een te beperkte gegevensweergave beperkt de flexibiliteit in de analyse en de Data Insights Agent-functionaliteit.
* **gebruiken altijd vriendschappelijke vertoningsnamen**. Zorg ervoor dat alle velden die u in de gegevensweergave definieert, metrisch of dimensionaal, een vriendelijke componentnaam hebben. Het proces om gebieden met een vriendschappelijke naam anders te noemen is vooral relevant voor gebieden van de gegevensreeksen van de de bronschakelaar van Adobe Analytics. Deze velden hebben vaak niet-vriendelijke, niet-identificeerbare namen, zoals `eVar41` of `prop25` .
* **Gebruik onderscheidende namen**. Afzonderlijke namen zijn vooral relevant wanneer u hetzelfde veld gebruikt als een metrische en een dimensie-component in de gegevensweergave. Of wanneer u een veld gebruikt in meerdere componenten van hetzelfde type (bijvoorbeeld in twee verschillende metriek), elk met verschillende componentinstellingen.
* **Gebruik een component noemend overeenkomst**. U kunt een component gebruiken noemend overeenkomst om componenten te groeperen. **[!UICONTROL Orders | Product]** en **[!UICONTROL Orders | Customer]** kunnen bijvoorbeeld onderscheid maken tussen verschillende volgordemetriek die mogelijk in uw gegevens voorkomen.
* **Gebruik het Woordenboek van Gegevens**. Voeg een beschrijving en andere relevante gegevens voor componenten in het gegevenswoordenboek toe. De Insight Agent van Gegevens gebruikt momenteel geen beschrijving en markeringen van het Woordenboek van Gegevens, maar het zou in de toekomst kunnen.
* **Gebruik goedgekeurde berekende metriek**. Ga akkoord met een proces waarbij alleen goedgekeurde berekende metriek als componenten in de gegevensweergave worden gebruikt en gebruik geen experimentele berekende metriek.
* **Deel vereiste segmenten**. Zorg ervoor dat u segmenten deelt en dat segmenten zichtbaar zijn die vereist zijn voor Data Insights Agent-aanwijzingen.
* **normaliseert op componentennamen over gegevensmeningen**. Als u dezelfde velden als een component gebruikt in meerdere gegevensweergaven, moet u ervoor zorgen dat u één vriendelijke naam en één id voor die component gebruikt. Met één naam en id kan de Data Insights Agent wisselen tussen gegevensweergaven zonder context te verliezen.

>[!MORELIKETHIS]
>
>[&#x200B; montages van de Component &#x200B;](/help/data-views/component-settings/overview.md)
>&#x200B;>[Gegevenswoordenboek &#x200B;](/help/components/data-dictionary/data-dictionary-overview.md)
>&#x200B;>[Berekende metrische waarde goedkeuren &#x200B;](/help/components/calc-metrics/cm-workflow/cm-approving.md)
>&#x200B;>[Segmenten delen &#x200B;](/help/components/segments/seg-share.md)
>
