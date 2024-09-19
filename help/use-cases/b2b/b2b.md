---
title: Accountgegevens toevoegen als een opzoekgegevensset
description: Leer hoe te om rekeningsgegevens als raadplegingsdataset aan Customer Journey Analytics toe te voegen
exl-id: d345f680-b657-4b87-9560-a50fc59bb7a7
solution: Customer Journey Analytics
feature: Use Cases
role: User
source-git-commit: cb47ac777958f6aaf26258d4aaed755b7657f36e
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Accountgegevens toevoegen als een opzoekgegevensset

Dit B2B-gebruiksgeval laat zien hoe u accountgegevens kunt toevoegen aan een analyse op persoonlijk niveau en op gebeurtenisniveau. Wanneer u accountgegevens toevoegt, kunt u vragen zoals:

* Welke bedrijfsnaam wordt aangepast aan deze account?
* Welke rollen worden in deze rekening vertegenwoordigd?
* Werken bepaalde rollen (zoals IT Manager) bij één account anders dan dezelfde rol bij een andere account?

Om de informatie van rekeningsgegevens toe te voegen, voegt u toe en gebruikt a [ raadpleging ](/help/technotes/glossary.md) dataset die deze informatie bevat.

Het gaat om de volgende stappen:

1. [ creeer een raadplegingsschema ](#create-lookup-schema) in Experience Platform.
1. [ creeer een raadplegingsdataset ](#create-lookup-dataset) in Experience Platform dat u toestaat om op CSV-Gebaseerde rekeningsgegevens in te voeren.
1. [ combineer datasets in een verbinding ](#combine-datasets-in-a-connection) in Customer Journey Analytics, met inbegrip van de raadpleging u creeerde.
1. [ creeer een gegevensmening ](#create-a-data-view-from-this-connection) in Customer Journey Analytics.
1. [ analyseer deze gegevens ](#analyze-the-data-in-workspace) in Workspace in Customer Journey Analytics.

>[!NOTE]
>
>Tabellen opzoeken kunnen een formaat hebben van maximaal 1 GB.
>

## Opzoekschema maken

Wanneer u uw eigen schema voor de [ raadplegings ](/help/technotes/glossary.md) lijst creeert, zorgt dat schema ervoor dat de gebruikte dataset in Customer Journey Analytics met de correcte opstelling (verslagtype) beschikbaar is. De beste praktijken moeten [ tot een klasse van het douaneschema ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui) leiden die voor alle raadplegingslijsten kan worden opnieuw gebruikt.

![ creeer Nieuwe dialoog van de Klasse.](../assets/create-new-class.png)

## Opzoekgegevensset maken

Zodra het schema wordt gecreeerd moet u een raadplegingsdataset tot stand brengen, die op dat schema, in Experience Platform wordt gebaseerd. Deze opgezochte dataset bevat de rekeningsinformatie. Bijvoorbeeld: bedrijfsnaam, totaal aantal werknemers, domeinnaam, tot welke industrie het bedrijf behoort, jaarlijkse opbrengst, en meer. Zorg ervoor dat de gegevens een persoon-id bevatten die kan worden gekoppeld aan de persoon-id die in de gebeurtenisgegevens wordt gebruikt.

1. Ga in Experience Platform naar **[!UICONTROL Data Management > Datasets]** .
1. Klik op **[!UICONTROL + Create dataset]**.
1. Klik op **[!UICONTROL Create dataset from schema]**.
1. Selecteer de klasse Lookup Schema die u hebt gemaakt.
1. Klik op **[!UICONTROL Next]**.
1. Geef de gegevensset een naam (bijvoorbeeld `B2B Info` ) en geef een beschrijving op.
1. Klik op **[!UICONTROL Finish]**.

## Samenvattingsgegevens

Instructies op hoe te [ een Csv- dossier aan een XDM- schema ](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/tutorials/map-csv/existing-schema) in kaart brengen zou moeten helpen als u een Csv- dossier gebruikt.

[ Andere methodes ](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/home) zijn ook beschikbaar.

Het aan boord nemen van de gegevens en het bepalen van de raadpleging duurt ongeveer 2 tot 4 uur, afhankelijk van de grootte van de raadplegingstabel.

## Gegevenssets combineren in een verbinding

Voor dit voorbeeld, combineert u 3 datasets in één verbinding van de Customer Journey Analytics:

| Naam gegevensset | Beschrijving | Adobe Experience Platform Schema, klasse | Gegevens over gegevensset |
| --- | --- | --- | --- |
| B2B-impressie | Bevat klikstroom, gebeurtenis-vlakke gegevens op het rekeningsniveau. Het bevat bijvoorbeeld de e-mail-id en de bijbehorende account-id en de marketingnaam voor marketingadvertenties. Het bevat ook de indrukkingen voor die advertenties per gebruiker. | Gebaseerd op de XDM ExperienceEvent-schemaklasse | `emailID` wordt gebruikt als primaire identiteit en toegewezen een `Customer ID` naamruimte. Dit betekent dat deze wordt weergegeven als de standaard **[!UICONTROL Person ID]** in Customer Journey Analytics. ![ Impressies ](../assets/impressions-mixins.png) |
| B2B-profiel | Deze profieldataset vertelt u meer over de gebruikers in een rekening, zoals hun baantitel, tot welke rekening zij behoren, hun profiel van LinkedIn, etc. | Gebaseerd op de XDM-klasse Individueel profielschema | Selecteer `emailID` als primaire id in dit schema. |
| B2B-info | Zie &quot;Opzoekgegevensset maken&quot; hierboven. | B2B-account (aangepaste opzoekschema-klasse) | De relatie tussen `accountID` en de B2B dataset van de Indrukking wordt automatisch gecreeerd wanneer u de B2B dataset van Info met de B2B dataset van de Indrukking in Customer Journey Analytics verbindt, zoals die in de hieronder stappen wordt beschreven. ![ Opzoeken ](../assets/lookup-mixins.png) |

Hier is hoe u de datasets combineert:

1. Selecteer in Customer Journey Analytics de tab **[!UICONTROL Connections]** .
1. Selecteer de gegevenssets die u wilt combineren.
1. Voor de B2B dataset van Info, selecteer de sleutel die in uw raadplegingstabel (bijvoorbeeld `personKey.sourceKey`) wordt gebruikt. Dan selecteer zijn passende sleutel (overeenkomstige afmeting), ook in uw gebeurtenisdataset (bijvoorbeeld p `ersonKey.sourceKey`).
1. Klik op **[!UICONTROL Next]**.
1. De naam en beschrijft de verbinding en vormt het volgens [ deze instructies ](/help/connections/create-connection.md).
1. Klik op **[!UICONTROL Save]**.

## Een gegevensweergave maken van deze verbinding

Volg de instructies op [ het creëren van gegevensmeningen ](/help/data-views/create-dataview.md).

* Voeg alle componenten (afmetingen en metriek) toe die u van de datasets nodig hebt. Zorg ervoor dat voor metriek die deduplicatie voor het overtellen vereisen, u deze metriek dienovereenkomstig (zie [ Metrische montages van de deduplicatiecomponent ](/help/data-views/component-settings/metric-deduplication.md)) vormt. Voorbeelden van dergelijke cijfers zijn het aantal werknemers of opbrengsten.

## De gegevens in Workspace analyseren

U kunt nu Workspace-projecten maken op basis van de gegevens van alle drie datasets.

U vindt bijvoorbeeld antwoorden op de antwoorden in de inleiding:

* Verdeel de e-mailid op accountID om te bepalen tot welk bedrijf een e-mailid behoort.
* Hoeveel werknemers worden toegewezen aan een specifieke account-id?
* Tot welke branche behoort een account-id?

>[!MORELIKETHIS]
>
>Zie [ een project van voorbeeld B2B ](example.md) voor meer details.

