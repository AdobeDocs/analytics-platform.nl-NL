---
title: Aan de slag met Customer Journey Analytics
description: Inzicht in de vereisten en workflow die vereist zijn om Customer Journey Analytics te implementeren.
exl-id: cab218c0-009c-4669-9dfb-f8872a7f066b
solution: Customer Journey Analytics
feature: Basics
role: User
source-git-commit: 01df8b8b55ff8e8c0826bf98adfbd85d3412e6bb
workflow-type: tm+mt
source-wordcount: '787'
ht-degree: 1%

---

# Aan de slag met Customer Journey Analytics

Volg deze workflow om Customer Journey Analytics te implementeren. Sommige initiële taken worden uitgevoerd in Adobe Experience Platform, en andere in Customer Journey Analytics.

## Vereisten

Customer Journey Analytics is beschikbaar voor klanten die

* Zijn provisioned voor [ Adobe Experience Platform ](https://www.adobe.com/experience-platform.html), en
* De Customer Journey Analytics SKU hebben aangeschaft

## Workflow

| Taak | Details |
| --- | --- |
| **Stap 1: Als u van Adobe Analytics aan Customer Journey Analytics bevordert: Kies een verbeteringspad en verzend gegevens naar Adobe Experience Platform** | Er zijn verschillende paden beschikbaar wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics. Elk mogelijk upgradepad heeft zijn eigen voor- en nadelen en een pad dat geschikt is voor de ene organisatie heeft misschien geen zin voor de andere. <p>Voer een van de volgende twee handelingen uit om een upgrade uit te voeren van Adobe Analytics naar Customer Journey Analytics:</p><ul><li>Volg het upgradepad dat door de Adobe wordt aanbevolen. Voor meer informatie, zie [ Geadviseerde weg wanneer het bevorderen van Adobe Analytics aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).</li><li>Lees meer over alle beschikbare upgradepaden en kies het pad dat het beste past bij uw organisatie. Voor meer informatie, zie [ begonnen worden met de verbetering aan Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-getstarted.md).</li></ul> |
| **Stap 2: Krijg andere gegevens in Adobe Experience Platform** | Deze stap, uitgevoerd in Adobe Experience Platform, bestaat uit verschillende substappen:<ul><li>**Stap 2a: Bereid uw gegevensschema** voor: Het Model van de Gegevens van de Ervaring van het gebruik [ (XDM) ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) om de gegevens van de klantervaring te standaardiseren en [ schema&#39;s ](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html) voor het beheer van de klantervaring te bepalen.</li><li>**Stap 2b: Creeer een dataset die op het schema** wordt gebaseerd: De gegevens in Platform bestaat uit datasets, zoals e-maildatasets, de datasets van CRM, POS datasets, de dataset van Adobe Analytics, enz. Elke dataset bestaat uit een schema en batches gegevens. U kunt [ een dataset in Experience Platform ](https://experienceleague.adobe.com/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/create-datasets.html) tot stand brengen.</li><li>**Stap 2c: Voeg gegevens in Experience Platform** in: Hier, hebt u verscheidene opties.</li></ul> |
| **Stap 3: Creeer verbindingen tussen platformdatasets en Customer Journey Analytics** | Met een verbinding kunt u datasets van Adobe Experience Platform integreren in Workspace. Om over de datasets van het Experience Platform te rapporteren, moet u eerst een verbinding tussen datasets in Experience Platform en Werkruimte vestigen.<br> zie [ creeer of geef een verbinding ](/help/connections/create-connection.md) uit. |
| **Stap 4: Creeer gegevensmeningen** | Een gegevensweergave is een gefilterde weergave van de gegevens. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, de toewijzing, enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen.<br> zie [ een gegevensmening ](/help/data-views/create-dataview.md) creëren. |
| **Stap 5: Haven het melden API gebruik**</br> is slechts van toepassing wanneer het migreren van Adobe Analytics | De Customer Journey Analytics die API rapporteert, heeft dezelfde indeling, maar gebruikt een ander eindpunt. Geef het API-gebruik voor rapportage door van de Adobe Analytics-rapportage-API naar de Customer Journey Analytics-rapportage-API. |
| **Stap 6: De rekening voor het gebruiksgevallen van de Diervoeders van Gegevens en van de Data Warehouse**</br> is slechts van toepassing wanneer het migreren van Adobe Analytics | Bepaal hoe u de exportopties gebruikt die beschikbaar zijn in de Customer Journey Analytics om de gegevensfeeds en -Data Warehouse die u in Adobe Analytics gebruikte het beste te repliceren. <!-- link to docs Rob is creating --> |
| **Stap 7: Migreer projecten en componenten**</br> is slechts van toepassing wanneer het migreren van Adobe Analytics | In het gebied voor componentmigratie in Adobe Analytics kunt u projecten en de bijbehorende onderdelen migreren van Adobe Analytics naar Customer Journey Analytics.<p>Het migratieproces omvat:</p><ul><li>Adobe Analytics-projecten opnieuw maken in Customer Journey Analytics.</li><li>Mapping dimensies en metrics van Adobe Analytics-rapportsuites aan dimensies en metrics in dataweergaven van Customers Journey Analytics.</li></ul><p>Alvorens u met de migratie begint, voorbereidingen eerst [ om componenten en projecten van Adobe Analytics aan Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration.html) te migreren.</p><p>Nadat u alle noodzakelijke voorbereidingen maakt, kunt u [ componenten en projecten van Adobe Analytics aan Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration/component-migration.html) migreren.</p> |
| **Stap 8: Het gebruikersonboarden van het plan** | Net als in Adobe Analytics is Analysis Workspace het belangrijkste gebruikersgerichte hulpmiddel in de Customer Journey Analytics. Er zijn echter enkele belangrijke verschillen bij het gebruik van Analysis Workspace in de Customer Journey Analytics die gebruikers moeten onthouden.<p>Geef uw gebruikers voldoende tijd (3 - 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Customer Journey Analytics van Analysis Workspace.</p><p>Voor informatie over enkele zeer belangrijke verschillen tussen Adobe Analytics en Customer Journey Analytics, zie [ Gids van de Gebruiker voor de gebruikers van Adobe Analytics ](/help/getting-started/aa-to-cja-user.md).</p> |
| **Stap 9: Rapport over uw dwars-kanaalgegevens in Workspace** | Nadat u verbindingen en gegevensmeningen hebt gecreeerd, analyseer de gegevens u binnen gebruikend de macht en de flexibiliteit van Analysis Workspace hebt gebracht.<br> zie [ basisanalyse ](/help/analysis-workspace/perform-basic-analysis.md) uitvoeren en [ geavanceerde analyse ](/help/analysis-workspace/perform-adv-analysis.md) uitvoeren. |

## Hulplijnen voor snel starten

De [ Inname van Gegevens ](../data-ingestion/data-ingestion.md) sectie verstrekt snelle begingidsen op het werkschema hierboven. Deze snelstarthulplijnen tonen hoe u gegevens uit verschillende bronnen (waaronder Adobe Analytics) in Adobe Experience Platform kunt invoeren en deze gegevens vervolgens in de Customer Journey Analytics kunt gebruiken.
