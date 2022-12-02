---
title: Adobe Analytics-rapportenpakket-gegevens gebruiken in Customer Journey Analytics
description: Hoe te om Adobe Analytics rapportsuites voor opname in AEP en CJA te vormen
role: User
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: 292109fe4aa148b91ae10f6a9f143ba70dd0c813
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 1%

---


# Adobe Analytics-rapportenpakket-gegevens gebruiken in Customer Journey Analytics

Adobe Analytics-klanten kunnen hun rapportsuites in de Adobe Experience Platform en Customer Journey Analytics eenvoudig benutten met behulp van de [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=en). Hieronder wordt uitgelegd hoe u dit doet.

## Voorbereiding

Aangezien u klaar bent om Adobe Analytics te gaan gebruiken rapportsuites in AEP en CJA, zijn er verscheidene dingen u zou moeten doen om uw gegevens voor een naadloze beweging aan Customer Journey Analytics voor te bereiden. Lees de volgende pagina voor meer informatie:

* [Adobe Analytics naar Customer Journey Analytics evolutie](/help/getting-started/aa-to-cja.md)

## Rapportsuites instellen voor opname in de Adobe Experience Platform en CJA

Zodra u uw gegevens hebt voorbereid, bent u klaar om rapportreeksen voor gebruik in AEP en CJA te vormen.

1. **Maak een gegevensstroom voor elke rapportsuite die u in AEP en CJA wilt gebruiken.** De [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=en) is het gereedschap waarmee u [een verbinding maken](/help/connections/create-connection.md) (ook bekend als dataflow) tussen Adobe Analytics en AEP. U zult de bronschakelaar gebruiken om één dataflow voor elke rapportreeks tot stand te brengen u in AEP wilt gebruiken. De dataflow leidt tot een exemplaar van uw gegevens van de rapportreeks waar het schema is omgezet in  [XDM](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/schemas-and-experience-data-model.html?lang=nl) voor gebruik door AEP-toepassingen, met inbegrip van CJA. Elke rapportreeks die met een dataflow via de bronschakelaar wordt gevormd wordt opgeslagen als afzonderlijke dataset in het meer van Gegevens AEP. 13 maanden historische gegevens uit de rapportsuite worden automatisch bij elke gegevensstroom opgenomen en nieuwe gegevens worden doorlopend in AEP ingevoerd. Met de Bron van Analytics Schakelaar moet u zich geen zorgen maken over het creëren van het schema voortijdig. Er wordt automatisch een gestandaardiseerd schema voor Adobe Analytics gemaakt. De [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html?lang=en) kan worden gebruikt om dit schema te verbeteren voordat de gegevens in het Datameer worden opgeslagen en ter beschikking van CJA worden gesteld. Houd er rekening mee dat bepaalde soorten gegevens door de bronaansluiting worden uitgefilterd en niet aanwezig zijn in de gegevensset in het gegevensmeer van AEP. Andere rijen kunnen worden uitgefilterd tussen Data Lake en CJA. Zie [Adobe Analytics-gegevens vergelijken met CJA-gegevens](/help/troubleshooting/compare.md) voor meer informatie .
1. **Met Data Prep kunt u rapportsuites in CJA combineren.** Data Prep kan voor vele soorten gegevenstransformatie worden gebruikt, en één gemeenschappelijk gebruik voor de gegevens van Adobe Analytics is om verschillen in steun en/of eVar in afbeeldingen over veelvoudige rapportreeksen op te lossen zodat de rapportreeksen gemakkelijk binnen CJA kunnen worden gecombineerd. Zie [rapportsuites combineren met verschillende schema&#39;s](/help/use-cases/combine-report-suites.md) voor meer informatie .
1. **Kanaaloverschrijdende analyse inschakelen** indien nodig. Wanneer het combineren van veelvoudige datasets in CJA, kunnen de identiteit het stitching mogelijkheden van de Analytics van het Kanaal helpen verschillende identiteitskaart namespaces in één enkele SstitchedID voor één enkele mening van de klant over apparaten en kanalen oplossen. Zie [Overzicht van kanaalanalyse](/help/connections/cca/overview.md) voor meer informatie .
1. **Maak een of meer CJA-verbindingen.** Zodra de datasets voor uw rapportreeksen in het meer van Gegevens AEP beschikbaar zijn, kunt u één of meerdere tot stand brengen [CJA-verbindingen](/help/connections/overview.md) om die gegevensreeksen in CJA op te nemen. Binnen een verbinding, kunnen de gegevens van de rapportreeks met andere soorten gegevens worden gecombineerd, die u toestaan om een ware dwars-kanaalmening van klantenervaringen tot stand te brengen.
1. **Maak een of meer CJA-gegevensweergaven.** A [gegevensweergave](/help/data-views/data-views.md) is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van een verbinding te interpreteren CJA. Gegevensweergaven hebben veel kracht [configuratieopties](/help/data-views/create-dataview.md) voor het aanpassen van de gegevens die binnen aan uw gebruikers worden voorgesteld [Analysis Workspace](/help/analysis-workspace/home.md).

## Customer Journey Analytics en Adobe Analytics vergelijken

Customer Journey Analytics en Adobe Analytics hebben een aantal overeenkomsten. Zowel CJA als Adobe Analytics bieden bijvoorbeeld de kracht van Analysis Workspace voor een snelle analyse van de vrije vorm. Omdat CJA echter een toepassing is binnen de Adobe Experience Platform en AEP gebruikt voor gegevensinvoer, verschillen CJA en Adobe Analytics op een aantal belangrijke manieren. De volgende artikelen zijn nuttig om deze verschillen te begrijpen:

* [Adobe Analytics-gegevens vergelijken met CJA-gegevens](/help/troubleshooting/compare.md)
* [Ondersteuning voor Customer Journey Analytics-functies](/help/getting-started/aa-vs-cja/cja-aa.md)
* [Vergelijk terminologie voor de gegevens van de Analyse die door de Bronschakelaar van de Analyse worden overgegaan](/help/getting-started/aa-vs-cja/terminology.md)
* [Gegevensverwerking vergelijken in Adobe Analytics en CJA-rapportagefuncties](/help/getting-started/aa-vs-cja/data-processing-comparisons.md)
* [Virtuele rapportsuite, gegevensweergaven, AEP-sandboxen en de Bronverbinding voor analyse](/help/getting-started/aa-vs-cja/vrs-dataview-sandbox-adc.md)
* [Verwerkingsregels, VISTA en classificaties versus Data Prep](/help/getting-started/aa-vs-cja/pr-vista-dataprep.md)
* [STEUN, ECID, AACUSTOMID en de Analytics Source Connector](/help/getting-started/aa-vs-cja/aaid-ecid-adc.md)
