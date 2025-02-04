---
title: Gegevenssets transformeren voor B2B-zoekopdrachten
description: Beschrijft hoe te om gegevens in datasets van specifieke B2B raadplegingsschema's om te zetten
solution: Customer Journey Analytics
feature: Connections
role: Admin
exl-id: 7729c1b9-b3ed-4662-a446-2088389bbd97
source-git-commit: 32678fdedf1b384afce1998880af04f1af077943
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Gegevenssets transformeren voor B2B-zoekopdrachten

Om op persoon-gebaseerde raadplegingen op B2B gegevens (met inbegrip van rekeningen, kansen, marketing lijsten en campagnes) te steunen, is de transformatie van B2B raadplegingsdatasets vereist.

Deze transformatie is slechts beschikbaar voor datasets met gegevens voor B2B raadplegingsschema&#39;s, die op de volgende klassen worden gebaseerd:

* [ XDM de Verhouding van de Persoon van de Bedrijfs Rekening ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account-person-relation)
* [ XDM de Verhouding van de Person van BedrijfsOpportunity ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity-person-relation)
* [ XDM Bedrijfs de Leden van de Lijst van de Marketing ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list-members)
* [ XDM Bedrijfs Campagne Leden ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign-members)

>[!NOTE]
>
>Er geldt een limiet van maximaal 10.000 items voor elke id. Deze beperking houdt in dat voor elke id van een persoon u slechts 10.000 rekeningen, of 10.000 kansen, of 10.000 marketing lijsten, of 10.000 campagnes kunt hebben.


Om transformatie voor zulk een dataset toe te laten:

![ laat transformatiedataset ](/help/connections/assets/transform.gif) toe

* Controleer voor elke dataset de voorgestelde waarden voor **[!UICONTROL Key]** en **[!UICONTROL Matching key]**. Als u de waarden wijzigt op basis van de voorgestelde waarden, verschijnt er een waarschuwing met de vraag of u wilt doorgaan. U moet ervoor zorgen dat:

   * De waarde u voor **Sleutel** selecteert is gebaseerd op het gegevenstype van identiteitskaart van de Persoon.
   * De waarde u voor **het Aanpassen Sleutel** selecteert wordt bepaald als primair identiteitsgebied voor de gebeurtenisdataset.

* Selecteer de opties voor het importeren van nieuwe gegevens en gegevenssetbackfill.

* Selecteer **[!UICONTROL Transform dataset for B2B lookups]** .

  Deze optie transformeert de dataset zodat kan het voor op persoon-gebaseerde raadplegingen in scenario&#39;s B2B worden gebruikt.


  >[!IMPORTANT]
  >
  >Wanneer de transformatie is ingeschakeld en wanneer de verbinding is opgeslagen, is deze onomkeerbaar. U kunt de Sleutel, het Aanpassen sleutel en de configuratie van de dataset van de Transformatie niet wijzigen. U kunt de dataset slechts verwijderen, toevoegen en dan aanpassen.

Om transformatie voor één of meerdere datasets toe te laten die reeds deel van een bestaande verbinding uitmaken:

1. Verwijder de datasets uit de verbinding.
1. Sla de verbinding op.
1. Voeg de datasets aan de verbinding toe terwijl het aanzetten van transformatie voor de datasets.

## Achtergrondinformatie

Niet-getransformeerde datasets, voor schema&#39;s die op de vier hierboven vermelde schemaklassen worden gebaseerd, kunnen veelvoudige rijen voor één enkel persoonsidentificatie bevatten. Op persoon gebaseerde raadplegingen komen alleen overeen met de meest recente instantie van die persoon-id, waardoor een correcte persoon-id niet kan worden opgezocht op basis van accounts, mogelijkheden, marketinglijsten of campagnes.

De transformatie wijzigt de dataset van elk van de vier schemaklassen (oranje in de illustratie hieronder) zodat voor elke persoonsidentificatie een (voorwerp) serie voor de relevante gegevens (rekeningen, kansen, marketing lijsten of campagnes) in de raadplegingsdatasets (roze in de illustratie hieronder) wordt gecreeerd. Deze transformatie maakt het mogelijk om correct te werken met op personen-id gebaseerde zoekopdrachten.

![ B2B- schema&#39;s ](./assets/b2b-schemas.svg)
