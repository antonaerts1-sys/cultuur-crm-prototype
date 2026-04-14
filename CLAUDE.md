# Gedeeld CRM voor de Cultuursector

## Wat is dit project?

Een **gedeeld, modulair CRM-platform** specifiek voor de Vlaamse/Belgische cultuursector. Geen Salesforce of HubSpot die je moet ombuigen, maar software die vanaf nul is opgebouwd rond hoe cultuurhuizen echt werken. Meerdere organisaties delen dezelfde codebase, dezelfde kosten, en beslissen samen over de richting.

Het concept is ontwikkeld door **Statik** en wordt gelanceerd als antwoord op de RFP van **Kaaitheater vzw** (deadline offerte: 31/08/2025, lancering: 01/09/2026). Kaaitheater is de eerste beoogde "pionier".

---

## De twee bronnen

### 1. Concept deck: "Een gedeeld CRM — Software delen met de sector" (Statik)
- Pitch voor een cooperatief deelplatform naar het model van Opvang.Vlaanderen (200+ gemeenten, 1 platform)
- Kernprobleem: elke organisatie vindt het wiel opnieuw uit, generieke CRM's passen niet, vendor lock-in
- Oplossing: gedeelde softwarebasis, gedeeld eigenaarschap, samen beslissen, gedeelde kosten

### 2. RFP CRM Kaaitheater (1 juli 2025)
- 42 medewerkers (60+ in werkelijkheid), kunstenhuis in Brussel (dans, theater, performance, conversaties)
- Nomadische periode 2022-2027 (renovatie Sainctelettesquare), nieuw gebouw september 2027
- Projectverantwoordelijke: Jonas Maes — dubbele rol: digital communication & partnerships + ICT coordination
- Gefragmenteerde data over 5 systemen: Yesplan, Ticketmatic, Mailchimp, Zensoft, RStudio
- Voortraject: 6 maanden analyse (okt 2024 - apr 2025) begeleid door Digiraf (Gents adviesbureau voor mensgerichte digitalisering in social profit)

---

## Veldonderzoek: Interview 30CC (Robrecht)

Bron: `/Users/antonaerts/Downloads/Interviews CRM (1).pdf`

### 30CC profiel
- Cultuurcentrum Leuven, ~250 activiteiten/jaar + festivals (Leuven Jazz, Rode Hond, zomerfestival)
- Seizoen: september tot juni + zomerluik
- Schouwburg 480 zitplaatsen + diverse zalen en foyers
- **42.000 eigen tickets/jaar**, 33.000 tickets op een dag bij seizoensstart in juni
- 4 marcom medewerkers
- Publiek: 89% uit regio (30km), 55% uit Leuven. Veel studenten en internationaal publiek
- Tweetalig (NL/EN), soms drietalig (NL/EN/FR)
- Stedelijke VZW — GDPR is extra complex vanwege overheidsstatus

### Huidige systemen (nog meer versnipperd dan Kaaitheater)
| Systeem | Functie |
|---------|---------|
| **Ticketmatic** | Ticketing + beperkte CRM/communicatie |
| **iTheater / Yesplan** | Event- en ruimteplanning, technisch personeel |
| **Excel-lijsten** | Vrijwilligers, partners, curatoren, VIP's, buurtcontacten, amateurgezelschappen, dansers, kabinetsmedewerkers, crowd-funding, leerkrachten |
| **Prezly** | Perslijsten en persberichten |
| **Outlook** | BCC-mailings, losse contactgroepen |
| **Kleine Prins** | Boekhoudsoftware |
| **4 Drupal-websites** | 30CC, Cirklabo, Rode Hond, Leuven Jazz — verouderd, niet geintegreerd |

### Pijnpunten (letterlijk uit het interview)
1. **Geen centrale CRM-laag** — Professionele contacten verspreid in inboxen, Excels, individuele collega's
2. **Vertrekkend personeel = verlies van kennis en contacten** — Cruciaal probleem
3. **Geen funnel tracking** — Ticketmatic stopt bij de ticketknop, geen zicht op drop-off
4. **Driedubbel werk** — Wijzigingen apart in Ticketmatic, iTheater, website en communicatie invoeren
5. **Geen automatische koppelingen** = fouten en tijdsverlies
6. **Outlook/BCC-mailings** — Onprofessioneel, foutgevoelig, niet GDPR-proof
7. **Perslijsten** — Onderhoud intensief, veel verouderde contacten
8. **Boekhouding** — Kosten en opbrengsten niet gekoppeld per evenement, veel Excel-handwerk
9. **Analytics zwak** — Ticketmatic: open rates wel, maar geen funnels of per-item statistieken
10. **GDPR-discussie met stadsjuristen** — Beperking: enkel nieuwsbriefconsent, geen promo op basis van aankoop

### Wat 30CC mist aan Ticketmatic
- Geen funnels of per-item statistieken
- Rapportage beperkt (concentvraag)
- Geen interessesferen (alleen aankoophistoriek)
- Met vorig systeem (Spotler) hadden ze verfijnde segmentatie en A/B-testing — dat is nu weg
- API is makkelijk maar salesfunnel is niet compleet

### Inspiratie en droombeeld
- **deSingel** investeerde zwaar in custom Salesforce waar alles aan elkaar hangt (productiefiche, fotomap, narrowcasting, logistiek). Robrecht erkent: dit kan enkel met grote budgetten
- 30CC beseft: ze hebben geen "website" nodig maar **organisatiesoftware** die de hele flow ondersteunt en via API's doorstuwt naar website, nieuwsbrief, narrowcasting

**De 4 stappen van een evenement (hun mentaal model):**
1. **Eventorganisatie** — Artistiek team beslist, ruimte claimen, technische behoeften
2. **Campagne** — Segmentatie opzetten, beeldmateriaal, lancering, verkoop, kortingen, servicemails
3. **Het moment zelf** — Boekhouding, contractmanagement, hospitality, vrijwilligers
4. **Dashboarding & rapportage** — Per event en per jaar: kosten, opbrengsten, ROI

