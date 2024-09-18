---
title: Rapportageverzoeken annuleren in de Manager van de Activiteit van de Rapportering
description: Leer over hoe te om de Manager van de Activiteit van de Rapportering te gebruiken om capaciteitskwesties tijdens piekrapporteringstijden te diagnostiseren en te bevestigen.
solution: Customer Journey Analytics
feature: Basics
exl-id: 87da2447-f114-432a-9f63-e660c2541d0f
role: Admin
source-git-commit: def8b074ea468e409e340415d5e96f75d6b69312
workflow-type: tm+mt
source-wordcount: '1478'
ht-degree: 0%

---

# Rapportageverzoeken annuleren in de Manager van de Activiteit van de Rapportering

Met [!UICONTROL Reporting Activity Manager] kunnen beheerders snel rapportageaanvragen diagnosticeren en annuleren om problemen met de rapportcapaciteit tijdens piekrapportagetijden op te lossen.

Overweeg het volgende wanneer het annuleren van rapporteringsverzoeken:

* U kunt specifieke verzoeken annuleren, alle verzoeken van een specifieke gebruiker annuleren of alle verzoeken met betrekking tot een specifiek project annuleren.

* Wanneer u verzoeken annuleert, kunt u ook verkiezen om verdere verzoeken voor een bepaalde tijdspanne te beperken.

  Wanneer u een verder verzoek beperkt, wordt de actie geregistreerd in het [ Logboek van de Controle ](/help/privacy/audit-log.md) met de actienaam van EMBARGO.

* U kunt geen verzoek annuleren als de [!UICONTROL **Gebruiker**] kolom van een verzoek als [!UICONTROL **niet erkend**] toont. Wanneer dit voorkomt, betekent het dat de gebruiker in een login bedrijf is waar u geen administratieve toestemmingen hebt.

Voor meer informatie over het Melden van de Manager van de Activiteit, met inbegrip van zeer belangrijke voordelen en toestemmingsvereisten, zie [ het Overzicht van de Manager van de Activiteit ](/help/reporting-activity-manager/reporting-activity-overview.md) melden.

## Specifieke verzoeken annuleren

U kunt individuele verzoeken annuleren die een grote hoeveelheid rapporteringscapaciteit verbruiken. Wanneer u een aanvraag annuleert, kunt u ervoor kiezen deze gedurende een bepaalde periode verder te beperken.

1. Ga in Customer Journey Analytics naar **[!UICONTROL Tools]** > **[!UICONTROL Reporting Activity Manager]** .

1. Selecteer de verbinding waar u rapportageaanvragen wilt annuleren. <!--double-check this step-->

   Voor meer informatie over de gegevens beschikbaar op deze pagina, zie [ Mening rapporterend activiteit in de Manager van de Activiteit van de Rapportering ](/help/reporting-activity-manager/reporting-activity.md).

1. Selecteer het [!UICONTROL **lusje van Verzoeken**], dan selecteer één of meerdere verzoeken.

   <!-- add screenshot -->

1. Selecteer [!UICONTROL **annuleert verzoeken**].

   [!UICONTROL **annuleert _x_ verzoeken van het rapportverzoek**] dialoogdoos.

1. In het veld Bericht van annulering wordt het bericht weergegeven dat aan gebruikers wordt weergegeven wanneer hun aanvragen worden geannuleerd. Er wordt een standaardbericht weergegeven. U kunt het standaardbericht bijwerken voor meer informatie.

