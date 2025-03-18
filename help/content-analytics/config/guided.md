---
title: Configuratie met instructies voor inhoudsanalyse
description: Inhoud-analyse configureren met behulp van een configuratie met instructies aan boord
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
hide: true
hidefromtoc: true
exl-id: 4aff664c-3cd9-4591-8122-6ebff10e4a76
source-git-commit: 5eb9136107ed872639b02df2549a2f81dee83e76
workflow-type: tm+mt
source-wordcount: '3192'
ht-degree: 1%

---

# Configuratie met instructies voor inhoudsanalyse

>[!WARNING]
>
>Dit artikel is een voorlopige niet-officiële ontwerpversie van een toekomstige definitieve versie en maakt deel uit van de documentatie van Content Analytics. Alle inhoud kan worden gewijzigd en er kunnen geen wettelijke verplichtingen uit de huidige versie van dit artikel worden afgeleid.
>

{{release-limited-testing}}

De geleide configuratie helpt u om Inhoud Analytics snel en gemakkelijk te vormen. De configuratie met instructies gebruikt een wizard om de vereisten in te stellen voor het automatisch configureren van Content Analytics voor uw organisatie. In het **[!UICONTROL Configuration]** scherm, kunt u of een nieuwe configuratie tot stand brengen of een bestaande configuratie uitgeven.

>[!IMPORTANT]
>
>Per sandbox in uw organisatie kunt u slechts één configuratie voor Content Analytics-gegevens gebruiken.


De Content Analytics-configuratie openen

* Selecteer **[!UICONTROL Data Management]** > **[!UICONTROL Content Analytics]** in het hoofdmenu in Customer Journey Analytics.

In het scherm van de Configuratie van de Analyse van de Inhoud, ziet u een lijst van bestaande configuraties van de Analytics van de Inhoud.

