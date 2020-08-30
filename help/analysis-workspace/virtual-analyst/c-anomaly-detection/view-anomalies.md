---
description: U kunt anomalieën in een lijst of in een lijngrafiek bekijken.
title: Anomalieën weergeven in Analysis Workspace
uuid: 270a7ea9-6485-4c83-8220-5a2200bd7200
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 4%

---


# Anomalieën weergeven in Analysis Workspace

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

U kunt anomalieën in een lijst of in een lijngrafiek bekijken.

## De anomalieën van de mening in een lijst {#section_869A87B92B574A38B017A980ED8A29C5}

In een tijdreeks Freeform Lijst, wordt elke rij nu automatisch gemarkeerd met een donkergrijs uitroepteken als een gegevensanomalie is ontdekt.

![](assets/anomaly_detected.png)

De verticale grijze lijn in elke rij wijst op de verwachte waarde. Wanneer u over het uitroepteken hangt, wordt aangegeven in welke mate de afwijking afwijkt van de verwachte waarde (in + of - %).

## De anomalieën van de mening in een lijngrafiek {#section_7C1192AFDB4345A8A2CCFB3AE0C47D82}

De lijngrafiek toont de lichtgroene betrouwbaarheidsband met de afwijkende waarden (witte punten).

Als u op een witte stip klikt, wordt deze groen en toont u:

* De datum waarop de anomalie zich heeft voorgedaan
* De ruwe waarde van de anomalie
* De procentuele waarde boven of onder de verwachte waarde, die wordt weergegeven door de vaste groene lijn.

<!--* The Analyze link to start [Contribution Analysis](/help/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md).-->

![](assets/anomaly_linechart.png)

Als u veelvoudige metriek in de lijngrafiek hebt, tonen wij slechts de anomalieën en u moet over elke anomalie hangen om de betrouwbaarheidsband voor die metrisch te zien.

Het anomaly het vertrouwensinterval van de Opsporing schrapt automatisch niet de y-as van een visualisatie om de grafiek potentieel leesbaarder te maken.

U hebt de optie om het betrouwbaarheidsinterval toe te staan om de grafiek te schalen. Klik op het pictogram Instellingen (versnelling) en controleer **[!UICONTROL Allow Anomaly Detection to Scale Y Axis]**.

![](assets/scale-y-axis.png)

