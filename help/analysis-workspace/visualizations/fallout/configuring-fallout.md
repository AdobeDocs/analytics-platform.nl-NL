---
description: 'null'
title: Een uitvalvisualisatie configureren
uuid: fc117745-baf3-46fb-873d-9307092cc337
translation-type: tm+mt
source-git-commit: 1fb46acc9c7c70e64058d2c6a8fdcde119910fec
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 2%

---


# Een uitvalvisualisatie configureren

>[!NOTE]
>
>U bekijkt de documentatie voor de Werkruimte van de Analyse in de Analyse van de Reis van de Klant. Zijn eigenschapreeks verschilt lichtjes van [De Werkruimte van de analyse in de traditionele Analyse van Adobe](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/home.html). [Meer informatie...](/help/getting-started/cja-aa.md)

U kunt touchpoints specificeren om een multi-dimensionale uitloopopeenvolging tot stand te brengen. Gewoonlijk is een touchpoint een pagina op je site. touchpoints zijn echter niet beperkt tot pagina&#39;s. Bijvoorbeeld, kunt u gebeurtenissen, zoals eenheden, evenals unieke bezoekers en terugkeerbezoeken toevoegen. U kunt afmetingen, zoals een categorie, browser type, of interne onderzoekstermijn ook toevoegen.

U kunt segmenten binnen een touchpoint zelfs toevoegen. Bijvoorbeeld, zou u segmenten, zoals iOS en Android gebruikers kunnen willen vergelijken. Sleep de gewenste segmenten aan de bovenkant van de uitval en de informatie over die segmenten wordt toegevoegd aan het uitvalrapport. Als u slechts die segmenten wilt tonen, kunt u de Al basislijn van Bezoeken verwijderen.

Er is geen beperking op het aantal stappen u kunt toevoegen of het aantal gebruikte afmetingen.

Je kunt paden op eVars, inclusief merchandising eVars en [lijstVars](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/page-variables.html) (variabelen die meerdere waarden per hit kunnen hebben, zoals producten, listVars, merchandising eVars en list props). Bijvoorbeeld, veronderstel iemand schoenen kijkt, shirt op één pagina, en op de volgende pagina kijken zij naar shirt, sokken. Het volgende productstroomrapport van schoenen zal shirt en sokken zijn, NIET shirt.

1. Sleep een [!UICONTROL Fallout] visualisatie van de drop-down Visualisaties in [!UICONTROL Freeform Table].

1. Sleep de dimensie van de Pagina in de Freeform Lijst en van daar, sleep een pagina (in dit geval, Huis - JJEsquire) in **[!UICONTROL Add TouchPoint]** veld als eerste aanraakpunt.

   ![](assets/fallout1.png)

   Beweeg over een touchpoint om de uitval en andere informatie over dat niveau te zien, zoals de naam van touchpoint, de bezoekerstelling op dat punt, en het succespercentage voor dat touchpoint te zien (en het succespercentage met andere touchpoints te vergelijken).

   De omcirkelde aantallen in het grijze gedeelte van de bar tonen de uitval tussen touchpoints (niet de algemene neerslag aan dat punt). Het Touchpoint % toont de geslaagde doorbraak van de vorige stap naar de huidige stap in het uitvalrapport.

   U kunt één enkele pagina aan het eindrapport, eerder dan de volledige dimensie ook toevoegen. Klik de juiste pijl &quot;>&quot;op de paginafmeting om de specifieke pagina te kiezen om aan het reserverapport toe te voegen.

1. Blijf toevoegend touchpoints tot uw opeenvolging volledig is.

   U kunt **meerdere aanraakpunten combineren** door één of meerdere extra degenen op een touchpoint te slepen.

   >[!NOTE]
   >
   >De veelvoudige Segmenten worden aangesloten bij EN, maar de veelvoudige punten zoals afmetingspunten en metriek worden aangesloten bij OF.

   ![](assets/multiple_obj_touchpoint.png)

1. U kunt ook **beperk individuele touchpoints aan de volgende klap** (in tegenstelling tot &quot;uiteindelijk&quot;) binnen het pad. Onder elk touchpoint, is er een selecteur met de opties &quot;Eventuele Weg&quot;en &quot;Volgende Hit&quot;, zoals hier getoond:

   ![](assets/next-hit-eventually.png)

<table id="table_A91D99D9364B41929CC5A5BC907E8985"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Uiteindelijk pad </p> <p>(standaard) </p> </td> 
   <td colname="col2"> <p>De bezoekers worden geteld die "uiteindelijk"op de volgende pagina in de weg zullen landen, maar niet noodzakelijk op de volgende klap. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Volgende uur </p> </td> 
   <td colname="col2"> <p>De bezoekers worden geteld die op de volgende pagina in de weg op de zeer volgende klap zullen landen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Afvalinstellingen {#section_0C7C89D72F0B4D6EB467F278AC979093}

| Instelling | Beschrijving |
|--- |--- |
| valcontainer <ul><li>Bezoek</li><li>Bezoeker</li></ul> | Laat u tussen Bezoek en Bezoeker schakelen om bezoekerspad te analyseren. Het gebrek is Bezoeker.  Met deze instellingen kunt u de betrokkenheid van bezoekers op bezoekersniveau (voor verschillende bezoeken) begrijpen of de analyse beperken tot één bezoek. |
| Toon &quot;Alle Bezoekers&quot; als eerste touchpoint | U kunt dit deselecteren als u liever niet &quot;Alle bezoekers&quot; als eerste touchpoint hebt. |

Wanneer u **klik met de rechtermuisknop op een aanraakpunt**, worden de volgende opties weergegeven:

| Optie | Beschrijving |
|--- |--- |
| Trend touchpoint | Zie trendgegevens voor een touchpoint in een lijngrafiek, met sommige pre-gebouwde anomalieopsporingsgegevens. |
| Trend touchpoint (%) | Trends het totale reservepercentage. |
| Trend alle touchpoints (%) | Trends alle touchpoint percentages in de uitval (behalve &quot;Alle Bezoekingen&quot;, als deze zijn inbegrepen), op dezelfde grafiek. |
| De onderbreking in dit touchpoint | Bekijk wat bezoekers tussen twee touchpoints (dit touchpoint en het volgende touchpoint) deden als ze naar het volgende touchpoint gingen. Dit leidt tot een vrije vormlijst die uw afmetingen toont. U kunt afmetingen en andere elementen van de lijst vervangen. |
| De uitval van dit touchpoint uitsplitsen | Bekijk wat mensen die het niet door de trechter haalden onmiddellijk na de geselecteerde stap deden. |
| Creeer segment van touchpoint | Creeer een nieuw segment van geselecteerd touchpoint. |
