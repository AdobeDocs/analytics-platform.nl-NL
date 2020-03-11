---
title: Veelgestelde vragen over klantreisanalyse
description: Analyse van de reis van de klant - Veelgestelde vragen.
translation-type: tm+mt
source-git-commit: 336adb3762258cc657ffa5c74a50d28e6f63c7db

---


# Veelgestelde vragen

| Vraag | Antwoord |
|---|---|
| **Vereisten** |  |
| Hebt u apparaatgrafiek of apparaatcoop nodig voor de analyse van de reis van de klant? | No, Private Device Graph or Device Coop is not required for Customer Journey Analytics. Ze worden zelfs nog niet ondersteund. |
| Hebt u de Experience Cloud ID (ECID) nodig voor de analyse van de reis van de klant? | Nee, de Analyse van de Reis van de Klant steunt om het even welke identiteitskaart in een dataset, of dat ECID of om het even welke andere identiteitskaart is u kiest. |
| Wat gebeurt er als u uw gegevens vóór de analyse van de reis van de klant moet uitpakken, transformeren, laden? | Vandaag, moet u met een partner ETL (Unifi of Informatica) werken als u uw gegevens moet omzetten alvorens het in AEP te zetten. Als u ETL nodig hebt nadat de gegevens al zijn ingevoerd, biedt AEP Query Services enkele beperkte opties. |
| **Stiksel** |  |
| Kan de Analyse van de Reis van de Klant op apparaten of over datasets &quot;aansluiten&quot;? | Nee. De Analyse van de Reis van de klant is een &quot;breng-uw-identiteitskaart&quot;analysesysteem. In de werkzaamheden staan plannen voor een goede aanpak. |
| Wordt het stitching van anoniem gedrag aan voor authentiek verklaard gedrag gesteund? | Nee, nog niet. |
| **Gegevens ophalen in de reisanalyse van de klant** |  |
| Wat is de verwachte latentie voor de Analyse van de Reis van de Klant op Platform? | <ul><li>Onder normale belasting: &lt; 60<br>**minutenOpmerking:**In het geval van een ongebruikelijk hoog volume van gegevensstroom door de pijpleiding, zou het tot 24 uren kunnen vergen.</li><li>Back-upgegevens (maximaal 10 miljard gebeurtenissen): &lt; 4 weken</li></ul> |
| Hoe verbindt u online gegevens met off-line gegevens in de Analyse van de Reis van de Klant? | De Analyse van de Reis van de klant is een &quot;breng uw eigen identiteitskaart&quot;analysesysteem. Zolang de persoon identiteitskaart tussen datasets aanpast, kan de Analyse van de Reis van de Klant segmenten, attributie, stroom, reserve, enz. verbinden over datasets. |
| Hoe breng ik mijn offline gegevens naar de Analyse van de Reis van de Klant? | Klanten moeten eerst alle gegevens naar AEP brengen voordat ze deze kunnen gebruiken met Customer Reader Analytics. De gegevens van het Experience Platform over instapkaartteam kunnen klanten indien nodig helpen aanbevelingen of advies te geven. |
| Hoe krijg ik Analytische gegevens in de Analyse van de Reis van de Klant? | De analysegegevens kunnen met AEP door de Verbinding van Gegevens van Analytics worden verbonden. De meeste analytische gebieden worden gebracht over in formaat XDM, maar andere gebieden zijn nog niet beschikbaar (als de afmetingen van de Kanalen van de Marketing). |
| Hoe lang duurt het om datasetelementen in een gegevensmening samen te stellen? | Een paar uur om te beginnen en een paar dagen om een back-up te maken van de laatste 13 maanden van gegevens. |
| Is het noodzakelijk om PII gegevens te brengen om verbindingen tussen de gegevens te vestigen? | Nr, kunt u om het even welke identiteitskaart, met inbegrip van een knoeiboel van een klant identiteitskaart gebruiken, die geen PII is. |
| **Traditionele analytische componenten** |  |
| Wat betekent dit voor ons traditionele Adobe Analytics-product? | De Analyse van de Reis van de Klant is ons volgende generatieanalyseproduct. Het evolueren van onze huidige producten naar de Analyse van de Reis van de Klant zal jaren en een hoop coördinatie samen vergen. Deze release is een grote stap in die richting. |
| Kan ik segmenten van de Analyse van de Reis van de Klant aan AEP of andere oplossingen delen? | Nog niet. We zijn op zoek naar nieuwe, innovatieve manieren om in de toekomst segmenten te delen van Customer Journey Analytics naar AEP die niet zo lang wachten. Dat gezegd, kunt u de output van de Diensten van de Vraag aan Verenigd Profiel als potentiële alternerende actie delen. |
| Wat is er gebeurd met mijn oude eVar-omgeving? | Vars, props en gebeurtenissen in de traditionele betekenis van Adobe Analytics bestaan niet meer in de Analyse van de Reis van de Klant. U hebt onbeperkte schema-elementen (afmetingen, metriek, lijstvelden). Zo worden alle attributie montages u gebruikte om tijdens het proces van de gegevensinzameling toe te passen nu toegepast bij vraagtijd. |
| Waar zijn al mijn zitting en veranderlijke persistentie montages nu? | De Analyse van de Reis van de klant past al deze montages op rapporttijd toe, en deze montages leven nu in de Mening van Gegevens. De wijzigingen in deze instellingen zijn nu retroactief en u kunt meerdere versies gebruiken door meerdere gegevensweergaven te gebruiken! |
| Wat gebeurt er met onze bestaande segmenten/berekende maatstaven? | De Analyse van de Reis van de klant gebruikt niet meer eVars, pro&#39;s, of gebeurtenissen en in plaats daarvan gebruikt om het even welk schema AEP. Dit betekent dat geen van de bestaande segmenten of calc metriek compatibel is met de Analyse van de Reis van de Klant. |
| Hoe verwerken de Analyses van de Reis van de Klant `Uniques Exceeded` beperkingen? | De Analyse van de Reis van de klant heeft geen unieke waardebeperkingen, zodat te hoeven om hen ongerust te maken! |
| Als ik een bestaande [!DNL Data Workbench] klant ben, kan ik nu naar de Analyse van de Reis van de Klant overgaan? | Het hangt ervan af. Als u sterk op het Verenigde Proces van de Klant (UCP) vertrouwt, zult u willen wachten tot wij het stitching uitgevoerd hebben. Als u al hoge verificatiecijfers voor klanten hebt, of als u al uw gegevens op één locatie wilt opslaan, of als u van eVars wilt afzien, is de analyse van de reis van de klant wellicht een goede oplossing. |

