---
title: Veelgestelde vragen over attributie
description: Antwoorden op veelgestelde vragen over attributie.
translation-type: tm+mt
source-git-commit: 05bc0b378c962f4513ab292d518e32f5f70f7dfd
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 2%

---


# Veelgestelde vragen over attributie

>[!NOTE] U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

**Wat is het regelitem &quot;Geen&quot; wanneer u een kenmerk gebruikt?**

Het regelitem Geen is een catch-all-item dat alle conversies vertegenwoordigt die zonder aanraakpunten in het terugzoekvenster zijn uitgevoerd. Probeer een langer tijdbereik op te nemen in het rapportvenster.

**Waarom zie ik soms data buiten mijn rapporteringsvenster wanneer het gebruiken van attributiemodellen?**

Deze extra datums zijn het gevolg van het terugzoekvenster van de bezoeker. Zie [Gegevens buiten rapportagevenster](https://helpx.adobe.com/analytics/kb/data-appearing-outside-reporting-window.html) in Analytics KB voor meer informatie. Adobe is van plan deze extra rijen in een volgende release uit te filteren.

**Wanneer moet ik een terugzoekopdracht voor bezoekerskenmerk gebruiken?**

De keuze van de terugzoekfunctie voor attributie hangt af van het gebruikte geval. Als conversies doorgaans langer duren dan één bezoek, wordt het aangeraden een bezoeker terug te zoeken. Het maken van een virtuele rapportsuite met een definitie voor een langer bezoek is ook een potentiële oplossing.

**Hoe vergelijken props en eVars wanneer het gebruiken van attributie?**

Attribution wordt opnieuw berekend tijdens de uitvoering van het rapport, zodat er geen verschil is tussen een prop of eVar (of een andere dimensie) voor het maken van attributiemodellen. Props kunnen blijven bestaan met een terugzoekvenster of toewijzingsmodel en instellingen voor eVar-toewijzing/vervaldatum worden genegeerd.

**Zijn toewijzingsmodellen alleen beschikbaar als ik een virtuele rapportsuite gebruik waarvoor verwerking van rapporttijd is ingeschakeld?**

Attributiemodellen zijn beschikbaar buiten virtuele rapportsuites. Terwijl zij de verwerking van de rapporttijd op de achtergrond gebruiken, zijn de attributiemodellen beschikbaar aan zowel standaardrapportreeksen als virtuele rapportreeksen.

**Welke afmetingen en metriek worden niet gesteund?**

Het deelvenster Kenmerken ondersteunt alle afmetingen. Niet-ondersteunde meetgegevens zijn:

* Unieke bezoekers
* Bezoeken
* Voorvallen
* Paginaweergaven
* A4T-meetwaarden
* Metrische tijdwaarden
* Bounces
* Stuitpercentage
* Geopend
* Gesloten
* Pagina&#39;s niet gevonden
* Zoekopdrachten
* Bezoeken van één pagina
* Eenmalige toegang

**Werkt de toewijzing met classificaties?**

Ja, classificaties worden volledig ondersteund.

**Werkt de toewijzing met gegevensbronnen?**

Ja, de meeste gegevensbronnen worden ondersteund. Kenmerken is niet mogelijk bij gegevensbronnen op overzichtsniveau omdat deze niet aan een Analytics-bezoeker-id zijn gekoppeld. De gegevensbronnen van identiteitskaart van de transactie worden ook gesteund, tenzij zij in een virtuele rapportreeks met toegelaten verwerking van de rapporttijd worden gebruikt.

**Werkt attributie met de integratie van Advertising Analytics?**

Metagegevensafmetingen, zoals type en trefwoord, werken met kenmerk. Metrische gegevens (zoals afbeeldingen, kosten, klikken, gemiddelde positie en gemiddelde kwaliteitsscore) gebruiken echter gegevensbronnen op overzichtsniveau en zijn daarom niet compatibel.

**Hoe werkt attributie met marketingkanalen?**

Toen de marketingkanalen voor het eerst werden geïntroduceerd, hadden ze alleen de eerste en laatste aanraakafmetingen. Expliciete eerste/laatste aanraakafmetingen zijn niet meer nodig met de huidige versie van de toewijzing. Adobe biedt algemene afmetingen voor Marketingkanaal en Marketingkanaaldetails, zodat u deze kunt gebruiken met het gewenste attributiemodel. Deze generieke afmetingen gedragen zich hetzelfde als de laatste aanraakkanaalafmetingen, maar worden anders geëtiketteerd om verwarring te voorkomen bij het gebruik van marketingkanalen met een ander toewijzingsmodel.

Aangezien de afmetingen van de marketingkanalen afhankelijk zijn van een traditionele &quot;visit&quot;-definitie (zoals gedefinieerd door hun verwerkingsregels), kan de definitie van hun &quot;visit&quot; niet worden gewijzigd met behulp van virtuele-rapportsuites.

**Hoe werkt attributie met variabelen met meerdere waarden, zoals list vars?**

Sommige afmetingen in Analytics kunnen meerdere waarden bevatten bij één druk. Veelvoorkomende voorbeelden zijn list vars en de productvariabele.

Wanneer de attributie wordt toegepast op multi-value klappen, krijgen alle waarden in de zelfde klappers de zelfde creditering. Aangezien vele waarden dit krediet kunnen ontvangen, kan het rapporttotaal verschillend zijn dan als u elk individueel lijnpunt samenstelde. Het rapporttotaal wordt gededupliceerd, terwijl elke afzonderlijke waarde van de dimensie juiste kredieten krijgt.

**Hoe werkt attributie met segmentatie?**

Attributie wordt altijd uitgevoerd vóór segmentatie en segmentatie wordt uitgevoerd voordat rapportfilters worden toegepast. Dit concept is ook op virtuele rapportsuites van toepassing gebruikend segmenten.

Als u bijvoorbeeld een VRS maakt met een toegepast segment &quot;Weergaveits&quot;, kunt u andere kanalen in een tabel zien met behulp van bepaalde attributiemodellen.

![Virtuele rapportsuite met alleen weergave](assets/vrs-aiq-example.png)

>[!NOTE] Als een segment klappen onderdrukt die uw metrisch bevatten, zullen die metrische instanties niet aan om het even welke afmeting worden toegeschreven. Nochtans, zal een gelijkaardig rapportfilter eenvoudig sommige afmetingswaarden verbergen, zonder enige invloed op metriek die per het attributiemodel wordt verwerkt. Hierdoor kan een segment lagere waarden retourneren dan een filter met een vergelijkbare definitie.
