
Vraag jij je ook af of het al rendabel is om een thuis batterij aan te schafen?
Ik ook! daarom heb ik deze tool gemaakt. hopelijk heb jij er ook wat aan..

hieronder staat hoe je deze moet gebruiken.

# Energie Calculator - README

Gemaakt voor: iedereen die nadenkt over een thuisbatterij, zonnepanelen, en/of een elektrische auto op een dynamisch stroomcontract.

---

## Wat doet deze tool?

Je vult je eigen situatie in en de calculator laat je zien wat je per jaar kwijt bent aan stroom, in vier scenario's naast elkaar. Van het slechtste geval (vast contract, auto 's avonds laden) tot het beste (dynamisch contract, thuisbatterij, auto 's nachts laden). Alles herrekent live terwijl je sliders versleept of getallen intypt.

---

## Hoe gebruik je het?

**Sliders:** sleep om een waarde in te stellen.
**Getallen direct intypen:** klik op de groene waarde naast een slider. Die verandert in een invoerveld. Type je getal, druk Enter of klik ergens anders. De slider volgt mee. Met Escape annuleer je.
**Batterij-presets:** klik op een van de vier systeemkaartjes (Tesla DIY, Powerwall 3, Huawei, Victron). Die vult automatisch de vier batterijsliders in met realistische getallen voor dat systeem. Pas je daarna een slider aan, dan springt de selectie automatisch naar "Aangepast".

---

## Wat kun je instellen?

### Situatie-toggles (bovenaan het invoerpaneel)

**Elektrische auto: ja/nee**
Zet je dit op nee, dan verdwijnen alle auto-rijen uit de berekening. Handig als je de tool deelt met iemand zonder EV. De derde KPI-kaart bovenaan schakelt dan om naar "eigen zonnestroom benut" in plaats van auto-besparing.

**Salderingsregeling: actief / vervallen**
Dit is de belangrijkste schakelaar. Zet je hem op "actief" (situatie tot en met 2026), dan telt zonnestroom die je teruglevert mee tegen het volledige stroomtarief. Zet je hem op "vervallen" (situatie na 1 januari 2027), dan is teruggeleverde stroom alleen nog de terugleververgoeding waard, wat een stuk minder is. Je ziet een oranje banner verschijnen en alle jaarcijfers zakken direct. Dit laat goed zien hoe groot het effect van de afschaffing van de saldering is.

---

### Huishouden

**Jaarverbruik huis**
Hoe meer je verbruikt, hoe groter het absolute voordeel van een batterij en een slim contract. Een huishouden met warmtepomp zit al snel op 5.000-7.000 kWh per jaar.

**Zonnepanelen capaciteit (kWp)**
Meer panelen = meer opwek = meer te besparen via de batterij. Maar: als je veel meer opwekt dan je verbruikt, heb je ook een grotere batterij nodig om dat nuttig te benutten. Die twee hangen dus sterk samen.

**Opbrengst per kWp**
In Nederland gem. 875-920 kWh per kWp per jaar. Arnhem/Gelderland: ~900. Zuidelijker of zonniger dak: hoger. Oost-west opstelling of gedeeltelijke schaduw: lager, reken dan op 750-830.

---

### Tarieven

**Vast tarief**
Dit is je all-in stroomprijs als je een vast of variabel contract hebt (inclusief energiebelasting en btw). Gemiddeld in Nederland 2025-2026: ~€0,27/kWh. Dit is ook de referentieprijs voor scenario A.

**Dynamisch dagpiek (17-21u)**
De prijs die je betaalt op een dynamisch contract tijdens de duurste uren. In de winter en op bewolkte dagen kan dit oplopen tot €0,40-0,50/kWh. De batterij probeert juist dit te vermijden.

**Dynamisch nacht (01-06u)**
Dit is de kans. 's Nachts is stroom op een dynamisch contract vaak twee tot drie keer goedkoper dan overdag. Hier laad je de batterij en je auto. Gemiddeld €0,16-0,20/kWh all-in.

**Terugleververgoeding**
Wat je krijgt per kWh die je teruglevert aan het net na 2027. Verplicht minimaal 50% van het kale leveringstarief, wat in de praktijk neerkomt op ~€0,06-0,10/kWh. Stel je de saldering in op "vervallen", dan rekent de tool hier automatisch mee.

> Het verschil tussen dagpiek en nachtprijs is de motor achter de hele businesscase. Hoe groter dat verschil, hoe sneller de batterij zichzelf terugverdient.

---

### Elektrische auto

**Kilometers per jaar**
Meer rijden = meer laadstroom = groter verschil tussen avond- en nachtladen. Dit is vaak de grootste enkelvoudige besparing in de hele berekening, want je hebt het over honderden kWh per jaar.

**Verbruik (kWh/100km)**
Model X: ~22 kWh/100km in de praktijk (officieel lager). Model 3: ~16-18. Een grotere of zwaardere auto verbruikt meer, wat het voordeel van nachtladen vergroot.

**Laadverlies AC (thuis)**
Bij thuisladen via een wallbox gaat er altijd wat verloren als warmte. Typisch 8-12%. Dit verhoogt de werkelijke laadstroom ten opzichte van wat de auto daadwerkelijk verbruikt op de weg.

> Let op: de Tesla Model X ondersteunt geen V2H (vehicle-to-home). Je kunt de auto-accu niet gebruiken om je huis van stroom te voorzien. De pijl gaat altijd één kant op: net of batterij naar de auto.

---

### Thuisbatterij

**Batterij-presets**
Vier systemen zijn vooringesteld met realistische specs:

| Systeem | kWh | Investering | Verlies | Cycli/jr |
|---|---|---|---|---|
| Tesla 18650 DIY | 20 | €3.500 | 10% | 280 |
| Tesla Powerwall 3 | 13,5 | €9.500 | 7% | 365 |
| Huawei LUNA2000 | 15 | €5.800 | 8% | 330 |
| Victron + Pylontech | 14,4 | €4.200 | 9% | 310 |

**Bruikbare capaciteit**
Hoeveel kWh je daadwerkelijk in en uit de batterij kunt halen. Bij de Tesla 18650 DIY houd je rekening met een SoC-venster van 10-90% om de cellen te ontzien, vandaar dat 20 kWh bruikbaar uit een pakket van ~24 kWh realistisch is.

**Investering totaal**
Alle materiaalkosten bij elkaar: batterijpakket, BMS, omvormer, behuizing, bekabeling, installatie. Hoe lager dit getal, hoe sneller de terugverdientijd. Je kunt hier boven het slider-maximum typen voor duurdere systemen.

**Round-trip verlies**
Elk laad/ontlaad-cyclus verlies je een procent of twee aan warmte. Bij 10% verlies betekent: laad je 10 kWh in, dan haal je er 9 kWh uit. Dit tikt mee in de arbitrage-berekening.

**Laadcycli per jaar**
Hoe vaak de batterij per jaar een volledige cyclus doorloopt. Zomers meer (zonnestroom bufferen), winters meer (nacht-arbitrage). 280 cycli per jaar is realistisch voor een actief gestuurd systeem.

---

## De vier scenario's

| | Wat het betekent |
|---|---|
| **A** | Vast tarief, auto 's avonds laden. Slechtste situatie, dit is je referentie. |
| **B** | Dynamisch contract maar je doet niets speciaals. Je profiteert iets van lagere nachttarieven, maar onbewust. |
| **C** | Dynamisch + je laadt de auto bewust 's nachts tussen 01:00-06:00. Geen extra investering nodig, alleen een laadschema instellen in de Tesla-app of via Home Assistant. |
| **D** | Dynamisch + thuisbatterij + nachtladen. De batterij buffert zonnestroom overdag en goedkope netstroom 's nachts, en vermijdt dure piekmomenten. Dit is de optimale situatie. |

Het verschil tussen A en D is je maximale besparing. De terugverdientijd van het batterijproject is de investering gedeeld door wat de batterij zelf bijdraagt (D minus C).

---

## Delen

**Kopieer link** - de URL bevat alle ingestelde waarden als parameters. Plak je die in WhatsApp of e-mail, dan ziet de ontvanger exact jouw berekening. Werkt alleen als je het bestand op een webserver host (bijv. tiiny.host of netlify.com/drop - sleep het HTML-bestand erin en je hebt binnen 30 seconden een publieke URL).

**Download** - slaat een kopie op van de pagina inclusief huidige staat. Als je een naam hebt ingevuld, begint de bestandsnaam daar mee.

---

## Wat de tool niet doet

- Netbeheerkosten (~€400-500/jaar) zijn in alle scenario's gelijk, dus die zijn buiten beschouwing gelaten. Ze veranderen niets aan het verschil tussen de scenario's.
- Geen rekening met toekomstige prijsstijgingen of -dalingen.
- Geen rekening met degradatie van de batterijcellen over de jaren.
- Geen financieel advies. De cijfers zijn indicatief.

---

*Gebouwd op basis van EPEX NL dag/nacht-spreads 2024-2025. Salderingsregeling vervalt 1 januari 2027.*
