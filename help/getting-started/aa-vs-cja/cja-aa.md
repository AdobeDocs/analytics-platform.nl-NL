---
title: Ondersteuning van Customer Journey Analytics-functies
description: Customer Journey Analytics in vergelijking met Adobe Analytics-functies ingesteld.
exl-id: be19aa27-58aa-438d-806c-e27c9a289797
solution: Customer Journey Analytics
feature: Basics
role: User
source-git-commit: 75edfb09e3d2d4673d4c7f86b53eb5a620e77cbc
workflow-type: tm+mt
source-wordcount: '2251'
ht-degree: 1%

---

# Ondersteuning van Customer Journey Analytics-functies

In de volgende tabellen wordt aangegeven welke functies in Adobe Analytics worden ondersteund, gedeeltelijk of niet worden ondersteund in de Customer Journey Analytics en welke functies van Customer Journey Analytics niet worden ondersteund of beschikbaar zijn in Adobe Analytics. Deze lijsten worden na verloop van tijd gewijzigd wanneer functies aan de Customer Journey Analytics worden toegevoegd.

## Volledig ondersteunde functies/componenten {#full-support}

| Adobe Analytics-functie | Opmerkingen over ondersteuning |
| --- | --- |
| Anomalische detectie | Volledige ondersteuning |
| Attribution IQ | Volledige ondersteuning |
| Bodemdetectie | [ Volledige steun ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/bot-detection.html) |
| Berekende cijfers | Volledige ondersteuning. Eventuele bestaande berekende metrische waarden in de traditionele Analysis Workspace worden niet naar de Customer Journey Analytics overgebracht. |
| Kalendergebeurtenissen | Volledige ondersteuning. De gebeurtenissen van de kalender zijn uitgevoerd als [ Annotaties ](/help/components/annotations/overview.md) in Workspace. |
| CSV-download | Volledige ondersteuning |
| Aangepaste kalenders | Volledige ondersteuning |
| Datumvergelijkingen | Volledige ondersteuning |
| Datumbereiken | Alle functionaliteit voor datumbereik wordt ondersteund. |
| Dimensies | Volledige ondersteuning. Customer Journey Analytics gebruikt XDM en ondersteunt onbeperkte afmetingen. Customer Journey Analytics is niet gekoppeld aan de aangepaste eVars of props van traditionele Adobe Analytics. |
| GDPR-verwijdering | Volledige ondersteuning. GDPR wordt nu gecoördineerd met [!UICONTROL Adobe Experience Platform] . Customer Journey Analytics overerft alle gegevenswijzigingen die [!UICONTROL Experience Platform] aanbrengt in onderliggende gegevenssets. |
| Rapportage van optillen en betrouwbaarheid | Volledige steun via [ het paneel van de Experimentatie ](/help/analysis-workspace/c-panels/experimentation.md) |
| Variabelen/List-eigenschappen | Volledige ondersteuning. Customer Journey Analytics gebruikt XDM en ondersteunt onbeperkte tekenreeksarrays die op dezelfde manier kunnen worden gebruikt als listVars. |
| Merchandising-eVars | Volledige steun via [ bindende dimensies en bindende metriek ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html#binding-dimension) |
| Metrics | Volledige steun; de Customer Journey Analytics gebruikt het Model van de Gegevens van de Ervaring (XDM) en steunt onbeperkte metriek en is niet verbonden aan de gebeurtenissen van het douanesucces van Adobe Analytics. Sommige standaardmetriek zijn anders genoemd van Adobe Analytics: Bezoekers = Mensen, Bezoekingen = Sessies, Hits = Gebeurtenissen. |
| Projecten, filters, en berekende metriek van Adobe Analytics aan Customer Journey Analytics migreren | Volledige ondersteuning. |
| Mobiele scorecard/dashboards | Volledige ondersteuning |
| Deelvensters | Volledige ondersteuning voor de volgende deelvensters: Leeg deelvenster, Kenmerken, Vrije vorm, Snelle inzichten en Volgende of vorige item. |
| PDF exporteren | Volledige ondersteuning |
| Projectcursus | Volledige ondersteuning |
| Projectkoppeling | Volledige ondersteuning |
| Tijdverwerking rapporteren | Volledige steun; Customer Journey Analytics baseert zich uitsluitend op de Verwerking van de Tijd van het Rapport. |
| API-toegang rapporteren | Volledige Steun; Beschikbaar door [ Customer Journey Analytics API ](https://developer.adobe.com/cja-apis/docs/). |
| Geplande rapporten/projecten | Volledige ondersteuning |
| Segmenten | Volledige ondersteuning. Nu &quot;Filters&quot; genoemd - merk op dat bestaande segmenten in traditionele Analysis Workspace niet naar Customer Journey Analytics worden overgebracht. |
| Gegevensbronnen op overzichtsniveau | Volledige ondersteuning |
| Virtuele rapportsuites | Volledige ondersteuning. Nu geroepen [ meningen van Gegevens ](/help/data-views/create-dataview.md). |
| Samengestelde cursus virtuele rapportsuite | Volledige ondersteuning. Nu onderdeel van gegevensweergaven. |
| Apparaat, Browser, Referrer, de dimensies van de Technologie | Ondersteund voor zowel ](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html) - gebaseerde datasets van de bron 0} Analytics {en voor datasets die door WebSDK worden geproduceerd. [ Verwijs naar [ documentatie waarop de variabelen van Analytics via ADC ](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics.html) worden gesteund.Als u de gegevensinzameling van SDK van het Web van het Experience Platform gebruikt, worden het Apparaat en de dimensies die op de raadpleging van het Apparaat worden gebaseerd momenteel niet gesteund. Toekomstige steun is gepland. Voor het toevoegen van apparaat en browser raadplegingen aan uw gegevensbestand van SDK van het Web, verwijs naar [ deze documentatie ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html) |
| De invoegtoepassing voor het streamen van media-verzamelingen | Streaming-mediagegevens zijn beschikbaar via de bronaansluiting Analytics als onderdeel van het deelvenster Mediagelijktijdige viewers en het deelvenster Media Playback Time Spent in Workspace. |

{style="table-layout:auto"}

## Op een nieuwe manier ondersteund {#new-support}

| Functie | Notities |
| --- | --- |
| Analyses voor doel (A4T) | De [ integratie tussen Adobe Customer Journey Analytics en Doel ](https://experienceleague.adobe.com/en/docs/target/using/integrate/cja/target-reporting-in-cja) verstrekt krachtige analyse en tijdbesparende hulpmiddelen voor uw optimaliseringsprogramma. |
| Publicatie door het publiek | Wordt ondersteund als de Adobe een licentie heeft voor Customer Data Platform of Journey Optimizer-producten. [ Publiceren van het publiek ](/help/components/audiences/audiences-overview.md) verzendt publiek naar het Profiel van de Klant in real time in Experience Platform. |
| Classificaties | Nu genoemd &quot;de Datasets van de Raadpleging&quot;. Classificaties die worden gebruikt in Analytics kunnen worden geïmporteerd naar het Experience Platform en de Customer Journey Analytics met behulp van de Analytics Classifications Source Connector. De datasets van de opzoekopdracht kunnen ook direct aan Experience Platform worden geupload en beschikbaar in Customer Journey Analytics. |
| Bouwer van classificatieregel | Ondersteund gebruikend [ substrings ](/help/data-views/component-settings/substring.md) in Customer Journey Analytics. Gebruikt tekenreeksmanipulaties in rapporttijd eerder dan raadplegingsdatasets. |
| Aangepaste sessielengte | De lengte van de zitting kan door [ montages van de Zitting ](../../data-views/create-dataview.md#session-settings) in een mening van Gegevens worden gevormd. Zie [ montages van de Zitting ](../../data-views/session-settings.md) voor meer informatie. <br/> het behandelen van mobiele achtergrondgebeurtenissen wordt gesteund door Adobe Experience Platform Mobile SDK. Zie [ Levenscyclus voor Edge Network ](https://developer.adobe.com/client-sdks/documentation/lifecycle-for-edge-network/) voor meer informatie. |
| Omrekening in valuta | Ondersteund als deel van [ die een metrische component ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/format.html#currency) in een gegevensmening formatteren. |
| Klantkenmerken | Deze worden nu &quot;profielgegevenssets&quot; genoemd en worden niet automatisch geïmporteerd uit het Experience Cloud, maar moeten naar het Experience Platform worden geüpload voordat ze beschikbaar zijn in de Customer Journey Analytics. |
| Gegevensfeeds | De uitvoer van gegevens van de eerste generatie van datasets is beschikbaar door de [ Toegang API van de Gegevens van het Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html) en door [ Doelen van het Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html). Deze opties verstrekken gebeurtenis/rijniveau de uitvoer van alle gegevens die in het meer van Gegevens van het Experience Platform worden verzameld of worden opgenomen. Kolommen met gegevens na het proces zijn niet beschikbaar omdat postkolommen bij de query worden berekend. Exporteren van postkolommen is beschikbaar via rapportage. |
| Rapportage van Data Warehouse | [ de Volledige Uitvoer van de Lijst van de Customer Journey Analytics ](/help/analysis-workspace/export/export-cloud.md) is de evolutie van de rapporten van de Data Warehouse in Adobe Analytics, met vele nieuwe, vaak-gevraagde eigenschappen die niet vandaag in Data Warehouse beschikbaar zijn. |
| De ingangen, de Uitgangen, en de tijd bestede dimensies en metriek | Ondersteund (Ingangen en Uitgangen worden nu Sessiebegin en Sessieeinde genoemd) en worden op een iets andere manier berekend. |
| Instellingen voor eVar-persistentie | eVars maken geen deel meer uit van de Customer Journey Analytics. De instellingen voor persistentie maken nu echter deel uit van de gegevensweergave en zijn beschikbaar voor alle dimensies. Onthoud dat persistentie is gebaseerd op de verwerking van de rapporttijd, niet op de verwerking van gegevensverzameling. Dimensionen in gegevensweergaven zijn beperkt tot een maximale persistentie van 90 dagen en ondersteunen geen onbeperkte persistentie. |
| Geoosegmenteringsafmetingen | [ Volledige steun ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html) |
| Op grafiek gebaseerde stitching | Door [ op grafiek-gebaseerde Stitching ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/stitching/overview#graph-based-stitching), kunt u de macht van de identiteitsgrafiek in [ de Dienst van de Identiteit van Adobe Experience Platform gebruiken ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/home) om datasets aan hun aangewezen identiteit op te heffen. |
| IP obfuscatie | Voor klanten die van de Customer Journey Analytics de bronschakelaar van de Analyse gebruiken om gegevens van Adobe Analytics in Customer Journey Analytics te bevolken: IP de montages van de verwarring die in Adobe Analytics worden toegepast stromen door aan uw gegevens van de Customer Journey Analytics. U kunt deze instellingen desgewenst in Adobe Analytics beheren.<p>Voor klanten die van de Customer Journey Analytics SDK gebruiken van het Web van het Experience Platform om gegevens in Platform en Customer Journey Analytics direct te bevolken. U kunt Prep van Gegevens voor de Inzameling van Gegevens in Platform gebruiken om regels te vormen die het IP adres verduisteren dat op de vereisten van uw bedrijf wordt gebaseerd. |
| Marketingkanalen | Wanneer het gebruiken van de bron van Analytics schakelaar, stromen de gegevens van Kanalen van de marketing in Customer Journey Analytics door die schakelaar. De regels van het Kanaal van de marketing worden gevormd in traditionele Adobe Analytics en sommige regels worden niet gesteund. Zie [ Customer Journey Analytics die Kanalen ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/aa-data/marketing-channels.html) op de markt brengt voor meer informatie. <br/> voor implementaties WebSDK, rapport-tijd de verwerkingsregels van het marketingkanaal worden gesteund door [ Afgeleide gebieden ](../../data-views/derived-fields/derived-fields.md). |
| Handelswijzigingsvariabele persistentie | Volledige Steun via [ bindende dimensies en bindende metriek ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html#binding-dimension) |
| Metrische deduplicatie | Nu gevormd op metriek binnen de Mening van Gegevens. De metrische deduplicatie gebeurt op het persoon of zittingsniveau eerder dan de Dataset, de mening van Gegevens, of het niveau van de Verbinding. |
| Nieuwe versus herhaalde sessierapportage | Vroeger verwezenlijkt gebruikend de dimensie van het Aantal van het Bezoek. De nieuwe vs. Herhaal zittingen worden gesteund [ met een terugkijkvenster van 13 maanden ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/data-views/data-views-usecases.html). |
| Verwerkingsregels, VISTA-regels, regels voor verwerking van marketingkanalen | Ondersteund gebruikend de functionaliteit van de Prep van Gegevens van Adobe Experience Platform evenals [ afgeleide gebieden ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/derived-fields.html) voor zowel WebSDK gebaseerde datasets als gegevens van de de bronschakelaar van de Analyse. |
| Variabele voor producten | Binnen het Experience Platform, kunnen de gebruikers een serie van voorwerpen binnen een datasetschema gebruiken om aan dit gebruiksgeval te voldoen. Binnen Customer Journey Analytics, kunnen de klanten om het even welk aantal productvariabelen gebruiken en zijn niet beperkt tot één enkele variabele zoals in Adobe Analytics. |
| Projectdeling | Delen van projecten wordt alleen ondersteund door gebruikers van Customer Journey Analytics - er wordt geen project gedeeld tussen Customer Journey Analytics en de traditionele Analysis Workspace. |
| Report Builder | Ondersteund met een nieuwe Office 365-insteekmodule voor Excel. |
| Gebruikersmachtigingen/besturingselementen voor gegevenstoegang | De Customer Journey Analytics maakt onderscheid tussen [ Adobe Admin Console ](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html) productbeheerders, de beheerders van het productprofiel, en gebruikers. Alleen productbeheerders kunnen verbindingen, projecten, filters of berekende metriek maken/bijwerken/verwijderen die door andere gebruikers zijn gemaakt, terwijl productbeheerders en productprofielbeheerders de weergave Gegevens kunnen bewerken. Er zijn aanvullende gebruikersmachtigingen beschikbaar voor bijvoorbeeld het maken van berekende metriek, filters of annotaties. |
| Visualisaties | Alle Workspace-visualisaties worden ondersteund, met uitzondering van de Kaartweergave. |
| Draaien tussen apparaten en kanalen | Ondersteund voor gebeurtenisgegevenssets die identiteitsgegevens bevatten. Zie [ Plaatsen ](../../stitching/overview.md). |

{style="table-layout:auto"}

## Gedeeltelijke ondersteuning {#partial}

| Functie | Notities |
| --- | --- |
| Deelvensters | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. De deelvensters Segmentvergelijking en Analyse voor Doel (A4T) worden niet ondersteund. |

{style="table-layout:auto"}

## Geen steun, maar gepland {#planned}

| Functie | Notities |
| --- | --- |
| Waarschuwingen | Er is steun gepland. |
| Bijdrage-analyse | Er is steun gepland. |
| Projectsjablonen | Er is steun gepland. |
| Real-time rapportage | Er is steun gepland. |
| Segment-IQ | Er is steun gepland. |
| Gegevensbronnen van transactie-id | Er is steun gepland. |

{style="table-layout:auto"}

## Geen ondersteuning, nog niet gepland {#not-planned}

| Functie | Notities |
| --- | --- |
| Activity Map | De steun is nog niet gepland. |
| Advertising Cloud | De steun is nog niet gepland. |

{style="table-layout:auto"}

## Wordt nooit ondersteund {#never}

* Metrische personen met behulp van Cross-Device Coop

## Adobe Customer Journey Analytics-functies niet beschikbaar in Adobe Analytics {#cja-not-aa}

De volgende tabel bevat een lijst met functies die beschikbaar zijn in de Customer Journey Analytics, maar die niet worden ondersteund in Adobe Analytics.

| Functie | Meer details |
| --- | --- |
| Mogelijkheid om gegevenssets te combineren (zoals Adobe Analytics-rapportenreeksen) | De Customer Journey Analytics staat u toe om gegevens ](/help/connections/combined-dataset.md) van veelvoudige rapportreeksen te combineren [ alsof zij één enkele rapportreeks in Adobe Analytics waren. |
| Opslag voor alle soorten gegevens | Customer Journey Analytics wordt gecombineerd met de capaciteit van het Experience Platform om allerlei gegevensschema&#39;s en types te houden. Gebruikend [ Model van de Gegevens van de Ervaring (XDM) ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl), kunnen de gegevens uniform worden vertegenwoordigd en georganiseerd, klaar voor combinatie en exploratie. Adobe Analytics is hoofdzakelijk geconcentreerd op Web en mobiele analysegegevens met sommige mogelijkheden om gegevens [ in te voeren ](https://experienceleague.adobe.com/docs/analytics/import/home.html). |
| Apparaatanalyse | Customer Journey Analytics steunt de naadloze combinatie apparaat-specifieke datasets van unauthenticated en voor authentiek verklaarde zittingen. De Customer Journey Analytics biedt aan om historische gegevens aan bekende apparaten terug te vullen. In Adobe Analytics is deze mogelijkheid beperkt tot één rapportsuite en het gebruik van een apparaatgrafiek. |
| Verbeteringen voor Dimension | Customer Journey Analytics biedt meer flexibiliteit bij het gebruik van dimensies: <ul><li>**op numerieke basis gebaseerde afmetingen van de Douane**: [ creeer uw eigen op numeriek-gebaseerde afmetingen binnen een gegevensmening ](/help/data-views/create-dataview.md#components).</li><li>**Sort op koord-gebaseerde afmetingen**: [ Sort op koord-gebaseerde afmetingen alfabetisch in een vrije vormlijst.](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md#sort-tables) </li></ul><p>In Adobe Analytics waren slechts enkele ingebouwde numerieke afmetingen beschikbaar en sorteren op tekenreeksgebaseerde afmetingen was niet mogelijk.</p> |
| Afgeleide velden | [ Voortgekomen gebieden ](/help/data-views/derived-fields/derived-fields.md) staan voor rapport-tijd transformaties aan uw gegevens toe. Gegevens kunnen tijdens de vlucht worden gecombineerd, gecorrigeerd of gemaakt en worden met terugwerkende kracht toegepast op alle rapporten. |
| Uitgebreide opties voor beveiliging en privacy - HIPAA-gereedheid | Customer Journey Analytics is HIPAA klaar en biedt [ extra veiligheidsopties ](/help/privacy/cmk.md) voor regelgevende naleving aan. Adobe Analytics is niet klaar voor HIPAA. |
| Experimentatieanalyse | De Customer Journey Analytics kan [ de lift en het vertrouwen van om het even welk experiment ](/help/analysis-workspace/c-panels/experimentation.md) van om het even welke gegevensbron evalueren die als deel van een verbinding wordt bepaald. Deze evaluatie staat u toe om oorzaak-en-effect verhoudingen tussen klanteninteractie te begrijpen die om het even welk kanaal overspannen. Analyse is beperkt tot experimentatieanalyse via A4T. |
| Voorspelling | [ die ](/help/analysis-workspace/c-forecast/forecasting.md) voorspelt is een vermogen AI/ML dat een statistische voorspelling voor op tijd-reeksen betrekking hebbende gegevens omvat die op de historische gegevens worden gebaseerd die reeds in Customer Journey Analytics bestaan. Prognoses kunnen in vrije-vormlijsten en lijngrafiekvisualisaties verschijnen. |
| Analyse met instructies | [ Geleide analyse ](/help/guided-analysis/overview.md) is een rapporteringsformaat dat gebruikers toestaat om hun gegevensbehoeften snel zelf-te dienen zodat zij hoogstaande inzichten kunnen snel krijgen en meer gegeven-gedreven besluiten nemen. De geleide analyse maakt deel uit van Adobe Product Analytics, een toevoeging aan Customer Journey Analytics. |
| Intelligente bijschriften | Intelligente bijschriften maken gebruik van geavanceerde Machine Learning en Generative AI om waardevolle natuurlijke taalinzichten te bieden voor Workspace-visualisaties. De aanvankelijke versie verstrekt auto-geproduceerde inzichten voor de [ visualisatie van de Lijn ](/help/analysis-workspace/visualizations/line.md). |
| Transformaties in de rapporttijd | [ de meningen van Gegevens ](/help/data-views/data-views.md) in Customer Journey Analytics staan u toe om gegevens van een verbinding verder te interpreteren. U kunt gegevens wijzigen of verwijderen zonder uw implementatie te wijzigen, subtekenreeksen gebruiken om afmetingen te manipuleren, metriek van om het even welke waarde tot stand te brengen, of filtersubtekenreeksen. Al deze transformaties worden niet-destructief uitgevoerd. Adobe Analytics biedt beperkte mogelijkheden via virtuele rapportsuites en aangepaste sessielengte. |
| BI Extension | De [ Uitbreiding van BI ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-usecases/data-export/bi-extension) laat u CJA direct met populaire BI visualiseringshulpmiddelen zoals PowerBI of Tableau verbinden. Door deze extensie te gebruiken, kunt u uw BI-rapporten precies laten overeenkomen met wat u ziet in Analysis Workspace en andere CJA-rapportageinterfaces. Dit is een veel gemakkelijkere manier om BI rapportering voor CJA zonder de behoefte te krijgen om rapporten/metriek van ruwe gegevens opnieuw te maken. |
| SQL-toegang | Met de optie Data Distiller kan Customer Journey Analytics de beperkingen verwijderen van gegevens die zijn verzameld bij de backendverwerking van de Adobe. U kunt uw gegevens met SQL wijzigen, waarden en datasets tot stand brengen uniek aan uw zaken en blijven onderzoeken. Analytics biedt geen ondersteuning voor SQL-toegang tot de bijbehorende gegevens. |
| Stiksel | [ Stitching ](/help/stitching/overview.md) is een krachtige eigenschap die de geschiktheid van een gebeurtenisdataset voor kanaalanalyse opheft. De analyse van het dwars-kanaal is een belangrijkste gebruiksgeval dat de Customer Journey Analytics kan behandelen, toestaand u om rapporten over veelvoudige datasets van verschillende kanalen naadloos te combineren en in werking te stellen, die op een gemeenschappelijke herkennings (persoonidentiteitskaart) worden gebaseerd. |
| Onbeperkte klantdimensies en metriek | De afmetingen van de Customer Journey Analytics zijn onbeperkt. Waarden kunnen numeriek, tekst, objecten, lijsten of mengsels van allemaal zijn. Dimensionen kunnen worden genest of hiërarchisch. <br/> door contrast, steunt Adobe Analytics tot een maximum van 75 steunen en 250 eVars. |
| Onbeperkte unieke waarden | Customer Journey Analytics ondersteunt onbeperkte unieke waarden of dimensie-items die binnen één dimensie kunnen worden gerapporteerd.<p>Er zijn geen [ kardinaliteitsgrenzen op een dimensie ](/help/components/dimensions/high-cardinality.md), die voor om het even welke unieke waarde toestaat om te verschijnen en worden geteld.</p><p>Met deze methode worden rapportage- en analysebeperkingen die kunnen bestaan bij grootschalige Adobe Analytics-implementaties, verwijderd. Dit leidt tot [!UICONTROL Low Traffic] -labels.</p><p>In Customer Journey Analytics, is het mogelijk om een [!UICONTROL Uniques Exceeded] etiket te zien, maar deze komen veel minder vaak voor en kunnen worden verlicht door een filter of een segment op de gegevens toe te passen.</p> |

{style="table-layout:auto"}
