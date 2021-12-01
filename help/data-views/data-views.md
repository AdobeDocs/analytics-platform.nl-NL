---
title: Overzicht van gegevensweergaven
description: In een gegevensweergave wordt aangegeven hoe u elementen van de gegevens in de CJA-verbinding wilt interpreteren, zoals metriek, afmetingen, sessies, enzovoort.
exl-id: f69e6e38-ac98-49a6-b0ce-f642af2932ae
solution: Customer Journey Analytics
source-git-commit: faaf3d19ed37019ba284b41420628750cdb413b8
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 0%

---

# Overzicht van gegevensweergaven

Een gegevensmening is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van te interpreteren [verbinding](/help/connections/create-connection.md). Hiermee worden alle afmetingen en metriek opgegeven die beschikbaar zijn in Analysis Workspace en de kolommen waarvan die dimensies en metriek hun gegevens verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

>[!NOTE]
>
>Alle instellingen die u selecteert of wijzigt in een gegevensweergave, zijn retroactief en niet-destructief. Met andere woorden, de onderliggende gegevens worden niet permanent gewijzigd.

U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met zeer verschillende sets componenten (afmetingen/metriek). U kunt ook gegevensweergaven maken met verschillende instellingen voor de time-out van een bezoek, de toewijzing, enz. U kunt bijvoorbeeld één gegevensweergave hebben waarin alle afmetingen zijn ingesteld op [!UICONTROL Last Touch]en tegelijkertijd, een andere gegevensmening (die op de zelfde dataset wordt gebaseerd) met alle dimensies die aan worden geplaatst [!UICONTROL First Touch].

Werkruimteprojecten in Customer Journey Analytics zijn gebaseerd op gegevensweergaven.

## Mogelijkheden voor gegevensweergaven

De meningen van gegevens laten u spontaan schemaelementmontages veranderen, zonder het moeten het schema in Adobe Experience Platform veranderen of uw milieu opnieuw uitvoeren CJA.

* **U kunt een component wijzigen van Metrisch in een Dimension en andersom**. U kunt metriek van koordgebieden tot stand brengen of dimensies van numerieke gebieden tot stand brengen. Dit maakt uw leven gemakkelijker, omdat u geen numeriek gebied in uw schema XDM voor elke metrisch moet creëren u wilt. In plaats daarvan kunt u deze alleen spontaan maken in het dialoogvenster met gegevensweergaven. Hier volgen enkele voorbeelden:
   * **Een of meer en/of één afmetingen maken van één schemaveld**. Het is een één-op-veel relatie. U kunt bijvoorbeeld een of meer omzetmaatstaven en/of een of meer inkomstendimensies maken van één schemaveld.
   * **Een tekenreeksveld als metrisch gebruiken**: Wanneer u een schema in Experience Platform met een dataset bevolkt, zou u niet omhoog kunnen weten welke schemaelementen u nodig hebt. Het kan bijvoorbeeld zijn dat u niet besefte dat u een metrische waarde nodig had voor &quot;Fouten op een pagina&quot;. Als gevolg hiervan hebt u geen numeriek schema-element voor dit effect gemaakt. Door een tekenreekselement als metrisch te gebruiken, kunt u nu de montages van gegevensmeningen gebruiken om te specificeren dat wanneer een koord het woord &quot;fout&quot;bevat, het als metrisch kan worden gebruikt.
   * **Een numeriek veld gebruiken als dimensie**: Bijvoorbeeld, als u de metrisch van de Opbrengst van de afmeting van de Opbrengst wilt trekken, zou de afmeting van de Opbrengst elke waarde als afmetingspunt ($100, $175, $1.000, enz.) tonen en het aantal instanties voor elk dimensie-item. De opbrengst als metrisch zou zich als het altijd gedraagt.

* **U kunt meerdere metriek maken met verschillende attribuutmodellen of met verschillende terugzoekvensters** vanuit hetzelfde schemaveld.

