---
description: De Berekende Bouwer van Metriek verstrekt een canvas om Dimensionen, Metriek, Filters, en Functies te slepen en te laten vallen om douanemetriek tot stand te brengen die op containerhiërarchische logica, regels, en exploitanten wordt gebaseerd. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige berekende metriek of complexe, berekende metriek bouwen en opslaan.
title: Metrische gegevens samenstellen
feature: Calculated Metrics
exl-id: 4d03a51d-c676-483c-98e2-d7283e8d71b0
source-git-commit: 7cdd81c9e38219d2d17decd5b9c3e987b814fc53
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 0%

---

# Metrische gegevens samenstellen

Customer Journey Analytics biedt een canvas voor het slepen en neerzetten van dimensies, metriek, filters en functies om aangepaste metrische gegevens te maken op basis van logica in de containerhiërarchie, regels en operatoren. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige berekende metriek of complexe, berekende metriek bouwen en opslaan.

## Beginnen met het bouwen van een berekende metrische waarde

U kunt de berekende metrische bouwer gebruiken om berekende metriek tot stand te brengen. Wanneer gecreeerd op deze manier, zijn de berekende metriek beschikbaar in de componentenlijst en kunnen dan in projecten door uw organisatie worden gebruikt. Alternatief, kunt u snel berekende metrisch tot stand brengen, zoals die in [ wordt beschreven creeer berekende metriek voor één enkel project ](/help/components/apply-create-metrics.md#create-calculated-metrics-for-a-single-project) in [ Metriek ](/help/components/apply-create-metrics.md).

Heb toegang tot de berekende metrische bouwer beginnen creërend berekende metrisch die in de componentenlijst beschikbaar is.

1. Heb toegang tot de berekende metrische bouwer op om het even welke volgende manieren:

   * Open in Analysis Workspace een project en selecteer vervolgens **[!UICONTROL Components]** > **[!UICONTROL Create metric]** .
   * In Analysis Workspace, open een project, dan selecteer **plus** pictogram naast de [!UICONTROL **sectie van Metriek**] in de linkerspoorlijn.
   * Ga in [!DNL Customer Journey Analytics] naar **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]** en selecteer vervolgens **[!UICONTROL + Add]** boven aan de pagina Berekende meetgegevens.

