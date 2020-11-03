---
description: Projectdeling en projectrollen in Workspace
keywords: Analysis Workspace sharing
title: Projecten delen
translation-type: tm+mt
source-git-commit: a991dce6abaf90cbca06de75606a2517cb5b6484
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 3%

---


# Projecten delen

>[!NOTE]
>
>U bekijkt de documentatie voor Analysis Workspace in Customer Journey Analytics. De functieset wijkt enigszins af van [Analysis Workspace in het traditionele Adobe Analytics](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

Door een project te delen, stelt u het beschikbaar voor andere Analysis Workspace-gebruikers in uw organisatie. Alle [kromming](curate.md) u hebt toegepast wordt weerspiegeld wanneer de ontvangers het project openen.

## Projectrollen {#Roles}

U kunt ontvangers aan één van drie projectrollen toevoegen. De rollen van het project zijn verbonden aan de gebruiker en specifieke projectidentiteitskaart De rollen van het project zijn onafhankelijk van gebruikerstoestemmingen die in [Adobe Experience Cloud-beheerconsole](https://docs.adobe.com/content/help/nl-NL/core-services/interface/manage-users-and-products/admin-getting-started.html).

| Rol | Projectbeheersing |
|---|---|
| Kan bewerken | Ontvangers kunnen **[!UICONTROL Save]** veranderingen in een project en functie als mede-eigenaars. Deze rol is nuttig als u een project met andere collega&#39;s wilt cobeheren; dit omvat het uitgeven, schrappen, en het wijzigen van ontvankelijke lijsten voor een gedeeld project. <br>Opmerking: Analysis Workspace biedt momenteel geen ondersteuning voor live samenwerken. Het wordt daarom aanbevolen dat slechts één gebruiker een project tegelijk bewerkt. Als projecten tegelijkertijd worden opgeslagen, blijft de laatste versie behouden. |
| Kan dupliceren | Ontvangers kunnen **[!UICONTROL Save as]** en toegang hebben tot de linkerspoorstaaf. Projectinteracties zijn in deze rol niet beperkt. Deze rol is nuttig als u een project aan gebruikers wilt delen die de gegevens van uw organisatie en hoe te om Analysis Workspace begrijpen, maar u wilt niet uw project veranderen. |
| Kan worden weergegeven | Ontvangers kunnen niet Opslaan als en hebben geen toegang tot de linkerrail. De interactie tussen projecten is ook beperkt. Deze rol is handig als u een project wilt delen met gebruikers die minder bekend zijn met de gegevensstructuur van uw organisatie, Analysis Workspace of Adobe Analytics in het algemeen. U wilt echter nog steeds dat ze gegevens en inzichten in een veilige omgeving gebruiken.<br>Meer informatie over de [Kan projectervaring bekijken](/help/analysis-workspace/curate-share/view-only-projects.md). |

>[!IMPORTANT]
> De begunstigden van projecten die vóór 18 juni 2020 werden toegevoegd, zijn gemigreerd naar een projectrol. Gebruikers van Admin die zijn gemigreerd naar de **[!UICONTROL Can edit]** rol en gebruikers die niet-beheerder zijn, zijn gemigreerd naar de **[!UICONTROL Can duplicate]** rol. Deze rollen verstrekken de zelfde projectervaring die zij eerder hadden. Bovendien zijn alle groepen (inclusief &quot;Alle&quot;) naar de **[!UICONTROL Can duplicate]** rol.

### Geen rol toegewezen (ontvangers projectkoppeling)

Als aan een ontvanger geen rol wordt toegewezen en een ontvanger ontvangt [link](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/shareable-links.html) aan het project (**[!UICONTROL Share]>[!UICONTROL Get project link]**), worden ze standaard in een rol geplaatst. Ontvangen beheerders **[!UICONTROL Can edit]** en niet-beheerders ontvangen **[!UICONTROL Can duplicate]**.

### Meerdere rollen toegewezen

Als een ontvanger in veelvoudige rollen wordt geplaatst, zullen zij altijd de hoogste ervaring krijgen. Dit kan voorkomen als een ontvanger zowel als individu als deel van een groep wordt toegevoegd. Als een ontvanger bijvoorbeeld de opdracht **[!UICONTROL Can edit]** als individu en **[!UICONTROL Can view]** als lid van een groep ontvangen zij een **[!UICONTROL Can edit]** ervaring met projecten.

### Beheerders en rollen

Beheerders die in een **[!UICONTROL Can duplicate]** of **[!UICONTROL Can view]** de rol zal deze beperkte ervaring opdoen wanneer zij een project openen . Indien gewenst kan een beheerder zijn rol verhogen tot **[!UICONTROL Can edit]** op elk moment **[!UICONTROL Components]>[!UICONTROL Projects]**.

## Ontvangers toevoegen aan gedeeld project {#Add}

Om ontvangers aan uw gedeelde project toe te voegen:

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Share project]**.
Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd eerst uw project op te slaan.
1. Voeg ontvangers of groepen ontvangers toe.
Verwijs naar het hulppictogram bij de bovenkant voor beschrijvingen van elke rol.
1. (Optioneel) Deel ingesloten projectcomponenten (segmenten, berekende metriek en datumbereiken) met alle ontvangers.
Nadat deze componenten worden gedeeld, zullen deze in de drop-down Componenten van de Werkruimte van de ontvanger verschijnen. Deze instelling blijft niet bestaan, het is een enkelvoudige actie op het moment van delen.
1. (Optioneel) Stel deze pagina in als de bestemmingspagina voor ontvangers.
Deze instelling blijft niet bestaan. Het is een enkelvoudige actie op het moment van delen.
1. Klik op Delen.
U kunt ook op **[!UICONTROL Curate and Share]** om automatisch projectcuratie toe te passen. Als een project reeds is gedeeld, zullen deze knopen zeggen **[!UICONTROL Update]** en **[!UICONTROL Curate & Update]**. Meer informatie over [projectcursus](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/curate.html).

![](assets/share-proj-modal.png)

## Delen naar groepen ontvangers {#Groups}

Alle gebruikers kunnen projecten aan groepen delen, die een inzameling van ontvangers zijn. In Adobe Analytics worden groepen gedefinieerd op basis van productprofielen in de [Adobe Experience Cloud-beheerconsole](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html).

* Beheerders kunnen gegevens delen met elke groep, inclusief Alles.
* Niet-beheerders kunnen delen met groepen waarvan zij lid zijn, met uitzondering van &quot;Alle&quot;.

## Een projectkoppeling delen {#Links}

U kunt een koppeling krijgen naar een project onder **[!UICONTROL Share]>[!UICONTROL Get project link]**. Wanneer geklikt, zullen de ontvangers worden vereist om login alvorens in het project te landen. Als de ontvanger niet in een rol is geplaatst, zullen zij een standaardrol ontvangen. Ontvangen beheerders **[!UICONTROL Can edit]** en niet-beheerders ontvangen **[!UICONTROL Can duplicate]**. [Meer informatie](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/shareable-links.html) informatie over het maken van deelbare koppelingen naar Workspace-projecten.

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
| Als beheerder, welke projectervaring zal ik zien? | Beheerders die in een **[!UICONTROL Can duplicate]** of **[!UICONTROL Can view]** de rol zal deze beperkte ervaring opdoen wanneer zij een project openen . Indien gewenst kan een beheerder zijn rol verhogen tot **[!UICONTROL Can edit]** op elk moment **[!UICONTROL Components]>[!UICONTROL Projects]**. |
| Wat gebeurt er als een ontvanger in één rol als individu en een andere rol als lid van een groep wordt geplaatst? | Als een ontvanger in veelvoudige rollen wordt geplaatst, zullen zij altijd de hogere ervaring ontvangen. Als een ontvanger bijvoorbeeld de opdracht **[!UICONTROL Can edit]** als individu en **[!UICONTROL Can view]** als lid van een groep ontvangen zij een **[!UICONTROL Can edit]** ervaring met projecten. |
| Welke ervaring krijgt een ontvanger als deze een projectverbinding opent? | Ontvangers krijgen de rol die u hen in de deelmodus hebt geplaatst. Als aan een ontvanger geen rol wordt toegewezen en een koppeling naar het project wordt ontvangen (**[!UICONTROL Share]>[!UICONTROL Get project link]**), worden ze standaard in een rol geplaatst. Ontvangen beheerders **[!UICONTROL Can edit]** en niet-beheerders ontvangen **[!UICONTROL Can duplicate]**. |
