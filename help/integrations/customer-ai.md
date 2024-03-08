---
description: Ontdek hoe Adobe Experience Platform Customer AI-gegevens integreren met Workspace in Customer Journey Analytics.
title: AI-gegevens van de klant integreren met Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
exl-id: 5411f843-be3b-4059-a3b9-a4e1928ee8a9
feature: Experience Platform Integration
source-git-commit: 46d799ad2621d83906908a3f60a59a1027c6518c
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 0%

---

# AI-gegevens van klanten integreren met Adobe Customer Journey Analytics

{{release-limited-testing}}

[Customer AI](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/customer-ai/overview.html), als onderdeel van Adobe Experience Platform Intelligent Services, biedt marketers de kracht om klantprognoses op individueel niveau te genereren.

Met behulp van invloedrijke factoren kan de AI van de Klant u vertellen wat een klant waarschijnlijk zal doen en waarom. Bovendien kunnen marketers profiteren van de voorspellingen en inzichten van de klant van AI om de ervaringen van klanten aan te passen door de meest geschikte aanbiedingen en berichten te bedienen.

AI van de Klant baseert zich op individuele gedragsgegevens en profielgegevens voor het rangschikken van eigenschappen. De AI van de Klant is flexibel in die zin dat het in veelvoudige gegevensbronnen, met inbegrip van Adobe Analytics, Adobe Audience Manager, de gegevens van de Gebeurtenis van de Consumentenervaring en de gegevens van de Gebeurtenis van de Ervaring kan nemen. Als u de bronschakelaar van het Experience Platform gebruikt om Adobe Audience Manager en Adobe Analytics gegevens in te brengen, neemt het model automatisch de standaardgebeurtenistypen op om het model te trainen en te scoren. Als u uw eigen dataset van de Gebeurtenis van de Ervaring zonder standaardgebeurtenistypen brengt, zullen om het even welke relevante gebieden als douanegebeurtenissen of profielattributen moeten worden in kaart gebracht als u het in het model wilt gebruiken. Dit kan worden gedaan in de configuratiestap van AI van de Klant in Experience Platform.

De AI van de klant kan met de Customer Journey Analytics integreren voor zover de door de AI van de Klant ingeschakelde datasets kunnen worden gebruikt in gegevensweergaven en rapportage in Customer Journey Analytics. U kunt:

* **Volgheidscores bijhouden voor een gebruikerssegment in de loop van de tijd**.
   * Gebruiksscenario: begrijp hoe waarschijnlijk klanten in een bepaald segment zijn dat ze moeten converteren.
   * Voorbeeld: een markator in een hotelketen wil begrijpen hoe waarschijnlijk het is dat een hotelklant een showticket koopt op de concertlocatie van het hotel.
* **Analyseren welke succesgebeurtenissen of kenmerken zijn gekoppeld aan propensiteitsscores**.
   * Gebruik hoofdletters/kleine letters: begrip van de kenmerken of succesgebeurtenissen die zijn gekoppeld aan propensiteitsscores.
   * Voorbeeld: een marketer in een hotelketen wil begrijpen hoe aankopen van showtickets op de concertlocatie van een hotel gekoppeld zijn aan nevenscores.
* **Volg de ingangsstroom voor klantenneiging over verschillende het scoren looppas**.
   * Gebruiksscenario: Begrijp mensen die aanvankelijk gebruikers met een lage dichtheid waren en in de loop der tijd gebruikers met een hoge dichtheid werden.
   * Voorbeeld: een marketer in een hotelketen wil begrijpen welke hotelklanten aanvankelijk werden geïdentificeerd als klanten met een lage neiging om een showticket te kopen, maar in de loop der tijd werden klanten met een hoge neiging om een showticket te kopen.
* **Kijk naar de verdeling van de neiging**.
   * Gebruik hoofdletters/kleine letters: begrip voor de spreiding van de scores voor de dichtheid om nauwkeuriger te zijn bij het definiëren van segmenten.
   * Voorbeeld: een detailhandelaar wil een specifieke promotie voor $50 van een product in werking stellen. Ze willen misschien slechts een zeer beperkte promotie uitvoeren vanwege de begroting, enzovoort. Zij analyseren de gegevens en besluiten slechts de top 80%+ van hun klanten te richten.
