---
title: Overzicht van titelformaat
description: Leer over de concepten, de voordelen, de eerste vereisten, en de beperkingen van identiteit stitching.
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
exl-id: 1c42efac-b3d2-437b-8b0b-9c6fdfed8520
role: Admin
source-git-commit: d1ba2d203738ca9bf74d17bb93712eff26f88f25
workflow-type: tm+mt
source-wordcount: '982'
ht-degree: 0%

---

# Overzicht van tekenreeksen

>[!NOTE]
>
>U moet het Customer Journey Analytics **Uitgezochte** pakket of hoger hebben (voor [ op gebied-gebaseerd het stitching ](fbs.md)) of het Customer Journey Analytics **Prime** pakket of hoger (voor [ op grafiek-gebaseerd het stitching ](gbs.md)) om de functionaliteit te gebruiken die in deze sectie wordt beschreven. Neem contact op met de beheerder als u niet zeker weet welk Customer Journey Analytics-pakket u hebt.

Identiteitsstitching (of eenvoudig, stitching) is een krachtige eigenschap die de geschiktheid van een gebeurtenisdataset voor kanaalanalyse verhoogt. Kanaaloverschrijdende analyse is een belangrijk gebruiksgeval voor Customer Journey Analytics. De eigenschap staat u toe om rapporten naadloos op veelvoudige datasets van verschillende kanalen te combineren en in werking te stellen, die op een gemeenschappelijke herkenningsteken (persoonsidentiteitskaart) worden gebaseerd.

Wanneer u datasets met gelijkaardige persoon IDs combineert, wordt de attributie gedragen over apparaten en kanalen. Een gebruiker bezoekt bijvoorbeeld uw site via een advertentie op zijn desktopcomputer. De gebruiker koopt een product maar dan ontmoet de gebruiker een kwestie met de orde. De gebruiker geeft dan uw team van de klantendienst een vraag om de kwestie te helpen oplossen. Met kanaalanalyse, kunt u de gebeurtenissen van het vraagcentrum aan de advertentie toeschrijven die de gebruiker oorspronkelijk klikte.

Helaas zijn niet alle gegevenssets die op gebeurtenissen zijn gebaseerd en die deel uitmaken van uw verbinding in Customer Journey Analytics, voldoende gevuld met gegevens die deze toewijzing uit het vak ondersteunen. Vooral web-based of mobiel-gebaseerde ervaringsdatasets hebben vaak geen daadwerkelijke informatie van identiteitskaart van de persoon beschikbaar over alle gebeurtenissen.

Als u de id inschakelt, worden de identiteiten binnen de rijen van een gegevensset herhaald om ervoor te zorgen dat de gewenste personen-id-gegevens beschikbaar zijn voor zoveel mogelijk gebeurtenissen. Bij het zoeken naar gebruikersgegevens in geverifieerde en niet-geverifieerde sessies wordt de gemeenschappelijke ID-waarde van de persoon bepaald die kan worden gebruikt. Dit opnieuw gebruiken verhelpt ongelijke verslagen aan één enkele persoonsidentiteitskaart voor analyse op het persoonniveau, eerder dan op het apparaat of koekjesniveau. Als een gemeenschappelijke ID-waarde echter niet kan worden bepaald, wordt in plaats daarvan de permanente ID-waarde gebruikt.

Customer Journey Analytics steunt twee soorten het stitching: [ op gebied-gebaseerde het stitching ](fbs.md) en [ op grafiek-gebaseerde het stitching ](gbs.md).

## Vereisten

>[!IMPORTANT]
>
>Als niet aan alle voorwaarden wordt voldaan, kan de analyse van meerdere kanalen niet correct worden uitgevoerd.

Voordat u stitching gebruikt, moet u ervoor zorgen dat uw organisatie is voorbereid met het volgende:

- Onder andere het samenvoegen van geverifieerde en niet-geverifieerde gebruikersgegevens wordt opgenomen. Zorg ervoor dat u aan de toepasselijke wetten en verordeningen, met inbegrip van het verkrijgen van noodzakelijke eindgebruikertoestemmingen voldoet, alvorens het stitching op een gebeurtenisdataset te activeren.

- Importeer de gewenste gegevens naar Adobe Experience Platform:

   - Voor de gegevens van Adobe Analytics, zie [ Gebruikend de gegevens van de het rapportreeks van Adobe Analytics in Customer Journey Analytics ](/help/getting-started/aa-vs-cja/aa-data-in-cja.md).
   - Voor andere soorten gegevens, zie [ een schema ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui) en [ Samenvatting gegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home) in de documentatie van Adobe Experience Platform creëren.

