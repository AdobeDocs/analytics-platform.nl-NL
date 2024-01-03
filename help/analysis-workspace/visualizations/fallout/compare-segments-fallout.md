---
description: U kunt filters maken vanuit een aanraakpunt, filters toevoegen als aanraakpunt en hoofdworkflows vergelijken met verschillende filters in Analysis Workspace.
keywords: fallout en filters;filters in fallout-analyse;vergelijk filters in fallout
title: Filters toepassen in falloutanalyse
feature: Visualizations
exl-id: 85b1024f-acd2-43b7-b4b1-b10961ba43e8
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Filters toepassen in falloutanalyse

U kunt filters maken vanuit een aanraakpunt, filters toevoegen als aanraakpunt en hoofdworkflows vergelijken met verschillende filters in Analysis Workspace.

>[!IMPORTANT]
>
>Filters die als controlepunten in Vallout worden gebruikt moeten een container gebruiken die op een lager niveau dan de algemene context van de Vallout visualisatie is. Met een persoonlijk-context Fallout, moeten de filters die als controlepunten worden gebruikt bezoek of op gebeurtenis-gebaseerde filters zijn. Bij een &#39;visit-context&#39;-uitval moeten filters die als controlepunt worden gebruikt op gebeurtenissen gebaseerde filters zijn. Als u een ongeldige combinatie gebruikt, is de fallout 100%. Er is een waarschuwing toegevoegd aan de Fallout-visualisatie die wordt weergegeven wanneer u een incompatibel filter toevoegt als aanraakpunt. Bepaalde ongeldige combinaties van filtercontainers leiden tot ongeldige Fallout-diagrammen, zoals:

* Een persoonlijk filter gebruiken als aanraakpunt binnen een persoonlijk-context-uitvalvisualisatie
* Een persoonlijk filter gebruiken als aanraakpunt binnen een &#39;visit-context&#39;-uitvalvisualisatie
* Een op bezoek gebaseerd filter gebruiken als aanraakpunt binnen een visualisatie van de &quot;visit-context&quot;

## Een filter maken van een aanraakpunt {#section_915E8FBF35CD4F34828F860C1CCC2272}

1. Maak een filter vanuit een specifiek aanraakpunt waarin u bijzonder geïnteresseerd bent en dat u op andere rapporten kunt toepassen. U doet dit door met de rechtermuisknop op het aanraakpunt te klikken en **[!UICONTROL Create filter from touchpoint]**.

   ![Het vervolgkeuzemenu Aanraakpunt met Segment maken van aanraakpunt gemarkeerd.](assets/segment-from-touchpoint.png)

   De Filterbouwer wordt geopend en wordt vooraf gevuld met het vooraf gebouwde opeenvolgende filter dat overeenkomt met het geselecteerde aanraakpunt:

   ![De Bouwer van de Filter toont de pre-bevolkte en pre-gebouwde opeenvolgende filter.](assets/segment-builder.png)

1. Geef het filter een titel en een beschrijving en sla het op.

   U kunt dit filter nu gebruiken in elk project dat u wilt.

## Een filter toevoegen als aanraakpunt {#section_17611C1A07444BE891DC21EE8FC03EFC}

Als u bijvoorbeeld wilt zien hoe uw gebruikers in de VS zich ontwikkelen en de neerslag beïnvloeden, sleept u de gebruikers in de VS naar de uitval:

![Het filter Gebruikers in de VS is geselecteerd en gemarkeerd en wordt naar de uitval gesleept.](assets/segment-touchpoint.png)

U kunt ook een AND-aanraakpunt maken door het Amerikaanse gebruikersfilter naar een ander controlepunt te slepen.

## Filters vergelijken in fallout {#section_E0B761A69B1545908B52E05379277B56}

U kunt een onbeperkt aantal filters vergelijken in de Fallout-visualisatie.

1. Selecteer de filters die u wilt vergelijken in het dialoogvenster [!UICONTROL Filter] spoorstaaf links. In ons voorbeeld hebben we twee filters geselecteerd: US Users en Non-US Users.
1. Sleep ze naar de neerzetzone van het filter bovenaan.

   ![De uitvalweergave met geselecteerde filters en de rode pijl die naar de neerzetzone van het filter wijst.](assets/segment-drop.png)

1. Optioneel: u kunt &quot;Alle bezoeken&quot; behouden als de standaardcontainer of deze verwijderen.

   ![De uitvalfunctie die alle bezoeken toont, samen met de twee filters die in de vorige stap zijn gesleept.](assets/seg-compare.png)

1. U kunt nu de fallout vergelijken over de twee filters, zoals waar het ene filter het andere overtreft, of andere inzichten.
