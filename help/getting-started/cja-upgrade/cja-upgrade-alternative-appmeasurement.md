---
title: Alternatieve methoden bij upgrade naar Customer Journey Analytics
description: Meer informatie over de alternatieve methoden bij het upgraden naar Customer Journey Analytics
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 0bf35c67-c8ae-4349-93fb-b9806c1064a8
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '1302'
ht-degree: 0%

---

# Alternatief voor upgrade: Gebruik AppMeasurement-gegevensverzameling met Experience Platform Web SDK en Customer Journey Analytics {#data-collection-appmeasurement}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-appmeasurement-logic"
>title="AppMeasurement-logica gebruiken met de Web SDK"
>abstract="In plaats van gegevens via een XDM-object te verzenden, verzendt u al uw variabelen in AppMeasurement-indeling via het gegevensobject.<br><br> deze optie bespaart implementatietijd door u toe te staan om uw logica van AppMeasurement aan XDM in kaart te brengen, eerder dan het bevolken van een voorwerp XDM van kras. Het leidt echter in de loop der tijd tot extra complexiteit omdat elk veld dat u in de toekomst toevoegt, in de gegevensstroom aan XDM moet worden toegewezen."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-appmeasurement-logic-step"
>title="Wijzig je AppMeasurement logica om naar het Web SDK te verwijzen"
>abstract="Deze stap wordt weergegeven omdat u een sneltoets voor de implementatie hebt gekozen. Kopieer of wijzig uw AppMeasurement-logica om het gegevensobject te vullen in plaats van het s-object. Wijzig bijvoorbeeld de toewijzing van s.eVar1 aan gegevens.__adobe.analytics.eVar1 en repeat voor alle variabelen van de Analyse."

<!-- markdownlint-enable MD034 -->

{{upgrade-note}}

