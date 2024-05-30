---
description: Leer hoe u de resultaten van tests A/B in het paneel van de Experimentatie van de Customer Journey Analytics kunt analyseren.
title: Deelvenster Experimentatie
feature: Panels
exl-id: e11169b4-2c73-4dd4-bca7-c26189d60631
role: User
source-git-commit: e0cf556a094726edbee35b21bf71d5d1f227fcc7
workflow-type: tm+mt
source-wordcount: '1838'
ht-degree: 0%

---

# Deelvenster Experimentatie

De **[!UICONTROL Experimentation]** in dit deelvenster kunnen analisten verschillende gebruikerservaringen, marketing of berichtvariaties vergelijken om te bepalen wat het beste is om een bepaald resultaat te bepalen. U kunt de lift en het vertrouwen van om het even welk A/B experiment van om het even welk experimentatieplatform evalueren - online, off-line, van Adobe oplossingen zoals Doel of Journey Optimizer, en zelfs (breng-uw-eigen) gegevens BYO.

Meer informatie over de [integratie tussen Adobe Customer Journey Analytics en Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/integrate/cja/target-reporting-in-cja).

## Toegangsbeheer {#access}

Het deelvenster Experimentatie kan door alle gebruikers van Customers Journey Analytics worden gebruikt. Er zijn geen beheerdersrechten of andere machtigingen vereist. Voor de installatie (stappen 1 en 2 hieronder) zijn echter handelingen vereist die alleen door beheerders kunnen worden uitgevoerd.

## Nieuwe functies in Berekende metriek {#functions}

Er zijn twee nieuwe geavanceerde functies toegevoegd: [!UICONTROL Lift] en [!UICONTROL Confidence]. Zie voor meer informatie [Referentie - geavanceerde functies](/help/components/calc-metrics/cm-adv-functions.md).

## Stap 1: Verbinding maken om gegevensset(s) te experimenteren {#connection}

Het aanbevolen gegevensschema is dat de experimentele gegevens zich in een [Objectarray](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/array) die de experimentele gegevens en de variantgegevens in twee afzonderlijke dimensies bevat. Beide dimensies moeten in een **enkel** objectarray. Als u uw experimentele gegevens in één dimensie hebt (met experimentele en variantgegevens in een afgebakende tekenreeks), kunt u de [substring](/help/data-views/component-settings/substring.md) het plaatsen in gegevensmeningen om de afmeting in twee voor gebruik in het paneel te verdelen.

Nadat uw experimentele gegevens zijn [ingesloten](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home) naar Adobe Experience Platform, [een verbinding maken in Customer Journey Analytics](/help/connections/create-connection.md) naar een of meer experimentele gegevenssets.

## Stap 2: Contextlabels toevoegen in gegevensweergaven {#context-labels}

In de weergave-instellingen van gegevensweergaven van Customers Journey Analytics kunnen beheerders toevoegen [contextlabels](/help/data-views/component-settings/overview.md) aan een afmeting of metrische en Customer Journey Analytics diensten zoals [!UICONTROL Experimentation] kunnen deze labels voor hun doeleinden gebruiken. Er worden twee vooraf gedefinieerde labels gebruikt voor het deelvenster Experimentatie:

* [!UICONTROL Experimentation Experiment]
* [!UICONTROL Experimentation Variant]

In uw gegevensmening die experimentatiegegevens bevat, kies twee afmeting, één met de experimentatiegegevens en één met de variantgegevens. Geef vervolgens een label aan deze afmetingen met de **[!UICONTROL Experiment]** en de **[!UICONTROL Variant]** labels.

![Context-labelopties voor Experimentation en Experimentation Variant.](assets/context-label.png)

Zonder deze labels werkt het deelvenster Experimenteren niet, omdat er geen experimenten zijn om mee te werken.

## Stap 3: Het deelvenster Experimenteren configureren {#configure}

1. In de Werkruimte van de Customer Journey Analytics, sleep het paneel van de Experimentatie in een project.

![Het deelvenster Experimentatie is naar een project gesleept.](assets/experiment.png)

