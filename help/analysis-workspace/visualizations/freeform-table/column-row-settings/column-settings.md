---
description: Leer hoe u kolominstellingen kunt bewerken om kolomopmaak te configureren, waarvan sommige voorwaardelijk kunnen zijn.
title: Kolominstellingen
feature: Visualizations
exl-id: b41d8a12-e8d9-405c-ac71-6567397aec6b
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 14%

---

# [!UICONTROL Column Settings]

[!UICONTROL Column Settings] Laat u kolom het formatteren vormen, wat waarvan voorwaardelijk kan zijn.

Bekijk hier een video over rij- en kolominstellingen:

>[!VIDEO](https://video.tv.adobe.com/v/40382/?quality=12)

## Bewerken [!UICONTROL Column Settings] {#edit-column-settings}

Toegang tot [!UICONTROL Column Settings]Sleep een tabel voor vrije vorm naar het project en klik vervolgens op het tandwielpictogram in de kolomkop.

![De kolominstellingen tonen Totaal aantal cellen, Tabelcellen en Tabelcelvoorvertoning.](assets/column_settings.png)

U kunt instellingen bewerken **voor meerdere kolommen tegelijk**. Dit is heel eenvoudig: selecteer meerdere kolommen en klik op het instellingenpictogram van een van de kolommen. Alle wijzigingen die u aanbrengt, worden toegepast op alle kolommen waarin u cellen hebt geselecteerd.

| Element | Beschrijving |
| --- | --- |
| Getal | Hiermee wordt bepaald of in een cel de numerieke waarde voor de metrische waarde wordt weergegeven of verborgen. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de numerieke waarde het aantal paginaweergaven voor het rij-item. |
| Percentage | Bepaalt of een cel de percentagewaarde voor metrisch toont/verbergt. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de percentagewaarde het aantal paginaweergaven voor het rijitem gedeeld door de totale paginaweergaven voor de kolom.  Opmerking: we kunnen percentages van meer dan 100% weergeven, om nauwkeuriger te zijn. We verplaatsen het bovenste gebonden plafond ook naar 1000% om ervoor te zorgen dat kolommen te groot kunnen worden. |
| Anomalies | Hiermee wordt bepaald of de waarden in deze kolom een anomaliedetectie uitvoeren. |
| Tekst koptekst tekstomloop | Hiermee kunt u de koptekst laten omlopen in Freeform-tabellen om kopteksten leesbaarder te maken en tabellen beter deelbaar te maken. Dit is handig voor .pdf-rendering en voor metriek met lange namen. Standaard ingeschakeld. |
| nul interpreteren als geen waarde | Voor cellen met een waarde 0 bepaalt u of een cel van 0 of een lege cel moet worden weergegeven. Dit is handig wanneer u gegevens bekijkt voor elke dag van een maand, en sommige dagen zijn nog niet gebeurd.  In plaats van &#39;0&#39; voor toekomstige datums weer te geven, kunnen lege cellen worden weergegeven. Grafieken voldoen ook aan deze instelling (ze geven dus geen lijn of balk weer met 0 waarden als deze instelling is ingeschakeld). |
| Achtergrond | Hiermee bepaalt u of alle celopmaak, inclusief de staafgrafiek en voorwaardelijke opmaak, in een cel wordt weergegeven of verborgen. |
| Staafgrafiek | Hiermee wordt een horizontale staafgrafiek weergegeven die de waarde van de cel ten opzichte van het totaal voor de kolom vertegenwoordigt. |
| Voorwaardelijke opmaak | Zie de onderstaande paragraaf. |
| Tabelcelvoorvertoning | Toont een voorproef van hoe elke cel met de momenteel geselecteerde opmaakopties wordt getoond. |

## Voorwaardelijke opmaak {#conditional-formatting}

Met voorwaardelijke opmaak wordt opmaak toegepast op de bovenste, middelste en onderste limieten die u kunt definiëren. Het toepassen van voorwaardelijke opmaak (kleuren, enz.) in Freeform-tabellen wordt ook automatisch ingeschakeld voor onderverdelingen, tenzij &quot;Aangepaste&quot; limieten zijn geselecteerd.

![De voorwaardelijke opmaakopties met Aangepast geselecteerd.](assets/conditional-formatting.png)

| Element | Beschrijving |
| --- | --- |
| Voorwaardelijke opmaak | Hiermee past u een vooraf geconfigureerde kleurenset van uw keuze toe op cellen. Afhankelijk van welke van de vier beschikbare kleurenschema&#39;s u selecteert, worden de verschillende kleuren toegewezen aan hoge waarden, middelpuntwaarden, en lage waarden. <br> Als u een dimensie in de tabel vervangt, worden de limieten voor voorwaardelijke opmaak opnieuw ingesteld. Wanneer u een metric vervangt, worden de limieten voor die kolom opnieuw berekend (waarbij de metric op de X-as staat en de dimensie op de Y-as). |
| Percentagelimieten gebruiken | Wijzig het limietbereik zodat dit op percentages wordt gebaseerd in plaats van op absolute waarden. Dit werkt voor metriek die uitsluitend op percentage-gebaseerd (zoals het Tarief van de Stuiting) evenals voor metriek zijn die een telling en een percentage (zoals de Weergaven van de Pagina. hebben) |
| Automatisch genereren | Berekent automatisch de bovenste/middelste/onderste limieten op basis van de gegevens. De bovengrens is de hoogste waarde in deze kolom. De ondergrens is de laagste en het middelpunt is het gemiddelde van de boven- en ondergrens. |
| Aangepast | Handmatig bovenste/middelste/onderste limieten toewijzen. Dit biedt u de flexibiliteit om te bepalen wanneer een kolomwaarde goed, gemiddeld, of slecht wordt. |
| Voorwaardelijk opmaakpalet | Kies welke van de vier beschikbare kleurenschema&#39;s u voor uw voorwaardelijke formatteren wilt gebruiken. |

## Niet-standaard toewijzingsmodel gebruiken {#attribution}

Hiermee kunt u de standaardkenmerkset overschrijven in [Gegevensweergaven](/help/data-views/component-settings/attribution.md).

>[!NOTE]
>
>Houd rekening met het volgende wanneer u de toewijzing van een component bijwerkt naar een niet-standaard toewijzingsmodel:
>
>* **Wanneer het gebruiken van de component in een rapport met *één dimensie*:** De toewijzing van de component negeert het toewijzingsmodel wanneer een niet-standaard toewijzingsmodel wordt gebruikt.
>
>* **Wanneer het gebruiken van de component in een rapport met *meerdere dimensies*:** De toewijzing van de component behoudt het toewijzingsmodel wanneer een niet-standaard toewijzingsmodel wordt gebruikt.
>
>   Meerdere afmetingen zijn alleen beschikbaar als [gegevens exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md).
>
> Zie voor meer informatie over toewijzing [Instellingen voor persistentiecomponenten](/help/data-views/component-settings/persistence.md).

Een niet-standaard toewijzingsmodel gebruiken voor een metrisch object in een Analysis Workspace:

1. Klik op het pictogram Instellingen (versnelling) op een metrische waarde in een kolom Tabel voor vrije vorm.

   ![De opties voor kolominstelling waarmee de optie Gegevensinstellingen wordt gemarkeerd: de niet-standaard toewijzingsmodus gebruiken.](assets/attribution-checkbox.png)

2. Onder **[!UICONTROL Data Settings]**, controle **[!UICONTROL Use non-default attribution model]**. Zie voor meer informatie over verschillende toewijzingsmodellen [Attributiemodellen](/help/data-views/component-settings/attribution.md).

   ![De opties van het Model van de Attributie van de Kolom tonen Lineair geselecteerd.](assets/attribution-select.png)

>[!MORELIKETHIS]
>
>* [Databronnen beheren](/help/analysis-workspace/visualizations/t-sync-visualization.md)
