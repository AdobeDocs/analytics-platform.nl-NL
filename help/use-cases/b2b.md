---
title: (B2B) voeg rekening-vlakke gegevens als raadplegingsdataset toe
description: Leer hoe te om op rekening-gebaseerde gegevens als raadplegingsdataset aan CJA toe te voegen
translation-type: tm+mt
source-git-commit: de5717d42fbe29554351a789cce594ac9ad47ee1
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---


# (B2B) voeg rekening-vlakke gegevens als raadplegingsdataset toe

Dit B2B-gebruiksgeval toont u hoe u uw gegevens kunt opgeven op accountniveau in plaats van op persoonlijke niveau voor analyse. De rekening-vlakke analyse kan vragen zoals beantwoorden

* Welke bedrijfsnaam wordt aangepast aan deze account?
* Hoeveel werknemers worden geassocieerd met deze rekening/bedrijf?
* Welke rollen worden vertegenwoordigd in deze rekening?
* Hoe presteert deze rekening als geheel met betrekking tot een specifieke marketingcampagne, in vergelijking met een andere rekening?
* Worden bepaalde rollen (zoals de Manager van IT) bij één rekening zich verschillend gedraagt dan de zelfde rol bij een verschillende rekening?

U verwezenlijkt dit alles door de rekening-vlakke informatie als a in te brengen [raadpleging](/help/getting-started/cja-glossary.md) dataset (gelijkend op classificaties in traditionele Analytics van Adobe).

U creeert eerst een raadplegingsschema in het Platform van de Ervaring van Adobe, dan creeer een gegevens van de raadplegingslijst door op .csv-Gebaseerde rekening-vlakke gegevens in te nemen. Dan gaat u te werk om een verbinding CJA tot stand te brengen die verschillende datasets, met inbegrip van de raadpleging combineert u creeerde. U creeert dan een gegevensmening en kunt tenslotte al dit gegeven in Werkruimte gebruiken.

>[!NOTE]
>
>De lijsten van de Raadpleging kunnen tot 1 GB in grootte zijn.

## 1. Creeer raadplegingsschema (het Platform van de Ervaring)

