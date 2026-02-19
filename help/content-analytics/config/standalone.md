---
title: Content Analytics configureren (standalone)
description: Stap-voor-stap gids om Adobe Content Analytics als standalone oplossing te vormen. Leer hoe u schema's, gegevenssets, gegevensstreams en rapporten voor uitgebreide inzichten van inhoudsprestaties instelt zonder een volledige Customer Journey Analytics-implementatie.
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
source-git-commit: f95910d3bd6e9f0e7be7bf272e9c363b4a4a5429
workflow-type: tm+mt
source-wordcount: '2447'
ht-degree: 1%

---

# Zelfstandige configuratie

>[!IMPORTANT]
>
>Deze configuratiehandleiding is bedoeld voor klanten die een licentie hebben verkregen voor het zelfstandige Adobe Content Analytics-pakket. In de handleiding wordt ervan uitgegaan dat u Customer Journey Analytics of een andere Experience Platform-toepassing niet hebt gebruikt of van plan bent te gebruiken buiten de mogelijkheden en functies van Content Analytics. Zie [&#x200B; Content Analytics &#x200B;](configuration.md) vormen als u Content Analytics als deel van een bestaande implementatie van Customer Journey Analytics wilt vormen en gebruiken.
>

Content Analytics is in licentie gegeven als een zelfstandig product, maar de configuratie vindt plaats in Experience Platform en Customer Journey Analytics. Deze platforms bieden de infrastructuur voor gegevensverzameling en -analyse die Content Analytics nodig heeft en gebruikt. Deze handleiding bevat alle specifieke instructies die u nodig hebt, zelfs als u nog niet eerder in Experience Platform en Customer Journey Analytics werkt.

Voordat u begint met het instellen van een zelfstandige Content Analytics, moet u:

* Basiskennis hebben van concepten voor webanalyse, vertrouwd zijn met systemen voor tagbeheer en basiskennis van JavaScript.
* Plan 4-6 uur voor de eerste installatie, plus extra tijd om de installatie te testen en te valideren.

## Terminologie

Deze gids gebruikt verscheidene technische termijnen, van Experience Platform en Customer Journey Analytics, die u niet zou kunnen kennen. Hieronder volgt een uitleg van deze termen (met referentiekoppelingen) in de context van Content Analytics:

| Term | Toelichting |
|---|---|
| **Schema** | A [&#x200B; schema &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition) is een reeks regels die de structuur en het formaat van gegevens vertegenwoordigen en bevestigen. Op hoog niveau bieden schema&#39;s een abstracte definitie van een echt object, zoals een gebeurtenis die op een website plaatsvindt, zoals een klik. En geef een overzicht van de gegevens die in elke instantie van dat object moeten worden opgenomen. |
| **Dataset** | A [&#x200B; dataset &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview) is een opslag en beheersconstructie voor een inzameling van gegevens, typisch een lijst, die een schema (kolommen) en gebieden (rijen) bevat. Een dataset is als een gegevensbestandlijst waar elke rij een gebeurtenis van uw website is. |
| **DataStream** | A [&#x200B; datastream &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview) vertegenwoordigt de server-zijconfiguratie die gegevens van uw website aan de correcte dataset in Adobe Experience Platform leidt. Een gegevensstroom fungeert als een gegevenssnelweg die uw site verbindt met uw opslag. |
| **Markeringen** | [&#x200B; de Markeringen &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) in Experience Platform zijn de volgende generatie mogelijkheden van het markeringsbeheer van Adobe. Met labels kunnen klanten eenvoudig analyses, marketing en advertentietags implementeren en beheren die nodig zijn om relevante klantervaringen te stimuleren. In Content Analytics kunt u met het tagbeheersysteem van Adobe code bijhouden code op uw website implementeren zonder dat u elke pagina op dezelfde manier hoeft te bewerken. De functionaliteit Codes is vergelijkbaar met de functionaliteit die u wellicht kent van Google Tag Manager. |
| **Sandbox** | Experience Platform verstrekt [&#x200B; zandbakken &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) die één enkele instantie van Experience Platform in afzonderlijke virtuele milieu&#39;s verdelen helpen digitale ervaringstoepassingen ontwikkelen en evolueren. Content Analytics gebruikt typisch de *zandbak van de Productie*. |
| **Verbinding** | [&#x200B; de Verbindingen &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/overview) bepalen welke datasets van Experience Platform worden opgenomen. Een verbinding bepaalt het verband tussen uw dataset (waar de gegevens in AEP) en Customer Journey Analytics (waar u het analyseert) worden opgeslagen. Via een verbinding worden de verzamelde gegevens beschikbaar gesteld voor rapportage. |
| **Mening van Gegevens** | A [&#x200B; gegevensmening &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-views) is een container die u laat bepalen hoe te om gegevens van een verbinding te interpreteren. In een gegevensweergave worden alle afmetingen en maatstaven opgegeven waarover u kunt rapporteren. Een gegevensmening is als een configuratie die de rijen en kolommen beschikbaar voor u aan gebruik in uw analyse bepaalt. |
| **Analysis Workspace** | [&#x200B; Analysis Workspace &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home) is een belemmering-en-dalings browser interface die u gebruikt om uw rapporten en analyses van Content Analytics te bouwen. |
| **Ervaring** | In Content Analytics, verwijst een [&#x200B; ervaring &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/content-analytics#terminology) naar al tekstinhoud op een Web-pagina die kan worden gevangen en worden geanalyseerd gebaseerd op de pagina URL. |
| **Activa** | In Content Analytics, is een [&#x200B; activa &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/content-analytics#terminology) een individueel en uniek stuk van inhoud, als een beeld. |


## Overzicht van setup

Deze configuratiegidsen u in de opstelling van alle toepassingen die worden vereist om een werkende **standalone** implementatie van Content Analytics te hebben. U kunt de opstelling in drie fasen verdelen, waar elke fase op vorige bouwt:

**Fase 1** - [&#x200B; voorbereidingen uw milieu &#x200B;](#prepare-your-environment). In deze fase, plaatst u gebruikerstoestemmingen en verifieert uw gegevensinfrastructuur. Zonder deze juiste machtigingen en gegevensstructuur kunt u de overige stappen niet voltooien. Het gaat om de volgende stappen:

1. **vorm toegangsbeheer en toestemmingen** om de configuratie en de implementatie van Content Analytics te steunen.
1. **opstelling een schema en dataset** om het model (schema) van de gegevens te bepalen u inzichten van inhoudsanalyses van en wilt verzamelen waar om die gegevens (dataset) te verzamelen.

**Fase 2** - [&#x200B; vorm gegevensinzameling &#x200B;](#configure-data-collection). In deze fase, creeert u de pijpleiding die inhoudsgegevens van uw website vangt. Content Analytics weet dus welke content bezoekers gebruiken voor jouw content.

1. **opstelling een datastream** om te vormen hoe uw verzamelde gegevens aan de dataset worden verpletterd.
1. **Websitetags van het Gebruik** om regels en gegevenselementen tegen de gegevens in uw gegevenslaag op uw website te vormen en ervoor te zorgen dat het gegeven wordt verzonden naar de gevormde datastream.
1. **stelt** aan een testmilieu **op en bevestigt** de gegevensinzameling alvorens u aan een productiemilieu publiceert.

**Fase 3** - [&#x200B; opstelling die &#x200B;](#set-up-reporting) rapporteert. Maak in deze fase de verzamelde gegevens beschikbaar voor analyse in rapporten. Je krijgt dus de inzichten van de inhoudsprestaties die je uit Content Analytics wilt halen.

1. **opstelling een verbinding** aan uw dataset.
1. **opstelling een gegevensmening** om metriek en afmetingen te bepalen.
1. **vorm en voer Content Analytics** uit.
1. **opstelling een project** om uw rapporten en visualisaties van Content Analytics te bouwen.


## Uw omgeving voorbereiden

In deze fase, plaatst u gebruikerstoestemmingen en verifieert uw gegevensinfrastructuur.

### Toegangsbeheer en machtigingen configureren

In deze sectie wordt beschreven welke toegang u nodig hebt voor het product, de productprofielen en welke machtigingen vereist zijn voor het configureren en instellen van een zelfstandige Content Analytics. Hoewel u alleen geïnteresseerd bent in de functionaliteit van Content Analytics, werkt die functionaliteit alleen correct als u toegang en machtigingen hebt voor andere Experience Platform-producten.

#### Toegangsbeheer

Met Toegangsbeheer bepaalt u of u toegang hebt tot een Experience Platform-product.

U hebt een systeembeheerder of een productbeheerder nodig om u als beheerder voor een product of een productprofiel toe te voegen. Een productbeheerder kan u alleen als beheerder voor het beheerde product (profiel) toevoegen. Een systeembeheerder kan productbeheerders aan elk product (profiel) toevoegen.

>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; gebruikers voor een productprofiel &#x200B;](https://video.tv.adobe.com/v/333860/?quality=12&learn=on){target="_blank"} voor een demo video beheren.


>[!ENDSHADEBOX]

Voor zelfstandige Content Analytics moet u een productbeheerder zijn voor de volgende producten en productprofielen:

* Adobe Experience Platform
   * AEP-Default-All-Users (het standaardprofiel voor toegang tot de productiesandbox)

* Adobe Experience Platform-gegevensverzameling
   * Standaardgegevensverzameling, alle toegang

* Adobe Experience Platform Privacy Service

* Customer Journey Analytics (aangepast)
   * Customer Journey Analytics (of een ander standaardprofiel van het product)

U definieert toegang tot productbeheerders via de Admin Console:

1. Toegang [&#x200B; Admin Console &#x200B;](https://adminconsole.adobe.com).
1. Selecteer **[!UICONTROL Products]**.
1. Selecteer het specifieke product.
1. Selecteer het tabblad **[!UICONTROL Admins]**. 
1. Selecteer **[!UICONTROL Add admin]** om een beheerder aan het product toe te voegen.
1. Voer een of meer e-mailnamen of gebruikersnamen in het dialoogvenster **[!UICONTROL Add product administrators]** in. Selecteer **[!UICONTROL Save]** voor opslaan.


U definieert toegang tot de productprofielbeheerder via de Admin Console:

1. Toegang [&#x200B; Admin Console &#x200B;](https://adminconsole.adobe.com).
1. Selecteer **[!UICONTROL Products]**.
1. Selecteer het specifieke product. Zorg ervoor dat u al toegang hebt tot de productbeheerder.
1. Selecteer **[!UICONTROL Product profiles]**.
1. Selecteer het specifieke productprofiel.
1. Selecteer het tabblad **[!UICONTROL Admins]**. 
1. Selecteer **[!UICONTROL Add admin]** om een beheerder aan het productprofiel toe te voegen.
1. Voer een of meer e-mailnamen of gebruikersnamen in het dialoogvenster **[!UICONTROL Add product profile administrators]** in. Selecteer **[!UICONTROL Save]** voor opslaan.


#### Machtigingen

De toestemmingen bepalen wat u binnen een product kunt doen zodra u toegang tot het product hebt.

U definieert machtigingen voor Experience Platform in de [!UICONTROL Permissions] -interface en u gebruikt op kenmerken gebaseerd toegangsbeheer. Voor Customer Journey Analytics definieert u machtigingen via [!UICONTROL Admin Console] .

##### Experience Platform

De interface [!UICONTROL Permissions] in Experience Platform is gebaseerd op de definitie van een rol. Een rol is een inzameling van middel gebaseerde toestemmingen. In een nieuwe, provisioned omgeving zijn twee standaardrollen beschikbaar: **[!UICONTROL Default Production All Access]** en **[!UICONTROL Sandbox Administrators]**.

Voor Content Analytics, moet u verifiëren of de volgende middelen en bijbehorende toestemmingen aan deze rollen worden toegevoegd:

* Standaardproductie alle toegangsrol

   * Gegevensverzameling
      * Gegevensstromen weergeven
      * Gegevensstromen beheren

   * Gegevensbeheer
      * Gegevensbestanden weergeven
      * Datasets beheren

   * Gegevensmodellering
      * Schema&#39;s weergeven
      * Schema&#39;s beheren
      * Identiteitsmetagegevens beheren


* Sandbox-beheerdersrol

   * Sandboxes
      * Prod
      * (elke andere sandbox die u voor Content Analytics wilt gebruiken)

   * Sandbox-beheer
      * Pakketten beheren
      * Sandboxen beheren
      * Sandbox opnieuw instellen
      * Sandbox weergeven


Binnen de interface van Toestemmingen kunt u zowel rollen als bijbehorende toestemmingen verifiëren. En welke gebruikers tot de rol behoren.

1. Toegang tot Experience Platform voor uw organisatie.
1. Selecteer **[!UICONTROL Quick access]** in het welkomstscherm in **[!UICONTROL View all]** .
1. Laat het speld ![&#x200B; PinOn &#x200B;](/help/assets/icons/PinOn.svg) voor **[!UICONTROL Permissions]** toe, zodat **[!UICONTROL Permissions]** beschikbaar binnen **[!UICONTROL Quick Access]** voor toekomstig gebruik wordt.
1. Selecteer **[!UICONTROL Permissions]**.
1. Selecteer ![&#x200B; Gebruiker &#x200B;](/help/assets/icons/User.svg) **[!UICONTROL Roles]**.
1. Selecteer de specifieke rol die u wilt verifiëren (bijvoorbeeld **[!UICONTROL Default Production All Access]**). Selecteer **[!UICONTROL View all]** om alle machtigingen weer te geven.
1. In het **[!UICONTROL Details]** -scherm:
   1. Controleer de lijst **[!UICONTROL Resources]** in **[!UICONTROL Permissions]** .
   1. Controleer de namen van de sandboxen in **[!UICONTROL Sandboxes]** .

   Om het even welke updates te maken, uitgezocht ![&#x200B; geef &#x200B;](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** uit.
   1. Om een ontbrekend middel toe te voegen, **[!UICONTROL Resource name]** ![&#x200B; voeg &#x200B;](/help/assets/icons/Add.svg) van **[!UICONTROL Resources]** toe > **[!UICONTROL Adobe Experience Platform]** linkerspoor.
   1. Om een ontbrekende toestemming toe te voegen, selecteer ![&#x200B; ChevronDown &#x200B;](/help/assets/icons/ChevronDown.svg) binnen het middel dat de toestemming in het belangrijkste paneel mist, en selecteer de ontbrekende toestemming.

      ![&#x200B; interface van Toestemmingen &#x200B;](/help/content-analytics/assets/aep-permissions-ui.png)

   Selecteer **[!UICONTROL Save]** om een update op te slaan.

1. In het scherm Gebruikers of gebruikersgroepen:
   1. Verifieer de juiste individuele gebruikers of de groep gebruikers deel van deze rol uitmaken.
      1. Selecteer ![&#x200B; UserAdd &#x200B;](/help/assets/icons/UserAdd.svg) Gebruikers in Gebruikers toevoegen om individuele gebruikers toe te voegen u in Admin Console hebt bepaald.
      1. Selecteer ![&#x200B; toevoegen &#x200B;](/help/assets/icons/Add.svg) Groepen in de groepen van Gebruikers toevoegt om gebruikersgroepen toe te voegen u in Admin Console hebt bepaald.


##### Customer Journey Analytics

Customer Journey Analytics biedt geen ondersteuning voor op kenmerken gebaseerd toegangsbeheer. Als u machtigingen wilt opgeven, gebruikt u de Admin Console.

Voor Content Analytics moet u controleren of de volgende Customer Journey Analytics-productprofielmachtigingen zijn opgenomen:

* Gegevensweergaven
   * Alle beschikbare gegevensweergaven.

* Rapportagetools
   * Toegang tot analyse met instructies?
   * Berekende maateenheden maken
   * Segment maken
   * Toegang tot labs?
   * Aantekening maken
   * Aanmaken publiek?
   * Weergave publiek?
   * Toegang tot controlelogbestanden
   * Projectkoppelingen delen met iedereen
   * Voorspelling
   * AI-assistent: productkennis
   * Data Insights Agent
   * Intelligente bijschriften
   * Vermelding gegevensopslag?

* Gereedschappen voor gegevensweergave
   * Volledige tabelexport?
   * CJA BI Extension?

Deze machtigingen voor Customer Journey Analytics verifiëren en bijwerken:

1. Toegang [&#x200B; Admin Console &#x200B;](https://adminconsole.adobe.com).
1. Selecteer **[!UICONTROL Products]**.
1. Selecteer het **[!UICONTROL Customer Journey Analytics]** -product.
1. Selecteer **[!UICONTROL Product profiles]**.
1. Selecteer het standaardinrichtingsprofiel dat beschikbaar is voor Customer Journey Analytics. Bijvoorbeeld: **[!UICONTROL Customer Journey Analytics]** .
1. Selecteer **[!UICONTROL Permissions]** in het scherm met productprofielen.
1. Selecteer om het even welke ![&#x200B; geef &#x200B;](/help/assets/icons/Edit.svg) knopen uit om de toestemmingen uit te geven. In het dialoogvenster **[!UICONTROL Edit permissions for Customer Journey Analytics]** :

   ![&#x200B; de Toestemmingen UI van CJA &#x200B;](../assets/cja-permissions-ui.png)

   1. Selecteer **[!UICONTROL Data Views]** en schakel **[!UICONTROL Auto-include: On]** in. Met deze schakeloptie zorgt u ervoor dat alle gegevensweergaven automatisch deel uitmaken van de **[!UICONTROL Included permission items]** .
   1. Selecteer **[!UICONTROL Reporting Tools]** en controleer of alle hierboven vermelde machtigingen deel uitmaken van de **[!UICONTROL Included permission items]** .
   1. Selecteer **[!UICONTROL Data View Tools]** en controleer of alle hierboven vermelde machtigingen deel uitmaken van de **[!UICONTROL Included permission items]** .

   Selecteer **[!UICONTROL Save]**.


### Schema en gegevensset instellen

Als u gegevens van uw website wilt verzamelen, moet u eerst bepalen welk soort gegevens u wilt verzamelen, afhankelijk van Content Analytics-inzichten. En ook hoe die gegevens worden opgeslagen. Beide concepten worden verklaard in [&#x200B; Opstelling een schema en dataset &#x200B;](/help/data-ingestion/aepwebsdk.md#set-up-a-schema-and-dataset) in [&#x200B; Samenvattingsgegevens via de 3&rbrace; snelle startgids van SDK van het Web van Adobe Experience Platform &lbrace;.](/help/data-ingestion/aepwebsdk.md)


## Gegevensverzameling configureren

In deze fase maakt u de pijplijn die inhoudsgegevens van uw website vastlegt.

### Een gegevensstroom instellen

U hebt gedefinieerd welke gegevens u wilt verzamelen en hoe u die gegevens wilt opslaan. De volgende stap is ervoor te zorgen dat de gegevens die van uw website worden verzameld aan de dataset worden verpletterd. U moet opstelling en een gegevensstroom vormen, die in [&#x200B; Opstelling een datastream &#x200B;](/help/data-ingestion/aepwebsdk.md#set-up-a-datastream) in de [&#x200B; Samenvatting gegevens via de 3&rbrace; snelle startgids van SDK van het Web van Adobe Experience Platform &lbrace;wordt verklaard.](/help/data-ingestion/aepwebsdk.md)


### Tags gebruiken

U hebt gedefinieerd welke gegevens moeten worden verzameld (schema), hoe die gegevens (dataset) moeten worden opgeslagen en hoe de verzamelde gegevens van uw website naar de gegevensset (datastream) worden gerouteerd. Als volgende stap moet u uw website van labels voorzien om regels en gegevenselementen tegen de gegevens in uw gegevenslaag op uw website te vormen. Als u uw website codeert, zorgt u ervoor dat gegevens naar de geconfigureerde gegevensstroom worden verzonden. Het etiketteren van uw website met de hulp van Markeringen wordt verklaard in [&#x200B; Markeringen van het Gebruik &#x200B;](/help/data-ingestion/aepwebsdk.md#use-tags) in de [&#x200B; Samenvatting gegevens via de 3&rbrace; snelle startgids van SDK van het Web van Adobe Experience Platform.](/help/data-ingestion/aepwebsdk.md)


### Implementeren en valideren

U kunt de code nu implementeren in de ontwikkelingsversie van uw website binnen de tag `<head>` . Wanneer uw website wordt geïmplementeerd, worden gegevens verzameld in Adobe Experience Platform. Die gegevens zijn vervolgens onderworpen aan Content Analytics.

Valideer uw implementatie, verbeter het waar nodig, en zodra correct, stel het in uw het opvoeren en productiemilieu gebruikend de het publiceren werkschemafunctie van Markeringen op


## Rapportage instellen

In deze fase stelt u de verzamelde gegevens beschikbaar voor analyse in rapporten.

### Opstelling een verbinding aan uw dataset

Als u de verzamelde gegevens wilt rapporteren en die gegevens voor Content Analytics wilt configureren, moet u een verbinding instellen in Customer Journey Analytics. De verbinding verbindt met de dataset die de verzamelde gegevens bevat. Hoe te opstelling wordt een verbinding verklaard in [&#x200B; Opstelling een verbinding &#x200B;](../../data-ingestion/aepwebsdk.md#set-up-a-connection) in [&#x200B; Samenvatting gegevens via de 3&rbrace; snelle startgids van SDK van het Web van Adobe Experience Platform &lbrace;.](/help/data-ingestion/aepwebsdk.md)


### Een gegevensweergave instellen

De laatste stap voordat u Content Analytics kunt configureren, is het definiëren van een gegevensweergave. Een gegevensweergave is een container specifiek voor Customer Journey Analytics waarmee u kunt bepalen hoe gegevens van een verbinding moeten worden geïnterpreteerd. In een gegevensweergave kunt u metriek en afmetingen definiëren vanuit de gegevens van een of meer datasets waarmee Customer Journey Analytics is verbonden. Hoe te opstelling wordt een gegevensmening verklaard in [&#x200B; Opstelling een gegevensmening &#x200B;](/help/data-ingestion/aepwebsdk.md#set-up-a-data-view) in [&#x200B; Samenvatting gegevens via de 3&rbrace; snelle startgids van SDK van het Web van Adobe Experience Platform &lbrace;.](/help/data-ingestion/aepwebsdk.md)


### Content Analytics configureren

U hebt nu alles om Content Analytics te configureren.

#### Configuratie met instructies

Gebruik de [&#x200B; geleide configuratietovenaar &#x200B;](guided.md) en selecteer de gegevensmening u als deel van [&#x200B; Opstelling een stap van de gegevensmening &#x200B;](#set-up-a-data-view) creeerde. Deze selectie zorgt ervoor dat Content Analytics wordt geconfigureerd en geïmplementeerd vóór de gegevens die u van uw website verzamelt.

Houd er rekening mee dat de wizard Bewerken met instructies de volgende aanvullende specifieke Content Analytics-objecten configureert:

* **Dataset**, die opstelling automatisch voor de gebeurtenissen van Content Analytics is. Deze dataset gebruikt een specifiek schema van Content Analytics dat reeds wordt gecreeerd en beschikbaar.
* **DataStream**, die opstelling automatisch aan de gebeurtenissen van stroomContent Analytics in de dataset van Content Analytics is.
* **bezit van Markeringen**, dat opstelling automatisch en gevormd met de uitbreiding van Content Analytics is. Deze eigenschap Tags zorgt ervoor dat uw website Content Analytics-gegevens verzendt naar de Content Analytics-gegevensstroom en de Content Analytics-gegevensset.

  >[!IMPORTANT]
  >
  >Verzeker u de optie selecteert om een Nieuw bezit van Markeringen als deel van de [&#x200B; stap van de inzameling van Gegevens &#x200B;](guided.md#new-configuration-1) in de tovenaar tot stand te brengen.
  >


#### Handmatige configuratie

Om Content Analytics voor uw website uit te voeren, moet u het bezit van de Markeringen van Content Analytics [&#x200B; manueel &#x200B;](manual.md) publiceren.


### Een project instellen

Opstelling een project in Customer Journey Analytics om uw [&#x200B; rapporten en visualisaties van Content Analytics &#x200B;](/help/content-analytics/report/report.md) te bouwen. Alternatief, kunt u a [&#x200B; malplaatje van Content Analytics &#x200B;](/help/content-analytics/report/report.md#template) gebruiken om begonnen te worden.
