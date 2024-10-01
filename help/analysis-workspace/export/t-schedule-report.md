---
description: Een Analysis Workspace-project per e-mail verzenden of het plannen voor levering.
keywords: Analysis Workspace
title: Rapporten per e-mail naar anderen verzenden
feature: Curate and Share
mini-toc-levels: 3
exl-id: 36b5133a-2cd3-4cf1-a6fa-93a02dba276a
role: User
source-git-commit: 388e008f4ee092dd8224bfacd020cdf762d4fb82
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Bestanden naar anderen verzenden

U kunt rapporten van de Customer Journey Analytics als dossiers naar geselecteerde gebruikers per e-mail verzenden. U kunt bestanden ad hoc verzenden of u kunt bestanden configureren voor verzending volgens een schema. Bestanden kunnen in CSV- of PDF-indeling worden verzonden.

Alle tags die op het project zijn toegepast, worden automatisch toegepast op het exporteren.

Andere methodes om de gegevens van de Customer Journey Analytics uit te voeren zijn ook beschikbaar, zoals die in [ overzicht van de Uitvoer ](/help/analysis-workspace/export/export-project-overview.md) wordt beschreven.

## Bestand nu verzenden {#now}

Een bestand direct per e-mail naar ontvangers verzenden:

1. Klik op **[!UICONTROL Share]>[!UICONTROL Export file]** .
1. Geef het bestandstype op:
   * [!UICONTROL **CSV**]: Kies deze optie als u onbewerkte-tekstgegevens wilt.
   * [!UICONTROL **PDF**]: Kies deze optie als u het gedownloade dossier alle getoonde (zichtbare) lijsten en visualisaties in het project wilt bevatten.
1. (Optioneel) Voeg een beschrijving toe die u in de e-mail wilt opnemen om uit te leggen welk bestand wordt ontvangen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. (Alleen voor klanten van het gezondheidsschild) Geef een wachtwoord op. Zie de sectie Wachtwoord-beschermt een gepland rapport.
1. (Optioneel) Klik op **[!UICONTROL Show scheduling options]** om een leveringsschema op te geven.
1. Klik op **[!UICONTROL Send Now]**.

![ het Send dossiervenster en verzendt nu knoop.](assets/send-file-no-scheduling-options.JPG)

## Bestand verzenden volgens schema {#schedule}

Een bestand volgens een terugkerend schema per e-mail naar ontvangers verzenden:

1. Klik op **[!UICONTROL Share]>[!UICONTROL Schedule file export]** .
1. Geef het bestandstype op (CSV of PDF).
1. (Optioneel) Voeg een beschrijving toe die in de e-mail wordt opgenomen om uit te leggen welk bestand wordt ontvangen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. (Alleen voor klanten van het gezondheidsschild) Geef een wachtwoord op. Zie de sectie Wachtwoord-beschermt een gepland rapport.
1. Geef het bereik op waarover de planning moet worden geleverd door Starten op en Eindigen op de invoer te wijzigen. De einddatum moet binnen een jaar zijn vanaf de dag dat het schema wordt opgesteld of gewijzigd.
1. Geef de leveringsfrequentie op. Elke frequentie maakt verschillende aanpassingen mogelijk.
1. Klik op **[!UICONTROL Send on schedule]**.

![ het Send dossiervenster en het plannen opties die worden getoond om het Beginnen, het Eindigen op data, en de dagelijkse frequentiemontages te tonen.](assets/send-file.JPG)

## Geplande projectmanager {#manager}

Geplande Analysis Workspace-projecten kunnen worden beheerd via **[!UICONTROL Analytics]> [!UICONTROL Components] >[!UICONTROL Scheduled Projects]** .

In de Geplande Manager van Projecten, kunt u terugkomende projectprogramma&#39;s uitgeven en schrappen. Zoek naar een programma in de onderzoeksbar of door de filteropties in het linkerpaneel te gebruiken. U kunt filteren op tag, goedgekeurde schema&#39;s, eigenaars en meer.

| Veld | Beschrijving |
| --- | --- |
| [!UICONTROL Favorites] | Als u het sterpictogram selecteert, wordt dit schema een favoriet. |
| [!UICONTROL Schedule ID] | Deze id wordt vooral gebruikt voor foutopsporingsdoeleinden. |
| [!UICONTROL Title and Description] | Titel en beschrijving van dit project. |
| [!UICONTROL Owner] | De persoon die het project heeft gemaakt en bezit. |
| [!UICONTROL Tags] | (facultatief) het etiketteren is een goede manier om projecten te organiseren. Alle gebruikers kunnen labels maken en een of meer tags toepassen op een project. U kunt echter alleen labels zien voor de projecten die u hebt of die met u zijn gedeeld. |
| [!UICONTROL Delivered To] | De ontvanger(s) van dit geplande project. |
| [!UICONTROL Expiration Date] | U kunt de vervaldatum instellen op maximaal één jaar, ongeacht de frequentie van de planning. |
| [!UICONTROL Frequency] | Hoe vaak wilt u dat dit planningsproject naar de ontvanger(s) wordt verzonden. |
| [!UICONTROL Execution Time] | Op welk tijdstip van de dag dit geplande project wordt verzonden. |
| [!UICONTROL Number of Queries] | Het aantal vragen tegen dit project. |

