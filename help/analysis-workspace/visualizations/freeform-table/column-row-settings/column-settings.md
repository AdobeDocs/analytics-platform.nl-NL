---
description: Leer hoe u kolominstellingen kunt bewerken om kolomopmaak te configureren, waarvan sommige voorwaardelijk kunnen zijn.
title: Kolominstellingen
feature: Visualizations
exl-id: b41d8a12-e8d9-405c-ac71-6567397aec6b
role: User
source-git-commit: 4bf8c616965718426efe880865acb0e5054b6a31
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 7%

---

# [!UICONTROL Column Settings]

Met [!UICONTROL Column settings] kunt u kolomopmaak configureren, waarvan sommige voorwaardelijk kunnen zijn.


>[!BEGINSHADEBOX]

Zie ](/help/assets/icons/VideoCheckedOut.svg) [ Rij en kolommontages 0} VideoCheckedOut in een Vrije vormlijst ](https://video.tv.adobe.com/v/40382/?quality=12&learn=on){target="_blank"} voor een demo video.![

{{videoaa}}

>[!ENDSHADEBOX]


Om tot [!UICONTROL Column settings] toegang te hebben, selecteer ![ montages van de Kolom ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg) in de kolomrubriek.

![Kolominstellingen](assets/column-settings.png)


U kunt instellingen voor meerdere kolommen tegelijk bewerken. Selecteer veelvoudige kolommen en selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) in om het even welke geselecteerde kolommen. Alle wijzigingen die u aanbrengt, worden toegepast op alle kolommen met cellen die erin zijn geselecteerd.

