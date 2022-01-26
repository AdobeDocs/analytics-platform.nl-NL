---
title: Ondersteuning voor Customer Journey Analytics-functies
description: Customer Journey Analytics-functies vergeleken met Adobe Analytics-functies ingesteld.
exl-id: be19aa27-58aa-438d-806c-e27c9a289797
solution: Customer Journey Analytics
source-git-commit: be823f0ce9ff65528b34cb8d5693b60e2ff0ee11
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 3%

---

# Ondersteuning voor Customer Journey Analytics-functies

In de volgende tabellen wordt aangegeven welke functies in Adobe Analytics worden ondersteund, gedeeltelijk of niet ondersteund in Customer Journey Analytics (CJA). Deze lijsten worden na verloop van tijd gewijzigd wanneer functies aan CJA worden toegevoegd.

## Volledig ondersteunde functies/componenten

| Adobe Analytics-functie | Opmerkingen over ondersteuning |
| --- | --- |
| Anomaliedetectie | Volledige ondersteuning |
| Attribution IQ | Volledige ondersteuning |
| Berekende standaarden | volledige ondersteuning; Merk op dat bestaande berekende metriek in traditionele Analysis Workspace niet naar CJA zal worden uitgevoerd. |
| Draaien tussen apparaten en kanalen | volledige ondersteuning; Zie [Kanaaloverschrijdende analyse](/help/connections/cca/overview.md). |
| CSV-download | Volledige ondersteuning |
| Aangepaste kalenders | Volledige ondersteuning |
| Datumvergelijkingen | Volledige ondersteuning |
| Datumbereik | Alle functionaliteit voor datumbereik wordt ondersteund. |
| zomertijd | Volledige ondersteuning |
| Dimensies | volledige ondersteuning; CJA gebruikt XDM en ondersteunt onbeperkte afmetingen. CJA is niet gekoppeld aan de aangepaste eVars of props van traditionele Adobe Analytics. |
| Buiten-de-box Analysis Workspace-afmetingen (bv. Browsertype, Type referentie, Besturingssysteem enz.) | CJA biedt deze afmetingen native zolang de basis-XDM-velden (zoals gebruikersagent of apparaat-id) zijn gevuld. Voor klanten die de Verbinding van Gegevens van de Analyse (ADC) gebruiken, zijn sommige van deze afmetingen beschikbaar, maar niet allen. Raadpleeg onze [documentatie over de door ADC ondersteunde analytische variabelen](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/acp_connectors_overview/analytics_mapping_fields.md). |
| GDPR-verwijdering | volledige ondersteuning; merkt op dat GDPR nu wordt behandeld in coördinatie met [!UICONTROL Adobe Experience Platform]. CJA neemt alle gegevenswijzigingen over [!UICONTROL Experience Platform] maakt aan onderliggende datasets. |
| Variabelen/lijsteigenschappen weergeven | volledige ondersteuning; CJA gebruikt XDM en steunt onbeperkte koordseries die op dezelfde manier als listVars kunnen worden gebruikt. |
| Handelswijzigingsvariabele persistentie | Volledige ondersteuning via [afmetingen binden en metriek binden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html?lang=en#binding-dimension) (januari 2022) |
| Merchandising-eVars | Volledige ondersteuning via [afmetingen binden en metriek binden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html?lang=en#binding-dimension) (januari 2022) |
| Metrics | volledige ondersteuning; CJA gebruikt het Model van de Gegevens van de Ervaring (XDM) en steunt onbeperkte metriek en is niet verbonden aan de gebeurtenissen van het douanesucces van traditionele Analytics. Merk op dat sommige standaardmetriek van traditionele Analytics zijn anders genoemd: Bezoekers = Personen, Bezoeken = Sessies, Hits = Gebeurtenissen. |
| Metrische deduplicatie | Volledige ondersteuning |
| Deelvensters | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. |
| PDF exporteren | Volledige ondersteuning |
| Projectcuratie | Volledige ondersteuning |
| Projectkoppeling | Volledige ondersteuning |
| Report Builder (Excel-plug-in) | Volledige ondersteuning |
| Tijdverwerking rapporteren | volledige ondersteuning; CJA baseert zich uitsluitend op de Verwerking van de Tijd van het Rapport. |
| API-toegang rapporteren | volledige ondersteuning; Beschikbaar via [CJA API](https://www.adobe.io/cja-apis/docs/). |
| Geplande rapporten/projecten | Volledige ondersteuning |
| Segmenten | volledige ondersteuning; Nu &quot;Filters&quot; genoemd - merk op dat bestaande segmenten in traditionele Analysis Workspace niet worden geëxporteerd naar CJA. |
| Gebruikersmachtigingen/Toegangsbeheer voor gegevens | volledige ondersteuning; CJA maakt onderscheid tussen [Adobe Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html?lang=en) productbeheerders en gebruikers. Alleen productbeheerders kunnen <ul><li>Verbindingen of gegevensweergaven maken/bijwerken/verwijderen</li><li>Werk/schrap projecten, filters, of calc metriek bij die door andere gebruikers werden gecreeerd, en</li><li>Een Workspace-project delen met alle gebruikers.</li></ul> |
| Virtuele rapportsuites | volledige ondersteuning; Wordt nu aangeroepen [Gegevens](/help/data-views/create-dataview.md). |
| VRS-componentcursus | volledige ondersteuning; Nu onderdeel van gegevensweergaven. |

## Ondersteund met caveats

| Functie | Notities |
| --- | --- |
| A4T | De steun wordt verleend door gebieden in [Adobe Analytics Source Connector](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=en). |
| Classificaties | Nu genoemd &quot;de Datasets van de Raadpleging&quot;. Classificaties die worden gebruikt in Analytics kunnen worden geïmporteerd naar het Experience Platform en CJA met behulp van de gegevensconnector voor analytische classificaties. Gegevenssets voor opzoeken kunnen ook rechtstreeks naar AEP worden geüpload en beschikbaar worden gesteld in CJA. |
| Aangepaste sessie | Ondersteuning voor alle andere aangepaste sessionisatiefuncties dan mobiele achtergrondhits. |
| Klantkenmerken | Nu &quot;profielgegevenssets&quot; genoemd, worden ze niet automatisch geïmporteerd uit Experience Cloud, maar moeten ze worden geüpload naar AEP voordat ze beschikbaar zijn in CJA. |
| Apparaat, browser, technologische afmetingen | Deze afmetingen worden automatisch opgenomen wanneer een AEP-gegevensset specifieke XDM-schemavelden bevat en voldoet aan de XDM Experience Event-klasse. |
| De ingangen, de Uitgangen, en de tijd bestede dimensies en metriek | Ondersteund (Ingangen en Uitgangen worden nu Sessiebegin en Sessieeinde genoemd) en worden op een iets andere manier berekend. |
| Instellingen voor eVar-persistentie | eVars maken geen deel meer uit van CJA. De instellingen voor persistentie maken nu echter deel uit van de gegevensweergave en zijn beschikbaar voor alle dimensies. Onthoud dat persistentie is gebaseerd op de verwerking van de rapporttijd, niet op de verwerking van gegevensverzameling. Dimension in gegevensweergaven zijn beperkt tot een maximale persistentie van 90 dagen en ondersteunen geen onbeperkte persistentie. |
| GeoSegmentation-afmetingen | Alle GeoSegmentation/geography die in Adobe Analytics wordt verzameld stroomt in CJA door de Verbinding van Gegevens van de Analyse. Implementaties die geen gebruik maken van de gegevensconnector Analytics, zoals toepassingen die voor digitale gegevensverzameling afhankelijk zijn van AEP Web SDK, hebben niet de volledige serie van automatisch uitgevoerde geografische zoekopdrachten (land en staat worden ondersteund, plaats en ritssluiting worden niet ondersteund). |
| Marketingkanalen | De gegevens van Kanalen van de marketing stromen in CJA door de Verbinding van Gegevens van de Analyse. De regels van het Kanaal van de marketing moeten nog in traditionele Adobe Analytics worden gevormd. Sommige regels worden niet ondersteund. Zie voor meer informatie [Documentatie CJA-marketingkanalen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html?lang=en#cja-usecases). |
| Productvariabele | Binnen het Experience Platform, kunnen de gebruikers serie van de typegebieden van Objecten binnen een datasetschema gebruiken om aan dit gebruiksgeval te voldoen. Binnen CJA kunnen klanten een willekeurig aantal productvariabelen gebruiken en zijn ze niet beperkt tot één variabele, zoals in Adobe Analytics. |
| Project delen | Het delen van projecten wordt alleen ondersteund door gebruikers van CJA - er wordt geen project gedeeld tussen CJA en de traditionele Analysis Workspace. |
| Visualisaties | Alle visualisaties worden ondersteund, behalve voor de visualisatie Kaart. |

## Gedeeltelijke ondersteuning

| Functie | Notities |
| --- | --- |
| Bot filteren | Voor gegevenssets die zijn gebaseerd op gegevenssets op basis van analytische bronaansluiting, wordt beide filtering toegepast. De algemene bot filtering logica voor andere datasets wordt niet uitgevoerd door de [!UICONTROL Experience Platform] of CJA. |
| Media Analytics | De gegevens van media zijn beschikbaar als deel van de Verbinding van Gegevens van Analytics. |
| Deelvensters | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. De deelvensters Segment vergelijken, Analytics voor Doel (A4T) en Medium Gelijktijdige Viewers worden niet ondersteund. |
| Verwerkingsregels | Voor op gegevensschakelaar-gebaseerde datasets van Gegevens van Analytics, worden de verwerkingsregels nog toegepast. [Mogelijkheden voor gegevensuitwisseling in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html?lang=en) kan ook worden gebruikt als vervanging voor verwerkingsregels voor gegevens die rechtstreeks naar het Platform gaan. |

## Momenteel niet ondersteund, maar gepland

| Functie | Notities |
| --- | --- |
| Waarschuwingen | Er is steun gepland. |
| Builder voor classificatieregels | Het zal lichtjes verschillend in CJA werken, gebruikend koordmanipulaties in rapporttijd eerder dan raadplegingsdatasets. |
| Contributieanalyse | Er is steun gepland. |
| Rapportage van Data Warehouse (100% rijexport) | Ondersteuning is gepland via de Analysis Workspace-interface. Adobe Experience Platform [[!UICONTROL Query Service]](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=en) verstrekt ook een interface voor deze gebruiksgevallen in CJA. |
| ID-instelling via apparaatgrafiek | Er is steun gepland. |
| Lift and Trust Reporting | Er is steun gepland. |
| Verwerkingsregels, VISTA-regels, regels voor verwerking van distributiekanalen | De steun geplande, maar zal bij vraag-tijd eerder dan tijdens gegevensinzameling voor flexibelere en retroactieve en niet-destructieve gegevensmanipulaties werken. |
| Projectsjablonen | Er is steun gepland. |
| Real-time rapportage | Er is steun gepland. |
| Segment-IQ | Er is steun gepland. |
| Segmentpublicatie (segmenten verzenden van Workspace naar Experience Cloud) | Er is steun gepland. Wordt in CJA &quot;Audience Publishing&quot; genoemd. |
| Nieuwe versus herhaalde sessierapportage | De steun is gepland met sommige bedenkingen. |

## Steun nog niet gepland

| Functie | Notities |
| --- | --- |
| Activity Map | De steun is nog niet gepland. |
| Advertising Cloud | De steun is nog niet gepland. |
| Builder voor classificatieregels | De steun is nog niet gepland. |
| Gegevensfeeds | De steun is nog niet gepland. |
| Samenvattingsgegevensbronnen | De steun is nog niet gepland. |
| Gegevensbronnen van transactie-id | De steun is nog niet gepland. |
| Valutaconversie | De steun is nog niet gepland. |
| Real Time Reports | De steun is nog niet gepland. |

## Wordt nooit ondersteund

* Metrische personen met behulp van Cross-Device Coop
* Dashboards voor rapporten en analyses
* Bladwijzers voor rapporten en analyses
* Doelstellingen voor rapporten en analyses
* Gebeurtenissen van de agenda voor rapporten en analyses
* Mobiele services
