---
description: Een Analysis Workspace-project verzenden via e-mail of het plannen voor levering.
keywords: Analysis Workspace
title: Projecten plannen
feature: Curate and Share
mini-toc-levels: 3
exl-id: 36b5133a-2cd3-4cf1-a6fa-93a02dba276a
source-git-commit: 6f3ae14e4d34de17ed64ae30cee4611e4d6f3226
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 1%

---

# Projecten plannen

Vanuit de werkruimte **[!UICONTROL Share]** kunt u Analysis Workspace-projecten via e-mail naar geselecteerde ontvangers verzenden. Bestanden kunnen in CSV- of PDF-indeling worden verzonden.

## Bestand nu verzenden {#now}

Een bestand direct via e-mail naar ontvangers verzenden:

1. Klik op **[!UICONTROL Share]>[!UICONTROL Export file]**.
1. Geef het bestandstype op:
   * [!UICONTROL **CSV**]: Kies deze optie als u gegevens in onbewerkte tekst wilt.
   * [!UICONTROL **PDF**]: Kies deze optie als het gedownloade bestand alle weergegeven (zichtbare) tabellen en visualisaties in het project moet bevatten.
1. (Optioneel) Voeg een beschrijving toe die u in de e-mail wilt opnemen om uit te leggen welk bestand wordt ontvangen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. (Alleen voor klanten van het gezondheidsschild) Geef een wachtwoord op. Zie de sectie Wachtwoord-beschermt een gepland rapport.
1. Klik op **[!UICONTROL Send Now]**.
1. (Optioneel) Klik op **[!UICONTROL Show scheduling options]** om een leveringsschema op te geven.

![Bestand nu verzenden](assets/send-file-no-scheduling-options.JPG)

## Bestand verzenden volgens schema {#schedule}

Een bestand volgens een terugkerend schema via e-mail naar ontvangers verzenden:

1. Klik op **[!UICONTROL Share]>[!UICONTROL Schedule file export]**.
1. Geef het bestandstype op (CSV of PDF).
1. (Optioneel) Voeg een beschrijving toe die in de e-mail wordt opgenomen om uit te leggen welk bestand wordt ontvangen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. (Alleen voor klanten van het gezondheidsschild) Geef een wachtwoord op. Zie de sectie Wachtwoord-beschermt een gepland rapport.
1. Geef het bereik op waarover de planning moet worden geleverd door Starten op en Eindigen op de invoer te wijzigen. De einddatum moet binnen een jaar zijn vanaf de dag dat het schema wordt opgesteld of gewijzigd.
1. Geef de leveringsfrequentie op. Elke frequentie maakt verschillende aanpassingen mogelijk.
1. Klik op **[!UICONTROL Send on schedule]**.

![](assets/send-file.JPG)

## Geplande projectmanager {#manager}

Geplande Analysis Workspace-projecten kunnen worden beheerd onder **[!UICONTROL Analytics]> [!UICONTROL Components] >[!UICONTROL Scheduled Projects]**.

Zie voor meer informatie [Geplande projecten](/help/components/scheduled-projects-manager.md)

## Wachtwoord-beschermt een gepland project {#password}

>[!NOTE]
>
>De optie om een gepland project met een wachtwoord te beveiligen wordt alleen weergegeven voor klanten van Customers Journey Analytics die de [Gezondheidsschild](https://business.adobe.com/solutions/experience-cloud-for-healthcare.html) add-on product.

De Adobe gebruikt het wachtwoord om geplande projecten te coderen, of zij in .pdf of .csv formaten worden verzonden.

Nadat uw bedrijf de SKU van het Schild van de Gezondheidszorg heeft gekocht en voor het is toegelaten, verschijnt de vraag om een wachtwoord voor een gepland project tot stand te brengen onder twee omstandigheden:

* Wanneer iemand een nieuw gepland project maakt.

* Wanneer een bestaand gepland project op het punt staat te worden verzonden. Het momenteel geplande project wordt uitgeschakeld totdat wachtwoordbeveiliging is ingesteld. De eigenaar van het geplande project ontvangt een e-mail met dit doel.

![wachtwoordbeveiliging](assets/password.png)

### Wachtwoordvereisten

De wachtwoordvereisten voldoen aan de standaard voor Adobe, die minimaal 8 tekens vereist met ten minste één getal en één speciaal teken.

### Wachtwoord-beschermt een nieuw gepland project

1. Nadat u uw project hebt opgeslagen, ga naar **[!UICONTROL Share]** > **[!UICONTROL Send file now]**, of [!UICONTROL Share] > **[!UICONTROL Send file on schedule]**.
1. Volg de bovenstaande instructies onder [Bestand nu verzenden](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/curate-share/t-schedule-report.html#now) of [Bestand verzenden volgens schema](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/curate-share/t-schedule-report.html#schedule).

### Wachtwoord-beschermt een bestaand gepland project

Vóór de tijd waarvoor een project gepland is, zal de eigenaar van het project een e-mail gelijkaardig aan dit ontvangen:

![email](assets/email-password.png)

1. Log terug in de Customer Journey Analytics.
1. Klik op **[!UICONTROL View Scheduled Project]**.
1. In de **[!UICONTROL Edit scheduled project]** voert u een wachtwoord in en voert u dit opnieuw in.
1. (Slechts) de ontvangers van het geplande project weten over dit wachtwoord.


