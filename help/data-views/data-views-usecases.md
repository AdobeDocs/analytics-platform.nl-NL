---
title: Gebruik gevallen voor gegevensweergaven in Customer Journey Analytics
description: Meerdere gebruiksgevallen die de flexibiliteit en kracht van gegevensweergaven in Customer Journey Analytics tonen
translation-type: tm+mt
source-git-commit: 7db2474bf3cd16863c597295399a262c328172dc
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---


# Gebruiksscenario&#39;s voor gegevensweergaven

De mogelijkheden voor

## Creeer metrisch van Orden van een pageTitle (koord) schemagebied

Wanneer u bijvoorbeeld een gegevensweergave maakt, kunt u een [!UICONTROL Orders]-metrische waarde maken vanuit een schemaveld [!UICONTROL pageTitle] dat een tekenreeks is. Hier volgen de volgende stappen:

1. Sleep op het tabblad Componenten de [!UICONTROL pageTitle] naar de sectie [!UICONTROL Metrics] onder [!UICONTROL Included Components].
   ![](assets/use-case1a.png)
1. Markeer nu de metrische waarde die u net hebt gesleept en wijzig de naam hiervan onder [!UICONTROL Component Settings] aan de rechterkant:
   ![](assets/orders.png)
1. Open het dialoogvenster [!UICONTROL Include/Exclude Values] aan de rechterkant en geef de volgende instellingen op:
   ![](assets/orders2.png)

   De uitdrukking &quot;bevestiging&quot;wijst erop dat dit een orde is. Na het controleren van alle paginatitels waar aan die criteria wordt voldaan, zal &quot;1&quot;voor elke instantie worden geteld. Het resultaat is nieuw metrisch (niet berekend metrisch.) Het werkt met Attribution IQ, filters, en overal anders kunt u standaardmetriek gebruiken.
1. U kunt een attributiemodel voor deze metrisch, zoals [!UICONTROL Last Touch], met [!UICONTROL Lookback window] van [!UICONTROL Session] verder specificeren.
U kunt ook een andere [!UICONTROL Orders] metrisch van het zelfde gebied tot stand brengen en een verschillend attributiemodel voor het specificeren, zoals [!UICONTROL First Touch], en een verschillende [!UICONTROL Lookback window], zoals [!UICONTROL 30 days].

## Meerdere afmetingen maken van één schemaveld

## Gehele getallen gebruiken als afmetingen

34:00

Met inbegrip van emmer