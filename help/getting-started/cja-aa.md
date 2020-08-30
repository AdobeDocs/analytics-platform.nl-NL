---
title: Customer Journey Analytics-functionaliteit
description: De eigenschappen van de Analyse van de Reis van de klant vergeleken met de eigenschappen van de Analyse van Adobe plaatsen.
translation-type: tm+mt
source-git-commit: 7d2abfb2cd91ee7574fce10847abb89f14b5388e
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 5%

---


# Customer Journey Analytics-functionaliteit

De volgende lijsten maken een lijst van welke eigenschappen in de Analyse van Adobe worden gesteund, gedeeltelijk of niet gesteund in de Analyse van de Reis van de Klant (CJA). Deze lijsten zullen in tijd veranderen aangezien de eigenschappen aan CJA worden toegevoegd.

## Volledig ondersteunde functies/onderdelen

| Functie | Opmerkingen |
| --- | --- |
| Metrics | CJA hefboomwerkingen het Model van de Gegevens van de Ervaring (XDM) en steunt onbeperkte metriek en is niet gebonden aan de gebeurtenissen van het douanesucces van traditionele Analytics. Merk op dat sommige standaardmetriek van traditionele Analytics zijn anders genoemd: Bezoekers = Mensen, Bezoeken = Zittingen, Hits = Gebeurtenissen. |
| Dimensies | CJA hefboomwerkingen XDM en steunt onbeperkte afmetingen en is niet gebonden aan de gebeurtenissen van het douanesucces van traditionele Analytics. |
| Lijst variabelen/Lijst Props | CJA hefboomwerkingen XDM en steunen onbeperkte lijstvariabelen |
| Datumbereik | Aangepaste agenda-ondersteuning is gepland. |
| Berekende standaarden | Merk op dat om het even welke bestaande calc metriek in de traditionele Werkruimte van de Analyse niet aan CJA zal worden gesteund. |
| Segmenten | Nu genoemd &quot;Filters&quot; - merk op dat om het even welke bestaande segmenten in de traditionele Werkruimte van de Analyse niet aan CJA zullen worden gemeld. |
| Anomaliedetectie | Volledige steun vanaf juni 2020 |
| Attribution IQ | Volledige support |
| Projectralculatie | Volledige support |
| Projectkoppeling | Volledige support |
| Datumvergelijkingen | Volledige support |
| Virtuele rapportsuites | Nu geroepen [Gegevensweergaven](/help/data-views/create-dataview.md). |
| VRS Component Curation | Nu deel van de Meningen van Gegevens. |
| Rapporttijdverwerking | CJA baseert zich uitsluitend op de Verwerking van de Tijd van het Rapport. |
| GDPR-verwijdering | Merk op dat GDPR nu wordt behandeld in coördinatie met [!UICONTROL Experience Platform] - CJA erft alle gegevenswijzigingen [!UICONTROL Experience Platform] maakt aan onderliggende datasets. |

## Ondersteund met caveats

| Functie | Opmerkingen |
| --- | --- |
| Productvariabele | De productvariabele die momenteel beschikbaar is voor rapportering voor gegevens die met het schema van de Gebeurtenis van de Ervaring in overeenstemming zijn (specifiek gebruikend het productListItems voorwerp). |
| Visualisaties | Alle visualisaties worden gesteund behalve de visualisatie van de Kaart. |
| AAM-doelgroepen | Als de klanten gebruiken [!UICONTROL Analytics Data Connector] gegevensreeksen, deze gegevens zullen deel uitmaken van de ADC-gegevens. |
| Projectdeling | Het delen van het project wordt slechts gesteund tussen gebruikers van CJA - er is geen project het delen tussen CJA en de traditionele Werkruimte van de Analyse. |
| Aangepaste sessie | Steun voor alle eigenschappen van de douanesessie buiten mobiele achtergrondhits. |
| persistentiemontages van eVar | Vars maken geen deel meer uit van CJA. Nochtans, maken de persistentiemontages nu deel uit van de Meningen van Gegevens en zijn beschikbaar voor alle afmetingen. Houd in mening dat de persistentie op de verwerking van de rapporttijd, niet de verwerking van de gegevensinzameling gebaseerd is. Dit betekent dat alle persistentie gebaseerd zal zijn op de rapporteringsdatumrange in plaats van op alle gegevens. |
| Classificaties | Nu genoemd de &quot;Datasets van de Raadpleging&quot;, worden zij niet automatisch ingevoerd uit traditionele Analytica. Ze moeten worden geüpload naar AEP voordat ze beschikbaar zijn in CJA. |
| Klantkenmerken | Nu genoemd &quot;de Datasets van het Profiel&quot;, worden zij niet automatisch ingevoerd uit de Wolk van de Ervaring, maar zullen aan AEP moeten worden geupload alvorens zij in CJA beschikbaar zijn. |

