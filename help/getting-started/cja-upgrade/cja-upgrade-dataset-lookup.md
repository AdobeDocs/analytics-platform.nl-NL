---
title: Opzoekgegevenssets maken om gegevens in Customer Journey Analytics te classificeren
description: Leer hoe te om raadplegingsdatasets te creëren om gegevens in Customer Journey Analytics te classificeren
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: f5443ddd-81d0-43cc-99cb-215e7ddf5acf
source-git-commit: 1e4c14334da54a5a6e4a0f36b3538c6e4d1a0b6f
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Opzoekgegevenssets maken om gegevens in Customer Journey Analytics te classificeren

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

Net als classificatiegegevens in Adobe Analytics zijn opzoekgegevenssets de methode voor het classificeren van gegevens in Customer Journey Analytics.

Wanneer het gebruiken van de Bron van Analytics schakelaar, worden sommige standaardraadplegingsdatasets automatisch toegepast in rapporttijd. Voor meer informatie, zie [ standaardraadplegingen aan uw datasets ](/help/connections/standard-lookups.md) toevoegen.

Om gegevens in Customer Journey Analytics te classificeren wanneer het gebruiken van het Web SDK van het Experience Platform, moet u een schema XDM en een raadplegingsdataset voor elke dimensie tot stand brengen die gegevens bevat die u wilt classificeren.

## Een XDM-schema maken

Creeer een nieuw schema XDM voor elke dimensie die gegevens bevat die u in Customer Journey Analytics wilt classificeren. Wanneer u de raadplegingsdataset in een recentere stap creeert, zal het naar dit schema verwijzen.

Herhaal dit proces voor elke dimensie die gegevens bevat die u wilt classificeren.

Om een schema voor gebruik met een raadplegingsdataset in Customer Journey Analytics tot stand te brengen:

1. Selecteer in Adobe Experience Platform **[!UICONTROL Schemas]** in het gedeelte **[!UICONTROL Data Management]** in de linkertrack.

1. Selecteer **[!UICONTROL Create schema]** .

   ![ creeer schemaknoop ](assets/schema-create.png)

1. Selecteer **[!UICONTROL Manual]** . Zo kunt u handmatig velden en veldgroepen aan uw schema toevoegen. Kies **[!UICONTROL Select]** om door te gaan naar de volgende pagina van de wizard voor het maken van bestanden.

1. Selecteer op de pagina **[!UICONTROL Schema details]** eerst **[!UICONTROL Other]** en vervolgens **[!UICONTROL Custom]** .

   ![ creeer douane ](assets/schema-custom.png)

1. Selecteer **[!UICONTROL Create class]** .

   <!-- add screenshot -->

1. Geef in het dialoogvenster **[!UICONTROL Create class]** een naam en beschrijving voor het schema op, selecteer **[!UICONTROL Record]** en selecteer vervolgens **[!UICONTROL Create]** .

