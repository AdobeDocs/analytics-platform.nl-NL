---
description: Voor de prognose in Analysis Workspace wordt een reeks geavanceerde statistische technieken gebruikt om de voorspelde waarden te bepalen.
title: Statistische technieken voor prognoses
feature: Visualizations
role: User
source-git-commit: 1bd24ee1163e4615bf5626c51aec9f167352f2f6
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---


# Statistische technieken voor de prognose

De dienst van het voorspellen steunt momenteel Profeet en is getoond om efficiënt en betrouwbaar voor de meeste gegevens te werken. Prophet is een veelgebruikt opensource-prognosepakket dat door Meta is ontwikkeld. Het ontleedt gegevens in tendensen, seizoensinvloeden, en gebeurteniscomponenten. Het Prophet model is efficiënt en schalen goed aan vele het voorspellen toepassingen. Bovendien werkt het model krachtig tegen uitschieters en ontbrekende gegevens.

In de toekomst zijn er plannen om modellen te selecteren op basis van heuristiek, bijvoorbeeld Online Approximate Gaussian Proces voor het stromen van gegevens, of NeuralProfeet te kiezen wanneer de gebruikers beste het voorspellen nauwkeurigheid specificeren en langere wachttijd kunnen tolereren.

De service downloadt automatisch gegevens wanneer er te veel gegevenspunten zijn, om de responstijd te garanderen. De doelresponstijd is ingesteld op ~3 seconden. Op dit moment, wanneer het aantal gegevenspunten groter is dan 5500, worden de gegevens van de tijdreeksen adaptief gedownsampled, afhankelijk van de lengte van de gegevens. De uitvoer wordt teruggezet naar de oorspronkelijke gegevensfrequentie, zodat het adaptieve samplingproces de gebruikerservaring niet beïnvloedt.

De vakantie-effecten worden in overweging genomen wanneer er meerdere jaren gegevens beschikbaar zijn. Momenteel wordt de lijst met vakanties in kwestie als volgt vastgesteld:

* Martin Luther King Day
* Voorzitter Dag
* Herdenkingsdag
* Juli 4
* Thanksgiving
* Zwarte vrijdag
* Cyber maandag
* Kerstmis

De dienst kan een eenvoudige anomalie (uitschieters) verwijdering ook doen, bijvoorbeeld door gegevenspunten te verwijderen die buiten zes sigmawaaier zijn. Dit is niet standaard ingeschakeld omdat alle gegevenspunten geldig zijn. Anomalies kunnen een negatieve invloed hebben op de kwaliteit van het model, ook al is het Profeet-model in het algemeen veerkrachtig voor buitenstaanders.

De service accepteert door de gebruiker opgegeven seizoensgebondenheid-instellingen, bijvoorbeeld seizoensgebondenheid per dag en per week. Anders selecteert het model automatisch de seizoensgebondenheid. Voor verschillende gegevensgranulariteit, gebruikt de dienst verschillende lengten van historische gegevens om het voorspellen modellen te bouwen. Voor dagelijkse gegevens worden bijvoorbeeld meer dan een jaar gegevens verzameld (indien beschikbaar). Voor uurgegevens worden er acht weken gegevens verzameld (indien beschikbaar). Het trekken van gegevens kan tijdrovend zijn en veroorzaakt soms langere wachttijd.

De historische gegevens die vereist zijn voor verschillende tijdsgranulariteit:

| Granulariteit | Vereiste historische gegevens |
|---|--:|
| Minute | 3 dagen |
| Uur | 2 weken |
| Dag | 8 weken |
| Week | 2 jaar |
| Maand | 2 jaar |
| Kwart | 8 kwart |
| Jaar | 8 jaar |


Het prognoseresultaat voor elke gespecificeerde tijd komt met een voorspellingsinterval (dat door onderste en bovengrens wordt bepaald), dat naar verwachting de toekomstige waargenomen waarde 95% van de tijd zal bevatten, vaak, die als betrouwbaarheidsinterval wordt bedoeld. Er is geen limiet aan de mate waarin de dienst in de toekomst kan voorspellen. De onzekerheid in de prognose neemt echter toe met data die verder in de toekomst liggen, hetgeen tot uiting komt in een breder voorspellingsinterval in de loop der tijd.

De dienst maakt geen veronderstellingen over gebruikersgegevens. Bijvoorbeeld, veronderstelt de dienst niet de gegevens niet negatief zijn. Dit betekent dat de prognoses en/of de grenzen daarvan negatief kunnen zijn, als de gegevens een sterke neerwaartse trend vertonen, ook al zijn alle waargenomen gegevenspunten niet-negatief.


## Verwijzingen

1. Taylor, Sean J., en Benjamin Letham: *Prognoses op schaal.* The American Statisticus 72.1 (2018): 37-45.
1. Triebe, Oskar, et al.: *Neuralprophet: Verklarende prognose op schaal.* arXiv preprint arXiv:211.15397(2021).
1. Zhang en Arbor: *Nauwkeurige detectie van tijdreeksen.* Amerikaanse octrooiaanvraag #18/057883.

