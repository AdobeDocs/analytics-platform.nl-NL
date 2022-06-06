---
title: Publicatieoverzicht CJA-soorten publiek
description: Meer informatie over het concept publiekspublicaties in Customer Journey Analytics
exl-id: 30404bfc-0ee7-4f01-842c-7e6156dc0b45
source-git-commit: cfc4824c214ba8b60877bebe10a697f706f9c2fb
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 1%

---

# Publicatieoverzicht van CJA Audience

>[!NOTE]
>
>Deze functionaliteit is momenteel in [beperkte tests](/help/release-notes/releases.md).

U kunt nu publiek maken en publiceren dat is ontdekt in Customer Journey Analytics (CJA) naar [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en) (RTCP) in Adobe Experience Platform voor klantgerichtheid en personalisatie. Met het Profiel van de Klant in real time, kunt u een holistische mening van elke individuele klant zien door gegevens van veelvoudige kanalen, met inbegrip van online, off-line, CRM, en derde te combineren. Het profiel staat u toe om uw klantengegevens in een verenigde mening te consolideren die een actionable, timestamped rekening van elke klanteninteractie aanbiedt.

Het publiek publiceert een duidelijke manier om actie te ondernemen tegen de inzichten die in CJA zijn gevonden. Deze acties kunnen het volgende omvatten:

* E-mails verzenden naar dit publiek.
* Pushberichten verzenden naar dit publiek.
* Het publiek gebruiken voor een reis in Adobe Journey Optimizer.
* Het publiek naar een derde via een bestemming van een Experience Platform exporteren.
* Het verrijken van het Real-time klantenprofiel met nuttige attributen die uit op gebeurtenis-gebaseerde gegevens in CJA worden afgeleid, zonder het moeten alle gebeurtenisgegevens aan RTCP toevoegen.

## Belangrijke terminologie

**Publiek**: Een reeks of lijst met identiteiten die zowel een naamruimte als een specifieke id hebben die betrekking hebben op die naamruimte. Soorten publiek kunnen vanuit de Adobe Experience Platform worden vervoerd en toepassingen die er bovenop zitten (zoals CJA). Soorten publiek kan gemengde naamruimten bevatten.

**Filter**: Een reeks regels die, wanneer geëvalueerd over een reeks gegevens voor een tijdspanne, een ondergroep van gegevens veroorzaakt. Een filter kan in het proces worden gebruikt om een publiek tot stand te brengen wanneer gekoppeld aan andere ondersteunende diensten. Filters worden gedefinieerd en onderhouden in CJA.

**Filters** versus **Segmenten**: CJA gebruikt het concept &quot;segmenten&quot; niet, maar gebruikt &quot;filters&quot;. Hoewel beide een reeks regels zijn die gelijkaardige logica kunnen bevatten, produceren zij verschillende output. Een filter wordt gebruikt om een dataset voor analysedoeleinden te versmallen. Een segment wordt gebruikt om een lijst met identiteiten te produceren die voor activering kunnen worden gebruikt. De segmenten produceren publiek in het Profiel van de Klant in real time, terwijl de filters (alleen) niet. CJA Audience Publishing is het proces waarmee we een CJA-filter gebruiken om een publiek te maken dat kan worden verbruikt door het Real-time klantprofiel.

## Toestemmingen

Beheerders krijgen automatisch de opdracht [!UICONTROL Audience Publishing] toestemming in Adobe Admin Console. Zij kunnen deze toestemming aan individuele gebruikers verlenen.

## Volgende stappen

* [Soorten publiek maken en publiceren](/help/components/audiences/publish.md)
* [Soorten publiek beheren](/help/components/audiences/manage.md)
