---
title: Ondersteuning voor Customer Journey Analytics-functies
description: Customer Journey Analytics-functies vergeleken met Adobe Analytics-functies ingesteld.
exl-id: be19aa27-58aa-438d-806c-e27c9a289797
solution: Customer Journey Analytics
feature: Basics
source-git-commit: 264b5a3d3793ab6531f570d83cbd4fd96bfbd67a
workflow-type: tm+mt
source-wordcount: '2080'
ht-degree: 3%

---

# Ondersteuning voor Adobe Customer Journey Analytics-functies

In de volgende tabellen wordt aangegeven welke functies in Adobe Analytics worden ondersteund, gedeeltelijk of niet worden ondersteund in Customer Journey Analytics en welke functies van Customer Journey Analytics niet worden ondersteund of beschikbaar zijn in Adobe Analytics. Deze lijsten worden na verloop van tijd gewijzigd wanneer functies aan Customer Journey Analytics worden toegevoegd.

## Volledig ondersteunde functies/componenten {#full-support}

| Adobe Analytics-functie | Opmerkingen over ondersteuning |
| --- | --- |
| Anomaliedetectie | Volledige ondersteuning |
| Attribution IQ | Volledige ondersteuning |
| Berekende standaarden | Volledige ondersteuning. Eventuele bestaande berekende metrische waarden in de traditionele Analysis Workspace worden niet naar Customer Journey Analytics geëxporteerd. |
| Kalendergebeurtenissen | Volledige ondersteuning. Kalendergebeurtenissen zijn geïmplementeerd als [Annotaties](/help/components/annotations/overview.md) in Workspace. |
| CSV-download | Volledige ondersteuning |
| Aangepaste kalenders | Volledige ondersteuning |
| Datumvergelijkingen | Volledige ondersteuning |
| Datumbereik | Alle functionaliteit voor datumbereik wordt ondersteund. |
| Dimensies | Volledige ondersteuning. Customer Journey Analytics gebruikt XDM en ondersteunt onbeperkte afmetingen. Customer Journey Analytics is niet gekoppeld aan de aangepaste eVars of props van traditionele Adobe Analytics. |
| GDPR-verwijdering | Volledige ondersteuning; merk op dat GDPR nu wordt afgehandeld in coördinatie met [!UICONTROL Adobe Experience Platform]. Customer Journey Analytics neemt alle wijzigingen in de gegevens over [!UICONTROL Experience Platform] maakt aan onderliggende datasets. |
| Lift and Trust Reporting | Volledige ondersteuning via [Deelvenster Experimentatie](/help/analysis-workspace/c-panels/experimentation.md) |
| Variabelen/lijsteigenschappen weergeven | Volledige ondersteuning. Customer Journey Analytics gebruikt XDM en ondersteunt onbeperkte tekenreeksarrays die op dezelfde manier kunnen worden gebruikt als listVars. |
| Merchandising-eVars | Volledige ondersteuning via [afmetingen binden en metriek binden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html#binding-dimension) |
| Metrics | Volledige steun; Customer Journey Analytics gebruikt het Model van de Gegevens van de Ervaring (XDM) en steunt onbeperkte metriek en is niet verbonden aan de gebeurtenissen van het douanesucces van Adobe Analytics. Sommige standaardmetriek zijn anders genoemd van Adobe Analytics: Bezoekers = Mensen, Bezoekingen = Sessies, Hits = Gebeurtenissen. |
| Mobiel scorebord/dashboards | Volledige ondersteuning |
| Deelvensters | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. |
| PDF exporteren | Volledige ondersteuning |
| Projectcuratie | Volledige ondersteuning |
| Projectkoppeling | Volledige ondersteuning |
| Tijdverwerking rapporteren | Volledige ondersteuning; Customer Journey Analytics is uitsluitend afhankelijk van de rapporttijdverwerking. |
| API-toegang rapporteren | Volledige ondersteuning; beschikbaar via de [CUSTOMER JOURNEY ANALYTICS API](https://developer.adobe.com/cja-apis/docs/). |
| Geplande rapporten/projecten | Volledige ondersteuning |
| Segmenten | Volledige ondersteuning. Nu &quot;Filters&quot; genoemd - merk op dat bestaande segmenten in traditionele Analysis Workspace niet worden overgebracht naar Customer Journey Analytics. |
| Virtuele rapportsuites | Volledige ondersteuning. Wordt nu aangeroepen [Gegevens weergeven](/help/data-views/create-dataview.md). |
| Component Curation van Virtual Report Suite | Volledige ondersteuning. Deel nu van Gegevens. |
| Streaming media-analyse | De mediagegevens zijn beschikbaar via de bronaansluiting Analytics als onderdeel van het deelvenster Mediagelijktijdige viewers en het deelvenster Media Playback Time Spent in Workspace. |

{style="table-layout:auto"}

## Op een nieuwe manier ondersteund {#new-support}

| Functie | Notities |
| --- | --- |
| Publiek publiceren (Segmentpublicatie) | Wordt ondersteund als een licentie wordt verleend voor Adobe Data Platform of Journey Optimizer-producten. [Publiek publiceren](/help/components/audiences/audiences-overview.md) verzendt publiek naar het Profiel van de Klant in real time in Experience Platform. |
| Classificaties | Nu genoemd &quot;de Datasets van de Raadpleging&quot;. Classificaties die in Analytics worden gebruikt, kunnen naar het Experience Platform en de Customer Journey Analytics worden geïmporteerd met behulp van de Bronconnector voor analytische classificaties. De datasets van de opzoekopdracht kunnen ook direct aan Experience Platform worden geupload en beschikbaar in Customer Journey Analytics worden gemaakt. |
| Builder voor classificatieregels | Ondersteund met [subtekenreeksen](/help/data-views/component-settings/substring.md) in Customer Journey Analytics. Gebruikt tekenreeksmanipulaties in rapporttijd eerder dan raadplegingsdatasets. |
| Aangepaste sessie | Aangepaste sessionisatie kan worden geconfigureerd via de [Sessieinstellingen](../../data-views/create-dataview.md#session-settings) in een gegevensweergave. Zie  [Contextbewuste sessies](../../data-views/context-aware-sessions.md) voor meer informatie . <br/>De verwerking van mobiele achtergrondgebeurtenissen wordt ondersteund via de Adobe Experience Platform Mobile SDK. Zie [Levenscyclus voor Edge Network](https://developer.adobe.com/client-sdks/documentation/lifecycle-for-edge-network/) voor meer informatie . |
| Valutaconversie | Ondersteund als onderdeel van [het formatteren van een metrische component](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/format.html?lang=en#currency) in een gegevensweergave. |
| Handelswijzigingsvariabele persistentie | Volledige ondersteuning via [afmetingen binden en metriek binden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html#binding-dimension) |
| Klantkenmerken | Deze worden nu &quot;profielgegevenssets&quot; genoemd en worden niet automatisch geïmporteerd uit Experience Cloud, maar moeten naar het Experience Platform worden geüpload voordat ze beschikbaar zijn in Customer Journey Analytics. |
| Gegevensfeeds | De uitvoer van gegevens van de eerste generatie van datasets is beschikbaar door [API voor gegevenstoegang van Experience Platforms](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=en) en via [Experience Platform Doelen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en). Deze opties verstrekken gebeurtenis/rijniveau de uitvoer van alle gegevens die in het meer van Gegevens van het Experience Platform worden verzameld of worden opgenomen. Kolommen met gegevens na het proces zijn niet beschikbaar omdat postkolommen bij de query worden berekend. Exporteren van postkolommen is beschikbaar via rapportage. |
| Metrische deduplicatie | Nu gevormd op metriek binnen de Mening van Gegevens. De metrische deduplicatie gebeurt op het persoon of zittingsniveau eerder dan de Dataset, de Mening van Gegevens, of het niveau van de Verbinding. |
| De ingangen, de Uitgangen, en de tijd bestede dimensies en metriek | Ondersteund (Ingangen en Uitgangen worden nu Sessiebegin en Sessieeinde genoemd) en worden op een iets andere manier berekend. |
| Instellingen voor eVar-persistentie | eVars maken geen deel meer uit van Customer Journey Analytics. De instellingen voor persistentie maken nu echter deel uit van de gegevensweergave en zijn beschikbaar voor alle dimensies. Onthoud dat persistentie is gebaseerd op de verwerking van de rapporttijd, niet op de verwerking van gegevensverzameling. Dimension in gegevensweergaven zijn beperkt tot een maximale persistentie van 90 dagen en ondersteunen geen onbeperkte persistentie. |
| IP Obfuscatie | Voor Customer Journey Analytics-klanten die de Analytics-bronconnector gebruiken om gegevens van Adobe Analytics in Customer Journey Analytics te vullen: IP-verduisteringsinstellingen die in Adobe Analytics zijn toegepast, worden doorgevoerd in uw Customer Journey Analytics-gegevens. U kunt deze instellingen desgewenst in Adobe Analytics beheren.<p>Voor Customer Journey Analytics klanten die SDK van het Web van het Experience Platform gebruiken om gegevens in Platform en Customer Journey Analytics direct te bevolken. U kunt Prep van Gegevens voor de Inzameling van Gegevens in Platform gebruiken om regels te vormen die het IP adres verduisteren dat op de vereisten van uw bedrijf wordt gebaseerd. |
| Nieuwe versus herhaalde sessierapportage | Vroeger verwezenlijkt gebruikend de dimensie van het Aantal van het Bezoek. Nieuwe sessies vs. herhalingssessies worden ondersteund [met een terugzoekvenster van 13 maanden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/data-views/data-views-usecases.html?lang=en). |
| Productvariabele | Binnen het Experience Platform, kunnen de gebruikers serie van de typegebieden van Objecten binnen een datasetschema gebruiken om aan dit gebruiksgeval te voldoen. Binnen Customer Journey Analytics kunnen klanten een willekeurig aantal productvariabelen gebruiken en zijn ze niet beperkt tot één variabele, zoals in Adobe Analytics. |
| Project delen | Het delen van projecten wordt alleen ondersteund door gebruikers van Customer Journey Analytics. Er wordt geen project gedeeld tussen Customer Journey Analytics en de traditionele Analysis Workspace. |
| Visualisaties | Alle visualisaties worden ondersteund, behalve voor de visualisatie Kaart. |
| Report Builder (Excel-plug-in) | Ondersteund met een nieuwe Office 365-insteekmodule voor Excel. |
| Gebruikersmachtigingen/Toegangsbeheer voor gegevens | Customer Journey Analytics maakt onderscheid tussen [Adobe Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html) productbeheerders, productprofielbeheerders en gebruikers. Alleen productbeheerders kunnen verbindingen, projecten, filters of berekende metriek maken/bijwerken/verwijderen die door andere gebruikers zijn gemaakt, terwijl productbeheerders en productprofielbeheerders de weergave van gegevens kunnen bewerken. Er zijn extra gebruikersmachtigingen beschikbaar voor bijvoorbeeld het maken van berekende metriek, filter of annotaties. |
| Verwerkingsregels, VISTA-regels, regels voor verwerking van distributiekanalen | Ondersteund met Adobe Experience Platform Data Prep-functionaliteit voor zowel WebSDK-gegevenssets als gegevens van de gegevensbronconnector van Analytics. |
| Marketingkanalen | Wanneer het gebruiken van de Bron van Analytics schakelaar, stromen de gegevens van Kanalen van de marketing in Customer Journey Analytics door die schakelaar. De regels van het Kanaal van de marketing worden gevormd in traditionele Adobe Analytics en sommige regels worden niet gesteund. Zie voor meer informatie [Customer Journey Analytics Marketing Channel-documentatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/aa-data/marketing-channels.html). <br/>Voor implementaties WebSDK, rapport-tijd de verwerkingsregels van de afzetkanalen worden gesteund door [Afgeleide velden](../../data-views/derived-fields/derived-fields.md). |

{style="table-layout:auto"}

## Gedeeltelijke ondersteuning {#partial}

| Functie | Notities |
| --- | --- |
| Draaien tussen apparaten en kanalen | Ondersteund voor gegevenssets die rechtstreeks identiteitsgegevens bevatten (ook wel &quot;op het veld gebaseerde&quot; stitching genoemd). Grafiekgebaseerde stitching wordt nog niet ondersteund, maar gepland. Zie [Stiksel](../../stitching/overview.md). |
| Bot filteren | Voor [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html)Op gegevenssets gebaseerde gegevenssets worden beide gefilterd. De algemene bot filtering logica voor andere datasets wordt niet uitgevoerd door de [!UICONTROL Experience Platform] of Customer Journey Analytics. |
| Apparaat, Browser, Referrer, de dimensies van de Technologie | Ondersteund voor [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html)- gebaseerde datasets. Zie [documentatie over de door ADC ondersteunde analytische variabelen](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics.html?lang=en).<p>Als u de gegevensinzameling van SDK van het Web van het Experience Platform gebruikt, worden het Apparaat en de dimensies die op de raadpleging van het Apparaat worden gebaseerd momenteel niet gesteund. Toekomstige steun is gepland. |
| GeoSegmentation-afmetingen | Alle GeoSegmentation/geography die in Adobe Analytics wordt verzameld stroomt in Customer Journey Analytics door [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html). Implementaties die de bronschakelaar van Analytics niet gebruiken, maar zich op SDK van het Web van Experience Platforms voor digitale gegevensinzameling baseren, kunnen gebruiken [Experience Edge Geo Lookup Service](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=en). |
| Deelvensters | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. De deelvensters Segmentvergelijking en Analyse voor Doel (A4T) worden niet ondersteund. |
| Verwerkingsregels | Voor de bron van Analytics op schakelaar-gebaseerde datasets, worden de verwerkingsregels nog toegepast. [Mogelijkheden voor gegevensuitwisseling in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html) kan ook worden gebruikt als vervanging voor verwerkingsregels voor gegevens die rechtstreeks naar het Platform gaan. |
| A4T | De gedeeltelijke steun wordt verleend door gebieden in [Bronconnector voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html). Ondersteuning voor A4T-vriendelijke namen op doelactiviteiten en -ervaringen is gepland. |

{style="table-layout:auto"}

## Geen steun, maar gepland {#planned}

| Functie | Notities |
| --- | --- |
| Waarschuwingen | Er is steun gepland. |
| Contributieanalyse | Er is steun gepland. |
| Rapportage Data Warehouse | Ondersteuning is gepland via de Analysis Workspace-interface. Adobe Experience Platform [[!UICONTROL Query Service]](<https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl>) verstrekt ook een interface voor deze gebruiksgevallen in Customer Journey Analytics. |
| ID-instelling via apparaatgrafiek | Er is steun gepland. |
| Projectsjablonen | Er is steun gepland. |
| Real-time rapportage | Er is steun gepland. |
| Segment-IQ | Er is steun gepland. |
| Gegevensbronnen van transactie-id | Er is steun gepland. |
| Projecten/filters/berekende gegevens migreren van Adobe Analytics naar Customer Journey Analytics | Er is steun gepland. |
| Gegevensbronnen op overzichtsniveau | Er is steun gepland. |

{style="table-layout:auto"}

## Geen ondersteuning, nog niet gepland {#not-planned}

| Functie | Notities |
| --- | --- |
| Activity Map | De steun is nog niet gepland. |
| Advertising Cloud | De steun is nog niet gepland. |

{style="table-layout:auto"}

## Nooit ondersteund {#never}

* Metrische personen met behulp van Cross-Device Coop
* Dashboards voor rapporten en analyses
* Bladwijzers voor rapporten en analyses
* Doelstellingen voor rapporten en analyses

## Adobe Customer Journey Analytics-functies niet beschikbaar in Adobe Analytics {#cja-not-aa}

De volgende tabel bevat een lijst met functies die beschikbaar zijn in Customer Journey Analytics, maar die niet worden ondersteund in Adobe Analytics.

| Functie | Meer details |
| --- | --- |
| Opslag voor alle soorten gegevens | Customer Journey Analytics wordt gecombineerd met de capaciteit van het Experience Platform om allerlei gegevensschema&#39;s en types te houden. Gebruiken [Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl)Gegevens kunnen op uniforme wijze worden weergegeven en geordend, klaar voor combinatie en onderzoek. Adobe Analytics is vooral gericht op analytische gegevens voor het web en mobiele apparaten en beschikt over enkele mogelijkheden om [importgegevens](https://experienceleague.adobe.com/docs/analytics/import/home.html). |
| Onbeperkte Dimension en cijfers van klanten | De Customer Journey Analytics-afmetingen zijn onbeperkt; waarden kunnen numeriek, tekst, objecten, lijsten of mengsels van allemaal zijn. Dimension kunnen genest of hiërarchisch zijn. Analytics ondersteunt maximaal 75 props en 250 eVars. |
| Onbeperkte kardinaliteit / unieke waarden | Customer Journey Analytics ondersteunt onbeperkte unieke waarden of dimensie-items die binnen één dimensie kunnen worden gerapporteerd. Adobe Analytics is beperkt tot 500.000 unieke waarden. De onbeperkte unieke waarden of dimensies verwijderen de rapportage- en analysebeperkingen die momenteel bestaan met grootschalige analytische implementatie. |
| Tijdtransformaties rapporteren | De Transformaties van de Tijd van het rapport (beter gekend als de Mening van Gegevens) in Customer Journey Analytics staat u toe om gegevens van een verbinding verder te interpreteren. U kunt gegevens wijzigen of verwijderen zonder deze opnieuw te implementeren; subtekenreeksen gebruiken om afmetingen te manipuleren; metriek maken op basis van een willekeurige waarde; subtekenreeksen filteren. Transformatie wordt allemaal niet-destructief uitgevoerd. Adobe Analytics biedt beperkte mogelijkheden door middel van virtuele rapportsuites en sessionisatie. |
| Experimentatieanalyse | Customer Journey Analytics kan de lift en het vertrouwen evalueren van experimenten vanuit elke gegevensbron die is gedefinieerd als onderdeel van een verbinding. Deze evaluatie staat u toe om oorzaak-en-effect verhoudingen tussen klanteninteractie te begrijpen die om het even welk kanaal overspannen. Analytics is beperkt tot experimentatieanalyses via de integratie Analytics for Target (A4T). |
| Cross-device Analytics | Customer Journey Analytics steunt de naadloze combinatie apparaat-specifieke datasets van unauthenticated en voor authentiek verklaarde zittingen. Customer Journey Analytics biedt aan back-up te maken van historische gegevens op bekende apparaten. In Analytics, is dit vermogen beperkt tot één enkele rapportreeks en het gebruik van een apparatengrafiek. |
| SQL Access | Met de optie Gegevens-Distiller kan Customer Journey Analytics gegevens die zijn verzameld op Adobe backend-verwerking verwijderen. U kunt uw gegevens met SQL wijzigen, waarden en datasets tot stand brengen uniek aan uw zaken en blijven onderzoeken. Analytics biedt geen ondersteuning voor SQL-toegang tot de bijbehorende gegevens. |
| Uitgebreide beveiligings- en privacyopties - HIPAA-gereedheid | Customer Journey Analytics is HIPAA klaar en biedt extra veiligheidsopties voor regelnaleving aan. Adobe Analytics is niet klaar voor HIPAA. |

{style="table-layout:auto"}
