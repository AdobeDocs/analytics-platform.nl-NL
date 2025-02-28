---
title: Inhoud analyseren configureren
description: Een overzicht van het configureren van Content Analytics
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
hide: true
hidefromtoc: true
exl-id: 3ea46223-c7d0-4b1f-bc84-4f35494f13a0
source-git-commit: 596e54a559bac69214e1de3ea37da6177f110b7a
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 1%

---

# Inhoud analyseren configureren

>[!WARNING]
>
>Dit artikel is een voorlopige niet-officiële ontwerpversie van een toekomstige definitieve versie en maakt deel uit van de documentatie van Content Analytics. Alle inhoud kan worden gewijzigd en er kunnen geen wettelijke verplichtingen uit de huidige versie van dit artikel worden afgeleid.
>

{{release-limited-testing}}

De configuratie van Content Analytics bestaat uit de volgende stappen:

![ Configuratie van Inhoud Analytics ](../assets/aca-configuration.svg)

1. Gebruik de Inhoud Analytics [ geleide configuratie ](guided.md) tovenaar om u door alle stappen te begeleiden die worden vereist om de eerste vereisten voor een configuratie van de Analytics van de Inhoud te plaatsen. U kunt uw configuraties opslaan en later terugkeren.
1. Zodra u met de configuratiewaarden vertrouwd bent, kunt u de configuratie uitvoeren. Deze implementatie leidt tot alle vereiste artefacten, die op wat u in de tovenaar hebt gevormd worden gebaseerd. De volgende artefacten worden gecreeerd, bijgewerkt of geselecteerd:
   * Aangepaste reisanalyse
      * A [ gegevensmening ](/help/data-views/data-views.md) wordt geselecteerd.
      * A [ verbinding ](/help/connections/overview.md) wordt geselecteerd, automatisch afgeleid uit de geselecteerde gegevensmening.
   * Experience Platform
      * De sandbox wordt geselecteerd en wordt automatisch afgeleid van de verbinding. De benodigde workflows en services worden ingeschakeld in de sandbox.
      * Inhoudsanalyseschema&#39;s worden geselecteerd in de sandbox. Indien niet beschikbaar, worden de noodzakelijke schema&#39;s gecreeerd.
      * Gegevenssets voor inhoudanalyse zijn geselecteerd in de sandbox. Indien niet beschikbaar, worden de noodzakelijke datasets gecreeerd.
   * Gegevensverzameling
      * Een gegevensstroom wordt gecreeerd en de dienst van Experience Platform wordt gevormd binnen de gegevensstroom om gegevens aan de de ervaringsdataset van de Analyse van de Inhoud te stromen.
      * Een eigenschap Tag wordt gemaakt met de Adobe Content Analytics-extensie die is geconfigureerd voor de juiste sandbox, datastream en andere configuratieopties van de configuratietovenaar.
1. Alleen wanneer u de eigenschap Tag handmatig publiceert, wordt Content Analytics op effectieve wijze geïmplementeerd en geactiveerd.
1. U kunt sommige beperkte veranderingen in een uitgevoerde configuratie slechts aanbrengen gebruikend de [ geleide configuratie](guided.md) tovenaar. Bijvoorbeeld, verander de [ gegevensmening ](/help/data-views/data-views.md).
1. U kunt andere veranderingen in een uitgevoerde configuratie door de [ uitbreiding van de Analyse van de Inhoud van Adobe ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview) in het bijbehorende bezit van de Markering aanbrengen.
1. Slechts wanneer u manueel het bezit van de Markering opnieuw publiceert, worden de configuratiewijzigingen van stap 4 en 5 effectief opgesteld en geactiveerd.


Voordat u Content Analytics configureert, moet u controleren of aan de volgende voorwaarden is voldaan:


>[!PREREQUISITES]
>
>* U hebt de gebruikersagent en IP adres voor de featurisatieservice toegestaan-vermeld die in de Analytics van de Inhoud wordt gebruikt. De tekenreeks Gebruikersagent is `AdobeFeaturization/1.0` .
>* U hebt een rol van Customer Journey Analytics Product Administrator, met de extra bevoegdheden om verbindingen te beheren en gegevensverzamelingen te beheren. De vereiste Experience Platform-machtigingen zijn:
>  
>   | Categorie | Machtiging | Beschrijving |
>   |---|---|---|
>   | [!UICONTROL Data Collection] | Gegevensstromen weergeven | Alleen-lezen toegang tot gegevensstreams. |
>   | [!UICONTROL Data Collection] | Gegevensstromen beheren | Toegang tot het lezen, maken, bewerken en verwijderen van gegevensstromen. |
>   | [!UICONTROL Data Modeling] | [!UICONTROL View Schemas] | Alleen-lezen toegang tot schema&#39;s en gerelateerde bronnen. |
>   | [!UICONTROL Data Modeling] | [!UICONTROL Manage Schemas] | Toegang tot het lezen, maken, bewerken en verwijderen van schema&#39;s en gerelateerde bronnen. |
>   | [!UICONTROL Data Management] | [!UICONTROL View Datasets] | Alleen-lezen toegang voor gegevenssets en schema&#39;s. |
>   | [!UICONTROL Data Management] | [!UICONTROL Manage Datasets] | Toegang tot het lezen, creëren, uitgeven, en schrappen datasets. Alleen-lezen toegang voor schema&#39;s. |
>   | [!UICONTROL Data Ingestion] | [!UICONTROL Manage Sources] | Toegang tot bronnen lezen, maken, bewerken en uitschakelen. |
>   | [!UICONTROL Identity Management] | [!UICONTROL View Identity Namespaces] | Alleen-lezen toegang voor naamruimten. |
>
>* U hebt zorgvuldig de volgende belangrijke configuratieopties overwogen:
>
>   * Uw site is geschikt voor ervaringsrapporten? Een correcte rapportage van de ervaring is alleen mogelijk als aan de volgende voorwaarden is voldaan:
>   * De site-inhoud wordt alleen door URL&#39;s aangestuurd.
>   * De pagina&#39;s op uw site kunnen worden gereproduceerd met de pagina-URL en u begrijpt welke optionele URL-parameters een rol spelen.
>* U hebt een duidelijk inzicht in welke pagina&#39;s u de analyse en inzichten van de betrokkenheid van inhoud wilt vastleggen.
>* U hebt een duidelijk inzicht in welke (type) elementen u de analyse en inzichten van de betrokkenheid van inhoud wilt vastleggen.
>


>[!MORELIKETHIS]
>
>* [ Geleide configuratie ](guided.md)
>* [ Handmatige configuratie ](manual.md)
>* [ Toegangsbeheer ](/help/technotes/access-control.md)
>


