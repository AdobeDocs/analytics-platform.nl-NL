---
title: Een publiek maken en publiceren naar het realtime profiel van de klant
description: Leer hoe u publiek kunt publiceren vanuit Customer Journey Analytics
exl-id: 0221f9f1-df65-4bd6-a31d-33d1a1ba0cfe
feature: Audiences
role: User
source-git-commit: d903745e105edb11ef6f43b6137e1e03d43e5e07
workflow-type: tm+mt
source-wordcount: '1638'
ht-degree: 0%

---

# Soorten publiek maken en publiceren

Dit onderwerp bespreekt hoe te om publiek tot stand te brengen en te publiceren dat in Customer Journey Analytics aan [ in real time het Profiel van de Klant ](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=nl) in Adobe Experience Platform voor klant wordt geïdentificeerd die en verpersoonlijking richt.

Lees dit [ overzicht ](/help/components/audiences/audiences-overview.md) om met het concept publiek van de Customer Journey Analytics vertrouwd te maken.

## Een publiek maken en publiceren {#create}

1. Voer een van de volgende handelingen uit om een publiek te maken en te publiceren:

   | Aanmaakmethode | Details |
   | --- | --- |
   | Vanuit het hoofdmenu **[!UICONTROL Components]>[!UICONTROL Audiences]** | De pagina Soortbeheer wordt geopend. Klik op **[!UICONTROL Create audience]** en [!UICONTROL Audience builder] wordt geopend. |
   | Vanuit een tabel voor vrije vorm | Klik met de rechtermuisknop op een item in een tabel met vrije vorm en selecteer **[!UICONTROL Create audience from selection]** . Met deze methode wordt het filter vooraf gevuld met de dimensie of het dimensie-item dat u in de tabel hebt geselecteerd. |
   | Via de interface voor het maken/bewerken van filters | Schakel het vakje met de tekst **[!UICONTROL Create an audience from this filter]** in. Met deze methode wordt het filter vooraf gevuld. |

   {style="table-layout:auto"}

   <!-- add beneath the Freeform table row above: | From within a Journey canvas visualization | Right-click a node in a Journey canvas visualization and select **[!UICONTROL Create audience]**. Using this method pre-populates the filter with the dimension or dimension item you selected in the table. | -->

1. Het publiek opbouwen.

   Configureer deze instellingen voordat u het publiek kunt publiceren.

   ![ Schermafbeelding van creeer een publiek die montages boeien in de volgende sectie worden beschreven.](assets/create-audience.png)

   | Instelling | Beschrijving |
   | --- | --- |
   | [!UICONTROL Name] | De naam van het publiek. |
   | [!UICONTROL Tags] | Alle tags die u aan het publiek wilt toewijzen voor organisatorische doeleinden. U kunt een bestaande tag gebruiken of een nieuwe tag invoeren. |
   | [!UICONTROL Description] | Voeg een goede beschrijving van het publiek toe, om het van anderen te onderscheiden. |
   | [!UICONTROL Refresh frequency] | De frequentie waarmee u het publiek wilt vernieuwen.<ul><li>U kunt een eenmalig publiek maken (standaard) dat niet hoeft te worden vernieuwd. Dit kan bijvoorbeeld handig zijn voor specifieke, eenmalige campagnes.</li><li>U kunt andere vernieuwingsintervallen selecteren. Voor de vernieuwingsfrequentie van 4 uur geldt een limiet van 75 tot 150 publieksvernieuwingen, afhankelijk van de machtiging van uw Customer Journey Analytics.</li></ul> |
   | Vervaldatum | Wanneer het publiek stopt met vernieuwen. De standaardwaarde is 1 jaar vanaf de aanmaakdatum. Het verouderen van het publiek wordt op dezelfde manier behandeld als het verlopen van geplande rapporten - admin krijgt een e-mail een maand alvorens het publiek verloopt. |
   | Zoekvenster vernieuwen | Hiermee geeft u aan hoe ver u wilt teruggaan in uw gegevensvenster om dit publiek te maken. De maximale duur is 90 dagen. |
   | [!UICONTROL One-time date range] | Datumbereik wanneer u wilt dat het eenmalig publiek wordt gepubliceerd. |
   | [!UICONTROL Filter] | Filters zijn de belangrijkste invoer voor het publiek. U kunt maximaal 20 filters toevoegen. Deze filters kunnen worden gekoppeld met `And` - of `Or` -operatoren. |
   | [!UICONTROL View sample IDs] | Een voorbeeld van id&#39;s in dit publiek. Zoek met de zoekbalk naar voorbeeld-id&#39;s. |

   {style="table-layout:auto"}

