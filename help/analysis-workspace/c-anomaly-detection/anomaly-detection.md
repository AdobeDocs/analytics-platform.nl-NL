---
description: Meer informatie over de detectie van anomalieën in Analysis Workspace.
title: Hoe Anomaly Detection werkt
feature: Anomaly Detection
exl-id: f706cdb9-bc80-42b9-9450-4f68bdb3fd85
source-git-commit: 689235eb0b982f4e572282f1c73e4606f9d82b12
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# Overzicht van anomaliedetectie

U kunt gegevensanomalieën contextafhankelijk weergeven en analyseren in Analysis Workspace.

[Videozelfstudie Anomaly Detection](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/anomaly-detection-in-analysis-workspace.html) 4:53

Anomaly Detection biedt een statistische methode om te bepalen hoe een bepaalde metrische waarde is gewijzigd ten opzichte van eerdere gegevens.

Met Anomaly Detection kunt u &quot;echte signalen&quot; scheiden van &quot;ruis&quot; en vervolgens mogelijke factoren identificeren die tot die signalen of anomalieën hebben bijgedragen. Met andere woorden, het laat je zien welke statistische fluctuaties belangrijk zijn en welke niet. U kunt dan de worteloorzaak van een ware anomalie identificeren. Bovendien kunt u betrouwbare metrische (KPI) prognoses krijgen.

Voorbeelden van anomalieën die u kunt onderzoeken zijn:

* Drastische afname in gemiddelde orderwaarde
* Pieken in orders met lage inkomsten
* Spikes of druppels in proefregistraties
* Druppels in weergaven van openingspagina&#39;s
* Spikes in videobuffergebeurtenissen
* Spikes in lage videobitsnelheden

Analysis Workspace-algoritme voor het opsporen van anomalieën bevat

* Naast de bestaande dagelijkse granulariteit wordt ook ondersteuning geboden voor granulariteit per uur, week en maand.
* Bewustzijn van seizoensgebondenheid (zoals &quot;Zwarte Vrijdag&quot;) en feestdagen.
