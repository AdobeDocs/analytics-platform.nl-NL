---
title: Gegevensinstellingen voor productgebruik
description: Instellingen voor productgebruik inschakelen, uitschakelen of configureren.
source-git-commit: 7d22c512e8e96963b288567704d2245e64411b10
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Gegevensinstellingen voor productgebruik {#product-usage-data-settings}

{{release-limited-testing}}

De _montages van Gegevens_ pagina behandelt uw configuratie van het productgebruik. U kunt deze pagina gebruiken om productgebruik voor uw organisatie in of uit te schakelen. U kunt ook configureren onder welke Adobe Experience Platform-sandbox de gegevensset wordt gemaakt en desgewenst het venster voor gegevensbehoud negeren. Het is alleen zichtbaar voor productbeheerders.

**[!UICONTROL Customer Journey Analytics]** > **[!UICONTROL Tools]** > **[!UICONTROL Product Usage]** > **[!UICONTROL Data settings]**

>[!IMPORTANT]
>Wanneer u deze functie inschakelt, moet u de voorwaarden accepteren voordat u deze kunt gebruiken. Wanneer u deze voorwaarden accepteert, doet u dit namens uw hele organisatie.

De volgende instellingen zijn beschikbaar op deze pagina:

* **[!UICONTROL Enable product usage]**: hiermee schakelt u de beschikbaarheid van gegevensverzameling voor productgebruik in of uit. Als u productgebruik dan het in de toekomst toelaat onbruikbaar maakt, worden de dataset, de verbinding en de gegevensmening niet geschrapt. Het bijhouden van wijzigingen wordt globaal uitgeschakeld voor uw organisatie wanneer deze wordt uitgeschakeld.
* **[!UICONTROL Sandbox]** - Hiermee wordt bepaald onder welke Adobe Experience Platform-sandbox het schema en de gegevensset worden gemaakt. De sandbox die u kiest, heeft geen invloed op de gegevensverzameling voor productgebruik. Als u deze sandbox-instelling wijzigt, worden alle bestaande gegevens verwijderd. Er wordt een nieuwe gegevensset, verbinding en gegevensweergave gemaakt in de geselecteerde sandbox.
* **[!UICONTROL Override data retention window]**: Elke gegevensset heeft een standaardvenster voor gegevensbehoud. Als deze instelling is uitgeschakeld, volgt het productgebruik die standaardtijdsperiode. U kunt deze instelling inschakelen als u de hoeveelheid tijd wilt verkorten waarin de gegevens worden bewaard. Het verkorten van het venster van het gegevensbehoud en hulp verminderen kosten en staat u toe om aan om het even welke werknemer-specifieke privacyrichtlijnen te voldoen. U kunt geen gegevensbehoud voorbij het de standaardvenster van het gegevensbehoud van de dataset uitbreiden.

>[!CONTEXTUALHELP]
>id="cja_product_usage_sandbox"
>title="Adobe Experience Platform-sandbox"
>abstract="Bepaalt de zandbak van Adobe Experience Platform dat het schema en de dataset onder worden gecreeerd."

>[!CONTEXTUALHELP]
>id="cja_product_usage_data_retention"
>title="Venster voor gegevensbehoud overschrijven"
>abstract="De beschikbaarheid van productgebruiksgegevens versnellen om de kosten te verlagen of de privacyrichtlijnen na te leven."
