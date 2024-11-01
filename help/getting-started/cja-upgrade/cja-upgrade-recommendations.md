---
title: Aanbevolen pad bij upgrade van Adobe Analytics naar Customer Journey Analytics
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: ea16705e96047cbcf41e428d2018ea7c72b2afac
workflow-type: tm+mt
source-wordcount: '1419'
ht-degree: 0%

---

# Upgrade van Adobe Analytics naar Customer Journey Analytics

Voordat u begint met het upgradeproces van Adobe Analytics naar Customer Journey Analytics, moet u eerst de aanbevolen upgradestappen begrijpen.

>[!NOTE]
>
>De upgrade-stappen die in deze sectie worden beschreven, zijn de aanbevolen upgradestappen die elke organisatie kan gebruiken om een upgrade van Adobe Analytics naar Customer Journey Analytics uit te voeren.
>
>Nochtans, afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, zouden de geadviseerde verbeteringsstappen niet praktisch voor uw organisatie kunnen zijn. In dat geval, gebruik [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) om verbeteringsstappen dynamisch te produceren die aan de unieke omstandigheden van uw organisatie worden aangepast.

## Aanbevolen upgradestappen voor de meeste organisaties

De geadviseerde stappen wanneer bevordering van Adobe Analytics aan Customer Journey Analytics is een nieuwe implementatie van het Web SDK van het Experience Platform, dat de aangewezen methode van de gegevensinzameling voor Customer Journey Analytics is. In combinatie met de SDK van het Web, adviseert de Adobe ook het gebruiken van de de bronschakelaar van de Analyse om historische gegevens van Adobe Analytics te behouden en zij-aan-zijgegevensvergelijking uit te voeren.

Na volledig transitioning aan Customer Journey Analytics, kan de bron van Analytics schakelaar worden uitgezet en het Web SDK van het Experience Platform kan exclusief worden gebruikt.

### Aanbevolen upgradeproces op hoog niveau

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

### Gedetailleerde aanbevolen upgradestappen

De volgende stappen tonen het aanbevolen proces voor het upgraden van Adobe Analytics naar Customer Journey Analytics.

Afhankelijk van de unieke omgeving en vereisten van uw organisatie zijn deze aanbevolen stappen mogelijk niet geschikt voor uw organisatie. In dat geval, gebruik [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) om verbeteringsstappen dynamisch te produceren die aan de unieke omstandigheden van uw organisatie worden aangepast.

1. [ Plan uw XDM schemaarchitectuur ](/help/getting-started/cja-upgrade/cja-upgrade-schema-architect.md).

1. [ creeer uw gewenste douaneschema in Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md).

1. [ creeer een dataset in Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-dataset.md).

1. Vouw de sectie uit waarin uw huidige Adobe Analytics-implementatie wordt beschreven en voer de bijbehorende stappen uit:

   +++Voor Adobe Analytics-implementaties met AppMeasurement

   1. [ creeer een gegevensstroom in Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-datastream.md). <!-- Is this correct? Will customers on the Web SDK already have a datastream that they only need to add AEP as a service to? Or does this step apply to everyone?-->

+++

   +++Voor Adobe Analytics-implementaties met de extensie Analytics (tags)

   1. [ creeer een gegevensstroom in Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-datastream.md). <!-- Is this correct? Will customers on the Web SDK already have a datastream that they only need to add AEP as a service to? Or does this step apply to everyone?-->

+++

+++ Voor Adobe Analytics-implementaties met de Web SDK

   Er zijn geen extra stappen vereist.

+++

1. [ voeg Adobe Experience Platform als dienst aan uw datastream ](/help/getting-started/cja-upgrade/cja-upgrade-datastream-addplatform.md) toe.

1. Gebruik de volgende lijst om het even welke eigenschappen van Adobe Analytics te identificeren die u in Customer Journey Analytics wilt blijven gebruiken, dan de verstrekte informatie gebruiken om te leren hoe te om die eigenschappen als deel van de verbetering aan Customer Journey Analytics te vormen:

   | Adobe Analytics-functie | Implementatievoorschriften voor Customer Journey Analytics | Aanvullende informatie |
   |---------|----------|---------|
   | Classificatiegegevens | Creeer een raadplegingsdataset voor elke dimensie die classificatiegegevens bevat. |  |
   | Marketingkanalen | Een afgeleid veld voor een marketingkanaal maken. |  |
   | Bedekking activiteitenoverzicht en koppeling bijhouden | N.v.t. | Adobe werkt momenteel aan Activity Map-overlayondersteuning voor Customer Journey Analytics. |
   | Gegevensfeeds | Geen configuratie vereist tijdens implementatie.<br/>[ leer over de diverse uitvoeropties in Customer Journey Analytics ](/help/analysis-workspace/export/export-project-overview.md). | Hoewel een directe vervanging voor de Diervoeders van Gegevens nog niet beschikbaar in Customer Journey Analytics is, kunt u de rapporten van de Customer Journey Analytics van Analysis Workspace voor gebruik in derdehulpmiddelen uitvoeren of met buitengegevens combineren. |
   | Data Warehouse | Geen configuratie vereist tijdens implementatie.<br/>[ Leer over de Volledige Uitvoer van de Lijst in Customer Journey Analytics ](/help/analysis-workspace/export/export-cloud.md). | De Volledige Uitvoer van de Lijst van de Customer Journey Analytics is de evolutie van de rapporten van de Data Warehouse in Adobe Analytics, met vele nieuwe, vaak-gevraagde eigenschappen die niet vandaag in Data Warehouse beschikbaar zijn. |
   | Streaming mediagegevens |  |  |

