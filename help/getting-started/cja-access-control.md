---
title: CJA Access Control
description: Leer over toegangsbeheervereisten voor het creëren van verbindingen, het toevoegen van datasets, het creëren van gegevensmeningen, enz.
solution: Customer Journey Analytics
feature: CJA Basics
source-git-commit: 13513561ec288c1f4ab69128769cd0e7c059e44b
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---


# CJA Access Control

Om verbindingen tot stand te brengen, voeg datasets toe, etc., hebt u de volgende toestemmingen in nodig [Admin Console](https://adminconsole.adobe.com/enterprise/):

* Als u toegang wilt krijgen tot Customer Journey Analytics of verbinding wilt maken, moet u als beheerder aan de **Customer Journey Analytics-product** in de [Admin Console](https://adminconsole.adobe.com/enterprise/). Aan productbeheerders worden de volgende machtigingen verleend:
   * Verbindingen of gegevensweergaven maken/bijwerken/verwijderen
   * Projecten, filters, berekende metriek of filters die door andere gebruikers worden gemaakt bijwerken/verwijderen
   * Een Workspace-project delen met alle gebruikers
* Het alleen binnen Customer Journey Analytics beheren van een product is niet voldoende om een verbinding te maken, bij te werken of te verwijderen. Om een verbinding aan een dataset van de Experience Platform tot stand te brengen, hebt u ook de toestemmingen van het Experience Platform nodig. U moet specifiek deel uitmaken van een **Productprofiel Experience Platform** dat u de volgende toestemmingen geeft:
   * Schema&#39;s weergeven
   * Schema&#39;s beheren
   * Identiteitsnaamruimten weergeven
   * Gegevensbestanden weergeven

Voor meer informatie over de toestemmingen van het Experience Platform, zie [Toegangsbeheer in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html).

>[!NOTE]
>
>U kunt geen toestemmingen op individuele metriek of dimensies in Customer Journey Analytics verlenen of ontkennen zoals u in traditionele Adobe Analytics kunt. Metriek en afmetingen kunnen worden gewijzigd in [gegevensweergaven](/help/data-views/data-views.md) en zijn derhalve onderhevig aan wijzigingen in de CJA, die ook de rapportage met terugwerkende kracht wijzigen.

## Toegang van gebruikers

Niet-productbeheerders (gebruikers) in Customer Journey Analytics kunnen de Weergaven of Verbindingen van Gegevens niet bekijken, maar kunnen filters, projecten, en berekende metriek tot stand brengen.