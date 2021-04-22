---
title: Wat is een gegevensweergave in Customer Journey Analytics?
description: In een gegevensweergave wordt aangegeven hoe u elementen van de gegevens in de CJA-verbinding wilt interpreteren, zoals metriek, afmetingen, sessies, enzovoort.
exl-id: f69e6e38-ac98-49a6-b0ce-f642af2932ae
translation-type: tm+mt
source-git-commit: 37c667b9c3f85e781c79a6595648be63c686649b
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 0%

---

# Wat is een gegevensweergave?

Een gegevensweergave bevindt zich boven op een Customer Journey Analytics (CJA) [verbinding](/help/connections/create-connection.md). Een verbinding combineert één of meerdere datasets van Adobe Experience Platform en verbindt het met CJA. In de gegevensweergave wordt aangegeven hoe u elementen van de gegevens in de verbinding wilt interpreteren, zoals metriek, afmetingen, sessies, enzovoort. Gegevensweergaven worden gedefinieerd als voorbereiding op het rapporteren van gegevens in Workspace.

>[!NOTE]
>
>Alle instellingen die u selecteert of wijzigt in een gegevensweergave, zijn retroactief en niet-destructief. Met andere woorden, de onderliggende gegevens worden niet permanent gewijzigd.

U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met zeer verschillende sets componenten (afmetingen/metriek). U kunt ook gegevensweergaven maken met verschillende instellingen voor de time-out van een bezoek, de toewijzing, enz. U kunt bijvoorbeeld een gegevensweergave hebben waarin alle afmetingen zijn ingesteld op [!UICONTROL Last Touch] en tegelijkertijd een andere gegevensweergave (op basis van dezelfde gegevensset) met alle afmetingen ingesteld op [!UICONTROL First Touch].

Werkruimteprojecten in Customer Journey Analytics zijn gebaseerd op gegevensweergaven.

## Nieuwe functies in gegevensweergaven?

De nieuwste update van gegevensweergaven biedt u veel meer flexibiliteit in wat u kunt doen met gegevensweergaven. Deze verhogingen laten u **schemaelementmontages in de Mening van Gegevens spontaan veranderen, zonder het moeten het schema in Adobe Experience Platform veranderen of uw milieu CJA opnieuw uitvoeren**.

* **U kunt een component wijzigen van Metrisch in Dimension en andersom**. U kunt metriek van koordgebieden tot stand brengen of dimensies van numerieke gebieden tot stand brengen. Dit maakt uw leven gemakkelijker, omdat u geen numeriek gebied in uw schema XDM voor elke metrisch moet creëren u wilt. In plaats daarvan kunt u deze alleen spontaan maken in het dialoogvenster met gegevensweergaven. Hier volgen enkele voorbeelden:
   * **Maak een of meer en/of één afmetingen van één schemaveld**. Het is een één-op-veel relatie. U kunt bijvoorbeeld een of meer omzetmaatstaven en/of een of meer inkomstendimensies maken van één schemaveld.
   * **Gebruik een tekenreeksveld als metrisch**: Wanneer u een schema in Experience Platform met een dataset bevolkt, zou u niet omhoog kunnen weten welke schemaelementen u nodig hebt. Het kan bijvoorbeeld zijn dat u niet besefte dat u een metrische waarde nodig had voor &quot;Fouten op een pagina&quot;. Als gevolg hiervan hebt u geen numeriek schema-element voor dit effect gemaakt. Door een tekenreekselement als metrisch te gebruiken, kunt u nu de montages van gegevensmeningen gebruiken om te specificeren dat wanneer een koord het woord &quot;fout&quot;bevat, het als metrisch kan worden gebruikt.
   * **Een numeriek veld gebruiken als een afmeting**: Bijvoorbeeld, als u de metrisch van de Opbrengst van de afmeting van de Opbrengst wilt trekken, zou de afmeting van de Opbrengst elke waarde als afmetingspunt ($100, $175, $1.000, enz.) tonen en het aantal instanties voor elk dimensie-item. De opbrengst als metrisch zou zich als het altijd gedraagt.

* **U kunt meerdere metriek maken met verschillende attributiemodellen of met verschillende terugzoekvensters** van hetzelfde schemaveld.

