---
title: Een gegevensweergave maken of bewerken
description: Alle instellingen die u kunt aanpassen om een gegevensweergave te maken of te bewerken.
exl-id: 02494ef6-cc32-43e8-84a4-6149e50b9d78
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: f578b8e381f59abb1f22e00718531f216fefaef8
workflow-type: tm+mt
source-wordcount: '2293'
ht-degree: 0%

---

# Een gegevensweergave maken of bewerken

Het creëren van een gegevensmening impliceert of het creëren van metriek en dimensies van schemaelementen of het gebruiken van standaardcomponenten. De meeste schemaelementen kunnen of een afmeting of metrisch afhankelijk van de vereisten van uw zaken zijn. Nadat u een schema-element naar een gegevensweergave hebt gesleept, worden aan de rechterkant opties weergegeven waarmee u de werking van de dimensie of de metrische instelling in Customer Journey Analytics kunt aanpassen.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ creeer of geef een gegevensmening ](https://video.tv.adobe.com/v/35110/?quality=12&learn=on){target="_blank"} voor een demo video uit.

>[!ENDSHADEBOX]


Een gegevensweergave maken of bewerken:

1. Login aan [ Customer Journey Analytics ](https://analytics.adobe.com) en selecteert **[!UICONTROL Data views]**, naar keuze van **[!UICONTROL Data management]**, in het hoogste menu.
1. Selecteer **[!UICONTROL Create new data view]** om een gegevensweergave te maken. U kunt ook een bestaande gegevensweergave selecteren in de lijst met gegevensweergaven om deze te bewerken.


## Configureren {#configure}

Een nieuwe of bestaande gegevensweergave configureren:

>[!BEGINTABS]

>[!TAB  Standaard ]

![ vorm gegevensmening ](assets/dataview-configure.png)

>[!TAB  B2B edition ]

![ vorm gegevensmening B2B ](assets/dataview-configure-b2b.png)

>[!ENDTABS]


1. Selecteer de tab **[!UICONTROL Configure]** (als deze nog niet actief is).


1. Geef details [!UICONTROL Settings] , [!UICONTROL Container] en [!UICONTROL Calendar] op (zie hieronder).
1. Selecteer **[!UICONTROL Save and continue]** als u de nieuwe of bestaande gegevensweergave wilt blijven configureren. Selecteer **[!UICONTROL Save]** om de configuratie voor uw bestaande gegevensweergave op te slaan.


### Instellingen {#configure-settings}


>[!CONTEXTUALHELP]
>id="dataview_externalid"
>title="Externe id"
>abstract="Het wijzigen van de externe id kan van invloed zijn op de manier waarop de naam van de gegevensweergave wordt weergegeven in externe bronnen, zoals hulpprogramma&#39;s voor bedrijfsinformatie."


Verstrekt overkoepelende montages voor de gegevensmening.

| Instelling | Beschrijving |
| --- | --- |
| **[!UICONTROL Connection]** | Dit gebied verbindt de gegevensmening met de verbinding die u vroeger vestigde, die één of meerdere datasets van Adobe Experience Platform bevat. |
| **[!UICONTROL Name]** | Vereist. De naam van de gegevensweergave. Deze waarde wordt weergegeven in het vervolgkeuzemenu rechtsboven in Analysis Workspace. |
| **[!UICONTROL External ID]** | Vereist. De naam van gegevensmening u in externe bronnen, zoals bedrijfsintelligentiegereedschappen kunt gebruiken. De standaardwaarde is `unspecified` . Als u geen externe id opgeeft, wordt de naam gegenereerd op basis van de naam van de gegevensweergave en worden spaties vervangen door onderstrepingstekens. |
| **[!UICONTROL Description]** | Optioneel. Adobe raadt een gedetailleerde beschrijving aan, zodat gebruikers begrijpen waarom de gegevensweergave bestaat en voor wie deze is ontworpen. |

{style="table-layout:auto"}

### Compatibiliteit {#compatibility}


>[!CONTEXTUALHELP]
>id="dataview_dataviewsinadobejourneyoptimizer"
>title="Gegevensweergaven in Journey Optimizer"
>abstract="Customer Journey Analytics moet een verbinding en gegevensweergave gebruiken die compatibel zijn met Adobe Journey Optimizer. Standaard worden automatisch een verbinding en een gegevensweergave voor dit doel gemaakt.<br/> Alternatief, kunt u deze optie toelaten om dit de standaardgegevensmening te maken die in Adobe Journey Optimizer rapportering wordt gebruikt. Wanneer toegelaten, worden alle noodzakelijke die componenten voor Journey Optimizer worden vereist toegevoegd aan deze gegevensmening, en alle noodzakelijke datasets van Journey Optimizer worden toegevoegd aan de verbinding verbonden aan deze gegevensmening."
>additional-url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/integrations/ajo#connection" text="Welke componenten en datasets worden toegevoegd."


Bevat instellingen die van toepassing zijn bij gebruik van Adobe Journey Optimizer in aanvulling op Customer Journey Analytics.

Deze sectie is alleen zichtbaar voor beheerders die zijn ingericht met Journey Optimizer.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL **Reeks als standaardgegevensmening in Adobe Journey Optimizer**] | Met deze configuratieoptie wordt de rapportage in Journey Optimizer en Customer Journey Analytics gestandaardiseerd. Het staat u ook toe om geavanceerde analyse van uw gegevens van Adobe Journey Optimizer in Customer Journey Analytics uit te voeren (door ![ Open ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_OpenInLight_18_N.svg) te selecteren [!UICONTROL **analyseert in CJA**] terwijl in Journey Optimizer).<p>Journey Optimizer heeft toegang nodig tot een Customer Journey Analytics-gegevensweergave om dit type analyse uit te voeren.<p>Schakel deze optie in om dit de standaardgegevensweergave te maken die wordt gebruikt in Journey Optimizer-rapportage voor uw sandbox.</p><p>Deze configuratieoptie automatisch:</p><ul><li>Vormt alle vereiste datasets van Journey Optimizer in de bijbehorende verbinding in Customer Journey Analytics voor gebruik met Journey Optimizer.</li><li>Hiermee maakt u een set Journey Optimizer-meetgegevens en -afmetingen in de gegevensweergave (inclusief afgeleide velden en berekende meetgegevens). Contextlabels worden automatisch ingesteld op al deze maatstaven en dimensies.</li></ul><p><p>Houd rekening met het volgende wanneer u deze optie inschakelt: <ul><li>U kunt de standaardgegevensweergave later wijzigen, maar hierdoor kunnen uw Journey Optimizer-rapportgegevens veranderen. Als u deze optie uitschakelt nadat deze is ingeschakeld, wordt u gevraagd een nieuwe standaardgegevensweergave te selecteren.</li><li>Als u reeds handaanpassingen aan de datasets, afmetingen, of metriek in de de gegevensmening van Customer Journey Analytics maakte, blijven uw handaanpassingen intact wanneer het toelaten van deze configuratieoptie. Met deze optie maakt u aanvullende aanpassingen waarmee de rapportage in Journey Optimizer en Customer Journey Analytics verder wordt gestandaardiseerd. U kunt deze optie ook handmatig aanpassen nadat u deze hebt ingeschakeld.</li><li>Als deze optie is geselecteerd, kan de verbinding die aan de gegevensweergave is gekoppeld, niet worden verwijderd.</li></ul>Zie [ Adobe Journey Optimizer met Adobe Customer Journey Analytics ](/help/integrations/ajo.md) voor meer informatie integreren. |

{style="table-layout:auto"}

### Containers

Hiermee geeft u de naam van containers voor de gegevensweergave aan. De namen van de container worden vaak gebruikt in [ segmenten ](/help/components/filters/filters-overview.md#Filter-containers).

| Instelling | Beschrijving |
| --- | --- |
| [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} <br/>**[!UICONTROL Global Account container name]** | `Global Account` (standaardwaarde). De container [!UICONTROL Global Account] bevat elke sessie en gebeurtenis voor globale accounts binnen de opgegeven tijdsperiode. Als uw organisatie een andere term gebruikt, kunt u de naam van de container hier wijzigen. |
| [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} <br/>**[!UICONTROL Account container name]** | `Account` (standaardwaarde). De container [!UICONTROL Account] bevat elke sessie en gebeurtenis voor accounts binnen de opgegeven tijdsperiode. Als uw organisatie een andere term gebruikt, kunt u de naam van de container hier wijzigen. |
| [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} <br/>**[!UICONTROL Opportunity container name]** | `Opportunity` (standaardwaarde). De container [!UICONTROL Opportunity] bevat elke sessie en gebeurtenis voor mogelijkheden binnen de opgegeven tijdsperiode. Als uw organisatie een andere term gebruikt, kunt u de naam van de container hier wijzigen. |
| [!BADGE  B2B edition ]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} <br/>**[!UICONTROL Buying group container name]** | `Buying Group` (standaardwaarde). De container [!UICONTROL Buying group] bevat elke sessie en gebeurtenis voor het aanschaffen van groepen binnen de opgegeven tijdsperiode. Als uw organisatie een andere term gebruikt, kunt u de naam van de container hier wijzigen. |
| **[!UICONTROL Person container name]** | `Person` (standaardwaarde). De container [!UICONTROL Person] bevat elke sessie en gebeurtenis voor personen binnen de opgegeven tijdsperiode. Als uw organisatie een andere term gebruikt (bijvoorbeeld &quot;Bezoeker&quot; of &quot;Gebruiker&quot;), kunt u de naam van de container hier wijzigen. |
| **[!UICONTROL Session container name]** | `Session` (standaardwaarde). Met de container [!UICONTROL Session] kunt u paginainteracties, campagnes of conversies voor een bepaalde sessie identificeren. U kunt de naam van deze container wijzigen in &#39;Visit&#39; of in een andere term die uw organisatie verkiest. |
| **[!UICONTROL Event container name]** | `Event` (standaardwaarde). De container [!UICONTROL Event] definieert individuele gebeurtenissen in een dataset. Als uw organisatie een andere term gebruikt (bijvoorbeeld &quot;Hits&quot; of &quot;Paginaweergaven&quot;), kunt u de naam van de container hier wijzigen. |

{style="table-layout:auto"}

### Kalender

Hiermee geeft u de kalender-indeling aan die moet worden gevolgd door de gegevensweergave. U kunt veelvoudige gegevensmeningen hebben die op de zelfde [ Verbinding ](/help/connections/create-connection.md) worden gebaseerd en hen verschillende kalendertypes of tijdstreken geven. Deze gegevensmeningen kunnen teams toestaan die verschillende kalendertypes gebruiken om hun respectieve behoeften met de zelfde onderliggende gegevens aan te passen.

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL **streek van de Tijd**] | Kies in welke tijdzone de gegevens moeten worden weergegeven. Als u een tijdzone kiest die op de Tijd van de Besparing van het Daglicht werkt, worden de gegevens automatisch aangepast om dat te weerspiegelen. In de lente wanneer de klokken één uur vooruit aanpassen, is een gat van één uur aanwezig. In de val wanneer de klokken één uur achter aanpassen, wordt één uur herhaald tijdens de verschuiving van DST. |
| [!UICONTROL **Type van Kalender**] | Bepaal hoe weken van de maand worden gegroepeerd.<br>**Gregorian:** Standaard kalenderformaat. Kwarten worden gegroepeerd op maand.<br>**4-5-4 Kleinhandel:** Een gestandaardiseerde 4-5-4 detailhandelkalender. De eerste en laatste maanden van het kwartaal bevatten vier weken, terwijl de tweede maand van het kwartaal uit vijf weken bestaat.<br>**Douane (4-5-4):** Gelijkaardig aan 4-5-4 kalender behalve kunt u de eerste dag van het jaar kiezen en welk jaar dat de &quot;extra&quot;week voorkomt.<br>**Douane (4-4-5):** de eerste en tweede maanden van elk kwartaal bevatten 4 weken, terwijl de laatste week van elk kwartaal uit 5 weken bestaat.<br>**Douane (5-4-4):** De eerste maand van elk kwartaal bestaat uit 5 weken, terwijl de tweede en derde maand van elk kwartaal uit 4 weken bestaat. |
| [!UICONTROL **Eerste maand van het jaar**] en [!UICONTROL **Eerste dag van week**] | Zichtbaar voor het Gregoriaanse kalendertype. Geef op op welke maand het kalenderjaar moet beginnen en op welke dag elke week moet beginnen. |
| [!UICONTROL **Eerste dag van huidig jaar**] | Zichtbaar voor aangepaste kalendertypen. Geef op welke dag van het jaar het huidige jaar moet beginnen. Op basis van deze waarde wordt de eerste dag van elke week automatisch opgemaakt in de kalender. |
| [!UICONTROL **Jaar waarin de &quot;extra&quot;week voorkomt**] | Met de meeste kalenders van 364 dagen (52 weken van elk 7 dagen), accumuleert elk jaar leftoverdagen tot zij aan een extra week toevoegen. Deze extra week wordt dan toegevoegd aan de laatste maand van dat jaar. Geef op aan welk jaar u de extra week wilt toevoegen. |

