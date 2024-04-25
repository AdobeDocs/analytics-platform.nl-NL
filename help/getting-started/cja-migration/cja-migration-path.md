---
title: Het migratiepad voor Customers Journey Analytics kiezen
description: Leer de voor- en nadelen van de mogelijke migratiepaden bij het migreren naar de Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 9559ba10-cbaf-4243-9c85-a0a5f6e3bbff
source-git-commit: 5a0c383104fa4df79bc3c24d4af3677d255612f6
workflow-type: tm+mt
source-wordcount: '2641'
ht-degree: 0%

---

# Stap 2: kies uw migratiepad

+++ breid deze sectie uit om te zien waar de informatie op deze pagina in het grotere migratieproces past. Controleer of alle vorige migratiestappen zijn voltooid.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige migratietaken hebt uitgevoerd.

De informatie op deze pagina behandelt Stap 2 van de migratie, zoals benadrukt in de hieronder lijst:

| Migratietaak | Details |
|---------|----------|
| **Stap 1: [Aan de slag met de migratie](/help/getting-started/cja-migration/cja-migration-getstarted.md)** | Leer de voordelen van migratie naar Adobe Analytics en het basismigratieproces. |
| <span class="preview">**Stap 2: kies het migratiepad**</span> | <span class="preview">Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen.</span> |
| **Stap 3: [Gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van het migratiepad dat u hebt gekozen in Stap 2. |
| **Stap 4: [Historische gegevens behouden](/help/getting-started/cja-migration/cja-migration-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 5: [Extra implementatietaken uitvoeren](/help/getting-started/cja-getting-started.md)** | Op dit punt in het migratieproces, moet u diverse taken uitvoeren alvorens uw milieu van de Customer Journey Analytics klaar aan gebruik is.<p>Deze extra taken gelden voor migraties uit Adobe Analytics en voor nieuwe implementaties van Customers Journey Analytics.</p><p>Deze taken omvatten:</p><ul><li>Andere gegevens in Experience Platform plaatsen</li><li>Verbindingen maken tussen de gegevenssets van het Platform en Customer Journey Analytics</li><li>Gegevensweergaven maken</li><li>Het gebruik van de API voor rapportage porteren</li><li>Verantwoording van gegevensfeeds en -Data Warehouse</li><li>Projecten en onderdelen migreren</li><li>Gebruiker aan boord plannen</li></ul> <p>Zie voor meer informatie [Aan de slag met Customer Journey Analytics](/help/getting-started/cja-getting-started.md). |

{style="table-layout:auto"}

+++

Nadat u besluit om aan Customer Journey Analytics te migreren, moet u de optimale migratieweg voor uw organisatie bepalen.

Het pad dat u kiest voor migreren van Adobe Analytics naar Customer Journey Analytics, is afhankelijk van de volgende factoren:

* Uw bestaande Adobe Analytics-implementatie

* Uw doelstellingen voor de toekomst

Gebruik de informatie op deze pagina om te bepalen welke weg van de de migratiemigratie van de Customer Journey Analytics het best richt op de huidige implementatie van uw organisatie en toekomstige doelstellingen.

Om het optimale migratiepad voor uw organisatie te bepalen, moeten de volgende secties opeenvolgend worden gelezen:

1. Eerste, [de beschikbare migratiepaden begrijpen](#understand-migration-methods).

1. Dan, [beoordelen welke migratiepaden voor u beschikbaar zijn](#assess-the-migration-methods-available-to-you-based-on-your-current-adobe-analytics-implementation).

1. En ten slotte, [wegen de voor- en nadelen van elk migratiepad](#weigh-the-advantages-and-disadvantages-of-the-migration-methods-available-to-you).

## Migratiepaden begrijpen

Er zijn verschillende migratiepaden voor migreren van Adobe Analytics naar Customer Journey Analytics.

Over het algemeen verschilt elk migratiepad in het inspanningsniveau dat nodig is om de migratie uit te voeren, alsook in de levensvatbaarheid op lange termijn die wordt bereikt nadat de migratie is voltooid.

De volgende tabel geeft een overzicht van elk migratiepad, het inspanningsniveau en de levensvatbaarheid op lange termijn:

| Migratiepad | inspanningsniveau | Lange levensvatbaarheid |
|---------|----------|---------|
| **Nieuwe implementatie van het Web SDK van het Experience Platform**</br> Terwijl dit technisch geen migratie is, kunt u beginnen gebruikend Customer Journey Analytics door een nieuwe implementatie van het Web SDK van het Experience Platform te doen. Hierdoor kunt u gegevens naar Adobe Experience Platform Edge Network en Customer Journey Analytics verzenden. <p>Voor organisaties nog niet op het Web SDK, is dit migratieweg misschien het meest ongecompliceerd in het krijgen van gegevens aan Edge Network omdat het het minste aantal stappen vereist; nochtans, omdat al het werk omhoog (zoals het creëren van het schema XDM) wordt gedaan, vereist het een grotere aanvankelijke inspanning.</p><p>De basisstappen zijn:</p><ol><li>Maak een XDM-schema voor uw organisatie.</li><li>Voer SDK van het Web uit.</li><li>Gegevens verzenden naar platform.</li></ol> | Hoog | Hoog |
| **Uw Adobe Analytics-implementatie migreren voor gebruik van de Web SDK**</br> Als uw implementatie van Adobe Analytics AppMeasurement of de uitbreiding van Analytics is, kunt u het migreren om het te gebruiken Adobe Experience Platform Web SDK beginnen gegevens naar Edge Network en Adobe Analytics te verzenden, alvorens het naar Customer Journey Analytics te verzenden.<p>Voor organisaties nog niet op het Web SDK, is dit de gemakkelijkste en gemakkelijkste manier om gegevens aan Edge Network te krijgen; het vereist meer stappen, maar biedt een meer methodische overgang van Adobe Analytics aan Customer Journey Analytics, met tastbaardere mijlpalen.</p><p>De basisstappen zijn:</p><ol><li>Verplaats uw bestaande Adobe Analytics-implementatie naar de Web SDK en controleer of alles werkt in Adobe Analytics.</li><li>Creeer een schema XDM voor uw organisatie aangezien u tijd hebt.</li><li>Gebruik Datstroomtoewijzing om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema.</li><li>Gegevens verzenden naar platform.</li></ol> | Gemiddeld | Hoog |
| **De bestaande Adobe Analytics Web SDK-implementatie configureren**</br> Als uw Adobe Analytics-implementatie al gebruikmaakt van de Adobe Experience Platform Web SDK, kunt u zo weinig mogelijk gegevens naar de Customer Journey Analytics verzenden.<p>Voordat u gegevens naar de Customer Journey Analytics verzendt, kunt u overwegen het Adobe Analytics-schema bij te werken voor de specifieke behoeften van uw organisatie en andere platformtoepassingen die u gebruikt.</p><p>De basisstappen zijn:</p><ol><li>Gegevens verzenden naar Customer Journey Analytics.<!-- What's involved here? Just point it at CJA? --></li><li>(Optioneel) Maak een XDM-schema voor uw organisatie terwijl u tijd hebt.</li><li>(Voorwaardelijk) als u een XDM-schema hebt gemaakt, gebruikt u gegevenstoewijzing om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema.</li></ol> | Laag | Hoog |
| **De Bronverbinding Analytics gebruiken**</br> Als uw Adobe Analytics-implementatie AppMeasurement of de extensie Analytics is, kunt u beginnen met het verzenden van gegevens naar een gegevensweergave in Customer Journey Analytics.<p>Dit is de eenvoudigste manier om gegevens naar de Customer Journey Analytics te krijgen, maar op de lange termijn is dit de minst haalbare methode.</p> | Laag | Laag |

{style="table-layout:auto"}

Gebruik het volgende diagram om te helpen visualiseren waar elk migratiepad in termen van inspanningsniveau en levensvatbaarheid op lange termijn valt:

![cja-migratiepaden](assets/cja-migration-methods.png)

## Evalueer de migratiepaden die voor u beschikbaar zijn op basis van uw huidige Adobe Analytics-implementatie

Niet alle migratiepaden zijn beschikbaar voor elk type Adobe Analytics-implementatie.

Gebruik de onderstaande informatie om u te helpen begrijpen welke migratiepad het meest geschikt is voor uw organisatie.

Neem contact op met uw Adobe als u meer specifiek advies, advies of ondersteuning nodig hebt.

| Bestaande Adobe Analytics-implementatie | Beschikbare migratiepaden |
|---------|----------|
| AppMeasurement | <ul><li>Nieuwe implementatie van het Web SDK van het Experience Platform</li><li>Adobe Analytics migreren naar de web SDK</li><li>Bronverbinding voor analyse</li></ul> |
| Adobe Analytics-extensie | <ul><li>Nieuwe implementatie van het Web SDK van het Experience Platform</li><li>Adobe Analytics migreren naar de web SDK</li><li>Bronverbinding voor analyse</li></ul> |
| Web SDK | <ul><li>Vorm de implementatie van SDK van het Web van Adobe Analytics om gegevens naar Customer Journey Analytics te verzenden</li></ul> |

{style="table-layout:auto"}

## De voor- en nadelen van de beschikbare migratiepaden wegen

De voor- en nadelen van een bepaald migratiepad verschillen afhankelijk van uw bestaande Adobe Analytics-implementatie.

Voordat u de onderstaande informatie gebruikt om te bepalen welk migratiepad geschikt is voor u, raadpleegt u de informatie in [Migratiepaden begrijpen](#understand-migration-methods) als je dat nog niet hebt gedaan.

### Voor Adobe Analytics-implementaties met: extensie AppMeasurement en Adobe Analytics

Hieronder vindt u de migratiepaden die beschikbaar zijn voor organisaties die Adobe Analytics met AppMeasurement of de Adobe Analytics-extensie hebben geïmplementeerd. Breid elke sectie uit om de voor- en nadelen van elk migratiepad weer te geven.

**Migratiepaden:**

+++Nieuwe implementatie van het Web SDK van het Experience Platform

| Voordelen | Nadelen |
|----------|---------|
| <ul><li>**Biedt alle voordelen van het hosten van gegevens in de Edge Network van de Ervaring**: <p>Deze voordelen zijn onder meer:</p><ul><li>Zeer krachtige rapportage en beschikbaarheid van gegevens, omdat Adobe Experience Platform is gebouwd op voeding [Gebruiksgevallen voor realtime personalisatie](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)</li><li>Tags consolideren voor het verzamelen van Adobe Experience Cloud-gegevens tussen andere Experiencen Cloud (AJO, RTCDP enzovoort)</li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (voor prop, eVar, gebeurtenis, enzovoort)</li></ul></li><li>**Gebruikt een XDM-schema**: [XDM-schema&#39;s](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) Dit is een flexibel schema voor het definiëren van alle velden die u nodig hebt, en alleen die velden die relevant zijn. Door een XDM-schema te gebruiken, kunt u weg van de Adobe Analytics Experience Event-veldgroep.</li><li>**Geen tekenlimieten**: Het XDM-schema heeft geen tekenbeperkingen.</li><li>**Toekomstbestendig**: De SDK van het Web Experience Platform ontvangt alle nieuwste functies en functies.</li><li>**Betere nauwkeurigheid van bezoekersidentificatie**: De SDK van het Web Experience Platform gebruikt [Apparaat-id&#39;s van eerste partij](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/first-party-device-ids.html) voor een betere nauwkeurigheid van de identificatie van de bezoeker.</li></ul> | <ul><li>**Hiervoor is een nieuwe implementatie vereist**: De eis om een nieuwe implementatie uit te voeren betekent de volgende nadelen: </li><ul><li>**Tijdrovend**: Dit is het meest tijdrovende en veeleisende migratiepad, omdat het vereist dat u opnieuw begint met een nieuwe implementatie.</li><li>**Moet het volledige schema in XDM opnieuw creëren**: Voordat u kunt beginnen met het implementeren van de Web SDK, moet u het volledige schema opnieuw maken in XDM.</li><li>**Regels en gegevenselementen opnieuw maken**: Voordat u kunt beginnen met het implementeren van de SDK van het Web, moet u alle regelvoorwaarden en gegevenselementen van uw Adobe Analytics-implementatie opnieuw maken.</li></ul></ul> |

{style="table-layout:auto"}

+++

+++ Adobe Analytics migreren naar de SDK van het Web Experience Platform

| Voordelen | Nadelen |
|----------|---------|
| <ul><li>**Biedt alle voordelen van het hosten van gegevens in de Edge Network van de Ervaring**: <p>Deze voordelen zijn onder meer:</p><ul><li>Zeer krachtige rapportage en beschikbaarheid van gegevens, omdat Adobe Experience Platform is gebouwd op voeding [Gebruiksgevallen voor realtime personalisatie](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)</li><li>Tags consolideren voor het verzamelen van Adobe Experience Cloud-gegevens tussen andere Experiencen Cloud (AJO, RTCDP enzovoort)</li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (voor prop, eVar, gebeurtenis, enzovoort)</li></ul><li>**Gebruikt uw bestaande implementatie**: Hoewel deze aanpak enige wijzigingen in de implementatie vereist, is er geen volledig nieuwe implementatie nodig. U kunt de bestaande gegevenslaag en -code gebruiken met minimale wijzigingen in de implementatielogica zonder dat dit van invloed is op uw bestaande Adobe Analytics-rapportage.</li><li>**Biedt flexibiliteit om een XDM-schema voor uw organisatie op een later tijdstip te maken**: U kunt uw bestaande Adobe Analytics-implementatie migreren om de SDK van het Web te gebruiken en te valideren dat alles in Adobe Analytics werkt, en vervolgens het XDM-schema maken. Deze flexibiliteit maakt een meer methodische en doordachte migratie mogelijk.</li><li>**Gebruikt een XDM-schema**: [XDM-schema&#39;s](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) Dit is een flexibel schema voor het definiëren van alle velden die u nodig hebt, en alleen die velden die relevant zijn. Door een XDM-schema te gebruiken, kunt u weg van de Adobe Analytics Experience Event-veldgroep.</li><li>(bij migratie uit de Adobe Analytics-tagextensie) **Behoudt regels en gegevenselementen**: Terwijl er nieuwe regelhandelingen nodig zijn, kunt u de bestaande gegevenselementen en regelvoorwaarden opnieuw gebruiken met minimale wijzigingen.</li><li>**Geen tekenlimieten**: Het XDM-schema heeft geen tekenbeperkingen.</li><li>**Toekomstbestendig**: De SDK van het Web Experience Platform ontvangt alle nieuwste functies en functies.</li><li>**Betere nauwkeurigheid van bezoekersidentificatie**: De SDK van het Web Experience Platform gebruikt [Apparaat-id&#39;s van eerste partij](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/first-party-device-ids.html) voor een betere nauwkeurigheid van de identificatie van de bezoeker.</li></ul> | <ul><li>**Vereist toewijzing om gegevens naar Platform te verzenden**: Wanneer uw organisatie klaar is om Customer Journey Analytics te gebruiken, moet u gegevens naar een gegevensset in Adobe Experience Platform verzenden. Deze actie vereist dat elk gebied in het gegevensvoorwerp een ingang in het hulpmiddel van de gegevenstoewijzing is dat het aan een XDM schemagebied toewijst. Voor deze workflow hoeft u slechts één keer toewijzingen uit te voeren, en dit betekent niet dat u implementatiewijzigingen aanbrengt. Het is echter een extra stap die niet vereist is bij het verzenden van gegevens in een XDM-object.</li><li>**Technische schuld**: Omdat deze benadering een gewijzigde vorm van uw bestaande implementatie gebruikt, kan het moeilijker zijn om implementatielogica te volgen en veranderingen in de toekomst uit te voeren wanneer nodig. </li><li>(Alleen bij migreren uit AppMeasurement) **Implementatiewijzigingen vereisen ingrijpen van de ontwikkelaar**: Als u veranderingen in uw implementatie van SDK van het Web wilt aanbrengen, moet u met uw ontwikkelingsteam werken om de code op uw plaats uit te geven. Dit is niet van toepassing wanneer het migreren aan het Web SDK van de de markeringsuitbreiding van de Analyse.</li></ul> |

{style="table-layout:auto"}

+++

+++Gebruik de Bronverbinding Analytics

| Voordelen | Nadelen |
|----------|---------|
| <ul><li>Minder tijdrovende en veeleisende migratieweg. <p>Gegevens worden snel naar Customer Journey Analytics gemigreerd met minimale investeringen</p></li></ul> | <ul><li>**Gegevens worden niet naar de Edge Network verzonden**: <p>Dit leidt tot de volgende nadelen:</p><ul><li>Hoogste niveau van [latentie](/help/admin/guardrails.md#latencies) in rapportage over alle migratiepaden; niet geoptimaliseerd voor realtime gebruik van personalisatie.</li><li>Gegevens kunnen niet worden gedeeld met andere Adobe Experience Platform-toepassingen; ze zijn beperkt tot alleen Customers Journey Analytics</li><li>Reliant op de nomenclatuur van Adobe Analytics (prop, eVar, gebeurtenis, enzovoort)</li></ul><li>**Moeilijk om naar SDK van het Web in de toekomst te bewegen**: </li><li>**Gebruikt de het gebiedsgroep van de Gebeurtenis van de Ervaring van Analytics in uw schema**: Deze veldgroep voegt veel Adobe Analytics-gebeurtenissen toe die niet nodig zijn in uw Customer Journey Analytics-schema.  Dit kan leiden tot een overzichtelijker, complex schema dan wat anders voor Customer Journey Analytics nodig is.</li></ul> |

{style="table-layout:auto"}

+++

### Voor Adobe Analytics-implementaties met: Web SDK

Het volgende migratiepad is beschikbaar voor organisaties die Adobe Analytics met het Web SDK van het Experience Platform hebben geïmplementeerd:

**Migratiepad:**

+++Configureer de Adobe Analytics Web SDK-implementatie om gegevens naar de Customer Journey Analytics te verzenden

| Voordelen | Nadelen |
|----------|---------|
| Dit is het voorkeursmigratiepad als uw Adobe Analytics-implementatie de Web SDK al gebruikt.<ul><li>**Biedt alle voordelen van het hosten van gegevens in de Edge Network van de Ervaring**: <p>Deze voordelen zijn onder meer:</p><ul><li>Zeer krachtige rapportage en beschikbaarheid van gegevens, omdat Adobe Experience Platform is gebouwd op voeding [Gebruiksgevallen voor realtime personalisatie](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)</li><li>Tags consolideren voor het verzamelen van Adobe Experience Cloud-gegevens tussen andere Experiencen Cloud (AJO, RTCDP enzovoort)</li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (voor prop, eVar, gebeurtenis, enzovoort)</li></ul><li>**Gebruikt uw bestaande implementatie**: Hoewel deze aanpak enige wijzigingen in de implementatie vereist, is er geen volledig nieuwe implementatie nodig. U kunt de bestaande gegevenslaag en -code gebruiken met minimale wijzigingen in de implementatielogica zonder dat dit van invloed is op uw bestaande Adobe Analytics-rapportage.</li><li>**Verstrekt een optie om een schema te gebruiken XDM**: U kunt ervoor kiezen om uw bestaande Adobe Analytics-schema te gebruiken of een XDM-schema- en toewijzingsvelden in het gegevensobject te maken voor uw XDM-schema. [XDM-schema&#39;s](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) Dit is een flexibel schema voor het definiëren van alle velden die u nodig hebt, en alleen die velden die relevant zijn. <p>Zie &quot;Gebruikend het schema XDM&quot;hieronder voor meer informatie over de voordelen om het schema te gebruiken XDM.</p></li><li>**Behoudt regels en gegevenselementen**: Terwijl er nieuwe regelhandelingen nodig zijn, kunt u de bestaande gegevenselementen en regelvoorwaarden opnieuw gebruiken met minimale wijzigingen.</li><li>**Geen tekenlimieten**: Er zijn geen tekengrenzen als u ervoor kiest om een XDM-schema te maken en te gebruiken.</li><li>**Toekomstbestendig**: De SDK van het Web Experience Platform ontvangt alle nieuwste functies en functies.</li><li>**Betere nauwkeurigheid van bezoekersidentificatie**: De SDK van het Web Experience Platform gebruikt [Apparaat-id&#39;s van eerste partij](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/first-party-device-ids.html) voor een betere nauwkeurigheid van de identificatie van de bezoeker.</li></ul><p>**Kies uw schema**</p><p>Wanneer u dit migratiepad gebruikt, kunt u kiezen of u uw bestaande Adobe Analytics-schema wilt gebruiken of u het XDM-schema kunt bijwerken zodat u het beter kunt afstemmen op de behoeften van uw organisatie wanneer u andere platformtoepassingen gaat gebruiken.</p><p>**Het Adobe Analytics-schema gebruiken**</p><p>De voordelen van het Adobe Analytics-schema zijn:</p><ul><li>Gemakkelijk migreren<p>Als u reeds gegevens naar Adobe Analytics met het Web SDK van Adobe Experience Platform verzendt, kunt u de extra dienst aan uw gegevensstroom toevoegen om gegevens naar Adobe Experience Platform te verzenden (die dan in uw configuratie van de Customer Journey Analytics kan worden gebruikt).</p></li></ul><p>De nadelen van het gebruik van het Adobe Analytics-schema zijn:</p><ul><li>Terwijl het gebruiken van het schema van Adobe Analytics beperkt u niet in termen van hoe het met andere toepassingen van het Platform kan worden gebruikt, resulteert het in een schema dat complexer is dan het anders zou kunnen zijn. Dit komt omdat het Adobe Analytics-schema veel objecten bevat die specifiek zijn voor Adobe Analytics en die waarschijnlijk niet door uw organisatie zullen worden gebruikt.<p>Wanneer wijzigingen in het schema vereist zijn, moet u door duizenden ongebruikte velden bladeren om het veld te zoeken dat moet worden bijgewerkt.</p></li></ul><p>**Het XDM-schema gebruiken**</p><p>De voordelen van het bijwerken van het XDM-schema zijn:</p><ul><li>Een gestroomlijnd schema dat aan de behoeften van uw organisatie en de specifieke toepassingen van het Platform wordt aangepast die u gebruikt.</li><p>Wanneer veranderingen in het schema worden vereist, moet u niet door duizenden ongebruikte gebieden bewegen om het gebied te vinden dat het bijwerken vereist.</p></ul><p>De nadelen van het bijwerken van het XDM-schema zijn:</p><ul><li>Het bijwerken van uw schema is een tijdrovend proces dat wordt vereist alvorens u begint gegevens naar Customer Journey Analytics te verzenden.</li></ul> | Geen |

{style="table-layout:auto"}

+++

## Vervolgens verzendt u gegevens naar Adobe Experience Platform

Nadat u de bovenstaande informatie hebt gebruikt om een migratiepad te kiezen, leert u hoe u [gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md) afhankelijk van het migratiepad dat u hebt gekozen.
