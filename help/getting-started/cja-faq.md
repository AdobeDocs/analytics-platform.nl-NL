---
title: Customer Journey Analytics Veelgestelde vragen
description: Customer Journey Analytics - Veelgestelde vragen.
exl-id: 778ed2de-bc04-4b09-865e-59e386227e06
translation-type: tm+mt
source-git-commit: 76260b7362396c76942dadab599607cd038ed651
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 1%

---

# Veelgestelde vragen

## Vereisten

| Vraag | Antwoord |
| --- | --- |
| Heb ik [!UICONTROL Private Device Graph] of [!UICONTROL Device Coop] voor [!UICONTROL Customer Journey Analytics] nodig? | Nee, [!UICONTROL Private Device Graph] of [!UICONTROL Device Coop] zijn niet vereist voor [!UICONTROL Customer Journey Analytics]. Ze worden zelfs nog niet ondersteund. |
| Heb ik [!UICONTROL Experience Cloud ID] (ECID) voor [!UICONTROL Customer Journey Analytics] nodig? | Nr, [!UICONTROL Customer Journey Analytics] steunt om het even welke identiteitskaart in een dataset, of dat [!UICONTROL ECID] of een andere identiteitskaart is u kiest. |
| Wat als ik (Extraheren, Transformeren, Laden) mijn gegevens vóór [!UICONTROL Customer Journey Analytics] moet ETL? | Vandaag, moet u met een partner ETL (Unifi of Informatica) werken als u uw gegevens moet omzetten alvorens het in AEP te zetten. Als u ETL nodig hebt nadat de gegevens al zijn ingevoerd, biedt [!UICONTROL Adobe Experience Platform Query Services] enkele beperkte opties. |

## Gegevens ophalen

| Vraag | Antwoord |
| --- | --- |
| Kan [!UICONTROL Customer Journey Analytics] &quot;aansluiten&quot;over apparaten of over datasets? | Ja. [!UICONTROL Customer Journey Analytics] is een &#39;breng-uw-eigen-identiteitskaart&#39; analysesysteem. We hebben in november 2020 een verstikkende oplossing uitgebracht. Meer informatie. |
| Wordt het stitching van anoniem gedrag aan voor authentiek verklaard gedrag gesteund? | Nee, nog niet. |

## Gegevens ophalen in [!UICONTROL Customer Journey Analytics]

