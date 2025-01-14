---
title: Instellingen van component Attributie
description: Hiermee kunt u de standaardattributie voor een metrische waarde instellen.
exl-id: bc7ae6e3-7c9b-4994-97ce-690f3bdcbee5
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: e4e0c3cf2e865454837df6626c3b1b09f119f07f
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Instellingen van component Attributie {#attribution-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_component_metric_attribution"
>title="Attributie"
>abstract="Vorm het standaardattributiemodel dat op metrisch in rapporten wordt toegepast."

<!-- markdownlint-enable MD034 -->


Met Attributie kunt u aanpassen hoe dimensie-items krediet krijgen voor succesgebeurtenissen.

![ de meningsvenster van Gegevens die de Vastgestelde attributieoptie benadrukken ](../assets/attribution-settings.png)

Bijvoorbeeld:

1. Een persoon op uw site klikt op een koppeling naar een betaalde zoekopdracht naar een van uw productpagina&#39;s. Ze voegen het product aan hun winkelwagentje toe, maar kopen het niet.
2. De volgende dag zien ze een bericht in de sociale media van een van hun vrienden. Ze klikken op de koppeling en voltooien de aankoop.

In sommige rapporten wilt u mogelijk de volgorde toewijzen aan Geavanceerd zoeken. In andere rapporten, zou u de orde aan Sociaal kunnen willen worden toegeschreven. Met kenmerk kunt u dit aspect van rapportage beheren.

## Standaardtoewijzingsmodel van een component instellen

U kunt een standaardattributiemodel voor bepaalde metrisch plaatsen door metrisch het plaatsen in de gegevensmening bij te werken. Als u dit doet, overschrijft u het attributiemodel van de maateenheid op elk moment dat het in Analysis Workspace wordt gebruikt.

>[!NOTE]
>
>Houd rekening met het volgende wanneer u attributie op een metrische waarde inschakelt:
>
>* **wanneer het gebruiken van de component in een rapport met *één enkele afmeting*:** de attributie van de component negeert het toewijzingsmodel wanneer een niet-gebrek attributiemodel wordt gebruikt.
>
>* **wanneer het gebruiken van de component in een rapport met *veelvoudige afmetingen*:** de attributie van de component behoudt het toewijzingsmodel wanneer een niet-gebrek attributiemodel wordt gebruikt.
>
>   De veelvoudige afmetingen zijn beschikbaar slechts wanneer [ het uitvoeren van gegevens aan de wolk ](/help/analysis-workspace/export/export-cloud.md).
>
> Voor meer informatie over toewijzing, zie {de montages van de componenten van 0} Persistence ](/help/data-views/component-settings/persistence.md).[

Het standaardtoewijzingsmodel van een component bijwerken:

1. Ga naar de gegevensmening die de component bevat waarvan standaardattributiemodel u wilt bijwerken.

1. Selecteer de component en vouw vervolgens de sectie Kenmerk aan de rechterkant van het scherm uit.

   ![ de meningsvenster van Gegevens die de Vastgestelde attributieoptie benadrukken ](../assets/attribution-settings.png)

1. Selecteer [!UICONTROL **Vastgestelde attributie**], dan selecteren het attributiemodel in het [!UICONTROL **Model van de Attributie**] drop-down menu.

   Zie [ modellen van de Attributie ](#attribution-models) om over elk attributiemodel te leren.

1. Selecteer [!UICONTROL **sparen en ga**] verder.

>[!TIP]
>
>Als uw organisatie vereist dat metrisch veelvoudige attributie montages heeft, kunt u één van het volgende doen:
>
> * Kopieer de metrische waarde in de gegevensweergave met elke gewenste attributie-instelling. U kunt dezelfde metrische waarde meerdere keren opnemen in een gegevensweergave, zodat elke meting een andere instelling heeft. Zorg ervoor dat u elke metrisch geschikt etiketteert zodat de analisten het verschil tussen deze metriek begrijpen wanneer het produceren van rapporten.
>
> * Overschrijf de metrische waarde in Analysis Workspace. In de montages van de Kolom van metrische [ ](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md), uitgezochte **[!UICONTROL Use non-default attribution model]** om het de attributiemodel van metrische metrische te veranderen en raadplegingsvenster voor dat specifieke rapport.

## Attributiemodellen {#attribution-models}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataviews_component_attribution_attributionmodels"
>title="Model"
>abstract="Selecteer een attributiemodel voor metrisch."

<!-- markdownlint-enable MD034 -->

{{attribution-models-details}}


## Venster Opzoeken

{{attribution-lookback-window}}



## Voorbeeld van kenmerk {#attribution-example}

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


