---
description: Gebruik de belangrijkste metrische samenvatting visualisatie om metrische prestaties over twee chronologie te vergelijken.
title: Samenvatting van metrische sleutel
feature: Visualizations
exl-id: ef606c53-b370-419a-904b-573ee6d70a8d
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---

# Samenvatting van metrische sleutel

De [!UICONTROL Key metric summary] Met visualisatie kunt u zien hoe een belangrijke metrische waarde binnen één tijdsbestek trending. Ook kunt u de metrische prestaties in twee tijdframes vergelijken. Het biedt de voordelen van meerdere visualisaties die in één visualisatie worden gecombineerd:

* **[!UICONTROL Line]** visualisaties die tonen hoe metrisch voor de primaire en vergelijkingsdatumwaaiers trendt

* **[!UICONTROL Summary percent change]** die de metrische verhoging of daling tussen primaire en vergelijkingsdatumwaaiers toont

* Huidige totale waarde ([!UICONTROL **overzichtsnummer**]) voor de metrische

## Gebruik hoofdletters

Deze visualisatie heeft betrekking op een aantal veelvoorkomende gebruiksgevallen, waaronder:

* Een analist probeert te begrijpen hoe de creatie van kansen deze maand in vergelijking met hetzelfde tijdsbestek vorig jaar eruit zag.

* Een markering die onderzoekt hoe de productie van lood voor een specifiek loodtype van deze maand in vorige maand is veranderd.

* Een uitvoerend directeur die wil begrijpen hoe nieuwe boekingen van dit kwartaal aan vorig kwartaal veranderden.

## Vorm de Belangrijkste metrische samenvatting

1. Sleep de **[!UICONTROL Key metric summary]** visualisatie van de **[!UICONTROL Visualizations]** in de linkerspoorstaaf in een paneel.

1. Vorm visualisatie door metrisch, een primaire datumwaaier, en een waaier van de vergelijkingsdatum en een filter (indien gewenst) te selecteren:

   ![Zeer belangrijke metrische configuratie die de opties voor metrisch, primaire datumwaaier, de waaier van de vergelijkingsdatum, en segment tonen.](assets/key-metric-config.png)

   | Configuratie-instelling | Definitie |
   | --- | --- |
   | **[!UICONTROL Metric]** | Selecteer metrisch u wilt onderzoeken. Alle metriek worden ondersteund. |
   | **[!UICONTROL Primary date range]** | Het huidige datumbereik voor de vrije-vormtabel. |
   | **[!UICONTROL Comparison date range]** | Het datumbereik waarmee u het primaire datumbereik wilt vergelijken. |
   | **[!UICONTROL Filter (optional)]** | Filters waarin u specifiek geïnteresseerd bent voor deze samenvatting. |

   {style="table-layout:auto"}

1. Klik op **[!UICONTROL Build]**.

<!--## How the Key Metric Summary visualization handles the comparison date range

(This will probably release in January. Per Jaden Howell)

* If the primary date range is set to the panel date range, there are 2-6 options that are considered 'relative' to the primary date range. These usually include the previous period (same amount of time immediately proceeding the primary date range), and 52 weeks prior to that date range.

* If the comparison date range is set to one of the 'relative' options, upon updating the primary date range, the comparison date range updates to the period immediate preceding the panel date range.

* If your comparison date range is *not* set to a 'relative' option, then updating the panel date range changes your primary date range, but has no effect on the comparison date range.

**Example 1**

Primary date range is set to the panel's date range: 'Yesterday'
Comparison date range is set to a relative date range, one of: 'Previous day', 'Same day last week', 'Same day 4 weeks prior', 'Same day last month', 'Same day last year', or 'Same day 52 weeks prior'.
When I change the panel's date range to 'This month', the comparison date range will update to 'Previous month'.

**Example 2**
 
