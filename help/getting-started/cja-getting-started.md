---
title: Klantreisanalyse aan de slag
description: Klantreisanalyse wordt gestart.
translation-type: tm+mt
source-git-commit: 1aebe79040b6c8b9eb8a336e158f5ce6d2ea16a4

---


# Klantreisanalyse aan de slag

Om de Analyse van de Reis van de Klant uit te voeren, moet u deze werkschema volgen. Sommige aanvankelijke taken worden uitgevoerd in het Platform van de Ervaring van Adobe, en wat in de Analyse van de Reis van de Klant.

## Voorwaarden

Klantreisanalyse is beschikbaar voor klanten die

* Zijn de Analyse van Adobe [Uitgezochte, Eerste, of Ultieme](https://www.adobe.com/analytics/compare-adobe-analytics-packages.html) klanten
* Wordt provisioned voor het Platform van de Ervaring van [Adobe](https://www.adobe.com/experience-platform.html)
* De SKU van de Analyse van de Reis van de Klant hebben gekocht

## Werkstroom

| Taak | Indien uitgevoerd | Details |
|---|---|---|
| **Stap 1: Bereid uw gegevensschema voor** | Adobe Experience Platform | Het Model van de Gegevens van de Ervaring van [Adobe van het gebruik (XDM)](https://www.adobe.io/apis/experienceplatform/home/xdm.html) om de gegevens van de klantenervaring te standaardiseren en schema&#39;s voor het beheer van de klantenervaring te bepalen. |
| **Stap 2: Creeer een dataset die op het schema wordt gebaseerd** | Adobe Experience Platform | De gegevens in Platform bestaan uit gegevensreeksen, zoals e-mailgegevensreeksen, de datasets van CRM, POS- gegevensreeksen, de dataset van de Analyse van Adobe, enz. Elke gegevensreeksen bestaat uit een schema en partijen gegevens. U kunt een gegevensreeks [in het Platform](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/creating_a_dataset_tutorial/creating_a_dataset_tutorial.md)van de Ervaring tot stand brengen.<br>Hoewel het schema voor datasets die in de Analyse van de Reis van de Klant kan worden ingevoerd flexibel is, moet het met sommige basisregels in overeenstemming zijn. Het is best om ervoor te zorgen uw gegevens aan deze vereisten voldoen alvorens hen in Platform te uploaden. (Merk op dat het schema zowel metriek als afmetingen omvat.)<br>Er zijn drie types van gegevens die met de Analyse van de Reis van de Klant compatibel zijn:<ul><li>**Gebeurtenisgegevens**: Gegevens die gebeurtenissen in de tijd vertegenwoordigen (bv. Webbezoeken, interacties, transacties, POS-gegevens, enquêtegegevens, en peilgegevens, enz.). Dit is typische klikstroomgegevens, met een klantenidentiteitskaart of een koekjesidentiteitskaart, en timestamp. Met de gegevens van de Gebeurtenis, staan wij u toe om het even welke identiteitskaart te gebruiken u wilt.</li><li>**Gegevens** zoeken: Dit gegeven wordt gebruikt aan raadplegingswaarden of sleutels die in uw Gebeurtenis of gegevens van het Profiel worden gevonden. Bijvoorbeeld, zou u raadplegingsgegevens kunnen uploaden die numerieke IDs in uw gebeurtenisgegevens aan productnamen in kaart brengen.</li><li>**Profielgegevens**: Gegevens die op uw bezoekers, gebruikers, of klanten in de gegevens van de Gebeurtenis worden toegepast. Bijvoorbeeld, staat u toe om de gegevens van CRM over uw klanten te uploaden.</li></ul> |
| **Stap 3:verbindingen tussen platformdatasets en de Analyse van de Reis van de Klant tot stand brengen** | Klantreisanalyse | Zie Een verbinding [maken](/help/connections/create-connection.md). |
| **Stap 4: Gegevensweergaven maken** | Klantreisanalyse | Zie [Een gegevensweergave](/help/data-views/create-dataview.md)maken. |
| **Stap 5: Rapport over uw dwars-kanaalgegevens in Werkruimte** | Klantreisanalyse | Zie [Basisanalyse](/help/projects/perform-basic-analysis.md) uitvoeren en geavanceerde analyse [uitvoeren](/help/projects/perform-adv-analysis.md). |

## Bereid uw gegevensschema voor

[Creeer een schema gebruikend de Redacteur van het Schema](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/schema_editor_tutorial/schema_editor_tutorial.md)


