---
title: CJA Access Control
description: Leer over toegangsbeheervereisten voor het creëren van verbindingen, het toevoegen van datasets, het creëren van gegevensmeningen, enz.
solution: Customer Journey Analytics
feature: CJA Basics
exl-id: c258fa39-c0b6-45a1-8547-79516c15a215
source-git-commit: c80c10e1e4887bfe7fdc3b59d0dfe415b1b0d5eb
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# CJA Access Control

Als u taken wilt uitvoeren in Customer Journey Analytics, moet u als beheerder aan de **Customer Journey Analytics-productprofiel** in de [Admin Console](https://adminconsole.adobe.com/enterprise/). Aan productbeheerders worden de volgende machtigingen verleend:

* Verbindingen of gegevensweergaven maken/bijwerken/verwijderen
* Projecten, filters, berekende metriek of filters die door andere gebruikers worden gemaakt bijwerken/verwijderen
* Werkruimteprojecten delen met alle gebruikers

## Vereiste Adobe Experience Platform-machtigingen

Het alleen in Customer Journey Analytics beheren van een product is niet voldoende om een verbinding te maken, bij te werken of te verwijderen. Om een verbinding aan een dataset van de Experience Platform tot stand te brengen, hebt u ook de toestemmingen van het Experience Platform nodig. U moet specifiek deel uitmaken van een **Productprofiel Experience Platform** dat u de volgende toestemmingen geeft:

* Schema&#39;s weergeven
* Schema&#39;s beheren
* Identiteitsnaamruimten weergeven
* Gegevensbestanden weergeven

Voor meer informatie over de toestemmingen van het Experience Platform, zie [Toegangsbeheer in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html).

## Toegang verlenen tot individuele metriek of dimensies

U kunt geen toestemmingen op individuele metriek of dimensies in Customer Journey Analytics verlenen of ontkennen zoals u in traditionele Adobe Analytics kunt. Metriek en afmetingen kunnen worden gewijzigd in [gegevensweergaven](/help/data-views/data-views.md) en zijn derhalve onderhevig aan wijzigingen in de CJA, die ook de rapportage met terugwerkende kracht wijzigen.

## Toegang van gebruikers

Niet-productbeheerders (gebruikers) in Customer Journey Analytics kunnen geen gegevensweergaven of verbindingen weergeven, maar kunnen wel filters, projecten en berekende metriek maken.

