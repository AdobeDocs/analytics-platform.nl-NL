---
title: Instellingen van component Attributie
description: Hiermee kunt u de standaardattributie voor een metrische waarde instellen.
exl-id: bc7ae6e3-7c9b-4994-97ce-690f3bdcbee5
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: 05cc65f3a463bc71db85d85292a172784c3d7c75
workflow-type: tm+mt
source-wordcount: '1933'
ht-degree: 0%

---

# Instellingen van component Attributie

De attributie geeft u de capaciteit om aan te passen hoe de afmetingspunten krediet voor succesgebeurtenissen krijgen.

![](../assets/attribution-settings.png)

Bijvoorbeeld:

1. Een persoon op uw site klikt op een koppeling naar een betaalde zoekopdracht naar een van uw productpagina&#39;s. Ze voegen het product aan hun winkelwagentje toe, maar kopen het niet.
2. De volgende dag zien ze een bericht in de sociale media van een van hun vrienden. Ze klikken op de koppeling en voltooien de aankoop.

In sommige rapporten wilt u mogelijk de volgorde toewijzen aan Geavanceerd zoeken. In andere rapporten, zou u de orde aan Sociaal kunnen willen worden toegeschreven. Met kenmerk kunt u dit aspect van rapportage beheren.

## Standaardtoewijzingsmodel van een component instellen

U kunt een standaardattributiemodel voor bepaalde metrisch plaatsen door metrisch het plaatsen in de gegevensmening bij te werken. Als u dit doet, overschrijft u het attributiemodel van de maateenheid op elk moment dat het in Analysis Workspace wordt gebruikt.

>[!NOTE]
>
>Houd rekening met het volgende wanneer u attributie op een metrische waarde inschakelt:
>
>* **Wanneer het gebruiken van de component in een rapport met *één dimensie*:** De toewijzing van de component negeert het toewijzingsmodel wanneer een niet-standaard toewijzingsmodel wordt gebruikt.
>
>* **Wanneer het gebruiken van de component in een rapport met *meerdere dimensies*:** De toewijzing van de component behoudt het toewijzingsmodel wanneer een niet-standaard toewijzingsmodel wordt gebruikt.
>
>   Meerdere afmetingen zijn alleen beschikbaar als [gegevens exporteren naar de cloud](/help/analysis-workspace/export/export-cloud.md).
>
> Zie voor meer informatie over toewijzing [Instellingen voor persistentiecomponenten](/help/data-views/component-settings/persistence.md).

Het standaardtoewijzingsmodel van een component bijwerken:

1. Ga naar de gegevensmening die de component bevat waarvan standaardattributiemodel u wilt bijwerken.

1. Selecteer de component en vouw vervolgens de sectie Kenmerk aan de rechterkant van het scherm uit.

   ![](../assets/attribution-settings.png)

