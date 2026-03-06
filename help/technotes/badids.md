---
title: Ongeldige Customer Journey Analytics-id's
description: Onjuiste id's (BAVID's) in Customer Journey Analytics begrijpen. Leer hoe u onjuiste id's in uw gegevens kunt identificeren, waarom deze van invloed zijn op de rapportage en hoe u de blootstelling aan onjuiste id's in uw verbindingen kunt onderzoeken en oplossen.
solution: Customer Journey Analytics
feature: Basics
role: Admin
source-git-commit: b7b2a1f3eb1c149caf65ab3e4321e4f4347695cc
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---


# Ongeldige id&#39;s

Dit artikel biedt context voor beschadigde id&#39;s en hoe u de aanwezigheid of het risico van een dergelijke id in uw gegevens kunt detecteren met behulp van Query Service.


>[!INFO]
>
>Slechte IDs wordt ook bedoeld als BAVIDs in de interface van Customer Journey Analytics (voortkomend uit [&#x200B; Analytics BAVID &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-cloud-kcs/kbarticles/ka-16444)).
>

## Definitie

In Customer Journey Analytics is een ongeldige id een id als onderdeel van alle gegevens die in een verbinding zijn gedefinieerd:

* met een specifieke id-waarde die begint
   * van een gebied van identiteitskaart van de persoon (niet-gestippelde datasets), **of**
   * van een persistente ID of een persoonsidentiteitskaart veld (stitching-enabled datasets),

  **en**
* is op meer dan één miljoen (1.000.000) gebeurtenissen in de verbindingsgegevens (die voor alle datasets binnen de verbinding worden geteld), binnen een maand.

Wanneer een ID-waarde wordt gemarkeerd als een slechte id, worden toekomstige gebeurtenissen die die id-waarde bevatten, verwijderd uit de verbindingsgegevens en niet weergegeven in de rapportage.

### Voorbeeld

Een voorbeeld van een Slecht scenario IDs is dat u douane of placeholder waarden op het gebied van identiteitskaart van de persoon (bijvoorbeeld, `undefined` voor anoniem verkeer) hebt. Voor een gegevensset met stitching-mogelijkheden kan deze situatie nog grotere gevolgen hebben voor de rapportgegevens, aangezien de kwaliteit van de stitching het meest waarschijnlijk wordt beïnvloed. Om dit op te lossen, zou u de stitching opstelling kunnen moeten ontruimen en re-toelaten, met inbegrip van het schrappen van historische gegevens van datasets in de verbinding.


## Metrics

De Customer Journey Analytics Connection-interface biedt **[!UICONTROL Bad IDs]** metrische informatie op verschillende plaatsen in de interface.

* U ziet **[!UICONTROL Bad IDs]** (of **[!UICONTROL BAVIDs]** ) als mogelijke redenen voor het overslaan van records in het dialoogvenster **[!UICONTROL Check skipped details]** . Gebruik **[!UICONTROL Check detail]** (als beschikbaar) hieronder **[!UICONTROL Records skipped]** in het [&#x200B; detailscherm van een verbinding &#x200B;](/help/connections/create-connection.md).
* Voor een stitching ingeschakelde dataset, [**[!UICONTROL Dataset preview]**](/help/stitching/use-stitching-ui.md#bad-ids) toont **[!UICONTROL Bad IDs]** als deel van **[!UICONTROL Stitching metrics]**. Deze metrisch kan u helpen mogelijke Onjuiste IDs gevallen identificeren. Houd er echter rekening mee dat deze metrische waarde wordt berekend op basis van een beperkte set gegevens.

Verwijs naar [&#x200B; Verkeerde blootstelling IDs &#x200B;](#bad-ids-exposure) om u te helpen slechte aanwezigheid IDs voor een dataset identificeren die u van plan bent om binnen een verbinding (ongeacht als het stitching-toegelaten of niet) te gebruiken.


## Belichting

Om de Blootstelling te onderzoeken Slechte IDs voor een bepaald datasetgebied, denk na uitvoerend de volgende vraag in de Dienst van de Vraag van Experience Platform. Controleer de bovenste geretourneerde ID-waarden om te zien of er mogelijk ongeldige id&#39;s zijn. Ben zich ervan bewust dat de [&#x200B; Onjuiste definitie van identiteitskaart &#x200B;](#definition) rekening houdt met alle datasets binnen de verbinding.


### Identificeer (risico van) Beschadigde IDs binnen een gebied

U kunt Experience Platform Query gebruiken voor service om het potentiële risico van beschadigde id&#39;s in een veld te identificeren.

Met de onderstaande query worden de eerste 20 ID-waarden uit een veld geretourneerd. In aflopende volgorde op basis van het aantal gebeurtenissen in totaal. En waar elke waarde binnen een bepaald interval wordt ontdekt (bijvoorbeeld binnen de laatste 30 dagen).

Voer deze query uit voor een specifiek veld met de persoon-id dat u wilt analyseren. Voor een dataset die het stitching vereist, kunt u de vraag voor een blijvend gebied van identiteitskaart ook in werking stellen.

```sql
SELECT
    /* INSERT FIELD HERE */,
    COUNT(*) AS occurrences
FROM /* INSERT DATASET TABLE NAME HERE */
WHERE timestamp >= NOW() - INTERVAL '30 days' 
GROUP BY /* INSERT FIELD HERE */
ORDER BY occurrences DESC
LIMIT 20; 
```

Vervang `INSERT FIELD HERE` in de query, afhankelijk van het type veld dat u controleert op onjuiste id&#39;s:

* `full.field.path.from.XDM.schema` (voor tekenreeksvelden die zijn gedefinieerd in XDM-schema)
* `identityMap['namespace_value'][0].id` (voor velden die zijn gedefinieerd met `namespace_value` in `identityMap` )

Controleer de resultaten om te zien of er problematische waarden van identiteitskaart zijn. Als douane of placeholder waarden, of waarden met hoog voorkomen die binnen een maand dicht bij 1 miljoen op het niveau van verbindingsgegevens krijgen of kunnen krijgen.
Zelfs als uw implementatie zich nog in de ontwikkelingsfase bevindt, zou u het risico van slechte aanwezigheid moeten beoordelen IDs zodra de opstelling stabiel en klaar voor productie is.
