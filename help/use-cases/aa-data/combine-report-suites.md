---
title: Rapportsuites combineren met verschillende schema's
description: Leer hoe te om Prep van Gegevens te gebruiken om rapportreeksen met verschillende schema's te combineren
exl-id: 2656cc21-3980-4654-bffb-b10908cb21f5
source-git-commit: 69356510596d047d80af63338fccca71e8af53cd
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 1%

---

# Rapportsets combineren met verschillende schema&#39;s

De [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en) brengt rapportsuite-gegevens van Adobe Analytics naar de Adobe Experience Platform (AEP) voor gebruik door AEP-toepassingen, zoals Real-time Customer Data Platform en Customer Journey Analytics (CJA). Elke rapportsuite die in AEP wordt geïntroduceerd, wordt geconfigureerd als een individuele bronverbindingsgegevensstroom en elke gegevensstroom landt als een gegevensset binnen het AEP-gegevensmeer. De verbinding van de Bron van Analytics leidt tot één dataset per rapportreeks.

CJA-klanten gebruiken [verbindingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en) gegevenssets van het gegevensmeer van AEP te integreren in de Analysis Workspace van CJA. Wanneer echter een combinatie wordt gemaakt van een combinatie van een rapportsuite, moeten de schemaverschillen tussen de rapportsuites worden opgelost aan de hand van de [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html?lang=en) functionaliteit. Het doel is ervoor te zorgen dat Adobe Analytics-variabelen zoals props en eVars een consistente betekenis hebben in CJA.

## Schemaverschillen tussen rapportsuites zijn problematisch

Stel dat uw bedrijf gegevens van twee verschillende rapportsuites in AEP wil brengen voor gebruik door CJA, en veronderstelt de schema&#39;s voor de twee rapportsuites verschillen:

| Reeks A rapporteren | Reeks B rapporteren |
| --- | --- |
| eVar1 = Zoekterm | eVar1 = Bedrijfseenheid |
| eVar2 = Klantcategorie | eVar2 = Zoekterm |

Om het eenvoudig te houden, laten we zeggen dat dit de enige gedefinieerde eVars zijn voor beide rapportsuites.

Stel dat u de volgende handelingen uitvoert:

- Een verbinding met een bron voor Analytics maken (zonder gegevensprep) die wordt toegevoegd **Reeks A rapporteren** in AEP data Lake als **Gegevensset A**.
- Een verbinding met een bron voor Analytics maken (zonder gegevensprep) die wordt toegevoegd **Reeks B rapporteren** in AEP data Lake als **Gegevensset B**.
- Een [CJA-verbinding](/help/connections/create-connection.md) gebeld **Alle rapportsets** die Dataset A en Dataset B combineert.
- Een [CJA-gegevensweergave](/help/data-views/create-dataview.md) gebeld **Globale weergave** dat is gebaseerd op de Al verbinding van de Reeksen van het Rapport.

Zonder het gebruik van Prep van Gegevens om de schemaverschillen tussen Dataset A en Dataset B op te lossen, zullen eVars in de Globale mening gegevensmening een mengeling van waarden bevatten:

| Algemene weergave van gegevens in CJA |
| --- |
| eVar1 => een combinatie van zoektermen en bedrijfseenheden |
| eVar2 => een combinatie van klantcategorieën en zoektermen |

Deze situatie leidt tot betekenisloze verslagen voor eVar1 en eVar2:

- De velden eVar bevatten een mengeling van waarden met verschillende semantische betekenissen.
- Zoektermen worden verdeeld tussen eVar1 en eVar2.
- Het is niet mogelijk verschillende toewijzingsmodellen te gebruiken voor elk van zoektermen, bedrijfseenheden en klantcategorieën.

## De Prep van Gegevens van AEP van het gebruik om schemaverschillen tussen rapportreeksen op te lossen

De Prep-functionaliteit van Gegevens van Experience Platform is geïntegreerd met de Bronverbinding Analytics en kan worden gebruikt om de schemaverschillen op te lossen die in het bovenstaande scenario worden beschreven. Dit resulteert in eVars met verenigbare betekenissen in de CJA gegevensmening. (De naamgevingsconventies die hieronder worden gebruikt, kunnen naar wens worden aangepast.)

