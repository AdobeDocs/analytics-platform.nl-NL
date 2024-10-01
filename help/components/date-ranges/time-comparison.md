---
description: Met Datumvergelijking in Analysis Workspace kunt u elke kolom met een datumbereik gebruiken en een algemene datumvergelijking maken, zoals jaar-over-jaar, kwartaal-over-kwartaal, maand-over-maand enzovoort.
title: Datumvergelijking
feature: Calendar
exl-id: 08113536-658f-486b-ac56-6c531240c3c2
role: User
source-git-commit: 483c0d3bcc6ff700395a51a4d550844fb6af30d2
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# Datumvergelijking

Met Datumvergelijking in Analysis Workspace kunt u elke kolom met een datumbereik gebruiken en een algemene datumvergelijking maken, zoals: jaar-over-jaar, kwartaal-over-kwartaal, maand-over-maand enzovoort.

## Vergelijk tijdsperiodes

De analyse vereist context, en vaak wordt die context verstrekt door een vorige tijdspanne. Bijvoorbeeld, de vraag *hoeveel beter of slechter doet u nu in vergelijking met dit tijd vorig jaar?* is essentieel voor het begrijpen van uw bedrijf. De vergelijking van de datum omvat automatisch de kolom van het a *verschil*, die de percentageverandering in vergelijking met een gespecificeerde tijdspanne toont.

1. Creeer de lijst van de a [ Vrije vorm ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md), met om het even welke afmetingen en metriek u over een tijdspanne wilt vergelijken.
1. Open het contextmenu voor een tabelrij en selecteer **[!UICONTROL Compare time periods]** .

   ![ rij van de Lijst met de geselecteerde Punten van de Tijd van de Vergelijking ](assets/compare-time.png)

   >[!NOTE]
   >
   >Deze optie van het contextmenu is gehandicapt voor metrische rijen, de rijen van de datumwaaier, en rijen van de tijddimensie.

1. Afhankelijk van de manier waarop u het datumbereik van de tabel hebt ingesteld, kunt u het volgende vergelijken:

   | Optie | Beschrijving |
   |---|---|
   | **[!UICONTROL Prior *x *weken/maanden/kwartalen/jaar aan deze datumwaaier]** | Vergelijk met het geselecteerde datumbereik vlak voor dit datumbereik. |
   | **[!UICONTROL These x weeks / months / quarters / years last year to this date range]** | Vergelijk met dezelfde datumbereik een jaar geleden. |
   | **[!UICONTROL Custom date range to this date range]** | Hiermee kunt u een aangepast datumbereik definiëren. |

   >[!NOTE]
   >
   >Wanneer u een aangepast aantal dagen selecteert, bijvoorbeeld 7 oktober - 20 oktober (een bereik van 14 dagen), krijgt u slechts twee opties: **[!UICONTROL Prior 14 days before this date range]** en **[!UICONTROL Custom date range to this date range]** .

1. De resulterende vergelijking ziet er als volgt uit:

   ![ Vrije Lijst die een vergelijking van datumwaaiers en percentageverandering toont.](assets/compare-time-result.png)

   Rijen in de kolom Percentage wijziging worden rood weergegeven voor negatieve waarden en groen voor positieve waarden.

## Een tijdspannekolom toevoegen ter vergelijking

U kunt nu een tijdsperiode toevoegen aan elke kolom in een tabel, zodat u een andere tijdsperiode kunt toevoegen dan de periode waarop uw kalender is ingesteld.

1. Klik met de rechtermuisknop op een kolom in de tabel en selecteer **[!UICONTROL Add time period column]** .

   ![](assets/add-time-period-column.png)

1. Afhankelijk van de manier waarop u het datumbereik van de tabel hebt ingesteld, kunt u het volgende vergelijken:

   | Optie | Beschrijving |
   |---|---|
   | **[!UICONTROL Prior *x *weken/maanden/kwartalen/jaar aan deze datumwaaier]** | Voeg een kolom toe met week/maand/enz. onmiddellijk voor dit datumbereik. |
   | **[!UICONTROL These *x *weken/maanden/kwartalen/jaar vorig jaar aan deze datumwaaier]** | Voeg hetzelfde datumbereik toe een jaar geleden. |
   | **[!UICONTROL Custom date range to this date range]** | Hiermee kunt u een aangepast datumbereik maken. |

   >[!NOTE]
   >
   >Wanneer u een aangepast aantal dagen selecteert, bijvoorbeeld 7 oktober - 20 oktober (een bereik van 14 dagen), krijgt u slechts twee opties: **[!UICONTROL Prior 14 days before this date range]** en **[!UICONTROL Custom date range to this date range]** .

1. De tijdsperiode wordt ingevoegd boven de kolom die u hebt geselecteerd:

   ![ Vrije Lijst die Voorvallen voor huidige kalenderperiode en de vorige kalendermaand tonen.](assets/add-time-period-column2.png)

1. U kunt zoveel tijdkolommen toevoegen als u wilt, maar u kunt ook verschillende datumbereiken combineren en met elkaar in overeenstemming brengen:

1. Bovendien kunt u op elke kolom sorteren, die de orde van dagen afhankelijk van de kolom verandert u sorteert.

## Kolom-datums uitlijnen zodat deze op dezelfde rij beginnen

U kunt de datums van elke kolom uitlijnen op alle datums die op dezelfde rij beginnen.

U maakt bijvoorbeeld een vergelijking van dag tot dag voor de laatste week (die eindigt op 5 oktober 2024) en de vorige week. Standaard begint de linkerkolom met 22 september en de rechterkolom met 29 september.

![ niet uitgelijnde data ](assets/not-align-dates.png)

U kunt **[!UICONTROL Align dates from each column to all start on the same row]** in [ Montages ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md#settings-1) voor de Freeform lijstvisualisatie toelaten om kolomdata te richten om op de zelfde rij te beginnen.

![](assets/align-dates.png)

Houd rekening met het volgende wanneer u deze optie gebruikt:

* Deze instelling wordt standaard ingeschakeld voor alle nieuwe projecten.

* Deze instelling is van toepassing op de hele tabel. Als u deze instelling bijvoorbeeld wijzigt voor een uitsplitsing binnen de tabel, wordt de instelling toegepast op de hele tabel.

