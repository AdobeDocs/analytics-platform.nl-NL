---
title: Kenmerken van Customer Journey Analytics
description: Meer informatie over unieke functies van Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 4e6cacb9-4eca-4dfb-bce4-e69850507596
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Kenmerken van Customer Journey Analytics {#feature-support-upgrade}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-tie-data"
>title="Gegevens van verschillende bronnen samenvoegen"
>abstract="(Aanbevolen) Gegevens van verschillende web-, mobiele en offline eigenschappen tellen om één geconsolideerde weergave van het gedrag van de klant te maken. Dit vermogen om analysegegevens uit andere kanalen te combineren is het belangrijkste gebruiksgeval voor Customer Journey Analytics."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-stitch-datasets"
>title="Stikbereiken van meerdere gegevenssets"
>abstract="Als om het even welk van uw datasets geen primaire herkenningsteken (zoals Experience Cloud identiteitskaart) deelt, kunt u die gegevens nog verbinden gebruikend een andere dimensie, zoals login gebruikersbenaming of e-mailadres."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-stitch-customer-care"
>title="Neem contact op met de klantenservice van Adobe voor het genereren van een gegevensset"
>abstract="Als u een gebied hebt dat een herkenningsteken bevat dat in veelvoudige datasets bestaat maar niet het primaire herkenningsteken is, kunt u dat gebruiken om een nieuwe dataset met een verenigbare herkenningsteken te produceren."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-integrate-rtcdp"
>title="Integreren met CDP in real time"
>abstract="Combineer profielgegevens van veelvoudige bronnen om publiek en segmenten te produceren die op gebruikerseigenschappen worden gebaseerd."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-integrate-target"
>title="Tijdelijk integreren met Adobe Target"
>abstract="Adobe raadt aan om Adobe Journey Optimizer te integreren met het oog op het gebruik van personalisatie. Integratie met Adobe Target is mogelijk, maar een kortetermijnoplossing."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-integrate-ajo"
>title="Integreren met Journey Optimizer"
>abstract="Lever verbonden, contextafhankelijke en persoonlijke ervaringen aan klanten."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-integrate-aam"
>title="Tijdelijk integreren met Adobe Audience Manager"
>abstract="Adobe raadt aan om voor publiek-gebaseerde gebruiksgevallen te integreren met Adobe Real-time CDP. Integratie met Audience Manager is mogelijk, maar een kortetermijnoplossing."

<!-- markdownlint-enable MD034 -->

{{upgrade-note}}

In de volgende lijst staan alleen die Customer Journey Analytics-functies die tijdens het upgradeproces in overweging moeten worden genomen. Voor een uitvoerige lijst die toont welke eigenschappen van Adobe Analytics volledig, gedeeltelijk gesteund, of niet gesteund in Customer Journey Analytics worden gesteund, zie [ de eigenschapsteun van Customer Journey Analytics ](/help/getting-started/aa-vs-cja/cja-aa.md).

Houd rekening met de volgende Customer Journey Analytics-functies die u wilt gebruiken bij het upgraden naar Customer Journey Analytics:

| Customer Journey Analytics-functie | Functie |
|---------|----------|
| [ het Webgegevens van de tijd met gegevens van andere kanalen, zoals de gegevens van het vraagcentrum ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-usecases/cross-channel/cross-channel) | Customer Journey Analytics wordt gecombineerd met de mogelijkheid van Experience Platform om allerlei gegevensschema&#39;s en -typen te bevatten. Gebruikend [ Model van de Gegevens van de Ervaring (XDM) ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl), kunnen de gegevens uniform worden vertegenwoordigd en georganiseerd, klaar voor combinatie en exploratie. Adobe Analytics is hoofdzakelijk geconcentreerd op Web en mobiele analysegegevens met sommige mogelijkheden om gegevens [ in te voeren ](https://experienceleague.adobe.com/docs/analytics/import/home.html). |
| [ Stitch de klappen van andere datasets die een douaneafmeting gebruiken ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/stitching/overview) | Customer Journey Analytics staat u toe om gegevens [ van veelvoudige rapportreeksen te combineren ](/help/connections/combined-dataset.md) alsof zij één enkele rapportreeks in Adobe Analytics waren. |
| [ integreer met Adobe in real time CDP ](/help/components/audiences/audiences-overview.md) | U kunt [ publiek ](/help/components/audiences/audiences-overview.md) creëren en publiceren dat in Customer Journey Analytics aan het Profiel van de Klant in real time in Adobe Experience Platform voor klant wordt ontdekt die en verpersoonlijking richt. |
| [ integreer met Adobe Target (A4T) ](/help/integrations/at.md) | Het doel dat in Customer Journey Analytics meldt laat u toe om [ te meten en over de activiteiten van Adobe Target ](/help/integrations/at.md) direct in Customer Journey Analytics te rapporteren. Adobe raadt echter aan om de integratie met Adobe Journey Optimizer te bevorderen voor het gebruik van personalisatie. |
| [ integreren met Adobe Journey Optimizer ](/help/integrations/ajo.md) | U kunt gegevens vormen die door Journey Optimizer worden geproduceerd om [ geavanceerde analyse in Customer Journey Analytics ](/help/integrations/ajo.md) uit te voeren. |
| [ integreren met Adobe Audience Manager ](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/implementation-integration-guides/integration-experience-platform/aam-aep-audience-sharing) | U kunt [ de eigenschappen en de segmenten van Audience Manager aan Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/implementation-integration-guides/integration-experience-platform/aam-aep-audience-sharing) delen. Adobe raadt echter aan om voor publieksgebaseerde gebruikscase te integreren met Adobe Real-time CDP. |
