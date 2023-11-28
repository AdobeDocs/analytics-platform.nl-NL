---
description: Door visualisatie te synchroniseren kunt u bepalen welke datatabel of gegevensbron overeenkomt met een visualisatie.
keywords: Analysis Workspace;Visualisatie synchroniseren met gegevensbron
title: Databronnen beheren
feature: Visualizations
exl-id: f9e89bef-0e78-49c7-8b7b-1fefd709c0cd
source-git-commit: c343a729de4cb13473a7acc04e837b5e5f69809b
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 3%

---

# Databronnen beheren

Door visualisatie te synchroniseren kunt u bepalen welke datatabel of gegevensbron overeenkomt met een visualisatie.

**Tip:** U kunt zien welke visualisaties gerelateerd zijn aan de kleur van de stip naast de titel. Gelijktijdige kleuren betekenen dat visualisaties zijn gebaseerd op dezelfde gegevensbron.

Door een gegevensbron te beheren, kunt u de gegevensbron weergeven of de selectie vergrendelen. Deze instellingen bepalen hoe de visualisatie verandert (of niet verandert) wanneer er nieuwe gegevens binnenkomen.

1. [Een project maken](/help/analysis-workspace/home.md) met een datatabel en een [visualisatie](/help/analysis-workspace/visualizations/freeform-analysis-visualizations.md).
1. Selecteer in de gegevenstabel de cellen (gegevensbron) die u aan de visualisatie wilt koppelen.
1. Klik in de visualisatie op de stip naast de titel om de **[!UICONTROL Data Source]** in. Selecteren **[!UICONTROL Show Data Source]** of **[!UICONTROL Lock Selection]**.

   ![Het dialoogvenster Gegevensbron met de opties die in de volgende sectie worden beschreven.](assets/manage-data-source.png)

   Als u een visualisatie synchroniseert met een tabelcel, wordt een nieuwe (verborgen) tabel gemaakt en wordt de gesynchroniseerde visualisatie met die tabel gekleurd.

| Element | Beschrijving |
|--- |--- |
| [!UICONTROL Linked Visualizations] | Als er visualisaties zijn die met een vrije vorm of cohortlijst worden verbonden, opent de hoogste linkerpunt om van de aangesloten visualisaties een lijst te maken en een &quot;show&quot;checkbox optie te hebben om de lijst te tonen/te verbergen.  Als u de muisaanwijzer boven de gekoppelde visualisatie houdt, gaat u naar de gekoppelde visualisatie. |
| [!UICONTROL Show Data Source] | Hiermee kunt u (door het selectievakje in te schakelen) of de datatabel die overeenkomt met de visualisatie verbergen (door deze uit te schakelen). |
| [!UICONTROL Lock Selection] | Schakel deze instelling in om de visualisatie te vergrendelen op de gegevens die momenteel zijn geselecteerd in de corresponderende gegevenstabel. Als deze optie is ingeschakeld, kiest u tussen:  <ul><li>**Geselecteerde posities**: Kies deze optie als de visualisatie vergrendeld moet blijven op de posities die in de corresponderende gegevenstabel zijn geselecteerd. Deze posities zullen zichtbaar blijven, zelfs als de specifieke posten in deze posities veranderen. Kies deze optie bijvoorbeeld als u de vijf belangrijkste campagnemenamen in deze visualisatie altijd wilt weergeven, ongeacht de naam van welke campagne in de bovenste vijf voorkomt.</li> <li>**Geselecteerde items**: Kies deze optie als de visualisatie vergrendeld moet blijven op de specifieke items die momenteel zijn geselecteerd in de bijbehorende gegevenstabel. Deze items blijven zichtbaar, zelfs als ze een andere positie innemen onder de items in de tabel. Kies deze optie bijvoorbeeld als u in deze visualisatie altijd dezelfde vijf specifieke campagnemenamen wilt weergeven, ongeacht de plaats waar die campagnemenamen staan.</li></ul> |

Deze architectuur verschilt van de vorige omdat Analysis Workspace niet langer een dubbele, verborgen tabel maakt waarin de vergrendelde selectie voor u wordt opgeslagen. De gegevensbron verwijst nu naar de tabel waaruit u de visualisatie hebt gemaakt.

**Gebruiksscenario&#39;s:**

* U kunt een overzichtsvisualisatie tot stand brengen en het sluiten aan een cel in de lijst u het van creeerde. Wanneer u &quot;Gegevensbron tonen&quot;toelaat, toont het u precies waar deze informatie uit in de lijst komt. De brongegevens worden grijs weergegeven:

  ![Locatie van gegevensbron in een werkblad.](assets/data-source2.png)>
* U kunt veel visualisaties toevoegen en deze uit verschillende cellen in dezelfde tabel betrekken, zoals u hier ziet. De tabel is hetzelfde als in het bovenstaande voorbeeld, maar de broncel (en metrisch) zijn anders:

  ![Locatie van gegevensbron met toegevoegde visualisaties die afkomstig zijn van meerdere cellen](assets/data-source3.png)>
* U kunt zien of er visualisaties zijn die met een vrije vorm of een cohortlijst worden verbonden door de hoogste linkerpunt (de Montages van de Gegevensbron) te klikken. Als u de muis hierboven houdt, wordt de gekoppelde visualisatie weergegeven. En als u erop klikt, gaat u direct naar de gekoppelde visualisatie.

  ![Instellingen gegevensbron waarmee een gekoppelde visualisatie wordt gemarkeerd voor weergaven boven aan pagina.](assets/linked-visualizations.png)>
