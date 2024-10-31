---
description: Hoe te om de vragen van de gegevensanalyse van de documentatie van de Customer Journey Analytics te stellen
title: AI-assistent voor gegevensanalyse in Customer Journey Analytics
role: User, Admin
solution: Customer Journey Analytics
hidefromtoc: true
hide: true
source-git-commit: 1442aa9be5e6a6dc283ba559a2ff6c46de862425
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---


# AI-assistent voor gegevensanalyse in Customer Journey Analytics - Alpha

De Medewerker van AI van de Analyse van Gegevens is een intelligente, context-bewuste gespreksagent die u kan helpen sneller en efficiënt vragen beantwoorden u van uw gegevens van Analysis Workspace in Customer Journey Analytics kunt hebben.

De Medewerker kijkt door alle gegevens in een gegevensmening, met inbegrip van de verschillende soorten metriek en componenten, en vertaalt uw herinnering in de juiste afmeting, metrisch, en datumwaaier voor deze analyse. In plaats van vertrouwd te moeten zijn met de componenten van de gegevensmening, en dan die componenten te slepen en te laten vallen in de beste combinatie om uw vraag te beantwoorden, kunt u de vraag eenvoudig typen in de Medewerker AI.

## Functies binnen bereik versus functies buiten bereik voor de versie van de Alpha

Functies binnen bereik:

| Ondersteunde functie | Beschrijving |
| --- | --- |
| Visualisaties maken en bijwerken | Hiermee genereert u een vrije-vormtabel en de bijbehorende visualisatie (bijvoorbeeld lijn, balk, donut, enz.).<p>Voorbeeld: *wat is de winst over SKUs van Februari aan Mei?* |
| Ondersteunde visualisatietypen | Lijnen, Meerdere regels, Vrije vorm, Staaf, Donut, Summiere nummervisualisaties |
| Snelle detectie buiten bereik | Als u een herinnering voorlegt die buiten werkingsgebied, zoals &quot;uitvoert dit project&quot;is, antwoordt de Medewerker door u te laten weten dat de vraag buiten werkingsgebied is. |
| Vragen verduidelijken | Als u een vraag stelt die niet genoeg context voor de Medewerker AI heeft om te antwoorden, of te algemeen is, antwoordt de Medewerker AI met een het verduidelijken vraag en/of voorgestelde opties. Voorbeelden: <p>**Onderdelen**<ul><li>Metrisch: *welke metrische &quot;opbrengst&quot;metrisch u bedoelde?*</li><li>Dimension: *welke van hieronder &quot;gebieden&quot;wilt u zich op concentreren?*</li><li>Filter: *Welke &quot;filter van de Rekening&quot;wilde u toepassen?*</li><li>De Waaier van de datum: *door &quot;vorige maand&quot;, bedoelde u de laatste volledige maand of de laatste 30 dagen?*</li></ul>**punten van het Dimension**: Welke &quot;opslagnaam&quot;bedoelde u? (bijvoorbeeld Winkel #5274, Winkel #2949, enz.) |
| Meervoudig draaien | De AI-assistent reageert op een vraag met de context van de eerdere vraag(en), zodat gebruikers de visualisaties kunnen bijwerken en vervolgvragen kunnen stellen. Voorbeeld: *toon me in plaats daarvan de gegevens van Maart aan April.* |
| Feedback | <ul><li>Stompelen omhoog</li><li>Miniatuur omlaag</li><li>Markering</li></ul> |

Functies buiten bereik:

| Niet-ondersteunde functie | Beschrijving |
| --- | --- |
| Samenvatting of reactie online | De AI-assistent kan niet online reageren in de chatrail met een beknopt antwoord van een gebruiker prompt.Voorbeeld van aanwijzingen die buiten het bereik vallen:<ul><li>*geef me een samenvatting van de inzichten van mijn laatste herinnering.*</li><li>*vat de hoogtepunten van de lijnvisualisatie samen.*</li></ul> |
| Vragen verduidelijken | Het verduidelijken van vragen is beperkt tot componenten en afmetingspunten. De AI-assistent kan geen duidelijkheid verschaffen over gegevensweergaven, visualisaties, granulariteit van gegevens, vergelijking, bereik, enzovoort. Zonder vragen te verduidelijken, blijft de Medewerker aan wat de gebruiker het meest waarschijnlijk vraagt. Als het een onverwachte visualisatie of gegevensgranulariteit terugkeert, kan de gebruiker dan de multi-draai/updatemogelijkheid gebruiken om de visualisatie en de gegevens aan te passen. |
| Workspace-acties/mogelijkheden | De AI-assistent kan geen actie ondernemen voor een gebruiker in Workspace, behalve het maken en bijwerken van visualisaties. Het kan bijvoorbeeld het volgende niet doen:<ul><li>Contextafhankelijke knoppen voor handelingen (toevoegen aan diagram, nieuw deelvenster, nieuwe tabel)</li><li>Delen</li><li>Exporteren</li><li>Downloaden</li><li>Gebruikersvoorkeuren beheren</li><li>Curate</li><li>Gegevensweergave beheren</li><li>Analytische dashboards-app</li><li>Attributie</li></ul> |
| Niet-ondersteunde visualisatietypen | <ul><li>Stroom</li><li>Fallout</li><li>Cohortabel</li><li>Gebied, gebied gestapeld</li><li>Stapel gestapeld</li><li>Opsommingsteken</li><li>Combo</li><li>Histogram</li><li>Horizontale balk, horizontale balk gestapeld</li><li>Hoofdmetrische samenvatting</li><li>Spreiding</li><li>Samenvattingswijziging</li><li>Tekst</li><li>Treemap</li><li>Venn</li></ul> |
| Uitleg en controleerbaarheid | Transparante beschrijving of citaat voor hoe de Medewerker AI een reactie produceerde, en die u van een manier voorzien om te bevestigen dat het antwoord correct is. |

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

## AI-assistent voor gegevensanalyse openen




## AI-assistent voor gegevensanalyse gebruiken

1. Navigeer in Customer Journey Analytics naar de geleverde sandbox.

1. Open een Workspace-project.


## Voorbeeldgegevens, aanwijzingen voor analyse

Hier zijn een paar voorbeelden van hoe de AI Assistent op herinneringen, en de verwachte visualisaties antwoordt:



## Aankondiging van aanbevolen procedures

TBD

## Alpha testverwachtingen en gevraagde feedback

TB D

## Vragen en contact

E-mail `taylorb@adobe.com` (PM)
Vragen en feedback verzenden via het zwarte kanaal van de Alpha




