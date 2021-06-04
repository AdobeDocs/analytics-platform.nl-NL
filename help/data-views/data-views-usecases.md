---
title: Gebruik gevallen voor gegevensweergaven in Customer Journey Analytics
description: Meerdere gebruiksgevallen die de flexibiliteit en kracht van gegevensweergaven in Customer Journey Analytics tonen
exl-id: 6ecbae45-9add-4554-8d83-b06ad016fea9
source-git-commit: acf2728539562a2bb9be2adfbeb7ae6cc4f3dffd
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Gebruiksscenario&#39;s voor gegevensweergaven

Deze gebruiksgevallen tonen de flexibiliteit en kracht van gegevensweergaven in Customer Journey Analytics.

## 1. Een metrische waarde maken op basis van een tekenreeksschemaveld

Wanneer u bijvoorbeeld een gegevensweergave maakt, kunt u een [!UICONTROL Orders]-metrische waarde maken vanuit een schemaveld [!UICONTROL pageTitle] dat een tekenreeks is. Hier volgen de volgende stappen:

1. Sleep op het tabblad Componenten de [!UICONTROL pageTitle] naar de sectie [!UICONTROL Metrics] onder [!UICONTROL Included Components].
   ![](assets/use-case1a.png)
1. Markeer nu de metrische waarde die u net hebt gesleept en wijzig de naam hiervan onder [!UICONTROL Component Settings] aan de rechterkant:
   ![](assets/orders.png)
1. Open het dialoogvenster [!UICONTROL Include/Exclude Values] aan de rechterkant en geef de volgende instellingen op:
   ![](assets/orders2.png)

   De uitdrukking &quot;bevestiging&quot;wijst erop dat dit een orde is. Na het controleren van alle paginatitels waar aan die criteria wordt voldaan, zal &quot;1&quot;voor elke instantie worden geteld. Het resultaat is nieuw metrisch (niet berekend metrisch.) Een metrisch die inbegrepen/uitgesloten waarden heeft kan overal worden gebruikt andere metrisch. Het werkt met Attribution IQ, filters, en overal anders kunt u standaardmetriek gebruiken.
1. U kunt een attributiemodel voor deze metrisch, zoals [!UICONTROL Last Touch], met [!UICONTROL Lookback window] van [!UICONTROL Session] verder specificeren.
U kunt ook een andere [!UICONTROL Orders] metrisch van het zelfde gebied tot stand brengen en een verschillend attributiemodel voor het specificeren, zoals [!UICONTROL First Touch], en een verschillende [!UICONTROL Lookback window], zoals [!UICONTROL 30 days].

Een ander voorbeeld zou de identiteitskaart van de Bezoeker, een afmeting, als metrisch moeten gebruiken om te bepalen hoeveel Bezoeker IDs uw bedrijf heeft.

## 2. Gehele getallen gebruiken als afmetingen

Eerder, zouden gehelen automatisch als metriek in CJA worden behandeld. Cijfers (inclusief aangepaste gebeurtenissen uit Adobe Analytics) kunnen nu als afmetingen worden beschouwd. Hier volgt een voorbeeld:

1. Sleep het gehele getal [!UICONTROL call_length_min] naar de sectie [!UICONTROL Dimensions] onder [!UICONTROL Included Components]:

   ![](assets/integers.png)

1. U kunt [!UICONTROL Value Bucketing] nu toevoegen om deze dimensie op een beknopte manier in rapportering voor te stellen. (Zonder vastzetten, zou elk geval van deze dimensie als lijnpunt in Werkruimte rapporterend verschijnen.)

   ![](assets/bucketing.png)

## 3. Numerieke afmetingen gebruiken als &#39;metriek&#39; in stroomdiagrammen

U kunt een numerieke dimensie gebruiken om &quot;metriek&quot;in uw [!UICONTROL  Flow] visualisatie te krijgen.

