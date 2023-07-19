---
description: De filterontwikkelaar biedt een canvas voor het slepen en neerzetten van metrische Dimension, filters en gebeurtenissen om personen te filteren op basis van containerhiërarchische logica, regels en operatoren. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige of complexe filters maken en opslaan waarmee u persoonlijke kenmerken en handelingen kunt identificeren voor bezoeken en gebeurtenissen.
title: Filters maken
feature: Filters
exl-id: 2107f301-4137-4e97-9aa7-07824b842e16
source-git-commit: d045ecf73f7e15940510b764814fb853222e88cc
workflow-type: tm+mt
source-wordcount: '1295'
ht-degree: 1%

---

# Filter builder

De [!UICONTROL Filter builder] Hiermee kunt u eenvoudige of complexe filters maken waarmee u persoonlijke kenmerken en handelingen kunt identificeren voor bezoeken en gebeurtenissen. Het verstrekt een canvas om metrische afmetingen, gebeurtenissen, of andere filters te slepen en te laten vallen om personen te filtreren die op hiërarchische logica, regels, en exploitanten worden gebaseerd.

Voor informatie over hoe u snelle filters kunt maken die alleen van toepassing zijn op het project waar ze zijn gemaakt, raadpleegt u [Snelle filters](/help/components/filters/quick-filters.md).

## Toegang krijgen tot de constructor Filter

U kunt tot de Bouwer van de Filter op om het even welke volgende manieren toegang hebben:

* **Bovenste navigatie**: Klikken **[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Filters]**.
* **[!UICONTROL Analysis Workspace]**: Open een project in Analysis Workspace en selecteer **[!UICONTROL + Components]** > **[!UICONTROL Create filter]**.
* **[!UICONTROL Report Builder]**: [Werken met filters in Report Builder](/help/report-builder/work-with-filters.md).

## Overzicht van Builder-criteria {#section_F61C4268A5974C788629399ADE1E6E7C}

