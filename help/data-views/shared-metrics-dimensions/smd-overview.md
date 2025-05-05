---
title: Overzicht van gedeelde metriek en dimensies
description: Gebruik dezelfde dimensie of metrische referentie in meerdere gegevensweergaven.
exl-id: 998a9f9b-cfa7-4b97-b32b-d50e35d01b39
source-git-commit: f03c82375a907821c8e3f40b32b4d4200a47323f
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Overzicht van gedeelde metriek en dimensies

De gedeelde metriek &amp; de afmetingen verstrekken een centrale plaats om afmetingen en metriek te beheren die over om het even welk aantal gegevensmeningen kunnen worden gebruikt. Deze componenten zijn vooral van belang voor organisaties die meerdere gegevensweergaven gebruiken, vooral als die gegevensweergaven gemeenschappelijke componentinstellingen delen. Wijzigingen in gedeelde metriek en dimensies worden direct toegepast op elke gegevensweergave waarop de wijziging wordt toegepast. Wanneer het uitgeven van een individuele gegevensmening, kunnen de gedeelde dimensies en metriek door het pictogram van de a ![ Gedeelde component ](/help/assets/icons/CCLibrary.svg) naast de componentennaam worden geïdentificeerd.

Terwijl gedeelde afmetingen en metriek gemeenschappelijke componenten om over vele gegevensmeningen toelaten worden gebruikt, kunnen zij niet over verbindingen worden gedeeld.

## Workflow

De meeste organisaties gebruiken het volgende overkoepelende werkschema om dimensies en metriek in tijd te dedupliceren en te handhaven:

1. De componenten van de invoer uit elke gegevensmening die over veelvoudige gegevensmeningen zouden kunnen worden gedeeld. Als in meerdere gegevensweergaven dezelfde dimensie of metrische waarde wordt gebruikt, wordt u aangeraden alle instanties van die component te importeren. Hoewel bij deze beste manier duplicaten worden geïmporteerd, worden deze geïmporteerd zodat ze kunnen worden gededupliceerd en hun respectieve referenties naar Workspace-projecten behouden.
1. Controleer alle componenten die dezelfde component-id gebruiken maar andere componentinstellingen hebben. Selecteer voor elke groep gedupliceerde componenten de gewenste componentinstellingen die moeten worden toegepast op alle andere componenten die die component-id delen.
1. Controleer alle componenten die dezelfde component-id gebruiken en dezelfde componentinstellingen hebben. Deze afmetingen of meetwaarden kunnen eenvoudig en veilig worden samengevoegd.

## [!UICONTROL Shared Metrics & Dimensions] manager

**[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Data views]** > **[!UICONTROL Shared Metrics & Dimensions]**

Als u naar deze interface navigeert, worden alle huidige afmetingen en metriek weergegeven die beschikbaar zijn om te worden gedeeld door meerdere gegevensweergaven. De rechterbovenhoek bevat twee knoppen om componenten aan deze interface toe te voegen:

* **[!UICONTROL Import]**: opent een modaal venster dat u een gegevensmening laat selecteren, dan laat u componenten selecteren om voor het delen ter beschikking te stellen.
* **[!UICONTROL Create new]**: Opent de [ Gedeelde componentenredacteur ](shared-component-editor.md).

Direct onder deze twee knoppen zijn vier overzichtskaarten zichtbaar:

![ de kaartvoorproef van het Overzicht ](assets/overview-cards.png)

* **Metriek**: Het totale aantal metriek beschikbaar om over gegevensmeningen voor deze verbinding te delen. Elke verbinding kan tot 10.000 gedeelde metriek bevatten.
* **Dimensies**: Het totale aantal dimensies beschikbaar over gegevensmeningen voor deze verbinding te delen. Elke verbinding kan tot 10.000 gedeelde afmetingen bevatten.
* **dupliceer componenten aan overzicht**: Wanneer het invoeren van componenten over veelvoudige gegevensmeningen, zouden sommige dimensies of metriek zelfde componentenidentiteitskaart kunnen delen. Het aantal in deze overzichtskaart toont het totale aantal componenten die zelfde componentenidentiteitskaart maar verschillende componentenmontages hebben. Als u **[!UICONTROL Review]** selecteert, wordt een filter ingeschakeld waarmee u de gewenste component kunt selecteren die als bron van waarheid fungeert voor alle andere componenten met dezelfde id.
* **Componenten beschikbaar om** samen te voegen: Als een afmeting of metrische aandeel zelfde component ID en de zelfde componentenmontages deelt, dan zijn zij effectief identiek en klaar om te dedupliceren. Als u **[!UICONTROL Review]** selecteert, wordt een filter ingeschakeld waarmee u alle componenten met dezelfde component-id kunt samenvoegen tot één gedeelde dimensie of metrische waarde.

