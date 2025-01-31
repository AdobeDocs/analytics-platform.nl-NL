---
description: Opeenvolgende filters zijn filters die de operator THEN gebruiken om de volgorde van filtervoorwaarden te definiëren.
title: Opeenvolgende filters
feature: Filters
exl-id: 64cb10b5-36f0-42c8-b687-ae5de5ced8b5
source-git-commit: 4bf8c616965718426efe880865acb0e5054b6a31
workflow-type: tm+mt
source-wordcount: '2343'
ht-degree: 1%

---

# Opeenvolgende filters

U maakt opeenvolgende filters met de logische operator [!UICONTROL Then] tussen componenten, containers en componenten of containers. De logische operator [!UICONTROL Then] impliceert dat een filtervoorwaarde optreedt, gevolgd door een andere.



>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Opeenvolgende segmentatie ](https://video.tv.adobe.com/v/25405/?quality=12&learn=on){target="_blank"} voor een demo video.

{{videoaa}}

>[!ENDSHADEBOX]

Een opeenvolgend filter heeft sommige [ basisfunctionaliteit ](#basics) en extra opties die u kunt vormen om meer ingewikkeldheid aan de opeenvolgende filter toe te voegen:

![ Opeenvolgende filter ](assets/sequential-filter.gif)

* [ na en binnen ](#after-and-within) beperkingen voor toen logica in de definitie van de opeenvolgingsfilter:

* Welke gegevens aan [ omvatten ](#include) als deel van de algemene opeenvolging voor de filterdefinitie. Of voor een reeks die is gedefinieerd als onderdeel van een container. Standaard wordt rekening gehouden met alle overeenkomende gegevens. Dat gegeven wordt geïdentificeerd door ![ UserGroup ](/help/assets/icons/UserGroup.svg) [!UICONTROL Include Everyone].

   * Selecteer ![ SequenceBefore ](/help/assets/icons/SequenceBefore.svg) **[!UICONTROL Only Before Sequence]** om slechts gegevens vóór de opeenvolging te overwegen.
   * Selecteer ![ SequenceAfter ](/help/assets/icons/SequenceAfter.svg) **[!UICONTROL Only After Sequence]** om slechts gegevens na de opeenvolging te overwegen.

* Welke gegevens aan [ uitsluiten ](#exclude) als deel van de opeenvolgende filterdefinitie.

* Hoe te [ logisch gezien groeperen ](#logic-group) voorwaarden in uw opeenvolgende filterdefinitie.

## Basisbeginselen



De grondbeginselen van de bouw van een opeenvolgende filter zijn niet verschillend dan de bouw van een regelmatige filter gebruikend de [ bouwer van de Filter ](filter-builder.md). U kunt de [ bouwer van de Definitie ](filter-builder.md#definition-builder) gebruiken om uw filterdefinitie te construeren. In die constructie, gebruikt u componenten, containers, exploitanten en logica. Een regelmatige filter wordt automatisch een opeenvolgend filter zodra u de **[!UICONTROL Then]** exploitant in de belangrijkste definitie of in om het even welke containers selecteert u binnen de [ Bouwer van de Definitie ](filter-builder.md#definition-builder) gebruikt.

### Voorbeelden

In de onderstaande voorbeelden ziet u hoe u sequentiële filters in verschillende gebruikscategorieën gebruikt.

#### Eenvoudige reeks

Identificeer personen die een pagina hebben bekeken en vervolgens een andere pagina hebben bekeken. De gegevens op gebeurtenisniveau worden gefilterd met deze reeks. Ongeacht eerdere sessies of sessies van voorbije, vorige of tijdelijke personen, of de tijd of het aantal paginaweergaven die zich tussen de sessies voordoen.

![ Opeenvolgende filter omvat iedereen ](assets/sequence-include-everyone.png)

#### Volgorde voor sessies

Identificeer personen die een pagina in een sessie hebben bekeken en bekijk vervolgens een andere pagina in een andere sessie. Om tussen zittingen te onderscheiden, gebruik containers om de opeenvolging te bouwen en ![ te bepalen Bezoek ](/help/assets/icons/Visit.svg) **[!UICONTROL Session]** niveau voor elke container.

![ filter van de Opeenvolging over zittingen ](assets/sequence-filter-session.png)

#### Volgorde op gemengde niveaus

Identificeer personen die twee pagina&#39;s voor een onbepaald aantal sessies weergeven en bekijk vervolgens een derde pagina in een aparte sessie. Opnieuw, gebruiks containers om de opeenvolging te bouwen en ![ Bezoek ](/help/assets/icons/Visit.svg) **[!UICONTROL Session]** niveau op de container te bepalen die de afzonderlijke zitting bepaalt.

![ filter van de Opeenvolging met afzonderlijke definitieve zitting ](assets/sequence-filter-final-session.png)

#### Samengevoegde reeks

Identificeer personen die tijdens hun eerste sessie een specifieke pagina bezochten en later een aantal andere pagina&#39;s bezochten. Om tussen de opeenvolging van gebeurtenissen te onderscheiden, gebruikcontainers om de logica op a ![ WebPage ](/help/assets/icons/WebPage.svg) te scheiden **[!UICONTROL Session]** containerniveau.

![ de gezamenlijke containers van de Zitting ](assets/session-aggregate-containers.png)


#### Een reeks nesten

Identificeer alle zittingen waar een persoon één pagina vóór een andere pagina bezoekt en dan follow-up zittingen heeft die twee andere pagina&#39;s impliceren. U kunt bijvoorbeeld alle sessies identificeren waarbij een persoon eerst de startpagina bezoekt, vervolgens een pagina van categorie 1 en vervolgens andere sessies heeft waarin in elke sessie de pagina van categorie 2 en 3 wordt bezocht.

![ Geneste opeenvolging ](assets/sequence-nested.png)

## [!UICONTROL After] en [!UICONTROL Within]

U kunt ](/help/assets/icons/Clock.svg) Klok **[!UICONTROL After]** en ![ Klok ](/help/assets/icons/Clock.svg) gebruiken **[!UICONTROL Within]** de **[!UICONTROL Then]** exploitant om extra [ tijdbeperkingen ](#time-constraints) of [ beperkingen voor Gebeurtenissen, Zittingen of Dimensionen ](#event-session-and-dimension-constraints) te bepalen.![

### Tijdbeperkingen

Tijdsbeperkingen toepassen op de operator **[!UICONTROL Then]** :

1. Selecteer ![ Klok ](/help/assets/icons/Clock.svg).
1. Selecteer **[!UICONTROL Within]** of **[!UICONTROL After]** in het contextmenu.
1. Geef een tijdsperiode op (**[!UICONTROL Minute]**, **[!UICONTROL Hour]** tot **[!UICONTROL Years]** ).
1. Selecteer ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) **[!UICONTROL *aantal *]**om popup te openen die u toestaat om binnen te typen of een aantal te specificeren gebruikend **[!UICONTROL -]**of **[!UICONTROL +]**.

Om een tijdbeperking te verwijderen, gebruik ![ CrossSize75 ](/help/assets/icons/CrossSize75.svg).

In de onderstaande tabel worden de tijdbeperkingsoperatoren gedetailleerder uitgelegd.

| Operatoren | Beschrijving |
|--- |--- |
| **[!UICONTROL After]** | De operator [!UICONTROL After] wordt gebruikt om een minimumlimiet op te geven voor de tijd tussen twee controlepunten. Wanneer u de waarden Na instelt, begint de tijdlimiet wanneer het filter wordt toegepast. Als de operator [!UICONTROL After] bijvoorbeeld op een container is ingesteld om personen te identificeren die pagina A bezoeken, maar pas na één dag naar pagina B terugkeren, begint die dag wanneer de bezoeker pagina A verlaat.  De bezoeker die in het filter moet worden opgenomen, moet na het verlaten van pagina A ten minste 1440 minuten (één dag) overbrengen om pagina B te kunnen bekijken. |
| **[!UICONTROL Within]** | De operator [!UICONTROL Within] wordt gebruikt om een maximumlimiet op te geven voor de hoeveelheid tijd tussen twee controlepunten. Als de operator [!UICONTROL Within] bijvoorbeeld op een container is ingesteld om personen te identificeren die pagina A bezoeken en vervolgens binnen één dag naar pagina B terugkeren, begint die dag wanneer de persoon pagina A verlaat. Om in het filter te worden opgenomen, heeft de persoon een maximumtijd van één dag alvorens pagina B te openen. De persoon die in het filter moet worden opgenomen, moet pagina B openen binnen maximaal 1440 minuten (één dag) nadat hij pagina A heeft verlaten om pagina B te bekijken. |
| **[!UICONTROL After but Within]** | Wanneer u zowel de operatoren [!UICONTROL After] als [!UICONTROL Within] gebruikt, beginnen en eindigen beide operatoren parallel, niet opeenvolgend. <br/> bijvoorbeeld, bouwt u een filter met de container die aan wordt geplaatst: `After = 1 Week(s) and Within = 2 Week(s)`.<br/> de voorwaarden om bezoekers in dit filter te identificeren worden voldaan slechts tussen één en twee weken. Beide voorwaarden worden afgedwongen vanaf het moment van de eerste paginaweergave. |


#### Voorbeelden

Enkele voorbeelden van het gebruik van de tijdbeperkingen.

##### [!UICONTROL After] operator

Identificeer personen die slechts na twee weken een pagina en vervolgens een andere pagina hebben bezocht. Bijvoorbeeld personen die de startpagina hebben bezocht, maar de vrouwen | Hiermee wordt de pagina pas na twee weken weergegeven.

![ Opeenvolging na ](assets/sequence-after.png)

Als er op 1 juni 2024 om 00:01 een paginaweergave voor Home plaatsvindt, wordt de pagina Vrouwen weergegeven | De tonen komen overeen zolang de paginaweergave plaatsvindt na 15 juni 2024 00:01.

##### [!UICONTROL Within] operator

Identificeer personen die een pagina en een andere pagina binnen vijf minuten hebben bezocht. Bijvoorbeeld personen die de startpagina hebben bezocht en vervolgens de vrouwen | Hiermee wordt de pagina binnen 5 minuten weergegeven.

![ Opeenvolging binnen ](assets/sequence-within.png)

Als op 1 juni 2024 om 12:01 een paginaweergave voor Home plaatsvindt, wordt een paginaweergave voor Vrouwen weergegeven | De tonen komen overeen zolang de paginaweergave plaatsvindt vóór 15 juni 2024 12:16.

##### [!UICONTROL After] but [!UICONTROL Within] operator

Identificeer personen die een pagina bezochten en vervolgens een andere pagina bezochten na twee weken, maar binnen één maand. Bijvoorbeeld personen die de startpagina hebben bezocht en vervolgens na twee weken en binnen een maand de Vrouwen | Shoes page.

![ Opeenvolging na maar binnen ](assets/sequence-afterbutwithin.png)

Personen die op 1 juni 2024 op de startpagina komen en die terugkeren naar de Vrouwen | Shoes page na 15 juni 2019 00:01, maar vóór 1 juli 2019 komt in aanmerking voor het segment.


### [!UICONTROL Event] -, [!UICONTROL Session] - en [!UICONTROL Dimension] -beperkingen

De ![ Klok ](/help/assets/icons/Clock.svg) **[!UICONTROL After]** en ![ Klok ](/help/assets/icons/Clock.svg) **[!UICONTROL Within]** beperkingen staan u niet alleen toe om een tijdbeperking maar ook een gebeurtenis, een zitting of een afmetingsbeperking te specificeren. Selecteer **[!UICONTROL Event(s)]**, **[!UICONTROL Session(s)]** of **[!UICONTROL Other dimensions]** ![ ChevronRight ](/help/assets/icons/ChevronRight.svg) **[!UICONTROL *naam van het Dimension *]**. U kunt het [!UICONTROL *gebied van het Onderzoek*] aan onderzoek naar een afmeting gebruiken.

#### Voorbeeld

Hieronder ziet u een voorbeeld van een sequentieel filter dat zoekt naar personen die een productcategoriepagina hebben bezocht (Vrouwen) | Shoes), gevolgd door een afrekenpagina (Afhandeling | Bedankt) op één pagina.

![ filter van de Opeenvolging binnen ](assets/sequence-filter-within.png)

De volgende voorbeeldreeksen komen overeen of komen niet overeen:

| Reeks | ![ AppleReject ](/help/assets/icons/ApproveReject.svg) |
|--- | :---: |
| Pagina `Women \| Shoes` gevolgd door pagina `Checkout \| Thank You` | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) |
| Pagina `Women \| Shoes` gevolgd door pagina `Women \| Tops` gevolgd door pagina `Checkout \| Thank You` | ![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) |

## [!UICONTROL Include]

U kunt opgeven welke gegevens u wilt opnemen in het opeenvolgende filter of in een opeenvolgende container die deel uitmaakt van het opeenvolgende filter.

### [!UICONTROL Everyone] {#include_everyone}

Om een opeenvolgend filter tot stand te brengen dat iedereen omvat, selecteer de optie ![ UserGroup ](/help/assets/icons/UserGroup.svg) **[!UICONTROL Include Everyone]**.

Het opeenvolgende filter identificeert gegevens die overeenkomen met het opgegeven patroon als geheel.  Hieronder ziet u een voorbeeld van een filter met een standaardsequentie waarmee u zoekt naar personen die een pagina met productcategorieën hebben bezocht (Vrouwen) | Shoes), gevolgd door een afrekenpagina (Afhandeling | Dank u.). De filter wordt geplaatst aan ![ UserGroup ](/help/assets/icons/UserGroup.svg) **[!UICONTROL Include Everyone]**.

![ Opeenvolgende filter omvat iedereen ](assets/sequence-include-everyone.png)

De volgende voorbeeldreeksen komen overeen of komen niet overeen:

| | Reeks | ![ AppleReject ](/help/assets/icons/ApproveReject.svg) |
|---:|--- | --- |
| 1 | `Women \| Shoes` dan `Checkout \| Thank You` in dezelfde sessie | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) |
| 2 | `Women \| Shoes` then `Men \| Shoes` then `Checkout \| Thank You` (voor verschillende sessies) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) |
| 3 | `Checkout \| Thank You` then `Women \| Shoes` | ![ RemoveCircle ](/help/assets/icons/RemoveCircle.svg) |

### [!UICONTROL Only Before Sequence] en [!UICONTROL Only After Sequence]

De opties ![ SequenceBefore ](/help/assets/icons/SequenceBefore.svg) **[!UICONTROL Only Before Sequence]** en ![ SequenceAfter ](/help/assets/icons/SequenceAfter.svg) **[!UICONTROL Only After Sequence]** filter de gegevens aan een ondergroep vóór of na de gespecificeerde opeenvolging.

* ![ SequenceBefore ](/help/assets/icons/SequenceBefore.svg) **slechts vóór Opeenvolging**: Omvat alle gegevens vóór een opeenvolging en de eerste gegevens van de opeenvolging zelf. Als een reeks meerdere keren als onderdeel van de gegevens wordt weergegeven, bevat [!UICONTROL Only Before Sequence] de eerste hit van de laatste instantie van de reeks en alle vorige treffers.
* ![ SequenceAfter ](/help/assets/icons/SequenceAfter.svg) **slechts na Reeks**: Omvat alle klappen na een opeenvolging en de laatste gegevens van de opeenvolging zelf. Als een reeks meerdere keren als onderdeel van de gegevens wordt weergegeven, bevat [!UICONTROL Only After Sequence] de laatste hit van de eerste instantie van de reeks en alle volgende treffers.

Overweeg een definitie die een opeenvolging van een component met criteria specificeert die door B worden geïdentificeerd, (toen) door een component met criteria wordt gevolgd die door D worden geïdentificeerd. De drie opties zouden gegevens als volgt identificeren:


| B Vervolgens D | A | B | C | D | E | F |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| Inclusief iedereen | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) |
| Alleen voor reeks | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) |  |  |  |  |
| Alleen na reeks |  |  |  | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) |