{style="table-layout:auto"}

## Onderdelen

Vervolgens kunt u de componenten van een gegevensweergave instellen. Dit betekent dat u metriek en afmetingen kunt maken op basis van schema-elementen. U kunt ook standaardcomponenten gebruiken.

>[!IMPORTANT]
>
>Tot 5.000 metriek en 5.000 dimensies kunnen aan één enkele gegevensmening worden toegevoegd.

1. Selecteer de tab **[!UICONTROL Components]** .

   ![ Componenten tabel ](assets/dataview-components.png)

   U ziet de [!UICONTROL Connection] linksboven, die de gegevenssets en de [!UICONTROL Schema fields] verderop bevat.  De reeds inbegrepen componenten zijn standaardcomponenten (systeem geproduceerd) die voor alle gegevensmeningen (zoals Gebeurtenissen, Mensen, de metriek van zittingen, en Minuut, Kwart, Week afmetingen) worden vereist. Adobe past standaard ook het filter **[!UICONTROL Contains data]** en **[!UICONTROL is not deprecated]** toe, zodat alleen Schema-velden worden weergegeven die gegevens bevatten en die niet zijn afgekeurd.

1. Onderzoek naar een schemagebied gebruikend ![ het pictogram van het Onderzoek ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) **[!UICONTROL Search schema fields]** of vind een gebied door zich in om het even welke datasetinzamelingen, als ![ pictogram van de Omslag ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Folder_18_N.svg) **[!UICONTROL Event datasets]** te bewegen.<br/> Alternatief, kunt u een afgeleid gebied tot stand brengen gebruikend ![ het pictogram van Gegevens ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Data_18_N.svg) **leidt tot afgeleid gebied**. Zie [ Afgeleide gebieden ](./derived-fields/derived-fields.md) voor meer informatie.

