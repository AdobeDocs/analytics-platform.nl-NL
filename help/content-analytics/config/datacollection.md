---
title: Content Analytics-gegevensverzameling
description: Een overzicht van hoe gegevens in Content Analytics worden verzameld
solution: Customer Journey Analytics
feature: Content Analytics
role: Admin
exl-id: 584587e6-45fd-4fc3-a7a6-6685481ddee7
source-git-commit: feb253b20820112d5aa4b4eee31cff74d99fa186
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 0%

---

# Content Analytics-gegevensverzameling

{{release-limited-testing}}

In dit artikel wordt gedetailleerd uitgelegd hoe Content Analytics gegevens verzamelt


## Definities

In het kader van dit artikel worden de volgende definities gebruikt:

* **Ervaring**: Een ervaring wordt bepaald als tekstinhoud op een volledige Web-pagina. Voor gegevensverzameling registreert Content Analytics de ervaring-id die is gebaseerd op de pagina-URL. Later wordt de tekst op de pagina vastgelegd via de ophaalservice.
* **identiteitskaart van de Ervaring**: Een unieke combinatie relevante URL (basis URL plus om het even welke parameters die inhoud op de pagina drijven) en [ ervaringsversie ](manual.md#versioning).
   * U specificeert, als deel van de [ configuratie ](configuration.md), welke parameters voor om het even welke bepaalde volledige URL relevant zijn.
   * U bepaalt het herkenningsteken van de a [ versie ](manual.md#versioning) aan gebruik, zodat verzamelt u behoorlijk veranderingen in uw ervaringen.
* **Activa**: Een beeld. Content Analytics registreert de URL van het element.
* **identiteitskaart van Activa**: URL van de activa.
* **Relevante URL**: De basis URL plus om het even welke parameters die inhoud op de pagina drijven.


## Functionaliteit

Content Analytics vereist de Experience Platform Edge Network Web SDK om gebeurtenisgegevens over inhoud te verzamelen. Die verzameling van gebeurtenisgegevens wordt gecombineerd met de (bestaande) gegevensverzameling van gedragsgebeurtenisgegevens via mechanismen zoals Experience Platform Edge Network (Web SDK, Server API) of de bronconnector van Analytics (bijvoorbeeld met AppMeasurement).

De Content Analytics-bibliotheek verzamelt gegevens wanneer:

* Content Analytics is opgenomen in de tagbibliotheek die op de pagina is geladen.
* De pagina URL wordt gevormd in de [ uitbreiding van Content Analytics ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/content-analytics/overview){target="_blank"}, een deel van de inbegrepen bibliotheek van Markeringen.



## Content Analytics, gebeurtenis

Een Content Analytics-gebeurtenis bestaat uit:

* Standaardvelden
   * Tijdstempel
   * Identiteit
* De meningen van de ervaring (als om het even welk, en als gevormd)
* De ervaring klikt (als om het even welk, en als gevormd)
* Elementweergaven (indien aanwezig en indien geconfigureerd)
* Elementklikken (indien aanwezig en indien geconfigureerd)


Content Analytics-gebeurtenissen worden verzameld als een reeks van:

1. [ A geregistreerde mening of klik ](#recorded-view-or-click).
1. [ een regelmatige of specifieke (gedrags) gebeurtenis ](#regular-or-specific-behaviorial-event).

Content Analytics verzamelt gegevens op deze manier om die reeks te weerspiegelen in plaats van een weergave te verzamelen of klik apart van het verzamelen van de gebeurtenis direct na die weergave of klik. Op deze manier wordt ook de hoeveelheid verzamelde gegevens verminderd.

### Opgenomen weergave of klik

Een elementweergave wordt opgenomen wanneer:

* Het middel is niet uitgesloten volgens de Content Analytics-extensieconfiguratie.
* De waarde van de activa is 75%.
* Dit element is nog niet opgenomen voor deze pagina.

Een elementklik wordt opgenomen wanneer:

* Het element is weergegeven.
* Het middel is niet uitgesloten volgens de Content Analytics-extensieconfiguratie.
* Klik rechtstreeks op het element (een koppeling) dat naar een andere pagina leidt.

Er wordt een ervaringsweergave opgenomen wanneer:

* Ervaringen zijn ingeschakeld in de Content Analytics-configuratie.

Er wordt een ervaringsklik opgenomen wanneer:

* Elke klik vindt plaats op een koppeling op de pagina waarvoor ervaringen zijn ingeschakeld.


### Gewone of specifieke (gedrags)gebeurtenis

Triggers om een reguliere of specifieke (gedrags)gebeurtenis te starten in de context van Content Analytics zijn:

* Web SDK of AppMettings verzendt een gebeurtenis.
* De zichtbaarheid verandert in verborgen, bijvoorbeeld:
   * Pagina wordt verwijderd
   * Tabblad Overschakelen
   * Browser minimaliseren
   * Browser sluiten
   * Scherm vergrendelen
* De URL verandert, wat resulteert in een gewijzigde relevante URL.
* De geregistreerde en klaar om te worden verzonden meningen van activa overschrijden het aantal van 32.


## Schema&#39;s

Content Analytics-gegevens worden verzameld in datasets in Experience Platform, op basis van specifieke Content Analytics-schema&#39;s. Referentieschema&#39;s zijn openbaar:

* [ Digitaal schema van Activa ](https://github.com/adobe/xdm/blob/master/components/classes/digital-asset.schema.json)
* [ Digitaal schema van de Ervaring ](https://github.com/adobe/xdm/blob/master/components/classes/digital-experience.schema.json)
* [ schema van de Inhoud van de Gebeurtenis van de Ervaring ](https://github.com/adobe/xdm/blob/master/components/fieldgroups/experience-event/experienceevent-content.schema.json)