**Ideaalbeeld:** Centrale softwarelaag waarin alle betrokkenen (technici, communicatie, programmatoren, boekhouding) met hun rol kunnen werken. Data wordt een keer ingevoerd en stroomt door naar alle kanalen.

### Reactie op gedeeld platform
- "Kleine CC's kunnen dit niet" (alleen betalen) — bevestigt de nood aan een deelmodel
- "Droomsoftware => workshop met 5 CC's" — er is actieve interesse om samen te werken

### Contacttypes die nu in Excel zitten (= moet allemaal in het CRM)
Genodigden events, curatoren, professionele contacten artistieke collega's, partners Rode Hond, leerkrachten, buurtfamilies, crowd-funding donateurs, dansers, amateurgezelschappen, kabinetsmedewerkers, leveranciers, pers

---

## Sectoranalyse: de Vlaamse cultuursector en CRM

### Het digitale landschap (bron: CultuurConnect-bevraging 2024, 114 organisaties)

**Ticketing (90% heeft een systeem):**
- **Ticketmatic** — Belgisch, marktleider. 67% van cultuurcentra, 61% van kunstenorganisaties. 300+ klanten. CRM zit ingebouwd maar is beperkt
- **Recreatex** (Vintia/Gantner) — tweede speler, vooral gemeentelijke context (25% gemeenschapscentra)
- **Tixly** — Zweeds, groeiend. Gekozen door CultuurConnect voor gedeelde ticketing (contract tot 2030)

**Planning (54% heeft een systeem):**
- **Yesplan** — Belgisch, 63% van cultuurcentra. 300+ venues. Sterke API

**CRM: de grote leegte**
- **Slechts 11% heeft een apart CRM-systeem.** De meeste leunen op wat Ticketmatic aanbiedt
- Dit is het gat in de markt

**Websites (97% heeft er een):**
- Tevredenheid is lager dan bij ticketing (54% vs 68%). Signaal voor verbetering

### De kernproblemen van de sector

1. **Data-fragmentatie** — ticketing, website, email, planning, boekhouding spreken niet met elkaar. #1 gevraagde verbetering in CultuurConnect-bevraging
2. **Organisaties bezitten hun eigen publieksdata niet** — historisch probleem, vooral bij touring producties
3. **Ticketing-systeem is ontoereikend als CRM** — gebouwd voor transacties, niet voor publiekswerking
4. **Gebrek aan budget, tijd en expertise** — niet alleen voor analyse maar ook voor actie (campagnes, outreach)
5. **Slechte datakwaliteit** — duplicaten, incomplete records, inconsistente invoer
6. **Geen unified view** — iemand die tickets koopt, nieuwsbrief ontvangt, website bezoekt en workshop volgt verschijnt als 4 aparte personen
7. **Te veel manueel werk** — dubbele invoer, handmatige exports
8. **Moeilijk om nieuw/divers publiek te bereiken** — zonder goede data is publieksopbouw giswerk

### Wat publiekswerking nodig heeft aan data

Subsidiegevers verwachten steeds meer. Organisaties hebben nodig:
- Demografische gegevens (leeftijd, opleiding, geografie, socio-economisch)
- Bezoekfrequentie en -patronen (nieuw vs terugkerend)
- Cross-venue gedrag (bezoekt iemand meerdere huizen?)
- Genre-voorkeur en programmeringsaffiniteit
- Digitale engagement (website, e-mail, social)
- Abonnementen/lidmaatschappen
- Diversiteitsmetrieken (culturele achtergrond, toegankelijkheid)
- Participatie buiten voorstellingen (workshops, educatief, community)

**Wat ze echt hebben:** Vooral transactiedata uit ticketverkoop. Het gat tussen ambitie en realiteit is enorm.

### Rapporteringseisen Vlaamse Overheid

- **Kunstendecreet** (5-jarige werkingssubsidies 2023-2027): Verantwoording via KIOSK-platform
- **Participatiedecreet**: Participatieve activiteiten voor breed publiek incl. kwetsbare groepen
- Verplichte registratie in **UiTdatabank** (Publiq) voor alle gesubsidieerde activiteiten
- Rapportage over publieksopbouw, diversiteit in programmering/personeel/bestuur
- **Implicatie**: CRM moet rapportage kunnen genereren die aligned is met deze overheidseisen

### GDPR in de cultuursector

- Expliciet consent management voor alle contactdata
- Recht op vergetelheid / data portabiliteit
- Cross-organisatie datadeling (gedeelde ticketing clusters) vereist zorgvuldig juridisch kader
- De Belgische GBA/APD handhaaft actief
- OSLO-standaardisering (Publiq + departement CJM) werkt aan interoperabiliteitsstandaarden binnen GDPR

---

## De digitale infrastructuur van de sector

### Drie overheidsgefinancierde pijlers

**Publiq** (voorheen CultuurNet + CJP):
- **UiTdatabank**: 28.000+ organisatoren, 215.000+ activiteiten/jaar. Het kloppend hart
- **UiTPAS**: Participatiepas, korting voor mensen met beperkt budget
- **Museumpas**: 350.000+ abonnees, 230+ musea (platform gebouwd door Statik)
- **Data exchange platform** in ontwikkeling (data mesh + OSLO-standaarden)

**CultuurConnect** (fusie Bibnet + Locus, 2016):
- 2.100+ ledenorganisaties (bibliotheken, podiumhuizen, gemeenschapscentra)
- **Gedeelde Ticketing**: 48 venues in 12 regionale clusters, via Tixly. EUR 0,35/ticket
- **Vernieuwingstraject CRM**: Actief bezig met CRM-verkenning voor de sector. Details beperkt publiek beschikbaar
- **Digitaal Podium**: Gedeelde digitale basisinfrastructuur voor 248 doelorganisaties
- Cooperatief model: stuurgroep, productgroepen, werkgroepen. Elke organisatie gelijke stem

