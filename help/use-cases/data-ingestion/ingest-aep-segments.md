---
title: Adobe Experience Platform-publiek vertalen in Customer Journey Analytics
description: Verklaart hoe te om Adobe Experience Platform publiek in Customer Journey Analytics voor verdere analyse in te nemen.
solution: Customer Journey Analytics
feature: Use Cases
exl-id: cb5a4f98-9869-4410-8df2-b2f2c1ee8c57
source-git-commit: e7e3affbc710ec4fc8d6b1d14d17feb8c556befc
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# Maak kennis met Adobe Experience Platform en Adobe Customer Journey Analytics

Deze gebruikszaak verkent een tijdelijke, handmatige manier om het Adobe Experience Platform (Adobe Experience Platform) publiek in Customer Journey Analytics te brengen. Dit publiek zou in de Bouwer van het Segment van Adobe Experience Platform, of Adobe Audience Manager, of andere hulpmiddelen kunnen gecreeerd zijn, en opgeslagen in het Profiel van de Klant in real time (RTCP). Het publiek bestaat uit een set profiel-id&#39;s, samen met eventuele toepasselijke kenmerken/gebeurtenissen/enzovoort. en wij willen hen in de Werkruimte van de Customer Journey Analytics voor analyse brengen.

## Vereisten

* Toegang tot Adobe Experience Platform (Adobe Experience Platform), in het bijzonder Real-Time Klantprofiel.
* Toegang tot het maken/beheren van Adobe Experience Platform-schema&#39;s en gegevenssets.
* Toegang tot Adobe Experience Platform Query Service (en de mogelijkheid om SQL te schrijven) of een ander hulpprogramma om bepaalde lichte transformaties uit te voeren.
* Toegang tot Customer Journey Analytics. U moet een Customer Journey Analytics-productbeheerder zijn om Customer Journey Analytics-verbindingen en gegevensweergaven te maken/wijzigen.
* Mogelijkheid om de Adobe-API&#39;s te gebruiken (segmentatie, optioneel andere)

## Stap 1: Kies een of meer doelgroepen in het profiel voor realtime klanten {#audience}

Adobe Experience Platform [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en) (RTCP) laat u een holistische mening van elke individuele klant zien door gegevens van veelvoudige kanalen, met inbegrip van online, off-line, CRM, en derde te combineren.

U hebt waarschijnlijk al een publiek in RTCP dat uit diverse bronnen kan zijn gekomen. Kies een of meer soorten publiek om in te nemen in Customer Journey Analytics.

## Stap 2: Een profielgegevensset voor Unie maken voor het exporteren

