---
description: Hier ziet u voorbeelden van berekende metriek.
title: Voorbeelden van berekende metriek
feature: Calculated Metrics
exl-id: 5e73ab52-627a-4064-bfb7-354c0ba1e4ee
source-git-commit: 976f481b6886a4f260f44854a30c47ab0dad7955
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Voorbeelden van berekende metriek

In dit artikel worden voorbeelden getoond van het definiëren van geavanceerdere berekende meetwaarden.

## Stuitpercentage

U wilt de stuiteringsfrequentie berekenen.

+++ Details

De definitie van een stuit is onderwerp voor een andere bespreking maar voor dit voorbeeld, definieert u een Verworpen gebeurtenissegment waar het Begin van de Zitting 1 en Zitting Eind evenaart 1. Met dit segment definieert u wel de frequentie van teruggestuurde sessies aan sessies.


### Segment

![&#x200B; Stuiterende gebeurtenissen &#x200B;](assets/example-bounce-bouncedevents.png)

### Berekende metrische waarde

![&#x200B; Stuitsnelheid &#x200B;](assets/example-bounce-rate.png)


### Afgeleide velden

Alternatief, kunt u a [&#x200B; stuittarief bepalen gebruikend afgeleide gebieden &#x200B;](/help/data-views/derived-fields/derived-fields.md#bounces).

Afgeleide gebieden maken deel uit van een mening van Gegevens die het voordeel heeft dat niet elke gebruiker de definitie van metrisch tarief met betrekking tot Stuiteren kan met voeten treden of wijzigen. Dat voordeel heeft ook een beperking ingevoerd. De gebruikers die geen toegang tot een gegevensmening hebben kunnen geen afgeleide gebieden gebruiken en moeten aan segmenten en berekende metriek een stuiteringstarief gebruiken.

Zie voor meer achtergrondinformatie over hoe te om grenzen en stuittarief in Customer Journey Analytics te berekenen, dit [&#x200B; blogpost &#x200B;](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/calculating-bounces-amp-bounce-rate-in-adobe-customer-journey/ba-p/706446).

+++


## Voorwaardelijke paginaweergaven

U wilt een berekende maatstaf definiëren die alleen de paginaweergaven berekent voor de pagina&#39;s die in meer dan 100 sessies zijn bezocht.

+++ Details

![&#x200B; Voorwaardelijke paginameningen &#x200B;](assets/conditional-page-views.png)

+++

## Paginaweergaven voor de bovenste 30% sessies

U wilt een berekende metrisch bepalen die slechts paginameningen voor de hoogste 30% zittingen berekent.

+++ Details

![&#x200B; Hoogste 30% paginameningen &#x200B;](assets/top30-page-views.png)

+++
