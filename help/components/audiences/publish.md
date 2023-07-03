---
title: Een publiek maken en publiceren naar het realtime profiel van de klant
description: Leer hoe u publiek kunt publiceren vanuit Customer Journey Analytics
exl-id: 0221f9f1-df65-4bd6-a31d-33d1a1ba0cfe
feature: Audiences
source-git-commit: edbad9c9d3dc0b48db5334828a18ef652d4a38aa
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# Soorten publiek maken en publiceren

Dit onderwerp bespreekt hoe te om publiek tot stand te brengen en te publiceren dat in Customer Journey Analytics aan wordt geïdentificeerd [Klantprofiel in realtime](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=en) in Adobe Experience Platform voor klantgerichtheid en personalisatie.

Lees deze [overzicht](/help/components/audiences/audiences-overview.md) kennis te nemen van het begrip Customer Journey Analytics-publiek.

## publiek maken {#create}

1. U kunt op drie manieren een publiek maken:

   | Aanmaakmethode | Details |
   | --- | --- |
   | Van de belangrijkste **[!UICONTROL Components]>[!UICONTROL Audiences]** menu | De pagina Soortbeheer wordt geopend. Klikken **[!UICONTROL Create audience]** en de [!UICONTROL Audience builder] wordt geopend. |
   | Vanuit een tabel voor vrije vorm | Klik met de rechtermuisknop op een item in een tabel voor vrije vorm en selecteer **[!UICONTROL Create an audience from selection]**. Met deze methode wordt het filter vooraf gevuld met de dimensie of het dimensie-item dat u in de tabel hebt geselecteerd. |
   | Via de interface voor het maken/bewerken van filters | Schakel het selectievakje **[!UICONTROL Create an audience from this filter]**. Met deze methode wordt het filter vooraf gevuld. |

   {style="table-layout:auto"}

1. Het publiek opbouwen.

   Configureer deze instellingen voordat u het publiek kunt publiceren.

   ![](assets/create-audience.png)

   | Instelling | Beschrijving |
   | --- | --- |
   | [!UICONTROL Name] | De naam van het publiek. |
   | [!UICONTROL Tags] | Alle tags die u aan het publiek wilt toewijzen voor organisatorische doeleinden. U kunt een bestaande tag gebruiken of een nieuwe tag invoeren. |
   | [!UICONTROL Description] | Voeg een goede beschrijving van het publiek toe om het van anderen te onderscheiden. |
   | [!UICONTROL Refresh frequency] | De frequentie waarmee u het publiek wilt vernieuwen.<ul><li>U kunt een eenmalig publiek maken (standaard) dat niet hoeft te worden vernieuwd. Dit kan bijvoorbeeld handig zijn voor specifieke, eenmalige campagnes.</li><li>U kunt andere vernieuwingsintervallen selecteren. Voor de vernieuwingsfrequentie van 4 uur geldt een limiet van 75 tot 150 publieksvernieuwingen, afhankelijk van uw Customer Journey Analytics machtiging.</li></ul> |
   | Vervaldatum | Wanneer het publiek stopt met vernieuwen. De standaardwaarde is 1 jaar vanaf de aanmaakdatum. Het verouderen van het publiek wordt op dezelfde manier behandeld als het verlopen van geplande rapporten - admin krijgt een e-mail een maand alvorens het publiek verloopt. |
   | Zoekvenster vernieuwen | Hiermee geeft u aan hoe ver u wilt teruggaan in uw gegevensvenster om dit publiek te maken. De maximale duur is 90 dagen. |
   | [!UICONTROL One-time date range] | Datumbereik wanneer u wilt dat het eenmalig publiek wordt gepubliceerd. |
   | [!UICONTROL Filter] | Filters zijn de belangrijkste invoer voor het publiek. U kunt maximaal 20 filters toevoegen. Deze filters kunnen worden aangesloten met `And` of `Or` operatoren. |
   | [!UICONTROL View sample IDs] | Een voorbeeld van id&#39;s in dit publiek. Gebruik de zoekbalk om te zoeken naar voorbeeld-id&#39;s. |

   {style="table-layout:auto"}

