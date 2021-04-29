---
title: Voeg globale raadplegingen aan uw datasets toe
description: Gebruik globale raadplegingen om de rapportage te vergroten met nuttige dimensies in Customer Journey Analytics.
exl-id: ab91659b-a1e6-4f6b-8976-410cf894d1a0
translation-type: tm+mt
source-git-commit: 8224fd2fde787f0d3cf0cb983641efc588c316b0
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Voeg globale raadplegingen aan uw datasets toe

Globale raadplegingen verbeteren de capaciteit van Customer Journey Analytics om over sommige dimensies/attributen te rapporteren die niet door zich nuttig zijn maar wanneer zich bij andere gegevens gevoegd. Voorbeelden zijn kenmerken van mobiele apparaten en kenmerken van de afmetingen van het besturingssysteem en de browser, zoals versienummers van de browser. Een &#39;Global Lookup&#39; lijkt sterk op een set opzoekgegevens (bekend als classificaties in traditionele Adobe Analytics). Globale zoekopdrachten zijn echter van toepassing op alle Experience Cloud-organisaties. Globale raadplegingen worden automatisch toegepast op alle gebeurtenisdatasets die bepaalde XDM schemagebieden bevatten (zie hieronder voor de specifieke gebieden.)
Voor elke schemaplaats die Adobe classificeert, bestaat een globale raadplegingsdataset. U kunt globale raadplegingsdatasets met de Bron van Analytics Schakelaar of met andere douanedatasets gebruiken die hen kunnen goedkeuren.

In traditionele Adobe Analytics worden deze dimensies alleen weergegeven, terwijl u in CJA deze dimensies actief moet opnemen wanneer u gegevensweergaven maakt. Wanneer een gebruiker, in het werkschema van Verbindingen, een dataset selecteert die als één met een sleutel voor globale raadplegingen wordt gemarkeerd, dan weet de gegevensmeningen UI om alle van de globale raadplegingsdimensies zoals beschikbaar voor het melden te omvatten. De werkstroom van gegevensweergaven weet om deze globale opzoekafmetingen zoals beschikbaar voor de gegevensmening te omvatten. De opzoekbestanden worden automatisch bijgewerkt en beschikbaar gehouden in alle regio&#39;s en voor alle accounts. Zij worden opgeslagen in regio-specifieke organisaties verbonden aan de klant.

## Globale raadplegingen van het gebruik met de datasets van de Gegevensverbinding van Adobe

De globale raadplegingsdatasets worden automatisch toegepast op rapporttijd. Als u [de Verbinding van Gegevens van Analytics](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=en#connectors) gebruikt en u in een dimensie brengt waarvoor Adobe een globale raadpleging verstrekt, passen wij automatisch deze globale raadpleging toe. Als een gebeurtenisdataset [XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en) gebieden bevat, kunnen wij globale raadplegingen op het toepassen.

## Beschikbare algemene opzoekvelden

* `browser`
   * `browser`, `group_id`, `id`
* `browser_group`
   * `browser_group`, `id`
* `os`
   * `os`,  `group_id`,  `id`
* `os_group`
   * `os_group`,  `id`
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

## Rapport over globale opzoekdimensies

Als u de globale opzoekafmetingen wilt rapporteren, moet u deze toevoegen wanneer u een gegevensweergave maakt in Customer Journey Analytics:

![](assets/global-lookup.png)

U kunt de opgezochte gegevens in Werkruimte dan zien:

![](assets/gl-reporting.png)
