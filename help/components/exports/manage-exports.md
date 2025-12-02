---
description: Bestaande exportbewerkingen beheren
keywords: Analysis Workspace
title: Exporteren beheren
feature: Components
exl-id: 0c21802a-c46f-41be-9356-d836c038b174
role: User
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 0%

---

# Exporteren beheren

Nadat u een volledige lijst zoals die in [&#x200B; wordt beschreven de rapporten van Customer Journey Analytics van de Uitvoer naar de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md) uitvoert, zijn de uitvoer beschikbaar op het [!UICONTROL Exports] lusje op de [!UICONTROL Exports] pagina.

U kunt alleen de exportbewerkingen zien die u maakt.

## Exporteren en zoeken

Als u informatie wilt zoeken die u nodig hebt, kunt u de lijst met exportbewerkingen filteren of naar een exportbewerking zoeken.

### De lijst met exportbewerkingen filteren

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **Uitvoer**] tabel.

1. Selecteer het **pictogram van de Filter**.

   <!--add screenshot -->

   U kunt filteren op de volgende criteria:

   | Filter | Beschrijving |
   |---------|----------|
   | [!UICONTROL **Type van Rekening**] | Het accounttype waaraan het exporteren is gekoppeld. De volgende accounttypen zijn beschikbaar: <ul><li>[!UICONTROL **AEP Gegevens die Zone**] aanvoeren</li><li>[!UICONTROL **Amazon S3 Rol ARN**]</li><li>[!UICONTROL **Azure SAS**]</li><li>[!UICONTROL **Azure RBAC**]</li><li>[!UICONTROL **Google Cloud Platform**]</li><li>[!UICONTROL **Snowflake**]</li></ul>. |
   | [!UICONTROL **Status**] | De status van de uitvoer. De volgende statussen zijn beschikbaar: <ul><li>[!UICONTROL **Actief**]: Wijst erop dat een geplande uitvoer nog niet is verlopen, of dat een eenmalig uitvoer nog niet heeft voltooid. </li><li>[!UICONTROL **Voltooid**]: Wijst erop dat de uitvoer met succes heeft uitgevoerd. Voor geplande export geeft dit aan dat de planning is verlopen.</li><li>[!UICONTROL **Ontbroken**]<p>In de volgende situaties kan het exporteren mislukken. Beweeg over [!UICONTROL **Ontbroken**] status om details over de mislukking te zien. <ul><li>Geplande exportvervaldatum</li><li>Rijlimiet bereikt voor geplande export </li></ul> </p></li></ul> |
   | [!UICONTROL **Frequentie**] | Hoe vaak het exporteren plaatsvindt. De volgende frequenties zijn beschikbaar: <ul><li>[!UICONTROL **Één keer**]</li><li>[!UICONTROL **Dagelijks**]</li><li>[!UICONTROL **Wekelijks**]</li><li>[!UICONTROL **Maandelijks**]</li><li>[!UICONTROL **jaarlijks**]</li></ul> |

   {style="table-layout:auto"}

### Exporteren zoeken

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Selecteer de [!UICONTROL **Uitvoer**] tabel.

1. Typ in het zoekveld alle informatie die is gekoppeld aan het exporteren waarnaar u zoekt. U kunt naar gegevens uit om het even welke kolom zoeken beschikbaar in de lijst.

## Een exportbewerking bewerken

U kunt de eigenschappen, indeling, planning en locatie-informatie van een exportbewerking bewerken.

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Voor [!UICONTROL **Uitvoer**] lusje, selecteer checkbox naast de uitvoer u wilt uitgeven.

   Deze optie is niet beschikbaar als u meerdere exportbewerkingen selecteert.

1. Selecteer [!UICONTROL **uitgeven**].

   De [!UICONTROL **volledige lijst van de Uitvoer**] dialoogvertoningen.

