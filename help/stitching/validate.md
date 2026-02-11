---
title: Identiteitsinstellingen valideren in Customer Journey Analytics
description: Leer hoe u identiteitsstitching in Customer Journey Analytics kunt valideren. Meet de verificatiepercentages en identificatie voor en na het stitching.
solution: Customer Journey Analytics
feature: Stitching, Cross-Channel Analysis
role: Admin
exl-id: b9b73926-6502-4a48-ba73-c784f80950d3
source-git-commit: 0eb3fec2e52fe0850c5f42777edbdb5d981988fb
workflow-type: tm+mt
source-wordcount: '1620'
ht-degree: 0%

---

# Stikken valideren

Het doel van [&#x200B; identiteit het stitching &#x200B;](/help/stitching/overview.md) (of eenvoudig, het stitching) is de geschiktheid van een gebeurtenisdataset voor kanaalanalyse te verhogen. Deze verhoging wordt bereikt wanneer alle rijen van gegevens in de dataset de gewenste hoogste-orde identiteit bevatten die beschikbaar is. Met deze hoogte kunt u:

* Persoonlijke rapporten maken, zonder anonieme personen uit te sluiten.
* Meerdere apparaten aansluiten op één persoon.
* Verbind een persoon over kanalen.

In dit artikel worden analysemethoden beschreven om de hoogte van een of meer nieuw gecreëerde, geordende gegevenssets te meten en om het vertrouwen te wekken dat stitching deze voordelen oplevert.

De analysemethodes impliceren {de montages van de de meningscomponent van 0} Gegevens [&#x200B; die typisch toegankelijk aan beheerders zijn. &#x200B;](/help/data-views/component-settings/overview.md) De methodes vereisen ook analisten, die in een project van Analysis Workspace werken, om berekende metriek en visualisaties tot stand te brengen.

Hoewel deze analysemethoden kunnen worden gebruikt voor stitching in het veld en op grafiek gebaseerde stitching, zijn sommige elementen mogelijk niet aanwezig in de dataset, vooral in een op grafiek gebaseerd stitching scenario. Deze ontbrekende elementen kunnen het moeilijk maken om de lift rechtstreeks in Analysis Workspace te berekenen.

>[!NOTE]
>
>De (validering van) het koppelen van een of meer gegevenssets draagt uiteindelijk bij tot betere analyse en inzichten. In dit artikel wordt echter niet ingegaan op de algemene waarde van een Customer Journey Analytics-configuratie met alle gegevenssets in Experience Platform die zijn uitgelijnd op dezelfde naamruimte. En dat al deze datasets vriendschappelijk worden samengevoegd om analyse over een volledige klantenreis uit te voeren.


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; Plaatsende enablement en bevestiging &#x200B;](https://video.tv.adobe.com/v/3478126?captions=dut&quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]



## Vastzetten in validatie van verbindingen

In deze sectie wordt beschreven hoe u de bevestiging kunt valideren die u hebt ingeschakeld in de interface Verbindingen.

### Verbindingsaanbevelingen

Om het stitching te bevestigen die u in de interface van Verbindingen toeliet, selecteer een korte en representatieve periode voor **[!UICONTROL Dataset backfill]**. Bijvoorbeeld een week.

In het onderstaande voorbeeld wilt u de gegevensset met gebeurtenissen koppelen. U hebt opstelling een testverbinding waarin u de gebeurtenisdataset toevoegt. Voor die dataset definieert u **[!UICONTROL ECID]** **[!UICONTROL Namespace]** als **[!UICONTROL Persistent ID]** en **[!UICONTROL Visitor Hashed Email Address (directMarketing.hashedEmail)]** als **[!UICONTROL Person ID]** . Als u deze instelling wilt valideren, definieert u een **[!UICONTROL Dataset backfill]** voor een klein tijdvenster (24 januari 2026 - 10 februari 2026). U gebruikt dat kleine venster om te controleren of het stitching werkt zoals bedoeld.

![&#x200B; het Plaatsen config &#x200B;](/help/stitching/assets/stitching-config.png)

### Voorwaarden voor gegevensweergave

Voor stitching bevestiging, moet u ervoor zorgen u alle vereiste afmetingen en metriek van uw gestikte dataset hebt die in een gegevensmening wordt bepaald. Maak een gegevensweergave op basis van de eerder gedefinieerde verbinding. In de **[!UICONTROL Components]** stap van de configuratie van de gegevensmening, moet u:

* Voeg **[!UICONTROL Identity Namespace]** vanuit **[!UICONTROL Metrics & Dimensions]** als een dimensie toe aan de lijst **[!UICONTROL Dimensions]** .

  ![&#x200B; Namespace van de Identiteit &#x200B;](/help/stitching/assets/identity-namespace.png)


* Selecteer in **[!UICONTROL Visitor Hashed Email Address Identifier]** de persoon-id die u als de persoon-id voor uw gebeurtenissen hebt gedefinieerd. **[!UICONTROL Schema fields]** Voeg het veld als een dimensie toe aan de lijst **[!UICONTROL Dimensions]** en als een metrische waarde aan de lijst **[!UICONTROL Metrics]** . Wijzig **[!UICONTROL Component name]** voor metrisch aan `Email set`.

  ![&#x200B; E-mailherkenningsteken &#x200B;](/help/stitching/assets/email-identifier.png)

Zorg ervoor dat u de gegevensweergave opslaat.

### Workspace-project maken

In Workspace maakt u een nieuw project en gebruikt u een vrije-vormtabel om de **[!UICONTROL Email set]** -metrische waarde weer te geven voor het datumbereik dat u hebt gedefinieerd om de stitching-configuratie te testen. In deze vrije-vormtabel staan de gebeurtenissen die wel een e-mailadres hebben voordat u een koppeling maakt.

![&#x200B; het Titel overzicht vrije lijst van de vorm - E-mail reeks &#x200B;](/help/stitching/assets/workspace-emailset.png)

Als u gebeurtenissen wilt zien waarvoor een e-mailadres is ingesteld na het koppelingsproces, definieert u een berekende metrische waarde `Email stitched namespace` . Die berekende metrische waarde bekijkt **[!UICONTROL Events]** die een **[!UICONTROL Identity Namespace]** gelijk aan de hashed email naamruimte `email_lc_sha256` hebben.

![&#x200B; het Plaatsen overzicht - E-mail gestikte namespace berekende metrisch &#x200B;](/help/stitching/assets/cm-email-stitched-namespace.png)

Als u de nieuwe berekende metrische waarde **[!UICONTROL Email stitched namespace]** toevoegt aan de vrije-vormlijst, ziet u de toename in het aantal gebeurtenissen die nu een e-mailadres na het het stitching proces hebben.

![&#x200B; Stitching overzicht vrije lijst van de vorm - E-mail reeks en vastgemaakt &#x200B;](/help/stitching/assets/workspace-emailset-stitched.png)

U kunt meer inzichten krijgen wanneer u twee extra berekende metriek bepaalt.

* **[!UICONTROL Email authentication rate]**. Deze berekende metrisch bepaalt het authentificatietarief vóór het stitching proces.

  ![&#x200B; berekend metrische definitie van het e-mailauthentificatiesnelheid &#x200B;](/help/stitching/assets/cm-email-authentication-rate.png)

* **[!UICONTROL Stitched authentication rate]**. Deze berekende metrisch bepaalt het authentificatietarief na het stitching proces.

  ![&#x200B; Stitched authentificatietarief berekende metrische definitie &#x200B;](/help/stitching/assets/cm-stitched-authentication-rate.png)

Voeg deze twee extra berekende metriek aan uw freeform lijst toe, en u kunt de toename in stitched gebeurtenissen zien.

![&#x200B; het Plaatsen overzicht vrije vormlijst - voor authentiek verklaard &#x200B;](/help/stitching/assets/workspace-authenticated.png)

Voor meer inzichten, kunt u twee meer berekende metriek (**[!UICONTROL Percent increase]** en **[!UICONTROL Lift]**) aan uw vrije lijst toevoegen om het effect van uw stitching configuratie te zien.

![&#x200B; het Plaatsen overzicht vrije vormlijst - Voor authentiek verklaarde Lift &#x200B;](/help/stitching/assets/workspace-authenticated-lift.png)



## Validatie aanvragen

In deze sectie wordt beschreven hoe u de stitching kunt valideren die u van Adobe hebt aangevraagd. Deze methode is afgekeurd, maar u zou nog datasets kunnen hebben die gebruikend deze methode werden vastgemaakt.

### Voorwaarden voor gegevensweergave

Voor het stitching de metingsplan van de bevestigingsbevestiging, moet u ervoor zorgen u alle vereiste afmetingen en metriek van uw gestikte dataset hebt die in een gegevensmening wordt bepaald. Controleer of de velden `stitchedID.id` en `stitchedID.namespace.code` als afmetingen zijn toegevoegd. Terwijl de gestikte dataset een nauwkeurige kopie van de originele dataset is, voegt het stitching proces deze twee nieuwe kolommen aan de dataset toe:

* Gebruik `stitchedID.namespace.code` om een **[!UICONTROL Stitched Namespace]** -dimensie te definiëren. Deze dimensie bevat de naamruimte van de identiteit waarnaar de rij is verheven, bijvoorbeeld `Email` of `Phone` . Of de naamruimte waar het stitching-proces naar terugloopt, zoals `ECID` .
  ![&#x200B; Stitched namespace dimensie &#x200B;](/help/stitching/assets/stitchednamespace-dimension.png)

* Gebruik `stitchedID.id` om een **[!UICONTROL Stitched ID value]** -dimensie te definiëren. Deze dimensie bevat de onbewerkte waarde van de identiteit. Bijvoorbeeld: hashed email, hashed phone, ECID. Deze waarde wordt gebruikt bij **[!UICONTROL Stitched Namespace]** .
  ![&#x200B; Verplaatste dimensie van identiteitskaart &#x200B;](/help/stitching/assets/stitchedid-dimension.png)


Bovendien moet u twee stitching metriek toevoegen die op de aanwezigheid van waarden in een dimensie gebaseerd zijn.

1. Gebruik het gebied dat persoonsidentiteitskaart van de gestikte dataset bevat om metrisch te vormen die bepaalt of een persoonsidentiteitskaart wordt geplaatst. Voeg deze persoon-id toe, zelfs als u op grafiek gebaseerde stitching gebruikt, aangezien de persoon-id helpt om een basislijn te bepalen. Als de persoon-id zich niet in de gegevensset bevindt, is de basislijn 0%.

   In het onderstaande voorbeeld fungeert `personalEmail.address` als de identiteit en wordt het gebruikt om de **[!UICONTROL _Email set]** -parameter te maken.
   ![&#x200B; metrische reeks E-mail &#x200B;](/help/stitching/assets/emailset-metric.png)

1. Gebruik het veld `stitchedID.namespace.code` om een **[!UICONTROL Email stitched namespace]** metrische waarde te maken. Verzeker u [&#x200B; omvat omvat exclusief waarden in componentenmontages &#x200B;](/help/data-views/component-settings/include-exclude-values.md), zodat overweegt u slechts waarden van namespace u probeert om rijen van gegevens op te heffen.
   1. Selecteer **[!UICONTROL Set include/exclude values]**.
   1. Selecteer **[!UICONTROL If all criteria are met]** als de **[!UICONTROL Match]** .
   1. Geef **[!UICONTROL Equals]** `email` op als de **[!UICONTROL Criteria]** om gebeurtenissen te selecteren die naar de naamruimte E-mail zijn verplaatst.

   ![&#x200B; E-mail verbonden namespace metrisch &#x200B;](/help/stitching/assets/emailstitchednamespace-metric.png)

### Gestikte afmetingen

Met beide dimensies die aan de gegevensmening worden toegevoegd, gebruik [&#x200B; Vrije lijsten &#x200B;](/help/analysis-workspace/visualizations/freeform-table/freeform-table.md) in Analysis Workspace om de gegevens te controleren die elke dimensie heeft.

In de **[!UICONTROL Stitched Namespace]** metingslijst, ziet u typisch twee rijen voor elke dataset. Eén rij vertegenwoordigt wanneer het koppelingsproces de fallback-methode (ECID) moest gebruiken. De andere rij bevat gebeurtenissen die zijn gekoppeld aan de gewenste naamruimte voor de identiteit (e-mail).

Voor de **[!UICONTROL Stitched ID value]** dimensietabel ziet u de onbewerkte waarden die uit de gebeurtenissen komen. In deze tabel ziet u dat de waarden tussen de permanente id en de gewenste persoon-id eindigen.

![&#x200B; Controle verstikte dimensies &#x200B;](/help/stitching/assets/check-data-on-stitching.png)


### Apparaatgecentreerde of persoongerichte rapportage

Wanneer u een verbinding maakt, moet u definiëren welk veld of welke identiteit wordt gebruikt voor de persoon-id. Bijvoorbeeld, op een Webdataset, als u een apparatenidentiteitskaart als persoonsidentiteitskaart kiest, dan creeert u apparaat-centric rapporten en verliest de capaciteit om zich bij deze gegevens met andere off-line kanalen aan te sluiten. Als u een kanaaloverschrijdend veld of een identiteit selecteert, bijvoorbeeld een e-mailbericht, verliest u bij niet-geverifieerde gebeurtenissen. Om dit effect te begrijpen, moet u erachter komen hoeveel van het verkeer unauthenticated is en hoeveel van het verkeer voor authentiek verklaard is.

1. Maak een berekende metrische waarde **[!UICONTROL Unauthenticated events over total]**. Bepaal de regel in de regelbouwer zoals hieronder getoond:
   ![&#x200B; Niet voor authentiek verklaarde gebeurtenissen over totaal &#x200B;](/help/stitching/assets/calcmetric-unauthenticatedeventsovertotal.png)

1. Maak een berekende metrische waarde **[!UICONTROL Email authentication rate]** op basis van de **[!UICONTROL _Email set]** -waarde die u eerder hebt gedefinieerd. Bepaal de regel in de regelbouwer zoals hieronder getoond:
   ![&#x200B; Het tarief van de E-mail authentificatie &#x200B;](/help/stitching/assets/calcmetric-emailauthenticationrate.png)

1. Gebruik **[!UICONTROL Unauthenticated events over total]** berekende metrisch, samen met **[!UICONTROL Email authentication rate]** berekende metrisch, om a [&#x200B; &#x200B;](/help/analysis-workspace/visualizations/donut.md) visualisatie van de Donut te creëren. De visualisatie toont het aantal gebeurtenissen in de dataset die unauthenticated en voor authentiek verklaard zijn.

   ![&#x200B; de details van de Identificatie &#x200B;](/help/stitching/assets/identification-details.png)



### Vastleggingscijfers

U wilt de identificatieprestaties vóór en na het stikken meten. Hiertoe maakt u drie extra berekende maatstaven:

1. Een **[!UICONTROL Stitched authentication rate]** berekende metrische waarde die het aantal gebeurtenissen berekent waar de gestikte naamruimte aan de gewenste identiteit over het totale aantal gebeurtenissen wordt geplaatst. Wanneer u de gegevensweergave instelt, hebt u een **[!UICONTROL Email stitched namespace]** -metrische code gemaakt die een filter bevat dat alleen moet worden geteld wanneer voor een gebeurtenis een naamruimte is ingesteld op e-mail. De berekende metrische waarde gebruikt deze **[!UICONTROL Email stitched namespace]** metrische waarde om een indicatie te geven van welk percentage van de gegevens de gewenste identiteit heeft.
   ![&#x200B; Stitched metrisch berekend authentificatietarief &#x200B;](/help/stitching/assets/calcmetric-stitchedauthenticationrate.png)

1. Een **[!UICONTROL Percent increase]** berekende maatstaf die de onbewerkte percentagewijziging tussen de huidige en de gestikte identificatiesnelheid berekent.
   ![&#x200B; Percentage berekende toename metrisch &#x200B;](/help/stitching/assets/calcmetric-percentincrease.png)

1. Een **[!UICONTROL Lift]** berekende maatstaf die de lift berekent tussen de huidige identificatiesnelheid en de geneutraliseerde identificatiesnelheid.
   ![&#x200B; Lift berekende metrisch &#x200B;](/help/stitching/assets/calcmetric-lift.png)


### Conclusie

Als u alle gegevens in een Analysis Workspace Freeform-tabel combineert, kunt u de impact en waarde die stitching biedt, inclusief:

* Huidige verificatiesnelheid: de basislijn van het aantal gebeurtenissen dat al de juiste persoon-id had over het totale aantal gebeurtenissen.
* Stitched authentication rate: Het nieuwe aantal gebeurtenissen die correcte persoon identiteitskaart over het totale aantal gebeurtenissen hebben.
* Percentage verhoging: de ruwe percentageverhoging van het stitched authentificatiesnelheid minus het basislijnhuidige authentificatiesnelheid.
* Optillen: De procentuele wijziging ten opzichte van de huidige verificatiesnelheid van de basislijn.

![&#x200B; prestaties van de Identificatie &#x200B;](/help/stitching/assets/identification-performance.png)


## Toetsen

De belangrijkste punten uit dit artikel zijn dat u door het stitching van validatie en analyse kunt helpen:

* Verstrek een uitvoerige douanemening van authentificatiedoeltreffendheid door stroom tegenover gestikte tarieven te vergelijken.
* Hiermee kunt u de verbetering duidelijk meten aan de hand van percentageverhogingen en liftmetriek.
* Help de ware impact van het implementeren van stitching op gebruikersverificatie te identificeren.
* Creeer een gestandaardiseerde manier om authentificatieprestaties over teams mee te delen.
* Gegevensgestuurde beslissingen over verificatiestrategie en optimalisatie toestaan.

Deze cijfers geven samen belanghebbenden een volledig beeld van hoe Customer Journey Analytics stitching authentificatiesuccespercentages en algemene prestaties van de persoonsidentificatie beïnvloedt.
