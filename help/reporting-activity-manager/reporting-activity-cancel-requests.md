---
title: Rapportageverzoeken annuleren in de Manager van de Activiteit van de Rapportering
description: Leer over hoe te om de Manager van de Activiteit van de Rapportering te gebruiken om capaciteitskwesties tijdens piekrapporteringstijden te diagnostiseren en te bevestigen.
solution: Customer Journey Analytics
feature: Basics
source-git-commit: 23509d26e08b50a6b7a133fdc9a3e2d2d3e8fe43
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# Rapportageverzoeken annuleren in de Manager van de Activiteit van de Rapportering

{{release-limited-testing}}

De [!UICONTROL Reporting Activity Manager] kunnen beheerders rapportageaanvragen snel diagnosticeren en annuleren om problemen met de rapportagecapaciteit tijdens piekrapportagetijden op te lossen.

Overweeg het volgende wanneer het annuleren van rapporteringsverzoeken:

* U kunt specifieke verzoeken annuleren, alle verzoeken van een specifieke gebruiker annuleren of alle verzoeken met betrekking tot een specifiek project annuleren.

* Wanneer u verzoeken annuleert, kunt u ook verkiezen om verdere verzoeken voor een bepaalde tijdspanne te beperken.

* U kunt een aanvraag niet annuleren als de [!UICONTROL **Gebruiker**] de kolom van een verzoek toont zoals [!UICONTROL **Niet herkend**]. Wanneer dit voorkomt, betekent het dat de gebruiker in een login bedrijf is waar u geen administratieve toestemmingen hebt.

Voor meer informatie over het Melden van de Manager van de Activiteit, met inbegrip van zeer belangrijke voordelen en toestemmingsvereisten, zie [Overzicht van Activity Manager rapporteren](/help/reporting-activity-manager/reporting-activity-overview.md).

## Specifieke verzoeken annuleren

U kunt individuele verzoeken annuleren die een grote hoeveelheid rapporteringscapaciteit verbruiken.

1. Ga in de Customer Journey Analytics naar **[!UICONTROL Tools]** > **[!UICONTROL Reporting Activity Manager]**.

1. Selecteer de verbinding waar u rapportageaanvragen wilt annuleren. <!--double-check this step-->

   Zie voor meer informatie over de gegevens die op deze pagina beschikbaar zijn [Rapportactiviteiten weergeven in de rapportagManager](/help/reporting-activity-manager/reporting-activity.md).

1. Selecteer de [!UICONTROL **Verzoeken**] selecteert u een of meer aanvragen.

   <!-- add screenshot -->

1. Selecteren [!UICONTROL **Aanvragen annuleren**].

   De [!UICONTROL **Annuleren _x_ verzoeken om rapportage**] wordt weergegeven.

1. In het veld Bericht van annulering wordt het bericht weergegeven dat aan gebruikers wordt weergegeven wanneer hun aanvragen worden geannuleerd. Er wordt een standaardbericht weergegeven. U kunt het standaardbericht bijwerken voor meer informatie.

