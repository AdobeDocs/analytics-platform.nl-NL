---
title: Een gegevensweergave maken
description: Beschrijft hoe te om een gegevensmening aan een dataset van het Platform in de Analyse van de Reis van de Klant (CJA) te creëren.
translation-type: tm+mt
source-git-commit: de265170126c1a9fc1f66364a79a74ff487d0b71
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---


# Een gegevensweergave maken

Een gegevensmening is gelijkaardig aan een virtuele rapportreeks in Analytics in zoverre dat het in betekenis een &quot;gefilterde&quot;mening van de gegevens is. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor een bezoekonderbreking, toewijzing, enz. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen. Bijvoorbeeld, kon u één gegevensmening hebben waar alle afmetingen aan &quot;Laatste Aanraking&quot;worden geplaatst, en, gelijktijdig, een andere gegevensmening (die op de zelfde dataset wordt gebaseerd) met alle afmetingen aan &quot;Eerste Aanraking&quot;worden geplaatst.

De projecten van de werkruimte in de Analyse van de Reis van de Klant zijn gebaseerd op gegevensmeningen.

Klik [hier](https://docs.adobe.com/content/help/en/platform-learn/tutorials/cja/basic-configuration-for-data-views.html) voor een videooverzicht.

## Voorwaarde

Alvorens u gegevensmeningen kunt tot stand brengen, moet u [opstelling één of meerdere verbindingen aan de datasets van het Platform van de Ervaring](/help/connections/create-connection.md).

## Instellingen configureren

1. Ga in de Reisanalyse van de Klant naar de **[!UICONTROL Data Views]** tabblad

1. Klik **[!UICONTROL Add]** om een gegevensmening toe te voegen en zijn montages te vormen.

   | Sessieinstelling | Definitie |
   |---|---|
   | Verbinding | Dit gebied verbindt de gegevensmening met de verbinding die u vroeger vestigde, die bevat [!UICONTROL Experience Platform] gegevensset(s). |
   | Naam | Het geven van de gegevensmening is een naam verplicht. |
   | Beschrijving | Een gedetailleerde beschrijving is niet verplicht, maar aanbevolen. |
   | Tags toevoegen | Met tags kunt u uw gegevensweergaven in categorieën indelen. |
   | Tijdzone | Kies de tijdzone voor uw gegevensweergave. |
   | Time-out sessie | Selecteer wat uw definitie van een &quot;zitting&quot; is. De sessie time-out instelling bepaalt de hoeveelheid inactiviteit die een unieke bezoeker moet hebben voordat een nieuwe sessie automatisch wordt gestart. De standaardinstelling is 30 minuten. Bijvoorbeeld, als u de zittingsonderbreking aan 45 minuten plaatst, wordt een nieuwe zittingsgroepering gecreeerd voor elke opeenvolging van verzamelde hits, die door 45 minuten van inactiviteit wordt gescheiden. <!--This setting impacts not only your visit counts, but also how visit segment containers are evaluated, and the visit expiration logic for any eVars expiring on visit. Decreasing the session timeout will likely increase the total number of visits in your reporting, while increasing the visit timeout will likely decrease the total number of visits in your reporting. This needs to be reviewed.--> |
   | Nieuwe sessie starten met gebeurtenis | Een nieuwe zitting begint wanneer een gebeurtenis in brand wordt gestoken, ongeacht of een zitting uit heeft vastgesteld. De pas gecreëerde zitting omvat de gebeurtenis die het begon. Bovendien, kunt u veelvoudige gebeurtenissen gebruiken om een zitting en een nieuwe zittingsbrand te beginnen als om het even welk van die gebeurtenissen in de gegevens worden waargenomen. Dit het plaatsen zal uw bezoektelling, de het segmentcontainer van de Zitting (vroeger Bezoek), en de logica van de bezoekafloop op afmetingen beïnvloeden. |
   | Filters toevoegen | &quot;Filters&quot; is de term voor &quot;segmenten&quot; in de Journalistiek van de Klant. Als u uw gegevens wilt filtreren, sleep hier de aangewezen filter van de linkerspoor. Als u geen filter selecteert, zal de gegevensmening elk van uw gegevens bevatten. |

1. Klik op **[!UICONTROL Continue]**.

## Componenten toevoegen

1. Nu is het tijd om componenten (afmetingen, metriek) aan de gegevensmening (gelijkend op de curationervaring in virtuele rapportreeksen toe te voegen.) Bericht dat elk van de gebieden in de datasets nu in afmetingen of metriek vertaald zijn. De afmetingen en de metriek van de belemmering in het paneel of **[!UICONTROL Select All]** om alle componenten toe te voegen.

   ![](assets/add-all-components.png)

1. Klik op de **[!UICONTROL Add Components]** tabblad om afmetingen en maatstaven toe te voegen aan de gegevensweergave.

   ![](assets/add-all-components2.png)

1. (Facultatief) u kunt een component anders noemen aan een vriendschappelijke naam of zijn attributie montages veranderen door het te selecteren en zijn het plaatsen uit te geven. Merk op dat de onderliggende naam wordt bewaard. Voor meer informatie, zie [Gegevensweergaven en -toewijzing configureren](/help/data-views/configure-dataviews.md).

1. De volgende stappen zijn: [component- en attributie-instellingen opgeven](/help/data-views/configure-dataviews.md).