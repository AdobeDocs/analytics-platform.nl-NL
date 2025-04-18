---
title: Adobe Analytics-rapportsuite gebruiken in Customer Journey Analytics
description: Hoe te om Adobe Analytics rapportsuites voor opname in Adobe Experience Platform en Customer Journey Analytics te vormen
role: User
solution: Customer Journey Analytics
feature: Basics
exl-id: db5506e0-6159-4d4b-8149-e4966dab9807
source-git-commit: eb9b749a5c61da3b4b5d2eeeed93bf5e4702a415
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# Adobe Analytics-rapportsuite gebruiken in Customer Journey Analytics

De klanten van Adobe Analytics kunnen hun rapportsuites in Adobe Experience Platform en Customer Journey Analytics gemakkelijk hefboomwerken gebruikend de [ bron van Analytics schakelaar ](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html). Hieronder wordt uitgelegd hoe u dit doet.

>[!IMPORTANT]
>
>U moet het **Uitgezochte** pakket hebben om gegevensanalyse over meer dan één rapportreeks uit te voeren. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt. &#x200B;

## Voorbereiding

Aangezien u klaar bent om Adobe Analytics te gebruiken rapportsuites in Adobe Experience Platform en Customer Journey Analytics, zijn er verscheidene dingen u zou moeten doen om uw gegevens voor een naadloze beweging aan Customer Journey Analytics voor te bereiden. Lees de volgende pagina voor meer informatie:

* [Adobe Analytics naar Customer Journey Analytics evolutie](/help/getting-started/aa-to-cja.md)

## Rapportsuites instellen voor opname in de Adobe Experience Platform en Customer Journey Analytics

Zodra u uw gegevens hebt voorbereid, bent u klaar om rapportsuites voor gebruik in Adobe Experience Platform en Customer Journey Analytics te vormen.

