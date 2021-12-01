---
title: De CJA-verbindingsgrootte schatten
description: Rapport over uw huidige gebruik van Customer Journey Analytics
exl-id: 5599b34f-342d-4c68-b7c9-2ac3ea50d078
solution: Customer Journey Analytics
source-git-commit: faaf3d19ed37019ba284b41420628750cdb413b8
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# De verbindingsgrootte schatten

Mogelijk moet u weten hoeveel rijen gegevens u momenteel hebt in [!UICONTROL Customer Journey Analytics]. Het doel van dit onderwerp is u te tonen hoe te om over uw huidige gebruik van te rapporteren [!UICONTROL Customer Journey Analytics].

1. In [!UICONTROL Customer Journey Analytics]klikt u op de knop **[!UICONTROL Connections]** tab.
1. Op de [!UICONTROL Edit connection] , selecteert u een verbinding waarvan u de grootte van het gebruik of de verbinding wilt bepalen.

   ![Verbinding bewerken](assets/edit-connection.png)

1. Selecteer een dataset die uw deel van de verbinding van de linkerspoorstaaf is. In dit geval is het de dataset &quot;B2B Impression&quot;.

   ![gegevensset](assets/dataset.png)

1. Klik op het blauwe pictogram (i) (info) naast de naam ervan. U zult merken dat de dataset 3.8k rijen/gebeurtenissen heeft. Voor het exacte aantal rijen klikt u bovendien op **[!UICONTROL Edit in Experience Platform]** onder de voorbeeldtabel. Dit zal u aan datasets in omleiden [!UICONTROL Adobe Experience Platform].

   ![Gegevens AEP-gegevensset](assets/data-size.png)

1. Let op: **[!UICONTROL Total records]** voor deze gegevensset bedraagt de hoeveelheid 3,83 k records, waarbij de grootte van de gegevens 388,59 kB is.

1. Herhaal stap 1-5 voor andere datasets in uw verbinding en voeg omhoog het aantal verslagen/rijen toe. Het uiteindelijke geaggregeerde getal is de gebruikstemetrische waarde van de verbinding. Dit is het aantal rijen van de datasets van uw verbinding die u van gaat krijgen [!UICONTROL Adobe Experience Platform].

## Aantal toegevoegde rijen bepalen

Het aantal gebeurtenissen dat daadwerkelijk is opgenomen in [!UICONTROL Customer Journey Analytics] hangt van uw montages van de verbindingsconfiguratie af. Bovendien als u verkeerde identiteitskaart van de Persoon selecteerde of als dit identiteitskaart niet beschikbaar voor sommige rijen in de datasets is, dan [!UICONTROL Customer Journey Analytics] Deze rijen worden genegeerd. Voer de volgende stappen uit om de werkelijke rijen met opgenomen gebeurtenissen te bepalen:

1. Wanneer u de verbinding hebt opgeslagen, maakt u een gegevensweergave van dezelfde verbinding zonder filters.
1. Creeer een project van de Werkruimte en selecteer de correcte gegevensmening. Een vrije-vormtabel maken en de **[!UICONTROL Events]** metrisch met een **[!UICONTROL Year]** dimensie. Kies een groot voldoende datumbereik in de kalender voor datumselectie om alle gegevens in de verbinding in te kapselen. Op deze manier kunt u het aantal gebeurtenissen zien waarin [!UICONTROL Customer Journey Analytics].

   ![Werkruimteproject](assets/event-number.png)

   >[!NOTE]
   >
   >Dit laat u het aantal gebeurtenissen zien die van uw gebeurtenisdataset worden opgenomen. Het omvat profiel en raadplegingstype geen datasets. Voer stap 1-3 onder &quot;De verbindingsgrootte schatten&quot; voor profiel- en opzoekgegevenssets uit en voeg de nummers toe om het totale aantal rijen voor deze verbinding op te halen.

## Diagnose discrepanties

In sommige gevallen, kunt u opmerken dat het totale aantal gebeurtenissen die door uw verbinding worden opgenomen verschillend is dan het aantal rijen in de dataset in [!UICONTROL Adobe Experience Platform]. In dit voorbeeld heeft de dataset &quot;B2B Impression&quot; 7650 rijen, maar de dataset bevat 3830 rijen in [!UICONTROL Adobe Experience Platform]. Er zijn verschillende redenen waarom er verschillen kunnen optreden en de volgende stappen kunnen worden uitgevoerd om een diagnose te stellen:

1. Verdeel deze dimensie door **[!UICONTROL Platform Dataset ID]** en u zult twee datasets met de zelfde grootte maar verschillend opmerken **[!UICONTROL Platform Dataset IDs]**. Elke dataset heeft 3825 verslagen. Dat betekent [!UICONTROL Customer Journey Analytics] 5 records genegeerd wegens ontbrekende persoon-id&#39;s of ontbrekende tijdstempels:

   ![uitsplitsing](assets/data-size2.png)

1. Als we inchecken [!UICONTROL Adobe Experience Platform], is er geen dataset met ID &quot;5f21c12b732044194bffc1d0&quot;, vandaar dat iemand deze specifieke dataset van schrapte [!UICONTROL Adobe Experience Platform] wanneer de eerste verbinding werd gemaakt. Later werd het toegevoegd aan [!UICONTROL Customer Journey Analytics] maar een andere [!UICONTROL Platform Dataset ID] is gegenereerd door [!UICONTROL Adobe Experience Platform].

Meer informatie over de [implicaties van gegevensset en het schrappen van verbindingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html?lang=en#implications-of-deleting-data-components) in [!UICONTROL Customer Journey Analytics] en [!UICONTROL Adobe Experience Platform].
