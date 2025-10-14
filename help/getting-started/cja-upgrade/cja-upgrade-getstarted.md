---
title: Ga aan de slag met de upgrade naar Customer Journey Analytics
description: Upgrade van Adobe Analytics naar Customer Journey Analytics plannen
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: fd3b36ab-72c1-469a-b2c7-419813c82425
source-git-commit: eb9b749a5c61da3b4b5d2eeeed93bf5e4702a415
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Stap 1: Ga aan de slag met de upgrade naar Customer Journey Analytics

>[!AVAILABILITY]
>
>De informatie op deze pagina wordt vervangen door de volgende uitgebreidere upgrade-informatie: <ul><li>**Aanbevolen verbeteringsstappen**<p>Voor gedetailleerde informatie, zie [&#x200B; Geadviseerde weg wanneer bevordering van Adobe Analytics aan Customer Journey Analytics &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).</p></li><li>**Gids van de Verbetering van Customer Journey Analytics**<p>Er is een nieuwe upgradehandleiding beschikbaar waarmee op dynamische wijze upgradestappen worden gegenereerd die zijn afgestemd op uw organisatie en uw unieke omstandigheden.</p><p>Als u vanuit Customer Journey Analytics toegang wilt tot de hulplijn, selecteert u de tab **[!UICONTROL Workspace]** en vervolgens **[!UICONTROL Upgrade to Customer Journey Analytics]** in het linkerdeelvenster. Volg de aanwijzingen op het scherm.</p></li></ul>

Customer Journey Analytics is de volgende generatie analyses. Het staat multi-kanaalgegevensinzameling (zowel online als off-line gegevens) toe, gecombineerd met krachtige rapport-tijd verwerkingsfunctionaliteit (door de definitie van componenten en afgeleide gebieden in gegevensmeningen).

Voordat u begint met het upgraden van Adobe Analytics naar Customer Journey Analytics, dient u te weten wat de voordelen van Customer Journey Analytics zijn en welke stappen nodig zijn om de upgrade te voltooien.

## De voordelen van Customer Journey Analytics begrijpen

Na zijn enkele zeer belangrijke voordelen: (Voor een uitvoerige lijst, evenals meer informatie over elk van deze zeer belangrijke eigenschappen, zie [&#x200B; Eigenschappen beschikbaar slechts in Customer Journey Analytics &#x200B;](/help/getting-started/aa-vs-cja/cja-aa.md#adobe-customer-journey-analytics-features-not-available-in-adobe-analytics).)

* [Melding via meerdere kanalen](/help/getting-started/aa-to-cja-user.md#changes-to-data-architecture)

  Customer Journey Analytics wordt gecombineerd met de mogelijkheid van Experience Platform om allerlei gegevensschema&#39;s en -typen te bevatten. Verzamel en rapporteer gegevens van meerdere kanalen, zoals digitale (Web), verkooppuntsystemen, mobiele systemen, CRM-systemen en meer.

* [Transformaties in de gegevensweergave bij uitvoering rapporteren](/help/getting-started/aa-vs-cja/vrs-dataview-sandbox-adc.md#customer-journey-analytics-data-views)

  Met gegevensweergaven in Customer Journey Analytics kunt u gegevens van een verbinding verder interpreteren. U kunt gegevens wijzigen of verwijderen zonder uw implementatie te wijzigen, subtekenreeksen gebruiken om dimensies te manipuleren, metriek van om het even welke waarde, segmentsubevents, of afgeleide gebieden te gebruiken. Al deze transformaties zijn niet-destructief.

* [Transformaties gelden voor historische en nieuwe gegevens](/help/getting-started/aa-vs-cja/vrs-dataview-sandbox-adc.md)

  De manipulatie van de Mening van gegevens kan op zowel historische als nieuwe gegevens op een niet destructieve manier worden toegepast.

* [Afgeleide velden](/help/data-views/derived-fields/derived-fields.md)

  De afgeleide gebieden staan voor rapport-tijd transformaties aan uw gegevens toe. Gegevens kunnen tijdens de vlucht worden gecombineerd, gecorrigeerd of gemaakt en worden met terugwerkende kracht toegepast op alle rapporten.

* [Gegevensweergaven vervangen virtuele rapportsuites](/help/getting-started/aa-to-cja-user.md#changes-to-the-concept-of-virtual-report-suites)

  De meningen van gegevens nemen het concept virtuele rapportreeksen zoals zij vandaag bestaan en breiden het uit om extra controles op de gegevens toe te laten die door verbindingen ter beschikking worden gesteld. Deze veranderingen maken algemene montages zoals timezone en zittingsonderbrekingsintervallen configureerbaar en retroactief.

* [Onbeperkte klantdimensies en metriek](/help/getting-started/aa-to-cja-user.md#changes-to-the-concept-of-evars-and-props)

  Waarden kunnen numeriek zijn, tekst, objecten, lijsten of mengsels van alle waarden. Dimensies kunnen genest of hiërarchisch zijn.

## Het upgradeproces begrijpen

<!-- Include a graphic of the end-to-end process, as well as links to each step of the process -->
De informatie op deze pagina behandelt Stap 1 van het verbeteringsproces, zoals benadrukt in de lijst hieronder. Voer alle stappen in deze tabel uit om een upgrade uit te voeren van Adobe Analytics naar Customer Journey Analytics.

| Upgradetaak | Details |
|---------|----------|
| <span class="preview">**Stap 1: Krijg begonnen met de verbetering**</span> | <span class="preview"> leer de voordelen om aan Customer Journey Analytics en het basis verbeteringsproces te bevorderen.</span> |
| **Stap 2: [&#x200B; kies de verbeteringspad](/help/getting-started/cja-upgrade/cja-upgrade-path.md)** | Er zijn verschillende methoden beschikbaar voor de upgrade naar Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen. |
| **Stap 3: [&#x200B; verzendt gegevens naar Adobe Experience Platform](/help/getting-started/cja-upgrade/cja-upgrade-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van het upgradepad dat u hebt gekozen in Stap 2. |
| **Stap 4: [&#x200B; behoud historische gegevens](/help/getting-started/cja-upgrade/cja-upgrade-historical-data.md)** | De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar. |
| **Stap 5: [&#x200B; voer extra implementatietaken uit](/help/getting-started/cja-getting-started.md)** | Op dit punt in het upgradeproces moet u verschillende taken uitvoeren voordat uw Customer Journey Analytics-omgeving gebruiksklaar is.<p>Deze extra taken zijn van toepassing op upgrades vanuit Adobe Analytics en nieuwe Customer Journey Analytics-implementaties.</p><p>Deze taken omvatten:</p><ul><li>Andere gegevens in Experience Platform plaatsen</li><li>Verbindingen maken tussen de gegevenssets van het Platform en Customer Journey Analytics</li><li>Gegevensweergaven maken</li><li>Het gebruik van de API voor rapportage porteren</li><li>Boekhouding voor gegevensfeeds en Data Warehouse</li><li>Projecten en onderdelen migreren</li><li>Gebruiker aan boord plannen</li></ul> <p>Voor meer informatie, zie [&#x200B; Customer Journey Analytics Begonnen &#x200B;](/help/getting-started/cja-getting-started.md) worden. |

{style="table-layout:auto"}

## Kies eerst het upgradepad

Er zijn verschillende methoden beschikbaar voor de upgrade naar Customer Journey Analytics. [&#x200B; kies de methode die voor uw organisatie &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-path.md) het best is.

Het upgradepad dat u kiest, is afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en van langetermijndoelen.
