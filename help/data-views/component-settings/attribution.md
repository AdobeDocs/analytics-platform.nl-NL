---
title: Instellingen van component Attributie
description: Hiermee kunt u de standaardattributie voor een metrische waarde instellen.
source-git-commit: af357167e65f4a577880832818221f6edbfc8b0a
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 1%

---


# Instellingen van component Attributie

Met kenmerk kunt u een standaardattributiemodel instellen voor een metrische waarde. U kunt het attributiemodel van een bepaalde metrische waarde overschrijven terwijl u in Analysis Workspace werkt.

![Attributie](../assets/attribution-settings.png)

| Instelling | Beschrijving/Hoofdletters gebruiken |
| --- | --- |
| [!UICONTROL Set attribution] | Schakelt een standaard attributiemodel in wanneer deze metrische waarde wordt gebruikt. Deze standaardwaarde kan in [!UICONTROL Freeform Table] of in Berekend Metrisch worden met voeten getreden. |
| [!UICONTROL Attribution model] | Hier kunt u opgeven welk standaard [attributiemodel](/help/analysis-workspace/attribution/models.md) moet worden gebruikt. Wordt standaard ingesteld op [!UICONTROL Last Touch]. De opties zijn: Laatste aanraking, Eerste aanraking, Lineair, Deelname, Zelfde aanraking, U-Vormen, J Curve, Omgekeerde J, Tijdvermindering, Douane, Algorithmic. Sommige van deze opties maken extra velden die moeten worden ingevuld, zoals Aangepast of Tijdverlies. U kunt veelvoudige metriek tot stand brengen gebruikend het zelfde gebied - dit betekent u één [!UICONTROL Last touch] omzet metrisch en één [!UICONTROL First Touch] opbrengst metrisch kunt hebben, maar gebaseerd op het zelfde opbrengstgebied in het schema. |
| [!UICONTROL Lookback window] | Hier kunt u een standaardterugzoekvenster voor metrische gegevens opgeven. De opties zijn: [!UICONTROL Person] (Rapportagevenster), [!UICONTROL Session], [!UICONTROL Custom]. Wanneer [!UICONTROL Custom] wordt geselecteerd, geven wij u ook de optie om om het even welk aantal dagen/weken/maanden/etc. te selecteren. (maximaal 90 dagen), net als [!UICONTROL Attribution IQ]. U kunt veelvoudige metriek hebben gebruikend het zelfde schemagebied, maar elk met een afzonderlijk raadplegingsvenster. |