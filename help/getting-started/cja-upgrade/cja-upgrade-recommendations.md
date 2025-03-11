---
title: Upgrade van Adobe Analytics naar Customer Journey Analytics
description: Meer informatie over de aanbevolen stappen bij het upgraden van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: d35f8615-66f5-4823-b0b8-433852246dd2
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '1616'
ht-degree: 0%

---

# Upgrade van Adobe Analytics naar Customer Journey Analytics

Wanneer bevordering van Adobe Analytics aan Customer Journey Analytics, kunt u de [ geadviseerde verbeteringsstappen ](#recommended-upgrade-steps-for-most-organizations) volgen. Of u kunt [ verbeteringsstappen ](#dynamically-generate-upgrade-steps-for-your-organization) voor de unieke omstandigheden van uw organisatie dynamisch produceren.

## Aanbevolen upgradestappen voor de meeste organisaties {#upgrade-process}

Het aanbevolen proces om van Adobe Analytics naar Customer Journey Analytics te upgraden is een nieuwe implementatie van de Experience Platform Web SDK, de voorkeursmethode voor gegevensverzameling voor Customer Journey Analytics. In combinatie met de Web SDK raadt Adobe u ook aan om de Analytics-bronconnector te gebruiken als hulp bij de overgang naar Customer Journey Analytics. Gebruik de gegevensbronconnector Analytics om historische Adobe Analytics-gegevens te behouden en gegevens naast elkaar te vergelijken.

Nadat u genoeg historische gegevens gebruikend het Web SDK van Experience Platform hebt en u volledig aan Customer Journey Analytics overgegaan, kan de Analytics bronschakelaar worden uitgezet en het Web SDK kan exclusief worden gebruikt.

>[!NOTE]
>
>Als de upgrade-stappen die in deze sectie worden beschreven niet praktisch zijn voor uw organisatie, gebruikt u de Customer Journey Analytics Upgrade Guide om upgradestappen dynamisch te genereren die zijn afgestemd op de unieke omstandigheden van uw organisatie. (Als u vanuit Customer Journey Analytics toegang wilt krijgen tot de hulplijn, selecteert u de tab **[!UICONTROL Workspace]** en vervolgens **[!UICONTROL Upgrade to Customer Journey Analytics]** in het linkerdeelvenster. Volg de aanwijzingen op het scherm.)

### Aanbevolen upgradeproces op hoog niveau {#high-level-upgade-process}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-historical-data"
>title="Historische gegevens van Adobe Analytics"
>abstract="Breng uw historische Adobe Analytics-rapportenpakket gegevens naar Adobe Experience Platform en Customer Journey Analytics."

<!-- markdownlint-enable MD034 -->

1. **voer SDK van het Web van Experience Platform (voor aan de gang zijnde gegevensinzameling) uit**

   Een nieuwe implementatie van de Experience Platform Web SDK is de beste manier om gegevens voor Customer Journey Analytics te verzamelen. Het biedt de beste basis om het beste uit Customer Journey Analytics te halen, omdat het de krachtigste, ongecompliceerde en toekomstbestendige methode is voor de implementatie van Customer Journey Analytics.

   * Zeer krachtige rapportering en beschikbaarheid van gegevens, omdat Adobe Experience Platform is gebouwd voor het gebruik van realtime personalisatie

   * Consolideer implementatie voor Adobe Experience Cloud-gegevensverzameling tussen andere Experience Cloud-producten (AJO, RTCDP, enzovoort)

   * Niet afhankelijk van de Adobe Analytics-nomenclatuur (zoals prop, eVar, event, enzovoort)

1. **opstelling de Adobe Analytics bronschakelaar (voor het brengen over historische gegevens)**

   Voor een vloeiende overgang naar de Experience Platform Web SDK met Customer Journey Analytics raadt Adobe ook aan de Adobe Analytics-bronaansluiting te gebruiken. Hierdoor kunt u historische gegevens behouden en gegevens van uw bestaande Adobe Analytics-implementatie in Customer Journey Analytics naast elkaar weergeven met de gegevens van uw nieuwe Experience Platform Web SDK-implementatie.

   Met de bronaansluiting Analytics kunt u:

   * Breng uw historische Adobe Analytics-rapportenpakket gegevens naar Adobe Experience Platform en Customer Journey Analytics.

     U kunt de gegevensbronaansluiting voor Analytics zo lang actief houden als u nodig hebt om de historische Adobe Analytics-gegevens te behouden.

   * Bekijk de gegevens die zijn verzameld met de oorspronkelijke Adobe Analytics-implementatie (AppMeasurement, de analytische extensie of de Web SDK Extension) in Customer Journey Analytics. U kunt deze gegevens naast elkaar vergelijken met die van uw nieuwe implementatie van SDK van het Web.

     U kunt de bronaansluiting voor Analytics actief houden totdat u bekend bent met de verschillen en deze op uw gemak kunt gebruiken. <!--elaborate on what those differences are? -->

   De bronconnector van Analytics als zelfstandige implementatie is geen aanbevolen langetermijnmethode voor het gebruik van Customer Journey Analytics. Dit komt door de hoge latentie, geclusterde en complexe schema&#39;s, het vertrouwen op de nomenclatuur van Adobe Analytics (eigenschap, eVar, enzovoort), en het probleem om uiteindelijk van de de bronschakelaar van de Analytics aan de geadviseerde implementatie van SDK van het Web over te gaan.

### Gedetailleerde aanbevolen upgradestappen

In de volgende stappen wordt beschreven welk proces wordt aanbevolen voor het upgraden van Adobe Analytics naar Customer Journey Analytics.

Elke stap biedt een verklaring op hoog niveau van een meer gedetailleerd proces. Volg de koppeling voor elke stap en voltooi de bijbehorende taken en ga vervolgens terug naar deze pagina en ga verder met de volgende stap in het proces.

1. [ Plan uw XDM schemaarchitectuur ](/help/getting-started/cja-upgrade/cja-upgrade-schema-architect.md).

1. [ creeer uw gewenste douaneschema in Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md).

   Houd rekening met de volgende opties bij het maken van uw schema:

   * Als u Customer Journey Analytics met RTCDP wilt integreren, moet u de **[!UICONTROL Profile]** optie op uw schema toelaten, zoals die in [ wordt beschreven creeer een schema XDM om met Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md) te gebruiken. Als deze optie is ingeschakeld en gegevens worden opgenomen in gegevenssets die op dit schema zijn gebaseerd, worden die gegevens samengevoegd in het realtime profiel van de klant.

   * Als u het stromen media gegevens wilt omvatten, moet u [ uw schema vormen om het stromen gegevens ](/help/data-ingestion/streaming.md) in te voeren en te gebruiken.

1. [ creeer een dataset in Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-dataset.md).

1. (Optioneel) Als u classificatiegegevens gebruikt in Adobe Analytics, kunt u classificatiegegevens toevoegen aan uw gegevensset in Customer Journey Analytics.

   Om dit te doen, [ creeer een raadplegingsdataset voor elke dimensie die classificatiegegevens ](/help/getting-started/cja-upgrade/cja-upgrade-dataset-lookup.md) bevat.

1. Voor de implementaties van Adobe Analytics die AppMeasurement of de uitbreiding van Analytics (markeringen) gebruiken, [ creeer een gegevensstroom in Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-datastream.md) <!-- Is this correct? Will customers on the Web SDK already have a datastream that they only need to add AEP as a service to? Or does this step apply to everyone?-->.

   Voor Adobe Analytics-implementaties die gebruikmaken van de Web SDK, bestaat al een gegevensstroom. Voor meer informatie, zie [ uw bestaande implementatie van SDK van het Web van Adobe Analytics vormen om gegevens naar Platform ](/help/getting-started/cja-upgrade/cja-upgrade-existing-adobe-analytics-websdk.md) te verzenden.

1. [ voeg Adobe Experience Platform als dienst aan uw datastream ](/help/getting-started/cja-upgrade/cja-upgrade-datastream-addplatform.md) toe.

1. (Optioneel) Als u Customer Journey Analytics wilt integreren met Adobe Journey Optimizer, gebruikt u het aanpassingsobject in uw implementatie voor gebruik in Adobe Journey Optimizer.

1. Vouw de sectie uit waarin wordt beschreven hoe u Experience Platform Web SDK voor uw Customer Journey Analytics-implementatie wilt implementeren en voer vervolgens de bijbehorende stappen uit:

   +++Handmatige implementatie (JS-bestand)

   1. [ voegt alloy.js aan uw plaats ](https://experienceleague.adobe.com/en/docs/experience-platform/edge/fundamentals/installing-the-sdk#option-2-installing-the-prebuilt-standalone-version%22) toe.

   1. Vul een XDM-object en verzend het naar de gegevensstroom.

+++

   +++Tags

   1. [ creeer een markeringsbezit en voeg de uitbreiding van SDK van het Web van Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-tag-property.md) toe.

   1. [De extensie Adobe Experience Platform Web SDK toevoegen aan de eigenschap tag](/help/getting-started/cja-upgrade/cja-upgrade-tag-extension.md)

   1. [ voert de ladersmarkering op uw plaats ](/help/getting-started/cja-upgrade/cja-upgrade-tag-loader.md) uit.

   1. [ voeg de logica van de gegevensinzameling XDM aan uw markering ](/help/getting-started/cja-upgrade/cja-upgrade-tag-xdm.md) toe.

+++

+++ API

   1. Gebruik de Edge Network API om gegevens naar de gewenste gegevensstroom te verzenden.

+++

1. [ bevestigt dat uw implementatie van SDK van het Web gegevens naar een dataset ](/help/getting-started/cja-upgrade/cja-upgrade-dataset-ingestion.md) verzendt.

1. [ creeer een verbinding in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-connection.md).

1. (Optioneel) Til webgegevens met gegevens uit andere kanalen, zoals gegevens van het callcenter.

   U verwezenlijkt dit door extra datasets aan uw verbinding van Customer Journey Analytics toe te voegen, zoals die in [ wordt beschreven de vraagcentrum van de Invoer en Webgegevens ](/help/use-cases/cross-channel/call-center.md).

1. [ creeer een gegevensmening in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md).

1. [ bevestigt dat het gegeven in de gegevensmening in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-validate.md) stroomt.

1. [ Migreer projecten en componenten ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration).

   <!-- You might not want to do this, based on the schema? Ask Zach. Will it work if you have all new schema fields? What would you want to just build from scratch. Maybe everything? -->

1. (Facultatief) als u marketing kanalen in Adobe Analytics gebruikt, kunt u [ tot een marketing kanaal afgeleid gebied in Customer Journey Analytics ](/help/data-views/derived-fields/derived-fields.md#marketing-channels) leiden.

   Afgeleide velden zijn een belangrijk aspect van real-time rapportage in Customer Journey Analytics. Een afgeleid gebied staat u toe om (vaak complexe) gegevensmanipulaties op de vlucht, door een klantgerichte regelbouwer te bepalen.

   Eén toepassing voor afgeleide velden is het definiëren van een afgeleid veld Marketing Channel dat het juiste marketingkanaal bepaalt op basis van een of meer voorwaarden (bijvoorbeeld URL-parameter, pagina-URL of paginanaam).

   Gebruik [ het marketing kanaalfunctiesjabloon ](/help/data-views/derived-fields/derived-fields.md#marketing-channels) op afgeleide gebieden om snel een afgeleid gebied voor marketing kanalen tot stand te brengen.

1. Vergelijk gegevens in Adobe Analytics van uw oude implementatie met gegevens in Customer Journey Analytics van uw nieuwe implementatie en zorg ervoor dat u alle verschillen begrijpt en waarom deze bestaan. <!-- Expound on this. Link to somewhere? There will be a lot of differences. -->

1. Breng historische gegevens van Adobe Analytics met behulp van de Analytics-bronconnector:

   >[!NOTE]
   >
   >Gebruik de volgende stappen als u nog geen bronconnector voor Analytics hebt gemaakt.
   >
   >Als u reeds de Analytics bronschakelaar met Customer Journey Analytics gebruikt, volg de stappen in [ Overgang van de Analytics bronschakelaar aan het Web SDK voor Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-from-source-connector.md).

   1. [Maak een XDM-schema voor de bronconnector van Analytics](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-schema.md)

   1. Als u reeds geen Analytics bronschakelaar hebt, [ creeer de Analytics bronschakelaar en kaartgebieden aan uw XDM schema ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector.md).

      of

      Als u reeds een Analytics bronschakelaar hebt, [ kaartgebieden van de bronschakelaar aan uw schema XDM ](/help/getting-started/cja-upgrade/cja-upgrade-from-source-connector.md).

   1. [ voeg de gegevensset van de bron van Analytics aan de verbinding ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-dataset.md) toe.

1. De gebruiker aan boord gaan.

   Net als in Adobe Analytics is Analysis Workspace het belangrijkste gebruikersgerichte hulpmiddel in Customer Journey Analytics. Er zijn echter enkele belangrijke verschillen bij het gebruik van Analysis Workspace in Customer Journey Analytics die gebruikers moeten onthouden.

   Geef uw gebruikers voldoende tijd (3 tot 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Analysis Workspace in Customer Journey Analytics.

   Voor informatie over enkele zeer belangrijke verschillen tussen Adobe Analytics en Customer Journey Analytics, zie [ Gids van de Gebruiker voor de gebruikers van Adobe Analytics ](/help/getting-started/aa-to-cja-user.md).

1. Leer over [ eigenschapsteun in Customer Journey Analytics ](/help/getting-started/aa-vs-cja/cja-aa.md). De meeste Adobe Analytics-functies worden ondersteund in Customer Journey Analytics en er zijn veel extra functies beschikbaar in Customer Journey Analytics.

1. Schakel Adobe Analytics uit wanneer de Customer Journey Analytics Web SDK-implementatie is voltooid en u vertrouwd bent met de gegevens die u verzamelt.

   Adobe raadt u aan uw Adobe Analytics-omgeving na de implementatie van Customer Journey Analytics gedurende een bepaalde periode in bedrijf te houden.

   Voor meer informatie over het gebruik van Adobe Analytics tijdens en na een verbetering, evenals de voorgestelde timing van het onbruikbaar maken van Adobe Analytics, zie [ evalueren hoe lang u Adobe Analytics na bevordering aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-fully-move.md) nodig hebt.

## Upgrade-stappen voor uw organisatie dynamisch genereren

Afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, begrijpen de geadviseerde verbeteringsstappen die in [ worden beschreven de geadviseerde verbeteringsstappen ](#1-understand-the-recommended-upgrade-steps) niet praktisch voor uw organisatie zou kunnen zijn.

Om verbeteringsstappen voor de unieke omstandigheden van uw organisatie dynamisch te produceren:

1. Voltooi de Customer Journey Analytics Upgrade Guide.

   Als u vanuit Customer Journey Analytics toegang wilt tot de hulplijn, selecteert u de tab **[!UICONTROL Workspace]** en vervolgens **[!UICONTROL Upgrade to Customer Journey Analytics]** in het linkerdeelvenster. Volg de aanwijzingen op het scherm.

   Nadat u deze upgradehandleiding hebt voltooid, ontvangt u stapsgewijze instructies waarin de optimale upgradestappen worden beschreven die uniek zijn voor uw organisatie-vereisten. Dit zijn de upgradestappen die het beste aansluiten op uw bestaande Adobe Analytics-omgeving en uw doelen voor Customer Journey Analytics.

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
