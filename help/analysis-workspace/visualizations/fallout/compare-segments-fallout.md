---
description: U kunt vanuit een aanraakpunt segmenten maken, segmenten als aanraakpunt toevoegen en de belangrijkste workflows in verschillende segmenten in Analysis Workspace vergelijken.
keywords: fallout en segmenten;segmenten in falloutanalyse;vergelijk segmenten in fallout
title: Segmenten toepassen in een falloutanalyse
feature: Visualizations
exl-id: 85b1024f-acd2-43b7-b4b1-b10961ba43e8
role: User
source-git-commit: b14bc43a0cdf4901c5df171a116943beb2124991
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Segmenten toepassen in een falloutanalyse

U kunt vanuit een aanraakpunt segmenten maken, segmenten als aanraakpunt toevoegen en de belangrijkste workflows in verschillende segmenten in Analysis Workspace vergelijken.

>[!IMPORTANT]
>
>De segmenten die als controlepunten in Vallout worden gebruikt moeten een container gebruiken die op een lager niveau dan de algemene context van de Vallout visualisatie is. Met een persoon-contextVallout, moeten de segmenten die als controlepunten worden gebruikt zitting of op gebeurtenis-gebaseerde segmenten zijn. Met een zitting-contextVallout, moeten de segmenten die als controlepunt worden gebruikt op gebeurtenis-gebaseerde segmenten zijn. Als u een ongeldige combinatie gebruikt, is de fallout 100%. Er verschijnt een waarschuwing voor de valutamarkering wanneer u een incompatibel segment toevoegt als aanraakpunt. Bepaalde ongeldige combinaties van segmentcontainercombinaties leiden tot ongeldige Fallout-diagrammen, zoals:
>
>* Het gebruiken van een op persoon-gebaseerd segment als touchpoint binnen een persoon-contextVallout visualisatie
>* Het gebruiken van een op persoon-gebaseerd segment als touchpoint binnen een zitting-contextVallout visualisatie
>* Het gebruiken van een op zitting-gebaseerd segment als touchpoint binnen een zitting-contextVallout visualisatie

## Een segment maken van een aanraakpunt

1. Maak een segment van een bepaald aanraakpunt waarin u bijzonder geïnteresseerd bent en dat u op andere rapporten kunt toepassen. Klik met de rechtermuisknop op het aanraakpunt en selecteer **[!UICONTROL Create segment from touchpoint]** .

   ![ het drop-down menu van het Aanraakpunt met Create segment van benadrukt aanraakpunt.](assets/fallout-createfilter.png)

   [!UICONTROL Segment builder] opent, vooraf bevolkt met het vooraf gebouwde opeenvolgende segment dat aanraakpunt aanpast u selecteerde:

   ![ de Bouwer van het Segment toont het pre-bevolkte en pre-gebouwde opeenvolgende segment.](assets/fallout-definefilter.png)

1. Geef het segment een titel en een beschrijving en sla het op.

   U kunt dit segment nu gebruiken in elk gewenst project.

## Een segment toevoegen als aanraakpunt

Als u bijvoorbeeld wilt zien hoe uw gebruikers in de VS zich ontwikkelen en de neerslag beïnvloeden, sleept u gewoon het Amerikaanse gebruikerssegment naar de uitval:

![ het segment van de Gebruikers van de V.S. selecteerde en benadrukte om in de reserve te slepen.](assets/fallout-addfilter.png)

U kunt ook een AND-aanraakpunt maken door het Amerikaanse gebruikerssegment naar een ander controlepunt te slepen.

## Segmenten vergelijken bij uitvallen

U kunt een onbeperkt aantal segmenten vergelijken in de Fallout-visualisatie.

1. Selecteer in het deelvenster [!UICONTROL Segment] aan de linkerkant de segmenten die u wilt vergelijken. In het voorbeeld, worden drie segmenten geselecteerd: *Details van de Vlucht: Versie van de pagina A*, *Details van de Vlucht: Versie van de pagina B*, en *Details van de Vlucht: Versie van de pagina C*.
1. U sleept de drie segmenten naar de neerzetzone Segment boven aan de visualisatie.


1. Facultatief: U kunt *Alle Bebezoeken* als standaardcontainer houden of de container schrappen.

   ![ de Vallout die Alle Bezoeken samen met de twee segmenten tonen die in de vorige stap worden gesleept.](assets/fallout-multiplefilters.png)

1. U kunt nu de uitval over de drie segmenten vergelijken, zoals waar een segment een ander segment overtreft, of andere inzichten.
