---
title: Aan de slag met de analyse van de reis van de klant
description: De Analyse van de Reis van de klant Begonnen.
translation-type: tm+mt
source-git-commit: 12ab54b09caea3b7bb5fbc345ba5e396c198a36c

---


# Aan de slag met de analyse van de reis van de klant

Om de Analyse van de Reis van de Klant uit te voeren, moet u deze werkschema volgen. Sommige initiële taken worden uitgevoerd in het Adobe Experience Platform en andere in de Analyse voor reizen van klanten.

| Taak | Waar uitgevoerd | Details |
|---|---|---|
| **Stap 1: Uw gegevens ophalen in het Adobe Experience Platform** | Adobe Experience Platform |  |
| **Stap 2: Gegevensschema voorbereiden** | Adobe Experience Platform | Met [Adobe Experience Data Model (XDM)](https://www.adobe.io/apis/experienceplatform/home/xdm.html) kunt u gegevens voor klantervaring standaardiseren en schema&#39;s definiëren voor het beheer van klantervaring. |
| **Stap 3: Creeer een dataset die op het schema wordt gebaseerd** | Adobe Experience Platform | De gegevens in Platform bestaan uit gegevensreeksen, zoals e-mailgegevensreeksen, de datasets van CRM, POS gegevensreeksen, de dataset van de Analyse van Adobe, enz.. Elke gegevensset bestaat uit een schema en gegevensbatches. U kunt een gegevensset maken [in Experience Platform](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/creating_a_dataset_tutorial/creating_a_dataset_tutorial.md).<br>Hoewel het schema voor datasets die in de Analyse van de Reis van de Klant kunnen worden ingevoerd flexibel is, moet het met sommige basisregels in overeenstemming zijn. U kunt het beste controleren of uw gegevens aan deze vereisten voldoen voordat u ze uploadt naar Platform. (Schema bevat zowel metriek als afmetingen.)<br>Er zijn drie soorten gegevens die compatibel zijn met de Analyse van de Reis van de Klant:<ul><li>**Gebeurtenisgegevens**: Gegevens die gebeurtenissen in de tijd vertegenwoordigen (bv. webbezoeken, interacties, transacties, POS-gegevens, enquêtegegevens, gegevens van de indruk enz.). Dit zijn typisch klikstroomgegevens, met een klant identiteitskaart of een koekjesidentiteitskaart, en een timestamp. Met gebeurtenisgegevens kunt u de gewenste id gebruiken.</li><li>**Gegevens** opzoeken: Deze gegevens worden gebruikt voor het opzoeken van waarden of toetsen in de gebeurtenis- of profielgegevens. U kunt bijvoorbeeld opzoekgegevens uploaden waarmee numerieke id&#39;s in uw gebeurtenisgegevens worden toegewezen aan productnamen.</li><li>**Profielgegevens**: Gegevens die worden toegepast op uw bezoekers, gebruikers of klanten in de gebeurtenisgegevens. Bijvoorbeeld, staat u toe om de gegevens van CRM over uw klanten te uploaden.</li></ul> |
| **Stap 3:Verbindingen maken tussen platformdatasets en de Analyse van de Reis van de Klant** | Klantreisanalyse | Zie Verbinding [maken](/help/connections/create-connection.md). |
| **Stap 4: Gegevensweergaven maken** | Klantreisanalyse | Zie [Een gegevensweergave](/help/data-views/create-dataview.md)maken. |
| **Stap 5: Rapport over uw kanaalgegevens in Workspace** | Klantreisanalyse | Zie [Basisanalyse](/help/projects/perform-basic-analysis.md) uitvoeren en [Geavanceerde analyse](/help/projects/perform-adv-analysis.md)uitvoeren. |

## Vereisten

Klantreisanalyse is beschikbaar voor klanten die

* Zijn Adobe Analytics [Select-, Premier- of Ultimate](https://www.adobe.com/analytics/compare-adobe-analytics-packages.html) -klanten, en
* zijn ingericht voor het [Adobe Experience Platform](https://www.adobe.com/experience-platform.html), en
* De SKU voor de analyse van de reis van de klant hebben aangeschaft

## Gegevensschema voorbereiden

[Een schema maken met de Schema-editor](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/schema_editor_tutorial/schema_editor_tutorial.md)

## Stap 1: Uw gegevens ophalen in het Adobe Experience Platform

Voordat u gegevens van het Experience Platform kunt gebruiken in CJA, moet u die gegevens opnemen in Platform. Er zijn verschillende manieren om dit te doen:

* Gebruik de Adobe Analytics Platform Connector als u bestaande Adobe Analytics-gegevens wilt opnemen.
* Als u andere gegevens wilt inbrengen, gebruikt u bestanden in de indeling .csv of Parquet naar


## Stap 1 a: Breng uw bestaande analysegegevens naar het Adobe Experience Platform

Gebruik de Adobe Analytics Platform Connector om traditionele analysegegevens over te brengen in Platform. U kunt één bronverbinding per rapportreeks tot stand brengen. Zie [Een bronverbinding maken met Adobe Analytics](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/sources_tutorial/adobe-analytics-ui-tutorial.md) in de documentatie van het Adobe Experience Platform.

Zodra de verbinding wordt gecreeerd, wordt een doelschema en een dataset automatisch gecreeerd om de inkomende gegevens te bevatten. Bovendien vindt de terugvulling van gegevens plaats en neemt deze tot 13 maanden aan historische gegevens in. Wanneer de aanvankelijke opname voltooit, kunt u met Stap x te werk gaan om een verbinding tussen deze dataset van Analytics en Analytics van de Reis van de Klant tot stand te brengen.

## Stap 1 b: Een schema maken