| B Dan D (komt meerdere keren voor) | A | B | C | D | B | C | D | E |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Inclusief iedereen | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) |
| Alleen voor reeks | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) |  |  |  |
| Alleen na reeks |  |  |  | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) | ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) |

#### Voorbeeld

U hebt drie versies van een sequentieel filter voor sitesecties gedefinieerd. Één met de optie ![ UserGroup ](/help/assets/icons/UserGroup.svg) **[!UICONTROL Include Everyone]**, met de optie ![ SequenceBefore ](/help/assets/icons/SequenceBefore.svg) **[!UICONTROL Only Before Sequence]**, en met de optie ![ SequenceAfter ](/help/assets/icons/SequenceAfter.svg) **[!UICONTROL Only After Sequence]**. U noemde de drie filters dienovereenkomstig.

![ de filter van de Opeenvolging ](assets/site-section-filters.png)

Wanneer het melden van plaatssecties die deze drie filters gebruiken, kijkt de voorbeeldoutput in een vrije vormlijst als:

![ Opeenvolgend filterrapport ](assets/sequential-filter-freeform-table.png)

## [!UICONTROL Exclude]

De definities van de filter omvatten alle gegevens tenzij u specifiek ![ Gebruiker ](/help/assets/icons/User.svg) [!UICONTROL Person] uitsluiten, ![ Bezoek ](/help/assets/icons/Visit.svg) [!UICONTROL Session], of ![ WebPage ](/help/assets/icons/WebPage.svg) [!UICONTROL Event] gegevens gebruikend **[!UICONTROL Exclude]**.

