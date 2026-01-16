---
title: Overzicht van tekenreeksen
description: Overzicht van stitching
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
exl-id: 1c42efac-b3d2-437b-8b0b-9c6fdfed8520
role: Admin
source-git-commit: d117ba255151f730e0b5e4958ee56f5ffc88ade9
workflow-type: tm+mt
source-wordcount: '902'
ht-degree: 0%

---

# Overzicht van tekenreeksen

>[!NOTE]
>
>U moet het **Uitgezochte** pakket of hoger hebben (voor [&#x200B; op gebied-gebaseerd het stitching &#x200B;](fbs.md)) of **Prime** pakket of hoger (voor [&#x200B; op grafiek-gebaseerd het stitching &#x200B;](gbs.md)) om de functionaliteit te gebruiken die in deze sectie wordt beschreven. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.

Identiteitsstitching (of eenvoudig, stitching) is een krachtige eigenschap die de geschiktheid van een gebeurtenisdataset voor kanaalanalyse verhoogt. Kanaaloverschrijdende analyse is een belangrijk gebruiksgeval voor Customer Journey Analytics. De eigenschap staat u toe om rapporten naadloos op veelvoudige datasets van verschillende kanalen te combineren en in werking te stellen, die op een gemeenschappelijke herkenningsteken (persoonsidentiteitskaart) worden gebaseerd.

Wanneer u datasets met gelijkaardige persoon IDs combineert, wordt de attributie gedragen over apparaten en kanalen. Een gebruiker bezoekt bijvoorbeeld uw site via een advertentie op zijn desktopcomputer. De gebruikers kopen een product maar dan ontmoet de gebruiker een kwestie met de orde. De gebruiker geeft dan uw team van de klantendienst een vraag om de kwestie te helpen oplossen. Met kanaalanalyse, kunt u de gebeurtenissen van het vraagcentrum aan de advertentie toeschrijven die de gebruiker oorspronkelijk klikte.

Helaas zijn niet alle gegevenssets die op gebeurtenissen zijn gebaseerd en die deel uitmaken van uw verbinding in Customer Journey Analytics, voldoende gevuld met gegevens die deze toewijzing uit het vak ondersteunen. Vooral web-based of mobiel-gebaseerde ervaringsdatasets hebben vaak geen daadwerkelijke informatie van identiteitskaart van de persoon beschikbaar over alle gebeurtenissen.

Door middel van plaatsing kunnen identiteiten binnen rijen van één gegevensset opnieuw worden ingesteld, zodat de persoon-id (naastgelegen ID) voor elke gebeurtenis beschikbaar is. Bij het zoeken naar gebruikersgegevens van zowel geverifieerde als niet-geverifieerde sessies wordt de gemeenschappelijke ID-waarde van de persoon bepaald die kan worden gebruikt als aangesloten id. Door dit opnieuw genereren kunnen afwijkende records worden omgezet in één naastgelegen id die kan worden geanalyseerd op het niveau van de persoon in plaats van op het apparaat of cookie.

Customer Journey Analytics steunt twee soorten het stitching: [&#x200B; op gebied-gebaseerde het stitching &#x200B;](fbs.md) en [&#x200B; op grafiek-gebaseerde het stitching &#x200B;](gbs.md).

## Vereisten

>[!IMPORTANT]
>
>Als niet aan alle voorwaarden wordt voldaan, kan de analyse van meerdere kanalen niet correct worden uitgevoerd.

Voordat u stitching gebruikt, moet u ervoor zorgen dat uw organisatie is voorbereid met het volgende:

- Onder andere het samenvoegen van geverifieerde en niet-geverifieerde gebruikersgegevens wordt opgenomen. Zorg ervoor dat u aan de toepasselijke wetten en verordeningen, met inbegrip van het verkrijgen van noodzakelijke eindgebruikertoestemmingen voldoet, alvorens het stitching op een gebeurtenisdataset te activeren. Zie [&#x200B; identiteitsgebieden in UI &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity) voor meer informatie bepalen.

- Importeer de gewenste gegevens naar Adobe Experience Platform:

   - Voor de gegevens van Adobe Analytics, zie [&#x200B; Gebruikend de gegevens van de het rapportreeks van Adobe Analytics in Customer Journey Analytics &#x200B;](/help/getting-started/aa-vs-cja/aa-data-in-cja.md).
   - Voor andere soorten gegevens, zie [&#x200B; een schema &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui) en [&#x200B; Samenvatting gegevens &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home) in de documentatie van Adobe Experience Platform creëren.

U profiteert van kanaalanalyse als u een of meer van uw gestikte datasets met andere datasets, zoals de gegevens van het vraagcentrum, als deel van het bepalen van uw verbinding van Customer Journey Analytics combineert. Deze verbindingsconfiguratie veronderstelt dat die andere datasets reeds een persoonsidentiteitskaart op elke rij, gelijkend op vastgemaakte identiteitskaart bevatten.

## Sstitching inschakelen

U kunt stitching op twee manieren inschakelen:

- [&#x200B; Verzoek om het stitching &#x200B;](/help/stitching/use-stitching.md) toe te laten. Zodra goedgekeurd, wordt een dubbele dataset gecreeerd voor de dataset waarvoor u het stitching hebt gevraagd. Deze dubbele dataset bevat een extra kolom met het gestikte herkenningsteken. U moet een nieuwe verbinding tot stand brengen of een bestaande verbinding uitgeven die de gestikte dataset omvat om de gestikte gegevens in Customer Journey Analytics te gebruiken.
- [&#x200B; laat het stikken in de interface van Verbindingen &#x200B;](/help/stitching/use-stitching-ui.md) [!BADGE &#x200B; Beta &#x200B;]{type=Informative} toe. Wanneer u het stitching voor een dataset in de interface van Verbindingen vormt, komt het stiching &quot;op de vlucht&quot;voor, tijdens de opname van gegevens van die dataset in Customer Journey Analytics.

## Beperkingen

>[!IMPORTANT]
>
>
>- Pas om het even welke verandering toe die u aan het schema van de brongebeurtenisdataset ook aan het nieuwe gestikte datasetschema aanbrengt.
>
>- Als u de brondataset verwijdert, stopt de gestikte dataset verwerking en wordt verwijderd door het systeem.
>
>- De etiketten van het gebruik van gegevens worden niet automatisch verspreid aan het gestikte datasetschema. Als u de etiketten van het gegevensgebruik hebt die op het schema van de brondataset worden toegepast, moet u deze etiketten van het gegevensgebruik manueel op het gestikte datasetschema toepassen. Zie [&#x200B; het Leiden de etiketten van het gegevensgebruik in Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview) voor meer informatie.

Stikken is een baanbrekende en robuuste functie, maar heeft beperkingen op de manier waarop het kan worden gebruikt.

- Alleen gegevenssets voor gebeurtenissen worden ondersteund. Andere datasets, zoals raadplegingsdatasets, worden niet gesteund.
- Bij het aanbrengen van een stift wordt het veld dat voor stitching wordt gebruikt, op geen enkele wijze getransformeerd. Bij het aanbrengen van tekenreeksen wordt de waarde in het opgegeven veld gebruikt zoals deze bestaat in de ongeordende gegevensset in het gegevensmeer.
- Het stitching proces is case-sensitive. Als bijvoorbeeld soms het woord &#39;Bob&#39; in het veld wordt weergegeven en soms het woord &#39;BOB&#39; wordt weergegeven, worden deze id&#39;s behandeld als twee aparte personen.

Zorg ervoor dat u het stikken niet verwart met:

- De samenvoeging van twee of meer datasets. Stitching is slechts op één dataset van toepassing. Het samenvoegen van gegevenssets vindt plaats als gevolg van het instellen van een Customer Journey Analytics-verbinding en het selecteren van dezelfde persoon-id in de geselecteerde gegevenssets in de verbinding.

- De verbinding van twee datasets. In Customer Journey Analytics wordt vaak een samenvoeging gebruikt voor zoekopdrachten of classificaties in Analysis Workspace. Hoewel het stitching gebruikmaakt verbind zich aan functionaliteit, impliceert het proces zelf meer dan verbindingen.


## Journey Optimizer-gegevenssets

Het plaatsen steunt de volgende automatisch geproduceerde datasets van Journey Optimizer:

- AJO Journey Step Events
- Gegevensset van gebeurtenis Inbound Activity van AJO
- Gegevensset AJO-oppervlakken
- Gegevensset AJO Message Feedback Event* AJO Push Tracking Experience Event Dataset
- AJO Email Tracking Experience Event Dataset
- Gegevensset voor AJO BCC-feedbackgebeurtenis
- Gegevens over feedbackgebeurtenis AJO Live-activiteiten
- Dataset AJO ExD-beslissingsgebeurtenis

>[!MORELIKETHIS]
>
>[&#x200B; Op gebied-gebaseerde het stitching &#x200B;](fbs.md)
>[Op grafiek gebaseerde stitching &#x200B;](gbs.md)
>[Sstitching gebruiken &#x200B;](use-stitching.md)
>[Sstitching valideren &#x200B;](validate.md)
>[Veelgestelde vragen over stitching &#x200B;](faq.md)

