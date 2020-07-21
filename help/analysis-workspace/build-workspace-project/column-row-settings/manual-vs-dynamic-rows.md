---
title: Dynamische waarden versus statische waarden
description: Hoe te met dynamische en statische afmetingswaarden in lijsten in wisselwerking te staan.
translation-type: tm+mt
source-git-commit: 0477302df92ccab30d9f3a45cc7b22f2112a0c70
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 2%

---


# Dynamische waarden versus waarden van statische afmetingen in vrije-vormtabellen

>[!NOTE] U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

In Freeform-tabellen kunnen de rijen en kolommen verschillende componentwaarden bevatten. Deze waarden kunnen dynamisch (verandering met tijd) of statisch (veranderen niet met tijd) zijn, afhankelijk van de analyse die u wilt bouwen.

## Dynamische waarden van afmetingen

De dynamische afmetingswaarden veranderen met tijd en zijn afhankelijk van metrisch die door in de vrije vormlijst wordt gesorteerd. De dynamische waarden van de afmeting worden geprefereerd wanneer u de hoogste punten voor een bepaalde tijdspanne wilt analyseren.

Wanneer u een dimensie in een vrije vormlijst laat vallen, zijn de dynamische rijen teruggekeerd. Zij vertegenwoordigen de hoogste punten die aan de afmeting voor een bepaalde metrisch en tijdspanne beantwoorden. U kunt ook een dimensie neerzetten in vrije-vormtabelkolommen en de dimensie wordt automatisch uitgebreid naar de bovenste waarden van de vijf dimensies.

Als u bijvoorbeeld de dimensie Browsertype naar de tabel sleept, worden de waarden van de bovenste browsertype (bijv. Microsoft, Apple, Google, enz.) Hiermee gaat u dynamisch terug naar de tabelrijen. Indien neergezet in een kolom, de hoogste 5 waarden van de Browser van het Type dynamisch terugkeren.

Dynamische waarden van afmetingen hebben de optie voor het rijfilter en er zijn **geen** vergrendelingspictogrammen en X-pictogrammen aanwezig.

## Statische waarden voor afmetingen

De waarden van de statische afmeting veranderen niet met tijd; het zijn vaste componenten die altijd worden geretourneerd in een vrije-vormtabel. De statische waarden van de afmeting worden geprefereerd wanneer u altijd het zelfde punt wilt analyseren, of het specifieke campagnes of specifieke dagen in de week zijn.

Wanneer u handmatig bepaalde componentwaarden (afmetingen, metrisch, segment, datumbereik) in een tabel selecteert en neerzet, is het resultaat een statische lijst met rijen of kolommen. U kunt ook statische waarden voor dimensies maken als u dat wilt:

* Van rijen, klik met de rechtermuisknop > [!UICONTROL Display only selected rows]
* Van kolommen, klik met de rechtermuisknop > [!UICONTROL Make item static]

Wanneer u bijvoorbeeld over specifieke BrowserType-items sleept, zoals Microsoft en Apple, worden die twee specifieke items altijd in de tabel geplaatst.

Waarden voor statische afmetingen hebben **niet** de optie Rijfilter. In plaats daarvan worden op elk item de pictogrammen Vergrendelen en X weergegeven. Klik op het X-pictogram om die waarde voor de dimensie uit de tabel te verwijderen.

## Waarden voor gemengde dimensies

Dimensiewaarden van verschillende afmetingen kunnen aan dezelfde tabel worden toegevoegd. De rijkopbal zegt &quot;Gemengde Afmetingen&quot;in deze gevallen. Deze waarden voor afmetingen zijn statisch. Bijvoorbeeld, toevoegend specifieke afmetingswaarden van de Browser dimensie van het Type en andere afmeting waarden van de Browser afmeting.

## Totaal aantal rijen vrije vorm

Dynamische en statische rijen gedragen zich anders in de vrije-vormtotale rij. Standaard:

* Dynamische rijen worden samengevat op de server en worden niet-gedupliceerde afmetingen zoals bezoeken of bezoekers
* Statische rijen worden als client-side opgeteld en dedupliceren **niet** metriek.

[Meer informatie over de totale](https://docs.adobe.com/content/help/nl-NL/analytics/analyze/analysis-workspace/build-workspace-project/workspace-totals.html) opties van de Werkruimte voor dynamische en statische rijen.
