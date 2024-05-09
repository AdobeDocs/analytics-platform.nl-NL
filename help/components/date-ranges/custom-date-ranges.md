---
description: Maak aangepaste datumbereiken in Analysis Workspace en sla deze op als tijdcomponenten.
keywords: Analysis Workspace
title: Aangepaste datumbereiken maken
feature: Calendar
exl-id: 1a7df63a-bf18-4c38-b7e2-e83c2d278544
role: User
source-git-commit: 47b7747b37f82e4d75d5272ce1d8d37f4e497bb5
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Aangepaste datumbereiken maken

U kunt aangepaste datumbereiken maken in Analysis Workspace en deze opslaan als tijdcomponenten.

Zie voor informatie over het toevoegen van bestaande datumbereiken aan een project [Overzicht van kalender- en datumbereiken](/help/components/date-ranges/calendar.md).

Een aangepast datumbereik maken:

1. Selecteer in Adobe Analytics **[!UICONTROL Components]** > **[!UICONTROL Date ranges]**.

   ![datumbereikpagina](assets/date-ranges.png)

1. Selecteren [!UICONTROL **Nieuw datumbereik maken**].

1. Geef de volgende informatie op in de constructor Datumbereik:

   | Optie | Beschrijving |
   |---------|----------|
   | [!UICONTROL **Titel**] | De titel van het datumbereik zoals deze wordt weergegeven wanneer gebruikers de titel selecteren in Analysis Workspace. |
   | [!UICONTROL **Beschrijving**] | Een beschrijving voor het datumbereik. |
   | [!UICONTROL **Tags**] | Alle tags die u wilt toepassen op het datumbereik. |
   | [!UICONTROL **Datumbereik**] | Hiermee kunt u een aangepast datumbereik kiezen. Standaard zijn de laatste 30 dagen geselecteerd. |
   | [!UICONTROL **Voorinstelling**] | Maak een keuze in een lijst met vooraf ingestelde datumbereiken, zoals [!UICONTROL **Gisteren**], [!UICONTROL **Laatste 7 dagen**], [!UICONTROL **Laatste 30 dagen**], enzovoort. |
   | [!UICONTROL **Begintijd**] | De tijd van de dag waarop het datumbereik begint. |
   | [!UICONTROL **Eindtijd**] | De tijd van de dag waarop het datumbereik eindigt. |
   | [!UICONTROL **Roldatums gebruiken**] | Het rollen datums staan u toe om een dynamisch rapport te produceren dat vooruit of achteruit voor een bepaalde periode kijkt die op wordt gebaseerd wanneer u het rapport in werking stelde. Bijvoorbeeld, als u op alle geplaatste Orden &quot;Vorige Maand&quot;wilt rapporteren (die op het Gemaakt gebied van de Datum wordt gebaseerd) en dat rapport in December in werking stellen, zou u orden zien die in november worden geplaatst. Als je datzelfde rapport in januari zou uitvoeren, zou je orders zien geplaatst in december.<ul><li>**[!UICONTROL Date Preview]**: Geeft aan welke tijdsperiode de schuivende kalender omsluit.</li><li>**[!UICONTROL Start]**: U kunt kiezen uit de huidige dag, de huidige week, de huidige maand, het huidige kwartaal en het huidige jaar.</li><li>**[!UICONTROL End]**: U kunt kiezen uit de huidige dag, de huidige week, de huidige maand, het huidige kwartaal en het huidige jaar.</li></ul><br>Standaard geselecteerd. |

1. Selecteren [!UICONTROL **Opslaan**].

## Voorbeeld: datumbereik voor &quot;twee maanden geleden&quot; {#section_C4109C57CB444BB2A79CC8082BD67294}

De volgende waaier van de douanedatum toont een datumwaaier voor &quot;twee maanden geleden,&quot;met een Summiere visualisatie van de Verandering die richtingsverandering toont.

![](assets/date-range-two-months-ago.png)

Het aangepaste datumbereik wordt boven aan het dialoogvenster [!UICONTROL Date Range] deelvenster in uw project:

![](assets/date-range-panel-two-months-ago.png)

U kunt dit aangepaste datumbereik naar een kolom slepen naast een aangepast maandelijks roldatumbereik met de voorinstelling Laatste maand voor een vergelijking. Voeg een Summiere visualisatie van de Verandering toe en selecteer de totalen van elke kolom om richtingsverandering te tonen:

![](assets/date-range-two-months-table.png)

## Voorbeeld: een 7-daags roldatumbereik gebruiken {#section_7EF63B2E9FF54D2E9144C4F76956A8DD}

U kunt een datumbereik maken dat een 7-daags schuivend venster opgeeft dat een week geleden eindigt:

![](assets/create_date_range.png)

Gebruiken *`rolling daily`*.

* De instellingen voor Start worden *`current day minus 6 days`*.

* De instellingen voor Einde worden *`current day minus 7 days`*.

Dit datumbereik kan een component zijn die u naar elke vrije-vormtabel sleept.