1. Ga met [ Gebieden van de berekende metrische bouwer ](#areas-of-the-calculated-metrics-builder) verder.

## Gebieden van de berekende metriebouwer

<!-- 

>[!CONTEXTUALHELP]
>id="cja_journeycanvas_viz_product_compatibility"
>title="Product compatibility"
>abstract="Indicates where in Customer Journey Analytics this calculated metric can be used, such as in Analysis Workspace, Report Builder, and so forth."  
>"Some calculated metrics cannot be used with experimentation. Calculated metrics that are not compatible with experimentation have the following value: "Everywhere in Customer Journey Analytics (excluding experimentation)" "
>"Various factors affect whether a calculated metric is compatible with experimentation. Learn more (https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation#use-in-experimentation) ."
>additional-url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation#use-in-experimentation" text="Use calculated metrics in experimentation"

-->

In de volgende afbeelding en de bijbehorende tabel worden enkele hoofdgebieden en kenmerken van de builder van berekende metriek uitgelegd.

![ Nieuw berekend metriekvenster dat belangrijkste die gebieden en eigenschappen toont in deze sectie worden beschreven.](assets/cm_builder_ui.png)

| Veld | Beschrijving |
| --- | --- |
| Titel | De naam van de metrische waarde is verplicht. U kunt metrisch opslaan tenzij het wordt genoemd. |
| Beschrijving | Geef het een gebruikersvriendelijke beschrijving om te tonen waarvoor het wordt gebruikt en het van gelijkaardige degenen te onderscheiden. <p>De beschrijving wordt ook weergegeven in een rapport. Het is beter NIET om de formule in de beschrijving te zetten - in plaats daarvan, beschrijf wat deze metrisch zou moeten en niet zouden moeten worden gebruikt. (De formule wordt geproduceerd aangezien u metrisch bouwt, onder de Summiere rubriek. Dientengevolge, is het niet nodig om de formule aan de beschrijving toe te voegen.) </p> |
| Indeling | U kunt kiezen uit Decimaal, Tijd, Percentage en Valuta. |
| Decimalen | Toont hoeveel decimalen in het rapport zullen worden getoond. Het maximumaantal decimalen dat u kunt opgeven is 10. |
| Naar boven trends tonen als... | Deze metrische polariteit die toont of de Analyse een stijgende trend in metrisch als goed (groen) of slecht (rood) zou moeten beschouwen. Als gevolg hiervan zal de grafiek van het rapport als groen of rood worden weergegeven wanneer het omhoog gaat. |
| Valuta | De basisvaluta voor deze gegevensweergave. |
| Tags | Tags zijn een goede manier om metriek in te delen. Alle gebruikers kunnen tags maken en een of meer tags toepassen op een metrische waarde. U kunt echter alleen tags zien voor de filters die u bezit of die met u zijn gedeeld. Welke soorten markeringen moet u creëren? Hier volgen enkele suggesties voor handige tags:<ul><li>{de namen van 0} Team **, zoals Sociale Marketing, Mobiele Marketing.**</li><li>**Projecten** (analysetags), zoals ingang-pagina analyse.</li><li>**Categorieën**, zoals Vrouwen; Geografie.</li><li>**Werkschema&#39;s**, zoals om worden goedgekeurd; Gekruld voor (een specifieke bedrijfseenheid)</li></ul> |
| Samenvatting | <p>De Summiere formule werkt op elk ogenblik bij u een verandering in de metrische definitie aanbrengt. Deze formule wordt ook weergegeven in de metrische rail links als u de muisaanwijzer boven een metrische waarde houdt en op de knop <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" id="image_BDA0EAF89C19440CB02AE248BA3F968E" /> pictogram. </p> |
| Definitie | Dit is waar u in metriek/berekende metriek, filters, en/of functies sleept om berekende metrisch te bouwen. <ul><li>Als u in berekende metrisch sleept, zal het zijn metrische definitie automatisch uitbreiden. </li> <li>U kunt definities nesten met containers. In tegenstelling tot filtercontainers werken deze containers echter als een wiskundige expressie en bepalen ze de volgorde van bewerkingen. </li> </ul> |
| Operator | Gedeeld door ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Divide_18_N.svg" width="15" id="image_320D7363DE024BDEB21E44606C8B367F" width="25px" /> ) is de standaardoperator, plus de operatoren +, - en x. |
| Voorvertoning | Hiermee kunt u snel informatie lezen over mogelijke fouten. De voorvertoning beslaat de laatste 90 dagen. Dit is een manier om aanvankelijk te graven of u de juiste componenten voor uw metrisch hebt geselecteerd. Een onverwacht resultaat zou betekenen u een tweede blik bij de metrische definitie moet nemen. |
| Productcompatibiliteit | Geeft aan waar in de Customer Journey Analytics deze berekende metrische waarde kan worden gebruikt. <p>De mogelijke waarden zijn:</p><ul><li>[!UICONTROL **overal in Customer Journey Analytics**]: Berekende metrisch kan door alle Customer Journey Analytics, met inbegrip van Analysis Workspace, Report Builder, etc. worden gebruikt.</li><li>[!UICONTROL **overal in Customer Journey Analytics (exclusief experimenteren)**]: Berekende metrisch kan door alle Customer Journey Analytics, behalve in het paneel van de Experimentatie worden gebruikt.</li> <p>Voor informatie over de criteria die bepalen of berekende metrisch met experimenteren kan worden gebruikt, zie [ Berekende metriek van het Gebruik in het paneel van de Experimentatie ](/help/analysis-workspace/c-panels/experimentation.md#use-calculated-metrics-in-the-experimentation-panel) in [ het paneel van de Experimentatie ](/help/analysis-workspace/c-panels/experimentation.md).</p></ul> |
| Toevoegen | Voor alle soorten berekende metriek, kunt u containers en statische aantallen aan de definitie toevoegen. Voor geavanceerde berekende metriek, kunt u filters en functies ook toevoegen.<ul><li>Containers werken als een wiskundige expressie en bepalen de volgorde van bewerkingen. Dus alles in een container wordt verwerkt voor de volgende bewerking.</li><li>Wanneer u een filter naar een container sleept, wordt alles in die container gefilterd. (Alleen geavanceerde berekende cijfers)</li><li>U kunt meerdere filters in een container stapelen.</li></ul> |
| Pictogram tandwiel (metrisch type, kenmerk) | Als u het tandwielpictogram naast een metrische waarde selecteert, kunt u het metrische type en de kenmerkmodellen opgeven. <p>**Nota:** overweeg het volgende wanneer het bijwerken van de attributie van een component aan een niet-gebrek attributiemodel:</p><ul><li>**wanneer het gebruiken van de component in een rapport met *één enkele afmeting*:** de attributie van de component negeert het toewijzingsmodel wanneer een niet-gebrek attributiemodel wordt gebruikt.</li><li>**wanneer het gebruiken van de component in een rapport met *veelvoudige afmetingen*:** de attributie van de component behoudt het toewijzingsmodel wanneer een niet-gebrek attributiemodel wordt gebruikt.</li><li>De veelvoudige afmetingen zijn beschikbaar slechts wanneer [ het uitvoeren van gegevens aan de wolk ](/help/analysis-workspace/export/export-cloud.md).</li></ul> <p>Voor meer informatie over toewijzing, zie {de montages van de componenten van 0} Persistence ](/help/data-views/component-settings/persistence.md).[</p> |
| Plus (+)-pictogram | Hiermee kunt u een nieuwe component maken, zoals een nieuw filter (waarmee u naar de Filterbouwer gaat). |
| Componenten zoeken | Met deze zoekbalk kunt u zoeken naar afmetingen, metriek, filters (alleen geavanceerde berekende meetgegevens) en functies (alleen geavanceerde berekende meetgegevens). |
| Lijst van Dimensionen | In plaats van de berekende metrische bouwer te verlaten om een eenvoudig filter (in de Bouwer van de Filter), b.v. &quot;Pagina = Homepage&quot;te bouwen, kunt u in Pagina slepen en Homepage direct van de berekende metrische bouwer selecteren. Dit resulteert in een veel gestroomlijnder werkschema voor het creëren van gefilterde berekende metriek. |
| Lijst met meetwaarden | De cijfers zijn ingedeeld in drie categorieën:<ul><li>Standaardwaarden</li><li>Berekende cijfers</li><li>Metrische sjablonen - onder aan de lijst.</li></ul>Wanneer u de cursor boven een metrische waarde houdt, ziet u het pictogram Info rechts ervan. Als u op dit pictogram klikt, krijgt u de volgende informatie:<ul><li>De formule van hoe het wordt berekend.</li><li>Een voorproeftrend van metrisch.</li><li>Een bewerkingspictogram (potlood) rechtsboven dat u naar de berekende metrische builder brengt waar u deze berekende metrische waarde kunt bewerken.</li></ul> |
| Lijst met filters | (Alleen Geavanceerde berekende metriek) Als beheerder worden in deze lijst alle filters weergegeven die in uw aanmeldingsbedrijf zijn gemaakt. Als u een gebruiker niet-Admin bent, toont deze lijst filters u bezit en die met u worden gedeeld. |
| Lijst met functies | (Alleen geavanceerde berekende metriek) Functies zijn verdeeld in twee lijsten: Standaard (het meest gebruikt) en Geavanceerd. |
| Selector gegevensweergave | Met deze kiezer (rechtsboven) kunt u overschakelen naar een andere gegevensweergave. |
