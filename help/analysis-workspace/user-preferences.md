---
title: Gebruikersvoorkeuren instellen in Analysis Workspace
description: U kunt algemene voorkeuren en projectvoorkeuren instellen voor gebruikers.
feature: Workspace Basics
exl-id: 6a934be7-0612-41ff-964e-77abc0b1efda
solution: Customer Journey Analytics
source-git-commit: c343a729de4cb13473a7acc04e837b5e5f69809b
workflow-type: tm+mt
source-wordcount: '3214'
ht-degree: 0%

---

# Gebruikersvoorkeuren

U kunt instellingen voor Analysis Workspace en de bijbehorende componenten voor alle nieuwe projecten of deelvensters beheren die u maakt. Bestaande projecten en deelvensters worden niet beïnvloed.

## Voorkeuren bijwerken

1. Ga in de Customer Journey Analytics naar de [!UICONTROL **Projecten**] openingspagina, en selecteer vervolgens [!UICONTROL **Voorkeuren bewerken**].

   ![De weergave Werkruimteprojecten markeert de voorkeursopties voor Bewerken die op deze pagina worden beschreven.](assets/user-preferences.png)

   of

   Productbeheerders kunnen voorkeuren van IMS-organisaties bijwerken door naar de [!UICONTROL **Componenten**] tab, dan selecteren [!UICONTROL **Voorkeuren**].