1. (Optioneel) Toekomstige verzoeken voor een bepaalde periode beperken:

   1. Laat de optie toe om [!UICONTROL **verdere verzoeken**] te beperken.

      ![ annuleert 1 verzoek die de Volgende geselecteerde verzoeken van Beperken en het bericht van de Annulering tonen.](assets/restrict-subsequent-requests.png)

   1. Kies een van de volgende opties:

      | Optie | Functie |
      |---------|----------|
      | [!UICONTROL **Gebruiker &amp; project**] | De gebruikers verbonden aan de geselecteerde verzoeken zullen tijdelijk worden beperkt van het runnen van rapporteringsverzoeken voor de bijbehorende projecten. |
      | [!UICONTROL **Gebruiker**] | De gebruikers verbonden aan de geselecteerde verzoeken zullen tijdelijk worden beperkt van het maken van om het even welke rapporteringsverzoeken. |
      | [!UICONTROL **Project**] | De projecten verbonden aan de geselecteerde verzoeken zullen tijdelijk van alle rapporteringsverzoeken worden beperkt. |
      | [!UICONTROL **Beperkt voor**] | Kies hoe lang aanvragen worden beperkt. U kunt 1 minuut (standaard), 5 minuten, 10 minuten, 15 minuten of 30 minuten kiezen. <!-- double-check this --><p>U kunt een beperking niet eerder verwijderen nadat deze is ingesteld.</p> |

      {style="table-layout:auto"}

