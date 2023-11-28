---
description: De Berekende Bouwer van Metriek verstrekt een canvas om Dimensionen, Metriek, Filters, en Functies te slepen en te laten vallen om douanemetriek tot stand te brengen die op containerhiërarchische logica, regels, en exploitanten wordt gebaseerd. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige berekende metriek of complexe, berekende metriek bouwen en opslaan.
title: Cijfers samenstellen
feature: Calculated Metrics
exl-id: 4d03a51d-c676-483c-98e2-d7283e8d71b0
source-git-commit: c343a729de4cb13473a7acc04e837b5e5f69809b
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 0%

---

# Metrische gegevens samenstellen

Customer Journey Analytics biedt een canvas voor het slepen en neerzetten van dimensies, metriek, filters en functies om aangepaste metrische gegevens te maken op basis van logica in de containerhiërarchie, regels en operatoren. Met dit geïntegreerde ontwikkelingshulpmiddel kunt u eenvoudige berekende metriek of complexe, berekende metriek bouwen en opslaan.

## Beginnen met het bouwen van een berekende metrische waarde

U kunt op de volgende manieren beginnen met het maken van een berekende metrische waarde:

* Open in Analysis Workspace een project en selecteer vervolgens **[!UICONTROL Components]** > **[!UICONTROL Create metric]**.
* Open in Analysis Workspace een project en selecteer vervolgens de **Plus** pictogram naast [!UICONTROL **Metrisch**] in het linkerspoor.
* In [!DNL Customer Journey Analytics], ga naar **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]** selecteert u vervolgens **[!UICONTROL + Add]** boven aan de pagina Berekende metriek.

## Gebieden van de builder van Berekende metriek

In de volgende afbeelding en de bijbehorende tabel worden enkele hoofdgebieden en kenmerken van de builder van berekende metriek uitgelegd.

![Nieuw berekend metriekvenster dat de belangrijkste gebieden en eigenschappen toont die in deze sectie worden beschreven.](assets/cm_builder_ui.png)

