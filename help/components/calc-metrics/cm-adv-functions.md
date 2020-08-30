---
title: Referentie - geavanceerde functies
description: Heb toegang tot deze functies door te controleren tonen Geavanceerd in de drop-down lijst van Functies.
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '2946'
ht-degree: 1%

---


# Referentie - geavanceerde functies

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Heb toegang tot deze functies door te controleren **[!UICONTROL Show Advanced]** in de **[!UICONTROL Functions]** vervolgkeuzelijst.

## Tabelfuncties versus roerfuncties

Een lijstfunctie is één waar de output het zelfde voor elke rij van de lijst is. Een rijfunctie is één waar de output voor elke rij van de lijst verschillend is.

## Wat betekent de include-Zeros parameter?

Het vertelt of om nul in de berekening te omvatten. Soms betekent nul &quot;niets&quot;, maar soms is het belangrijk.

Bijvoorbeeld, als u metrisch van de Opbrengst hebt, en dan een Metrische Meningen van de Pagina aan het rapport toevoegen, zijn er plotseling meer rijen voor uw opbrengst die allen nul zijn. Je wilt waarschijnlijk niet dat dit invloed heeft op een MEAN, MIN, QUARTILE, enz. berekeningen die u op de opbrengstkolom hebt. In dit geval, zou u de include-zeros parameter controleren.

Anderzijds, als u twee metriek hebt u in geinteresseerd bent, kan het niet eerlijk zijn om te zeggen dat één een hoger gemiddelde of minimum heeft omdat sommige van zijn rijen nul waren, zodat zou u niet de parameter controleren om nul te omvatten.

## EN

Geeft de waarde van zijn argument terug. Gebruik NIET om ervoor te zorgen dat een waarde niet gelijk aan één bepaalde waarde is.

>[!NOTE]
>
>0 (nul) betekent Vals, en een andere waarde is Waar.

```
AND(logical_test1,[logical_test2],...)
```

| Argument | Beschrijving |
|---|---|
| *logical_test1* | Vereist. Om het even welke waarde of uitdrukking die aan WAAR of VALS kunnen worden geëvalueerd. |
| *logical_test2* | Optioneel. Extra condities die je wilt evalueren als TRUE of FALSE |

## Afwijkende telling (dimensie)

Keert de benaderende verschillende telling van afmetingspunten voor de geselecteerde afmeting terug. De functie gebruikt de methode HyperLogLog (HLL) om verschillende tellingen te benaderen.  Het wordt gevormd om de waarde te waarborgen binnen 5% van de daadwerkelijke waarde 95% van de tijd is.

```
Approximate Count Distinct (dimension)
```

| Argument |  |
|---|---|
| *dimensie* | De afmeting waarvoor u de benaderende verschillende punttelling wilt. |

## Voorbeeld Gebruiksscenario

Het geschatte Telling Distinct (klantenidentiteitskaart eVar) is een gemeenschappelijk gebruiksgeval voor deze functie.

Definitie voor nieuwe &quot;Approximate Customers&quot;berekende metrisch:

![](assets/approx-count-distinct.png)

Dit is hoe metrisch &quot;Approximate Klanten&quot;in rapportering zou kunnen worden gebruikt:

![](assets/approx-customers.png)

## Uniques overschreden

