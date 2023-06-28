---
title: Overzicht van kanaalanalyse
description: Identiteitskaart van de re-zeer belangrijke persoon van veelvoudige datasets aan naakte personen samen.
exl-id: 69763313-de27-4487-8e32-8277f1f693d8
solution: Customer Journey Analytics
feature: Cross-Channel Analytics
hide: true
hidefromtoc: true
source-git-commit: cf6da1f126933f17e05fb458f52dff93c1601891
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# Overzicht van kanaalanalyse

**Reis-IQ: Kanaaloverschrijdende analyse** is een eigenschap die u toestaat om identiteitskaart van de persoon van een dataset re-zeer belangrijk te maken, die een naadloze combinatie veelvoudige datasets toelaat. CCA bekijkt gebruikersgegevens van zowel voor authentiek verklaarde als niet voor authentiek verklaarde zittingen om een vastgemaakte identiteitskaart te produceren. Met Kanaaloverschrijdende analyse kunt u vragen beantwoorden zoals:

* Hoeveel mensen beginnen met hun ervaring in één kanaal, en eindigen het in een andere?
* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt het aanwijzen van campagnes die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn begrip van campagnedoeltreffendheid als ik rekening houd met apparatuurreizen? Hoe verandert mijn trechter-analyse?
* Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze?
* Hoe verschilt het gedrag van gebruikers met meerdere apparaten van de gebruikers met één apparaat?

Wanneer u datasets met gelijkaardige persoon IDs combineert, wordt de attributie gedragen over apparaten en kanalen. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Die gebruiker ontmoet een kwestie met hun orde, dan geeft uw team van de klantendienst een vraag om het te helpen oplossen. Met de Analytics van het Kanaal, kunt u vraag centrumgebeurtenissen aan de advertentie toeschrijven die zij oorspronkelijk klikte.

## Vereisten

>[!IMPORTANT]
>
>Het nalaten om aan alle voorwaarden te voldoen kan in de oncapaciteit resulteren om een verbinding CCA of slechte resultaten tot stand te brengen wanneer het combineren van datasets.

Voordat u de functie Kanaalanalyse gebruikt, moet u controleren of uw organisatie is voorbereid met behulp van het volgende:

* Eén gegevensset in Adobe Experience Platform moet uit twee kolommen bestaan waarmee u personen kunt identificeren:
   * A **blijvende id**, een id aanwezig op elke rij. Bijvoorbeeld een persoon-id die is gegenereerd door een Adobe Analytics-AppMeasurement-bibliotheek.
   * A **transient ID**, een id die alleen op bepaalde rijen voorkomt. Een gehashte gebruikersnaam of e-mailadres bijvoorbeeld wanneer een persoon de verificatie uitvoert. U kunt vrijwel elke gewenste id gebruiken, mits deze minstens één keer aanwezig is op dezelfde gebeurtenis als een bepaalde permanente id.
* Een andere dataset, zoals de gegevens van het vraagcentrum, die een transient identiteitskaart op elke rij bevat. Deze persoon-id moet op dezelfde manier worden opgemaakt als de tijdelijke id in de andere dataset.
* Met deze functie kunt u gegevenssets samenvoegen die het samenvoegen van geverifieerde en niet-geverifieerde gebruikersgegevens kunnen omvatten. Zorg ervoor dat u voldoet aan de toepasselijke wetten en regels, inclusief het verkrijgen van de benodigde machtigingen voor eindgebruikers, voordat u gegevenssets samenvoegt.

## Beperkingen

>[!IMPORTANT]
>
>Om het even welke verandering in het globale schema van de gebeurtenisdataset moet ook in het nieuwe gestikte datasetschema worden toegepast, anders zal het de gestikte dataset breken.
>
>Ook, als u de brondataset verwijdert, stopt de gestikte dataset verwerking en wordt verwijderd door het systeem.

De Kanaalanalyse is een baanbrekende en robuuste eigenschap, maar heeft beperkingen op hoe het kan worden gebruikt.