| Veld | Beschrijving |
| --- | --- |
| Titel | De naam van de metrische waarde is verplicht. U kunt metrisch opslaan tenzij het wordt genoemd. |
| Beschrijving | Geef het een gebruikersvriendelijke beschrijving om te tonen waarvoor het wordt gebruikt en het van gelijkaardige degenen te onderscheiden. <p>De beschrijving wordt ook weergegeven in een rapport. Het is beter NIET om de formule in de beschrijving te zetten - in plaats daarvan, beschrijf wat deze metrisch zou moeten en niet zouden moeten worden gebruikt. (De formule wordt geproduceerd aangezien u metrisch bouwt, onder de Summiere rubriek. Dientengevolge, is het niet nodig om de formule aan de beschrijving toe te voegen.) </p> |
| Indeling | U kunt kiezen uit Decimaal, Tijd, Percentage en Valuta. |
| Decimalen | Toont hoeveel decimalen in het rapport zullen worden getoond. Het maximumaantal decimalen dat u kunt opgeven is 10. |
| Naar boven trends tonen als... | Deze metrische polariteit die toont of de Analyse een stijgende trend in metrisch als goed (groen) of slecht (rood) zou moeten beschouwen. Als gevolg hiervan zal de grafiek van het rapport als groen of rood worden weergegeven wanneer het omhoog gaat. |
| Valuta | De basisvaluta voor deze gegevensweergave. |
| Tags | Tags zijn een goede manier om metriek in te delen. Alle gebruikers kunnen tags maken en een of meer tags toepassen op een metrische waarde. U kunt echter alleen tags zien voor de filters die u bezit of die met u zijn gedeeld. Welke soorten markeringen moet u creëren? Hier volgen enkele suggesties voor handige tags:<ul><li>**Teamnamen**, zoals Sociale marketing, Mobiele marketing.</li><li>**Projecten** (analysetags), zoals analyse van de pagina Entry.</li><li>**Categorieën**, zoals Vrouwen; Geografie.</li><li>**Workflows**, zoals goed te keuren; afgewikkeld voor (een specifieke bedrijfseenheid)</li></ul> |
| Samenvatting | <p>De Summiere formule werkt op elk ogenblik bij u een verandering in de metrische definitie aanbrengt. Deze formule wordt ook weergegeven in de metrische rail links als u de muisaanwijzer boven een metrische waarde houdt en op de knop <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Info_18_N.svg" id="image_BDA0EAF89C19440CB02AE248BA3F968E" /> pictogram. </p> |
| Definitie | Dit is waar u in metriek/berekende metriek, filters, en/of functies sleept om berekende metrisch te bouwen. <ul><li>Als u in berekende metrisch sleept, zal het zijn metrische definitie automatisch uitbreiden. </li> <li>U kunt definities nesten met containers. In tegenstelling tot filtercontainers werken deze containers echter als een wiskundige expressie en bepalen ze de volgorde van bewerkingen. </li> </ul> |
| Operator | Gedeeld door ( <img placement="inline"  src="https://spectrum.adobe.com/static/icons/workflow_18/Smock_Divide_18_N.svg" width="15" id="image_320D7363DE024BDEB21E44606C8B367F" width="25px" /> ) is de standaardoperator, plus de operatoren +, - en x. |
| Voorvertoning | Hiermee kunt u snel informatie lezen over mogelijke fouten. De voorvertoning beslaat de laatste 90 dagen. Dit is een manier om aanvankelijk te graven of u de juiste componenten voor uw metrisch hebt geselecteerd. Een onverwacht resultaat zou betekenen u een tweede blik bij de metrische definitie moet nemen. |
| Productcompatibiliteit | Voor berekende metriek die u in Customer Journey Analytics creeert, is deze waarde altijd vermeld zoals [!UICONTROL **Volledig verwerkte gegevens**]. Berekende metriek kan slechts gegevens van gebeurtenisdatasets omvatten. |
| Toevoegen | Voor alle soorten berekende metriek, kunt u containers en statische aantallen aan de definitie toevoegen. Voor geavanceerde berekende metriek, kunt u filters en functies ook toevoegen.<ul><li>Containers werken als een wiskundige expressie en bepalen de volgorde van bewerkingen. Dus alles in een container wordt verwerkt voor de volgende bewerking.</li><li>Wanneer u een filter naar een container sleept, wordt alles in die container gefilterd. (Alleen geavanceerde berekende cijfers)</li><li>U kunt meerdere filters in een container stapelen.</li></ul> |
| Pictogram tandwiel (metrisch type, kenmerk) | Als u het tandwielpictogram naast een metrische waarde selecteert, kunt u het metrische type en de kenmerkmodellen opgeven. <p>**Opmerking:** Houd rekening met het volgende wanneer u de toewijzing van een component bijwerkt naar een niet-standaard toewijzingsmodel:</p><ul><li>**Wanneer het gebruiken van de component in een rapport met *één dimensie*:** De toewijzing van de component negeert het toewijzingsmodel wanneer een niet-standaard toewijzingsmodel wordt gebruikt.</li><li>**Wanneer het gebruiken van de component in een rapport met *meerdere dimensies*:** De toewijzing van de component behoudt het toewijzingsmodel wanneer een niet-standaard toewijzingsmodel wordt gebruikt.</li><li>Meerdere afmetingen zijn alleen beschikbaar als [gegevens exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md).</li></ul> <p>Zie voor meer informatie over toewijzing [Instellingen voor persistentiecomponenten](/help/data-views/component-settings/persistence.md).</p> |
| Plus (+)-pictogram | Hiermee kunt u een nieuwe component maken, zoals een nieuw filter (waarmee u naar de Filterbouwer gaat). |
| Componenten zoeken | Met deze zoekbalk kunt u zoeken naar afmetingen, metriek, filters (alleen geavanceerde berekende meetgegevens) en functies (alleen geavanceerde berekende meetgegevens). |
| Lijst van Dimensionen | In plaats van de Berekende metrische bouwer te verlaten om een eenvoudig filter (in de Bouwer van de Filter), b.v. &quot;Pagina = Homepage&quot;te bouwen, kunt u in Pagina slepen en Homepage direct van de Berekende metrische bouwer selecteren. Dit resulteert in een veel gestroomlijnder werkschema voor het creëren van gefilterde berekende metriek. |
| Lijst met meetwaarden | De cijfers zijn ingedeeld in drie categorieën:<ul><li>Standaardwaarden</li><li>Berekende standaarden</li><li>Metrische sjablonen - onder aan de lijst.</li></ul>Wanneer u de cursor boven een metrische waarde houdt, ziet u het pictogram Info rechts ervan. Als u op dit pictogram klikt, krijgt u de volgende informatie:<ul><li>De formule van hoe het wordt berekend.</li><li>Een voorproeftrend van metrisch.</li><li>Een bewerkingspictogram (potlood) rechtsboven dat u naar de berekende metrische bouwer brengt waar u deze berekende metrische waarde kunt bewerken.</li></ul> |
| Lijst met filters | (Alleen Geavanceerde berekende metriek) Als beheerder worden in deze lijst alle filters weergegeven die in uw aanmeldingsbedrijf zijn gemaakt. Als u een gebruiker niet-Admin bent, toont deze lijst filters u bezit en die met u worden gedeeld. |
| Lijst met functies | (Alleen geavanceerde berekende metriek) Functies zijn verdeeld in twee lijsten: Standaard (het meest gebruikt) en Geavanceerd. |
| Selector gegevensweergave | Met deze kiezer (rechtsboven) kunt u overschakelen naar een andere gegevensweergave. |