1. Op de [Componenten ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=en#configure-component-settings) tabel in de Datumweergave sleept u het schemaveld [!UICONTROL Marketing Channels] naar het [!UICONTROL Metrics] gebied onder [!UICONTROL Included components].
2. In Werkruimterapportage, toont deze stroom [!UICONTROL Marketing Channels] die in [!UICONTROL Orders] stroomt:

![](assets/flow.png)

## 4. Filteren van subgebeurtenissen uitvoeren

Deze mogelijkheid is specifiek van toepassing op arrayvelden. Met de functionaliteit include/exclude kunt u filteren op subgebeurtenisniveau, terwijl filters (segmenten) die in de filterbuilder zijn ingebouwd, u alleen filteren op gebeurtenisniveau geven. Zo kunt u sub-gebeurtenis het filtreren door te gebruiken omvat/sluit in de Mening van Gegevens, en dan die nieuwe metrische dimensie in een filter op het gebeurtenisniveau van verwijzingen.

Gebruik bijvoorbeeld de functie voor het opnemen/uitsluiten van gegevens in gegevensweergaven om alleen te verwijzen naar producten die een omzet van meer dan 50 dollar hebben gegenereerd. Dus als u een bestelling hebt die een product van 50 dollar en een product van 25 dollar bevat, verwijderen we alleen de aankoop van het product van 25 dollar, niet de volledige bestelling.

1. Op de [Componenten ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=en#configure-component-settings) tabel in de Datumweergave sleept u het schemaveld [!UICONTROL Revenue] naar het [!UICONTROL Metrics] gebied onder [!UICONTROL Included components].
1. Selecteer metrisch en vorm het volgende op de rechterkant:
a. Selecteer [!UICONTROL Currency] onder [!UICONTROL Format].
b. Selecteer onder [!UICONTROL Currency] USD.
c. Selecteer onder [!UICONTROL Include/Exclude Values] het selectievakje naast [!UICONTROL Set include/exclude values].
d. Selecteer [!UICONTROL If all criteria are met] onder [!UICONTROL Match].
e. Selecteer [!UICONTROL is greater than or equal] onder [!UICONTROL Criteria].
f. Geef &quot;50&quot; op als waarde.

Met deze nieuwe instellingen kunt u alleen inkomsten met een hoge waarde bekijken en alles onder $50 filteren.

## 5. De instelling [!UICONTROL No Value Options] gebruiken

Uw bedrijf heeft mogelijk tijd besteed aan het trainen van uw gebruikers om &quot;Niet gespecificeerd&quot;in rapporten te verwachten. De standaardwaarde in gegevensweergaven is &quot;Geen waarde&quot;. U kunt [de naam van &quot;Geen Waarde&quot;nu veranderen in &quot;Niet gespecificeerd&quot;](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=en#configure-no-value-options-settings) in de UI van de Mening van Gegevens.

Een ander voorbeeld zou een dimensie voor een registratie van het lidmaatschapsprogramma zijn. In dit geval kunt u de naam &quot;Geen waarde&quot; wijzigen in &quot;Registratie van geen lidmaatschapsprogramma&quot;.

## 6. Meerdere metriek maken met verschillende [!UICONTROL Attribution]-instellingen

Met de functie [!UICONTROL Duplicate] rechtsboven maakt u een aantal maateenheden voor inkomsten met verschillende toewijzingsinstellingen, zoals [!UICONTROL First Touch], [!UICONTROL Last Touch] en [!UICONTROL Algorithmic].

Vergeet niet elke metrisch anders te noemen om op de verschillen, zoals &quot;Algorithmic Revenue&quot;te wijzen:

![](assets/algo-revenue.png)

Zie [Gegevensweergaven maken](/help/data-views/create-dataview.md) voor meer informatie over andere instellingen voor gegevensweergaven.
Voor een conceptueel overzicht van gegevensmeningen, zie [Overzicht van de meningen van Gegevens](/help/data-views/data-views.md).
