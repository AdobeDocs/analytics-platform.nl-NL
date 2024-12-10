---
title: Overzicht van tekenreeksen
description: Overzicht van stitching
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
exl-id: 1c42efac-b3d2-437b-8b0b-9c6fdfed8520
role: Admin
source-git-commit: 4ce1b22cce3416b8a82e5c56e605475ae6c27d88
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# Overzicht van tekenreeksen

>[!NOTE]
>
>U moet het **Uitgezochte** pakket of hoger hebben (voor [ op gebied-gebaseerd het stitching ](fbs.md)) of **Prime** pakket of hoger (voor [ op grafiek-gebaseerd het stitching ](gbs.md)) om de functionaliteit te gebruiken die in deze sectie wordt beschreven. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.

Identiteitsstitching (of eenvoudig, stitching) is een krachtige eigenschap die de geschiktheid van een gebeurtenisdataset voor kanaalanalyse verhoogt. De analyse van het dwars-kanaal is een belangrijkste gebruiksgeval dat de Customer Journey Analytics kan behandelen, toestaand u om rapporten naadloos op veelvoudige datasets van verschillende kanalen te combineren en in werking te stellen, die op een gemeenschappelijke herkennings (persoonID) wordt gebaseerd.

Wanneer u datasets met gelijkaardige persoon IDs combineert, wordt de attributie gedragen over apparaten en kanalen. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Die gebruiker ontmoet een kwestie met hun orde, dan geeft uw team van de klantendienst een vraag om het te helpen oplossen. Met kanaalanalyse, kunt u de gebeurtenissen van het vraagcentrum aan de advertentie toeschrijven die zij oorspronkelijk klikte.

Jammer genoeg, niet alle op gebeurtenis-gebaseerde datasets die deel van uw verbinding in Customer Journey Analytics uitmaken zijn voldoende bevolkt met gegevens om deze attributie uit de doos te steunen. Vooral web-based of mobiel-gebaseerde ervaringsdatasets hebben vaak geen daadwerkelijke informatie van persoonidentiteitskaart beschikbaar over alle gebeurtenissen.

Door middel van tekenreeksen kunnen identiteiten binnen rijen van één gegevensset opnieuw worden ingesteld, zodat de persoon-id (naastgelegen ID) voor elke gebeurtenis beschikbaar is. Bij het zoeken naar gebruikersgegevens van zowel geverifieerde als niet-geverifieerde sessies wordt de gemeenschappelijke waarde van de tijdelijke id (de persoon-id) bepaald die kan worden gebruikt als een vergrendelde id. Door dit opnieuw activeren kunnen afwijkende records worden omgezet in één naadloze id voor analyse op persoonlijke niveau in plaats van op apparaat- of cookieniveau.

De Customer Journey Analytics steunt twee soorten het stitching: [ op gebied-gebaseerde het stitching ](fbs.md) en [ op grafiek-gebaseerde het stitching ](gbs.md).

## Vereisten

>[!IMPORTANT]
>
>Als niet aan alle voorwaarden wordt voldaan, kan de analyse van meerdere kanalen niet correct worden uitgevoerd.

Voordat u stitching gebruikt, moet u ervoor zorgen dat uw organisatie is voorbereid met het volgende:

- Onder andere het samenvoegen van geverifieerde en niet-geverifieerde gebruikersgegevens wordt opgenomen. Zorg ervoor dat u aan de toepasselijke wetten en verordeningen, met inbegrip van het verkrijgen van noodzakelijke eindgebruikertoestemmingen voldoet, alvorens het stitching op een gebeurtenisdataset te activeren. Zie [ identiteitsgebieden in UI ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity) voor meer informatie bepalen.

- Importeer de gewenste gegevens naar Adobe Experience Platform:

   - Voor de gegevens van Adobe Analytics, zie [ Gebruikend de gegevens van de het rapportreeks van Adobe Analytics in Customer Journey Analytics ](/help/getting-started/aa-vs-cja/aa-data-in-cja.md).
   - Voor andere soorten gegevens, zie [ een schema ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui) en [ Samenvatting gegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home) in de documentatie van Adobe Experience Platform creëren.

U profiteert van kanaalanalyse als u één of meerdere van uw gestikte datasets met andere datasets, zoals de gegevens van het vraagcentrum, als deel van het bepalen van uw verbinding van de Customer Journey Analytics combineert. Deze verbindingsconfiguratie veronderstelt dat die andere datasets reeds een persoonsidentiteitskaart op elke rij, gelijkend op vastgemaakte identiteitskaart bevatten.


## Beperkingen

>[!IMPORTANT]
>
>- Geen ondersteuning voor het gebruik van `identityMap` als permanente id. U moet een specifieke id in de gegevensset (bijvoorbeeld `ECID` ) definiëren als de permanente id.
>
>- Pas om het even welke verandering toe die u aan het schema van de brongebeurtenisdataset ook aan het nieuwe gestikte datasetschema aanbrengt, anders breekt het de gestikte dataset.
>
>- Als u de brondataset verwijdert, stopt de gestikte dataset verwerking en wordt verwijderd door het systeem.
>
>- De etiketten van het gebruik van gegevens worden niet automatisch verspreid aan het gestikte datasetschema. Als u de etiketten van het gegevensgebruik hebt die op het schema van de brondataset worden toegepast, moet u deze etiketten van het gegevensgebruik manueel op het gestikte datasetschema toepassen. Zie [ het Leiden de etiketten van het gegevensgebruik in Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview) voor meer informatie.

Stikken is een baanbrekende en robuuste functie, maar heeft beperkingen op de manier waarop het kan worden gebruikt.

- Alleen gegevenssets voor gebeurtenissen worden ondersteund. Andere datasets, zoals raadplegingsdatasets, worden niet gesteund.
- Bij het aanbrengen van een stift wordt het veld dat voor stitching wordt gebruikt, op geen enkele wijze getransformeerd. Bij het aanbrengen van tekenreeksen wordt de waarde in het opgegeven veld gebruikt zoals deze bestaat in de ongeordende gegevensset in het gegevensmeer.
- Het stitching proces is case-sensitive. Als bijvoorbeeld soms het woord &#39;Bob&#39; in het veld wordt weergegeven en soms het woord &#39;BOB&#39; wordt weergegeven, worden deze id&#39;s behandeld als twee aparte personen.

Zorg ervoor dat u het stikken niet verwart met:

- De samenvoeging van twee of meer datasets. Stitching is slechts op één dataset van toepassing. Het samenvoegen van datasets vindt plaats als resultaat van vestiging een verbinding van de Customer Journey Analytics en het selecteren van zelfde persoonsidentiteitskaart over de geselecteerde datasets in de verbinding.

- De verbinding van twee datasets. In Customer Journey Analytics, wordt een verbinding vaak gebruikt voor raadplegingen of classificaties in Analysis Workspace. Hoewel het stitching gebruikmaakt verbind zich aan functionaliteit, impliceert het proces zelf meer dan verbindingen.

>[!MORELIKETHIS]
>
>[ Op gebied gebaseerde het stitching ](fbs.md)
>[Op grafiek gebaseerde stitching ](gbs.md)
>[Sstitching gebruiken ](use-stitching.md)
>[Veelgestelde vragen over stitching ](faq.md)

