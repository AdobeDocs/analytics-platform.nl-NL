---
title: De opmerkingen bij de huidige release van de Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste release Customer Journey Analytics
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 4f228dbe58a9efbe988f274c071c61ec5e36d321
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 1%

---

# Opmerkingen bij de huidige Adobe Customer Journey Analytics-release (juli 2024)

**Laatste update**: 29 juli 2024

Deze releaseopmerkingen hebben betrekking op de periode van 17 juli 2024 tot en met augustus 2024. De versies van Adobe Customer Journey Analytics werken op a [ ononderbroken leveringsmodel ](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [ Het begin van de Uitvoer ](releases.md) | [ Algemene Beschikbaarheid ](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Intelligente Alarm** | Intelligente waarschuwingen zijn nu beschikbaar in de Customer Journey Analytics, zodat u direct op de hoogte kunt worden gesteld wanneer zich abnormale gebeurtenissen in uw gegevens voordoen.<p>U kunt waarschuwingen instellen die moeten worden geactiveerd op basis van afwijkende drempelwaarden, gewijzigde percentages of specifieke gegevenspunten. Het alarm verstrekt korrelige controles die met Anomaly Detection integreren, die teweegbrengen wanneer u hen het meest nodig hebt.</p><p>Het gebruik van intelligente waarschuwingen in de Customer Journey Analytics is bijna hetzelfde als het gebruik van intelligente waarschuwingen in Adobe Analytics. Een belangrijk verschil is dat waarschuwingen per uur niet beschikbaar zijn in de Customer Journey Analytics. Dit verschil is omdat gegevensinvoer voor de diverse soorten gebeurtenisgegevens die kunnen worden opgenomen volledig is na een vertraging, typisch die zich van 3 tot 9 uur voorbij de tijd van de gegevensgebeurtenis uitstrekken.</p><p>(Bijgewerkte documentatiekoppelingen die moeten worden gevolgd)</p><!--<p>[Learn more](/help/analysis-workspace/c-intelligent-alerts/intellligent-alerts.md)</p> --> |  | TBD |
| **montages van de Beheerder om de rekeningen en de plaatsen te controleren die wanneer het uitvoeren van rapporten aan de wolk** worden gebruikt | Een nieuw [ lusje &quot;van montages Admin&quot;in de Manager van Plaatsen ](/help/components/exports/manage-export-locations.md#configure-company-wide-settings-administrators-only) geeft beheerders controle over of de gebruikers rekeningen en plaatsen kunnen tot stand brengen en uitgeven.<p>Deze montages zijn van toepassing wanneer de gebruikers [ de rekeningen van de wolkenuitvoer ](/help/components/exports/cloud-export-accounts.md) vormen en [ de plaatsen van de wolkenuitvoer ](/help/components/exports/cloud-export-locations.md) vormen.</p><p>Beheerders kunnen ook de typen accounts beperken die gebruikers kunnen maken en gebruiken. Tot de accounttypen behoren Google Cloud Platform, Azure RBAC, Amazon S3, AEP Data Landing Zone, Snowflake enzovoort.</p><p>Eerder kon elke gebruiker accounts en locaties maken, bewerken en gebruiken voor elk type account.</p> | vrijdag 11 juli 2024 | zaterdag 19 juli 2024 |
| **Summiere-vlakke Gegevensbronnen** | Staat u toe om tijdreeksgegevens in te brengen die geen persoon identiteitskaart hebben Deze tijdreeksgegevens kunnen worden gebruikt om verschillende gebruiksgevallen te ondersteunen, zoals:<ul><li>Prestatie-indicatoren op hoog niveau presenteren als onderdeel van of naast gegevens op gebeurtenisniveau. Dit kan iets omvatten zoals een datum en één enkele metrische waarde of veelvoudige dimensies en metriek omvatten, zoals reclame indrukken, e-mail opent, reclame uitgaven, kosten van goed verkocht, en meer.</li><li>Het uploaden van doelstellingen of doelstellingen op een dagelijkse, wekelijkse, maandelijkse of driemaandelijkse basis en het plaatsen van deze doelstellingen of doelstellingen tegen gebeurtenis-vlakke metriek helpen visualiseren hoe de metriek tegen de organisatorische doelstellingen of doelstellingen trending.</li></ul><p>(Bijgewerkte documentatiekoppelingen die moeten worden gevolgd)</p> |  | maandag 11 augustus 2024 |
| **Voortgekomen Gebieden - Deduplicate functie** | De [ functie Deduplicate ](/help/data-views/derived-fields/derived-fields.md#deduplicate) in Afgeleide Gebieden helpt u om het tellen van een waarde veelvoudige tijden te verhinderen. |  | donderdag 17 juli 2024 |
| **Geleide Levering van de Analyse voor klanten CJA** | Met een geleide analyse kunnen gebruikers zelf hoogwaardige gegevens en inzichten bedienen over de reis van de klant via geleide workflows, op basis van de kanaalgegevens van de Customer Journey Analytics. <p>De interfunctionele teams, van marketing aan product, kunnen in echt - tijd verbinden om deze rapporten te gebruiken en te begrijpen.</p><p>Er zijn nu maximaal 11 geleide analyseweergaven beschikbaar in CJA-pakketten. [Meer informatie](https://experienceleague.adobe.com/en/docs/analytics-platform/using/guided-analysis/overview)</p> |  | donderdag 17 juli 2024 |
| **de rekeningen en de plaatsen van het Aandeel die voor de uitvoer en de invoer** worden gebruikt | Gebruikers kunnen de accounts en locaties die ze maken nu beschikbaar maken voor alle gebruikers in hun organisatie. Alleen account- en locatie-eigenaars en systeembeheerders kunnen accounts en locaties bewerken en verwijderen. Eerder konden accounts en locaties alleen worden gebruikt door de gebruiker die ze heeft gemaakt. Deze montages zijn beschikbaar wanneer de gebruikers [ de rekeningen van de wolkenuitvoer ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/exports/cloud-export-accounts) vormen en [ de plaatsen van de wolkenuitvoer ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/exports/cloud-export-locations) vormen. | donderdag 12 juni 2024 | zaterdag 19 juli 2024 |
| **de Soorten van het publiek worden gepubliceerd aan een nieuwe &quot;sectie van het publiek&quot;in Experience Platform** | Soorten publiek die vanuit de Customer Journey Analytics worden gepubliceerd, zijn nu beschikbaar in de nieuwe sectie &quot;Soorten publiek&quot; in Adobe Experience Platform.<p>Eerder waren publiek dat vanuit Customer Journey Analytics werd gepubliceerd, beschikbaar in Experience Platform onder de sectie &quot;Segmenten&quot;.</p><p>Deze verbetering biedt de volgende voordelen:</p><ul><li>Het publiek heeft niet langer een vertraging van 1 uur voordat het in het Experience Platform wordt weergegeven; het zijn pas seconden nadat het is gepubliceerd.</li><li>De soorten publiek kunnen in Experience Platform worden gesorteerd door de kolom &quot;Oorsprong&quot;te gebruiken, die de toepassing toont waarvan het publiek oorspronkelijk werd gepubliceerd.</li><li>Met de filter- en sorteeropties in het Experience Platform kunt u sneller het desbetreffende publiek vinden.</li></ul> <p>(Koppeling naar documentatie)</p> |  | TBD |

{style="table-layout:auto"}

## Oplossingen in Customer Journey Analytics

AN-306000; AN-288748; AN-351547; AN-351110

## Belangrijke kennisgevingen voor beheerders van Customers Journey Analytics

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. | | |

{style="table-layout:auto"}

## Gerelateerde bronnen

* [Opmerkingen bij de vorige release van Customer Journey Analytics voor 2024](/help/release-notes/2024.md)
* [ de versienota&#39;s van Adobe Analytics ](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
* [ het stromen toe:voegen-op versienota&#39;s van de Inzameling van Media ](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [ de versienota&#39;s van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html)
* [Documentatieupdates Customer Journey Analytics](/help/release-notes/doc-changes.md)
