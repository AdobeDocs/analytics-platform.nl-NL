---
title: Overzicht van gegevensweergaven
description: In een gegevensweergave wordt aangegeven hoe u elementen van de gegevens in de verbinding met de Customer Journey Analytics wilt interpreteren, zoals metriek, afmetingen, sessies, enzovoort.
exl-id: f69e6e38-ac98-49a6-b0ce-f642af2932ae
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: 0e4e4621abe02c022981e458282543908b2396c2
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# Overzicht van gegevensweergaven

Een gegevensmening is een container specifiek voor Customer Journey Analytics die u laat bepalen hoe te om gegevens van a [ verbinding ](/help/connections/create-connection.md) te interpreteren. Hiermee worden alle afmetingen en metriek opgegeven die beschikbaar zijn in Analysis Workspace en de kolommen waarvan die dimensies en metriek hun gegevens verkrijgen. Gegevensweergaven worden gedefinieerd ter voorbereiding op rapportage in Analysis Workspace.

>[!NOTE]
>
>Alle instellingen die u selecteert of wijzigt in een gegevensweergave, zijn retroactief en niet-destructief. Met andere woorden, de onderliggende gegevens worden niet permanent gewijzigd.

U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met zeer verschillende sets componenten (afmetingen/metriek). U kunt ook gegevensweergaven maken met verschillende instellingen voor de time-out van een bezoek, de toewijzing, enz. U kunt bijvoorbeeld een gegevensweergave hebben waarin alle afmetingen zijn ingesteld op [!UICONTROL Last Touch] en tegelijkertijd een andere gegevensweergave (op basis van dezelfde gegevensset) met alle afmetingen ingesteld op [!UICONTROL First Touch] .

Workspace-projecten in Customer Journey Analytics zijn gebaseerd op gegevensweergaven.

>[!IMPORTANT]
>
>Tot 5.000 metriek en 5.000 dimensies kunnen aan één enkele gegevensmening worden toegevoegd.

## Mogelijkheden voor gegevensweergaven {#capabilities}

De meningen van gegevens laten u spontaan de montages van het schemaelement veranderen, zonder het moeten het schema in Adobe Experience Platform veranderen of uw milieu van de Customer Journey Analytics opnieuw uitvoeren.

* U kunt een component veranderen van metrisch in een afmeting en vice versa. U kunt metriek van koordgebieden tot stand brengen of dimensies van numerieke gebieden tot stand brengen. Deze functionaliteit maakt uw leven gemakkelijker, omdat u geen numeriek gebied in uw schema XDM voor elke metrisch moet creëren u wilt. In plaats daarvan kunt u deze alleen spontaan maken in het dialoogvenster met gegevensweergaven. Hier volgen enkele voorbeelden:
   * **creeer één of meerdere en/of één dimensies van één enkel schemagebied**. Het is een één-op-veel relatie. U kunt bijvoorbeeld een of meer omzetmaatstaven en/of een of meer inkomstendimensies maken van één schemaveld.
   * **Gebruik een koordgebied als metrisch**: Wanneer u een schema in Experience Platform met een dataset bevolkt, zou u niet omhoog kunnen weten welke schemaelementen u nodig hebt. Bijvoorbeeld, kunt u niet gerealiseerd hebben dat u metrisch voor *Fouten op een pagina* nodig had. Als gevolg hiervan hebt u geen numeriek schema-element voor dit effect gemaakt. Wanneer u een tekenreekselement als metrisch gebruikt, kunt u nu de instellingen voor gegevensweergaven gebruiken om op te geven dat een tekenreeks altijd het woord `error` bevat en als metrisch kan worden gebruikt.
   * **gebruik een numeriek gebied als afmeting**: Bijvoorbeeld, als u metrische Inkomsten van de afmeting van de Inkomsten wilt trekken, zou de afmeting van de Inkomsten elke waarde als afmetingspunt tonen. En het aantal instanties voor elk afmetingspunt als metrisch.

* U kunt veelvoudige metriek met verschillende attributiemodellen of verschillende raadplegingsvensters van het zelfde schemagebied tot stand brengen.

* U kunt de id van een component bewerken voor compatibiliteit met de weergave van kruisgegevens. De component-id is de id die de rapportage-API gebruikt om een specifieke metrische of dimensie te identificeren. Omdat u willekeurig vele metriek of afmetingen van één gebied kunt tot stand brengen XDM, hebt u de optie om uw eigen componentenidentiteitskaart te bepalen Dientengevolge, metrisch u in één project van Workspace gebruikt kan op gegevensmeningen (en API) compatibel worden gebruikt. Zelfs als de metriek op totaal verschillende gebieden van verschillende verbindingen, gegevensmeningen, of van een verschillend schema in XDM gebaseerd zijn.

