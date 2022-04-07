---
title: CJA-gebruikershandleiding voor Adobe Analytics-gebruikers
description: Wat vanuit het perspectief van de gebruiker te overwegen wanneer uw bedrijf gegevens van Adobe Analytics aan Customer Journey Analytics verplaatst
role: User
solution: Customer Journey Analytics
feature: CJA Basics
exl-id: e4762cca-b2da-422b-b48f-2a5fec14c97f
source-git-commit: 570fb36de0ed81f001ed6115e73d1d4347f368ec
workflow-type: tm+mt
source-wordcount: '1245'
ht-degree: 0%

---

# CJA-gebruikershandleiding voor Adobe Analytics-gebruikers

Uw bedrijf begint Customer Journey Analytics in dienst te nemen. Als gebruiker die bekend is met Adobe Analytics, hebt u al een geweldige start. Wanneer u met Customer Journey Analytics werkt, zult u enige gelijkenissen en enkele grote verschillen zien. Deze pagina is bedoeld om de dingen uit te leggen die niet zijn gewijzigd, en ook een aantal van de grote verschillen. Wij zullen u ook vertellen hoe u meer informatie over nieuwe concepten kunt krijgen, en verdere stappen om UW klantenreis gemakkelijker en succesvoller te maken.

Verschillende functies in CJA zijn in vergelijking met traditionele Adobe Analytics hernoemd en opnieuw ontworpen om aan de industrienormen te voldoen. Sommige bijgewerkte terminologie omvat segmenten, virtuele rapportsuites, classificaties, klantenattributen, en containernamen. Vertrouwde concepten zoals eVars en props bestaan niet meer, samen met de beperkingen die ze opleggen.

## Wat niet is gewijzigd

Veel van wat u op de verslaggevende kant kent, is niet veranderd.

* U kunt de kracht van [Analysis Workspace](/help/analysis-workspace/home.md) om uw gegevens te analyseren. De werkruimte werkt hetzelfde als in traditionele Adobe Analytics.
* U hebt ook dezelfde versie van [Adobe Analytics-dashboards](/help/mobile-app/home.md) beschikbaar. Dashboards (ook bekend als Mobile App) werkt hetzelfde als in traditionele Adobe Analytics.
* [Report Builder](/help/report-builder/report-buider-overview.md) heeft een nieuwe interface en loopt nu op PCs, Macs, en de Webversie van Excel.

Wat de rapportage betreft, **wat is anders** is dat u toegang hebt tot veel meer gegevens over meerdere kanalen om te analyseren. Hier is een voorbeeld van een aantal visualisaties die bronnen van dwars-kanaalgegevens omvatten:

![meerkanaalse visualisaties](assets/cross-channel.png)

## Nieuwe architectuur {#architecture}

Customer Journey Analytics krijgt zijn gegevens van Adobe Experience Platform. Met Experience Platform kunt u klantgegevens en inhoud van elk systeem of kanaal centraliseren en standaardiseren. Bovendien kunt u door middel van het leren van gegevens en computers het ontwerp en de levering van persoonlijke ervaringen verbeteren.

De gegevens van de klant in het platform worden opgeslagen als datasets, die uit een schema en partijen gegevens bestaan. Zie voor meer informatie over het platform [Overzicht van Adobe Experience Platform-architectuur](https://experienceleague.adobe.com/docs/platform-learn/tutorials/intro-to-platform/basic-architecture.html?lang=en).

Uw CJA-beheerder heeft [verbindingen](/help/connections/create-connection.md) naar gegevenssets in Platform. Ze hebben toen gebouwd [gegevensweergaven](/help/data-views/data-views.md) binnen die verbindingen. Beschouw gegevensweergaven als vergelijkbaar met virtuele rapportsuites. Gegevensweergaven vormen de basis voor rapportage in Customer Journey Analytics. Het concept van een rapportsuite bestaat niet meer.

## Verbindingen

Een verbinding laat uw Analysebeheerder datasets van integreren [!DNL Adobe Experience Platform] in [!UICONTROL Workspace]. Om verslag uit te brengen over [!DNL Experience Platform] datasets, moet u eerst een verband tussen datasets in vestigen [!DNL Experience Platform] en [!UICONTROL Workspace].

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/35111/?quality=12&learn=on)

