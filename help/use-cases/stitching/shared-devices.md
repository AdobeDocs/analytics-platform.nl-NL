---
title: Gedeelde apparaten
description: Uitleg van hoe te om gedeelde apparaten te behandelen gebruikend het stitching en andere technieken.
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
role: Admin
exl-id: a7d14968-33a2-46a8-8e32-fb6716650d0a
source-git-commit: 9118a3c20158b1a0373fab1b41595aa7b07075f6
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Gedeelde apparaten

Dit artikel verstrekt context op gedeelde apparaten, hoe te om gegevens van gedeelde apparaten te behandelen en te verlichten gebruikend [ het stitching ](/help/stitching/overview.md), en gedeelde apparatenblootstelling in uw gegevens te begrijpen gebruikend de Dienst van de Vraag.

## Wat is een gedeeld apparaat?

Een gedeeld apparaat is een apparaat dat door meer dan één persoon wordt gebruikt. De gemeenschappelijke scenario&#39;s zijn apparaten zoals tabletten, apparaten die in kiosken worden gebruikt of computermateriaal dat door agenten in een vraagcentrum wordt gedeeld.

Wanneer twee personen hetzelfde apparaat gebruiken en beide een aankoop doen, kunnen voorbeeldgebeurtenisgegevens er als volgt uitzien:

| Gebeurtenis | Tijdstempel | Paginanaam | Apparaat-id | E-mail |
|--:|---|---|---|---|
| 1 | 2023-05-12 12:01 | Homepage | `1234` | |
| 2 | 2023-05-12 12:02 | Productpagina | `1234` | |
| 3 | 2023-05-12 12:03 | Volgorde succesvol | `1234` | `ryan@a.com` |
| 4 | 2023-05-12 12:07 | Productpagina | `1234` | |
| 5 | 2023-05-12 12:08 | Volgorde succesvol | `1234` | `cassidy@a.com` |

Zoals u uit deze lijst kunt zien, zodra de authentificatie op gebeurtenissen 3 en 5 gebeurt, begint een verbinding tussen apparaat identiteitskaart en een persoonidentiteitskaart te vormen. Om inzicht te krijgen in de impact van marketingactiviteiten op individueel niveau, moeten deze ongeoorloofde gebeurtenissen worden toegeschreven aan de juiste persoon.

<!--
The order success (purchase) events assign the data accurately to the correct email. How this assignment impacts your analysis depends on how you perform analysis:

- Device centric approach: analysis performed using the Device ID. With this approach, both authenticated and unauthenticated data are included in analysis. However, this approach does not allow for a more person based analysis. 
- Person centric approach: analysis performed using the email address or other person identifier. With this approach, only authenticated events are included in the analysis. This approach doesn't provide a complete picture of the customer journey, including acquisition

-->

## Centrische analyse van personen verbeteren

Het koppelingsproces verhelpt dit toewijzingsprobleem door de geselecteerde persoon-id (in de voorbeeldgegevens, de e-mail) toe te voegen aan gebeurtenissen waar die id niet bestaat. Het plaatsen hefboomwerkingen een afbeelding tussen Apparaat IDs en Persoon IDs om ervoor te zorgen dat zowel voor authentiek verklaard als niet voor authentiek verklaard verkeer in analyse kan worden gebruikt, die het persoon centric houdt. Zie [ het Plaatsen ](/help/stitching/overview.md) voor meer informatie.

Bij het instellen van tekenreeksen kunnen gedeelde apparaatgegevens worden toegewezen met de kenmerk last-auth of door het apparaat gesplitste kenmerk. Alle pogingen om niet-geverifieerde gebeurtenissen aan een bekende gebruiker te hechten zijn niet-deterministisch.


### Attributie laatste auth

