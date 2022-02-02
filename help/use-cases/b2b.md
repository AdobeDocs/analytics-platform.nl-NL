---
title: (B2B) Gegevens op accountniveau toevoegen als een opzoekgegevensset
description: Leer hoe te om op rekening-gebaseerde gegevens als raadplegingsdataset aan CJA toe te voegen
exl-id: d345f680-b657-4b87-9560-a50fc59bb7a7
solution: Customer Journey Analytics
feature: Use Cases
source-git-commit: c36dddb31261a3a5e37be9c4566f5e7ec212f53c
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# (B2B) Gegevens op accountniveau toevoegen als een opzoekgegevensset

In deze B2B-gebruikscase ziet u hoe u uw gegevens op accountniveau kunt opgeven in plaats van op persoonlijke niveau voor analyse. Analyse op accountniveau kan vragen zoals

* Welke bedrijfsnaam wordt aangepast aan deze account?
* Hoeveel werknemers worden geassocieerd met dit rekening/bedrijf?
* Welke rollen worden in deze rekening vertegenwoordigd?
* Hoe presteert deze rekening als geheel met betrekking tot een specifieke marketingcampagne, in vergelijking met een andere rekening?
* Werken bepaalde rollen (zoals IT Manager) bij één account anders dan dezelfde rol bij een andere account?

U bereikt dit alles door de gegevens op accountniveau als een [opzoeken](/help/getting-started/cja-glossary.md) dataset.