**meemoo**:
- Digitale archivering en preservatie cultureel erfgoed

**Strategische implicatie**: CultuurConnect is al bezig met een CRM-traject. Statik's initiatief moet hier **mee alignen** of zich er duidelijk tegenover positioneren. Concurreren met de overheidsinfrastructuur is onverstandig — samenwerken is de weg.

---

## Kaaitheater: diepteanalyse

### Profiel
- Opgericht 1977 door Hugo De Greef als festival voor hedendaagse podiumkunsten
- Een van de belangrijkste kunstencentra van de Vlaamse Gemeenschap in Brussel
- Sterk verbonden met de "Flemish Wave" (De Keersmaeker, Fabre, Lauwers)
- Missie sinds 2019: "How to Be Many?" — over toegankelijkheid, agency, machtsverdeling
- Coordinatoren: Agnes Quackels en Barbara Van Lindt
- **Beheersovereenkomst voor 10 jaar** (2023-2032) — gevestigde instelling
- **Werkingssubsidie: EUR 2.764.800/jaar** (Kunstendecreet) + ~EUR 280.000 VGC + eigen inkomsten
- Geschat totaalbudget: **3,5-4,5 miljoen EUR/jaar**

### Gebouw en zalen
- Art Deco-theater uit 1932, Saincteletteplein 20. Grote zaal: ~700 plaatsen, kleine zaal: 200/400
- Kaaistudio's aan de Oude Graanmarkt (voormalige brouwerij)
- Renovatie door BULK architecten: nieuwe tweede zaal, stadsbalkon op het dak, nieuwe ingang kanaalkant

### Publiek
- ~75 producties per seizoen
- Geschat 40.000-70.000 bezoeken per seizoen (normaal)
- 45% jonger dan 35 jaar
- 32% koopt voor het eerst een ticket
- **Pay What You Can** sinds september 2022: 5 prijsniveaus (EUR 7-35+), bezoeker kiest zelf
  - Gevolg voor CRM: traditionele prijscategorieen (student, senior) bestaan niet meer als segmentatie-proxy

### Brussels context (cruciaal voor CRM-design)
- 1,2 miljoen inwoners, 62% van buitenlandse afkomst
- 200.000+ expats (EU, NATO, internationaal)
- Sterk meertalig: NL/FR/EN/DE
- Kaaitheater = Vlaamse Gemeenschap maar opereert in overwegend Franstalige stad
- Website: NL/EN (opvallend: niet NL/FR)
- Persbureaus: SERENAI (NL/EN/DE), NAKAMI (FR)
- Brussel = wereldhoofdstad hedendaagse dans (P.A.R.T.S., Rosas, Charleroi danse)

### Relatie met Rosas
- Rosas opgericht in 1983 specifiek voor het Kaaitheaterfestival
- Diepe historische band, gesprekken over "verregaande samenwerking" in 2019
- Er is nu een "Rosas Performance Space" op de locatiepagina van Kaaitheater
- Relevant voor CRM: gezelschaps- en productiedata van Rosas zal waarschijnlijk in het systeem moeten

### Communicatieteam
- Jonas Maes — Digital communication & partnerships + ICT coordination
- Mara Ittel — Digital & social content creator
- Titane Michiels — Ticketing & communication
- Social media: Facebook 22.000+ likes, Instagram ~16.000 followers

### Huidige systemen
| Systeem | Functie | Contacten |
|---------|---------|-----------|
| **Ticketmatic** | Ticketverkoop & vrijkaarten, ingebouwde CRM (beperkt) | 11.000+ |
| **Yesplan** | Planning productie & techniek, locatieplanning | 2.000+ (productie-gerelateerd) |
| **Mailchimp** | Nieuwsbrieven & direct mails | 8.000+ (opt-in) |
| **Zensoft** | Boekhouding & facturatie | 1.500+ (handmatig + e-facturatie) |
| **RStudio** | Data-analyse & visualisatie | Leest data, slaat niet op |

---

## Statik: wie zijn zij?

### Bedrijfsprofiel
- Digitaal bureau in Leuven, opgericht 2006 door **Pieter Jelle De Brue** (CEO)
- Mede-eigenaar: **David Pinte**
- ~30 FTE: 4 strategen, 12 developers/analisten, 4 UX/UI, 5 content/marketing, 1 videograaf, 4 PM's
- Zelfsturende teams van 5-8 personen sinds 2012
- **B Corp gecertificeerd** sinds 2021
- Evolueert naar **steward-ownership** (eigenaarschap blijft bij de missie, niet bij investeerders)
- Omzet: ~EUR 1,5-1,6M/jaar
- Tech stack: **Laravel + Vue.js**, Ionic voor mobile, AWS hosting
- Sinds 2016 exclusief werken met organisaties die balanceren tussen winst en positieve impact

### Track record cultuur
- **Museumpas** (voor Publiq): 350.000 abonnees, 230+ musea. Laravel + Vue.js. Conversie van 84% naar 98,5%. Genomineerd IT/Digital Project of the Year
- Blog claimt **30+ culturele partners**
- Integraties met Ticketmatic, SRO, UiTdatabank
- Specifieke projecten als STUK, CC Strombeek, Passa Porta, Het Depot worden in het concept-deck genoemd maar zijn niet publiek zichtbaar op hun portfolio

### Let op
- De claim dat Statik Opvang.Vlaanderen bouwde is **niet publiek verifieerbaar** — het staat niet op hun portfolio
- "Collega Anton" en "Dylan" zijn niet vindbaar in publieke Statik-profielen
- Er zijn geen publieke referenties naar een "gedeeld CRM"-initiatief van Statik voor cultuur

---

## Concurrentielandschap

### Wie gaat er op de Kaaitheater RFP inschrijven?

**Ticketmatic zelf** — De olifant in de kamer. Ze hebben 67% marktaandeel en breiden hun CRM-functionaliteit uit. Ze kunnen argumenteren: "je hebt al onze data, waarom een extra systeem?"

