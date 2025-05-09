---
description: Bestaande exportbewerkingen beheren
keywords: Analysis Workspace
title: Exporteren beheren
feature: Components
exl-id: 0c21802a-c46f-41be-9356-d836c038b174
role: User
source-git-commit: 6f8a43acfba23d6faeff078873742315f1506699
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 0%

---

# Exporteren beheren

Nadat u een volledige tabel hebt geëxporteerd zoals wordt beschreven in [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md), de uitvoer beschikbaar op [!UICONTROL Exports] op het tabblad [!UICONTROL Exports] pagina.

U kunt alleen de exportbewerkingen zien die u maakt.

## Exporteren en zoeken

Als u informatie wilt zoeken die u nodig hebt, kunt u de lijst met exportbewerkingen filteren of naar een exportbewerking zoeken.

### De lijst met exportbewerkingen filteren

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Uitvoer**] tab.

1. Selecteer de **Filter** pictogram.

   <!--add screenshot -->

   U kunt filteren op de volgende criteria:

   | Filter | Beschrijving |
   |---------|----------|
   | [!UICONTROL **Accounttype**] | Het accounttype waaraan het exporteren is gekoppeld. De volgende accounttypen zijn beschikbaar: <ul><li>[!UICONTROL **AEP gegevenslandingszone**]</li><li>[!UICONTROL **Amazon S3 Role ARN**]</li><li>[!UICONTROL **Azure SAS**]</li><li>[!UICONTROL **Azure RBAC**]</li><li>[!UICONTROL **Google Cloud Platform**]</li><li>[!UICONTROL **Snowflake**]</li></ul>. |
   | [!UICONTROL **Status**] | De status van de uitvoer. De volgende statussen zijn beschikbaar: <ul><li>[!UICONTROL **Actief**]: Geeft aan dat een geplande export nog niet is verlopen of dat een eenmalige export nog niet is voltooid. </li><li>[!UICONTROL **Voltooid**]: Geeft aan dat een exportbewerking is geëxporteerd. Voor geplande export geeft dit aan dat de planning is verlopen.</li><li>[!UICONTROL **Mislukt**]<p>In de volgende situaties kan het exporteren mislukken. Houd de aanwijzer boven de [!UICONTROL **Mislukt**] status om details over de fout te zien. <ul><li>Geplande exportvervaldatum</li><li>Rijlimiet bereikt voor geplande export </li></ul> </p></li></ul> |
   | [!UICONTROL **Frequentie**] | Hoe vaak het exporteren plaatsvindt. De volgende frequenties zijn beschikbaar: <ul><li>[!UICONTROL **Eén keer**]</li><li>[!UICONTROL **Dagelijks**]</li><li>[!UICONTROL **Wekelijks**]</li><li>[!UICONTROL **Maandelijks**]</li><li>[!UICONTROL **Jaarlijks**]</li></ul> |

   {style="table-layout:auto"}

### Exporteren zoeken

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Selecteer de [!UICONTROL **Uitvoer**] tab.

1. Typ in het zoekveld alle informatie die is gekoppeld aan het exporteren waarnaar u zoekt. U kunt naar gegevens uit om het even welke kolom zoeken beschikbaar in de lijst.

## Een exportbewerking bewerken

U kunt de eigenschappen, indeling, planning en locatie-informatie van een exportbewerking bewerken.

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Op de [!UICONTROL **Uitvoer**] selecteert u het selectievakje naast het exportbestand dat u wilt bewerken.

   Deze optie is niet beschikbaar als u meerdere exportbewerkingen selecteert.

1. Selecteren [!UICONTROL **Bewerken**].

   De [!UICONTROL **Volledige tabel exporteren**] wordt weergegeven.

