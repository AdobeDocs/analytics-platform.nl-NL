---
description: Gebruik intelligente bijschriften om inzichten in de natuurlijke taal te genereren en trends snel binnen de visualisaties te laten overkomen.
title: Intelligente bijschriften
feature: Visualizations
exl-id: d32d3cda-ecbf-4ee7-a8b7-7c3c71b5df75
role: User
source-git-commit: dae2282717d5d84862259d5b056fbfeb2d068cce
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Intelligente bijschriften

Intelligente bijschriften maken gebruik van geavanceerde Machine Learning en Generative AI om waardevolle natuurlijke taalinzichten te bieden voor Workspace-visualisaties. De aanvankelijke versie verstrekt auto-geproduceerde inzichten voor de [ visualisatie van de Lijn ](line.md). Er volgen nog andere visualisaties.

Intelligente bijschriften zijn gericht op:

* Analysten die verhalen nodig hebben om met andere gebruikers te delen. De analisten hebben deze inzichten nodig om context aan hun gebruikers te kunnen verstrekken.
* Zakelijke gebruikers die snel op hoog niveau willen ontdekken.

Bijschriften zijn beschikbaar voor alle gebruikers van de Customer Journey Analytics en vereisen geen speciale machtigingen.

## Intelligente bijschriften starten {#launch}

Als u automatisch gegenereerde bijschriften wilt starten voor lijnvisualisatie, klikt u op het pictogram **[!UICONTROL Intelligent captions]** rechtsboven in de visualisatie.

![ het venster van de Analyse van de Lancering die de Intelligente titels voor de Trend van de Kijken van het Product toont. ](assets/intell-caps-1.png)

Inzichten in natuurlijke talen worden nu gegenereerd.

Houd rekening met het volgende:

* U hebt minimaal drie gegevenspunten nodig om bijschriften te kunnen genereren. Anders krijgt u mogelijk een fout met de tekst &quot;Onvoldoende gegevens om te analyseren.&quot;

* Bijschriften worden telkens gegenereerd wanneer de onderliggende geselecteerde gegevens in de tabel veranderen waardoor de visualisatie wordt ingeschakeld.

* Als de tabel meerdere metriek bevat, worden alleen bijschriften gegenereerd voor de eerste metrische waarde of voor de metrische waarde die momenteel door de gebruiker is geselecteerd.

* Als u het project op dit punt opslaat en het later opnieuw laadt, worden de bijschriften automatisch bijgewerkt met nieuwe gegevens. Hetzelfde geldt voor geplande projecten en PDF-bestanden die uit dit project worden geëxporteerd.

## Bijschriften weergeven en interpreteren {#view}

Hier volgt een voorbeeld van hoe de bijschriften eruit zouden kunnen zien:

![ Intelligente titels voor de visualisatie van de Lijn met inbegrip van Seizoensonaliteit, Min, Max, Spiek, en Weigeren.](assets/captions.png)

## Kopiëren naar klembord {#copy}

U kunt de bijschriften naar een klembord kopiëren en ze in een PowerPoint of andere gereedschappen plakken. Selecteer ![ titels van het Exemplaar aan klembord ](/help/assets/icons/Copy.svg) bij het hoogste recht van de dialoog van titels.

## Bijschriften bewerken {#edit}

U kunt de bijschriften bewerken, zoals een bepaalde categorie inzichten verbergen of de verbergen. Als u bijvoorbeeld niet wilt weten wat de minimale volgorde is, kunt u dat inzicht verbergen en op Toepassen klikken. en niet meer.

1. Selecteer ![ uitgeven intelligente vertoning van titels ](/help/assets/icons/EditInLight.svg) in de Intelligente dialoog van titels.

1. Wissel tussen ![ Zichtbaarheid ](/help/assets/icons/Visibility.svg) om een specifiek inzicht (als **[!UICONTROL Min]**) te tonen, of ![ VisibilityOff ](/help/assets/icons/VisibilityOff.svg) om een specifiek inzicht (als **[!UICONTROL Spike]**) te verbergen.

   ![ geef intelligente titels ](assets/edit-intelligent-captions.png) uit

1. Selecteer **[!UICONTROL Apply]** .


## Feedback geven

U kunt feedback geven over de gegenereerde intelligente bijschriften.

1. Selecteer ![ Meer acties ](/help/assets/icons/More.svg) in de Intelligente dialoog van titels.

1. Selecteer ![ Goede reactie ](/help/assets/icons/ThumbUpOutline.svg) **[!UICONTROL Good response]**, ![ ThumbDownOutline ](/help/assets/icons/ThumbDownOutline.svg) **[!UICONTROL Bad response]**, of ![ Vlag ](/help/assets/icons/Flag.svg) **[!UICONTROL Report]**.

1. Geef in het dialoogvenster **[!UICONTROL Thank you for your feedback]** uw feedback op en selecteer **[!UICONTROL Submit]** om de feedback te verzenden.

## Bijschriften exporteren {#export}

U kunt **uitvoertitels via PDF**, zolang het project met de geproduceerde titels wordt bewaard.

## Bijschriften in-/uitschakelen {#toggle}

Als u liever geen intelligente bijschriften wilt weergeven, schakelt u deze functie uit.

1. Ga naar [ de voorkeur van Visualisaties ](/help/analysis-workspace/user-preferences.md#visualizations-preferences).
1. Schakel **[!UICONTROL Show intelligent captions]** uit.

   ![ de visualisatieopties van de Lijn die de optie tonen om intelligente titels uit te schakelen.](assets/toggle-captions.png)

1. Selecteer **[!UICONTROL Save]** om de voorkeur op te slaan.





## Intelligente bijschriften in mobiele scoreborden

De intelligente titels zijn ook beschikbaar in Customer Journey Analytics [ mobiele scorecards ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dashboards/manage-scorecard#captions).

## Toegang tot functies

De volgende parameters regelen de toegang tot intelligente bijschriften:

* **toegang van de Oplossing**: De Intelligente eigenschap van titels is beschikbaar in Customer Journey Analytics, maar niet in Adobe Analytics.

* **Contractuele toegang**: Als u intelligente titels niet kunt gebruiken, gelieve te contacteren de beheerder of de Vertegenwoordiger van de Rekening van de Adobe van uw organisatie. Voordat u Intelligent kunt gebruiken in uw organisatie, moet u akkoord gaan met bepaalde juridische voorwaarden die betrekking hebben op GenAI.

* **Toestemmingen**: In [!UICONTROL Adobe Admin Console], bepaalt de [!UICONTROL Reporting Tools] **[!UICONTROL Intelligent Captions]** toestemming toegang. Admin van het a [ productprofiel ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) moet deze stappen in [!UICONTROL Admin Console] volgen:
   1. Navigeer naar **[!UICONTROL Admin Console]** > **[!UICONTROL Products and services]** > **[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Product Profiles]** .
   1. Selecteer de titel van het productprofiel waarvoor u toegang tot de Intelligente bijschriften wilt verlenen.
   1. Selecteer **[!UICONTROL Permissions]** in het specifieke productprofiel.
   1. Selecteer ![ uitgeven ](/help/assets/icons/Edit.svg) om uit te geven **[!UICONTROL Reporting Tools]**.
   1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) om **Intelligente Bijschriften** aan **[!UICONTROL Included permission items]** toe te voegen.

      ![ voeg toestemming ](./assets/intelligent-captions-permissions.png) toe

   1. Selecteer **[!UICONTROL Save]** om de machtigingen op te slaan.

Zie [ controle van de Toegang ](/help/technotes/access-control.md#access-control) voor meer informatie.