U maakt eerst een opzoekschema in Adobe Experience Platform en maakt vervolgens een gegevensset van een opzoektabel door op .csv gebaseerde gegevens op accountniveau in te voeren. Dan gaat u te werk om een verbinding in Customer Journey Analytics (CJA0 tot stand te brengen die verschillende datasets, met inbegrip van de raadpleging combineert u creeerde. Vervolgens maakt u een gegevensweergave en ten slotte kunt u al deze gegevens gebruiken in Workspace.

>[!NOTE]
>
>Tabellen opzoeken kunnen een formaat hebben van maximaal 1 GB.

## 1. Opzoekschema maken (Experience Platform)

Uw eigen schema voor het [opzoeken](/help/getting-started/cja-glossary.md) de lijst zorgt ervoor dat de gebruikte dataset in CJA met de correcte opstelling (verslagtype) beschikbaar zal zijn. De beste praktijken zijn [een aangepaste schema-klasse maken](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#create-new-class) genoemd &quot;Opzoeken&quot;, leeg van om het even welk element, dat voor alle raadplegingslijsten kan worden opnieuw gebruikt.

![](assets/create-new-class.png)

## 2. Opzoekgegevensset maken (Experience Platform)

Zodra het schema is gecreeerd, moet u een raadplegingsdataset van dat schema, in Experience Platform tot stand brengen. Deze raadplegingsdataset bevat account-vlakke marketing informatie, zoals: de naam van het bedrijf, het totale aantal werknemers, de domeinnaam, de industrie waartoe zij behoren, de jaarlijkse opbrengst, of zij huidige klanten van de Experience Platform zijn of niet, welke verkoopfase zij binnen zijn, welk team binnen de rekening CJA gebruikt, enz.

>[!IMPORTANT]
>
>CJA steunt geen gehelen in raadplegingsdatasets. Als u de geheelgebieden in uw schema XDM voor uw raadplegingsdataset toevoegt, zult u niet die gehelen als metriek of berekende metriek kunnen gebruiken. Bijvoorbeeld, als annualRevenue of totalEmployees als gehelen worden gedefinieerd, zullen zij als &quot;0&quot;in rapportering in CJA tonen. Als u ze echter toewijst als tekenreeksen, kunt u ze als opzoekinformatie gebruiken.

Zo worden annualRevenue of totalEmployees in het volgende voorbeeld gedefinieerd als Geheel getal - dat is de reden waarom het &quot;0&quot;toont in CJA.

1. Ga in Adobe Experience Platform naar **[!UICONTROL Data Management > Datasets]**.
1. Klik op **[!UICONTROL + Create dataset]**.
1. Klik op **[!UICONTROL Create dataset from schema]**.
1. Selecteer de klasse Lookup Schema die u hebt gemaakt.
1. Klik op **[!UICONTROL Next]**.
1. Geef de gegevensset een naam (in ons voorbeeld B2B Info) en geef een beschrijving op.
1. Klik op **[!UICONTROL Finish]**.

## 3. Gegevens in Experience Platform opnemen

Instructies over hoe [Een CSV-bestand toewijzen aan een XDM-schema](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html) moet u helpen als u een CSV-bestand gebruikt.

[Andere methoden](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html) zijn ook beschikbaar.

Het aan boord nemen van de gegevens en het bepalen van de raadpleging duurt ongeveer 2 tot 4 uur, afhankelijk van de grootte van de raadplegingstabel.

## 4. Gegevenssets combineren in een verbinding (Customer Journey Analytics)

Voor dit voorbeeld, combineren wij 3 datasets in één verbinding CJA:

| Naam gegevensset | Beschrijving | AEP Schema, klasse | Gegevens over gegevensset |
| --- | --- | --- | --- |
| B2B-impressie | Bevat klikstroom, gebeurtenis-vlakke gegevens op het rekeningsniveau. Het bevat bijvoorbeeld de e-mail-id en de bijbehorende account-id en de marketingnaam voor marketingadvertenties. Het omvat ook de indrukkingen voor die advertenties, per gebruiker. | Gebaseerd op de XDM ExperienceEvent-schemaklasse | De `emailID` wordt gebruikt als primaire identiteit en toegewezen aan `Customer ID` naamruimte. Als gevolg hiervan wordt deze standaard weergegeven **[!UICONTROL Person ID]** in Customer Journey Analytics. ![Impressies](assets/impressions-mixins.png) |
| B2B-profiel | Deze profieldataset vertelt u meer over de gebruikers in een rekening, zoals hun baantitel, tot welke rekening zij behoren, hun profiel van LinkedIn, etc. | Gebaseerd op de XDM-klasse Individueel profielschema | U hoeft niet te selecteren `emailID` als primaire id in dit schema. Zorg ervoor dat u **[!UICONTROL Profile]**; Als u dat niet doet, kan CJA geen verbinding maken met de `emailID` in B2B-profiel met de `emailID` in B2B-indrukgegevens. ![Profiel](assets/profile-mixins.png) |
| B2B-info | Zie &quot;Opzoekgegevensset maken&quot; hierboven. | B2BAccount (aangepaste opzoekschema-klasse) | De relatie tussen `accountID` en de B2B dataset van de Impressies automatisch is gecreeerd door de B2B dataset van Info met de B2B dataset van de Impressie in CJA aan te sluiten, zoals die in de hieronder stappen wordt beschreven. ![Opzoeken](assets/lookup-mixins.png) |

Hier is hoe u de datasets combineert:

1. Selecteer in Customer Journey Analytics de **[!UICONTROL Connections]** tab.
1. Selecteer de datasets (in ons voorbeeld, de drie hierboven) u wilt combineren.
1. Voor de B2B gegevensreeks van Info selecteert `accountID` die in uw raadplegingslijst zal worden gebruikt. Selecteer vervolgens de overeenkomende sleutel (corresponderende dimensie), ook `accountID` in uw gebeurtenisdataset.
1. Klik op **[!UICONTROL Next]**.
1. Naam en beschrijf de verbinding en vorm het volgens [deze instructies](/help/connections/create-connection.md).
1. Klik op **[!UICONTROL Save]**.

## 5. Een gegevensweergave maken van deze verbinding

Volg de instructies op [gegevensweergaven maken](/help/data-views/create-dataview.md).

* Voeg alle componenten (afmetingen en metriek) toe die u van de datasets nodig hebt.

## 6. De gegevens in Workspace analyseren

U kunt de projecten van de Werkruimte nu tot stand brengen die op de gegevens van alle 3 datasets worden gebaseerd.

U vindt bijvoorbeeld antwoorden op de antwoorden in de inleiding:

* Verdeel de e-mailid op accountID om te bepalen tot welk bedrijf een e-mailid behoort.
* Hoeveel werknemers worden toegewezen aan een specifieke account-id?
* Tot welke branche behoort een account-id?

![](assets/project-lookup.png)
