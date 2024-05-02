---
title: Historische gegevens behouden bij upgrade naar Customer Journey Analytics
description: Leer hoe u historische gegevens kunt behouden bij de upgrade naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 1d17151b-3a12-468e-9a4f-9e5994599570
source-git-commit: c64f7a1676f4fd3712e618e26357f430e7d9f019
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Stap 4: historische gegevens behouden bij upgrades

++ + breid deze sectie uit om te zien waar de informatie op deze pagina in het grotere verbeteringsproces past. Zorg ervoor dat alle vorige upgradestappen zijn voltooid.

Voordat u doorgaat met deze sectie, moet u eerst controleren of u alle vorige upgradetaken hebt uitgevoerd.

De informatie op deze pagina behandelt Stap 4 van het verbeteringsproces, zoals benadrukt in de hieronder lijst:

| Upgradetaak | Details |
|---------|----------|
| **Stap 1: [Aan de slag met de upgrade](/help/getting-started/cja-upgrade/cja-upgrade-getstarted.md)** | Leer de voordelen van een upgrade naar de Customer Journey Analytics en het standaard upgradeproces. |
| **Stap 2: [Het upgradepad kiezen](/help/getting-started/cja-upgrade/cja-upgrade-path.md)** | Er zijn verschillende methoden beschikbaar voor de upgrade naar de Customer Journey Analytics. Kies de methode die het meest geschikt is voor uw organisatie, afhankelijk van de huidige Adobe Analytics-omgeving van uw organisatie en langetermijndoelstellingen. |
| **Stap 3: [Gegevens verzenden naar Adobe Experience Platform](/help/getting-started/cja-upgrade/cja-upgrade-send-to-platform.md)** | Het proces voor het verzenden van gegevens naar Adobe Experience Platform is afhankelijk van het upgradepad dat u hebt gekozen in Stap 2. |
| <span class="preview">**Stap 4: historische gegevens behouden**</span> | <span class="preview">De meeste organisaties moeten hun historische gegevens van Adobe Analytics voor een bepaalde hoeveelheid tijd behouden. Hiervoor zijn verschillende opties beschikbaar.</span> |
| **Stap 5: [Extra implementatietaken uitvoeren](/help/getting-started/cja-getting-started.md)** | Op dit punt in het verbeteringsproces, moet u diverse taken uitvoeren alvorens uw milieu van de Customer Journey Analytics klaar is te gebruiken.<p>Deze extra taken zijn van toepassing op upgrades vanuit Adobe Analytics en op nieuwe implementaties van Customers Journey Analytics.</p><p>Deze taken omvatten:</p><ul><li>Andere gegevens in Experience Platform plaatsen</li><li>Verbindingen maken tussen de gegevenssets van het Platform en Customer Journey Analytics</li><li>Gegevensweergaven maken</li><li>Het gebruik van de API voor rapportage porteren</li><li>Verantwoording van gegevensfeeds en -Data Warehouse</li><li>Projecten en onderdelen migreren</li><li>Gebruiker aan boord plannen</li></ul> <p>Zie voor meer informatie [Aan de slag met Customer Journey Analytics](/help/getting-started/cja-getting-started.md). |

{style="table-layout:auto"}

+++

Kies een van de volgende opties om historische gegevens te behouden wanneer u van Adobe Analytics naar Customer Journey Analytics gaat:

>[!IMPORTANT]
>
>Wanneer u kiest hoe u historische gegevens wilt behouden, neemt u contact op met de accountvertegenwoordiger van de Adobe om de prijs te bepalen.

## De Bronverbinding Analytics gebruiken

U kunt de [Bronverbinding voor analyse](/help/data-ingestion/analytics.md) om historische gegevens te behouden. Ongeacht het upgradepad dat u kiest (zelfs als u een upgrade uitvoert met de SDK van het web), kunt u de Bronverbinding Analytics gebruiken om historische gegevens uit uw Adobe Analytics-omgeving te behouden.

U kunt de Verbinding van de Bron van Analytics gebruiken om historische gegevens te behouden door historische gegevens in zijn eigen specifieke plaats, los van uw huidige gegevens te brengen.

De verbinding van de Bron van Analytics moet functioneren zolang u toegang tot de historische gegevens nodig hebt.

<!-- Another possibility in the future: Map historical data in a way that allows you to tie it to your new data.  Possible? Explain -->

## Bestaande Adobe Analytics-implementatie onderhouden

U kunt uw bestaande Adobe Analytics-implementatie gedurende een specifiek tijdsbestek (bijvoorbeeld 1 jaar) naast uw nieuwe Customer Journey Analytics-implementatie handhaven. Houd rekening met het volgende wanneer u deze optie kiest:

* Gegevens zijn niet beschikbaar in Experience Platform.

* U zou moeten van plan zijn om de implementatie van Adobe Analytics te decommuniceren nadat u voldoende gegevens in Customer Journey Analytics hebt.

## Voer vervolgens aanvullende implementatietaken uit

Op dit punt in het verbeteringsproces, moet u diverse implementatietaken uitvoeren alvorens uw milieu van de Customer Journey Analytics klaar is te gebruiken.

Deze extra taken zijn van toepassing op upgrades vanuit Adobe Analytics en op nieuwe implementaties van Customers Journey Analytics.

Deze taken omvatten:

* Andere gegevens in Experience Platform plaatsen

* Verbindingen maken tussen de gegevenssets van het Platform en Customer Journey Analytics

* Gegevensweergaven maken

* Het gebruik van de API voor rapportage porteren

* Verantwoording van gegevensfeeds en gebruiksgevallen van Data Warehouse

* Projecten en onderdelen migreren

* Gebruiker aan boord plannen

Voor meer informatie, begin met Stap 2 binnen [Aan de slag met Customer Journey Analytics](/help/getting-started/cja-getting-started.md).
