---
title: Publicatieoverzicht van publiek publiek Customer Journey Analytics
description: Leer over het concept publiek publiceren in Customer Journey Analytics
exl-id: 30404bfc-0ee7-4f01-842c-7e6156dc0b45
feature: Audiences
source-git-commit: 3a3122934e0fb3d89ac94cc8be8799d43dd1c987
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 1%

---

# Publicatieoverzicht Customer Journey Analytics Publiek

U kunt nu publiek maken dat is ontdekt in Customer Journey Analytics naar [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en) in Adobe Experience Platform voor klantgerichtheid en personalisatie.

Het publiceren van publiek biedt een duidelijke manier om inzichten binnen Customer Journey Analytics te activeren en actie te ondernemen. Deze acties kunnen het volgende omvatten:

* Het publiek gebruiken voor een reis in Adobe Journey Optimizer.
* Het publiek naar een derde via een bestemming van een Experience Platform exporteren.
* Het verrijken van het Real-Time klantenprofiel met nuttige attributen die uit op gebeurtenis-gebaseerde gegevens in Customer Journey Analytics worden afgeleid.
* Dit alles doen met minimale vertraging na publicatie van het publiek. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-components/audiences/publish.html?lang=en#latency)
* Eenmalig publiek publiceren of terugkerend publiek.

Het publiek u in Customer Journey Analytics creeert moet niet op datasets worden gebaseerd die voor profiel worden toegelaten. U kunt historische gegevens in Experience Platform opnemen zonder bijbehorende datasets en schema&#39;s voor profiel toe te laten. Gebruik deze datasets vervolgens om relevante doelgroepen in de Customer Journey Analytics te ontdekken en deze doelgroepen voor activeringsdoeleinden te publiceren naar Real-time Customer Profile in Experience Platform.

## Belangrijke terminologie

**Publiek**: Een set of lijst met identiteiten met zowel een naamruimte als een specifieke id die betrekking heeft op die naamruimte. Soorten publiek kunnen vanuit de Adobe Experience Platform worden vervoerd en toepassingen die er bovenop zitten (zoals Customer Journey Analytics). Het publiek kan gemengde naamruimten bevatten.

**Filter**: Een reeks regels die, wanneer geëvalueerd over een reeks gegevens voor een tijdsperiode, een ondergroep van gegevens veroorzaakt. Een filter kan in het proces worden gebruikt om een publiek tot stand te brengen wanneer gekoppeld aan andere ondersteunende diensten. Filters worden gedefinieerd en onderhouden in de Customer Journey Analytics.

**Filters** versus **Segmenten**: Customer Journey Analytics gebruikt niet het begrip &quot;segmenten&quot;, maar gebruikt &quot;filters&quot;. Hoewel beide een reeks regels zijn die gelijkaardige logica kunnen bevatten, produceren zij verschillende output. Een filter wordt gebruikt om een dataset voor analysedoeleinden te versmallen. Een segment wordt gebruikt om een lijst met identiteiten te produceren die voor activering kunnen worden gebruikt. De segmenten produceren publiek in het Profiel van de Klant in real time, terwijl de filters (alleen) niet. Het Publiceren van het Publiek van de Customer Journey Analytics is het proces waardoor wij een filter van de Customer Journey Analytics gebruiken om een publiek tot stand te brengen dat door het Profiel van de Klant in real time kan worden verbruikt.

## Toestemmingen

* Beheerders krijgen automatisch de opdracht **[!UICONTROL Audience Publishing]** toestemming in Adobe Admin Console.

* Beheerders kunnen deze machtiging verlenen aan individuele gebruikers.

* Beheerders hebben ook de opdracht **[!UICONTROL Manage Profiles]** toestemming in Adobe Experience Platform.

## Beheer en instemming van gegevens

Wanneer u een publiek in Customer Journey Analytics publiceert, worden de etiketten en het beleid van het Beleid van Gegevens verbonden aan de gebieden die in het publiek worden gebruikt geregistreerd.  Wanneer het publiek in om het even welke app van de Ervaring van de Adobe wordt geactiveerd, zijn alle bijbehorende etiketten en het beleid van het Beleid van Gegevens beschikbaar voor dat publiek en de aangewezen handhaving kan worden toegepast. [Meer informatie over toestemming](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=en#consent-policy).

## Volgende stappen

* [Soorten publiek maken en publiceren](/help/components/audiences/publish.md)
* [Soorten publiek beheren](/help/components/audiences/manage.md)
