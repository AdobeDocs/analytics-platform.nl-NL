---
description: Leer hoe u projecten in Analysis Workspace kunt beheren. De kromming beperkt toegang tot componenten alvorens u een project deelt.
keywords: Analysis Workspace curation
title: Cursieve projecten
feature: Curate and Share
exl-id: f9636191-8414-458c-9881-8c03f3d45efb
role: User
source-git-commit: 084c995658a5cf698d253f1c15229f621a8c55d5
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# Cursieve projecten

Met Curatie kunt u de componenten (afmetingen, metriek, segmenten, datumbereiken) beperken voordat u een project deelt. Wanneer een ontvanger het project opent, zien zij een beperkte reeks componenten die u voor hen hebt gebogen. Curation is een optionele maar aanbevolen stap voordat een project wordt gedeeld.

>[!NOTE]
> Productprofielen zijn het belangrijkste mechanisme dat bepaalt welke componenten een gebruiker kan zien. Zij worden beheerd door [ Adobe Experience Cloud Admin Console ](https://experienceleague.adobe.com/nl/docs/core-services/interface/administration/admin-tool-experience-cloud). Curatie is een secundair segment.

## Projectcursus toepassen

1. Selecteer **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]** .
De componenten die in het project worden gebruikt worden automatisch toegevoegd.
Als een project veelvoudige gegevensmening heeft, ziet u een gebogen dalingsdoel voor elke gegevensmening in het project.
1. (Optioneel) Als u meer componenten wilt toevoegen, sleept u componenten die u wilt delen van het linkerdeelvenster naar de neerzetzone **[!UICONTROL Curate components]** voor de gegevensweergave.
1. Selecteer **[!UICONTROL Done]** .

<!--
Curation can also be applied from the [!UICONTROL Share] menu by selecting **[!UICONTROL Curate and Share]**. This option automatically curates the project to the components in use in the project. You can add additional components following the steps above.
-->

![ het venster van de Componenten van de Kromme die de componenten in gebruik in het project tonen.](assets/curation-field.png)

Wanneer een ontvanger een gebogen project opent, zien zij slechts de gebogen reeks componenten u hebt bepaald:


## Projectcursus verwijderen

U verwijdert de curatie van een project door de volledige set componenten in het linkerdeelvenster te herstellen:

1. Selecteer **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]** .
1. Selecteer **[!UICONTROL Remove Curation]** .
1. Selecteer **[!UICONTROL Done]** .

## Opties voor componentcurving

In een beheerd project krijgt de ontvanger de optie **[!UICONTROL Show All]** -componenten in het linkerdeelvenster. [!UICONTROL Show All] onthult verschillende reeksen componenten, afhankelijk van:

* Het machtigingsniveau van de gebruiker (beheerder of niet-beheerder)
* Projectrol (eigenaar/editor of niet)
* Type toegepaste kromming (op projectniveau)

| Curvetype | Admin kan | Niet-admin-projecteigenaar (of bewerkingsrol) kan zien | Niet-admin dubbele rol kan worden weergegeven |
| --- | --- | --- | --- |
| **Verborgen Componenten &#x200B;** van een gegevensmening **&#x200B; | Alle componenten van de gegevensweergave zijn beschikbaar voor rapportage (voor verborgen componenten moet u &#x200B;** [!UICONTROL Show all]** selecteren) | Niet beschikbaar voor rapportage | Niet beschikbaar voor rapportage |
| **toegevoegde of verwijderde Componenten van een gegevensmening** | Alleen componenten die aan de gegevensweergave zijn toegevoegd (verborgen of niet verborgen). Beheerders kunnen geen gegevens rapporteren over velden of componenten die niet in de gegevensweergave zijn gedefinieerd. | Alleen componenten die zijn toegevoegd aan de gegevensweergave of componenten die eigendom zijn van of worden gedeeld met de gebruiker. Verborgen onderdelen zijn niet beschikbaar (zoals de cursus Virtuele rapportsuite). | Alleen componenten die aan de gegevensweergave zijn toegevoegd, worden niet verborgen en worden opgenomen in de projectcuratie. |
| **gekromde componenten in een Project** | Alle componenten in de gegevensweergave die beschikbaar zijn voor rapportage (voor verborgen componenten moet u **[!UICONTROL Show all]** selecteren) | Alle niet-verborgen componenten van de gegevensweergave (klik op Alles tonen) | Alleen gebogen componenten, plus eventuele componenten die eigendom zijn van of gedeeld worden met de gebruiker |
| **Gekleurd Project die een gegevensmening met verborgen componenten gebruiken** | Alle gegevenscomponenten die beschikbaar zijn voor rapportage (voor verborgen en niet-verwerkte componenten moet u **[!UICONTROL Show all]** selecteren) | Alle niet-beheerde projectcomponenten, alle niet-verborgen componenten van de gegevensmening, en om het even welke componenten die door of met de gebruiker worden bezeten worden gedeeld | Alleen gebogen componenten, plus eventuele componenten die eigendom zijn van of gedeeld worden met de gebruiker |
