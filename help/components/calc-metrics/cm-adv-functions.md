---
title: Referentie - geavanceerde functies
description: U hebt toegang tot deze functies door Geavanceerd tonen in de vervolgkeuzelijst Functies te selecteren.
feature: Calculated Metrics
exl-id: 3689a499-817d-4a59-8a1f-5f7bda297268
role: User
source-git-commit: ecf8156df0b31e81f1a5546829c6100831b2a600
workflow-type: tm+mt
source-wordcount: '2832'
ht-degree: 2%

---

# Referentie - geavanceerde functies

Heb toegang tot deze functies door **[!UICONTROL Show all]** te selecteren onder ![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL Functions]** lijst in het paneel van Componenten. Schuif omlaag om de lijst met Geavanceerde functies weer te geven.

## Tabelfuncties versus rijfuncties

Een tabelfunctie is een functie waarbij de uitvoer voor elke rij van de tabel hetzelfde is. Een rijfunctie is een functie waarbij de uitvoer voor elke rij van de tabel anders is. Indien van toepassing en relevant, wordt een functie geannoteerd met het type functie.

## Wat betekent de parameter include-zeros?

Het vertelt of nullen in de berekening moeten worden opgenomen. Soms betekent nul *niets*, maar soms is het belangrijk.

Bijvoorbeeld, als u metrisch van de Opbrengst hebt, en dan metrische vertoningen van de Pagina aan het rapport toevoegt, zijn er plotseling meer rijen voor uw opbrengst, die allen nul zijn. U wilt waarschijnlijk niet dat extra metrisch om het even welk [ MEAN ](cm-functions.md#mean), [ MIN ](cm-functions.md#row-min), [ KWALITEIT ](cm-functions.md#quartile), en meer berekeningen te beïnvloeden die u in de opbrengstkolom hebt. In dit geval controleert u de parameter `include-zeros` .

Een alternatief scenario is dat u twee metriek van rente hebt en één een hoger gemiddelde of een minimum heeft omdat sommige rijen nul zijn.  In dat geval kunt u ervoor kiezen om de parameter niet te controleren en nullen op te nemen.


## en

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL AND(logical_test)]**


Conjunctie. Niet gelijk aan nul wordt beschouwd als waar en gelijk aan nul wordt beschouwd als onwaar. De uitvoer is 0 (false) of 1 (true).


| Argument | Beschrijving |
|---|---|
| logical_test | Vereist minstens één parameter, maar kan om het even welk aantal parameters nemen. Elke waarde of expressie die kan worden geëvalueerd op TRUE of FALSE |

## Telling bij benadering onderscheiden

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL APPROXIMATE COUNT DISTINCT(dimension)]**


Retourneert de geschatte, verschillende telling van dimensie-items voor de geselecteerde dimensie.


| Argument | Beschrijving |
|---|---|
| dimensie | De afmeting waarvoor u de benaderende verschillende punttelling wilt berekenen |

### Voorbeeld

Een veel voorkomend geval voor deze functie is wanneer u een benaderend aantal klanten wilt krijgen.




## Arc Cosine

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL ARC COSINE(metric)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch | De cosinus van de hoek die u wilt instellen van -1 tot 1 |



## Boog sinus

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL ARC SINE(metric)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch | De sinus van de hoek die u wilt instellen van -1 tot 1 |



## Booghoek

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL ARC TANGENT(metric)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch | De tangens van de hoek u van -1 tot 1 wilt |



## Cdf-T

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL CDF-T(metric, number)]**


Keert de waarschijnlijkheid terug dat een willekeurige variabele met student-t distributie met n graden van vrijheid een z-score minder dan kolom heeft.


| Argument | Beschrijving |
|---|---|
| metrisch | Metrisch waarvoor u de Cumulatieve Functie van de Distributie van de student t-distribution zou willen |
| getal | De vrijheidsgraden voor de cumulatieve distributiefunctie van de t-distribution van de student |

### Voorbeeld

```
CDF-T(-∞, n) = 0
CDF-T(∞, n) = 1
CDF-T(3, 5) ? 0.99865
CDF-T(-2, 7) ? 0.0227501
CDF-T(x, ∞) ? cdf_z(x)
```


## Cdf-Z

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL CDF-Z(metric, number)]**


Retourneert de waarschijnlijkheid dat een willekeurige variabele met een normale distributie een z-score heeft minder dan col.


| Argument | Beschrijving |
|---|---|
| metrisch | De metrische waarde waarvoor u de cumulatieve distributiefunctie van de Standaard Normale Distributie zou willen |

### Voorbeelden

```
CDF-Z(-∞) = 0
CDF-Z(∞) = 1
CDF-Z(0) = 0.5
CDF-Z(2) ? 0.97725
CDF-Z(-3) ? 0.0013499
```

## Plafond

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL CEILING(metric)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch | De metrische waarde die u wilt afronden |


