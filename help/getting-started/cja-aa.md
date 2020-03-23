---
title: Klantenservice voor analyse van reisgegevens
description: De kenmerken van de analysefuncties van de Klanten in vergelijking met de functies van Adobe Analytics zijn ingesteld.
translation-type: tm+mt
source-git-commit: 1d65b22ab2323bebf42b2782b2bab2ed52869a02

---


# Klantenservice voor analyse van reisgegevens

In de volgende tabellen wordt aangegeven welke functies in Adobe Analytics worden ondersteund, gedeeltelijk of niet ondersteund in CJA (Customer Journey Analytics). Deze lijsten worden na verloop van tijd gewijzigd wanneer functies aan CJA worden toegevoegd.

## Volledig ondersteunde functies/componenten

| Functie | Notities |
| --- | --- |
| Metrisch | CJA gebruikt het Model van de Gegevens van de Ervaring (XDM) en steunt onbeperkte metriek en is niet verbonden aan de gebeurtenissen van het douanesucces van traditionele Analytics. Merk op dat sommige standaardmetriek van traditionele Analytics zijn anders genoemd: Bezoekers = Personen, Bezoeken = Sessies, Hits = Gebeurtenissen. |
| Afmetingen | CJA maakt gebruik van XDM en ondersteunt onbeperkte afmetingen en is niet gekoppeld aan de aangepaste succesgebeurtenissen van traditionele Analytics. |
| Variabelen/lijsteigenschappen weergeven | CJA gebruikt XDM en ondersteunt onbeperkte lijstvariabelen |
| Datumbereik | Ondersteuning voor Aangepaste agenda is gepland. |
| Berekende cijfers | Merk op dat om het even welke bestaande calc metriek in de traditionele Werkruimte van de Analyse niet naar CJA zal worden overgebracht. |
| Segmenten | Nu genoemd &quot;Filters&quot; - merk op dat om het even welke bestaande segmenten in de traditionele Werkruimte van de Analyse niet naar CJA zullen worden overgebracht. |
| Attributie-IQ | Volledige ondersteuning |
| Projectcuratie | Volledige ondersteuning |
| Projectkoppeling | Volledige ondersteuning |
| Datumvergelijkingen | Volledige ondersteuning |
| Virtuele rapportsets | Nu genoemd de [Mening](/help/data-views/create-dataview.md)van Gegevens. |
| VRS-componentcursus | Nu onderdeel van gegevensweergaven. |
| Tijdverwerking rapporteren | CJA baseert zich uitsluitend op de Verwerking van de Tijd van het Rapport. |
| GDPR-verwijdering | Merk op dat GDPR nu wordt behandeld in coördinatie met het Platform van de Ervaring van Adobe - CJA erft wat het Platform van de Ervaring van gegevens aan onderliggende datasets maakt. |

## Ondersteund met caveats

| Functie | Notities |
| --- | --- |
| Productvariabele | De productvariabele die momenteel beschikbaar is voor rapportage voor gegevens die voldoen aan het schema Experience Event (met name met behulp van het productListItems-object). |
| Visualisaties | Alle visualisaties worden ondersteund, behalve voor de visualisatie Kaart. |
| AAM-publiek | Als de klanten de datasets van de Gegevensverbinding van Analytics gebruiken, zullen deze gegevens deel van de gegevens ADC uitmaken. |
| Project delen | Het delen van projecten wordt slechts gesteund tussen gebruikers van CJA - er is geen project delend tussen CJA en de traditionele Werkruimte van de Analyse. |
| Aangepaste sessie | Ondersteuning voor alle andere aangepaste sessionisatiefuncties dan mobiele achtergrondhits. |
| Standaardinstellingen voor eVar | eVars maken geen deel meer uit van CJA. De instellingen voor persistentie maken nu echter deel uit van de gegevensweergave en zijn beschikbaar voor alle dimensies. Onthoud dat persistentie is gebaseerd op de verwerking van de rapporttijd, niet op de verwerking van gegevensverzameling. Dit betekent dat alle persistentie gebaseerd zal zijn op het bereik van de rapportagedatum in plaats van op de volledige gegevens. |
| Classificaties | Deze worden nu &#39;Gegevensbestanden opzoeken&#39; genoemd en worden niet automatisch geïmporteerd uit traditionele analysemogelijkheden. Ze moeten worden geüpload naar AEP voordat ze beschikbaar zijn in CJA. |
| Klantkenmerken | Nu &quot;profielgegevenssets&quot; genoemd, worden ze niet automatisch geïmporteerd uit Experience Cloud, maar moeten ze worden geüpload naar AEP voordat ze beschikbaar zijn in CJA. |

