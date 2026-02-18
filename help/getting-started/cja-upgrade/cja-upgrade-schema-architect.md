---
title: Uw schema archiveren voor gebruik met Customer Journey Analytics
description: Leer hoe u een XDM-schema ontwerpt dat de flexibiliteit van Customer Journey Analytics ontgrendelt en tegelijkertijd een praktisch migratiepad vanuit Adobe Analytics ondersteunt.
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: f932110a-ca9d-40d1-9459-064ef9cd23da
source-git-commit: 5808de9b39d3c8fa5632755958ddb887c081b203
workflow-type: tm+mt
source-wordcount: '1467'
ht-degree: 0%

---

# Uw schema archiveren voor gebruik met Customer Journey Analytics {#upgrade-schema-architect}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-schema-architect"
>title="Een schema archiveren"
>abstract="Bespreek binnen uw organisatie de vereisten van gegevensinzameling, en bepaal hoe u een schema voor gebruik in Adobe Experience Platform wilt bouwen. Deze stap verschijnt omdat u het geadviseerde proces wilt gebruiken om een schema te gebruiken dat aan uw organisatie wordt aangepast. Het correct uitvoeren van deze stap is essentieel, aangezien een schema dat alle teams binnen uw organisatie zich richt op maakt gegevensopname beduidend gemakkelijker.<br><br> de geschatte tijd om alle relevante partijen in uw organisatie samen te brengen zich op een verenigd schema te richten is 1-2 maanden. Dit tijdkader hangt sterk af van het aantal teams die worden vereist om te coördineren, en het aantal dimensies + metriek om zich op te richten."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

