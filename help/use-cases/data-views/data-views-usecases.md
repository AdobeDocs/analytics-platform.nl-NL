---
title: Gebruik gevallen voor gegevensweergaven in Customer Journey Analytics
description: Meerdere gebruiksgevallen die de flexibiliteit en kracht van gegevensweergaven in Customer Journey Analytics tonen
exl-id: 6ecbae45-9add-4554-8d83-b06ad016fea9
solution: Customer Journey Analytics
feature: Data Views
role: User
source-git-commit: 629935d66b0f2c5731806a68cc2fcda5fb11fc9a
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 0%

---

# Gebruiksscenario&#39;s voor gegevensweergaven

Deze gebruiksgevallen illustreren de flexibiliteit en kracht van gegevensweergaven in Customer Journey Analytics.

## Metingen voor bindingsafmetingen gebruiken

Zie het [ bindende metriek van het Gebruik ](binding-dimensions-metrics.md) gebruiksgeval voor meer details.

## Samenvattingsgegevens gebruiken

Zie het [ summiere gegevens van het Gebruik ](summary-data.md) gebruiksgeval voor meer details.

## Gebruikskwesties voor extensie BI

Zie de [ BI uitbreidingsgebruiksgevallen ](bi-extension-usecases.md) op hoe te om een aantal gebruiksgevallen te verwezenlijken gebruikend de uitbreiding van Customer Journey Analytics BI.

## Een metrische waarde maken op basis van een tekenreeksschemaveld {#string}

Wanneer u bijvoorbeeld een gegevensweergave maakt, kunt u een [!UICONTROL Orders] -metrische waarde maken vanuit een [!UICONTROL Page Title] -schemaveld dat een tekenreeks is.



1. Sleep op de tab **[!UICONTROL Components]** de **[!UICONTROL Page Title]** naar de sectie **[!UICONTROL Metrics]** onder [!UICONTROL Included components] .
1. Markeer de metrische waarde waarin u net hebt gesleept en wijzig de naam in `Orders` in de lus **[!UICONTROL Component Settings]** on
1. Open de sectie **[!UICONTROL Include/Exclude Values]** en geef de volgende instellingen op:
   1. Schakel **[!UICONTROL Set include exclude values]** in.
   1. Selecteer **[!UICONTROL If all criteria are met]** in **[!UICONTROL Match]** .
   1. Geef `confirmation` op. Deze tekst voor page_title wijst erop dat deze pagina met het plaatsen van een orde verwant is. Nadat u alle paginatitels hebt gecontroleerd waaraan aan deze criteria is voldaan, wordt voor elke instantie een `1` geteld. Het resultaat is een nieuwe metrische (geen berekende metrisch.) Metrisch die inbegrepen/uitgesloten waarden heeft kan overal worden gebruikt om het even welke andere metrisch kan worden gebruikt. Het werkt met Attribution IQ, filters, en overal anders kunt u standaardmetriek gebruiken.

   ![ Dimension aan metrisch ](../assets/string-to-metric.gif) {width=100%}
1. U kunt een attributiemodel voor deze metrische waarde, zoals [!UICONTROL Last Touch] , verder opgeven met een [!UICONTROL Lookback window] van [!UICONTROL Session] .
U kunt ook een andere [!UICONTROL Orders] -metrische waarde maken vanuit hetzelfde veld en een ander attributiemodel opgeven. Bijvoorbeeld [!UICONTROL First Touch] en een andere [!UICONTROL Lookback window] , zoals [!UICONTROL 30 days] .

Een ander voorbeeld zou identiteitskaart van de Persoon, een dimensie, als metrisch moeten gebruiken om te bepalen hoeveel Persoon IDs uw bedrijf heeft.

## Gehele getallen gebruiken als afmetingen {#integers}

Eerder, zouden gehelen automatisch als metriek in Customer Journey Analytics worden behandeld. Cijfers (inclusief aangepaste gebeurtenissen uit Adobe Analytics) kunnen nu als afmetingen worden beschouwd. Hier volgt een voorbeeld:



1. Sleep het gehele getal **[!UICONTROL Duration]** naar de sectie **[!UICONTROL Dimensions]** onder [!UICONTROL Included Components] :
1. U kunt nu **[!UICONTROL Value Bucketing]** toevoegen om deze dimensie op een gekorte manier in de rapportage te presenteren. Zonder boekingen, zou elk geval van deze dimensie als lijnpunt in Workspace rapportering verschijnen.
   ![ Geheel Geheel aan afmeting ](../assets/integer-to-dimension.gif) {width=100%}


## Numerieke afmetingen gebruiken als meetwaarden in stroomdiagrammen {#numeric}

