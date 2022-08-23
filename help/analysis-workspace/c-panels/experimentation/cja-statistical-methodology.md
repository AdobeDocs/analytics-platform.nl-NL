---
source-git-commit: 99b190e1afe7068d11fd9d53c5be72008958a9c2
workflow-type: tm+mt
source-wordcount: '1446'
ht-degree: 0%

---
# Inleiding tot de statistische methodologie in het deelvenster Experimentatie van het CJA

In dit artikel worden de statistische berekeningen beschreven die door het panel van deskundigen in CJA worden gebruikt. CJA gebruikt geavanceerde statistische methoden om te berekenen **vertrouwen** dat op elk ogenblik geldig is, die u toestaat om uw experimenten zolang te leiden u wilt, en uw resultaten onophoudelijk te controleren.

In dit artikel wordt beschreven hoe A/B-tests werken en wordt een intuïtieve inleiding tot Adobe geboden ***Elke geldige betrouwbaarheidsreeks***. De technische details en verwijzingen zijn aan het eind opgenomen voor gebruikers van deskundigen.

## A/B-tests en oorzakelijk verband

A/B-tests worden vaak omschreven als een &quot;gouden standaard&quot; bij de beoordeling van de causale impact van een soort &quot;interventie&quot;. Het zijn gerandomiseerde tests, wat in de context van online tests betekent dat wij sommige willekeurig geselecteerde gebruikers aan een bepaalde variatie van een website, een bericht of een e-mail, en een andere willekeurig geselecteerde reeks gebruikers aan andere blootstellen **variant** of **behandeling**. Na blootstelling meten we vervolgens het resultaat **Metrisch(e)** we zijn geïnteresseerd in ( e-mails , abonnementen of aankopen worden bijvoorbeeld geopend ) .

Zoals in de onderstaande afbeelding wordt geïllustreerd, betekent het feit dat we willekeurig gebruikers toewijzen aan elke variantgroep dat de groepen gemiddeld dezelfde kenmerken zullen hebben. Elk verschil in resultaten kan dus worden geïnterpreteerd als een gevolg van de verschillen in ontvangen varianten, dat wil zeggen dat we een **causaal** verband tussen onze interventies en de resultaten waar wij belang bij hebben . Dit staat u toe om rigoureuze, verklaarbare, gegevens gedreven besluiten te nemen in het optimaliseren van uw bedrijfsdoelstellingen, en zo is het testen A/B een fundamenteel deel van toolkit van om het even welke moderne verpersoonlijkingsdeskundige.

<p style="text-align:center;"><img width="75%" src="img/causal-inference-cartoon.png" alt="causaal-inf"></p>


Een belangrijke vraag is nu of eventuele waargenomen verschillen &quot;echte effecten&quot; zijn of ontstaan door willekeur. Op intuïtieve wijze, als er slechts een klein verschil in de resultaatmetriek tussen groepen is, dan zou dit toevallig kunnen worden waargenomen, terwijl de grotere verschillen eerder &quot;reëel&quot;zullen zijn. De technische term hier is dat onze metingen *schattingen* van de werkelijke waarden van het gemiddelde voor elke variantgroep. Statistische effecttechnieken bieden ons manieren om de mate van onzekerheid in onze schattingen te kwantificeren - daar staan de concepten van **p-waarden** en **Vertrouwelijke intervallen** Maar om dit te begrijpen, moeten we eerst statistische fouten begrijpen.

## Statistische test- en controlefouten

Veel statistische methoden zijn ontworpen om twee soorten fouten te beheersen: **Onjuiste positieven** (fouten van type I), en **False Negatives** (Type II-fouten). Deze worden weergegeven in de onderstaande tabel.


<p style="text-align:center;"><img width="50%" src="img/contingency_table_stats_errors.png" alt="ContingencyTable"></p>


