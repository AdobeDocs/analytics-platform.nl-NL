---
title: Instellingen van component Attributie
description: Hiermee kunt u de standaardattributie voor een metrische waarde instellen.
exl-id: bc7ae6e3-7c9b-4994-97ce-690f3bdcbee5
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: b353983b13cbbfb4c846e75aecc1b78da26ddeb2
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 1%

---

# Instellingen van component Attributie

Met kenmerk kunt u een standaardattributiemodel instellen voor een metrische waarde. U kunt het attributiemodel van een bepaalde metrische waarde overschrijven terwijl u in Analysis Workspace werkt.

![Attributie](../assets/attribution-settings.png)

| Instelling | Beschrijving/Hoofdletters gebruiken |
| --- | --- |
| [!UICONTROL Set attribution] | Schakelt een standaard attributiemodel in wanneer deze metrische waarde wordt gebruikt. Deze standaardwaarde kan worden overschreven in een [!UICONTROL Freeform Table] of in een Berekend metrisch. |
| [!UICONTROL Attribution model] | Hier kunt u opgeven welke standaard [toewijzingsmodel](/help/analysis-workspace/attribution/models.md) te gebruiken. Standaardwaarden: [!UICONTROL Last Touch]. De opties zijn: Laatste aanraking, Eerste aanraking, Lineair, Deelname, Zelfde aanraking, U-Vormen, J Curve, Omgekeerde J, Tijdvermindering, Douane, Algorithmic. Sommige van deze opties maken extra velden die moeten worden ingevuld, zoals Aangepast of Tijdverlies. U kunt meerdere metriek maken met hetzelfde veld - dit betekent dat u er één kunt maken [!UICONTROL Last touch] omzet metrisch en één [!UICONTROL First Touch] omzet metrisch, maar gebaseerd op het zelfde opbrengstgebied in het schema. |
| [!UICONTROL Lookback window] | Hier kunt u een standaardterugkijkvenster voor metrisch zoeken opgeven. De opties zijn: [!UICONTROL Person] (Rapportagevenster), [!UICONTROL Session], [!UICONTROL Custom]. Wanneer [!UICONTROL Custom] is geselecteerd, kunt u ook een willekeurig aantal dagen/weken/maanden/enzovoort selecteren. (maximaal 90 dagen), net als [!UICONTROL Attribution IQ]. U kunt veelvoudige metriek hebben gebruikend het zelfde schemagebied, maar elk met een afzonderlijk raadplegingsvenster. |

{style=&quot;table-layout:auto&quot;}
