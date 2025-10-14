---
title: Instellingen voor metagegevensdeduplicatie
description: Telling slechts het eerste voorkomen van metrisch in rapporten.
exl-id: ced0c637-5cbe-47a4-897a-eb79961986a3
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: af88be97f303095129177b2132c6711c648cea34
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# Instellingen voor metagegevensdeduplicatie {#metric-deduplication-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_component_metric_deduplication"
>title="Metrische deduplicatie"
>abstract="Vorm metrisch om slechts waarden te tellen die niet-herhalend voorkomen."

<!-- markdownlint-enable MD034 -->


Met Metrische deduplicatie kunt u een metrische waarde configureren, zodat waarden alleen op niet-herhaalde wijze worden geteld.

![&#x200B; Metrische deduplicatie &#x200B;](../assets/metric-deduplication.png)

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Metric deduplication] | Een selectievakje waarmee u metrische deduplicatie kunt inschakelen. Standaard uitgeschakeld. |
| [!UICONTROL Deduplication scope] | Hiermee kunt u bepalen hoe ver de unieke controle achteruit gaat.<br/>**[!UICONTROL Global account]**: Alleen de eerste metrische instantie in het rapportagevenster wordt geteld.<br/>**[!UICONTROL Account]**: Alleen de eerste metrische instantie in het rapportagevenster wordt geteld.<br/>**[!UICONTROL Opportunity]**: Alleen de eerste metrische instantie in het rapportagevenster wordt geteld.<br/>**[!UICONTROL Buying group]**: Alleen de eerste metrische instantie in het rapportagevenster wordt geteld.<br/>**[!UICONTROL Person]**: Alleen de eerste metrische instantie in het rapportagevenster wordt geteld.<br>**[!UICONTROL Session]**: Alleen de eerste metrische instantie van de sessie wordt geteld. <br> |
| [!UICONTROL Deduplication ID] | In plaats van deduplicatie toe te passen op metrisch zelf, staat u toe om metrische deduplicatie toe te passen die op een afmeting wordt gebaseerd. Waardevol voor dimensies zoals de aankoop-id om deduplicatie toe te passen. |
| [!UICONTROL Value to keep] | <ul><li>**houd eerste instantie**: Gebruik dit in situaties waar de aanvankelijke instantie van metrisch geldige is. De meest voorkomende is waarschijnlijk een aankoopbevestiging. Zelfs als iemand per ongeluk de pagina opnieuw laadt en er een ander exemplaar van een aankoopbevestiging komt, is de eerste gebeurtenis de geldige.</li><li>**houd laatste instantie**: Gebruik dit in situaties waar de laatste instantie nuttiger om is te verzamelen. Voorbeeld: iemand werkt zijn onlineprofiel bij. We willen slechts één van deze updates per sessie tellen. Tijdens de sessie kunnen ze hun profiel echter meerdere keren bijwerken. Als we het eerste geval behouden, kunnen er activiteiten zijn die niet aan de gebeurtenis gebonden zijn. In dit geval is het zinvoller om het laatste geval te behouden.</li></ul> |

{style="table-layout:auto"}

>[!CAUTION]
>
>De deduplicatie bij a _persoon_ werkingsgebied wordt geëvalueerd door volledige maanden in tijd UTC. Een rapportagevenster voor een gedeeltelijke maand geeft mogelijk niet alle eerste of laatste exemplaren weer, als sommige gevallen zich binnen de volledige maand maar buiten de rapportagedatums hebben voorgedaan.
