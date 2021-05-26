---
title: Gebruik gevallen voor gegevensweergaven in Customer Journey Analytics
description: Meerdere gebruiksgevallen die de flexibiliteit en kracht van gegevensweergaven in Customer Journey Analytics tonen
exl-id: 6ecbae45-9add-4554-8d83-b06ad016fea9
source-git-commit: 7386645aa63ddbf1fcc8835037c13382e117ef1e
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 1%

---

# Gebruiksscenario&#39;s voor gegevensweergaven

Deze gebruiksgevallen tonen de flexibiliteit en kracht van gegevensweergaven in Customer Journey Analytics.

## 1. Creeer metrisch van Orden van een pageTitle (koord) schemagebied

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

U kunt gebeurtenissen filteren om alleen weer te geven wat u wilt zien. Gebruik bijvoorbeeld de functie voor het opnemen/uitsluiten van gegevens in gegevensweergaven om alleen te verwijzen naar producten die een omzet van meer dan 50 dollar hebben gegenereerd. Dus als u een bestelling hebt die een product van 50 dollar en een product van 25 dollar bevat, verwijderen we alleen de aankoop van het product van 25 dollar, niet de volledige bestelling.

1. Op de [Componenten ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=en#configure-component-settings) tabel in de Datumweergave sleept u het schemaveld [!UICONTROL Orders] naar het [!UICONTROL Metrics] gebied onder [!UICONTROL Included components].
1. Selecteer metrisch en vorm het volgende op de rechterkant:
   1. Selecteer onder [!UICONTROL Format] de optie [!UICONTROL Currency].
   1. Selecteer onder [!UICONTROL Currency] USD.
   1. Selecteer onder [!UICONTROL Include/Exclude Values] het selectievakje naast [!UICONTROL Set include/exclude values].
   1. Selecteer onder [!UICONTROL Match] de optie [!UICONTROL If all criteria are met].
   1. Selecteer onder [!UICONTROL Criteria] de optie [!UICONTROL is greater than or equal].
   1. Geef &quot;50&quot; op als waarde.

Zie [Gegevensweergaven maken](/help/data-views/create-dataview.md) voor meer informatie over andere instellingen voor gegevensweergaven.
Voor een conceptueel overzicht van gegevensmeningen, zie [Overzicht van de meningen van Gegevens](/help/data-views/data-views.md).