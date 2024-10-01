---
description: Met Curatie kunt u componenten beperken voordat u een project deelt.
keywords: Analysis Workspace curation
title: Cursieve projecten
feature: Curate and Share
exl-id: f9636191-8414-458c-9881-8c03f3d45efb
role: User
source-git-commit: de04792035aa7c235751019ee9f9fe5b74b9b102
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Cursieve projecten

Met Curatie kunt u de componenten (afmetingen, meetwaarden, filters, datumbereiken) beperken voordat u een project deelt. Wanneer een ontvanger het project opent, zullen zij een beperkte reeks componenten zien die u voor hen hebt gebogen. Curation is een optionele maar aanbevolen stap voordat een project wordt gedeeld.

>[!NOTE]
> Productprofielen zijn het belangrijkste mechanisme dat bepaalt welke componenten een gebruiker kan zien. Zij worden beheerd door de [ Admin Console van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html). Curatie is een secundair filter.

## Projectcursus toepassen

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]** .
De componenten die in het project worden gebruikt zullen automatisch worden toegevoegd.
1. (Optioneel) Als u meer componenten wilt toevoegen, sleept u de componenten die u wilt delen van het linkerdeelvenster naar het veld [!UICONTROL Curate Components] .
1. Klik op **[!UICONTROL Done]**.

U kunt de curve ook toepassen vanuit het menu [!UICONTROL Share] door op **[!UICONTROL Curate and Share]** te klikken. Deze optie leidt automatisch het project tot de componenten in gebruik in het project. U kunt aanvullende componenten toevoegen na de bovenstaande stappen.

![ het venster van de Componenten van de Kromme die de componenten in gebruik in het project tonen.](assets/curation-field.png)

## Samengevoegde projectweergave

Wanneer een ontvanger een gebogen project opent, zullen zij slechts de gebogen reeks componenten zien u hebt bepaald:

![ Een gedeeld beheerd project dat componenten toont u bepaalde.](assets/curate-project.png)

## Projectcursus verwijderen

U verwijdert de curatie van een project door de volledige set componenten in het linkerdeelvenster te herstellen:

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]** .
1. Klik op **[!UICONTROL Remove Curation]**.
1. Klik op **[!UICONTROL Done]**.

## Opties voor componentcurving

In een beheerd project krijgt de ontvanger de optie **[!UICONTROL Show All]** -componenten in het linkerdeelvenster. [!UICONTROL Show All] onthult verschillende reeksen componenten, afhankelijk van:

* Het machtigingsniveau van de gebruiker (beheerder of niet-beheerder)
* Projectrol (eigenaar/editor of niet)
* Type toegepaste kromming (op projectniveau)

| Curvetype | Admin kan | Niet-admin-projecteigenaar (of bewerkingsrol) kan zien | Niet-admin dubbele rol kan worden weergegeven |
| --- | --- | --- | --- |
| **Componenten &quot;verborgen&quot;van een gegevensmening** | Alle componenten van de gegevensmening beschikbaar voor het melden (de verborgen componenten vereisen klikkend &quot;toont allen&quot;) | Niet beschikbaar voor rapportage | Niet beschikbaar voor rapportage |
| **toegevoegde of verwijderde Componenten van een gegevensmening** | Alleen componenten die aan de gegevensweergave zijn toegevoegd (verborgen of niet verborgen). Beheerders kunnen geen gegevens rapporteren over velden of componenten die niet zijn gedefinieerd in de gegevensweergave. | Alleen componenten die zijn toegevoegd aan de gegevensweergave of componenten die eigendom zijn van of worden gedeeld met de gebruiker. Verborgen onderdelen zijn niet beschikbaar (zoals de cursus Virtuele rapportsuite). | Alleen componenten die aan de DV zijn toegevoegd, worden niet verborgen en zijn opgenomen in de projectcuratie. |
| **gekromde componenten in een Project** | Alle componenten van de gegevensmening beschikbaar voor het melden (de verborgen componenten vereisen klikkend &quot;toont allen&quot;) | Alle niet-verborgen componenten van de gegevensweergave (klik op Alles tonen) | Alleen gebogen componenten, plus eventuele componenten die eigendom zijn van of gedeeld worden met de gebruiker |
| **Gekleurd Project die een gegevensmening met verborgen componenten gebruiken** | Alle gegevenscomponenten die beschikbaar zijn voor rapportage (voor verborgen en niet-gekromde componenten moet u op Alles tonen klikken) | Alle niet-beheerde projectcomponenten, alle niet-verborgen componenten van de gegevensmening, en om het even welke componenten die door of met de gebruiker worden bezeten worden gedeeld | Alleen gebogen componenten, plus eventuele componenten die eigendom zijn van of gedeeld worden met de gebruiker |
