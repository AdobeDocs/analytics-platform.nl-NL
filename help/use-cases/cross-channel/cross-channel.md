---
title: Reisanalyse Kanaal
description: Analyseer en extraheer inzichten van klanteninteractie over de klantenreis.
exl-id: 285532b1-eb37-4984-9559-054a18515ddf
solution: Customer Journey Analytics
feature: Use Cases, Cross-Channel Analysis
role: User
source-git-commit: 5e80e68c6b5d3dca19dae21c6719b040b28afaf9
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---

# Kanaaloverschrijdende analyse {#cross-channel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-additional-datasets"
>title="Extra datasets toevoegen aan uw verbinding"
>abstract="Nadat u gegevens aan een dataset in Adobe Experience Platform toevoegt, kunt u die dataset aan uw verbinding in Customer Journey Analytics toevoegen. Zorg ervoor dat wanneer het toevoegen van gegevens van andere kanalen die zij aan het schema aanhangen dat uw organisatie gebruikt.<br><br> elke dataset die u toevoegt vereist een enorme hoeveelheid werk, in het bijzonder rond het verzekeren dat het unieke herkenningsteken voor elke gebeurtenis bestaat en ervoor zorgt dat de overkoepelende gegevensstructuur aan het douaneschema van uw organisatie voldoet. Het vestigen van deze werkschema kan coördinatie over vele teams binnen uw organisatie over verscheidene maanden verspreiden."

<!-- markdownlint-enable MD034 -->

De analyse tussen kanalen laat één enkele geconsolideerde mening van klantengedrag over diverse kanalen door gegevens van diverse Web, mobiele, en off-line eigenschappen te verenigen toe. U kunt deze geconsolideerde weergave bijvoorbeeld gebruiken om de interactie van klanten op verschillende desktops en mobiele apparaten te analyseren, zodat u het gedrag van klanten begrijpt en inzichten kunt ophalen om de beleving van digitale klanten te optimaliseren. U kunt klanteninteractie over kanalen, met inbegrip van digitale en off-line kanalen zoals steuninteractie en in-store aankopen ook analyseren om de klantenreis beter te begrijpen en te optimaliseren.

## Implementatiestappen

![&#x200B; stroom van implementatiestappen zoals die in deze sectie wordt beschreven.](../assets/cca-architecture.png)

1. [&#x200B; creeer schema&#39;s &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=nl-NL) voor gegevens die moeten worden opgenomen.
1. [&#x200B; creeer datasets &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/create-datasets-and-ingest-data.html?lang=nl-NL) voor gegevens die moeten worden opgenomen.
1. [&#x200B; Ingest gegevens in Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/understanding-data-ingestion.html?lang=nl-NL):
   1. Op gebeurtenis-gebaseerde gegevens ![&#x200B; gebeurtenis &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Events_18_N.svg) van website of mobiele app door de Edge Network of de bron van Analytics schakelaar.
   2. De gegevens van het profiel ![&#x200B; profiel &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_User_18_N.svg) (bijvoorbeeld van een systeem van CRM, de toepassing van het vraagcentrum, loyaliteitstoepassing).
   3. Opzoekgegevens ![&#x200B; raadpleging &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Search_18_N.svg) (bijvoorbeeld productnaam, categorie van een systeem van de productinformatie).

1. Gebruik een gemeenschappelijke namespaceidentiteitskaart over datasets. Het gebruik [&#x200B; Stitching &#x200B;](../../stitching/overview.md) om het even welke op gebeurtenis-gebaseerde dataset ![&#x200B; gegevens op te heffen verfrist zich &#x200B;](https://spectrum.adobe.com/static/icons/workflow_18/Smock_DataRefresh_18_N.svg) met betrekking tot het verstrekken van gemeenschappelijke identiteitskaart op elke rij. Customer Journey Analytics gebruikt momenteel de services Experience Platform Profile of Identity niet voor stitching.
1. Voer om het even welke voorbereiding van douanegegevens uit om een gemeenschappelijke sleutel over tijdreeksdatasets te verzekeren die in Customer Journey Analytics moeten worden opgenomen.
1. Opzoekgegevens een primaire id geven die kan worden gekoppeld aan een veld in de gebeurtenisgegevens. Telt als rijen in licentie.
1. Stel dezelfde primaire id voor profielgegevens in als de primaire id van de gebeurtenisgegevens.
1. [&#x200B; creeer een verbinding &#x200B;](../../connections/overview.md) om de relevante datasets van Experience Platform aan Customer Journey Analytics in te voeren.
1. [&#x200B; creeer een gegevensmening &#x200B;](/help/data-views/create-dataview.md) op de verbinding om de specifieke afmetingen en metriek te selecteren die in de mening moeten worden omvat. Attributie- en toewijzingsinstellingen worden ook geconfigureerd in de gegevensweergave. Deze instellingen worden tijdens het rapport berekend.
1. [&#x200B; creeer een project &#x200B;](/help/analysis-workspace/home.md) om dashboards en rapporten binnen Analysis Workspace te vormen.

## Overwegingen

Zorg ervoor dat u bij het instellen van deze workflow rekening houdt met de volgende punten.

* Voor het analyseren van gegevens tussen kanalen is dezelfde id-naamruimte vereist voor elke record.
* Het verenigingsproces van het verenigen van verschillende datasets vereist een gemeenschappelijke primaire persoon/entiteitsleutel over de datasets.
* Secundaire op sleutels gebaseerde unies worden momenteel niet ondersteund.
* Het stitching proces staat voor het opnieuw teweegbrengen van identiteiten in rijen toe die op voorbijgaande identiteitskaart (zoals een authentificatie ID) informatie van verslagen worden gebaseerd die zelfde blijvende identiteitskaart delen.Dit staat voor het oplossen van ongelijke verslagen aan één enkele gestikte identiteitskaart voor analyse op het persoonniveau, eerder dan op het apparaat of koekjesniveau toe.
* Objecten en kenmerken van hetzelfde XDM-veld worden in Customer Journey Analytics samengevoegd tot één dimensie. Om veelvoudige attributen van diverse datasets in de zelfde dimensie van Customer Journey Analytics samen te voegen, zouden de datasets het zelfde XDM gebied of schema moeten van verwijzingen voorzien.

