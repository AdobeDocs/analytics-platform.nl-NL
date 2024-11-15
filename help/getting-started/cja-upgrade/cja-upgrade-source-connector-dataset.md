---
title: Voeg de gegevensset van de bron van de Analyse aan de verbinding toe
description: Leer hoe te om de gegevensreeks van de bron van Analytics aan de verbinding toe te voegen
role: Admin
solution: Customer Journey Analytics
feature: Basics
hide: true
hidefromtoc: true
exl-id: 424485a3-a076-4656-83b6-733f16cc2326
source-git-commit: aedf7a2ad41b09521938b789dbaf1c193cdb661f
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Voeg de gegevensset van de bron van de Analyse aan de verbinding toe

>[!NOTE]
> 
>Voer de stappen op deze pagina pas uit nadat u alle vorige upgradestappen hebt uitgevoerd. U kunt de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) volgen, of u kunt de verbeteringsstappen volgen die dynamisch voor uw organisatie met [ Adobe Analytics aan de verbeteringsvragenlijst van de Customer Journey Analytics ](https://gigazelle.github.io/cja-ttv/) werden geproduceerd.
>
>Nadat u de stappen op deze pagina hebt uitgevoerd, gaat u door met het volgen van de aanbevolen upgradestappen of de dynamisch gegenereerde upgradestappen.

>[!NOTE]
>
>De informatie op deze pagina gaat uit van het volgende:
>
>* U gaat een upgrade uitvoeren van Adobe Analytics naar Customer Journey Analytics.
>* U gebruikt SDK van het Web voor uw toekomstige gegevensinzameling van de Customer Journey Analytics.
>* U wilt de de bronschakelaar van de Analyse gebruiken om uw historische gegevens van de Adobe te brengen in Customer Journey Analytics.

## Begrijp hoe de de bronschakelaar van de Analyse historische gegevens in Customer Journey Analytics kan brengen

U kunt de Analytics-bronconnector gebruiken om Adobe Analytics-rapportsuite-gegevens over te brengen naar Adobe Experience Platform. Deze gegevens kunnen vervolgens als historische gegevens in Customer Journey Analytics worden gebruikt.

Dit proces veronderstelt dat u een schema wilt [ tot stand brengen XDM wanneer het bevorderen aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md), omdat u een gestroomlijnd schema wilt dat aan de behoeften van uw organisatie en de specifieke toepassingen van het Platform wordt aangepast die u gebruikt.

Om de bron van Analytics schakelaar te gebruiken om historische gegevens in Customer Journey Analytics te brengen, moet u:

1. [Maak een XDM-schema voor de bronconnector van Analytics](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-schema.md)

1. [De bronaansluiting voor Analytics en kaartvelden maken](/help/getting-started/cja-upgrade/cja-upgrade-source-connector.md)

1. Voeg de gegevensset van de bron van Analytics aan de verbinding toe, zoals hieronder beschreven.

## Voeg de gegevensset van de bron van de Analyse aan de verbinding toe

Nadat u [ een Analytics bronschakelaar voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector.md) creeert, wordt een dataset automatisch gecreeerd voor de gegevens van Analytics.

U moet deze automatisch gecreeerde dataset aan de zelfde verbinding toevoegen die u voor uw implementatie van SDK van het Web creeerde. Dit brengt de gegevens van Analytics in de zelfde gegevensmening in Customer Journey Analytics zoals uw gegevens van SDK van het Web.

Om de automatisch gecreeerde dataset aan de zelfde verbinding toe te voegen die u voor uw implementatie van SDK van het Web creeerde:

1. Selecteer in Customer Journey Analytics de tab **[!UICONTROL Connections]** .

1. Selecteer de verbinding die u [ voor uw implementatie van SDK van het Web ](/help/getting-started/cja-upgrade/cja-upgrade-connection.md) creeerde.

1. Selecteer **[!UICONTROL Edit]** .

   ![ geef verbinding ](assets/connection-add-dataset.png) uit

1. Selecteer **[!UICONTROL Add datasets]** rechtsboven.

   ![ geef verbinding ](assets/connection-add-dateset2.png) uit

1. De rol aan of onderzoek naar de dataset die automatisch werd gecreeerd toen u de Analytics bronschakelaar creeerde.

   De naam van deze gegevensset is de naam van uw rapportsuite, gevolgd door `midValues` . Bijvoorbeeld: `My report suite midValues`

1. Schakel het selectievakje naast de naam van de gegevensset in en selecteer vervolgens **[!UICONTROL Next]** .

   ![ geef verbinding ](assets/connection-add-dataset3.png) uit

1. Geef de volgende informatie op:

   <!-- Copied from help/connections/create-connection.md. Should we single source? -->

   | Instelling | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Person ID]** | Alleen beschikbaar voor gebeurtenis- en profielgegevenssets. Selecteer een persoon-id in de vervolgkeuzelijst met beschikbare identiteiten. Deze identiteiten werden bepaald in het datasetschema in het Experience Platform. Zie hieronder voor informatie over het gebruik van Identiteitskaart als Persoon identiteitskaart<p>Als er geen persoon-id&#39;s zijn waaruit u kunt kiezen, betekent dit dat een of meer personen-id&#39;s niet zijn gedefinieerd in het schema. Zie [ identiteitsgebieden in UI ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity) voor meer informatie bepalen. <p>De waarde voor de geselecteerde persoon-id wordt als hoofdlettergevoelig beschouwd. `abc123` en `ABC123` zijn bijvoorbeeld twee verschillende waarden. |
   | **[!UICONTROL Timestamp]** | Alleen voor gebeurtenis- en samenvattingsgegevenssets wordt deze instelling automatisch ingesteld op het standaardtijdstempelveld van op gebeurtenissen gebaseerde schema&#39;s in Experience Platform. |
   | **[!UICONTROL Timezone]** | Alleen beschikbaar voor samenvattingsgegevens. Selecteer de aangewezen tijdzone voor de tijdreekssummiere gegevens. |
   | **[!UICONTROL Data source type]** | Selecteer een type gegevensbron. <br/> de Types van gegevensbronnen omvatten: <ul><li>[!UICONTROL Web data]</li><li>[!UICONTROL Mobile App data]</li><li>[!UICONTROL POS data]</li><li>[!UICONTROL CRM data]</li><li>[!UICONTROL Survey data]</li><li>[!UICONTROL Call Center data]</li><li>[!UICONTROL Product data]</li><li> [!UICONTROL Accounts data]</li><li> [!UICONTROL Transaction data]</li><li>[!UICONTROL Customer Feedback data]</li><li> [!UICONTROL Other]</li></ul>Dit veld wordt gebruikt om de typen gebruikte gegevensbronnen te controleren. |

   {style="table-layout:auto"}

