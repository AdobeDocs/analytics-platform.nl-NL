---
title: Analytics Source Connector-gegevens vergelijken met Adobe Analytics
description: Verschillen in gegevens begrijpen bij het bekijken van vergelijkbare rapporten in Adobe Analytics en Customer Journey Analytics.
role: Developer, Admin
solution: Customer Journey Analytics
exl-id: dd273c71-fb5b-459f-b593-1aa5f3e897d2
feature: Troubleshooting
keywords: queryservice;Query-service;sql-syntaxis
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 0%

---

# Analytics Source Connector-gegevens vergelijken met Adobe Analytics

Aangezien uw organisatie Customer Journey Analytics goedkeurt, is het mogelijk om sommige verschillen in gegevens tussen Adobe Analytics en Customer Journey Analytics op te merken. Deze verschillen zijn normaal en kunnen om verschillende redenen voorkomen. Customer Journey Analytics is ontworpen om u in staat te stellen een aantal van de beperkingen van uw gegevens in Adobe Analytics te verhelpen. Deze flexibiliteit kan enige verschillen veroorzaken in de manier waarop Customer Journey Analytics gegevens interpreteert. In dit artikel wordt uitgelegd welke verschillen er zijn in de manier waarop Customer Journey Analytics en Adobe Analytics omgaan met uw gegevens.

Deze pagina veronderstelt dat u de gegevens van Adobe Analytics in Adobe Experience Platform gebruikend de [ Bron van Analytics schakelaar ](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html), dan creeerde a [ verbinding ](/help/connections/overview.md) en [ gegevensmening ](/help/data-views/data-views.md) in Customer Journey Analytics.

![ de gegevensstroom van Adobe Analytics door de gegevensschakelaar aan Adobe Experience Platform en aan de Analyse van de Reis van de Klant gebruikend de verbindingen van CJA.](assets/compare.png)

Houd rekening met de volgende mogelijke redenen waarom gegevens kunnen verschillen tussen rapportageplatforms:

* **Verschillende datasets of rapportreeksen**: Zorg ervoor dat de rapportreeks in Adobe Analytics en de rapportreeks die de Schakelaar van Source gegevens voortbrengt het zelfde zijn.
* **de montages van de Kalender**: De reeksen van het rapport in Adobe Analytics bevatten een tijdzone en andere kalendermontages die u kunt vormen. Op dezelfde manier hebben gegevensweergaven in Customer Journey Analytics een aparte instelling die u kunt beheren. Zorg ervoor dat deze instellingen overeenkomen tussen producten als pariteit gewenst is.
* **Extra datasets**: Customer Journey Analytics verstrekt het vermogen om veelvoudige datasets binnen één enkele verbinding te omvatten. Deze verschillen omvatten extra gebeurtenisdatasets, profieldatasets, of raadplegingsdatasets. Deze mogelijkheid is een belangrijk verschil tussen Adobe Analytics en Customer Journey Analytics, waardoor insight gegevens over meerdere kanalen kan verwerken.
* **Gestitched datasets**: Adobe verstrekt de capaciteit om persoon IDs tussen twee datasets te analyseren, resulterend in een nieuwe dataset die verbonden IDs bevat. Deze [ verbonden datasets ](/help/stitching/overview.md) bevatten extra gegevens voorbij wat een het rapportreeks van Adobe Analytics aanbiedt.
* **Gegevensbronnen**: Customer Journey Analytics omvat geen type van [ Gegevensbronnen ](https://experienceleague.adobe.com/en/docs/analytics/import/data-sources/overview) geupload aan een het rapportreeks van Adobe Analytics, met inbegrip van summiere gegevensbronnen of de gegevensbronnen van transactieID.
* **Dimension en metrische montages**: Binnen een gegevensmening, bevat elke afmeting en metrisch zijn eigen montages die uw organisatie kan veranderen. Deze wijzigingen zijn van toepassing op het moment waarop het verslag wordt uitgevoerd en worden dus met terugwerkende kracht toegepast. De Dimension- en metrische instellingen in Adobe Analytics wijzigen de manier waarop gegevens worden verzameld, zodat deze wijzigingen van toepassing zijn vanaf dat punt. Als u de componentinstellingen in een van beide producten hebt gewijzigd, kunnen er rapportverschillen ontstaan. Als u zich richt op een specifieke dimensie, moet u ervoor zorgen dat de attributie- en persistentie-instellingen overeenkomen tussen Adobe Analytics en Customer Journey Analytics.

  >[!TIP]
  >
  >Adobe adviseert hoogst dat de dimensies in Adobe Analytics een toewijzing van &quot;[!UICONTROL Most recent (last)]&quot;gebruiken. Deze toewijzingsinstelling maakt veel meer toewijzingsflexibiliteit in Customer Journey Analytics mogelijk.

* **de definitie van het Bezoek**: Naast individuele afmeting en metrische montages, bevat de gegevensmening zelf montages die fundamenteel veranderen hoe de videogegevens worden geïnterpreteerd. Bijvoorbeeld, kunt u een segment op een volledige gegevensmening (gelijkend op a [ Virtuele rapportreeks ](https://experienceleague.adobe.com/en/docs/analytics/components/virtual-report-suites/vrs-about) in Adobe Analytics) toepassen. U kunt ook de definitie van een duur van een bezoek wijzigen of automatisch een nieuw bezoek starten voor elke gewenste gebeurtenis. Al deze instellingen kunnen een aanzienlijke invloed hebben op de rapportage van verschillen tussen Customer Journey Analytics en Adobe Analytics.

## Aantal records tussen producten controleren

Als alle bovenstaande instellingen er hetzelfde uitzien en u het aantal records tussen producten wilt valideren, kunt u de volgende stappen uitvoeren:

1. In Adobe Experience Platform [ de Diensten van de Vraag van 0}, stel de volgende Totale Verslagen door timestamps vraag in werking:](https://experienceleague.adobe.com/en/docs/experience-platform/query/home)

   ```sql
   SELECT
     Substring(from_utc_timestamp(timestamp,'{timeZone}'), 1, 10) AS Day,
     Count(_id) AS Records
   FROM  {dataset}
   WHERE   timestamp >= from_utc_timestamp('{fromDate}','UTC')
     AND timestamp < from_utc_timestamp('{toDate}','UTC')
     AND timestamp IS NOT NULL
     AND enduserids._experience.aaid.id IS NOT NULL
   GROUP BY Day
   ORDER BY Day;
   ```

1. In Adobe Analytics [ het voer van Gegevens ](https://experienceleague.adobe.com/en/docs/analytics/export/analytics-data-feed/data-feed-overview), produceer voederdossiers voor de gewenste datumwaaier. Tel het aantal rijen in elk bestand, waarbij de volgende rijen worden geïdentificeerd en uitgesloten:

   * `exclude_hit` is niet `0` (gegevens die in beide producten van Analysis Workspace zijn uitgesloten)
   * `hit_source` is `0` , `3` , `5` , `7` , `8` , `9` of `10` (Gegevensbronnen en andere niet-raakgegevens)
   * `page_event` is `53` of `63` (Streaming Media houdt-live hits)

   Rijen die aan een van de bovenstaande criteria voldoen, worden niet opgenomen in de insluitingsworkflow van de Source-connector voor Analytics en moeten daarom ook worden uitgesloten bij het tellen van rijen voor gegevensinvoer.

1. De totale verslagen in de Diensten van de Vraag zouden het aantal rijen in een gegevensvoer voor de zelfde tijdspanne moeten aanpassen.
