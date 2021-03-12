---
title: Overzicht van onderdelen
description: Leer welke componenten CJA aanbiedt, en hoe u hen in rapportering kunt gebruiken.
translation-type: tm+mt
source-git-commit: c1699c4319b3b840d8420f3ffa1a4bd1c1d9a4d4
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 17%

---


# Overzicht van onderdelen

Componenten zijn functies in Customer Journey Analytics die kunnen worden gebruikt in rapporten of als aanvulling op rapportagefuncties. U kunt deze componenten als volgt beheren:

1. Meld u met uw Adobe ID-gegevens aan bij [analytics.adobe.com](https://analytics.adobe.com).
2. Navigeer naar [!UICONTROL Components] > [!UICONTROL Components] in het koptekstmenu.

U kunt de volgende componenten beheren:

* [**Filters**](filters/filters-overview.md): Delen van uw gegevens uitsluiten om de nadruk te leggen op elementen met een gemeenschappelijke dimensie
* [**Berekende cijfers**](calc-metrics/calc-metr-overview.md): Metriek en formules gebruiken als nieuwe componenten voor rapportage
* [**Datumbereiken**](date-ranges/overview.md): De datumbereiken aanpassen en verfijnen die Analysis Workspace biedt
* [**Projecten**](/help/analysis-workspace/home.md): Uw projecten organiseren en onderhouden in Analysis Workspace

## Analysis Workspace-componenten

De componenten in Analysis Workspace bestaan uit metriek, dimensies, segmenten, en tijdgranulariteit die u op een project kunt slepen-en-neerzetten. Aangepaste componenten die u maakt, worden aan deze deelvensters toegevoegd, zoals aangepaste datumbereiken.

Als u het deelvenster Componenten wilt openen, klikt u op het pictogram **[!UICONTROL Components]** in de linkertrack. U kunt schakelen tussen deelvensters (Leeg paneel, [Deelvenster Vrije vorm](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md), [Quick Insights](/help/analysis-workspace/c-panels/quickinsight.md) of [Attribution IQ](/help/analysis-workspace/c-panels/attribution.md) deelvenster), [Visualisaties](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md) en Componenten met behulp van de pictogrammen voor de linkerspoorstaaf of met [sneltoetsen](/help/analysis-workspace/build-workspace-project/fa-shortcut-keys.md).

![](assets/components.png)

Zie [Een project](/help/analysis-workspace/home.md) voor informatie over het gebruiken van Componenten in een project tot stand brengen.

## Componenthandelingen

U kunt componenten (afzonderlijk of door meer dan één te selecteren) op verschillende manieren beheren. Klik met de rechtermuisknop op een component of klik op **[!UICONTROL Actions]** boven aan de lijst met componenten.

>[!NOTE]
>
>Deze handelingen zijn niet van toepassing op tijdcomponenten.

| Component Handeling | Beschrijving |
|--- |--- |
| Tag | U kunt componenten ordenen of beheren door er tags op toe te passen. De component wordt vervolgens weergegeven in de respectievelijke componentbeheerfunctie, zoals Analytics > Componenten > Segmenten, of Analytics > Componenten > Projecten |
| Favorieten | Voeg de component toe aan de lijst met favorieten. De component wordt vervolgens weergegeven in de respectievelijke componentbeheerfunctie, zoals Analytics > Componenten > Segmenten, of Analytics > Componenten > Projecten. |
| Goedkeuren | Keur de component goed om deze canonicaal te maken. De component wordt vervolgens weergegeven in de respectievelijke componentbeheerfunctie, zoals Analytics > Componenten > Segmenten, of Analytics > Componenten > Projecten |
| Delen | Alleen van toepassing op segmenten. |
| Verwijderen | Alleen van toepassing op segmenten. |

Bekijk de video over het maken van statistieken, segmenten en datums:

>[!VIDEO](https://video.tv.adobe.com/v/23979)

## Machtigingen voor componenttoegang

Beheerders kunnen bepalen (via [Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=en#manage-users-and-products)) welke componenten aan gebruikers worden blootgesteld in de rapportage. In de volgende tabel ziet u hoe deze machtigingen voor componenttoegang werken:

| Curvetype | Admin kan | Niet-admin-projecteigenaar (of bewerkingsrol) kan zien | Niet-beheerder dubbele rol |
| --- | --- | --- | --- |
| **Componenten &quot;verborgen&quot; in een gegevensweergave** | Alle componenten van de gegevensmening beschikbaar voor het melden (de verborgen componenten vereisen klikkend &quot;toont allen&quot;) | Niet beschikbaar voor rapportage | Niet beschikbaar voor rapportage |
| **Componenten die zijn toegevoegd of verwijderd uit een gegevensweergave** | Alleen componenten die aan de gegevensweergave zijn toegevoegd (verborgen of niet verborgen). Beheerders kunnen geen gegevens rapporteren over velden of componenten die niet zijn gedefinieerd in de gegevensweergave. | Alleen componenten die zijn toegevoegd aan de gegevensweergave of componenten die eigendom zijn van of worden gedeeld met de gebruiker. Verborgen componenten zijn niet beschikbaar (zoals VRS-curatie). | Alleen componenten die aan de DV zijn toegevoegd, worden niet verborgen en zijn opgenomen in de projectcuratie. |
| **Samengevoegde componenten in een project** | Alle componenten van de gegevensmening beschikbaar voor het melden (de verborgen componenten vereisen klikkend &quot;toont allen&quot;) | Alle niet-verborgen componenten van de gegevensweergave (klik op Alles tonen) | Alleen gebogen componenten, plus eventuele componenten die eigendom zijn van of gedeeld worden met de gebruiker |
| **Gekromd project dat een gegevensmening met verborgen componenten gebruikt** | Alle gegevenscomponenten die beschikbaar zijn voor rapportage (voor verborgen en niet-gekromde componenten moet u op Alles tonen klikken) | Alle niet-beheerde projectcomponenten, alle niet-verborgen componenten van de gegevensmening, en om het even welke componenten die door of met de gebruiker worden bezeten worden gedeeld | Alleen gebogen componenten, plus eventuele componenten die eigendom zijn van of gedeeld worden met de gebruiker |

