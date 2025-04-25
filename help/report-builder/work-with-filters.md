---
title: Hoe worden segmenten in Report Builder in Customer Journey Analytics gebruikt?
description: Beschrijft hoe te om segmenten in Report Builder voor Customer Journey Analytics te gebruiken
role: User
feature: Report Builder
type: Documentation
exl-id: 1f39d7f4-b508-45d8-9b97-81242c3805d3
solution: Customer Journey Analytics
source-git-commit: 6dd8a70293161ff58361953a7e48a98834b7abe0
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# Werken met segmenten

U kunt segmenten toepassen wanneer u een nieuw gegevensblok maakt of wanneer u **[!UICONTROL Edit data block]** in het deelvenster **[!UICONTROL Commands]** selecteert.

## Segmenten toepassen op een gegevensblok

Als u een segment wilt toepassen op het volledige gegevensblok, dubbelselecteert u een segment of sleept u segmenten uit de lijst met componenten naar de sectie Segmenten van de tabel.

## Filters toepassen op individuele metriek

Filters toepassen met behulp van segmenten op individuele metriek:

* Sleep een of meer segmenten van **[!UICONTROL Segments]** naar een metrische waarde in de tabel.

* Alternatief:

   1. Selecteer ![ MoreSmall ](/help/assets/icons/MoreSmall.svg) voor specifieke metrisch in de **[!UICONTROL Table]** ruit en selecteer dan **[!UICONTROL Filter metric]**.

      ![ segmentlusje die metriek tonen.](./assets/filter-metric.png){zoomable="yes"}

   1. Selecteer een of meer segmenten in het keuzemenu **[!UICONTROL Segments]** . De segmenten worden toegevoegd aan de lijst van **[!UICONTROL Segments applied]** .

      ![ toegepaste Segmenten ](assets/segments-applied.png)
   1. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om een segment uit de **[!UICONTROL Segment applied]** lijst te verwijderen. Of selecteer **[!UICONTROL Clear all]** om alle segmenten uit de lijst van **[!UICONTROL Segment applied]** te verwijderen.
   1. Selecteer **[!UICONTROL Apply]** .

Als u toegepaste filters wilt weergeven, plaatst u de muisaanwijzer boven of selecteert u een metrische waarde in het deelvenster Tabel. De metriek met toegepaste segmenten tonen een segmentpictogram.


## Snel segmenten bewerken

U kunt het deelvenster **[!UICONTROL Quick edit]** gebruiken om segmenten voor bestaande gegevensblokken toe te voegen, te verwijderen of te vervangen.

Wanneer u een bereik cellen in het werkblad selecteert, wordt met de koppeling **[!UICONTROL Segments]** in het deelvenster **[!UICONTROL Quick edit]** een overzicht weergegeven van de segmenten die worden gebruikt door de gegevensblokken in die selectie.

Segmenten bewerken met het deelvenster **[!UICONTROL Quick edit]** :

1. Selecteer een bereik cellen uit een of meerdere gegevensblokken.

1. Selecteer de koppeling **[!UICONTROL Segments]** om het deelvenster **[!UICONTROL Quick edit]** **[!UICONTROL Segments]** te starten.


### Segmenten toevoegen of verwijderen

U kunt segmenten toevoegen of verwijderen met de opties Toevoegen/Verwijderen.

1. Selecteer de tab **[!UICONTROL Add/Remove]** in het deelvenster **[!UICONTROL Quick edit]** **[!UICONTROL Segments]** .


   1. Selecteer een of meer segmenten in het keuzemenu **[!UICONTROL Segments]** . De segmenten worden toegevoegd aan de lijst van **[!UICONTROL Segments applied]** .
   1. Selecteer ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) om een segment uit de **[!UICONTROL Segment applied]** lijst te verwijderen.
   1. Selecteer **[!UICONTROL Apply]** .

Report Builder geeft een bericht weer ter bevestiging van de toegepaste segmentwijzigingen.

### Segmenten vervangen

U kunt een bestaand segment vervangen door een ander segment om te wijzigen hoe de gegevens worden gesegmenteerd.

1. Selecteer de tab **[!UICONTROL Replace]** in het deelvenster **[!UICONTROL Quick edit]** **[!UICONTROL Segments]** .

1. Gebruik het **de lijst van het Onderzoek** onderzoeksgebied om van specifieke segmenten de plaats te bepalen.

1. Selecteer een of meer segmenten die u wilt vervangen.

1. Zoek naar één of meerdere segmenten van Replace met dropdown-menu om het segment aan de **[!UICONTROL Replace with]** lijst toe te voegen.

1. Selecteer **[!UICONTROL Apply]** .

Report Builder werkt de lijst met segmenten bij om de vervanging te weerspiegelen.

## Gegevensbloksegmenten vanuit cel definiëren

Gegevensblokken kunnen verwijzen naar segmenten uit een cel. De veelvoudige gegevensblokken kunnen de zelfde cel voor segmenten van verwijzingen voorzien, toestaand u om segmenten voor veelvoudige gegevensblokken tegelijkertijd gemakkelijk te schakelen.

Segmenten uit een cel toepassen:

1. [ creeer een nieuw gegevensblok ](create-a-data-block.md#create-a-data-block) of geef een bestaand gegevensblok uit.
1. Selecteer het tabblad **[!UICONTROL Segments]** om segmenten te definiëren.
1. Selecteer ![ DataViewSelector ](/help/assets/icons/DataViewSelector.svg).

   ![ Uitgezochte segment van cel ](assets/select-segment-from-cell.png){zoomable="yes"}

1. Selecteer de cel waaruit u wilt dat de gegevensblokken naar een segment verwijzen.

1. Dubbelselecteer om een segment aan de cel toe te voegen. U kunt ook een of meer segmenten naar de sectie **[!UICONTROL Segments included]** slepen.

1. Selecteer **[!UICONTROL Apply]** om de referentiecel te maken.

1. Van het **lusje van Segmenten**, voeg het pas gecreëerde segment van de verwijzingscel aan uw gegevensblok toe.

   ![ segmenten lusje die Sheet1 tonen!J1 (Alle Gegevens) segment dat aan de lijst wordt toegevoegd.](assets/segment-from-cell-applied.png){zoomable="yes"}

1. Selecteer **[!UICONTROL Finish]** .

Als u de referentiecel als een segment wilt toepassen op andere gegevensblokken, gebruikt u de celverwijzing als een van de segmenten in de lijst **[!UICONTROL Segments]** op het tabblad **[!UICONTROL Table]** .

### Een referentiecel gebruiken om gegevensbloksegmenten te wijzigen

1. Selecteer de referentiecel in het werkblad.

1. Selecteer de koppeling onder **[!UICONTROL Segments from cell]** in het menu **[!UICONTROL Quick Edit]** .

   ![ segmenten van celverbinding die Sheet1 tonen!J1 (Alle Gegevens) ](assets/select-segment-from-cell-in-sheet.png){zoomable="yes"}

1. Selecteer het segment in het keuzemenu.

1. Selecteer **[!UICONTROL Apply]** .
