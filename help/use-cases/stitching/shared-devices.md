---
title: Gedeelde apparaten
description: Uitleg van hoe te om gedeelde apparaten te behandelen gebruikend het stitching en andere technieken.
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
hide: true
hidefromtoc: true
role: Admin
source-git-commit: 1a5646700dba6362a35158890f2917fc472fbddd
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 0%

---


# Gedeelde apparaten

Dit artikel verstrekt context op gedeelde apparaten, hoe te om gegevens van gedeelde apparaten te behandelen en te verlichten gebruikend het stitching, en gedeelde apparatenblootstelling in uw gegevens te begrijpen gebruikend de Dienst van de Vraag.

## Wat is een gedeeld apparaat?

Een gedeeld apparaat is een apparaat dat door meer dan één persoon wordt gebruikt. De gemeenschappelijke scenario&#39;s zijn apparaten zoals tabletten, apparaten die in kiosken worden gebruikt of computermateriaal dat door agenten in een vraagcentra wordt gedeeld.

Wanneer twee personen hetzelfde apparaat gebruiken en beide een aankoop doen, kunnen voorbeeldgebeurtenisgegevens er als volgt uitzien:

| Tijdstempel | Paginanaam | Apparaat-id | E-mail |
|---|---|---|---|
| 2023-05-12 12:01 | Homepage | `1234` | |
| 2023-05-12 12:02 | Productpagina | `1234` | |
| 2023-05-12 12:03 | Volgorde succesvol | `1234` | `ryan@a.com` |
| 2023-05-12 12:07 | Productpagina | `1234` | |
| 2023-05-12 12:08 | Volgorde succesvol | `1234` | `cassidy@a.com` |

De gebeurtenissen voor het slagen van de bestelling (aankoop) wijzen de gegevens correct toe aan de juiste e-mail. Hoe deze toewijzing van invloed is op uw analyse, hangt af van de manier waarop u de analyse uitvoert:

- Apparaatgerichte benadering: analyse uitgevoerd met de apparaat-id. Met deze aanpak worden zowel geverifieerde als niet-geverifieerde gegevens opgenomen in de analyse. Deze aanpak maakt echter geen meer persoonlijke analyse mogelijk.
- Centrische benadering van personen: analyse uitgevoerd met het e-mailadres of een andere persoon-id. Met deze aanpak worden alleen geverifieerde gebeurtenissen opgenomen in de analyse. Deze benadering geeft geen volledig beeld van de reis van de klant, met inbegrip van aankoop

## Centrische analyse van personen verbeteren

De voorbeeldgegevens zijn een combinatie van zowel geverifieerde als niet-geverifieerde activiteit voor hetzelfde apparaat. De uitdaging is een persoon aan het niet voor authentiek verklaarde verkeer toe te wijzen, zodat kunt u een persoon-centric analyse uitvoeren en de Analyses van de Reis van de Klant verhinderen om de activiteiten te laten vallen die geen persoon identiteitskaart waarde hebben. U kunt deze uitdaging op twee manieren oplossen: u kunt het stitching gebruiken of u kunt de functie voor het opnieuw instellen van ECID&#39;s implementeren. Beide opties worden in de onderstaande secties besproken.

### Stiksel

Het stitching proces richt het gebrek van de persoon centric benadering. Door een tik in te stellen, wordt de id van de geselecteerde persoon (in de voorbeeldgegevens, in het e-mailbericht) toegevoegd aan gebeurtenissen waarbij die id niet bestaat. Het plaatsen hefboomwerkingen een afbeelding tussen Apparaat IDs en Persoon IDs om ervoor te zorgen dat zowel voor authentiek verklaard als niet voor authentiek verklaard verkeer in analyse kan worden gebruikt, die het persoon centric houdt. Zie [ het Plaatsen ](/help/stitching/overview.md) voor meer informatie.

Bij het instellen van tekenreeksen kunnen gedeelde apparaatgegevens worden toegewezen met de kenmerk last-auth of door het apparaat gesplitste kenmerk. Implementatiewijzigingen via ECID-reset kunnen echter ook betrekking hebben op gedeelde apparaten.


#### Attributie laatste auth

Last-auth kenmerkt alle onbekende activiteit van een gedeeld apparaat aan de gebruiker die het laatst voor authentiek verklaarde. Last-auth wordt gebruikt in Audience Manager, en is de aangewezen benadering voor het gebruiksgevallen van het Profiel van de Gegevens van de Klant in real time. De identiteitsdienst van het Experience Platform bouwt de grafiek op de last-auth attributie en als zodanig gebruikt in grafiek-gebaseerde stitching. Zie [ grafiek die van de Identiteit regels verbindt overzicht ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-linking-rules/overview) voor meer informatie.

