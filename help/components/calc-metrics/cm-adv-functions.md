---
title: Referentie - geavanceerde functies
description: U hebt toegang tot deze functies door Geavanceerd tonen in de vervolgkeuzelijst Functies te selecteren.
translation-type: tm+mt
source-git-commit: fc5a462f3d216d8cae3ce060a45ec79a44c4c918
workflow-type: tm+mt
source-wordcount: '2946'
ht-degree: 1%

---


# Referentie - geavanceerde functies

>[!NOTE] U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

U hebt toegang tot deze functies door deze te controleren **[!UICONTROL Show Advanced]** in de **[!UICONTROL Functions]** vervolgkeuzelijst.

## Tabelfuncties versus rijfuncties

Een tabelfunctie is een functie waarbij de uitvoer voor elke rij van de tabel hetzelfde is. Een rijfunctie is een functie waarbij de uitvoer voor elke rij van de tabel anders is.

## Wat betekent de Include-Zeros-parameter?

Het vertelt of nullen in de berekening moeten worden opgenomen. Soms betekent nul &quot;niets&quot;, maar soms is het belangrijk.

Bijvoorbeeld, als u metrisch van de Opbrengst hebt, en dan metrische vertoningen van de Pagina aan het rapport toevoegt, zijn er plotseling meer rijen voor uw opbrengst die allen nul zijn. U wilt waarschijnlijk niet dat dit invloed heeft op MEAN, MIN, QUARTILE, enzovoort. berekeningen die u op de opbrengstkolom hebt. In dat geval controleert u de parameter include-zeros.

Aan de andere kant, als u twee metriek hebt die u geinteresseerd in bent, kan het niet eerlijk zijn om te zeggen dat één een hoger gemiddelde of een minimum heeft omdat sommige van zijn rijen nul waren, zodat zou u niet de parameter controleren om nullen te omvatten.

## EN

Retourneert de waarde van het argument ervan. Gebruik NOT om ervoor te zorgen dat een waarde niet gelijk is aan één bepaalde waarde.

>[!NOTE] 0 (nul) betekent Onwaar en elke andere waarde is Waar.

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
| *dimensie* | De afmeting waarvoor u de benaderende verschillende punttelling wilt. |

## Voorbeeld: hoofdletter gebruiken

Het geschatte onderscheid van de Telling (klant ID eVar) is een gemeenschappelijk gebruiksgeval voor deze functie.

Definitie voor een nieuwe berekende metrische waarde &quot;Benaderende Klanten&quot;:

![](assets/approx-count-distinct.png)

Dit is hoe &quot;Benadert Klanten&quot;metrisch zou kunnen worden gebruikt in het melden van:

![](assets/approx-customers.png)

## Uniques Exceeded

