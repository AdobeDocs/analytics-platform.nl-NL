---
title: AEP-publiek opnemen in Customer Journey Analytics
description: Verklaart hoe te om AEP publiek in Customer Journey Analytics voor verdere analyse op te nemen.
solution: Customer Journey Analytics
feature: Use Cases
exl-id: cb5a4f98-9869-4410-8df2-b2f2c1ee8c57
source-git-commit: 9c4869bb632f3d69d8704009744246b975cb5c4a
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 0%

---

# AEP-publiek opnemen in Customer Journey Analytics (CJA)

Deze gebruikszaak verkent een tijdelijke, handmatige manier om Adobe Experience Platform (AEP)-publiek naar CJA te brengen. Dit publiek zou in de Bouwer van het Segment van AEP, of Adobe Audience Manager, of andere hulpmiddelen kunnen gecreeerd zijn, en opgeslagen in het Profiel van de Klant in real time (RTCP). Het publiek bestaat uit een set profiel-id&#39;s, samen met eventuele toepasselijke kenmerken/gebeurtenissen/enzovoort. en wij willen hen in de Werkruimte van CJA voor analyse brengen.

## Vereisten

* Toegang tot Adobe Experience Platform (AEP), in het bijzonder Real-time Klantprofiel.
* Toegang tot AEP-schema&#39;s en gegevenssets maken/beheren.
* Toegang tot AEP Query Service (en de mogelijkheid om SQL te schrijven) of een ander hulpmiddel om bepaalde lichte transformaties uit te voeren.
* Toegang tot Customer Journey Analytics. U moet een CJA-productbeheerder zijn om CJA-verbindingen en gegevensweergaven te maken/wijzigen.
* Mogelijkheid om de Adobe-API&#39;s te gebruiken (segmentatie, optioneel andere)

## Stap 1: Kies een of meer doelgroepen in het profiel voor realtime klanten {#audience}

Adobe Experience Platform [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en) (RTCP) laat u een holistische mening van elke individuele klant zien door gegevens van veelvoudige kanalen, met inbegrip van online, off-line, CRM, en derde te combineren.

U hebt waarschijnlijk al een publiek in RTCP dat uit diverse bronnen kan zijn gekomen. Kies een of meer soorten publiek om in CJA in te nemen.

## Stap 2: Een profielgegevensset voor Unie maken voor het exporteren

