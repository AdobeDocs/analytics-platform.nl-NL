---
title: Configuratie met instructies voor inhoudsanalyse
description: Inhoud-analyse configureren met behulp van een configuratie met instructies aan boord
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
exl-id: 4aff664c-3cd9-4591-8122-6ebff10e4a76
source-git-commit: e3f0a7b9958151d678810bbe84740dd4d30b49e5
workflow-type: tm+mt
source-wordcount: '2448'
ht-degree: 0%

---

# Configuratie met instructies voor inhoudsanalyse

{{release-limited-testing}}


De geleide configuratie helpt u om Inhoud Analytics snel en gemakkelijk te vormen. De configuratie met instructies gebruikt een wizard om de vereisten in te stellen voor het automatisch configureren van Content Analytics voor uw organisatie. In het **[!UICONTROL Configuration]** scherm, kunt u of een nieuwe configuratie tot stand brengen of een bestaande configuratie uitgeven.

>[!IMPORTANT]
>
>Per sandbox in uw organisatie kunt u slechts één configuratie voor Content Analytics-gegevens gebruiken.

De Content Analytics-configuratie openen

* Selecteer **[!UICONTROL Data Management]** > **[!UICONTROL Content Analytics Configuration]** in het hoofdmenu in Customer Journey Analytics.

In het **[!UICONTROL Content Analytics Configurations]** -scherm ziet u een tabel met bestaande Content Analytics-configuraties.

![Configuraties voor](../assets/aca-configuration-table.png) Content Analytics
Voor elke configuratie zijn de volgende gegevens beschikbaar:

| Kolom | Beschrijving |
|---|---|
| **[!UICONTROL Name]** | De naam van de configuratie. |
| **[!UICONTROL Created by]** | De technische rekening die de configuratie creeerde. |
| **[!UICONTROL Created on]** | De tijdstempel op het moment dat de configuratie werd gemaakt. |
| **[!UICONTROL Modified on]** | De tijdstempel wanneer de configuratie voor het laatst is gewijzigd. |
| **[!UICONTROL Sandbox]** | De sandbox binnen de organisatie waarin Content Analytics is (gepland) geconfigureerd en geïmplementeerd. |
| **[!UICONTROL Status]** | De status van de configuratie. De status kan zijn:<br/>![ StatusGray ](/help/assets/icons/StatusGray.svg) **[!UICONTROL Draft]**: De configuratie wordt bewaard voor later, en niet opgesteld.<br/>![ StatusRed ](/help/assets/icons/StatusRed.svg) **[!UICONTROL Failed]**: De configuratie heeft ontbroken. U kunt **[!UICONTROL Edit]** selecteren om informatie over de fout op te halen. Adobe pakt mislukte implementaties proactief aan. U kunt contact opnemen met de klantenservice voor meer informatie.<br/>![StatusGreen](/help/assets/icons/StatusGreen.svg) **[!UICONTROL Complete]**: de configuratie is voltooid en met succes geïmplementeerd. |

