---
title: Analysegegevens toewijzen van meerdere IMS-organisaties
description: Leer hoe u kunt verzoeken om gegevens van rapportreeksen van veelvoudige bronIMS organisaties aan een organisatie van bestemmingsIMS in kaart te brengen.
role: Admin
solution: Customer Journey Analytics
feature: Adobe Analytics Integration,Administration
hide: true
hidefromtoc: true
source-git-commit: 3c34bd50c12b370f5e9f95ac5d6357de4f63e5f6
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# Analysegegevens toewijzen van meerdere IMS-organisaties

De bronschakelaar van de Analyse kan slechts gegevens van Adobe Analytics rapportreeksen opnemen die tot de zelfde organisatie behoren waarvoor u gerechtigd bent om Customer Journey Analytics te gebruiken. De functie om analysegegevens van veelvoudige organisaties in kaart te brengen IMS verstrekt een oplossing voor deze beperking. Het proces om deze functie in te schakelen wordt in dit artikel beschreven.


## Scenario

U bent voorzien van veelvoudige organisaties IMS en hebt de gegevens van Analytics in veelvoudige rapportreeksen over deze organisaties IMS. Deze instelling kan het resultaat zijn van:

* verwervingen of fusies
* organisatorische structuurvereisten
* beperkingen voor regionale inzet

Uit de doos, kunt u niet over de combinatie gegevens van veelvoudige rapportreeksen over veelvoudige organisaties IMS in Customer Journey Analytics rapporteren. De reden voor deze beperking is dat gegevensinvoer van Adobe Analytics naar Experience Platform via de Analytics-bronconnector alleen de opname van gegevens die eigendom zijn van één IMS-organisatie ondersteunt. De IMS-organisatie waarvoor u provisioned bent en die u gebruikt om u aan te melden bij Adobe Analytics, Experience Platform en Customer Journey Analytics.

Met de *gegevens van de Analytics van de kaart van veelvoudige organisaties IMS* eigenschap, kunt u Adobe verzoeken om gegevens in kaart te brengen. De eigenschap gebruikt de bron van Analytics schakelaar om gegevens van rapportreeksen in kaart te brengen die over veelvoudige *bron* organisaties IMS aan datasets verblijven die deel van één *bestemming* organisatie IMS uitmaken. Bijvoorbeeld:

| Illustratie | Toelichting |
|---|---|
| ![&#x200B; gegevens van de Kaart over veelvoudige organisaties IMS &#x200B;](/help/getting-started/assets/map-data-across-ims-orgs.svg) | Deze afbeelding staat u toe om over rapportreeksen te rapporteren die in organisatie 1 bestaan IMS, organisatie 2 IMS, en organisatie 3 IMS van één verbinding in Customer Journey Analytics die binnen organisatie 3 wordt geleverd IMS. |

{style="table-layout:fixed"}

## Hoe wordt het gebruikt

Om de *gegevens van de Analytics van de kaart van veelvoudige organisaties IMS* eigenschap te vormen en toe te laten, moet u om de afbeelding door uw de rekeningsmanager van Adobe verzoeken. Daartoe:

1. Als beheerder van de bestemmingsIMS organisatie, verzoek goedkeurings e-mails van alle bronIMS organisatiebeheerder waarvoor u rapportreeksen wilt in kaart brengen. U kunt de volgende tekst als sjabloon voor de e-mail gebruiken om goedkeuring aan te vragen bij de IMS-bronbeheerders.

   | Voorbeeldsjabloon voor e-mail |
   | --- |
   | *de naamvertegenwoordiger van het Bedrijf*, om de geselecteerde bestemmingsorg toegang tot de volgende organisaties IMS (lijst van bronIMS organen) te verlenen, moeten wij ervoor zorgen dat een beheerder voor elke IMS org hun goedkeuring voorlegt om toegang tot hun gegevens toe te staan. Hierdoor kunnen we ervoor zorgen dat we de toegangsrechten voor gegevens van elke betrokken IMS org hebben gerespecteerd. Om ervoor te zorgen dat wij behoorlijk goedkeuring hebben, te hebben gelieve een geregistreerd Adobe admin voor elk beheer of antwoord op deze e-mail met hun naam en IMS org die zij vertegenwoordigen, die &quot;I goedkeuren&quot;zeggen om op te geven zij hun goedkeuring geven om de gegevens van deze IMS org in de bestemmingsorg [ lijstbestemming IMS org ] te hebben verschijnen. Deze beheerder moet een beheerder zijn die in het Adobe-systeem is geregistreerd als beheerder voor die IMS org. |

1. Verzend een e-mail als bestemmingsIMS organisatiebeheerder aan de de rekeningsmanager van Adobe die om de afbeelding van rapportreeksen binnen veelvoudige bronIMS organisaties aan de bestemmingsIMS organisatie verzoekt. Voeg de goedkeuringse-mails bij die u van de bron-IMS-organisatiebeheerders hebt ontvangen.

Zodra de accountmanager het e-mailbericht ontvangt met het verzoek om analysegegevens van meerdere organen toe te wijzen, wordt het verzoek in Adobe gecontroleerd. De accountmanager neemt contact met u op voor aanvullende vragen, optionele training en andere informatie.

Zodra goedgekeurd, wordt de gevraagde afbeelding gecreeerd en u wordt op de hoogte gebracht. De bronIMS organisatienaam wordt toegevoegd aan de naam van de rapportreeks in de [&#x200B; lijst van de het rapportreeksen van Analytics &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics#select-data) in Experience Platform.

## Beperkingen en risico&#39;s

De volgende beperkingen zijn van toepassing voor de *gegevens van de Analytics van de kaart van veelvoudige organisaties IMS* eigenschap:

* U kunt een rapportsuite slechts eenmaal verbinden in verschillende organisaties.
* U moet alle verbindingen voor een organisatie schrappen IMS die als bestemmingsIMS organisatie in een afbeelding wordt bepaald alvorens u kunt verzoeken om de afbeelding te schrappen.
* ECID&#39;s zijn niet compatibel tussen toegewezen bron-IMS-organisaties en niet compatibel met de doel-IMS-organisatie.
* Een gebruiker met voldoende toestemmingen om de Analytics bronschakelaar in de organisatie van bestemmingsIMS te vormen heeft de capaciteit om de gegevens van Analytics van om het even welke in kaart gebrachte bronIMS organisatie in te voeren. Er worden voor die gebruiker geen machtigingen gecontroleerd voor een van de bron-IMS-organisaties.