* **U kunt de id van een component**  bewerken. Dit wordt gebruikt voor compatibiliteit tussen gegevensweergaven. De component-id is de id die de rapportage-API gebruikt om een specifieke metrische of dimensie te identificeren. Omdat u willekeurig vele metriek of dimensies van één XDM gebied kunt tot stand brengen, zullen wij u de optie geven om uw eigen componentenidentiteitskaart te bepalen. Dientengevolge, metrisch u in één project van de Werkruimte gebruikt kan over gegevensmeningen (en API) compatibel zijn, zelfs als zij op totaal verschillende gebieden van verschillende verbindingen of gegevensmeningen of van een verschillend schema in XDM gebaseerd zijn.

* **U kunt de vriendschappelijke componentennaam specificeren die in Analysis Workspace** zal verschijnen. Deze naam wordt standaard overgenomen van de weergavenaam van het schema, maar u kunt deze naam nu overschrijven voor deze specifieke gegevensweergave.

* **U kunt meer op schema betrekking hebbende informatie over componenten** , zoals bekijken: het type gegevensset (gebeurtenis, profiel, raadpleging) waaruit het afkomstig is; welk schematype (koord, geheel, etc.) het afkomstig was van; en het schemapad (het XDM-veld waarop het is gebaseerd).

* **U kunt een** component labelen om het zoeken naar de component in Workspace eenvoudiger te maken.

* **U kunt een component verbergen in de rapportage**. Voor sommige maateenheden en dimensies is een tweede metrische waarde of dimensie vereist voor de configuratie (zoals metrische deduplicatie of aanschafdeduplicatie). Dit staat u toe om metrisch of afmeting te bepalen die in de montages van een andere metrisch of afmeting kan worden gebruikt zonder direct in rapportering (zoals aankoopidentiteitskaart) worden blootgesteld.

* **U kunt opmaak toepassen op metrische** getallen, zoals decimalen, tijd, percentages of valuta&#39;s. het specificeren van decimalen; een opwaartse trend vertonen als groen of rood; en het opgeven van valutaopties.

* U kunt **een metrische of afmeting tot stand brengen die op slechts enkele waarden op het schemagebied** wordt gebaseerd. Als u bijvoorbeeld een &#39;foutmeting&#39; wilt, kunt u een metrische waarde maken in het veld Paginanaam, maar alleen pagina&#39;s opnemen die het woord &#39;fout&#39; bevatten. De metrische fouten die hiermee worden gemaakt, worden ondersteund door filters, kunnen worden ingevoegd in berekende metriek en werken met kenmerk, stroom, fallout, enzovoort.

* Voor afmetingen kunt u **automatisch alleen bepaalde waarden in een bepaald veld opnemen of uitsluiten**. Als een ontwikkelaar bijvoorbeeld een onjuiste waarde van `dev mistake` naar een veld verzendt, kunt u deze eenvoudig uitsluiten van rapportage met een uitsluitingsregel en gedraagt het zich alsof het nooit in de gegevens bestond.

* U kunt de naam van uw containers **wijzigen** in een gegevensweergave en die hernoemde containeroppervlakte hebben in elk project van de Werkruimte dat op die gegevensmening gebaseerd is.

## Voorwaarden voor gegevensweergaven

* Alvorens u gegevensmeningen kunt tot stand brengen, moet u [opstelling één of meerdere verbindingen aan Experience Platform datasets](/help/connections/create-connection.md).
* Als u een gegevensweergave wilt maken of beheren, hebt u een [set machtigingen nodig in Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=en#admin-access-permissions).

## De weergave-instellingen die u kunt overschrijven in de werkruimte

Sommige instellingen voor gegevensweergave kunnen worden overschreven in Analysis Workspace op projectniveau, andere niet.

* Venster Opzoeken
* Metrische kenmerken
* Bepaalt of gebruikers het regelitem Geen waarde in een rapport al dan niet zien

## De instellingen van de gegevensweergave die u niet kunt overschrijven in de werkruimte

* Componenttype
* Metrische opmaak
* Naam gegevensweergave
* Dimension-toewijzing

## Gegevensweergaven verwijderen

Als u een gegevensmening in [!UICONTROL Customer Journey Analytics] schrapt, zal een foutenmelding erop wijzen dat om het even welke projecten van de Werkruimte die van deze geschrapte gegevensmening afhangen niet meer zullen werken.
