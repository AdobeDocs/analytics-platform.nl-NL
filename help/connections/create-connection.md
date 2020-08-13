---
title: Een verbinding maken
description: Beschrijft hoe te om een verbinding aan een dataset van het Platform in de Analyse van de Reis van de Klant tot stand te brengen.
translation-type: tm+mt
source-git-commit: 92702a78f4b3d3413f91d896749db10102412fba
workflow-type: tm+mt
source-wordcount: '1578'
ht-degree: 1%

---


# Een verbinding maken

Een verbinding laat u datasets van integreren [!DNL Adobe Experience Platform] in [!UICONTROL Workspace]. Om verslag uit te brengen over [!DNL Experience Platform] datasets, moet u eerst een verbinding tussen datasets in vestigen [!DNL Experience Platform] en [!UICONTROL Workspace].

Klik [hier](https://docs.adobe.com/content/help/en/platform-learn/tutorials/cja/connecting-customer-journey-analytics-to-data-sources-in-platform.html) voor een videooverzicht.

>[!IMPORTANT]
>
>U kunt meerdere [!DNL Experience Platform] datasets in één enkele verbinding.

## Selecteer sandbox en datasets

1. Ga naar [https://analytics.adobe.com](https://analytics.adobe.com).

1. Klik op de **[!UICONTROL Connections]** tabblad

1. Klik **[!UICONTROL Create new connection]** rechtsboven.

   ![Verbinding maken](assets/create-connection0.png)

1. Kies een zandbak in het Platform van de Ervaring dat de dataset/s bevat waaraan u een verbinding wilt tot stand brengen.

   Het Platform van de Ervaring van Adobe verstrekt [sandboxes](https://docs.adobe.com/content/help/en/experience-platform/sandbox/home.html) die één platforminstantie in afzonderlijke virtuele omgevingen verdelen om toepassingen voor digitale ervaring te helpen ontwikkelen en ontwikkelen. U kunt aan sandboxes als &quot;gegevenssilo&#39;s&quot;denken die gegevensreeksen bevatten. De sandboxes worden gebruikt om toegang tot gegevensreeksen te controleren.  Zodra u de zandbak hebt geselecteerd, toont de linkerspoorstaaf alle datasets in die zandbak waaruit u kunt trekken.

   >[!IMPORTANT]
   >
   >U kunt tot gegevens over sandboxes toegang hebben, d.w.z. u kunt datasets binnen één zandbak slechts combineren.

1. Selecteer één of meerdere datasets waarin u wilt trekken [!UICONTROL Customer Journey Analytics] en klik op **[!UICONTROL Add]**.

   (Als u een hoop datasets hebt waaruit u kunt kiezen, kunt u zoeken naar de juiste datasets met behulp van de **[!UICONTROL Search datasets]** de onderzoeksbar boven de lijst van datasets.)

## Gegevensset configureren

Aan de rechterkant, kunt u de dataset nu vormen u hebt toegevoegd.

![Gegevensset configureren](assets/create-connection.png)

1. **[!UICONTROL Dataset type]**: Voor elke dataset die u aan deze verbinding toevoegde, [!UICONTROL Customer Journey Analytics] plaatst automatisch het datasettype dat op de gegevens wordt gebaseerd die binnen komen.

   Er zijn 3 verschillende datasettypes: [!UICONTROL Event] gegevens, [!UICONTROL Profile] gegevens, en [!UICONTROL Lookup] gegevens.

   | Dataset Type | Beschrijving | Tijdstempel | Schema | Persoon-id |
   |---|---|---|---|---|
   | [!UICONTROL Event] | Gegevens die gebeurtenissen in de tijd weergeven (bv. webbezoeken, interacties, transacties, POS-gegevens, enquêtegegevens, en impressiegegevens, enz.). Bijvoorbeeld, zou dit typische klikstroomgegevens, met een klantenidentiteitskaart of een koekjesidentiteitskaart, en timestamp kunnen zijn. Met de gegevens van de Gebeurtenis, hebt u flexibiliteit wat betreft welke identiteitskaart als identiteitskaart van de Persoon wordt gebruikt. | Wordt automatisch geplaatst aan het standaardtimestamp gebied van op gebeurtenis-gebaseerde schema&#39;s in [UICONTROL-ervaringsplatform]. | Om het even welk ingebouwd of douaneschema dat op een klasse XDM met het gedrag van de Reeks van de &quot;Tijd&quot;gebaseerd is. De voorbeelden omvatten &quot;Gebeurtenis van de Ervaring XDM&quot;of &quot;Gebeurtenis van het Besluit XDM.&quot; | U kunt kiezen welke Persoon-id u wilt opnemen. Elk datasetschema dat in het Platform van de Ervaring wordt bepaald kan zijn eigen reeks van één of meerdere identiteiten hebben die en met een Identiteit worden bepaald Namespace worden geassocieerd. Om het even welk van deze kunnen als identiteitskaart van de Persoon worden gebruikt. De voorbeelden omvatten Koekje identiteitskaart, Stitched identiteitskaart, Gebruiker - identiteitskaart, het Volgen Code, enz. |
   | [!UICONTROL Lookup] | analoog aan een classificatiebestand. Dit gegeven wordt gebruikt om op waarden of sleutels te kijken die in uw gegevens van de Gebeurtenis of van het Profiel worden gevonden. Bijvoorbeeld, zou u raadplegingsgegevens kunnen uploaden die numerieke IDs in uw gebeurtenisgegevens aan productnamen in kaart brengen. | N.v.t. | Om het even welk ingebouwd of douaneschema dat op een klasse XDM met het &quot;Verslag&quot;gedrag, behalve de klasse &quot;van het Individuele Profiel XDM&quot;gebaseerd is. | N.v.t. |
   | [!UICONTROL Profile] | analoog aan [!UICONTROL Customer Attributes] - voor niet-veranderende en niet-temporele kenmerken. Gegevens die op uw bezoekers, gebruikers, of klanten in worden toegepast [!UICONTROL Event] gegevens. Bijvoorbeeld, staat u toe om de gegevens van CRM over uw klanten te uploaden. | N.v.t. | Om het even welk ingebouwd of douaneschema dat op de klasse &quot;van het Individuele Profiel XDM&quot;gebaseerd is. | U kunt kiezen welke Persoon-id u wilt opnemen. Elke dataset die in [!DNL Experience Platform] heeft zijn eigen reeks van één of meerdere bepaalde Identiteitskaart van de Persoon, zoals Koekje - identiteitskaart, Verplaatste identiteitskaart, Gebruiker - identiteitskaart, het Volgen Code, enz.<br>![Persoon-id ](assets/person-id.png)**Opmerking**: Als u een verbinding creeert die datasets met verschillende IDs omvat, zal de rapportering op dat wijzen. Om datasets echt samen te voegen, moet u de zelfde identiteitskaart van de Persoon gebruiken. |

1. **[!UICONTROL Dataset ID]**: Deze ID wordt automatisch gegenereerd.

1. **[!UICONTROL Time stamp]**: voeg hier inhoud toe

1. **[!UICONTROL Schema]**: Dit is het [schema](https://docs.adobe.com/content/help/en/experience-platform/xdm/schema/composition.html) gebaseerd waarop de dataset in het Platform van de Ervaring van Adobe werd gecreeerd.

1. **[!UICONTROL Person ID]**: Selecteer een persoonsidentiteitskaart van de dropdown lijst van beschikbare identiteiten. Deze identiteiten werden bepaald in het datasetschema in het Platform van de Ervaring. Zie hieronder voor informatie over hoe te om de Kaart van de Identiteit als identiteitskaart van de Persoon te gebruiken

   >[!IMPORTANT]
   >
   >Als er geen persoon IDs te kiezen van zijn, betekent dat één of meerdere persoon IDs niet in het schema is bepaald. Weergave [deze video](https://youtu.be/G_ttmGl_LRU) over het definiëren van een identiteit in het ervaringsplatform.

1. Klik **[!UICONTROL Next]** om naar de [!UICONTROL Enable Connection] dialoog.

### Identiteitskaart van het gebruik als identiteitskaart van de Persoon

De Analyse van de Reis van de klant steunt nu de capaciteit om de Kaart van de Identiteit voor zijn identiteitskaart van de Persoon te gebruiken. De Kaart van de identiteit is een structuur van kaartgegevens die iemand toestaat om zeer belangrijk -> waardeparen te uploaden. De sleutels zijn identiteitsnaamruimten en de waarde is een structuur die de identiteitswaarde bevat. De kaart van de Identiteit bestaat op elke rij/gebeurtenis die wordt geupload en voor elke rij dienovereenkomstig bevolkt.

De Kaart van de Identiteit is beschikbaar voor om het even welke dataset die een schema gebruikt dat op wordt gebaseerd [ExperienceEvent XDM](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html) klasse. Wanneer u zulk een dataset selecteert die in een Verbinding moet worden omvat CJA, hebt u de optie om of een gebied als primaire identiteitskaart of de Kaart van de Identiteit te selecteren:

![](assets/idmap1.png)

Als u de Kaart van de Identiteit selecteert, krijgt u twee extra configuratieopties:

| Optie | Beschrijving |
|---|---|
| [!UICONTROL Use Primary ID Namespace] | Dit instrueert CJA, per rij, om de identiteit in de Kaart van de Identiteit te vinden die met een attribuut primary=true duidelijk is en dat als identiteitskaart van de Persoon voor die rij gebruikt. Dit betekent dat dit de primaire sleutel is die in het Platform van de Ervaring voor het verdelen zal worden gebruikt. Het is ook de eerste kandidaat voor gebruik als bezoekersidentiteitskaart van CJA (afhankelijk van hoe de dataset in een Verbinding CJA wordt gevormd). |
| [!UICONTROL Namespace] | (Deze optie is alleen beschikbaar als u de primaire id Namespace niet gebruikt.) Identiteit namespaces is een component van [Adobe Experience Platform Identity Service](https://docs.adobe.com/content/help/en/experience-platform/identity/namespaces.html) die dienen als indicatoren van de context waarop een identiteit betrekking heeft. Als u een namespace specificeert, zal CJA de Kaart van de Identiteit van elke rij voor deze namespacesleutel zoeken en de identiteit onder dat namespace als persoonsidentiteitskaart voor die rij gebruiken. Merk op dat aangezien CJA geen volledig datasetaftasten van alle rijen kan doen om te bepalen welke namespaces eigenlijk aanwezig zijn, alle mogelijke namespaces in dropdown vermeld zijn. U moet weten welke namespaces in de gegevens worden gespecificeerd; dit kan niet automatisch worden gedetecteerd. |

### Draagtassen voor de rand van de identiteitskaart

Deze lijst toont de twee configuratieopties wanneer de randgevallen aanwezig zijn en hoe zij worden behandeld:

| Optie | Geen IDs is aanwezig in de Kaart van de Identiteit | Geen id&#39;s zijn gemarkeerd als primair | Veelvoudige IDs zijn duidelijk als primair | Enige identiteitskaart wordt duidelijk als primair | Ongeldige namespace met identiteitskaart duidelijk als primair |
|---|---|---|---|---|---|
| **&quot;Primaire ID Namespace gebruiken&quot; ingeschakeld** | De rij wordt gelaten vallen door CJA. | De rij wordt gelaten vallen door CJA, aangezien geen primaire identiteitskaart wordt gespecificeerd. | Alle IDs duidelijk als primair, onder alle namespaces, worden gehaald in een lijst. Vervolgens worden ze alfabetisch gesorteerd; met dit nieuwe sorteren, wordt eerste namespace met zijn eerste identiteitskaart gebruikt als identiteitskaart van de Persoon | Één enkele identiteitskaart duidelijk als primair wordt gebruikt als identiteitskaart van de Persoon | Alhoewel namespace (niet aanwezig in AEP) ongeldig kan zijn, zal CJA primaire identiteitskaart onder dat namespace als identiteitskaart van de Persoon gebruiken. |
| **Specifieke identiteitskaartnaamruimte geselecteerd** | De rij wordt gelaten vallen door CJA. | Al IDs onder geselecteerde namespace wordt gehaald in een lijst en eerste wordt gebruikt als identiteitskaart van de Persoon | Al IDs onder geselecteerde namespace wordt gehaald in een lijst en eerste wordt gebruikt als identiteitskaart van de Persoon | Al IDs onder geselecteerde namespace wordt gehaald in een lijst en eerste wordt gebruikt als identiteitskaart van de Persoon | Al IDs onder geselecteerde namespace wordt gehaald in een lijst en eerste wordt gebruikt als identiteitskaart van de Persoon (Slechts kan een geldige namespace in de aanmaaktijd van de Verbinding worden geselecteerd, zodat is het niet mogelijk voor een ongeldige namespace/identiteitskaart die als identiteitskaart van de Persoon moet worden gebruikt) |

## Verbinding inschakelen

![Verbinding inschakelen](assets/create-connection2.png)

1. Om een verbinding toe te laten, bepaal deze montages:

   | Optie | Beschrijving |
   |---|---|
   | [!UICONTROL Name Connection] | Geef de verbinding een beschrijvende naam. De verbinding kan niet zonder een naam worden bewaard. |
   | [!UICONTROL Description] | Voeg meer detail toe om deze verbinding van anderen te onderscheiden. |
   | [!UICONTROL Datasets] | De datasets die in deze verbinding inbegrepen zijn. |
   | [!UICONTROL Automatically import all new datasets in this connection, beginning today.] | Selecteer deze optie als u een aan de gang zijnde verbinding wilt vestigen, zodat om het even welke nieuwe gegevensbatches die aan de datasets in deze verbinding automatisch worden toegevoegd in stromen [!UICONTROL Workspace]. |
   | [!UICONTROL Import all existing data] | Wanneer u deze optie selecteert en de verbinding opslaat, worden alle bestaande (historische) gegevens van [!DNL Experience Platform] voor alle datasets die in deze verbinding zijn zal worden ingevoerd. In de toekomst zullen ook alle bestaande historische gegevens voor alle nieuwe gegevensbestanden die aan deze opgeslagen verbinding worden toegevoegd, automatisch worden geïmporteerd. <br>**Merk op dat, zodra deze verbinding wordt bewaard, dit het plaatsen niet kan worden veranderd.** |

   **Vergeet niet dat:**

   * Als de cumulatieve grootte van de historische gegevens voor alle datasets in de verbinding 1.5 Billion rijen overschrijdt, zal een foutenmelding erop wijzen dat u niet deze hoeveelheid historische gegevens kunt invoeren. Nochtans, als u een dataset met 1 Billion rijen van historische gegevens moest toevoegen, en die gegevens invoert, en een week later, een andere dataset van de zelfde grootte toevoegt en zijn historische gegevens invoert, zou dit werken.
   * Wij geven voorrang aan nieuwe gegevens die aan een dataset in de verbinding worden toegevoegd, zodat heeft dit gegeven de laagste latentie.
   * Om het even welk backfill (historische) gegeven wordt ingevoerd tegen een langzamer tarief.

1. Klik op **[!UICONTROL Save]**.

De volgende stap in de workflow is: [een gegevensweergave maken](/help/data-views/create-dataview.md).
