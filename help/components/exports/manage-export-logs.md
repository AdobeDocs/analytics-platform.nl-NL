---
description: Logboeken beheren voor bestaande exportbewerkingen
keywords: Analysis Workspace
title: Exportlogboeken beheren
feature: Components
exl-id: 6d676a0a-b117-421e-9a90-8c550f08d474
role: User
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# Exportlogboeken beheren

In exportlogboeken vindt u details over elke exportbewerking. Deze logbestanden worden gegenereerd wanneer Analysis Workspace-gegevens naar de cloud worden geëxporteerd. (Voor informatie over hoe de gegevens naar de wolk kunnen worden uitgevoerd, zie {de rapporten van Customer Journey Analytics van 0} de Uitvoer naar de wolk [.)](/help/analysis-workspace/export/export-cloud.md)

Voor geplande exportbewerkingen weerspiegelen logboeken de exportinstellingen zoals deze waren toen het logboek werd verzonden. Logbestanden kunnen niet worden verwijderd.

## Exportlogboeken weergeven

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **Logboeken**] tabel.

   ![ venster van de Uitvoer die de Logs tabel tonen ](assets/export-logs-tab.png)

   De details voor elk logboek worden getoond in de beschikbare kolommen.

1. Voer een van de volgende handelingen uit:

   * [ pas de kolommen ](#configure-columns) aan die worden getoond.

   * Selecteer het **pictogram van de Informatie** ![ pictogram van de Informatie ](assets/information-icon.png) naast de logboeknaam om de uitvoer te bekijken die met het logboek wordt geassocieerd.

   * Selecteer het **uitgeven uitvoerpictogram** ![ pictogram van de Informatie ](assets/edit-export-icon.png) naast de logboeknaam om de uitvoer uit te geven die met het logboek wordt geassocieerd.

     Voor meer informatie over het uitgeven van een uitvoer, zie [ de rapporten van Customer Journey Analytics van de Uitvoer aan de wolk ](/help/analysis-workspace/export/export-cloud.md).

## Filteren en zoeken naar logbestanden

Om informatie te vinden u nodig hebt, kunt u of de lijst van logboeken filtreren of naar een logboek zoeken.

### De lijst met logbestanden filteren

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **Logboeken**] tabel.

1. Selecteer het **pictogram van de Filter**.

   ![ voert venster uit dat de lijst van de Filter door het type van Rekening toont ](assets/export-log-filters.png)

   U kunt filteren op de volgende criteria:

   | Filter | Beschrijving |
   |---------|----------|
   | [!UICONTROL **identiteitskaart van de Uitvoer**] | Geef de export-id op van het exportlogboek dat u wilt weergeven. |
   | [!UICONTROL **Type van Rekening**] | Het accounttype waaraan het logbestand is gekoppeld. De volgende accounttypen zijn beschikbaar: <ul><li>[!UICONTROL **AEP Gegevens die Zone**] aanvoeren</li><li>[!UICONTROL **Amazon S3 Rol ARN**]</li><li>[!UICONTROL **Azure SAS**]</li><li>[!UICONTROL **Azure RBAC**]</li><li>[!UICONTROL **Google Cloud Platform**]</li><li>[!UICONTROL **Snowflake**]</li></ul>. |
   | [!UICONTROL **Status**] | De status van de uitvoer. De volgende statussen zijn beschikbaar: <ul><li>[!UICONTROL **Hangende**]: Een specifiek geval van de uitvoer is begonnen maar is nog niet volledig.<p>Als u een exportbewerking met de status In behandeling opnieuw uitvoert, wordt het exportproces vertraagd.</p></li><li>[!UICONTROL **Voltooid**]: Een specifiek geval van de uitvoer heeft verwerking gebeëindigd en is beschikbaar in de uitvoerrekening.</li><li>[!UICONTROL **Ontbroken**]<p>In verschillende situaties kan het exporteren mislukken. Houd de muisaanwijzer boven de status Mislukt om details over de fout weer te geven.<p>Voor meer informatie over mogelijke redenen voor een mislukking, zie [ ontbroken uitvoer ](/help/components/exports/troubleshoot-exports.md) problemen oplossen.</p> |

   {style="table-layout:auto"}

### Logbestanden zoeken

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **Logboeken**] tabel.

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

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **Logboeken**] tabel.

