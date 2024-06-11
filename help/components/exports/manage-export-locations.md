---
description: De exportlocatie van de cloud beheren waar Customer Journey Analytics-gegevens kunnen worden verzonden
keywords: Analysis Workspace
title: Locaties en accounts voor cloudexport beheren
feature: Components
exl-id: 8e82fe6f-99df-4360-8693-99692aac002b
role: User, Admin
source-git-commit: 6e36885cfba60c808b9f069159670db6834fe41f
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# Locaties en accounts voor cloudexport beheren

U kunt de exportlocaties van de cloud weergeven, bewerken en verwijderen.

Voor informatie over het maken van een nieuwe locatie raadpleegt u [Cloudexportlocaties configureren](/help/components/exports/cloud-export-locations.md).

## Filter- en zoeklocaties

Als u informatie wilt zoeken die u nodig hebt, kunt u de lijst met locaties filteren of naar een locatie zoeken.

### De lijst met locaties filteren

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Locaties**] tab.

1. Selecteer de **Filter** pictogram.

   <!-- add screenshot -->

   U kunt filteren op de volgende criteria:

   | Filter | Beschrijving |
   |---------|----------|
   | [!UICONTROL **Type locatie**]<!--should this be changed to Account type?--> | Het accounttype waaraan de locatie is gekoppeld. De volgende accounttypen kunnen beschikbaar zijn: <ul><li>[!UICONTROL **AEP gegevenslandingszone**]</li><li>[!UICONTROL **Amazon S3 Role ARN**]</li><li>[!UICONTROL **Azure SAS**]</li><li>[!UICONTROL **Azure RBAC**]</li><li>[!UICONTROL **Google Cloud Platform**]</li><li>[!UICONTROL **Snowflake**]</li></ul> |
   | [!UICONTROL **Account**] | De naam van de account waaraan de locatie is gekoppeld. |
   | [!UICONTROL **Gemaakt door**] | Het e-mailadres van de gebruiker die de locatie heeft gemaakt. |

   {style="table-layout:auto"}

### Zoeken naar locaties

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Locaties**] tab.

1. (Voorwaardelijk) Als u een systeembeheerder bent, kunt u de [!UICONTROL **Locaties voor alle gebruikers weergeven**] om locaties weer te geven die door alle gebruikers in uw organisatie zijn gemaakt.

1. Typ in het zoekveld alle informatie die is gekoppeld aan de locatie waarnaar u zoekt. U kunt naar gegevens uit om het even welke kolom zoeken beschikbaar in de lijst.

## Locaties bewerken

Een locatie kan alleen worden bewerkt door de gebruiker die de locatie heeft gemaakt of door een systeembeheerder.

Een locatie bewerken:

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Locaties**] tab.

1. (Voorwaardelijk) Als u een systeembeheerder bent, kunt u de [!UICONTROL **Locaties voor alle gebruikers weergeven**] om locaties weer te geven die door alle gebruikers in uw organisatie zijn gemaakt.

1. Selecteer de locatie die u wilt bewerken.

   ![Exporteert het venster met het tabblad Locaties en de lijst met locaties.](assets/locations-edit.png)

1. Selecteren [!UICONTROL **Bewerken**].

1. Breng de gewenste wijzigingen aan en selecteer vervolgens [!UICONTROL **Opslaan**].

## Locaties verwijderen

Als u een locatie verwijdert, worden exportbewerkingen die gebruikmaken van de locatie ook verwijderd. Controleer het bevestigingsvenster bij het verwijderen om te controleren of er geen exportbewerkingen aan de locatie zijn gekoppeld.

Een locatie verwijderen:

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Locaties**] tab.

1. (Voorwaardelijk) Als u een systeembeheerder bent, kunt u de [!UICONTROL **Locaties voor alle gebruikers weergeven**] om locaties weer te geven die door alle gebruikers in uw organisatie zijn gemaakt.

1. Selecteer een of meer locaties die u wilt verwijderen.

   ![Exporteert een venster met het tabblad Locaties en een lijst met locaties](assets/locations-edit.png)

1. Selecteren [!UICONTROL **Verwijderen**].

   Het dialoogvenster Locatie verwijderen wordt weergegeven.

1. Controleer in het dialoogvenster Locatie verwijderen of de locatie niet is gekoppeld aan een exportbewerking voordat u het verwijderen bevestigt.

   ![Dialoogvenster Locatie bevestigen verwijderen](assets/delete-location-confirmation-dialog.png)

1. Selecteren [!UICONTROL **Verwijderen**] nogmaals ter bevestiging.

## Accounts bewerken

Een account kan alleen worden bewerkt door de gebruiker die het heeft gemaakt of door een systeembeheerder.

Een account bewerken:

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Locatieaccounts**] tab.

   ![Exporteert venster met het tabblad Locatierekeningen](assets/account-add.png)

1. (Voorwaardelijk) Als u een systeembeheerder bent, kunt u de [!UICONTROL **Accounts weergeven voor alle gebruikers**] om locaties weer te geven die door alle gebruikers in uw organisatie zijn gemaakt.

1. Selecteren [!UICONTROL **Details weergeven**] op de account die u wilt bewerken.

1. Breng de gewenste wijzigingen aan en selecteer vervolgens [!UICONTROL **Opslaan**].

## Accountsleutels weergeven

Nadat u een account hebt gemaakt, kunt u de accountsleutels voor dat account bekijken. Mogelijk moet u deze informatie weergeven als u de account niet hebt geconfigureerd bij uw cloud provider [toen u oorspronkelijk de rekening vormde](/help/components/exports/cloud-export-accounts.md).

Aan menings sleutels verbonden aan een de uitvoerrekening:

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Locatieaccounts**] tab.

   ![Exporteert venster met het tabblad Locatierekeningen](assets/account-add.png)

1. (Voorwaardelijk) Als u een systeembeheerder bent, kunt u de [!UICONTROL **Accounts weergeven voor alle gebruikers**] om locaties weer te geven die door alle gebruikers in uw organisatie zijn gemaakt.

1. Selecteer het pictogram met drie punten op de account die u wilt bewerken en selecteer vervolgens [!UICONTROL **Accountsleutels**].

## Accounts verwijderen

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Locatieaccounts**] tab.

   ![Exporteert venster met het tabblad Locatierekeningen](assets/account-add.png)

1. (Voorwaardelijk) Als u een systeembeheerder bent, kunt u de [!UICONTROL **Accounts weergeven voor alle gebruikers**] om locaties weer te geven die door alle gebruikers in uw organisatie zijn gemaakt.

1. Selecteer het pictogram met drie punten op de account die u wilt bewerken en selecteer vervolgens [!UICONTROL **Account verwijderen**].

1. Selecteren [!UICONTROL **Verwijderen**] nogmaals in het bevestigingsvenster.
