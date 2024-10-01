---
title: Referentie - basisfuncties
description: Met de Calculated Metrics Builder kunt u statistische en wiskundige functies toepassen om geavanceerde berekende metriek te bouwen.
feature: Calculated Metrics
exl-id: 63775753-337b-4dec-a3a2-a3a0ee9aac2e
role: User
source-git-commit: 5b441472a21db99728d012c19f12d98f984086f5
workflow-type: tm+mt
source-wordcount: '1071'
ht-degree: 1%

---

# Referentie - basisfuncties


De [ Berekende metrieke bouwer ](cm-workflow/cm-build-metrics.md) laat u statistische en wiskundige functies toepassen.

Hier volgt een alfabetische lijst van de functies en hun definities.

>[!NOTE]
>
>Waar [!DNL metric] wordt geïdentificeerd als een argument in een functie, zijn andere expressies van metriek ook toegestaan. [!DNL MAXV(metrics)] staat bijvoorbeeld ook [!DNL MAXV(PageViews + Visits).] toe


## Tabelfuncties versus rijfuncties

Een tabelfunctie is een functie waarbij de uitvoer voor elke rij van de tabel hetzelfde is. Een rijfunctie is een functie waarbij de uitvoer voor elke rij van de tabel anders is.



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

![](assets/std_dev.png)

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

![](assets/variance_eq.png)

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