Alle gedeelde afmetingen en metriek worden weergegeven onder de vier overzichtskaarten.

![ Beschikbare afmetingen en metrieke voorproef ](assets/shared-metrics-dimensions.png)

* **Filter**: Selecteer het ![ pictogram van de Filter ](../../assets/icons/Filter.svg) pictogram om beschikbare filters te tonen of te verbergen. De volgende filters zijn beschikbaar:
   * **[!UICONTROL Component type]**: Alleen afmetingen of alleen cijfers weergeven.
   * **[!UICONTROL Dataset]**: alleen componenten weergeven waarin de gegevensset is opgenomen in de gegevensweergaven waarnaar een component wordt gedeeld.
   * **[!UICONTROL Data view]**: alleen componenten weergeven die worden gedeeld met die gegevensweergave.
   * **[!UICONTROL Created by]**: alleen componenten weergeven die door een bepaalde gebruiker zijn gemaakt.
   * **[!UICONTROL Duplicates]**: alleen componenten weergeven die dezelfde component-id hebben als een andere component. Deze filters zijn identiek aan het herzien van componenten door de overzichtskaarten.
* **Onderzoek**: Gebruik het ![ pictogram van het Onderzoek ](../../assets/icons/Search.svg) pictogram om naar een component door naam te zoeken.
* **[!UICONTROL Connection]**: Een drop-down menu dat de [ verbinding ](/help/connections/overview.md) verandert. De gedeelde afmetingen en de metriek zijn altijd specifiek voor één enkele verbinding.
* **[!UICONTROL Customize table]**: Selecteer het ![ Customize lijstpictogram ](/help/assets/icons/ColumnSetting.svg) pictogram om kolommen in de lijst te tonen of te verbergen. Beschikbare opties zijn:
   * **[!UICONTROL Field name]**: De naam van de gedeelde dimensie of metrische waarde. Dit veld is altijd zichtbaar.
   * **[!UICONTROL Type]**: geeft aan of de component een dimensie of metrisch is. Dit veld is altijd zichtbaar.
   * **[!UICONTROL Dataset type]**: Het type gegevensset. De meeste datasets zijn gebeurtenisdatasets.
   * **[!UICONTROL Shared to data view]**: alle gegevensweergaven waarnaar deze component wordt gedeeld. Dit veld is altijd zichtbaar. Selecteer de koppeling om een modaal model te openen waarin alle gegevensweergaven worden weergegeven waarin deze component beschikbaar is.
   * **[!UICONTROL Datasets]**: alle gegevenssets die zijn opgenomen in elke gegevensweergave waarnaar deze component wordt gedeeld. Selecteer de verbinding om een modaal te openen die van alle datasets voor de component een lijst maakt.
   * **[!UICONTROL Created by]**: De naam van de persoon die de component heeft gemaakt of geïmporteerd in de interface voor gedeelde metriek en afmetingen.
   * **[!UICONTROL Schema type]**: De indeling waarin de gegevens worden opgeslagen. Voorbeelden zijn `string` , `double` of `boolean` .
   * **[!UICONTROL Component ID]**: De component-id van de dimensie of metrisch. Om het even welke componenten die zelfde componentenidentiteitskaart in deze interface delen moeten worden herzien en worden gedupliceerd.
   * **[!UICONTROL Schema]**: Het schemapad voor de afmeting of metrisch. Bijvoorbeeld `web.webPageDetails.URL` .
   * **[!UICONTROL Description]**: De [ beschrijving ](/help/data-views/component-settings/overview.md) van de component.
   * **[!UICONTROL Context labels]**: De [ contextetiketten ](/help/data-views/component-settings/overview.md) voor de component.
   * **[!UICONTROL Include/Exclude values]**: Maakt een lijst van het aantal regels zoals die onder [ worden gespecificeerd omvat/sluit waarden ](/help/data-views/component-settings/include-exclude-values.md) uit.
   * **[!UICONTROL Data usage labels]**: De [ etiketten van het gegevensgebruik ](https://experienceleague.adobe.com/nl/docs/experience-platform/data-governance/labels/overview) voor het schemagebied.
   * **[!UICONTROL Deprecated]**: geeft aan of de afgekeurde markering is ingesteld.
   * **[!UICONTROL Format]**: De indeling waarin waarden worden weergegeven. Boeken worden meestal weergegeven als `True | False`, metriek wordt meestal weergegeven als `Decimal` , enzovoort.
   * **[!UICONTROL Metric deduplication]**: De [ Metrische deduplicatie ](/help/data-views/component-settings/metric-deduplication.md) montages van de component &lbrace;.
   * **[!UICONTROL Behavior]**: De montages van het Gedrag van de component [&#128279;](/help/data-views/component-settings/behavior.md).
   * **[!UICONTROL Attribution]**: De montages van de Attributie van de component [&#128279;](/help/data-views/component-settings/attribution.md).
   * **[!UICONTROL No value option]**: De 1&rbrace; geen waardeopties van de component [&#128279;](/help/data-views/component-settings/no-value-options.md).
   * **[!UICONTROL Value bucketing]**: De 1&rbrace; waarde van de component &lbrace;[&#128279;](/help/data-views/component-settings/value-bucketing.md) montages knippert.
   * **[!UICONTROL Persistence]**: De 1&rbrace; persistentie [&#128279;](/help/data-views/component-settings/persistence.md) montages van de component &lbrace;.
   * **[!UICONTROL Lowercase]**: Wijst erop als de component in kleine letters toegelaten op de montages van het Gedrag van de component [&#128279;](/help/data-views/component-settings/behavior.md) wordt gebaseerd.
   * **[!UICONTROL Substring]**: De 1&rbrace; Substring [&#128279;](/help/data-views/component-settings/substring.md) montages van de component &lbrace;.
   * **[!UICONTROL Summary data group]**: De montages van de 1&rbrace; Summiere gegevensgroep van de component [&#128279;](/help/data-views/component-settings/summary-data-group.md).
   * **[!UICONTROL Date created]**: De datum waarop de component is gemaakt of geïmporteerd.
   * **[!UICONTROL Last modified]**: als de component is gewijzigd nadat deze is gemaakt, de datum waarop deze voor het laatst is gewijzigd.
* **[!UICONTROL Job history]**: Selecteer het ![ pictogram van de Geschiedenis ](/help/assets/icons/History.svg) pictogram om een modaal venster te openen dat alle instanties van het invoeren van dimensies en metriek van individuele gegevensmeningen toont.

## Componenten bewerken of componenten delen met gegevensweergaven

Schakel het selectievakje naast een component in om alle beschikbare handelingen weer te geven die u kunt uitvoeren. Meerdere selecties worden ondersteund.

![ Voorproef van beschikbare acties ](assets/smd-actions.png)

* ![ pictogram van het Potlood ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]**: Open de geselecteerde afmetingen en metriek in de [ gedeelde componentenredacteur ](shared-component-editor.md), die u hun [ componentenmontages ](/help/data-views/component-settings/overview.md) laat aanpassen. Wanneer u meerdere componenten selecteert die u wilt bewerken, worden deze allemaal geopend in de componenteditor. U kunt componenten in de componenteditor verplaatsen en klikken om hetzelfde veld voor meerdere componenten te bewerken.
* ![ pictogram van het Aandeel ](/help/assets/icons/ShareAlt.svg) **[!UICONTROL Share to data view(s)]**: Opent een venster dat alle gegevensmeningen beschikbaar binnen de geselecteerde verbinding toont. Schakel het selectievakje in voor elke gegevensweergave waarin u deze component beschikbaar wilt maken en selecteer vervolgens **[!UICONTROL Share]** .
* ![ Unshare pictogram ](/help/assets/icons/SaveTo.svg) **[!UICONTROL Unshare from data view(s)]**: Opent een venster dat alle gegevensmeningen toont die deze component momenteel met wordt gedeeld. Schakel het selectievakje in voor elke gegevensweergave waaruit u de beschikbaarheid van deze component wilt verwijderen en selecteer vervolgens **[!UICONTROL Unshare]** .
* ![ Dupliceer pictogram ](/help/assets/icons/Copy.svg) **[!UICONTROL Duplicate]**: Creeert een exemplaar van de geselecteerde component(en). Er wordt een nieuwe component-id gegenereerd voor gedupliceerde componenten.
* ![ pictogram van de Schrapping ](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]**: Verwijdert de geselecteerde componenten uit de interface. Als de geselecteerde componenten met om het even welke gegevensmeningen worden gedeeld, worden zij unshared.