## Vertrouwen (onder)

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL CONFIDENCE(normalizing-container, success-metric, control, significance-treshold)]**

Bereken het om het even welke tijd-geldige vertrouwen **lager** gebruikend de methode WASKR zoals die in [ wordt beschreven tijd-eenvormige centrale beperkingstheorie en asymptotische vertrouwensopeenvolgingen ](http://arxiv.org/pdf/2103.06476).

Vertrouwen is een waarschijnlijkheidsmeting van hoeveel bewijs er is dat een bepaalde variant dezelfde is als de besturingsvariant. Een hoger vertrouwen geeft minder bewijs voor de aanname dat de besturingsvariant en de niet-besturingsvariant dezelfde prestaties leveren.

| Argument | Beschrijving |
| --- | --- |
| normalizing-container | De basis (Mensen, Zittingen, of Gebeurtenissen) waarop een test in werking wordt gesteld. |
| succesmetrisch | De metrische of metrische waarde waarmee een gebruiker varianten vergelijkt. |
| besturen | De variant waarmee alle andere varianten in het experiment worden vergeleken. Voer de naam in van het element Dimensie besturingsvariant. |
| significantiedrempel | De drempel in deze functie is ingesteld op een standaardwaarde van 95%. |

## Vertrouwen (boven)

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL CONFIDENCE(normalizing-container, success-metric, control, significance-treshold)]**

Bereken het om het even welk-tijd-geldige vertrouwen **hoger** gebruikend de methode WASKR zoals die in [ wordt beschreven tijd-eenvormige centrale beperkingstheorie en asymptotische vertrouwensopeenvolgingen ](http://arxiv.org/pdf/2103.06476).

Vertrouwen is een waarschijnlijkheidsmeting van hoeveel bewijs er is dat een bepaalde variant dezelfde is als de besturingsvariant. Een hoger vertrouwen geeft minder bewijs voor de aanname dat de besturingsvariant en de niet-besturingsvariant dezelfde prestaties leveren.

| Argument | Beschrijving |
| --- | --- |
| normalizing-container | De basis (Mensen, Zittingen, of Gebeurtenissen) waarop een test in werking wordt gesteld. |
| succesmetrisch | De metrische of metrische waarde waarmee een gebruiker varianten vergelijkt. |
| besturen | De variant waarmee alle andere varianten in het experiment worden vergeleken. Voer de naam in van het element Dimensie besturingsvariant. |
| significantiedrempel | De drempel in deze functie is ingesteld op een standaardwaarde van 95%. |


## Cosine

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL COSINE(metric)]**

[!BADGE  Rij ]{type="Neutral"}

| Argument | Beschrijving |
|---|---|
| metrisch | De hoek in radialen waarvoor u de cosinus wilt gebruiken |


## Kubus Root

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL CUBE ROOT(metric)]**


Retourneert de positieve kubuswortel van een getal. De kubuswortel van een aantal is de waarde van dat aantal dat tot de macht van 1/3 wordt opgeheven.


| Argument | Beschrijving |
|---|---|
| metrisch | Metrisch waarvoor u de kubuswortel wilt berekenen |



## Cumulatief

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL CUMULATIVE(number, metric)]**

Retourneert de som van de laatste n-elementen van kolom x. Indien n > 0, som de laatste n elementen of x. Indien n &lt; 0, som de voorafgaande elementen.

| Argument | Beschrijving |
| --- | --- |
| getal | The last N number of rows to return the sum for. Als N &lt;= 0 is, gebruikt u alle vorige rijen. |
| metrisch | Metrisch waarvoor u de Cumulatieve Som zou willen. |

### Voorbeelden

| Datum | Ontvangsten | CUMULATIEF(0, inkomsten) | CUMULATIEF(2, inkomsten) |
|------|------:|--------------:|--------------:|
| mei | $ 500 | $ 500 | $ 500 |
| juni | $ 200 | $ 700 | $ 700 |
| juli | $ 400 | $ 1.100 | $ 600 |


## Cumulatief (gemiddeld)

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL CUMULATIVE AVERAGE(number, metric)]**

Retourneert het gemiddelde van de laatste n elementen van kolom x. Indien n > 0, som de laatste n elementen of x. Indien n &lt; 0, som de voorafgaande elementen.

| Argument | Beschrijving |
| --- | --- |
| getal | Het laatste N aantal rijen om het gemiddelde voor terug te keren. Als N &lt;= 0 is, gebruikt u alle vorige rijen. |
| metrisch | Metrisch waarvoor u het Cumulatieve Gemiddelde zou willen. |

