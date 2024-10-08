# Inleiding

Dit ontwerp (*solution design*) biedt een gedetailleerde aanpak voor het
implementeren en optimaliseren van lokale energiesystemen, gebaseerd op de
waardestroom "Optimaliseren van capaciteit". In een tijd waarin
energie-efficiëntie en duurzaamheid steeds belangrijker worden, richt dit
ontwerp zich op het verbeteren van de capaciteit van lokale systemen door
middel van technologische innovatie en strategische planning. Het ontwerp
beschrijft de stappen die nodig zijn om kansen te verkennen, oplossingen te
ontwikkelen, en de systemen effectief te beheren, met als doel een
toekomstbestendig en schaalbaar lokaal energiemodel te creëren.

> [!NOTE]
> Een *Energy Hub* functioneert als een (virtueel) lokaal energiesysteem,
> waarin lokaal (duurzaam) opgewekte elektriciteit, warmte, koude en biogassen
> zoveel mogelijk ook lokaal worden benut, via een slim balancering systeem
> afgestemd op de vraag. Discrepanties tussen vraag en aanbod worden opgevangen
> via opslag- en flex/conversiesystemen en via uitwisselingen met gereguleerde
> netten binnen de randvoorwaarde van kwaliteit van levering en beschikbaarheid
> van infrastructuur.

