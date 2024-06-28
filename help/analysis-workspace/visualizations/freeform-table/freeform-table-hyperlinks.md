---
title: Hyperlinks maken in een vrije-vormtabel in Analysis Workspace
description: Leer hoe u hyperlinks maakt voor dimensie-items in een vrije-vormtabel in Analysis Workspace
feature: Visualizations
role: User
exl-id: 24fc2d24-b8c2-4664-8b9c-beda284f9033
source-git-commit: 8941b6a8339294cf121a07ca0c14bac50342d04e
workflow-type: tm+mt
source-wordcount: '1736'
ht-degree: 0%

---

# Hyperlinks maken voor afmetingen in een vrije-vormtabel

U kunt hyperlinks maken voor dimensie-items, zodat hierop kan worden geklikt in een vrije-vormtabel in Analysis Workspace.

Deze functionaliteit is vooral handig bij het maken van hyperlinks voor de volgende typen dimensies:

* Items Dimensionen die URL-waarden hebben waarnaar u een koppeling wilt maken (bijvoorbeeld een pagina-URL-dimensie)

* Items van een Dimension die onderverdelingen bevatten met URL-waarden waarnaar u wilt koppelen (bijvoorbeeld een pagina-naamdimensie met een indeling van een pagina-URL-dimensie)

* Items of uitsplitsingen in Dimensionen met waarden die onderdeel zijn van een URL waarnaar u een koppeling wilt maken (bijvoorbeeld een paginanaam die deel uitmaakt van een URL)

+++ Bekijk een videodemonstratie van deze functie.

