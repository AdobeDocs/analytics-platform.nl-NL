---
description: 'null'
title: Overzicht van uitval
uuid: 2d98899e-e401-4d7a-8af0-de0002f84178
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 2%

---


# Overzicht van uitval

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Vallout-visualisaties bieden meer opties voor het samenstellen van uw uitvalrapporten. Uit de uitvalrapporten blijkt waar bezoekers een vooraf gedefinieerde reeks pagina&#39;s hebben verlaten (uitgevallen) en doorlopen (doorgevallen).

Met uitvalvisualisaties kunt u

* Voer zij aan zij vergelijkingen van twee verschillende segmenten in het zelfde rapport uit.
* Trechterstappen (aanraakpunten) slepen, neerzetten en opnieuw rangschikken
* Waarden van verschillende afmetingen en maateenheden mixen en afstemmen
* Een multidimensionaal uitvalrapport maken
* Identificeer waar de klanten onmiddellijk na het vallen gaan

Bij Uitvallen worden de conversie- en uitvalsnelheden tussen elke stap of elk aanraakpunt in een reeks weergegeven.

U kunt bijvoorbeeld de uitvalpunten van een bezoeker bijhouden tijdens een aankoopproces. Selecteer gewoon een begin- en een eindaanraakpunt en voeg tussenliggende aanraakpunten toe om een websitenavigatiepad te maken. Maar je kunt ook multidimensionale fallouts doen.

Een uitvalvisualisatie is handig voor het analyseren van:

* Conversiepercentages via specifieke processen op uw site (zoals een aankoop- of registratieproces).
* Algemene verkeersstromen met een groter bereik: Van de mensen die de homepage zagen, toont deze stroom hoeveel er doorgingen om een onderzoek uit te voeren, en toen hoeveel van hen uiteindelijk naar een specifiek punt gingen kijken.
* Correlaties tussen gebeurtenissen op uw site. Correlaties laten zien welk percentage van de mensen die naar je privacybeleid keken, een product heeft gekocht.

[Volledige visualisatie op YouTube](https://www.youtube.com/watch?v=VcrfHSyIoj8&amp;index=52&amp;list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) (4:15)

## Segmentatie als basis voor flow en fallout {#section_654F37A398C24DDDB1552A543EE29AA9}

Segmenten die zijn toegepast op deelvensters Werkruimte, werken iets anders dan segmenten die zijn toegepast op rapportage over fallout en stroom in Rapporten en Analytics of Ad hoc analysis. Meestal leveren ze precies dezelfde resultaten op. Het belangrijkste verschil is dat Rapporten &amp; Analytics en Ad hoc analysis het segment bij elke stap van de opeenvolging toepassen. Dit kan tot iets verschillende resultaten leiden.

Laten we een voorbeeld nemen van fallout met twee stappen:

![](assets/fallout_segments1.png)

Als u dan een segment op het het paneelniveau van de Werkruimte toepast, combineert het segment met de reserve als dit:

![](assets/fallout_seg.png)

Wanneer daarentegen Rapporten &amp; Analytics en Ad hoc analysis het segment berekenen, wordt het segment op deze manier gecombineerd:

![](assets/fallout_segments3.png)

Rapporten &amp; Analytics en Ad hoc analysis combineren het segment met elke stap. Wanneer de containers zich op hetzelfde niveau bevinden als de uitval (bv. bezoek of bezoekersniveau), zal dit ertoe leiden dat het aantal bezoeken of bezoekers gelijk wordt gesteld.

Als het segment dat op het paneel wordt toegepast kleiner is dan het valniveau (bijvoorbeeld raakniveau), geeft het segment echter verschillende resultaten vanwege de manier waarop het wordt gecombineerd met het rapport. Om te herhalen, komen de aantallen in Analysis Workspace in de meeste gevallen overeen met die in Reports &amp; Analytics en Ad hoc analysis. Ze komen alleen **niet** overeen als alle onderstaande gevallen waar zijn:

* Het segment bevindt zich niet op hetzelfde niveau als de uitval.
* Het segment heeft een variabele waarbij de bezoeker/bezoeker meerdere waarden kan hebben tijdens een bezoek/bezoeker.

In het zeldzame geval waarin u Analysis Workspace de Rapporten &amp; manier van Analytics moet hebben om segmenten toe te passen aan fallout/stroom, eenvoudig laat vallen het segment in elke falloutstap in Werkruimte en het zal in de zelfde aantallen resulteren.
