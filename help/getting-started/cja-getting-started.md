---
title: Aan de slag met Customer Journey Analytics
description: Inzicht in de vereisten en workflow die vereist zijn om Customer Journey Analytics te implementeren.
exl-id: cab218c0-009c-4669-9dfb-f8872a7f066b
solution: Customer Journey Analytics
feature: Basics
role: User
source-git-commit: 7bc4425f11980780ab64a201029cd63e4bd7849c
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 1%

---

# Aan de slag met Customer Journey Analytics

Voor het implementeren van Customer Journey Analytics moet u deze workflow volgen. Sommige initiële taken worden uitgevoerd in Adobe Experience Platform en andere in Customer Journey Analytics.

## Vereisten

Customer Journey Analytics is beschikbaar voor klanten die

* zijn ingericht voor [Adobe Experience Platform](https://www.adobe.com/experience-platform.html), en
* De Customer Journey Analytics SKU hebben aangeschaft

## Workflow

| Taak | Details |
| --- | --- |
| **Stap 1: Als u van Adobe Analytics naar Customer Journey Analytics migreert: kies een migratiepad en verzend gegevens naar Adobe Experience Platform** | Er zijn verschillende paden beschikbaar voor het migreren van Adobe Analytics naar Customer Journey Analytics. Elk mogelijk migratiepad heeft zijn eigen voor- en nadelen, en een pad dat geschikt is voor de ene organisatie heeft misschien geen zin voor de andere. <p>Ga voor een migratie van Adobe Analytics naar Customer Journey Analytics naar [Aan de slag met de migratie naar Customer Journey Analytics](/help/getting-started/cja-migration/cja-migration-getstarted.md). <!-- [Utilizing Adobe Analytics report suite data in Customer Journey Analytics](/help/getting-started/aa-vs-cja/aa-data-in-cja.md) --> </p> |
| **Stap 2: Andere gegevens in Adobe Experience Platform ophalen** | Deze stap, uitgevoerd in Adobe Experience Platform, omvat verschillende substappen:<ul><li>**Stap 2a: Bereid uw gegevensschema voor**: Gebruik [Adobe Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) om de gegevens van de klantervaring te standaardiseren en [schema&#39;s definiëren](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html) voor het beheer van de gebruikerservaring.</li><li>**Stap 2b: Creeer een dataset die op het schema wordt gebaseerd**: De gegevens in Platform bestaan uit gegevenssets, zoals e-mailgegevenssets, CRM-gegevenssets, POS-gegevenssets, de Adobe Analytics-gegevensset, enz. Elke dataset bestaat uit een schema en partijen gegevens. U kunt [een dataset in Experience Platform creëren](https://experienceleague.adobe.com/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/create-datasets.html).</li><li>**Stap 2c: Gegevens opnemen in Experience Platform**: Hier hebt u verschillende opties.</li></ul> |
| **Stap 3: Creeer verbindingen tussen platformdatasets en Customer Journey Analytics** | Met een verbinding kunt u gegevenssets van Adobe Experience Platform integreren in Workspace. Om over de datasets van het Experience Platform te rapporteren, moet u eerst een verband tussen datasets in Experience Platform en Werkruimte vestigen.<br>Zie [Verbinding maken of bewerken](/help/connections/create-connection.md). |
| **Stap 4: Gegevensweergaven maken** | Een gegevensweergave is een gefilterde weergave van de gegevens. U kunt verschillende gegevensweergaven maken voor dezelfde verbinding, met verschillende instellingen voor de time-out van een bezoek, de toewijzing, enzovoort. U kunt veelvoudige gegevensmeningen voor één enkele dataset tot stand brengen.<br>Zie [Een gegevensweergave maken](/help/data-views/create-dataview.md). |
| **Stap 5: Poort het rapport API-gebruik**</br> Alleen van toepassing bij migreren uit Adobe Analytics | De Customer Journey Analytics die API rapporteert, heeft dezelfde indeling, maar gebruikt een ander eindpunt. Geef het API-gebruik voor rapportage door van de Adobe Analytics-API voor rapportage naar de Customer Journey Analytics-API. |
| **Stap 6: Account voor het gebruik van gegevensfeeds en Data Warehouse**</br> Alleen van toepassing bij migreren uit Adobe Analytics | Bepaal hoe u de exportopties gebruikt die beschikbaar zijn in de Customer Journey Analytics om de gegevensfeeds en -Data Warehouse die u in Adobe Analytics gebruikte het beste te repliceren. <!-- link to docs Rob is creating --> |
| **Stap 7: Projecten en onderdelen migreren**</br> Alleen van toepassing bij migreren uit Adobe Analytics | In het gebied voor componentmigratie in Adobe Analytics kunt u projecten en de bijbehorende onderdelen migreren van Adobe Analytics naar Customer Journey Analytics.<p>Voor informatie over het herhalen van uw projecten van Adobe Analytics in Customer Journey Analytics, evenals het in kaart brengen van projectcomponenten van een het rapportreeks van Adobe Analytics aan een de gegevensmening van de Customer Journey Analytics, zie [Componenten en projecten migreren van Adobe Analytics naar Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/component-migration.html).</p> |
| **Stap 8: De gebruiker van het plan aan boord gaat** | Net als in Adobe Analytics is Analysis Workspace het belangrijkste gebruikersgerichte hulpmiddel in de Customer Journey Analytics. Er zijn echter enkele belangrijke verschillen bij het gebruik van Analysis Workspace in de Customer Journey Analytics die gebruikers moeten onthouden.<p>Geef uw gebruikers voldoende tijd (3 - 6 maanden) om vertrouwd te raken met de belangrijkste verschillen in Customer Journey Analytics van Analysis Workspace.</p><p>Voor informatie over enkele belangrijke verschillen tussen Adobe Analytics en Customer Journey Analytics raadpleegt u [Gebruikershandleiding voor Adobe Analytics-gebruikers](/help/getting-started/aa-to-cja-user.md).</p> |
| **Stap 9: Rapport over uw kanaalgegevens in Workspace** | Nadat u verbindingen en gegevensmeningen hebt gecreeerd, analyseer de gegevens u binnen gebruikend de macht en de flexibiliteit van Analysis Workspace hebt gebracht.<br>Zie [Basisanalyse uitvoeren](/help/analysis-workspace/perform-basic-analysis.md) en [Geavanceerde analyse uitvoeren](/help/analysis-workspace/perform-adv-analysis.md). |

## Hulplijnen voor snel starten

De [Gegevensinvoer](../data-ingestion/data-ingestion.md) bevat snelle handleidingen voor de bovenstaande workflow. Deze snelstarthulplijnen tonen hoe u gegevens uit verschillende bronnen (waaronder Adobe Analytics) in Adobe Experience Platform kunt invoeren en deze gegevens vervolgens in de Customer Journey Analytics kunt gebruiken.
