---
description: Hoe te om de vragen van de gegevensanalyse van de documentatie van de Customer Journey Analytics te stellen
title: AI-assistent voor gegevensanalyse in Customer Journey Analytics
role: User, Admin
solution: Customer Journey Analytics
hidefromtoc: true
hide: true
source-git-commit: e18d8facbd54ae65d158ce2c72f47709ef988f8f
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 0%

---


# AI-assistent voor gegevensanalyse in Customer Journey Analytics - Alpha

De Medewerker van AI van de Analyse van Gegevens is een intelligente, context-bewuste gespreksagent die u kan helpen sneller en efficiënt vragen beantwoorden u van uw gegevens van Analysis Workspace in Customer Journey Analytics kunt hebben.

De Medewerker kijkt door alle gegevens in een gegevensmening, met inbegrip van de verschillende soorten metriek en componenten, en vertaalt uw herinnering in de juiste afmeting, metrisch, en datumwaaier voor deze analyse. In plaats van vertrouwd te moeten zijn met de componenten van de gegevensmening, en dan die componenten te slepen en te laten vallen in de beste combinatie om uw vraag te beantwoorden, kunt u de vraag eenvoudig typen in de Medewerker AI.

## Functies binnen bereik versus functies buiten bereik voor de versie van de Alpha

### Functies binnen bereik

