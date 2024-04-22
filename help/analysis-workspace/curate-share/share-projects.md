---
description: Projectdeling en projectrollen in Workspace
keywords: Analysis Workspace delen
title: Projecten delen
feature: Curate and Share
exl-id: ac4ed73a-e890-46cc-be08-4ccedf66b47d
role: User
source-git-commit: 19923592c8c50d93e150ba908f23313513d3450b
workflow-type: tm+mt
source-wordcount: '1940'
ht-degree: 0%

---

# Projecten delen

U kunt een Analysis Workspace-project delen met de volgende typen personen:

* Gebruikers en groepen in uw organisatie die toegang hebben tot Adobe Customer Journey Analytics

  U kunt de toegang Bewerken, Dupliceren of Weergeven delen

* Gebruikers en groepen in uw organisatie die geen toegang hebben tot Customer Journey Analytics

  Ontvangers hebben alleen-lezen toegang

* Personen buiten uw organisatie

  Ontvangers hebben alleen-lezen toegang

Alle [kromming](curate.md) Wanneer ontvangers het project openen, wordt u deze toepassing vóór het delen weergegeven.

Hier volgt een video-overzicht van het delen van projecten:

>[!VIDEO](https://video.tv.adobe.com/v/36207/?quality=12)


## Delen met gebruikers en groepen van Customers Journey Analytics in uw organisatie {#Add}

U kunt een project met bestaande gebruikers of groepen van de Customer Journey Analytics in uw organisatie delen. Wanneer u een project deelt zoals beschreven in deze sectie, moeten de gebruikers u met delen reeds een rekening van de Customer Journey Analytics hebben.

U kunt een specifieke rol met gebruikers of groepen delen, of u kunt een verbinding delen.

* [Een specifieke projectrol delen](#share-a-specific-project-role)

* [Een koppeling naar een project delen](#share-a-link-to-a-project)

## Een specifieke projectrol delen

Wanneer het delen van een specifieke projectrol met gebruikers en groepen in uw organisatie, overweeg het volgende:

* Projectrollen (**[!UICONTROL Edit original]**, **[!UICONTROL Edit copy]**, en **[!UICONTROL Read only]**) is gekoppeld aan de gebruiker en specifieke project-id. De rollen van het project zijn onafhankelijk van gebruikerstoestemmingen die in [Adobe Experience Cloud-beheerconsole](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

* In de Customer Journey Analytics worden groepen gedefinieerd op basis van productprofielen in het dialoogvenster [Adobe Experience Cloud-beheerconsole](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html). Beheerders kunnen gegevens delen met elke groep, inclusief Alles. Niet-beheerders kunnen delen met elke groep waarvan zij lid zijn, met uitzondering van &quot;Alle&quot;.

* Een gebruiker die in veelvoudige rollen wordt geplaatst krijgt altijd de hoogste ervaring. Dit kan voorkomen als een gebruiker zowel als individu als deel van een groep wordt toegevoegd. Als een gebruiker bijvoorbeeld de opdracht **[!UICONTROL Edit original]** als individu en **[!UICONTROL Read only]** als lid van een groep ontvangen zij een **[!UICONTROL Edit original]** ervaring met projecten.

* Beheerders die in het dialoogvenster **[!UICONTROL Edit copy]** of **[!UICONTROL Read only]** de rol krijgt die beperkte ervaring wanneer zij een project openen . Een beheerder kan zijn rol wijzigen in **[!UICONTROL Edit original]** door het project met zichzelf te delen en de rol Edit toe te kennen, zoals beschreven in de volgende procedure.

* Als de veelvoudige projecten worden geselecteerd om worden gedeeld, zullen de ontvangers aan de bestaande lijst van ontvangers voor elk project worden toegevoegd.

  Project A wordt bijvoorbeeld al gedeeld met ontvangers 1, 2 en 3, terwijl Project B al wordt gedeeld met ontvangers 4, 5 en 6.

  De projecten A en B worden dan gedeeld met ontvangers 4 en 7. De nieuwe aandelenlijst voor Project A is nu 1, 2, 3, 4, en 7, terwijl de nieuwe aandeellijst voor Project B 4, 5, 6, en 7 is.

Een specifieke projectrol delen met gebruikers of groepen in uw organisatie:

1. Selecteer in Customer Journey Analytics de optie [!UICONTROL **Werkruimte**] tab, dan selecteren [!UICONTROL **Projecten**] in het linkerspoor.

1. Schakel het selectievakje naast een of meer projecten die u wilt delen in en selecteer vervolgens [!UICONTROL **Delen**].

   of

   Als u alleen een afzonderlijk project wilt delen, opent u het project dat u wilt delen en selecteert u **[!UICONTROL Share]** > **[!UICONTROL Share with Workspace users]**.
Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd eerst uw project op te slaan.

   Het dialoogvenster Project delen wordt weergegeven. De [!UICONTROL **Delen via koppeling**] en [!UICONTROL **Instellingen**] delen van het dialoogvenster zijn alleen zichtbaar wanneer u één project deelt.

   ![Het projectvenster Delen.](assets/share-proj-modal.png)

1. Voeg ontvangers of groepen ontvangers toe aan een van de opgegeven rolvelden:

   **Origineel bewerken:** Ontvangers kunnen **[!UICONTROL Save]** veranderingen in een project en functie als mede-eigenaars. Deze rol is nuttig als u een project met andere collega&#39;s wilt cobeheren; dit omvat het uitgeven, schrappen, en het wijzigen van ontvankelijke lijsten voor een gedeeld project. <br>Opmerking: Analysis Workspace biedt momenteel geen ondersteuning voor live samenwerken. Het wordt daarom aanbevolen dat slechts één gebruiker een project tegelijk bewerkt. Als projecten tegelijkertijd worden opgeslagen, blijft de laatste versie behouden.

   **Kopie bewerken:** Ontvangers kunnen **[!UICONTROL Save as]** en toegang hebben tot de linkerspoorstaaf. Projectinteracties zijn in deze rol niet beperkt. Deze rol is nuttig als u een project aan gebruikers wilt delen die de gegevens van uw organisatie en hoe te om Analysis Workspace begrijpen, maar u wilt niet uw project veranderen.

   **Alleen-lezen:** Ontvangers kunnen niet **[!UICONTROL Save]** of **[!UICONTROL Save as]** en hebben geen toegang tot de linkerspoorstaaf. De interactie tussen projecten is ook beperkt. Deze rol is nuttig als u een project aan gebruikers wilt delen die minder vertrouwd met de gegevensstructuur van uw organisatie, Analysis Workspace of Customer Journey Analytics over het algemeen zijn. U wilt echter nog steeds dat ze gegevens en inzichten in een veilige omgeving gebruiken. Meer informatie over de [Alleen-lezen ervaring met een project](/help/analysis-workspace/curate-share/view-only-projects.md).

1. (Voorwaardelijk) Als u één project deelt, kies of om de volgende opties toe te laten wanneer het delen van het project:

   * **Ingesloten projectcomponenten delen:** Deelt filters, berekende metriek, en datumwaaiers met alle ontvangers. Nadat deze componenten worden gedeeld, zullen deze in de drop-down Componenten van de Werkruimte van de ontvanger verschijnen. Deze instelling blijft niet bestaan. Het is een eenmalige actie op het moment van delen.

   * **Instellen als bestemmingspagina voor ontvangers:** Hiermee stelt u deze pagina in als de bestemmingspagina voor ontvangers. Deze instelling blijft niet bestaan. Het is een eenmalige actie op het moment van delen.

1. Selecteren **[!UICONTROL Share]**. (Als het project al is gedeeld, selecteert u [!UICONTROL **Bijwerken**].)

   of

   Selecteren **[!UICONTROL Curate and Share]** om automatisch projectcuratie toe te passen. (Als het project al is gedeeld, selecteert u **[!UICONTROL Curate & Update]**.) Meer informatie over [projectcursus](curate.md).

## Een koppeling naar een project delen

Houd rekening met het volgende wanneer u een koppeling deelt zoals wordt beschreven in deze sectie:

* Ontvangers die de koppeling gebruiken, moeten zich aanmelden bij de Customer Journey Analytics voordat ze toegang krijgen tot het project.

* Als aan een ontvanger geen rol wordt toegewezen en een ontvanger ontvangt [link](/help/analysis-workspace/curate-share/shareable-links.md) aan het project (**[!UICONTROL Share]>[!UICONTROL Get project link]**) krijgen ze standaard een rol toegewezen. Ontvangen beheerders **[!UICONTROL Edit original]** en niet-beheerders ontvangen **[!UICONTROL Edit copy]**.

De projectkoppeling delen met gebruikers in uw organisatie:

1. Sla het project op. Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd uw project op te slaan voordat u een koppeling deelt.

1. Selecteren **[!UICONTROL Share]** > **[!UICONTROL Share with Workspace users]** selecteert u vervolgens **[!UICONTROL Copy]** naast de **[!UICONTROL Share by link]** veld.

   ![Het project van het Aandeel benadrukkend het Aandeel door verbindingsgebied.](assets/share-proj-modal.png)

1. Deel de koppeling met gebruikers in uw organisatie. U kunt het bijvoorbeeld in een e-mail, op een interne website, enzovoort plakken.

## Een project delen met iedereen (geen aanmelding vereist) {#share-public-link}

U kunt [alleen-lezen toegang](/help/analysis-workspace/curate-share/view-only-projects.md) naar Analysis Workspace-projecten voor mensen die geen toegang hebben tot Customer Journey Analytics. Dit kan het volgende omvatten:

* Personen buiten uw organisatie

* Personen binnen uw organisatie die geen toegang hebben tot Customer Journey Analytics

>[!NOTE]
>
>Houd rekening met het volgende wanneer u een Analysis Workspace-project deelt met mensen die geen toegang hebben tot Customer Journey Analytics:
>
>* De capaciteit om een project op deze manier te delen kan door de beheerder van de Customer Journey Analytics worden onbruikbaar gemaakt, zoals die in [Voorkeuren](/help/analysis-workspace/user-preferences.md). Als u een project niet kunt delen zoals die in deze sectie wordt beschreven, heeft uw beheerder van de Customer Journey Analytics deze mogelijkheid onbruikbaar gemaakt.
>
>* Projecten met meer dan 50 uitgebreide visualisaties kunnen niet worden gedeeld met mensen die geen toegang tot Customer Journey Analytics hebben.
>
>* Gebruikers met wie u deelt, kunnen alle filters weergeven die tijdens het project op het project zijn toegepast [kromming](curate.md).
> 
>* Gebruikers met wie u deelt, kunnen het datumbereik van het project wijzigen. De datumwaaier u voor het project plaatst wordt getoond door gebrek.
>
>* Een project zou ontoegankelijk kunnen worden als vele gebruikers proberen om tot een bepaalde verbinding tezelfdertijd toegang te hebben. Standaard hebben meer dan 190 personen elke 5 minuten toegang tot één koppeling. Als uw organisatie deze limiet heeft bereikt, wacht u 5 minuten en probeert u de koppeling opnieuw te openen.
>
>* De [!UICONTROL Share with anyone] -functie is geblokkeerd voor zowel de licenties voor het Healthcare Shield als de &#39;Privacy &amp; Security Shield&#39;-licenties.

In de volgende videodemonstratie en de bijbehorende documentatie worden de opties beschreven voor het delen van een koppeling met iedereen:

>[!VIDEO](https://video.tv.adobe.com/v/3420093/?learn=on)

Een Analysis Workspace-project met iedereen delen:

1. Open het Analysis Workspace-project dat u wilt delen.

1. Klikken **[!UICONTROL Share]** > **[!UICONTROL Share with anyone]**.

   Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd uw project op te slaan.

   <!-- Add screen shot of new modal -->

1. De optie **[!UICONTROL Link is active]** als deze optie nog niet is ingeschakeld.

   Als u deze optie selecteert, wordt een koppeling naar het project gemaakt die met iedereen kan worden gedeeld. U kunt toegang tot het project op elk ogenblik onbruikbaar maken door deze optie onbruikbaar te maken.

   De eigenaar van het project is ook de eigenaar van deze verbinding. De eigendom van de koppeling kan alleen naar een andere gebruiker worden overgedragen wanneer de projecteigendom wordt overgedragen, zoals in [Gebruikerselementen overdragen of verlopen van account instellen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/user-product-management/users-assets.html) in de handleiding Analytics Admin.

1. Geef op of u de volgende beveiligingsoptie wilt inschakelen (deze optie kan worden beheerd door de beheerder van de Customer Journey Analytics):

   * **[!UICONTROL Require Experience Cloud authentication]:**

     Wanneer deze optie wordt toegelaten, zijn de enige gebruikers die tot het project kunnen toegang hebben degenen die login aan de organisatie van Adobe Experience Cloud kunnen zijn waar het project dat u deelt werd gecreeerd. Gebruikers met wie u deelt, hoeven echter geen toegang tot Adobe Analytics te hebben.

     De beheerders van de Customer Journey Analytics kunnen deze voorkeur voor het bedrijf vormen, zoals die in wordt beschreven [Voorkeuren](/help/analysis-workspace/user-preferences.md). U zou de volgende scenario&#39;s, afhankelijk van kunnen ontmoeten hoe de beheerder deze optie vormde:

      * Als deze optie niet zichtbaar is, heeft de beheerder van de Customer Journey Analytics deze functie niet ingeschakeld.

      * Als deze optie wordt toegelaten en u het niet kunt onbruikbaar maken, betekent dit dat uw beheerder van de Customer Journey Analytics Experience Cloud authentificatie voor iedereen vereist die tot de projecten van Analysis Workspace toegang heeft. Dit is altijd het geval voor organisaties die een vergunning hebben voor het gezondheidsschild.

1. Naast de **[!UICONTROL Share with anyone (no login required)]** veld, klikt u op de knop **Koppeling kopiëren** pictogram ![Koppelingspictogram kopiëren](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Link_18_N.svg)) om de koppeling naar het systeemklembord te kopiëren.

1. Deel de koppeling met de personen die u toegang tot het project wilt geven. U kunt de koppeling bijvoorbeeld in een e-mail plakken.

   Iedereen met wie u de koppeling deelt, kan het Analysis Workspace-project bekijken.

1. (Optioneel) U kunt op de knop **Nieuwe koppeling genereren** pictogram ![Koppelingspictogram genereren](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg) om toegang van gebruikers te verwijderen die eerder een verbinding aan het project ontvingen. Er wordt een nieuwe koppeling gegenereerd die u kunt delen met gebruikers die toegang willen krijgen tot het project.

1. Selecteren **[!UICONTROL Close]** om het dialoogvenster Delen te sluiten. Uw wijzigingen worden automatisch opgeslagen.

## Projecten weergeven die met u worden gedeeld

Wanneer iemand een project met u deelt door [delen van een specifieke projectrol](#share-a-specific-project-role), kunt u de gedeelde projecten openen vanuit de [Het tabblad Projecten van de landingspagina Analytics](/help/getting-started/landing.md#navigate-the-projects-tab).

Wanneer iemand een project met u deelt door een koppeling te delen (van de [Tabblad Project delen](#share-a-link-to-a-project) of met een [delen met koppeling voor iedereen](#share-a-project-with-anyone-no-login-required)), moet u de verbinding gebruiken die met u werd gedeeld om tot het project toegang te hebben. De koppeling kan bijvoorbeeld zijn gedeeld in een e-mail, op een interne website, enzovoort.

## Ingesloten componenten delen

Hier volgt een video over het onderwerp:

>[!VIDEO](https://video.tv.adobe.com/v/24713/?quality=12)

## Veelgestelde vragen {#FAQs}

| Vraag | Antwoord |
|---|---|
| Wat gebeurt er als twee editors tegelijkertijd een project opslaan? | De wijzigingen worden niet samengevoegd en de laatst opgeslagen projectversie blijft behouden. Analysis Workspace biedt momenteel geen ondersteuning voor live samenwerken. |
| Als beheerder, welke projectervaring zal ik zien? | Beheerders die in een **[!UICONTROL Edit copy]** of **[!UICONTROL Read only]** de rol zal deze beperkte ervaring opdoen wanneer zij een project openen . Indien gewenst kan een beheerder zijn rol verhogen tot **[!UICONTROL Edit original]** op elk moment **[!UICONTROL Components]>[!UICONTROL Projects]**. |
| Wat gebeurt er als een ontvanger in één rol als individu en een andere rol als lid van een groep wordt geplaatst? | Als een ontvanger in veelvoudige rollen wordt geplaatst, zullen zij altijd de hogere ervaring ontvangen. Als een ontvanger bijvoorbeeld de opdracht **[!UICONTROL Edit original]** als individu en **[!UICONTROL Can view]** als lid van een groep ontvangen zij een **[!UICONTROL Edit original]** ervaring met projecten. |
| Welke ervaring krijgt een ontvanger als hij of zij een projectverbinding opent? | Ontvangers krijgen de rol die u hen in de deelmodus hebt geplaatst. Als een ontvanger geen rol wordt toegewezen en een verbinding aan het project (**[!UICONTROL Share]** > **[!UICONTROL Share with Workspace users]** selecteert u vervolgens **[!UICONTROL Copy]** naast de **[!UICONTROL Share by link]** (veld), worden deze standaard in een rol geplaatst. Ontvangen beheerders **[!UICONTROL Edit original]** en niet-beheerders ontvangen **[!UICONTROL Edit copy]**. |
