---
title: Customer Journey Analytics Veelgestelde vragen
description: Customer Journey Analytics - Veelgestelde vragen.
translation-type: tm+mt
source-git-commit: eb7d7d80ee07298f7d0fe308bdc93a3435f2c381
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 1%

---


# Veelgestelde vragen

| Vraag | Antwoord |
| --- | --- |
| **Vereisten** |  |
| Moet ik apparaatgrafiek of apparaatcoop gebruiken voor [!UICONTROL Customer Journey Analytics]? | No, Private Device Graph of Device Coop is niet vereist voor [!UICONTROL Customer Journey Analytics]. Ze worden zelfs nog niet ondersteund. |
| Heb ik Experience Cloud-ID (ECID) nodig voor [!UICONTROL Customer Journey Analytics]? | Nee, [!UICONTROL Customer Journey Analytics] steunt om het even welke identiteitskaart in een dataset, of dat ECID of om het even welke andere identiteitskaart is u kiest. |
| Wat gebeurt er als ik mijn gegevens voor Customer Journey Analytics moet ophalen (extraheren, transformeren, laden)? | Vandaag, moet u met een partner ETL (Unifi of Informatica) werken als u uw gegevens moet omzetten alvorens het in AEP te zetten. Als u ETL nodig hebt nadat de gegevens al zijn ingevoerd, biedt AEP Query Services enkele beperkte opties. |
| **Stiksel** |  |
| Kan [!UICONTROL Customer Journey Analytics] &quot;aansluiten&quot; op verschillende apparaten of op verschillende gegevenssets? | Nee. [!UICONTROL Customer Journey Analytics] is een &#39;breng-uw-eigen-identiteitskaart&#39; analysesysteem. In de werkzaamheden staan plannen voor een goede aanpak. |
| Wordt het stitching van anoniem gedrag aan voor authentiek verklaard gedrag gesteund? | Nee, nog niet. |
| **Gegevens ophalen in[!UICONTROL Customer Journey Analytics]** |  |
| Kan ik gegevens uit verschillende Experience Platform sandboxen combineren in één CJA-verbinding? | Nee, u hebt geen toegang tot gegevens in verschillende sandboxen. U kunt alleen gegevenssets combineren die zich binnen dezelfde sandbox bevinden. [Meer informatie...](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-connections/create-connection.html#select-sandbox-and-datasets) |
| Wat is de verwachte latentie voor [!UICONTROL Customer Journey Analytics] op [!UICONTROL Experience Platform]? | <ul><li>Onder normale belasting: &lt; 60 minuten <br>**Opmerking:** In het geval van een ongebruikelijk hoog volume van gegevensstroom door de pijpleiding, zou het tot 24 uren kunnen vergen.</li><li>Backfill-gegevens (tot 13 maanden aan gegevens, ongeacht de grootte): &lt; 4 weken</li></ul> |
| Hoe kan ik online gegevens verbinden met offline gegevens in [!UICONTROL Customer Journey Analytics]? | [!UICONTROL Customer Journey Analytics] is een &#39;breng je eigen id&#39; analysesysteem. Zolang de persoonidentiteitskaart tussen datasets aanpast, [!UICONTROL Customer Journey Analytics] kan segmenten, attributie, stroom, fallout, enz. verbinden over datasets. |
| Hoe breng ik mijn offline gegevens in Customer Journey Analytics? | U moet eerst alle gegevens naar het Experience Platform brengen voordat u deze kunt gebruiken met Customer Journey Analytics. Het team voor gegevens aan boord van het Experience Platform kan u, indien nodig, aanbevelingen of advies geven. |
| Hoe krijg ik Analytische gegevens in Customer Journey Analytics? | De analysegegevens kunnen met Experience Platform door [Gegevensconnector Analytics](https://docs.adobe.com/content/help/en/experience-platform/sources/connectors/adobe-applications/analytics.html). De meeste analytische gebieden worden gebracht over in formaat XDM, maar andere gebieden zijn nog niet beschikbaar (als de afmetingen van de Kanalen van de Marketing). |
| Hoe lang duurt het om datasetelementen in een gegevensmening samen te stellen? | Een paar uur om te beginnen en een paar dagen om een back-up te maken van de laatste 13 maanden van gegevens. |
| Is het noodzakelijk om PII gegevens te brengen om verbindingen tussen de gegevens te vestigen? | Nr, kunt u om het even welke identiteitskaart, met inbegrip van een knoeiboel van een klant identiteitskaart gebruiken, die geen PII is. |
| **Traditionele analytische componenten** |  |
| Wat betekent dit voor ons traditionele Adobe Analytics-product? | Customer Journey Analytics is ons product van de volgende generatie. Het evolueren van onze huidige producten naar Customer Journey Analytics zal jaren duren en veel coördinatie samen. Voor meer informatie raadpleegt u [Ondersteuning voor Customer Journey Analytics-functies](/help/getting-started/cja-aa.md). |
| Kan ik segmenten van Customer Journey Analytics tot AEP of andere oplossingen delen? | Nog niet. We zijn op zoek naar nieuwe, innovatieve manieren om in de toekomst segmenten van Customer Journey Analytics naar AEP te delen die niet zo lang wachten. Dat gezegd, kunt u de output van de Diensten van de Vraag aan Verenigd Profiel als potentiële alternerende actie delen. |
| Wat is er gebeurd met mijn oude eVar-omgeving? | Vars, props en gebeurtenissen in de traditionele Adobe Analytics-zin bestaan niet meer in Customer Journey Analytics. U hebt onbeperkte schema-elementen (afmetingen, metriek, lijstvelden). Zo worden alle attributie montages u gebruikte om tijdens het proces van de gegevensinzameling toe te passen nu toegepast bij vraagtijd. |
| Waar zijn al mijn zitting en veranderlijke persistentie montages nu? | Customer Journey Analytics past al deze instellingen toe tijdens de rapporttijd en deze instellingen worden nu in de gegevensweergave weergegeven. De wijzigingen in deze instellingen zijn nu retroactief en u kunt meerdere versies gebruiken door meerdere gegevensweergaven te gebruiken! |
| Wat gebeurt er met onze bestaande segmenten/berekende maatstaven? | Customer Journey Analytics gebruikt niet langer eVars, props of gebeurtenissen en gebruikt in plaats daarvan een AEP-schema. Dit betekent geen van de bestaande segmenten of de cijfers van de calc compatibel met Customer Journey Analytics zijn. |
| Hoe werkt Customer Journey Analytics? `Uniques Exceeded` beperkingen? | Customer Journey Analytics heeft geen unieke waardebeperkingen, dus hoeft u zich daar geen zorgen over te maken! |
| Als ik een bestaande [!DNL Data Workbench] klant, kan ik nu naar Customer Journey Analytics gaan? | Het hangt ervan af. Als u sterk op het Verenigde Proces van de Klant (UCP) vertrouwt, zult u willen wachten tot wij het stitching uitgevoerd hebben. Als u reeds hoge klantenauthentificatiecijfers hebt, of als u al uw gegevens op één plaats wilt, of van eVars zou willen schrappen, zou Customer Journey Analytics een goede pasvorm kunnen zijn. |