>[!NOTE]
>
>Deze functie werkt niet met tariefmaatstaven zoals opbrengst per persoon. De functie gebruikt het gemiddelde van de tarieven in plaats van de inkomsten over de laatste N op te tellen en personen over de laatste N op te tellen en hen vervolgens te verdelen. <br/> in plaats daarvan, gebruik [**[!UICONTROL CUMULATIVE(revenue)]**](#cumulative) ![ verdeel ](/help/assets/icons/Divide.svg) [**[!UICONTROL CUMULATIVE(person)]**](#cumulative).
>


## Gelijk

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL EQUAL()]**


Gelijk. De uitvoer is 0 (false) of 1 (true).


| Argument | Beschrijving |
|---|---|
| metrisch_X | |
| metrisch_Y | |

### Voorbeeld

`Metric 1 = Metric 2`



## Exponentiële regressie: Correlatiecoëfficiënt

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL EXPONENTIAL REGRESSION: CORRELATION COEFFICIENT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u met metrisch_Y zou willen correleren |
| metrisch_Y | Metrisch die u met metrisch_X zou willen correleren |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |

## Exponentiële regressie: voorspeld Y

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL EXPONENTIAL REGRESSION: PREDICTED Y(metric_X, metric_Y, include_zeros)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen. |
| metrisch_Y | Metrisch die u als afhankelijke gegevens zou willen aanwijzen. |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |


## Exponentiële regressie: Intercept

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL EXPONENTIAL REGRESSION: INTERCEPT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}

| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |


## Exponentiële regressie: helling

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL EXPONENTIAL REGRESSION: SLOPE(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |


## Floor

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL FLOOR(metric_X, metric_Y, include_zeros)]**

[!BADGE  Rij ]{type="Neutral"}

| Argument | Beschrijving |
|---|---|
| metrisch | De metrische waarde die u wilt afronden. |


## Groter dan

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL GREATER THAN()]**


De uitvoer is 0 (false) of 1 (true).


| Argument | Beschrijving |
|---|---|
| metrisch_X | |
| metrisch_Y | |

### Voorbeeld

`Metric 1 > Metric 2`

## Groter dan of gelijk aan

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL GREATER THAN OR EQUAL()]**


Groter dan of gelijk aan. De uitvoer is 0 (false) of 1 (true).


| Argument | Beschrijving |
|---|---|
| metrisch_X |  |
| metrisch_Y |  |

### Voorbeeld

`Metric 1 >= Metric 2`



## Hyperbolische cosinus

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL HYPERBOLIC COSINE(metric)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch | De hoek in radialen waarvoor u de hyperbolische cosinus wilt vinden |



## Hyperbolische sinus

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL HYPERBOLIC SINE(metric)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch | De hoek in radialen waarvoor u de hyperbolische sinus wilt vinden |



## Hyperbolische hoek

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL HYPERBOLIC TANGENT(metric)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch | De hoek in radialen waarvoor u de hyperbolische tangens wilt vinden |


## Indien

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL IF(logical_test, value_if_true, value_if_false)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| logical_test | Vereist. Elke waarde of expressie die kan worden geëvalueerd op TRUE of FALSE |
| value_if_true | De waarde die u wilt zijn teruggekeerd als het logical_test argument aan WAAR evalueert. (Dit argument wordt standaard ingesteld op 0 als het niet wordt opgenomen.) |
| value_if_false | De waarde die u wilt worden geretourneerd als het argument logical_test naar FALSE evalueert. (Dit argument wordt standaard ingesteld op 0 als het niet wordt opgenomen.) |


## Minder dan

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL LESS THAN()]**


De uitvoer is 0 (false) of 1 (true).


| Argument | Beschrijving |
|---|---|
| metrisch_X | |
| metrisch_Y | |


### Voorbeeld

`Metric 1 < Metric 2`

## Kleiner dan of gelijk aan

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL LESS THAN OR EQUAL()]**

Kleiner dan of gelijk aan. De uitvoer is 0 (false) of 1 (true).


| Argument | Beschrijving |
|---|---|
| metrisch_X | |
| metrisch_Y | |

### Voorbeeld

`Metric 1 <= Metric 2`



## Lineaire regressie: Correlatiecoëfficiënt

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL LINEAR REGRESSION: CORRELATION COEFFICIENT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u met metrisch_Y zou willen correleren |
| metrisch_Y | Metrisch die u met metrisch_X zou willen correleren |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |



## Lineaire regressie: Intercept

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL LINEAR REGRESSION: INTERCEPT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |



## Lineaire regressie: voorspeld Y

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL LINEAR REGRESSION: PREDICTED Y(metric_X, metric_Y, include_zeros)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |



## Lineaire regressie: helling

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL LINEAR REGRESSION: SLOPE(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |


## Logbestand basis 10

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL LOG BASE 10(metric)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch | Het positieve reële getal waarvoor u de natuurlijke logaritme met grondtal 10 wilt gebruiken |


## Logregressie: Correlatiecoëfficiënt

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL LOG REGRESSION: CORRELATION COEFFICIENT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u met metrisch_Y zou willen correleren |
| metrisch_Y | Metrisch die u met metrisch_X zou willen correleren |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |


## Logregressie: Onderscheppen

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL LOG REGRESSION: INTERCEPT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |



## Logregressie: voorspeld Y

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL LOG REGRESSION: PREDICTED Y(metric_X, metric_Y, include_zeros)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |



## Logregressie: helling

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL LOG REGRESSION: SLOPE(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |



## Natuurlijk logboek

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL NATURAL LOG(metric)]**


Retourneert de natuurlijke logaritme van een getal. Natuurlijk logaritme is gebaseerd op de constante e (2.71828182845904). LN is het omgekeerde van de functie EXP.


| Argument | Beschrijving |
|---|---|
| metrisch | Het positieve reële getal waarvoor u de natuurlijke logaritme wilt |



## Niet

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL NOT(logical)]**


Negatie als een booleaanse waarde. De uitvoer is 0 (false) of 1 (true).


| Argument | Beschrijving |
|---|---|
| logisch | Vereist. Een waarde of expressie die kan worden geëvalueerd op TRUE of FALSE |



## Niet gelijk

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL NOT EQUAL()]**


Niet gelijk. De uitvoer is 0 (false) of 1 (true).


| Argument | Beschrijving |
|---|---|
| metrisch_X | |
| metrisch_Y | |

### Voorbeeld

`Metric 1 != Metric 2`


## of

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL OR(logical_test)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| logical_test | Vereist minstens één parameter maar kan om het even welk aantal parameters nemen. Elke waarde of expressie die kan worden geëvalueerd op TRUE of FALSE |


>[!NOTE]
>
>0 (nul) betekent Onwaar en elke andere waarde is Waar.


## Pi

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL PI()]**

Retourneert Pi: 3,14159...


## Stroomregressie: Correlatiecoëfficiënt

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL POWER REGRESSION: CORRELATION COEFFICIENT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u met metrisch_Y zou willen correleren |
| metrisch_Y | Metrisch die u met metrisch_X zou willen correleren |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |



## Stroomregressie: Intercept

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL POWER REGRESSION: INTERCEPT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |


## Stroomregressie: voorspeld Y

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL POWER REGRESSION: PREDICTED Y(metric_X, metric_Y, include_zeros)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |



