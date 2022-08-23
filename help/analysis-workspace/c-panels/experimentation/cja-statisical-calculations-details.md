---
source-git-commit: c95e01a80f3f3ddcabfee171ee357a5cf9e81e53
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---
# Statistische berekeningen in het deelvenster Experimentatie van CJA: Details

Deze pagina documenteert de gedetailleerde statistische berekeningen die in het Experimentatievenster van CJA worden gebruikt. Het is bestemd voor technische gebruikers.


## Omzetsnelheid

de omrekeningskoers of **gemiddelde**, *μ<sub>ν</sub>* voor elke variant *ν* in een experiment wordt gedefinieerd als een verhouding tussen de som van de metrieke eenheden en het aantal eenheden dat aan die meting is toegewezen; *N<sub>ν</sub>*:
<p style="text-align:center;"><img width="15%" src="img/mean_definition.png" alt="metrisch gemiddelde"></p>
Hier,

- *Y<sub>ν</sub>* is de waarde van metrisch voor elke eenheid *i*, die is toegewezen aan een bepaalde variant *ν*.
- De som over eenheden *i* hangt van de keus van het normaliseren metrisch af.
   - Indien *Mensen* is normaliserend metrisch, is elke eenheid een unieke persoon/profiel.
   - Indien *Sessies* is normaliserend metrisch, is elke eenheid een unieke zitting.
   - Indien *Gebeurtenissen* is normaliserend metrisch, is elke eenheid een unieke gebeurtenis.

In het algemeen, zou deze het normaliseren metrisch moeten worden gekozen om aan uw eenheid van onafhankelijkheid gelijkwaardig te zijn, d.w.z., als het gedrag van een gebruiker in één zitting van hun gedrag in een andere zitting onafhankelijk zal zijn, dan zijn de zittingen redelijk normaliserend metrisch.

Waar nodig wordt de standaardafwijking van het monster gebruikt, met de uitdrukking


<p style="text-align:center;"><img width="30%" src="img/stdev_definition.png" alt="metrisch gemiddelde"></p>


## Optillen

De lift tussen een variant  *ν* en de besturingsvariant  *ν<sub>0</sub>* is de relatieve &quot;delta&quot; in omrekeningskoersen, gedefinieerd als
<p style="text-align:center;"><img width="15%" src="img/lift_definition.png" alt="metrisch gemiddelde"></p>
wanneer de afzonderlijke omrekeningskoersen overeenkomen met de hierboven omschreven waarden.


## Vertrouwensreeksen

