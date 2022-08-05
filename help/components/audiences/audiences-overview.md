---
title: Publicatieoverzicht CJA-soorten publiek
description: Meer informatie over het concept publiekspublicaties in Customer Journey Analytics
exl-id: 30404bfc-0ee7-4f01-842c-7e6156dc0b45
source-git-commit: 94b3e7417b82e9ae3ad080884d4c184bee412c2c
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 1%

---

# Publicatieoverzicht van CJA Audience

>[!NOTE]
>
>Deze functie staat momenteel in [beperkte tests](/help/release-notes/releases.md).

U kunt nu publiek maken en publiceren dat is ontdekt in Customer Journey Analytics (CJA) naar [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en) (RTCP) in Adobe Experience Platform voor klantgerichtheid en personalisatie.

Het publiceren van publiek biedt een duidelijke manier om binnen CJA gevonden inzichten te activeren en actie te ondernemen. Deze acties kunnen het volgende omvatten:

* Het publiek gebruiken voor een reis in Adobe Journey Optimizer.
* Het publiek naar een derde via een bestemming van een Experience Platform exporteren.
* Het verrijken van het Real-Time klantenprofiel met nuttige attributen die uit op gebeurtenis-gebaseerde gegevens in CJA worden afgeleid.
* Dit alles doen met minimale vertraging na publicatie van het publiek (een paar minuten)
* Eenmalig publiek of terugkerend publiek publiceren

## Belangrijke terminologie

**Publiek**: Een reeks of lijst met identiteiten die zowel een naamruimte als een specifieke id hebben die betrekking hebben op die naamruimte. Soorten publiek kunnen vanuit de Adobe Experience Platform worden vervoerd en toepassingen die er bovenop zitten (zoals CJA). Soorten publiek kan gemengde naamruimten bevatten.

**Filter**: Een reeks regels die, wanneer geëvalueerd over een reeks gegevens voor een tijdspanne, een ondergroep van gegevens veroorzaakt. Een filter kan in het proces worden gebruikt om een publiek tot stand te brengen wanneer gekoppeld aan andere ondersteunende diensten. Filters worden gedefinieerd en onderhouden in CJA.

**Filters** versus **Segmenten**: CJA gebruikt het concept &quot;segmenten&quot; niet, maar gebruikt &quot;filters&quot;. Hoewel beide een reeks regels zijn die gelijkaardige logica kunnen bevatten, produceren zij verschillende output. Een filter wordt gebruikt om een dataset voor analysedoeleinden te versmallen. Een segment wordt gebruikt om een lijst met identiteiten te produceren die voor activering kunnen worden gebruikt. De segmenten produceren publiek in het Profiel van de Klant in real time, terwijl de filters (alleen) niet. CJA Audience Publishing is het proces waarmee we een CJA-filter gebruiken om een publiek te maken dat kan worden verbruikt door het Real-time klantprofiel.

## Toestemmingen

* Beheerders krijgen automatisch de opdracht **[!UICONTROL Audience Publishing]** toestemming in Adobe Admin Console.

* Beheerders kunnen deze machtiging verlenen aan individuele gebruikers.

* Beheerders hebben ook de opdracht **[!UICONTROL Manage Profiles]** toestemming in Adobe Experience Platform.

## Volgende stappen

* [Soorten publiek maken en publiceren](/help/components/audiences/publish.md)
* [Soorten publiek beheren](/help/components/audiences/manage.md)
