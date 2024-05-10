---
title: Gebruiksscenario's voor gegevensinvoer
description: Verschillende gevallen van gegevensexport voor Customer Journey Analytics begrijpen
solution: Customer Journey Analytics
feature: Use Cases
role: Admin
source-git-commit: 19018e31bb2a46e88a27643fe10c388b40de243e
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---


# Gebruiksscenario&#39;s bij exporteren van gegevens

Deze sectie bevat gebruiksgevallen voor gegevensexport. Elk geval van gebruik wordt beschreven in zijn eigen artikel. Voor sommige van de gebruiksgevallen wordt meer dan één oplossing geleverd.

## Inleiding

Een van de unieke verschillen tussen Adobe Analytics en Customer Journey Analytics houdt verband met de verwerking van gegevens voor attributie en sessionisatie. Zie [Gegevensverwerking in Adobe Analytics en Customer Journey Analytics vergelijken](/help/getting-started/aa-vs-cja/data-processing-comparisons.md) voor meer informatie .

### Adobe Analytics: toewijzing en sessionisatie van de verzameltijd.

In Adobe Analytics worden alle gebeurtenissen live en op volgorde verwerkt met apparaat-id, zodat Adobe klikstroomgegevens kan genereren, opslaan en exporteren met blijvend of toegeschreven waarden op het moment van verzameling, zoals:

* persistentie van het Dimension (bijvoorbeeld gedragscodes die na 90 dagen verlopen).
* Bezoek het nummer en de sessionisatie.
* Dimension waarden, berekend door verwerking en VISTA regels.

Dit is van invloed op de uitvoer van gegevens uit Adobe Analytics:

* Gegevensverwerking is statisch na eerste verzameling.
* Gegevensfeeds omvatten &quot;postkolommen&quot;, die de verwerking van de verzameltijd weerspiegelen.


### Customer Journey Analytics: toewijzing en sessionisatie tijdens de query

In Customer Journey Analytics, worden de gebeurtenissen niet verzameld in orde en een persoon identiteitskaart wordt gebruikt in plaats van een apparatenidentiteitskaart, toestaand Customer Journey Analytics om attributie en zittingsonisatie bij rapporttijd bij te werken. Dit type gegevensverzameling introduceert flexibiliteit, zoals:

* Stitching kan _replay_ gegevens dagelijks of wekelijks, associërend anonieme gebeurtenissen met bekende gebeurtenissen. Zie [Stiksel](../../stitching/overview.md) voor meer informatie .
* Sessionisatie en aanhoudend waarden veranderen telkens als
   * nieuwe gegevens worden verzameld of
   * stitching voegt gebeurtenissen toe aan de geschiedenis van een persoon .

De verwerking tijdens de verslagperiode heeft gevolgen voor de uitvoer van gegevens uit Customer Journey Analytics. Exporteren die persistente waarden bevatten, komen niet overeen met rapporten van Customers Journey Analytics en waarden verdwijnen over een bepaalde tijd.

Voor metrische consistentie, is het gebruik van de nieuwe eigenschappen in Customer Journey Analytics aangewezen. In het algemeen is de exportfunctionaliteit van Experience Platform- en Customer Journey Analytics-gegevens hoger dan de functionaliteit voor gegevensinvoer van Adobe Analytics. Experience Platform en Customer Journey Analytics bieden:

* nieuwe gegevensbronnen en verwerking die onderworpen zijn aan gegevensexport

   * niet-digitale gegevensbronnen op te nemen;
   * aangepaste toeschrijving en sessionisatie toepassen op basis van bedrijfsregels, en
   * de reis van de klant up-to-date houden met stitching.

* de verwezenlijking van op maat gesneden gevallen van gegevensexport

   * gegevens naar waar u ze nodig hebt exporteren, waaronder Business Intelligence (BI)-gereedschappen en cloudinstellingen,
   * gegevens gesynchroniseerd houden met Analysis Workspace via de integratie van BI-gereedschappen,
   * het is niet nodig om verwerkingslogica in uw eigen systemen te herhalen,
   * nieuwe steun voor berekende metriek, afgeleide gebieden en segmentatie, en