| Ondersteunde functie | Beschrijving |
| --- | --- |
| **bouwt en werkt visualisaties** bij | Hiermee genereert u een vrije-vormtabel en de bijbehorende visualisatie (bijvoorbeeld lijn, balk, donut, enz.).<p>Voorbeeld: *wat is de winst over SKUs van Februari aan Mei?* |
| **Ondersteunde visualisatietypen** | <ul><li>Lijn</li><li>Meerdere regels</li><li>Vrije vorm</li><li>Balk</li><li>Donut</li><li>Samenvattingsnummer</li></ul> |
| **uit-van-werkingsgebied snelle opsporing** | Als u een herinnering voorlegt die buiten werkingsgebied, zoals &quot;uitvoert dit project&quot;is, antwoordt de Medewerker door u te laten weten dat de vraag buiten werkingsgebied is. |
| **het Verhelderen van vragen** | Als u een vraag stelt die niet genoeg context voor de Medewerker AI heeft om te antwoorden, of te algemeen is, antwoordt de Medewerker AI met een het verduidelijken vraag en/of voorgestelde opties. Voorbeelden: <p>**Onderdelen**<ul><li>Metrisch: *welke metrische &quot;opbrengst&quot;metrisch u bedoelde?*</li><li>Dimension: *welke van hieronder &quot;gebieden&quot;wilt u zich op concentreren?*</li><li>Filter: *Welke &quot;filter van de Rekening&quot;wilde u toepassen?*</li><li>De Waaier van de datum: *door &quot;vorige maand&quot;, bedoelde u de laatste volledige maand of de laatste 30 dagen?*</li></ul>**punten van het Dimension**: Welke &quot;opslagnaam&quot;bedoelde u? (bijvoorbeeld Winkel #5274, Winkel #2949, enz.) |
| **Multi-draai** | De AI-assistent reageert op een vraag met de context van de eerdere vraag(en), zodat gebruikers de visualisaties kunnen bijwerken en vervolgvragen kunnen stellen. Voorbeeld: *toon me in plaats daarvan de gegevens van Maart aan April.* |
| **Terugkoppeling** | <ul><li>Stompelen omhoog</li><li>Miniatuur omlaag</li><li>Markering</li></ul> |

### Functies buiten bereik

| Niet-ondersteunde functie | Beschrijving |
| --- | --- |
| **overzicht of reactie van binnen-lijn** | De AI-assistent kan niet online reageren in de chatrail met een beknopt antwoord van een gebruiker prompt.Voorbeeld van aanwijzingen die buiten het bereik vallen:<ul><li>*geef me een samenvatting van de inzichten van mijn laatste herinnering.*</li><li>*vat de hoogtepunten van de lijnvisualisatie samen.*</li></ul> |
| **het Verhelderen van vragen** | Het verduidelijken van vragen is beperkt tot componenten en afmetingspunten. De AI-assistent kan geen duidelijkheid verschaffen over gegevensweergaven, visualisaties, granulariteit van gegevens, vergelijking, bereik, enzovoort. Zonder vragen te verduidelijken, blijft de Medewerker aan wat u het meest waarschijnlijk vraagt. Als het een onverwachte visualisatie of gegevensgranulariteit terugkeert, kunt u het multi-draai/updatemogelijkheid dan gebruiken om de visualisatie en de gegevens aan te passen. |
| **de Acties van Workspace / Mogelijkheden** | De AI-assistent kan geen actie ondernemen voor een gebruiker in Workspace, behalve het maken en bijwerken van visualisaties. Het kan bijvoorbeeld het volgende niet doen:<ul><li>Contextafhankelijke knoppen voor handelingen (toevoegen aan diagram, nieuw deelvenster, nieuwe tabel)</li><li>Delen</li><li>Exporteren</li><li>Downloaden</li><li>Gebruikersvoorkeuren beheren</li><li>Curate</li><li>Gegevensweergave beheren</li><li>Analytische dashboards-app</li><li>Attributie</li></ul> |
| **Niet gestaafde visualisatietypen** | <ul><li>Stroom</li><li>Fallout</li><li>Cohortabel</li><li>Gebied, gebied gestapeld</li><li>Stapel gestapeld</li><li>Opsommingsteken</li><li>Combo</li><li>Histogram</li><li>Horizontale balk, horizontale balk gestapeld</li><li>Hoofdmetrische samenvatting</li><li>Spreiding</li><li>Samenvattingswijziging</li><li>Tekst</li><li>Treemap</li><li>Venn</li></ul> |
| **Verklaringsbaarheid en Verifiability** | Transparante beschrijving of citaat voor hoe de Medewerker AI een reactie produceerde, en die u van een manier voorzien om te bevestigen dat het antwoord correct is. |

## Toegang tot functies in de gebruikersinterface van de Customer Journey Analytics

[ hebben wij zelfs deze sectie voor de Alpha nodig?]

De volgende parameters regelen de toegang tot de Hulpeigenschap van de Analyse AI van Gegevens:

* **de toegang van de Oplossing**: De Medewerker van de Analyse AI van Gegevens is beschikbaar voor de Eerste en Uiteindelijke klanten van de Customer Journey Analytics. Het is niet beschikbaar in Adobe Analytics.

Het is ook beschikbaar in Adobe Experience Platform, Adobe Journey Optimizer, Adobe Real-Time CDP en aanvullende Experience Platform-apps.

* **Contractuele toegang**: Als u geen Medewerker kunt gebruiken AI, gelieve te contacteren de beheerder of de Vertegenwoordiger van de Rekening van de Adobe van uw organisatie. Voordat uw organisatie Data Analysis AI Assistant kan gebruiken, moet u akkoord gaan met bepaalde juridische voorwaarden die betrekking hebben op GenAI.

* **Toestemmingen**: In [!UICONTROL Adobe Admin Console], bepaalt de [!UICONTROL Reporting Tools] **[!UICONTROL AI Assistant: Data Analysis]** toestemming toegang tot dit hulpmiddel. Admin van het a [ productprofiel ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) moet deze stappen in [!UICONTROL Admin Console] volgen:
   1. Ga naar **[!UICONTROL Admin Console]** > **[!UICONTROL Products and services]** > **[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Product Profiles]**
   1. Selecteer de titel van het productprofiel waartoe u toegang wilt verlenen aan [!UICONTROL AI Assistant: Product Knowledge] .
   1. Selecteer **[!UICONTROL Permissions]** in het specifieke productprofiel.
   1. Selecteer ![ uitgeven ](/help/assets/icons/Edit.svg) om uit te geven **[!UICONTROL Reporting Tools]**.
   1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) om **Medewerker AI toe te voegen: De Analyse van gegevens** aan **[!UICONTROL Included permission items]**.

      ![ voeg toestemming ](assets/ai-assistant-permissions.png) toe.

   1. Selecteer **[!UICONTROL Save]** om de machtigingen op te slaan.

