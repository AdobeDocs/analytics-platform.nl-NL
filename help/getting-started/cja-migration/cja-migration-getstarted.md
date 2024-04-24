---
title: Aan de slag met de migratie naar Customer Journey Analytics
description: Uw migratie van Adobe Analytics naar Customer Journey Analytics plannen
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: fd3b36ab-72c1-469a-b2c7-419813c82425
source-git-commit: 7bc4425f11980780ab64a201029cd63e4bd7849c
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# Stap 1: Ga aan de slag met de migratie naar Customer Journey Analytics

Customer Journey Analytics is de volgende generatie analyses. Het staat multi-kanaalgegevensinzameling (zowel online als off-line gegevens) toe, gecombineerd met krachtige rapport-tijd verwerkingsfunctionaliteit (door de definitie van componenten en afgeleide gebieden in gegevensmeningen).

Voordat u begint met het migreren van Adobe Analytics naar Customer Journey Analytics, moet u de voordelen van Customer Journey Analytics begrijpen, evenals de stappen die nodig zijn om te migreren.

## Begrijp de voordelen van Customer Journey Analytics

Hieronder vindt u een aantal belangrijke voordelen: (Voor een uitgebreide lijst en meer informatie over elk van deze belangrijkste functies raadpleegt u [Functies die alleen beschikbaar zijn in Customer Journey Analytics](/help/getting-started/aa-vs-cja/cja-aa.md#adobe-customer-journey-analytics-features-not-available-in-adobe-analytics).)

* [Melding via meerdere kanalen](/help/getting-started/aa-to-cja-user.md#changes-to-data-architecture)

  Customer Journey Analytics wordt gecombineerd met de capaciteit van het Experience Platform om allerlei gegevensschema&#39;s en types te houden. Verzamel en rapporteer gegevens van meerdere kanalen, zoals digitale (Web), verkooppuntsystemen, mobiele systemen, CRM-systemen en meer.

* [Transformaties in de gegevensweergave bij uitvoering rapporteren](/help/getting-started/aa-vs-cja/vrs-dataview-sandbox-adc.md#customer-journey-analytics-data-views)

  Met gegevensweergaven in Customer Journey Analytics kunt u gegevens van een verbinding verder interpreteren. U kunt gegevens wijzigen of verwijderen zonder uw implementatie te wijzigen, subtekenreeksen gebruiken om afmetingen te manipuleren, metriek van om het even welke waarde tot stand te brengen, subtekenreeksen te filteren, of afgeleide gebieden te gebruiken. Al deze transformaties zijn niet-destructief.

* [Transformaties gelden voor historische en nieuwe gegevens](/help/getting-started/aa-vs-cja/vrs-dataview-sandbox-adc.md)

  De manipulatie van de Mening van gegevens kan op zowel historische als nieuwe gegevens op een niet destructieve manier worden toegepast.

* [Afgeleide velden](/help/data-views/derived-fields/derived-fields.md)

  De afgeleide gebieden staan voor rapport-tijd transformaties aan uw gegevens toe. Gegevens kunnen tijdens de vlucht worden gecombineerd, gecorrigeerd of gemaakt en worden met terugwerkende kracht toegepast op alle rapporten.

* [Gegevensweergaven vervangen virtuele rapportsuites](/help/getting-started/aa-to-cja-user.md#changes-to-the-concept-of-virtual-report-suites)

  De meningen van gegevens nemen het concept virtuele rapportreeksen zoals zij vandaag bestaan en breiden het uit om extra controles op de gegevens toe te laten die door verbindingen ter beschikking worden gesteld. Deze veranderingen maken algemene montages zoals timezone en zittingsonderbrekingsintervallen configureerbaar en retroactief.

* [Onbeperkte klantdimensies en metriek](/help/getting-started/aa-to-cja-user.md#changes-to-the-concept-of-evars-and-props)

  Waarden kunnen numeriek zijn, tekst, objecten, lijsten of mengsels van alle waarden. Dimensionen kunnen worden genest of hiërarchisch.

## Begrijp het migratieproces

<!-- Include a graphic of the end-to-end process, as well as links to each step of the process -->
De informatie op deze pagina behandelt Stap 1 van de migratie, zoals benadrukt in de lijst hieronder. Voer alle stappen in deze tabel uit om te migreren van Adobe Analytics naar Customer Journey Analytics.

| Migratietaak | Details |
|---------|----------|
| <span class="preview">**Stap 1: Aan de slag met de migratie**</span> | <span class="preview">Leer de voordelen van migratie naar Adobe Analytics en het basismigratieproces.</span> |
| **Stap 2: [Het migratiepad kiezen](/help/getting-started/cja-migration/cja-migration-path.md)** | Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen. |
| **Stap 3: [Gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van het migratiepad dat u hebt gekozen in Stap 2. |
| **Stap 4: [Historische gegevens behouden](/help/getting-started/cja-migration/cja-migration-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 5: [Extra implementatietaken uitvoeren](/help/getting-started/cja-getting-started.md)** | Op dit punt in het migratieproces, moet u diverse taken uitvoeren alvorens uw milieu van de Customer Journey Analytics klaar aan gebruik is.<p>Deze extra taken gelden voor migraties uit Adobe Analytics en voor nieuwe implementaties van Customers Journey Analytics.</p><p>Deze taken omvatten:</p><ul><li>Andere gegevens in Experience Platform plaatsen</li><li>Verbindingen maken tussen de gegevenssets van het Platform en Customer Journey Analytics</li><li>Gegevensweergaven maken</li><li>Het gebruik van de API voor rapportage porteren</li><li>Verantwoording van gegevensfeeds en -Data Warehouse</li><li>Projecten en onderdelen migreren</li><li>Gebruiker aan boord plannen</li></ul> <p>Zie voor meer informatie [Aan de slag met Customer Journey Analytics](/help/getting-started/cja-getting-started.md). |

{style="table-layout:auto"}

## Kies eerst het migratiepad

Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. [Kies de methode die het beste bij uw organisatie past](/help/getting-started/cja-migration/cja-migration-path.md).

Het migratiepad dat u kiest, is afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en van langetermijndoelen.
