---
title: Ondersteuning voor Customer Journey Analytics-functies
description: Customer Journey Analytics-functies vergeleken met Adobe Analytics-functies ingesteld.
translation-type: tm+mt
source-git-commit: 9733d6471e6f1c886fd27b702654349d6760870c
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 5%

---


# Ondersteuning voor Customer Journey Analytics-functies

In de volgende tabellen wordt aangegeven welke functies in Adobe Analytics worden ondersteund, gedeeltelijk of niet ondersteund in Customer Journey Analytics (CJA). Deze lijsten worden na verloop van tijd gewijzigd wanneer functies aan CJA worden toegevoegd.

## Volledig ondersteunde functies/componenten

| Functie | Notities |
| --- | --- |
| Metrics | CJA gebruikt het Model van de Gegevens van de Ervaring (XDM) en steunt onbeperkte metriek en is niet verbonden aan de gebeurtenissen van het douanesucces van traditionele Analytics. Merk op dat sommige standaardmetriek van traditionele Analytics zijn anders genoemd: Bezoekers = Personen, Bezoeken = Sessies, Hits = Gebeurtenissen. |
| Dimensies | CJA maakt gebruik van XDM en ondersteunt onbeperkte afmetingen en is niet gekoppeld aan de aangepaste succesgebeurtenissen van traditionele Analytics. |
| Variabelen/lijsteigenschappen weergeven | CJA gebruikt XDM en ondersteunt onbeperkte lijstvariabelen |
| Datumbereik | Ondersteuning voor Aangepaste agenda is gepland. |
| Berekende standaarden | Bestaande cijfers in de traditionele Analysis Workspace worden niet naar CJA verzonden. |
| Segmenten | Nu &quot;Filters&quot; genoemd - merk op dat bestaande segmenten in traditionele Analysis Workspace niet worden geëxporteerd naar CJA. |
| Anomaliedetectie | Volledige ondersteuning vanaf september 2020 |
| Attribution IQ | Volledige ondersteuning |
| Projectcuratie | Volledige ondersteuning |
| Projectkoppeling | Volledige ondersteuning |
| Datumvergelijkingen | Volledige ondersteuning |
| Virtuele rapportsuites | Wordt nu aangeroepen [Gegevens](/help/data-views/create-dataview.md). |
| VRS-componentcursus | Nu onderdeel van gegevensweergaven. |
| Tijdverwerking rapporteren | CJA baseert zich uitsluitend op de Verwerking van de Tijd van het Rapport. |
| GDPR-verwijdering | Merk op dat GDPR nu in coördinatie met [!UICONTROL Experience Platform] - CJA neemt alle gegevenswijzigingen over [!UICONTROL Experience Platform] maakt aan onderliggende datasets. |

## Ondersteund met caveats

| Functie | Notities |
| --- | --- |
| Productvariabele | De productvariabele die momenteel beschikbaar is voor rapportage voor gegevens die voldoen aan het schema Experience Event (met name met behulp van het productListItems-object). |
| Visualisaties | Alle visualisaties worden ondersteund, behalve voor de visualisatie Kaart. |
| AAM publiek | Als klanten [!UICONTROL Analytics Data Connector] gegevenssets, deze gegevens maken deel uit van de ADC-gegevens. |
| Project delen | Het delen van projecten wordt alleen ondersteund door gebruikers van CJA - er wordt geen project gedeeld tussen CJA en de traditionele Analysis Workspace. |
| Aangepaste sessie | Ondersteuning voor alle andere aangepaste sessionisatiefuncties dan mobiele achtergrondhits. |
| Instellingen voor eVar-persistentie | eVars maken geen deel meer uit van CJA. De instellingen voor persistentie maken nu echter deel uit van de gegevensweergave en zijn beschikbaar voor alle dimensies. Onthoud dat persistentie is gebaseerd op de verwerking van de rapporttijd, niet op de verwerking van gegevensverzameling. Dit betekent dat alle persistentie gebaseerd zal zijn op het bereik van de rapportagedatum in plaats van op de volledige gegevens. |
| Classificaties | Deze worden nu &#39;Gegevensbestanden opzoeken&#39; genoemd en worden niet automatisch geïmporteerd uit traditionele analysemogelijkheden. Ze moeten worden geüpload naar AEP voordat ze beschikbaar zijn in CJA. |
| Klantkenmerken | Nu &quot;profielgegevenssets&quot; genoemd, worden ze niet automatisch geïmporteerd uit Experience Cloud, maar moeten ze worden geüpload naar AEP voordat ze beschikbaar zijn in CJA. |

## Gedeeltelijke ondersteuning

| Functie | Notities |
| --- | --- |
| Analysis Workspace-afmetingen buiten de box (zoals browsertype, Type referentie, Marketingkanalen, Nummer bezoek, enz.) | CJA biedt deze afmetingen niet native. Voor klanten die de Verbinding van Gegevens van de Analyse (ADC) gebruiken, zijn sommige van deze afmetingen beschikbaar, maar niet allen. Raadpleeg onze [documentatie over de door ADC ondersteunde analytische variabelen](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/acp_connectors_overview/analytics_mapping_fields.md). |
| Deelvensters | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. De deelvensters Segmentvergelijking en Analyse voor Doel (A4T) worden niet ondersteund. |
| Merchandising-eVars | Merchandising eVars zal slechts met op ADC-Gebaseerde datasets werken tenzij zij strikt aan het zelfde XDM schema (gelijkend op de beperkingen van de productlijst hierboven) in overeenstemming zijn. |
| Bot filteren | Voor gegevenssets op basis van de analytische gegevensconnector (ADC) wordt beide filters toegepast. De algemene bot filtering logica voor andere datasets wordt niet uitgevoerd door de [!UICONTROL Experience Platform] of CJA. |
| Verwerkingsregels | Voor op ADC-Gebaseerde datasets, worden de verwerkingsregels nog toegepast. |
| Identiteitsinstellingen voor meerdere apparaten | Klanten zijn beperkt tot &quot;eenmalige&quot; sites van de gegevens via Query Service, of moeten deze logica momenteel toepassen op gegevens voordat [!UICONTROL Experience Platform] gegevensinvoer. |

## Momenteel niet ondersteund, maar gepland

| Functie | Notities |
| --- | --- |
| Contributieanalyse | Er is steun gepland. |
| Segment-IQ | Er is steun gepland. |
| Segmentpublicatie (segmenten verzenden van Workspace naar Experience Cloud) | Er is steun gepland. |
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
| Media Analytics | De steun is nog niet gepland. |
| Advertising Cloud | De steun is nog niet gepland. |
| Report Builder (Excel-plug-in) | De steun is nog niet gepland. |
| Activity Map | De steun is nog niet gepland. |
| Builder voor classificatieregels | De steun is nog niet gepland. |
| Samenvattingsgegevensbronnen | De steun is nog niet gepland. |
| Real-time rapportage | De steun is nog niet gepland. |

## Wordt nooit ondersteund

* Metrische personen met behulp van Cross-Device Coop
* Dashboards voor rapporten en analyses
* Bladwijzers voor rapporten en analyses
* Doelstellingen voor rapporten en analyses
* Gebeurtenissen van de agenda voor rapporten en analyses
* Ad Hoc Analysis
* Rapportage Data Warehouse - [!UICONTROL Experience Platform Query Service] wordt de nieuwe interface voor deze gebruiksgevallen in CJA.
* Mobiele services
* Gegevensfeeds