U kunt regeldefinities en containers toevoegen om uw filters te definiëren. (Voor informatie over de toegang tot van de Bouwer van de Filter, zie [Toegang krijgen tot de constructor Filter](#access-the-filter-builder).)

![](assets/segment_builder_ui_2.png)

1. **[!UICONTROL Title]**: Geef het filter een naam.
1. **[!UICONTROL Description]**: Geef een beschrijving voor het filter op.
1. **[!UICONTROL Tags]**: [Codeer het filter](/help/components/filters/manage-filters.md) u maakt door tags te kiezen uit een lijst met bestaande tags of door een nieuwe tag te maken.
1. **[!UICONTROL Definitions]**: Dit is waar u [filters maken en configureren](/help/components/filters/filters-overview.md), voegt regels toe en nest- en reekscontainers.
1. **[!UICONTROL Show]**: (Selector bovenste container.) Hiermee kunt u het bovenste niveau selecteren [container](/help/components/filters/filters-overview.md) ( [!UICONTROL Person], [!UICONTROL Session], [!UICONTROL Event]). De standaard container op hoofdniveau is de Event-container.
1. **[!UICONTROL Options]**: (tandwiel) pictogram

   * **[!UICONTROL + Add container]**: Hiermee kunt u een nieuwe container (onder de container op het hoogste niveau) toevoegen aan de filterdefinitie.
   * **[!UICONTROL Exclude]**: Hiermee kunt u het filter definiëren door een of meer afmetingen, filters of metriek uit te sluiten.

1. **[!UICONTROL Dimensions]**: Componenten worden uit de lijst Dimension gesleept en verwijderd (oranje zijbalk).
1. **[!UICONTROL Operator]**: U kunt waarden vergelijken en beperken gebruikend geselecteerde exploitanten.
1. **[!UICONTROL Value]**: De waarde die u hebt ingevoerd of geselecteerd voor de afmeting of het filter of de metrische waarde.
1. **[!UICONTROL Attribution Models]**: Deze modellen zijn alleen beschikbaar voor afmetingen en bepalen op welke waarden in een dimensie moet worden gefilterd. Dimension-modellen zijn vooral handig bij opeenvolgende filters.

   * **[!UICONTROL Repeating]** (standaard): Bevat varianten en doorlopende waarden voor de dimensie.
   * **[!UICONTROL Instance]**: Bevat exemplaren voor de dimensie.
   * **[!UICONTROL Non-repeating instance]**: Hiermee worden unieke (niet-herhalende) instanties voor de dimensie opgenomen. Dit is het model dat wordt toegepast in Flow wanneer herhaalde instanties worden uitgesloten.

   ![](assets/attribution-models.jpg)

   **Voorbeeld: Gebeurtenisfilter waarbij eVar1 = A**

   | Voorbeeld | A | A | A (blijft bestaan) | B | A | C |
   |---|---|---|---|---|---|---|
   | Herhalend | X | X | X | - | X | - |
   | Instance | X | X | - | - | X | - |
   | Niet-herhalende instantie | X | - | - | - | X | - |
1. **[!UICONTROL And/Or/Then]**: Wijst het [!UICONTROL AND/OR/THEN] operatoren tussen containers of regels. Met de operator THEN kunt u [opeenvolgende filters definiëren](/help/components/filters/filters-overview.md).
1. **[!UICONTROL Metric]**: (Groene zijbalk) Metrisch die is gesleept en verwijderd uit de lijst Metriek.
1. **[!UICONTROL Comparison]** operator: U kunt waarden vergelijken en beperken gebruikend geselecteerde exploitanten.
1. **[!UICONTROL Value]**: De waarde die u hebt ingevoerd of geselecteerd voor de afmeting of het filter of de metrische waarde.
1. **[!UICONTROL X]**: (Verwijderen) Hiermee kunt u dit deel van de filterdefinitie verwijderen.
1. **[!UICONTROL Experience Cloud publishing]**: Als u een Adobe Analytics-filter publiceert naar de Experience Cloud, kunt u het filter voor marketingactiviteiten gebruiken in [!DNL Audience Manager] en in andere activeringskanalen. [Meer informatie...](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html)
1. **[!UICONTROL Audience library]**: Personeelsservices beheren de vertaling van personeels-filters. Daarom lijkt het op het maken en beheren van soorten publiek op het maken en gebruiken van filters, met de extra mogelijkheid om het publieksfilter te delen met de Experience Cloud. [Meer informatie...](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html)
1. **[!UICONTROL Search]**: Hiermee doorzoekt u de lijst met afmetingen, filters of metriek.
1. **[!UICONTROL Dimensions]**: (Lijst) Klik de kopbal om uit te breiden.
1. **[!UICONTROL Metrics]**: Klik op de koptekst om deze uit te vouwen.
1. **[!UICONTROL Filters]**: Klik op de koptekst om deze uit te vouwen.
1. **[!UICONTROL Data View selector]**: Hiermee selecteert u de rapportsuite waarin dit filter wordt opgeslagen. U kunt het filter nog steeds in alle gegevensweergaven gebruiken.
1. **[!UICONTROL Filter Preview]**: Hiermee kunt u een voorvertoning van de belangrijkste meetgegevens weergeven om te zien of u een geldig filter hebt en hoe breed het filter is. Vertegenwoordigt de verdeling van de dataset u kunt verwachten om te zien of past u dit filter toe. Toont 3 concentrische cirkels en een lijst om het aantal en het percentage gelijken voor te tonen [!UICONTROL Event], [!UICONTROL Person], en [!UICONTROL Session] voor een filter dat tegen een dataset wordt uitgevoerd. Dit diagram wordt direct bijgewerkt nadat u de filterdefinitie hebt gemaakt of gewijzigd.
1. **[!UICONTROL Product Compatibility]**: Bevat een lijst met Adobe Analytics-producten (Analysis Workspace, [!UICONTROL Reports & Analytics], Data Warehouse) waarmee het filter dat u hebt gemaakt compatibel is. De meeste filters zijn compatibel met alle producten. Niet alle operatoren en dimensies zijn echter compatibel met alle analytische producten, met name [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segment-reference/seg-compatibility.html). Dit diagram wordt direct bijgewerkt nadat u wijzigingen in de filterdefinitie hebt aangebracht.
1. **[!UICONTROL Save]** of **[!UICONTROL Cancel]**: Hiermee slaat u het filter op of annuleert u het. Na klikken **[!UICONTROL Save]**, gaat u naar Filterbeheer waar u het filter kunt beheren.

Filters met ingesloten datumbereiken werken in Analysis Workspace nog steeds anders dan [!UICONTROL Reports & Analytics]: In Workspace overschrijft een filter met een ingesloten datumbereik het datumbereik van het deelvenster. Daarentegen [!UICONTROL Reports & Analytics] geeft u de doorsnede van de waaier van de rapportdatum en de ingebedde de datumwaaier van de filter.

## Een filter maken {#build-filters}

1. U sleept gewoon een Dimension-, filter- of metrische gebeurtenis van het linkerdeelvenster naar het deelvenster [!UICONTROL Definitions] veld.

   ![](assets/drag_n_drop_dimension.png)

1. Stel de [operator](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segment-reference/seg-operators.html) in het keuzemenu.
1. Voer een waarde in voor het geselecteerde item of selecteer een waarde.
1. Voeg indien nodig extra containers toe met **[!UICONTROL And]**, **[!UICONTROL Or]**, of **[!UICONTROL Then]** regels.
1. Nadat u de containers hebt geplaatst en de regels hebt ingesteld, raadpleegt u de resultaten van het filter in het validatieschema rechtsboven. De validator geeft het percentage en het absolute aantal paginaweergaven, bezoeken en unieke personen aan die overeenkomen met het filter dat u hebt gemaakt.
1. Onder **[!UICONTROL Tags]**, [tag](/help/components/filters/manage-filters.md) de container door een bestaande tag te selecteren of een nieuwe tag te maken.
1. Klikken **[!UICONTROL Save]** om het filter op te slaan.

   U wordt naar de [Filterbeheer](/help/components/filters/manage-filters.md), waar u uw filter op meerdere manieren kunt labelen, delen en beheren.

## Containers toevoegen {#section_1C38F15703B44474B0718CEF06639EFD}

U kunt [een kader van containers opbouwen](/help/components/filters/filters-overview.md) en plaatst u vervolgens tussen logische regels en operatoren.

1. Klik op **[!UICONTROL Options > Add container]**.

   Een nieuwe [!UICONTROL **Gebeurtenis**] container wordt geopend zonder [!UICONTROL **Gebeurtenis**] (Paginaweergave) geïdentificeerd.

   ![](assets/new_container.png)

1. Wijzig desgewenst het containertype.
1. Sleep een Dimension, filter of gebeurtenis van het linkerdeelvenster naar de container.
1. Doorgaan met het toevoegen van nieuwe containers van het hoogste niveau **[!UICONTROL Options]** > **[!UICONTROL Add container]** boven aan de definitie of voeg containers vanuit een container toe om logica te nesten.

   **OF**

   Selecteer een of meer regels en klik op **[!UICONTROL Options]** > **[!UICONTROL Add container from selection]**. Hierdoor verandert uw selectie in een aparte container.

## Datumbereiken gebruiken {#concept_252A83D43B6F4A4EBAB55F08AB2A1ACE}

U kunt filters bouwen die het rollen datumwaaiers bevatten om vragen over aan de gang zijnde campagnes of gebeurtenissen te beantwoorden.

U kunt bijvoorbeeld eenvoudig een filter maken dat &#39;iedereen bevat die de afgelopen 60 dagen een aankoop heeft gedaan&#39;.

U maakt een Session-container en voegt de [!UICONTROL Last 60 days] tijdbereik en metrisch [!UICONTROL Orders is greater than or equal to 1], met een operator AND.

Hier volgt een video over het gebruik van roldatumbereiken in filters:

>[!VIDEO](https://video.tv.adobe.com/v/25403/?quality=12)

## Stapelfilters {#task_58140F17FFD64FF1BC30DC7B0A1B0E6D}

Het stapelen van filters werkt door de criteria in elk filter te combineren gebruikend een &quot;en&quot;exploitant, en dan het toepassen van de gecombineerde criteria. Dit kan in een project van de Werkruimte direct of in de bouwer van de Filter worden gedaan.

Als u bijvoorbeeld een filter &quot;Mobiele gebruikers&quot; en een filter &quot;geografie van de VS&quot; stapelt, worden alleen gegevens geretourneerd voor gebruikers van mobiele telefoons in de VS.

U kunt deze filters beschouwen als bouwstenen of modules die u in een filterbibliotheek kunt opnemen, zodat gebruikers deze filters naar eigen inzicht kunnen gebruiken. Op die manier kunt u het aantal benodigde filters aanzienlijk verminderen. Stel dat u 40 filters hebt:

* 20 voor gebruikers van mobiele telefoons in verschillende landen (VS_mobile, Duitsland_mobile, Frankrijk_mobile, Brazilië_mobile, enz.)
* 20 voor gebruikers van tablets in verschillende landen (US_tablet, Germany_tablet, France_tablet, Brazilië_tablet, enz.)

Door filter het stapelen te gebruiken, kunt u uw filteraantal tot 22 verminderen en hen stapelen zoals nodig. U moet de volgende filters maken:

* één filter voor mobiele gebruikers
* één filter voor tabletgebruikers
* 20 filters voor de verschillende geografische gebieden

>[!NOTE]
>
>Wanneer het stapelen van twee filters, worden zij door gebrek verbonden door een EN verklaring. Dit kan niet in een OF verklaring worden veranderd.

1. Ga naar de Filterbouwer.

1. Geef een titel en beschrijving voor het filter op.

1. Klikken **[!UICONTROL Show filters]** om de lijst met filters in de linkernavigatie weer te geven.

1. Sleep de filters die u wilt stapelen naar het canvas met filterdefinitie.

1. Selecteren [!UICONTROL **Opslaan**].

