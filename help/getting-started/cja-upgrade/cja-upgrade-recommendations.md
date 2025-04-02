---
title: Upgrade van Adobe Analytics naar Customer Journey Analytics
description: Meer informatie over de aanbevolen stappen bij het upgraden van Adobe Analytics naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: d35f8615-66f5-4823-b0b8-433852246dd2
source-git-commit: dafd4360d12c5b8a6b9ce99799722cecbca9768c
workflow-type: tm+mt
source-wordcount: '3236'
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

   * Consolideer implementatie voor Adobe Experience Cloud-gegevensverzameling tussen andere Experience Cloud-producten (AJO, RTCDP enzovoort)

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

Afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, begrijpen de geadviseerde verbeteringsstappen die in [ worden beschreven de geadviseerde verbeteringsstappen ](#recommended-upgrade-steps-for-most-organizations) niet praktisch voor uw organisatie zou kunnen zijn. In dit geval kunt u dynamisch upgradestappen genereren voor de unieke omstandigheden van uw organisatie. Het genereren van deze stappen hangt af van het feit of u al toegang hebt tot Customer Journey Analytics.

### Voor klanten die toegang hebben tot Customer Journey Analytics

Om verbeteringsstappen voor de unieke omstandigheden van uw organisatie dynamisch te produceren:

1. Voltooi de Customer Journey Analytics Upgrade Guide.

   Selecteer in Customer Journey Analytics de tab **[!UICONTROL Workspace]** en selecteer vervolgens **[!UICONTROL Upgrade to Customer Journey Analytics]** in het linkerdeelvenster. Volg de aanwijzingen op het scherm.

   Nadat u deze upgradehandleiding hebt voltooid, ontvangt u stapsgewijze instructies waarin de optimale upgradestappen worden beschreven die uniek zijn voor uw organisatie-vereisten. Dit zijn de upgradestappen die het beste aansluiten op uw bestaande Adobe Analytics-omgeving en uw doelen voor Customer Journey Analytics. De upgradestappen zijn beschikbaar als een deelbare koppeling of als een downloadbaar CSV-bestand.

1. Volg de gegenereerde stapsgewijze instructies om te upgraden naar Customer Journey Analytics.

### Voor klanten die nog geen toegang hebben tot Customer Journey Analytics

Om verbeteringsstappen voor de unieke omstandigheden van uw organisatie dynamisch te produceren:

1. Neem contact op met uw Adobe-accountteam om de Customer Journey Analytics Upgrade Guide te voltooien.

   Uw Adobe-accountteam kan u door de upgradehandleiding leiden en u een .csv-bestand bieden met de vragen, antwoorden en dynamisch gegenereerde upgradestappen die uniek zijn voor uw organisatie.

   Voordat u contact opneemt met uw Adobe-accountteam, moet u de vragen die zijn opgenomen in de upgradehandleiding voor Customer Journey Analytics kennen en uw antwoorden bepalen. De Customer Journey Analytics Upgrade Guide bevat de volgende vragen en mogelijke antwoorden:


   | Vraag | Beschikbare antwoorden | Aanvullende informatie |
   |---------|----------|---------|
   | Selecteer de optie die uw huidige Adobe Analytics-implementatie beschrijft. Deze informatie kan van invloed zijn op alternatieve upgradeopties die beschikbaar zijn wanneer u een upgrade naar Customer Journey Analytics uitvoert. | Selecteer een optie: <ul><li>**AppMeasurement:**<br/> een implementatie van JavaScript die AppMeasurement.js op een pagina laadt, en gegevens verzendt naar Adobe gebruikend het s voorwerp (bijvoorbeeld, s.eVar1).</li><li>**uitbreiding van Adobe Analytics (markeringen):** <br/> de markeringsimplementatie van A die de Inzameling van Gegevens van Adobe Experience Platform laadt (die vroeger als Lancering wordt bekend). De extensie Adobe Analytics is geïnstalleerd op de tag.</li><li>**de uitbreiding van SDK van het Web van Experience Platform (markeringen):**<br/> de markeringsimplementatie van A die de Inzameling van de Gegevens van Adobe Experience Platform laadt (vroeger gekend als Lancering). Voor de tag is de extensie Web SDK geïnstalleerd.</li><li>**Experience Platform Web SDK (alloy.js):** een implementatie van JavaScript die de bibliotheek van SDK van het Web (alloy.js) op een pagina laadt, en gegevens naar Adobe verzendt gebruikend een nuttige lading JSON.</li><li>**Bulk API van de Invoeging van Gegevens:**<br/> een implementatie die de API van de gegevenstoevoeging of bulkgegevenstoevoeging gebruikt.</li><li>**Experience Platform Mobile SDK:**<br/> een implementatie die Adobe Experience Platform Mobile SDK gebruikt.</li><li>**AppMeasurement die een hulpmiddel van het het markeringsbeheer van de derde gebruikt:**<br/> een implementatie die een hulpmiddel van het het markeringsbeheer van de derde gebruikt.</li><li>**niet-Adobe Analytics product:**<br/> een implementatie die gegevens voor een product buiten Adobe Analytics, zoals Google Analytics verzamelt. Als u deze optie selecteert, worden verschillende opties in de upgradehandleiding uitgeschakeld die niet van toepassing zijn bij het upgraden naar Customer Journey Analytics vanuit een niet-Adobe Analytics-product. </li><li>**ik weet niet:**<br/> als u niet de persoon bent die uw implementatie beheert, kunt u deze optie tijdelijk selecteren.</li></ul><p>Selecteer indien van toepassing:<ul><li>**onze implementatie gebruikt momenteel de bron Analytics verbinding:**<br/> de bron van Analytics schakelaar staat u toe om waarde van Customer Journey Analytics gemakkelijk te krijgen, maar vereist dat u voor zowel Adobe Analytics als Customer Journey Analytics betaalt. Deze gids kan u helpen zich op een onafhankelijke implementatie van SDK van het Web bewegen.</li></ul></p> | <ul><li>[ begrijp uw implementatie van Adobe Analytics en hoe het uw verbetering aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-analytics-implementation.md#understand-your-adobe-analytics-implementation-and-how-it-affects-your-upgrade-to-customer-journey-analytics) beïnvloedt</li><li>[ Overgang van de Analytics bronschakelaar aan het Web SDK voor Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-from-source-connector.md)</li></ul> |
   | De meeste Adobe Analytics-functies zijn direct beschikbaar in Customer Journey Analytics. De volgende functies moeten echter tijdens het upgradeproces in overweging worden genomen. Selecteer de bestanden die u wilt gebruiken. | Selecteer alles wat van toepassing is:<ul><li>**Historische gegevens van Adobe Analytics:**</br> breng uw historische gegevens van de het rapportreeks van Adobe Analytics in Adobe Experience Platform en Customer Journey Analytics.</li><li>**Componenten en projecten van Adobe Analytics:**</br> Componenten van Adobe Analytics omvatten: Projecten (met hun bijbehorende vrije vormlijsten en visualisaties), segmenten, en berekende metriek.</li><li>**Bedekking van de kaart van de Activiteit en verbinding het volgen:**</br> browser van A uitbreiding die u toestaat om verbinding het volgen gegevens als bedekking op uw plaats te zien.</li><li>**gegevens van de Classificatie:**</br> Groep of categoriseer gegevens als afzonderlijke dimensies.</li><li>**de Kanalen van de Marketing:**</br> creeer regels die categoriseren hoe de klanten op uw plaats aankomen.</li><li>**Data Warehouse:**</br> de Uitvoer verwerkte gegevens van Adobe Analytics in spreadsheetformaat.</li><li>**Gegevensfeeds:**Een exacte vervanging voor gegevensfeeds is nog niet beschikbaar in Customer Journey Analytics. Nochtans, kan de gelijkaardige functionaliteit met mogelijkheden zoals volledige lijstuitvoer, de uitvoer van de dataset van het Platform, het hulpmiddelintegratie van BI, en rapporteringsAPI worden bereikt.</br></li><li>**het stromen media gegevens:**</br> toe:voegen-op aan Adobe Analytics en Customer Journey Analytics die in gegevensinzameling van media, zoals audio, video, of gestroomde inhoud specialiseert.</li></ul> | <ul><li>[ begrijp de eigenschapsteun van Adobe Analytics wanneer bevordering aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-adobe-analytics-features.md)</li></ul> |
   | De meeste nieuwe functies zijn direct beschikbaar in Customer Journey Analytics. De volgende functies moeten echter tijdens het upgradeproces in overweging worden genomen. Selecteer de bestanden die u wilt gebruiken. | Selecteer alles wat van toepassing is:<ul><li>**tijd verzamelde gegevens met gegevens uit andere bronnen (e.x. de gegevens van het contactcentrum):**</br> (Geadviseerd) de gegevens van de tijd van diverse Web, mobiele, en off-line eigenschappen om één enkele, geconsolideerde mening van klantengedrag tot stand te brengen. Dit vermogen om analysegegevens uit andere kanalen te combineren is het belangrijkste gebruiksgeval voor Customer Journey Analytics.</li><li>**Stitch klappen van andere datasets die een douaneafmeting gebruiken:**<br/> als om het even welk van uw datasets geen primair herkenningsteken (zoals identiteitskaart van Experience Cloud) deelt, kunt u nog die gegevens verbinden gebruikend een andere afmeting, zoals login gebruikersbenaming of e-mailadres.</li><li>**integreer met Adobe Journey Optimizer:**<br/> lever verbonden, contextafhankelijke, en gepersonaliseerde ervaringen aan klanten.</li><li>**integreer met Adobe Real-Time CDP:**<br/> combineer profielgegevens van veelvoudige bronnen om publiek en segmenten te produceren die op gebruikerssporen worden gebaseerd.</li><li>**integreer met Adobe Target (A4T):**<br/> Adobe adviseert het integreren met Adobe Journey Optimizer voor de gevallen van het verpersoonlijkingsgebruik. Integratie met Adobe Target is mogelijk, maar een kortetermijnoplossing.</li><li>**integreer met Adobe Audience Manager:**<br/> Adobe adviseert het integreren met Adobe in real time CDP voor op publiek-gebaseerde gebruiksgevallen. Integratie met Audience Manager is mogelijk, maar een kortetermijnoplossing.</li></ul> | [ Begrijp eigenschappen uniek aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-customer-journey-analytics-features.md) |
   | Selecteer hoe u Adobe Analytics en Customer Journey Analytics uiteindelijk wilt gebruiken: | Selecteer een optie: <ul><li>**ik ben van plan volledig naar Customer Journey Analytics van Adobe Analytics te bewegen:**<br/> (Geadviseerd) Adobe adviseert dat u volledig van Adobe Analytics aan Customer Journey Analytics overgaat. Tijdens de overgangsperiode moet u Adobe Analytics naast Customer Journey Analytics uitvoeren om gegevens naast elkaar te vergelijken. Als u op de hoogte bent van de gegevens, kunt u Adobe Analytics uitschakelen.</li><li>**ik ben van plan om beide producten van Analytics te houden:**<br/> (Niet geadviseerd) als u deze optie selecteert, omvat uw contract met Adobe zowel Adobe Analytics als Customer Journey Analytics, die voor uw organisatie in tijd duurder kunnen zijn.</li></ul> | [ evalueert wanneer om Adobe Analytics na bevordering aan Customer Journey Analytics onbruikbaar te maken ](/help/getting-started/cja-upgrade/cja-upgrade-fully-move.md) |
   | Selecteer hoe u het Customer Journey Analytics-schema wilt configureren: | Selecteer een optie: <ul><li>**ik wil een schema gebruiken dat aan mijn organisatie wordt aangepast:**</br> (Geadviseerd) Aanpassen van uw schema staat uw organisatie toe om slechts te volgen wat u nodig hebt en overheadkosten te vermijden verbonden aan rommelige en onnodige gebieden. Deze optie omvat gebiedsgroepen die door het Web SDK worden toegevoegd en gebiedsgroepen die aan uw organisatie worden aangepast.</li><li>**ik wil het standaardschema van Adobe Analytics gebruiken:**</br> (Niet geadviseerd) het schema van Adobe Analytics bevat meer dan duizend gebieden, die tot verpletterd en complex schema kunnen leiden. Uw organisatie zou gedwongen worden het concept van props en eVars te blijven volgen, een erfenisconcept dat niet in Customer Journey Analytics wordt gebruikt. Integratie met andere Adobe Experience Platform-services is moeilijker.</li></ul> | [ kies uw schema voor Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-existing.md) |
   | Selecteer de gewenste manier om Customer Journey Analytics te implementeren: | <ul><li>**Handmatige implementatie (alloy.js):**<br/> omvat de bibliotheek van SDK van het Web (alloy.js) op elke pagina uw plaats.</li><li>**Markeringen:**<br/> (Geadviseerd) als u nog geen Markeringen gebruikt, installeer de markeringslader op uw plaats. Als u al tags gebruikt, kunt u de extensie Web SDK toevoegen aan de eigenschap tag. Deze optie omvat implementaties die tags gebruiken in Adobe Experience Platform Data Collection en systemen voor tagbeheer van derden.</li><li>**API:**<br/> gebruik de gegevensinzameling API om gegevens rechtstreeks naar een gegevensstroom te verzenden. Zowel niet-geverifieerde (client-naar-server) als geverifieerde (server-naar-server) typen worden ondersteund.</li></ul> | [ begrijp de implementatieopties van SDK van het Web wanneer bevordering aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-websdk-implementation.md) |
   | (Optioneel) Selecteer een andere upgrademethode | <ul><li>**Soley gebruik de Analytics bronschakelaar:**<br/> (Niet geadviseerd) u kunt de Analytics bronschakelaar als enige implementatieweg voor Customer Journey Analytics gebruiken.<p>Met deze optie bespaart u tijd bij de implementatie door snel gegevens naar Customer Journey Analytics te verzenden. Er zijn echter diverse tekortkomingen, zoals een hogere latentie en het feit dat Adobe Analytics zich in de toekomst moeilijk van kan ontdoen.</p></li><li>**ik wil mijn logica van AppMeasurement met het Web SDK gebruiken:**<br/> In plaats van het verzenden van gegevens door een voorwerp XDM, verzend al uw variabelen in het formaat van AppMeasurement door het gegevensvoorwerp.<p>Met deze optie bespaart u de implementatietijd doordat u uw AppMeasurement-logica kunt toewijzen aan XDM in plaats van een XDM-object helemaal zelf te vullen. Het leidt echter in de loop der tijd tot extra complexiteit omdat elk veld dat u in de toekomst toevoegt, in de gegevensstroom aan XDM moet worden toegewezen.</p></li><li>**ik wil mijn gegevenslaag naar Adobe zonder extra configuratie verzenden:**<br/> In plaats van het verzenden van gegevens door een voorwerp XDM, kunt u uw volledige gegevenslaag naar Adobe door het gegevensvoorwerp verzenden.<p>Deze optie bespaart implementatietijd door u toe te staan om uw gegevenslaag aan XDM in kaart te brengen, eerder dan het bevolken van een voorwerp XDM van kras. Deze toewijzing is echter een grote hoeveelheid werk omdat er een grote hoeveelheid gegevens zal zijn die Adobe niet gemakkelijk kan interpreteren. Deze optie voegt in de loop der tijd ook extra complexiteit toe, omdat elk veld dat u later in de toekomst aan uw gegevens toevoegt, in de gegevensstroom aan XDM moet worden toegewezen.</p></li></ul> | <ul><li>[ alternatief van de Verbetering: Gebruik de bron van Analytics schakelaar exclusief om aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-alternative-source-connector.md) te bevorderen</li><li>[ alternatief van de Verbetering: De gegevensinzameling van AppMeasurement van het gebruik met het Web SDK van Experience Platform en Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-alternative-appmeasurement.md)</li><li>[ alternatief van de Verbetering: verzend uw gegevenslaag aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-alternative-data-layer.md)</li></ul> |

   Nadat u deze upgradehandleiding met uw Adobe-accountteam hebt voltooid, ontvangt u een .csv-bestand met de vragen, antwoorden en dynamisch gegenereerde upgradestappen die het beste aansluiten op uw bestaande Adobe Analytics-omgeving en uw doelstellingen voor Customer Journey Analytics.

1. Volg de gegenereerde stapsgewijze instructies in het CSV-bestand om te upgraden naar Customer Journey Analytics.

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