1. De gegevensvoorvertoning interpreteren.

   De voorvertoning voor het publiek wordt weergegeven in de rechtertrack. Hiermee kunt u een samengevatte analyse maken van het publiek dat u hebt gemaakt.

   ![ Schermafbeelding van de gegevensvoorproef die een samengevatte analyse van het publiek tonen.](assets/data-preview.png)

   | Voorvertoning instellen | Beschrijving |
   | --- | --- |
   | [!UICONTROL Data preview] window | Het datumbereik voor het publiek. |
   | [!UICONTROL Total people] | Een samenvattingsnummer van het totale aantal personen in dit publiek. Het kan maar liefst 20 miljoen mensen gaan. Als uw publiek meer dan 20 miljoen mensen telt, moet u de omvang van het publiek reduceren voordat u het publiek kunt publiceren. |
   | [!UICONTROL Audience size limit] | Toont hoe ver van de 20 miljoen grens dit publiek is. |
   | [!UICONTROL Estimated audience return] | Deze instelling is handig voor het opnieuw toewijzen van klanten in dit publiek die terugkeren naar uw site, mobiele app of ander kanaal (met andere woorden, die weer in deze dataset worden weergegeven). <p>Hier kunt u het tijdkader (volgende 7 dagen, volgende 2 weken, volgende maand) selecteren voor het geschatte aantal klanten dat kan terugkeren. |
   | [!UICONTROL Estimated to return] | Dit aantal geeft u een geschat aantal terugkerende klanten over het tijdkader dat u van de drop-down lijst selecteerde. We kijken naar de historische waarde van de kroon voor dit publiek om dit getal te voorspellen. |
   | [!UICONTROL Preview metrics] | Dit het plaatsen staat u toe om specifieke metriek te bekijken om te zien of dit publiek een disproportioneel bedrag aan dit metrisch bijdraagt, zoals &quot;[!UICONTROL Revenue]&quot;of &quot;[!UICONTROL Average time on site]&quot;. Het geeft u het totale aantal metrisch, evenals het percentage van het totaal het vertegenwoordigt. U kunt elke metrische waarde selecteren die beschikbaar is in de gegevensweergave. |
   | [!UICONTROL Namespaces included] | De specifieke naamruimten die zijn gekoppeld aan de personen in uw publiek. Voorbeelden zijn ECID, CRM-id, e-mailadressen enzovoort. |
   | [!UICONTROL Sandbox] | De [ zandbak van het Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=nl) waarin dit publiek verblijft. Wanneer u dit publiek publiceert naar Platform, kunt u er alleen mee werken binnen de grenzen van deze sandbox. |

   {style="table-layout:auto"}

1. Controleer de publieksconfiguratie en klik op **[!UICONTROL Publish]** .

   Als alles goed ging, ontvangt u een bevestigingsbericht dat het publiek werd gepubliceerd. Het duurt slechts een minuut of twee voordat dit publiek in Experience Platform verschijnt. (Zelfs voor het publiek met miljoenen leden moet het minder dan 5 minuten duren.)

1. Klik **[!UICONTROL View audience in AEP]** binnen het zelfde bericht en u zult aan het [ Segment UI ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html) in Adobe Experience Platform worden genomen. Zie hieronder voor meer informatie.

## Wat gebeurt er nadat een publiek is gemaakt en gepubliceerd? {#after-audience-created}