1. De gegevensvoorvertoning interpreteren.

   De voorvertoning voor het publiek wordt weergegeven in de rechtertrack. Hiermee kunt u een samengevatte analyse maken van het publiek dat u hebt gemaakt.

   ![](assets/data-preview.png)

   | Voorvertoning instellen | Beschrijving |
   | --- | --- |
   | [!UICONTROL Data preview] venster | Het datumbereik voor het publiek. |
   | [!UICONTROL Total people] | Een samenvattingsnummer van het totale aantal personen in dit publiek. Het kan maar liefst 20 miljoen mensen gaan. Als uw publiek meer dan 20 miljoen mensen telt, moet u de omvang van het publiek reduceren voordat u het publiek kunt publiceren. |
   | [!UICONTROL Audience size limit] | Toont hoe ver van de 20 miljoen grens dit publiek is. |
   | [!UICONTROL Estimated audience return] | Deze instelling is handig als u klanten in dit publiek die terugkeren naar uw site opnieuw wilt richten. (Met andere woorden, die opnieuw in deze dataset worden gezien.) <p>Hier kunt u het tijdkader (volgende 7 dagen, volgende 2 weken, volgende maand) selecteren voor het geschatte aantal klanten dat kan terugkeren. |
   | [!UICONTROL Estimated to return] | Dit aantal geeft u een geschat aantal terugkerende klanten over het tijdkader dat u van de drop-down lijst selecteerde. We kijken naar de historische waarde van de kroon voor dit publiek om dit getal te voorspellen. |
   | [!UICONTROL Preview metrics] | Met deze instelling kunt u naar specifieke maateenheden kijken om te zien of dit publiek een onevenredig grote bijdrage levert aan deze metrische waarde, zoals &#39;[!UICONTROL Revenue]&#39; of &#39;[!UICONTROL Average time on site]&quot;. Het geeft u het totale aantal metrisch, evenals het percentage van het totaal het vertegenwoordigt. U kunt elke metrische waarde selecteren die beschikbaar is in de gegevensweergave. |
   | [!UICONTROL Namespaces included] | De specifieke naamruimten die zijn gekoppeld aan de personen in uw publiek. Voorbeelden zijn ECID, CRM-id, e-mailadressen enzovoort. |
   | [!UICONTROL Sandbox] | De [Experience Platform sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=en) waarin dit publiek woont. Wanneer u dit publiek naar het Platform publiceert, kunt u er alleen binnen de grenzen van deze sandbox mee werken. |

   {style="table-layout:auto"}

1. Controleer uw publieksconfiguratie tweemaal en klik **[!UICONTROL Publish]**.

   Als alles goed ging, ontvangt u een bevestigingsbericht dat het publiek werd gepubliceerd. Het duurt slechts een minuut of twee voordat dit publiek in Experience Platform verschijnt. (Zelfs voor het publiek met miljoenen leden moet het minder dan 5 minuten duren.)

1. Klikken **[!UICONTROL View audience in AEP]** in hetzelfde bericht en u gaat naar de [Gebruikersinterface segment](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=en) in Adobe Experience Platform. Zie hieronder voor meer informatie.

## Wat gebeurt er nadat een publiek is gemaakt? {#after-audience-created}

Nadat u een publiek hebt gecreeerd, leidt Adobe tot een Experience Platform het stromen segment voor elk nieuw publiek van Customer Journey Analytics. Er wordt alleen een Adobe Experience Platform-streaming segment gemaakt als uw organisatie is ingesteld op segmentatie bij streaming.

* Het Adobe Experience Platform-segment heeft dezelfde naam/beschrijving als het Customer Journey Analytics-publiek, maar aan de naam wordt de Customer Journey Analytics-gebruikers-id toegevoegd om ervoor te zorgen dat deze uniek is.
* Als de naam/beschrijving van het Customer Journey Analytics-publiek verandert, geeft de naam/beschrijving van het Adobe Experience Platform-segment die wijziging ook weer.
* Als een gebruiker een Customer Journey Analytics-publiek verwijdert, wordt het Adobe Experience Platform-segment NIET verwijderd. De reden is dat het publiek van de Customer Journey Analytics later kan worden verwijderd.

## Latentieoverwegingen {#latency}

Op verschillende momenten vóór, tijdens en na het publiceren van de doelgroep kunnen er latentie optreden. Hier volgt een overzicht van mogelijke vertragingen.

![Latentie van Adobe Experience Platform naar Customer Journey Analytics](assets/latency-diagram.png)

| Aantal | Latentiepunt | Latentieduur |
| --- | --- | --- |
| Niet weergegeven | Adobe Analytics to Analytics Source Connector (A4T) | Tot 30 minuten |
| 1 | Gegevensopname in Data Lake (van Analytics Source Connector of andere bronnen) | Tot 90 minuten |
| 2 | Gegevensopname van Experience Platform Data Lake naar Customer Journey Analytics | Tot 90 minuten |
| 3 | Publiceren van het publiek naar het profiel van de Klant in real time, met inbegrip van de automatische verwezenlijking van het het stromen segment, en het toestaan van het segment klaar om de gegevens te ontvangen. | Ongeveer 60 minuten |
| 4 | Frequentie vernieuwen voor publiek | <ul><li>Eenmalige vernieuwing (vertraging van minder dan 5 minuten)</li><li>Vernieuwen elke 4 uur, dagelijks, wekelijks, maandelijks (latentie gaat hand in hand met de vernieuwingsfrequentie) |
| 5 | Doel maken in Adobe Experience Platform: Het nieuwe segment activeren | 1-2 uur |

