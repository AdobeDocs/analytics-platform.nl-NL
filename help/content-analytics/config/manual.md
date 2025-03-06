---
title: Handmatige configuratie van Content Analytics
description: Inhoud handmatig configureren
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
hide: true
hidefromtoc: true
exl-id: 2b2d1cc2-36da-4960-ab31-0a398d131ab8
source-git-commit: 35298dd6d18ebb07d104a608aeff06cb864ee1dc
workflow-type: tm+mt
source-wordcount: '441'
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

Om een nieuwe configuratie of veranderingen te activeren u aan een bestaande configuratie aanbracht:

1. U moet de [ het publiceren stroom ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) volgen {target="_blank"}. Slechts wanneer u met succes de bibliotheek voor het bezit van de Markering hebt gepubliceerd dat uw configuratie van de Analytics van de Inhoud bevat, worden de gegevens van de Analytics van de Inhoud verzameld voor de domeinen, ervaringen en activa die u hebt gevormd.

1. U moet [ installeren ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/environments/environments#installation) inbedt code in het `<head>` element van de pagina&#39;s op uw ontwikkelings, het opvoeren of het publiceren milieu, behoudens de Analytics van de Inhoud.


## Deactiveren

Het verzamelen van gegevens voor inhoudsanalyse uitschakelen:

1. Verwijder [ bed code ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/environments/environments) in het `<head>` element van de pagina&#39;s op uw ontwikkelings, het opvoeren of productiemilieu, behoudens de Analytics van de Inhoud in.
1. [ Schrap ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) het bijbehorende bezit van de Markering voor u de configuratie van de Analytics van de Inhoud.



## Wijzigen

In het algemeen, zou u de [ geleide configuratietovenaar ](guided.md) moeten gebruiken om veranderingen in uw implementatie aan te brengen.

Alternatief, kunt u de [ uitbreiding van de Analyse van de Inhoud van Adobe ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview) in het bezit van de Markering gebruiken verbonden aan uw configuratie van de Analyse van de Inhoud om veranderingen in de volgende artefacten aan te brengen:

* [ Sandbox en datastream ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-datastreams) {target="_blank"}.

  >[!CAUTION]
  >
  >U moet verifiëren dat de zandbak en de gegevensstroom u in de uitbreiding van de Analyse van de Inhoud van Adobe vormt reeds voor Analytics van de Inhoud gebruikend de [ geleide configuratie ](guided.md) in een vroeger stadium worden gevormd. Deze configuratie zorgt ervoor dat alle vereiste artefacten beschikbaar zijn.<br/><br/> u moet ook verifiëren dat u updates voor zandbak of gegevensstromen zich niet in een andere configuratie van de Analyse van de Inhoud mengt die wordt gevormd om de zelfde zandbak of gegevensstromen te gebruiken.
  >

* [ Gebeurtenis het filtreren ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-event-filtering) {target="_blank"}

  U kunt reguliere expressies bewerken om de manier te wijzigen waarop u pagina&#39;s en elementen filtert.


Nadat u veranderingen in de uitbreiding van de Analyse van de Inhoud van Adobe aanbrengt, verzeker uw gebruik [ het publiceren stroom ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) {target="_blank"} om uw veranderingen te activeren.



>[!MORELIKETHIS]
>
>[ Geleide configuratie ](guided.md)
>[Overzicht van de Codes voor gegevensverzameling ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview)
>


## Versioning

Als u een versie van de ervaringen met Content Analytics nodig hebt, moet u een algemene `adobe.getContentExperienceVersion` functie toevoegen aan de pagina&#39;s die u een ervaring hebt die u wilt analyseren.

De functie `adobe.getContentExperienceVersion` moet een tekenreeks als waarde retourneren. Dit kan alles zijn wat u kiest om de versie te identificeren. De versie wordt toegevoegd aan de URL van de ervaring-id.

Als de functie niet aanwezig is of geen waarde wordt geretourneerd van de functie, wordt de waarde `NoVersion` als standaardwaarde gebruikt.

### Voorbeeld

```
function adobe.getContentExperienceVersion() {
  return "1.0";
}
```