1. Selecteer [!UICONTROL **verdergaan met annulering**].

   In Analysis Workspace wordt een melding weergegeven waarin gebruikers worden geïnformeerd dat het verzoek is geannuleerd. Voor meer informatie over hoe dit in Analysis Workspace verschijnt, zie [ Ervaring wanneer de gebruikers tot een geannuleerd rapport ](#experience-when-users-access-a-cancelled-report) toegang hebben.

## Aanvragen door gebruiker annuleren

U kunt alle aanvragen annuleren die aan een of meer gebruikers zijn gekoppeld. Wanneer u verzoeken annuleert die aan een gebruiker zijn gekoppeld, kunt u verzoeken van die gebruiker voor een bepaalde periode verder beperken.

1. Ga in Customer Journey Analytics naar **[!UICONTROL Tools]** > **[!UICONTROL Reporting Activity Manager]** .

1. Selecteer de verbinding waar u rapportageaanvragen wilt annuleren. <!--double-check this step-->

   Voor meer informatie over de gegevens beschikbaar op deze pagina, zie [ Mening rapporterend activiteit in de Manager van de Activiteit van de Rapportering ](/help/reporting-activity-manager/reporting-activity.md).

1. Selecteer het [!UICONTROL **lusje van Gebruikers**], dan selecteer één of meerdere gebruikers.

   <!-- add screenshot -->

1. Selecteer [!UICONTROL **annuleert verzoeken**].

   [!UICONTROL **annuleert _x_ verzoeken van het rapport van x gebruikers**] vertoningen van de dialoogdoos.

1. In het veld Bericht van annulering wordt het bericht weergegeven dat aan gebruikers wordt weergegeven wanneer hun aanvragen worden geannuleerd. Er wordt een standaardbericht weergegeven. U kunt het standaardbericht bijwerken voor meer informatie.

1. (Optioneel) Toekomstige verzoeken voor een bepaalde periode beperken:

   1. Laat de optie toe om [!UICONTROL **verdere verzoeken**] te beperken

      ![ annuleert 1 verzoek die de Beperk verdere verzoeken door geselecteerde gebruiker tonen.](assets/restrict-subsequent-requests-user.png)

   1. Kies een van de volgende opties:

      | Optie | Functie |
      |---------|----------|
      | [!UICONTROL **Gebruiker &amp; project**] | Geselecteerde gebruikers kunnen tijdelijk geen rapportageaanvragen voor de bijbehorende projecten indienen. <p>Dit is de minst beperkende optie.</p> |
      | [!UICONTROL **Gebruiker**] | Geselecteerde gebruikers kunnen tijdelijk geen rapportageaanvragen indienen. |
      | [!UICONTROL **Project**] | Projecten die aan de geselecteerde gebruikers zijn gekoppeld, worden beperkt tot alle rapportageaanvragen die door gebruikers worden ingediend. |
      | [!UICONTROL **Beperkt voor**] | Kies hoe lang aanvragen worden beperkt. U kunt 1 minuut (standaard), 5 minuten, 10 minuten, 15 minuten of 30 minuten kiezen. <!--double-check this--> <p>U kunt een beperking niet eerder verwijderen nadat deze is ingesteld.</p> |

      {style="table-layout:auto"}

1. Selecteer [!UICONTROL **verdergaan met annulering**].

   In Analysis Workspace wordt een melding weergegeven waarin gebruikers worden geïnformeerd dat het verzoek is geannuleerd. Voor meer informatie over hoe dit in Analysis Workspace verschijnt, zie [ Ervaring wanneer de gebruikers tot een geannuleerd rapport ](#experience-when-users-access-a-cancelled-report) toegang hebben.

## Aanvragen door project annuleren

U kunt alle verzoeken annuleren die aan één of meerdere projecten worden geassocieerd. Wanneer het annuleren van verzoeken verbonden aan een project, kunt u verkiezen om verzoeken verbonden aan dat project voor een bepaalde tijdspanne verder te beperken.

1. Ga in Customer Journey Analytics naar **[!UICONTROL Tools]** > **[!UICONTROL Reporting Activity Manager]** .

1. Selecteer de verbinding waar u rapportageaanvragen wilt annuleren. <!--double-check this step-->

   Voor meer informatie over de gegevens beschikbaar op deze pagina, zie [ Mening rapporterend activiteit in de Manager van de Activiteit van de Rapportering ](/help/reporting-activity-manager/reporting-activity.md).

1. Selecteer het [!UICONTROL **lusje van Projecten**], dan selecteer één of meerdere projecten.

   <!-- add screenshot -->

1. Selecteer [!UICONTROL **annuleert verzoeken**].

   [!UICONTROL **annuleert _x_ rapportverzoeken van x projecten**] vertoningen van de dialoogdoos.

1. In het veld Bericht van annulering wordt het bericht weergegeven dat aan gebruikers wordt weergegeven wanneer hun aanvragen worden geannuleerd. Er wordt een standaardbericht weergegeven. U kunt het standaardbericht bijwerken voor meer informatie.

1. (Optioneel) Toekomstige verzoeken voor een bepaalde periode beperken:

   1. Laat de optie toe om [!UICONTROL **verdere verzoeken**] te beperken.

      ![ annuleert 1 verzoek die de Beperk verdere verzoeken door project tonen ](assets/restrict-subsequent-requests-project.png)

   1. Kies een van de volgende opties:

      | Optie | Functie |
      |---------|----------|
      | [!UICONTROL **Gebruiker &amp; project**] | Geselecteerde projecten worden tijdelijk beperkt van alle rapportageaanvragen die door de betrokken gebruikers worden ingediend.<p>Dit is de minst beperkende optie.</p> |
      | [!UICONTROL **Gebruiker**] | De gebruikers verbonden aan de geselecteerde projecten zullen worden beperkt van het indienen van om het even welke rapporteringsverzoeken. |
      | [!UICONTROL **Project**] | De geselecteerde projecten zullen tijdelijk van om het even welke rapporteringsverzoeken worden beperkt die door om het even welke gebruiker worden gemaakt. |
      | [!UICONTROL **Beperkt voor**] | Kies hoe lang aanvragen worden beperkt. U kunt 1 minuut (standaard), 5 minuten, 10 minuten, 15 minuten of 30 minuten kiezen. <!--double-check this--> <p>U kunt een beperking niet eerder verwijderen nadat deze is ingesteld.</p> |

      {style="table-layout:auto"}

1. Selecteer [!UICONTROL **verdergaan met annulering**].

   In Analysis Workspace wordt een melding weergegeven waarin gebruikers worden geïnformeerd dat het verzoek is geannuleerd. Voor meer informatie over hoe dit in Analysis Workspace verschijnt, zie [ Ervaring wanneer de gebruikers tot een geannuleerd rapport ](#experience-when-users-access-a-cancelled-report) toegang hebben.

## Aanvragen door toepassing annuleren

U kunt alle aanvragen annuleren die aan een of meer toepassingen zijn gekoppeld. Wanneer u aanvragen die aan een toepassing zijn gekoppeld, annuleert, kunt u de aan die toepassing gekoppelde verzoeken gedurende een bepaalde periode verder beperken.

Toepassingen zijn onder andere:

* ANALYSIS WORKSPACE UI
* Workspace-projecten
* Report Builder
* Builder-gebruikersinterface: Segment, Berekende afmetingen, Annotaties, Soorten publiek, enzovoort.
* API-aanroepen vanuit de 2.0-API
* Waarschuwingen
* Volledige tabelexport
* Delen met koppelingen van anderen
* Analyse met instructies
* Een andere toepassing die de Analyse meldend motor vraagt

Aanvragen door toepassing annuleren:

1. Ga in Customer Journey Analytics naar **[!UICONTROL Tools]** > **[!UICONTROL Reporting Activity Manager]** .

1. Selecteer de verbinding waar u rapportageaanvragen wilt annuleren. <!--double-check this step-->

   Voor meer informatie over de gegevens beschikbaar op deze pagina, zie [ Mening rapporterend activiteit in de Manager van de Activiteit van de Rapportering ](/help/reporting-activity-manager/reporting-activity.md).

1. Selecteer het [!UICONTROL **lusje van Toepassingen**], dan selecteer één of meerdere toepassingen.

   <!-- add screenshot -->

1. Selecteer [!UICONTROL **annuleert verzoeken**].

   [!UICONTROL **annuleert _x_ rapportverzoeken van x projecten**] vertoningen van de dialoogdoos.

1. In het veld Bericht van annulering wordt het bericht weergegeven dat aan gebruikers wordt weergegeven wanneer hun aanvragen worden geannuleerd. Er wordt een standaardbericht weergegeven. U kunt het standaardbericht bijwerken voor meer informatie.

1. (Optioneel) Toekomstige verzoeken voor een bepaalde periode beperken:

   1. Laat de optie toe om [!UICONTROL **verdere verzoeken**] te beperken

      ![ annuleert 1 verzoek die de Beperk verdere verzoeken door geselecteerde toepassing tonen.](assets/restrict-subsequent-requests-application.png)

   1. Kies een van de volgende opties:

      | Optie | Functie |
      |---------|----------|
      | [!UICONTROL **Gebruiker &amp; project**] | De geselecteerde toepassingen zullen tijdelijk van om het even welke rapporteringsverzoeken worden beperkt die door de bijbehorende gebruikers en de projecten worden gemaakt.<p>Dit is de minst beperkende optie.</p> |
      | [!UICONTROL **Gebruiker**] | Gebruikers die bij de geselecteerde toepassingen horen, kunnen geen rapportageaanvragen indienen. |
      | [!UICONTROL **Project**] | De projecten verbonden aan de geselecteerde toepassingen zullen van om het even welke rapporteringsverzoeken worden beperkt die door om het even welke gebruiker worden gemaakt. |
      | [!UICONTROL **Beperkt voor**] | Kies hoe lang aanvragen worden beperkt. U kunt 1 minuut (standaard), 5 minuten, 10 minuten, 15 minuten of 30 minuten kiezen. <!--double-check this--> <p>U kunt een beperking niet eerder verwijderen nadat deze is ingesteld.</p> |

      {style="table-layout:auto"}

1. Selecteer [!UICONTROL **verdergaan met annulering**].

   Er wordt een melding weergegeven in de toepassing (bijvoorbeeld in Analysis Workspace) om gebruikers te laten weten dat het verzoek is geannuleerd. Voor meer informatie over hoe dit in Analysis Workspace verschijnt, zie [ Ervaring wanneer de gebruikers tot een geannuleerd rapport ](#experience-when-users-access-a-cancelled-report) toegang hebben.

## Ervaring wanneer de gebruikers tot een geannuleerd rapport toegang hebben

In Analysis Workspace zien gebruikers de volgende berichten wanneer ze proberen toegang te krijgen tot een rapport of visualisatie die wordt beïnvloed door een annulering:

### Bericht over het project

Wanneer de gebruikers proberen om tot een project toegang te hebben dat door een annulering wordt beïnvloed, zien zij een bericht die hen informeren dat het rapport tijdelijk beperkt is:

![ het annuleringsbericht van het Project ](assets/workspace-canceled-report.png)

### Bericht over de visualisatie

Wanneer gebruikers proberen om tot een visualisatie toegang te hebben die door een annulering wordt beïnvloed, zien zij een bericht die hen informeren dat de gegevensverwerking voor het rapport tijdelijk beperkt is:

![ het annuleringsbericht van de Visualisatie ](assets/workspace-cancelled-visualization.png)
