# Inleiding

> [!NOTE]
> TODO

# Scope, strategie & motivatie

- [ ] TODO: beperken tot waardestroom "Optimaliseren van capaciteit voor lokale
  energiesystemen
- [ ] TODO: beperken tot capabilities van de netbeheerder om dataproducten aan
  te kunnen leveren
- [ ] TODO: input zijn functionele eisen, customer journey van WG EnergyHubs,
  Blauwdruk EIGEN, ChatGPT, Doelarchitectuur Datadelen (NBEA)
- [ ] TODO: Perspectief beperkt zich tot dat van regionale netbeheerder, met
  focus op het leveren van dataproducten
- [ ] TODO: Stakeholders (GV-klant, gemeente, ontwikkelbedrijf,
  realisatiebedrijf, exploitatiebedrijf)

# Functionele eisen

Functionele eisen specificeren de specifieke functionaliteiten en prestaties
die een systeem of product moet bieden om aan de behoeften en verwachtingen van
de gebruikers te voldoen. Ze beschrijven de vereiste taken, processen en
interacties die het systeem moet ondersteunen om de beoogde doelen te bereiken.

|#  |Als             |Wil ik                                                                               |Want|
|--:|----------------|-------------------------------------------------------------------------------------|----|
| 1.|Ontwikkelbedrijf|Standaard verbruiksprofielen van bedrijfsprocessen (met een resolutie van 15 minuten)|?|
| 2.|Ontwikkelbedrijf|Standaard opwek profielen voor verschillende (weers)omstandigheden|?|
| 3.|Ontwikkelbedrijf|Informatie van de netbeheerder over de lokale netsituatie, beperkingen en uitbreidingsplannen|?|
| 4.|Ontwikkelbedrijf|Verbruiksprofielen (vermogen in kW) van *bedrijfsprocessen* op basis van historische data (met een resolutie van 15 minuten)|?|
| 5.|Ontwikkelbedrijf|De netsituatie en topologie (hoe zijn de bedrijven elektrisch met elkaar verbonden, met welke kabels en op welke velden zijn zij aangesloten)|?|
| 6.|Ontwikkelbedrijf|Een overzicht van het opgestelde vermogen van de lokale elektriciteitsopwekking per type en per invoedingspunt|?|
| 7.|Ontwikkelbedrijf|Een overzicht van de huidige capaciteit (kWh) en maximaal vermogen (kW) van bestaande batterij-installaties per aansluiting|?|
| 8.|Ontwikkelbedrijf|Een overzicht van de huidige mogelijkheden voor vraagsturing|?|
| 9.|Ontwikkelbedrijf|Een doorkijk van de toename van de vermogensvraag op basis van verduurzamingsplannen van de bedrijven|?|

# Kwaliteitseisen

> [!NOTE]
> Kwaliteitseisen (non-functionals) conform ISO/IEC 25010

# Future State (Soll)

In dit hoofdstuk wordt een gedetailleerd beeld geschetst van de gewenste
toekomstige situatie waarin de waardestroom "Optimaliseren van capaciteit voor
lokale energiesystemen" volledig is gerealiseerd. Er wordt beschreven hoe de
verwachte verbeteringen in efficiëntie, flexibiliteit en duurzaamheid van de
lokale energiesystemen tot stand komen.

> [!NOTE]
> Een waardestroom is een reeks stappen die een organisatie doorloopt om waarde
> te creëren en te leveren aan haar klanten, van begin tot eind. Het omvat alle
> activiteiten, van het identificeren van de behoefte tot het uiteindelijke
> leveren van het product of de dienst. Elke stap draagt bij aan het verhogen
> van de waarde voor de eindgebruiker.

Daarnaast wordt belicht hoe de geïmplementeerde oplossingen bijdragen aan het
optimaal benutten van beschikbare energiebronnen en aan het versterken van de
energie-infrastructuur voor de lange termijn.

## Value Stream: Optimaliseren van capaciteit voor lokale energiesystemen

In deze sectie wordt de waardestroom stap voor stap uitgewerkt, waarbij elke
stap van de waardestroom gedetailleerd wordt beschreven om de optimale
capaciteit voor lokale energiesystemen te realiseren. De uitwerking van elke
stap van de waardestroom beschrijft het benodigde landschap vanuit proces-,
applicatie-, platform- en dataperspectief.

![Optimaliseren van capaciteit](assets/value_stream-20240904.png)

