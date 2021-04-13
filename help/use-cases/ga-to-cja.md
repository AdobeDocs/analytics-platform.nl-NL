---
title: Google Analytics in Adobe Experience Platform krijgen voor analyse in Customer Journey Analytics (CJA)
description: 'Verklaart hoe te hefboomwerking Customer Journey Analytics (CJA) om uw Google Analytics en firebase gegevens in Adobe Experience Platform in te voeren. '
exl-id: 314378c5-b1d7-4c74-a241-786198fa0218
translation-type: tm+mt
source-git-commit: 58842436ab3388ba10ad0df0b35c78f68b02f0a3
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---


# Gegevens van Google Analytics opnemen in Adobe Experience Platform

Dit gebruiksgeval concentreert zich op hoe te om uw gegevens van Google Analytics als dataset in Adobe Experience Platform in te nemen. We zullen uitleggen hoe we zowel historische als live gegevens kunnen opnemen. Zodra gedaan, kunt u beide datasets in Customer Journey Analytics combineren om een dwars-apparatenmening van de reis van uw gebruiker te bereiken.

Datasets in het Experience Platform bestaan uit twee dingen: een schema en de daadwerkelijke verslagen in de dataset. Het schema (wij roepen dit het Model van Gegevens van de Ervaring of XDM voor kort) is als de kolommen van de dataset en is als blauwdruk of de regels die de gegevens zelf beschrijven. Binnen het Platform, verstrekt Adobe 2 types van schema&#39;s:

* Buiten-de-doosschema&#39;s dat u uw gegevens van Google Analytics aan automatisch kunt in kaart brengen (genoemd het schema van de Gebeurtenis van de Ervaring)
* Aangepaste schema&#39;s die u kunt maken en waarmee u de Google Analytics-gegevens eenvoudig kunt toewijzen

Één van de krachtigste aspecten van het gegevensmodel van Adobe is dat het u toestaat om al uw gegevens van de klanteninteractie in één gemeenschappelijk schema te standaardiseren - dit maakt het veel gemakkelijker om de gegevens samen in CJA te binden.

## Vereisten

Voor het uitvoeren van deze taken hebt u de volgende toegang en machtigingen nodig:

