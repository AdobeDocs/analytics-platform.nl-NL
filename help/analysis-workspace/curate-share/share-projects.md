---
description: Projectdeling en projectrollen in Workspace
keywords: Analysis Workspace delen
title: Projecten delen
feature: Curate and Share
exl-id: ac4ed73a-e890-46cc-be08-4ccedf66b47d
role: User
source-git-commit: a62ac798da9d66fa3d88262ef7d04aa4bf6a3303
workflow-type: tm+mt
source-wordcount: '1942'
ht-degree: 0%

---

# Projecten delen {#share-projects}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_shareprojects"
>title="Projecten delen"
>abstract="U kunt om het even welk van deze projectrollen met andere gebruikers in uw organisatie delen."

<!-- markdownlint-enable MD034 -->


U kunt een Analysis Workspace-project delen met de volgende typen personen:

* Gebruikers en groepen in uw organisatie die toegang hebben tot Adobe Customer Journey Analytics

  U kunt de toegang Bewerken, Dupliceren of Weergeven delen

* Gebruikers en groepen in uw organisatie die geen toegang hebben tot Customer Journey Analytics

  Ontvangers hebben alleen-lezen toegang

* Personen buiten uw organisatie

  Ontvangers hebben alleen-lezen toegang

Om het even welke [ kromming ](curate.md) u voorafgaand aan het delen toepast wordt weerspiegeld wanneer de ontvangers het project openen.

+++ Bekijk een video waarin wordt getoond hoe u projecten kunt delen.

