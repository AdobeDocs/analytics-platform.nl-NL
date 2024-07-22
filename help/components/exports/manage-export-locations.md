---
description: De exportlocatie van de cloud beheren waar Customer Journey Analytics-gegevens kunnen worden verzonden
keywords: Analysis Workspace
title: Locaties en accounts voor cloudexport beheren
feature: Components
exl-id: 8e82fe6f-99df-4360-8693-99692aac002b
role: User, Admin
source-git-commit: 8fc8e3e4057663bd4bdf38e41bb3129df442f749
workflow-type: tm+mt
source-wordcount: '1364'
ht-degree: 0%

---

# Locaties en accounts voor cloudexport beheren

U kunt de exportlocaties van de cloud weergeven, bewerken en verwijderen.

Voor informatie over hoe te om een nieuwe plaats tot stand te brengen, zie [ de plaatsen van de wolkenuitvoer ](/help/components/exports/cloud-export-locations.md) vormen.

## Filter- en zoeklocaties

Als u informatie wilt zoeken die u nodig hebt, kunt u de lijst met locaties filteren of naar een locatie zoeken.

### De lijst met locaties filteren

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **Plaatsen**] tabel.

1. Selecteer het **pictogram van de Filter**.

   <!-- add screenshot -->

   U kunt filteren op de volgende criteria:

   | Filter | Beschrijving |
   |---------|----------|
   | [!UICONTROL **Type van Plaats**]<!--should this be changed to Account type?--> | Het accounttype waaraan de locatie is gekoppeld. De volgende accounttypen kunnen beschikbaar zijn: <ul><li>[!UICONTROL **AEP Gegevens het Landing Zone**]</li><li>[!UICONTROL **Amazon S3 Rol ARN**]</li><li>[!UICONTROL **Azure SAS**]</li><li>[!UICONTROL **Azure RBAC**]</li><li>[!UICONTROL **Google Cloud Platform**]</li><li>[!UICONTROL **Snowflake**]</li></ul> |
   | [!UICONTROL **Rekening**] | De naam van de account waaraan de locatie is gekoppeld. |
   | [!UICONTROL **die door**] wordt gecreeerd | Het e-mailadres van de gebruiker die de locatie heeft gemaakt. |

   {style="table-layout:auto"}

### Zoeken naar locaties

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **Plaatsen**] tabel.

1. (Voorwaardelijk) als u een systeembeheerder bent, kunt u de [!UICONTROL **plaatsen van de Mening voor alle gebruikers**] optie toelaten om plaatsen te bekijken die door alle gebruikers in uw organisatie worden gecreeerd.

1. Typ in het zoekveld alle informatie die is gekoppeld aan de locatie waarnaar u zoekt. U kunt naar gegevens uit om het even welke kolom zoeken beschikbaar in de lijst.

## Locaties bewerken

Een locatie kan alleen worden bewerkt door de gebruiker die de locatie heeft gemaakt of door een systeembeheerder.

Een locatie bewerken:

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **Plaatsen**] tabel.

1. (Voorwaardelijk) als u een systeembeheerder bent, kunt u de [!UICONTROL **plaatsen van de Mening voor alle gebruikers**] optie toelaten om plaatsen te bekijken die door alle gebruikers in uw organisatie worden gecreeerd.

1. Selecteer de locatie die u wilt bewerken.

   ![ voert venster uit dat het lusje en de lijst van plaatsen toont.](assets/locations-edit.png)

1. Selecteer [!UICONTROL **uitgeven**].

1. Breng om het even welke gewenste veranderingen aan, dan uitgezocht [!UICONTROL **sparen**].

## Locaties verwijderen

Als u een locatie verwijdert, worden exportbewerkingen die gebruikmaken van de locatie ook verwijderd. Controleer het bevestigingsvenster bij het verwijderen om te controleren of er geen exportbewerkingen aan de locatie zijn gekoppeld.

Een locatie verwijderen:

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **Plaatsen**] tabel.

1. (Voorwaardelijk) als u een systeembeheerder bent, kunt u de [!UICONTROL **plaatsen van de Mening voor alle gebruikers**] optie toelaten om plaatsen te bekijken die door alle gebruikers in uw organisatie worden gecreeerd.

1. Selecteer een of meer locaties die u wilt verwijderen.

   ![ het venster van Uitvoer die het lusje en de lijst van plaatsen tonen ](assets/locations-edit.png)

1. Selecteer [!UICONTROL **Schrapping**].

   Het dialoogvenster Locatie verwijderen wordt weergegeven.

1. Controleer in het dialoogvenster Locatie verwijderen of de locatie niet is gekoppeld aan een exportbewerking voordat u het verwijderen bevestigt.

   ![ de bevestigingsdialoog van de Plaats van de Schrapping ](assets/delete-location-confirmation-dialog.png)