Met [!UICONTROL Exclude] kunt u algemene gegevens negeren en filters met meer focus maken. Met Uitsluiten kunt u ook filters maken die bepaalde groepen personen uitsluiten. Bijvoorbeeld, om een filter te bepalen dat personen specificeert die orden plaatste en dan die groep personen uitsluiten om *niet-kopers* te identificeren. De beste manier is om regels te maken die een brede definitie gebruiken in plaats van [!UICONTROL Exclude] te gebruiken om specifieke personen die overeenkomen met specifieke include-waarden, als doel in te stellen.

Voorbeeld van uitsluitingsdefinities zijn:

* **sluit pagina&#39;s** uit. Gebruik een filterdefinitie om een specifieke pagina (zoals *Pagina van het Huis*) van een rapport uit te schrappen, tot een regel van de Gebeurtenis te leiden waar de pagina `Home Page` evenaart, en dan de regel uit te sluiten. Deze definitie omvat automatisch alle pagina&#39;s behalve de *Pagina van het Huis*.
* **sluit verwijzende domeinen** uit. Gebruik een definitie die alleen verwijzende domeinen van Google.com omvat en alle andere uitsluitt.
* **identificeer niet-kopers**. Identificeer wanneer orden groter dan nul zijn en sluit dan [!UICONTROL Person] uit.

