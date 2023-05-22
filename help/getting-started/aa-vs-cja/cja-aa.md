---
title: Ondersteuning voor Customer Journey Analytics-functies
description: Customer Journey Analytics-functies vergeleken met Adobe Analytics-functies ingesteld.
exl-id: be19aa27-58aa-438d-806c-e27c9a289797
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: 8c8e2db9b42deee081ce3b74481d0ad82c76818f
workflow-type: tm+mt
source-wordcount: '1994'
ht-degree: 3%

---

# Ondersteuning voor Customer Journey Analytics-functies

In de volgende tabellen wordt aangegeven welke functies in Adobe Analytics (AA) worden ondersteund, gedeeltelijk of niet ondersteund in Customer Journey Analytics (CJA) en welke functies van CJA niet worden ondersteund of beschikbaar zijn in AA. Deze lijsten worden na verloop van tijd gewijzigd wanneer functies aan CJA worden toegevoegd.

## Volledig ondersteunde functies/componenten {#full-support}

| Adobe Analytics-functie | Opmerkingen over ondersteuning |
| --- | --- |
| Anomaliedetectie | Volledige ondersteuning |
| Attribution IQ | Volledige ondersteuning |
| Berekende standaarden | volledige ondersteuning; Merk op dat bestaande berekende metriek in traditionele Analysis Workspace niet naar CJA zal worden uitgevoerd. |
| Kalendergebeurtenissen | Volledige ondersteuning. Kalendergebeurtenissen zijn geïmplementeerd als [Annotaties](/help/components/annotations/overview.md) in Workspace. |
| CSV-download | Volledige ondersteuning |
| Aangepaste kalenders | Volledige ondersteuning |
| Datumvergelijkingen | Volledige ondersteuning |
| Datumbereik | Alle functionaliteit voor datumbereik wordt ondersteund. |
| Dimensies | volledige ondersteuning; CJA gebruikt XDM en ondersteunt onbeperkte afmetingen. CJA is niet gekoppeld aan de aangepaste eVars of props van traditionele Adobe Analytics. |
| GDPR-verwijdering | volledige ondersteuning; merkt op dat GDPR nu wordt behandeld in coördinatie met [!UICONTROL Adobe Experience Platform]. CJA neemt alle gegevenswijzigingen over [!UICONTROL Experience Platform] maakt aan onderliggende datasets. |
| Lift and Trust Reporting | Volledige ondersteuning via [Deelvenster Experimentatie](/help/analysis-workspace/c-panels/experimentation.md) |
| Variabelen/lijsteigenschappen weergeven | volledige ondersteuning; CJA gebruikt XDM en steunt onbeperkte koordseries die op dezelfde manier als listVars kunnen worden gebruikt. |
| Merchandising-eVars | Volledige ondersteuning via [afmetingen binden en metriek binden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html#binding-dimension) |
| Metrics | volledige ondersteuning; CJA gebruikt het Model van de Gegevens van de Ervaring (XDM) en steunt onbeperkte metriek en is niet verbonden aan de gebeurtenissen van het douanesucces van traditionele Analytics. Merk op dat sommige standaardmetriek van traditionele Analytics zijn anders genoemd: Bezoekers = Personen, Bezoeken = Sessies, Hits = Gebeurtenissen. |
| Mobiel scorebord/dashboards | Volledige ondersteuning |
| Deelvensters | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. |
| PDF exporteren | Volledige ondersteuning |
| Projectcuratie | Volledige ondersteuning |
| Projectkoppeling | Volledige ondersteuning |
| Tijdverwerking rapporteren | volledige ondersteuning; CJA baseert zich uitsluitend op de Verwerking van de Tijd van het Rapport. |
| API-toegang rapporteren | volledige ondersteuning; Beschikbaar via [CJA API](https://www.adobe.io/cja-apis/docs/). |
| Geplande rapporten/projecten | Volledige ondersteuning |
| Segmenten | volledige ondersteuning; Nu &quot;Filters&quot; genoemd - merk op dat bestaande segmenten in traditionele Analysis Workspace niet worden geëxporteerd naar CJA. |
| Virtuele rapportsuites | volledige ondersteuning; Wordt nu aangeroepen [Gegevens](/help/data-views/create-dataview.md). |
| VRS-componentcursus | volledige ondersteuning; Nu onderdeel van gegevensweergaven. |
| Streaming media-analyse | De mediagegevens zijn beschikbaar via de gegevensverbinding Analytics als onderdeel van het deelvenster Mediagelijktijdige viewers en het deelvenster Media Playback Time Spent in Workspace. |

{style="table-layout:auto"}

## Nieuwe ondersteuning {#new-support}

| Functie | Notities |
| --- | --- |
| Publiek publiceren (Segmentpublicatie) | Wordt ondersteund als een licentie wordt verleend voor Adobe Data Platform of Journey Optimizer-producten. [Publiek publiceren](/help/components/audiences/audiences-overview.md) verzendt publiek naar het Profiel van de Klant in real time in Experience Platform. |
| Classificaties | Nu genoemd &quot;de Datasets van de Raadpleging&quot;. Classificaties die worden gebruikt in Analytics kunnen worden geïmporteerd naar het Experience Platform en CJA met behulp van de Bronconnector voor analytische classificaties. Gegevenssets voor opzoeken kunnen ook rechtstreeks naar AEP worden geüpload en beschikbaar worden gesteld in CJA. |
| Builder voor classificatieregels | Ondersteund met [subtekenreeksen](/help/data-views/component-settings/substring.md) in CJA. Gebruikt tekenreeksmanipulaties in rapporttijd eerder dan raadplegingsdatasets. |
| Aangepaste sessie | Ondersteuning voor alle aangepaste sessionisatiefuncties, behalve mobiele achtergrondgebeurtenissen. |
| Handelswijzigingsvariabele persistentie | Volledige ondersteuning via [afmetingen binden en metriek binden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/persistence.html#binding-dimension) |
| Klantkenmerken | Nu &quot;profielgegevenssets&quot; genoemd, worden ze niet automatisch geïmporteerd uit Experience Cloud, maar moeten ze worden geüpload naar AEP voordat ze beschikbaar zijn in CJA. |
| Gegevensfeeds | De uitvoer van gegevens van de eerste generatie is beschikbaar via [API voor toegang tot AEP-gegevens](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=en) en via [AEP-doelen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en). Deze opties bieden gebeurtenis-/rijniveau-export van alle gegevens die zijn verzameld of opgenomen in het AEP Data Lake. Kolommen met gegevens na het proces zijn niet beschikbaar omdat postkolommen bij de query worden berekend. Exporteren van postkolommen is beschikbaar via rapportage. |
| Metrische deduplicatie | Nu gevormd op metriek binnen de Mening van Gegevens. De metrische deduplicatie gebeurt op het persoon of zittingsniveau eerder dan de Dataset, de Mening van Gegevens, of het niveau van de Verbinding. |
| De ingangen, de Uitgangen, en de tijd bestede dimensies en metriek | Ondersteund (Ingangen en Uitgangen worden nu Sessiebegin en Sessieeinde genoemd) en worden op een iets andere manier berekend. |
| Instellingen voor eVar-persistentie | eVars maken geen deel meer uit van CJA. De instellingen voor persistentie maken nu echter deel uit van de gegevensweergave en zijn beschikbaar voor alle dimensies. Onthoud dat persistentie is gebaseerd op de verwerking van de rapporttijd, niet op de verwerking van gegevensverzameling. Dimension in gegevensweergaven zijn beperkt tot een maximale persistentie van 90 dagen en ondersteunen geen onbeperkte persistentie. |
| IP Obfuscatie | Voor CJA-klanten die de Analytics Source Connector gebruiken om gegevens van Adobe Analytics in CJA te vullen: De IP die de verduisteringsmontages in Adobe Analytics worden toegepast stromen door aan uw gegevens CJA. U kunt deze instellingen desgewenst in Adobe Analytics beheren.<p>Voor klanten CJA die SDK van het Web van Adobe Experience Platform gebruiken om gegevens in Platform en CJA direct te bevolken: U kunt Prep van Gegevens voor de Inzameling van Gegevens in Platform gebruiken om regels te vormen die het IP adres zullen verduisteren dat op de vereisten van uw bedrijf wordt gebaseerd. |
| Nieuwe versus herhaalde sessierapportage | Vroeger verwezenlijkt gebruikend de dimensie van het Aantal van het Bezoek. Nieuwe sessies vs. herhalingssessies worden ondersteund [met een terugzoekvenster van 13 maanden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/data-views-usecases.html?lang=en#new-repeat). |
| Productvariabele | Binnen het Experience Platform, kunnen de gebruikers serie van de typegebieden van Objecten binnen een datasetschema gebruiken om aan dit gebruiksgeval te voldoen. Binnen CJA kunnen klanten een willekeurig aantal productvariabelen gebruiken en zijn ze niet beperkt tot één variabele, zoals in Adobe Analytics. |
| Project delen | Het delen van projecten wordt alleen ondersteund door gebruikers van CJA - er wordt geen project gedeeld tussen CJA en de traditionele Analysis Workspace. |
| Visualisaties | Alle visualisaties worden ondersteund, behalve voor de visualisatie Kaart. |
| Report Builder (Excel-plug-in) | Ondersteund met een nieuwe Office 365-insteekmodule voor Excel. |
| Gebruikersmachtigingen/Toegangsbeheer voor gegevens | CJA maakt onderscheid tussen [Adobe Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html) productbeheerders, productprofielbeheerders en gebruikers. Alleen productbeheerders kunnen verbindingen, projecten, filters of berekende metriek maken/bijwerken/verwijderen die door andere gebruikers zijn gemaakt, terwijl productbeheerders en productprofielbeheerders de weergave van gegevens kunnen bewerken. Er zijn extra gebruikersmachtigingen beschikbaar voor bijvoorbeeld het maken van berekende metriek, filter of annotaties. |
| Verwerkingsregels, VISTA-regels, regels voor verwerking van distributiekanalen | Ondersteund met Adobe Experience Platform Data Prep-functionaliteit voor zowel WebSDK-gegevenssets als gegevens van de gegevensconnector Analytics Data. |

{style="table-layout:auto"}

## Gedeeltelijke ondersteuning {#partial}

| Functie | Notities |
| --- | --- |
| Marketingkanalen | De gegevens van Kanalen van de marketing stromen in CJA door de Bron van Analytics Schakelaar. De regels van het Kanaal van de marketing moeten nog in traditionele Adobe Analytics worden gevormd en sommige regels worden niet gesteund. Zie voor meer informatie [Documentatie CJA-marketingkanalen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html#cja-usecases). Bovendien, voor implementaties WebSDK, zijn de stop&#39;s beschikbaar voor het bepalen van marketing kanalen cliënt-kant. Er is voorzien in toekomstige steun voor verwerkingsregels voor afzetkanalen die zich in de verslagtijd bevinden. |
| Draaien tussen apparaten en kanalen | Ondersteund voor gegevenssets die rechtstreeks identiteitsgegevens bevatten (ook wel &quot;op het veld gebaseerde&quot; stitching genoemd). Grafiekgebaseerde stitching wordt nog niet ondersteund, maar gepland. Zie [Kanaaloverschrijdende analyse](/help/cca/overview.md). |
| Bot filteren | Voor [Adobe Analytics Source Connector](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html)Op gegevenssets gebaseerde gegevenssets worden beide gefilterd. De algemene bot filtering logica voor andere datasets wordt niet uitgevoerd door de [!UICONTROL Experience Platform] of CJA. |
| Apparaat, Browser, Referrer, de dimensies van de Technologie | Ondersteund voor [Adobe Analytics Source Connector](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html)- gebaseerde datasets. Raadpleeg onze [documentatie over de door ADC ondersteunde analytische variabelen](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics.html?lang=en).<p>Als u geen Adobe Source Connector gebruikt om gegevens van Adobe Analytics in CJA te bevolken, maar in plaats daarvan de gegevensinzameling van SDK van het Web van het Experience Platform te gebruiken, worden het Apparaat en de dimensies die op de raadpleging van het Apparaat worden gebaseerd momenteel niet gesteund. Toekomstige steun is gepland. |
| GeoSegmentation-afmetingen | Alle GeoSegmentation/geography die in Adobe Analytics wordt verzameld stroomt in CJA door [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html). Implementaties die geen gebruik maken van de Bronverbinding Analytics, zoals die welke voor digitale gegevensverzameling afhankelijk zijn van AEP Web SDK, zullen niet de volledige serie van automatisch uitgevoerde geografische zoekopdrachten hebben: Land en staat worden wereldwijd ondersteund, stad en zip niet. |
| Deelvensters | Het deelvenster Lege deelvensters, het deelvenster Kenmerken, het deelvenster Vrije vorm en Snelle inzichten worden volledig ondersteund. De deelvensters Segmentvergelijking en Analyse voor Doel (A4T) worden niet ondersteund. |
| Verwerkingsregels | Voor Analytics Source Connector-gebaseerde datasets, worden de verwerkingsregels nog toegepast. [Mogelijkheden voor gegevensuitwisseling in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html) kan ook worden gebruikt als vervanging voor verwerkingsregels voor gegevens die rechtstreeks naar het Platform gaan. |
| A4T | De gedeeltelijke steun wordt verleend door gebieden in [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html). Ondersteuning voor A4T-vriendelijke namen op doelactiviteiten en -ervaringen is gepland. |

{style="table-layout:auto"}

## Momenteel niet ondersteund, maar gepland {#planned}

| Functie | Notities |
| --- | --- |
| Waarschuwingen | Er is steun gepland. |
| Contributieanalyse | Er is steun gepland. |
| Rapportage Data Warehouse | Ondersteuning is gepland via de Analysis Workspace-interface. Adobe Experience Platform [[!UICONTROL Query Service]](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=nl) verstrekt ook een interface voor deze gebruiksgevallen in CJA. |
| ID-instelling via apparaatgrafiek | Er is steun gepland. |
| Projectsjablonen | Er is steun gepland. |
| Real-time rapportage | Er is steun gepland. |
| Segment-IQ | Er is steun gepland. |
| Valutaconversie | Er is steun gepland. |
| Gegevensbronnen van transactie-id | Er is steun gepland. |
| Projecten/filters/berekende metriek van AA aan CJA migreren | Er is steun gepland. |
| Gegevensbronnen op overzichtsniveau | Er is steun gepland. |

{style="table-layout:auto"}

## Steun nog niet gepland {#not-planned}

| Functie | Notities |
| --- | --- |
| Activity Map | De steun is nog niet gepland. |
| Advertising Cloud | De steun is nog niet gepland. |

{style="table-layout:auto"}

## Wordt nooit ondersteund {#never}

* Metrische personen met behulp van Cross-Device Coop
* Dashboards voor rapporten en analyses
* Bladwijzers voor rapporten en analyses
* Doelstellingen voor rapporten en analyses

## CJA-functies niet beschikbaar in Adobe Analytics {#cja-not-aa}

De volgende tabel bevat een lijst met functies die beschikbaar zijn in Customer Journey Analytics (CJA), maar die niet worden ondersteund in Adobe Analytics (AA).

| Functie | Meer details |
| --- | --- |
| Opslag voor alle soorten gegevens | CJA wordt gecombineerd met de capaciteit van het Experience Platform om allerlei gegevensschema&#39;s en types te houden. Gebruiken [Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl)Gegevens kunnen op uniforme wijze worden weergegeven en geordend, klaar voor combinatie en onderzoek. Adobe Analytics is vooral gericht op analytische gegevens voor het web en mobiele apparaten en beschikt over enkele mogelijkheden om [importgegevens](https://experienceleague.adobe.com/docs/analytics/import/home.html). |
| Onbeperkte Dimension en cijfers van klanten | CJA-afmetingen zijn onbeperkt; waarden kunnen numeriek, tekst, objecten, lijsten of mengsels van allemaal zijn. Dimension kunnen genest of hiërarchisch zijn. Analytics ondersteunt maximaal 75 props en 250 eVars. Hiermee worden de huidige metingsbeperkingen met afmetingen en gebeurtenissen verwijderd. |
| Onbeperkte kardinaliteit / unieke waarden | CJA ondersteunt onbeperkte unieke waarden of dimensie-items die binnen één dimensie kunnen worden gerapporteerd. AA is beperkt tot unieke waarden van 500 kB. Hierdoor worden de rapportage- en analysebeperkingen opgeheven die momenteel bestaan met grootschalige implementatie van Analytics. |
| Tijdtransformaties rapporteren | De Transformaties van de Tijd van het rapport (beter gekend als de Mening van Gegevens) in CJA staat u toe om gegevens van een verbinding verder te interpreteren. U kunt gegevens wijzigen of verwijderen zonder deze opnieuw te implementeren; subtekenreeksen gebruiken om afmetingen te manipuleren; metriek van om het even welke waarde tot stand brengen; filtersubgebeurtenissen. Dit kan allemaal niet-destructief worden gedaan. Adobe Analytics biedt beperkte mogelijkheden door middel van virtuele rapportsuites en sessionisatie. |
| Experimentatieanalyse | CJA kan de lift en het vertrouwen evalueren van experimenten vanuit elke gegevensbron die is gedefinieerd als onderdeel van een verbinding. Dit staat u toe om oorzaak-en-effect verhoudingen tussen klanteninteractie te begrijpen die om het even welk kanaal overspannen. Analytics is beperkt tot experimentatieanalyses via de integratie Analytics for Target (A4T). |
| Cross-device Analytics | CJA steunt de naadloze combinatie apparaat-specifieke datasets van unauthenticated en voor authentiek verklaarde zittingen. U kunt ook back-ups maken van historische gegevens op bekende apparaten. In Analytics, is dit vermogen beperkt tot één enkele rapportreeks en het gebruik van een apparatengrafiek. |
| SQL Access | Met de optie Gegevens-Distiller kan CJA de beperkingen van gegevens die zijn verzameld op Adobe backend-verwerking verwijderen. U kunt uw gegevens met SQL wijzigen, nieuwe waarden en datasets tot stand brengen uniek aan uw zaken en blijven onderzoeken. Analytics biedt geen ondersteuning voor SQL-toegang tot de bijbehorende gegevens. |
| Uitgebreide beveiligings- en privacyopties - HIPAA-gereedheid | CJA is HIPAA klaar en biedt extra veiligheidsopties voor regelnaleving aan. Adobe Analytics is niet klaar voor HIPAA. |

{style="table-layout:auto"}
