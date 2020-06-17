---
description: U kunt gegevensanomalieën contextafhankelijk weergeven en analyseren in Analysis Workspace.
title: Overzicht van anomaliedetectie
uuid: 991fde08-198c-4410-9606-d5a4f3dd8339
translation-type: tm+mt
source-git-commit: fc5a462f3d216d8cae3ce060a45ec79a44c4c918
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 7%

---


# Overzicht van anomaliedetectie

>[!NOTE] U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

U kunt gegevensanomalieën contextafhankelijk weergeven en analyseren in Analysis Workspace.

[Anomaly Detection on YouTube](https://www.youtube.com/watch?v=krXyQCjXoeU&amp;index=63&amp;list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) (4:53)

Anomaly Detection biedt een statistische methode om te bepalen hoe een bepaalde metrische waarde is gewijzigd ten opzichte van eerdere gegevens.

Met Anomaly Detection kunt u &quot;echte signalen&quot; scheiden van &quot;ruis&quot; en vervolgens mogelijke factoren identificeren die tot die signalen of anomalieën hebben bijgedragen. Met andere woorden, het laat je zien welke statistische fluctuaties belangrijk zijn en welke niet. U kunt dan de worteloorzaak van een ware anomalie identificeren. Bovendien kunt u betrouwbare metrische (KPI) prognoses krijgen.

Voorbeelden van anomalieën die u kunt onderzoeken zijn:

* Drastische afname in gemiddelde orderwaarde
* Pieken in orders met lage inkomsten
* Spikes of druppels in proefregistraties
* Druppels in weergaven van openingspagina&#39;s
* Spikes in videobuffergebeurtenissen
* Spikes in lage videobitsnelheden

Both Anomaly Detection and [Contribution Analysis](https://docs.adobe.com/content/help/nl-NL/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html) are core workflows in Analysis Workspace. U kunt de Analyse van de Bijdrage tegen om het even welke dagelijkse anomalie in werking stellen en het resultaat in uw project van Analysis Workspace inbedden.

>[!IMPORTANT] De analyse van de bijdrage is nog niet beschikbaar in Customer Journey Analytics.

Analysis Workspace-algoritme voor het opsporen van anomalieën bevat

* Naast de bestaande dagelijkse granulariteit wordt ook ondersteuning geboden voor granulariteit per uur, week en maand.
* Bewustzijn van seizoensgebondenheid (zoals &quot;Zwarte Vrijdag&quot;) en feestdagen.

## Anomaliedetectie uitschakelen

U kunt anomaliedetectie op kolomniveau uitschakelen door naar de kolominstellingen te gaan en de controle ongedaan te maken **[!UICONTROL Anomalies]**.

![](assets/turnoff_anomalies.png)
