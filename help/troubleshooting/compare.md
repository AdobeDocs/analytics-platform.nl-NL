---
title: Uw AA-gegevens vergelijken met CJA-gegevens
description: Leer hoe u uw Adobe Analytics-gegevens kunt vergelijken met gegevens in Customer Journey Analytics
role: Data Engineer, Data Architect, Admin
solution: Customer Journey Analytics
exl-id: dd273c71-fb5b-459f-b593-1aa5f3e897d2
source-git-commit: 2088fd98510887e86cffb6bd957d32a35fcfc467
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# Adobe Analytics-gegevens vergelijken met CJA-gegevens

Aangezien uw organisatie CJA goedkeurt, kunt u sommige verschillen in gegevens tussen Adobe Analytics en CJA opmerken. Dit is normaal en kan om verschillende redenen voorkomen. CJA is ontworpen om u toe te staan om op enkele beperkingen op uw gegevens in AA te verbeteren. Onverwachte/onbedoelde discrepanties kunnen zich echter voordoen. Dit artikel is ontworpen om u te helpen voor die verschillen diagnostiseren en op te lossen zodat u en uw team CJA kunnen gebruiken onbelemmerd door zorgen over gegevensintegriteit.

Laten we aannemen dat u Adobe Analytics-gegevens via de [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html)en maakte vervolgens een CJA-verbinding met deze dataset.

![gegevensstroom](assets/compare.png)

Vervolgens hebt u een gegevensweergave gemaakt en tijdens de rapportage van deze gegevens over CJA hebt u afwijkingen van de rapportresultaten in Adobe Analytics vastgesteld.

Hier volgen enkele stappen om uw oorspronkelijke Adobe Analytics-gegevens te vergelijken met de Adobe Analytics-gegevens die nu in Customer Journey Analytics staan.

## Vereisten

* Zorg ervoor de dataset van Analytics in AEP gegevens voor de datumwaaier bevat u onderzoekt.

* Zorg ervoor dat de rapportsuite die u hebt geselecteerd in Analytics overeenkomt met de rapportsuite die in Adobe Experience Platform is ingevoerd.

## Stap 1: Metrische voorvallen uitvoeren in Adobe Analytics

De [Voorval](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html) metrisch toont het aantal treffers waar een bepaalde afmeting werd geplaatst of voortgeduurd.

1. In Analytics > [!UICONTROL Workspace]Sleep het datumbereik waarover u wilt rapporteren als een dimensie naar een [!UICONTROL Freeform] tabel.

1. De [!UICONTROL Occurrences] De metrische waarde wordt automatisch toegepast op dat datumbereik.

1. Sla dit project op zodat u het kunt gebruiken in de vergelijking.

## Stap 2: De resultaten vergelijken met [!UICONTROL Total records by timestamps] in CJA

Vergelijk nu de [!UICONTROL Occurrences] in Analytics aan de Totale verslagen door timestamps in Customer Journey Analytics.

De totale Verslagen door timestamps zouden met Voorkomen moeten aanpassen, op voorwaarde dat geen verslagen door de Bronschakelaar van de Analyse werden gelaten vallen - zie de sectie hieronder.

>[!NOTE]
>
>Dit werkt alleen voor gewone middelste gegevenssets, niet voor gebonden gegevenssets (via [Kanaaloverschrijdende analyse](/help/connections/cca/overview.md)). Houd er rekening mee dat de boekhouding voor de persoon-id die in CJA wordt gebruikt van essentieel belang is voor het maken van de vergelijking. Dat is misschien niet altijd eenvoudig om te repliceren in AA, vooral als de Kanaalanalyse is ingeschakeld.

