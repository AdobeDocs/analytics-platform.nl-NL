---
title: Afmetingen marketingkanaal gebruiken
description: Leer hoe te om de de bronschakelaar van de Analyse te gebruiken om de verwerkingsregels van het Kanaal van de Marketing in Adobe Experience Platform te brengen.
exl-id: d1739b7d-3410-4c61-bb08-03dd4161c529
solution: Customer Journey Analytics
feature: Use Cases
role: User
source-git-commit: 0e9dc47b80db142801a94dcbf31470d99a610949
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# Afmetingen marketingkanaal gebruiken

Als uw organisatie de [ Analytics bronschakelaar ](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/connectors/adobe-applications/analytics) gebruikt om de gegevens van de rapportreeks in Customer Journey Analytics te brengen, kunt u een verbinding in Customer Journey Analytics vormen om op de dimensies van het Kanaal van de Marketing te rapporteren.

>[!IMPORTANT]
>
>Zie [ Voortgekomen gebieden - het malplaatje van de Kanalen van de Marketing ](/help/data-views/derived-fields/derived-fields.md#marketing-channels) voor inheemse productfunctionaliteit om op de dimensies van het marketing kanaal te rapporteren.
>


## Vereisten

* De gegevens van de Reeks van het rapport moeten reeds in Adobe Experience Platform worden ingevoerd gebruikend de [ bron van Analytics schakelaar ](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/connectors/adobe-applications/analytics). Andere gegevensbronnen worden niet ondersteund, omdat marketingkanalen vertrouwen op verwerkingsregels in een Analytics-rapportsuite.
* De verwerkingsregels voor marketingkanalen moeten al zijn ingesteld. Zie [ Regels van de Verwerking voor de Kanalen van de Marketing ](https://experienceleague.adobe.com/nl/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/marketing-channels/c-rules) in de gids van de Componenten van Adobe Analytics.

## Schema-elementen marketingkanaal

Zodra u de de bronschakelaar van de Analyse op een gewenste rapportreeks vestigt, wordt een schema XDM gecreeerd voor u. Dit schema bevat alle analytische afmetingen en metriek als onbewerkte gegevens. Deze onbewerkte gegevens bevatten geen kenmerk of persistentie. In plaats daarvan, loopt elke gebeurtenis door de verwerkingsregels van het marketing kanaal en registreert de eerste regel het aanpast. U geeft de toewijzing en persistentie op wanneer u een gegevensweergave in Customer Journey Analytics maakt.

1. [ creeer een verbinding ](/help/connections/create-connection.md) die een dataset omvat die op de Analytics bronschakelaar wordt gebaseerd.
2. [ creeer een gegevensmening ](/help/data-views/create-dataview.md) die de volgende afmetingen omvat:
   * **`channel.typeAtSource`**: Equivalent aan de [ 2&rbrace; dimensie van het Kanaal van de Marketing &lbrace;.](https://experienceleague.adobe.com/nl/docs/analytics/components/dimensions/marketing-channel)
   * **`channel._id`**: Equivalent aan het [ het kanaaldetail van de Marketing ](https://experienceleague.adobe.com/nl/docs/analytics/components/dimensions/marketing-detail)
3. Geef elke dimensie het gewenste attributiemodel en de persistentie. Als u zowel eerste als laatste aanraakafmetingen wilt, sleept u elke dimensie van het marketingkanaal meerdere keren naar het gebied met componenten. Geef elke dimensie het gewenste attributiemodel en de persistentie. Adobe raadt ook aan om elke dimensie een weergavenaam te geven om het gebruik in Workspace te vergemakkelijken.
4. Maak de gegevensweergave.

De afmetingen van uw marketingkanaal zijn nu beschikbaar voor gebruik in Analysis Workspace.

>[!NOTE]
>
> De bronaansluiting voor Analytics vereist dat zowel `channel.typeAtSource` (Marketing Channel) als `channel._id` (Marketing Channel Detail) worden gevuld. Anders wordt geen van beide naar de XDM ExperienceEvent overgedragen. Een leeg Marketing Channel-detail in de bronrapportsuite resulteert in een lege `channel._id` en de bronconnector van Analytics wordt ook leeg gelaten `channel.typeAtSource` . Deze spaties kunnen resulteren in verschillen tussen Adobe Analytics en Customer Journey Analytics.

## Verschillen in verwerking en architectuur

>[!IMPORTANT]
>
>Er zijn verscheidene fundamentele gegevensverschillen tussen de gegevens van de rapportreeks en van het Platform. Adobe raadt u ten zeerste aan om de verwerkingsregels van uw rapportenpakket aan te passen om een correcte gegevensverzameling in Experience Platform te vergemakkelijken.

>[!NOTE]
>
>Om de doeltreffendheid van de Marketing Kanalen voor attributie en Customer Journey Analytics te maximaliseren, zijn sommige [ herzien beste praktijken ](https://experienceleague.adobe.com/nl/docs/analytics/components/marketing-channels/mchannel-best-practices) beschikbaar.

De montages van het Marketing kanaal werken verschillend tussen de gegevens van het Platform en rapportsuite gegevens. Houd rekening met de volgende verschillen bij het instellen van marketingkanalen voor Customer Journey Analytics:

* **is Eerste Pagina van Bezoek**: Dit regelcriterium is gemeenschappelijk in verscheidene gebrek marketing kanaaldefinities. Om het even welke verwerkingsregel die deze criteria bevat wordt genegeerd in Platform (andere criteria in de zelfde regel blijven van toepassing). De zittingen worden bepaald bij de tijd van de gegevensvraag in plaats van op het tijdstip van gegevensinzameling, verhinderend Platform deze specifieke regelcriteria te gebruiken. Adobe raadt aan om alle regels voor de verwerking van marketingkanalen die de criteria &#39;Is First Page of Visit&#39; bevatten, opnieuw te evalueren en te kiezen voor alternatieve benaderingen waarmee uw doelstellingen worden bereikt.

  ![ Eerste pagina van bezoek ](../assets/first-page-of-visit.png)

* **met voeten treedt laatste-Aanraakkanaal**: Dit het plaatsen in de Manager van het Kanaal van de Marketing verhindert normaal bepaalde kanalen om laatste aanraakkanaalkrediet te krijgen. Het platform negeert deze instelling, waardoor brede kanalen zoals Direct of Intern op potentieel ongewenste manieren naar metriek kunnen verwijzen. Adobe raadt aan kanalen te verwijderen waarvoor Laatste aanraakkanaal negeren is uitgeschakeld.
   * U kunt het marketingkanaal &#39;Direct&#39; verwijderen in Marketing Channel Manager en vervolgens voor dat kanaal vertrouwen op de dimensie-item &#39;Geen waarde&#39; van de Customer Journey Analytics. U kunt dit afmetingspunt aan &quot;Direct&quot;ook anders noemen of het afmetingspunt volledig uitsluiten wanneer het vormen van een gegevensmening.
   * U kunt ook een classificatie voor marketingkanalen maken, waarbij elke waarde afzonderlijk wordt ingedeeld, behalve voor kanalen die u in Customer Journey Analytics wilt uitsluiten. U kunt deze classificatiedimensie dan gebruiken wanneer het creëren van een gegevensmening in plaats van `channel.typeAtSource`.

  ![ Overschrijf laatste aanrakingskanaal ](../assets/override-last-touch-channel.png)

* **Vervaldatum van het Kanaal van de Marketing**: Deze betrokkenheidsperiode die bepaalt de periode van inactiviteit alvorens een persoon een nieuw eerste aanrakingskanaal in de gegevens van de rapportreeks kan verkrijgen. Het platform gebruikt zijn eigen attributie montages, zodat wordt dit het plaatsen volledig genegeerd in Customer Journey Analytics.

  ![ het kanaalvervalsing van de Marketing ](../assets/marketing-channel-expiration.png)

## Gegevens tussen Customer Journey Analytics en Adobe Analytics vergelijken

Omdat de architectuur van Adobe Experience Platform anders is dan een Adobe Analytics-rapportenpakket, zijn de resultaten niet gegarandeerd gelijk. U kunt echter de volgende tips gebruiken om deze vergelijking eenvoudiger te maken:

* Controleer of de architecturale verschillen die hierboven zijn vermeld, geen invloed hebben op uw vergelijking. Tot deze verschillen behoren het verwijderen van kanalen die het laatste aanraakkanaal niet overschrijven, en het verwijderen van regelcriteria die het eerste resultaat zijn van een bezoek (sessie).
* Controleer of uw verbinding dezelfde rapportsuite gebruikt als Adobe Analytics. Als uw Customer Journey Analytics-verbinding meerdere rapportsuites bevat met hun eigen regels voor het verwerken van marketingkanalen, is er geen eenvoudige manier om deze te vergelijken met Adobe Analytics. U zou een afzonderlijke verbinding voor elke rapportreeks willen tot stand brengen om gegevens te vergelijken.
* Zorg ervoor dat u de zelfde datumwaaiers vergelijkt, en dat de tijdzone die in uw gegevensmening plaatst het zelfde als de tijdzone van de rapportreeks is.
* Gebruik een model van de douaneattributie wanneer het bekijken van de gegevens van de rapportreeks. Bijvoorbeeld, gebruik de [ dimensie van het Kanaal van de Marketing ](https://experienceleague.adobe.com/nl/docs/analytics/components/dimensions/marketing-channel) met metriek die een niet-gebrek attributiemodel gebruiken. Adobe adviseert tegen het vergelijken van de standaardafmetingen [ Eerste aanrakingskanaal ](https://experienceleague.adobe.com/nl/docs/analytics/components/dimensions/first-touch-channel) of [ Laatste aanrakingskanaal ](https://experienceleague.adobe.com/nl/docs/analytics/components/dimensions/last-touch-channel), omdat zij op attributie baseren die in de rapportreeks wordt verzameld. Customer Journey Analytics vertrouwt niet op de toewijzingsgegevens van een rapportsuite, maar deze worden berekend wanneer een Customer Journey Analytics-rapport wordt uitgevoerd.
* Sommige metriek hebben geen redelijke vergelijking wegens architecturale verschillen tussen de gegevens van de rapportreeks en van het Platform. Voorbeelden zijn bezoeken/sessies, personen/personen en voorvallen/gebeurtenissen.
