---
title: Vergelijking met Adobe Analytics
description: Overzicht van hoe Customer Journey Analytics zich verhoudt tot Adobe Analytics.
solution: Customer Journey Analytics
feature: Basics
exl-id: bde36283-86af-4b1a-9cbe-e251676b2951
role: User
source-git-commit: 46d799ad2621d83906908a3f60a59a1027c6518c
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Vergelijking met Adobe Analytics

In dit gedeelte van de documentatie wordt uitgelegd hoe u de verschillen tussen Adobe Customer Journey Analytics en Adobe Analytics kunt vergelijken en begrijpen.

Het fundamentele verschil tussen de twee oplossingen is de breedte van gegevens u (kan) overwegen wanneer het bouwen van uw rapporten en analyse.

In Customer Journey Analytics, *alle* de gegevensbron kan deel van de gegevens uitmaken u voor rapportering en analyse gebruikt. Adobe Analytics is voornamelijk gericht op online gegevens die worden verzameld van websites en mobiele apps. Adobe Analytics biedt mogelijkheden om gegevens uit andere bronnen te importeren, maar het belangrijkste doel hiervan is om meer context te bieden rond de eerder vermelde online gegevens.

## Gegevensverzameling

Customer Journey Analytics baseert zich op gegevens die in de datasets van Adobe Experience Platform worden opgeslagen. U hebt verscheidene opties om gegevens van deze datasets in Experience Platform te verzamelen en in te voeren. Deze opties worden meer gedetailleerd beschreven in de [Overzicht van gegevensinname](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/data-ingestion.html).

Adobe Analytics verzamelt uiteindelijk gegevens binnen de oplossing zelf. Ook hier hebt u verschillende opties om die gegevens te verzamelen. Deze opties worden in de [Adobe Analytics-implementatiehandleiding](https://experienceleague.adobe.com/docs/analytics/implementation/home.html).

U kunt de gegevens van uw Adobe Analytics-rapportsuite in Customer Journey Analytics gebruiken met de [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html). Deze schakelaar neemt de gegevens die in Adobe Analytics worden verzameld in Experience Platform op. U kunt dan een verbinding aan deze dataset in Customer Journey Analytics tot stand brengen. Zie [Gegevens uit Adobe Analytics-rapportsuite gebruiken in Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html) voor meer informatie .


## Gegevensverwerking

Voordat u gegevens kunt rapporteren, moet u deze gegevens vaak verwerken om ervoor te zorgen dat de gegevens correct kunnen worden gebruikt voor rapportage. Gegevensverwerking kan plaatsvinden tijdens het verzamelen en tijdens het rapporteren.

In het algemeen, wordt de Customer Journey Analytics ontworpen om met de verzamelde en opgeslagen gegevens in de dataset van het Experience Platform in rapporttijd te werken. De Customer Journey Analytics biedt krachtige rapport-tijd verwerkingsfunctionaliteit aan om de gegevens klaar voor rapportering en analyse te verzekeren. Als u gegevens moet toewijzen, transformeren en valideren voordat deze in het Experience Platform worden opgenomen, kunt u de opdracht [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html) functionaliteit van Experience Platform.

In Adobe Analytics vindt de meeste verwerking van gegevens plaats onmiddellijk nadat de gegevens zijn verzameld.

Zie [Gegevensverwerking in Adobe Analytics en Customer Journey Analytics vergelijken](data-processing-comparisons.md) en [Verwerkingsregels, VISTA, en classificaties versus Prep van Gegevens](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/pr-vista-dataprep.html) voor meer informatie .


## Terminologie

De Customer Journey Analytics biedt flexibiliteit op hoe u dimensies en metriek bepaalt, die door de flexibiliteit wordt toegelaten die de onderliggende op model van de Gegevens van de Ervaring (XDM) gebaseerde schema&#39;s verstrekken. Wanneer Adobe Analytics bijvoorbeeld bezoekers, bezoeken en treffers gebruikt, gebruikt de Customer Journey Analytics personen, sessies en gebeurtenissen als equivalente concepten (u kunt de naamgeving naar eigen inzicht wijzigen).

Zie [Vergelijk terminologie voor de gegevens van de Analyse die door de bron van de Analyse schakelaar worden overgegaan](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/terminology.html) voor meer informatie over de verschillen in terminologie .


## Virtuele rapportage-omgevingen en sandboxen

Adobe Analytics heeft het concept van virtuele rapportsuites, die u toestaat om uw verzamelde gegevens te segmenteren en toegang tot die gesegmenteerde gegevens te controleren.

Customer Journey Analytics heeft een vergelijkbaar concept, genaamd gegevensweergaven. Gegevensweergaven zijn containers waarmee u kunt bepalen hoe gegevens van een verbinding moeten worden geïnterpreteerd. Ze bieden ultieme flexibiliteit om dimensies en maatstaven te specificeren en te configureren in voorbereiding op uw rapportage en analyse.

Experience Platform biedt sandboxen die kunnen worden beschouwd als een container met gegevens en toepassingen voor een bepaalde omgeving. De functionaliteit van een sandbox is niet gerelateerd aan een virtuele Adobe Analytics-rapportsuite of gegevensweergave van een Customer Journey Analytics. Adobe Analytics heeft zelf helemaal geen afhankelijkheid of relatie met Experience Platform sandboxen. Customer Journey Analytics ondersteunt wel Experience Platforms sandboxen, maar er zijn enkele belangrijke punten.

Zie [Virtuele rapportsuites, de meningen van Gegevens, de zandbakken van Adobe Experience Platform, en de de bronschakelaar van de Analyse](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/vrs-dataview-sandbox-adc.html) voor meer informatie .


## Identiteiten

Customer Journey Analytics steunt de identiteiten die u als deel van de schema&#39;s bepaalt waaraan de datasets die uw gegevens bevatten in overeenstemming zijn. Identiteiten vormen als zodanig een grondbegrip van het Experience Platform, dat de Customer Journey Analytics gebruikt bij het opzetten van een [verbinding](../../connections/overview.md) (door de persoon-id voor elke gegevensset te definiëren) en bij het toepassen van [verstikken](../../stitching/overview.md) voor kanaalanalyse. Een belangrijke identiteit die wordt gebruikt door de Experience Platform-SDK&#39;s en -API is de Experience Cloud-id (ECID).

Adobe Analytics gebruikt een meer definitieve reeks identiteitsvelden, zoals de Adobe Analytics ID (AID). Bij gebruik van de gegevensbronaansluiting krijgen deze Adobe Analytics-identificatievelden een speciale behandeling. Zie [AID, ECID, AACUSTOMID en de bronconnector Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aaid-ecid-adc.html) voor meer informatie .


## Ondersteunde functies

Een overzicht van Adobe Analytics-functies en hoe deze functies door Customer Journey Analytics worden ondersteund, kunt u vinden op [Ondersteuning van Customer Journey Analytics-functies](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/cja-aa.html).