[!UICONTROL Exclude] kan worden gebruikt om een opeenvolging te identificeren waar de personen geen deel van specifieke zittingen uitmaken of specifieke gebeurtenissen uitvoeren. [!UICONTROL Exclude] kan ook worden opgenomen in een [!UICONTROL Logic Group] (zie hieronder).

U kunt containers uitsluiten, geen componenten.

### Voorbeelden

Zie hieronder voor voorbeelden van het gebruik van [!UICONTROL Exclude] .

#### [!UICONTROL Exclude] within

Identificeer personen die een pagina hebben bezocht, geen andere pagina hebben bezocht en vervolgens weer een andere pagina hebben bezocht. U sluit de container uit gebruikend ![ Plaatsende ](/help/assets/icons/Setting.svg) [!UICONTROL Exclude]. Een uitgesloten container wordt geïdentificeerd door een dunne rode balk aan de linkerkant.

![ sluit opeenvolging ](assets/sequence-exclude.png) uit


#### [!UICONTROL Exclude] bij begin

Identificeer personen die een pagina hebben bezocht zonder ooit naar een andere pagina te gaan. Mensen die een aankoop hebben uitgecheckt zonder ooit de homepage te hebben bezocht, bijvoorbeeld.

![ Reeks sluit begin ](assets/sequence-exclude-start.png) uit


