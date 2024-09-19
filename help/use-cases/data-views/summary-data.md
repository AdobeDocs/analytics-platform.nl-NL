---
title: Samenvattingsgegevens gebruiken in Customer Journey Analytics
description: Uitleg van alle details over hoe u summiere gegevens in Customer Journey Analytics kunt brengen
solution: Customer Journey Analytics
feature: Use Cases
role: Admin
exl-id: 80139806-618a-46ff-b2c4-32d7bb85a526
source-git-commit: e6f57b03689bd9aaaec12c13fc95da5b079b901e
workflow-type: tm+mt
source-wordcount: '4609'
ht-degree: 7%

---

# Samenvattingsgegevens gebruiken

Dit is handig als u wilt weten hoe u overzichtsgegevens kunt gebruiken in uw rapportage en analyse. Het gebruiksgeval detailleert alle stappen die worden vereist om summiere gegevens in Customer Journey Analytics te gebruiken:

- [ Samenvatting ](#ingest) gegevens en andere gegevensbronnen in Experience Platform.
- Opstelling uw [ Verbinding ](#connection) voor de summiere gegevens en andere gegevensbronnen.
- Vorm uw [ mening van Gegevens ](#data-view) om uw gegevensbronnen te combineren.
- Rapport en analyseer in [ Workspace ](#workspace) op uw gecombineerde gegevens.

Het gebruiksgeval verstrekt steekproefgegevens voor summiere gegevens, gebeurtenisgegevens en raadplegingsgegevens. Alle gegevens bevatten willekeurige waarden.

## Ingest

U gebruikt de volgende voorbeeldsummiere gegevens voor dit gebruiksgeval, tonend summiere gegevens voor lopende campagnes op Facebook.

+++Samenvattingsgegevens

| _id | campagne_naam | kosten | indruk | campagne_id | netwerk | ad_group | tijdstempel |
|---|---|---:|---:|---|---|---|---|
| 1 | 123 Campagne | 100 | 5000 | abc123 | facebook | abc-adgroup | 2024-07-18T18 :20: 39.000Z |
| 2 | 123 Campagne | 50 | 4000 | def123 | facebook | def-adgroup | 2024-07-18T18 :20: 39.000Z |
| 3 | 123 Campagne | 125 | 6000 | ghi123 | facebook | ghi-adgroup | 2024-07-18T18 :20: 39.000Z |
| 4 | 456 Campagne | 25 | 2500 | abc456 | facebook | abc-adgroup | 2024-07-18T18 :20: 39.000Z |
| 5 | 456 Campagne | 10 | 1000 | def456 | facebook | def-adgroup | 2024-07-18T18 :20: 39.000Z |
| 6 | 456 Campagne | 115 | 5500 | ghi456 | facebook | ghi-adgroup | 2024-07-18T18 :20: 39.000Z |
| 7 | 789 Campagne | 200 | 9000 | abc789 | facebook | abc-adgroup | 2024-07-18T18 :20: 39.000Z |
| 8 | 789 Campagne | 20 | 2000 | def789 | facebook | def-adgroup | 2024-07-18T18 :20: 39.000Z |
| 9 | 789 Campagne | 225 | 12000 | ghi789 | facebook | ghi-adgroup | 2024-07-18T18 :20: 39.000Z |
| 10 | 987 Campagne | 125 | 10000 | abc987 | facebook | abc-adgroup | 2024-07-18T18 :20: 39.000Z |
| 11 | 987 Campagne | 120 | 15000 | def987 | facebook | def-adgroup | 2024-07-18T18 :20: 39.000Z |
| 12 | 987 Campagne | 315 | 22500 | ghi987 | facebook | ghi-adgroup | 2024-07-18T18 :20: 39.000Z |
| 13 | 654 Campagne | 325 | 20000 | abc654 | facebook | abc-adgroup | 2024-07-18T18 :20: 39.000Z |
| 14 | 654 Campagne | 320 | 25000 | def654 | facebook | def-adgroup | 2024-07-18T18 :20: 39.000Z |
| 15 | 654 Campagne | 315 | 22500 | ghi654 | facebook | ghi-adgroup | 2024-07-18T18 :20: 39.000Z |
| 16 | 321 Campagne | 25 | 2000 | abc321 | facebook | abc-adgroup | 2024-07-18T18 :20: 39.000Z |
| 17 | 321 Campagne | 20 | 2500 | def321 | facebook | def-adgroup | 2024-07-18T18 :20: 39.000Z |
| 18 | 321 Campagne | 15 | 2250 | ghi321 | facebook | ghi-adgroup | 2024-07-18T18 :20: 39.000Z |

[![DataDownload](/help/assets/icons/DataDownload.svg)](./assets/summary-data.csv)

+++

Als u de samenvattingsgegevens wilt gebruiken in Customer Journey Analytics, in een rapport of als onderdeel van het analyseren van gegevens in Workspace, hebt u

- een samenvattingsschema in Experience Platform,
- een samenvattende dataset in Experience Platform,
- een verbinding in Customer Journey Analytics die wordt gevormd om de summiere dataset te gebruiken,
- een gegevensmening in Customer Journey Analytics, correct gevormd met metriek en dimensies voor de summiere gegevens.

U gebruikt deze samenvattingsgegevens naast een dataset voor gebeurtenisgegevens en een dataset voor raadplegingsgegevens.

+++Gebeurtenisgegevens

Gebeurtenisgegevens zijn beschikbaar in de Gegevensset voorbeeldgebeurtenisgegevens. De voorbeeldgegevens zien er als volgt uit:

| tijdstempel | _id | page_name | person_id | tracking_code | orders | opbrengst_bedrag |
|---|---:|---|---|---|---:|---:|
| 2024-07-18T19 :15: 39+00:00 | 1 | homepage | person-1abc123 | abc123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 2 | bevestigingspagina | person-1abc123 |  | 1 | 174,25 |
| 2024-07-18T19 :15: 39+00:00 | 3 | homepage | person-2def123 | def123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 4 | homepage | person-3ghi123 | ghi123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 5 | bevestigingspagina | person-3ghi123 |  | 1 | 149,25 |
| 2024-07-18T19 :15: 39+00:00 | 6 | homepage | person-4abc456 | abc456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 7 | homepage | person-5def456 | def456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 8 | homepage | person-6ghi456 | ghi456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 9 | bevestigingspagina | person-6ghi456 |  | 1 | 159,25 |
| 2024-07-18T19 :15: 39+00:00 | 10 | homepage | person-7abc789 | abc789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 11 | homepage | person-8def789 | def789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 12 | homepage | person-9ghi789 | ghi789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 13 | bevestigingspagina | person-9ghi789 |  | 1 | 124,25 |
| 2024-07-18T19 :15: 39+00:00 | 14 | homepage | person-10abc987 | abc987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 15 | homepage | person-11def987 | def987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 16 | homepage | person-12ghi987 | ghi987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 17 | homepage | person-13abc654 | abc654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 18 | homepage | person-14def654 | def654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 19 | homepage | person-15ghi654 | ghi654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 20 | bevestigingspagina | person-15ghi654 |  | 1 | 174,25 |
| 2024-07-18T19 :15: 39+00:00 | 21 | homepage | person-16abc321 | abc321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 22 | homepage | person-17def321 | def321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 23 | homepage | person-18ghi321 | ghi321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 24 | homepage | person-19abc123 | abc123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 25 | homepage | person-20def123 | def123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 26 | homepage | person-21ghi123 | ghi123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 27 | bevestigingspagina | person-21ghi123 |  | 1 | 149,25 |
| 2024-07-18T19 :15: 39+00:00 | 28 | homepage | person-22abc456 | abc456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 29 | homepage | person-23def456 | def456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 30 | homepage | person-24ghi456 | ghi456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 31 | homepage | person-25abc789 | abc789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 32 | bevestigingspagina | person-25abc789 |  | 1 | 139,25 |
| 2024-07-18T19 :15: 39+00:00 | 33 | homepage | person-26abc987 | abc987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 34 | homepage | person-27def987 | def987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 35 | homepage | person-28ghi987 | ghi987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 36 | homepage | person-29abc654 | abc654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 37 | bevestigingspagina | person-29abc654 |  | 1 | 124,25 |
| 2024-07-18T19 :15: 39+00:00 | 38 | homepage | person-30def654 | def654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 39 | homepage | person-31ghi654 | ghi654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 40 | homepage | person-32abc321 | abc321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 41 | homepage | person-33ghi456 | ghi456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 42 | bevestigingspagina | person-33ghi456 |  | 1 | 174,25 |
| 2024-07-18T19 :15: 39+00:00 | 43 | homepage | person-34abc789 | abc789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 44 | homepage | person-35def789 | def789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 45 | homepage | person-36ghi789 | ghi789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 46 | bevestigingspagina | person-36ghi789 |  | 1 | 149,25 |
| 2024-07-18T19 :15: 39+00:00 | 47 | homepage | person-37abc987 | abc987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 48 | homepage | person-38def987 | def987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 49 | homepage | person-39ghi987 | ghi987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 50 | homepage | person-40abc654 | abc654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 51 | bevestigingspagina | person-40abc654 |  | 1 | 124,25 |
| 2024-07-18T19 :15: 39+00:00 | 52 | homepage | person-41def654 | def654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 53 | homepage | person-42ghi654 | ghi654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 54 | homepage | person-43abc321 | abc321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 55 | homepage | person-44def321 | def321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 56 | homepage | person-45ghi321 | ghi321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 57 | homepage | person-46abc123 | abc123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 58 | bevestigingspagina | person-46abc123 |  | 1 | 174,25 |
| 2024-07-18T19 :15: 39+00:00 | 59 | homepage | person-47def123 | def123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 60 | homepage | person-48ghi123 | ghi123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 61 | homepage | person-49abc456 | abc456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 62 | homepage | person-50def456 | def456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 63 | homepage | person-51ghi456 | ghi456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 64 | homepage | person-52abc789 | abc789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 65 | bevestigingspagina | person-52abc789 |  | 1 | 149,25 |
| 2024-07-18T19 :15: 39+00:00 | 66 | homepage | person-53abc987 | abc987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 67 | homepage | person-54def987 | def987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 68 | homepage | person-55ghi987 | ghi987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 69 | bevestigingspagina | person-55ghi987 |  | 1 | 124,25 |
| 2024-07-18T19 :15: 39+00:00 | 70 | homepage | person-56abc123 | abc123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 71 | homepage | person-57def123 | def123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 72 | bevestigingspagina | person-57def123 |  | 1 | 174,25 |
| 2024-07-18T19 :15: 39+00:00 | 73 | homepage | person-58ghi123 | ghi123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 74 | homepage | person-59abc456 | abc456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 75 | bevestigingspagina | person-59abc456 |  | 1 | 149,25 |
| 2024-07-18T19 :15: 39+00:00 | 76 | homepage | person-60def456 | def456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 77 | homepage | person-61ghi456 | ghi456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 78 | homepage | person-62abc789 | abc789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 79 | bevestigingspagina | person-62abc789 |  | 1 | 159,25 |
| 2024-07-18T19 :15: 39+00:00 | 80 | homepage | person-63def789 | def789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 81 | homepage | person-64ghi789 | ghi789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 82 | homepage | person-65abc987 | abc987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 83 | bevestigingspagina | person-65abc987 |  | 1 | 124,25 |
| 2024-07-18T19 :15: 39+00:00 | 84 | homepage | person-66def987 | def987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 85 | homepage | person-67ghi987 | ghi987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 86 | homepage | person-68abc654 | abc654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 87 | homepage | person-69def654 | def654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 88 | homepage | person-70ghi654 | ghi654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 89 | homepage | person-71abc321 | abc321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 90 | bevestigingspagina | person-71abc321 |  | 1 | 174,25 |
| 2024-07-18T19 :15: 39+00:00 | 91 | homepage | person-72def321 | def321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 92 | homepage | person-73ghi321 | ghi321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 93 | homepage | person-74abc123 | abc123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 94 | homepage | person-75def123 | def123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 95 | homepage | person-76ghi123 | ghi123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 96 | homepage | person-77abc456 | abc456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 97 | bevestigingspagina | person-77abc456 |  | 1 | 149,25 |
| 2024-07-18T19 :15: 39+00:00 | 98 | homepage | person-78def456 | def456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 99 | homepage | person-79ghi456 | ghi456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 100 | homepage | person-80abc789 | abc789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 101 | homepage | person-81abc987 | abc987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 102 | bevestigingspagina | person-81abc987 |  | 1 | 139,25 |
| 2024-07-18T19 :15: 39+00:00 | 103 | homepage | person-82def987 | def987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 104 | homepage | person-83ghi987 | ghi987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 105 | homepage | person-84abc654 | abc654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 106 | homepage | person-85def654 | def654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 107 | bevestigingspagina | person-85def654 |  | 1 | 124,25 |
| 2024-07-18T19 :15: 39+00:00 | 108 | homepage | person-86ghi654 | ghi654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 109 | homepage | person-87abc321 | abc321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 110 | homepage | person-88ghi456 | ghi456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 111 | homepage | person-89abc789 | abc789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 112 | bevestigingspagina | person-89abc789 |  | 1 | 174,25 |
| 2024-07-18T19 :15: 39+00:00 | 113 | homepage | person-90def789 | def789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 114 | homepage | person-91ghi789 | ghi789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 115 | homepage | person-92abc987 | abc987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 116 | bevestigingspagina | person-92abc987 |  | 1 | 149,25 |
| 2024-07-18T19 :15: 39+00:00 | 117 | homepage | person-93def987 | def987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 118 | homepage | person-94ghi987 | ghi987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 119 | homepage | person-95abc654 | abc654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 120 | homepage | person-96def654 | def654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 121 | bevestigingspagina | person-96def654 |  | 1 | 124,25 |
| 2024-07-18T19 :15: 39+00:00 | 122 | homepage | person-97ghi654 | ghi654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 123 | homepage | person-98abc321 | abc321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 124 | homepage | person-99def321 | def321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 125 | homepage | person-100ghi321 | ghi321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 126 | homepage | person-101abc123 | abc123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 127 | homepage | person-102def123 | def123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 128 | bevestigingspagina | person-102def123 |  | 1 | 174,25 |
| 2024-07-18T19 :15: 39+00:00 | 129 | homepage | person-103ghi123 | ghi123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 130 | homepage | person-104abc456 | abc456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 131 | homepage | person-105def456 | def456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 132 | homepage | person-106ghi456 | ghi456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 133 | homepage | person-107abc789 | abc789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 134 | homepage | person-108abc987 | abc987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 135 | bevestigingspagina | person-108abc987 |  | 1 | 149,25 |
| 2024-07-18T19 :15: 39+00:00 | 136 | homepage | person-109def987 | def987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 137 | homepage | person-110ghi987 | ghi987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 138 | bevestigingspagina | person-110ghi987 |  |  |  |
| 2024-07-18T19 :15: 39+00:00 | 139 | homepage | person-111def987 | def987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 140 | homepage | person-112def987 |  | 1 | 124,25 |
| 2024-07-18T19 :15: 39+00:00 | 141 | bevestigingspagina | person-112def987 |  | 1 | 149,25 |
| 2024-07-18T19 :15: 39+00:00 | 142 | homepage | person-113ghi987 | ghi987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 143 | homepage | person-114abc654 | abc654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 144 | homepage | person-115def654 | def654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 145 | bevestigingspagina | person-115def654 |  | 1 | 159,25 |
| 2024-07-18T19 :15: 39+00:00 | 146 | homepage | person-116ghi654 | ghi654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 147 | homepage | person-117abc321 | abc321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 148 | homepage | person-118def321 | def321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 149 | bevestigingspagina | person-118def321 |  | 1 | 124,25 |
| 2024-07-18T19 :15: 39+00:00 | 150 | homepage | person-119ghi321 | ghi321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 151 | homepage | person-120abc123 | abc123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 152 | homepage | person-121def123 | def123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 153 | homepage | person-122ghi123 | ghi123 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 154 | homepage | person-123abc456 | abc456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 155 | homepage | person-124def456 | def456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 156 | bevestigingspagina | person-124def456 |  | 1 | 174,25 |
| 2024-07-18T19 :15: 39+00:00 | 157 | homepage | person-125ghi456 | ghi456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 158 | homepage | person-126abc789 | abc789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 159 | homepage | person-127abc987 | abc987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 160 | homepage | person-128def987 | def987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 161 | homepage | person-129ghi987 | ghi987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 162 | homepage | person-130abc654 | abc654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 163 | bevestigingspagina | person-130abc654 |  | 1 | 149,25 |
| 2024-07-18T19 :15: 39+00:00 | 164 | homepage | person-131def654 | def654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 165 | homepage | person-132ghi654 | ghi654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 166 | homepage | person-133abc321 | abc321 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 167 | homepage | person-134ghi456 | ghi456 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 168 | bevestigingspagina | person-134ghi456 |  | 1 | 139,25 |
| 2024-07-18T19 :15: 39+00:00 | 169 | homepage | person-135abc789 | abc789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 170 | homepage | person-136def789 | def789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 171 | homepage | person-137ghi789 | ghi789 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 172 | homepage | person-138abc987 | abc987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 173 | bevestigingspagina | person-138abc987 |  | 1 | 124,25 |
| 2024-07-18T19 :15: 39+00:00 | 174 | homepage | person-139def987 | def987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 175 | homepage | person-140ghi987 | ghi987 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 176 | homepage | person-141abc654 | abc654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 177 | homepage | person-142def654 | def654 |  |  |
| 2024-07-18T19 :15: 39+00:00 | 178 | bevestigingspagina | person-142def654 |  | 1 | 174,25 |
| 2024-07-18T19 :15: 39+00:00 | 179 | homepage | person-143ghi654 | ghi654 |  |  |

[![DataDownload](/help/assets/icons/DataDownload.svg)](./assets/event-data.csv)

+++

+++ Gegevens opzoeken

De gegevens van de opzoekopdracht zijn beschikbaar in de Dataset van de Gegevens van de Opzoekmachine van het Voorbeeld. De voorbeeldgegevens zien er als volgt uit:

| _id | tracking_code | ad_group | campagne_naam |
|---|---|---|---|
| 1 | abc123 | abc-adgroup | 123 Campagne |
| 2 | def123 | def-adgroup | 123 Campagne |
| 3 | ghi123 | ghi-adgroup | 123 Campagne |
| 4 | abc456 | abc-adgroup | 456 Campagne |
| 5 | def456 | def-adgroup | 456 Campagne |
| 6 | ghi456 | ghi-adgroup | 456 Campagne |
| 7 | abc789 | abc-adgroup | 789 Campagne |
| 8 | def789 | def-adgroup | 789 Campagne |
| 9 | ghi789 | ghi-adgroup | 789 Campagne |
| 10 | abc987 | abc-adgroup | 987 Campagne |
| 11 | def987 | def-adgroup | 987 Campagne |
| 12 | ghi987 | ghi-adgroup | 987 Campagne |
| 13 | abc654 | abc-adgroup | 654 Campagne |
| 14 | def654 | def-adgroup | 654 Campagne |
| 15 | ghi654 | ghi-adgroup | 654 Campagne |
| 16 | abc321 | abc-adgroup | 321 Campagne |
| 17 | def321 | def-adgroup | 321 Campagne |
| 18 | ghi321 | ghi-adgroup | 321 Campagne |

[![ DataDownload ](/help/assets/icons/DataDownload.svg) gegevens van de de steekproefraadpleging van de Download {](./assets/lookup-data.csv)
+++

>[!INFO]
>
>Verdere details voor opstellingsschema&#39;s en datasets voor de gebeurtenis en raadplegingsgegevens worden niet verstrekt. Deze opstelling wordt verondersteld gemeenschappelijke kennis en volgt de zelfde stappen zoals voor de raadplegingsgegevens.
>


### Samenvattingsschema

Voor samenvattingsgegevens is een samenvattingsschema in Experience Platform vereist. Een samenvattingsschema is een schema dat de XDM Summary Metrics als basisklasse gebruikt.

Een overzichtsschema maken in Experience Platform:

1. Selecteer **[!UICONTROL Experience Platform]** in het menu   ![ app ](/help/assets/icons/Apps.svg)   app-switch.
1. Selecteer **[!UICONTROL Schemas]** in het linkerspoor.
1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create schema]**.
1. Selecteer **[!UICONTROL Manual]** in het dialoogvenster **[!UICONTROL Create a schema]** . Gebruik vervolgens **[!UICONTROL Select]** om door te gaan.
1. Selecteer in de stap **[!UICONTROL Select a class]** van de wizard **[!UICONTROL Schemas]** > **[!UICONTROL Create schema]** de optie **[!UICONTROL Other]** bij de opties **[!UICONTROL Select a base class for this schema]** .
1. Van de lijst, selecteer **[!UICONTROL XDM Summary Metrics]** (of gebruik ![ Onderzoek ](/help/assets/icons/Search.svg) gebied om te zoeken) en selecteer **[!UICONTROL Next]**.
1. Voer in de stap **[!UICONTROL Name and review]** van de wizard **[!UICONTROL Schemas]** > **[!UICONTROL Create schema]** een **[!UICONTROL Schema display name]** voorbeeld `Example Summary Data Schema` en een optionele beschrijving in. Selecteer **[!UICONTROL Finish]** om deze stap te voltooien.

De structuur van het basissamenvattingsschema wordt weergegeven en kan worden aangevuld met de velden voor uw samenvattingsgegevens. U voegt velden aan een schema toe met behulp van veldgroepen.

U voegt als volgt een veldgroep met de velden voor de voorbeeldgegevens toe:

1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add]** in **[!UICONTROL Field groups]**.
1. Selecteer **[!UICONTROL Create new field group]** in het dialoogvenster **[!UICONTROL Add field groups]** .
1. Voer een **[!UICONTROL Display name]** in voor de veldgroep, bijvoorbeeld `Example Summary Data` . Geef desgewenst een beschrijving op.
1. Selecteer **[!UICONTROL Add field groups]** .
1. U bent terug in het gebruikersinterface van de schemastructuur. Selecteer de nieuwe **[!UICONTROL Example Summary Data]** in **[!UICONTROL Field groups]** .
1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) naast de schemanaam **[!UICONTROL Example summary Data Schema]**. Er wordt een deelvenster **[!UICONTROL Field properties]** geopend waarin u details voor een veld kunt toevoegen.
   1. Voer een **[!UICONTROL Field name]** in: `campaign_id`
   1. Voer een **[!UICONTROL Display name]** in: `campaign_id`
   1. Selecteer een **[!UICONTROL Type]** in de vervolgkeuzelijst **[!UICONTROL Select data type]** : **[!UICONTROL String]**
   1. Controleer of **[!UICONTROL Assign to]** **[!UICONTROL Field group]** is geselecteerd en selecteer **[!UICONTROL Example Summary Data]** in het vervolgkeuzemenu.
   1. Blader omlaag naar de onderkant en selecteer **[!UICONTROL Apply]** .
1. Herhaal de vorige stap voor de andere velden van de samenvattingsgegevens. Zie de onderstaande tabel voor de juiste waarden.

   | Veldnaam | Weergavenaam | Type | Veldgroep |
   |---|---|---|---|
   | `ad_group` | `ad_group` | String | Voorbeeldsamenvattingsgegevens |
   | `campaign_name` | `campaign_name` | String | Voorbeeldsamenvattingsgegevens |
   | `cost` | `cost` | Dubbel | Voorbeeldsamenvattingsgegevens |
   | `impression` | `impression` | Geheel | Voorbeeldsamenvattingsgegevens |
   | `network` | `network` | String | Voorbeeldsamenvattingsgegevens |

1. Als u de **[!UICONTROL Example Summary Data]** -veldgroep wilt opslaan als onderdeel van uw schema, selecteert u **[!UICONTROL Save]** . U ziet een bevestiging wanneer uw schema met succes wordt bewaard.

U hebt nu een schema gedefinieerd waarin het model voor uw samenvattingsgegevens wordt weergegeven. Gelijkaardig aan hieronder.

![ Schema van de Gegevens van het Voorbeeld Summiere ](../assets/example-summary-schema.png)





### Samenvattingsgegevensset

Om uw summiere gegevens in Experience Platform op te slaan, moet u eerst een dataset tot stand brengen, en dan uw summiere gegevens in de dataset uploaden.

Een gegevensset maken:

1. Selecteer **[!UICONTROL Experience Platform]** in het menu   ![ app ](/help/assets/icons/Apps.svg)   app-switch.
1. Selecteer **[!UICONTROL Datasets]** in het linkerspoor.
1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create dataset]**.
1. Selecteer **[!UICONTROL Create dataset from schema]** in het scherm **[!UICONTROL Datasets]** > **[!UICONTROL Create datasets]** .
1. In de **[!UICONTROL Select schema]** stap van de **[!UICONTROL Workflows]** > **[!UICONTROL Create dataset from schema]** tovenaar, ![ onderzoek ](/help/assets/icons/Search.svg) naar en selecteer uw **[!UICONTROL Example Summary Data Schema]**.
1. Selecteer **[!UICONTROL Next]** .
1. In de stap **[!UICONTROL Configure dataset]** van de wizard **[!UICONTROL Workflows]** > **[!UICONTROL Create dataset from schema]** :
   1. Voer een **[!UICONTROL Name]** in voor de gegevensset, bijvoorbeeld: `Example Summary Data Dataset` . Geef desgewenst een beschrijving op.
   1. Selecteer **[!UICONTROL Finish]** .

U ziet een scherm dat de details van uw nieuwe dataset toont.

Om uw steekproefgegevens in deze dataset te uploaden:

1. Selecteer **[!UICONTROL Experience Platform]** in het menu   ![ app ](/help/assets/icons/Apps.svg)   app-switch.
1. Selecteer **[!UICONTROL Workflows]** in het linkerspoor.
   1. Selecteer **[!UICONTROL Map CSV to XDM schema]** in de **[!UICONTROL Data ingestion]** -opties in het **[!UICONTROL Workflows]** -scherm.
   1. Selecteer **[!UICONTROL Launch]** in het deelvenster **[!UICONTROL Map CSV to XDM schema]** .
1. In de stap **[!UICONTROL Dataflow detail]** van de wizard **[!UICONTROL Workflows]** > **[!UICONTROL Map CSV to XDM schema]** :
   1. Selecteer **[!UICONTROL Existing dataset]** voor **[!UICONTROL Target dataset]** .
   1. Selecteer **[!UICONTROL Example Summary Data Dataset]** in de vervolgkeuzelijst.
   1. Selecteer **[!UICONTROL Next]** .
1. In de stap **[!UICONTROL Select data]** van de wizard **[!UICONTROL Workflows]** > **[!UICONTROL Map CSV to XDM schema]** :
   1. Sleep het bestand met samenvattingsgegevens in de CSV-indeling naar **[!UICONTROL Drag and drop files]** . U kunt ook **[!UICONTROL Choose files]** gebruiken om het bestand te selecteren.
   1. Zorg ervoor dat **[!UICONTROL Data format]** en **[!UICONTROL Delimiter]** de juiste waarden voor de voorbeeldgegevens hebben. Bijvoorbeeld **[!UICONTROL Delimited]** als **[!UICONTROL Data format]** en **[!UICONTROL ,]** als **[!UICONTROL Delimiter]** .
   1. In **[!UICONTROL Sample data]** wordt een voorbeeld (10 records) van uw overzichtsgegevens weergegeven.
   1. Selecteer **[!UICONTROL Next]** .
1. In de stap **[!UICONTROL Mapping]** van de wizard **[!UICONTROL Workflows]** > **[!UICONTROL Map CSV to XDM schema]** :
   ![ de datasetafbeelding van het Voorbeeld ](../assets/example-dataset-mapping.png)
   1. Controleer of alle gegevensvelden van de **[!UICONTROL Source Data]** correct zijn toegewezen aan de corresponderende **[!UICONTROL Target fields]** in het schema. Voor de voorbeeldgegevens worden geen fouten gerapporteerd omdat u de velden in uw schema expliciet een naam geeft die lijkt op de veldnamen in de voorbeeldgegevens. Anders kunt u dit scherm gebruiken om de toewijzing te corrigeren.
   1. U kunt naar keuze selecteren ![ Gaan ](/help/assets/icons/Gear.svg) **[!UICONTROL Validate]** om (opnieuw) de gegevens te bevestigen.
   1. U kunt naar keuze selecteren ![ Voorproef ](/help/assets/icons/Preview.svg) **[!UICONTROL Preview data]** om een dialoog met een voorproef van de gegevens te openen zodra geladen in de dataset.
   1. Selecteer **[!UICONTROL Finish]** .

In **[!UICONTROL Sources]** > **[!UICONTROL Dataflow - XX/XX/XXXX, XX:XX XX]** wordt de status van het uploaden weergegeven. Vernieuw om updates van de upload te zien. Wanneer dit is gelukt, worden de voorbeeldgegevens in het Experience Platform geladen.




## Verbinding

Om uw steekproefgegevens in Customer Journey Analytics te gebruiken, creeert u een verbinding die de Dataset van de Gegevens van het Voorbeeld Summiere van Experience Platform omvat.


1. Selecteer **[!UICONTROL Customer Journey Analytics]** in het menu   ![ app ](/help/assets/icons/Apps.svg)   app-switch.
1. Selecteer **[!UICONTROL Connections]** in het bovenste menu.
1. Selecteer **[!UICONTROL Create new connection]** .
1. In **[!UICONTROL Connections]** > **[!UICONTROL Untitled connection]** :
   1. Voer een **[!UICONTROL Connection name]** in, bijvoorbeeld `Example Connection Using Summary Data` .
   1. Selecteer de zandbak die de dataset bevat u en de andere datasets creeerde u van de zandbak dropdown lijst wilt omvatten.
   1. Selecteer **[!UICONTROL less than 1 million]** in de vervolgkeuzelijst **[!UICONTROL Average number of daily events]** .
   1. Selecteer **[!UICONTROL Add datasets]** .
   1. In de stap **[!UICONTROL Select datasets]** van de wizard **[!UICONTROL Add datasets]** :
      1. Onderzoek ![ Onderzoek ](/help/assets/icons/Search.svg) en selecteer **[!UICONTROL Example Summary Data Dataset]**, **[!UICONTROL Example Event Data Dataset]**, en **[!UICONTROL Example Lookup Data Dataset]**.
      1. Selecteer **[!UICONTROL Next]** .
   1. In de stap **[!UICONTROL Datasets settings]** van de wizard **[!UICONTROL Add datasets]** :

      1. Voor **[!UICONTROL Example Event Data Dataset]** :

         1. Bevestig dat de selecties voor **[!UICONTROL Person ID]** (`person_id`) en **[!UICONTROL Timestamp]** correct zijn.
         1. Selecteer **[!UICONTROL Web Data]** in het menu **[!UICONTROL Data source type]** .
         1. Schakel **[!UICONTROL Import all new data]** in.
         1. Schakel **[!UICONTROL Backfill all existing data]** in.

      1. Voor **[!UICONTROL Example Lookup Data Dataset]** :

         1. Selecteer **[!UICONTROL tracking_code]** als **[!UICONTROL Key]** en **[!UICONTROL tracking_code (Event datasets)]** als **[!UICONTROL Matching]** Sleutel.
         1. Selecteer **[!UICONTROL Web Data]** in het menu **[!UICONTROL Data source type]** .
         1. Schakel **[!UICONTROL Import all new data]** in.
         1. Schakel **[!UICONTROL Backfill all existing data]** in.

      1. Voor **[!UICONTROL Example Summary Data Dataset]** :

         1. Bevestig dat de selecties voor **[!UICONTROL Timestamp]** en **[!UICONTROL Timezone]** correct zijn.
         1. Schakel **[!UICONTROL Import all new data]** in.
         1. Schakel **[!UICONTROL Backfill all existing data]** in.

      1. Selecteer **[!UICONTROL Add datasets]** .

1. Selecteer in het **[!UICONTROL Connections]** > **[!UICONTROL Example Connection using Summary Data]** verbindingsscherm **[!UICONTROL Save]** om de verbinding op te slaan.

De gegevens van de datasets worden toegevoegd aan Customer Journey Analytics, die een paar uren kan vergen. Wees dus alstublieft geduldig voordat u verdergaat.

Na een tijdje, verifieer dat de gegevens van uw datasets behoorlijk in Customer Journey Analytics worden geladen.

1. Selecteer **[!UICONTROL Customer Journey Analytics]** in het menu   ![ app ](/help/assets/icons/Apps.svg)   app-switch.
1. Selecteer **[!UICONTROL Connections]** in het bovenste menu.
1. Selecteer de verbinding, bijvoorbeeld **[!UICONTROL Example Connection Using Summary Data]** .
1. Selecteer een geschikt gegevensbereik in de details **[!UICONTROL Connection]** > **[!UICONTROL Example Connection Using Summary data]** .
   1. Selecteer ![ Kalender ](/help/assets/icons/Calendar.svg) en selecteer dan **[!UICONTROL Last 7 days]**.
   1. Selecteer **[!UICONTROL Apply]** .

In de lijst van **[!UICONTROL Datasets]**, zouden de waarden in de **[!UICONTROL Records added]** kolom moeten bevestigen dat de gegevens van uw datasets nu deel van Customer Journey Analytics uitmaken.

![ Verbinding van het Voorbeeld voor summiere gegevens ](../assets/example-connection-summary-data.png)

## Gegevens, weergave

Om ervoor te zorgen dat u de juiste gegevens in Workspace kunt rapporteren, wilt u een gegevensweergave maken met de relevante maatstaven en afmetingen.

1. Selecteer **[!UICONTROL Customer Journey Analytics]** in het menu   ![ app ](/help/assets/icons/Apps.svg)   app-switch.
1. Selecteer **[!UICONTROL Data views]** in het bovenste menu.
1. Selecteer **[!UICONTROL Create new data view]** .
1. In **[!UICONTROL Data views]**, ga door de tovenaar schermen om uw gegevensmening te vormen.
   1. In de **[!UICONTROL Configure]** -stap van **[!UICONTROL Data views]** :
      1. Selecteer uw verbinding vanuit **[!UICONTROL Settings]** | **[!UICONTROL Connection]** . Bijvoorbeeld **[!UICONTROL Example Connection Using Summary Data]** .
      1. Voer een **[!UICONTROL Name]** in voor de gegevensweergave, bijvoorbeeld `Example Data View Using Summary Data` .
      1. Laat alle andere instellingen staan.
      1. Selecteer **[!UICONTROL Save and continue]** .
   1. In de **[!UICONTROL Components]** stap van **[!UICONTROL Data views]** > **[!UICONTROL Example Data View Using Summary Data]** :
      1. Voeg de volgende componenten aan de lijst van Dimensionen en van Metriek toe. Voor de duidelijkheid worden de componentnamen gewijzigd van hun standaardnaam met **[!UICONTROL Component name]** in **[!UICONTROL Component settings]** in het deelvenster Componenten (rechts).

         **Cijfers**

         | Componentnaam | Gegevensset | Schema, gegevenstype | Schemapad |
         |---|---|---|---|
         | Kosten | Gegevensset voorbeeldsamenvattingsgegevens | Dubbel | *_huurder* .cost |
         | Impressies | Gegevensset voorbeeldsamenvattingsgegevens | Geheel | *_huurder* .IMAGE |
         | Orders | Gegevensbestand voorbeeldgebeurtenisgegevens | Geheel | *_huurder* .orders |
         | Ontvangsten | Gegevensbestand voorbeeldgebeurtenisgegevens | Dubbel | *_huurder* .Revenue_amount |

         **Dimensies**

         | Componentnaam | Gegevensset | Schema, gegevenstype | Schemapad |
         |---|---|---|---|
         | Advertentiegroep (opzoeken) | Voorbeeld van gegevensdatabase opzoeken | String | *_huurder*.ad_group |
         | Advertentiegroep (overzicht) | Gegevensset voorbeeldsamenvattingsgegevens | String | *_huurder*.ad_group |
         | Campagne-id | Gegevensset van samenvattingsgegevens controleren | String | *_huurder* .campagne_id |
         | Campagnenaam (opzoeken) | Voorbeeld van gegevensdatabase opzoeken | String | *_huurder* .campagne_name |
         | Naam campagne (overzicht) | Gegevensset voorbeeldsamenvattingsgegevens | String | *_huurder* .campagne_name |
         | Netwerk | Gegevensset voorbeeldsamenvattingsgegevens | String | *_huurder* .network |
         | Paginanaam | Gegevensbestand voorbeeldgebeurtenisgegevens | String | *_huurder* .page_name |
         | Persoon-id | Gegevensbestand voorbeeldgebeurtenisgegevens | String | *_huurder* .person_id |
         | Trackingcode (gebeurtenis) | Gegevensbestand voorbeeldgebeurtenisgegevens | String | *_huurder*.tracking_code |
         | Trackingcode (opzoeken) | Voorbeeld van gegevensdatabase opzoeken | String | *_huurder*.tracking_code |

      1. Selecteer de **[!UICONTROL Tracking Code (Event)]** -dimensie in de lijst **[!UICONTROL Dimensions]** . In het deelvenster Componenten:

         ![ het Volgen gegevens van de codesamenvatting ](../assets/tracking-code-summary-data.png)
         1. Ontvouw ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Summary Data Group]**.
         1. Schakel **[!UICONTROL Create grouping]** in.
         1. Selecteer **[!UICONTROL Campaign Id]** in de vervolgkeuzelijst **[!UICONTROL Dimension]** . Deze stap zorgt ervoor dat gebeurtenisgegevens en samenvattingsgegevens correct worden gecombineerd voor rapportage.
         1. U kunt desgewenst **[!UICONTROL Hide in reporting]** inschakelen. [!UICONTROL Hide in reporting] zorgt ervoor dat de geselecteerde dimensie ([!UICONTROL Campaign Id]) wordt verborgen in Analysis Workspace en andere Customer Journey Analytics rapportagegereedschappen. Als u deze optie hebt ingeschakeld, kunt u de optie verifiëren:
            1. Selecteer de **[!UICONTROL Campaign Id]** -dimensie in de lijst **[!UICONTROL Dimensions]** .
            1. U ziet dat **[!UICONTROL Hide component in reporting]** in **[!UICONTROL Component settings]** nu automatisch is ingeschakeld.

      1. Maak een nieuw afgeleid veld, bijvoorbeeld `Campaign Name (Lookup Derived Field)`, om ervoor te zorgen dat u in Workspace de dimensie Campagnenaam (Opzoeken) uit de gegevensset Gegevens opzoeken kunt gebruiken.

         ![ Voortgekomen gebied voor campagnenaam ](../aa-data/../assets/summary-derived-field.png)

         1. Selecteer **[!UICONTROL campaign_id]** voor **[!UICONTROL Value]** .
         1. Selecteer **[!UICONTROL Example Lookup Data Dataset]** in het vervolgkeuzemenu **[!UICONTROL Lookup dataset]** .
         1. Selecteer **[!UICONTROL tracking_code]** in het vervolgkeuzemenu **[!UICONTROL Matching Key]** .
         1. Selecteer **[!UICONTROL campaign_name]** in het vervolgkeuzemenu **[!UICONTROL Values to return]** .
         1. Selecteer **[!UICONTROL Save]** .

      1. Voeg het nieuwe afgeleide veld **[!UICONTROL Campaign Name (Lookup Derived Field)]** toe aan de lijst met **[!UICONTROL Dimensions]** -componenten.

      1. Selecteer de **[!UICONTROL Campaign Name (Lookup)]** -dimensie in de lijst **[!UICONTROL Dimensions]** . In het deelvenster Componenten:

         ![ Afgeleide Groep van Gegevens van het Gebied Summiere ](../assets/derived-field-summary-data-group.png)

         1. Ontvouw ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Summary Data Group]**.
         1. Schakel **[!UICONTROL Create grouping]** in.
         1. Selecteer **[!UICONTROL Campaign Name (Lookup Derived Field)]** in de vervolgkeuzelijst **[!UICONTROL Dimension]** . Deze stap zorgt ervoor dat de Naam van de Campagne (Opzoeken) van de Dataset van de Gegevens van de Opzoeken van het Voorbeeld veilig in het melden (zie [ Workspace ](#workspace)) kan worden gebruikt.

      1. Selecteer de metrische waarde **[!UICONTROL Revenue]** in de lijst **[!UICONTROL Metrics]** . In het deelvenster Componenten:

         ![ de summiere gegevens van de Opbrengst ](../assets/revenue-summary-data.png)
         1. Ontvouw ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Attribution]**.
            1. Selecteer ![ AttributionLastTouch ](/help/assets/icons/AttributionLastTouch.svg) **[!UICONTROL Last Touch]** van de **[!UICONTROL Attribution Model]** dropdown lijst.
            1. Selecteer **[!UICONTROL 30 Day]** in de vervolgkeuzelijst **[!UICONTROL Lookback window]** .
         1. Ontvouw ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) **Formaat**.
            1. Selecteer **[!UICONTROL Currency]** in de vervolgkeuzelijst **[!UICONTROL Format]** .
            1. Selecteer **[!UICONTROL 2]** in de vervolgkeuzelijst **[!UICONTROL Decimal places]** .

      1. Selecteer de metrische waarde **[!UICONTROL Orders]** in de lijst **[!UICONTROL Metrics]** . In het deelvenster Componenten:

         ![ orden summiere gegevens ](../assets/orders-summary-data.png)
         1. Ontvouw ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Attribution]**.
            1. Selecteer ![ AttributionLastTouch ](/help/assets/icons/AttributionLastTouch.svg) **[!UICONTROL Last Touch]** van de **[!UICONTROL Attribution Model]** dropdown lijst.
            1. Selecteer **[!UICONTROL 30 Day]** in de vervolgkeuzelijst **[!UICONTROL Lookback window]** .
         1. Ontvouw ![ ChevronDown ](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Format]**.
            1. Selecteer **[!UICONTROL Decimal]** in de vervolgkeuzelijst **[!UICONTROL Format]** .
            1. Selecteer **[!UICONTROL ▲ Good (green)]** in de vervolgkeuzelijst **[!UICONTROL Show upward trend as]** .

      1. Selecteer **[!UICONTROL Save and continue]** .

   1. In de **[!UICONTROL Settings]** -stap van **[!UICONTROL Data views]** :
      1. Laat alle instellingen op de standaardwaarden staan.
      1. Selecteren **[!UICONTROL Save and finish.]**

