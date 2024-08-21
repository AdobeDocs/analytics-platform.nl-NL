---
title: Gedeelde apparaten
description: Uitleg van hoe te om gedeelde apparaten te behandelen gebruikend het stitching en andere technieken.
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
hide: true
hidefromtoc: true
role: Admin
source-git-commit: d94f6d6b592b2ddecfa0b1024b9ae045b3c3ce11
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 2%

---


# Gedeelde apparaten

Dit artikel verstrekt context op gedeelde apparaten, hoe te om gegevens van gedeelde apparaten te behandelen en te verlichten gebruikend het stitching, en gedeelde apparatenblootstelling in uw gegevens te begrijpen gebruikend de Dienst van de Vraag.

## Wat is een gedeeld apparaat?

Een gedeeld apparaat is een apparaat dat door meer dan één persoon wordt gebruikt. De gemeenschappelijke scenario&#39;s zijn apparaten zoals tabletten, apparaten die in kiosken worden gebruikt of computermateriaal dat door agenten in een vraagcentra wordt gedeeld.

Wanneer twee personen hetzelfde apparaat gebruiken en beide een aankoop doen, kunnen voorbeeldgebeurtenisgegevens er als volgt uitzien:

| Tijdstempel | Paginanaam | Apparaat-id | E-mail |
|---|---|---|---|
| 2023-05-12 12:01 | Homepage | 1234 | |
| 2023-05-12 12:02 | Productpagina | 1234 | |
| 2023-05-12 12:03 | Volgorde succesvol | 1234 | <ryan@a.com> |
| 2023-05-12 12:07 | Productpagina | 1234 | |
| 2023-05-12 12:08 | Volgorde succesvol | 1234 | <cassidy@a.com> |

De gebeurtenissen voor het slagen van de bestelling (aankoop) wijzen de gegevens correct toe aan de juiste e-mail. Hoe deze toewijzing van invloed is op uw analyse, hangt af van de manier waarop u de analyse uitvoert:

- Apparaatgerichte benadering: analyse uitgevoerd met de apparaat-id. Met deze aanpak worden zowel geverifieerde als niet-geverifieerde gegevens opgenomen in de analyse. Deze aanpak maakt echter geen meer persoonlijke analyse mogelijk.
- Centrische benadering van personen: analyse uitgevoerd met het e-mailadres of een andere persoon-id. Met deze aanpak worden alleen geverifieerde gebeurtenissen opgenomen in de analyse. Deze benadering geeft geen volledig beeld van de reis van de klant, met inbegrip van aankoop

## Centrische analyse van personen verbeteren

Voor een betere persoonlijke centrische analyse van gedeelde apparaten hebt u twee opties: u kunt stitching gebruiken of u kunt ECID-resetfunctionaliteit implementeren. Beide benaderingen worden in de onderstaande secties nader besproken.

### Stiksel

Het stitching proces richt het gebrek van de persoon centric benadering. Door een tik in te stellen, wordt de id van de geselecteerde persoon (in de voorbeeldgegevens, in het e-mailbericht) toegevoegd aan gebeurtenissen waarbij die id niet bestaat. Het plaatsen hefboomwerkingen een afbeelding tussen Apparaat IDs en Persoon IDs om ervoor te zorgen dat zowel voor authentiek verklaard als niet voor authentiek verklaard verkeer in analyse kan worden gebruikt, die het persoon centric houdt. Zie [ het Plaatsen ](/help/stitching/overview.md) voor meer informatie.

Bij het instellen van tekenreeksen kunnen gedeelde apparaatgegevens worden toegewezen met de kenmerk last-auth of door het apparaat gesplitste kenmerk. Implementatiewijzigingen via ECID-reset kunnen echter ook betrekking hebben op gedeelde apparaten.


#### Attributie laatste auth

Last-auth kenmerkt alle onbekende activiteit van een gedeeld apparaat aan de gebruiker die het laatst voor authentiek verklaarde. Last-auth wordt gebruikt in Audience Manager, en is de aangewezen benadering voor het gebruiksgevallen van het Profiel van de Gegevens van de Klant in real time. De identiteitsdienst van het Experience Platform bouwt de grafiek op de last-auth attributie en als zodanig gebruikt in grafiek-gebaseerde stitching. Zie [ grafiek die van de Identiteit regels verbindt overzicht ](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-linking-rules/overview) voor meer informatie.

Als u de kenmerk last-auth gebruikt in stitching, worden de id&#39;s met titel omgezet, zoals in de onderstaande tabel wordt getoond.

| Tijdstempel | Paginanaam | Apparaat-id | E-mail | Id met titel |
|---|---|---|---|---|
| 2023-05-12 12:01 | Homepage | 1234 | | <cassidy@a.com> |
| 2023-05-12 12:02 | Productpagina | 1234 | | <cassidy@a.com> |
| 2023-05-12 12:03 | Volgorde succesvol | 1234 | <ryan@a.com> | <cassidy@a.com> |
| 2023-05-12 12:07 | Productpagina | 1234 | | <cassidy@a.com> |
| 2023-05-12 12:08 | Volgorde succesvol | 1234 | <cassidy@a.com> | <cassidy@a.com> |
| 2023-05-13 11:13 | Homepage | 1234 | | <cassidy@a.com> |


#### Apparaatsplitsing

