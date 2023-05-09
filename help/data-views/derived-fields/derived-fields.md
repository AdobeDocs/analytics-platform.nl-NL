---
title: Afgeleide velden
description: Een afgeleid gebied specificeert rapport-tijd manipulatie van schemagebieden en/of standaardcomponenten door een reeks beschikbare functies en functiesjablonen.
solution: Customer Journey Analytics
feature: Data Views
hide: true
hidefromtoc: true
exl-id: 1ba38aa6-7db4-47f8-ad3b-c5678e5a5974
badgeDerivedFields: label="New Feature" type="Positive"
source-git-commit: cb63cd52a1618f2e1048f2779c4e6c0317e94f64
workflow-type: tm+mt
source-wordcount: '2914'
ht-degree: 3%

---


# Afgeleide velden

{{release-limited-testing}}

>[!NOTE]
>
>In afwachting van de definitieve updates, ziet u [!UICONTROL Custom field] in plaats van [!UICONTROL Derived field] in de gebruikersinterface.


Afgeleide velden zijn een belangrijk aspect van de functionaliteit voor real-time rapportage in Customer Journey Analytics (CJA). Een afgeleid gebied staat u toe om (vaak complexe) gegevensmanipulaties op de vlucht, door een klantgerichte regelbouwer te bepalen. Vervolgens kunt u dat afgeleide veld als een component (metrisch of dimensionaal) gebruiken in [Werkruimte](../../analysis-workspace/home.md) of zelfs het afgeleide veld nader te definiëren als een component in [Gegevens, weergave](../data-views.md).

