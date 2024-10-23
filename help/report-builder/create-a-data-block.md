---
title: Hoe te om een gegevensblok tot stand te brengen gebruikend Report Builder in Customer Journey Analytics
description: Beschrijft hoe te om een gegevensblok tot stand te brengen.
role: User
feature: Report Builder
type: Documentation
exl-id: 46382621-d5e1-41d6-865c-782ec28a21fa
solution: Customer Journey Analytics
source-git-commit: c56c77079aa21fb740fda6bec333731a1f82a48f
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 0%

---

# Een gegevensblok maken

A *gegevensblok* is de lijst van gegevens die door één enkel gegevensverzoek worden gecreeerd. Een werkboek van de Report Builder kan veelvoudige gegevensblokken bevatten. Wanneer u een gegevensblok creeert, vorm eerst het gegevensblok en bouwt dan het gegevensblok.

## Het gegevensblok configureren

Vorm de aanvankelijke parameters van het gegevensblok voor de het blokplaats van Gegevens, de meningen van Gegevens, en een waaier van de Datum.

1. Klik **creëren gegevensblok**.

   ![ Schermafbeelding die de Create optie van het gegevensblok toont.](./assets/create_db.png)

1. Plaats de **plaats van het blok van Gegevens**.

   De optie voor gegevensbloklocatie definieert de werkbladlocatie waar de rapportbuilder de gegevens aan uw werkblad toevoegt.

   Als u de locatie van het gegevensblok wilt opgeven, selecteert u één cel in het werkblad of voert u een celadres in, zoals a3, \\\$a3, a\\$3 of sheet1!a2. De opgegeven cel wordt de linkerbovenhoek van het gegevensblok wanneer de gegevens worden opgehaald.

1. Kies de **meningen van Gegevens**.

   Met de optie Gegevens kunt u een gegevensweergave kiezen in een vervolgkeuzelijst of naar een gegevensweergave verwijzen vanuit een cellocatie.

1. Plaats de **waaier van de Datum**.

   Met de optie Datumbereik kunt u een datumbereik kiezen. Datumbereiken kunnen vast zijn of doorlopen. Voor informatie over de opties van de datumwaaier, zie [ Selecteer een Waaier van de Datum ](select-date-range.md).

1. Klik **daarna**.

   ![ Schermafbeelding die de optie van de datumwaaier en de actieve Volgende knoop tonen.](./assets/choose_date_data_view3.png)

   Nadat u het gegevensblok vormt, kunt u afmetingen, metriek, en filters selecteren om uw gegevensblok te bouwen. De tabbladen Dimensionen, Metriek en Filters worden boven het deelvenster Tabelbouwer weergegeven.

## Het gegevensblok samenstellen

Om het gegevensblok te bouwen, selecteer rapportcomponenten, en pas dan de lay-out aan.

1. Voeg Dimensionen, Metriek, en Filters toe.

   Schuif de componentenlijsten of gebruik het **onderzoek** gebied om van componenten de plaats te bepalen. Sleep componenten naar het deelvenster Tabel of dubbelklik op een componentnaam in de lijst om de component automatisch toe te voegen aan het deelvenster Tabel.

   Dubbelklik op een component om deze toe te voegen aan een standaardsectie van de tabel.

   - De componenten van het Dimension worden toegevoegd aan de sectie van de Rij of aan de sectie van de Kolom als u een afmeting reeds in de kolommen hebt.
   - Datumcomponenten worden toegevoegd aan de sectie Kolom.
   - Filtercomponenten worden toegevoegd aan de sectie Filters.

   **begindatum als Dimension**

   Stel de begindatum in als een dimensie om de begindatum van uw gegevensblok duidelijk te identificeren. Dit is nuttig als u een regelmatig gepland rapport hebt dat een het rollen datumwaaier heeft of als u een onconventioneel datumwaaier hebt en u van de begindatum moet duidelijk zijn.

   ![ het Schermafbeelding die de datum van het Begin in de lijst van dimensies toont.](./assets/start-date-dimension.png){width="30%"}

1. Rangschik de punten in de ruit van de Lijst om de lay-out van uw gegevensblok aan te passen.

   Sleep componenten in het deelvenster Tabel om de volgorde van componenten te wijzigen of klik met de rechtermuisknop op de naam van een component en selecteer een component in het optiemenu.

   Wanneer u componenten aan de lijst toevoegt, wordt een voorproef van het gegevensblok getoond bij de het blokplaats van Gegevens in het aantekenvel. De lay-out van de voorvertoning van gegevensblokken wordt automatisch bijgewerkt wanneer u items in de tabel toevoegt, verplaatst of verwijdert.

   ![ Schermafbeelding die de toegevoegde componenten en het bijgewerkte werkblad tonen.](./assets/image10.png)

   **Vertoning of verbergt rij en kolomkopballen**

1. Klik het **de montagespictogram van de Lijst**.

   ![ Schermafbeelding die de de montagesoptie van de Lijst toont.](./assets/table-settings.png){width="35%"}

1. Schakel de optie Rij- en kolomkoppen weergeven in of uit. De kopteksten worden standaard weergegeven.

   **verberg of toon afmetingsetiketten en metrische kopballen**

1. Klik op het ellipspictogram op de afmetingen of de kolomkoppen om de instellingen weer te geven.

   ![ het weglatingspictogram in de sectie van de Rij.](./assets/row-heading.png){width="35%"}

1. Klik op Verbergen of Tonen om de dimensielabels of kolomkoppen in en uit te schakelen. Alle labels worden standaard weergegeven.

1. Klik **Afwerking**.

   Er wordt een verwerkingsbericht weergegeven terwijl de analysegegevens worden opgehaald.

   ![ Het verwerkingsbericht.](./assets/image11.png)

   De Report Builder wint de gegevens terug en toont het voltooide gegevensblok in het aantekenvel.

   ![ het voltooide gegevensblok.](./assets/image12.png)