**Belgische digitale bureaus met cultuurervaring:**
- Little Miss Robot (Antwerpen) — UX-driven digitaal productdesign
- Code d'Or (Gent) — webbureau, heeft met Yesplan gewerkt
- Starring Jane — gespecialiseerd in ledenorganisaties

**Platform-leveranciers:**
- Tixly/Tix Benelux — al partner van CultuurConnect
- ACA Group — technologiepartner van Publiq voor data exchange platform

**Internationale spelers:**
- Spektrix (UK) — cloud-based, ticketing + CRM + fundraising + marketing. 600+ organisaties. Sterk in UK/Ierland, niet significant in Belgie/Benelux. Zou kunnen willen expanderen
- Tessitura — enterprise-grade, voor grote instellingen (Met Opera, National Theatre London). Complex, duur
- PatronManager — gebouwd op Salesforce, CRM + ticketing + fundraising
- Peppered/CultureSuite — CMS specifiek voor cultuur, integreert met Tixly en Spektrix

**Open source:**
- CiviCRM — 14.000+ nonprofits, 30+ talen. Gratis maar vereist technische expertise

### Statik's concurrentievoordelen
1. Enige partij die een **gedeeld/cooperatief model** voorstelt (niet alleen voor Kaaitheater maar voor de sector)
2. Diepe relatie met **Publiq** (Museumpas-platform)
3. **B Corp + steward-ownership** traject sluit aan bij waarden cultuursector
4. Kennis van sector-terminologie en werkprocessen
5. **Future-proofing** argument: Kaaitheater betaalt voor iets dat steeds beter wordt naarmate meer huizen instappen

### Statik's kwetsbaarheden
1. **Nog geen bestaand CRM-product** — ze moeten van nul bouwen terwijl anderen al werkende systemen hebben
2. **Ticketmatic kan bundelen** — "blijf bij ons, we bouwen het CRM erbij" is een sterk argument
3. **CultuurConnect's eigen CRM-traject** — als de overheid dit al faciliteert, wat is Statik's rol?
4. **Klein bureau** (~30 FTE, EUR 1,5M omzet) voor een ambitieus sectorbreed platform
5. **Opvang.Vlaanderen-referentie niet verifieerbaar**

---

## Internationale benchmarks

### UK (meest geavanceerd in arts CRM)
- **Arts Council England's Illuminate** (met PwC): gratis publieksdata-platform voor alle gefinancierde organisaties. Verplicht voor rapportage
- **The Audience Agency's Audience Finder**: data van 800+ organisaties, 170 miljoen tickets, 59 miljoen transacties
- **Audience Spectrum**: segmenteert de hele UK-bevolking in 10 profielen op basis van culturele attitudes. Integreert met CRM-systemen

### Trends (2025-2026)
1. **Platform consolidatie** — van best-of-breed naar geintegreerde platformen
2. **AI-gestuurde personalisatie** — gepersonaliseerde communicatie is de verwachting, geen differentiator
3. **CRM als strategische functie** — geleid vanuit de top, niet alleen marketing
4. **Cross-venue datadeling** — UK en Vlaanderen bewegen beide naar sectorbreed data-ecosysteem
5. **First-party data prioriteit** — met cookie-deprecatie en privacy-regulering wordt eigen publieksdata essentieel
6. **Predictive analytics** — at-risk abonnees identificeren, no-shows voorspellen, prijsoptimalisatie
7. **Toegankelijkheid en inclusie** — data-driven benadering van ondervertegenwoordigd publiek
8. **Real-time dashboards** — van jaarlijkse rapportage naar live inzichten
9. **AI-assisted marketing** — geautomatiseerde campagne-optimalisatie, contentgeneratie
10. **Mobile-first** — apps, mobiele tickets, in-venue digitale ervaringen

---

## Functionele vereisten Kaaitheater (5 categorieen, MoSCoW)

De requirements staan in een apart Excel-document ("Functionele requirements_RFP_CRM_Kaaitheater"), maar de hoofdcategorieen zijn:

### 1. Publiek: Registratie, voorkeuren & privacy
- Publieksgericht contactbeheer
- Voorkeurenbeheer (welke communicatie wil iemand ontvangen?)
- GDPR-compliance, consent tracking

### 2. Contactbeheer: Aanmaak, beheer & synchronisatie
- Centrale contactdatabase, deduplicatie/merge
- Synchronisatie met Yesplan, Ticketmatic, Mailchimp, Zensoft
- Contacten een keer aanpassen = overal up-to-date

### 3. Communicatie & e-mailcampagnes
- Gerichte campagnes vanuit het CRM
- Segmentatie-gestuurde doelgroepen
- Mogelijk vervanging van Mailchimp

### 4. Segmentatie, analyse & dashboards
- Cross-systeem data ("welke tickethouders kregen ook een nieuwsbrief?")
- Rapportage voor beleidsvragen (publieksopbouw, participatie, inclusie, diversiteit)
- Dashboards per gebruikersprofiel
- Rapportage-export aligned met KIOSK/Kunstendecreet

### 5. Beveiliging & toegangsbeheer
- Rolgebaseerde toegang per team
- Vertrouwelijkheid contactdata, GDPR

---

## Niet-functionele vereisten (ISO 25010)

- **Interoperabiliteit**: real-time data-uitwisseling, makkelijk exporteerbaar
- **Beschikbaarheid**: altijd beschikbaar
- **Vertrouwelijkheid**: alleen geautoriseerden
- **Wijzigbaarheid**: Kaaitheater moet zelf aanpassingen doen zonder IT-kennis
- **Effectiviteit & efficientie**: snel en nauwkeurig doelen behalen
- **Flexibiliteit**: bruikbaar in niet-initieel gespecificeerde contexten

---

## Evaluatiecriteria Kaaitheater