1. Ga met [ verder creeer een raadplegingsdataset ](#create-a-lookup-dataset).

## Een opzoekgegevensset maken

Nadat u [ een schema XDM ](#create-an-xdm-schema-for-lookup-datasets) creeert om voor een raadplegingsdataset te gebruiken, moet u de raadplegingsdataset tot stand brengen en het in kaart brengen aan uw schema.

Herhaal dit proces voor elke dimensie die gegevens bevat die u wilt classificeren.

Om een raadplegingsdataset voor gebruik met een schema in Customer Journey Analytics tot stand te brengen:

>[!NOTE]
>
>Het volgende proces gebruikt een Csv- dossier om de dataset tot stand te brengen. U kunt ook elke andere methode gebruiken die beschikbaar is voor het importeren van gegevens naar een Experience Platform, zoals het instellen van een gegevensstroom.

1. Selecteer in Adobe Experience Platform **[!UICONTROL Workflows]** in de linkertrack.

   ![ creeer douane ](assets/lookup-dataset-workflows.png)

1. Selecteer **[!UICONTROL Map CSV to XDM schema]** en selecteer vervolgens **[!UICONTROL Launch]** .

1. Selecteer **[!UICONTROL New dataset]** in de sectie **[!UICONTROL Dataset details]** .

1. Geef een naam en een beschrijving voor de gegevensset op.

1. Op het **[!UICONTROL Schema]** gebied, selecteer het schema dat u voor raadplegingsdatasets creeerde, zoals die in [ wordt beschreven creeer een schema voor raadplegingsdatasets ](#create-a-schema-for-lookup-datasets).

1. Selecteer **[!UICONTROL Next]** .

1. Selecteer **[!UICONTROL Upload files]** in de sectie **[!UICONTROL Map CSV to XDM schema page]** de optie **[!UICONTROL Choose files]** en blader in het bestandssysteem naar het bestand dat de classificatiegegevens bevat voor de dimensie waarvoor u classificatiegegevens wilt toepassen. Dit kan bijvoorbeeld een spreadsheet zijn met de veld-id&#39;s en de bijbehorende veldnamen. <!-- correct? How can I better explain what this file is?-->

   ![ Csv- dossier van de Kaart ](assets/lookup-map-csv.png)

1. Selecteren **[!UICONTROL Next]**

1. Nadat het bestand is geüpload, controleert u de toewijzingen om na te gaan of ze correct zijn. De kolommen van het CSV-bestand worden weergegeven onder **[!UICONTROL Source Data]** en de bijbehorende XDM-schemavelden worden weergegeven onder **[!UICONTROL Target Field]** .

   Het platform verstrekt automatisch intelligente aanbevelingen voor auto-in kaart gebrachte gebieden die op het doelschema of de dataset worden gebaseerd dat u selecteerde. U kunt toewijzingsregels handmatig aanpassen aan uw gebruiksgevallen.

   Voor meer informatie over het toewijzingsproces, zie [ een Csv- dossier aan een bestaand schema XDM ](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/tutorials/map-csv/existing-schema) in de documentatie van het Experience Platform in kaart brengen.

1. Selecteer **[!UICONTROL Finish]** .

1. Ga met [ verder toevoegen de raadplegingsdataset aan uw verbinding in Customer Journey Analytics ](#add-the-lookup-dataset-to-your-connection-in-customer-journey-analytics).

## Voeg de raadplegingsdataset aan uw verbinding in Customer Journey Analytics toe

Nadat u [ een schema XDM ](#create-an-xdm-schema-for-lookup-datasets) creeert en [ een raadplegingsdataset ](#create-a-lookup-dataset) creeert, moet u de raadplegingsdataset aan uw verbinding in Customer Journey Analytics toevoegen.

Herhaal dit proces voor elke dimensie die gegevens bevat die u wilt classificeren.

Om de raadplegingsdataset aan uw verbinding in Customer Journey Analytics toe te voegen:

1. Selecteer in Customer Journey Analytics de tab **[!UICONTROL Connections]** .

1. Selecteer ![ Meer pictogram ](assets/More.svg) naast de verbinding waar u de raadplegingsdataset wilt toevoegen, dan selecteren **[!UICONTROL Edit]**.

   <!-- add screenshot -->

1. Selecteer **[!UICONTROL Add datasets]** .

1. Selecteer in het dialoogvenster **[!UICONTROL Add datasets]** de opzoekgegevensset die u hebt gemaakt en selecteer vervolgens **[!UICONTROL Next]** .

1. In het **[!UICONTROL Person ID]** gebied, selecteer een persoonsidentiteitskaart van de beschikbare identiteiten die in het uw datasetschema worden bepaald dat u in Experience Platform vormde. <!-- fill out other fields? -->

1. Selecteer **[!UICONTROL Add datasets]** en selecteer vervolgens **[!UICONTROL Save]** .

1. Gebruikend het **[!UICONTROL Key]** gebied en het **[!UICONTROL Matching key]** gebied, creeer een correlatie tussen het gebied in uw raadplegingsdataset met dat in uw gebeurtenis of samenvattingsdataset.

1. Nadat alle raadplegingsdatasets aan uw verbinding in Customer Journey Analytics worden toegevoegd, ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.

