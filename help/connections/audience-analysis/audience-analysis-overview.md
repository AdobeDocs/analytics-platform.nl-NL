---
title: Overzicht van de analyse van het publiek
description: Meer informatie over het analyseren van publiek van RTCDP in Customer Journey Analytics.
solution: Customer Journey Analytics
feature: Audiences
role: Admin
hide: true
hidefromtoc: true
source-git-commit: ca2adce7be8a28fa72323915473a8c2283741889
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 1%

---

# Overzicht van de analyse van het publiek

<!-- add hidden text in this article when this feature releases: /help/components/audiences/audiences-overview.md and this article: /help/analysis-workspace/templates/use-templates.md-->

>[!NOTE]
>
>Begrijp het verschil tussen publieksanalyse en publiek het publiceren:
>
>* **analyse van het publiek**: Staat u toe om de gegevens van het publiekslidmaatschap van de datasets van het Profiel van Experience Platform in een verbinding van Customer Journey Analytics in te voeren.
>* **het Publiceren van het publiek**: Staat u toe om publiek tot stand te brengen en te publiceren dat in Customer Journey Analytics aan Adobe Experience Platform voor klant het richten en verpersoonlijken wordt ontdekt. Voor informatie over publiek het publiceren, zie [&#x200B; publiek het publiceren overzicht &#x200B;](/help/components/audiences/audiences-overview.md).

De analyse van het publiek staat u toe om de gegevens van het publiekslidmaatschap van de Gegevensreeksen van het Profiel van Experience Platform in een verbinding van Customer Journey Analytics in te voeren. Soorten publiek wordt beschikbaar als nieuwe afmetingen voor gebruik in Analysis Workspace.

In het volgende diagram en de bijbehorende tabel ziet u een voorstelling op hoog niveau van de manier waarop een configuratie voor publieksanalyse in Customer Journey Analytics Experience Platform-publieksgegevens beschikbaar maakt in Analysis Workspace:

![&#x200B; overzicht van de de analyseanalyse van het publiek &#x200B;](assets/audience-analysis-overview.png)

| Getal | Functie | Functie |
|---------|----------|---------|
| 1 | Configuratie van publieksanalyse | De configuratieinterface in Customer Journey Analytics die voor het vormen van publieksanalyse wordt gebruikt. |
| 2 | Sandbox | Moet de profieldataset bevatten die u aan uw verbinding wilt toevoegen. |
| 3 | Profielgegevensset | Moet de Experience Platform-publieksgegevens bevatten die u wilt analyseren. Deze profieldataset wordt toegevoegd aan de verbinding die u selecteert. |
| 4 | Samenvoegbeleid | Het samenvoegbeleid dat is gekoppeld aan het Experience Platform-publiek dat u wilt analyseren. |
| 5 | Profielgegevens | De profielgegevens die zijn gekoppeld aan het samenvoegbeleid dat u selecteert. Deze gegevens zijn beschikbaar in Experience Platform-gegevenssets. |
| 6 | Nieuwe opzoekgegevensset | Verstrekt vriendschappelijke namen voor de nieuwe publieksafmetingen die worden gecreeerd. <p>De opzoekdataset wordt automatisch gecreeerd en aan de verbinding toegevoegd, samen met de profieldataset u selecteert.</p> |
| 7 | Verbinding | De verbinding waar u de profieldataset wilt toevoegen die u selecteert. |
| 8 | Nieuwe doelafmetingen | Nieuwe publieksafmetingen <!--and metrics?--> die het publiek van Experience Platform vertegenwoordigen die in de profieldataset inbegrepen zijn u selecteerde, en beschikbaar voor rapportering in Analysis Workspace zijn. Deze afmetingen worden automatisch gemaakt. |
| 9 | Gegevensweergaven | De gegevensweergaven die u selecteert en die aan uw verbinding zijn gekoppeld. Dit zijn de gegevensweergaven die u wilt gebruiken voor het analyseren van Experience Platform-publieksgegevens in Analysis Workspace. Deze gegevensweergaven worden automatisch geconfigureerd met Experience Platform-publieksgegevens voor rapportage. |

## publieksanalyse configureren

Wanneer u publieksanalyse vormt, selecteert u de zandbak en voegt beleid verbonden aan het publiek van Experience Platform dat u wilt analyseren samen. Customer Journey Analytics leidt tot een nieuwe raadplegingsdataset, dan voegt automatisch de raadplegingsdataset en de profieldataset aan de verbinding toe u kiest.

>[!IMPORTANT]
>
>De gegevens van het publiek worden elke nacht opnieuw verwerkt en gegenereerd, waardoor de gegevens van het publiek alleen voor de vorige dag (&quot;gisteren&quot;) nauwkeurig zijn.
>
>Het publiek is beschikbaar in de gegevensmeningen van Customer Journey Analytics op de dag nadat u de configuratie van de publieksanalyse creeert.

Voor meer informatie, zie [&#x200B; publieksanalyse &#x200B;](/help/connections/audience-analysis/audience-analysis-configure.md) vormen.

## De configuraties van de publieksanalyse beheren

U kunt de configuraties van de publieksanalyse beheren nadat zij worden gecreeerd. U kunt configuraties weergeven, bewerken en verwijderen.

Voor informatie over het beheren van bestaande configuraties van de publieksanalyse, zie [&#x200B; de configuraties van de publieksanalyse beheren &#x200B;](/help/connections/audience-analysis/audience-analysis-manage.md).

## Gebruikersgegevens in Customer Journey Analytics analyseren

Met de publieksgegevens beschikbaar in Customer Journey Analytics kunt u actioneerbare inzichten krijgen in het gedrag van publieksleden op verschillende kanalen.

U kunt bijvoorbeeld het gedrag bijhouden van individuele klanten die deel uitmaakten van dezelfde e-mailpromotie. Met het publiek beschikbaar in Customer Journey Analytics, kunt u de volgende soorten informatie over elk publiekslid zien:

* Doorklikken van de e-mail naar de site die uiteindelijk tot een aankoop heeft geleid

* Leden van het publiek die uiteindelijk een in-store aankoop maakten

Voor meer informatie, zie [&#x200B; het publiek van Experience Platform in Customer Journey Analytics &#x200B;](/help/connections/audience-analysis/analyze-audiences.md) analyseren.

## De rol van de analyse van het publiek en toestemmingsvereisten

De volgende Customer Journey Analytics-rollen en Experience Platform-machtigingen zijn vereist voor publieksanalyse:

| Capaciteit | Customer Journey Analytics rol- of machtigingsvereisten | Experience Platform-machtigingsvereisten |
|---------|----------|----------|
| [&#x200B; creeer de configuraties van de publieksanalyse &#x200B;](/help/connections/audience-analysis/audience-analysis-configure.md) | Systeembeheerder | <ul><li>Gegevensbestanden: leesmachtigingen</li><li>Schema&#39;s: lezen, schrijven</li><li>Naamruimten: lezen</li></ul> |
| {de dimensies van de het publiek van de mening van 0} Mening in de gegevensmening [&#128279;](/help/connections/audience-analysis/audience-analysis-configure.md#view-audience-dimensions-in-the-data-view) | Beheerder van productprofielen voor het productprofiel waaraan de gegevensweergave is toegewezen <p>Voor meer informatie, zie [&#x200B; controle van de Toegang &#x200B;](/help/technotes/access-control.md).</p> | N.v.t. |
| Analysedimensies voor het publiek gebruiken in Analysis Workspace | Toegang tot een gegevensweergave waar de afmetingen voor de publieksanalyse zijn toegevoegd | N.v.t. |

## Limieten voor de analyse van het publiek

Overweeg de volgende grenzen wanneer [&#x200B; het vormen publieksanalyse &#x200B;](/help/connections/audience-analysis/audience-analysis-configure.md):

* Eén sandbox biedt ondersteuning voor maximaal 100 configuraties voor publieksanalyse.

* Een verbinding kan met slechts één configuratie van de publieksanalyse worden geassocieerd.