1. Wanneer u uw specifiek schemagebied vond of uw afgeleid gebied bepaalde, sleep dat gebied, zoals ![ pictogram van het Handvat ](https://spectrum.adobe.com/static/icons/workflow_22/Smock_DragHandle_22_N.svg) **[!UICONTROL Page Name]**, van het linkerspoor in **[!UICONTROL Metrics]** of **[!UICONTROL Dimensions]** sectie onder **[!UICONTROL Included components]**.
U kunt het zelfde schemagebied in de dimensies of metrieksecties veelvoudige tijden slepen en de zelfde afmeting of metrisch op verschillende manieren vormen. Bijvoorbeeld, van het pageName gebied, kunt u een dimensie tot stand brengen die `Product Pages` wordt genoemd, en een andere wordt genoemd `Error pages`, door verschillende [ montages van de Component ](component-settings/overview.md) op het recht te gebruiken.
Als u een schemagebiedomslag van het linkerspoor sleept, worden de gebieden in de omslag automatisch gesorteerd in de aangewezen sectie. Tekenreeksvelden worden weergegeven in de sectie [!UICONTROL Dimensions] en numerieke schematypen worden weergegeven in de sectie [!UICONTROL Metrics] . U kunt ook op **[!UICONTROL Add all]** klikken en alle schemavelden worden toegevoegd aan de desbetreffende sectie.

1. Zodra u een component selecteert, verschijnen de montages op het recht.

   ![ geselecteerde component van Gegevens ](assets/dataview-component-pagename.png)

   Vorm de component gebruikend [ montages van de Component ](component-settings/overview.md). Welke componentinstellingen beschikbaar zijn, hangt af van het feit of de component een dimensie/metrische component is en van het gegevenstype schema. Voorbeelden van instellingen:

   * [[!UICONTROL Attribution]](component-settings/attribution.md)
   * [[!UICONTROL Behavior]](component-settings/behavior.md)
   * [[!UICONTROL Format]](component-settings/format.md)
   * [[!UICONTROL Include exclude values]](component-settings/include-exclude-values.md)
   * [[!UICONTROL Metric deduplication]](component-settings/metric-deduplication.md)
   * [[!UICONTROL No value options]](component-settings/no-value-options.md)
   * [[!UICONTROL Persistence]](component-settings/persistence.md)
   * [[!UICONTROL Value bucketing]](component-settings/value-bucketing.md)

1. Selecteer **[!UICONTROL Save and continue]** als u de nieuwe of bestaande gegevensweergave wilt blijven configureren. Selecteer **[!UICONTROL Save]** om de configuratie voor uw bestaande gegevensweergave op te slaan.

### Maten of afmetingen dupliceren

Het dupliceren van metriek of afmetingen en het vervolgens wijzigen van specifieke montages is een gemakkelijke manier om veelvoudige metriek of afmetingen van één enkel schemagebied tot stand te brengen. Selecteer de instelling [!UICONTROL Duplicate] onder de naam van de metrische waarde of de afmetingen rechtsboven. Wijzig de nieuwe dimensie of metrische waarde en sla deze onder een beschrijvende naam op.

### Filterschemavelden of -gegevenssets

U kunt {het pictogram van de Filter ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg) schemagebieden in het linkerspoor door [!UICONTROL data type], [!UICONTROL datasets], [!UICONTROL data governance], en [!UICONTROL other] criteria ([!UICONTROL contains data], [!UICONTROL is identity], en [!UICONTROL is not deprecated]) filtreren:![

![ de gebieden van de Filter ](assets/dataview-components-filter.png)

>[!TIP]
>
>Als de componenten niet behoorlijk in uw gegevensmening laden en u een foutenmelding in plaats daarvan ziet, gelieve te verwijzen naar [ Gebrek van toestemmingen ](../troubleshooting/lack-of-permissions.md) voor een resolutie.


### Opgenomen onderdelen {#included-components}


>[!CONTEXTUALHELP]
>id="dataview_includedcomponents_filter_datagovernance_custom"
>title="Aangepaste labels"
>abstract="Naast de labels die Adobe biedt, kunt u ook uw eigen aangepaste labels voor uw organisatie definiëren."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview" text="Overzicht van labels voor gegevensgebruik"

>[!CONTEXTUALHELP]
>id="dataview_includedcomponents_filter_datagovernance_contract"
>title="Contractlabels"
>abstract="De etiketten van het contract (C) worden gebruikt om gegevens te categoriseren die contractuele verplichtingen hebben of met het beleid van het gegevensbeheer van uw organisatie verwant zijn."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview" text="Overzicht van labels voor gegevensgebruik"

>[!CONTEXTUALHELP]
>id="dataview_includedcomponents_filter_datagovernance_identity"
>title="Identiteitslabels"
>abstract="De etiketten van de identiteit (I) worden gebruikt om gegevens te categoriseren die een specifieke persoon kunnen identificeren of contacteren."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview" text="Overzicht van labels voor gegevensgebruik"

>[!CONTEXTUALHELP]
>id="dataview_includedcomponents_filter_datagovernance_sensitive"
>title="Gevoelige labels"
>abstract="Gevoelige labels (S) worden gebruikt om gegevens te categoriseren die u en uw organisatie als gevoelig beschouwen."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview" text="Overzicht van labels voor gegevensgebruik"


>[!CONTEXTUALHELP]
>id="dataview_includedcomponents_filter_datagovernance_partner_ecosystem"
>title="Partnerecosysteem"
>abstract="De etiketten van het Ecosysteem van de partner (P) worden gebruikt om gegevens te categoriseren die met derdepartners worden gedeeld."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview" text="Overzicht van labels voor gegevensgebruik"

>[!CONTEXTUALHELP]
>id="dataview_includedcomponents_filter_datagovernance_policies"
>title="Beleid"
>abstract="Om gegevensgebruikslabels effectief te steunen gegevensnaleving, moet het beleid van het gegevensgebruik worden uitgevoerd. Beleid voor gegevensgebruik is regels die het soort marketingacties beschrijven dat u mag uitvoeren op gegevens in Experience Platform of waarvan u een beperking hebt ingesteld. De filters van Beleid passen het toegelaten beleid op de Mening van Gegevens toe."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview" text="Overzicht van labels voor gegevensgebruik"


>[!CONTEXTUALHELP]
>id="dataview_includedcomponents_filter_responsible_engagement"
>title="Verantwoordelijke betrokkenheidslabels"
>abstract="Verantwoordelijke labels voor betrokkenheid worden gebruikt om verantwoordelijke betrokkenheid te ondersteunen."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview" text="Overzicht van labels voor gegevensgebruik"


**[!UICONTROL Included components]** bevat de lijst met **[!UICONTROL Metrics]** en **[!UICONTROL Dimensions]** die u configureert voor de gegevensweergave.

* Om naar componenten te zoeken, gebruik ](/help/assets/icons/Search.svg) **[!UICONTROL _componenten van het 1} Onderzoek_]**.![
* Om de vermelde inbegrepen componenten te filtreren, selecteer ![ Filter ](/help/assets/icons/Filter.svg).

  ![ omvat de dialoog van de componentenfilter ](assets/dataview_includedcomponents_filter.png)

  In het dialoogvenster **[!UICONTROL Filter field by]** kunt u filteren op de volgende categorieën:

   * **[!UICONTROL Data type]** - U kunt een of meer van de volgende gegevenstypen selecteren: [!UICONTROL String], [!UICONTROL Integer], [!UICONTROL Short], [!UICONTROL Boolean], [!UICONTROL Double], [!UICONTROL Byte], [!UICONTROL Long], [!UICONTROL Date] of [!UICONTROL Date-time].
   * **[!UICONTROL Datasets]** - Selecteer een of meer gegevenssets.
   * **[!UICONTROL Data governance]**: Selecteer een of meer labels in de subcategorieën [!UICONTROL Custom labels] , [!UICONTROL Contract labels] , [!UICONTROL Identity labels] , [!UICONTROL Sensitivity labels] , P [!UICONTROL artner ecosystem] of [!UICONTROL Policies] .
   * **[!UICONTROL Other]** - Selecteer een of meer opties [!UICONTROL Contains data] , [!UICONTROL Is identity] of [!UICONTROL Is not deprecated] .

  Selecteer **[!UICONTROL Apply]** om de filters toe te passen.



## Instellingen {#dataview-settings}

1. Selecteer de tab **[!UICONTROL Settings]** .
1. Vorm segmenten om op uw volledige gegevensmening toe te passen. Zie [ Montages (segmenten) ](#settings-filters) hieronder.
1. Configureer de sessietime-out en metriek. Zie [ montages van de Zitting ](#session-settings) hieronder.
1. Selecteer **[!UICONTROL Save and continue]** als u de nieuwe of bestaande gegevensweergave wilt blijven configureren. Selecteer **[!UICONTROL Save]** om de configuratie voor uw bestaande gegevensweergave op te slaan.

### Instellingen (segmenten) {#segment-settings}

U kunt segmenten toevoegen die van toepassing zijn op een volledige gegevensweergave. Dit segment wordt toegepast op om het even welk rapport dat u in Workspace loopt. Sleep een segment van de lijst in de linkerspoor aan het **[!UICONTROL Add segments]** gebied.

### Sessieinstellingen

Bepaal de periode van inactiviteit tussen gebeurtenissen alvorens een zitting verloopt en nieuwe wordt begonnen. Er is een tijdsperiode vereist. U kunt desgewenst ook een nieuwe sessie forceren om te starten wanneer een gebeurtenis een bepaalde metrische waarde bevat. Zie [ montages van de Zitting ](session-settings.md) voor meer details.

### Gegevensvoorbeeld

In de gegevensvoorvertoning worden (voor de verschillende containers) de gegevens van deze gegevensweergave vergeleken met die van de verbinding. Het percentage van de voorvertoning is gebaseerd op het totale aantal in de verbinding van de laatste 90 dagen.

Als de voorvertoning niet wordt geladen, wordt de verbinding mogelijk nog steeds opnieuw gevuld.

Klik op **[!UICONTROL Save and finish]** als alle gewenste instellingen zijn opgegeven.