U kunt ColumnSetting](/help/assets/icons/ColumnSetting.svg) gebruiken ![om de tabel aan te passen. Selecteer welke kolommen u wilt weergeven in het dialoogvenster **[!UICONTROL Customize table]** en selecteer **[!UICONTROL Apply]** om de wijzigingen toe te passen.

Via het scherm Content Analytics **[!UICONTROL Configuration]** kunt u een nieuwe configuratie maken of een bestaande configuratie bewerken.

Een nieuwe configuratie maken:

* Selecteer **[!UICONTROL Create configuration]** . Deze actie opent de [ geleide configuratietovenaar ](#guided-configuration-wizard).

Een bestaande configuratie bewerken:

* Selecteer ![Meer](/help/assets/icons/More.svg) en vervolgens ![Bewerken](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** voor een bestaande Content Analytics-configuratie. Met deze actie wordt de [begeleide configuratiewizard](#guided-configuration-wizard) geopend.

## Begeleide configuratiewizard

De geleide configuratietovenaar bestaat uit vier secties ([ Details ](#details), [ mening van Gegevens ](#data-view), [ Vangst &amp; definitie van de Ervaring ](#experience-capture-and-definition), en [ inzameling van Gegevens ](#data-collection)), elk die u voor details vragen die aan opstelling worden vereist en Content Analytics behoorlijk vormen. Voltooi elke sectie voordat u naar de volgende sectie gaat, omdat sommige instellingen in een sectie afhankelijk kunnen zijn van configuratiewaarden in eerdere secties.

### Details {#onboarding-details}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aca_onboarding_details_button"
>title="Details"
>abstract="Geef een naam op voor de verbinding. In de **[!UICONTROL Data view]** secties , **[!UICONTROL Experience capture and definition]** en **[!UICONTROL Data collection]** secties geeft u meer details om ervoor te zorgen dat Content Analytics correct kan worden geconfigureerd."

>[!CONTEXTUALHELP]
>id="aca_onboarding_details_name_header"
>title="Bijzonderheden"
>abstract="In deze handleiding worden de vereisten vastgesteld die nodig zijn voor het configureren van Content Analytics. Geef een naam op voor deze configuratie"

<!-- markdownlint-enable MD034 -->

Elke configuratie vereist een unieke naam. Bijvoorbeeld, `Example Content Analytics configuration`. De naam wordt vereist om een configuratie te bewaren of uit te voeren.

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
>title="Geselecteerde gegevensweergave opschonen"
>abstract="U hebt een gegevensweergave geselecteerd die al is ingericht voor Content Analytics. Dat de bestaande configuratie van Content Analytics wordt verwijderd en de gegevensmening is provisioned met uw nieuwe configuratie."

>[!CONTEXTUALHELP]
>id="aca_onboarding_dataview_prev_cleanup_labels_dialog"
>title="Vorige gegevensweergave opschonen"
>abstract="U hebt een nieuwe gegevensweergave geselecteerd. De Content Analytics-configuratie voor de vorige geselecteerde gegevensweergave wordt verwijderd."

<!-- markdownlint-enable MD034 -->

Uw configuratie vereist de selectie van de mening van a [ Gegevens ](/help/data-views/data-views.md).

1. Een gegevensweergave selecteren

   * Om een nieuwe gegevensmening voor een configuratie te selecteren, gebruik ![ Gegevens ](/help/assets/icons/Data.svg) **[!UICONTROL Select Data view]**.

     ![ configuratie van Content Analytics van een gegevensmening ](../assets/aca-configuration-dataview.png)

   * Om een gegevensmening voor een configuratie te wijzigen, uitgezocht ![ geef ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** uit.

     ![ configuratie van Content Analytics van een gegevensmening ](../assets/aca-configuration-dataview-edit.png)


   In beide scenario&#39;s ziet u een dialoogvenster **[!UICONTROL Data view]** waarin u een gegevensweergave voor uw configuratie kunt selecteren.

   ![ configuratie van Content Analytics van een gegevensmening - de lijst van gegevensmeningen ](../assets/aca-configuration-dataview-dialog.png)

   Voor een nieuwe configuratie, toont de lijst slechts gegevensmeningen die met zandbakken worden geassocieerd die geen actieve configuratie hebben. Bovendien ziet u alleen gegevensweergaven die zijn gekoppeld aan sandboxen waartoe u toegang hebt en verbindingen die u kunt wijzigen.

   Als u een bestaande configuratie bewerkt, worden in de lijst alleen gegevensweergaven weergegeven die beschikbaar zijn in de sandbox die al is gekoppeld aan de bestaande configuratie.

   U kunt de volgende handelingen uitvoeren:

   * Om naar een specifieke gegevensmening te zoeken, gebruik het ![ 1} gebied van het Onderzoek {.](/help/assets/icons/Search.svg)
   * Om de lijst van beschikbare gegevensmeningen te filtreren, selecteer ![ tonen filters ](/help/assets/icons/Filter.svg). U kunt de lijst filteren op [!UICONTROL Connection] , [!UICONTROL Owner] en [!UICONTROL Sandbox] .<br/>Gebruik ![Verbergen](/help/assets/icons/Filter.svg) **[!UICONTROL Hide filters]** om het filtervenster te verbergen.
   * Als u wilt definiëren welke kolommen in de tabel moeten worden weergegeven, selecteert u ![Kolominstellingen](/help/assets/icons/ColumnSetting.svg). Selecteer welke kolommen u in het **[!UICONTROL Customize table]** dialoogvenster wilt weergeven en selecteer **[!UICONTROL Apply]** om de wijzigingen toe te passen.

1. Selecteer ![ SelectBox ](/help/assets/icons/SelectBox.svg) de gegevensmening die u wilt gebruiken.
1. Selecteer **[!UICONTROL Save]** om de geselecteerde gegevensweergave te bevestigen. Selecteer **[!UICONTROL Cancel]** om te annuleren.


In Customer Journey Analytics, is de a [ gegevensmening ](/help/data-views/data-views.md) gebonden aan een verbinding van Customer Journey Analytics [ ](/help/connections/overview.md). En een verbinding is gebaseerd op een zandbak binnen uw organisatie. Nadat u de configuratie hebt opgeslagen, wordt **[!UICONTROL Sandbox]** automatisch gevuld met de naam van de sandbox op basis van de geselecteerde gegevensweergave.


### Vastleggen en definiëren van ervaring {#onboarding-experiences}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aca_onboarding_experiences_button"
>title="Vastleggen en definiëren van ervaring"
>abstract="U kunt ervoor kiezen ervaringen op te nemen in de gegevens die u met Content Analytics verzamelt. Wanneer geselecteerd, moet u één of meerdere combinaties regex en vraagparameters bepalen om te bepalen waarvoor URLs u ervaringen wilt omvatten."

>[!CONTEXTUALHELP]
>id="aca_onboarding_experiences_header"
>title="Ervaar vastleggen en definiëren"
>abstract="Ervaringen verzamelen in Content Analytics"

>[!CONTEXTUALHELP]
>id="aca_onboarding_experiences_parameters_header"
>title="Ervaar vastleggen en definiëren"
>abstract="Geef de parameters op die bepalen hoe inhoud op uw website wordt weergegeven."

>[!CONTEXTUALHELP]
>id="aca_onboarding_experiencecapture_new_include_experiences"
>title="Vastleggen en definiëren van ervaring"
>abstract="Indien ingeschakeld, worden ervaringsgegevens verzameld, worden ervaringskenmerken gegenereerd en is ervaringsrapportage beschikbaar."

>[!CONTEXTUALHELP]
>id="aca_onboarding_experiencecapture_edit_include_experiences"
>title="Vastleggen en definiëren van ervaring"
>abstract="Indien ingeschakeld, worden ervaringsgegevens verzameld, worden ervaringskenmerken gegenereerd en is ervaringsrapportage beschikbaar. ![ het gebruik <br><br/> geeft ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** uit om de configuratie van de gegevensinzameling voor ervaringen in het bezit van Markeringen te wijzigen dat met de huidige configuratie wordt geassocieerd."

>[!CONTEXTUALHELP]
>id="aca_onboarding_experiencecapture_edit_button"
>title="Ervaar vastleggen en definiëren"
>abstract="U moet de instellingen voor het verzamelen van ervaringsgegevens bewerken in de Adobe Content Analytics-extensie in de eigenschap Tags die is gekoppeld aan de huidige configuratie."

<!-- markdownlint-enable MD034 -->

In deze sectie kunt u ervoor kiezen ervaringen op te nemen in de gegevens die u met Content Analytics verzamelt.  Een ervaring is alle tekst op een webpagina die reproduceerbaar is met behulp van de URL die wordt gebruikt door de eerste gebruiker die die webpagina bezoekt.

Standaard is **[!UICONTROL Include experiences]** uitgeschakeld. Als deze optie is geselecteerd, moet u definiëren voor welke URL&#39;s u ervaringen wilt opnemen.

Overweeg alleen om ervaringen op te nemen als het volgende van toepassing is:

* De pagina&#39;s op de site moeten reproduceerbaar zijn met behulp van de pagina-URL.
* De tekstinhoud die door een bepaalde gebruiker wordt gezien, kan met de pagina-URL worden gereproduceerd en is niet afhankelijk van cookies of andere verpersoonlijkingsmechanismen.

Ervaringen opnemen in een nieuwe of niet geïmplementeerde configuratie:

![ de configuratieervaring van de Analyse van de Inhoud vangen en definitie ](../assets/aca-configuration-experience.png)

1. Schakel **[!UICONTROL Include experiences]** in. De knevel om ervaringen toe te laten beïnvloedt het volgende:

   * Gegevensverzameling in de Content Analytics-extensie
   * Het proces dat ervaringskenmerken genereert op basis van gebeurtenisgegevens van Content Analytics
   * De rapportagesjabloon in Customer Journey Analytics.

1. Specificeer de parameters voor de manier waarop inhoud op uw website wordt weergegeven. De parameters zijn nul of meer combinaties van a **[!UICONTROL Domain regular expression]** en **[!UICONTROL Query parameters]**. De queryparameters geven aan welke parameters van invloed zijn op de inhoud van uw pagina. Met deze invoer kan Content Analytics parameters negeren die geen invloed hebben op de inhoud van de pagina wanneer een unieke ervaring wordt gedefinieerd.
   1. Voer een **[!UICONTROL Domain regular expression]** in, bijvoorbeeld `/^(?!.*\b(store|help|admin)\b)/` . Gebruik `/` om normale expressies te omzeilen. De reguliere expressie van het domein geeft aan op welke URL&#39;s deze parameters van toepassing zijn. U kunt bijvoorbeeld meerdere sites hebben en voor elke site wordt de inhoud door verschillende parameters aangedreven. Als de queryparameters op al uw pagina&#39;s van toepassing zijn, kunt u met `.*` alle pagina&#39;s aangeven.
   1. Geef een door komma&#39;s gescheiden lijst op van **[!UICONTROL Query parameters,]** bijvoorbeeld `outdoors, patio, kitchen` .
1. Selecteer **[!UICONTROL Remove]** als u een combinatie van de reguliere expressie van het domein en queryparameters wilt verwijderen.
1. Selecteer **[!UICONTROL Add Regex]** als u een andere combinatie van een reguliere expressie en queryparameters wilt toevoegen.

Bestaande bewerkingen bewerken of nieuwe ervaringen opnemen in een geïmplementeerde configuratie:

![ de configuratievenis van Content Analytics vangen en definitie ](../assets/aca-configuration-experience-edit.png)

* Schakel **[!UICONTROL Include experiences]** in of uit om:

   * Het proces dat ervaringskenmerken genereert van Content Analytics-gebeurtenisgegevens
   * De rapportagesjabloon in Customer Journey Analytics.

* Selecteer ![ uitgeven ](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** om de configuratie van gegevensinzameling voor ervaringen in Content Analytics verder uit te geven. U wordt opnieuw gericht aan de [ uitbreiding van Adobe Content Analytics ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-event-filtering) in het bezit van Markeringen dat met de huidige configuratie wordt geassocieerd.


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
>abstract="Geef aan welke items moeten worden **opgenomen** of **uitgesloten** bij het verzamelen van gegevens voor Content Analytics"

>[!CONTEXTUALHELP]
>id="aca_onboarding_datacollection_experiences_edit_button"
>title="Dataverzameling"
>abstract="U kunt de instellingen voor pagina&#39;s in de Adobe Content Analytics-extensie bewerken in de eigenschap Codes die is gekoppeld aan de huidige configuratie."

>[!CONTEXTUALHELP]
>id="aca_onboarding_datacollection_assets_edit_button"
>title="Dataverzameling"
>abstract="U kunt de instellingen voor elementen in de Adobe Content Analytics-extensie bewerken in de eigenschap Codes die is gekoppeld aan de huidige configuratie."

>[!CONTEXTUALHELP]
>id="aca_onboarding_datacollection_tags_disabled_description "
>title="Tags, eigenschap uitgeschakeld"
>abstract="Content Analytics-extensie is al actief."

<!-- markdownlint-enable MD034 -->

#### Nieuwe configuratie {#new-configuration}

In een nieuwe configuratie moet u definiëren of u een bestaande eigenschap Codes wilt gebruiken of een nieuwe eigenschap Codes wilt maken. En u moet de pagina&#39;s en items definiëren die u wilt opnemen of uitsluiten, met behulp van reguliere expressies.

* Een bestaande eigenschap Tags gebruiken:

  ![Content Analytics-gegevensverzameling Bestaande tag](../assets/aca-configuration-datacollection-existingtag.png)

   1. Selecteer **[!UICONTROL Choose existing]** .
   2. Selecteer een bestaande eigenschap in het vervolgkeuzemenu **[!UICONTROL Tags property]** . U kunt beginnen te typen om naar de beschikbare opties te zoeken en te beperken. U kunt geen eigenschap Codes selecteren die al wordt gebruikt door een andere geïmplementeerde Content Analytics-configuratie.


* Een nieuwe eigenschap voor tags maken:

  ![ de Nieuwe Markering van de Inzameling van Gegevens van Content Analytics ](../assets/aca-configuration-datacollection-newtag.png)

   1. Selecteer **[!UICONTROL Create new]** .
   1. Geef een **[!UICONTROL Tags name]** op, bijvoorbeeld `ACA Test for Documentation` .
   1. Geef **[!UICONTROL Domains]** op, bijvoorbeeld `example.com` .

* Geef aan welke pagina&#39;s moeten worden opgenomen of uitgesloten bij het verzamelen van gegevens voor Content Analytics.

  Geef een reguliere-expressiereeks op voor **[!UICONTROL Pages to include / exclude]** . <br/> Bijvoorbeeld: `^(?!.*documentation).*` om alle documentatiepagina&#39;s van Content Analytics uit te sluiten.

* Geef aan welke elementen moeten worden opgenomen of uitgesloten bij het verzamelen van gegevens voor Content Analytics.

  Geef een tekenreeks voor reguliere expressies op voor **[!UICONTROL Assets to include / exclude]**. <br/> Bijvoorbeeld: `^(?!.*(logo\.jpg|\.svg)).*$` om alle embleem JPEG en beelden van SVG van Content Analytics uit te sluiten.

>[!IMPORTANT]
>
>In het geval dat u een bestaande implementatie van SDK van het Web hebt die de [ bibliotheek Javascript ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/install/library) gebruikt, en niet de [ uitbreiding van Markeringen ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) gebruikt, moet u de automatische inbegrepen uitbreiding van SDK van het Web van het pas gecreëerde bezit van Markeringen manueel verwijderen.



#### Bestaande configuratie {#existing-configuration}

Voor een bestaande configuratie kunt u de eigenschap Codes niet bewerken. U kunt de pagina&#39;s en elementen echter wel bewerken om deze in of uit te sluiten.

* Als u wilt bewerken welke pagina&#39;s moeten worden opgenomen of uitgesloten bij het verzamelen van gegevens voor Content Analytics, selecteert u ![Bewerken](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** onder **[!UICONTROL Experience]**. U wordt omgeleid naar de [Adobe Content Analytics-extensie](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-event-filtering) die is gekoppeld aan de eigenschap Tags voor de huidige Content Analytics-configuratie. U kunt de reguliere expressie bewerken om pagina&#39;s op te nemen of uit te sluiten. Zorg ervoor dat u [uw wijzigingen publiceert](#publish) .

* Als u wilt bewerken welke items moeten worden opgenomen of uitgesloten bij het verzamelen van gegevens voor Content Analytics, selecteert u ![Bewerken](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** onder **[!UICONTROL Asset]**. U wordt omgeleid naar de [Adobe Content Analytics-extensie](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview#configure-event-filtering) die is gekoppeld aan de eigenschap Tags voor de huidige Content Analytics-configuratie. U kunt de reguliere expressie bewerken om elementen op te nemen of uit te sluiten. Zorg ervoor dat u [uw wijzigingen publiceert](#publish) .

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

Wanneer u een configuratie maakt of bewerkt, hebt u de volgende opties:

* **[!UICONTROL Discard]**: alle wijzigingen die als onderdeel van de configuratie zijn aangebracht, worden genegeerd.
* **[!UICONTROL Save for later]**: in een configuratie aangebrachte wijzigingen worden opgeslagen. U kunt de configuratie in een later stadium herzien om verdere veranderingen aan te brengen, of de configuratie uit te voeren. Alleen een waarde voor [!UICONTROL Name] is vereist om een configuratie op te slaan.
* **[!UICONTROL Implement]**: instellingen voor of wijzigingen die in een configuratie zijn aangebracht, worden opgeslagen en geïmplementeerd. Alle gebieden die als ![ worden gemerkt Vereiste ](/help/assets/icons/Required.svg) vereiste waarden moeten hebben. De uitvoering bestaat uit:

   * **[!UICONTROL Customer Journey Analytics]** configuratie:
      * De geselecteerde gegevensweergave wordt bijgewerkt en bevat nu de Content Analytics-dimensie en metriek.
      * De verbinding die aan de geselecteerde gegevensmening wordt gebonden wordt gewijzigd om de gebeurtenissen van Content Analytics en attributen datasets te omvatten.
      * Er wordt een rapportsjabloon voor Content Analytics toegevoegd aan Workspace.


   * **[!UICONTROL Adobe Experience Platform]** configuratie:
      * Het maken van schema&#39;s om gebeurtenissen voor Content Analytics, elementkenmerken en (indien geconfigureerd) ervaringskenmerken te modelleren.
      * Het creëren van datasets om de gebeurtenissen van de Analytics van de Inhoud, activa attributen en (indien gevormd) ervaringsattributen te verzamelen.
      * Het creëren van een gegevensstroom die de featurization dienst gebruikt om inhoudsattributen van de gebeurtenissen van de Analyse van de Inhoud te produceren en bij te werken.


   * **[!UICONTROL Data collection]** configuratie:
      * De nieuwe of bestaande eigenschap Tags is geconfigureerd ter ondersteuning van het verzamelen van Content Analytics-gegevens. Deze configuratie houdt in dat de extensie Adobe Content Analytics voor tags wordt opgenomen.
      * Er wordt een gegevensstroom gemaakt voor gebeurtenissen van Content Analytics.
      * De extensie Adobe Content Analytics is geconfigureerd om ervoor te zorgen dat gebeurtenissen Content Analytics naar de gegevensstroom worden verzonden voor Content Analytics.
      * Als het Web SDK niet voor het bezit van Markeringen wordt gevormd, wordt een nieuwe configuratie van SDK van het Web gecreeerd om slechts de gebeurtenissen van de Analyse van de Inhoud te verzenden.
      * Als het Web SDK voor dit bezit van Markeringen wordt gevormd, worden geen veranderingen aangebracht in de bestaande configuratie van SDK van het Web.


* **[!UICONTROL Save]**: wijzigingen die in een geïmplementeerde configuratie zijn aangebracht, worden opgeslagen en de implementatie wordt bijgewerkt.
* **[!UICONTROL Exit]**. Sluit de configuratie met instructies af. Alle wijzigingen die in een geïmplementeerde configuratie zijn aangebracht, worden genegeerd.


## Publiceren {#publish}

Om gegevens voor uw configuratie van Content Analytics te beginnen verzamelen, moet u [ manueel ](manual.md) publiceren het bezit van Markeringen dat wordt gecreeerd nadat u **[!UICONTROL Implement]** selecteerde.


>[!MORELIKETHIS]
>
>[ Handmatige configuratie ](manual.md)
>
