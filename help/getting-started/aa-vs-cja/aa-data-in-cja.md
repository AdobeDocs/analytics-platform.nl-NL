---
title: Adobe Analytics-rapportsuite voor gegevens in Customer Journey Analytics gebruiken
description: Hoe te om Adobe Analytics rapportsuites voor opname in Adobe Experience Platform en Customer Journey Analytics te vormen
role: User
solution: Customer Journey Analytics
feature: Basics
exl-id: db5506e0-6159-4d4b-8149-e4966dab9807
source-git-commit: 46d799ad2621d83906908a3f60a59a1027c6518c
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# Adobe Analytics-rapportsuite voor gegevens in Customer Journey Analytics gebruiken

Adobe Analytics-klanten kunnen hun rapportsuites in de Adobe Experience Platform en de Customer Journey Analytics eenvoudig benutten met behulp van de [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html). Hieronder wordt uitgelegd hoe u dit doet.

>[!IMPORTANT]
>
>U moet beschikken over **Selecteren** pakket om gegevensanalyse uit te voeren over meer dan één rapportreeks. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt. &#x200B;

## Voorbereiding

Aangezien u klaar bent om Adobe Analytics te gebruiken rapportreeksen in Adobe Experience Platform en Customer Journey Analytics, zijn er verscheidene dingen u zou moeten doen om uw gegevens voor een naadloze beweging aan Customer Journey Analytics voor te bereiden. Lees de volgende pagina voor meer informatie:

* [Adobe Analytics naar Customer Journey Analytics evolutie](/help/getting-started/aa-to-cja.md)

## Rapportsuites instellen voor opname in de Adobe Experience Platform en de Customer Journey Analytics

Zodra u uw gegevens hebt voorbereid, bent u klaar om rapportseries voor gebruik in Adobe Experience Platform en Customer Journey Analytics te vormen.