Het volgende is gemeenschappelijke acties in de Geplande Manager van Projecten:

| Handeling | Beschrijving |
|---|---|
| **[!UICONTROL Edit schedule]** | Klik op de titel van de planning om de leveringsinstellingen bij te werken. |
| **[!UICONTROL Delete schedule]** | Selecteer het geplande project in de lijst en klik dan Schrapping van het menu. Hiermee verwijdert u het geselecteerde schema voor het project. Het project zelf wordt niet verwijderd. |
| **[!UICONTROL Add tags]** | Selecteer het geplande project in de lijst en kies &quot;Tag&quot; of &quot;Goedkeuren&quot; om uw schema&#39;s te ordenen en ze gemakkelijker te maken om naar te zoeken. |
| **[!UICONTROL View failed schedules]** | Navigeer naar het linkerdeelvenster > Overige filters > Kan de mislukte planningen niet zien. |
| **[!UICONTROL View expired schedules]** | Navigeer naar het linkerdeelvenster > Andere filters > Verlopen om de verlopen programma&#39;s te zien. Klik de titel van het programma aan opstelling een nieuw leveringsprogramma. |
| **[!UICONTROL View schedule ID]** | Navigeer naar kolomopties rechtsboven en voeg de kolom Id van planning toe aan de tabel. De geplande id is vaak handig voor foutopsporing. |

De Geplande Manager van Projecten toont de punten die een specifieke gebruiker heeft gecreeerd. Als de gebruikersaccount in de toepassing is uitgeschakeld, worden alle geplande leveringen gestopt.
Voor meer informatie, zie [ Geplande projecten ](/help/components/scheduled-projects-manager.md).

## Wachtwoord-beschermt een gepland project {#password}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_workspace_sendfile_password"
>title="Wachtwoordversleuteling"
>abstract="Het opgegeven wachtwoord wordt gebruikt om het bestand voor het geplande project te coderen. De beveiligingsvereisten voor uw organisatie vereisen wachtwoordversleuteling."

<!-- markdownlint-enable MD034 -->


>[!NOTE]
>
>De optie om een gepland project wachtwoord-te beschermen verschijnt slechts voor de klanten van de Customer Journey Analytics die het ](https://business.adobe.com/solutions/industries/healthcare.html) toe:voegen-op product van het Schild van de Gezondheidszorg van de 1} hebben gekocht.[

De Adobe gebruikt het wachtwoord om geplande projecten te coderen, of zij in .pdf of .csv formaten worden verzonden.

Nadat uw bedrijf SKU van het Schild van de Gezondheidszorg heeft gekocht en voor het is toegelaten, wordt de herinnering om een wachtwoord voor een gepland project tot stand te brengen getoond in de volgende omstandigheden:

* Wanneer iemand een nieuw gepland project maakt.

* Wanneer een bestaand gepland project op het punt staat te worden verzonden. Het momenteel geplande project is uitgeschakeld totdat wachtwoordbeveiliging is ingesteld. De eigenaar van het geplande project ontvangt een e-mail met informatie over deze vereiste.

![ geeft gepland projectvenster en wachtwoord encryptiebericht uit die uw organisatie wijzen vereisen wachtwoordencryptie.](assets/password.png)

### Wachtwoordvereisten

De wachtwoordvereisten voldoen aan de normen voor Adobe, waarbij minimaal 8 tekens vereist zijn met ten minste één getal en één speciaal teken.

### Wachtwoord-beschermt een nieuw gepland project

1. Nadat u het project hebt opgeslagen, gaat u naar **[!UICONTROL Share]** > **[!UICONTROL Send file now]** of **[!UICONTROL Share]** > **[!UICONTROL Send file on schedule]** .
1. Volg de instructies hierboven, onder [ verzenden nu dossier ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/curate-share/t-schedule-report.html#now) of [ verzenden dossier op programma ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/curate-share/t-schedule-report.html#schedule).

### Wachtwoord-beschermt een bestaand gepland project

Voordat een project wordt gepland, ontvangt de eigenaar van het project een e-mail die hierop lijkt:

![ het e-mailbericht dat van de Customer Journey Analytics op wachtwoordencryptie wijst wordt vereist voor uw organisatie.](assets/email-password.png)

1. Meld u aan bij de Customer Journey Analytics.
1. Selecteer **[!UICONTROL View Scheduled Project]** .
1. Voer in het dialoogvenster **[!UICONTROL Edit scheduled project]** een wachtwoord in en voer het opnieuw in.
1. Laat de ontvangers van het geplande project over dit wachtwoord weten. Het wachtwoord niet verspreiden onder personen die geen ontvangers zijn van het geplande project.
