---
description: Afmetingen en dimensies in Analysis Workspace onderverdelen.
keywords: Analysis Workspace
title: Afmetingen onderverdelingen
feature: Dimensions
exl-id: 6b433db3-02c1-4deb-916e-b01c0b79889e
solution: Customer Journey Analytics
role: User
source-git-commit: c56c77079aa21fb740fda6bec333731a1f82a48f
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Afsplitsingsafmetingen in Workspace

U kunt uw gegevens op onbeperkte manieren voor uw specifieke behoeften opsplitsen; bouwt vragen gebruikend relevante metriek, dimensies, filters, tijdlijnen, en andere waarden van de analyseonderbreking.

1. In a [ Vrije lijst ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md), van het contextmenu van één of meerdere geselecteerde rijen, uitgezochte **[!UICONTROL Breakdown]** ![ ChevronRight ](/help/assets/icons/ChevronRight.svg).

   ![ Resultaat van de Stap die alarm van geselecteerde selectie toont.](assets/breakdown.png)

1. Selecteer in het submenu **[!UICONTROL Dimensions]** , **[!UICONTROL Metrics]** , **[!UICONTROL Filters]** of **[!UICONTROL Date ranges]** en selecteer vervolgens een item.

U kunt metriek onderverdelen door afmetingspunten of publieksfilters over geselecteerde tijdsperioden. U kunt ook verder naar beneden boren tot een meer korrelig niveau.

>[!NOTE]
>
>Het aantal uitsplitsingen dat in de tabel moet worden weergegeven, is beperkt tot 200. Deze limiet neemt toe voor uitsplitsingen exporteren.

## Uitsplitsing naar positie

Standaard zijn uitsplitsingen vast op statische rijitems. Stel dat u de bovenste pagina&#39;s met dimensies (Homepage, Zoekresultaten, Afhandeling) opsplitst op Marketingkanaal. Dan verlaat u het project en keert twee weken later terug. Nadat u het project opnieuw hebt geopend, zijn de bovenste drie pagina&#39;s gewijzigd. In plaats daarvan zijn Homepage, Zoekresultaten en Afhandeling de bovenste 4-6 pagina&#39;s. Standaard worden uw uitsplitsingen naar marketingkanaal nog steeds weergegeven onder Homepage, Zoekresultaten en Afhandeling, ook al bevinden ze zich nu in de rijen 4-6.

In tegenstelling, **Uitsplitsing door positie**, onderbreekt altijd top 3 punten, ongeacht wat deze punten zijn. Verwijzend naar het voorbeeld, wanneer u uw project opnieuw opent, zijn de onderbrekingen van het Kanaal van de Marketing gebonden aan de hoogste 3 pagina&#39;s in de lijst. En niet naar Homepage, zoekresultaten en afhandeling, die nu in de rijen 4 tot en met 6 staan. Zie [ montages van de Rij ](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md) hoe te om dit het plaatsen te vormen.



## Toewijzingsmodellen toepassen op uitsplitsingen

Voor elke uitsplitsing binnen een tabel kan ook een toewijzingsmodel worden toegepast. Dit attributiemodel kan hetzelfde zijn of verschillen van de bovenliggende kolom. Bijvoorbeeld, kunt u lineaire Orden op uw afmeting van de Kanalen van de Marketing analyseren maar U-Vormde Orden op de specifieke het volgen codes binnen een Kanaal toepassen. Als u het toewijzingsmodel wilt bewerken dat is toegepast op een uitsplitsing, beweegt u de muisaanwijzer over het uitsplitsingsmodel en selecteert u **[!UICONTROL Edit]** .

![ Vergelijking van de Attributie van de Orde die de montages van de Onderbreking tonen ](assets/breakdown-attribution.png)

Dit is het verwachte gedrag wanneer het toepassen van attributiemodellen op onderverdelingen of het uitgeven van hen:

* Als u een attributie toepast terwijl er geen andere attributies bestaan, wordt de attributie toegepast op de gehele kolomstructuur.

* Als u een uitsplitsing toevoegt nadat een toewijzing is toegepast, wordt de standaardinstelling gebruikt voor de opgegeven uitsplitsing die is toegevoegd (als die dimensie een standaardinstelling heeft). Anders wordt de uitsplitsing van de bovenliggende kolom gebruikt. Sommige dimensies hebben een standaardtoewijzing. De tijdafmetingen en de referentie gebruiken bijvoorbeeld Gelijke aanraking. De dimensie van het Product gebruikt Last Touch. Andere afmetingen hebben geen gebrek, en zullen de toewijzing van de ouderkolom gebruiken.

* Als de kolomstructuur al kenmerken bevat, heeft het wijzigen van de toewijzing alleen invloed op de eigenschap die u bewerkt.

+++ Video&#39;s weergeven waarin dimensies en dimensies worden geïllustreerd

Dimensionen in Analysis Workspace

>[!VIDEO](https://video.tv.adobe.com/v/23971)

Uitsplitsingen naar Dimension

>[!VIDEO](https://video.tv.adobe.com/v/23969)

Afmetingen en metriek toevoegen aan uw project in Analysis Workspace:

>[!VIDEO](https://video.tv.adobe.com/v/30606)

Werken met afmetingen in een tabel voor vrije vorm:

>[!VIDEO](https://video.tv.adobe.com/v/40179)

Uitsplitsingen naar positie van Dimension:

>[!VIDEO](https://video.tv.adobe.com/v/24033)

{{videoaa}}

+++