1. Voor informatie over de beschikbare voorkeuren op elk tabblad gaat u verder met een van de volgende secties in dit artikel:

   * [Algemene voorkeuren](#general-preferences)

   * [Voorkeuren IMS-organisatie](#ims-organization-preferences)

   * [Voorkeuren voor projecten en analyses](#project-preferences)

   * [Voorkeuren voor de tabel Vrije vorm](#freeform-table-preferences)

   * [Voorkeuren voor visualisatie](#visualizations-preferences)

## Algemene voorkeuren

Algemene voorkeuren zijn van toepassing op uw Customer Journey Analytics in de browser. Voor informatie over hoe u deze voorkeuren kunt openen, raadpleegt u [Voorkeuren bijwerken](#update-preferences).

| Voorkeur | Opties |
| --- | --- |
| Openingspagina | Kies welke pagina als de standaardpagina wordt weergegeven wanneer u Adobe Analytics opent: <ul><li>Projectlijst (standaard)</li><li>Leeg project</li><li>Specifiek project geselecteerd uit een lijst</li></ul> |
| Tips weergeven | Hiermee geeft u tips weer in een blauw vak rechtsonder in Analysis Workspace. <p>Deze optie is standaard ingeschakeld.</p> |
| Onderdelen die worden weergegeven in linkerspoorweggroepen | Kies hoeveel van elke component in het menu Componenten in de linkerspoorstaaf moet worden weergegeven. <p>Als u 0 kiest, is de component niet meer toegankelijk vanaf de linkerspoorstaaf van uw werkruimten.</p><p>Standaard worden vijf componenten weergegeven voor elk van de volgende opties:</p> <ul><li>Dimensies</li><li>Metrics</li><li>Filters</li><li>Datumbereiken</li></ul> <p>Zie voor meer informatie over Componenten in Analysis Workspace [Overzicht van componenten](/help/components/overview.md).</p> |

## Voorkeuren IMS-organisatie

U kunt bedrijfvoorkeur bijwerken die op alle gebruikers en projecten binnen uw organisatie van toepassing is. Voor informatie over hoe u deze voorkeuren kunt openen, raadpleegt u [Voorkeuren bijwerken](#update-preferences).

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Projectdeling** | | |
| | Alleen delen met Workspace-gebruikers toestaan | <p>Wanneer deze optie is ingeschakeld, kunnen gebruikers in uw organisatie de optie &quot;Delen met iedereen&quot; niet zien in het menu Delen. Dit betekent dat gebruikers geen projecten kunnen delen met mensen die geen Analysis Workspace-account in uw organisatie hebben, zoals beschreven in [Een project delen met iedereen (geen aanmelding vereist)](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [Projecten delen](/help/analysis-workspace/curate-share/share-projects.md).</p><p>Deze optie is standaard uitgeschakeld voor alle organisaties (wat betekent dat gebruikers projecten kunnen delen met personen buiten de organisatie), behalve voor klanten die een vergunning hebben gekregen voor het gezondheidszorgschild. </p><p>Houd rekening met het volgende wanneer u deze optie in- of uitschakelt:</p> <ul><li><p>Wanneer u deze optie inschakelt, hebben mensen die eerder via de optie &quot;Delen met iedereen&quot; toegang tot een project hebben gekregen, geen toegang meer tot het project.</p></li><li><p>Als deze optie is ingeschakeld (om alleen delen met Workspace-gebruikers toe te staan) en later is uitgeschakeld (om delen met iedereen toe te staan), krijgen mensen die eerder toegang tot een project hebben gekregen via de optie Delen met iedereen) niet automatisch weer toegang tot het project. In dit geval moet de gebruiker die het project heeft gedeeld de [!UICONTROL **De koppeling is actief**] optie die beschikbaar is wanneer u een project deelt met iedereen ([!UICONTROL **Delen**] > [!UICONTROL **Delen met iedereen**]), zoals beschreven in [Een project delen met iedereen (geen aanmelding vereist)](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [Projecten delen](/help/analysis-workspace/curate-share/share-projects.md).</p></li><li><p>**Voor klanten die een vergunning hebben voor het gezondheidszorgschild:** Deze optie is standaard ingeschakeld en kan niet worden uitgeschakeld. Voordat u deze optie kunt uitschakelen zodat gebruikers de optie &quot;Delen met iedereen&quot; kunnen gebruiken, moet u eerst de optie [!UICONTROL **Projectkoppelingen delen met iedereen**] machtiging (onder [!UICONTROL **Rapportagetools**]) in de Adobe Admin Console. Nadat de machtiging is toegevoegd, kunt u deze optie uitschakelen en vervolgens de resulterende juridische kennisgeving accepteren. Voor informatie over hoe te om een toestemming in de Admin Console toe te voegen, zie [Productmachtigingen beheren in de Admin Console](https://helpx.adobe.com/enterprise/using/manage-permissions-and-roles.html).</p></li> |
| | Verificatie van Experience Cloud vereisen | <p>Wanneer toegelaten, moeten de mensen die toegang tot een project van &quot;Aandeel met iedereen&quot;optie in Analysis Workspace worden verleend voor authentiek verklaren gebruikend hun geloofsbrieven van het Experience Cloud.</p> <p>Nadat deze optie is ingeschakeld, wordt de optie &quot;Verificatie van Experience Cloud vereisen&quot; ingeschakeld in het dialoogvenster Delen wanneer een gebruiker een project deelt met de optie &quot;Delen met iedereen&quot;. De gebruiker die het project deelt, kan dit niet uitschakelen. (Voor informatie over hoe de gebruikers projecten met iedereen kunnen delen, zie [Een project delen met iedereen (geen aanmelding vereist)](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [Projecten delen](/help/analysis-workspace/curate-share/share-projects.md).)</p> <p>Houd rekening met het volgende wanneer u deze optie inschakelt:</p><ul><li><p>Wanneer u deze optie inschakelt, worden alle projecten die eerder met de optie &quot;Delen met iedereen&quot; zijn gedeeld en waarvoor de optie &quot;Verificatie van Experience Cloud vereisen&quot; niet is ingeschakeld, gedeactiveerd.</p></li> <li><p>Als deze optie wordt toegelaten (om Experience Cloud authentificatie te vereisen) en dan later onbruikbaar gemaakt (om iedereen met de verbinding toe te staan om tot het project toegang te hebben), krijgen de mensen die eerder toegang tot een project door &quot;Aandeel met iedereen&quot;aandeeloptie ontvingen niet automatisch hun toegang tot het project terug. In dit geval moet de gebruiker die het project deelde de optie &quot;Verbinding is actief&quot;toelaten die beschikbaar wanneer het delen van een project met iedereen ([!UICONTROL **Delen**] > [!UICONTROL **Delen met iedereen**] > [!UICONTROL **De koppeling is actief**]), zoals beschreven in [Een project delen met iedereen (geen aanmelding vereist)](/help/analysis-workspace/curate-share/share-projects.md#share-public-link) in [Projecten delen](/help/analysis-workspace/curate-share/share-projects.md).</p></li> <li><p>Deze optie is alleen beschikbaar als SSO in uw organisatie is geïmplementeerd. Voor informatie over hoe de systeembeheerders SSO voor uw organisatie kunnen toelaten, zie [Identiteit instellen en Single Sign-On](https://helpx.adobe.com/enterprise/using/set-up-identity.html){target=_blank}.</p><p>Als SSO voor uw organisatie wordt gevormd, controleer om te zien of wordt om het even welk soort auto-rekening verwezenlijking uitgevoerd in de console. Typisch, zou een systeembeheerder dit opstelling, zoals die in wordt beschreven [Automatisch account maken inschakelen](https://helpx.adobe.com/enterprise/using/automatic-account-creation.html){target=_blank}.</p></li><li><p>Als uw organisatie een vergunning geeft voor het Gezondheidsschild, is deze optie standaard ingeschakeld en kan deze optie niet worden uitgeschakeld.</p></li></ul> |

{style="table-layout:auto"}

## Voorkeuren voor projecten en analyses

U kunt deze voorkeuren aanpassen voor alle nieuwe Analysis Workspace-projecten, nieuwe Analysis Workspace-deelvensters en nieuwe analyses met instructies. Voor informatie over hoe u deze voorkeuren kunt openen, raadpleegt u [Voorkeuren bijwerken](#update-preferences).

Sommige van deze voorkeuren kunnen ook worden aangepast voor afzonderlijke projecten in Analysis Workspace, zoals beschreven in [Overzicht van project](/help/analysis-workspace/build-workspace-project/freeform-overview.md).

Klik op de gekoppelde voorkeurstitels voor meer informatie en context over elke voorkeur.

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Weergave** | | |
|  | [Weergavedichtheid](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html) | Kies hoeveel inhoud u op het scherm wilt weergeven door de verticale opvulling van de linkerrails, vrije-vormtabellen en cohortabellen te verminderen. <ul><li>Compact</li><li>Comfortabel</li><li>Uitgebreid (standaard)</li></ul> |
| | [Kleur, palet](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/color-palettes.html) | Kies de paletten voor visualisatiekleuren die worden gebruikt in Analysis Workspace en de analyse Met instructies. <ul><li> Categorisch palet: toegepast op veel visualisaties in Analysis Workspace en analyse met instructies. Elke kleur vertegenwoordigt een duidelijke categoriale waarde. Kies een optie voor door de Adobe opgegeven opties of voer een aangepast palet in dat met komma&#39;s gescheiden hexwaarden wordt gedefinieerd.</li><li> Divergent palet: toegepast op de Cohort-tabel in Analysis Workspace en analyse met instructies voor groei van gebruiker. Dit palet heeft een numerieke betekenis met twee uiteinden en een basislijn in het midden.<li> Sequentieel palet: toegepast op de geleide analyse van de frequentie-trends (gestapelde balk). Dit palet heeft een numerieke betekenis, van licht tot donker.</li></ul> |
| **Gegevens** | | |
|  | [Gegevens, weergave](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?#report-suite) | Kies uit waar tabellen en visualisaties de gegevens afleiden. <ul><li>Recentste (standaard)</li><li>Specifieke gegevensweergave die is geselecteerd in een lijst</li></ul> |
|  | [Kalender](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?#calendar) | Selecteer uit een lijst van: <ul><li>Door Adobe opgegeven bereiken (standaard is deze maand)</li><li>Aangepast gedefinieerde bereiken</li></ul> |
|  | [Type deelvenster](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html) | <ul><li>Vrije vorm (standaard)</li><li>Leeg</li><li>Snelle inzichten</li></ul> |
|  | Herhalingsinstanties tellen | Geeft aan of herhalingsinstanties worden geteld in rapporten. Met deze instelling (indien geactiveerd) worden bijvoorbeeld meerdere weergaven van opeenvolgende pagina&#39;s op dezelfde pagina behandeld als weergaven van meerdere pagina&#39;s. Als deze optie is uitgeschakeld, tellen ze als een weergave van één pagina. <p>**Opmerking:** Deze instelling heeft alleen invloed op bepaalde metriek (zoals Bezoekingen voor één pagina) en is niet van toepassing op de stroomweergave of op de uitvalweergave.</p> |
|  | Getalnotatie | <ul><li>1.000.00 (standaard)</li><li>1.000,00</li><li>1 000,00</li></ul> |
|  | CSV-scheidingsteken | <ul><li>Komma (standaard)</li><li>Puntkomma</li><li>Colon</li><li>Pijp</li><li>Periode</li><li>Spatie</li><li>Tab</li></ul> |
|  | Annotaties tonen | Kies of annotaties zichtbaar zijn in uw projecten. Zie voor meer informatie over annotaties [Overzicht van annotaties](/help/components/annotations/overview.md). |


## Voorkeuren voor de tabel Vrije vorm

U kunt de voorkeuren voor vrije-vormtabellen aanpassen voor alle nieuwe projecten die u in Analysis Workspace maakt. Voor informatie over hoe u deze voorkeuren kunt openen, raadpleegt u [Voorkeuren bijwerken](#update-preferences).

Sommige van deze voorkeuren kunnen ook worden aangepast voor afzonderlijke tabellen.

Klik op de titels van de gekoppelde sectie voor meer informatie en context over de beschikbare voorkeuren.

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Tabel** | | |
| | Tabeltype | <ul><li>Vrije vorm</li><li>Tabelbuilder</li></ul> |
| | Standaardtabelmetrisch | <ul><li>Voorvallen</li><li>Unieke bezoekers</li><li>Bezoeken</li></ul> |
| | Standaardtabelafmetingen | Kies uit Minuut, Uur, Dag, Week, Maand, Kwart of Jaar. |
| | Datums uitlijnen | Selecteer deze optie als u datums uit elke kolom wilt uitlijnen met alle datums die op dezelfde rij beginnen. |
| **[Kolom](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)** | | |
| | Koptekst van tekstomloop | Hiermee kunt u de koptekst laten omlopen in Freeform-tabellen om kopteksten leesbaarder te maken en tabellen beter deelbaar te maken. Dit is handig voor .pdf-rendering en voor metriek met lange namen. Standaard ingeschakeld. |
| | Totalen tonen | Dit totaal is doorgaans gelijk aan of een subset van de [!UICONTROL Grand Total]. Het geeft alle tabelfilters weer die binnen de vrije-vormtabel worden toegepast, inclusief de [!UICONTROL Include None] -optie. |
| | Totaal tonen | Dit totaal vertegenwoordigt alle gebeurtenissen die zijn verzameld, ook wel &#39;totaal gegevensweergave&#39; genoemd. Wanneer een filter op paneelniveau of binnen de vrije vormlijst wordt toegepast, past dit totaal aan om op alle gebeurtenissen te wijzen die aan de filtercriteria voldoen. Groot totaal wordt niet ondersteund voor tabellen of uitsplitsingen met [statische rijen](/help/analysis-workspace/visualizations/freeform-table/workspace-totals.md). |
| | Menggrijswaarden tonen | Lijngrafieken onder aan het diagram weergeven of verbergen. Als de legenda is verborgen, wordt deze niet langer visueel doorverwezen naar de regels. |
| | Getal | Hiermee wordt bepaald of in een cel de numerieke waarde voor de metrische waarde wordt weergegeven of verborgen. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de numerieke waarde het aantal paginaweergaven voor het rij-item. |
| | Percentage | Bepaalt of een cel de percentagewaarde voor metrisch toont/verbergt. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de percentagewaarde het aantal paginaweergaven voor het rijitem gedeeld door de totale paginaweergaven voor de kolom.  Opmerking: we kunnen percentages van meer dan 100% weergeven, om nauwkeuriger te zijn. We verplaatsen het bovenste gebonden plafond ook naar 1000% om ervoor te zorgen dat kolommen te groot kunnen worden. |
| | anomalieën tonen <!-- This setting was moved from the "Project" tab. this is already in the tool/docs under "Freeform table, But the doc doesn't give a definition. --> | Hiermee wordt bepaald of de waarden in deze kolom een anomaliedetectie uitvoeren. |
| | nul interpreteren als geen waarde | Voor cellen met een waarde 0 bepaalt u of een cel van 0 of een lege cel moet worden weergegeven. Dit is handig wanneer u gegevens bekijkt voor elke dag van een maand, en sommige dagen zijn nog niet gebeurd.  In plaats van &#39;0&#39; voor toekomstige datums weer te geven, kunnen lege cellen worden weergegeven. Grafieken voldoen ook aan deze instelling (ze geven dus geen lijn of balk weer met 0 waarden als deze instelling is ingeschakeld). |
| | Achtergrond | Hiermee wordt bepaald of alle celopmaak, inclusief de staafgrafiek en voorwaardelijke opmaak, in een cel wordt weergegeven of verborgen <ul><li>Staafgrafiek</li> Hiermee wordt een horizontale staafgrafiek weergegeven die de waarde van de cel ten opzichte van het totaal voor de kolom vertegenwoordigt. <li>Voorwaardelijke opmaak</li>Zie Voorwaardelijke opmaak in voor meer informatie over voorwaardelijke opmaak [Kolominstellingen](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)</ul> |
| | Celvoorvertoning | Toont een voorproef van hoe elke cel met de momenteel geselecteerde opmaakopties wordt getoond. |
| **[Rij](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)** | | |
| | Uitsplitsing naar positie | Selecteer deze optie als u wilt dat de uitsplitsing bij de positie van het item blijft en niet bij het item zelf. Zie voor meer informatie over uitsplitsingen [Afmetingen onderverdelingen](/help/components/dimensions/t-breakdown-fa.md). |
| | Percentage berekening | <ul><li>Kolom</li><li>Rij</li></ul> |
| | Kolomtotalen (alleen statische rijen) | <ul><li>De som van rijen weergeven: geeft de som van de afzonderlijke regelitems weer </li><li>Totaal-generaal weergeven: geeft de gedupliceerde som van rijen weer.</li></ul> |

## Voorkeuren voor visualisatie

U kunt de visualisatievoorkeuren bijwerken voor alle nieuwe projecten die u in Analysis Workspace maakt. Voor informatie over hoe u deze voorkeuren kunt openen, raadpleegt u [Voorkeuren bijwerken](#update-preferences).

Sommige van deze voorkeuren kunnen ook worden aangepast voor afzonderlijke visualisaties.

Klik op de titels van de gekoppelde sectie voor meer informatie en context over de beschikbare voorkeuren.

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Algemene standaardinstellingen** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor alle visualisaties. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legendetekst voor alle visualisaties verbergen. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as voor alle visualisaties. Dit kan nuttig zijn als u een grote dataset hebt. |
| | Dubbele as weergeven (indien van toepassing) | Is slechts van toepassing als u twee metriek hebt - u kunt een y-as op de linkerzijde (voor één metrisch) en op het recht (voor andere metrisch) hebben. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Normalisatie (indien van toepassing) | Dwingt metriek tot gelijke verhoudingen. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Y-as anker bij nul | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as NON-ZERO ingesteld als de standaardinstelling van het diagram. Als u dit vakje inschakelt, wordt de y-as gedwongen tot nul (en wordt het diagram opnieuw getekend). |
| | Afwijkingen van schaal Y-as toestaan | Als u veelvoudige metriek in een grafiek hebt, moet u over elke anomalie bewegen om de betrouwbaarheidsband voor die metrisch te zien. De y-as wordt niet automatisch geschaald om de visualisatie beter leesbaar te maken met het betrouwbaarheidsinterval Anomaly-detectie. Met deze optie kan het betrouwbaarheidsinterval de visualisatie schalen. <p>Zie voor meer informatie [anomalieën weergeven in Analysis Workspace](/help/analysis-workspace/virtual-analyst/c-anomaly-detection/view-anomalies.md).</p> |
| **[Lijn](/help/analysis-workspace/visualizations/line.md)** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor de lijnvisualisatie. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor lijnvisualisatie verbergen. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as in de lijnvisualisatie. Dit kan nuttig zijn als u een grote dataset hebt. |
| | Dubbele as weergeven (indien van toepassing) | Is slechts van toepassing als u twee metriek hebt - u kunt een y-as op de linkerzijde (voor één metrisch) en op het recht (voor andere metrisch) hebben. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Normalisatie (indien van toepassing) | Dwingt metriek tot gelijke verhoudingen. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | x-as tonen | Hiermee geeft u de x-as weer op het lijndiagram. |
| | Y-as tonen | Hiermee geeft u de y-as op het lijndiagram weer. |
| | Y-as van anker | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as NON-ZERO ingesteld als de standaardinstelling van het diagram. Als u dit vakje inschakelt, wordt de y-as gedwongen tot nul (en wordt het diagram opnieuw getekend). |
| | min. tonen | Bedek een label voor een minimumwaarde om de dalen snel in metrische vorm te markeren. Opmerking: de hoofdwaarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie. |
| | max. tonen | bedek een label voor de maximumwaarde om de pieken snel in metrisch formaat te markeren. Opmerking: de maximale waarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie. |
| | Trendline tonen | Toon een regressie of bewegende gemiddelde trendline aan uw lijnreeks. Met behulp van trendlines wordt een duidelijker patroon in de gegevens weergegeven. |
| **[Cohort](/help/analysis-workspace/visualizations/cohort-table/t-cohort.md)** | | |
| | Granulariteit | Voor getreneerde visualisaties kunt u de tijdsgranulariteit (Dag, Week, Maand, Kwart, of Jaar) veranderen. Deze wijziging geldt ook voor de gegevensbrontabel. |
| | Alleen percentages weergeven | Hiermee verwijdert u de getalwaarde en geeft u alleen het percentage weer. |
| | Percentages afronden naar dichtstbijzijnde gehele getal | Rondt de percentagewaarde aan het meest dichtbijgelegen geheel in plaats van het tonen van de decimale waarde. |
| | Gemiddelde percentagerij weergeven | Hiermee voegt u een nieuwe rij boven aan de tabel in en voegt u vervolgens het gemiddelde voor de waarden binnen elke kolom toe. |
| **[Combografieken](/help/analysis-workspace/visualizations/combo-charts.md)** | | |
| | X-as tonen | Hiermee geeft u de x-as weer op de Combo-grafiek. |
| | Y-as tonen | Hiermee geeft u de y-as weer op de keuzelijst met invoervak. |
| | Scheepjes weergeven op lijnen | Ballonnen tonen op lijnen in Combo-grafieken. |
| **[Hoofdmetrische samenvatting](/help/analysis-workspace/visualizations/key-metric.md)** | | |
| | Weergavetype Samenvatting | <ul><li>Percentage wijziging benadrukken</li><li>Nummerwaarde benadrukken</li></ul> |
| | Meerdere regels tonen | hoe of verberg lijngrafieken bij de bodem van de grafiek. Als de legenda is verborgen, wordt deze niet langer visueel doorverwezen naar de regels. |
| | max. en min. tonen op vonklines | Minimum- en maximumwaarden tonen op primaire diagrammen en vergelijkingslijngrafieken. |
| | Vergelijking tonen | Vergelijkingsgegevens tonen. Wanneer deze optie is verborgen, worden zowel het vergelijkingsregeldiagram als de summiere wijzigingsobjecten verborgen. |
| | Nummerwaardeopties | In de [!UICONTROL **Hoofdmetrische samenvatting**] sectie <ul><li>Percentage wijziging tonen</li><li>Raw-verschil tonen</li>Onbewerkt verschil tussen de totale waarde van de meting in het primaire datumbereik en het secundaire datumbereik</ul> |
| **[Uitval](/help/analysis-workspace/visualizations/fallout/configuring-fallout.md)** | | |
| | Container | Hiermee kunt u schakelen tussen Bezoek en Bezoeker om het plakken van bezoekers te analyseren. De standaardinstelling is Bezoeker. Met deze instellingen kunt u de betrokkenheid van personen op persoonlijke niveau (tijdens verschillende sessies) begrijpen of de analyse beperken tot één sessie. <p>De volgende opties zijn beschikbaar:</p> <ul><li>Bezoek</li><li>Bezoeker</li></ul> |
| **[Stroom](/help/analysis-workspace/visualizations/c-flow/create-flow.md)** | | |
| | Container | In de [!UICONTROL **Stroom**] sectie <ul><li>Bezoek</li><li>Bezoeker</li></ul> |
| | Labels voor tekstomloop | Normaal gesproken worden de labels op de Flow-elementen ingekort om de schermruimte op te slaan, maar u kunt het volledige label zichtbaar maken door dit selectievakje in te schakelen. Standaard = uitgeschakeld. |
| | Herhalingsinstanties opnemen | Stroomvisualisaties zijn gebaseerd op instanties van een dimensie. Met deze instelling kunt u herhaalde exemplaren, zoals opnieuw laden van pagina&#39;s, opnemen of uitsluiten. Herhalingen kunnen echter niet worden verwijderd uit Flow-visualisaties met multigetaxeerde afmetingen, zoals listVars, listProps, s.product, merchandising Vars, enz. Standaard = uitgeschakeld. |
| | Knopinfo weergeven | Bepaalt of tooltips die knoopgegevens bevatten wanneer het hangen over individuele knopen binnen een stroomvisualisatie worden getoond. |
| | Aantal kolommen | Hiermee bepaalt u hoeveel kolommen u in het stroomdiagram wilt opnemen. |
| | Items uitgevouwen per kolom | Hoeveel punten u in elke kolom wilt. |
| **Gestapelde diagrammen** | | |
| | 100% gestapeld | Met deze instelling op een gestapeld gebied, gestapelde staaf of horizontale staaf verandert u het diagram in een &#39;100% gestapelde&#39; visualisatie. <p>Zie voor meer informatie [Stapel en balk gestapeld](/help/analysis-workspace/visualizations/bar.md).</p> |
| **[Histogram](/help/analysis-workspace/visualizations/histogram.md)** | | |
| | Aantal emmers | Kies het aantal gegevensbereiken (emmers) in de visualisatie. Het maximumaantal emmers is 50. <p>Zie voor meer informatie [Histogram](/help/analysis-workspace/visualizations/histogram.md).</p> |
| | Telmethode | Kies een van de volgende opties: <ul><li>Actief</li><li>Bezoek</li><li>Bezoeker</li></ul> <p>Als u dit bijvoorbeeld gebruikt in combinatie met paginaweergaven, kunt u per persoon paginaweergaven, paginaweergaven voor een bezoek of paginaweergaven per gebeurtenis kiezen. Bij Actief wordt &quot;Voorvallen&quot; gebruikt als de metrische y-as in een vrije-vormtabel.</p> |
| **[Samenvattingswijziging](/help/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Waarde | <!-- Seem to be basically the same options as in "Number value options" --> <ul><li>Percentage wijziging</li><li>Onbewerkt verschil</li></ul> |
| | Percentage | De waarden van vertoningen in percentages voor de Summiere visualisaties van de Verandering. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor de visualisatie Samenvattingswijziging verbergen. |
| **[Samenvattingsnummer](/help/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Percentage | De waarden van vertoningen in percentages voor de Summiere visualisaties van het Aantal. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor de visualisatie Samenvattingsnummer verbergen. |
| | Samenvattingswaarde met | Kies uit Max, Min, Gemiddeld, Mediaan en Sum. |
| | Afkorting | In de [!UICONTROL **Samenvattingsnummer**] sectie |
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

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] **>** [!UICONTROL **Voorkeuren**].

   ![Gebruikersvoorkeuren](assets/user-preferences.png)

1. Selecteer rechtsboven de optie **[!UICONTROL Restore defaults]**.

1. Selecteer **[!UICONTROL Restore defaults]**.

## [!UICONTROL Dark theme]

Als u liever een donkere achtergrond voor uw Adobe Analytics-gebruikersinterface hebt, kunt u schakelen tussen [!UICONTROL Dark theme].

1. Klik op het gebruikerspictogram van het Experience Cloud rechtsboven.

   ![donkerthema](assets/dark-theme.png)

1. Verplaats de **[!UICONTROL Dark theme]** naar rechts.

