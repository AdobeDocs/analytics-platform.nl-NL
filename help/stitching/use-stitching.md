---
title: Sstitching gebruiken
description: Hoe wordt stitching gebruikt
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
role: Admin
exl-id: a04c74ab-606e-45a9-a3e4-0d476c8d2426
source-git-commit: 7cd0bd94ec45b1570d0be765d95b25defa3e1b87
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Sstitching gebruiken

Zodra uw organisatie aan alle [ eerste vereisten ](#prerequisites) voldoet en gemeenschappelijke [ beperkingen ](#limitations) en het stitching methode specifieke ([ op gebied-gebaseerde ](#limitations-1) en [ op grafiek-gebaseerde ](#limitations-2)) beperkingen begrijpt, kunt u deze stappen volgen om het stitching in Customer Journey Analytics te beginnen gebruiken.

## Opties selecteren

Het Customer Journey Analytics-pakket waarop u recht hebt, bepaalt de beschikbare tekenreeksmethoden, opties voor de initiële duur van de backfill, het terugzoekvenster, de herhalingsfrequentie en het maximale aantal gegevenssets dat is toegestaan voor stitching. Zie de [ het productbeschrijving van Customer Journey Analytics ](https://helpx.adobe.com/nl/legal/product-descriptions/customer-journey-analytics.html) voor meer details. Bepaal de beschikbare opties voordat u ondersteuning aanvraagt.

| | Customer Journey Analytics <br/> Uitgezocht | Customer Journey Analytics <br/> Prime | Customer Journey Analytics <br/> Ultimate |
|---|---|---|---|
| Beschikbare stitmethoden | <li>Veldgebaseerde stitching</li> | <li>Veldgebaseerde stitching</li><li>Op grafiek gebaseerde stitching</li> | <li>Veldgebaseerde stitching</li><li>Op grafiek gebaseerde stitching</li> |
| Eenmalige duur van de backfill-functie | 13 maanden | 13 maanden | 25 maanden |
| Zoekvenster en herhalingsfrequentie | <li>1 dag, elke dag</li><li>tot 7 dagen, wekelijks</li> | <li>1 dag, elke dag</li><li>tot 14 dagen, wekelijks</li> | <li>1 dag, elke dag</li><li>tot 30 dagen, wekelijks</li> |
| Maximumaantal gegevenssets dat is toegestaan voor stitching | 5 | 15 | 50 |

## Verzoek om ondersteuning

1. Neem contact op met de klantenondersteuning van Adobe via de volgende informatie:

   - Een verzoek om stitching in te schakelen.
   - De dataset-id voor de gegevensset die u opnieuw wilt invoeren.
   - De kolomnaam (identiteitspad en naamruimte) van de permanente id voor de gewenste gegevensset (de id die op elke rij wordt weergegeven).
   - Als de dataset `identityMap` ondersteunt:
      - Geef voor stitching op basis van velden de naamruimte op voor zowel de permanente als tijdelijke id&#39;s.
      - Geef voor op grafiek gebaseerde stitching de naamruimte op voor de persistente id en de naamruimte voor identiteiten die moet worden gebruikt voor het opvragen van de identiteitsgrafiek.
   - Als de gegevensset `identityMap` niet ondersteunt:
      - Voor op veld gebaseerde stitching, de kolomnaam van transient identiteitskaart voor de gewenste dataset (persoonsidentificatie, die ook als verbinding tussen datasets in de context van een verbinding dienst doet).
      - Voor op een grafiek gebaseerde stitching, de identiteitsnaamruimte die voor het vragen van de identiteitsgrafiek moet worden gebruikt.
   - Uw voorkeur voor terugkijkvenster en herhalingsfrequentie. Zie uw pakket van Customer Journey Analytics voor de [ beschikbare opties ](#options).
   - Naam van sandbox.


2. De Adobe Klantenondersteuning werkt samen met de Adobe-engineering, zodat u op uw verzoek kunt aansluiten. Als deze optie is ingeschakeld, wordt in Adobe Experience Platform een nieuwe opnieuw weergegeven gegevensset met een nieuwe kolom met een naastgelegen id weergegeven. De klantenondersteuning van Adobe kan de id van de nieuwe gegevensset opgeven.

3. Als Adobe voor het eerst is ingeschakeld, wordt een back-up van opgeslagen gegevens gemaakt. Zie uw pakket van Customer Journey Analytics voor de [ beschikbare optie ](#options).

4. Als u de nieuwe gestikte dataset in een dwars-kanaalanalyse wilt gebruiken, moet u de nieuwe verbonden dataset aan a [ verbinding ](../connections/overview.md) in Customer Journey Analytics toevoegen. Voeg vervolgens andere gegevenssets toe die vereist zijn voor kanaalanalyse en selecteer de juiste persoon-id voor elke gegevensset.

5. [ creeer een gegevensmening ](/help/data-views/create-dataview.md) die op de verbinding wordt gebaseerd.

<!-- To do: Paragraph on backfill once product and marketing determine the best way forward. -->

Zodra de gegevensweergave is ingesteld, kunt u de Customer Journey Analytics-rapportanalyse uitvoeren op alle kanalen en apparaten.

<!-- Uncomment once stitching UI is available (for limited testing)..

### Do It Yourself

|Positive|[!BADGE New Feature]{type=Positive before-title="false"}|

{{release-limited-testing-section}}

Alternatively, you can set up and use stitching through the Customer Journey Analytics user interface:

1. Go to the [Create and manage stitched datasets](stitching-ui.md) and follow steps to rekey your dataset.

2. [Create a connection](/help/connections/create-connection.md) in Customer Journey Analytics using the newly generated dataset and any other datasets that you want to include. Choose the correct person ID for each dataset.

3. [Create a connection](/help/connections/create-connection.md) in Customer Journey Analytics using the newly generated dataset and any other datasets that you want to include. Choose the correct person ID for each dataset.
   
4. [Create a data view](/help/data-views/create-dataview.md) based on the connection.

Once the data view is set up, the cross-channel analysis in Customer Journey Analytics is just like any other analysis in Customer Journey Analytics, except now the data operates across channels and devices.

-->
