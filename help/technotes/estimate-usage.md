---
title: Je Customer Journey Analytics-gebruik beheren
description: Hierin wordt uitgelegd hoe u uw Customer Journey Analytics-gebruik beheert.
role: Admin
feature: Basics
exl-id: 7a5d1173-8d78-4360-a97a-1ab0a60af135
source-git-commit: 6d23203468032510446711ff5a874fd149531a9a
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Je Customer Journey Analytics-gebruik beheren

>[!TIP]
>
>Gebruik de [**[!UICONTROL Usage]**&#x200B;interface &#x200B;](/help/connections/manage-connections.md#usage) aan **&#x200B; mening &#x200B;** het gebruik van opgenomen en te melden rijen over alle verbindingen in Customer Journey Analytics.



U kunt uw Customer Journey Analytics-gebruik beheren in de [**[!UICONTROL Connections]**-interface &#x200B;](/help/connections/create-connection.md) . In deze interface kunt u de Customer Journey Analytics-gegevensbewaring definiëren als een schuifvenster in maanden (1 maand, 3 maanden, 6 maanden, enzovoort), op verbindingsniveau.

Het belangrijkste voordeel is dat u alleen gegevens opslaat of rapporteert die van toepassing zijn en nuttig zijn, en oudere gegevens verwijdert die niet meer nuttig zijn. Het helpt u onder uw contractgrenzen te blijven en vermindert het risico van overleeftijdskosten.

Als u de standaardinstelling (uitgeschakeld) verlaat, wordt de bewaarperiode vervangen door de bewaarinstelling voor Adobe Experience Platform-gegevens. Als je 25 maanden aan gegevens hebt in Experience Platform, krijgt Customer Journey Analytics 25 maanden aan gegevens via back-up. Als u 10 van die maanden in Platform schrapte, zou Customer Journey Analytics de resterende 15 maanden behouden.

Het bewaren van gegevens is gebaseerd op tijdstempels en is alleen van toepassing op gebeurtenisdatasets en summiere gegevensdatasets. Er bestaat geen instelling voor het schuivende gegevensvenster voor profiel- of opzoekgegevenssets, omdat er geen relevante tijdstempels zijn. Als uw verbinding om het even welk profiel of raadplegingsdatasets omvat, aangezien zij met gebeurtenisdatasets worden aangesloten, worden de gegevens bewaard in Customer Journey Analytics die op uw montages van het gegevensbehoud op de tijdstempels van de gebeurtenisdataset wordt gebaseerd.


>[!MORELIKETHIS]
>
>[&#x200B; Bekijk uw gebruik van Customer Journey Analytics &#x200B;](/help/connections/manage-connections.md#usage)