* **U kunt de id van een component bewerken** - dit wordt gebruikt voor compatibiliteit tussen gegevensweergaven. De component-id is de id die de rapportage-API gebruikt om een specifieke metrische of dimensie te identificeren. Omdat u willekeurig vele metriek of dimensies van één XDM gebied kunt tot stand brengen, zullen wij u de optie geven om uw eigen componentenidentiteitskaart te bepalen. Dientengevolge, metrisch u in één project van de Werkruimte gebruikt kan over gegevensmeningen (en API) compatibel zijn, zelfs als zij op totaal verschillende gebieden van verschillende verbindingen of gegevensmeningen of van een verschillend schema in XDM gebaseerd zijn.

* **U kunt de vriendschappelijke componentennaam specificeren die in Analysis Workspace zal verschijnen**. Deze naam wordt standaard overgenomen van de weergavenaam van het schema, maar u kunt deze naam nu overschrijven voor deze specifieke gegevensweergave.

* **U kunt meer op schema betrekking hebbende informatie over componenten bekijken** , zoals: het type gegevensset (gebeurtenis, profiel, raadpleging) waaruit het afkomstig is; welk schematype (koord, geheel, etc.) het afkomstig was van; en het schemapad (het XDM-veld waarop het is gebaseerd).

* **U kunt een component labelen** om het zoeken naar de werkruimte eenvoudiger te maken.

* **U kunt een component verbergen in de rapportage**. Voor sommige maateenheden en dimensies is een tweede metrische waarde of dimensie vereist voor de configuratie (zoals metrische deduplicatie of aanschafdeduplicatie). Dit staat u toe om metrisch of afmeting te bepalen die in de montages van een andere metrisch of afmeting kan worden gebruikt zonder direct in rapportering (zoals aankoopidentiteitskaart) worden blootgesteld.

* **U kunt opmaak toepassen op metrisch**, zoals decimale getallen, tijd, procent of valuta; het specificeren van decimalen; een opwaartse trend vertonen als groen of rood; en het opgeven van valutaopties.

* U kunt **creeer metrisch of afmeting die op slechts enkele waarden op het schemagebied wordt gebaseerd**. Als u bijvoorbeeld een &#39;foutmeting&#39; wilt, kunt u een metrische waarde maken in het veld Paginanaam, maar alleen pagina&#39;s opnemen die het woord &#39;fout&#39; bevatten. De metrische fouten die hiermee worden gemaakt, worden ondersteund door filters, kunnen worden ingevoegd in berekende metriek en werken met kenmerk, stroom, fallout, enzovoort.

* Voor afmetingen kunt u **automatisch alleen bepaalde waarden in een bepaald veld opnemen of uitsluiten**. Als een ontwikkelaar bijvoorbeeld een onjuiste waarde heeft verzonden van `dev mistake` in een veld kunt u het eenvoudig uitsluiten van rapportage met behulp van een regel voor uitsluiten. Het gedrag van het veld is hetzelfde als dat van de gegevens.

* U kunt **naam van containers wijzigen** in een gegevensmening en hebben die anders genoemde containeroppervlakte in om het even welk project van de Werkruimte dat op die gegevensmening gebaseerd is.

## Voorwaarden voor gegevensweergaven

* Voordat u gegevensweergaven kunt maken, moet u [opstelling één of meerdere verbindingen met de datasets van de Experience Platform](/help/connections/create-connection.md).
* Als u een gegevensweergave wilt maken of beheren, hebt u een [set machtigingen in Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=en#admin-access-permissions).

## De weergave-instellingen die u kunt overschrijven in de werkruimte

Sommige instellingen voor gegevensweergave kunnen worden overschreven in Analysis Workspace op projectniveau, andere niet.

* [!UICONTROL Lookback window]
* Metrische kenmerk
* Of gebruikers de [!UICONTROL No Value] lijstitem in een rapport

## De instellingen van de gegevensweergave die u niet kunt overschrijven in de werkruimte

* [!UICONTROL Component type]
* Metrische opmaak
* Naam gegevensweergave
* Dimension-toewijzing

## Gegevensweergaven verwijderen

Als u een gegevensweergave verwijdert in [!UICONTROL Customer Journey Analytics], geeft een foutbericht aan dat [!UICONTROL Workspace] projecten die afhankelijk zijn van deze verwijderde gegevensweergave, werken niet meer.

## Volgende stappen

* [Gegevensweergaven maken](/help/data-views/create-dataview.md)
* [Gebruiksscenario&#39;s voor gegevensweergaven](/help/data-views/data-views-usecases.md)