Apparaat-spleet attributen anonieme activiteit van een gedeeld apparaat aan de gebruiker in dichtste nabijheid van de anonieme activiteit. Apparaatsplitsing wordt momenteel gebruikt voor stitching op basis van veld. Apparaatsplitsing is de voorkeursbenadering voor analytische gebruikgevallen, aangezien apparaatsplitsing zowel de ongeautoriseerde als de geverifieerde activiteit aan de dichtstbijzijnde bekende persoon krediet geeft. Apparaatsplitsing wordt momenteel gebruikt voor stitching op basis van veld.

Als u een apparaat-gesplitste kenmerk gebruikt in stitching, worden Stitched ID&#39;s opgelost zoals in de onderstaande tabel wordt getoond.

| Tijdstempel | Paginanaam | Apparaat-id | E-mail | Id met titel |
|---|---|---|---|---|
| 2023-05-12 12:01 | Homepage | 1234 | | <ryan@a.com> |
| 2023-05-12 12:02 | Productpagina | 1234 | | <ryan@a.com> |
| 2023-05-12 12:03 | Volgorde succesvol | 1234 | <ryan@a.com> | <ryan@a.com> |
| 2023-05-12 12:07 | Productpagina | 1234 | | <ryan@a.com> |
| 2023-05-12 12:08 | Volgorde succesvol | 1234 | <cassidy@a.com> | <cassidy@a.com> |
| 2023-05-13 11:13 | Homepage | 1234 | | <cassidy@a.com> |


### ECID opnieuw instellen

Zoals de naam impliceert, voert het terugstellen van ECID functionaliteit uit die ECID op een vooraf bepaalde trekker, in de meeste gevallen een login of logout gebeurtenis terugstelt. Met deze implementatie krijgt één apparaat een nieuwe ECID telkens wanneer de vooraf bepaalde trigger wordt geactiveerd. Essentieel, dwingt dit terugstellen het apparaat om a *nieuw apparaat* opnieuw en opnieuw van een gegevensperspectief te worden. De ECID-reset helpt ook te voorkomen dat gedeelde apparaten zelfs in de gegevens worden weergegeven. Er zijn geen aanvullende algoritmen vereist, maar u hebt de verantwoordelijkheid om het ECID-resetsignaal te implementeren als onderdeel van de implementatie van de Adobe voor gegevensverzameling.


Als u de ECID-instelling gebruikt, worden de geselecteerde id&#39;s omgezet zoals in de onderstaande tabel wordt getoond.

| Tijdstempel | Paginanaam | Apparaat-id | E-mail | Id met titel |
|---|---|---|---|---|
| 2023-05-12 12:01 | Homepage | 1234 | | <ryan@a.com> |
| 2023-05-12 12:02 | Productpagina | 1234 | | <ryan@a.com> |
| 2023-05-12 12:03 | Volgorde succesvol | 1234 | <ryan@a.com> | <ryan@a.com> |
| 2023-05-12 12:07 | Productpagina | 5678 | | <cassidy@a.com> |
| 2023-05-12 12:08 | Volgorde succesvol | 5678 | <cassidy@a.com> | <cassidy@a.com> |
| 2023-05-13 11:13 | Homepage | 5678 | | <cassidy@a.com> |

## Gedeelde apparaatbelichting

Overweeg verschillende factoren om correct te begrijpen hoe wijdverspreide gedeelde apparaten in uw organisatie zijn. Bovendien kunt u door inzicht te krijgen in de algemene bijdrage van gebeurtenissen van gedeelde apparaten, beter inzicht krijgen in het effect op de algemene gebeurtenisgegevens die worden gebruikt voor analyse.

Om de gedeelde apparatenblootstelling te begrijpen, kunt u over het uitvoeren van de volgende vragen denken.

1. Begrijp het aantal apparaten dat wordt gedeeld. U kunt een query gebruiken die de apparaat-id&#39;s telt waaraan twee of meer persoon-id&#39;s zijn gekoppeld. Een voorbeeldquery zou er als volgt kunnen uitzien:

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


2. Voor de gedeelde apparaten, resulterend uit de eerste vraag, moet u begrijpen hoeveel gebeurtenissen van de totale gebeurtenissen aan deze gedeelde apparaten kunnen worden toegeschreven. Deze toewijzing geeft u een beter inzicht in de invloed van gedeelde apparaten op uw gegevens en in de impact wanneer u een analyse uitvoert. Een voorbeeldquery zou er als volgt kunnen uitzien:

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

3. Voor de gebeurtenissen die aan gedeelde apparaten (het resultaat van de tweede vraag) worden toegewezen, moet u begrijpen hoeveel van deze gebeurtenissen GEEN identiteitskaart van de Persoon hebben. Anders vermeld, hoeveel van de gedeelde apparatengebeurtenissen anonieme gebeurtenissen zijn. Uiteindelijk heeft het algoritme (last-auth, device-split, ECID-reset) dat u selecteert om de gegevenskwaliteit te verbeteren, invloed op deze anonieme gedeelde apparaatgebeurtenissen. Een voorbeeldquery zou er als volgt kunnen uitzien:

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

4. Tot slot wilt u de blootstelling begrijpen elke klant wegens gebeurtenismisclassificatie zou ervaren. Om deze blootstelling te krijgen, moet u, voor elk gedeeld apparaat, het percentage anonieme gebeurtenissen berekenen met betrekking tot het totale aantal gebeurtenissen. Een voorbeeldquery zou er als volgt kunnen uitzien:

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