1. (Facultatief) om toekomstige verzoeken voor een bepaalde periode te beperken, laat de optie toe [!UICONTROL **Verdere verzoeken beperken**] Kies vervolgens een van de volgende opties:

   | Optie | -functie |
   |---------|----------|
   | [!UICONTROL **Gebruiker en project**] | De gebruikers verbonden aan de geselecteerde verzoeken zullen tijdelijk worden beperkt van het runnen van rapporteringsverzoeken voor de bijbehorende projecten. |
   | [!UICONTROL **Gebruiker**] | De gebruikers verbonden aan de geselecteerde verzoeken zullen tijdelijk worden beperkt van het maken van om het even welke rapporteringsverzoeken. |
   | [!UICONTROL **Project**] | De projecten verbonden aan de geselecteerde verzoeken zullen tijdelijk van alle rapporteringsverzoeken worden beperkt. |
   | [!UICONTROL **Beperkt voor**] | Kies hoe lang aanvragen worden beperkt. U kunt 1 minuut (standaard), 5 minuten, 10 minuten, 15 minuten of 30 minuten kiezen. <!-- double-check this --><p>U kunt een beperking niet eerder verwijderen nadat deze is ingesteld.</p> |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Doorgaan met annulering**].

   In Analysis Workspace wordt een melding weergegeven waarin gebruikers worden geïnformeerd dat het verzoek is geannuleerd. Ga voor meer informatie over hoe dit in Analysis Workspace wordt weergegeven naar [Ervaring wanneer de gebruikers tot een geannuleerd rapport toegang hebben](#experience-when-users-access-a-cancelled-report).

## Aanvragen door gebruiker annuleren

U kunt alle aanvragen annuleren die aan een of meer gebruikers zijn gekoppeld.

1. Ga in de Customer Journey Analytics naar **[!UICONTROL Tools]** > **[!UICONTROL Reporting Activity Manager]**.

1. Selecteer de verbinding waar u rapportageaanvragen wilt annuleren. <!--double-check this step-->

   Zie voor meer informatie over de gegevens die op deze pagina beschikbaar zijn [Rapportactiviteiten weergeven in de rapportagManager](/help/reporting-activity-manager/reporting-activity.md).

1. Selecteer de [!UICONTROL **Gebruikers**] selecteert u een of meer gebruikers.

   <!-- add screenshot -->

1. Selecteren [!UICONTROL **Aanvragen annuleren**].

   De [!UICONTROL **Annuleren _x_ rapporteert verzoeken van x gebruikers**] wordt weergegeven.

1. In het veld Bericht van annulering wordt het bericht weergegeven dat aan gebruikers wordt weergegeven wanneer hun aanvragen worden geannuleerd. Er wordt een standaardbericht weergegeven. U kunt het standaardbericht bijwerken voor meer informatie.

1. (Facultatief) om toekomstige verzoeken voor een bepaalde periode te beperken, laat de optie toe [!UICONTROL **Verdere verzoeken beperken**] Kies vervolgens een van de volgende opties:

   | Optie | -functie |
   |---------|----------|
   | [!UICONTROL **Gebruiker en project**] | Geselecteerde gebruikers kunnen tijdelijk geen rapportageaanvragen voor de bijbehorende projecten indienen. |
   | [!UICONTROL **Gebruiker**] | Geselecteerde gebruikers kunnen tijdelijk geen rapportageaanvragen indienen. |
   | [!UICONTROL **Project**] | Projecten die aan de geselecteerde gebruikers zijn gekoppeld, worden beperkt tot alle rapportageaanvragen die door gebruikers worden ingediend. |
   | [!UICONTROL **Beperkt voor**] | Kies hoe lang aanvragen worden beperkt. U kunt 1 minuut (standaard), 5 minuten, 10 minuten, 15 minuten of 30 minuten kiezen. <!--double-check this--> <p>U kunt een beperking niet eerder verwijderen nadat deze is ingesteld.</p> |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Doorgaan met annulering**].

   In Analysis Workspace wordt een melding weergegeven waarin gebruikers worden geïnformeerd dat het verzoek is geannuleerd. Ga voor meer informatie over hoe dit in Analysis Workspace wordt weergegeven naar [Ervaring wanneer de gebruikers tot een geannuleerd rapport toegang hebben](#experience-when-users-access-a-cancelled-report).

## Aanvragen door project annuleren

U kunt alle verzoeken annuleren die aan één of meerdere projecten worden geassocieerd.

1. Ga in de Customer Journey Analytics naar **[!UICONTROL Tools]** > **[!UICONTROL Reporting Activity Manager]**.

1. Selecteer de verbinding waar u rapportageaanvragen wilt annuleren. <!--double-check this step-->

   Zie voor meer informatie over de gegevens die op deze pagina beschikbaar zijn [Rapportactiviteiten weergeven in de rapportagManager](/help/reporting-activity-manager/reporting-activity.md).

1. Selecteer de [!UICONTROL **Projecten**] selecteert u vervolgens een of meer projecten.

   <!-- add screenshot -->

1. Selecteren [!UICONTROL **Aanvragen annuleren**].

   De [!UICONTROL **Annuleren _x_ rapporteert verzoeken van x projecten**] wordt weergegeven.

1. In het veld Bericht van annulering wordt het bericht weergegeven dat aan gebruikers wordt weergegeven wanneer hun aanvragen worden geannuleerd. Er wordt een standaardbericht weergegeven. U kunt het standaardbericht bijwerken voor meer informatie.

1. (Facultatief) om toekomstige verzoeken voor een bepaalde periode te beperken, laat de optie toe [!UICONTROL **Verdere verzoeken beperken**] Kies vervolgens een van de volgende opties:

   | Optie | -functie |
   |---------|----------|
   | [!UICONTROL **Gebruiker en project**] | Geselecteerde projecten worden tijdelijk beperkt van alle rapportageaanvragen die door de betrokken gebruikers worden ingediend. |
   | [!UICONTROL **Gebruiker**] | De gebruikers verbonden aan de geselecteerde projecten zullen worden beperkt van het indienen van om het even welke rapporteringsverzoeken. |
   | [!UICONTROL **Project**] | De geselecteerde projecten zullen tijdelijk van om het even welke rapporteringsverzoeken worden beperkt die door om het even welke gebruiker worden gemaakt. |
   | [!UICONTROL **Beperkt voor**] | Kies hoe lang aanvragen worden beperkt. U kunt 1 minuut (standaard), 5 minuten, 10 minuten, 15 minuten of 30 minuten kiezen. <!--double-check this--> <p>U kunt een beperking niet eerder verwijderen nadat deze is ingesteld.</p> |

   {style="table-layout:auto"}

1. Selecteren [!UICONTROL **Doorgaan met annulering**].

   In Analysis Workspace wordt een melding weergegeven waarin gebruikers worden geïnformeerd dat het verzoek is geannuleerd. Ga voor meer informatie over hoe dit in Analysis Workspace wordt weergegeven naar [Ervaring wanneer de gebruikers tot een geannuleerd rapport toegang hebben](#experience-when-users-access-a-cancelled-report).

## Ervaring wanneer de gebruikers tot een geannuleerd rapport toegang hebben

In Analysis Workspace, zien de gebruikers het volgende bericht wanneer zij proberen om tot een rapport toegang te hebben dat door een beheerder werd geannuleerd:

![cancel-user-notice](assets/cancel-user-facing.png)