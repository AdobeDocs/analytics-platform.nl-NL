---
title: Standaardraadplegingen toevoegen aan uw datasets
description: Gebruik standaardraadplegingen om de rapportage te vergroten met nuttige dimensies in Customer Journey Analytics.
exl-id: ab91659b-a1e6-4f6b-8976-410cf894d1a0
solution: Customer Journey Analytics
source-git-commit: 067502a0d69bd0b085ecb5e6cbd3ae062f33daef
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Standaardraadplegingen toevoegen aan uw datasets

>[!IMPORTANT]
>De standaard Lookups zijn slechts beschikbaar voor de gegevensbronnen van de Verbinding van Gegevens van Analytics in CJA. U kunt deze alleen gebruiken als u de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) of de Experience Platform-gegevensverzameling-API&#39;s.

De standaardraadplegingen (die ook als Adobe-Geleverde raadplegingen worden bekend) verbeteren de capaciteit van Customer Journey Analytics om over sommige dimensies/attributen te melden die niet door zich nuttig zijn maar wanneer zich bij andere gegevens gevoegd. Voorbeelden zijn kenmerken van mobiele apparaten en kenmerken van de afmetingen van het besturingssysteem en de browser, zoals versienummers van de browser. Een &#39;Standaard opzoeken&#39; lijkt op een opzoekgegevensset. De standaardraadplegingen zijn toepasselijk over organisaties van Experience Cloud. Zij worden automatisch toegepast op alle gebeurtenisdatasets die bepaalde XDM schemagebieden (zie hieronder voor de specifieke gebieden. bevatten) Een standaardraadplegingsdataset bestaat voor elke schemalplaats die Adobe classificeert.

In traditionele Adobe Analytics worden deze dimensies alleen weergegeven, terwijl u in CJA deze dimensies actief moet opnemen wanneer u gegevensweergaven maakt. In het werkschema van Verbindingen, selecteert u een dataset die als met een sleutel voor standaardraadpleging wordt gemarkeerd. De interface voor gegevensweergaven weet automatisch dat alle standaardopzoekafmetingen moeten worden opgenomen, zoals beschikbaar is voor rapportage. De opzoekbestanden worden automatisch bijgewerkt en beschikbaar gehouden in alle regio&#39;s en voor alle accounts. Zij worden opgeslagen in regio-specifieke organisaties verbonden aan de klant.

## Standaardraadplegingen gebruiken met gegevenssets voor gegevensaansluiting voor Adobe-gegevens

De standaard raadplegingsdatasets worden automatisch toegepast op rapporttijd. Als u de Verbinding van Gegevens van Analytics gebruikt en u een afmeting brengt waarvoor Adobe een standaardraadpleging verstrekt, passen wij automatisch deze standaardraadpleging toe. Als een gebeurtenisdataset XDM gebieden bevat, kunnen wij standaardraadplegingen op het toepassen.

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

Als u de standaardopzoekafmetingen wilt rapporteren, moet u deze toevoegen wanneer u een gegevensweergave maakt in Customer Journey Analytics:

![](assets/global-lookup.png)

U kunt de opgezochte gegevens in Werkruimte dan zien:

![](assets/gl-reporting.png)
