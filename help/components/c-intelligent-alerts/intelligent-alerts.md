---
description: Alarm maakt korrelige controle over meldingen mogelijk, en integratie met anomaliedetectie.
title: Overzicht van waarschuwingen
feature: Workspace Basics
role: User, Admin
source-git-commit: def8b074ea468e409e340415d5e96f75d6b69312
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Overzicht van waarschuwingen

Met waarschuwingen in Customer Journey Analytics kunt u op basis van gewijzigde percentages of specifieke gegevenspunten op de hoogte worden gesteld.

Afhankelijk van uw Customer Journey Analytics-pakket kunt u ook waarschuwingen gebruiken die op basis van afwijkende drempelwaarden moeten worden geactiveerd. Deze alarm (die ook als &quot;Intelligente Alarm&quot;wordt bekend), verstrekt korrelige controles die met [ Anomaly Detectie ](/help/analysis-workspace/c-anomaly-detection/anomaly-detection.md) integreren, die teweegbrengen wanneer u hen het meest nodig hebt.

Met waarschuwingen kunt u:

* Voorbeeld van hoe vaak een waarschuwing wordt geactiveerd
* Waarschuwingen verzenden via e-mail of SMS met koppelingen naar automatisch gegenereerde Analysis Workspace-projecten
* &quot;gestapelde&quot; waarschuwingen maken die meerdere meetgegevens vastleggen in één waarschuwing
* Berichten maken op basis van anomalieën (90%, 95%, 99%, 99,75% en 99,9% drempelwaarden; % wijziging; boven/onder) (Alleen beschikbaar voor klanten van Customers Journey Analytics met een Select-, Premier- of Ultimate-pakket)

Het volgende videoleerprogramma verstrekt een basisoverzicht van alarm: [ Alarm ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/intelligent-alerts.html) (5:34)

## Begrijp hoe waarschuwingen verschillen in Customer Journey Analytics met Adobe Analytics

Het gebruik van waarschuwingen in Customer Journey Analytics is bijna hetzelfde als het gebruik van waarschuwingen in Adobe Analytics. Er zijn echter belangrijke verschillen.

Voor meer informatie, zie [ de eigenschapvergelijking van het Alarm: Customer Journey Analytics en Adobe Analytics ](/help/components/c-intelligent-alerts/alerts-feature-comparison.md).

## Anomalische zoekopdracht voor waarschuwingen

>[!NOTE]
>
>Het gebruiken van alarm met anomalieopsporing (die ook als _Intelligente Alarm_ wordt bekend) is beschikbaar slechts aan organisaties met een Uitgezochte Customer Journey Analytics, Primair, of Ultimate pakket.

Als een waarschuwing afwijkende detectie gebruikt, varieert de trainingsperiode op basis van de voor de waarschuwing geselecteerde granulariteit.

* Maandelijkse granulariteit: 15 maanden + zelfde marge vorig jaar
* Wekelijkse granulariteit: 15 weken + zelfde bereik vorig jaar
* Dagelijkse granulariteit: 35 dagen + zelfde bereik vorig jaar
* Urogranulariteit: 336 uur

Voor meer informatie, zie [ Statistische technieken die in Anomaly Detection ](/help/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md) worden gebruikt.

## Waarschuwingen maken

Voor informatie over hoe te om alarm in Customer Journey Analytics tot stand te brengen, zie [ alarm ](/help/components/c-intelligent-alerts/alert-builder.md) creëren.

>[!IMPORTANT]
>
>Het gebruik van tijdstempelgegevens voor het maken van waarschuwingen kan ervoor zorgen dat waarschuwingen onjuist worden afgespeeld. Adobe raadt aan om niet-tijdstempelgegevens te gebruiken voor waarschuwingen.

## Waarschuwingen beheren

U kunt bestaande waarschuwingen beheren in het venster Waarschuwingen. U kunt verschillende beheertaken uitvoeren voor waarschuwingen, zoals labelen, hernoemen, verwijderen en meer.

Voor meer informatie over hoe te om bestaand alarm in Customer Journey Analytics te beheren, zie [ alarm ](/help/components/c-intelligent-alerts/alert-manager.md) leiden.

