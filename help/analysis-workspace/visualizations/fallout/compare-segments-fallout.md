---
description: U kunt segmenten van een touchpoint tot stand brengen, segmenten toevoegen als touchpoint, en zeer belangrijke werkschema's over diverse segmenten in de Werkruimte van de Analyse vergelijken.
keywords: fallout and segmentation;segments in fallout analysis;compare segments in fallout
title: Segmenten toepassen in een uitvalanalyse
uuid: e87a33df-160e-4943-8d02-4d6609ae3bb1
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 1%

---


# Filters toepassen in de valanalyse

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

U kunt filters van een touchpoint tot stand brengen, segmenten toevoegen als touchpoint, en zeer belangrijke werkschema&#39;s over diverse filters in de Werkruimte van de Analyse vergelijken.

>[!IMPORTANT]
>
>De filters die als controlepunten in Uitval worden gebruikt moeten een container gebruiken die op een lager niveau dan de algemene context van de visualisatie van de Uitloop is. Met een bezoeker-contextUitval, moeten de filters die als controlepunten worden gebruikt bezoek of op slag-gebaseerde filters zijn. Met een bezoek-contextUitval, moeten de filters die als controlepunt worden gebruikt op hit-Gebaseerde segmenten zijn. Als u een ongeldige combinatie gebruikt, zal de fall-out 100% zijn. Wij hebben een waarschuwing aan de visualisatie van de Uitloop toegevoegd die zal tonen wanneer u een onverenigbare filter als touchpoint toevoegt. Bepaalde ongeldige combinaties van filtercontainers zullen tot ongeldige diagrammen van de Uitloop, zoals leiden:

* Het gebruiken van een op bezoeker-gebaseerd filter als touchpoint binnen een bezoeker-contextVallout visualisatie
* Het gebruiken van een op bezoeker-gebaseerd filter als touchpoint binnen een bezoek-contextVallout visualisatie
* Het gebruiken van een op bezoek-Gebaseerd filter als touchpoint binnen een bezoek-contextVallout visualisatie

## Creeer een filter van een touchpoint {#section_915E8FBF35CD4F34828F860C1CCC2272}

1. Creeer een filter van een specifiek touchpoint dat u in bijzonder geinteresseerd bent en dat nuttig zou kunnen zijn om op andere rapporten van toepassing te zijn. U doet dit door het touchpoint met de rechtermuisknop aan te klikken en te selecteren **[!UICONTROL Create filter from touchpoint]**.

   ![](assets/segment-from-touchpoint.png)

   De ontwerper van de Filter opent, pre-bevolkt met de pre-gebouwde opeenvolgende filter die touchpoint aanpast u selecteerde:

   ![](assets/segment-builder.png)

1. Geef het filter een titel en een beschrijving en sla het op.

   U kunt deze filter in om het even welk project nu gebruiken u wenst.

## Voeg een filter als touchpoint toe {#section_17611C1A07444BE891DC21EE8FC03EFC}

Als u wilt zien, bijvoorbeeld, hoe uw gebruikers in de VS trends en de gevolgen voor de uitval, sleept u gewoon het filter van de Amerikaanse gebruikers naar de uitval:

![](assets/segment-touchpoint.png)

Of u kunt een EN touchpoint tot stand brengen door het de gebruikersfilter van de V.S. op een ander controlepunt te slepen.

## Vergelijk filters in uitval {#section_E0B761A69B1545908B52E05379277B56}

U kunt een onbeperkt aantal filters in de visualisatie van de Uitloop vergelijken.

1. Selecteer de segmenten die u wilt vergelijken met de [!UICONTROL Filter] de trein links. In ons voorbeeld, hebben wij 2 segmenten geselecteerd: Gebruikers in de VS en gebruikers buiten de VS.
1. Sleep hen in de dalingsstreek van de Filter bij de bovenkant.

   ![](assets/segment-drop.png)

1. Optioneel: U kunt &quot;Alle Bezoeken&quot;als standaardcontainer houden of het schrappen.

   ![](assets/seg-compare.png)

1. U kunt de uitval over de twee filters nu vergelijken, zoals waar één filter een andere overtreft, of andere inzichten.