#### [!UICONTROL Exclude] aan einde

Identificeer personen die één pagina hebben bezocht maar nooit andere pagina&#39;s hebben bezocht. Bijvoorbeeld personen die uw homepage hebben bezocht, maar nooit een van uw afhandelingspagina&#39;s.

![ Sequentie sluit eind ](assets/sequence-exclude-end.png) uit


## [!UICONTROL Logic Group]

>[!NOTE]
>
>Een [!UICONTROL Logic Group] kan alleen worden gedefinieerd in een opeenvolgend filter, wat betekent dat de operator [!UICONTROL Then] wordt gebruikt in de container.

Met de Logic Group kunt u voorwaarden groeperen in één controlepunt voor opeenvolgende filters. Als onderdeel van de reeks wordt de logica die is gedefinieerd in de container die is geïdentificeerd als Logic Group, geëvalueerd na een voorafgaand controlepunt en vóór een volgend volgend controlepunt.

Aan de voorwaarden binnen de Logische Groep zelf kan in om het even welke orde worden voldaan. Niet-opeenvolgende containers (gebeurtenis, sessie, persoon) vereisen daarentegen niet dat aan de voorwaarden ervan wordt voldaan binnen de gehele reeks, wat mogelijk niet-intuïtieve resultaten oplevert bij gebruik met een Dan-operator.

