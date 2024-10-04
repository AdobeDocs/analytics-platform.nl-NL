---
title: Een publiek maken en publiceren naar het realtime profiel van de klant
description: Leer hoe u publiek kunt publiceren vanuit Customer Journey Analytics
exl-id: 0221f9f1-df65-4bd6-a31d-33d1a1ba0cfe
feature: Audiences
role: User
source-git-commit: e131fd78ceee67a05a1ea7256e58b4b34ce44ae5
workflow-type: tm+mt
source-wordcount: '1865'
ht-degree: 1%

---

# Soorten publiek maken en publiceren {#create-and-publish-audiences}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_audiences_refreshfrequency"
>title="Frequentie vernieuwen"
>abstract="Zie hoe vaak het lidmaatschap van een publiek opnieuw wordt beoordeeld.<br/> Één keer wordt het publiek geëvalueerd slechts eenmaal."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_components_audiences_audiencelimit"
>title="Audioregimiet"
>abstract="Het vernieuwen van het publiek is beperkt op basis van hoe vaak ze worden vernieuwd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_component_audiences_refreshlookbackwindow"
>title="Zoekvenster vernieuwen"
>abstract="Definieer het aantal terugzoekdagen vanaf vandaag waaruit een publiek wordt geëvalueerd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_component_audiences_audiencesizelimit"
>title="Limiet voor doelgrootte"
>abstract="Het publiek mag niet meer dan 20 miljoen leden tellen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_component_audiences_namespacesincluded"
>title="Ingesloten naamruimten"
>abstract="De identiteiten in dit publiek bestaan uit de onderstaande naamruimten."

<!-- markdownlint-enable MD034 -->




Dit onderwerp bespreekt hoe te om publiek tot stand te brengen en te publiceren dat in Customer Journey Analytics aan [ in real time het Profiel van de Klant ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/home) in Adobe Experience Platform voor klant wordt geïdentificeerd die en verpersoonlijking richt.

Lees dit [ overzicht ](/help/components/audiences/audiences-overview.md) om met het concept publiek van de Customer Journey Analytics vertrouwd te maken.

## Een publiek maken en publiceren {#create}

1. Voer een van de volgende handelingen uit om een publiek te maken en te publiceren:

   | Aanmaakmethode | Details |
   | --- | --- |
   | Vanuit de **[!UICONTROL Audiences]** -interface. | Selecteer **[!UICONTROL Components]** > **[!UICONTROL Audiences]** in het hoofdmenu Customer Journey Analytics. De interface van het publiek toont. Selecteer **[!UICONTROL Create audience]** maken en [!UICONTROL Audience builder] wordt geopend. |
   | Vanuit een visualisatie in Analysis Workspace | Met veel visualisaties in Analysis Workspace kunt u een publiek maken via het contextmenu. Bijvoorbeeld, kunt u **[!UICONTROL Create audience]** van het contextmenu van een punt in a [ Freeform lijst ](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) of een knoop in [ het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md) selecteren.<p>Met deze methode wordt het filter in de Audience Builder vooraf gevuld met de dimensie of het dimensie-item dat u hebt geselecteerd.</p><p>Met de volgende visualisaties kunt u een publiek maken via het snelmenu:</p><ul><li>[ Lijst van de Cohort ](/help/analysis-workspace/visualizations/cohort-table/cohort-analysis.md)</li><li>[Uitval](/help/analysis-workspace/visualizations/fallout/fallout-flow.md)</li><li>[Stroom](/help/analysis-workspace/visualizations/c-flow/flow.md)</li><li>[Vrije-vormentabel](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md)</li><li>[ het canvas van de Reis ](/help/analysis-workspace/visualizations/journey-canvas/journey-canvas.md)</li><li>[Venn](/help/analysis-workspace/visualizations/venn.md)</li></ul><p>**Nota:** het publiek kan berekende metriek niet omvatten. Als u probeert om een publiek tot stand te brengen dat berekende metrisch bevat, is berekende metrisch niet inbegrepen in de publieksdefinitie.</p> |
   | Via de interface voor het maken/bewerken van filters | Schakel het vakje met de tekst **[!UICONTROL Create an audience from this filter]** in. Met deze methode wordt het filter vooraf gevuld. Zie [ filters ](/help/components/filters/create-filters.md) voor meer informatie creëren. |

   {style="table-layout:auto"}