Wanneer bevordering aan Customer Journey Analytics, adviseert Adobe [&#x200B; een nieuwe implementatie van de SDK van het Web van Experience Platform &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-recommendations.md). Nochtans, afhankelijk van verscheidene factoren, zoals chronologie en middelbeperkingen, zouden de geadviseerde verbeteringsstappen niet praktisch voor uw organisatie kunnen zijn.

U kunt de gegevensverzamelingslogica van uw AppMeasurement- of Analytics-extensie gebruiken met het Web SDK om gegevens naar Platform en Customer Journey Analytics te verzenden in plaats van gegevens te verzamelen met het XDM-object. Dit alternatief zorgt echter voor extra complexiteit in de loop der tijd.

## Voordelen en nadelen

Deze methode is wederzijds exclusief met [&#x200B; verzendend uw volledige gegevenslaag naar Customer Journey Analytics &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-alternative-appmeasurement.md), omdat beide methodes de zelfde taak verwezenlijken. (Deze methode heeft de voorkeur boven het verzenden van de gehele gegevenslaag naar Adobe. Het is verfijnder omdat props en evars allemaal door gegevens gaan.__adobe.analytics._veranderlijk-naam_.)

Overweeg de volgende voor- en nadelen van het gebruik van dit upgradealternatief:

| Voordelen | Nadelen |
|----------|---------|
| Dit is het voorkeurspad voor upgrades als uw Adobe Analytics-implementatie al gebruikmaakt van de Web SDK.<ul><li>**verstrekt alle voordelen om gegevens in Ervaring Edge Network** te ontvangen: <p>Deze voordelen zijn onder meer:</p><ul><li>Zeer krachtige rapportering en gegevensbeschikbaarheid omdat Adobe Experience Platform aan macht [&#x200B; wordt gebouwd verpersoonlijkingsgebruiksgevallen in real time &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html?lang=nl-NL)</li><li>Consolideer implementatie voor Adobe Experience Cloud-gegevensverzameling tussen andere Experience Cloud-producten (AJO, RTCDP, enzovoort)</li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (zoals prop, eVar, event, enzovoort)</li></ul><li>**gebruikt uw bestaande implementatie**: Terwijl deze benadering sommige implementatieveranderingen vereist, vereist het geen volledig nieuwe implementatie van kras. U kunt de bestaande gegevenslaag en -code gebruiken met minimale wijzigingen in de implementatielogica zonder dat dit van invloed is op uw bestaande Adobe Analytics-rapportage.</li><li>**verstrekt een optie om een schema XDM** te gebruiken: U kunt verkiezen om uw bestaand schema van Adobe Analytics te gebruiken of een XDM schema en kaartgebieden in het gegevensvoorwerp tot stand te brengen aan uw schema XDM. [&#x200B; XDM- schema&#39;s &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/home#xdm-schemas) zijn een flexibel schema om het even welke gebieden te bepalen u, en slechts die gebieden nodig hebt die relevant zijn. <p>Zie &quot;Gebruikend uw eigen schema XDM&quot;hieronder voor meer informatie over de voordelen om uw eigen schema te gebruiken XDM.</p></li><li>**behoudt regels en gegevenselementen**: Terwijl het nieuwe regelacties vereist, kunt u uw bestaande gegevenselementen en regelvoorwaarden met minimale veranderingen opnieuw gebruiken.</li><li>**Toekomstbestendig**: Als u verkiest om uw eigen schema te gebruiken XDM, dan zijn de toekomstige implementatieupdates gemakkelijker.</li></ul> | <ul><li>**vereist afbeelding om gegevens naar Platform** te verzenden: Wanneer uw organisatie klaar is om Customer Journey Analytics te gebruiken, moet u gegevens naar een gegevensreeks in Adobe Experience Platform verzenden. Deze actie vereist dat elk gebied in het gegevensvoorwerp een ingang in het hulpmiddel van de gegevenstoewijzing is dat het aan een XDM schemagebied toewijst. Voor deze workflow hoeft u slechts één keer toewijzingen uit te voeren, en dit betekent niet dat u implementatiewijzigingen aanbrengt. Het is echter een extra stap die niet vereist is bij het verzenden van gegevens in een XDM-object.</li><li>**introduceert extra ingewikkeldheid in tijd**: Om het even welk gebied u in de toekomst toevoegt moet aan XDM in de gegevensstroom in kaart worden gebracht.<p>Telkens wanneer een nieuw veld aan uw implementatie wordt toegevoegd, kunt u een van de volgende handelingen uitvoeren:</p><ul><li>**Optie 1:** bevolkt een nieuwe willekeurige gebeurtenis of nieuwe steun in het gegevensvoorwerp, dan kaart het aan het gewenste gebied XDM.<p>Dit proces bevordert consistentie voor de cliënt-zijimplementatie, maar het vereist afbeelding.</p></li><li>**Optie 2:** verlaat het gegevensvoorwerp als erfenisimplementatie en begin slechts het voorwerp XDM voor alle nieuwe gebieden te bevolken.<p>Dit proces vereist geen toewijzing, maar het betekent dat sommige van uw variabelen slechts in een gegevensvoorwerp worden gevestigd, terwijl andere variabelen slechts in een voorwerp XDM worden gevestigd. Wanneer u uw implementatie moet problemen oplossen, moet u naar twee plaatsen gaan. Zorg ervoor dat uw interne workflows hiervoor geschikt zijn.</p></li></ul> |

{style="table-layout:auto"}

## Standaardstappen

De basisstappen voor het migreren van een implementatie van Adobe Analytics (of AppMeasurement of de uitbreiding van Analytics) om Web SDK te gebruiken om gegevens naar Customer Journey Analytics te verzenden zijn:

1. Migreer uw Adobe Analytics-implementatie om de Adobe Experience Platform Web SDK te gebruiken en gegevens naar Edge Network te verzenden.

   Met deze stap kunt u uw bestaande Adobe Analytics-implementatie migreren voor gebruik van de Web SDK. U kunt desgewenst gegevens naar Adobe Analytics verzenden om te controleren of alles in Adobe Analytics werkt voordat u gegevens naar Customer Journey Analytics verzendt. Nadat dit wordt gevormd en de gegevens in Adobe Analytics bevredigend zijn, kunt u gegevens van Edge Network naar Customer Journey Analytics verzenden.

   Dankzij deze flexibiliteit is een meer methodische en doordachte upgrade naar Customer Journey Analytics mogelijk.

   Raadpleeg de volgende artikelen in de documentatie van Adobe Analytics voor informatie over hoe u dit kunt doen:

   * [&#x200B; Migreer aan het Web SDK gebruikend markeringen &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/implementation/aep-edge/web-sdk/analytics-extension-to-web-sdk)

   * [&#x200B; Migreer aan het Web SDK gebruikend JavaScript &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/implementation/aep-edge/web-sdk/appmeasurement-to-web-sdk)

1. Gegevens verzenden van Edge Network naar Platform.

   1. Verzend al uw variabelen in AppMeasurement-indeling via het gegevensobject.

      Voor meer informatie, zie [&#x200B; objecten van Gegevens veranderlijke afbeelding aan Adobe Analytics &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/implementation/aep-edge/data-var-mapping).

   1. Kies uw schema.

      U kunt kiezen of u uw bestaande Adobe Analytics-schema wilt gebruiken, of u kunt een XDM-schema maken dat beter op de behoeften van uw organisatie wordt afgestemd wanneer u andere platformservices gaat gebruiken.

      Adobe raadt u aan een XDM-schema te maken. Voor meer informatie, zie [&#x200B; een douaneschema tot stand brengen om met uw implementatie van SDK van het Web van Customer Journey Analytics &#x200B;](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md) te gebruiken.

      +++Adobe Analytics-schema gebruiken

      | Voordelen | Nadelen |
      |----------|---------|
      | <p>De voordelen van het Adobe Analytics-schema zijn:</p><ul><li>Eenvoudig upgraden<p>Als u reeds gegevens naar Adobe Analytics met het Web SDK van Adobe Experience Platform verzendt, kunt u de extra dienst aan uw gegevensstroom toevoegen om gegevens naar Adobe Experience Platform te verzenden (die dan in uw configuratie van Customer Journey Analytics kan worden gebruikt).</p></li></ul> | <p>De nadelen van het gebruik van het Adobe Analytics-schema zijn:</p><ul><li>Terwijl het gebruiken van het schema van Adobe Analytics beperkt u niet in termen van hoe het met andere toepassingen van het Platform kan worden gebruikt, resulteert het in een schema dat complexer is dan het anders zou kunnen zijn. Dit komt omdat het Adobe Analytics-schema veel objecten bevat die specifiek zijn voor Adobe Analytics en die waarschijnlijk niet door uw organisatie zullen worden gebruikt.<p>Wanneer wijzigingen in het schema vereist zijn, moet u door duizenden ongebruikte velden bladeren om het veld te zoeken dat moet worden bijgewerkt.</p></li></ul> |

      +++

      +++Een XDM-schema maken

      | Voordelen | Nadelen |
      |----------|---------|
      | <ul><p>De voordelen van het bijwerken aan uw eigen schema XDM omvatten:</p><ul><li>Een gestroomlijnd schema dat aan de behoeften van uw organisatie en de specifieke toepassingen van het Platform wordt aangepast die u gebruikt.</li><p>Wanneer veranderingen in het schema worden vereist, moet u niet door duizenden ongebruikte gebieden bewegen om het gebied te vinden dat het bijwerken vereist.</p></ul> | <p>De nadelen van het bijwerken aan uw eigen schema XDM omvatten:</p><ul><li>Het bijwerken van uw schema is een tijdrovend proces dat wordt vereist alvorens u begint gegevens naar Platform te verzenden.</li></ul> |

      +++

   1. Gebruik gegevenstoewijzing om alle velden in het gegevensobject toe te wijzen aan uw XDM-schema.

      Voor meer informatie, zie [&#x200B; Afbeelding &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/datastreams/data-prep?lang=en#mapping) in [&#x200B; Prep van Gegevens voor de Inzameling van Gegevens &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/datastreams/data-prep) in de documentatie van Experience Platform.

{{upgrade-final-step}}.




