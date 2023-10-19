---
description: Logboeken beheren voor bestaande exportbewerkingen
keywords: Analysis Workspace
title: Exportlogboeken beheren
feature: Components
exl-id: 6d676a0a-b117-421e-9a90-8c550f08d474
source-git-commit: b0eff3702ce92bab8a3d75bc07e1b33c168805c2
workflow-type: tm+mt
source-wordcount: '803'
ht-degree: 0%

---

# Exportlogboeken beheren

In exportlogboeken vindt u details over elke exportbewerking. Deze logbestanden worden gegenereerd wanneer Analysis Workspace-gegevens naar de cloud worden geëxporteerd. (Voor informatie over hoe gegevens naar de cloud kunnen worden geëxporteerd, raadpleegt u [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md).)

Voor geplande exportbewerkingen weerspiegelen logboeken de exportinstellingen zoals deze waren toen het logboek werd verzonden. Logbestanden kunnen niet worden verwijderd.

## Exportlogboeken weergeven

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Logboeken**] tab.

   ![Tabblad Logboeken exporteren](assets/export-logs-tab.png)

   De details voor elk logboek worden getoond in de beschikbare kolommen.

1. Voer een van de volgende handelingen uit:

   * [De kolommen aanpassen](#configure-columns) die worden weergegeven.

   * Selecteer de **Informatiepictogram** ![Informatiepictogram](assets/information-icon.png) naast de logboeknaam om de uitvoer te bekijken die met het logboek wordt geassocieerd.

   * Selecteer de **Exportpictogram bewerken** ![Informatiepictogram](assets/edit-export-icon.png) naast de logboeknaam om de uitvoer uit te geven die met het logboek wordt geassocieerd.

     Voor meer informatie over het bewerken van een exportbewerking raadpleegt u [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md).

## Filteren en zoeken naar logbestanden

Om informatie te vinden u nodig hebt, kunt u of de lijst van logboeken filtreren of naar een logboek zoeken.

### De lijst met logbestanden filteren

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Logboeken**] tab.

1. Selecteer de **Filter** pictogram.

   ![Filterinformatie](assets/export-log-filters.png)

   U kunt filteren op de volgende criteria:

   | Filter | Beschrijving |
   |---------|----------|
   | [!UICONTROL **Id exporteren**] | Geef de export-id op van het exportlogboek dat u wilt weergeven. |
   | [!UICONTROL **Accounttype**] | Het accounttype waaraan het logbestand is gekoppeld. De volgende accounttypen zijn beschikbaar: <ul><li>[!UICONTROL **AEP gegevenslandingszone**]</li><li>[!UICONTROL **Amazon S3 Role ARN**]</li><li>[!UICONTROL **Azure SAS**]</li><li>[!UICONTROL **Azure RBAC**]</li><li>[!UICONTROL **Google Cloud Platform**]</li><li>[!UICONTROL **Snowflake**]</li></ul>. |
   | [!UICONTROL **Status**] | De status van de uitvoer. De volgende statussen zijn beschikbaar: <ul><li>[!UICONTROL **In behandeling**]: Er is een specifieke instantie van een exportbewerking gestart, maar deze is nog niet voltooid.<p>Als u een exportbewerking met de status In behandeling opnieuw uitvoert, wordt het exportproces vertraagd.</p></li><li>[!UICONTROL **Voltooid**]: Een specifiek exemplaar van een exportbewerking is voltooid en is beschikbaar in de exportaccount.</li><li>[!UICONTROL **Mislukt**]<p>In verschillende situaties kan het exporteren mislukken. Houd de muisaanwijzer boven de status Mislukt om details over de fout weer te geven.<p>Voor meer informatie over mogelijke redenen voor een mislukking, zie [Problemen met mislukte exportbewerkingen oplossen](/help/components/exports/troubleshoot-exports.md).</p> |

   {style="table-layout:auto"}

### Logbestanden zoeken

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Logboeken**] tab.

1. In het onderzoeksgebied, begin het typen van om het even welke informatie verbonden aan het logboek u zoekt. U kunt naar gegevens uit om het even welke kolom zoeken beschikbaar in de lijst.

<!-- removed for MVP: Retry an export You can re-run the export associated with the selected log, using the data as it was on the day the log was originally exported. This is useful when selecting a log that show a failed export or when selecting a log that was accidentally deleted. 

Retrying an export that has a status of Pending will delay the export process.