>[!VIDEO](https://video.tv.adobe.com/v/3430411/?learn=on)

+++

## Hyperlinks maken voor een of meer afmetingsitems

Houd rekening met het volgende wanneer u hyperlinks maakt voor dimensie-items:

* De hyperlinks die u maakt, worden opgeslagen in de vrije-vormtabel in het Analysis Workspace-project. Hyperlinks blijven niet bestaan wanneer u dezelfde dimensie- of dimensie-items in een andere tabel of in een ander project gebruikt.

* Als u de gegevensweergave van de vrije-vormlijst wijzigt, zijn alle hyperlinks die voor dimensies of dimensie-items in de tabel zijn gemaakt, nog steeds beschikbaar, op voorwaarde dat de dimensie in de gegevensweergave bestaat.

* URL&#39;s worden niet gecontroleerd op geldigheid wanneer u de hyperlink maakt.

  Als u een hyperlink maakt die een ongeldige URL heeft, of als u een hyperlink maakt die verwijst naar een dimensie-item dat geen URL-waarde heeft (door rechtstreeks naar het dimensie-item te verwijzen of door het `$value` of `$breakdown` (variabelen), wordt een foutbericht weergegeven voor gebruikers die op de hyperlink klikken.

* Hyperlinks die voor één enkel afmetingspunt worden gecreeerd treden hyperlinks met voeten die op de afmeting worden gecreeerd.

* Hyperlinks zijn niet functioneel in [gedownloade PDF-bestanden](/help/analysis-workspace/export/download-send.md).

U kunt als volgt hyperlinks maken voor een of meer dimensies:

1. Voer een van de volgende handelingen uit in een vrije-vormtabel in Analysis Workspace:

   * **Een hyperlink maken voor één dimensie-item:** Klik met de rechtermuisknop op het dimensie-item in de tabel waarvoor u de hyperlink wilt maken en selecteer vervolgens [!UICONTROL **Hyperlink maken**].

     ![Hyperlink maken voor één dimensie-item](assets/hyperlink-single-add.png)

     De [!UICONTROL **Hyperlink maken**] wordt weergegeven. De naam van het dimensie-item waarvoor u een hyperlink maakt, wordt weergegeven in het dialoogvenster.

     ![Hyperlink maken voor één itemdialoogvenster](assets/hyperlink-dialog-single.png)

   * **Maak hyperlinks voor alle afmetingsitems in een afmetingskolom:** Klik met de rechtermuisknop op de naam van de dimensie in de kolomkop Afmeting en selecteer [!UICONTROL **Hyperlinks maken voor alle dimensie-items**].

     ![Hyperlink maken voor een dimensie](assets/hyperlink-multiple-add.png)

     De [!UICONTROL **Hyperlinks maken voor alle dimensie-items**] wordt weergegeven. De naam van de dimensie waarvoor u hyperlinks maakt, wordt weergegeven in het dialoogvenster.

     ![Dialoogvenster Hyperlinks maken](assets/hyperlink-dialog-multiple.png)

1. Kies een van de volgende opties:

   * [!UICONTROL **De waarde van het dimensie-item gebruiken als de URL**]: Kies deze optie voor afmetingsitems met URL-waarden, zoals een pagina-URL-dimensie.

     Als u bijvoorbeeld een pagina-URL-dimensie gebruikt waarvan de waarde van elk dimensie-item een URL is, maakt u met deze optie een hyperlink naar de URL.

   * [!UICONTROL **Een aangepaste URL maken**]: Geef een statische of dynamische aangepaste URL op. Kies deze optie om hyperlinks te maken voor dimensie-items die geen URL-waarden hebben.

     Als u bijvoorbeeld een dimensie Paginanaam gebruikt waarbij de waarde van elk dimensie-item de naam van een pagina is (en niet een volledige URL), kunt u met deze optie een hyperlink opgeven die u wilt gebruiken als de koppeling voor het dimensie-item.

     Als u dynamische URL&#39;s wilt maken voor meerdere dimensie-items, kunt u de opdracht `$value` en `$breakdown` variabelen in uw aangepaste URL. Zie de onderstaande tabel voor meer informatie.

     Als u een aangepaste URL wilt maken, geeft u de volgende informatie op:

     | Veld | Beschrijving |
     |---------|----------|
     | [!UICONTROL **Aangepaste URL**] | Geef een aangepaste URL op die u voor de hyperlink wilt gebruiken. URL&#39;s moeten als volledig gekwalificeerde URL&#39;s worden ingevoerd. Bijvoorbeeld: <https://www.example.com><p>De aangepaste URL die u maakt, kan statisch of dynamisch zijn:</p> <ul><li>**Statische URL&#39;s:** Als u een hyperlink maakt voor een afzonderlijk dimensie-item, is een statische URL mogelijk voldoende. <p>Neem het volgende voorbeeld: als u bijvoorbeeld een pagina-naamafmetingsitem hebt, kunt u een statische URL maken die gebruikers koppelt aan de specifieke webpagina die u aan de paginanaam wilt koppelen.</p><p>Veronderstel dat u hyperlinks voor een lijst van afmetingspunten wilt tot stand brengen, elk die met zijn respectieve definitie in de documentatie binnen een interne wiki- pagina verbinden.</p><p>U kunt dit bereiken door een statische URL te maken voor elk dimensie-item. Bijvoorbeeld:</p><p>https://wiki.internal.company_name/page_name#item_definition</p></li><li>**Dynamische URL&#39;s:** Als u een hyperlink voor veelvoudige afmeting punten of voor alle afmetingspunten in een afmetingskolom creeert, dan is dynamische URL waarschijnlijk praktischer. <p>Als u aangepaste URL&#39;s dynamisch wilt maken, neemt u variabelen in de URL op waarmee de URL dynamisch kan worden gewijzigd op basis van de waarde van de dimensie zelf of de waarde van de afbraakdimensie.</p><p>Wanneer u variabelen gebruikt, worden dimensieitems die tekens bevatten die niet geldig zijn in URL&#39;s (zoals spaties), URL-gecodeerd.</p><p>De volgende variabelen zijn beschikbaar: (**Opmerking**: Hoewel u deze variabelen in dezelfde URL kunt gebruiken, is het waarschijnlijker dat u ze afzonderlijk gebruikt.)</p> <ul><li>**`$value`:** Hiermee kunt u de waarde van het dimensie-item invoegen in de URL die u opgeeft. <p>Neem het volgende scenario als voorbeeld:</p><p>Stel dat u hyperlinks wilt maken voor alle pagina-naamatems in een vrije-vormtabel, waarbij de waarde van elk dimensie-item deel uitmaakt van de URL van een webpagina. In dit geval kunt u één aangepaste URL maken die dynamisch voor elk dimensie-item wordt aangepast. </p><p>U kunt dit bereiken door de `$value` aan het einde van de aangepaste URL die u opgeeft. Bijvoorbeeld:</p> <p>https://company-name.com/browse/product#\$value</p><p>Wanneer deze aangepaste URL wordt toegepast op de pagina-naamatems waarvan de waarden &quot;ProductY&quot; en &quot;ProductZ&quot; zijn, zien de gegenereerde hyperlinks er ongeveer als volgt uit: </p><p>https://company-name.com/browse/product#ProductY</p><p>en</p><p> https://company-name.com/browse/product#ProductZ </p><p>![waarden gebruiken in hyperlinks](assets/table-hyperlinks-vaule.png)</p><p>**Tip**: Als u alleen de opdracht `$value` variabele in het veld Aangepaste URL zou gelijk zijn aan het selecteren van de [!UICONTROL **De waarde van het dimensie-item gebruiken**] als u de URL maakt.</p></li><li>**`$breakdown`:** Hiermee kunt u de waarde van het item voor de splitsingsdimensie invoegen in de URL die u opgeeft. Dit staat u toe om een afmeting met een gebruikersvriendelijke naam in uw rapport (zoals een afmeting van de Naam van het Product) te gebruiken terwijl het creëren van hyperlink die op een afbraakafmeting wordt gebaseerd die minder gebruikersvriendelijk (zoals een identiteitskaart van het Product of de afmeting van URL van de Pagina) zou kunnen zijn.<p>Bij het verwijzen naar een uitsplitsingsdimensie is het het meest gebruikelijk dat er slechts één uitsplitsingspost voor een gegeven dimensie-item is. Indien er meerdere uitsplitsingsposten zijn voor een gegeven dimensie-item, wordt de waarde van de eerste uitsplitsingspost gebruikt in de URL. Als er geen uitsplitsingsitems worden weergegeven, is de URL ongeldig. Op de uitsplitsingsposten wordt dezelfde sorteervolgorde toegepast als op de tabel.</p><p>U geeft de afbraakdimensie op in het dialoogvenster [!UICONTROL **Dimensie uitsplitsing**] veld hieronder.</p> <p>Overweeg het voorbeeldscenario dat voor wordt beschreven [!UICONTROL **Dimensie uitsplitsing**] veld hieronder.</p></li></ul> |
     | [!UICONTROL **Afmetingen onderverdelingen (optioneel)**] | Typ de naam van de afbraakdimensie die u wilt gebruiken en selecteer deze in de vervolgkeuzelijst. <p>Als u een afbrekingsdimensie in dit veld selecteert, moet u ernaar verwijzen met de opdracht `$breakdown` variabele in de URL die u in het dialoogvenster [!UICONTROL **Aangepaste URL**] veld.</p><p>Neem het volgende scenario als voorbeeld:</p><p>Veronderstel dat u hyperlinks voor alle de afmetingspunten van de Naam van het Product in een vrije lijst wilt tot stand brengen. Elk item van de productnaam bevat een uitsplitsing van een product-id-dimensie.</p></p>In dit geval, kunt u hyperlinks voor elke dimensie van de Naam van het Product tot stand brengen die gebruikers aan de productpagina door de waarde van de de verdelingsdimensie van identiteitskaart van het Product te gebruiken leidt. </p><p>U kunt dit bereiken door de `$breakdown` variabele tot het einde van de aangepaste URL die u in het dialoogvenster [!UICONTROL **Aangepaste URL**] veld. Bijvoorbeeld:</p><p>https://company-name.com/browse/product/$breakdown</p><p>Wanneer deze aangepaste URL wordt toegepast op de elementen van de productnaam met items voor de afbraakdimensie waarvan de waarden &quot;ProductY&quot; en &quot;ProductZ&quot; zijn, zien de gegenereerde hyperlinks er ongeveer als volgt uit:</p><p>https://company-name.com/browse/product/ProductY</p><p>en</p><p>https://company-name.com/browse/product/ProductZ</p><p>Vervolgens selecteert u de dimensie Product ID in het dialoogvenster [!UICONTROL **Dimensie uitsplitsing**] field </p><p>![gebruik onderverdelingen in hyperlinks](assets/table-hyperlinks-breakdown.png)</p> |

1. Selecteren [!UICONTROL **Maken**].

   Gebruikers die de vrije-vormlijst bekijken zien de hyperlinked dimensiepunten. Wanneer gebruikers op een dimensie-item klikken, worden ze naar de pagina&#39;s met hyperlinks op een apart browsertabblad geleid.

   <!-- add screenshot of a table with hyperlinks.-->

1. [Het project opslaan](/help/analysis-workspace/build-workspace-project/save-projects.md) om uw wijzigingen op te slaan.

## Hyperlinks bewerken

U kunt hyperlinks bewerken die zijn gemaakt voor dimensies of dimensies-items in een vrije-vormtabel.

1. Voer een van de volgende handelingen uit in een vrije-vormtabel in Analysis Workspace:

   * **Een hyperlink bewerken voor één dimensie-item:** Klik met de rechtermuisknop op het dimensie-item in de tabel waar u de hyperlink wilt bewerken.

     ![Hyperlink bewerken voor één dimensie-item](assets/hyperlink-single-edit.png)

   * **Bewerk hyperlinks voor alle dimensie-items in een dimensiekolom:** Klik met de rechtermuisknop op de naam van de dimensie in de kolomkop Afmeting.

     ![Hyperlink bewerken voor een dimensie](assets/hyperlink-dimension-edit.png)

1. Selecteren [!UICONTROL **Hyperlink bewerken**] in het snelmenu.

   De [!UICONTROL **Hyperlinks bewerken voor dimensie-items**] wordt weergegeven.

1. Voor informatie over de configuratieopties voor het bewerken van de hyperlink raadpleegt u Stap 3 in de [Hyperlinks maken voor een of meer afmetingsitems](#create-hyperlinks-for-one-or-more-dimension-items) sectie hierboven, selecteer vervolgens [!UICONTROL **Toepassen**] als u klaar bent met uw updates.

1. [Het project opslaan](/help/analysis-workspace/build-workspace-project/save-projects.md) om uw wijzigingen op te slaan.

## Hyperlinks verwijderen

U kunt hyperlinks verwijderen die zijn gemaakt voor dimensie-items in een vrije-vormtabel.

>[!NOTE]
>
>Als u in een vrije-vormlijst een dimensie verwijdert die hyperlinks bevat, blijven de hyperlinks niet behouden als u dezelfde dimensie weer aan de vrije-vormtabel toevoegt.

Hyperlinks verwijderen uit dimensieitems:

1. Voer een van de volgende handelingen uit in een vrije-vormtabel in Analysis Workspace:

   * **Een hyperlink verwijderen uit één dimensie-item:** Klik met de rechtermuisknop op het dimensie-item in de tabel waar u de hyperlink wilt verwijderen.

     ![Hyperlink verwijderen uit één dimensie-item](assets/hyperlink-single-remove.png)

   * **Verwijder hyperlinks uit alle afmetingsitems in een afmetingskolom:** Klik met de rechtermuisknop op de naam van de dimensie in de kolomkop Afmeting.

     ![Hyperlink verwijderen uit een dimensie](assets/hyperlink-dimension-remove.png)

1. Selecteren [!UICONTROL **Hyperlink verwijderen**] in het snelmenu.

   De hyperlink wordt verwijderd uit het item met één dimensie (als u één dimensie-item hebt geselecteerd) of uit alle dimensie-items (als u de naam van de dimensie hebt geselecteerd in de kolomkop met dimensie).

1. [Het project opslaan](/help/analysis-workspace/build-workspace-project/save-projects.md) om uw wijzigingen op te slaan.
