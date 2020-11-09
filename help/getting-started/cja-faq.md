---
title: Customer Journey Analytics Veelgestelde vragen
description: Customer Journey Analytics - Veelgestelde vragen.
translation-type: tm+mt
source-git-commit: 3b3d0b0858d559e94f1bed6a31a63b018ed32a23
workflow-type: tm+mt
source-wordcount: '1142'
ht-degree: 1%

---


# Veelgestelde vragen

## Vereisten

| Vraag | Antwoord |
| --- | --- |
| Moet ik [!UICONTROL Private Device Graph] of [!UICONTROL Device Coop] for [!UICONTROL Customer Journey Analytics]? | Nee, [!UICONTROL Private Device Graph] of [!UICONTROL Device Coop] niet vereist zijn voor [!UICONTROL Customer Journey Analytics]. Ze worden zelfs nog niet ondersteund. |
| Moet ik [!UICONTROL Experience Cloud ID] (ECID) voor [!UICONTROL Customer Journey Analytics]? | Nee, [!UICONTROL Customer Journey Analytics] steunt om het even welke identiteitskaart in een dataset, of dat is [!UICONTROL ECID] of een andere id die u kiest. |
| Wat moet ik doen als ik mijn gegevens moet extraheren, transformeren, laden? [!UICONTROL Customer Journey Analytics]? | Vandaag, moet u met een partner ETL (Unifi of Informatica) werken als u uw gegevens moet omzetten alvorens het in AEP te zetten. Als u ETL nodig hebt nadat de gegevens al zijn ingevoerd, [!UICONTROL Adobe Experience Platform Query Services] bevat enkele beperkte opties. |

## Gegevens ophalen

| Vraag | Antwoord |
| --- | --- |
| Kan [!UICONTROL Customer Journey Analytics] &quot;aansluiten&quot; op verschillende apparaten of op verschillende gegevenssets? | Ja. [!UICONTROL Customer Journey Analytics] is een &#39;breng-uw-eigen-identiteitskaart&#39; analysesysteem. We hebben in november 2020 een verstikkende oplossing uitgebracht. Meer informatie. |
| Wordt het stitching van anoniem gedrag aan voor authentiek verklaard gedrag gesteund? | Nee, nog niet. |

## Gegevens ophalen in [!UICONTROL Customer Journey Analytics]

