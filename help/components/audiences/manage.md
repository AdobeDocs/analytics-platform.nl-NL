---
title: In Customer Journey Analytics gemaakt publiek beheren
description: Leer hoe u het publiek beheert in Customer Journey Analytics
source-git-commit: 7013237e11cb173d54dcbe236967b49d89810975
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 1%

---


# In Customer Journey Analytics gemaakt publiek beheren

Door eerder gemaakte soorten publiek te beheren, kunt u

* **Schema of planning ongedaan maken** automatisch publiek vernieuwen/bijwerken. De maximale vervaldatum in de planning is 1 jaar.
* **Een publiek vernieuwen in het schema** wanneer het bijna verlopen is. Het uitbreiden van het publiek wordt op dezelfde manier behandeld als het verlopen van geplande rapporten - admin krijgt een e-mail een maand alvorens het programma verloopt.
* De weergave van **laatste keer dat een publiek is bijgewerkt**
* Meer inzicht in de **de tijd die nodig was om een publiek te maken** van Customer Journey Analytics (CJA), en de hoeveelheid tijd het kostte om het publiek in het Profiel van de Klant in real time voor activeringsdoeleinden te hebben getoond.
* Zie of het publiek in CJA **actief wordt gebruikt door het Profiel van de Klant in real time** of (idealiter) een Experience Platform-toepassing die het publiek gebruikt dat door CJA is gemaakt.

## Gebruikersinterface voor beheer

screenshot

| UI-instelling | Definitie |
| --- | --- |
| Filters verbergen/tonen | Hiermee kunt u de volgende filters in de linkerrails weergeven of verbergen: <ul><li>Gegevens, weergave</li><li>Eigenaar</li><li>Frequentie vernieuwen</li><li>Tags</li></ul> |
| Titel en beschrijving |  |
| Gegevens |
| Grootte publiek |  |
| Eigenaar |  |
| Frequentie vernieuwen |  |
| Tags |  |
| Laatst vernieuwd |  |
| Laatst gewijzigd |  |

{style=&quot;table-layout:auto&quot;}

## CJA-publiek weergeven en gebruiken in Experience Platform

U kunt CJA-publiek in Platform bekijken door naar [!UICONTROL Segments] > [!UICONTROL Create segments] > [!UICONTROL Audiences] tab > [!UICONTROL CJA Audiences].

U kunt CJA-publiek naar de segmentdefinitie voor AEP-segmenten slepen.

![](assets/audiences-aep.png)

Als u ervoor kiest om deze Publiek naar het meer van Gegevens van AEP uit te voeren, zal het als dataset verschijnen die aan de Klasse van het Schema van het Individuele Profiel XDM in overeenstemming is:

![](assets/aep-datalake.png)

