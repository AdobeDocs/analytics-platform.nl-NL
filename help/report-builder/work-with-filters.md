---
title: Hoe worden segmenten in Report Builder in Customer Journey Analytics gebruikt?
description: Beschrijft hoe te om segmenten in Report Builder voor Customer Journey Analytics te gebruiken
role: User
feature: Report Builder
type: Documentation
exl-id: 1f39d7f4-b508-45d8-9b97-81242c3805d3
solution: Customer Journey Analytics
source-git-commit: bd2d45b9fc1380e36fc482ee75e1a9bbb26f6cf7
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# Werken met segmenten in Report Builder

U kunt Segmenten toepassen wanneer u een nieuw gegevensblok creeert of wanneer u **uitgezocht geef gegevensblok** optie van het paneel van BEVELINGEN uit.

## Segmenten toepassen op een gegevensblok

Als u een segment wilt toepassen op het volledige gegevensblok, dubbelklikt u op een segment of sleept u segmenten uit de lijst met componenten naar de sectie Segmenten van de tabel.

## Segmenten toepassen op afzonderlijke metriek

Als u segmenten wilt toepassen op afzonderlijke metrische elementen, sleept u een segment naar een metrische waarde in de tabel. U kunt **ook klikken...** pictogram aan het recht van metrisch in de ruit van de Lijst en dan selecteren **metrisch segment**. Als u toegepaste segmenten wilt weergeven, plaatst u de muisaanwijzer boven of selecteert u een metrische waarde in het deelvenster Tabel. De metriek met toegepaste segmenten tonen een segmentpictogram.

![ segmentlusje die metriek tonen.](./assets/filter_by.png)

## Snel segmenten bewerken

Met het deelvenster Snel bewerken kunt u segmenten voor bestaande gegevensblokken toevoegen, verwijderen of vervangen.

Wanneer u een waaier van cellen in spreadsheet selecteert, de **verbinding van Segmenten** in Snel uitgeeft paneel toont een summiere lijst van de segmenten die door de gegevensblokken in die selectie worden gebruikt.

Segmenten bewerken met het deelvenster Snel bewerken

1. Selecteer een bereik cellen uit een of meerdere gegevensblokken.

   ![ Snel geef segmentpaneel uit die segmentopties voor gegevensmeningen, datumwaaier, en segmenten tonen.](./assets/select_multiple_dbs.png)

1. Klik op de koppeling Segmenten om het deelvenster Snel bewerken - Segmenten te starten.

   ![ het segmentpaneel dat het Add segmentgebied en toegepaste segmenten toont.](./assets/quick_edit_filters.png)

### Een segment toevoegen of verwijderen

U kunt segmenten toevoegen of verwijderen met de opties Toevoegen/Verwijderen.

1. Selecteer **toevoegen/verwijderen** lusje in Snel geef-segmenten paneel uit.

   Alle segmenten die zijn toegepast op de geselecteerde gegevensblokken, worden weergegeven in het deelvenster Snel bewerken-segmenten. De segmenten die op alle gegevensblokken in de selectie worden toegepast worden vermeld onder **op alle geselecteerde gegevensblokken** rubriek worden toegepast. De segmenten die op sommige maar niet alle gegevensblokken worden toegepast zijn vermeld onder **op 1 of meer geselecteerde gegevensblokken** rubriek worden toegepast.

   Wanneer de veelvoudige segmenten in de geselecteerde gegevensblokken aanwezig zijn, kunt u naar specifieke segmenten zoeken gebruikend **toevoegen het onderzoeksgebied van het Segment**.

   ![ het Add segmentgebied.](./assets/add_filter.png)

1. Voeg segmenten toe door segmenten van **te selecteren voeg segment** drop-down menu toe.

   De lijst met doorzoekbare segmenten bevat alle segmenten die toegankelijk zijn voor de gegevensweergaven die aanwezig zijn in een of meer van de geselecteerde gegevensblokken en alle segmenten die wereldwijd beschikbaar zijn in de organisatie.

   Als u een segment toevoegt, wordt het segment toegepast op alle gegevensblokken in de selectie.

