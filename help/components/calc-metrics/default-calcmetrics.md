---
description: Adobe biedt verschillende berekende maatstaven die u kunt gebruiken. Deze pagina bevat een overzicht van die metingen en het gebruik waarvoor ze zijn bedoeld.
title: Sjablonen voor berekende metriek
feature: Calculated Metrics
exl-id: 08d11cce-170e-42a2-806f-e0a28b70a2dc
role: User
source-git-commit: d13f980d1fbae3f608bf64587f59dc22c3fac9ce
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Sjablonen voor berekende metriek

Customer Journey Analytics verstrekt de volgende berekende metriesjablonen om de gemeenschappelijkste gebruiks-gevallen te behandelen. Deze Adobe bepaalde berekende metriek wordt geïdentificeerd door een klein ![ 1} embleem AdobeLogoSmall {. ](/help/assets/icons/AdobeLogoSmall.svg) Om snel op deze metriek te filtreren, selecteer ![ Etiket ](/help/assets/icons/Label.svg) **[!UICONTROL Adobe Template]** in de [ filter van Componenten ](/help/components/overview.md#filter).

| Metrische naam berekend | Beschrijving <br/> Formule |
|---------|----------|
| **[!UICONTROL Session start rate]** | Het percentage dat om het even welk afmetingspunt op de eerste gebeurtenis van een zitting voorkwam.<p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Session Starts] [ standaardcomponent ](/help/data-views/component-reference.md) in uw [ gegevensmening ](/help/data-views/create-dataview.md) omvat.</p>Samenvatting: **(** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **Het begin van de Zitting** ![ verdeelt ](/help/assets/icons/Divide.svg) ![ Gebeurtenis ](/help/assets/icons/Event.svg) **zittingen** **)** |
| **[!UICONTROL Time spent per person]** | De gemiddelde hoeveelheid tijd die een persoon aan om het even welk bepaald afmetingspunt heeft doorgebracht.<p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Time Spent (seconds)] [ standaardcomponent ](/help/data-views/component-reference.md) in uw [ gegevensmening ](/help/data-views/create-dataview.md) omvat. Het filter Laatste gebeurtenis van Zitting uitsluiten wordt toegepast op metrische personen. De filter sluit de laatste gebeurtenis van elke zitting in een dataset uit. Deze uitsluiting kan u helpen bij het analyseren van gebruikersgedrag dat leidt tot een gebeurtenis of actie, zoals een aankoop of het verzenden van een formulier, terwijl u de definitieve actie zelf uitsluit.</p>Samenvatting: **(** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **bestede Tijd (seconden)** ![ verdeelt ](/help/assets/icons/Divide.svg) ![ Segmentatie ](/help/assets/icons/Segmentation.svg) **sluit laatste gebeurtenis van zitting (** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **Mensen) uit)** |
| **[!UICONTROL Sessions per person]** | Het gemiddelde aantal sessies per persoon.<p>Samenvatting: **(** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **zittingen** ![ verdelen ](/help/assets/icons/Divide.svg) ![ Gebeurtenis ](/help/assets/icons/Event.svg) **Mensen** **)** |
| **[!UICONTROL Time spent per session]** | De gemiddelde hoeveelheid tijd die een persoon per Zitting aan om het even welk bepaald afmetingspunt doorbracht.<p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Time Spent (seconds)] [ standaardcomponent ](/help/data-views/component-reference.md) in uw [ gegevensmening ](/help/data-views/create-dataview.md) omvat. Het filter Laatste gebeurtenis van Zitting uitsluiten wordt toegepast op metrische sessies. De filter sluit de laatste gebeurtenis van elke zitting in een dataset uit. Deze uitsluiting kan u helpen bij het analyseren van gebruikersgedrag dat leidt tot een gebeurtenis of actie, zoals een aankoop of het verzenden van een formulier, terwijl u de definitieve actie zelf uitsluit.</p>Samenvatting: **(** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **bestede Tijd (seconden)** ![ verdeelt ](/help/assets/icons/Divide.svg) ![ Segmentatie ](/help/assets/icons/Segmentation.svg) **sluit laatste gebeurtenis van zitting (** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **zittingen)** uit |
| **[!UICONTROL Session end rate]** | Het percentage dat om het even welk afmetingspunt op de laatste gebeurtenis van een zitting voorkwam. <p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Session Ends] [ standaardcomponent ](/help/data-views/component-reference.md) in uw [ gegevensmening ](/help/data-views/create-dataview.md) omvat.</p>Samenvatting: **(** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **beëindigt de Zitting** ![ verdeel ](/help/assets/icons/Divide.svg) ![ Gebeurtenis ](/help/assets/icons/Event.svg) **Zittingen** **)** |
| **[!UICONTROL Web sessions]** | Het aantal sessies op de website. |
| **[!UICONTROL Survey completion rate]** | De frequentie waarmee mensen een enquête hebben voltooid nadat ze deze hebben gestart. |
| **[!UICONTROL Multi-channel session rate]** | De verhouding van zittingen die voorkwamen die veelvoudige kanalen (zoals Webverkeer en mobiel verkeer) omvatte, vergeleken die die slechts één enkel kanaal omvatte. |
| **[!UICONTROL Multi-channel person rate]** | De verhouding tussen mensen die aan meerdere kanalen hebben deelgenomen, en mensen die slechts aan één kanaal hebben deelgenomen. |
| **[!UICONTROL Mobile app sessions]** | Het aantal sessies dat is opgetreden in de mobiele app. |
| **[!UICONTROL Web+app cross-channel sessions]** | Het aantal sessies dat zowel webverkeer als mobiel verkeer omvatte. |
| **[!UICONTROL Cost of calls]** | De totale kosten voor vraag van het vraagcentrum. <!-- <p>Summary: Call length</p> --> |
| **[!UICONTROL Average call duration]** | De gemiddelde duur van vraag die aan het vraagcentrum wordt gemaakt. |
| **[!UICONTROL Average cost per call]** | De gemiddelde kosten van vraag die aan het callcenter wordt gemaakt. |
| **[!UICONTROL Average call survey score]** | De gemiddelde onderzoeksscore betreffende vraag die aan het vraagcentrum wordt gemaakt. |

{style="table-layout:auto"}