| Vraag | Antwoord |
| --- | --- |
| Kan ik gegevens van verschillende [!UICONTROL Adobe Experience Platform] zandbakken in één [!UICONTROL Customer Journey Analytics] verbinding combineren? | Nee, u hebt geen toegang tot gegevens in verschillende sandboxen. U kunt alleen gegevenssets combineren die zich binnen dezelfde sandbox bevinden. [Meer informatie...](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-connections/create-connection.html#select-sandbox-and-datasets) |
| Wat is de verwachte latentie voor [!UICONTROL Customer Journey Analytics] op [!UICONTROL Adobe Experience Platform]? | <ul><li>Onder normale belasting: &lt; 60 minuten <br>**Opmerking:** In het geval van een ongebruikelijk hoog gegevensvolume door de pijpleiding, kan het tot 24 uur duren.</li><li>Backfill-gegevens (tot 13 maanden aan gegevens, ongeacht de grootte): &lt; 4 weken</li></ul> |
| Hoe verbind ik online gegevens met off-line gegevens in [!UICONTROL Customer Journey Analytics]? | [!UICONTROL Customer Journey Analytics] is een &#39;breng je eigen id&#39; analysesysteem. Zolang de persoonidentiteitskaart tussen datasets aanpast, [!UICONTROL Customer Journey Analytics] filters, attributie, stroom, fallout, enz. kan verbinden over datasets. |
| Hoe breng ik mijn off-line gegevens in [!UICONTROL Customer Journey Analytics]? | U moet eerst om het even welke gegevens brengen aan Experience Platform alvorens u het met [!UICONTROL Customer Journey Analytics] kunt gebruiken. Het team voor gegevens aan boord van het Experience Platform kan u, indien nodig, aanbevelingen of advies geven. |
| Hoe krijg ik [!UICONTROL Adobe Analytics] gegevens in [!UICONTROL Customer Journey Analytics]? | [!UICONTROL Adobe Analytics] gegevens kunnen via de  [Adobe Analytics Source Connector](https://docs.adobe.com/content/help/en/experience-platform/sources/connectors/adobe-applications/analytics.html) op het Experience Platform worden aangesloten. De meeste [!UICONTROL Adobe Analytics] gebieden worden gebracht over in formaat XDM, maar andere gebieden zijn nog niet beschikbaar (zoals [!UICONTROL Marketing Channels] afmetingen). |
| Hoe lang duurt het om datasetelementen in een gegevensmening samen te stellen? | Een paar uur om te beginnen en een paar dagen om een back-up te maken van de laatste 13 maanden van gegevens. |
| Is het noodzakelijk om PII gegevens te brengen om verbindingen tussen de gegevens te vestigen? | Nr, kunt u om het even welke identiteitskaart, met inbegrip van een knoeiboel van een klant identiteitskaart gebruiken, die geen PII is. |

## Traditionele [!UICONTROL Adobe Analytics]-componenten

| Vraag | Antwoord |
| --- | --- |
| Wat betekent dit voor ons traditionele [!UICONTROL Adobe Analytics] product? | [!UICONTROL Customer Journey Analytics] is ons product van de volgende generatie. Het evolueren van onze huidige producten naar [!UICONTROL Customer Journey Analytics] zal jaren en veel coördinatie vergen. Raadpleeg [Ondersteuning van Customer Journey Analytics-functies](/help/getting-started/cja-aa.md) voor meer informatie. |
| Kan ik filters van [!UICONTROL Customer Journey Analytics] aan AEP of andere oplossingen delen? | Nog niet. We zijn op zoek naar nieuwe, innovatieve manieren om filters van [!UICONTROL Customer Journey Analytics] naar AEP te delen in de toekomst die niet zo lang wachten. Dat gezegd, kunt u de output van de Diensten van de Vraag aan Verenigd Profiel als potentiële alternerende actie delen. |
| Wat is er gebeurd met mijn oude eVar-omgeving? | Vars, props en gebeurtenissen in de traditionele Adobe Analytics-betekenis bestaan niet meer in [!UICONTROL Customer Journey Analytics]. U hebt onbeperkte schema-elementen (afmetingen, metriek, lijstvelden). Zo worden alle attributie montages u gebruikte om tijdens het proces van de gegevensinzameling toe te passen nu toegepast bij vraagtijd. |
| Waar zijn al mijn zitting en veranderlijke persistentie montages nu? | [!UICONTROL Customer Journey Analytics] Hiermee past u al deze instellingen toe tijdens de rapporttijd. Deze instellingen worden nu live weergegeven in de gegevensweergave. De wijzigingen in deze instellingen zijn nu retroactief en u kunt meerdere versies gebruiken door meerdere gegevensweergaven te gebruiken! |
| Wat gebeurt er met onze bestaande segmenten/berekende maatstaven? | [!UICONTROL Customer Journey Analytics] gebruikt niet langer eVars, props of gebeurtenissen en gebruikt in plaats daarvan een AEP-schema. Dit betekent geen van de bestaande segmenten of de cijfers van de calc compatibel met [!UICONTROL Customer Journey Analytics] zijn. |
| Hoe behandelt [!UICONTROL Customer Journey Analytics] `Uniques Exceeded` beperkingen? | [!UICONTROL Customer Journey Analytics] heeft geen unieke waardebeperkingen, dus hoeft u zich daar geen zorgen over te maken! |
| Als ik een bestaande [!DNL Data Workbench] klant ben, kan ik nu naar [!UICONTROL Customer Journey Analytics] gaan? | Het hangt ervan af. Als u sterk op het Verenigde Proces van de Klant (UCP) vertrouwt, zult u willen wachten tot wij het stitching uitgevoerd hebben. Als u reeds hoge klantenauthentificatiecijfers hebt, of als u al uw gegevens op één plaats wilt, of van eVars zou willen schrappen, zou Customer Journey Analytics een goede pasvorm kunnen zijn. |

## Implicaties van het verwijderen van gegevenscomponenten

Wat de schrapping betreft, gaat het om zes onderdelen: zandbak, schema, dataset, verbinding, gegevensmening, en de projecten van de Werkruimte. Hier zijn enkele mogelijke scenario&#39;s voor het verwijderen van een van deze componenten:

| Wat als ik... | Dit gebeurt... |
| --- | --- |
| Een sandbox verwijderen in [!UICONTROL Adobe Experience Platform]? | Als u een sandbox verwijdert, wordt de gegevensstroom naar [!UICONTROL Customer Journey Analytics]-verbindingen met gegevenssets in die sandbox gestopt. Verbindingen in CJA die aan die sandbox zijn gekoppeld, worden momenteel niet automatisch verwijderd. |
| Schrap een schema in [!UICONTROL Adobe Experience Platform], maar niet de dataset/s verbonden aan dit schema? | [!UICONTROL Adobe Experience Platform] staat niet toe dat schema&#39;s worden geschrapt die één of meerdere datasets verbonden aan hen hebben. Nochtans, kan Admin met de aangewezen reeks rechten de datasets eerst schrappen en dan het schema schrappen. |
| Een gegevensset verwijderen in [!UICONTROL Adobe Experience Platform]? | Het schrappen van een dataset in AEP zal gegevensstroom van die dataset aan om het even welke Verbindingen tegenhouden die die dataset omvatten. Om het even welke gegevens van die dataset worden niet automatisch geschrapt van bijbehorende Verbindingen CJA. |
| Een gegevensset verwijderen in [!UICONTROL Customer Journey Analytics]? | U kunt momenteel geen dataset verwijderen binnen een verbinding die is opgeslagen. U moet de gehele verbinding verwijderen en opnieuw beginnen. (U kunt echter een gegevensset verwijderen in [!UICONTROL Adobe Experience Platform].) |
| Een batch uit een dataset verwijderen (in [!UICONTROL Adobe Experience Platform])? | Als een partij uit een [!UICONTROL Adobe Experience Platform] dataset wordt geschrapt, zal de zelfde partij uit om het even welke Verbindingen worden verwijderd CJA die die specifieke partij bevatten.  CJA wordt op de hoogte gesteld van het verwijderen van batches in [!UICONTROL Adobe Experience Platform]. |
| Wilt u een batch **verwijderen terwijl deze in** wordt opgenomen?[!UICONTROL Customer Journey Analytics] | Als er slechts één partij in de dataset is, zullen geen gegevens of gedeeltelijke gegevens van die partij in [!UICONTROL Customer Journey Analytics] verschijnen. De inname wordt teruggedraaid. Als, bijvoorbeeld, er 5 partijen in de dataset zijn en 3 van hen reeds zijn opgenomen toen de dataset werd geschrapt, zullen de gegevens van die 3 partijen in [!UICONTROL Customer Journey Analytics] verschijnen. |
| Een verbinding verwijderen in [!UICONTROL Customer Journey Analytics]? | Een foutbericht geeft aan dat:<ul><li>De gegevensweergaven die voor de verwijderde verbinding zijn gemaakt, werken niet meer.</li><li> Op dezelfde manier zullen om het even welke projecten van de Werkruimte die van gegevensmeningen in de geschrapte verbinding afhangen ophouden werkend.</li></ul> |
| Een gegevensweergave verwijderen in [!UICONTROL Customer Journey Analytics]? | Een foutenmelding zal erop wijzen dat om het even welke projecten van de Werkruimte die van deze geschrapte gegevensmening afhangen niet meer werkend zullen zijn. |
