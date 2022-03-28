---
description: Gebruik ad-hocfilters in Analysis Workspace.
title: Ad-hocprojectfilters
feature: CJA Workspace Basics
role: User, Admin
exl-id: 79513ad9-3c9d-441e-a5c5-c2b1e5cacc2e
source-git-commit: c053a1517030b68875fe7f4518dbbd473dbe1b47
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---

# Ad-hocprojectfilters

Met ad-hocprojectfilters kunt u een component rechtstreeks naar de neerzetzone van het deelvenster slepen om een filter te maken. Het filter wordt een [filter op projectniveau](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-components/cja-filters/quick-filters.html) lokaal aan het huidige project.

Hier volgt een video over het maken van ad-hocprojectfilters:

>[!VIDEO](https://video.tv.adobe.com/v/23978/?quality=12)


1. 
   1. Zet een componenttype (afmetingen, afmeting, item, gebeurtenis, metrisch, segment, segmentsjabloon, datumbereik) neer in de neerzetzone van het filter boven in een deelvenster. Componenttypen worden automatisch omgezet in ad-hocfilters of [Snelle filters](/help/components/filters/quick-filters.md) indien compatibel.

   Hier ziet u hoe u een filter voor het Twitter-verwijzingsdomein kunt maken:

   ![](assets/ad-hoc1.png)

   Dit filter wordt automatisch toegepast in uw deelvenster en u kunt de resultaten direct zien.

1. U kunt een onbeperkt aantal filters toevoegen aan een deelvenster.
1. Raadpleeg de onderstaande sectie als u dit filter wilt opslaan.

Houd rekening met het volgende:

* U **kan** Zet de volgende componenttypen neer in de filterzone: berekende metriek en afmetingen/metriek waarvan u geen filters kunt bouwen.
* Voor volledige afmetingen en gebeurtenissen maakt Analysis Workspace &#39;exists&#39; raakfilters. Voorbeelden: `Hit where eVar1 exists` of `Hit where event1 exists`.
* Als &#39;unspecified&#39; of &#39;none&#39; wordt neergezet in de neerzetzone van het filter, wordt deze automatisch omgezet in een filter &#39;does not exist&#39;, zodat deze op de juiste wijze wordt behandeld tijdens het filteren.

## Ad-hocprojectfilters opslaan {#ad-hoc-save}

U kunt deze filters opslaan door de volgende stappen uit te voeren:

1. Houd de muisaanwijzer boven het filter in de neerzetzone en klik op het pictogram &quot;i&quot;.
1. Klik op het bewerkingspotlood om naar de Filterbouwer te gaan.
1. Controleren **[!UICONTROL Make available to all projects and add to your component list]**.
1. Klik op **[!UICONTROL SAVE]**.

Als het filter eenmaal is opgeslagen, is het beschikbaar in de lijst met onderdelen van het linkerspoor en kan het met andere gebruikers worden gedeeld via Filterbeheer.

