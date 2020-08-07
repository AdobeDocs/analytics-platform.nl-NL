---
title: Dynamische versus statische afmetingspunten in vrije vormlijsten
description: Hoe te met dynamische en statische afmetingspunten in lijsten in wisselwerking te staan.
translation-type: tm+mt
source-git-commit: cee89d021e9cd034246fe9367bc8910dac7ca7cf
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 2%

---


# Dynamische versus statische afmetingspunten in vrije vormlijsten

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

In de lijsten Freeform, kunnen de rijen en de kolommen diverse componentenwaarden in hen bevatten. Deze waarden kunnen dynamisch (verandering met tijd) of statisch (veranderen niet met tijd), afhankelijk van de analyse zijn die u wilt bouwen.

## Dynamische-dimensielitems

De dynamische afmetingspunten veranderen met tijd en zijn afhankelijk van metrisch die door in de freeformlijst wordt gesorteerd. De dynamische afmetingspunten worden aangewezen wanneer u de hoogste punten voor een bepaalde tijdspanne wilt analyseren.

Wanneer u een afmeting in een freeformlijst laat vallen, zijn de dynamische rijen teruggekeerd. Zij vertegenwoordigen de hoogste punten die aan de afmeting voor een bepaalde metrische en tijdspanne beantwoorden. U kunt een afmeting in de kolommen van de freeformlijst ook laten vallen en de afmeting breidt automatisch in de hoogste 5 afmetingspunten uit.

Bijvoorbeeld, wanneer u de Browser dimensie van het Type in de lijst sleept, de hoogste Browser de afmetingspunten van het Type (b.v. Microsoft, Apple, Google, enz.) keert dynamisch aan de lijstrijen terug. Als gelaten vallen in een kolom, de bovenkant 5 Browser de afmetingspunten van het Type dynamisch terugkeren.

De dynamische afmetingspunten hebben de optie van de rijfilter, en doen **niet** hebben vergrendelings- en X-pictogrammen aanwezig.

![](assets/dynamic-items.png)

## Statische dimensieitems

De statische afmetingspunten veranderen niet met tijd; zij zijn vaste componenten die altijd in een freeform lijst zijn teruggekeerd. De statische afmetingspunten worden de voorkeur gegeven wanneer u altijd het zelfde punt wilt analyseren, of het specifieke campagnes of specifieke dagen in de week zijn.

Wanneer u manueel specifieke componentenwaarden (afmeting, metrisch, segment, datumwaaier) in een lijst selecteert en laat vallen, is het resultaat een statische lijst van rijen of kolommen. De statische afmetingspunten kunnen ook tot stand worden gebracht als u verkiest om:

* Van rijen, klik met de rechtermuisknop > [!UICONTROL Display only selected rows]
* Van kolommen, klik met de rechtermuisknop > [!UICONTROL Make item static]

Bijvoorbeeld, wanneer u over specifieke Browser punten van het Type zoals Microsoft en Apple sleept, worden die 2 specifieke punten altijd getrokken in de lijst.

Statische dimensieitems **niet** heb de optie van de rijfilter. In plaats daarvan zijn de pictogrammen van het slot en van X aanwezig op elk punt. Klik het pictogram van X om dat afmetingspunt uit de lijst te verwijderen.

![](assets/static-items.png)

## Posten met gemengde afmetingen

De punten van de maat van verschillende afmetingen kunnen aan de zelfde lijst worden toegevoegd. De rijkopbal zegt &quot;Gemengde Afmetingen&quot;in deze gevallen. Deze afmetingspunten zijn statisch. Bijvoorbeeld, toevoegend specifieke afmetingspunten van de Browser afmeting van het Type en andere afmetingspunten van de Browser afmeting.

![](assets/mixed-dimensions.png)

## Totaal vrije rijen

De dynamische en statische rijen gedragen zich verschillend in de freeform totale rij. Standaard:

* De dynamische rijen worden samengevat server-kant en deduplicatie metriek zoals bezoeken of bezoekers
* De statische rijen worden samengevat cliënt-kant en doen **niet** deduplicatie-metingen. Om de totale rij server-kant te berekenen, verander het plaatsen van de Rij aan **Totaal-generaal weergeven**. [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/analyze/analysis-workspace/build-workspace-project/workspace-totals.html)