* overweging van veiligheid en gegevensbeheer door ontwerp

   * alle gegevens controleren die door gebruiker en bestemming worden uitgevoerd;
   * limieten vaststellen voor de gegevens die beschikbaar zijn voor uitvoer, en
   * waarschuwingsberichten instellen voor leveringsproblemen en limieten voor geplande leveringstermijnen.


## Gebruik hoofdletters en oplossingen

Over het algemeen worden bij het exporteren van gegevens een aantal gebruiksgevallen ondersteund. Elk geval van gebruik is verschillend in termen van de gegevens die worden vereist en hoe te om tot die gegevens toegang te hebben en uit te voeren. Experience Platform en Customer Journey Analytics bieden een aantal functies die onafhankelijk of gecombineerd de verschillende gebruiksgevallen kunnen oplossen. De onderstaande tabel geeft een overzicht van geïdentificeerde gevallen waarin gegevens worden geëxporteerd en de functies voor Experience Platform en Customer Journey Analytics om deze gebruiksgevallen te implementeren.

| Gebruiksscenario&#39;s bij exporteren van gegevens | Functies voor Experience Platform en Customer Journey Analytics |
|---|---|
| **Gegevensback-up**<br/> Bewaar een volledige kopie van uw digitale gegevens voor compatibiliteits- of regelgevingsdoeleinden. | **Experience Platform**: [**Gegevensbestanden exporteren**](export-datasets.md)<br/> Exporteer gegevens die in Experience Platform zijn verzameld rechtstreeks naar cloudinstellingen volgens een planning of een ad-hoc-procedure.<br/>*Momenteel beperkte release is er naar verwachting in juni 2024 een volledige release voor klanten van Customers Journey Analytics.* |
| **Gegevensvalidatie**<br/> Evalueer klikstroomgegevens voor de nauwkeurigheid van de gegevensinzameling. | **Experience Platform**: [**Query-service (Data Distiller) en exportgegevenssets**](queryservice-export-datasets.md)<br/> Interactieve PostSQL-interface om ad-hoc SQL-query&#39;s uit te voeren met uw favoriete SQL-gereedschap om de gegevens in uw datasets te valideren.<br/><br/>**Customer Journey Analytics**: [**Volledige tabel exporteren**](export-full-table.md)<br/> Valideer verwerkte gegevens van CJA met toegepaste attributie en sessionisatie. |
| **Data Lake-, Data Warehouse- of BI-gereedschappen**<br/> Breng digitale gegevens in uw eigen hulpmiddelen BI of het Meer van Gegevens voor gebruik met extra datasets. | **Customer Journey Analytics**: [**BI Extension**](bi-extension.md)<br/> Voeg Customer Journey Analytics verwerkte metriek aan de hulpmiddelen van de gegevensvisualisatie zoals Power BI toe en combineer met extra gegevens voor douanerapporten <br/><br/>**Experience Platform**: [**Query-service (Data Distiller) en exportgegevenssets**](queryservice-export-datasets.md)<br> Genereer aangepaste klikstreamgegevens met behulp van SQL die naar wolkendoelen moeten worden geleverd. |
| **Gereedheid voor AI/ML**<br/> Verbeter de modellen en taken voor kunstmatige intelligentie/machinaal leren met gegevens over Customers Journey Analytics. | **Customer Journey Analytics**: [**Volledige tabel exporteren**](export-full-table.md)<br/> De verwerkte afmetingen en metriek van de Customer Journey Analytics van de uitvoer naar wolkenbestemmingen eenmalig of terugkerend, met inbegrip van berekende metriek en segmentatie.<br/><br/>**Experience Platform**: [**Query-service (Data Distiller) en exportgegevenssets**](queryservice-export-datasets.md)<br/> Genereer aangepaste klikstreamgegevens met behulp van SQL om AI / ML-modellen te verrijken. |

