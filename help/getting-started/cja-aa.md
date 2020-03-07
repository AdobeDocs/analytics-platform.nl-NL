---
title: Customer Journey Analytics biedt ondersteuning voor de functie
description: De eigenschappen van de Analyse van de Reis van de klant vergeleken met de eigenschappen van de Analyse van Adobe plaatsen.
translation-type: tm+mt
source-git-commit: 1d65b22ab2323bebf42b2782b2bab2ed52869a02

---


# Customer Journey Analytics biedt ondersteuning voor de functie

De volgende lijsten maken een lijst van welke eigenschappen in de Analyse van Adobe worden gesteund, gedeeltelijk gesteund of niet gesteund in de Analyse van de Reis van de Klant (CJA). Deze lijsten zullen in tijd veranderen aangezien de eigenschappen aan CJA worden toegevoegd.

## Volledig ondersteunde functies/onderdelen

| Functie | Opmerkingen |
| --- | --- |
| Metriek | CJA hefboomwerkingen het Model van de Gegevens van de Ervaring (XDM) en steunt onbeperkte metriek en is niet gebonden aan de gebeurtenissen van het douanesucces van traditionele Analytics. Merk op dat sommige standaardmetriek van traditionele Analytics zijn anders genoemd: Bezoekers = Mensen, Bezoeken = Zittingen, Hits = Gebeurtenissen. |
| Afmetingen | CJA hefboomwerkingen XDM en steunt onbeperkte afmetingen en is niet gebonden aan de gebeurtenissen van het douanesucces van traditionele Analytics. |
| Variabelen/lijstprofielen | CJA hefboomwerkingen XDM en steunt onbeperkte lijstvariabelen |
| Datumbereik | De steun van de Kalender van de douane wordt gepland. |
| Berekende waarden | Merk op dat om het even welke bestaande calc metriek in de traditionele Werkruimte van de Analyse niet aan CJA zal worden gesteund. |
| Segmenten | Nu genoemd &quot;Filters&quot; - merk op dat om het even welke bestaande segmenten in de traditionele Werkruimte van de Analyse niet aan CJA zullen worden gesteund. |
| Attributie IQ | Volledige support |
| Projectomschrijving | Volledige support |
| Projectkoppeling | Volledige support |
| Datumvergelijkingen | Volledige support |
| Virtuele rapportsuites | Nu genoemd de [Meningen](/help/data-views/create-dataview.md)van Gegevens. |
| VRS-componentregistratie | Nu een deel van de Meningen van Gegevens. |
| Verwerking van de Tijd van het rapport | CJA baseert zich uitsluitend op de Verwerking van de Tijd van het Rapport. |
| GDPR-verwijdering | Merk op dat GDPR nu in coördinatie met het Platform van de Ervaring van Adobe wordt behandeld - CJA erft wat het Platform van de Ervaring van gegevensveranderingen aan onderliggende datasets aanbrengt. |

## Ondersteund met caveats

| Functie | Opmerkingen |
| --- | --- |
| Productvariabele | De productvariabele die momenteel beschikbaar voor rapportering voor gegevens is die aan het schema van de Gebeurtenis van de Ervaring in overeenstemming zijn (specifiek gebruikend het productListItems voorwerp). |
| Visualisaties | Alle visualisaties worden gesteund behalve de visualisatie van de Kaart. |
| AAM-publiek | Als de klanten de datasets van de Gegevensschakelaar van de Analytics gebruiken, zullen dit gegeven deel van de gegevens van ADC uitmaken. |
| Projectdeling | Het delen van het project wordt slechts gesteund tussen gebruikers van CJA - er is geen project delend tussen CJA en de traditionele Werkruimte van de Analyse. |
| Aangepaste sessie | Steun voor alle eigenschappen van de douanesessie buiten mobiele achtergrondklappen. |
| Var persistentie-instellingen | Vars maken niet meer deel uit van CJA. Nochtans, zijn de persistentiemontages nu een deel van de Meningen van Gegevens en zijn beschikbaar voor alle afmetingen. Houd in mening dat de persistentie op de verwerking van de rapporttijd, niet gegevensverzamelingsverwerking gebaseerd is. Dit betekent dat alle persistentie gebaseerd zal zijn op de rapporteringsdatumrange in plaats van op alle gegevens. |
| Classificaties | Nu genoemd &quot;de Datasets van de Raadpleging&quot;, worden zij niet automatisch ingevoerd uit traditionele Analytics. Ze moeten worden geüpload naar AEP voordat ze beschikbaar zijn in CJA. |
| Klantattributen | Nu genoemd &quot;de Datasets van het Profiel&quot;, worden zij niet automatisch ingevoerd uit de Wolk van de Ervaring, maar zullen aan AEP moeten worden geupload alvorens zij in CJA beschikbaar zijn. |

