---
description: Met functies kunt u uw gegevens filteren/sorteren en statistische analyses uitvoeren.
title: Functies gebruiken
feature: Calculated Metrics
exl-id: 7a41aa4e-90c6-4242-a801-2eef6b524cfe
source-git-commit: 664576605b8be098a751609536e388c304c65513
workflow-type: tm+mt
source-wordcount: '4050'
ht-degree: 1%

---

# Functies gebruiken

Met functies kunt u uw gegevens filteren, sorteren en eenvoudige en complexe statistische analyses uitvoeren.

Voor een lijst van alle functies, verwijs naar [ Basisfuncties ](/help/components/calc-metrics/cm-functions.md) en [ Geavanceerde Functies ](/help/components/calc-metrics/cm-adv-functions.md).


>[!NOTE]
>
>Waar [!DNL metric] wordt geïdentificeerd als een argument in een functie, zijn andere expressies van metriek ook toegestaan. [!DNL MAXV(metrics)] staat bijvoorbeeld ook [!DNL MAXV(PageViews + Visits).] toe
>

>[!NOTE]
>
>Wanneer u functies opneemt in de definitie van de berekende metrieke builder, past u altijd de functie toe voordat u in metriek of filters sleept.
>

## Tabelfuncties versus rijfuncties

Een tabelfunctie is een functie waarbij de uitvoer voor elke rij van de tabel hetzelfde is. Een rijfunctie is een functie waarbij de uitvoer voor elke rij van de tabel anders is.

## Wat betekent de Include-Zeros-parameter?

Het vertelt of nullen in de berekening moeten worden opgenomen. Soms betekent nul &quot;niets&quot;, maar soms is het belangrijk.

Bijvoorbeeld, als u metrisch van de Opbrengst hebt, en dan metrische vertoningen van de Pagina aan het rapport toevoegt, zijn er plotseling meer rijen voor uw opbrengst die allen nul zijn. U wilt waarschijnlijk niet dat dit invloed heeft op MEAN, MIN, QUARTILE, enzovoort. berekeningen die u op de opbrengstkolom hebt. In dat geval controleert u de parameter include-zeros.

Aan de andere kant, als u twee metriek hebt die u geinteresseerd in bent, kan het niet eerlijk zijn om te zeggen dat één een hoger gemiddelde of een minimum heeft omdat sommige van zijn rijen nul waren, zodat zou u niet de parameter controleren om nullen te omvatten.

<!-- This video is way too outdated and too much AA oriented to comfortably show as part of CJA functionality 

