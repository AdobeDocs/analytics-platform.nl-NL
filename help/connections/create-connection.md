---
title: Verbinding maken
description: Beschrijft hoe te om tot een verbinding aan een dataset van het Platform in Customer Journey Analytics te leiden.
translation-type: tm+mt
source-git-commit: eb7d7d80ee07298f7d0fe308bdc93a3435f2c381
workflow-type: tm+mt
source-wordcount: '1614'
ht-degree: 1%

---


# Verbinding maken

Een verbinding laat u datasets van integreren [!DNL Adobe Experience Platform] in [!UICONTROL Workspace]. Om verslag uit te brengen over [!DNL Experience Platform] datasets, moet u eerst een verband tussen datasets in vestigen [!DNL Experience Platform] en [!UICONTROL Workspace].

Klikken [hier](https://docs.adobe.com/content/help/en/platform-learn/tutorials/cja/connecting-customer-journey-analytics-to-data-sources-in-platform.html) voor een video-overzicht.

>[!IMPORTANT]
>
>U kunt meerdere [!DNL Experience Platform] datasets in één enkele verbinding.

## Sandbox en datasets selecteren

1. Ga naar [https://analytics.adobe.com](https://analytics.adobe.com).

1. Klik op de knop **[!UICONTROL Connections]** tab.

1. Klikken **[!UICONTROL Create new connection]** rechtsboven.

   ![Verbinding maken](assets/create-connection0.png)

1. Kies een sandbox in het Experience Platform die de gegevensset of gegevenssets bevat waarnaar u een verbinding wilt maken.

   Adobe Experience Platform biedt [sandboxen](https://docs.adobe.com/content/help/en/experience-platform/sandbox/home.html) die één enkele instantie van het Platform in afzonderlijke virtuele milieu&#39;s verdelen helpen digitale ervaringstoepassingen ontwikkelen en ontwikkelen. U kunt sandboxen beschouwen als &#39;gegevenssilo&#39;s&#39; die gegevenssets bevatten. Sandboxen worden gebruikt om de toegang tot gegevenssets te beheren.  Als u de sandbox hebt geselecteerd, geeft de linkerrail alle gegevenssets in die sandbox weer waaruit u kunt trekken.

   >[!IMPORTANT]
   >
   >U hebt geen toegang tot gegevens in verschillende sandboxen. U kunt dus alleen gegevenssets combineren die zich binnen dezelfde sandbox bevinden.

1. Selecteer een of meer gegevenssets die u wilt gebruiken [!UICONTROL Customer Journey Analytics] en klik op **[!UICONTROL Add]**.

   (Als u veel datasets hebt waaruit u kunt kiezen, kunt u naar de juiste zoeken met de **[!UICONTROL Search datasets]** zoekbalk boven de lijst met gegevenssets.)

## Gegevensset configureren

Aan de rechterkant kunt u nu de gegevensset(s) configureren die u hebt toegevoegd.

![Gegevensset configureren](assets/create-connection.png)

1. **[!UICONTROL Dataset type]**: Voor elke dataset die u aan deze verbinding toevoegde, [!UICONTROL Customer Journey Analytics] plaatst automatisch het datasettype dat op de gegevens wordt gebaseerd die binnen komen.

   Er zijn 3 verschillende datasettypes: [!UICONTROL Event] gegevens, [!UICONTROL Profile] gegevens, en [!UICONTROL Lookup] gegevens.

   | Type gegevensset | Beschrijving | Tijdstempel | Schema | Persoon-id |
   |---|---|---|---|---|
   | [!UICONTROL Event] | Gegevens die gebeurtenissen in de tijd vertegenwoordigen (bv. webbezoeken, interacties, transacties, POS-gegevens, enquêtegegevens, gegevens van de indruk enz.). Dit kunnen bijvoorbeeld standaard klikstreamgegevens zijn, met een klant-id of een cookie-id en een tijdstempel. Bij Gebeurtenisgegevens hebt u enige flexibiliteit met betrekking tot de id die wordt gebruikt als de Person-id. | Wordt automatisch ingesteld op het standaardtijdstempelveld vanuit op gebeurtenissen gebaseerde schema&#39;s in [!UICONTROL Experience Platform]. | Om het even welk ingebouwd of douaneschema dat op een klasse XDM met het &quot;gedrag van de Reeks van de Tijd&quot;gebaseerd is. Voorbeelden zijn &quot;XDM Experience Event&quot; of &quot;XDM Decision Event&quot;. | U kunt kiezen welke persoon-id u wilt opnemen. Voor elk gegevenssetschema dat in het Experience Platform is gedefinieerd, kan een eigen set met een of meer identiteiten zijn gedefinieerd en gekoppeld aan een naamruimte Identiteit. Elk van deze kan worden gebruikt als de persoon-id. Voorbeelden zijn Cookie-id, Stitched ID, Gebruikersnaam, Trackingcode enzovoort. |
   | [!UICONTROL Lookup] | (Dit is hetzelfde als een bestand met classificaties in traditionele Adobe Analytics.) Deze gegevens worden gebruikt om waarden of toetsen in uw gebeurtenis- of profielgegevens op te zoeken. U kunt bijvoorbeeld opzoekgegevens uploaden waarmee numerieke id&#39;s in uw gebeurtenisgegevens worden toegewezen aan productnamen. Zie [dit geval gebruiken](/help/use-cases/b2b.md) bijvoorbeeld. | N.v.t. | Een ingebouwd of aangepast schema dat is gebaseerd op een XDM-klasse met het gedrag &quot;Opnemen&quot;, behalve de klasse &quot;Individueel profiel XDM&quot;. | N.v.t. |
   | [!UICONTROL Profile] | Analoog aan [!UICONTROL Customer Attributes] - voor niet-veranderende en niet-temporele kenmerken. Gegevens die worden toegepast op uw bezoekers, gebruikers of klanten in de [!UICONTROL Event] gegevens. Bijvoorbeeld, staat u toe om de gegevens van CRM over uw klanten te uploaden. | N.v.t. | Een ingebouwd of aangepast schema dat is gebaseerd op de klasse &quot;XDM Individual Profile&quot;. | U kunt kiezen welke persoon-id u wilt opnemen. Elke gegevensset die in de [!DNL Experience Platform] heeft een eigen set van een of meer personen-id&#39;s gedefinieerd, zoals Cookie-id, Stitched ID, Gebruikersnaam, Trackingcode, enzovoort.<br>![Persoon-id ](assets/person-id.png)**Opmerking**: Als u een verbinding creeert die datasets met verschillende IDs omvat, zal het melden dat weerspiegelen. Om datasets echt samen te voegen, moet u zelfde Persoon identiteitskaart gebruiken. |

1. **[!UICONTROL Dataset ID]**: Deze id wordt automatisch gegenereerd.

1. **[!UICONTROL Time stamp]**: Alleen voor gebeurtenisgegevenssets wordt deze instelling automatisch ingesteld op het standaardtijdstempelveld vanuit op gebeurtenissen gebaseerde schema&#39;s in [!UICONTROL Experience Platform].

1. **[!UICONTROL Schema]**: Dit is het [schema](https://docs.adobe.com/content/help/en/experience-platform/xdm/schema/composition.html) op basis waarvan de gegevensset in Adobe Experience Platform is gemaakt.

1. **[!UICONTROL Person ID]**: Selecteer een persoon-id in de vervolgkeuzelijst met beschikbare identiteiten. Deze identiteiten werden bepaald in het datasetschema in het Experience Platform. Zie hieronder voor informatie over het gebruik van Identiteitskaart als Persoon identiteitskaart

   >[!IMPORTANT]
   >
   >Als er geen persoon-id&#39;s zijn waaruit u kunt kiezen, betekent dit dat een of meer persoon-id&#39;s niet zijn gedefinieerd in het schema. Weergave [deze video](https://youtu.be/G_ttmGl_LRU) over het definiëren van een identiteit in Experience Platform.

1. Klikken **[!UICONTROL Next]** om naar de [!UICONTROL Enable Connection] .

### Identiteitskaart gebruiken als identiteitskaart van de Persoon

Customer Journey Analytics ondersteunt nu de mogelijkheid om de identiteitskaart te gebruiken voor de bijbehorende persoon-id. Identiteitskaart is een structuur van kaartgegevens die iemand toestaat om sleutel -> waardeparen te uploaden. De sleutels zijn identiteitsnaamruimten en de waarde is een structuur die de identiteitswaarde bevat. De identiteitskaart bestaat op elke rij/gebeurtenis die wordt geüpload en wordt voor elke rij overeenkomstig gevuld.

De Kaart van de Identiteit is beschikbaar voor om het even welke dataset die een schema gebruikt dat op [ExperienceEvent XDM](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html) klasse. Wanneer u een dergelijke dataset selecteert die in een Verbinding CJA moet worden omvat, hebt u de optie om of een gebied als primaire identiteitskaart of de Kaart van de Identiteit te selecteren:

![](assets/idmap1.png)

Als u Identiteitskaart selecteert, krijgt u twee extra configuratieopties:

| Optie | Beschrijving |
|---|---|
| [!UICONTROL Use Primary ID Namespace] | Dit instrueert CJA, per rij, om de identiteit in de Kaart van de Identiteit te vinden die met een primair=true attribuut duidelijk is en dat als Persoon identiteitskaart voor die rij te gebruiken. Dit betekent dat dit de primaire sleutel is die in Experience Platform voor het verdelen zal worden gebruikt. Het is ook de eerste kandidaat voor gebruik als bezoekersidentiteitskaart van CJA (afhankelijk van hoe de dataset in een Verbinding CJA wordt gevormd). |
| [!UICONTROL Namespace] | (Deze optie is alleen beschikbaar als u de primaire-id-naamruimte niet gebruikt.) Identiteitsnaamruimten zijn een component van [Adobe Experience Platform Identity Service](https://docs.adobe.com/content/help/en/experience-platform/identity/namespaces.html) die dienen als indicatoren van de context waarop een identiteit betrekking heeft. Als u een naamruimte opgeeft, zoekt CJA in elke rij naar Identiteitskaart voor deze naamruimtesleutel en gebruikt de identiteit onder die naamruimte als de persoon-id voor die rij. Merk op dat aangezien CJA geen volledige datasetaftasten van alle rijen kan doen om te bepalen welke namespaces eigenlijk aanwezig zijn, alle mogelijke namespaces zijn vermeld in dropdown. U moet weten welke naamruimten in de gegevens zijn opgegeven. dit kan niet automatisch worden gedetecteerd. |

### Kwalen met de rand van Identity Map

Deze lijst toont de twee configuratieopties wanneer de randgevallen aanwezig zijn en hoe zij worden behandeld:

| Optie | Er zijn geen id&#39;s aanwezig op de identiteitskaart | Geen id&#39;s zijn gemarkeerd als primair | Meerdere id&#39;s zijn gemarkeerd als primaire id | Eén id is gemarkeerd als primaire id | Ongeldige naamruimte met een id gemarkeerd als primair |
|---|---|---|---|---|---|
| **&quot;Primaire id-naamruimte gebruiken&quot; ingeschakeld** | De rij wordt neergezet door CJA. | De rij wordt neergezet door CJA, aangezien geen primaire identiteitskaart wordt gespecificeerd. | Alle id&#39;s die als primair zijn gemarkeerd, worden onder alle naamruimten geëxtraheerd naar een lijst. Vervolgens worden ze alfabetisch gesorteerd; met deze nieuwe sortering wordt de eerste naamruimte met de eerste id gebruikt als de Persoon-id. | De enige id die als primair is gemarkeerd, wordt gebruikt als de persoon-id. | Hoewel de naamruimte ongeldig kan zijn (niet aanwezig in AEP), gebruikt CJA de primaire id onder die naamruimte als de Person-id. |
| **Specifieke naamruimte Identiteitskaart geselecteerd** | De rij wordt neergezet door CJA. | Alle id&#39;s onder de geselecteerde naamruimte worden geëxtraheerd naar een lijst en de eerste id wordt gebruikt als de Person-id. | Alle id&#39;s onder de geselecteerde naamruimte worden geëxtraheerd naar een lijst en de eerste id wordt gebruikt als de Person-id. | Alle id&#39;s onder de geselecteerde naamruimte worden geëxtraheerd naar een lijst en de eerste id wordt gebruikt als de Person-id. | Alle id&#39;s onder de geselecteerde naamruimte worden geëxtraheerd naar een lijst en de eerste id wordt gebruikt als de Person-id. (Alleen een geldige naamruimte kan tijdens het maken van de verbinding worden geselecteerd, zodat een ongeldige naamruimte/id niet kan worden gebruikt als Person-id.) |

## Verbinding inschakelen

![Verbinding inschakelen](assets/create-connection2.png)

1. Definieer de volgende instellingen om een verbinding in te schakelen:

   | Optie | Beschrijving |
   |---|---|
   | [!UICONTROL Name Connection] | Geef de verbinding een beschrijvende naam. De verbinding kan niet zonder een naam worden opgeslagen. |
   | [!UICONTROL Description] | Voeg meer details toe om deze verbinding van anderen te onderscheiden. |
   | [!UICONTROL Datasets] | De datasets die in deze verbinding inbegrepen zijn. |
   | [!UICONTROL Automatically import all new datasets in this connection, beginning today.] | Selecteer deze optie als u een aan de gang zijnde verbinding wilt vestigen, zodat om het even welke nieuwe gegevensbatches die aan de datasets in deze verbinding worden toegevoegd automatisch in stromen [!UICONTROL Workspace]. |
   | [!UICONTROL Import all existing data] | Wanneer u deze optie selecteert en de verbinding opslaat, worden alle bestaande (historische) gegevens van [!DNL Experience Platform] voor alle datasets die in deze verbinding zijn zal worden ingevoerd. In de toekomst worden alle bestaande historische gegevens voor nieuwe gegevenssets die aan deze opgeslagen verbinding zijn toegevoegd, ook automatisch geïmporteerd. <br>**Als deze verbinding eenmaal is opgeslagen, kan deze instelling niet worden gewijzigd.** |

   **Houd er rekening mee dat:**

   * Als de cumulatieve grootte van de historische gegevens voor alle datasets in de verbinding meer dan 1,5 miljard rijen bedraagt, zal een foutenmelding erop wijzen dat u niet deze hoeveelheid historische gegevens kunt invoeren. Nochtans, als u een dataset met 1 Miljoen rijen van historische gegevens moest toevoegen, en die gegevens invoerden, en een week later, een andere dataset van de zelfde grootte toevoegde en zijn historische gegevens invoerde, zou dit werken.
   * Wij geven prioriteit aan nieuwe gegevens die aan een dataset in de verbinding worden toegevoegd, zodat hebben deze gegevens de laagste latentie.
   * Alle backfill (historische) gegevens worden langzamer geïmporteerd (tot 13 maanden aan gegevens, ongeacht de grootte).

1. Klik op **[!UICONTROL Save]**.

De volgende stap in de workflow is: [een gegevensweergave maken](/help/data-views/create-dataview.md).