Afgeleide velden kunnen veel tijd en moeite besparen, in vergelijking met het transformeren of manipuleren van gegevens op andere locaties buiten CJA. zoals [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html), [Data Distiller](https://experienceleague.adobe.com/docs/experience-platform/query/data-distiller/overview.html?lang=en)of binnen uw eigen ETL-processen (Extract Transform Load) / Extract Load Transform (ELT-processen).

Afgeleide velden worden gedefinieerd binnen [Gegevensweergaven](../data-views.md), zijn gebaseerd op een set functies die als regels worden gedefinieerd en worden toegepast op beschikbare standaard- en/of schemavelden.

Voorbeelden van gebruiksgevallen zijn:

- Definieer een afgeleid veld Paginanaam dat onjuiste waarden voor de verzamelde paginanamen corrigeert om de waarden voor de paginanaam te corrigeren.

- Definieer een afgeleid veld Marketingkanaal dat het juiste marketingkanaal bepaalt op basis van een of meer voorwaarden (bijvoorbeeld URL-parameter, pagina-URL, paginanaam).

## Afgeleide veldinterface

Wanneer u een afgeleid veld maakt of bewerkt, gebruikt u de afgeleide veldinterface.

![Dialoogvenster Afgeleid veld](assets/derived-field-dialog.png)


|  | Naam | Beschrijving |
|---------|----------|--------|
| 1 | **Kiezer** | U gebruikt het selectiegebied om uw ![Functie](assets/Smock_Function_18_N.svg) functie,![Pictogram voor functiesjabloon](assets/Smock_FileTemplate_18_N.svg) functiesjabloon,![Pictogram Schema-veld](assets/Smock_Folder_18_N.svg) schemaveld, of![Standaardveldpictogram](assets/Smock_DragHandle_18_N.svg)het standaardgebied op aan de regelbouwer. <br/>Gebruik de vervolgkeuzelijst om te selecteren tussen [!UICONTROL Functions], [!UICONTROL Function templates], [!UICONTROL Schema fields], en [!UICONTROL Standard fields].<br/>Met de opdracht ![Zoekpictogram](assets/Smock_Search_18_N.svg) Zoekvak. <br/>U kunt de lijst met geselecteerde objecten filteren door ![Filterpictogram](assets/Smock_Filter_18_N.svg) Filteren en filters opgeven in het dialoogvenster [!UICONTROL Filter fields by] . U kunt filters eenvoudig verwijderen met ![Pictogram Sluiten](assets/CrossSize75.svg) voor elk filter. |
| 2 | **Regelbouwer** | U bouwt uw afgeleid gebied opeenvolgend gebruikend één of meerdere regels. Een regel is een specifieke implementatie van een functie en wordt daarom altijd met slechts één functie geassocieerd. U maakt een regel door een functie naar de regelbouwer te slepen. Het functietype bepaalt de interface van de regel.<br/>Zie de [Regelinterface](#rule-interface) voor meer informatie . <br/>U kunt een functie bij het begin, het eind, of binnen tussen regels opnemen reeds beschikbaar in de regelbouwer. De laatste regel in de regelbouwer bepaalt de definitieve output van het afgeleide gebied. |
| 3 | **[!UICONTROL ** Veldinstellingen **]** | U kunt het afgeleide veld een naam geven en beschrijven en het veldtype controleren. |
| 4 | **[!UICONTROL ** Uiteindelijke uitvoer **]** | In dit gebied wordt ter plekke een bijgewerkte voorvertoning van uitvoerwaarden weergegeven, gebaseerd op gegevens in de afgelopen 30 dagen en de wijzigingen die u aanbrengt in het afgeleide veld in de regelbuilder. |

{style="table-layout:auto"}

## Veldsjabloonwizard

Wanneer u voor het eerst toegang krijgt tot de afgeleide veldinzet, [!UICONTROL Start with a field template] wordt weergegeven.

1. Selecteer de sjabloon die het beste het type veld beschrijft dat u wilt maken.
2. Selecteer **[!UICONTROL ** Selecteren **]** om door te gaan.

Het dialoogvenster met afgeleide velden wordt gevuld met regels (en functies) die vereist of handig zijn voor het type veld dat u hebt geselecteerd. Zie [Functiesjablonen](#function-templates) voor meer informatie over de beschikbare sjablonen.

## Regelinterface

Wanneer u een regel in de regelbouwer bepaalt, gebruikt u de regelinterface.

![Regelinterface](assets/rule-interface.png)

|  | Naam | Beschrijving |
|---------|----------|--------|
| A | **Naam van regel** | Standaard is de regelnaam **Regel X** (X verwijst naar een volgnummer). Als u de naam van een regel wilt bewerken, selecteert u de naam en typt u de nieuwe naam, bijvoorbeeld `Query Parameter`. |
| B | **Functienaam** | De geselecteerde functienaam voor de regel, bijvoorbeeld [!DNL URL PARSE]. Wanneer de functie de laatste in de reeks functies is en de uiteindelijke uitvoerwaarden bepaalt, wordt de functienaam gevolgd door [!DNL - FINAL OUTPUT]bijvoorbeeld [!DNL URL PARSE - FINAL OUTPUT]. <br/>Als u een pop-up met meer informatie over de functie wilt weergeven, selecteert u ![Help-pictogram](assets/Smock_HelpOutline_18_N.svg). |
| C | **Beschrijving van regel** | U kunt desgewenst een beschrijving aan een regel toevoegen.<br/>Selecteren ![Meer pictogram](assets/More.svg)selecteert u vervolgens **[!UICONTROL ** Beschrijving toevoegen **]** om een beschrijving toe te voegen of **[!UICONTROL ** Beschrijving bewerken **]** om een bestaande beschrijving te bewerken.<br/>Gebruik de editor om een beschrijving in te voeren. U kunt de werkbalk gebruiken om de tekst op te maken (met de stijlkiezer, vet, cursief, onderstrepen, rechts, links, gecentreerd, kleur, nummerlijst, opsommingslijst) en om koppelingen toe te voegen aan externe informatie. <br/>Klik buiten de editor om het bewerken van de beschrijving te voltooien. |
| D | **Functiegebied** | Definieert de logica van de functie. De interface is afhankelijk van het type functie. Zie [Functieverwijzing](#function-reference) voor gedetailleerde informatie over elk van de ondersteunde functies. |

{style="table-layout:auto"}

## Een afgeleid veld maken

1. Selecteer een bestaande gegevensweergave of maak een gegevensweergave. Zie [Gegevensweergaven](../data-views.md) voor meer informatie .

2. Selecteer **[!UICONTROL ** Componenten **]** van de weergave Gegevens.

3. Selecteren **[!UICONTROL ** Afafgeleid veld maken **]** van de linkerspoorstaaf.

4. Als u een afgeleid veld wilt definiëren, gebruikt u de [!UICONTROL Create derived field] interface. Zie [Afgeleide veldinterface](#derived-field-interface).

   Als u het nieuwe afgeleide veld wilt opslaan, selecteert u **[!UICONTROL ** Opslaan **]**.

5. Het nieuwe afgeleide veld wordt toegevoegd aan de [!UICONTROL Derived fields >] container, als onderdeel van **[!UICONTROL ** Schema-velden **]** in de linkertrack van de gegevensweergave.


## Een afgeleid veld bewerken

1. Selecteer een bestaande gegevensweergave. Zie [Gegevensweergaven](../data-views.md) voor meer informatie .

2. Selecteer **[!UICONTROL ** Componenten **]** van de weergave Gegevens.

3. Selecteren **[!UICONTROL ** Schema-velden **]** in de [!UICONTROL Connection] aan de linkerkant.

4. Selecteren **[!UICONTROL ** Afgeleide velden >**]** container.

5. Houd de cursor boven het afgeleide veld dat u wilt bewerken en selecteer ![Pictogram Bewerken](assets/Smock_Edit_18_N.svg).

6. Als u het afgeleide veld wilt bewerken, gebruikt u de opdracht [!UICONTROL Edit derived field] interface. Zie [Afgeleide veldinterface](#derived-field-interface).

   - Selecteren **[!UICONTROL ** Opslaan **]** om het bijgewerkte afgeleide veld op te slaan.

   - Selecteren **[!UICONTROL ** Annuleren **]** om wijzigingen die u hebt aangebracht in het afgeleide veld te annuleren.

   - Selecteren **[!UICONTROL ** Opslaan als **]** om het afgeleide gebied als nieuw afgeleid gebied te bewaren. Het nieuwe afgeleide veld heeft dezelfde naam als het oorspronkelijke bewerkte afgeleide veld met `(copy)` toegevoegd.

## Een afgeleid veld verwijderen

1. Selecteer een bestaande gegevensweergave. Zie [Gegevensweergaven](../data-views.md) voor meer informatie .

2. Selecteer **[!UICONTROL ** Componenten **]** van de weergave Gegevens.

3. Selecteren **[!UICONTROL ** Schema-velden **]** tab in [!UICONTROL Connection] venster.

4. Selecteren **[!UICONTROL ** Afgeleide velden >**]** container.

5. Houd de cursor boven het afgeleide veld dat u wilt verwijderen en selecteer ![Pictogram Bewerken](assets/Smock_Edit_18_N.svg).

6. In het gebruik **[!UICONTROL ** Afgeleid veld bewerken **]** -interface selecteert u Verwijderen.

   A [!UICONTROL Delete component] wordt u gevraagd de verwijdering te bevestigen. Overweeg om het even welke externe verwijzingen er aan het afgeleide gebied buiten de mening van Gegevens zouden kunnen bestaan.

   - Selecteren **[!UICONTROL ** Doorgaan **]** om het afgeleide veld te verwijderen.


## Functiesjablonen

Om snel een afgeleid gebied voor specifieke gebruiksgevallen tot stand te brengen, zijn de functiesjablonen beschikbaar. Deze functiesjablonen zijn toegankelijk vanuit het selectiegebied in de afgeleide veldinterface of worden weergegeven bij het eerste gebruik in het dialoogvenster [!UICONTROL Start with a field template] wizard.


### Marketingkanalen

Dit malplaatje wordt gevormd om te gebruiken [URL-parse](#dnl-url-parse) en [Hoofdletters/kleine letters](#dnl-case-when) werkt meerdere keren om de juiste waarden van een URL op te halen. De logica wordt dan toegepast op deze waarden om URL aan een specifiek marketing kanaal te associëren.

+++ Details

Als u de sjabloon wilt gebruiken, moet u de juiste parameters opgeven voor elke functie die wordt vermeld als onderdeel van de regels in de sjabloon. Zie [Functieverwijzing](#function-reference) voor meer informatie .

![Constructor voor sjabloonregels voor marketingkanalen](assets/marketing-channel-template.png)

+++

<!--

+++ Data clean up template

>[!WARNING]
>
>Could not find any information on this template.
+++

-->

## Functieverwijzing

Voor elke ondersteunde functie vindt u hieronder meer informatie over:

- specificaties:
   - invoergegevenstype: type ondersteunde gegevens,
   - invoer: mogelijke waarden voor invoer,
   - opgenomen operatoren: operatoren die voor deze functie worden ondersteund (indien aanwezig);
   - limiet: maximumaantal regels (met deze functie) dat u kunt gebruiken in een afgeleid veld,
   - uitvoer.

- gebruiksgevallen, waaronder:
   - gegevens voordat het afgeleide veld wordt gedefinieerd;
   - hoe het afgeleide veld moet worden gedefinieerd,
   - gegevens na het definiëren van het afgeleide veld.

- beperkingen (indien van toepassing).


<!-- Concatenate -->

### [!DNL Concatenate]

Hiermee combineert u twee of meer velden, afgeleide velden of door de gebruiker ingevoerde waarden in één veld met gedefinieerde scheidingstekens.

+++ Details

## Specificaties {#concatenate-io}

| Gegevenstype invoer | Invoer | Opgenomen operatoren | Limiet | Uitvoer |
|---|---|---|:--:|---|
| <p>String</p> | <ul><li>Twee of meer waarden die moeten worden gecombineerd<ul><li>Velden</li><li>Afgeleide waarde van een vorige regel</li><li>Door gebruiker ingevoerde waarde</li></ul></li><li>Scheidingstekens<ul><li>Invoer of selectie van een scheidingsteken voor elke waarde</li></ul></li> </ul> | <p>N.v.t.</p> | <p>2</p> | <p>Nieuw afgeleid veld</p> |

{style="table-layout:auto"}


## Hoofdletters gebruiken {#concatenate-uc}

U verzamelt momenteel de codes van de luchthaven van herkomst en de luchthaven van bestemming als afzonderlijke velden. U wilt de twee velden samenvoegen tot één afmeting, gescheiden door een afbreekstreepje (-). Zo kunt u de combinatie oorsprong en bestemming analyseren om hoogste geboekte routes te identificeren.

Veronderstellingen:

- Oorsprong en doelwaarden worden verzameld in afzonderlijke velden in dezelfde tabel.
- De gebruiker bepaalt of het scheidingsteken &#39;-&#39; tussen de waarden moet worden gebruikt.

Stel dat de volgende boekingen plaatsvinden:

- De klant ABC123 boekt een vlucht tussen Salt Lake City (SLC) en Orlando (MCO)
- De klant ABC456 boekt een vlucht tussen Salt Lake City (SLC) en Los Angeles (LAX)
- De klant ABC789 boekt een vlucht tussen Salt Lake City (SLC) en Seattle (SEA)
- Klant ABC987 boekt een vlucht tussen Salt Lake City (SLC) en San Jose (SJO)
- De klant ABC654 boekt een vlucht tussen Salt Lake City (SLC) en Orlando (MCO)

Het gewenste verslag moet er als volgt uitzien:

| Oorsprong/bestemming | Bladwijzers |
|----|---:|
| SLC-MCO | 2 |
| SLC-LAX | 1 |
| SLC-SEA | 1 |
| SLC-SJO | 1 |

{style="table-layout:auto"}


### Gegevens voor {#concatenate-uc-databefore}

| Oorsprong | Doel |
|----|---:|
| SLC | MCO |
| SLC | LAX |
| SLC | ZEE |
| SLC | SJO |
| SLC | MCO |

{style="table-layout:auto"}

### Afgeleid veld {#concatenate-derivedfield}

U definieert een nieuwe [!UICONTROL Origin - Destination] afgeleid veld. U gebruikt de [!UICONTROL CONCATENATE] functie om een regel te definiëren die de [!UICONTROL Original] en [!UICONTROL Destination] velden die de `-` [!UICONTROL Delimiter].

![[!DNL Concatenate] regel](assets/concatenate.png)

### Gegevens na {#concatenate-dataafter}

| Oorsprong - Bestemming<br/>(afgeleid veld) |
|---|
| SLC-MCO |
| SLC-LAX |
| SLC-SEA |
| SLC-SJO |
| SLC-MCO |

{style="table-layout:auto"}

+++

<!-- CASE WHEN -->

### [!DNL Case When]

Hiermee past u voorwaarden toe op basis van gedefinieerde criteria in een of meer velden. Deze criteria worden vervolgens gebruikt om de waarden in een nieuw afgeleid veld te definiëren op basis van de volgorde van de voorwaarden.

+++ Details

## Specificaties {#casewhen-io}

| Gegevenstype invoer | Invoer | Opgenomen operatoren | Limiet | Uitvoer |
|---|---|---|:---:|---|
| <ul><li>String</li><li>Numeriek</li><li>Datum/datum/tijd</li></ul> | <ul><li>Invoervelden</li><li>Criteria</li></ul> | <p><u>Tekenreeksen</u></p><ul><li>Equals (Is gelijk aan)</li><li>Gelijk aan om het even welke termijn</li><li>Contains the phrase (Bevat de woordgroep)</li><li>Contains any term (Bevat een term)</li><li>Contains all terms (Bevat alle termen)</li><li>Starts with (Begint met)</li><li>Begint met elke term</li><li>Ends with (Eindigt met)</li><li>Eindigt met om het even welke termijn</li><li>Does not equal (Is niet gelijk aan)</li><li>Is niet gelijk aan een term</li><li>Does not contain the phrase (Bevat niet de woordgroep)</li><li>Does not contain any term (Bevat geen enkele term)</li><li>Bevat niet alle termen</li><li>Begint niet met</li><li>Begint niet met enige termijn</li><li>Eindigt niet met</li><li>Beëindigt geen term</li><li>Is ingesteld</li><li>Is niet ingesteld</li></ul><p><u>Numeriek</u></p><ul><li>Equals (Is gelijk aan)</li><li>Does not equal (Is niet gelijk aan)</li><li>Is groter dan</li><li>Is groter dan of gelijk aan</li><li>Is kleiner dan</li><li>Is kleiner dan of gelijk aan</li><li>Is ingesteld</li><li>Is niet ingesteld</li></ul><p><u>Datums</u></p><ul><li>Equals (Is gelijk aan)</li><li>Does not equal (Is niet gelijk aan)</li><li>Is later dan</li><li>Is hoger dan of gelijk aan</li><li>Is voor</li><li>Is voor of gelijk aan</li><li>Is ingesteld</li><li>Is niet ingesteld</li></ul> | <p>5</p> | <p>Nieuw afgeleid veld</p> |

{style="table-layout:auto"}


## Hoofdlettergebruik 1 {#casewhen-uc1}

U wilt regels definiëren om verschillende marketingkanalen te identificeren door trapsgewijze logica toe te passen om een marketingkanaalveld in te stellen op de juiste waarde:

- Als de verwijzer afkomstig is van een zoekmachine en de pagina een querytekenreekswaarde heeft waar `cid` contains `ps_`, dient het afzetkanaal te worden geïdentificeerd als een [!DNL *Betaalde zoekopdracht*].
- Als de verwijzer afkomstig is van een zoekmachine en de pagina niet de queryreeks heeft `cid`, dient het afzetkanaal te worden geïdentificeerd als een [!DNL *Natuurlijk zoeken*].
- Als een pagina een waarde van het vraagkoord heeft waar `cid` contains `em_`, dient het afzetkanaal te worden geïdentificeerd als een [!DNL *E-mail*].
- Als een pagina een waarde van het vraagkoord heeft waar `cid` contains `ds_`, dient het afzetkanaal te worden geïdentificeerd als een [!DNL *Advertentie weergeven*].
- Als een pagina een waarde van het vraagkoord heeft waar `cid` contains `so_`, dient het afzetkanaal te worden geïdentificeerd als een [!DNL *Betaald sociaal*].
- Als de referentie afkomstig is van een verwijzend domein van [!DNL twitter.com], [!DNL facebook.com], [!DNL linkedin.com], of [!DNL tiktok.com], dient het afzetkanaal te worden geïdentificeerd als een [!DNL *Natuurlijk sociaal*].
- Indien aan geen van de bovenstaande voorschriften wordt voldaan, moet het afzetkanaal als [!DNL *Andere referentie*].

Als uw site de volgende voorbeeldgebeurtenissen ontvangt: [!UICONTROL Referrer] en [!UICONTROL Page URL]Deze gebeurtenissen moeten als volgt worden omschreven:

| [!DNL Event] | [!DNL Referrer] | [!DNL Page URL] | [!DNL Marketing Channel] |
|:--:|----|----|----|
| 1 | `https://facebook.com` | `https://site.com/home` | [!DNL Natural Social] |
| 2 | `https://abc.com` | `https://site.com/?cid=ds_12345678` | [!DNL Display] |
| 3 |  | `https://site.com/?cid=em_12345678` | [!DNL Email] |
| 4 | `https://google.com` | `https://site.com/?cid=ps_abc098765` | [!DNL Paid Search] |
| 5 | `https://google.com` | `https://site.com/?cid=em_765544332` | [!DNL Email] |
| 6 | `https://google.com` |  | [!DNL Natural Search] |

{style="table-layout:auto"}

### Gegevens voor {#casewhen-uc1-databefore}

| [!UICONTROL Referrer] | [!DNL Page URL] |
|----|----|
| `https://facebook.com` | `https://site.com/home` |
| `https://abc.com` | `https://site.com/?cid=ds_12345678` |
|  | `https://site.com/?cid=em_12345678` |
| `https://google.com` | `https://site.com/?cid=ps_abc098765` |
| `https://google.com` | `https://site.com/?cid=em_765544332` |
| `https://google.com` |

{style="table-layout:auto"}

### Afgeleid veld {#casewhen-uc1-derivedfield}

U definieert een nieuwe `Marketing Channel` afgeleid veld. U gebruikt de [!UICONTROL CASE WHEN] functies voor het definiëren van regels die waarden maken voor het object op basis van bestaande waarden voor beide `Page URL` en `Referring URL` veld.

Let op het gebruik van de functie [!UICONTROL URL PARSE] om regels te definiëren voor het ophalen van de waarden voor `Page Url` en `Referring Url` vóór de [!UICONTROL CASE WHEN] worden toegepast.

![[!DNL Case when] regel 1](assets/case-when-1.png)

### Gegevens na {#casewhen-uc1-dataafter}

| [!DNL Marketing Channel] |
|----|
| [!DNL Natural Social] |
| [!DNL Display] |
| [!DNL Email] |
| [!DNL Paid Search] |
| [!DNL Email] |
| [!DNL Natural Search] |

{style="table-layout:auto"}


## Hoofdlettergebruik 2 {#casewhen-uc2}

U hebt verschillende verschillende zoekvariaties verzameld in uw [!DNL Product Finding Methods] dimensie. Om de algemene prestaties van onderzoek te begrijpen versus doorbladeren, moet u heel wat tijd doorbrengen die de resultaten manueel combineert.

Uw site verzamelt de volgende waarden voor uw [!DNL Product Finding Methods] dimensie. Uiteindelijk geven al deze waarden een zoekopdracht aan.

| Verzamelde waarde | Werkelijke waarde |
|---|---|
| [!DNL search p13n_no] | [!DNL search] |
| [!DNL search p13n_yes] | [!DNL search] |
| [!DNL search refine p13n_no] | [!DNL search] |
| [!DNL search refine p13n_yes ] | [!DNL search] |
| [!DNL search redirect p13n_yes] | [!DNL search] |
| [!DNL search-redirect] | [!DNL search] |

{style="table-layout:auto"}


### Gegevens voor {#casewhen-uc2-databefore}

| [!DNL Product Finding Methods] |
|----|
| [!DNL search p13_no] |
| [!DNL search p13_yes] |
| [!DNL browse] |
| [!DNL search refine p13_no] |
| [!DNL search refine p13_yes] |
| [!DNL browse] |
| [!DNL search redirect p13_yes] |
| [!DNL search-redirect] |
| [!DNL browse] |

{style="table-layout:auto"}

### Afgeleid veld {#casewhen-uc2-derivedfield}

U definieert een `Product Finding Methods (new)` afgeleid veld. U maakt de volgende [!UICONTROL CASE WHEN] regels in regelbuilder. Deze regels passen logica op alle mogelijke variaties van oude toe [!UICONTROL Product Finding Methods] veldwaarden voor `search` en `browse` met de [!UICONTROL Contains the phrase] criterium.

![[!DNL Case When] regel 2](assets/case-when-2.png)

### Gegevens na {#casewhen-uc2-dataafter}

| [!DNL Product Finding Methods (new)] |
|----|
| [!DNL search] |
| [!DNL search] |
| [!DNL browse] |
| [!DNL search] |
| [!DNL search] |
| [!DNL browse] |
| [!DNL search] |
| [!DNL search] |
| [!DNL browse] |

{style="table-layout:auto"}


## Hoofdlettergebruik 3 {#casewhen-uc3}

Als reisbedrijf, zou u reisduur voor boekte reizen willen opzeggen zodat kunt u op opgemaakte lengten van reizen melden.

Veronderstellingen:

- De organisatie verzamelt reisduur naar een numeriek veld.
- Ze willen de duur van 1 tot 3 dagen in een emmer met de naam &#39;[!DNL short trip]&#39;
- Ze willen de duur van 4 tot 7 dagen in een emmer met de naam &#39;[!DNL medium trip]&#39;
- Ze willen de tijdsduur van 8+ dagen in een emmer met de naam &#39;[!DNL long trip]&#39;
- 132 reizen werden geboekt voor een duur van 1 dag
- 110 reizen werden geboekt voor een duur van 2 dagen
- 105 reizen werden geboekt voor een duur van 3 dagen
- 99 reizen werden geboekt voor een duur van 4 dagen
- 92 reizen werden geboekt voor een duur van 5 dagen
- 85 reizen werden geboekt voor een duur van 6 dagen
- 82 reizen werden geboekt voor een duur van 7 dagen
- 78 reizen werden geboekt voor een duur van 8 dagen
- 50 reizen werden geboekt voor een duur van 9 dagen
- 44 reizen werden geboekt voor een duur van 10 dagen
- 38 reizen werden geboekt voor een duur van 11 dagen
- 31 reizen werden geboekt voor een duur van 12 dagen

Uw gewenste rapport zou als moeten kijken:

| [!DNL Trip Duration Type] | [!DNL Bookings] |
|----|---:|
| [!DNL medium trip] | 358 |
| [!DNL short trip] | 347 |
| [!DNL long trip] | 241 |

{style="table-layout:auto"}

### Gegevens voor {#casewhen-uc3-databefore}

| [!DNL Trip Duration] |
|---:|
| 1 |
| 12 |
| 3 |
| 6 |
| 4 |
| 8 |
| 6 |
| 2 |
| 1 |
| 2 |
| 21 |
| 8 |

### Afgeleid veld {#casewhen-uc3-derivedfield}

U definieert een `Trip Duration (bucketed)` afgeleid veld. U maakt de volgende [!UICONTROL CASE WHEN] regel in regelbouwer. Deze regel past logica toe om de oude [!UICONTROL Trip Duration] veldwaarden in drie waarden: `short trip`, `medium  trip`, en `long trip`.

![[!DNL Case When] regel 3](assets/case-when-3.png)


### Gegevens na {#casewhen-uc3-dataafter}

| [!DNL Trip Duration (bucketed)] |
|---|
| [!DNL short trip] |
| [!DNL long trip] |
| [!DNL short trip] |
| [!DNL medium trip] |
| [!DNL medium trip] |
| [!DNL long trip] |
| [!DNL medium trip] |
| [!DNL short trip] |
| [!DNL short trip] |
| [!DNL short trip] |
| [!DNL long trip] |
| [!DNL long trip] |


## Restricties

CJA gebruikt een geneste containerstructuur, gemodelleerd na Adobe Experience Platform [XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) (Experience Data Model). Zie [Containers](../create-dataview.md#containers) en [Filtercontainers](../../components/filters/filters-overview.md#filter-containers) voor meer achtergrondinformatie. Dit containermodel, zij het flexibel door aard, legt sommige beperkingen op wanneer het gebruiken van de regelbouwer.

CJA gebruikt het volgende standaardcontainermodel:

<p align="center">
<img src="./assets/containers.png" width="50%" valign="middle">
</p>



De volgende beperkingen zijn van toepassing en worden afgedwongen wanneer *selecteren* en *instellen* waarden.

|  | Restricties |
|:---:|----|
| **<span style='color: red'>A</span>** | Waarden *selecteren* binnen dezelfde [!UICONTROL If], [!UICONTROL Else If] construct (gebruiken [!UICONTROL And] of [!UICONTROL Or]) in een regel moet afkomstig zijn van dezelfde container en kan van elk type zijn (tekenreeks ![String](assets/Smock_ABC_18_N.svg), numeriek ![Numeriek](assets/Smock_123_18_N.svg), enzovoort). <br/>![Afhankelijkheid A](assets/dependency-a.png) |
| **<span style='color: red'>B</span>** | Alle waarden die u *set* over een regel moet van de zelfde container zijn en het zelfde type of een afgeleide waarde van het zelfde type hebben. <br/> ![Afhankelijkheid B](assets/dependency-b.png) |
| **<span style='color: blue'>C</span>** | De waarden die u *selecteren* dwars [!UICONTROL If], [!UICONTROL Else If] constructies in de regel do *niet* moeten afkomstig zijn uit dezelfde container en moet *niet* moeten van hetzelfde type zijn. <br/> ![Afhankelijkheid C](assets/dependency-c.png) |

{style="table-layout:auto"}

+++


<!-- FIND AND REPLACE -->

### [!DNL Find and Replace]

Hiermee zoekt u alle waarden in een geselecteerd veld en vervangt u deze waarden door een andere waarde in een nieuw afgeleid veld.

+++ Details

## Specificaties {#findreplace-io}

| Gegevenstype invoer | Invoer | Opgenomen operatoren | Limiet | Uitvoer |
|---|---|---|:---:|---|
| <p>String</p> | <ul><li><span>Veldcriteria &#39;Wanneer moet ik vervangen&#39;</span></li><li><span>Veldwaarde &#39;vervangen door&#39;</span><ul><li><span>Door gebruiker ingevoerd</span></li><li><span>Afzonderlijk veld</span></li></ul></li></ul> | <p><u>Tekenreeksen</u></p><ul><li>Alles zoeken en Alles vervangen</li></ul> | <p>1</p> | <p>Nieuw afgeleid veld</p> |

{style="table-layout:auto"}


## Hoofdletters gebruiken {#findreplace-uc}

U hebt een aantal misvormde waarden ontvangen voor uw externe marketingkanaalrapport, bijvoorbeeld `email%20 marketing` in plaats van `email marketing`. Deze misvormde waarden breken uw rapportering en maken het moeilijker te zien hoe e-mail presteert. U wilt vervangen `email%20marketing` with `email marketing`.

**Oorspronkelijk rapport**

| [!DNL External Marketing Channels] | [!DNL Sessions] |
|---|--:|
| [!DNL email marketing] | 500 |
| [!DNL email %20marketing] | 24 |

{style="table-layout:auto"}

**Voorkeursrapport**

| [!DNL External Marketing Channels] | [!DNL Sessions] |
|---|--:|
| [!DNL email marketing] | 524 |


### Gegevens voor {#findreplace-uc-databefore}

| [!DNL External Marketing] |
|----|
| [!DNL email marketing] |
| [!DNL email%20marketing] |
| [!DNL email marketing] |
| [!DNL email marketing] |
| [!DNL email%20marketing] |

{style="table-layout:auto"}

### Afgeleid veld {#findreplace-uc-derivedfield}

U definieert een `Email Marketing (updated)` afgeleid veld. U gebruikt de [!UICONTROL FIND AND REPLACE] functie om een regel te definiëren voor het zoeken en vervangen van alle instanties van `email%20marketing` with `email marketing`.

![[!DNL Find and Replace] regel](assets/find-and-replace.png)

### Gegevens na {#findreplace-uc-dataafter}

| [!DNL External Marketing (updated)] |
|----|
| [!DNL email marketing] |
| [!DNL email marketing] |
| [!DNL email marketing] |
| [!DNL email marketing] |
| [!DNL email marketing] |

{style="table-layout:auto"}

+++


<!-- LOOKUP -->

### [!DNL Lookup]

Definieert een set opzoekwaarden die worden vervangen door corresponderende waarden.

+++ Details


## Specificaties {#lookup-io}

| Gegevenstype invoer | Invoer | Opgenomen operatoren | Limiet | Uitvoer |
|---|---|---|:---:|---|
| <ul><li>String</li><li>Numeriek</li><li>Datum</li></ul> | <ul><li>Eén veld</li><li>Bestand opzoeken<ul><li>Toetskolom</li><li>Nieuwe veldkolom</li></ul></li></ul> | <p>N.v.t.</p> | <p>5</p> | <p>Nieuw afgeleid veld</p> |

{style="table-layout:auto"}


## Hoofdlettergebruik 1 {#lookup-uc1}

U hebt een CSV-bestand met een sleutelkolom voor `hotelID` en een of meer aanvullende kolommen met betrekking tot de `hotelID`: `city`, `rooms`, `hotel name`.
U verzamelt [!DNL Hotel ID] in een dimensie, maar wil een [!DNL Hotel Name] van de `hotelID` in het CSV-bestand.

**CSV-bestandsstructuur en -inhoud**

| [!DNL hotelID] | [!DNL city] | [!DNL rooms] | [!DNL hotel name] |
|---|---|---:|---|
| [!DNL SLC123] | [!DNL Salt Lake City] | 40 | [!DNL SLC Downtown] |
| [!DNL LAX342] | [!DNL Los Angeles] | 60 | [!DNL LA Airport] |
| [!DNL SFO456] | [!DNL San Francisco] | 75 | [!DNL Market Street] |

{style="table-layout:auto"}

**Huidig rapport**

| [!DNL Hotel ID] | Productweergaven |
|---|---:|
| [!DNL SLC123] | 200 |
| [!DNL LX342] | 198 |
| [!DNL SFO456] | 190 |

{style="table-layout:auto"}


**Gewenst rapport**

| [!DNL Hotel Name] | Productweergaven |
|----|----:|
| [!DNL SLC Downtown] | 200 |
| [!DNL LA Airport] | 198 |
| [!DNL Market Street] | 190 |

{style="table-layout:auto"}

### Gegevens voor {#lookup-uc1-databefore}

| [!DNL Hotel ID] |
|----|
| [!DNL SLC123] |
| [!DNL LAX342] |
| [!DNL SFO456] |

{style="table-layout:auto"}


### Afgeleid veld {#lookup-uc1-derivedfield}

U definieert een `Hotel Name` afgeleid veld. U gebruikt de [!UICONTROL LOOKUP] functie om een regel te definiëren waarin u waarden van de [!UICONTROL Hotel ID] veld en vervangen door nieuwe waarden.

![[!DNL Lookup] regel 1](assets/lookup-1.png)

### Gegevens na {#lookup-uc1-dataafter}

| [!DNL Hotel Name] |
|----|
| [!DNL SLC Downtown] |
| [!DNL LA Airport] |
| [!DNL Market Street] |

{style="table-layout:auto"}


## Hoofdlettergebruik 2 {#lookup-uc2}

U hebt URL&#39;s verzameld in plaats van de vriendelijke paginanaam voor verschillende pagina&#39;s. Deze gemengde verzameling van waarden breekt de rapportage af.

### Gegevens voor {#lookup-uc2-databefore}

| [!DNL Page Name] |
|---|
| [!DNL Home Page] |
| [!DNL Flight Search] |
| `http://www.adobetravel.ca/Hotel-Search` |
| `https://www.adobetravel.com/Package-Search` |
| [!DNL Deals & Offers] |
| `http://www.adobetravel.ca/user/reviews` |
| `https://www.adobetravel.com.br/Generate-Quote/preview` |

{style="table-layout:auto"}

### Afgeleid veld {#lookup-uc2-derivedfield}

U definieert een `Page Name (updated)` afgeleid veld. U gebruikt de [!UICONTROL LOOKUP] functie om een regel te definiëren waarin u waarden van uw bestaande [!UICONTROL Page Name] veld en vervangen door bijgewerkte correcte waarden.

![[!DNL Lookup] regel 2](assets/lookup-2.png)

### Gegevens na {#lookup-uc2-dataafter}

| [!DNL Page Name (updated)] |
|---|
| [!DNL Home Page] |
| [!DNL Flight Search] |
| [!DNL Hotel Search] |
| [!DNL Package Search] |
| [!DNL Deals & Offers] |
| [!DNL Reviews] |
| [!DNL Generate Quote] |

+++

<!-- URL PARSE -->

### [!DNL URL Parse]

Hiermee worden verschillende delen van een URL uitgeparseerd, zoals protocol-, host-, pad- of queryparameters.

+++ Details

## Specificaties {#urlparse-io}

| Gegevenstype invoer | Invoer | Opgenomen operatoren | Limiet | Uitvoer |
|---|---|---|:---:|---|
| <ul><li>String</li></ul> | <ul><li>Eén veld</li><li>Parseren, optie<ul><li>Protocol ophalen</li><li>Host ophalen</li><li>Pad ophalen</li><li>Query-waarde ophalen<ul><li>Query-param</li></ul></li><li>Hashwaarde ophalen</li></ul></li></ul></li></ul> | <p>N.v.t.</p> | <p>5</p> | <p>Nieuw afgeleid veld</p> |

{style="table-layout:auto"}


## Hoofdlettergebruik 1 {#urlparse-uc1}

U wilt het verwijzende domein van verwijzende URL als deel van de reeks van regels van een marketingkanaal slechts gebruiken.

### Gegevens voor {#urlparse-uc1-databefore}

| [!DNL Referring URL] |
|----|
| `https://www.google.com/` |
| `https://duckduckgo.com/` |
| `https://t.co/` |
| `https://l.facebook.com/` |

{style="table-layout:auto"}

### Afgeleid veld {#urlparse-uc1-derivedfield}

U definieert een  `Referring Domain` afgeleid veld. U gebruikt de [!UICONTROL URL PARSE] functie om een regel te bepalen om de gastheer van te halen [!UICONTROL Referring URL] en sla dat op in het nieuwe afgeleide veld.

![[!DNL Url Parse] regel 1](assets/url-parse-1.png)

### Gegevens na {#urlparse-uc1-dataafter}

| [!DNL Referrer Domain] |
|----|
| [!DNL www.google.com] |
| [!DNL duckduckgo.com] |
| [!DNL t.co] |
| [!DNL l.facebook.com] |

{style="table-layout:auto"}


## Hoofdlettergebruik 2 {#urlparse-uc2}

U wilt de waarde van `cid` parameter van een queryreeks in een [!DNL Page URL] als deel van de output van een afgeleid het volgen coderapport.

### Gegevens voor {#urlparse-uc2-databefore}

| [!DNL Page URL] |
|----|
| `https://www.adobe.com/?cid=abc123` |
| `https://www.adobe.com/?em=email1234&cid=def123` |
| `https://www.adobe.com/landingpage?querystring1=test&test2=1234&cid=xyz123` |

{style="table-layout:auto"}

### Afgeleid veld {#urlparse-uc2-derivedfield}

U definieert een `Query String CID` afgeleid veld. U gebruikt de [!UICONTROL URL PARSE] functie om een regel te bepalen om de waarde van de parameter van het vraagkoord in te halen [!UICONTROL Page URL] veld, opgeven `cid` als de queryparameter. De outputwaarde wordt opgeslagen op het nieuwe afgeleide gebied.

![[!DNL Url Parse] regel 2](assets/url-parse-2.png)

### Gegevens na {#urlparse-uc2-dataafter}

| [!DNL Query String CID] |
|----|
| [!DNL abc123] |
| [!DNL def123] |
| [!DNL xyz123] |

{style="table-layout:auto"}

+++