> [!NOTE]
> Voor de inhoudelijke uitwerking van de waardestroom wordt de [Blauwdruk
> Energy Hubs](https://www.eigen-energyhubs.nl/de-blauwdruk/) van EIGEN
> gebruikt. Voor dit ontwerp worden de meest relevante punten als context
> opgevoerd. Voor meer detail, zie de Blauwdruk.

### Stappen

Elke stap in de waardestroom creëert waarde voor de primaire stakeholder, de
grootverbruikklant (GV-klant):

|Stap                       |Waarde                                           |
|---------------------------|-------------------------------------------------|
|**Verkennen**              |Biedt inzicht in het potentieel van het opzetten van een *Energy Hub* en brengt mogelijke risico's in kaart|
|**Onderzoek & ontwerp**    |Legt de juridische en technische basis en voorziet in een concreet implementatiepad|
|**Realiseren**             |Implementatie van het ontwerp voor de *Energy Hub* en verhoogt operationele capaciteit|
|**Operationeel beheer**    |Biedt inzicht en optimaliseert prestaties van de *Energy Hub*|
|**Evaluatie & verbetering**|Voorziet in langdurige efficiëntie en duurzaamheid van de *Energy Hub*|

Alle bovengenoemde stappen worden verder toegelicht in de volgende
hoofdstukken.

### Capabilities

Vanuit het perspectief van de dataleverende netbeheerder moeten een aantal
*capabilities* ingevuld worden om daadwerkelijk de gevraagde dataproducten te
kunnen leveren.

> [!NOTE]
> Een *capability* verwijst naar de specifieke vaardigheden, middelen of
> processen die een organisatie in staat stellen om bepaalde taken effectief
> uit te voeren en strategische doelstellingen te bereiken. Benoemde
> capabilities zijn onderdeel van het [NBility Capability
> Model](https://www.edsn.nl/nbility-model/).

|Capability                                       |Beschrijving                                           |
|-------------------------------------------------|-------------------------------------------------------|
|C.6.4.1 Marktdata beschikbaar maken voor partijen|Beschikbaar maken van **gesloten data** als dataproduct|
|C.6.4.2 Open data beschikbaar maken voor derden  |Beschikbaar maken van **open data** als dataproduct    |

*Business Services* vanuit capabilitie duiden welke ondersteuning vanuit de
netbeheerders vereist is voor uitvoer van de waardestroomstappen om tot een
geoptimaliseerd lokaal energiesysteem te komen.

## Verkennen

Onderzoeken met welke lokale omstandigheden rekening kan en moet worden
gehouden en of er voldoende momentum kan worden gecreëerd bij bedrijven om een
(voorloper voor) een *Energy Hub* op te zetten.

![Verkennen](assets/verkennen-20240904.png)

Het diagram illustreert hoe de aangegeven behoefte tot het optimaliseren van
capaciteit van de GV-klant het proces "Analyseren behoefte" start, wat leidt
tot de status "Behoefte geanalyseerd". Binnen dit proces wordt de basis gelegd
voor verdere stappen in de
[waardestroom](#value-stream-optimaliseren-van-capaciteit-voor-lokale-energiesystemen).
Het nieuw op te zetten Ontwikkelbedrijf is verantwoordelijk voor het uitvoeren
van de analyse, namens de GV-klanten.

Ter ondersteuning van de analyse worden de volgende dataproducten gevraagd:

|Dataproduct |Functionele eisen|Beschrijving|Type|Oorsprong|
|------------|-----------------|------------|----|---------|
|Nettopologie|5                |Beschrijving van de topologie van een (mogelijke) *Energy Hub*. Het gaat hier zowel om informatie van *aansluitingen* die in aanmerking komen voor deelname aan de *Energy Hub*, als geografische informatie|Open|Decentraal|
|SBI-profiel |1                |Algemene verbruiksdata per bedrijfsproces|Open|Centraal|

- [ ] TODO: zijn meer dataproducten nodig voor de verkenningsfase?

Deze dataproducten worden gerealiseerd via de capability [C.6.4.2 Open data
beschikbaar maken voor derden](#c642-open-data-beschikbaar-maken-voor-derden).

## Onderzoek & ontwerp

Het ontwikkelen van gedetailleerde oplossingen om de capaciteit van lokale
energiesystemen te optimaliseren. Het betreft hier technische ontwikkeling,
economische analyse, simulatie & modellering en wet- en regelgeving.

![Onderzoek & ontwerp](assets/onderzoek-20240909.png)

In deze waardestroomstap wordt de verkenningsfase, na een positief advies,
opgevolgd met diepgaand onderzoek en ontwerp. Het ontwikkelbedrijf verwerkt het
resultaat van het onderzoek en ontwerp in een "Beslisdocument", wat effectief
het *businessplan* voor het op te richten exploitatiebedrijf is. Alle
bedrijfsprocessen worden uitgevoerd door het ontwikkelbedrijf.

Ter ondersteuning van het opstellen van het beslisdocument worden de volgende
dataproducten gevraagd:

|Dataproduct|Functionele eisen|Beschrijving|Type|Oorsprong|
|-----------|-----------------|------------|----|---------|
|GV-meetdata|4                |Verbruiksprofielen (vermogen in kW) van *bedrijfsprocessen* op basis van historische data|Gesloten|Centraal|

## Realiseren

> [!NOTE]
> TODO

## Operationeel beheer

> [!NOTE]
> TODO

## Evaluatie & verbeteren

> [!NOTE]
> TODO

## C.6.4.1 Marktdata beschikbaar maken voor partijen

> [!NOTE]
> TODO

## C.6.4.2 Open data beschikbaar maken voor derden

> [!NOTE]
> TODO

# Beslissingen & aannames

> [!NOTE]
> TODO

- [ ] TODO: ontvangt de netbeheerder gegevens van e.g. aannemer?
- [ ] TODO: hoe handhaaft een netbeheerder het energieprofiel van een EnergyHub?

# Uitzonderingen op architectuurprincipes

> [!NOTE]
> TODO

# Risico's & mitigatie

> [!NOTE]
> TODO