* Toegang tot Adobe Experience Platform
* Toegang tot Universal Google Analytics (versie Google Analytics 360) of Google Analytics 4 (versie met gratis versie of versie Google Analytics 360)
* Toegang tot Customer Journey Analytics en zijn [Admin toestemmingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=en#admin-access-permissions).

Hoe u gegevens van Google Analytics in Adobe Experience Platform brengt hangt van welke versie van Google Analytics af u gebruikt:

| Als u... | U hebt deze licentie ook nodig... | En doe dit... |
| --- | --- | --- |
| **Universele Google Analytics** | Google Analytics 360 | Voer stap 1 - 5 van de onderstaande instructies uit |
| **Google Analytics 4** | Gratis GA-versie of Google Analytics 360 | Voer stap 1 en 3-5 van de onderstaande instructies uit. Geen behoefte aan stap 2. |

## Voorbeeld van historische gegevens

### 1. Verbind uw gegevens van Google Analytics met BigQuery

De volgende instructies zijn gebaseerd op Universal Google Analytics. Zij zijn van toepassing op historische gegevens. Ga voor instructies over live streaminggegevens naar Live streaming gegevens in AEP plaatsen.

Zie [deze instructies](https://support.google.com/analytics/answer/3416092?hl=en).

### 2. Google Analytics-sessies transformeren naar gebeurtenissen in BigQuery

>[!IMPORTANT]
>
>Deze stap is alleen van toepassing op klanten van Universal Analytics

GA-gegevens slaan elke record in de gegevens op als een gebruikerssessie in plaats van als afzonderlijke gebeurtenissen. U moet een SQL vraag tot stand brengen om de Universele gegevens van Analytics in een ervaring-Platform-volgzaam formaat om te zetten. U past de functie &quot;Unest&quot; toe op het veld &quot;hits&quot; in het GA-schema. Hier volgt het SQL-voorbeeld dat u kunt gebruiken:

`SQL sample`

Zodra de vraag voltooit, sparen de volledige resultaten in een lijst BigQuery.

Zie [deze instructies](https://support.google.com/analytics/answer/3437618?hl=en).

Of bekijk deze video:

>[!VIDEO](https://video.tv.adobe.com/v/332634)

### 3. Exporteer Google Analytics-gebeurtenissen in JSON-indeling naar Google Cloud Storage en sla deze op in een emmertje

Vervolgens importeert u de Google Analytics-gebeurtenissen in JSON-indeling naar Google Cloud Storage. Dan breng je het in het Experience Platform.

Zie [deze instructies](https://support.google.com/analytics/answer/3437719?hl=en&amp;ref_topic=3416089).

### 4. De gegevens van Google Cloud Storage in Experience Platform brengen

Selecteer **[!UICONTROL Sources]** in Experience Platform en zoek de optie **[!UICONTROL Google Cloud Storage]**. Van daar, moet u enkel de dataset vinden u van de Grote Vraag had bewaard.

Bekijk deze video voor instructies:

>[!VIDEO](https://video.tv.adobe.com/v/332641)

### 5. GCS-gebeurtenissen importeren naar Adobe Experience Platform en toewijzen aan XDM-schema

Daarna, kunt u de GA gebeurtenisgegevens in een bestaande dataset in kaart brengen die u eerder creeerde, of een nieuwe dataset creëren gebruikend welk XDM- schema u kiest. Zodra u het schema hebt geselecteerd, past het Experience Platform machine het leren toe om elk van de gebieden in de gegevens van Google Analytics aan uw eigen schema automatisch in kaart te brengen.

Toewijzingen zijn zeer gemakkelijk te veranderen en u kunt zelfs afgeleide of berekende gebieden van de gegevens van Google Analytics tot stand brengen. Nadat u de velden hebt toegewezen aan uw XDM-schema, kunt u deze import op terugkerende basis plannen en tijdens het innameproces foutvalidatie toepassen. Op die manier weet u zeker dat er geen problemen zijn met de gegevens die u hebt geïmporteerd.

## Live streaming Google Analytics-gegevens verwerken

U kunt ook livestreaminggebeurtenissen vastleggen van Google Tag Manager rechtstreeks naar Adobe Experience Platform.

### Aangepaste variabelen toevoegen

Nadat u zich hebt aangemeld bij de Google Tag Manager-account, moet u aangepaste constante variabelen toevoegen die betrekking hebben op Adobe org-id en gegevensset-id&#39;s. U hebt waarschijnlijk al variabelen in Google Tag Manager die naar Google Analytic worden verzonden, zoals het e-mailadres van de klant, de naam van de klant, de taal en de aanmeldingsstatus van de klant. U moet vijf nieuwe aangepaste variabelen definiëren:

* Adobe Experience Cloud org ID
* DCS Streaming-eindpunt
* ID gegevensset Experience Platform
* Schema
* Tijdstempel pagina.

Het krijgen van deze waarden zorgt ervoor dat alle gegevens van Google Analytics naar de correcte dataset worden verzonden en het juiste schema hebben. Als u de Experience Cloud Org of een van de andere variabelen die we zojuist hebben genoemd niet kent, kan uw accountmanager van Adobe u helpen deze op te sporen.

Nadat u deze aangepaste variabelen hebt gedefinieerd, kunnen we een trigger instellen om alle gegevens die u al verzendt, ook naar de Google Analytics van het Experience Platform te verzenden.

### Een trigger instellen in Google Tag Manager

In dit voorbeeld is de trigger Account Creation gedefinieerd, waarbij `pageUrl equals account-creation` is gedefinieerd. Door enige informatie aan deze trigger toe te voegen, kunt u ervoor zorgen dat gegevens naar zowel Google Analytics als AEP worden verzonden wanneer de gebruiker met succes verifieert en de pagina voor het maken van een account wordt geladen.

Bekijk deze video voor instructies:

>[!VIDEO](https://video.tv.adobe.com/v/332668)

### Volgende stappen

Als de Adobe Experience Platform de live Google Analytics-gegevens heeft ontvangen en u een back-up hebt gemaakt van de historische Google Analytics-gegevens van BigQuery, kunt u naar CJA springen en

1. [Maak uw eerste ](/help/connections/create-connection.md) verbinding, waarmee de GA-gegevens worden gekoppeld aan al uw andere klantgegevens met een gemeenschappelijke &quot;klant-id&quot;.
1. Voer een verbluffende analyse uit in Workspace, bijvoorbeeld..

*Is dit waar dit onderwerp zou moeten stoppen of moeten we in detail ingaan over de verbinding?*