U hebt nu de gegevensweergave ingesteld voor een juiste rapportage over samenvattingsgegevens.


## Workspace

Maak een nieuw project in Analysis Workspace om uw samenvattingsgegevens te melden.

1. Selecteer **[!UICONTROL Customer Journey Analytics]** in het menu   ![ app ](/help/assets/icons/Apps.svg)   app-switch.
1. Selecteer **[!UICONTROL Workspace]** in het bovenste menu.
1. Selecteer **[!UICONTROL Create project]** .
1. Selecteer **[!UICONTROL Blank Workspace project]** in het dialoogvenster met opties om een leeg Workspace-project te maken.
1. Selecteer **[!UICONTROL Create]** .

Er wordt een leeg canvas weergegeven met een deelvenster [!UICONTROL Freeform] , dat bestaat uit een leeg [!UICONTROL Freeform table] .

1. Zorg ervoor dat de gegevensweergave die voor het deelvenster is geselecteerd, verwijst naar de gegevensweergave die de configuratie voor de samenvattingsgegevens bevat. Bijvoorbeeld: **[!UICONTROL Example Data View Using Summary Data.]**
1. Zorg ervoor dat het gegevensbereik geldig is voor de gegevens waarover u wilt rapporteren. Bijvoorbeeld: **[!UICONTROL Last 2 full months]** .
1. Sleep **[!UICONTROL Tracking Code (Event)]** vanuit **[!UICONTROL Dimensions]** en zet de dimensie neer op de lege tabel voor vrije vorm.
1. Sleep **[!UICONTROL Orders]** vanuit **[!UICONTROL Metrics]** en zet de metrische waarde neer op de kolom **[!UICONTROL Events]** om die kolom in de tabel voor vrije vorm te vervangen.
1. Sleep **[!UICONTROL Revenue]** van **[!UICONTROL Metrics]**, en laat vallen metrisch om als extra kolom aan de lijst van de Vrije vorm toe te voegen.
1. Sleep **[!UICONTROL Impressions (Summary)]** van **[!UICONTROL Metrics]**, en laat vallen metrisch om als extra kolom aan de lijst van de Vrije vorm toe te voegen.
1. Sleep **[!UICONTROL Cost (Summary)]** van **[!UICONTROL Metrics]**, en laat vallen metrisch om als extra kolom aan de lijst van de Vrije vorm toe te voegen.
1. Als u uw project wilt opslaan, selecteert u **[!UICONTROL Project]** > **[!UICONTROL Save]** en geeft u een naam op voor het project. Bijvoorbeeld `Example Project Using Summary Data` .