Het creëren van uw eigen schema voor [raadpleging](/help/getting-started/cja-glossary.md) de lijst zorgt ervoor dat de gebruikte dataset in CJA met de correcte opstelling (verslagtype) beschikbaar zal zijn. De beste praktijken moeten [een aangepaste schemaklasse maken](https://docs.adobe.com/content/help/en/experience-platform/xdm/tutorials/create-schema-ui.html#create-new-class) geroepen &quot;Raadpleging&quot;, leeg van om het even welk element, dat voor alle raadplegingslijsten kan worden opnieuw gebruikt.

![](assets/create-new-class.png)

## 2. Maak de set raadplegingsgegevens (het platform van de Ervaring)

Zodra het schema is gecreeerd, moet u een raadplegingsdataset van dat schema, in het Platform van de Ervaring tot stand brengen. Deze raadplegingsdataset bevat rekening-vlakke marketing informatie, zoals: de bedrijfsnaam, het totale aantal werknemers, domeinnaam, welke industrie zij tot, jaarlijkse opbrengst behoren, of zij huidige klanten van het Platform van de Ervaring of niet zijn, welke verkoopstadium zij binnen zijn, welk team binnen de rekening CJA gebruikt, enz.

>[!IMPORTANT]
>
>CJA steunt geen gehelen in raadplegingsdatasets. Als u de geheelgebieden in uw schema XDM voor uw raadplegingsdataset toevoegt, zult u niet die gehelen als metriek of berekende metriek kunnen gebruiken. Bijvoorbeeld, als annualRevenue of totalEmployees als gehelen worden gedefinieerd, zullen zij als &quot;0&quot;in rapportering in CJA tonen. Nochtans, als u hen als koorden toewijst, kunt u hen als raadplegingsinformatie gebruiken.

Bijvoorbeeld, wordt annualRevenue of totalEmployees gedefinieerd als Geheel in het volgende voorbeeld, dat is de reden, zijn tonend &quot;0&quot;in CJA.

1. In het Platform van de Ervaring van Adobe, ga naar **[!UICONTROL Data Management > Datasets]**.
1. Klik op **[!UICONTROL + Create dataset]**.
1. Klik op **[!UICONTROL Create dataset from schema]**.
1. Selecteer de klasse van het Schema van de Raadpleging u creeerde.
1. Klik op **[!UICONTROL Next]**.
1. Noem de dataset (in ons voorbeeld, B2B Info) en verstrek een beschrijving.
1. Klik op **[!UICONTROL Finish]**.

## 3. Verzamel gegevens in het ervaringsplatform

Instructies over hoe te [Een CSV-bestand toewijzen aan een XDM-schema](https://docs.adobe.com/content/help/en/experience-platform/ingestion/tutorials/map-a-csv-file.html) moet u helpen als u een CSV-bestand gebruikt.

[Andere methoden](https://docs.adobe.com/content/help/en/experience-platform/ingestion/home.html) zijn ook beschikbaar.

Het aan boord gaan van de gegevens en het vestigen van de raadpleging nemen ongeveer 2 tot 4 uur, afhankelijk van de grootte van de raadplegingslijst.

## 4. Gegevensreeksen combineren in een verbinding (Analyse van de Reis van de Klant)

Bijvoorbeeld, combineren wij 3 datasets in één verbinding CJA:

| Naam dataset | Beschrijving | AEP Schema klasse | Gegevens over gegevensverzameling |
|---|---|---|---|
| B2B-onderdruk | Bevat klikstroom, gebeurtenis-vlakke gegevens op het rekeningsniveau. Bijvoorbeeld, bevat het e-mailidentiteitskaart en overeenkomstige rekeningsidentiteitskaart, evenals de marketing naam, voor het runnen van marketing advertenties. Het omvat ook de indrukken voor die advertenties, per gebruiker. | Gebaseerd op XDM ExperienceEvent schemaklasse | De `emailID` wordt gebruikt als primaire identiteit en toegewezen aan een `Customer ID` naamruimte. Dientengevolge, zal het als gebrek verschijnen **[!UICONTROL Person ID]** in Klantreisanalyse. ![Impressie](assets/impressions-mixins.png) |
| B2B-profiel | Deze profieldataset vertelt u meer over de gebruikers in een rekening, zoals hun baantitel, welke rekening zij tot, hun profiel LinkedIn, enz. behoren. | Gebaseerd op XDM Individuele het schemaklasse van het Profiel | Geen behoefte te selecteren `emailID` als primaire identiteitskaart in dit schema. Zorg ervoor om toe te laten **[!UICONTROL Profile]**; Als u niet, zal CJA niet kunnen verbinden `emailID` in B2B-profiel met `emailID` in B2B-onderdrukkingsgegevens. (Dit vermogen wordt genoemd op gebied-gebaseerd stikken.) ![Profiel](assets/profile-mixins.png) |
| B2B-gegevens | Zie &quot;hierboven reeks raadplegingsgegevens maken&quot;. | B2BAccount (klasse aangepast raadplegingsschema) | De relatie tussen `accountID` en de B2B dataset van Impressies is automatisch gecreeerd door de B2B dataset van Info met de B2B dataset van de Impressie in CJA, zoals die in de hieronder stappen wordt beschreven te verbinden. ![Zoeken](assets/lookup-mixins.png) |

Hier is hoe u de datasets combineert:

1. In de Analyse van de Reis van de Klant, selecteer **[!UICONTROL Connections]** tabblad
1. Selecteer de datasets (in ons voorbeeld, de drie hierboven) u wilt combineren.
1. Voor de B2B dataset van Info, selecteer `accountID` sleutel die in uw raadplegingslijst zal worden gebruikt. Dan selecteer zijn passende sleutel (overeenkomstige afmeting), ook `accountID` in uw gebeurtenisdataset.
1. Klik op **[!UICONTROL Next]**.
1. De naam en beschrijft de verbinding en vormt het volgens [deze instructies](/help/connections/create-connection.md).
1. Klik op **[!UICONTROL Save]**.

## 5. Creeer een gegevensmening van deze verbinding

Volg de instructies op [gegevensweergaven maken](/help/data-views/create-dataview.md).

* Voeg alle componenten (afmetingen en metriek) toe die u van de datasets nodig hebt.

## 6. Analyseer de gegevens in Werkruimte

U kunt de projecten van de Werkruimte nu tot stand brengen die op de gegevens van alle 3 datasets worden gebaseerd.

Bijvoorbeeld, kunt u antwoorden op de antwoorden vinden die in de inleiding worden gesteld:

* Onderdeel de e-mailID door accountID om uit te zoeken tot welk bedrijf een e-mailid behoort.
* Hoeveel werknemers worden in kaart gebracht aan een specifieke rekeningsidentiteitskaart
* Aan welke branche hoort een account-id thuis?

![](assets/project-lookup.png)
