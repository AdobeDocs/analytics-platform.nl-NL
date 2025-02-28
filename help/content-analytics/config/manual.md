---
title: Handmatige configuratie van Content Analytics
description: Inhoud handmatig configureren
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
hide: true
hidefromtoc: true
exl-id: 2b2d1cc2-36da-4960-ab31-0a398d131ab8
source-git-commit: 0cd9cd508d474df3dff176bca4596d0379ac86b4
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Handmatige configuratie van Content Analytics

>[!WARNING]
>
>Dit artikel is een voorlopige niet-officiële ontwerpversie van een toekomstige definitieve versie en maakt deel uit van de documentatie van Content Analytics. Alle inhoud kan worden gewijzigd en er kunnen geen wettelijke verplichtingen uit de huidige versie van dit artikel worden afgeleid.
>

{{release-limited-testing}}

In dit artikel worden de handmatige handelingen beschreven die vereist zijn om een Content Analytics-configuratie te activeren of deactiveren of om uw Content Analytics-implementatie te bewerken.

De volgende handmatige configuratiehandelingen zijn beschikbaar:

## Activeren

Om een nieuwe configuratie of veranderingen te activeren u aan een bestaande configuratie aanbracht, moet u [ publiceren ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) {target="_blank"} het bijbehorende bezit van de Markering. Alleen wanneer u de eigenschap Content Analytics Tag publiceert, worden de gegevens van Content Analytics verzameld voor de domeinen, ervaring en elementen die u hebt geconfigureerd.


## Deactiveren

Om het verzamelen gegevens van inhoudsanalyse te deactiveren, [ unpublish ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) {target="_blank"} het bijbehorende bezit van de Markering voor u de configuratie van de Analyse van de Inhoud.



## Wijzigen

In het algemeen, zou u de [ geleide configuratietovenaar ](guided.md) moeten gebruiken om veranderingen in uw implementatie aan te brengen.

U kunt ook de extensie Adobe Content Analytics in de eigenschap Tag gebruiken die is gekoppeld aan de configuratie Content Analytics om de volgende artefacten te wijzigen:

* [ Sandbox en datastream ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-datastreams) {target="_blank"}.

  >[!CAUTION]
  >
  >U moet verifiëren dat de zandbak en de gegevensstroom u in de uitbreiding van de Analyse van de Inhoud van Adobe vormt reeds voor Analytics van de Inhoud gebruikend de [ geleide configuratie ](guided.md) in een vroeger stadium worden gevormd. Deze configuratie zorgt ervoor dat alle vereiste artefacten beschikbaar zijn.<br/><br/> u moet ook verifiëren dat u updates voor zandbak of gegevensstromen zich niet in een andere configuratie van de Analyse van de Inhoud mengt die wordt gevormd om de zelfde zandbak of gegevensstromen te gebruiken.
  >

* [ Gebeurtenis het filtreren ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-event-filtering) {target="_blank"}.

  U kunt reguliere expressies bewerken om de manier te wijzigen waarop u pagina&#39;s en elementen filtert.


Nadat u veranderingen in de uitbreiding van de Analyse van de Inhoud van Adobe aanbrengt, zorg uw [ activeer ](#activate) uw veranderingen.



>[!MORELIKETHIS]
>
>[ Geleide configuratie ](guided.md)
>[Overzicht van de Codes voor gegevensverzameling ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview)
>