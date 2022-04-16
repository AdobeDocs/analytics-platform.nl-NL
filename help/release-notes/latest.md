---
title: Huidige opmerkingen bij de release Customer Journey Analytics weergeven
description: Opmerkingen bij de nieuwste CJA-release
exl-id: e8eab856-34e0-4875-b441-b1e680b9e111
feature: Release Notes
source-git-commit: 56f62d8af96e64a6867e38a9701219bcefc62a6a
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 1%

---

# Opmerkingen bij de huidige release van Customer Journey Analytics (CJA) (april 2022)

>[!NOTE]
>
>Deze pagina bevat pre-releasegegevens die kunnen worden gewijzigd.

**Laatste update**: 13 april 2022

## Belangrijkste kenmerken

| Functie | Beschrijving | [Doeldatum](/help/release-notes/releases.md) |
| ----------- | ---------- | ----- |
| Dimension-subtekenreeksen | Verstrekt veelvoudige methodes om het gewenste deel van een koord voor gebruik als afmetingspunten te halen. Met deze functie kunt u ook een tekenreeksdimensie als een array behandelen als de tekenreeks gescheiden waarden bevat. [Meer informatie](../data-views/component-settings/substring.md) | 20 april 2022 |
| Data prep for Analytics Source Connector | De [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) is nu geïntegreerd met de [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html) door Adobe Experience Platform geboden mogelijkheden. Klanten van Adobe Real-time Customer Data Platform (RTCDP), CJA en Adobe Journey Optimizer (AJO) kunnen nu de veldgroep Analytics uitbreiden met extra veldgroepen. Ze kunnen ook gebruikmaken van 100+ Data Prep-operatoren om de analysegegevens te verrijken tijdens inname in Adobe Experience Platform (AEP). RTCDP-klanten kunnen nu meerdere voor gegevensvoorvoegsel ingeschakelde rapportsuites inschakelen voor Profiel.<p>CJA-klanten die meerdere rapportsuites via de Bronverbinding voor analyse invoeren, hebben nu een manier om kolomverschillen tussen rapportsuites te deconfliceren. Als bijvoorbeeld &quot;Zoekterm&quot; is opgeslagen in `eVar1` in één rapportsuite en in `eVar2` in een andere rapportreeks, die de Prep van Gegevens gebruikt kunt u de het gebiedsgroep van de Analyse met een nieuwe kolom uitbreiden die de waarden van twee eVars samenvoegt. | 25 april 2022 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>[Customer Journey Analytics-documentupdates](/help/release-notes/doc-changes.md)
