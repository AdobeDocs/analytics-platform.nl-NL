---
description: Gebruik ad-hocfilters in Analysis Workspace.
title: Ad-hocprojectfilters
feature: Workspace Basics
role: User, Admin
source-git-commit: 275c552b14a4c2a47e00d0600ac3eae6811beae9
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---


# Ad-hocprojectfilters

Hier volgt een video over het maken van ad-hocprojectfilters:

>[!VIDEO](https://video.tv.adobe.com/v/23978/?quality=12)

U kunt ad hoc projectfilters tot stand brengen als u wilt snel onderzoeken hoe een filter uw project zou kunnen beïnvloeden, zonder naar de Bouwer van het Segment te gaan. Beschouw deze filters als tijdelijke filters op projectniveau. Ze maken doorgaans geen deel uit van uw filter &quot;bibliotheek&quot;, zoals componentfilters in de linkerrail. U kunt de bestanden echter opslaan, zoals hieronder wordt weergegeven.

Voor een vergelijking van wat ad-hoc projectfilters kunnen doen versus volledig-afgewerkte component-vlakke filters, ga [hier](/help/components/filters/filters-overview.md).

1. Zet een componenttype (afmetingen, afmeting, item, gebeurtenis, metrisch, filter, filtersjabloon, datumbereik) neer in de neerzetzone van het filter boven in een deelvenster. Componenttypen worden automatisch omgezet in filters.
Hier ziet u hoe u een filter voor het Twitter-verwijzingsdomein kunt maken:

   ![](assets/ad-hoc1.png)

   Dit filter wordt automatisch toegepast in uw deelvenster en u kunt de resultaten direct zien.

1. U kunt een onbeperkt aantal componenten aan een paneel toevoegen.
1. Raadpleeg de onderstaande sectie als u dit filter wilt opslaan.

Houd rekening met het volgende:

* U **kunt niet** de volgende componenttypen in de filterzone neerzetten: berekende metriek en afmetingen/metriek waarvan u geen filters kunt bouwen.
* Voor volledige afmetingen en gebeurtenissen maakt Analysis Workspace &#39;exists&#39; raakfilters. Voorbeelden: `Hit where eVar1 exists` of `Hit where event1 exists`.
* Als &#39;unspecified&#39; of &#39;none&#39; wordt neergezet in de neerzetzone van het filter, wordt deze automatisch omgezet in een filter &#39;does not exist&#39;, zodat deze op de juiste wijze wordt behandeld tijdens het filteren.

>[!NOTE]
>
>Segmenten die op deze manier worden gemaakt, bevinden zich intern in het project.

## Ad-hocprojectfilters opslaan {#ad-hoc-save}

U kunt deze filters opslaan door de volgende stappen uit te voeren:

1. Houd de muisaanwijzer boven het filter in de neerzetzone en klik op het pictogram &quot;i&quot;.
1. Klik in het informatievenster dat wordt weergegeven op **[!UICONTROL Save]**.

   ![](assets/segment-info.png)

## Wat zijn alleen-projectfilters?

Filters met alleen een project zijn snelle filters of ad-hocprojectfilters in de werkruimte. Wanneer het uitgeven van/het openen van hen in de filterbouwer dan zal het project-enige vakje verschijnen. Als ze een snel filter toepassen in de builder maar het selectievakje voor het beschikbaar stellen niet inschakelen, is het nog steeds een filter dat alleen voor het project geldt, maar kan het niet meer worden geopend in de builder voor kwaliteitscontrole. Als ze het selectievakje inschakelen en OPSLAAN, is dit nu een filter voor een lijst met componenten.