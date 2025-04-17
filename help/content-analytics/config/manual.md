---
title: Handmatige configuratie van Content Analytics
description: Inhoud handmatig configureren
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
exl-id: 2b2d1cc2-36da-4960-ab31-0a398d131ab8
source-git-commit: bc2c959497230d7672d43d5cd409ca62d4627d6a
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Handmatige configuratie van Content Analytics

{{release-limited-testing}}


In dit artikel worden de handmatige handelingen beschreven die vereist zijn om de gegevensverzameling van een Content Analytics-configuratie te starten of te stoppen, of om uw Content Analytics-implementatie te bewerken.

De volgende handmatige configuratiehandelingen zijn beschikbaar:

## Gegevensverzameling starten

De gegevensverzameling starten voor een geïmplementeerde Content Analytics-configuratie:

1. Volg [ het publiceren stroom ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview){target="_blank"}. Publiceer met succes de bibliotheek voor het bezit van Markeringen dat uw configuratie van Content Analytics bevat.

1. [ installeer ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/environments/environments#installation) de ingebedde code in het `<head>` element van de pagina&#39;s op uw ontwikkelings, het opvoeren of het publiceren milieu, behoudens Content Analytics.


## Gegevensverzameling stoppen

De gegevensverzameling voor een geïmplementeerde Content Analytics-configuratie stoppen:

1. Verwijder de [ ingebedde code ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/environments/environments) in het `<head>` element van de pagina&#39;s op uw ontwikkelings, het opvoeren of productiemilieu, behoudens Content Analytics.
1. [ Schrap ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) het bijbehorende bezit van Markeringen voor uw configuratie van Content Analytics.



## Gegevensverzameling wijzigen

U kunt sommige minder belangrijke veranderingen in een uitgevoerde configuratie aanbrengen gebruikend de [ geleide configuratietovenaar ](guided.md). Wijzig bijvoorbeeld de gegevensweergave of schakel ervaringen in of uit.

U gebruikt de [ uitbreiding van Adobe Content Analytics ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview) in het bezit van Markeringen verbonden aan uw configuratie van Content Analytics om veranderingen in de volgende artefacten aan te brengen:

* [ Sandbox en datastream ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-datastreams){target="_blank"}.

  >[!CAUTION]
  >
  >Verifieer dat de zandbak en de gegevensstroom u in de uitbreiding van Adobe Content Analytics vormt reeds voor Content Analytics gebruikend de [ geleide configuratie ](guided.md) in een vroeger stadium worden gevormd. Deze configuratie zorgt ervoor dat alle vereiste artefacten beschikbaar zijn.<br/><br/> verifieert ook dat de updates voor zandbak of gegevensstromen zich niet in een andere configuratie van Content Analytics mengen die wordt gevormd om de zelfde zandbak of gegevensstromen te gebruiken.
  >

* [ Ervaring vangen en definitie ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview?lang=en#configure-experience-capture-and-definition)

  U kunt ervaringen in- of uitschakelen en de combinaties van reguliere expressie en queryparameters bewerken om te bepalen hoe inhoud op uw website wordt weergegeven.

* [ Gebeurtenissegmentering ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-event-segmenting){target="_blank"}

  U kunt reguliere expressies bewerken om de manier te wijzigen waarop u pagina&#39;s en elementen segmenteert.


Nadat u veranderingen in de uitbreiding van Adobe Content Analytics aanbrengt, verzeker uw gebruik [ het publiceren stroom ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview){target="_blank"} om de inzameling van gegevens te beginnen die op de aangebrachte veranderingen worden gebaseerd.



>[!MORELIKETHIS]
>
>[ Geleide configuratie ](guided.md)
>[Overzicht van de Codes voor gegevensverzameling ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview)
>


## Versioning

Als u Content Analytics-ervaringen wilt verzamelen, kunt u het beste een versie implementeren om ervoor te zorgen dat nieuwe ervaringen (wijzigingen in uw webpagina) correct worden verzameld.

Als u versioning wilt implementeren, voegt u een algemene `adobe.getContentExperienceVersion` functie toe op de pagina&#39;s die u een ervaring hebt die u wilt analyseren.

De functie `adobe.getContentExperienceVersion` moet een tekenreeks retourneren als waarde, wat u ook kunt kiezen, om de versie te identificeren. De versie wordt toegevoegd aan [ identiteitskaart URL van de Ervaring ](/help/content-analytics/report/components.md#experience-metadata).

Als de functie niet aanwezig is of geen waarde wordt geretourneerd van de functie, wordt de waarde `NoVersion` als standaardwaarde gebruikt.

### Voorbeeld

```
window.adobe = window.adobe || {};
window.adobe.getContentExperienceVersion = () => {
  return "1.0";
};
```