De nadruk in dit document ligt op het perspectief van de netbeheerder; welke
informatie moet worden verstrekt aan de verschillende stakeholders om een
passende oplossing voor het optimaliseren van capaciteit te kunnen
implementeren? De context voor dit document is ontleend vanuit de [Blauwdruk
Energy Hubs](https://www.eigen-energyhubs.nl/de-blauwdruk/), waarbij op deze
blauwdruk wordt voortgebouwd. Ook de definities (her)gebruikt in dit document
zijn overgenomen uit de blauwdruk.

Voor de netbeheerder zijn de dataproducten behorende bij
[waardestroomstappen](#stappen) en de uitwerking van de
[capabilities](#capabilities) het meest relevant, dit is de basis voor het uit
te voeren werk door de verschillende implementatiepartijen (e.g. EDSN, *DSO*s
en *TSO*).

## Leeswijzer

Het ontwerp is gestructureerd rondom de waardestroom [Optimaliseren van
capaciteit](#value-stream-optimaliseren-van-capaciteit-voor-lokale-energiesystemen),
waarbij elke waardestroomstap – *Verkennen*, *Onderzoek & Ontwerp*,
*Realiseren*, *Operationeel Beheer*, en *Evaluatie & Verbetering* – stap voor
stap wordt toegelicht. Per fase worden de activiteiten, actoren, systemen en
gewenste resultaten beschreven. Daarnaast wordt per waardestroomstap een
gedetailleerde invulling van de gevraagde informatiebehoefte beschreven als
dataproduct.

De cohesie van de oplossing wordt toetsbaar gemaakt door de koppeling te maken
tussen *functionele- en kwaliteitseisen*, *waardestroom* (gecreëerde waarde),
*capabilities* en *proces- en data-uitwerking*.

## TODO

- [ ] Toetsen of Blauwdruk Energy Hubs van toepassing is
- [ ] Aanvullen functionele eisen voor *realisatiebedrijf* en
  *exploitatiebedrijf*
- [ ] Kwaliteitseisen bepalen voor dataproducten en uitwerken
- [ ] Verder uitwerken dataproducten voor *Onderzoek & ontwerp*
- [ ] Toetsen aannames rondom inhoud en gebruik van dataproducten
- [ ] Uitwerken *Realisatie*,  *Operationeel beheer* en *Evaluatie en
  verbeteren*: capabilities, bedrijfsprocessen en dataproducten
- [ ] Uitwerken *capabilities*: wie gaat wat doen en met welke tooling?
- [ ] Uitwerken resterende informatiebehoefte tot dataproducten
- [ ] Ontwerp vertalen naar *features*

# Scope

De reikwijdte (*scope*) van de oplossing beschreven in dit ontwerp beperkt zich
tot implementatie van de waardestroom "Optimaliseren van capaciteit voor lokale
energiesystemen". Het perspectief van de oplossing wordt beperkt tot dat van de
netbeheerder. Daar waar context en achtergrond vereist is om de oplossing
kunnen toetsen aan de hand van de functionele eisen en informatiebehoefte wordt
de *Blauwdruk Energy Hubs* gebruikt.

## Stakeholders

De volgende stakeholders zijn betrokken binnen dit ontwerp:

* *GV-klant*: verbruikt, wekt of slaat elektrische energie op binnen de eigen
  locatie;
* *netbeheerder*: beheert de fysieke netinfrastructuur en faciliteert het
  functioneren van de markt;
* *ontwikkelbedrijf*: regie-organisatie om tot de benodigde aanpassingen en
  randvoorwaarden voor een *Energy Hub* te komen. Fungeert als voorloper voor
  het exploitatiebedrijf (de *Energy Hub*);
* *realisatiebedrijf*: door ontwikkelbedrijf opgerichte projectorganisatie;
* *exploitatiebedrijf*: investeert in de benodigde *assets* en draagt zorg dat
  de balans tussen vraag en aanbod van (elektrische) energie op een economisch
  optimale manier en binnen de randvoorwaarden van de netbeheerder(s) wordt
  afgestemd.

# Functionele eisen

Functionele eisen specificeren de specifieke functionaliteiten en prestaties
die een systeem of product moet bieden om aan de behoeften en verwachtingen van
de gebruikers te voldoen. Ze beschrijven de vereiste taken, processen en
interacties die het systeem moet ondersteunen om de beoogde doelen te bereiken.

|#  |Als             |Wil ik                                                                               |Want|
|--:|----------------|-------------------------------------------------------------------------------------|----|
| 1.|Ontwikkelbedrijf|Standaard verbruiksprofielen van bedrijfsprocessen (met een resolutie van 15 minuten)|?|
| 2.|Ontwikkelbedrijf|Standaard opwekprofielen voor verschillende (weers)omstandigheden|?|
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
> opgevoerd. Voor meer detail, zie de blauwdruk.

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
*capabilities* ingevuld worden om daadwerkelijk de gevraagde waarde
(dataproducten) te kunnen leveren.

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
|[Nettopologie](https://netbeheer-nederland.github.io/dp-eh-nettopologie/)|5                |Beschrijving van de topologie van een (mogelijke) *Energy Hub*. Het gaat hier zowel om informatie van *aansluitingen* die in aanmerking komen voor deelname aan de *Energy Hub*, als geografische informatie|Open|Decentraal|
|SBI verbruiksdata|1                |Algemene verbruiksdata per bedrijfsactiviteit|Open|Centraal|

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
|GV-meetdata|4                |TODO: Verbruiksprofielen (vermogen in kW) van *bedrijfsprocessen* op basis van historische data|Gesloten|Centraal|

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

Deze *capability beschrijft het vermogen om open data beschikbaar te maken voor
derden ten behoeve van energietransitie of anderszins omgevingsvraagstukken uit
te wisselen met klanten en/of andere stakeholders als gemeenten,
energiecorporaties, warmtebedrijven, woningcorporaties, provincies,
rijksoverheid en consultancybureau's. Deze capability betreft open data.

![C.6.4.2 Open data beschikbaar maken voor derden](assets/c642_open_data_beschikbaar_maken_voor_derden-20240909.png)

# Beslissingen & aannames

## Aannames

- [ ] De blauwdruk vraagt om informatie over de "netsituatie en topologie".
  Binnen dit ontwerp wordt deze informatiebehoefte concreet gemaakt naar:
  - (actuele) capaciteit- en belastingprofielen van station,
    transformator(veld) en kabel;
  - meetgegevens van GV-klanten;
  - geografische informatie van netcomponenten (huidig & gepland);
  - connectiviteitsinformatie van netcomponenten (huidig & gepland);
  - aansluit- en transportovereenkomst behorende bij een aansluiting (ATO).
- [ ] Is het *Standaard opwekprofiel* gelijk in de implementatie als het
  *Standaard verbruiksprofiel*? Dus per SBI-code, zonder weerinformatie
- [ ] Primaire business case van een *Energy Hub* is peak-shaving en verkoop
  van flexibiliteit
- [ ] TODO: Wat is de business case voor een netbeheerder?
- [ ] TODO: ontvangt de netbeheerder gegevens van b.v. een aannemer?
- [ ] TODO: wie bepaalt het energieprofiel van een specifieke GV-klant die
      onderdeel is van een EnergyHub?
- [ ] TODO: hoe handhaaft een netbeheerder het energieprofiel van een EnergyHub?

# Uitzonderingen op architectuurprincipes

Er zijn geen uitzonderingen gemaakt op de principes beschreven in de
*Doelarchitectuur Datadelen* van NBEA.