## Gedeeltelijke ondersteuning

| Functie | Notities |
| --- | --- |
| Afmetingen van de buiten-de-box Analyse-werkruimte (bijv. Browsertype, Type Referenter, Marketingkanalen, Nummer bezoek, enz.) | CJA biedt deze afmetingen niet native. Voor klanten die de Verbinding van Gegevens van de Analyse (ADC) gebruiken, zijn sommige van deze afmetingen beschikbaar, maar niet allen. Raadpleeg de [documentatie over de analytische variabelen die via ADC](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/acp_connectors_overview/analytics_mapping_fields.md)worden ondersteund. |
| Deelvensters | Het deelvenster Lege deelvensters, Kenmerken en Vrije vorm worden volledig ondersteund. Segmentvergelijking wordt niet ondersteund. |
| Merchandising Vars | Merchandising eVars zal slechts met op ADC-Gebaseerde datasets werken tenzij zij strikt aan het zelfde XDM schema (gelijkend op de beperkingen van de productlijst hierboven) in overeenstemming zijn. |
| Bot filteren | Voor gegevenssets op basis van de analytische gegevensconnector (ADC) wordt beide filters toegepast. De algemene bot filtering logica voor andere datasets wordt niet uitgevoerd door het Platform van de Ervaring of CJA. |
| Verwerkingsregels | Voor op ADC-Gebaseerde datasets, worden de verwerkingsregels nog toegepast. |
| Identiteitsinstellingen voor meerdere apparaten | De klanten zijn beperkt tot &quot;eenmalig&quot;steunen van de gegevens via de Dienst van de Vraag, of moeten momenteel deze logica op gegevens toepassen voorafgaand aan de gegevensopname van het Platform van de Ervaring. |

## Momenteel niet ondersteund, maar gepland

| Functie | Notities |
| --- | --- |
| Anomaly Detection | Er is steun gepland. |
| Bijdrage-analyse | Er is steun gepland. |
| Segment-IQ | Er is steun gepland. |
| Segmentpublicatie (segmenten van Workspace naar Experience Cloud verzenden) | Er is steun gepland. |
| Gebruikersmachtigingen/Toegangsbeheer voor gegevens | Alle gebruikers in CJA hebben de zelfde toegangscontroles - dit betekent alle gebruikers toegang tot alle verbindingen, gegevensmeningen, enz. hebben. In feite zijn alle gebruikers gebruikers op beheerniveau in CJA. De steun is gepland voor 2020. |
| CSV-download | Er is steun gepland. |
| Geplande rapporten/projecten | Er is steun gepland. |
| Waarschuwingen | Er is steun gepland. |
| Aangepaste kalenders | Er is steun gepland. |
| Marketingkanalen | Er is steun gepland. |
| PDF exporteren | Er is steun gepland. |
| API-toegang rapporteren | Ondersteuning is gepland; alleen beschikbaar met API 2.0. |
| ID-instelling via apparaatgrafiek | Er is steun gepland. |

## Steun nog niet gepland

| Functie | Notities |
| --- | --- |
| A4T | De steun is nog niet gepland. |
| Video Analytics | De steun is nog niet gepland. |
| Advertising Cloud | De steun is nog niet gepland. |
| Report Builder (Excel-plug-in) | De steun is nog niet gepland. |
| Activiteitenkaart | De steun is nog niet gepland. |
| Classification Rule Builder | De steun is nog niet gepland. |
| Samenvattingsgegevensbronnen | De steun is nog niet gepland. |
| Real-time rapportage | De steun is nog niet gepland. |

## Wordt nooit ondersteund

| Functie | Notities |
| --- | --- |
| Metrische personen met behulp van Cross-Device Coop |  |
| Dashboards voor rapporten en analyses |  |
| Bladwijzers voor rapporten en analyses |  |
| Doelstellingen voor rapporten en analyses |  |
| Gebeurtenissen van de agenda voor rapporten en analyses |  |
| Ad hoc-analyse |  |
| Data Warehouse Reporting | De Adobe Experience Platform Query Service wordt de nieuwe interface voor deze gebruiksgevallen in CJA. |
| Mobiele services |  |
| Gegevensfeeds |  |
