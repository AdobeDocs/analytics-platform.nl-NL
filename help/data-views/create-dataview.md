---
title: Een gegevensweergave maken
description: Beschrijft hoe te om een gegevensmening tot stand te brengen aan een dataset van het Platform in de Analyse van de Reis van de Klant (CJA).
translation-type: tm+mt
source-git-commit: c85b5d2e702a38aa6569da893a25bacd39604f8a

---


# Een gegevensweergave maken

Een gegevensmening is gelijkaardig aan een virtuele rapportreeks in Analytics in zoverre dat het in betekenis een &quot;gefiltreerde&quot;mening van de gegevens is. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van het bezoek, de toewijzing, enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen. Bijvoorbeeld, kon u één gegevensmening hebben waar alle afmetingen aan &quot;Laatste Aanraking&quot;worden geplaatst, en, gelijktijdig, een andere gegevensmening (die op de zelfde dataset wordt gebaseerd) met alle afmetingen die aan &quot;Eerste Aanraking&quot;worden geplaatst.

De projecten van de werkruimte in de Analyse van de Reis van de Klant zijn gebaseerd op gegevensmeningen.

Klik [hier](https://docs.adobe.com/content/help/en/platform-learn/tutorials/cja/basic-configuration-for-data-views.html) voor een videooverzicht.

## Voorwaarde

Alvorens u gegevensmeningen kunt tot stand brengen, moet u aan [opstelling één of meerdere verbindingen aan de datasets](/help/connections/create-connection.md)van het Platform van de Ervaring van Adobe.

## Instellingen configureren

1. In de Analyse van de Reis van de Klant, ga naar de **[!UICONTROL Data Views]** tabel.

1. Klik **[!UICONTROL Add]** om een gegevensmening toe te voegen en zijn montages te vormen.

   | Sessieinstelling | Definitie |
   |---|---|
   | Verbinding | Dit gebied verbindt de gegevensmening met de verbinding die u vroeger vestigde, die de dataset/s van het Platform bevat. |
   | Naam | Het geven van de gegevensmening is een naam verplicht. |
   | Beschrijving | Een gedetailleerde beschrijving is niet verplicht, maar aanbevolen. |
   | Tags toevoegen | Met tags kunt u uw gegevensweergaven in rubrieken indelen. |
   | Tijdzone | Kies de tijdzone voor uw gegevensmening. |
   | Time-out sessie | Selecteer wat uw definitie van een &quot;zitting&quot;is. De zittingsonderbreking die bepaalt de hoeveelheid inactiviteit een unieke bezoeker moet hebben alvorens een nieuwe zitting automatisch is begonnen. De standaardinstelling is 30 minuten. Bijvoorbeeld, als u de zittingsonderbreking aan 45 minuten plaatst, wordt een nieuwe zittingsgroepering gecreeerd voor elke opeenvolging van verzamelde hits, die door 45 minuten van inactiviteit wordt gescheiden. <!--This setting impacts not only your visit counts, but also how visit segment containers are evaluated, and the visit expiration logic for any eVars expiring on visit. Decreasing the session timeout will likely increase the total number of visits in your reporting, while increasing the visit timeout will likely decrease the total number of visits in your reporting. This needs to be reviewed.--> |
   | Nieuwe sessie starten met gebeurtenis | Een nieuwe zitting begint wanneer een gebeurtenis wordt in brand gestoken, ongeacht of een zitting uit heeft vastgesteld. De pas gecreëerde zitting omvat de gebeurtenis die het begon. Bovendien, kunt u veelvoudige gebeurtenissen gebruiken om een zitting en een nieuwe zittingsbrand te beginnen als om het even welk van die gebeurtenissen in de gegevens worden waargenomen. Dit het plaatsen zal uw bezoektelling, de het segmentcontainer van de Zitting (vroeger Bezoek), en de logica van de bezoekafloop op afmetingen beïnvloeden. |
   | Filters toevoegen | &quot;Filters&quot;is de termijn voor &quot;segmenten&quot;in de Analyse van de Reis van de Klant. Als u uw gegevens wilt filtreren, sleep hier de aangewezen filter van de linkerspoor. Als u geen filter selecteert, zal de gegevensmening elk van uw gegevens bevatten. |

1. Klik op **[!UICONTROL Continue]**.

## Onderdelen toevoegen

1. Nu is het tijd om componenten (afmetingen, metriek) aan de gegevensmening (gelijkend op de curationervaring in virtuele rapportreeksen toe te voegen.) Bericht dat elk van de gebieden in de datasets nu in afmetingen of metriek vertaald zijn. De afmetingen en de metriek van de belemmering in het paneel of **[!UICONTROL selecteren allen** om alle componenten toe te voegen.

   ![](assets/add-all-components.png)

1. Klik het **[!UICONTROL Add Components]** lusje om afmetingen en metriek aan de gegevensmening toe te voegen.

   ![](assets/add-all-components2.png)

1. (Facultatief) u kunt een component anders noemen aan een vriendschappelijke naam of zijn attributie montages veranderen door het te selecteren en zijn het plaatsen uit te geven. Merk op dat de onderliggende naam wordt bewaard. Voor meer informatie, zie [gegevensuitzichten en attributie](/help/data-views/configure-dataviews.md)vormen.

1. De volgende stappen moeten component en attributie montages [](/help/data-views/configure-dataviews.md)specificeren.