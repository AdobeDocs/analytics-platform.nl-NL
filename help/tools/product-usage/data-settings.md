---
title: Gegevensinstellingen voor productgebruik
description: Instellingen voor productgebruik inschakelen, uitschakelen of configureren.
hide: true
hidefromtoc: true
source-git-commit: 8f2a340f59d8cdf97a5309ec20dc36f49b8f1129
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# Gegevensinstellingen voor productgebruik {#product-usage-data-settings}

{{release-limited-testing}}

De _montages van Gegevens_ pagina behandelt uw configuratie van het productgebruik. U kunt deze pagina gebruiken om productgebruik voor uw organisatie in of uit te schakelen. U kunt ook configureren onder welke Adobe Experience Platform-sandbox de gegevensset wordt gemaakt en desgewenst het venster voor gegevensbehoud negeren. Het is alleen zichtbaar voor productbeheerders.

**Customer Journey Analytics** > **Hulpmiddelen** > **Gebruik van het Product** > **montages van Gegevens**

>[!IMPORTANT]
>
>Wanneer u deze functie inschakelt, moet u de voorwaarden accepteren voordat u deze kunt gebruiken. Wanneer u deze voorwaarden accepteert, doet u dit namens uw hele organisatie.

De volgende instellingen zijn beschikbaar op deze pagina:

* **laat productgebruik** toe: Knevels de beschikbaarheid van de gegevensinzameling van het productgebruik. Als u productgebruik toelaat, dan het in de toekomst onbruikbaar maakt, worden de dataset, de verbinding en de gegevensmening niet geschrapt. Het bijhouden van wijzigingen wordt globaal uitgeschakeld voor uw organisatie wanneer deze wordt uitgeschakeld.
* **Sandbox**: Bepaalt de zandbak van Adobe Experience Platform dat het schema en de dataset onder worden gecreeerd. De sandbox die u kiest, heeft geen invloed op de gegevensverzameling voor productgebruik. Als u deze sandbox-instelling wijzigt, worden een aparte gegevensset, verbinding en gegevensweergave gemaakt. Historische gegevens blijven in de vorige sandbox staan.
* **het venster van het het gegevensbehoud van de met voeten treden**: Elke dataset heeft een venster van het standaardgegevensbehoud. Als deze instelling is uitgeschakeld, volgt het productgebruik die standaardtijdsperiode. U kunt deze instelling inschakelen als u de hoeveelheid tijd wilt verkorten waarin de gegevens worden bewaard. U kunt geen gegevensbehoud voorbij het de standaardvenster van het gegevensbehoud van de dataset uitbreiden.

>[!CONTEXTUALHELP]
>id="cja_product_usage_sandbox"
>title="Adobe Experience Platform-sandbox"
>abstract="Bepaalt de zandbak van Adobe Experience Platform dat het schema en de dataset onder worden gecreeerd."

>[!CONTEXTUALHELP]
>id="cja_product_usage_data_retention"
>title="Venster voor gegevensbehoud overschrijven"
>abstract="De beschikbaarheid van productgebruiksgegevens versnellen om de kosten te helpen verlagen."
