---
description: De anomalische opsporing in de Werkruimte van de Analyse maakt gebruik van een reeks geavanceerde statistische technieken om te bepalen of een waarneming al dan niet als abnormaal moet worden beschouwd.
title: Statistische technieken voor anomaliedetectie
uuid: b6ef6a2e-0836-4c9a-bf7e-01910199bb92
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 2%

---


# Statistische technieken voor anomaliedetectie

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

De anomalische opsporing in de Werkruimte van de Analyse maakt gebruik van een reeks geavanceerde statistische technieken om te bepalen of een waarneming al dan niet als abnormaal moet worden beschouwd.

Afhankelijk van de in het rapport gebruikte datum van granulariteit worden drie verschillende statistische technieken gebruikt - specifiek voor de anomaliedetectie per uur, dag, week of maand. Elke statistische techniek wordt hieronder beschreven.

## Anomalische detectie voor dagelijkse granulariteit

Voor dagelijkse granularity overzichten, overweegt het algoritme verscheidene belangrijke factoren om de nauwkeurigste mogelijke resultaten te leveren. Eerst, bepaalt het algoritme welk type van model dat op beschikbare gegevens wordt gebaseerd waarvan wij tussen één van twee klassen - een op tijd-reeks-gebaseerd model of een uitbijter-ontdekkingsmodel (genoemd functioneel het filtreren) selecteren.

De keuze van het tijdreeksmodel is gebaseerd op de volgende combinaties voor het type fout, trend en seizoensgebondenheid (ETS) zoals beschreven door [Hyndman et al. (2008)](https://www.springer.com/us/book/9783540719168). Specifiek, probeert het algoritme de volgende combinaties:

1. ANA (additieve fout, geen trend, additieve seizoensgebondenheid)
1. AAA (additieve fout, additieve trend, additieve seizoensgebondenheid)
1. MNM (multiplicatieve fout, geen trend, multiplicatieve seizoensgebondenheid)
1. MNA (multiplicatieve fout, geen trend, additieve seizoensgebondenheid)
1. AN (additieve fout, additieve trend, geen seizoensgebondenheid)

Het algoritme test de geschiktheid van elk van deze door met het beste gemiddelde absolute percentagefout (MAPE) te selecteren. Als de MAPE van het beste model van de tijdreeks groter is dan 15% nochtans, wordt het functionele filtreren toegepast. Doorgaans zijn gegevens met een hoge herhalingsgraad (bv. week in week of maand in maand) het beste geschikt voor een tijdreeksmodel.

Na modelselectie, past het algoritme dan de resultaten aan die op vakantie, en jaar-over-jaar seizoonaliteit worden gebaseerd. Voor feestdagen controleert het algoritme of een van de volgende feestdagen aanwezig is in het rapporteringsdatumbereik:

* Herdenkingsdag
* Juli 4
* Thanksgiving
* Zwarte Vrijdag
* Cyber Maandag
* 24-26 december
* Januari 1
* 31 december

Deze vakanties werden geselecteerd op basis van uitgebreide statistische analyse van vele klantgegevens om vakanties te identificeren die het meest tot het hoogste aantal trends van klanten deden. Terwijl de lijst zeker niet uitputtend voor alle klanten of bedrijfscycli is, vonden wij dat het toepassen van deze vakantie beduidend de prestaties van het algoritme algemeen voor bijna alle datasets van klanten verbeterde.

Zodra het model is geselecteerd en de feestdagen in de rapporteringsdatumwaaier zijn geïdentificeerd, gaat het algoritme op de volgende manier te werk:

1. Constructie van de afwijkende referentieperiode - dit omvat tot 35 dagen vóór de rapporteringsdatumwaaier, en een matchingdatumwaaier 1 jaar voorafgaand (die voor schrikkeldagen wanneer vereist en met inbegrip van enige toepasselijke vakantie rekenschap geeft die op een verschillende kalenderdag van het vorige jaar kan hebben plaatsgevonden).
1. Test of de vakanties in de huidige periode (exclusief het voorgaande jaar) op basis van de meest recente gegevens anomalisch zijn.
1. Als de vakantie in de huidige datumwaaier anomalisch is, pas de verwachte waarde en het betrouwbaarheidsinterval van de huidige vakantie aan gezien de vakantie van het voorafgaande jaar (met inachtneming van twee dagen vóór en na). De correctie voor de huidige vakantie is gebaseerd op het laagste gemiddelde absolute foutenpercentage van:

   1. Additieve effecten
   1. Multiplicatieve effecten
   1. YoY verschil

Let op de dramatische verbetering van de prestaties op kerstdag en nieuwjaarsdag in het volgende voorbeeld:

![](assets/anomaly_statistics.png)

## Anomaly detectie voor uurgranularity

Uurgegevens baseren zich op de zelfde methode van het tijdreeksenalgoritme die het dagelijkse granularity algoritme doet. Zij is echter sterk afhankelijk van twee trendpatronen: de 24-uurscyclus en de weekcyclus. Om deze twee seizoensinvloeden te vangen, construeert het uuralgoritme twee afzonderlijke modellen voor een weekend en een weekdag gebruikend de zelfde hierboven geschetste benadering.

De opleidingsvensters voor uurtrends baseren zich op een terugkijkvenster van 336 uur.

## Anomalische detectie voor wekelijkse en maandelijkse granulariteiten

Wekelijkse en maandelijkse trends vertonen niet dezelfde wekelijkse of dagelijkse trends die worden aangetroffen bij dagelijkse of uurlijke granulariteiten, zodat een dergelijk afzonderlijk algoritme wordt gebruikt. Voor wekelijkse en maandelijkse uitbijters wordt een tweestapsdetectiebenadering gebruikt, die bekend staat als de Gegeneraliseerde Extreme Studentized Deviate (GESD) test. Bij deze test wordt rekening gehouden met het maximumaantal verwachte anomalieën in combinatie met de aangepaste kastmethode (een niet-parametrische methode voor de detectie van uitbijters) om het maximumaantal uitschieters te bepalen. De twee stappen zijn:

1. Aangepaste functie voor het kavel-plot: Deze functie bepaalt het maximumaantal anomalieën dat aan de inputgegevens wordt gegeven.
1. GESD-functie: Toegepast op de inputgegevens met de output van stap 1.

De voor vakantie en &quot;Jeugd&quot; vastgestelde afwijkingsdetectiestap voor seizoensgebondenheid trekt de gegevens van vorig jaar vervolgens af van de gegevens van dit jaar en herhaalt vervolgens de gegevens opnieuw met behulp van het hierboven beschreven tweestapsproces om te controleren of de anomalieën seizoensmatig geschikt zijn. Elk van deze datumgranulariteiten gebruikt een terugblik van 15 periodes inclusief de geselecteerde rapporteringsdatumwaaier (of 15 maanden of 15 weken) en een overeenkomstige datumwaaier 1 jaar geleden voor opleiding.
