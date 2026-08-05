# Agent 02 – Internationaler Geschäftsmodell-Scout

**Auftrag:** Real existierende Geschäftsmodelle in USA, Kanada, UK, Australien/NZ,
Skandinavien, Niederlande und Israel identifizieren, die in Deutschland noch
schwach verbreitet sind („Time-Machine-Arbitrage").

Stand: 2026-08-05 · Verbindliche Grundlage: `01_nordstern_und_anforderungen.md`,
`02_research_methodik.md`

---

## 0. Methodik, Reichweite und ehrliche Grenzen dieser Recherche

**Durchgeführt:** 30 englisch-/deutschsprachige Web-Recherchen (WebSearch) über
sechs Suchwellen, gezielt entlang der Auftragsbegriffe (boring business recurring
revenue, vertical SaaS blue collar, AI receptionist contractors pricing,
monitoring as a service HVAC, route based recurring revenue, equipment as a
service, compliance as a service SMB, managed service provider vertical, SaaS
enabled marketplace trades, hardware plus subscription B2B) plus länderspezifische
Suchen (AU/NZ, UK, NL, Skandinavien, Israel, Kanada) und deutsche Klon-Suchen.

**Nicht durchgeführt / erzwungene Grenze – muss transparent bleiben:**

1. **WebSearch-Budget der Session war nach 200 Aufrufen (session-weit, geteilt mit
   den Parallel-Agenten) erschöpft.** Die letzten fünf geplanten deutschen
   Klon-Suchen (DGUV-V3-Prüfsoftware, Live-Videowache DE, Aufzug-Monitoring DE,
   Telematik DE, HACCP-Temperaturmonitoring DE) konnten nicht mehr ausgeführt
   werden.
2. **WebFetch war zum Zeitpunkt der Vertiefung technisch blockiert.** Der
   Agent-Proxy verweigerte CONNECT für sämtliche Hosts mit HTTP 403 (verifiziert
   per `curl` gegen `example.com` → `CONNECT tunnel failed, response 403`). Es
   konnten daher **keine Preisseiten direkt gelesen** werden. Alle Preisangaben
   stammen aus Suchergebnis-Snippets sekundärer Vergleichs-/Presseseiten.

**Konsequenz für die Bewertung:** Preise, die aus Vergleichsportalen stammen
(z. B. „Podium kostet ~399 $/Monat"), sind mit **[F-sek]** gekennzeichnet:
belegt, aber nicht von der Herstellerseite verifiziert. Vor jeder Entscheidung
über ein Modell muss der Preis auf der Anbieterseite gegengeprüft werden. Punkt 11
(deutscher Klon) ist dort, wo keine Suche mehr möglich war, ausdrücklich als
**[A] unverifizierte Marktkenntnis – Prüfauftrag** markiert. Diese Felder dürfen
nicht als Fakt weiterverwendet werden.

**Kennzeichnung (nach 01, Abschnitt 8):**

| Kennung | Bedeutung |
|---|---|
| **[F]** | Fakt aus benannter Quelle, hier: Suchergebnis mit URL |
| **[F-sek]** | Fakt aus Sekundärquelle (Vergleichsportal/Presse), Herstellerseite nicht gegengeprüft |
| **[S]** | Schätzung, Rechenweg offengelegt |
| **[A]** | Annahme, unsichere Bandbreite, ausdrücklich nicht belegt |

**Anzahl dokumentierter Modelle: 36.**

---

## 1. Das Grundmuster – warum die Arbitrage überhaupt existiert

Vor den Einzelmodellen die Struktur dahinter. Vier wiederkehrende Mechaniken
erklären fast jedes gefundene Modell:

**M1 – Pflicht statt Überzeugung.** Der wiederkehrende Umsatz entsteht aus einer
gesetzlichen, normativen oder versicherungsseitigen Pflicht (Brandschutzprüfung,
Rückflussverhinderer, Legionellen, DGUV, HACCP, Arbeitsschutz). Der Kunde kündigt
nicht, weil er nicht kündigen *darf*. Höchste Retention, niedrigste
Preissensitivität. Beispiele: Inspect Point, SwiftComply, BRYCER, EcoOnline,
BriqSafe.

**M2 – Sensor + Cloud + Vertrag = Wartungs-Abo.** Günstige Hardware (5–150 $) wird
platziert, erzeugt Daten, und die Daten rechtfertigen ein monatliches Abo, das ein
Vielfaches der Hardwarekosten beträgt. Der Vertrag lebt, weil die Abschaltung des
Sensors ein *Risiko* erzeugt. Beispiele: Otodata (ab 1,50 $/Monat/Tank [F-sek]),
SmartAC, SmartSense, WINT, Blackline Safety.

**M3 – Software frisst den Disponenten.** In „unsexy" Route- und
Handwerksbranchen ersetzt Software die teuerste Engpassrolle (Disponent, CSR,
Verkaufscoach). Der Kunde zahlt aus dem eingesparten Lohn, nicht aus dem
IT-Budget. Deshalb sind die Preise (200–5.000 $/Monat) so viel höher als bei
klassischem KMU-SaaS. Beispiele: ServiceTitan, Avoca, Numa, Rilla.

**M4 – Route-Dichte als Burggraben.** Physische Routen (Wäsche, Fett, Akten,
Schädlinge, Filter) skalieren nicht linear: Der zehnte Kunde in derselben Straße
kostet fast nichts. Wer die Dichte hat, gewinnt dauerhaft. Cintas fährt darauf
51,0 % Bruttomarge [F].

**Die deutsche Arbitrage-These:** In Deutschland ist M1 stark besetzt (TÜV, DEKRA,
Prüfdienstleister), M4 stark besetzt (MEWA, Bardusch, Rentokil), **M2 und M3 sind
schwach besetzt** – vor allem in der Kombination „Sensor/Software + laufender
Servicevertrag für den Mittelstand-Handwerksbetrieb". Dort liegt der Hebel.

---

## 2. Übersichtstabelle (36 Modelle)

| # | Modell | Land | Referenz-Anbieter | MRR-Anker | Übertragbar DE | DE-Klon vorhanden? |
|---|---|---|---|---|---|---|
| 1 | AI-Rezeptionist für Handwerk/Home Services | USA | Avoca, Goodcall, Rosie | 49–3.000 $/Mon | mittel | ja, viele, jung |
| 2 | Voice-AI Serviceannahme Autohaus | USA | Numa | 200–1.500 $/Mon/Standort | hoch | kaum |
| 3 | Voice-AI Restaurant/Reservierung | USA | Slang.ai | 399–599 $/Mon/Standort | mittel | kaum |
| 4 | Vertikales Field-Service-SaaS + Embedded Payments | USA | ServiceTitan | ≥10k $ ACV | mittel | ja, ohne Payments |
| 5 | SMB-Field-Service-SaaS | CA/USA | Jobber, Housecall Pro | 49–299 $/Mon | niedrig (besetzt) | ja, stark |
| 6 | Trades-Job-Management AU/NZ (Job- statt Seat-Pricing) | AU/NZ | ServiceM8, Tradify | 29–349 AUD/Mon | mittel | teilweise |
| 7 | Compliance-SaaS Renewables-Installateure | UK | Payaca | 54 £ + 30 £/Nutzer | **hoch** | nein |
| 8 | Brandschutz-Prüf-SaaS (ITM) | USA | Inspect Point | Preis auf Anfrage | **hoch** | schwach |
| 9 | Rückflussverhinderer-/Cross-Connection-Compliance | USA/IE | SwiftComply, BRYCER | Preis auf Anfrage | mittel | nein (anderes Recht) |
| 10 | Legionellen-/Wassersicherheits-Compliance-SaaS | UK/NL | BriqSafe, aquaAdept, C365Cloud | Preis auf Anfrage | **hoch** | schwach |
| 11 | EHS-/Gefahrstoff-Compliance-SaaS | NO | EcoOnline | Preis auf Anfrage | mittel | ja (Quentic) |
| 12 | Mobile Inspektions-/Checklisten-Plattform | AU | SafetyCulture | 5–24 $/Seat/Mon | mittel | teilweise |
| 13 | vCISO-/Compliance-Plattform für Dienstleister | IL | Cynomi | Preis auf Anfrage | **hoch** | nein |
| 14 | Vertikaler MSP (Dental, Veterinär) | USA | Dark Horse, PACT-One | 140–400 $/Seat/Mon | **hoch** | schwach |
| 15 | Managed Print / Device-as-a-Service | USA | diverse | pro Seite / pro Gerät | niedrig (besetzt) | ja, stark |
| 16 | Lone-Worker-/Gasdetektion Hardware+Abo | CA | Blackline Safety | Gerät + SaaS-Abo | mittel | schwach |
| 17 | Fleet-Telematik + KI-Dashcam | USA | Samsara, Motive | 25–60 $/Fzg/Mon | niedrig (besetzt) | ja, stark |
| 18 | Remote Live-Guarding (Videowache mit Eingriff) | USA | Deep Sentinel / SentinelNow | 50–100 $/Kamera/Mon | mittel | ja, klassisch |
| 19 | Mobile Überwachungseinheit als Mietabo | USA | LiveView Technologies | 1.200–3.400 $/Einheit/Mon | **hoch** | schwach |
| 20 | Robot-as-a-Service Reinigung | CA | Avidbots | 600–900 $/Robot/Mon | mittel | schwach |
| 21 | Equipment-as-a-Service / Pay-per-Use | DK | Grundfos (Cooling-as-a-Service) | ergebnisabhängig | niedrig für Nico | schwach |
| 22 | HVAC-Sensor als Mitgliedschafts-Motor | USA | SmartAC.com | Endkunden-Membership ~1.000 $/Jahr | **hoch** | nein |
| 23 | Autonome HVAC-Optimierung als SaaS | CA | BrainBox AI | Monatsgebühr < Einsparung | mittel | schwach |
| 24 | Tank-Füllstands-Monitoring als Abo | CA/USA | Otodata, Tank Utility | ab 1,50 $/Tank/Mon | mittel | schwach |
| 25 | Cold-Chain-/HACCP-Monitoring als Service | USA | SmartSense by Digi | Preis auf Anfrage | mittel | ja (Testo u. a.) |
| 26 | Wasserschaden-Prävention Hardware+SaaS | IL | WINT | Preis auf Anfrage | mittel | nein |
| 27 | Aufzug-IoT herstellerunabhängig | UK/FR | uptime.ac | Preis auf Anfrage | **hoch** | schwach |
| 28 | Resident Benefits Package (Bündel-Ancillary) | USA | Second Nature | 20–50 $/Einheit/Mon | mittel | nein |
| 29 | Managed WiFi / Bulk Internet MDU | USA | Elauwit, Wanaport | 40–75 $/Einheit/Mon | mittel | schwach |
| 30 | Route-Business Berufskleidung/Textil | USA | Cintas, UniFirst | Wochenvertrag | niedrig (besetzt) | ja, stark |
| 31 | Route-Business Aktenvernichtung + Medizinabfall gebündelt | USA | diverse | 100–150 $/Stopp | mittel | teilweise |
| 32 | Route-Business Altspeiseöl + Fettabscheider mit Software | USA | Grease Connections + Reiter | ~210 $/Standort/Mon | mittel | teilweise |
| 33 | Industrielles Vending / Vendor Managed Inventory | USA | Fastenal FMI | Verbrauch + Bindung | mittel | schwach |
| 34 | Micro Markets / Unattended Retail | USA | 365 Retail Markets | 19–25k $ GP/Standort/Jahr | mittel | schwach |
| 35 | Speech Analytics für Außendienst | USA | Rilla | 199–349 $/Rep/Mon | **hoch** | nein |
| 36 | White-Label-Reseller-Plattform für Agenturen | CA | Vendasta | 99–999 $/Mon + Wholesale | mittel | schwach |

Ergänzende Bausteine, die keine eigenständigen Maschinen sind, aber
Umsatzhebel in mehreren Modellen: Embedded Consumer Financing (Wisetack, 3,9 %
Transaktionsgebühr [F-sek]), Aerial Measurement as a Service (EagleView,
15–87 $/Report [F-sek]), Pay-per-Call-Leadgen, Solar-O&M-Verträge
(10–30 $/kW/Jahr [F-sek]), Submetering-as-a-Service, Safety-Training-Abo.
Sie sind unter Abschnitt 4 dokumentiert.

---

## 3. Modell-Steckbriefe

---

### Modell 1 – AI-Rezeptionist / Voice-AI-CSR für Handwerks- und Home-Service-Betriebe

1. **Modellname:** AI Receptionist / AI CSR (Customer Service Representative) as a Service
2. **Herkunftsland:** USA
3. **Anbieter + URL:**
   - Avoca AI – https://www.avoca.ai/industries/hvac
   - Goodcall – https://www.goodcall.com
   - Rosie – https://heyrosie.com
   - Jobber AI Receptionist (Add-on) – https://www.getjobber.com
   - Numa (Home Services) – https://numa.com
4. **Zielgruppe:** HVAC-, Sanitär-, Elektro-, Dach- und Schädlingsbetriebe mit
   5–200 Mitarbeitern; Kernschmerz: verpasste Anrufe außerhalb der Bürozeit.
5. **Leistung:** KI nimmt eingehende Anrufe 24/7 an, qualifiziert, bucht Termine
   direkt ins Field-Service-System (ServiceTitan/Jobber/Housecall Pro), eskaliert
   Notfälle, protokolliert, versendet SMS-Follow-up.
6. **Preisstruktur konkret:**
   - Autocalls ab **34 $/Monat** [F-sek]
   - Numa **49 $/Monat** [F-sek]; Goodcall **66 $/Monat** jährlich / **79 $/Monat** monatlich [F-sek]
   - Jobber AI Receptionist **99 $/Monat** als Add-on [F-sek]
   - Rosie Professional **49 $** (250 Min.), Scale **149 $/Monat**, Flat **199 $/Monat** [F-sek]
   - Avoca (Mid-Market): geschätzt **1.000–3.000 $/Monat**, Abrechnung überwiegend
     pro KI-Gesprächsminute, kein öffentlicher Preis [F-sek]
   - Klassischer Antwortdienst zum Vergleich: 50–500 $/Monat bzw. **0,75–1,50 $/Anruf** [F-sek]
   - Quelle: https://pipelineon.com/blog/ai-receptionist-contractor/ ,
     https://www.getnextphone.com/blog/ai-receptionist-pricing-guide ,
     https://www.avoca.ai/blog/how-much-does-an-answering-service-cost-a-guide-for-businesses
7. **USP:** 24/7-Erreichbarkeit zu 5–10 % der Kosten eines menschlichen
   Callcenters, mit direkter Terminbuchung statt bloßer Nachrichtenannahme.
8. **Traktion:** Avoca hat **>125 Mio. $ bei 1 Mrd. $ Bewertung** eingesammelt
   (Seed/A/B, Series A geführt von Kleiner Perkins) [F] –
   https://www.prnewswire.com/news-releases/avoca-raises-125m-at-1b-valuation-to-power-americas-services-economy-with-ai-302753962.html
   (Meldung datiert 2026-04-27).
9. **Übertragbarkeit DE: mittel.** Das Problem (verpasste Anrufe im Handwerk) ist
   in DE identisch und durch Fachkräftemangel eher größer. Aber: der deutsche Markt
   ist bereits von Dutzenden Kleinanbietern besetzt, und die Preisanker sind
   deutlich niedriger als in den USA.
10. **Hürden DE:** DSGVO (Gesprächsaufzeichnung/-transkription braucht
    Einwilligung bzw. Hinweiston, AV-Vertrag, EU-Hosting), TKG/TTDSG bei
    Rufnummernbehandlung, Betriebsrat bei Aufzeichnung von Mitarbeitergesprächen
    (§ 87 Abs. 1 Nr. 6 BetrVG – Leistungskontrolle), Sprachmodellqualität für
    Dialekt/Fachbegriffe im Handwerk (Norddeutsch, Fachjargon), Zahlungsverhalten
    unkritisch bei SEPA-Lastschrift.
11. **Deutscher Klon: JA, dicht besetzt – aber jung und billig.** Belegt:
    **Agentino** ab 49 €/Monat, **Foncall** ab 99 €/Monat (DSGVO-konform
    beworben), **Vokaro** 99 €/Monat Flat, **Placetel** (Telekom-Tochter) Grow
    69 €/750 Min., Professional 129 €/1.500 Min., Enterprise 359 €/4.000 Min.,
    **FoxifAI** ab 1.920 € Setup + ab 100 €/Monat, **SpeakKI** [F-sek] –
    https://www.placetel.de/ratgeber/ki-telefonassistent ,
    https://agentino.de/ , https://vokaro.net/kosten/ki-telefonassistent-kosten .
    Marktpreis DE: **39–89 €/Monat** für typische Handwerksbetriebe, Bandbreite
    30 € bis >500 €, Minutenpreise 0,10–0,28 € [F-sek] –
    https://speakki.de/blog/ki-telefonassistent-kosten .
    **Bewertung:** Der Markt ist in DE *nicht* mehr offen, aber er ist um den
    Faktor 5–20 unter dem US-Preisniveau angekommen. Wer hier eintritt,
    konkurriert über Preis – Ausschlusskriterium K.-o. Nr. 6 („gewinnt nur über
    niedrige Preise") droht.
12. **Delegierbarkeit: hoch** nach Standardisierung (Onboarding = konfigurieren,
    testen, übergeben). Aber: Einrichtung pro Kunde ist heute noch beratungsnah.

**Warnung (Friedhofsprüfung):** Der günstige Segment-Preis in DE (49 €) bei
gleichzeitig hohen LLM-Sprachkosten macht die Bruttomarge fragil. Kriterium 2
(≥ 65 % Bruttomarge) ist bei 49 €/Monat mit Telefonie- und LLM-Kosten nicht
sicher erreichbar.

---

### Modell 2 – Voice-AI für Autohaus-Serviceannahme

1. **Modellname:** Dealership Service AI / AI Operating System for Dealerships
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Numa – https://numa.com
4. **Zielgruppe:** Autohäuser, speziell **Serviceabteilungen** (Werkstattannahme)
   – eingesetzt in Ford-, GM-, BMW-, Honda- und Toyota-Händlernetzen [F-sek].
5. **Leistung:** KI-Agenten für Statusupdates zum Fahrzeug, Terminbuchung,
   „missed-call rescue" über Sprache und SMS, Smart Inbox über alle
   Kundenkonversationen.
6. **Preisstruktur konkret:** kein öffentlicher Preis. Branchenberichte:
   **200–400 $/Monat pro Standort („rooftop")** als Einstieg, Händlergruppen und
   Enterprise **500–1.500 $/Monat** [F-sek] –
   https://oncrew.ai/blog/numa-pricing-2026 . Zusätzlich existiert ein
   **Pay-for-Performance-Modell: Zahlung nur für tatsächlich gebuchte Termine**
   [F-sek] – https://serviceagent.ai/blogs/numa-pricing/
7. **USP:** Nicht generischer Telefonassistent, sondern tief in
   Dealer-Management-Systeme integriert; das Statusupdate („Ist mein Auto
   fertig?") ist der mit Abstand häufigste Anruf und komplett automatisierbar.
8. **Traktion:** **32 Mio. $ Series B**, Gesamtfinanzierung **48 Mio. $** [F-sek];
   Inc.-5000-Platz 168 mit **2.248 % Dreijahreswachstum** [F-sek] –
   https://www.prnewswire.com/news-releases/numa-unveils-the-first-ai-agent-platform-for-auto-dealerships-302350393.html
9. **Übertragbarkeit DE: hoch.** Deutschland hat ~36.000 Kfz-Betriebe [A,
   Größenordnung, nicht in dieser Session belegt]; das Problem „Werkstatt-Telefon
   klingelt permanent, Annahme ist besetzt" ist identisch und in DE durch
   Personalmangel akut. Preisanker 200–400 $ ist für einen Autohausbetrieb
   trivial gegenüber einem Servicemitarbeiter.
10. **Hürden DE:** DSGVO wie Modell 1; Anbindung an deutsche DMS (CDK, Loco-Soft,
    Werbas, KSR) ist die eigentliche Eintrittsbarriere – dort liegt aber auch der
    Burggraben. Herstellervorgaben/Corporate-Identity-Regeln der Importeure können
    Freigabeprozesse verlängern. Betriebsrat bei größeren Gruppen relevant.
11. **Deutscher Klon:** In den Recherchen **kein spezialisierter deutscher
    Anbieter für Autohaus-Serviceannahme gefunden**. Die deutschen
    KI-Telefonassistenten (Agentino, Vokaro, Placetel) sind branchenneutral und
    nicht DMS-integriert [F, Negativbefund aus Suche „KI Telefonassistent
    Handwerker Deutschland"; explizite Autohaus-Suche war wegen Budget nicht mehr
    möglich → **Prüfauftrag**].
12. **Delegierbarkeit: hoch.** Ein Implementierungs-Team kann Standorte nach
    Playbook ausrollen; Vertrieb läuft über Händlergruppen (wenige große Kunden =
    Kriterium 5 erfüllt).

---

### Modell 3 – Voice-AI für Restaurants (Reservierung + Telefonannahme)

1. **Modellname:** Restaurant Voice AI / Phone Answering as a Service
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Slang.ai – https://www.slang.ai
4. **Zielgruppe:** Restaurants mit Reservierungsbetrieb, Einzel- und Kettenstandorte.
5. **Leistung:** Beantwortet jeden eingehenden Anruf, verwaltet Reservierungen
   nativ in OpenTable, SevenRooms und Yelp, 24/7.
6. **Preisstruktur konkret:** **Core 399 $/Monat**, **Premium ab 599 $/Monat**;
   Superhost-Service **450–600 $/Monat pro Standort**; Flatrate pro Standort,
   *nicht* pro Anruf oder pro Reservierung [F-sek] –
   https://loman.ai/blog/slang-ai-reviews-pricing-alternatives ,
   https://www.perfectvenue.com/post/slang-ai-review
7. **USP:** Einziger Anbieter, der während des Gesprächs *tatsächlich bucht*,
   statt nur einen Buchungslink zu senden – plus native
   Reservierungssystem-Integrationen.
8. **Traktion:** Anbieterangaben (nicht unabhängig verifiziert): 50 % mehr
   Telefonreservierungen, 96 % Gästezufriedenheit, bis zu 200 gesparte Stunden
   pro Monat [F-sek, Anbieterbehauptung] – Forbes-Beitrag 2025-10-02:
   https://www.forbes.com/sites/quickerbettertech/2025/10/02/for-restaurants-slang-ai-is-a-great-example-of-an-ai-platform-using-voice-recognition-for-roi/
9. **Übertragbarkeit DE: mittel.** Preisanker 399–599 $/Monat ist für den
   deutschen Gastro-Mittelstand hoch; deutsche Restaurants sind extrem
   preissensibel und margenschwach. Der US-Preis lässt sich in DE realistisch
   **nicht** halten [S: deutsche Gastronomie hat nach Mehrwertsteuer- und
   Lohnkostendruck geringere Umsatzrendite als US-Betriebe → Zahlungsbereitschaft
   eher 99–199 €/Monat, Bandbreite unsicher].
10. **Hürden DE:** DSGVO; Integration in deutsche Reservierungssysteme
    (OpenTable ist präsent, aber Quandoo, Resmio, formitable/Zenchef dominieren
    Teilsegmente); hohe Fluktuation und Insolvenzquote in der Gastronomie →
    schlechte Zahlungsmoral und hoher Churn.
11. **Deutscher Klon:** nicht recherchiert (Budget). **[A] Prüfauftrag** –
    vermutlich existieren Ableger der generischen KI-Telefonassistenten für
    Gastro, aber keine tiefe Reservierungssystem-Integration.
12. **Delegierbarkeit: hoch**, aber Kundenzahl-Problem: Bei 150 €/Monat braucht
    man **667 Restaurants für 100.000 €/Monat** [S: 100.000 ÷ 150 = 667] – das
    verstößt gegen Kriterium 5 („wenige hochwertige Kunden").

---

### Modell 4 – Vertikales Field-Service-SaaS mit Embedded Payments (Referenzmodell)

1. **Modellname:** Vertical SaaS + Fintech für die Gewerke
2. **Herkunftsland:** USA
3. **Anbieter + URL:** ServiceTitan – https://www.servicetitan.com
4. **Zielgruppe:** HVAC-, Sanitär-, Elektro-, Garagentor-, Dachbetriebe im
   Mid-Market (Fokus: Kunden ab 10.000 $ Jahreswert).
5. **Leistung:** Ende-zu-Ende-Plattform: Disposition, Auftragsverwaltung,
   Angebot, Rechnung, CRM, Marketingattribution, Payments, Payroll, Finanzierung.
6. **Preisstruktur konkret:** kein öffentlicher Listenpreis; Zielsegment sind
   **Kunden mit ≥ 10.000 $ ACV**, davon 8.000 Stück [F-sek]. Zusätzlich
   Take-Rate auf durchgeleitete Zahlungen (kein reines Seat-Modell) [F-sek].
7. **USP:** Nicht Software, sondern Betriebssystem inkl. Zahlungsströmen; das
   macht Wechsel praktisch unmöglich.
8. **Traktion (harte Zahlen):** Umsatz 2024 **614 Mio. $**, TTM 2025 **817 Mio. $**;
   **8.000+ Kunden** mit **55,7 Mrd. $ Gross Transaction Volume**; IPO Dez. 2024
   (71 $ → 101 $ am ersten Tag), **9,7 Mrd. $ Marktkapitalisierung**, >95 %
   Enterprise-Retention [F-sek] – https://www.saastr.com/5-interesting-learnings-from-servicetitan-at-1b-in-arr/ ,
   https://sacra.com/c/servicetitan/ . Bei 12 Monaten bis Juli 2024: 685 Mio. $
   Umsatz, +24 % YoY, impliziter ARR 772 Mio. $ [F-sek].
9. **Übertragbarkeit DE: mittel.** Die Kategorie ist in DE existent
   (Handwerkersoftware), aber der **Fintech-Layer fehlt fast vollständig**. Der
   ServiceTitan-Hebel – Geld verdienen an der Zahlung, nicht am Sitzplatz – ist
   in DE unbesetzt. Allerdings: Als Neugründung gegen Plancraft/HERO/ToolTime
   anzutreten ist ein Kapitalwettlauf, kein Bootstrapping-Spiel.
10. **Hürden DE:** ZAG-Erlaubnispflicht bzw. Kooperation mit einem lizenzierten
    Zahlungsinstitut (Nico-Ausschlusskriterium „stark reguliert" greift, wenn
    Payments *Kern* wird → K.-o. Nr. 3 möglich); GoBD/DATEV-Anbindung;
    Rechnungspflichten (E-Rechnung ab 2025/2028 in DE); deutlich geringere
    Zahlungsbereitschaft.
11. **Deutscher Klon: JA, stark.** Über 30 Anbieter im DACH-Markt, Preise
    **15–120 €/Nutzer/Monat**; belegt: Meisterwerk ab ~15 €, Plancraft ab ~49 €,
    HERO ab 49 € (Basis) bzw. 99 €, Das Programm 74,90 €, Hawepro ab 39 €,
    ToolTime (Preise zuletzt gesenkt) [F-sek] –
    https://agentino.de/blog/handwerker-software-vergleich-beste-tools/ ,
    https://trusted.de/handwerkersoftware .
    **Bewertung: Markt besetzt, Preisdruck steigt (ToolTime senkt Preise) →
    für Maschine A als Kernmodell ungeeignet.** Als *Andockstelle* (Add-on zu
    bestehenden Systemen) dagegen sehr interessant.
12. **Delegierbarkeit: hoch** – aber Kapitalbedarf verstößt gegen Annahme A1
    (20–60 k € Startkapital) und A10 (kein VC).

---

### Modell 5 – SMB-Field-Service-SaaS (Jobber / Housecall Pro)

1. **Modellname:** SMB Field Service Management SaaS
2. **Herkunftsland:** Kanada (Jobber) / USA (Housecall Pro)
3. **Anbieter + URL:** https://www.getjobber.com , https://www.housecallpro.com
4. **Zielgruppe:** Kleinstbetriebe bis ~15 Mitarbeiter, Garten-, Reinigungs-,
   Sanitär-, Elektro-Gewerke.
5. **Leistung:** Angebot, Termin, Auftrag, Rechnung, Zahlung, Kundenkommunikation.
6. **Preisstruktur konkret:** Jobber Core ~49 $/Monat, Connect ~129 $/Monat,
   Grow ~249 $/Monat; Housecall Pro Basic 59 $/Monat (1 Nutzer), Essentials
   149 $/Monat (bis 5), Max 299 $/Monat (bis 8) [F-sek] –
   https://www.itqlick.com/compare/jobber/housecall-pro
7. **USP:** Extrem niedrige Einstiegshürde, Self-Service-Onboarding.
8. **Traktion:** Housecall Pro **>15.000 Kunden / 100.000 Nutzer**; Jobber
   **>70.000 kleine Unternehmen** [F-sek] – gleiche Quelle.
9. **Übertragbarkeit DE: niedrig.** Kategorie in DE besetzt (siehe Modell 4).
10. **Hürden DE:** siehe Modell 4.
11. **Deutscher Klon: JA, stark** (Plancraft, HERO, ToolTime, Meisterwerk).
12. **Delegierbarkeit: hoch** – aber Kundenzahl-Problem: 100.000 €/Monat bei
    99 €/Monat = **1.010 Kunden** [S] → Verstoß gegen Kriterium 5.

**Verwendung dieses Modells:** Nicht als Maschine A, sondern als **Kanal**. Wer
ein Add-on baut, das in Jobber/Plancraft/HERO andockt, kauft sich deren
Vertriebsreichweite (vgl. Wisetack-Modell, Abschnitt 4).

---

### Modell 6 – Job-Volumen-Pricing statt Seat-Pricing (AU/NZ)

1. **Modellname:** Job-based Pricing für Trades-Software
2. **Herkunftsland:** Australien / Neuseeland
3. **Anbieter + URL:** ServiceM8 – https://www.servicem8.com ; Tradify –
   https://www.tradifyhq.com ; Simpro – https://www.simprogroup.com
4. **Zielgruppe:** Tradies (Handwerker) mit 1–20 Mitarbeitern.
5. **Leistung:** Auftragsmanagement mobil-first.
6. **Preisstruktur konkret:**
   - **ServiceM8: Preis nach Auftragsvolumen, nicht nach Nutzerzahl** – Free
     (30 Jobs), Starter 29 AUD, Growing 79 AUD, Premium 149 AUD, Premium Plus
     349 AUD/Monat [F-sek]
   - Tradify (AU, Stand April 2026): Lite 48 AUD, Pro 52 AUD, Plus 62 AUD **pro
     Nutzer/Monat exkl. GST**; NZ: 48–62 NZD [F-sek]
   - Quelle: https://stackpick.com.au/servicem8-review-australia/ ,
     https://stackpick.com.au/tradify-pricing-australia/
7. **USP (das eigentlich Übertragbare):** Das **Preismodell**. Abrechnung nach
   Auftragsvolumen entkoppelt den Preis von der Mitarbeiterzahl und beseitigt den
   größten Kaufeinwand im Handwerk („mein Geselle nutzt es eh nicht, wieso zahle
   ich 49 € für ihn?").
8. **Traktion:** keine belastbaren Nutzerzahlen in dieser Recherche gefunden.
9. **Übertragbarkeit DE: mittel** als Produkt, **hoch als Preislogik.** Jedes
   deutsche Modell in diesem Bericht sollte prüfen, ob Volumen- statt
   Seat-Pricing die Conversion hebt.
10. **Hürden DE:** keine spezifischen über Modell 4 hinaus.
11. **Deutscher Klon:** Preismodell in DE fast durchgängig Seat-basiert (15–120 €
    pro Nutzer/Monat [F-sek]) → **Volumenpricing ist in DE eine offene Nische.**
12. **Delegierbarkeit:** n/a (Preislogik, kein eigenes Modell).

---

### Modell 7 – Compliance-Field-Service-SaaS für Erneuerbare-Energien-Installateure ⭐

1. **Modellname:** Vertical SaaS für Wärmepumpen-/PV-/Wallbox-Installateure mit
   Förder- und Compliance-Workflow
2. **Herkunftsland:** UK
3. **Anbieter + URL:** Payaca – https://www.payaca.com
4. **Zielgruppe:** Installateure für Wärmepumpen, Solar und Ladeinfrastruktur.
5. **Leistung:** Angebot, Auftrag, Rechnung **plus** die branchenspezifischen
   Compliance- und Förder-Workflows (MCS-Zertifizierung, Boiler Upgrade Scheme
   etc.), die generische Field-Service-Software nicht abbildet.
6. **Preisstruktur konkret:** **54 £/Monat Basis + 30 £/Monat je zusätzlichem
   Nutzer** [F-sek] – https://www.saashub.com/alternatives/post-payaca-2022-07-19-the-6-best-heating-engineer-software-tools-you-should-be-choosing-from-in-2022
7. **USP:** „Payaca hat sich eine starke Nische im UK-Erneuerbaren-Sektor
   erarbeitet, speziell für die Compliance- und Workflow-Anforderungen von
   Wärmepumpen-, Solar- und EV-Ladepunkt-Installateuren" [F-sek] –
   https://www.itrade.net/post/job-scheduling-software-uk-compare-the-best-options-for-trades-businesses
8. **Traktion:** keine Kundenzahlen in dieser Recherche belegt.
9. **Übertragbarkeit DE: HOCH – eines der stärksten Ergebnisse dieser Recherche.**
   Begründung: Deutschland hat mit BEG/BAFA/KfW-Förderung, GEG,
   Hydraulischer-Abgleich-Nachweis, VDE-AR-N 4105-Anmeldung, Netzbetreiber-
   Anmeldeprozessen und Marktstammdatenregister einen **erheblich komplexeren
   Compliance-Stack als UK**. Genau diese Bürokratie ist heute in DE
   Handarbeit auf Papier und in Excel. Der Schmerz ist größer als in UK, die
   Software fehlt.
10. **Hürden DE:** Keine Erlaubnispflicht für den Softwareanbieter selbst
    (wichtig: **kein K.-o. nach Nr. 3**, solange man Werkzeug liefert und nicht
    Energieberatung als Leistung verkauft – die Grenze zur
    Energieberater-Zulassung/EEE-Liste muss sauber gezogen werden). Risiko:
    Förderrecht ändert sich häufig → laufender Pflegeaufwand (das ist zugleich
    der Burggraben und die Rechtfertigung der Monatsgebühr, vgl. Leitfrage 10).
    DSGVO unkritisch. Zahlungsverhalten der Zielgruppe gut (volle Auftragsbücher).
11. **Deutscher Klon: NEIN – Lücke bestätigt, soweit recherchierbar.** Der
    deutsche Handwerkersoftware-Markt (Plancraft, HERO, ToolTime, Meisterwerk,
    Das Programm) ist **branchengeneralistisch**; in keiner der ausgewerteten
    Vergleichsübersichten wird ein Anbieter mit Fördermittel-/GEG-Compliance-Fokus
    genannt [F, Negativbefund aus zwei Vergleichsseiten:
    https://trusted.de/handwerkersoftware , https://agentino.de/blog/handwerker-software-vergleich-beste-tools/].
    **Prüfauftrag** an Agent 01/03: gegen enerchart, SmartHeat, Zolar-Partnertools
    und die Verbands-Tools (ZVSHK, BSW) gegenprüfen.
12. **Delegierbarkeit: hoch.** Produktpflege (Förderlogik) ist an einen
    Fachredakteur delegierbar; Onboarding standardisierbar; Support skaliert.

---

### Modell 8 – Brandschutz-Prüf- und Wartungs-SaaS (Inspection, Testing & Maintenance) ⭐

1. **Modellname:** Fire ITM Software (Inspection · Testing · Maintenance)
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Inspect Point – https://www.inspectpoint.com ; BRYCER /
   The Compliance Engine – https://www.thecomplianceengine.com
4. **Zielgruppe:** Brandschutz-Fachfirmen (Sprinkler, Feuerlöscher,
   Brandmeldeanlagen), außerdem Facility-Betreiber und Behörden.
5. **Leistung:** Vollständiger Prüfworkflow – Terminserien für wiederkehrende
   Prüfungen, mobile Prüfformulare nach NFPA/ULC/Joint Commission/DNV/California
   Title 19, KI-gestützter Inspection Assistant, Mängelverfolgung, automatische
   Nachverkaufs-Angebote aus Mängeln, Rechnung, Zahlung.
6. **Preisstruktur konkret:** **Kein öffentlicher Preis, quote-based** [F] –
   https://www.softwareadvice.com/fleet-management/inspect-point-profile/ ,
   https://capterra.com/p/148287/Inspect-Point/ . Dokumentiert als „Preis auf
   Anfrage" gemäß Methodik-Regel 3; keine Schätzung.
7. **USP:** Die Software verwandelt eine **Pflichtprüfung** in eine
   **Vertriebsmaschine**: Jeder dokumentierte Mangel erzeugt automatisch ein
   Angebot. Das ist der Grund, warum Prüffirmen dafür zahlen – nicht Effizienz,
   sondern Zusatzumsatz.
8. **Traktion:** SwiftComply (verwandtes Segment) wird von **über 400 Städten in
   Nordamerika** genutzt und ist SOC-2-Type-2-zertifiziert [F-sek] –
   https://www.swiftcomply.com/backflow-prevention-software/
9. **Übertragbarkeit DE: HOCH.** Deutschland hat eine mindestens ebenso dichte
   Prüfpflichtlandschaft: DIN 14675 (Brandmeldeanlagen), DIN 14676
   (Rauchwarnmelder), DIN EN 671 (Wandhydranten), DGUV Vorschrift 3
   (Elektroprüfung), Prüfverordnungen der Länder (PrüfVO NRW u. a.),
   Sachverständigenprüfung technischer Anlagen. Die Prüffirmen arbeiten
   überwiegend mit Papier, Excel und Insellösungen [A – Marktkenntnis,
   **nicht in dieser Session belegt, Prüfauftrag an Agent 01**].
10. **Hürden DE:**
    - **Kein K.-o. nach Nr. 3**, solange man *Software für Prüfer* verkauft und
      nicht selbst prüft. Sobald man selbst Prüfleistung erbringt, greifen
      Sachkundenachweise und ggf. Zulassung → dann K.-o.
    - DSGVO gering, da Objektdaten statt Personendaten.
    - Normtexte sind urheberrechtlich geschützt (DIN/VDE) – Prüfformulare dürfen
      nicht 1:1 abgebildet werden ohne Lizenz. **Das ist die reale Hürde** und
      gleichzeitig der Burggraben für den, der die Lizenz beschafft.
    - Zahlungsverhalten der Zielgruppe (etablierte Mittelständler): gut.
11. **Deutscher Klon: schwach.** Es gibt Prüfmanagement-Module in großen
    FM-/CAFM-Systemen und Nischenanbieter, aber kein sichtbares Äquivalent zu
    Inspect Point (mobil-first, prüferzentriert, mit automatischer
    Mängel-zu-Angebot-Konversion) [A – **nicht belegt, die geplante Suche
    „DGUV V3 Prüfsoftware Anbieter" konnte wegen Budgeterschöpfung nicht mehr
    ausgeführt werden. Zwingender Prüfauftrag.**]
12. **Delegierbarkeit: hoch.** Sehr standardisierbar; Support ist
    formularzentriert; Vertrieb über Innungen/Fachverbände.

---

### Modell 9 – Cross-Connection-/Rückflussverhinderer-Compliance für Versorger

1. **Modellname:** Backflow Compliance Management as a Service
2. **Herkunftsland:** USA / Irland
3. **Anbieter + URL:** SwiftComply – https://www.swiftcomply.com ; BRYCER –
   https://www.thecomplianceengine.com/backflow ; Backflow Solutions –
   https://backflow.com
4. **Zielgruppe:** **Wasserversorger und Kommunen** (nicht die Prüfer) – sie
   müssen nachweisen, dass jede Rückflussverhinderer-Armatur im Versorgungsgebiet
   fristgerecht geprüft wurde.
5. **Leistung:** Register aller Geräte, automatische Fristenerinnerung an
   Eigentümer, Portal für zertifizierte Prüfer zum Hochladen von Prüfberichten,
   Eskalation bei Nichteinhaltung, Behördenreporting.
6. **Preisstruktur konkret:** kein öffentlicher Preis [F].
7. **USP:** Die Kommune zahlt, um ihre eigene Haftung zu reduzieren – der
   Vertrag ist praktisch unkündbar, solange die Pflicht existiert.
8. **Traktion:** **>400 Städte in Nordamerika**, SOC 2 Type 2 [F-sek] – s. o.
9. **Übertragbarkeit DE: mittel.** Deutschland regelt Rückflussverhinderung über
   DIN EN 1717 / DIN 1988-100 und die Trinkwasserverordnung; die
   Nachweispflicht liegt in DE stärker beim Anlagenbetreiber als beim Versorger.
   Das Geschäftsmodell muss deshalb umgebaut werden: **Zielkunde wären in DE
   Wohnungsunternehmen und Gewerbeimmobilien, nicht Stadtwerke.**
10. **Hürden DE:** Kommunale Vergabe (Ausschreibungspflicht ab Schwellenwert,
    lange Zyklen, Referenzanforderungen) – das kollidiert mit Nicos
    Anti-Kriterium „steifes Anzug-Business" und mit „Geschwindigkeit bis zum
    ersten Umsatz". Öffentliche Hand zahlt zuverlässig, aber langsam.
11. **Deutscher Klon:** nicht recherchierbar (Budget). **[A] Prüfauftrag.**
12. **Delegierbarkeit: hoch** im Betrieb, **niedrig im Vertrieb** (öffentliche
    Ausschreibungen sind schwer delegierbar).

---

### Modell 10 – Legionellen- und Wassersicherheits-Compliance-Software ⭐

1. **Modellname:** Water Safety / Legionella Compliance SaaS
2. **Herkunftsland:** UK (mit NL-Präsenz)
3. **Anbieter + URL:** BriqSafe – https://www.briqsafe.com ; aquaAdept –
   https://www.legionella-software.co.uk ; C365Cloud –
   https://www.applytosupply.digitalmarketplace.service.gov.uk/g-cloud/services/484419072622087 ;
   Collabit – https://collabitsoftware.com/water-hygiene-and-treatment-software/
4. **Zielgruppe:** Zwei Seiten – (a) Wasserhygiene-Dienstleister und
   FM-Unternehmen als *Werkzeugnutzer*, (b) Gebäudebetreiber (Krankenhäuser,
   Pflege, Hotels, Wohnungswirtschaft) als *Nachweispflichtige*.
5. **Leistung:** Digitales Wasserlogbuch, Gefährdungsbeurteilung,
   Temperatur-Messreihen, Spülpläne, Probenahme-Dokumentation,
   RAG-Compliance-Dashboard, Auditspur gegen ACOP L8 / HSG274 / HTM 04-01.
6. **Preisstruktur konkret:** kein öffentlicher Preis; alle Anbieter
   quote-based [F].
7. **USP:** Haftungsverlagerung. Bei einem Legionellen-Ausbruch ist die lückenlose
   Dokumentation der Unterschied zwischen Bußgeld und Strafverfahren.
8. **Traktion:** BriqSafe: **>19.000 tägliche Nutzer in UK und Niederlande**
   [F-sek, Anbieterangabe] – https://www.briqsafe.com/
9. **Übertragbarkeit DE: HOCH.** Deutschland hat mit der **Trinkwasserverordnung
   (§ 14b TrinkwV, Untersuchungspflicht für Großanlagen zur Trinkwassererwärmung)
   und VDI 6023 / DVGW W 551** eine mindestens gleich strenge, teils strengere
   Pflichtlage. Betroffen: praktisch **jedes Mehrfamilienhaus mit
   Zentralwarmwasser** ab definierter Anlagengröße – das sind in DE
   Hunderttausende Objekte. Die Dokumentation läuft heute weitgehend über
   PDF-Protokolle und Labor-Excel [A – Marktkenntnis, nicht belegt].
10. **Hürden DE:**
    - **Kein K.-o.**, solange man Software liefert. Probenahme selbst ist
      akkreditierungspflichtig (§ 15 TrinkwV, Labore nach DIN EN ISO/IEC 17025) →
      diese Leistung **nicht** selbst erbringen, sondern Laborpartner anbinden.
    - DSGVO gering (Objektdaten), aber Mieterdaten bei Wohnungswirtschaft
      berühren personenbezogene Daten → AV-Verträge nötig.
    - Wohnungswirtschaft zahlt zuverlässig, entscheidet aber langsam und
      gremiengetrieben (Genossenschaften, kommunale Wohnungsgesellschaften).
11. **Deutscher Klon: schwach.** Es existieren Labor-Portale und
    CAFM-Module; ein spezialisiertes, mobil-first Wassersicherheits-SaaS
    nach BriqSafe-Vorbild ist mir aus der Recherche **nicht** begegnet [A –
    nicht belegt, **Prüfauftrag**].
12. **Delegierbarkeit: hoch.**

---

### Modell 11 – EHS-/Gefahrstoff-Compliance-SaaS (Skandinavien)

1. **Modellname:** EHS & Chemical Compliance SaaS
2. **Herkunftsland:** Norwegen
3. **Anbieter + URL:** EcoOnline – https://www.ecoonline.com
4. **Zielgruppe:** Industrie, Bau, Gesundheitswesen, öffentliche Hand – überall
   wo Gefahrstoffe gehandhabt oder Arbeitsschutz dokumentiert werden muss.
5. **Leistung:** Chemical Manager (Sicherheitsdatenblatt-Verwaltung,
   Gefahrstoffkataster), Safety Manager (Vorfälle, Gefährdungsbeurteilung,
   Inspektionen), ESG-Reporting.
6. **Preisstruktur konkret:** quote-based, keine Preise veröffentlicht;
   Kosten variieren nach Modulen, Standorten und Nutzerzahl [F-sek] –
   https://checkthat.ai/brands/ecoonline/pricing
7. **USP:** Gefahrstoffkataster ist Pflicht, extrem pflegeintensiv und wird
   niemals wieder manuell gemacht, wenn es einmal digital ist → nahe null Churn.
8. **Traktion:** **>11.000 Kunden weltweit**; Umsatz **67,2 Mio. $ bei 611
   Mitarbeitern (2025)** [F-sek] – https://getlatka.com/companies/ecoonline.com ;
   Eigentümer: Summa Equity (PE) – https://summaequity.com/investments/ecoonline/
   **Rechnerisch [S]:** 67,2 Mio. $ ÷ 11.000 Kunden ≈ **6.100 $ Jahresumsatz pro
   Kunde** ≈ 510 $/Monat. Umsatz pro Mitarbeiter: 67,2 Mio. ÷ 611 = **110.000 $**
   – für SaaS niedrig, deutet auf hohen Service-/Datenpflegeanteil hin.
9. **Übertragbarkeit DE: mittel.** Die Pflicht existiert in DE (GefStoffV,
   TRGS 400/510, ArbSchG, DGUV) – aber der Markt ist besetzt.
10. **Hürden DE:** keine regulatorische Eintrittshürde für den Softwareanbieter.
11. **Deutscher Klon: JA – Quentic (Berlin, heute Teil von EcoOnline).** Genau
    diese Konsolidierung zeigt: Der DE-Markt war attraktiv genug, um vom
    norwegischen Anbieter gekauft zu werden [A – die Quentic/EcoOnline-Verbindung
    ist Marktkenntnis, in dieser Session nicht belegt; **Prüfauftrag**].
12. **Delegierbarkeit: hoch**, aber der Zahl 110.000 $ Umsatz/Mitarbeiter nach
    ist die Marge geringer als bei reinem SaaS → Kriterium 7 (≥ 65 %
    Bruttomarge) fraglich.

---

### Modell 12 – Mobile Inspektions-/Checklisten-Plattform (Horizontal, aus AU)

1. **Modellname:** Operations & Inspection Platform (Seat-basiert)
2. **Herkunftsland:** Australien
3. **Anbieter + URL:** SafetyCulture (iAuditor) – https://safetyculture.com
4. **Zielgruppe:** Alle Branchen mit Frontline-Personal: Bau, Einzelhandel,
   Gastronomie, Produktion, Logistik.
5. **Leistung:** Digitale Checklisten, Inspektionen, Vorfallmeldung, Training,
   Asset-Verwaltung, Sensorik.
6. **Preisstruktur konkret:** **Lite-Seats 5 $/Monat**, **Premium 24 $/Monat pro
   Sitz**; 20 Vollsitze jährlich = 5.760 $/Jahr, 50 = 14.400 $/Jahr, 100 =
   28.800 $/Jahr [F-sek] – https://www.g2.com/products/safetyculturehq/pricing ,
   https://www.educate-me.co/blog/safetyculture-pricing
7. **USP:** Gratis-Einstieg für kleine Teams, Wachstum über Sitzplätze
   (Product-Led Growth in einer Branche ohne Software-Affinität).
8. **Traktion:** geschätzter **ARR 90,3 Mio. $ (2025)**, Gesamtumsatz 2024
   **161,5 Mio. $**, Bewertung **1,7–2,5 Mrd. $** (Quellen weichen ab), **910
   Mitarbeiter (Stand 30.06.2026)**, **298 Mio. $ Funding** (Blackbird, Insight
   Partners, Index Ventures) [F-sek] – https://getlatka.com/companies/safetyculture.com ,
   https://pitchbook.com/profiles/company/60535-18
9. **Übertragbarkeit DE: mittel** – horizontal, damit kapitalintensiv im Vertrieb.
10. **Hürden DE:** **Betriebsrat ist hier die zentrale Hürde**: Digitale
    Checklisten mit Zeitstempel und Nutzerzuordnung sind mitbestimmungspflichtig
    nach § 87 Abs. 1 Nr. 6 BetrVG (technische Einrichtung zur
    Leistungsüberwachung). In DE braucht jedes Rollout eine Betriebsvereinbarung
    – das verlängert Sales-Zyklen um Monate und ist ein realer Grund, warum
    solche Tools in DE langsamer wachsen.
11. **Deutscher Klon: teilweise** – Quentic, Simplifier, diverse CAFM-Module.
12. **Delegierbarkeit: hoch.**

---

### Modell 13 – vCISO-/Compliance-Plattform als Dienstleister-Multiplikator ⭐

1. **Modellname:** vCISO-as-a-Platform (Enablement statt Endkunde)
2. **Herkunftsland:** Israel
3. **Anbieter + URL:** Cynomi – https://cynomi.com
4. **Zielgruppe:** **Nicht KMU direkt, sondern MSPs, MSSPs und Beratungen**, die
   KMU bedienen. Das ist das eigentlich Kopierbare.
5. **Leistung:** Multi-Tenant-Plattform, die automatisiert erzeugt, was ein
   virtueller CISO liefern müsste: Risikobewertung, Compliance-Readiness,
   Gap-Analyse, maßgeschneiderte Sicherheitsrichtlinien, priorisierter
   Maßnahmenplan, Aufgabenverfolgung, kundenfertige Reports.
6. **Preisstruktur konkret:** kein öffentlicher Preis [F]. Marktkontext für die
   Endleistung: vCISO-Dienstleistungen für Startups/KMU werden mit
   **2.999 $/Monat** angeboten [F-sek] –
   https://cybersecurityos.gumroad.com/l/cybershield-vciso ; SOC-2-Gesamtkosten
   für KMU **20.000–35.000 $**, Tooling für ein 50-Personen-Unternehmen
   **1.700–4.100 $/Monat** [F-sek] – https://trycomp.ai/soc-2-cost-breakdown
7. **USP:** Der Anbieter verkauft nicht an tausende KMU, sondern an hunderte
   Dienstleister, die jeweils dutzende KMU bedienen. **Ein Vertriebsgespräch =
   30 Endkunden.** Das ist der Hebel, der Kriterium 5 („wenige hochwertige
   Kunden") und Kriterium 20 (Skalierbarkeit) gleichzeitig erfüllt.
8. **Traktion:** **37 Mio. $ Series B (April 2025)**, co-geführt von Insight
   Partners und Entrée Capital, mit Canaan, Flint Capital, S16VC; zuvor 3,5 Mio. $
   Seed + 500 k $ Innovate-UK-Zuschüsse [F] –
   https://www.globenewswire.com/news-release/2025/04/23/3066238/0/en/Cynomi-Secures-37M-in-Series-B-Funding-to-Expand-Agentic-AI-Cybersecurity-Platform-Capabilities-for-Service-Providers.html
9. **Übertragbarkeit DE: HOCH – und zwar als Muster, nicht nur als Produkt.**
   Für DE relevant: **NIS2** (Umsetzung in DE über NIS2UmsuCG) zwingt ab 2024/25
   zehntausende mittelständische Unternehmen erstmals zu formalisiertem
   Informationssicherheitsmanagement. Der deutsche Mittelstand hat dafür weder
   Personal noch Prozesse. Die Nachfrage ist gesetzlich erzwungen (Mechanik M1)
   und der Zeitpunkt ist jetzt.
10. **Hürden DE:**
    - **Achtung K.-o.-Prüfung Nr. 3:** Solange man *Software für Dienstleister*
      liefert, gibt es keine Erlaubnispflicht. Sobald man selbst als vCISO
      auftritt und Sicherheitsverantwortung übernimmt, entsteht erhebliche
      Haftung (K.-o. Nr. 9). **Das Plattformmodell ist zulässig, das
      Beratungsmodell wäre grenzwertig.**
    - DSGVO: Verarbeitung von Sicherheitsinformationen der Endkunden → AV-Ketten
      über zwei Stufen (Plattform → MSP → Endkunde), sauber zu modellieren.
    - Sprachqualität: Richtlinien und Reports müssen juristisch belastbares
      Deutsch sein – höhere Latte als bei Voice-AI.
11. **Deutscher Klon: NEIN gefunden.** In den Suchergebnissen ist Cynomi mit
    Büros in Israel, UK und USA vertreten; ein deutschsprachiges Äquivalent für
    NIS2-Enablement von MSPs ist nicht aufgetaucht [F, Negativbefund; jedoch
    keine dedizierte DE-Suche möglich → **Prüfauftrag**, u. a. gegen
    DriveLock, Hornetsecurity, Enginsight, indevis].
12. **Delegierbarkeit: hoch.** Partner-Enablement ist Playbook-Arbeit; der
    Endkunden-Support liegt beim MSP, nicht beim Plattformbetreiber – **das ist
    der beste Delegations-Hebel im gesamten Bericht** (Nico wird strukturell aus
    dem Endkunden-Support herausgehalten, vgl. Anti-Kriterium „täglicher
    Kundensupport").

---

### Modell 14 – Vertikal spezialisierter Managed Service Provider ⭐

1. **Modellname:** Vertical MSP (branchenexklusiver IT-Dienstleister)
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Dark Horse Tech (Dental) – https://www.darkhorsetech.com ;
   PACT-One (Dental) – https://www.pact-one.com ; Medix Dental –
   https://medixdental.com
4. **Zielgruppe:** **Eine** Branche, exklusiv: Zahnarztpraxen, Tierarztpraxen,
   Anwaltskanzleien, Apotheken.
5. **Leistung:** Komplette IT-Verantwortung – Monitoring, Patchen, Backup,
   Security, Helpdesk, Hardware-Lifecycle, **plus** branchenspezifisches Wissen
   (z. B. Cornerstone/Avimark bei Veterinär, Röntgen-/PACS-Anbindung bei Dental).
6. **Preisstruktur konkret:**
   - Dental-IT: **ab 699 $/Monat**, Jahresverträge **ab 799 $/Monat** je nach
     Praxisgröße [F-sek]
   - Veterinär: **140–180 $ pro Nutzer/Monat** [F-sek]
   - Allgemein: 70–150 $/Nutzer/Monat bei 1–50 Sitzen; 100–250 $ bei 75–150
     Sitzen; **200–400+ $ in regulierten Branchen** mit Security- und
     Compliance-Bundle [F-sek]
   - Quellen: https://www.pact-one.com/2024/03/best-dental-it-companies-in-the-united-states/ ,
     https://www.flamingo.run/blog/msp-pricing-models ,
     https://cortavo.com/cortavo-guides/managed-it-services-healthcare-providers
7. **USP:** „Die Nische ist keine Beschränkung, sie ist der Burggraben" –
   Spezialisierung bringt höhere Sätze, schnellere Abschlüsse und Kundentreue,
   die nicht verdunstet, wenn ein Wettbewerber 10 $ günstiger anbietet [F-sek] –
   https://tacticsmarketing.com/blog/the-niche-isnt-a-constraint.-its-the-moat
8. **Traktion:** kein einzelner Anbieter mit veröffentlichten Zahlen; das Muster
   ist über mehrere unabhängige Quellen belegt (5 Fundstellen → Muster nach
   Methodik-Regel 4 erfüllt).
9. **Übertragbarkeit DE: HOCH.** Rechnung: Bei 1.500 €/Monat pro Praxis braucht
   man **67 Praxen für 100.000 €/Monat** [S: 100.000 ÷ 1.500 = 66,7]. Das erfüllt
   Kriterium 5 (wenige hochwertige Kunden) hervorragend. In DE gibt es ca. 40.000
   Zahnarztpraxen [A, Größenordnung, nicht belegt] → 67 Kunden = 0,17 % Marktanteil.
10. **Hürden DE:**
    - **Anti-Kriterien-Konflikt:** MSP bedeutet Helpdesk und damit potenziell
      Notfallreaktion. Nicos K.-o. Nr. 7 („permanente Wochenend-/Notfallarbeit")
      und Nr. 8 (24/7 durch Nico) greifen **nur**, wenn Nico selbst im Dienstplan
      steht. Ein bezahltes Team ist zulässig – also **nur mit Personal ab Tag 1
      finanzierbar**. Das verschiebt den Kapitalbedarf nach oben.
    - Bruttomarge im MSP-Geschäft liegt typisch bei 45–60 % [A] – Kriterium 2
      (Ziel ≥ 65 %) wird eher verfehlt, K.-o. Nr. 5 (< 45 %) aber nicht
      ausgelöst.
    - DSGVO/Gesundheitsdaten: bei Arztpraxen § 203 StGB (Schweigepflicht,
      „berufsmäßig tätige Gehilfen") → Verschwiegenheitsverpflichtung aller
      Mitarbeiter zwingend, sonst Strafbarkeit. Machbar, aber Pflichtprogramm.
    - KHZG/Gematik-Themen bei Heilberufen erhöhen Komplexität.
11. **Deutscher Klon: schwach.** Der deutsche MSP-Markt ist überwiegend
    generalistisch und regional; branchen-exklusive MSPs sind selten [A –
    Marktkenntnis, nicht belegt, **Prüfauftrag**].
12. **Delegierbarkeit: mittel bis hoch.** Technik ist delegierbar, aber
    Personalintensität ist hoch (Kriterium 4 erfüllt, Kriterium 6 nur mit
    starkem Ops-Lead).

---

### Modell 15 – Managed Print / Device-as-a-Service

1. **Modellname:** MPS / DaaS
2. **Herkunftsland:** USA (global etabliert)
3. **Anbieter + URL:** https://managedprint.com , https://www.cds-yes.com ,
   uniFLOW Online (Canon)
4. **Zielgruppe:** KMU und Mittelstand mit Druckerflotte.
5. **Leistung:** Alle Toner/Verbrauchsmaterialien automatisch vor Erschöpfung
   geliefert, alle Teile und Arbeit für Reparaturen, vorbeugende Wartung nach
   Plan, Remote-Monitoring der Gerätezustände, Helpdesk mit Live-Telefontriage,
   regelmäßige Business Reviews mit Nutzungsauswertung [F-sek] –
   https://www.comprobusiness.com/insights/the-ultimate-guide-to-managed-print-services/
6. **Preisstruktur konkret:** drei Modelle – **Cost-per-Page**,
   **Cost-per-User** (flache Monatsgebühr je Mitarbeiter mit Zugriff),
   **pro Gerät/Monat** (z. B. uniFLOW Online) [F-sek]. Keine konkreten Beträge
   in den Quellen.
7. **USP:** Der Kunde kauft keine Drucker mehr, sondern gedruckte Seiten. Eine
   Rechnung, keine Überraschungen.
8. **Traktion:** etablierte Kategorie, keine Startup-Zahlen relevant.
9. **Übertragbarkeit DE: niedrig – Markt vollständig besetzt.** Aufgenommen, weil
   es die **Blaupause** für „Hardware + Verbrauch + Wartung = Monatspauschale"
   ist, die auf andere Gerätearten übertragbar ist (siehe Modelle 22, 24, 33).
10. **Hürden DE:** keine.
11. **Deutscher Klon: JA, stark** (Konica Minolta, Ricoh, Canon, Kyocera und
    hunderte Systemhäuser).
12. **Delegierbarkeit: hoch.**

---

### Modell 16 – Lone-Worker-Schutz und Gasdetektion als Hardware+Abo

1. **Modellname:** Connected Safety (Device + SaaS)
2. **Herkunftsland:** Kanada
3. **Anbieter + URL:** Blackline Safety – https://www.blacklinesafety.com
4. **Zielgruppe:** Industrie mit Alleinarbeitsplätzen: Energie, Chemie, Wasser,
   Versorger, Kommunen.
5. **Leistung:** Rugged-Gerät (G7/G8) mit Gasdetektion, Sturzerkennung,
   Notruf, Zwei-Wege-Sprechverbindung, Live-Daten in die Cloud (Blackline Live);
   **inklusive 24/7-Überwachungsdienst durch bemannte Leitstelle.**
6. **Preisstruktur konkret:** Gerätepreis + Monats-Abo pro Gerät; konkrete
   Beträge nicht öffentlich [F]. Vertriebsweg u. a. AWS Marketplace –
   https://aws.amazon.com/marketplace/pp/prodview-wc7ixanpjyw3g
7. **USP:** „Hardware-nahes Softwaregeschäft, in dem die Investmentthese auf
   ARR-Expansion beruht, nicht auf Stückzahlen" [F-sek] –
   https://www.shashi.co/2026/04/blackline-safety-goes-private-what.html
8. **Traktion (harte Zahlen):** Q1 2026 Rekordumsatz **38,8 Mio. $** bei
   **adj. EBITDA 1,7 Mio. $**; Geschäftsjahr 2025: **150,5 Mio. $ Umsatz,
   6,1 Mio. $ adj. EBITDA**; Kanada-Segment Q1 2026 **7,1 Mio. $ (+3 %)** [F] –
   https://www.businesswire.com/news/home/20260312637663/en/Blackline-Safety-Reports-Record-First-Quarter-2026-Revenue-of-$38.8-million-and-Record-First-Quarter-Adjusted-EBITDA-of-$1.7-million
   **2026 Übernahme durch Francisco Partners (Going Private)** [F-sek].
   **Rechnung [S]:** EBITDA-Marge FY2025 = 6,1 ÷ 150,5 = **4,1 %** – für ein
   Hardware-lastiges Modell typisch und **weit unter Nicos Zielmarke von 30 %**.
   Das ist die wichtigste Warnung dieses Steckbriefs.
9. **Übertragbarkeit DE: mittel.** Bedarf existiert (DGUV Regel 112-139
   Alleinarbeit, Personen-Notsignal-Anlagen nach DIN VDE V 0825-1). Aber:
   Hardware-Entwicklung ist kapitalintensiv, Marge dünn.
10. **Hürden DE:** PNA-Normkonformität (DIN VDE V 0825), Betriebsrat
    (Ortung von Mitarbeitern ist hochgradig mitbestimmungspflichtig und in DE
    kulturell schwer durchsetzbar – **die zentrale Hürde**), DSGVO
    (Standortdaten = personenbezogen).
11. **Deutscher Klon: schwach** (es gibt PNA-Anbieter, aber wenig
    Cloud-/ARR-Logik) [A, **Prüfauftrag**].
12. **Delegierbarkeit: mittel** – Hardware bindet Kapital und
    Lieferkettenmanagement.

**Lehre für Maschine A:** Hardware-Eigenentwicklung senkt die EBITDA-Marge
dramatisch (4,1 % [S]). Wenn Hardware, dann **zugekauft und weiterverrechnet**,
nicht selbst entwickelt.

---

### Modell 17 – Fleet-Telematik mit KI-Dashcam

1. **Modellname:** Connected Operations / Video-Telematik
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Samsara – https://www.samsara.com ; Motive –
   https://gomotive.com
4. **Zielgruppe:** Flottenbetreiber ab ca. 10 Fahrzeugen.
5. **Leistung:** GPS, Fahrverhaltensanalyse, KI-Dashcam mit Ereigniserkennung,
   Wartungsplanung, Compliance.
6. **Preisstruktur konkret:** Samsara Software **27–33 $/Fahrzeug/Monat**, mit
   KI-Dashcam **40–60+ $/Fahrzeug/Monat**; Hardware 99–148 $/Fahrzeug;
   Regierungs-Preisliste nennt **55 $/Monat je Dual-Dashcam**; Fahrer-ID-Token
   9,99 $/Fahrer; **3-Jahres-Vertrag verpflichtend**. Motive ab **25 $/Fahrzeug/
   Monat**, 12-Monats-Mindestlaufzeit [F-sek] –
   https://airpinpoint.com/compare/samsara-pricing , https://tech.co/fleet-management/samsara-vs-motive
7. **USP:** Nicht Ortung, sondern Schadensvermeidung – die Videobeweisführung
   senkt Versicherungsprämien und Haftungsrisiken messbar.
8. **Traktion:** Samsara ist börsennotiert; keine Zahlen in dieser Recherche erhoben.
9. **Übertragbarkeit DE: niedrig – besetzt.**
10. **Hürden DE:** **Kameraüberwachung von Fahrern ist in DE der härteste
    Betriebsrats- und DSGVO-Fall überhaupt.** Innenraumkameras sind praktisch
    nur mit Betriebsvereinbarung und Anlassbezug durchsetzbar; permanente
    Aufzeichnung ist unzulässig. Das erklärt die schwächere Marktdurchdringung
    in DE – und es ist keine Marktlücke, sondern eine Rechtsschranke.
11. **Deutscher Klon: JA, stark** (Vimcar, Webfleet/Bridgestone, YellowFox) [A,
    Marktkenntnis, **Prüfauftrag**].
12. **Delegierbarkeit: hoch.**

**Lehre:** Nicht jede „Lücke" in DE ist eine Chance. Manche sind Rechtsschranken.
Diese Unterscheidung gehört in die Bewertung jedes Modells.

---

### Modell 18 – Remote Live-Guarding (Videowache mit aktivem Eingriff)

1. **Modellname:** Live Video Monitoring / Remote Guarding
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Deep Sentinel – https://www.deepsentinel.com ; Produkt
   SentinelNow (2025 eingeführt) –
   https://www.retaildive.com/press-release/20250630-deep-sentinel-unveils-sentinelnow-remote-live-guard-security-on-demand-for
4. **Zielgruppe:** Ursprünglich Privathaushalte, seit 2025 explizit
   **Mehrfamilien- und Gewerbeobjekte** (Lobbys, Ladenfronten, Parkgaragen).
5. **Leistung:** KI erkennt Ereignis → **menschlicher Wachmann greift binnen
   Sekunden per Lautsprecher ein** und ruft ggf. Polizei. Nicht Aufzeichnung,
   sondern Abschreckung in Echtzeit.
6. **Preisstruktur konkret:** **ab 100 $/Monat für eine Kamera**,
   **+50 $/Monat je weiterer Kamera**, **12-Monats-Mindestlaufzeit**;
   SentinelNow für Property-Teams **ab 50 $/Monat** [F-sek] –
   https://www.security.org/home-security-systems/deep-sentinel/ ,
   Pressemitteilung 2025-06-30 s. o.
7. **USP:** Ersetzt den physischen Wachmann (in DE 25–40 €/Stunde [A]) durch
   eine Leitstelle, die 40 Objekte gleichzeitig betreut. Der Preisunterschied ist
   zweistellig.
8. **Traktion:** keine Umsatzzahlen belegt.
9. **Übertragbarkeit DE: mittel.** Nachfrage existiert (Baustellendiebstahl,
   Leerstandsobjekte, Wertstoffhöfe). Aber die deutsche Sicherheitsbranche ist
   organisiert und die Leitstellen-Infrastruktur (NSL nach DIN EN 50518) ist
   normiert.
10. **Hürden DE:**
    - **§ 34a GewO Bewachungserlaubnis** ist erforderlich, wenn man
      Bewachungsleistungen erbringt. Das ist ein **K.-o.-Kandidat nach Nr. 3**
      („Erlaubnispflicht … als Kern"). Ausweg: Technik liefern und mit
      lizenzierter NSL kooperieren – dann liegt die Erlaubnispflicht beim Partner.
    - DSGVO: Videoüberwachung öffentlich zugänglicher Räume, § 4 BDSG,
      Kennzeichnungspflicht, Löschfristen.
    - Kulturell: Live-Ansprache per Lautsprecher ist in DE ungewohnt und
      rechtlich heikler (Persönlichkeitsrecht).
11. **Deutscher Klon: JA, aber in klassischer Form** – deutsche
    Notruf-Serviceleitstellen (Securitas, Kötter, VdS-zertifizierte NSL) bieten
    Aufschaltung; die KI-gestützte, kameradichte, monatlich abonnierbare Variante
    für kleine Gewerbekunden ist schwächer besetzt [A, **Prüfauftrag** – die
    geplante Suche konnte nicht mehr ausgeführt werden].
12. **Delegierbarkeit: hoch** im Technikteil, **niedrig** im Leitstellenbetrieb
    (24/7-Personal, Schichtplanung – zulässig laut K.-o. Nr. 8, aber teuer).

---

### Modell 19 – Mobile Überwachungseinheit als Mietabo ⭐

1. **Modellname:** Mobile Surveillance Unit (MSU) as a Subscription
2. **Herkunftsland:** USA
3. **Anbieter + URL:** LiveView Technologies (LVT) – https://www.lvt.com
4. **Zielgruppe:** Baustellen, Parkplätze, Einzelhandelsflächen, Bauhöfe,
   Veranstaltungen, Logistikflächen – überall ohne Strom und Netz.
5. **Leistung:** Autarke, solarbetriebene Kamera-Einheit auf Anhänger oder Mast
   mit Mobilfunkanbindung, Beleuchtung, Lautsprecher, KI-Analyse und
   Fernüberwachung. Wird **nicht verkauft, sondern monatlich vermietet**.
6. **Preisstruktur konkret:** **1.200–3.400 $ pro Einheit und Monat**;
   Anbieterangabe „1.500–4.000 $ je nach Konfiguration"; Kaufpreis zum Vergleich
   **38.000–52.000 $ pro Einheit** [F-sek] –
   https://www.spot.ai/blog/liveview-technologies-pricing-2026 ,
   https://securenh.com/lvt-mobile-surveillance-unit-prices-monthly-costs/
7. **USP:** Das ist das **sauberste Equipment-as-a-Service-Modell im ganzen
   Bericht**: hoher Monatspreis, physisches Asset, kein Kunden-Support-Terror,
   klarer ROI (ein verhinderter Kupferdiebstahl bezahlt Monate).
   **Unit Economics [S]:** Kaufpreis 45.000 $ (Mittelwert) ÷ 2.300 $/Monat
   (Mittelwert Miete) = **Amortisation in ca. 20 Monaten**, danach läuft dasselbe
   Asset weiter. Bei 5 Jahren Nutzungsdauer: 138.000 $ Mieteinnahmen auf
   45.000 $ Invest = **3,1x** vor Betriebskosten.
8. **Traktion:** LVT ist in den USA Marktführer der Kategorie; keine Umsatzzahlen
   in dieser Recherche belegt.
9. **Übertragbarkeit DE: HOCH.** Der Bedarf ist in DE massiv: Baustellendiebstahl,
   Metalldiebstahl an Bahn- und Energieanlagen, Vandalismus an Bauhöfen,
   Photovoltaik-Freiflächen (Modul- und Kabeldiebstahl ist ein wachsendes
   Problem). Zielkunden sind **Bauunternehmen, Projektentwickler,
   Energieversorger, Kommunen** – also wenige, große, zahlungsfähige Kunden
   (Kriterium 5 ✅).
   **Rechnung für Maschine A [S]:** Bei 1.800 €/Monat Mietpreis braucht man
   **56 Einheiten für 100.000 €/Monat** (100.000 ÷ 1.800 = 55,6). Bei 25.000 €
   Anschaffung je Einheit [A] sind das **1,4 Mio. € gebundenes Kapital** – über
   Leasing/Mietkauf finanzierbar, aber weit über Annahme A1 (20–60 k €
   Startkapital). **Das Modell ist kapitalintensiv und skaliert nur mit
   Fremdkapital oder Wachstum aus Cashflow.**
10. **Hürden DE:**
    - **§ 34a GewO** nur, wenn eigene Bewachung; reine Gerätevermietung +
      Aufschaltung auf eine Partner-NSL umgeht das.
    - DSGVO: Kamera auf Baustelle erfasst Beschäftigte → Betriebsrat des
      *Kunden* (§ 87 BetrVG), Hinweisbeschilderung, Löschkonzept. Lösbar, aber
      Vertragswerk nötig.
    - Mobilfunkabdeckung in ländlichen Regionen (relevant für Standort
      Nordwestdeutschland, Annahme A3).
    - Diebstahl der Einheit selbst → Versicherung.
11. **Deutscher Klon: schwach.** Es gibt in DE Baustellen-Videoüberwachung als
    Dienstleistung, aber das standardisierte Mietabo-Produkt mit
    Solar-Anhänger-Flotte und Software-Layer ist kaum ausgeprägt [A,
    **Prüfauftrag**].
12. **Delegierbarkeit: HOCH.** Logistik (Aufstellen, Abholen) ist reine
    Ausführung; Monitoring liegt beim Partner; Nico wäre nach Aufbau der
    Prozesse strukturell draußen. **Bestes Delegierbarkeits-Profil unter den
    physischen Modellen.**

---

### Modell 20 – Robot-as-a-Service (Reinigung)

1. **Modellname:** RaaS – Cleaning Robots
2. **Herkunftsland:** Kanada
3. **Anbieter + URL:** Avidbots – https://www.avidbots.com
4. **Zielgruppe:** Einkaufszentren, Flughäfen, Logistikzentren,
   Gebäudereinigungsunternehmen.
5. **Leistung:** Autonome Scheuersaugmaschine inkl. Wartung, Software, Updates,
   Reporting – als Monatsmiete.
6. **Preisstruktur konkret:** **ca. 600–900 $/Monat** im RaaS-Modell;
   Kaufpreis Avidbots Neo 2 **ca. 40.000–60.000 $** [F-sek] –
   https://servicerobotco.com/pricing/robot-pricing-guide ,
   https://sproutmation.com/blog/complete-guide-cleaning-robot-rental-programs-2026
   **Rechnung [S]:** 50.000 $ Kaufpreis ÷ 750 $/Monat = **67 Monate
   Amortisation** – deutlich schlechter als beim Überwachungsanhänger (20
   Monate). Grund: der Roboter verschleißt, der Anhänger kaum.
7. **USP:** Der Kunde vergleicht mit Reinigungspersonal, nicht mit einer Maschine.
8. **Traktion:** Brain Corp ist Softwareplattform hinter Fremdrobotern (Tennant
   T7AMR), kein eigenes Servicegeschäft [F-sek].
9. **Übertragbarkeit DE: mittel.** Gebäudereinigung in DE ist ein
   Niedriglohnmarkt mit harten Preisen; die Substitutionsrechnung geht bei
   deutschen Reinigungslöhnen (Lohngruppe 1 ca. 14–15 €/h [A]) schlechter auf als
   in den USA.
10. **Hürden DE:** Betriebsrat (Personalersatz), Maschinenrichtlinie/CE,
    Haftpflicht bei autonomem Betrieb in Publikumsbereichen.
11. **Deutscher Klon: schwach** (Nilfisk, Kärcher bieten Robotik, aber
    überwiegend als Verkauf, nicht als RaaS) [A, **Prüfauftrag**].
12. **Delegierbarkeit: mittel** – Serviceeinsätze am Gerät binden Techniker.

---

### Modell 21 – Equipment-as-a-Service / Pay-per-Use (Skandinavien)

1. **Modellname:** EaaS / Machine-as-a-Service / Cooling-as-a-Service
2. **Herkunftsland:** Dänemark (Referenzfall)
3. **Anbieter + URL:** Grundfos – https://www.grundfos.com ; Konzeptquellen:
   https://www.machinemetrics.com/blog/what-is-equipment-as-a-service ,
   https://www.3ds.com/industries/industrial-equipment/equipment-as-service
4. **Zielgruppe:** Produzierende Unternehmen und Gebäudebetreiber.
5. **Leistung:** Der Hersteller behält das Eigentum an der Anlage; der Kunde zahlt
   für Nutzung oder Ergebnis. Wartung, Monitoring und Upgrades sind inkludiert.
6. **Preisstruktur konkret:** Beim Grundfos-Modell **„Cooling-as-a-Service": Der
   Kunde zahlt periodisch auf Basis der erzielten Einsparung gegenüber der alten
   Anlage** [F-sek] – https://shoplogix.com/blog/equipment-as-a-service/
7. **USP:** Der Kunde hat kein Investitionsrisiko; der Anbieter verdient an
   Verfügbarkeit und Effizienz statt an Stückzahlen.
8. **Traktion:** Grundfos ist etabliert; keine Modellzahlen belegt.
9. **Übertragbarkeit DE: niedrig für Nico.** Das Modell setzt entweder eigene
   Fertigung oder sehr viel Bilanzkapital voraus. Es widerspricht Annahme A1
   und A10.
10. **Hürden DE:** Bilanzierung (Leasing vs. Miete, IFRS 16/HGB),
    Finanzierungsstruktur, ggf. Erlaubnispflicht bei Finanzierungsleasing (§ 1
    Abs. 1a KWG) → **K.-o.-Risiko Nr. 3**, wenn die Finanzierung selbst
    gewerbsmäßig betrieben wird.
11. **Deutscher Klon: schwach** – deutsche Maschinenbauer diskutieren EaaS seit
    Jahren, setzen es aber selten um.
12. **Delegierbarkeit: mittel.**

**Warum trotzdem aufgenommen:** Die **Preislogik** („Kunde zahlt aus der
Einsparung") ist ein starkes Verkaufsargument, das in mehreren anderen Modellen
dieses Berichts wiederverwendbar ist (22, 23, 26, 29).

---

### Modell 22 – Sensor-Monitoring als Motor für Wartungs-Mitgliedschaften ⭐

1. **Modellname:** Proactive Service Membership powered by Sensors
2. **Herkunftsland:** USA
3. **Anbieter + URL:** SmartAC.com – https://www.smartac.com
4. **Zielgruppe:** **HVAC-Fachbetriebe** (nicht Endkunden) – das ist der Clou:
   Verkauft wird an den Handwerksbetrieb, der damit sein eigenes
   Endkunden-Abo verkauft.
5. **Leistung:** Der Betrieb platziert beim Endkunden Sensoren an der Anlage;
   der Betrieb erhält eine gebrandete App und ein Contractor-Dashboard;
   Störungen werden erkannt, bevor der Kunde anruft. Ergebnis: der Betrieb kann
   ein Wartungs-Abo verkaufen, das der Kunde nicht kündigt.
6. **Preisstruktur konkret:** SmartAC-Preis nicht öffentlich [F]. Belegt sind
   die **Endkunden-Ökonomie**: bei 1.000 Mitgliedern und **~1.000 $
   Jahresumsatz pro Mitglied** erhält eine Retentionsverbesserung von 70 % auf
   96 % **über 260.000 $ Jahresumsatz** [F-sek]; Anbieterangaben: **20 %
   Abschlussquote** bei Endkunden, **97 % jährliche Retention** bei Nutzung von
   Sensoren + gebrandeter App [F-sek] –
   https://www.smartac.com/blog/how-smart-ac-technology-boosts-service-membership-sales ,
   https://www.citybiz.co/article/830798/sensors-memberships-and-recurring-revenue-smartac-and-certainpath-are-rewiring-hvac-growth/
   **Ableitung [S]:** 1.000 $/Jahr ≈ **83 $/Monat Endkunden-Abo**.
7. **USP:** Die Sensordaten sind der **Kündigungsschutz**. Ein Wartungsvertrag
   ohne Sensor ist ein Versprechen; mit Sensor ist er ein sichtbarer Dienst.
   Genau das erklärt den Sprung von 70 % auf 97 % Retention.
8. **Traktion:** Fallstudie „Iceberg Home Services: 80.000 $ Neuumsatz" [F-sek,
   Anbieter-PR] –
   https://www.prnewswire.com/news-releases/smartac-helps-iceberg-home-services-drive-proactive-hvac-service-and-80k-in-new-revenue-302684703.html
9. **Übertragbarkeit DE: HOCH – und strategisch das interessanteste Modell für
   Nicos Profil.** Begründung:
   - Deutschland hat **Millionen Heizungsanlagen** mit gesetzlicher
     Wartungsempfehlung und – neu – **GEG-Heizungsprüfpflicht** (Heizungsprüfung
     und -optimierung für Gasheizungen; hydraulischer Abgleich).
   - Der Wärmepumpen-Hochlauf erzeugt eine Generation neuer, komplexer Anlagen,
     die der Endkunde nicht versteht und der Betrieb nicht laufend besuchen kann.
   - SHK-Betriebe in DE haben genau dasselbe Problem wie US-HVAC-Betriebe:
     Wartungsverträge sind margenstark, aber schwer zu verkaufen und zu halten.
   - **Verkauft wird B2B an Betriebe → wenige, hochwertige Kunden (Kriterium 5 ✅),
     kein Endkunden-Support durch Nico (Anti-Kriterium vermieden).**
   **Rechnung [S]:** 200 SHK-Betriebe × 500 €/Monat = **100.000 €/Monat**.
   Bei ca. 50.000 SHK-Betrieben in DE [A, Größenordnung] wären das 0,4 %
   Marktanteil.
10. **Hürden DE:**
    - DSGVO: Verbrauchsdaten aus Privathaushalten sind personenbezogen →
      Einwilligung des Endkunden, AV-Vertrag mit dem Betrieb, EU-Hosting. Machbar,
      aber Pflichtprogramm.
    - Messstellenbetriebsgesetz greift **nicht**, solange man nicht abrechnungs-
      relevant misst – wichtige Abgrenzung, sonst droht Regulierung (K.-o. Nr. 3).
    - Hersteller-Ökosysteme (Vaillant, Viessmann, Bosch) bauen eigene Konnektivität
      → **Friedhofsrisiko**: der Hersteller kann die Schnittstelle schließen.
      Gegenstrategie: herstellerunabhängige Nachrüst-Sensorik (wie uptime.ac im
      Aufzugmarkt, Modell 27).
    - Handwerkskammer-/Innungsvertrieb ist in DE der Schlüsselkanal und
      kulturell zugänglich (passt zu Nicos „bodenständiger Kultur", Kriterium 25).
11. **Deutscher Klon: NEIN gefunden.** Es gibt Hersteller-Apps
    (Vaillant myVAILLANT, Viessmann ViCare) – aber die sind **herstellergebunden
    und dienen dem Hersteller, nicht dem Betrieb**. Ein herstellerunabhängiges,
    betriebszentriertes Sensor+Membership-Enablement ist mir in der Recherche
    nicht begegnet [A, kein DE-Suchlauf möglich → **hoher Prüfauftrag an
    Agent 01 und Agent 03**].
12. **Delegierbarkeit: hoch.** Onboarding = Sensor-Kit versenden + Schulung;
    Support ist B2B und in Geschäftszeiten; Produktentwicklung bleibt bei Nico
    (das ist die Rolle, die er *will*, siehe „Ideale Langfristrolle").

---

### Modell 23 – Autonome HVAC-Optimierung als SaaS

1. **Modellname:** Autonomous Building AI
2. **Herkunftsland:** Kanada
3. **Anbieter + URL:** BrainBox AI – https://brainboxai.com
4. **Zielgruppe:** Betreiber gewerblicher Bestandsimmobilien.
5. **Leistung:** KI übernimmt autonom die Steuerung vorhandener HVAC-Anlagen –
   **ohne Retrofit, ohne zusätzliche Sensoren**, rein über bestehende
   Gebäudeleittechnik.
6. **Preisstruktur konkret:** Monatsgebühr, Höhe nach Gebäudetyp, Anzahl,
   Standort; Anbieterversprechen: **„die Monatsgebühr liegt unter der Einsparung
   auf der Energierechnung"** [F-sek] –
   https://brainboxai.com/decarbonization-solution-that-pays-for-itself
7. **USP:** Netto-positive Preisgestaltung – der Kunde kann rechnerisch nicht
   verlieren. Das ist das stärkste Verkaufsargument der gesamten Recherche.
8. **Traktion:** Partnerschaften (u. a. Fortune Energy Partners, Texas) belegt
   [F-sek]; keine Umsatzzahlen.
9. **Übertragbarkeit DE: mittel.** Energiepreise in DE sind höher als in den USA
   → die Einsparungsrechnung ist in DE **besser**, nicht schlechter. Hemmnis ist
   die Heterogenität deutscher Gebäudeleittechnik (Siemens, Sauter, Kieback&Peter,
   WAGO) und die Zugriffsverweigerung der Facility-Dienstleister.
10. **Hürden DE:** IT-Sicherheit/OT-Zugriff (Gebäudeleittechnik ans Internet zu
    hängen ist in DE ein Compliance-Thema, bei KRITIS sogar reguliert), Haftung
    bei Fehlsteuerung (K.-o. Nr. 9 prüfen: Ausfall einer Klimaanlage im
    Rechenzentrum oder Krankenhaus = Großschaden → **Haftungsbegrenzung
    vertraglich zwingend**).
11. **Deutscher Klon: schwach** (aedifion aus Köln ist der nächste Kandidat) [A,
    **Prüfauftrag**].
12. **Delegierbarkeit: mittel** – die Anbindung je Gebäude ist projektnah
    (Kriterium 17 „kein dauerhaftes Projektgeschäft ohne Standardisierung"
    gefährdet).

---

### Modell 24 – Tank-Füllstandsmonitoring als Abo

1. **Modellname:** Tank Level Monitoring as a Service
2. **Herkunftsland:** Kanada / USA
3. **Anbieter + URL:** Otodata – https://www.otodatatankmonitors.com ;
   Tank Utility – https://www.tankutility.com
4. **Zielgruppe:** **Energiehändler** (Flüssiggas-, Heizöl-, Industriegas-Händler)
   – nicht die Endkunden.
5. **Leistung:** Funk-Füllstandssensor am Tank, Portal und App, Prognose für
   Tourenplanung, Vermeidung von Leerläufen.
6. **Preisstruktur konkret (sehr gut belegt):**
   - Otodata: **ab 1,50 $/Monat, keine Vorabkosten** [F-sek]
   - **72 % der Flüssiggashändler** bieten Tankmonitoring an, **Durchschnittsgebühr
     54,32 $ pro Tank** (Erhebungszeitraum lt. Gray, Gray & Gray Energy & Propane
     Survey 2023); **36 % der Heizölhändler**, Durchschnittsgebühr **26,53 $**
     [F-sek] – https://bpnews.com/feature-articles/tank-monitoring-solutions-monitors-portals-apps
   **Marge [S]:** Einkauf 1,50 $/Monat, Weitergabe 26,53–54,32 $ (jährlich oder
   monatlich – die Quelle differenziert nicht eindeutig; **Unsicherheit
   ausdrücklich markiert**). Selbst bei jährlicher Gebühr von 54 $ gegen 18 $
   Jahreskosten liegt die Bruttomarge bei **67 %** – Kriterium 2 erfüllt.
7. **USP:** Der Händler spart Leerfahrten und verhindert Kundenverlust durch
   Leerlauf; der Sensor bindet den Kunden an den Händler.
8. **Traktion:** Otodata nutzt Cat-M1/NB-IoT über Bell Canada, Geräte aktivieren
   sich automatisch bei Ankunft [F-sek] –
   https://www.aeris.com/resources/otodata-smarter-monitoring/
9. **Übertragbarkeit DE: mittel.** Zielgruppe existiert (Heizöl- und
   Flüssiggashändler, Landwirtschaft mit Diesel- und Güllebehältern,
   Industriegase). Der deutsche Heizölmarkt schrumpft strukturell – das ist ein
   **Gegenwind, der offen benannt werden muss**. Wachstumsfeld dagegen:
   AdBlue, Schmierstoffe, Futtermittel-Silos, Streusalz, Flüssiggas in
   Nicht-Erdgas-Gebieten (relevant für Nordwestdeutschland, Annahme A3).
10. **Hürden DE:** Mobilfunk-Roaming/IoT-SIM-Kosten, Explosionsschutz (ATEX) bei
    Gasbehältern → Zertifizierung der Sensorik zwingend (Zukauf, nicht
    Eigenbau!), Eichrecht **nicht** betroffen solange nicht abrechnungsrelevant.
11. **Deutscher Klon: schwach** – es gibt Tanksensorik-Anbieter, aber selten mit
    Händler-Portal und Tourenoptimierung als Abo [A, **Prüfauftrag**].
12. **Delegierbarkeit: hoch.**

---

### Modell 25 – Cold-Chain-/Lebensmittelsicherheits-Monitoring als Service

1. **Modellname:** Food Safety & Cold Chain Monitoring as a Service
2. **Herkunftsland:** USA
3. **Anbieter + URL:** SmartSense by Digi – https://www.smartsense.co
4. **Zielgruppe:** Restaurantketten, Lebensmitteleinzelhandel, Apotheken,
   Labore, Krankenhäuser.
5. **Leistung:** Kabellose, batteriegepufferte Sensoren + Mobilfunk-Gateway →
   Dashboard mit Alarmmanagement, Analytik, Enterprise-Übersicht; Inbetriebnahme
   je Standort **innerhalb von Stunden** [F-sek].
6. **Preisstruktur konkret:** kein öffentlicher Preis [F].
7. **USP:** Ersetzt die manuelle Temperaturliste am Kühlschrank (HACCP) durch
   lückenlose Aufzeichnung – spart Personalzeit *und* verhindert Warenverlust.
   Doppelter ROI.
8. **Traktion:** Digi International ist börsennotiert; keine Segmentzahlen erhoben.
9. **Übertragbarkeit DE: mittel.** HACCP-Pflicht besteht in DE über
   EU-VO 852/2004 – die Nachfrage ist gesetzlich erzwungen (Mechanik M1).
10. **Hürden DE:** Der Markt ist besetzt (Testo Saveris, Ebro, Comark).
    Preisniveau in DE niedrig.
11. **Deutscher Klon: JA** (Testo, Ebro Electronic) [A, **Prüfauftrag**].
12. **Delegierbarkeit: hoch.**

---

### Modell 26 – Wasserschaden-Prävention als Hardware+SaaS (Israel)

1. **Modellname:** Water Intelligence / Leak Prevention
2. **Herkunftsland:** Israel
3. **Anbieter + URL:** WINT – https://www.wint.ai
4. **Zielgruppe:** Bauunternehmen (während der Bauphase), Gewerbeimmobilien,
   Industrie, Rechenzentren.
5. **Leistung:** KI-Software plus vernetzte Hardware am Rohrsystem erkennt
   Anomalien und **schließt das Ventil automatisch**, bevor Schaden entsteht.
6. **Preisstruktur konkret:** kein öffentlicher Preis [F].
7. **USP:** Der Versicherer ist der eigentliche Treiber – Wasserschäden sind der
   häufigste Gebäudeschaden. Prämienrabatt finanziert das Abo.
8. **Traktion:** **35 Mio. $ Series C**, co-geführt von Inven Capital und Insight
   Partners; Kunden u. a. **Empire State Building, Microsoft, HP, PepsiCo,
   Suffolk Construction, Azrieli Group, Weizmann Institute** [F] –
   https://techcrunch.com/2023/08/10/water-intelligence-startup-wint-nabs-35m-to-help-companies-find-and-stop-leaks/
9. **Übertragbarkeit DE: mittel.** Leitungswasserschäden sind auch in DE der
   Schadenschwerpunkt der Wohngebäudeversicherung. Der Kanal wäre
   **Versicherer und Wohnungswirtschaft**, nicht der Endkunde.
10. **Hürden DE:** Trinkwasserinstallation ist DVGW-reguliert; ein automatisches
    Absperrventil im Trinkwassernetz braucht DVGW-Zulassung → Zukauf zertifizierter
    Komponenten zwingend. Einbau nur durch eingetragenen SHK-Betrieb.
    Versicherungskooperationen sind langsam (Anzug-Business – Anti-Kriterium).
11. **Deutscher Klon: NEIN in dieser Ausprägung** (Grohe Sense Guard und Syr
    sind Endkundenprodukte, kein gewerbliches SaaS mit Versichererlogik) [A,
    **Prüfauftrag**].
12. **Delegierbarkeit: mittel** (Installationskoordination).

---

### Modell 27 – Herstellerunabhängiges Aufzug-IoT ⭐

1. **Modellname:** Brand-agnostic Elevator Predictive Maintenance
2. **Herkunftsland:** UK/Frankreich (Paris und London)
3. **Anbieter + URL:** uptime.ac – https://uptime.ac
4. **Zielgruppe:** **Aufzugs-Serviceunternehmen** (primär) sowie Wohn- und
   Gewerbeimmobilienbetreiber.
5. **Leistung:** Nachrüstbare Digitalsensoren, per 4G an **jeden beliebigen
   Aufzug** anschließbar; KI-System liefert Echtzeitdaten zu Sicherheit,
   Leistung und drohenden Ausfällen.
6. **Preisstruktur konkret:** kein öffentlicher Preis [F].
7. **USP (das entscheidende Detail):** **Herstellerunabhängigkeit.** Kone, Otis,
   Schindler und TK Elevator bieten alle eigene Monitoring-Produkte (z. B. TK MAX)
   – aber nur für **eigene** Anlagen. Der freie Serviceunternehmer mit gemischtem
   Bestand hat kein Werkzeug. Genau diese Lücke besetzt uptime.ac: „Das
   markenagnostische Angebot erlaubt Aufzugs-Serviceanbietern, ihr
   Wartungsportfolio auszubauen und die Kundenbindung zu verbessern" [F-sek] –
   https://eustartup.news/startup-showcase-uptime-ac-the-leading-iot-predictive-technology-for-elevators/
8. **Traktion:** **über 200 Unternehmen in Europa**, gegründet 2016, **über
   11 Mio. $ eingesammelt**, Investor u. a. Serena [F-sek] –
   https://www.crunchbase.com/organization/uptime-ac , https://www.serena.vc/portfolio-profile/uptime/
9. **Übertragbarkeit DE: HOCH.** Deutschland hat rund **800.000 Aufzugsanlagen**
   [A, Größenordnung, nicht in dieser Session belegt – **prüfen**]. Der Markt
   für freie Aufzugswartung (außerhalb der vier Großen) ist in DE stark und
   politisch gewollt (Kartellrechtsgeschichte der Aufzugsbranche). Zusätzlich:
   **wiederkehrende Prüfpflicht nach BetrSichV durch zugelassene
   Überwachungsstellen** – die Daten aus dem Monitoring reduzieren
   Prüfvorbereitungsaufwand.
10. **Hürden DE:** Eingriff in Aufzugssteuerungen ist sicherheitsrelevant
    (Aufzugsrichtlinie 2014/33/EU) → **nur auslesende, nicht steuernde Sensorik**,
    sonst Konformitätsbewertung nötig (K.-o.-Risiko Nr. 3). ZÜS-Prüfung bleibt
    beim Prüfdienst. Betriebsrat irrelevant. Zahlungsverhalten der
    Aufzugsdienstleister: gut.
11. **Deutscher Klon: schwach.** Es gibt Ansätze (u. a. Digital Spine, Aufzughelden
    – beide Namen aus Marktkenntnis, **in dieser Session nicht belegt**), aber
    keine sichtbare Marktdurchdringung [A, **Prüfauftrag mit hoher Priorität**].
12. **Delegierbarkeit: hoch.** Sensorinstallation macht der Aufzugsmonteur des
    Kunden, nicht der Anbieter – exzellenter Skalierungshebel.

---

### Modell 28 – Resident Benefits Package (gebündelte Zusatzleistungen)

1. **Modellname:** RBP – Resident Benefits Package
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Second Nature – https://www.secondnature.com ; Latchel –
   https://latchel.com
4. **Zielgruppe:** **Hausverwaltungen** – die es an ihre Mieter weitergeben.
5. **Leistung:** Bündel aus Filterlieferung, Mieterhaftpflicht, Bonitätsaufbau
   („credit building" durch Meldung pünktlicher Mieten), Concierge-Support,
   Schädlingsservice – als ein Posten im Mietvertrag.
6. **Preisstruktur konkret:** **20–50 $ pro Einheit und Monat** an den Mieter;
   Beispiel: Einkauf 25–30 $, Verkauf 45 $ → **~15 $ Marge pro Einheit/Monat**
   [F-sek]; 100 Einheiten × 30 $ = **36.000 $ Zusatzumsatz p. a.** [F-sek] –
   https://butterflymx.com/blog/resident-benefits-package/ ,
   https://latchel.com/how-to-increase-revenue-per-unit-with-a-resident-benefits-package/
7. **USP:** Die Hausverwaltung bekommt eine neue Ertragsquelle ohne
   Mehrarbeit – deshalb verkauft sie es aktiv.
8. **Traktion:** Second Nature: **42 Mio. $ Funding**, u. a. 16,4 Mio. $ Series C
   (2020) mit **MANN+HUMMEL** (deutscher Filterhersteller) als strategischem
   Investor; **>100.000 Abonnenten** [F-sek] –
   https://techcrunch.com/2020/03/25/secondnature-raises-16-4m-for-healthy-home-subscription-products-like-air-and-water-filters/ ,
   https://www.crunchbase.com/organization/secondnaturenow
9. **Übertragbarkeit DE: mittel, mit ernster Rechtshürde.**
10. **Hürden DE:** **Das deutsche Mietrecht ist der Blocker.** Die
    Betriebskostenverordnung (BetrKV) hat einen **abschließenden Katalog**
    umlagefähiger Kosten; „Concierge-Paket" oder „Bonitätsaufbau" gehören nicht
    dazu. Eine Zwangskopplung an den Mietvertrag wäre AGB-rechtlich angreifbar
    (§ 307 BGB) und möglicherweise ein unzulässiges Koppelungsgeschäft.
    **Umsetzbar nur als freiwilliges Mieter-Angebot** – damit fällt die
    Durchdringung von ~100 % auf vielleicht 10–20 % [A] und das Modell
    verliert seinen Kern. **Realistische Einstufung: eher niedrig als mittel.**
11. **Deutscher Klon: NEIN** – aus genau diesem Grund.
12. **Delegierbarkeit: hoch**, aber irrelevant bei blockiertem Kernmechanismus.

**Wert dieses Steckbriefs:** Er zeigt exemplarisch, dass eine Lücke auch eine
Rechtsschranke sein kann. Solche Fälle gehören in den Bericht, damit sie nicht
später als „Chance" wiederentdeckt werden.

---

### Modell 29 – Managed WiFi / Bulk Internet für Mehrfamilienobjekte

1. **Modellname:** Managed WiFi / Bulk Internet für MDU
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Elauwit – https://www.elauwit.com ; Wanaport –
   https://www.wanaport.com ; Quantum – https://quantumwi.fi
4. **Zielgruppe:** Eigentümer und Verwalter von Wohnanlagen ab ca. 50 Einheiten.
5. **Leistung:** Ein Netz für das gesamte Objekt; jeder Mieter erhält Internet
   ohne eigenen Vertrag; Verwaltung erhält Einnahmen oder Marge.
6. **Preisstruktur konkret:** Managed WiFi bis **40 $ pro Einheit/Monat**
   Zusatzertrag für die Immobilie; Bulk-Verträge **45–75 $ pro Einheit/Monat**
   (35–45 % günstiger als Einzelverträge); Wirtschaftlichkeitsschwelle ab
   **50+ Einheiten**, mindestens ~25; Fünfjahresvertrag über 200 Einheiten:
   **480.000–1,56 Mio. $ Gesamtumsatz, 8.000–26.000 $ Gewinn pro Monat** [F-sek] –
   https://quantumwi.fi/blog/bulk-internet-model/ ,
   https://www.adaptiv-networks.com/transforming-mdu-internet-services/
7. **USP:** Fünfjahresverträge mit einer Immobilie statt hunderte Einzelkunden –
   ideal nach Kriterium 5.
8. **Traktion:** keine Anbieterzahlen erhoben.
9. **Übertragbarkeit DE: mittel.**
10. **Hürden DE:** **Das „Nebenkostenprivileg" für Kabel-TV ist zum 30.06.2024
    entfallen** – die Umlage von Medienkosten über die Betriebskosten ist damit
    erschwert; für Glasfaser gibt es das befristete Glasfaserbereitstellungsentgelt
    (§ 72 TKG). Zusätzlich gilt der **Anbieterwechsel-Schutz des Endnutzers
    (§ 71 TKG)** – Zwangsanschluss ist unzulässig. Wer Internet an Mieter
    verkauft, ist **TKG-pflichtiger Anbieter** (Meldepflicht bei der
    Bundesnetzagentur, Kundenschutzpflichten, ggf. TKÜ-Pflichten) → **K.-o.-Prüfung
    Nr. 3 erforderlich; wahrscheinlich zu reguliert für Nicos Profil.**
11. **Deutscher Klon: schwach**, weil reguliert (Vodafone, Tele Columbus/PYUR
    dominieren die Objektversorgung).
12. **Delegierbarkeit: hoch**, aber Regulierung dominiert.

---

### Modell 30 – Route-Business Berufskleidung/Textil (Referenz für Routenökonomie)

1. **Modellname:** Uniform & Facility Services Rental
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Cintas – https://www.cintas.com ; UniFirst –
   https://www.unifirst.com
4. **Zielgruppe:** Produzierendes Gewerbe, Gastronomie, Werkstätten, Gesundheitswesen.
5. **Leistung:** Wöchentliche Anfahrt: getragene Kleidung abholen, saubere
   liefern, gleichzeitig Fußmatten, Wischmopps, Sanitärbedarf auffüllen.
6. **Preisstruktur konkret:** Wochenpreise pro Mitarbeiter/Artikel; keine
   Listenpreise erhoben. **Mehrjahresverträge mit automatischer Verlängerung**
   [F-sek].
7. **USP:** **Routendichte.** „Mit steigender Kundendichte in einer Region wird
   jede Route effizienter, was Margen und Rendite verbessert" [F-sek].
8. **Traktion (harte Zahlen):** Cintas **Bruttomarge 1,45 Mrd. $ = 51,0 % vom
   Umsatz, Allzeithoch, +40 Basispunkte YoY** [F-sek]; Segment „Uniform Rental
   and Facility Services" = **~77 % des Konzernumsatzes** (Anfang 2026);
   **Übernahme von UniFirst für 5,5 Mrd. $**, kombiniert **~1,5 Mio. Kunden**,
   erwartete Synergien 375 Mio. $ in vier Jahren [F-sek] –
   https://www.investing.com/analysis/cintas-bets-big-on-route-density-as-the-unifirst-deal-rewrites-industry-economics-200672309 ,
   https://www.mdm.com/news/top-distributor-sectors/facilities-maintenance-mro/together-at-last-cintas-to-acquire-unifirst-for-5-5b/
9. **Übertragbarkeit DE: niedrig – Markt besetzt** (MEWA, Bardusch, Elis,
   CWS) [A, Marktkenntnis].
10. **Hürden DE:** Kapitalintensiv (Wäschereien), Tarifbindung.
11. **Deutscher Klon: JA, stark.**
12. **Delegierbarkeit: hoch.**

**Warum aufgenommen:** Die Zahl **51 % Bruttomarge bei einem physischen
Routengeschäft** [F-sek] ist der beste verfügbare Beleg dafür, dass Mechanik M4
funktioniert – und die Referenz, an der jedes deutsche Routen-Modell gemessen
werden muss.

---

### Modell 31 – Aktenvernichtung + Medizinabfall gebündelt (Compliance-Route)

1. **Modellname:** Compliance-driven Route Service (Shred + Med Waste)
2. **Herkunftsland:** USA
3. **Anbieter + URL:** MedWaste Management – https://www.medwastemngmt.com ;
   Red Bags – https://redbags.com ; Marktübersicht: https://bizbite.io/businesses/document-shredding
4. **Zielgruppe:** Arztpraxen, Kanzleien, Finanzdienstleister, Personalabteilungen.
5. **Leistung:** Regelmäßige Abholung, dokumentierte Vernichtung/Entsorgung,
   Vernichtungsnachweis.
6. **Preisstruktur konkret:** **100–150 $ pro Serviceeinsatz** bei
   Standardvolumen; **Verträge 12–36 Monate mit monatlicher automatischer
   Abrechnung**; **Churn 5–8 % pro Jahr** auf gesunden Routen; **Bruttomarge
   ca. 40 %**; Bewertung: **4–7x EBITDA** für wiederkehrenden Service, Einmal-
   Aufträge nur 1–3x oder gar nicht bewertet [F-sek] –
   https://bizbite.io/businesses/document-shredding ,
   https://ctacquisitions.com/prepare-your-business-for-sale/document-destruction-exit/ ,
   https://goneforgoodfranchise.com/how-to-start-a-paper-shredding-business/
7. **USP:** **Compliance-getrieben und rezessionsresistent** – HIPAA, GLBA,
   FACTA, SOX erzeugen die Nachfrage. Bündelung spart dem Kunden doppelte
   Grundgebühren und Kraftstoffzuschläge.
8. **Traktion:** Kategoriedaten, keine Einzelfirma.
9. **Übertragbarkeit DE: mittel.** DSGVO + DIN 66399 (Schutzklassen/
   Sicherheitsstufen der Datenträgervernichtung) erzeugen in DE einen mindestens
   gleich starken Pflichtdruck. Medizinabfall unterliegt der
   Abfallverzeichnisverordnung (AS 180104/180103).
10. **Hürden DE:** **Entsorgungsfachbetrieb-Zertifizierung** (§ 56 KrWG) und
    Beförderungserlaubnis (§ 54 KrWG) sind für gefährliche Abfälle
    erlaubnispflichtig → **K.-o.-Risiko Nr. 3**, wenn Medizinabfall der Kern ist.
    Reine Aktenvernichtung ist weniger reguliert (DIN 66399 ist Norm, keine
    Erlaubnis). **Bruttomarge 40 %** [F-sek] liegt unter Nicos Zielmarke von
    65 % und nahe der K.-o.-Schwelle von 45 %.
11. **Deutscher Klon: JA** (Rhenus Data Office, Reisswolf, Remondis) [A].
12. **Delegierbarkeit: hoch** operativ.

---

### Modell 32 – Altspeiseöl + Fettabscheider mit Software-Layer

1. **Modellname:** UCO/FOG Route mit Routen- und Prognose-Software
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Grease Connections – https://greaseconnections.com ;
   Software: Reiter Software – https://reiterusa.com , Route Simplified –
   https://routesimplified.com ; KI-Disposition: DispatchNode –
   https://www.dispatchnode.com/industries/grease-trap
4. **Zielgruppe:** Restaurants, Kantinen, Lebensmittelverarbeiter.
5. **Leistung:** Doppelrichtung – der Kunde **zahlt** für das Leeren des
   Fettabscheiders und **erhält Geld** für das Altspeiseöl. Bündelung bindet den
   Account.
6. **Preisstruktur konkret:** Altöl bringt **~210 $ pro Restaurant und Monat**,
   ca. **70 Gallonen pro Restaurant und Monat**; Skalierung von 150 auf 500
   Kunden = **378.000–1,26 Mio. $ Jahresumsatz**; ein Saugwagen mit 8–10
   Restaurants pro Tag erzeugt **2.500–4.500 $ Tagesumsatz** [F-sek] –
   https://greaseconnections.com/used-cooking-oil-pricing-guide/ ,
   https://greasetraplocator.com/used-cooking-oil-business/
7. **USP:** „Technologie ermöglicht Wachstum über die 200-Kunden-Mauer hinaus,
   an der die meisten UCO-Unternehmen stagnieren" [F-sek]. Reiter prognostiziert,
   **wie voll jeder Öltank in Wochen sein wird**, und plant die Route danach.
8. **Traktion:** Kategoriedaten.
9. **Übertragbarkeit DE: mittel.** Altspeiseöl ist in DE über die
   Biokraftstoffquote (THG-Quote) wertvoll; Fettabscheider-Entleerung ist über
   **DIN EN 1825 und die kommunalen Entwässerungssatzungen Pflicht** (Mechanik M1).
10. **Hürden DE:** Entsorgungsfachbetrieb (§ 56 KrWG), Transportgenehmigung,
    Nachweisverordnung. **K.-o.-Risiko Nr. 3, wenn selbst entsorgt wird.**
    Ausweg: **nur den Software- und Dispositionslayer verkaufen** – dann ist es
    Modell 33/8 statt eines Entsorgungsgeschäfts.
11. **Deutscher Klon: teilweise** (Entsorger existieren, Software-Layer schwach) [A].
12. **Delegierbarkeit: hoch** operativ, aber Fuhrpark = Kapital.

---

### Modell 33 – Industrielles Vending / Vendor Managed Inventory

1. **Modellname:** Industrial Vending / FMI / Onsite
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Fastenal – https://www.fastenal.com/fast/services-and-solutions/fastvend ;
   AutoCrib – https://fastenertool.com/vmi-solutions/autocrib-vendor-managed-inventory/
4. **Zielgruppe:** Produzierende Betriebe, Werkstätten, Instandhaltung.
5. **Leistung:** Ausgabeautomat für Verbrauchsmaterial (Handschuhe, Bohrer,
   Schleifmittel, PSA) direkt an der Verbrauchsstelle; automatische
   Nachbestellung; Verbrauchsauswertung; teils eigenes Personal und
   Mikro-Lager beim Kunden („Onsite").
6. **Preisstruktur konkret:** Der Automat ist meist kostenlos, der Ertrag kommt
   aus dem Verbrauchsmaterial – klassische Rasierklingen-Logik. Keine
   Listenpreise erhoben.
7. **USP:** **Über 40.000 installierte Automaten weltweit** [F-sek]; der Automat
   ist physischer Lock-in – solange er in der Halle steht, kauft der Kunde dort.
8. **Traktion:** Fastenal ist börsennotiert; Kategorieführer [F-sek] –
   https://www.fastenal.com/content/solutions/pdf/vending.pdf
9. **Übertragbarkeit DE: mittel.** In DE besetzen Würth, Hoffmann Group und
   Hahn+Kolb Teile davon; der **Software- und Datenlayer** (Verbrauchsanalytik,
   Kostenstellenzuordnung, automatische Disposition) ist schwächer ausgeprägt [A].
10. **Hürden DE:** Betriebsrat bei personenbezogener Entnahmeerfassung
    (§ 87 BetrVG!), Kapitalbindung im Warenbestand, niedrige Handelsmarge →
    K.-o. Nr. 5 prüfen.
11. **Deutscher Klon: schwach im Software-Layer, stark im Handel.**
12. **Delegierbarkeit: hoch.**

---

### Modell 34 – Micro Markets / Unattended Retail

1. **Modellname:** Micro Market (unbeaufsichtigter Selbstbedienungs-Shop)
2. **Herkunftsland:** USA
3. **Anbieter + URL:** 365 Retail Markets – https://365retailmarkets.com ;
   Micromart, Seaga
4. **Zielgruppe:** Betriebe mit 100+ Mitarbeitern ohne Kantine, Logistikzentren,
   Krankenhäuser, Hotels.
5. **Leistung:** Offene Regale + Kühlung + Selbstbedienungs-Kiosk mit
   Kartenzahlung, 24/7 nutzbar, betrieben durch einen Operator.
6. **Preisstruktur konkret (gute Zahlen):** Ein Micro Market in einem Büro mit
   200+ Mitarbeitern erzielt **19.000–25.000 $ Rohertrag pro Jahr nach
   Warenkosten**; Micro Markets erzielen **30–50 % mehr Umsatz pro Standort** als
   Automaten; **>35.000 aktive Micro Markets in Nordamerika**, Standortzahl
   **+28 % in einem Jahr**, Kategorie **>1 Mrd. $ Jahresumsatz**; Konsumenten
   gaben **53 % mehr** aus als an Automaten (2024) [F-sek] –
   https://vmfsusa.com/blogs/business/micro-markets-operator-guide ,
   https://365retailmarkets.com/blog/expanding-your-vending-business-strategies-smart-store-micro-markets
   **Rechnung [S]:** 100.000 €/Monat = 1,2 Mio. €/Jahr Rohertrag ÷ 22.000 $
   je Standort ≈ **55 Standorte** – erreichbar, aber mit hohem
   Logistikaufwand pro Standort.
7. **USP:** Höherer Umsatz je Fläche als Automaten, keine Personalkosten am
   Standort, 100 % des Ertrags beim Operator (keine Umsatzbeteiligung).
8. **Traktion:** siehe oben, Kategoriedaten belegt.
9. **Übertragbarkeit DE: mittel.** Nachfrage besteht (Kantinensterben,
   Schichtbetriebe). Aber: **Diebstahlquote ist der Killer** – das US-Modell
   basiert auf Vertrauen in geschlossenen Betriebsgeländen.
10. **Hürden DE:** Lebensmittelhygiene (EU-VO 852/2004, HACCP-Konzept),
    Preisangabenverordnung, Pfandpflicht (Rücknahme!), Kassensicherungsverordnung
    (§ 146a AO, TSE-Pflicht für elektronische Kassen), Betriebsrat bei
    Mitarbeiterausweis-Bezahlung. Das ist viel Verwaltung – **kollidiert mit
    Nicos Anti-Kriterium „Unterlagen prüfen, Fristen verwalten"**.
11. **Deutscher Klon: schwach** (Selecta, Aramark bieten Ansätze) [A].
12. **Delegierbarkeit: hoch** operativ (Nachfüllrouten), niedrig administrativ.

---

### Modell 35 – Speech Analytics für den Außendienst ⭐

1. **Modellname:** Virtual Ride-Along / Conversation Intelligence für Feldverkauf
2. **Herkunftsland:** USA
3. **Anbieter + URL:** Rilla – https://www.rilla.com
4. **Zielgruppe:** Home-Services-Betriebe mit **5–50 Außendienstlern**,
   Ursprungssegment: Betriebe mit 5–50 Mio. $ Umsatz; heute auch Telekom, Solar,
   Versicherung.
5. **Leistung:** Der Verkäufer nimmt das Kundengespräch per App auf; KI
   transkribiert, analysiert, gibt Feedback; der Vertriebsleiter macht
   „virtuelle Mitfahrten" statt echter. Ein Leiter kann 30 statt 3 Verkäufer
   coachen.
6. **Preisstruktur konkret (sehr gut belegt):** **199–349 $ pro Vertriebler und
   Monat**; alternativ **4.000–5.000 $ pro Platz und Jahr, Minimum 5 Plätze →
   Einstieg ca. 20.000 $/Jahr** plus Implementierung [F-sek] –
   https://www.salesask.com/alternatives/rilla/rilla-pricing-guide-2026 ,
   https://sacra.com/c/rilla/
7. **USP:** Das Coaching-Nadelöhr im Außendienst wird aufgelöst. Der ROI ist
   direkt messbar (Abschlussquote, durchschnittlicher Auftragswert).
8. **Traktion (harte Zahlen):** **51 Mio. $ ARR (2025)** bei **ca. 2.000 Kunden**,
   **Net Revenue Retention > 115 %** (Anfang 2025), starker Cashflow [F-sek] –
   https://sacra.com/c/rilla/
   **Rechnung [S]:** 51 Mio. $ ÷ 2.000 Kunden = **25.500 $ Jahresumsatz pro
   Kunde** ≈ 2.125 $/Monat – konsistent mit 199–349 $ × ca. 7–10 Vertrieblern.
9. **Übertragbarkeit DE: HOCH, aber mit dem härtesten Rechtsvorbehalt im
   Bericht.** Das Problem (Vertriebscoaching skaliert nicht) ist in DE identisch.
   Nico hat mit CallSuite und `cs_arbeitszeit` bereits Vorarbeit in genau dieser
   Richtung (Anrufe, Erreicht, Termine – siehe Asset-Tabelle in 01).
10. **Hürden DE – hier liegt die Entscheidung:**
    - **Aufzeichnung von Kundengesprächen ohne Einwilligung ist in DE nach
      § 201 StGB strafbar** (Verletzung der Vertraulichkeit des Wortes). Das
      ist kein DSGVO-Bußgeld, das ist **Strafrecht**. Zulässig nur mit
      ausdrücklicher, dokumentierter Einwilligung *beider* Seiten.
    - **§ 87 Abs. 1 Nr. 6 BetrVG:** Leistungs- und Verhaltenskontrolle →
      Betriebsvereinbarung zwingend, wo ein Betriebsrat existiert.
    - Konsequenz: Das US-Produkt ist in DE **nicht 1:1 einsetzbar.** Die deutsche
      Variante muss entweder (a) mit expliziter Einwilligungsmechanik im
      Gesprächseinstieg arbeiten oder (b) auf **Telefonie** ausweichen, wo der
      Einwilligungs-Ansagetext etabliert ist – genau das Feld, in dem Nicos
      Twilio-Stack bereits produktiv läuft.
    - Sprachmodellqualität Deutsch: für Transkription inzwischen gut, für
      Coaching-Bewertung („war das eine gute Einwandbehandlung?") deutlich
      schwächer als Englisch [A].
11. **Deutscher Klon: NEIN gefunden.** Es gibt deutsche Conversation-Intelligence
    für Inside Sales/Callcenter, aber kein Äquivalent für den **Außendienst im
    Handwerk/Home Services** [A, kein DE-Suchlauf möglich → **Prüfauftrag**].
12. **Delegierbarkeit: hoch.** Reines SaaS, Onboarding standardisierbar.

---

### Modell 36 – White-Label-Reseller-Plattform für lokale Dienstleister

1. **Modellname:** Channel-/Reseller-Plattform (Marktplatz für Agenturen)
2. **Herkunftsland:** Kanada
3. **Anbieter + URL:** Vendasta – https://www.vendasta.com
4. **Zielgruppe:** **Agenturen, Medienhäuser, Telkos, Banken** – die ihrerseits
   lokale KMU bedienen.
5. **Leistung:** CRM + Marktplatz mit **250+ White-Label-Martech-Produkten**
   (Einträge, Reputation, Social, SEO, Websites), die der Partner unter eigener
   Marke weiterverkauft; wiederkehrende Rechnungsstellung inkl. Fremdprodukten.
6. **Preisstruktur konkret:** **Starter 99 $/Monat, Professional 499 $/Monat,
   Premium 999 $/Monat** – aber als **Mindestumsatz-Offset**: Die Plattformgebühr
   beträgt **0 $**, wenn der monatliche Wholesale-Produkteinkauf das Tier-Minimum
   erreicht; sonst wird das volle Minimum berechnet [F-sek] –
   https://checkthat.ai/brands/vendasta/pricing
7. **USP:** Das **Offset-Preismodell** ist bemerkenswert: Es macht die
   Plattform für erfolgreiche Partner kostenlos und bestraft nur Karteileichen.
   Perfekt ausgerichtete Anreize.
8. **Traktion:** keine Umsatzzahlen erhoben.
9. **Übertragbarkeit DE: mittel.** Das **Preismodell** ist hochgradig
   übertragbar auf jedes Partner-/Reseller-Modell in diesem Bericht.
10. **Hürden DE:** Wettbewerbsdichte im Agenturmarkt; deutsche Agenturen sind
    klein und kapitalschwach.
11. **Deutscher Klon: schwach** [A].
12. **Delegierbarkeit: hoch** – Partner-Enablement statt Endkunden-Support (wie
    Modell 13).

---

## 4. Ergänzende Umsatzbausteine (keine eigenständigen Maschinen)

Diese Elemente sind zu klein oder zu abhängig, um allein Maschine A zu sein,
aber sie erhöhen den Umsatz pro Kunde in mehreren der obigen Modelle erheblich.

| Baustein | Anbieter | Zahlen | Relevanz für DE |
|---|---|---|---|
| **Embedded Consumer Financing** | Wisetack | **3,9 % Transaktionsgebühr**, keine Setup-/Abogebühr, Darlehen 500–25.000 $ (Limit auf 65.000 $ erhöht), 0–35,9 % APR, Auszahlung in 1–3 Bankarbeitstagen; integriert in Jobber, ServiceTitan, Housecall Pro, FieldPulse, Service Fusion und 50+ Plattformen [F-sek] – https://www.wisetack.com/ , https://servicemag.org/software/wisetack | In DE Erlaubnispflicht (Kreditvermittlung § 34c GewO / § 34i GewO bzw. Kooperation mit Bank) → **direkter Konflikt mit Nicos K.-o. Nr. 3 und der Ausschlussliste**. Nicht empfohlen. |
| **Aerial Measurement as a Service** | EagleView | Standardreport **15–38 $**, Premium bis **87 $** (Bid Perfect); Abo „EagleView One" seit Juni 2025, quote-based; 98,77 % CompassData-verifizierte Genauigkeit; von Versicherungs-Schadenregulierern akzeptiert [F-sek] – https://roofingsoftwareguide.com/guides/eagleview-pricing/ | In DE Luftbildverfügbarkeit und Datenschutz anders; Dachdeckerhandwerk kleiner strukturiert. Mittel. |
| **Drohnen-Inspektion als Retainer** | diverse | Abo **1.500–3.000 $/Monat** bei wöchentlichen Flügen (mittelgroße Baustellen); wiederkehrende Verträge **15–25 % günstiger** als Einzelflüge; Solar: 300–500 $/MW; Dach gewerblich 600–3.500 $ [F-sek] – https://www.getmonetizely.com/articles/how-to-create-profitable-subscription-pricing-models-for-drone-inspection-services , https://dronebundle.com/blog/drone-inspection-services | In DE EU-Drohnenverordnung, Betriebsgenehmigung, Aufstiegserlaubnis – machbar, aber personengebunden (Pilot) → Delegierbarkeit mittel. |
| **Pay-per-Call-Leadgen** | Service Direct, 99calls | Exklusive Leads **30–80 $** (HVAC/Sanitär/Elektro); Home-Improvement-Leads 45–75 $ **plus 28,99 $/Monat**; Shared Leads konvertieren nur zu **5–15 %**, CAC über solche Plattformen ~**1.430 $** [F-sek] – https://servicedirect.com/ , https://clicksgeek.com/pay-per-lead-services/ | In DE existent (Aroundhome, DAA), aber Leadgen ist **kein wiederkehrender Umsatz im Sinne von Kriterium 1** und hoch volatil. Als Kernmodell abzulehnen. |
| **Solar-O&M-Vertrag** | diverse | Wohngebäude **~30 $/kW/Jahr** (US DOE) bzw. 100–300 $ Jahrespauschale; Gewerbe/Utility **10–20 $/kW/Jahr**; Monitoring 0–100 $/Jahr bis 100 kW [F-sek] – https://ppm.solar/commercial-solar-om-guide/ | In DE mit >4 Mio. PV-Anlagen [A] hohe Stückzahl, aber sehr niedrige Beträge pro Anlage → nur mit Portfoliokunden (Betreibergesellschaften) tragfähig. |
| **Submetering as a Service** | utiliVisor, Triacta | Submeter werden von privaten Firmen installiert und **über ein Abonnement überwacht**, das der Gebäudeeigentümer unterhalten muss [F-sek] – https://buildinginnovationhub.org/resource/improve-building-operations/energy-use-submetering-faq/ | In DE **eichrechtlich reguliert** (MessEG/MessEV) sobald abrechnungsrelevant; Messstellenbetrieb ist reguliert → K.-o.-Risiko. |
| **Safety-Training-Abo** | Vector Solutions | **>450 Kurse** im HSE-Premium-Katalog; Mengenrabatt ab 5 Plätzen 10–20 %, ab 50 Plätzen mehr, Richtwert ~120 $/Platz [F-sek] – https://www.vectorsolutions.com/ | In DE existiert Pflicht (jährliche Unterweisung nach § 12 ArbSchG, DGUV V1) → Mechanik M1. Markt aber besetzt. |

---

## 5. Querschnittsauswertung

### 5.1 Die acht am besten nach Deutschland übertragbaren Modelle

Auswahlkriterien: (a) Pflicht- oder Kostendruck erzeugt die Nachfrage,
(b) Zielkunde ist B2B mit wenigen, hochwertigen Accounts, (c) Nico ist strukturell
nicht Leistungserbringer, (d) kein K.-o. nach Abschnitt 6 der Grundlage,
(e) DE-Klon schwach oder nicht vorhanden.

| Rang | Modell | Kern-Begründung | Größte Gefahr |
|---|---|---|---|
| 1 | **#22 Sensor-Monitoring als Motor für Wartungs-Mitgliedschaften** (SmartAC) | Verkauf an SHK-Betriebe, nicht Endkunden. Wärmepumpen-Hochlauf + GEG erzeugen die Nachfrage. 200 Betriebe × 500 € = 100k €/Monat [S]. Passt exakt zu Nicos Technikinteresse und hält ihn aus dem Endkundensupport. | Heizungshersteller schließen die Schnittstelle. Gegenmittel: herstellerunabhängige Nachrüstsensorik. |
| 2 | **#7 Compliance-SaaS für Wärmepumpen-/PV-/Wallbox-Installateure** (Payaca) | DE hat mit BEG/BAFA/KfW/GEG/VDE-Anmeldung einen deutlich komplexeren Förder- und Nachweisstack als UK. Deutsche Handwerkersoftware ist generalistisch – die Nische ist offen. | Förderrecht ändert sich ständig (zugleich der Burggraben). Plancraft/HERO könnten das Modul nachbauen. |
| 3 | **#19 Mobile Überwachungseinheit als Mietabo** (LVT) | 1.200–3.400 $/Einheit/Monat [F-sek], Amortisation ~20 Monate [S], wenige Großkunden, physisch-technisch (Nicos Interessenprofil), beste Delegierbarkeit der physischen Modelle. | Kapitalintensiv – 56 Einheiten für 100k €/Monat = ~1,4 Mio. € Assets [S]. Braucht Leasing. § 34a GewO über NSL-Partner umgehen. |
| 4 | **#8 Brandschutz-/Prüf-SaaS** (Inspect Point) | Pflichtprüfungen (DIN 14675, DGUV V3, PrüfVO) + „Mangel wird automatisch zum Angebot". Höchste Retention aller Modelle. | DIN-/VDE-Normtexte sind lizenzpflichtig. Ohne Lizenz kein Produkt – mit Lizenz ein Burggraben. |
| 5 | **#13 vCISO-/Compliance-Plattform für Dienstleister** (Cynomi) | NIS2 zwingt zehntausende deutsche Mittelständler ab sofort. Verkauf an MSPs = ein Gespräch, 30 Endkunden. Bester Delegations-Hebel im Bericht: Endkundensupport liegt strukturell beim Partner. | Sobald man selbst vCISO ist, entsteht Haftung (K.-o. Nr. 9). Strikt Plattform bleiben. |
| 6 | **#27 Herstellerunabhängiges Aufzug-IoT** (uptime.ac) | Die vier großen Aufzugkonzerne monitoren nur eigene Anlagen; freie Wartungsfirmen mit Mischbestand haben nichts. Nachrüstsensorik installiert der Kunde selbst. 200 Kunden in Europa belegen den Markt [F-sek]. | Sicherheitsrelevanz – nur auslesend, nie steuernd, sonst Konformitätsbewertung. DE-Klon-Prüfung offen. |
| 7 | **#35 Speech Analytics für den Außendienst** (Rilla) | 51 Mio. $ ARR bei 2.000 Kunden, NRR >115 % [F-sek]. 199–349 $/Rep/Monat. Nico hat mit CallSuite/Twilio den Stack schon. | **§ 201 StGB** – Gesprächsaufzeichnung ohne Einwilligung ist strafbar. Nur mit sauberer Einwilligungsmechanik, am besten telefoniebasiert. |
| 8 | **#14 Vertikal spezialisierter MSP** (Dental/Veterinär) | 1.500 €/Monat × 67 Kunden = 100k €/Monat [S]. Nur 0,17 % Marktanteil nötig. Extrem berechenbarer Umsatz. | Bruttomarge 45–60 % [A] unter Nicos Ziel; Helpdesk braucht Personal ab Tag 1; § 203 StGB bei Heilberufen. |

**Nicht in die Top 8, obwohl wirtschaftlich stark:** #4 ServiceTitan
(Kapitalwettlauf, verstößt gegen A1/A10), #30 Cintas (Markt besetzt, kapitalintensiv),
#26 WINT (Versichererkanal = Anzug-Business), #34 Micro Markets (Verwaltungslast
kollidiert mit Nicos Anti-Kriterien), #28 RBP (deutsches Mietrecht blockiert
den Kernmechanismus), #29 MDU-Internet (TKG-reguliert).

---

### 5.2 Die drei größten „in Deutschland noch offen"-Lücken

**Lücke 1 – Der Handwerksbetrieb als Kunde eines Enablement-Produkts, nicht als
Softwarenutzer.**
Der deutsche Markt verkauft dem Handwerker **Verwaltungssoftware**
(15–120 €/Nutzer/Monat [F-sek]) und drückt dabei die Preise gegenseitig
(ToolTime hat gesenkt [F-sek]). Der US-/UK-Markt verkauft dem Handwerker
**zusätzlichen Umsatz**: SmartAC verkauft ihm Mitgliedschaften (~1.000 $/Jahr
pro Endkunde, 97 % Retention [F-sek]), Rilla verkauft ihm Abschlussquote
(199–349 $/Rep/Monat [F-sek]), Inspect Point verwandelt Prüfmängel in
Angebote, Payaca verkauft ihm die Förderbürokratie weg. **In Deutschland
existiert praktisch kein Anbieter, der dem Handwerksbetrieb ein Produkt
verkauft, dessen ROI in Euro Mehrumsatz statt in gesparten Bürostunden
gemessen wird.** Das ist die größte und am schnellsten adressierbare Lücke.
Zahlungsbereitschaft folgt automatisch: Ein Betrieb, der 500 €/Monat zahlt und
3.000 €/Monat Mehrumsatz sieht, kündigt nicht.

**Lücke 2 – Herstellerunabhängige Nachrüst-Sensorik mit Service-Layer für
Bestandsanlagen.**
Drei unabhängige Fälle in dieser Recherche zeigen dasselbe Muster: uptime.ac
(Aufzüge, brand-agnostic, 200 Kunden in Europa), Otodata (Tanks, ab 1,50 $/Monat
Einkauf gegen 26–54 $ Weiterverkauf), SmartAC (HVAC). Gemeinsamer Nenner: Der
**Anlagenhersteller** baut Konnektivität nur für seine eigenen Geräte; der
**Serviceunternehmer mit gemischtem Bestand** hat kein Werkzeug. Deutschland
ist ein Bestandsanlagen-Land par excellence – 800.000 Aufzüge [A],
Millionen Heizungen, hunderttausende Kälteanlagen, alle von unabhängigen
Servicefirmen gewartet. **Es fehlt der neutrale Layer.** Die Rechtslage ist
günstig (kein K.-o., solange nur ausgelesen und nicht gesteuert wird), die
Marge ist gut (67 % im Otodata-Fall [S]), und die Delegierbarkeit ist hoch,
weil der Kunde selbst installiert.

**Lücke 3 – Compliance-Software, die aus der Pflicht ein Verkaufsereignis macht.**
Deutschland hat mehr Prüf- und Nachweispflichten als jedes der untersuchten
Länder: DGUV V3, DIN 14675, VDI 6023/TrinkwV, BetrSichV, GefStoffV, GEG,
DIN EN 1825, NIS2. Deutsche Anbieter bauen daraus **Dokumentationswerkzeuge**.
Die angelsächsischen Anbieter bauen daraus **Vertriebssysteme**: Inspect Point
erzeugt aus jedem Mangel ein Angebot, SwiftComply eskaliert automatisch an
säumige Eigentümer, Cynomi erzeugt aus der Lücke den Dienstleistungsauftrag.
**Der Unterschied ist nicht technisch, er ist konzeptionell** – und deshalb
kopierbar, ohne einen Kapitalwettlauf zu führen. Zusatzbefund: Der Zeitpunkt
für NIS2 (Modell 13) ist jetzt, weil die Umsetzungspflicht gerade greift und
der Mittelstand weder Personal noch Prozess hat.

---

### 5.3 Übertragbare Preis- und Vertragsmechaniken (unabhängig vom Modell)

Diese Mechaniken sind in DE unterrepräsentiert und lassen sich auf jedes
gewählte Modell aufsetzen:

1. **Volumen- statt Sitzplatzpreis** (ServiceM8: 29–349 AUD nach Auftragszahl
   [F-sek]) – beseitigt den häufigsten Kaufeinwand im Handwerk.
2. **Netto-positive Preisgestaltung** (BrainBox AI: „Monatsgebühr liegt unter der
   Einsparung" [F-sek]) – der Kunde kann rechnerisch nicht verlieren.
3. **Pay-for-Performance** (Numa: Zahlung nur für gebuchte Termine [F-sek]) –
   senkt die Einstiegshürde radikal, erfordert aber saubere Attribution.
4. **Mindestumsatz-Offset** (Vendasta: Plattformgebühr 0 $, wenn Wholesale-Einkauf
   das Tier-Minimum erreicht [F-sek]) – ideal für Partner-Modelle.
5. **Miete statt Verkauf bei physischen Assets** (LVT: 45.000 $ Asset erzeugt
   2.300 $/Monat, Amortisation ~20 Monate [S]).
6. **Weiterverkaufsmarge auf fremder Sensorik** (Otodata: 1,50 $ Einkauf,
   26–54 $ Verkaufspreis am Markt [F-sek]) – Hardware **nie** selbst entwickeln
   (Blackline: 4,1 % EBITDA-Marge [S] als Warnung).
7. **Setup-Gebühr + Monatsgebühr** ist im deutschen KI-Telefoniemarkt bereits
   etabliert (FoxifAI: 1.920 € Setup + ab 100 €/Monat [F-sek]) – belegt, dass
   deutsche KMU eine Einrichtungsgebühr akzeptieren (Kriterium 18 ✅).

---

### 5.4 Warnungen und Friedhofsbefunde

| Befund | Beleg | Konsequenz |
|---|---|---|
| Hardware-Eigenentwicklung zerstört die Marge | Blackline Safety: 6,1 Mio. $ adj. EBITDA auf 150,5 Mio. $ Umsatz FY2025 = **4,1 %** [S aus F] | Nicos Ziel ist 30 % EBITDA. Hardware nur zukaufen. |
| Route-Geschäfte sind margenbegrenzt | Aktenvernichtung **~40 % Bruttomarge** [F-sek]; Cintas als Weltklasse-Benchmark **51 %** [F-sek] | Nicos Ziel ≥ 65 % Bruttomarge ist mit reinen Routengeschäften nicht erreichbar. |
| Der deutsche KI-Telefonassistenzmarkt ist bereits im Preiskampf | DE 39–89 €/Monat [F-sek] vs. US 199–3.000 $/Monat [F-sek] | Markteintritt dort bedeutet Wettbewerb über Preis → K.-o. Nr. 6. |
| Manche „Lücken" sind Rechtsschranken, keine Chancen | Dashcam-Innenraumaufnahme (BetrVG/DSGVO), RBP (BetrKV/§ 307 BGB), MDU-Internet (TKG), Gesprächsaufzeichnung (§ 201 StGB) | Jede identifizierte Lücke muss gegen die Frage geprüft werden: fehlt hier ein Anbieter oder eine Erlaubnis? |
| Vertikales SaaS wird teuer eingekauft – aber auch teuer aufgebaut | Vertikales SaaS handelt mit **25–30 % Bewertungsaufschlag** ggü. horizontalem; mit Embedded Fintech **7–9,5x Umsatz** vs. 4,8–6,2x; PE-Rekord **73 Vertical-SaaS-Deals über 15,3 Mrd. $ in Q1 2025** [F-sek] – https://www.saasmag.com/vertical-saas-outperforming-horizontal-2026/ , https://skalingventures.substack.com/p/defining-the-saas-ecosystem-and-niche | Unternehmenswert (Kriterium 8) ist bei vertikalem SaaS belegbar hoch – das stützt die Top-8-Auswahl. |
| Blue-Collar-Branchen wehren sich gegen Software | „In Sektoren, die noch mehr offline als online sind – Bau, Logistik, Fertigung – stoßen SaaS-Tools oft auf Zynismus oder offene Ablehnung" [F-sek] – https://www.newarkventurepartners.com/blog/the-blue-collar-tech-sales-playbook/ | Der Vertrieb ist die eigentliche Schwierigkeit, nicht das Produkt. Passt allerdings zu Nicos Stärke („stark im Verkaufen, Präsentieren, Überzeugen"). |

---

## 6. Offene Prüfaufträge (an Orchestrator und Agenten 01, 03, 08)

Diese Punkte konnten wegen erschöpftem Suchbudget und blockiertem WebFetch
**nicht** verifiziert werden und dürfen bis zur Prüfung nicht als Fakt gelten:

| # | Prüfauftrag | Betrifft Modell | Priorität |
|---|---|---|---|
| P1 | Existiert in DE ein Anbieter für herstellerunabhängiges Heizungs-/Wärmepumpen-Monitoring, das an **SHK-Betriebe** verkauft wird? (gegen Vaillant, Viessmann, Bosch, 1Komma5Grad, thermondo prüfen) | 22 | **sehr hoch** |
| P2 | Existiert in DE eine Handwerkersoftware mit **BEG/BAFA/KfW/GEG-Compliance-Modul**? (gegen Plancraft, HERO, ToolTime, ZVSHK-Tools, enerchart prüfen) | 7 | **sehr hoch** |
| P3 | DGUV-V3-/Prüffristen-Softwaremarkt DE: Anbieter, Preise, Reifegrad | 8 | hoch |
| P4 | Aufzug-Monitoring DE: Digital Spine, Aufzughelden und weitere – Marktdurchdringung und Preise | 27 | hoch |
| P5 | Deutsche NIS2-Enablement-Plattformen für MSPs (gegen Enginsight, Hornetsecurity, indevis, DriveLock prüfen) | 13 | hoch |
| P6 | Deutsche Anbieter für Baustellen-Videoüberwachung als **standardisiertes Mietabo** mit Solaranhängerflotte; Preisniveau in € | 19 | hoch |
| P7 | Deutsche Conversation-Intelligence für Außendienst; Rechtsgutachten § 201 StGB + § 87 BetrVG zur zulässigen Produktgestaltung | 35 | hoch |
| P8 | Legionellen-/TrinkwV-Compliance-Software DE: Anbieter und Preise | 10 | mittel |
| P9 | Verifikation aller mit [F-sek] gekennzeichneten Preise auf den Herstellerseiten (WebFetch war blockiert) | alle | mittel |
| P10 | Größenordnungen, die als [A] markiert sind: Anzahl SHK-Betriebe DE, Kfz-Betriebe DE, Aufzugsanlagen DE, Zahnarztpraxen DE | 2, 14, 22, 27 | mittel |

---

## 7. Vollständige Quellenliste

**AI-Telefonie / Voice-AI**
- https://pipelineon.com/blog/ai-receptionist-contractor/
- https://www.getnextphone.com/blog/ai-receptionist-pricing-guide
- https://www.avoca.ai/blog/how-much-does-an-answering-service-cost-a-guide-for-businesses
- https://www.prnewswire.com/news-releases/avoca-raises-125m-at-1b-valuation-to-power-americas-services-economy-with-ai-302753962.html
- https://serviceagent.ai/blogs/avoca-ai-pricing/
- https://oncrew.ai/blog/numa-pricing-2026
- https://serviceagent.ai/blogs/numa-pricing/
- https://www.prnewswire.com/news-releases/numa-unveils-the-first-ai-agent-platform-for-auto-dealerships-302350393.html
- https://loman.ai/blog/slang-ai-reviews-pricing-alternatives
- https://www.perfectvenue.com/post/slang-ai-review
- https://www.forbes.com/sites/quickerbettertech/2025/10/02/for-restaurants-slang-ai-is-a-great-example-of-an-ai-platform-using-voice-recognition-for-roi/
- https://speakki.de/blog/ki-telefonassistent-kosten
- https://www.placetel.de/ratgeber/ki-telefonassistent
- https://vokaro.net/kosten/ki-telefonassistent-kosten
- https://agentino.de/

**Vertical SaaS / Field Service**
- https://www.saastr.com/5-interesting-learnings-from-servicetitan-at-1b-in-arr/
- https://sacra.com/c/servicetitan/
- https://www.wing.vc/content/servicetitans-ipo-a-deep-dive
- https://www.itqlick.com/compare/jobber/housecall-pro
- https://stackpick.com.au/servicem8-review-australia/
- https://stackpick.com.au/tradify-pricing-australia/
- https://www.itrade.net/post/job-scheduling-software-uk-compare-the-best-options-for-trades-businesses
- https://www.softwareadvice.co.uk/software/126649/bigchange
- https://www.commusoft.com/en-gb/blog/best-field-service-management-software-uk/
- https://trusted.de/handwerkersoftware
- https://agentino.de/blog/handwerker-software-vergleich-beste-tools/
- https://www.saasmag.com/vertical-saas-outperforming-horizontal-2026/
- https://www.newarkventurepartners.com/blog/the-blue-collar-tech-sales-playbook/
- https://skalingventures.substack.com/p/defining-the-saas-ecosystem-and-niche

**Compliance / Prüf-SaaS**
- https://www.inspectpoint.com/
- https://www.softwareadvice.com/fleet-management/inspect-point-profile/
- https://capterra.com/p/148287/Inspect-Point/
- https://www.swiftcomply.com/backflow-prevention-software/
- https://www.thecomplianceengine.com/backflow
- https://www.briqsafe.com/
- https://www.legionella-software.co.uk/
- https://collabitsoftware.com/water-hygiene-and-treatment-software/
- https://getlatka.com/companies/ecoonline.com
- https://summaequity.com/investments/ecoonline/
- https://checkthat.ai/brands/ecoonline/pricing
- https://www.g2.com/products/safetyculturehq/pricing
- https://www.educate-me.co/blog/safetyculture-pricing
- https://getlatka.com/companies/safetyculture.com
- https://pitchbook.com/profiles/company/60535-18
- https://trycomp.ai/soc-2-cost-breakdown
- https://www.globenewswire.com/news-release/2025/04/23/3066238/0/en/Cynomi-Secures-37M-in-Series-B-Funding-to-Expand-Agentic-AI-Cybersecurity-Platform-Capabilities-for-Service-Providers.html
- https://www.msspalert.com/news/cynomi-nets-37-million-to-expand-agentic-ai-in-vciso-platform
- https://www.vectorsolutions.com/

**Managed Services / MSP**
- https://www.flamingo.run/blog/msp-pricing-models
- https://www.pact-one.com/2024/03/best-dental-it-companies-in-the-united-states/
- https://www.darkhorsetech.com/blogs/the-best-dental-it-support-companies-of-2025
- https://cortavo.com/cortavo-guides/managed-it-services-healthcare-providers
- https://tacticsmarketing.com/blog/the-niche-isnt-a-constraint.-its-the-moat
- https://www.comprobusiness.com/insights/the-ultimate-guide-to-managed-print-services/
- https://www.cds-yes.com/blog-post/managed-print-services-cost-pricing-guide

**Hardware + Abo / IoT / Monitoring**
- https://www.businesswire.com/news/home/20260312637663/en/Blackline-Safety-Reports-Record-First-Quarter-2026-Revenue-of-$38.8-million-and-Record-First-Quarter-Adjusted-EBITDA-of-$1.7-million
- https://www.shashi.co/2026/04/blackline-safety-goes-private-what.html
- https://airpinpoint.com/compare/samsara-pricing
- https://tech.co/fleet-management/samsara-vs-motive
- https://www.security.org/home-security-systems/deep-sentinel/
- https://www.retaildive.com/press-release/20250630-deep-sentinel-unveils-sentinelnow-remote-live-guard-security-on-demand-for
- https://www.spot.ai/blog/liveview-technologies-pricing-2026
- https://securenh.com/lvt-mobile-surveillance-unit-prices-monthly-costs/
- https://servicerobotco.com/pricing/robot-pricing-guide
- https://sproutmation.com/blog/complete-guide-cleaning-robot-rental-programs-2026
- https://www.smartac.com/
- https://www.smartac.com/blog/how-smart-ac-technology-boosts-service-membership-sales
- https://www.citybiz.co/article/830798/sensors-memberships-and-recurring-revenue-smartac-and-certainpath-are-rewiring-hvac-growth/
- https://www.prnewswire.com/news-releases/smartac-helps-iceberg-home-services-drive-proactive-hvac-service-and-80k-in-new-revenue-302684703.html
- https://brainboxai.com/decarbonization-solution-that-pays-for-itself
- https://bpnews.com/feature-articles/tank-monitoring-solutions-monitors-portals-apps
- https://www.aeris.com/resources/otodata-smarter-monitoring/
- https://www.smartsense.co/food-service/restaurants/
- https://techcrunch.com/2023/08/10/water-intelligence-startup-wint-nabs-35m-to-help-companies-find-and-stop-leaks/
- https://www.timesofisrael.com/israeli-smart-water-leak-detection-startup-raises-35-million-from-funding-round/
- https://eustartup.news/startup-showcase-uptime-ac-the-leading-iot-predictive-technology-for-elevators/
- https://www.crunchbase.com/organization/uptime-ac
- https://www.serena.vc/portfolio-profile/uptime/

**Equipment as a Service**
- https://www.machinemetrics.com/blog/what-is-equipment-as-a-service
- https://www.3ds.com/industries/industrial-equipment/equipment-as-service
- https://shoplogix.com/blog/equipment-as-a-service/
- https://limble.com/learn/equipment-as-service

**Route-Businesses**
- https://www.investing.com/analysis/cintas-bets-big-on-route-density-as-the-unifirst-deal-rewrites-industry-economics-200672309
- https://www.mdm.com/news/top-distributor-sectors/facilities-maintenance-mro/together-at-last-cintas-to-acquire-unifirst-for-5-5b/
- https://bizbite.io/businesses/document-shredding
- https://ctacquisitions.com/prepare-your-business-for-sale/document-destruction-exit/
- https://goneforgoodfranchise.com/how-to-start-a-paper-shredding-business/
- https://redbags.com/shredding-medical-waste-combo/
- https://greaseconnections.com/used-cooking-oil-pricing-guide/
- https://greasetraplocator.com/used-cooking-oil-business/
- https://routesimplified.com/blog/makes-the-used-cooking-oil-collector-job-easier/
- https://www.dispatchnode.com/industries/grease-trap
- https://www.pestpac.com/blog/best-pest-control-scheduling-software
- https://www.fieldproxy.ai/resources/blog/pest-control-business-guide-from-route-planning-to-recurring-revenue-d1-27
- https://www.fastenal.com/content/solutions/pdf/vending.pdf
- https://www.fastenal.com/fast/services-and-solutions/fastvend
- https://vmfsusa.com/blogs/business/micro-markets-operator-guide
- https://365retailmarkets.com/blog/expanding-your-vending-business-strategies-smart-store-micro-markets

**Immobilien-/Ancillary-Modelle**
- https://butterflymx.com/blog/resident-benefits-package/
- https://latchel.com/how-to-increase-revenue-per-unit-with-a-resident-benefits-package/
- https://www.secondnature.com/blog/what-is-a-resident-benefits-package
- https://techcrunch.com/2020/03/25/secondnature-raises-16-4m-for-healthy-home-subscription-products-like-air-and-water-filters/
- https://www.crunchbase.com/organization/secondnaturenow
- https://quantumwi.fi/blog/bulk-internet-model/
- https://www.adaptiv-networks.com/transforming-mdu-internet-services/
- https://www.elauwit.com/resources/bulk-internet-for-multifamily-your-top-questions-answered

**Vertrieb / Umsatzbausteine**
- https://sacra.com/c/rilla/
- https://www.salesask.com/alternatives/rilla/rilla-pricing-guide-2026
- https://astucia.io/blog/podium-pricing-2026-what-smbs-actually-pay
- https://www.socialpilot.co/reviews/blogs/podium-pricing
- https://checkthat.ai/brands/vendasta/pricing
- https://www.vendasta.com/platform/
- https://www.wisetack.com/
- https://servicemag.org/software/wisetack
- https://roofingsoftwareguide.com/guides/eagleview-pricing/
- https://www.getmonetizely.com/articles/how-to-create-profitable-subscription-pricing-models-for-drone-inspection-services
- https://dronebundle.com/blog/drone-inspection-services
- https://servicedirect.com/
- https://clicksgeek.com/pay-per-lead-services/
- https://ppm.solar/commercial-solar-om-guide/
- https://buildinginnovationhub.org/resource/improve-building-operations/energy-use-submetering-faq/
- https://www.tidemarkcap.com/vskp-chapter/marketplace-take-rates

**Nordische / EU-Referenzen**
- https://www.netguru.com/blog/nordic-greentechs
- https://sifted.eu/articles/nordic-soonicorn-unicorn-startup-list
- https://www.vccafe.com/vertical-ai-market-map-2026-israeli-startups-and-funding-rounds/
- https://www.ampeco.com/ev-charging-solutions/charge-point-operator/
- https://chargedevs.com/newswire/monta-acquires-abb-nordics-ev-charge-point-management-software-customer-contracts-through-vourity-deal/

---

*Ende Agent 02. Alle Zahlen sind gekennzeichnet. Alle nicht verifizierbaren
Aussagen sind als [A] mit Prüfauftrag markiert. Es wurden keine Zahlen erfunden.*
