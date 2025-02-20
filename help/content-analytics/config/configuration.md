---
title: Inhoud analyseren configureren
description: Een overzicht van het configureren van Content Analytics
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
hide: true
hidefromtoc: true
exl-id: 3ea46223-c7d0-4b1f-bc84-4f35494f13a0
source-git-commit: cea253d3b1da080e6735989d59cc6eda44afc203
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# Inhoud analyseren configureren

>[!WARNING]
>
>Dit artikel is een voorlopige niet-officiële ontwerpversie van een toekomstige definitieve versie en maakt deel uit van de documentatie van Content Analytics. Alle inhoud kan worden gewijzigd en er kunnen geen wettelijke verplichtingen uit de huidige versie van dit artikel worden afgeleid.
>

{{release-limited-testing}}


Om Inhoud Analytics voor uw organisatie te vormen, gebruikt u de Inhoud Analytics [ geleide configuratie ](guided.md). De configuratietovenaar begeleidt u door alle stappen die worden vereist om de eerste vereisten voor een automatische configuratie van de Analytics van de Inhoud te plaatsen.

## Vereisten

Voordat u Content Analytics configureert, moet u controleren of aan de volgende voorwaarden is voldaan:

* U hebt de gebruikersagent en IP adres voor de featurisatieservice toegestaan-vermeld die in de Analytics van de Inhoud wordt gebruikt. De tekenreeks Gebruikersagent is `AdobeFeaturization/1.0` .
* U hebt een rol van Customer Journey Analytics Product Administrator, met de extra bevoegdheden om verbindingen te beheren en gegevensverzamelingen te beheren. De vereiste Experience Platform-machtigingen zijn:

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

   * Uw site is geschikt voor ervaringsrapporten? Een correcte rapportage van de ervaring is alleen mogelijk als aan de volgende voorwaarden is voldaan:
      * De site-inhoud wordt alleen door URL&#39;s aangestuurd.
      * De pagina&#39;s op uw site kunnen worden gereproduceerd met de pagina-URL en u begrijpt welke optionele URL-parameters een rol spelen.
   * U hebt een duidelijk inzicht in welke pagina&#39;s u de analyse en inzichten van de betrokkenheid van inhoud wilt vastleggen.
   * U hebt een duidelijk inzicht in welke (type) elementen u de analyse en inzichten van de betrokkenheid van inhoud wilt vastleggen.


>>
[!MORELIKETHIS]
>>
* [ Toegangsbeheer ](/help/technotes/access-control.md)
>