U kunt een numerieke dimensie gebruiken om meetgegevens in uw [!UICONTROL  Flow] visualisatie te krijgen.

1. Voor de Mening van Gegevens [ Componenten ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview) tabel, sleep het [!UICONTROL Marketing Channels] schemagebied in het [!UICONTROL Metrics] gebied onder [!UICONTROL Included components].
2. In Workspace-rapportering toont deze flow [!UICONTROL Marketing Channels] die doorloopt in [!UICONTROL Orders] :

![ de stroom van het Kanaal van de Marketing van e-mail aan uitgang/orden.](../assets/flow.png)

## Filteren van subgebeurtenissen uitvoeren {#sub-event}

Deze mogelijkheid is specifiek van toepassing op arrayvelden. Met de functionaliteit include/exclude kunt u filteren op het niveau van de subgebeurtenis, terwijl filters (segmenten) die in de filterbuilder zijn ingebouwd, u alleen filteren op het niveau van de gebeurtenis geven. Zo, kunt u subevent filtreren door te gebruiken omvat/sluit in de meningen van Gegevens, en dan die nieuwe metrische dimensie in een filter op het gebeurtenisniveau van verwijzingen te voorzien.

Gebruik bijvoorbeeld de functie voor het opnemen/uitsluiten van gegevens in de gegevensweergaven om alleen de nadruk te leggen op producten die verkopen van meer dan € 50 hebben gegenereerd. Dus als u een bestelling hebt die een productaankoop van 50 dollar en een productaankoop van 25 dollar bevat, verwijdert de functie voor het opnemen/uitsluiten de productaankoop van 25 dollar, niet de volledige bestelling.

1. Voor de Mening van Gegevens [ Componenten ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview) tabel, sleep het **[!UICONTROL Revenue]** schemagebied in het **[!UICONTROL Metrics]** gebied onder [!UICONTROL Included components].
1. Selecteer metrisch en vorm het volgende op de rechterkant:
a. Selecteer onder **[!UICONTROL Format]** **[!UICONTROL Currency]** .
b. Selecteer onder **[!UICONTROL Currency]** **[!UICONTROL USD]** .
c. Selecteer onder **[!UICONTROL Include/Exclude Values]** het selectievakje naast **[!UICONTROL Set include/exclude values]** .
d. Selecteer onder **[!UICONTROL Match]** de optie **[!UICONTROL If all criteria are met]** .
e. Selecteer onder **[!UICONTROL Criteria]** **[!UICONTROL is greater than or equal]** .
f. Geef `50` op als waarde.

Met deze nieuwe instellingen kunt u alleen inkomsten met een hoge waarde bekijken en alles onder $50 filteren.

## De instelling [!UICONTROL No value options] gebruiken {#no-value}

Uw bedrijf heeft mogelijk tijd besteed aan het trainen van uw gebruikers om &quot;Niet gespecificeerd&quot;voor dimensies in rapporten te verwachten. De standaardwaarde voor afmetingen in gegevensweergaven is &quot;Geen waarde&quot;. U kunt echter per dimensie opgeven hoe geen waarde moet worden gerapporteerd. Zie de No value opties voor een afmetingscomponent.

![ Geen waardeopties ](../assets/no-value-options.gif) {width=100%}


## Meerdere metriek met verschillende attributie-instellingen maken {#attribution}

Gebruik de functie **[!UICONTROL Duplicate]** rechtsboven om een aantal metrische gegevens voor totale omzet te maken met verschillende toewijzingsinstellingen, zoals **[!UICONTROL First Touch]** , **[!UICONTROL Last Touch]** en **[!UICONTROL Algorithmic]** .

Vergeet niet elke metrische naam te wijzigen om de verschillen te weerspiegelen, zoals `Total Revenue (Algorithmic)`

![ Dupliceer metrisch voor verschillende attributie montages ](../assets/duplicate-metric-for-attribution.gif) {width=100%}

Voor meer informatie over andere montages van gegevensmeningen, zie [ gegevensmeningen ](/help/data-views/create-dataview.md) creëren.
Voor een conceptueel overzicht van gegevensmeningen, zie [ overzicht van de meningen van Gegevens ](/help/data-views/data-views.md).

## Nieuwe sessie- en retoursessierapport {#new-repeat}

U kunt bepalen of een zitting inderdaad de eerste-ooit zitting voor een gebruiker of een terugkeerzitting is. Gebaseerd op het rapporteringsvenster dat u voor deze gegevensmening en een 13 maanden raadplegingsvenster bepaalde. Met deze rapportage kunt u bijvoorbeeld bepalen:

* Welk percentage van uw bestellingen komt uit nieuwe of terugkeerzittingen?

* Voor een bepaald marketingkanaal, of een specifieke campagne, richt u zich op nieuwe gebruikers of terugkeergebruikers? Hoe beïnvloedt deze keuze de omrekeningskoersen?

Eén dimensie en twee metriek vereenvoudigen deze rapportage:

* [ Type van Zitting ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-reference) - deze afmeting heeft twee waarden: [!UICONTROL New] en [!UICONTROL Returning]. Het [!UICONTROL New] lijstitem omvat al gedrag (namelijk metriek tegen deze dimensie) van een zitting die als bepaalde eerste zitting van een persoon is bepaald. Alle andere elementen worden opgenomen in het regelitem [!UICONTROL Returning] (ervan uitgaande dat alles tot een sessie behoort). Wanneer metriek geen deel uitmaken van een sessie, vallen ze voor deze dimensie in het emmertje &quot;Niet van toepassing&quot;.

* [ Eerste-tijdzittingen ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-reference). De metrische waarde van Eerste sessies wordt gedefinieerd als de eerste sessie van een persoon die binnen het rapportagevenster is gedefinieerd.

* [ de zittingen van de Terugkeer ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-reference) Metrische de zittingen van de Terugkeer is het aantal zittingen die geen eerste-tijdzitting van een persoon waren.—>

De volgende onderdelen openen:

1. Ga in de redacteur van de gegevensmening.
1. Selecteer de tab **[!UICONTROL Components]** en selecteer vervolgens **[!UICONTROL Standard components]** in de linkertrack.
1. Sleep de componenten **[!UICONTROL Session type]** , **[!UICONTROL First-time Sessions]** en **[!UICONTROL Return Sessions]** naar de gegevensweergave.

Nieuwe sessies worden bijna altijd correct gerapporteerd. De enige uitzonderingen zijn:

* Wanneer een eerste zitting vóór het 13 maanden raadplegingsvenster voorkwam. <br/> Deze zitting wordt genegeerd.

* Wanneer een sessie zowel het terugzoekvenster als het rapportagevenster omvat. <br/> bijvoorbeeld, stelt u een rapport van 1 Juni aan 15 Juni, 2022 in werking. Het terugkijkvenster zou zich van 1 mei 2021 tot 31 mei 2022 uitstrekken. Als een sessie op 30 mei 2022 begint en op 1 juni 2022 eindigt, wordt de sessie opgenomen in het terugzoekvenster. En alle sessies in het rapportagevenster worden als retoursessies geteld.

## De functionaliteit Datum en tijd gebruiken {#date}

Schema&#39;s in Adobe Experience Platform bevatten [!UICONTROL Date] - en [!UICONTROL Date-Time] -velden. De weergave Gegevens van Customers Journey Analytics ondersteunt deze velden nu. Wanneer u deze gebieden in een gegevensmening als afmeting sleept, kunt u hun [ formaat ](/help/data-views/component-settings/format.md) specificeren. Deze notatie bepaalt hoe de velden worden weergegeven in de rapportage. Bijvoorbeeld:

* Als u voor de datumnotatie **[!UICONTROL Day]** met de notatie **[!UICONTROL Month, Day, Year]** selecteert, ziet een voorbeelduitvoer in de rapportage er als volgt uit: 23 augustus 2022.

* Als u voor de datum-tijdnotatie **[!UICONTROL Minute of Day]** met de notatie **[!UICONTROL Hour:Minute]** selecteert, kan de uitvoer er als volgt uitzien: 20:20.

De data na 1 Jan, 1900 (met de enige uitzondering van 1 Jan, 1970) en datum-tijd waarden na 1 Jan, 2000 00 :00: 00 worden gesteund.

### Datum- en datumnotatiefalen

* Datum: Een reismaatschappij verzamelt de vertrekdatum voor reizen als een veld in de gegevens. Het bedrijf wil graag een rapport hebben waarin de [!UICONTROL Day of Week] voor alle vertrekdatums wordt vergeleken om te begrijpen wat het populairst is. Het bedrijf zou hetzelfde willen doen voor de [!UICONTROL Month of Year] .

* Datum/tijd: een detailhandelsmaatschappij int de tijd voor elk van hun aankopen in-store verkooppunt (POS). Over een bepaalde maand wil het bedrijf graag de drukste boodschappenperioden van [!UICONTROL Hour of Day] begrijpen.

>[!MORELIKETHIS]
>
>[ Datum en datum-Tijd in de component die van het Formaat ](/help/data-views/component-settings/format.md) plaatsen
>

