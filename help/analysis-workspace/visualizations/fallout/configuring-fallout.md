---
description: Leer hoe u de aanraakpunten configureert en opgeeft om een multidimensionale uitvalvolgorde te maken.
title: Een Fallout Visualisatie configureren
feature: Visualizations
exl-id: 3d888673-d7b1-45ef-bd3a-97b98466fb0e
role: User
source-git-commit: d91e6aaebd14bc02f53b28820dd6013350e36d36
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# Een fallout-visualisatie configureren {#configure-fallout-visualization}


U kunt de aanraakpunten opgeven om een multidimensionale fallout-reeks te maken. Doorgaans is een aanraakpunt een pagina op uw site. Aanraakpunten zijn echter niet beperkt tot pagina&#39;s. U kunt bijvoorbeeld gebeurtenissen, zoals eenheden, en unieke personen en terugkeerbezoeken toevoegen. U kunt ook dimensies toevoegen, zoals een categorie, type browser of interne zoekterm.

U kunt zelfs segmenten binnen een aanraakpunt toevoegen. U kunt bijvoorbeeld segmenten, zoals iOS- en Android™-gebruikers, vergelijken. Sleep de gewenste segmenten naar de bovenkant van de uitval en de informatie over die segmenten wordt toegevoegd aan het uitvalrapport. Als u alleen die segmenten wilt tonen, kunt u de basislijn Alle bezoeken verwijderen.

Er geldt geen beperking voor het aantal stappen dat u kunt toevoegen of het aantal gebruikte dimensies.

U kunt op afmetingen, metriek, en segmenten schilderen. Stel dat iemand bijvoorbeeld naar schoenen, shirt kijkt op de ene pagina en op de volgende pagina naar shirt, sokken. Het volgende productflowrapport van schoenen is shirt en sokken, NOT shirt.

## Gebruiken