1. Selecteer [!UICONTROL **Schrapping**] opnieuw om te bevestigen.

## Accounts bewerken

Een account kan alleen worden bewerkt door de gebruiker die het heeft gemaakt of door een systeembeheerder.

Een account bewerken:

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **rekeningen van de Plaats**] tabel.

   ![ het venster van Uitvoer het tonen van de rekeningen tabel van de Plaats ](assets/account-add.png)

1. (Voorwaardelijk) als u een systeembeheerder bent, kunt u de [!UICONTROL **rekeningen van de Mening voor alle gebruikers**] optie toelaten om plaatsen te bekijken die door alle gebruikers in uw organisatie worden gecreeerd.

1. Selecteer [!UICONTROL **details van de Mening**] op de rekening die u wilt uitgeven.

1. Breng om het even welke gewenste veranderingen aan, dan uitgezocht [!UICONTROL **sparen**].

## Accountsleutels weergeven

Nadat u een account hebt gemaakt, kunt u de accountsleutels voor dat account bekijken. U zou deze informatie kunnen moeten bekijken als u niet klaar was met het vormen van de rekening met uw wolkenleverancier [ toen u oorspronkelijk de rekening ](/help/components/exports/cloud-export-accounts.md) vormde.

Aan menings sleutels verbonden aan een de uitvoerrekening:

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **rekeningen van de Plaats**] tabel.

   ![ het venster van Uitvoer het tonen van de rekeningen tabel van de Plaats ](assets/account-add.png)

1. (Voorwaardelijk) als u een systeembeheerder bent, kunt u de [!UICONTROL **rekeningen van de Mening voor alle gebruikers**] optie toelaten om plaatsen te bekijken die door alle gebruikers in uw organisatie worden gecreeerd.

1. Selecteer het pictogram met drie punten op de rekening die u wilt uitgeven, dan selecteren [!UICONTROL **sleutels van de Rekening**].

## Accounts verwijderen

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **rekeningen van de Plaats**] tabel.

   ![ het venster van Uitvoer het tonen van de rekeningen tabel van de Plaats ](assets/account-add.png)

1. (Voorwaardelijk) als u een systeembeheerder bent, kunt u de [!UICONTROL **rekeningen van de Mening voor alle gebruikers**] optie toelaten om plaatsen te bekijken die door alle gebruikers in uw organisatie worden gecreeerd.

1. Selecteer het 3 puntpictogram op de rekening die u wilt uitgeven, dan selecteren [!UICONTROL **rekening van de Schrapping**].

1. Selecteer [!UICONTROL **Schrapping**] opnieuw op de bevestigingsdialoog.

## Bedrijfsbrede instellingen configureren (alleen beheerders)

Systeembeheerders kunnen gebruikers beperken bij het maken van accounts en locaties, of ze kunnen de typen accounts beperken die gebruikers kunnen maken en gebruiken.

![ Admin montages tabel ](assets/locations-admin-settings.png)

### Configureren of gebruikers accounts kunnen maken en bewerken

Door gebrek, kunnen alle gebruikers in de organisatie rekeningen tot stand brengen en rekeningen uitgeven die zij in uw milieu van de Customer Journey Analytics creëren, zoals die in [ wordt beschreven vormen wolkenuitvoerrekeningen ](/help/components/exports/cloud-export-accounts.md).

