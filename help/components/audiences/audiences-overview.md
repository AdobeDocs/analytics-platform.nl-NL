---
title: Publicatieoverzicht CJA-soorten publiek
description: Meer informatie over het concept publiekspublicaties in Customer Journey Analytics
exl-id: 30404bfc-0ee7-4f01-842c-7e6156dc0b45
source-git-commit: 7b86650cd3475a203d597baeec2ec2152e082b10
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Publicatieoverzicht van CJA Audience

U kunt nu publiek maken en publiceren dat is ontdekt in Customer Journey Analytics (CJA) naar [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en) (RTCDP) in Adobe Experience Platform voor klantgerichtheid en personalisatie.

Het publiceren van publiek biedt een duidelijke manier om binnen CJA gevonden inzichten te activeren en actie te ondernemen. Deze acties kunnen het volgende omvatten:

* Het publiek gebruiken voor een reis in Adobe Journey Optimizer.
* Het publiek naar een derde via een bestemming van een Experience Platform exporteren.
* Het verrijken van het Real-Time klantenprofiel met nuttige attributen die uit op gebeurtenis-gebaseerde gegevens in CJA worden afgeleid.
* Dit alles doen met minimale vertraging na publicatie van het publiek. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-components/audiences/publish.html?lang=en#latency)
* Eenmalig publiek publiceren of terugkerend publiek.

Het publiek u in CJA creeert moet niet op datasets worden gebaseerd die voor profiel worden toegelaten. U kunt historische gegevens in Experience Platform opnemen zonder bijbehorende datasets en schema&#39;s voor profiel toe te laten. Vervolgens gebruikt u deze gegevenssets om relevante doelgroepen in CJA te ontdekken en deze doelgroepen naar RTCDP in Experience Platform te publiceren voor activeringsdoeleinden.

## Belangrijke terminologie

**Publiek**: Een reeks of lijst met identiteiten die zowel een naamruimte als een specifieke id hebben die betrekking hebben op die naamruimte. Soorten publiek kunnen vanuit de Adobe Experience Platform worden vervoerd en toepassingen die er bovenop zitten (zoals CJA). Soorten publiek kan gemengde naamruimten bevatten.

**Filter**: Een reeks regels die, wanneer geëvalueerd over een reeks gegevens voor een tijdspanne, een ondergroep van gegevens veroorzaakt. Een filter kan in het proces worden gebruikt om een publiek tot stand te brengen wanneer gekoppeld aan andere ondersteunende diensten. Filters worden gedefinieerd en onderhouden in CJA.

**Filters** versus **Segmenten**: CJA gebruikt het concept &quot;segmenten&quot; niet, maar gebruikt &quot;filters&quot;. Hoewel beide een reeks regels zijn die gelijkaardige logica kunnen bevatten, produceren zij verschillende output. Een filter wordt gebruikt om een dataset voor analysedoeleinden te versmallen. Een segment wordt gebruikt om een lijst met identiteiten te produceren die voor activering kunnen worden gebruikt. De segmenten produceren publiek in het Profiel van de Klant in real time, terwijl de filters (alleen) niet. CJA Audience Publishing is het proces waarmee we een CJA-filter gebruiken om een publiek te maken dat kan worden verbruikt door het Real-time klantprofiel.

## Toestemmingen

* Beheerders krijgen automatisch de opdracht **[!UICONTROL Audience Publishing]** toestemming in Adobe Admin Console.

* Beheerders kunnen deze machtiging verlenen aan individuele gebruikers.

* Beheerders hebben ook de opdracht **[!UICONTROL Manage Profiles]** toestemming in Adobe Experience Platform.

## Beheer en instemming van gegevens

Wanneer u een publiek in CJA publiceert, worden de etiketten en het beleid van het Beleid van Gegevens verbonden aan de gebieden die in het publiek worden gebruikt geregistreerd.  Wanneer het publiek wordt geactiveerd in een Adobe Experience App, zijn alle bijbehorende labels en beleidsregels voor gegevensbeheer beschikbaar voor dat publiek en kan de juiste handhaving worden toegepast. [Meer informatie over toestemming](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=en#consent-policy).

## Volgende stappen

* [Soorten publiek maken en publiceren](/help/components/audiences/publish.md)
* [Soorten publiek beheren](/help/components/audiences/manage.md)