U profiteert van kanaalanalyse als u een of meer van uw gestikte datasets met andere datasets, zoals de gegevens van het vraagcentrum, als deel van het bepalen van uw verbinding van Customer Journey Analytics combineert. Deze verbindingsconfiguratie veronderstelt dat die andere datasets reeds een persoonsidentiteitskaart van zelfde namespace op zoveel mogelijk rijen bevatten.

Zodra uw organisatie aan generische [ eerste vereisten ](overview.md#prerequisites) voldoet, begrijpt gemeenschappelijke [ beperkingen ](overview.md#limitations), en ook het stitching van methode specifiek ([ op gebied-gebaseerde ](fbs.md) en [ op grafiek-gebaseerde ](gbs.md)) eerste vereisten en beperkingen, kunt u deze stappen volgen om te verzoeken en te beginnen het stitching in Customer Journey Analytics.

## Beperkingen

Stikken is een baanbrekende en robuuste functie, maar heeft beperkingen op de manier waarop het kan worden gebruikt.

- Alleen gegevenssets voor gebeurtenissen worden ondersteund. Andere datasets, zoals raadplegingsdatasets, worden niet gesteund.
- Bij het aanbrengen van een stift wordt het veld dat voor stitching wordt gebruikt, op geen enkele wijze getransformeerd. Bij het aanbrengen van tekenreeksen wordt de waarde in het opgegeven veld gebruikt zoals deze bestaat in de ongeordende gegevensset in het gegevensmeer.
- Het stitching proces is case-sensitive. Identiteitswaarden `Bob` en `BOB` worden bijvoorbeeld als twee afzonderlijke personen behandeld.

Zorg ervoor dat u het stikken niet verwart met:

- De samenvoeging van twee of meer datasets. Stitching is slechts op één dataset van toepassing. Het samenvoegen van gegevenssets vindt plaats als gevolg van het instellen van een Customer Journey Analytics-verbinding en het selecteren van dezelfde persoon-id in de geselecteerde gegevenssets in de verbinding.

- De verbinding van twee datasets. In Customer Journey Analytics wordt vaak een samenvoeging gebruikt voor zoekopdrachten of classificaties in Analysis Workspace. Hoewel het stitching gebruikmaakt verbind zich aan functionaliteit, impliceert het proces zelf meer dan verbindingen.


## Opties

Het Customer Journey Analytics-pakket waarop u recht hebt, bepaalt de beschikbare tekenreeksmethoden, opties voor de initiële duur van de backfill, het terugzoekvenster, de herhalingsfrequentie en het maximale aantal gegevenssets dat is toegestaan voor stitching. Zie de [ het productbeschrijving van Customer Journey Analytics ](https://helpx.adobe.com/legal/product-descriptions/customer-journey-analytics.html) voor meer details. Bepaal de beschikbare opties voordat u stitching inschakelt.

| | Customer Journey Analytics <br/> Uitgezocht | Customer Journey Analytics <br/> Prime | Customer Journey Analytics <br/> Ultimate |
|---|---|---|---|
| Beschikbare stitmethoden | Veldgebaseerde stitching | Op gebied-gebaseerd het stitching <br/> op grafiek-gebaseerde het stitching | Op gebied-gebaseerd het stitching <br> op grafiek-gebaseerde het stitching</li> |
| Eenmalige duur van de backfill-functie | 13 maanden | 13 maanden | 25 maanden |
| Zoekvenster en herhalingsfrequentie | 1 dag, elke dag <br/> tot 7 dagen, wekelijks | 1 dag, elke dag <br/> tot 14 dagen, wekelijks | 1 dag, elke dag <br/> tot 30 dagen, wekelijks |
| Maximumaantal gegevenssets dat is toegestaan voor stitching | 5 | 15 | 50 |

## Sstitching inschakelen

U kunt stitching op twee manieren inschakelen:

- [ Verzoek om het stitching ](/help/stitching/use-stitching.md) (afgekeurd) toe te laten. Zodra goedgekeurd, wordt een dubbele dataset gecreeerd voor de dataset waarvoor u het stitching hebt gevraagd. Deze dubbele dataset bevat een extra kolom met het gestikte herkenningsteken. U moet een nieuwe verbinding tot stand brengen of een bestaande verbinding uitgeven die de gestikte dataset omvat om de gestikte gegevens in Customer Journey Analytics te gebruiken.
- [ laat het stikken in de interface van Verbindingen ](/help/stitching/use-stitching-ui.md) toe. Wanneer u het stitching voor een dataset in de interface van Verbindingen vormt, komt het stitching op de vlucht, tijdens de opname van gegevens van die dataset in Customer Journey Analytics voor.


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
>[ Op gebied-gebaseerde het stitching ](fbs.md)
>[Op grafiek gebaseerde stitching ](gbs.md)
>[Sstitching gebruiken ](use-stitching.md)
>[Sstitching valideren ](validate.md)
>[Veelgestelde vragen over stitching ](faq.md)

