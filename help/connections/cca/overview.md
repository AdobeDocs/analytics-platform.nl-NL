---
title: Overzicht van kanaalanalyse
description: Identiteitskaart van de bezoeker van hersleutel van veelvoudige datasets om bezoekers samen te binden.
translation-type: tm+mt
source-git-commit: 23a7a52ed6fc0a39ce1466a6d7b658dbdf7c6c14
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---


# Overzicht van kanaalanalyse

**Reis-IQ: De** Analyse van het Kanaal een eigenschap die u toestaat om identiteitskaart van de persoon van een dataset opnieuw aan te wijzen, die een naadloze combinatie veelvoudige datasets toelaat. CCA bekijkt gebruikersgegevens van zowel voor authentiek verklaarde als niet voor authentiek verklaarde zittingen om een vastgemaakte identiteitskaart te produceren. Met Kanaaloverschrijdende analyse kunt u vragen beantwoorden zoals:

* Hoeveel mensen beginnen met hun ervaring in één kanaal, en eindigen het in een andere?
* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt het aanwijzen van campagnes die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn inzicht in de doeltreffendheid van campagnes als ik rekening houd met cross-device reizen? Hoe verandert mijn trechter-analyse?
* Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze?
* Hoe verschilt het gedrag van gebruikers met meerdere apparaten van de gebruikers met één apparaat?

Wanneer u datasets met gelijkaardige persoon IDs combineert, wordt de attributie gedragen over apparaten en kanalen. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Die gebruiker ontmoet een kwestie met hun orde, dan geeft uw team van de klantendienst een vraag om het te helpen oplossen. Met de Analytics van het Kanaal, kunt u vraag centrumgebeurtenissen aan de advertentie toeschrijven die zij oorspronkelijk klikte.

## Vereisten

>[!IMPORTANT]
>
>Het nalaten om aan alle voorwaarden te voldoen kan in de oncapaciteit resulteren om een verbinding CCA of slechte resultaten tot stand te brengen wanneer het combineren van datasets.

Voordat u de functie Kanaalanalyse gebruikt, moet u controleren of uw organisatie is voorbereid met behulp van het volgende:

* Eén gegevensset in Adobe Experience Platform moet uit twee kolommen bestaan waarmee bezoekers kunnen worden geïdentificeerd:
   * A **persistent ID**, een identifier aanwezig op elke rij. Bijvoorbeeld een bezoekersidentiteitskaart die door een bibliotheek van Adobe Analytics AppMeasurement wordt geproduceerd.
   * A **transient ID**, een herkenningsteken aanwezig op slechts enkele rijen. Een gehashte gebruikersnaam of e-mailadres bijvoorbeeld wanneer een bezoeker de verificatie uitvoert. U kunt vrijwel elke gewenste id gebruiken, mits deze minstens één keer aanwezig is op dezelfde gebeurtenis als een bepaalde permanente id.
* Een andere dataset, zoals de gegevens van het vraagcentrum, die een transient identiteitskaart op elke rij bevat. Deze persoon-id moet op dezelfde manier worden opgemaakt als de tijdelijke id in de andere dataset.
* Met deze functie kunt u gegevenssets samenvoegen die het samenvoegen van geverifieerde en niet-geverifieerde gebruikersgegevens kunnen omvatten. Zorg ervoor dat u voldoet aan de toepasselijke wetten en regels, inclusief het verkrijgen van de benodigde machtigingen voor eindgebruikers, voordat u gegevenssets samenvoegt.

## Beperkingen

De Kanaalanalyse is een baanbrekende en robuuste eigenschap, maar heeft beperkingen op hoe het kan worden gebruikt.

* De huidige mogelijkheden voor opnieuw aanvragen zijn beperkt tot één stap (permanente id tot tijdelijke id). Het opnieuw activeren in meerdere stappen (bijvoorbeeld een blijvende id naar een tijdelijke id en een andere tijdelijke id) wordt niet ondersteund.
* Alleen gegevenssets voor gebeurtenissen worden ondersteund. Andere datasets, zoals raadplegingsdatasets, worden niet gesteund.
* Aangepaste id-kaarten die in uw organisatie worden gebruikt, worden niet ondersteund.
* De Adobe-grafiek en de privégrafiek worden niet ondersteund.
* Met Kanaaloverschrijdende analyse wordt het veld dat wordt gebruikt voor stitching op geen enkele manier getransformeerd. Op velden gebaseerde stitching gebruikt de waarde in het opgegeven veld zoals deze bestaat in de ongeordende dataset in het gegevensmeer. Als bijvoorbeeld soms het woord &#39;Bob&#39; in het veld wordt weergegeven en soms het woord &#39;BOB&#39; wordt weergegeven, worden deze als twee aparte personen behandeld.


## Kanaaloverschrijdende analyse inschakelen

Zodra uw organisatie aan alle voorwaarden voldoet en zijn beperkingen begrijpt, kunt u deze stappen volgen beginnen het in CJA te gebruiken.

1. Importeer de gewenste gegevens naar Adobe Experience Platform. Zie [Een schema maken](https://docs.adobe.com/content/help/en/experience-platform/xdm/tutorials/create-schema-ui.html) en [Gegevens invoegen](https://docs.adobe.com/content/help/en/experience-platform/ingestion/home.html) in de documentatie van Adobe Experience Platform.
1. Neem contact op met uw accountmanager van Adobe, die het volgende bevat:
   * Een verzoek om Kanaaloverschrijdende analyse in te schakelen
   * De dataset-id voor de gegevensset die u opnieuw wilt gebruiken
   * De kolomnaam van blijvende identiteitskaart voor de gewenste dataset (Herkenningsteken die op elke rij verschijnt)
   * De kolomnaam van transient identiteitskaart voor gewenste dataset (de verbinding van persoonsidentificatie tussen datasets)
   * Uw voorkeur van [replay](replay.md) frequentie en raadplegingslengte. De opties omvatten een replay eens per week met een 7 dagen terugkijkvenster, of een replay elke dag met een 1 dag terugkijkvenster.
1. De Adobe Account Manager schakelt Channel Analytics in bij het ontvangen van uw verzoek. Als deze optie is ingeschakeld, wordt in Adobe Experience Platform een nieuwe gegevensset met een nieuwe ID-kolom weergegeven. Uw Adobe Account Manager kan de nieuwe gegevensset-id en de kolomnaam van de persoon-id opgeven.
1. [Creeer een ](../create-connection.md) verbinding in CJA gebruikend de onlangs geproduceerde dataset en om het even welke andere datasets die u wilt omvatten. Kies correcte persoon identiteitskaart voor elke dataset.
1. [Maak een ](/help/data-views/create-dataview.md) gegevensweergave op basis van de verbinding.

<!-- To do: Paragraph on backfill once product and marketing determine the best way forward. -->

Zodra de gegevensmening opstelling is, is de Analyse in CJA enkel als een andere analyse in CJA, behalve nu de gegevens over kanalen en apparaten werken.
