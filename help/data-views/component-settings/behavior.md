---
title: Instellingen van gedragcomponent
description: Specificeer hoe een afmeting of metrisch gedrag in het melden.
exl-id: 170f445f-1eac-4b70-8956-1afb0cb2d611
solution: Customer Journey Analytics
feature: Data Views
role: Admin
source-git-commit: 50599b36d333cae3735c6d4fd1b0af6fcabe9177
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# Instellingen van gedragcomponent {#behavior-component-settings}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="dataview_component_dimension_behavior"
>title="Gedrag"
>abstract="Van toepassing op afmetingen en metrische onderdelen. Bepaal hoe de lijnpunten voor dit metrisch worden bijeengevoegd. Geef op of de tekenreekswaarden voor deze dimensie lager moeten worden ingesteld."

<!-- markdownlint-enable MD034 -->


Gedraginstellingen zijn zowel voor afmetingen als voor metriek beschikbaar. De beschikbaarheid van instellingen is afhankelijk van het gegevenstype van de component en het schema.

![ montages van het Gedrag ](../assets/behavior-settings.png)

## Dimension-gedragsinstellingen

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Lower case] | De-dupliceert rijen die de zelfde waarde maar verschillend geval hebben. Indien ingeschakeld, worden alle gevallen van een dimensie met dezelfde waarde gerapporteerd als kleine letters. Uw gegevens bevatten bijvoorbeeld de waarden `"liverpool"` , `"Liverpool"` en `"LIVERPOOL"` in een tekenreeksdimensie. Als [!UICONTROL Lower case] is ingeschakeld, worden alle drie waarden gecombineerd in `"liverpool"` . Als deze optie is uitgeschakeld, worden alle drie de waarden als afzonderlijk van elkaar behandeld. |

{style="table-layout:auto"}

>[!NOTE]
>
>Als u [!UICONTROL Lower case] op een dimensie van een raadplegingsdataset toelaat, kunnen de veelvoudige raadplegingswaarden voor het zelfde herkenningsteken bestaan. Als dit conflict optreedt, gebruikt Customer Journey Analytics de eerste ASCII-gesorteerde waarde (hoofdletters staan voor waarden in kleine letters). Adobe raadt u af opzoekgegevenssets te gebruiken die dezelfde waarde bevatten wanneer [!UICONTROL Lower case] is ingeschakeld.

![ case-sensitive afmeting ](../assets/case-sens-workspace.png)

## Instellingen voor metrisch gedrag

| Instelling | Omschrijving/gebruik |
| --- | --- |
| [!UICONTROL Count values] | Zichtbaar op de gegevenstypen Geheel getal en Dubbel schema. Verhoog metrisch met de gespecificeerde hoeveelheid. Hiermee wordt bijvoorbeeld de waarde van de kolom met 50 verhoogd.`50` |
| [!UICONTROL Count instances] | Zichtbaar op de gegevenstypen Geheel getal en Dubbel schema. Verhoog de metrische waarde met één, ongeacht de waarde. De aanwezigheid van om het even welke waarde verhoogt metrisch. Hiermee wordt bijvoorbeeld een metrische waarde met 1 verhoogd als de waarde van de kolom `50` is. |
| [!UICONTROL Values to count] | Zichtbaar op de gegevenstypen van een Booleaans schema. Hiermee kunt u bepalen of de metrische waarde toeneemt door `true` , `false` of beide te tellen. |

{style="table-layout:auto"}

U kunt in Analysis Workspace zowel een metrische waarde &#39;Bestellingen&#39; als &#39;Opbrengst&#39; genereren met dezelfde kolom met gebeurtenisgegevenssets met verschillende gedragingen. Sleep de kolom met de dataset &#39;Revenue&#39; tweemaal naar de gegevensweergave en stel de ene kolom in op &#39;Telwaarden&#39; en de andere op &#39;Telinstanties&#39;. De metrische tellingen van &quot;Orders&quot;instanties, terwijl metrische tellingen van &quot;Inkomsten&quot;waarden.