Watch this [video](https://youtu.be/SSyWvomnewI) to understand the use of functions.

-->

+++ Basisfuncties


## Absolute waarde (rij)

Retourneert de absolute waarde van een getal. De absolute waarde van een getal is het getal met een positieve waarde.

```
ABS(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde waarvoor u de absolute waarde wilt. |

## Maximum kolom

Retourneert de grootste waarde in een set dimensieelementen voor een metrische kolom. MAXV evalueert verticaal binnen één enkele (metrische) kolom over afmetingselementen.

```
MAXV(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Een metrisch die u zou willen geëvalueerd hebben. |

## Minimaal kolom

Retourneert de laagste waarde in een set dimensieelementen voor een metrische kolom. MINV evalueert verticaal binnen één enkele kolom (metrisch) over afmetingselementen.

```
MINV(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Een metrisch die u zou willen geëvalueerd hebben. |

## Aantal kolommen

Voegt alle numerieke waarden voor metrisch binnen een kolom (over de elementen van een afmeting) toe.

```
SUM(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde waarvoor u de totale waarde of som wilt. |

## Aantal (tabel)

Retourneert het aantal of het aantal niet-nulwaarden voor een metrische waarde binnen een kolom (het aantal unieke elementen dat binnen een dimensie wordt gerapporteerd).

```
COUNT(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde die u wilt tellen. |

## Exponent (rij)

Keert *e* op tot de macht van een bepaald aantal. De constante *e* evenaart 2.71828182845904, de basis van natuurlijke logaritme. EXP is het omgekeerde van LN, de natuurlijke logaritme van een aantal.

```
EXP(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De exponent die op de basis *wordt toegepast e*. |

## Uitstel

Power Operator


pow (x, y) = x <sup> y </sup> = x *x* x*.. (y tijden)


## Gemiddeld (tabel)

Retourneert het rekenkundig gemiddelde (of gemiddelde) voor een metrische waarde in een kolom.

```
MEAN(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde waarvoor u het gemiddelde wilt. |

## Mediaan (tabel)

Retourneert de mediaan voor een metrische waarde in een kolom. De mediaan is het getal in het midden van een reeks getallen, dat wil zeggen dat de helft van de getallen waarden heeft die groter zijn dan of gelijk zijn aan de mediaan, en de helft kleiner dan of gelijk is aan de mediaan.

```
MEDIAN(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde waarvoor u de mediaan wilt. |

## Modulo

The rest of col1 / col2, using Euclidean Division.

Retourneert de rest na het delen van x door y.

```
x = floor(x/y) + modulo(x,y)
```

De geretourneerde waarde heeft hetzelfde teken als de invoer (of is nul).

```
modulo(4,3) = 1 
modulo(-4,3) = -1 
modulo(-3,3) = 0
```

Als u altijd een positief getal wilt ophalen, gebruikt u

```
modulo(modulo(x,y)+y,y)
```

## Percentage (tabel)

Retourneert het k-th-percentiel van waarden voor een metrische waarde. U kunt deze functie gebruiken om een acceptatiedrempel vast te stellen. U kunt bijvoorbeeld afmetingselementen bekijken die boven het 90-percentiel liggen.

```
PERCENTILE(metric,k)
```

<table id="table_35CD840ACFB44CD9979881DB8823CC53"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Argument </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <i> metrisch </i> </td> 
   <td colname="col2"> De metrische kolom die relatieve status definieert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>k </p> </td> 
   <td colname="col2"> De percentielwaarde in het bereik 0 tot en met 100. </td> 
  </tr> 
 </tbody> 
</table>

## Kwartaal (tabel)

Retourneert de kwartiel van waarden voor een metrische waarde. Bijvoorbeeld, kunnen de kwartielen worden gebruikt om de hoogste 25% van producten te vinden die de meeste opbrengst drijven. MINV, MEDIAN en MAXV retourneren dezelfde waarde als QUARTILE wanneer quart gelijk is aan respectievelijk 0 (nul), 2 en 4.

```
QUARTILE(metric,quart)
```

<table id="table_64EA3DAAE77541439D59FAF0353F83A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Argument </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <i> metrisch </i> </td> 
   <td colname="col2"> De metrische waarde waarvoor u de kwartielwaarde wilt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>kwart </p> </td> 
   <td colname="col2"> Geeft aan welke *value moet worden geretourneerd. </td> 
  </tr> 
 </tbody> 
</table>

&#42; als *kwart* = 0, KWALITEIT de minimumwaarde terugkeert. Als *kwart* = 1, KWALITEIT eerste kwartiel (25 percentiel) terugkeert. Als *kwart* = 2, KWALITEIT eerste kwartiel (percentiel 50) terugkeert. Als *kwart* = 3, KWALITEIT eerste kwartiel (75 percentiel) terugkeert. Als *kwart* = 4, KWALITEIT de maximumwaarde terugkeert.

## Rond

Geeft als resultaat het dichtstbijzijnde gehele getal voor een bepaalde waarde. Bijvoorbeeld, als u het melden van muntdecimalen voor opbrengst wilt vermijden en een product $569.34 heeft, gebruik de formule Rond ( *Opbrengst*) aan ronde opbrengst aan dichtstbijzijnde dollar, of $569. Een product dat $569,51 rapporteert, wordt afgerond naar de dichtstbijzijnde dollar, ofwel $570.

```
ROUND(metric)
```

| Argument | Beschrijving |
|---|---|
| *aantal* | De metrische waarde die u wilt afronden. |

Afgerond zonder een cijfers parameter is het zelfde als rond met een cijfers parameter van 0, namelijk rond aan het dichtstbijzijnde geheel. Met een cijferparameter keert het dat vele cijfers rechts van decimaal terug. Als cijfers negatief zijn, keert het 0&#39;s aan de linkerzijde van decimaal terug.

```
round( 314.15, 0) = 314 
round( 314.15, 1) = 314.1 
round( 314.15, -1) = 310 
round( 314.15, -2) = 300
```

## Aantal rijen

Geeft als resultaat het aantal rijen voor een bepaalde kolom (het aantal unieke elementen dat binnen een dimensie wordt gerapporteerd). &quot;Onkruisen&quot; wordt geteld als 1.

## Max. rij

Het maximum van de kolommen in elke rij.

## Min. rij

Het minimum van de kolommen in elke rij.

## Rijsom

De som van de kolommen van elke rij.

## Vierkante hoofdmap (rij)

Retourneert de positieve vierkantswortel van een getal. De vierkantswortel van een getal is de waarde van dat getal dat tot de macht 1/2 wordt verheven.

```
SQRT(metric)
```

| Argument | Beschrijving |
|---|---|
| *aantal* | De metrische waarde waarvoor u de vierkantswortel wilt. |

## Standaardafwijking (tabel)

Retourneert de standaardafwijking, of vierkantswortel van de variantie, gebaseerd op een samplepopulatie van gegevens.

De vergelijking voor STDEV is:

![](../assets/std_dev.png)

waar x het steekproefgemiddelde (*metrisch*) is en *n* is de steekproefgrootte.

```
STDEV(metric)
```

<table id="table_8BCF2E4B02434AABAAD026FB3C4E8B2F"> 
 <tbody> 
  <tr> 
   <td> <b> Argument </b> </td> 
   <td> <b> Beschrijving </b> </td> 
  </tr> 
  <tr> 
   <td> <b> <i> metrisch </i> </b> </td> 
   <td> <p> De metrische waarde waarvoor u standaardafwijking wilt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Variantie (tabel)

Geeft de variantie gebaseerd op een samplepopulatie van gegevens.

De vergelijking voor VARIANCE is:

![](../assets/variance_eq.png)

waar x het steekproefgemiddelde is, MEAN (*metrisch*), en *n* is de steekproefgrootte.

```
VARIANCE(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde waarvoor u de variantie wilt. |

Als u een variantie wilt berekenen, bekijkt u een hele kolom met getallen. Van die lijst van aantallen berekent u eerst het gemiddelde. Zodra u het gemiddelde hebt gaat u door elke ingang en doet het volgende:

1. Trek het gemiddelde van het getal af.

2. Maak het resultaat vierkant.

3. Voeg dat toe aan het totaal.

Als u de hele kolom hebt doorlopen, hebt u één totaal. Vervolgens deelt u dat totaal door het aantal items in de kolom. Dat getal is de variantie voor de kolom. Het is een enkel getal. Deze wordt echter weergegeven als een kolom met getallen.

In het geval van een kolom van drie artikelen:

1

2

3

Het gemiddelde van deze kolom is 2. De variantie voor de kolom zal ((1 - 2) <sup> 2 </sup> + (2 - 2) zijn <sup> </sup> + (3 - 2) <sup> 2 </sup>/3 = 2/3.

+++

+++ Geavanceerde functies


## EN

Retourneert de waarde van het argument ervan. Gebruik NOT om ervoor te zorgen dat een waarde niet gelijk is aan één bepaalde waarde.

>[!NOTE]
>
>0 (nul) betekent Onwaar en elke andere waarde is Waar.

```
AND(logical_test1,[logical_test2],...)
```

| Argument | Beschrijving |
|---|---|
| *logical_test1* | Vereist. Elke waarde of expressie die kan worden geëvalueerd op TRUE of FALSE. |
| *logical_test2* | Optioneel. Aanvullende voorwaarden die u als TRUE of FALSE wilt evalueren |

## Verschil bij benadering aantal (afmeting)

Retourneert de geschatte, verschillende telling van dimensie-items voor de geselecteerde dimensie. De functie gebruikt de methode HyperLogLog (HLL) om verschillende aantallen te benaderen.  Het wordt gevormd om de waarde binnen 5% van de daadwerkelijke waarde 95% van de tijd te waarborgen.

```
Approximate Count Distinct (dimension)
```

| Argument |  |
|---|---|
| *afmeting* | De afmeting waarvoor u de benaderende verschillende punttelling wilt. |

### Voorbeeld: hoofdletter gebruiken

Het geschatte Verschil van de Telling (de eVar van identiteitskaart van de klant) is een gemeenschappelijk gebruiksgeval voor deze functie.

Definitie voor een nieuwe berekende metrische waarde &quot;Benaderende Klanten&quot;:

![ benaderen graafschap verschillende nieuwe afmetingsdefinitie die identiteitskaart van de Klant tonen (eVar1) ](../assets/approx-count-distinct.png)

Dit is hoe &quot;Benadert Klanten&quot;metrisch zou kunnen worden gebruikt in het melden van:

![ Vrije-vormlijst die Unieke Bezoekers en Benaderde Klanten toont ](../assets/approx-customers.png)

### Telfuncties vergelijken

Distinct() is bij benadering een verbetering ten opzichte van de functies Count() en RowCount() omdat de gemaakte metrische waarde in elk dimensionaal rapport kan worden gebruikt om een geschatte telling van items voor een afzonderlijke dimensie te renderen. Bijvoorbeeld, een telling van klant IDs die in een Mobiel Rapport van het Type van Apparaat wordt gebruikt.

Deze functie zal marginaal minder nauwkeurig zijn dan Count() en RowCount() omdat het de methode HLL gebruikt, terwijl Count() en RowCount() exacte aantallen zijn.

## Boogcosinus (rij)

Retourneert de arccosinus, of omgekeerd van de cosinus, van een metrische waarde. De arccosinus is de hoek waarvan de cosinus getal is. De geretourneerde hoek wordt opgegeven in radialen tussen 0 (nul) en pi. Als u het resultaat wilt omzetten van radialen in graden, vermenigvuldigt u het met 180/PI( ).

```
ACOS(metric)
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek die u wilt instellen van -1 tot 1. |

## Boogsinus (rij)

Retourneert de arcsinus, of omgekeerde sinus, van een getal. De arcsinus is de hoek waarvan de sinus een getal is. De geretourneerde hoek wordt opgegeven in radialen in het bereik -pi/2 tot pi/2. Als u de arcsinus in graden wilt uitdrukken, vermenigvuldigt u het resultaat met 180/PI( ).

```
ASIN(metric)
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek die u wilt instellen van -1 tot 1. |

## Booghoek (rij)

Retourneert de arctangens, of omgekeerde tangens, van een getal. De arctangens is de hoek waarvan de tangens getal is. De geretourneerde hoek wordt opgegeven in radialen in het bereik -pi/2 tot pi/2. Als u de arctangens in graden wilt uitdrukken, vermenigvuldigt u het resultaat met 180/PI( ).

```
ATAN(metric)
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek die u wilt instellen van -1 tot 1. |

## Exponentiële regressie: voorspelde Y (rij)

Berekent de voorspelde y-waarden (metrisch_Y), gezien de bekende x-waarden (metrisch_X) gebruikend de &quot;minste vierkanten&quot;methode om de lijn van best te berekenen past gebaseerd op.

```
ESTIMATE.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Cdf-T

Retourneert het percentage waarden in de t-distributie van een student met n vrijheidsgraden met een z-score kleiner dan x.

```
cdf_t( -∞, n ) = 0
cdf_t(  ∞, n ) = 1
cdf_t( 3, 5 ) ? 0.99865
cdf_t( -2, 7 ) ? 0.0227501
cdf_t( x, ∞ ) ? cdf_z( x )
```

## Cdf-Z

Retourneert het percentage van waarden in een normale distributie met een z-score van minder dan x.

```
cdf_z( -∞ ) = 0
cdf_z( ∞ ) = 1
cdf_z( 0 ) = 0.5
cdf_z( 2 ) ? 0.97725
cdf_z( -3 ) ? 0.0013499
```

## Plakken (rij)

Geeft als resultaat het kleinste gehele getal dat niet kleiner is dan een bepaalde waarde. Bijvoorbeeld, als u het melden van muntdecimalen voor opbrengst wilt vermijden en een product $569.34 heeft, gebruik de formule CEILING ( *Inkomsten*) aan ronde opbrengst tot de dichtstbijzijnde dollar, of $570.

```
CEILING(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde die u wilt afronden. |

## Vertrouwen

[!UICONTROL Confidence] is een probabilistische maat van hoeveel bewijs er is dat een bepaalde variant het zelfde als de controlevariant is. Een hoger vertrouwen geeft minder bewijs voor de aanname dat de besturingsvariant en de niet-besturingsvariant dezelfde prestaties leveren.

```
fx Confidence (normalizing-container, success-metric, control, significance-threshold)
```

| Argument | Beschrijving |
| --- | --- |
| Container normaliseren | De basis (Mensen, Zittingen, of Gebeurtenissen) waarop een test zal worden in werking gesteld. |
| Metrisch met succes | De metrische of metrische waarde waarmee een gebruiker varianten vergelijkt. |
| Besturing | De variant waarmee alle andere varianten in het experiment worden vergeleken. Voer de naam in van het element Dimensie besturingsvariant. |
| Significantiedrempel | De drempel in deze functie is ingesteld op een standaardwaarde van 95%. |

{style="table-layout:auto"}

## Cosinus (rij)

Geeft als resultaat de cosinus van de opgegeven hoek. Als de hoek in graden is, vermenigvuldig de hoek met PI()/180.

```
COS(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor u de cosinus wilt gebruiken. |

## Kubus Root

Retourneert de positieve kubuswortel van een getal. De kubuswortel van een aantal is de waarde van dat aantal dat tot de macht van 1/3 wordt opgeheven.

```
CBRT(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde waarvoor u de kuburoot wilt gebruiken. |

## Cumulatief

Retourneert de som van x voor de laatste N-rijen (zoals geordend door de dimensie, met hashwaarden voor op tekenreeks gebaseerde velden).

Als N &lt;= 0 gebruikt het alle vorige rijen. Aangezien het door de afmeting wordt bevolen is het slechts nuttig op afmetingen die een natuurlijke orde zoals datum of weglengte hebben.

```
| Date | Rev  | cumul(0,Rev) | cumul(2,Rev) |
|------+------+--------------+--------------|
| May  | $500 | $500         | $500         |
| June | $200 | $700         | $700         |
| July | $400 | $1100        | $600         |
```

## Cumulatief gemiddelde

Retourneert het gemiddelde van de laatste N-rijen.

Als N &lt;= 0 gebruikt het alle vorige rijen. Aangezien het door de afmeting wordt bevolen is het slechts nuttig op afmetingen die een natuurlijke orde zoals datum of weglengte hebben.

>[!NOTE]
>
>Dit werkt niet zoals u zou kunnen verwachten met tariefmetriek zoals opbrengst/persoon: het gemiddelde van de tarieven in plaats van het optellen van opbrengst over laatste N en het optellen van personen over laatste N en dan het verdelen van hen. Gebruik in plaats daarvan

```
cumul(revenue)/cumul(person)
```

## Gelijk

Retourneert items die exact overeenkomen voor een numerieke waarde of tekenreekswaarde.

## Exponentiële regressie_ correlatiecoëfficiënt (tabel)

Keert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen ( *metrisch_A* en *metrisch_B*) voor de regressievergelijking terug.

```
CORREL.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u met *wilt correleren metrisch_Y*. |
| *metrisch_Y* | Metrisch die u met *wilt correleren metrisch_X*. |

## Exponentiële regressie: Intercept (tabel)

Keert intercept, *b*, tussen twee metrische kolommen ( *metrisch_X* en *metrisch_Y*) voor terug

```
INTERCEPT.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Exponentiële regressie: helling (tabel)

Keert de helling, *a*, tussen twee metrische kolommen ( *metrisch_X* en *metrisch_Y*) voor terug.

```
SLOPE.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Vloer (rij)

Geeft als resultaat het grootste gehele getal dat niet groter is dan een bepaalde waarde. Bijvoorbeeld, als u het melden van muntdecimalen voor opbrengst wilt vermijden en een product $569.34 heeft, gebruik de formuleFLOOR ( *Inkomsten*) aan ronde opbrengst neer aan de dichtstbijzijnde dollar, of $569.

```
FLOOR(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde die u wilt afronden. |

## Groter dan

Retourneert items waarvan het numerieke aantal groter is dan de ingevoerde waarde.

## Groter dan of gelijk aan

Retourneert items waarvan het numerieke getal groter dan of gelijk is aan de ingevoerde waarde.

## Hyperbolische cosinus (rij)

Geeft de hyperbolische cosinus van een getal.

```
COSH(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor u de hyperbolische cosinus wilt vinden. |

## Hyperbolische sinus (rij)

Geeft de hyperbolische sinus van een getal.

```
SINH(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor u de hyperbolische sinus wilt vinden. |

## Hyperbolische hoek (rij)

Retourneert de hyperbolische tangens van een getal.

```
TANH(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor u de hyperbolische tangens wilt vinden. |

## IF (rij)

De IF-functie retourneert één waarde als een door u opgegeven voorwaarde de waarde TRUE oplevert en een andere waarde als die voorwaarde de waarde FALSE oplevert.

```
IF(logical_test, [value_if_true], [value_if_false])
```

| Argument | Beschrijving |
|---|---|
| *logical_test* | Vereist. Elke waarde of expressie die kan worden geëvalueerd op TRUE of FALSE. |
| *[value_if_true]* | De waarde die u wilt zijn teruggekeerd als het *logical_test* argument aan WAAR evalueert. (Dit argument wordt standaard ingesteld op 0 als het niet wordt opgenomen.) |
| *[value_if_false]* | De waarde die u wilt zijn teruggekeerd als het *logical_test* argument aan VALS evalueert. (Dit argument wordt standaard ingesteld op 0 als het niet wordt opgenomen.) |

## Minder dan

Retourneert items waarvan het numerieke aantal kleiner is dan de ingevoerde waarde.

## Kleiner dan of gelijk aan

Retourneert items waarvan het numerieke getal kleiner dan of gelijk is aan de ingevoerde waarde.

## Optillen

Retourneert de Lift die een bepaalde variant had in conversies over een besturingsvariant. Dit is het verschil in prestaties tussen een bepaalde variant en de basislijn, gedeeld door de prestaties van de basislijn, uitgedrukt als een percentage.

```
fx Lift (normalizing-container, success-metric, control)
```

| Argument | Beschrijving |
| --- | --- |
| Container normaliseren | De basis (Mensen, Zittingen, of Gebeurtenissen) waarop een test zal worden in werking gesteld. |
| Metrisch met succes | De metrische of metrische waarde waarmee een gebruiker varianten vergelijkt. |
| Besturing | De variant waarmee alle andere varianten in het experiment worden vergeleken. Voer de naam in van het element Dimensie besturingsvariant. |

{style="table-layout:auto"}

## Lineaire regressie_ Correlatiecoëfficiënt

Y = a X + b. Retourneert de correlatiecoëfficiënt

## Lineaire regressie_ Intercept

Y = a X + b. Retourneert b.

## Lineaire regressie_ Voorspeld Y

Y = a X + b. Retourneert Y.

## Lineaire regressie_ Helling

Y = a X + b. Retourneert a.

## Logbasis 10 (rij)

Retourneert de natuurlijke logaritme met grondtal 10 van een getal.

```
LOG10(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Het positieve reële getal waarvoor u de natuurlijke logaritme met grondtal 10 wilt gebruiken. |

## Logregressie: Correlatiecoëfficiënt (tabel)

Keert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor de regressievergelijking [!DNL Y = a ln(X) + b] terug. Deze wordt berekend met behulp van de CORREL-vergelijking.

```
CORREL.LOG(metric_X,metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u met *wilt correleren metrisch_Y*. |
| *metrisch_Y* | Metrisch die u met *wilt correleren metrisch_X*. |

## Logregressie: Onderscheppen (tabel)

Keert intercept *b* als minste vierkantsregressie tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor de regressievergelijking [!DNL Y = a ln(X) + b] terug. Deze wordt berekend met behulp van de INTERCEPT-vergelijking.

```
INTERCEPT.LOG(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Logregressie: voorspelde Y (rij)

Berekent de voorspelde [!DNL y] -waarden (metrisch_Y), op basis van de bekende [!DNL x] -waarden (metrisch_X) met de methode &quot;kleinste vierkantjes&quot; voor het berekenen van de regel van best fit op basis van [!DNL Y = a ln(X) + b] . Deze wordt berekend met behulp van de ESTIMATE-vergelijking.

In regressieanalyse, berekent deze functie de voorspelde [!DNL y] waarden (*metrisch_Y*), gezien de bekende [!DNL x] waarden (*metrisch_X*) gebruikend logaritme voor het berekenen van de lijn van best past voor de regressievergelijking [!DNL Y = a ln(X) + b]. De [!DNL a] -waarden komen overeen met elke x-waarde en [!DNL b] is een constante waarde.

```
ESTIMATE.LOG(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Logregressie: helling (tabel)

Keert de helling, *a*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor de regressievergelijking [!DNL Y = a ln(X) + b] terug. Het wordt berekend gebruikend de vergelijking van de REEKS.

```
SLOPE.LOG(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_A* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_B* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Natuurlijk logboek

Retourneert de natuurlijke logaritme van een getal. Natuurlijk logaritmen zijn gebaseerd op constante *e* (2.71828182845904). LN is het omgekeerde van de functie EXP.

```
LN(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Het positieve reële getal waarvoor u de natuurlijke logaritme wilt. |

## NOT

Retourneert 1 als het getal 0 is of retourneert 0 als een ander getal.

```
NOT(logical)
```

| Argument | Beschrijving |
|---|---|
| *logisch* | Vereist. Een waarde of expressie die kan worden geëvalueerd op TRUE of FALSE. |

Het gebruik van NOT vereist weten of de expressies (&lt;, >, =, &lt;>, enz.) 0 of 1 waarden retourneren.

## Niet gelijk

Retourneert alle items die niet exact overeenkomen met de ingevoerde waarde.

## Of (rij)

Geeft TRUE terug als een argument TRUE is, of FALSE als alle argumenten FALSE zijn.

>[!NOTE]
>
>0 (nul) betekent Onwaar en elke andere waarde is Waar.

```
OR(logical_test1,[logical_test2],...)
```

| Argument | Beschrijving |
|---|---|
| *logical_test1* | Vereist. Elke waarde of expressie die kan worden geëvalueerd op TRUE of FALSE. |
| *logical_test2* | Optioneel. Aanvullende voorwaarden die u als TRUE of FALSE wilt evalueren |

## Pi

Retourneert de constante PI, 3.14159265358979, nauwkeurig tot 15 cijfers.

```
PI()
```

De [!DNL PI] functie heeft geen argumenten.

## Stroomregressie: Correlatiecoëfficiënt (tabel)

Keert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y = b*X] terug.

```
CORREL.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u met *wilt correleren metrisch_Y*. |
| *metrisch_Y* | Metrisch die u met *wilt correleren metrisch_X*. |

## Stroomregressie: Intercept (tabel)

Keert onderschepping, *b*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y = b*X] terug.

```
 INTERCEPT.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Stroomregressie: voorspeld Y (rij)

Berekent de voorspelde [!DNL y] -waarden ( [!DNL metric_Y] ), op basis van de bekende [!DNL x] -waarden ( [!DNL metric_X] ) met de methode &quot;kleinste vierkantjes&quot; voor het berekenen van de regel die het meest geschikt is voor [!DNL Y = b*X] .

```
 ESTIMATE.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Stroomregressie: helling (tabel)

Keert de helling, *a*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y = b*X] terug.

```
SLOPE.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Kwartaalregressie: Correlatiecoëfficiënt (tabel)

Keert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y=(a*X+b)] *** terug.

```
CORREL.QUADRATIC(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u met *wilt correleren metrisch_Y*. |
| *metrisch_Y* | Metrisch die u met *wilt correleren metrisch_X*. |

## Quadratische regressie: Intercept (tabel)

Keert onderschepping, *b*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y=(a*X+b)]*** terug.

```
INTERCEPT.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Quadratische regressie: voorspelde Y (rij)

Berekent de voorspelde [!DNL y] -waarden (metrisch_Y), op basis van de bekende [!DNL x] -waarden (metrisch_X) met de methode met de kleinste vierkantjes voor het berekenen van de best aangepaste regel met [!DNL Y=(a*X+b)] ****.

```
ESTIMATE.QUADRATIC(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_A* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_B* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |

## Kwadratische regressie: helling (tabel)

Keert de helling, *a*, tussen twee metrische kolommen (*metrisch_X* en metrisch_Y) voor [!DNL Y=(a*X+b)]*** terug.

```
SLOPE.QUADRATIC(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: Correlatiecoëfficiënt (tabel)

Keert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metrisch_X)* en *metrisch_Y*) voor [!DNL Y = a/X+b] terug.

```
CORREL.RECIPROCAL(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u met *wilt correleren metrisch_Y*. |
| *metrisch_Y* | Metrisch die u met *wilt correleren metrisch_X*. |

## Wederkerige regressie: Intercept (tabel)

Keert onderschepping, *b*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y = a/X+b] terug.

```
INTERCEPT.RECIPROCAL(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: voorspelde Y (rij)

Berekent de voorspelde [!DNL y] -waarden (metrisch_Y), op basis van de bekende [!DNL x] -waarden (metrisch_X) met behulp van de methode met de kleinste vierkantjes voor het berekenen van de best aangepaste regel met [!DNL Y = a/X+b] .

```
ESTIMATE.RECIPROCAL(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: helling (tabel)

Keert de helling, *a*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y = a/X+b] terug.

```
SLOPE.RECIPROCAL(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Sinus (rij)

Geeft als resultaat de sinus van de opgegeven hoek. Als de hoek in graden is, vermenigvuldig de hoek met PI()/180.

```
SIN(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor u de sinus wilt gebruiken. |

## T-score

Alias voor Z-score, d.w.z. de afwijking van het gemiddelde gedeeld door de standaardafwijking

## T-test

Voert een t-test uit met t-score van col en n vrijheidsgraden.

De handtekening is `t_test( x, n, m )` . Onder, roept het eenvoudig `m*cdf_t(-abs(x),n)`. (Dit is vergelijkbaar met de functie z-test die `m*cdf_z(-abs(x))` uitvoert.

Hier is `m` het aantal staarten. `n` is de mate van vrijheid. Dit moeten getallen zijn (constant voor het gehele rapport, d.w.z. niet op rij-voor-rij-basis).

`X` is de t-test statistiek en zou vaak een formule (bijvoorbeeld zscore) zijn die op een metrische waarde is gebaseerd en op elke rij wordt geëvalueerd.

De geretourneerde waarde is de waarschijnlijkheid dat de teststatistiek x gezien de vrijheidsgraad en het aantal staarten wordt weergegeven.

**Voorbeelden:**

1. Gebruik het om uitschieters te vinden:

   ```
   t_test( zscore(bouncerate), row-count-1, 2)
   ```

1. Combineer het met `if` om zeer hoge of lage stuiterende tarieven te negeren, en telbezoeken op alles te tellen:

   ```
   if ( t_test( z-score(bouncerate), row-count, 2) < 0.01, 0, visits )
   ```

## Raaklijn

Retourneert de tangens van de opgegeven hoek. Als de hoek in graden is, vermenigvuldig de hoek met PI()/180.

```
TAN (metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor u de tangens wilt. |

## Z-score (rij)

Geeft de Z-score, of de normale score, gebaseerd op een normale distributie. De Z-score is het aantal standaardafwijkingen dat een waarneming van het gemiddelde is. Een Z-score van 0 (nul) betekent dat de score gelijk is aan het gemiddelde. Een Z-score kan positief of negatief zijn en geeft aan of deze boven of onder het gemiddelde ligt en hoeveel standaardafwijkingen er zijn.

De vergelijking voor Z-score is:

![](../assets/z_score.png)

waarbij [!DNL x] de onbewerkte score is, [!DNL μ] het gemiddelde van de populatie is en [!DNL σ] de standaardafwijking van de populatie.

>[!NOTE]
>
>[!DNL μ] (mu) en [!DNL σ] (sigma) worden automatisch berekend van metrisch.

Z-score (metrisch)

<table id="table_AEA3622A58F54EA495468A9402651E1B">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Argument </th>
   <th colname="col2" class="entry"> Beschrijving </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> <i> metrisch </i> </td>
   <td colname="col2"> <p> Retourneert de waarde van het eerste argument anders dan nul. </p> </td>
  </tr>
 </tbody>
</table>

## Z-test

Voert een n-tailed Z-test met Z-score van A uit.

Retourneert de waarschijnlijkheid dat de huidige rij toevallig in de kolom kan worden weergegeven.

>[!NOTE]
>
>gaat ervan uit dat de waarden normaal worden verdeeld.

+++

