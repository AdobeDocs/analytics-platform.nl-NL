---
title: Streaming media-verzameling instellen voor Customer Journey Analytics
description: Meer informatie over het instellen van streaming media Collection voor Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: b807099d-a61d-48f9-9fec-94ecc6b76213
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Streaming media-verzameling instellen voor Customer Journey Analytics {#streaming-media-setup}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-media-edge"
>title="Media Edge instellen en implementeren"
>abstract="Als u van plan bent om de het stromen Inzameling van Media met Customer Journey Analytics te gebruiken, moet u specifieke selecties bij bepaalde stappen in het verbeteringsproces maken. Bijvoorbeeld, moet u de MediaAnalytics het gebiedsgroep van Details van Interacties aan uw schema toevoegen, Media Analytics in de gegevensstroom toelaten, en meer."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

Net als in Adobe Analytics kan de verzameling streamingmedia worden gebruikt voor het verzamelen van streaming mediagegevens voor gebruik in Customer Journey Analytics. Als u de Verzameling van de Media van de Streaming met Adobe Analytics gebruikt, zou u het in uw verbeteringsplannen aan Customer Journey Analytics moeten omvatten.

Terwijl u de stappen doorloopt om van Adobe Analytics naar Customer Journey Analytics te upgraden, maakt u de volgende selecties om uw gegevens voor streaming media Collection in te dienen:

* Wanneer u het schema voor Customer Journey Analytics maakt, neemt u de veldgroep `MediaAnalytics Interaction Details` op.

  Voor meer informatie over het toevoegen van deze gebiedsgroep, zie [ Opstelling het schema in Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#set-up-the-schema-in-adobe-experience-platform) in de Streaming Gids van de Inzameling van Media.

  Voor informatie over het creëren van het schema, zie [ een douaneschema tot stand brengen om met Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md) te gebruiken.

* Schakel Media Analytics in wanneer u de gegevensstroom voor Customer Journey Analytics configureert.

  Voor meer informatie over het toelaten van deze optie, zie [ een gegevensstroom in Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#configure-a-datastream-in-adobe-experience-platform) in de Streaming Gids van de Inzameling van Media vormen.

  Voor informatie over het creëren van de gegevensstroom, zie [ een gegevensstroom tot stand brengen om met Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-datastream.md) te gebruiken.

  >[!NOTE]
  >
  >Als uw Adobe Analytics-implementatie al gebruikmaakt van de Experience Platform Web SDK, is deze stap niet nodig.

* Neem bij het maken van een gegevensweergave voor Customer Journey Analytics de vereiste schemavelden op voor de verzameling streamingmedia.

  Zorg ervoor u deze schemagebieden aan de correcte waarden in het voorwerp XDM in kaart brengt.

  Voor meer informatie over de vereiste gebieden, zie [ een gegevensmening in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md) in de Streaming Gids van de Inzameling van Media creëren.

  Voor informatie over het creëren van de gegevensmening, zie [ een gegevensmening in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md) creëren.

<!--

------------------

The steps for implementing the Streaming Media Collection in Customer Journey Analytics differ depending on your current Streaming Media Collection implementation in Adobe Analytics. 

Streaming Media Collection can be implemented in Adobe Analytics in either of the following ways:

* [Edge Network implementations for the Streaming Media Collection](#edge-network-implementations)

* [Adobe Analytics-only implementations for the Streaming Media Collection](#adobe-analytics-only-implementations)

For more information about the differences between these implementation methods, see [Implement the Streaming Media Collection](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/overview) in the Streaming Media Collection Guide.

## Edge Network implementations for the Streaming Media Collection

If the Streaming Media Collection is [implemented using the Edge Network in your Adobe Analytics implementation](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/overview#edge-implementation-methods), this means that some steps that are required to upgrade the Streaming Media Collection to Customer Journey Analytics have already been completed as part of your Adobe Analytics implementation. Following are the completed steps:

* [Set up the schema in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#set-up-the-schema-in-adobe-experience-platform)

* [Create a dataset in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#create-a-dataset-in-adobe-experience-platform)

* [Configure a datastream in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#configure-a-datastream-in-adobe-experience-platform)

The following additional steps need to be completed as part of the upgrade to Customer Journey Analytics:

>[!NOTE]
>
>As you complete the Customer Journey Analytics upgrade steps, make sure you use the schema, dataset, and datastream from your Streaming Media Collection implementation in Adobe Analytics.

* [Create a connection in Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-connection.md)

* [Create a data view in Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md)


## Adobe Analytics-only implementations for the Streaming Media Collection

If the Streaming Media Collection is [implemented using an Adobe Analytics-only implementation in your Adobe Analytics environment](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/overview#adobe-analytics-only-implementation-methods), this means that Streaming Media data is not yet going to Edge Network. 

As you create the schema, dataset, datastream, connection, and data view as part of your upgrade from Adobe Analytics to Customer Journey Analytics, make the following selections to account for Streaming Media Collection data:

* When creating the schema for Customer Journey Analytics, include the `MediaAnalytics Interaction Details` field group.

  For more information about adding this field group, see [Set up the schema in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#set-up-the-schema-in-adobe-experience-platform) in the Streaming Media Collection Guide.

  For information about creating the schema, see [Create a custom schema to use with Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md).

* When configuring the datastream for Customer Journey Analytics, enable Media Analytics. 

  For more information about enabling this option, see [Configure a datastream in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/media-analytics/using/implementation/edge-recommended/media-edge-sdk/implementation-edge#configure-a-datastream-in-adobe-experience-platform) in the Streaming Media Collection Guide.

  For information about creating the datastream, see [Create a datastream to use with Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-datastream.md).

* When creating a data view for Customer Journey Analytics, include the required schema fields for the Streaming Media Collection.

  Make sure you map these schema fieldds to the correct values in the XDM object.

  For more information about the required fields, see [Create a data view in Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md) in the Streaming Media Collection Guide.

  For information about creating the data view, see [Create a data view in Customer Journey Analytics](/help/getting-started/cja-upgrade/cja-upgrade-dataview.md).

  -->
