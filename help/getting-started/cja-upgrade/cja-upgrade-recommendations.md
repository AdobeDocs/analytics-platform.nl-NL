---
title: Aanbevolen pad bij upgrade van Adobe Analytics naar Customer Journey Analytics
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: 711e92db7084592dc562eda3d0dcf33bcb4a62d4
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---

# Upgrade van Adobe Analytics naar Customer Journey Analytics

Voordat u begint met het upgradeproces van Adobe Analytics naar Customer Journey Analytics, moet u eerst de aanbevolen upgradestappen begrijpen.

Afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, zouden de geadviseerde verbeteringsstappen niet praktisch voor uw organisatie kunnen zijn. Nadat u de aanbevolen stappen voor upgrades hebt begrepen, vult u de vragenlijst in om upgradestappen dynamisch te genereren die zijn afgestemd op de unieke omstandigheden van uw organisatie.

## 1. Inzicht in de aanbevolen stappen voor upgrades

>[!NOTE]
>
>De upgrade-stappen die in deze sectie worden beschreven, zijn de aanbevolen upgradestappen die elke organisatie kan gebruiken om een upgrade van Adobe Analytics naar Customer Journey Analytics uit te voeren.
>
>Nochtans, afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, zouden de geadviseerde verbeteringsstappen niet praktisch voor uw organisatie kunnen zijn. Nadat u de geadviseerde verbeteringsstappen begrijpt, voltooi [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) om verbeteringsstappen dynamisch te produceren die aan de unieke omstandigheden van uw organisatie worden aangepast.

De geadviseerde stappen wanneer bevordering van Adobe Analytics aan Customer Journey Analytics is een nieuwe implementatie van het Web SDK van het Experience Platform, dat de aangewezen methode van de gegevensinzameling voor Customer Journey Analytics is. In combinatie met de SDK van het Web, adviseert de Adobe ook het gebruiken van de de bronschakelaar van de Analyse om historische gegevens van Adobe Analytics te behouden en zij-aan-zijgegevensvergelijking uit te voeren.

Na volledig transitioning aan Customer Journey Analytics, kan de bron van Analytics schakelaar worden uitgezet en het Web SDK van het Experience Platform kan exclusief worden gebruikt.

1. **voer SDK van het Web van Experience Platforms uit**

   Een nieuwe implementatie van het Web SDK van het Experience Platform is de beste manier om gegevens voor Customer Journey Analytics te verzamelen. Het biedt de beste basis om het meeste uit Customer Journey Analytics te halen, omdat het de krachtigste, ongecompliceerde en toekomstbestendige methode is voor het implementeren van Customer Journey Analytics.

   * Zeer krachtige rapportering en beschikbaarheid van gegevens, omdat Adobe Experience Platform is gebouwd voor het gebruik van realtime personalisatie

   * Consolideer implementatie voor Adobe Experience Cloud-gegevensverzameling tussen andere producten van Experiencen Cloud (AJO, RTCDP, enzovoort)

   * Niet afhankelijk van de Adobe Analytics-nomenclatuur (voor prop, eVar, gebeurtenis, enzovoort)

1. **Opstelling de bron van Adobe Analytics schakelaar**

   Om met een vlotte overgang te helpen om het Web SDK van het Experience Platform met Customer Journey Analytics te gebruiken, adviseert de Adobe ook het gebruiken van de bron van Adobe Analytics schakelaar. Dit staat u toe om historische gegevens te behouden en gegevens van uw bestaande implementatie van Adobe Analytics in Customer Journey Analytics, zij aan zij met de gegevens van uw nieuwe implementatie van SDK van het Web van Experience Platforms te bekijken.

   Met de bronaansluiting Analytics kunt u:

   * Breng uw historische Adobe Analytics-rapportenpakket gegevens naar Adobe Experience Platform en Customer Journey Analytics.

     U kunt de gegevensbronaansluiting voor Analytics zo lang actief houden als u nodig hebt om de historische Adobe Analytics-gegevens te behouden.

   * Bekijk de gegevens die met uw originele implementatie van Adobe Analytics (of AppMeasurement, de Uitbreiding van Analytics, of de Uitbreiding van SDK van het Web) binnen Customer Journey Analytics worden verzameld. U kunt deze gegevens zij aan zij met dat van uw nieuwe implementatie van SDK van het Web vergelijken.

     U kunt de bronaansluiting voor Analytics actief houden totdat u bekend bent met de verschillen en deze op uw gemak kunt gebruiken. <!--elaborate on what those differences are? -->

   De bronschakelaar van de Analyse als stand-alone implementatie is geen geadviseerde methode op lange termijn voor het gebruiken van Customer Journey Analytics. Dit is wegens hoge latentie, geclusterde en complexe schema&#39;s, vertrouwen op de nomenclatuur van Adobe Analytics (steun, eVar, etc.), en moeilijkheden in uiteindelijk het bewegen van de bronschakelaar aan de geadviseerde implementatie van SDK van het Web.