U wilt de bevoegdheid gebruiken om over summiere gegevens te rapporteren en over kosten per indruk en terugkeer op ad-uitgave (ROAS) te melden. Om op deze metriek te rapporteren, moet u twee berekende metriek tot stand brengen.

1. Selecteer **[!UICONTROL Components]** > **[!UICONTROL Calculated metrics]** .
1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add]** om nieuwe berekende metrisch toe te voegen.
   1. Geef `Cost per Impression` op voor de lus **[!UICONTROL Name]** .
   1. Selecteer **[!UICONTROL Currency]** voor **[!UICONTROL Format]** .
   1. Geef `4` op voor **[!UICONTROL Decimal places]** .
   1. Gebruik ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Cost (Summary)]** **[!UICONTROL ÷]** **[!UICONTROL Impressions (Summary)]** als **[!UICONTROL Definition]**.
   1. Selecteer **[!UICONTROL Save]** .
1. Selecteer ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add]** om een andere nieuwe berekende metrische waarde toe te voegen.
   1. Geef `Return on Ad Spend` op voor de lus **[!UICONTROL Name]** .
   1. Selecteer **[!UICONTROL Currency]** voor **[!UICONTROL Format]** .
   1. Selecteer `2` voor **[!UICONTROL Decimal places]** .
   1. Het gebruik ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Revenue (Last Touch | 30 Days)]** **[!UICONTROL −]** ![ Gebeurtenis ](/help/assets/icons/Event.svg) **[!UICONTROL Cost (Summary)]** als **[!UICONTROL Definition]**.
   1. Selecteer **[!UICONTROL Save]** .

