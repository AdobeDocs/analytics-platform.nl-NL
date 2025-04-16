---
title: Meer informatie over het publicatieoverzicht van Customer Journey Analytics Audiences
description: Meer informatie over het concept publiekspublicaties in Customer Journey Analytics
exl-id: 30404bfc-0ee7-4f01-842c-7e6156dc0b45
feature: Audiences
role: User, Admin
source-git-commit: 9393be88ab7320adb5bd046701667f638673af5e
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 1%

---

# Publicatieoverzicht publiek

U kunt publiek tot stand brengen en publiceren dat in Customer Journey Analytics aan [ wordt ontdekt het Profiel van de Klant in real time ](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl) in Adobe Experience Platform voor klant richt en verpersoonlijking.

Het publiek publiceert een duidelijke manier om inzichten die in Customer Journey Analytics zijn gevonden, te activeren en er actie tegen te ondernemen. Deze acties kunnen het volgende omvatten:

* Het publiek gebruiken voor een reis in Adobe Journey Optimizer.
* Het publiek naar een derde exporteren via een Experience Platform-bestemming.
* Het realtime-klantprofiel verrijken met nuttige kenmerken die zijn afgeleid van op gebeurtenissen gebaseerde gegevens in Customer Journey Analytics.
* Dit alles doen met minimale vertraging na publicatie van het publiek. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-components/audiences/publish.html#latency)
* Eenmalig publiek publiceren of terugkerend publiek.

Het publiek dat u in Customer Journey Analytics maakt, hoeft niet gebaseerd te zijn op gegevenssets die zijn ingeschakeld voor profiel. U kunt historische gegevens invoeren in Experience Platform zonder de bijbehorende gegevenssets en schema&#39;s voor profielen in te schakelen. Gebruik deze datasets vervolgens om relevante doelgroepen in Customer Journey Analytics te ontdekken en deze doelgroepen voor activeringsdoeleinden te publiceren naar Real-time Customer Profile in Experience Platform.

## Belangrijke terminologie

**Publiek**: Een reeks of een lijst van identiteiten die zowel een namespace als specifieke identiteitskaart met betrekking tot die namespace hebben. Soorten publiek kunnen vanuit de Adobe Experience Platform worden vervoerd en toepassingen die er bovenop zitten (zoals Customer Journey Analytics). Het publiek kan gemengde naamruimten bevatten.

**Segment**: Een reeks regels die, wanneer geëvalueerd over een reeks gegevens voor een tijdsperiode, een ondergroep van gegevens veroorzaakt. Een segment kan in het proces worden gebruikt om een publiek tot stand te brengen wanneer gekoppeld aan andere ondersteunende diensten. Segmenten worden gedefinieerd en onderhouden in Customer Journey Analytics.

## Machtigingen

* Beheerders krijgen automatisch de machtiging **[!UICONTROL Audience Publishing]** in Adobe Admin Console.

* Beheerders en beheerders van productprofielen kunnen individuele gebruikers toestemming geven voor **[!UICONTROL Audience Creation]** en **[!UICONTROL Audience View]** . Zie [ gebruiker-vlakke toegangsbeheer ](/help/technotes/access-control.md#user-level-access) voor meer informatie.

* Beheerders hebben ook de machtiging **[!UICONTROL Manage Profiles]** nodig in Adobe Experience Platform.

## Beheer van gegevens en toestemming

Wanneer u een publiek in Customer Journey Analytics publiceert, worden de labels en het beleid voor gegevensbeheer opgenomen die zijn gekoppeld aan de velden die worden gebruikt in het publiek.  Wanneer het publiek wordt geactiveerd in een Adobe Experience App, zijn alle bijbehorende labels en beleidsregels voor gegevensbeheer beschikbaar voor dat publiek en kan de juiste handhaving worden toegepast. [ leer meer over toestemming ](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html#consent-policy).

## Volgende stappen

* [Soorten publiek maken en publiceren](/help/components/audiences/publish.md)
* [Soorten publiek beheren](/help/components/audiences/manage.md)
