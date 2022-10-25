---
description: Een Analysis Workspace-project verzenden via e-mail of het plannen voor levering.
keywords: Analysis Workspace
title: Projecten plannen
feature: Curate and Share
mini-toc-levels: 3
exl-id: 36b5133a-2cd3-4cf1-a6fa-93a02dba276a
source-git-commit: eba2eb71ca434e0306c018b80209caf52266ee15
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# Projecten plannen

Vanuit de werkruimte **Menu Delen**, kunt u Analysis Workspace-projecten via e-mail naar geselecteerde ontvangers verzenden. Bestanden kunnen in CSV- of PDF-indeling worden verzonden.

## Bestand nu verzenden {#now}

Een bestand direct via e-mail naar ontvangers verzenden:

1. Klikken **Delen > Bestand nu verzenden**.
1. Geef het bestandstype op (CSV of PDF).
1. (Optioneel) Voeg een beschrijving toe die in de e-mail wordt opgenomen om uit te leggen welk bestand wordt ontvangen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. (Alleen voor klanten van het gezondheidsschild) Geef een wachtwoord op. Zie de sectie Wachtwoord-beschermt een gepland rapport.
1. Klikken **Nu verzenden**.
1. (Optioneel) Klik op **Planningsopties tonen** om een leveringsschema op te geven.

![Bestand nu verzenden](assets/send-file-no-scheduling-options.JPG)

## Bestand verzenden volgens schema {#schedule}

Een bestand volgens een terugkerend schema via e-mail naar ontvangers verzenden:

1. Klikken **Delen > Bestand verzenden volgens schema**.
1. Geef het bestandstype op (CSV of PDF).
1. (Optioneel) Voeg een beschrijving toe die in de e-mail wordt opgenomen om uit te leggen welk bestand wordt ontvangen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. (Alleen voor klanten van het gezondheidsschild) Geef een wachtwoord op. Zie de sectie Wachtwoord-beschermt een gepland rapport.
1. Geef het bereik op waarover de planning moet worden geleverd door Starten op en Eindigen op de invoer te wijzigen. De einddatum moet binnen een jaar zijn vanaf de dag dat het schema wordt opgesteld of gewijzigd.
1. Geef de leveringsfrequentie op. Elke frequentie maakt verschillende aanpassingen mogelijk.
1. Klikken **Verzenden volgens schema**.

![](assets/send-file.JPG)

## Geplande projectmanager {#manager}

Geplande Analysis Workspace-projecten kunnen worden beheerd in het kader van **Analyse > Componenten > Geplande projecten**.

In de Geplande Manager van Projecten, kunt u terugkomende projectprogramma&#39;s uitgeven en schrappen. Zoek naar een programma in de onderzoeksbar of door de filteropties in het linkerspoor te gebruiken. U kunt filteren op tag, goedgekeurde schema&#39;s, eigenaars en meer.

Het volgende is gemeenschappelijke acties in de Geplande Manager van Projecten:

| Handeling | Beschrijving |
|---|---|
| **Tijdschema bewerken** | Klik op de titel van de planning om de leveringsinstellingen bij te werken. |
| **Schema verwijderen** | Selecteer het geplande project in de lijst en klik dan Schrapping van het menu. Hiermee verwijdert u het geselecteerde schema voor het project. het project zelf wordt niet verwijderd . |
| **Tags toevoegen** | Selecteer het geplande project in de lijst en kies &quot;Tag&quot; of &quot;Goedkeuren&quot; om uw schema&#39;s te ordenen en ze gemakkelijker te maken om naar te zoeken. |
| **Ontbroken schema&#39;s weergeven** | Navigeer naar de linkertrack > Overige filters > Kan geen mislukte planningen zien. |
| **Verlopen schema&#39;s weergeven** | Navigeer naar de linkerrail > Andere filters > Verlopen om programma&#39;s te zien die zijn verlopen. Klik de titel van het programma aan opstelling een nieuw leveringsprogramma. |
| **Plan-id weergeven** | Navigeer naar kolomopties rechtsboven en voeg de kolom Id van planning toe aan de tabel. De geplande id is vaak handig voor foutopsporing. |

De Geplande Manager van Projecten toont de punten die een specifieke gebruiker heeft gecreeerd. Als de gebruikersaccount in de toepassing is uitgeschakeld, worden alle geplande leveringen gestopt.

## Wachtwoord-beschermt een gepland project {#password}

>[!NOTE]
>
>De optie om een gepland project met een wachtwoord te beveiligen wordt alleen weergegeven voor CJA-klanten die de [Gezondheidsschild](https://experienceleague.adobe.com/docs/blueprints-learn/architecture/vertical-blueprints/healthcare-vertical.html%3Flang%3Den) add-on product.

Adobe gebruikt het wachtwoord om geplande projecten te coderen, of zij in .pdf of .csv formaten worden verzonden.

Nadat uw bedrijf de SKU van het Schild van de Gezondheidszorg heeft gekocht en voor het is toegelaten, verschijnt de vraag om een wachtwoord voor een gepland project tot stand te brengen onder twee omstandigheden:

* Wanneer iemand een nieuw gepland project maakt.

* Wanneer een bestaand gepland project op het punt staat te worden verzonden. Het momenteel geplande project wordt uitgeschakeld totdat wachtwoordbeveiliging is ingesteld. De eigenaar van het geplande project ontvangt een e-mail met dit doel.

![wachtwoordbeveiliging](assets/password.png)

### Wachtwoordvereisten

De wachtwoordvereisten voldoen aan de Adobe-standaard, die minimaal 8 tekens vereist met ten minste één getal en één speciaal teken.

### Nieuw gepland project

1. Nadat u het project hebt opgeslagen, gaat u naar Delen > Bestand nu verzenden of Delen > Bestand op schema verzenden.
1. Volg de bovenstaande instructies onder Bestand nu delen of Bestand delen volgens schema.

### Bestaand gepland project

Vóór de tijd waarvoor een project gepland is, zal de eigenaar van het project een e-mail gelijkaardig aan dit ontvangen:

![email](assets/email-password.png)

1. Klik op **[!UICONTROL View Scheduled Project]**.
1. In de **[!UICONTROL Edit scheduled project]** voert u een wachtwoord in en voert u dit opnieuw in.
1. (Slechts) de ontvangers van het geplande project weten over dit wachtwoord.