Om het publiek naar een dataset uit te voeren die uiteindelijk aan een verbinding in CJA kan worden toegevoegd, moet u een dataset tot stand brengen het waarvan schema een Profiel is [Unieschema](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=en#understanding-union-schemas).

De schema&#39;s van de unie zijn samengesteld uit veelvoudige schema&#39;s die de zelfde klasse delen en voor Profiel toegelaten. Met het samenvoegingsschema kunt u een samenvoeging zien van alle velden in schema&#39;s die dezelfde klasse delen. Het Profiel van de Klant in real time gebruikt het verenigingsschema om een holistische mening van elke individuele klant tot stand te brengen.

## Stap 3: Een publiek naar de profielunie exporteren via een API-aanroep {#export}

Alvorens u een publiek in CJA kunt brengen, moet u het naar een dataset van AEP uitvoeren. Dit kan alleen worden gedaan met de segmentatie-API, en met name met de [API-eindpunt voor taken exporteren](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en).

U kunt een uitvoerbaan tot stand brengen gebruikend publiekidentiteitskaart van uw keus, en de resultaten in de dataset van de Vereniging van het Profiel zetten AEP u in Stap 2 creeerde. Hoewel u verschillende kenmerken/gebeurtenissen voor het publiek kunt exporteren, hoeft u alleen het veld met de specifieke profiel-id te exporteren dat overeenkomt met het veld met de persoon-id dat wordt gebruikt in de CJA-verbinding waarop u wilt gaan tekenen (zie onder in Stap 5).

## Stap 4: De exportuitvoer bewerken

De resultaten van de exporttaak moeten worden omgezet in een afzonderlijke profielgegevensset om te worden opgenomen in CJA.  Deze transformatie kan worden uitgevoerd met [AEP Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=en)of een ander transformatiegereedschap van uw keuze. We hebben alleen de profiel-id (die overeenkomt met de persoon-id in CJA) en een of meer gebruikers-id(&#39;s) nodig om de rapportage in CJA uit te voeren.

De standaard exporttaak bevat echter meer gegevens en daarom moeten we deze uitvoer bewerken om irrelevante gegevens te verwijderen en enkele zaken te verplaatsen.  Ook, moet u een schema/dataset eerst tot stand brengen alvorens u de getransformeerde gegevens aan het toevoegt.

Hier is een voorbeeld van de uitvoeroutput in de de verenigingsdataset van het Profiel, **voor** alle bewerkingen:

![Onbewerkte uitvoer](assets/export-unedited.png)

Let op het volgende:

* De gebruikers-id staat onder `segmentmembership.ups.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.status`.
* De status moet &quot;gerealiseerd&quot; of &quot;binnengekomen&quot; zijn, maar niet &quot;verlaten&quot;.

Dit is het formaat van de dataset van het Profiel die u in CJA kunt verzenden.

![Bewerkte uitvoer](assets/export-edited.png)

Hier volgen de gegevenselementen die aanwezig moeten zijn:

* `_aresprodvalidation` tekenreeksveld: Verwijst naar uw organisatie-id. U zult anders zijn.
* `personID` tekenreeksveld: Dit is het standaard XDM schemagebied op de datasets van het Profiel om de persoon te identificeren. Gebruik de profiel-id van het exporteren.
* `audienceMembershipId` tekenreeksveld: De gebruikers-id uit de exportbewerking.  OPMERKING: Dit veld kan een naam krijgen die u maar wilt (vanuit uw eigen schema).
* Voeg een vriendelijke naam voor het publiek toe (`audienceMembershipIdName`), zoals

   ![Vriendelijke publieksnaam](assets/audience-name.png)

* Voeg desgewenst andere publieksmetagegevens toe.

## Stap 5: Deze profielgegevensset toevoegen aan een bestaande verbinding in CJA

U kunt [een nieuwe verbinding maken](/help/connections/create-connection.md), maar de meeste klanten zullen de dataset van het Profiel aan een bestaande verbinding willen toevoegen. De gebruikers-id&#39;s verrijken de bestaande gegevens in CJA.

## Stap 6: Bestaande CJA-gegevensweergave wijzigen (of nieuwe CJA-gegevensweergave maken)

Toevoegen `audienceMembershipId`, `audienceMembershipIdName` en `personID` in de gegevensweergave.

## Stap 7: Rapport in werkruimte

U kunt nu rapporteren over `audienceMembershipId`, `audienceMembershipIdName` en `personID` in Workspace.

## Aanvullende opmerkingen

* U zou dit proces op een regelmatige kadentie moeten uitvoeren, zodat de publieksgegevens constant binnen CJA worden verfrist.
* U kunt meerdere soorten publiek importeren binnen één CJA-verbinding. Dit vergroot de complexiteit van het proces, maar het is mogelijk. Dit werkt alleen als u enkele wijzigingen aanbrengt in het bovenstaande proces:
   1. Voer dit proces voor elk gewenst publiek in uw publieksinzameling binnen RTCP uit.
   1. Wanneer u de transformaties van de uitvoer van de exporttaak uitvoert, moet u een lijst maken met `audienceMembershipId(s)`, omdat één CJA-persoon-id tot meerdere soorten publiek kan behoren. Op een gegeven moment in de toekomst zal CJA arrays/objectarrays in profieldatasets ondersteunen. Wanneer deze worden ondersteund, gebruikt u een array met objecten voor de `audienceMembershipId` of `audienceMembershipIdName` is de beste optie. Extraheer in de tussentijd alle huidige gebruikers-id&#39;s voor elke profiel-id in de uitvoer-taakuitvoer (met de status &quot;gereed&quot; of &quot;ingevoerd&quot;) en plaats deze in een tekenreeks met door komma&#39;s gescheiden waarden (dat wil zeggen, `<id1>,<id2>,...`).  Als er een publiek-id is met de status &quot;exited&quot;, controleert u of deze zich NIET in de lijst bevindt.  Als u de vriendschappelijke naamvereniging met identiteitskaart wilt handhaven, kunt u het op het eind van elke identiteitskaart in de lijst (samen met andere meta-gegevens) vastmaken.
   1. Maak in de gegevensweergave een nieuwe dimensie met behulp van de subtekenreekstransformatie op het tabblad `audienceMembershipId` veld voor het omzetten van de tekenreeks met door komma&#39;s gescheiden waarden in een array. OPMERKING: momenteel is er een limiet van 10 waarden in de array .
   1. U kunt nu verslag uitbrengen over deze nieuwe dimensie `audienceMembershipIds` in CJA Workspace.