1. Voeg a ![&#x200B; ConversionFunnel &#x200B;](/help/assets/icons/ConversionFunnel.svg) **[!UICONTROL Fallout]** visualisatie toe. Zie [&#x200B; een visualisatie aan een paneel &#x200B;](../freeform-analysis-visualizations.md#add-visualizations-to-a-panel) toevoegen.
1. Sleep een pagina, bijvoorbeeld huis, van de afmeting van de Pagina op *toevoegt touchpoint* drop-down menu.

   ![&#x200B; de homepage van de pagina van het Huis dimensie die aan het Add gebied van het Aanraakpunt wordt gesleept.](assets/fallout-drag.png)

   Houd de muisaanwijzer boven een aanraakpunt om de fallout en andere informatie over dat niveau te zien, zoals de naam van het aanraakpunt en de persoon die op dat punt telt. En zie het succespercentage voor dat aanraakpunt (en vergelijk het succespercentage met andere aanraakpunten.)

   De omcirkelde getallen in het grijze gedeelte van de balk geven de fallout tussen aanraakpunten aan (niet de totale fallout naar dat punt). In **[!UICONTROL Touchpoint %]** ziet u hoe de vorige stap is doorgelopen naar de huidige stap in het falloutrapport.

   U kunt ook één pagina toevoegen aan het fallout-rapport in plaats van de volledige dimensie. Klik de juiste pijl ![&#x200B; ChevronRight &#x200B;](/help/assets/icons/ChevronRight.svg) op de paginadimensie om een specifieke pagina te kiezen om aan het rapport van de Vallout toe te voegen.

1. Voeg aanraakpunten toe totdat de reeks is voltooid.

   U kunt **veelvoudige touchpoints** combineren door één of meerdere extra componenten op een touchpoint te slepen.

   >[!NOTE]
   >
   >De veelvoudige segmenten worden aangesloten bij EN, maar de veelvoudige punten zoals afmetingspunten en metriek worden aangesloten bij OF.

   ![&#x200B; de Pagina :CamerRoll of Pagina: Gemarkeerde de aanrakingspunten van de Camera.](assets/fallout-or.png)

1. U kunt **individuele touchpoints aan de volgende gebeurtenis** (in tegenstelling tot *uiteindelijk*) binnen de weg ook beperken. Onder elk aanraakpunt bevindt zich een kiezer met de opties **[!UICONTROL Eventual path]** en **[!UICONTROL Next event]** , zoals u hier ziet:

   ![&#x200B; de Al mening die van Bebezoeken de Eventuele benadrukte optie van de Weg toont. &#x200B;](assets/fallout-nexthit.png)

   | Optie | Beschrijving |
   |---|---|
   | **[!UICONTROL Eventual path]** (standaardwaarde) | De personen worden geteld dat *uiteindelijk* op de volgende pagina in de weg zal landen, maar niet noodzakelijk op de volgende gebeurtenis. |
   | **[!UICONTROL Next event]** | Personen worden geteld die op de volgende pagina op het pad zullen landen bij de allervolgende gebeurtenis. |


## Instellingen {#settings}

>[!CONTEXTUALHELP]
>id="workspace_fallout_container"
>title="Fallout container"
>abstract="Selecteer een container om het plakken te analyseren. Deze selectie helpt u om betrokkenheid te begrijpen en beperkt de analyse tot de geselecteerde container."

Als onderdeel van de visualisatie zijn specifieke instellingen beschikbaar.

| Fallout container | Beschrijving |
|--- |--- |
| **[!UICONTROL Session]** of **[!UICONTROL Person]** | Schakel tussen [!UICONTROL Session] en [!UICONTROL Person] om het plakken van personen te analyseren. De standaardwaarde is [!UICONTROL Person] . Met deze instellingen kunt u de betrokkenheid van personen op persoonlijke niveau (tijdens verschillende sessies) begrijpen of de analyse beperken tot één sessie. |


## Contextmenu

Als onderdeel van de visualisatie zijn specifieke opties voor contextmenu&#39;s beschikbaar.

![&#x200B; opties van de Fallout &#x200B;](assets/fallout-options.png)

| Optie | Beschrijving |
|--- |--- |
| **[!UICONTROL Trend touchpoint]** | Zie trendgegevens voor een aanraakpunt in een lijngrafiek, met sommige vooraf gebouwde anomaliedetectiegegevens. |
| **[!UICONTROL Trend touchpoint (%)]** | Hiermee wordt het totale uitvalpercentage verhoogd. |
| **[!UICONTROL Trend all touchpoints (%)]** | Hiermee worden alle aanraakpuntpercentages in de fallout (behalve **[!UICONTROL All People]** als deze is opgenomen) in hetzelfde diagram gekweekt. |
| **[!UICONTROL Break down fallthrough at this touchpoint]** | Bekijk wat personen deden tussen twee aanraakpunten (dit aanraakpunt en het volgende aanraakpunt) als ze doorgingen naar het volgende aanraakpunt. Hiermee maakt u een vrije-vormtabel waarin de afmetingen worden weergegeven. U kunt afmetingen en andere elementen van de tabel vervangen. Bijvoorbeeld, een lijst die **[!UICONTROL Fallthrough: All People > Page equals any of home]** wordt geëtiketteerd en **[!UICONTROL Page]** als afmeting en **[!UICONTROL People]** bevat die door het [&#x200B; project-slechts snelle segment &#x200B;](/help/components/segments/seg-quick.md) **[!UICONTROL Fallthrough: All People > Page equals any of home]** als metrisch wordt gesegmenteerd. Inspecteer het segment om te begrijpen hoe het reservesegment wordt bepaald. |
| **[!UICONTROL Break down fallout at this touchpoint]** | Bekijk wat mensen die het niet via de funnel hebben gedaan, direct na de geselecteerde stap hebben gedaan. Hiermee maakt u een vrije-vormtabel waarin de afmetingen worden weergegeven. U kunt afmetingen en andere elementen van de tabel vervangen. Bijvoorbeeld, een lijst die **[!UICONTROL Fallout: People > Page equals any of home]** wordt geëtiketteerd en **[!UICONTROL Page]** als dimensie en **[!UICONTROL People]** bevat die door het [&#x200B; project-enige snelle segment &#x200B;](/help/components/segments/seg-quick.md) **[!UICONTROL Fallthrough: All Visitors > Page equals any of home]** segment als metrisch wordt gesegmenteerd. Inspecteer het segment om te begrijpen hoe het reservesegment wordt bepaald. |
| **[!UICONTROL Create segment from touchpoint]** | Maak een nieuw segment van het geselecteerde aanraakpunt. |

>[!MORELIKETHIS]
>
>[&#x200B; voeg een visualisatie aan een paneel toe &#x200B;](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>&#x200B;>[Visualisatie-instellingen &#x200B;](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>&#x200B;>[Contextmenu Visualisatie &#x200B;](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>