* U kunt de vriendschappelijke componentennaam specificeren die in Analysis Workspace verschijnt. Deze naam wordt standaard overgenomen van de weergavenaam van het schema, maar u kunt deze naam nu overschrijven voor deze specifieke gegevensweergave.

* U kunt meer op schema betrekking hebbende informatie over componenten bekijken. Bijvoorbeeld:

   * het type gegevensset (gebeurtenis, profiel, opzoekopdracht, samenvatting) waaruit de component afkomstig is;
   * welk schematype (koord, geheel, etc.) het van oorsprong is, en
   * het schemapad (het XDM gebied dat het gebaseerd is op).

* U kunt een component labelen om het zoeken naar de component in Workspace eenvoudiger te maken.

* U kunt een component verbergen in de rapportage. Voor sommige maateenheden en dimensies is een tweede metrische waarde of dimensie vereist voor de configuratie (zoals metrische deduplicatie of aanschafdeduplicatie, bijvoorbeeld). Door een component te verbergen, kunt u een component definiëren die kan worden gebruikt in de instellingen van een andere component zonder dat deze beschikbaar wordt gemaakt in de rapportage.

* U kunt opmaak toepassen op metrische gegevens, zoals cijfers achter de komma, de tijd, het percentage of de valuta, decimalen, groene of rode cijfers en de groene of rode cijfers die u opgeeft en valutaopties.

* U kunt een metrische of afmeting tot stand brengen die op slechts enkele waarden op het schemagebied wordt gebaseerd. Als u bijvoorbeeld een metrische waarde voor fouten wilt, kunt u een metrische waarde maken in het veld Paginanaam, maar alleen pagina&#39;s opnemen die het woord `error` bevatten. De op deze manier gemaakte fouten ondersteunen filters, kunnen in berekende metriek worden ingevoegd en werken met kenmerk, stroom, fallout, enzovoort.

* Voor afmetingen kunt u automatisch alleen bepaalde waarden in een bepaald veld opnemen of uitsluiten. Als een ontwikkelaar bijvoorbeeld een onjuiste waarde van `dev mistake` naar een veld verzendt, kunt u deze eenvoudig uitsluiten van rapportage met een regel voor uitsluiten. De dimensie gedraagt zich alsof de verkeerde waarde nooit in de gegevens bestond.

* U kunt de naam van uw containers wijzigen in een gegevensweergave en de namen van containers wijzigen in elk Workspace-project dat is gebaseerd op die gegevensweergave.

## Voorwaarden voor gegevensweergaven {#prerequisites}

* Alvorens u gegevensmeningen kunt tot stand brengen, moet u opstelling één of meerdere verbindingen aan Experience Platform datasets ](/help/connections/create-connection.md).[
* Om een gegevensmening tot stand te brengen of te beheren, hebt u a [ reeks toestemmingen in Adobe Admin Console ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) nodig.
* Als u de [ bronschakelaar van Adobe Analytics ](/help/data-ingestion/analytics.md) gebruikt of Adobe Analytics achtergrondkennis hebt, zou u kunnen willen begrijpen hoe de gebieden in uw schema&#39;s en datasets op de tegenhangers van Adobe Analytics betrekking hebben. Zie [ het gebiedsafbeeldingen van Analytics ](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/mapping/analytics) voor meer informatie.

## Instellingen voor gegevensweergave die u kunt overschrijven in Workspace {#settings-override}

Sommige instellingen voor gegevensweergave kunnen worden overschreven in Analysis Workspace op projectniveau, andere niet.

* [!UICONTROL Lookback window]
* Metrische kenmerk
* Bepaalt of gebruikers het [!UICONTROL No Value] regelitem in een rapport al dan niet zien

## Instellingen voor gegevensweergave die u niet kunt overschrijven in Workspace {#settings-no-override}

* [!UICONTROL Component type]
* Metrische opmaak
* Naam gegevensweergave
* Toewijzing Dimension

## Gegevensweergaven verwijderen {#delete}

Als u een gegevensweergave verwijdert in [!UICONTROL Customer Journey Analytics] , geeft een foutbericht aan dat [!UICONTROL Workspace] -projecten die afhankelijk zijn van deze verwijderde gegevensweergave, niet meer werken.

## Volgende stappen

* [Gegevensweergaven maken](/help/data-views/create-dataview.md)
* [Gebruiksscenario&#39;s voor gegevensweergaven](/help/use-cases/data-views/data-views-usecases.md)
