---
description: Leer hoe Workspace totalen worden berekend.
title: Totaal Workspace
feature: Visualizations
exl-id: ba14b88c-44c2-45f6-b68f-f5c1263a89dd
role: User
source-git-commit: 770320a0b16d26e0755203a3524b000db30cac82
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---

# Totaal Workspace {#workspace-totals}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_grandtotal"
>title="Eindtotaal"
>abstract="Groot totaal wordt niet ondersteund voor tabellen of uitsplitsingen met statische rijen"

<!-- markdownlint-enable MD034 -->


In Freeform-tabellen wordt op elk uitsplitsingsniveau een totale rij weergegeven met twee totalen:

![ vrije lijst die van de Vrije Vorm het grote totaal en het lijsttotaal benadrukt.](assets/total-row.png)

* **[!UICONTROL Table total]** ➊ - Dit totaal is doorgaans gelijk aan of een subset van de [!UICONTROL Grand total] . Het totaal weerspiegelt alle tabelsegmenten die binnen de vrije-vormtabel worden toegepast, inclusief de optie [!UICONTROL Include None] .
* **[!UICONTROL Grand total]** (**[!UICONTROL out of]** *aantal*) ➋ - Dit totaal vertegenwoordigt alle gebeurtenissen die zijn verzameld. Wanneer een segment wordt toegepast op paneelniveau of binnen de vrije-vormlijst, past dit totaal aan om op alle gebeurtenissen te wijzen die aan de segmentcriteria voldoen.




## Totalen weergeven

Onder ![ Plaatsend ](/help/assets/icons/Setting.svg) **[!UICONTROL Column settings]**, zijn er opties aan **[!UICONTROL Show totals]** en **[!UICONTROL Show grand total]**. Als deze instellingen niet zijn ingeschakeld, worden de totalen uit de tabel verwijderd. Dit is mogelijk het geval als totalen onzinnig zijn.


[ Statische rij ](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md) gedraagt zich verschillend, en wordt gecontroleerd gebruikend ![ Plaatsend ](/help/assets/icons/Setting.svg) **[!UICONTROL Row Settings]**.

| Optie | Beschrijving |
|---|---|
| **[!UICONTROL Show sum of current rows as the total]** | Een som van de rijen in de tabel aan de clientzijde weergeven. Dit totaal **** dedupliceert metriek zoals zittingen of personen niet. |
| **[!UICONTROL Show grand total]** | Een som aan de serverzijde weergeven. Dit totaal dedupliceert metriek zoals sessies of personen. |

Zie [ Dynamische versus statische afmetingspunten in vrije vormlijsten ](column-row-settings/manual-vs-dynamic-rows.md).


## Veelgestelde vragen

| Vragen | Antwoord |
|---|---|
| Welk *totaal* zijn de grijze kolompercentages die op worden gebaseerd? | Dit *totaal* hangt van **[!UICONTROL Percentages]** het plaatsen selectie onder **[!UICONTROL Row Settings]** af:<ul><li>Percentage berekenen op kolom - Dit is de standaardinstelling. De percentages zijn gebaseerd op het totaal van de Lijst.</li><li>Percentage berekenen op rij - Percentages worden gebaseerd op het Eindtotaal.</li></ul> |
| Hoe beïnvloedt de instelling van **[!UICONTROL Include "No value"]** de totalen? | Als het **[!UICONTROL Include "No value"]** plaatsen wordt ongecontroleerd, wordt de **[!UICONTROL No value]** rij verwijderd uit de lijst, het totaal van de Lijst, en door aan om het even welke berekende metriek loopt die [*Totale* metrische types ](/help/components/calc-metrics/cm-workflow/m-metric-type-alloc.md) gebruiken. |
| Wanneer de douanetabelsegmenten op een vrije vormlijst worden toegepast, doe al mijn berekende metriek en voorwaardelijke het formatteren rekening voor het segment? | Momenteel niet. **[!UICONTROL Include "No value"]** is een account, maar aangepaste tabelsegmenten hebben geen invloed op het volgende:<ul><li>Het maximale/minimale bereik van de kolom dat bij voorwaardelijke opmaak wordt gebruikt, loopt over alle gegevens.</li><li>Berekende waarden die gebruikmaken van **[!UICONTROL Grand total]** -metrische typen.</li><li>Berekende metriek met functies die over rijen in een vrije vormlijst berekenen: Kolomsom, Kolommaximum, Kolom min, Aantal, Gemiddelde, Mediaan, Percentage, Kwartaal, Aantal rijen, Standaardafwijking, Variantie, Cumulatief, Cumulatief Gemiddelde, Regressievarianten, T-Score, T-Test, Z-Score en Z-Test.</li></ul> |
| Wat weerspiegelt het metrische type **[!UICONTROL Grand total]** in Berekende metriek? | **[!UICONTROL Grand total]** blijft naar **[!UICONTROL Grand total]** verwijzen en geeft geen segmenten weer die op een tabel of de **[!UICONTROL Table total]** zijn toegepast. |
| Welk totaal wordt getoond wanneer de gegevens of van een vrije vormlijst worden gekopieerd en worden gekleefd of via CSV worden gedownload? | De totale rij geeft alleen **[!UICONTROL Table total]** weer en neemt de instelling voor de kolom **[!UICONTROL Show totals]** in acht. |
