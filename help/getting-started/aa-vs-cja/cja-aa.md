---
title: Ondersteuning voor Customer Journey Analytics-functies
description: Customer Journey Analytics-functies vergeleken met Adobe Analytics-functies ingesteld.
exl-id: be19aa27-58aa-438d-806c-e27c9a289797
solution: Customer Journey Analytics
feature: Basics
role: User
source-git-commit: c526531206887acf7c750c8759d4eec5dd24935f
workflow-type: tm+mt
source-wordcount: '2478'
ht-degree: 1%

---

# Ondersteuning voor Customer Journey Analytics-functies

In de volgende tabellen wordt aangegeven welke functies uniek zijn voor Customer Journey Analytics en welke Adobe Analytics-functies worden ondersteund, gedeeltelijk of niet ondersteund in Customer Journey Analytics. Deze lijsten worden na verloop van tijd gewijzigd wanneer functies aan Customer Journey Analytics worden toegevoegd.

## Functies die uniek zijn voor Adobe Customer Journey Analytics {#cja-not-aa}

De volgende tabel bevat een lijst met functies die beschikbaar zijn in Customer Journey Analytics, maar die niet worden ondersteund in Adobe Analytics.

| Functie | Meer details |
| --- | --- |
| **Mogelijkheid om datasets (zoals het rapportreeksen van Adobe Analytics) te combineren** | Customer Journey Analytics staat u toe om gegevens [&#128279;](/help/connections/combined-dataset.md) van veelvoudige rapportreeksen te combineren  alsof zij één enkele rapportreeks in Adobe Analytics waren. |
| **Opname voor om het even welk soort gegevens** | Customer Journey Analytics wordt gecombineerd met de mogelijkheid van Experience Platform om allerlei gegevensschema&#39;s en -typen te bevatten. Gebruikend [ Model van de Gegevens van de Ervaring (XDM) ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl), kunnen de gegevens uniform worden vertegenwoordigd en georganiseerd, klaar voor combinatie en exploratie. Adobe Analytics is hoofdzakelijk geconcentreerd op Web en mobiele analysegegevens met sommige mogelijkheden om gegevens [ in te voeren ](https://experienceleague.adobe.com/docs/analytics/import/home.html?lang=nl-NL). |
| **BI Uitbreiding** | De [ Uitbreiding van BI ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-usecases/data-export/bi-extension) laat u CJA direct met populaire hulpmiddelen van de BBI visualisatie zoals PowerBI of Tableau verbinden. Door deze extensie te gebruiken, kunt u uw BI-rapporten precies laten overeenkomen met wat u ziet in Analysis Workspace en andere CJA-rapportageinterfaces. Dit is een veel gemakkelijkere manier om BI rapportering voor CJA te krijgen zonder de behoefte om rapporten/metriek van ruwe gegevens opnieuw te maken. |
| **Content Analytics** | [ Content Analytics ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/content-analytics/content-analytics) helpt marketers begrijpen hoe de inhoud de belangrijkste prestatiesindicatoren beïnvloedt die een zaken heeft bepaald. Naast de gedragsgegevens verzamelt Content Analytics gegevens over hoe inhoud wordt verbruikt en hoe inhoud invloed heeft. |
| **dwars-ApparaatAnalytics** | Customer Journey Analytics ondersteunt de naadloze combinatie van apparaatspecifieke gegevenssets van niet-geverifieerde en geverifieerde sessies. Customer Journey Analytics biedt back-ups van historische gegevens aan bekende apparaten. In Adobe Analytics is deze mogelijkheid beperkt tot één rapportsuite en het gebruik van een apparaatgrafiek. |
| **de verhogingen van Dimension** | Customer Journey Analytics biedt meer flexibiliteit bij het gebruik van dimensies: <ul><li>**op numerieke basis gebaseerde afmetingen van de Douane**: [ creeer uw eigen op numeriek-gebaseerde afmetingen binnen een gegevensmening ](/help/data-views/create-dataview.md#components).</li><li>**Sort op koord-gebaseerde afmetingen**: [ Sort op koord-gebaseerde afmetingen alfabetisch in een vrije vormlijst.](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md#sort-tables) </li></ul><p>In Adobe Analytics waren slechts enkele ingebouwde numerieke afmetingen beschikbaar en sorteren op tekenreeksgebaseerde afmetingen was niet mogelijk.</p> |
| **Voortgekomen Gebieden** | [ Voortgekomen gebieden ](/help/data-views/derived-fields/derived-fields.md) staan voor rapport-tijd transformaties aan uw gegevens toe. Gegevens kunnen tijdens de vlucht worden gecombineerd, gecorrigeerd of gemaakt en deze transformaties zijn met terugwerkende kracht van toepassing op alle rapporten. |
| **Verbeterde veiligheid en privacyopties** - de gereedheid van HIPAA | Customer Journey Analytics is HIPAA klaar en biedt [ extra veiligheidsopties ](/help/privacy/cmk.md) voor regelgevende naleving aan. Adobe Analytics is niet klaar voor HIPAA. |
| **de analyse van de Experimentatie** | Customer Journey Analytics kan [ de lift en het vertrouwen van om het even welk experiment ](/help/analysis-workspace/c-panels/experimentation.md) van om het even welke gegevensbron evalueren die als deel van een verbinding wordt bepaald. Deze evaluatie staat u toe om oorzaak-en-effect verhoudingen tussen klanteninteractie te begrijpen die om het even welk kanaal overspannen. Analyse is beperkt tot experimentatieanalyse via A4T. |
| **Voorspelling** | [ die ](/help/analysis-workspace/c-forecast/forecasting.md) voorspelt is een vermogen AI/ML dat een statistische voorspelling voor op tijd-reeksen betrekking hebbende gegevens omvat die op de historische gegevens worden gebaseerd die reeds in Customer Journey Analytics bestaan. Prognoses kunnen in vrije-vormlijsten en lijngrafiekvisualisaties verschijnen. |
| **Geleide analyse** | [ Geleide analyse ](/help/guided-analysis/overview.md) laat gebruikers toe om hoogkwalitatieve gegevens en inzichten over de klantenreis door geleide werkschema&#39;s te dienen, die op de dwars-kanaalgegevens van Customer Journey Analytics worden voortgebouwd. |
| **Intelligente Bijschriften** | [ Intelligente titels ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) gebruiken het Geavanceerde Leren van de Machine en Generatieve AI om waardevolle natuurlijk-taalinzichten voor Workspace visualisaties te verstrekken. Intelligente bijschriften worden ondersteund voor de volgende visualisaties: Lijn, Meerdere regels, Staaf, Horizontale balk, Donut, Gebied, Stroom en Fallout. |
| **Canvas van de Reis** | [ het canvas van de Reis ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/visualizations/journey-canvas/journey-canvas?lang=en) is een visualisatie in de werkruimte van de Analyse die u toestaat om te analyseren hoe de mensen door of uit een bepaalde reis te werk gaan vallen. |
| **Gebruik van het Product** | [ het gebruik van het Product ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/tools/product-usage/usage-overview) toont u hoe uw organisatie Customer Journey Analytics gebruikt. |
| **rapport-tijd transformaties** | [ de meningen van Gegevens ](/help/data-views/data-views.md) in Customer Journey Analytics staan u toe om gegevens van een verbinding verder te interpreteren. U kunt gegevens wijzigen of verwijderen zonder uw implementatie te wijzigen, subtekenreeksen gebruiken om afmetingen te manipuleren, metriek van om het even welke waarde tot stand te brengen, of filtersubtekenreeksen. Al deze transformaties worden niet-destructief uitgevoerd. Adobe Analytics biedt beperkte mogelijkheden via virtuele rapportsuites en aangepaste sessielengte. |
| **Gedeelde metriek en dimensies over gegevensmeningen** | Staat u toe om dimensie en metrische montages over veelvoudige gegevensmeningen [&#128279;](/help/data-views/shared-metrics-dimensions/smd-overview.md) toe te passen.  Wijzigingen in een gedeelde dimensie of metrische waarde zijn van toepassing op alle instanties van die dimensie of metrisch in alle toepasselijke gegevensweergaven. |
| **SQL toegang** | Met de optie Data Distiller kan Customer Journey Analytics de beperkingen verwijderen van gegevens die zijn verzameld bij Adobe-backendverwerking. U kunt uw gegevens met SQL wijzigen, waarden en datasets tot stand brengen uniek aan uw zaken en blijven onderzoeken. Analytics biedt geen ondersteuning voor SQL-toegang tot de bijbehorende gegevens. |
| **Stitching** | [ Stitching ](/help/stitching/overview.md) is een krachtige eigenschap die de geschiktheid van een gebeurtenisdataset voor kanaalanalyse opheft. Kanaaloverschrijdende analyse is een belangrijkste gebruikscase die Customer Journey Analytics kan behandelen, die u toestaat om rapporten over veelvoudige datasets van verschillende kanalen naadloos te combineren en in werking te stellen, die op een gemeenschappelijke herkennings (persoon ID) wordt gebaseerd. |
| **Malplaatjes in Adobe Journey Optimizer** | Pas de nieuwe rapporteringsinterface in Adobe Journey Optimizer aan door a [ malplaatje ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/templates/create-templates?lang=en) in Customer Journey Analytics te creëren of uit te geven, dan sparen het malplaatje dat op de pagina van Rapporten in Journey Optimizer moet worden gebruikt. |
| **Onbeperkte klantendimensies en metriek** | Customer Journey Analytics-afmetingen zijn onbeperkt; waarden kunnen numeriek, tekst, objecten, lijsten of mengsels van allemaal zijn. Dimensies kunnen genest of hiërarchisch zijn. <br/> door contrast, steunt Adobe Analytics tot een maximum van 75 steunen en 250 eVars. |
| **Onbeperkte unieke waarden** | Customer Journey Analytics biedt ondersteuning voor onbeperkte unieke waarden of dimensie-items die binnen één dimensie kunnen worden gerapporteerd.<p>Er zijn geen [ kardinaliteitsgrenzen op een dimensie ](/help/components/dimensions/high-cardinality.md), die voor om het even welke unieke waarde toestaat om te verschijnen en worden geteld.</p><p>Met deze methode worden rapportage- en analysebeperkingen die kunnen bestaan bij grootschalige Adobe Analytics-implementaties, verwijderd. Dit leidt tot [!UICONTROL Low Traffic] -labels.</p><p>In Customer Journey Analytics is het mogelijk om een label [!UICONTROL Uniques Exceeded] te zien, maar deze komen veel minder vaak voor en kunnen worden beperkt door een segment op de gegevens toe te passen.</p> |

## Volledig ondersteunde Adobe Analytics-functies/onderdelen {#full-support}

| Adobe Analytics-functie | Opmerkingen over CJA-ondersteuning |
| --- | --- |
| **Anomaly opsporing** | Volledige ondersteuning |
| **overdracht van Activa** | Volledige ondersteuning |
| **Attribution IQ** | Volledige ondersteuning |
| **Bot opsporing** | [ Volledige steun ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/bot-detection.html?lang=nl-NL) |
| **Berekende standaarden** | Volledige ondersteuning. Eventuele bestaande berekende metrische waarden in de traditionele Analysis Workspace worden niet naar Customer Journey Analytics geëxporteerd. |
| **Kalendergebeurtenissen** | Volledige ondersteuning. De gebeurtenissen van de kalender zijn uitgevoerd als [ Annotaties ](/help/components/annotations/overview.md) in Workspace. |
| **download CSV** | Volledige ondersteuning |
| **Kalenders van de Douane** | Volledige ondersteuning |
| **vergelijkingen van de Datum** | Volledige ondersteuning |
| **waaiers van de Datum** | Alle functionaliteit voor datumbereik wordt ondersteund. |
| **Dimensies** | Volledige ondersteuning. Customer Journey Analytics gebruikt XDM en ondersteunt onbeperkte afmetingen. Customer Journey Analytics is niet gekoppeld aan de aangepaste eVars of props van traditionele Adobe Analytics. |
| **GDPR schrapping** | Volledige ondersteuning. GDPR wordt nu gecoördineerd met [!UICONTROL Adobe Experience Platform] . Customer Journey Analytics overerft alle gegevenswijzigingen die [!UICONTROL Experience Platform] aanbrengt in de onderliggende gegevenssets. |
| **Ophef en vertrouwen rapporterend** | Volledige steun via [ het paneel van de Experimentatie ](/help/analysis-workspace/c-panels/experimentation.md) |
| **variabelen van de Lijst/Props van de Lijst** | Volledige ondersteuning. Customer Journey Analytics gebruikt XDM en ondersteunt onbeperkte tekenreeksarrays die op dezelfde manier kunnen worden gebruikt als listVars. |
| **Merchandising Vars** | Volledige steun via [ bindende dimensies en bindende metriek ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html?lang=nl-NL#binding-dimension) |
| **Cijfers** | Volledige ondersteuning; Customer Journey Analytics gebruikt het Experience Data Model (XDM) en ondersteunt onbeperkte metriek en is niet gekoppeld aan de aangepaste succesgebeurtenissen van Adobe Analytics. Sommige standaardmetriek zijn anders genoemd van Adobe Analytics: Bezoekers = Mensen, Bezoekingen = Sessies, Hits = Gebeurtenissen. |
| **migrerende projecten, segmenten, en berekende metriek van Adobe Analytics aan Customer Journey Analytics** | Volledige ondersteuning. |
| **Mobiele scorecard/dashboards** | Volledige ondersteuning |
| **Panelen** | Volledige ondersteuning voor de volgende deelvensters: Leeg deelvenster, Kenmerken, Vrije vorm, Snelle inzichten en Volgende of vorige item. |
| **de uitvoer van PDF** | Volledige ondersteuning |
| **de curatie van het Project** | Volledige ondersteuning |
| **Project het verbinden** | Volledige ondersteuning |
| **malplaatjes van het Product** | Omvat [ pre-gebouwde malplaatjes ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/templates/use-templates) en [ malplaatjes van het Bedrijf ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/templates/create-templates#access-a-company-template). |
| **Verwerking rapportduur** | Volledige ondersteuning; Customer Journey Analytics is uitsluitend afhankelijk van de rapporttijdverwerking. |
| **Meldend API toegang** | Volledige Steun; Beschikbaar door [ Customer Journey Analytics API ](https://developer.adobe.com/cja-apis/docs/). |
| **Geplande rapporten/projecten** | Volledige ondersteuning |
| **Segmenten** | Volledige ondersteuning. (voorheen &quot;Filters&quot; genoemd.) |
| **het stromen de Inzameling van Media** | Streaming-mediagegevens zijn beschikbaar via de bronaansluiting Analytics als onderdeel van het deelvenster Mediagelijktijdige viewers en het deelvenster Media Playback Time Spent in Workspace. |
| **Summiere-vlakke gegevensbronnen** | Volledige ondersteuning |
| **Virtuele rapportsuites** | Volledige ondersteuning. Nu geroepen [ meningen van Gegevens ](/help/data-views/create-dataview.md). |
| **Virtuele de componentencuratie van de rapportsuite** | Volledige ondersteuning. Nu onderdeel van gegevensweergaven. |
| **Apparaat, Browser, Referrer, de dimensies van de Technologie** | Ondersteund voor zowel [&#128279;](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=nl-NL) - gebaseerde datasets van de bron 0&rbrace; Analytics &lbrace;en voor datasets die door WebSDK worden geproduceerd.  Verwijs naar [ documentatie waarop de variabelen van Analytics via ADC ](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics.html?lang=nl-NL) worden gesteund. Als u Experience Platform Web SDK-gegevensverzameling gebruikt, worden Apparaat en afmetingen die zijn gebaseerd op de zoekopdracht van het apparaat momenteel niet ondersteund. Toekomstige steun is gepland. Voor het toevoegen van apparaat en browser raadplegingen aan uw SDK gegevensstroom van het Web, verwijs naar [ deze documentatie ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=nl-NL) |

## Op een nieuwe manier ondersteund {#new-support}

| Functie | Notities |
| --- | --- |
| **Advertising Cloud** | U kunt [ historische gegevens voor AMO IDs en EF IDs voor gebruik in Customer Journey Analytics ](https://experienceleague.adobe.com/nl/docs/advertising/integrations/analytics/planning/rvars-to-evars) verzamelen. |
| **Waarschuwingen** | Het proces van [ het gebruiken van alarm in Customer Journey Analytics ](/help/components/c-intelligent-alerts/alerts-feature-comparison.md) is bijna identiek aan het gebruiken van alarm in Adobe Analytics. <p>Wegens het tijdstip van gegevensverzameling in Customer Journey Analytics zijn uurwaarschuwingen echter niet beschikbaar. In Customer Journey Analytics kunnen waarschuwingen worden geconfigureerd voor dagelijks, wekelijks of maandelijks.</p> |
| **Analytics voor Doel (A4T)** | De [ integratie tussen Adobe Customer Journey Analytics en Doel ](https://experienceleague.adobe.com/nl/docs/target/using/integrate/cja/target-reporting-in-cja) verstrekt krachtige analyse en tijdbesparende hulpmiddelen voor uw optimaliseringsprogramma. |
| **Publiek publiceren** | Wordt ondersteund als er een licentie is voor Adobe Customer Data Platform of Journey Optimizer-producten. [ Publiceren van het publiek ](/help/components/audiences/audiences-overview.md) verzendt publiek naar het Profiel van de Klant in real time in Experience Platform. |
| **Classificaties** | Nu genoemd &quot;de Datasets van de Raadpleging&quot;. Classificaties die in Analytics worden gebruikt, kunnen naar de Experience Platform en Customer Journey Analytics worden geïmporteerd met behulp van de Analytics Classifications Source Connector. Gegevenssets voor opzoeken kunnen ook rechtstreeks naar Experience Platform worden geüpload en beschikbaar worden gesteld in Customer Journey Analytics. |
| **de regelbouwer van de Classificatie** | Ondersteund gebruikend [ substrings ](/help/data-views/component-settings/substring.md) in Customer Journey Analytics. Gebruikt tekenreeksmanipulaties in rapporttijd eerder dan raadplegingsdatasets. |
| **Eigen zittingslengte** | De lengte van de zitting kan door [ montages van de Zitting ](../../data-views/create-dataview.md#session-settings) in een mening van Gegevens worden gevormd. Zie [ montages van de Zitting ](../../data-views/session-settings.md) voor meer informatie. <br/> het behandelen van mobiele achtergrondgebeurtenissen wordt gesteund door Adobe Experience Platform Mobile SDK. Zie [ Levenscyclus voor Edge Network ](https://developer.adobe.com/client-sdks/documentation/lifecycle-for-edge-network/) voor meer informatie. |
| **de omzetting van de Valuta** | Ondersteund als deel van [ die een metrische component ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/format.html?lang=nl-NL#currency) in een gegevensmening formatteren. |
| **Klantkenmerken** | Deze worden nu &quot;profielgegevenssets&quot; genoemd en worden niet automatisch geïmporteerd uit Experience Cloud, maar moeten naar Experience Platform worden geüpload voordat ze beschikbaar zijn in Customer Journey Analytics. |
| **het voer van Gegevens** | De uitvoer van gegevens van de eerste generatie van datasets is beschikbaar door [ de Toegang API van Gegevens van Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=nl-NL) en door [ Doelen van Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=nl-NL). Met deze opties kunt u alle verzamelde of opgenomen gegevens op gebeurtenis-/rijniveau exporteren naar het Experience Platform Data Lake. Gegevenskolommen na verwerking zijn niet beschikbaar omdat postkolommen bij vraagtijd worden berekend. Exporteren van postkolommen is beschikbaar via rapportage. |
| **Data Warehouse die** meldt | [ de Volledige Uitvoer van de Lijst van Customer Journey Analytics ](/help/analysis-workspace/export/export-cloud.md) is de evolutie van de rapporten van Data Warehouse in Adobe Analytics, met vele nieuwe, vaak-gevraagde eigenschappen die niet vandaag in Data Warehouse beschikbaar zijn. |
| **Ingangen, Uitgangen, en Tijd bestede dimensies en metriek** | Ondersteund (Ingangen en Uitgangen worden nu Sessiebegin en Sessieeinde genoemd) en worden op een iets andere manier berekend. |
| **de persistentiemontages van eVar** | eVars maken geen deel meer uit van Customer Journey Analytics. De instellingen voor persistentie maken nu echter deel uit van de gegevensweergave en zijn beschikbaar voor alle dimensies. Onthoud dat persistentie is gebaseerd op de verwerking van de rapporttijd, niet op de verwerking van gegevensverzameling. De afmetingen die zijn ingesteld in de gegevensweergaven zijn beperkt tot een maximale persistentie van 90 dagen en ondersteunen geen onbeperkte persistentie. |
| **de dimensies van Geosegmentation** | [ Volledige steun ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=nl-NL) |
| **op grafiek-gebaseerde het stitching** | Door [ op grafiek-gebaseerde Stitching ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/stitching/overview#graph-based-stitching), kunt u de macht van de identiteitsgrafiek in [ de Dienst van de Identiteit van Adobe Experience Platform gebruiken ](https://experienceleague.adobe.com/nl/docs/experience-platform/identity/home) om datasets aan hun aangewezen identiteit op te heffen. |
| **Waarschuwingen** | Het proces om [ alarm ](/help/components/c-intelligent-alerts/intelligent-alerts.md) in Customer Journey Analytics te gebruiken is bijna identiek aan het gebruiken van alarm in Adobe Analytics. Nochtans, zijn er [ belangrijke verschillen ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/alerts/alerts-feature-comparison). |
| **IP verduistering** | Voor Customer Journey Analytics-klanten die de Analytics-bronconnector gebruiken om gegevens van Adobe Analytics in Customer Journey Analytics te vullen: IP-verduisteringsinstellingen die in Adobe Analytics zijn toegepast, worden doorgevoerd in uw Customer Journey Analytics-gegevens. U kunt deze instellingen desgewenst in Adobe Analytics beheren.<p>Voor Customer Journey Analytics-klanten die Experience Platform Web SDK gebruiken om gegevens rechtstreeks in te vullen in Platform en Customer Journey Analytics. U kunt Prep van Gegevens voor de Inzameling van Gegevens in Platform gebruiken om regels te vormen die het IP adres verduisteren dat op de vereisten van uw bedrijf wordt gebaseerd. |
| **de Kanalen van de Marketing** | Wanneer het gebruiken van de bron van Analytics schakelaar, stromen de gegevens van Kanalen van de Marketing in Customer Journey Analytics door die schakelaar. De regels van het Kanaal van de marketing worden gevormd in traditionele Adobe Analytics en sommige regels worden niet gesteund. Zie [ de In de handel brengende Kanalen van Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/aa-data/marketing-channels.html?lang=nl-NL) voor meer informatie. <br/> voor implementaties WebSDK, rapport-tijd de verwerkingsregels van het marketingkanaal worden gesteund door [ Afgeleide gebieden ](../../data-views/derived-fields/derived-fields.md). |
| **Merchandising veranderlijke persistentie** | Volledige Steun via [ bindende dimensies en bindende metriek ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html?lang=nl-NL#binding-dimension) |
| **Metrische deduplicatie** | Nu gevormd op metriek binnen de Mening van Gegevens. De metrische deduplicatie gebeurt op het persoon of zittingsniveau eerder dan de Dataset, de mening van Gegevens, of het niveau van de Verbinding. |
| **Nieuwe vs. herhalingszitting die** melden | Vroeger verwezenlijkt gebruikend de dimensie van het Aantal van het Bezoek. De nieuwe vs. Herhaal zittingen worden gesteund [ met een terugkijkvenster van 13 maanden ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/data-views/data-views-usecases.html?lang=nl-NL). |
| **Regels van de Verwerking, de regels van VISTA, de verwerkingsregels van het Kanaal van de Marketing** | Ondersteund gebruikend de functionaliteit van de Prep van Gegevens van Adobe Experience Platform evenals [ afgeleide gebieden ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/derived-fields.html?lang=nl-NL) voor zowel WebSDK gebaseerde datasets als gegevens van de de bronschakelaar van de Analyse. |
| **veranderlijke Producten** | Binnen Experience Platform, kunnen de gebruikers een serie van voorwerpen binnen een datasetschema gebruiken om aan dit gebruiksgeval te voldoen. In Customer Journey Analytics kunnen klanten een willekeurig aantal productvariabelen gebruiken en zijn ze niet beperkt tot één variabele, zoals in Adobe Analytics. |
| **het delen van het Project** | Het delen van projecten wordt alleen ondersteund door gebruikers van Customer Journey Analytics. Er wordt geen project gedeeld tussen Customer Journey Analytics en de traditionele Analysis Workspace. |
| **Report Builder** | Ondersteund met een nieuwe Office 365-insteekmodule voor Microsoft Excel. |
| **de toestemmingen van de Gebruiker/de toegangscontroles van Gegevens** | Customer Journey Analytics onderscheidt tussen [ Adobe Admin Console ](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html?lang=nl-NL) productbeheerders, de beheerders van het productprofiel, en gebruikers. Alleen productbeheerders kunnen verbindingen, projecten, segmenten of berekende metriek maken/bijwerken/verwijderen die door andere gebruikers zijn gemaakt, terwijl productbeheerders en productprofielbeheerders de weergave Gegevens kunnen bewerken. Er zijn aanvullende gebruikersmachtigingen beschikbaar voor bijvoorbeeld het maken van berekende metriek, segmenten of annotaties. |
| **Visualisaties** | Alle Workspace-visualisaties worden ondersteund, met uitzondering van de Kaartweergave. |
| **dwars-apparaat/dwars-kanaal het stitching** | Ondersteund voor gebeurtenisgegevenssets die identiteitsgegevens bevatten. Zie [ Plaatsen ](../../stitching/overview.md). |

## Gedeeltelijke ondersteuning {#partial}

| Functie | Notities |
| --- | --- |
| **de panelen van Workspace** | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. De deelvensters Segmentvergelijking en Analyse voor Doel (A4T) worden niet ondersteund. |

## Geen steun, maar gepland {#planned}

| Functie | Notities |
| --- | --- |
| **Echt - tijd rapporterend** | Er is steun gepland. |
| **Segment-IQ** | Er is steun gepland. |
| **de gegevensbronnen van identiteitskaart van de Transactie** | Er is steun gepland. |

## Geen ondersteuning, nog niet gepland {#not-planned}

| Functie | Notities |
| --- | --- |
| **Activity Map** | De steun is nog niet gepland. |
| **analyse van de Bijdrage** | De steun is nog niet gepland. |

## Wordt nooit ondersteund {#never}

* Metrische personen met behulp van Cross-Device Coop
* Triggers
