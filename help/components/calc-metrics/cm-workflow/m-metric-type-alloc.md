---
description: Meer informatie over
title: Type cijfers en attributie
feature: Calculated Metrics
exl-id: da73a9ba-542e-436c-bdb2-b629b5b6f760
source-git-commit: c343a729de4cb13473a7acc04e837b5e5f69809b
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 4%

---

# Type cijfers en attributie

Als u het tandwielpictogram naast een metrische waarde selecteert, kunt u het metrische type en het attributiemodel opgeven.

## Metrisch type

Om metrisch type te specificeren wanneer het bouwen van berekende metrisch:

1. Selecteer het tandwielpictogram naast metrisch waarvan type u wilt selecteren.

   ![Het tandwielpictogram met pop-up die Metrisch type toont gelijk aan Norm.](assets/cm_type_alloc.png)

1. Kies een van de volgende opties:

   | Metrisch type | Definitie |
   |---|---|
   | Standaard | Deze cijfers zijn dezelfde maatstaven die standaard worden gebruikt [!DNL Analytics] rapportage. Als een formule uit één enkele norm bestond, toont het identieke gegevens aan zijn niet-berekende-metrische tegenhanger. Standaardmetriek zijn handig voor het maken van berekende metriek die specifiek is voor elk afzonderlijk regelitem. Bijvoorbeeld: [Orders] / [Sessies] neemt orden voor dat specifieke lijnpunt en verdeelt het door het aantal zittingen voor dat specifieke lijnpunt. |
   | Totaal | Gebruik het totaal-generaal voor de rapportageperiode in elke post. Als een formule uit één enkel Eindtotaal metrisch bestond, toont het het zelfde Grote totale aantal op elk lijnpunt. Eindwaarden zijn handig voor het maken van berekende metriek die met totale gegevens wordt vergeleken. Bijvoorbeeld: [Orders] / [Totaal aantal sessies] toont het aandeel van orden tegen ALLE zittingen op een kanaal, niet alleen de zittingen aan het specifieke lijnpunt. |

## Attributie

Voor informatie over attributie in Customer Journey Analytics raadpleegt u [Instellingen van component Attributie](/help/data-views/component-settings/attribution.md).