* **Kijk naar de neiging om in de loop der tijd een actie voor een bepaald cohort uit te voeren**.
   * Hoofdlettergebruik: houd een specifieke code in de loop van de tijd bij.
   * Voorbeeld: een markator in een hotelketen wil hun bronzen laag volgen ten opzichte van hun zilveren laag, of een zilveren laag ten opzichte van hun gouden laag, in de loop van de tijd. Ze zien de neiging van elke cohort om het hotel in de loop van de tijd te boeken.

Voer de volgende stappen uit om AI-gegevens van de klant daadwerkelijk te integreren met Customer Journey Analytics:

>[!NOTE]
>
>Sommige stappen worden uitgevoerd in Adobe Experience Platform voordat de uitvoer in Customer Journey Analytics wordt uitgevoerd.


## Stap 1: Een AI-instantie van een klant configureren

Nadat u de gegevens hebt voorbereid en al uw gegevens en schema&#39;s hebt geïnstalleerd, begint u met het volgende: [Een AI-instantie van een klant configureren](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/customer-ai/user-guide/configure.html) in Adobe Experience Platform.

## Stap 2: Opstelling een verbinding van de Customer Journey Analytics aan de datasets van AI van de Klant

In Customer Journey Analytics kunt u nu [een of meer verbindingen maken](/help/connections/create-connection.md) op gegevenssets van het Experience Platform die van instrumenten zijn voorzien voor de AI van de Klant. Elke voorspelling, zoals &quot;Waarschijnlijkheid om rekening te bevorderen&quot;, vergelijkt met één dataset. Deze datasets worden weergegeven met het voorvoegsel &quot;Customer AI Scores in EE Format - name_of_application&quot;.

>[!IMPORTANT]
>
>Elke AI-instantie van de Klant heeft twee uitvoergegevenssets als de schakeloptie is ingeschakeld om scores voor Customer Journey Analytics tijdens de configuratie in Stap 1 in te schakelen. Eén uitvoergegevensset wordt weergegeven in de indeling Profile XDM en één in de indeling Experience Event XDM.

![CAI-scores](assets/cai-scores.png)

![Verbinding maken](assets/create-conn.png)

Hier is een voorbeeld van een schema XDM dat de Customer Journey Analytics als deel van een bestaande of nieuwe dataset zou opnemen:

![CAI-schema](assets/cai-schema.png)

(Merk op dat het voorbeeld een profieldataset is; de zelfde reeks schemavoorwerp zou deel van een dataset van de Gebeurtenis van de Ervaring uitmaken die de Customer Journey Analytics zou grijpen. De dataset van de Gebeurtenis van de Ervaring zou timestamps als scoredatum omvatten.) Elke klant die in dit model een score heeft behaald, heeft een scoreDate, enzovoort. geassocieerd met hen.

## Stap 3: Creeer gegevensmeningen die op deze verbindingen worden gebaseerd

In Customer Journey Analytics kunt u nu doorgaan naar [gegevensweergaven maken](/help/data-views/create-dataview.md) met de dimensies (zoals score, scoredatum, waarschijnlijkheid, enzovoort) en metriek die zijn ingevoerd als onderdeel van de verbinding die u hebt gemaakt.

![Gegevensweergavevenster maken](assets/create-dataview.png)

## Stap 4: Rapport over CAI-scores in Workspace

In de Werkruimte van de Customer Journey Analytics, creeer een nieuw project en trek in visualisaties.

### Scherptediepte van trend

Hier is een voorbeeld van een project van de Werkruimte met de gegevens van CAI die de tendensiteitsscores voor een segment van gebruikers in tijd, in &#x200B; een gestapeld staafdiagram trends:

![Score-emmers](assets/workspace-scores.png)

### Tabel met redencodes

Hier volgt een tabel met redencodes waarom een segment een &#x200B; met een hoge of lage dichtheid heeft:

![Reden](assets/reason-codes.png)

### Invoerstroom voor klantgevoeligheid

Dit stroomdiagram toont de ingangsstroom voor klantenneiging over verschillende het scoren looppas &#x200B;:

![Invoer stroom](assets/flow.png)

### Verdeling van de dichtheid

In dit staafdiagram wordt de verdeling van &#x200B; voor de dichtheid getoond:

![Distributie](assets/distribution.png)

### Propensiteit overlapt

In dit Venn-diagram ziet u de nevenoverlappingen in verschillende scoring-reeksen:

![Propensiteit overlapt](assets/venn.png)
