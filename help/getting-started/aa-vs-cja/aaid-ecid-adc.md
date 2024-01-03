---
title: STEUN, ECID, AACUSTOMID en de bronaansluiting voor Analytics
description: Leer hoe de Analytics-bronconnector werkt met Adobe Analytics-identiteitsvelden.
exl-id: c983cf50-0b6c-4daf-86a8-bcd6c01628f7
feature: Basics
role: User
source-git-commit: 811fce4f056a6280081901e484c3af8209f87c06
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# STEUN, ECID, AACUSTOMID en de bronaansluiting voor Analytics

Adobe Analytics-gegevens bevatten meerdere identiteitsvelden. Drie belangrijke identiteitsvelden worden door de [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en): STEUN, ECID, AACUSTOMID.

## STEUN

Adobe Analytics ID (AID) is de primaire apparaat-id in Adobe Analytics en is gegarandeerd aanwezig op elke gebeurtenis die via de Analytics-bronconnector wordt doorgegeven. AID wordt ook wel &quot;verouderde analysetoewijzing-id&quot; genoemd of `s_vi` cookie-id. Er wordt echter wel een STEUN ingesteld, zelfs als de `s_vi` cookie is niet aanwezig. STEUN wordt vertegenwoordigd door de `post_visid_high/post_visid_low` kolommen in [Adobe Analytics-gegevensfeeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=en#columns%2C-descriptions%2C-and-data-types).

In de bronconnector Analytics wordt AID omgezet in `HEX(post_visid_high) + "-" + HEX(post_visid_low)`. Het veld STEUN voor een bepaalde gebeurtenis bevat één identiteit die een van de verschillende typen kan zijn, zoals beschreven in [Bewerkingsvolgorde voor analytische id&#39;s](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/analytics-order-of-operations.html?lang=en%5B%5D). (Binnen een volledige rapportreeks, kan AID een mengeling van types over gebeurtenissen bevatten. Het type voor elke gebeurtenis wordt aangegeven in het dialoogvenster `post_visid_type` kolom in Gegevensdoorvoer Analytics.) Zie ook: [Referentie gegevenskolom](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=en).

## ECID

ECID (Experience Cloud-id), ook wel MCID (Marketing Cloud-id) genoemd, is een apart veld voor de apparaat-id dat in Adobe Analytics wordt ingevuld wanneer Analytics wordt geïmplementeerd met behulp van de [Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=en). ECID wordt vertegenwoordigd door de `mcvisid` kolom in Adobe Analytics-gegevensfeeds.

Als er een ECID bestaat voor een gebeurtenis, kan de STEUN gebaseerd zijn op ECID, afhankelijk van of de Analytics [respijtperiode](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/grace-period.html?lang=en) is geconfigureerd. Zie ook: [Verzoeken voor analyse en Experience Cloud-id](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/legacy-analytics.html?lang=en).

## AACUSTOMID

AACUSTOMID is een apart veld voor id dat in Adobe Analytics wordt ingevuld op basis van het gebruik van de `s.VisitorID` in de analytische implementatie. AACUSTOMID wordt vertegenwoordigd door de `cust_visid` kolom in Adobe Analytics-gegevensfeeds. Als AACUSTOMID aanwezig is, wordt de STEUN gebaseerd op AACUSTOMID. (AACUSTOMID retourneert alle andere id&#39;s zoals gedefinieerd in de bovenstaande volgorde van bewerkingen.)

## Hoe de bronschakelaar van de Analyse deze identiteiten behandelt

De bronschakelaar van Analytics geeft deze identiteiten door aan Adobe Experience Platform in XDM vorm als:

* `endUserIDs._experience.aaid.id`
* `endUserIDs._experience.mcid.id`
* `endUserIDs._experience.aacustomid.id`

Deze velden zijn niet gemarkeerd als identiteiten. In plaats daarvan worden dezelfde identiteiten gekopieerd naar XDM&#39;s **_identityMap_** als sleutelwaardeparen, als volgt:

* `{ "key": "AAID", "value": [ { "id": "<identity>", "primary": <true or false> } ] }`
* `{ "key": "ECID", "value": [ { "id": "<identity>", "primary": <true or false> } ] }`
* `{ "key": "AACUSTOMID", "value": [ { "id": "<identity>", "primary": false } ] }`

De items tussen haakjes &lt;> geven plaatsen aan waar werkelijke waarden worden weergegeven.

Binnen identityMap:

* Als ECID aanwezig is, wordt deze gemarkeerd als de primaire identiteit voor de gebeurtenis. In dit geval kan steun gebaseerd zijn op ECID volgens de bovenstaande beschrijving.
Anders wordt STEUN gemarkeerd als de primaire identiteit voor de gebeurtenis.
* AACUSTOMID is nooit gemarkeerd als primaire id voor de gebeurtenis. Als AACUSTOMID echter aanwezig is, is STEUN gebaseerd op AACUSTOMID zoals in de bovenstaande beschrijving wordt beschreven.

## Customer Journey Analytics en primaire id

Wat de Customer Journey Analytics betreft, is de definitie van primaire id alleen belangrijk als u besluit de primaire id te gebruiken als de persoon-id. Dat is echter niet verplicht. U kunt een andere identiteitskolom kiezen als Persoon-id.
