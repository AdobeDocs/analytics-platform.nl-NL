---
description: Met een interdimensionale stroom kunt u gebruikerspaden in verschillende dimensies bekijken.
title: Interdimensionale stromen
uuid: 51d08531-1c56-46c7-b505-bd8d5e6aa6c1
exl-id: 459166b1-a522-45b6-9d2c-69e3409e442e
source-git-commit: f74b5e79b6713050869301adb95e2a73705330da
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 1%

---

# Interdimensionale stromen

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van [Analysis Workspace in traditionele Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Met een interdimensionale stroom kunt u gebruikerspaden in verschillende dimensies bekijken.

Een afmetingslabel boven aan elke stroomkolom maakt het gebruik van meerdere dimensies in een stroomvisualisatie intuïtiever:

![](assets/flow.png)

We zullen naar twee gebruiksgevallen kijken: een gebruiksgeval voor apps en een gebruiksgeval voor het web.

## Eerste hoofdletter gebruiken: app

De [!UICONTROL Action Name] dimensie werd toegevoegd aan de stroom, met het hoogste teruggekeerde punt dat [!UICONTROL ItemAdded] is:

![](assets/multi-dimensional-flow.png)

Als u de interactie tussen schermen/pagina&#39;s en acties in deze app wilt verkennen, kunt u de paginadimensie naar meerdere plaatsen slepen, afhankelijk van wat u wilt verkennen:

* Sleep het naar een van de uiteinden van de neerzetzone (binnen de met zwart omgezette rechthoekige zone die wordt weergegeven) naar **vervang** de bovenste resultaten aan de uiteinden:

   ![](assets/multi-dimensional-flow2.png) ![](assets/multi-dimensional-flow3.png)

* Sleep het naar de witruimte aan het einde (let op de zwarte haak) om **aan** de visualisatie toe te voegen:

   ![](assets/multi-dimensional-flow4.png)

Hier is het resultaat als u besluit om het item ItemScaled in de juiste kolom met de dimensie van de Pagina te vervangen. Het bovenste resultaat wordt nu gewijzigd in het bovenste resultaat voor de pagina-afmeting:

![](assets/multi-dimensional-flow5.png)

Nu kunt u zien hoe klanten door acties en pagina&#39;s bewegen. U kunt de stroom verder verkennen door op verschillende knooppunten te klikken:

![](assets/multi-dimensional-flow6.png)

Dit is wat gebeurt als u een andere dimensie van de Naam van de Actie op het eind van visualisatie toevoegt:

![](assets/multi-dimensional-flow7.png)

Op deze manier kunt u diepgaande inzichten en mogelijke wijzigingen aanbrengen in de app die u analyseert.

## Hoofdlettergebruik twee: web

In dit geval kunt u zien hoe u kunt analyseren welke campagnes de meeste items naar een website sturen.

Sleep de dimensie van de Naam van de Campagne in een nieuwe stroom:

![](assets/multi-dimensional-flow8.png)

Nu wil ik zien aan welke pagina&#39;s die campagnes verkeer drijven, zodat sleep ik de dimensie van de Pagina rechts van de stroomresultaten om op visualisatie toe te voegen:

![](assets/multi-dimensional-flow9.png)
