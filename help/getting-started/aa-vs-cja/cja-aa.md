---
title: Ondersteuning voor Customer Journey Analytics-functies
description: Customer Journey Analytics-functies vergeleken met Adobe Analytics-functies ingesteld.
exl-id: be19aa27-58aa-438d-806c-e27c9a289797
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: 94b3e7417b82e9ae3ad080884d4c184bee412c2c
workflow-type: tm+mt
source-wordcount: '1507'
ht-degree: 3%

---

# Ondersteuning voor Customer Journey Analytics-functies

In de volgende tabellen wordt aangegeven welke functies in Adobe Analytics worden ondersteund, gedeeltelijk of niet ondersteund in Customer Journey Analytics (CJA). Deze lijsten worden na verloop van tijd gewijzigd wanneer functies aan CJA worden toegevoegd.

## Volledig ondersteunde functies/componenten

| Adobe Analytics-functie | Opmerkingen over ondersteuning |
| --- | --- |
| Anomaliedetectie | Volledige ondersteuning |
| Attribution IQ | Volledige ondersteuning |
| Publiek publiceren | Volledige ondersteuning. Opgeroepen Segment Publishing (verzending van segmenten van Workspace naar Experience Cloud) in AA. [Publiek publiceren](/help/components/audiences/audiences-overview.md) verzendt publiek naar het Profiel van de Klant in real time in Experience Platform. |
| Berekende standaarden | volledige ondersteuning; Merk op dat bestaande berekende metriek in traditionele Analysis Workspace niet naar CJA zal worden uitgevoerd. |
| Kalendergebeurtenissen | Volledige ondersteuning. Kalendergebeurtenissen zijn geïmplementeerd als [Annotaties](/help/components/annotations/overview.md) in Workspace. |
| Builder voor classificatieregels | Volledige ondersteuning. Geroepen [subtekenreeksen](/help/data-views/component-settings/substring.md) in CJA. Gebruikt tekenreeksmanipulaties in rapporttijd eerder dan raadplegingsdatasets. |
| Draaien tussen apparaten en kanalen | volledige ondersteuning; Zie [Kanaaloverschrijdende analyse](/help/connections/cca/overview.md). |
| CSV-download | Volledige ondersteuning |
| Aangepaste kalenders | Volledige ondersteuning |
| Datumvergelijkingen | Volledige ondersteuning |
| Datumbereik | Alle functionaliteit voor datumbereik wordt ondersteund. |
| zomertijd | Volledige ondersteuning |
| Apparaat, Browser, Referrer, de dimensies van de Technologie | Deze afmetingen worden automatisch opgenomen wanneer een AEP-gegevensset specifieke XDM-schemavelden bevat en voldoet aan de XDM Experience Event-klasse. Raadpleeg onze [documentatie over de door ADC ondersteunde analytische variabelen](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics.html?lang=en).<p>Als u geen Adobe Source Connector gebruikt om gegevens van Adobe Analytics in CJA te bevolken, maar in plaats daarvan de gegevensinzameling van SDK van het Web van het Experience Platform te gebruiken, worden het Apparaat en de dimensies die op de raadpleging van het Apparaat worden gebaseerd momenteel niet gesteund. Zij zullen in de nabije toekomst worden gesteund. |
| Dimensies | volledige ondersteuning; CJA gebruikt XDM en ondersteunt onbeperkte afmetingen. CJA is niet gekoppeld aan de aangepaste eVars of props van traditionele Adobe Analytics. |
| GDPR-verwijdering | volledige ondersteuning; merkt op dat GDPR nu wordt behandeld in coördinatie met [!UICONTROL Adobe Experience Platform]. CJA neemt alle gegevenswijzigingen over [!UICONTROL Experience Platform] maakt aan onderliggende datasets. |
| Variabelen/lijsteigenschappen weergeven | volledige ondersteuning; CJA gebruikt XDM en steunt onbeperkte koordseries die op dezelfde manier als listVars kunnen worden gebruikt. |
| Handelswijzigingsvariabele persistentie | Volledige ondersteuning via [afmetingen binden en metriek binden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html#binding-dimension) |
| Merchandising-eVars | Volledige ondersteuning via [afmetingen binden en metriek binden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html#binding-dimension) |
| Metrics | volledige ondersteuning; CJA gebruikt het Model van de Gegevens van de Ervaring (XDM) en steunt onbeperkte metriek en is niet verbonden aan de gebeurtenissen van het douanesucces van traditionele Analytics. Merk op dat sommige standaardmetriek van traditionele Analytics zijn anders genoemd: Bezoekers = Personen, Bezoeken = Sessies, Hits = Gebeurtenissen. |
| Metrische deduplicatie | Volledige ondersteuning |
| Mobiel scorebord/dashboards | Volledige ondersteuning |
| Deelvensters | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. |
| PDF exporteren | Volledige ondersteuning |
| Projectcuratie | Volledige ondersteuning |
| Projectkoppeling | Volledige ondersteuning |
| Report Builder (Excel-plug-in) | Volledige ondersteuning |
| Tijdverwerking rapporteren | volledige ondersteuning; CJA baseert zich uitsluitend op de Verwerking van de Tijd van het Rapport. |
| API-toegang rapporteren | volledige ondersteuning; Beschikbaar via [CJA API](https://www.adobe.io/cja-apis/docs/). |
| Geplande rapporten/projecten | Volledige ondersteuning |
| Segmenten | volledige ondersteuning; Nu &quot;Filters&quot; genoemd - merk op dat bestaande segmenten in traditionele Analysis Workspace niet worden geëxporteerd naar CJA. |
| Streaming media-analyse | De mediagegevens zijn beschikbaar op 30 juli 2022 als onderdeel van het deelvenster Mediagelijktijdige viewers en het deelvenster Tijd voor afspelen van media in Workspace. |
| Gebruikersmachtigingen/Toegangsbeheer voor gegevens | volledige ondersteuning; CJA maakt onderscheid tussen [Adobe Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html) productbeheerders en gebruikers. Alleen productbeheerders kunnen <ul><li>Verbindingen of gegevensweergaven maken/bijwerken/verwijderen</li><li>Werk/schrap projecten, filters, of calc metriek bij die door andere gebruikers werden gecreeerd, en</li><li>Een Workspace-project delen met alle gebruikers.</li></ul> |
| Virtuele rapportsuites | volledige ondersteuning; Wordt nu aangeroepen [Gegevens](/help/data-views/create-dataview.md). |
| VRS-componentcursus | volledige ondersteuning; Nu onderdeel van gegevensweergaven. |

{style=&quot;table-layout:auto&quot;}

## Ondersteund met caveats

| Functie | Notities |
| --- | --- |
| A4T | De steun wordt verleend door gebieden in [Adobe Analytics Source Connector](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html). |
| Classificaties | Nu genoemd &quot;de Datasets van de Raadpleging&quot;. Classificaties die worden gebruikt in Analytics kunnen worden geïmporteerd naar het Experience Platform en CJA met behulp van de Bronconnector voor analytische classificaties. Gegevenssets voor opzoeken kunnen ook rechtstreeks naar AEP worden geüpload en beschikbaar worden gesteld in CJA. |
| Aangepaste sessie | Ondersteuning voor alle aangepaste sessionisatiefuncties, behalve voor mobiele achtergrondgeluiden. |
| Klantkenmerken | Nu &quot;profielgegevenssets&quot; genoemd, worden ze niet automatisch geïmporteerd uit Experience Cloud, maar moeten ze worden geüpload naar AEP voordat ze beschikbaar zijn in CJA. |
| [!UICONTROL Device], [!UICONTROL Browser], [!UICONTROL Referrer], [!UICONTROL Technology] afmetingen | Deze afmetingen worden automatisch opgenomen wanneer een AEP-gegevensset specifieke XDM-schemavelden bevat en voldoet aan de XDM Experience Event-klasse. Raadpleeg onze [documentatie over welke analytische variabelen worden gesteund via Analytics Source Connector](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics.html). Voor klanten CJA die niet de BronSchakelaar gebruiken om gegevens van Adobe Analytics in CJA te bevolken, maar in plaats daarvan de gegevensinzameling van SDK van het Web van AEP gebruiken, [!UICONTROL Device] en dimensies die zijn gebaseerd op de zoekopdracht van het apparaat worden momenteel niet ondersteund, maar worden in de nabije toekomst wel ondersteund. |
| De ingangen, de Uitgangen, en de tijd bestede dimensies en metriek | Ondersteund (Ingangen en Uitgangen worden nu Sessiebegin en Sessieeinde genoemd) en worden op een iets andere manier berekend. |
| Instellingen voor eVar-persistentie | eVars maken geen deel meer uit van CJA. De instellingen voor persistentie maken nu echter deel uit van de gegevensweergave en zijn beschikbaar voor alle dimensies. Onthoud dat persistentie is gebaseerd op de verwerking van de rapporttijd, niet op de verwerking van gegevensverzameling. Dimension in gegevensweergaven zijn beperkt tot een maximale persistentie van 90 dagen en ondersteunen geen onbeperkte persistentie. |
| GeoSegmentation-afmetingen | Alle GeoSegmentation/geography die in Adobe Analytics wordt verzameld stroomt in CJA door [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html). Implementaties die geen gebruik maken van de Bronverbinding Analytics, zoals die welke voor digitale gegevensverzameling afhankelijk zijn van AEP Web SDK, zullen niet de volledige serie van automatisch uitgevoerde geografische zoekopdrachten hebben: Land en staat worden wereldwijd ondersteund, stad en zip niet. |
| IP Obfuscatie | Voor CJA-klanten die de Analytics Source Connector gebruiken om gegevens van Adobe Analytics in CJA te vullen: De IP die de verduisteringsmontages in Adobe Analytics worden toegepast stromen door aan uw gegevens CJA. U kunt deze instellingen desgewenst in Adobe Analytics beheren.<p>Voor klanten CJA die SDK van het Web van Adobe Experience Platform gebruiken om gegevens in Platform en CJA direct te bevolken: U kunt Prep van Gegevens voor de Inzameling van Gegevens in Platform gebruiken om regels te vormen die het IP adres zullen verduisteren dat op de vereisten van uw bedrijf wordt gebaseerd. |
| Marketingkanalen | De gegevens van Kanalen van de marketing stromen in CJA door de Bron van Analytics Schakelaar. De regels van het Kanaal van de marketing moeten nog in traditionele Adobe Analytics worden gevormd. Sommige regels worden niet ondersteund. Zie voor meer informatie [Documentatie CJA-marketingkanalen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html#cja-usecases). |
| Nieuwe versus herhaalde sessierapportage | Ondersteund op 17 augustus 2022, [met een terugzoekvenster van 13 maanden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views-usecases.html?lang=en#new-repeat). |
| Productvariabele | Binnen het Experience Platform, kunnen de gebruikers serie van de typegebieden van Objecten binnen een datasetschema gebruiken om aan dit gebruiksgeval te voldoen. Binnen CJA kunnen klanten een willekeurig aantal productvariabelen gebruiken en zijn ze niet beperkt tot één variabele, zoals in Adobe Analytics. |
| Project delen | Het delen van projecten wordt alleen ondersteund door gebruikers van CJA - er wordt geen project gedeeld tussen CJA en de traditionele Analysis Workspace. |
| Visualisaties | Alle visualisaties worden ondersteund, behalve voor de visualisatie Kaart. |

{style=&quot;table-layout:auto&quot;}

## Gedeeltelijke ondersteuning

| Functie | Notities |
| --- | --- |
| Bot filteren | Voor [Adobe Analytics Source Connector](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html)Op gegevenssets gebaseerde gegevenssets worden beide gefilterd. De algemene bot filtering logica voor andere datasets wordt niet uitgevoerd door de [!UICONTROL Experience Platform] of CJA. |
| Deelvensters | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. De deelvensters Segmentvergelijking en Analyse voor Doel (A4T) worden niet ondersteund. |
| Verwerkingsregels | Voor Analytics Source Connector-gebaseerde datasets, worden de verwerkingsregels nog toegepast. [Mogelijkheden voor gegevensuitwisseling in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html) kan ook worden gebruikt als vervanging voor verwerkingsregels voor gegevens die rechtstreeks naar het Platform gaan. |

{style=&quot;table-layout:auto&quot;}

## Momenteel niet ondersteund, maar gepland

| Functie | Notities |
| --- | --- |
| Waarschuwingen | Er is steun gepland. |
| Contributieanalyse | Er is steun gepland. |
| Rapportage van Data Warehouse (100% rijexport) | Ondersteuning is gepland via de Analysis Workspace-interface. Adobe Experience Platform [[!UICONTROL Query Service]](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl) verstrekt ook een interface voor deze gebruiksgevallen in CJA. |
| ID-instelling via apparaatgrafiek | Er is steun gepland. |
| Lift and Trust Reporting | Er is steun gepland. |
| Verwerkingsregels, VISTA-regels, regels voor verwerking van distributiekanalen | De steun geplande, maar zal bij vraag-tijd eerder dan tijdens gegevensinzameling voor flexibelere en retroactieve en niet-destructieve gegevensmanipulaties werken. |
| Projectsjablonen | Er is steun gepland. |
| Real-time rapportage | Er is steun gepland. |
| Segment-IQ | Er is steun gepland. |

{style=&quot;table-layout:auto&quot;}

## Steun nog niet gepland

| Functie | Notities |
| --- | --- |
| Activity Map | De steun is nog niet gepland. |
| Advertising Cloud | De steun is nog niet gepland. |
| Valutaconversie | De steun is nog niet gepland. |
| Gegevensfeeds | De steun is nog niet gepland. |
| Samenvattingsgegevensbronnen | De steun is nog niet gepland. |
| Gegevensbronnen van transactie-id | De steun is nog niet gepland. |

{style=&quot;table-layout:auto&quot;}

## Wordt nooit ondersteund

* Metrische personen met behulp van Cross-Device Coop
* Dashboards voor rapporten en analyses
* Bladwijzers voor rapporten en analyses
* Doelstellingen voor rapporten en analyses
* Mobiele services