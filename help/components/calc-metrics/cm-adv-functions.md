---
title: Referentie - geavanceerde functies
description: Heb toegang tot deze functies door te controleren tonen Geavanceerd in de drop-down lijst van Functies.
translation-type: tm+mt
source-git-commit: b521079bb9b3828ec3487b635366f5442f6fc4bd

---


# Referentie - geavanceerde functies

Heb toegang tot deze functies door **[!UICONTROL Show Advanced]** in de **[!UICONTROL Functions]** drop-down lijst te controleren.

## Tabel Functies versus Row-functies

Een lijstfunctie is één waar de output het zelfde voor elke rij van de lijst is. Een rijfunctie is één waar de output voor elke rij van de lijst verschillend is.

## Wat betekent de Include-Zeros parameter?

Het vertelt of om nul in de berekening te omvatten. Soms betekent nul &quot;niets&quot;, maar soms is het belangrijk.

Bijvoorbeeld, als u metrisch van de Opbrengst hebt, en voeg dan metrisch de Meningen van de Pagina aan het rapport toe, zijn er plotseling meer rijen voor uw opbrengst die allen nul zijn. Je wilt waarschijnlijk niet dat dit invloed heeft op een MEAN, MIN, QUARTILE, enzovoort. berekeningen die u op de opbrengstkolom hebt. In dit geval, zou u de include-zeros parameter controleren.

Aan de andere kant, als u twee metriek hebt die u in geinteresseerd bent, kan het niet eerlijk zijn om te zeggen dat één een hoger gemiddelde of minimum heeft omdat sommige van zijn rijen nul waren, zodat zou u niet de parameter controleren om nul te omvatten.

## EN

Geeft de waarde van zijn argument terug. Gebruik NIET om ervoor te zorgen dat een waarde niet gelijk aan één bepaalde waarde is.

> [!NOTE] 0 (nul) betekent Vals, en om het even welke andere waarde is Waar.

```
AND(logical_test1,[logical_test2],...)
```

| Argument | Beschrijving |
|---|---|
| *logical_test1* | Vereist. Om het even welke waarde of uitdrukking die aan WAAR of VALS kan worden geëvalueerd. |
| *logical_test2* | Optioneel. Extra voorwaarden die u als WAAR of VALS wilt evalueren |

## Geschatte graafscheiding (dimensie)

Keert de benaderende verschillende telling van afmetingspunten voor de geselecteerde afmeting terug. De functie gebruikt de methode HyperLogLog (HLL) om verschillende tellingen te benaderen.  Het wordt gevormd om de waarde te waarborgen is binnen 5% van de daadwerkelijke waarde 95% van de tijd.

```
Approximate Count Distinct (dimension)
```

| Argument |  |
|---|---|
| *dimensie* | De afmeting waarvoor u de benaderende verschillende punttelling wilt. |

## Voorbeeld Gebruiksscenario

Het Geschatte Afwijken van de Telling (klant identiteitskaart eVar) is een gemeenschappelijk gebruiksgeval voor deze functie.

Definitie voor een nieuwe &quot;Approximate Klanten&quot;berekende metrisch:

![](assets/approx-count-distinct.png)

Dit is hoe metrisch &quot;Approximate Klanten&quot;in rapportering zou kunnen worden gebruikt:

![](assets/approx-customers.png)

## Uniques overschreden

