---
title: Filterbeheer
description: hoe u filters in Customer Journey Analytics kunt beheren
exl-id: b8869560-0cf1-4e5d-a03c-dfca85d05e66
feature: Filters
role: User
source-git-commit: e84010b9ea9e6385574e8b1a04f7eccbba3ebc90
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Filterbeheer

De Filtermanager biedt vele manieren aan om filters, zoals het delen, het etiketteren, het goedkeuren, het kopiëren, het schrappen, en het merken als favorieten te leiden.

In Filterbeheer worden alle filters weergegeven die u hebt en die met u zijn gedeeld. Gebruikers op beheerniveau kunnen alle filters in de organisatie zien. In dit overzicht worden de gebruikersinterface en de mogelijkheden van Filters Manager weergegeven.

![](assets/filter-manager-ui.png)

## Toegang krijgen tot Filters Manager

1. Selecteer in Customer Journey Analytics de optie **[!UICONTROL Components]** tab, dan selecteren **[!UICONTROL Filters]**.

## Beschikbare acties in Filterbeheer

In het venster Filters kunt u:

* [De lijst met filters filteren](/help/components/filters/filters-filter.md)

* [Filters markeren als favorieten](/help/components/filters/filters-favorite.md)

* [Filters goedkeuren](/help/components/filters/filters-approve.md)

* [Labelfilters](/help/components/filters/filters-tag.md)

* [Filters delen](/help/components/filters/filters-share.md)

* Exporteer een filter naar een CSV-bestand.

* [Filters kopiëren](/help/components/filters/filters-copy.md)

* Filters verwijderen

## Kolommen configureren

U kunt de informatie vormen die voor elk filter in de manager van Filters wordt getoond door de kolommen te vormen die worden getoond.

U configureert als volgt de zichtbare kolommen in Filters:

1. Selecteer in Customer Journey Analytics de optie **[!UICONTROL Components]** tab, dan selecteren **[!UICONTROL Filers]**.

1. Selecteer in Filters Manager de optie **Kolommen aanpassen** pictogram ![Het pictogram Kolommen aanpassen](assets/customize-columns-icon.png)Selecteer vervolgens de kolommen die u wilt weergeven in Filters Manager.

   De volgende kolommen zijn beschikbaar:

   | Kolomtitel | Beschrijving |
   |---|---|
   | Titel en beschrijving | Deze waarden zijn opgenomen in de filterconstructor. Als u de titel en beschrijving wilt bewerken, selecteert u de titelkoppeling om de Filterbouwer te openen. |
   | Favorieten | Hiermee geeft u sterpictogrammen weer naast elk filter, zodat u filters kunt markeren als favorieten. Zie voor meer informatie [Filters markeren als favorieten](/help/components/filters/filters-favorite.md). |
   | Gegevens, weergave | Deze kolom geeft aan in welke gegevensweergave het filter het laatst is opgeslagen. |
   | Eigenaar | Hiermee wordt aangegeven wie de eigenaar van het filter is. Als niet-beheerder kunt u alleen filters zien die u bezit of die met u gedeeld zijn. |
   | Labels (niet gecontroleerd in kolomkiezer, vandaar dat de kolom niet wordt weergegeven) | Tags die op het filter zijn toegepast, door u of door personen die het filter met u hebben gedeeld. |
   | Gedeeld met | Hier worden personen of groepen weergegeven (alleen Admin) of Alle personen (alleen Admin) waarmee u het filter hebt gedeeld. <p>Wanneer een filter door u of met u wordt gedeeld, wordt een pictogram voor delen weergegeven naast de filternaam.</p> |
   | Datum gewijzigd | Hiermee wordt de datum weergegeven waarop het filter voor het laatst is gewijzigd. |
   | Gebruikt in | Hiermee wordt getoond in hoeveel componenten het filter momenteel wordt gebruikt. <p>Bijvoorbeeld, als de filter in 40 projecten en 2 alarm wordt gebruikt, dan toont de waarde van deze kolom zoals [!UICONTROL **42 componenten**].</p> <p>Selecteer de waarde in deze kolom om de uitsplitsing te zien van waar het filter wordt gebruikt (bijvoorbeeld [!UICONTROL **Projecten (40)**], [!UICONTROL **Waarschuwingen (2)**]).</p><p>Filters kunnen in elk van de volgende componenttypen worden gebruikt:</p> <ul><li>Berekende cijfers</li><li>Projecten</li><li>Geplande projecten</li></ul><p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd.</p><p>Houd rekening met het volgende wanneer u deze kolom weergeeft:</p><ul><li>Deze informatie omvat geen gebruik van API, Report Builder, of Data Warehouse.</li><li>De [!UICONTROL **Gebruikt in**] wordt niet standaard weergegeven. [Kolommen configureren](#configure-columns) om het weer te geven.</li><li>Als deze kolom geen gegevens bevat voor een bepaalde component, maar deze een [!UICONTROL **Laatst gebruikt**] datum, kan de component in een analyse zijn gebruikt zonder worden bewaard.</li><li>Deze informatie is alleen beschikbaar voor systeembeheerders.</li></ul><p>U kunt de [Gegevenswoordenboek](/help/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie kunt u bijhouden en beter begrijpen hoe componenten in uw organisatie worden gebruikt.</p> |
   | Laatst gebruikt | Hiermee geeft u de datum weer waarop het filter voor het laatst is gebruikt in een van de volgende componenttypen: <ul><li>Berekende cijfers</li><li>Projecten</li><li>Geplande projecten</li><li>Filters</li></ul> <p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, of of het zou moeten worden geschrapt.</p><p>Houd rekening met het volgende wanneer u deze kolom weergeeft:</p><ul><li>Deze informatie omvat geen gebruik van API, Report Builder, of Data Warehouse.</li><li>Voor sommige componenten bevat deze kolom mogelijk geen gegevens als de component voor het laatst is gebruikt vóór september 2023.</li><li>Deze informatie is alleen beschikbaar voor systeembeheerders.</li></ul><p>U kunt de [Gegevenswoordenboek](/help/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie kunt u bijhouden en beter begrijpen hoe componenten in uw organisatie worden gebruikt. |

   {style="table-layout:auto"}