1. Werk een van de beschikbare opties bij. Voor informatie over elke optie, zie [&#x200B; Uitvoer volledige lijsten van Analysis Workspace &#x200B;](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace) in [&#x200B; de rapporten van Customer Journey Analytics van de Uitvoer aan de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md).

## Een exportbewerking dupliceren

U kunt een bestaande exportbewerking dupliceren.

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Voor [!UICONTROL **Uitvoer**] lusje, selecteer checkbox naast de uitvoer u wilt dupliceren.

   Deze optie is niet beschikbaar als u meerdere exportbewerkingen selecteert.

1. Selecteer [!UICONTROL **Dupliceren**].

   Er wordt een duplicaat van de exportbewerking gemaakt. De naam van de nieuwe exportbewerking komt overeen met de naam van de oorspronkelijke exportbewerking, waarbij _[!UICONTROL - Copy]_&#x200B;aan de bestandsnaam wordt toegevoegd.

1. (Facultatief) [&#x200B; geef de nieuwe uitvoer &#x200B;](#edit-an-export) uit, met inbegrip van het dossier - noem en een andere eigenschappen u wilt veranderen.

## Handmatig een exportbewerking starten

U kunt een exportbewerking handmatig starten voor een geplande exportbewerking of een eenmalige exportbewerking die eerder is voltooid.

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Op [!UICONTROL **voert**] lusje uit, selecteer checkbox naast de uitvoer u wilt in werking stellen.

   Deze optie is niet beschikbaar als u meerdere exportbewerkingen selecteert.

1. Selecteer [!UICONTROL **nu de Uitvoer**].

## Een exportlabel geven

Wanneer u labels toepast op een exportbewerking, kunt u deze tags weergeven in de kolom [!UICONTROL Tags] op de pagina van [!UICONTROL Exports] . Zie [&#x200B; kolommen &#x200B;](#configure-columns) voor meer informatie vormen.

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Op [!UICONTROL **voert**] lusje uit, selecteer checkbox naast één of meerdere uitvoer die u wilt etiketteren.

1. Selecteer [!UICONTROL **uitgeven markeringen**].

1. In de [!UICONTROL **de uitvoer van de Markering**] dialoog, typ de naam van een markering om een nieuwe markering tot stand te brengen, of kies een bestaande markering van het drop-down menu.

   Alle gebruikelijke labels tussen de geselecteerde exportbewerkingen worden weergegeven in het dialoogvenster Code. <!-- what happens if one export has a tag and another doesn't? Is the tag removed if you don't select it? I'm guessing not, but maybe check -->

1. Selecteer [!UICONTROL **toepassen markeringen**].

## Een exportbewerking verwijderen

U kunt exportbewerkingen verwijderen van de pagina Exporteren. Geplande exportbewerkingen die worden verwijderd, worden niet meer verzonden.

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Op [!UICONTROL **voert**] lusje uit, selecteer checkbox naast één of meerdere uitvoer die u wilt schrappen.

1. Selecteer [!UICONTROL **Schrapping**], dan uitgezocht [!UICONTROL **Schrapping**] wanneer u het bevestigingsbericht ziet.

## Kolommen op de pagina [!UICONTROL Exports] configureren

U kunt kolommen toevoegen of verwijderen op het tabblad [!UICONTROL Exports] om te configureren welke informatie wordt weergegeven.

Selecteer een kolomkop om het exporteren op die kolom te sorteren. Standaard worden exportbewerkingen gesorteerd op de datum en tijd waarop de exportbewerking voor het laatst is gewijzigd.

1. In Customer Journey Analytics, uitgezochte [!UICONTROL **Componenten**] > [!UICONTROL **voert**] uit.

1. Op het [!UICONTROL **Uitvoer**] lusje, selecteer **aanpassen lijst** pictogram ![&#x200B; aanpassen lijst &#x200B;](assets/customize-table-icon.png) in het hoger-recht van de [!UICONTROL Exports] pagina.

   De volgende kolommen zijn beschikbaar:

   | Beschikbare kolom | Beschrijving |
   |---------|----------|
   | Naam | De naam van de exportbewerking. De gebruikers geven uitvoer een naam wanneer zij tot hen, zoals die in [&#x200B; worden beschreven de rapporten van Customer Journey Analytics van de Uitvoer aan de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md) leiden. |
   | ID | De id wordt automatisch toegewezen aan de exportbewerking wanneer deze wordt gemaakt. <!-- True? --> |
   | Naam gegevensweergave | De naam van de gegevensweergave die aan het exporteren is gekoppeld. De gebruikers kunnen de gegevensmening selecteren wanneer zij tot de uitvoer leiden, zoals die in [&#x200B; wordt beschreven de rapporten van Customer Journey Analytics van de Uitvoer aan de wolk &#x200B;](/help/analysis-workspace/export/export-cloud.md). |
   | Status | De status van de uitvoer. Beschikbare statussen zijn [!UICONTROL Active] , [!UICONTROL Completed] en [!UICONTROL Failed] .<p> **Nota:** voor informatie over het oplossen van problemenontbroken uitvoer, zie [&#x200B; ontbroken uitvoer problemen oplossen &#x200B;](/help/components/exports/troubleshoot-exports.md).</p> |
   | Tags | Hiermee geeft u alle tags weer die op het exporteren zijn toegepast. Voor informatie over hoe te om markeringen op de uitvoer toe te passen, zie [&#x200B; Tags en de uitvoer &#x200B;](#tag-an-export). |
   | Tabelgrootte (laatste verzending) | De grootte van de export wanneer deze voor het laatst is verzonden. |
   | Gemaakt door | De gebruiker die de exportbewerking heeft gemaakt. |
   | Gemaakt | De datum en tijd waarop de exportbewerking is gemaakt. <!-- true? --> |
   | Locatie | De locatie op de account waar de gegevens zijn geëxporteerd. |
   | Account | De account waarin de gegevens zijn geëxporteerd. |
   | Frequentie | De frequentie waarin de uitvoer wordt verzonden. Beschikbare opties zijn [!UICONTROL One time] , [!UICONTROL Daily] , [!UICONTROL Weekly] , [!UICONTROL Monthly by day of the week] , [!UICONTROL Monthly by day of the month] , [!UICONTROL Yearly by day of the month] en [!UICONTROL Yearly by specific date] . |
   | Verzonden tijd | Het tijdstip waarop het exporteren is verzonden. |
   | Laatst verzonden | De laatste keer dat de exportbewerking is verzonden. |
   | Laatst gewijzigd | De laatste keer dat de exportbewerking is gewijzigd. De punten op de pagina van Uitvoer worden gesorteerd door deze kolom door gebrek. |
   | Accounttype | Het type cloudaccount waarin de gegevens zijn geëxporteerd. Beschikbare accounttypen zijn [!UICONTROL Amazon S3 Role ARN] , [!UICONTROL Google Cloud Platform] , [!UICONTROL Azure SAS] , [!UICONTROL Azure RBAC] , [!UICONTROL Snowflake] en [!UICONTROL Adobe Experience Platform] . |

   {style="table-layout:auto"}

1. Zorg ervoor dat alle kolommen die u wilt weergeven, zijn geselecteerd. Geselecteerde kolommen worden weergegeven op de pagina Exporteren en geven de relevante informatie weer.