1. Kwaliteit van het voorstel
2. Projectplan
3. Timing
4. Kwaliteit diensten (projectbeheer, advies, opleiding)
5. Kwaliteit software
6. Kwaliteit leverancier (cases, track record)
7. Ondersteuning en onderhoud
8. Kwaliteit hosting en back-up
9. Gebruiksvriendelijkheid
10. Budget
11. Future proofing

---

## Wat Kaaitheater in de offerte verwacht

1. Info over het bedrijf (ervaring, certificeringen, demo)
2. Visie op de samenwerking
3. Visie op het project (testperiode, training, opleiding)
4. Minimaal 3 cases (samenvatting, timing, budget, contactpersoon)
5. Projectplan met overzicht requirements
6. Profielen (type en aantal ingezet)
7. Budget (eenmalig + terugkerend + licentiekosten)
8. Timing (doorlooptijd en prestatietijd per profiel)
9. Ondersteuning (eerste/tweede lijn, ticketing, reactietijd, een aanspreekpunt)
10. Beeindiging van contracten

---

## Feature-architectuur

### Kernprincipe: de productie als ruggengraat

Dit is geen CRM. Dit is **organisatiesoftware voor de cultuursector.** Het verschil: een CRM denkt vanuit het contact. Organisatiesoftware denkt vanuit de **productie** — het evenement is het middelpunt, en alle contacten, campagnes, financien en rapportage hangen eraan vast.

De architectuur volgt het 4-stappenmodel uit het 30CC-interview:

#### Stap 1: Programmatie & planning
Een artistiek team beslist: we programmeren X op datum Y. Vanaf dat moment bestaat er een **productiedossier** in het systeem waar alles aan vasthangt. Niet als Yesplan-kopie, maar als de plek waar alle informatie samenkomt.

Features:
- Productiedossier als centraal object (trekt data uit Yesplan: zaal, data, gezelschap, technische behoeften)
- Gezelschapsprofiel met historiek ("Needcompany speelde hier 4x, laatste keer 380 tickets verkocht")
- Castinglijst en technische contacten gekoppeld aan de productie
- Beeldmateriaal en persdossier gekoppeld (bron voor campagnes, website, narrowcasting)
- Ruimte- en middelenplanning zichtbaar (read-only uit Yesplan)

#### Stap 2: Campagne & verkoop
Zodra de productie bestaat, kan communicatie ermee aan de slag. Niet "maak een segment en exporteer naar Mailchimp", maar direct vanuit het productiedossier.

Features:
- Campagne-builder gekoppeld aan productie (niet losse mailings, maar een campagneplan per productie)
- Automatische segmentsuggestie op basis van productie-profiel ("hedendaagse dans, internationaal gezelschap → dit segment, verwachte respons 4,2%")
- Verkooptracking: hoeveel tickets zijn er al, hoe verloopt de curve, moet er bijgestuurd worden?
- Servicemails per productie (bevestiging, herinnering, locatie-info, nazorg)
- Funnel tracking: nieuwsbrief geopend → website bezocht → ticket bekeken → ticket gekocht (of afgehaakt — precies wat 30CC mist)

#### Stap 3: Het moment zelf
De avond van de voorstelling.

Features:
- Gastenlijst / hospitality (VIP, pers, partners, genodigden — nu Excel-tabbladen bij 30CC)
- Vrijwilligersplanning gekoppeld aan productie
- No-show tracking (wie had een ticket maar kwam niet?)
- Horeca-/sponsorafspraken per productie
- Real-time bezettingsgraad

#### Stap 4: Evaluatie & rapportage
Per productie, per seizoen, per jaar — en aligned met subsidie-eisen.

Features:
- Per-productie dashboard: tickets verkocht, campagne-resultaten, kosten, opbrengsten, ROI
- Per-seizoen overzicht: publieksevolutie, genre-verdeling, nieuw vs terugkerend publiek
- Kunstendecreet-rapportage: diversiteitsmetrieken, bereik, participatie (export naar KIOSK)
- Benchmarking binnen het gedeelde platform (geanonimiseerd): "onze open rate voor dans is 38%, sector-gemiddelde is 28%"
- Vergelijking met vorig seizoen / vorig jaar

---

### Module 1: Contactbeheer — niet een contact, maar een relatie

#### Rollen in plaats van types
Een persoon is vaak meerdere dingen tegelijk in de cultuursector:
- Een curator die ook bezoeker is die ook partner is bij een festival
- Een artiest die ook buurtbewoner is die ook vrijwilliger was
- Een journalist die ook trouwe bezoeker is

Het contactprofiel werkt met **meerdere rollen per contact**. Elke rol heeft eigen context. De contacttypes uit 30CC's Excel-tabbladen worden rollen:

**Publieksrollen:** Bezoeker, abonnee, nieuwsbrieflezer, deelnemer (workshop/educatief), donor/crowd-funder
**Professionele rollen:** Artiest, gezelschap (organisatie), curator, programmator (extern), technicus (freelance)
**Partnerrollen:** Coproducent, gastlocatie, sponsor, subsidiegever, leverancier, horeca-partner
**Communicatierollen:** Pers/journalist (per medium, per taal), influencer, blogger
**Interne rollen:** Vrijwilliger, stagiair, buurtfamilie, leerkracht, kabinetsmedewerker, amateurgezelschap

#### Unified profiel
Een contactprofiel toont alles over een persoon, ongeacht de bron:
- Contactgegevens (met bronvermelding: "e-mail via Ticketmatic, adres via Zensoft")
- Alle rollen en de context per rol
- Volledige tijdlijn: tickets, mails, notities, producties waar betrokken, hospitalitylijsten, ontmoetingen
- Relatie met organisatie (bv. "contactpersoon bij Needcompany")
- Consent-status per kanaal (nieuwsbrief: opt-in sinds X, promo: geen consent)
- "Wie kent deze persoon?" — welke collega heeft het meeste contact gehad

