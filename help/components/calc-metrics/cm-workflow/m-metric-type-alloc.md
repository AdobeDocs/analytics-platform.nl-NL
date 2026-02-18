---
description: Meer informatie over metrische tekst en kenmerk.
title: Type en kenmerk van de meter
feature: Calculated Metrics
exl-id: da73a9ba-542e-436c-bdb2-b629b5b6f760
source-git-commit: c209341400bf4e0c00719075f0fc82f81ca9dbb4
workflow-type: tm+mt
source-wordcount: '571'
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
     | **[!UICONTROL Standard]** | Als een formule uit één enkele standaardmetrische norm bestaat, toont het identieke gegevens aan zijn niet-berekende-metrische tegenhanger. Standaardmetriek zijn handig om berekende metriek te maken die specifiek zijn voor elk afzonderlijk regelitem. <p>Bijvoorbeeld, ![ ](/help/assets/icons/Event.svg) **[!UICONTROL Orders]** de Gebeurtenis van 0} ![ verdeelt ](/help/assets/icons/Divide.svg) Gebeurtenis ![ ](/help/assets/icons/Event.svg) neemt de orden voor dat specifieke lijnpunt en verdeelt het door het aantal zittingen voor dat specifieke lijnpunt.**[!UICONTROL Sessions]** |
     | **[!UICONTROL Grand total]** | Gebruik **[!UICONTROL Grand total]** voor de rapportageperiode in elk regelitem. Als een formule uit één enkel Eindtotaal metrisch bestaat, toont berekende metrisch het zelfde Grote totale aantal op elk lijnpunt. De grote totale metriek zijn nuttig wanneer u berekende metriek wilt tot stand brengen die tegen totale gegevens vergelijkt. <p>Bijvoorbeeld, ![ de Gebeurtenis van 0} ](/help/assets/icons/Event.svg) **[!UICONTROL Orders]** verdeelt ![ ](/help/assets/icons/Divide.svg) Gebeurtenis ![ ](/help/assets/icons/Event.svg) toont het aandeel van orden tegen alle zittingen, niet alleen de zittingen aan het specifieke lijnpunt. **[!UICONTROL Total Sessions]** In dit voorbeeld, specificeert u **[!UICONTROL Grand Total]** voor de ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Sessions]** metrisch in uw berekende metrisch, die het automatisch in ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Total Sessions]** zal veranderen. |

   * Geef **[!UICONTROL Attribution]** op.

      1. U kunt:

         * Schakel **[!UICONTROL Use non-default attribution model]** uit om het standaard kolomkenmerkingsmodel, Last Touch, te gebruiken met een terugkijkvenster van 30 dagen.
         * Schakel **[!UICONTROL Use non-default attribution model]** in. In het dialoogvenster **[!UICONTROL Column attribution model]**

            * Selecteer a **[!UICONTROL Model]** van de [ attributiemodellen ](#attribution-models).
            * Selecteer a **[!UICONTROL Container]** van de [ container ](#container) opties.
            * Selecteer a **[!UICONTROL Lookback window]** van de [ raadplegingsvenster ](#lookback-window) opties. Als u **[!UICONTROL Custom Time]** selecteert, kunt u de tijdsperiode definiëren in **[!UICONTROL Minute(s)]** tot **[!UICONTROL Quarter(s)]** .

      1. Selecteer **[!UICONTROL Apply]** om het niet-standaard toewijzingsmodel toe te passen. Selecteer Annuleren om te annuleren.

     Als u al een niet-standaard toewijzingsmodel hebt gedefinieerd, selecteert u **[!UICONTROL Edit]** om de selectie te wijzigen.

Zie [ Voorbeeld ](#example) voor een voorbeeld om een attributiemodel, container, en raadplegingsvenster te gebruiken.


## Attributiemodellen {#attribution-models}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_nondefaultattributionmodel"
>title="Niet-standaard toewijzingsmodel gebruiken"
>abstract="Schakel een niet-standaard attributiemodel in voor de geselecteerde metrische waarde."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attributionmodel"
>title="Model"
>abstract="Selecteer een attributiemodel voor metrisch."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_lasttouch"
>title="Laatste aanraking"
>abstract="100% van het krediet gaat naar de laatste waarde van de dimensie die een bezoeker heeft gezien."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_firsttouch"
>title="Eerste aanraking"
>abstract="100% van het krediet gaat naar de waarde van de eerste dimensie die een bezoeker ziet."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_linear"
>title="Lineair"
>abstract="De creditering wordt gelijkmatig over alle afmetingswaarden verdeeld."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_participation"
>title="Deelname"
>abstract="100% is bestemd voor elke waarde van de dimensie die een bezoeker ziet.<br/> de totalen van de Kolom zijn overdreven."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_sametouch"
>title="Zelfde aanraking"
>abstract="Er wordt alleen rekening gehouden met waarden van dimensies die zich voordoen bij dezelfde gebeurtenis als conversie."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_instance"
>title="Zelfde aanraking"
>abstract="Er wordt alleen rekening gehouden met waarden van dimensies die zich voordoen bij dezelfde gebeurtenis als conversie."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_ushaped"
>title="U-vorm"
>abstract="40% van de kredieten voor de waarde van de eerste dimensie, 40% tot de laatste, 20% gedeeld door het midden."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_jcurve"
>title="J Curve"
>abstract="60% is bestemd voor de laatste dimensie, 20% voor de eerste, 20% voor het midden."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_jshaped"
>title="J Curve"
>abstract="60% is bestemd voor de laatste dimensie, 20% voor de eerste, 20% voor het midden."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_inversej"
>title="Omgekeerd J"
>abstract="60% is bestemd voor de waarde van de eerste dimensie, 20% voor de laatste, 20% voor het midden."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_reversejshaped"
>title="Omgekeerd J"
>abstract="60% is bestemd voor de waarde van de eerste dimensie, 20% voor de laatste, 20% voor het midden."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_timedecay"
>title="Tijdverlies"
>abstract="Dimension-waarden die het dichtst bij een conversie liggen, krijgen het meeste krediet."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_custom"
>title="Aangepast"
>abstract="Definieer uw eigen op positie gebaseerde toewijzingsweging."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_positionbased"
>title="Aangepast"
>abstract="Definieer uw eigen op positie gebaseerde toewijzingsweging."

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_algorithmic"
>title="Algorithmic"
>abstract="Krediet wordt dynamisch bepaald op basis van een statistisch algoritme."

{{attribution-models-details}}


## Container {#container}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_container"
>title="Container"
>abstract="Selecteer een container om het gewenste bereik voor de toewijzing in te stellen."

{{attribution-container}}


## Venster Opzoeken {#lookback-winwow}

>[!CONTEXTUALHELP]
>id="components_calculatedmetrics_attribution_lookbackwindow"
>title="Venster Opzoeken"
>abstract="Deze instelling bepaalt het venster met gegevenstoewijzing dat voor elke conversie wordt toegepast."

{{attribution-lookback-window}}




## Voorbeeld

{{attribution-example}}

>[!MORELIKETHIS]
>
>[ de componentenmontages van de Attributie ](/help/data-views/component-settings/attribution.md)
>[Metrische deelname ](participation-metric.md)
>

