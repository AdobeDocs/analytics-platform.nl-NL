---
title: Ondersteuning voor Customer Journey Analytics-functies
description: Customer Journey Analytics-functies vergeleken met Adobe Analytics-functies ingesteld.
exl-id: be19aa27-58aa-438d-806c-e27c9a289797
source-git-commit: 58627fd11c4031449f156e70cbfa41dac143ac90
workflow-type: tm+mt
source-wordcount: '1075'
ht-degree: 4%

---

# Ondersteuning voor Customer Journey Analytics-functies

In de volgende tabellen wordt aangegeven welke functies in Adobe Analytics worden ondersteund, gedeeltelijk of niet ondersteund in Customer Journey Analytics (CJA). Deze lijsten worden na verloop van tijd gewijzigd wanneer functies aan CJA worden toegevoegd.

## Volledig ondersteunde functies/componenten

| Adobe Analytics-functie | Opmerkingen over ondersteuning |
| --- | --- |
| Anomaliedetectie | Volledige ondersteuning |
| Attribution IQ | Volledige ondersteuning |
| Berekende standaarden | Bestaande cijfers in de traditionele Analysis Workspace worden niet naar CJA verzonden. |
| Draaien tussen apparaten en kanalen | Zie [Kanaaloverschrijdende analyse](/help/connections/cca/overview.md). |
| Datumvergelijkingen | Volledige ondersteuning |
| Datumbereik | Ondersteuning voor Aangepaste agenda is gepland. |
| Dimensies | CJA gebruikt XDM en ondersteunt onbeperkte afmetingen en is niet gekoppeld aan de aangepaste eVars of props van traditionele Analytics. |
| Buiten-de-box Analysis Workspace-afmetingen (bv. Browsertype, Type referentie, Besturingssysteem enz.) | CJA biedt deze afmetingen native zolang de basis-XDM-velden (zoals gebruikersagent of apparaat-id) zijn gevuld. Voor klanten die de Verbinding van Gegevens van de Analyse (ADC) gebruiken, zijn sommige van deze afmetingen beschikbaar, maar niet allen. Raadpleeg onze [documentatie waarop analysevariabelen worden ondersteund via ADC](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/acp_connectors_overview/analytics_mapping_fields.md). |
| GDPR-verwijdering | Merk op dat GDPR nu in coördinatie met [!UICONTROL Adobe Experience Platform] wordt behandeld - CJA erft welke gegevensveranderingen [!UICONTROL Experience Platform] aan onderliggende datasets maakt. |
| Variabelen/lijsteigenschappen weergeven | CJA gebruikt XDM en steunt onbeperkte koordseries die op dezelfde manier als listVars kunnen worden gebruikt. |
| Metrics | CJA gebruikt het Model van de Gegevens van de Ervaring (XDM) en steunt onbeperkte metriek en is niet verbonden aan de gebeurtenissen van het douanesucces van traditionele Analytics. Merk op dat sommige standaardmetriek van traditionele Analytics zijn anders genoemd: Bezoekers = Personen, Bezoeken = Sessies, Hits = Gebeurtenissen. |
| PDF exporteren | Volledige ondersteuning |
| Projectcuratie | Volledige ondersteuning |
| Projectkoppeling | Volledige ondersteuning |
| Tijdverwerking rapporteren | CJA baseert zich uitsluitend op de Verwerking van de Tijd van het Rapport. |
| API-toegang rapporteren | Nu beschikbaar met de [CJA API](https://www.adobe.io/cja-apis/docs/). |
| Geplande rapporten/projecten | Volledige ondersteuning |
| Segmenten | Nu &quot;Filters&quot; genoemd - merk op dat bestaande segmenten in traditionele Analysis Workspace niet worden geëxporteerd naar CJA. |
| Gebruikersmachtigingen/Toegangsbeheer voor gegevens | CJA maakt onderscheid tussen Adobe Admin Console-productbeheerders en -gebruikers. Alleen productbeheerders kunnen 1) verbindingen of gegevensweergaven maken/bijwerken/verwijderen, 2) projecten, filters of meetgegevens bijwerken/verwijderen die door andere gebruikers zijn gemaakt, en 3) een Workspace-project delen met alle gebruikers |
| Virtuele rapportsuites | Wordt nu [Gegevensweergaven](/help/data-views/create-dataview.md) genoemd. |
| VRS-componentcursus | Nu onderdeel van gegevensweergaven. |
| A4T | De steun wordt verleend door gebieden in [de Verbinding van Gegevens van Analytics](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=en). |

## Ondersteund met caveats