>[!IMPORTANT]
>
>Als de vereiste opstelling in de gegevensmeningen van de Customer Journey Analytics niet is voltooid, ontvangt u dit bericht alvorens u kunt te werk gaan: &quot;[!UICONTROL Please configure the experiment and variant dimensions in Data Views]&quot;.
>

1. Configureer de instellingen voor deelvensterinvoer.

   | Instelling | Definitie |
   | --- | --- |
   | **[!UICONTROL Experiment]** | Een reeks variaties op een ervaring die aan eindgebruikers werden blootgesteld om te bepalen welke het beste is om in onbeperkte tijd te houden. Een experiment bestaat uit twee of meer varianten, waarvan er één als de besturingsvariant wordt beschouwd. Deze instelling is vooraf gevuld met de afmetingen die zijn gelabeld met de  **[!UICONTROL Experiment]** in gegevensweergaven en de waarde van het experiment van de laatste drie maanden. |
   | **[!UICONTROL Control Variant]** | Een van twee of meer wijzigingen in de ervaring van een eindgebruiker die worden vergeleken om het betere alternatief te identificeren. Eén variant moet als controlevariant worden gekozen en slechts één variant kan als controlevariant worden beschouwd. Deze instelling is vooraf gevuld met de afmetingen die zijn gelabeld met de  **[!UICONTROL Variant]** label in gegevensweergaven. Deze instelling geeft de variantgegevens weer die bij dit experiment horen. |
   | **[!UICONTROL Success Metrics]** | De metrische of metrische waarde waarmee een gebruiker varianten vergelijkt. De variant met het meest gewenste resultaat voor de omzettingsmeting (hoogste of laagste) wordt de &quot;best presterende variant&quot; van een experiment genoemd. U kunt maximaal vijf metriek toevoegen. |
   | **[!UICONTROL Normalizing Metric]** | De basis ([!UICONTROL People], [!UICONTROL Sessions], of [!UICONTROL Events]) waarop een test wordt uitgevoerd. Een test kan bijvoorbeeld de conversiesnelheden van verschillende variaties vergelijken, waarbij **[!UICONTROL Conversion rate]** wordt berekend als **[!UICONTROL Conversions per session]** of **[!UICONTROL Conversions per person]**. |
   | **[!UICONTROL Date Range]** | Het datumbereik wordt automatisch ingesteld op basis van de eerste gebeurtenis die in Customer Journey Analytics is ontvangen voor het geselecteerde experiment. Indien nodig kunt u het datumbereik beperken of uitbreiden tot een specifieker tijdsbestek. |

1. Klik op **[!UICONTROL Build]**.

## Stap 4: De uitvoer van het deelvenster weergeven {#view}

Het deelvenster Experimentatie bevat een uitgebreide set gegevens en visualisaties waarmee u beter kunt begrijpen hoe uw experimenten werken. Boven in het deelvenster ziet u een samenvattingsregel waarmee u de deelvensterinstellingen die u hebt geselecteerd, kunt herinneren. U kunt het deelvenster op elk gewenst moment bewerken door in de rechterbovenhoek op het potlood te klikken.

U krijgt ook een tekstsamenvatting die aangeeft of het experiment al dan niet overtuigend is en die het resultaat samenvat. Conclusiviteit is gebaseerd op statistische significantie. (Zie &quot;Statistische methodologie&quot; hieronder.) U kunt samenvattingsnummers zien voor de best presterende variant met de hoogste lichtsterkte en betrouwbaarheid.

Voor elk succes wordt metrisch u selecteerde, één vrije lijst en één omzettingstendens getoond.

![De output van de Experimentatie die één vrije lijst en één trend van de omzettingssnelheid toont.](assets/exp-output1.png)

De [!UICONTROL Line] de grafiek geeft u [!UICONTROL Control] versus [!UICONTROL Control Variant] prestaties:

![De uitvoer van de lijngrafiek die de prestaties van de Variant van de Controle tegenover van de Controle toont.](assets/exp-output2.png)

>[!NOTE]
>
>Dit panel ondersteunt momenteel geen analyse van A/A-tests.

