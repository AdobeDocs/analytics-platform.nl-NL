---
title: Marketingkanaalafmetingen gebruiken in Adobe Experience Platform
description: Gebruik de Analytics Source Connector om de verwerkingsregels van het Kanaal van de Marketing in Adobe Experience Platform te brengen.
exl-id: d1739b7d-3410-4c61-bb08-03dd4161c529
solution: Customer Journey Analytics
feature: Use Cases
source-git-commit: af9113f3afced902b385747bceaa9e51b72d83e6
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 0%

---

# Marketingkanaalafmetingen gebruiken in Adobe Experience Platform

Als uw organisatie de [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html) om de gegevens van de rapportreeks in CJA te brengen, kunt u een verbinding in CJA vormen om over de afmetingen van het Kanaal van de Marketing te rapporteren.

## Vereisten

* Gegevens uit een rapportsuite moeten al in Adobe Experience Platform worden geïmporteerd met de opdracht [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html). Andere gegevensbronnen worden niet ondersteund, omdat marketingkanalen vertrouwen op verwerkingsregels in een Analytics-rapportsuite.
* De verwerkingsregels voor marketingkanalen moeten al zijn ingesteld. Zie [Verwerkingsregels voor distributiekanalen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/marketing-channels/c-rules.html?lang=en) in de traditionele handleiding Analytics Components (Analytische onderdelen).

## Schema-elementen marketingkanaal

Zodra u de Verbinding van de Bron van Analytics op een gewenste rapportreeks vestigt, wordt een schema XDM gecreeerd voor u. Dit schema bevat alle analytische afmetingen en metriek als onbewerkte gegevens. Deze onbewerkte gegevens bevatten geen kenmerk of persistentie. In plaats daarvan, loopt elke gebeurtenis door de verwerkingsregels van het marketing kanaal en registreert de eerste regel het aanpast. U geeft kenmerk en persistentie op wanneer u een gegevensweergave maakt in CJA.

