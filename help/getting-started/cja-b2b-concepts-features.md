---
title: Concepten en functies van Customer Journey Analytics B2B edition
description: Concepten en functies voor de B2B edition of Customer Journey Analytics.
solution: Customer Journey Analytics
feature: Basics
role: User, Admin
badgePremium: label="B2B edition"
exl-id: df2cc922-d214-49b9-8fdb-443cc1dac05b
source-git-commit: a9c22cfd7077fd9e1ac4b9ea4ec0e016e9d2425b
workflow-type: tm+mt
source-wordcount: '1468'
ht-degree: 0%

---


# B2B edition-concepten en -functies

Dit artikel verklaart concepten zoals verbindingen, herkenningstekens, containers, en datasets, algemeen gebruikt in Customer Journey Analytics. En hoe de Customer Journey Analytics B2B edition extra functies toevoegt aan deze concepten.


## Verbindingen en id&#39;s

In Customer Journey Analytics kiest u een gemeenschappelijke id, ook wel Persoon-id genoemd, waarmee u uw gebeurtenisgegevens kunt verbinden met andere gegevenssets, zoals profielgegevensset en opzoekgegevenssets. Dit type verbinding wordt een op persoon gebaseerde verbinding genoemd die op persoon-gebaseerde rapportering en analyse vergemakkelijkt.

In Customer Journey Analytics B2B edition kunt u kiezen tussen een persoonlijke verbinding of een verbinding op basis van een account. Een op account gebaseerde verbinding vergemakkelijkt rapportage en analyse op basis van account.

* Voor een op persoon gebaseerde verbinding selecteert u Person als primaire id. U kunt dan uw verbinding, gegevensmening en werkruimteprojecten voor op persoon-gebaseerde rapportering vormen en opstelling.
* Voor een verbinding op basis van een account selecteert u Account als primaire id. Vervolgens kunt u desgewenst extra containers toevoegen voor Global Account, Buying Group en Opportunity. Afhankelijk van of u een Global Account toevoegt of niet, is uw primaire id een account-id of een algemene account-id.


## Containers

In de containers van Customer Journey Analytics worden geproduceerd als deel van de configuratie van een verbinding en gegevensmening, en verstrekken gegevensstructuur en werkingsgebied. Containers slaan groepen id&#39;s op om alle tijdstempels van de gebeurtenis te laten volgen door unieke id&#39;s. Die opslag maakt het snel en prestatiever uitvoeren van functies zoals segmentatie, attributie en visualisatie mogelijk.

### Standaardcontainers

Customer Journey Analytics is gebouwd rond het concept van drie containers: Persoon, Zitting, en Gebeurtenis. Tijdens een configuratie, worden deze containers impliciet geproduceerd.