| Vraag | Antwoord |
| --- | --- |
| Kan ik gegevens combineren van verschillende [!UICONTROL Adobe Experience Platform] sandboxen in één [!UICONTROL Customer Journey Analytics] verbinding? | Nee, u hebt geen toegang tot gegevens in verschillende sandboxen. U kunt alleen gegevenssets combineren die zich binnen dezelfde sandbox bevinden. [Meer informatie...](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-connections/create-connection.html#select-sandbox-and-datasets) |
| Wat is de verwachte latentie voor [!UICONTROL Customer Journey Analytics] op [!UICONTROL Adobe Experience Platform]? | <ul><li>Onder normale belasting: &lt; 60 minuten <br>**Opmerking:** In het geval van een ongebruikelijk hoog volume van gegevensstroom door de pijpleiding, zou het tot 24 uren kunnen vergen.</li><li>Backfill-gegevens (tot 13 maanden aan gegevens, ongeacht de grootte): &lt; 4 weken</li></ul> |
| Hoe kan ik online gegevens verbinden met offline gegevens in [!UICONTROL Customer Journey Analytics]? | [!UICONTROL Customer Journey Analytics] is een &#39;breng je eigen id&#39; analysesysteem. Zolang de persoonidentiteitskaart tussen datasets aanpast, [!UICONTROL Customer Journey Analytics] kan segmenten, attributie, stroom, fallout, enz. verbinden over datasets. |
| Hoe kan ik mijn offline gegevens overbrengen naar [!UICONTROL Customer Journey Analytics]? | U moet eerst alle gegevens naar het Experience Platform halen voordat u deze kunt gebruiken [!UICONTROL Customer Journey Analytics]. Het team voor gegevens aan boord van het Experience Platform kan u, indien nodig, aanbevelingen of advies geven. |
| Hoe krijg ik [!UICONTROL Adobe Analytics] gegevens in [!UICONTROL Customer Journey Analytics]? | [!UICONTROL Adobe Analytics] gegevens kunnen via de [Adobe Analytics Source Connector](https://docs.adobe.com/content/help/en/experience-platform/sources/connectors/adobe-applications/analytics.html). Meeste [!UICONTROL Adobe Analytics] velden worden overgedragen in XDM-indeling, maar andere velden zijn nog niet beschikbaar (zoals [!UICONTROL Marketing Channels] afmetingen). |
| Hoe lang duurt het om datasetelementen in een gegevensmening samen te stellen? | Een paar uur om te beginnen en een paar dagen om een back-up te maken van de laatste 13 maanden van gegevens. |
| Is het noodzakelijk om PII gegevens te brengen om verbindingen tussen de gegevens te vestigen? | Nr, kunt u om het even welke identiteitskaart, met inbegrip van een knoeiboel van een klant identiteitskaart gebruiken, die geen PII is. |

## Traditioneel [!UICONTROL Adobe Analytics] componenten

| Vraag | Antwoord |
| --- | --- |
| Wat betekent dit voor onze traditionele [!UICONTROL Adobe Analytics] product? | [!UICONTROL Customer Journey Analytics] is ons product van de volgende generatie. Overschakelen van onze huidige producten naar [!UICONTROL Customer Journey Analytics] zal jaren en veel coördinatie vergen . Voor meer informatie raadpleegt u [Ondersteuning voor Customer Journey Analytics-functies](/help/getting-started/cja-aa.md). |
| Kan ik segmenten delen van [!UICONTROL Customer Journey Analytics] naar AEP of andere oplossingen? | Nog niet. We zijn op zoek naar nieuwe, innovatieve manieren om segmenten te delen van [!UICONTROL Customer Journey Analytics] naar AEP in de toekomst zonder zo&#39;n lange vertraging. Dat gezegd, kunt u de output van de Diensten van de Vraag aan Verenigd Profiel als potentiële alternerende actie delen. |
| Wat is er gebeurd met mijn oude eVar-omgeving? | Vars, props en gebeurtenissen in de traditionele Adobe Analytics-zin bestaan niet meer in [!UICONTROL Customer Journey Analytics]. U hebt onbeperkte schema-elementen (afmetingen, metriek, lijstvelden). Zo worden alle attributie montages u gebruikte om tijdens het proces van de gegevensinzameling toe te passen nu toegepast bij vraagtijd. |
| Waar zijn al mijn zitting en veranderlijke persistentie montages nu? | [!UICONTROL Customer Journey Analytics] Hiermee past u al deze instellingen toe tijdens de rapporttijd. Deze instellingen worden nu live weergegeven in de gegevensweergave. De wijzigingen in deze instellingen zijn nu retroactief en u kunt meerdere versies gebruiken door meerdere gegevensweergaven te gebruiken! |
| Wat gebeurt er met onze bestaande segmenten/berekende maatstaven? | [!UICONTROL Customer Journey Analytics] gebruikt niet langer eVars, props of gebeurtenissen en gebruikt in plaats daarvan een AEP-schema. Dit betekent dat geen van de bestaande segmenten of statistische gegevens compatibel zijn met [!UICONTROL Customer Journey Analytics]. |
| Hoe werkt [!UICONTROL Customer Journey Analytics] handgreep `Uniques Exceeded` beperkingen? | [!UICONTROL Customer Journey Analytics] heeft geen unieke waardebeperkingen, dus hoeft u zich daar geen zorgen over te maken! |
| Als ik een bestaande [!DNL Data Workbench] klant, kan ik naar [!UICONTROL Customer Journey Analytics] nu? | Het hangt ervan af. Als u sterk op het Verenigde Proces van de Klant (UCP) vertrouwt, zult u willen wachten tot wij het stitching uitgevoerd hebben. Als u reeds hoge klantenauthentificatiecijfers hebt, of als u al uw gegevens op één plaats wilt, of van eVars zou willen schrappen, zou Customer Journey Analytics een goede pasvorm kunnen zijn. |

## Implicaties van het verwijderen van gegevenscomponenten

Wat de schrapping betreft, gaat het om zes onderdelen: zandbak, schema, dataset, verbinding, gegevensmening, en de projecten van de Werkruimte. Hier zijn enkele mogelijke scenario&#39;s voor het verwijderen van een van deze componenten:

| Wat als ik... | Dit gebeurt... |
| --- | --- |
| Een sandbox verwijderen in [!UICONTROL Adobe Experience Platform]? | Als u een sandbox verwijdert, worden eventuele [!UICONTROL Customer Journey Analytics] verbindingen met gegevenssets in die sandbox. Gegevenssets in CJA worden momenteel echter niet verwijderd. |
| Schema&#39;s verwijderen in [!UICONTROL Adobe Experience Platform], maar niet de dataset(s) verbonden aan dit schema? | [!UICONTROL Adobe Experience Platform] staat niet toe dat schema&#39;s worden geschrapt die één of meerdere datasets verbonden aan hen hebben. Nochtans, kan Admin met de aangewezen reeks rechten de datasets eerst schrappen en dan het schema schrappen. |
| Een gegevensset verwijderen in [!UICONTROL Adobe Experience Platform]? | Er is geen melding in [!UICONTROL Customer Journey Analytics]; echter, als het stromen gegevens wordt aangezet, zouden geen nieuwe gegevens binnen komen na de tijd de datasets werden geschrapt.<br>Met andere woorden, als de instelling **[!UICONTROL Automatically import all new datasets in this connection, beginning today]** in de verbinding wordt toegelaten, zouden geen nieuwe gegevens binnen komen na de tijd de datasets werden geschrapt. |
| Een gegevensset verwijderen in [!UICONTROL Customer Journey Analytics]? | U kunt momenteel geen dataset verwijderen binnen een verbinding die is opgeslagen. U moet de gehele verbinding verwijderen en opnieuw beginnen. (U kunt echter wel een gegevensset verwijderen in [!UICONTROL Adobe Experience Platform].) |
| Een batch verwijderen uit een dataset (in [!UICONTROL Adobe Experience Platform])? | Als de batch al in [!UICONTROL Customer Journey Analytics], [!UICONTROL Customer Journey Analytics] is zich momenteel niet bewust van dat de partij is geschrapt. Als de partij niet is ingeslikt, kan deze uiteraard niet meer worden ingenomen zodra deze is verwijderd in [!UICONTROL Adobe Experience Platform]. |
| Een batch verwijderen **tijdens de inname** in [!UICONTROL Customer Journey Analytics]? | Als er slechts één partij in de dataset is, zullen geen gegevens of gedeeltelijke gegevens van die partij in verschijnen [!UICONTROL Customer Journey Analytics]. De inname wordt teruggedraaid. Als, bijvoorbeeld, er 5 partijen in de dataset zijn en 3 van hen reeds zijn opgenomen toen de dataset werd geschrapt, zullen de gegevens van die 3 partijen in verschijnen [!UICONTROL Customer Journey Analytics]. |
| Een verbinding verwijderen in [!UICONTROL Customer Journey Analytics]? | Een foutbericht geeft aan dat:<ul><li>De gegevensweergaven die voor de verwijderde verbinding zijn gemaakt, werken niet meer.</li><li> Op dezelfde manier zullen om het even welke projecten van de Werkruimte die van gegevensmeningen in de geschrapte verbinding afhangen ophouden werkend.</li></ul> |
| Een gegevensweergave verwijderen in [!UICONTROL Customer Journey Analytics]? | Een foutenmelding zal erop wijzen dat om het even welke projecten van de Werkruimte die van deze geschrapte gegevensmening afhangen niet meer werkend zullen zijn. |
| Een Workspace-project verwijderen in [!UICONTROL Customer Journey Analytics]? | U kunt het project opnieuw maken of u kunt een tijdelijke oplossing gebruiken om het project te herstellen. Ga gewoon door naar [!UICONTROL Admin > Logs > Usage and Access Log], zoek het verwijderde project en kopieer de id ervan. Open vervolgens een werkruimteproject en werk de id in de URL bij met de gekopieerde werkruimte. Sla het project vervolgens op. |
