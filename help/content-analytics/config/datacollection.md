---
title: Content Analytics-gegevensverzameling
description: Een overzicht van hoe gegevens in Content Analytics worden verzameld
solution: Customer Journey Analytics
feature: Content Analytics
hide: true
hidefromtoc: true
role: Admin
source-git-commit: d835411beba3d40f67d2f93ee76aa5eda6f45041
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---


# Content Analytics-gegevensverzameling

In dit artikel wordt gedetailleerd uitgelegd hoe content Analytics gegevens verzamelt


## Definities

In het kader van dit artikel worden de volgende definities gebruikt:

* **Ervaring**: Een ervaring wordt bepaald als tekstinhoud op een volledige Web-pagina. Voor gegevensverzameling registreert Content Analytics de ervaring-id. Content Analytics neemt de tekst niet op de pagina op.
* **Activa**: Een beeld. Content Analytics registreert de URL van het element.
* **Relevante URL**: De basis URL plus om het even welke parameters die inhoud op de pagina drijven.
* **identiteitskaart van de Ervaring**: Een unieke combinatie relevante URL en ervaringsversie.
   * U specificeert, als deel van de [ configuratie ](configuration.md), welke parameters voor om het even welke bepaalde volledige URL relevant zijn.
   * U kunt het [ versieherkenningsteken ](manual.md#versioning) bepalen dat wordt gebruikt. Voor gegevensverzameling wordt de versie niet in overweging genomen. Alleen de relevante URL wordt verzameld.

## Functionaliteit

De Content Analytics-bibliotheek verzamelt gegevens wanneer:

* Content Analytics is opgenomen in de tagbibliotheek die op de pagina is geladen.
* De pagina URL wordt gevormd in de [ uitbreiding van Content Analytics ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview) {target="_blank"}, deel van de inbegrepen bibliotheek van Markeringen.


### Content Analytics, gebeurtenis

Een Content Analytics-gebeurtenis bestaat uit:

* Standaardvelden
   * Tijdstempel
   * Identiteit
* De meningen van de ervaring (als om het even welk, en als gevormd)
* De ervaring klikt (als om het even welk, en als gevormd)
* Elementweergaven (indien aanwezig en indien geconfigureerd)
* Elementklikken (indien aanwezig en indien geconfigureerd)

#### Opgenomen weergaven of klikken

Een elementweergave wordt opgenomen wanneer:

* Het middel is niet uitgesloten volgens de ACA-extensieconfiguratie.
* De waarde van de activa is 75%.
* Dit element is nog niet opgenomen voor deze pagina.

Een elementklik wordt opgenomen wanneer:

* Het element is weergegeven.
* Het middel is niet uitgesloten volgens de ACA-extensieconfiguratie.
* Klik rechtstreeks op het element (een koppeling) dat naar een andere pagina leidt.

Er wordt een ervaringsweergave opgenomen wanneer:

* Ervaringen zijn ingeschakeld in de Content Analytics-configuratie.

Er wordt een ervaringsklik opgenomen wanneer:

* Elke klik vindt plaats op een koppeling op de pagina waarvoor ervaringen zijn ingeschakeld.


#### Verzonden gebeurtenissen

Content Analytics-gebeurtenissen worden verzonden wanneer aan de volgende twee voorwaarden wordt voldaan:

* Inhoud wordt verzonden, wat optreedt wanneer:

   * Een elementweergave of klik wordt opgenomen.
   * Er wordt een ervaringsweergave of een klik opgenomen.

* Een trigger voor het verzenden van een gebeurtenis wordt geactiveerd, wat optreedt wanneer:

   * Web SDK of AppMettings verzendt een gebeurtenis.
   * De zichtbaarheid verandert in verborgen, bijvoorbeeld:
      * Pagina wordt verwijderd
      * Tabblad Overschakelen
      * Browser minimaliseren
      * Browser sluiten
      * Scherm vergrendelen
   * De URL verandert, wat resulteert in een gewijzigde relevante URL.
   * Een elementweergave overschrijdt de batchlimiet van 32.


## Schema&#39;s

Content Analytics-gegevens worden verzameld in datasets in Experience Platform, op basis van specifieke Content Analytics-schema&#39;s. Referentieschema&#39;s zijn openbaar en worden gebruikt in een standaardimplementatie van Content Analytics.

* [ Digitaal schema van Activa ](https://github.com/adobe/xdm/blob/master/components/classes/digital-asset.schema.json)
* [ Digitaal schema van de Ervaring ](https://github.com/adobe/xdm/blob/master/components/classes/digital-experience.schema.json)
* [ schema van de Inhoud van de Gebeurtenis van de Ervaring ](https://github.com/adobe/xdm/blob/master/components/fieldgroups/experience-event/experienceevent-content.schema.json)
