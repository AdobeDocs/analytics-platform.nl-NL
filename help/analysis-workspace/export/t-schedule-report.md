---
description: Leer hoe u een Analysis Workspace-project rechtstreeks of volgens een planning voor e-maillevering verzendt.
keywords: Analysis Workspace
title: Projecten verzenden en plannen
feature: Curate and Share
mini-toc-levels: 3
exl-id: 36b5133a-2cd3-4cf1-a6fa-93a02dba276a
role: User
source-git-commit: c91ee21a3d4e20e3bdaeb75f2011ede6eee6cba0
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# Projecten verzenden en plannen

U kunt Customer Journey Analytics-projecten als bestanden via e-mail naar geselecteerde gebruikers verzenden. U kunt ad hoc dossiers verzenden, of u kunt projecten vormen om op een programma worden verzonden. Projecten kunnen in CSV- of PDF-indeling worden verzonden.

Alle tags die op het project zijn toegepast, worden automatisch toegepast op het exporteren.

Andere methodes om de gegevens van Customer Journey Analytics uit te voeren zijn ook beschikbaar, zoals die in [ wordt beschreven Overzicht van de Uitvoer ](/help/analysis-workspace/export/export-project-overview.md).

![ verzend dossier ](assets/send-file.png)

## Bestand verzenden

Een bestand via e-mail naar ontvangers verzenden:

1. Selecteer **[!UICONTROL Share]>[!UICONTROL Send file]** .
1. Geef het bestandstype op:
   * [!UICONTROL **CSV**]: Kies deze optie als u onbewerkte-tekstgegevens wilt.
   * [!UICONTROL **PDF**]: Kies deze optie als u het gedownloade dossier alle getoonde (zichtbare) lijsten en visualisaties in het project wilt bevatten.
