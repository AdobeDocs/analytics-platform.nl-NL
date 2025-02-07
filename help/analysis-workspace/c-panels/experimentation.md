---
description: Leer hoe u de resultaten van tests A/B in het paneel van de Experimentatie van de Customer Journey Analytics kunt analyseren.
title: Deelvenster Experimentatie
feature: Panels
exl-id: e11169b4-2c73-4dd4-bca7-c26189d60631
role: User
source-git-commit: dbf0ef92069778f6c805fa4315864b2c2c4a6622
workflow-type: tm+mt
source-wordcount: '2139'
ht-degree: 0%

---

# Deelvenster Experimentatie {#experimentation-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_experimentation_button"
>title="Experimentatie"
>abstract="Maak een deelvenster om verschillende gebruikerservaringen, marketing of berichtvariaties te vergelijken. En om te bepalen welke variatie het beste is om een specifiek resultaat te bepalen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_experimentation_panel"
>title="Experimentatie"
>abstract="Vergelijk verschillende gebruikerservaringen, marketing, of overseinenvariaties om te bepalen wat het best in het drijven van een specifiek resultaat is.<br/><br/>**Parameters **<br/>**Experiment**: Het experiment dat wordt geanalyseerd.<br>**variant van de Controle**: De variant van de controle voor het geselecteerde experiment.<br/>**metrisch van het Succes**: Tot 5 standaard (niet-berekende) succesmetriek om het experiment tegen te analyseren.<br/>**Normaliserend metrisch**: Mensen, zittingen, of gebeurtenissen. Deze maatstaf (ook wel de telmethode genoemd) wordt de noemer van de berekening van de lift. Deze maatstaf heeft ook invloed op de manier waarop de gegevens worden geaggregeerd voordat de betrouwbaarheidsberekening wordt toegepast."

<!-- markdownlint-enable MD034 -->


>[!BEGINSHADEBOX]

