---
description: De Berekende Metrische Manager biedt vele manieren om metriek, zoals het delen, het filtreren, het etiketteren, het goedkeuren, het kopiëren, het schrappen, en het merken als favorieten te leiden.
title: Berekend metrisch beheer
feature: Calculated Metrics
exl-id: 8b257ecc-a596-4b34-ac26-eda16835f1ba
source-git-commit: e994a53934ae25802fb16e912d0fdee32d5ea524
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 0%

---

# Het berekende manager van metriek

De berekende metrische pagina biedt vele manieren aan om metriek, zoals het delen, het filtreren, het etiketteren, het goedkeuren, het kopiëren, het schrappen, en het merken als favorieten te leiden.

De Berekende metrische manager toont u alle filters u bezit en die met u zijn gedeeld. Gebruikers op beheerniveau kunnen alle aangepaste maatstaven in de organisatie zien. Dit overzicht geeft de gebruikersinterface en de mogelijkheden van de Berekende metrische manager.

![ Berekend metriekvenster dat beschikbare filters toont.](assets/calc-metric-manager.png)

## Toegang tot het Berekende manager van metriek

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **Berekende metriek**].

## Beschikbare acties in het beheer van berekende metriek

In het Berekende manager van metriek, kunt u:

* [Berekende maateenheden filteren](/help/components/calc-metrics/cm-workflow/cm-filter.md)

* [Berekende metriek markeren als favorieten](/help/components/calc-metrics/cm-workflow/cm-favorite.md)

* [Berekende waarden goedkeuren](/help/components/calc-metrics/cm-workflow/cm-approving.md)

* [Berekende maatstaven voor tags](/help/components/calc-metrics/cm-workflow/cm-tagging.md)

* [Berekende maatstaven delen](/help/components/calc-metrics/cm-workflow/cm-sharing.md)

* Exporteer een berekende metrische waarde naar een CSV-bestand.

* [Berekende cijfers kopiëren](/help/components/calc-metrics/cm-workflow/cm-copy.md)

* Berekende waarden verwijderen

## Kolommen configureren

U kunt de informatie vormen die voor elke berekende metrisch in de Berekende metriekmanager wordt getoond door de kolommen te vormen die worden getoond.

Om de zichtbare kolommen in het Berekende manager van metriek te vormen:

1. Selecteer in Customer Journey Analytics de tab **[!UICONTROL Components]** en selecteer vervolgens **[!UICONTROL Calculated metrics]** .

