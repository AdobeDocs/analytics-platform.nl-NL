---
description: Een Analysis Workspace-project per e-mail verzenden of het plannen voor levering.
keywords: Analysis Workspace
title: Gegevens van Customer Journey Analytics naar anderen verzenden per e-mail
feature: Curate and Share
mini-toc-levels: 3
exl-id: 36b5133a-2cd3-4cf1-a6fa-93a02dba276a
source-git-commit: 16f1a732260ace8393d7303134fc351740fd1661
workflow-type: tm+mt
source-wordcount: '969'
ht-degree: 0%

---

# Gegevens van Customer Journey Analytics naar anderen verzenden via e-mail

U kunt rapporten van de Customer Journey Analytics uitvoeren door het naar geselecteerde ontvangers door e-mail te verzenden. U kunt bestanden ad hoc verzenden of u kunt bestanden configureren voor verzending volgens een schema. Bestanden kunnen in CSV- of PDF-indeling worden verzonden.

Alle tags die op het project zijn toegepast, worden automatisch toegepast op het exporteren.

Er zijn ook andere methoden beschikbaar voor het exporteren van gegevens van Customers Journey Analytics, zoals beschreven in [Overzicht van exporteren](/help/analysis-workspace/export/export-project-overview.md).

## Bestand nu verzenden {#now}

Een bestand direct per e-mail naar ontvangers verzenden:

1. Klik op **[!UICONTROL Share]>[!UICONTROL Export file]**.
1. Geef het bestandstype op:
   * [!UICONTROL **CSV**]: Kies deze optie als u gegevens in onbewerkte tekst wilt.
   * [!UICONTROL **PDF**]: Kies deze optie als het gedownloade bestand alle weergegeven (zichtbare) tabellen en visualisaties in het project moet bevatten.
1. (Optioneel) Voeg een beschrijving toe die u in de e-mail wilt opnemen om uit te leggen welk bestand wordt ontvangen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. (Alleen voor klanten van het gezondheidsschild) Geef een wachtwoord op. Zie de sectie Wachtwoord-beschermt een gepland rapport.
1. (Optioneel) Klik op **[!UICONTROL Show scheduling options]** om een leveringsschema op te geven.
1. Klik op **[!UICONTROL Send Now]**.

![Het venster Bestand verzenden en de knop Nu verzenden.](assets/send-file-no-scheduling-options.JPG)

## Bestand verzenden volgens schema {#schedule}

Een bestand volgens een terugkerend schema per e-mail naar ontvangers verzenden:

1. Klik op **[!UICONTROL Share]>[!UICONTROL Schedule file export]**.
1. Geef het bestandstype op (CSV of PDF).
1. (Optioneel) Voeg een beschrijving toe die in de e-mail wordt opgenomen om uit te leggen welk bestand wordt ontvangen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. (Alleen voor klanten van het gezondheidsschild) Geef een wachtwoord op. Zie de sectie Wachtwoord-beschermt een gepland rapport.
1. Geef het bereik op waarover de planning moet worden geleverd door Starten op en Eindigen op de invoer te wijzigen. De einddatum moet binnen een jaar zijn vanaf de dag dat het schema wordt opgesteld of gewijzigd.
1. Geef de leveringsfrequentie op. Elke frequentie maakt verschillende aanpassingen mogelijk.
1. Klik op **[!UICONTROL Send on schedule]**.

![Het venster Bestand verzenden en de planningsopties worden weergegeven om de instellingen voor Starten, Einden op datums en dagelijkse frequentie weer te geven.](assets/send-file.JPG)

## Geplande projectmanager {#manager}

Geplande Analysis Workspace-projecten kunnen worden beheerd onder **[!UICONTROL Analytics]> [!UICONTROL Components] >[!UICONTROL Scheduled Projects]**.

In de Geplande Manager van Projecten, kunt u terugkomende projectprogramma&#39;s uitgeven en schrappen. Zoek naar een programma in de onderzoeksbar of door de filteropties in het linkerspoor te gebruiken. U kunt filteren op tag, goedgekeurde schema&#39;s, eigenaars en meer.

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
| **[!UICONTROL View failed schedules]** | Navigeer naar de linkertrack > Overige filters > Kan geen mislukte planningen zien. |
| **[!UICONTROL View expired schedules]** | Navigeer naar de linkerrail > Andere filters > Verlopen om programma&#39;s te zien die zijn verlopen. Klik de titel van het programma aan opstelling een nieuw leveringsprogramma. |
| **[!UICONTROL View schedule ID]** | Navigeer naar kolomopties rechtsboven en voeg de kolom Id van planning toe aan de tabel. De geplande id is vaak handig voor foutopsporing. |

De Geplande Manager van Projecten toont de punten die een specifieke gebruiker heeft gecreeerd. Als de gebruikersaccount in de toepassing is uitgeschakeld, worden alle geplande leveringen gestopt.
Zie voor meer informatie [Geplande projecten](/help/components/scheduled-projects-manager.md).

## Wachtwoord-beschermt een gepland project {#password}

>[!NOTE]
>
>De optie om een gepland project met een wachtwoord te beveiligen wordt alleen weergegeven voor klanten van Customers Journey Analytics die de [Gezondheidsschild](https://business.adobe.com/solutions/experience-cloud-for-healthcare.html) add-on product.

De Adobe gebruikt het wachtwoord om geplande projecten te coderen, of zij in .pdf of .csv formaten worden verzonden.

Nadat uw bedrijf SKU van het Schild van de Gezondheidszorg heeft gekocht en voor het is toegelaten, wordt de herinnering om een wachtwoord voor een gepland project tot stand te brengen getoond in de volgende omstandigheden:

* Wanneer iemand een nieuw gepland project maakt.

* Wanneer een bestaand gepland project op het punt staat te worden verzonden. Het momenteel geplande project is uitgeschakeld totdat wachtwoordbeveiliging is ingesteld. De eigenaar van het geplande project ontvangt een e-mail met informatie over deze vereiste.

![Het bericht voor geplande projectvensters bewerken en wachtwoordversleuteling die aangeeft dat uw organisatie wachtwoordversleuteling nodig heeft.](assets/password.png)

### Wachtwoordvereisten

De wachtwoordvereisten voldoen aan de normen voor Adobe, waarbij minimaal 8 tekens vereist zijn met ten minste één getal en één speciaal teken.

### Wachtwoord-beschermt een nieuw gepland project

1. Nadat u uw project hebt opgeslagen, gaat u naar **[!UICONTROL Share]** > **[!UICONTROL Send file now]**, of **[!UICONTROL Share]** > **[!UICONTROL Send file on schedule]**.
1. Volg de bovenstaande instructies onder [Bestand nu verzenden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/curate-share/t-schedule-report.html#now) of [Bestand verzenden volgens schema](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/curate-share/t-schedule-report.html#schedule).

### Wachtwoord-beschermt een bestaand gepland project

Voordat een project wordt gepland, ontvangt de eigenaar van het project een e-mail die hierop lijkt:

![De e-mailmelding van de Customer Journey Analytics waarin wachtwoordversleuteling wordt aangegeven, is vereist voor uw organisatie.](assets/email-password.png)

1. Meld u aan bij de Customer Journey Analytics.
1. Selecteren **[!UICONTROL View Scheduled Project]**.
1. In de **[!UICONTROL Edit scheduled project]** voert u een wachtwoord in en voert u dit opnieuw in.
1. Laat de ontvangers van het geplande project over dit wachtwoord weten. Het wachtwoord niet verspreiden onder personen die geen ontvangers zijn van het geplande project.