_dit artikel documenteert het paneel van de Experimentatie in_ ![ CustomerJourneyAnalytics ](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**._<br/>_zie [ Analytics voor het paneel van het Doel ](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/panels/a4t-panel) voor informatie over hoe te om de activiteiten en de ervaringen van Adobe Target in_ ![ AdobeAnalytics ](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics** te analyseren._

>[!ENDSHADEBOX]


In het deelvenster **[!UICONTROL Experimentation]** kunnen analisten verschillende gebruikerservaringen, marketing- of berichtvariaties vergelijken om te bepalen wat het beste is om een bepaald resultaat te bepalen. U kunt de lift en het vertrouwen van om het even welk A/B experiment van om het even welk experimentatieplatform evalueren: online, off-line, van Adobe oplossingen zoals Doel of Journey Optimizer, en zelfs (breng-uw-eigen) gegevens BYO.

Lees meer over de [ integratie tussen Adobe Customer Journey Analytics en Adobe Target ](https://experienceleague.adobe.com/en/docs/target/using/integrate/cja/target-reporting-in-cja).

## Toegangsbeheer {#access}

Het deelvenster Experimentatie kan door alle gebruikers van Customers Journey Analytics worden gebruikt. Er zijn geen beheerdersrechten of andere machtigingen vereist. Nochtans, vereisen de eerste vereisten acties die slechts de beheerders kunnen uitvoeren.

## Functies in berekende metriek

Er zijn twee geavanceerde functies beschikbaar: Optillen en Vertrouwen. Voor meer informatie, zie [ Verwijzing - geavanceerde functies ](/help/components/calc-metrics/cm-adv-functions.md).

## Vereisten

Als u het deelvenster voor experimenten wilt gebruiken, moet u aan de volgende voorwaarden voldoen:

### Verbinding maken om gegevenssets te experimenteren

Het geadviseerde gegevensschema is voor de experimentatiegegevens om in een [ serie van Objecten ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/array) te zijn die het experiment en de variantgegevens in twee afzonderlijke dimensies bevat. Beide dimensies moeten in a **enige** objecten serie zijn. Als u uw experimentatiegegevens in één enkele afmeting (met experiment en variantgegevens in een afgebakend koord) hebt, kunt u [ substring ](/help/data-views/component-settings/substring.md) gebruiken plaatsend in gegevensmeningen om de afmeting in twee voor gebruik in het paneel te verdelen.


Nadat uw experimentatiegegevens [ ](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home) in Adobe Experience Platform zijn opgenomen, [ creeer een verbinding in Customer Journey Analytics ](/help/connections/create-connection.md) aan één of meerdere experimentele datasets.

### Contextlabels toevoegen in gegevensweergaven

In de montages van de gegevensmeningen van de Customer Journey Analytics, kunnen beheerders [ contextetiketten ](/help/data-views/component-settings/overview.md) aan een afmeting toevoegen of metrisch en de diensten van de Customer Journey Analytics zoals [!UICONTROL Experimentation] paneel kan deze etiketten voor hun doeleinden gebruiken. Er worden twee vooraf gedefinieerde labels gebruikt voor het deelvenster Experimentatie:

* [!UICONTROL Experimentation Experiment]
* [!UICONTROL Experimentation Variant]

Kies in de gegevensweergave die experimentatiegegevens bevat twee dimensies, één met de experimentatiegegevens en één met de variantgegevens. Vervolgens geeft u die afmetingen het label **[!UICONTROL Experimentation Experiment]** en **[!UICONTROL Experimentation Variant]** .

![ de etiketopties van de context voor Experimentatie en Variant van de Experimentatie.](assets/context-label.png)

Zonder deze labels werkt het deelvenster Experimenteren niet, omdat er geen experimenten zijn om mee te werken.

## Gebruiken

Een deelvenster **[!UICONTROL Experimentation]** gebruiken:

1. Maak een deelvenster **[!UICONTROL Experimentation]** . Voor informatie over hoe te om een paneel tot stand te brengen, zie [ een paneel ](panels.md#create-a-panel) creëren.


1. Specificeer de [ input ](#panel-input) voor het paneel.

1. Neem de [ output ](#panel-output) voor het paneel waar.

   >[!IMPORTANT]
   >
   >Als de vereiste instellingen in de gegevensweergaven van de Customer Journey Analytics niet zijn voltooid, ontvangt u dit bericht voordat u verdergaat: [!UICONTROL Please configure the experiment and variant dimensions in Data views] .
   >

### Deelvensterinvoer

Het deelvenster Experimentatie gebruiken:

1. Configureer de instellingen voor deelvensterinvoer:

   ![ het paneel van de Experimentatie sleepte in een project.](assets/experiment-input.png)

   | Instelling | Definitie |
   | --- | --- |
   | **[!UICONTROL Date Range]** | Het datumbereik voor het deelvenster Experimentatie wordt automatisch ingesteld op basis van de eerste gebeurtenis die in Customer Journey Analytics is ontvangen voor het geselecteerde experiment. Indien nodig kunt u het datumbereik beperken of uitbreiden tot een specifieker tijdsbestek. |
   | **[!UICONTROL Experiment]** | Een reeks variaties op een ervaring die aan eindgebruikers werden blootgesteld om te bepalen welke het beste is om in onbeperkte tijd te houden. Een experiment bestaat uit twee of meer varianten, waarvan er één als de besturingsvariant wordt beschouwd. Deze instelling wordt vooraf gevuld met de afmetingen die in de gegevensweergave zijn gelabeld met het label **[!UICONTROL Experiment]** en de waarde van de experimentele gegevens voor de laatste drie maanden. |
   | **[!UICONTROL Control variant]** | Een van twee of meer wijzigingen in de ervaring van een eindgebruiker die worden vergeleken om het betere alternatief te identificeren. Eén variant moet als controlevariant worden gekozen en slechts één variant kan als controlevariant worden beschouwd. Deze instelling is vooraf gevuld met de afmetingen die in de gegevensweergaven zijn gelabeld met het label **[!UICONTROL Variant]** . Deze instelling geeft de variantgegevens weer die bij dit experiment horen. |
   | **[!UICONTROL Success metrics]** ➊ | De metrische of metrische waarde waarmee een gebruiker varianten vergelijkt. De variant met het meest wenselijke resultaat voor metrische omzetting (of het hoogste of het laagste) wordt verklaard de *best presterende variant* van een experiment. U kunt maximaal vijf metriek toevoegen. |
   | **[!UICONTROL Normalizing metric]** ➋ | De basis ([!UICONTROL People], [!UICONTROL Sessions], of [!UICONTROL Events]) waarop een test wordt uitgevoerd. Een test kan bijvoorbeeld de conversiesnelheden van verschillende variaties vergelijken waarbij **[!UICONTROL Conversion rate]** wordt berekend als Paginaweergave |
   | **[!UICONTROL Include confidence upper/lower bounds]** | Schakel deze optie in om boven- en ondergrenzen voor betrouwbaarheidsniveaus weer te geven. |


1. Selecteer **[!UICONTROL Build]** .

### Deelvensteruitvoer

Het deelvenster Experimentatie bevat een uitgebreide set gegevens en visualisaties waarmee u beter kunt begrijpen hoe uw experimenten werken. Bij de bovenkant van het paneel, ](../visualizations/summary-number-change.md) worden de summiere veranderingen van 0} {verstrekt om u aan de paneelmontages te herinneren u selecteerde. [ U kunt het deelvenster op elk gewenst moment bewerken door het bewerkingspotlood rechtsboven te selecteren.

U krijgt ook een tekstsamenvatting die aangeeft of het experiment al dan niet overtuigend is en die het resultaat samenvat. De conclusie is gebaseerd op statistische betekenis (zie [ Statistische methodologie ](#adobes-statistical-methodology).) U kunt samenvattingsaantallen voor de best presterende variant met de hoogste lift en het vertrouwen zien.

Voor elk metrisch succes selecteerde u, wordt de lijst van de a [ vrije vorm ](../visualizations/freeform-table/freeform-table.md) visualisatie en een tarief van de omzettings [ lijn ](../visualizations/line.md) visualisatie getoond.

![ de output van de Experimentatie die één vrije lijst en één trend van de omzettingssnelheid tonen.](assets/experiment-output.png)


>[!NOTE]
>
>Dit panel ondersteunt momenteel geen analyse van A/A-tests.

#### De resultaten interpreteren

1. **Experiment is overtuigend**: Telkens als u het experimentatierapport bekijkt, worden de gegevens die in het experiment tot dit punt zijn geaccumuleerd geanalyseerd. De analyse verklaart een experiment om overtuigend te zijn wanneer *op om het even welk ogenblik* geldig vertrouwen een drempel van 95% voor *minstens één* van de varianten kruist. Met meer dan twee armen wordt een Benjamini-Hochberg-correctie toegepast om meervoudige hypothesetests te corrigeren.

2. **best presterende variant**: Wanneer een experiment wordt verklaard om overtuigend te zijn, wordt de variant met de hoogste omzettingspercentage geëtiketteerd als best presterende variant. Merk op dat deze variant of de controle of basislijnvariant moet zijn, of één van de varianten die de 95% *op elk ogenblik* geldige betrouwbaarheidsdrempel (met toegepaste correcties Benjamini-Hochberg) kruisen.

3. **het tarief van de Omzetting**: De omzettingspercentage dat wordt getoond is een verhouding van de succes metrische waarde ➊ aan het normaliseren metrische ➋. Merk op dat deze waarde groter kan zijn dan 1, als metrisch niet binair is (1 of 0 voor elke eenheid in het experiment)

4. **Lift**: De samenvatting van het Experimentenrapport toont het Lift over Basislijn, die een maatregel van de percentageverbetering in de omzettingssnelheid van een bepaalde variant over de basislijn is. Dit is het verschil in prestaties tussen een bepaalde variant en de basislijn, gedeeld door de prestaties van de basislijn, uitgedrukt als een percentage.

5. **Vertrouwen**: Het wanneer geldig vertrouwen dat wordt getoond is een probabilistische maatregel van hoeveel bewijs er is dat een bepaalde variant het zelfde als de controlevariant is. Een hoger vertrouwen geeft minder bewijs voor de aanname dat de besturingsvariant en de niet-besturingsvariant dezelfde prestaties leveren. Het vertrouwen is een waarschijnlijkheid (uitgedrukt als percentage) dat u een kleiner verschil in omrekeningskoersen tussen een bepaalde variant en het besturingselement zou hebben waargenomen. In werkelijkheid is er geen verschil in de werkelijke onderliggende omrekeningskoersen. In termen van *p* - waarden, is het getoonde vertrouwen 1 - *p* - waarde.

>[!NOTE]
>
>Bij een volledige beschrijving van de resultaten moet rekening worden gehouden met alle beschikbare gegevens (bijvoorbeeld het ontwerp van het experiment, de steekproefgrootten, de omrekeningskoersen, het vertrouwen, enzovoort) en niet alleen met de verklaring van overtuigend of niet. Zelfs wanneer een resultaat nog niet overtuigend is, kan er nog steeds overtuigend bewijs zijn dat een bepaalde variant anders is dan een andere (betrouwbaarheidsintervallen zijn bijvoorbeeld bijna niet-overlapt). Idealiter zouden alle statistische gegevens, die op een continu spectrum worden geïnterpreteerd, de besluitvorming moeten beïnvloeden.

## Statistische methodologie van de Adobe {#statistics}

Om gemakkelijk te interpreteren en veilige statistische gevolgtrekking te verstrekken, heeft de Adobe een statistische methodologie goedgekeurd die op [ wordt gebaseerd altijd Geldige Reeksen van het Vertrouwen ](https://arxiv.org/abs/2103.06476).

Een vertrouwensopeenvolging is a *opeenvolgend* analoog van een betrouwbaarheidsinterval. Om te begrijpen wat een vertrouwensvolgorde is, stel je voor dat je je experimenten honderd keer herhaalt. En bereken een schatting van gemiddelde zaken metrisch (bijvoorbeeld het open tarief van een e-mail) en zijn bijbehorende 95%-vertrouwen opeenvolging voor *elke nieuwe gebruiker* die het experiment ingaat.

Een 95% betrouwbaarheidsreeks omvat de &quot;ware&quot;waarde van zaken metrisch in 95 van de 100 experimenten die u in werking stelde. (Een betrouwbaarheidsinterval van 95% kon slechts eenmaal per experiment worden berekend om dezelfde 95% dekkingsgarantie te geven, niet bij elke nieuwe gebruiker). Met vertrouwensreeksen kunt u dus voortdurend experimenten volgen zonder dat het aantal fout-positieve fouten toeneemt, dat wil zeggen dat het gebruik van &quot;peeking&quot; bij resultaten is toegestaan.

## Niet-gerandomiseerde afmetingen interpreteren {#non-randomized}

Met Customer Journey Analytics kunnen analisten elke gewenste dimensie kiezen. Maar hoe interpreteer je een analyse waarbij de als experiment gekozen dimensie niet een is waarvoor mensen willekeurig worden gekozen?

Neem bijvoorbeeld een advertentie die een persoon ziet. U kunt in het meten van de verandering in wat metrisch (bijvoorbeeld, gemiddelde opbrengst) geinteresseerd zijn als u besluit om personen *en B* in plaats van *en A* te tonen. Het causale effect van het tonen van advertentie B in plaats van advertentie A is van cruciaal belang voor het nemen van een besluit over het in de handel brengen. Dit causale effect kan worden gemeten als de gemiddelde opbrengst over de gehele bevolking, als u de status-quo van het tonen van advertentie A vervangt door de alternatieve strategie van het tonen van advertentie B.

A/B-tests zijn de gouden standaard in de industrie voor het objectief meten van de effecten van dergelijke interventies. De kritieke reden waarom een A/B-test aanleiding geeft tot een causale schatting is te wijten aan de randomisatie van personen die een van de mogelijke varianten ontvangen.

Kijk nu eens naar een dimensie die niet bereikt wordt door randomisatie, bijvoorbeeld, de staat van de persoon in de VS. Personen komen voornamelijk uit twee staten, New York en Californië. De gemiddelde omzet van de verkoop van een winterkledingmerk kan in beide staten verschillen als gevolg van de verschillen in het regionale weer. In een dergelijke situatie kan het weer de werkelijke oorzaak zijn van de verkoop van winterkleding, en niet het feit dat de geografische situatie van personen verschillend is.

Met het deelvenster voor experimenten in de Customer Journey Analytics kunt u gegevens analyseren als het gemiddelde inkomstenverschil per land van de persoon. In een dergelijke situatie heeft de output geen causale interpretatie. Een dergelijke analyse kan echter nog steeds van belang zijn. Het geeft een schatting (samen met maatstaven voor onzekerheid) van het verschil in gemiddelde inkomsten van de staten van de personen.  Deze waarde wordt ook bedoeld als *Statistische het Testen van de Samenvatting*. Het resultaat van deze analyse kan interessant zijn, maar niet noodzakelijkerwijs uitvoerbaar. Eenvoudig omdat u niet willekeurig hebt gekozen en soms geen personen aan één van de mogelijke waarden van de dimensie kunt willekeurig plaatsen.

In de volgende afbeelding worden deze situaties gecontrasteerd:

![ Diagram van A die de Gegevens van de Waarneming en het Gerandomiseerde Experiment tonen.](assets/randomize.png)

Wanneer u het effect van interventie X op resultaat Y wilt meten, is het mogelijk dat de werkelijke oorzaak van beide factoren de verwarrende factor C is. Als de gegevens niet worden bereikt door personen op X te randomiseren, is de impact moeilijker te meten en de analyse verklaart uitdrukkelijk voor C. Randomization breekt de afhankelijkheid van X op C, die ons toestaat om het effect van X op Y te meten zonder het moeten zich over andere variabelen ongerust maken.

## Berekende meetwaarden gebruiken in experimenten {#use-in-experimentation}

>[!NOTE]
>
>Voor organisaties die zowel Customer Journey Analytics als Adobe Journey Optimizer gebruiken, is de informatie in deze sectie ook op experimenteringseigenschappen binnen Journey Optimizer van toepassing.

Niet alle berekende meetgegevens zijn compatibel met het deelvenster Experimentatie.

Berekende meetgegevens met een van de volgende meetwaarden of constanten zijn niet compatibel met het deelvenster Experimentatie:

* De metriek van de basis van a [ summiere dataset ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/summary-data)
* De metriek van de basis die door elkaar worden verdeeld of samen worden vermenigvuldigd (bijvoorbeeld, `Revenue`/ `Orders`)
* Constanten die worden toegevoegd aan of afgetrokken van een metrische basis (bijvoorbeeld `Revenue+50`)
* Een of meer van de volgende basismeetwaarden:
   * Mensen

De berekende metriek die niet compatibel met het paneel van de Experimentatie zijn hebben de waarde [!UICONTROL **overal in Customer Journey Analytics (exclusief experimenteren)**] op het [!UICONTROL **de verenigbaarheid van het Product**] gebied wanneer het creëren van berekende metrisch. Voor informatie over het creëren van berekende metrisch, zie [ metriek ](/help/components/calc-metrics/cm-workflow/cm-build-metrics.md) bouwen.

## Berekende meetwaarden gebruiken in het deelvenster Experimentatie

Verwijs naar deze blogpost voor informatie over [ gebruikend berekende metriek in het paneel van de Experimentatie ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/using-derived-metrics-in-cja-s-experimentation-panel/ba-p/593119).

>[!MORELIKETHIS]
>[ het Beheersen van de Experimentatie van Adobe Customer Journey Analytics ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-blogs/mastering-adobe-customer-journey-analytics-experimentation-your/ba-p/732338)
>
