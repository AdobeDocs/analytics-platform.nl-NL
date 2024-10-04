---
title: Vergelijken met uw Adobe Analytics-gegevens
description: Leer hoe u uw Adobe Analytics-gegevens kunt vergelijken met gegevens in Customer Journey Analytics
role: Data Engineer, Data Architect, Admin
solution: Customer Journey Analytics
exl-id: dd273c71-fb5b-459f-b593-1aa5f3e897d2
feature: Troubleshooting
keywords: queryservice;Query-service;sql-syntaxis
source-git-commit: 90d1c51c11f0ab4d7d61b8e115efa8257a985446
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 0%

---

# Vergelijken met uw Adobe Analytics-gegevens

Aangezien uw organisatie Customer Journey Analytics goedkeurt, kunt u sommige verschillen in gegevens tussen Adobe Analytics en Customer Journey Analytics opmerken. Dit is normaal en kan om verschillende redenen voorkomen. Customer Journey Analytics is ontworpen om u toe te staan om op sommige beperkingen van uw gegevens in AA te verbeteren. Onverwachte en onbedoelde discrepanties kunnen zich echter voordoen. Dit artikel is ontworpen om u te helpen voor die verschillen diagnostiseren en op te lossen zodat u en uw team Customer Journey Analytics kunnen gebruiken zonder dat u zich zorgen hoeft te maken over gegevensintegriteit.

Laten wij veronderstellen u de gegevens van Adobe Analytics in Adobe Experience Platform via de [ Bron van Analytics schakelaar ](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) opnam, en dan een verbinding van de Customer Journey Analytics creeerde gebruikend deze dataset.

![ de gegevensstroom van Adobe Analytics door de gegevensschakelaar aan Adobe Experience Platform en aan de Analyse van de Reis van de Klant gebruikend verbindingen CJA.](assets/compare.png)

Vervolgens hebt u een gegevensweergave gemaakt en tijdens de rapportage van deze gegevens over de Customer Journey Analytics hebt u afwijkingen gezien van de rapportresultaten in Adobe Analytics.

Hier volgen enkele stappen om uw oorspronkelijke Adobe Analytics-gegevens te vergelijken met de Adobe Analytics-gegevens die nu in Customer Journey Analytics zijn.

## Vereisten

* Zorg ervoor de dataset van de Analyse in Adobe Experience Platform gegevens voor de datumwaaier bevat u onderzoekt.

* Zorg ervoor dat de rapportsuite die u hebt geselecteerd in Analytics overeenkomt met de rapportsuite die in Adobe Experience Platform is ingevoerd.

## Stap 1: De metrische voorvallen in Adobe Analytics uitvoeren

De [ metrische voorkomen ](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html) toont het aantal treffers waar een bepaalde afmeting werd geplaatst of voortgeduurd.

1. Sleep in Analytics > [!UICONTROL Workspace] het datumbereik waarover u wilt rapporteren als een dimensie naar een [!UICONTROL Freeform] -tabel.

1. De metrische waarde [!UICONTROL Occurrences] wordt automatisch toegepast op dat datumbereik.

1. Sla dit project op zodat u het kunt gebruiken in de vergelijking.

## Stap 2: Vergelijk de resultaten met [!UICONTROL Total records by timestamps] in Customer Journey Analytics

Vergelijk nu [!UICONTROL Occurrences] in Analytics met de Totale verslagen door timestamps in Customer Journey Analytics.

Het totaal aantal records per tijdstempel moet overeenkomen met het aantal exemplaren, op voorwaarde dat er geen records zijn neergezet door de Source-connector voor Analytics - zie de onderstaande sectie.

>[!NOTE]
>
>Dit werkt voor regelmatige middentechnieken slechts, niet gestikte dataset (via [ het Stitching ](/help/stitching/overview.md)). Houd er rekening mee dat de boekhouding voor de persoon-id die in de Customer Journey Analytics wordt gebruikt van essentieel belang is voor het maken van de vergelijking. Dat is misschien niet altijd gemakkelijk om in Adobe Analytics te repliceren, vooral als Stitching is ingeschakeld.

