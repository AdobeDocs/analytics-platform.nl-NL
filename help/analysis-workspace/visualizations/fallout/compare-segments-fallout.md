---
description: U kunt vanuit een aanraakpunt segmenten maken, segmenten als aanraakpunt toevoegen en de belangrijkste workflows in verschillende segmenten in Analysis Workspace vergelijken.
keywords: fallout en segmenten;segmenten in falloutanalyse;vergelijk segmenten in fallout
title: Segmenten toepassen in een falloutanalyse
feature: Visualizations
exl-id: 85b1024f-acd2-43b7-b4b1-b10961ba43e8
role: User
source-git-commit: 0101986bb86c49776a044f754d912dc1bcb9422c
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Segmenten toepassen in een falloutanalyse

U kunt vanuit een aanraakpunt segmenten maken, filters toevoegen als aanraakpunt en hoofdworkflows vergelijken met verschillende filters in Analysis Workspace.

>[!IMPORTANT]
>
>Filters die als controlepunten in Vallout worden gebruikt moeten een container gebruiken die op een lager niveau dan de algemene context van de Vallout visualisatie is. Met een persoonlijk-contextUitval, moeten de filters die als controlepunten worden gebruikt zitting of op gebeurtenis-gebaseerde filters zijn. Bij een sessiecontext Fallout moeten filters die als controlepunt worden gebruikt op gebeurtenissen gebaseerde filters zijn. Als u een ongeldige combinatie gebruikt, is de fallout 100%. Er verschijnt een waarschuwing voor de valutamarkering wanneer u een incompatibel filter toevoegt als aanraakpunt. Bepaalde ongeldige combinaties van filtercontainers leiden tot ongeldige Fallout-diagrammen, zoals:
>
>* Een persoonlijk filter gebruiken als aanraakpunt binnen een persoonlijk-context-uitvalvisualisatie
>* Het gebruiken van een op persoon-gebaseerd filter als touchpoint binnen een zitting-contextVallout visualisatie
>* Het gebruiken van een op zitting-gebaseerd filter als touchpoint binnen een zitting-contextVallout visualisatie

## Een filter maken van een aanraakpunt

1. Maak een filter vanuit een specifiek aanraakpunt waarin u bijzonder geïnteresseerd bent en dat u op andere rapporten kunt toepassen. Klik met de rechtermuisknop op het aanraakpunt en selecteer **[!UICONTROL Create filter from touchpoint]** .

   ![ het drop-down menu van het Aanraakpunt met Create segment van benadrukt aanraakpunt.](assets/fallout-createfilter.png)

   [!UICONTROL Filter builder] opent, vooraf ingevuld met het vooraf gebouwde opeenvolgende filter dat aanraakpunt aanpast u selecteerde:

   ![ de Bouwer van de Filter toont de pre-bevolkte en pre-gebouwde opeenvolgende filter.](assets/fallout-definefilter.png)

1. Geef het filter een titel en een beschrijving en sla het op.

   U kunt dit filter nu gebruiken in elk project dat u wilt.

## Een filter toevoegen als aanraakpunt

Als u bijvoorbeeld wilt zien hoe uw gebruikers in de VS zich ontwikkelen en de neerslag beïnvloeden, sleept u de gebruikers in de VS naar de uitval:

![ het geselecteerde en benadrukte filter van Gebruikers van de V.S. om in de reserve te slepen.](assets/fallout-addfilter.png)

U kunt ook een AND-aanraakpunt maken door het Amerikaanse gebruikersfilter naar een ander controlepunt te slepen.

## Filters vergelijken in fallout

U kunt een onbeperkt aantal filters vergelijken in de Fallout-visualisatie.

1. Selecteer in het deelvenster [!UICONTROL Filter] aan de linkerkant de filters die u wilt vergelijken. In het voorbeeld, worden drie filters geselecteerd: *Details van de Vlucht: Versie van de pagina A*, *Details van de Vlucht: Versie van de pagina B*, en *Details van de Vlucht: Versie van de pagina C*.
1. Sleep de drie filters naar de neerzetzone Filter boven aan de visualisatie.


1. Facultatief: U kunt *Alle Bebezoeken* als standaardcontainer houden of de container schrappen.

   ![ de Vallout die Alle Bezoeken samen met de twee filters tonen die in de vorige stap worden gesleept.](assets/fallout-multiplefilters.png)

1. U kunt nu de fallout vergelijken over de drie filters, zoals waar het ene filter het andere overtreft, of andere inzichten.
