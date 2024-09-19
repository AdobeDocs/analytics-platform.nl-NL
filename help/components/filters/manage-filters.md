---
title: Filterbeheer
description: hoe u filters in Customer Journey Analytics kunt beheren
exl-id: b8869560-0cf1-4e5d-a03c-dfca85d05e66
feature: Filters
role: User
source-git-commit: e994a53934ae25802fb16e912d0fdee32d5ea524
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 0%

---

# Filterbeheer

De Filtermanager biedt vele manieren aan om filters, zoals het delen, het etiketteren, het goedkeuren, het kopiëren, het schrappen, en het merken als favorieten te leiden.

In Filterbeheer worden alle filters weergegeven die u hebt en die met u zijn gedeeld. Gebruikers op beheerniveau kunnen alle filters in de organisatie zien. In dit overzicht worden de gebruikersinterface en de mogelijkheden van Filters Manager weergegeven.

![](assets/filter-manager-ui.png)

## Toegang krijgen tot Filters Manager

1. Selecteer in Customer Journey Analytics de tab **[!UICONTROL Components]** en selecteer vervolgens **[!UICONTROL Filters]** .

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

1. Selecteer in Customer Journey Analytics de tab **[!UICONTROL Components]** en selecteer vervolgens **[!UICONTROL Filers]** .

1. In de manager van Filters, selecteer **kolommen** pictogram ![ aanpassen kolommen pictogram ](assets/customize-columns-icon.png), dan selecteer de kolommen die u in de manager van Filters wilt worden getoond.

   De volgende kolommen zijn beschikbaar:

   | Kolomtitel | Beschrijving |
   |---|---|
   | Titel en beschrijving | Deze waarden zijn opgenomen in de filterconstructor. Als u de titel en beschrijving wilt bewerken, selecteert u de titelkoppeling om de Filterbouwer te openen. |
   | Favorieten | Hiermee geeft u sterpictogrammen weer naast elk filter, zodat u filters kunt markeren als favorieten. Voor meer informatie, zie [ filters van het Teken als favorieten ](/help/components/filters/filters-favorite.md). |
   | Gegevens, weergave | Deze kolom geeft aan in welke gegevensweergave het filter het laatst is opgeslagen. |
   | Eigenaar | Hiermee wordt aangegeven wie de eigenaar van het filter is. Als niet-beheerder kunt u alleen filters zien die u bezit of die met u gedeeld zijn. |
   | Labels (niet gecontroleerd in kolomkiezer, vandaar dat de kolom niet wordt weergegeven) | Tags die op het filter zijn toegepast, door u of door personen die het filter met u hebben gedeeld. |
   | Gedeeld met | Hier worden personen of groepen weergegeven (alleen Admin) of Alle personen (alleen Admin) waarmee u het filter hebt gedeeld. <p>Wanneer een filter door u of met u wordt gedeeld, wordt een pictogram voor delen weergegeven naast de filternaam.</p> |
   | Datum gewijzigd | Hiermee wordt de datum weergegeven waarop het filter voor het laatst is gewijzigd. |
   | Gebruikt in | Hiermee kunt u zien waar filters momenteel worden gebruikt en hoe vaak ze in elk gebied worden gebruikt. <p>Bijvoorbeeld, als de filter in 40 projecten en 2 alarm wordt gebruikt, dan toont de waarde van deze kolom als [!UICONTROL **42 componenten**].</p> <p>Selecteer de waarde in deze kolom om de uitsplitsing te zien van waar de filters (bijvoorbeeld, [!UICONTROL **Projecten (40)**] worden gebruikt, [!UICONTROL **Mobiele Scorecards (2)**]). Bovendien kunt u de lijst met items weergeven waarin de filters worden gebruikt. Bijvoorbeeld, zie zo de lijst van projecten waar zij worden gebruikt, selecteer de [!UICONTROL **Projecten (40)**] verbinding.</p><p>Elk van de volgende gebieden toont het aantal instanties van filters die in dat gebied worden gebruikt:</p>  <ul><li>[!UICONTROL **Projecten**]<p>Bevat filters die [ in de filterbouwer ](/help/components/filters/filter-builder.md#) werden gecreeerd en voor alle projecten beschikbaar zijn.</p></li><li>[!UICONTROL **Ad hoc componenten**]<p>Bevat filters die [ als snelle filters ](/help/components/filters/quick-filters.md) werden gecreeerd en beschikbaar slechts binnen één enkel project zijn.</p></li><li>[!UICONTROL **Geplande projecten**]</li><li>[!UICONTROL **Mobiele Scorecards**]</li><li>[!UICONTROL **Annotaties**]</li><li>[!UICONTROL **Berekende standaarden**]</li><li>[!UICONTROL **Report Builder**]<p>Als u deze optie selecteert, wordt een CSV-bestand gedownload met de volgende kolommen gegevens:</p><ul><li>Naam Report Builder</li><li>Laatst geopend</li><li>Laatst geopende IMS-gebruikersnaam</li><li>Laatst geopende gebruikersnaam</li></ul></li><p>Wanneer u informatie voor Report Builder bekijkt, zijn de gebruiksgegevens beschikbaar vanaf september 2024.</p></ul><p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd.</p><p>Houd rekening met het volgende wanneer u deze kolom weergeeft:</p><ul><li>Deze informatie is alleen beschikbaar voor systeembeheerders.</li><li>[!UICONTROL **Gebruikt in**] kolom toont niet door gebrek. [ vorm kolommen ](#configure-columns) om het te tonen.</li><li>Als een filter een andere filter in zijn definitie omvat, wordt om het even welk gebruik van die filter niet getoond in [!UICONTROL **Gebruikt in**] kolom. Als een filter in de definitie van een ander type van component (zoals berekend metrisch) inbegrepen is, dan wordt het gebruik getoond in [!UICONTROL **Gebruikt in**] kolom.</li><li>Deze informatie omvat geen gebruik van de API of Data Warehouse.</li><li>Als er geen gegevens in deze kolom voor een bepaalde component zijn maar het heeft a [!UICONTROL **laatst gebruikte**] datum, zou de component in een analyse kunnen worden gebruikt zonder worden bewaard.</li><li>Gebruiksgegevens zijn beschikbaar vanaf september 2023.</li></ul><p>U kunt het [ Woordenboek van Gegevens ](/help/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie gebruiken om u spoor van te houden en beter te begrijpen hoe de componenten in uw organisatie worden gebruikt.</p> |
   | Laatst gebruikt | Hiermee geeft u de datum weer waarop het filter voor het laatst is gebruikt in een van de volgende componenttypen: <ul><li>Berekende cijfers</li><li>Projecten</li><li>Geplande projecten</li><li>Filters</li></ul> <p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, of of het zou moeten worden geschrapt.</p><p>Houd rekening met het volgende wanneer u deze kolom weergeeft:</p><ul><li>Deze informatie omvat geen gebruik van API, Report Builder, of Data Warehouse.</li><li>Voor sommige componenten bevat deze kolom mogelijk geen gegevens als de component voor het laatst is gebruikt vóór september 2023.</li><li>Deze informatie is alleen beschikbaar voor systeembeheerders.</li></ul><p>U kunt het [ Woordenboek van Gegevens ](/help/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie gebruiken om u spoor van te houden en beter te begrijpen hoe de componenten in uw organisatie worden gebruikt. |

   {style="table-layout:auto"}
