---
title: Wat zijn componenten in Customer Journey Analytics?
description: Leer welke componenten CJA aanbiedt, en hoe u hen in rapportering kunt gebruiken.
exl-id: f9b0b3c2-7c88-4bef-af33-0d309cafe799
solution: Customer Journey Analytics
feature: Components
source-git-commit: 440a23258b0a4bd024894168e3201ee0c2d5c756
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 6%

---

# Overzicht van onderdelen

Componenten zijn functies in Customer Journey Analytics die kunnen worden gebruikt in rapporten of als aanvulling op rapportagefuncties. U kunt deze componenten als volgt beheren:

1. Aanmelden bij [analytics.adobe.com](https://analytics.adobe.com) je Adobe ID-gebruikersgegevens gebruiken.
2. Navigeren naar [!UICONTROL Components] > [!UICONTROL Components] in het koptekstmenu.

U kunt de volgende componenten beheren:

* [**Annotaties**](/help/components/annotations/overview.md): Communiceer contextuele gegevensnuances en inzichten aan uw organisatie.
* [**Filters**](filters/filters-overview.md): Delen van uw gegevens uitsluiten om de nadruk te leggen op elementen met een gemeenschappelijke dimensie
* [**Berekende cijfers**](calc-metrics/calc-metr-overview.md): Metriek en formules gebruiken als nieuwe componenten voor rapportage
* [**Datumbereiken**](date-ranges/overview.md): De datumbereiken aanpassen en verfijnen die Analysis Workspace biedt
* [**Projecten**](/help/analysis-workspace/home.md): Uw projecten organiseren en onderhouden in Analysis Workspace

## Analysis Workspace-componenten

Componenten in Analysis Workspace bestaan uit metriek, afmetingen, filters en tijdkorreligheid die u naar een project kunt slepen en neerzetten. Aangepaste componenten die u maakt, worden aan deze deelvensters toegevoegd, zoals aangepaste datumbereiken.

Als u het deelvenster Componenten wilt openen, klikt u op de knop **[!UICONTROL Components]** in de linkerspoorstaaf. U kunt schakelen tussen deelvensters (leeg deelvenster, [Deelvenster Vrije vorm](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md), [Snelle inzichten](/help/analysis-workspace/c-panels/quickinsight.md), of [Attribution IQ](/help/analysis-workspace/c-panels/attribution.md) paneel), [Visualisaties](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md)en Componenten die de pictogrammen van de linkerspoorstaaf of het gebruik van [sneltoetsen](/help/analysis-workspace/build-workspace-project/fa-shortcut-keys.md).

![](assets/components.png)

Zie [Een project maken](/help/analysis-workspace/home.md) voor informatie over het gebruiken van Componenten in een project.

## Componenthandelingen

U kunt componenten (afzonderlijk of door meer dan één te selecteren) op verschillende manieren beheren. Klik met de rechtermuisknop op een component of klik op **[!UICONTROL Actions]** boven aan de lijst met componenten.

>[!NOTE]
>
>Deze handelingen zijn niet van toepassing op tijdcomponenten.

| Component Handeling | Beschrijving |
| --- | --- |
| Tag | U kunt componenten ordenen of beheren door er tags op toe te passen. Het verschijnt dan in de respectieve componentenmanager, zoals [!UICONTROL Analytics] > [!UICONTROL Components] > [!UICONTROL Filters], of [!UICONTROL Analytics] > [!UICONTROL Components] > [!UICONTROL Projects] |
| Favorieten | Voeg de component toe aan de lijst met favorieten. Het verschijnt dan in de respectieve componentenmanager, zoals [!UICONTROL Analytics] > [!UICONTROL Components] > [!UICONTROL filters], of [!UICONTROL Analytics] > [!UICONTROL Components] > [!UICONTROL Projects]. |
| Goedkeuren | Keur de component goed om deze canonicaal te maken. Het verschijnt dan in de respectieve componentenmanager, zoals [!UICONTROL Analytics] > [!UICONTROL Components] > [!UICONTROL Filters], of  [!UICONTROL Analytics] > [!UICONTROL Components] > [!UICONTROL Projects] |
| Delen | Alleen van toepassing op filters. |
| Verwijderen | Alleen van toepassing op filters. |

Bekijk de video over het maken van statistieken, filters en datums:

>[!VIDEO](https://video.tv.adobe.com/v/23979)

## Componenten beheren {#actions}

U kunt componenten rechtstreeks in de linkerspoorstaaf beheren.

1. Klik met de rechtermuisknop op een component.

   of

   Selecteer een component en selecteer vervolgens de **Handeling** (3 punten) boven aan de lijst met componenten.

   >[!TIP]
   >
   >   U kunt meerdere componenten selecteren door Shift ingedrukt te houden of door Command (in Mac) of Ctrl (in Windows) ingedrukt te houden.


   ![](assets/component-actions.png)

   | Component, actie | Beschrijving |
   |--- |--- |
   | [!UICONTROL **Tag**] | U kunt componenten ordenen of beheren door er tags op toe te passen. U kunt vervolgens zoeken op tag in de linkertrack door op het filter te klikken of # te typen. Tags fungeren ook als filters in de componentmanagers. |
   | [!UICONTROL **Favorieten**] | Voeg de component toe aan de lijst met favorieten. Net als tags kunt u zoeken op Favorieten in het linkerspoor en deze filteren in de componentmanagers. |
   | [!UICONTROL **Goedkeuren**] | Markeer componenten zoals Goedgekeurd om aan uw gebruikers te laten weten dat de component door de organisatie is goedgekeurd. Net als tags kunt u zoeken op Goedgekeurd in de linkertrack en door hen filteren in de componentmanagers. |
   | [!UICONTROL **Delen**] | Delen van componenten naar gebruikers in uw organisatie. Deze optie is alleen beschikbaar voor aangepaste componenten, zoals filters of berekende meetwaarden. |
   | [!UICONTROL **Verwijderen**] | Verwijder componenten die u niet meer nodig hebt. Deze optie is alleen beschikbaar voor aangepaste componenten, zoals filters of berekende meetwaarden. |

De componenten van de douane kunnen ook door hun respectieve managers van de Component worden beheerd. De [Filters beheren](/help/components/filters/manage-filters.md).

## De componentenlijst zoeken, filteren en sorteren

U kunt zoeken, filteren en sorteren de componentenlijst in de linkerspoor van Analysis Workspace om van een bepaalde component snel de plaats te bepalen.

### De componentenlijst doorzoeken

1. Selecteer **Componenten** pictogram ![Pictogram Componenten](assets/components-icon.png) in het linkerspoor.

1. Typ in het zoekveld de naam van de component die u in het project wilt gebruiken.

   Het type component kan door zowel kleur als pictogram worden geïdentificeerd. **Dimension** ![Dimension-pictogram](assets/dimension-icon.png) oranje zijn, **Filters** ![Filterpictogram](assets/segment-icon.png) blauw zijn, **Datumbereiken** ![Pictogram Datumbereik](assets/date-range-icon.png) paars zijn, en **Metrisch** ![Metrisch pictogram](assets/default-metric-icon.png) zijn groen. Het pictogram Adobe ![Adobe-pictogram](assets/default-calc-metric-icon.png) Hiermee wordt een berekende metrische sjabloon of een filtersjabloon aangegeven en wordt het rekenprijspictogram weergegeven ![Pictogram Rekenmachine](assets/calculated-metric-icon-created.png) wees op berekende metrisch die door een beheerder van Analytics in uw organisatie werd gecreeerd.

1. Selecteer de component wanneer deze in de vervolgkeuzelijst wordt weergegeven.

### De componentlijst filteren

1. Selecteer **Componenten** pictogram ![Pictogram Componenten](assets/components-icon.png) in het linkerspoor.

1. Selecteer **Filter** pictogram ![Filter gegevenswoordenboek, pictogram](assets/components-filter-icon.png).

   of

   Typ het hekje (#) in het zoekveld.

1. Selecteer een van de volgende filteropties om de lijst met componenten te filteren:

   | Optie | -functie |
   |---------|----------|
   | [!UICONTROL **Goedgekeurd**] | Alleen componenten tonen die zijn gemarkeerd als goedgekeurd door een beheerder. |
   | [!UICONTROL **Favorieten**] | Alleen componenten tonen die zich in de lijst Favorieten bevinden. Voor informatie over het toevoegen van componenten aan uw lijst van favorieten, zie [Componenten beheren](#manage-components). |
   | [!UICONTROL **Dimensies**] | Alleen componenten weergeven die Dimension zijn. |
   | [!UICONTROL **Cijfers**] | Alleen componenten weergeven die Metrisch zijn. |
   | [!UICONTROL **Filters**] | Alleen componenten weergeven die filters zijn. |
   | [!UICONTROL **Datumbereiken**] | Alleen componenten tonen die Datumbereik hebben. |
   | [!UICONTROL **Alles tonen**] | Alle componenten tonen. Deze optie is alleen beschikbaar voor beheerders. |
   | [!UICONTROL **Niet goedgekeurd**] | Alleen componenten tonen die nog niet zijn gemarkeerd als goedgekeurd door een beheerder. Als beheerder, is dit nuttig wanneer het identificeren van componenten die uw overzicht en goedkeuring vereisen. Deze optie is alleen beschikbaar voor beheerders. |

1. (Optioneel) Als u de lijst verder wilt uitlijnen, kunt u de lijst met componenten sorteren, zoals beschreven in [De componentlijst sorteren](#sort-the-component-list).

### De componentlijst sorteren

{{release-limited-testing-section}}

1. (Optioneel) Pas filters toe op de lijst met componenten, zoals beschreven in [De componentlijst filteren](#filter-the-component-list).

1. Selecteer **Componenten** pictogram ![Pictogram Componenten](assets/components-icon.png) in het linkerspoor.

1. Selecteer **Sorteren** pictogram ![Pictogram Componenten sorteren](assets/component-sort-icon.png)Selecteer vervolgens een van de volgende filteropties om de lijst met componenten te sorteren:

   {{components-sort-options}}

## Machtigingen voor componenttoegang

In Analysis Workspace kunnen beheerders [krullen](/help/analysis-workspace/curate-share/curate.md) welke componenten bij de rapportage aan gebruikers worden blootgesteld.
