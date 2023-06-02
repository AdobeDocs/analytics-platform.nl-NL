---
description: Adobe verstrekt diverse berekende metriek die u kunt gebruiken. Deze pagina bevat een overzicht van die metingen en het gebruik waarvoor ze zijn bedoeld.
title: Berekende standaardwaarden
feature: Calculated Metrics
exl-id: 08d11cce-170e-42a2-806f-e0a28b70a2dc
source-git-commit: 5e69b1aceb767343882b9cc85c0011bb1593f4af
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Berekende standaardwaarden

Customer Journey Analytics verstrekt de volgende berekende metriek om de gemeenschappelijkste gebruiks-gevallen te behandelen:

| Metrische naam berekend | Beschrijving | Formule |
|---------|----------|---------|
| Beginsnelheid van sessie | Het percentage dat om het even welk afmetingspunt op de eerste gebeurtenis van een zitting voorkwam.<p>Deze berekende metrisch wordt automatisch toegevoegd aan Werkruimte wanneer u omvat `[Session Starts]` [standaardonderdeel](/help/data-views/component-reference.md) in uw [gegevensweergave](/help/data-views/create-dataview.md).</p> | `[Session Starts] / [Sessions]` |
| Tijd besteed per persoon | De gemiddelde hoeveelheid tijd die een persoon aan om het even welk bepaald afmetingspunt heeft doorgebracht.<p>Deze berekende metrisch wordt automatisch toegevoegd aan Werkruimte wanneer u omvat `[Time Spent (seconds)]` [standaardonderdeel](/help/data-views/component-reference.md) in uw [gegevensweergave](/help/data-views/create-dataview.md).</p> | `[Time Spent (seconds)] / [Users]` |
| Sessies per persoon | Het gemiddelde aantal sessies per persoon. | `[Sessions] / [Users]` |
| Tijd besteed per sessie | De gemiddelde hoeveelheid tijd die een persoon per Zitting aan om het even welk bepaald afmetingspunt doorbracht.<p>Deze berekende metrisch wordt automatisch toegevoegd aan Werkruimte wanneer u omvat `[Time Spent (seconds)]` [standaardonderdeel](/help/data-views/component-reference.md) in uw [gegevensweergave](/help/data-views/create-dataview.md).</p> | `[Time Spent (seconds)] / [Sessions]` |
| Eindfrequentie sessie | Het percentage dat om het even welk afmetingspunt op de laatste gebeurtenis van een zitting voorkwam. <p>Deze berekende metrisch wordt automatisch toegevoegd aan Werkruimte wanneer u omvat `[Session Ends]` [standaardonderdeel](/help/data-views/component-reference.md) in uw [gegevensweergave](/help/data-views/create-dataview.md).</p> | `[Session Ends] / [Sessions]` |

{style="table-layout:auto"}