U kunt voorkomen dat gebruikers accounts maken. Wanneer u dat doet, kunnen gebruikers nog steeds accounts gebruiken die ze al hebben gemaakt, maar ze kunnen ze niet meer bewerken. U kunt rekeningen schrappen die de gebruikers hebben gecreeerd, zoals die in [ wordt beschreven een rekening ](#delete-an-account) schrappen.

Alle gebruikers beperken in het maken en bewerken van accounts:

1. In Customer Journey Analytics, selecteer **[!UICONTROL Components]** > **[!UICONTROL Exports]**, dan selecteren de [!UICONTROL **montages Admin**] tabel.

1. In de [!UICONTROL **rekeningen van Plaatsen**] sectie, schrap de optie, [!UICONTROL **staat gebruikers toe om plaatsrekeningen**] tot stand te brengen en te beheren.

1. Selecteer [!UICONTROL **sparen**].

1. (Facultatief) Schrap om het even welke rekeningen die de gebruikers hebben gecreeerd die u hen niet meer wilt gebruiken, zoals die in [ wordt beschreven een rekening ](#delete-an-account) schrappen.

### Configureren of gebruikers locaties kunnen maken en bewerken

Door gebrek, kunnen alle gebruikers in de organisatie plaatsen tot stand brengen en plaatsen uitgeven zij in uw milieu van de Customer Journey Analytics creëren, zoals die in [ wordt beschreven vormen de plaatsen van de wolkenuitvoer ](/help/components/exports/cloud-export-locations.md).

U kunt voorkomen dat gebruikers locaties maken. Wanneer u dat doet, kunnen gebruikers nog steeds alle locaties gebruiken die ze al hebben gemaakt, maar kunnen ze ze niet meer bewerken. U kunt plaatsen schrappen die de gebruikers hebben gecreeerd, zoals die in [ worden beschreven plaats van de Schrapping ](#delete-a-location).

Alle gebruikers beperken van het maken en bewerken van locaties:

1. In Customer Journey Analytics, selecteer **[!UICONTROL Components]** > **[!UICONTROL Eports]**, dan selecteren de [!UICONTROL **montages Admin**] tabel.

1. In de [!UICONTROL **sectie van Plaats**], schrap de optie, [!UICONTROL **staat gebruikers toe om plaatsen**] tot stand te brengen en te leiden.

1. Selecteer [!UICONTROL **sparen**].

1. (Facultatief) Schrap om het even welke plaatsen die de gebruikers hebben gecreeerd die u hen niet meer wilt gebruiken, zoals die in [ wordt beschreven Schrap een plaats ](#delete-a-location).

### Beperken welke accounttypen gebruikers kunnen maken en gebruiken

U kunt de accounttypen beperken die gebruikers zien in de volgende omstandigheden:

* Wanneer [ het creëren van nieuwe rekeningen ](/help/components/exports/cloud-export-accounts.md).
* Wanneer het kiezen van welke rekeningen te gebruiken wanneer het uitvoeren van dossiers gebruikend [ volledige lijstuitvoer ](/help/analysis-workspace/export/export-cloud.md).

Wanneer u accounttypen beperkt zoals beschreven in deze sectie, zijn accounts van het type dat u beperkt, niet meer zichtbaar voor gebruikers. Dit betekent dat er geen nieuwe accounts van dat type kunnen worden gemaakt en dat bestaande accounts van dat type niet kunnen worden gebruikt bij het exporteren van bestanden die gebruikmaken van volledige tabelexport.

Nochtans, moeten de bestaande rekeningen die voor geplande uitvoer worden gevormd worden geschrapt als u hen wilt beperken worden gebruikt.

#### Zorg ervoor dat accounts niet worden gebruikt voor geplande exportbewerkingen

Wanneer u accounttypen beperkt, worden bestaande accounts verborgen en niet verwijderd.

Als de programma&#39;s reeds worden gevormd om gegevens naar een rekening te verzenden die van het type is dat u beperkt, zullen de programma&#39;s blijven lopen zelfs nadat u het accounttype beperkt, en de gegevens zullen blijven worden verzonden naar de rekening. Als bijvoorbeeld een volledige tabelexport gepland is om gegevens naar een accounttype te verzenden dat u beperkt, gaat het programma door.

Als u moet ervoor zorgen dat de rekeningen van een bepaald type niet in geplande uitvoer worden gebruikt, kunt u de rekeningen schrappen alvorens u [ de accounttypes ](#limit-the-account-types-that-are-available-to-users) beperkt.

Accounts verwijderen:

1. Zoek de accounts van het accounttype dat u wilt beperken. Deze worden gebruikt voor geplande exportbewerkingen.

1. Schrap de rekeningen, zoals die in [ worden beschreven Schrap een rekening ](#delete-an-account).

1. Ga met de volgende sectie verder, [ Beperk de rekeningstypes die aan gebruikers ](#limit-the-account-types-that-are-available-to-users) beschikbaar zijn.

#### De accounttypen beperken die beschikbaar zijn voor gebruikers

U kunt als volgt de accounttypen beperken die beschikbaar zijn voor gebruikers bij het maken en gebruiken van accounts:

1. In Customer Journey Analytics, selecteer **[!UICONTROL Components]** > **[!UICONTROL Exports]**, dan selecteren de [!UICONTROL **montages Admin**] tabel.

1. Bepaal de plaats van [!UICONTROL **Toegelaten accounttypes**] sectie.

   De volgende accounttypen zijn standaard beschikbaar voor gebruikers. Schakel een van deze accounttypen uit die u gebruikers wilt beperken.

   * [!UICONTROL **AEP Gegevens het Landing Zone**]

   * [!UICONTROL **Amazon S3 Rol ARN**]

   * [!UICONTROL **Google Cloud Platform**]

   * [!UICONTROL **Azure SAS**]

   * [!UICONTROL **Azure RBAC**]

   * [!UICONTROL **Snowflake**]

1. Selecteer [!UICONTROL **sparen**].
