---
title: Opmerkingen bij de release van Customer Journey Analytics
description: Aanvullende informatie voor de nieuwste versie van Customer Journey Analytics weergeven
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 14718476695dcf121c94ba4cb8b2c39e5874342d
workflow-type: tm+mt
source-wordcount: '1200'
ht-degree: 2%

---

# Opmerkingen bij de huidige Customer Journey Analytics-release (februari 2026)

**Laatste update**: 12 februari, 2026

Deze opmerkingen hebben betrekking op de releaseperiode van februari 2026. De versies van Adobe Customer Journey Analytics werken op a [&#x200B; ononderbroken leveringsmodel &#x200B;](releases.md), dat voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie en beschrijving | [&#x200B; Het begin van de Uitvoer &#x200B;](releases.md) | [&#x200B; Algemene Beschikbaarheid &#x200B;](releases.md) |
| ----------- | ------- | ---- |
| **Hoog treedt met voeten kopbal** <p>U kunt een koptekstnaam en een geheime koptekstwaarde opgeven in Content Analytics. Deze [&#x200B; kopbal treedt configuratie &#x200B;](/help/content-analytics/config/guided.md#header-overrides) met voeten ervoor dat Content Analytics de kopballen van douaneHTTP verzendt om om het even welke bot opsporing of de technologieën van het toegangsverkeer te mijden u hebt uitgevoerd.</p> |  | dinsdag 2 februari 2026 |
| **omvat veelvoudige afmetingskolommen in een vrije vormlijst**<p>U kunt nu maximaal vijf dimensiekolommen opnemen in een vrije-vormlijst, zodat u meerdere dimensiepunten naast elkaar kunt weergeven. Elke rij van afmetingspunten gedraagt zich als één enkel samengevoegd afmetingspunt.</p><p>U kunt filters, het sorteren, het breken, en meer op vrije vormlijsten met veelvoudige afmetingskolommen toepassen om een diepere en meer douaneanalyse tot stand te brengen.</p><p>Eerder kon u slechts één dimensiekolom in een vrije-vormlijst opnemen.</p><p>Voor meer informatie, zie [&#x200B; veelvoudige afmetingskolommen in een vrije vormlijst &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table-multidimensions.md) omvatten.</p> | donderdag 28 januari 2026 | maart <p>(Oorspronkelijk gepland voor 18 februari 2026)</p> |
| **de lijsten van de Soort door veelvoudige kolommen**<p>U kunt de gegevens van een vrije-vormlijst door veelvoudige kolommen in Analysis Workspace nu sorteren, of zij dimensies of metriek zijn.</p><p>Wanneer u gegevens voor meerdere kolommen sorteert, worden de gegevens gesorteerd op basis van de prioriteit die u aan elke kolom toewijst. De prioriteitsnummering wordt weergegeven naast het sorteerpictogram.</p><p>Voor meer informatie, zie [&#x200B; Filter en sorteer vrije vormlijsten &#x200B;](/help/analysis-workspace/visualizations/freeform-table/filter-and-sort.md).</p> | donderdag 28 januari 2026 | maart <p>(Oorspronkelijk gepland voor 18 februari 2026)</p> |
| **Volledige de uitvoerverbeteringen van de lijst**<p>De volledige tabelexport bevat de volgende verbeteringen:</p><p>Verbeteringen voor maken en configuratie van export</p><ul><li>Maak een exportbewerking van de pagina Exporteren. Eerder kon u alleen een exportbewerking maken vanuit Analysis Workspace door met de rechtermuisknop op de tabel te klikken.</li><li>Voeg een nieuwe account of locatie toe bij het maken van een exportbewerking.</li><li>Automatisch de naam van bestanden maken en de map plaatsen van geëxporteerde bestanden. Hierdoor kunnen bestandsnamen op een logische manier voorspelbaar zijn en in mappen worden ingedeeld. Eerder waren bestandsnamen onvoorspelbaar en gegroepeerd in één map.</li><li>Ondersteuning voor het exporteren van gegevens als Parquet-bestanden voor betere compatibiliteit met gegevenspaketten. Eerder werden alleen CSV en JSON ondersteund.</li></ul><p>Verbeteringen voor exportbeheer</p><ul><li>U kunt een of meer exportbewerkingen op de pagina Exporteren vernieuwen of annuleren.</li><li>Verzend een of meer exportbewerkingen opnieuw vanaf de pagina Logs.</li><li>E-mail individuele gebruikers of groepen wanneer de uitvoer ontbreekt of op het punt staat te verlopen.</li><li>Nauwkeuriger foutberichten voor mislukte exportbewerkingen.</li></ul><p>Berekende metrische, segment- en dimensieverbeteringen</p><ul><li>Ondersteuning voor meer berekende metrische functies. Eerder werden alleen eenvoudige rekenkundige functies ondersteund.</li><li>Pas segmenten toe bij het maken van een exportbewerking.</li><li>Ondersteuning voor dubbel-gegevenstypeafmetingen voor betere precisie.</li></ul><p>Administratieve verbeteringen</p><ul><li>Beheerders kunnen nu alle export- en logbestanden bekijken, ongeacht wie deze heeft gemaakt.</li></ul><p>(Koppeling met documentatie die moet worden gevolgd.)</p> | donderdag 25 februari 2026 | donderdag 11 maart 2026<p>(Oorspronkelijk gepland voor 4 maart 2026)</p> |
| **Content Analytics: De duimnagels en voorproeven van de verstrooiing** <p>Wanneer u een spreidingsvisualisatie weergeeft in Content Analytics, wordt nu een miniatuur van het element weergegeven wanneer u de cursor boven een punt in het diagram houdt. Met deze miniatuur kunt u snel en eenvoudig zien welke inhoud wordt weergegeven in het diagram.</p><p>(Koppeling met documentatie die moet worden gevolgd.)</p> | woensdag 17 februari 2026 | dinsdag 2 maart 2026 |
| **Content Analytics: De duimnagels en voorproeven van de Bar visualisatie** <p>Wanneer u een horizontale balk visualisatie weergeeft in Content Analytics, wordt nu een miniatuur van het element weergegeven wanneer u de cursor boven een balk in het diagram houdt. Met deze miniatuur kunt u snel en eenvoudig zien welke inhoud wordt weergegeven in het diagram.</p><p>(Koppeling met documentatie die moet worden gevolgd.)</p> | dinsdag 23 februari 2026 | dinsdag 9 maart 2026 |
| **Update aan de Benaderende functie van de Telling Distinct**<p>Het HLL probabilistic algoritme dat in de Approximate functie wordt gebruikt van de Telling wordt spoedig bijgewerkt. De resulterende uitvoer voor getallen die deze functie gebruiken, kan als volgt enigszins afwijken van historische getallen:<ul><li>Bij het tellen van zeer kleine hoeveelheden unieke waarden, zullen de resultaten worden verbeterd om nauwkeurige tellingen te gebruiken eerder dan het gebruiken van ramingen.</li><li>Wanneer u iets groter telt, behouden telramingen dezelfde nauwkeurigheid als vóór deze update (schattingen zijn nauwkeurig binnen 5 procent van het exacte getal, 95 procent van de tijd).</li></ul><p>Voor meer informatie over de Benaderende functie van de Telling Distinct, zie [&#x200B; Benaderende Telling Distinct &#x200B;](/help/components/calc-metrics/cm-adv-functions.md#approximate-count-distinct) in [&#x200B; Geavanceerde functies &#x200B;](/help/components/calc-metrics/cm-adv-functions.md)</p> |  | Maart 2026 |
| **Steun voor gegevensspiegel**  <p>Met steun voor model-gebaseerde schema&#39;s en de functionaliteit van de vangst van veranderingsgegevens (CDC) voor specifieke bronschakelaars in Experience Platform, zal Customer Journey Analytics [&#x200B; functionaliteit van de gegevenspiegel van &#x200B;](/help/data-mirror/data-mirror.md) kunnen steunen [!DNL Snowflake], [!DNL Azure Databricks], en [!DNL Google BigQuery].</p><p>Neem contact op met uw Adobe-accountteam voor toegang tot de bètaversie.</p> | Beta-release: 24 september 2025 | TBD |
| **Streaming media de diensten: De planningsgegevens van de steun** <p>U kunt nu planningsgegevens van eerder live streaming media-inhoud uploaden om de viewerstatus eenvoudiger en nauwkeuriger bij te houden.</p><p>Hieronder volgen voorbeelden van live-inhoud die wordt ondersteund met het uploaden van planningsgegevens:</p><ul><li>SNELLE (Free Ad Supported TV) platforms</li><li>Lokale streams</li><li>Levende sport</li></ul><p>Door planningsgegevens te uploaden, kunt u de viewergegevens bijhouden voor afzonderlijke programma&#39;s die worden uitgevoerd tijdens de tijd die u aangeeft in het uploadbestand. U kunt zelfs kijkersgegevens voor specifieke onderwerpen of programmasegmenten verzamelen.</p><p>Deze mogelijkheden zijn beschikbaar ongeacht de manier waarop u de Verzameling van de Media van de Streaming uitvoerde.</p><p>Eerder, was het moeilijk om een bepaalde zitting aan specifieke programma&#39;s nauwkeurig te verbinden wanneer het analyseren van levende inhoud, en het was niet mogelijk om een bepaalde zitting aan individuele onderwerpen of programmasegmenten te binden.</p><p>Voor meer informatie, zie [&#x200B; planningsgegevens uploaden om levende inhoud &#x200B;](https://experienceleague.adobe.com/nl/docs/media-analytics/using/media-use-cases/track-schedule-data) te volgen</p> | donderdag 29 oktober 2025 | Eerste helft van 2026<p>(Oorspronkelijk gepland voor vrijgave op 29 oktober 2025)</p> |
| **combineer rapportsuites van veelvoudige IMS organen**<p>Met de Analytics Source Connector kunt u rapportsuites van meerdere IMS-instanties combineren. Dit [&#x200B; dwars-IMS gegevenstoewijzingseigenschap &#x200B;](/help/getting-started/aa-vs-cja/mapping-data-ims-orgs.md) staat organisaties toe om een gecombineerde mening van hun klantengegevens te hebben, zelfs wanneer dat klantengegeven over veelvoudige organisaties IMS wordt verspreid. <p>**Nota:** Deze configuratie is beschikbaar slechts door een verzoek aan de Zorg van de Klant van Adobe voor te leggen.</p> |  | vrijdag 12 februari 2026 |

## Oplossingen in Customer Journey Analytics

**Analysis Workspace**: AN-421930, AN-424997, AN-424194, AN-425515, AN-425254, AN-423174, AN-428 834, AN-306540, AN-426014, AN-427801
**Componenten**:
**Content Analytics**:
**Geleide analyse**:
**de Uitvoer**: AN-422041, AN-421599, AN-422112
**meningen van Gegevens**:
**Uitvoering**:
**Report Builder**: AN-391415, AN-425125
**het Melden**: AN-425817, AN-424362, AN-425752, AN-425278, AN-422249, AN-40346 24727 AN-426791 AN-427985
**Segmentatie**: AN-428905, AN-428232
**Geplande rapporten**: AN-425484, AN-425137
**Gedeelde metriek en dimensies**:
**Andere**: AN-428833, AN-425074


## Belangrijke kennisgevingen voor Customer Journey Analytics-beheerders

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **TLS 1.2 de verwijdering van de manuscriptsuites** | donderdag 11 februari 2026 | Kennisgeving aan beheerders: Adobe is van plan op 27 mei 2026 de ondersteuning voor de volgende TLS 1.2-coderingssuites van Adobe-servers voor gegevensverzameling te verwijderen.<ul><li>`TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_128_CBC_SHA`</li><li>`TLS_RSA_WITH_AES_256_CBC_SHA`</li></ul><p>Voor de meeste implementaties is geen actie van de klant vereist. Deze wijziging heeft vooral invloed op analysegegevens die worden verzonden vanuit verouderde native toepassingen die verouderde TLS-bibliotheken gebruiken, en op een klein aantal webbezoekers in verouderde browsers of besturingssystemen. Als u de ondersteuning voor deze coderingssuites verwijdert, wordt de beveiliging verbeterd en wordt Adobe afgestemd op moderne coderingsstandaarden. Minder dan 0,1% van het gegevensverzamelingsverkeer is op dit moment afhankelijk van deze cijfersuites.</p> |

## Gerelateerde bronnen

* [Opmerkingen bij de vorige Customer Journey Analytics-release voor 2025](/help/release-notes/2025.md)
* [&#x200B; de versienota&#39;s van Adobe Analytics &#x200B;](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=nl-NL)
* [&#x200B; het stromen de versienota&#39;s van de Inzameling van Media &#x200B;](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html?lang=nl-NL)
* [&#x200B; de versienota&#39;s van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl-NL)
* [Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
