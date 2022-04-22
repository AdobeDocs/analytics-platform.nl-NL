---
title: AEP-publiek opnemen in Customer Journey Analytics
description: Verklaart hoe te om AEP publiek in Customer Journey Analytics voor verdere analyse op te nemen.
solution: Customer Journey Analytics
feature: Use Cases
source-git-commit: ed01fd0899cac21fff156e0c31dc2b52ff7c8cca
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---


# AEP-publiek opnemen in Customer Journey Analytics (CJA)

>[!NOTE]
>
>Dit onderwerp is in voorbereiding.

(Brandon, fyi, &#39;Unified Profile&#39; is een verouderde term voor &#39;Real-time klantprofiel&#39; - volgens de documentmanager van AEP. U zult geen doc op UP vinden in de AEP doc set.)

Deze gebruikszaak verkent een tijdelijke, handmatige manier om Adobe Experience Platform (AEP)-publiek naar CJA te brengen. Dit publiek zou in de Bouwer van het Segment van AEP, of Adobe Audience Manager, of andere hulpmiddelen kunnen gecreeerd zijn, en opgeslagen in het Profiel van de Klant in real time (RTCP). Het publiek bestaat uit lijsten met personen-id&#39;s, profiel-id&#39;s, enz. en wij willen hen in de Werkruimte van CJA voor analyse brengen.

## Vereisten

* Toegang tot Adobe Experience Platform (AEP), in het bijzonder Real-time Klantprofiel.
* Toegang tot Customer Journey Analytics
* Wilt u aangepaste code schrijven?
* Wat nog meer.

## Stap 1: Kies een of meer doelgroepen in het profiel voor realtime klanten {#audience}

Adobe Experience Platform [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en) (RTCP) laat u een holistische mening van elke individuele klant zien door gegevens van veelvoudige kanalen, met inbegrip van online, off-line, CRM, en derde te combineren. U hebt waarschijnlijk al een publiek in RTCP dat uit diverse bronnen kan zijn gekomen. Kies een of meer soorten publiek.

## Stap 2: Een profielgegevensset voor Unie maken voor het exporteren

Om het publiek naar een dataset uit te voeren die dan een verbinding aan CJA kan maken, moet u een dataset tot stand brengen het waarvan schema een Profiel is [Unieschema](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=en#understanding-union-schemas).
De schema&#39;s van de unie zijn samengesteld uit veelvoudige schema&#39;s die de zelfde klasse delen en voor Profiel toegelaten. Met het samenvoegingsschema kunt u een samenvoeging zien van alle velden in schema&#39;s die dezelfde klasse delen. Het Profiel van de Klant in real time gebruikt het verenigingsschema om een holistische mening van elke individuele klant tot stand te brengen.

## Stap 3: Een publiek naar een dataset exporteren via een API-aanroep {#export}

Alvorens u een publiek in CJA kunt brengen, moet u het naar een dataset in AEP uitvoeren. Dit kan alleen worden gedaan met de segmentatie-API, en met name met de [API-eindpunt voor taken exporteren](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en). U kunt een uitvoerbaan tot stand brengen en de resultaten in de dataset van de Vereniging van het Profiel zetten AEP u in Stap 2 creeerde.

## Stap 4: De exportuitvoer bewerken

Wanneer het creëren van de uitvoerbaan voor een publiek, hebben wij slechts identiteitskaart van de Persoon en identiteitskaart van de Publiek nodig om de rapportering in CJA te doen. De standaard exporttaak bevat echter meer gegevens en dus moeten we deze uitvoer bewerken om overbodige gegevens te verwijderen.

Hier is een voorbeeld van de uitvoeroutput in de de verenigingsdataset van het Profiel, **voor** alle bewerkingen:

![Onbewerkte uitvoer](assets/export-unedited.png)

Let op het volgende:

* De gebruikers-id staat onder `segmentmembership.ups.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.status`.
* De status moet &quot;gerealiseerd&quot; of &quot;binnengekomen&quot; zijn, maar niet &quot;verlaten&quot;. Vervang &quot;exited&quot; door &quot;blank&quot;.

Dit is het formaat van de dataset van het Profiel die u in CJA kunt verzenden.

![Bewerkte uitvoer](assets/export-edited.png)

Hier volgen de gegevenselementen die aanwezig moeten zijn:

* `_aresprodvalidation`: Verwijst naar uw organisatie-id. U zult anders zijn.
* `personID`: In dit geval een vriendelijke naam
* `audienceMembershipIdList` tekenreeksveld: De gebruikers-id
* Voeg een vriendelijke naam voor het publiek toe (`audienceMembershipIdName`), zoals

   ![Vriendelijke publieksnaam](assets/audience-name.png)

## Stap 5: Verbinding maken in CJA met deze profielgegevensset

[Verbinding maken](/help/connections/create-connection.md)

## Stap 6: Een gegevensweergave maken

Toevoegen `audienceMembershipIdName` en `personID` naar de gegevensweergave.

## Stap 7: Rapport in werkruimte

U kunt nu rapporteren over `audienceMembershipIdName` en `personID` in Workspace.
Screenshot zou geweldig zijn.

Ga als volgt te werk:

schrijven meer stappen voor wanneer u mensen behandelt die lid van veelvoudige toehoorders zijn.