## Gedeeltelijke support

| Functie | Opmerkingen |
| --- | --- |
| De afmetingen van de Werkruimte van de Analyse uit-van-de-doosanalyse (b.v. Browser Type, het Type van Verwijzer, de Kanalen van de Marketing, het Aantal van het Bezoek enz.) | CJA levert deze afmetingen niet natief op. Voor klanten die de Schakelaar van de Gegevens van de Analyse (ADC) gebruiken, zijn sommige van deze afmetingen beschikbaar, maar niet allen. Gelieve te verwijzen naar onze [documentatie waarover de variabelen van de Analyse via ADC](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/acp_connectors_overview/analytics_mapping_fields.md)worden gesteund. |
| Panelen | Het lege Comité, het Comité van de Attributie, en het Comité Freeform worden volledig gesteund. De Vergelijking van het segment wordt niet gesteund. |
| Merchandising eVars | Merchandising eVars zal slechts met op ADC-Gebaseerde datasets werken tenzij zij strikt met het zelfde schema XDM (gelijkend op de beperkingen van de productlijst hierboven) in overeenstemming zijn. |
| Bodemfilters | Voor gegevenssets op basis van analytics Data Connector (ADC) wordt zowel filtering toegepast. De algemene bot filterlogica voor andere datasets wordt niet uitgevoerd door het Platform van de Ervaring of CJA. |
| Verwerkingsregels | Voor op ADC-Gebaseerde datasets, worden de verwerkingsregels nog toegepast. |
| Identiteitskaarten voor verschillende apparaten | De klanten zijn beperkt tot &quot;éénmalige&quot;plaatsen van de gegevens via de Dienst van de Vraag, of moeten momenteel deze logica op gegevens toepassen voorafgaand aan de gegevensopname van het Platform van de Ervaring. |

## Momenteel niet ondersteund, maar gepland

| Functie | Opmerkingen |
| --- | --- |
| Anomaly Detection | De steun is gepland. |
| Bijdrage-analyse | De steun is gepland. |
| Segment-IQ | De steun is gepland. |
| Het Publiceren van het segment (verzendend segmenten van Werkruimte naar de Wolk van de Ervaring) | De steun is gepland. |
| Toegangsrechten/toegangscontroles voor gebruikers | Alle gebruikers in CJA hebben de zelfde toegangscontroles - dit betekent alle gebruikers toegang tot alle verbindingen, gegevensmeningen, enz. hebben. Fundamenteel, zijn alle gebruikers admin-vlakke gebruikers in CJA. De steun is gepland voor 2020. |
| CSV-download | De steun is gepland. |
| Geplande rapporten/projecten | De steun is gepland. |
| Waarschuwingen | De steun is gepland. |
| Aangepaste agenda | De steun is gepland. |
| Marketingkanalen | De steun is gepland. |
| PDF-export | De steun is gepland. |
| Meldend API Toegang | De steun is gepland - zal slechts met API 2.0 beschikbaar zijn. |
| ID Stitching via Device Graph | De steun is gepland. |

## Nog niet geplande steun

| Functie | Opmerkingen |
| --- | --- |
| A4T | De steun is nog niet gepland. |
| Videoanalyse | De steun is nog niet gepland. |
| Cloud voor reclame | De steun is nog niet gepland. |
| De Bouwer van het rapport (de stop van Excel) | De steun is nog niet gepland. |
| Activiteitenkaart | De steun is nog niet gepland. |
| Bouwer van indelingsregel | De steun is nog niet gepland. |
| Summiere Gegevensbronnen | De steun is nog niet gepland. |
| Real-time rapportage | De steun is nog niet gepland. |

## Wordt nooit ondersteund

| Functie | Opmerkingen |
| --- | --- |
| Mensen metrisch gebruikend de Coop van het Apparaat van het Kruis |  |
| Dashboards voor rapporten en analyses |  |
| Rapporten en analytische bladwijzers |  |
| Streefcijfers voor rapporten en analyses |  |
| Gebeurtenissen van rapporten en analytische agenda |  |
| Ad-hocanalyse |  |
| Rapportering van gegevens | De Dienst van de Vraag van het Platform van de Ervaring van Adobe zal de nieuwe interface voor deze gebruiksgevallen in CJA zijn. |
| Mobiele services |  |
| Gegevensinvoer |  |