* De huidige mogelijkheden voor opnieuw aanvragen zijn beperkt tot één stap (permanente id tot tijdelijke id). Het opnieuw activeren in meerdere stappen (bijvoorbeeld een blijvende id naar een tijdelijke id en een andere tijdelijke id) wordt niet ondersteund.
* Alleen gegevenssets voor gebeurtenissen worden ondersteund. Andere datasets, zoals raadplegingsdatasets, worden niet gesteund.
* Aangepaste id-kaarten die in uw organisatie worden gebruikt, worden niet ondersteund.
* De persoonlijke grafiek voor meerdere apparaten wordt niet ondersteund.
* Met Kanaaloverschrijdende analyse wordt het veld dat wordt gebruikt voor stitching op geen enkele manier getransformeerd. Op velden gebaseerde stitching gebruikt de waarde in het opgegeven veld zoals deze bestaat in de ongeordende dataset in het gegevensmeer. Het hechten proces is hoofdlettergevoelig. Als bijvoorbeeld soms het woord &#39;Bob&#39; in het veld wordt weergegeven en soms het woord &#39;BOB&#39; wordt weergegeven, worden deze als twee aparte personen behandeld.
* Op bepaalde gebieden-gebaseerde het stitching is case-sensitive, voor de datasets van Analytics die door de Bron van de Analyse wordt geproduceerd Schakelaar, adviseert Adobe om het even welke regels van VISTA of verwerkingsregels te herzien die op het transient gebied van identiteitskaart van toepassing zijn om ervoor te zorgen dat geen van deze regels nieuwe vormen van zelfde identiteitskaart introduceert. U moet er bijvoorbeeld voor zorgen dat er geen VISTA- of verwerkingsregels zijn die een lagere waarde voor het overgangsveld Id invoeren voor slechts een deel van de gebeurtenissen.
* Veldgebaseerde stitching combineert of voegt geen velden samen.
* Het veld Tijdelijke id moet één type id bevatten (d.w.z. id&#39;s uit één naamruimte). Het veld Tijdelijke id mag bijvoorbeeld geen combinatie bevatten van aanmeldings-id&#39;s en e-mailid&#39;s.
* Als er meerdere gebeurtenissen voorkomen met dezelfde tijdstempel voor dezelfde permanente id, maar met verschillende waarden in het overgangsveld voor de id, wordt voor veldoverstikking gekozen op basis van alfabetische volgorde. Dus als de blijvende id A twee gebeurtenissen heeft met dezelfde tijdstempel en een van de gebeurtenissen Bob opgeeft en de andere id Ann opgeeft, kiest u Ann in het veld.
* Als een apparaat door veelvoudige mensen wordt gedeeld en het totale aantal overgangen tussen gebruikers overschrijdt 50.000, houdt CCA ophoudt stitching gegevens voor dat apparaat.


## Kanaaloverschrijdende analyse inschakelen

Zodra uw organisatie aan alle voorwaarden voldoet en zijn beperkingen begrijpt, kunt u deze stappen volgen beginnen het in Customer Journey Analytics te gebruiken.

1. Importeer de gewenste gegevens naar Adobe Experience Platform. Voor Adobe Analytics-gegevens raadpleegt u [Adobe Analytics-rapportenpakket-gegevens gebruiken in Customer Journey Analytics](/help/getting-started/aa-vs-cja/aa-data-in-cja.md). Voor andere soorten gegevens raadpleegt u [Een schema maken](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html) en [Gegevens samenvoegen](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html) in de documentatie van Adobe Experience Platform.
1. Neem contact op met de klantenondersteuning van Adobe via de volgende informatie:
   * Een verzoek om Kanaaloverschrijdende analyse in te schakelen
   * De dataset-id voor de gegevensset die u opnieuw wilt gebruiken
   * De kolomnaam van blijvende identiteitskaart voor de gewenste dataset (Herkenningsteken die op elke rij verschijnt)
   * De kolomnaam van transient identiteitskaart voor gewenste dataset (de verbinding van persoonsidentificatie tussen datasets)
   * Je voorkeur van [replay](replay.md) frequentie en terugkijklengte. De opties omvatten een replay eens per week met een 7 dagen terugkijkvenster, of een replay elke dag met een 1 dag terugkijkvenster
   * Naam van sandbox.
1. De Klantenondersteuning van Adobe werkt samen met Adobe-engineering om Kanaalanalyse mogelijk te maken wanneer u uw verzoek ontvangt. Als deze optie is ingeschakeld, wordt in Adobe Experience Platform een nieuwe gegevensset met een nieuwe kolom met personen-id weergegeven. Adobe Klantenondersteuning kan de nieuwe gegevensset-id en de kolomnaam van de persoon-id opgeven.
1. Als Adobe voor het eerst wordt ingeschakeld, wordt een back-up van de gegevens met een stitched-functie gemaakt die teruggaat tot het begin van de vorige maand (tot 60 dagen). Om deze backfill te kunnen uitvoeren, moet de tijdelijke id zo lang in de niet-opgeslagen gegevens aanwezig zijn.
1. [Verbinding maken](/help/connections/create-connection.md) in Customer Journey Analytics die de onlangs geproduceerde dataset en andere datasets gebruiken die u wilt omvatten. Kies correcte persoon identiteitskaart voor elke dataset.
1. [Een gegevensweergave maken](/help/data-views/create-dataview.md) op basis van de verbinding.

<!-- To do: Paragraph on backfill once product and marketing determine the best way forward. -->

Zodra de gegevensmening opstelling is, is de analyse in Customer Journey Analytics enkel als een andere analyse in Customer Journey Analytics, behalve nu werkt de gegevens over kanalen en apparaten.
