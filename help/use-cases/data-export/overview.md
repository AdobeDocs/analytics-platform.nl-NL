---
title: Gebruiksscenario's bij exporteren van gegevens
description: Werken met verschillende gevallen waarin gegevens worden geëxporteerd voor Customer Journey Analytics
solution: Customer Journey Analytics
feature: Use Cases
role: Admin
exl-id: 8b9c164e-01da-4b43-8e2c-99904223cae5
source-git-commit: efb961c571ddcde1017e6bf2080fc2a97c28bb13
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---

# Gebruiksscenario&#39;s bij exporteren van gegevens {#data-export-use-cases}

<!-- This contextual help is for the upgrade checklist -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-data-feeds-step"
>title="Exportfuncties gebruiken die vergelijkbaar zijn met Gegevensfeeds"
>abstract="Een exacte vervanging voor gegevensfeeds is nog niet beschikbaar in Customer Journey Analytics. Echter, gelijkaardige functionaliteit kan met mogelijkheden zoals volledige lijstuitvoer, de uitvoer van de dataset van het Platform, BI hulpmiddelintegratie, en rapporteringsAPI worden bereikt."

<!-- markdownlint-enable MD034 -->

In deze sectie worden gebruiksgevallen voor gegevensuitvoer beschreven en wordt uitgelegd hoe u deze gebruiksgevallen kunt implementeren met een of meer functies van Customer Journey Analytics of Experience Platform. Elke functionaliteit wordt nader beschreven in een afzonderlijk artikel.

## Inleiding

Een van de unieke verschillen tussen Adobe Analytics en Customer Journey Analytics houdt verband met de verwerking van gegevens voor attributie en sessionisatie. Zie [ gegevensverwerking over Adobe Analytics en Customer Journey Analytics ](/help/getting-started/aa-vs-cja/data-processing-comparisons.md) voor meer informatie vergelijken.

### Adobe Analytics: toewijzing en sessionisatie van de verzameltijd.

In Adobe Analytics worden alle gebeurtenissen live en op volgorde verwerkt met apparaat-id, zodat Adobe klikstroomgegevens kan genereren, opslaan en exporteren met aanhoudend of toegewezen waarden op het moment van de verzameling, zoals:

* Dimension persistentie (bijvoorbeeld code voor het bijhouden van campagnes die na 90 dagen verlopen).
* Bezoek het nummer en de sessionisatie.
* Dimension-waarden, berekend op basis van verwerking en VISTA-regels.

Dit is van invloed op de uitvoer van gegevens uit Adobe Analytics:

* Gegevensverwerking is statisch na eerste verzameling.
* Gegevensfeeds omvatten &quot;postkolommen&quot;, die de verwerking van de verzameltijd weerspiegelen.


### Customer Journey Analytics: toewijzing en sessionisatie tijdens de query

In Customer Journey Analytics worden gebeurtenissen niet op volgorde verzameld en wordt een persoon-id gebruikt in plaats van een apparaat-id, zodat Customer Journey Analytics kenmerk en sessionisatie op het rapporttijdstip kan bijwerken. Dit type gegevensverzameling introduceert flexibiliteit, zoals:

* Stitching kan _gegevens dagelijks of wekelijks opnieuw spelen 1&rbrace;, associerend anonieme gebeurtenissen met bekende gebeurtenissen._ Zie [ het Plaatsen ](../../stitching/overview.md) voor meer informatie.
* Sessionisatie en aanhoudend waarden veranderen telkens als
   * nieuwe gegevens worden verzameld of
   * stitching voegt gebeurtenissen toe aan de geschiedenis van een persoon .

De verwerking tijdens de verslagperiode is van invloed op de uitvoer van gegevens uit Customer Journey Analytics. Exporteren die blijvende waarden bevatten, komen niet overeen met Customer Journey Analytics-rapporten en waarden verdwijnen over een bepaalde tijd.

Voor metrische consistentie, is het gebruik van de nieuwe eigenschappen in Customer Journey Analytics aangewezen. Over het algemeen overschrijdt de Experience Platform- en Customer Journey Analytics-functie voor gegevensexport de functionaliteit voor gegevensinvoer van Adobe Analytics. Experience Platform en Customer Journey Analytics bieden:

* nieuwe gegevensbronnen en verwerking die onderworpen zijn aan gegevensexport

   * niet-digitale gegevensbronnen op te nemen;
   * aangepaste toeschrijving en sessionisatie toepassen op basis van bedrijfsregels, en
   * de reis van de klant up-to-date houden met stitching.

