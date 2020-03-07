---
title: Referentie - basisfuncties
description: 'De Berekende Bouwer van Metriek laat u statistische en wiskundige functies toepassen om Geavanceerde Berekende Metriek te bouwen. '
translation-type: tm+mt
source-git-commit: b521079bb9b3828ec3487b635366f5442f6fc4bd

---


# Referentie - basisfuncties

De Berekende Bouwer van Metriek laat u statistische en wiskundige functies toepassen om Geavanceerde Berekende Metriek te bouwen.

Hier is een alfabetische lijst van de functies en hun definities.

> [!NOTE] Waar [!DNL metric] als argument in een functie wordt geïdentificeerd, worden andere uitdrukkingen van metriek ook toegestaan. Bijvoorbeeld, staat [!DNL MAXV(metrics)] ook toe voor [!DNL MAXV(PageViews + Visits).]

## Tabel Functies versus Row-functies

Een lijstfunctie is één waar de output het zelfde voor elke rij van de lijst is. Een rijfunctie is één waar de output voor elke rij van de lijst verschillend is.

## Absolute waarde (rij)

Keert de absolute waarde van een aantal terug. De absolute waarde van een aantal is het aantal met een positieve waarde.

```
ABS(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Metrisch waarvoor u de absolute waarde wilt. |

## Maximum kolom

Keert de grootste waarde in een reeks afmetingselementen voor een metrische kolom terug. MAXV evalueert verticaal binnen één enkele (metrische) kolom over afmetingselementen.

```
MAXV(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Een metrisch die u zou willen geëvalueerd hebben. |

## Minimaal kolom

Keert de kleinste waarde in een reeks afmetingselementen voor een metrische kolom terug. MINV evalueert verticaal binnen één enkele (metrische) kolom over afmetingselementen.

```
MINV(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Een metrisch die u zou willen geëvalueerd hebben. |

## Kolom Som

Voegt alle numerieke waarden voor metrisch binnen een kolom (over de elementen van een afmeting) toe.

```
SUM(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Metrisch waarvoor u de totale waarde of de som wilt. |

## Aantal (tabel)

Keert het aantal, of de telling, van niet-nul waarden voor metrisch binnen een kolom (het aantal unieke die elementen terug binnen een afmeting worden gemeld).

```
COUNT(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De metrisch die u wilt tellen. |

## Exponent (rij)

Keert op *e* opgeheven aan de macht van een bepaald aantal terug. De constante *e* is 2.71828182845904, de basis van de natuurlijke logaritme. EXP is het omgekeerde van LN, de natuurlijke logaritme van een aantal.

```
EXP(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | De exponent was van toepassing op de basis *e*. |

## Uitstel

Energiebeheerder

<pre>
pow(x,y) =<sup>xy</sup> = x*x*x*.. (y times)
</pre>

## Gemiddelde (tabel)

Keert het rekenkundig gemiddelde, of gemiddelde, voor metrisch in een kolom terug.

```
MEAN(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Metrisch waarvoor u het gemiddelde wilt. |

## Mediaan (tabel)

Keert de mediaan voor metrisch in een kolom terug. De mediaan is het aantal in het midden van een reeks aantal-dat is, hebben de helft de aantallen waarden die groter dan of gelijk aan de mediaan zijn, en de helft is minder dan of gelijk aan de mediaan.

```
MEDIAN(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Metrisch waarvoor u de mediaan wilt. |

## Modulo

De rest van col1/col2, gebruikmakend van Euclidean-divisie.

Keert de rest na het verdelen x door y terug.

```
x = floor(x/y) + modulo(x,y)
```

De terugkeerwaarde heeft het zelfde teken zoals de input (of is nul).

```
modulo(4,3) = 1 
modulo(-4,3) = -1 
modulo(-3,3) = 0
```

Om altijd een positief aantal te krijgen, gebruik

```
modulo(modulo(x,y)+y,y)
```

## Percentiel (tabel)

Keert het k-th percentiel van waarden voor metrisch terug. U kunt deze functie gebruiken om een drempel van goedkeuring te vestigen. Bijvoorbeeld, kunt u beslissen afmetingselementen te onderzoeken die boven het 90 percentiel scoren.

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
   <td colname="col1"> <i>metrisch</i> </td> 
   <td colname="col2"> De metrische kolom die relatieve staat bepaalt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>k </p> </td> 
   <td colname="col2"> De percentielwaarde in waaier 0 tot 100, inclusief. </td> 
  </tr> 
 </tbody> 
</table>

## Kwart (tabel)

Keert het kwartiel van waarden voor metrisch terug. Bijvoorbeeld, kunnen de kwartielen worden gebruikt om de hoogste 25% van producten te vinden die de meeste opbrengst drijven. MINV, MEDIAN, en MAXV keren de zelfde waarde terug zoals KWANTITAAL wanneer de quart aan 0 (nul), 2, respectievelijk 4 gelijk is.

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
   <td colname="col1"> <i>metrisch</i> </td> 
   <td colname="col2"> Metrisch waarvoor u de kwartielwaarde wilt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>kwart </p> </td> 
   <td colname="col2"> Wijst op welke *value aan terugkeer. </td> 
  </tr> 
 </tbody> 
</table>

*If *quart* = 0, KWAAR de minimumwaarde terug. Als *quart* = 1, keert QUARTILE het eerste kwartiel (25 percentiel) terug. Als *quart* = 2, keert QUARTILE het eerste kwartiel (50 percentiel) terug. Als *quart* = 3, keert QUARTILE het eerste kwartiel (75 percentiel) terug. Als *quart* = 4, KWAAR de maximumwaarde terug.

## Rond

Keert het meest dichtbijgelegen geheel voor een bepaalde waarde terug. Bijvoorbeeld, als u het melden van muntdecimalen voor opbrengst wilt vermijden en een product $569.34 heeft, gebruik de formuleRonde ( *Opbrengst*) aan ronde opbrengst aan de dichtstbijzijnde dollar, of $569. Een product dat $569,51 meldt, is rond tot de dichtstbijzijnde dollar, of $570.

```
ROUND(metric)
```

| Argument | Beschrijving |
|---|---|
| *nummer* | De metrisch u wilt ronden. |

Rond zonder een cijferparameter is het zelfde als rond met een cijferparameter van 0, namelijk rond aan het meest dichtbijgelegen geheel. Met een cijferparameter keert het dat vele cijfers rechts van de decimaal terug. Als de cijfers negatief zijn, keert het 0&#39;s links van de decimaal terug.

```
round( 314.15, 0) = 314 
round( 314.15, 1) = 314.1 
round( 314.15, -1) = 310 
round( 314.15, -2) = 300
```

## Aantal rijen

Keert de telling van rijen voor een bepaalde kolom (het aantal unieke die elementen terug binnen een afmeting worden gemeld). &quot;Overschrijding&quot; wordt geteld als 1.

## Row Max

Het maximum van de kolommen in elke rij.

## Row Min

Het minimum van de kolommen in elke rij.

## Row Sum

De som kolommen van elke rij.

## Vierkante wortel (rij)

Keert de positieve vierkantswortel van een aantal terug. De vierkantswortel van een aantal is de waarde van dat aantal dat aan de macht van 1/2 wordt opgeheven.

```
SQRT(metric)
```

| Argument | Beschrijving |
|---|---|
| *nummer* | Metrisch waarvoor u de vierkantswortel wilt. |

## Standaardafwijking (tabel)

Keert de standaardafwijking, of vierkantswortel van de variantie terug, die op een steekproefpopulatie van gegevens wordt gebaseerd.

De vergelijking voor STDEV is:

![](assets/std_dev.png)

waarin x het gemiddelde (*metrisch*) van het monster is en *n* de steekproefgrootte.

```
STDEV(metric)
```

<table id="table_8BCF2E4B02434AABAAD026FB3C4E8B2F"> 
 <tbody> 
  <tr> 
   <td> <b> Argument</b> </td> 
   <td> <b> Beschrijving</b> </td> 
  </tr> 
  <tr> 
   <td> <b> <i> metrisch</i></b> </td> 
   <td> <p> Metrisch waarvoor u voor standaardafwijking wilt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Variantie (tabel)

Keert de variantie terug die op een steekproefpopulatie van gegevens wordt gebaseerd.

De vergelijking voor VARIANCE is:

![](assets/variance_eq.png)

waarbij x het gemiddelde van het monster is, MEAN(*metrisch*) en *n* de steekproefgrootte.

```
VARIANCE(metric)
```

| Argument | Beschrijving |
|---|---|
| *metrisch* | Metrisch waarvoor u de variantie wilt. |

om een variantie te berekenen bekijkt u een volledige kolom van aantallen. Van die lijst van aantallen berekent u eerst het gemiddelde. Zodra u het gemiddelde hebt ga u door elke ingang en doe het volgende:

1. Trek het gemiddelde van het aantal af.

2. Het resultaat uitlijnen.

3. Voeg dat toe aan het totaal.

Zodra u over de volledige kolom hebt herhaald hebt u één enkel totaal. U verdeelt dan dat totaal door het aantal punten in de kolom. Dat aantal is de variantie voor de kolom. Het is één getal. Het wordt, echter, getoond als kolom van aantallen.

Als voorbeeld, zeg u een drie-puntskolom hebt:

1

2

3

Het gemiddelde van deze kolom is 2. De variantie voor de kolom is ((1 - 2)² + (2 - 2)² + (3 - 2)²/3 = 2/3. In Ad hoc Analyse zal dit als dit kijken:

1 2/3

2 2/3

3 2/3
