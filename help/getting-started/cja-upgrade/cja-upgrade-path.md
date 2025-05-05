---
title: Het Customer Journey Analytics-upgradepad kiezen
description: Leer de voor- en nadelen van de mogelijke upgradepaden bij de upgrade naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 9559ba10-cbaf-4243-9c85-a0a5f6e3bbff
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '2975'
ht-degree: 0%

---

# Stap 2: kies uw upgradepad

+++ breid deze sectie uit om te zien waar de informatie op deze pagina in het grotere verbeteringsproces past. Controleer of alle vorige upgradestappen zijn voltooid.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige upgradetaken hebt uitgevoerd.

De informatie op deze pagina behandelt Stap 2 van het verbeteringsproces, zoals benadrukt in de hieronder lijst:

| Upgradetaak | Details |
|---------|----------|
| **Stap 1: [ wordt begonnen met verbetering](/help/getting-started/cja-upgrade/cja-upgrade-getstarted.md)** | Leer de voordelen van een upgrade naar Customer Journey Analytics en het standaard upgradeproces. |
| <span class="preview">**Stap 2: Kies de verbeteringspad**</span> | <span class="preview"> de diverse methodes zijn beschikbaar voor bevordering aan Customer Journey Analytics. Kies de methode die voor uw organisatie, afhankelijk van het huidige milieu van Adobe Analytics van uw organisatie en langetermijndoelstellingen het best is.</span> |
| **Stap 3: [ verzendt gegevens naar Adobe Experience Platform](/help/getting-started/cja-upgrade/cja-upgrade-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van het upgradepad dat u hebt gekozen in Stap 2. |
| **Stap 4: [ behoud historische gegevens](/help/getting-started/cja-upgrade/cja-upgrade-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 5: [ voer extra implementatietaken uit](/help/getting-started/cja-getting-started.md)** | Op dit punt in het upgradeproces moet u verschillende taken uitvoeren voordat uw Customer Journey Analytics-omgeving gebruiksklaar is.<p>Deze extra taken zijn van toepassing op upgrades vanuit Adobe Analytics en nieuwe Customer Journey Analytics-implementaties.</p><p>Deze taken omvatten:</p><ul><li>Andere gegevens in Experience Platform plaatsen</li><li>Verbindingen maken tussen de gegevenssets van het Platform en Customer Journey Analytics</li><li>Gegevensweergaven maken</li><li>Het gebruik van de API voor rapportage porteren</li><li>Boekhouding voor gegevensfeeds en Data Warehouse</li><li>Projecten en onderdelen migreren</li><li>Gebruiker aan boord plannen</li></ul> <p>Voor meer informatie, zie [ Customer Journey Analytics Begonnen ](/help/getting-started/cja-getting-started.md) worden. |

{style="table-layout:auto"}

+++

>[!AVAILABILITY]
>
>De informatie op deze pagina wordt vervangen door de volgende uitgebreidere upgrade-informatie: <ul><li>**Aanbevolen verbeteringsstappen**<p>Voor gedetailleerde informatie, zie [ Geadviseerde weg wanneer bevordering van Adobe Analytics aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).</p></li><li>**Gids van de Verbetering van Customer Journey Analytics**<p>Er is een nieuwe upgradehandleiding beschikbaar waarmee op dynamische wijze upgradestappen worden gegenereerd die zijn afgestemd op uw organisatie en uw unieke omstandigheden.</p><p>Als u vanuit Customer Journey Analytics toegang wilt tot de hulplijn, selecteert u de tab **[!UICONTROL Workspace]** en vervolgens **[!UICONTROL Upgrade to Customer Journey Analytics]** in het linkerdeelvenster. Volg de aanwijzingen op het scherm.</p></li></ul>


Nadat u hebt besloten om een upgrade naar Customer Journey Analytics uit te voeren, moet u het optimale upgradepad voor uw organisatie bepalen.

Het pad dat u kiest voor de upgrade van Adobe Analytics naar Customer Journey Analytics, is afhankelijk van de volgende factoren:

* Uw bestaande Adobe Analytics-implementatie

* Uw doelstellingen voor de toekomst

Aan de hand van de informatie op deze pagina kunt u bepalen welk Customer Journey Analytics-upgradepad het beste kan worden afgestemd op de huidige implementatie en toekomstige doelstellingen van uw organisatie.

Om het optimale verbeteringspad voor uw organisatie te bepalen, zouden de volgende secties opeenvolgend moeten worden gelezen:

1. Eerst, [ begrijpt de verbeteringspaden die ](#understand-upgrade-paths) beschikbaar zijn.

1. Dan, [ beoordeelt welke verbeteringswegen aan u ](#assess-the-upgrade-paths-available-to-you-based-on-your-current-adobe-analytics-implementation) beschikbaar zijn.

1. En tenslotte, wegen [ de voordelen en de nadelen van elke verbeteringsweg ](#weigh-the-advantages-and-disadvantages-of-the-upgrade-paths-available-to-you).

## Upgrade-paden begrijpen

Er zijn verschillende upgradepaden voor de upgrade van Adobe Analytics naar Customer Journey Analytics.

Over het algemeen verschilt elk upgradepad in het inspanningsniveau dat nodig is om de upgrade uit te voeren, en in de levensvatbaarheid op lange termijn die wordt bereikt nadat de upgrade is voltooid.

De volgende lijst maakt een lijst van elk verbeteringsweg, zijn niveau van inspanning, en zijn levensvatbaarheid op lange termijn:

| Upgradepad | inspanningsniveau | Lange levensvatbaarheid |
|---------|----------|---------|
| **Nieuwe implementatie van het Web SDK van Experience Platform met de Analytics bronschakelaar**</br> u kunt beginnen Customer Journey Analytics te gebruiken door een nieuwe implementatie van het Web SDK van Experience Platform te doen. Hierdoor kunt u gegevens naar Adobe Experience Platform Edge Network en Customer Journey Analytics verzenden. Bovendien gebruikt u de bronconnector Analytics om historische gegevens naar Customer Journey Analytics te brengen.<p>Voor organisaties nog niet op het Web SDK, is dit verbeteringspad misschien het meest ongecompliceerd in het krijgen van gegevens aan Edge Network omdat het het minste aantal stappen vereist; nochtans, omdat al het werk omhoog (zoals het creëren van het XDM schema) wordt gedaan, vereist het een grotere aanvankelijke inspanning.</p><p>De basisstappen zijn:</p><ol><li>Maak een XDM-schema voor uw organisatie.</li><li>Implementeer de Web SDK.</li><li>Gegevens verzenden naar platform.</li><li>Zet de bronconnector voor Analytics op.</br> de bron van Analytics schakelaar wordt gebruikt om historische gegevens van Adobe Analytics in Customer Journey Analytics te brengen.<!-- For more information about this recommended upgrade path, see [Recommended path when upgrading from Adobe Analytics to Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).--></li></ol><p><!-- **Note:** This is the recommended upgrade path when upgrading to Customer Journey Analytics. For more information about this recommended upgrade path, see [Recommended path when upgrading from Adobe Analytics to Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md). --></p> | Hoog | Hoog |
| **Nieuwe implementatie van het Web SDK van Experience Platform**</br> u kunt beginnen Customer Journey Analytics te gebruiken door een nieuwe implementatie van het Web SDK van Experience Platform te doen. Hierdoor kunt u gegevens naar Adobe Experience Platform Edge Network en Customer Journey Analytics verzenden. <p>Voor organisaties nog niet op het Web SDK, is dit verbeteringspad misschien het meest ongecompliceerd in het krijgen van gegevens aan Edge Network omdat het het minste aantal stappen vereist; nochtans, omdat al het werk omhoog (zoals het creëren van het XDM schema) wordt gedaan, vereist het een grotere aanvankelijke inspanning.</p><p>De basisstappen zijn:</p><ol><li>Maak een XDM-schema voor uw organisatie.</li><li>Implementeer de Web SDK.</li><li>Gegevens verzenden naar platform.</li></ol> | Hoog | Hoog |
| **Migreer uw implementatie van Adobe Analytics om het Web SDK**</br> te gebruiken als uw implementatie van Adobe Analytics AppMeasurement of de uitbreiding van de Analyse is, kunt u het migreren om het te gebruiken Adobe Experience Platform Web SDK beginnen gegevens naar Edge Network en Adobe Analytics te verzenden, alvorens het naar Customer Journey Analytics te verzenden.<p>Voor organisaties die nog niet op het Web SDK staan, is dit de gemakkelijkste en meest vlotte manier om gegevens aan Edge Network te krijgen; het vereist meer stappen, maar biedt een meer methodische overgang van Adobe Analytics aan Customer Journey Analytics, met tastbaardere mijlpalen.</p><p>De basisstappen zijn:</p><ol><li>Verplaats uw bestaande Adobe Analytics-implementatie naar de Web SDK en controleer of alles werkt in Adobe Analytics.</li><li>Creeer een schema XDM voor uw organisatie aangezien u tijd hebt.</li><li>Gebruik Datstroomtoewijzing om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema.</li><li>Gegevens verzenden naar platform.</li></ol> | Gemiddeld | Hoog |
| **vorm uw bestaande implementatie van SDK van het Web van Adobe Analytics**</br> als uw implementatie van Adobe Analytics reeds SDK van het Web van Adobe Experience Platform gebruikt, kunt u beginnen gegevens naar Platform te verzenden door opstelling een gegevensstroom. Of, als u reeds gegevens naar Platform verzendt, moet u eenvoudig een verbinding tussen de datasets van het Platform en Customer Journey Analytics tot stand brengen.<p>Voordat u gegevens naar Platform verzendt voor gebruik in Customer Journey Analytics, kunt u overwegen het Adobe Analytics-schema bij te werken voor de specifieke behoeften van uw organisatie en andere platformtoepassingen die u gebruikt.</p><p>De basisstappen zijn:</p><ol><li>Gegevens verzenden naar platform.<p>Als u al gegevens naar Platform verzendt met uw Adobe Analytics-implementatie, is deze stap niet vereist. U moet eenvoudig een verbinding tussen de datasets van het Platform en Customer Journey Analytics tot stand brengen, zoals later in dit proces wordt beschreven.</p></li><li>(Optioneel) Maak een XDM-schema voor uw organisatie terwijl u tijd hebt.</li><li>(Voorwaardelijk) als u een XDM-schema hebt gemaakt, gebruikt u gegevenstoewijzing om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema.</li></ol> | Laag | Hoog |
| **Gebruik de Schakelaar van Source van de Analyse**</br> als uw implementatie van Adobe Analytics AppMeasurement of de uitbreiding van de Analyse is, kunt u beginnen gegevens naar een gegevensmening in Customer Journey Analytics te verzenden.<p>Dit is de eenvoudigste manier om gegevens naar Customer Journey Analytics te krijgen, maar op de lange termijn is dit de minst haalbare methode.</p> <p>**Nota:** Deze verbeteringspad kan onafhankelijk worden gebruikt. Voor de beste resultaten raden we u echter aan dit upgradepad te gebruiken in combinatie met een nieuwe implementatie van de Experience Platform WebSDK. <!-- For more information about this recommended upgrade path, see [Recommended path when upgrading from Adobe Analytics to Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).--> </p> | Laag | Laag |

{style="table-layout:auto"}

Gebruik het volgende diagram om te helpen visualiseren waar elk verbeteringspad op het spectrum in termen van inspanningsniveau en levensvatbaarheid op lange termijn valt:

![ cja verbeteringspaden ](assets/cja-upgrade-path-chart.png)

## Evalueer de upgradepaden die beschikbaar zijn op basis van uw huidige Adobe Analytics-implementatie

Niet zijn alle upgradepaden beschikbaar voor elk type Adobe Analytics-implementatie.

Gebruik de onderstaande informatie om u te helpen begrijpen welke upgradeweg het meest geschikt is voor uw organisatie.

Neem contact op met uw Adobe-vertegenwoordiger als u meer specifiek advies, advies of ondersteuning nodig hebt.

| Bestaande Adobe Analytics-implementatie | Beschikbare upgradepaden |
|---------|----------|
| AppMeasurement | <ul><li>Nieuwe implementatie van de Experience Platform Web SDK</li><li>Adobe Analytics migreren naar Web SDK</li><li>Analytics Source Connector</li><li>(Aanbevolen) Nieuwe implementatie van de Experience Platform Web SDK met de Analytics Source Connector</li></ul> |
| Adobe Analytics-extensie | <ul><li>Nieuwe implementatie van de Experience Platform Web SDK</li><li>Adobe Analytics migreren naar Web SDK</li><li>Analytics Source Connector</li><li>(Aanbevolen) Nieuwe implementatie van de Experience Platform Web SDK met de Analytics Source Connector</li></ul> |
| Web SDK | <ul><li>Configureer de Adobe Analytics Web SDK-implementatie om gegevens naar het platform te verzenden</li><li>(Aanbevolen) Nieuwe implementatie van de Experience Platform Web SDK met de Analytics Source Connector</li></ul> |

{style="table-layout:auto"}

## Wissel de voor- en nadelen af van de upgradepaden die voor u beschikbaar zijn

De voor- en nadelen van een bepaald upgradepad zijn afhankelijk van uw bestaande Adobe Analytics-implementatie.

Alvorens u de informatie hieronder gebruikt om te bepalen welke verbeteringspad voor u juist is, herzie de informatie in [ verbeteringspaden ](#understand-migration-methods) begrijpen als u niet reeds hebt.

>[!NOTE]
>
>Terwijl elk van de verbeteringswegen die in de volgende secties worden beschreven onafhankelijk kunnen worden gebruikt, adviseert Adobe een twee-uitgesproken verbeteringsbenadering wanneer bevordering van Adobe Analytics aan Customer Journey Analytics, ongeacht uw huidige implementatie van Adobe Analytics: **de bron van Adobe Analytics schakelaar** en a **nieuwe implementatie van Experience Platform WebSDK**.
><!-- For more information about this recommended upgrade path, see [Recommended path when upgrading from Adobe Analytics to Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md) -->

### Voor Adobe Analytics-implementaties met: AppMeasurement- en Adobe Analytics-extensie

Hieronder vindt u de upgradepaden die beschikbaar zijn voor organisaties die Adobe Analytics met AppMeasurement of de Adobe Analytics-extensie hebben geïmplementeerd. Vouw elke sectie uit om de voor- en nadelen van elk upgradepad weer te geven.

#### Paden upgraden

+++Nieuwe implementatie van de Experience Platform Web SDK

| Voordelen | Nadelen |
|----------|---------|
| <ul><li>**verstrekt alle voordelen om gegevens in Ervaring Edge Network** te ontvangen: <p>Deze voordelen zijn onder meer:</p><ul><li>Zeer krachtige rapportering en gegevensbeschikbaarheid omdat Adobe Experience Platform aan macht [ wordt gebouwd verpersoonlijkingsgebruiksgevallen in real time ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)</li><li>Consolideer implementatie voor Adobe Experience Cloud-gegevensverzameling tussen andere Experience Cloud-producten (AJO, RTCDP, enzovoort)</li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (zoals prop, eVar, event, enzovoort)</li></ul></li><li>**Toekomstbestendig**: De toekomstige implementatieupdates zijn gemakkelijker.</li></ul> | <ul><li>**vereist een nieuwe implementatie van kras**: Het vereiste om een nieuwe implementatie van kras te doen betekent de volgende nadelen: </li><ul><li>**tijdrovend**: Dit is het meest tijdrovende en veeleisende verbeteringspad omdat het vereist dat u opnieuw met een nieuwe implementatie begint.</li><li>**moet het volledige schema in XDM** opnieuw creëren: Alvorens u kunt beginnen SDK van het Web uit te voeren, moet u het volledige schema in XDM opnieuw creëren.</li><li>**moet regels en gegevenselementen** opnieuw tot stand brengen: Alvorens u kunt beginnen het Web SDK uit te voeren, moet u om het even welke regelvoorwaarden en gegevenselementen van uw implementatie van Adobe Analytics opnieuw tot stand brengen.</li></ul><li>**verklaart niet om historische gegevens te behouden:** Adobe adviseert gebruikend de Analytics bronschakelaar samen met een nieuwe implementatie van het Web SDK van Experience Platform historische gegevens na bevordering aan Customer Journey Analytics te behouden. <!-- For more information about this recommended upgrade path, see [Recommended path when upgrading from Adobe Analytics to Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md) --></li><li>**verklaart niet voor het vergelijken van gegevens van uw originele implementatie met dat van uw nieuwe implementatie:** Adobe adviseert gebruikend de Analytics bronschakelaar samen met een nieuwe implementatie van het Web SDK van Experience Platform gegevens na bevordering aan Customer Journey Analytics te vergelijken. <!-- For more information about this recommended upgrade path, see [Recommended path when upgrading from Adobe Analytics to Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md) --></li></ul> |

{style="table-layout:auto"}

+++

+++ Adobe Analytics migreren naar Experience Platform Web SDK

| Voordelen | Nadelen |
|----------|---------|
| <ul><li>**verstrekt alle voordelen om gegevens in Ervaring Edge Network** te ontvangen: <p>Deze voordelen zijn onder meer:</p><ul><li>Zeer krachtige rapportering en gegevensbeschikbaarheid omdat Adobe Experience Platform aan macht [ wordt gebouwd verpersoonlijkingsgebruiksgevallen in real time ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)</li><li>Consolideer implementatie voor Adobe Experience Cloud-gegevensverzameling tussen andere Experience Cloud-producten (AJO, RTCDP, enzovoort)</li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (zoals prop, eVar, event, enzovoort)</li></ul><li>**gebruikt uw bestaande implementatie**: Terwijl deze benadering sommige implementatieveranderingen vereist, vereist het geen volledig nieuwe implementatie van kras. U kunt de bestaande gegevenslaag en -code gebruiken met minimale wijzigingen in de implementatielogica zonder dat dit van invloed is op uw bestaande Adobe Analytics-rapportage.</li><li>**verstrekt flexibiliteit om een schema XDM voor uw organisatie in een recentere tijd** tot stand te brengen: U kunt uw bestaande implementatie van Adobe Analytics migreren om het Web SDK te gebruiken en te bevestigen dat alles in Adobe Analytics werkt, dan tot het schema XDM leiden. Dankzij deze flexibiliteit is een meer methodische en doordachte upgrade naar Customer Journey Analytics mogelijk.</li></ul> | <ul><li>**vereist afbeelding om gegevens naar Platform** te verzenden: Wanneer uw organisatie klaar is om Customer Journey Analytics te gebruiken, moet u gegevens naar een gegevensreeks in Adobe Experience Platform verzenden. Deze actie vereist dat elk gebied in het gegevensvoorwerp een ingang in het hulpmiddel van de gegevenstoewijzing is dat het aan een XDM schemagebied toewijst. Voor deze workflow hoeft u slechts één keer toewijzingen uit te voeren, en dit betekent niet dat u implementatiewijzigingen aanbrengt. Het is echter een extra stap die niet vereist is bij het verzenden van gegevens in een XDM-object.</li><li>**Technische schuld**: Omdat deze benadering een gewijzigde vorm van uw bestaande implementatie gebruikt, kan het moeilijker zijn om implementatielogica te volgen en veranderingen in de toekomst uit te voeren wanneer nodig. </li></ul> |

{style="table-layout:auto"}

+++

+++Gebruik de Analytics Source Connector

| Voordelen | Nadelen |
|----------|---------|
| <ul><li>Minder tijdrovend en veeleisend upgradepad. <p>Gegevens worden snel naar Customer Journey Analytics gemigreerd met minimale investeringen</p></li></ul> | <ul><li>**Gegevens worden niet verzonden naar Edge Network**: <p>Dit leidt tot de volgende nadelen:</p><ul><li>Het hoogste niveau van [ latentie ](/help/technotes/guardrails.md#latencies) in het melden van over alle verbeteringswegen; niet geoptimaliseerd voor verpersoonlijkingsgebruiksgevallen in real time.</li><li>Gegevens kunnen niet worden gedeeld met andere Adobe Experience Platform-toepassingen; ze zijn alleen beperkt tot Customer Journey Analytics</li><li>Reliant op de Adobe Analytics-nomenclatuur (prop, eVar, event, enzovoort)</li></ul><li>**Moeilijk om naar het Web SDK in de toekomst te bewegen**: Uiteindelijk, zult u waarschijnlijk toegang tot de voordelen willen die door het Web SDK van Experience Platform worden verstrekt. Als u de Experience Platform Web SDK wilt gaan gebruiken, moet u een nieuwe implementatie uitvoeren.</li><li>**gebruikt de het gebiedsgroep van de Gebeurtenis van de Ervaring van Analytics in uw schema**: Deze gebiedsgroep voegt vele gebeurtenissen van Adobe Analytics toe die niet nodig in uw schema van Customer Journey Analytics zijn.  Dit kan leiden tot een overzichtelijker, complex schema dan wat anders nodig is voor Customer Journey Analytics.</li></ul><p>Vanwege deze nadelen raadt Adobe u aan de bronconnector Analytics te gebruiken in combinatie met een nieuwe implementatie van Experience Platform Web SDK. <!-- For more information about this recommended upgrade path, see [Recommended path when upgrading from Adobe Analytics to Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md) --></p> |

{style="table-layout:auto"}

+++

### Voor Adobe Analytics-implementaties met: Web SDK

Het volgende upgradepad is beschikbaar voor organisaties die Adobe Analytics hebben geïmplementeerd met de Experience Platform Web SDK.

Wanneer u dit upgradepad kiest, moet u ook uw schema kiezen.

#### Upgradepad

+++Configureer de Adobe Analytics Web SDK-implementatie om gegevens naar het platform te verzenden

| Voordelen | Nadelen |
|----------|---------|
| Dit is het voorkeurspad voor upgrades als uw Adobe Analytics-implementatie al gebruikmaakt van de Web SDK.<ul><li>**verstrekt alle voordelen om gegevens in Ervaring Edge Network** te ontvangen: <p>Deze voordelen zijn onder meer:</p><ul><li>Zeer krachtige rapportering en gegevensbeschikbaarheid omdat Adobe Experience Platform aan macht [ wordt gebouwd verpersoonlijkingsgebruiksgevallen in real time ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)</li><li>Consolideer implementatie voor Adobe Experience Cloud-gegevensverzameling tussen andere Experience Cloud-producten (AJO, RTCDP, enzovoort)</li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (zoals prop, eVar, event, enzovoort)</li></ul><li>**gebruikt uw bestaande implementatie**: Terwijl deze benadering sommige implementatieveranderingen vereist, vereist het geen volledig nieuwe implementatie van kras. U kunt de bestaande gegevenslaag en -code gebruiken met minimale wijzigingen in de implementatielogica zonder dat dit van invloed is op uw bestaande Adobe Analytics-rapportage.</li><li>**verstrekt een optie om een schema XDM** te gebruiken: U kunt verkiezen om uw bestaand schema van Adobe Analytics te gebruiken of een XDM schema en kaartgebieden in het gegevensvoorwerp tot stand te brengen aan uw schema XDM. [ XDM- schema&#39;s ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) zijn een flexibel schema om het even welke gebieden te bepalen u, en slechts die gebieden nodig hebt die relevant zijn. <p>Zie &quot;Gebruikend uw eigen schema XDM&quot;hieronder voor meer informatie over de voordelen om uw eigen schema te gebruiken XDM.</p></li><li>**behoudt regels en gegevenselementen**: Terwijl het nieuwe regelacties vereist, kunt u uw bestaande gegevenselementen en regelvoorwaarden met minimale veranderingen opnieuw gebruiken.</li><li>**Toekomstbestendig**: Als u verkiest om uw eigen schema te gebruiken XDM, dan zijn de toekomstige implementatieupdates gemakkelijker.</li></ul> | Geen |

{style="table-layout:auto"}

+++

#### Kies uw schema

Als u het upgradepad hebt gekozen waarmee u de Adobe Analytics Web SDK-implementatie kunt configureren voor het verzenden van gegevens naar Platform, kunt u het schema kiezen dat u wilt gebruiken.

U kunt kiezen of u uw bestaande Adobe Analytics-schema wilt gebruiken, of u kunt een update naar uw eigen XDM-schema uitvoeren om deze beter aan te passen aan de behoeften van uw organisatie wanneer u andere platformservices gaat gebruiken.

+++Gebruik het Adobe Analytics-schema met de Adobe Analytics Web SDK-implementatie

| Voordelen | Nadelen |
|----------|---------|
| <p>De voordelen van het Adobe Analytics-schema zijn:</p><ul><li>Eenvoudig upgraden<p>Als u reeds gegevens naar Adobe Analytics met het Web SDK van Adobe Experience Platform verzendt, kunt u de extra dienst aan uw gegevensstroom toevoegen om gegevens naar Adobe Experience Platform te verzenden (die dan in uw configuratie van Customer Journey Analytics kan worden gebruikt).</p></li></ul> | <p>De nadelen van het gebruik van het Adobe Analytics-schema zijn:</p><ul><li>Terwijl het gebruiken van het schema van Adobe Analytics beperkt u niet in termen van hoe het met andere toepassingen van het Platform kan worden gebruikt, resulteert het in een schema dat complexer is dan het anders zou kunnen zijn. Dit komt omdat het Adobe Analytics-schema veel objecten bevat die specifiek zijn voor Adobe Analytics en die waarschijnlijk niet door uw organisatie zullen worden gebruikt.<p>Wanneer wijzigingen in het schema vereist zijn, moet u door duizenden ongebruikte velden bladeren om het veld te zoeken dat moet worden bijgewerkt.</p></li></ul> |

+++

+++Gebruik uw eigen XDM-schema met de Adobe Analytics Web SDK-implementatie

| Voordelen | Nadelen |
|----------|---------|
| <ul><p>De voordelen van het bijwerken aan uw eigen schema XDM omvatten:</p><ul><li>Een gestroomlijnd schema dat aan de behoeften van uw organisatie en de specifieke toepassingen van het Platform wordt aangepast die u gebruikt.</li><p>Wanneer veranderingen in het schema worden vereist, moet u niet door duizenden ongebruikte gebieden bewegen om het gebied te vinden dat het bijwerken vereist.</p></ul> | <p>De nadelen van het bijwerken aan uw eigen schema XDM omvatten:</p><ul><li>Het bijwerken van uw schema is een tijdrovend proces dat wordt vereist alvorens u begint gegevens naar Platform te verzenden.</li></ul> |

+++

## Vervolgens verzendt u gegevens naar Adobe Experience Platform

Nadat u de informatie hierboven gebruikt om een verbeteringspad te kiezen, leer hoe te [ gegevens verzenden naar Adobe Experience Platform ](/help/getting-started/cja-upgrade/cja-upgrade-send-to-platform.md) afhankelijk van de verbeteringspad die u koos.