1. Voordat u de gegevensstromen van de bronverbinding maakt voor Report Suite A en Report Suite B, [Een nieuw schema maken](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en) in AEP (we noemen het **Unified Schema** in ons voorbeeld.) Voeg het volgende toe aan het schema:

   | &quot;Unified Schema&quot; |
   | --- |
   | **XDM ExperienceEvent** class |
   | **Adobe Analytics ExperienceEvent-sjabloon** veldgroep |

1. Een andere veldgroep toevoegen aan het schema of [een aangepaste veldgroep maken](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/field-groups.html?lang=en#:~:text=To%20create%20a%20new%20field,section%20in%20the%20left%20rail) en voeg het toe aan het schema. We maken een nieuwe veldgroep en noemen deze **Verenigde velden**. Vervolgens voegen we de volgende velden toe aan de nieuwe veldgroep:

   | Aangepaste veldgroep &quot;Verenigde velden&quot;  |
   | --- |
   | Zoekterm |
   | Bedrijfseenheid |
   | Klantcategorie |

1. De gegevensstroom van de bronverbinding maken voor **Reeks A rapporteren**, selecteren **Unified Schema** voor gebruik in de gegevensstroom. Voeg als volgt aangepaste toewijzingen toe aan de gegevensstroom:

   | Een bronveld van de rapportsuite | Doelveld uit veldgroep Verenigde velden |
   | --- | --- |
   | \_experience.analytics.customDimensions.eVars.eVar1 | _\&lt;path>_.search_term |
   | \_experience.analytics.customDimensions.eVars.eVar2 | _\&lt;path>_.Customer_category |

   >[!NOTE]
   >
   >Het XDM-pad voor uw doelvelden is afhankelijk van de structuur van uw aangepaste veldgroep.

1. De gegevensstroom van de bronverbinding maken voor **Reeks B rapporteren**, nogmaals selecteren **Unified Schema** voor gebruik in de gegevensstroom. De workflow toont aan dat twee velden een beschrijvingsnaamconflict hebben. Dit komt doordat de beschrijvingen voor eVar1 en eVar2 in Report Suite B anders zijn dan in Report Suite A. Maar we weten dit al, zodat we het conflict veilig kunnen negeren en aangepaste toewijzingen als volgt kunnen gebruiken:

   | Bronveld van Reeks B rapporteren | Doelveld uit veldgroep Verenigde velden |
   |---|---|
   | \_experience.analytics.customDimensions.eVars.eVar1 | _\&lt;path>_.Business_unit |
   | _experience.analytics.customDimensions.eVars.eVar2 | _\&lt;path>_.search_term |

1. Maak nu een **Alle rapportsets** verbinding voor CJA, het combineren van Dataset A en Dataset B.

1. Een **Globale weergave** gegevensweergave in CJA. Negeer de oorspronkelijke velden eVar en neem alleen de velden van de veldgroep Verenigde velden op.

   **Globale weergave** gegevensweergave in CJA:

   | Bronveld | Opnemen in de gegevensweergave? |
   | --- | --- | 
   | \_experience.analytics.customDimensions.eVars.eVar1 | Nee |
   | \_experience.analytics.customDimensions.eVars.eVar2 | Nee |
   | _\&lt;path>_.search_term | Ja |
   | _\&lt;path>_.Customer_category  | Ja |
   | _\&lt;path>_.Business_unit | Ja |

U hebt nu eVar1 en eVar2 van de bronrapportreeksen aan drie nieuwe gebieden in kaart gebracht. Merk op dat een ander voordeel van het gebruiken van de afbeeldingen van de Prep van Gegevens is dat de bestemmingsgebieden nu op semantisch betekenisvolle namen (de term van het Onderzoek, BedrijfsEenheid, de categorie van de Klant) in plaats van de minder betekenisvolle namen van eVar (eVar1, eVar2.) worden gebaseerd.

>[!NOTE]
>
>De verenigde groep van het douaneveld, en de bijbehorende gebiedstoewijzingen kunnen aan bestaande gegevensstromen en datasets van de Bron van Analytics van de Schakelaar op elk ogenblik worden toegevoegd. Dit is echter alleen van invloed op doorlopende gegevens.

## Meer dan alleen rapportsuites

De mogelijkheden van Prep van Gegevens om datasets met verschillende schema&#39;s te combineren gaat voorbij Analytics rapportreeksen. Stel dat u twee datasets hebt die de volgende gegevens bevatten:

| Dataset A = Analytics report suite via Analytics Source Connector |
| --- |
| `eVar1` => Klantcategorie |

| Dataset B = Gegevens callcenter |
| --- |
| Some_field => Klantcategorie |

Gebruikend de Prep van Gegevens, kunt u de Categorie van de Klant in eVar 1 in de gegevens van Analytics met de Categorie van de Klant op Some_field in de gegevens van het vraagcentrum combineren. Hier is één manier waarop je dat kunt doen. Ook hier kan de naamgevingsconventie aan uw wensen worden aangepast.

1. Maak een schema in AEP. Voeg het volgende toe aan het schema:

   | &quot;Uitgebreid schema&quot; |
   | --- | 
   | **XDM Experience Event** class |
   | **Adobe Analytics Experience Event-sjabloon** veldgroep |

1. Maak een nieuwe veldgroep en voeg deze toe aan het schema. Velden toevoegen aan de veldgroep:

   | Aangepaste veldgroep &quot;Klantgegevens&quot;  |
   | --- |
   | Customer_category |

1. Maak de gegevensstroom voor **Gegevensset A**, selecteren **Uitgebreid schema** als uw schema. Voeg als volgt aangepaste toewijzingen toe aan de gegevensstroom:

   | Gegevensset A-bronveld | Doelveld uit de veldgroep Klantgegevens |
   | --- | --- |
   | \_experience.analytics.customDimensions.eVars.eVar2 | _\&lt;path>_.Customer_category |

1. Maak de gegevensstroom voor **Gegevensset B**, nogmaals selecteren **Uitgebreid schema** als uw schema. Voeg als volgt aangepaste toewijzingen toe aan de gegevensstroom:

   | Bronveld Gegevensset B | Doelveld uit de veldgroep Klantgegevens |
   | --- | --- |
   | _\&lt;path>_.Some_field | _\&lt;path>_.Customer_category |

1. Creeer een verbinding CJA die Dataset A en Dataset B combineert.

1. Maak een gegevensweergave in CJA met de zojuist gemaakte CJA-verbinding. Negeer de oorspronkelijke velden van de eVar en neem alleen de velden op van de veldgroep Klantgegevens.

   Gegevensweergave in CJA:

   | Bronveld | Opnemen in de gegevensweergave? |
   |---|---|
   | \_experience.analytics.customDimensions.eVars.eVar1 | Nee |
   | \_experience.analytics.customDimensions.eVars.eVar2 | Nee |
   | _\&lt;path>_.Customer_category | Ja |

## Data Prep vs. Component ID

Zoals hierboven is beschreven, kunt u met Data Prep verschillende velden aan elkaar toewijzen in meerdere Adobe Analytics-rapportsets. Dit is nuttig in CJA wanneer u gegevens van veelvoudige datasets in één enkele verbinding wilt combineren CJA. Nochtans, als u van plan bent om de rapportreeksen in afzonderlijke verbindingen te houden CJA maar u één reeks rapporten over die verbindingen en gegevensmeningen wilt gebruiken, verstrekt het veranderen van onderliggende identiteitskaart van de Component in CJA een manier om rapporten compatibel te maken zelfs als de schema&#39;s verschillend zijn. Zie [Componentinstellingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/overview.html?lang=en) voor meer informatie .

Het wijzigen van de component-id is een CJA-functie en heeft geen invloed op de gegevens van de Analytics Source Connector die naar Real-time Customer Profile en RTCDP wordt verzonden.
