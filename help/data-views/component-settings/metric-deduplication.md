---
title: Instellingen voor metagegevensdeduplicatie
description: Telling slechts het eerste voorkomen van metrisch in rapporten.
exl-id: ced0c637-5cbe-47a4-897a-eb79961986a3
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: 81e04d177596430b6e9d971cb1b157b461524314
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Instellingen voor metagegevensdeduplicatie

Met Metrische deduplicatie kunt u een metrische waarde configureren, zodat waarden alleen op niet-herhaalde wijze worden geteld.

![Metrische deduplicatie](../assets/metric-deduplication.png)

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Metric deduplication] | Een selectievakje waarmee u metrische deduplicatie kunt inschakelen. Standaard uitgeschakeld. |
| [!UICONTROL Deduplication scope] | Hiermee kunt u bepalen hoe ver de unieke controle achteruit gaat.<br>**Sessie**: Alleen de eerste metrische instantie van de sessie wordt geteld.<br>**Persoon**: Alleen de eerste metrische instantie in het rapportagevenster wordt geteld. |
| [!UICONTROL Deduplication ID] | In plaats van deduplicatie toe te passen op metrisch zelf, staat u toe om metrische deduplicatie toe te passen die op een afmeting wordt gebaseerd. Waardevol voor dimensies zoals de aankoop-id om deduplicatie toe te passen. |
| [!UICONTROL Value to keep] | <ul><li>**Eerste instantie behouden**: Gebruik dit in situaties waar de eerste instantie van de metrische waarde geldig is. De meest voorkomende is waarschijnlijk een aankoopbevestiging. Zelfs als iemand per ongeluk de pagina opnieuw laadt en er een ander exemplaar van een aankoopbevestiging komt, is de eerste gebeurtenis de geldige.</li><li>**Laatste instantie behouden**: Gebruik dit in situaties waarin de laatste instantie zinvoller is om te verzamelen. Voorbeeld: Iemand werkt zijn onlineprofiel bij. Wij willen slechts één van deze updates per zitting tellen. Tijdens de sessie kunnen ze hun profiel echter meerdere keren bijwerken. Als we het eerste geval behouden, kunnen er activiteiten zijn die niet aan de gebeurtenis gebonden zijn. In dit geval is het zinvoller om het laatste geval te behouden.</li></ul> |

{style="table-layout:auto"}

>[!CAUTION]
>
>Deduplicatie op een _persoon_ bereik wordt geëvalueerd met volledige maanden UTC-tijd. Een rapportagevenster voor een gedeeltelijke maand geeft mogelijk niet alle eerste of laatste exemplaren weer, als sommige gevallen zich binnen de volledige maand maar buiten de rapportagedatums hebben voorgedaan.
