---
title: Een gegevensweergave maken
description: Beschrijft hoe te om een gegevensmening tot stand te brengen aan een dataset van het Platform in Customer Journey Analytics (CJA).
exl-id: 02494ef6-cc32-43e8-84a4-6149e50b9d78
translation-type: tm+mt
source-git-commit: a0ea2be203aa2e0df7b195e259b6d98c0c027652
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Een gegevensweergave maken

Een gegevensmening is gelijkaardig aan een virtuele rapportreeks in Analytics in die zin dat het in zekere zin een &quot;gefilterde&quot;mening van de gegevens is. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, de toewijzing enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen. U kunt bijvoorbeeld een gegevensweergave hebben waarin alle afmetingen zijn ingesteld op Laatste aanraking en tegelijkertijd een andere gegevensweergave (op basis van dezelfde gegevensset) met alle afmetingen ingesteld op Eerste aanraking.

Werkruimteprojecten in Customer Journey Analytics zijn gebaseerd op gegevensweergaven.

Klik [hier](https://docs.adobe.com/content/help/en/platform-learn/tutorials/cja/basic-configuration-for-data-views.html) voor een video-overzicht.

## Vereiste

Alvorens u gegevensmeningen kunt tot stand brengen, moet u [opstelling één of meerdere verbindingen aan Experience Platform datasets](/help/connections/create-connection.md).

## Instellingen configureren

1. Ga in Customer Journey Analytics naar het tabblad **[!UICONTROL Data Views]**.

1. Klik **[!UICONTROL Add]** om een gegevensmening toe te voegen en zijn montages te vormen.

   | Sessieinstelling | Definitie |
   |---|---|
   | Verbinding | Dit gebied verbindt de gegevensmening met de verbinding die u vroeger oprichtte, die [!UICONTROL Experience Platform] dataset/s bevat. |
   | Naam | Het is verplicht de gegevensweergave een naam te geven. |
   | Beschrijving | Een gedetailleerde beschrijving is niet verplicht, maar aanbevolen. |
   | Codes toevoegen | Met tags kunt u de gegevensweergaven indelen in categorieën. |
   | Tijdzone | Kies de tijdzone voor de gegevensweergave. |
   | Time-out sessie | Selecteer wat uw definitie van een &quot;sessie&quot; is. De time-outinstelling voor de sessie definieert de hoeveelheid inactiviteit die een unieke bezoeker moet hebben voordat een nieuwe sessie automatisch wordt gestart. De standaardwaarde is 30 minuten. Als u de sessietime-out bijvoorbeeld instelt op 45 minuten, wordt een nieuwe sessiegroep gemaakt voor elke reeks resultaten die wordt verzameld, gescheiden door 45 minuten inactiviteit. <!--This setting impacts not only your visit counts, but also how visit segment containers are evaluated, and the visit expiration logic for any eVars expiring on visit. Decreasing the session timeout will likely increase the total number of visits in your reporting, while increasing the visit timeout will likely decrease the total number of visits in your reporting. This needs to be reviewed.--> |
   | Nieuwe sessie starten met gebeurtenis | Een nieuwe sessie wordt gestart wanneer een gebeurtenis wordt geactiveerd, ongeacht of er een time-out voor een sessie is opgetreden. De nieuwe sessie bevat de gebeurtenis die deze heeft gestart. Bovendien kunt u meerdere gebeurtenissen gebruiken om een sessie te starten en een nieuwe sessie wordt geactiveerd als een van deze gebeurtenissen in de gegevens wordt waargenomen. Dit het plaatsen zal uw bezoektelling, de het segmentcontainer van de Zitting (vroeger Bezoek), en de logica van de bezoekafloop op dimensies beïnvloeden. |
   | Filters toevoegen | &quot;Filters&quot; is de term voor &quot;segmenten&quot; in Customer Journey Analytics. Als u de gegevens wilt filteren, sleept u het juiste filter   hier vanaf de linkerspoorlijn . Als u geen filter selecteert, bevat de gegevensweergave al uw gegevens. |

1. Klik op **[!UICONTROL Continue]**.

## Componenten toevoegen

1. Nu is het tijd om componenten (afmetingen, metriek) aan de gegevensmening toe te voegen. Merk op dat elk van de gebieden in de datasets nu in afmetingen of metriek wordt vertaald. Sleep afmetingen en metriek in het paneel of **[!UICONTROL Select All]** om alle componenten toe te voegen.

   ![](assets/add-all-components.png)

1. Klik op het tabblad **[!UICONTROL Add Components]** om afmetingen en metriek toe te voegen aan de gegevensweergave.

   ![](assets/add-all-components2.png)

1. (Optioneel) U kunt de naam van een component wijzigen in een vriendelijke naam of de toewijzingsinstellingen wijzigen door de component te selecteren en de instelling te bewerken. De onderliggende naam blijft behouden. Zie [Gegevensweergaven en -toewijzing configureren](/help/data-views/configure-dataviews.md) voor meer informatie.

1. De volgende stappen zijn het [specificeren component en attributie montages](/help/data-views/configure-dataviews.md).

## Gegevensweergaven verwijderen

Als u een gegevensmening in [!UICONTROL Customer Journey Analytics] schrapt, zal een foutenmelding erop wijzen dat om het even welke projecten van de Werkruimte die van deze geschrapte gegevensmening afhangen zullen ophouden werkend.
