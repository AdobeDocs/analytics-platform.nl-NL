---
description: De Adobe verstrekt diverse berekende metriek die u kunt gebruiken. Deze pagina bevat een overzicht van die metingen en het gebruik waarvoor ze zijn bedoeld.
title: Berekende standaardwaarden
feature: Calculated Metrics
exl-id: 08d11cce-170e-42a2-806f-e0a28b70a2dc
role: User
source-git-commit: a507417c945f827ebb8bc92f7b5f54a9c4e6faa0
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Berekende standaardwaarden

Customer Journey Analytics verstrekt de volgende standaard berekende metriek om de gemeenschappelijkste gebruiks-gevallen te behandelen. Deze Adobe bepaalde gebrek berekende metriek wordt geïdentificeerd door een klein ![ 1} embleem AdobeLogoSmall {. ](/help/assets/icons/AdobeLogoSmall.svg) Om snel op deze metriek te filtreren, selecteer ![ Etiket ](/help/assets/icons/Label.svg) **[!UICONTROL Adobe Template]** in de [ filter van Componenten ](/help/components/overview.md#filter).

| Metrische naam berekend | Beschrijving <br/> Formule |
|---------|----------|
| **[!UICONTROL Session Start Rate]** | Het percentage dat om het even welk afmetingspunt op de eerste gebeurtenis van een zitting voorkwam.<p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Session Starts] [ standaardcomponent ](/help/data-views/component-reference.md) in uw [ gegevensmening ](/help/data-views/create-dataview.md) omvat.</p>Samenvatting: **(** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **Zitting begint** ![ verdelen ](/help/assets/icons/Divide.svg) ![ Gebeurtenis ](/help/assets/icons/Event.svg) **zittingen** **)** |
| **[!UICONTROL Time Spent Per Person]** | De gemiddelde hoeveelheid tijd die een persoon aan om het even welk bepaald afmetingspunt heeft doorgebracht.<p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Time Spent (seconds)] [ standaardcomponent ](/help/data-views/component-reference.md) in uw [ gegevensmening ](/help/data-views/create-dataview.md) omvat. Het filter Laatste gebeurtenis van Zitting uitsluiten wordt toegepast op metrische personen. De filter sluit de laatste gebeurtenis van elke zitting in een dataset uit. Deze uitsluiting kan u helpen bij het analyseren van gebruikersgedrag dat leidt tot een gebeurtenis of actie, zoals een aankoop of het verzenden van een formulier, terwijl u de definitieve actie zelf uitsluit.</p>Samenvatting: **(** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **Tijd bestede (seconden)** ![ verdeel ](/help/assets/icons/Divide.svg) ![ Segmentatie ](/help/assets/icons/Segmentation.svg) **sluit Laatste Gebeurtenis van Zitting (** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **Mensen) uit)** |
| **[!UICONTROL Sessions Per Person]** | Het gemiddelde aantal sessies per persoon.<p>Samenvatting: **(** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **zittingen** ![ verdelen ](/help/assets/icons/Divide.svg) ![ Gebeurtenis ](/help/assets/icons/Event.svg) **Mensen** **)** |
| **[!UICONTROL Time Spent Per Session]** | De gemiddelde hoeveelheid tijd die een persoon per Zitting aan om het even welk bepaald afmetingspunt doorbracht.<p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Time Spent (seconds)] [ standaardcomponent ](/help/data-views/component-reference.md) in uw [ gegevensmening ](/help/data-views/create-dataview.md) omvat. Het filter Laatste gebeurtenis van Zitting uitsluiten wordt toegepast op metrische sessies. De filter sluit de laatste gebeurtenis van elke zitting in een dataset uit. Deze uitsluiting kan u helpen bij het analyseren van gebruikersgedrag dat leidt tot een gebeurtenis of actie, zoals een aankoop of het verzenden van een formulier, terwijl u de definitieve actie zelf uitsluit.</p>Samenvatting: **(** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **Tijd bestede (seconden)** ![ verdeel ](/help/assets/icons/Divide.svg) ![ Segmentatie ](/help/assets/icons/Segmentation.svg) **sluit Laatste Gebeurtenis van Zitting (** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **zittingen)** uit |
| **[!UICONTROL Session End Rate]** | Het percentage dat om het even welk afmetingspunt op de laatste gebeurtenis van een zitting voorkwam. <p>Dit berekende metrisch wordt automatisch toegevoegd aan Workspace wanneer u de [!UICONTROL Session Ends] [ standaardcomponent ](/help/data-views/component-reference.md) in uw [ gegevensmening ](/help/data-views/create-dataview.md) omvat.</p>Samenvatting: **(** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **Zitting beëindigt** ![ verdeel ](/help/assets/icons/Divide.svg) ![ Gebeurtenis ](/help/assets/icons/Event.svg) **zittingen** **)** |

{style="table-layout:auto"}