This option is not available when selecting multiple logs. -->

<!-- 1. In Customer Journey Analytics, select [!UICONTROL **Components**] > [!UICONTROL **Exports**].

1. Select the [!UICONTROL **Logs**] tab, then select a log.

1. Select [!UICONTROL **Retry**]. -->

## Een exportbewerking bewerken

U kunt de export bewerken die aan een specifiek logboek is gekoppeld.

Deze optie is niet beschikbaar als u meerdere logbestanden selecteert.

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Logboeken**] tab.

1. Zoek het logboek dat is gekoppeld aan het exportbestand dat u wilt bewerken.

1. Selecteer de **Exporteren bewerken** pictogram ![pictogram exportlogboek](assets/export-icon.png) naast de lognaam.

   of

   Schakel het selectievakje naast het logbestand in en selecteer vervolgens [!UICONTROL **Exporteren bewerken**].

## Kolommen configureren

U kunt kolommen toevoegen aan of verwijderen uit de [!UICONTROL Logs] om te configureren welke informatie wordt weergegeven.

Selecteer een kolomkop om de logbestanden op die kolom te sorteren. Logbestanden worden standaard gesorteerd op de datum en tijd waarop het exporteren is gestart.

Om kolommen op te vormen [!UICONTROL Logs] tab:

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Logboeken**] tab.

1. Selecteer de **Tabel aanpassen** pictogram ![tabel aanpassen](assets/customize-table-icon.png) in de rechterbovenhoek van het [!UICONTROL Logs] pagina.

   De volgende kolommen zijn beschikbaar:

   | Beschikbare kolom | Beschrijving |
   |---------|----------|
   | Exportnaam | De naam van de exportbewerking. De gebruikers geven de uitvoer een naam wanneer zij tot hen leiden, zoals die in worden beschreven [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md). |
   | Id exporteren | De id wordt automatisch toegewezen aan de exportbewerking wanneer deze wordt gemaakt. <!-- True? --> |
   | Instantie-id | De id van de instantie Customer Journey Analytics. <!-- True? --> |
   | Naam gegevensweergave | De naam van de gegevensweergave die aan het exporteren is gekoppeld. Gebruikers kunnen de gegevensweergave selecteren wanneer ze de exportbewerking maken, zoals wordt beschreven in [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md). |
   | Aantal bestanden | Het aantal bestanden dat is opgenomen in de exportbewerking. |
   | Grootte | De grootte van de exportbewerking.<p>De bestandsgrootte wordt berekend met een basis van 1024, die soms wordt weergegeven als KIB en MIB. Als uw cloudprovider de grootte berekent met een basis van 1000, kan dit ertoe leiden dat de grootte die wordt weergegeven in uw cloudprovider enigszins afwijkt van de grootte die hier wordt weergegeven.</p> |
   | Locatie | De locatie op de account waar de gegevens zijn geëxporteerd. |
   | Account | De account waarin de gegevens zijn geëxporteerd. |
   | Status | De status van de uitvoer. Beschikbare statussen zijn [!UICONTROL Pending], [!UICONTROL Delivered], en [!UICONTROL Failed]. |
   | Datum van levering | De datum waarop de uitvoer heeft plaatsgevonden. |
   | Accounttype | Het type cloudaccount waarin de gegevens zijn geëxporteerd. Beschikbare accounttypen zijn [!UICONTROL Amazon S3 Role ARN], [!UICONTROL Google Cloud Platform], [!UICONTROL Azure SAS], [!UICONTROL Azure RBAC], [!UICONTROL Snowflake], en [!UICONTROL Adobe Experience Platform]. |
   | Aantal rijen | Het aantal rijen dat is opgenomen in de geëxporteerde tabel. |

   {style="table-layout:auto"}

1. Zorg ervoor dat alle kolommen die u wilt weergeven, zijn geselecteerd. Geselecteerde kolommen worden weergegeven op de [!UICONTROL Logs] pagina en de relevante informatie weergeven.

## Controlelogboeken weergeven

De uitvoer van volledige tabellen wordt ook bijgehouden in het dialoogvenster [Customer Journey Analytics auditlogs](/help/privacy/audit-log.md). <!-- Need to see what the Component Type for full-table export will be and add it here. Also, under "Event type captured by audit logs" there would be a new event type called "Full-table export". 4 actions would be "Create, Delete, Edit, Export" and "API_Request"? Also information about the locations. Probably have a different component for the location credentials.-->
