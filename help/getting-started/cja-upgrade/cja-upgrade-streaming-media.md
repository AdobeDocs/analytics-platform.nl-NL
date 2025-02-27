---
title: Streaming media-verzameling instellen voor Customer Journey Analytics
description: Meer informatie over het instellen van streaming media Collection voor Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
source-git-commit: 68ce73ddf805ec377fdb2c539683507f191c9249
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Streaming media-verzameling instellen voor Customer Journey Analytics {#streaming-media-setup}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-media-edge"
>title="Media Edge instellen en implementeren"
>abstract="U kunt de Adobe Streaming Media Collection zo configureren dat Experience Platform Edge gegevens beschikbaar maakt in Customer Journey Analytics."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

De stappen voor het implementeren van de Streaming Media Collection in Customer Journey Analytics verschillen afhankelijk van uw huidige implementatie van Streaming Media Collection in Adobe Analytics.

De inzameling van de Media van het stromen kan in Adobe Analytics op één van beide volgende manieren worden uitgevoerd:

* [Edge Network-implementaties voor de streaming media Collection](#edge-network-implementations)

+++ Infografisch weergeven

  ![ het stromen Media op de implementatie van Edge ](assets/streaming-media-edge.png)

+++

* [Alleen Adobe Analytics-implementaties voor de streaming Media Collection](#adobe-analytics-only-implementations)

+++ Infografisch weergeven

  ![ Analytics-Enige implementatie ](assets/analytics-implementation.png)

+++

Voor meer informatie over de verschillen tussen deze implementatiemethodes, zie [ de Streaming Inzameling van Media ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/overview) in de Streaming Gids van de Inzameling van Media uitvoeren.

## Edge Network-implementaties voor de streaming media Collection

Als de het stromen Inzameling van Media [ wordt uitgevoerd gebruikend Edge Network in uw implementatie van Adobe Analytics ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/overview#edge-implementation-methods), betekent dit dat sommige stappen die worden vereist om de het stromen Inzameling van Media aan Customer Journey Analytics te bevorderen reeds als deel van uw implementatie van Adobe Analytics zijn voltooid. De volgende stappen zijn voltooid:

* [ Opstelling het schema in Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#set-up-the-schema-in-adobe-experience-platform)

* [ creeer een dataset in Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#create-a-dataset-in-adobe-experience-platform)

* [ vorm een gegevensstroom in Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#configure-a-datastream-in-adobe-experience-platform)

De volgende aanvullende stappen moeten worden uitgevoerd als onderdeel van de upgrade naar Customer Journey Analytics:

>[!NOTE]
>
>Wanneer u de Customer Journey Analytics-upgradesstappen uitvoert, moet u het schema, de gegevensset en de gegevensstroom uit de implementatie van de Streaming Media Collection in Adobe Analytics gebruiken.

* [Verbinding maken in Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-connection.md)

* [Een gegevensweergave maken in Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md)


## Alleen Adobe Analytics-implementaties voor de streaming Media Collection

Als de het stromen Inzameling van Media [ wordt uitgevoerd gebruikend een Adobe Analytics-Enige implementatie in uw milieu van Adobe Analytics ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/overview#adobe-analytics-only-implementation-methods), betekent dit dat het Streamen van de gegevens van Media nog niet naar Edge Network gaat.

Als u het schema, de dataset, de gegevensstroom, de verbinding, en de gegevensmening als deel van uw verbetering van Adobe Analytics aan Customer Journey Analytics creeert, maak de volgende selecties aan rekening voor het stromen gegevens van de Inzameling van Media:

* Wanneer u het schema voor Customer Journey Analytics maakt, neemt u de veldgroep `MediaAnalytics Interaction Details` op.

  Voor meer informatie over het toevoegen van deze gebiedsgroep, zie [ Opstelling het schema in Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#set-up-the-schema-in-adobe-experience-platform) in de Streaming Gids van de Inzameling van Media.

  Voor informatie over het creëren van het schema, zie [ een douaneschema tot stand brengen om met Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md) te gebruiken.

* Schakel Media Analytics in wanneer u de gegevensstroom voor Customer Journey Analytics configureert.

  Voor meer informatie over het toelaten van deze optie, zie [ een gegevensstroom in Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#configure-a-datastream-in-adobe-experience-platform) in de Streaming Gids van de Inzameling van Media vormen.

  Voor informatie over het creëren van de gegevensstroom, zie [ een gegevensstroom tot stand brengen om met Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-datastream.md) te gebruiken.

* Neem bij het maken van een gegevensweergave voor Customer Journey Analytics de vereiste schemavelden op voor de verzameling streamingmedia.

  Zorg ervoor u deze schemagebieden aan de correcte waarden in het voorwerp XDM in kaart brengt.

  Voor meer informatie over de vereiste gebieden, zie [ een gegevensmening in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md) in de Streaming Gids van de Inzameling van Media creëren.

  Voor informatie over het creëren van de gegevensmening, zie [ een gegevensmening in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md) creëren.