| Optie | Beschrijving |
| --- | --- |
| **[!UICONTROL Show total]** | Een som van de kolommen aan de clientzijde weergeven. Dit totaal **** dedupliceert metriek zoals zittingen of personen niet. |
| **[!UICONTROL Show grand total]** | Toon een server-zijsom van de kolom. Het totaal-generaal dedupliceert metriek zoals zittingen of personen. |
| **[!UICONTROL Show sparkline]** | Een lijndiagram weergeven bij de kolomkop. |
| **[!UICONTROL Number]** | Bepaal of een cel de numerieke waarde voor de metrische waarde weergeeft/verbergt. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de numerieke waarde het aantal paginaweergaven voor het rij-item. |
| **[!UICONTROL Percent]** | Bepaal of een cel de percentagewaarde voor metrisch toont/verbergt. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de percentagewaarde het aantal paginaweergaven voor het rijitem, gedeeld door de totale paginaweergaven voor de kolom.  Opmerking: percentages van meer dan 100% zijn mogelijk om accuraat te zijn. Het bovenste gebonden uiteinde kan naar 1.000% worden verplaatst om te voorkomen dat de kolombreedte te groot wordt. |
| **[!UICONTROL Show anomalies]** | Bepaal of de waarden in deze kolom een anomaliedetectie uitvoeren. |
| **[!UICONTROL Show forecast]** | Bepaal of de voorspelde waarden in deze kolom worden weergegeven. |
| **[!UICONTROL Wrap header text]** | Plaats de koptekst in Freeform-tabellen om kopteksten leesbaarder te maken en tabellen beter deelbaar te maken. Wrappen is handig voor het renderen van PDF en voor metriek met lange namen. Standaard ingeschakeld. |
| **[!UICONTROL Interpret zero as no value]** | Bepaal of voor cellen met een waarde 0 een cel of een lege cel moet worden weergegeven. Deze interpretatie is handig wanneer u gegevens voor elke dag van een maand bekijkt en bepaalde dagen in de toekomst.  In plaats van &#39;0&#39; voor toekomstige datums weer te geven, worden lege cellen weergegeven. Bij grafieken wordt deze instelling ook gebruikt (diagrammen geven geen lijn of balk met 0 waarden weer). |
| **[!UICONTROL Background]** | Bepaal of in een cel alle celopmaak wordt weergegeven of verborgen, inclusief de staafgrafiek en voorwaardelijke opmaak. |
| **[!UICONTROL Bar Graph]** | Een horizontale staafgrafiek tonen die de waarde van de cel ten opzichte van het totaal voor de kolom vertegenwoordigt. |
| **[!UICONTROL Conditional Formatting]** | Gebruik voorwaardelijke opmaak. Zie de [ sectie ](#conditional-formatting) hieronder. |
| **[!UICONTROL Table Cell Preview]** | Een voorbeeld van hoe elke cel wordt weergegeven met de momenteel geselecteerde opmaakopties toegepast. |
| **[!UICONTROL Use non-default attribution model]** | Gebruik een niet-standaard toewijzingsmodel. Zie de [ sectie ](#use-non-default-attribution-model) hieronder. |

## Voorwaardelijke opmaak {#conditional-formatting}

Met voorwaardelijke opmaak wordt opmaak toegepast op de bovenste, middelste en onderste limieten die u kunt definiëren. Het toepassen van voorwaardelijke opmaak in Freeform-tabellen wordt ook automatisch ingeschakeld voor uitsplitsingen, tenzij [!UICONTROL Custom] limieten zijn geselecteerd.

![ Voorwaardelijke het formatteren ](./assets/conditional-formatting.png)

| Opties voor voorwaardelijke opmaak | Beschrijving |
| --- | --- |
| **[!UICONTROL  Use percent limits]** | Wijzig het limietbereik zodat dit op percentages wordt gebaseerd in plaats van op absolute waarden. Het percentagelimietbereik werkt voor metriek die uitsluitend op percentage gebaseerd zijn (zoals Stuitsnelheid) en voor metriek die een telling en een percentage hebben (zoals Paginaweergaven). |
| **[!UICONTROL Auto-generated]** | Berekent automatisch de bovenste/middelste/onderste limieten op basis van de gegevens. De bovengrens is de hoogste waarde in deze kolom. De ondergrens is de laagste en het middelpunt is het gemiddelde van de boven- en ondergrens. |
| **[!UICONTROL Custom]** | Wijs **[!UICONTROL Upper limit]**, **[!UICONTROL Midpoint]** en **[!UICONTROL Lower limit]** handmatig toe. De grenzen verstrekken de flexibiliteit om te bepalen wanneer een kolomwaarde goed, gemiddeld, of slecht wordt. |
| **[!UICONTROL Conditional formatting palette]** | Pas een vooraf geconfigureerde kleurenset toe op cellen. Afhankelijk van welke van de vier beschikbare kleurenschema&#39;s u selecteert, worden de verschillende kleuren toegewezen aan hoge waarden, middelpuntwaarden, en lage waarden. <br> Als u een dimensie in de tabel vervangt, worden de limieten voor voorwaardelijke opmaak opnieuw ingesteld. Wanneer u een metric vervangt, worden de limieten voor die kolom opnieuw berekend (waarbij de metric op de X-as staat en de dimensie op de Y-as). |

## Niet-standaard toewijzingsmodel gebruiken {#use-non-default-attribution-model}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_column_usenondefaultattributionmodel"
>title="Niet-standaard toewijzingsmodel gebruiken"
>abstract="Schakel een niet-standaard toewijzingsmodel in voor de geselecteerde kolommen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_column_usenondefaultattributionmodel_disabled"
>title="Niet-standaard toewijzingsmodel gebruiken"
>abstract="Niet-standaardtoewijzingsmodus is niet beschikbaar voor deze metrische waarde."

<!-- markdownlint-enable MD034 -->



U kunt het standaardattributiemodel met voeten treden dat in [ meningen van Gegevens ](/help/data-views/component-settings/attribution.md) wordt gevormd.

>[!NOTE]
>
>Houd rekening met het volgende wanneer u de toewijzing van een component bijwerkt naar een niet-standaard toewijzingsmodel:
>
>* **wanneer het gebruiken van de component in een rapport met *één enkele afmeting*:** de attributie van de component negeert het toewijzingsmodel wanneer een niet-gebrek attributiemodel wordt gebruikt.
>
>* **wanneer het gebruiken van de component in een rapport met *veelvoudige afmetingen*:** de attributie van de component behoudt het toewijzingsmodel wanneer een niet-gebrek attributiemodel wordt gebruikt.
>
>   De veelvoudige afmetingen zijn beschikbaar slechts wanneer [ het uitvoeren van gegevens aan de wolk ](/help/analysis-workspace/export/export-cloud.md).
>
> Voor meer informatie over toewijzing, zie {de montages van de componenten van 0} Persistence ](/help/data-views/component-settings/persistence.md).[

Een niet-standaard toewijzingsmodel gebruiken voor een metrisch object in een Analysis Workspace:

1. Selecteer **[!UICONTROL Use non-default attribution model]** . Als deze optie al is geselecteerd, gebruikt u **[!UICONTROL Edit]** om het toewijzingsmodel te bewerken. U kunt ook de selectie opheffen om terug te keren naar het standaardtoewijzingsmodel.

   ![ de Kolom die opties plaatst die de optie van de Montages van Gegevens benadrukken: Gebruik niet-standaardattributiemodus.](assets/attribution-checkbox.png)

2. Selecteer in **[!UICONTROL Column attribution model]** een **[!UICONTROL Model]** en een **[!UICONTROL Lookback window]** . Het terugkijkvenster bepaalt het venster van gegevensattributie dat voor elke omzetting wordt toegepast.

   ![ de Opties van het Model van de Attributie van de Kolom die Lineair tonen.](assets/attribution-select.png)


### Attributiemodellen

{{attribution-models-details}}

### Venster Opzoeken

{{attribution-lookback-window}}



>[!MORELIKETHIS]
>
>* [Databronnen beheren](/help/analysis-workspace/visualizations/t-sync-visualization.md)
