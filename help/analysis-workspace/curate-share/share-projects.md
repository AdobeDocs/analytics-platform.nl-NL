---
description: Projectdeling en projectrollen in Workspace
keywords: Analysis Workspace delen
title: Projecten delen
exl-id: ac4ed73a-e890-46cc-be08-4ccedf66b47d
source-git-commit: 8cee89a8ed656ad6376e64c8327aa7c94a937ce9
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 0%

---

# Projecten delen

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset verschilt enigszins van [Analysis Workspace in traditionele Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Door een project te delen, stelt u het beschikbaar voor andere Analysis Workspace-gebruikers in uw organisatie. Elke [curatie](curate.md) die u hebt toegepast, wordt weerspiegeld wanneer ontvangers het project openen.

## Projectrollen {#Roles}

U kunt ontvangers aan één van drie projectrollen toevoegen. De rollen van het project zijn verbonden aan de gebruiker en specifieke projectidentiteitskaart Projectrollen zijn onafhankelijk van gebruikersmachtigingen die worden beheerd in de [Adobe Experience Cloud-beheerconsole](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

| Rol | Projectbeheersing |
|---|---|
| Kan bewerken | Ontvangers kunnen **[!UICONTROL Save]** in een project veranderen en als mede-eigenaars functioneren. Deze rol is nuttig als u een project met andere collega&#39;s wilt cobeheren; dit omvat het uitgeven, schrappen, en het wijzigen van ontvankelijke lijsten voor een gedeeld project. <br>Opmerking: Analysis Workspace biedt momenteel geen ondersteuning voor live samenwerken. Het wordt daarom aanbevolen dat slechts één gebruiker een project tegelijk bewerkt. Als projecten tegelijkertijd worden opgeslagen, blijft de laatste versie behouden. |
| Kan dupliceren | Ontvangers kunnen **[!UICONTROL Save as]** en de linkerrail gebruiken. Projectinteracties zijn in deze rol niet beperkt. Deze rol is nuttig als u een project aan gebruikers wilt delen die de gegevens van uw organisatie en hoe te om Analysis Workspace begrijpen, maar u wilt niet uw project veranderen. |
| Kan worden weergegeven | Ontvangers kunnen niet Opslaan als en hebben geen toegang tot de linkerrail. De interactie tussen projecten is ook beperkt. Deze rol is nuttig als u een project aan gebruikers wilt delen die minder vertrouwd met de gegevensstructuur van uw organisatie, Analysis Workspace of Customer Journey Analytics over het algemeen zijn. U wilt echter nog steeds dat ze gegevens en inzichten in een veilige omgeving gebruiken.<br>Meer informatie over  [Kan projectervaring](/help/analysis-workspace/curate-share/view-only-projects.md) bekijken. |

>[!IMPORTANT]
> De begunstigden van projecten die vóór 18 juni 2020 werden toegevoegd, zijn gemigreerd naar een projectrol. Admin-gebruikers migreerden naar de rol **[!UICONTROL Can edit]** en gebruikers zonder beheer migreerden naar de rol **[!UICONTROL Can duplicate]**. Deze rollen verstrekken de zelfde projectervaring die zij eerder hadden. Bovendien zijn alle groepen (inclusief &quot;Alles&quot;) gemigreerd naar de rol **[!UICONTROL Can duplicate]**.

### Geen rol toegewezen (ontvangers projectkoppeling)

Als een ontvanger geen rol wordt toegewezen en een [link](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html) aan het project (**[!UICONTROL Share]>[!UICONTROL Get project link]**) ontvangt, zullen zij in een rol door gebrek worden geplaatst. Beheerders ontvangen **[!UICONTROL Can edit]** en niet-beheerders ontvangen **[!UICONTROL Can duplicate]**.

### Meerdere rollen toegewezen

Als een ontvanger in veelvoudige rollen wordt geplaatst, zullen zij altijd de hoogste ervaring krijgen. Dit kan voorkomen als een ontvanger zowel als individu als deel van een groep wordt toegevoegd. Bijvoorbeeld, als een ontvanger de **[!UICONTROL Can edit]** rol als individu en **[!UICONTROL Can view]** rol als lid van een groep wordt gegeven, zullen zij een **[!UICONTROL Can edit]** projectervaring ontvangen.

### Beheerders en rollen

Beheerders die in een **[!UICONTROL Can duplicate]**- of **[!UICONTROL Can view]**-rol worden geplaatst, krijgen die beperkte ervaring wanneer ze een project openen. Indien gewenst kan een beheerder zijn rol op elk moment tot **[!UICONTROL Can edit]** via **[!UICONTROL Components]>[!UICONTROL Projects]** vergroten.

## Ontvangers toevoegen aan gedeeld project {#Add}

Om ontvangers aan uw gedeelde project toe te voegen:

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Share project]**.
Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd eerst uw project op te slaan.
1. Voeg ontvangers of groepen ontvangers toe.
Verwijs naar het hulppictogram bij de bovenkant voor beschrijvingen van elke rol.
1. (Optioneel) Deel ingesloten projectcomponenten (filters, berekende meetgegevens en datumbereiken) met alle ontvangers.
Nadat deze componenten worden gedeeld, zullen deze in de drop-down Componenten van de Werkruimte van de ontvanger verschijnen. Deze instelling blijft niet bestaan, het is een enkelvoudige actie op het moment van delen.
1. (Optioneel) Stel deze pagina in als de bestemmingspagina voor ontvangers.
Deze instelling blijft niet bestaan. Het is een enkelvoudige actie op het moment van delen.
1. Klik op Delen.
U kunt **[!UICONTROL Curate and Share]** ook klikken om projectcuratie automatisch toe te passen. Als een project reeds is gedeeld, zullen deze knopen **[!UICONTROL Update]** en **[!UICONTROL Curate & Update]** zeggen. Meer informatie over [projectcuratie](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html).

![](assets/share-proj-modal.png)

## Delen naar groepen ontvangers {#Groups}

Alle gebruikers kunnen projecten aan groepen delen, die een inzameling van ontvangers zijn. In Customer Journey Analytics worden groepen gedefinieerd door productprofielen in de [Adobe Experience Cloud-beheerconsole](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

* Beheerders kunnen gegevens delen met elke groep, inclusief Alles.
* Niet-beheerders kunnen delen met groepen waarvan zij lid zijn, met uitzondering van &quot;Alle&quot;.

## Een projectkoppeling delen {#Links}

U kunt een verbinding een project onder **[!UICONTROL Share]>[!UICONTROL Get project link]** krijgen. Wanneer geklikt, zullen de ontvangers worden vereist om login alvorens in het project te landen. Als de ontvanger niet in een rol is geplaatst, zullen zij een standaardrol ontvangen. Beheerders ontvangen **[!UICONTROL Can edit]** en niet-beheerders ontvangen **[!UICONTROL Can duplicate]**. [Leer ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html) meer over het creëren van deelbare verbindingen aan de projecten van de Werkruimte.

## Projecten delen in de projectmanager {#Manager}

Projecten kunnen ook worden gedeeld vanuit **[!UICONTROL Components]>[!UICONTROL Projects]**. U kunt één project delen volgens dezelfde stappen hierboven.  Als de veelvoudige projecten worden geselecteerd om worden gedeeld, zullen de ontvangers aan de bestaande lijst van ontvangers voor elk project worden toegevoegd.

Bijvoorbeeld:

* Project A wordt gedeeld aan ontvangers 1, 2, 3
* Project B wordt gedeeld aan ontvangers 4, 5, 6

Als Project A en B zijn geselecteerd, worden ontvangers 4 en 7 toegevoegd aan de aandelenlijsten. De nieuwe lijst van het aandeel voor elk project is nu:

* Project A: 1, 2, 3, 4, 7
* Project B: 4, 5, 6, 7

![](assets/mult-proj-sharing.png)

## Veelgestelde vragen {#FAQs}

| Vraag | Antwoord |
|---|---|
| Wat gebeurt er als twee editors tegelijkertijd een project opslaan? | De wijzigingen worden niet samengevoegd en de laatst opgeslagen projectversie blijft behouden. Analysis Workspace biedt momenteel geen ondersteuning voor live samenwerken. |
| Als beheerder, welke projectervaring zal ik zien? | Beheerders die in een **[!UICONTROL Can duplicate]**- of **[!UICONTROL Can view]**-rol worden geplaatst, krijgen die beperkte ervaring wanneer ze een project openen. Indien gewenst kan een beheerder zijn rol op elk moment tot **[!UICONTROL Can edit]** via **[!UICONTROL Components]>[!UICONTROL Projects]** vergroten. |
| Wat gebeurt er als een ontvanger in één rol als individu en een andere rol als lid van een groep wordt geplaatst? | Als een ontvanger in veelvoudige rollen wordt geplaatst, zullen zij altijd de hogere ervaring ontvangen. Bijvoorbeeld, als een ontvanger de **[!UICONTROL Can edit]** rol als individu en **[!UICONTROL Can view]** rol als lid van een groep wordt gegeven, zullen zij een **[!UICONTROL Can edit]** projectervaring ontvangen. |
| Welke ervaring krijgt een ontvanger als deze een projectverbinding opent? | Ontvangers krijgen de rol die u hen in de deelmodus hebt geplaatst. Als een ontvanger geen rol wordt toegewezen en een verbinding aan het project (**[!UICONTROL Share]>[!UICONTROL Get project link]**) ontvangt, zullen zij in een rol door gebrek worden geplaatst. Beheerders ontvangen **[!UICONTROL Can edit]** en niet-beheerders ontvangen **[!UICONTROL Can duplicate]**. |