1. Zoek het logboek dat is gekoppeld aan het exportbestand dat u wilt bewerken.

1. Selecteer het **uitgeeft de pictogram van het de uitvoerlogboek** pictogram ![ ](assets/export-icon.png) naast de logboeknaam.

   of

   Selecteer checkbox naast het logboek, dan uitgezocht [!UICONTROL **geef uitvoer**] uit.

## Kolommen configureren

U kunt kolommen toevoegen of verwijderen op het tabblad [!UICONTROL Logs] om te configureren welke informatie wordt weergegeven.

Selecteer een kolomkop om de logbestanden op die kolom te sorteren. Logbestanden worden standaard gesorteerd op de datum en tijd waarop het exporteren is gestart.

Kolommen configureren op het tabblad [!UICONTROL Logs] :

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **Logboeken**] tabel.

1. Selecteer **aanpassen lijst** pictogram ![ lijst ](assets/customize-table-icon.png) in het hoger-recht van de [!UICONTROL Logs] pagina aanpassen.

   De volgende kolommen zijn beschikbaar:

   | Beschikbare kolom | Beschrijving |
   |---------|----------|
   | Exportnaam | De naam van de exportbewerking. De gebruikers geven uitvoer een naam wanneer zij tot hen, zoals die in [ worden beschreven de rapporten van Customer Journey Analytics van de Uitvoer aan de wolk ](/help/analysis-workspace/export/export-cloud.md) leiden. |
   | Id exporteren | De id wordt automatisch toegewezen aan de exportbewerking wanneer deze wordt gemaakt. <!-- True? --> |
   | Instantie-id | De id van de Customer Journey Analytics-instantie. <!-- True? --> |
   | Naam gegevensweergave | De naam van de gegevensweergave die aan het exporteren is gekoppeld. De gebruikers kunnen de gegevensmening selecteren wanneer zij tot de uitvoer leiden, zoals die in [ wordt beschreven de rapporten van Customer Journey Analytics van de Uitvoer aan de wolk ](/help/analysis-workspace/export/export-cloud.md). |
   | Aantal bestanden | Het aantal bestanden dat is opgenomen in de exportbewerking. |
   | Grootte | De grootte van de exportbewerking.<p>De bestandsgrootte wordt berekend met een basis van 1024, die soms wordt weergegeven als KIB en MIB. Als uw cloudprovider de grootte berekent met een basis van 1000, kan dit ertoe leiden dat de grootte die wordt weergegeven in uw cloudprovider enigszins afwijkt van de grootte die hier wordt weergegeven.</p> |
   | Locatie | De locatie op de account waar de gegevens zijn geëxporteerd. |
   | Account | De account waarin de gegevens zijn geëxporteerd. |
   | Status | De status van de uitvoer. Beschikbare statussen zijn [!UICONTROL Pending] , [!UICONTROL Delivered] en [!UICONTROL Failed] . |
   | Datum van levering | De datum waarop de uitvoer heeft plaatsgevonden. |
   | Accounttype | Het type cloudaccount waarin de gegevens zijn geëxporteerd. Beschikbare accounttypen zijn [!UICONTROL Amazon S3 Role ARN] , [!UICONTROL Google Cloud Platform] , [!UICONTROL Azure SAS] , [!UICONTROL Azure RBAC] , [!UICONTROL Snowflake] en [!UICONTROL Adobe Experience Platform] . |
   | Aantal rijen | Het aantal rijen dat is opgenomen in de geëxporteerde tabel. |

   {style="table-layout:auto"}

1. Zorg ervoor dat alle kolommen die u wilt weergeven, zijn geselecteerd. Geselecteerde kolommen worden weergegeven op de pagina [!UICONTROL Logs] en geven de relevante informatie weer.

## Controlelogboeken weergeven

De volledig-lijst uitvoer wordt ook gevolgd in de [ controlelogboeken van Customer Journey Analytics ](/help/privacy/audit-log.md). <!-- Need to see what the Component Type for full-table export will be and add it here. Also, under "Event type captured by audit logs" there would be a new event type called "Full-table export". 4 actions would be "Create, Delete, Edit, Export" and "API_Request"? Also information about the locations. Probably have a different component for the location credentials.-->