#### Kennisbehoud
Het "vertrekkend personeel = kennisverlies"-probleem (30CC) oplossen:
- Notities en relatiegeschiedenis vastleggen bij het contact, niet in de inbox van een medewerker
- "Contact-eigenaar" toewijzen (wie is het aanspreekpunt?)
- **Vertrek-workflow**: als een medewerker de organisatie verlaat, triggered het systeem: welke contacten beheerde deze persoon? Welke relaties moeten overgedragen worden?

#### Deduplicatie
- Real-time bij sync, niet achteraf. Fuzzy matching op naam + email + adres
- Review-queue voor twijfelgevallen
- Merge met audit trail (welke brondata werd samengevoegd)
- Conflict resolution: als Ticketmatic en Zensoft een ander adres hebben, welke wint?

---

### Module 2: Segmentatie — de taal van de sector

#### Gedragsgebaseerde segmentatie
- Genre-affiniteit: bezoekers die >3 dansvoorstellingen zagen maar nooit theater
- Seizoensgedrag: mensen die altijd op de seizoensopening komen maar daarna afhaken
- Boekingspatroon: bezoekers die steeds later boeken (impulsief) vs vroege planners
- No-show patroon: mensen die tickets kopen maar niet komen
- Frequentie-verandering: trouwe bezoekers waarvan de frequentie daalt (churn-risico)

#### Engagement-gebaseerde segmentatie
- Cross-kanaal: nieuwsbrief geopend + ticket gekocht = engaged. Nooit geopend maar toch tickets = ander kanaal nodig
- Funnel drop-off: website bezocht maar niet gekocht (precies wat 30CC mist aan Ticketmatic)
- Campagne-respons: welke boodschap/beeldtaal werkt voor welk segment?
- Social media engagement dat nog niet vertaald is in bezoek