Net als Count() en RowCount() is Approximate Count Distinct() onderworpen aan [&quot;uniques boven&quot; limieten](https://marketing.adobe.com/resources/help/en_US/reference/metrics_uniques_high_numbers.html). Indien de &quot;overschrijding van de uniques&quot;-limiet binnen een bepaalde maand voor een dimensie wordt bereikt, wordt de waarde geteld als 1-afmeting-item.

## Het vergelijken van de Functies van de Telling

Approximate Count Distinct() is een verbetering over Count() en RowCount() functies omdat metrisch gecreeerd in om het even welk dimensionaal rapport kan worden gebruikt om een benaderende telling van punten voor een afzonderlijke afmeting terug te geven. Bijvoorbeeld, een telling van klant IDs die in een Mobiel rapport van het Type van Apparaat wordt gebruikt.

Deze functie zal marginaal minder nauwkeurig zijn dan Count() en RowCount() omdat het de methode HLL gebruikt, terwijl Count() en RowCount() het exacte aantal zijn.

## Arc Cosine (rij)

Geeft de arccosine, of omgekeerd van de cosine, van metrisch terug. De arccosine is de hoek waarvan de cosinus het getal is. De teruggekeerde hoek wordt gegeven in radianten in waaier 0 (nul) aan pi. Als je het resultaat van radialen wilt omzetten in graden, vermenigvuldig het dan met 180/PI( ).

```
ACOS(metric)
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek u van -1 tot 1 wilt. |

## Boog sinus (rij)

Geeft de arcsinus, of omgekeerde sinus, van een getal. De arcsinus is de hoek waarvan de sinus aantal is. De teruggekeerde hoek wordt gegeven in radianten in waaier - pi/2 aan pi/2. Om de arcsinus in graden uit te drukken, vermenigvuldig het resultaat met 180/PI ( ).

```
ASIN(metric) 
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek u van -1 tot 1 wilt. |

## Boog tang (rij)

Keert de noordtangens, of omgekeerde raaklijn, van een aantal terug. De noordtangens is de hoek de waarvan raaklijn aantal is. De teruggekeerde hoek wordt gegeven in radianten in waaier - pi/2 aan pi/2. Om de arctangens in graden uit te drukken, vermenigvuldig het resultaat met 180/PI ( ).

```
ATAN(metric)
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek u van -1 tot 1 wilt. |

## Exponentiële regressie: Voorspeld Y (rij)

Berekent de voorspelde y-waarden (metric_Y), gegeven de bekende x-waarden (metric_X) gebruikend de &quot;minste kwadraten&quot;methode om de lijn van best te berekenen geschikt gebaseerd op.

```
ESTIMATE.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Cdf-T

Keert het percentage van waarden in de t-distributie van een student met n graden van vrijheid terug die een z-score minder dan x hebben.

```
cdf_t( -∞, n ) = 0 
cdf_t(  ∞, n ) = 1 
cdf_t( 3, 5 ) ? 0.99865 
cdf_t( -2, 7 ) ? 0.0227501 
cdf_t( x, ∞ ) ? cdf_z( x )
```

## Cdf-Z

Keert het percentage waarden in een normale distributie terug die een z-score minder dan x hebben.

```
cdf_z( -∞ ) = 0 
cdf_z( ∞ ) = 1 
cdf_z( 0 ) = 0.5 
cdf_z( 2 ) ? 0.97725 
cdf_z( -3 ) ? 0.0013499 
 
```

## Plafond (rij)

Keert het kleinste geheel niet minder dan een bepaalde waarde terug. Bijvoorbeeld, als u het melden van muntdecimalen voor opbrengst wilt vermijden en een product $569.34 heeft, gebruik de formule CEILING ( *Opbrengst*) aan ronde opbrengst tot de dichtstbijzijnde dollar, of $570.

```
CEILING(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrisch die u wilt ronden. |

## Cosine (rij)

Keert de cosinus van de bepaalde hoek terug. Als de hoek in graden is, vermenigvuldig de hoek met PI( )/180.

```
COS(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor je de cosinus wilt. |

## Cube Root

Keert de positieve kubuswortel van een aantal terug. De kubuswortel van een aantal is de waarde van dat aantal dat aan de macht van 1/3 wordt opgeheven.

```
CBRT(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Metrisch waarvoor u de kubuswortel wilt. |

## Cumulatief

Keert de som van x voor de laatste N rijen (zoals die door de afmeting wordt bevolen, terug gebruikend knoeiboelwaarden voor koord gebaseerde gebieden).

Als N &lt;= 0 gebruikt het alle vorige rijen. Aangezien het door de afmeting wordt bevolen is het slechts nuttig op afmetingen die een natuurlijke orde zoals datum of weglengte hebben.

```
| Date | Rev  | cumul(0,Rev) | cumul(2,Rev) | 
|------+------+--------------+--------------| 
| May  | $500 | $500         | $500         | 
| June | $200 | $700         | $700         | 
| July | $400 | $1100        | $600         | 
 
```

## Cumulatief gemiddelde

Keert het gemiddelde van de laatste rijen van N terug.

Als N &lt;= 0 gebruikt het alle vorige rijen. Aangezien het door de afmeting wordt bevolen is het slechts nuttig op afmetingen die een natuurlijke orde zoals datum of weglengte hebben.

> [!NOTE] Dit werkt niet zoals u met tariefmetriek zoals opbrengst/bezoeker zou kunnen verwachten: het gemiddelde van de tarieven, in plaats van de inkomsten over de laatste N op te tellen en bezoekers op de laatste N op te tellen en ze vervolgens te verdelen. In plaats daarvan, gebruik

```
cumul(revenue)/cumul(visitor)
```

## Gelijk

Keert punten terug die precies voor een numerieke of koordwaarde aanpassen.

## Exponentiële regressie_ correlatiecoëfficiënt (tabel)

Keert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen ( *metric_A* en *metric_B*) voor de regressievergelijking terug.

```
CORREL.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u met *metric_Y* zou willen correleren. |
| *Metrisch_Y* | Metrisch die u met *metric_X* zou willen correleren. |

## Exponentiële regressie: Intercept (tabel)

Keert het onderschepsel, *b*, tussen twee metrische kolommen ( *metric_X* en *metric_Y*) voor terug

```
INTERCEPT.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Exponentiële regressie: Helling (tabel)

Keert de helling, *a*, tussen twee metrische kolommen ( *metric_X* en *metric_Y*) voor terug.

```
SLOPE.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Vloer (rij)

Keert het grootste geheel terug niet groter dan een bepaalde waarde. Bijvoorbeeld, als u het melden van muntdecimalen voor opbrengst wilt vermijden en een product $569.34 heeft, gebruik de formule FLOOR ( *Opbrengst*) aan ronde opbrengst neer aan de dichtstbijzijnde dollar, of $569.

```
FLOOR(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrisch u wilt ronden. |

## Groter dan

Keert punten terug de waarvan numerieke telling groter is dan de ingegane waarde.

## Groter dan of gelijk

Keert punten terug de waarvan numerieke telling groter dan of gelijk aan de ingegane waarde is.

## Hyperbolische cosine (rij)

Geeft de hyperbolische cosinus van een getal terug.

```
COSH(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor je de hyperbolische cosinus wilt vinden. |

## Hyperbolische sinus (rij)

Geeft de hyperbolische sinus van een getal terug.

```
SINH(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor je de hyperbolische sinus wilt vinden. |

## Hyperbolisch tangent (rij)

Geeft de hyperbolische tangens van een getal terug.

```
TANH(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor je de hyperbolische tanget wilt vinden. |

## IF (rij)

De IF-functie retourneert één waarde als een voorwaarde die u opgeeft evalueert tot TRUE, en een andere waarde als die voorwaarde evalueert tot FALSE.

```
IF(logical_test, [value_if_true], [value_if_false])
```

| Argument | Beschrijving |
|---|---|
| *logical_test* | Vereist. Om het even welke waarde of uitdrukking die aan WAAR of VALS kan worden geëvalueerd. |
| *[waarde_if_true]* | De waarde die u wilt zijn teruggekeerd als het *logical_test* argument aan WAAR evalueert. (Dit argument blijft aan 0 in gebreke als niet inbegrepen.) |
| *[value_if_false]* | De waarde die u wilt zijn teruggekeerd als het *logical_test* argument aan VALS evalueert. (Dit argument blijft aan 0 in gebreke als niet inbegrepen.) |

## Minder dan

Keert punten terug de waarvan numerieke telling minder dan de ingegane waarde is.

## Minder dan of gelijk aan

Keert punten terug de waarvan numerieke telling minder dan of gelijk aan de ingegane waarde is.

## Lineaire regressie_ correlatiecoëfficiënt

Y = X + b. Geeft de correlatiecoëfficiënt terug

## Lineaire regressie_ Intercept

Y = X + b. Retourzendingen b.

## Lineaire regressie_ Voorspeld Y

Y = X + b. Geeft Y terug.

## Lineaire regressie_ Slope

Y = X + b. Geeft a.

## Logbasis 10 (rij)

Keert de basis-10 logaritme van een aantal terug.

```
LOG10(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Het positieve echte aantal waarvoor u de basis-10 logaritme wilt. |

## Gerregressie van het stamhout: Correlatiecoëfficiënt (tabel)

Keert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metric_X* en *metric_Y*) voor de regressievergelijking terug [!DNL Y = a ln(X) + b]. Het wordt berekend met behulp van de CORREL vergelijking.

```
CORREL.LOG(metric_X,metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u met *metric_Y* zou willen correleren. |
| *Metrisch_Y* | Metrisch die u met *metric_X* zou willen correleren. |

## Gerregressie van het stamhout: Intercept (tabel)

Keert intercept *b* als minste vierkantsregressie tussen twee metrische kolommen (*metric_X* en *metric_Y*) voor de regressievergelijking terug [!DNL Y = a ln(X) + b]. Het wordt berekend gebruikend de vergelijking INTERCEPT.

```
INTERCEPT.LOG(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Logboekregressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden (metric_Y), gezien de bekende [!DNL x] waarden (metric_X) gebruikend de &quot;minste kwadraten&quot;methode om de lijn van best te berekenen geschikt gebaseerd op [!DNL Y = a ln(X) + b]. Het wordt berekend gebruikend de ESTIMATE vergelijking.

In regressieanalyse, berekent deze functie de voorspelde [!DNL y] waarden (*metric_Y*), gezien de bekende [!DNL x] waarden (*metric_X*) gebruikend logaritme voor het berekenen van de lijn van het best geschikt voor de regressievergelijking [!DNL Y = a ln(X) + b]. De [!DNL a] waarden beantwoorden aan elke x waarde, en [!DNL b] is een constante waarde.

```
ESTIMATE.LOG(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Gerregressie van het stamhout: Helling (tabel)

Keert de helling, *a*, tussen twee metrische kolommen (*metric_X* en *metric_Y*) voor de regressievergelijking terug [!DNL Y = a ln(X) + b]. Het wordt berekend gebruikend de vergelijking van de SLOOP.

```
SLOPE.LOG(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_A* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_B* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Natuurlijk logboek

Keert de natuurlijke logaritme van een aantal terug. Natuurlijke logaritmen zijn gebaseerd op constante *e* (2.71828182845904). LN is het omgekeerde van de functie EXP.

```
LN(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Het positieve echte getal waarvoor je de natuurlijke logaritme wilt. |

## NIET

Keert 1 terug als het aantal 0 is of 0 terugkeert als een ander aantal.

```
NOT(logical)
```

| Argument | Beschrijving |
|---|---|
| *logisch* | Vereist. Een waarde of een uitdrukking die aan WAAR of VALS kan worden geëvalueerd. |

Het gebruiken van NIET vereist het weten of de uitdrukkingen (&lt;, >, =, &lt;>, enz.) keer 0 of 1 waarden terug.

## Niet gelijk

Keert alle punten terug die niet de nauwkeurige gelijke van de ingegane waarde bevatten.

## Of (rij)

Geeft TRUE terug als een argument WAAR is, of geeft FALSE terug als alle argumenten FALSE zijn.

> [!NOTE] 0 (nul) betekent Vals, en om het even welke andere waarde is Waar.

```
OR(logical_test1,[logical_test2],...)
```

| Argument | Beschrijving |
|---|---|
| *logical_test1* | Vereist. Om het even welke waarde of uitdrukking die aan WAAR of VALS kan worden geëvalueerd. |
| *logical_test2* | Optioneel. Extra voorwaarden die u als WAAR of VALS wilt evalueren |

## Pi

Geeft de constante PI, 3.14159265358979, nauwkeurig aan 15 cijfers.

```
PI()
```

De [!DNL PI]functie heeft geen argumenten.

## Stroomregressie: Correlatiecoëfficiënt (tabel)

Keert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metric_X* en *metric_Y*) voor [!DNL Y = b*X]terug.

```
CORREL.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u met *metric_Y* zou willen correleren. |
| *Metrisch_Y* | Metrisch die u met *metric_X* zou willen correleren. |

## Stroomregressie: Intercept (tabel)

Keert het onderschepsel, *b*, tussen twee metrische kolommen (*metric_X* en *metric_Y*) voor [!DNL Y = b*X]terug.

```
 INTERCEPT.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Stroomregressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden ( [!DNL metric_Y]), gegeven de bekende [!DNL x] waarden ( [!DNL metric_X]) gebruikend de &quot;minste kwadraten&quot;methode om de lijn van het best geschikt voor te berekenen [!DNL Y = b*X].

```
 ESTIMATE.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Stroomregressie: Helling (tabel)

Keert de helling, *a*, tussen twee metrische kolommen (*metric_X* en *metric_Y*) voor [!DNL Y = b*X]terug.

```
SLOPE.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Quadratische regressie: Correlatiecoëfficiënt (tabel)

Geeft de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metric_X* en *metric_Y*) voor [!DNL Y=(a*X+b)]*****.

```
CORREL.QUADRATIC(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u met *metric_Y* zou willen correleren. |
| *Metrisch_Y* | Metrisch die u met *metric_X* zou willen correleren. |

## Quadratische regressie: Intercept (tabel)

Geeft het intercept, *b*, tussen twee metrische kolommen (*metric_X* en *metric_Y*) voor [!DNL Y=(a*X+b)]***** terug.

```
INTERCEPT.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Quadratische regressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden (metric_Y), gegeven de bekende [!DNL x] waarden (metric_X) gebruikend de minste kwadratenmethode om de lijn van best fit te berekenen gebruikend [!DNL Y=(a*X+b)]****.

```
ESTIMATE.QUADRATIC(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_A* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_B* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |

## Quadratische regressie: Helling (tabel)

Keert de helling, *a*, tussen twee metrische kolommen (*metric_X* en metric_Y) voor [!DNL Y=(a*X+b)]***** terug.

```
SLOPE.QUADRATIC(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: Correlatiecoëfficiënt (tabel)

Keert de correlatiecoëfficiënt, *r*, tussen twee metrische kolommen (*metric_X)* en *metric_Y*) voor [!DNL Y = a/X+b]terug.

```
CORREL.RECIPROCAL(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u met *metric_Y* zou willen correleren. |
| *Metrisch_Y* | Metrisch die u met *metric_X* zou willen correleren. |

## Wederkerige regressie: Intercept (tabel)

Keert het onderschepsel, *b*, tussen twee metrische kolommen (*metric_X* en *metric_Y*) voor [!DNL Y = a/X+b]terug.

```
INTERCEPT.RECIPROCAL(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden (metric_Y), gezien de bekende [!DNL x] waarden (metric_X) gebruikend de minste kwadratenmethode om de lijn van best te berekenen past gebruikend [!DNL Y = a/X+b].

```
ESTIMATE.RECIPROCAL(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: Helling (tabel)

Keert de helling, *a*, tussen twee metrische kolommen (*metric_X* en *metric_Y*) voor [!DNL Y = a/X+b]terug.

```
SLOPE.RECIPROCAL(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Zine (rij)

Keert de sinus van de bepaalde hoek terug. Als de hoek in graden is, vermenigvuldig de hoek met PI( )/180.

```
SIN(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor je de sinus wilt. |

## T-score

Alias voor Z-Score, namelijk de afwijking van het gemiddelde gedeeld door de standaardafwijking

## T-test

Voert een t-test met een mat met t-score van koel en n vrijheidsgraden uit.

De handtekening is `t_test( x, n, m )`. Onderdoor roept het simpelweg `m*cdf_t(-abs(x),n)`. (Dit is gelijkaardig aan de z-test functie die loopt `m*cdf_z(-abs(x))`.

Hier `m` is het aantal staarten, en `n` is de mate van vrijheid. Dit moeten cijfers zijn (constant voor het gehele rapport, d.w.z. niet veranderend op rij per rijbasis).

`X` is de t-test-statistiek, en zou vaak een formule (bv. zscore) zijn die op metrisch wordt gebaseerd en op elke rij zal worden geëvalueerd.

De terugkeerwaarde is de waarschijnlijkheid om de teststatistiek x gezien de graden van vrijheid en het aantal staarten te zien.

**Voorbeelden:**

1. Gebruik het om uitschieters te vinden:

   ```
   t_test( zscore(bouncerate), row-count-1, 2)
   ```

1. Combineer het met `if` om zeer hoge of lage sprongtarieven te negeren, en tellingsbezoeken op al het andere:

   ```
   if ( t_test( z-score(bouncerate), row-count, 2) < 0.01, 0, visits )
   ```

## Tangent

Keert de tangens van de bepaalde hoek terug. Als de hoek in graden is, vermenigvuldig de hoek met PI( )/180.

```
TAN (metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor je de raaklijn wilt. |

## Z-score (rij)

Keert de Z-score, of normale score terug, die op een normale distributie wordt gebaseerd. De Z-score is het aantal standaardafwijkingen dat een waarneming van het gemiddelde is. Een Z-score van 0 (nul) betekent dat de score gelijk is aan het gemiddelde. Een Z-score kan positief of negatief zijn, die erop wijst of het boven of onder het gemiddelde is en door hoeveel standaardafwijkingen.

De vergelijking voor Z-score is:

![](assets/z_score.png)

waar [!DNL x] de ruwe score is, [!DNL μ] is het gemiddelde van de populatie, en [!DNL σ] is de standaardafwijking van de populatie.

> [!NOTE] [!DNL μ] (mu) en[!DNL σ] (sigma) worden automatisch berekend uit metrisch.

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
   <td colname="col2"> <p> Keert de waarde van zijn eerste non-zero argument terug. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Z-test

Voert een n-tailed Z-test uit met Z-score van A.

Keert de waarschijnlijkheid terug dat de huidige rij toevallig in de kolom kon worden gezien.

> [!NOTE] Veronderstelt dat de waarden normaal verdeeld zijn.

