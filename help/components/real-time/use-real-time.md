---
description: Begrijp hoe u real-time rapporten kunt gebruiken in Analysis Workspace.
title: Real-Time rapportage gebruiken
feature: Real-time Reporting
role: User
exl-id: 6e7dba80-5fb9-4554-b989-85eb54a4bd6a
source-git-commit: d8ff5191ea96b8871f6aaba1fc28211c22a13e0d
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Real-time rapportage gebruiken {#use-real-time-reporting}

>[!CONTEXTUALHELP]
>id="workspace_panel_realtime_refresh"
>title="In real time vernieuwen"
>abstract="Schakel deze optie in om gegevens en visualisaties in dit deelvenster in real-time te vernieuwen."

{{release-limited-testing}}

Als u real-time rapportage wilt gebruiken, schakelt u de schakeloptie **[!UICONTROL Real-time refresh]** in op een van de volgende deelvensters in uw Workspace-project:

* [Leeg deelvenster](/help/analysis-workspace/c-panels/blank-panel.md)
* [Vrije vorm](/help/analysis-workspace/c-panels/freeform-panel.md)
* [Attributie](/help/analysis-workspace/c-panels/attribution.md)
* [Volgende of vorige item](/help/analysis-workspace/c-panels/next-previous.md)

Er wordt een bericht weergegeven met de tijdstempel van de meest recente vernieuwing van de gegevens. Bijvoorbeeld: [!UICONTROL &#x200B; *Laatste verfrist zich bij 07 :55 pm*].

Selecteer in het keuzemenu de real-time periode waarover u wilt rapporteren. Beschikbare opties zijn:

* [!UICONTROL Last 15 minutes]
* [!UICONTROL Last 30 minutes]
* [!UICONTROL Last hour]
* [!UICONTROL Last 8 hours]
* [!UICONTROL Last 24 hours]

Alle visualisaties in het deelvenster worden nu elke minuut bijgewerkt met maximaal 30 minuten, terwijl het browsertabblad met het deelvenster voor real-time vernieuwen actief is.

Als voorbeeld, zie onder een momentopname van a **[!UICONTROL Real-time reporting panel]** die **[!UICONTROL Total Revenue / Hour]** bar visualization en **[!UICONTROL Total Revenue / Hour]** vrije vormlijst aangezien tijdbewegingen van **[!UICONTROL *06:26pm*]** aan **[!UICONTROL *06 :27 pm *]**&#x200B;vernieuwt.

![ In real time verfrist zich ](assets/real-time-refresh.gif)

Na 30 minuten of zodra het browsertabblad inactief wordt, wordt de schakeloptie **[!UICONTROL Real-time refresh]** automatisch uitgeschakeld en worden real-time updates gestopt.

Zodra in real time verfrist knevel gehandicapt is, keert het paneel (en alle visualisaties binnen) terug naar [ gebruik de standaard rapporteringsgegevens en eigenschappen van Customer Journey Analytics ](real-time.md#how-it-works).