## Stroomregressie: helling

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL POWER REGRESSION: SLOPE(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |



## Kwartaalregressie: Correlatiecoëfficiënt

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL QUADRATIC REGRESSION: CORRELATION COEFFICIENT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u met metrisch_Y zou willen correleren |
| metrisch_Y | Metrisch die u met metrisch_X zou willen correleren |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |

## Quadratische regressie: Intercept

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL QUADRATIC REGRESSION: INTERCEPT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |


## Quadratische regressie: voorspeld Y

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL QUADRATIC REGRESSION: PREDICTED Y(metric_X, metric_Y, include_zeros)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |

## Kwadratische regressie: helling

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL QUADRATIC REGRESSION: SLOPE(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |



## Wederkerige regressie: Correlatiecoëfficiënt

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL RECIPROCAL REGRESSION: CORRELATION COEFFICIENT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u met metrisch_Y zou willen correleren |
| metrisch_Y | Metrisch die u met metrisch_X zou willen correleren |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |


## Wederkerige regressie: Intercept

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL RECIPROCAL REGRESSION: INTERCEPT(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |


## Wederkerige regressie: voorspeld Y

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL RECIPROCAL REGRESSION: PREDICTED Y(metric_X, metric_Y, include_zeros)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |


## Wederkerige regressie: helling

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL RECIPROCAL REGRESSION: SLOPE(metric_X, metric_Y, include_zeros)]**


[!BADGE  Lijst ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch_X | Metrisch die u als afhankelijke gegevens zou willen aanwijzen |
| metrisch_Y | Metrisch die u als onafhankelijke gegevens zou willen aanwijzen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |




## Sinus

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL SINE(metric)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch | De hoek in radialen waarvoor u de sinus wilt gebruiken |




## T-score

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL T-SCORE(metric, include_zeros)]**


De afwijking van [ MEAN ](cm-functions.md#mean), die door de standaardafwijking wordt verdeeld. Alias voor [ z-Score ](#z-score).


| Argument | Beschrijving |
|---|---|
| metrisch | Metrisch waarvoor u de Score van T zou willen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |


## T-test

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL T-TEST(metric, degrees, tails)]**


Voert een t-test met mtailed t-score van x en n graden van vrijheid uit.


| Argument | Beschrijving |
|---|---|
| metrisch | Metrisch waarop u een Test van T zou willen uitvoeren |
| graden | Vrijheidsgraden |
| staarten | De lengte van de staart die moet worden gebruikt voor de T-test |

### Details

De handtekening is T-TEST (metrisch, graden, staarten). Onder, roept het eenvoudig ***m*** ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) **[[!DNL CDF-T(-ABSOLUTE VALUE(tails), degrees)]](#cdf-t)**. Deze functie is gelijkaardig aan **[z-TEST](#z-test)** functie, die ***m*** ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg) **[[!DNL CDF-Z(-ABSOLUTE VALUE(tails))]](#cdf-z)** in werking stelt.

- ***m*** is het aantal staarten.
- ***n*** is de graden van vrijheid, en zou een constant aantal voor het volledige rapport moeten zijn, namelijk niet veranderend op een rij door rijbasis.
- ***x*** is de t-test statistiek, en zou vaak een formule (bijvoorbeeld, **[z-SCORE](#z-score)**) zijn die op metrisch wordt gebaseerd en op elke rij wordt geëvalueerd.

De geretourneerde waarde is de waarschijnlijkheid dat de teststatistiek x gezien de vrijheidsgraad en het aantal staarten wordt weergegeven.

**Voorbeelden:**

1. Gebruik het om uitschieters te vinden:

   ```
   T-TEST(Z-SCORE(bouncerate), ROW COUNT - 1, 2)
   ```

1. Combineer het met **[ALS](#if)** om zeer hoge of lage stuittarieven te negeren, en zittingen op alles anders te tellen:

   ```
   IF(T-TEST(Z-SCORE(bouncerate), ROW COUNT - 1, 2) < 0.01, 0, sessions )
   ```




## Raaklijn

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL TANGENT(metric)]**


Retourneert de tangens van de opgegeven hoek. Als de hoek in graden is, vermenigvuldig de hoek met PI()/180.


| Argument | Beschrijving |
|---|---|
| metrisch | De hoek in radialen waarvoor u de tangens wilt |



## Z-score

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL Z-SCORE(metric, include_zeros)]**


[!BADGE  Rij ]{type="Neutral"}


| Argument | Beschrijving |
|---|---|
| metrisch | De metrisch waarvoor u de Score van Z zou willen |
| include_zeros | Of nul-waarden in de berekeningen moeten worden opgenomen |

Een Z-score van 0 (nul) impliceert dat de score gelijk is aan het gemiddelde. Een Z-score kan positief of negatief zijn en geeft aan of deze boven of onder het gemiddelde ligt en hoeveel standaardafwijkingen er zijn.

De vergelijking voor Z-score is:

![](assets/z_score.png)

Waar ***[!DNL x]*** de onbewerkte score is, is ***[!DNL μ]*** het gemiddelde van de populatie en is ***[!DNL σ]*** de standaardafwijking van de populatie.

>[!NOTE]
>
>***[!DNL μ]*** (mu) en ***[!DNL σ]*** (sigma) worden automatisch berekend op basis van de metrische waarde.



## Z-test

![ Effect ](/help/assets/icons/Effect.svg) **[!UICONTROL Z-TEST(metric_tails)]**


Voert een n-tailed z-test met een z-score van x uit.


| Argument | Beschrijving |
|---|---|
| metrisch | Metrisch waarop u een Test van Z zou willen uitvoeren |
| staarten | De lengte van de staart die moet worden gebruikt voor de Z-test |

>[!NOTE]
>
>gaat ervan uit dat de waarden normaal worden verdeeld.









<!--



## AND

Returns the value of its argument. Use NOT to make sure that a value is not equal to one particular value.

>[!NOTE]
>
>0 (zero) means False, and any other value is True.

```
AND(logical_test1,[logical_test2],...)
```

|  Argument  | Description  |
|---|---|
|  *logical_test1* | Required. Any value or expression that can be evaluated to TRUE or FALSE.  |
|  *logical_test2* | Optional. Additional conditions that you want to evaluate as TRUE or FALSE  |

## Approximate Count Distinct (dimension)

Returns the approximated distinct count of dimension items for the selected dimension. The function uses the HyperLogLog (HLL) method of approximating distinct counts.&nbsp; It is configured to guarantee the value is within 5% of the actual value 95% of the time.

```
Approximate Count Distinct (dimension)
```

|  Argument  |  |
|---|---|
|  *dimension* | The dimension for which you want the approximate distinct item count.  |

### Example Use Case

Approximate Count Distinct (customer ID eVar) is a common use case for this function.

Definition for a new 'Approximate Customers' calculated metric:

![Approximate county distinct new dimension definition showing Customer ID (eVar1)](assets/approx-count-distinct.png)

This is how the "Approximate Customers" metric could be used in reporting:

![Freeform Table showing Unique Visitors and Approximate Customers ](assets/approx-customers.png)

### Comparing Count Functions

Approximate Count Distinct() is an improvement over Count() and RowCount() functions because the metric created can be used in any dimensional report to render an approximated count of items for a separate dimension. For example, a count of customer IDs used in a Mobile Device Type report.

This function will be marginally less accurate than Count() and RowCount() because it uses the HLL method, whereas Count() and RowCount() are exact counts.

## Arc Cosine (Row)

Returns the arccosine, or inverse of the cosine, of a metric. The arccosine is the angle whose cosine is number. The returned angle is given in radians in the range 0 (zero) to pi. If you want to convert the result from radians to degrees, multiply it by 180/PI( ).

```
ACOS(metric)
```

|  Argument  |  |
|---|---|
|  *metric* | The cosine of the angle you want from -1 to 1. |

## Arc Sine (Row)

Returns the arcsine, or inverse sine, of a number. The arcsine is the angle whose sine is number. The returned angle is given in radians in the range -pi/2 to pi/2. To express the arcsine in degrees, multiply the result by 180/PI( ).

```
ASIN(metric)
```

|  Argument  |  |
|---|---|
|  *metric* | The cosine of the angle you want from -1 to 1. |

## Arc Tangent (Row)

Returns the arctangent, or inverse tangent, of a number. The arctangent is the angle whose tangent is number. The returned angle is given in radians in the range -pi/2 to pi/2. To express the arctangent in degrees, multiply the result by 180/PI( ).

```
ATAN(metric)
```

|  Argument  |  |
|---|---|
|  *metric* | The cosine of the angle you want from -1 to 1. |

## Exponential Regression: Predicted Y (Row)

Calculates the predicted y-values (metric_Y), given the known x-values (metric_X) using the "least squares" method for calculating the line of best fit based on .

```
ESTIMATE.EXP(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Cdf-T

Returns the percentage of values in a student's t-distribution with n degrees of freedom that have a z-score less than x.

```
cdf_t( -∞, n ) = 0
cdf_t(  ∞, n ) = 1
cdf_t( 3, 5 ) ? 0.99865
cdf_t( -2, 7 ) ? 0.0227501
cdf_t( x, ∞ ) ? cdf_z( x )
```

## Cdf-Z

Returns the percentage of values in a normal distribution that have a z-score less than x.

```
cdf_z( -∞ ) = 0
cdf_z( ∞ ) = 1
cdf_z( 0 ) = 0.5
cdf_z( 2 ) ? 0.97725
cdf_z( -3 ) ? 0.0013499

```

## Exponential Regression: Intercept (Table)

Returns the intercept, *b*, between two metric columns ( *metric_X* and *metric_Y*) for

```
INTERCEPT.EXP(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Exponential Regression: Slope (Table)

Returns the slope, *a*, between two metric columns ( *metric_X* and *metric_Y*) for .

```
SLOPE.EXP(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Floor (Row)

Returns the largest integer not greater than a given value. For example, if you want to avoid reporting currency decimals for revenue and a product has $569.34, use the formula FLOOR( *Revenue*) to round revenue down to the nearest dollar, or $569.

```
FLOOR(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The metric you want to round.  |

## Greater Than

Returns items whose numeric count is greater than the value entered.

## Greater Than or Equal

Returns items whose numeric count is greater than or equal to the value entered.

## Hyperbolic Cosine (Row)

Returns the hyperbolic cosine of a number.

```
COSH(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The angle in radians for which you want to find the hyperbolic cosine.  |

## Hyperbolic Sine (Row)

Returns the hyperbolic sine of a number.

```
SINH(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The angle in radians for which you want to find the hyperbolic sine.  |

## Hyperbolic Tangent (Row)

Returns the hyperbolic tangent of a number.

```
TANH(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The angle in radians for which you want to find the hyperbolic tanget.  |

## IF (Row)

The IF function returns one value if a condition you specify evaluates to TRUE, and another value if that condition evaluates to FALSE.

```
IF(logical_test, [value_if_true], [value_if_false])
```

|  Argument  | Description  |
|---|---|
|  *logical_test* | Required. Any value or expression that can be evaluated to TRUE or FALSE.  |
|  *[value_if_true]* | The value that you want to be returned if the *logical_test* argument evaluates to TRUE. (This argument defaults to 0 if not included.)  |
|  *[value_if_false]* | The value that you want to be returned if the *logical_test* argument evaluates to FALSE. (This argument defaults to 0 if not included.)  |

## Less Than

Returns items whose numeric count is less than the value entered.

## Less Than or Equal

Returns items whose numeric count is less than or equal to the value entered.

## Lift

Returns the Lift a particular variant had in conversions over a control variant. It is the difference in performance between a given variant and the baseline, divided by the performance of the baseline, expressed as a percentage. 

```
fx Lift (normalizing-container, success-metric, control)
```

| Argument | Description |
| --- | --- |
| Normalizing Container | The basis (People, Sessions, or Events) on which a test will be run. |
| Success Metric | The metric or metrics that a user is comparing variants with. |
| Control | The variant that all other variants in the experiment are being compared with. Enter the name of the control variant dimension item. |

{style="table-layout:auto"}

## Linear regression_ Correlation Coefficient

Y = a X + b. Returns the correlation coefficient

## Linear regression_ Intercept

Y = a X + b. Returns b.

## Linear regression_ Predicted Y

Y = a X + b. Returns Y.

## Linear regression_ Slope

Y = a X + b. Returns a.

## Log Base 10 (Row)

Returns the base-10 logarithm of a number.

```
LOG10(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The positive real number for which you want the base-10 logarithm.  |

## Log regression: Correlation coefficient (Table)

Returns the correlation coefficient, *r*, between two metric columns (*metric_X* and *metric_Y*) for the regression equation [!DNL Y = a ln(X) + b]. It is calculated using the CORREL equation.

```
CORREL.LOG(metric_X,metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to correlate with *metric_Y*.  |
|  *metric_Y* | A metric that you would like to correlate with *metric_X*.  |

## Log regression: Intercept (Table)

Returns the intercept *b* as the least squares regression between two metric columns (*metric_X* and *metric_Y*) for the regression equation [!DNL Y = a ln(X) + b]. It is calculated using the INTERCEPT equation.

```
INTERCEPT.LOG(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Log Regression: Predicted Y (Row)

Calculates the predicted [!DNL y] values (metric_Y), given the known [!DNL x] values (metric_X) using the "least squares" method for calculating the line of best fit based on [!DNL Y = a ln(X) + b]. It is calculated using the ESTIMATE equation.

In regression analysis, this function calculates the predicted [!DNL y] values (*metric_Y*), given the known [!DNL x] values (*metric_X*) using the logarithm for calculating the line of best fit for the regression equation [!DNL Y = a ln(X) + b]. The [!DNL a] values correspond to each x value, and [!DNL b] is a constant value.

```
ESTIMATE.LOG(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Log regression: Slope (Table)

Returns the slope, *a*, between two metric columns (*metric_X* and *metric_Y*) for the regression equation [!DNL Y = a ln(X) + b]. It is calculated using the SLOPE equation.

```
SLOPE.LOG(metric_A, metric_B)
```

|  Argument  | Description  |
|---|---|
|  *metric_A* | A metric that you would like to designate as the dependent data.  |
|  *metric_B* | A metric that you would like to designate as the independent data.  |

## Natural Log

Returns the natural logarithm of a number. Natural logarithms are based on the constant *e* (2.71828182845904). LN is the inverse of the EXP function.

```
LN(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The positive real number for which you want the natural logarithm.  |

## NOT

Returns 1 if the number is 0 or returns 0 if another number.

```
NOT(logical)
```

|  Argument  | Description  |
|---|---|
|  *logical* | Required. A value or expression that can be evaluated to TRUE or FALSE.  |

Using NOT requires knowing if the expressions (<, >, =, <> , etc.) return 0 or 1 values.

## Not equal

Returns all items that do not contain the exact match of the value entered.

## Or (Row)

Returns TRUE if any argument is TRUE, or returns FALSE if all arguments are FALSE.

>[!NOTE]
>
>0 (zero) means False, and any other value is True.

```
OR(logical_test1,[logical_test2],...)
```

|  Argument  | Description  |
|---|---|
|  *logical_test1* | Required. Any value or expression that can be evaluated to TRUE or FALSE.  |
|  *logical_test2* | Optional. Additional conditions that you want to evaluate as TRUE or FALSE  |

## Pi

Returns the constant PI, 3.14159265358979, accurate to 15 digits.

```
PI()
```

The [!DNL PI]function has no arguments.

## Power regression: Correlation coefficient (Table)

Returns the correlation coefficient, *r*, between two metric columns (*metric_X* and *metric_Y*) for [!DNL Y = b*X].

```
CORREL.POWER(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to correlate with *metric_Y*.  |
|  *metric_Y* | A metric that you would like to correlate with *metric_X*.  |

## Power regression: Intercept (Table)

Returns the intercept, *b*, between two metric columns (*metric_X* and *metric_Y*) for [!DNL Y = b*X].

```
 INTERCEPT.POWER(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Power regression: Predicted Y (Row)

Calculates the predicted [!DNL y] values ( [!DNL metric_Y]), given the known [!DNL x] values ( [!DNL metric_X]) using the "least squares" method for calculating the line of best fit for [!DNL Y = b*X].

```
 ESTIMATE.POWER(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Power regression: Slope (Table)

Returns the slope, *a*, between two metric columns (*metric_X* and *metric_Y*) for [!DNL Y = b*X].

```
SLOPE.POWER(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Quadratic regression: Correlation coefficient (Table)

Returns the correlation coefficient, *r*, between two metric columns (*metric_X* and *metric_Y*) for [!DNL Y=(a*X+b)]****.

```
CORREL.QUADRATIC(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to correlate with *metric_Y*.  |
|  *metric_Y* | A metric that you would like to correlate with *metric_X*.  |

## Quadratic regression: Intercept (Table)

Returns the intercept, *b*, between two metric columns (*metric_X* and *metric_Y*) for [!DNL Y=(a*X+b)]****.

```
INTERCEPT.POWER(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Quadratic regression: Predicted Y (Row)

Calculates the predicted [!DNL y] values (metric_Y), given the known [!DNL x] values (metric_X) using the least squares method for calculating the line of best fit using [!DNL Y=(a*X+b)]**** .

```
ESTIMATE.QUADRATIC(metric_A, metric_B)
```

|  Argument  | Description  |
|---|---|
|  *metric_A* | A metric that you would like to designate as the dependent data.  |
|  *metric_B* | A metric that you would like to designate as the dependent data.  |

## Quadratic regression: Slope (Table)

Returns the slope, *a*, between two metric columns (*metric_X* and metric_Y) for [!DNL Y=(a*X+b)]****.

```
SLOPE.QUADRATIC(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Reciprocal regression: Correlation coefficient (Table)

Returns the correlation coefficient, *r*, between two metric columns (*metric_X)* and *metric_Y*) for [!DNL Y = a/X+b].

```
CORREL.RECIPROCAL(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to correlate with *metric_Y*.  |
|  *metric_Y* | A metric that you would like to correlate with *metric_X*.  |

## Reciprocal regression: Intercept (Table)

Returns the intercept, *b*, between two metric columns (*metric_X* and *metric_Y*) for [!DNL Y = a/X+b].

```
INTERCEPT.RECIPROCAL(metric_A, metric_B)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Reciprocal regression: Predicted Y (Row)

Calculates the predicted [!DNL y] values (metric_Y), given the known [!DNL x] values (metric_X) using the least squares method for calculating the line of best fit using [!DNL Y = a/X+b].

```
ESTIMATE.RECIPROCAL(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Reciprocal regression: Slope (Table)

Returns the slope, *a*, between two metric columns (*metric_X* and *metric_Y*) for [!DNL Y = a/X+b].

```
SLOPE.RECIPROCAL(metric_X, metric_Y)
```

|  Argument  | Description  |
|---|---|
|  *metric_X* | A metric that you would like to designate as the dependent data.  |
|  *metric_Y* | A metric that you would like to designate as the independent data.  |

## Sine (Row)

Returns the sine of the given angle. If the angle is in degrees, multiply the angle by PI( )/180.

```
SIN(metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The angle in radians for which you want the sine.  |

## T-Score

Alias for Z-Score, namely the deviation from the mean divided by the standard deviation

## T-Test

Performs an m-tailed t-test with t-score of col and n degrees of freedom.

The signature is `t_test( x, n, m )`. Underneath, it simply calls `m*cdf_t(-abs(x),n)`. (This is similar to the z-test function which runs `m*cdf_z(-abs(x))`.

Here, `m` is the number of tails, and `n` is the degrees of freedom. These should be numbers (constant for the whole report, i.e. not changing on a row by row basis).

`X` is the t-test statistic, and would often be a formula (e.g. zscore) based on a metric and will be evaluated on every row.

The return value is the probability of seeing the test statistic x given the degrees of freedom and number of tails.

**Examples:**

1. Use it to find outliers:

   ```
   t_test( zscore(bouncerate), row-count-1, 2)
   ```

1. Combine it with `if` to ignore very high or low bounce rates, and count visits on everything else:

   ```
   if ( t_test( z-score(bouncerate), row-count, 2) < 0.01, 0, visits )
   ```

## Tangent

Returns the tangent of the given angle. If the angle is in degrees, multiply the angle by PI( )/180.

```
TAN (metric)
```

|  Argument  | Description  |
|---|---|
|  *metric* | The angle in radians for which you want the tangent.  |

## Z-Score (Row)

Returns the Z-score, or normal score, based upon a normal distribution. The Z-score is the number of standard deviations an observation is from the mean. A Z-score of 0 (zero) means the score is the same as the mean. A Z-score can be positive or negative, indicating whether it is above or below the mean and by how many standard deviations.

The equation for Z-score is:

![](assets/z_score.png)

where [!DNL x] is the raw score, [!DNL μ] is the mean of the population, and [!DNL σ] is the standard deviation of the population.

>[!NOTE]
>
>[!DNL μ] (mu) and[!DNL σ] (sigma) are automatically calculated from the metric.

Z-score(metric)

<table id="table_AEA3622A58F54EA495468A9402651E1B">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Argument </th>
   <th colname="col2" class="entry"> Description </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"> <i>metric</i> </td>
   <td colname="col2"> <p> Returns the value of its first non-zero argument. </p> </td>
  </tr>
 </tbody>
</table>

## Z-Test

Performs an n-tailed Z-test with Z-score of A.

Returns the probability that the current row could be seen by chance in the column.

>[!NOTE]
>
>Assumes that the values are normally distributed.

-->