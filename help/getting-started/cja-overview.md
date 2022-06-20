---
title: Overzicht van Customer Journey Analytics
description: Leer hoe u met Customer Journey Analytics Analysis Workspace gegevens uit Experience Platform kunt gebruiken.
exl-id: f4f692c9-5951-4fa2-8e9f-5eeff0f79d10
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: 9afc0931622509769e53ff5df3ffaa2d99894488
workflow-type: tm+mt
source-wordcount: '1258'
ht-degree: 1%

---

# Overzicht van Customer Journey Analytics

Customer Journey Analytics is een analysemogelijkheid waarmee u de kracht van Analysis Workspace kunt gebruiken met gegevens van Adobe Experience Platform. Het kan onderbreken, filter, vraag, en visualiseert jaren&#39; waarde van gegevens, en wordt gecombineerd met de capaciteit van het Platform om allerlei gegevensschema&#39;s en types te houden. Met de **Experience Data Model (XDM)** Gegevens kunnen op uniforme wijze worden weergegeven en geordend, klaar voor combinatie en onderzoek. **Experience Query Services** staat u toe om SQL-compatibele hulpmiddelen en kaders te gebruiken om al uw gegevens te vragen en te manipuleren.

De CJA-architectuur op hoog niveau wordt hier weergegeven:

![architectuur](assets/cja-architecture.png)

Hier volgt een video-overzicht van Customer Journey Analytics:

>[!VIDEO](https://video.tv.adobe.com/v/30090/?quality=12)

## CJA vergelijken met Traditionele Adobe Analytics

Customer Journey Analytics breidt het bereik van Adobe Analytics uit door gebruiksvriendelijke kanaalmogelijkheden te bieden en beperkingen in eerdere versies van Adobe Analytics te verwijderen. Enkele opmerkelijke verbeteringen zijn:

* **Onbeperkte variabelen en gebeurtenissen**: De concepten eVars, props en gebeurtenissen bestaan niet meer. De gegevens zijn vooral gericht op dimensies en metriek. Gegevenssets kunnen een onbeperkte hoeveelheid unieke afmetingen en metriek hebben.
* **Onbeperkte unieke waarden**: Adobe Experience Platform is niet beperkt tot enige unieke beperking.
* **Historische gegevens wijzigen**: Met Adobe Experience Platform kunnen gegevens worden verwijderd of gecorrigeerd.
* **Gegevens uit meerdere rapporten**: Bestaande implementaties van meerdere gegevenssets kunnen in Platform worden gecombineerd.

De eerste release van Customer Journey Analytics bevat veel van de functies die in Analysis Workspace zijn opgenomen. Voor een volledige lijst raadpleegt u [Ondersteuning voor Customer Journey Analytics-functies](/help/getting-started/aa-vs-cja/cja-aa.md).

## CJA vergelijken met apparaatanalyse

[Apparaatanalyse](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html) integreert met [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=nl), waarbij de coopgrafiek of de privégrafiek wordt gebruikt om te bepalen hoe digitale apparaten aan personen worden toegewezen. Deze is beschikbaar voor Adobe Analytics Ultimate-klanten.

CJA daarentegen integreert met Adobe Experience Platform-gegevenssets en maakt kanaalanalyse in Analysis Workspace mogelijk. Hoewel CJA nog niet met de coop of de Privé identiteitsgrafieken integreert, kunt u &quot;uw eigen identiteitskaart&quot;brengen om datasets samen te voegen. Die datasets kunnen verder gaan dan digitale gegevens om zowel online als offline aanraakpunten te omvatten. CJA-voorwaarden worden hieronder gedetailleerder behandeld.

## Hoofdgebruik

Met Customer Journey Analytics kunt u:

* **Bekijk de klant in een reiscontext**: U kunt gegevens opeenvolgend bekijken en analyseren, die veelvoudige kanalen overspannen. De gegevens van uw vraagcentrum, POS systemen, en online eigenschappen kunnen in één enkele rapporteringsmening worden gecombineerd.
* **Inzichten voor iedereen beschikbaar maken**: De gegevenstoegang van de democratisering en meer mensen laten bedrijfsbesluiten met gegeven-afgeleide inzichten maken. Iedereen in de organisatie met verantwoordelijkheid voor om het even welk aspect van de klantenervaring kan echte besluiten sneller maken, die op volledigere gegevens worden gebaseerd.
* **Maak gebruik van de kracht van gegevenswetenschap voor uw analisten**: Customer Journey Analytics laat normale mensen data science gebruiken om diepe inzichten en analyse te ontsluiten.
* **Visualiseer en interactie met uw datasets gebruikend ad hoc rapportering**: De werkruimte kan om het even welke dataset van Adobe Experience Platform gebruiken die aan sommige basisregels in overeenstemming is.
* **Niet-webgegevens weergeven**: De werkruimte is niet langer beperkt tot een starre definitie van een &#39;hit&#39; of &#39;event&#39;. De schema&#39;s van de douane staan volledige controle over gegevens en definities toe.
* **Meer controle over het manipuleren van gegevens**: De gegevens van de verandering u hebt geupload, creeert nieuwe datasets, en voert hen in Werkruimte in. Adobe Experience Platform biedt hulpprogramma&#39;s voor het opvragen, extraheren, transformeren en laden via de Experience Cloud Query Service.

## Vereisten

Voordat u kunt beginnen met het gebruik van Customer Journey Analytics, moet aan de volgende voorwaarden worden voldaan:

* Uw organisatie heeft een actief contract met Adobe Analytics voor Select, Prime of Ultimate met de Customer Journey Analytics add-on. Neem contact op met de accountmanager van uw organisatie als u niet zeker weet welk type contract u hebt of als u de CJA-invoegtoepassing hebt.
* Uw organisatie is ingericht voor Adobe Experience Platform.

## Beheerdersrechten

Om verbindingen tot stand te brengen, voeg datasets toe, enz., hebt u de volgende toestemmingen in nodig [Admin Console](https://adminconsole.adobe.com/enterprise/):

* Als u toegang wilt krijgen tot Customer Journey Analytics of verbinding wilt maken, moet u als Admin aan het dialoogvenster **Customer Journey Analytics-product** in de [Admin Console](https://adminconsole.adobe.com/enterprise/). Aan productbeheerders worden de volgende machtigingen verleend:
   * Verbindingen of gegevensweergaven maken/bijwerken/verwijderen
   * Werk/schrapt projecten, filters, calc metriek of filters bij die door andere gebruikers worden gecreeerd
   * Een Workspace-project delen met alle gebruikers
* Het alleen binnen Customer Journey Analytics beheren van een product is niet voldoende om een verbinding te maken, bij te werken of te verwijderen. Om een verbinding aan een dataset van de Experience Platform tot stand te brengen, hebt u ook de toestemmingen van het Experience Platform nodig. U moet specifiek deel uitmaken van een **Productprofiel Experience Platform** dat u de volgende toestemmingen geeft:
   * Schema&#39;s weergeven
   * Schema&#39;s beheren
   * Identiteitsnaamruimten weergeven
   * Gegevensbestanden weergeven

Voor meer informatie over de toestemmingen van het Experience Platform, zie [Toegangsbeheer in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html).

>[!NOTE]
>
>U kunt geen toestemming geven voor individuele metriek of dimensies in Customer Journey Analytics, zoals in traditionele Adobe Analytics. Metriek en afmetingen kunnen worden gewijzigd in [gegevensweergaven](/help/data-views/data-views.md) en zijn derhalve onderhevig aan wijzigingen in de CJA, die ook de rapportage met terugwerkende kracht wijzigen.

### Toegang van gebruikers

Niet-productbeheerders (gebruikers) in Customer Journey Analytics kunnen de Weergaven of Verbindingen van Gegevens niet bekijken, maar kunnen filters, projecten, en berekende metriek tot stand brengen.

## Terminologie-updates

Verschillende functies in CJA hebben in vergelijking met traditionele Adobe Analytics een andere naam gekregen om zich aan te passen aan de industriestandaarden. Enkele bijgewerkte terminologie:

* Segmenten worden nu &#39;filters&#39; genoemd.
* Virtuele rapportsets worden nu &#39;gegevensweergaven&#39; genoemd.
* Classificaties worden nu &#39;Gegevensbestanden opzoeken&#39; genoemd.
* Klantkenmerken worden nu &#39;profielgegevenssets&#39; genoemd.
* De containers van de greep zijn nu genoemd geworden &quot;Event&quot;containers.
* Visitecontainers worden nu &#39;Sessie&#39;-containers genoemd.
* Bezoekerscontainers worden nu &#39;Person&#39;-containers genoemd.

## Andere mogelijkheden die op Adobe Experience Platform zijn gebaseerd

Customer Journey Analytics is één van de mogelijkheden van velen die op de Adobe Experience Platform vertrouwen. Met verschillende andere mogelijkheden, die ook op Experience Platform zijn gebaseerd, kunt u optimaal profiteren van uw gegevens.

Met Adobe Experience Platform kunt u klantgegevens en -inhoud van elk systeem centraliseren en standaardiseren en gegevens en computertraining toepassen om het ontwerp en de levering van persoonlijke ervaringen te verbeteren. De gegevens van de klant in het platform worden opgeslagen als datasets, die uit een schema en partijen gegevens bestaan. Zie voor meer informatie over het platform [Overzicht van Adobe Experience Platform-architectuur](https://experienceleague.adobe.com/docs/platform-learn/tutorials/intro-to-platform/basic-architecture.html).

Van de Ingestie van Gegevens aan directe SQL toegang, zijn verscheidene componenten van het Experience Platform centraal aan Customer Journey Analytics en handelen samen met het:

* [Query-service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl): Gebruik standaard SQL om gegevens van Adobe Experience Platform terug te winnen, zoals de oplossingsgegevens van de Adobe, klant 1st-party gegevens, of een andere Platform gegevens. Het is een server-zonder hulpmiddel dat u toestaat om zich bij om het even welke datasets aan te sluiten en de vraagresultaten als nieuwe dataset voor gebruik in rapportering, de Werkruimte van de Wetenschap van Gegevens, of voor opname in de Dienst van het Profiel te vangen. U kunt de Dienst van de Vraag gebruiken om gegevensanalysecosystemen te bouwen, die tot een beeld van consumenten over hun diverse interactiekanalen leiden. Deze kanalen zouden de systemen van het Punt-van-verkoop, Web, Mobiel, CRM, enz. kunnen omvatten.
* [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html):
* [Identiteitsservice](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html):
* [Werkruimte voor gegevenswetenschap](https://experienceleague.adobe.com/docs/experience-platform/data-science-workspace/home.html) in de optie &quot;developer&quot;: u kunt prebuilt artificiële intelligentie (AI) en machine-leert modellen in Adobe Experience Platform gebruiken om diverse punten van de klantenreis te beïnvloeden. Door verborgen inzichten te negeren, kunt u betere voorspellingen over de klantenreis maken, geadviseerde beste volgende stappen voorstellen, of lastige processen automatiseren.

## Video&#39;s

* Werken met gegevens in Customer Journey Analytics:

   >[!VIDEO](https://video.tv.adobe.com/v/32112/?quality=12)

* Architectuur en integratie van Customer Journey Analytics:

   >[!VIDEO](https://video.tv.adobe.com/v/32483/?quality=12)

