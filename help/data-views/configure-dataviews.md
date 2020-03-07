---
title: Gegevensweergaven en -toewijzing configureren
description: Beschrijft hoe te om een gegevensmening aan een dataset van het Platform in de Analyse van de Reis van de Klant te creëren
translation-type: tm+mt
source-git-commit: c85b5d2e702a38aa6569da893a25bacd39604f8a

---


# Instellingen voor componenten en toewijzingen

Vars, de steunen, en de gebeurtenissen in de traditionele betekenis van de Analyse van Adobe bestaan niet meer in de Analyse van de Reis van de Klant. In plaats daarvan, hebt u onbeperkte schemaelementen (afmetingen, metriek, lijstgebieden). Alle attributie montages die u gebruikte om op eVars en steunen tijdens het proces van de gegevensinzameling toe te passen worden nu toegepast op vraagtijd - ook genoemd geworden rapport-tijd verwerking.

Klik [hier](https://docs.adobe.com/content/help/en/platform-learn/tutorials/cja/attribution-settings-in-data-views.html) voor een videooverzicht.

Houd dit in mening alvorens u attributie montages toepast:

* In het gebruikersinterface van gegevensmeningen, specificeert u de standaardattributie. **Opmerking**: Op een recentere datum, zult u deze montages in de projecten van de Werkruimte kunnen met voeten treden. Nochtans, is deze functionaliteit momenteel niet beschikbaar.

* De montages van de attributen in de Analyse van de Reis van de Klant zijn niet-destructief en retroactief. Met andere woorden, kunt u geen onherstelbare schade aan uw datasets in de Analyse van de Reis van de Klant doen. Zelfs als u toevallig iets schrapt, kunt u altijd terug naar het Platform van de Ervaring gaan en de dataset terugbrengen binnen. (Houd in mening, echter, dat het terugbrengen van de dataset in extra kosten zal veroorzaken.)

* Als u een afmeting &quot;gedraagt zich&quot;zoals een traditionele Var (omzettingsvariabele) wenst te hebben, zou u het met &quot;Laatste Bezoek van de Aanraking&quot;attributen door gebrek moeten vormen.

* Als u wenst om een afmeting &quot;te hebben gedraagt zich&quot;zoals een traditionele hulp (verkeersvariabele), zou u het met &quot;Zelfde Aanraking&quot;attributen door gebrek moeten vormen.

* Als u wenst om metrisch &quot;gedraag&quot;als standaard metrisch te hebben, zou u om het even wat niet moeten veranderen.

* De montages van de attributen voor metriek treden attributie montages voor afmetingen met voeten.

## Onderdeelinstellingen en toewijzingsinstellingen opgeven

Nadat u de instellingen [van de gegevensweergave en de toegevoegde componenten hebt](/help/data-views/create-dataview.md) ingesteld en opgeslagen, bent u klaar om de toewijzingsinstellingen op te geven als u dit wilt doen. U kunt attributie/afloop/terugkijkmontages voor afmetingen en metriek specificeren. Als, bijvoorbeeld, u attributie voor een afmeting wilt voortbestaan, zult u waarschijnlijk een tijd van de douanebeëindiging willen plaatsen. Bijvoorbeeld, als u een &quot;Volgende code&quot;afmeting (een campagnevariabele) wilt die aan de attributen van de &quot;Laatste Aanraking&quot;wordt geplaatst om voor een week te blijven bestaan, voeg een douanevervalsing van 1 week toe.

>[!IMPORTANT]
>U kunt verkiezen om geen toewijzing/afloop te plaatsen. In dat geval zullen de afmetingen zich gedragen als... . De metriek zonder attributie de vastgestelde montages zullen de montages voor de afmeting erven dat dit metrisch wordt toegepast op.

![](assets/edit-component.png)

1. Specificeer component en attributie montages voor afmetingen en metriek. Zie hieronder voor informatie over individuele instellingen.

1. Klik **[!UICONTROL Save]** om uw gegevensmening te bewaren.


### Componentinstellingen

U kunt de naam van metrisch of afmeting in iets veranderen gebruikersvriendelijker. Merk op dat de onderliggende naam niet verandert, enkel de vertoningsnaam.

### Attributiemodel

Het model beschrijft de distributie van omzettingen in de gebeurtenissen in een groep. Bijvoorbeeld, eerste aanraking of laatste aanraking. Bepaalt hoe de Analyse van de Reis van de Klant krediet voor een succesgebeurtenis toewijst als een variabele veelvoudige waarden vóór de gebeurtenis ontvangt.

| UI-pictogram | Attributiemodel | Definitie | Wanneer te gebruiken |
| --- | --- | --- | --- |
| ![Laatste aanraking](assets/last_touch1.png) | Laatste aanraking | Verleent 100% krediet aan het aanrakingspunt dat onlangs voor omzetting voorkomt. | Het meest fundamentele en gemeenschappelijke attributiemodel. Het wordt vaak gebruikt voor omzettingen met een korte bezinningscyclus. Last Touch wordt algemeen gebruikt door teams die onderzoek marketing leiden of interne onderzoekssleutelwoorden analyseren. |
| ![Eerste aanraking](assets/first_touch.png) | Eerste aanraking | Geeft 100% krediet aan het aanrakingspunt dat eerst in het de terugkijkvenster van de attributie wordt gezien. | Een ander gemeenschappelijk toewijzingsmodel dat nuttig is voor het analyseren van marketingkanalen die bedoeld zijn om bekendheid te geven aan het merk of om klanten aan te trekken. Het wordt vaak gebruikt door vertonings of sociale marketing teams, maar is ook groot voor het beoordelen van de doeltreffendheid van de onsite productaanbeveling. |
| ![Zelfde aanraking](assets/same_touch.png) | Zelfde aanraking | Verleent 100% krediet aan de zeer treffer waar de omzetting plaatsvond. Als een aanrakingspunt niet op de zelfde klap zoals een omzetting gebeurt, wordt het geknipt onder &quot;niets&quot;. | Een nuttig model wanneer het evalueren van de inhoud of de gebruikerservaring die onmiddellijk op het tijdstip van omzetting werd voorgesteld. Product- of ontwerpteams gebruiken dit model vaak om de doeltreffendheid van een pagina te beoordelen waar conversie plaatsvindt. |
| ![Lineair](assets/linear.png) | Lineair | Geeft evenveel krediet aan elk aanraakpunt dat wordt gezien voor een conversie. | Nuttig voor omzettingen met langere bezinningscycli of gebruikerservaringen die frequentere klantenovereenkomst vereisen. Het wordt vaak gebruikt door teams die mobiele app berichtdoeltreffendheid meten of met op abonnement-gebaseerde producten. |
| ![U-vormig](assets/u_shaped.png) | U-vormig | Geeft 40% krediet aan de eerste interactie, 40% krediet aan de laatste interactie, en verdeelt de resterende 20% aan om het even welke aanrakingspunten binnen tussen. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor omzettingen met twee aanraakpunten wordt aan beide een krediet van 50% toegekend. | Een goed model voor degenen die interacties waarderen die een conversie introduceerden of sloten, maar nog steeds assistentie interacties willen herkennen. U-vormige attributie wordt algemeen gebruikt door teams die een evenwichtiger benadering kiezen maar meer krediet willen geven aan kanalen die een omzetting vonden of sluiten. |
| ![J-vorm](assets/j_shaped.png) | J-vorm | Geeft 60% krediet aan de laatste interactie, 20% krediet aan de eerste interactie, en verdeelt de resterende 20% aan om het even welke aanrakingspunten binnen tussen. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor omzettingen met twee aanrakingspunten, wordt 75% krediet gegeven aan de laatste interactie, en 25% wordt krediet gegeven aan de eerste. | Dit model is groot voor degenen die aan vinders en sluiters voorrang geven, maar zich op het sluiten van interactie willen concentreren. De J-vormige attributie wordt vaak gebruikt door teams die een evenwichtiger benadering kiezen en meer krediet willen geven aan kanalen die een omzetting sluiten. |
| ![Inverse J-vorm](assets/inverse_j.png) | Invers J | Geeft 60% krediet aan het eerste aanraakpunt, 20% krediet aan het laatste aanraakpunt, en deelt de resterende 20% aan om het even welke aanrakingspunten binnen tussen. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor omzettingen met twee aanrakingspunten, wordt 75% krediet gegeven aan de eerste interactie, en 25% wordt krediet gegeven aan het laatste. | Dit model is ideaal voor degenen die aan vinders en sluiters voorrang geven, maar zich op het vinden van interactie willen concentreren. De omgekeerde eigenschap van J wordt gebruikt door teams die een evenwichtigere benadering kiezen en meer krediet aan kanalen willen geven die een omzetting in werking stelden. |
| ![Aangepast](assets/custom.png) | Aangepast | Hiermee kunt u de gewichten opgeven die u wilt geven aan de eerste aanraakpunten, de laatste aanraakpunten en alle tussenliggende aanraakpunten. De gespecificeerde waarden worden genormaliseerd aan 100% zelfs als de ingegane douanenummers niet aan 100 toevoegen. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor interactie met twee aanrakingspunten, wordt de middenparameter genegeerd. De eerste en laatste aanraakpunten worden dan genormaliseerd aan 100%, en de kredieten worden dienovereenkomstig toegewezen. | Dit model is perfect voor degenen die volledige controle willen over hun toewijzingsmodel en specifieke behoeften hebben waaraan andere toewijzingsmodellen niet voldoen. |
| ![Verval van tijd](assets/time_decay.png) | Verval | Volgt en exponentieel verval met een parameter van de douanehalfwaardetijd, waar het gebrek 7 dagen is. Het gewicht van elk kanaal hangt van de hoeveelheid tijd af die tussen de initiatie van het aanrakingspunt en de uiteindelijke omzetting overging. De formule die wordt gebruikt om krediet te bepalen is `2`<sup>`(-t/halflife)`</sup>, waar `t` is de hoeveelheid tijd tussen een aanrakingspunt en een omzetting. Alle aanraakpunten worden dan genormaliseerd tot 100%. | Ideaal voor teams die regelmatig videoreclame of markten tegen gebeurtenissen met een vooraf bepaalde datum beheren. Hoe langer een conversie plaatsvindt na een marketinggebeurtenis, hoe minder krediet wordt gegeven. |
| ![Deelname](assets/participation.png) | Deelname | Geeft 100% krediet aan alle unieke aanraakpunten. Het totale aantal omzettingen wordt opgepompt in vergelijking met andere toewijzingsmodellen. De participatie dedupliceert kanalen die veelvoudige tijden worden gezien. | Uitstekend om te begrijpen wie klanten vaak aan een bepaalde interactie worden blootgesteld. De organisaties van media gebruiken vaak dit model om inhoudssnelheid te berekenen. De detailhandelorganisaties gebruiken vaak dit model om te begrijpen welke delen van hun plaats aan omzetting kritiek zijn. |

### Verlopen

Specificeert een tijdspanne, of een gebeurtenis, waarna verloopt de afmetingswaarde (ontvangt niet meer krediet voor succesgebeurtenissen). U kunt de attributieafloop op de zitting, de persoon, of het douaneniveau plaatsen.

| Instellen | Definitie |
|---|---|
| Sessie | Vroeger bekend als het &#39;Bezoek&#39;-niveau. De gebeurtenissen van de omzetting voorbij de paginamening of de zitting associëren niet met de afmeting of metrisch. |
| Persoon (rapportagevenster) | Vroeger bekend als het &quot;Bezoekerniveau&quot;. De gebeurtenissen van de omzetting niet verbonden aan deze persoon associëren niet met de afmeting of metrisch. |
| Aangepaste tijd | Geef de aangepaste minuten, uren, dagen, maanden of kwartalen op. De gebeurtenissen van de omzetting voorbij de gespecificeerde tijdspanne associëren niet met de afmeting of metrisch. |

Voor meer informatie, zie IQ van de [Attributie doc](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/attribution/attribution.html).

### Referentievenster

Een raadplegingsvenster is de hoeveelheid tijd een omzetting zou moeten terugkijken om aanrakingspunten te omvatten. De modellen van de attributen die meer krediet aan eerste interactie geven zien grotere verschillen wanneer het bekijken van verschillende raadplegingsvensters.

* **Sessie:** Kijkt terug naar het begin van een sessie waar een conversie plaatsvond. De raadplegingsvensters van het bezoek zijn smal, aangezien zij niet voorbij de zitting kijken. De de raadplegingsvensters van de zitting respecteren de gewijzigde bezoekdefinitie in gegevensmeningen.
* **Persoon (rapportagevenster):** Bekijk alle zittingen file tot de 1ste van de maand van de huidige datumwaaier. De de raadplegingsvensters van de persoon zijn breed, aangezien zij vele zittingen kunnen overspannen. Bijvoorbeeld, als de waaier van de rapportdatum 15 september - september 30 is, omvat de waaier van de persoonraadpleging datumwaaier 1 - september 30.
