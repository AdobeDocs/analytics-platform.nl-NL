---
title: Hoe worden segmenten in Report Builder in Customer Journey Analytics gebruikt?
description: Beschrijft hoe te om segmenten in Report Builder voor Customer Journey Analytics te gebruiken
role: User
feature: Report Builder
type: Documentation
exl-id: 1f39d7f4-b508-45d8-9b97-81242c3805d3
solution: Customer Journey Analytics
source-git-commit: 0d87f28aa4f8c1b16f46227abad7d374800dcb66
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# Werken met segmenten in Report Builder

U kunt Segmenten toepassen wanneer u een nieuw gegevensblok creeert of wanneer u **uitgezocht geef gegevensblok** optie van het paneel van BEVELINGEN uit.

## Filters toepassen op een gegevensblok

Als u een filter op het volledige gegevensblok wilt toepassen, dubbelklikt u op een filter of sleept u filters uit de lijst met componenten naar de sectie Filters van de tabel.

## Filters toepassen op individuele metriek

Als u filters wilt toepassen op afzonderlijke maateenheden, sleept u een filter naar een metrische waarde in de tabel. U kunt **ook klikken...** pictogram rechts van metrisch in de ruit van de Lijst en dan selecteren **metrische filter**. Als u toegepaste filters wilt weergeven, plaatst u de muisaanwijzer boven of selecteert u een metrische waarde in het deelvenster Tabel. Metrische gegevens met toegepaste filters geven een filterpictogram weer.

![ het lusje van Filters tonend metriek.](./assets/filter_by.png)

## Filters voor snel bewerken

Met het deelvenster Snel bewerken kunt u filters voor bestaande gegevensblokken toevoegen, verwijderen of vervangen.

Wanneer u een waaier van cellen in spreadsheet selecteert, **de verbinding van Filters** in Snel uitgeeft paneel toont een summiere lijst van de filters die door de gegevensblokken in die selectie worden gebruikt.

Filters bewerken met het deelvenster Snel bewerken

1. Selecteer een bereik cellen uit een of meerdere gegevensblokken.

   ![ Snel geef filterpaneel uit dat filteropties voor gegevensmeningen, datumwaaier, en filters toont.](./assets/select_multiple_dbs.png)

1. Klik op de koppeling Filters om het deelvenster Snel bewerken - Filters te starten.

   ![ het paneel van Filters die het Add gebied van de Filter en Toegepaste Filters tonen lijsten.](./assets/quick_edit_filters.png)

### Een filter toevoegen of verwijderen

U kunt filters toevoegen of verwijderen met de opties Toevoegen/Verwijderen.

1. Selecteer **toevoegen/verwijderen** lusje in Snel uitgeven-filters paneel.

   Alle filters die op de geselecteerde gegevensblokken worden toegepast, worden vermeld in het deelvenster Quick Edit-filters. De filters die op alle gegevensblokken in de selectie worden toegepast worden vermeld onder **op alle geselecteerde gegevensblokken** rubriek worden toegepast. De filters die op sommige maar niet alle gegevensblokken worden toegepast zijn vermeld onder **op 1 of meer geselecteerde gegevensblokken** rubriek wordt toegepast.

   Wanneer de veelvoudige filters in de geselecteerde gegevensblokken aanwezig zijn, kunt u naar specifieke filters zoeken gebruikend **toevoegen het onderzoeksgebied van de Filter**.

   ![ het Add gebied van de Filter.](./assets/add_filter.png)

1. Voeg filters toe door filters van **te selecteren voeg filter** drop-down menu toe.

   De lijst met doorzoekbare filters bevat alle filters die toegankelijk zijn voor de gegevensweergaven die aanwezig zijn in een of meer van de geselecteerde gegevensblokken, en alle filters die algemeen beschikbaar zijn in de organisatie.

   Wanneer u een filter toevoegt, wordt het filter toegepast op alle gegevensblokken in de selectie.

1. Om filters te verwijderen, klik het schrappingspictogram **x** rechts van filters in de **toegepaste Filters** lijst.

1. Klik **toepassen** om veranderingen te bewaren en aan het hubpaneel terug te keren.

   Report Builder geeft een bericht weer om de wijzigingen van het toegepaste filter te bevestigen.

### Een filter vervangen

U kunt een bestaand filter vervangen door een ander filter om te wijzigen hoe de gegevens worden gefilterd.

1. Selecteer **vervangen** lusje in Snel uitgeven-filters paneel.

   ![ selecteer Replace tabel.](./assets/replace_filter.png)

1. Gebruik het **de lijst van het Onderzoek** onderzoeksgebied om van specifieke filters de plaats te bepalen.

1. Kies een of meer filters die u wilt vervangen.

1. Zoek een of meer filters in het veld Vervangen door.

   Het selecteren van een filter voegt het aan **toe vervangt met**... lijst.

   ![ het Replace lusje met de Mensen op App geselecteerde gegevensblok en Replace met lijst die Personen op Herziene App tonen.](./assets/replace_screen_new.png)

1. Klik **toepassen**.

   Report Builder werkt de lijst met filters bij om de vervanging te weerspiegelen.

### Gegevensblokfilters definiëren op basis van cel

Gegevensblokken kunnen verwijzen naar filters uit een cel. Meerdere gegevensblokken kunnen verwijzen naar dezelfde cel voor filters, zodat u gemakkelijk kunt schakelen tussen filters voor meerdere gegevensblokken tegelijk.

Filters toepassen uit een cel

1. Navigeer naar stap 2 in het maken of bewerken van gegevensblokken. Zie [ een Blok van Gegevens ](./create-a-data-block.md) creëren.
1. Klik het **lusje van Filters** om filters te bepalen.
1. Klik **creeer filter van cel**.

   ![ creeer filter van celpictogram.](./assets/create-filter-from-cell.png)

1. Selecteer de cel waaruit u wilt dat de gegevensblokken naar een filter verwijzen.

1. Voeg de gewenste filters toe aan de cel door te dubbelklikken op het filter of door het te slepen naar de sectie Filters Included.

   Opmerking: Er kan slechts één keuze voor de desbetreffende cel tegelijk worden geselecteerd.

   ![ voegt filter van celvenster toe die de inbegrepen Filters tonen.](./assets/select-filters.png)

1. Klik **toepassen** om de verwijzingscel tot stand te brengen.

1. Van het **lusje van Filters**, voeg de pas gecreëerde filter van de verwijzingscel aan uw gegevensblok toe.

   ![ het lusje van Filters die Sheet1 tonen!J1 (Alle Gegevens) filter aan de lijst wordt toegevoegd.](./assets/reference-cell-filter.png)

1. Klik **Afwerking**.

   Er kan nu naar deze cel worden verwezen door andere gegevensblokken in hun filters. Als u de referentiecel als filter wilt toepassen op andere gegevensblokken, voegt u de celverwijzing vanuit het tabblad Filters gewoon toe aan de bijbehorende filters.

#### De referentiecel gebruiken om gegevensblokfilters te wijzigen

1. Selecteer de referentiecel in het werkblad.

1. Klik de verbinding onder **Filters van Cel** in Snel uitgeven menu.

   ![ Filters van celverbinding die Sheet1 tonen!J1 (Alle Gegevens) ](./assets/filters-from-cell-link.png)

1. Selecteer het filter in de keuzelijst.

   ![ drop-down menu van de Filter ](./assets/filter-drop-down.png)

1. Klik **toepassen**.
