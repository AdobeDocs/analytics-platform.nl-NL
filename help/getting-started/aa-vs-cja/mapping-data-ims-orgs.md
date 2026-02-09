---
title: Gegevenstoewijzing tussen IMS
description: Leer hoe u kunt verzoeken om gegevens van rapportreeksen van veelvoudige bronIMS organisaties aan een organisatie van bestemmingsIMS in kaart te brengen.
role: Admin
solution: Customer Journey Analytics
feature: Adobe Analytics Integration,Administration
hide: true
hidefromtoc: true
exl-id: c109742b-c1c5-45b3-971f-f8dcf814ec37
source-git-commit: 16486ded009a9dbd9170240c0941853a4deec0af
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# Gegevenstoewijzing tussen IMS

De bronschakelaar van de Analyse kan slechts gegevens van Adobe Analytics rapportreeksen opnemen die tot de zelfde organisatie behoren waarvoor u gerechtigd bent om Customer Journey Analytics te gebruiken. De *eigenschap van de gegevenstoewijzing van 0&rbrace; dwars-IMS is een eigenschap om de gegevens van de Analyse van veelvoudige organisaties in kaart te brengen IMS en verstrekt een oplossing voor deze beperking.* Het proces om deze functie in te schakelen wordt in dit artikel beschreven.


## Scenario

U bent voorzien van veelvoudige organisaties IMS en hebt de gegevens van Analytics in veelvoudige rapportreeksen over deze organisaties IMS. Deze instelling kan het resultaat zijn van:

* verwervingen of fusies
* organisatorische structuurvereisten
* beperkingen voor regionale inzet

Uit de doos, kunt u niet over de combinatie gegevens van veelvoudige rapportreeksen over veelvoudige organisaties IMS in Customer Journey Analytics rapporteren. De reden voor deze beperking is dat gegevensinvoer van Adobe Analytics naar Experience Platform via de Analytics-bronconnector alleen de opname van gegevens die eigendom zijn van één IMS-organisatie ondersteunt. De IMS-organisatie waarvoor u provisioned bent en die u gebruikt om u aan te melden bij Adobe Analytics, Experience Platform en Customer Journey Analytics.

Met de *dwars-IMS gegevenstoewijzing* eigenschap, kunt u Adobe verzoeken om gegevens in kaart te brengen. De eigenschap gebruikt de bron van Analytics schakelaar aan kaartgegevens van rapportreeksen die over veelvoudige *bron* organisaties IMS verblijven om reeksen (en uiteindelijke datasets) te melden die deel van één *bestemmings* organisatie IMS uitmaken. Bijvoorbeeld:

| Illustratie | Toelichting |
|---|---|
| ![&#x200B; gegevens van de Kaart over veelvoudige organisaties IMS &#x200B;](/help/getting-started/assets/map-data-across-ims-orgs.svg) | Deze afbeelding staat u toe om over rapportreeksen te rapporteren die in organisatie 1 bestaan IMS, organisatie 2 IMS, en organisatie 3 IMS van één verbinding in Customer Journey Analytics die binnen organisatie 3 wordt geleverd IMS. |

{style="table-layout:fixed"}

## Hoe wordt het gebruikt

Om de *dwars-IMS gegevenstoewijzingseigenschap* te vormen en toe te laten, moet u om de afbeelding door uw de rekeningsmanager van Adobe verzoeken. Daartoe:

1. Als beheerder van de bestemmingsIMS organisatie, verzoek goedkeurings e-mails van alle bronIMS organisatiebeheerder waarvoor u rapportreeksen wilt in kaart brengen. U kunt de volgende tekst als sjabloon voor de e-mail gebruiken om goedkeuring aan te vragen bij de IMS-bronbeheerders.

   | Voorbeeldsjabloon voor e-mail |
   | --- |
   | *de naamvertegenwoordiger van het Bedrijf*, om de geselecteerde bestemmingsorg toegang tot de volgende organisaties IMS (lijst van bronIMS organen) te verlenen, moeten wij ervoor zorgen dat een beheerder voor elke IMS org hun goedkeuring voorlegt om toegang tot hun gegevens toe te staan. Hierdoor kunnen we ervoor zorgen dat we de toegangsrechten voor gegevens van elke betrokken IMS org hebben gerespecteerd. Om ervoor te zorgen dat wij behoorlijk goedkeuring hebben, te hebben gelieve een geregistreerd Adobe admin voor elk beheer of antwoord op deze e-mail met hun naam en IMS org die zij vertegenwoordigen, die &quot;I goedkeuren&quot;zeggen om op te geven zij hun goedkeuring geven om de gegevens van deze IMS org in de bestemmingsorg [ lijstbestemming IMS org ] te hebben verschijnen. Deze beheerder moet een beheerder zijn die in het Adobe-systeem is geregistreerd als beheerder voor die IMS org. |

1. Stuur een e-mail naar de Adobe-accountmanager namens de IMS-bestemmingsbeheerder die de toewijzing aanvraagt van rapportsuites binnen meerdere IMS-bronorganisaties naar de IMS-doelorganisatie. Voeg de goedkeuringse-mails bij die u van de bron-IMS-organisatiebeheerders hebt ontvangen.

Zodra de Adobe-accountmanager het e-mailbericht ontvangt met het verzoek om analysegegevens van meerdere organen toe te wijzen, wordt het verzoek beoordeeld in Adobe. De Adobe-accountmanager neemt contact met u op voor aanvullende vragen, optionele training en andere informatie.

Zodra goedgekeurd, wordt de gevraagde afbeelding gecreeerd en u wordt op de hoogte gebracht. De bronIMS organisatienaam wordt toegevoegd aan de naam van de rapportreeks in de [&#x200B; lijst van de het rapportreeksen van Analytics &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics#select-data) in Experience Platform.


## Beperkingen

De volgende beperkingen zijn van toepassing voor de *dwars-IMS gegevenstoewijzingseigenschap*:

* U kunt een rapportsuite slechts eenmaal verbinden in verschillende organisaties.
* U moet alle verbindingen voor een organisatie schrappen IMS die als bestemmingsIMS organisatie in een afbeelding wordt bepaald alvorens u kunt verzoeken om de afbeelding te schrappen.
* ECID&#39;s zijn niet compatibel tussen toegewezen bron-IMS-organisaties en niet compatibel met de doel-IMS-organisatie.


## Overwegingen

U zou de volgende onderwerpen kunnen willen overwegen alvorens u om de *dwars-IMS gegevenstoewijzingseigenschap* verzoekt:

### Profielen

Zodra de *dwars-IMS gegevenstoewijzingseigenschap* wordt goedgekeurd, kunt u gegevens aan Experience Platform voor één of meerdere van de rapportreeksen in de organisatie van bestemmingsIMS toevoegen. U doet dit door de configuratie van de [&#x200B; bron van Analytics schakelaar &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics). De datasets van het doel worden dan gecreeerd in Experience Platform. Als deel van deze configuratie en proces, hebt u de optie om profielgegevens van één of meerdere rapportreeksen naar de dienst van het Profiel te verzenden.

Schat het totale aantal profielen dat het resultaat is van de configuratie en het proces, zoals hierboven beschreven. Zorg ervoor dat het totale aantal binnen het aantal profielen is u contractueel gerechtigd aan voor de bestemmingsorganisatie. Pas [&#x200B; het filtreren regels en voorwaarden &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics#filtering-for-profile){target="_blank"} toe om gegevens van opname aan de dienst van het Profiel te omvatten of uit te sluiten. Of schakel de optie uit om profielgegevens naar de profielservice te verzenden voor relevante rapportsuites.


### Stiksel

Zodra de *dwars-IMS gegevenstoewijzingseigenschap* wordt goedgekeurd, kunt u gegevens aan Experience Platform voor één of meerdere van de rapportreeksen in de organisatie van bestemmingsIMS toevoegen. U doet dit door de configuratie van de [&#x200B; bron van Analytics schakelaar &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics). De datasets van het doel voor de rapportreeksen u in de de bronschakelaar van de Analyse vormde worden dan gecreeerd in Experience Platform. Als deel van deze configuratie en proces, hebt u de optie om profielgegevens van één of meerdere rapportreeksen naar de dienst van het Profiel te verzenden.

U kunt zowel op gebied-gebaseerde [&#x200B; als &#x200B;](/help/stitching/fbs.md) op grafiek-gebaseerde [&#x200B; stitching op de doeldatasets gebruiken. &#x200B;](/help/stitching/gbs.md) Wanneer u op grafiek-gebaseerd het stitching op één of meerdere van deze doeldatasets gebruikt, zorg u binnen uw contractuele rechten voor het aantal profielen blijft, zoals die in de [&#x200B; 1&rbrace; sectie van Profielen &lbrace;worden geschetst.](#profiles)

Als u niet voor het Profiel van de Klant in real time wordt vergunning gegeven, maar u nog op grafiek-gebaseerd het stitching op één of meerdere doeldatasets wilt gebruiken, verzekert u slechts de [&#x200B; Dienst van de Identiteit &#x200B;](/help/stitching/faq.md#enable-a-dataset-for-the-identity-service) voor deze doeldatasets toelaat.


### Machtigingen

Een gebruiker met voldoende toestemmingen om de Analytics bronschakelaar in de organisatie van bestemmingsIMS te vormen heeft de capaciteit om de gegevens van Analytics van om het even welke in kaart gebrachte bronIMS organisatie in te voeren. Er worden voor die gebruiker geen machtigingen gecontroleerd voor een van de bron-IMS-organisaties.

### Gegevens rapporteren

De *eigenschap van de gegevenstoewijzing van 0&rbrace; dwars-IMS &lbrace;is slechts een eerste stap om u te verzekeren kunt de gegevens als deel van een verbinding van Customer Journey Analytics* gebruiken [, één of meerdere &#x200B;](/help/connections/overview.md) gegevensmeningen [&#x200B; en &#x200B;](/help/data-views/data-views.md) werkruimteprojecten [. &#x200B;](/help/analysis-workspace/home.md) U moet de gegevens die u nu in één IMS-organisatie hebt, zorgvuldig inspecteren. En overweeg eigenschappen zoals gegevens prep, afgeleide gebieden, extra raadplegingslijsten, en meer alvorens u over deze gegevens kunt behoorlijk rapporteren.
