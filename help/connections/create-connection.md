---
title: Verbinding maken
description: Beschrijft hoe te om een verbinding aan een dataset van het Platform in de Analyse van de Reis van de Klant tot stand te brengen.
translation-type: tm+mt
source-git-commit: fa7898d73756c33a0bae22c8758bc9f0a649626a

---


# Verbinding maken

Een verbinding laat u datasets van [!DNL Adobe Experience Platform] in integreren [!UICONTROL Workspace]. Om over de datasets van het Platform te rapporteren, moet u eerst een verbinding tussen datasets in Platform en Werkruimte vestigen.

Klik [hier](https://docs.adobe.com/content/help/en/platform-learn/tutorials/cja/connecting-customer-journey-analytics-to-data-sources-in-platform.html) voor een video-overzicht.

>[!IMPORTANT] U kunt veelvoudige datasets van het Platform in één enkele verbinding combineren.

1. Ga naar [https://analytics.adobe.com](https://analytics.adobe.com).

1. Klik op het **[!UICONTROL Connections]** tabblad.

1. Klik **[!UICONTROL Create new connection]** op de rechterbovenhoek.

![Verbinding maken](assets/create-connection.png)

1. De linkerspoorstaaf toont alle datasets in Platform die u van kunt trekken. Selecteer een of meer gegevenssets die u wilt gebruiken [!UICONTROL Customer Journey Analytics] en klik op **[!UICONTROL Add]**. (Als u veel datasets hebt waaruit u kunt kiezen, kunt u naar de juiste zoeken met de zoekbalk boven de lijst met gegevenssets.)

1. Daarna, voor elke dataset die u aan deze verbinding toevoegde, plaatst [!UICONTROL Customer Journey Analytics] automatisch het datasettype dat op de gegevens wordt gebaseerd die binnen komen. Er zijn 3 verschillende datasettypes: Gebeurtenisgegevens, profielgegevens en opzoekgegevens.

   | Type gegevensset | Beschrijving | Tijdstempel | Schema | Persoon-id |
   |---|---|---|---|---|
   | [!UICONTROL Event] | Gegevens die gebeurtenissen in de tijd vertegenwoordigen (bv. webbezoeken, interacties, transacties, POS-gegevens, enquêtegegevens, gegevens van de indruk enz.). Dit zijn typisch klikstroomgegevens, met een klant identiteitskaart of een koekjesidentiteitskaart, en een timestamp. Met gebeurtenisgegevens kunt u de gewenste id gebruiken. | Wordt ingesteld op Tijdstempel. | Het schema van het Platform dat dit datasettype is gebaseerd op. | N.v.t. |
   | [!UICONTROL Lookup] | Dit is gelijk aan een bestand met classificaties. Deze gegevens worden gebruikt voor het opzoeken van waarden of toetsen in de gebeurtenis- of profielgegevens. U kunt bijvoorbeeld opzoekgegevens uploaden waarmee numerieke id&#39;s in uw gebeurtenisgegevens worden toegewezen aan productnamen. | N.v.t. | Het schema van het Platform dat dit datasettype is gebaseerd op. | N.v.t. |
   | [!UICONTROL Profile] | Analoog aan [!UICONTROL Customer Attributes] - voor niet-veranderende en niet-temporale kenmerken. Gegevens die worden toegepast op uw bezoekers, gebruikers of klanten in de [!UICONTROL Event] gegevens. Bijvoorbeeld, staat u toe om de gegevens van CRM over uw klanten te uploaden. | N.v.t. | Het [!UICONTROL Platform] schema waarop dit gegevenstype is gebaseerd. | U kunt kiezen welke persoon-id u wilt opnemen. Voor elke gegevensset die in het Adobe Experience Platform is gedefinieerd, is een eigen set met een of meer personen-id&#39;s gedefinieerd, zoals Cookie-id, Stitched ID, Gebruikersnaam, Trackingcode, enzovoort.<br>![Persoon](assets/person-id.png)**IDNote **: Als u een verbinding creeert die datasets met verschillende IDs omvat, zal het melden dat weerspiegelen. Om datasets echt samen te voegen, moet u zelfde identiteitskaart van de Persoon gebruiken. |

1. Als u klikt, gaat **[!UICONTROL Next]** u naar het [!UICONTROL Create Connection] dialoogvenster.

   ![Verbinding maken](assets/create-connection2.png)

1. Definieer de volgende instellingen in het [!UICONTROL Create Connection] dialoogvenster:

   | Veld | Beschrijving |
   |---|---|
   | [!UICONTROL Name Connection] | Geef de verbinding een beschrijvende naam. De verbinding kan niet zonder een naam worden opgeslagen. |
   | [!UICONTROL Description] | Voeg meer details toe om deze verbinding van anderen te onderscheiden. |
   | [!UICONTROL Datasets] | De datasets die in deze verbinding inbegrepen zijn. |
   | [!UICONTROL Automatically import all new datasets in this connection, beginning today.] | Selecteer deze optie als u een aan de gang zijnde verbinding wilt vestigen, zodat om het even welke nieuwe gegevensbatches die aan de datasets in deze verbinding worden toegevoegd automatisch in stromen [!UICONTROL Workspace]. |
   | [!UICONTROL Import all existing data] | Wanneer u deze optie selecteert en de verbinding opslaat, worden alle bestaande (historische) gegevens van Platform voor alle datasets die in deze verbinding aanwezig zijn, geïmporteerd. In de toekomst worden alle bestaande historische gegevens voor nieuwe gegevenssets die aan deze opgeslagen verbinding zijn toegevoegd, ook automatisch geïmporteerd. <br>**Als deze verbinding eenmaal is opgeslagen, kan deze instelling niet worden gewijzigd.** |

   **Houd er rekening mee dat:**

   * Als de cumulatieve grootte van de historische gegevens voor alle datasets in de verbinding meer dan 1,5 miljard rijen bedraagt, zal een foutenmelding erop wijzen dat u niet deze hoeveelheid historische gegevens kunt invoeren. Nochtans, als u een dataset met 1 Miljoen rijen van historische gegevens moest toevoegen, en die gegevens invoerden, en een week later, een andere dataset van de zelfde grootte toevoegde en zijn historische gegevens invoerde, zou dit werken.
   * Wij geven prioriteit aan nieuwe gegevens die aan een dataset in de verbinding worden toegevoegd, zodat hebben deze gegevens de laagste latentie.
   * Alle backfill (historische) gegevens worden langzamer geïmporteerd.

1. Klik op **[!UICONTROL Save]**.

De volgende stap in de workflow is het [maken van een gegevensweergave](/help/data-views/create-dataview.md).