1. (Optioneel) Breng historische gegevens van Adobe Analytics met behulp van de bronconnector Analytics.

   Voor meer informatie, zie [ Gebruik een bronschakelaar ](/help/data-ingestion/sources.md#use-a-source-connector) in [ Samenvatten en gebruik gegevens gebruikend bronschakelaars ](/help/data-ingestion/sources.md).

1. Gebruik de volgende lijst om het even welke eigenschappen van de Customer Journey Analytics te identificeren die u wilt, dan de verstrekte informatie gebruiken om te leren hoe te om die eigenschappen als deel van de verbetering aan Customer Journey Analytics te vormen:

   | Customer Journey Analytics-eigenschappen die u wilt | Implementatievoorschriften voor Customer Journey Analytics | Aanvullende informatie |
   |---------|----------|---------|
   | Webgegevens met gegevens van andere kanalen zoals de gegevens van het vraagcentrum | Nadat u een verbinding (zoals die in een recentere stap wordt beschreven) creeert, voeg extra datasets aan uw verbinding in Customer Journey Analytics toe. |  |
   | Integreren met RTCDP | Profiel in uw schema inschakelen en een profielgegevensset maken voor gebruik in RTCDP | Dit moet tijdens het maken van uw XDM-schema worden gedaan. |
   | Integreren met Adobe Journey Optimizer | Het personalisatieobject in uw implementatie gebruiken voor gebruik in Adobe Journey Optimizer |  |

1. Vouw de sectie uit waarin de gewenste Customer Journey Analytics-implementatie wordt beschreven en voer vervolgens de bijbehorende stappen uit:

   +++Handmatige implementatie (JS-bestand)

   1. [ voegt alloy.js aan uw plaats ](https://experienceleague.adobe.com/en/docs/experience-platform/edge/fundamentals/installing-the-sdk#option-2-installing-the-prebuilt-standalone-version%22) toe.

+++

   +++Tags

   1. [ creeer een markeringsbezit in de gegevensinzameling van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/get-started/quick-start#create-a-property).

+++

+++ API

   1. Gebruik de Edge Network-API om gegevens naar de gewenste gegevensstroom te verzenden.

+++

1. [ creeer een verbinding in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-connection.md).

1. [ creeer een gegevensmening in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md).

1. [ bevestigt dat het gegeven in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-validate.md) stroomt.

1. [ Migreer projecten en componenten ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration).

1. Vergelijk gegevens van uw oude implementatie met die van uw nieuwe implementatie en zorg ervoor u om het even welke verschillen begrijpt en waarom zij bestaan.

1. De gebruiker aan boord gaan.

   Net als in Adobe Analytics is Analysis Workspace het belangrijkste gebruikersgerichte hulpmiddel in de Customer Journey Analytics. Er zijn echter enkele belangrijke verschillen bij het gebruik van Analysis Workspace in de Customer Journey Analytics die gebruikers moeten onthouden.

   Geef uw gebruikers voldoende tijd (3 - 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Customer Journey Analytics van Analysis Workspace.

   Voor informatie over enkele zeer belangrijke verschillen tussen Adobe Analytics en Customer Journey Analytics, zie [ Gids van de Gebruiker voor de gebruikers van Adobe Analytics ](/help/getting-started/aa-to-cja-user.md).

1. Schakel gegevensverzameling van AppMeasurementen uit.

1. Schakel de bronaansluiting Analytics uit.

   Met de implementatie van SDK van het Web van het Experience Platform, is de bron van Analytics schakelaar nodig slechts voor historische gegevens van Adobe Analytics en om gegevens van uw originele implementatie met dat van uw nieuwe implementatie te vergelijken.

   Wanneer u genoeg historische gegevens van uw nieuwe implementatie hebt en u met de rapporteringsverschillen in Customer Journey Analytics vertrouwd bent, zou u de Analytics bronschakelaar moeten uitzetten.

## Upgrade-stappen voor uw organisatie dynamisch genereren

Afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, begrijpen de geadviseerde verbeteringsstappen die in [ worden beschreven de geadviseerde verbeteringsstappen ](#1-understand-the-recommended-upgrade-steps) niet praktisch voor uw organisatie zou kunnen zijn.

Om verbeteringsstappen voor de unieke omstandigheden van uw organisatie dynamisch te produceren:

1. Voltooi [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/).

   Nadat u deze vragenlijst hebt voltooid, ontvangt u stapsgewijze instructies met een beschrijving van de optimale upgradestappen die uniek zijn voor uw organisatie-vereisten. Dit zijn de verbeteringsstappen die het best met uw bestaande milieu van Adobe Analytics en uw doelstellingen voor Customer Journey Analytics richten.

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









