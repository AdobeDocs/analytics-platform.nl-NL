---
title: Instellingen van gedragcomponent
description: Specificeer hoe een afmeting of metrisch gedrag in het melden.
exl-id: 170f445f-1eac-4b70-8956-1afb0cb2d611
solution: Customer Journey Analytics
feature: Data Views
source-git-commit: c36dddb31261a3a5e37be9c4566f5e7ec212f53c
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---

# Instellingen van gedragcomponent

Gedraginstellingen zijn zowel voor afmetingen als voor metriek beschikbaar. De beschikbare instellingen zijn afhankelijk van het gegevenstype van de component en het schema.

![Gedragsinstellingen](../assets/behavior-settings.png)

## Instellingen voor Dimension-gedrag

| Instelling | Beschrijving |
| --- | --- |
| [!UICONTROL Lower case] | De-dupliceert rijen die de zelfde waarde maar verschillend geval hebben. Indien ingeschakeld, worden alle gevallen van een dimensie met dezelfde waarde gerapporteerd als kleine letters. De gegevens bevatten bijvoorbeeld de waarden `"liverpool"`, `"Liverpool"`, en `"LIVERPOOL"` in een tekenreeksdimensie. Indien [!UICONTROL Lower case] is ingeschakeld, worden alle drie waarden gecombineerd in `"liverpool"`. Als deze optie is uitgeschakeld, worden alle drie de waarden als afzonderlijk van elkaar behandeld. |

![Hoofdlettergevoelige dimensie](../assets/case-sens-workspace.png)

>[!NOTE]
>
>Als u [!UICONTROL Lower case] op een dimensie van de raadplegingsdataset, kunnen de veelvoudige raadplegingswaarden voor het zelfde herkenningsteken bestaan. Als dit conflict gebeurt, gebruikt CJA de eerste ASCII gesorteerde waarde (waarden in hoofdletters staan voor waarden in kleine letters). Adobe adviseert tegen het gebruiken van raadplegingsdatasets die de zelfde waarde bevatten wanneer [!UICONTROL Lower case] is ingeschakeld.

## Instellingen voor metrisch gedrag

| Instelling | Beschrijving/Hoofdletters gebruiken |
| --- | --- |
| [!UICONTROL Count values] | Zichtbaar op de gegevenstypen Geheel getal en Dubbel schema. Verhoog metrisch met de gespecificeerde hoeveelheid. Vergroot bijvoorbeeld de waarde van de kolom met 50 als de waarde van de kolom gelijk is `50`. |
| [!UICONTROL Count instances] | Zichtbaar op de gegevenstypen Geheel getal en Dubbel schema. Verhoog de metrische waarde met één, ongeacht de waarde. De aanwezigheid van om het even welke waarde verhoogt metrisch. Hiermee wordt bijvoorbeeld de waarde van een kolom met 1 verhoogd `50`. |
| [!UICONTROL Values to count] | Zichtbaar op de gegevenstypen van een Booleaans schema. Hiermee kunt u bepalen of de metrische waarde wordt verhoogd door te tellen `true`, `false`, of beide. |

U kunt in Analysis Workspace zowel een metrische waarde &#39;Bestellingen&#39; als &#39;Opbrengst&#39; genereren met dezelfde kolom met gebeurtenisgegevenssets met verschillende gedragingen. Sleep de kolom met de dataset &#39;Revenue&#39; tweemaal naar de gegevensweergave en stel de ene kolom in op &#39;Telwaarden&#39; en de andere op &#39;Telinstanties&#39;. De metrische tellingen van &quot;Orders&quot;instanties, terwijl metrische tellingen van &quot;Inkomsten&quot;waarden.
