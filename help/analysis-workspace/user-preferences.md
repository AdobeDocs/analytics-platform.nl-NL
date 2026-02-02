---
title: Gebruikersvoorkeuren
description: Leer hoe u algemene voorkeuren en projectvoorkeuren instelt voor gebruikers.
feature: Workspace Basics
exl-id: 6a934be7-0612-41ff-964e-77abc0b1efda
solution: Customer Journey Analytics
role: User
source-git-commit: bc708b34814550b89f6c9916d8bc48850008c1dc
workflow-type: tm+mt
source-wordcount: '3889'
ht-degree: 0%

---

# Gebruikersvoorkeuren

U kunt gebruikersinstellingen of voorkeuren voor Analysis Workspace en verwante componenten voor alle nieuwe projecten of deelvensters beheren die u maakt. Bestaande projecten en deelvensters worden niet beïnvloed.

## Voorkeuren bewerken

U kunt uw voorkeuren op de volgende manieren bijwerken:

- Selecteer ![&#x200B; UserAdmin &#x200B;](/help/assets/icons/UserAdmin.svg) **[!UICONTROL Edit preferences]** van het belangrijkste interface van Workspace.
- Selecteer **[!UICONTROL Project]** > **[!UICONTROL User preferences]** in het menu wanneer u in een Workspace-project werkt.
- Selecteer **[!UICONTROL Components]** > **[!UICONTROL Preferences]** in de bovenste menubalk in Customer Journey Analytics (alleen beschikbaar voor productbeheerders).

## Voorkeuren configureren

U kunt de volgende voorkeuren configureren:

### Algemene voorkeuren

Algemene voorkeuren gelden voor uw Customer Journey Analytics-ervaring in de browser. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [&#x200B; voorkeur van de Update &#x200B;](#update-preferences).

| Voorkeur | Opties |
| --- | --- |
| **[!UICONTROL Landing page]** | Kies welke pagina als de standaardpagina wordt weergegeven wanneer u Customer Journey Analytics opent: <ul><li>Projectlijst (standaard)</li><li>Leeg project</li><li>Lege analyse met instructies voor trends</li><li>Specifiek project, geselecteerd uit een lijst</li></ul> |
| **[!UICONTROL Tips]** | Hiermee geeft u tips weer in een blauw vak rechtsonder in Analysis Workspace. <p>Deze optie is standaard ingeschakeld.</p> |
| **[!UICONTROL Components displayed in left panel groups]** | Kies in het menu Componenten in het linkerdeelvenster hoeveel van elke componentgroep u wilt weergeven. <p>Als u 0 kiest voor een componentgroep, is de componentgroep niet langer toegankelijk vanuit het linkerdeelvenster.</p><p>Standaard worden 5 componenten weergegeven voor elk van de volgende componentgroepen:</p> <ul><li>Dimensies</li><li>Metrics</li><li>Segmenten</li><li>Datumbereiken</li></ul> <p>Voor meer informatie over Componenten in Analysis Workspace, zie [&#x200B; Overzicht van Componenten &#x200B;](/help/components/overview.md).</p> |

### Voorkeuren IMS-organisatie {#ims-organization-preferences}

>[!CONTEXTUALHELP]
>id="workspace_prefs_shareonlyworkspace"
>title="Alleen delen met Workspace-gebruikers toestaan"
>abstract="Als deze optie is ingeschakeld, is de optie **[!UICONTROL Share with anyone]** niet meer beschikbaar voor gebruikers die een Analysis Workspace-project delen. De mensen die eerder toegang tot een project door deze aandeeloptie kregen kunnen niet meer tot het project toegang hebben."

>[!CONTEXTUALHELP]
>id="workspace_prefs_requireexperiencecloudauth"
>title="Experience Cloud-verificatie vereisen"
>abstract="Als deze optie is ingeschakeld, moeten personen die toegang hebben tot een project via de optie **[!UICONTROL Share with anyone]** in Analysis Workspace, zich verifiëren met hun Experience Cloud-gegevens."

>[!CONTEXTUALHELP]
>id="workspace_prefs_projectcommenting"
>title="Opmerkingen over projecten toestaan"
>abstract="Als dit is ingeschakeld, is een gebied met opmerkingen beschikbaar in de rechterspoorlijn van elk project in Analysis Workspace."


U kunt bedrijfvoorkeur bijwerken die op alle gebruikers en projecten binnen uw organisatie van toepassing is. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [&#x200B; voorkeur van de Update &#x200B;](#update-preferences).

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **het Lusje van Malplaatjes** | | |
|  | Tabblad Sjablonen verbergen | Verbergt het Lusje van Malplaatjes voor alle gebruikers in uw organisatie. |
| **het delen van het Project** | | |
| | Alleen delen met Workspace-gebruikers toestaan | Wanneer deze optie is ingeschakeld, kunnen gebruikers in uw organisatie de optie **[!UICONTROL Share with anyone]** niet zien in het menu **[!UICONTROL Share]** . Dit betekent dat de gebruikers geen projecten met mensen kunnen delen die geen rekening van Analysis Workspace in uw organisatie hebben zoals die in [&#x200B; wordt beschreven een project met iedereen (geen vereiste login) &#x200B;](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [&#x200B; projecten van het Aandeel &#x200B;](/help/analysis-workspace/curate-share/share-projects.md).<br/> Deze optie wordt onbruikbaar gemaakt door gebrek voor alle organisaties (betekenend dat de gebruikers projecten met mensen buiten de organisatie kunnen delen) behalve klanten die het Schild van de Gezondheidszorg in licentie hebben gegeven. <p>Houd rekening met het volgende wanneer u deze optie in- of uitschakelt:<ul><li>Wanneer u deze optie inschakelt, hebben mensen die eerder via de optie [!UICONTROL Share with anyone] delen toegang tot een project hebben gekregen, geen toegang meer tot het project.</li><li>Als deze optie is ingeschakeld (om alleen delen met Workspace-gebruikers toe te staan) en later is uitgeschakeld (om delen met iedereen toe te staan), krijgen mensen die eerder via de optie [!UICONTROL Share with anyone] delen toegang tot een project hebben gekregen, niet automatisch weer toegang tot het project. In dit geval, moet de gebruiker die het project deelde de [!UICONTROL **Verbinding toelaten is actieve**] optie die beschikbaar is wanneer het delen van een project met iedereen **([!UICONTROL Share]** > **[!UICONTROL Share with anyone]**), zoals die in [&#x200B; wordt beschreven een project met iedereen (geen vereiste login) &#x200B;](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [&#x200B; projecten van het Aandeel &#x200B;](/help/analysis-workspace/curate-share/share-projects.md).</li><li>**voor klanten die het Schild van de Gezondheidszorg vergunning geven:** Deze optie wordt toegelaten door gebrek en kan niet worden onbruikbaar gemaakt. Voordat u deze optie kunt uitschakelen zodat gebruikers de optie [!UICONTROL Share with anyone] delen kunnen gebruiken, moet u eerst de machtiging [!UICONTROL Share project links with anyone] (onder [!UICONTROL Reporting Tools] ) toevoegen in de Adobe Admin Console. Nadat de machtiging is toegevoegd, kunt u deze optie uitschakelen en vervolgens de resulterende juridische kennisgeving accepteren. Voor informatie over hoe te om een toestemming in Admin Console toe te voegen, zie [&#x200B; producttoestemmingen in Admin Console &#x200B;](https://helpx.adobe.com/nl/enterprise/using/manage-permissions-and-roles.html) leiden.</li></ul> |
| | Experience Cloud-verificatie vereisen | Wanneer deze optie is ingeschakeld, moeten personen die via de optie **[!UICONTROL Share with anyone]** in Analysis Workspace toegang krijgen tot een project, zich verifiëren met hun Experience Cloud-gegevens.<p>Wanneer deze optie is ingeschakeld en een gebruiker een project deelt met de optie [!UICONTROL Share with anyone] delen, wordt de optie [!UICONTROL Require Experience Cloud authentication] ingeschakeld in het dialoogvenster Delen en kan deze optie niet worden uitgeschakeld door de gebruiker die het project deelt. Voor informatie over hoe de gebruikers projecten met iedereen kunnen delen, zie [&#x200B; een project met iedereen (geen vereiste login) delen &#x200B;](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [&#x200B; projecten van het Aandeel &#x200B;](/help/analysis-workspace/curate-share/share-projects.md). <p> <p>Houd rekening met het volgende wanneer u deze optie inschakelt: <ul><li>Wanneer u deze optie inschakelt, worden alle projecten die eerder zijn gedeeld met de optie [!UICONTROL Share with anyone] delen en waarvoor de optie [!UICONTROL Require Experience Cloud authentication] niet is ingeschakeld, gedeactiveerd.<p>Als deze optie is ingeschakeld (om Experience Cloud-verificatie te vereisen) en later is uitgeschakeld (om iedereen met de koppeling toegang te geven tot het project), krijgen mensen die eerder via de optie [!UICONTROL Share with anyone] delen toegang tot een project hebben gekregen niet automatisch opnieuw toegang tot het project. In dit geval, moet de gebruiker die het project deelde de [!UICONTROL Link is active] optie toelaten die wanneer het delen van een project met iedereen **([!UICONTROL Share]** > **[!UICONTROL Share with anyone]** > **[!UICONTROL Link is active]**) beschikbaar is, zoals die in [&#x200B; wordt beschreven een project met iedereen (geen vereiste login) &#x200B;](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [&#x200B; projecten van het Aandeel &#x200B;](/help/analysis-workspace/curate-share/share-projects.md).</li><li>Deze optie is alleen beschikbaar als SSO in uw organisatie is geïmplementeerd. Voor informatie over hoe de systeembeheerders SSO voor uw organisatie kunnen toelaten, zie [&#x200B; Identiteit van de Opstelling en Enige Sign-On &#x200B;](https://helpx.adobe.com/nl/enterprise/using/set-up-identity.html).</p><p>Als SSO voor uw organisatie wordt gevormd, controleer om te zien of wordt om het even welk soort auto-rekening verwezenlijking uitgevoerd in de console. Typisch, zou een systeembeheerder deze opstelling, zoals die in [&#x200B; wordt beschreven automatische rekeningsverwezenlijking &#x200B;](https://helpx.adobe.com/nl/enterprise/using/automatic-account-creation.html) toelaten.</li><li>Als uw organisatie een vergunning geeft voor het Gezondheidsschild, is deze optie standaard ingeschakeld en kan deze optie niet worden uitgeschakeld.</li></ul> |
| Opmerkingen over projecten | Opmerkingen over projecten toestaan | Als deze optie is ingeschakeld, is een gebied met opmerkingen beschikbaar op de rechterspoorlijn van elk project in Analysis Workspace. <p>De eigenaars van het project kunnen het commentaargebied voor een bepaald project onbruikbaar maken, zoals die in [&#x200B; worden beschreven leidt tot projecten &#x200B;](/help/analysis-workspace/build-workspace-project/create-projects.md).</p> <p>Voor meer informatie over het becommentariëren in de projecten van Analysis Workspace, zie [&#x200B; commentaren in projecten &#x200B;](/help/analysis-workspace/build-workspace-project/comment-projects.md) toevoegen en beheren.</p> |

{style="table-layout:auto"}

### Voorkeuren voor projecten en analyses {#project-and-analysis-preferences}

>[!CONTEXTUALHELP]
>id="workspace_prefs_categoricalpalette"
>title="Categorisch palet"
>abstract="Toegepast op vele visualisaties in Analysis Workspace en analyse met instructies. Elke kleur vertegenwoordigt een duidelijke categoriale waarde."

>[!CONTEXTUALHELP]
>id="workspace_prefs_divergingpalette"
>title="Verticaal, palet"
>abstract="Toegepast op de Cohort-tabel in Analysis Workspace en analyse met instructies voor groei van gebruiker. Dit palet heeft een numerieke betekenis met twee uiteinden en een basislijn in het midden."

>[!CONTEXTUALHELP]
>id="workspace_prefs_sequentialpalette"
>title="Sequentieel, palet"
>abstract="Toegepast op de geleide analyse van de frequentie trends (gestapelde balk). Dit palet heeft een numerieke betekenis, van licht tot donker."

U kunt deze voorkeuren aanpassen voor alle nieuwe Analysis Workspace-projecten, nieuwe Analysis Workspace-deelvensters en nieuwe analyses met instructies. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [&#x200B; voorkeur van de Update &#x200B;](#update-preferences).

Sommige van deze zelfde voorkeur kunnen ook voor individuele projecten in Analysis Workspace worden aangepast, zoals die in [&#x200B; het overzicht van het Project &#x200B;](/help/analysis-workspace/build-workspace-project/freeform-overview.md) wordt beschreven.

<!--
>[!IMPORTANT]
>
>You can no longer define the number format in the **[!UICONTROL Project & Analyses]** > **[!UICONTROL Data]** section of **[!UICONTROL User preferences]**. The number format is automatically determined by the [default language that is configured](https://experienceleague.adobe.com/nl/docs/core-services/interface/features/browser-language) for the logged in user.
>
-->


| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Vertoning** | | |
|  | [&#x200B; dichtheid van de Mening &#x200B;](/help/analysis-workspace/build-workspace-project/view-density.md) | Kies hoeveel inhoud u op het scherm wilt weergeven door de verticale opvulling van het linkerdeelvenster, vrije-vormtabellen en coderingstabellen te verminderen. <ul><li>Compact</li><li>Comfortabel</li><li>Uitgebreid (standaard)</li></ul> |
| | [&#x200B; palet van de Kleur &#x200B;](/help/analysis-workspace/build-workspace-project/color-palettes.md) | Kies de visualisatiekleurenpaletten die in Analysis Workspace worden gebruikt en de geleide analyse. <ul><li> Categorisch palet: toegepast op veel visualisaties in Analysis Workspace en op geleide analyses. Elke kleur vertegenwoordigt een duidelijke categoriale waarde. Maak een keuze uit door Adobe verschafte opties of voer een aangepast palet in dat wordt gedefinieerd door komma&#39;s gescheiden hexwaarden.</li><li> Divergent palet: toegepast op de Cohort-tabel in Analysis Workspace en analyse met instructies voor groei van gebruiker. Dit palet heeft een numerieke betekenis met twee uiteinden en een basislijn in het midden.<li> Sequentieel palet: toegepast op de geleide analyse van de frequentie-trends (gestapelde balk). Dit palet heeft een numerieke betekenis, van licht tot donker.</li></ul> |
| **Gegevens** | | |
|  | [&#x200B; mening van Gegevens &#x200B;](/help/analysis-workspace/c-panels/panels.md#data-view) | Kies de gegevens waar tabellen en visualisaties hun gegevens afleiden. <ul><li>Recentste (standaard)</li><li>Specifieke gegevensweergave die is geselecteerd in een lijst</li></ul> |
|  | [&#x200B; Kalender &#x200B;](/help/analysis-workspace/c-panels/panels.md#calendar) | Selecteer uit een lijst van: <ul><li>Door Adobe opgegeven bereiken (standaard is deze maand)</li><li>U kunt [!UICONTROL Make date range components relative to panel calendar by default] inschakelen.</li></ul> |
|  | [&#x200B; Type van Comité &#x200B;](/help/analysis-workspace/c-panels/panels.md#panel-types) | <ul><li>Vrije vorm (standaard)</li><li>Leeg</li><li>Snelle inzichten</li></ul> |
|  | Instantie tellen | Schakel [!UICONTROL Count repeat instances] in om op te geven of herhalingsinstanties worden geteld in rapporten. Als deze optie is ingeschakeld, worden meerdere weergaven van opeenvolgende pagina&#39;s naar dezelfde pagina beschouwd als weergaven van meerdere pagina&#39;s. Als deze optie is uitgeschakeld, worden meerdere opeenvolgende paginaweergaven weergegeven op hetzelfde aantal pagina&#39;s als een weergave van één pagina. <p>**Nota:** Dit het plaatsen beïnvloedt slechts bepaalde metriek (zoals Sessies) en het is niet van toepassing op Stroom of Vallout visualisaties.</p> |
|  | Getalnotatie | <ul><li>1.000.00 (standaard)</li><li>1.000,00</li><li>1 000 00</li></ul> |
|  | CSV-scheidingsteken | <ul><li>Komma (standaard)</li><li>Puntkomma</li><li>Colon</li><li>Pijp</li><li>Periode</li><li>Spatie</li><li>Tab</li></ul> |
|  | Annotaties tonen | Kies of annotaties zichtbaar zijn in uw projecten. Voor meer informatie over annotaties, zie [&#x200B; Overzicht van Annotaties &#x200B;](/help/components/annotations/overview.md). |


### Voorkeuren voor de tabel Vrije vorm {#freeform-table-preferences}

>[!CONTEXTUALHELP]
>id="workspace_prefs_showanomalies"
>title="anomalieën tonen"
>abstract="Als u **[!UICONTROL Show anomalies]** selecteert, worden automatisch anomaliedetectie uitgevoerd voor de eerste metrische kolom die wordt toegevoegd aan de visualisatie van een Freeform-tabel uit een tijdreeks."

>[!CONTEXTUALHELP]
>id="workspace_prefs_showforecast"
>title="Voorvertoning weergeven"
>abstract="Als u **[!UICONTROL Show forecast]** selecteert, wordt automatisch de eerste metrische kolom voorspeld die wordt toegevoegd aan de visualisatie van een tijdreeks voor de Freeform-tabel."


>[!CONTEXTUALHELP]
>id="workspace_prefs_defaulttablemetric"
>title="Standaardtabelmetrisch"
>abstract="Selecteer standaard metrisch voor vrije vormlijsten te gebruiken. Als de geselecteerde gegevensweergave niet de geselecteerde standaardmetrische waarde bevat, schakelt de tabel automatisch over naar een andere primaire metrische waarde."


U kunt de voorkeuren voor vrije-vormtabellen aanpassen voor alle nieuwe projecten die u in Analysis Workspace maakt. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [&#x200B; voorkeur van de Update &#x200B;](#update-preferences).

Sommige van deze voorkeuren kunnen ook worden aangepast voor afzonderlijke tabellen.

Selecteer de titels van de gekoppelde sectie voor meer informatie en context over de beschikbare voorkeuren.

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Lijst** | | |
| | Tabeltype | <ul><li>Vrije vorm</li><li>Tabelbuilder</li></ul> |
| | Standaardtabelmetrisch | <ul><li>Gebeurtenissen</li><li>Sessies</li><li>Mensen</li></ul> |
| | Standaardtabelafmetingen | Kies uit Minuut, Uur, Dag, Week, Maand, Kwart of Jaar. |
| | Datums uitlijnen | Selecteer deze optie als u datums uit elke kolom wilt uitlijnen met alle datums die op dezelfde rij beginnen. |
| **[Kolom](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)** | | |
| | Koptekst van tekstomloop | Hiermee kunt u de koptekst laten omlopen in Freeform-tabellen om kopteksten leesbaarder te maken en tabellen beter deelbaar te maken. Dit is handig voor .pdf-rendering en voor metriek met lange namen. Standaard ingeschakeld. |
| | Totalen tonen | Dit totale aantal is typisch gelijk aan of een ondergroep van [!UICONTROL Grand Total]. Dit weerspiegelt alle tabelsegmenten die binnen de vrije-vormtabel worden toegepast, inclusief de optie [!UICONTROL Include None] . |
| | Totaal tonen | Dit totaal van totalen aantal vertegenwoordigt alle gebeurtenissen die zijn verzameld, soms die als *totaal van de gegevensmening* worden bedoeld. Wanneer een segment wordt toegepast op paneelniveau of binnen de vrije-vormlijst, past dit totaal aan om op alle gebeurtenissen te wijzen die aan de segmentcriteria voldoen. Het grote totaal wordt niet gesteund voor lijsten of onderverdelingen met [&#x200B; statische rijen &#x200B;](/help/analysis-workspace/visualizations/freeform-table/workspace-totals.md). |
| | Menggrijswaarden tonen | Lijngrafieken onder aan het diagram weergeven of verbergen. Als de legenda is verborgen, wordt deze niet langer visueel doorverwezen naar de regels. |
| | Getal | Hiermee wordt bepaald of in een cel de numerieke waarde voor de metrische waarde wordt weergegeven of verborgen. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de numerieke waarde het aantal paginaweergaven voor het rij-item. |
| | Percentage | Bepaalt of een cel de percentagewaarde voor metrisch toont/verbergt. Als de metrische waarde bijvoorbeeld paginaweergaven is, is de percentagewaarde het aantal paginaweergaven voor het rijitem gedeeld door de totale paginaweergaven voor de kolom.  Opmerking: u kunt percentages van meer dan 100% weergeven, zodat u nauwkeuriger kunt zijn. U kunt het bovenste gebonden uiteinde ook naar 1.000% verplaatsen om ervoor te zorgen dat kolommen in te grote breedten kunnen groeien. |
| | anomalieën tonen <!-- This setting was moved from the "Project" tab. this is already in the tool/docs under "Freeform table, But the doc doesn't give a definition. --> | Hiermee wordt bepaald of de waarden in deze kolom een anomaliedetectie uitvoeren. |
| | Voorvertoning weergeven | Hiermee bepaalt u of de voorspelde waarden automatisch worden weergegeven voor de eerste metrische kolom in een tijdreeks vrije-vormtabel die u maakt. |
| | nul interpreteren als geen waarde | Voor cellen met een waarde 0 bepaalt u of een cel van 0 of een lege cel moet worden weergegeven. Dit is handig wanneer u gegevens bekijkt voor elke dag van een maand, en sommige dagen zijn nog niet gebeurd.  In plaats van &#39;0&#39; voor toekomstige datums weer te geven, kunnen lege cellen worden weergegeven. Grafieken voldoen ook aan deze instelling (carts geven bijvoorbeeld geen lijn of balk met 0 waarden weer als deze instelling is ingeschakeld). |
| | Achtergrond | Hiermee wordt bepaald of alle celopmaak, inclusief de staafgrafiek en voorwaardelijke opmaak, in een cel wordt weergegeven of verborgen <ul><li>Staafgrafiek</li> Hiermee wordt een horizontale staafgrafiek weergegeven die de waarde van de cel ten opzichte van het totaal voor de kolom vertegenwoordigt. <li>Voorwaardelijke opmaak</li>Voor meer informatie over voorwaardelijk formatteren, zie &quot;Voorwaardelijke het formatteren&quot;in [&#x200B; Montages van de Kolom &#x200B;](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)</ul> |
| | Celvoorvertoning | Toont een voorproef van hoe elke cel met de momenteel geselecteerde opmaakopties wordt getoond. |
| **[Rij](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)** | | |
| | Uitsplitsing naar positie | Selecteer deze optie als u wilt dat de uitsplitsing bij de positie van het item blijft en niet bij het item zelf. Voor meer informatie over onderverdelingen, zie [&#x200B; onderverdelingen dimensies &#x200B;](/help/components/dimensions/t-breakdown-fa.md). |
| | Percentage berekening | <ul><li>Kolom</li><li>Rij</li></ul> |
| | Kolomtotalen (alleen statische rijen) | <ul><li>De som van rijen weergeven: geeft de som van de afzonderlijke regelitems weer </li><li>Totaal-generaal weergeven: geeft de gedupliceerde som van rijen weer.</li></ul> |

### Voorkeuren voor visualisatie {#visalization-preferences}

>[!CONTEXTUALHELP]
>id="workspace_prefs_defaultflowcontainer"
>title="Standaardcontainer"
>abstract="Selecteer de standaardcontainer voor [!UICONTROL Flow] visualisaties. Als de geselecteerde gegevensweergave niet de geselecteerde standaardcontainer bevat, schakelt de [!UICONTROL Flow] visualisatie automatisch over naar een andere primaire container."

>[!CONTEXTUALHELP]
>id="workspace_prefs_defaultfalloutcontainer"
>title="Standaardcontainer"
>abstract="Selecteer de standaardcontainer voor [!UICONTROL Fallout] visualisaties. Als de geselecteerde gegevensweergave niet de geselecteerde standaardcontainer bevat, schakelt de [!UICONTROL Fallout] visualisatie automatisch over naar een andere primaire container."

>[!CONTEXTUALHELP]
>id="workspace_prefs_defaulthistogramcountingmethod"
>title="Standaardtelmethode"
>abstract="Selecteer de standaardtelmethode die voor [!UICONTROL Histogram] visualisaties moet worden gebruikt. Als de geselecteerde gegevensweergave niet de geselecteerde standaardtelmethode bevat, schakelt de visualisatie van [!UICONTROL Histogram] automatisch over naar een andere primaire telmethode."

>[!CONTEXTUALHELP]
>id="workspace_prefs_defaultjourneycanvascontainer"
>title="Standaardcontainer"
>abstract="Selecteer de standaardcontainer voor [!UICONTROL Journey canvas] visualisaties. Als de geselecteerde gegevensweergave niet de geselecteerde standaardcontainer bevat, schakelt de [!UICONTROL Journey canvas] visualisatie automatisch over naar een andere primaire container."


U kunt de visualisatievoorkeuren bijwerken voor alle nieuwe projecten die u in Analysis Workspace maakt. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [&#x200B; voorkeur van de Update &#x200B;](#update-preferences).

Sommige van deze voorkeuren kunnen ook worden aangepast voor afzonderlijke visualisaties.

Selecteer de titels van de gekoppelde sectie voor meer informatie en context over de beschikbare voorkeuren.

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Algemene Gebreken** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor alle visualisaties. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legendetekst voor alle visualisaties verbergen. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as voor alle visualisaties. Deze voorkeur kan nuttig zijn als u een grote dataset hebt. |
| | Dubbele as weergeven (indien van toepassing) | Is slechts van toepassing als u twee metriek hebt - u kunt een y-as op de linkerzijde (voor één metrisch) en op het recht (voor andere metrisch) hebben. Deze voorkeur is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Normalisatie (indien van toepassing) | Dwingt metriek tot gelijke verhoudingen. Deze voorkeur is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Y-as anker bij nul | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as door het standaarddiagram bijgewerkt naar NON-ZERO. Als u dit vakje inschakelt, wordt de y-as geforceerd naar nul (en wordt de grafiek opnieuw getekend). |
| | Ankeranomalieën bij het schalen van de Y-as | De y-as wordt geschaald met afwijkende waarden. |
| **[Lijn](/help/analysis-workspace/visualizations/line.md)** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor de lijnvisualisatie. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor lijnvisualisatie verbergen. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as in de lijnvisualisatie. Deze voorkeur kan nuttig zijn als u een grote dataset hebt. |
| | Dubbele as weergeven (indien van toepassing) | Is slechts van toepassing als u twee metriek hebt - u kunt een y-as op de linkerzijde (voor één metrisch) en op het recht (voor andere metrisch) hebben. Deze voorkeur is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Normalisatie (indien van toepassing) | Dwingt metriek tot gelijke verhoudingen. Deze voorkeur is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | x-as tonen | Hiermee geeft u de x-as weer op het lijndiagram. |
| | Y-as tonen | Hiermee geeft u de y-as op het lijndiagram weer. |
| | Y-as van anker | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as NON-ZERO weergegeven als de standaardinstelling van het diagram. Als u dit selectievakje inschakelt, wordt de y-as gedwongen op nul te komen (en wordt de grafiek opnieuw getekend). |
| | Afwijkingen van schaal Y-as toestaan | Als u veelvoudige metriek in een grafiek hebt, moet u over elke anomalie bewegen om de betrouwbaarheidsband voor die metrisch te zien. De y-as wordt niet automatisch geschaald om de visualisatie beter leesbaar te maken met het betrouwbaarheidsinterval Anomaly-detectie. Met deze instelling kan het betrouwbaarheidsinterval de visualisatie schalen. <p>Voor meer informatie, zie [&#x200B; anomalieën van de Mening in Analysis Workspace &#x200B;](/help/analysis-workspace/c-anomaly-detection/view-anomalies.md).</p> |
| | Schalen van Y-as toestaan voor voorspelling | Als u voorspelde waarden buiten de bovenste en onderste begrenzing van de historische waarden hebt, worden deze voorspelde waarden niet automatisch geschaald op de y-as. Als u deze optie inschakelt, wordt de y-as voor de voorspelde waarden op de juiste wijze geschaald. |
| | min. tonen | Bedek een label voor een minimumwaarde om de dalen snel in metrische vorm te markeren. Opmerking: de hoofdwaarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie. |
| | max. tonen | bedek een label voor de maximumwaarde om de pieken snel in metrisch formaat te markeren. Opmerking: de maximale waarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie. |
| | Trendline tonen | Toon een regressie of bewegende gemiddelde trendline aan uw lijnreeks. Met behulp van trendlines wordt een duidelijker patroon in de gegevens weergegeven. |
| **[Cohort](/help/analysis-workspace/visualizations/cohort-table/t-cohort.md)** | | |
| | [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} <br/> Container | Selecteer de aangewezen container voor cohortanalyse in het geval van een op rekening-gebaseerde [!BADGE &#x200B; verbinding van B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}. <p>De volgende opties zijn beschikbaar:</p> <ul><li>Globale Rekeningen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Rekeningen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Het kopen van Groepen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Kansen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Persoon</li></ul> |
| | Granulariteit | Voor getreneerde visualisaties kunt u de tijdsgranulariteit (Dag, Week, Maand, Kwart, of Jaar) veranderen. Deze wijziging geldt ook voor de gegevensbrontabel. |
| | Alleen percentages weergeven | Hiermee verwijdert u de getalwaarde en geeft u alleen het percentage weer. |
| | Percentages afronden naar dichtstbijzijnde gehele getal | Rondt de percentagewaarde aan het meest dichtbijgelegen geheel in plaats van het tonen van de decimale waarde. |
| | Gemiddelde percentagerij weergeven | Hiermee voegt u een nieuwe rij boven aan de tabel in en voegt u vervolgens het gemiddelde voor de waarden binnen elke kolom toe. |
| **[Combo grafieken](/help/analysis-workspace/visualizations/combo-charts.md)** | | |
| | X-as tonen | Hiermee geeft u de x-as weer op de Combo-grafiek. |
| | Y-as tonen | Hiermee geeft u de y-as weer op de keuzelijst met invoervak. |
| | Scheepjes weergeven op lijnen | Ballonnen tonen op lijnen in Combo-grafieken. |
| **[Zeer belangrijke Metrische Samenvatting](/help/analysis-workspace/visualizations/key-metric.md)** | | |
| | Weergavetype Samenvatting | <ul><li>Percentage wijziging benadrukken</li><li>Nummerwaarde benadrukken</li></ul> |
| | Meerdere regels tonen | hoe of verberg lijngrafieken bij de bodem van de grafiek. Als de legenda is verborgen, wordt deze niet langer visueel doorverwezen naar de regels. |
| | max. en min. tonen op vonklines | Minimum- en maximumwaarden tonen op primaire diagrammen en vergelijkingslijngrafieken. |
| | Vergelijking tonen | Vergelijkingsgegevens tonen. Wanneer deze optie is verborgen, zijn zowel het vergelijkingsregeldiagram als de summiere wijzigingsobjecten verborgen. |
| | Nummerwaardeopties | In de [!UICONTROL **Zeer belangrijke Metrische Summiere**] sectie <ul><li>Percentage wijziging tonen</li><li>Raw-verschil tonen</li>Onbewerkt verschil tussen de totale waarde van de meting in het primaire datumbereik en het secundaire datumbereik</ul> |
| **[Uitval](/help/analysis-workspace/visualizations/fallout/configuring-fallout.md)** | | |
| | Container | Selecteer de voorkeurscontainer om het plakken te analyseren. De aangewezen container helpt u rekenschap overeenkomst op diverse B2B containerniveaus [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} begrijpen, persoonbetrokkenheid op het persoonniveau (over zittingen), of de analyse beperken tot één enkele zitting. <p>De volgende opties zijn beschikbaar:</p> <ul><li>Globale Rekeningen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Rekeningen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Het kopen van Groepen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Kansen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Sessie</li><li>Persoon</li></ul> |
| **[Stroom](/help/analysis-workspace/visualizations/c-flow/create-flow.md)** | | |
| | Container | Selecteer de voorkeurscontainer die u wilt analyseren. De aangewezen container helpt u rekenschap overeenkomst op diverse B2B containerniveaus [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} begrijpen, persoonbetrokkenheid op het persoonniveau (over zittingen), of de analyse beperken tot één enkele zitting. <p>De volgende opties zijn beschikbaar:</p> <ul><li>Globale Rekeningen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Rekeningen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Het kopen van Groepen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Kansen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Sessie</li><li>Persoon</li></ul> |
| | Labels voor tekstomloop | Normaal gesproken worden de labels op de Flow-elementen ingekort om de schermruimte op te slaan, maar u kunt het volledige label zichtbaar maken door dit selectievakje in te schakelen. Standaard = uitgeschakeld. |
| | Herhalingsinstanties opnemen | Stroomvisualisaties zijn gebaseerd op instanties van een dimensie. Deze instelling biedt u de mogelijkheid om herhaalde exemplaren op te nemen of uit te sluiten, bijvoorbeeld Pagina opnieuw wordt geladen. Herhalingen kunnen echter niet worden verwijderd uit Flow-visualisaties met multigetaxeerde afmetingen, zoals listVars, listProps, s.product, merchandising Vars, enz. Standaard = uitgeschakeld. |
| | Knopinfo weergeven | Bepaalt of tooltips, die knoopgegevens bevatten, wanneer het hangen over individuele knopen binnen een stroomvisualisatie worden getoond. |
| | Aantal kolommen | Hiermee bepaalt u hoeveel kolommen u in het stroomdiagram wilt opnemen. |
| | Items uitgevouwen per kolom | Hoeveel punten u in elke kolom wilt. |
| **[het canvas van de Reis](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md)** | | |
| | Container | Selecteer de voorkeurscontainer om het plakken te analyseren. De aangewezen container helpt u rekenschap overeenkomst op diverse B2B containerniveaus [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"} begrijpen, persoonbetrokkenheid op het persoonniveau (over zittingen), of de analyse beperken tot één enkele zitting. <p>De volgende opties zijn beschikbaar:</p> <ul><li>Globale Rekeningen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Rekeningen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Het kopen van Groepen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Kansen [!BADGE &#x200B; B2B edition &#x200B;]{type=Informative url="https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-b2b/cja-b2b-edition" newtab=true tooltip="Customer Journey Analytics B2B edition"}</li><li>Sessie</li><li>Persoon</li></ul> |
| **Gestapelde Grafieken** | | |
| | 100% gestapeld | Met deze instelling op een gestapeld gebied, gestapelde staaf of horizontale staaf verandert u het diagram in een &#39;100% gestapelde&#39; visualisatie. <p>Voor meer informatie, zie [&#x200B; gestapelde bar en bar &#x200B;](/help/analysis-workspace/visualizations/bar.md).</p> |
| **[Histogram](/help/analysis-workspace/visualizations/histogram.md)** | | |
| | Aantal emmers | Kies het aantal datumbereiken (emmers) in de visualisatie. Het maximumaantal emmers is 50. <p>Voor meer informatie, zie [&#x200B; Histogram &#x200B;](/help/analysis-workspace/visualizations/histogram.md).</p> |
| | Telmethode | Kies een van de volgende opties: <ul><li>Actief</li><li>Sessie</li><li>Persoon</li></ul> <p>Als u bijvoorbeeld met paginaweergaven werkt, kunt u per persoon paginaweergaven, paginaweergaven voor een bezoek of paginaweergaven per gebeurtenis kiezen. Bij Actief wordt &quot;Voorvallen&quot; gebruikt als de metrische y-as in een vrije-vormtabel.</p> |
| **[Summiere Verandering](/help/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Waarde | <!-- Seem to be basically the same options as in "Number value options" --> <ul><li>Percentage wijziging</li><li>Onbewerkt verschil</li></ul> |
| | Percentage | De waarden van vertoningen in percentages voor de Summiere visualisaties van de Verandering. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor de visualisatie Samenvattingswijziging verbergen. |
| **[Summiere Aantal](/help/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Percentage | De waarden van vertoningen in percentages voor de Summiere visualisaties van het Aantal. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor de visualisatie Samenvattingsnummer verbergen. |
| | Samenvattingswaarde met | Kies uit Max, Min, Gemiddeld, Mediaan en Sum. |
| | Afkorting | In de sectie **[!UICONTROL Summary Number]** |
| **[Boomstructuur](/help/analysis-workspace/visualizations/treemap.md)** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor de Treemap-visualisaties. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as in de Treemap-visualisatie. Deze voorkeur kan nuttig zijn als u een grote dataset hebt. |
| **[Venn](/help/analysis-workspace/visualizations/venn.md)** | | |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legendetekst voor de Venn-visualisatie verbergen. |
| **[Spreiding](/help/analysis-workspace/visualizations/scatterplot.md)** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor de verstrooiingsvisualisaties. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor de verstrooiing verbergen. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as in de verstrooiingsvisualisatie.  Deze voorkeur kan nuttig zijn als u een grote dataset hebt. |
| | Anker y-as bij nul | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as NON-ZERO weergegeven als de standaardinstelling van het diagram. Als u dit vakje inschakelt, wordt de y-as geforceerd naar nul (en wordt de grafiek opnieuw getekend). |

## Standaardvoorkeuren herstellen

U kunt al uw gebruikersvoorkeuren herstellen naar de standaardwaarden van het systeem. Deze voorkeur beïnvloedt beheerdervoorkeur onder het Bedrijf tabel niet.

Deze handeling kan niet ongedaan worden gemaakt.

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] **>** [!UICONTROL **Voorkeur**] van het hoogste menu. Of selecteer **[!UICONTROL Project]** > **[!UICONTROL User settings]** in het menu Workspace.

1. Selecteer **[!UICONTROL Restore defaults]** in de rechterbovenhoek.

1. Selecteer **[!UICONTROL Restore defaults]** in **[!UICONTROL Restore system default settings]** .

## [!UICONTROL Dark theme]

Als u liever een donkere achtergrond voor uw Customer Journey Analytics-gebruikersinterface hebt, kunt u schakelen naar [!UICONTROL Dark theme] .

1. Selecteer het Experience Cloud-gebruikerspictogram rechtsboven.

   ![&#x200B; donker-thema &#x200B;](assets/dark-theme.png)

1. Schakel **[!UICONTROL Dark theme]** in.

