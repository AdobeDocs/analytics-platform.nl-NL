---
description: Datums en datumbereiken opgeven of een voorinstelling selecteren.
title: Overzicht van kalender- en datumbereiken
feature: Calendar
solution: Customer Journey Analytics
exl-id: 4afdc68b-97f8-4d8a-9d13-e2f3986873f1
role: User
source-git-commit: 47b7747b37f82e4d75d5272ce1d8d37f4e497bb5
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Overzicht van kalender- en datumbereiken

Met de kalender kunt u datums en datumbereiken opgeven of een voorinstelling selecteren. Datumbereiken zijn een type component dat u kunt gebruiken in Workspace-projecten. Ze stellen u in staat om gegevens te zien die in de loop der tijd trended zijn of om te zien wanneer gebeurtenissen het meest voorkomen. Datumbereiken hebben een kleurcode die paars is. Met aangepaste datumbereiken kunt u de datums aanpassen die u in Workspace-projecten ziet.

De kalenderselecties zijn van toepassing op paneelniveau, maar u hebt de optie om hen op alle panelen toe te passen. Wanneer u in Workspace op een datumbereik klikt, worden de huidige kalendermaand en de vorige kalendermaand in de interface weergegeven. U kunt deze twee kalenders aanpassen door op de rechter- en linkerpijlen in elke respectievelijke bovenhoek te klikken.

![Kalender die oktober 2022 en november 2022 toont met 1 door 30 november geselecteerd.](assets/aw_calendar2.png){width="60%"}

Met de eerste klik op een kalender wordt een datumbereikselectie gestart. Met de tweede klik voltooit u een datumbereikselectie die wordt gemarkeerd. Als de `Shift` toets ingedrukt houdt (of met de rechtermuisknop klikt), wordt toegevoegd aan het momenteel geselecteerde bereik.

U kunt ook datums (en tijdafmetingen) naar een Workspace-project slepen. U kunt specifieke dagen, weken, maanden, jaren of een roldatum selecteren.

[Datumbereik en -kalender gebruiken in Analysis Workspace](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/calendar-and-date-ranges/using-dates-in-analysis-workspace.html) (4:07)

| Instelling | Beschrijving |
| --- | --- |
| Geselecteerde dagen | Geselecteerde dagen/weken/maanden/jaren |
| Roldatums gebruiken | Het rollen datums staan u toe om een dynamisch rapport te produceren dat vooruit of achteruit voor een bepaalde periode kijkt die op wordt gebaseerd wanneer u het rapport in werking stelde. Bijvoorbeeld, als u op alle geplaatste Orden &quot;Vorige Maand&quot;wilt rapporteren (die op het Gemaakt gebied van de Datum wordt gebaseerd) en dat rapport in December in werking stellen, zou u orden zien die in november worden geplaatst. Als je datzelfde rapport in januari zou uitvoeren, zou je orders zien geplaatst in december.<ul><li>**[!UICONTROL Date Preview]**: Geeft aan welke tijdsperiode de schuivende kalender omsluit.</li><li>**[!UICONTROL Start]**: U kunt kiezen uit de huidige dag, de huidige week, de huidige maand, het huidige kwartaal en het huidige jaar.</li><li>**[!UICONTROL End]**: U kunt kiezen uit de huidige dag, de huidige week, de huidige maand, het huidige kwartaal en het huidige jaar.</li></ul>Voor een voorbeeld gaat u [hier](/help/components/date-ranges/custom-date-ranges.md). |
| Datumbereik | Hiermee kunt u een vooraf ingesteld datumbereik kiezen. De laatste 30 dagen is de standaardinstelling. **[!UICONTROL This week/month/quarter/year (excluding today)]** Hiermee kunt u kiezen uit datumbereiken zonder gegevens van vandaag over een hele dag. |
| Toepassen op alle deelvensters | Hiermee kunt u niet alleen het geselecteerde datumbereik voor het huidige deelvenster wijzigen, maar ook voor alle andere deelvensters in het project. |
| Toepassen | Hiermee past u het datumbereik alleen toe op dit deelvenster. |

