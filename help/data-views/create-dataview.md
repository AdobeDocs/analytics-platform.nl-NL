---
title: Een gegevensweergave maken
description: Beschrijft hoe te om een gegevensmening tot stand te brengen aan een dataset van het Platform in de Analyse van de Reis van de Klant (CJA).
translation-type: tm+mt
source-git-commit: c85b5d2e702a38aa6569da893a25bacd39604f8a

---


# Een gegevensweergave maken

Een gegevensmening is gelijkaardig aan een virtuele rapportreeks in Analytics in die zin dat het in zekere zin een &quot;gefilterde&quot;mening van de gegevens is. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, de toewijzing enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen. U kunt bijvoorbeeld een gegevensweergave hebben waarin alle afmetingen zijn ingesteld op Laatste aanraking en tegelijkertijd een andere gegevensweergave (op basis van dezelfde gegevensset) met alle afmetingen ingesteld op Eerste aanraking.

De projecten van de werkruimte in de Analyse van de Reis van de Klant zijn gebaseerd op gegevensmeningen.

Klik [hier](https://docs.adobe.com/content/help/en/platform-learn/tutorials/cja/basic-configuration-for-data-views.html) voor een video-overzicht.

## Vereiste

Voordat u gegevensweergaven kunt maken, moet u een of meer verbindingen [instellen met de gegevenssets](/help/connections/create-connection.md)van het Adobe Experience Platform.

## Instellingen configureren

1. Ga in de Analyse van de Reis van de Klant, naar het **[!UICONTROL Data Views]** lusje.

1. Klik **[!UICONTROL Add]** om een gegevensmening toe te voegen en zijn montages te vormen.

   | Sessieinstelling | Definitie |
   |---|---|
   | Verbinding | Dit gebied verbindt de gegevensmening met de verbinding die u vroeger vestigde, die de dataset/s van het Platform bevat. |
   | Naam | Het is verplicht de gegevensweergave een naam te geven. |
   | Beschrijving | Een gedetailleerde beschrijving is niet verplicht, maar aanbevolen. |
   | Codes toevoegen | Met tags kunt u de gegevensweergaven indelen in categorieën. |
   | Tijdzone | Kies de tijdzone voor de gegevensweergave. |
   | Time-out sessie | Selecteer wat uw definitie van een &quot;sessie&quot; is. De time-outinstelling voor de sessie definieert de hoeveelheid inactiviteit die een unieke bezoeker moet hebben voordat een nieuwe sessie automatisch wordt gestart. De standaardwaarde is 30 minuten. Als u de sessietime-out bijvoorbeeld instelt op 45 minuten, wordt een nieuwe sessiegroep gemaakt voor elke reeks resultaten die wordt verzameld, gescheiden door 45 minuten inactiviteit. <!--This setting impacts not only your visit counts, but also how visit segment containers are evaluated, and the visit expiration logic for any eVars expiring on visit. Decreasing the session timeout will likely increase the total number of visits in your reporting, while increasing the visit timeout will likely decrease the total number of visits in your reporting. This needs to be reviewed.--> |
   | Nieuwe sessie starten met gebeurtenis | Een nieuwe sessie wordt gestart wanneer een gebeurtenis wordt geactiveerd, ongeacht of er een time-out voor een sessie is opgetreden. De nieuwe sessie bevat de gebeurtenis die deze heeft gestart. Bovendien kunt u meerdere gebeurtenissen gebruiken om een sessie te starten en een nieuwe sessie wordt geactiveerd als een van deze gebeurtenissen in de gegevens wordt waargenomen. Dit het plaatsen zal uw bezoektelling, de het segmentcontainer van de Zitting (vroeger Bezoek), en de logica van de bezoekafloop op dimensies beïnvloeden. |
   | Filters toevoegen | &quot;Filters&quot; is de term voor &quot;segmenten&quot; in de Analyse van de Reis van de Klant. Als u uw gegevens wilt filteren, sleept u het juiste filter hier van de linkerspoorstaaf. Als u geen filter selecteert, bevat de gegevensweergave al uw gegevens. |

1. Klik op **[!UICONTROL Continue]**.

## Componenten toevoegen

1. Nu is het tijd om componenten (afmetingen, metriek) aan de gegevensmening (gelijkend op de curvaring in virtuele rapportreeksen toe te voegen.) Merk op dat elk van de gebieden in de datasets nu in afmetingen of metriek wordt vertaald. Sleep de afmetingen en metriek naar het deelvenster of **[!UICONTROL Selecteer Alles** om alle componenten toe te voegen.

   ![](assets/add-all-components.png)

1. Klik op het **[!UICONTROL Add Components]** tabblad om afmetingen en metriek toe te voegen aan de gegevensweergave.

   ![](assets/add-all-components2.png)

1. (Optioneel) U kunt de naam van een component wijzigen in een vriendelijke naam of de toewijzingsinstellingen wijzigen door de component te selecteren en de instelling te bewerken. De onderliggende naam blijft behouden. Zie [Gegevensweergaven en -toewijzing](/help/data-views/configure-dataviews.md)configureren voor meer informatie.

1. De volgende stappen zijn het [opgeven van de instellingen](/help/data-views/configure-dataviews.md)voor component en kenmerk.