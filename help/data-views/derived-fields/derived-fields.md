---
title: Afgeleide velden
description: Een afgeleid gebied specificeert rapport-tijd manipulatie van schemagebieden en/of standaardcomponenten door een reeks beschikbare functies en functiesjablonen.
solution: Customer Journey Analytics
feature: Data Views
hide: true
hidefromtoc: true
source-git-commit: cf36e6c662835b10c60f400c95e341865a9e56b1
workflow-type: tm+mt
source-wordcount: '3015'
ht-degree: 3%

---


# Afgeleide velden

Afgeleide velden zijn een belangrijk aspect van de functionaliteit voor real-time rapportage in Customer Journey Analytics (CJA). Een afgeleid (douane) gebied staat u toe om (vaak complexe) gegevensmanipulaties te bepalen, door een klantgerichte regelbouwer. Vervolgens kunt u dat afgeleide veld als een component (metrisch of dimensionaal) gebruiken in [Werkruimte](../../analysis-workspace/home.md) of zelfs nader te definiëren als component in [Gegevens, weergave](../data-views.md).

Afgeleide velden kunnen veel tijd en moeite besparen, in vergelijking met het transformeren of manipuleren van gegevens op andere locaties buiten CJA. zoals [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html), [Data Distiller](https://experienceleague.adobe.com/docs/experience-platform/query/data-distiller/overview.html?lang=en)of binnen uw eigen ETL-processen (Extract Transform Load) / Extract Load Transform (ELT-processen).

Afgeleide velden worden gedefinieerd als aangepaste velden binnen [Gegevensweergaven](../data-views.md), zijn gebaseerd op een set functies en worden toegepast op beschikbare standaard- en/of schemavelden.

Voorbeelden van gebruiksgevallen zijn:

- Definieer een aangepast veld Paginanaam waarmee onjuist verzamelde waarden voor paginanamen worden gecorrigeerd.

- Definieer een aangepast veld Marketingkanaal dat het juiste marketingkanaal bepaalt op basis van een of meer voorwaarden (bijvoorbeeld URL-parameter, pagina-URL, paginanaam).


## Aangepaste veldinterface

Wanneer u een aangepast veld maakt of bewerkt, gebruikt u de aangepaste veldinterface.

![Dialoogvenster Aangepast veld](assets/custom-field-dialog.png)


|  | Naam | Beschrijving |
|---------|----------|--------|
| 1 | **Kiezer** | U gebruikt het selectiegebied om uw ![Functie](assets/Smock_Function_18_N.svg) functie,![Pictogram voor functiesjabloon](assets/Smock_FileTemplate_18_N.svg) functiesjabloon,![Pictogram Schema-veld](assets/Smock_Folder_18_N.svg) schemaveld, of![Standaardveldpictogram](assets/Smock_DragHandle_18_N.svg)het standaardgebied op aan de regelbouwer. <br/>Gebruik de vervolgkeuzelijst om te selecteren tussen [!UICONTROL Functions], [!UICONTROL Function templates], [!UICONTROL Schema fields], en [!UICONTROL Standard fields].<br/>Met het vak Zoeken kunt u zoeken naar functies, functiesjablonen, schema&#39;s en standaardvelden. <br/>U kunt de lijst met geselecteerde objecten filteren door ![Filterpictogram](assets/Smock_Filter_18_N.svg) Filteren en filters opgeven in het dialoogvenster [!UICONTROL Filter fields by] . U kunt filters eenvoudig verwijderen met ![Pictogram Sluiten](assets/CrossSize75.svg) voor elk filter. |
| 2 | **Regelbouwer** | U kunt een aangepast veld opeenvolgend maken met een of meer regels. Een regel is een specifieke implementatie van een functie en wordt daarom altijd met slechts één functie geassocieerd. U creeert een regel door een functie in de Bouwer van de Regel te slepen en te laten vallen. Het functietype bepaalt de interface van de regel.<br/>Zie de [Regelinterface](#rule-interface) voor meer informatie . <br/>U kunt een functie bij het begin, het eind, of binnen tussen regels opnemen reeds beschikbaar in de Bouwer van de Regel. De laatste regel in de Bouwer van de Regel bepaalt de definitieve output van het douanegebied. |
| 3 | **[!UICONTROL ** Veldinstellingen **]** | U kunt het aangepaste veld een naam geven en beschrijven en het veldtype controleren. |
| 4 | **[!UICONTROL ** Uiteindelijke uitvoer **]** | In dit gebied ziet u een ter plekke bijgewerkte voorvertoning van uitvoerwaarden, gebaseerd op gegevens in de afgelopen 30 dagen en de wijzigingen die u aanbrengt in het aangepaste veld in de regelbouwer. |

{style="table-layout:auto"}

Wanneer u de interface van het gebied van de Douane voor het eerst opent, [!UICONTROL Start with a field template] wordt weergegeven.

![Dialoogvenster Sjabloonwizard voor aangepaste velden](assets/field-template-dialog.png)

1. Selecteer de sjabloon die het beste het type veld beschrijft dat u wilt maken.
2. Selecteer **[!UICONTROL ** Selecteren **]** om door te gaan.

Het dialoogvenster Aangepast wordt gevuld met regels (en functies) die vereist of handig zijn voor het type veld dat u hebt geselecteerd. Zie [Functiesjablonen](#function-templates) voor meer informatie over de beschikbare sjablonen.

## Regelinterface

Wanneer u een regel in de Bouwer van de Regel bepaalt, gebruikt u de regelinterface.

![Regelinterface](assets/rule-interface.png)

|  | Naam | Beschrijving |
|---------|----------|--------|
| A | **Naam van regel** | Standaard is de regelnaam **Regel X** (X verwijst naar een volgnummer). Als u de naam van een regel wilt bewerken, selecteert u de naam en typt u de nieuwe naam, bijvoorbeeld `Query Parameter`. |
| B | **Functienaam** | De geselecteerde functienaam voor de regel, bijvoorbeeld [!DNL URL PARSE]. Wanneer de functie de laatste in de reeks functies is en de uiteindelijke uitvoerwaarden bepaalt, wordt de functienaam gevolgd door [!DNL FINAL OUTPUT]bijvoorbeeld [!DNL URL PARSE - FINAL OUTPUT]. <br/>Als u een pop-up met meer informatie over de functie wilt weergeven, selecteert u ![Help-pictogram](assets/Smock_HelpOutline_18_N.svg). |
| C | **Beschrijving van regel** | U kunt desgewenst een beschrijving aan een regel toevoegen.<br/>Selecteren ![Meer pictogram](assets/More.svg)selecteert u vervolgens **[!UICONTROL ** Beschrijving toevoegen **]** om een beschrijving toe te voegen of **[!UICONTROL ** Beschrijving bewerken **]** om een bestaande beschrijving te bewerken.<br/>Gebruik de editor om een beschrijving in te voeren. U kunt de werkbalk gebruiken om de tekst op te maken (met de stijlkiezer, vet, cursief, onderstrepen, rechts, links, gecentreerd, kleur, nummerlijst, opsommingslijst) en om koppelingen toe te voegen aan externe informatie. <br/>Klik buiten de editor om het bewerken van de beschrijving te voltooien. |
| D | **Functiegebied** | Definieert de logica van de functie. De interface is afhankelijk van het type functie. Zie [Functieverwijzing](#function-reference) voor gedetailleerde informatie over elk van de ondersteunde functies. |

{style="table-layout:auto"}

## Een aangepast veld maken

1. Selecteer een bestaande gegevensweergave of maak een gegevensweergave. Zie [Gegevensweergaven](../data-views.md) voor meer informatie .

2. Selecteer **[!UICONTROL ** Componenten **]** van de weergave Gegevens.

3. Selecteren **[!UICONTROL ** Aangepast veld maken **]** van de linkerspoorstaaf.

4. Als u uw aangepaste veld wilt definiëren, gebruikt u de opdracht [!UICONTROL Create custom field] interface. Zie [Aangepaste veldinterface](#custom-field-interface).

   Als u het nieuwe aangepaste veld wilt opslaan, selecteert u **[!UICONTROL ** Opslaan **]**.

5. Uw nieuwe aangepaste veld wordt toegevoegd aan de **[!UICONTROL ** Aangepaste velden >**]** container, als onderdeel van **[!UICONTROL ** Schema-velden **]** in de linkertrack van de gegevensweergave.


## Een aangepast veld bewerken

1. Selecteer een bestaande gegevensweergave. Zie [Gegevensweergaven](../data-views.md) voor meer informatie .

2. Selecteer **[!UICONTROL ** Componenten **]** van de weergave Gegevens.

3. Selecteren **[!UICONTROL ** Schema-velden **]** in de [!UICONTROL Connection] aan de linkerkant.

4. Selecteren **[!UICONTROL ** Aangepaste velden >**]** container.

5. Houd de cursor boven het aangepaste veld dat u wilt bewerken en selecteer ![Pictogram Bewerken](assets/Smock_Edit_18_N.svg).

6. Als u uw aangepaste veld wilt bewerken, gebruikt u de opdracht [!UICONTROL Edit custom field] interface. Zie [Aangepaste veldinterface](#custom-field-interface).

   - Selecteren **[!UICONTROL ** Opslaan **]** om het bijgewerkte aangepaste veld op te slaan.

   - Selecteren **[!UICONTROL ** Annuleren **]** om wijzigingen die u in het aangepaste veld hebt aangebracht, te annuleren.

   - Selecteren **[!UICONTROL ** Opslaan als **]** om het aangepaste veld op te slaan als een nieuw aangepast veld. Het nieuwe aangepaste veld heeft dezelfde naam als het oorspronkelijke bewerkte aangepaste veld met `(copy)` toegevoegd.

## Een aangepast veld verwijderen

1. Selecteer een bestaande gegevensweergave. Zie [Gegevensweergaven](../data-views.md) voor meer informatie .

2. Selecteer **[!UICONTROL ** Componenten **]** van de weergave Gegevens.

3. Selecteren **[!UICONTROL ** Schema-velden **]** tab in [!UICONTROL Connection] venster.

4. Selecteren **[!UICONTROL ** Aangepaste velden >**]** container.

5. Houd de muisaanwijzer boven het aangepaste veld dat u wilt verwijderen en selecteer ![Pictogram Bewerken](assets/Smock_Edit_18_N.svg).

6. In het gebruik **[!UICONTROL ** Aangepast veld bewerken **]** -interface selecteert u Verwijderen.

   A [!UICONTROL Delete component] wordt u gevraagd de verwijdering te bevestigen. Houd rekening met eventuele externe verwijzingen naar het aangepaste veld buiten de weergave Gegevens.

   - Selecteren **[!UICONTROL ** Doorgaan **]** om het aangepaste veld te verwijderen.


## Functiesjablonen

Als u snel een aangepast veld voor specifieke gebruiksgevallen wilt maken, zijn er functiesjablonen beschikbaar. Deze functiesjablonen zijn toegankelijk vanuit het gebied Selector in de interface van het veld Aangepast of worden weergegeven bij het eerste gebruik in het dialoogvenster [!UICONTROL Start with a field template] wizard.


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

Voor elke ondersteunde functie vindt u hieronder meer informatie:

- input, operatoren en output

- gebruiksgevallen, waaronder:
   - gegevens voordat het aangepaste veld wordt gedefinieerd
   - het aangepaste veld definiëren
   - gegevens na het definiëren van het aangepaste veld


<!-- Concatenate -->

### [!DNL Concatenate]

Hiermee voegt u twee of meer velden, aangepaste velden of door de gebruiker ingevoerde waarden samen tot één veld met gedefinieerde scheidingstekens.

+++ Details

## Invoer / Operatoren / Uitvoer {#concatenate-io}

| Gegevenstype invoer | Invoer | Opgenomen operatoren | Uitvoer |
|---|---|---|---|
| <p>String</p> | <ul><li>Twee of meer waarden die moeten worden gecombineerd<ul><li>Velden</li><li>Afgeleide waarde van een vorige regel</li><li>Door gebruiker ingevoerde waarde</li></ul></li><li>Scheidingstekens<ul><li>Invoer of selectie van een scheidingsteken voor elke waarde</li></ul></li> </ul> | <p>N.v.t.</p> | <p>Nieuw aangepast veld</p> |

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
|---|---|
| SLC-MCO | 2 |
| SLC-LAX | 1 |
| SLC-SEA | 1 |
| SLC-SJO | 1 |

{style="table-layout:auto"}


### Gegevens voor {#concatenate-uc-databefore}

| Oorsprong | Doel |
|----|----|
| SLC | MCO |
| SLC | LAX |
| SLC | ZEE |
| SLC | SJO |
| SLC | MCO |

{style="table-layout:auto"}

### Aangepast veld {#concatenate-customfield}

U definieert een nieuwe **[!UICONTROL ** Oorsprong - Bestemming **]** aangepast veld. U gebruikt de **[!UICONTROL CONCATENATE]** functie om een regel te definiëren die de [!UICONTROL Original] en [!UICONTROL Destination] velden die de `-` [!UICONTROL Delimiter].

![[!DNL Concatenate] regel](assets/concatenate.png)

### Gegevens na {#concatenate-dataafter}

| Oorsprong - Bestemming<br/>(aangepast veld) |
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

Hiermee past u voorwaarden toe op basis van gedefinieerde criteria in een of meer velden. Deze criteria worden vervolgens gebruikt om de waarden in een nieuw aangepast veld te definiëren op basis van de volgorde van de voorwaarden.

+++ Details

## Invoer / Operatoren / Uitvoer {#casewhen-io}

| Gegevenstype invoer | Invoer | Opgenomen operatoren | Uitvoer |
|---|---|---|---|
| <ul><li>String</li><li>Numeriek</li><li>Datum/datum/tijd</li></ul> | <ul><li>Invoervelden</li><li>Criteria</li></ul> | <p><u>Tekenreeksen</u></p><ul><li>Equals (Is gelijk aan)</li><li>Gelijk aan om het even welke termijn</li><li>Contains the phrase (Bevat de woordgroep)</li><li>Contains any term (Bevat een term)</li><li>Contains all terms (Bevat alle termen)</li><li>Starts with (Begint met)</li><li>Begint met elke term</li><li>Ends with (Eindigt met)</li><li>Eindigt met om het even welke termijn</li><li>Does not equal (Is niet gelijk aan)</li><li>Is niet gelijk aan een term</li><li>Does not contain the phrase (Bevat niet de woordgroep)</li><li>Does not contain any term (Bevat geen enkele term)</li><li>Bevat niet alle termen</li><li>Begint niet met</li><li>Begint niet met enige termijn</li><li>Eindigt niet met</li><li>Beëindigt geen term</li><li>Is ingesteld</li><li>Is niet ingesteld</li></ul><p><u>Numeriek</u></p><ul><li>Equals (Is gelijk aan)</li><li>Does not equal (Is niet gelijk aan)</li><li>Is groter dan</li><li>Is groter dan of gelijk aan</li><li>Is kleiner dan</li><li>Is kleiner dan of gelijk aan</li><li>Is ingesteld</li><li>Is niet ingesteld</li></ul><p><u>Datums</u></p><ul><li>Equals (Is gelijk aan)</li><li>Does not equal (Is niet gelijk aan)</li><li>Is later dan</li><li>Is hoger dan of gelijk aan</li><li>Is voor</li><li>Is voor of gelijk aan</li><li>Is ingesteld</li><li>Is niet ingesteld</li></ul> | <p>Nieuw aangepast veld</p> |

{style="table-layout:auto"}


## Hoofdlettergebruik 1 {#casewhen-uc1}

U wilt regels definiëren om verschillende marketingkanalen te identificeren door trapsgewijze logica toe te passen om een marketingkanaalveld in te stellen op de juiste waarde:

- Als de verwijzer afkomstig is van een zoekmachine en de pagina een querytekenreekswaarde heeft waar `cid` contains `ps_`, dient het afzetkanaal te worden geïdentificeerd als een **Betaalde zoekopdracht**.
- Als de verwijzer afkomstig is van een zoekmachine en de pagina niet de queryreeks heeft `cid`, dient het afzetkanaal te worden geïdentificeerd als een **Natuurlijk zoeken**.
- Als een pagina een waarde van het vraagkoord heeft waar `cid` contains `em_`, dient het afzetkanaal te worden geïdentificeerd als een **E-mail**.
- Als een pagina een waarde van het vraagkoord heeft waar `cid` contains `ds_`, dient het afzetkanaal te worden geïdentificeerd als een **Advertentie weergeven**.
- Als een pagina een waarde van het vraagkoord heeft waar `cid` contains `so_`, dient het afzetkanaal te worden geïdentificeerd als een **Betaald sociaal**.
- Als de referentie afkomstig is van een verwijzend domein van twitter.com, facebook.com, linkedin.com of tiktok.com, moet het marketingkanaal worden geïdentificeerd als een **Natuurlijk sociaal**.
- Indien aan geen van de bovenstaande voorschriften wordt voldaan, moet het afzetkanaal als **Andere referentie**.

Als uw site de volgende voorbeeldgebeurtenissen ontvangt, die Referrer en Page URL bevatten, moeten deze gebeurtenissen als volgt worden geïdentificeerd:

| Gebeurtenis | Referrer | Pagina-URL | Marketingkanaal |
|:----:|----|----|----|
| 1 | `https://facebook.com` | `https://site.com/home` | Natuurlijk sociaal |
| 2 | `https://abc.com` | `https://site.com/?cid=ds_12345678` | Weergave |
| 3 |  | `https://site.com/?cid=em_12345678` | E-mail |
| 4 | `https://google.com` | `https://site.com/?cid=ps_abc098765` | Betaalde zoekopdracht |
| 5 | `https://google.com` | `https://site.com/?cid=em_765544332` | E-mail |
| 6 | `https://google.com` |  | Natuurlijk zoeken |

{style="table-layout:auto"}

### Gegevens voor {#casewhen-uc1-databefore}

| Referrer | Pagina-URL |
|----|----|
| `https://facebook.com` | `https://site.com/home` |
| `https://abc.com` | `https://site.com/?cid=ds_12345678` |
|  | `https://site.com/?cid=em_12345678` |
| `https://google.com` | `https://site.com/?cid=ps_abc098765` |
| `https://google.com` | `https://site.com/?cid=em_765544332` |
| `https://google.com` |

{style="table-layout:auto"}

### Aangepast veld {#casewhen-uc1-customfield}

U definieert een nieuwe `Marketing Channel` aangepast veld. U gebruikt de **[!UICONTROL CASE WHEN]** functies voor het definiëren van regels die waarden maken voor het object op basis van bestaande waarden voor beide `Page URL` en `Referring URL` veld.

Let op het gebruik van de functie **[!UICONTROL ** URL-PARSE **]** om regels te definiëren voor het ophalen van de waarden voor `Page Url` en `Referring Url` vóór de **[!UICONTROL ** GEVEN WANNEER **]** worden toegepast.

![[!DNL Case when] regel 1](assets/case-when-1.png)

### Gegevens na {#casewhen-uc1-dataafter}

| Marketingkanaal |
|----|
| Natuurlijk sociaal |
| Weergave |
| E-mail |
| Betaalde zoekopdracht |
| E-mail |
| Natuurlijk zoeken |

{style="table-layout:auto"}


## Hoofdlettergebruik 2 {#casewhen-uc2}

U hebt verschillende verschillende zoekvariaties verzameld binnen de dimensie Zoekmethoden voor producten. Om de algemene prestaties van onderzoek te begrijpen versus doorbladeren, moet u heel wat tijd doorbrengen die de resultaten manueel combineert.

Uw site verzamelt de volgende waarden voor de dimensie Methoden zoeken in uw product. Uiteindelijk geven al deze waarden een zoekopdracht aan.

| Verzamelde waarde | Werkelijke waarde |
|---|---|
| search p13n_no | zoeken |
| zoek p13n_yes | zoeken |
| zoeken p13n_no verfijnen | zoeken |
| zoek p13n_yes verfijnen | zoeken |
| p13n_yes doorzoeken | zoeken |
| doorzoeken | zoeken |

{style="table-layout:auto"}


### Gegevens voor {#casewhen-uc2-databefore}

| Methoden voor het zoeken van producten |
|----|
| search p13_no |
| zoek p13_ja |
| doorbladeren |
| zoek verfijnen p13_no |
| zoek verfijnen p13_yes |
| doorbladeren |
| doorzoeken p13_ja |
| doorzoeken |
| doorbladeren |

{style="table-layout:auto"}

### Aangepast veld {#casewhen-uc2-customfield}

U definieert een `Product Finding Methods (new)` aangepast veld. U maakt de volgende **[!UICONTROL ** GEVEN WANNEER **]** regels in de Bouwer van de Regel. Deze regels passen logica op alle mogelijke variaties van oude toe **[!UICONTROL ** Methoden voor het zoeken van producten **]** veldwaarden voor `search` en `browse` met de **[!UICONTROL Contains the phrase]** criterium.

![[!DNL Case When] regel 2](assets/case-when-2.png)

### Gegevens na {#casewhen-uc2-dataafter}

| Methoden voor het zoeken van producten (nieuw) |
|----|
| zoeken |
| zoeken |
| doorbladeren |
| zoeken |
| zoeken |
| doorbladeren |
| zoeken |
| zoeken |
| doorbladeren |

{style="table-layout:auto"}


## Hoofdlettergebruik 3 {#casewhen-uc3}

Als reisbedrijf, zou u reisduur voor boekte reizen willen opzeggen zodat kunt u op opgemaakte lengten van reizen melden.

Veronderstellingen:

- De organisatie verzamelt reisduur naar een numeriek veld.
- Ze willen een duur van 1-3 dagen in een emmer &quot;korte reis&quot; steken
- Ze willen een duur van 4 tot 7 dagen in een emmer steken, &#39;gemiddelde reis&#39; genoemd
- Ze willen de duur van 8+ dagen in een emmer &quot;lange reis&quot; stoppen
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

| Type reisduur | Bladwijzers |
|----|---:|
| middelmatige reis | 358 |
| korte reis | 347 |
| lange reis | 241 |

{style="table-layout:auto"}

### Gegevens voor {#casewhen-uc3-databefore}

| Duur reis |
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

{style="table-layout:auto"}

### Aangepast veld {#casewhen-uc3-customfield}

U definieert een `Trip Duration (bucketed)` aangepast veld. U maakt de volgende **[!UICONTROL ** GEVEN WANNEER **]** regel in de Bouwer van de Regel. Deze regel past logica toe om de oude **[!UICONTROL ** Duur reis **]** veldwaarden in drie waarden: `short trip`, `medium  trip`, en `long trip`.

![[!DNL Case When] regel 3](assets/case-when-3.png)


### Gegevens na {#casewhen-uc3-dataafter}

| Duur van de reis (gespaard) |
|---|
| korte reis |
| lange reis |
| korte reis |
| middelmatige reis |
| middelmatige reis |
| lange reis |
| middelmatige reis |
| korte reis |
| korte reis |
| korte reis |
| lange reis |
| lange reis |

+++


<!-- FIND AND REPLACE -->

### [!DNL Find and Replace]

Hiermee zoekt u alle waarden in een geselecteerd veld en vervangt u deze waarden door een andere waarde in een nieuw aangepast veld.

+++ Details

## Invoer / Operatoren / Uitvoer {#findreplace-io}

| Gegevenstype invoer | Invoer | Opgenomen operatoren | Uitvoer |
|---|---|---|---|
| <p>String</p> | <ul><li><span>Veldcriteria &#39;Wanneer moet ik vervangen&#39;</span></li><li><span>Veldwaarde &#39;vervangen door&#39;</span><ul><li><span>Door gebruiker ingevoerd</span></li><li><span>Afzonderlijk veld</span></li></ul></li></ul> | <p><u>Tekenreeksen</u></p><ul><li>Alles zoeken en Alles vervangen</li></ul> | <p>Nieuw aangepast veld</p> |

{style="table-layout:auto"}


## Hoofdletters gebruiken {#findreplace-uc}

U hebt een aantal misvormde waarden ontvangen voor uw externe marketingkanaalrapport, bijvoorbeeld `email%20 marketing` in plaats van `email marketing`. Deze misvormde waarden breken uw rapportering en maken het moeilijker te zien hoe e-mail presteert. U wilt vervangen `email%20marketing` with `email marketing`.

**Oorspronkelijk rapport**

| Externe marketingkanalen | Sessies |
|---|---|
| e-mailmarketing | 500 |
| email%20marketing | 24 |

{style="table-layout:auto"}

**Voorkeursrapport**

| Externe marketingkanalen | Sessies |
|---|---|
| e-mailmarketing | 524 |


### Gegevens voor {#findreplace-uc-databefore}

| Externe marketing |
|----|
| e-mailmarketing |
| email%20marketing |
| e-mailmarketing |
| e-mailmarketing |
| email%20marketing |

{style="table-layout:auto"}

### Aangepast veld {#findreplace-uc-customfield}

U definieert een `Email Marketing (updated)` aangepast veld. U gebruikt de **[!UICONTROL FIND AND REPLACE]** functie om een regel te definiëren voor het zoeken en vervangen van alle instanties van `email%20marketing` with `email marketing`.

![[!DNL Find and Replace] regel](assets/find-and-replace.png)

### Gegevens na {#findreplace-uc-dataafter}

| Externe marketing<br/>(aangepast veld) |
|----|
| e-mailmarketing |
| e-mailmarketing |
| e-mailmarketing |
| e-mailmarketing |
| e-mailmarketing |

{style="table-layout:auto"}

+++


<!-- LOOKUP -->

### [!DNL Lookup]

Definieert een set opzoekwaarden die worden vervangen door corresponderende waarden.

+++ Details


## Invoer / Operatoren / Uitvoer {#lookup-io}

| Gegevenstype invoer | Invoer | Opgenomen operatoren | Uitvoer |
|---|---|---|---|
| <ul><li>String</li><li>Numeriek</li><li>Datum</li></ul> | <ul><li>Sing-veld</li><li>Bestand opzoeken<ul><li>Toetskolom</li><li>Nieuwe veldkolom</li></ul></li></ul> | <p>N.v.t.</p> | <p>Nieuw aangepast veld</p> |

{style="table-layout:auto"}


## Hoofdlettergebruik 1 {#lookup-uc1}

U hebt een CSV-bestand met een sleutelkolom voor `hotelID` en een of meer aanvullende kolommen met betrekking tot de `hotelID`: `city`, `rooms`, `hotel name`.
U verzamelt Hotel-id in een dimensie, maar u wilt een dimensie Hotel-naam maken die is afgeleid van de `hotelID` in het CSV-bestand.

**CSV-bestandsstructuur en -inhoud**

| hotelID | stad | kamers | hotelnaam |
|---|---|---:|---|
| SLC123 | Salt Lake City | 40 | SLC Downtown |
| LAX342 | Los Angels | 60 | Luchthaven LA |
| SFO456 | San Francisco | 75 | Market Street |

{style="table-layout:auto"}

**Huidig rapport**

| Hotel-id | Productweergaven |
|---|---:|
| SLC123 | 200 |
| LX342 | 198 |
| SFO456 | 190 |

{style="table-layout:auto"}


**Gewenst rapport**

| Hotelnaam | Productweergaven |
|----|----:|
| SLC Downtown | 200 |
| Luchthaven LA | 198 |
| Market Street | 190 |

{style="table-layout:auto"}

### Gegevens voor {#lookup-uc1-databefore}

| Hotel-id |
|----|
| SLC123 |
| LAX342 |
| SFO456 |

{style="table-layout:auto"}


### Aangepast veld {#lookup-uc1-customfield}

U definieert een `Hotel Name` aangepast veld. U gebruikt de **[!UICONTROL ** VERGRENDELEN **]** functie om een regel te definiëren waarin u waarden van de **[!UICONTROL ** Hotel-id **]** veld en vervangen door nieuwe waarden.

![[!DNL Lookup] regel 1](assets/lookup-1.png)

### Gegevens na {#lookup-uc1-dataafter}

| Hotelnaam |
|----|
| SLC Downtown |
| Luchthaven LA |
| Market Street |

{style="table-layout:auto"}


## Hoofdlettergebruik 2 {#lookup-uc2}

U hebt URL&#39;s verzameld in plaats van de vriendelijke paginanaam voor verschillende pagina&#39;s. Deze gemengde verzameling van waarden breekt de rapportage af.

### Gegevens voor {#lookup-uc2-databefore}

| Paginanaam |
|---|
| Startpagina |
| Zoeken in vliegen |
| `http://www.adobetravel.ca/Hotel-Search` |
| `https://www.adobetravel.com/Package-Search` |
| Handelingen en aanbiedingen |
| `http://www.adobetravel.ca/user/reviews` |
| `https://www.adobetravel.com.br/Generate-Quote/preview` |

{style="table-layout:auto"}

### Aangepast veld {#lookup-uc2-customfield}

U definieert een `Page Name (updated)` aangepast veld. U gebruikt de **[!UICONTROL ** VERGRENDELEN **]** functie om een regel te definiëren waarin u waarden van uw bestaande **[!UICONTROL ** Paginanaam **]** veld en vervangen door bijgewerkte correcte waarden.

![[!DNL Lookup] regel 2](assets/lookup-2.png)

### Gegevens na {#lookup-uc2-dataafter}

| Paginanaam (bijgewerkt) |
|---|
| Startpagina |
| Zoeken in vliegen |
| Hotel zoeken |
| Pakket zoeken |
| Handelingen en aanbiedingen |
| Revisies |
| Offerte genereren |

+++

<!-- URL PARSE -->

### [!DNL URL Parse]

Hiermee worden verschillende delen van een URL uitgeparseerd, zoals protocol-, host-, pad- of queryparameters.

+++ Details

## Invoer / Operatoren / Uitvoer {#urlparse-io}

| Gegevenstype invoer | Invoer | Opgenomen operatoren | Uitvoer |
|---|---|---|---|
| <ul><li>String</li></ul> | <ul><li>Sing-veld</li><li>Parseren, optie<ul><li>Protocol ophalen</li><li>Host ophalen</li><li>Pad ophalen</li><li>Query-waarde ophalen<ul><li>Query-param</li></ul></li><li>Hashwaarde ophalen</li></ul></li></ul></li></ul> | <p>N.v.t.</p> | <p>Nieuw aangepast veld</p> |

{style="table-layout:auto"}


## Hoofdlettergebruik 1 {#urlparse-uc1}

U wilt het verwijzende domein van verwijzende URL als deel van de reeks van regels van een marketingkanaal slechts gebruiken.

### Gegevens voor {#urlparse-uc1-databefore}

| URL verwijzen |
|----|
| `https://www.google.com/` |
| `https://duckduckgo.com/` |
| `https://t.co/` |
| `https://l.facebook.com/` |

{style="table-layout:auto"}

### Aangepast veld {#urlparse-uc1-customfield}

U definieert een  `Referring Domain` aangepast veld. U gebruikt de **[!UICONTROL ** URL-PARSE **]** functie om een regel te bepalen om de gastheer van te halen **URL verwijzen** en sla dat op in het nieuwe aangepaste veld.

![[!DNL Url Parse] regel 1](assets/url-parse-1.png)

### Gegevens na {#urlparse-uc1-dataafter}

| Referentiedomein |
|----|
| www.google.com |
| duckduckgo.com |
| t.co |
| l.facebook.com |

{style="table-layout:auto"}


## Hoofdlettergebruik 2 {#urlparse-uc2}

U wilt de waarde van `cid` parameter van een vraagkoord in een Pagina URL als deel van de output van een afgeleid het volgen coderapport.

### Gegevens voor {#urlparse-uc2-databefore}

| Pagina-URL |
|----|
| `https://www.adobe.com/?cid=abc123` |
| `https://www.adobe.com/?em=email1234&cid=def123` |
| `https://www.adobe.com/landingpage?querystring1=test&test2=1234&cid=xyz123` |

{style="table-layout:auto"}

### Aangepast veld {#urlparse-uc2-customfield}

U definieert een `Query String CID` aangepast veld. U gebruikt de **[!UICONTROL ** URL-PARSE **]** functie om een regel te bepalen om de waarde van de parameter van het vraagkoord in de Pagina URL te halen, specificerend `cid` als de queryparameter. De uitvoerwaarde wordt opgeslagen in het nieuwe aangepaste veld.

![[!DNL Url Parse] regel 2](assets/url-parse-2.png)

### Gegevens na {#urlparse-uc2-dataafter}

| Query String CID |
|----|
| abc123 |
| def123 |
| xyz123 |

{style="table-layout:auto"}

+++