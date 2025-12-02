---
title: Customer Journey Analytics-handleiding voor snel starten
description: Inzicht in de vereisten en workflow die vereist zijn om Customer Journey Analytics te implementeren.
exl-id: cab218c0-009c-4669-9dfb-f8872a7f066b
solution: Customer Journey Analytics
feature: Basics
role: User
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 1%

---

# Handleiding voor snel starten

Als u Customer Journey Analytics wilt implementeren, moet u deze workflow volgen. Sommige initiële taken worden uitgevoerd in Adobe Experience Platform en sommige in Customer Journey Analytics.

## Vereisten

Customer Journey Analytics is beschikbaar voor klanten die

* Zijn provisioned voor [&#x200B; Adobe Experience Platform &#x200B;](https://www.adobe.com/experience-platform.html), en
* Customer Journey Analytics SKU hebben aangeschaft

## Workflow

| Taak | Details |
| --- | --- |
| **Stap 1: Als u van Adobe Analytics aan Customer Journey Analytics bevordert: Kies een verbeteringspad en verzend gegevens naar Adobe Experience Platform** | Er zijn verschillende paden beschikbaar wanneer u een upgrade uitvoert van Adobe Analytics naar Customer Journey Analytics. Elk mogelijk upgradepad heeft zijn eigen voor- en nadelen en een pad dat geschikt is voor de ene organisatie heeft misschien geen zin voor de andere. <p>Voer een van de volgende twee handelingen uit om een upgrade uit te voeren van Adobe Analytics naar Customer Journey Analytics:</p><ul><li>Volg het door Adobe aanbevolen upgradepad. Voor meer informatie, zie [&#x200B; Geadviseerde weg wanneer bevordering van Adobe Analytics aan Customer Journey Analytics &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md).</li><li>Leer over alle beschikbare verbeteringspaden en kies de weg die uw organisatie het beste past. Voor meer informatie, zie [&#x200B; begonnen worden met de verbetering aan Customer Journey Analytics &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-getstarted.md).</li></ul> |
| **Stap 2: Krijg andere gegevens in Adobe Experience Platform** | Deze stap, uitgevoerd in Adobe Experience Platform, omvat verschillende substappen:<ul><li>**Stap 2a: Bereid uw gegevensschema** voor: Het Model van de Gegevens van de Ervaring van Adobe van het gebruik [&#x200B; (XDM) &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) om gegevens van de klantenervaring te standaardiseren en [&#x200B; schema&#39;s &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html) voor het beheer van de klantenervaring te bepalen.</li><li>**Stap 2b: Creeer een dataset die op het schema** wordt gebaseerd: De gegevens in Platform bestaan uit datasets, zoals e-maildatasets, de datasets van CRM, POS datasets, de dataset van Adobe Analytics, enz. Elke dataset bestaat uit een schema en partijen gegevens. U kunt [&#x200B; tot een dataset in Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/create-datasets.html) leiden.</li><li>**Stap 2c: De samenvattingsgegevens in Experience Platform**: Hier, hebt u verscheidene opties.</li></ul> |
| **Stap 3: Creeer verbindingen tussen platformdatasets en Customer Journey Analytics** | Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over de datasets van Experience Platform te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en Workspace vestigen.<br> zie [&#x200B; creeer of geef een verbinding &#x200B;](/help/connections/create-connection.md) uit. |
| **Stap 4: Creeer gegevensmeningen** | Een gegevensweergave is een gefilterde weergave van de gegevens. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, de toewijzing, enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen.<br> zie [&#x200B; een gegevensmening &#x200B;](/help/data-views/create-dataview.md) creëren. |
| **Stap 5: Haven het melden API gebruik**</br> is slechts van toepassing wanneer het migreren van Adobe Analytics | De Customer Journey Analytics-API voor rapportage heeft dezelfde indeling, maar gebruikt een ander eindpunt. Geef het API-gebruik voor rapportage door van de Adobe Analytics-API voor rapportage naar de Customer Journey Analytics-API voor rapportage. |
| **Stap 6: De rekening voor de gebruiksgevallen van de Diervoeders van Gegevens en Data Warehouse**</br> is slechts van toepassing wanneer het migreren van Adobe Analytics | Bepaal hoe u de exportopties die beschikbaar zijn in Customer Journey Analytics, wilt gebruiken om de gegevensfeeds en Data Warehouse-functies die u in Adobe Analytics gebruikte, het beste te repliceren. <!-- link to docs Rob is creating --> |
| **Stap 7: Migreer projecten en componenten**</br> is slechts van toepassing wanneer het migreren van Adobe Analytics | In het gebied voor componentmigratie in Adobe Analytics kunt u projecten en de bijbehorende onderdelen migreren van Adobe Analytics naar Customer Journey Analytics.<p>Het migratieproces omvat:</p><ul><li>Adobe Analytics-projecten opnieuw maken in Customer Journey Analytics.</li><li>Mapping dimensies and metrics from Adobe Analytics report suites to afmetingen and metrics in Customer Journey Analytics data views.</li></ul><p>Alvorens u met de migratie begint, eerst [&#x200B; voorbereidingen treffen om componenten en projecten van Adobe Analytics aan Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration/prepare-component-migration.html) te migreren.</p><p>Nadat u alle noodzakelijke voorbereidingen maakt, kunt u [&#x200B; componenten en projecten van Adobe Analytics aan Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration/component-migration.html) migreren.</p> |
| **Stap 8: De gebruiker van het plan onboarding** | Net als in Adobe Analytics is Analysis Workspace het belangrijkste gebruikersgerichte hulpmiddel in Customer Journey Analytics. Er zijn echter enkele belangrijke verschillen bij het gebruik van Analysis Workspace in Customer Journey Analytics die gebruikers moeten onthouden.<p>Geef uw gebruikers voldoende tijd (3 tot 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Analysis Workspace in Customer Journey Analytics.</p><p>Voor informatie over enkele zeer belangrijke verschillen tussen Adobe Analytics en Customer Journey Analytics, zie [&#x200B; Gids van de Gebruiker voor de gebruikers van Adobe Analytics &#x200B;](/help/getting-started/aa-to-cja-user.md).</p> |
| **Stap 9: Rapport over uw dwars-kanaalgegevens in Workspace** | Nadat u verbindingen en gegevensmeningen hebt gecreeerd, analyseer de gegevens u binnen gebruikend de macht en de flexibiliteit van Analysis Workspace hebt gebracht.<br> zie [&#x200B; basisanalyse &#x200B;](/help/analysis-workspace/perform-basic-analysis.md) uitvoeren en [&#x200B; geavanceerde analyse &#x200B;](/help/analysis-workspace/perform-adv-analysis.md) uitvoeren. |

## Hulplijnen voor snel starten

De [&#x200B; Inname van Gegevens &#x200B;](../data-ingestion/data-ingestion.md) sectie verstrekt snelle begingidsen op het werkschema hierboven. Deze snelstarthulplijnen tonen hoe u gegevens uit verschillende bronnen (waaronder Adobe Analytics) in Adobe Experience Platform kunt invoeren en deze gegevens vervolgens in Customer Journey Analytics kunt gebruiken.