U kunt opnieuw bepalen hoe deze containers worden genoemd wanneer u een gegevensmening vormt maar de hiërarchie en de verhoudingen tussen de containers wordt vooraf bepaald. De container van de Zitting wordt geproduceerd gebaseerd op hoe u een zitting in de [&#x200B; montages van de Zitting &#x200B;](/help/data-views/session-settings.md) in uw gegevensmening bepaalt.

![&#x200B; B2C &#x200B;](assets/b2c-containers.svg){zoomable="yes"}


### B2B-containers

In Customer Journey Analytics B2B edition wordt een container Account toegevoegd aan de lijst met gegenereerde containers. En u hebt de optie om de generatie van extra containers, zoals Globale Rekening, het Kopen Groep, en Kans te vormen.

De hiërarchie en de relaties tussen de containers zijn vooraf bepaald. Opportunity, Buying Group en Person zijn alle containers op hetzelfde niveau van de container van de account. In die hiërarchie wordt de container van de Zitting tussen de container van de Persoon en de container van de Gebeurtenis geproduceerd gebaseerd op hoe u een zitting in de [&#x200B; montages van de Zitting &#x200B;](/help/data-views/session-settings.md) in uw gegevensmening bepaalt. Er worden momenteel geen extra sessiecontainers gegenereerd en ondersteund, bijvoorbeeld tussen de container Account en de container Event. Zie de onderstaande tabel voor een beschrijving en het basisgebruik van de B2B-containers.

![&#x200B; B2B &#x200B;](assets/b2b-containers.svg){zoomable="yes"}

| B2B-container | Beschrijving <br/> Basis gebruiksgeval |
|---|---|
| Account | Een bedrijf dat een klant of potentiële klant van uw zaken is. De onderneming zou een dochteronderneming of een afdeling van een grotere organisatie kunnen zijn. Account vertegenwoordigt de organisatie waarnaar u verkoopt en die u wilt bijhouden op organisatieniveau. |
| Globale account (optioneel) | De belangrijkste moedermaatschappij van een groep verbonden ondernemingen. Een global account heeft geen moedermaatschappij, maar kan dochterondernemingen of afdelingen hebben die tot de global account behoren. Wanneer u de globale container van de Rekening hebt gevormd in uw verbinding, zou een rekening die geen ouder of geen dochterondernemingen heeft op zowel het rekeningsgebied als globaal rekeningsgebied moeten worden vermeld. |
| Opportunity (optioneel) | Een verzameling producten en diensten die samen worden verkocht. Een kans bestond vaak uit verschillende fasen in de verkoopcyclus tot de sluiting van de verkoop.<br> u zou gegevens gebruiken om de opportuniteitsvooruitgang door de verkooptrechter te meten. Bijvoorbeeld een rapport dat details over de hoogste kansen verstrekt die zich van fase 3 aan fase 4 bewogen. |
| Groep voor kopen (optioneel) | Een verzameling personen binnen een organisatie die betrokken is bij het besluitvormingsproces voor de aankoop van een product of dienst. <br/> u zou het kopen groepsgegevens gebruiken om het kopen groepen door campagnebeheer te volgen. Stel bijvoorbeeld dat u een publiekssegment van belangrijke inkoopgroepen maakt.<br/> U wilt waarschijnlijk een zoekopdracht vanuit de inkoopgroep naar profielgegevens, zodat u gegevens over de personen in een inkoopgroep kunt melden. |
| Persoon | Een individu, dat vaak door een uniek e-mailadres wordt geïdentificeerd dat met het bedrijf in wisselwerking heeft gestaan. <br/> u zou de profielgegevens gebruiken om mensen te identificeren die voor een rekening werken. Bijvoorbeeld: richt alle mensen bij een rekening die zich voor een conferentie hebben aangemeld. |

>[!IMPORTANT]
>
>* Als u **&#x200B;**&#x200B;de Globale container van de Rekening in een op rekening-gebaseerde verbinding hebt toegelaten, zou elk verslag in uw gebeurtenisdatasets een identiteitskaart van de Rekening en Globale identiteitskaart van de Rekening moeten bevatten. Als dat niet het geval is, wordt de record overgeslagen.
>* Als u **&#x200B;**&#x200B;niet de Globale container van de Rekening in een op rekening-gebaseerde verbinding hebt toegelaten, zou elk verslag in uw gebeurtenisdatasets een identiteitskaart van de Rekening moeten bevatten. Als dat niet het geval is, wordt de record overgeslagen.

U kunt de B2B-containers gebruiken voor specifieke B2B-functionaliteit in Analysis Workspace:

* **Segmentatie**: [&#x200B; B2B segmentcontainers &#x200B;](/help/components/segments/seg-overview.md#b2b-containers) staan u toe om segmenten met een containerwerkingsgebied voorbij persoon, zitting of gebeurtenis te bouwen. Bijvoorbeeld: een account met een segment voor gebeurtenisregistratie of een Amerikaanse account met inkoopgroepen en een opportuniteitssegment voor fase 5.

  >[!NOTE]
  >
  >De B2B-gebeurtenisgegevens in een op een account gebaseerde setup in Customer Journey Analytics B2B edition kunnen gegevensrijen zonder persoon of sessie bevatten. Bijvoorbeeld: een rij die de voortgang van het opportuniteitsstadium aangeeft. Wanneer u uw segment evalueert, houd in mening dat de mensen en de zittingen niet meer de juiste criteria kunnen zijn.
  >

* **Attributie**: U kunt de nieuwe B2B containers in [&#x200B; attributiepaneel &#x200B;](/help/analysis-workspace/c-panels/attribution.md), in [&#x200B; montages van de attributie component &#x200B;](/help/data-views/component-settings/attribution.md) gebruiken, in [&#x200B; berekende metriek &#x200B;](/help/components/calc-metrics/cm-workflow/m-metric-type-alloc.md), of in [&#x200B; kolommen in een lijst Freeform &#x200B;](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md). Accountoverzichten worden verlengd tot 13 maanden.

* **Visualizations**: [&#x200B; Fall uit &#x200B;](/help/analysis-workspace/visualizations/fallout/fallout-flow.md), [&#x200B; Stroom &#x200B;](/help/analysis-workspace/visualizations/c-flow/flow.md), [&#x200B; het canvas van de Reis &#x200B;](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md), en [&#x200B; de lijst van de Cohort &#x200B;](/help/analysis-workspace/visualizations/cohort-table/cohort-analysis.md) visualisaties steunen de nieuwe B2B containers. U kunt de nieuwe containers bijvoorbeeld gebruiken om te begrijpen hoe het kopen van groepen inhoud verbruikt, of hoe opportuniteitscohorten naar het sluiten van een verkoop toe bewegen.
U kunt de standaardcontainer voor deze visualisaties in de [&#x200B; gebruikersvoorkeur &#x200B;](/help/analysis-workspace/user-preferences.md#visualizations-preferences) ook plaatsen.

Segmenten, attributie en visualisaties in combinatie met de B2B-containers ondersteunen u in diepgaande B2B-analyses en -inzichten.


## Gegevenssets

In Customer Journey Analytics B2B wordt onderscheid gemaakt tussen de volgende gegevenstypen en gegevenssets.

| Gegevenstype | Tijdreeks | Containerrecords | Veldrecords |
|---|---|---|---|
| **Datasets** | {de datasets van de Gebeurtenis 0} **bijvoorbeeld:**<br/><ul><li>Digitale analysemogelijkheden</li><li>CRM-gebeurtenissen</li><li>Persoonlijke gebeurtenissen</li><li>Gegevens van callcenter</li></ul> | {de datasets van het 0} Profiel **bijvoorbeeld:**<br/><ul><li>CRM-gegevens</li><li>AJO B2B-records</li><li>CDP-records</li><ul> | **Classificaties**<br/> bijvoorbeeld:<ul><li>Campagnebestanden</li><li>Records voor marketinglijsten</li><li>Metagegevens inhoud</li><li>Productdossiers</li></ul> |
| Vereisten | **Stempel van de Tijd**<br> Elk verslag vereist:<ul><li>Account-id</li><li>Global Account ID (optioneel)</li></ul> | **identiteitskaart van de Rekening**<br> Vereist de Verslagen van de Rekening een containeridentiteitskaart, als:<ul><li>Account</li><li>Persoon</li><li>Opportunity</li><li>Groep voor kopen</li></ul> | **het Aanpassen van sleutel**<br> Vereist Verslagen identiteitskaart in een container of gebeurtenisdataset, als:<ul><li>Campagne-id</li><li>Inhoud-id</li><li>Product-id</li></ul> |

{style="table-layout:fixed"}

Een voorbeeld van een op een account gebaseerde verbinding in de Customer Journey Analytics B2B edition:

![&#x200B; Voorbeeld op rekening-gebaseerde verbinding &#x200B;](assets/b2b-datasets.svg)

Customer Journey Analytics B2B edition biedt de [&#x200B; kaartinterface van de Verbinding &#x200B;](/help/connections/create-connection.md#connection-map) aan om u van een overzicht van het verband tussen datasets in uw verbinding te voorzien.


Net als in Customer Journey Analytics staan tijdreeksgegevens voor gebeurtenissen centraal in Customer Journey Analytics B2B edition. Het belangrijkste verschil voor een op rekening-gebaseerde verbinding is dat u een rekeningsidentiteitskaart op elk verslag in uw gebeurtenisdataset in plaats van persoonsidentiteitskaart nodig hebt.

Wanneer u [&#x200B; datasetmontages &#x200B;](/help/connections/create-connection.md#dataset-settings) voor uw op rekening-gebaseerde verbinding in Customer Journey Analytics B2B edition vormt, hangen de opties beschikbaar voor sommige montages van het [&#x200B; datasettype &#x200B;](/help/connections/create-connection.md#dataset-types) af. U moet bijvoorbeeld:

* Specificeer herkenningstekens voor elk van de containers die u voor uw gebeurtenisdatasets hebt gevormd.
* Definieer een accountveld of algemeen accountveld voor uw profielgegevenssets.
* Bepaal sleutels en hoe te om deze sleutels (door container van gebied) voor raadplegingsdatasets aan te passen.

## Afstemmen op container of veld

U kunt voor elke raadplegingsdataset bepalen, of u de dataset door gebied of door container aanpast.

### Afstemmen op container

Als een recorddataset een gelijke door container gebruikt, wordt de recorddataset behandeld als een type van profieldataset en als dataset van het Profiel in het gebruikersinterface. De gelijke van het gebruik door container op datasets die containerverslagen bevatten en die uw gevormde containers steunen. Bijvoorbeeld een gegevensset voor inkoopgroep.

### Overeenkomst per veld

Als een recorddataset een gelijke door gebied gebruikt, wordt de recorddataset behandeld als type van raadplegingsdataset en als dataset van de Opzoekopdracht in het gebruikersinterface. De gelijke van het gebruik door gebied op datasets die extra classificatiedetails door raadpleging bevatten. Bijvoorbeeld, een dataset van het Lid van de Lijst van de Marketing, of een dataset van de Details van het Product.


## Rapport over op personen en rekeningen gebaseerde gegevens

Als u op persoon-gebaseerde containers (en persoonsidentiteiten) en op rekening-gebaseerde containers (en rekeningsidentiteiten) wilt rapporteren, zou u twee afzonderlijke verbinding binnen Customer Journey Analytics moeten opzetten. Eén verbinding waarbij u Person als primaire id selecteert, en één verbinding waarbij u Account als primaire id selecteert. Customer Journey Analytics biedt geen ondersteuning voor persoonlijke en op account gebaseerde rapportage vanuit één containerhiërarchie.

