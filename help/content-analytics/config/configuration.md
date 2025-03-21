---
title: Inhoud analyseren configureren
description: Een overzicht van het configureren van Content Analytics
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
hide: true
hidefromtoc: true
exl-id: 3ea46223-c7d0-4b1f-bc84-4f35494f13a0
source-git-commit: 01459765d84a46d170c1619ffeae184957bbf839
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Inhoud analyseren configureren

{{draft-aca}}

{{release-limited-testing}}

De configuratie van Content Analytics bestaat uit de volgende stappen:

![ Configuratie van Inhoud Analytics ](../assets/aca-configuration.svg){zoomable="yes"}

1. Gebruik de Content Analytics [ geleide configuratie ](guided.md) tovenaar om u door alle stappen te begeleiden die worden vereist aan opstelling de eerste vereisten voor een configuratie van Content Analytics. U kunt uw configuraties op elk ogenblik bewaren en later terugkeren.
1. Zodra u met de configuratiewaarden vertrouwd bent, kunt u de configuratie uitvoeren. Deze implementatie leidt tot alle vereiste artefacten, die op wat worden gebaseerd u in de tovenaar hebt gevormd.
1. Slechts wanneer u [ manueel ](manual.md) het bezit van Markeringen publiceert, zal uw configuratie van Content Analytics effectief worden opgesteld en geactiveerd.

1. U kunt sommige minder belangrijke veranderingen in een uitgevoerde configuratie slechts aanbrengen gebruikend de [ geleide configuratie](guided.md) tovenaar. Bijvoorbeeld, verander de [ mening van Gegevens ](/help/data-views/data-views.md).
1. U kunt andere veranderingen in een uitgevoerde configuratie aanbrengen gebruikend de [ uitbreiding van Adobe Content Analytics ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview) in het bijbehorende bezit van Markeringen.
1. Slechts wanneer u [ manueel ](manual.md) het bezit van Markeringen opnieuw publiceert, worden de configuratiewijzigingen effectief opgesteld en geactiveerd.


## Vereisten

Voordat u Content Analytics configureert, moet u controleren of aan de volgende voorwaarden is voldaan:

* U hebt de gebruikersagent en IP adres voor de featurisatieservice toegestaan-vermeld die in de Analytics van de Inhoud wordt gebruikt. Het koord van de Agent van de Gebruiker om te vormen is: <code> AdobeFeaturization/1.0</code>.
* U hebt een Customer Journey Analytics Product Administrator-rol, met de extra machtigingen om verbindingen te beheren en gegevensweergaven te beheren.
* U hebt de vereiste Experience Platform-machtigingen:

  | Categorie | Machtiging | Beschrijving |
  |---|---|---|
  | [!UICONTROL Data Collection] | Gegevensstromen weergeven | Alleen-lezen toegang tot gegevensstreams. |
  | [!UICONTROL Data Collection] | Gegevensstromen beheren | Toegang tot het lezen, maken, bewerken en verwijderen van gegevensstromen. |
  | [!UICONTROL Data Modeling] | [!UICONTROL View Schemas] | Alleen-lezen toegang tot schema&#39;s en gerelateerde bronnen. |
  | [!UICONTROL Data Modeling] | [!UICONTROL Manage Schemas] | Toegang tot het lezen, maken, bewerken en verwijderen van schema&#39;s en gerelateerde bronnen. |
  | [!UICONTROL Data Management] | [!UICONTROL View Datasets] | Alleen-lezen toegang voor gegevenssets en schema&#39;s. |
  | [!UICONTROL Data Management] | [!UICONTROL Manage Datasets] | Toegang tot het lezen, creëren, uitgeven, en schrappen datasets. Alleen-lezen toegang voor schema&#39;s. |
  | [!UICONTROL Data Ingestion] | [!UICONTROL Manage Sources] | Toegang tot bronnen lezen, maken, bewerken en uitschakelen. |
  | [!UICONTROL Identity Management] | [!UICONTROL View Identity Namespaces] | Alleen-lezen toegang voor naamruimten. |

* U hebt zorgvuldig de volgende belangrijke configuratieopties overwogen:

   * Uw site is geschikt voor ervaringsrapporten. Een correcte rapportage van de ervaring is alleen mogelijk als aan de volgende voorwaarden is voldaan:
      * U kunt de site-inhoud alleen benaderen door openbare URL&#39;s. Voor toegang tot de site zijn geen persoonlijke tokens, cookies of andere mechanismen vereist die niet beschikbaar zijn via de URL.
      * De pagina&#39;s op uw site kunnen worden gereproduceerd met de pagina-URL en u begrijpt welke optionele URL-parameters een rol spelen.
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
