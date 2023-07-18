---
title: Een gegevensblok maken met Report Builder in Customer Journey Analytics
description: Beschrijft hoe te om een gegevensblok tot stand te brengen.
role: Data Engineer, Data Architect, Admin, User
feature: Report Builder
type: Documentation
exl-id: 46382621-d5e1-41d6-865c-782ec28a21fa
solution: Customer Journey Analytics
source-git-commit: f09dffe3d134c423b69f6ca75337f3aca3f51410
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# Een gegevensblok maken

A *gegevensblok* Dit is de tabel met gegevens die worden gemaakt door één gegevensaanvraag. Een werkboek van Report Builder kan veelvoudige gegevensblokken bevatten. Wanneer u een gegevensblok creeert, vorm eerst het gegevensblok en bouwt dan het gegevensblok.

## Het gegevensblok configureren

Vorm de aanvankelijke parameters van het gegevensblok voor de het blokplaats van Gegevens, de meningen van Gegevens, en een waaier van de Datum.

1. Klikken **Gegevensblok maken**.

   ![](./assets/create_db.png)

1. Stel de **Locatie gegevensblok**.

   De optie voor gegevensbloklocatie definieert de werkbladlocatie waar de rapportbuilder de gegevens aan uw werkblad toevoegt.

   Als u de locatie van het gegevensblok wilt opgeven, selecteert u één cel in het werkblad of voert u een celadres in, zoals a3, \\\$a3, a\\$3 of sheet1!a2. De opgegeven cel wordt de linkerbovenhoek van het gegevensblok wanneer de gegevens worden opgehaald.

1. Kies de optie **Gegevensweergaven**.

   Met de optie Gegevens kunt u een gegevensweergave kiezen in een vervolgkeuzelijst of naar een gegevensweergave verwijzen vanuit een cellocatie.

1. Stel de **Datumbereik**.

   Met de optie Datumbereik kunt u een datumbereik kiezen. Datumbereiken kunnen vast zijn of doorlopen. Voor informatie over opties voor gegevensbereiken raadpleegt u [Een datumbereik selecteren](select-date-range.md).

1. Klikken **Volgende**.

   ![](./assets/choose_date_data_view3.png)

   Nadat u het gegevensblok vormt, kunt u afmetingen, metriek, en filters selecteren om uw gegevensblok te bouwen. De tabbladen Dimension, Metriek en Filters worden boven het deelvenster Tabelbouwer weergegeven.
<!--
    ![](./assets/image9.png)
  -->


## Het gegevensblok samenstellen

Om het gegevensblok te bouwen, selecteer rapportcomponenten, en pas dan de lay-out aan.

1. Voeg Dimension, Metriek, en Filters toe.

   Schuif de componentlijsten of gebruik de component **zoeken** veld voor het zoeken van componenten. Sleep componenten naar het deelvenster Tabel of dubbelklik op een componentnaam in de lijst om de component automatisch toe te voegen aan het deelvenster Tabel.

   Dubbelklik op een component om deze toe te voegen aan een standaardsectie van de tabel.

   - Dimension-componenten worden toegevoegd aan de sectie Rij of aan de sectie Kolom als u al een dimensie hebt in de kolommen.
   - De componenten van de datum worden toegevoegd aan de sectie van de Kolom.
   - Filtercomponenten worden toegevoegd aan de sectie Filters.

1. Rangschik de punten in de ruit van de Lijst om de lay-out van uw gegevensblok aan te passen.

   Sleep componenten in het deelvenster Tabel om de volgorde van componenten te wijzigen of klik met de rechtermuisknop op de naam van een component en selecteer een component in het optiemenu.

   Wanneer u componenten aan de lijst toevoegt, wordt een voorproef van het gegevensblok getoond bij de het blokplaats van Gegevens in het aantekenvel. De lay-out van de voorvertoning van gegevensblokken wordt automatisch bijgewerkt wanneer u items in de tabel toevoegt, verplaatst of verwijdert.

   ![](./assets/image10.png)

   **Rij- en kolomkoppen weergeven of verbergen**

1. Klik op de opdracht Gegevensblok bewerken in de Report Builder-hub.

1. Klik op de knop **Tabel** instellingenpictogram.

   ![voorlopige afbeelding](./assets/table-settings.png){width="35%"}

1. Schakel de optie Rij- en kolomkoppen weergeven in of uit. De kopteksten worden standaard weergegeven.

   **Dimensie-labels en metrische koppen verbergen of weergeven**

1. Klik op het ellipspictogram op de afmetingen of de kolomkoppen om de instellingen weer te geven.

   ![voorlopige afbeelding](./assets/row-heading.png){width="35%"}

1. Klik op Verbergen of Tonen om de dimensielabels of kolomkoppen in en uit te schakelen. Alle labels worden standaard weergegeven.

1. Klikken **Voltooien**.

   Er wordt een verwerkingsbericht weergegeven terwijl de analysegegevens worden opgehaald.

   ![](./assets/image11.png)

   Report Builder wint de gegevens terug en toont het voltooide gegevensblok in het aantekenvel.

   ![](./assets/image12.png)
