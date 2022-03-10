---
title: De CJA-verbindingsgrootte schatten
description: Rapport over uw huidige gebruik van Customer Journey Analytics
exl-id: 5599b34f-342d-4c68-b7c9-2ac3ea50d078
solution: Customer Journey Analytics
feature: Connections
source-git-commit: cd48a91ca3affc39cf71451bdd8a44ca7669523b
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# De verbindingsgrootte schatten

Mogelijk moet u weten hoeveel rijen gegevens u momenteel hebt in [!UICONTROL Customer Journey Analytics]. Ga als volgt te werk om een accuraat overzicht te krijgen van het gebruik van de records (gegevensrijen) met gebeurtenisgegevens van uw organisatie **voor elk van de verbindingen die door uw organisatie worden gecreeerd**.

1. In [!UICONTROL Customer Journey Analytics]klikt u op de knop **[!UICONTROL Connections]** tab.

   U kunt nu een lijst met al uw huidige verbindingen zien.

1. Klik op elke naam van de verbinding om deze weer te geven.

1. Voeg de **[!UICONTROL Records of event data available]** voor alle gemaakte verbindingen. (Afhankelijk van de grootte van de verbinding kan het even duren voordat het nummer wordt weergegeven.)

   ![gebeurtenisgegevens](assets/event-data.png)

1. Als u een som van alle rijen met gebeurtenisgegevens hebt, zoekt u de machtiging &quot;Rijen van gegevens&quot; op in het Customer Journey Analytics-contract dat uw bedrijf met Adobe heeft ondertekend.

   Dit geeft u het maximumaantal rijen van gegevens die in de Orde van de Verkoop worden geautoriseerd. Als het aantal rijen gegevens dat uit Stap 3 is voortgekomen groter is dan dit aantal, gaat u over.

1. U kunt deze situatie op verschillende manieren verhelpen:

   * Wijzig uw [instellingen voor gegevensbehoud](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/manage-connections.html?lang=en#set-rolling-window-for-connection-data-retention).
   * [Ongebruikte verbindingen verwijderen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html?lang=en#implications-of-deleting-data-components).
   * [Een gegevensset verwijderen in AEP](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html?lang=en#implications-of-deleting-data-components).
   * Neem contact op met de accountmanager van de Adobe om een licentie voor extra capaciteit te verkrijgen.

## Over gebruiksoverschrijdingen

De gebruikslimieten worden dagelijks door Adobe strikt gecontroleerd en gehandhaafd. &quot;Rijen van gegevens&quot;: de dagelijkse gemiddelde rijen van gegevens die beschikbaar zijn voor analyse binnen Customer Journey Analytics.

Stel dat uw contractrecht het aantal rijen tot 1 miljoen beperkt. Stel dat u op dag 1 van het gebruik van Customer Journey Analytics 2 miljoen rijen gegevens uploadt. Op dag 2 verwijdert u 1 miljoen rijen en behoudt u het gebruik het toegewezen maximum. Voor dag 1 worden overgebruikskosten aangerekend.

## Diagnose discrepanties

In sommige gevallen, kunt u opmerken dat het totale aantal gebeurtenissen die door uw verbinding worden opgenomen verschillend is dan het aantal rijen in de dataset in [!UICONTROL Adobe Experience Platform]. In dit voorbeeld heeft de dataset &quot;B2B Impression&quot; 7650 rijen, maar de dataset bevat 3830 rijen in [!UICONTROL Adobe Experience Platform]. Er zijn verschillende redenen waarom er verschillen kunnen optreden en de volgende stappen kunnen worden uitgevoerd om een diagnose te stellen:

1. Verdeel deze dimensie door **[!UICONTROL Platform Dataset ID]** en u zult twee datasets met de zelfde grootte maar verschillend opmerken **[!UICONTROL Platform Dataset IDs]**. Elke dataset heeft 3825 verslagen. Dat betekent [!UICONTROL Customer Journey Analytics] 5 records genegeerd wegens ontbrekende persoon-id&#39;s of ontbrekende tijdstempels:

   ![uitsplitsing](assets/data-size2.png)

1. Als we inchecken [!UICONTROL Adobe Experience Platform], is er geen dataset met ID &quot;5f21c12b732044194bffc1d0&quot;, vandaar dat iemand deze specifieke dataset van schrapte [!UICONTROL Adobe Experience Platform] wanneer de eerste verbinding werd gemaakt. Later werd het opnieuw toegevoegd aan Customer Journey Analytics, maar een ander [!UICONTROL Platform Dataset ID] is gegenereerd door [!UICONTROL Adobe Experience Platform].

Meer informatie over de [implicaties van gegevensset en het schrappen van verbindingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html?lang=en#implications-of-deleting-data-components) in [!UICONTROL Customer Journey Analytics] en [!UICONTROL Adobe Experience Platform].
