---
title: Opzoekgegevenssets maken om gegevens in Customer Journey Analytics te classificeren
description: Leer hoe u opzoekgegevenssets maakt om gegevens in Customer Journey Analytics te classificeren
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: f5443ddd-81d0-43cc-99cb-215e7ddf5acf
source-git-commit: 03e9fb37684f8796a18a76dc0a93c4e14e6e7640
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 0%

---

# Opzoekgegevenssets maken om gegevens in Customer Journey Analytics te classificeren {#upgrade-lookup-dataset}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-lookup-dataset-create"
>title="Maak een opzoekgegevensset voor elke dimensie met classificatiegegevens"
>abstract="Net als classificatiegegevens in Adobe Analytics zijn opzoekgegevenssets de methode voor het classificeren van gegevens in Customer Journey Analytics."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

Net als classificatiegegevens in Adobe Analytics zijn opzoekgegevenssets de methode voor het classificeren van gegevens in Customer Journey Analytics.

Wanneer het gebruiken van de Bron van Analytics schakelaar, worden sommige standaardraadplegingsdatasets automatisch toegepast in rapporttijd. Voor meer informatie, zie [&#x200B; standaardraadplegingen aan uw datasets &#x200B;](/help/connections/standard-lookups.md) toevoegen.

Om gegevens in Customer Journey Analytics te classificeren wanneer het gebruiken van het Web SDK van Experience Platform, moet u een douaneschema en een raadplegingsdataset voor elke dimensie tot stand brengen die gegevens bevat die u wilt classificeren.

## Creeer een douaneschema om met de raadplegingsdataset te gebruiken

Maak een nieuw aangepast schema voor elke dimensie die gegevens bevat die u in Customer Journey Analytics wilt classificeren. Wanneer u de raadplegingsdataset in een recentere stap creeert, zal het naar dit schema verwijzen.

Herhaal dit proces voor elke dimensie die gegevens bevat die u wilt classificeren.

Een schema maken voor gebruik met een opzoekgegevensset in Customer Journey Analytics:

1. Selecteer in Adobe Experience Platform **[!UICONTROL Schemas]** in het gedeelte **[!UICONTROL Data Management]** in de linkertrack.

1. Selecteer **[!UICONTROL Create schema]** .

   ![&#x200B; creeer schemaknoop &#x200B;](assets/schema-create.png)

1. Selecteer **[!UICONTROL Manual]** . Zo kunt u handmatig velden en veldgroepen aan uw schema toevoegen. Kies **[!UICONTROL Select]** om door te gaan naar de volgende pagina van de wizard voor het maken van bestanden.

1. Selecteer op de pagina **[!UICONTROL Schema details]** eerst **[!UICONTROL Other]** en vervolgens **[!UICONTROL Custom]** .

   ![&#x200B; creeer douane &#x200B;](assets/schema-custom.png)

1. Selecteer **[!UICONTROL Create class]** .

   <!-- add screenshot -->

1. Geef in het dialoogvenster **[!UICONTROL Create class]** een naam en beschrijving voor het schema op, selecteer **[!UICONTROL Record]** en selecteer vervolgens **[!UICONTROL Create]** .

1. Ga met [&#x200B; verder creeer een raadplegingsdataset &#x200B;](#create-a-lookup-dataset).

## Een opzoekgegevensset maken

Nadat u [&#x200B; een douaneschema &#x200B;](#create-a-custom-schema-to-use-with-the-lookup-dataset) creeert om voor een raadplegingsdataset te gebruiken, moet u de raadplegingsdataset tot stand brengen en het in kaart brengen aan uw schema.

Herhaal dit proces voor elke dimensie die gegevens bevat die u wilt classificeren.

Een opzoekgegevensset maken voor gebruik met een schema in Customer Journey Analytics:

>[!NOTE]
>
>Het volgende proces gebruikt een Csv- dossier om de dataset tot stand te brengen. U kunt ook elke andere methode gebruiken die beschikbaar is voor het importeren van gegevens naar Experience Platform, zoals het instellen van een gegevensstroom.

1. Selecteer in Adobe Experience Platform **[!UICONTROL Workflows]** in de linkertrack.

   ![&#x200B; creeer douane &#x200B;](assets/lookup-dataset-workflows.png)

1. Selecteer **[!UICONTROL Map CSV to XDM schema]** en selecteer vervolgens **[!UICONTROL Launch]** .

1. Selecteer **[!UICONTROL New dataset]** in de sectie **[!UICONTROL Dataset details]** .

1. Geef een naam en een beschrijving voor de gegevensset op.

1. Op het **[!UICONTROL Schema]** gebied, selecteer het schema dat u voor raadplegingsdatasets creeerde, zoals die in [&#x200B; wordt beschreven creeer een schema voor raadplegingsdatasets &#x200B;](#create-a-schema-for-lookup-datasets).

1. Selecteer **[!UICONTROL Next]** .

1. Selecteer **[!UICONTROL Upload files]** in de sectie **[!UICONTROL Map CSV to XDM schema page]** de optie **[!UICONTROL Choose files]** en blader in het bestandssysteem naar het bestand dat de classificatiegegevens bevat voor de dimensie waarvoor u classificatiegegevens wilt toepassen. Dit kan bijvoorbeeld een spreadsheet zijn met de veld-id&#39;s en de bijbehorende veldnamen. <!-- correct? How can I better explain what this file is?-->

   ![&#x200B; Csv- dossier van de Kaart &#x200B;](assets/lookup-map-csv.png)

1. Selecteren **[!UICONTROL Next]**

1. Nadat het bestand is geüpload, controleert u de toewijzingen om na te gaan of ze correct zijn. De kolommen van het CSV-bestand worden weergegeven onder **[!UICONTROL Source Data]** en de bijbehorende XDM-schemavelden worden weergegeven onder **[!UICONTROL Target Field]** .

   Het platform verstrekt automatisch intelligente aanbevelingen voor auto-in kaart gebrachte gebieden die op het doelschema of de dataset worden gebaseerd dat u selecteerde. U kunt toewijzingsregels handmatig aanpassen aan uw gebruiksgevallen.

   Voor meer informatie over het toewijzingsproces, zie [&#x200B; een Csv- dossier aan een bestaand schema XDM &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/ingestion/tutorials/map-csv/existing-schema) in de documentatie van Experience Platform in kaart brengen.

1. Selecteer **[!UICONTROL Finish]** .

1. Ga met [&#x200B; verder toevoegen de raadplegingsdataset aan uw verbinding in Customer Journey Analytics &#x200B;](#add-the-lookup-dataset-to-your-connection-in-customer-journey-analytics).

## De opzoekgegevensset toevoegen aan uw verbinding in Customer Journey Analytics

Nadat u [&#x200B; een douaneschema &#x200B;](#create-a-custom-schema-to-use-with-the-lookup-dataset) creeert en u [&#x200B; een raadplegingsdataset &#x200B;](#create-a-lookup-dataset) creeert, moet u de raadplegingsdataset aan uw verbinding in Customer Journey Analytics toevoegen.

Herhaal dit proces voor elke dimensie die gegevens bevat die u wilt classificeren.

Om de raadplegingsdataset aan uw verbinding in Customer Journey Analytics toe te voegen:

1. Selecteer in Customer Journey Analytics **[!UICONTROL Connections]** (optioneel in **[!UICONTROL Data management]** ) in het bovenste menu.

1. Selecteer ![&#x200B; Meer pictogram &#x200B;](assets/More.svg) naast de verbinding waar u de raadplegingsdataset wilt toevoegen, dan selecteren **[!UICONTROL Edit]**.

   <!-- add screenshot -->

1. Selecteer **[!UICONTROL Add datasets]** .

1. Selecteer in het dialoogvenster **[!UICONTROL Add datasets]** de opzoekgegevensset die u hebt gemaakt en selecteer vervolgens **[!UICONTROL Next]** .

1. Selecteer in het veld **[!UICONTROL Person ID]** een persoon-id uit de beschikbare identiteiten die zijn gedefinieerd in het schema voor uw gegevensset dat u hebt geconfigureerd in Experience Platform. <!-- fill out other fields? -->

1. Selecteer **[!UICONTROL Add datasets]** en selecteer vervolgens **[!UICONTROL Save]** .

   <!-- is there a step right in between here where you select the dataset -->

1. Gebruikend het **[!UICONTROL Key]** gebied en het **[!UICONTROL Matching key]** gebied, creeer een correlatie tussen het gebied in uw raadplegingsdataset met dat in uw gebeurtenis of samenvattingsdataset.

1. Herhaal dit proces totdat alle opzoekgegevenssets zijn toegevoegd aan uw verbinding in Customer Journey Analytics.

{{upgrade-final-step}}

