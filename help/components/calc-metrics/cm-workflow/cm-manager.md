---
description: De Berekende Metrische Manager biedt vele manieren om metriek, zoals het delen, het filtreren, het etiketteren, het goedkeuren, het kopiëren, het schrappen, en het merken als favorieten te leiden.
title: Berekende standaard-beheer
feature: Calculated Metrics
exl-id: 8b257ecc-a596-4b34-ac26-eda16835f1ba
source-git-commit: adbdbc0d8c6eaeb0dd57792170ef8a8a304b424c
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 2%

---

# Het berekende manager van metriek

De berekende metrische pagina biedt vele manieren aan om metriek, zoals het delen, het filtreren, het etiketteren, het goedkeuren, het kopiëren, het schrappen, en het merken als favorieten te leiden.

De Berekende metrische manager toont u alle filters u bezit en die met u zijn gedeeld. Gebruikers op beheerniveau kunnen alle aangepaste maatstaven in de organisatie zien. Dit overzicht geeft de gebruikersinterface en de mogelijkheden van de Berekende metrische manager.

![](assets/calc-metric-manager.png)

## Toegang tot het Berekende manager van metriek

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Berekende cijfers**].

## Beschikbare acties in het beheer van berekende metriek

In het Berekende manager van metriek, kunt u:

* [Berekende maateenheden filteren](/help/components/calc-metrics/cm-workflow/cm-filter.md)

* [Berekende metriek markeren als favorieten](/help/components/calc-metrics/cm-workflow/cm-favorite.md)

* [Berekende standaard goedkeuren](/help/components/calc-metrics/cm-workflow/cm-approving.md)

* [Berekende standaard een label geven](/help/components/calc-metrics/cm-workflow/cm-tagging.md)

* [Berekende standaard delen](/help/components/calc-metrics/cm-workflow/cm-sharing.md)

* Exporteer een berekende metrische waarde naar een CSV-bestand.

* [Berekende cijfers kopiëren](/help/components/calc-metrics/cm-workflow/cm-copy.md)

* Berekende waarden verwijderen

## Kolommen configureren

U kunt de informatie vormen die voor elke berekende metrisch in de Berekende metriekmanager wordt getoond door de kolommen te vormen die worden getoond.

Om de zichtbare kolommen in het Berekende manager van metriek te vormen:

1. Selecteer in Customer Journey Analytics de optie **[!UICONTROL Components]** tab, dan selecteren **[!UICONTROL Calculated metrics]**.

1. Selecteer in het beheer van berekende metriek de optie **Kolommen aanpassen** pictogram ![Het pictogram Kolommen aanpassen](assets/customize-columns-icon.png)selecteert u vervolgens de kolommen die u wilt weergeven in het beheer van berekende metriek.

   De volgende kolommen zijn beschikbaar:

   | Kolomtitel | Beschrijving |
   |---|---|
   | Favorieten | De sterpictogrammen van vertoningen naast elke berekende metrisch, toestaand u om berekende metriek als favorieten te merken. Zie voor meer informatie [Berekende metriek markeren als favorieten](/help/components/calc-metrics/cm-workflow/cm-favorite.md). |
   | Titel en beschrijving | Deze waarden worden verstrekt in de Berekende metrische bouwer. Als u de titel en beschrijving wilt bewerken, selecteert u de titelkoppeling om de builder voor berekende metrische gegevens te openen. |
   | Rapportsuite | Wijst erop in welke rapportreeks metrisch het laatst werd bewaard. |
   | Eigenaar | Geeft aan wie de aangepaste metrische waarde bezit. Als niet-beheerder, kunt u slechts metriek zien u bezit of die met u werden gedeeld. |
   | Tags | Toont markeringen die op metrisch, of door u of door mensen werden toegepast die berekende metrisch met u deelden. |
   | Gedeeld met | Hiermee geeft u personen of groepen (alleen beheerder) of Alles (alleen beheerder) weer waarmee u de berekende metrische waarde hebt gedeeld. <p>Wanneer berekende metrisch wordt gedeeld, toont een aandeelpictogram naast de berekende metrische naam.</p> |
   | Datum gewijzigd | Geeft de datum aan waarop de aangepaste metrische waarde voor het laatst is gewijzigd. |
   | Gebruikt in | **Opmerking:** Deze functionaliteit bevindt zich in de beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het proces van de release van de Customer Journey Analytics raadpleegt u [Release van de Customer Journey Analytics-functie](/help/release-notes/releases.md).<p>Toont hoeveel componenten berekende metrisch momenteel binnen wordt gebruikt. <p>Bijvoorbeeld, als berekende metrisch in 40 projecten en 2 alarm wordt gebruikt, dan toont de waarde van deze kolom zoals [!UICONTROL **42 componenten**].</p> <p>Selecteer de waarde in deze kolom om de uitsplitsing te zien van waar de berekende metrische waarde wordt gebruikt (bijvoorbeeld [!UICONTROL **Projecten (40)**], [!UICONTROL **Waarschuwingen (2)**]).</p><p>Berekende metriek kunnen in om het even welke volgende componenttypes worden gebruikt:</p> <ul><li>Waarschuwingen</li><li>Berekende standaarden</li><li>Projecten</li><li>Geplande projecten</li></ul><p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd.</p><p>Deze informatie omvat geen gebruik van API, Report Builder, of Data Warehouse.</p><p>U kunt de [Gegevenswoordenboek](/help/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie kunt u bijhouden en beter begrijpen hoe componenten in uw organisatie worden gebruikt.</p><p>De [!UICONTROL **Gebruikt in**] wordt niet standaard weergegeven. [Kolommen configureren](#configure-columns) om het weer te geven.</p> |
   | Laatst gebruikt | **Opmerking:** Deze functionaliteit bevindt zich in de beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het proces van de release van de Customer Journey Analytics raadpleegt u [Release van de Customer Journey Analytics-functie](/help/release-notes/releases.md).<p>Toont de datum toen berekende metrisch het laatst in om het even welke volgende componententypes werd gebruikt:</p> <ul><li>Waarschuwingen</li><li>Berekende standaarden</li><li>Projecten</li><li>Geplande projecten</li></ul> <p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, of of het zou moeten worden geschrapt.</p><p>Deze informatie omvat geen gebruik van de API of Report Builder.</p><p>U kunt de [Gegevenswoordenboek](/help/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie kunt u bijhouden en beter begrijpen hoe componenten in uw organisatie worden gebruikt. |

   {style="table-layout:auto"}