Primary date range is set to the panel's date range: 'Yesterday'
Comparison date range is set to a non-relative date range, such as 'Feb 2nd, 2022', 'Highest sales day', 'Last week', etc. 

>[!NOTE]
>
>Last week is relative to the day the project is opened on, but it is not based on the panel's date range of 'Yesterday'. In other cases, such as if the panel's date range was 'This week', it may be relative.

When you change the panel's date range to '4 days ago', the comparison date range remains at the previous selection. -->

## De uitvoer weergeven

![De belangrijkste metrische output die de metische, summiere verandering, samenvattingsaantal, en lijngrafieken toont.](assets/key-metric-output.png)

Opmerking:

* De **[!UICONTROL Previous period]** lijngrafiek (altijd grijs weergegeven) komt overeen met de **[!UICONTROL Comparison date range]** in de configuratiestap.

* Als een vergelijkingsdatumbereik niet is opgegeven tijdens de configuratie of verborgen is in de visualisatie-instellingen, wordt alleen de lijngrafiek voor het primaire datumbereik weergegeven. De samenvattingswijziging wordt verborgen.

* Vanaf hier kunt u de cursor boven de lijngrafieken houden om de statistieken voor afzonderlijke dagen weer te geven:

![Bezoekersstatistieken](assets/key-metric-output2.png)

## Visualisatie-instellingen

De Belangrijkste metrische samenvatting biedt veelvoudige flexibele montages aan om betere rapportering en communicatie van belangrijke metriek toe te laten. Instellingen zijn toegankelijk via het tandwielpictogram in de rechterbovenhoek van de visualisatie.

![Belangrijke metrische samenvattingsinstellingen met het weergavetype Samenvatting, Algemeen en weergaveopties.](assets/key-metric-settings.png)

| Instelling | Beschrijving |
| --- | --- |
| **[!UICONTROL Emphasize percent change]** | Samenvattingswijziging in opvallende vetgedrukte tekst weergeven in het midden van de visualisatie |
| **[!UICONTROL Emphasize number value]** | Samenvattingsnummer in opvallende, vette letters weergeven in het midden van de visualisatie |
| **[!UICONTROL Legend visible]** | De legenda onder aan de visualisatie weergeven of verbergen |
| **[!UICONTROL Show annotations]** | Annotaties die zijn toegevoegd door een beheerder tonen of verbergen |
| **[!UICONTROL Show sparklines]** | Lijngrafieken onder aan het diagram weergeven of verbergen. Als de legenda is verborgen, wordt deze niet langer visueel doorverwezen naar de regels |
| **[!UICONTROL Show min and max on sparklines]** | Minimum- en maximumwaarden tonen of verbergen in primaire en vergelijkingslijngrafieken |
| **[!UICONTROL Show comparison]** | Vergelijkingsgegevens tonen of verbergen. Wanneer deze optie is verborgen, worden zowel het vergelijkingsregeldiagram als de summiere wijzigingsobjecten verborgen. |
| **[!UICONTROL Show total number]** | Samenvattingsnummer tonen of verbergen |
| **[!UICONTROL Show raw difference]** | Onbewerkt verschil tonen of verbergen tussen de totale waarde van de metrische waarde in het primaire datumbereik en het secundaire datumbereik |
| **[!UICONTROL Abbreviate value]** | Afkorting van numerieke waarden om gecommuniceerde inzichten te vereenvoudigen (bijvoorbeeld 20.000 -> 20K) |

## Visualisatie bewerken

Na het bouwen van visualisatie, kunt u de originele configuratie nog uitgeven.

1. Klik op het potloodpictogram in de rechterbovenhoek van de visualisatie (naast het tandwielpictogram voor instellingen).

   ![Bewerkingspictogram.s voor visualisatie](assets/edit-icon.png)

   U wordt nu teruggezet naar de originele configuratiemening.

1. Wijzig desgewenst het metrische bereik, het primaire datumbereik, het vergelijkingsdatumbereik of het filter.
