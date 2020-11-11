---
title: De verbindingsgrootte schatten
description: Rapport over wat uw huidige gebruik van Customer Journey Analytics is (voor factureringsdoeleinden)
translation-type: tm+mt
source-git-commit: 62172cafb080e4eb4a1bba2c9d7d874fe68d14b2
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# De verbindingsgrootte schatten

Mogelijk moet u weten hoeveel rijen gegevens u momenteel hebt in [!UICONTROL Customer Journey Analytics]. Het doel van dit onderwerp is u te tonen hoe te om over wat te rapporteren uw huidige gebruik van [!UICONTROL Customer Journey Analytics] is, voor factureringsdoeleinden.

1. Klik in [!UICONTROL Customer Journey Analytics] op het tabblad **[!UICONTROL Connections]**.
1. Selecteer in het scherm [!UICONTROL Edit connection] een verbinding waarvoor u de grootte van het gebruik/de verbinding wilt bepalen.

   ![Verbinding bewerken](assets/edit-connection.png)

1. Selecteer een dataset die uw deel van verbinding van de linkerspoorstaaf is. In dit geval is het de dataset &quot;B2B Impression&quot;.

   ![gegevensset](assets/dataset.png)

1. Klik op het blauwe pictogram (i) (info) naast de naam ervan. De gegevensset heeft 3.800 rijen/gebeurtenissen. Voor het exacte aantal rijen klikt u bovendien op **[!UICONTROL Edit in Experience Platform]** onder de voorbeeldtabel. Dit zal u aan de datasets in [!UICONTROL Adobe Experience Platform] opnieuw richten.

   ![Gegevens AEP-gegevensset](assets/data-size.png)

1. Merk op **[!UICONTROL Total records]** voor deze dataset hoeveelheid aan 3.83k verslagen, met de grootte van de gegevens 388.59 KB is.

1. Herhaal stap 1-5 voor andere datasets in uw verbinding en voeg omhoog het aantal verslagen/rijen toe. Het definitieve samengevoegde aantal zal het gebruik metrisch van uw verbinding zijn, en dit is het aantal rijen van de datasets van uw verbinding die u van [!UICONTROL Adobe Experience Platform] gaat opnemen.

## Aantal toegevoegde rijen bepalen

Het aantal gebeurtenissen die daadwerkelijk in CJA worden opgenomen hangt van uw montages van de verbindingsconfiguratie af. Bovendien als u verkeerde identiteitskaart van de Persoon selecteerde of als dit identiteitskaart niet beschikbaar voor sommige rijen in de datasets is, dan [!UICONTROL Customer Journey Analytics] zal die rijen negeren. Op deze manier kunt u de werkelijke rijen met gebeurtenissen vaststellen die worden ingevoerd wanneer een verbinding is opgeslagen.

1. Wanneer u de verbinding hebt opgeslagen, maakt u een gegevensweergave van dezelfde verbinding zonder filters.
1. Creeer een project van de Werkruimte en selecteer de correcte gegevensmening. Creeer een vrije vormlijst en sleep en laat vallen **[!UICONTROL Events]** metrisch met een **[!UICONTROL Year]** afmeting. Kies het maximale datumbereik in de kalender voor datumselectie. Hierdoor kunt u het aantal gebeurtenissen zien dat in [!UICONTROL Customer Journey Analytics] wordt opgenomen.

   ![Werkruimteproject](assets/event-number.png)

   >[!NOTE]
   >
   >Dit laat u het aantal gebeurtenissen zien die van uw gebeurtenisdataset worden opgenomen. Het omvat profiel en raadplegingstype geen datasets. Voer stap 1-3 voor profiel- en opzoekgegevenssets uit en voeg de nummers toe om het totaal aan gebeurtenissen voor deze verbinding op te halen.

## Foutopsporingsverschillen opsporen

U kunt opgemerkt hebben dat het totale aantal ingegrepen gebeurtenissen &quot;7650&quot;is, maar de verbinding had slechts de gebeurtenisdataset &quot;B2B Impression&quot;met &quot;3830 rijen&quot;in AEP. Waarom is er een discrepantie? Laten we wat foutopsporing uitvoeren.

1. Verdeel deze afmeting door **[!UICONTROL Platform Dataset ID]** en u zult twee datasets met de zelfde grootte maar verschillend **[!UICONTROL Platform Dataset IDs]** opmerken. Elke dataset heeft 3825 verslagen. Dat betekent dat [!UICONTROL Customer Journey Analytics] 5 records heeft genegeerd vanwege ontbrekende persoon-id&#39;s of BAVID&#39;s (Big Visitor ID&#39;s):

   ![uitsplitsing](assets/data-size2.png)

1. Als we [!UICONTROL Adobe Experience Platform] inchecken, is er bovendien geen dataset met ID &quot;5f21c12b732044194bffc1d0&quot;, vandaar dat iemand deze specifieke dataset heeft verwijderd uit [!UICONTROL Adobe Experience Platform] toen de eerste verbinding werd gemaakt. Later werd het opnieuw toegevoegd aan [!UICONTROL Customer Journey Analytics], maar verschillende [!UICONTROL Platform Dataset ID] werd geproduceerd door [!UICONTROL Adobe Experience Platform].

   Lees meer over [implicaties van dataset en verbindingsschrapping](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html?lang=en#implications-of-deleting-data-components) in [!UICONTROL Customer Journey Analytics] en [!UICONTROL Adobe Experience Platform].