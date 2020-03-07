---
title: Veelgestelde vragen over reisanalyse van klant
description: De Analyse van de Reis van de klant - Veelgestelde Vragen.
translation-type: tm+mt
source-git-commit: cca701c2a18d094ee4b172b032c125e710b51ff0

---


# Vaak gestelde vragen

| Vraag | Antwoord |
|---|---|
| **Voorwaarden** |  |
| Hebt u Device Graph of Device Coop nodig voor de analyse van de reis van de klant? | Nr, de Grafiek van het Privé Apparaat of de Coop van het Apparaat worden niet vereist voor de Analyse van de Reis van de Klant. In feite worden ze nog niet gesteund. |
| Hebt u de Cloud-ID (EHID) van de Experience nodig voor de analyse van de reis van de Klant? | Nee, de Analyse van de Reis van de Klant steunt om het even welke identiteitskaart in een dataset, of dat ECID of een andere identiteitskaart is u kiest. |
| Wat als u uw gegevens vóór de Analyse van de Reis van de Klant moet ETL? | Vandaag, moet u met een partner ETL (Unifi of Informatica) werken als u uw gegevens moet omzetten alvorens het in AEP te zetten. Als u ETL nodig hebt nadat de gegevens reeds zijn ingeslikt, verstrekt de Diensten van de Vraag AEP sommige beperkte opties. |
| **Stitching** |  |
| Kan de Analyse van de Reis van de Klant over apparaten of over datasets &quot;stikken&quot;? | Nee. De Analyse van de Reis van de klant is een &quot;breng-uw-eigen-identiteitskaart&quot;analysesysteem. De plannen voor een goede stikkende aanpak staan in de werkzaamheden. |
| Wordt het stikken van anoniem gedrag aan voor authentiek verklaard gedrag gesteund? | Nee, nog niet. |
| **Gegevens in de analyse van de reis van de Klant ophalen** |  |
| Wat is de verwachte latentie voor de Analyse van de Reis van de Klant op Platform? | <ul><li>Onder normale belasting: &lt; 60<br>**minutenOpmerking:**In het geval van een ongebruikelijk hoog volume van gegevensstroom door de pijpleiding, kon het tot 24 uur vergen.</li><li>Back-upgegevens (tot 10 miljard gebeurtenissen): &lt; 4 weken</li></ul> |
| Hoe verbindt u online gegevens met off-line gegevens in de Analyse van de Reis van de Klant? | De Analyse van de Reis van de klant is een analysesysteem &quot;breng uw eigen identiteitskaart&quot; Zolang de persoonidentiteitskaart tussen datasets aanpast, kan de Analyse van de Reis van de Klant segmenten, attributie, stroom, neerslag, enz. verbinden. over datasets. |
| Hoe breng ik mijn off-line gegevens in de Analyse van de Reis van de Klant? | De klanten moeten om het even welke gegevens aan AEP eerst brengen alvorens zij het met de Analyse van de Reis van de Klant kunnen gebruiken. De gegevens van het ervaringsplatform over het instapteam kunnen, indien nodig, helpen om klanten aanbevelingen of advies te bieden. |
| Hoe krijg ik de gegevens van de Analyse in de Analyse van de Reis van de Klant? | De gegevens van de analyse kunnen met AEP door de Schakelaar van de Gegevens van de Analyse worden verbonden. De meeste gebieden van de Analyse worden gebracht over in formaat XDM, maar andere gebieden zijn nog niet beschikbaar (als de afmetingen van de Kanalen van de Marketing). |
| Hoe lang duurt het om datasetelementen in een gegevensmening te assembleren? | Een paar uur om te beginnen, en een paar dagen om van de laatste 13 maanden van gegevens een back-up te maken. |
| Is het noodzakelijk om PII gegevens te brengen om verbindingen tussen de gegevens te vestigen? | Nr, kunt u om het even welke identiteitskaart, met inbegrip van een knoeiboel van een klantenidentiteitskaart gebruiken, die geen PII is. |
| **Traditionele analytische componenten** |  |
| Wat betekent dit voor ons traditionele product van de Analyse van Adobe? | De Analyse van de Reis van de klant is ons product van de volgende generatie van de Analyse. Het evolueren van onze huidige producten naar Customer Journey Analytics zal jaren duren en veel coördinatie samen. Deze versie is een grote stap in de goede richting. |
| Kan ik segmenten van de Analyse van de Reis van de Klant aan AEP of andere oplossingen delen? | Nog niet. Wij bekijken nieuwe, innovatieve manieren om segmenten van de Analyse van de Reis van de Klant aan AEP in de toekomst te delen die niet zulk een lange vertraging hebben. Dat gezegd, kunt u de output van de Diensten van de Vraag aan Verenigd Profiel als potentiële alternerende actie delen. |
| Wat is er gebeurd met mijn oude eVar-omgeving? | Vars, de steunen, en de gebeurtenissen in de traditionele betekenis van de Analyse van Adobe bestaan niet meer in de Analyse van de Reis van de Klant. U hebt onbeperkte schemaelementen (afmetingen, metriek, lijstgebieden). Zo worden alle attributie montages u gebruikte om tijdens het proces van de gegevensinzameling toe te passen nu toegepast in vraagtijd. |
| Waar zijn al mijn zitting en veranderlijke persistentiemontages nu? | De Analyse van de Reis van de klant past elk van deze montages in rapporttijd toe, en deze montages leven nu in de Meningen van Gegevens. De veranderingen in deze montages zijn nu retroactief, en u kunt veelvoudige versies hebben door de veelvoudige Meningen van Gegevens te gebruiken! |
| Wat gebeurt er met onze bestaande segmenten/berekende waarden? | De Analyse van de Reis van de klant gebruikt niet meer eVars, props, of gebeurtenissen en gebruikt in plaats daarvan om het even welk schema AEP. Dit betekent geen van de bestaande segmenten of de calc metriek compatibel met de Analyse van de Reis van de Klant zijn. |
| Hoe behandelt de Analyse van de Reis van de Klant `Uniques Exceeded` beperkingen? | De Analyse van de Reis van de klant heeft geen unieke waardebeperkingen, zodat te hoeven om zich geen zorgen over hen te maken! |
| Als ik een bestaande [!DNL Data Workbench] klant ben, kan ik nu naar de Analyse van de Reis van de Klant overgaan? | Het hangt ervan af. Als u sterk op het Verenigde Proces van de Klant (UCP) vertrouwt, zult u willen wachten tot wij het stikken uitgevoerd hebben. Als u reeds acht tarieven van de klantenauthentificatie hebt, of als u al uw gegevens op één plaats wilt, of van eVars zou willen afzien, zou de Analyse van de Reis van de Klant een goede pasvorm kunnen zijn. |

