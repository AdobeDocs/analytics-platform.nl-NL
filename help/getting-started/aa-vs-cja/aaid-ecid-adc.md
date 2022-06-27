---
source-git-commit: f97439676c61acf1b6ba8818ef1d06542402e675
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---
# STEUN, ECID, AACUSTOMID en de Analytics Source Connector

Adobe Analytics-gegevens bevatten meerdere identiteitsvelden. Drie belangrijke identiteitsvelden worden door de [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en):

* **STEUN** is de primaire apparaat-id in Adobe Analytics en is gegarandeerd aanwezig op elke gebeurtenis die wordt doorgegeven via de Analytics Source Connector. AID wordt soms ook wel de &#39;verouderde analyse-id&#39; of de &#39;s\_vi cookie-id&#39; genoemd, maar er wordt ook een AID gemaakt, zelfs als het s\_vi cookie niet aanwezig is. STEUN wordt vertegenwoordigd door de **_post\_visid\_high/post\_visid\_low_** kolommen in [Adobe Analytics-gegevensfeeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=en#columns%2C-descriptions%2C-and-data-types). In de Analytics Source Connector wordt de HULP getransformeerd naar **HEX(post_visid_high) + &quot;-&quot; + HEX(host_visid_low)**. Het veld STEUN voor een bepaalde gebeurtenis bevat één identiteit die een van de verschillende typen kan zijn, zoals beschreven in [Bewerkingsvolgorde voor analytische id&#39;s](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/analytics-order-of-operations.html?lang=en%5B%5D). (Binnen een volledige rapportreeks, kan AID een mengeling van types over gebeurtenissen bevatten. Het type voor elke treffer wordt aangegeven in de **_[post\_]visid\_type_** kolom in Analytics-gegevensfeeds.) Zie ook: [Referentie gegevenskolom](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=en).
* **ECID** (Experience Cloud-id), ook wel MCID (Marketing Cloud-id) genoemd, is een apart veld voor de apparaat-id dat in Adobe Analytics wordt ingevuld wanneer Adobe Analytics wordt geïmplementeerd met behulp van de [Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=en). ECID wordt vertegenwoordigd door de **_mcvisid_** kolom in Adobe Analytics-gegevensfeeds. Als er een ECID bestaat voor een gebeurtenis, kan de STEUN gebaseerd zijn op ECID, afhankelijk van of de Analytics [respijtperiode](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/grace-period.html?lang=en) is geconfigureerd. Zie ook: [Analyses en Experience Cloud-id-verzoeken](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/legacy-analytics.html?lang=en).
* **AACUSTOMID** is een afzonderlijk identifier-veld dat in Adobe Analytics wordt ingevuld op basis van het gebruik van de variabele s.VisitorID in de analytische implementatie. AACUSTOMID wordt vertegenwoordigd door de **_cust_visid_** kolom in Adobe Analytics-gegevensfeeds. Als AACUSTOMID aanwezig is, wordt de STEUN gebaseerd op AACUSTOMID. (AACUSTOMID retourneert alle andere id&#39;s zoals gedefinieerd in de bovenstaande volgorde van bewerkingen.)

De verbinding van de Bron van Analytics gaat door deze identiteiten aan AEP in vorm XDM als:

* endUserIDs.\_experience.id.id
* endUserIDs.\_experience.mcid.id
* endUserIDs.\_experience.accustomid.id

Deze velden zijn niet gemarkeerd als identiteiten. In plaats daarvan worden dezelfde identiteiten gekopieerd naar XDM&#39;s **_identityMap_** als sleutelwaardeparen, als volgt:

* { &quot;key&quot;: &quot;AID&quot;, &quot;value&quot;: [ { &quot;id&quot;: &quot;**_\&lt;identity>_**&quot;, &quot;primair&quot;: **_\&lt;true or=&quot;&quot; false=&quot;&quot;>_**} ] }
* { &quot;key&quot;: &quot;ECID&quot;, &quot;value&quot;: [ { &quot;id&quot;: &quot;**_\&lt;identity>_**&quot;, &quot;primair&quot;: **_\&lt;true or=&quot;&quot; false=&quot;&quot;>_** } ] }
* { &quot;key&quot;: &quot;AACUSTOMID&quot;, &quot;value&quot;: [ { &quot;id&quot;: &quot;**_\&lt;identity>_**&quot;, &quot;primair&quot;: **false** } ] }

Binnen identityMap:

* Als ECID aanwezig is, wordt deze gemarkeerd als de primaire identiteit voor de gebeurtenis. In dit geval kan steun gebaseerd zijn op ECID volgens de bovenstaande beschrijving.
Anders wordt STEUN gemarkeerd als de primaire identiteit voor de gebeurtenis.
* AACUSTOMID is nooit gemarkeerd als primaire id voor de gebeurtenis. Als AACUSTOMID echter aanwezig is, is de steun gebaseerd op AACUSTOMID, zoals in de bovenstaande beschrijving wordt uiteengezet.

Wat CJA betreft, is de definitie van primaire id alleen van belang als de eindgebruiker besluit de primaire id te gebruiken als de persoon-id. Dat is echter niet verplicht. De gebruiker kan een andere identiteitskolom kiezen als Persoon-id.

