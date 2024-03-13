---
title: Standaardraadplegingen toevoegen aan uw datasets
description: Gebruik standaardraadplegingen om rapportage met nuttige dimensies in Customer Journey Analytics te vergroten.
exl-id: ab91659b-a1e6-4f6b-8976-410cf894d1a0
solution: Customer Journey Analytics
feature: Connections
role: Admin
source-git-commit: 5807700b9fe10769bf86f5c4020dd7c23df6e616
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Standaardraadplegingen toevoegen aan uw datasets

>[!IMPORTANT]
>
>De standaard Lookups zijn slechts beschikbaar voor de gegevensbronnen van de bron van de Analyse schakelaar in Customer Journey Analytics. U kunt ze gebruiken met standaard Adobe Analytics-implementaties, of de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)of de Experience Platform-API&#39;s voor gegevensverzameling.
>

De standaardraadplegingen (die ook als Adobe-geleverde raadplegingen worden bekend) verbeteren de capaciteit van Customer Journey Analytics om over sommige dimensies/attributen te melden die niet door zich nuttig zijn maar wanneer zich bij andere gegevens gevoegd. Voorbeelden zijn kenmerken van mobiele apparaten en kenmerken van de afmetingen van het besturingssysteem en de browser, zoals versienummers van de browser. Een &quot;StandaardOpzoeken&quot;is gelijkaardig aan een raadplegingsdataset. De standaardraadplegingen zijn van toepassing op organisaties van het Experience Cloud. Zij worden automatisch toegepast op alle gebeurtenisdatasets die bepaalde XDM schemagebieden (zie hieronder voor de specifieke gebieden. bevatten) Een standaardraadplegingsdataset bestaat voor elke schemalplaats die de Adobe classificeert.

In traditionele Adobe Analytics worden deze dimensies op zichzelf weergegeven, terwijl u deze dimensies in de Customer Journey Analytics actief moet opnemen wanneer u gegevensweergaven maakt. In het werkschema van Verbindingen, selecteert u een dataset die als met een sleutel voor standaardraadpleging wordt gemarkeerd. De interface voor gegevensweergaven weet automatisch dat alle standaardopzoekafmetingen moeten worden opgenomen, zoals beschikbaar is voor rapportage. De opzoekbestanden worden automatisch bijgewerkt en beschikbaar gehouden in alle regio&#39;s en voor alle accounts. Zij worden opgeslagen in regio-specifieke organisaties verbonden aan de klant.

## Standaardraadplegingen gebruiken met de gegevenssets van de bronconnector van Analytics

De standaard raadplegingsdatasets worden automatisch toegepast op rapporttijd. Als u de de bronschakelaar van de Analyse gebruikt en u in een afmeting brengt waarvoor de Adobe een standaardraadpleging verstrekt, passen wij automatisch deze standaardraadpleging toe. Als een gebeurtenisdataset XDM gebieden bevat, kunnen wij standaardraadplegingen op het toepassen.

<!--
### Specific IDs that need to be populated

The following IDs need to be populated in the specific XDM mixins for this functionality to work:

* Environment Details Mixin – device/typeID value populated - Must match Device Atlas IDs and will populate device data.
* Adobe Analytics ExperienceEvent Template Mixin or Adobe Analytics ExperienceEvent Full Extension Mixin with analytics/environment/browserIDStr and analytics/environment/operatingSystemIDStr. Both must match the Adobe IDs and  populate browser and OS data, respectively.

You need these mixins with the three IDs populated (device/typeID, environment/browserIDStr, and environment/operatingSystemIDStr). The lookup dimensions will then be pulled automatically by Customer Journey Analytics and will be available in the Data View.

The catch here is that they can only populate those IDs today if they have a direct relationship with Device Atlas. They are Device Atlas IDs, and they provide an API to allow a customer to look them up. This is a significant hurdle, and we may just want to take the reference to this capability out of the product documentation until we have a productized way to expose the Device Atlas ID lookup functionality.
-->

### Beschikbare standaardopzoekvelden

* `browser`
   * `browser`, `group_id`, `id`
* `browser_group`
   * `browser_group`, `id`
* `os`
   * `os`, `group_id`, `id`
* `os_group`
   * `os_group`, `id`
* `mobile_audio_support - multi`
* `mobile_color_depth`
* `mobile_cookie_support`
* `mobile_device_name`
* `mobile_device_number_transmit`
* `mobile_device_type`
* `mobile_drm - multi`
* `mobile_image_support - multi`
* `mobile_information_services`
* `mobile_java_vm - multi`
* `mobile_mail_decoration`
* `mobile_manufacturer`
* `mobile_max_bookmark_url_length`
* `mobile_max_browser_url_length`
* `mobile_max_mail_url_length`
* `mobile_net_protocols - multi`
* `mobile_os`
* `mobile_push_to_talk`
* `mobile_screen_height`
* `mobile_screen_size`
* `mobile_screen_width`
* `mobile_video_support - multi`

## Rapport over standaardopzoekafmetingen

Om over de standaardraadplegingsdimensies te rapporteren, moet u hen toevoegen wanneer u een gegevensmening in Customer Journey Analytics creeert:

![Een gegevensweergave maken met de lijst Componenten toevoegen](assets/global-lookup.png)

U kunt de opgezochte gegevens in Werkruimte dan zien:

![Vrije-vormtabel met de gegevens](assets/gl-reporting.png)
