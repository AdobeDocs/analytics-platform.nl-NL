---
description: Met Datumvergelijking in Analysis Workspace kunt u elke kolom met een datumbereik gebruiken en een algemene datumvergelijking maken, zoals jaar-over-jaar, kwartaal-over-kwartaal, maand-over-maand enzovoort.
title: Datumvergelijking
feature: Calendar
exl-id: 08113536-658f-486b-ac56-6c531240c3c2
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 5%

---

# Datumvergelijking

Met Datumvergelijking in Analysis Workspace kunt u elke kolom met een datumbereik gebruiken en een algemene datumvergelijking maken, zoals: jaar-over-jaar, kwartaal-over-kwartaal, maand-over-maand enzovoort.

## Vergelijk tijdsperiodes

De analyse vereist context, en vaak wordt die context verstrekt door een vorige tijdspanne. Bijvoorbeeld de vraag &quot;Hoeveel beter/slechter doen we dan op dit moment vorig jaar?&quot; is fundamenteel voor het begrijpen van uw zaken. De Vergelijking van de datum omvat automatisch een &quot;verschilkolom&quot;, die de percentageverandering in vergelijking met een gespecificeerde tijdspanne toont.

1. Maak een tabel voor vrije vorm met de afmetingen en metriek die u over een tijdsperiode wilt vergelijken.
1. Klik met de rechtermuisknop op een tabelrij en selecteer **[!UICONTROL Compare Time Periods]**.

   ![Tabelrij met geselecteerde tijdvakken vergelijken](assets/compare-time.png)

   >[!IMPORTANT]
   >
   >Deze klikoptie is gehandicapt voor metrische rijen, de rijen van de datumwaaier, en de rijen van de tijddimensie.

1. Afhankelijk van de manier waarop u het datumbereik van de tabel hebt ingesteld, kunt u het volgende vergelijken:

   | Optie | Beschrijving |
   |---|---|
   | **[!UICONTROL Prior week/month/quarter/year to this date range]** | Vergelijkt met week/maand/enz. onmiddellijk voor dit datumbereik. |
   | **[!UICONTROL This week/month/quarter/year last year]** | Vergelijkt tot de zelfde datumwaaier een jaar geleden. |
   | **[!UICONTROL Select range]** | Hiermee kunt u een aangepast datumbereik selecteren. |

   >[!NOTE]
   >
   >Wanneer u een aangepast aantal dagen selecteert, bijvoorbeeld 7 oktober - 20 oktober (een bereik van 14 dagen), krijgt u slechts twee opties: **[!UICONTROL Prior 14 days before this date range]**, en **[!UICONTROL Select range]**.

1. De resulterende vergelijking ziet er als volgt uit:

   ![De Lijst van de vrije vorm die een vergelijking van datumwaaiers en percentageverandering toont.](assets/compare-time-result.png)

   De rijen in de kolom Percentage wijziging worden rood weergegeven voor negatieve waarden en groen voor positieve waarden.

1. (Optioneel) Net als bij andere Workspace-projecten kunt u visualisaties maken op basis van deze tijdvergelijkingen. Hier ziet u bijvoorbeeld een staafgrafiek:

   ![Projectbalkgrafiek van werkruimte.](assets/compare-time-barchart.png)

   Als u het percentage van de wijziging in het staafdiagram wilt weergeven, moet u beschikken over de optie [!UICONTROL Percentages] instelling ingeschakeld in het dialoogvenster [!UICONTROL Visualization Settings].

## Een tijdspannekolom toevoegen ter vergelijking

U kunt nu een tijdsperiode toevoegen aan elke tabelkolom. Zo kunt u een andere tijdsperiode toevoegen dan de periode waarop uw kalender is ingesteld. Dit is een andere manier om datums te vergelijken.

1. Klik met de rechtermuisknop op een kolom in de tabel en selecteer **[!UICONTROL Add Time Period Column]** ![Lijst met kolommen in de tabel met de optie Tijdskolom toevoegen gemarkeerd ](assets/add-time-period-column.png)

1. Afhankelijk van de manier waarop u het datumbereik van de tabel hebt ingesteld, kunt u het volgende vergelijken:

   | Optie | Beschrijving |
   |---|---|
   | **[!UICONTROL Prior week/month/quarter/year to this date range]** | Voegt een kolom met de week/maand/enz. toe. onmiddellijk voor dit datumbereik. |
   | **[!UICONTROL This week/month/quarter/year last year]** | Hiermee voegt u hetzelfde datumbereik toe een jaar geleden. |
   | **[!UICONTROL Select range]** | Hiermee kunt u een aangepast datumbereik selecteren. |

   >[!NOTE]
   >
   >Wanneer u een aangepast aantal dagen selecteert, bijvoorbeeld 7 oktober - 20 oktober (een bereik van 14 dagen), krijgt u slechts twee opties: **[!UICONTROL Prior 14 days before this date range]**, en **[!UICONTROL Select range]**.

1. De tijdsperiode wordt ingevoegd vóór de kolom die u hebt geselecteerd:

   ![Vrije-vormentabel met vermelding van het aantal voorvallen voor de lopende kalenderperiode en de voorafgaande kalendermaand.](assets/add-time-period-column2.png)

1. U kunt zoveel tijdkolommen toevoegen als u wilt, maar u kunt ook verschillende datumbereiken combineren en met elkaar in overeenstemming brengen:

   ![De lijst van Freeform toont voorkomen voor deze maand, vorige maand, vorige maand een jaar geleden, en één week van vorige maand een jaar geleden.](assets/add-time-period-column4.png)

1. Bovendien kunt u op elke kolom sorteren, die de orde van dagen afhankelijk van de kolom zult veranderen u sorteert.

## Kolom-datums uitlijnen zodat deze op dezelfde rij beginnen {#section_5085E200082048CB899C3F355062A733}

Met een nieuwe instelling voor alle tabellen kunt u **[!UICONTROL Align Dates from each column to all start on the same row (applies to entire table)]**. &quot;Is van toepassing op volledige lijst&quot;betekent dat als u, bijvoorbeeld een uitsplitsing in de lijst doet, en als u dit het plaatsen voor de uitsplitsing verandert, het het plaatsen voor de volledige lijst zal veranderen.

![Tabel met vrije vorm met pop-up Tabelinstellingen waarin de datums van elke kolom worden uitgelijnd op alle beginwaarden van dezelfde rij.](assets/date-comparison-setting.png)

>[!IMPORTANT]
>
>Deze instelling is **uitgeschakeld** (niet ingeschakeld) voor alle bestaande projecten en **enabled** (gecontroleerd) voor alle nieuwe projecten.

Voorbeeld: wanneer u ervoor kiest de datums op elkaar af te stemmen, als u een vergelijking maakt van maand tot maand tussen oktober en september 2016, begint de linkerkolom met 1 oktober en begint de rechterkolom met 1 september:

![Vergelijking met maandgemiddelden.](assets/add-time-period-column3.png)

<!-- 

<p>See Jonny Moon's email from November 3. </p>

 -->