## Rapportsuites {#report-suites}

Uw gegevens van de rapportsuite kunnen via de Adobe Analytics Source Connector of de Web SDK in Experience Platform worden gebracht, als uw organisatie zich nog steeds op het Adobe Analytics-platform bevindt en CJA/AEP toevoegt. U zult typisch datasets die rapport-reeks specifiek gebruikend het schema van Analytics zijn.

Verslagen vormen echter niet langer de basis voor rapportage in CJA - [gegevensweergaven](/help/data-views/data-views.md) zijn. Zie de onderstaande sectie voor meer informatie over gegevensweergaven.

Bestaande implementaties van meerdere gegevenssets kunnen in Experience Platform worden gecombineerd. De verbindingen en gegevensmeningen die op deze gegevensreeksen gebaseerd zijn kunnen gegevens combineren die eerder in afzonderlijke rapportreeksen bestonden.

## (Virtueel) rapportsuites zijn nu &#39;gegevensweergaven&#39; {#data-views}

[!UICONTROL Data views] het concept van virtuele - rapportensuites zoals ze vandaag bestaan , uitbreiden tot [extra controles van de gegevens toelaten](/help/data-views/create-dataview.md) beschikbaar gesteld door verbindingen. Dit maakt timezone en zittingsonderbreking uit intervallen configureerbaar. U kunt kenmerken en vervalwaarden ook dynamisch toepassen op afzonderlijke dimensies. Deze worden met terugwerkende kracht toegepast op alle gegevens.

**Wat u moet doen**:

* U ziet dat in Workspace de rapportsuite-kiezer die u nu gebruikt, u de mogelijkheid biedt een keuze te maken uit de gegevensweergaven die uw beheerder met u heeft gedeeld:

   ![data-view-selector](assets/data-views.png)

* U vertrouwd maken met de vele [gebruik gevallen rond gegevensweergaven](/help/data-views/data-views-usecases.md).

## Vars en props

[!UICONTROL eVars], [!UICONTROL props], en [!UICONTROL events] in de traditionele Adobe Analytics-zin niet meer bestaan in [!UICONTROL Customer Journey Analytics]. U hebt onbeperkte schema-elementen (afmetingen, metriek, lijstvelden). Zo worden alle attributie montages u gebruikte om tijdens het proces van de gegevensinzameling toe te passen nu toegepast bij vraagtijd.

**Wat u moet doen**:

* Verken uzelf met de vele manieren deze schemaelementen kunnen worden gebruikt om neer in uw gegevens te boor.

## Segmenten zijn nu &#39;filters&#39;

[!UICONTROL Customer Journey Analytics] gebruikt niet langer eVars, props of gebeurtenissen en gebruikt in plaats daarvan een AEP-schema. Dit betekent dat geen van de bestaande segmenten compatibel is met [!UICONTROL Customer Journey Analytics]. Daarnaast is de naam van &quot;segmenten&quot; gewijzigd in &quot;filters&quot;.

Voorlopig kunt u niet delen/publiceren [!UICONTROL filters] ([!UICONTROL segments]) van [!DNL Customer Journey Analytics] aan Experience Platform verenigde Profiel, of andere toepassingen van de Experience Cloud. Deze functionaliteit wordt momenteel ontwikkeld.

**Wat u moet doen**:

* Als u bestaande Adobe Analytics-segmenten naar Customer Journey Analytics wilt verplaatsen, geeft u de volgende opties weer [deze video](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/moving-adobe-analytics-segments-to-customer-journey-analytics.html?lang=en).
* Anders maakt u de filters opnieuw in Customer Journey Analytics.

## Berekende standaarden

[!UICONTROL Customer Journey Analytics] gebruikt niet langer eVars, props of gebeurtenissen en gebruikt in plaats daarvan een AEP-schema. Dit betekent dat geen van de bestaande berekende meetwaarden compatibel is met [!UICONTROL Customer Journey Analytics].