## Gedeeltelijke ondersteuning

| Functie | Opmerkingen |
| --- | --- |
| De afmetingen van de Werkruimte van de uit-van-de-doos Analyse (b.v. Browser Type, het Type van Referrer, de Kanalen van de Marketing, het Aantal van het Bezoek enz.) | CJA verstrekt deze afmetingen natively niet. Voor klanten die de Schakelaar van de Gegevens van de Analyse (ADC) gebruiken, zijn sommige van deze afmetingen beschikbaar, maar niet allen. Raadpleeg onze [documentatie waarop de analytische variabelen via ADC worden ondersteund](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/acp_connectors_overview/analytics_mapping_fields.md). |
| Deelvensters | Het lege Comité, het Comité van de Attributie, het Comité Freeform, en de Snelle Inzichten worden volledig gesteund. De vergelijking en de Analyse van het Segment voor de panelen van het Doel (A4T) worden niet gesteund. |
| Merchandising-eVars | Merchandising eVars zal slechts met op ADC-Gebaseerde datasets werken tenzij zij strikt met het zelfde schema XDM (gelijkend op de beperkingen van de productlijst hierboven) in overeenstemming zijn. |
| Bodemfilter | Voor gegevenssets op basis van analytische gegevens-connector (ADC) wordt bot filtering toegepast. De algemene bot filtering logica voor andere datasets wordt niet uitgevoerd door de [!UICONTROL Experience Platform] of CJA. |
| Verwerkingsregels | Voor op ADC-Gebaseerde datasets, worden de verwerkingsregels nog toegepast. |
| Identiteitskaart voor meerdere apparaten kiezen | De klanten zijn beperkt tot &quot;eenmalig&quot;plaatsen van de gegevens via de Dienst van de Vraag, of moeten momenteel deze logica op gegevens voorafgaand aan [!UICONTROL Experience Platform] gegevensopname. |

## Momenteel niet ondersteund, maar gepland

| Functie | Opmerkingen |
| --- | --- |
| Contributieanalyse | Er is steun gepland. |
| Segment-IQ | Er is steun gepland. |
| Segment Publishing (segmenten vanuit de werkruimte naar de cloud van de ervaring verzenden) | Er is steun gepland. |
| Gebruikersrechten/toegangscontroles voor gegevens | Alle gebruikers in CJA hebben de zelfde toegangscontroles - dit betekent alle gebruikers toegang tot alle verbindingen, gegevensmeningen, enz. hebben. Fundamenteel, zijn alle gebruikers admin-vlakke gebruikers in CJA. De steun is gepland voor 2020. |
| CSV-download | Er is steun gepland. |
| Geplande rapporten/projecten | Er is steun gepland. |
| Waarschuwingen | Er is steun gepland. |
| Aangepaste kalenders | Er is steun gepland. |
| Marketingkanalen | Er is steun gepland. |
| PDF-export | Er is steun gepland. |
| API-toegang melden | De steun is gepland - zal slechts met API 2.0 beschikbaar zijn. |
| ID Stitching via Device Graph | Er is steun gepland. |

## Steun nog niet gepland

| Functie | Opmerkingen |
| --- | --- |
| A4T | De steun is nog niet gepland. |
| Videoanalyse | De steun is nog niet gepland. |
| Advertising Cloud | De steun is nog niet gepland. |
| De Bouwer van het rapport (de stop van Excel) | De steun is nog niet gepland. |
| Activity Map | De steun is nog niet gepland. |
| Builder voor classificatieregels | De steun is nog niet gepland. |
| Summiere Gegevensbronnen | De steun is nog niet gepland. |
| Real-time rapportage | De steun is nog niet gepland. |

## Wordt nooit ondersteund

| Functie | Opmerkingen |
| --- | --- |
| De metrische mensen die de Coop van het Kruisapparaat gebruiken |  |
| Dashboards voor rapporten en analyses |  |
| Rapporten en analytische bladwijzers |  |
| Doelstellingen voor rapporten en analyses |  |
| Evenementen van de Kalender van rapporten &amp; van de Analyse |  |
| Ad Hoc Analysis |  |
| Data Warehouse Reporting | [!UICONTROL Experience Platform Query Service] zal de nieuwe interface voor deze gebruiksgevallen in CJA zijn. |
| Mobiele services |  |
| Gegevensfeeds |  |
