---
title: Configureer uw bestaande Adobe Analytics Web SDK-implementatie om gegevens naar het platform te verzenden
description: Meer informatie over het configureren van uw bestaande Adobe Analytics Web SDK-implementatie
role: Admin
solution: Customer Journey Analytics
feature: Basics
exl-id: 1459a512-bfa8-4805-97e8-5b6acc6e4ac9
source-git-commit: 33e962bc3834d6b7d0a49bea9aa06c67547351c1
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Configureer uw bestaande Adobe Analytics Web SDK-implementatie om gegevens naar het platform te verzenden {#existing-websdk-implementation}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="cja-upgrade-remove-aa-from-datastream"
>title="Adobe Analytics verwijderen als service uit de gegevensstroom"
>abstract="Met SDK van het Web volledig functioneel, werk met uw beheerder van het Platform om Adobe Analytics als dienst uit de datastream te verwijderen. Voordat u dit doet, moet u ervoor zorgen dat uw gebruikers zijn overgegaan van het gebruik van Adobe Analytics naar Customer Journey Analytics."

<!-- markdownlint-enable MD034 -->

{{upgrade-note}}

Als uw Adobe Analytics-implementatie al gebruikmaakt van de Adobe Experience Platform Web SDK, kunt u beginnen met het verzenden van gegevens naar Platform door een gegevensstroom in te stellen. Of, als u reeds gegevens naar Platform verzendt, moet u eenvoudig een verbinding tussen de datasets van het Platform en Customer Journey Analytics tot stand brengen.


## Voordelen en nadelen

Houd rekening met de volgende voor- en nadelen van het configureren van uw bestaande Adobe Analytics Web SDK-implementatie voor het verzenden van gegevens naar Platform:

| Voordelen | Nadelen |
|----------|---------|
| Dit is het voorkeurspad voor upgrades als uw Adobe Analytics-implementatie al gebruikmaakt van de Web SDK.<ul><li>**verstrekt alle voordelen om gegevens in Ervaring Edge Network** te ontvangen: <p>Deze voordelen zijn onder meer:</p><ul><li>Zeer krachtige rapportering en gegevensbeschikbaarheid omdat Adobe Experience Platform aan macht [ wordt gebouwd verpersoonlijkingsgebruiksgevallen in real time ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html)</li><li>Consolideer implementatie voor Adobe Experience Cloud-gegevensverzameling tussen andere Experience Cloud-producten (AJO, RTCDP, enzovoort)</li><li>Niet afhankelijk van de Adobe Analytics-nomenclatuur (zoals prop, eVar, event, enzovoort)</li></ul><li>**gebruikt uw bestaande implementatie**: Terwijl deze benadering sommige implementatieveranderingen vereist, vereist het geen volledig nieuwe implementatie van kras. U kunt de bestaande gegevenslaag en -code gebruiken met minimale wijzigingen in de implementatielogica zonder dat dit van invloed is op uw bestaande Adobe Analytics-rapportage.</li><li>**verstrekt een optie om een schema XDM** te gebruiken: U kunt verkiezen om uw bestaand schema van Adobe Analytics te gebruiken of een XDM schema en kaartgebieden in het gegevensvoorwerp tot stand te brengen aan uw schema XDM. [ XDM- schema&#39;s ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home#xdm-schemas) zijn een flexibel schema om het even welke gebieden te bepalen u, en slechts die gebieden nodig hebt die relevant zijn. <p>Zie &quot;Gebruikend uw eigen schema XDM&quot;hieronder voor meer informatie over de voordelen om uw eigen schema te gebruiken XDM.</p></li><li>**behoudt regels en gegevenselementen**: Terwijl het nieuwe regelacties vereist, kunt u uw bestaande gegevenselementen en regelvoorwaarden met minimale veranderingen opnieuw gebruiken.</li><li>**Toekomstbestendig**: Als u verkiest om uw eigen schema te gebruiken XDM, dan zijn de toekomstige implementatieupdates gemakkelijker.</li></ul> | <ul><li>**vereist afbeelding om gegevens naar Platform** te verzenden: Wanneer uw organisatie klaar is om Customer Journey Analytics te gebruiken, moet u gegevens naar een gegevensreeks in Adobe Experience Platform verzenden. Deze actie vereist dat elk gebied in het gegevensvoorwerp een ingang in het hulpmiddel van de gegevenstoewijzing is dat het aan een XDM schemagebied toewijst. Voor deze workflow hoeft u slechts één keer toewijzingen uit te voeren, en dit betekent niet dat u implementatiewijzigingen aanbrengt. Het is echter een extra stap die niet vereist is bij het verzenden van gegevens in een XDM-object.</li><li>**introduceert extra ingewikkeldheid in tijd**: Om het even welk gebied u in de toekomst toevoegt moet aan XDM in de gegevensstroom in kaart worden gebracht.<p>Telkens wanneer een nieuw veld aan uw implementatie wordt toegevoegd, kunt u een van de volgende handelingen uitvoeren:</p><ul><li>**Optie 1:** bevolkt een nieuwe willekeurige gebeurtenis of nieuwe steun in het gegevensvoorwerp, dan kaart het aan het gewenste gebied XDM.<p>Dit proces bevordert consistentie voor de cliënt-zijimplementatie, maar het vereist afbeelding.</p></li><li>**Optie 2:** verlaat het gegevensvoorwerp als erfenisimplementatie en begin slechts het voorwerp XDM voor alle nieuwe gebieden te bevolken.<p>Dit proces vereist geen toewijzing, maar het betekent dat sommige van uw variabelen slechts in een gegevensvoorwerp worden gevestigd, terwijl andere variabelen slechts in een voorwerp XDM worden gevestigd. Wanneer u uw implementatie moet problemen oplossen, moet u naar twee plaatsen gaan. Zorg ervoor dat uw interne workflows hiervoor geschikt zijn.</p></li></ul> |

{style="table-layout:auto"}

## Implementatiestappen

1. Gegevens verzenden van Edge Network naar Platform. Verzend al uw variabelen in AppMeasurement-indeling via het gegevensobject.

   Voor meer informatie, zie [ objecten van Gegevens veranderlijke afbeelding aan Adobe Analytics ](https://experienceleague.adobe.com/en/docs/analytics/implementation/aep-edge/data-var-mapping).

1. Kies uw schema.

   U kunt kiezen of u uw bestaande Adobe Analytics-schema wilt gebruiken, of u kunt een XDM-schema maken dat beter op de behoeften van uw organisatie wordt afgestemd wanneer u andere platformservices gaat gebruiken.

   Adobe raadt u aan een XDM-schema te maken. Voor meer informatie, zie [ een douaneschema tot stand brengen om met uw implementatie van SDK van het Web van Customer Journey Analytics ](/help/getting-started/cja-upgrade/cja-upgrade-schema-create.md) te gebruiken.

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

   Voor meer informatie, zie [ Afbeelding ](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/data-prep?lang=en#mapping) in [ Prep van Gegevens voor de Inzameling van Gegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/data-prep) in de documentatie van Experience Platform.

{{upgrade-final-step}}