| Functie | Notities |
| --- | --- |
| Classificaties | Nu genoemd &quot;de Datasets van de Raadpleging&quot;. Classificaties die worden gebruikt in Analytics kunnen worden geïmporteerd naar het Experience Platform en CJA met behulp van de gegevensconnector voor analytische classificaties. Gegevenssets voor opzoeken kunnen ook rechtstreeks naar AEP worden geüpload en beschikbaar worden gesteld in CJA. |
| Aangepaste sessie | Ondersteuning voor alle andere aangepaste sessionisatiefuncties dan mobiele achtergrondhits. |
| Klantkenmerken | Nu &quot;profielgegevenssets&quot; genoemd, worden ze niet automatisch geïmporteerd uit Experience Cloud, maar moeten ze worden geüpload naar AEP voordat ze beschikbaar zijn in CJA. |
| Apparaat, browser, technologische afmetingen | Deze afmetingen worden automatisch opgenomen wanneer een AEP-gegevensset specifieke XDM-schemavelden bevat en voldoet aan de XDM Experience Event-klasse. |
| De ingangen, de Uitgangen, en de tijd bestede dimensies en metriek | Ondersteund (Ingangen en Uitgangen worden nu Sessiebegin en Sessieeinde genoemd) en worden op een iets andere manier berekend. |
| Instellingen voor eVar-persistentie | eVars maken geen deel meer uit van CJA. De instellingen voor persistentie maken nu echter deel uit van de gegevensweergave en zijn beschikbaar voor alle dimensies. Onthoud dat persistentie is gebaseerd op de verwerking van de rapporttijd, niet op de verwerking van gegevensverzameling. Dimension in gegevensweergaven zijn beperkt tot een maximale persistentie van 90 dagen en ondersteunen geen onbeperkte persistentie. |
| Marketingkanalen | De gegevens van Kanalen van de marketing stromen in CJA door de Verbinding van Gegevens van de Analyse. De regels van het Kanaal van de marketing moeten nog in traditionele Adobe Analytics worden gevormd. Sommige regels worden niet ondersteund. Zie [CJA-documentatie over marketingkanalen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html?lang=en#cja-usecases) voor meer informatie. |
| Productvariabele | Binnen het Experience Platform, kunnen de gebruikers serie van de typegebieden van Objecten binnen een datasetschema gebruiken om aan dit gebruiksgeval te voldoen. Binnen CJA kunnen klanten een willekeurig aantal productvariabelen gebruiken en zijn ze niet beperkt tot één variabele, zoals in Adobe Analytics. |
| Project delen | Het delen van projecten wordt alleen ondersteund door gebruikers van CJA - er wordt geen project gedeeld tussen CJA en de traditionele Analysis Workspace. |
| Visualisaties | Alle visualisaties worden ondersteund, behalve voor de visualisatie Kaart. |

## Gedeeltelijke ondersteuning

| Functie | Notities |
| --- | --- |
| Bot filteren | Voor gegevenssets op basis van de analytische gegevensconnector (ADC) wordt beide filters toegepast. De algemene binaire filterlogica voor andere datasets wordt niet uitgevoerd door [!UICONTROL Experience Platform] of CJA. |
| Media Analytics | De gegevens van media zijn beschikbaar als deel van de Verbinding van Gegevens van Analytics. |
| Merchandising-eVars | Het gedrag van Merchandising eVars kan worden bereikt gebruikend dimensies binnen een Serie van Objecten aangezien een koopjesdising eVar niet wordt geplaatst om persistentie te gebruiken. Op dit moment is de persistentie van de dimensie van de koophandel niet beschikbaar. |
| Deelvensters | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. De deelvensters Segment vergelijken, Analytics voor Doel (A4T) en Medium Gelijktijdige Viewers worden niet ondersteund. |
| Verwerkingsregels | Voor op gegevensschakelaar-gebaseerde datasets van Gegevens van Analytics, worden de verwerkingsregels nog toegepast. [De mogelijkheden van de prep van gegevens in het ](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html?lang=en) Platform van de Ervaring van Adobe kunnen ook als vervanging voor verwerkingsregels voor gegevens worden gebruikt die rechtstreeks naar Platform gaan. |

## Momenteel niet ondersteund, maar gepland

| Functie | Notities |
| --- | --- |
| Waarschuwingen | Er is steun gepland. |
| Contributieanalyse | Er is steun gepland. |
| CSV-download | Er is steun gepland. |
| Aangepaste kalenders | Er is steun gepland. |
| Rapportage van Data Warehouse (100% rijexport) | Ondersteuning is gepland via de Analysis Workspace-interface. [!UICONTROL Experience Platform Query Service] verstrekt ook een interface voor deze gebruiksgevallen in CJA. |
| ID-instelling via apparaatgrafiek | Er is steun gepland. |
| Metrische deduplicatie | Er is steun gepland. |
| Handelswijzigingsvariabele persistentie | Er is steun gepland. |
| Real-time rapportage | Er is steun gepland. |
| Report Builder (Excel-plug-in) | Er is steun gepland. |
| Segment-IQ | Er is steun gepland. |
| Segmentpublicatie (segmenten verzenden van Workspace naar Experience Cloud) | Er is steun gepland. |

## Steun nog niet gepland

| Functie | Notities |
| --- | --- |
| Activity Map | De steun is nog niet gepland. |
| Advertising Cloud | De steun is nog niet gepland. |
| Builder voor classificatieregels | De steun is nog niet gepland. |
| Gegevensfeeds | De steun is nog niet gepland. |
| Samenvattingsgegevensbronnen | De steun is nog niet gepland. |

## Wordt nooit ondersteund

* Metrische personen met behulp van Cross-Device Coop
* Dashboards voor rapporten en analyses
* Bladwijzers voor rapporten en analyses
* Doelstellingen voor rapporten en analyses
* Gebeurtenissen van de agenda voor rapporten en analyses
* Mobiele services
