---
title: Voeg de gegevensset van de bron van de Analyse aan de verbinding toe
description: Leer hoe te om de gegevensreeks van de bron van Analytics aan de verbinding toe te voegen
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 424485a3-a076-4656-83b6-733f16cc2326
source-git-commit: 03e9fb37684f8796a18a76dc0a93c4e14e6e7640
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Voeg de gegevensset van de bron van de Analyse aan de verbinding toe {#upgrade-source-connector-dataset}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-source-connector-dataset"
>title="Voeg de gegevensset van de bron van de Analyse aan uw verbinding toe"
>abstract="Nu de historische gegevens uit uw Analytics-rapportenreeks zich in Adobe Experience Platform bevinden, voegt u die gegevensset toe aan uw bestaande verbinding die u hebt gemaakt toen u Customer Journey Analytics voor het eerst configureerde. Zodra deze stap is voltooid, zijn historische gegevens beschikbaar in Customer Journey Analytics.<br><br> Toevoegend een dataset aan een verbinding in Customer Journey Analytics is ongecompliceerd, die slechts een paar minuten neemt om te voltooien."

<!-- markdownlint-enable MD034 -->

{{upgrade-note-step}}

## Begrijp hoe de de bronschakelaar van de Analyse historische gegevens in Customer Journey Analytics kan brengen

U kunt de Analytics-bronconnector gebruiken om Adobe Analytics-rapportsuite-gegevens over te brengen naar Adobe Experience Platform. Deze gegevens kunnen vervolgens worden gebruikt als historische gegevens in Customer Journey Analytics.

Dit proces veronderstelt dat u een schema wilt [ tot stand brengen XDM wanneer het bevorderen aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md), omdat u een gestroomlijnd schema wilt dat aan de behoeften van uw organisatie en de specifieke toepassingen van het Platform wordt aangepast die u gebruikt.

Als u de Analytics-bronconnector wilt gebruiken om historische gegevens over te brengen naar Customer Journey Analytics, moet u:

1. [Maak een XDM-schema voor de bronconnector van Analytics](/help/getting-started/cja-upgrade/cja-upgrade-source-connector-schema.md)

1. Als u reeds geen Analytics bronschakelaar hebt, [ creeer de Analytics bronschakelaar en kaartgebieden aan uw XDM schema ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector.md).

   of

   Als u reeds een Analytics bronschakelaar hebt, [ kaartgebieden van de bronschakelaar aan uw schema XDM ](/help/getting-started/cja-upgrade/cja-upgrade-from-source-connector.md).

1. Voeg de gegevensset van de bron van Analytics aan de verbinding toe, zoals hieronder beschreven.

## Voeg de gegevensset van de bron van de Analyse aan de verbinding toe

Nadat u [ een Analytics bronschakelaar voor historische gegevens ](/help/getting-started/cja-upgrade/cja-upgrade-source-connector.md) creeert, wordt een dataset automatisch gecreeerd voor de gegevens van Analytics.

U moet deze automatisch gecreeerde dataset aan de zelfde verbinding toevoegen die u voor uw implementatie van SDK van het Web creeerde. Dit brengt de gegevens van Analytics in de zelfde gegevensmening in Customer Journey Analytics zoals uw gegevens van Web SDK.

Om de automatisch gecreeerde dataset aan de zelfde verbinding toe te voegen die u voor uw implementatie van SDK van het Web creeerde:

1. Selecteer in Customer Journey Analytics **[!UICONTROL Connections]** (optioneel in **[!UICONTROL Data management]** ) in het bovenste menu.

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
   | **[!UICONTROL Person ID]** | Alleen beschikbaar voor gebeurtenis- en profielgegevenssets. Selecteer een persoon-id in de vervolgkeuzelijst met beschikbare identiteiten. Deze identiteiten werden bepaald in het datasetschema in Experience Platform. Zie hieronder voor informatie over het gebruik van Identiteitskaart als Persoon identiteitskaart<p>Als er geen persoon-id&#39;s zijn waaruit u kunt kiezen, betekent dit dat een of meer personen-id&#39;s niet zijn gedefinieerd in het schema. Zie [ identiteitsgebieden in UI ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity) voor meer informatie bepalen. <p>De waarde voor de geselecteerde persoon-id wordt als hoofdlettergevoelig beschouwd. `abc123` en `ABC123` zijn bijvoorbeeld twee verschillende waarden. |
   | **[!UICONTROL Timestamp]** | Alleen voor gebeurtenis- en samenvattingsgegevenssets wordt deze instelling automatisch ingesteld op het standaardtijdstempelveld vanuit op gebeurtenissen gebaseerde schema&#39;s in Experience Platform. |
   | **[!UICONTROL Timezone]** | Alleen beschikbaar voor samenvattingsgegevens. Selecteer de aangewezen tijdzone voor de tijdreekssummiere gegevens. |
   | **[!UICONTROL Data source type]** | Selecteer een type gegevensbron. <br/> de Types van gegevensbronnen omvatten: <ul><li>[!UICONTROL Web data]</li><li>[!UICONTROL Mobile App data]</li><li>[!UICONTROL POS data]</li><li>[!UICONTROL CRM data]</li><li>[!UICONTROL Survey data]</li><li>[!UICONTROL Call Center data]</li><li>[!UICONTROL Product data]</li><li> [!UICONTROL Accounts data]</li><li> [!UICONTROL Transaction data]</li><li>[!UICONTROL Customer Feedback data]</li><li> [!UICONTROL Other]</li></ul>Dit veld wordt gebruikt om de typen gebruikte gegevensbronnen te controleren. |

   {style="table-layout:auto"}

1. Laat in de sectie **[!UICONTROL Import new data]** de optie **[!UICONTROL Import all new data]** uitgeschakeld.

   Omdat u de gegevensset van de de bronschakelaar van de Analyse voor historische gegevens gebruikt, wilt u geen toekomstige gegevens brengen die in deze dataset worden verzameld.

1. Selecteer **[!UICONTROL Request backfill]** in de sectie **[!UICONTROL Dataset backfill]** .

1. Bepaal de periode die u de verbindingsbackfill in Customer Journey Analytics wilt omvatten door de begin en einddata in te gaan of door het kalenderpictogram ![ Kalender ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Calendar_18_N.svg) te selecteren.

   Wees expliciet wanneer u de datums opgeeft die u wilt terugvullen. Afhankelijk van verschillende factoren kunt u een van de volgende handelingen uitvoeren:

   * Kies een einddatum die de zelfde datum is zoals toen u eerst begonnen gegevens met uw implementatie van SDK van het Web te verzamelen.

   * Kies een einddatum die kort na de datum is toen u eerst begonnen gegevens met uw implementatie van SDK van het Web te verzamelen, dan de segmenten van de gegevensmening te gebruiken om de overlappende gegevens uit te filteren.

   * Kies een einddatum die resulteert in een grotere gegevensoverlapping en gebruik vervolgens de segmenten van de gegevensweergave om de overlappende gegevens uit te filteren.

     **Nota:** Deze optie zou in verhoogde kosten resulteren omdat er meer rijen in de verbinding zouden zijn.

   <!-- Include any of the following?  Make sure you're explicit as to the dates you request backfill to. You want to request it to the date that you start gathering data with your Web SDK implementation. Also possibly include segments for any overlapping date. So you could request everything and then use a segment to exclude data that you don't want. That way if you need to move up the date, then you could change the date in the filter. Downside would be that you might pay for double rows.  When they do that, they're going to see all schema fields from both their custom schema and their Analytics schema. So they'll need to be cognizant to select the right fields, and never select any Analytics fields, because they will be mapped as part of the source connector. Never select any Analytics field group fields because they'll be mapped.  -->

1. Selecteer **[!UICONTROL Queue backfill]** .

1. Selecteer **[!UICONTROL Add datasets]** en selecteer vervolgens **[!UICONTROL Save]** om de verbinding op te slaan.

1. (Voorwaardelijk) als u raadplegingsdatasets gebruikt, moet u de raadplegingsdataset tot stand brengen en het toevoegen aan uw verbinding. Voor meer informatie, zie [ raadplegingsdatasets creëren om gegevens in Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-dataset-lookup.md) te classificeren.

   Dit is alleen vereist als u dit nog niet hebt gedaan bij het configureren van uw Web SDK-implementatie.

{{upgrade-final-step}}