## Stap 5: interpreteer de resultaten {#interpret}

1. **Experimenteer is Sluiten**: Telkens wanneer u het experimentatierapport bekijkt, worden de gegevens die zich in het experiment tot op dit punt hebben verzameld, geanalyseerd. En verklaart een experiment &quot;Sluiten&quot;wanneer het wanneer geldige vertrouwen een drempel van 95% overschrijdt voor *ten minste één* van de varianten (waarbij een Benjamini-Hochberg-correctie wordt toegepast wanneer er meer dan twee armen zijn, ter correctie voor meervoudige hypothesetests).

2. **Variant die het beste presteert**: Wanneer een experiment overtuigend wordt verklaard, wordt de variant met de hoogste omrekeningskoers aangeduid als de best presterende variant. Merk op dat deze variant ofwel de besturingsvariant of de basisvariant moet zijn, ofwel een van de varianten die de betrouwbaarheidsdrempel van 95% overschrijdt (met Benjamini-Hochberg correcties toegepast).

3. **Conversiesnelheid**: De omrekeningskoers die wordt getoond is een verhouding van de metrische waarde van het succes aan de normaliserende metrische waarde. Merk op dat deze waarde soms groter kan zijn dan 1, als metrisch niet binair is (1 of 0 voor elke eenheid in het experiment)

4. **Optillen**: De samenvatting van het Experimentenrapport toont de Lift over Basislijn, die een maat is voor de procentuele verbetering van de conversiesnelheid van een bepaalde variant ten opzichte van de basislijn. Dit is het verschil in prestaties tussen een bepaalde variant en de basislijn, gedeeld door de prestaties van de basislijn, uitgedrukt als een percentage.

5. **Vertrouwen**: Het op elk moment geldige vertrouwen dat wordt aangetoond, is een probabilistische maat van hoeveel bewijs er is dat een bepaalde variant dezelfde is als de besturingsvariant. Een hoger vertrouwen geeft minder bewijs voor de aanname dat de besturingsvariant en de niet-besturingsvariant dezelfde prestaties leveren. Meer in het bijzonder is het vertrouwen dat wordt weergegeven een waarschijnlijkheid (uitgedrukt als een percentage) dat u een kleiner verschil in omrekeningskoersen tussen een bepaalde variant en het besturingselement zou hebben waargenomen, als er in werkelijkheid geen verschil is in de werkelijke onderliggende omrekeningskoersen. In termen van *p*-waarden, het weergegeven vertrouwen is 1 - *p*-value.

>[!NOTE]
>
>Bij een volledige beschrijving van de resultaten moet rekening worden gehouden met alle beschikbare gegevens (bijvoorbeeld het ontwerp van het experiment, de steekproefgrootten, de omrekeningskoersen, het vertrouwen, enzovoort) en niet alleen met de verklaring van overtuigend of niet. Zelfs wanneer een resultaat nog niet overtuigend is, kan er nog steeds overtuigend bewijs zijn dat een bepaalde variant anders is dan een andere (betrouwbaarheidsintervallen zijn bijvoorbeeld bijna niet-overlapt). Idealiter zouden alle statistische gegevens, die op een continu spectrum worden geïnterpreteerd, de besluitvorming moeten beïnvloeden.

## Statistische methodologie van de Adobe {#statistics}

