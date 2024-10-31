---
title: Componentinstellingen voor gedrag
description: Specificeer hoe een afmeting of metrisch zich in het melden gedraagt.
exl-id: 170f445f-1eac-4b70-8956-1afb0cb2d611
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: a236b2126c4b998b4d97caab014556e3ee3a9e83
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# Componentinstellingen voor gedrag {#behavior-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja_dataview_component_dimension_behavior"
>title="Gedrag"
>abstract="Bepaal hoe regelitems in deze dimensie worden geaggregeerd.<br/><br/>**Parameters **<br/>**Lager geval**: Staat u toe om te specificeren of de koordwaarden op het gebied lager zouden moeten worden toegelaten."

<!-- markdownlint-enable MD034 -->


Gedragsinstellingen zijn beschikbaar voor zowel dimensies als metrics. De beschikbaarheid van instellingen is afhankelijk van het gegevenstype van de component en het schema.

![ montages van het Gedrag ](../assets/behavior-settings.png)

## Instellingen voor gedrag van Dimensionen

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Lower case] | Hiermee worden rijen met dezelfde waarde maar verschillende hoofdletters/kleine letters gededupliceerd. Indien ingeschakeld worden alle instanties van een dimensie met dezelfde waarde gerapporteerd als kleine letters. Uw gegevens bevatten bijvoorbeeld de waarden `"liverpool"` , `"Liverpool"` en `"LIVERPOOL"` in een tekenreeksdimensie. Als [!UICONTROL Lower case] is ingeschakeld, worden alle drie waarden gecombineerd in `"liverpool"` . Indien deze optie is uitgeschakeld, worden alle drie de waarden als afzonderlijk behandeld. |

{style="table-layout:auto"}

>[!NOTE]
>
>Als u [!UICONTROL Lower case] op een dimensie van een raadplegingsdataset toelaat, kunnen de veelvoudige raadplegingswaarden voor het zelfde herkenningsteken bestaan. Als dit conflict gebeurt, gebruikt de Customer Journey Analytics de eerste gesorteerde ASCII-waarde (de waarden in hoofdletters staan voor de waarden in kleine letters). Adobe raadt aan geen opzoekgegevenssets te gebruiken die dezelfde waarde bevatten wanneer [!UICONTROL Lower case] is ingeschakeld.

![ case-sensitive afmeting ](../assets/case-sens-workspace.png)

## Instellingen voor metrisch gedrag

| Instelling | Beschrijving/gebruik |
| --- | --- |
| [!UICONTROL Count values] | Zichtbaar op de gegevenstypen Geheel getal en Dubbel schema. Verhoog metrisch met de gespecificeerde hoeveelheid. Vergroot bijvoorbeeld de waarde van een metrische waarde met 50 als de waarde van de kolom `50` is. |
| [!UICONTROL Count instances] | Zichtbaar op de gegevenstypen Geheel getal en Dubbel schema. Verhoog metrisch met één, ongeacht de waarde. Als een waarde aanwezig is, wordt de metrische waarde vergroot. Hiermee wordt bijvoorbeeld een metrische waarde met 1 verhoogd als de waarde van de kolom `50` is. |
| [!UICONTROL Values to count] | Zichtbaar op de gegevenstypen van een Booleaans schema. Hiermee kunt u bepalen of de metrische waarde toeneemt door `true` , `false` of beide te tellen. |

{style="table-layout:auto"}

U kunt in Analysis Workspace zowel een metrische waarde &#39;Bestellingen&#39; als &#39;Opbrengst&#39; genereren met dezelfde kolom met gebeurtenisgegevenssets met verschillende gedragingen. Sleep de gegevenssetkolom &#39;Opbrengst&#39; tweemaal naar de gegevensweergave en stel een kolom in op &#39;Waarden tellen&#39; en een andere op &#39;Instanties tellen&#39;. De metrische tellingen van &quot;Orders&quot;, terwijl de metrische tellingswaarden van &quot;Omzet&quot;.