Adobe adviseert het creëren van een model van de Gegevens van de douaneervaring [&#x200B; (XDM) schema voor Customer Journey Analytics wanneer het uitvoeren van &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home) de Inzameling van Gegevens van Adobe Experience Platform [. &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/collection/home) Dit schema maken wordt doorgaans uitgevoerd voordat implementatiewijzigingen of code worden gewijzigd. Met een aangepast schema kunt u een beknopt, organisatie-specifiek gegevenscontract ontwerpen zonder beperkingen van Adobe Analytics over te nemen. Zie [&#x200B; uw schema voor Customer Journey Analytics &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-schema-existing.md) kiezen om meer over de types van schema&#39;s te leren beschikbaar aan uw organisatie.

Schema&#39;s zijn bedoeld als gepolijste versies van hoe u wilt dat uw gegevens op lange termijn gestructureerd zijn. Wijzigingen in schema&#39;s zijn duur omdat ze van invloed zijn op gegevensverzameling, validatie en downstreamservices. U kunt aan schema&#39;s in tijd toevoegen aangezien de bedrijfsvereisten toestaan; nochtans, kunnen de schemagebieden niet worden verwijderd zodra het gegeven in hen begint te stromen.

## Schema&#39;s vergelijken met gegevensweergaven

De datapijplijn voor Customer Journey Analytics bevat verschillende gebieden voor gegevensverzameling en gegevensinterpretatie. Wanneer u een upgrade uitvoert vanuit Adobe Analytics, wordt vaak geprobeerd om props en eVars met hun gedrag opnieuw te maken in XDM. In plaats daarvan, gebruik SDK van het Web om de gegevens te verzamelen en [&#x200B; meningen van Gegevens &#x200B;](/help/data-views/data-views.md) te gebruiken om te bepalen hoe dat gegeven in rapporten wordt geïnterpreteerd.

| Laag | Primair doel | Flexibiliteit | Wat hoort | Wat niet hoort |
|---|---|---|---|---|
| **XDM schema** | De duurzame structuur en betekenis van verzamelde gegevens definiëren | Onbuigzaam; beschouwd als onveranderlijke gegevenspunten | Vorm van gebeurtenis en entiteit, veldbetekenis, relaties, toegestane waarden, hergebruik via kanalen | Genummerde &quot;slots&quot; (eVar1/prop1), attributie-/persistentielogica, rapporteringsspecifieke tijdelijke oplossingen |
| **de meningen van Gegevens** | Bepaal hoe de verzamelde gegevens zich in analyse gedragen | Flexibel; kan vrij worden gewijzigd en gegevens met terugwerkende kracht herinterpreteren | Componentinstellingen, kenmerk en persistentiegedrag, afgeleide velden, gefilterde meetwaarden, berekende meetwaarden | Fundamentele betekenis van velden; deze betekenis moet stabiel zijn in het schema |

## Vergelijk schema&#39;s met de gegevensinzameling van Adobe Analytics

Het Experience Data Model dat Customer Journey Analytics gebruikt, biedt aanzienlijk meer flexibiliteit dan de meeste andere Analytics-oplossingen (inclusief Adobe Analytics). Het vestigen van een stevig schema is de kans van uw organisatie om het dragen van voorwaartse beperkingen te vermijden die in andere producten van Analytics bestaan.

| Algemene gewoonte van Adobe Analytics | Betere benadering in XDM + Customer Journey Analytics |
|---|---|
| Het ontwerpen rond genummerde groeven (`eVar1` - `eVar250`, `prop1` - `prop75`) | Maak velden met een stabiele betekenis (bijvoorbeeld `search.term` , `content.category` , `user.membershipTier` ) en gebruik deze op consistente wijze |
| Coderingspersistentie/toewijzing/vervaldatum in het gegevensmodel | Leg duurzame feiten vast in het schema; pas attributie- en persistentiegedrag toe op het niveau van de gegevensweergave |
| Dezelfde waarde in meerdere variabelen dupliceren om rapportgedrag te bereiken | Sla de waarde eenmaal op en maak er meerdere componenten (afmetingen/metriek) van in gegevensweergaven |
| Het creëren van een uniek &quot;metrisch gebied&quot;voor elke telling die u zou kunnen willen | Leg de juiste feiten één keer vast (vaak als opsommingen/laarzen/tekenreeksen) en definieer metriek vervolgens als gefilterde tellingen in gegevensweergaven |
| Variabelen ontwerpen voor rapportage vooraf oplossen | Ontwerp uw schema om feiten vast te leggen en gegevensweergaven te gebruiken om de rapportsemantiek op te lossen |

## Een schema maken met behulp van algemene kenmerken

Een verenigd schema over kanalen wordt mogelijk wanneer u een reeks herbruikbare attributen normaliseert die over vele gebeurtenissen verschijnen. Voorbeelden zijn:

* **de context van de Ervaring:** plaats/app naam, milieu, scène, kanaal, merk
* **context van de Reis:** campagne herkenningstekens, verwijzend context, experimenteerherkenningstekens
* **de staat van de Gebruiker:** het programma geopende status, lidmaatschapsrij, accounttype
* **de details van de Interactie:** interactienaam/type, gebied UI, elementetiket, foutencategorie

De sleutel is om te standaardiseren wat het gebied ongeacht kanaal vertegenwoordigt. Vermijd het anders modelleren van het zelfde concept over kanalen tenzij zij werkelijk verschillende concepten vertegenwoordigen. Het is bijvoorbeeld verstandig om geen aparte schemavelden te hebben voor campagne-id&#39;s voor het web en voor mobiele campagne-id&#39;s. Afzonderlijke schemagebieden maken het moeilijker om kanaalterugkeer op te richten en gegevens uit te geven. Als bij het rapporteren een onderscheid wordt vereist, kunt u per kanaal segmenteren of meerdere velden aaneenschakelen om dat onderscheid te maken. U kunt hetzelfde schemaveld gebruiken in een willekeurig aantal dimensies of metriek.

Een praktische manier om veelvoudige kanalen te steunen terwijl het houden van één enkele schemastrategie is a **kern + uitbreidingen** patroon te gebruiken:

* **Kern:** gebieden die globaal over kanalen en teams van toepassing zijn
* **Uitbreidingen:** kanaal- of domein-specifieke gebiedsgroepen die slechts waar nodig van toepassing zijn (Webinteractie, handel, mobiele levenscyclus, server-zijspecificaties)

Dit patroon steunt één enkele organisatorische schemastrategie zonder teams te dwingen om onnodige gebieden te bevolken.

## Voorkeur voor standaardveldgroepen waar deze passen

Adobe raadt aan gestandaardiseerde veldgroepen te gebruiken waar deze aan uw behoeften voldoen en deze uit te breiden met aangepaste velden voor organisatiespecifieke concepten.

Standaard veldgroepen helpen u doorgaans:

* Verminder dubbelzinnigheid door bekende veldsemantiek te gebruiken
* Eenvoudiger uitlijnen tussen teams
* Interoperabiliteit in Adobe Experience Platform-toepassingen ondersteunen

Aangepaste velden zijn geschikt wanneer:

* Uw organisatie heeft concepten die niet schitterend aan standaardgebieden
* U hebt aanvullende kenmerken nodig om te voldoen aan de vereisten voor rapportage, governance of activering
* U wilt een business-specific taxonomie (bijvoorbeeld, interne inhoudscategorieën) vertegenwoordigen

## Bepalen hoe metrische gegevens worden geteld

In Adobe Analytics behandelen veel teams de variabele `events` als het enige middel om metriek te volgen. In Customer Journey Analytics kunt u metrische gegevens op meerdere manieren bijhouden, afhankelijk van wat u moet tellen en hoe u deze wilt interpreteren.

Wanneer het ontwerpen van een schema, houd aan feiten. Bijvoorbeeld `error.type = "validation"` , `user.isLoggedIn = true` , `checkout.step = "shipping"` . Bepaal metriek in de gegevensmening als tellingen en gefilterde tellingen over die feiten. Bijvoorbeeld:

* `checkout.step` (enum/string) kan macht hebben:
   * Afhandeling: stap voor verzending bereikt (tel waar `checkout.step == "shipping"` )
   * &quot;Afhandeling: betalingsstap bereikt&quot;
* `error.type` (enum/string) kan macht hebben:
   * Validatiefouten
   * &quot;Autorisatiefouten&quot;
* `user.isLoggedIn` (Boolean) kan de volgende mogelijkheden inschakelen:
   * &quot;Voor authentiek verklaarde zittingen&quot;
   * &quot;Authenticated conversions&quot;

>[!TIP]
>
>Wanneer het beslissen of iets een specifiek gebied in het schema versus een afgeleid gebied later zou moeten zijn, verkies het vangen van het duurzame feit in het schema als het over het algemeen nuttig en stabiel is. U kunt afgeleide velden gebruiken om gegevens na de verzameling te corrigeren of om te vormen.

## Gelijkheid met Adobe Analytics behouden tijdens de overgang zonder schemabagage

Sommige organisaties moeten de rapportage van Adobe Analytics voortzetten terwijl ze een upgrade naar Customer Journey Analytics uitvoeren. U kunt pariteit handhaven zonder analytische-specifieke artefacten in uw schemaontwerp op lange termijn te introduceren gebruikend de volgende benadering:

1. **het gebiedspaden van XDM van het Gebruik die Adobe Analytics erkent en automatisch in kaart brengt:** wanneer u erkende gebieden XDM door Edge Network naar Adobe Analytics verzendt, worden zij [&#x200B; automatisch in kaart gebracht &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/xdm-var-mapping) zonder extra configuratie.
1. **de gebieden van douane XDM van het Gebruik voor organisatie-specifieke concepten:** Om het even welke gebieden XDM die niet automatisch in kaart worden gebracht aan een variabele van de Analyse door:sturen als [&#x200B; variabelen van de Contextgegevens &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/page-vars/contextdata) in Adobe Analytics.
1. **de verwerkingsregels van Adobe Analytics van het Gebruik om die variabelen van contextgegevens aan props/eVars in kaart te brengen:** [&#x200B; de regels van de Verwerking &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/processing-rules/pr-overview) laat uiteindelijk u toe om het even welk gebied van douane XDM in om het even welke eVar of steun in kaart te brengen. Dit concept ondersteunt pariteitsrapportage in Adobe Analytics terwijl uw schema schoon en gecentreerd op Customer Journey Analytics blijft.

## Belanghebbenden identificeren en eigendomsstructuur definiëren

Het schemaontwerp slaagt wanneer de gebiedsbetekenis wordt overeengekomen en gehandhaafd. Terwijl de organisatiestructuren variëren, nemen de volgende rollen algemeen deel:

* **Admin/analist van de Analyse**: bepaalt het melden van vragen, bevestigt dat de gebieden betekenisvolle concepten vertegenwoordigen, en de puntteksten van de overzichtsanalyse in gegevensmeningen.
* **ontwikkelaar/implementatieeigenaar**: Zorgt ervoor dat de gebieden betrouwbaar kunnen worden verzameld gebruikend het Web SDK en richt zich op de gegevenslaag/app instrumentatie.
* **architect/ingenieur van Gegevens**: verzekert schemaconconsistentie, hergebruik over domeinen, en verenigbaarheid met de stroomafwaartse diensten.
* **Privacy/beheer belanghebbende**: De gegevensminimalisering van recensies, toestemmingsverwachtingen, en beperkingen van het gegevensgebruik.

Definieer een duidelijke eigenaar voor schemawijzigingen. Een stabiel schema met gedisciplineerde veranderingscontrole verhindert stroomafwaartse breuk en vermindert rework. Overweeg een workflow of gereedschap voor het bijhouden van wijzigingen te gebruiken om verzoeken te democratiseren en wijzigingsbeheer in de loop der tijd te beheren.

## Overwegingen met betrekking tot privacy en bestuur

Het ontwerp van een schema moet de verwachtingen ten aanzien van privacy en governance weerspiegelen, in overeenstemming met het privacybeleid van uw organisatie. Houd rekening met de volgende punten wanneer u het schema ontwikkelt:

* Verzamel alleen wat u nodig hebt om gedefinieerde gebruiksgevallen te ondersteunen.
* Zorg ervoor dat de vereisten voor toestemming en gegevensgebruik worden weerspiegeld in uw verzamelingsstrategie. Zie [&#x200B; SDK van het Web gebruiken om gegevens van de klantentoestemming &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/consent/sdk) voor meer informatie te verwerken.
* Bedenk hoe gevoelige gebieden worden geëtiketteerd en gecontroleerd binnen de beheersinstrumenten van Adobe Experience Platform. Zie [&#x200B; Adobe Customer Journey Analytics en de Governance van Gegevens &#x200B;](/help/privacy/privacy-overview.md) voor meer informatie.

## Volgende stappen

Zodra u een schemaarchitectuur hebt gevestigd en overeengekomen, kunt u beginnen creërend het in Adobe Experience Platform. Zie [&#x200B; een douaneschema tot stand brengen om met Customer Journey Analytics &#x200B;](cja-upgrade-schema-create.md) voor meer informatie te gebruiken.