Als u de kenmerk last-auth gebruikt in stitching, worden de id&#39;s met titel omgezet, zoals in de onderstaande tabel wordt getoond.

| Tijdstempel | Paginanaam | Apparaat-id | E-mail | Id met titel |
|---|---|---|---|---|
| 2023-05-12 12:01 | Homepage | `1234` | | `cassidy@a.com` |
| 2023-05-12 12:02 | Productpagina | `1234` | | `cassidy@a.com` |
| 2023-05-12 12:03 | Volgorde succesvol | `1234` | `ryan@a.com` | `cassidy@a.com` |
| 2023-05-12 12:07 | Productpagina | `1234` | | `cassidy@a.com` |
| 2023-05-12 12:08 | Volgorde succesvol | `1234` | `cassidy@a.com` | `cassidy@a.com` |
| 2023-05-13 11:13 | Homepage | `1234` | | `cassidy@a.com` |


#### Apparaatsplitsing

Apparaat-spleet attributen anonieme activiteit van een gedeeld apparaat aan de gebruiker in dichtste nabijheid van de anonieme activiteit. Apparaatsplitsing wordt momenteel gebruikt voor stitching op basis van veld. Apparaatsplitsing is de voorkeursbenadering voor analytische gebruikgevallen, aangezien apparaatsplitsing zowel de ongeautoriseerde als de geverifieerde activiteit aan de dichtstbijzijnde bekende persoon krediet geeft. Apparaatsplitsing wordt momenteel gebruikt voor stitching op basis van veld.

Als u een apparaat-gesplitste kenmerk gebruikt in stitching, worden Stitched ID&#39;s opgelost zoals in de onderstaande tabel wordt getoond.

| Tijdstempel | Paginanaam | Apparaat-id | E-mail | Id met titel |
|---|---|---|---|---|
| 2023-05-12 12:01 | Homepage | `1234` | | `ryan@a.com` |
| 2023-05-12 12:02 | Productpagina | `1234` | | `ryan@a.com` |
| 2023-05-12 12:03 | Volgorde succesvol | `1234` | `ryan@a.com` | `ryan@a.com` |
| 2023-05-12 12:07 | Productpagina | `1234` | | `ryan@a.com` |
| 2023-05-12 12:08 | Volgorde succesvol | `1234` | `cassidy@a.com` | `cassidy@a.com` |
| 2023-05-13 11:13 | Homepage | `1234` | | `cassidy@a.com` |


### ECID opnieuw instellen

Zoals de naam impliceert, voert het terugstellen van ECID functionaliteit uit die ECID op een vooraf bepaalde trekker, in de meeste gevallen een login of logout gebeurtenis terugstelt. Met deze implementatie krijgt één apparaat een nieuwe ECID telkens wanneer de vooraf bepaalde trigger wordt geactiveerd. Essentieel, dwingt dit terugstellen het apparaat om a *nieuw apparaat* opnieuw en opnieuw van een gegevensperspectief te worden. De ECID-reset helpt ook te voorkomen dat gedeelde apparaten zelfs in de gegevens worden weergegeven. Er zijn geen aanvullende algoritmen vereist, maar u hebt de verantwoordelijkheid om het ECID-resetsignaal te implementeren als onderdeel van de implementatie van de Adobe voor gegevensverzameling.


Als u de ECID-instelling gebruikt, worden de geselecteerde id&#39;s omgezet zoals in de onderstaande tabel wordt getoond.

| Tijdstempel | Paginanaam | Apparaat-id | E-mail | Id met titel |
|---|---|---|---|---|
| 2023-05-12 12:01 | Homepage | `1234` | | `ryan@a.com` |
| 2023-05-12 12:02 | Productpagina | `1234` | | `ryan@a.com` |
| 2023-05-12 12:03 | Volgorde succesvol | `1234` | `ryan@a.com` | `ryan@a.com` |
| 2023-05-12 12:07 | Productpagina | 5678 | | `cassidy@a.com` |
| 2023-05-12 12:08 | Volgorde succesvol | 5678 | `cassidy@a.com` | `cassidy@a.com` |
| 2023-05-13 11:13 | Homepage | 5678 | | `cassidy@a.com` |

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

   Voor de gedeelde apparaten die worden geïdentificeerd, bepaal hoeveel gebeurtenissen van het totaal aan deze apparaten kunnen worden toegeschreven. Dit verstrekt inzicht in de invloed gedeelde apparaten op uw gegevens en de implicaties voor analyse hebben.

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