De vertrouwensreeks voor een afzonderlijke variant wordt niet weergegeven in het deelvenster CJA-experimenten *ν* centraal staat in de door Adobe gebruikte statistische methodologie en zo wordt hier gedefinieerd (weergegeven op basis van [Waudby-Smith et al.](https://doi.org/10.48550/arXiv.2103.06476)).

> Stel dat u geïnteresseerd bent in het schatten van een doelparameter *ψ* (zoals de conversiesnelheid van een variant in een experiment). Vervolgens kan de tweedeling tussen een reeks &quot;vaste-tijdvertrouwensintervallen&quot; en een tijduniforme vertrouwensreeks als volgt worden samengevat:
<p style="text-align:center;"><img width="60%" src="img/ci_vs_cs.png" alt="metrisch gemiddelde"></p>

Met andere woorden - voor een regelmatig betrouwbaarheidsinterval, de probabilistische garantie dat de doelparameter binnen het waardenbereik ligt *Ċ<sub>t</sub>* is slechts geldig voor één vaste waarde van *n* waarbij *n* het aantal monsters). Omgekeerd geldt voor een betrouwbaarheidsreeks dat altijd/alle waarden van de monstergrootte *t* De &quot;werkelijke&quot; waarde van de parameter van belang ligt binnen de grenzen *<SPAN STYLE="text-decoration:overline">C</SPAN><sub>t</sub>*.

Dit heeft een aantal diepgaande implicaties die zeer belangrijk zijn voor online tests:
- Het CS kan desgewenst worden bijgewerkt wanneer nieuwe gegevens beschikbaar komen.
- Experimenten kunnen continu worden bewaakt, adaptief worden gestopt of voortgezet.
- De type-I fout wordt gecontroleerd bij alle stoptijden, met inbegrip van gegeven-afhankelijke tijden.

Adobe maakt gebruik van Asymptotic Betrouwbaarheidssequences, die voor een individuele variant met gemiddelde schatting *μ* heeft het formulier

<p style="text-align:center;"><img width="45%" src="img/confidence_sequence_individual.png" alt="metrisch gemiddelde"></p>

Waar:
- *N* is het aantal eenheden voor die variant
- *σ* is een steekproefschatting van de standaardafwijking (eerder gedefinieerd)
- *α* is het gewenste niveau van de type-I-fout (of de kans op een onjuiste dekking)
- *μ*<sup> 2</sup> is een constante waarmee de samplegrootte wordt ingesteld waarbij de CS het strengst is. Adobe heeft gekozen voor een universele waarde van *μ*<sup> 2</sup> = 10<sup>-2,8</sup>, die geschikt is voor de soorten omrekeningskoersen die in online-experimenten worden waargenomen.


## Vertrouwen

Het vertrouwen dat door Adobe wordt gebruikt is een &quot;op elk moment geldig&quot; vertrouwen, dat wordt verkregen door de betrouwbaarheidsvolgorde voor het gemiddelde behandelingseffect om te keren.

Om precies te zijn, stellen wij vast dat in een tweeledig voorbeeld *t* de test op het verschil in gemiddelden tussen twee varianten bestaat uit een 1:1-afbeelding tussen de *p*-waarde voor deze test en het betrouwbaarheidsinterval voor het verschil in gemiddelden. Naar analogie geldt een tijdsduur *p*-value kan worden verkregen door de (op elk moment geldige) betrouwbaarheidssequentie voor de gemiddelde schatting van het effect van de behandeling om te keren:
<p style="text-align:center;"><img width="22%" src="img/ate_definition.png" alt="metrisch gemiddelde"></p>

De schatter die wij gebruiken is een omgekeerde neiging gewogen (IPW) schatter. Overweeg *N = N<sub>0</sub>* + *N<sub>1</sub>* eenheden, de varianttoewijzingen voor elke eenheid $i$ gelabeld door *A<sub>i</sub>=0,1* indien de eenheid is toegewezen aan variant ν=0,1. Indien de gebruikers met een vaste waarschijnlijkheid (neiging) worden belast *π<sub>0</sub>, (1-π<sub>0</sub>)* en de resultaten ervan *Y<sub>i</sub>*, dan is de IPW-schatting
<p style="text-align:center;"><img width="45%" src="img/ipw_definition.png" alt="metrisch gemiddelde"></p>

Merk op dat *f* Waudby-Smith et al. toonde aan dat de Vertrouwensvolgorde voor deze schatter is:
<p style="text-align:center;"><img width="55%" src="img/cs_ate_definition1.png" alt="metrisch gemiddelde"></p>

De toewijzingswaarschijnlijkheid vervangen door de empirische schattingen: *π<sub>0</sub> = N<sub>0</sub>/N* kan de variantieterm worden uitgedrukt in het gemiddelde van de afzonderlijke monsters  *μ<sub>{0,1}</sub>* en standaardafwijkingsramingen,  *σ<sub>{0,1}</sub>* als:

<p style="text-align:center;"><img width="55%" src="img/cs_ate_var.png" alt="metrisch gemiddelde"></p>


Herinnerend aan het feit dat voor een reguliere hypothesetest met teststatistiek *z = (μ<sub>1</sub> - μ<sub>0</sub>)/ σ<sub>p</sub>*, is er een overeenkomst tussen $p$-waarden en betrouwbaarheidsintervallen:

<p style="text-align:center;"><img width="55%" src="img/pvalue_ci_correspondence.png" alt="metrisch gemiddelde"></p>

waar *#* de cumulatieve verdeling van de normale waarde. Voor altijd geldig *p*-waarden, gezien de betrouwbaarheidsvolgorde voor het hierboven gedefinieerde gemiddelde behandelingseffect, kunnen we deze relatie omkeren:
<p style="text-align:center;"><img width="75%" src="img/anytimevalid-pvalue.png" alt="metrisch gemiddelde"></p>

Tot slot **altijd geldig *vertrouwen*** is
<p style="text-align:center;"><img width="22%" src="img/anytimevalid-confidence.png" alt="metrisch gemiddelde"></p>


## Een experiment declareren als &quot;Sluiten&quot;

Voor een experiment met twee armen, toont het paneel van de Experimentatie CJA een bericht verklarend dat een Experimenteer is **overtuigend** wanneer het geldige betrouwbaarheidsinterval meer dan 95% bedraagt (d.w.z. *p*-waarde is lager dan 5%).

Wanneer meer dan twee varianten aanwezig zijn, wordt de Bonferoni-correctie toegepast. Voor een experiment met *K* en een enkele basisbehandeling (controle) *K-1* onafhankelijke hypothesetests. De Bonferoni-correctie betekent dat wij de nulhypothese verwerpen dat de controle en een bepaalde variant gelijke middelen hebben, als dat ooit zo is *p*-waarde is lager dan een drempelwaarde van 0,05/(K-1).


## Best presterende arm

Wanneer een experiment overtuigend wordt verklaard, wordt de best presterende arm getoond. Dit is de arm met de beste prestaties (hoogste gemiddelde of omzettingspercentage), onder de Reeks die de controle omvat, en alle armen die een *p*-waarde die onder de Bonferonni-drempel ligt.