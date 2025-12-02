---
title: Rapportsuites combineren met verschillende schema's
description: Leer hoe te om Prep van Gegevens te gebruiken om rapportreeksen met verschillende schema's te combineren
exl-id: 2656cc21-3980-4654-bffb-b10908cb21f5
feature: Use Cases
role: User
source-git-commit: a133f60e66b34a851d2e8e1c0a853cdbc1f8d51f
workflow-type: tm+mt
source-wordcount: '1321'
ht-degree: 0%

---

# Rapportsets combineren met verschillende schema&#39;s

De [&#x200B; bron van Analytics schakelaar &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html) brengt de gegevens van de rapportreeks van Adobe Analytics in Adobe Experience Platform voor gebruik door de toepassingen van Adobe Experience Platform, zoals het Platform van Gegevens van de Klant in real time en Customer Journey Analytics (Customer Journey Analytics). Elke rapportreeks die in Adobe Experience Platform wordt gebracht wordt gevormd als individuele gegevensstroom van de bronverbinding, en elk dataflow land als dataset binnen het de gegevensmeer van Adobe Experience Platform. De bronschakelaar van de Analyse leidt tot één dataset per rapportreeks.

De klanten van Customer Journey Analytics gebruiken [&#x200B; verbindingen &#x200B;](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) om datasets van het de gegevensmeer van Adobe Experience Platform in Customer Journey Analytics Analysis Workspace te integreren. Nochtans, wanneer het combineren van rapportsuites binnen een verbinding, schemaverschillen tussen rapportsuites moeten worden opgelost gebruikend de 1&rbrace; functionaliteit van de Prep van de Gegevens van Adobe Experience Platform [&#x200B; &lbrace;. &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html) Het doel is ervoor te zorgen dat Adobe Analytics-variabelen zoals props en eVars in Customer Journey Analytics een consistente betekenis hebben.

## Schemaverschillen tussen rapportsuites zijn problematisch

Stel dat uw bedrijf gegevens van twee verschillende rapportsuites naar Adobe Experience Platform wil brengen voor gebruik door Customer Journey Analytics, en veronderstelt de schema&#39;s voor de twee rapportsuites verschillen:

| Reeks A rapporteren | Reeks B rapporteren |
| --- | --- |
| eVar1 = Zoekterm | eVar1 = Bedrijfseenheid |
| eVar2 = Klantcategorie | eVar2 = Zoekterm |

Voor de eenvoud, veronderstel dit de enige bepaalde eVars voor beide rapportreeksen zijn.

Stel dat u de volgende handelingen uitvoert:

- Creeer een Analytics bronverbinding (zonder gebruik van gegevens prep) die **Reeks A van het Rapport** in het gegevensmeer van Adobe Experience Platform opneemt aangezien **Dataset A**.
- Creeer een Analytics bronverbinding (zonder gebruik van gegevens prep) die **Reeks B van het Rapport** in het gegevensmeer van Adobe Experience Platform opneemt aangezien **Dataset B**.
- Creeer de verbinding van a [&#x200B; Customer Journey Analytics &#x200B;](/help/connections/create-connection.md) riep **Alle Reeksen van het Rapport** die Dataset A en Dataset B combineren.
- Creeer a [&#x200B; de gegevensmening van Customer Journey Analytics &#x200B;](/help/data-views/create-dataview.md) geroepen **Globale Mening** die op de Al verbinding van de Reeksen van het Rapport gebaseerd is.

Zonder het gebruik van Prep van Gegevens om de schemaverschillen tussen Dataset A en Dataset B op te lossen, zullen eVars in de Globale mening gegevensmening een mengeling van waarden bevatten:

| Algemene weergave van gegevens in Customer Journey Analytics |
| --- |
| eVar1 => een combinatie van zoektermen en bedrijfseenheden |
| eVar2 => een combinatie van klantcategorieën en zoektermen |

Deze situatie leidt tot betekenisloze rapporten voor eVar1 en eVar2:

- De eVar-velden bevatten een mengeling van waarden met verschillende semantische betekenissen.
- Zoektermen worden verspreid tussen eVar1 en eVar2.
- Het is niet mogelijk verschillende toewijzingsmodellen te gebruiken voor elk van zoektermen, bedrijfseenheden en klantcategorieën.

## Adobe Experience Platform Data Prep gebruiken om schemaverschillen tussen rapportsuites op te lossen

De Experience Platform Data Prep-functionaliteit is geïntegreerd met de bronconnector van Analytics en kan worden gebruikt om de schemaverschillen op te lossen die in het bovenstaande scenario worden beschreven. Dit resulteert in eVars met consistente betekenissen in de gegevensweergave van Customer Journey Analytics. (De naamgevingsconventies die hieronder worden gebruikt, kunnen naar wens worden aangepast.)

1. Alvorens de bronverbindingsdataflows voor de Reeks van het Rapport A en de Reeks B van het Rapport tot stand te brengen, [&#x200B; creeer een nieuw schema &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html) in Adobe Experience Platform (wij zullen het **Verenigd Schema** in ons voorbeeld roepen.) Voeg het volgende toe aan het schema:

   | &quot;Unified Schema&quot; |
   | --- |
   | **XDM ExperienceEvent** klasse |
   | **Adobe Analytics ExperienceEvent Malplaatje** gebiedsgroep |

1. Voeg een andere gebiedsgroep aan het schema toe of [&#x200B; creeer een groep van het douanegebied &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/field-groups.html#:~:text=To%20create%20a%20new%20field,section%20in%20the%20left%20rail) en voeg het aan het schema toe. Wij zullen een nieuwe gebiedsgroep tot stand brengen en het **Verenigde Gebieden** roepen. Vervolgens voegen we de volgende velden toe aan de nieuwe veldgroep:

   | Aangepaste veldgroep &quot;Verenigde velden&quot;  |
   | --- |
   | Zoekterm |
   | Bedrijfseenheid |
   | Klantcategorie |

1. Creeer de gegevensstroom van de bronverbinding voor **Reeks A van het Rapport**, die **Verenigd Schema** voor gebruik in dataflow selecteren. Voeg als volgt aangepaste toewijzingen toe aan de gegevensstroom:

   | Een bronveld van de rapportsuite | Doelveld uit veldgroep Verenigde velden |
   | --- | --- |
   | \_experience.analytics.customDimensions.eVars.eVar1 | _\&lt;path>_.Search_term |
   | \_experience.analytics.customDimensions.eVars.eVar2 | _\&lt;path>_.Customer_category |

   >[!NOTE]
   >
   >Het XDM-pad voor uw doelvelden is afhankelijk van de structuur van uw aangepaste veldgroep.

1. Creeer de gegevensstroom van de bronverbinding voor **Reeks B van het Rapport**, opnieuw selecterend **Verenigd Schema** voor gebruik in dataflow. De workflow toont aan dat twee velden een beschrijvingsnaamconflict hebben. Dit komt doordat de beschrijvingen voor eVar1 en eVar2 in Report Suite B anders zijn dan in Report Suite A. Maar we weten dit al, zodat we het conflict veilig kunnen negeren en aangepaste toewijzingen als volgt kunnen gebruiken:

   | Bronveld van Reeks B rapporteren | Doelveld uit veldgroep Verenigde velden |
   |---|---|
   | \_experience.analytics.customDimensions.eVars.eVar1 | _\&lt;path>_.Business_unit |
   | _experience.analytics.customDimensions.eVars.eVar2 | _\&lt;path>_.Search_term |

1. Creëer nu een **Al verbinding van het Rapport** voor Customer Journey Analytics, die Dataset A en Dataset B combineren.

1. Creeer a **Globale mening** gegevensmening in Customer Journey Analytics. Negeer de oorspronkelijke eVar-velden en neem alleen de velden van de veldgroep Verenigde velden op.

   **Globale mening** gegevensmening in Customer Journey Analytics:

   | Source-veld | Opnemen in de gegevensweergave? |
   | --- | --- |
   | \_experience.analytics.customDimensions.eVars.eVar1 | Nee |
   | \_experience.analytics.customDimensions.eVars.eVar2 | Nee |
   | _\&lt;path>_.Search_term | Ja |
   | _\&lt;path>_.Customer_category  | Ja |
   | _\&lt;path>_.Business_unit | Ja |

U hebt nu eVar1 en eVar2 van de suites van het bronrapport aan drie nieuwe gebieden in kaart gebracht. Een ander voordeel van het gebruik van gegevenspreparaties is dat de doelvelden nu zijn gebaseerd op semantisch betekenisvolle namen (zoekterm, bedrijfseenheid, categorie van klanten) in plaats van de minder betekenisvolle eVar-namen (eVar1, eVar2.)

>[!NOTE]
>
>De verenigde groep van het douaneveld, en de bijbehorende gebiedstoewijzingen kunnen aan bestaande gegevensstromen van de bron van Analytics en datasets op elk ogenblik worden toegevoegd. Dit is echter alleen van invloed op doorlopende gegevens.

## Meer dan alleen rapportsuites

De mogelijkheden van de Prep van Gegevens om datasets met verschillende schema&#39;s te combineren gaat voorbij Analytics rapportreeksen. Stel dat u twee datasets hebt die de volgende gegevens bevatten:

| Dataset A = Analytics report suite via de bronconnector van Analytics |
| --- |
| `eVar1` => Klantcategorie |

| Dataset B = Gegevens callcenter |
| --- |
| Some_field => Klantcategorie |

Gebruikend de Prep van Gegevens, kunt u de Categorie van de Klant in eVar 1 in de gegevens van Analytics met de Categorie van de Klant op Some_field in de gegevens van het vraagcentrum combineren. Hier is één manier waarop je dat kunt doen. Ook hier kan de naamgevingsconventie aan uw wensen worden aangepast.

1. Maak een schema in Adobe Experience Platform. Voeg het volgende toe aan het schema:

   | &quot;Uitgebreid schema&quot; |
   | --- |
   | **klasse van de Gebeurtenis van de Ervaring 0&rbrace; XDM** |
   | **het Malplaatje van de Gebeurtenis van de Ervaring van Adobe Analytics** gebiedsgroep |

1. Maak een nieuwe veldgroep en voeg deze toe aan het schema. Velden toevoegen aan de veldgroep:

   | Aangepaste veldgroep &quot;Klantgegevens&quot;  |
   | --- |
   | Customer_category |

1. Creeer dataflow voor **Dataset A**, die **Uitgebreid Schema** als uw schema selecteren. Voeg als volgt aangepaste toewijzingen toe aan de gegevensstroom:

   | Gegevensset A-bronveld | Doelveld uit de veldgroep Klantgegevens |
   | --- | --- |
   | \_experience.analytics.customDimensions.eVars.eVar2 | _\&lt;path>_.Customer_category |

1. Creeer dataflow voor **Dataset B**, opnieuw selecterend **Uitgebreid Schema** als uw schema. Voeg als volgt aangepaste toewijzingen toe aan de gegevensstroom:

   | Bronveld Gegevensset B | Doelveld uit de veldgroep Klantgegevens |
   | --- | --- |
   | _\&lt;path>_.Some_field | _\&lt;path>_.Customer_category |

1. Maak een Customer Journey Analytics-verbinding waarin Dataset A en Dataset B worden gecombineerd.

1. Maak een gegevensweergave in Customer Journey Analytics met de Customer Journey Analytics-verbinding die u zojuist hebt gemaakt. Negeer de originele eVar-velden en neem alleen de velden op van de veldgroep Klantgegevens.

   Gegevensweergave in Customer Journey Analytics:

   | Source-veld | Opnemen in de gegevensweergave? |
   |---|---|
   | \_experience.analytics.customDimensions.eVars.eVar1 | Nee |
   | \_experience.analytics.customDimensions.eVars.eVar2 | Nee |
   | _\&lt;path>_.Customer_category | Ja |

## Data Prep vs. Component ID

Zoals hierboven is beschreven, kunt u met Data Prep verschillende velden aan elkaar toewijzen in meerdere Adobe Analytics-rapportensuites. Dit is handig in Customer Journey Analytics wanneer u gegevens uit meerdere gegevenssets wilt combineren tot één Customer Journey Analytics-verbinding. Als u de rapportsuites echter in afzonderlijke Customer Journey Analytics-verbindingen wilt bewaren, maar u wilt één set rapporten gebruiken voor die verbindingen en gegevensweergaven, biedt het wijzigen van de onderliggende Component ID in Customer Journey Analytics een manier om rapporten compatibel te maken, zelfs als de schema&#39;s verschillend zijn. Zie {de Montages van de Component 0} [&#x200B; voor meer informatie.](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/overview.html)

Het wijzigen van de Component ID is een Customer Journey Analytics-enige functie en heeft geen invloed op gegevens van de Analytics-bronconnector die naar Real-time Customer Profile en RTCDP wordt verzonden.
