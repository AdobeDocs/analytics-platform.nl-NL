---
title: Instellingen voor metagegevensdeduplicatie
description: Telling slechts het eerste voorkomen van metrisch in rapporten.
exl-id: ced0c637-5cbe-47a4-897a-eb79961986a3
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: e2ebda486eae7740351370f48bdf104c90494ae3
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 1%

---

# Instellingen voor metagegevensdeduplicatie

Met Metrische deduplicatie kunt u een metrische waarde configureren, zodat waarden alleen op niet-herhaalde wijze worden geteld.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Metric deduplication] | Een selectievakje waarmee u metrische deduplicatie kunt inschakelen. Standaard uitgeschakeld. |
| [!UICONTROL Deduplication scope] | Hiermee kunt u bepalen hoe ver de unieke controle achteruit gaat.<br>**Sessie**: Alleen de eerste metrische instantie van de sessie wordt geteld.<br>**Persoon**: Alleen de eerste metrische instantie in het rapportagevenster wordt geteld. |
| [!UICONTROL Deduplication ID] | In plaats van deduplicatie toe te passen op metrisch zelf, staat u toe om metrische deduplicatie toe te passen die op een afmeting wordt gebaseerd. Waardevol voor dimensies zoals de aankoop-id om deduplicatie toe te passen. |

{style=&quot;table-layout:auto&quot;}

>[!CAUTION]
>
>   Deduplicatie op een _persoon_ bereik wordt geëvalueerd met volledige maanden UTC-tijd. Een rapportagevenster voor een gedeeltelijke maand geeft mogelijk niet alle eerste of laatste exemplaren weer, als sommige gevallen zich binnen de volledige maand maar buiten de rapportagedatums hebben voorgedaan.