1. In Adobe Experience Platform [Query-services](https://experienceleague.adobe.com/docs/experience-platform/query/best-practices/adobe-analytics.html)voert u het volgende uit [!UICONTROL Total Records by timestamps] query:

```
SELECT Substring(from_utc_timestamp(timestamp,'{timeZone}'), 1, 10) as Day, \ 
        Count(_id) AS Records 
        FROM  {dataset} \ 
        WHERE timestamp>=from_utc_timestamp('{fromDate}','UTC') \ 
        AND timestamp<from_utc_timestamp('{toDate}','UTC') \ 
        AND timestamp IS NOT NULL \ 
        AND enduserids._experience.aaid.id IS NOT NULL  \ 
        GROUP BY Day \ 
        ORDER BY Day; 
```

1. In [Gegevensdoorvoer analyseren](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html), identificeert u aan de hand van de onbewerkte gegevens of bepaalde rijen zijn uitgefilterd door de connector van de bron voor analyse.

   De [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) Hiermee kunt u bepaalde rijen filteren tijdens de transformatie naar het XDM-schema. Er kunnen meerdere redenen zijn waarom de hele rij niet geschikt is voor transformatie. Als een van de volgende analytische velden deze waarden heeft, wordt de hele rij uitgefilterd.

   | Veld Analyse | Waarden die ertoe leiden dat een rij wordt neergezet |
   | --- | --- |
   | Uit_schakelen | y, Y |
   | Alleen in_data | Niet 0 |
   | Exclusief_hit | Niet 0 |
   | Bot_id | Niet 0 |
   | Hit_source | 0, 3, 5, 7, 8, 9, 10 |
   | Page_event | 53 63 |

   Zie voor meer informatie over hit\_source: [Referentie gegevenskolom](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=en). Zie voor meer informatie over page\_event: [Pagina-gebeurtenis opzoeken](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-page-event.html?lang=en).

1. Als de schakelaar rijen filtreerde, trek die rijen van af [!UICONTROL Occurrences] metrisch. Het resulterende getal moet overeenkomen met het aantal gebeurtenissen in de Adobe Experience Platform-gegevenssets.

## Waarom records tijdens inname van AEP gefilterd of overgeslagen kunnen worden

CJA [Verbindingen](/help/connections/create-connection.md) staat u toe om veelvoudige datasets samen te brengen en samen te voegen die op gemeenschappelijke identiteitskaart van de Persoon over de datasets worden gebaseerd. Op de achtergrond passen we deduplicatie toe: de volledige buitenste verbinding of de vereniging op gebeurtenisdatasets die op timestamps worden gebaseerd, en toen binnenste zich bij profiel en raadplegingsdataset aansluiten, die op identiteitskaart van de Persoon wordt gebaseerd.

Hier zijn een aantal redenen waarom records kunnen worden overgeslagen bij het opnemen van gegevens van AEP.

* **Ontbrekende tijdstempels** - Als er tijdstempels ontbreken in gebeurtenisgegevenssets, worden deze records tijdens inname volledig genegeerd of overgeslagen.

* **Ontbrekende persoon-id&#39;s** - Ontbrekende personen-id&#39;s (op basis van de gegevensset voor gebeurtenissen en/of van de gegevensset voor profiel/zoekopdracht) zorgen ervoor dat deze records worden genegeerd of overgeslagen. De reden is dat er geen gemeenschappelijke IDs of passende sleutels zijn om zich bij de verslagen aan te sluiten.

* **Ongeldige of grote persoon-id&#39;s** - Met ongeldige IDs, kan het systeem geen geldige gemeenschappelijke identiteitskaart onder de datasets vinden om zich aan te sluiten. In sommige gevallen heeft de kolom met de persoon-id ongeldige personen-id&#39;s, zoals &quot;undefined&quot; of &quot;00000000&quot;. Een persoon-id (met een combinatie van cijfers en letters) die in een gebeurtenis meer dan 1 miljoen keer per maand wordt weergegeven, kan niet aan een specifieke gebruiker of persoon worden toegewezen. Het wordt gecategoriseerd als ongeldig. Deze records kunnen niet in het systeem worden opgenomen en resulteren in foutgevoelige inname en rapportage.
