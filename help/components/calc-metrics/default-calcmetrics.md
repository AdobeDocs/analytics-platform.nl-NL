---
description: Adobe biedt verschillende berekende maatstaven die u kunt gebruiken. Deze pagina bevat een overzicht van die metingen en het gebruik waarvoor ze zijn bedoeld.
title: Sjablonen voor berekende metriek
feature: Calculated Metrics
exl-id: 08d11cce-170e-42a2-806f-e0a28b70a2dc
role: User
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Sjablonen voor berekende metriek

Customer Journey Analytics biedt de volgende berekende metriesjablonen voor de meest gebruikte gevallen. Deze Adobe-bepaalde berekende metriek worden geïdentificeerd door een klein ![&#x200B; 1&rbrace; embleem AdobeLogoSmall &lbrace;. &#x200B;](/help/assets/icons/AdobeLogoSmall.svg) Om deze metriek snel te filtreren, selecteer ![&#x200B; Etiket &#x200B;](/help/assets/icons/Label.svg) **[!UICONTROL Adobe Template]** in de [&#x200B; filter van Componenten &#x200B;](/help/components/overview.md#filter).

| Metrische naam berekend | Beschrijving <br/> Formule |
|---------|----------|
| **[!UICONTROL Session start rate]** | Het percentage dat om het even welk afmetingspunt op de eerste gebeurtenis van een zitting voorkwam.<p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Session Starts] [&#x200B; standaardcomponent &#x200B;](/help/data-views/component-reference.md) in uw [&#x200B; gegevensmening &#x200B;](/help/data-views/create-dataview.md) omvat.</p>Samenvatting: **(** ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) **Het begin van de Zitting** ![&#x200B; verdeelt &#x200B;](/help/assets/icons/Divide.svg) ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) **zittingen** **)** |
| **[!UICONTROL Time spent per person]** | De gemiddelde hoeveelheid tijd die een persoon aan om het even welk bepaald afmetingspunt heeft doorgebracht.<p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Time Spent (seconds)] [&#x200B; standaardcomponent &#x200B;](/help/data-views/component-reference.md) in uw [&#x200B; gegevensmening &#x200B;](/help/data-views/create-dataview.md) omvat. Het segment sluit laatste Gebeurtenis van Zitting uit wordt toegepast op metrisch van Mensen uit. Het segment sluit de laatste gebeurtenis van elke zitting in een dataset uit. Deze uitsluiting kan u helpen bij het analyseren van gebruikersgedrag dat leidt tot een gebeurtenis of actie, zoals een aankoop of het verzenden van een formulier, terwijl u de definitieve actie zelf uitsluit.</p>Samenvatting: **(** ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) **bestede Tijd (seconden)** ![&#x200B; verdeelt &#x200B;](/help/assets/icons/Divide.svg) ![&#x200B; Segmentatie &#x200B;](/help/assets/icons/Segmentation.svg) **sluit laatste gebeurtenis van zitting (** ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) **Mensen) uit)** |
| **[!UICONTROL Sessions per person]** | Het gemiddelde aantal sessies per persoon.<p>Samenvatting: **(** ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) **zittingen** ![&#x200B; verdelen &#x200B;](/help/assets/icons/Divide.svg) ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) **Mensen** **)** |
| **[!UICONTROL Time spent per session]** | De gemiddelde hoeveelheid tijd die een persoon per Zitting aan om het even welk bepaald afmetingspunt doorbracht.<p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Time Spent (seconds)] [&#x200B; standaardcomponent &#x200B;](/help/data-views/component-reference.md) in uw [&#x200B; gegevensmening &#x200B;](/help/data-views/create-dataview.md) omvat. Het segment sluit laatste Gebeurtenis van Zitting uit wordt toegepast op metrisch van Zitting. Het segment sluit de laatste gebeurtenis van elke zitting in een dataset uit. Deze uitsluiting kan u helpen bij het analyseren van gebruikersgedrag dat leidt tot een gebeurtenis of actie, zoals een aankoop of het verzenden van een formulier, terwijl u de definitieve actie zelf uitsluit.</p>Samenvatting: **(** ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) **bestede Tijd (seconden)** ![&#x200B; verdeelt &#x200B;](/help/assets/icons/Divide.svg) ![&#x200B; Segmentatie &#x200B;](/help/assets/icons/Segmentation.svg) **sluit laatste gebeurtenis van zitting (** ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) **zittingen)** uit |
| **[!UICONTROL Session end rate]** | Het percentage dat om het even welk afmetingspunt op de laatste gebeurtenis van een zitting voorkwam. <p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Session Ends] [&#x200B; standaardcomponent &#x200B;](/help/data-views/component-reference.md) in uw [&#x200B; gegevensmening &#x200B;](/help/data-views/create-dataview.md) omvat.</p>Samenvatting: **(** ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) **beëindigt de Zitting** ![&#x200B; verdeel &#x200B;](/help/assets/icons/Divide.svg) ![&#x200B; Gebeurtenis &#x200B;](/help/assets/icons/Event.svg) **Zittingen** **)** |
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