Om gemakkelijk te interpreteren en veilige statistische conclusies te kunnen trekken, heeft de Adobe een statistische methodologie aangenomen die gebaseerd is op [Altijd geldige betrouwbaarheidsreeksen](https://arxiv.org/abs/2103.06476).

Een betrouwbaarheidsreeks is een *sequentieel* analoog van een betrouwbaarheidsinterval. Om te begrijpen wat een vertrouwensopeenvolging is, stel voor herhalend uw experimenten honderd keer, en het berekenen van een schatting van gemiddelde bedrijfs metrisch (bijvoorbeeld open tarief van een e-mail) en zijn bijbehorende 95%-betrouwbaarheidsopeenvolging voor *elke nieuwe gebruiker* dat het experiment binnenkomt.

Een 95% betrouwbaarheidsreeks omvat de &quot;ware&quot;waarde van zaken metrisch in 95 van de 100 experimenten die u in werking stelde. (Een betrouwbaarheidsinterval van 95% kon slechts eenmaal per experiment worden berekend om dezelfde 95% dekkingsgarantie te geven, niet bij elke nieuwe gebruiker). Met vertrouwensreeksen kunt u dus voortdurend experimenten volgen zonder dat het aantal fout-positieve fouten toeneemt, dat wil zeggen dat het gebruik van &quot;peeking&quot; bij resultaten is toegestaan.

## Niet-gerandomiseerde afmetingen interpreteren {#non-randomized}

Met Customer Journey Analytics kunnen analisten elke gewenste dimensie selecteren als &#39;experiment&#39;. Maar hoe interpreteer je een analyse waarbij de als experiment gekozen dimensie niet een is waarvoor mensen willekeurig worden gekozen?

Neem bijvoorbeeld een advertentie die een persoon ziet. Misschien bent u geïnteresseerd in het meten van de verandering in wat metrisch (bijvoorbeeld gemiddelde opbrengst) als u besluit om personen &quot;ad B&quot; in plaats van &quot;ad A&quot; te tonen. Het causale effect van het aantonen van advertentie B in plaats van advertentie A is van cruciaal belang om tot het besluit over het in de handel brengen te komen. Dit causale effect kan worden gemeten als de gemiddelde opbrengst over de gehele bevolking, indien u de status quo van het tonen van steun A vervangt door de alternatieve strategie van het tonen van steun B.

A/B-tests zijn de gouden standaard in de industrie voor het objectief meten van de effecten van dergelijke interventies. De kritieke reden waarom een A/B-test aanleiding geeft tot een causale schatting is te wijten aan de randomisatie van personen die een van de mogelijke varianten ontvangen.

Kijk nu eens naar een dimensie die niet bereikt wordt door randomisatie, bijvoorbeeld, de staat van de persoon in de VS. Laten we zeggen dat mensen voornamelijk uit twee staten komen, New York en Californië. De gemiddelde omzet van de verkoop van een winterkledingmerk kan in beide staten verschillen als gevolg van de verschillen in het regionale weer. In een dergelijke situatie kan het weer de werkelijke oorzaak zijn van de verkoop van winterkleding, en niet het feit dat de geografische situatie van personen verschillend is.

Met het deelvenster voor experimenten in de Customer Journey Analytics kunt u gegevens analyseren als het gemiddelde inkomstenverschil per land van de persoon. In een dergelijke situatie heeft de output geen causale interpretatie. Een dergelijke analyse kan echter nog steeds van belang zijn. Het geeft een schatting (samen met maatstaven voor onzekerheid) van het verschil in gemiddelde inkomsten van de staten van de personen.  Deze waarde wordt ook wel &quot;Statistical Hypothesis Testing&quot; genoemd. Het resultaat van deze analyse is misschien interessant, maar niet noodzakelijkerwijs actionabel, omdat u personen niet en soms niet kunt koppelen aan een van de mogelijke waarden van de dimensie.

In de volgende afbeelding worden deze situaties gecontrasteerd:

![Een diagram met waarnemingsgegevens en het gerandomiseerde experiment.](assets/randomize.png)

Wanneer u het effect van interventie X op resultaat Y wilt meten, is het mogelijk dat de werkelijke oorzaak van beide factoren de verwarrende factor C is. Als de gegevens niet worden bereikt door personen op X te randomiseren, is de impact moeilijker te meten en de analyse verklaart uitdrukkelijk voor C. Randomization breekt de afhankelijkheid van X op C, die ons toestaat om het effect van X op Y te meten zonder het moeten zich over andere variabelen ongerust maken.

## Berekende meetwaarden gebruiken in het deelvenster Experimentatie

Zie dit blogbericht voor meer informatie over [afgeleide meetgegevens gebruiken in het deelvenster Experimentatie](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/using-derived-metrics-in-cja-s-experimentation-panel/ba-p/593119).