Voeg uw berekende metriek aan uw rapport toe.

1. Sleep **[!UICONTROL Cost per Impression]** ![ Rekenmachine ](/help/assets/icons/Calculator.svg) van **[!UICONTROL Metrics]** en laat vallen metrisch om als extra kolom aan de lijst Freeform toe te voegen.
   1. Selecteer ![ plaatsende ](/help/assets/icons/Setting.svg) montages van de Kolom.
      1. Schakel **[!UICONTROL Percent]** uit.
1. Sleep **[!UICONTROL Return on Ad Spend]** ![ Rekenmachine ](/help/assets/icons/Calculator.svg) van **[!UICONTROL Metrics]** en laat vallen metrisch om als extra kolom aan de lijst Freeform toe te voegen.
   1. Selecteer ![ plaatsende ](/help/assets/icons/Setting.svg) montages van de Kolom.
      1. Schakel **[!UICONTROL Percent]** uit.
      1. Schakel **[!UICONTROL Conditional formatting]** in.
         1. Selecteer **[!UICONTROL Auto-generated]** .
         1. Selecteer een voorkeur **[!UICONTROL Conditional formatting palette]** .
   1. Selecteer **[!UICONTROL Save]** om uw project op te slaan.

Voer de volgende stappen uit als u de campagnenaam wilt rapporteren in plaats van de code te volgen (gebeurtenis):

1. Dupliceer de visualisatie van de **[!UICONTROL Summary Data Report]** Freeform-tabel.
1. Wijzig de naam van de gedupliceerde visualisatie in `Summary Data Report (using Campaign Name)` .
1. Vervang ![ Schakelaar ](/help/assets/icons/Switch.svg) de **[!UICONTROL Tracking Code (Event)]** dimensie met de **[!UICONTROL Campaign Name (Lookup)]** dimensie.

U kunt correct op de Naam van de Campagne (Opzoeken) wegens het afgeleide gebied melden u creeerde, en de samenvattingscomponentenconfiguratie van de gegevensgroep voor de Naam van de Campagne (Opzoeken). Zie [ mening van Gegevens ](#data-view).

Uw uiteindelijke project moet er net zo uitzien als hieronder.

![ Project van het Voorbeeld dat Summiere Gegevens gebruikt, die Samenvattend Comité van Gegevens met Samenvattend Rapport van Gegevens tonen ](../assets/summary-workspace.png)


>[!MORELIKETHIS]
>
>[ Summiere gegevens ](/help/data-views/summary-data.md)
>[Samenvattende de componentenmontages van de gegevensgroep ](/help/data-views/component-settings/summary-data-group.md)
