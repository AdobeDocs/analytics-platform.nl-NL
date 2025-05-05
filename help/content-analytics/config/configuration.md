---
title: Inhoud analyseren configureren
description: Een overzicht van het configureren van Content Analytics
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
exl-id: 3ea46223-c7d0-4b1f-bc84-4f35494f13a0
source-git-commit: 6d23203468032510446711ff5a874fd149531a9a
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Inhoud analyseren configureren

De configuratie van Content Analytics bestaat uit de volgende stappen:

![ Configuratie van Inhoud Analytics ](../assets/aca-configuration.svg){zoomable="yes"}

1. Gebruik de Content Analytics [ geleide configuratie ](guided.md) tovenaar om u door alle stappen te begeleiden die worden vereist aan opstelling de eerste vereisten voor een configuratie van Content Analytics. U kunt uw configuraties op elk ogenblik bewaren en later terugkeren.
1. Zodra u met de configuratiewaarden vertrouwd bent, kunt u de configuratie uitvoeren. Deze implementatie leidt tot alle vereiste artefacten, die op wat worden gebaseerd u in de tovenaar hebt gevormd.
1. Slechts wanneer u [ manueel ](manual.md) het bezit van Markeringen publiceert, wordt uw configuratie van Content Analytics effectief opgesteld en de gegevensinzameling is begonnen.

1. U kunt sommige minder belangrijke veranderingen in een uitgevoerde configuratie slechts aanbrengen gebruikend de [ geleide configuratie](guided.md) tovenaar. Bijvoorbeeld, verander de [ gegevensmening ](/help/data-views/data-views.md).
1. U kunt andere veranderingen in een uitgevoerde configuratie aanbrengen gebruikend de [ uitbreiding van Adobe Content Analytics ](https://experienceleague.adobe.com/nl/docs/experience-platform/tags/extensions/client/content-analytics/overview) in het bijbehorende bezit van Markeringen.
1. Slechts wanneer u [ manueel ](manual.md) het bezit van Markeringen opnieuw publiceert, worden de configuratiewijzigingen effectief opgesteld en de gegevensinzameling, die op uw veranderingen wordt gebaseerd, is begonnen.


## Vereisten

Voordat u Content Analytics configureert, moet u controleren of aan de volgende voorwaarden is voldaan:

* U hebt de gebruikersagent en IP adres voor de featurisatieservice toegestaan-vermeld die in de Analytics van de Inhoud wordt gebruikt. Het koord van de Agent van de Gebruiker om te vormen is: <code> AdobeFeaturization/1.0</code>.
* Als u [ SDK van het Web gebruikend JavaScript ](https://experienceleague.adobe.com/nl/docs/experience-platform/web-sdk/install/library){target="_blank"} voor regelmatige gedragsgegevensinzameling hebt uitgevoerd, zorg ervoor u de standaardnaam <code> gebruikt.</code> voor de JavaScript-bibliotheek.
* U hebt een Customer Journey Analytics Product Administrator-rol, met de extra machtigingen om verbindingen te beheren en gegevensweergaven te beheren.
* Als u overweegt om de ervaringen van Content Analytics te verzamelen, zorg u opstelling en werk [ Content Analytics versioning ](manual.md#versioning) bij die op veranderingen op uw Web-pagina&#39;s wordt gebaseerd.
* U moet [ toestemmingen voor gegevensinzameling ](https://experienceleague.adobe.com/nl/docs/experience-platform/collection/permissions){target="_blank"} hebben:
   * [ de toestemmingen van Experience Platform ](https://experienceleague.adobe.com/nl/docs/experience-platform/collection/permissions#adobe-experience-platform-permissions){target="_blank"}
   * [ de toestemmingen van de Inzameling van Gegevens van Experience Platform ](https://experienceleague.adobe.com/nl/docs/experience-platform/collection/permissions#adobe-experience-platform-data-collection-permissions){target="_blank"}
* U hebt zorgvuldig de volgende belangrijke configuratieopties overwogen:

   * Uw site is geschikt voor ervaringsrapporten. Een correcte rapportage van de ervaring is alleen mogelijk als aan de volgende voorwaarden is voldaan:
      * De pagina&#39;s op de site moeten reproduceerbaar zijn met de pagina-URL.
      * De tekstinhoud die door een bepaalde gebruiker wordt gezien, kan met de pagina-URL worden gereproduceerd en is niet afhankelijk van cookies of andere verpersoonlijkingsmechanismen.
   * U hebt een duidelijk inzicht in welke pagina&#39;s u de analyse en inzichten van de betrokkenheid van inhoud wilt vastleggen.
   * U hebt een duidelijk inzicht in welke (type) elementen u de analyse en inzichten van de betrokkenheid van inhoud wilt vastleggen.


## Toegangsbeheer

>[!IMPORTANT]
>
>Er is geen Content Analytics-machtiging die u kunt configureren om Content Analytics-toegang in of uit te schakelen voor individuele gebruikers of groepen gebruikers.
>

Om een gebruiker of een groep gebruikers toegang tot Content Analytics te verlenen, moet u de gebruiker of de groep gebruikers toegang tot één of meerdere [ gegevensmeningen verstrekken die voor Content Analytics ](guided.md#data-view) worden gevormd.

Deze toegang impliceert:

1. De voor Content Analytics ingeschakelde gegevensweergave maakt deel uit van de gegevensweergavemachtigingen voor een specifiek Customer Journey Analytics-productprofiel.
1. Dat specifieke Customer Journey Analytics-productprofiel is een van de productprofielen die aan de gebruiker of groep gebruikers zijn toegewezen.

>[!MORELIKETHIS]
>
>* [ Geleide configuratie ](guided.md)
>* [ Handmatige configuratie ](manual.md)
>* [ Toegangsbeheer ](/help/technotes/access-control.md)
>
