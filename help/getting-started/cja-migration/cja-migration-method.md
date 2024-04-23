---
title: Kies een migratiemethode voor Customers Journey Analytics
description: Ontdek de voor- en nadelen van de mogelijke migratiemethoden bij het migreren naar de Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 9559ba10-cbaf-4243-9c85-a0a5f6e3bbff
source-git-commit: 3e362a62d2ffd6d15e3028706e3704264df80222
workflow-type: tm+mt
source-wordcount: '2026'
ht-degree: 0%

---

# Stap 2: Kies uw migratiemethode voor Customers Journey Analytics

+++ breid deze sectie uit om te zien waar de informatie op deze pagina in het grotere migratieproces past. Controleer of alle vorige migratiestappen zijn voltooid.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige migratietaken hebt uitgevoerd.

De informatie op deze pagina heeft betrekking op Stap 2, zoals aangegeven in de onderstaande tabel:

| Migratietaak | Details |
|---------|----------|
| **Stap 1: [Aan de slag met de migratie](/help/getting-started/cja-migration/cja-migration-getstarted.md)** | Leer de voordelen van migratie naar Adobe Analytics en het basismigratieproces. |
| <span class="preview">**Stap 2: [Kies de migratiemethode](/help/getting-started/cja-migration/cja-migration-method.md)**</span> | <span class="preview">Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen.</span> |
| **Stap 3: [Gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van de migratiemethode die u hebt gekozen in Stap 1. |
| **Stap 4: [Gegevens toewijzen aan het XDM-schema](/help/getting-started/cja-migration/cja-migration-xdm.md)** | [XDM-schema&#39;s](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) in Adobe Experience Platform worden gebruikt om de gegevensstructuur op een consistente en herbruikbare manier te beschrijven. Door gegevens consistent in verschillende systemen te definiëren, wordt het eenvoudiger om betekenis te behouden en zo waarde te verkrijgen van gegevens.<p>De meeste migratiemethodes vereisen dat u of een nieuw schema XDM creeert, of uw bestaand schema van Adobe Analytics aan XDM in kaart brengt door datastream afbeelding te gebruiken.</p> |
| **Stap 5: [Historische gegevens behouden](/help/getting-started/cja-migration/cja-migration-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 6: [Gebruiker aan boord plannen](/help/getting-started/cja-migration/cja-migration-onboarding.md)** | Geef uw gebruikers voldoende tijd (3 - 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Customer Journey Analytics van Analysis Workspace. |
| **Stap 7: [Poort voor het gebruik van de rapportage-API](/help/getting-started/cja-migration/cja-migration-api.md)** | De Customer Journey Analytics die API rapporteert, heeft dezelfde indeling, maar gebruikt een ander eindpunt. Geef het API-gebruik voor rapportage door van de Adobe Analytics-API voor rapportage naar de Customer Journey Analytics-API. |
| **Stap 8: [Gegevensfeeds en -Data Warehouse vervangen](/help/getting-started/cja-migration/cja-migration-export-options.md)** | Bepaal hoe u de exportopties in de Customer Journey Analytics wilt gebruiken om de functies Gegevensfeeds en Data Warehouse te vervangen die u in Adobe Analytics gebruikte. |
| **Stap 9: [Projecten en onderdelen migreren](/help/getting-started/cja-migration/cja-migration-projects.md)** | In het gebied voor componentmigratie in Adobe Analytics kunt u projecten en de bijbehorende onderdelen migreren van Adobe Analytics naar Customer Journey Analytics. |

{style="table-layout:auto"}

+++

Nadat u besluit om aan Customer Journey Analytics te migreren, moet u de optimale migratiemethode voor uw organisatie bepalen.

De methode die u kiest voor het migreren van Adobe Analytics naar Customer Journey Analytics, is afhankelijk van de volgende factoren:

* Uw bestaande Adobe Analytics-implementatie

* Uw doelstellingen voor de toekomst

Gebruik de informatie op deze pagina om te bepalen welke de migratiemethode van de Customer Journey Analytics het best richt op de huidige implementatie van uw organisatie en toekomstige doelstellingen.

De volgende secties moeten opeenvolgend worden gelezen om de optimale migratiemethode voor uw organisatie te bepalen:

1. Eerste, [de beschikbare migratiemethoden begrijpen](#understand-migration-methods).

1. Dan, [beoordelen welke migratiemethoden u kunt gebruiken](#assess-the-migration-methods-available-to-you-based-on-your-current-adobe-analytics-implementation).

1. En ten slotte, [wegen de voor- en nadelen van elke migratiemethode](#weigh-the-advantages-and-disadvantages-of-the-migration-methods-available-to-you).

## Migratiemethoden begrijpen

Er bestaan verschillende migratiemethoden voor de migratie van Adobe Analytics naar Customer Journey Analytics.

In het algemeen verschilt elke migratiemethode in het inspanningsniveau dat nodig is om de migratie uit te voeren, en in de levensvatbaarheid op lange termijn die wordt bereikt nadat de migratie is voltooid.

De volgende tabel geeft een overzicht van elke migratiemethode, het inspanningsniveau en de levensvatbaarheid op lange termijn:

| Migratiemethode | inspanningsniveau | Lange levensvatbaarheid |
|---------|----------|---------|
| **Nieuwe implementatie van de Web SDK**</br> U kunt een nieuwe Adobe Experience Platform Web SDK-implementatie uitvoeren om gegevens naar de Adobe Experience Platform-Edge Network te verzenden <!-- what is the correct branding -->. <p>Voor organisaties nog niet op het Web SDK, is deze migratiemethode misschien het meest ongecompliceerd in het krijgen van gegevens aan Edge Network (die het minste aantal stappen vereist); nochtans, omdat al het werk vóór (zoals het creëren van het schema XDM) wordt gedaan, vereist het meer een grotere aanvankelijke inspanning.</p><p>De basisstappen zijn:</p><ol><li>Maak een XDM-schema voor uw organisatie.</li><li>Voer SDK van het Web uit.</li><li>Gegevens verzenden naar platform.</li></ol> | Hoog | Hoog |
| **Uw Adobe Analytics-implementatie migreren voor gebruik van de Web SDK**</br> Als uw implementatie van Adobe Analytics AppMeasurement of de uitbreiding van Analytics is, kunt u het migreren om het te gebruiken Adobe Experience Platform Web SDK beginnen gegevens naar Edge Network te verzenden alvorens het naar Customer Journey Analytics te verzenden. <!-- what else? --><p>Dit is de eenvoudigste en meest vloeiende manier om gegevens naar de Edge Network te krijgen; het vereist meer stappen, maar biedt een meer methodische overgang met tastbaardere mijlpalen.</p><p>De basisstappen zijn:</p><ol><li>Verplaats uw bestaande Adobe Analytics-implementatie naar de Web SDK en bevestig dat alles daar werkt.</li><li>Creeer een schema XDM voor uw organisatie aangezien u tijd hebt.</li><li>Gebruik gegevenstoewijzing om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema.</li><li>Gegevens verzenden naar platform.</li></ol> | Gemiddeld | Hoog |
| **Configureer uw bestaande Adobe Analytics Web SDK-implementatie om gegevens naar de Customer Journey Analytics te verzenden**</br> Als uw Adobe Analytics-implementatie al gebruikmaakt van de Web SDK, kunt u zo weinig mogelijk gegevens naar de Customer Journey Analytics verzenden.<p>Voordat u gegevens naar de Customer Journey Analytics verzendt, kunt u overwegen het Adobe Analytics-schema bij te werken voor de specifieke behoeften van uw organisatie en andere platformtoepassingen die u wilt gebruiken.</p><p>De basisstappen zijn:</p><ol><li>Gegevens verzenden naar Customer Journey Analytics.<!-- What's involved here? Just point it at CJA? --></li><li>(Optioneel) Maak een XDM-schema voor uw organisatie terwijl u tijd hebt.</li><li>(Voorwaardelijk) Als u een XDM-schema hebt gemaakt, gebruikt u gegevensstroomtoewijzing om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema.</li></ol> | Laag | Hoog |
| **Bronverbinding voor analyse**</br> Als uw Adobe Analytics-implementatie AppMeasurement of de extensie Analytics is, kunt u beginnen met het verzenden van gegevens naar een gegevensweergave in Customer Journey Analytics.<p>Dit is de eenvoudigste manier om gegevens naar de Customer Journey Analytics te krijgen, maar op de lange termijn is dit de minst haalbare methode.</p> | Laag | Laag |

{style="table-layout:auto"}

Gebruik het volgende diagram om te helpen visualiseren waar elke migratiemethode op het spectrum valt in termen van inspanningsniveau en levensvatbaarheid op lange termijn:

![cja-migratiemethoden](assets/cja-migration-methods.png)

## Evalueer de migratiemethoden waarover u beschikt op basis van uw huidige Adobe Analytics-implementatie

Niet alle migratiemethoden zijn beschikbaar voor elk type Adobe Analytics-implementatie.

Gebruik de onderstaande informatie om u te helpen begrijpen welke migratiemethode het meest geschikt is voor uw organisatie.

Neem contact op met uw Adobe als u meer specifiek advies, advies of ondersteuning nodig hebt.

| Adobe Analytics-implementatie | Beschikbare migratiemethoden |
|---------|----------|
| AppMeasurement | <ul><li>Nieuwe implementatie van de Web SDK</li><li>Adobe Analytics migreren naar de web SDK</li><li>Bronverbinding voor analyse</li></ul> |
| Adobe Analytics-extensie | <ul><li>Nieuwe implementatie van de Web SDK</li><li>Adobe Analytics migreren naar de web SDK</li><li>Bronverbinding voor analyse</li></ul> |
| Web SDK | <ul><li>Vorm de implementatie van SDK van het Web van Adobe Analytics om gegevens naar Customer Journey Analytics te verzenden</li></ul> |

{style="table-layout:auto"}

## De voor- en nadelen van de beschikbare migratiemethoden afwegen

De voor- en nadelen van een bepaalde migratiemethode verschillen afhankelijk van uw bestaande Adobe Analytics-implementatie.

Voordat u de onderstaande informatie gebruikt om te bepalen welke migratiemethode geschikt is voor u, raadpleegt u de informatie in [Migratiemethoden begrijpen](#understand-migration-methods) als je dat nog niet hebt gedaan.

### Voor Adobe Analytics-implementaties met: extensie AppMeasurement en Adobe Analytics

In de volgende tabel worden de migratiemethoden weergegeven die beschikbaar zijn voor organisaties die Adobe Analytics met AppMeasurement of de Adobe Analytics-extensie hebben geïmplementeerd:

| Migratiemethode | Voordelen | Nadelen |
|---------|----------|---------|
| **Nieuwe implementatie van de Web SDK** | <ul><li>Gebruikt een XDM-schema, een flexibel schema om de velden te definiëren die u nodig hebt, en alleen die velden die relevant zijn (zodat u zich kunt verplaatsen van de Adobe Analytics Experience Event-veldgroep)</li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (voor prop, eVar, gebeurtenis, enzovoort)</li><li>Geen tekenlimiet (100 tekens voor props)</li><li>Zeer krachtige rapportage en beschikbaarheid van gegevens, omdat Adobe Experience Platform is gebouwd op voeding [Gebruiksgevallen voor realtime personalisatie](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)</li><li>Toekomstbestendig (u krijgt alle nieuwste functies en functies)</li><li>Tags consolideren voor het verzamelen van Adobe Experience Cloud-gegevens tussen andere Experiencen Cloud (AJO, RTCDP enzovoort)</li><li>[Apparaat-id&#39;s van eerste partij](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/first-party-device-ids.html) voor een grotere nauwkeurigheid van de identificatie van de bezoeker</li></ul> | <ul><li>De meest tijdrovende en veeleisende migratiemethode<p>Moet het volledige schema in XDM opnieuw tot stand brengen alvorens u kunt beginnen het Web SDK uit te voeren</p></li></ul> |
| **Adobe Analytics migreren naar de web SDK** | <ul><li>Behoudt de regels en gegevenselementen die al in uw Adobe Analytics-implementatie zijn geconfigureerd.</li><li>Hiermee kunt u naar de SDK van het web gaan zonder dat dit van invloed is op uw bestaande Adobe Analytics-rapportage.</li><li>Verstrekt flexibiliteit om een schema XDM voor uw organisatie in een recentere tijd tot stand te brengen: een flexibel schema om het even welke gebieden te bepalen u, en slechts die gebieden nodig hebt die relevant zijn.</br>Vereist niet de Adobe Analytics Experience Event-veldgroep in Customer Journey Analytics. <!-- With the new implementation, you're double-counting with 2 implementation; with the migration, you're double-counting, but both of them are through Edge Network. --></li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (voor prop, eVar, gebeurtenis, enzovoort)</li><li>Geen tekenlimiet (100 tekens voor props)</li><li>Zeer krachtige rapportage en beschikbaarheid van gegevens, omdat Adobe Experience Platform is gebouwd op voeding [Gebruiksgevallen voor realtime personalisatie](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)</li><li>Toekomstbestendig (u krijgt alle nieuwste functies en functies)</li><li>Tags consolideren voor het verzamelen van Adobe Experience Cloud-gegevens tussen andere Experiencen Cloud (AJO, RTCDP enzovoort)</li><li>[Apparaat-id&#39;s van eerste partij](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/first-party-device-ids.html) voor een grotere nauwkeurigheid van de identificatie van de bezoeker</li></ul> | <ul><li>Moet op een gegeven moment in de toekomst voldoen aan een XDM-schema, waarbij gebruik wordt gemaakt van gegevenstoewijzing.</li><li>Neemt enige technische schuld op. Verouderde AppMeasurement- of analyseextensiecode kan bijvoorbeeld blijven bestaan. </li></ul> |
| **Bronverbinding voor analyse** | <ul><li>Minder tijdrovende en veeleisende migratiemethode. <p>Gegevens worden snel naar Customer Journey Analytics gemigreerd met minimale investeringen</p></li></ul> | <ul><li>De gegevens worden niet verzonden naar de Edge Network en kunnen niet met andere toepassingen van Adobe Experience Platform worden gedeeld; het wordt beperkt tot Customer Journey Analytics slechts<li>Moeilijk om naar SDK van het Web in de toekomst te bewegen</li><li>Gebruikt de het gebiedsgroep van de Gebeurtenis van de Ervaring van Analytics in uw schema.</br>Deze veldgroep voegt veel Adobe Analytics-gebeurtenissen toe die niet nodig zijn in uw Customer Journey Analytics-schema.  Dit kan leiden tot een overzichtelijker, complex schema dan wat anders voor Customer Journey Analytics nodig is.</li><li>Hoogste niveau van [latentie](/help/admin/guardrails.md#latencies) alle implementatiemethoden</li></ul> |

{style="table-layout:auto"}

### Voor Adobe Analytics-implementaties met: Web SDK

De volgende lijst toont de migratiemethodes beschikbaar voor organisaties die Adobe Analytics met het Web SDK hebben uitgevoerd:

| Migratiemethode | Voordelen | Nadelen |
|---------|----------|---------|
| **Vorm de implementatie van SDK van het Web van Adobe Analytics om gegevens naar Customer Journey Analytics te verzenden** | Dit is de voorkeursmigratiemethode als uw Adobe Analytics-implementatie al gebruikmaakt van de Web SDK. <p>Wanneer u deze implementatiemethode gebruikt, kunt u kiezen of u uw bestaande Adobe Analytics-schema wilt gebruiken of dat u het XDM-schema kunt bijwerken zodat u het beter kunt afstemmen op de behoeften van uw organisatie wanneer u andere platformtoepassingen gaat gebruiken.</p><p>**Het Adobe Analytics-schema gebruiken**</p><p>De voordelen van het Adobe Analytics-schema zijn:</p><ul><li>Gemakkelijk migreren<p>Als u reeds gegevens naar Adobe Analytics met het Web SDK van Adobe Experience Platform verzendt, kunt u de extra dienst aan uw gegevensstroom toevoegen om gegevens naar Adobe Experience Platform te verzenden (die dan in uw configuratie van de Customer Journey Analytics kan worden gebruikt).</p></li></ul><p>De nadelen van het gebruik van het Adobe Analytics-schema zijn:</p><ul><li>Terwijl het gebruiken van het schema van Adobe Analytics beperkt u niet in termen van hoe het met andere toepassingen van het Platform kan worden gebruikt, resulteert het in een schema dat complexer is dan het anders zou kunnen zijn. Dit komt omdat het Adobe Analytics-schema veel objecten bevat die specifiek zijn voor Adobe Analytics en die waarschijnlijk niet door uw organisatie worden gebruikt.<p>Wanneer wijzigingen in het schema vereist zijn, moet u door duizenden ongebruikte velden bladeren om het veld te zoeken dat moet worden bijgewerkt.</p></li></ul><p>**Het XDM-schema gebruiken**</p><p>De voordelen van het bijwerken van het XDM-schema zijn:</p><ul><li>Een gestroomlijnd schema dat aan de behoeften van uw organisatie en de specifieke toepassingen van het Platform wordt aangepast die u gebruikt.</li><p>Wanneer veranderingen in het schema worden vereist, moet u niet door duizenden ongebruikte gebieden bewegen om het gebied te vinden dat het bijwerken vereist.</p></ul><p>De nadelen van het bijwerken van het XDM-schema zijn:</p><ul><li>Het bijwerken van uw schema is een tijdrovend proces dat wordt vereist alvorens u begint gegevens naar Customer Journey Analytics te verzenden.</li></ul> | Geen |

{style="table-layout:auto"}

## Vervolgens verzendt u gegevens naar Adobe Experience Platform

Nadat u de bovenstaande informatie gebruikt om een migratiemethode te kiezen, leert u hoe te [gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md) afhankelijk van de gekozen migratiemethode.