1. Bouw het publiek gebruikend de [ bouwer van de Publiek ](#audience-builder).

1. Interpreteer de gegevens gebruikend het [ voorproef van de Datum ](#data-preview) paneel.

1. Selecteer **[!UICONTROL [!UICONTROL View sample IDs]]** om een voorbeeld van id&#39;s in dit publiek weer te geven. In de **[!UICONTROL Sample IDs]** dialoog kunt u ![ Onderzoek ](/help/assets/icons/Search.svg) gebruiken [!UICONTROL *steekproef IDs van het Onderzoek*] om steekproef IDs te zoeken.

1. Controleer de publieksconfiguratie en selecteer **[!UICONTROL Publish]**.
U ontvangt een bevestigingsbericht dat het publiek wordt gepubliceerd. Publicatie duurt slechts een minuut of twee voordat dit publiek in Experience Platform verschijnt.

1. Selecteer **[!UICONTROL View audience in AEP]** binnen het zelfde bericht en u wordt genomen aan [ Segment UI ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/overview) in Adobe Experience Platform. Zie hieronder voor meer informatie.

## Audience builder

Configureer deze instellingen om uw publiek te definiëren of bij te werken.

![ Schermafbeelding van creeer een publiek die montages boeien in de volgende sectie worden beschreven.](assets/create-audience.png)

| Instelling | Beschrijving |
| --- | --- |
| ![ Gegevens ](/help/assets/icons/Data.svg) | Selecteer de gegevensweergave die u wilt gebruiken voor het maken van een publiek. |
| **[!UICONTROL Name]** | De naam van het publiek. Bijvoorbeeld: `Really Interested in Potential Car Buyers` |
| **[!UICONTROL Tags]** | Alle tags die u aan het publiek wilt toewijzen voor organisatorische doeleinden. U kunt een of meer bestaande tags selecteren of een nieuwe tags invoeren. |
| **[!UICONTROL Description]** | Een beschrijving van het publiek, om het van anderen te onderscheiden. Bijvoorbeeld: `Build an audience of really interested potential car buyers` |
| **[!UICONTROL Refresh frequency]** | De frequentie waarmee u het publiek wilt vernieuwen.<p/>U kunt kiezen tussen <ul><li>**[!UICONTROL One time]** publiek: een publiek (standaard) dat niet hoeft te worden vernieuwd. Deze optie kan bijvoorbeeld handig zijn voor specifieke, eenmalige campagnes.<br/> u moet specificeren a **[!UICONTROL One time date range]**. U kunt ![ Kalender ](/help/assets/icons/Calendar.svg) gebruiken om een datumwaaier in te gaan.</li><li>Een verfrissend publiek. U kunt uit de volgende opties selecteren:<ul><li>**[!UICONTROL Every 4 hour]** s: een publiek dat om de 4 uur verfrist.</li><li>**[!UICONTROL Daily]**: een publiek dat dagelijks vernieuwt</li><li>**[!UICONTROL Weekly]** : een publiek dat wekelijks vernieuwt.</li><li>**[!UICONTROL Monthly]**: een publiek dat maandelijks vernieuwt</li></ul></li><br/> voor het verfrissen van publiek, moet u specificeren:<ul><li>**[!UICONTROL Refresh lookback window]**. Definieer het aantal terugzoekdagen vanaf vandaag dat een publiek wordt geëvalueerd. U kunt opties selecteren of een aangepaste tijd definiëren. Het maximum is 90 dagen.</li><li>**[!UICONTROL Expiration date]**: Definieer wanneer het publiek stopt met vernieuwen. U kunt ![ Kalender ](/help/assets/icons/Calendar.svg) gebruiken om een datum te selecteren. De standaardwaarde is 1 jaar vanaf de aanmaakdatum. Het uitbreiden van het publiek wordt gelijkaardig behandeld aan het verlopen van geplande rapporten. De beheerder krijgt een maand voordat het publiek vervalt een e-mail.</li></ul> Let op: er geldt een limiet van 75 tot 150 publieksvernieuwingen, afhankelijk van de machtiging van uw Customer Journey Analytics.</li></ul> |
| **[!UICONTROL Filter]** | Filters zijn de belangrijkste invoer voor het publiek. De belemmering en laat vallen één of meerdere filters van het linker ![ deelvenster van de Segmentatie ](/help/assets/icons/Segmentation.svg) **[!UICONTROL Filter]** op het gebied van de Filter. U kunt het ![ Onderzoek ](/help/assets/icons/Search.svg) gebruiken [!UICONTROL *filters van het Onderzoek*] om naar filters te zoeken. U kunt maximaal 20 filters toevoegen. Filters kunnen worden gekoppeld met **[!UICONTROL And]** - of **[!UICONTROL Or]** -operatoren.<p>Wanneer u een publiek maakt op basis van een visualisatie in Analysis Workspace (zoals een vrije-vormtabel of het canvas Reis), blijven alle filters behouden die op het deelvenster of de kolom zijn toegepast. U kunt alle filters verwijderen die automatisch worden toegepast.</p> |
| **[!UICONTROL Data preview]** | Selecteer ![ Info ](/help/assets/icons/Info.svg) om de [ voorproef van Gegevens ](#data-preview) voor de geselecteerde datumwaaier te tonen of te verbergen. |

## Gegevensvoorbeeld

Het deelvenster Gegevensvoorbeeld bevat de volgende informatie.

| Element | Beschrijving |
| --- | --- |
| **[!UICONTROL Total people]** | Een samenvattingsnummer van het totale aantal personen in dit publiek. De maximale grootte is 20 miljoen mensen. Als uw publiek meer dan 20 miljoen mensen telt, moet u de doelgrootte reduceren voordat u kunt publiceren. |
| **[!UICONTROL Audience size limit]** | Visualisatie om te laten zien hoe ver dit publiek verwijderd is van de 20 miljoen grens. |
| **[!UICONTROL Estimated audience return]** | U kunt deze waarde gebruiken om personen in dit publiek die terugkeren naar uw site, mobiele app of een ander kanaal opnieuw als doel in te stellen.<p>U kunt het tijdkader (**[!UICONTROL Next 7 days]**, **[!UICONTROL Next 2 weeks]**, of **[!UICONTROL Next month]**) voor het geschatte aantal klanten selecteren die kunnen terugkeren. |
| **[!UICONTROL Estimated to return]** | Dit aantal geeft u een geschat aantal terugkerende klanten over het tijdkader dat u selecteerde. Dit aantal wordt voorspeld gebruikend het historische kinnetarief voor dit publiek. |
| **[!UICONTROL Preview metrics]** | U kunt specifieke metrisch selecteren om te zien hoe de gegevens voor dat metrisch is gebaseerd op het publiek u bepaalt.  Elke metrische vertoningen van de Voorproef een totaal voor metrisch die op het publiek wordt gebaseerd. En een percentage van het publiek baseerde metrisch van het algemene totaal van metrisch, zoals die door de gegevensmening wordt bepaald. 381 personen (de metrische waarde die u hebt geselecteerd) zijn bijvoorbeeld het resultaat van uw publieksdefinitie. Dit is 5% van het totale aantal personen dat beschikbaar is in de gegevensweergave. U kunt elke metrische waarde selecteren die beschikbaar is in de gegevensweergave. |
| **[!UICONTROL Namespaces included]** | De specifieke naamruimten die zijn gekoppeld aan de personen in uw publiek. Voorbeelden zijn ECID, CRM-id, e-mailadressen enzovoort. |
| **[!UICONTROL Sandbox]** | De [ zandbak van het Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) waarin dit publiek verblijft. Wanneer u dit publiek publiceert naar Platform, kunt u alleen met het publiek werken binnen de grenzen van deze sandbox. |

{style="table-layout:auto"}

## Wat gebeurt er nadat een publiek is gemaakt en gepubliceerd? {#after-audience-created}

Nadat u een publiek in de Customer Journey Analytics creeert en publiceert, is het publiek beschikbaar in Experience Platform. Er wordt alleen een Adobe Experience Platform-streamingsegment gemaakt als uw organisatie is ingesteld op streamingsegmentatie.

* Het publiek in Platform deelt de zelfde naam en de beschrijving zoals het publiek van de Customer Journey Analytics. De naam wordt toegevoegd met de Customer Journey Analytics publiek-id om ervoor te zorgen dat het publiek uniek is.
* Wijzigingen die worden aangebracht in de naam of beschrijving van het publiek in de Customer Journey Analytics, worden weerspiegeld in het Experience Platform.
* Als een publiek in Customer Journey Analytics wordt geschrapt, blijft het publiek beschikbaar in Experience Platform.

## Latentieoverwegingen {#latency}

Op verschillende momenten vóór, tijdens en na het publiceren van de doelgroep kunnen er latentie optreden. Hier volgt een overzicht van mogelijke vertragingen.

![ Latenties in publiek het publiceren zoals die in deze sectie worden beschreven.](assets/latency-diagram.svg)

|  | Latentiepunt | Latentieduur |
| --- | --- | --- |
| Niet weergegeven | Adobe Analytics naar Analytics-bronconnector (A4T) | Tot 30 minuten |
| 1 | Gegevensopname in het gegevensmeer (van de bronconnector van Analytics of andere bronnen) | Tot 90 minuten |
| 2 | Gegevensopname van Experience Platform Data Lake naar Customer Journey Analytics | Tot 90 minuten |
| 3 | Publiceren van het publiek aan het Profiel van de Klant in real time, met inbegrip van automatische verwezenlijking van het het stromen segment, en het toestaan van het segment klaar om de gegevens te ontvangen. | Enkele seconden |
| 4 | Frequentie vernieuwen voor publiek | <ul><li>Eenmalige vernieuwing (vertraging van minder dan 5 minuten)</li><li>Vernieuwen elke 4 uur, dagelijks, wekelijks, maandelijks (latentie gaat hand in hand met de vernieuwingsfrequentie) |
| 5 | Doel maken in Adobe Experience Platform: het nieuwe segment activeren | 1-2 uur |

{style="table-layout:auto"}

## Customer Journey Analytics publiek in Experience Platform gebruiken {#audiences-aep}

Customer Journey Analytics neemt alle naamruimte- en id-combinaties van uw gepubliceerde publiek en streamt deze naar Real-time Customer Data Platform. Customer Journey Analytics verzendt het publiek naar Experience Platform met de primaire identiteitsreeks, volgens wat als [!UICONTROL Person ID] werd geselecteerd toen de verbinding werd gevormd.

Real-time Customer Data Platform controleert vervolgens elke naamruimte/ID-combinatie en zoekt naar een profiel waarvan het deel kan uitmaken. Een profiel is in feite een cluster van gekoppelde naamruimten, id&#39;s en apparaten. Als er een profiel wordt gevonden, worden de naamruimte en de id toegevoegd aan de andere id&#39;s in dit profiel als kenmerk voor segmentlidmaatschap. <user@adobe.com> kan bijvoorbeeld op alle apparaten en kanalen worden toegepast. Als er geen profiel wordt gevonden, wordt er een nieuw profiel gemaakt.

Customers Journey Analytics in platform weergeven:

1. Vouw **[!UICONTROL Customer]** uit in het linkerdeelvenster en selecteer vervolgens **[!UICONTROL Audiences]** . <!-- is there a folder called "Customer Journey Analytics? -->

1. Selecteer de tab **[!UICONTROL Browse]** .

1. Voer een van de volgende handelingen uit om het publiek te zoeken dat u vanuit de Customer Journey Analytics hebt gepubliceerd:

   ![ optie van het publiek in het linkerpaneel ](assets/aep-audiences.png)

   * Soort de lijst door de **[!UICONTROL Origin]** kolom om publiek te bekijken dat [!UICONTROL **Customer Journey Analytics**] als oorsprong toont.

   * Filter ![ Filter ](/help/assets/icons/Filter.svg) op **[!UICONTROL Origin]** en selecteer **[!UICONTROL Customer Journey Analytics]**.

   * Gebruik het ![ 1} onderzoeksgebied van het Onderzoek {.](/help/assets/icons/Search.svg)

Voor meer informatie over het gebruiken van Soorten publiek in Platform, zie de ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder) sectie van het publiek [ in de [ gids UI van de Bouwer van het Segment ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder) in de documentatie van het Experience Platform.


## Veelgestelde vragen {#faq}

Veelgestelde vragen over het publiceren van publiek.

+++**wat gebeurt als een gebruiker niet meer een lid van een publiek in Customer Journey Analytics is?**

In dit geval wordt een afsluitgebeurtenis vanuit de Customer Journey Analytics naar het Experience Platform verzonden.

+++

+++**wat gebeurt als u een publiek in Customer Journey Analytics schrapt?**

Wanneer een Publiek van de Customer Journey Analytics wordt geschrapt, wordt dat publiek niet meer getoond in het Experience Platform UI. Profielen die aan dat publiek zijn gekoppeld, worden echter niet verwijderd in het Experience Platform.

+++

+++**als een overeenkomstig profiel niet in Real-time Customer Data Platform bestaat, wordt een nieuw profiel gecreeerd?**

Ja, dat zal het wel.

+++

+++**verzendt de Customer Journey Analytics de publieksgegevens over als pijpleidingsgebeurtenissen of als plat dossier dat ook naar het gegevenspeer gaat?**

De Customer Journey Analytics stroomt de gegevens naar Real-time Customer Data Platform via pijpleiding, en deze gegevens worden ook verzameld in een systeemdataset in het gegevensmeer.

+++

+++**Welke identiteiten verzendt de Customer Journey Analytics over?**

Welke identiteit/namespace paren die in de [ opstelling van de Verbinding ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) werden gespecificeerd. Specifiek, de stap wanneer een gebruiker het gebied selecteert zij als Persoon identiteitskaart willen gebruiken.

+++

+++**Welke identiteitskaart wordt gekozen als primaire identiteit?**

Zie hierboven. Er wordt slechts één identiteit per Customer Journey Analytics verzonden.

+++

+++**verwerkt Real-time Customer Data Platform ook de berichten van de Customer Journey Analytics? Kan de Customer Journey Analytics identiteiten aan een grafiek van de profielidentiteit toevoegen door publiek te delen?**

Nee. Er wordt slechts één identiteit per persoon verzonden, dus er zijn geen grafiekranden die Real-time Customer Data Platform kan gebruiken.

+++

+++**welke tijd van dag doet dagelijkse, wekelijkse, en maandelijkse verfrissingen voorkomen? Welke dag van de week komt wekelijkse verfrissingen voor?**

De timing van verfrissen is gebaseerd op wanneer het originele publiek werd gepubliceerd en ankers aan dat tijdstip van dag (en dag van week of maand).

+++

+++**kunt u de dagelijkse, wekelijkse, en maandelijkse tijd van vormen verfrissen?**

Nee, gebruikers kunnen de vernieuwingstijd niet configureren.

+++


## Volgende stappen

* Om dit publiek te beheren, ga naar [ Beheer UI ](/help/components/audiences/manage.md).
