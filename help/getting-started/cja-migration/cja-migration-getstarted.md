---
title: Aan de slag met de migratie naar Customer Journey Analytics
description: Uw migratie van Adobe Analytics naar Customer Journey Analytics plannen
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: fd3b36ab-72c1-469a-b2c7-419813c82425
source-git-commit: 21d77f06595993172460b724dc7991cb9a5a02a8
workflow-type: tm+mt
source-wordcount: '792'
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
Deze pagina vertegenwoordigt Stap 1 van de migratie, zoals aangetoond in de volgende lijst. Voer alle stappen in deze tabel uit om te migreren van Adobe Analytics naar Customer Journey Analytics.

| Taak | Details |
|---------|----------|
| **Stap 1: [Aan de slag met de migratie](/help/getting-started/cja-migration/cja-migration-getstarted.md)** | Leer de voordelen van migratie naar Adobe Analytics en het basismigratieproces. |
| **Stap 2: [Kies de migratiemethode](/help/getting-started/cja-migration/cja-migration-method.md)** | Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. Kies de methode die het beste bij uw organisatie past, rekening houdend met de huidige Adobe Analytics-omgeving van uw organisatie en uw langetermijndoelstellingen. |
| **Stap 3: [Gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-migration/cja-migration-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van de migratiemethode die u hebt gekozen in Stap 1. |
| **Stap 4: [Gegevens toewijzen aan het XDM-schema](/help/getting-started/cja-migration/cja-migration-xdm.md)** | [XDM-schema&#39;s](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) in Adobe Experience Platform worden gebruikt om de gegevensstructuur op een consistente en herbruikbare manier te beschrijven. Door gegevens consistent in verschillende systemen te definiëren, wordt het eenvoudiger om betekenis te behouden en zo waarde te verkrijgen van gegevens.<p>De meeste migratiemethodes vereisen dat u of een nieuw schema XDM creeert, of uw bestaand schema van Adobe Analytics aan XDM in kaart brengt door datastream afbeelding te gebruiken.</p> |
| **Stap 5: [Historische gegevens behouden](/help/getting-started/cja-migration/cja-migration-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 6: [Gebruiker aan boord plannen](/help/getting-started/cja-migration/cja-migration-onboarding.md)** | Geef uw gebruikers voldoende tijd (3 - 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Customer Journey Analytics van Analysis Workspace. |
| **Stap 7: [Poort voor het gebruik van de rapportage-API](/help/getting-started/cja-migration/cja-migration-api.md)** | De Customer Journey Analytics die API rapporteert, heeft dezelfde indeling, maar gebruikt een ander eindpunt. Geef het API-gebruik voor rapportage door van de Adobe Analytics-API voor rapportage naar de Customer Journey Analytics-API. |
| **Stap 8: [Gegevensfeeds en -Data Warehouse vervangen](/help/getting-started/cja-migration/cja-migration-export-options.md)** | Bepaal hoe u de exportopties in de Customer Journey Analytics wilt gebruiken om de functies Gegevensfeeds en Data Warehouse te vervangen die u in Adobe Analytics gebruikte. |
| **Stap 9: [Projecten en onderdelen migreren](/help/getting-started/cja-migration/cja-migration-projects.md)** | In het gebied voor componentmigratie in Adobe Analytics kunt u projecten en de bijbehorende onderdelen migreren van Adobe Analytics naar Customer Journey Analytics. |
| **Stap 10: [Na de migratie uitvoeren](/help/getting-started/cja-getting-started.md)** | Nadat u de migratie voltooit, moet u diverse taken uitvoeren, met inbegrip van het brengen van andere gegevens in Experience Platform, het creëren van verbindingen tussen de datasets van het Platform en Customer Journey Analytics, het creëren van gegevensmeningen, en het leren hoe te om over kanaalgegevens in Analysis Workspace te rapporteren. |

{style="table-layout:auto"}

## Kies eerst de migratiemethode

Er zijn verschillende methoden beschikbaar voor migreren naar Customer Journey Analytics. [Kies de methode die het beste bij uw organisatie past](/help/getting-started/cja-migration/cja-migration-method.md).

De door u gekozen migratiemethode is afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en van langetermijndoelstellingen.
