---
description: U kunt filters maken vanuit een aanraakpunt, filters toevoegen als aanraakpunt en hoofdworkflows vergelijken met verschillende filters in Analysis Workspace.
keywords: fallout en filters;filters in fallout-analyse;vergelijk filters in fallout
title: Filters toepassen in falloutanalyse
exl-id: 85b1024f-acd2-43b7-b4b1-b10961ba43e8
translation-type: tm+mt
source-git-commit: 76260b7362396c76942dadab599607cd038ed651
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# Filters toepassen in falloutanalyse

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

U kunt filters maken vanuit een aanraakpunt, filters toevoegen als aanraakpunt en hoofdworkflows vergelijken met verschillende filters in Analysis Workspace.

>[!IMPORTANT]
>
>Filters die als controlepunten in Vallout worden gebruikt moeten een container gebruiken die op een lager niveau dan de algemene context van de Vallout visualisatie is. Bij een val in de context van de bezoeker moeten filters die als controlepunten worden gebruikt, bezoekers of op hit-Gebaseerde filters zijn. Bij een &#39;visit-context&#39;-uitval moeten filters die als controlepunt worden gebruikt, op een hit gebaseerde filters zijn. Als u een ongeldige combinatie gebruikt, is de fallout 100%. Er is een waarschuwing toegevoegd aan de Fallout-visualisatie die wordt weergegeven wanneer u een incompatibel filter toevoegt als aanraakpunt. Bepaalde ongeldige combinaties van filtercontainers leiden tot ongeldige Fallout-diagrammen, zoals:

* Een op bezoekers gebaseerd filter gebruiken als aanraakpunt binnen een bezoekerscontext-Fallout-visualisatie
* Een op bezoekers gebaseerd filter gebruiken als aanraakpunt binnen een &#39;visit-context&#39;-uitvalvisualisatie
* Een op bezoek gebaseerd filter gebruiken als aanraakpunt binnen een visualisatie van de &quot;visit-context&quot;

## Een filter maken van een aanraakpunt {#section_915E8FBF35CD4F34828F860C1CCC2272}

1. Maak een filter vanuit een specifiek aanraakpunt waarin u bijzonder geïnteresseerd bent en dat u op andere rapporten kunt toepassen. U doet dit door met de rechtermuisknop op het aanraakpunt te klikken en **[!UICONTROL Create filter from touchpoint]** te selecteren.

   ![](assets/segment-from-touchpoint.png)

   De Filterbouwer wordt geopend en wordt vooraf gevuld met het vooraf gebouwde opeenvolgende filter dat overeenkomt met het geselecteerde aanraakpunt:

   ![](assets/segment-builder.png)

1. Geef het filter een titel en een beschrijving en sla het op.

   U kunt dit filter nu gebruiken in elk project dat u wilt.

## Een filter toevoegen als aanraakpunt {#section_17611C1A07444BE891DC21EE8FC03EFC}

Als u bijvoorbeeld wilt zien hoe uw gebruikers in de VS zich ontwikkelen en de neerslag beïnvloeden, sleept u de gebruikers in de VS naar de uitval:

![](assets/segment-touchpoint.png)

U kunt ook een AND-aanraakpunt maken door het Amerikaanse gebruikersfilter naar een ander controlepunt te slepen.

## Filters vergelijken in fallout {#section_E0B761A69B1545908B52E05379277B56}

U kunt een onbeperkt aantal filters vergelijken in de Fallout-visualisatie.

1. Selecteer de filters die u wilt vergelijken in de [!UICONTROL Filter]-rail aan de linkerkant. In ons voorbeeld hebben we twee filters geselecteerd: Amerikaanse gebruikers en gebruikers buiten de VS.
1. Sleep ze naar de neerzetzone van het filter bovenaan.

   ![](assets/segment-drop.png)

1. Optioneel: U kunt &quot;Alle Bezoekopdrachten&quot; als de standaardcontainer behouden of verwijderen.

   ![](assets/seg-compare.png)

1. U kunt nu de fallout vergelijken over de twee filters, zoals waar het ene filter het andere overtreft, of andere inzichten.
