---
title: De opmerkingen bij de huidige release van de Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste release Customer Journey Analytics
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 6e94dcf003c26af5ce32544655477b1074b504b5
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 7%

---

# Huidige Adobe Customer Journey Analytics-releaseopmerkingen (september 2023)

**Laatste update**: 7 september 2023

Deze releaseopmerkingen betreffen de releaseperiode van 13 september 2023 tot en met 3 oktober 2023. Adobe Customer Journey Analytics-releases werken op een [continu leveringsmodel](releases.md) die voor een scalable, gefaseerde benadering van eigenschapplaatsing toestaat. Deze releaseopmerkingen worden daarom meerdere keren per maand bijgewerkt. Controleer ze regelmatig.

## Nieuwe of bijgewerkte functies

| Functie | Beschrijving | [Uitvoeren start](releases.md) | [Algemene beschikbaarheid](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **Steun voor classificaties A4T in de Bron van Analytics Schakelaar** | Ondersteuning voor nieuwe `correlationID` veld voor Adobe Analytics | De `_experience.decisioning.propositions.scopeDetails.correlationID` Het veld is nu beschikbaar in het Adobe Analytics-bronverbindingsschema. Dit veld wordt gebruikt ter ondersteuning van A4T-classificaties en wordt vanaf september 2023 ingevuld. | | N.v.t. | 12 september 2023 |
| **Updates voor afgeleide velden** | De volgende updates zijn uitgevoerd voor de functie voor afgeleide velden:<ul><li>De [!UICONTROL Lookup] functie is hernoemd naar [!UICONTROL Classify]met extra opties voor het laden van CSV-gegevens. **(releases 27 september 2023)**</li><li>Er zijn aanvullende functies beschikbaar die u kunt gebruiken bij het definiëren van een afgeleid veld: [!UICONTROL Trim], [!UICONTROL Lowercase] en [!UICONTROL Lookup].</li><li>Afgeleide velddefinities ondersteunen nu ook velden van [!UICONTROL Lookup] en [!UICONTROL Profile] datasets.</li></ul>[Meer informatie](/help/data-views/derived-fields/derived-fields.md) | N.v.t. | 13 september 2023 |
| **Nieuwe functies in Adobe Product Analytics** | <ul><li>**Anomaly Detection**: Vergelijk gebeurtenissen met verwachte waarden die zijn afgeleid van historische trends. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/guided-analysis/trends/usage.html)</li><li>**Trends Frequency of use view**: Bepaal de manier waarop u de functies aanpast op basis van de gebruiksfrequentie. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/guided-analysis/trends/frequency.html)</li><li>**Gebruikersvoorkeuren**: Configureer een aantal gebruikersvoorkeuren, zoals kleurenpaletten en getalnotatie. [Meer informatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/user-preferences.html)</li></ul> | N.v.t. | 18 september 2023 |
| **Zoeken naar Edge-apparaten** | Schakel automatische gegevensverzameling van apparaattypen in via het Edge-netwerk van het Experience Platform. Deze Experience Edge-service biedt voordelen voor Customer Journey Analytics samen met andere Experience Platform-apps. (Koppeling naar documentatie) | N.v.t. | 27 september 2023 |

{style="table-layout:auto"}

## Oplossingen in Customer Journey Analytics

AN-310972; AN-319509; AN-322245; AN-323411; AN-323719; AN-326101; AN-326125; AN-3 32688


## Belangrijke kennisgevingen voor beheerders van Customers Journey Analytics

| Bericht | Bericht toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| N.v.t. | N.v.t. | N.v.t. |

{style="table-layout:auto"}

## Aankondigingen van einde levensduur (EOL)

| EOL-product of -functie | Datum toegevoegd of bijgewerkt | Beschrijving |
| --- | --- | --- |
| **Migratie naar Adobe I/O OAuth Server-aan-Server geloofsbrieven** | 11 mei 2023 | Adobe Analytics API, Customer Journey Analytics API, en LiveStream klanten die de geloofsbrieven van JWT van Adobe I/O gebruiken moeten aan de geloofsbrieven van Adobe I/O OAuth Server-aan-Server door migreren **1 januari 2025**. Adobe I/O staat niet toe dat vanaf 1 mei 2024 nieuwe JWT-referenties worden gemaakt. Klanten die JWT gebruiken moeten een nieuwe Server-aan-Server referentie OAuth tot stand brengen of hun bestaande JWT-referentie migreren naar een OAuth Server-aan-Server referentie. Klanten moeten ook hun clienttoepassingen bijwerken om de nieuwe OAuth Server-to-Server referenties te kunnen gebruiken. <ul><li>[Migreren van JWT-gebruikersgegevens (Service Account)](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)</li><li>[De nieuwe OAuth Server-to-Server-referenties gebruiken](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation/)</li><li>[Veelgestelde vragen](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs/)</li></ul> |

{style="table-layout:auto"}


## Gerelateerde bronnen

* [Opmerkingen bij de vorige release van Customer Journey Analytics voor 2023](/help/release-notes/2023.md)
* [Opmerkingen bij de release van Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=en)
* [Opmerkingen bij de release Media Analytics](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Releaseopmerkingen bij Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl)
* [Documentatieupdates Customer Journey Analytics](/help/release-notes/doc-changes.md)
