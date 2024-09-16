---
description: Het nieuwe systeem van de Intelligente Alarm staat voor meer korrelige controle over alarm toe en integreert anomalieopsporing met het waakzame systeem.
title: Overzicht van intelligente waarschuwingen
feature: Workspace Basics
role: User, Admin
source-git-commit: 640624ab017d8fc0e7b942c2f00c71cf255c4296
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Overzicht van intelligente waarschuwingen

>[!NOTE]
>
>Intelligente waarschuwingen zijn beschikbaar voor alle klanten. Als u echter Anomaly Detection wilt gebruiken in Intelligent Alerts, moet u Customer Journey Analytics Select, Premiere of Ultimate hebben.

Met intelligente waarschuwingen (of alleen &quot;waarschuwingen&quot;) in Customer Journey Analytics kunt u op de hoogte worden gesteld wanneer zich abnormale gebeurtenissen in uw gegevens voordoen.

U kunt waarschuwingen instellen die moeten worden geactiveerd op basis van afwijkende drempelwaarden, gewijzigde percentages of specifieke gegevenspunten. Het alarm verstrekt korrelige controles die met [ Anomaly Detectie ](/help/analysis-workspace/c-anomaly-detection/anomaly-detection.md) integreren, die teweegbrengen wanneer u hen het meest nodig hebt.

Met intelligente waarschuwingen kunt u:

* Waarschuwingen opbouwen op basis van anomalieën (90%, 95%, 99%, 99,75% en 99,9% drempels; procentuele wijziging; boven/onder))
* Voorbeeld van hoe vaak een waarschuwing wordt geactiveerd
* Waarschuwingen verzenden via e-mail of SMS met koppelingen naar automatisch gegenereerde Analysis Workspace-projecten
* &quot;gestapelde&quot; waarschuwingen maken die meerdere meetgegevens vastleggen in één waarschuwing

Het volgende videoleerprogramma verstrekt een basisoverzicht van alarm: [ Intelligente Alarm ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/intelligent-alerts.html) (5:34)

## Begrijp hoe waarschuwingen verschillen in Customer Journey Analytics met Adobe Analytics

Het gebruik van intelligente waarschuwingen in de Customer Journey Analytics is bijna hetzelfde als het gebruik van intelligente waarschuwingen in Adobe Analytics. Er zijn echter belangrijke verschillen.

Voor meer informatie, zie [ Intelligente de eigenschapvergelijking van het Alarm: Customer Journey Analytics en Adobe Analytics ](/help/components/c-intelligent-alerts/alerts-feature-comparison.md).

## Anomalische zoekopdracht voor waarschuwingen

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
>Het gebruik van tijdstempelgegevens voor het maken van waarschuwingen kan ervoor zorgen dat waarschuwingen onjuist worden afgespeeld. Adobe raadt u aan om niet-tijdstempelgegevens te gebruiken voor intelligente waarschuwingen.

## Waarschuwingen beheren

U kunt bestaande waarschuwingen beheren in het venster Waarschuwingen. U kunt verschillende beheertaken uitvoeren voor waarschuwingen, zoals labelen, hernoemen, verwijderen en meer.

Voor meer informatie over hoe te om bestaand alarm in Customer Journey Analytics te beheren, zie [ alarm ](/help/components/c-intelligent-alerts/alert-manager.md) leiden.