1. Om segmenten te verwijderen, klik het schrappingspictogram **x** rechts van segmenten in de **toegepaste Segmenten** lijst.

1. Klik **toepassen** om veranderingen te bewaren en aan het hubpaneel terug te keren.

   Report Builder geeft een bericht weer ter bevestiging van de toegepaste segmentwijzigingen.

### Een segment vervangen

U kunt een bestaand segment vervangen door een ander segment om te wijzigen hoe de gegevens worden gesegmenteerd.

1. Selecteer **vervangen** lusje in Snel geef-segmenten paneel uit.

   ![ selecteer Replace tabel.](./assets/replace_filter.png)

1. Gebruik het **de lijst van het Onderzoek** onderzoeksgebied om van specifieke segmenten de plaats te bepalen.

1. Kies een of meer segmenten die u wilt vervangen.

1. Zoeken naar een of meer segmenten in het veld Vervangen door.

   Het selecteren van een segment voegt het aan **toe vervangt met**... lijst.

   ![ het Replace lusje met de Mensen op App geselecteerde gegevensblok en Replace met lijst die Personen op Herziene App tonen.](./assets/replace_screen_new.png)

1. Klik **toepassen**.

   Report Builder werkt de lijst met segmenten bij om de vervanging te weerspiegelen.

### Gegevensbloksegmenten vanuit cel definiëren

Gegevensblokken kunnen verwijzen naar segmenten uit een cel. De veelvoudige gegevensblokken kunnen de zelfde cel voor segmenten van verwijzingen voorzien, toestaand u om segmenten voor veelvoudige gegevensblokken tegelijkertijd gemakkelijk te schakelen.

Segmenten uit een cel toepassen

1. Navigeer naar stap 2 in het maken of bewerken van gegevensblokken. Zie [ een Blok van Gegevens ](./create-a-data-block.md) creëren.
1. Klik het **lusje van Segmenten** om segmenten te bepalen.
1. Klik **creeer segment van cel**.

   ![ creeer segment van celpictogram.](./assets/create-filter-from-cell.png)

1. Selecteer de cel waaruit u wilt dat de gegevensblokken naar een segment verwijzen.

1. Voeg het segment toe dat u aan de cel wilt toevoegen door te dubbelklikken op het segment of door het segment te slepen naar de sectie Segmenten inclusief.

   Opmerking: Er kan slechts één keuze voor de desbetreffende cel tegelijk worden geselecteerd.

   ![ voegt segment van celvenster toe die de inbegrepen segmenten tonen.](./assets/select-filters.png)

1. Klik **toepassen** om de verwijzingscel tot stand te brengen.

1. Van het **lusje van Segmenten**, voeg het pas gecreëerde segment van de verwijzingscel aan uw gegevensblok toe.

   ![ segmenten lusje die Sheet1 tonen!J1 (Alle Gegevens) segment dat aan de lijst wordt toegevoegd.](./assets/reference-cell-filter.png)

1. Klik **Afwerking**.

   Nu kan naar deze cel worden verwezen door andere gegevensblokken in hun segmenten. Als u de referentiecel als een segment wilt toepassen op andere gegevensblokken, voegt u de celverwijzing vanuit het tabblad Segmenten toe aan de segmenten ervan.

#### De referentiecel gebruiken om gegevensbloksegmenten te wijzigen

1. Selecteer de referentiecel in het werkblad.

1. Klik de verbinding onder **Segmenten van Cel** in Snel uitgeven menu.

   ![ segmenten van celverbinding die Sheet1 tonen!J1 (Alle Gegevens) ](./assets/filters-from-cell-link.png)

1. Selecteer het segment in het keuzemenu.

   ![ segment drop-down menu ](./assets/filter-drop-down.png)

1. Klik **toepassen**.
