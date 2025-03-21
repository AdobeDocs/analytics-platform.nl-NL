---
title: Handmatige configuratie van Content Analytics
description: Inhoud handmatig configureren
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
hide: true
hidefromtoc: true
exl-id: 2b2d1cc2-36da-4960-ab31-0a398d131ab8
source-git-commit: 01459765d84a46d170c1619ffeae184957bbf839
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Handmatige configuratie van Content Analytics

{{draft-aca}}

{{release-limited-testing}}

In dit artikel worden de handmatige handelingen beschreven die vereist zijn om een Content Analytics-configuratie te activeren of deactiveren of om uw Content Analytics-implementatie te bewerken.

De volgende handmatige configuratiehandelingen zijn beschikbaar:

## Activeren

Om een nieuwe configuratie of veranderingen te activeren u aan een bestaande configuratie aanbracht:

1. U moet de [ het publiceren stroom ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) volgen {target="_blank"}. Publiceer met succes de bibliotheek voor het bezit van Markeringen dat uw configuratie van Content Analytics bevat.

1. U moet [ installeren ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/environments/environments#installation) de ingebedde code in het `<head>` element van de pagina&#39;s op uw ontwikkelings, het opvoeren of het publiceren milieu, behoudens Content Analytics.


## Deactiveren

De verzameling analytische gegevens van inhoud uitschakelen:

1. Verwijder de [ ingebedde code ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/environments/environments) in het `<head>` element van de pagina&#39;s op uw ontwikkelings, het opvoeren of productiemilieu, behoudens Content Analytics.
1. [ Schrap ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) het bijbehorende bezit van Markeringen voor uw configuratie van Content Analytics.



## Wijzigen

U kunt sommige minder belangrijke veranderingen in een uitgevoerde configuratie aanbrengen gebruikend de [ geleide configuratietovenaar ](guided.md). Wijzig bijvoorbeeld de gegevensweergave.

U gebruikt de [ uitbreiding van Adobe Content Analytics ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview) in het bezit van Markeringen verbonden aan uw configuratie van Content Analytics om veranderingen in de volgende artefacten aan te brengen:

* [ Sandbox en datastream ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-datastreams) {target="_blank"}.

  >[!CAUTION]
  >
  >Verifieer dat de zandbak en de gegevensstroom u in de uitbreiding van Adobe Content Analytics vormt reeds voor Content Analytics gebruikend de [ geleide configuratie ](guided.md) in een vroeger stadium worden gevormd. Deze configuratie zorgt ervoor dat alle vereiste artefacten beschikbaar zijn.<br/><br/> verifieert ook dat de updates voor zandbak of gegevensstromen zich niet in een andere configuratie van Content Analytics mengen die wordt gevormd om de zelfde zandbak of gegevensstromen te gebruiken.
  >

* [ Ervaring vangen en definitie ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview?lang=en#configure-experience-capture-and-definition)

  U kunt de reguliere expressie bewerken om de manier waarop u werkt te wijzigen.

* [ Gebeurtenis het filtreren ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-event-filtering) {target="_blank"}

  U kunt reguliere expressies bewerken om de manier te wijzigen waarop u pagina&#39;s en elementen filtert.


Nadat u veranderingen in de uitbreiding van de Analyse van de Inhoud van Adobe aanbrengt, verzeker uw gebruik [ het publiceren stroom ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) {target="_blank"} om uw veranderingen te activeren.



>[!MORELIKETHIS]
>
>[ Geleide configuratie ](guided.md)
>[Overzicht van de Codes voor gegevensverzameling ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview)
>


## Versioning

Als u een versie van uw Content Analytics-ervaringen nodig hebt, moet u een algemene `adobe.getContentExperienceVersion` functie toevoegen aan de pagina&#39;s die u een analyse wilt maken.

De functie `adobe.getContentExperienceVersion` moet een tekenreeks retourneren als waarde, wat u ook kunt kiezen, om de versie te identificeren. De versie wordt toegevoegd aan [ identiteitskaart URL van de Ervaring ](/help/content-analytics/report/components.md#experience-metadata).

Als de functie niet aanwezig is of geen waarde wordt geretourneerd van de functie, wordt de waarde `NoVersion` als standaardwaarde gebruikt.

### Voorbeeld

```
function adobe.getContentExperienceVersion() {
  return "1.0";
}
```