1. Laat in de sectie **[!UICONTROL Import new data]** de optie **[!UICONTROL Import all new data]** uitgeschakeld.

   Omdat u de gegevensset van de de bronschakelaar van de Analyse voor historische gegevens gebruikt, wilt u geen toekomstige gegevens brengen die in deze dataset worden verzameld.

1. Selecteer **[!UICONTROL Request backfill]** in de sectie **[!UICONTROL Dataset backfill]** .

1. Bepaal de periode die u backfill wilt omvatten door de begin en einddata in te gaan of door het kalenderpictogram ![ Kalender ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg) te selecteren.

   De bronschakelaar van de Analyse voert 13 maanden van gegevens (ongeacht grootte) voor productiesandboxen in. De back-up van niet-productie sandboxen is 3 maanden.

   >[!IMPORTANT]
   >
   >Wees expliciet wanneer u de datums opgeeft die u wilt terugvullen. De einddatum zou de datum moeten zijn toen u eerst begonnen gegevens met uw implementatie van SDK van het Web te verzamelen.
   >
   >Alternatief, kunt u een datum kiezen kort na de datum toen u eerst begonnen gegevens met uw implementatie van SDK van het Web te verzamelen, dan gebruiksegmenten om de overlappende gegevens uit te filteren.

   <!-- Include any of the following?  Make sure you're explicit as to the dates you request backfill to. You want to request it to the date that you start gathering data with your Web SDK implementation. Also possibly include segments for any overlapping date. So you could request everything and then use a segment to exclude data that you don't want. That way if you need to move up the date, then you could change the date in the filter. Downside would be that you might pay for double rows.  When they do that, they're going to see all schema fields from both their custom schema and their Analytics schema. So they'll need to be cognizant to select the right fields, and never select any Analytics fields, because they will be mapped as part of the source connector. Never select any Analytics field group fields because they'll be mapped.  -->

1. Selecteer **[!UICONTROL Queue backfill]** .

1. Selecteer **[!UICONTROL Add datasets]** en selecteer vervolgens **[!UICONTROL Save]** om de verbinding op te slaan.

1. Ga na de [ geadviseerde verbeteringsstappen ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md#recommended-upgrade-steps-for-most-organizations) of [ dynamisch geproduceerde verbeteringsstappen ](https://gigazelle.github.io/cja-ttv/) verder.
