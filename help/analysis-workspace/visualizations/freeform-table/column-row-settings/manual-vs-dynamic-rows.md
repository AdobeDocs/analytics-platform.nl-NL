---
title: Dynamische versus statische dimensie-items in vrije-vormtabellen
description: Hoe te met dynamische en statische afmetingspunten in lijsten in wisselwerking staan
feature: Visualizations
exl-id: 7806f535-15c7-40f4-955a-724d9752969d
source-git-commit: ab30cd4e884dbf92d4148e8f81a638a8ea0b63f3
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Dynamische versus statische dimensie-items in vrije-vormtabellen

In Freeform-tabellen kunnen de rijen en kolommen verschillende componentwaarden bevatten. Deze waarden kunnen dynamisch (verandering met tijd) of statisch (veranderen niet met tijd) zijn, afhankelijk van de analyse die u wilt bouwen.

## Dynamische dimensie-items

De dynamische afmetingspunten veranderen met tijd en zijn afhankelijk van metrisch die door in de vrije vormlijst wordt gesorteerd. Items met een dynamische dimensie hebben de voorkeur wanneer u de bovenste items gedurende een bepaalde tijdsperiode wilt analyseren.

Wanneer u een dimensie in een vrije vormlijst laat vallen, zijn de dynamische rijen teruggekeerd. Zij vertegenwoordigen de hoogste punten die aan de afmeting voor een bepaalde metrisch en tijdspanne beantwoorden. U kunt ook een dimensie neerzetten in vrije tabelkolommen en de dimensie wordt automatisch uitgebreid naar de bovenste 5 dimensieitems.

Als u bijvoorbeeld de afmetingen Browsertype naar de tabel sleept, worden de bovenste dimensie van Browsertype weergegeven (bijvoorbeeld Microsoft, Apple, Google, enz.) Hiermee gaat u dynamisch terug naar de tabelrijen. Indien neergezet in een kolom, de top 5 Browser de afmetingspunten van het Type dynamisch terugkeren.

Items voor dynamische afmetingen hebben de optie Rijfilter en de X-pictogrammen en doen dit **niet** hebben vergrendelingspictogram aanwezig. <!--do they have the lock icon? --> Wanneer u op de x naast een element met een dynamische dimensie klikt, wordt automatisch een filter toegepast. Zie voor meer informatie over het toepassen van filters op tabellen [Tabellen filteren en sorteren](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).


![Een vrije-vormlijst die het filterpictogram benadrukt.](assets/dynamic-items.png)

## Statische dimensie-items

De statische afmetingspunten veranderen niet met tijd; zij zijn vaste componenten die altijd in een vrije vormlijst zijn teruggekeerd. De statische afmetingspunten worden geprefereerd wanneer u altijd het zelfde punt wilt analyseren, of het specifieke campagnes of specifieke dagen in de week zijn.

Wanneer u handmatig bepaalde componentwaarden (afmetingen, metrisch, filter, datumbereik) in een tabel selecteert en neerzet, bestaat het resultaat uit een statische lijst met rijen of kolommen. De statische afmetingspunten kunnen ook worden gecreeerd als u verkiest:

* Van rijen, klik met de rechtermuisknop > [!UICONTROL Display only selected rows]
* Van kolommen, klik met de rechtermuisknop > [!UICONTROL Make item static]

Wanneer u bijvoorbeeld over specifieke BrowserType-items sleept, zoals Microsoft en Apple, worden die twee specifieke items altijd in de tabel geplaatst.

Statische dimensie-items doen dit **niet** hebben de optie Rijfilter. In plaats daarvan worden op elk item de pictogrammen Vergrendelen en X weergegeven. Klik op het X-pictogram om dat dimensie-item uit de tabel te verwijderen.

![Een tabel met vrije vorm waarin het browsertype en de Microsoft-rij worden aangeduid met een slotpictogramopmerking: dit dimensielement is statisch en verandert niet met de tijd.](assets/static-items.png)

## Items met gemengde dimensies

Items van verschillende Dimensionen kunnen aan dezelfde tabel worden toegevoegd. In deze gevallen staat in de rijkop &quot;Gemengd Dimension&quot;. Deze dimensie-items zijn statisch. Bijvoorbeeld, toevoegend specifieke afmetingspunten van de Browser dimensie van het Type en andere afmetingspunten van de Browser afmeting.

![Een tabel voor vrije vorm die de kolom Gemengde Dimensionen markeert.](assets/mixed-dimensions.png)

## Totaal aantal rijen vrije vorm

Dynamische en statische rijen gedragen zich anders in de vrije-vormtotale rij. Standaard:

* Dynamische rijen zijn optellings server-kant en de-duplicaatmetriek zoals bezoeken of personen
* Statische rijen worden als client samengevoegd en wel **niet** deduplicatie van metingen. Als u de totale rijserver wilt berekenen, wijzigt u de rijinstelling in **Totaal-generaal tonen**. [Meer informatie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.html)
