---
title: Gebruikershandleiding voor Adobe Analytics-gebruikers
description: Wat moet u vanuit het perspectief van de gebruiker overwegen wanneer uw bedrijf gegevens van Adobe Analytics naar Customer Journey Analytics verplaatst?
role: User
solution: Customer Journey Analytics
feature: Basics
exl-id: e4762cca-b2da-422b-b48f-2a5fec14c97f
source-git-commit: 720751130d0f66bddffd13c6f160a85fcc7a7206
workflow-type: tm+mt
source-wordcount: '1427'
ht-degree: 0%

---

# Gebruikershandleiding voor Adobe Analytics-gebruikers

Als uw organisatie Adobe Customer Journey Analytics in dienst begint te nemen, kunt u enige gelijkenissen en verschillen tussen Adobe Analytics en Customer Journey Analytics opmerken. Deze pagina is bedoeld om deze verschillen toe te lichten, zodat uw organisatie sneller kan deelnemen aan de nieuwe implementatie- en rapportageworkflow. Deze pagina biedt ook extra bronnen over nieuwe concepten en verdere stappen om uw reis als analist gemakkelijker en succesvoller te maken.

Verschillende functies in Customer Journey Analytics krijgen een andere naam en worden opnieuw ontworpen om aan de industriestandaarden te voldoen. Sommige bijgewerkte terminologie omvat segmenten, virtuele rapportsuites, classificaties, klantenattributen, en containernamen. De beperkingen van eVars en props bestaan niet meer, ten gunste van flexibele aangepaste afmetingen en maatstaven.

## Wat niet is gewijzigd

Veel van wat u op de verslaggevende kant kent is niet veranderd.

* U kunt nog de macht van [ Analysis Workspace ](/help/analysis-workspace/home.md) gebruiken om uw gegevens te analyseren. Workspace werkt hetzelfde als in traditionele Adobe Analytics.
* De zelfde versie van [ dashboards van Adobe Analytics ](/help/mobile-app/home.md) is beschikbaar, en werkt zo ook tussen Customer Journey Analytics en Adobe Analytics.
* [ Report Builder ](/help/report-builder/rb-overview.md) heeft een nieuwe interface en loopt op Vensters van MS, MacOS, en de Webversie van Excel. (Vóór deze versie van Report Builder kon u de toepassing alleen op Mac gebruiken als u deze op VMware had uitgevoerd.) Deze versie biedt nog geen ondersteuning voor traditionele AA-gegevensaanvragen.

## Wijzigingen in de rapportage

U hebt veel meer toegang tot kanaalgegevens om te analyseren. Bijvoorbeeld, kunt u een werkruimteproject tot stand brengen dat prestaties van veelvoudige kanalen analyseert, op voorwaarde dat deze datasets door uw organisatie worden opgenomen en in gegevensmeningen inbegrepen die door Customer Journey Analytics worden gebruikt (zie &quot;Veranderingen in gegevensarchitectuur&quot;hieronder).

![ de Bronmening die van Gegevens multi-kanaal-visualisaties ](assets/cross-channel.png) tonen

## Wijzigingen in gegevensarchitectuur {#architecture}

Customer Journey Analytics haalt zijn gegevens op uit Adobe Experience Platform. Met Experience Platform kunt u klantgegevens en -inhoud van elk systeem of kanaal centraliseren en standaardiseren. Met kunt u gegevenswetenschappen en computerleren toepassen om het ontwerp en de levering van persoonlijke ervaringen te verbeteren.

De gegevens van de klant in Experience Platform worden opgeslagen als datasets, die uit a [ schema ](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/schemas-and-experience-data-model.html) en partijen gegevens bestaan. Voor meer detail op het platform, zie [ het Overzicht van de Architectuur van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/platform-learn/tutorials/intro-to-platform/basic-architecture.html).

Uw Customer Journey Analytics Admin vestigt [ verbindingen ](/help/connections/create-connection.md) aan datasets in Experience Platform. Zij bouwen dan [ gegevensmeningen ](/help/data-views/data-views.md) gebruikend die verbindingen. De meningen van gegevens zijn conceptueel gelijkaardig aan virtuele rapportreeksen, en zijn de basis van rapportering in Customer Journey Analytics. Aangezien Experience Platform alle gegevens voor rapportage levert, bestaan deze sets niet meer als een container voor gegevens.

Met een verbinding kunnen uw Analytics Admin gegevenssets van Adobe Experience Platform integreren in Customer Journey Analytics.


<!-- Outdated UI