1. **creeer een gegevensstroom voor elke rapportreeks u wenst om in Adobe Experience Platform en Customer Journey Analytics te gebruiken.** De [ bron van Analytics schakelaar ](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html) is het hulpmiddel dat u toestaat om [ een verbinding ](/help/connections/create-connection.md) (a.k.a dataflow) tussen Adobe Analytics en Adobe Experience Platform tot stand te brengen. U zult de bronschakelaar gebruiken om één dataflow voor elke rapportreeks tot stand te brengen u in Adobe Experience Platform wilt gebruiken. Dataflow leidt tot een exemplaar van uw gegevens van de rapportreeks waar het schema in [ XDM ](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/schemas-and-experience-data-model.html) voor consumptie door de toepassingen van Adobe Experience Platform met inbegrip van Customer Journey Analytics is omgezet.<p>Elke rapportreeks die met een dataflow via de bronschakelaar wordt gevormd wordt opgeslagen als afzonderlijke dataset in het meer van Gegevens van Adobe Experience Platform. 13 maanden historische rapportsuite-gegevens worden automatisch bij elke gegevensstroom opgenomen en nieuwe gegevens worden doorlopend naar Adobe Experience Platform verzonden. (Met ingang van 26 april 2023 is de achtergrondvulling in niet-productiesandboxen beperkt tot 3 maanden.) Met de bronschakelaar van de Analyse hoeft u zich geen zorgen te maken over het vooraf maken van het schema. Er wordt automatisch een gestandaardiseerd schema voor Adobe Analytics gemaakt. Nochtans, kan het hulpmiddel van de Prep van Gegevens van Adobe Experience Platform [ ](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html) worden gebruikt om dit schema te verbeteren alvorens het gegeven in het meer van Gegevens wordt opgeslagen en ter beschikking gesteld aan Customer Journey Analytics. Houd er rekening mee dat bepaalde soorten gegevens worden gesegmenteerd door de bronaansluiting en niet aanwezig zijn in de gegevensset in het Data Lake van Adobe Experience Platform. Andere rijen kunnen worden opgesplitst tussen Data Lake en Customer Journey Analytics. Zie [ uw gegevens van Adobe Analytics met de gegevens van Customer Journey Analytics ](/help/troubleshooting/compare.md) voor meer details vergelijken.
1. **Prep van Gegevens van het Gebruik om u te helpen rapportreeksen in Customer Journey Analytics combineren.** Data Prep kan worden gebruikt voor vele soorten gegevenstransformatie, en één algemeen gebruik voor Adobe Analytics gegevens is om verschillen in pro- en/of eVar-toewijzingen over veelvoudige rapportreeksen op te lossen zodat de rapportsuites gemakkelijk in Customer Journey Analytics kunnen worden gecombineerd. Zie [ rapportreeksen met verschillende schema&#39;s ](/help/use-cases/aa-data/combine-report-suites.md) voor meer details combineren.
1. **laat het Plaatsen** zonodig toe. Wanneer u meerdere gegevenssets combineert in Customer Journey Analytics, kunt u met de koppelingsmogelijkheden verschillende id-naamruimten omzetten in één vergrendelde id voor één weergave van de klant op verschillende apparaten en kanalen. Zie [ het Plaatsen overzicht ](../../stitching/overview.md) voor meer details.
1. **creeer één of meerdere verbindingen van Customer Journey Analytics.** Zodra de datasets voor uw rapportreeksen in het Meer van Gegevens van Adobe Experience Platform beschikbaar zijn, kunt u één of meerdere [ verbindingen van Customer Journey Analytics ](/help/connections/overview.md) tot stand brengen om die datasets in Customer Journey Analytics te brengen. Binnen een verbinding, kunnen de gegevens van de rapportreeks met andere soorten gegevens worden gecombineerd, die u toestaan om een ware dwars-kanaalmening van klantenervaringen tot stand te brengen.
1. **creeer één of meerdere de gegevensmeningen van Customer Journey Analytics.** a [ gegevensmening ](/help/data-views/data-views.md) is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van een verbinding van Customer Journey Analytics te interpreteren. De meningen van gegevens hebben vele krachtige [ configuratieopties ](/help/data-views/create-dataview.md) voor het aanpassen van de gegevens die aan uw gebruikers binnen [ Analysis Workspace ](/help/analysis-workspace/home.md) worden voorgesteld.

## Customer Journey Analytics en Adobe Analytics vergelijken

Customer Journey Analytics en Adobe Analytics hebben een aantal overeenkomsten. Zowel Customer Journey Analytics als Adobe Analytics bieden bijvoorbeeld de kracht van Analysis Workspace voor een snelle analyse van de vrije vorm. Aangezien Customer Journey Analytics echter een toepassing is binnen de Adobe Experience Platform en Adobe Experience Platform gebruikt voor gegevensinvoer, verschillen Customer Journey Analytics en Adobe Analytics op een aantal belangrijke manieren. De volgende artikelen zijn nuttig om deze verschillen te begrijpen:

* [Adobe Analytics-gegevens vergelijken met Customer Journey Analytics-gegevens](/help/troubleshooting/compare.md)
* [Ondersteuning voor Customer Journey Analytics-functies](/help/getting-started/aa-vs-cja/cja-aa.md)
* [Vergelijk terminologie voor de gegevens van de Analyse die door de bron van de Analyse schakelaar worden overgegaan](/help/getting-started/aa-vs-cja/terminology.md)
* [Vergelijk gegevensverwerking in Adobe Analytics en Customer Journey Analytics rapportfuncties](/help/getting-started/aa-vs-cja/data-processing-comparisons.md)
* [Virtuele rapportsuites, gegevensweergaven, Adobe Experience Platform-sandboxen en de gegevensbronconnector van Analytics](/help/getting-started/aa-vs-cja/vrs-dataview-sandbox-adc.md)
* [Verwerkingsregels, VISTA en classificaties versus Data Prep](/help/getting-started/aa-vs-cja/pr-vista-dataprep.md)
* [STEUN, ECID, AACUSTOMID en de bronaansluiting voor Analytics](/help/getting-started/aa-vs-cja/aaid-ecid-adc.md)
