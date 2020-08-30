---
title: Gegevensweergaven en -toewijzing configureren
description: Beschrijft hoe te om een gegevensmening aan een dataset van het Platform in de Analyse van de Reis van de Klant te creëren
translation-type: tm+mt
source-git-commit: e32311ce4975107e1b7ca2cb2eaadc2c68a93c92
workflow-type: tm+mt
source-wordcount: '1520'
ht-degree: 1%

---


# Component- en attributie-instellingen

Vars, props en events in de traditionele Adobe Analytics-betekenis bestaan niet meer in Klantreisanalyse. In plaats daarvan, hebt u onbeperkte schemaelementen (afmetingen, metriek, lijstgebieden). Alle attributiemontages die u gebruikte om op eVars en steunen tijdens het proces van de gegevensinzameling toe te passen worden nu toegepast in vraagtijd - ook gekend als rapport-tijd verwerking.

Klik [hier](https://docs.adobe.com/content/help/en/platform-learn/tutorials/cja/attribution-settings-in-data-views.html) voor een videooverzicht.

Houd dit in mening alvorens u attributie montages toepast:

* In het gebruikersinterface van de gegevensmeningen, specificeert u de standaardattributen. **Opmerking**: Op een recentere datum, zult u deze montages in de projecten van de Werkruimte met voeten kunnen treden. Nochtans, is deze functionaliteit momenteel niet beschikbaar.

* De montages van de attributen in de Analyse van de Reis van de Klant zijn niet destructief en retroactief. Met andere woorden, kunt u geen onherstelbare schade aan uw datasets in de Analyse van de Reis van de Klant doen. Zelfs als u per ongeluk iets verwijdert, kunt u altijd teruggaan naar [!UICONTROL Experience Platform] en breng de dataset terug binnen. (Houd in mening, echter, dat het terugbrengen van de dataset binnen extra kosten zal veroorzaken.)

* Als u een afmeting &quot;gedraagt&quot;zoals een traditionele eVar (omzettingsvariabele) wenst te hebben, zou u het met de attributen van het &quot;Laatste Aanraakbezoek&quot;door gebrek moeten vormen.

* Als u een afmeting &quot;gedraagt&quot;zoals een traditionele hulp (verkeersvariabele) wenst te hebben, zou u het met &quot;Zelfde Aanraking&quot;attributen door gebrek moeten vormen.

* Als u wenst om metrisch &quot;gedrag&quot;als standaard metrisch te hebben, zou u om het even wat niet moeten veranderen.

* De montages van de attributen voor metriek treden attributie montages voor afmetingen met voeten.

## Onderdeelinstellingen en toewijzingsinstellingen opgeven

Nadat u [instellingen voor gegevensweergave instellen en opslaan](/help/data-views/create-dataview.md) en toegevoegde componenten, bent u bereid om attributie montages te specificeren, als u verkiest om dit te doen. U kunt attributie/afloop/terugkijkmontages voor afmetingen en metriek specificeren. Als, bijvoorbeeld, u attributie voor een afmeting wilt voortbestaan, zult u waarschijnlijk een tijd van de douaneafloop willen plaatsen. Bijvoorbeeld, als u een &quot;het Volgen code&quot;dimensie (een campagnevariabele) aan de attributen van de &quot;Laatste Aanraking&quot;wilt voortbestaan voor een week, voeg een douanevervalsing van 1 week toe.

>[!IMPORTANT]
>U kunt verkiezen om geen toewijzing/afloop te plaatsen. In dat geval zullen de afmetingen zich gedragen als steunbetuigingen (&quot;Zelfde aanraking&quot;). De metriek zonder attributie de vastgestelde montages zullen de montages voor de afmeting erven die dit metrisch wordt toegepast op.

![](assets/edit-component.png)

1. Specificeer component en attributie montages voor afmetingen en metriek. Zie hieronder voor informatie over de afzonderlijke instellingen.

1. Klik **[!UICONTROL Save]** om uw gegevensweergave op te slaan.


### Componentinstellingen

U kunt de naam van metrisch of afmeting in iets veranderen gebruikersvriendelijker. Merk op dat de onderliggende naam niet verandert, enkel de vertoningsnaam.

### Attributiemodel

Het model beschrijft de distributie van omzettingen in de gebeurtenissen in een groep. Bijvoorbeeld, eerste aanraking of laatste aanraking. Bepaalt hoe de Analyse van de Reis van de Klant krediet voor een succesgebeurtenis toewijst als een variabele veelvoudige waarden vóór de gebeurtenis ontvangt.

| UI-pictogram | Attributiemodel | Definitie | Wanneer te gebruiken |
| --- | --- | --- | --- |
| ![Laatste aanraking](assets/last_touch1.png) | Laatste aanraking | Geeft 100% krediet aan het aanrakingspunt dat onlangs voor omzetting voorkomt. | Het meest fundamentele en gemeenschappelijke attributiemodel. Het wordt vaak gebruikt voor omzettingen met een korte bezinningscyclus. Last Touch wordt algemeen gebruikt door teams die zoekmarketing beheren of interne zoektrefwoorden analyseren. |
| ![Eerste aanraking](assets/first_touch.png) | Eerste aanraking | Geeft 100% krediet aan het aanrakingspunt dat eerst in het de terugkijkvenster van de attributie wordt gezien. | Een ander gemeenschappelijk attributiemodel dat nuttig is voor het analyseren van marketingkanalen die bedoeld zijn om merkbekendheid te geven of klanten aan te schaffen. Het wordt vaak gebruikt door tentoonstellings of sociale marketing teams, maar is ook groot voor het beoordelen van de doeltreffendheid van de onsite productaanbeveling. |
| ![Zelfde aanraking](assets/same_touch.png) | Zelfde aanraking | Geeft 100% krediet aan de zeer hit waar de conversie plaatsvond. Als een aanrakingspunt niet op de zelfde klap zoals een omzetting gebeurt, wordt het geknipt onder &quot;niets&quot;. | Een nuttig model wanneer het evalueren van de inhoud of de gebruikerservaring die onmiddellijk op het tijdstip van omzetting werd voorgesteld. Product- of ontwerpteams gebruiken vaak dit model om de effectiviteit van een pagina te beoordelen waar conversie plaatsvindt. |
| ![Lineair](assets/linear.png) | Lineair | Biedt evenveel krediet aan elk aanraakpunt dat wordt gezien voor een conversie. | Nuttig voor conversies met langere evaluatiecycli of gebruikerservaringen die een frequentere klantenservice nodig hebben. Het wordt vaak gebruikt door teams die mobiele app berichtdoeltreffendheid of met op abonnement-gebaseerde producten meten. |
| ![U-vorm](assets/u_shaped.png) | U-vorm | Geeft 40% krediet aan de eerste interactie, 40% krediet aan de laatste interactie, en verdeelt de resterende 20% aan om het even welke aanrakingspunten binnen. Voor omzettingen met één aanraakpunt, wordt 100% krediet gegeven. Voor omzettingen met twee aanrakingspunten, wordt 50% krediet gegeven aan allebei. | Een goed model voor degenen die interacties waarderen die een omzetting introduceerden of gesloten, maar nog willen het bijstaan van interactie erkennen. U-vormige attributie wordt algemeen gebruikt door teams die een evenwichtiger benadering nemen maar meer krediet aan kanalen willen geven die een omzetting vonden of sluiten. |
| ![J-Shaped](assets/j_shaped.png) | J-Shaped | Geeft 60% krediet aan de laatste interactie, 20% krediet aan de eerste interactie, en verdeelt de resterende 20% aan om het even welke aanrakingspunten binnen. Voor omzettingen met één aanraakpunt, wordt 100% krediet gegeven. Voor omzettingen met twee aanrakingspunten, wordt 75% krediet gegeven aan de laatste interactie, en wordt 25% krediet gegeven aan de eerste. | Dit model is groot voor degenen die aan vinders en sluiters voorrang geven, maar zich bij het sluiten van interactie willen concentreren. J-vormige attributie wordt vaak gebruikt door teams die een evenwichtiger benadering kiezen en meer krediet willen verlenen aan kanalen die een omzetting sluiten. |
| ![Inverse J-vorm](assets/inverse_j.png) | Invers J | Geeft 60% krediet aan het eerste aanraakpunt, 20% krediet aan het laatste aanraakpunt, en verdeelt de resterende 20% aan om het even welke aanrakingspunten binnen. Voor omzettingen met één aanraakpunt, wordt 100% krediet gegeven. Voor omzettingen met twee aanrakingspunten, wordt 75% krediet gegeven aan de eerste interactie, en wordt 25% krediet gegeven aan het laatste. | Dit model is ideaal voor degenen die aan vinders en sluiters voorrang geven, maar zich op het vinden van interactie willen concentreren. De omgekeerde eigenschap van J wordt gebruikt door teams die een evenwichtiger benadering kiezen en meer krediet aan kanalen willen geven die een omzetting in werking stelden. |
| ![Aangepast](assets/custom.png) | Aangepast | Hiermee kunt u het gewicht opgeven dat u wilt geven aan de eerste aanraakpunten, de laatste aanraakpunten en alle tussenliggende aanraakpunten. De gespecificeerde waarden worden genormaliseerd aan 100% zelfs als de ingegane douanenummers niet aan 100 toevoegen. Voor omzettingen met één aanraakpunt, wordt 100% krediet gegeven. Voor interactie met twee aanrakingspunten, wordt de middenparameter genegeerd. De eerste en laatste aanraakpunten worden dan genormaliseerd aan 100%, en de kredieten worden dienovereenkomstig toegewezen. | Dit model is ideaal voor diegenen die volledige controle over hun toewijzingsmodel willen en specifieke behoeften hebben waaraan andere toewijzingsmodellen niet voldoen. |
| ![Tijdsvertraging](assets/time_decay.png) | Tijd-Verval | Volgt en exponentieel verval met een parameter van de douanehalfwaardetijd, waar het gebrek 7 dagen is. Het gewicht van elk kanaal hangt van de hoeveelheid tijd af die tussen de initiatie van het aanrakingspunt en de uiteindelijke omzetting overging. De formule voor de bepaling van het krediet is `2`<sup>`(-t/halflife)`</sup>, waarbij `t` is de hoeveelheid tijd tussen een aanraakpunt en een conversie. Alle aanraakpunten worden dan genormaliseerd tot 100%. | Ideaal voor teams die regelmatig videoreclame maken of op de markt brengen tegen evenementen met een vooraf bepaalde datum. Hoe langer een conversie plaatsvindt na een marketinggebeurtenis, hoe minder krediet wordt gegeven. |
| ![Deelname](assets/participation.png) | Deelname | Biedt 100% krediet aan alle unieke aanraakpunten. Het totale aantal omzettingen wordt opgepompt in vergelijking met andere toerekeningsmodellen. De participatie dedupliceert kanalen die veelvoudige tijden worden gezien. | Uitstekend om te begrijpen wie vaak aan een bepaalde interactie wordt blootgesteld. De organisaties van media gebruiken vaak dit model om inhoudssnelheid te berekenen. De detailhandelorganisaties gebruiken vaak dit model om te begrijpen welke delen van hun plaats aan omzetting kritiek zijn. |

### Vervaldatum

Specificeert een tijdspanne, of een gebeurtenis, waarna het afmetingspunt verloopt (ontvangt niet meer krediet voor succesgebeurtenissen). U kunt het attributieverstrijken op de zitting, de persoon, of het douaneniveau plaatsen.

| Instelling | Definitie |
|---|---|
| Sessie | Vroeger het &#39;Visit&#39;-niveau genoemd. De gebeurtenissen van de omzetting voorbij de paginamening of de zitting associëren niet met de afmeting of metrisch. |
| Persoon (rapportagevenster) | Vroeger het &quot;Bezoekerniveau&quot; genoemd. De gebeurtenissen van de omzetting niet verbonden aan deze persoon associëren niet met de afmeting of metrisch. |
| Aangepaste tijd | Specificeer de douanemomenten, de uren, de dagen, de maanden, of de kwartalen. De gebeurtenissen van de omzetting voorbij de gespecificeerde tijdspanne associëren niet met de afmeting of metrisch. |

Voor meer informatie, zie [Attributie IQ doc](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html).

### Referentievenster

Een terugkijkvenster is de hoeveelheid tijd een omzetting zou moeten terugkijken om aanrakingspunten te omvatten. De modellen van de attributen die meer krediet aan eerste interactie geven zien grotere verschillen wanneer het bekijken van verschillende raadplegingsvensters.

* **Zitting:** Het kijkt terug naar het begin van een sessie waar een conversie plaatsvond. De de raadplegingsvensters van het bezoek zijn smal, aangezien zij niet voorbij de zitting kijken. De de raadplegingsvensters van de zitting respecteren de gewijzigde bezoekdefinitie in gegevensmeningen.
* **Persoon (rapportagevenster):** Bekijk alle zittingen file tot de 1st van de maand van de huidige datumwaaier. De de raadplegingsvensters van de persoon zijn breed, aangezien zij vele zittingen kunnen overspannen. Bijvoorbeeld, als de waaier van de rapportdatum 15 september - september 30 is, omvat de waaier van de persoonshadbackdatum 1 - september 30.