## Over datumbereiken in het relatieve deelvenster {#relative-panel-dates}

Als u in Werkruimte werkt, kunt u de componenten van het datumbereik ten opzichte van de deelvensterkalender maken. Drie veelvoorkomende gebruiksgevallen waarbij relatieve deelvensterdatums van kracht worden, zijn Combo-diagrammen, Overzicht van belangrijkste metriek en Datumbereiken van de Freeform-tabel.

Relatieve paneeldatumbereiken gebruiken

1. Selecteer de **Werkruimte** tab.
1. Selecteren **Leeg project**.
1. Voeg afmetingen, metriek, en filters van de linkerspoorstaaf toe.
1. Klik op het veld voor het datumbereik van het deelvenster om de instelling voor het relatieve datumbereik van het deelvenster in of uit te schakelen.
1. Selecteren **Componenten voor datumbereik ten opzichte van de deelvensterkalender maken**.
   * Selecteer de optie om de componenten van het datumbereik te maken ten opzichte van de deelvensterkalender.
Als u relatieve datums selecteert, worden de roldatums gebaseerd op de begindatum van de deelvensterkalender en niet op de datum van vandaag.
   * Als deze optie niet wordt geselecteerd, dan zal het rollen van data op de datum van vandaag gebaseerd zijn.

   ![Kalender met component Datumbereik maken ten opzichte van geselecteerde deelvensterkalender](assets/relative-date-selected.png){width="60%"}

1. Klikken **Toepassen**.
De relatieve datums worden rechtsboven weergegeven.

   ![Vrije-vormtabel met relatieve datums gemarkeerd en met vorige maand gemarkeerd. ](assets/relative-date-range1.png)

## Richtlijnen voor datumbereiken in het relatieve deelvenster {#guidelines}

Houd rekening met de volgende richtlijnen wanneer u relatieve datumbereiken in het deelvenster gebruikt.

### Formulieren en relatieve datumbereiken {#formula-relative-dates}

Als u relatieve datums hebt geselecteerd, wordt voor alle datumformules de begindatum van het deelvenster gebruikt als beginpunt.

### Aangepaste kalenders en relatieve datumbereiken {#custom-calendar-formulas}

Wanneer u een aangepaste weekkalender gebruikt en u maanden of jaren toevoegt, berekent de formule de verschuiving van de dag in de opgegeven periode. De werkelijke datum kan verschillen vanwege de verschuiving. De formule kiest de dag die op de zelfde plaats in de douanekalender aankomt. Bijvoorbeeld de derde vrijdag van de derde week in een aangepaste kalender.

### Informatie over filters die gebruikmaken van roldatums en relatieve datumbereiken in het deelvenster {#segments-relative-dates}

Als u een filter maakt of een filter gebruikt met een roldatum, bijvoorbeeld de Laatste 7 dagen of de Laatste 2 weken, en u klikt op de filtervoorvertoning, begint de roldatum vanaf *Vandaag* in plaats van de begindatum van het deelvenster. Het resultaat is dat de voorvertoning van het filter niet overeenkomt wanneer u het filter in de tabel daadwerkelijk gebruikt. De voorvertoning wordt beïnvloed, niet het filter zelf.

## Richtlijnen voor datumbereiken en voorvertoningen in het deelvenster {#guidelines-panel-dates}

* Vanaf de release van februari worden voorvertoningen van componenten en gegevens gebaseerd op het datumbereik van het deelvenster en niet op de laatste 90 dagen.
* Alle componenten die in de linkerspoorstaaf worden vermeld zullen beschikbaar zijn gebaseerd op de waaier van de paneeldatum.
* Alle datumvoorvertoningen in het filter en de berekende metrische builders worden gebaseerd op het bereik van de paneeldatum (tenzij betreden van de componentenmanagers, die geen bijbehorend paneel hebben, zullen zij nog op de laatste 90 dagen gebaseerd zijn).
* In alle voorvertoningen van gegevens worden gegevens of componenten weergegeven op basis van het datumbereik van het deelvenster.