1. In de Berekende metriekmanager, selecteer **aanpassen kolommen** pictogram ![ aanpassen kolompictogram ](assets/customize-columns-icon.png), dan selecteer de kolommen die u in de Berekende metriekmanager wilt worden getoond.

   De volgende kolommen zijn beschikbaar:

   | Kolomtitel | Beschrijving |
   |---|---|
   | Favorieten | De sterpictogrammen van vertoningen naast elke berekende metrisch, toestaand u om berekende metriek als favorieten te merken. Voor meer informatie, zie [ Markeer berekende metriek als favorieten ](/help/components/calc-metrics/cm-workflow/cm-favorite.md). |
   | Titel en beschrijving | Deze waarden worden verstrekt in de Berekende metrische bouwer. Als u de titel en beschrijving wilt bewerken, selecteert u de titelkoppeling om de builder voor berekende metrische gegevens te openen. |
   | Rapportsuite | Wijst erop in welke rapportreeks metrisch het laatst werd bewaard. |
   | Eigenaar | Geeft aan wie de aangepaste metrische waarde bezit. Als niet-beheerder, kunt u slechts metriek zien u bezit of die met u werden gedeeld. |
   | Tags | Toont markeringen die op metrisch, of door u of door mensen werden toegepast die berekende metrisch met u deelden. |
   | Gedeeld met | Hiermee geeft u personen of groepen (alleen beheerder) of Alles (alleen beheerder) weer waarmee u de berekende metrische waarde hebt gedeeld. <p>Wanneer berekende metrisch wordt gedeeld, toont een aandeelpictogram naast de berekende metrische naam.</p> |
   | Datum gewijzigd | Geeft de datum aan waarop de aangepaste metrische waarde voor het laatst is gewijzigd. |
   | Gebruikt in | Hiermee kunt u zien waar berekende metriek momenteel worden gebruikt en hoe vaak deze in elk gebied worden gebruikt. <p>Bijvoorbeeld, als berekende metrisch in 40 projecten en 2 alarm wordt gebruikt, dan toont de waarde van deze kolom als [!UICONTROL **42 componenten**]. <p>Selecteer de waarde in deze kolom om de uitsplitsing te zien van waar de berekende metriek (bijvoorbeeld, [!UICONTROL **Projecten (40)**] worden gebruikt, [!UICONTROL **Mobiele Scorecards (2)**]). Bovendien kunt u de lijst van punten bekijken waar de berekende metriek worden gebruikt. Bijvoorbeeld, om de lijst van projecten te zien waar zij worden gebruikt, selecteer de [!UICONTROL **Projecten (40)**] verbinding.</p><p>Elk van de volgende gebieden toont het aantal instanties van berekende metriek die in dat gebied worden gebruikt:</p> <ul><li>[!UICONTROL **Projecten**]<p>Bevat berekende metriek die [ in de berekende metrische bouwer ](/help/components/apply-create-metrics.md#create-calculated-metrics-for-all-projects) werden gecreeerd en voor alle projecten beschikbaar zijn.</p></li><li>[!UICONTROL **Ad hoc componenten**]<p>Bevat berekende metriek die [ als snelle berekende metriek ](/help/components/apply-create-metrics.md#create-calculated-metrics-for-a-single-project) werden gecreeerd en beschikbaar slechts binnen één enkel project zijn.</p></li><li>[!UICONTROL **Geplande projecten**]</li><li>[!UICONTROL **Mobiele Scorecards**]</li><li>[!UICONTROL **Annotaties**]</li><li>[!UICONTROL **Report Builder**]<p>Als u deze optie selecteert, wordt een CSV-bestand gedownload met de volgende kolommen gegevens:</p><ul><li>Naam Report Builder</li><li>Laatst geopend</li><li>Laatst geopende IMS-gebruikersnaam</li><li>Laatst geopende gebruikersnaam</li></ul><p>Wanneer u informatie voor Report Builder bekijkt, zijn de gebruiksgegevens beschikbaar vanaf september 2024.</p></li></ul><p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, waar het wordt gebruikt, en of het moet worden geschrapt of worden gewijzigd.</p><p>Houd rekening met het volgende wanneer u deze kolom weergeeft:</p><ul><li>Deze informatie is alleen beschikbaar voor systeembeheerders.</li><li>[!UICONTROL **Gebruikt in**] kolom toont niet door gebrek. [ vorm kolommen ](#configure-columns) om het te tonen.</li><li>Als berekende metrisch andere berekende metrisch in zijn definitie omvat, wordt om het even welk gebruik van die berekende metrisch niet getoond in [!UICONTROL **gebruikt in**] kolom. Als berekende metrisch inbegrepen in de definitie van een ander type van component (zoals een filter) is, dan wordt het gebruik getoond in [!UICONTROL **Gebruikt in**] kolom.</li><li>Deze informatie omvat geen gebruik van de API of Data Warehouse.</li><li>Als er geen gegevens in deze kolom voor een bepaalde component zijn maar het heeft a [!UICONTROL **laatst gebruikte**] datum, zou de component in een analyse kunnen worden gebruikt zonder worden bewaard.</li><li>Gebruiksgegevens zijn beschikbaar vanaf september 2023.</li></ul><p>U kunt het [ Woordenboek van Gegevens ](/help/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie gebruiken om u spoor van te houden en beter te begrijpen hoe de componenten in uw organisatie worden gebruikt.</p> |
   | Laatst gebruikt | Toont de datum toen berekende metrisch het laatst in om het even welke volgende componententypes werd gebruikt: <ul><li>Berekende cijfers</li><li>Projecten</li><li>Geplande projecten</li></ul> <p>Deze informatie kan u helpen bepalen of een component voor gebruikers in uw organisatie waardevol is, of of het zou moeten worden geschrapt.</p><p>Houd rekening met het volgende wanneer u deze kolom weergeeft:</p><ul><li>Deze informatie omvat geen gebruik van API, Report Builder, of Data Warehouse.</li><li>Voor sommige componenten bevat deze kolom mogelijk geen gegevens als de component voor het laatst is gebruikt vóór september 2023.</li><li>Deze informatie is alleen beschikbaar voor systeembeheerders.</li></ul><p>U kunt het [ Woordenboek van Gegevens ](/help/components/data-dictionary/data-dictionary-overview.md) samen met deze informatie gebruiken om u spoor van te houden en beter te begrijpen hoe de componenten in uw organisatie worden gebruikt. |

   {style="table-layout:auto"}
