---
title: CJA Access Control
description: Leer over toegangsbeheervereisten voor de drie niveaus van toegang in CJA.
solution: Customer Journey Analytics
feature: CJA Basics
exl-id: c258fa39-c0b6-45a1-8547-79516c15a215
source-git-commit: ed1885b4dd560bdbce66a1fa2bad1bcd822a3ea3
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# CJA Access Control

Customer Journey Analytics (CJA) wordt bepaald door drie toegangsniveaus of drie rollen: De rol van Admin van het product, de rol van Admin van het Profiel van het Product, en gebruiker-vlakke toegang. In dit onderwerp worden deze rollen gedetailleerder beschreven.

## De rol Productbeheerder

Productbeheerders hebben machtigingen om alle taken uit te voeren die nodig zijn in CJA. U moet als productbeheerder aan de **Customer Journey Analytics-productprofiel** in de [Admin Console](https://adminconsole.adobe.com/enterprise/) onder Customer Journey Analytics > tabblad Beheer > Admin. Aan productbeheerders worden de volgende machtigingen verleend:

* Verbindingen of gegevensweergaven maken/bijwerken/verwijderen
* Projecten, filters, berekende metriek of filters die door andere gebruikers worden gemaakt bijwerken/verwijderen
* Werkruimteprojecten delen met alle gebruikers

Het alleen in Customer Journey Analytics beheren van een product is niet voldoende om een verbinding te maken, bij te werken of te verwijderen. Om een verbinding aan een dataset van de Experience Platform tot stand te brengen, hebt u ook de toestemmingen van het Experience Platform nodig. U moet specifiek deel uitmaken van een **Productprofiel Experience Platform** dat u de volgende toestemmingen geeft:

* Gegevensmodellering: Schema&#39;s weergeven, schema&#39;s beheren
* Gegevensbeheer: Datasets weergeven, Gegevens beheren
* Gegevensinname: Bronnen beheren
* Identiteitsnaamruimten weergeven

Voor meer informatie over de toestemmingen van het Experience Platform, zie [Toegangsbeheer in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html).

## Beheerdersrol productprofiel

Deze rol is vergelijkbaar met de productbeheerder, maar heeft een beperktere reikwijdte. Een productprofiel is een set machtigingen. Een beheerder van een productprofiel kan bijvoorbeeld toegang geven tot alle of specifieke gegevensweergaven aan leden van een productprofiel. Voor rapportagegereedschappen kunnen deze beheerders de volgende machtigingen toevoegen:

![beheerdersrechten](assets/permissions.png)

## Toegang op gebruikersniveau

Niet-productbeheerders (gebruikers) in Customer Journey Analytics kunnen geen gegevensweergaven of -verbindingen maken, bewerken of bekijken. De gebruikers kunnen filters, projecten, publiek, en berekende metriek met speciale toestemmingen in de Admin Console tot stand brengen.

## Workspace-projectcursus

Voor meer informatie over hoe te om componenten (afmetingen, metriek, segmenten, datumwaaiers) op het het projectniveau van de Werkruimte te beperken, en hoe de kromming aan gegevensmeningen gebonden is, zie [Cursieve projecten](/help/analysis-workspace/curate-share/curate.md).

## Toegang verlenen tot individuele metriek of dimensies

U kunt geen toestemmingen op individuele metriek of dimensies in Customer Journey Analytics verlenen of ontkennen zoals u in traditionele Adobe Analytics kunt. Metriek en afmetingen kunnen worden gewijzigd in [gegevensweergaven](/help/data-views/data-views.md) en zijn derhalve onderhevig aan wijzigingen in de CJA, die ook de rapportage met terugwerkende kracht wijzigen.

