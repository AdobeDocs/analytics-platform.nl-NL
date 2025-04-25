---
title: Wat zijn beperkte labels in Report Builder
description: Beschrijft beperkte labels in Report Builder
role: User
feature: Report Builder
type: Documentation
solution: Customer Journey Analytics
exl-id: 99c3c66e-928e-4363-a6a9-bbcab792337a
source-git-commit: 6dd8a70293161ff58361953a7e48a98834b7abe0
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Beperkte labels in Report Builder

Over het algemeen worden aan gegevensbeheer gerelateerde instellingen in Customer Journey Analytics overgenomen van Experience Platform. Dankzij de integratie tussen Customer Journey Analytics en Experience Platform Data Governance kunnen gevoelige gegevens van Customer Journey Analytics worden geëtiketteerd en kan het privacybeleid worden gehandhaafd.

De etiketten en het beleid van de privacy die op datasets worden gecreeerd door Experience Platform worden verbruikt kunnen in het werkschema van de gegevensmeningen van Customer Journey Analytics worden aangeschept. Deze labels stoppen of waarschuwen gebruikers die metriek en afmetingen van gevoelige velden maken. Voor informatie over datasets, zie [ Overzicht van Datasets ](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview)

Wanneer gegevens uit Customer Journey Analytics worden geëxporteerd (via rapportage, export, API, enz.), worden bovendien waarschuwingen of labels toegevoegd om gebruikers te laten weten dat een rapport gevoelige informatie bevat die op een specifieke manier moet worden behandeld.

Dankzij deze integratie kunt u de compatibiliteit beheren. Gegevensstewards in uw organisatie kunnen beleid plaatsen om gebruik te beperken. Dit betekent dat uw Customer Journey Analytics-gebruikers gegevens betrouwbaarder kunnen gebruiken, in de wetenschap dat deze in overeenstemming zijn met het beleid dat wordt gedefinieerd door data stewards.

Voor meer informatie, zie [ Customer Journey Analytics en de Governance van Gegevens ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-privacy/privacy-overview)

## Beperkte gegevens weergeven

In Customer Journey Analytics worden twee door Adobe gedefinieerde beleidsregels weergegeven die van invloed zijn op rapportage, downloaden en delen:

* Beleid voor analyse afdwingen
* Downloadbeleid afdwingen

De componenten onderworpen aan dit beleid zijn grijs uit en hebben een ![ InfoOutline ](/help/assets/icons/InfoOutline.svg) pictogram. Wanneer u de muisaanwijzer boven het pictogram Info houdt, wordt een notitie weergegeven die het volgende aangeeft: **[!UICONTROL Policies have been applied to this field prohibiting use of this data]** .

Voor meer informatie, zie [ Etiketten en beleid ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-governance).

<!--

![The policy note indicating prohibited use of data.](assets/rb-restricted-label.png){zoomable="yes"}
-->

## Rapporten bijwerken die beperkte gegevens bevatten

Wanneer een gebruiker een Report Builder-rapport heeft gemaakt met gegevenselementen die later worden beperkt, wordt een foutbericht weergegeven wanneer het rapport wordt vernieuwd.

![ het foutenbericht wordt getoond nadat de gegevenselementen later worden beperkt.](assets/error-restricted-data.png){width="100%" zoomable="yes"}