1. Werk een van de beschikbare opties bij. Voor informatie over elke optie raadpleegt u [Volledige tabellen exporteren vanuit Analysis Workspace](/help/analysis-workspace/export/export-cloud.md#export-full-tables-from-analysis-workspace) in [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md).

## Een exportbewerking dupliceren

U kunt een bestaande exportbewerking dupliceren.

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Op de [!UICONTROL **Uitvoer**] selecteert u het selectievakje naast de exportbewerking die u wilt dupliceren.

   Deze optie is niet beschikbaar als u meerdere exportbewerkingen selecteert.

1. Selecteren [!UICONTROL **Dupliceren**].

   Er wordt een duplicaat van de exportbewerking gemaakt. De naam van de nieuwe exportbewerking komt overeen met de naam van de oorspronkelijke exportbewerking, met _[!UICONTROL - Copy]_&#x200B;toegevoegd aan de bestandsnaam.

1. (Optioneel) [De nieuwe exportbewerking bewerken](#edit-an-export), inclusief de bestandsnaam en andere eigenschappen die u wilt wijzigen.

## Handmatig een exportbewerking starten

U kunt een exportbewerking handmatig starten voor een geplande exportbewerking of een eenmalige exportbewerking die eerder is voltooid.

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Op de [!UICONTROL **Uitvoer**] selecteert u het selectievakje naast het exportbestand dat u wilt uitvoeren.

   Deze optie is niet beschikbaar als u meerdere exportbewerkingen selecteert.

1. Selecteren [!UICONTROL **Nu exporteren**].

## Een exportlabel geven

Wanneer u labels toepast op een exportbewerking, kunt u deze tags weergeven in het dialoogvenster [!UICONTROL Tags] kolom op de [!UICONTROL Exports] pagina. Zie [Kolommen configureren](#configure-columns) voor meer informatie .

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Op de [!UICONTROL **Uitvoer**] selecteert u het selectievakje naast een of meer exportbewerkingen die u wilt labelen.

1. Selecteren [!UICONTROL **Codes bewerken**].

1. In de [!UICONTROL **Tag exporteren**] typt u de naam van een tag om een nieuwe tag te maken of kiest u een bestaande tag in het vervolgkeuzemenu.

   Alle gebruikelijke labels tussen de geselecteerde exportbewerkingen worden weergegeven in het dialoogvenster Code. <!-- what happens if one export has a tag and another doesn't? Is the tag removed if you don't select it? I'm guessing not, but maybe check -->

1. Selecteren [!UICONTROL **Labels toepassen**].

## Een exportbewerking verwijderen

U kunt exportbewerkingen verwijderen van de pagina Exporteren. Geplande exportbewerkingen die worden verwijderd, worden niet meer verzonden.

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Op de [!UICONTROL **Uitvoer**] selecteert u het selectievakje naast een of meer exportbewerkingen die u wilt verwijderen.

1. Selecteren [!UICONTROL **Verwijderen**] selecteert u vervolgens [!UICONTROL **Verwijderen**] wanneer u het bevestigingsbericht ziet.

## Kolommen configureren op het tabblad [!UICONTROL Exports] page

U kunt kolommen toevoegen aan of verwijderen uit de [!UICONTROL Exports] om te configureren welke informatie wordt weergegeven.

Selecteer een kolomkop om het exporteren op die kolom te sorteren. Standaard worden exportbewerkingen gesorteerd op de datum en tijd waarop de exportbewerking voor het laatst is gewijzigd.

1. Selecteer in Customer Journey Analytics [!UICONTROL **Componenten**] > [!UICONTROL **Uitvoer**].

1. Op de [!UICONTROL **Uitvoer**] selecteert u de **Tabel aanpassen** pictogram ![tabel aanpassen](assets/customize-table-icon.png) in de rechterbovenhoek van het [!UICONTROL Exports] pagina.

   De volgende kolommen zijn beschikbaar:

   | Beschikbare kolom | Beschrijving |
   |---------|----------|
   | Naam | De naam van de exportbewerking. De gebruikers geven de uitvoer een naam wanneer zij tot hen leiden, zoals die in worden beschreven [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md). |
   | ID | De id wordt automatisch toegewezen aan de exportbewerking wanneer deze wordt gemaakt. <!-- True? --> |
   | Naam gegevensweergave | De naam van de gegevensweergave die aan het exporteren is gekoppeld. Gebruikers kunnen de gegevensweergave selecteren wanneer ze de exportbewerking maken, zoals wordt beschreven in [Rapporten van de Customer Journey Analytics van de uitvoer naar de wolk](/help/analysis-workspace/export/export-cloud.md). |
   | Status | De status van de uitvoer. Beschikbare statussen zijn [!UICONTROL Active], [!UICONTROL Completed], en [!UICONTROL Failed].<p> **Opmerking:** Voor informatie over het oplossen van problemen ontbrak de uitvoer, zie [Problemen met mislukte exportbewerkingen oplossen](/help/components/exports/troubleshoot-exports.md).</p> |
   | Tags | Hiermee geeft u alle tags weer die op het exporteren zijn toegepast. Voor informatie over het toepassen van labels op een exportbewerking raadpleegt u [Een exportlabel geven](#tag-an-export). |
   | Tabelgrootte (laatste verzending) | De grootte van de export wanneer deze voor het laatst is verzonden. |
   | Gemaakt door | De gebruiker die de exportbewerking heeft gemaakt. |
   | Gemaakt | De datum en tijd waarop de exportbewerking is gemaakt. <!-- true? --> |
   | Locatie | De locatie op de account waar de gegevens zijn geëxporteerd. |
   | Account | De account waarin de gegevens zijn geëxporteerd. |
   | Frequentie | De frequentie waarin de uitvoer wordt verzonden. Beschikbare opties zijn [!UICONTROL One time], [!UICONTROL Daily], [!UICONTROL Weekly], [!UICONTROL Monthly by day of the week], [!UICONTROL Monthly by day of the month], [!UICONTROL Yearly by day of the month], en [!UICONTROL Yearly by specific date]. |
   | Verzonden tijd | Het tijdstip waarop het exporteren is verzonden. |
   | Laatst verzonden | De laatste keer dat de exportbewerking is verzonden. |
   | Laatst gewijzigd | De laatste keer dat de exportbewerking is gewijzigd. De punten op de pagina van Uitvoer worden gesorteerd door deze kolom door gebrek. |
   | Accounttype | Het type cloudaccount waarin de gegevens zijn geëxporteerd. Beschikbare accounttypen zijn [!UICONTROL Amazon S3 Role ARN], [!UICONTROL Google Cloud Platform], [!UICONTROL Azure SAS], [!UICONTROL Azure RBAC], [!UICONTROL Snowflake], en [!UICONTROL Adobe Experience Platform]. |

   {style="table-layout:auto"}

1. Zorg ervoor dat alle kolommen die u wilt weergeven, zijn geselecteerd. Geselecteerde kolommen worden weergegeven op de pagina Exporteren en geven de relevante informatie weer.
