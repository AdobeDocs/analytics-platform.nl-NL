---
title: Veelgestelde vragen over reisanalyse van klanten
description: Reisanalyse van de klant - Veelgestelde vragen.
translation-type: tm+mt
source-git-commit: 297ed03ff59cc8d719a6bf0984e82597e8d33392
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 1%

---


# Veelgestelde vragen

| Vraag | Antwoord |
| --- | --- |
| **Vereisten** |  |
| Heb ik Device Graph of Device Coop nodig voor [!UICONTROL Customer Journey Analytics]? | Neen, de Privé Grafiek van het Apparaat of Coop van het Apparaat worden niet vereist voor [!UICONTROL Customer Journey Analytics]. In feite worden ze nog niet gesteund. |
| Heb ik een Ervaring Cloud ID (ECID) nodig voor [!UICONTROL Customer Journey Analytics]? | Nee, [!UICONTROL Customer Journey Analytics] steunt om het even welke identiteitskaart in een dataset, of dat ECID of een andere identiteitskaart is u kiest. |
| Wat als ik aan ETL (Extract, Transform, Laden) mijn gegevens voorafgaand aan de Analyse van de Reis van de Klant nodig heb? | Vandaag, moet u met een partner ETL (Unifi of Informatica) werken als u uw gegevens moet omzetten alvorens het in AEP te zetten. Als u ETL nodig hebt nadat de gegevens reeds zijn ingeslikt, verstrekt de Diensten van de Vraag AEP sommige beperkte opties. |
| **Stitching** |  |
| Kan [!UICONTROL Customer Journey Analytics] &quot;stitch&quot; over apparaten of over datasets? | Nee. [!UICONTROL Customer Journey Analytics] is een &#39;breng-uw-eigen-identiteitskaart&#39; analysesysteem. Plannen voor een goede verstikkende aanpak staan in de werkzaamheden. |
| Wordt het stikken van anoniem gedrag aan voor authentiek verklaard gesteund gedrag? | Nee, nog niet. |
| **Het krijgen van gegevens in[!UICONTROL Customer Journey Analytics]** |  |
| Kan ik gegevens van verschillende sandboxes van het Platform van de Ervaring in één verbinding CJA combineren? | Nee, u hebt geen toegang tot gegevens over sandboxes. U kunt slechts datasets combineren die binnen de zelfde zandbak worden gevestigd. [Meer informatie...](https://docs.adobe.com/content/help/en/analytics-platform/using/cja-connections/create-connection.html#select-sandbox-and-datasets) |
| Wat is de verwachte latentie voor [!UICONTROL Customer Journey Analytics] op [!UICONTROL Experience Platform]? | <ul><li>Onder normale belasting: &lt; 60 minuten <br>**Opmerking:** In het geval van een ongebruikelijk groot gegevensvolume door de pijpleiding kan het tot 24 uur duren.</li><li>Back-upgegevens (tot 10 miljard evenementen): &lt; 4 weken</li></ul> |
| Hoe ik online gegevens aan off-line gegevens in verbind [!UICONTROL Customer Journey Analytics]? | [!UICONTROL Customer Journey Analytics] is een &quot;breng uw eigen identiteitskaart&quot;analysesysteem. Zolang de persoonidentiteitskaart tussen datasets aanpast, [!UICONTROL Customer Journey Analytics] kan segmenten, attributie, stroom, uitval, enz. verbinden. over gegevensreeksen. |
| Hoe breng ik mijn off-line gegevens in de Analyse van de Reis van de Klant? | U moet eerst alle gegevens naar het ervaringsplatform brengen voordat u deze kunt gebruiken bij de analyse van de reis van de klant. De gegevens van het ervaringsplatform over instapniveau kunnen u indien nodig helpen aanbevelingen te doen of advies in te winnen. |
| Hoe krijg ik de gegevens van de Analyse in de Analyse van de Reis van de Klant? | Analytische gegevens kunnen via het [Analytics Data Connector](https://docs.adobe.com/content/help/en/experience-platform/sources/connectors/adobe-applications/analytics.html). De meeste gebieden van de Analyse worden gebracht over in formaat XDM, maar andere gebieden zijn nog niet beschikbaar (als de afmetingen van de Kanalen van de Marketing). |
| Hoe lang duurt het om datasetelementen in een gegevensmening te assembleren? | Een paar uur om te beginnen, en een paar dagen om een back-up te maken van de laatste 13 maanden van gegevens. |
| Is het noodzakelijk om PII gegevens te brengen om verbindingen tussen de gegevens te vestigen? | Nr, kunt u om het even welke identiteitskaart, met inbegrip van een knoeiboel van een klantenidentiteitskaart gebruiken, die geen PII is. |
| **Traditionele analytische onderdelen** |  |
| Wat betekent dit voor ons traditionele product van de Analyse van Adobe? | De Analyse van de Reis van de Klant is ons product van de volgende generatie van de Analyse. Het evolueren van onze huidige producten naar Customer Journey Analytics zal jaren duren en veel coördinatie samen. |
| Kan ik segmenten delen van de Analyse van de Reis van de Klant aan AEP of andere oplossingen? | Nog niet. Wij bekijken nieuwe, innovatieve manieren om segmenten van de Analyse van de Reis van de Klant aan AEP in de toekomst te delen die niet zulk een lange vertraging hebben. Dat gezegd, kunt u de output van de Diensten van de Vraag aan Verenigd Profiel als potentiële alternerende actie delen. |
| Wat is er met mijn oude eVar-omgeving gebeurd? | Vars, props en events in de traditionele Adobe Analytics-betekenis bestaan niet meer in Klantreisanalyse. U hebt onbeperkte schemaelementen (afmetingen, metriek, lijstgebieden). Zo worden alle attributie montages u gebruikte om tijdens het proces van de gegevensinzameling toe te passen nu toegepast in vraagtijd. |
| Waar zijn al mijn zitting en veranderlijke persistentiemontages nu? | De Analyse van de Reis van de klant past elk van deze montages in rapporttijd toe, en deze montages leven nu in de Meningen van Gegevens. De veranderingen in deze montages zijn nu retroactief, en u kunt veelvoudige versies hebben door de veelvoudige Meningen van Gegevens te gebruiken! |
| Wat gebeurt er met onze bestaande segmenten/berekende maatstaven? | De Analyse van de Reis van de klant gebruikt niet meer eVars, steunen, of gebeurtenissen en in plaats daarvan gebruikt om het even welk schema AEP. Dit betekent geen van de bestaande segmenten of calc metriek compatibel zijn met de Analyse van de Reis van de Klant. |
| Hoe behandelt de Analyse van de Reis van de Klant `Uniques Exceeded` beperkingen? | De Analyse van de Reis van de klant heeft geen unieke waardebeperkingen, zodat te hoeven om zich over hen ongerust te maken! |
| Als ik een bestaande [!DNL Data Workbench] klant, kan ik nu naar Klant Journey Analytics overstappen? | Het hangt af. Als u sterk op het Verenigde Proces van de Klant (UCP) baseert, zult u willen wachten tot wij het stikken uitgevoerd hebben. Als u al hoge gebruikersidentificatiesnelheden hebt, of als u al uw gegevens op één plaats wilt hebben, of van eVars wilt afzien, is de analyse van de reis van de Klant wellicht een goede oplossing. |

