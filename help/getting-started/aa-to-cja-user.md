---
title: Gebruikershandleiding voor Adobe Analytics-gebruikers
description: Wat vanuit het perspectief van de gebruiker te overwegen wanneer uw bedrijf gegevens van Adobe Analytics aan Customer Journey Analytics verplaatst
role: User
solution: Customer Journey Analytics
feature: Basics
exl-id: e4762cca-b2da-422b-b48f-2a5fec14c97f
source-git-commit: a25129c0a319b13f5167c8cde9535dbb4b3ca65a
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Gebruikershandleiding voor Adobe Analytics-gebruikers

Als uw organisatie Adobe Customer Journey Analytics in dienst begint te nemen, kunt u enige gelijkenissen en verschillen tussen Adobe Analytics en Customer Journey Analytics opmerken. Deze pagina is bedoeld om deze verschillen toe te lichten, zodat uw organisatie sneller kan deelnemen aan de nieuwe implementatie- en rapportageworkflow. Deze pagina biedt ook extra bronnen over nieuwe concepten en verdere stappen om uw reis als analist gemakkelijker en succesvoller te maken.

Verschillende functies in Customer Journey Analytics krijgen een nieuwe naam en worden opnieuw ontworpen om aan de industriestandaarden te voldoen. Sommige bijgewerkte terminologie omvat segmenten, virtuele rapportsuites, classificaties, klantenattributen, en containernamen. De beperkingen van eVars en props bestaan niet meer, ten gunste van flexibele aangepaste afmetingen en maatstaven.

## Wat niet is gewijzigd

Veel van wat u op de verslaggevende kant kent is niet veranderd.

* U kunt de kracht van [Analysis Workspace](/help/analysis-workspace/home.md) om uw gegevens te analyseren. Workspace werkt op dezelfde manier als in traditionele Adobe Analytics.
* Dezelfde versie van [Adobe Analytics-dashboards](/help/mobile-app/home.md) is beschikbaar en werkt op vergelijkbare wijze tussen Customer Journey Analytics en Adobe Analytics.
* [Report Builder](/help/report-builder/report-buider-overview.md) heeft een nieuwe interface en loopt op MS Windows, MacOS, en de Webversie van Excel. (Vóór deze versie van Report Builder kunt u deze alleen gebruiken in Mac als u deze versie op VMware hebt uitgevoerd.) Deze versie biedt nog geen ondersteuning voor traditionele AA-gegevensaanvragen.

## Wijzigingen in de rapportage

U hebt veel meer toegang tot kanaalgegevens om te analyseren. Bijvoorbeeld, kunt u een werkruimteproject tot stand brengen dat prestaties van veelvoudige kanalen analyseert, op voorwaarde dat deze datasets door uw organisatie worden opgenomen en in gegevensmeningen inbegrepen die door Customer Journey Analytics worden gebruikt (zie &quot;Veranderingen in gegevensarchitectuur&quot;hieronder).

![meerkanaalse visualisaties](assets/cross-channel.png)

## Wijzigingen in gegevensarchitectuur {#architecture}

Customer Journey Analytics krijgt zijn gegevens van Adobe Experience Platform. Met Experience Platform kunt u klantgegevens en inhoud van elk systeem of kanaal centraliseren en standaardiseren. Bovendien kunt u door middel van het leren van gegevens en computers het ontwerp en de levering van persoonlijke ervaringen verbeteren.