Een vals positief is een onjuiste afwijzing van de nulhypothese, terwijl dat juist is. In de context van online A/B-tests betekent dit dat we (ten onrechte) concluderen dat de resultaten van het zakendoen verschillend zijn tussen variantwapens, terwijl het in feite hetzelfde was. Voordat we het experiment uitvoeren, kiezen we doorgaans een drempel *α*. Nadat het experiment is uitgevoerd, *p*-value wordt berekend, en wij verwerpen ongeldig als *p &lt; α*. Een veel gebruikte drempel is *α*= 0 , 05 , wat betekent dat we op lange termijn verwachten dat 5 van de 100 experimenten valse positieven zijn .

Ondertussen betekent een False Negative dat we de nulhypothese niet verwerpen, terwijl die in feite onwaar is. Voor A/B-tests betekent dit dat we de nulhypothese niet afwijzen (terugroepen, in de nulhypothese staat dat de resultaatmeting voor de verschillende soorten hetzelfde is), terwijl deze in feite anders is. Om dit soort fouten te kunnen aanpakken, moeten we over het algemeen voldoende gebruikers in ons experiment hebben om een bepaalde **Voeding**, gedefinieerd als 1-*β* (d.w.z. één min de waarschijnlijkheid van een fout van type II).

Voor de meeste statistische bepalingstechnieken moet u de grootte van de steekproef vooraf bepalen op basis van de effectgrootte die u wilt bepalen en de fouttolerantie (*α* en *β*). Maar Adobe is ontworpen om voortdurend naar de resultaten te kijken, voor elke samplegrootte.



## Adobe _Altijd geldige betrouwbaarheidsreeksen_

