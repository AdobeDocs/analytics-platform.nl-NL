---
description: Maak aangepaste datumbereiken in Analysis Workspace en sla deze op als tijdcomponenten.
keywords: Analysis Workspace
title: Aangepaste datumbereiken maken
feature: Reports & Analytics Basics
uuid: c8873d41-454d-4f22-ad1f-38cacec5a3bc
exl-id: 1a7df63a-bf18-4c38-b7e2-e83c2d278544
translation-type: tm+mt
source-git-commit: 3c10451d5a70e4f733634efb9648da843e4c0db1
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 4%

---

# Aangepaste datumbereiken maken

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Maak aangepaste datumbereiken in Analysis Workspace en sla deze op als tijdcomponenten.

**[!UICONTROL Components]** > **[!UICONTROL New Date Range]**

Er wordt een datumbereik toegepast op paneelniveau. Als u een datumbereik aan uw project wilt toevoegen, klikt u op **Deelvensters** > *`<select panel>`* en geeft u een nieuw datumbereik op.

## Datumbereik voor &quot;twee maanden geleden&quot;

De volgende waaier van de douanedatum toont een datumwaaier voor &quot;twee maanden geleden,&quot;met een Summiere visualisatie van de Verandering die richtingsverandering toont.

![](assets/date-range-two-months-ago.png)

Het aangepaste datumbereik wordt boven aan het deelvenster [!UICONTROL Date Range] in uw project weergegeven:

![](assets/date-range-panel-two-months-ago.png)

U kunt dit aangepaste datumbereik naar een kolom slepen naast een aangepast maandelijks roldatumbereik met de voorinstelling Laatste maand voor een vergelijking. Voeg een Summiere visualisatie van de Verandering toe en selecteer de totalen van elke kolom om richtingsverandering te tonen:

![](assets/date-range-two-months-table.png)

## Een 7-daags roldatumbereik gebruiken

Een datumbereik is van toepassing op paneelniveau. Als u een datumbereik aan uw project wilt toevoegen, klikt u op **Handelingen** > **Deelvenster toevoegen** en geeft u een nieuw datumbereik op.

In de Bouwer van de Waaier van de Waaier van de Datum, kunt u een waaier van de douanedatum tot stand brengen die in het paneel van Componenten met andere datumwaaiers toont.

U kunt bijvoorbeeld een datumbereik maken dat een rolvenster van 7 dagen opgeeft dat een week geleden eindigt:

![](assets/create_date_range.png)

Gebruik *`rolling daily`*.

* De begininstellingen zijn *`current day minus 14 days`*.

* De instellingen voor Einde zijn *`current day minus 7 days`*.

Dit datumbereik kan een component zijn die u naar elke vrije-vormtabel sleept.
