---
description: De cursus laat u componenten beperken alvorens een project te delen.
keywords: Analysis Workspace curation
title: Werkruimteprojecten van de curate
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 3%

---


# Werkruimteprojecten van de curate

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

De cursus laat u de componenten (afmetingen, metriek, segmenten, datumwaaiers) beperken alvorens een project te delen. Wanneer een ontvanger het project opent, zullen zij een beperkte reeks componenten zien die u voor hen hebt gebogen. De cursus is een facultatieve maar geadviseerde stap alvorens een project te delen.

>[!NOTE]
> De profielen van het product zijn het primaire mechanisme dat bepaalt welke componenten een gebruiker kan zien. Zij worden beheerd door de Console van Admin van de Ervaring van Adobe Cloud. Curatie is een secundair filter.

## projectcursus toepassen

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]**.
De componenten die in het project worden gebruikt zullen automatisch worden toegevoegd.
   **Opmerking**: Als een project veelvoudige rapportreeksen heeft, zult u een curate gebied voor elke rapportreeks in het project zien.
1. (Facultatief) om meer componenten toe te voegen, sleep componenten u van de linkerspoor aan wilt delen [!UICONTROL Curate Components] veld.
1. Klik op **[!UICONTROL Done]**.

De kromming kan ook vanaf [!UICONTROL Share] menu door te klikken **[!UICONTROL Curate and Share]**. Deze optie leidt automatisch het project tot de componenten in gebruik in het project. U kunt extra componenten na de stappen hierboven toevoegen.

![](assets/curation-field.png)

## Verboren projectweergave

Wanneer een ontvanger een gebogen project opent, zullen zij slechts de gebogen reeks componenten zien u hebt bepaald:

![](assets/curate-project.png)

## Verwijder projectcursus

Om de projectkromming te verwijderen en de volledige reeks componenten in de linkerspoorstaaf te herstellen:
1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Curate Project Data]**.
1. Klik op **[!UICONTROL Remove Curation]**.
1. Klik op **[!UICONTROL Done]**.

## Virtuele rapportcursus (VRS)

Om kromming op een rapport-reeks niveau toe te passen, zodat het op vele projecten meteen van toepassing is, kunt u [De curate componenten in een Virtuele Reeks van het Rapport (VRS)](https://docs.adobe.com/content/help/en/analytics/components/virtual-report-suites/vrs-components.html).

>[!NOTE]
> De kromming van VRS wordt altijd toegepast vóór projectkromming. Dit betekent dat zelfs als uw beheerd project bepaalde componenten omvat, zij uit zullen worden gefiltreerd als de gebogen VRS hen niet omvat.

## Alle componenten weergeven, optie

In een beheerd project of VRS, zal de ontvanger met de optie aan worden voorgesteld **[!UICONTROL Show All]** onderdelen in de linker spoorstaaf. [!UICONTROL Show All] openbaart verschillende reeksen componenten, afhankelijk van:

* Het de toestemmingsniveau van de gebruiker (admin of niet-admin)
* Projectrol (eigenaar/redacteur of niet)
* Soort curatie toegepast (VRS of project)

| Type valuta | Admins | Niet-beheerder projecteigenaar of geef rol uit | Niet-beheerder duplicaat of rol bekijken |
|---|---|---|---|
| Gecumuleerde VRS | Alle niet-gebogen VRS-onderdelen | Niet-gekrulde componenten van VRS die deze rol bezit of die met hen zijn gedeeld | Niet-gekrulde componenten van VRS die deze rol bezit of die met hen zijn gedeeld |
| Geautomatiseerd project | Alle niet-behandelde projectcomponenten | Alle niet-behandelde projectcomponenten | Niet-curated projectcomponenten die deze rol bezit of die met hen zijn gedeeld |
| Gecumuleerd project in een gelabelde VRS | Alle niet-gebogen onderdelen, vermeld onder **[!UICONTROL Non-Curated Project Components]** en **[!UICONTROL Non-Curated VRS Components]** | Alle niet-gebogen projectcomponenten EN niet-gebogen componenten van VRS die deze rol bezit of die met hen zijn gedeeld | Niet-gebogen VRS en projectcomponenten die deze rol bezit of die met hen zijn gedeeld |
