---
description: Verklaart hoe te om metrisch tot stand te brengen die toont welke Kanalen van de Marketing in rijorden bijwonen.
title: Een complexere, berekende metrisch maken
feature: Calculated Metrics
exl-id: 33cb441d-d003-408d-ba67-1bcdd0e821ff
source-git-commit: 1b6e1d432bfe4b0574b8ee68bcfa940941f3c36f
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Bouw complexere berekende metrisch

Dit artikel verklaart een complexer voorbeeld van berekende metrisch. Deze berekende maatstaven laten zien welke marketingkanalen helpen bij het besturen van bestellingen. Dit type van berekende metrisch kan aan om het even welke afmeting of succesgebeurtenis worden aangepast.

1. Begin om berekende metrisch te bouwen, zoals die in [&#x200B; wordt beschreven bouwt metriek &#x200B;](/help/components/calc-metrics/cm-workflow/cm-build-metrics.md).

1. Geef in de builder Berekende metriek de naam van de metrische waarde `Assisted Online Orders` of iets gelijkaardigs.

1. Selecteer de metrische waarde **[!UICONTROL Online Orders]** in de **[!UICONTROL Metrics]** -componenten en sleep de metrische waarde naar het **[!UICONTROL Definition]** -gebied.

   1. Selecteer ![&#x200B; Plaatsend &#x200B;](/help/assets/icons/Setting.svg) voor metrisch.
   1. Selecteer **[!UICONTROL Use non-default attribution model]** .
   1. Pas het attributiemodel aan in **[!UICONTROL Column attribution model]** .
      1. Selecteer **[!UICONTROL Custom]** voor **[!UICONTROL Model]** . Stel **[!UICONTROL Starter]** in op `0` , **[!UICONTROL Player]** op `100` en **[!UICONTROL Closer]** op `0` .
      1. Selecteer **[!UICONTROL Visitor]** voor **[!UICONTROL Container]** .
      1. Selecteer **[!UICONTROL 30 Days]** voor **[!UICONTROL Lookback window]** .

      1. Selecteer **[!UICONTROL Apply]** .

      ![&#x200B; de attributiemodel van de Kolom &#x200B;](assets/complex-calculated-metric.png)

1. Selecteer **[!UICONTROL Save]** om de berekende metrische waarde op te slaan.

De berekende metrische waarde gebruiken:

1. Maak in Analysis Workspace een vrije-vormtabel met de **[!UICONTROL Marketing Channel]** -dimensie **[!UICONTROL Online Orders]** en de nieuwe **[!UICONTROL Assisted Online Orders]** -metrische waarde.

   ![&#x200B; het Marketing Kanaal steunde Online Orden &#x200B;](assets/marketing-channel-assists.png)

1. (Facultatief) deel metrisch met andere gebruikers in uw organisatie, zoals die in [&#x200B; wordt beschreven aandeel berekende metriek &#x200B;](/help/components/calc-metrics/cm-workflow/cm-sharing.md).

Dit is een gemakkelijke manier om te zien welke Marketing Channels hebben geholpen bij het bestellen van rijorders. U kunt ook vanuit een vrije-vormtabel elke gewenste metrische waarde selecteren en in het contextmenu het attributiemodel rechtstreeks in de tabel aanpassen.
