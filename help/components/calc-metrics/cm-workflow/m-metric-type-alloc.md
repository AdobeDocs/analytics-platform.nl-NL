---
description: Meer informatie over metrische tekst en kenmerk
title: Metrisch type en kenmerk
feature: Calculated Metrics
exl-id: da73a9ba-542e-436c-bdb2-b629b5b6f760
source-git-commit: 8f3b30ca6d20d633669d7e9180884c24e0b9a52e
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 0%

---

# Metrisch type en kenmerk

U kunt metrisch type en [ attributiemodel ](#attribution-models) voor metrisch in een berekende metrische definitie vormen.

1. Selecteer ![ Plaatsend ](/help/assets/icons/Setting.svg) in de metrische component.
1. In het dialoogvenster Pop-up:

   ![ Metrisch type en attributie ](assets/cm-type-alloc.png)

   * Geef de waarde **[!UICONTROL Metric type]** op:

     | Metrisch type | Definitie |
     |---|---|
     | **[!UICONTROL Standard]** | Als een formule uit één enkele standaardmetrische norm bestaat, toont het identieke gegevens aan zijn niet-berekende-metrische tegenhanger. Standaardmetriek zijn handig om berekende metriek te maken die specifiek zijn voor elk afzonderlijk regelitem. <p>Bijvoorbeeld, ](/help/assets/icons/Event.svg) **[!UICONTROL Orders]** ![ de Gebeurtenis van 0} ](/help/assets/icons/Divide.svg) verdeelt ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Sessions]** neemt de orden voor dat specifieke lijnpunt en verdeelt het door het aantal zittingen voor dat specifieke lijnpunt.![ |
     | **[!UICONTROL Grand total]** | Gebruik **[!UICONTROL Grand total]** voor de rapportageperiode in elk regelitem. Als een formule uit één enkel Eindtotaal metrisch bestaat, toont berekende metrisch het zelfde Grote totale aantal op elk lijnpunt. De grote totale metriek zijn nuttig wanneer u berekende metriek wilt tot stand brengen die tegen totale gegevens vergelijkt. <p>Bijvoorbeeld, ](/help/assets/icons/Event.svg) de Gebeurtenis van 0} **[!UICONTROL Orders]** ![ verdeelt ](/help/assets/icons/Divide.svg) ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Total Sessions]** toont het aandeel van orden tegen alle zittingen, niet alleen de zittingen aan het specifieke lijnpunt. ![ In dit voorbeeld, specificeert u **[!UICONTROL Grand Total]** voor de ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Sessions]** metrisch in uw berekende metrisch, die het automatisch in ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Total Sessions]** zal veranderen. |

   * Geef **[!UICONTROL Attribution]** op.

      1. U kunt:

         * Schakel **[!UICONTROL Use non-default attribution model]** uit om het standaard kolomkenmerkingsmodel, Last Touch, te gebruiken met een terugkijkvenster van 30 dagen.
         * Schakel **[!UICONTROL Use non-default attribution model]** in. In het dialoogvenster **[!UICONTROL Column attribution model]**

            * Selecteer een **[!UICONTROL Model]** in de attributiemodellen.
            * Selecteer een **[!UICONTROL Lookback window]** . Als u **[!UICONTROL Custom Time]** selecteert, kunt u de tijdsperiode definiëren in **[!UICONTROL Minute(s)]** tot **[!UICONTROL Quarter(s)]** . Zie [ venster van de Lookback ](#lookback-window) voor meer informatie

      1. Selecteer **[!UICONTROL Apply]** om het niet-standaard toewijzingsmodel toe te passen. Selecteer Annuleren om te annuleren.

     Als u al een niet-standaard toewijzingsmodel hebt gedefinieerd, selecteert u **[!UICONTROL Edit]** om de selectie te wijzigen.

Zie [ Voorbeeld ](#example) voor een voorbeeld om een attributiemodel en raadplegingsvenster te gebruiken.


## Attributie {#attribution}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_nondefaultattributionmodel"
>title="Niet-standaard toewijzingsmodel gebruiken"
>abstract="Schakel een niet-standaard attributiemodel in voor de geselecteerde metrische waarde."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attributionmodel"
>title="Model"
>abstract="Selecteer een attributiemodel voor metrisch."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_lasttouch"
>title="Laatste aanraking"
>abstract="100% van het krediet gaat naar de laatste waarde van de dimensie die een bezoeker heeft gezien."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_firsttouch"
>title="Eerste aanraking"
>abstract="100% van het krediet gaat naar de waarde van de eerste dimensie die een bezoeker ziet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_linear"
>title="Lineair"
>abstract="De creditering wordt gelijkmatig over alle afmetingswaarden verdeeld."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_participation"
>title="Deelname"
>abstract="100% is bestemd voor elke waarde van de dimensie die een bezoeker ziet.<br/> de totalen van de Kolom zijn overdreven."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_sametouch"
>title="Zelfde aanraking"
>abstract="Er wordt alleen rekening gehouden met waarden van dimensies die zich voordoen bij dezelfde gebeurtenis als conversie."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_ushaped"
>title="U-vorm"
>abstract="40% van de kredieten voor de waarde van de eerste dimensie, 40% tot de laatste, 20% gedeeld door het midden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_jcurve"
>title="J Curve"
>abstract="60% is bestemd voor de laatste dimensie, 20% voor de eerste, 20% voor het midden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_inversej"
>title="Omgekeerd J"
>abstract="60% is bestemd voor de waarde van de eerste dimensie, 20% voor de laatste, 20% voor het midden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_timedecay"
>title="Tijdverlies"
>abstract="De waarden van het Dimension dichtst in tijd aan een omzetting krijgen het meeste krediet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_custom"
>title="Tijdverlies"
>abstract="De waarden van het Dimension dichtst in tijd aan een omzetting krijgen het meeste krediet."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_algorithmic"
>title="Algorithmic"
>abstract="Krediet wordt dynamisch bepaald op basis van een statistisch algoritme."

<!-- markdownlint-enable MD034 -->



{{attribution-models-details}}


### Venster Opzoeken {#lookback-window}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_calculatedmetrics_attribution_lookbackwindow"
>title="Venster Opzoeken"
>abstract="Deze instelling bepaalt het venster met gegevenstoewijzing dat voor elke conversie wordt toegepast."

<!-- markdownlint-enable MD034 -->

{{attribution-lookback-window}}


### Voorbeeld van kenmerk {#attribution-example}

Bekijk het volgende voorbeeld:

1. Op 15 september arriveert een persoon via een betaalde zoekadvertentie naar uw site en verlaat hij vervolgens.
1. Op 18 september arriveert de persoon opnieuw naar uw site via een link naar sociale media die hij van een vriend heeft gekregen. Ze voegen verschillende artikelen aan hun winkelwagentje toe, maar kopen niets.
1. Op 24 september stuurt uw marketingteam hen een e-mail met een coupon voor sommige objecten in hun winkelwagentje. Ze passen de coupon toe, maar gaan naar verschillende andere sites om te zien of er andere coupons beschikbaar zijn. Ze vinden een andere advertentie via een advertentie en kopen uiteindelijk $50.

Afhankelijk van het terugkijkvenster en het attributiemodel, ontvangen de kanalen verschillende kredieten. Hieronder volgen enkele voorbeelden:

* Gebruikend **eerste aanraking** en venster van de a **zittingsterugblik**, kijkt de attributie slechts het derde bezoek. Tussen e-mail en display was e-mail de eerste, dus e-mail krijgt 100% krediet voor de aankoop van $50.

* Gebruikend **eerste aanraking** en venster van de a **persoonraadpleging**, kijkt de attributie naar alle drie bezoeken. De betaalde zoekopdracht was de eerste, dus krijgt deze 100% krediet voor de aankoop van $50.

* Gebruikend **lineair** en venster van de a **zittingsterugblik**, is het krediet verdeeld tussen e-mail en vertoning. Beide kanalen krijgen elk $25 krediet.
Gebruikend **lineair** en het venster van de a **persoonraadpleging**, wordt het krediet verdeeld tussen betaald onderzoek, sociaal, e-mail, en vertoning. Elk kanaal krijgt $12,50 krediet voor deze aankoop.

* Gebruikend **j-Gegeld** en a **persoon terugkijkvenster**, wordt het krediet verdeeld tussen betaald onderzoek, sociaal, e-mail, en vertoning.

   * 60% krediet wordt gegeven aan vertoning, voor $30.
   * 20% krediet wordt gegeven voor betaalde zoekopdrachten, voor $10.
   * De resterende 20% is verdeeld tussen sociale media en e-mail, wat elk $5 geeft.

* Gebruikend **Verval van de Tijd** en venster van de a **persoonraadpleging**, wordt het krediet verdeeld tussen betaald onderzoek, sociaal, e-mail, en vertoning. De standaardhalfwaardetijd van 7 dagen gebruiken:

   * Tussenruimte van nul dagen tussen aanraakpunt weergeven en conversie. `2^(-0/7) = 1`
   * Ruimte van nul dagen tussen aanraakpunt en conversie via e-mail. `2^(-0/7) = 1`
   * Tussenruimte van zes dagen tussen sociale aanraakpunten en conversie. `2^(-6/7) = 0.552`
   * Tussenruimte van negen dagen tussen betaald aanraakpunt en conversie. `2^(-9/7) = 0.41`
   * Het normaliseren van deze waarden resulteert in het volgende:

      * Weergave: 33,8%, krijgt $16,88
      * E-mail: 33,8% ontvangt $ 16,88
      * Sociaal: 18,6%, $ 9,32
      * Betaalde zoekopdracht: 13,8%, krijgt $6,92

Conversiegebeurtenissen die doorgaans hele getallen bevatten, worden gedeeld als het krediet tot meer dan één kanaal behoort. Als twee kanalen bijvoorbeeld een bijdrage leveren aan een bestelling met behulp van een lineair toewijzingsmodel, krijgen beide kanalen 0,5 van die volgorde. Deze gedeeltelijke metriek worden samengevat over alle mensen dan rond gemaakt aan het dichtstbijzijnde geheel voor rapportering.


>[!MORELIKETHIS]
>
>[ de componentenmontages van de Attributie ](/help/data-views/component-settings/attribution.md)
>[Metrische deelname ](participation-metric.md)
>

