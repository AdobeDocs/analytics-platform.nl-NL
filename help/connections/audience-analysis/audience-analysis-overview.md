---
title: Overzicht van de analyse van het publiek
description: Meer informatie over het analyseren van publiek van RTCDP in Customer Journey Analytics.
solution: Customer Journey Analytics
feature: Audiences
role: Admin
hide: true
hidefromtoc: true
source-git-commit: 3654d452f2bc4fec5f53854307536b3b8679eac3
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 2%

---

# Overzicht van de analyse van het publiek

<!-- add hidden text in this article when this feature releases: /help/components/audiences/audiences-overview.md -->

>[!NOTE]
>
>Analyse van het publiek wijkt af van publicatie van het publiek, zodat u publiek kunt maken en publiceren dat in Customer Journey Analytics aan Adobe Experience Platform wordt ontdekt voor klantgerichtheid en personalisatie. Voor informatie over publiek het publiceren, zie [ publiek het publiceren overzicht ](/help/components/audiences/audiences-overview.md).

De analyse van het publiek staat u toe om de gegevens van het publiekslidmaatschap van de Gegevensreeksen van het Profiel van Experience Platform in een verbinding van Customer Journey Analytics in te voeren. Soorten publiek wordt beschikbaar als nieuwe afmetingen voor gebruik in Analysis Workspace.

In het volgende diagram en de bijbehorende tabel ziet u een voorstelling op hoog niveau van de manier waarop een configuratie voor publieksanalyse in Customer Journey Analytics publieksgegevens uit Experience Platform beschikbaar maakt in Analysis Workspace:

![ overzicht van de de analyseanalyse van het publiek ](assets/audience-analysis-overview.png)

| Getal | Functie | Functie |
|---------|----------|---------|
| 1 | Configuratie van publieksanalyse | De interface van de configuratie in Customer Journey Analytics die voor het vormen van publieksanalyse wordt gebruikt. |
| 2 | Sandbox | Moet de profieldataset bevatten die u aan uw verbinding wilt toevoegen. |
| 3 | Profielgegevensset | Moet de Experience Platform-publieksgegevens bevatten die u wilt analyseren. Deze profieldataset wordt toegevoegd aan de verbinding die u selecteert. |
| 4 | Samenvoegbeleid | Het samenvoegbeleid dat is gekoppeld aan het Experience Platform-publiek dat u wilt analyseren. |
| 5 | Profielgegevens | De profielgegevens die zijn gekoppeld aan het samenvoegbeleid dat u selecteert. Deze gegevens zijn beschikbaar in Experience Platform-gegevenssets. |
| 6 | Nieuwe opzoekgegevensset | Verstrekt vriendschappelijke namen voor de nieuwe publieksafmetingen die worden gecreeerd. De opzoekdataset wordt automatisch gecreeerd en aan de verbinding toegevoegd, samen met de profieldataset u selecteert. |
| 7 | Verbinding | De verbinding waar u de profieldataset wilt toevoegen die u selecteert. |
| 8 | Nieuwe doelafmetingen | Nieuwe publieksafmetingen <!--and metrics?--> die het publiek van Experience Platform vertegenwoordigen die in de profieldataset inbegrepen zijn u selecteerde, en beschikbaar voor rapportering in Analysis Workspace zijn. Deze afmetingen worden automatisch gemaakt. |
| 9 | Gegevensweergaven | De gegevensweergaven die u selecteert en die aan uw verbinding zijn gekoppeld. Dit zijn de gegevensweergaven die u wilt gebruiken voor het analyseren van Experience Platform-publieksgegevens in Analysis Workspace. Deze gegevensweergaven worden automatisch geconfigureerd met Experience Platform-publieksgegevens voor rapportage. |
| 10 | Analysis Workspace | Het gebied binnen Customer Journey Analytics waar u rapporten maakt met daarin het Experience Platform-publiek dat wordt ingenomen. |

## publieksanalyse configureren

Wanneer u publieksanalyse vormt, selecteert u de zandbak en voegt beleid verbonden aan het publiek van Experience Platform dat u wilt analyseren samen. Customer Journey Analytics leidt tot een nieuwe raadplegingsdataset, dan voegt automatisch de raadplegingsdataset en de profieldataset aan de verbinding toe u kiest.

Voor meer informatie, zie [ publieksanalyse ](/help/connections/audience-analysis/audience-analysis-configure.md) vormen.

## Gebruikersgegevens in Customer Journey Analytics analyseren

Met de publieksgegevens beschikbaar in Customer Journey Analytics kunt u actioneerbare inzichten krijgen in het gedrag van publieksleden op verschillende kanalen.

U kunt bijvoorbeeld het gedrag bijhouden van individuele klanten die deel uitmaakten van dezelfde e-mailpromotie. Met het publiek beschikbaar in Customer Journey Analytics, kunt u de volgende soorten informatie over elk publiekslid zien:

* Doorklikken van de e-mail naar de site die uiteindelijk tot een aankoop heeft geleid

* Leden van het publiek die uiteindelijk een in-store aankoop maakten

Voor meer informatie, zie [ het publiek van Experience Platform in Customer Journey Analytics ](/help/connections/audience-analysis/analyze-audiences.md) analyseren.










