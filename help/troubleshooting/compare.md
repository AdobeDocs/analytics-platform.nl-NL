---
title: Uw AA-gegevens vergelijken met CJA-gegevens
description: Leer hoe u uw Adobe Analytics-gegevens kunt vergelijken met gegevens in Customer Journey Analytics
role: Data Engineer, Data Architect, Admin
solution: Customer Journey Analytics
source-git-commit: b0d29964c67d8a6a847a05dbe113b8213b346f9b
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---


# Adobe Analytics-gegevens vergelijken met CJA-gegevens

Stel dat u Adobe Analytics-gegevens in AEP hebt ingevoerd via de Bronverbinding Analytics en vervolgens een CJA-verbinding hebt gemaakt met deze dataset.

![gegevensstroom](assets/compare.png)

Vervolgens hebt u een gegevensweergave gemaakt en tijdens de rapportage van deze gegevens over CJA hebt u afwijkingen van de rapportresultaten in Adobe Analytics vastgesteld.

Hier volgen enkele stappen om uw oorspronkelijke Adobe Analytics-gegevens te vergelijken met de Adobe Analytics-gegevens die nu in Customer Journey Analytics staan.

## Vereisten

* Zorg ervoor de dataset van Analytics in AEP gegevens voor de datumwaaier bevat u onderzoekt.

* Zorg ervoor dat de rapportsuite die u hebt geselecteerd in Analytics overeenkomt met de rapportsuite die in Adobe Experience Platform is ingevoerd.


## Stap 1: Metrische voorvallen uitvoeren in Adobe Analytics

De [Voorval](https://experienceleague.adobe.com/docs/analytics/components/metrics/occurrences.html?lang=en) metrisch toont het aantal treffers waar een bepaalde afmeting werd geplaatst of voortgeduurd.

1. In Analytics > [!UICONTROL Workspace]Sleep het datumbereik waarover u wilt rapporteren als een dimensie naar een [!UICONTROL Freeform] tabel.

1. De [!UICONTROL Occurrences] De metrische waarde wordt automatisch toegepast op dat datumbereik.

1. Sla dit project op zodat u het kunt gebruiken in de vergelijking.

## Stap 2: De resultaten vergelijken met [!UICONTROL Total records by timestamps] in CJA

Vergelijk nu de [!UICONTROL Occurrences] in Analytics aan de Totale verslagen door timestamps in Customer Journey Analytics.

De totale Verslagen door timestamps zouden met Voorkomen moeten aanpassen, op voorwaarde dat geen verslagen door de Bronschakelaar van de Analyse werden gelaten vallen - zie de sectie hieronder.

>[!NOTE]
>
>Dit werkt alleen voor gewone middelste gegevenssets, niet voor gebonden gegevenssets (via [Kanaaloverschrijdende analyse](/help/connections/cca/overview.md)). Houd er rekening mee dat de boekhouding voor de persoon-id die in CJA wordt gebruikt van essentieel belang is voor het maken van de vergelijking. Dat is misschien niet altijd eenvoudig om te repliceren in AA, vooral als de Kanaalanalyse is ingeschakeld.

1. In Adobe Experience Platform [Query-services](https://experienceleague.adobe.com/docs/experience-platform/query/best-practices/adobe-analytics.html), voer de volgende Totaal Records door timestamps-query uit:

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

1. In [Gegevensdoorvoer analyseren](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=en), identificeert u aan de hand van de onbewerkte gegevens of bepaalde rijen door de connector Analytics Source kunnen worden neergezet.

   De [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) kan rijen tijdens de transformatie naar XDM-schema neerzetten. Er kunnen meerdere redenen zijn waarom de hele rij niet geschikt is voor transformatie. Als om het even welke volgende gebieden van Analytics deze waarden hebben, zal de volledige rij worden gelaten vallen.

   | Veld Analyse | Waarden die ervoor zorgen dat deze wordt verwijderd |
   | --- | --- |
   | Uit_schakelen | `y, Y` |
   | Alleen in_data | Niet 0 |
   | Exclusief_hit | Niet 0 |
   | Bot_id | Niet 0 |
   | Hit_source | 0,3,5,7,8,9,10 |
   | Page_event | 53 63 |

1. Als de schakelaar rijen liet vallen, trek die rijen van metrische Voorvallen af. Het resulterende getal moet overeenkomen met het aantal gebeurtenissen in de AEP-gegevenssets.

## Waarom records kunnen worden verwijderd of overgeslagen tijdens inname van AEP

CJA [Verbindingen](/help/connections/create-connection.md) staat u toe om veelvoudige datasets samen te brengen en samen te voegen die op gemeenschappelijke identiteitskaart van de Persoon over de datasets worden gebaseerd. Op de achtergrond passen we deduplicatie toe: volledige buitenste verbinding of vereniging op gebeurtenisdatasets die op timestamps worden gebaseerd en dan binnenste zich bij profiel en raadplegingsdataset aansluiten, die op identiteitskaart van de Persoon wordt gebaseerd.

Hier zijn een aantal redenen waarom records kunnen worden overgeslagen bij het opnemen van gegevens van AEP.

* **Ontbrekende tijdstempels** - Als er tijdstempels ontbreken in gebeurtenisgegevenssets, worden deze records tijdens inname volledig genegeerd of overgeslagen. omdat zij gegevenssets samen zouden laten verenigen .

* **Ontbrekende persoon-id&#39;s** - Ontbrekende personen-id&#39;s (op basis van de gegevensset met gebeurtenissen en/of op basis van de gegevensset met profielen/opzoekingen) zorgen ervoor dat deze records worden genegeerd of overgeslagen. De reden is dat er geen gemeenschappelijke IDs of passende sleutels zijn om zich bij de verslagen aan te sluiten.

* **Ongeldige personen-id&#39;s** - Met ongeldige IDs, kan het systeem geen geldige gemeenschappelijke identiteitskaart onder de datasets vinden om zich aan te sluiten. In sommige gevallen heeft de kolom met de persoon-id ongeldige personen-id&#39;s, zoals &quot;undefined&quot; of &quot;00000000&quot;.

* **Id van grote persoon** - Een persoon-id met een combinatie van cijfers en letters die in een gebeurtenis meer dan 1 miljoen keer per maand voorkomt, kan niet worden toegewezen aan een specifieke gebruiker of persoon. Het wordt gecategoriseerd als ongeldig. Deze records kunnen niet in het systeem worden opgenomen en resulteren in foutgevoelige inname en rapportage.


