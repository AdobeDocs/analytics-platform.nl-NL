---
title: Dynamische versus statische dimensie-items in vrije-vormtabellen
description: Hoe te met dynamische en statische afmetingspunten in lijsten in wisselwerking staan
feature: Visualizations
exl-id: 7806f535-15c7-40f4-955a-724d9752969d
role: User
source-git-commit: 388042e24a7b9d33ac88e05a68689308e6258339
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# Dynamische en statische dimensie-items in vrije-vormtabellen

In Freeform-tabellen kunnen de rijen en kolommen verschillende componentwaarden bevatten. Deze waarden kunnen dynamisch (verandering met tijd) of statisch (veranderen niet met tijd) zijn, afhankelijk van de analyse die u wilt bouwen.

## Dynamische dimensie-items

De dynamische afmetingspunten veranderen met tijd en zijn afhankelijk van metrisch die door in de vrije vormlijst wordt gesorteerd. Items met een dynamische dimensie hebben de voorkeur wanneer u de bovenste items gedurende een bepaalde tijdsperiode wilt analyseren.

Wanneer u een dimensie in een vrije vormlijst laat vallen, zijn de dynamische rijen teruggekeerd. Zij vertegenwoordigen de hoogste punten die aan de afmeting voor een bepaalde metrisch en tijdspanne beantwoorden. U kunt ook een dimensie neerzetten in vrije tabelkolommen en de dimensie wordt automatisch uitgebreid naar de bovenste 5 dimensieitems.

Als u bijvoorbeeld de afmetingen Browsertype naar de tabel sleept, worden de bovenste dimensie van Browsertype weergegeven (bijvoorbeeld Microsoft, Apple, Google, enz.) Hiermee gaat u dynamisch terug naar de tabelrijen. Indien neergezet in een kolom, de top 5 Browser de afmetingspunten van het Type dynamisch terugkeren.

De dynamische afmetingspunten hebben de optie van de rijfilter en de pictogrammen van X, en hebben **** geen slotpictogram aanwezig. <!--do they have the lock icon? --> Wanneer u op de x klikt naast een item met een dynamische dimensie, wordt automatisch een filter toegepast. Voor meer informatie over het toepassen van filters op lijsten, zie [ Filter en sorteerlijsten ](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).


![ A Freeform Lijst die het filterpictogram benadrukt.](assets/dynamic-items.png)

## Statische dimensie-items

De statische afmetingspunten veranderen niet met tijd; zij zijn vaste componenten die altijd in een vrije vormlijst zijn teruggekeerd. De statische afmetingspunten worden geprefereerd wanneer u altijd het zelfde punt wilt analyseren, of het specifieke campagnes of specifieke dagen in de week zijn.

Wanneer u handmatig bepaalde componentwaarden (afmetingen, metrisch, filter, datumbereik) in een tabel selecteert en neerzet, bestaat het resultaat uit een statische lijst met rijen of kolommen. De statische afmetingspunten kunnen ook worden gecreeerd als u verkiest:

* Vanuit rijen klikt u met de rechtermuisknop > [!UICONTROL Display only selected rows]
* Van kolommen, klik met de rechtermuisknop > [!UICONTROL Make item static]

Wanneer u bijvoorbeeld over specifieke BrowserType-items sleept, zoals Microsoft en Apple, worden die twee specifieke items altijd in de tabel geplaatst.

De statische afmetingspunten hebben **** niet de optie van de rijfilter. In plaats daarvan worden op elk item de pictogrammen Vergrendelen en X weergegeven. Klik op het X-pictogram om dat dimensie-item uit de tabel te verwijderen.

![ A Freeform Lijst die de Browser Type en de rij van Microsoft met een slotpictogramnota toont: Dit afmetingspunt is statisch en zal niet met tijd veranderen.](assets/static-items.png)

## Items met gemengde dimensies

Items van verschillende Dimensionen kunnen aan dezelfde tabel worden toegevoegd. In deze gevallen staat in de rijkop &quot;Gemengd Dimension&quot;. Deze dimensie-items zijn statisch. Bijvoorbeeld, toevoegend specifieke afmetingspunten van de Browser dimensie van het Type en andere afmetingspunten van de Browser afmeting.

![ A Freeform Lijst die de Gemengde kolom van Dimensionen benadrukt.](assets/mixed-dimensions.png)

## Totaal aantal rijen vrije vorm

Dynamische en statische rijen gedragen zich anders in de vrije-vormtotale rij. Standaard:

* Dynamische rijen zijn optellings server-kant en de-duplicaatmetriek zoals bezoeken of personen
* De statische rijen worden samengevat cliënt-kant en **niet** de-dubbele metriek. Om de totale rij server-kant te berekenen, verander de Rij die aan **plaatsen toont groot totaal**. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.html)