De gegevens van de klant in het Experience Platform worden opgeslagen als datasets, die uit een [schema](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/schemas-and-experience-data-model.html) en batches gegevens. Zie voor meer informatie over het platform [Overzicht van Adobe Experience Platform-architectuur](https://experienceleague.adobe.com/docs/platform-learn/tutorials/intro-to-platform/basic-architecture.html).

Uw Customer Journey Analytics Admin vestigt [verbindingen](/help/connections/create-connection.md) op gegevensreeksen in Experience Platform. Vervolgens bouwen ze [gegevensweergaven](/help/data-views/data-views.md) die verbindingen gebruiken. De meningen van gegevens zijn conceptueel gelijkaardig aan virtuele rapportreeksen, en zijn de basis van rapportering in Customer Journey Analytics. Aangezien het Experience Platform alle gegevens voor rapportering verstrekt, bestaan de rapportreeksen niet meer als container voor gegevens.

Met een verbinding kunnen uw Analytics Admin gegevenssets van Adobe Experience Platform integreren in Customer Journey Analytics, die in de volgende video zijn opgenomen:

>[!VIDEO](https://video.tv.adobe.com/v/35111/?quality=12)

Adobe biedt veelvoudige manieren aan om gegevens in te brengen in Adobe Experience Platform, met inbegrip van rapportreeksgegevens door de van de Bron Adobe Analytics Schakelaar of Web SDK. De bestaande implementaties van veelvoudige rapportreeksen kunnen in Experience Platform worden gecombineerd. De verbindingen en gegevensmeningen die op deze datasets gebaseerd zijn kunnen gegevens combineren die eerder in afzonderlijke rapportreeksen bestonden.

## Wijzigingen in het concept van virtuele-rapportensuites {#data-views}

[!UICONTROL Data views] het concept van virtuele - rapportensuites zoals ze vandaag bestaan , uitbreiden tot [extra controles van de gegevens toelaten](/help/data-views/create-dataview.md) beschikbaar gesteld door verbindingen. Deze veranderingen maken algemene montages zoals timezone en zittingsonderbrekingsintervallen configureerbaar en retroactief. De individuele veranderlijke montages zoals attributie en vervaldatum kunnen ook op een rapport of een niveau van de gegevensmening worden aangepast. Deze instellingen zijn niet-destructief en retroactief.

U ziet dat de rapportsuite-kiezer in de rechterbovenhoek u nu in de beschikbare gegevensweergaven laat kiezen:

![data-view-selector](assets/data-views.png)

Zie [Gebruik hoofdletters en kleine letters in gegevensweergaven](/help/use-cases/data-views/data-views-usecases.md) voor meer informatie over dit concept .

## Wijzigingen in het concept van eVars en props

De begrippen [!UICONTROL eVars], [!UICONTROL props], en [!UICONTROL events] in het traditionele Adobe Analytics bestaat niet meer in [!UICONTROL Customer Journey Analytics]. In Adobe Analytics worden in eVars en props beschrijvingen van inhoud, klanten, campagnes, enzovoort opgeslagen. en gebeurtenissen tellen dingen zoals opbrengst, abonnementen, of geproduceerde lood. Customer Journey Analytics behoudt beide typen gegevens en u kunt ze op dezelfde manier benaderen - vanaf de linkerspoorstaaf in Analysis Workspace, onder Dimension of Metrics.

In Customer Journey Analytics zijn onbeperkte schema-elementen beschikbaar, zoals afmetingen, metriek en lijstvelden. Deze worden toegewezen aan onbeperkte schemaelementen met inbegrip van afmetingen, metriek en lijstgebieden in Experience Platform. Alle instellingen voor bezoeken en toeschrijvingen die zijn toegepast na de verwerkingsregels in Adobe Analytics, zijn nu van toepassing op het querytijdstip in Customer Journey Analytics.

Met deze flexibiliteit, kunt u in situaties lopen waarin één enkel schemagebied als zowel dimensies als metrisch kan worden gebruikt om verschillende het volgen behoeften te steunen.

## Wijzigingen van het begrip &quot;segmenten&quot;

Adobe heeft de naam van de component &quot;segmenten&quot; gewijzigd in &quot;filters&quot; om deze beter af te stemmen op de industriestandaarden en een beter onderscheid te maken met segmenten in Adobe Experience Platform.

[!UICONTROL Customer Journey Analytics] gebruikt niet meer eVars, props, of gebeurtenissen en gebruikt in plaats daarvan de het schemagebiedsnaam van het Experience Platform waaraan zij in kaart zijn gebracht. Deze wijziging betekent dat geen van de bestaande segmenten in Adobe Analytics compatibel is met [!UICONTROL Customer Journey Analytics]. Zie de volgende video als u bestaande Adobe Analytics-segmenten naar Customer Journey Analytics wilt verplaatsen:

>[!VIDEO](https://video.tv.adobe.com/v/31982/?quality=12)

Hoewel u nog niet kunt delen of publiceren [!UICONTROL filters] ([!UICONTROL segments]) van [!DNL Customer Journey Analytics] aan Experience Platform verenigd Profiel, is deze functionaliteit in ontwikkeling.

Naast het concept van segmenten die veranderen, worden de segmentcontainers ook bijgewerkt.

* **Handcontainers zijn nu [!UICONTROL Event] containers**. De [!UICONTROL Event] Met container kunt u persoonlijke gegevens onderverdelen op basis van individuele gebeurtenissen.
* **Bezoek containers zijn nu [!UICONTROL Session] containers**. De [!UICONTROL Session] Met container kunt u paginainteracties, campagnes of conversies voor een specifieke sessie identificeren.
* **Bezoekerscontainers zijn nu [!UICONTROL Person] containers**. De [!UICONTROL Person] container omvat elke zitting en gebeurtenis voor een persoon binnen het gespecificeerde tijdkader.

## Wijzigingen in het concept van berekende meetwaarden

Berekende metriek hebben een vergelijkbare naam tussen Adobe Analytics en Customer Journey Analytics. Maar [!UICONTROL Customer Journey Analytics] gebruikt niet meer eVars, props, of gebeurtenissen en gebruikt in plaats daarvan om het even welk element van het Experience Platform schema. Deze fundamentele wijziging betekent dat geen van de bestaande berekende meetwaarden compatibel is met [!UICONTROL Customer Journey Analytics]. Bekijk de volgende video als u berekende metriek van Adobe Analytics naar Customer Journey Analytics wilt verplaatsen:

>[!VIDEO](https://video.tv.adobe.com/v/31788/?quality=12)

## Wijzigingen in instellingen voor variabeletoewijzing en -vervaldatum

[!UICONTROL Customer Journey Analytics] past alle veranderlijke montages, met inbegrip van attributie en afloop, op rapporttijd toe. Deze instellingen bevinden zich nu in [gegevensweergaven](/help/data-views/component-settings/persistence.md)en sommige variabeleninstellingen (zoals kenmerk) kunnen worden gewijzigd in Workspace-projecten.

U kunt meerdere versies van dezelfde variabele in dezelfde gegevensweergave hebben. Bijvoorbeeld, kunt u één het Volgen dimensie van de Code hebben die na 30 dagen verloopt, en een andere die aan het eind van een zitting verloopt. Beide volgcodeafmetingen gebruiken dezelfde brongegevens, maar gebruiken verschillende toewijzingsinstellingen.

U kunt ook meerdere gegevensweergaven hebben op basis van dezelfde verbinding. U kunt bijvoorbeeld een gegevensweergave hebben met een sessietime-out van 30 minuten en een andere met een sessietime-out van 15 minuten. Beide gegevensweergaven worden weergegeven in de rechterbovenkiezer, zodat u naadloos kunt overschakelen tussen de weergaven.

## Wijzigingen in het begrip classificatie

&quot;Classificaties&quot; worden nu &quot;Gegevensbestanden opzoeken&quot; genoemd. De datasets van de opzoekopdracht worden gebruikt om op waarden of sleutels te kijken die in uw gegevens van de Gebeurtenis of van het Profiel worden gevonden. U kunt bijvoorbeeld opzoekgegevens uploaden waarmee numerieke id&#39;s in uw gebeurtenisgegevens worden toegewezen aan productnamen. Zie [Gegevens op accountniveau toevoegen als een opzoekgegevensset](/help/use-cases/b2b/b2b.md) voor een voorbeeld gebruikt.

## Wijzigingen in het concept van klantkenmerken

De &quot;attributen van de Klant&quot;zijn nu genoemd geworden &quot;datasets van het Profiel&quot;. De datasets van het profiel bevatten gegevens die op uw personen, gebruikers, of klanten in worden toegepast [!UICONTROL Event] gegevens. Bijvoorbeeld, staat het u toe om de gegevens van CRM over uw klanten te uploaden. U kunt kiezen welke persoon-id u wilt opnemen. Elke gegevensset gedefinieerd in [!DNL Experience Platform] heeft een eigen set van een of meer personen-id&#39;s gedefinieerd.

## Wijzigingen in de manier waarop Adobe bezoekers identificeert

Customer Journey Analytics breidt de begrippen van identiteiten voorbij ECIDs uit om het even welke identiteitskaart te omvatten u, met inbegrip van Klant identiteitskaart, Cookie identiteitskaart, Titched ID, Gebruiker - identiteitskaart, het Volgen Code, etc. wilt gebruiken. Gebruikend gemeenschappelijke namespace identiteitskaart over datasets, of het gebruiken [Stiksel](../stitching/overview.md) de hulp verbindt mensen over verschillende datasets samen. Om het even welke gebruiker die opstelling een project van de Werkruimte in Customer Journey Analytics moet IDs begrijpen over de datasets wordt gebruikt. Bekijk de volgende video waarin het gebruik van identiteiten in Customer Journey Analytics wordt benadrukt:

>[!VIDEO](https://video.tv.adobe.com/v/30750/?quality=12)

## Veranderingen in het concept van laag-verkeersdimensie punt

In traditionele Adobe Analytics begint een variabele die te veel unieke waarden ontvangt, de dimensie-items onder te knippen [!UICONTROL Low-Traffic]. Customer Journey Analytics heeft minder beperkingen op velden met een hoge kwaliteit. Door wijzigingen in de rapportagearchitectuur kan Analysis Workspace vele meer unieke dimensies rapporteren. Zie [Resultaten afgekapt dimensie-item](../analysis-workspace/workspace-faq/results-truncated.md) voor meer informatie over hoe Customer Journey Analytics het rapporteren van dimensies met vele unieke waarden optimaliseert.
