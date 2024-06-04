---
title: Gegevenssets transformeren voor B2B-zoekopdrachten
description: Beschrijft hoe te om gegevens in datasets van specifieke B2B raadplegingsschema's om te zetten
solution: Customer Journey Analytics
feature: Connections
role: Admin
source-git-commit: ffa57c19174bf1618957efe7191c8486c8e3a900
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Gegevenssets transformeren voor B2B-zoekopdrachten

Om op persoon-gebaseerde raadplegingen op B2B gegevens (met inbegrip van rekeningen, kansen, marketing lijsten en campagnes) te steunen, is de transformatie van B2B raadplegingsdatasets vereist.

Deze transformatie is slechts beschikbaar voor datasets met gegevens voor B2B raadplegingsschema&#39;s, die op de volgende klassen worden gebaseerd:

* XDM Zakelijke account Person Relatie
* XDM Business Opportunity Person Relatie
* Leden van XDM Business Marketing List
* XDM Business Campaign-leden

Om transformatie voor zulk een dataset toe te laten:

![Transformatiegegevensset inschakelen](assets/transform-dataset.gif)

* Zorg ervoor dat u de juiste id selecteert voor **[!UICONTROL Key]** en **[!UICONTROL Matching key]** bijvoorbeeld `personKey.sourceKey`.

* Selecteer de opties voor het importeren van nieuwe gegevens en gegevenssetbackfill.

* Selecteren **[!UICONTROL Transform dataset for B2B lookups]**.

  Deze optie transformeert de dataset zodat kan het voor op persoon-gebaseerde raadplegingen in scenario&#39;s B2B worden gebruikt.


  >[!IMPORTANT]
  >
  >Wanneer de transformatie is ingeschakeld en wanneer de verbinding is opgeslagen, is deze onomkeerbaar. U kunt transformatie niet wijzigen die voor een dataset plaatst zodra een verbinding wordt bewaard, behalve door de dataset te verwijderen en opnieuw aan de verbinding toe te voegen.

Om transformatie voor één of meerdere datasets toe te laten die reeds deel van een bestaande verbinding uitmaken:

1. Verwijder de datasets uit de verbinding.
1. Sla de verbinding op.
1. Voeg de datasets aan de verbinding toe terwijl het aanzetten van transformatie voor de datasets

## Achtergrondinformatie

Niet-getransformeerde datasets, voor schema&#39;s die op de vier hierboven vermelde schemaklassen worden gebaseerd, kunnen veelvoudige rijen voor één enkel persoonsidentificatie bevatten. Op persoon gebaseerde raadplegingen komen alleen overeen met de meest recente instantie van die persoon-id, waardoor een correcte persoon-id niet kan worden opgezocht op basis van accounts, mogelijkheden, marketinglijsten of campagnes.

De transformatie wijzigt de dataset van elk van de vier schemaklassen (oranje in de illustratie hieronder) zodat voor elke persoonsidentificatie een (voorwerp) serie voor de relevante gegevens (rekeningen, kansen, marketing lijsten of campagnes) in de raadplegingsdatasets (roze in de illustratie hieronder) wordt gecreeerd. Deze transformatie maakt het mogelijk om correct te werken met op personen-id gebaseerde zoekopdrachten.

![B2B-schema&#39;s](./assets/b2b-schemas.svg)
