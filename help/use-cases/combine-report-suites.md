---
source-git-commit: 59bb2c89c964f5b843897c40c38b11ada46f990a
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 1%

---
# Rapportrechten met verschillende schema&#39;s combineren

## Overzicht

De [Bronverbinding voor analyse](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en) biedt een manier om rapportsuite-gegevens van Adobe Analytics naar de Adobe Experience Platform te brengen voor gebruik door AEP-toepassingen zoals RTCDP en CJA. Elke rapportsuite die in AEP wordt geïntroduceerd, wordt geconfigureerd als een individuele bronverbindingsgegevensstroom en elke gegevensstroom landt als een gegevensset binnen het AEP-gegevensmeer. (De verbinding van de Bron van Analytics zal één dataset per rapportreeks tot stand brengen.)

CJA-klanten gebruiken [verbindingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en) gegevenssets van het gegevensmeer van AEP te integreren in de Analysis Workspace van CJA. *Wanneer echter een combinatie wordt gemaakt van een combinatie van een rapportsuite, moeten de schemaverschillen tussen de rapportsuites worden opgelost aan de hand van de [Gegevensprep](https://experienceleague.adobe.com/docs/experience-platform/data-prep/home.html?lang=en) functionaliteit om ervoor te zorgen dat Adobe Analytics-variabelen zoals props en eVars een consistente betekenis hebben in CJA.*

## Hoe de schemaverschillen tussen rapportreeksen problematisch zijn

Stel dat uw bedrijf gegevens van twee verschillende rapportsuites in AEP wil brengen voor gebruik door CJA, en veronderstelt de schema&#39;s voor de twee rapportsuites verschillen:

| Reeks A rapporteren | Reeks B rapporteren |
| --- | --- |
| eVar1 => Zoekterm | eVar1 => Bedrijfseenheid |
| eVar2 => Klantcategorie | eVar2 => Zoekterm |

Om het eenvoudig te houden zullen we zeggen dat dit de enige gedefinieerde eVars zijn voor beide verslagen.

Stel dat u de volgende handelingen uitvoert:

- Een verbinding met een bron voor Analytics maken (zonder gegevensprep) die wordt toegevoegd **Reeks A rapporteren** in AEP data Lake als **Gegevensset A**.
- Een verbinding met een bron voor Analytics maken (zonder gegevensprep) die wordt toegevoegd **Reeks B rapporteren** in AEP data Lake als **Gegevensset B**.
- Een CJA-verbinding maken met de naam **Alle rapportsets** die Dataset A en Dataset B combineert.
- Een CJA-gegevensweergave maken met de naam **Globale weergave** dat is gebaseerd op de Al verbinding van de Reeksen van het Rapport.

Zonder het gebruik van Prep van Gegevens om de schemaverschillen tussen Dataset A en Dataset B op te lossen, zullen eVars in de Globale mening gegevensmening een mengeling van waarden bevatten:

| Algemene weergave van gegevens in CJA |
| --- |
| eVar1 => een combinatie van zoektermen en bedrijfseenheden |
| eVar2 => een combinatie van klantcategorieën en zoektermen |

Deze situatie zal leiden tot betekenisloze verslagen voor eVar1 en eVar2:

- De velden eVar bevatten een mengeling van waarden met verschillende semantische betekenissen.
- Zoektermen worden verdeeld tussen eVar1 en eVar2.
- Het zal niet mogelijk zijn om verschillende attributiemodellen voor elk van onderzoekstermijnen, bedrijfseenheden, en klantencategorieën te gebruiken.

## Het gebruiken van de Prep van Gegevens AEP om schemaverschillen tussen rapportreeksen voor gebruik in CJA op te lossen

De functionaliteit van de Prep van Gegevens van AEP is geïntegreerd met de Verbinding van de Bron van Analytics en kan worden gebruikt om de schemaverschillen op te lossen die in het scenario hierboven worden beschreven, resulterend in ars met verenigbare betekenis in de CJA gegevensmening. Hierna volgt een beschrijving van hoe dit kan worden verwezenlijkt. De onderstaande naamgevingsconventies kunnen naar wens worden aangepast.

Creëer vóór het creëren van de gegevensstromen van de bronverbinding voor de Reeks A van het Rapport en Suite B, een groep van het douanegebied in AEP (wij zullen het noemen **Verenigde velden** in ons voorbeeld) dat de volgende gebieden bevat:

| Aangepaste veldgroep &quot;Verenigde velden&quot;  |
| --- |
| Zoekterm |
| Bedrijfseenheid |
| Klantcategorie |

Een nieuw schema maken in AEP (we noemen het **Unified Schema** in ons voorbeeld.) Voeg de volgende veldgroepen toe aan het schema:

| Veldgroepen voor &quot;Unified Schema&quot; |
| --- |
| XDM Experience Event |
| Adobe Analytics Experience Event-sjabloon |
| Verenigde velden |

Bij het maken van de bronverbindingsgegevensstroom voor **Reeks A rapporteren**, selecteert u **Unified Schema** voor gebruik in de gegevensstroom. Voeg als volgt aangepaste toewijzingen toe:

| Een bronveld van de rapportsuite | Doelveld uit veldgroep Verenigde velden |
| --- | --- |
| \_experience.analytics.customDimensions.eVars.eVar1 | _\&lt;path>_.search_term |
| \_experience.analytics.customDimensions.eVars.eVar2 | _\&lt;path>_.Customer_category |

Opmerking: Het XDM-pad voor uw doelvelden is afhankelijk van de manier waarop u de aangepaste veldgroep instelt.

Bij het maken van de bronverbindingsgegevensstroom voor **Reeks B rapporteren** selecteert u nogmaals **Unified Schema** voor gebruik in de gegevensstroom. De workflow toont aan dat twee velden een beschrijvingsnaamconflict hebben. Dit komt doordat de beschrijvingen voor eVar1 en eVar2 in Report Suite B anders zijn dan in Report Suite A. Maar we weten dit al, zodat we het conflict veilig kunnen negeren en aangepaste toewijzingen als volgt kunnen gebruiken:

| Bronveld van Reeks B rapporteren | Doelveld uit veldgroep Verenigde velden |
|---|---|
| \_experience.analytics.customDimensions.eVars.eVar1 | _\&lt;path>_.Business_unit |
| _experience.analytics.customDimensions.eVars.eVar2 | _\&lt;path>_.search_term |

Maak nu een **Alle rapportsets** verbinding voor CJA, het combineren van Dataset A en Dataset B.

Een **Globale weergave** gegevensweergave in CJA. Negeer de oorspronkelijke velden eVar en neem alleen de velden van de veldgroep Verenigde velden op.

Globale weergave van weergavegegevens in CJA:

| Bronveld | Opnemen in de gegevensweergave? |
| --- | --- | 
| \_experience.analytics.customDimensions.eVars.eVar1 | Nee |
| \_experience.analytics.customDimensions.eVars.eVar2 | Nee |
| _\&lt;path>_.search_term | Ja |
| _\&lt;path>_.Customer_category  | Ja |
| _\&lt;path>_.Business_unit | Ja |

In wezen hebt u nu eVar1 en eVar2 van de bronrapportsuites aan drie nieuwe gebieden in kaart gebracht. Merk op dat een ander voordeel van het gebruiken van de afbeeldingen van de Prep van Gegevens is dat de bestemmingsgebieden nu op semantisch betekenisvolle namen (de term van het Onderzoek, BedrijfsEenheid, de categorie van de Klant) in plaats van de minder betekenisvolle namen van eVar (eVar1, eVar2.) worden gebaseerd.

Opmerking: De Verenigde de veldgroep van Gebieden van de douane, en bijbehorende gebiedstoewijzingen kunnen aan de bestaande gegevensstromen en datasets van de Bron van Analytics op elk ogenblik worden toegevoegd, nochtans zal dit vooruit:sturen slechts gegevens beïnvloeden.

## Meer dan alleen rapportsuites

De mogelijkheden van Prep van Gegevens om datasets met verschillende schema&#39;s te combineren gaat voorbij Analytics rapportreeksen. Stel dat u twee datasets hebt die de volgende gegevens bevatten:

| Dataset A = Analytics report suite via Analytics Source Connector |
| --- |
| eVar1 => Klantcategorie |

| Dataset B = Gegevens callcenter |
| --- |
| Some_field => Klantcategorie |

Met Data Prep kunt u de categorie Klant in eVar 1 in de Analytics-gegevens combineren met de categorie Klant in Some_field in de gegevens van het callcenter. Hier is één manier waarop je dat kunt doen. Ook hier kan de naamgevingsconventie aan uw wensen worden aangepast.

Een aangepaste veldgroep maken:

| Aangepaste veldgroep &quot;Klantgegevens&quot;  |
| --- |
| Customer_category |

Maak een schema in AEP. Voeg de volgende veldgroepen toe aan het schema:

| Veldgroepen voor &quot;Uitgebreid schema&quot; |
| --- | 
| XDM Experience Event |
| Adobe Analytics Experience Event-sjabloon |
| Klantgegevens |

Bij het maken van de gegevensstroom voor **Gegevensset A**, selecteert u **Uitgebreid schema** als uw schema. Voeg als volgt aangepaste toewijzingen toe:

| Gegevensset A-bronveld | Doelveld uit de veldgroep Klantgegevens |
| --- | --- |
| \_experience.analytics.customDimensions.eVars.eVar2 | _\&lt;path>_.Customer_category |

Bij het maken van de gegevensstroom voor **Gegevensset B** selecteert u nogmaals **Uitgebreid schema** als uw schema. Voeg als volgt aangepaste toewijzingen toe:

| Bronveld Gegevensset B | Doelveld uit de veldgroep Klantgegevens |
| --- | --- |
| _\&lt;path>_.Some_field | _\&lt;path>_.Customer_category |

Creeer een verbinding CJA die Dataset A en Dataset B combineert. Maak een gegevensweergave in CJA met de zojuist gemaakte CJA-verbinding. Negeer de oorspronkelijke velden van de eVar en neem alleen de velden op van de veldgroep Klantgegevens.

Gegevensweergave in CJA:

| Bronveld | Opnemen in de gegevensweergave? |
|---|---|
| \_experience.analytics.customDimensions.eVars.eVar1 | Nee |
| \_experience.analytics.customDimensions.eVars.eVar2 | Nee |
| _\&lt;path>_.Customer_category | Ja |

## Data Prep vs. Component ID

Zoals hierboven is beschreven, kunt u met Data Prep verschillende velden aan elkaar toewijzen in meerdere Adobe Analytics-rapportsets. Dit is nuttig in CJA wanneer u gegevens van veelvoudige datasets in één enkele verbinding wilt combineren CJA. Nochtans, als u van plan bent om de rapportreeksen in afzonderlijke verbindingen te houden CJA maar u één reeks rapporten over die verbindingen en gegevensmeningen wilt gebruiken, verstrekt het veranderen van onderliggende identiteitskaart van de Component in CJA een manier om rapporten compatibel te maken zelfs als de schema&#39;s verschillend zijn. Zie [Componentinstellingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/overview.html?lang=en) voor meer informatie .

Het veranderen van identiteitskaart van de Component is een CJA-enige functie en beïnvloedt geen gegevens van de Bron van Analytics Schakelaar die naar Verenigd Profiel en RTCDP wordt verzonden.
