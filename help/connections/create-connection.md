---
title: Een verbinding maken
description: Beschrijft hoe te om een verbinding aan een dataset van het Platform in de Analyse van de Reis van de Klant tot stand te brengen.
translation-type: tm+mt
source-git-commit: 41029fb428308a247df65072af4e419a90098a15

---


# Een verbinding maken

Een verbinding laat u datasets van het Platform van de Ervaring van Adobe in Werkruimte integreren. om over de datasets van het Platform te rapporteren, moet u eerst een verbinding tussen datasets in Platform en Werkruimte vestigen.

Klik [hier](https://docs.adobe.com/content/help/en/platform-learn/tutorials/cja/connecting-customer-journey-analytics-to-data-sources-in-platform.html) voor een videooverzicht.

>[!IMPORTANT] U kunt de veelvoudige datasets van het Platform in één enkele verbinding combineren.

1. Ga naar [https://analytics.adobe.com](https://analytics.adobe.com).

1. Klik op het **[!UICONTROL Connections]** tabblad.

1. Klik **[!UICONTROL Create new connection]** op de rechterbovenhoek.

![Verbinding maken](assets/create-connection.png)

1. De linkerspoorstaaf toont alle datasets in Platform waaruit u kunt trekken. Selecteer één of meerdere datasets(en) die u in de analyse van de Reis van de Klant wilt ophalen en klik op **[!UICONTROL Add]**. (Als u een hoop datasets hebt waaruit te kiezen, kunt u zoeken naar de juiste, met behulp van de zoekbalk boven de lijst met gegevenssets.)

1. Daarna, voor elke dataset die u aan deze verbinding toevoegde, plaatst de Analyse van de Reis van de Klant automatisch het datasettype dat op de gegevens wordt gebaseerd die binnen komen. Er zijn 3 verschillende datasettypes: De gegevens van de gebeurtenis, de gegevens van het Profiel, en de gegevens van de Raadpleging.

   | Type gegevensset | Beschrijving | Tijdstempel | Schema | Persoon-id |
   |---|---|---|---|---|
   | Gebeurtenis | Gegevens die gebeurtenissen in de tijd vertegenwoordigen (bv. Webbezoeken, interacties, transacties, POS-gegevens, enquêtegegevens, en peilgegevens, enz.). Dit is typische klikstroomgegevens, met een klantenidentiteitskaart of een koekjesidentiteitskaart, en timestamp. Met de gegevens van de Gebeurtenis, staan wij u toe om het even welke identiteitskaart te gebruiken u wilt. | Wordt ingesteld op Timestamp. | Het schema van het Platform dat dit datasettype is gebaseerd op. | N.v.t. |
   | Opzoeken | analoog aan een dossier van Classificaties. Dit gegeven wordt gebruikt aan raadplegingswaarden of sleutels die in uw Gebeurtenis of gegevens van het Profiel worden gevonden. Bijvoorbeeld, zou u raadplegingsgegevens kunnen uploaden die numerieke IDs in uw gebeurtenisgegevens aan productnamen in kaart brengen. | N.v.t. | Het schema van het Platform dat dit datasettype is gebaseerd op. | N.v.t. |
   | Profiel | Analogie op Eigenschappen van de Klant - voor niet-veranderende en niet-temporele attributen. Gegevens die op uw bezoekers, gebruikers, of klanten in de gegevens van de Gebeurtenis worden toegepast. Bijvoorbeeld, staat u toe om de gegevens van CRM over uw klanten te uploaden. | N.v.t. | Het schema van het Platform dat dit datasettype is gebaseerd op. | Je kunt kiezen welke persoon-ID je wilt opnemen. Elke dataset die in het Platform van de Ervaring van Adobe wordt bepaald heeft zijn eigen reeks van één of meerdere bepaalde Identiteitskaart van de Persoon, zoals identiteitskaart van het Koekje, Geplaatste identiteitskaart, Gebruiker - identiteitskaart, het Volgen Code, enz.<br>![Persoon](assets/person-id.png)**IDNote **: Als u een verbinding creeert die datasets met verschillende IDs omvat, zal het melden op dat wijzen. Om datasets echt samen te voegen, moet u de zelfde identiteitskaart van de Persoon gebruiken. |

1. Klik op **[!UICONTROL Next]**.

1. In de Create dialoog van de Verbinding, bepaal deze montages:

   | Veld | Beschrijving |
   |---|---|
   | Naam | Geef de verbinding een beschrijvende naam. De verbinding kan niet zonder een naam worden bewaard. |
   | Beschrijving | Voeg meer detail toe om deze verbinding van anderen te onderscheiden. |
   | Grootte | De collectieve grootte van de datasets in de gegevensverbinding. |
   | Datasets | De datasets die in deze verbinding inbegrepen zijn. |
   | Gegevensstreaming | Om te beginnen stromend gegevens voor deze verbinding, laat gegevens het stromen toe. Wanneer gegevens het stromen voor deze verbinding wordt toegelaten, wordt uw rekening gefactureerd voor de hoeveelheid gegevens die deze verbinding stroomt. (Merk op dat u gegevens ook kunt toelaten die in de Manager van Verbindingen stromen.) |

1. Klik op **[!UICONTROL Save]**. Wanneer u deze verbinding bewaart, gebeuren twee dingen:

   * U trekt in alle historische gegevens van Platform voor alle datasets die in deze verbinding zijn.
   * Als u het stromen toeliet, vestigt u een aan de gang zijnde verbinding, zodat om het even welke nieuwe gegevens die aan de datasets in deze verbinding worden toegevoegd automatisch in Werkruimte stromen.

De volgende stap in het werkschema moet een gegevensmening [tot stand brengen](/help/data-views/create-dataview.md).