## 2. Voer dynamisch upgradestappen voor uw organisatie uit

Afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, begrijpen de geadviseerde verbeteringsstappen die in [ worden beschreven de geadviseerde verbeteringsstappen ](#1-understand-the-recommended-upgrade-steps) niet praktisch voor uw organisatie zou kunnen zijn.

Om de dynamisch geproduceerde verbeteringsstappen voor de unieke omstandigheden van uw organisatie te bekijken:

1. Voltooi [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/).

   Nadat u deze vragenlijst hebt voltooid, ontvangt u stapsgewijze instructies waarin u de optimale upgradestappen beschrijft die uniek zijn voor uw organisatie. Dit zijn de verbeteringsstappen die het best met uw bestaande milieu van Adobe Analytics en uw doelstellingen voor Customer Journey Analytics richten.

1. Volg de gegenereerde stapsgewijze instructies om te upgraden naar Customer Journey Analytics.

<!--

Customer Journey Analytics is the next generation of analytics. It allows multi-channel data collection (both online and offline data), combined with powerful report-time processing functionality (through the definition of components and derived fields in data views). 



When upgrading from Adobe Analytics to Customer Journey Analytics, no single set of upgrade steps exist that are optimal for every organization.

Adobe recommends using the dynamically generated upgrade steps that are unique to your organization. These upgrade steps are generated after you complete an upgrade questionnaire, which helps you understand the best way for your organization to upgrade to Customer Journey Analytics. 

Generic upgrade steps are also available.

1. **Implement the Experience Platform Web SDK**

   A new implementation of the Experience Platform Web SDK provides the best foundation to get the most out of Customer Journey Analytics. 
   
   It is the most performant, straightforward, and future-proof method for implementing Customer Journey Analytics:

   * Highly performant reporting and data availability because Adobe Experience Platform is built to power real-time personalization use cases

   * Consolidate implementation for Adobe Experience Cloud data collection between other Experience Cloud products (AJO, RTCDP, and so forth)

   * Not reliant on Adobe Analytics nomenclature (prop, eVar, event, and so forth)

1. **Set up the Adobe Analytics source connector**

   The Analytics source connector is a recommended part of the piece when upgrading to Customer Journey Analytics. 

   The Analytics source connector allows you to:

   * Bring your historical Adobe Analytics report suite data into Adobe Experience Platform and Customer Journey Analytics. 
   
     You can keep the Analytics source connector running for as long as you need to retain the historical Adobe Analytics data. 
   
   * View the data collected with your original Adobe Analytics implementation (either AppMeasurement, the Analytics Extension, or the Web SDK Extension) within Customer Journey Analytics. You can compare this data side-by-side with that of your new Web SDK implementation. 
   
     You can keep the Analytics source connector running until you are familiar and comfortable with the differences. <!--elaborate on what those differences are? -->

<!--

   When you no longer need the Analytics source connector because you have enough historical data from your new implementation and you are familiar with the reporting differences in Customer Journey Analytics, you should turn off the Analytics source connector. With the Experience Platform Web SDK implementation, the Analytics source connector is not needed.  
   
   The Analytics source connector as a stand-alone implementation is not a recommended long-term method for using Customer Journey Analytics. This is because of high latency, cluttered and complex schemas, reliance on Adobe Analytics nomenclature (prop, eVar, and so forth), and difficulty in eventually moving from the source connector to the recommended Web SDK implementation. 
   
-->









