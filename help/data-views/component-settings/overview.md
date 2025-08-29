---
title: Componentinstellingen
description: De kernmontages van de mening voor een component van de gegevensmening.
exl-id: 6300d289-d308-476e-aa4e-05cdae361bb2
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: 96d6882c31a5e130219986d156c8e6eda84ec325
workflow-type: tm+mt
source-wordcount: '3702'
ht-degree: 1%

---

# Componentinstellingen {#component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_component_settings"
>title="Componentinstellingen"
>abstract="De naam, beschrijving en andere instellingen die betrekking hebben op een component weergeven en configureren. Schakel dit vakje in om deze component te verbergen voor gebruikers die geen beheerder zijn in de rapportage. Beheerders hebben nog steeds toegang tot de component door **[!UICONTROL Show all components]** te selecteren in een Workspace-project."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_component_contextlabels"
>title="Contextlabels"
>abstract="Het verwijderen van een contextlabel kan gevolgen hebben voor specifieke deelvensters of rapporten waar de component wordt vereist."

<!-- markdownlint-enable MD034 -->


De volgende informatie beschrijft de montages die een component van de gegevensmening gebruikt.

![ de montages van de Component die in deze sectie ](../assets/component-settings.png) worden beschreven

| Instelling | Omschrijving/gebruik |
| --- | --- |
| [!UICONTROL Component type] | Vereist. Hiermee kunt u een component wijzigen van Metrisch in Dimension of omgekeerd. Als u deze vervolgkeuzelijst wijzigt, wordt de component verplaatst naar het bijbehorende opgenomen componentgebied. |
| [!UICONTROL Component name] | Vereist. Hier geeft u de vriendschappelijke naam op die in Analysis Workspace wordt weergegeven. U kunt de naam van een component wijzigen en deze een specifieke naam geven voor de gegevensweergave. |
| [!UICONTROL Description] | Optioneel, maar aanbevolen. Verstrekt informatie over de component aan andere gebruikers. |
| [!UICONTROL Tags] | Optioneel. Hiermee kunt u de component labelen met aangepaste of kant-en-klare tags, zodat u gemakkelijker kunt zoeken en filteren in de gebruikersinterface van Analysis Workspace. |
| [!UICONTROL Context labels] | Optioneel. Een drop-down menu van beschikbare systeem-bepaalde [ contextetiketten ](#context-labels) die op een component kunnen worden toegepast. |
| [!UICONTROL Schema field name] | De naam van het schemaveld. |
| [!UICONTROL Dataset type] | Vereist. Een niet-bewerkbaar veld dat aangeeft uit welk gegevenstype de component afkomstig is (gebeurtenis, zoekopdracht of profiel). |
| [!UICONTROL Dataset] | Een niet-bewerkbaar veld dat aangeeft van welke gegevensset de component afkomstig is. Dit veld kan meerdere gegevenssets bevatten. |
| [!UICONTROL Schema type] | Een niet-bewerkbaar veld dat het gegevenstype van de component weergeeft. Hoewel u elk ondersteund schemaveldtype kunt gebruiken in Platform, worden niet alle veldtypen ondersteund in Customer Journey Analytics. De volgende gegevenstypen worden ondersteund: `Integer`, `Int`, `Long`, `Double`, `Float`, `Number`, `Short`, `Byte`, `String` en `Boolean`. Alleen het gegevenstype van het `String` schema is momenteel toegestaan in Lookup-gegevenssets. |
| [!UICONTROL Component ID] | Vereist. De [ Customer Journey Analytics API ](https://www.adobe.io/cja-apis/docs) gebruikt dit gebied om de component van verwijzingen te voorzien. Elke component in een gegevensweergave moet uniek zijn. Adobe genereert automatisch een id voor elke component. U kunt echter op het bewerkingspictogram klikken en de component-id wijzigen. Wanneer u de component-id wijzigt, worden alle bestaande Workspace-projecten met deze component verbroken. Hoewel elke component een unieke id in één gegevensweergave nodig heeft, kunt u dezelfde component-id in andere gegevensweergaven gebruiken. Als u dezelfde component-id in andere gegevensweergaven gebruikt, kunt u Workspace-projecten compatibel maken in verschillende gegevensweergaven. <br/> voor profiel en raadpleging gebaseerde componenten, heeft componentenidentiteitskaart een prefix die van identiteitskaart op dataset ID wordt gebaseerd (bijvoorbeeld: `642b28fcc1f0ee1c074265a0.person.name.firstName`). Wanneer u een profiel of een op raadpleging gebaseerde component, zoals `person.name.firstName`, in uw Workspace-project opnieuw wilt gebruiken en deze component in verschillende gegevensweergaven wilt configureren, moet u ervoor zorgen dat de naam van de component-id uniek wordt gewijzigd (bijvoorbeeld: `myUniqueID.person.name.firstName` ) in de verschillende gegevensweergaven. |
| [!UICONTROL Path] | Vereist. Een niet-bewerkbaar veld met het schemapad waaruit de component afkomstig is. |
| [!UICONTROL Data Usage Labels] | Alle labels voor gegevensgebruik die in Adobe Experience Platform aan deze component zijn toegewezen. [ leer meer ](/help/data-views/data-governance.md). |
| [!UICONTROL Hide component in reporting] | Hiermee kunt u de component uit de gegevensweergave voor niet-beheerders krullen. Beheerders hebben er nog steeds toegang toe door in een Analysis Workspace-project op [!UICONTROL Show All Components] te klikken. |

{style="table-layout:auto"}



>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ het type van Component montages ](https://video.tv.adobe.com/v/333112/?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Contextlabels

Contextlabels zijn door het systeem gedefinieerde labels die worden toegepast op componenten in een gegevensweergave. Wanneer contextetiketten op componenten (afmetingen of metriek) worden toegepast, wordt Customer Journey Analytics geïnstrueerd om deze context-geëtiketteerde componenten automatisch in bepaalde visualisaties of eigenschappen te gebruiken.

Met contextlabels kunt u semantische context bieden aan afzonderlijke gegevens.  In het algemeen hoeft Customer Journey Analytics de semantische betekenis van een dimensie of metrisch niet te kennen om de analyse uit te voeren.  Nochtans, vereisen sommige situaties (projectmalplaatjes en een paar geselecteerde visualisaties) Customer Journey Analytics semantische betekenis te begrijpen om één of ander type van analyse uit te voeren. Voor deze situaties worden contextlabels gemaakt.

De etiketten van de context werken op het componentenniveau (afmetingen of metrisch), en staan voor grote flexibiliteit binnen de gegevensmening voor de klant toe. U kunt bijvoorbeeld een contextlabel aan een dimensie toewijzen nadat u verschillende naverwerkingstransformaties op een veld hebt toegepast. Of zelfs bij een dimensie die op een afgeleid gebied gebaseerd is.  Contextlabels bieden een abstractielaag boven op componenten en velden.

Gemakshalve worden slimme standaardcontextlabels automatisch toegepast op componenten die zijn gebaseerd op velden met een specifiek XDM-pad. Het contextlabel **[!UICONTROL Commerce: Product Category]** wordt bijvoorbeeld automatisch toegepast op een **[!UICONTROL Category name]** -dimensie die is gebaseerd op het `productListItems.productCategories.categoryName` -schemapad. U kunt het contextlabel echter zonder problemen naar een andere component verplaatsen.

Om Adobe te stroomlijnen verstrekte projectmalplaatjes, zetten verscheidene integraties (zoals Journey Optimizer, Content Analytics, en meer) gegevensmeningen op waar uit de dooscomponenten op een specifieke manier worden geconstrueerd. En de aangewezen contextetiketten worden automatisch toegepast. Ook hier kunt u eenvoudig al deze contextlabels verplaatsen naar andere componenten die in de gegevensweergave zijn gemaakt en in plaats daarvan wordt uw aangepaste component gebruikt.

Contextlabels zijn ook relevant voor de openbaarmaking van projectsjablonen. De malplaatjes van het project realiseren snel de rapporteringsstichting voor verscheidene verschillende speciaal-gebouwde gebruiksgevallen. Nochtans, niet elke malplaatje steek voor elke gegevensmening en u wilt niet niet-toepasselijke malplaatjes tonen. Contextlabels worden gebruikt om sjablonen weer te geven op basis van het feit of de contextlabels zijn opgenomen in de geselecteerde gegevensweergave.  U kunt eenvoudig meer contextetiketten aan uw gegevensmening (componenten) toevoegen, en meer malplaatjes worden beschikbaar. U kunt ook contextlabels verwijderen om specifieke sjablonen te verbergen.

>[!NOTE]
>
>U kunt meerdere contextlabels toepassen op een component, maar u kunt niet één contextlabel toepassen op meerdere componenten in één gegevensweergave.
>

De voordelen van contextlabels zijn:

* **Handigheid**: U moet niet de zelfde component in elk paneel of visualisatie opnieuw selecteren.
* **ontgrendelt functionaliteit**: Sommige visualisaties (als [ Kaart ](/help/analysis-workspace/visualizations/map.md)) vereisen kennis over welke component breedte en lengtegraad is. Door contextlabels toe te wijzen, wordt die informatie doorgegeven aan de visualisatie.
* **Consistentie**: Iedereen in uw organisatie die aan één of meerdere projecten werkt die op een gegevensmening gebaseerd zijn die contextetiketten gebruikt krijgt het zelfde gedrag.
* **Zichtbaarheid van eigenschappen en malplaatjes**: Bepaalde visualisaties en eigenschappen verschijnen slechts wanneer het juiste contextetiket wordt toegewezen. Bijvoorbeeld:

   * A [ de visualisatie van de Kaart ](/help/analysis-workspace/visualizations/map.md) toont behoorlijk slechts wanneer Customer Journey Analytics weet welke gebieden breedte en lengte vertegenwoordigen.
   * De specifieke [ malplaatjes ](/help/analysis-workspace/templates/use-templates.md) zijn zichtbaar slechts wanneer de correcte contextetiketten worden toegepast en de bijbehorende componenten beschikbaar worden.

In de volgende situaties kunnen contextlabels vereist zijn:

* Om een reeks componenten te bepalen, kunt u in experimenteren gebruiken die het [ paneel van de Experimentatie gebruiken ](/help/analysis-workspace/c-panels/experimentation.md) in de projecten van Analysis Workspace.

  Voor meer informatie, zie [ met Journey Optimizer ](/help/integrations/ajo.md#data-view) integreren en [ Doel rapporterend ](/help/integrations/at.md).

* Om een reeks componenten te bepalen, kunt u binnen de [ kaart ](/help/analysis-workspace/visualizations/map.md) visualisatie in de projecten van Analysis Workspace gebruiken.

  Voor meer informatie, zie [ contextetiketten in gegevensmeningen ](/help/analysis-workspace/visualizations/map.md#add-context-labels-in-data-views) in [ Kaart ](/help/analysis-workspace/visualizations/map.md) toevoegen.

  **Nota**: De visualisatie van de Kaart is in de Beperkte het Testen fase van versie en zou niet nog in uw milieu beschikbaar kunnen zijn.

* Wanneer u [ malplaatjes gebruikt die door Adobe ](/help/analysis-workspace/templates/use-templates.md) worden verstrekt. Sommige sjablonen van Adobe werken mogelijk niet omdat bepaalde componenten niet in de gegevensweergave staan.

  Voor elke ontbrekende component is er een contextlabel beschikbaar in de gegevensweergave. U moet of het passende contextetiket aan een component toevoegen die reeds in uw gegevensmening is. Of u moet een nieuwe component aan uw gegevensmening toevoegen en het contextetiket aan de component toevoegen (als niet reeds automatisch verstrekt).

  Voor meer informatie, zie [ ontbrekende componenten aan de gegevensmening voor een bepaalde malplaatje ](/help/analysis-workspace/templates/create-templates.md#add-missing-components-to-the-data-view-for-a-given-template) in het artikel [ toevoegen en malplaatjes ](/help/analysis-workspace/templates/create-templates.md) beheren.


De volgende groepen contextlabels zijn beschikbaar, elk met een lijst met specifieke contextlabels.

+++ Campaign

| Naam | Beschrijving |
|------|-------------|
| Trackingcode | Trackingcode. |
| Code-instanties bijhouden | Code-instanties bijhouden. |

+++

+++ Commerce

| Naam | Beschrijving |
|------|-------------|
| Extra winkelwagentjes | Extra winkelwagentjes |
| Kleurafopen | De wagen wordt geopend. |
| Winkelwagentjes | Winkelwagentjes |
| Kleuraweergaven | Kleuraweergaven |
| Afbeeldingen | Afschrĳvingen. |
| Orders | Bestellingen. |
| Product | Product. |
| Productcategorie | Productcategorie. |
| Productweergaven | Productweergaven. |
| Ontvangsten | Ontvangsten. |
| Winkel | Winkel. |
| Eenheden | Eenheden. |

+++

+++ Experimentatie

| Naam | Beschrijving |
|------|-------------|
| Experimentatieexperiment | Een experiment is een reeks variaties op een ervaring die aan eindgebruikers werden blootgesteld om te bepalen wat het beste is om in eeuwigheid te blijven. |
| Experimentvariant | Variant is een van twee of meer wijzigingen in de ervaring van een eindgebruiker die worden vergeleken om het betere alternatief te identificeren. |

+++

+++ Media

| Naam | Beschrijving |
|------|-------------|
| Inhoud-id | Inhoud-id. |
| Tijd van inhoud besteed | Tijd van inhoud besteed. |
| Episode | Aflevering. |
| Type gebeurtenis | Type gebeurtenis. |
| Tijd besteed aan media | Tijd besteed aan media. |
| Seizoen | Reden. |
| Seconden sinds laatste Vraag | Seconden sinds laatste vraag. |
| Tonen | Tonen. |
| Te starten tijd | Te starten tijd. |
| Totale bufferduur | Totale bufferduur. |
| Totale pauzeduur | Totale pauzeduur. |
| Videolengte | Videolengte. |
| Videonaam | Videonaam. |

+++

+++ callcenter

| Naam | Beschrijving |
|------|-------------|
| Naam callcenter | Naam van callcenter. |
| Bellen | De kosten van de vraag. |
| Bel uren | Bellen naar uren. |
| De Lengte van de vraag | De lengte van de vraag. |
| Reden van oproep | Roep reden aan. |
| De Score van het Onderzoek van de vraag | Enquêtescore aanroepen. |
| Roept | Oproepen. |

+++

+++ Demografisch

| Naam | Beschrijving |
|------|-------------|
| Geslacht | Geslacht. |

+++

+++ Omgeving

| Naam | Beschrijving |
|------|-------------|
| Browser | Browser. |
| Browsertype | Browsertype. |
| Taal | Taal. |
| Besturingssysteem | Besturingssysteem |
| Besturingssysteem | Besturingssysteem. |
| Naam besturingssysteem | Naam besturingssysteem. |

+++

+++ Algemeen

| Naam | Beschrijving |
|------|-------------|
| Naam van handeling | Naam van handeling. |
| Handelingen | Handelingen. |
| Interactiekanaal | Interactiekanaal. |

+++

+++ Geo

| Naam | Beschrijving |
|------|-------------|
| Geo City | Geo city. |
| Geo Land | Geo country. |
| Geo Dma | Geo dma. |
| Geo | Geo regio. |
| Breedte | Latitude. |
| Lengtegraad | Lengtegraad. |
| Belangenpunt | Punt van belangstelling. |
| Staat | Staat. |

+++

+++ Marketingkanaal

| Naam | Beschrijving |
|------|-------------|
| Eerste aanraakkanaal | Eerste aanraakkanaal. |
| Details eerste aanraakkanaal | Details eerste aanraakkanaal. |
| Laatste aanraakkanaal | Laatste aanraakkanaal. |
| Details laatste aanraakkanaal | Laatste aanraakkanaaldetails. |
| Marketingkanaal | Marketingkanaal. |

+++

+++ Mobile

| Naam | Beschrijving |
|------|-------------|
| Toepassings-id | Application ID. |
| Mobiele vervoerder | Mobiele drager. |
| Mobiele crashes | Mobiele neerstortingen. |
| Naam van mobiel apparaat | Naam van mobiel apparaat. |
| Type mobiel apparaat | Mobiel apparaattype. |
| Mobiel in toepassingsberichtnaam | Mobiel in berichtnaam van app. |
| Mobiele installaties | Mobiele installaties. |
| Mobiele startpunten | Mobiele lanceringen. |
| Mobiele fabrikant | Mobiele fabrikant. |
| Mobiel bericht geannuleerd | Mobiel bericht wordt geannuleerd. |
| Mobiele berichtenklikken | Het mobiele bericht klikt. |
| Mobiele berichtimpressies | Mobiele berichtenimpressies. |
| Mobile Message Push Opt in | Mobiel bericht met pushaanmelding. |
| Naam van mobiel pushbericht | Naam van mobiel pushbericht. |
| Mobiele upgrades | Mobiele upgrades. |
| Tijd besteed per getimede actie | Tijd doorgebracht per getimede actie. |

+++

+++ Zoeken

| Naam | Beschrijving |
|------|-------------|
| Zoekmachine | Zoekprogramma. |
| Trefwoord Zoekmachine | Zoekmachine, trefwoord. |
| Zoekmachine natuurlijk | Zoekmachine natuurlijk. |
| Natuurlijk trefwoord voor zoekmachine | Zoekmachine natuurlijk trefwoord. |
| Zoekmachine betaald | Zoekprogramma betaald. |
| Door zoekmachine betaald trefwoord | Betaald trefwoord door zoekmachine zoeken. |

+++

+++ Enquête

| Naam | Beschrijving |
|------|-------------|
| Enquête | Beoordeling. |
| Antwoord enquête | Antwoord van enquête. |
| Voltooide onderzoeken | De enquête is voltooid. |
| Enquêtevraag | Vraag over enquête. |
| Beoordeling start | De enquête begint. |

+++

+++ Web

| Naam | Beschrijving |
|------|-------------|
| Gemiddelde pagina-tijd | Gemiddelde pagina-tijd. |
| Bounces | Bounces. |
| Itempagina | Itempagina. |
| Pagina afsluiten | Pagina afsluiten. |
| Pagina | Pagina. |
| Paginaweergaven | Paginaweergaven. |
| Referenter | Referrer. |
| Type referentie | Refererentype. |
| Referentiedomein | Verwijzen naar domein. |
| Origineel van domein verwijzen | Verwijzend domein origineel. |
| Opnieuw laden | Laadt opnieuw. |
| Bezoeken van één pagina | Bezoeken op één pagina. |
| Secties site | Secties van de site. |

+++

+++ B2B

| Naam | Beschrijving |
|------|-------------|
| Accountnaam | Accountnaam. |
| Naam van kopersgroep | Naam van kopersgroep |
| Naam opportunity | Naam opportunity |

+++

+++ Content Analytics

| Naam | Beschrijving |
|------|-------------|
| Absoluut linkerelement | Absoluut linkerkant van element. |
| Absoluut bovenaan | Absoluut bovenaan. |
| Elementkenmerken | Elementkenmerken. |
| Achtergrondkleuren van element | Achtergrondkleuren van element. |
| Elementcameraposities | Elementcameraposities. |
| Middelen cameranabijheid | Middelen cameranabijheid. |
| Instellingen voor middelencamera | Instellingen voor Asset Camera. |
| Elementklikken | Elementklikken. |
| Element gemaakt door | Element gemaakt door. |
| Aanmaakdatum van element | Gegevensbestand gemaakt element.e |
| Hoogte van bedrijfsmiddelenweergave | Hoogte van weergave van element. |
| Breedte van middelenweergave | Breedte van middelenweergave. |
| Voorgrondkleuren van element | Voorgrondkleuren van element. |
| Element-id | Element-id. |
| Elementafbeeldingstypen | Elementafbeeldingstypen. |
| Element laatst bijgewerkt door | Element laatst bijgewerkt. |
| Laatste bijgewerkte datum van element | Laatste bijgewerkte datum van element. |
| Belichtingsvoorwaarden voor bedrijfsmiddelen | Belichtingsvoorwaarden voor bedrijfsmiddelen. |
| URL voor elementkoppeling | URL voor elementkoppeling. |
| Elementnaam | Elementnaam. |
| Categorieën personen | Categorieën personen van middelen. |
| ID Asset Perception | Unieke id van activa die waarneembaar gelijk zijn. |
| Elementfotografie | Stijlen voor middelenfotografie. |
| Elementen | Elementen. |
| Source-element | Asset Source. |
| Elementlabels | Elementlabels. |
| Elementtype | Elementtype. |
| Weergaven van elementen | Elementweergaven. |
| Asset Visual Attached Spread | Asset Visual Attentie Spread. |
| Dichtheid van visuele elementen | Dichtheid van visuele inhoud van element. |
| Experience Attributes | Ervaar kenmerken. |
| Experience Channel | Ervaar het kanaal. |
| Ervaar klikken | Geniet van klikken. |
| Ervaring met Emoji Count | Ervaar het aantal Emoji. |
| Ervaar het aantal hashtags | Ervaar het aantal hashtags. |
| Ervaar de Horizontale Diepte van het Percentage | Ervaar de horizontale diepte van het percentage. |
| Ervaar trefwoorden | Ervaar trefwoorden. |
| Geniet van marketing | Geniet van marketing. |
| Ervaar verhalen | Ervaar verhalen. |
| Ervaar Persusiestrategieën | Ervaar Persuasiestrategieën. |
| Ervaar leesbaarheid Aantal woorden per reeks | Ervaar de leesbaarheid van het aantal woorden per zin. |
| Ervaar leesbaarheid | Ervaar leesbaarheidsscore. |
| Aantal leesbare zinnen | Ervaar het aantal leesbare volgreeksen. |
| Aantal woorden voor leesbaarheidsstop | Ervaar het aantal woorden voor leesbaarheidsstop. |
| Aantal tekstaanhalingstekens voor leesbaarheid | Ervaar het aantal tekstaanhalingstekens voor leesbaarheid. |
| Ervaar leesbaarheid | Ervaar leesbaarheid van het aantal woorden. |
| Ervaar Source | Ervaar Source. |
| Ervaring met tinten | Beleef tinten. |
| Ervaar de verticale percentagediepte | Beleef de verticale percentagediepte. |
| Weergaven beleven | Ervaar weergaven. |

+++

+++ Journey Optimizer

| Naam | Beschrijving |
|------|-------------|
| Handelingsfout (AJO) | Aantal fouten die door reisacties worden gegenereerd. |
| Uitvoerfout handeling | De voorwaarde van de fout die Journey Runtime verhinderde actie uit te voeren. |
| Handelinglabel (AJO) | De klant genereerde weergavenaam van het element waarmee de eindgebruiker interactie had. |
| Alternatieve uitgangen (AJO) | Het aantal afsluiten dat niet is opgetreden als gevolg van een profiel dat een eindknooppunt bereikt of mislukt als gevolg van een fout. |
| App-installaties (AJO) | Aantal toepassingsinstallaties. |
| App Launches (AJO) | Aantal keer dat een mobiele app wordt gestart. |
| Batch-id (AJO) | GUID die bij aanroeping van elke nieuwe partijinstantie voor een geplande Actie van de Reis of van de Campagne wordt gecreeerd. Bijvoorbeeld: als een geplande reis of Campagne Actie om 8.00am en 10.00am loopt, zullen er twee verschillende batchInstanceID&#39;s zijn. |
| Tijdstempel batchinstantie (AJO) | Het tijdstempel van de batchinstantie. |
| Stemmen voor uitgaande kanalen (afgekeurd) | Het totale aantal berichten die over uitgaande kanalen worden teruggestuurd. |
| Naam Campagne-actie (AJO) | De naam van de campagneactie. |
| Campagne-id (AJO) | De id van de campagne. |
| Campagnenaam (AJO) | De naam van de campagne. |
| Campagne-versie-id (AJO) | De versie-id van de campagne. |
| Kanaal | Het kanaal waarnaar deze gegevens moeten worden gecorreleerd. |
| Klikken (AJO) | Het totale aantal klikken over alle kanalen. |
| Beleidsafwijzing (AJO) | Aantal reisacties die wegens één of meerdere toestemmingsbeleid worden verworpen. |
| Fout bij beslissing over inhoud (AJO) | Foutberichten die worden gegenereerd door beslissingsknooppunten voor inhoud van de reis. |
| Fouten bij beslissingen over inhoud (AJO) | Aantal fouten die worden gegenereerd door beslissingsknooppunten voor inhoud van de reis. |
| Naam van inhoudsbesluit (AJO) | De naam van het inhoudsbeslissingsknooppunt van de reis. |
| Correlatie-id | Correlatie-id. |
| Aantal voorstellen (AJO) | Het aantal aangeboden objecten in het voorstel. |
| Binding van item beslissing | Een samengestelde id die item-id combineert met Experience Decisioning-aanvraag-id, waardoor gegevenspersistentie tussen interacties wordt ingeschakeld. |
| Beslissingsprovider (AJO) | De aanbieder die werd gevraagd om de beslissing te nemen. Deze dimensie wordt gebruikt wanneer de veelvoudige diensten besluiten voor de zelfde plaatsing of de activiteit kunnen nemen. |
| Beslissingsprovider (permanent) (AJO) | De beslissingsprovider waarvoor persistentie-binding is ingeschakeld. |
| Beslissingsbeleid-ID (AJO) | De id van het besluitvormingsbeleid dat wordt gebruikt bij de beslissing welke punten in dit voorstel moeten worden opgenomen. |
| Metrisch opmaken (AJO) | Metrisch opmaken. |
| Geleverd (afgekeurd) | Totaal aantal geleverde berichten. |
| Weergaven (AJO) | Dit aantal geeft AJO-berichten weer. Dit aantal omvat e-mail die wordt geopend, Webvertoningen, en in toepassingsvertoningen. Mobiele platforms rapporteren geen SMS- en pushberichtweergaven en worden daarom niet geteld. |
| Afgewezen (AJO) | Telt elke keer dat het inApp-bericht wordt gesloten door de Adobe SDK, ongeacht welke actie de eindgebruiker kiest om het bericht te sluiten. |
| ID droog uitvoeren (AJO) | Unieke id voor droge uitvoering. |
| E-mailvak wordt geopend (AJO) | Het totale aantal e-mailberichten dat wordt geopend door bots. |
| E-mail wordt geopend (AJO) | Het totale aantal e-mailberichten wordt geopend. |
| E-mailontvangerdomein (AJO) | Domein van e-mailadres. |
| E-mailonderwerp | E-mailonderwerp, niet-gepersonaliseerd. |
| Gebeurtenis-id | Een unieke id voor de gebeurtenis in de tijdreeks. |
| Id van afsluitcriteria (AJO) | De id van de uitreiscriteria die worden gebruikt om te bepalen of de reis moet worden verlaten. |
| Naam van afsluitcriteria (AJO) | Naam van uitstapcriteria. |
| Experiment-id (AJO) | De id van het experiment. |
| Naam experiment (AJO) | De naam van het experiment. |
| Aantal terugvalvoorstellen (AJO) | Het aantal terugvalaanbiedingen. |
| Ophaalfout | De voorwaarde van de fout die Journey Runtime verhinderde haal uit te voeren. |
| Binnenkomende klikken (AJO) | Het totale aantal klikken over binnenkomende kanalen. |
| Binnenkomende afwijzingen (AJO) | Totaal aantal ontslagen over binnenkomende kanalen. |
| Binnenkomende indrukkingen (AJO) | Totaal aantal indrukkingen over binnenkomende kanalen. |
| Binnenkomende verzendingen (AJO) | Het totale aantal verzendt over binnenkomende kanalen. |
| Inkomend geactiveerd (AJO) | Het voorstel werd gekozen om door de Adobe SDK te worden weergegeven. Andere factoren kunnen voorkomen dat het daadwerkelijk wordt weergegeven. |
| Is Send-Time geoptimaliseerd (AJO) | Is de uitvoering van berichten SendTimeOptimized? |
| Is testreis | Maakt het evenement deel uit van de uitvoering van een testreis? |
| Is testbericht (AJO) | Wordt het bericht verzonden als testuitvoering? |
| Object-id (permanent) (AJO) | De id van het item waarvoor persistentiebinding is ingeschakeld. |
| Objectnummer (AJO) | De id van het item. |
| Itemnaam (AJO) | De naam van het item. |
| Itemnaam (permanent) (AJO) | De naam van het item waarvoor persistentie-binding is ingeschakeld. |
| Fout in handeling op reis (AJO) | Foutberichten die worden gegenereerd door reisacties. |
| Naam van handelingknooppunt | De knooppuntnaam van de reisactie. |
| Reisboetters | True if the step event was a trip entry event for a profile. |
| Reiseinde (AJO) | Het einde van de reis. |
| Naam van knooppunt voor reisgebeurtenis | Deze waarde wordt ingesteld wanneer een segment of externe gebeurtenis zich voordoet in een transport. |
| Reden voor uitsluiting van reizen | Reden voor uitsluiting van reisvariant. |
| Naam van regel voor uitsluitingsregel voor reizen | Naam van de Regel die de ontkenning van de Ingang van de Reis veroorzaakte. |
| Uitsluitingen voor reizen (AJO) | Geef aan of de huidige step-gebeurtenis heeft geresulteerd in een teruggooi voor een profiel. Dit komt gewoonlijk doordat er plafonnering- of corresponderingsregels worden toegepast, waardoor verdere voortgang van de reis wordt voorkomen. |
| Type reisweg (AJO) | Het type uitgang dat voor de reisinstantie voorkwam. |
| Fouten op reis | Geeft de huidige status van de stap die is uitgevoerd. |
| Reis-id | De id van de reis. |
| Reisnaam | De naam van de reis. |
| Naam en versie van reis | De naam en versie van de reis. |
| Versie-id reis | De versie-id van de reis. |
| JourneyExits | True als de huidige stap tot een einde van een reisexemplaar heeft geleid. Dat is de laatste stap in een reis voor een bepaald profiel met succes werd uitgevoerd. |
| Landing Page Conversions (AJO) | Totaal aantal conversies op bestemmingspagina. |
| Openingspagina-id (AJO) | Unieke id voor landingspagina. |
| Openingspagina Source (AJO) | De bron van de bestemmingspagina. |
| Weergaven van bestemmingspagina (AJO) | Het totale aantal weergaven op de landingspagina. |
| Openingspagina klikt (AJO) | Het totale aantal klikken op de landingspagina. |
| Koppelings-URL (AJO) | De URL waarop de gebruiker heeft geklikt. |
| Bounce Reden (AJO) | De reden voor het bericht stuitert. |
| Reden voor berichtfout (AJO) | De reden voor de berichtfout. |
| Reden voor uitsluiting van bericht (AJO) | Uitsluitingsreden. |
| Berichtuitvalcategorie (AJO) | Categorie storing. |
| Reden voor mislukte berichten (AJO) | Redenen voor mislukking. |
| Type berichtfout (AJO) | Type fout. |
| Bericht-ID (AJO) | The message id to which this data should be correlated. |
| Berichttaal (AJO) | De taal van het bericht. |
| Berichtnaam (AJO) | De naam van het bericht. |
| Bericht opnieuw proberen (AJO) | Aantal pogingen opnieuw uitvoeren. |
| Berichtstatus (AJO) | Berichtstatus (bijvoorbeeld verzonden, teruggestuurd, fout, enz.) |
| Berichttype (AJO) | Of het bericht marketing of transactie is. |
| Berichtfeedbackstatus (afgekeurd) | Feedbackstatus. |
| Node Enters | True if the step event was a node entrance event for a profile. |
| Knooppunt-id | The node id of the trip node. |
| Node Name | De knooppuntnaam van het reisknooppunt. |
| Knooppunttype | Het knooptype van de wegknoop. |
| Naamruimte van geordende campagne (AJO) | De naamruimte van de identiteit van de georkestreerde actie. |
| Naam geordende actie campagne (AJO) | De naam van de actie van georkestreerde campagne. |
| Orchestrated Campaign Action Node ID (AJO) | De actie-id van de georkestreerde campagne. |
| Geordende campagne-id (AJO) | De id van de georkestreerde campagne. |
| Geordende campagnenaam (AJO) | De naam van de geordende campagne. |
| Geordende campagneversie-id (AJO) | De versie-id van de geordende campagne. |
| Uitgaande klikken (AJO) | Het totale aantal klikken over uitgaande kanalen. |
| Uitgaande fouten (afgekeurd) | Het totale aantal berichten die fouten over uitgaande kanalen hebben. |
| Uitgaande uitsluitingen (afgekeurd) | Het totale aantal uitsluitingsgebeurtenissen over uitgaande kanalen. |
| Uitgaande verzendingen (afgekeurd) | Totaal aantal berichten die over uitgaande kanalen worden verzonden. |
| Belangenpunt | punt van belangstelling. |
| Propositie-id (AJO) | De id van het voorstel. |
| Aangepaste acties duwen (AJO) | Het totale aantal aangepaste handelingen in pushinteractie. |
| Pushinteracties (AJO) | Het aantal keren dat een mobiele app wordt gestart vanwege een directe interactie met pushberichten. |
| Push Platform (AJO) | Push provider service, bijvoorbeeld APNS of FCM. |
| Titel duwen | Push Title, non-personalized. |
| Rangschikkingsstrategie-ID (AJO) | De rangschikkende strategie-ID. |
| Beleidsnaam voor geweigerde toestemming | Naam van het overeenkomstige verworpen toestemmingsbeleid. |
| Aantal opnieuw proberen (AJO) | Het aantal keren dat een bericht is verzonden, is opnieuw geprobeerd voordat het bericht is gelukt of mislukt. |
| Naam van regel | Naam van de Regel die de ontkenning van de Ingang van de Reis veroorzaakte. |
| Selectietype (AJO) | Dit is het type selectie dat wordt gebruikt wanneer een item wordt afgeleid als onderdeel van een beslissing. |
| Verzendt (afgekeurd) | Het totale aantal berichten dat over alle kanalen wordt verzonden. |
| SMS Inbound Message (AJO) | Het inkomende antwoord van SMS, bijvoorbeeld, einde, begin, onderteken, enz. |
| SMS Inbound Messages (AJO) | Binnenkomend SMS-antwoord, bijvoorbeeld stoppen, starten, abonneren, enz. |
| Sms-berichttype (AJO) | De leverancier van SMS, bijvoorbeeld, binnenkomend, binnenkomendReply of verzendt. |
| SMS-provider (AJO) | SMS-provider, bijvoorbeeld Sinch of Twilio. |
| Spam Complaint (AJO) | Totaal aantal klachten over spam. |
| Strategienaam (AJO) | Strategische naam. De strategische naam waarvan het item is afgeleid. |
| Naam van strategie (permanent) (AJO) | De strategienaam met toegelaten persistentie band. |
| Abonnementenlijst toegevoegd (AJO) | Het totale aantal toevoegingen aan een abonnementenlijst. |
| Abonnementenlijst-id (AJO) | Unieke id voor abonnementenlijst. |
| Abonnementenlijst wordt verwijderd (AJO) | Het totale aantal verwijderingen uit een abonnementenlijst. |
| Oppervlak (AJO) | Het kanaaloppervlak waarop het bericht is weergegeven. |
| Gericht (afgekeurd) | Dit aantal van het aantal keren dat een voorstel gericht was op een persoon. Dit is het aantal tijden een voorstel voor vertoning aan een persoon werd overwogen. |
| Naam doelregel (AJO) | De naam van de doelregel. |
| Testgebeurtenis (AJO) | Testgebeurtenis. |
| Te starten tijd | Te starten tijd. |
| Totale bufferduur | Totale bufferduur. |
| Totale pauzeduur | Totale pauzeduur. |
| Verkeerstype (AJO) | The Ranking Traffic Type. |
| Behandelings-id (AJO) | De id van de geselecteerde behandeling voor het experiment. |
| Naam behandeling (AJO) | De naam van de behandeling voor het experiment. |
| Unieke bezoekers in de experimenten (AJO) | De unieke bezoekers in het experiment. |
| Abonnement opzeggen (AJO) | Het totale aantal afmelders. |
| URL-label (AJO) | Label voor menselijke vriendelijkheid voor URL. |
| URL-id (AJO) | De unieke id van de URL waarop de gebruiker heeft geklikt. |

+++