Net als Count() en RowCount() is Approximate Count Distinct() onderworpen aan [Grenswaarden voor &quot;overschrijding van uniques&quot;](https://marketing.adobe.com/resources/help/en_US/reference/metrics_uniques_high_numbers.html). Indien de grenswaarde voor &quot;overschrijding uniques&quot; binnen een bepaalde maand voor een dimensie wordt bereikt, wordt de waarde geteld als 1 dimensiepunt.

## Het vergelijken van de Functies van de Telling

Approximate Count Distinct() is een verbetering over Count() en RowCount() functies omdat metrisch gecreeerd in om het even welk dimensionaal rapport kan worden gebruikt om een benaderende telling van punten voor een afzonderlijke afmeting terug te geven. Bijvoorbeeld, een telling van klant IDs die in een Mobiel rapport van het Type van Apparaat wordt gebruikt.

Deze functie zal marginaal minder nauwkeurig zijn dan Count() en RowCount() omdat het de methode HLL gebruikt, terwijl Count() en RowCount() precies tellen zijn.

## Arc Cosine (rij)

Keert het arccosine, of omgekeerd van de cosinus, van metrisch terug. Het arccosine is de hoek waarvan cosinus nummer is. De teruggekeerde hoek wordt gegeven in radianten in waaier 0 (nul) aan pi. Als je het resultaat van radianten wilt omzetten in graden, vermenigvuldig je het dan met 180/PI( ).

```
ACOS(metric)
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek u van -1 tot 1 wilt. |

## Boog sinus (rij)

Geeft de arcsinus, of omgekeerde sinus, van een getal terug. Het arcsine is de hoek waarvan de sinus aantal is. De teruggekeerde hoek wordt gegeven in radialen in het bereik -pi/2 tot pi/2. Om het arcsine in graden uit te drukken, vermenigvuldig het resultaat met 180/PI ( ).

```
ASIN(metric) 
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek u van -1 tot 1 wilt. |

## boogkanteling (rij)

Keert de noordtangens, of omgekeerde tangens, van een aantal terug. De noordtangens zijn de hoek waarvan de raaklijn aantal is. De teruggekeerde hoek wordt gegeven in radialen in het bereik -pi/2 tot pi/2. Om de arctangens in graden uit te drukken, vermenigvuldig het resultaat met 180/PI ( ).

```
ATAN(metric)
```

| Argument |  |
|---|---|
| *metrisch* | De cosinus van de hoek u van -1 tot 1 wilt. |

## Exponentiële regressie: Voorspeld Y (rij)

Berekent de voorspelde y-waarden (metric_Y), gezien de bekende x-waarden (metric_X) gebruikend de &quot;minste kwadraten&quot;methode om de lijn van best te berekenen geschikt gebaseerd op.

```
ESTIMATE.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Cdf-T

Keert het percentage waarden in de t-distributie van een student met n graden van vrijheid terug die een z-score minder dan x hebben.

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

Keert het kleinste geheel niet minder dan een bepaalde waarde terug. Bijvoorbeeld, als u het melden van muntdecimalen voor opbrengst wilt vermijden en een product $569.34 heeft, gebruik de formule CEILING ( *Ontvangsten*) om inkomsten tot de dichtstbijzijnde dollar, of $570, te genereren.

```
CEILING(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Metrisch die u wilt rond maken. |

## Cosine (rij)

Keert de cosinus van de bepaalde hoek terug. Als de hoek in graden is, vermenigvuldig de hoek met PI( )/180.

```
COS(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor je de cosinus wilt. |

## Keukenroet

Keert de positieve kubuswortel van een aantal terug. De kubuswortel van een aantal is de waarde van dat aantal dat aan de macht van 1/3 wordt opgeheven.

```
CBRT(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Metrisch waarvoor u de kubuswortel wilt. |

## Cumulatief

Keert de som van x voor de laatste N rijen (zoals bevolen door de afmeting, gebruikend knoeiboelwaarden voor koord gebaseerde gebieden) terug.

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

>[!NOTE]
>
>Dit werkt niet zoals u met tariefmetriek zoals opbrengst/bezoeker zou kunnen verwachten: het gemiddelde van de tarieven in plaats van de inkomsten over de laatste N op te tellen en de bezoekers over de laatste N op te tellen en ze vervolgens te verdelen. In plaats daarvan, gebruik

```
cumul(revenue)/cumul(visitor)
```

## Gelijk

Keert punten terug die precies voor een numerieke of koordwaarde aanpassen.

## Exponentiële regressie_ correlatiecoëfficiënt (tabel)

Geeft de correlatiecoëfficiënt terug; *r*, tussen twee metrieke kolommen ( *Metrisch_A* en *Metrisch_B*) voor de regressievergelijking .

```
CORREL.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Een metrisch die u met zou willen correleren *metrisch_Y*. |
| *metrisch_Y* | Een metrisch die u met zou willen correleren *Metrisch_X*. |

## Exponentiële regressie: Intercept (tabel)

Geeft de onderschepping terug, *b*, tussen twee metrieke kolommen ( *Metrisch_X* en *metrisch_Y*) voor

```
INTERCEPT.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Exponentiële regressie: helling (tabel)

Geeft de helling terug, *a*, tussen twee metrieke kolommen ( *Metrisch_X* en *metrisch_Y*) voor .

```
SLOPE.EXP(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Vloer (rij)

Keert het grootste geheel niet groter dan een bepaalde waarde terug. Bijvoorbeeld, als u wilt vermijden rapporterend munt decimals voor opbrengst en een product $569.34 heeft, gebruik de formule FLOOR ( *Ontvangsten*) om de omzet naar de dichtstbijzijnde dollar terug te brengen, of $569.

```
FLOOR(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Metrisch u wilt rond maken. |

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
| *metrisch* | De hoek in radianten waarvoor je de hyperbolische cosinus wilt vinden. |

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
| *metrisch* | De hoek in radialen waarvoor je de hyperbolische tangens wilt vinden. |

## IF (rij)

De IF-functie retourneert één waarde als een voorwaarde die u opgeeft evalueert naar TRUE en een andere waarde als die voorwaarde evalueert naar FALSE.

```
IF(logical_test, [value_if_true], [value_if_false])
```

| Argument | Beschrijving |
|---|---|
| *logical_test* | Vereist. Om het even welke waarde of uitdrukking die aan WAAR of VALS kunnen worden geëvalueerd. |
| *[waarde_if_true]* | De waarde die u wilt teruggeven als de *logical_test* argument evalueert tot TRUE. (Dit argument blijft aan 0 in gebreke als inbegrepen niet.) |
| *[waarde_if_false]* | De waarde die u wilt teruggeven als de *logical_test* argument evalueert tot FALSE. (Dit argument blijft aan 0 in gebreke als inbegrepen niet.) |

## Minder dan

Keert punten terug de waarvan numerieke telling minder dan de ingegane waarde is.

## Minder dan of gelijk aan

Keert punten terug de waarvan numerieke telling minder dan of gelijk aan de ingegane waarde is.

## Lineaire regressie_ correlatiecoëfficiënt

Y = een X + b. Geeft de correlatiecoëfficiënt terug

## Lineaire regressie_ Intercept

Y = een X + b. Retourzendingen b.

## Lineaire regressie_ Voorspeld Y

Y = een X + b. Geeft Y terug.

## Lineaire regressie_ Slope

Y = een X + b. Geeft a terug.

## Logbasis 10 (rij)

Keert basis-10 logaritme van een aantal terug.

```
LOG10(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Het positieve echte aantal waarvoor u de basis-10 logaritme wilt. |

## Logregressie: Correlatiecoëfficiënt (tabel)

Geeft de correlatiecoëfficiënt terug; *r*, tussen twee metrieke kolommen (*Metrisch_X* en *metrisch_Y*) voor de regressievergelijking [!DNL Y = a ln(X) + b]. Het wordt berekend met behulp van de CORREL vergelijking.

```
CORREL.LOG(metric_X,metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Een metrisch die u met zou willen correleren *metrisch_Y*. |
| *metrisch_Y* | Een metrisch die u met zou willen correleren *Metrisch_X*. |

## Logregressie: Intercept (tabel)

Geeft de intercept terug *b* als kleinste kwadratenregressie tussen twee metrische kolommen (*Metrisch_X* en *metrisch_Y*) voor de regressievergelijking [!DNL Y = a ln(X) + b]. Het wordt berekend gebruikend de vergelijking INTERCEPT.

```
INTERCEPT.LOG(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Logboekregressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden (metric_Y), gegeven de bekende [!DNL x] waarden (metric_X) die de &quot;minste kwadraten&quot;methode gebruiken om de lijn van best geschikt te berekenen gebaseerd op [!DNL Y = a ln(X) + b]. Het wordt berekend met behulp van de ESTIMATE vergelijking.

Bij regressieanalyse berekent deze functie de voorspelde [!DNL y] waarden (*metrisch_Y*), gezien de bekende [!DNL x] waarden (*Metrisch_X*) met behulp van de logaritme voor de berekening van de lijn die het best geschikt is voor de regressievergelijking [!DNL Y = a ln(X) + b]. De [!DNL a] de waarden komen overeen met elke x-waarde, en [!DNL b] is een constante waarde.

```
ESTIMATE.LOG(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Logregressie: helling (tabel)

Geeft de helling terug, *a*, tussen twee metrieke kolommen (*Metrisch_X* en *metrisch_Y*) voor de regressievergelijking [!DNL Y = a ln(X) + b]. Het wordt berekend gebruikend de vergelijking van de SLOPE.

```
SLOPE.LOG(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_A* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_B* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Natuurlijk logboek

Keert de natuurlijke logaritme van een aantal terug. Natuurlijke logaritmen zijn gebaseerd op de constante *e* (2 71828182845904). LN is het omgekeerde van de functie EXP.

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
| *logisch* | Vereist. Een waarde of een uitdrukking die aan WAAR of VALS kunnen worden geëvalueerd. |

Het gebruiken van NIET vereist het weten of de uitdrukkingen (&lt;, >, =, &lt;>, enz.) keer 0 of 1 waarden terug.

## Niet gelijk

Keert alle punten terug die niet de nauwkeurige gelijke van de ingegane waarde bevatten.

## Of (rij)

Geeft TRUE terug als een argument WAAR is, of geeft FALSE terug als alle argumenten FALSE zijn.

>[!NOTE]
>
>0 (nul) betekent Vals, en een andere waarde is Waar.

```
OR(logical_test1,[logical_test2],...)
```

| Argument | Beschrijving |
|---|---|
| *logical_test1* | Vereist. Om het even welke waarde of uitdrukking die aan WAAR of VALS kunnen worden geëvalueerd. |
| *logical_test2* | Optioneel. Extra condities die je wilt evalueren als TRUE of FALSE |

## Pi

Geeft constante PI, 3.14159265358979, nauwkeurig aan 15 cijfers.

```
PI()
```

De [!DNL PI]functie heeft geen argumenten.

## Stroomregressie: Correlatiecoëfficiënt (tabel)

Geeft de correlatiecoëfficiënt terug; *r*, tussen twee metrieke kolommen (*Metrisch_X* en *metrisch_Y*) voor [!DNL Y = b*X].

```
CORREL.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Een metrisch die u met zou willen correleren *metrisch_Y*. |
| *metrisch_Y* | Een metrisch die u met zou willen correleren *Metrisch_X*. |

## Stroomregressie: Intercept (tabel)

Geeft de onderschepping terug, *b*, tussen twee metrieke kolommen (*Metrisch_X* en *metrisch_Y*) voor [!DNL Y = b*X].

```
 INTERCEPT.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Stroomregressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden ( [!DNL metric_Y]), gezien de bekende [!DNL x] waarden ( [!DNL metric_X]) met behulp van de &quot;kleinste kwadraten&quot;-methode voor de berekening van de lijn die het best geschikt is voor [!DNL Y = b*X].

```
 ESTIMATE.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Stroomregressie: helling (tabel)

Geeft de helling terug, *a*, tussen twee metrieke kolommen (*Metrisch_X* en *metrisch_Y*) voor [!DNL Y = b*X].

```
SLOPE.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Quadratische regressie: Correlatiecoëfficiënt (tabel)

Geeft de correlatiecoëfficiënt terug; *r*, tussen twee metrieke kolommen (*Metrisch_X* en *metrisch_Y*) voor [!DNL Y=(a*X+b)]****.

```
CORREL.QUADRATIC(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Een metrisch die u met zou willen correleren *metrisch_Y*. |
| *metrisch_Y* | Een metrisch die u met zou willen correleren *Metrisch_X*. |

## Quadratische regressie: Intercept (tabel)

Geeft de onderschepping terug, *b*, tussen twee metrieke kolommen (*Metrisch_X* en *metrisch_Y*) voor [!DNL Y=(a*X+b)]****.

```
INTERCEPT.POWER(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Quadratische regressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden (metric_Y), gegeven de bekende [!DNL x] waarden (metric_X) die de minste kwadratenmethode gebruiken om de lijn het best te berekenen past gebruikend [!DNL Y=(a*X+b)]**** .

```
ESTIMATE.QUADRATIC(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_A* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *Metrisch_B* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |

## Quadratische regressie: helling (tabel)

Geeft de helling terug, *a*, tussen twee metrieke kolommen (*Metrisch_X* en (1) voor [!DNL Y=(a*X+b)]****.

```
SLOPE.QUADRATIC(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: Correlatiecoëfficiënt (tabel)

Geeft de correlatiecoëfficiënt terug; *r*, tussen twee metrieke kolommen (*metrisch_X)* en *metrisch_Y*) voor [!DNL Y = a/X+b].

```
CORREL.RECIPROCAL(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Een metrisch die u met zou willen correleren *metrisch_Y*. |
| *metrisch_Y* | Een metrisch die u met zou willen correleren *Metrisch_X*. |

## Wederkerige regressie: Intercept (tabel)

Geeft de onderschepping terug, *b*, tussen twee metrieke kolommen (*Metrisch_X* en *metrisch_Y*) voor [!DNL Y = a/X+b].

```
INTERCEPT.RECIPROCAL(metric_A, metric_B)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: Voorspeld Y (rij)

Berekent de voorspelde [!DNL y] waarden (metric_Y), gegeven de bekende [!DNL x] waarden (metric_X) die de minste kwadratenmethode gebruiken om de lijn het best te berekenen past gebruikend [!DNL Y = a/X+b].

```
ESTIMATE.RECIPROCAL(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Wederkerige regressie: helling (tabel)

Geeft de helling terug, *a*, tussen twee metrieke kolommen (*Metrisch_X* en *metrisch_Y*) voor [!DNL Y = a/X+b].

```
SLOPE.RECIPROCAL(metric_X, metric_Y)
```

| Argument | Beschrijving |
|---|---|
| *Metrisch_X* | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| *metrisch_Y* | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |

## Zine (rij)

Keert de sinus van de bepaalde hoek terug. Als de hoek in graden is, vermenigvuldig de hoek met PI( )/180.

```
SIN(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De hoek in radialen waarvoor je de sinus wilt. |

## T-score

Alias voor Z-score, namelijk de afwijking van het gemiddelde gedeeld door de standaardafwijking

## T-test

Voert een m-tailed t-test uit met t-score van col en n vrijheidsgraden.

De handtekening is `t_test( x, n, m )`. Onder, roept het eenvoudig `m*cdf_t(-abs(x),n)`. (Dit is vergelijkbaar met de z-testfunctie die wordt uitgevoerd `m*cdf_z(-abs(x))`.

Hier, `m` het aantal staarten is, en `n` de mate van vrijheid. Dit moeten cijfers zijn (constant voor het gehele rapport, d.w.z. niet veranderend op rij door rijbasis).

`X` is de t-teststatistiek en zou vaak een formule (bv. zscore) zijn die op een metrische basis is gebaseerd en op elke rij zal worden beoordeeld.

De terugkeerwaarde is de waarschijnlijkheid dat de teststatistiek x gezien de vrijheidsgraad en het aantal staarten wordt gezien.

**Voorbeelden:**

1. Gebruik het om uitschieters te vinden:

   ```
   t_test( zscore(bouncerate), row-count-1, 2)
   ```

1. Combineer het met `if` om zeer hoge of lage sprongpercentages te negeren, en bezoeken te tellen op al het andere:

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
| *metrisch* | De hoek in radialen waarvoor je de tangens wilt. |

## Z-score (rij)

Keert de Z-score, of de normale score terug, die op een normale distributie wordt gebaseerd. De Z-score is het aantal standaardafwijkingen dat een waarneming uit het gemiddelde volgt. Een Z-score van 0 (nul) betekent dat de score gelijk is aan het gemiddelde. Een Z-score kan positief of negatief zijn, erop wijzend of het boven of onder het gemiddelde is en door hoeveel standaardafwijkingen.

De vergelijking voor Z-score is:

![](assets/z_score.png)

waar [!DNL x] de ruwe score is, [!DNL μ] het gemiddelde van de bevolking is, en [!DNL σ] de standaardafwijking van de populatie.

>[!NOTE]
>
>[!DNL μ] mu) en[!DNL σ] (sigma) worden automatisch berekend uit metrisch.

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

Voert een n-tailed Z-test met Z-score van A uit.

Keert de waarschijnlijkheid terug dat de huidige rij toevallig in de kolom kon worden gezien.

>[!NOTE]
>
>Veronderstelt dat de waarden normaal verdeeld zijn.

