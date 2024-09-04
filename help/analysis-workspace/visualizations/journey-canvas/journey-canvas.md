---
description: Overzicht van het reiscanvas
title: Reiscanvas
feature: Visualizations
role: User
hide: true
hidefromtoc: true
exl-id: be03c3b2-8faf-47b8-b3ab-e953202bf488
source-git-commit: 2f42c64443cc5798388287e6f84b125fb8694812
workflow-type: tm+mt
source-wordcount: '1193'
ht-degree: 0%

---

# Overzicht van het reiscanvas

{{release-limited-testing}}

Met de reiscanvasvisualisatie kunt u uitgebreide inzichten analyseren en verkrijgen over de reizen die u aan uw gebruikers en klanten biedt. Het stelt je in staat om een reis helemaal vanaf het begin te definiëren of een reis vanuit Journey Optimizer te bekijken, dan te zien hoe mensen de reis hebben verlaten (verlaten) of doorgezet (doorheen).

U kunt [ analyses van gebruikersreizen ](/help/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md) bouwen door om het even welke combinatie gebeurtenissen, afmetingspunten, filters, en datumwaaiers te gebruiken om reisknopen tot stand te brengen. Verbind de knopen om de stroom van de reis tot stand te brengen, en veelvoudige wegen en beslissingspunten te omvatten. Sleep knooppunten op het canvas om de gebeurtenissen en omstandigheden van de rit opnieuw te rangschikken. Gegevens worden realtime bijgewerkt terwijl u wijzigingen aanbrengt.

## Belangrijkste kenmerken

De belangrijkste kenmerken van de visualisatie van het canvas Journey zijn:

* Een diepgaande analyse van de uitval en de doorslag die de meest complexe gebruikersreizen mogelijk maakt.

* Een canvas voor het toewijzen en visualiseren van de verschillende ingangspunten, knooppunten en paden van een gebruikersreis.

* Interacties voor slepen en neerzetten om componenten aan het canvas toe te voegen en bestaande knooppunten te verplaatsen.

* De optie om analyses van gebruikersreizen binnen het canvas van de Reis te bouwen of hen automatisch tot stand te brengen die op de reizen van Journey Optimizer worden gebaseerd.

## Potentiële inzichten

Hieronder volgen enkele voorbeelden van de typen inzichten die Journey canvas kan helpen bieden. U kunt kiezen of deze inzichten van alle mensen in de gegevensweergave zijn gebaseerd of op alle mensen die de reis begonnen.

**Fallthrough**

* Het aantal en het percentage personen dat de reis heeft voltooid (aangekomen bij het eindknooppunt)

* Het aantal en het percentage personen dat op een bepaald punt (knooppunt) van de reis aankwam

* De meest voorkomende stap die voor of na een bepaald punt (knooppunt) van de reis is gezet

**Uitval**

* De punten (knooppunten) van de reis waar mensen meestal uit de reis zijn gevallen

**Andere**

* Extra gegevens voor om het even welk knooppunt in de reis (door een afbraakdimensie voor de knoop toe te voegen)


## Kiezen tussen de visualisaties voor het canvas en de valklare taal

De visualisaties van het canvas van de reis zijn gelijkaardig aan [ Vallout visualizations ](/help/analysis-workspace/visualizations/fallout/fallout-flow.md), in die beide visualisaties tonen waar de personen verlieten (vielen uit) en door (vielen door) een vooraf bepaalde opeenvolging van pagina&#39;s verder gingen.

Er zijn echter belangrijke verschillen.

### De verschillen begrijpen

In de volgende tabel worden de typen analyses weergegeven die worden ondersteund in de visualisatie van het canvas Journey en in de visualisatie van de uitvalfunctie:

| Functie | Reiscanvasvisualisatie | Uitvalvisualisatie |
|---------|----------|---------|
| Lineaire reizen | Ja | Ja |
| Niet-lineaire ritten met meerdere toegangspunten en paden | Ja | Nee |
| Adobe Journey Optimizer-reizen | Ja | Nee |
| Primair metrisch | Elke metrische waarde, inclusief berekende metriek | Alleen de afmetingen van de sessie of gebruiker kunnen worden gebruikt |
| Secundair metrisch | Ja<p>Elke metrische waarde, inclusief berekende metriek</p> | Nee |
| Filters vergelijken | Nee | Ja<p>Vergelijk een [ onbeperkt aantal filters ](/help/analysis-workspace/visualizations/fallout/compare-segments-fallout.md#compare-filters-in-fallout)</p> |

### Kies welke visualisatie u wilt gebruiken

Alvorens u tussen het gebruiken van het canvas van de Reis of Vallout kiest, zorg ervoor u [ de verschillen tussen twee ](#understand-the-differences) begrijpt.

Als uw reserveanalyse slechts een lineaire reis impliceert die één enkel bekend begin en eind heeft, denk na gebruikend visualisatie van de a [ Vallout ](/help/analysis-workspace/visualizations/fallout/fallout-flow.md) als eenvoudigere optie voor deze meer eenvoudige gebruikersreizen.

Reiscanvas is van essentieel belang voor een valanalyse waarbij reizen met meerdere toegangspunten en -paden worden gemaakt, of voor het analyseren van reizen die in Journey Optimizer zijn gemaakt.

## Journey Optimizer-reizen analyseren

>[!NOTE]
>
>Als uw organisatie geen toegang tot Journey Optimizer heeft, kunt u nog [ analyses op het canvas van de Reis ](#build-analyses-in-customer-journey-analytics) bouwen.

Het analyseren van Journey Optimizer-reizen op het canvas Journey biedt diepgaande, activeerbare inzichten over hoe mensen met een reis omgaan.

Wanneer u een Journey Optimizer-reis analyseert in het canvas Journey, wordt de reis weergegeven met dezelfde volgorde, volgorde en structuur als in Journey Optimizer. Als u veranderingen in een reis binnen het canvas van de Reis kunt aanbrengen, [ de veranderingen worden niet meer gesynchroniseerd van Journey Optimizer ](#synchronization-between-journey-optimizer-and-journey-canvas).

### Voordelen van het analyseren van Journey Optimizer-reizen met Reiscanvas

Reiscanvas biedt een diepgaande, diepgaande analyse die niet mogelijk is in Journey Optimizer.

Het gebruik van het canvas Journey voor het analyseren van reizen die in Journey Optimizer zijn gemaakt, biedt verschillende voordelen:

* Maak gebeurtenissen met behulp van Customers Journey Analytics, maateenheden, filters of datumbereiken.

  In Journey Optimizer moet een technische gebruiker een gebeurtenis maken voordat deze aan een reis kan worden toegevoegd.

* Creeer publiek dat op een douaneknoop wordt gebaseerd die u creeert (lanceert de het publieksbouwer van de Customer Journey Analytics).

  In Journey Optimizer kunt u alleen een publiek maken voor vooraf gedefinieerde activiteiten.

* Analyseren van fallthrough en fallout

* Gebeurtenissen indelen met elke dimensie

* Gebeurtenissen combineren

* Connect-gebeurtenissen

* Gebeurtenissen hernoemen en verwijderen

* Veel meer

### Synchronisatie tussen Journey Optimizer en Reiscanvas

Nadat u een analyse hebt gemaakt van een Journey Optimizer-reis in het canvas Journey, worden gegevens in slechts één richting gesynchroniseerd, van Journey Optimizer tot het canvas Journey. Dit betekent dat veranderingen die zijn aangebracht in een reis op het canvas Journey nooit worden weerspiegeld in Journey Optimizer.

Bovendien worden wijzigingen in een reis bij Journey Optimizer-synchronisatie alleen doorgevoerd in Journey canvas als de reis ongewijzigd blijft op Journey canvas. Nadat u een reis in het canvas van de Reis wijzigt, worden om het even welke veranderingen u aan de reis in Journey Optimizer aanbrengt niet weerspiegeld in het canvas van de Reis. Om de veranderingen te zien die in het canvas van de Reis worden weerspiegeld, kunt u de reis in het canvas van de Reis schrappen en [ opnieuw creëren ](/help/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md).

### Verschillen na het wijzigen van een reis in het canvas van de Reis {#differences-after-modifying}

Nadat u een reis van Journey Optimizer in het canvas van de Reis wijzigt, kunnen de veranderingen in gegevensverwerking, beschikbare eigenschappen, en synchronisatiegedrag voorkomen.

>[!NOTE]
>
>Als u de oorspronkelijke staat van de reis wilt herstellen, drukt u op Ctrl+z nadat u de eerste wijziging in het canvas Reis hebt aangebracht. Of, kunt u schrappen en [ opnieuw creëren de reis in het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md)

#### Verschillen in gegevensverwerking

Nadat u een reis van Journey Optimizer in het canvas van de Reis wijzigt, zou u veranderingen in uw gegevens kunnen opmerken als uw reis metriek bevat die niet-standaard attributiemodellen hebben.

Dit komt omdat u, in tegenstelling tot Journey Optimizer, met het canvas Journey meerdere dimensies kunt toepassen binnen één reis. Dit vermogen betekent dat [ metrische attributie ](/help/data-views/component-settings/attribution.md) niet wordt gesteund.

#### Verschillen in functies

Nadat u een reis van Journey Optimizer in het canvas van de Reis wijzigt, is het [!UICONTROL **type van Knoop**] drop-down gebied niet meer beschikbaar.

Voor meer informatie over dit gebied, zie [ montages ](/help/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md) vormen.

#### Synchronisatieverschillen

Wijzigingen die in Journey Optimizer tijdens een reis worden aangebracht, worden alleen doorgevoerd in het canvas Journey als de reis ongewijzigd blijft op het canvas Journey.

Nadat u een Journey Optimizer-reis in het canvas Journey hebt aangepast, worden wijzigingen die u aanbrengt in de reis in Journey Optimizer niet meer doorgevoerd in het canvas Journey. Om de veranderingen te zien die in het canvas van de Reis worden weerspiegeld, kunt u de reis in het canvas van de Reis schrappen en [ opnieuw creëren ](/help/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md).

### Terminologische verschillen tussen Journey Optimizer en Customer Journey Analytics

Bepaalde termen die één ding betekenen in Journey Optimizer, betekenen iets anders in de Customer Journey Analytics. Wanneer u het canvas Reis gebruikt, worden de termen Customer Journey Analytics gebruikt.

| Term | Reiscanvas | Journey Optimizer |
|---------|----------|---------|
| **Gebeurtenis** | Één van verscheidene standaardmetriek die in Customer Journey Analytics beschikbaar is. Deze metrische tellingen dingen zoals opbrengst, abonnementen, of geproduceerde lood. | De categorie van activiteit die een gepersonaliseerde reis, zoals een online aankoop teweegbrengt. |

### Een Journey Optimizer-reis analyseren in het canvas Journey

Voor informatie over het analyseren van een reis van Journey Optimizer in het canvas van de Reis, zie [ een visualisatie van het canvas van de Reis vormen ](/help/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md).

## Analyses maken in Reis canvas

U kunt analyses maken op het canvas Journey die zijn gebaseerd op alle afmetingen of maatstaven die beschikbaar zijn in Analysis Workspace. Of je kunt reizen analyseren die gemaakt zijn in Journey Optimizer. Voor meer informatie, zie [ een visualisatie van het canvas van de Reis vormen ](/help/analysis-workspace/visualizations/journey-canvas/configure-journey-canvas.md).