Net als Count() en RowCount(), geldt bij benadering de limiet voor Distinct() voor tellen die wordt overschreden voor [&#39;unicques&#39;s](https://marketing.adobe.com/resources/help/en_US/reference/metrics_uniques_high_numbers.html). Als de limiet voor &quot;oneven overschreden&quot; binnen een bepaalde maand voor een dimensie wordt bereikt, wordt de waarde geteld als 1 dimensie-item.

## Telfuncties vergelijken

Distinct() is bij benadering een verbetering ten opzichte van de functies Count() en RowCount() omdat de gemaakte metrische waarde in elk dimensionaal rapport kan worden gebruikt om een geschatte telling van items voor een afzonderlijke dimensie te renderen. Bijvoorbeeld, een telling van klant IDs die in een Mobiel Rapport van het Type van Apparaat wordt gebruikt.

Deze functie zal marginaal minder nauwkeurig zijn dan Count() en RowCount() omdat het de methode HLL gebruikt, terwijl Count() en RowCount() exacte aantallen zijn.

## Boogcosinus (rij)

Retourneert de arccosinus, of omgekeerd van de cosinus, van een metrische waarde. De arccosinus is de hoek waarvan de cosinus getal is. De geretourneerde hoek wordt opgegeven in radialen in het bereik 0 (nul) tot pi. Als u het resultaat wilt omzetten van radialen in graden, vermenigvuldigt u het met 180/PI( ).

```
ACOS(metric)
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek die u wilt instellen van -1 tot en met 1. |

## Boogsinus (rij)

Retourneert de arcsinus, of omgekeerde sinus, van een getal. De arcsinus is de hoek waarvan de sinus een getal is. De geretourneerde hoek wordt opgegeven in radialen in het bereik -pi/2 tot pi/2. Als u de arcsinus in graden wilt uitdrukken, vermenigvuldigt u het resultaat met 180/PI( ).

```
ASIN(metric) 
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek die u wilt instellen van -1 tot en met 1. |

## Booghoek (rij)

Retourneert de arctangens, of omgekeerde tangens, van een getal. De arctangens is de hoek waarvan de tangens getal is. De geretourneerde hoek wordt opgegeven in radialen in het bereik -pi/2 tot pi/2. Als u de arctangens in graden wilt uitdrukken, vermenigvuldigt u het resultaat met 180/PI( ).

```
ATAN(metric)
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek die u wilt instellen van -1 tot en met 1. |

## Exponentiële regressie: Voorspeld Y (rij)

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

Geeft als resultaat het kleinste gehele getal dat niet kleiner is dan een bepaalde waarde. Als u bijvoorbeeld wilt voorkomen dat decimalen van valuta worden gerapporteerd voor inkomsten en een product $569,34 heeft, gebruikt u de formule CEILING( *Opbrengst*) om inkomsten te afronden tot de dichtstbijzijnde dollar, ofwel $570.

```
CEILING(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrische waarde die u wilt afronden. |

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

>[!NOTE] Dit werkt niet zoals u zou kunnen verwachten met tariefmetriek zoals opbrengst/bezoeker: het gemiddelde van de tarieven in plaats van de inkomsten over de laatste N op te tellen en bezoekers over de laatste N op te tellen en ze vervolgens te verdelen. Gebruik in plaats daarvan

```
cumul(revenue)/cumul(visitor)
```

## Gelijk

Retourneert items die exact overeenkomen voor een numerieke waarde of tekenreekswaarde.

## Exponentiële regressie_ correlatiecoëfficiënt (tabel)

Retourneert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen ( *metrische_A* en *metrische_B*) voor de regressievergelijking.

```
CORREL.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Een metrisch die u met *metrisch_Y* zou willen correleren. |
| *metrisch_Y* | Een metrisch die u met *metrisch_X* zou willen correleren. |

## Exponentiële regressie: Intercept (tabel)

Retourneert de onderschepping, *b*, tussen twee metrische kolommen ( *metrisch_X* en *metrisch_Y*) voor

```
INTERCEPT.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Exponentiële regressie: Helling (tabel)

Retourneert de helling, *a*, tussen twee metrische kolommen ( *metrische_X* en *metrische_Y*) voor .

```
SLOPE.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Vloer (rij)

Geeft als resultaat het grootste gehele getal dat niet groter is dan een bepaalde waarde. Als u bijvoorbeeld wilt voorkomen dat decimalen van valuta worden gerapporteerd voor inkomsten en een product heeft $569,34, gebruikt u de formule FLOOR( *Revenue*) om inkomsten naar beneden te afronden naar de dichtstbijzijnde dollar, ofwel $569.

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
| *[value_if_false]* | De waarde die u wilt worden geretourneerd als het argument *logical_test* naar FALSE evalueert. (Dit argument wordt standaard ingesteld op 0 als het niet wordt opgenomen.) |

## Minder dan

Retourneert items waarvan het numerieke aantal kleiner is dan de ingevoerde waarde.

## Kleiner dan of gelijk aan

Retourneert items waarvan het numerieke getal kleiner dan of gelijk is aan de ingevoerde waarde.

## Lineaire regressie_ Correlatiecoëfficiënt

Y = a X + b. Hiermee wordt de correlatiecoëfficiënt geretourneerd

## Lineaire regressie_ Intercept

Y = a X + b. Retourneert b.

## Lineaire regressie_ Voorspeld Y

Y = a X + b. Retourneert Y.

## Lineaire regressie_ Helling

Y = a X + b. Retourneert een.

## Logbasis 10 (rij)

Retourneert de natuurlijke logaritme met grondtal 10 van een getal.

```
LOG10(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Het positieve reële getal waarvoor u de natuurlijke logaritme met grondtal 10 wilt gebruiken. |

## Logregressie: Correlatiecoëfficiënt (tabel)

Retourneert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor de regressievergelijking [!DNL Y = a ln(X) + b]. Deze wordt berekend met behulp van de CORREL-vergelijking.

```
CORREL.LOG(metric_X,metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Een metrisch die u met *metrisch_Y* zou willen correleren. |
| *metrisch_Y* | Een metrisch die u met *metrisch_X* zou willen correleren. |

## Logregressie: Intercept (tabel)

Retourneert de onderschepping *b* als de kleinste kwadratenregressie tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor de regressievergelijking [!DNL Y = a ln(X) + b]. Deze wordt berekend met behulp van de INTERCEPT-vergelijking.

```
INTERCEPT.LOG(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Logboekregressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden (metrisch_Y), gezien de bekende [!DNL x] waarden (metrisch_X) gebruikend de &quot;minste vierkantjes&quot;methode voor het berekenen van de lijn van best past gebaseerd op [!DNL Y = a ln(X) + b]. Deze wordt berekend met behulp van de ESTIMATE-vergelijking.

In regressieanalyse, berekent deze functie de voorspelde [!DNL y] waarden (*metrisch_Y*), gezien de bekende [!DNL x] waarden (*meetkunde_X*) gebruikend logaritme voor het berekenen van de lijn van best geschikt voor de regressievergelijking [!DNL Y = a ln(X) + b]. De [!DNL a] waarden komen overeen met elke x-waarde en [!DNL b] zijn een constante waarde.

```
ESTIMATE.LOG(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Logregressie: Helling (tabel)

Retourneert de helling, *a*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor de regressievergelijking [!DNL Y = a ln(X) + b]. Het wordt berekend gebruikend de vergelijking van de REEKS.

```
SLOPE.LOG(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_A* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_B* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Natuurlijk logboek

Retourneert de natuurlijke logaritme van een getal. Natuurlijke logaritmen zijn gebaseerd op de constante *e* (2,71828182845904). LN is het omgekeerde van de functie EXP.

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

>[!NOTE] 0 (nul) betekent Onwaar en elke andere waarde is Waar.

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

De [!DNL PI]functie heeft geen argumenten.

## Stroomregressie: Correlatiecoëfficiënt (tabel)

Retourneert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y = b*X].

```
CORREL.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Een metrisch die u met *metrisch_Y* zou willen correleren. |
| *metrisch_Y* | Een metrisch die u met *metrisch_X* zou willen correleren. |

## Stroomregressie: Intercept (tabel)

Retourneert de onderschepping, *b*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y = b*X].

```
 INTERCEPT.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Stroomregressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden ( [!DNL metric_Y]), op basis van de bekende [!DNL x] waarden ( [!DNL metric_X]) met behulp van de methode &quot;kleinste vierkantjes&quot; voor het berekenen van de regel die het best geschikt is voor [!DNL Y = b*X].

```
 ESTIMATE.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Stroomregressie: Helling (tabel)

Retourneert de helling, *a*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y = b*X].

```
SLOPE.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Quadratische regressie: Correlatiecoëfficiënt (tabel)

Retourneert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metrische_X* en *metrische_Y*) voor [!DNL Y=(a*X+b)]****.

```
CORREL.QUADRATIC(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Een metrisch die u met *metrisch_Y* zou willen correleren. |
| *metrisch_Y* | Een metrisch die u met *metrisch_X* zou willen correleren. |

## Quadratische regressie: Intercept (tabel)

Retourneert de onderschepping, *b*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y=(a*X+b)]****.

```
INTERCEPT.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Quadratische regressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden (metrisch_Y), op basis van de bekende [!DNL x] waarden (metrisch_X) met behulp van de kleinste-kwadratenmethode voor het berekenen van de best fit met behulp van [!DNL Y=(a*X+b)]***.

```
ESTIMATE.QUADRATIC(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_A* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_B* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |

## Quadratische regressie: Helling (tabel)

Retourneert de helling, *a*, tussen twee metrische kolommen (*metrisch_X* en metrisch_Y) voor [!DNL Y=(a*X+b)]***.

```
SLOPE.QUADRATIC(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: Correlatiecoëfficiënt (tabel)

Retourneert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metrische_X)* en *metrische_Y*) voor [!DNL Y = a/X+b].

```
CORREL.RECIPROCAL(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Een metrisch die u met *metrisch_Y* zou willen correleren. |
| *metrisch_Y* | Een metrisch die u met *metrisch_X* zou willen correleren. |

## Wederkerige regressie: Intercept (tabel)

Retourneert de onderschepping, *b*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y = a/X+b].

```
INTERCEPT.RECIPROCAL(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden (metrisch_Y), gezien de bekende [!DNL x] waarden (metrisch_X) gebruikend de minste vierkantsmethode voor het berekenen van de lijn van best past het gebruiken [!DNL Y = a/X+b].

```
ESTIMATE.RECIPROCAL(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: Helling (tabel)

Retourneert de helling, *a*, tussen twee metrische kolommen (*metrisch_X* en *metrisch_Y*) voor [!DNL Y = a/X+b].

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

De handtekening is `t_test( x, n, m )`. Ondertussen roept het gewoon `m*cdf_t(-abs(x),n)`. (Dit is vergelijkbaar met de functie z-test die wordt uitgevoerd `m*cdf_z(-abs(x))`.

Hier `m` is het aantal staarten, en `n` is de vrijheidsgraad. Dit moeten getallen zijn (constant voor het gehele rapport, d.w.z. niet op rij-voor-rij-basis).

`X` is de t-test statistiek en zou vaak een formule (bv. zscore) zijn die op metrisch wordt gebaseerd en op elke rij wordt geëvalueerd.

De geretourneerde waarde is de waarschijnlijkheid dat de teststatistiek x gezien de vrijheidsgraad en het aantal staarten wordt weergegeven.

**Voorbeelden:**

1. Gebruik het om uitschieters te vinden:

   ```
   t_test( zscore(bouncerate), row-count-1, 2)
   ```

1. Combineer het met `if` om zeer hoge of lage stuiterende tarieven te negeren, en de bezoeken van de telling op al het andere te tellen:

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

![](assets/z_score.png)

waar [!DNL x] de onbewerkte score is, [!DNL μ] is het gemiddelde van de populatie en [!DNL σ] is de standaardafwijking van de populatie.

>[!NOTE] [!DNL μ] (mu) en (sigma[!DNL σ] ) worden automatisch berekend op basis van de meting.

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
   <td colname="col1"> <i>metrisch</i> </td> 
   <td colname="col2"> <p> Retourneert de waarde van het eerste argument anders dan nul. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Z-test

Voert een n-tailed Z-test met Z-score van A uit.

Retourneert de waarschijnlijkheid dat de huidige rij toevallig in de kolom kan worden weergegeven.

>[!NOTE] gaat ervan uit dat de waarden normaal worden verdeeld.