>[!VIDEO](https://video.tv.adobe.com/v/36207/?quality=12)

{{videoaa}}

+++

## Delen met gebruikers en groepen van Customers Journey Analytics in uw organisatie {#Add}

U kunt een project met bestaande gebruikers of groepen van de Customer Journey Analytics in uw organisatie delen. Wanneer u een project deelt zoals beschreven in deze sectie, moeten de gebruikers u met delen reeds een rekening van de Customer Journey Analytics hebben.

U kunt een specifieke rol met gebruikers of groepen delen, of u kunt een verbinding delen.

* [Een specifieke projectrol delen](#share-a-specific-project-role)

* [Een koppeling naar een project delen](#share-a-link-to-a-project)

## Een specifieke projectrol delen

Wanneer het delen van een specifieke projectrol met gebruikers en groepen in uw organisatie, overweeg het volgende:

* Projectrollen (**[!UICONTROL Edit original]**, **[!UICONTROL Edit copy]** en **[!UICONTROL Read only]**) zijn gekoppeld aan de gebruiker en specifieke project-id. De rollen van het project zijn onafhankelijk van gebruikerstoestemmingen die in de [ worden beheerd Adobe Experience Cloud admin console ](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

* In Customer Journey Analytics, worden de groepen bepaald door productprofielen in de [ Adobe Experience Cloud admin console ](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html). Beheerders kunnen gegevens delen met elke groep, inclusief Alles. Niet-beheerders kunnen delen met elke groep waarvan zij lid zijn, met uitzondering van &quot;Alle&quot;.

* Een gebruiker die in veelvoudige rollen wordt geplaatst krijgt altijd de hoogste ervaring. Dit kan voorkomen als een gebruiker zowel als individu als deel van een groep wordt toegevoegd. Als een gebruiker bijvoorbeeld de **[!UICONTROL Edit original]** rol als individu en de **[!UICONTROL Read only]** rol als lid van een groep krijgt, krijgt hij een **[!UICONTROL Edit original]** project beleving.

* Beheerders die in de rol **[!UICONTROL Edit copy]** of **[!UICONTROL Read only]** zijn geplaatst, krijgen die beperkte ervaring wanneer ze een project openen. Een beheerder kan zijn rol in **[!UICONTROL Edit original]** veranderen door het project met zichzelf te delen en de rol Edit toe te kennen, zoals beschreven in de volgende procedure.

* Als de veelvoudige projecten worden geselecteerd om worden gedeeld, zullen de ontvangers aan de bestaande lijst van ontvangers voor elk project worden toegevoegd.

  Project A wordt bijvoorbeeld al gedeeld met ontvangers 1, 2 en 3, terwijl Project B al wordt gedeeld met ontvangers 4, 5 en 6.

  De projecten A en B worden dan gedeeld met ontvangers 4 en 7. De nieuwe aandelenlijst voor Project A is nu 1, 2, 3, 4, en 7, terwijl de nieuwe aandeellijst voor Project B 4, 5, 6, en 7 is.

Een specifieke projectrol delen met gebruikers of groepen in uw organisatie:

1. In Customer Journey Analytics, selecteer het [!UICONTROL **Workspace**] lusje, dan selecteer [!UICONTROL **Projecten**] in het linkerpaneel.

1. Selecteer checkbox naast één of meerdere projecten die u wilt delen, dan selecteren [!UICONTROL **Aandeel**].

   of

   Als u alleen een afzonderlijk project wilt delen, opent u het project dat u wilt delen en selecteert u **[!UICONTROL Share]** > **[!UICONTROL Share with Workspace users]** .
Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd eerst uw project op te slaan.

   Het dialoogvenster Project delen wordt weergegeven. Het [!UICONTROL **Aandeel door verbinding**] en [!UICONTROL **3} secties van Montages {van de dialoogdoos is zichtbaar slechts wanneer het delen van één enkel project.**]

   ![ het het projectvenster van het Aandeel.](assets/share-proj-modal.png)

1. Voeg ontvangers of groepen ontvangers toe aan een van de opgegeven rolvelden:

   **geeft origineel uit:** Ontvangers kunnen **[!UICONTROL Save]** veranderingen in een project en een functie als medeeigenaars. Deze rol is nuttig als u een project met andere collega&#39;s wilt cobeheren; dit omvat het uitgeven, schrappen, en het wijzigen van ontvankelijke lijsten voor een gedeeld project. <br> Nota: Analysis Workspace steunt momenteel geen levende samenwerking, zodat wordt geadviseerd dat slechts één gebruiker een project in een bepaalde tijd uitgeeft. Als projecten tegelijkertijd worden opgeslagen, blijft de laatste versie behouden.

   **geef exemplaar uit:** Ontvangers kunnen **[!UICONTROL Save as]** en hebben toegang tot het linkerpaneel. Projectinteracties zijn in deze rol niet beperkt. Deze rol is nuttig als u een project aan gebruikers wilt delen die de gegevens van uw organisatie en hoe te om Analysis Workspace begrijpen, maar u wilt niet uw project veranderen.

   **las slechts:** Ontvangers kunnen niet **[!UICONTROL Save]** of **[!UICONTROL Save as]** en hebben geen toegang tot het linkerpaneel. De interactie tussen projecten is ook beperkt. Deze rol is nuttig als u een project aan gebruikers wilt delen die minder vertrouwd met de gegevensstructuur van uw organisatie, Analysis Workspace of Customer Journey Analytics over het algemeen zijn. U wilt echter nog steeds dat ze gegevens en inzichten in een veilige omgeving gebruiken. Leer meer over [ las slechts projectervaring ](/help/analysis-workspace/curate-share/view-only-projects.md).

1. (Voorwaardelijk) Als u één project deelt, kies of om de volgende opties toe te laten wanneer het delen van het project:

   * **Deel ingebedde projectcomponenten:** de filters van Aandelen, berekende metriek, en datumwaaiers met alle ontvangers. Nadat deze componenten zijn gedeeld, worden deze weergegeven in de vervolgkeuzelijst Componenten van de Workspace van de ontvanger. Deze instelling blijft niet bestaan. Het is een eenmalige actie op het moment van delen.

   * **Reeks als het landen pagina voor ontvangers:** plaatst deze pagina als het landen pagina voor ontvangers. Deze instelling blijft niet bestaan. Het is een eenmalige actie op het moment van delen.

1. Selecteer **[!UICONTROL Share]** . (Als het project reeds is gedeeld, uitgezochte [!UICONTROL **Update**].)

   of

   Selecteer **[!UICONTROL Curate and Share]** om automatisch projectcuratie toe te passen. (Als het project reeds is gedeeld, uitgezochte **[!UICONTROL Curate & Update]**.) Leer meer over [ projectcuratie ](curate.md).

## Een koppeling naar een project delen

Houd rekening met het volgende wanneer u een koppeling deelt zoals wordt beschreven in deze sectie:

* Ontvangers die de koppeling gebruiken, moeten zich aanmelden bij de Customer Journey Analytics voordat ze toegang krijgen tot het project.

* Als een ontvanger geen rol wordt toegewezen en a [ verbinding ](/help/analysis-workspace/curate-share/shareable-links.md) aan het project (**[!UICONTROL Share]ontvangt >[!UICONTROL Get project link]**), worden zij gegeven een rol door gebrek. Beheerders ontvangen **[!UICONTROL Edit original]** en niet-beheerders ontvangen **[!UICONTROL Edit copy]** .

De projectkoppeling delen met gebruikers in uw organisatie:

1. Sla het project op. Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd uw project op te slaan voordat u een koppeling deelt.

1. Selecteer **[!UICONTROL Share]** > **[!UICONTROL Share with Workspace users]** en selecteer vervolgens **[!UICONTROL Copy]** naast het veld **[!UICONTROL Share by link]** .

   ![ het project van het Aandeel dat het Aandeel door verbindingsgebied benadrukt.](assets/share-proj-modal.png)

1. Deel de koppeling met gebruikers in uw organisatie. U kunt het bijvoorbeeld in een e-mail, op een interne website, enzovoort plakken.

## Een project delen met iedereen (geen aanmelding vereist) {#share-public-link}

U kunt [ read-only toegang ](/help/analysis-workspace/curate-share/view-only-projects.md) tot de projecten van Analysis Workspace aan mensen verlenen die geen toegang tot Customer Journey Analytics hebben. Dit kan het volgende omvatten:

* Personen buiten uw organisatie

* Personen binnen uw organisatie die geen toegang hebben tot Customer Journey Analytics

>[!NOTE]
>
>Houd rekening met het volgende wanneer u een Analysis Workspace-project deelt met mensen die geen toegang hebben tot Customer Journey Analytics:
>
>* De capaciteit om een project op deze manier te delen kan door de beheerder van de Customer Journey Analytics worden onbruikbaar gemaakt, zoals die in [ Voorkeur ](/help/analysis-workspace/user-preferences.md) wordt beschreven. Als u een project niet kunt delen zoals die in deze sectie wordt beschreven, heeft uw beheerder van de Customer Journey Analytics deze mogelijkheid onbruikbaar gemaakt.
>
>* Projecten met meer dan 50 uitgebreide visualisaties kunnen niet worden gedeeld met mensen die geen toegang tot Customer Journey Analytics hebben.
>
>* De gebruikers u met deelt kunnen om het even welke filters bekijken die op het project tijdens [ kromming ](curate.md) werden toegepast.
> 
>* Gebruikers met wie u deelt, kunnen het datumbereik van het project wijzigen. De datumwaaier u voor het project plaatst wordt getoond door gebrek.
>
>* Een project zou ontoegankelijk kunnen worden als vele gebruikers proberen om tot een bepaalde verbinding tezelfdertijd toegang te hebben. Standaard hebben meer dan 190 personen elke 5 minuten toegang tot één koppeling. Als uw organisatie deze limiet heeft bereikt, wacht u 5 minuten en probeert u de koppeling opnieuw te openen.
>
>* De functie [!UICONTROL Share with anyone] is geblokkeerd voor licenties voor zowel het Healthcare Shield als het Privacy &amp; Security Shield.

In de volgende videodemonstratie en de bijbehorende documentatie worden de opties beschreven voor het delen van een koppeling met iedereen:

>[!VIDEO](https://video.tv.adobe.com/v/3420093/?learn=on)

Een Analysis Workspace-project met iedereen delen:

1. Open het Analysis Workspace-project dat u wilt delen.

1. Selecteer **[!UICONTROL Share]** > **[!UICONTROL Share with anyone]** .

   Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd uw project op te slaan.

   <!-- Add screen shot of new modal -->

1. Schakel de optie **[!UICONTROL Link is active]** in als deze nog niet is ingeschakeld.

   Als u deze optie selecteert, wordt een koppeling naar het project gemaakt die met iedereen kan worden gedeeld. U kunt toegang tot het project op elk ogenblik onbruikbaar maken door deze optie onbruikbaar te maken.

   De eigenaar van het project is ook de eigenaar van deze verbinding. De eigendom van de verbinding kan aan een andere gebruiker worden overgebracht slechts wanneer de projecteigendom wordt overgebracht, zoals die in [ wordt beschreven de gebruikersactiva van de Overdracht ](/help/tools/asset-transfer/transfer-assets.md) in de gids Admin van Analytics.

1. Geef op of u de volgende beveiligingsoptie wilt inschakelen (deze optie kan worden beheerd door de beheerder van de Customer Journey Analytics):

   * **[!UICONTROL Require Experience Cloud authentication]:**

     Wanneer deze optie wordt toegelaten, zijn de enige gebruikers die tot het project kunnen toegang hebben degenen die login aan de organisatie van Adobe Experience Cloud kunnen zijn waar het project dat u deelt werd gecreeerd. Gebruikers met wie u echter deelt, hoeven geen toegang tot Customer Journey Analytics te hebben.

     De beheerders van de Customer Journey Analytics kunnen deze voorkeur voor het bedrijf vormen, zoals die in [ Voorkeur ](/help/analysis-workspace/user-preferences.md) wordt beschreven. U zou de volgende scenario&#39;s, afhankelijk van kunnen ontmoeten hoe de beheerder deze optie vormde:

      * Als deze optie niet zichtbaar is, heeft de beheerder van de Customer Journey Analytics deze functie niet ingeschakeld.

      * Als deze optie wordt toegelaten en u het niet kunt onbruikbaar maken, betekent dit dat uw beheerder van de Customer Journey Analytics Experience Cloud authentificatie voor iedereen vereist die tot de projecten van Analysis Workspace toegang heeft. Dit is altijd het geval voor organisaties die een vergunning hebben voor het gezondheidsschild.

1. Naast het **[!UICONTROL Share with anyone (no login required)]** gebied, uitgezochte ![ Verbinding ](/help/assets/icons/Link.svg) om de verbinding aan uw systeemklembord te kopiëren.

1. Deel de koppeling met de personen die u toegang tot het project wilt geven. U kunt de koppeling bijvoorbeeld in een e-mail plakken.

   Iedereen met wie u de koppeling deelt, kan het Analysis Workspace-project bekijken.

1. (Facultatief) kunt u selecteren ![ produceer nieuw verbindingspictogram ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg) om toegang uit gebruikers te verwijderen die eerder een verbinding aan het project ontvingen. Er wordt een nieuwe koppeling gegenereerd die u kunt delen met gebruikers die toegang willen krijgen tot het project.

1. Selecteer **[!UICONTROL Close]** om het dialoogvenster Delen te sluiten. Uw wijzigingen worden automatisch opgeslagen.

## Projecten weergeven die met u worden gedeeld

Wanneer iemand een project met u deelt door [ een specifieke projectrol ](#share-a-specific-project-role) te delen, kunt u tot de gedeelde projecten van het [ lusje van Projecten van op de Analytics toegang hebben die pagina ](/help/getting-started/landing.md#navigate-the-projects-tab) landen.

Wanneer iemand een project met u deelt door een verbinding (of van het [ het projectlusje van het Aandeel ](#share-a-link-to-a-project) of het gebruiken van a [ aandeel met iedereen verbinding ](#share-a-project-with-anyone-no-login-required)) te delen, moet u de verbinding gebruiken die met u werd gedeeld om tot het project toegang te hebben. De koppeling kan bijvoorbeeld zijn gedeeld in een e-mail, op een interne website, enzovoort.

## Ingesloten componenten delen

Hier volgt een video over het onderwerp:

>[!VIDEO](https://video.tv.adobe.com/v/24713/?quality=12)

## Veelgestelde vragen {#FAQs}

| Vraag | Antwoord |
|---|---|
| Wat gebeurt er als twee editors tegelijkertijd een project opslaan? | De wijzigingen worden niet samengevoegd en de laatst opgeslagen projectversie blijft behouden. Analysis Workspace biedt momenteel geen ondersteuning voor live samenwerken. |
| Als beheerder, welke projectervaring zal ik zien? | Beheerders die in een **[!UICONTROL Edit copy]** - of **[!UICONTROL Read only]** -rol zijn geplaatst, krijgen die beperkte ervaring wanneer ze een project openen. Een beheerder kan zijn rol desgewenst op elk gewenst moment tot **[!UICONTROL Edit original]** uitbreiden via **[!UICONTROL Components]>[!UICONTROL Projects]** . |
| Wat gebeurt er als een ontvanger in één rol als individu en een andere rol als lid van een groep wordt geplaatst? | Als een ontvanger in veelvoudige rollen wordt geplaatst, zullen zij altijd de hogere ervaring ontvangen. Als een ontvanger bijvoorbeeld de **[!UICONTROL Edit original]** -rol als individu krijgt en de **[!UICONTROL Can view]** -rol als lid van een groep, krijgt hij of zij een **[!UICONTROL Edit original]** -projectervaring. |
| Welke ervaring krijgt een ontvanger als hij of zij een projectverbinding opent? | Ontvangers krijgen de rol die u hen in de deelmodus hebt geplaatst. Als een ontvanger geen rol wordt toegewezen en een koppeling naar het project ontvangt (**[!UICONTROL Share]** > **[!UICONTROL Share with Workspace users]** , selecteert u **[!UICONTROL Copy]** naast het veld **[!UICONTROL Share by link]** ), worden deze standaard in een rol geplaatst. Beheerders ontvangen **[!UICONTROL Edit original]** en niet-beheerders ontvangen **[!UICONTROL Edit copy]** . |
