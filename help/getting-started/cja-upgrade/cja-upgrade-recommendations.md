---
title: Aanbevolen pad bij upgrade van Adobe Analytics naar Customer Journey Analytics
description: Meer informatie over het aanbevolen pad wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: 6fe081690782272f550c8f9c33dfd9ae6b227d13
workflow-type: tm+mt
source-wordcount: '1470'
ht-degree: 0%

---

# Upgrade van Adobe Analytics naar Customer Journey Analytics

Wanneer bevordering van Adobe Analytics aan Customer Journey Analytics, adviseert de Adobe een nieuwe implementatie van het Web SDK van het Experience Platform, samen met de Analytics bronschakelaar, zoals die in [ wordt beschreven Geadviseerde verbeteringsstappen voor de meeste organisaties ](#recommended-upgrade-steps-for-most-organizations).

Afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, zouden de geadviseerde verbeteringsstappen niet praktisch voor uw organisatie kunnen zijn. In dat geval, gebruik [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) om verbeteringsstappen dynamisch te produceren die aan de unieke omstandigheden van uw organisatie worden aangepast.

## Aanbevolen upgradestappen voor de meeste organisaties

>[!NOTE]
>
>De upgrade-stappen die in deze sectie worden beschreven, zijn de aanbevolen upgradestappen die elke organisatie kan gebruiken om een upgrade van Adobe Analytics naar Customer Journey Analytics uit te voeren.
>
>Nochtans, afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, zouden de geadviseerde verbeteringsstappen niet praktisch voor uw organisatie kunnen zijn. In dat geval, gebruik [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) om verbeteringsstappen dynamisch te produceren die aan de unieke omstandigheden van uw organisatie worden aangepast.

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

In de volgende stappen wordt beschreven welk proces wordt aanbevolen voor het upgraden van Adobe Analytics naar Customer Journey Analytics.

Elke stap biedt een verklaring op hoog niveau van een meer gedetailleerd proces. Volg de koppeling voor elke stap en voltooi de bijbehorende taken en ga vervolgens terug naar deze pagina en ga verder met de volgende stap in het proces.

1. [ Plan uw XDM schemaarchitectuur ](/help/getting-started/cja-upgrade/cja-upgrade-schema-architect.md).

1. [ creeer uw gewenste douaneschema in Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md).

   Houd rekening met de volgende opties bij het maken van uw schema:

   * Als u Customer Journey Analytics met RTCDP wilt integreren, moet u de **[!UICONTROL Profile]** optie op uw schema toelaten, zoals die in [ wordt beschreven creeer een schema XDM om met Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md) te gebruiken. Als deze optie is ingeschakeld en gegevens worden opgenomen in gegevenssets die op dit schema zijn gebaseerd, worden die gegevens samengevoegd in het realtime profiel van de klant.

   * Als u het stromen media gegevens wilt omvatten, moet u [ uw schema vormen om het stromen gegevens ](/help/data-ingestion/streaming.md) in te voeren en te gebruiken.

1. [ creeer een dataset in Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-dataset.md).

1. (Optioneel) Als u classificatiegegevens gebruikt in Adobe Analytics, kunt u classificatiegegevens in Customer Journey Analytics toevoegen aan uw gegevensset.

   Creeer een raadplegingsdataset voor elke dimensie die classificatiegegevens bevat.

1. Voor de implementaties van Adobe Analytics die AppMeasurement of de uitbreiding van de Analyse (markeringen) gebruiken, [ creeer een gegevensstroom in Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-datastream.md). <!-- Is this correct? Will customers on the Web SDK already have a datastream that they only need to add AEP as a service to? Or does this step apply to everyone?-->

   Voor Adobe Analytics-implementaties met de Web SDK bestaat al een gegevensstroom.

1. [ voeg Adobe Experience Platform als dienst aan uw datastream ](/help/getting-started/cja-upgrade/cja-upgrade-datastream-addplatform.md) toe.

1. (Optioneel) Als u Customer Journey Analytics wilt integreren met Adobe Journey Optimizer, gebruikt u het aanpassingsobject in uw implementatie voor gebruik in Adobe Journey Optimizer.

1. (Optioneel) Breng historische gegevens van Adobe Analytics met behulp van de bronconnector Analytics.

   Voor meer informatie, zie [ Gebruik een bronschakelaar ](/help/data-ingestion/sources.md#use-a-source-connector) in [ Samenvatten en gebruik gegevens gebruikend bronschakelaars ](/help/data-ingestion/sources.md).

1. Vouw de sectie uit waarin de gewenste Customer Journey Analytics-implementatie wordt beschreven en voer vervolgens de bijbehorende stappen uit:

   +++Handmatige implementatie (JS-bestand)

   1. [ voegt alloy.js aan uw plaats ](https://experienceleague.adobe.com/en/docs/experience-platform/edge/fundamentals/installing-the-sdk#option-2-installing-the-prebuilt-standalone-version%22) toe.

   1. Vul een XDM-object en verzend het naar de gegevensstroom.

+++

   +++Tags

   1. [ creeer een markeringsbezit in de gegevensinzameling van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/get-started/quick-start#create-a-property).

   1. Voeg de extensie Adobe Experience Platform Web SDK toe.

   1. Implementeer de ladertag op uw site.

   1. Voeg XDM-logica voor gegevensverzameling toe aan uw tag.

+++

+++ API

   1. Gebruik de Edge Network-API om gegevens naar de gewenste gegevensstroom te verzenden.

+++

1. Bevestig dat uw implementatie van SDK van het Web gegevens naar een dataset verzendt.

1. [ creeer een verbinding in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-connection.md).

1. (Optioneel) Til webgegevens met gegevens uit andere kanalen, zoals gegevens van het callcenter.

   U verwezenlijkt dit door extra datasets aan uw verbinding van de Customer Journey Analytics toe te voegen.

1. [ creeer een gegevensmening in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md).

1. [ bevestigt dat het gegeven in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-validate.md) stroomt.

1. [ Migreer projecten en componenten ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration).

1. (Facultatief) als u marketing kanalen in Adobe Analytics gebruikt, kunt u [ tot een marketing kanaal afgeleid gebied in Customer Journey Analytics ](/help/data-views/derived-fields/derived-fields.md#marketing-channels) leiden.

   Afgeleide velden zijn een belangrijk aspect van real-time rapportage in Customer Journey Analytics. Een afgeleid gebied staat u toe om (vaak complexe) gegevensmanipulaties op de vlucht, door een klantgerichte regelbouwer te bepalen.

   Eén toepassing voor afgeleide velden is het definiëren van een afgeleid veld Marketing Channel dat het juiste marketingkanaal bepaalt op basis van een of meer voorwaarden (bijvoorbeeld URL-parameter, pagina-URL, paginanaam).

   Gebruik [ het marketing kanaalfunctiesjabloon ](/help/data-views/derived-fields/derived-fields.md#marketing-channels) op afgeleide gebieden om snel een afgeleid gebied voor marketing kanalen tot stand te brengen.

1. Vergelijk gegevens van uw oude implementatie met die van uw nieuwe implementatie en zorg ervoor u om het even welke verschillen begrijpt en waarom zij bestaan.

1. Leer over [ eigenschapsteun in Customer Journey Analytics ](/help/getting-started/aa-vs-cja/cja-aa.md). De meeste Adobe Analytics-functies worden ondersteund in de Customer Journey Analytics en er zijn veel extra functies beschikbaar in de Customer Journey Analytics.

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








