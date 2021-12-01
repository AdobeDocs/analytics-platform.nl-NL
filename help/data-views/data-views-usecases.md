---
title: Gebruik gevallen voor gegevensweergaven in Customer Journey Analytics
description: Meerdere gebruiksgevallen die de flexibiliteit en kracht van gegevensweergaven in Customer Journey Analytics tonen
exl-id: 6ecbae45-9add-4554-8d83-b06ad016fea9
solution: Customer Journey Analytics
source-git-commit: faaf3d19ed37019ba284b41420628750cdb413b8
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Gebruiksscenario&#39;s voor gegevensweergaven

Deze gebruiksgevallen tonen de flexibiliteit en kracht van gegevensweergaven in Customer Journey Analytics.

## 1. Een metrische waarde maken op basis van een tekenreeksschemaveld

Wanneer u bijvoorbeeld een gegevensweergave maakt, kunt u een [!UICONTROL Orders] metrisch van een [!UICONTROL pageTitle] schemaveld dat een tekenreeks is. Hier volgen de volgende stappen:

1. Sleep op het tabblad Componenten de knop [!UICONTROL pageTitle] in de [!UICONTROL Metrics] deel onder [!UICONTROL Included Components].
   ![](assets/use-case1a.png)
1. Markeer nu de metrische waarde die u net hebt gesleept en wijzig de naam hiervan [!UICONTROL Component Settings] rechts:
   ![](assets/orders.png)
1. Open de [!UICONTROL Include/Exclude Values] aan de rechterkant en geef het volgende op:
   ![](assets/orders2.png)

   De uitdrukking &quot;bevestiging&quot;wijst erop dat dit een orde is. Na het controleren van alle paginatitels waar aan die criteria wordt voldaan, zal &quot;1&quot;voor elke instantie worden geteld. Het resultaat is nieuw metrisch (niet berekend metrisch.) Een metrisch die inbegrepen/uitgesloten waarden heeft kan overal worden gebruikt andere metrisch. Het werkt met Attribution IQ, filters, en overal anders kunt u standaardmetriek gebruiken.
1. U kunt een attributiemodel voor deze metrische waarde verder opgeven, zoals [!UICONTROL Last Touch], met een [!UICONTROL Lookback window] van [!UICONTROL Session].
U kunt ook een andere [!UICONTROL Orders] metrisch van het zelfde gebied en specificeer een verschillend attributiemodel voor het, zoals [!UICONTROL First Touch]en een andere [!UICONTROL Lookback window], zoals [!UICONTROL 30 days].

Een ander voorbeeld zou de identiteitskaart van de Bezoeker, een afmeting, als metrisch moeten gebruiken om te bepalen hoeveel Bezoeker IDs uw bedrijf heeft.

## 2. Gehele getallen gebruiken als afmetingen

Eerder, zouden gehelen automatisch als metriek in CJA worden behandeld. Cijfers (inclusief aangepaste gebeurtenissen uit Adobe Analytics) kunnen nu als afmetingen worden beschouwd. Hier volgt een voorbeeld:

1. Sleep de [!UICONTROL call_length_min] geheel in [!UICONTROL Dimensions] deel onder [!UICONTROL Included Components]:

   ![](assets/integers.png)

1. U kunt nu toevoegen [!UICONTROL Value Bucketing] deze dimensie in de verslaglegging op een beknopte wijze te presenteren. (Zonder vastzetten, zou elk geval van deze dimensie als lijnpunt in Werkruimte rapporterend verschijnen.)

   ![](assets/bucketing.png)

## 3. Numerieke afmetingen gebruiken als &#39;metriek&#39; in stroomdiagrammen

U kunt een numerieke dimensie gebruiken om &#39;metriek&#39; in uw [!UICONTROL  Flow] visualisatie.

1. In de gegevensweergaven [Componenten](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=en#configure-component-settings) tabblad, sleept u de [!UICONTROL Marketing Channels] schemaveld in [!UICONTROL Metrics] areaal [!UICONTROL Included components].
2. In Workspace-rapportage wordt deze stroom weergegeven [!UICONTROL Marketing Channels] stromen naar [!UICONTROL Orders]:

![](assets/flow.png)

## 4. Filteren van subgebeurtenissen uitvoeren

Deze mogelijkheid is specifiek van toepassing op arrayvelden. Met de functionaliteit include/exclude kunt u filteren op subgebeurtenisniveau, terwijl filters (segmenten) die in de filterbuilder zijn ingebouwd, u alleen filteren op gebeurtenisniveau geven. Zo kunt u sub-gebeurtenis het filtreren door te gebruiken omvat/sluit in de Mening van Gegevens, en dan die nieuwe metrische dimensie in een filter op het gebeurtenisniveau van verwijzingen.

Gebruik bijvoorbeeld de functie voor het opnemen/uitsluiten van gegevens in gegevensweergaven om alleen te verwijzen naar producten die een omzet van meer dan 50 dollar hebben gegenereerd. Dus als u een bestelling hebt die een product van 50 dollar en een product van 25 dollar bevat, verwijderen we alleen de aankoop van het product van 25 dollar, niet de volledige bestelling.

1. In de gegevensweergaven [Componenten](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=en#configure-component-settings) tabblad, sleept u de [!UICONTROL Revenue] schemaveld in [!UICONTROL Metrics] areaal [!UICONTROL Included components].
1. Selecteer metrisch en vorm het volgende op de rechterkant: a. Onder [!UICONTROL Format], selecteert u [!UICONTROL Currency].
b. Onder [!UICONTROL Currency]selecteert u USD.
c. Onder [!UICONTROL Include/Exclude Values]schakelt u het selectievakje naast [!UICONTROL Set include/exclude values].
d. Onder [!UICONTROL Match], selecteert u [!UICONTROL If all criteria are met].
e. Onder [!UICONTROL Criteria], selecteert u [!UICONTROL is greater than or equal].
f. Geef &quot;50&quot; op als waarde.

Met deze nieuwe instellingen kunt u alleen inkomsten met een hoge waarde bekijken en alles onder $50 filteren.

## 5. De opdracht [!UICONTROL No Value Options] instellen

Uw bedrijf heeft mogelijk tijd besteed aan het trainen van uw gebruikers om &quot;Niet gespecificeerd&quot;in rapporten te verwachten. De standaardwaarde in gegevensweergaven is &quot;Geen waarde&quot;. U kunt nu [naam van &quot;Geen waarde&quot; wijzigen in &quot;Niet opgegeven&quot;](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=en#configure-no-value-options-settings) in de interface voor gegevensweergaven.

Een ander voorbeeld zou een dimensie voor een registratie van het lidmaatschapsprogramma zijn. In dit geval kunt u de naam &quot;Geen waarde&quot; wijzigen in &quot;Registratie van geen lidmaatschapsprogramma&quot;.

## 6. Meerdere metriek maken met verschillende [!UICONTROL Attribution] instellingen

Met de [!UICONTROL Duplicate] aan de rechterbovenhoek een aantal maatstaven voor inkomsten maken met verschillende toewijzingsinstellingen, zoals [!UICONTROL First Touch], [!UICONTROL Last Touch], en [!UICONTROL Algorithmic].

Vergeet niet elke metrisch anders te noemen om op de verschillen, zoals &quot;Algorithmic Revenue&quot;te wijzen:

![](assets/algo-revenue.png)

Zie voor meer informatie over andere instellingen van gegevensweergaven [Gegevensweergaven maken](/help/data-views/create-dataview.md).
Voor een conceptueel overzicht van gegevensweergaven raadpleegt u [Overzicht van gegevensweergaven](/help/data-views/data-views.md).
