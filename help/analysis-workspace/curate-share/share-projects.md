---
description: Projectdeling en projectrollen in Workspace
keywords: Analysis Workspace sharing
title: Werkruimteprojecten delen
translation-type: tm+mt
source-git-commit: 92dfb091a004ca7403f67e3f16527ea1e39cd01a
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 3%

---


# Werkruimteprojecten delen

>[!NOTE] U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van die van [Analysis Workspace in traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Door een project te delen, stelt u het beschikbaar voor andere Analysis Workspace-gebruikers in uw organisatie. Elke [curatie](curate.md) die u hebt toegepast, wordt weerspiegeld wanneer ontvangers het project openen.

## Projectrollen {#Roles}

U kunt ontvangers aan één van drie projectrollen toevoegen. De rollen van het project zijn verbonden aan de gebruiker en specifieke projectidentiteitskaart Projectrollen zijn onafhankelijk van gebruikersmachtigingen die worden beheerd in de beheerconsole [van de](https://docs.adobe.com/content/help/nl-NL/core-services/interface/manage-users-and-products/admin-getting-started.html)Adobe Experience Cloud.

| Rol | Projectbeheersing |
|---|---|
| Kan bewerken | Ontvangers kunnen wijzigingen in een project opslaan en als medeeigenaars fungeren. Deze rol is nuttig als u projecten met andere collega&#39;s wilt couitgeven.<br>Opmerking: Analysis Workspace biedt momenteel geen ondersteuning voor live samenwerken. Het wordt daarom aanbevolen dat slechts één gebruiker een project tegelijk bewerkt. Als projecten tegelijkertijd worden opgeslagen, blijft de laatste versie behouden. |
| Kan dupliceren | Ontvangers kunnen Opslaan als en toegang hebben tot de linkerrail. Projectinteracties zijn in deze rol niet beperkt. Deze rol is nuttig als u een project aan gebruikers wilt delen die de gegevens van uw organisatie en hoe te om Analysis Workspace begrijpen, maar u wilt niet uw project veranderen. |
| Kan worden weergegeven | Ontvangers kunnen niet Opslaan als en hebben geen toegang tot de linkerrail. De interactie tussen projecten is ook beperkt. Deze rol is handig als u een project wilt delen met gebruikers die minder bekend zijn met de gegevensstructuur van uw organisatie, Analysis Workspace of Adobe Analytics in het algemeen. U wilt echter nog steeds dat ze gegevens en inzichten in een veilige omgeving gebruiken.<br>Meer informatie over [Kan projectervaring](/help/analysis-workspace/curate-share/view-only-projects.md)bekijken. |

### Geen rol toegewezen

Als een ontvanger geen rol wordt toegewezen en een verbinding aan het project (**[!UICONTROL Share]>[!UICONTROL Get project link]**) ontvangt, zullen zij in de **[!UICONTROL Can view]**rol door gebrek worden geplaatst.

### Meerdere rollen toegewezen

Als een ontvanger in veelvoudige rollen wordt geplaatst, zullen zij altijd de hoogste ervaring krijgen. Dit kan voorkomen als een gebruiker zowel als individu als deel van een groep wordt toegevoegd. Bijvoorbeeld, als een gebruiker de **[!UICONTROL Can edit]** rol als individu en de **[!UICONTROL Can view]** rol als lid van een groep wordt gegeven, zullen zij een **[!UICONTROL Can edit]** projectervaring ontvangen.

### Beheerders en rollen

Beheerders die in een **[!UICONTROL Can duplicate]** of **[!UICONTROL Can view]** rol zijn geplaatst, krijgen die beperkte ervaring wanneer ze een project openen. Indien gewenst kan een beheerder zijn rol op elk gewenst moment **[!UICONTROL Can edit]** via **[!UICONTROL Components]>[!UICONTROL Projects]**verhogen.

## Ontvangers toevoegen aan gedeeld project {#Add}

Om ontvangers aan uw gedeelde project toe te voegen:

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Share project]**.
Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd eerst uw project op te slaan.
1. Voeg ontvangers of groepen gebruikers toe.
Verwijs naar het hulppictogram bij de bovenkant voor beschrijvingen van elke rol.
1. (Optioneel) Deel ingesloten projectcomponenten (segmenten, berekende metriek en datumbereiken) met alle ontvangers.
Nadat deze componenten worden gedeeld, zullen deze in de drop-down Componenten van de Werkruimte van de ontvanger verschijnen. Deze instelling blijft niet bestaan, het is een enkelvoudige actie op het moment van delen.
1. (Optioneel) Stel deze pagina in als de bestemmingspagina voor ontvangers.
Deze instelling blijft niet bestaan. Het is een enkelvoudige actie op het moment van delen.
1. Klik op Delen.
U kunt ook klikken **[!UICONTROL Curate and Share]** om de projectcuratie automatisch toe te passen. Als een project reeds is gedeeld, zullen deze knopen zeggen **[!UICONTROL Update]** en **[!UICONTROL Curate & Update]**. Meer informatie over [projectcuratie](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html).

![](assets/share-proj-modal.png)

## Delen naar groepen ontvangers {#Groups}

Alle gebruikers kunnen projecten aan groepen delen, die een inzameling van ontvangers zijn. In Adobe Analytics worden groepen gedefinieerd op basis van productprofielen in de beheerconsole [](https://docs.adobe.com/content/help/nl-NL/core-services/interface/manage-users-and-products/admin-getting-started.html)van Adobe Experience Cloud.

* Beheerders kunnen gegevens delen met elke groep, inclusief Alles.
* Niet-beheerders kunnen delen met groepen waarvan zij lid zijn, met uitzondering van &quot;Alle&quot;.

## Projecten delen in de projectmanager {#Manager}

Projecten kunnen ook worden gedeeld vanuit **[!UICONTROL Components]>[!UICONTROL Projects]**. U kunt één project delen volgens dezelfde stappen hierboven.

Als de veelvoudige projecten worden geselecteerd om worden gedeeld, zullen de ontvangers aan de bestaande lijst van ontvangers voor elk project worden toegevoegd. Bijvoorbeeld:

* Project A wordt gedeeld aan gebruikers 1, 2, 3
* Project B wordt gedeeld aan gebruiker 4, 5, 6
* Met Project A en B geselecteerd, worden gebruikers 4 en 7 toegevoegd aan de ontvankelijke lijsten. De nieuwe lijst van ontvangers voor elk project is nu:
   * Project A: 1, 2, 3, 4, 7
   * Project B: 4, 5, 6, 7
   ![](assets/mult-proj-sharing.png)

## FAQs {#FAQs}

| Vraag | Antwoord |
|---|---|
| Wat gebeurt er als twee editors tegelijkertijd een project opslaan? | De wijzigingen worden niet samengevoegd en de laatst opgeslagen projectversie blijft behouden. Analysis Workspace biedt momenteel geen ondersteuning voor live samenwerken. |
| Als beheerder, welke projectervaring zal ik zien? | Beheerders die in een **[!UICONTROL Can duplicate]** of **[!UICONTROL Can view]** rol zijn geplaatst, krijgen die beperkte ervaring wanneer ze een project openen. Indien gewenst kan een beheerder zijn rol op elk gewenst moment **[!UICONTROL Can edit]** via **[!UICONTROL Components]>[!UICONTROL Projects]**verhogen. |
| Wat gebeurt er als een gebruiker in één rol als individu en een andere rol als lid van een groep wordt geplaatst? | Als een ontvanger in veelvoudige rollen wordt geplaatst, zullen zij altijd de hogere ervaring ontvangen. Bijvoorbeeld, als een gebruiker de **[!UICONTROL Can edit]** rol als individu en de **[!UICONTROL Can view]** rol als lid van een groep wordt gegeven, zullen zij een **[!UICONTROL Can edit]** projectervaring ontvangen. |
| Waarom ontvangt een gebruiker een mening-slechts ervaring wanneer zij een projectverbinding krijgen? | Als een ontvanger geen rol wordt toegewezen en een verbinding aan het project (**[!UICONTROL Share]>[!UICONTROL Get project link]**) ontvangt, zullen zij in de **[!UICONTROL Can view]**rol door gebrek worden geplaatst. Als de gebruiker een verhoogde projectrol zou willen, kan de projecteigenaar of de redacteur hen toevoegen aan kunnen dupliceren of rol door het project uitgeven deelmodaal. |
