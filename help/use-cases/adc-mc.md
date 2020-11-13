---
title: Marketingkanalen importeren in CJA met behulp van de gegevensconnector Analytics
description: Gebruik de correcte montages van de Verbinding van Gegevens van Analytics om de verwerkingsregels van het Kanaal van de Marketing in Adobe Experience Platform te brengen.
translation-type: tm+mt
source-git-commit: 26486c79f6d94db1aa795bf024f581cad74c25f6
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---


# Marketingkanalen importeren in CJA met behulp van de gegevensconnector Analytics

Als uw organisatie [Analytics Data Connector](https://docs.adobe.com/content/help/en/experience-platform/sources/connectors/adobe-applications/analytics.html) gebruikt om rapportreeksgegevens in CJA te brengen, kunt u een verbinding in CJA vormen om op de dimensies van het Kanaal van de Marketing te rapporteren.

## Vereisten

* Gegevens uit de rapportsuite moeten al in Adobe Experience Platform worden geïmporteerd met de [Gegevensconnector voor analysemogelijkheden](https://docs.adobe.com/content/help/en/experience-platform/sources/connectors/adobe-applications/analytics.html).
* De verwerkingsregels voor marketingkanalen moeten al zijn ingesteld. Zie [Verwerkingsregels voor het in de handel brengen van Kanalen](https://docs.adobe.com/content/help/en/analytics/components/marketing-channels/c-rules.html) in de traditionele gids van de Componenten van Analytics.

## Schema-elementen marketingkanaal

Zodra u de Verbinding van Gegevens van Analytics op een gewenste rapportreeks gebruikt, wordt een schema XDM gecreeerd voor u. Dit schema bevat alle analytische afmetingen en metriek als onbewerkte gegevens. Deze onbewerkte gegevens bevatten geen kenmerk of persistentie. In plaats daarvan, loopt elke klap door de verwerkingsregels van het marketing kanaal en registreert de eerste regel het aanpast. U geeft kenmerk en persistentie op wanneer u een gegevensweergave maakt in CJA.

1. [Creeer een ](/help/connections/create-connection.md) verbinding die een dataset omvat die op de Verbinding van Gegevens van de Analyse wordt gebaseerd.
2. [Maak een ](/help/data-views/create-dataview.md) gegevensweergave met de volgende afmetingen:
   * **`channel.typeAtSource`**: Equivalent met de dimensie  [Marketing ](https://docs.adobe.com/content/help/en/analytics/components/dimensions/marketing-channel.html) channelle.
   * **`channel._id`**: Gelijk aan de details van het  [marketingkanaal](https://docs.adobe.com/content/help/en/analytics/components/dimensions/marketing-detail.html)
3. Geef elke dimensie het gewenste attributiemodel en de persistentie. Als u zowel eerste als laatste aanraakafmetingen wilt, sleept u elke dimensie van het marketingkanaal meerdere keren naar het gebied met componenten. Geef elke dimensie het gewenste attributiemodel en de persistentie. Adobe raadt ook aan om elke dimensie een weergavenaam te geven om het gebruik in Workspace te vereenvoudigen.
4. Maak de gegevensweergave.

De afmetingen van uw marketingkanaal zijn nu beschikbaar voor gebruik in Analysis Workspace.

## Verschillen in verwerking en architectuur

>[!IMPORTANT]
>
>Er zijn verscheidene fundamentele gegevensverschillen tussen de gegevens van de rapportreeks en Platform. Adobe raadt u ten zeerste aan om de verwerkingsregels voor marketingkanalen van uw rapportsuite aan te passen om een correcte gegevensverzameling in Platform te vergemakkelijken.


Aangezien de afmetingen van het eerste en laatste aanraakkanaal in wezen dezelfde dimensie hebben met verschillende attributiemodellen, kunt u vergelijkbare afmetingen opnieuw maken wanneer u [een gegevensweergave maakt](/help/data-views/create-dataview.md). U kunt meerdere dimensies maken op basis van hetzelfde schema-element, zodat deze verschillende toewijzingsmodellen en persistentie hebben.

## Verschillen tussen