Om gemakkelijk te interpreteren en veilige statistische conclusies te kunnen trekken, heeft Adobe een statistische methodologie aangenomen die gebaseerd is op [_Altijd geldige betrouwbaarheidsreeksen_](https://doi.org/10.48550/arXiv.2103.06476).

Een reeks van het Vertrouwen is een &quot;opeenvolgend&quot;analoog van een Interval van het Vertrouwen. Om te begrijpen wat een vertrouwensopeenvolging is, stel voor herhalend uw experimenten honderd keer, en het berekenen van een schatting van gemiddelde bedrijfsmetrisch (b.v. open tarief van een e-mail) en zijn bijbehorende 95%-Vertrouwensopeenvolging voor *elke nieuwe gebruiker* dat het experiment binnenkomt. Een 95% Vertrouwensreeks zal de &quot;ware&quot;waarde van zaken metrisch in 95 van de 100 experimenten omvatten die u in werking stelde. (Een betrouwbaarheidsinterval van 95% kan slechts eenmaal per experiment worden berekend om dezelfde 95%-dekkingsgarantie te bieden; niet bij elke nieuwe gebruiker). Met vertrouwensreeksen kunt u dus voortdurend experimenten volgen zonder dat de foutpercentages worden verhoogd, d.w.z. dat met deze resultaten kan worden gespiekt.

Het verschil tussen betrouwbaarheidsreeksen en betrouwbaarheidsintervallen voor één experiment wordt in de onderstaande animatie getoond:

<p style="text-align:center;"><img width="75%" src="img/confidence-sequence-evolution-comparison.gif" alt="CSGIF"></p>


We merken op dat vertrouwensreeksen de focus van A/B-tests verschuiven naar *schatting* in plaats van hypothesetests, d.w.z. waarbij de nadruk ligt op een nauwkeurige schatting van het verschil in middelen tussen behandelingen, en niet op het afwijzen van een nulhypothese op basis van een statistische significantiedrempel.

Nochtans, op een gelijkaardige manier aan het verband tussen $p$-values (of Vertrouwen) en de Intervallen van het Vertrouwen, is er ook een verband tussen de Reeksen van het Vertrouwen en om het even welk ogenblik geldige $p$-waarden (of om het even welk ogenblik geldig Vertrouwen). Gezien de vertrouwdheid van hoeveelheden als het Vertrouwen, biedt CJA altijd een geldig vertrouwen in haar verslagen.

De theoretische grondslagen van de Vertrouwensreeksen komen voort uit de studie van reeksen van willekeurige variabelen, die martingales worden genoemd. Hieronder vindt u een aantal belangrijke resultaten voor ervaren lezers, maar de overgangen voor de artsen zijn duidelijk:


> De opeenvolgingen van het vertrouwen kunnen als &quot;veilige&quot;opeenvolgende analogen van betrouwbaarheidsintervallen worden geïnterpreteerd: u kunt gegevens in uw A/B test op elk ogenblik bekijken en interpreteren u wilt, en veilig stoppen, of experimenten voortzetten. het overeenkomstige altijd geldige vertrouwen (of *p*-value) is ook veilig te interpreteren.

Aangezien de statistische methodologie &quot;op elk moment geldig&quot; is, is zij voorzichtiger dan een methode met een vaste tijdshorizon die op dezelfde steekproefomvang wordt toegepast. Dit betekent dat de &quot;altijd geldig&quot; *p*-waarden zijn doorgaans groter dan de overeenkomstige vaste horizon *p*-values (d.w.z. het altijd geldige vertrouwen zal kleiner zijn)

## De resultaten interpreteren

1. **Experimenteer is Sluiten**: Telkens wanneer u het experimentatierapport bekijkt, analyseert Adobe de gegevens die in het experiment tot op heden zijn verzameld en zal een experiment als &quot;Sluiten&quot; worden aangemerkt wanneer het altijd geldige vertrouwen een drempel van 95% overschrijdt voor *ten minste één* van de varianten (met een Bonferoni-correctie toegepast wanneer er meer dan twee armen zijn, om te corrigeren voor meervoudige hypothesetests).

2. **Best presterende variabele**: Wanneer een experiment overtuigend wordt verklaard, wordt de variant met de hoogste omrekeningskoers aangeduid als de best presterende variant. Deze variant moet ofwel de besturingsvariant of basislijnvariant zijn, ofwel een van de varianten die de 95% overschrijdt op een willekeurig moment geldige betrouwbaarheidsdrempel (met Bonferoni-correcties toegepast).

3. **Omzetsnelheid**: De omrekeningskoers die wordt getoond is een verhouding van de succes metrische waarde, aan de normaliserende metrische waarde. Merk op dat dit soms groter kan zijn dan 1, als metrisch niet binair is (1 of 0 voor elke eenheid in het experiment)

4. **Optillen**: De samenvatting van het experimentele rapport toont de Lift over de basislijn, die een maat is voor de procentuele verbetering van de conversiesnelheid van een bepaalde variant ten opzichte van de basislijn. Dit is het verschil in prestaties tussen een bepaalde variant en de basislijn, gedeeld door de prestaties van de basislijn, uitgedrukt als een percentage.

5. **Vertrouwen**: Het Geldige Vertrouwen van Anytime dat wordt getoond, is een probabilistische maatregel van hoeveel bewijs er is dat een bepaalde variant het zelfde als de controlevariant is. Een hoger vertrouwen geeft minder bewijs voor de aanname dat de besturingsvariant en de niet-besturingsvariant dezelfde prestaties leveren. Meer in het bijzonder is het vertrouwen dat wordt weergegeven een waarschijnlijkheid (uitgedrukt als een percentage) dat we een kleiner verschil in omrekeningskoersen tussen een bepaalde variant en het besturingselement zouden hebben gezien, als er in werkelijkheid geen verschil is in de werkelijke onderliggende omrekeningskoersen. In termen van *p*-waarden, het weergegeven vertrouwen is 1 - *p*-value.

Bij een volledige beschrijving van de resultaten moet echter rekening worden gehouden met alle beschikbare gegevens (bijv. opzet van het experiment, omvang van het monster, omrekeningskoersen, betrouwbaarheid enz.), en niet alleen met de verklaring van overtuigend of niet. Zelfs als een resultaat nog niet &quot;overtuigend&quot; is, kan er nog steeds overtuigend bewijs zijn dat de ene variant anders is dan de andere (zo zijn betrouwbaarheidsintervallen bijna niet-overlapt). Idealiter zou de besluitvorming moeten worden gebaseerd op alle statistische gegevens, die op een continu spectrum worden geïnterpreteerd.