1. (Optioneel) Gebruik **[!UICONTROL Description]** om een beschrijving toe te voegen die u in de e-mail wilt opnemen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. (Slechts voor de klanten van het Schild van de Gezondheidszorg) verstrek een wachtwoord aan [ wachtwoord-beschermt een gepland rapport ](#password-protect-a-new-scheduled-project).
1. (Facultatief) selecteer **[!UICONTROL Show scheduling options]** om [ een dossieruitvoer ](#schedule-file-export) te plannen.
1. Klik op **[!UICONTROL Send Now]**. Selecteer **[!UICONTROL Cancel]** om te annuleren.


## Bestanden exporteren plannen {#schedule}

Een bestand volgens een schema per e-mail naar ontvangers verzenden

1. Selecteer **[!UICONTROL Share]>[!UICONTROL Schedule file export]** .
1. Geef het bestandstype op:
   * [!UICONTROL **CSV**]: Kies deze optie als u onbewerkte-tekstgegevens wilt.
   * [!UICONTROL **PDF**]: Kies deze optie als u het gedownloade dossier alle getoonde (zichtbare) lijsten en visualisaties in het project wilt bevatten.
1. (Optioneel) Gebruik **[!UICONTROL Description]** om een beschrijving toe te voegen die u in de e-mail wilt opnemen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. (Slechts voor de klanten van het Schild van de Gezondheidszorg) verstrek een wachtwoord aan [ wachtwoord-beschermt een gepland rapport ](#password-protect-a-new-scheduled-project).
1. Zorg ervoor dat **[!UICONTROL Show scheduling options]** is geselecteerd.
1. Selecteer een **[!UICONTROL Frequency]** . U kunt kiezen tussen:

   | Frequentie | Opties |
   |---|---|
   | **[!UICONTROL Send hourly]** | Voer een waarde in voor **[!UICONTROL Send every number of hours]** . |
   | **[!UICONTROL Send daily]** | Selecteer een **[!UICONTROL Daily frequency]**: **[!UICONTROL Send every day]**, **[!UICONTROL Send every weekday]** of **[!UICONTROL Custom frequency]** .<br/> Als u **[!UICONTROL Custom frequency]** selecteert, ga een waarde voor **[!UICONTROL Send every number of days]** in. |
   | **[!UICONTROL Send weekly]** | Voer een waarde in voor **[!UICONTROL Send every number of weeks]** . Selecteer een **[!UICONTROL Day of week]** . |
   | **[!UICONTROL Send monthly by day of the week]** | Selecteer een **[!UICONTROL Day of week]** en een **[!UICONTROL Week of month]** . |
   | **[!UICONTROL Send monthly by day of the month]** | Selecteer een waarde in **[!UICONTROL Send on this day of the month]** . |
   | **[!UICONTROL Send yearly by day of the month]** | Selecteer een **[!UICONTROL Day of week]** , selecteer een **[!UICONTROL Week of month]** en selecteer een **[!UICONTROL Monthly of year]** . |
   | **[!UICONTROL Send yearly by specific date]** | Selecteer een **[!UICONTROL Month of year]** en selecteer een waarde in **[!UICONTROL Send on this day of the month]** . |

1. Voer een begindatum in in **[!UICONTROL Starting on]** . Alternatief, selecteer ![ Kalender ](/help/assets/icons/Calendar.svg) om een begindatum van de kalender te kiezen.

1. Voer een einddatum in in **[!UICONTROL Ending on]** . Alternatief, selecteer ![ Kalender ](/help/assets/icons/Calendar.svg) om een einddatum van de kalender te kiezen.
1. Selecteer **[!UICONTROL Send on schedule]** . Selecteer **[!UICONTROL Cancel]** om te annuleren.


## Wachtwoord-beschermt een gepland project {#password}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_sendfile_password"
>title="Wachtwoordversleuteling"
>abstract="Het opgegeven wachtwoord wordt gebruikt om het bestand voor het geplande project te coderen. De beveiligingsvereisten voor uw organisatie vereisen wachtwoordversleuteling."

<!-- markdownlint-enable MD034 -->


>[!NOTE]
>
>De optie om een gepland project te wachtwoord-beschermen verschijnt slechts voor de klanten van Customer Journey Analytics die het ](https://business.adobe.com/solutions/industries/healthcare.html) toe:voegen-op product van het Schild van de Gezondheidszorg [ hebben gekocht.

Adobe gebruikt het wachtwoord om geplande projecten te coderen, of zij in .pdf of .csv formaten worden verzonden.

Nadat uw bedrijf SKU van het Schild van de Gezondheidszorg heeft gekocht en voor het is toegelaten, wordt de herinnering om een wachtwoord voor een gepland project tot stand te brengen getoond in de volgende omstandigheden:

* Wanneer iemand een nieuw gepland project maakt.

* Wanneer een bestaand gepland project op het punt staat te worden verzonden. Het momenteel geplande project is uitgeschakeld totdat wachtwoordbeveiliging is ingesteld. De eigenaar van het geplande project ontvangt een e-mail met informatie over deze vereiste.

### Wachtwoordvereisten

De wachtwoordvereisten voldoen aan de Adobe-standaarden, die minimaal 8 tekens vereisen met ten minste één getal en één speciaal teken.

### Wachtwoord-beschermt een nieuw gepland project

1. Nadat u het project hebt opgeslagen, gaat u naar **[!UICONTROL Share]** > **[!UICONTROL Send file now]** of **[!UICONTROL Share]** > **[!UICONTROL Send file on schedule]** .
1. Volg de instructies hierboven, onder [ verzenden nu dossier ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/export/t-schedule-report.html#now) of [ verzenden dossier op programma ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/export/t-schedule-report.html#schedule).

### Wachtwoord-beschermt een bestaand gepland project

Wanneer u wachtwoord-beschermt een bestaand gepland project, ontvangt de projecteigenaar een e-mail gelijkend op dit:

![ het e-mailbericht dat van Customer Journey Analytics wachtwoordencryptie aangeeft wordt vereist voor uw organisatie.](assets/email-password.png)

1. Meld u aan bij Customer Journey Analytics.
1. Selecteer **[!UICONTROL View Scheduled Project]** .
1. Voer in het dialoogvenster **[!UICONTROL Edit scheduled project]** een wachtwoord in en voer het opnieuw in.
1. Laat de ontvangers van het geplande project over dit wachtwoord weten. Het wachtwoord niet verspreiden onder personen die geen ontvangers zijn van het geplande project.



## Geplande projectmanager {#manager}

Geplande Analysis Workspace-projecten kunnen worden beheerd vanuit de hoofdinterface via **[!UICONTROL Components]** > **[!UICONTROL Scheduled Projects]** . Voor meer informatie, zie [ Geplande projecten ](/help/components/scheduled-projects-manager.md).