1. In de Diensten van de Vraag van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/query/best-practices/adobe-analytics.html), stel de volgende [!UICONTROL Total Records by timestamps] vraag in werking:[

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

1. In [ Diefstal van Gegevens van Analytics ](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html), identificeer van de ruwe gegevens of sommige rijen uit door de schakelaar van Source van Analytics zouden kunnen zijn gefiltreerd.

   De [ schakelaar van Source van de Analyse ](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) zou bepaalde rijen tijdens de transformatie aan schema kunnen filtreren XDM. Er kunnen meerdere redenen zijn waarom de hele rij niet geschikt is voor transformatie. Als een van de volgende analytische velden deze waarden heeft, wordt de hele rij uitgefilterd.

   | Veld Analyse | Waarden die ertoe leiden dat een rij wordt neergezet |
   | --- | --- |
   | Uit_schakelen | y, Y |
   | Alleen in_data | Niet 0 |
   | Exclusief_hit | Niet 0 |
   | Bot_id | Niet 0 |
   | Hit_source | 0, 3, 5, 7, 8, 9, 10 |
   | Page_event | 53 63 |

   Voor meer informatie over hit\_source zie: [ de kolomverwijzing van Gegevens ](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html). Voor meer informatie over pagina\_event zie: [ de Opzoeken van de Gebeurtenis van de Pagina ](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-page-event.html).

1. Als de schakelaar rijen filtreerde, trek die rijen van metrisch [!UICONTROL Occurrences] af. Het resulterende getal moet overeenkomen met het aantal gebeurtenissen in de Adobe Experience Platform-gegevenssets.

## Waarom records tijdens inname vanuit Adobe Experience Platform gefilterd of overgeslagen kunnen worden

De Verbindingen van de Customer Journey Analytics [ ](/help/connections/create-connection.md) staan u toe om veelvoudige datasets samen te brengen en zich aan te sluiten die op gemeenschappelijke identiteitskaart van de Persoon over de datasets worden gebaseerd. Op het achterste eind, passen wij deduplicatie toe: volledige buitenste toetreden of verenigen op gebeurtenisdatasets die op timestamps worden gebaseerd, en dan binnengaan zich op profiel en raadplegingsdataset, die op identiteitskaart van de Persoon wordt gebaseerd.

Hier volgen enkele redenen waarom records kunnen worden overgeslagen bij het opnemen van gegevens uit Adobe Experience Platform.

* **Ontbrekende Tijdstempels** - als timestamps van gebeurtenisdatasets ontbreken, zullen die verslagen volledig worden genegeerd of tijdens opname overgeslagen.

* **Ontbrekende Identiteitskaart van de Persoon** - Ontbrekende Person IDs (van de gebeurtenissendataset en/of van profiel/raadplegingsdataset) veroorzaakt die verslagen om worden genegeerd of worden overgeslagen. De reden is dat er geen gemeenschappelijke IDs of passende sleutels zijn om zich bij de verslagen aan te sluiten.

* **Ongeldige of Grote Persoon IDs** - met ongeldige IDs, kan het systeem geen geldige gemeenschappelijke identiteitskaart onder de datasets vinden om zich bij te voegen. In sommige gevallen heeft de kolom met de persoon-id ongeldige personen-id&#39;s, zoals &quot;undefined&quot; of &quot;00000000&quot;. Een persoon-id (met een combinatie van cijfers en letters) die in een gebeurtenis meer dan 1 miljoen keer per maand wordt weergegeven, kan niet aan een specifieke gebruiker of persoon worden toegewezen. Het wordt gecategoriseerd als ongeldig. Deze records kunnen niet in het systeem worden opgenomen en resulteren in foutgevoelige inname en rapportage.