[!UICONTROL Logic Group] werd ontworpen om *verscheidene voorwaarden als groep te behandelen, zonder enige het opdracht geven tot* onder de gegroepeerde voorwaarden. Anders gezegd, is de volgorde van de voorwaarden binnen een logische groep irrelevant.

U kunt Logica Group het beste gebruiken:

* Opeenvolgende controlepunten groeperen.
* De constructie van opeenvolgende filters vereenvoudigen.

### Voorbeelden

Hier volgen voorbeelden van het gebruik van de container van de Logische Groep.

#### Elke bestelling

Identificeer personen die een pagina hebben bezocht en bekijk elke pagina in een willekeurige volgorde uit een andere set pagina&#39;s. Bijvoorbeeld, bezochten de mensen die de Homepage bezochten, dan elk van de Mannen pagina, de pagina van Vrouwen, en de pagina van Kinderen, ongeacht de orde.

U kunt dit filter maken zonder een [!UICONTROL Logic Group] , maar de constructie zal complex en ingewikkeld zijn. Geef elke reeks pagina&#39;s op die de bezoeker kan bekijken. Voor duidelijkheid, slechts wordt de eerste container geopend ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) en de andere containers zijn gesloten ![ ChevronRight ](/help/assets/icons/ChevronRight.svg). U kunt de inhoud van de andere containers afleiden door de titels.

![ Voorbeeld dat geen logische groep ](assets/logicgroup-example-notusing.png) gebruikt

U kunt [!UICONTROL Logic Group] gebruiken om het samenstellen van dit filter te vereenvoudigen, zoals hieronder wordt getoond. Verzeker u ![ Groep ](/help/assets/icons/Group.svg) **[!UICONTROL Logic Group]** voor de container selecteert.

![ Voorbeeld dat geen logische groep ](assets/logicgroup-example-using.png) gebruikt

#### Eerste overeenkomst

Identificeer personen die een pagina of een andere pagina hebben bezocht en vervolgens weer een andere pagina hebben bezocht. Bijvoorbeeld personen die de pagina Vrouwen of de pagina Mannen hebben bezocht, bezochten de kassa | Bedankt, pagina.

![ Voorbeeld dat eerste gelijke met logische groep ](assets/logicgroup-example-firstmatch.png) gebruikt

#### [!UICONTROL Exclude] [!UICONTROL And]

Identificeer personen die een pagina bezochten toen uitdrukkelijk geen reeks andere pagina&#39;s bezochten, maar opnieuw een andere pagina bezocht. Bijvoorbeeld, de personen die de Homepage bezochten, bezochten niet de Mannen of de Vrouwen pagina, maar bezochten de Kinderen pagina.

![ Logische groep sluit uit en ](assets/logicgroup-exclude-and.png)

#### [!UICONTROL Exclude] [!UICONTROL Or]

Identificeer personen die een pagina bezochten toen uitdrukkelijk geen pagina van een reeks pagina&#39;s bezocht, maar opnieuw een andere pagina bezocht. Bijvoorbeeld, de personen die de Homepage bezochten, bezochten niet de Mannen en de Vrouwen pagina, maar bezochten de Kinderen pagina.

![ Logische groep sluit uit en ](assets/logicgroup-exclude-or.png)


<!--
An example of a complex sequential filter if you want to find the persons that 

| Session One | Session Two | Session Three |
| --- | --- | --- |
| The person went to the main landing page A, excluded the campaign page B, and then viewed the Product page C.| The person again went to the main landing page A, excluded the campaign page B, and went again to the Product page C, and then to a new page D. | The person entered and followed that same path as in the first and second visits, then excluded page F to go directly to a targeted product on page G. |
-->


## Een laatste voorbeeld

Als laatste voorbeeld, wilt u mensen identificeren die over een specifieke productpagina leerden, zonder deze personen ooit door uw Empower Your Move campagne werden geraakt. En tijdens hun eerste bezoek aan uw online winkel werd de startpagina bekeken, maar werd niet verder gekeken naar fitness (tandwielproducten) producten uit de categorie Men. In hun volgende sessie direct daarna gingen ze echter naar een productpagina en plaatsten ze een onlinebestelling zonder eerst de startpagina te doorlopen.


![ Complex opeenvolgend filtervoorbeeld ](assets/sequential-complex.png)
