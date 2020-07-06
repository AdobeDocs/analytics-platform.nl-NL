---
title: Verbinding maken
description: Beschrijft hoe te om tot een verbinding aan een dataset van het Platform in Customer Journey Analytics te leiden.
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 1%

---


# Verbinding maken

Een verbinding laat u datasets van [!DNL Adobe Experience Platform] in integreren [!UICONTROL Workspace]. Om over [!DNL Experience Platform] datasets te rapporteren, moet u eerst een verband tussen datasets in [!DNL Experience Platform] en [!UICONTROL Workspace].

Klik [hier](https://docs.adobe.com/content/help/en/platform-learn/tutorials/cja/connecting-customer-journey-analytics-to-data-sources-in-platform.html) voor een video-overzicht.

>[!IMPORTANT]
>
>U kunt veelvoudige [!DNL Experience Platform] datasets in één enkele verbinding combineren.

1. Ga naar [https://analytics.adobe.com](https://analytics.adobe.com).

1. Klik op het **[!UICONTROL Connections]** tabblad.

1. Klik **[!UICONTROL Create new connection]** op de rechterbovenhoek.

   ![Verbinding maken](assets/create-connection.png)

1. Kies een sandbox in het Experience Platform die de gegevensset of gegevenssets bevat waarnaar u een verbinding wilt maken.

   Adobe Experience Platform biedt [sandboxen](https://docs.adobe.com/content/help/en/experience-platform/sandbox/home.html) die één Platform-instantie in afzonderlijke virtuele omgevingen verdelen om toepassingen voor digitale ervaring te ontwikkelen en te ontwikkelen. U kunt sandboxen beschouwen als &#39;gegevenssilo&#39;s&#39; die gegevenssets bevatten. Sandboxen worden gebruikt om de toegang tot gegevenssets te beheren. U hebt geen toegang tot gegevens in verschillende sandboxen. Als u de sandbox hebt geselecteerd, geeft de linkerrail alle gegevenssets in die sandbox weer waaruit u kunt trekken.

1. Selecteer een of meer gegevenssets die u wilt gebruiken [!UICONTROL Customer Journey Analytics] en klik op **[!UICONTROL Add]**.

   (Als u veel datasets hebt waaruit u kunt kiezen, kunt u naar de juiste zoeken met de zoekbalk boven de lijst met gegevenssets.)

1. Daarna, voor elke dataset die u aan deze verbinding toevoegde, plaatst [!UICONTROL Customer Journey Analytics] automatisch het datasettype dat op de gegevens wordt gebaseerd die binnen komen.

   Er zijn 3 verschillende datasettypes: [!UICONTROL Event] gegevens, [!UICONTROL Profile] gegevens en [!UICONTROL Lookup] gegevens.

   | Type gegevensset | Beschrijving | Tijdstempel | Schema | Persoon-id |
   |---|---|---|---|---|
   | [!UICONTROL Event] | Gegevens die gebeurtenissen in de tijd vertegenwoordigen (bv. webbezoeken, interacties, transacties, POS-gegevens, enquêtegegevens, gegevens van de indruk enz.). Dit kunnen bijvoorbeeld standaard klikstreamgegevens zijn, met een klant-id of een cookie-id en een tijdstempel. Bij Gebeurtenisgegevens hebt u enige flexibiliteit met betrekking tot de id die wordt gebruikt als de Person-id. | Wordt automatisch ingesteld op het standaardtijdstempelveld van op gebeurtenissen gebaseerde schema&#39;s in [UICONTROL-Experience Platform]. | Om het even welk ingebouwd of douaneschema dat op een klasse XDM met het &quot;gedrag van de Reeks van de Tijd&quot;gebaseerd is. Voorbeelden zijn &quot;XDM Experience Event&quot; of &quot;XDM Decision Event&quot;. | U kunt kiezen welke persoon-id u wilt opnemen. Voor elk gegevenssetschema dat in het Experience Platform is gedefinieerd, kan een eigen set met een of meer identiteiten zijn gedefinieerd en gekoppeld aan een naamruimte Identiteit. Elk van deze kan worden gebruikt als de persoon-id. Voorbeelden zijn Cookie-id, Stitched ID, Gebruikersnaam, Trackingcode enzovoort. |
   | [!UICONTROL Lookup] | Dit is gelijk aan een bestand met classificaties. Deze gegevens worden gebruikt om waarden of toetsen in uw gebeurtenis- of profielgegevens op te zoeken. U kunt bijvoorbeeld opzoekgegevens uploaden waarmee numerieke id&#39;s in uw gebeurtenisgegevens worden toegewezen aan productnamen. | N.v.t. | Een ingebouwd of aangepast schema dat is gebaseerd op een XDM-klasse met het gedrag &quot;Opnemen&quot;, behalve de klasse &quot;Individueel profiel XDM&quot;. | N.v.t. |
   | [!UICONTROL Profile] | Analoog aan [!UICONTROL Customer Attributes] - voor niet-veranderende en niet-temporale kenmerken. Gegevens die worden toegepast op uw bezoekers, gebruikers of klanten in de [!UICONTROL Event] gegevens. Bijvoorbeeld, staat u toe om de gegevens van CRM over uw klanten te uploaden. | N.v.t. | Een ingebouwd of aangepast schema dat is gebaseerd op de klasse &quot;XDM Individual Profile&quot;. | U kunt kiezen welke persoon-id u wilt opnemen. Elke gegevensset die in de gegevensset is gedefinieerd, [!DNL Experience Platform] heeft een eigen set met een of meer personen-id&#39;s gedefinieerd, zoals Cookie-id, Stitched ID, Gebruikersnaam, Trackingcode enzovoort.<br>![Persoon](assets/person-id.png)**IDNote **: Als u een verbinding creeert die datasets met verschillende IDs omvat, zal het melden dat weerspiegelen. Om datasets echt samen te voegen, moet u zelfde Persoon identiteitskaart gebruiken. |

1. Klik **[!UICONTROL Next]** om naar het [!UICONTROL Create Connection] dialoogvenster te gaan.

   ![Verbinding maken](assets/create-connection2.png)

1. Definieer de volgende instellingen in het [!UICONTROL Create Connection] dialoogvenster:

   | Veld | Beschrijving |
   |---|---|
   | [!UICONTROL Name Connection] | Geef de verbinding een beschrijvende naam. De verbinding kan niet zonder een naam worden opgeslagen. |
   | [!UICONTROL Description] | Voeg meer details toe om deze verbinding van anderen te onderscheiden. |
   | [!UICONTROL Datasets] | De datasets die in deze verbinding inbegrepen zijn. |
   | [!UICONTROL Automatically import all new datasets in this connection, beginning today.] | Selecteer deze optie als u een aan de gang zijnde verbinding wilt vestigen, zodat om het even welke nieuwe gegevensbatches die aan de datasets in deze verbinding worden toegevoegd automatisch in stromen [!UICONTROL Workspace]. |
   | [!UICONTROL Import all existing data] | Wanneer u deze optie selecteert en de verbinding opslaat, worden alle bestaande (historische) gegevens uit [!DNL Experience Platform] alle gegevenssets die in deze verbinding aanwezig zijn, geïmporteerd. In de toekomst worden alle bestaande historische gegevens voor nieuwe gegevenssets die aan deze opgeslagen verbinding zijn toegevoegd, ook automatisch geïmporteerd. <br>**Als deze verbinding eenmaal is opgeslagen, kan deze instelling niet worden gewijzigd.** |

   **Houd er rekening mee dat:**

   * Als de cumulatieve grootte van de historische gegevens voor alle datasets in de verbinding meer dan 1,5 miljard rijen bedraagt, zal een foutenmelding erop wijzen dat u niet deze hoeveelheid historische gegevens kunt invoeren. Nochtans, als u een dataset met 1 Miljoen rijen van historische gegevens moest toevoegen, en die gegevens invoerden, en een week later, een andere dataset van de zelfde grootte toevoegde en zijn historische gegevens invoerde, zou dit werken.
   * Wij geven prioriteit aan nieuwe gegevens die aan een dataset in de verbinding worden toegevoegd, zodat hebben deze gegevens de laagste latentie.
   * Alle backfill (historische) gegevens worden langzamer geïmporteerd.

1. Klik op **[!UICONTROL Save]**.

De volgende stap in de workflow is het [maken van een gegevensweergave](/help/data-views/create-dataview.md).
