---
title: Caveats
description: Voorzieningen voor de BI-extensie in verschillende BI-gereedschappen in Customer Journey Analytics
solution: Customer Journey Analytics
feature: Data Views
role: User
source-git-commit: cb0102923f10f39becd40cc4187d2e11fb8c4e2f
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Caveats


Elk van de ondersteunde BI-gereedschappen heeft een aantal bedenkingen bij het werken met de Customer Journey Analytics BI-extensie.

+++ BI-gereedschappen

>[!BEGINTABS]

>[!TAB  Desktop van Power BI ]

* Filteren van datumbereiken via Power BI Desktop Advanced is exclusief.  Voor uw einddatum, moet u één meer dan de dag selecteren u wilt melden. Bijvoorbeeld **[!UICONTROL is on or after]** `1/1/2023` **[!UICONTROL and before]** `1/2/2023` .
* Power BI Desktop wordt standaard ingesteld op **[!UICONTROL Import]** wanneer u een verbinding maakt. Gebruik **[!UICONTROL Direct Query]** niet.
* Power BI Desktop stelt gegevenstransformaties beschikbaar via Power Query.  De Vraag van de macht werkt hoofdzakelijk met het type van de Invoer verbindingen zodat een vele transformaties die u als datum of koordfuncties toepast een fout werpen die u op een het typeverbinding van de Invoer moet schakelen.  Als u gegevens bij vraagtijd moet omzetten, zou u afgeleide dimensies en metriek moeten gebruiken zodat te hoeven Power BI niet om de transformaties zelf te doen.
* De Desktop van Power BI begrijpt niet hoe te om datum-tijd typekolommen te behandelen zodat worden de **[!UICONTROL daterange*X *]**&#x200B;dimensies zoals **[!UICONTROL daterangehour]**&#x200B;en **[!UICONTROL daterangeminute]**&#x200B;niet gesteund.
* Power BI Desktop probeert standaard meerdere verbindingen te maken met behulp van meer Query Service-sessies.  Ga binnen aan de montages van Power BI voor uw project en maak parallelle vragen onbruikbaar.
* Power BI Desktop sorteert en beperkt alles op de client. De Desktop van Power BI heeft ook verschillende semantiek voor top *X* het filtreren die gebonden waarden omvat. U kunt dus niet dezelfde sortering en beperking maken als in Analysis Workspace.
* Eerdere versies van de Power BI Desktop-release van oktober 2024 breken PostSQL-gegevensbronnen uit. Gebruik de versie die in dit artikel wordt vermeld.

>[!TAB  Desktop Tableau ]

* Het filtreren van de Waaier van de Waaier van de Desktop van Tableau van Daten is exclusief. Voor uw einddatum, moet u één meer dan de dag selecteren u wilt melden.
* Wanneer u standaard een datum- of datum-tijddimensie zoals **[!UICONTROL Daterangemonth]** toevoegt aan de rijen van een blad, plaatst Tableau Desktop het veld in een **[!UICONTROL YEAR()]** -functie.  Om te krijgen wat u wilt, moet u die dimensie selecteren en van het drop-down menu selecteren de datumfunctie u wilt gebruiken.  Wijzig bijvoorbeeld **[!UICONTROL Year]** in **[!UICONTROL Month]** wanneer u **[!UICONTROL Daterangemonth]** wilt gebruiken.
* Het beperken van resultaten tot Top *X* is niet duidelijk in de Desktop van Tableau. U kunt de resultaten expliciet beperken of een berekend veld en de functie **[!UICONTROL INDEX()]** gebruiken.  Het toevoegen van een Hoogste *X* filter aan een afmeting produceert complexe SQL gebruikend binnen-sluit zich aan dat niet wordt gesteund.

>[!TAB  Leider ]

* De laagker heeft een maximumaantal verbindingen per knoop die tussen 5-100 wordt vereist plaatsen.  U kunt deze waarde niet instellen op 1.  Deze instelling houdt in dat een lagere verbinding altijd minimaal 5 van de beschikbare Query Service-sessies gebruikt.
* Met Liniaal kunt u een project maken met een weergave op basis van een Customer Journey Analytics-gegevensweergave. De plukker leidt dan tot een model dat op de afmetingen en metriek wordt gebaseerd, beschikbaar in de mening van Gegevens, gebruikend LookerML.  Deze projectweergave wordt niet automatisch bijgewerkt naar de bron.  Als u wijzigingen aanbrengt of toevoegt aan de afmetingen, metriek, berekende metriek of segmenten van de CJA-gegevensweergave, worden deze wijzigingen niet automatisch weergegeven in Kiezer.  U moet de projectweergave handmatig bijwerken of een nieuw project maken.
* De gebruikerservaring van de kiezer op datum- of datum-tijdvelden zoals **[!UICONTROL Daterange Date]** of **[!UICONTROL Daterangeday Date]** is verwarrend.
* Het datumbereik van Lager is exclusief in plaats van inclusief.  **[!UICONTROL until (before)]** is grijs, zodat u dat aspect kunt missen.  Voor uw einddag, moet u één meer dan de dag selecteren u wilt melden.
* In de viewer worden uw meetgegevens niet automatisch als meetgegevens beschouwd.  Wanneer u metrisch selecteert, door gebrek probeert de Teller metrisch als afmeting in de vraag te behandelen.  Om metriek als metrisch te behandelen, moet u een douanegebied tot stand brengen zoals hierboven geïllustreerd. Als sneltoets kunt u **[!UICONTROL ⋮]** selecteren, **[!UICONTROL Aggregate]** selecteren en vervolgens **[!UICONTROL Sum]** selecteren.

>[!TAB  Jupyter Notitieboekje ]

* Het belangrijkste voorbehoud voor Jupyter Notitieboekje is dat het hulpmiddel geen belemmering-en-dalingsgebruikersinterface zoals andere hulpmiddelen van BI heeft. U kunt goede beelden tot stand brengen, maar u moet code schrijven om dit te verwezenlijken.

>[!TAB  RStudio ]

* De illustratie werkt met een plat schema, dus de optie **[!UICONTROL FLATTEN]** is vereist.
* Het belangrijkste voorbehoud voor RStudio is dat het hulpmiddel geen belemmering-en-dalingsgebruikersinterface zoals andere hulpmiddelen van BI heeft. U kunt goede beelden tot stand brengen, maar u moet code schrijven om dit te verwezenlijken.

>[!ENDTABS]

+++