Zie [ controle van de Toegang ](/help/technotes/access-control.md#access-control) voor meer informatie.

## Toegang tot en gebruik Data Analysis AI Assistant

1. Ga naar deze koppeling om Workspace te openen in de Labs IMS Org (in het werkgebied) en u aan te melden bij uw Adobe ID.

1. Klik op **[!UICONTROL Blank project]** in de banner boven aan de projectpagina om een nieuw, leeg project te openen.

1. Klik op het AI Assistant-chatpictogram rechtsboven.

   ![ AI Hulp pictogram ](/help/assets/ai-asst-icon.png)

1. Stel in het dialoogvenster **[!UICONTROL Ask about Customer Journey Analytics]** onderaan een vraag over gegevensanalyse in de AI-assistent.

### Voorbeeld 1

Stel bijvoorbeeld dat u geïnteresseerd bent in de orders die uw bedrijf in juli heeft ontvangen.

1. Voer &quot;Bestellingen tonen in juli&quot; in.

   ![ AI herinnering ](/help/assets/ai-asst-prompt1.png)

1. De AI-assistent verzamelt nu inzichten door de gegevens in de gegevensweergave te bekijken, inclusief de meetgegevens en componenten. Het vertaalt de herinnering in de juiste afmeting/s, metrisch/s, en gegevenswaaier.

   Zoals u kunt zien, heeft het automatisch een grafiek van de Lijn en een vrije lijst geproduceerd die orden voor Juli tonen.

   ![ Antwoord aan herinnering - lijngrafiek en vrije vormlijst ](/help/assets/ai-asst-result.png)

### Voorbeeld 2

Daarna, wilt u zien hoe uw opbrengst per regio vergelijkt.

1. In het snelle venster, ga &quot;Show opbrengst door gebied in.&quot;

2. AI is slim genoeg om te begrijpen dat door &quot;gebied&quot;, u &quot;klantengebied&quot;bedoelt. Het produceert een staafdiagram dat opbrengst door gebied het best toont:

   ![ Grafiek van de Bar ](/help/assets/ai-asst-result2.png)

### Voorbeeld 3

Laten we nu eens kijken naar de inkomsten per productcategorie.

1. In het snelle venster, ga &quot;de opbrengsten van de Show door productcategorie&quot; in.

2. De AI-assistent voor gegevensanalyse gebruikt opnieuw de meest geschikte visualisatie, in dit geval de **[!UICONTROL Donut]** visualisatie, om de vraag te beantwoorden.

   ![Cirkeldiagram](/help/assets/ai-asst-result3.png)

### Voorbeeld 4

Tot slot wilt u weten welke SKU het meest rendabel is, en waar u marketing middelen zou moeten investeren.

1. In het snelle venster, vraag &quot;wat is de winst over SKUs van Februari aan Mei.&quot;

1. Een eenvoudige **[!UICONTROL Bar]** -grafiek geeft het meest beknopte antwoord:

   ![ Grafiek van de Bar ](/help/assets/ai-asst-result4.png)

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

TBD

## Alpha testverwachtingen en gevraagde feedback

Na het stellen van elke vraag, herzie zorgvuldig het verstrekte antwoord van de medewerker. Het is cruciaal om de gegenereerde visualisaties uitgebreid te evalueren voordat u feedback geeft.

Evalueer het antwoord: wordt het juiste antwoord gegeven?

Als de assistent reageert in de chat rail: evalueer de tekstuele reactie.

* Als een visualisatie/grafiek wordt getoond: evalueer de visualisatie. Is het de aangewezen/verwachte visualisatie voor uw vraag?

* Als een vrije-vormlijst wordt getoond: evalueer de vrije vormlijst. Zijn de gegevens van de vrije-vormlijst correct? Is het opsplitsen van gegevens op verzoek? Zijn de toegepaste filters die u vroeg of verwachtte?

* Als er een algemeen foutbericht wordt weergegeven waarin wordt aangegeven dat de vraag buiten het bereik valt, geeft u feedback over de vraag of het bericht buiten het bereik juist is wanneer u hierom wordt gevraagd. Was uw vraag eigenlijk binnen het bereik?

Geef voor elke reactie een duim omhoog of omlaag op basis van de respons

Na de duimen omhoog/omlaag selectie, gelieve een selectie voor de relevante multi-uitgezochte doos terugkoppelt. Als u aanvullende feedback wilt geven, voegt u notities toe in het geopende tekstvak.

## Vragen en contact

E-mail `taylorb@adobe.com` (PM)
Vragen en feedback verzenden op de slack channel van de Alpha: #aep-cja-ai-assistent-testers???


