---
description: Gebruik intelligente bijschriften om inzichten in de natuurlijke taal te genereren voor oppervlaktetrends binnen visualisaties.
title: Intelligente bijschriften
feature: Visualizations
exl-id: d32d3cda-ecbf-4ee7-a8b7-7c3c71b5df75
role: User
source-git-commit: de0eca21fa1b4ac71a8273676e851b596cf911a8
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Intelligente bijschriften {#intelligent-captions}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_intelligentcaptions_area"
>title="Intelligente bijschriften: gebied"
>abstract="Inzichten in de vorm van natuurlijke talen genereren om u te helpen gegevens voor deze visualisatie eenvoudiger te begrijpen en te interpreteren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_intelligentcaptions_bar"
>title="Intelligente bijschriften: balk"
>abstract="Inzichten in de vorm van natuurlijke talen genereren om u te helpen gegevens voor deze visualisatie eenvoudiger te begrijpen en te interpreteren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_intelligentcaptions_donut"
>title="Intelligente bijschriften: Donut"
>abstract="Inzichten in de vorm van natuurlijke talen genereren om u te helpen gegevens voor deze visualisatie eenvoudiger te begrijpen en te interpreteren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_intelligentcaptions_horizontalbar"
>title="Intelligente bijschriften: horizontale balk"
>abstract="Inzichten in de vorm van natuurlijke talen genereren om u te helpen gegevens voor deze visualisatie eenvoudiger te begrijpen en te interpreteren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_intelligentcaptions_line"
>title="Intelligente bijschriften: Lijn"
>abstract="Inzichten in de vorm van natuurlijke talen genereren om u te helpen gegevens voor deze visualisatie eenvoudiger te begrijpen en te interpreteren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_intelligentcaptions_fallout"
>title="Intelligente bijschriften: Uitvallen"
>abstract="Inzichten in de vorm van natuurlijke talen genereren om u te helpen gegevens voor deze visualisatie eenvoudiger te begrijpen en te interpreteren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_intelligentcaptions_flow"
>title="Intelligente bijschriften: Stroom"
>abstract="Inzichten in de vorm van natuurlijke talen genereren om u te helpen gegevens voor deze visualisatie eenvoudiger te begrijpen en te interpreteren."

<!-- markdownlint-enable MD034 -->

Intelligente bijschriften maken gebruik van geavanceerde Machine Learning en Generative AI om waardevolle natuurlijke taalinzichten te bieden voor Workspace-visualisaties. De aanvankelijke versie verstrekt auto-geproduceerde inzichten voor de [ visualisatie van de Lijn ](line.md). Er volgen nog andere visualisaties.

Intelligente bijschriften zijn gericht op:

* Analysten, die verhalen nodig hebben om met andere gebruikers te delen. De analisten hebben deze inzichten nodig om context aan hun gebruikers te kunnen verstrekken.
* Zakelijke gebruikers, die snel op hoog niveau willen ontdekken.

## Intelligente bijschriften starten {#launch}

Om auto-geproduceerde titels voor een lijnvisualisatie te lanceren, selecteer ![ AEMScreen ](/help/assets/icons/AI.svg) **[!UICONTROL Intelligent captions]** bij het hoogste recht van de visualisatie.

![ het venster van de Analyse van de Lancering die de Intelligente titels voor de Trend van de Kijken van het Product toont. ](assets/intell-caps-1.png)

Inzichten in natuurlijke talen worden nu gegenereerd.

Houd er rekening mee dat:

* U hebt minimaal drie gegevenspunten nodig om bijschriften te kunnen genereren. Anders krijgt u mogelijk een fout zoals **[!UICONTROL Not enough data to analyze]** .

* Bijschriften worden telkens gegenereerd wanneer de onderliggende geselecteerde gegevens veranderen in de tabel die de visualisatie beïnvloedt.

* Als de tabel meerdere metriek bevat, worden alleen bijschriften gegenereerd voor de eerste metrische waarde of voor de metrische waarde die momenteel door de gebruiker is geselecteerd.

* Als u het project op een specifiek punt opslaat en het later opnieuw laadt, worden de bijschriften automatisch bijgewerkt met nieuwe gegevens. Hetzelfde geldt voor geplande projecten en PDF-bestanden die uit een project worden geëxporteerd.

Hier is een voorbeeld van hoe intelligente bijschriften eruit zouden kunnen zien:

![ Intelligente titels voor de visualisatie van de Lijn met inbegrip van Seizoensonaliteit, Min, Max, Spiek, en Weigeren.](assets/captions.png)

## Handelingen

U kunt de volgende handelingen uitvoeren op intelligente bijschriften:

### Kopiëren naar klembord {#copy}

U kunt de bijschriften naar een klembord kopiëren en ze in een PowerPoint of andere gereedschappen plakken. Selecteer ![ titels van het Exemplaar aan klembord ](/help/assets/icons/Copy.svg) bij het hoogste recht van de dialoog van titels.

### Weergave bewerken {#edit}

U kunt de weergave van bijschriften bewerken, zoals een bepaalde categorie inzichten verbergen of verbergen.

1. Selecteer ![ uitgeven intelligente vertoning van titels ](/help/assets/icons/EditInLight.svg) in de Intelligente dialoog van titels.

1. Wissel tussen ![ Zichtbaarheid ](/help/assets/icons/Visibility.svg) om een specifiek inzicht (als **[!UICONTROL Min]**) te tonen, of ![ VisibilityOff ](/help/assets/icons/VisibilityOff.svg) om een specifiek inzicht (als **[!UICONTROL Spike]**) te verbergen.

   ![ geef intelligente titels ](assets/edit-intelligent-captions.png) uit

1. Selecteer **[!UICONTROL Apply]** .


### Feedback geven

U kunt feedback geven over de gegenereerde intelligente bijschriften.

1. Selecteer ![ Meer acties ](/help/assets/icons/More.svg) in de Intelligente dialoog van titels.

1. Selecteer ![ Goede reactie ](/help/assets/icons/ThumbUpOutline.svg) **[!UICONTROL Good response]**, ![ ThumbDownOutline ](/help/assets/icons/ThumbDownOutline.svg) **[!UICONTROL Bad response]**, of ![ Vlag ](/help/assets/icons/Flag.svg) **[!UICONTROL Report]**.

1. Geef in het dialoogvenster **[!UICONTROL Thank you for your feedback]** uw feedback op en selecteer **[!UICONTROL Submit]** om de feedback te verzenden.

### Exporteren {#export}

U kunt intelligente titels als deel van een PDF uitvoeren, zolang het project met de intelligente geproduceerde titels wordt bewaard.

### Uitschakelen {#toggle}

Als u liever geen intelligente bijschriften wilt weergeven, schakelt u de functie uit.

1. Ga naar [ de voorkeur van Visualisaties ](/help/analysis-workspace/user-preferences.md#visualizations-preferences).
1. Schakel **[!UICONTROL Show intelligent captions]** uit.

   ![ de visualisatieopties van de Lijn die de optie tonen om intelligente titels uit te schakelen.](assets/toggle-captions.png)

1. Selecteer **[!UICONTROL Save]** om de voorkeur op te slaan.


## Intelligente bijschriften in mobiele scoreborden

De intelligente titels zijn ook beschikbaar in Customer Journey Analytics [ mobiele scorecards ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dashboards/manage-scorecard#captions).

## Toegang tot functies

De volgende parameters regelen de toegang tot intelligente bijschriften:

* **toegang van de Oplossing**: De Intelligente eigenschap van titels is beschikbaar in Customer Journey Analytics, maar niet in Adobe Analytics.

* **Contractuele toegang**: Als u geen Intelligente titels kunt gebruiken, gelieve de beheerder van uw organisatie of de Vertegenwoordiger van de Rekening van de Adobe te contacteren. Voordat u Intelligente bijschriften kunt gebruiken in uw organisatie, moet u akkoord gaan met bepaalde juridische voorwaarden die betrekking hebben op GenAI.

* **Toestemmingen**: In [!UICONTROL Adobe Admin Console], bepaalt de [!UICONTROL Reporting Tools] **[!UICONTROL Intelligent Captions]** toestemming toegang. Admin van het a [ productprofiel ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) moet deze stappen in [!UICONTROL Admin Console] volgen:
   1. Navigeer naar **[!UICONTROL Admin Console]** > **[!UICONTROL Products and services]** > **[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Product Profiles]** .
   1. Selecteer de titel van het productprofiel waarvoor u toegang tot de Intelligente bijschriften wilt verlenen.
   1. Selecteer **[!UICONTROL Permissions]** in het specifieke productprofiel.
   1. Selecteer ![ uitgeven ](/help/assets/icons/Edit.svg) om uit te geven **[!UICONTROL Reporting Tools]**.
   1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) om **Intelligente Bijschriften** aan **[!UICONTROL Included permission items]** toe te voegen.

      ![ voeg toestemming ](./assets/intelligent-captions-permissions.png) toe

   1. Selecteer **[!UICONTROL Save]** om de machtigingen op te slaan.

Zie [ controle van de Toegang ](/help/technotes/access-control.md#access-control) voor meer informatie.