Om het publiek naar een dataset uit te voeren die uiteindelijk aan een verbinding in Customer Journey Analytics kan worden toegevoegd, moet u een dataset tot stand brengen het waarvan schema een Profiel is [Unieschema](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=en#understanding-union-schemas).

De schema&#39;s van de unie zijn samengesteld uit veelvoudige schema&#39;s die de zelfde klasse delen en voor Profiel toegelaten. Met het samenvoegingsschema kunt u een samenvoeging zien van alle velden in schema&#39;s die dezelfde klasse delen. Het Profiel van de Klant in real time gebruikt het verenigingsschema om een holistische mening van elke individuele klant tot stand te brengen.

## Stap 3: Een publiek naar de profielunie exporteren via een API-aanroep {#export}

Alvorens u een publiek in Customer Journey Analytics kunt brengen, moet u het naar een dataset van Adobe Experience Platform uitvoeren. Dit kan alleen worden gedaan met de segmentatie-API, en met name met de [API-eindpunt voor taken exporteren](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en).

U kunt een uitvoerbaan tot stand brengen gebruikend publiekidentiteitskaart van uw keus, en de resultaten in de dataset van de Vereniging van het Profiel plaatsen Adobe Experience Platform u in Stap 2 creeerde. Hoewel u verschillende kenmerken/gebeurtenissen voor het publiek kunt exporteren, hoeft u alleen het veld voor de specifieke profiel-id te exporteren dat overeenkomt met het veld voor de persoon-id dat wordt gebruikt in de Customer Journey Analytics-verbinding die u wilt gebruiken (zie onder in Stap 5).

## Stap 4: De exportuitvoer bewerken

De resultaten van de exporttaak moeten worden omgezet in een aparte profielgegevensset om te worden opgenomen in Customer Journey Analytics.  Deze transformatie kan worden uitgevoerd met [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=en)of een ander transformatiegereedschap van uw keuze. We hebben alleen de profiel-id (die overeenkomt met de persoon-id in Customer Journey Analytics) en een of meer gebruikers-id(&#39;s) nodig om de rapportage in Customer Journey Analytics uit te voeren.

De standaard exporttaak bevat echter meer gegevens en daarom moeten we deze uitvoer bewerken om irrelevante gegevens te verwijderen en enkele zaken te verplaatsen.  Ook, moet u een schema/dataset eerst tot stand brengen alvorens u de getransformeerde gegevens aan het toevoegt.

Hier is een voorbeeld van de uitvoeroutput in de de verenigingsdataset van het Profiel, **voor** alle bewerkingen:

![Onbewerkte uitvoer](../assets/export-unedited.png)

Let op het volgende:

* De gebruikers-id staat onder `segmentmembership.ups.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.status`.
* De status moet &quot;gerealiseerd&quot; of &quot;binnengekomen&quot; zijn, maar niet &quot;verlaten&quot;.

Dit is het formaat van de dataset van het Profiel die u in Customer Journey Analytics kunt verzenden.

![Bewerkte uitvoer](../assets/export-edited.png)

Hier volgen de gegevenselementen die aanwezig moeten zijn:

* `_aresprodvalidation` tekenreeksveld: Verwijst naar uw organisatie-id. U zult anders zijn.
* `personID` tekenreeksveld: Dit is het standaard XDM schemagebied op de datasets van het Profiel om de persoon te identificeren. Gebruik de profiel-id van het exporteren.
* `audienceMembershipId` tekenreeksveld: De gebruikers-id uit de exportbewerking.  OPMERKING: Dit veld kan een naam krijgen die u maar wilt (vanuit uw eigen schema).
* Voeg een vriendelijke naam voor het publiek toe (`audienceMembershipIdName`), zoals

  ![Vriendelijke publieksnaam](../assets/audience-name.png)

* Voeg desgewenst andere publieksmetagegevens toe.

## Stap 5: Deze profielgegevensset toevoegen aan een bestaande verbinding in Customer Journey Analytics

U kunt [een nieuwe verbinding maken](/help/connections/create-connection.md), maar de meeste klanten zullen de dataset van het Profiel aan een bestaande verbinding willen toevoegen. De gebruikers-id&#39;s verrijken de bestaande gegevens in Customer Journey Analytics.

## Stap 6: Bestaande (of nieuwe) weergave met Customer Journey Analytics-gegevens wijzigen

Toevoegen `audienceMembershipId`, `audienceMembershipIdName` en `personID` in de gegevensweergave.

## Stap 7: Rapport in werkruimte

U kunt nu rapporteren over `audienceMembershipId`, `audienceMembershipIdName` en `personID` in Workspace.

## Aanvullende opmerkingen

* U zou dit proces op een regelmatige kadentie moeten uitvoeren, zodat de publieksgegevens constant binnen Customer Journey Analytics worden verfrist.
* U kunt meerdere soorten publiek importeren binnen één Customer Journey Analytics-verbinding. Dit vergroot de complexiteit van het proces, maar het is mogelijk. Dit werkt alleen als u enkele wijzigingen aanbrengt in het bovenstaande proces:
   1. Voer dit proces voor elk gewenst publiek in uw publieksinzameling binnen RTCP uit.
   1. Customer Journey Analytics ondersteunt arrays/objectarrays in profielgegevenssets. Een [array van objecten](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/complex-data/object-arrays.html) voor publiekMembershipId of publiekMembershipIdName is de beste optie.
   1. Maak in de gegevensweergave een nieuwe dimensie met behulp van de subtekenreekstransformatie op het tabblad `audienceMembershipId` veld voor het omzetten van de tekenreeks met door komma&#39;s gescheiden waarden in een array. OPMERKING: momenteel is er een limiet van 10 waarden in de array .
   1. U kunt nu verslag uitbrengen over deze nieuwe dimensie `audienceMembershipIds` binnen werkruimte Customer Journey Analytics.