#### Relatie-gebaseerde segmentatie
- Alle contacten van gezelschap X (voor wanneer ze terugkomen)
- Perscontacten die over dans schrijven (niet over theater)
- Partners die al 3 seizoenen meedoen vs nieuwe partners
- Buurtbewoners (relevant voor community-programma's)

#### Beleidsgebaseerde segmentatie (subsidie-rapportage)
- Leeftijdsspreiding van het publiek
- Geografische herkomst (lokaal/regionaal/internationaal, postcodegebieden)
- Eerste bezoek vs terugkerend (publieksvernieuwing)
- Diversiteitsmetrieken (culturele achtergrond, toegankelijkheidsnoden)
- Participatie buiten voorstellingen (workshops, educatief, community)

#### Pay What You Can-segmentatie (Kaaitheater-specifiek)
- Welk prijsniveau kiezen mensen? Verschuift dat over tijd?
- Correlatie gekozen prijs / bezoekfrequentie
- Structureel laagste niveau + frequent bezoek = heel ander profiel dan eenmalig hoogste niveau
- Prijskeuze als engagement-indicator

#### Segmentatie-builder UX
- Visuele builder: regels combineren met EN/OF
- Live preview: hoeveel contacten vallen in dit segment?
- Opslaan als dynamisch segment (update automatisch) of statisch (snapshot)
- Kant-en-klare recepten: "Trouwe bezoekers die dreigen af te haken", "Nieuwsbriefabonnees die nooit een ticket kochten", "Pers dansrecensenten NL-talig"

---

### Module 3: Campagnes — van Mailchimp naar eigen kanaal

#### Waarom eigen campagnemodule?
30CC's pijn: segmentatie in Ticketmatic, export naar Mailchimp, campagne bouwen in Mailchimp, resultaten handmatig terugkoppelen. Dat is 4 systemen voor 1 mail. De campagnemodule moet dit in 1 flow doen.

Features:
- E-mail builder (templates per type: seizoensbrochure, voorstellingsherinnering, servicemail, persuitnodiging)
- Direct vanuit segment versturen, geen export nodig
- A/B-testing (onderwerpregel, verzendtijdstip, beeldmateriaal) — wat 30CC mist sinds Spotler
- Automatische servicemails per productie (bevestiging, herinnering, locatie-info, nabeschouwing)
- Campaign-to-ticket tracking: hoeveel tickets zijn er verkocht dankzij deze campagne? (De heilige graal die nu nergens bestaat)
- Open rate, click rate, unsubscribe per campagne EN per segment
- Drip campaigns / automation: "als iemand voor het eerst een ticket koopt, stuur na 3 dagen een welkomstmail"

---

### Module 4: Dashboards & rapportage

#### Per gebruikersprofiel
Niet iedereen ziet hetzelfde dashboard:
- **Programmator**: welke genres trekken publiek, welke gezelschappen scoren goed, nieuw vs terugkerend publiek per type
- **Communicatie**: campagne-resultaten, engagement metrics, segment-groei, funnel performance
- **Ticketing**: verkoopsnelheid per productie, bezettingsgraden, no-shows, Pay What You Can-verdeling
- **Directie**: seizoensoverzicht, publieksevolutie, diversiteitsmetrieken, benchmarking
- **Productie**: gastenlijsten, hospitalityplanning, vrijwilligers per evenement

#### Subsidie-rapportage
- One-click Kunstendecreet-export (bereik, diversiteit, participatie)
- UiTdatabank-synchronisatie (verplicht voor gesubsidieerde activiteiten)
- KIOSK-compatible output
- Vergelijking met beleidsdoelen ("we mikten op 30% nieuw publiek, we zitten op 28%")

#### Sector-benchmarks (deelmodel)
- Geanonimiseerde vergelijking met andere deelnemende huizen
- "Onze open rate voor dansnieuwsbrieven is 42%, sector-gemiddelde is 28%"
- "Onze no-show rate is 8%, vergelijkbare huizen zitten op 12%"
- Naar het model van UK's Audience Agency maar dan voor Vlaanderen

---

### Module 5: Sync-engine — het technische hart

#### Integraties (prioriteit)
1. **Ticketmatic API** — Core. Ticketverkoop, bezoekerdata, vrijkaarten, aankoophistoriek. Bi-directioneel: contactwijzigingen in CRM syncen terug
2. **Yesplan API** — Productiedata, zaalplanning, gezelschapscontacten. Lezen + productiedossier voeden
3. **Mailchimp API** (fase 1, vervangen in fase 2) — Mailinglijsten, campagnedata, open/click tracking
4. **Zensoft** — Boekhoudkundige contacten. API-beschikbaarheid onzeker, waarschijnlijk CSV import/export
5. **UiTdatabank API** (Publiq) — Verplicht voor gesubsidieerde activiteiten
6. **OSLO-standaarden** — Interoperabiliteit met toekomstige sectorinfrastructuur
7. **Prezly** (30CC-specifiek, maar relevant voor sector) — Perslijstbeheer en persbericht-tracking
8. **Website / CMS** — Formulierinschrijvingen, nieuwsbriefaanmeldingen, websitegedrag (voor funnel tracking)
9. **Social media API's** — Facebook, Instagram engagement data koppelen aan contactprofielen
10. **Narrowcasting** — Content-feed vanuit productiedossier naar foyer-schermen

#### Sync-principes
- Bi-directioneel waar mogelijk (contact wijzigen in CRM = wijzigt in Ticketmatic)
- Conflict resolution met duidelijke regels per veld ("meest recente wint" of "bron X heeft prioriteit")
- Audit trail: wie wijzigde wat, wanneer, vanuit welk systeem
- Real-time sync voor kritieke data (ticketverkoop), batch-sync voor minder urgent (boekhouding)
- Foutafhandeling met notificaties ("sync met Zensoft gefaald, 12 contacten niet bijgewerkt")

---

### Module 6: Consent management (GDPR)

Het 30CC-interview maakt duidelijk dat GDPR een dagelijkse realiteit is, niet een checkbox:
- Stadsjuristen bepaalden dat 30CC geen promo mag sturen op basis van aankoop, enkel bij expliciet nieuwsbriefconsent
- Dit verschilt per organisatie (stedelijke VZW vs private VZW)

Features:
- Granulaire consent per doel: nieuwsbrief, promo, servicemail, persuitnodiging, uitnodiging events
- Consent per kanaal: e-mail, telefoon, post, SMS
- Consent-historie met timestamp en bron ("opt-in via website op 12/01/2023")
- Automatische consent-vervaldata met re-opt-in campagnes
- "Recht op vergetelheid"-workflow: contact verwijderen uit alle systemen met audit trail
- Organisatie-specifieke consent-regels (stedelijke VZW = strenger dan private VZW) via feature toggles

---

### Module 7: Toegangsbeheer

Rolgebaseerde toegang afgestemd op hoe cultuurhuizen werken:

| Rol | Ziet | Kan doen |
|-----|------|----------|
| **Communicatie** | Alle contacten, campagnes, segmenten, dashboards | Campagnes versturen, segmenten maken, contacten bewerken |
| **Ticketing** | Bezoekers, verkoopdata, gastenlijsten | Contacten bewerken, vrijkaarten toewijzen, rapportage |
| **Productie** | Gezelschappen, artiesten, leveranciers, technische contacten | Contacten bewerken, hospitality beheren |
| **Programmatie** | Productieprofiel, publieksdata per genre, gezelschapshistoriek | Lezen, notities toevoegen |
| **Directie** | Alles, dashboards, benchmarks | Lezen, rapportage exporteren |
| **Admin** | Alles | Alles, inclusief instellingen, integraties, gebruikersbeheer |

---

### Deelmodel-specifieke features

Features die alleen bestaan omdat meerdere huizen hetzelfde platform delen:

1. **Sector-benchmarks** — Geanonimiseerde vergelijking op open rates, no-shows, publieksvernieuwing, bezettingsgraden. Naar het model van UK's Audience Agency
2. **Gedeelde templates** — Campagne-templates, segmentatie-recepten, rapportage-templates die werken voor de sector. Een nieuw huis start niet van nul
3. **Cross-venue inzichten** (met consent) — Gaat iemand die bij Kaaitheater dans kijkt ook naar STUK of deSingel? Goud voor programmatie en publiekswerking
4. **Gedeelde feature-ontwikkeling** — Kaaitheater's Pay What You Can-module wordt beschikbaar voor iedereen. 30CC's festivalmodule profiteert de hele sector
5. **Collectieve onderhandeling** — Als 20 huizen hetzelfde platform gebruiken, heb je meer leverage bij integratie-partners (Ticketmatic, Yesplan)
6. **Gedeeld leernetwerk** — Best practices uitwisselen: welke campagne-aanpak werkt het beste voor hedendaagse dans? Welke segmentatiestrategie vernieuwt het publiek het snelst?

---

### Innovatie-features (toekomst, maar meenemen in architectuur)

#### AI-gestuurde suggesties
- "Op basis van het profiel van deze productie en je historische data: dit is het aanbevolen segment, verwachte respons: 4,2%"
- Automatische genre-classificatie op basis van productie-omschrijving
- "Bezoekers die op artiest X kwamen, zouden artiest Y ook interessant vinden" (collaborative filtering)

#### Predictive churn
- Trouwe bezoekers die stilletjes afhaken: bezoekfrequentie daalt, mails worden minder geopend
- Automatisch signaleren voordat ze weg zijn
- Trigger: re-engagement campagne met persoonlijke aanbieding

#### Slimme deduplicatie
- Real-time bij sync, fuzzy matching, ML-getraind op culturele naampatronen (tweetalig, internationale namen)
- Suggesties: "Marie Vandenberghe (Ticketmatic) en M. Vandenberge (Mailchimp) zijn waarschijnlijk dezelfde persoon"

#### Prompt-based rapportage
- "Hoeveel nieuwe bezoekers hadden we dit seizoen bij dansvoorstellingen?"
- "Vergelijk de campagne-resultaten van de seizoensbrochure met vorig jaar"
- Natural language query op de dataset, resultaat als dashboard

#### Narrowcasting-feed
- Automatische content-feed vanuit productiedossier naar foyer-schermen
- "Vanavond in de grote zaal: [titel], [gezelschap], [beeld]"
- Dynamisch: past aan op basis van wat er die dag geprogrammeerd staat

#### Consent-lifecycle
- GDPR-consent verloopt. Automatische re-opt-in campagnes
- Granulaire consent-configuratie per organisatie (stedelijke VZW = strenger)
- Dashboard: "X% van je contacten heeft verlopend consent in de komende 3 maanden"

---

### Multi-tenant architectuur

- Een codebase, meerdere organisaties
- Feature toggles per organisatie (modules aan/uit, velden aan/uit)
- Organisatie-specifieke configuratie:
  - Terminologie (aanpasbaar per huis)
  - Velden en contactrollen (uitbreidbaar)
  - Integraties (welke systemen gekoppeld)
  - Taal (NL/FR/EN per organisatie)
  - Consent-regels (stedelijk vs privaat)
  - Branding (logo, kleuren in campagne-templates)
- Licentie op basis van organisatiegrootte (democratiserend: klein betaalt minder)
- Data strikt gescheiden per organisatie (behalve opt-in sector-benchmarks)

---

### Wat Ticketmatic niet kan (en dit platform wel)

Dit is cruciaal — het platform concurreert niet met Ticketmatic, het vult aan. Maar het gat moet helder zijn:

1. **Funnel tracking voorbij de ticketknop** — Ticketmatic ziet: iemand kocht. Het ziet niet: nieuwsbrief geopend → website bezocht → productie 3x bekeken → dan pas gekocht. Dat hele pad is onzichtbaar
2. **Professionele contacten** — Ticketmatic is voor ticketkopers. Gezelschappen, pers, leveranciers, curatoren, vrijwilligers zitten er niet in
3. **Cross-systeem inzichten** — "Welke nieuwsbriefabonnees kochten nog nooit een ticket?" vereist Mailchimp + Ticketmatic data
4. **Per-productie lifecycle** — Kosten, opbrengsten, campagnes, hospitality: alles gekoppeld aan een productie
5. **GDPR-compliant relatiebeheer** — Consent per kanaal, per doel, met vervaldata
6. **Kennisbehoud** — Notities, relatiegeschiedenis, context die niet verloren gaat als iemand vertrekt
7. **A/B-testing** — 30CC had dit bij Spotler, mist het nu enorm
8. **Sector-benchmarks** — Vergelijking met peers, bestaat nergens

---

## Belangrijke data

| Wat | Wanneer |
|-----|---------|
| Deadline offerte | 31/08/2025 |
| Voorstel presentatie | September 2025 (demo-moment) |
| Start project | Najaar 2025 |
| Lancering Kaaitheater | 01/09/2026 |
| Heropening gebouw Saincteletteplein | September 2027 |

De lancering 1 jaar voor de heropening is strategisch: systeem is ingewerkt tegen het moment dat het publiek terugkomt naar het nieuwe gebouw.

---

## Bestandslocaties

- Concept deck (Statik): `/Users/antonaerts/Downloads/Een gedeeld CRM (4).pdf`
- RFP Kaaitheater: `/Users/antonaerts/Downloads/RFP_CRM_Kaaitheater (2).pdf`
- Interview 30CC (Robrecht): `/Users/antonaerts/Downloads/Interviews CRM (1).pdf`
- Functionele requirements Excel: apart document ("Functionele requirements_RFP_CRM_Kaaitheater") — nog niet beschikbaar
- Offerte-template: bijlage in RFP ("offerte_CRM_Kaaitheater") — in te vullen door leverancier
- Prototype: `/Users/antonaerts/Claude Code/gedeeld-crm-cultuursector/prototype/index.html`

---

## Ontwikkelrichtlijnen

- **Taal UI**: Nederlands (primair), Frans en Engels (must-have voor Brussels context)
- **Design**: Strak, visueel, logisch — cultuursector verdient schoonheid, geen enterprise-grijs
- **Toegankelijkheid**: WCAG 2.1 AA minimum (expliciet gevraagd in concept-deck)
- **Terminologie**: Cultuursector-taal, niet generiek CRM
  - "Bezoekers" ipv "Leads"
  - "Producties" ipv "Deals"
  - "Gezelschappen" ipv "Accounts"
  - "Seizoen" ipv "Fiscal Year"
  - "Publiekswerking" ipv "Marketing"
  - "Deelnemers" ipv "Attendees"
- **Modulariteit**: Alles via toggles. Wat je niet gebruikt, zie je niet
- **No vendor lock-in**: Data altijd exporteerbaar
- **Interoperabel**: Aligned met OSLO-standaarden en UiTdatabank

---

## Strategische aandachtspunten

1. **CultuurConnect alignment** — Zij hebben een eigen CRM-vernieuwingstraject. Statik moet hier partner zijn, niet concurrent. Ideaal: Statik bouwt het platform, CultuurConnect faciliteert de governance en het cooperatieve model
2. **Ticketmatic als concurrent en partner** — Het CRM moet naadloos met Ticketmatic integreren, niet proberen het te vervangen. Ticketmatic vervangt = 67% van de sector meteen afhaken
3. **De RFP is voor Kaaitheater, het verhaal is voor de sector** — De offerte moet Kaaitheater overtuigen dat zij een werkend systeem krijgen op 01/09/2026. Het deelmodel is de architectuur-keuze die het betaalbaar en toekomstbestendig maakt
4. **Steward-ownership concreet maken** — Het concept-deck laat dit open. In de offerte moeten minstens 2-3 scenario's staan (vzw, cooperatie, steward-owned vennootschap) met voor/nadelen
5. **Brussels meertaligheid** — NL/FR/EN is geen nice-to-have maar een must. 62% van Brussel is van buitenlandse afkomst
6. **Pay What You Can** — Het systeem moet anders segmenteren dan op basis van ticketcategorie. Dit is een unieke Kaaitheater-eis die laat zien dat je hun werking begrijpt
