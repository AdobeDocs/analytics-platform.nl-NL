---
description: 'null'
title: Overzicht van deelvensters
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 2%

---


# Overzicht van deelvensters

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Een deelvenster is een verzameling tabellen en visualisaties. U hebt toegang tot deelvensters via het pictogram linksboven in Workspace. Deelvensters zijn handig wanneer u uw projecten wilt ordenen op basis van tijdsperiodes, bedrijfseenheden, geografie, enzovoort. Deze vier typen deelvensters zijn beschikbaar in Analysis Workspace voor Customer Journey Analytics:

* [Leeg deelvenster](blank-panel.md)
* [Deelvenster Snelle inzichten](quickinsight.md)
* [Deelvenster voor attributie](attribution.md)
* [Deelvenster Vrije vorm](freeform-panel.md)

Deelvensters Snelle inzichten, Lege tinten en Vrije vorm zijn ideale startpunten voor uw analyse, terwijl het deelvenster Kenmerken van IQ zichzelf leent voor geavanceerdere analyses. Een `"+"` knop is beschikbaar in projecten, zodat u op elk gewenst moment lege deelvensters kunt toevoegen.

Het standaardbeginvenster is het deelvenster Vrije vorm, maar u kunt ook het [lege deelvenster](/help/analysis-workspace/c-panels/blank-panel.md) als standaard instellen.

## Vervolgkeuzefilters in deelvensters

De dropzone van het deelvenster heeft vervolgkeuzemogelijkheden voor filteren. Met deze filters kunt u op beheerste wijze werken met de projectgegevens, zodat u diepgaande analyses kunt uitvoeren, uw projecten kunt vereenvoudigen en/of inzichten met anderen kunt delen.

Hier is een voorbeeld van een vereenvoudigd project: Stel dat u verschillende versies van een project/deelvenster hebt om landenspecifieke rapporten op te stellen. U kunt deze projecten/deelvensters nu samenvouwen tot één deelvenster en in een vervolgkeuzelijst met landen toevoegen om te filteren tussen verschillende gegevenssets.

![](assets/dropdowns.png)

Houd dit in gedachten:

* U kunt in veelvoudige componenten (of afmetingspunten) vallen, en dan tussen hen in een dropdown schakelen om de paneelinhoud te filtreren.
* U kunt ook meerdere vervolgkeuzelijsten maken in hetzelfde deelvenster.
* U kunt de titel van de vervolgkeuzelijst aanpassen door op de titel te klikken en deze te wijzigen, of u kunt de titel helemaal verwijderen door op de x naast de titel te klikken.
* U kunt drop-down filters tot stand brengen gebruikend om het even welk componententype: afmetingen, datumbereiken, segmenten en metriek. De datumbereiken in de vervolgkeuzelijst hebben altijd voorrang op de datumbereiken in het deelvenster.
* De kleuren van de component blijven behouden vanaf de linkerspoorstaaf: geel voor de dalingen van afmetingspunt, groen voor metriek, blauw voor segmenten, en paars voor datumwaaiers.
* De dropzone maakt nog steeds raaksegmenten voor items die als segmenten worden gesleept. U kunt deze zoals gewoonlijk wijzigen door het informatiepictogram (i) naast het segment, dan het potloodvormig uitgeeft pictogram te klikken en het in de Bouwer van het Segment uit te geven.

**Vervolgkeuzefilters maken en gebruiken:**

1. Selecteer items in het linkerspoor en zet ze, **terwijl u de toets** ingedrukt houdt, neer in de neerzetzone van het deelvenster.

   ![](assets/create_dropdown.png)

   Hierdoor worden de componenten omgezet in een vervolgkeuzelijst in plaats van in een segment. (U kunt ook segmenten toevoegen door de toets niet ingedrukt te houden.)

   ![](assets/dropdown.png)

1. Selecteer een van de opties in het vervolgkeuzemenu om de gegevens in het onderstaande deelvenster te wijzigen. (U kunt er ook voor kiezen om geen van de deelvenstergegevens te filteren door te selecteren **[!UICONTROL No filter]**.)
1. Als u de gegevens bijvoorbeeld ook via een marketingkanaal wilt segmenteren, kunt u een ander vervolgkeuzemenu met de naam &quot;Marketing Channel&quot; toevoegen:

   ![](assets/mc_dropdown.png)

