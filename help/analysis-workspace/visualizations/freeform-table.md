---
title: Vrije-vormentabel
description: Meer informatie over tabellen met vrije vorm en de samenstelling van tabellen met vrije vorm
translation-type: tm+mt
source-git-commit: fc5a462f3d216d8cae3ce060a45ec79a44c4c918
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 1%

---


# Vrije-vormentabel

>[!NOTE] U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

In Analysis Workspace is een tabel met vrije vorm niet alleen een gegevenstabel, maar ook een interactieve visualisatie. U kunt een combinatie [componenten](/help/components/overview.md) naar de rijen en kolommen slepen om een aangepaste tabel voor uw analyse te maken. Aangezien elke component wordt gelaten vallen, zal de lijst onmiddellijk bijwerken zodat kunt u snelle analyse doen.

U kunt de tabel op verschillende manieren aanpassen:

* **Rijen**
   * Elke afmetingsrij kan tot 400 rijen tonen, alvorens paginering voorkomt. U kunt meer rijen in één enkel scherm passen door de de [meningsdichtheid](/help/analysis-workspace/build-workspace-project/view-density.md)van het project aan te passen.
   * Rijen kunnen worden opgesplitst in extra componenten. Als u veel rijen tegelijk wilt splitsen, selecteert u gewoon meerdere rijen en sleept u de volgende component boven op de geselecteerde rijen. Meer weten over [uitsplitsingen](/help/components/dimensions/t-breakdown-fa.md)?
   * Rijen kunnen worden [gefilterd](/help/analysis-workspace/build-workspace-project/pagination-filtering-sorting.md) om een beperkte set items weer te geven. Aanvullende instellingen zijn beschikbaar onder [Rijinstellingen](/help/analysis-workspace/build-workspace-project/column-row-settings/table-settings.md).

* **Kolommen**
   * Componenten kunnen in kolommen worden gestapeld om gesegmenteerde metriek, analyse op meerdere tabbladen en nog veel meer te maken.
   * De weergave van elke kolom kan worden aangepast onder de [kolominstellingen](/help/analysis-workspace/build-workspace-project/column-row-settings/column-settings.md).
   * Er zijn verschillende acties beschikbaar via het [snelmenu](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/using-the-right-click-menu.html). Het menu bevat verschillende handelingen, afhankelijk van de vraag of u op de tabelkop, de rijen of de kolommen klikt.

## Constructor tabel voor vrije vorm

Als u verkiest om verscheidene componenten aan uw lijst eerst toe te voegen, dan geef de gegevens terug, kunt u de Bouwer van de Lijst van de Vrije vorm toelaten. Als de builder is ingeschakeld, kunt u in vele dimensies, onderverdelingen, metriek en segmenten slepen en neerzetten om tabellen te maken die complexere vragen beantwoorden. Gegevens worden niet ter plekke bijgewerkt, maar worden bijgewerkt wanneer u klikt **[!UICONTROL Build]**.

De Bouwer van de lijst is een tijd-besparende optie wanneer u een complexe vraag van de gegevens hebt, en u een idee van de lijst hebt u wilt construeren om uw vraag te beantwoorden. Andere voordelen van de tabelbuilder zijn de mogelijkheid om:

* Rangschik de lijst in het nauwkeurige formaat u nodig hebt, zonder het moeten op elke actie wachten om terug te geven.
* Snel tot 4 niveaus van onderverdelingen uitvoeren.
* Definieer de instellingen voor Rij en Onderverdeling voor elke tabelrij en dimensiekolom.
* **[!UICONTROL Breakdown by Position]** voor elk niveau van de lijst door gebrek (in traditionele Lijsten Freeform, is het gebrek **[!UICONTROL Breakdown by Item]**.)
* Statische rijen in de tabel handmatig ordenen. Als u bijvoorbeeld wilt dat metrische rijen in een bepaalde volgorde worden weergegeven.
* Geef een voorvertoning weer van de indeling van uw tabel voordat u echte gegevens rendert.

Kijk [hier](https://youtu.be/GUMWiJAmMGI)naar de Freeform Table Builder.

## Gegevens vrije-vormentabel exporteren

De gegevens in een vrije-vormlijst kunnen uit Analysis Workspace op een paar manieren worden gekopieerd:

* Klik met de rechtermuisknop op de tabelkoptekst en selecteer **[!UICONTROL Copy to Clipboard]**. Hiermee wordt de volledige (zichtbare) tabel geëxporteerd.
* Markeer specifieke cellen in de tabel, klik met de rechtermuisknop en selecteer deze of gebruik de Ctrl + C-sneltoets. **[!UICONTROL Copy to Clipboard]**
* **[!UICONTROL Project > Download CSV]**. Dit zal alle zichtbare lijsten in het project als CSV uitvoeren.
