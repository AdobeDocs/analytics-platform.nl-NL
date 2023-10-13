---
description: Met de Berekende Metrische bouwer, kan iedereen een participatie metrisch tot stand brengen.
title: Deelnemings-metrisch
feature: Calculated Metrics
exl-id: 0d102f0f-3bcc-4f3a-93d2-c2b991c636cb
source-git-commit: 6a9cae93011447fff0f74ca4ae15178e0a1f36aa
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Een metrische deelname maken

Dit artikel verklaart hoe te om een participatie metrisch tot stand te brengen. Een metrische participatie toont hoe de individuele waarden voor een afmeting (zoals de Weergaven van de Pagina, het Kanaal van de Marketing) tot zittingen bijdragen of aan zittingen deelnemen die specifieke metrisch bevatten (bijvoorbeeld Orders).

Dit type informatie kan handig zijn voor elke eigenaar van de inhoud.

>[!NOTE]
>
>De metriek met andere attributiemodellen, zoals Deelname, kan ook door beheerders als deel van a worden gecreeerd [gegevensweergave](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views.html). In het onderstaande voorbeeld ziet u hoe gebruikers met toegang tot de berekende metrische builder in Workspace deze kunnen maken.


1. Beginnen met het bouwen van metrische gegevens, zoals beschreven in [Metrische gegevens samenstellen](/help/components/calc-metrics/cm-workflow/cm-build-metrics.md).
1. Geef in de builder Berekende metriek een naam voor de metrische ‘Deelname’ of iets dergelijks.
1. Sleep metrisch die een succesgebeurtenis, bijvoorbeeld &quot;Orders&quot;bevatten, in het canvas van de Definitie.
1. Selecteren ![Tandwiel](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg) voor de metrische waarde.
1. Selecteer in de pop-up die wordt weergegeven **[!UICONTROL Use a non-default attribution model]** om de [toewijzingsmodel](/help/components/calc-metrics/cm-workflow/m-metric-type-alloc.md) van die gebeurtenis **[!UICONTROL Participation]** en selecteert u **[!UICONTROL Session]** voor de [!UICONTROL Lookback window]. Selecteren **[!UICONTROL Apply]** ter bevestiging.

   In het vak Definitie wordt de geselecteerde metrische waarde bijgewerkt door toevoegen  **(Partipatie|Sessie)** op naam.

   ![](assets/participation-setup.png)



1. Selecteren [!UICONTROL **Opslaan**] om metrisch te bewaren.
1. Gebruik berekende metrisch in uw rapport. Gebruik bijvoorbeeld de berekende [!DNL Orders (Session Participation)] metrisch (zoals bepaald in stap 5) in een rapport om te tonen welk Klantniveau aan (of aan) zittingen heeft bijgedragen die een orde bevatten.

   ![](assets/participation-pages-customer-tier.png)

1. (Optioneel) Deel de metrische gegevens met andere gebruikers in uw organisatie, zoals beschreven in [Berekende maatstaven delen](/help/components/calc-metrics/cm-workflow/cm-sharing.md).
