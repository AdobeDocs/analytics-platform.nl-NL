---
description: Adobe Analytics-dashboards maken en delen
title: scorecards maken en delen
feature: Analytics Dashboards
role: User, Admin
exl-id: 12531600-7e88-4d56-a2a5-e5b346f91937
solution: Customer Journey Analytics
source-git-commit: e7e3affbc710ec4fc8d6b1d14d17feb8c556befc
workflow-type: tm+mt
source-wordcount: '2457'
ht-degree: 0%

---

# Een mobiele scorecard maken

De volgende informatie instrueert curatoren van de gegevens van Adobe Analytics over hoe te om dashboards voor uitvoerende gebruikers te vormen en te presenteren. Om te beginnen kunt u de Adobe Analytics dashboards scorecard builder video bekijken:

>[!VIDEO](https://video.tv.adobe.com/v/343458)

>[!NOTE]
>Schermafbeeldingen met scoreborden voor deze pagina zijn gemaakt vanuit de gebruikersinterface van Adobe Analytics, niet vanuit Customer Journey Analytics. De gebruikersinterface is bijna identiek.

Een Adobe Analytics-scorecard toont belangrijke gegevensvisualisaties voor uitvoerende gebruikers in een getimede lay-out, zoals hieronder getoond:

![Voorbeeldscorecard](assets/intro_scorecard.png)

Als curator van dit scorecard, kunt u de scorecard bouwer gebruiken om te vormen welke tegels op scorecard voor uw uitvoerende consument verschijnen. U configureert ook hoe de gedetailleerde weergaven, of de onderverdelingen, kunnen worden aangepast wanneer op de tegels wordt getikt. De scorecard bouwerinterface wordt hieronder getoond:

![Scorecard Builder](assets/scorecard_builder.png)

Om scorecard tot stand te brengen, moet u het volgende doen:

1. Toegang krijgen tot [!UICONTROL Blank Mobile Scorecard] sjabloon.
2. Vorm scorecard met gegevens en bewaar het.

## Toegang krijgen tot [!UICONTROL Blank Mobile Scorecard] template {#template}

U hebt toegang tot de [!UICONTROL Blank Mobile Scorecard] malplaatje of door een nieuw project, of van het menu van Hulpmiddelen te creëren.

### Een nieuw project maken {#create}

1. Open Adobe Analytics en klik op de knop **[!UICONTROL Workspace]** tab.
1. Klikken **[!UICONTROL Create project]** en selecteert u de **[!UICONTROL Blank mobile scorecard]** projectsjabloon.
1. Klik op **[!UICONTROL Create]**.

![Scorecard-sjabloon](assets/new_template.png)

### Menu Gereedschappen

1. Van de **[!UICONTROL Tools]** menu, selecteert u **[!UICONTROL Analytics dashboards (Mobile App)]**.
1. Klik in het volgende scherm op **[!UICONTROL Create new scorecard]**.

## Vorm scorecard met gegevens en bewaar het {#configure}

Om het scorecardmalplaatje uit te voeren:

1. Onder **[!UICONTROL Properties]** (in de rechtse spoorstaaf), **[!UICONTROL Project data view]** waarvan u gegevens wilt gebruiken.

   ![selectie in gegevensweergave](assets/properties_save.png)

1. Als u een nieuwe tegel aan uw scorecard wilt toevoegen, sleept u een metrische waarde vanuit het linkerdeelvenster naar het **[!UICONTROL Drag and Drop Metrics Here]** zone. U kunt ook een metrische waarde tussen twee tegels invoegen met behulp van een vergelijkbare workflow.

   ![Tegels toevoegen](assets/build_list.png)


1. Van elke tegel, kunt u tot een gedetailleerde mening toegang hebben die extra informatie over metrisch, zoals hoogste punten voor een lijst van verwante afmetingen toont.

## Afmetingen of metingen toevoegen {#dimsmetrics}

Als u een gerelateerde afmeting aan een metrische waarde wilt toevoegen, sleept u een afmeting uit het linkerdeelvenster en zet u deze op een tegel neer.

U kunt bijvoorbeeld de juiste afmetingen toevoegen (zoals **[!DNL Marketing Channel]**, in dit voorbeeld) aan de **[!UICONTROL Unique Visitors]** metrisch door het te slepen en neer te zetten op de tegel. Uitsplitsingen naar Dimension worden weergegeven onder de [!UICONTROL Drill Ins] (uitsplitsing) afdeling van de tegelspecifieke **[!UICONTROL Properties]**. U kunt meerdere afmetingen aan elke tegel toevoegen.

![Afmetingen toevoegen](assets/layer_dimensions.png)

## Filters toepassen {#filters}

Als u filters wilt toepassen op afzonderlijke tegels, sleept u een filter (segmenten zijn filters in Customer Journey Analytics) uit het linkerdeelvenster en zet u het rechtstreeks boven op de tegel neer.

Als u het filter op alle tegels in de scorecard wilt toepassen, laat vallen de tegel bovenop de scorecard. U kunt ook filters toepassen door filters te selecteren in het filtermenu onder de datumbereiken. U [vorm en pas filters voor uw scorecards toe](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/using-drop-down-filters.html) Hetzelfde als in Adobe Analytics Workspace.

![Filters maken](assets/segment_ui.png)

## Datumbereiken toevoegen {#dates}

U kunt combinaties van datumbereiken toevoegen en verwijderen die u in uw scorecard kunt selecteren door de vervolgkeuzelijst met datumbereiken te selecteren.

![Nieuwe scorekaart](assets/new_score_card.png)

Elke nieuwe scorecard begint met 6 datumwaaiercombinaties die zich op de gegevens van vandaag en gisteren concentreren. U kunt overbodige datumbereiken verwijderen door op de x te klikken of u kunt elke datumbereikcombinatie bewerken door op het potlood te klikken.

![Nieuwe scorekaart2](assets/new_score_card2.png)

Als u een primaire datum wilt maken of wijzigen, gebruikt u de vervolgkeuzelijst om een van de beschikbare datumbereiken te selecteren of sleept u een datumcomponent van de rechterrail naar de neerzetzone.

![Nieuwe scorekaart3](assets/new_score_card3.png)

Als u een vergelijkingsdatum wilt maken, kunt u een keuze maken uit handige voorinstellingen voor algemene tijdvergelijkingen in het keuzemenu. U kunt ook een datumcomponent slepen en neerzetten vanaf de rechterrail.

![Nieuwe scorekaart4](assets/new_score_card4.png)

Als het gewenste datumbereik nog niet is gemaakt, kunt u een nieuw datumbereik maken door op het kalenderpictogram te klikken.

![Nieuwe scorekaart5](assets/new_score_card5.png)

Hiermee gaat u naar de builder van het datumbereik waar u een nieuwe component voor het datumbereik kunt maken en opslaan.

### Vergelijkingsdatumbereiken tonen of verbergen {#show-comparison-dates}

Als u datumbereiken met elkaar wilt vergelijken, schakelt u het **Inclusief vergelijkingsdatums** instellen.

![Inclusief vergelijkingsdatums](assets/include-comparison-dates.png)

De instelling is *op* standaard. Omschakelen naar *uit* als u geen vergelijkingsdata wilt bekijken.

![Niet-geselecteerde vergelijkingsdatuminstelling](assets/no-comparison-dates.png)

## Visualisaties toepassen {#viz}

De dashboards van de Analyse bieden vier visualisaties die u groot inzicht in afmetingspunten en metriek geven. Schakel over naar een andere visualisatie door de optie [!UICONTROL chart type] van een tegel [!UICONTROL Properties]. Selecteer gewoon de rechtertegel en wijzig vervolgens het diagramtype.

![Tegeleigenschappen](assets/properties.png)

Of klik op de knop [!UICONTROL Visualizations] pictogram in de linkerspoorstaaf en sleep en laat vallen de juiste visualisatie op de tegel:

![Visualisaties](assets/vizs.png)

### [!UICONTROL Summary Number]

Gebruik de Summiere visualisatie van het Aantal om een groot aantal te benadrukken dat in een project belangrijk is.

![Samenvattingsnummer](assets/summary-number.png)

### [!UICONTROL Donut]

Net als bij een cirkeldiagram toont deze visualisatie gegevens als delen van een geheel. Gebruik een donutgrafiek wanneer het vergelijken van percentages van een totaal. Stel dat u wilt zien welke advertentie-platform heeft bijgedragen aan het totale aantal unieke personen:

![Donut visualisatie](assets/donut-viz.png)

### [!UICONTROL Line]

De visualisatie van de Lijn vertegenwoordigt metriek gebruikend een lijn om te tonen hoe de waarden over een periode veranderen. Een lijngrafiek toont afmetingen in tijd maar werkt met om het even welke visualisatie. U visualiseert de dimensie van de productcategorie in dit voorbeeld.

![Lijnvisualisatie](assets/line.png)

### [!UICONTROL Horizontal Bar]

Deze visualisatie toont horizontale balken die verschillende waarden over een of meer meeteenheden vertegenwoordigen. Als u bijvoorbeeld gemakkelijk wilt zien wat uw beste producten zijn, gebruikt u [!UICONTROL Horizontal Bar] voor uw voorkeursvisualisatie.

![horizontale balk](assets/horizontal.png)

### Verwijderen [!UICONTROL Unspecified] dimensie-item

Als u wilt verwijderen [!UICONTROL Unspecified] dimensiepunten van uw gegevens, doe het volgende:

1. Selecteer de juiste tegel.
1. In de rechterspoorweg, onder **[!UICONTROL Drill ins]**, selecteert u de pijl-rechts naast het dimensie-item waarvan **[!UICONTROL Unspecified]** items die u wilt verwijderen.

   ![ongespecificeerd](assets/unspecified.png)

1. Klik op het pictogram naast **[!UICONTROL Unspecified]** om niet-opgegeven gegevens uit de rapportage te verwijderen. (U kunt ook elk ander dimensie-item verwijderen.)

## Eigenschappen van tegels weergeven en configureren {#tiles}

Wanneer u op een tegel klikt in de scorecard builder, geeft de rechterspoorstaaf de eigenschappen en kenmerken weer die aan die tegel en zijn detaildia zijn gekoppeld. In deze trein kunt u een nieuwe **Titel** voor de tegel en vormt u de tegel ook door filters toe te passen. Segmenten zijn filters in Customer Journey Analytics.

![Eigenschappen, tegel](assets/properties-tile-new.png)

## Gedetailleerde dia&#39;s weergeven {#view-detail-slides}

Wanneer u op tegels klikt, wordt in een dynamisch pop-upvenster weergegeven hoe de detaildia er uitziet voor de uitvoerende gebruiker in de app. U kunt dimensies toevoegen om uw gegevens naar behoefte op te splitsen. Als er geen dimensie is toegepast, wordt de afbraakdimensie **uur** of **dagen**, afhankelijk van het standaarddatumbereik.

De onderbrekingen verfijnen uw analyse door metriek door afmetingspunten zoals het volgende te verdelen:

* Unieke Visitors, metrisch uitgesplitst naar advertentie-Platform (AMO-id)
* Bezoeken uitgesplitst naar productcategorie (detailhandel)
* Totaal ontvangsten uitgesplitst naar productnaam

![Onderverdeling_weergave](assets/break_view.png)

Elke dimensie die aan de tegel wordt toegevoegd, wordt weergegeven in een vervolgkeuzelijst in de gedetailleerde weergave van de app. De uitvoerende gebruiker kan dan uit de opties kiezen die in de drop-down lijst worden vermeld.

## Detaildia&#39;s aanpassen {#customize-detail-slide}

Met aangepaste dia&#39;s kunt u zich nog meer richten op de informatie die u deelt met uw publiek.

>[!VIDEO](https://video.tv.adobe.com/v/3410002)

U kunt de lay-out voor elke detaildia wijzigen en tekst toevoegen om beter te verklaren wat de eindgebruiker in de gegevens kan zien. U kunt het grafiektype ook veranderen gebruikend het drop-down menu.

![Aangepaste detaildia](assets/custom-detail-slide.png)

### De dialay-out wijzigen

Wijzig de dialay-out om de nadruk op de belangrijkste informatie te leggen. U kunt bijvoorbeeld de lay-out zodanig wijzigen dat alleen een grafiek of alleen een tabel wordt weergegeven. Als u de dialay-out wilt wijzigen, selecteert u een van de vooraf ontworpen indelingen.

![Schuivende indeling](assets/layout.png)

U kunt de dialay-out ook veranderen door visualiseringscomponenten van de linkerspoorstaaf op het canvas te slepen en te laten vallen. Elke detaildia kan slechts twee visualisaties tegelijk bevatten.

![Schuifregelaar](assets/slide-layout-change.png)

### Beschrijvende tekst toevoegen aan een dia

U kunt tekst toevoegen om betekenisvolle informatie te verstrekken over wat in de grafieken of nuances over de gegevens bevat.

Als u tekst wilt toevoegen aan een detaildia, selecteert u een lay-out waarin de `T` of sleep de tekstvisualisatiecomponent van de linkerspoorstaaf over. De teksteditor wordt automatisch geopend wanneer u een nieuwe tekstvisualisatie toevoegt of een dialay-out met tekst kiest. De teksteditor bevat alle standaardopties voor de opmaak van de tekst. U kunt tekststijlen toepassen, zoals alinea&#39;s, koppen en subkoppen, en vette en cursieve lettertypen toepassen. U kunt tekst uitvullen, lijsten met opsommingstekens en nummers toevoegen en koppelingen toevoegen. Wanneer u klaar bent met bewerken, selecteert u de knop Minimaliseren in de rechterbovenhoek van de teksteditor om deze te sluiten. Als u de tekst die u al hebt toegevoegd wilt bewerken, selecteert u het potloodpictogram om de teksteditor opnieuw te openen.

![Schuifregelaar](assets/add-descriptive-text.png)

## Componenten verwijderen {#remove}

Op dezelfde manier om een component te verwijderen die op volledige scorecard wordt toegepast, klik overal op de scorecard buiten de tegels en verwijder het door het te klikken **x** dat wordt weergegeven wanneer u de muisaanwijzer op de component plaatst, zoals hieronder voor de component **Eerste bezoeken**:

![Remove_components](assets/new_remove.png)

## Gegevensartikelen maken {#create-data-story}

Een gegevensverhaal is een inzameling van ondersteunende gegevenspunten, bedrijfscontext, en verwante metriek die rond een centraal thema of metrisch wordt gebouwd.

Bijvoorbeeld, als u zich op Webverkeer concentreert, kan uw belangrijkste metrisch bezoeken zijn, maar u kunt ook in nieuwe personen, unieke personen geinteresseerd zijn, en u kunt gegevens willen zien uitgesplitst door Web-pagina of door welk apparatentype het verkeer uit komt. Met gegevensartikelen in mobiele scorecardprojecten kunt u uw belangrijkste metriek vooraan en centraal plaatsen en het hele verhaal achter de metriek vertellen met meerdere detaildia&#39;s.

Bekijk de video voor meer informatie over het maken van gegevensverhalen in mobiele scorecardprojecten in Analysis Workspace.

>[!VIDEO](https://video.tv.adobe.com/v/3416392/?quality=12&learn=on)

**Een gegevensartikel maken** {#data-story-create}

Bouw uw gegevensverhaal door veelvoudige detaildia&#39;s aan een tegel toe te voegen.

1. Begin met een mobiel scorecardproject.
1. Selecteer een tegel waarvan u een artikel wilt maken.
   ![Een gegevensartikel maken](assets/data-story1.png)
   ![Pictogrammen voor gegevensartikelen maken](assets/create-data-story.png){width=".50%"}
1. Voeg dia&#39;s toe om uw gegevensverhaal te bouwen. De eerste dia wordt standaard gegenereerd.
Als u nieuwe dia&#39;s wilt toevoegen, houdt u de muisaanwijzer boven een dia of klikt u op een dia en selecteert u een van de beschikbare opties:
   * Tik op + om een nieuwe dia te maken.
   * Tik op het dubbele pictogram om de bestaande dia te dupliceren.
1. Als u een lege dia maakt, sleept u componenten vanuit de linkerrail en zet u de component neer. U kunt ook een lay-out kiezen om de dia automatisch te vullen met de gegevens uit de tegel.
   ![Een gegevensartikel maken](assets/data-story2.png)
Tik op het prullenbakpictogram om een dia te verwijderen.

### Een gegevensartikel aanpassen {#customize-data-story}

Met gegevensartikelen kunt u alles aanpassen, zodat u informatie kunt delen die u wilt delen en alles kunt uitsluiten wat u niet nodig hebt. U kunt tegels en afzonderlijke dia&#39;s aanpassen om filters toe te voegen, onderverdelingen weer te geven, de lay-out te wijzigen en de visualisatie te wijzigen.

**Tegels aanpassen**

1. Tik op een tegel. De geselecteerde tegel krijgt een blauwe omtrek en de eigenschappen Naast elkaar staan in het rechterdeelvenster.
1. Wijzig de titel, het diagramtype en andere tegelopties.
1. Sleep een component naar de tegel.
   ![Een gegevensartikel maken](assets/data-story3.png)
Wanneer u een component, zoals een visualisatie, naar een tegel sleept, wordt de component toegepast op alle dia&#39;s met gegevensartikelen.
1. Als u een wijziging alleen op de titel wilt toepassen, houdt u Shift ingedrukt om de wijziging toe te passen.
   ![Een gegevensartikel maken](assets/data-story4.png)

>[!NOTE]
>Dia&#39;s nemen componenten van de tegel over, maar tegels nemen geen componenten van dia&#39;s over.

**Afzonderlijke dia&#39;s aanpassen**

U kunt de visualisatie voor afzonderlijke dia&#39;s in een gegevensartikel wijzigen. U kunt bijvoorbeeld een horizontale balk wijzigen in een donutgrafiek voor een bepaalde dia. U kunt ook de lay-out wijzigen. Zie [Detaildia&#39;s aanpassen](#customize-detail-slide).

### Een gegevensartikel voorvertonen {#preview-data-story}

Nadat u een gegevensartikel hebt gemaakt, gebruikt u de opdracht **Voorvertoning** om een gegevensartikel weer te geven en te interageren alsof u een app-gebruiker bent. Voor informatie over het voorvertonen van uw gegevensartikel raadpleegt u [Een voorvertoning van een scorecard weergeven](#preview)

### Navigeren tussen tegels en dia&#39;s {#navigate-tiles-slides}

Op de navigatiebalk worden pictogrammen weergegeven die aangeven wat er op elke dia staat. Met de navigatiebalk kunt u gemakkelijk naar een bepaalde dia navigeren als u veel dia&#39;s hebt.

Tik op de navigatiebalk om te schakelen tussen de tegel en de dia&#39;s.
![Een gegevensartikel maken](assets/data-story5.png)
![Een gegevensartikel maken](assets/data-story-nav.png){width="45%"}

U kunt ook heen en weer navigeren met de pijlen op het toetsenbord of door een component te selecteren en deze links of rechts van het scherm te houden om te schuiven.

## Voorvertoning scorecards {#preview}

U kunt voorvertonen hoe de scorecard eruitziet en functioneert zodra deze is gepubliceerd in de app Analytics-dashboards.

1. Klikken **[!UICONTROL Preview]** in de rechterbovenhoek van het scherm.

   ![Preview_scorecards](assets/preview.png)

1. Als u wilt zien hoe de scorecard er op verschillende apparaten uitziet, selecteert u een apparaat in het menu [!UICONTROL Device preview] vervolgkeuzemenu.

   ![Apparaat_voorvertoning](assets/device-preview.png)

1. Als u met de voorvertoning wilt werken, kunt u:

   * Klik met de linkermuisknop om tikken op het telefoonscherm te simuleren.

   * Gebruik de schuiffunctie van uw computer om het schuiven door het telefoonscherm met uw vinger te simuleren.

   * Klik en houd vast om het drukken en het houden van uw vinger op het telefoonscherm te simuleren. Dit is handig voor interactie met de visualisaties in de gedetailleerde weergave.

## Naamscorecards {#name}

Als u de scorecard een naam wilt geven, klikt u op de naamruimte linksboven in het scherm en typt u de nieuwe naam.

![Naming_Scorecards](assets/new_name.png)

## Scorecards delen {#share}

De scorecard delen met een Executive-gebruiker:

1. Klik op de knop **[!UICONTROL Share]** en selecteert u **[!UICONTROL Share scorecard]**.

1. In de **[!UICONTROL Share Mobile Scorecard]** de velden invullen met:

   * De naam van de scorecard opgeven
   * Een beschrijving van de scorecard
   * Relatieve tags toevoegen
   * Het specificeren van de ontvangers voor scorecard

1. Klik op **[!UICONTROL Share]**.

![Share_Scorecards](assets/new_share.png)

Nadat u een scorecard hebt gedeeld, kunnen uw ontvangers tot het op hun dashboards van Analytics toegang hebben. Als u verdere veranderingen in scorecard in de scorecard bouwer aanbrengt, zullen zij automatisch in gedeelde scorecard worden bijgewerkt. De uitvoerende gebruikers zullen dan de veranderingen zien nadat het scorecard op hun app verfrist.

Als u scorecard door nieuwe componenten bij te voegen bijwerkt, kunt u de scorecard opnieuw willen delen (en controle **[!UICONTROL Share embedded components]** ) om ervoor te zorgen dat uw uitvoerende gebruikers toegang tot deze veranderingen hebben.

### Schrappingskaarten delen met behulp van een deelbare koppeling

Met een deelbare koppeling kunt u eenvoudig een scorecard delen in een e-mail-, document- of tekstbericht-app. Met de link shareable kunnen ontvangers de scorecard openen op hun bureaublad of in de mobiele app dashboards. Dankzij de deelbare diepe koppeling is het nog eenvoudiger om projecten te delen en de betrokkenheid bij uw belanghebbenden te versterken.

Een scorecard delen met behulp van een shareable-koppeling

1. Klik op de knop **[!UICONTROL Share]** en selecteert u **[!UICONTROL Share scorecard]**.

   ![Share_Scorecards](assets/share-scorecard.png)

1. Kopieer de koppeling en plak deze in een e-mail-, document- of IM-app.

   Wanneer een ontvanger een bureaubladtoepassing of browser gebruikt om de koppeling te openen, wordt het mobiele scorecard-project geopend in Workspace.

   Wanneer een ontvanger de koppeling op een mobiel apparaat opent, wordt de scorecard rechtstreeks geopend in de app Analytics-dashboards.

   Als een ontvanger de mobiele app niet heeft gedownload, wordt hij of zij verwezen naar de app-aanbieding in de App Store of Google Play Store waar hij of zij deze kan downloaden.

