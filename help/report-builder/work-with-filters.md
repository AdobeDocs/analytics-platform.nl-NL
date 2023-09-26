---
title: Filters gebruiken in Report Builder in Customer Journey Analytics
description: Beschrijft hoe te filters in Report Builder voor Customer Journey Analytics gebruiken
role: Data Engineer, Data Architect, Admin, User
feature: Report Builder
type: Documentation
exl-id: 1f39d7f4-b508-45d8-9b97-81242c3805d3
solution: Customer Journey Analytics
source-git-commit: 49a35a256758b259dfb2133658bae617315774e4
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 0%

---

# Werken met filters in Report Builder

U kunt filters toepassen wanneer u een nieuw gegevensblok maakt of wanneer u de optie **Gegevensblok bewerken** in het deelvenster OPDRACHTEN.

## Filters toepassen op een gegevensblok

Als u een filter op het volledige gegevensblok wilt toepassen, dubbelklikt u op een filter of sleept u filters uit de lijst met componenten naar de sectie Filters van de tabel.

## Filters toepassen op individuele metriek

Als u filters wilt toepassen op afzonderlijke maateenheden, sleept u een filter naar een metrische waarde in de tabel. U kunt ook op de knop **...** pictogram rechts van metrisch in de ruit van de Lijst en selecteer dan **Metrisch filter**. Als u toegepaste filters wilt weergeven, plaatst u de muisaanwijzer boven of selecteert u een metrische waarde in het deelvenster Tabel. Metrische gegevens met toegepaste filters geven een filterpictogram weer.

![Tabblad Filters waarin gegevens worden weergegeven.](./assets/filter_by.png)

## Filters voor snel bewerken

Met het deelvenster Snel bewerken kunt u filters voor bestaande gegevensblokken toevoegen, verwijderen of vervangen.

Wanneer u een reeks cellen in het werkblad selecteert, wordt de **Filters** in het deelvenster Snel bewerken wordt een overzicht weergegeven van de filters die worden gebruikt door de gegevensblokken in die selectie.

Filters bewerken met het deelvenster Snel bewerken

1. Selecteer een bereik cellen uit een of meerdere gegevensblokken.

   ![Het filterdeelvenster Snel bewerken bevat filteropties voor gegevensweergaven, datumbereik en filters.](./assets/select_multiple_dbs.png)

1. Klik op de koppeling Filters om het deelvenster Snel bewerken - Filters te starten.

   ![in het deelvenster Filters worden het veld Filter toevoegen en de lijsten Filters die zijn toegepast weergegeven.](./assets/quick_edit_filters.png)

### Een filter toevoegen of verwijderen

U kunt filters toevoegen of verwijderen met de opties Toevoegen/Verwijderen.

1. Selecteer de **Toevoegen/verwijderen** in het deelvenster Quick edit-filters.

   Alle filters die op de geselecteerde gegevensblokken worden toegepast, worden vermeld in het deelvenster Quick Edit-filters. Filters die op alle gegevensblokken in de selectie zijn toegepast, worden onder de **Toegepast op alle geselecteerde gegevensblokken** kop. Filters die op enkele maar niet alle gegevensblokken zijn toegepast, worden vermeld onder de **Toegepast op 1 of meer geselecteerde gegevensblokken** kop.

   Wanneer de geselecteerde gegevensblokken meerdere filters bevatten, kunt u naar specifieke filters zoeken met de opdracht **Filter toevoegen** zoekveld.

   ![Het veld Filter toevoegen.](./assets/add_filter.png)

1. Filters toevoegen door filters te selecteren in het menu **Filter toevoegen** vervolgkeuzelijst.

   De lijst met doorzoekbare filters bevat alle filters die toegankelijk zijn voor de gegevensweergaven die aanwezig zijn in een of meer van de geselecteerde gegevensblokken, en alle filters die algemeen beschikbaar zijn in de organisatie.

   Wanneer u een filter toevoegt, wordt het filter toegepast op alle gegevensblokken in de selectie.

1. Als u filters wilt verwijderen, klikt u op het verwijderpictogram **x** rechts van filters in het dialoogvenster **Toegepaste filters** lijst.

1. Klikken **Toepassen** om de wijzigingen op te slaan en terug te keren naar het hubdeelvenster.

   Report Builder geeft een bericht weer ter bevestiging van de wijzigingen van het toegepaste filter.

### Een filter vervangen

U kunt een bestaand filter vervangen door een ander filter om te wijzigen hoe de gegevens worden gefilterd.

1. Selecteer de **Vervangen** in het deelvenster Quick edit-filters.

   ![Selecteer het tabblad Vervangen.](./assets/replace_filter.png)

1. Gebruik de **Zoeklijst** zoekveld om specifieke filters te zoeken.

1. Kies een of meer filters die u wilt vervangen.

1. Zoek een of meer filters in het veld Vervangen door.

   Als u een filter selecteert, wordt dit toegevoegd aan de **Vervangen door**... lijst.

   ![Het tabblad Vervangen met het gegevensblok Personen in app geselecteerd en de lijst Vervangen met bijgewerkte lijst met personen in app herzien.](./assets/replace_screen_new.png)

1. Klikken **Toepassen**.

   Report Builder werkt de lijst met filters bij om de vervanging te weerspiegelen.

### Gegevensblokfilters definiëren op basis van cel

Gegevensblokken kunnen verwijzen naar filters uit een cel. Meerdere gegevensblokken kunnen verwijzen naar dezelfde cel voor filters, zodat u gemakkelijk kunt schakelen tussen filters voor meerdere gegevensblokken tegelijk.

Filters toepassen uit een cel

1. Navigeer naar stap 2 in het maken of bewerken van gegevensblokken. Zie [Een gegevensblok maken](./create-a-data-block.md).
1. Klik op de knop **Filters** om filters te definiëren.
1. Klikken **Filter van cel maken**.

   ![Filter maken van celpictogram.](./assets/create-filter-from-cell.png)

1. Selecteer de cel waaruit u wilt dat de gegevensblokken naar een filter verwijzen.

1. Voeg de gewenste filters toe aan de cel door te dubbelklikken op het filter of door het te slepen naar de sectie Filters Included.

   Opmerking: Er kan slechts één keuze voor de desbetreffende cel tegelijk worden geselecteerd.

   ![Het filter Toevoegen vanuit het celvenster waarin de meegeleverde filters worden weergegeven.](./assets/select-filters.png)

1. Klikken **Toepassen** om de referentiecel te maken.

1. Van de **Filters** , voegt u het nieuwe filter Referentiecel toe aan uw gegevensblok.

   ![Tabblad Filters waarop het filter Sheet1 wordt weergegeven!J1 (Alle gegevens) dat aan de tabel is toegevoegd.](./assets/reference-cell-filter.png)

1. Klikken **Voltooien**.

   Er kan nu naar deze cel worden verwezen door andere gegevensblokken in hun filters. Als u de referentiecel als filter wilt toepassen op andere gegevensblokken, voegt u de celverwijzing vanuit het tabblad Filters gewoon toe aan de bijbehorende filters.

#### De referentiecel gebruiken om gegevensblokfilters te wijzigen

1. Selecteer de referentiecel in het werkblad.

1. Klik op de koppeling onder **Filters uit cel** in het menu Snel bewerken.

   ![Filters van celverbinding die Sheet1 toont!J1 (Alle Gegevens)](./assets/filters-from-cell-link.png)

1. Selecteer het filter in de keuzelijst.

   ![Vervolgkeuzemenu Filter](./assets/filter-drop-down.png)

1. Klikken **Toepassen**.