1. Selecteren [!UICONTROL **Kenmerk instellen**] selecteert u vervolgens het toewijzingsmodel in het dialoogvenster [!UICONTROL **Attributiemodel**] vervolgkeuzelijst.

   Zie [Attributiemodellen](#attribution-models) voor meer informatie over elk toewijzingsmodel.

1. Selecteren [!UICONTROL **Opslaan en doorgaan**].

>[!TIP]
>
>Als uw organisatie vereist dat metrisch veelvoudige attributie montages heeft, kunt u één van het volgende doen:
>
> * Kopieer de metrische waarde in de gegevensweergave met elke gewenste attributie-instelling. U kunt dezelfde metrische waarde meerdere keren opnemen in een gegevensweergave, zodat elke meting een andere instelling heeft. Zorg ervoor dat u elke metrisch geschikt etiketteert zodat de analisten het verschil tussen deze metriek begrijpen wanneer het produceren van rapporten.
>
> * Overschrijf de metrische waarde in Analysis Workspace. In metrische [Kolominstellingen](/help/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md), selecteert u **[!UICONTROL Use non-default attribution model]** om het de attributiemodel van metrisch en raadplegingsvenster voor dat specifiek rapport te veranderen.

## Attributiemodellen

Een attributiemodel bepaalt welke afmetingspunten krediet voor metrisch krijgen wanneer de veelvoudige waarden binnen het terugkijkvenster van metrisch worden gezien. Attributiemodellen zijn alleen van toepassing wanneer er meerdere dimensieitems zijn ingesteld in het terugzoekvenster. Als slechts één dimensie-item is ingesteld, krijgt dat dimensie-item 100% krediet, ongeacht het gebruikte attributiemodel.

| Pictogram | Attributiemodel | Definitie |
| :---: | :--- | --- |
| ![Laatste aanraking](../assets/attribution-models/last_touch1.png) | Laatste aanraking | Geeft 100% krediet aan het aanraakpunt dat het laatst voor de conversie optrad. Dit attributiemodel is doorgaans de standaardwaarde voor elke meting waarbij een attributiemodel niet op andere wijze is opgegeven. Organisaties gebruiken dit model doorgaans wanneer de conversietijd relatief kort is, zoals bij het analyseren van interne zoektrefwoorden. |
| ![Eerste aanraking](../assets/attribution-models/first_touch.png) | Eerste aanraking | Geeft 100% krediet aan het aanraakpunt dat het eerst wordt weergegeven in het terugkijkvenster van de attributie. Organisaties gebruiken dit model doorgaans om inzicht te krijgen in merkbekendheid of aanschaf door klanten. |
| ![Lineair](../assets/attribution-models/linear.png) | Lineair | Biedt hetzelfde krediet aan elk aanraakpunt dat wordt weergegeven voor een conversie. Dit is handig wanneer conversiecycli langer zijn of een frequentere betrokkenheid van klanten vereisen. Organisaties gebruiken dit toewijzingsmodel doorgaans om de doeltreffendheid van meldingen voor mobiele apps of voor producten op abonnementsbasis te meten. |
| ![Deelname](../assets/attribution-models/participation.png) | Deelname | Biedt 100% krediet aan alle unieke aanraakpunten. Aangezien elk aanraakpunt 100% krediet ontvangt, komt het metrische gegeven meestal uit op meer dan 100%. Als een dimensie-item meerdere afzonderlijke keren vóór een conversie wordt weergegeven, worden de waarden gededupliceerd naar 100%. Dit attributiemodel is ideaal in situaties waarin u wilt begrijpen welke aanraakpunten klanten het meest worden blootgesteld. Mediaorganisaties gebruiken dit model doorgaans om de snelheid van de inhoud te berekenen. De detailhandelorganisaties gebruiken typisch dit model om te begrijpen welke delen van hun plaats aan omzetting kritiek zijn. |
| ![Zelfde aanraking](../assets/attribution-models/same_touch.png) | Zelfde aanraking | Verleent 100% krediet aan de zelfde gebeurtenis waar de omzetting plaatsvond. Als er geen aanraakpunt plaatsvindt op dezelfde gebeurtenis als bij een conversie, wordt dit punt ingesloten onder &quot;Geen&quot;. Dit attributiemodel wordt soms gelijkgesteld met het hebben van helemaal geen attributiemodel. Het is waardevol in scenario&#39;s waar u geen waarden van andere gebeurtenissen wilt die beïnvloeden hoe metrisch krediet aan afmetingspunten geeft. Product- of ontwerpteams kunnen dit model gebruiken om de doeltreffendheid van een pagina te beoordelen waar conversie plaatsvindt. |
| ![U-vorm](../assets/attribution-models/u_shaped.png) | U-vorm | Biedt 40% krediet aan de eerste interactie, 40% aan de laatste interactie, en verdeelt de resterende 20% aan om het even welke aanraakpunten tussenin. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt aan beide een krediet van 50% toegekend. Dit attributiemodel wordt het best gebruikt in scenario&#39;s waar u eerste en laatste interactie het meest waart, maar wil geen extra interacties binnen volledig sluiten. |
| ![J Curve](../assets/attribution-models/j_shaped.png) | J Curve | Geeft 60% krediet aan de laatste interactie, 20% krediet aan de eerste interactie, en verdeelt de resterende 20% aan om het even welke aanraakpunten tussenin. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt 75% aan de laatste interactie besteed en wordt 25% aan de eerste. Net als bij U-Shaped, geeft dit attributiemodel de voorkeur aan de eerste en laatste interacties, maar is het zwaarder van belang voor de laatste interactie. |
| ![Omgekeerd J](../assets/attribution-models/inverse_j.png) | Omgekeerd J | Biedt 60% krediet aan het eerste aanraakpunt, 20% aan het laatste aanraakpunt en verdeelt de resterende 20% aan de tussenliggende aanraakpunten. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor conversies met twee aanraakpunten wordt 75% aan de eerste interactie toegekend en wordt 25% aan de laatste toegekend. Net als voor J-Shaped, geeft dit attributiemodel de voorkeur aan de eerste en laatste interacties, maar eerder de eerste interactie. |
| ![Tijdverlies](../assets/attribution-models/time_decay.png) | Tijdverlies | Volgt een exponentieel verval met een aangepaste parameter voor de halfwaardetijd, waarbij de standaardwaarde 7 dagen is. Het gewicht van elk kanaal is afhankelijk van de hoeveelheid tijd die is verstreken tussen het starten van het aanraakpunt en de uiteindelijke conversie. De formule die wordt gebruikt om het krediet te bepalen is `2^(-t/halflife)`, waarbij `t` is de hoeveelheid tijd tussen een aanraakpunt en een conversie. Alle aanraakpunten worden vervolgens genormaliseerd tot 100%. Ideaal voor scenario&#39;s waarin u de toewijzing wilt meten aan de hand van een specifieke en significante gebeurtenis. Hoe langer een conversie plaatsvindt na deze gebeurtenis, hoe minder krediet wordt gegeven. |
| ![Aangepast](../assets/attribution-models/custom.png) | Aangepast | Hiermee kunt u de gewichten opgeven die u wilt geven aan het eerste aanraakpunt, het laatste aanraakpunt en de tussenliggende aanraakpunten. De opgegeven waarden worden genormaliseerd naar 100%, zelfs als de ingevoerde aangepaste getallen niet bij 100 komen te liggen. Voor conversies met één aanraakpunt wordt 100% krediet gegeven. Voor interactie met twee aanraakpunten wordt de middelste parameter genegeerd. De eerste en laatste aanraakpunten worden vervolgens genormaliseerd tot 100% en de kredieten worden dienovereenkomstig toegewezen. Dit model is ideaal voor analisten die volledige controle willen hebben over hun attributiemodel en specifieke behoeften hebben waaraan andere attributiemodellen niet voldoen. |
| ![Algorithmic](../assets/attribution-models/algorithmic.png) | Algorithmic | Gebruikt statistische technieken om dynamisch de optimale allocatie van krediet voor de geselecteerde maatstaf vast te stellen. Het algoritme dat wordt gebruikt voor attributie is gebaseerd op de Harsanyi Dividend van coöperatieve speltheorie. Het dividend van Harsanyi is een generalisering van de Shapley-waardeoplossing (genoemd naar Lloyd Shapley, een Nobelprijswinnaar) voor het verdelen van krediet onder spelers in een spel met ongelijke bijdragen aan de uitkomst.<br>Op hoog niveau wordt de toewijzing berekend als een coalitie van spelers waaraan een overschot op billijke wijze moet worden verdeeld. De overtollige verdeling van elke coalitie wordt bepaald volgens het overschot dat eerder door elke subcoalitie (of eerder deelnemende dimensie-items) recursief werd gecreeerd. Raadpleeg voor meer informatie de originele documenten van John Harsanyi en Lloyd Shapley:<br>Shapley, Lloyd S. (1953). Een waarde voor spelletjes van één persoon. *Bijdragen aan de Theorie van Spelen, 2(28)*, 307-317.<br>Harsanyi, John C. (1963). Een vereenvoudigd onderhandelingsmodel voor het on-person coöperatieve spel. *Internationale economische evaluatie 4(2)*, 194-220. |

{style="table-layout:auto"}

## Venster Opzoeken

Een terugzoekvenster is de hoeveelheid tijd die een conversie moet terugkijken om aanraakpunten op te nemen. Als een dimensie-item buiten het terugzoekvenster wordt ingesteld, wordt de waarde niet opgenomen in attributieberekeningen.

* **14**: Er wordt een back-up van 14 dagen na de conversie gemaakt.
* **30**: Er wordt een back-up van maximaal 30 dagen na de conversie gemaakt.
* **60 dagen**: Er wordt een back-up van 60 dagen na de conversie gemaakt.
* **90 dagen**: Er wordt maximaal 90 dagen vanaf het moment van de conversie gezocht.
* **Sessie**: Zoekt terug naar het begin van de sessie waar een conversie heeft plaatsgevonden. De terugkijkervensters van de zitting respecteren gewijzigde [Time-out sessie](../create-dataview.md#session-settings).
* **Persoon (rapportagevenster)**: In deze modus wordt naar alle bezoeken gekeken vanaf de eerste maand van de huidige datumbereik. Als het bereik van de rapportdatum bijvoorbeeld 15 september tot en met 30 september is, omvat het bereik van de persoonlijke terugzoekdatum 1 september tot en met 30 september. Als u dit terugkijkvenster gebruikt, kunt u soms zien dat de afmetingspunten aan data buiten uw rapporterend venster worden toegeschreven.
* **Aangepaste tijd:** Hiermee kunt u een aangepast terugzoekvenster instellen vanaf het moment dat de conversie plaatsvond. U kunt het aantal minuten, uren, dagen, weken, maanden of kwartalen opgeven. Bijvoorbeeld, als een omzetting op 20 februari gebeurde, zou een terugkijkvenster van vijf dagen alle afmetingstips van 15 februari tot 20 februari in het attributiemodel evalueren.

## Voorbeeld

Bekijk het volgende voorbeeld:

1. Op 15 september arriveert een persoon via een betaalde zoekadvertentie naar uw site en verlaat hij vervolgens.
2. Op 18 september arriveert de persoon opnieuw naar uw site via een link naar sociale media die hij van een vriend heeft gekregen. Ze voegen verschillende artikelen aan hun winkelwagentje toe, maar kopen niets.
3. Op 24 september stuurt uw marketingteam hen een e-mail met een coupon voor sommige objecten in hun winkelwagentje. Ze passen de coupon toe, maar gaan naar verschillende andere sites om te zien of er andere coupons beschikbaar zijn. Ze vinden een andere advertentie via een advertentie en kopen uiteindelijk $50.

Afhankelijk van het terugkijkvenster en het attributiemodel, ontvangen de kanalen verschillende kredieten. Hieronder volgen enkele belangrijke voorbeelden:

* Gebruiken **eerste aanraking** en **terugzoekvenster sessie** De toeschrijving gaat alleen naar het derde bezoek. Tussen e-mail en display was e-mail de eerste, dus e-mail krijgt 100% krediet voor de aankoop van $50.
* Gebruiken **eerste aanraking** en **terugkijkvenster van persoon** De toeschrijving kijkt naar alle drie de bezoeken. De betaalde zoekopdracht was de eerste, dus krijgt deze 100% krediet voor de aankoop van $50.
* Gebruiken **lineair** en **terugzoekvenster sessie**, krediet wordt verdeeld tussen e-mail en weergave. Beide kanalen krijgen elk $25 krediet.
* Gebruiken **lineair** en **terugkijkvenster van persoon** De creditering wordt verdeeld tussen betaalde zoekopdrachten, sociale gegevens, e-mailgegevens en weergavegegevens. Elk kanaal krijgt $12,50 krediet voor deze aankoop.
* Gebruiken **J-vormig** en **terugkijkvenster van persoon** De creditering wordt verdeeld tussen betaalde zoekopdrachten, sociale gegevens, e-mailgegevens en weergavegegevens.
   * 60% krediet wordt gegeven aan vertoning, voor $30.
   * 20% krediet wordt gegeven voor betaalde zoekopdrachten, voor $10.
   * De resterende 20% is verdeeld tussen sociale media en e-mail, wat elk $5 geeft.
* Gebruiken **Tijdverlies** en **terugkijkvenster van persoon** De creditering wordt verdeeld tussen betaalde zoekopdrachten, sociale gegevens, e-mailgegevens en weergavegegevens. De standaardhalfwaardetijd van 7 dagen gebruiken:
   * Tussenruimte van nul dagen tussen aanraakpunt weergeven en conversie. `2^(-0/7) = 1`
   * Ruimte van nul dagen tussen aanraakpunt en conversie via e-mail. `2^(-0/7) = 1`
   * Tussenruimte van zes dagen tussen sociale aanraakpunten en conversie. `2^(-6/7) = 0.552`
   * Tussenruimte van negen dagen tussen betaald aanraakpunt en conversie. `2^(-9/7) = 0.41`
   * Het normaliseren van deze waarden resulteert in het volgende:
      * Weergave: 33,8%, krijgt $16,88
      * E-mail: 33,8% ontvangt $ 16,88
      * Sociaal: 18,6%, $ 9,32
      * Betaalde zoekopdracht: 13,8%, krijgt $6,92

Conversiegebeurtenissen die doorgaans hele getallen bevatten, worden gedeeld als het krediet tot meer dan één kanaal behoort. Als twee kanalen bijvoorbeeld een bijdrage leveren aan een bestelling met behulp van een lineair toewijzingsmodel, krijgen beide kanalen 0,5 van die volgorde. Deze gedeeltelijke metriek worden samengevat over alle mensen dan rond gemaakt aan het dichtstbijzijnde geheel voor rapportering.