1. **Maak een gegevensstroom voor elke rapportsuite die u in Adobe Experience Platform en Customer Journey Analytics wilt gebruiken.** De [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html) is het gereedschap waarmee u [een verbinding maken](/help/connections/create-connection.md) (ook bekend als dataflow) tussen Adobe Analytics en Adobe Experience Platform. U zult de bronschakelaar gebruiken om één dataflow voor elke rapportreeks tot stand te brengen u in Adobe Experience Platform wilt gebruiken. De dataflow leidt tot een exemplaar van uw gegevens van de rapportreeks waar het schema is omgezet in  [XDM](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/schemas-and-experience-data-model.html) voor gebruik door Adobe Experience Platform-toepassingen, met inbegrip van Customer Journey Analytics.<p>Elke rapportreeks die met een dataflow via de bronschakelaar wordt gevormd wordt opgeslagen als afzonderlijke dataset in het meer van Gegevens van Adobe Experience Platform. 13 maanden historische rapportsuite-gegevens worden automatisch bij elke gegevensstroom opgenomen en nieuwe gegevens worden doorlopend naar Adobe Experience Platform verzonden. (Met ingang van 26 april 2023 is de achtergrondvulling in niet-productiesandboxen beperkt tot 3 maanden.) Met de bronschakelaar van de Analyse hoeft u zich geen zorgen te maken over het vooraf maken van het schema. Er wordt automatisch een gestandaardiseerd schema voor Adobe Analytics gemaakt. Adobe Experience Platform [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html) kan worden gebruikt om dit schema te verbeteren voordat de gegevens in het Datameer worden opgeslagen en ter beschikking van de Customer Journey Analytics worden gesteld. Houd er rekening mee dat bepaalde soorten gegevens worden uitgefilterd door de bronaansluiting en niet aanwezig zijn in de gegevensset in het Adobe Experience Platform Data Lake. Andere rijen kunnen worden uitgefilterd tussen het Data Lake en de Customer Journey Analytics. Zie [Adobe Analytics-gegevens vergelijken met Customer Journey Analytics-gegevens](/help/troubleshooting/compare.md) voor meer informatie .
1. **Met Data Prep kunt u rapportsuites in Customer Journey Analytics combineren.** Data Prep kan voor vele soorten gegevenstransformatie worden gebruikt, en één gemeenschappelijk gebruik voor de gegevens van Adobe Analytics is om verschillen in pro en/of eVar afbeeldingen over veelvoudige rapportreeksen op te lossen zodat de rapportsuites gemakkelijk binnen Customer Journey Analytics kunnen worden gecombineerd. Zie [rapportsuites combineren met verschillende schema&#39;s](/help/use-cases/aa-data/combine-report-suites.md) voor meer informatie .
1. **Enable Stitching** indien nodig. Wanneer het combineren van veelvoudige datasets in Customer Journey Analytics, kunnen de het stitching mogelijkheden helpen verschillende identiteitskaart namespaces in één enkele vastgemaakte identiteitskaart voor één enkele mening van de klant over apparaten en kanalen oplossen. Zie [Overzicht van tekenreeksen](../../stitching/overview.md) voor meer informatie .
1. **Maak een of meer Customer Journey Analytics-verbindingen.** Zodra de datasets voor uw rapportreeksen in het meer van de Gegevens van Adobe Experience Platform beschikbaar zijn, kunt u één of meerdere tot stand brengen [Customer Journey Analytics-verbindingen](/help/connections/overview.md) deze gegevensbestanden in Customer Journey Analytics te brengen. Binnen een verbinding, kunnen de gegevens van de rapportreeks met andere soorten gegevens worden gecombineerd, die u toestaan om een ware dwars-kanaalmening van klantenervaringen tot stand te brengen.
1. **Maak een of meer gegevensweergaven voor Customers Journey Analytics.** A [gegevensweergave](/help/data-views/data-views.md) is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van een verbinding van de Customer Journey Analytics te interpreteren. Gegevensweergaven hebben veel kracht [configuratieopties](/help/data-views/create-dataview.md) voor het aanpassen van de gegevens die binnen aan uw gebruikers worden voorgesteld [Analysis Workspace](/help/analysis-workspace/home.md).

## Customer Journey Analytics en Adobe Analytics vergelijken

Customer Journey Analytics en Adobe Analytics hebben een aantal gelijkenissen. Zowel Customer Journey Analytics als Adobe Analytics bieden bijvoorbeeld de kracht van Analysis Workspace voor een snelle analyse van de vrije vorm. Aangezien Customer Journey Analytics echter een toepassing is binnen de Adobe Experience Platform en Adobe Experience Platform gebruikt voor gegevensinvoer, verschillen de Customer Journey Analytics en Adobe Analytics op een aantal belangrijke manieren. De volgende artikelen zijn nuttig om deze verschillen te begrijpen:

* [Adobe Analytics-gegevens vergelijken met Customer Journey Analytics-gegevens](/help/troubleshooting/compare.md)
* [Ondersteuning van Customer Journey Analytics-functies](/help/getting-started/aa-vs-cja/cja-aa.md)
* [Vergelijk terminologie voor de gegevens van de Analyse die door de bron van de Analyse schakelaar worden overgegaan](/help/getting-started/aa-vs-cja/terminology.md)
* [Vergelijk gegevensverwerking in Adobe Analytics en Customer Journey Analytics rapportagefuncties](/help/getting-started/aa-vs-cja/data-processing-comparisons.md)
* [Virtuele rapportsuites, gegevensweergaven, Adobe Experience Platform-sandboxen en de gegevensbronconnector van Analytics](/help/getting-started/aa-vs-cja/vrs-dataview-sandbox-adc.md)
* [Verwerkingsregels, VISTA en classificaties versus Data Prep](/help/getting-started/aa-vs-cja/pr-vista-dataprep.md)
* [STEUN, ECID, AACUSTOMID en de bronaansluiting voor Analytics](/help/getting-started/aa-vs-cja/aaid-ecid-adc.md)
