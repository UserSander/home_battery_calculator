
Vraag jij je ook af of het al rendabel is om een thuis batterij aan te schafen?
Ik ook! daarom heb ik deze tool gemaakt. hopelijk heb jij er ook wat aan..

hieronder staat hoe je deze moet gebruiken.

# Energie Calculator - README

Gemaakt voor: iedereen die nadenkt over een Tesla 18650 thuisbatterij, zonnepanelen, en/of een elektrische auto op een dynamisch stroomcontract.

---

## Wat doet deze tool?

Je vult je eigen situatie in en de calculator laat je zien wat je per jaar kwijt bent aan stroom, in vier scenario's naast elkaar. Van het slechtste geval (huidig contract, auto 's avonds laden) tot het beste (dynamisch contract, thuisbatterij, auto 's nachts laden). Alles herrekent live. Onderaan staat een break-even grafiek die laat zien wanneer de investering terugverdiend is, inclusief het effect van celdegradatie over de jaren.

---

## Hoe gebruik je het?

**Sliders:** sleep om een waarde in te stellen.

**Getallen direct intypen:** klik op de groene waarde naast een slider. Die verandert in een invoerveld. Type je getal, druk Enter of klik ergens anders. De slider volgt mee. Met Escape annuleer je. Je kunt buiten het slider-bereik typen voor extreme waarden.

**Batterij-presets:** klik op een van de vier systeemkaartjes. Die vult automatisch de batterijsliders in. Pas je daarna een slider aan, dan springt de selectie naar "Aangepast".

**Leveranciersdropdown:** kies je leverancier en het contracttype wordt automatisch meegenomen. De tariefsliders worden direct ingevuld op basis van het modelcontract van april 2026.

---

## Situatie-toggles

**Elektrische auto: ja/nee**
Zet je dit op nee, dan verdwijnen alle auto-rijen uit de berekening. De derde KPI-kaart schakelt om naar "eigen zonnestroom benut".

**Salderingsregeling: actief / vervallen**
De belangrijkste schakelaar voor 2027. Bij "actief" telt teruggeleverde zonnestroom mee tegen je volledige stroomtarief. Bij "vervallen" (na 1 januari 2027) krijg je alleen nog de lage terugleververgoeding, vaak €0,06-0,10/kWh. Je ziet het effect direct in alle jaarcijfers.

**Netcongestie: ja/nee**
Als jouw netbeheerder teruglevering blokkeert door congestie, telt teruggeleverde stroom op €0,00. Dit klinkt slecht, maar het vergroot het voordeel van een batterij fors: al die zon die je anders kwijtraakt kun je nu zelf opslaan en later gebruiken. Bij "ja" verschijnt een rode banner en worden de batterijbesparingen automatisch hoger berekend. Check bij Liander of Stedin of jouw postcodegebied onder congestie valt.

---

## Energiecontract

**Type contract: Vast / Variabel / Dynamisch**
Dit bepaalt hoe scenario A (jouw huidige situatie) berekend wordt. Bij vast en variabel betaal je één tarief voor alle uren. Bij dynamisch wisselt de prijs elk uur en heeft de batterij meer arbitrage-waarde omdat het verschil tussen goedkope en dure uren groot is. De dropdown filtert automatisch op het gekozen contracttype.

**Leverancier kiezen**
44 leveranciers beschikbaar, ingedeeld in dynamisch, variabel en vast (1, 2 en 3 jaar). Na selectie worden de tariefsliders ingevuld en verschijnt een banner met wat er geladen is en de bron. Tarieven zijn gebaseerd op modelcontracten van allecijfers.nl, bijgewerkt april 2026. Check je eigen contract voor de actuele waarden.

---

## Huishouden

**Jaarverbruik huis**
Meer verbruik = groter absoluut voordeel van een batterij. Warmtepomp-huishouden zit al snel op 5.000-7.000 kWh/jaar.

**Zonnepanelen capaciteit (kWp)**
Meer panelen = meer opwek = meer te besparen. Maar: meer panelen vragen ook om een grotere batterij om die opwek nuttig te benutten. Die twee hangen sterk samen.

**Opbrengst per kWp**
NL gemiddeld 875-920 kWh/kWp/jaar. Arnhem/Gelderland: ~900. Oost-west opstelling of gedeeltelijke schaduw: reken op 750-830.

---

## Tarieven

**Tarief incl. btw + EB**
Je all-in prijs bij een vast of variabel contract. Gemiddeld NL 2026: ~€0,24-0,27/kWh.

**Dagpiek (17-21u)**
De duurste uren op een dynamisch contract. De batterij vermijdt dit.

**Nacht (01-06u)**
De goedkoopste uren. Hier laad je de batterij en de auto. Het verschil tussen dagpiek en nachtprijs is de motor van de hele businesscase.

**Terugleververgoeding**
Wat je krijgt per kWh na 2027. Verplicht minimaal 50% van het kale leveringstarief, in de praktijk ~€0,06-0,10/kWh.

---

## Elektrische auto

**Kilometers per jaar**
Meer rijden = meer laadstroom = groter voordeel van nachtladen. Dit is vaak de grootste enkelvoudige besparing.

**Verbruik (kWh/100km)**
Model X praktijk: ~22 kWh/100km. Model 3: ~16-18.

**Laadverlies AC**
Bij thuisladen via wallbox gaat 8-12% verloren als warmte. Dit verhoogt de werkelijke laadstroom ten opzichte van werkelijk rijverbruik.

> Model X ondersteunt geen V2H. Stroom gaat altijd één kant op: net of batterij naar auto.

---

## Thuisbatterij

**Batterij-presets**

| Systeem | kWh | Investering | Verlies | Cycli/jr |
|---|---|---|---|---|
| Tesla 18650 DIY | 20 | €3.500 | 10% | 280 |
| Tesla Powerwall 3 | 13,5 | €9.500 | 7% | 365 |
| Huawei LUNA2000 | 15 | €5.800 | 8% | 330 |
| Victron + Pylontech | 14,4 | €4.200 | 9% | 310 |

**Bruikbare capaciteit**
Hoeveel kWh je daadwerkelijk in en uit kunt halen. Bij de Tesla 18650 DIY reken je met een SoC-venster van 10-90% om cellen te ontzien.

**Investering totaal**
Alle materiaalkosten: pakket, BMS, omvormer, behuizing, bekabeling, installatie. Je kunt boven het slider-maximum typen.

**Round-trip verlies**
Elk laad/ontlaad-cyclus gaat wat verloren. Bij 10%: laad je 10 kWh in, haal je er 9 kWh uit.

**Laadcycli per jaar**
Hoe vaak de batterij per jaar volledig cyclt. 280 is realistisch voor een actief gestuurd systeem.

**Celdegradatie per jaar**
Hoeveel capaciteit de batterij jaarlijks verliest. Tesla 18650-cellen: realistisch 2-3%/jaar. Na 10 jaar bij 2,5%/jaar heb je nog ~78% van de startcapaciteit. De terugverdientijd met degradatie is altijd langer dan zonder, en die "met degradatie" is de eerlijke waarde.

**Max. teruglevering net (kW)**
Sommige netbeheerders beperken hoeveel vermogen je terug mag leveren. Schuif naar links om een limiet in te stellen. Op 15 kW staat de slider op "onbeperkt".

---

## De vier scenario's

| | Wat het betekent |
|---|---|
| **A** | Jouw huidige contract, auto 's avonds laden. Dit is de referentie. |
| **B** | Dynamisch contract, geen actieve sturing. Je profiteert iets van lagere nachttarieven. |
| **C** | Dynamisch + bewust 's nachts laden tussen 01:00-06:00. Geen investering nodig, alleen een laadschema instellen in de Tesla-app of Home Assistant. |
| **D** | Dynamisch + thuisbatterij + nachtladen. De optimale situatie. |

Het verschil tussen A en D is je maximale besparing. De terugverdientijd van de batterij is de investering gedeeld door wat de batterij zelf bijdraagt bovenop scenario C.

---

## Break-even grafiek

Toont de cumulatieve besparing over 25 jaar in twee lijnen: zonder degradatie (groen, optimistisch) en met degradatie (amber, realistisch). De rode stippellijn is de investering. Waar de groene of amber lijn die lijn kruist, is het break-even punt. De groene stip markeert het realistisch break-even punt.

---

## Wat je nog moet regelen (buiten de calculator)

**Melding netbeheerder**
Batterijopslag boven 1 kWh vereist melding bij je netbeheerder (Liander, Stedin, Enexis). Doe dit vóór installatie. Het kost niets maar is verplicht. Formulier staat op de website van je netbeheerder.

**Verzekeraar informeren**
Meld actief dat je een zelfgebouwde Li-ion opslag installeert. Doe je dat niet en er ontstaat brand, betaalt de verzekeraar niet. Sommige verzekeraars vragen een veiligheidscertificaat; vraag dit na.

**Erkend installateur voor netaansluiting**
In Nederland is voor de aansluiting op het net een erkend elektrotechnisch installateur (installateur met NEN 1010-certificering) verplicht. Je kunt het meeste zelf bouwen, maar het aanknoppen op het net moet gedaan worden door iemand met die certificering.

**Brandveiligheid ruimte**
Bepaal waar de batterij staat: garage, schuur, technische ruimte. Eisen per locatie verschillen. Minimaal: CO2-blusser (5 kg) of Lith-Ex aerosol in de ruimte, voldoende ventilatie, geen brandbare materialen direct rondom het pakket.

**SoH meten vóór aankoop**
De calculator werkt met de capaciteit die je zelf invoert, maar een tweedehands Tesla-pakket kan sterk in SoH variëren. Meet altijd eerst de celspanning per module voor aankoop. Modules onder 70% SoH weggooien of als onderdelen doorverkopen.

---

## Wat de tool niet doet

- Netbeheerkosten (~€400-500/jaar) zijn in alle scenario's gelijk, dus ze veranderen niets aan de onderlinge vergelijking.
- Geen rekening met toekomstige prijsstijgingen of -dalingen.
- Geen rekening met een capaciteitstarief als de overheid dat doorvoert.
- Geen financieel advies. De cijfers zijn indicatief.

---

## Delen

**Kopieer link** - de URL bevat alle ingestelde waarden. Plak in WhatsApp of e-mail en de ontvanger ziet precies jouw berekening. Werkt alleen als je het bestand op een server host (tiiny.host of netlify.com/drop).

**Download** - slaat een kopie op met jouw naam als bestandsnaam, inclusief huidige staat.

---

*Leverancierstarieven: allecijfers.nl modelcontracten april 2026. Salderingsregeling vervalt 1 januari 2027. EPEX NL spreads 2024-2025.*