{style="table-layout:auto"}

## Customer Journey Analytics-publiek gebruiken in Experience Platform {#audiences-aep}

Customer Journey Analytics neemt alle naamruimte- en id-combinaties van uw gepubliceerde publiek en streamt deze naar RTCP (Real-Time Customer Profile). Customer Journey Analytics stuurt het publiek naar het Experience Platform met de primaire identiteitsset, afhankelijk van wat als de [!UICONTROL Person ID] wanneer de verbinding werd gevormd.

RTCP onderzoekt dan elke namespace/ID combinatie en zoekt een profiel dat het deel van kan uitmaken. Een profiel is in feite een cluster van gekoppelde naamruimten, id&#39;s en apparaten. Als er een profiel wordt gevonden, worden de naamruimte en de id toegevoegd aan de andere id&#39;s in dit profiel als kenmerk voor segmentlidmaatschap. Nu kan &#39;user@adobe.com&#39; bijvoorbeeld worden gebruikt op alle apparaten en kanalen. Als er geen profiel wordt gevonden, wordt er een nieuw profiel gemaakt.

U kunt Customer Journey Analytics-publiek in Platform bekijken door naar **[!UICONTROL Segments]** > **[!UICONTROL Create segments]** > **[!UICONTROL Audiences]** tab > **[!UICONTROL CJA Audiences]**.

U kunt Customer Journey Analytics-publiek naar de segmentdefinitie voor Adobe Experience Platform-segmenten slepen.

![](assets/audiences-aep.png)

## Veelgestelde vragen {#faq}

Veelgestelde vragen over het publiceren van publiek.

+++**Wat gebeurt er als een gebruiker geen lid meer is van een publiek in Customer Journey Analytics?**

In dit geval wordt een afsluitgebeurtenis vanuit Customer Journey Analytics naar het Experience Platform verzonden.

+++

+++**Wat gebeurt er als u een publiek in Customer Journey Analytics verwijdert?**

Wanneer een publiek van de Customer Journey Analytics wordt geschrapt, zal dat publiek niet meer in de interface van het Experience Platform verschijnen. Er zijn echter geen profielen die aan dat publiek zijn gekoppeld, die in het Platform worden verwijderd.

+++

+++**Als er geen corresponderend profiel bestaat in RTCDP, wordt er een nieuw profiel gemaakt?**

Ja, dat zal het wel.

+++

+++**Verstuurt Customer Journey Analytics de publieksgegevens over als pijpleidinggebeurtenissen of als een plat bestand dat ook naar data Lake gaat?**

Customer Journey Analytics stromen de gegevens in RTCP via pijpleiding, en deze gegevens worden ook verzameld in een systeemdataset in het gegevensmeer.

+++

+++**Welke identiteiten verzendt Customer Journey Analytics?**

Welke identiteit/naamruimteparen zijn opgegeven in het dialoogvenster [Verbinding instellen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en#create-connection). Specifiek, de stap wanneer een gebruiker het gebied selecteert zij als hun &quot;identiteitskaart van de Persoon&quot;willen gebruiken.

+++

+++**Welke ID wordt gekozen als primaire identiteit?**

Zie hierboven. We sturen slechts één identiteit per Customer Journey Analytics &quot;persoon&quot;.

+++

+++**Verwerkt RTCP ook de Customer Journey Analytics berichten? Kan Customer Journey Analytics identiteiten aan een grafiek van de profielidentiteit toevoegen door publiek te delen?**

Nee. We sturen slechts één identiteit per &quot;persoon&quot;, dus er zouden geen grafiekranden zijn voor RTCP om te verbruiken.

+++

+++**Op welk tijdstip van de dag worden dagelijks, wekelijks en maandelijks vernieuwd? Op welke dag van de week vinden wekelijkse vernieuwingen plaats?**

De timing van verfrissen is gebaseerd op wanneer het originele publiek werd gepubliceerd en ankers aan dat tijdstip van dag (en dag van week of maand).

+++

+++**Kunnen de dagelijkse, wekelijkse, en maandelijkse tijd van verfrissen door gebruikers worden gevormd?**

Nr, kunnen zij niet door gebruikers worden gevormd.

+++


## Volgende stappen

* Ga naar de [Gebruikersinterface voor beheer](/help/components/audiences/manage.md).