Nadat u een publiek in de Customer Journey Analytics creeert en publiceert, is het publiek beschikbaar in Experience Platform. Er wordt alleen een Adobe Experience Platform-streaming segment gemaakt als uw organisatie is ingesteld op segmentatie bij streaming.

* Het publiek in Platform deelt de zelfde naam/de beschrijving zoals het publiek van de Customer Journey Analytics, maar de naam zal met de Customer Journey Analytics publiek identiteitskaart worden toegevoegd om ervoor te zorgen dat het uniek is.
* Wijzigingen die worden aangebracht in de naam of beschrijving van het publiek in de Customer Journey Analytics, worden weerspiegeld in Platform.
* Als een publiek in Customer Journey Analytics wordt geschrapt, blijft het publiek beschikbaar in Platform.

## Latentieoverwegingen {#latency}

Op verschillende momenten vóór, tijdens en na het publiceren van de doelgroep kunnen er latentie optreden. Hier volgt een overzicht van mogelijke vertragingen.

![ Latenties in publiek het publiceren zoals die in deze sectie worden beschreven.](assets/latency-diagram.svg)

| Aantal | Latentiepunt | Latentieduur |
| --- | --- | --- |
| Niet weergegeven | Adobe Analytics naar Analytics-bronconnector (A4T) | Tot 30 minuten |
| 1 | Gegevensopname in het gegevensmeer (van de bronconnector van Analytics of andere bronnen) | Tot 90 minuten |
| 2 | Gegevensopname van Experience Platform Data Lake naar Customer Journey Analytics | Tot 90 minuten |
| 3 | Publiceren van het publiek naar het profiel van de Klant in real time, met inbegrip van de automatische verwezenlijking van het het stromen segment, en het toestaan van het segment klaar om de gegevens te ontvangen. | Enkele seconden |
| 4 | Frequentie vernieuwen voor publiek | <ul><li>Eenmalige vernieuwing (vertraging van minder dan 5 minuten)</li><li>Vernieuwen elke 4 uur, dagelijks, wekelijks, maandelijks (latentie gaat hand in hand met de vernieuwingsfrequentie) |
| 5 | Doel maken in Adobe Experience Platform: het nieuwe segment activeren | 1-2 uur |

{style="table-layout:auto"}

## Customer Journey Analytics publiek in Experience Platform gebruiken {#audiences-aep}

Customer Journey Analytics neemt alle namespace en identiteitskaart combinaties van uw gepubliceerd publiek en stroomt hen in het Profiel van de Klant in real time (RTCP). Customer Journey Analytics verzendt het publiek naar Experience Platform met de primaire identiteitsreeks, volgens wat als [!UICONTROL Person ID] werd geselecteerd toen de verbinding werd gevormd.

RTCP onderzoekt dan elke naamruimte/ID-combinatie en zoekt naar een profiel waarvan het deel kan uitmaken. Een profiel is in feite een cluster van gekoppelde naamruimten, id&#39;s en apparaten. Als er een profiel wordt gevonden, worden de naamruimte en de id toegevoegd aan de andere id&#39;s in dit profiel als kenmerk voor segmentlidmaatschap. <user@adobe.com> kan bijvoorbeeld op alle apparaten en kanalen worden toegepast. Als er geen profiel wordt gevonden, wordt er een nieuw profiel gemaakt.

Customers Journey Analytics in platform weergeven:

>[!AVAILABILITY]
>
>De functionaliteit die in de volgende stappen wordt beschreven, bevindt zich in de Beperkte testfase van de release en is mogelijk nog niet beschikbaar in uw omgeving. Als deze stappen niet aanpassen wat u in uw milieu ziet, gebruik in plaats daarvan de volgende stappen: Ga naar [!UICONTROL **Segmenten**] > [!UICONTROL **creeer segmenten**] > [!UICONTROL **Publiek**] lusje > [!UICONTROL **CJA Soorten**].
>
>Deze notitie wordt verwijderd wanneer de functionaliteit algemeen beschikbaar is. Voor informatie over het de versieproces van de Customer Journey Analytics, zie {de eigenschapversies van de Customer Journey Analytics 0} ](/help/release-notes/releases.md).[

1. Breid [!UICONTROL **Klant**] in het linkerspoor uit, dan selecteren [!UICONTROL **Soorten publiek**]. <!-- is there a folder called "Customer Journey Analytics? -->

1. Selecteer [!UICONTROL **doorbladeren**] tabel.

   ![ optie van het publiek in het linkerpaneel ](assets/audiences-aep.png)

1. Voer een van de volgende handelingen uit om het publiek te zoeken dat u vanuit de Customer Journey Analytics hebt gepubliceerd:

   * Soort de lijst door de [!UICONTROL **kolom van de Oorsprong**] om publiek te bekijken dat [!UICONTROL **Customer Journey Analytics**] als oorsprong toont.

   * Selecteer het filterpictogram.

   * Gebruik het zoekveld.

Voor meer informatie over het gebruiken van Soorten publiek in Platform, zie de ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#audiences) sectie van het publiek [ in [ de gids UI van de Bouwer van het Segment ](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html) in de documentatie van het Experience Platform.


## Veelgestelde vragen {#faq}

Veelgestelde vragen over het publiceren van publiek.

+++**wat gebeurt als een gebruiker niet meer een lid van een publiek in Customer Journey Analytics is?**

In dit geval wordt een afsluitgebeurtenis vanuit de Customer Journey Analytics naar het Experience Platform verzonden.

+++

+++**wat gebeurt als u een publiek in Customer Journey Analytics schrapt?**

Wanneer een Publiek van de Customer Journey Analytics wordt geschrapt, zal dat publiek niet meer in Experience Platform UI verschijnen. Nochtans, worden geen profielen verbonden aan dat publiek eigenlijk geschrapt in Platform.

+++

+++**als een overeenkomstig profiel niet in RTCDP bestaat, zal een nieuw profiel worden gecreeerd?**

Ja, dat zal het wel.

+++

+++**verzendt de Customer Journey Analytics de publieksgegevens over als pijpleidingsgebeurtenissen of als plat dossier dat ook naar gegevens meer gaat?**

De Customer Journey Analytics stroomt de gegevens in RTCP via pijpleiding, en deze gegevens worden ook verzameld in een systeemdataset in het gegevensmeer.

+++

+++**Welke identiteiten verzendt de Customer Journey Analytics over?**

Welke identiteit/namespace paren die in de [ opstelling van de Verbinding ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html#create-connection) werden gespecificeerd. Specifiek, de stap wanneer een gebruiker het gebied selecteert zij als hun &quot;identiteitskaart van de Persoon&quot;willen gebruiken.

+++

+++**Welke identiteitskaart wordt gekozen als primaire identiteit?**

Zie hierboven. We sturen slechts één identiteit per Customer Journey Analytics &quot;persoon&quot;.

+++

+++**verwerkt RTCP ook de berichten van de Customer Journey Analytics? Kan de Customer Journey Analytics identiteiten aan een grafiek van de profielidentiteit toevoegen door publiek te delen?**

Nee. We sturen slechts één identiteit per &quot;persoon&quot;, dus er zouden geen grafiekranden zijn voor RTCP om te verbruiken.

+++

+++**welke tijd van dag doet dagelijkse, wekelijkse, en maandelijkse verfrissingen voorkomen? Welke dag van de week komt wekelijkse verfrissingen voor?**

De timing van verfrissen is gebaseerd op wanneer het originele publiek werd gepubliceerd en ankers aan dat tijdstip van dag (en dag van week of maand).

+++

+++**kan de dag, de week, en de maandelijkse tijd van zich door gebruikers worden gevormd?**

Nr, kunnen zij niet door gebruikers worden gevormd.

+++


## Volgende stappen

* Om dit publiek te beheren, ga naar [ Beheer UI ](/help/components/audiences/manage.md).