**Wat u moet doen**:

* Als u berekende maateenheden van Adobe Analytics wilt verplaatsen naar Customer Journey Analytics, kunt u de weergave [deze video](https://experienceleague.adobe.com/docs/customer-journey-analytics-learn/tutorials/moving-your-calculated-metrics-from-adobe-analytics-to-customer-journey-analytics.html?lang=en).
* Anders maakt u de berekende metriek opnieuw in Customer Journey Analytics.

## Instellingen voor sessie en variabelerepersistentie

[!UICONTROL Customer Journey Analytics] past al deze instellingen tijdens het rapport toe en deze instellingen bevinden zich nu in [gegevensweergaven](/help/data-views/component-settings/persistence.md). De wijzigingen in deze instellingen zijn nu retroactief en u kunt meerdere versies gebruiken door meerdere gegevensweergaven te gebruiken.

## Classificaties zijn nu &#39;Gegevensbestanden opzoeken&#39;

De datasets van de opzoekopdracht worden gebruikt om op waarden of sleutels te kijken die in uw gegevens van de Gebeurtenis of van het Profiel worden gevonden. U kunt bijvoorbeeld opzoekgegevens uploaden waarmee numerieke id&#39;s in uw gebeurtenisgegevens worden toegewezen aan productnamen. Zie [dit geval gebruiken](/help/use-cases/b2b.md) bijvoorbeeld.

## Klantkenmerken zijn nu &#39;Profielgegevenssets&#39;

De datasets van het profiel bevatten gegevens die op uw bezoekers, gebruikers, of klanten in worden toegepast [!UICONTROL Event] gegevens. Bijvoorbeeld, staat het u toe om de gegevens van CRM over uw klanten te uploaden. U kunt kiezen welke persoon-id u wilt opnemen. Elke gegevensset die in de [!DNL Experience Platform] heeft een eigen set van een of meer personen-id&#39;s gedefinieerd, zoals Cookie-id, Stitched ID, Gebruikersnaam, Trackingcode, enzovoort.

## Identiteiten

CJA breidt de concepten van identiteiten voorbij ECIDs uit om het even welke identiteitskaart te omvatten u, met inbegrip van Klant identiteitskaart, Cookie identiteitskaart, Titched ID, Gebruiker - identiteitskaart, het Volgen Code, etc. wilt gebruiken. Gebruikend gemeenschappelijke namespace identiteitskaart over datasets, of het gebruiken [Kanaaloverschrijdende analyse](/help/connections/cca/overview.md) de hulp verbindt mensen over verschillende datasets samen. Om het even welke gebruiker die opstelling een project van de Werkruimte in CJA moet IDs begrijpen over de datasets wordt gebruikt.

Hier volgt een video waarin het gebruik van identiteiten in Customer Journey Analytics wordt benadrukt:

>[!VIDEO](https://video.tv.adobe.com/v/30750/?quality=12)

## De naam van containers is gewijzigd

U geeft een container op voor [elke gegevensweergave die u maakt](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=en#containers).

* **Handcontainers zijn nu &#39;Event&#39;-containers**. De [!UICONTROL Person] container bevat elke sessie en gebeurtenis voor bezoekers binnen de opgegeven tijdsperiode.
* **Bezoek containers zijn nu &#39;Sessie&#39;-containers**. De [!UICONTROL Session] Met container kunt u paginainteracties, campagnes of conversies voor een specifieke sessie identificeren.
* **Bezoekerscontainers zijn nu [!UICONTROL Person] containers**. De [!UICONTROL Person] container bevat elke sessie en gebeurtenis voor bezoekers binnen de opgegeven tijdsperiode.

**Wat u moet doen**:

U kunt de naam van elke container aanpassen aan de behoeften van uw organisatie.

## `Uniques Exceeded` beperkingen

[!UICONTROL Customer Journey Analytics] heeft geen unieke waardebeperkingen, dus hoeft u zich daar geen zorgen over te maken!
