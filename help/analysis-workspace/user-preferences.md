---
title: Gebruikersvoorkeuren instellen in Analysis Workspace
description: U kunt algemene voorkeuren en projectvoorkeuren instellen voor gebruikers.
feature: Workspace Basics
exl-id: 6a934be7-0612-41ff-964e-77abc0b1efda
solution: Customer Journey Analytics
role: User
source-git-commit: 501a9fbd7c8abd8a63348c2c8d11b88b31a0f6df
workflow-type: tm+mt
source-wordcount: '3451'
ht-degree: 0%

---

# Gebruikersvoorkeuren

U kunt gebruikersinstellingen of voorkeuren voor Analysis Workspace en verwante componenten voor alle nieuwe projecten of deelvensters beheren die u maakt. Bestaande projecten en deelvensters worden niet beïnvloed.

## Voorkeuren bijwerken

U kunt uw voorkeuren op de volgende manieren bijwerken:

- Selecteer ![ UserAdmin ](/help/assets/icons/UserAdmin.svg) **[!UICONTROL Edit preferences]** van het belangrijkste interface van Workspace.
- Selecteer **[!UICONTROL Project]** > **[!UICONTROL User preferences]** in het menu wanneer u in een Workspace-project werkt.
- Selecteer **[!UICONTROL Components]** > **[!UICONTROL Preferences]** in de bovenste hoofdbalk van Customer Journey Analytics (alleen beschikbaar voor productbeheerders).

## Voorkeuren configureren

U kunt de volgende voorkeuren configureren:

### Algemene voorkeuren