1. [Verbinding maken](/help/connections/create-connection.md) die een dataset omvat die op de Bronschakelaar van de Analytics wordt gebaseerd.
2. [Een gegevensweergave maken](/help/data-views/create-dataview.md) die de volgende afmetingen bevat:
   * **`channel.typeAtSource`**: Equivalent met de [Marketingkanaal](https://experienceleague.adobe.com/docs/analytics/components/dimensions/marketing-channel.html) dimensie.
   * **`channel._id`**: Equivalent met de [Detailgegevens marketingkanaal](https://experienceleague.adobe.com/docs/analytics/components/dimensions/marketing-detail.html)
3. Geef elke dimensie het gewenste attributiemodel en de persistentie. Als u zowel eerste als laatste aanraakafmetingen wilt, sleept u elke dimensie van het marketingkanaal meerdere keren naar het gebied met componenten. Geef elke dimensie het gewenste attributiemodel en de persistentie. Adobe raadt ook aan om elke dimensie een weergavenaam te geven om het gebruik in Workspace te vereenvoudigen.
4. Maak de gegevensweergave.

De afmetingen van uw marketingkanaal zijn nu beschikbaar voor gebruik in Analysis Workspace.

>[!NOTE]
>
> De verbinding van de Bron van de Analyse vereist dat allebei `channel.typeAtSource` (Marketingkanaal) en `channel._id` (Marketing Channel Detail) moet worden gevuld, anders wordt geen van beide naar de XDM ExperienceEvent overgedragen. Als het Detail van het Kanaal van de Marketing in de bronrapportreeks leeg is, resulteert dit in een leeg `channel._id` en de Analytics Source Connector wordt leeg gemaakt `channel.typeAtSource` ook. Dit kan resulteren in verschillen tussen Adobe Analytics en Customer Journey Analytics.

## Verschillen in verwerking en architectuur

>[!IMPORTANT]
>
>Er zijn verscheidene fundamentele gegevensverschillen tussen de gegevens van de rapportreeks en Platform. Adobe raadt u ten zeerste aan om de verwerkingsregels van uw rapportsuite aan te passen om een correcte gegevensverzameling in Platform te vergemakkelijken.

>[!NOTE]
>
>Om de doeltreffendheid van de Marketing Kanalen voor Attribution IQ en Customer Journey Analytics te maximaliseren, hebben wij sommige gepubliceerd [herziene beste praktijken](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/mchannel-best-practices.html).

De montages van het de verkoopkanaal werken verschillend tussen de gegevens van het Platform en rapportsuite gegevens. Houd rekening met de volgende verschillen bij het instellen van marketingkanalen voor CJA:

* **Is de eerste bezoekpagina**: Deze regelcriteria gelden voor verschillende standaarddefinities van marketingkanalen. Een verwerkingsregel die deze criteria bevat, wordt in het Platform genegeerd (andere criteria in dezelfde regel blijven van toepassing). De zittingen worden bepaald bij de tijd van de gegevensvraag in plaats van op het tijdstip van gegevensinzameling, verhinderend Platform deze specifieke regelcriteria te gebruiken. Adobe beveelt aan om alle regels voor de verwerking van marketingkanalen die de criteria &#39;Is First Page of Visit&#39; bevatten, opnieuw te evalueren en te kiezen voor alternatieve benaderingen waarmee uw doelstellingen worden bereikt.

   ![Eerste pagina van het bezoek](../assets/first-page-of-visit.png)

* **Laatste aanraakkanaal overschrijven**: Deze instelling in de Marketing Channel Manager voorkomt normaal gesproken dat bepaalde kanalen het laatste aanraakkanaalkrediet krijgen. Platform negeert deze instelling, waardoor brede kanalen zoals Direct of Intern op mogelijk ongewenste manieren naar metriek kunnen worden gekarakteriseerd. Adobe raadt aan kanalen te verwijderen waarvoor Laatste aanraakkanaal overschrijven is uitgeschakeld.
   * U kunt het marketingkanaal &#39;Direct&#39; verwijderen in de Marketing Channel Manager en vervolgens vertrouwen op het &#39;Geen waarde&#39;-dimensie-item van CJA voor dat kanaal. U kunt dit afmetingspunt aan &quot;Direct&quot;ook anders noemen of het afmetingspunt volledig uitsluiten wanneer het vormen van een gegevensmening.
   * U kunt ook een classificatie voor marketingkanalen maken, waarbij elke waarde naar zichzelf wordt geclassificeerd, behalve voor kanalen die u in CJA wilt uitsluiten. U kunt deze classificatiedimensie dan gebruiken wanneer het creëren van een gegevensmening in plaats van `channel.typeAtSource`.

   ![Laatste aanraakkanaal overschrijven](../assets/override-last-touch-channel.png)

* **Vervaldatum marketingkanaal**: Deze instelling voor de serviceperiode bepaalt de periode van inactiviteit voordat een bezoeker een nieuw eerste aanraakkanaal in de rapportsuite-gegevens kan verkrijgen. Platform gebruikt eigen attributie-instellingen, zodat deze instelling volledig wordt genegeerd in CJA.

   ![Vervaldatum marketingkanaal](../assets/marketing-channel-expiration.png)

## Gegevens tussen CJA en traditionele Analytics vergelijken

Omdat de architectuur van Adobe Experience Platform anders is dan een traditionele Analytics-rapportensuite, zijn de resultaten niet gegarandeerd gelijk aan elkaar. U kunt echter de volgende tips gebruiken om deze vergelijking eenvoudiger te maken:

* Controleer of de architecturale verschillen die hierboven zijn vermeld, geen invloed hebben op uw vergelijking. Dit omvat het verwijderen van kanalen die het laatste aanraakkanaal niet overschrijven, en het verwijderen van regelcriteria die het eerste aanraakpunt van een bezoek (sessie) zijn.
* Controleer tweemaal of uw verbinding de zelfde rapportreeks zoals traditionele Analytics gebruikt. Als uw verbinding CJA veelvoudige rapportreeksen met hun eigen de verwerkingsregels van het Kanaal van de Marketing bevat, is er geen gemakkelijke manier om het met traditionele Analytics te vergelijken. U zou een afzonderlijke verbinding voor elke rapportreeks willen tot stand brengen om gegevens te vergelijken.
* Zorg ervoor dat u de zelfde datumwaaiers vergelijkt, en dat de tijdzone die in uw gegevensmening plaatst het zelfde als de tijdzone van de rapportreeks is.
* Gebruik een model van de douaneattributie wanneer het bekijken van de gegevens van de rapportreeks. Gebruik bijvoorbeeld de [Marketingkanaal](https://experienceleague.adobe.com/docs/analytics/components/dimensions/marketing-channel.html) dimensie met metriek die een niet-standaard attributiemodel gebruiken. Adobe raadt u aan de standaardafmetingen niet te vergelijken [Eerste aanraakkanaal](https://experienceleague.adobe.com/docs/analytics/components/dimensions/first-touch-channel.html) of [Laatste aanraakkanaal](https://experienceleague.adobe.com/docs/analytics/components/dimensions/last-touch-channel.html), omdat ze afhankelijk zijn van toeschrijvingen die in de rapportsuite worden verzameld. CJA vertrouwt niet op de toewijzingsgegevens van een rapportsuite; in plaats daarvan, wordt het berekend wanneer een CJA- rapport in werking wordt gesteld.
* Sommige metriek hebben geen redelijke vergelijking wegens architecturale verschillen tussen de gegevens van de rapportreeks en Platform gegevens. Voorbeelden zijn bezoeken/sessies, bezoekers/personen en voorvallen/gebeurtenissen.
