---
description: Maak aangepaste datumbereiken in Analysis Workspace en sla deze op als tijdcomponenten.
keywords: Analysis Workspace
title: Aangepaste datumbereiken maken
feature: Calendar
exl-id: 1a7df63a-bf18-4c38-b7e2-e83c2d278544
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Aangepaste datumbereiken maken

Maak aangepaste datumbereiken in Analysis Workspace en sla deze op als tijdcomponenten.

**[!UICONTROL Components]** > **[!UICONTROL New Date Range]**

Er wordt een datumbereik toegepast op paneelniveau. Als u een datumbereik aan uw project wilt toevoegen, klikt u op **Deelvensters** > *`<select panel>`* en geeft u een nieuw datumbereik op.

## Datumbereik voor &quot;twee maanden geleden&quot;

De volgende waaier van de douanedatum toont een datumwaaier voor &quot;twee maanden geleden,&quot;met een Summiere visualisatie van de Verandering die richtingsverandering toont.

![De Bouwer van de Waaier van de Waaier die van het Gebruik twee maand geleden toont](assets/date-range-two-months-ago.png)

Het aangepaste datumbereik wordt boven aan het dialoogvenster [!UICONTROL Date Range] deelvenster in uw project:

![Deelvenster Datumbereik met pijl die wijst naar Twee maanden geleden.](assets/date-range-panel-two-months-ago.png)

U kunt dit aangepaste datumbereik naar een kolom slepen naast een aangepast maandelijks roldatumbereik met de voorinstelling Laatste maand voor een vergelijking. Voeg een Summiere visualisatie van de Verandering toe en selecteer de totalen van elke kolom om richtingsverandering te tonen:

![Samenvattingsverandering met een toename van 14,45%.](assets/date-range-two-months-table.png)

## Een 7-daags roldatumbereik gebruiken

Een datumbereik is van toepassing op paneelniveau. Als u een datumbereik aan uw project wilt toevoegen, klikt u op **Handelingen** > **Deelvenster toevoegen** en geeft u een nieuw datumbereik op.

In de Bouwer van de Waaier van de Waaier van de Datum, kunt u een waaier van de douanedatum tot stand brengen die in het paneel van Componenten met andere datumwaaiers toont.

U kunt bijvoorbeeld een datumbereik maken dat een rolvenster van 7 dagen opgeeft dat een week geleden eindigt:

![De Bouwer van de Waaier van de Waaier van de datum die een datumwaaier toont die 7 dagen het rollen venster specificeert.](assets/create_date_range.png)

Gebruiken *`rolling daily`*.

* De instellingen voor Start worden *`current day minus 14 days`*.

* De instellingen voor Einde worden *`current day minus 7 days`*.

Dit datumbereik kan een component zijn die u naar elke vrije-vormtabel sleept.