>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Configuring connections](https://video.tv.adobe.com/){target="_blank"} for a demo video.

>[!ENDSHADEBOX]

-->


Adobe biedt meerdere manieren om gegevens naar Adobe Experience Platform over te brengen, waaronder rapportsuite-gegevens via de Analytics-bronconnector of de Web SDK. De bestaande implementaties van veelvoudige rapportreeksen kunnen in Experience Platform worden gecombineerd. De verbindingen en gegevensmeningen die op deze datasets gebaseerd zijn kunnen gegevens combineren die eerder in afzonderlijke rapportreeksen bestonden.

## Wijzigingen in het concept van virtuele-rapportensuites {#data-views}

[!UICONTROL Data views] neem het concept virtuele rapportreeksen aangezien zij vandaag bestaan en breid het uit om [ extra controles op de gegevens ](/help/data-views/create-dataview.md) toe te laten die door verbindingen beschikbaar worden gemaakt. Deze veranderingen maken algemene montages zoals timezone en zittingsonderbrekingsintervallen configureerbaar en retroactief. De individuele veranderlijke montages zoals attributie en vervaldatum kunnen ook op een rapport of een niveau van de gegevensmening worden aangepast. Deze instellingen zijn niet-destructief en retroactief.

U ziet dat de rapportsuite-kiezer in de rechterbovenhoek u nu in de beschikbare gegevensweergaven laat kiezen:

![ gegeven-mening-selecteur ](assets/data-views.png)

Zie [ gevallen van het Gebruik rond gegevensmeningen ](/help/use-cases/data-views/data-views-usecases.md) voor meer informatie rond dit concept.

## Wijzigingen in het concept van eVars en props

De concepten [!UICONTROL eVars] , [!UICONTROL props] en [!UICONTROL events] in traditionele Adobe Analytics bestaan niet meer in [!UICONTROL Customer Journey Analytics] . In Adobe Analytics worden in eVars en props beschrijvingen van inhoud, klanten, campagnes, enzovoort opgeslagen. en gebeurtenissen tellen dingen zoals opbrengst, abonnementen, of geproduceerde lood. Customer Journey Analytics bewaart beide soorten gegevens, en u kunt tot hen toegang hebben de zelfde manier - van de linkerspoorstaaf in Analysis Workspace, onder Afmetingen of Metriek, respectievelijk.

In Customer Journey Analytics zijn onbeperkte schema-elementen beschikbaar, zoals afmetingen, metriek en lijstvelden. Deze worden toegewezen aan onbeperkte schema-elementen, zoals afmetingen, metriek en lijstgebieden in Experience Platform. Alle instellingen voor bezoeken en toeschrijvingen die zijn toegepast na de verwerkingsregels in Adobe Analytics, zijn nu van toepassing op het querytijdstip in Customer Journey Analytics.

Met deze flexibiliteit, kunt u in situaties lopen waarin één enkel schemagebied als zowel dimensies als metrisch kan worden gebruikt om verschillende het volgen behoeften te steunen.

## Wijzigingen van het begrip &quot;segmenten&quot;

Hoewel segmenten technisch niet van Adobe Analytics naar Customer Journey Analytics worden gemigreerd, kunt u het hulpmiddel van de componentenmigratie gebruiken om uw segmenten van Adobe Analytics in Customer Journey Analytics opnieuw tot stand te brengen. Segmenten worden opnieuw gemaakt in Customer Journey Analytics op basis van de afmetingen en maatstaven die zijn toegewezen. Voor meer informatie, zie [ voorbereidingen treffen om componenten en projecten van Adobe Analytics aan Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration.html) te migreren.

Hoewel u [!UICONTROL segments] ([!UICONTROL segments]) nog niet kunt delen of publiceren van [!DNL Customer Journey Analytics] naar Experience Platform Unified Profile, wordt deze functionaliteit momenteel ontwikkeld.

Naast het concept van segmenten die veranderen, worden de segmentcontainers ook bijgewerkt.

* **de containers van het Actief zijn nu [!UICONTROL Event] containers**. Met de container [!UICONTROL Event] kunt u de gegevens van de persoon opsplitsen op basis van individuele gebeurtenissen.
* **de containers van het Bezoek zijn nu [!UICONTROL Session] containers**. Met de container [!UICONTROL Session] kunt u paginainteracties, campagnes of conversies voor een bepaalde sessie identificeren.
* **de containers van de Bezoeker zijn nu [!UICONTROL Person] containers**. De container [!UICONTROL Person] bevat elke sessie en gebeurtenis voor een persoon binnen de opgegeven tijdsperiode.

## Wijzigingen in het concept van berekende meetwaarden

Berekende metriek hebben een vergelijkbare naam tussen Adobe Analytics en Customer Journey Analytics. [!UICONTROL Customer Journey Analytics] gebruikt echter geen variabelen, profielen of gebeurtenissen meer en gebruikt in plaats daarvan geen Experience Platform-schema-elementen. Deze fundamentele wijziging houdt in dat geen van de bestaande berekende meetgegevens compatibel is met [!UICONTROL Customer Journey Analytics] .


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Bewegend berekende metriek van Adobe Analytics aan Customer Journey Analytics ](https://video.tv.adobe.com/v/31788?quality=12&learn=on){target="_blank"} voor een demovideo op hoe te om berekende metriek te bewegen.

>[!ENDSHADEBOX]

## Wijzigingen in instellingen voor variabeletoewijzing en -vervaldatum

[!UICONTROL Customer Journey Analytics] past alle variabelemontages, met inbegrip van attributie en vervaldatum, op rapporttijd toe. Deze montages verblijven nu in [ gegevensmeningen ](/help/data-views/component-settings/persistence.md), en sommige veranderlijke montages (zoals attributie) kunnen in de projecten van Workspace worden veranderd.

U kunt meerdere versies van dezelfde variabele in dezelfde gegevensweergave hebben. Bijvoorbeeld, kunt u één het Volgen dimensie van de Code hebben die na 30 dagen verloopt, en een andere die aan het eind van een zitting verloopt. Beide volgcodeafmetingen gebruiken dezelfde brongegevens, maar gebruiken verschillende toewijzingsinstellingen.

U kunt ook meerdere gegevensweergaven hebben op basis van dezelfde verbinding. U kunt bijvoorbeeld een gegevensweergave hebben met een sessietime-out van 30 minuten en een andere met een sessietime-out van 15 minuten. Beide gegevensweergaven worden weergegeven in de rechterbovenkiezer, zodat u naadloos kunt overschakelen tussen de weergaven.

## Wijzigingen in het begrip classificatie

De &quot;classificaties&quot;zijn nu gekend als *datasets van de Opzoekopdracht*. De datasets van de opzoekopdracht worden gebruikt om op waarden of sleutels te kijken die in uw gegevens van de Gebeurtenis of van het Profiel worden gevonden. U kunt bijvoorbeeld opzoekgegevens uploaden waarmee numerieke id&#39;s in uw gebeurtenisgegevens worden toegewezen aan productnamen.

## Wijzigingen in het concept van klantkenmerken

De &quot;attributen van de Klant&quot;zijn nu genoemd geworden &quot;datasets van het Profiel&quot;. De datasets van het profiel bevatten gegevens die op uw personen, gebruikers, of klanten in de [!UICONTROL Event] gegevens worden toegepast. Bijvoorbeeld, staat het u toe om de gegevens van CRM over uw klanten te uploaden. U kunt kiezen welke persoon-id u wilt opnemen. Voor elke gegevensset die in [!DNL Experience Platform] wordt gedefinieerd, is een eigen set met een of meer personen-id&#39;s gedefinieerd.

## Wijzigingen in de manier waarop Adobe bezoekers identificeert

Customer Journey Analytics breidt de concepten van identiteiten uit tot buiten ECIDs om het even welke identiteitskaart te omvatten u, met inbegrip van Klant identiteitskaart, Cookie identiteitskaart, Titched ID, Gebruiker - identiteitskaart, het Volgen Code, etc. wilt gebruiken. Het gebruiken van gemeenschappelijke namespace identiteitskaart over datasets, of het gebruiken van [ het Stitching ](../stitching/overview.md) hulp verbindt mensen samen over verschillende datasets. Elke gebruiker die een Workspace-project in Customer Journey Analytics instelt, moet de gebruikte id&#39;s in de datasets begrijpen. Bekijk de volgende video waarin het gebruik van identiteiten in Customer Journey Analytics wordt benadrukt


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Gebruikend identiteit in Customer Journey Analytics ](https://video.tv.adobe.com/v/30750/?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]

## Veranderingen in het concept van laag-verkeersdimensie punt

In traditionele Adobe Analytics begint een variabele die te veel unieke waarden ontvangt, de dimensie-items onder [!UICONTROL Low-Traffic] te zetten. Customer Journey Analytics heeft minder beperkingen op velden met een hoge kwaliteit. Door wijzigingen in de rapportagearchitectuur kan Analysis Workspace vele meer unieke dimensieitems rapporteren. Zie [ Hoge kardinale afmetingen ](../components/dimensions/high-cardinality.md) voor meer informatie rond hoe Customer Journey Analytics het melden voor dimensies met vele unieke waarden optimaliseert.