{de configuraties van de Analytics van 0} Inhoud ](../assets/aca-configuration-table.png)
Voor elke configuratie zijn de volgende details beschikbaar:![

| Kolom | Beschrijving |
|---|---|
| **[!UICONTROL Name]** | De naam van de configuratie. |
| **[!UICONTROL Created by]** | De technische rekening die de configuratie creeerde. |
| **[!UICONTROL Created on]** | De tijdstempel op het moment dat de configuratie werd gemaakt. |
| **[!UICONTROL Modified on]** | De tijdstempel wanneer de configuratie voor het laatst is gewijzigd. |
| **[!UICONTROL Sandbox]** | De sandbox binnen de organisatie waarin Content Analytics is (gepland) geconfigureerd en geïmplementeerd. |
| **[!UICONTROL Status]** | De status van de configuratie. De status kan zijn:<br/>![ StatusGray ](/help/assets/icons/StatusGray.svg) **[!UICONTROL Draft]**: De configuratie wordt bewaard voor later, en niet opgesteld.<br/>![ StatusRed ](/help/assets/icons/StatusRed.svg) **[!UICONTROL Failed]**: De configuratie heeft ontbroken. U moet de configuratie bewerken en de benodigde wijzigingen aanbrengen.<br/>![ StatusGreen ](/help/assets/icons/StatusGreen.svg) **[!UICONTROL Complete]**: de configuratie is voltooid en met succes uitgevoerd. |

U kunt ![ gebruiken ColumnSetting ](/help/assets/icons/ColumnSetting.svg) om de lijst aan te passen. Selecteer welke kolommen u wilt weergeven in het dialoogvenster **[!UICONTROL Customize table]** en selecteer **[!UICONTROL Apply]** om de wijzigingen toe te passen.

Via het scherm Content Analytics **[!UICONTROL Configuration]** kunt u een nieuwe configuratie maken of een bestaande configuratie bewerken.

Een nieuwe configuratie maken:

* Selecteer **[!UICONTROL Create configuration]** . Met deze handeling opent u de wizard voor configuratie met instructies.

Een bestaande configuratie bewerken:

* Selecteer ![ Meer ](/help/assets/icons/More.svg) en dan ![ geef ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** voor een bestaande configuratie van de Analyse van de Inhoud uit. Met deze handeling opent u de wizard voor configuratie met instructies.

## Wizard Begeleide configuratie

De geleide configuratietovenaar bestaat uit vier secties ([ Details ](#details), [ mening van Gegevens ](#data-view), [ Vangst &amp; definitie van de Ervaring ](#experience-capture-and-definition), en [ de inzameling van Gegevens ](#data-collection)), elk die u voor details vragen die aan opstelling behoorlijk worden vereist en Inhoud Analytics vormen. Voltooi elke sectie voordat u naar de volgende sectie gaat, omdat bepaalde instellingen in een sectie mogelijk afhankelijk zijn van configuratiewaarden in eerdere secties.

### Details {#onboarding-details}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aca_onboarding_details_button"
>title="Details"
>abstract="Geef een naam op voor de verbinding. In de secties **[!UICONTROL Data view]** , **[!UICONTROL Experience capture and definition]** en **[!UICONTROL Data collection]** geeft u meer informatie om ervoor te zorgen dat Content Analytics correct kan worden geconfigureerd."

>[!CONTEXTUALHELP]
>id="aca_onboarding_details_name_header"
>title="Details"
>abstract="Deze handleiding stelt de vereisten in die nodig zijn om Content Analytics te configureren. Geef een naam op voor deze configuratie"

<!-- markdownlint-enable MD034 -->

Voor elke configuratie is een unieke naam vereist. Bijvoorbeeld `Example Content Analytics configuration` . De naam wordt vereist om een configuratie te bewaren of uit te voeren.

![ de configuratiedetails van Content Analytics ](../assets/aca-configuration-details.png)


### Gegevens, weergave {#onboarding-data-view}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="ac_onboarding_dataview_button"
>title="Gegevens, weergave"
>abstract="Voor de configuratie van Content Analytics moet u een bestaande gegevensweergave selecteren. U kunt de analysegegevens van de inhoud dus samenvoegen met andere gegevens."

>[!CONTEXTUALHELP]
>id="aca_onboarding_dataview_header"
>title="Gegevens, weergave"
>abstract="Selecteer in Customer Journey Analytics een bestaande gegevensweergave waarin u de analysegegevens voor de inhoud wilt samenvoegen."

>[!CONTEXTUALHELP]
>id="aca_onboarding_dataview_header_alt"
>title="Gegevens, weergave"
>abstract="Selecteer een bestaande gegevensweergave in Customer Journey Analytics waarmee u de analysegegevens van de inhoud wilt samenvoegen.<br/>"

>[!CONTEXTUALHELP]
>id="aca_onboarding_dataview_change_dialog"
>title="Nieuwe gegevensweergave"
>abstract="Als u een nieuwe gegevensweergave selecteert, wordt de gegevensweergave bijgewerkt met de afmetingen en metriek van Content Analytics. Indien nodig, wordt de bijbehorende verbinding ook bijgewerkt om de gegevenssets van Content Analytics op te nemen. De verbinding en de gegevensmening die momenteel voor Inhoud Analytics worden gevormd worden niet gewijzigd."

>[!CONTEXTUALHELP]
>id="aca_onboarding_dataview_current_cleanup_labels_dialog"
>title="Geselecteerde gegevensweergave opruimen"
>abstract="U hebt een gegevensweergave geselecteerd die al is ingericht voor Content Analytics. Dat de bestaande configuratie van Content Analytics wordt verwijderd en de mening van Gegevens is provisioned met uw nieuwe configuratie."

>[!CONTEXTUALHELP]
>id="aca_onboarding_dataview_prev_cleanup_labels_dialog"
>title="Vorige gegevensweergave opschonen"
>abstract="U hebt een nieuwe gegevensweergave geselecteerd. De Content Analytics-configuratie voor de vorige geselecteerde gegevensweergave wordt verwijderd."

<!-- markdownlint-enable MD034 -->

Uw configuratie vereist de selectie van de mening van a [ Gegevens ](/help/data-views/data-views.md).

1. Een gegevensweergave selecteren

   * Om een nieuwe mening van Gegevens voor een configuratie te selecteren, gebruik ![ Gegevens ](/help/assets/icons/Data.svg) **[!UICONTROL Select Data view]**.

     ![ Configuratie van de Analytics van de Inhoud van een mening van Gegevens ](../assets/aca-configuration-dataview.png)

   * Om een mening van Gegevens voor een configuratie te wijzigen, uitgezocht ![ geef ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** uit.

     ![ Configuratie van de Analytics van de Inhoud van een mening van Gegevens ](../assets/aca-configuration-dataview-edit.png)


   In beide scenario&#39;s ziet u een dialoogvenster **[!UICONTROL Data view]** waarin u een gegevensweergave voor uw configuratie kunt selecteren.

   ![ configuratie van Content Analytics van een mening van Gegevens - de lijst van de meningen van Gegevens ](../assets/aca-configuration-dataview-dialog.png)

   Voor een nieuwe configuratie, toont de lijst slechts de meningen van Gegevens die met zandbakken worden geassocieerd die geen actieve configuratie hebben.

   Als u een bestaande configuratie bewerkt, worden in de lijst alleen de gegevensweergaven weergegeven die beschikbaar zijn in de sandbox die al is gekoppeld aan de bestaande configuratie.

   * Om naar een specifieke mening van Gegevens te zoeken, gebruik het ![ 1} gebied van het Onderzoek {.](/help/assets/icons/Search.svg)
   * Om de lijst van beschikbare meningen van Gegevens te filtreren, selecteer ![ tonen filters ](/help/assets/icons/Filter.svg). U kunt de lijst filteren op Verbinding, Eigenaar en Sandbox.![ Verbergen van het gebruik ](/help/assets/icons/Filter.svg) **[!UICONTROL Hide filters]** om de filterruit te verbergen.<br/>
   * Om te bepalen welke kolommen in de lijst te tonen, selecteer ![ Montages van de Kolom ](/help/assets/icons/ColumnSetting.svg). Selecteer welke kolommen u wilt weergeven in het dialoogvenster **[!UICONTROL Customize table]** en selecteer **[!UICONTROL Apply]** om de wijzigingen toe te passen.

1. Selecteer **[!UICONTROL Save]** om de geselecteerde gegevensweergave te bevestigen. Selecteer **[!UICONTROL Cancel]** om te annuleren.


Een mening van Gegevens is gebonden aan een Verbinding van Customer Journey Analytics [ ](/help/connections/overview.md). En een Verbinding is gebaseerd op een zandbak binnen uw organisatie. Nadat u de configuratie hebt opgeslagen, wordt de eigennaam van de sandbox automatisch ingevuld in **[!UICONTROL Sandbox]** , op basis van de geselecteerde gegevensweergave.


### Vastleggen en definiëren van ervaring {#onboarding-experiences}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aca_onboarding_experiences_button"
>title="Vastleggen en definiëren van ervaring"
>abstract="U kunt Ervaringen opnemen in de gegevens die u verzamelt met Content Analytics. Wanneer geselecteerd, moet u één of meerdere combinaties regex en vraagparameters bepalen om te bepalen waarvoor URLs u ervaringen wilt omvatten."

>[!CONTEXTUALHELP]
>id="aca_onboarding_experiences_header"
>title="Vastleggen en definiëren van ervaring"
>abstract="Ervaringen verzamelen in Content Analytics"

>[!CONTEXTUALHELP]
>id="aca_onboarding_experiences_parameters_header"
>title="Vastleggen en definiëren van ervaring"
>abstract="Geef de parameters op die bepalen hoe inhoud op uw website wordt weergegeven."

>[!CONTEXTUALHELP]
>id="aca_onboarding_experiencecapture_edit_button"
>title="Vastleggen en definiëren van ervaring"
>abstract="U kunt de instellingen in de Adobe Content Analytics-extensie bewerken in de eigenschap Codes die is gekoppeld aan de huidige configuratie."

<!-- markdownlint-enable MD034 -->

In deze sectie kunt u Ervaringen opnemen in de gegevens die u verzamelt met Content Analytics.  Een ervaring is alle tekst op een webpagina die reproduceerbaar is met de URL die wordt gebruikt door de eerste gebruiker die die webpagina bezoekt.

Standaard is **[!UICONTROL Include experiences]** uitgeschakeld. Als deze optie is geselecteerd, moet u definiëren voor welke URL&#39;s u ervaringen wilt opnemen.

Neem alleen ervaringen op als het volgende van toepassing is:

* U kunt de site-inhoud alleen benaderen met openbare URL&#39;s. Voor toegang tot de site zijn geen persoonlijke tokens, cookies of andere mechanismen vereist die niet beschikbaar zijn via de URL.
* De pagina&#39;s op de site moeten reproduceerbaar zijn met de pagina-URL.

Ervaringen opnemen in een nieuwe of niet geïmplementeerde configuratie:

![ de configuratieervaring van de Analyse van de Inhoud vangen en definitie ](../assets/aca-configuration-experience.png)

1. Schakel **[!UICONTROL Include experiences]** in.
1. Optioneel. Geef de parameters op voor de weergave van inhoud op uw website. De parameters zijn nul of meer combinaties van a **[!UICONTROL Domain regular expression]** en **[!UICONTROL Query parameters]**.
   1. Voer een **[!UICONTROL Domain regular expression]** in, bijvoorbeeld `/^(?!.*\b(store|help|admin)\b)/` . Gebruik `/` om normale expressies te omzeilen.
   1. Geef een door komma&#39;s gescheiden lijst op van **[!UICONTROL Query parameters,]** bijvoorbeeld `outdoors, patio, kitchen` .
1. Selecteer **[!UICONTROL Remove]** als u een combinatie van de reguliere expressie van het domein en queryparameters wilt verwijderen.
1. Selecteer **[!UICONTROL Add Regex]** als u een andere combinatie van een reguliere expressie en queryparameters wilt toevoegen.

Bestaande bewerkingen uitvoeren of nieuwe ervaringen opnemen in een geïmplementeerde configuratie:

![ de configuratieervaring van de Analyse van de Inhoud vangen en definitie ](../assets/aca-configuration-experience-edit.png)

* Selecteer ![ uitgeven ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** om de configuratie van het verzamelen van Ervaringen in Content Analytics uit te geven. U wordt opnieuw gericht aan de [ uitbreiding van Adobe Content Analytics ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-event-filtering) in het bezit van Markeringen dat met de huidige configuratie wordt geassocieerd.




### Dataverzameling {#onboarding-data-collection}

In deze sectie configureert u hoe u de gegevens van de inhoudsanalyse kunt verzamelen.

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aca_onboarding_datacollection_button"
>title="Dataverzameling"
>abstract="Definieer welke eigenschap Codes u wilt gebruiken of maak een nieuwe eigenschap. Definieer met behulp van reguliere expressies de pagina&#39;s en elementen die u wilt opnemen of uitsluiten."

>[!CONTEXTUALHELP]
>id="aca_onboarding_datacollection_tag_header"
>title="Dataverzameling"
>abstract="**verstrek een bezit van Markeringen**"

>[!CONTEXTUALHELP]
>id="aca_onboarding_datacollection_pages_excluded_boldheader"
>title="Dataverzameling"
>abstract="**Pagina&#39;s om te omvatten/uit te sluiten**"

>[!CONTEXTUALHELP]
>id="aca_onboarding_datacollection_pages_excluded_header"
>title="Dataverzameling"
>abstract="Wijs op welke pagina&#39;s **** of **uitgesloten** zouden moeten zijn wanneer het verzamelen van gegevens voor Analytics van de Inhoud"

>[!CONTEXTUALHELP]
>id="aca_onboarding_datacollection_assets_excluded_boldheader"
>title="Dataverzameling"
>abstract="**Assets om te omvatten/uit te sluiten**"

>[!CONTEXTUALHELP]
>id="aca_onboarding_datacollection_assets_excluded_header"
>title="Dataverzameling"
>abstract="Wijs op welke activa **** of **uitgesloten** zouden moeten zijn wanneer het verzamelen van gegevens voor Analytics van de Inhoud"

>[!CONTEXTUALHELP]
>id="aca_onboarding_datacollection_experiences_edit_button"
>title="Dataverzameling"
>abstract="U kunt de instellingen voor pagina&#39;s in de Adobe Content Analytics-extensie bewerken in de eigenschap Codes die is gekoppeld aan de huidige configuratie."

>[!CONTEXTUALHELP]
>id="aca_onboarding_datacollection_assets_edit_button"
>title="Dataverzameling"
>abstract="U kunt de instellingen voor elementen in de Adobe Content Analytics-extensie bewerken in de eigenschap Codes die is gekoppeld aan de huidige configuratie."

<!-- markdownlint-enable MD034 -->

#### Nieuwe configuratie {#new-configuration}

In een nieuwe configuratie moet u definiëren of u een bestaande eigenschap Codes wilt gebruiken of een nieuwe eigenschap Codes wilt maken. En u moet de pagina&#39;s en de activa bepalen u wilt omvatten of uitsluiten, gebruikend regelmatige uitdrukkingen.

* Een bestaande eigenschap Codes gebruiken:

  ![ Inhoud analyseert de Verzameling van Gegevens de Bestaande Markering ](../assets/aca-configuration-datacollection-existingtag.png)

   1. Selecteer **[!UICONTROL Existing]** .
   2. Selecteer een bestaande eigenschap in het vervolgkeuzemenu **[!UICONTROL Tags property]** . U kunt beginnen te typen om naar de beschikbare opties te zoeken en te beperken.

* Een nieuwe eigenschap voor tags maken:

  ![ de Nieuwe Markering van de Inzameling van Gegevens van Content Analytics ](../assets/aca-configuration-datacollection-newtag.png)

   1. Selecteer **[!UICONTROL Create new]** .
   2. Geef een **[!UICONTROL Tags name]** op, bijvoorbeeld `ACA Test` .
   3. Geef **[!UICONTROL Domains]** op, bijvoorbeeld `example.com` .

* Als u ervoor hebt gekozen om ervaringen op te nemen, geeft u aan welke pagina&#39;s moeten worden opgenomen of uitgesloten bij het verzamelen van gegevens voor Content Analytics.

   * Geef een reguliere expressie op voor **[!UICONTROL Experience]** . Bijvoorbeeld: `/^(?!.*documentation).*/` om alle documentatiepagina&#39;s van Content Analytics uit te sluiten. Gebruik `/` om normale expressies te omzeilen.

* Geef aan welke elementen moeten worden opgenomen of uitgesloten bij het verzamelen van gegevens voor Content Analytics.

   * Geef een reguliere expressie op voor **[!UICONTROL Asset]** . Bijvoorbeeld: `/^(?!.*(logo\.jpg|\.svg)).*$/` als u alle logo-JPEG- en SVG-afbeeldingen van Content Analytics wilt uitsluiten. Gebruik `/` om normale expressies te omzeilen.


#### Bestaande configuratie {#existing-configuration}

Voor een bestaande configuratie kunt u de eigenschap Codes niet bewerken. U kunt de pagina&#39;s en elementen echter wel bewerken om deze in of uit te sluiten.

* Om uit te geven welke pagina&#39;s zouden moeten worden omvat of worden uitgesloten wanneer het verzamelen van gegevens voor Analytics van de Inhoud, uitgezocht ![ ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** onderaan **[!UICONTROL Experience]** uitgeven. U wordt opnieuw gericht aan de [ uitbreiding van Adobe Content Analytics ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-event-filtering) die met het bezit van Markeringen voor de huidige configuratie van Content Analytics wordt geassocieerd. U kunt de reguliere expressie bewerken om pagina&#39;s op te nemen of uit te sluiten. Verzeker u [ publiceert ](manual.md#publish) u verandert.

* Om uit te geven welke activa zouden moeten worden omvat of worden uitgesloten wanneer het verzamelen van gegevens voor Analytics van de Inhoud, uitgezocht ![ ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** onderaan **[!UICONTROL Asset]** uitgeven. U wordt opnieuw gericht aan de [ uitbreiding van Adobe Content Analytics ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-event-filtering) die met het bezit van Markeringen voor de huidige configuratie van Content Analytics wordt geassocieerd. U kunt de reguliere expressie bewerken om elementen op te nemen of uit te sluiten. Verzeker u [ publiceert ](manual.md#publish) uw veranderingen.

### Samenvatting {#summary}

Zodra u alle noodzakelijke details hebt verstrekt, verstrekt een samenvatting details over de artefacten die worden gecreeerd of gewijzigd.

* U ziet a **[!UICONTROL You're almost ready to implement _configuratienaam _voor de Samenvatting van de Analyse van de Inhoud]**wanneer u een nieuwe configuratie uitvoert.

* Voor bestaande uitgevoerde configuraties, ziet u de naam van de a **[!UICONTROL You have implemented _configuratie _voor de Samenvatting van de Analyse van de Inhoud]**.

![ Samenvatting van de Configuratie van de Analytics van de Inhoud ](../assets/aca-configuration-summary.png)

### Handelingen {#actions}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aca_onboarding_implementation_warning_dialog"
>title="Bevestiging van uitvoering"
>abstract="Als u **[!UICONTROL Implement]** selecteert, configureert u Inhoud analyseren op basis van de invoer die u in deze workflow hebt opgegeven. Verschillende instellingen worden standaard gekozen op basis van wat doorgaans nuttig is voor Content Analytics, maar u (als de voor de verwerking verantwoordelijke) moet de instellingen van elk artefact controleren om te bevestigen dat de instellingen zijn geïmplementeerd in overeenstemming met uw privacybeleid, contractuele rechten en verplichtingen en toestemmingsvereisten krachtens het toepasselijke recht.<br/><br/> Merk op dat geen gegevens zullen worden verzameld tot de bibliotheek van Markeringen verbonden aan deze configuratie manueel wordt gepubliceerd.<br/><br/> om attributen van beelden en tekst af te leiden, wint Adobe de attributen terug gebruikend:<ol><li>De URL, die wordt vastgelegd tijdens het bezoek van de site van de gebruiker, volgens de instellingen voor gegevensverzameling die u hebt geconfigureerd, en</li><li>De URL waar de afbeelding wordt gehost.</li></ol>U mag geen tags toewijzen aan afbeeldingen die worden gehost op sites van derden."

<!-- markdownlint-enable MD034 -->

Wanneer u een configuratie hebt gemaakt of bewerkt, zijn de volgende acties beschikbaar.

* **[!UICONTROL Discard]**: alle wijzigingen die zijn aangebracht als onderdeel van het maken van een nieuwe configuratie of het bewerken van een bestaande configuratie, worden genegeerd.
* **[!UICONTROL Save for later]**: Wijzigingen die in een nieuwe configuratie of een bestaande, nog niet geïmplementeerde configuratie zijn aangebracht, worden opgeslagen. U kunt de configuratie in een later stadium herzien om verdere veranderingen aan te brengen, of de configuratie uit te voeren.
* **[!UICONTROL Implement]**: instellingen voor of wijzigingen die zijn aangebracht in een nieuwe configuratie of een bestaande, nog niet geïmplementeerde configuratie, worden opgeslagen en geïmplementeerd. De uitvoering bestaat uit:
   * **[!UICONTROL Adobe Experience Platform]** configuratie:
      * Het maken van schema&#39;s om gebeurtenissen voor Content Analytics, elementkenmerken en (indien geconfigureerd) ervaringskenmerken te modelleren.
      * Het creëren van datasets om de gebeurtenissen van de Analytics van de Inhoud, activa attributen en (indien gevormd) ervaringsattributen te verzamelen.
      * Het creëren van een gegevensstroom die de featurization dienst gebruikt om inhoudsattributen van de gebeurtenissen van de Analyse van de Inhoud te produceren en bij te werken.
   * **[!UICONTROL Data collection]** configuratie:
      * Het nieuwe of bestaande bezit van Markeringen wordt gevormd om de gegevensinzameling van Content Analytics te steunen. Deze configuratie houdt in dat de extensie Adobe Content Analytics voor tags wordt opgenomen.
      * Er wordt een gegevensstroom gemaakt voor gebeurtenissen van Content Analytics.
      * De extensie Adobe Content Analytics is geconfigureerd om ervoor te zorgen dat gebeurtenissen Content Analytics naar de gegevensstroom worden verzonden voor Content Analytics.
      * Als het Web SDK niet voor het bezit van Markeringen wordt gevormd, wordt een nieuwe configuratie van SDK van het Web gecreeerd om slechts de gebeurtenissen van de Analyse van de Inhoud te verzenden.
      * Als het Web SDK voor dit bezit van Markeringen wordt gevormd, worden geen veranderingen aangebracht in de bestaande configuratie van SDK van het Web.
   * **[!UICONTROL Customer Journey Analytics]** configuratie:
      * De geselecteerde gegevensweergave wordt bijgewerkt met de dimensie Content Analytics en metriek.
      * De verbinding die aan de geselecteerde mening van Gegevens wordt gebonden wordt gewijzigd om de gebeurtenissen van Content Analytics en attributen datasets te omvatten.
      * Er wordt een rapportsjabloon voor Content Analytics toegevoegd aan Workspace.
* **[!UICONTROL Save]**: wijzigingen die in een geïmplementeerde configuratie zijn aangebracht, worden opgeslagen en de implementatie wordt bijgewerkt.
* **[!UICONTROL Exit]**. Sluit de configuratie met instructies af. Alle wijzigingen die in een geïmplementeerde configuratie zijn aangebracht, worden genegeerd.


## Publiceren {#publish}

Om uw configuratie van Content Analytics te activeren, moet u het bezit publiceren van Markeringen dat wordt gecreeerd nadat u **[!UICONTROL Implement]** [ manueel ](manual.md) selecteerde.


## Instellingen en configuraties aan boord

De volgende secties schetsen de montages en de configuraties die op [ Customer Journey Analytics ](#customer-journey-analytics-cja) worden toegepast, [ Experience Platform ](#experience-platform-aep) en [ de Inzameling van Gegevens ](#data-collection-dc) als deel van de implementatie van een configuratie van Content Analytics.

Voor de volgende scenario&#39;s worden nadere gegevens verstrekt:

* **het bezit van Markeringen** bestaat **✓** of bestaat niet **✕**.
* **SDK van het Web** uitbreiding voor het bezit van Markeringen bestaat **✓** of bestaat niet **✕**.
* Adobe **Content Analytics** uitbreiding voor het bezit van de Markering bestaat **✓** of bestaat niet **✕**.

### Customer Journey Analytics {#cja}

<table style="table-layout:fixed">
  <tr>
    <th></th>
    <th colspan="4">Scenario's:</th>
  </tr>
  <tr>
    <th>
      <strong> Plaatsende </strong>
    </th>
    <th>
      <strong> ✓ Tags <br> ✓ Web SDK <br/> ✓ Content Analytics </strong>
    </th>
    <th>
      <strong> ✓ Tags <br> ✓ Web SDK <br/> ✕ Content Analytics </strong>
    </th>
    <th>
      <strong> ✓ Tags <br> ✕ Web SDK <br/> ✕ Content Analytics </strong>
    </th>
    <th>
      <strong> ✕ Tags <br> ✕ Web SDK <br/> ✕ Content Analytics </strong>
    </th>
  </tr>
  <tbody>
    <tr>
      <td>Rapportsjabloon</td>
      <td colspan="4">Een rapportsjabloon is beschikbaar</td>
    </tr>
    <tr>
      <td>Gegevens, weergave</td>
      <td colspan="4">Gewijzigd/Gemaakt voor ACA-afmetingen en -cijfers</td>
    </tr>
    <tr>
      <td>Verbinding</td>
      <td colspan="4">Gewijzigd om ACA-gegevenssets op te nemen (ACA-gebeurtenissen, Asset-kenmerken, Experience Attribute)</td>
    </tr>
  </tbody>
</table>

### Experience Platform {#aep}

<table style="table-layout:fixed">
  <tr>
    <th></th>
    <th colspan="4">Scenario's:</th>
  </tr>
  <tr>
    <th>
      <strong> Plaatsende </strong>
    </th>
    <th>
      <strong> ✓ Tags <br> ✓ Web SDK <br/> ✓ Content Analytics </strong>
    </th>
    <th>
      <strong> ✓ Tags <br> ✓ Web SDK <br/> ✕ Content Analytics </strong>
    </th>
    <th>
      <strong> ✓ Tags <br> ✕ Web SDK <br/> ✕ Content Analytics </strong>
    </th>
    <th>
      <strong> ✕ Tags <br> ✕ Web SDK <br/> ✕ Content Analytics </strong>
    </th>
  </tr>
  <tbody>
    <tr>
      <td colspan="5"><strong><br/>Content Analytics Events-schema</strong></td>
    </tr>
    <tr>
      <td style="margin-left: 160.0px;">Naam</td>
      <td>Content Analytics Events</td>
      <td>Content Analytics Events</td>
      <td>Content Analytics Events</td>
      <td>Content Analytics Events</td>
    </tr>
    <tr>
      <td>Beschrijving</td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
    </tr>
    <tr>
      <td>Profiel ingeschakeld</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Gegevensset Content Analytics Events</strong></td>
    </tr>
    <tr>
      <td>Naam</td>
      <td>Content Analytics Events</td>
      <td>Content Analytics Events</td>
      <td>Content Analytics Events</td>
      <td>Content Analytics Events</td>
    </tr>
    <tr>
      <td>Schema</td>
      <td>Content Analytics-gebeurtenis</td>
      <td>Content Analytics-gebeurtenis</td>
      <td>Content Analytics-gebeurtenis</td>
      <td>Content Analytics-gebeurtenis</td>
    </tr>
    <tr>
      <td>Beschrijving</td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
    </tr>
    <tr>
      <td>Tags</td>
      <td><i>leeg?</i></td>
      <td><i>leeg?</i></td>
      <td><i>leeg?</i></td>
      <td><i>leeg?</i></td>
    </tr>
    <tr>
      <td>Systeemgegevensset</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
    </tr>
    <tr>
      <td>Profiel ingeschakeld</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
    </tr>
    <tr>
      <td>Gegevensbeheer (DULE-labels)</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Content Analytics-schema voor elementkenmerken</strong></td>
    </tr>
    <tr>
      <td>Naam</td>
      <td>Kenmerken Content Analytics-element</td>
      <td>Kenmerken Content Analytics-element</td>
      <td>Kenmerken Content Analytics-element</td>
      <td>Kenmerken Content Analytics-element</td>
    </tr>
    <tr>
      <td>Beschrijving</td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
    </tr>
    <tr>
      <td>Profiel ingeschakeld</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Gegevensset Content Analytics Assets Attributes</strong></td>
    </tr>
    <tr>
      <td>Naam</td>
      <td>Kenmerken Content Analytics-element</td>
      <td>Kenmerken Content Analytics-element</td>
      <td>Kenmerken Content Analytics-element</td>
      <td>Kenmerken Content Analytics-element</td>
    </tr>
    <tr>
      <td>Schema</td>
      <td>Kenmerken Content Analytics-element</td>
      <td>Kenmerken Content Analytics-element</td>
      <td>Kenmerken Content Analytics-element</td>
      <td>Kenmerken Content Analytics-element</td>
    </tr>
    <tr>
      <td>Beschrijving</td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
    </tr>
    <tr>
      <td>Tags</td>
      <td><i>leeg?</i></td>
      <td><i>leeg?</i></td>
      <td><i>leeg?</i></td>
      <td><i>leeg?</i></td>
    </tr>
    <tr>
      <td>Systeemgegevensset</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
    </tr>
    <tr>
      <td>Profiel ingeschakeld</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
    </tr>
    <tr>
      <td>Gegevensbeheer (DULE-labels)</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Schema Content Analytics-ervaringskenmerken</strong></td>
    </tr>
    <tr>
      <td>Naam</td>
      <td>Content Analytics Experience Attributes</td>
      <td>Content Analytics Experience Attributes</td>
      <td>Content Analytics Experience Attributes</td>
      <td>Content Analytics Experience Attributes</td>
    </tr>
    <tr>
      <td>Beschrijving</td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
    </tr>
    <tr>
      <td>Profiel ingeschakeld</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Gegevensset Content Analytics Experience Attributes</strong></td>
    </tr>
    <tr>
      <td>Naam</td>
      <td>Content Analytics Experience Attributes</td>
      <td>Content Analytics Experience Attributes</td>
      <td>Content Analytics Experience Attributes</td>
      <td>Content Analytics Experience Attributes</td>
    </tr>
    <tr>
      <td>Schema</td>
      <td>Content Analytics Experience Attributes</td>
      <td>Content Analytics Experience Attributes</td>
      <td>Content Analytics Experience Attributes</td>
      <td>Content Analytics Experience Attributes</td>
    </tr>
    <tr>
      <td>Beschrijving</td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
      <td><i>vooraf bepaalde tbd</i></td>
    </tr>
    <tr>
      <td>Tags</td>
      <td><i>leeg?</i></td>
      <td><i>leeg?</i></td>
      <td><i>leeg?</i></td>
      <td><i>leeg?</i></td>
    </tr>
    <tr>
      <td>Systeemgegevensset</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
    </tr>
    <tr>
      <td>Profiel ingeschakeld</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
      <td>Nee</td>
    </tr>
    <tr>
      <td>Gegevensbeheer (DULE-labels)</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
      <td>?</td>
    </tr>
  </tbody>
</table>


### Gegevensverzameling {#dc}

<table style="table-layout:fixed">
  <tr>
    <th></th>
    <th colspan="4">Scenario's:</th>
  </tr>
  <tr>
    <th>
      <strong> Plaatsende </strong>
    </th>
    <th>
      <strong> ✓ Tags <br> ✓ Web SDK <br/> ✓ Content Analytics </strong>
    </th>
    <th>
      <strong> ✓ Tags <br> ✓ Web SDK <br/> ✕ Content Analytics </strong>
    </th>
    <th>
      <strong> ✓ Tags <br> ✕ Web SDK <br/> ✕ Content Analytics </strong>
    </th>
    <th>
      <strong> ✕ Tags <br> ✕ Web SDK <br/> ✕ Content Analytics </strong>
    </th>
  </tr>
  <tbody>
    <tr>
      <td colspan="5"><strong><br/>DataStream</strong></td>
    </tr>
    <tr>
      <td>Naam</td>
      <td><i>bestaande waarde</i></td>
      <td>Content Analytics</td>
      <td>Content Analytics</td>
      <td>Content Analytics</td>
    </tr>
    <tr>
      <td>Beschrijving</td>
      <td><i>bestaande waarde</i></td>
      <td><i>vooraf bepaald</i></td>
      <td><i>vooraf bepaald</i></td>
      <td><i>vooraf bepaald</i></td>
    </tr>
    <tr>
      <td>Toewijzingsschema</td>
      <td><i>bestaande waarde</i></td>
      <td><i>vooraf bepaald</i></td>
      <td><i>vooraf bepaald</i></td>
      <td><i>vooraf bepaald</i></td>
    </tr>
    <tr>
      <td>Geolocatie en netwerk opzoeken</td>
      <td><i>bestaande waarden</i></td>
      <td>Alle opties uitgeschakeld</td>
      <td>Alle opties uitgeschakeld</td>
      <td>Alle opties uitgeschakeld</td>
    </tr>
    <tr>
      <td>Apparaat opzoeken</td>
      <td><i>bestaande waarde</i></td>
      <td>Geen apparaatgegevens verzamelen</td>
      <td>Geen apparaatgegevens verzamelen</td>
      <td>Geen apparaatgegevens verzamelen</td>
    </tr>
    <tr>
      <td>IP Obfuscatie</td>
      <td><i>bestaande waarde</i></td>
      <td>Geen</td>
      <td>Geen</td>
      <td>Geen</td>
    </tr>
    <tr>
      <td>Cookie eerste-id</td>
      <td><i>bestaande waarde</i></td>
      <td>Uit</td>
      <td>Uit</td>
      <td>Uit</td>
    </tr>
    <tr>
      <td>Identiteitskaart van derden synchroniseren</td>
      <td><i>bestaande waarde</i></td>
      <td>Uit</td>
      <td>Uit</td>
      <td>Uit</td>
    </tr>
    <tr>
      <td>Toegangstype</td>
      <td><i>bestaande waarde</i></td>
      <td>Gemengd verifiëren</td>
      <td>Gemengd verifiëren</td>
      <td>Gemengd verifiëren</td>
    </tr>
    <tr>
      <td>Media Analytics</td>
      <td><i>bestaande waarde</i></td>
      <td>Uit</td>
      <td>Uit</td>
      <td>Uit</td>
    </tr>
        <tr>
      <td>Boot Detection</td>
      <td><i>bestaande waarde</i></td>
      <td>Uit</td>
      <td>Uit</td>
      <td>Uit</td>
    </tr>
    <tr>
      <td>Toewijzing</td>
      <td><i>bestaande waarde</i></td>
      <td><i>door gebruiker opgegeven</i></td>
      <td><i>door gebruiker opgegeven</i></td>
      <td><i>door gebruiker opgegeven</i></td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/> bezit van Markeringen </strong><br/> een bestaand bezit of nieuw bezit. De naam en het domein worden verstrekt door de gebruiker.</td>
    </tr>
    <tr>
      <td>Naam</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td><i> verstrekte gebruiker </i> (gebrek "Content Analytics")</td>
    </tr>
    <tr>
      <td>Domein</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td ><i>vooraf bepaald</i></td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Tags, bibliotheek</strong></td>
    </tr>
    <tr>
      <td>Naam</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>
        <br/>
      </td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Web SDK-extensie</strong></td>
    </tr>
    <tr>
      <td>Naam</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Content Analytics - Web SDK</td>
      <td>Content Analytics - Web SDK</td>
    </tr>
    <tr>
      <td>IMS Org</td>
      <td><i>automatisch gevuld</i></td>
      <td><i>automatisch gevuld</i></td>
      <td><i>automatisch gevuld</i></td>
      <td><i>automatisch gevuld</i></td>
    </tr>
    <tr>
      <td>Edge-domein</td>
      <td><i>de bestaande waarde <br/> zou een update kunnen vereisen om de implementatie van AppMeasurement aan te passen</i></td>
      <td><i>de bestaande waarde <br/> zou een update kunnen vereisen om de implementatie van AppMeasurement aan te passen</i></td>
      <td>
        <a href="http://edge.adobedc.net"> edge.adobedc.net </a>
      </td>
      <td>
        <a href="http://edge.adobedc.net"> edge.adobedc.net </a>
      </td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Gegevensstromen</strong></td>
    </tr>
    <tr>
      <td>Productie</td>
      <td><i>bestaande die waarde <br/> de opheffing van de Gegevensstroom wordt gebruikt om naar een verschillende gegevensstroom te verzenden</i></td>
      <td><i>bestaande die waarde <br/> de opheffing van de Gegevensstroom wordt gebruikt om naar een verschillende gegevensstroom te verzenden</i></td>
      <td><i> verstrekte gebruiker </i>?</td>
      <td><i> verstrekte gebruiker </i>?</td>
    </tr>
    <tr>
      <td>Staging</td>
      <td><i>bestaande die waarde <br/> de opheffing van de Gegevensstroom wordt gebruikt om naar een verschillende gegevensstroom te verzenden</i></td>
      <td><i>bestaande die waarde <br/> de opheffing van de Gegevensstroom wordt gebruikt om naar een verschillende gegevensstroom te verzenden</i></td>
      <td><i> verstrekte gebruiker </i>?</td>
      <td><i> verstrekte gebruiker </i>?</td>
    </tr>
    <tr>
      <td>Ontwikkeling</td>
      <td><i>bestaande die waarde <br/> de opheffing van de Gegevensstroom wordt gebruikt om naar een verschillende gegevensstroom te verzenden</i></td>
      <td><i>bestaande die waarde <br/> de opheffing van de Gegevensstroom wordt gebruikt om naar een verschillende gegevensstroom te verzenden</i></td>
      <td><i> verstrekte gebruiker </i>?</td>
      <td><i> verstrekte gebruiker </i>?</td>
    </tr>
    <tr>
      <td>Privacy</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>In?</td>
      <td>In?</td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Identiteit</strong></td>
    </tr>
    <tr>
      <td>ECID migreren</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Ingeschakeld</td>
      <td>Ingeschakeld</td>
    </tr>
    <tr>
      <td>Cookies van derden gebruiken</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Ingeschakeld</td>
      <td>Ingeschakeld</td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Personalisatie</strong></td>
    </tr>
    <tr>
      <td>Doel migreren van at.js naar Web SDK</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Uitgeschakeld</td>
      <td>Uitgeschakeld</td>
    </tr>
    <tr>
      <td>Opslag voor personalisatie inschakelen</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Uitgeschakeld</td>
      <td>Uitgeschakeld</td>
    </tr>
    <tr>
      <td>Automatisch klikken op verzameling voor Adobe Journey Optimizer</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Altijd</td>
      <td>Altijd</td>
    </tr>
    <tr>
      <td>Automatisch klikken op verzameling voor Adobe Target</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Nooit</td>
      <td>Nooit</td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Gegevensverzameling</strong></td>
    </tr>
    <tr>
      <td>Klikken op interne koppelingen verzamelen</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Uitgeschakeld</td>
      <td>Uitgeschakeld</td>
    </tr>
    <tr>
      <td>Externe koppelingsklikken verzamelen</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Uitgeschakeld</td>
      <td>Uitgeschakeld</td>
    </tr>
    <tr>
      <td>Klikken op downloadkoppelingen verzamelen</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Uitgeschakeld</td>
      <td>Uitgeschakeld</td>
    </tr>
    <tr>
      <td>Wanneer u gebeurtenisgegevens verzendt, neemt u automatisch</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Alle standaardcontextgegevens</td>
      <td>Alle standaardcontextgegevens</td>
    </tr>
    <tr>
      <td>Streaming media</td>
      <td><i>bestaande waarden</i></td>
      <td><i>bestaande waarden</i></td>
      <td>Lege waarden</td>
      <td>Lege waarden</td>
    </tr>
    <tr>
      <td>DataStream-configuratieoverschrijvingen</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>Identieke gegevensstroomconfiguratie</td>
      <td>Identieke gegevensstroomconfiguratie</td>
    </tr>
    <tr>
      <td>Geavanceerde instellingen - Edge-basispad</td>
      <td><i>bestaande waarde</i></td>
      <td><i>bestaande waarde</i></td>
      <td>ee</td>
      <td>ee</td>
    </tr>
    <tr>
      <td colspan="5"><strong><br/>Content Analytics-extensie</strong></td>
    </tr>
    <tr>
      <td>Gegevensstromen</td>
      <td><i>bestaande waarde</i></td>
      <td><i>vooraf bepaald</i></td>
      <td><i>vooraf bepaald</i></td>
      <td><i>vooraf bepaald</i></td>
    </tr>
    <tr>
      <td>Ervaring vastleggen en definiëren</td>
      <td><i>bestaande waarde</i></td>
      <td><i>door gebruiker opgegeven</i></td>
      <td><i>door gebruiker opgegeven</i></td>
      <td><i>door gebruiker opgegeven</i></td>
    </tr>
    <tr>
      <td>Gebeurtenisfilters</td>
      <td><i>bestaande waarde</i></td>
      <td><i>door gebruiker opgegeven</i></td>
      <td><i>door gebruiker opgegeven</i></td>
      <td><i>door gebruiker opgegeven</i></td>
    </tr>
  </tbody>
</table>

>[!MORELIKETHIS]
>
>[ Handmatige configuratie ](manual.md)
>