* de verwezenlijking van op maat gesneden gevallen van gegevensexport

   * gegevens exporteren naar waar u ze nodig hebt, waaronder Business Intelligence (BI)-gereedschappen en cloudinstellingen,
   * gegevens gesynchroniseerd houden met Analysis Workspace via de integratie van BI-gereedschappen,
   * het is niet nodig om verwerkingslogica in uw eigen systemen te herhalen,
   * nieuwe steun voor berekende metriek, afgeleide gebieden en segmentatie, en

* overweging van veiligheid en gegevensbeheer door ontwerp

   * alle gegevens controleren die door gebruiker en bestemming worden uitgevoerd;
   * limieten vaststellen voor de gegevens die beschikbaar zijn voor uitvoer, en
   * waarschuwingsberichten instellen voor leveringsproblemen en limieten voor geplande leveringstermijnen.


## Gebruik gevallen en functies

Over het algemeen worden bij het exporteren van gegevens een aantal gebruiksgevallen ondersteund. Elk geval van gebruik is verschillend in termen van de gegevens die worden vereist en hoe te om tot die gegevens toegang te hebben en uit te voeren. Experience Platform en Customer Journey Analytics bieden een aantal functies die onafhankelijk of gecombineerd de verschillende gebruiksgevallen kunnen oplossen. De onderstaande tabel geeft een overzicht van geïdentificeerde gevallen waarin gegevens worden geëxporteerd en de functies van Experience Platform en Customer Journey Analytics om deze gebruiksgevallen te implementeren.

| Gebruiksscenario&#39;s bij exporteren van gegevens | Experience Platform- en Customer Journey Analytics-functionaliteit |
|---|---|
| **Steun van Gegevens**<br/> behoudt een volledig exemplaar van uw digitale gegevens voor naleving of regelgevende doeleinden. | **Experience Platform**: [**de datasets van de Uitvoer**](export-datasets.md)<br/> gegevens van de Uitvoer die in Experience Platform direct aan wolkenbestemmingen op een programma of ad hoc worden verzameld. |
| **Bevestiging van Gegevens**<br/> evalueert klikstroomgegevens voor de nauwkeurigheid van de gegevensinzameling. | **Experience Platform**: [**de Dienst van de Vraag (Gegevens Distiller) &amp; de datasets van de Uitvoer**](queryservice-export-datasets.md)<br/> Interactieve interface PostgreSQL om ad-hoc SQL vragen uit te voeren gebruikend uw favoriete SQL hulpmiddel om de gegevens in uw datasets te bevestigen.<br/><br/>**Customer Journey Analytics**: [**Uitvoer volledige lijst**](export-full-table.md)<br/> bevestigt verwerkte gegevens van CJA met toegepaste attributie en zitting. |
| **het Meer van Gegevens, Data Warehouse of BI hulpmiddelen**<br/> brengen digitale gegevens in uw eigen hulpmiddelen van BI of het Meer van Gegevens voor gebruik met extra datasets. | **Customer Journey Analytics**: [**BI de Uitbreiding**](bi-extension.md)<br/> voegt Customer Journey Analytics verwerkte metriek aan de hulpmiddelen van de gegevensvisualisatie zoals Power BI toe en combineert met extra gegevens voor douanerapporten <br/><br/>**Experience Platform**: [**Dienst van de Vraag (Gegevens Distiller) &amp; de datasets van de Uitvoer**](queryservice-export-datasets.md)<br> produceer aangepaste klikstroomgegevens gebruikend SQL om aan wolkenbestemmingen te worden geleverd. |
| **Readiness voor AI / ML**<br/> verbeter Kunstmatige Intelligentie/het Leren van de Machine modellen en taken met de gegevens van Customer Journey Analytics. | **Customer Journey Analytics**: [**de Uitvoer volledige lijst**](export-full-table.md)<br/> verwerkte afmetingen en metriek van de Uitvoer Customer Journey Analytics aan wolkenbestemmingen één keer of terugkerend, met inbegrip van berekende metriek en segmentatie.<br/><br/>**Experience Platform**: [**de Dienst van de Vraag (Gegevens Distiller) &amp; de datasets van de Uitvoer**](queryservice-export-datasets.md)<br/> produceer aangepaste klikstroomgegevens gebruikend SQL om modellen te verrijken AI/ML. |