Algemene voorkeuren gelden voor uw Customer Journey Analytics-ervaring in de browser. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [ voorkeur van de Update ](#update-preferences).

| Voorkeur | Opties |
| --- | --- |
| **[!UICONTROL Landing page]** | Kies welke pagina als de standaardpagina wordt weergegeven wanneer u Customer Journey Analytics opent: <ul><li>Projectlijst (standaard)</li><li>Leeg project</li><li>Lege analyse met instructies voor trends</li><li>Specifiek project, geselecteerd uit een lijst</li></ul> |
| **[!UICONTROL Tips]** | Hiermee geeft u tips weer in een blauw vak rechtsonder in Analysis Workspace. <p>Deze optie is standaard ingeschakeld.</p> |
| **[!UICONTROL Components displayed in left panel groups]** | Kies in het menu Componenten in het linkerdeelvenster hoeveel van elke componentgroep u wilt weergeven. <p>Als u 0 kiest voor een componentgroep, is de componentgroep niet langer toegankelijk vanuit het linkerdeelvenster.</p><p>Standaard worden 5 componenten weergegeven voor elk van de volgende componentgroepen:</p> <ul><li>Dimensies</li><li>Metrics</li><li>Filters</li><li>Datumbereiken</li></ul> <p>Voor meer informatie over Componenten in Analysis Workspace, zie [ Overzicht van Componenten ](/help/components/overview.md).</p> |

### Voorkeuren IMS-organisatie {#ims-organization-preferences}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_prefs_shareonlyworkspace"
>title="Alleen delen met Workspace-gebruikers toestaan"
>abstract="Als deze optie is ingeschakeld, is de optie **[!UICONTROL Share with anyone]** niet meer beschikbaar voor gebruikers die een Analysis Workspace-project delen. De mensen die eerder toegang tot een project door deze aandeeloptie kregen kunnen niet meer tot het project toegang hebben."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_prefs_requireexperiencecloudauth"
>title="Experience Cloud-verificatie vereisen"
>abstract="Wanneer toegelaten, moeten de mensen die toegang tot een project van het Aandeel met iedereen optie in Analysis Workspace worden verleend voor authentiek verklaren gebruikend hun geloofsbrieven van Experience Cloud."

<!-- markdownlint-enable MD034 -->


U kunt bedrijfvoorkeur bijwerken die op alle gebruikers en projecten binnen uw organisatie van toepassing is. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [ voorkeur van de Update ](#update-preferences).

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **het delen van het Project** | | |
| | Alleen delen met Workspace-gebruikers toestaan | Wanneer deze optie is ingeschakeld, kunnen gebruikers in uw organisatie de optie **[!UICONTROL Share with anyone]** niet zien in het menu **[!UICONTROL Share]** . Dit betekent dat de gebruikers geen projecten met mensen kunnen delen die geen rekening van Analysis Workspace in uw organisatie hebben zoals die in [ wordt beschreven een project met iedereen (geen vereiste login) ](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [ projecten van het Aandeel ](/help/analysis-workspace/curate-share/share-projects.md).<br/> Deze optie wordt onbruikbaar gemaakt door gebrek voor alle organisaties (betekenend dat de gebruikers projecten met mensen buiten de organisatie kunnen delen) behalve klanten die het Schild van de Gezondheidszorg in licentie hebben gegeven. <p>Houd rekening met het volgende wanneer u deze optie in- of uitschakelt:<ul><li>Wanneer u deze optie inschakelt, hebben mensen die eerder via de optie [!UICONTROL Share with anyone] delen toegang tot een project hebben gekregen, geen toegang meer tot het project.</li><li>Als deze optie is ingeschakeld (om alleen delen met Workspace-gebruikers toe te staan) en later is uitgeschakeld (om delen met iedereen toe te staan), krijgen mensen die eerder via de optie [!UICONTROL Share with anyone] delen toegang tot een project hebben gekregen, niet automatisch weer toegang tot het project. In dit geval, moet de gebruiker die het project deelde de [!UICONTROL **Verbinding toelaten is actieve**] optie die beschikbaar is wanneer het delen van een project met iedereen **([!UICONTROL Share]** > **[!UICONTROL Share with anyone]**), zoals die in [ wordt beschreven een project met iedereen (geen vereiste login) ](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [ projecten van het Aandeel ](/help/analysis-workspace/curate-share/share-projects.md).</li><li>**voor klanten die het Schild van de Gezondheidszorg vergunning geven:** Deze optie wordt toegelaten door gebrek en kan niet worden onbruikbaar gemaakt. Voordat u deze optie kunt uitschakelen zodat gebruikers de optie [!UICONTROL Share with anyone] delen kunnen gebruiken, moet u eerst de machtiging [!UICONTROL Share project links with anyone] (onder [!UICONTROL Reporting Tools] ) toevoegen in de Adobe Admin Console. Nadat de machtiging is toegevoegd, kunt u deze optie uitschakelen en vervolgens de resulterende juridische kennisgeving accepteren. Voor informatie over hoe te om een toestemming in Admin Console toe te voegen, zie [ producttoestemmingen in Admin Console ](https://helpx.adobe.com/enterprise/using/manage-permissions-and-roles.html) leiden.</li></ul> |
| | Experience Cloud-verificatie vereisen | Wanneer toegelaten, moeten de mensen die toegang tot een project van het Aandeel met iedereen optie in Analysis Workspace worden verleend voor authentiek verklaren gebruikend hun geloofsbrieven van Experience Cloud.<p>Wanneer deze optie is ingeschakeld en een gebruiker een project deelt met de optie [!UICONTROL Share with anyone] delen, wordt de optie [!UICONTROL Require Experience Cloud authentication] ingeschakeld in het dialoogvenster Delen en kan deze optie niet worden uitgeschakeld door de gebruiker die het project deelt. Voor informatie over hoe de gebruikers projecten met iedereen kunnen delen, zie [ een project met iedereen (geen vereiste login) delen ](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [ projecten van het Aandeel ](/help/analysis-workspace/curate-share/share-projects.md). <p> <p>Houd rekening met het volgende wanneer u deze optie inschakelt: <ul><li>Wanneer u deze optie inschakelt, worden alle projecten die eerder zijn gedeeld met de optie [!UICONTROL Share with anyone] delen en waarvoor de optie [!UICONTROL Require Experience Cloud authentication] niet is ingeschakeld, gedeactiveerd.<p>Als deze optie is ingeschakeld (om Experience Cloud-verificatie te vereisen) en later is uitgeschakeld (om iedereen met de koppeling toegang te geven tot het project), krijgen mensen die eerder via de optie [!UICONTROL Share with anyone] delen toegang tot een project hebben gekregen niet automatisch opnieuw toegang tot het project. In dit geval, moet de gebruiker die het project deelde de [!UICONTROL Link is active] * optie toelaten die wanneer het delen van een project met iedereen **([!UICONTROL Share]** > **[!UICONTROL Share with anyone]** > **[!UICONTROL Link is active]**) beschikbaar is, zoals die in [ wordt beschreven een project met iedereen (geen vereiste login) ](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [ projecten van het Aandeel ](/help/analysis-workspace/curate-share/share-projects.md).</li><li>Deze optie is alleen beschikbaar als SSO in uw organisatie is geïmplementeerd. Voor informatie over hoe de systeembeheerders SSO voor uw organisatie kunnen toelaten, zie [ Identiteit van de Opstelling en Enige Sign-On ](https://helpx.adobe.com/enterprise/using/set-up-identity.html).</p><p>Als SSO voor uw organisatie wordt gevormd, controleer om te zien of wordt om het even welk soort auto-rekening verwezenlijking uitgevoerd in de console. Typisch, zou een systeembeheerder deze opstelling, zoals die in [ wordt beschreven automatische rekeningsverwezenlijking ](https://helpx.adobe.com/enterprise/using/automatic-account-creation.html) toelaten.</li><li>Als uw organisatie een vergunning geeft voor het Gezondheidsschild, is deze optie standaard ingeschakeld en kan deze optie niet worden uitgeschakeld.</li></ul> |

{style="table-layout:auto"}

### Voorkeuren voor projecten en analyses {#project-and-analysis-preferences}


<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_prefs_categoricalpalette"
>title="Categorisch palet"
>abstract="Toegepast op vele visualisaties in Analysis Workspace en analyse met instructies. Elke kleur vertegenwoordigt een duidelijke categoriale waarde."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_prefs_divergingpalette"
>title="Verticaal, palet"
>abstract="Toegepast op de Cohort-tabel in Analysis Workspace en analyse met instructies voor groei van gebruiker. Dit palet heeft een numerieke betekenis met twee uiteinden en een basislijn in het midden."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_prefs_sequentialpalette"
>title="Sequentieel, palet"
>abstract="Toegepast op de geleide analyse van de frequentie trends (gestapelde balk). Dit palet heeft een numerieke betekenis, van licht tot donker."

<!-- markdownlint-enable MD034 -->


U kunt deze voorkeuren aanpassen voor alle nieuwe Analysis Workspace-projecten, nieuwe Analysis Workspace-deelvensters en nieuwe analyses met instructies. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [ voorkeur van de Update ](#update-preferences).

Sommige van deze zelfde voorkeur kunnen ook voor individuele projecten in Analysis Workspace worden aangepast, zoals die in [ het overzicht van het Project ](/help/analysis-workspace/build-workspace-project/freeform-overview.md) wordt beschreven.

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Vertoning** | | |
|  | [ dichtheid van de Mening ](/help/analysis-workspace/build-workspace-project/view-density.md) | Kies hoeveel inhoud u op het scherm wilt weergeven door de verticale opvulling van het linkerdeelvenster, vrije-vormtabellen en coderingstabellen te verminderen. <ul><li>Compact</li><li>Comfortabel</li><li>Uitgebreid (standaard)</li></ul> |
| | [ palet van de Kleur ](/help/analysis-workspace/build-workspace-project/color-palettes.md) | Kies de visualisatiekleurenpaletten die in Analysis Workspace worden gebruikt en de geleide analyse. <ul><li> Categorisch palet: toegepast op veel visualisaties in Analysis Workspace en op geleide analyses. Elke kleur vertegenwoordigt een duidelijke categoriale waarde. Maak een keuze uit door Adobe verschafte opties of voer een aangepast palet in dat wordt gedefinieerd door komma&#39;s gescheiden hexwaarden.</li><li> Divergent palet: toegepast op de Cohort-tabel in Analysis Workspace en analyse met instructies voor groei van gebruiker. Dit palet heeft een numerieke betekenis met twee uiteinden en een basislijn in het midden.<li> Sequentieel palet: toegepast op de geleide analyse van de frequentie-trends (gestapelde balk). Dit palet heeft een numerieke betekenis, van licht tot donker.</li></ul> |
| **Gegevens** | | |
|  | [ mening van Gegevens ](/help/analysis-workspace/c-panels/panels.md#data-view) | Kies de gegevens waar tabellen en visualisaties hun gegevens afleiden. <ul><li>Recentste (standaard)</li><li>Specifieke gegevensweergave die is geselecteerd in een lijst</li></ul> |
|  | [ Kalender ](/help/analysis-workspace/c-panels/panels.md#calendar) | Selecteer uit een lijst van: <ul><li>Door Adobe opgegeven bereiken (standaard is deze maand)</li><li>U kunt [!UICONTROL Make date range components relative to panel calendar by default] inschakelen.</li></ul> |
|  | [ Type van Comité ](/help/analysis-workspace/c-panels/panels.md#panel-types) | <ul><li>Vrije vorm (standaard)</li><li>Leeg</li><li>Snelle inzichten</li></ul> |
|  | Instantie tellen | Schakel [!UICONTROL Count repeat instances] in om op te geven of herhalingsinstanties worden geteld in rapporten. Als deze optie is ingeschakeld, worden meerdere weergaven van opeenvolgende pagina&#39;s naar dezelfde pagina beschouwd als weergaven van meerdere pagina&#39;s. Als deze optie is uitgeschakeld, worden meerdere opeenvolgende paginaweergaven weergegeven op hetzelfde aantal pagina&#39;s als een weergave van één pagina. <p>**Nota:** Dit het plaatsen beïnvloedt slechts bepaalde metriek (zoals Sessies) en het is niet van toepassing op Stroom of Vallout visualisaties.</p> |
|  | Getalnotatie | <ul><li>1.000.00 (standaard)</li><li>1.000,00</li><li>1 000 00</li></ul> |
|  | CSV-scheidingsteken | <ul><li>Komma (standaard)</li><li>Puntkomma</li><li>Colon</li><li>Pijp</li><li>Periode</li><li>Spatie</li><li>Tab</li></ul> |
|  | Annotaties tonen | Kies of annotaties zichtbaar zijn in uw projecten. Voor meer informatie over annotaties, zie [ Overzicht van Annotaties ](/help/components/annotations/overview.md). |


### Voorkeuren voor de tabel Vrije vorm {#freeform-table-preferences}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_prefs_showanomalies"
>title="anomalieën tonen"
>abstract="Als u **[!UICONTROL Show anomalies]** selecteert, worden automatisch anomaliedetectie uitgevoerd voor de eerste metrische kolom die wordt toegevoegd aan de visualisatie van een Freeform-tabel uit een tijdreeks."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_prefs_showforecast"
>title="Voorvertoning weergeven"
>abstract="Als u **[!UICONTROL Show forecast]** selecteert, wordt automatisch de eerste metrische kolom voorspeld die wordt toegevoegd aan de visualisatie van een tijdreeks voor de Freeform-tabel."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_prefs_defaulttablemetric"
>title="Standaardtabelmetrisch"
>abstract="Selecteer standaard metrisch voor vrije vormlijsten te gebruiken. Als de geselecteerde gegevensweergave niet de geselecteerde standaardmetrische waarde bevat, schakelt de tabel automatisch over naar een andere primaire metrische waarde."


<!-- markdownlint-enable MD034 -->



U kunt de voorkeuren voor vrije-vormtabellen aanpassen voor alle nieuwe projecten die u in Analysis Workspace maakt. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [ voorkeur van de Update ](#update-preferences).

Sommige van deze voorkeuren kunnen ook worden aangepast voor afzonderlijke tabellen.

Selecteer de titels van de gekoppelde sectie voor meer informatie en context over de beschikbare voorkeuren.

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Lijst** | | |
| | Tabeltype | <ul><li>Vrije vorm</li><li>Tabelbuilder</li></ul> |
| | Standaardtabelmetrisch | <ul><li>Voorvallen</li><li>Unieke bezoekers</li><li>Bezoeken</li></ul> |
| | Standaardtabelafmetingen | Kies uit Minuut, Uur, Dag, Week, Maand, Kwart of Jaar. |
| | Datums uitlijnen | Selecteer deze optie als u datums uit elke kolom wilt uitlijnen met alle datums die op dezelfde rij beginnen. |
| **[Kolom](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)** | | |
| | Koptekst van tekstomloop | Hiermee kunt u de koptekst laten omlopen in Freeform-tabellen om kopteksten leesbaarder te maken en tabellen beter deelbaar te maken. Dit is handig voor .pdf-rendering en voor metriek met lange namen. Standaard ingeschakeld. |
| | Totalen tonen | Dit totaal is doorgaans gelijk aan of een subset van de [!UICONTROL Grand Total] . Dit weerspiegelt alle tabelfilters die binnen de vrije-vormtabel worden toegepast, inclusief de optie [!UICONTROL Include None] . |
| | Totaal tonen | Dit totaal vertegenwoordigt alle gebeurtenissen die zijn verzameld, ook wel &#39;totaal gegevensweergave&#39; genoemd. Wanneer een filter op paneelniveau of binnen de vrije vormlijst wordt toegepast, past dit totaal aan om op alle gebeurtenissen te wijzen die aan de filtercriteria voldoen. Het grote totaal wordt niet gesteund voor lijsten of onderverdelingen met [ statische rijen ](/help/analysis-workspace/visualizations/freeform-table/workspace-totals.md). |
| | Menggrijswaarden tonen | Lijngrafieken onder aan het diagram weergeven of verbergen. Als de legenda is verborgen, wordt deze niet langer visueel doorverwezen naar de regels. |
| | Getal | Hiermee wordt bepaald of in een cel de numerieke waarde voor de metrische waarde wordt weergegeven of verborgen. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de numerieke waarde het aantal paginaweergaven voor het rij-item. |
| | Percentage | Bepaalt of een cel de percentagewaarde voor metrisch toont/verbergt. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de percentagewaarde het aantal paginaweergaven voor het rijitem gedeeld door de totale paginaweergaven voor de kolom.  Opmerking: we kunnen percentages van meer dan 100% weergeven, om nauwkeuriger te zijn. We verplaatsen het bovenste gebonden plafond ook naar 1000% om ervoor te zorgen dat kolommen te groot kunnen worden. |
| | anomalieën tonen <!-- This setting was moved from the "Project" tab. this is already in the tool/docs under "Freeform table, But the doc doesn't give a definition. --> | Hiermee wordt bepaald of de waarden in deze kolom een anomaliedetectie uitvoeren. |
| | Voorvertoning weergeven | Hiermee bepaalt u of de voorspelde waarden automatisch worden weergegeven voor de eerste metrische kolom in een tijdreeks vrije-vormtabel die u maakt. |
| | nul interpreteren als geen waarde | Voor cellen met een waarde 0 bepaalt u of een cel van 0 of een lege cel moet worden weergegeven. Dit is handig wanneer u gegevens bekijkt voor elke dag van een maand, en sommige dagen zijn nog niet gebeurd.  In plaats van &#39;0&#39; voor toekomstige datums weer te geven, kunnen lege cellen worden weergegeven. Grafieken voldoen ook aan deze instelling (ze geven dus geen lijn of balk weer met 0 waarden als deze instelling is ingeschakeld). |
| | Achtergrond | Hiermee wordt bepaald of alle celopmaak, inclusief de staafgrafiek en voorwaardelijke opmaak, in een cel wordt weergegeven of verborgen <ul><li>Staafgrafiek</li> Hiermee wordt een horizontale staafgrafiek weergegeven die de waarde van de cel ten opzichte van het totaal voor de kolom vertegenwoordigt. <li>Voorwaardelijke opmaak</li>Voor meer informatie over voorwaardelijk formatteren, zie &quot;Voorwaardelijke het formatteren&quot;in [ Montages van de Kolom ](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)</ul> |
| | Celvoorvertoning | Toont een voorproef van hoe elke cel met de momenteel geselecteerde opmaakopties wordt getoond. |
| **[Rij](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)** | | |
| | Uitsplitsing naar positie | Selecteer deze optie als u wilt dat de uitsplitsing bij de positie van het item blijft en niet bij het item zelf. Voor meer informatie over onderverdelingen, zie [ onderverdelingen dimensies ](/help/components/dimensions/t-breakdown-fa.md). |
| | Percentage berekening | <ul><li>Kolom</li><li>Rij</li></ul> |
| | Kolomtotalen (alleen statische rijen) | <ul><li>De som van rijen weergeven: geeft de som van de afzonderlijke regelitems weer </li><li>Totaal-generaal weergeven: geeft de gedupliceerde som van rijen weer.</li></ul> |

### Voorkeuren voor visualisatie {#visalization-preferences}

>[!CONTEXTUALHELP]
>id="workspace_prefs_defaultflowcontainer"
>title="Standaardtabelmetrisch"
>abstract="Selecteer de standaardcontainer die u wilt gebruiken voor stroomvisualisaties. Als de geselecteerde gegevensweergave niet de geselecteerde standaardcontainer bevat, schakelt de stroomvisualisatie automatisch over naar een andere primaire container."

>[!CONTEXTUALHELP]
>id="workspace_prefs_defaultfalloutcontainer"
>title="Standaardtabelmetrisch"
>abstract="Selecteer de standaardcontainer die u voor Fallout-visualisaties wilt gebruiken. Als de geselecteerde gegevensweergave niet de geselecteerde standaardcontainer bevat, wordt automatisch overgeschakeld op een andere primaire container voor de uitvalweergave."

U kunt de visualisatievoorkeuren bijwerken voor alle nieuwe projecten die u in Analysis Workspace maakt. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [ voorkeur van de Update ](#update-preferences).

Sommige van deze voorkeuren kunnen ook worden aangepast voor afzonderlijke visualisaties.

Selecteer de titels van de gekoppelde sectie voor meer informatie en context over de beschikbare voorkeuren.

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Algemene Gebreken** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor alle visualisaties. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legendetekst voor alle visualisaties verbergen. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as voor alle visualisaties. Dit kan nuttig zijn als u een grote dataset hebt. |
| | Dubbele as weergeven (indien van toepassing) | Is slechts van toepassing als u twee metriek hebt - u kunt een y-as op de linkerzijde (voor één metrisch) en op het recht (voor andere metrisch) hebben. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Normalisatie (indien van toepassing) | Dwingt metriek tot gelijke verhoudingen. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Y-as anker bij nul | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as NON-ZERO ingesteld als de standaardinstelling van het diagram. Als u dit vakje inschakelt, wordt de y-as gedwongen tot nul (en wordt het diagram opnieuw getekend). |
| | Ankeranomalieën bij het schalen van de Y-as | De y-as wordt geschaald met afwijkende waarden. |
| **[Lijn](/help/analysis-workspace/visualizations/line.md)** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor de lijnvisualisatie. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor lijnvisualisatie verbergen. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as in de lijnvisualisatie. Dit kan nuttig zijn als u een grote dataset hebt. |
| | Dubbele as weergeven (indien van toepassing) | Is slechts van toepassing als u twee metriek hebt - u kunt een y-as op de linkerzijde (voor één metrisch) en op het recht (voor andere metrisch) hebben. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Normalisatie (indien van toepassing) | Dwingt metriek tot gelijke verhoudingen. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | x-as tonen | Hiermee geeft u de x-as weer op het lijndiagram. |
| | Y-as tonen | Hiermee geeft u de y-as op het lijndiagram weer. |
| | Y-as van anker | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as NON-ZERO ingesteld als de standaardinstelling van het diagram. Als u dit vakje inschakelt, wordt de y-as gedwongen tot nul (en wordt het diagram opnieuw getekend). |
| | Afwijkingen van schaal Y-as toestaan | Als u veelvoudige metriek in een grafiek hebt, moet u over elke anomalie bewegen om de betrouwbaarheidsband voor die metrisch te zien. De y-as wordt niet automatisch geschaald om de visualisatie beter leesbaar te maken met het betrouwbaarheidsinterval Anomaly-detectie. Met deze optie kan het betrouwbaarheidsinterval de visualisatie schalen. <p>Voor meer informatie, zie [ anomalieën van de Mening in Analysis Workspace ](/help/analysis-workspace/c-anomaly-detection/view-anomalies.md).</p> |
| | Schalen van Y-as toestaan voor voorspelling | Als u voorspelde waarden buiten de bovenste en onderste begrenzing van de historische waarden hebt, wordt de y-as niet automatisch geschaald voor deze voorspelde waarden. Als u deze optie inschakelt, wordt de y-as voor de voorspelde waarden op de juiste wijze geschaald. |
| | min. tonen | Bedek een label voor een minimumwaarde om de dalen snel in metrische vorm te markeren. Opmerking: de hoofdwaarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie. |
| | max. tonen | bedek een label voor de maximumwaarde om de pieken snel in metrisch formaat te markeren. Opmerking: de maximale waarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie. |
| | Trendline tonen | Toon een regressie of bewegende gemiddelde trendline aan uw lijnreeks. Met behulp van trendlines wordt een duidelijker patroon in de gegevens weergegeven. |
| **[Cohort](/help/analysis-workspace/visualizations/cohort-table/t-cohort.md)** | | |
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
| | Vergelijking tonen | Vergelijkingsgegevens tonen. Wanneer deze optie is verborgen, worden zowel het vergelijkingsregeldiagram als de summiere wijzigingsobjecten verborgen. |
| | Nummerwaardeopties | In de [!UICONTROL **Zeer belangrijke Metrische Summiere**] sectie <ul><li>Percentage wijziging tonen</li><li>Raw-verschil tonen</li>Onbewerkt verschil tussen de totale waarde van de meting in het primaire datumbereik en het secundaire datumbereik</ul> |
| **[Uitval](/help/analysis-workspace/visualizations/fallout/configuring-fallout.md)** | | |
| | Container | Hiermee kunt u schakelen tussen **[!UICONTROL Session]** en **[!UICONTROL Person]** om het plakken van personen te analyseren. De standaardwaarde is **[!UICONTROL Person]** . Met deze instellingen kunt u de betrokkenheid van personen op persoonlijke niveau (tijdens verschillende sessies) begrijpen of de analyse beperken tot één sessie. <p>De volgende opties zijn beschikbaar:</p> <ul><li>Sessie</li><li>Persoon</li></ul> |
| **[Stroom](/help/analysis-workspace/visualizations/c-flow/create-flow.md)** | | |
| | Container | In de [!UICONTROL **Stroom**] sectie <ul><li>Sessie</li><li>Persoon</li></ul> |
| | Labels voor tekstomloop | Normaal gesproken worden de labels op de Flow-elementen ingekort om de schermruimte op te slaan, maar u kunt het volledige label zichtbaar maken door dit selectievakje in te schakelen. Standaard = uitgeschakeld. |
| | Herhalingsinstanties opnemen | Stroomvisualisaties zijn gebaseerd op instanties van een dimensie. Met deze instelling kunt u herhaalde exemplaren, zoals opnieuw laden van pagina&#39;s, opnemen of uitsluiten. Herhalingen kunnen echter niet worden verwijderd uit Flow-visualisaties met multigetaxeerde afmetingen, zoals listVars, listProps, s.product, merchandising Vars, enz. Standaard = uitgeschakeld. |
| | Knopinfo weergeven | Bepaalt of tooltips die knoopgegevens bevatten wanneer het hangen over individuele knopen binnen een stroomvisualisatie worden getoond. |
| | Aantal kolommen | Hiermee bepaalt u hoeveel kolommen u in het stroomdiagram wilt opnemen. |
| | Items uitgevouwen per kolom | Hoeveel punten u in elke kolom wilt. |
| **Gestapelde Grafieken** | | |
| | 100% gestapeld | Met deze instelling op een gestapeld gebied, gestapelde staaf of horizontale staaf verandert u het diagram in een &#39;100% gestapelde&#39; visualisatie. <p>Voor meer informatie, zie [ gestapelde Bar en bar ](/help/analysis-workspace/visualizations/bar.md).</p> |
| **[Histogram](/help/analysis-workspace/visualizations/histogram.md)** | | |
| | Aantal emmers | Kies het aantal datumbereiken (emmers) in de visualisatie. Het maximumaantal emmers is 50. <p>Voor meer informatie, zie [ Histogram ](/help/analysis-workspace/visualizations/histogram.md).</p> |
| | Telmethode | Kies een van de volgende opties: <ul><li>Actief</li><li>Sessie</li><li>Persoon</li></ul> <p>Als u dit bijvoorbeeld gebruikt in combinatie met paginaweergaven, kunt u per persoon paginaweergaven, paginaweergaven voor een bezoek of paginaweergaven per gebeurtenis kiezen. Bij Actief wordt &quot;Voorvallen&quot; gebruikt als de metrische y-as in een vrije-vormtabel.</p> |
| **[Summiere Verandering](/help/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Waarde | <!-- Seem to be basically the same options as in "Number value options" --> <ul><li>Percentage wijziging</li><li>Onbewerkt verschil</li></ul> |
| | Percentage | De waarden van vertoningen in percentages voor de Summiere visualisaties van de Verandering. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor de visualisatie Samenvattingswijziging verbergen. |
| **[Summiere Aantal](/help/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Percentage | De waarden van vertoningen in percentages voor de Summiere visualisaties van het Aantal. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor de visualisatie Samenvattingsnummer verbergen. |
| | Samenvattingswaarde met | Kies uit Max, Min, Gemiddeld, Mediaan en Sum. |
| | Afkorting | In de [!UICONTROL **Summiere sectie van het Aantal**] |
| **[Boomstructuur](/help/analysis-workspace/visualizations/treemap.md)** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor de Treemap-visualisaties. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as in de Treemap-visualisatie. Dit kan nuttig zijn als u een grote dataset hebt. |
| **[Venn](/help/analysis-workspace/visualizations/venn.md)** | | |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legendetekst voor de Venn-visualisatie verbergen. |
| **[Spreiding](/help/analysis-workspace/visualizations/scatterplot.md)** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor de verstrooiingsvisualisaties. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor de verstrooiing verbergen. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as in de verstrooiingsvisualisatie. Dit kan nuttig zijn als u een grote dataset hebt. |
| | Anker y-as bij nul | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as NON-ZERO ingesteld als de standaardinstelling van het diagram. Als u dit vakje inschakelt, wordt de y-as gedwongen tot nul (en wordt het diagram opnieuw getekend). |

## Standaardvoorkeuren herstellen

U kunt al uw gebruikersvoorkeuren herstellen naar de standaardwaarden van het systeem. Dit beïnvloedt beheerdervoorkeur onder het Bedrijf tabel niet.

Deze handeling kan niet ongedaan worden gemaakt.

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] **>** [!UICONTROL **Voorkeur**] van het hoogste menu. Of selecteer **[!UICONTROL Project]** > **[!UICONTROL User settings]** in het menu Workspace.

1. Selecteer **[!UICONTROL Restore defaults]** in de rechterbovenhoek.

1. Selecteer **[!UICONTROL Restore defaults]** in **[!UICONTROL Restore system default settings]** .

## [!UICONTROL Dark theme]

Als u liever een donkere achtergrond voor uw Customer Journey Analytics-gebruikersinterface hebt, kunt u schakelen naar [!UICONTROL Dark theme] .

1. Selecteer het Experience Cloud-gebruikerspictogram rechtsboven.

   ![ donker-thema ](assets/dark-theme.png)

1. Inschakelen **[!UICONTROL Dark theme]**..