Last-auth kenmerkt alle onbekende activiteit van een gedeeld apparaat aan de gebruiker die het laatst voor authentiek verklaarde. De identiteitsdienst van het Experience Platform bouwt de grafiek op de last-auth attributie en als zodanig gebruikt in grafiek-gebaseerde stitching. Zie [ grafiek die van de Identiteit regels ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-linking-rules/identity-optimization-algorithm#identity-optimization-algorithm-details) met elkaar verbindt voor meer informatie.

Wanneer kenmerk last-auth wordt gebruikt in stitching, worden id&#39;s met titel omgezet zoals in de onderstaande tabel wordt getoond.

| Tijdstempel | Paginanaam | Apparaat-id | E-mail | Id met titel |
|---|---|---|---|---|
| 2023-05-12 12:01 | Homepage | `1234` | | `cassidy@a.com` |
| 2023-05-12 12:02 | Productpagina | `1234` | | `cassidy@a.com` |
| 2023-05-12 12:03 | Volgorde succesvol | `1234` | `ryan@a.com` | `cassidy@a.com` |
| 2023-05-12 12:07 | Productpagina | `1234` | | `cassidy@a.com` |
| 2023-05-12 12:08 | Volgorde succesvol | `1234` | `cassidy@a.com` | `cassidy@a.com` |
| 2023-05-13 11:13 | Homepage | `1234` | | `cassidy@a.com` |


### Apparaatsplitsing

Apparaat-spleet attributen anonieme activiteit van een gedeeld apparaat aan de meest recente bekende gebruiker, die in het verleden kijkt. Apparaatsplitsing wordt momenteel gebruikt voor stitching op basis van veld.

Wanneer de apparaat-gespleten attributie in het stitching wordt gebruikt, oplossen de Getegrafeerde IDs zoals aangetoond in de hieronder lijst.

| Tijdstempel | Paginanaam | Apparaat-id | E-mail | Id met titel |
|---|---|---|---|---|
| 2023-05-12 12:01 | Homepage | `1234` | | `ryan@a.com` |
| 2023-05-12 12:02 | Productpagina | `1234` | | `ryan@a.com` |
| 2023-05-12 12:03 | Volgorde succesvol | `1234` | `ryan@a.com` | `ryan@a.com` |
| 2023-05-12 12:07 | Productpagina | `1234` | | `ryan@a.com` |
| 2023-05-12 12:08 | Volgorde succesvol | `1234` | `cassidy@a.com` | `cassidy@a.com` |
| 2023-05-13 11:13 | Homepage | `1234` | | `cassidy@a.com` |


<!--

### ECID reset 

As the name implies, ECID reset implements functionality that resets the ECID on a predetermined trigger, in most cases a login or logout event. With this implementation, a single device gets a new ECID every time the predetermined trigger fires. Essentially, this reset forces the device to become a *new device* over and again from a data perspective. The ECID reset also helps to prevent shared devices from even showing up in the data. No additional algorithms are required, but you have the responsibility to implement the ECID reset signal as part of your Adobe data collection implementation.


When using ECID reset, Stitched IDs resolve as shown in the table below. 

| Timestamp | Page name | Device ID | Email | Stitched ID |
|---|---|---|---|---|
| 2023-05-12 12:01 | Home page | `1234` | | `ryan@a.com`| 
| 2023-05-12 12:02 | Product page  | `1234` | |`ryan@a.com` | 
| 2023-05-12 12:03 | Order success | `1234` | `ryan@a.com` | `ryan@a.com` |
| 2023-05-12 12:07 | Product page  | 5678  | | `cassidy@a.com` | 
| 2023-05-12 12:08 | Order success | 5678 |  `cassidy@a.com` | `cassidy@a.com` |
| 2023-05-13 11:08 | Home page | 5678 | | `cassidy@a.com` |

-->

## Gedeelde apparaatbelichting

Overweeg verschillende factoren om correct te begrijpen hoe wijdverspreide gedeelde apparaten in uw organisatie zijn. Bovendien kunt u door inzicht te krijgen in de algemene bijdrage van gebeurtenissen van gedeelde apparaten, beter inzicht krijgen in het effect op de algemene gebeurtenisgegevens die worden gebruikt voor analyse.

Om de gedeelde apparatenblootstelling te begrijpen, kunt u over het uitvoeren van de volgende vragen denken.

1. **identificeer gedeelde apparaten**

   Om het aantal apparaten te begrijpen die worden gedeeld, voer een vraag uit die Apparaat IDs met twee of meer Gekoppelde Persoon IDs telt. Dit helpt apparaten identificeren die door veelvoudige individuen worden gebruikt.

   ```sql
   SELECT COUNT(*)
   FROM (
     SELECT /* INSERT PERSISTENT FIELD HERE */ AS persistent_id,
         COUNT(DISTINCT /* INSERT TRANSIENT FIELD HERE */) AS transient_count
     FROM /* INSERT DATASET HERE */
     GROUP BY 1
   )
   WHERE transient_count > 1; 
   ```


2. **Attributie van gebeurtenissen aan gedeelde apparaten**

   Voor de gedeelde apparaten die worden geïdentificeerd, bepaal hoeveel gebeurtenissen van het totaal aan deze apparaten kunnen worden toegeschreven. Deze toewijzing biedt inzicht in de invloed die gedeelde apparaten hebben op uw gegevens en de gevolgen voor de analyse.

   ```sql
   SELECT COUNT(*) AS total_events,
          COUNT(IF(shared_persistent_ids.persistent_id IS NOT NULL, 1, null)) shared_persistent_ids_events,
          (COUNT(IF(shared_persistent_ids.persistent_id IS NOT NULL, 1, null)) /
           COUNT(*)) * 100 AS shared_persistent_ids_events_percent
   FROM (
     SELECT /* INSERT PERSISTENT FIELD HERE */ AS persistent_id,
            /* INSERT TRANSIENT FIELD HERE */ AS transient_id
     FROM /* INSERT DATASET HERE */
   ) events
   LEFT JOIN (
     SELECT persistent_id
     FROM (
       SELECT /* INSERT PERSISTENT FIELD HERE */ AS persistent_id,
              COUNT(DISTINCT /* INSERT TRANSIENT FIELD HERE */) AS transient_count
       FROM /* INSERT DATASET HERE */
       GROUP BY 1
     )
     WHERE transient_count > 1
   ) shared_persistent_ids
   ON events.persistent_id = shared_persistent_ids.persistent_id; 
   ```

3. **identificeer anonieme gebeurtenissen op gedeelde apparaten**

   Bij de gebeurtenissen die aan gedeelde apparaten worden toegeschreven, bepaalt u hoeveel personen een Person-id hebben die anonieme gebeurtenissen aangeeft. Het algoritme dat u kiest (bijvoorbeeld last-auth, apparaat-split, of ECID-reset) om de gegevenskwaliteit te verbeteren, heeft invloed op deze anonieme gebeurtenissen.

   ```sql
   SELECT COUNT(IF(shared_persistent_ids.persistent_id IS NOT NULL, 1, null)) shared_persistent_ids_events,
          COUNT(IF(shared_persistent_ids.persistent_id IS NOT NULL AND events.transient_id IS NULL, 1, null)) shared_persistent_ids_anon_events,
          (COUNT(IF(shared_persistent_ids.persistent_id IS NOT NULL AND events.transient_id IS NULL, 1, null)) /
          COUNT(IF(shared_persistent_ids.persistent_id IS NOT NULL, 1, null))) * 100 AS shared_persistent_ids_anon_events_percent
   FROM (
     SELECT /* INSERT PERSISTENT FIELD HERE */ AS persistent_id,
            /* INSERT TRANSIENT FIELD HERE */ AS transient_id
     FROM /* INSERT DATASET HERE */ 
   ) events
   LEFT JOIN (
     SELECT persistent_id
     FROM (
       SELECT /* INSERT PERSISTENT FIELD HERE */ AS persistent_id,
              COUNT(DISTINCT /* INSERT TRANSIENT FIELD HERE */) AS transient_count
       FROM /* INSERT DATASET HERE */
       GROUP BY 1
     )
     WHERE transient_count > 1
   ) shared_persistent_ids 
   ON events.persistent_id = shared_persistent_ids.persistent_id; 
   ```

4. **berekent blootstelling van gebeurtenis misclassificatie**

   Ten slotte moet de blootstelling worden beoordeeld waarmee elke klant mogelijk wordt geconfronteerd als gevolg van een onjuiste classificatie van gebeurtenissen. Bereken het percentage anonieme gebeurtenissen over het totale aantal gebeurtenissen voor elk gedeeld apparaat. Dit helpt de potentiële invloed op de nauwkeurigheid van klantgegevens te begrijpen.

   ```sql
   SELECT COUNT(*) AS total_events,
          COUNT(IF(shared_persistent_ids.persistent_id IS NOT NULL, 1, null)) shared_persistent_ids_events,
          (COUNT(IF(shared_persistent_ids.persistent_id IS NOT NULL AND events.transient_id IS NULL, 1, null)) /
           COUNT(*)) * 100 AS shared_persistent_ids_events_percent
   FROM (
     SELECT /* INSERT PERSISTENT FIELD HERE */ AS persistent_id,
            /* INSERT TRANSIENT FIELD HERE */ AS transient_id
     FROM /* INSERT DATASET HERE */ 
   ) events
   LEFT JOIN (
     SELECT persistent_id
     FROM (
       SELECT /* INSERT PERSISTENT FIELD HERE */ AS persistent_id,
              COUNT(DISTINCT /* INSERT TRANSIENT FIELD HERE */) AS transient_count
       FROM /* INSERT DATASET HERE */
       GROUP BY 1
     )
     WHERE transient_count > 1
   ) shared_persistent_ids 
   ON events.persistent_id = shared_persistent_ids.persistent_id; 
   ```
