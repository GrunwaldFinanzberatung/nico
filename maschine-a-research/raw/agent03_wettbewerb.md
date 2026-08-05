# Agent 03 – Wettbewerbs- und Produktanalyse

Stand: 2026-08-05 · Agent 3 · Wellen-1-Output
Bezug: `01_nordstern_und_anforderungen.md`, `02_research_methodik.md`

---

## 0. DATENLAGE UND METHODENWARNUNG — BITTE ZUERST LESEN

Dieser Bericht ist **nicht vollständig recherchiert**. Die Ursache ist technisch,
nicht inhaltlich, und muss offengelegt werden, weil sie die Belastbarkeit
einzelner Abschnitte direkt bestimmt.

| Kanal | Status | Wirkung |
|---|---|---|
| WebSearch | **Budget der gesamten Session erschöpft** (200 von 200 Aufrufen; geteilt mit den parallel laufenden Agenten) | Nach 16 eigenen Suchanfragen abgebrochen |
| WebFetch (direkte Preisseiten) | **Vollständig blockiert** durch die Egress-Policy der Umgebung — HTTP 403 auf *jedem* Host, inklusive `wikipedia.org` | Keine einzige Preisseite konnte direkt gelesen werden |
| curl über den Agent-Proxy | Blockiert (`CONNECT tunnel failed, 403`) | Kein Ersatzweg |

**Konsequenz für die Auswertung:**

- **Feld A (KI-Telefonie)** ist belastbar recherchiert. 14 der 16 verfügbaren
  Suchanfragen gingen hierhin. Preise stammen aus Suchergebnis-Extrakten, nicht
  aus den Preisseiten selbst — sie sind daher **[F] mit Einschränkung**: die Zahl
  ist belegt, die Quelle ist ein Aggregator-/Vergleichsartikel, nicht der
  Anbieter selbst. Das ist bei Vergleichsportalen im Voice-AI-Umfeld relevant,
  weil viele dieser Artikel von Wettbewerbern betrieben werden (siehe §1.6).
- **Feld B (Handwerkersoftware)** ist teilrecherchiert: 4 Anbieter mit echten
  Preisen, der Rest fehlt.
- **Feld C (Monitoring/Wartung mit Hardware)** ist **nicht recherchiert**.
  Ich habe dazu **keine einzige verifizierte Preisangabe**. Nach Regel 2 der
  Methodik (`02_research_methodik.md`) wäre jede Preisnennung hier eine
  erfundene Zahl. Ich nenne daher **keine Preise für Feld C**, sondern
  formuliere den Strukturbefund und einen präzisen Nachrecherche-Auftrag.
  Das ist die ehrliche Antwort — nicht die vollständige.

**Empfehlung an den Orchestrator:** Feld C ist nach Aktenlage das Feld mit dem
*besten strukturellen Fit zu Nicos Kriterien* und der *schlechtesten Datenlage*.
Ein zweiter Recherchedurchlauf mit frischem Suchbudget, ausschließlich auf
Feld C, hat den höchsten Erkenntniswert pro eingesetztem Aufruf. Siehe §7.

---

## 1. FELD A — KI-Telefonie / Voice-Agents / Inbound-Automatisierung für KMU

### 1.1 Wettbewerbstabelle International (Produkt-Layer, KMU-gerichtet)

| Anbieter | Land | Zielgruppe | Setup | MRR | Nutzungspreis | Kernfeatures | Schwäche | Quelle |
|---|---|---|---|---|---|---|---|---|
| **Goodcall** | US | Lokale Dienstleister, Handwerk, Salons | keine genannt | 79 / 129 / 249 USD **pro Agent** [F] | Minuten unlimitiert; 0,50 USD je Unique Caller über Kontingent [F] | Voice-Agent, ein Agent = eine Rufnummer, Logic Flows, 14 Tage Trial | Preis ist *pro Agent/Standort*, skaliert schlecht bei Mehr-Standort; Abrechnung über „Unique Caller" ist für Kunden schwer prognostizierbar | cloudtalk.io/blog/goodcall-pricing, vida.io/blog/goodcall-pricing |
| **Slang.ai** | US | Restaurants (nur) | k. A. | 399 USD (Core) / 599 USD (Premium) **je Standort** [F] | unlimitiert inkl. [F] | Reservierungen, Gäste-FAQ, 24/7, zweisprachig (Premium) | Sehr teuer je Standort, **kein Free Trial**, extrem enge Vertikale | synthflow.ai/blog/slang-ai-pricing, loman.ai/blog/slang-ai-reviews-pricing-alternatives |
| **Rosie** | US | Service-Businesses, Contractors | **keine Setup-Gebühr** [F] | 49 / 149 / 299 USD [F] | 250 / 1.000 / 2.000 Min inkl.; Overage ~0,25 USD/Min (nicht offiziell publiziert) [A] | Spam-Filter, SMS-Buchungslink, In-Call-Terminbuchung (ab Scale), Warm Transfer, Dokumententraining (Growth) | Overage-Regel nicht transparent publiziert; Feature-Gating zwingt kleine Betriebe schnell in den 149er | oncrew.ai/blog/rosie-ai-pricing-2026, heyrosie.com |
| **Numa** | US | Autohäuser / Service-Center | k. A. | Quote-only; 149 USD/User (Capterra-Indexwert) [F]; realistisch 200–400 USD je Standort [A] | teils **pay-per-booked-appointment** [F] | RO-Management, Serviceterminierung, Statusupdates, SMS-lastig | Keine öffentliche Preisliste; SMS-zentriert statt voice-first | oncrew.ai/blog/numa-pricing-2026, serviceagent.ai/blogs/numa-pricing |
| **Smith.ai** | US | Kanzleien, Agenturen, KMU | k. A. | Human: ab 292,50 USD / 30 Calls; 765 USD / 90; 1.950 USD / 300 [F] · AI: ab 95 USD [F] | Overage 9,75–10,50 USD **je Anruf** [F]; Add-ons: Recording 0,25 / Booking 1,50 / CRM-Sync 0,50 USD je Call [F] | Human + AI Hybrid, Terminbuchung, CRM-Sync, Intake | Add-on-Stapelung treibt Effektivpreis; Analysen empfehlen 20–30 % Budgetpuffer über Listenpreis [F] | fast.io/resources/smith-ai-review-2026, cloudtalk.io/smith-ai-pricing |
| **Ruby** | US | Kanzleien, Ärzte, KMU | k. A. | 245–250 / 385–395 / 705–720 / 1.725 USD [F] | 50 / 100 / 200 / 500 Minuten → **3,53–4,90 USD je Minute** [F] | Rein menschlich, 24/7, bilingual, 30-Sek-Taktung | Extrem hoher Minutenpreis; strukturell nicht gegen AI verteidigbar | ruby.com/plans-and-pricing, vida.io/blog/ruby-receptionists-pricing |
| **AnswerConnect** | US | KMU allgemein | 75 USD (bei Direktabschluss meist erlassen) [F] | 179 USD / 100 Min bis 399 USD / 300 Min [F]; andere Quelle 325–575 USD [F] | Overage 1,75–2,25 USD/Min [F] | **Explizit human-only, „no AI, no bots"** | Positioniert sich gegen AI — das ist eine Wette gegen den Preisverfall | vida.io/blog/answerconnect-pricing, serviceagent.ai/blogs/answerconnect-pricing |
| **PolyAI** | UK | Enterprise (Banken, Telcos, Hotels) | k. A. | **Kein öffentlicher Preis**; Verträge ab ~150.000 USD/Jahr [F, Drittschätzung] | pro Minute, individuell quotiert [F] | Enterprise-Voice, Multi-Language, tiefe Integrationen | Nicht KMU-fähig; Sales-Zyklus lang | cloudtalk.io/poly-ai-pricing, nurix.ai/blogs/polyai-pricing-features-guide |
| **Air.ai** | US | KMU/BPO — **tot** | 25.000–100.000 USD Lizenz vorab [F] | — | — | — | **FTC-Klage 25.08.2025, Vergleich 18 Mio. USD März 2026, Vermarktungsverbot; Produkt seit Ende 2024 offline, Domain weiterverkauft** [F] | ftc-Verfahren via thoughtly.com/blog/air-ai-review, trillet.ai/blogs/air-ai-ftc-lawsuit-status-2026 |

### 1.2 Wettbewerbstabelle Infrastruktur-Layer (die „Motoren")

| Anbieter | Land | Modell | Listenpreis | Realistische Vollkosten | Funding | Quelle |
|---|---|---|---|---|---|---|
| **Vapi** | US | Dev-Plattform | 0,05 USD/Min beworben [F] | **0,10–0,30 USD/Min all-in** [F] | 2,1 Mio Seed (11/2023), 20 Mio Series A (12/2024), 50 Mio Series B (Peak XV) [F] | medium.com/@automation.labs, sovereignmagazine.com |
| **Retell AI** | US | Dev-Plattform | 0,07 USD/Min beworben [F] | **0,11–0,31 USD/Min**, kein Monatsminimum [F] | nur 5,1 Mio USD offengelegt, behauptet 50 Mio USD ARR [F] | cekura.ai/blogs/retell-ai-pricing-per-minute |
| **Bland AI** | US | Plattform mit Stufen | Start 0,14 / Build 299 USD→0,12 / Scale 499 USD→0,11 USD je Min [F] | wie gelistet | 40 Mio Series B (01/2025), gesamt 65 Mio [F] | builts.ai, tested.media |
| **Synthflow** | DE/US | No-Code-Plattform, White-Label | k. A. aus Suche | — | 20 Mio Series A (Accel) [F] | retellai.com/blog/vapi-vs-synthflow |
| **Parloa** | **DE** | Enterprise Agentic CX | k. A. | — | **350 Mio USD Series D (01/2026), Bewertung 3 Mrd. USD; gesamt > 560 Mio USD in < 4 Jahren** [F] | techcrunch.com/2026/01/15, vestbee.com |
| **Cognigy** | **DE** | Enterprise CAI | k. A. | — | **Für 955 Mio USD an NiCE verkauft; angekündigt 28.07.2025, abgeschlossen 08.09.2025; zuvor > 170 Mio USD VC** [F] | handelsblatt.com, cognigy.com/de/news |

> **Kritischer Befund zum Infrastruktur-Layer:** Der beworbene Minutenpreis
> (0,05–0,07 USD) und der reale Vollkostenpreis (0,10–0,31 USD) liegen um
> **Faktor 2–5** auseinander, weil LLM-Token, Premium-Stimmen und Telefonie
> nicht enthalten sind [F]. Jede Kalkulation, die mit dem Listenpreis rechnet,
> ist falsch.

### 1.3 Wettbewerbstabelle DACH — KI-Telefonassistenten

| Anbieter | Land | Zielgruppe | Setup | MRR | Nutzungspreis | Kernfeatures | Schwäche | Quelle |
|---|---|---|---|---|---|---|---|---|
| **fonio.ai** | **AT** | KMU, Handwerk, Kanzleien | k. A. | Solo 99 € / Team 299 € / Business [F] | Solo: 1 Nr. + 1.000 Min inkl.; Team: 3 Nr. + 3.000 Min; danach **0,12–0,15 €/Min** [F, Stand 01/2026] | DSGVO, EU-Server, Terminbuchung; **Zusatzfeatures 5–79 €/Feature/Monat** (zus. Rufnummer 7 €, Zusatzkontakte 20 €, WhatsApp 79 €) [F] | Feature-Entbündelung treibt Effektivpreis; Kernprodukt ist austauschbar | fonio.ai/en/pricing, fonio.ai/de/news-cool-stuff |
| **Vokaro** | DE | KMU, Gesundheitswesen, Handwerk | Sommer-Deal 2026: **Einrichtung kostenlos** [F] | 99 € regulär, 69 € Aktion bis 31.07.2026 [F] | k. A. | Branchentemplates, Folgetermine, Kassenleistungen, dt. Support; Setup ca. 1 Woche [F] | Rabattgetriebene Positionierung = Preisdruck; sehr kleine Firma | vokaro.net/kosten, vokaro.net/blog |
| **SpeakKI** | DE | KMU | **keine Einrichtungsgebühr, monatlich kündbar** [F] | k. A. aus Suche | 50 Freiminuten zum Einstieg [F] | dt. Anbieter | Preise nicht in den Suchergebnissen auffindbar | speakki.de/blog/ki-telefonassistent-kosten |
| **Livestep** | DE | Mittelstand, Handwerk, Kanzleien | k. A. | k. A. | k. A. | Datenschutz-/DE-Support-Positionierung | Kein öffentlicher Preis auffindbar | vokaro.net/blog |
| **Aaron.ai** | **DE** | Arztpraxen | k. A. | ab **119 €/Monat je Behandler** [F] | k. A. | Anrufannahme, Transkription, Kategorisierung | **Seit 2024 Teil von Doctolib; separate Buchung außerhalb Doctolib nicht mehr möglich** [F] — siehe §5, Chance 2 | zeeg.me/de/blog/content/aaron-telefonassistent, ordicall.ai |
| **Placetel AI** (Cisco/Telekom-Umfeld) | DE | Bestandskunden der Cloud-TK-Anlage | k. A. | Minutenpakete, **monatlich kündbar**, + **9 €/Monat je KI-Rufnummer** [F] | Minutenpakete | Direkt in die Telefonanlage integriert, Kalender/CRM/Callcenter | Nur für Placetel-Kunden — aber genau das ist die Waffe | premium-electronics.eu, placetel.de/ratgeber/ki-telefonassistent |
| **sipgate AI Agents** | DE | sipgate-Bestandskunden | k. A. | Pakete mit Freiminuten, flexibel anpassbar [F] | Freiminutenpakete | In die Cloud-TK-Anlage integriert, 24/7 | Nur für sipgate-Kunden | help.sipgate.de |
| **Telekom „Magenta AI Call Assistant"** | DE | Mobilfunk-Massenmarkt | — | **Preis offen**, evtl. kostenlos [F] | — | **Wird ins Netz integriert**, Aktivierung per „Hey Magenta"; MWC-Ankündigung | Noch nicht ausgerollt — aber die größte strukturelle Bedrohung des Feldes | handelsblatt.com/technik/it-internet/…/100204610.html |
| **Label Software** | DE | Handwerksbetriebe | k. A. | k. A. | k. A. | **Handwerker-ERP mit eigenem integriertem KI-Telefonassistenten** [F] | — (Bedeutung: siehe §5, Chance 1) | label-software.de/ki-in-handwerkersoftware/ki-telefonassistent |
| **VIER** | DE | Contactcenter / Enterprise | k. A. | Kein öffentlicher Preis [F] | k. A. | Cognitive Voice Gateway + „VIER Smart Dialog" (LLM-angebunden) | Enterprise-Vertrieb, nicht KMU | squt.de, digital-affin.de |

### 1.4 Wettbewerbstabelle DACH — menschliche Telefonservices (die Bestandsindustrie)

| Anbieter | Setup | MRR | Nutzungspreis | Besonderheit | Quelle |
|---|---|---|---|---|---|
| **ebuero AG** | k. A. | 59,90 € (Starter) / 99,90 € (Standard) / 179,90 € (Professional) [F] | **1,04–1,39 €/Min** je nach Paket [F]; +19,90 €/Monat für 24/7-Erweiterung [F] | Marktführer, 365 Tage, Sekretärinnen im Kundennamen | ebuero.de/preisverzeichnis/telefonsekretariat, telefon.services/anbieter/ebuero |
| **starbuero.de** | keine Grundgebühr [F] | 0 € | **0,49 €/Bearbeitungsminute je angenommenem Anruf** [F] | Preisbrecher | starbuero.de/preise, starbuero.de/handwerk |
| **Cloudsecretary** | — | 0 € | **ab 0,99 € je angenommenem Anruf**, keine Mindestlaufzeit [F] | Handwerk-Fokus | cloudsecretary.de |
| **phonea** | — | keine Grundgebühr [F] | **1,70 € je Anruf** (Handwerker-Tarif) [F] | Kanzlei/Notar/Handwerk | phonea.de/telefonservice-tarife |
| **Büroservice Strate** | — | — | **0,65 €/Min + 0,99 €/Anruf** (10 Anrufe inkl.) [F] | Handwerk | bs-strate.de |
| Marktbreite | — | — | — | **Über 40 deutsche Telefonservice-Anbieter im Vergleichstest gelistet** [F] | telefon.services/anbieter |

### 1.5 Preisspannen Feld A (verdichtet)

| Segment | Setup | Monatlich | Nutzung |
|---|---|---|---|
| **Infrastruktur / Dev-Plattform** (US) | 0 | 0–499 USD | 0,10–0,31 USD/Min Vollkosten [F] |
| **KI-Telefonassistent DACH, KMU** | 0 bis „auf Anfrage"; mehrere Anbieter werben explizit mit **0 € Setup** [F] | **29–299 €**, Kernband **69–199 €** [F]; Ausreißer bis 499 € bei hohem Volumen [F] | **0,10–0,28 €/Min**, fonio konkret 0,12–0,15 € [F] |
| **KI-Telefonassistent US, KMU** | meist 0 | **49–599 USD** [F] | oft „unlimited" oder 0,25 USD/Min |
| **Menschlicher Telefonservice DACH** | 0 | **0–179,90 €** Grundgebühr [F] | **0,49–1,70 €** je Minute bzw. je Anruf [F] |
| **Menschlicher Telefonservice US** | 0–75 USD [F] | 179–1.950 USD [F] | 1,75–2,25 USD/Min bzw. 9,75–10,50 USD/Anruf [F] |
| **Enterprise Voice AI** | — | — | ab ~150.000 USD/Jahr Vertragswert [F] |

**Die entscheidende Arbitrage — und warum sie sich gerade schließt:**

- Menschlich DACH: **1,04–1,39 €/Min** (ebuero) [F]
- KI-Vollkosten Plattform: ca. **0,10–0,12 €/Min** (0,11–0,13 USD bei 1 USD ≈ 0,92 € [A]) [S]
- → **Faktor 9–13** Kostenvorteil [S]. Gegen Ruby (3,54–4,51 €/Min umgerechnet [S]) sogar **Faktor 30–45** [S].

Aber: fonio verkauft Solo mit 1.000 Freiminuten für 99 € = **0,099 €/Min bei
Vollausschöpfung** [S]. Das liegt **unter** den eigenen Plattformvollkosten von
0,10–0,12 €/Min [S]. Das Geschäftsmodell trägt nur, solange die Kunden ihr
Kontingent **nicht** ausschöpfen. Die Marge kommt aus Unterauslastung, nicht aus
Wertschöpfung. Das ist ein instabiles Preisgleichgewicht und ein Vorbote weiterer
Konsolidierung.

### 1.6 Quellenkritik Feld A (wichtig)

Auffällig viele der auffindbaren „Anbietervergleiche" und „Pricing Guides"
werden von **direkten Wettbewerbern** betrieben: `synthflow.ai/blog/slang-ai-pricing`,
`retellai.com/blog/vapi-vs-synthflow`, `cloudtalk.io/blog/goodcall-pricing`,
`vokaro.net/kosten/...`, `fonio.ai/de/news-cool-stuff/ki-telefonassistent-kosten-10-anbieter`.
Diese Seiten sind **SEO-Waffen**, keine neutralen Tests. Zwei Folgerungen:

1. Alle hier mit [F] gekennzeichneten Fremdpreise sind vor einer Entscheidung
   **an der Primärquelle (Preisseite des Anbieters) zu verifizieren**.
2. Der Umstand, dass praktisch jeder Anbieter dieses Content-Spiel spielt, ist
   selbst ein Marktsignal: **Die Kundenakquise läuft über SEO-Preisvergleiche,
   der Markt ist bereits in der Preiskampfphase.** Das ist typisch für einen
   Markt kurz vor der Kommoditisierung, nicht für einen frühen Markt.

---

## 2. FELD B — Vertikale Prozess-/Betriebssoftware für deutsches Handwerk

### 2.1 Wettbewerbstabelle (soweit recherchiert)

| Anbieter | Land | Zielgruppe | Setup | MRR | Nutzungspreis | Kernfeatures | Schwäche | Quelle |
|---|---|---|---|---|---|---|---|---|
| **ToolTime** | DE | Handwerk, Solo bis 10+ MA | k. A. | **SOLO 79 € · TEAM 149 € · MAX ab 220 €** [F] | Weitere MA: **22 €** (Jahresvorauszahlung) / **34 €** (monatlich); Zusatzlizenz MAX 29,90 € [F] | Voller Funktionsumfang in allen Komplettlizenzen, „keine versteckten Kosten" [F] | Mindestlaufzeit 1 Monat *oder* 12 Monate [F] → schwache Bindung | trusted.de/tooltime-kosten, omr.com/en/reviews/product/tooltime/pricing |
| **plancraft** | DE | Handwerk, Bau | k. A. | **Business 74,90 € · Pro 139,90 € · Premium 249,90 €** (monatlich) [F]; **ab 47,92 €/Nutzer/Monat bei 2-Jahres-Bindung** [F] | Zusatz-Büro-User 39,92–59,90 €; mobile Lizenz 15,92–24,90 € [F] | Angebot/Rechnung/Projekt, mobil, KI-Roadmap | Preis skaliert hart pro Kopf; 2-Jahres-Bindung nötig für Listenpreis | trusted.de/plancraft-kosten, flinki.ai/tools/plancraft |
| **Craftnote** | DE | Handwerk, Baustellendoku | k. A. | **Baustelle 14,90 € · Fahrzeug 24,90 € · Büro 29,90 € · Büro Plus 49,90 €** je Nutzer/Monat, netto, jährliche Abrechnung [F] | — | Baudoku, Projektkommunikation, Zeiterfassung; positioniert als „WhatsApp-Ersatz fürs Handwerk" | **Kein dauerhaft kostenloser Plan mehr** [F] → Monetarisierungsdruck; sehr niedriger ACV | craftnote.de/preise, ki-syndikat.de/tools/craftnote |
| **Label Software** | DE | Handwerk | k. A. | nicht recherchiert | — | Klassisches Handwerker-ERP, **hat bereits einen eigenen KI-Telefonassistenten integriert** [F] | — | label-software.de/ki-in-handwerkersoftware/ki-telefonassistent |
| **Meisterwerk, Meisterox, u. a.** | DE | Handwerk | — | nicht recherchiert | — | Weitere aktive Wettbewerber im selben Preisband; betreiben eigene Vergleichs-Blogs | Marktenge | blog.meisterwerk.app, meisterox.app/blog |
| **Streit V.1, Moser, Sander & Doll, 1Tool** | DE/AT | Handwerk, Bau (Legacy-ERP) | **nicht recherchiert** | **nicht recherchiert** | — | — | — | — |
| **ServiceTitan (US), Jobber (CA), Housecall Pro (US), simPRO (AU)** | — | Field Service | **nicht recherchiert** | **nicht recherchiert** | — | — | — | — |

> Die vier fehlenden internationalen Anbieter und die deutschen Legacy-ERPs
> konnten nicht mehr abgefragt werden (Suchbudget). Sie sind im
> Nachrecherche-Auftrag §7 priorisiert.

### 2.2 Preisspanne Feld B

| Größe | Preis je Nutzer/Monat |
|---|---|
| Einstieg (mobile/Baustellen-Lizenz) | **14,90–24,90 €** [F] |
| Standard Büro-Arbeitsplatz | **29,90–79,00 €** [F] |
| Vollpaket kleines Team | **74,90–149,00 € je Betrieb** [F] |
| Vollpaket 10+ Mitarbeiter | **ab 220–249,90 € je Betrieb**, + 22–34 € je weiterem Kopf [F] |

**Gesamtband Feld B: ca. 15–250 €/Monat je Betrieb bzw. Nutzer** [F].

### 2.3 Strukturbefund Feld B

**Der Markt ist besetzt, VC-finanziert und im Konsolidierungsmodus.**

- plancraft: **38 Mio. € Series B (08/2025)**, Lead: Headline, mit Creandum,
  HTGF, xdeck; **Gesamtfinanzierung > 50 Mio. €**; **> 20.000 Kunden in
  11 Ländern**; Mittel gehen explizit in **KI-Features** [F].
- Daneben ToolTime, Craftnote, Meisterwerk, Meisterox sowie die etablierten
  Legacy-ERPs (Streit, Label, Moser, Sander & Doll), die ihre
  Bestandskundenbasis verteidigen — Label Software liefert bereits einen
  eigenen KI-Telefonassistenten mit [F].
- Es existiert bereits eine **Beratungs-/Implementierungsschicht**
  (`handwerkersoftware.pro` positioniert sich als Vermittler mehrerer Produkte) [F]
  — ein Zeichen für Marktreife, nicht für eine Lücke.

**Die Arithmetik, die Feld B für Nico erledigt:**

| Ziel | Nötige Kundenzahl bei 99 €/Monat | bei 199 €/Monat | bei 2.500 €/Monat |
|---|---|---|---|
| 10.000 €/Monat | 101 [S] | 51 [S] | 4 [S] |
| 100.000 €/Monat (Zwischenziel) | **1.010** [S] | **503** [S] | **40** [S] |
| 190.000 €/Monat (echtes Ziel lt. `01`, §2) | **1.919** [S] | **955** [S] | **76** [S] |

Kriterium 5 des Nordsterns lautet *„wenige hochwertige Kunden statt hunderte
Kleinkunden"*. Ein Produkt im 99–199-€-Band verlangt **500 bis 1.900 zahlende
Handwerksbetriebe**. Das ist keine Firma mit einem Vertriebler — das ist eine
Inside-Sales-Organisation mit 10–20 Köpfen, Churn-Management und
Performance-Marketing-Budget. Es ist exakt das Modell, für das plancraft
50 Mio. € eingesammelt hat. Nach Annahme A10 (`02_research_methodik.md`,
kein VC gewünscht) ist dieser Weg **nicht finanzierbar**.

**Verdict Feld B als eigenständiges Modell: ausgeschlossen.**
Nicht weil der Markt schlecht ist, sondern weil der Preispunkt und die
Kapitalintensität mit Nicos Kriterien 5, 20 und Annahme A10 kollidieren.

---

## 3. FELD C — Monitoring/Wartung-as-a-Service mit Hardware

### 3.1 Datenlage: leer

**Ich habe zu Feld C keine einzige verifizierte Preis- oder Anbieterangabe.**
Das Suchbudget war vor Beginn dieses Feldes erschöpft. Nach Regel 2 der
Methodik nenne ich hier **keine Preise** — weder [F] noch [A] mit erfundener
Bandbreite. Eine Tabelle mit ausgedachten Zahlen wäre schlimmer als eine leere
Tabelle, weil sie in die Bewertungsmatrix einfließen würde.

### 3.2 Was sich trotzdem sagen lässt: der Strukturbefund

Feld C unterscheidet sich in **vier** ökonomisch entscheidenden Punkten von
Feld A und B — und zwar in Nicos Richtung:

| Dimension | Feld A (Voice) | Feld B (Handwerk-SaaS) | Feld C (Monitoring/Wartung) |
|---|---|---|---|
| Preispunkt je Kunde | 29–299 €/Monat [F] | 15–250 €/Monat [F] | vermutlich deutlich höher, weil Hardware + Haftung + Nachweis gebündelt sind [A] |
| Nötige Kundenzahl für 100k € MRR | 335–3.400 [S] | 400–1.900 [S] | wenn 2.000–3.000 €/Monat je Kunde erreichbar: 33–50 [S] |
| Kaufgrund | Komfort / entgangener Umsatz | Effizienz | **Pflicht** (Gesetz, Norm, Versicherung) [A] |
| Substituierbarkeit | hoch — Telcos bundeln es weg | hoch | niedrig, sobald Sensorik verbaut und Historie aufgebaut ist [A] |

Leitfrage 2 der Methodik lautet: *„Wo entsteht wiederkehrender Umsatz aus einer
Pflicht statt aus Überzeugung?"* Feld C ist strukturell **das einzige der drei
Felder, das diese Frage positiv beantwortet.** Feld A und B verkaufen beide
Überzeugung („spart Zeit", „verpasst keine Anrufe"). Genau deshalb liegen sie
im 29–299-€-Band und genau deshalb fallen ihre Preise.

### 3.3 Zwingende Warnung: K.-o.-Kriterium 3

Mehrere der im Auftrag genannten Feld-C-Themen berühren
**Ausschlusskriterium 3** aus `01_nordstern_und_anforderungen.md`
(„stark reguliert … TÜV-Zulassung o. ä. **als Kern**"):

- Aufzugsprüfung, Brandschutzabnahme und Trinkwasseruntersuchung sind in
  Deutschland an **akkreditierte Stellen** gebunden (ZÜS, akkreditierte
  Trinkwasserlabore, Fachfirmen nach Norm).
- **Die Trennlinie ist scharf und entscheidungsrelevant:** Selbst die
  prüfpflichtige Leistung erbringen = **K.-o.** Die prüfpflichtige Leistung
  *messtechnisch vorbereiten, überwachen, dokumentieren und den Nachweis
  liefern* = **kein K.-o.**, sondern genau die Nische, in der Software +
  Sensorik + Managed Service verkäuflich sind, ohne die Akkreditierung zu
  brauchen.
- Diese Unterscheidung muss vor jeder Feld-C-Empfehlung anwaltlich bzw. anhand
  der einschlägigen Verordnungen (TrinkwV, BetrSichV, EnEfG, DIN 14675) geprüft
  werden. Sie ist bisher **nicht** geprüft.

### 3.4 Preisspanne Feld C

**Nicht ermittelbar.** Siehe §7 Nachrecherche-Auftrag, Priorität 1.

---

## 4. FEATURE-VERGLEICHSMATRIX

Legende: ● vollständig · ◐ teilweise · ○ nein · ? nicht recherchiert

| Feature | Goodcall | Rosie | Slang | Smith.ai | ebuero (human) | fonio | Vokaro | Placetel/sipgate | plancraft | ToolTime | Label SW |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Anruf annehmen 24/7 | ● | ● | ● | ● | ● (+19,90 €) | ● | ● | ● | ○ | ○ | ◐ |
| Deutsch muttersprachlich | ○ | ○ | ○ | ○ | ● | ● | ● | ● | – | – | ● |
| DSGVO / EU-Hosting | ? | ? | ? | ? | ● | ● | ● | ● | ● | ● | ● |
| Termin **in** den Kalender buchen | ● | ◐ (ab Scale) | ● | ◐ (1,50 $/Call) | ◐ | ● | ● | ● | ○ | ○ | ◐ |
| Warm Transfer an Menschen | ? | ● (ab Scale) | ? | ● | ● | ? | ? | ? | ○ | ○ | ? |
| **Menschlicher Fallback im selben Vertrag** | ○ | ○ | ○ | **●** | ● | ○ | ○ | ○ | ○ | ○ | ○ |
| Angebot / Rechnung erzeugen | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ● | ● | ● |
| Auftrags-/Projektsteuerung | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ● | ● | ● |
| Zeiterfassung Monteure | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ● | ● | ● |
| **Disposition / Einsatzplanung aus dem Anruf heraus** | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ◐ | ◐ | ◐ |
| **Wartungsvertrags-/Prüffristenverwaltung** | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | **○** | **○** | ? |
| **Anlagenstammdaten + Historie je Objekt** | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ◐ | ◐ | ? |
| **Sensorik / Fernüberwachung** | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ |
| **Compliance-Nachweis / Auditakte** | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ |
| **Ergebnisgarantie (pay per outcome)** | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ |
| **Managed Service (Anbieter bedient das System)** | ○ | ◐ (White-Glove ab 299 $) | ○ | ● | ● | ○ | ◐ (Setup) | ○ | ○ | ○ | ○ |

### 4.1 Die Kombination, die NIEMAND vollständig anbietet

Aus der Matrix lassen sich drei nirgends geschlossene Ketten ablesen:

**Lücke I — „Vom Anruf bis zum abgerechneten Auftrag" in einem Vertrag.**
Die Voice-Anbieter enden beim Kalendereintrag. Die ERP-Anbieter beginnen beim
Auftrag. Zwischen „Kunde ruft an" und „Auftrag ist disponiert, ausgeführt,
abgerechnet" liegt eine Bruchkante, die **kein einziger** der untersuchten
Anbieter überbrückt. Label Software ist der einzige, der von der ERP-Seite her
in Richtung Telefonie ausgreift [F] — und genau das zeigt, wohin die
Konsolidierung läuft.

**Lücke II — „Wartungsvertrag" statt „Projekt" als Datenmodell.**
Die gesamte deutsche Handwerkersoftware ist **projekt- und angebotszentriert**:
Angebot → Auftrag → Baustellendoku → Zeiterfassung → Rechnung [F]. Kein
untersuchter Anbieter hat **Anlage, Wartungszyklus, Prüffrist und
Nachweispflicht** als First-Class-Objekte. Für Betriebe, deren Umsatz aus
*wiederkehrenden Wartungsverträgen* stammt (Kälte/Klima, Aufzug, Brandschutz,
Tor/Antrieb, Trinkwasserhygiene, Ladeinfrastruktur), ist die vorhandene Software
strukturell falsch gebaut.

**Lücke III — Sensorik + Nachweis + Disposition + Abrechnung als ein Abo.**
Keine Zelle in der Matrix ist bei „Sensorik" oder „Compliance-Nachweis" gefüllt.
Das ist teilweise ein Artefakt der Auswahl (Feld-C-Anbieter wurden nicht
recherchiert) — aber es ist gesichert, dass **weder die Voice-Anbieter noch die
Handwerks-ERPs** in diese Richtung gehen.

---

## 5. „WARUM BIETET DAS NIEMAND VOLLSTÄNDIG AN?" — 10 Chancen mit Friedhofsprüfung

### Chance 1 — Standalone KI-Telefonassistent für deutsche KMU
**Urteil: FRIEDHOF (im Entstehen). Belastbar belegt.**

Vier unabhängige Signale, alle [F]:
1. **Telcos bundeln es weg.** Placetel verkauft die KI-Rufnummer für **9 €/Monat**
   an Bestandskunden [F]. sipgate liefert AI Agents als Paket in der TK-Anlage [F].
   Die Telekom hat den „Magenta AI Call Assistant" **direkt im Netz** angekündigt,
   Preis offen, möglicherweise inklusive [F]. Wenn der Anrufbeantworter mit
   Terminbuchung Teil des Telefonanschlusses wird, ist das eigenständige
   99-€-Abo tot.
2. **Vertikale Plattformen absorbieren es.** Aaron.ai — der prominenteste
   deutsche vertikale Telefonassistent — ist seit 2024 in Doctolib aufgegangen
   und **separat nicht mehr buchbar** [F]. Label Software liefert den KI-Assistenten
   im eigenen Handwerker-ERP mit [F].
3. **Der Preis ist bereits gefallen.** Einstieg bei 29 €/Monat [F], Vokaro
   rabattiert von 99 auf 69 € [F], mehrere Anbieter werben mit 0 € Setup und
   monatlicher Kündbarkeit [F]. Das ist das Preisverhalten eines Marktes in der
   Endphase der Differenzierung.
4. **Die Marge ist rechnerisch schon weg.** fonio Solo = 0,099 €/Min bei
   Vollausschöpfung gegen 0,10–0,12 €/Min Plattformvollkosten [S].
5. **Der Warnschuss:** Air.ai hat genau dieses Versprechen mit 25.000–100.000 USD
   Vorabgebühren verkauft — FTC-Klage, 18 Mio. USD Vergleich, Vermarktungsverbot,
   Produkt tot [F]. Das hat den Vertrauensvorschuss der Kategorie beschädigt.

*Warum es trotzdem so viele versuchen:* Weil die Bruttomarge auf dem Papier
schön aussieht und der Bau in 4 Wochen möglich ist. Genau das ist das Problem —
**null Eintrittsbarriere**.

---

### Chance 2 — Voice-Layer als White-Label-Motor für die 40+ bestehenden deutschen Telefonservice-Anbieter
**Urteil: ECHTE LÜCKE, aber mit hartem Zeitfenster (geschätzt 18–30 Monate) [A].**

Über 40 deutsche Telefonservice-Anbieter sind im Markt [F]. Sie rechnen heute
mit **0,49–1,70 € je Minute bzw. Anruf** ab [F] und haben ein rein menschliches
Kostenmodell. Der KI-Vollkostenpreis liegt bei 0,10–0,12 €/Min [S] —
**Faktor 9–13** [S]. Diese Anbieter haben: Kunden, Marke, Abrechnung,
Nachtdienste, Branchenkenntnis. Was ihnen fehlt: eine DSGVO-konforme
Voice-Engine mit deutscher Sprachqualität, die sie unter eigenem Namen
betreiben können.

*Warum bietet das niemand vollständig an?* Weil die US-Plattformen (Vapi,
Retell, Bland) Developer-Produkte ohne deutschen Rechtsrahmen und ohne
Branchen-Playbooks sind, und die deutschen Anbieter (fonio, Vokaro) selbst
Endkundengeschäft machen und damit **Wettbewerber** ihrer potenziellen
White-Label-Kunden sind. Synthflow adressiert White-Label, ist aber
US-/Developer-orientiert [F].

*Fit zu Nico:* Sehr gut in Kriterium 5 (wenige hochwertige B2B2B-Kunden statt
tausender KMU). 40 mögliche Kunden × z. B. 2.500 €/Monat = 100.000 € [S] bei
realistisch 30–50 % Marktdurchdringung → 30.000–50.000 €/Monat [S], also
Zwischenziel, nicht Endziel. **Reicht als Maschine A allein nicht.**

*Friedhofsrisiko:* Die Telefonservice-Anbieter könnten die Umstellung
verweigern, weil KI ihr eigenes Geschäftsmodell kannibalisiert (AnswerConnect
wirbt in den USA explizit mit **„no AI, no bots"** [F] — das ist genau diese
Verweigerungshaltung, in Marketing gegossen). Das ist das Hauptrisiko dieser
Chance und muss vor jedem Bau in 5 Erstgesprächen validiert werden.

---

### Chance 3 — „Vom Anruf zum abgerechneten Auftrag": Voice + Disposition + Abrechnung in einem Vertrag
**Urteil: HALBE LÜCKE — echt heute, in 24–36 Monaten geschlossen. Nicht als Kern empfehlenswert.**

Die Bruchkante zwischen Voice und ERP ist real und in der Matrix (§4)
nachweisbar. Aber: plancraft hat **38 Mio. € explizit für KI-Features**
eingesammelt und bedient 20.000 Kunden in 11 Ländern [F]; Label Software
liefert den Telefonassistenten bereits mit [F]. Wer diese Lücke schließt, hat
den Kundenzugang schon — Nico hätte ihn nicht. **Ein Angriff gegen einen
50-Mio.-€-finanzierten Gegner auf dessen Heimspielfeld, ohne VC (Annahme A10).**

---

### Chance 4 — Betriebssystem für **Wartungsvertrags-Betriebe** (nicht für Projekt-Handwerk)
**Urteil: ECHTE LÜCKE. Stärkste der Feld-B-Ableitungen.**

Belegt: Die gesamte recherchierte deutsche Handwerkersoftware ist
angebots-/projekt-/baustellenzentriert — ToolTime, plancraft, Craftnote
beschreiben sich durchgängig über Angebot, Rechnung, Projekt, Baudoku,
Zeiterfassung [F]. **Kein untersuchter Anbieter** führt Wartungsvertrag,
Prüffrist, Anlagenstammdaten und Nachweisakte als Kernobjekte (§4, Lücke II).

*Warum bietet das niemand an?* Drei plausible Gründe [A]:
1. Der TAM je Einzelgewerk (Kältetechnik, Aufzugsservice, Brandschutz,
   Torantriebe, Trinkwasserhygiene) ist zu klein für ein VC-Modell — genau
   deshalb ist er groß genug für ein bootstrapped Modell.
2. Es erfordert Normen-/Regelwerkswissen, das Software-Gründer nicht haben.
3. Die Legacy-ERPs (Streit, Moser, Sander & Doll) *könnten* es bedienen, sind
   aber technologisch alt — **nicht recherchiert, Prüfauftrag §7.**

*Wichtige Fit-Nuance:* Nicos Anti-Kriterium lautet „Fristen und Einzelfälle
**verwalten**". Hier verwaltet **die Software** die Fristen und der Kunde
profitiert davon. Nico baut das System, er bedient es nicht. Das ist zulässig —
aber die Grenze ist dünn und Agent 09 muss sie explizit prüfen.

*Preispunkt:* Wenn der Kunde ein haftungsrelevantes Nachweisproblem löst statt
Zeit zu sparen, sind Preise deutlich über dem 15–250-€-Band plausibel [A] —
das ist die einzige Konstruktion, die die Kundenzahl-Arithmetik aus §2.3 rettet.
**Muss preislich validiert werden, bevor darauf gebaut wird.**

---

### Chance 5 — Compliance-Monitoring-as-a-Service (Sensorik + Nachweis + Abo)
**Urteil: UNGEPRÜFT — kann nicht redlich beurteilt werden. Priorität 1 der Nachrecherche.**

Strukturell der beste Fit zu Nicos Kriterien (Pflichtkauf, Hardware, technisch,
wenige hochwertige Kunden, hohe Wechselkosten). Aber: Ich habe **keinen einzigen
verifizierten Anbieter und keinen einzigen Preis**. Eine Chance, die ich nicht
belegen kann, ist nach Regel 1 der Methodik keine Erkenntnis, sondern eine Idee.
Sie bleibt hier als **Hypothese mit Prüfauftrag** stehen, nicht als Befund.

*Bekanntes Friedhofsrisiko, das geprüft werden muss:* Das generische
„Predictive Maintenance mit Sensoren"-Versprechen hat zwischen 2016 und 2022
eine große Zahl von Industrie-4.0-Startups verbrannt. Ob das an der Technik,
an der Integration oder am fehlenden Pflichtkauf lag, ist die entscheidende
Frage. Wenn der Kaufgrund „Optimierung" war → Friedhof. Wenn der Kaufgrund
„gesetzlicher Nachweis" ist → anderes Spiel. **Diese Frage ist unbeantwortet.**

---

### Chance 6 — Ergebnisbasierte Abrechnung („pay per booked job") statt Abo
**Urteil: ECHTE LÜCKE, in Teilen aber bereits von einem Wettbewerber besetzt.**

In der gesamten Matrix (§4) ist die Zeile „Ergebnisgarantie" leer — mit einer
Ausnahme: **Numa** hat für Autohäuser Pay-for-Performance je gebuchtem Termin
eingeführt [F]. Das beweist, dass das Modell technisch und vertrieblich
funktioniert, und dass es **im deutschen Markt bei keinem der recherchierten
Anbieter existiert** [F].

*Warum bietet es niemand an?* Weil es Attributionsstreit erzeugt (war der
Termin wirklich durch die KI?) und die Umsatzprognose zerstört — beides
Gift für ein VC-finanziertes SaaS mit ARR-Story. Für ein bootstrapped
Unternehmen ist genau das ein **Vorteil**: es senkt die Kaufhürde beim
misstrauischen deutschen Handwerksmeister drastisch.

*Konflikt mit dem Nordstern:* Erfolgsabhängige Vergütung ist per Definition
**kein planbarer MRR** (Kriterium 1). Nur als Einstiegsmechanik in einen
Abovertrag zulässig, nicht als Dauermodell.

---

### Chance 7 — DSGVO/EU-Souveränität als Produktkern statt als Fußnote
**Urteil: TEILWEISE FRIEDHOF. Als alleiniges Differenzierungsmerkmal wertlos.**

fonio, Vokaro, Livestep, SpeakKI und Placetel führen **alle** „DSGVO", „EU-Server",
„deutscher Support" als zentrales Verkaufsargument [F]. Wenn fünf von fünf
Anbietern dasselbe Argument führen, ist es kein Differenzierungsmerkmal mehr,
sondern eine Eintrittsvoraussetzung. Zusätzlich ist der stärkste denkbare
Souveränitäts-Anbieter die Telekom selbst — und die tritt an [F].

*Was daran doch echt ist:* Nicht „DSGVO" als Label, sondern die **konkrete
Auftragsverarbeitung mit Berufsgeheimnisträgern und haftungsrelevanten Daten**
(§203 StGB bei Ärzten/Kanzleien, Betreiberpflichten bei Anlagen). Das ist eine
Nische mit echter Barriere — aber eine juristische, keine technische.

---

### Chance 8 — Mehrsprachiger Inbound für Betriebe mit ausländischen Kunden/Monteuren
**Urteil: WAHRSCHEINLICH FRIEDHOF. Feature, kein Unternehmen.**

Zweisprachigkeit ist bei Ruby und AnswerConnect **in jedem Tarif enthalten** [F];
Slang.ai verkauft sie als Premium-Aufpreis [F]. Bei LLM-basierten Voice-Agents
ist Mehrsprachigkeit ein Konfigurationsparameter, keine Entwicklungsleistung.
Preisliche Differenzierung darüber hält nicht.

---

### Chance 9 — Hybrid „KI zuerst, Mensch als Eskalation" in einem Vertrag
**Urteil: ECHTE LÜCKE in DACH — in den USA bereits besetzt.**

In der Matrix (§4) hat nur **Smith.ai** menschlichen Fallback und AI im selben
Produkt [F] — und das ist ein US-Anbieter. **Kein einziger recherchierter
DACH-Anbieter** kombiniert beides: fonio, Vokaro, SpeakKI, Placetel, sipgate
sind rein KI; ebuero, phonea, starbuero, Cloudsecretary sind rein menschlich [F].

*Warum nicht?* Weil es zwei völlig verschiedene Betriebsmodelle sind:
Softwarefirma vs. Personaldienstleister mit Schichtplanung. Wer aus der
Software kommt, will keine 40 Telefonistinnen führen. Wer aus dem Callcenter
kommt, kann keine Voice-Engine bauen.

*Fit zu Nico:* Ambivalent. Es löst das Qualitätsproblem und rechtfertigt einen
höheren Preis — aber es bedeutet **Personalführung im Schichtbetrieb mit
Nachtdiensten**. Ausschlusskriterium 7 und 8 (`01`, §6) sind nur dann nicht
verletzt, wenn ein **bezahltes 24/7-Team** die Schicht trägt und Nico nie in der
Eskalation steht. Das ist zulässig, aber teuer und senkt die Bruttomarge unter
die 65-%-Zielmarke [A]. Vermutlich besser über Zukauf/Partnerschaft mit einem
der 40 bestehenden Telefonservices als über Eigenaufbau — was direkt in
**Chance 2** mündet.

---

### Chance 10 — Enterprise-Voice für den deutschen Mittelstand (Lücke zwischen 299 € und 150.000 $)
**Urteil: ECHTE LÜCKE, aber der falsche Käufer für Nico.**

Die Preistabelle §1.5 zeigt ein klaffendes Loch: KMU-Produkte enden bei
299 €/Monat [F], Enterprise beginnt bei ~150.000 USD/Jahr Vertragswert
(PolyAI) [F] bzw. bei Parloa/Cognigy/VIER im nicht publizierten
Enterprise-Segment. Dazwischen — der klassische deutsche Mittelständler mit
200–2.000 Mitarbeitern, der 1.000–5.000 €/Monat zahlen würde — liegt ein
weitgehend unbedientes Band [S].

*Warum bedient es niemand?* Weil Enterprise-Anbieter mit
150.000-$-Deals höhere Deckungsbeiträge je Vertriebsstunde erzielen und
KMU-Anbieter Self-Service-Ökonomie brauchen. Das mittlere Band erfordert
**beratungsintensiven Direktvertrieb mit 3–6 Monaten Zyklus** — genau das, was
die beiden Extreme meiden.

*Der Haken für Nico:* Genau dieser Vertrieb ist Anzug-Business mit
IT-Sicherheitsfragebögen, Betriebsratsbeteiligung und Ausschreibungen. Das
kollidiert mit Nicos Anti-Kriterien („steifes Anzug-Business",
„Abhängigkeit von Konzernen"). Es ist eine echte Marktlücke — aber nicht seine.

---

### Chancen-Bilanz

| # | Chance | Urteil | Belegqualität |
|---|---|---|---|
| 1 | Standalone KI-Telefonassistent DACH | **FRIEDHOF im Entstehen** | hoch — 5 unabhängige Signale [F] |
| 2 | White-Label-Voice für 40+ Telefonservices | **ECHT**, Fenster 18–30 Monate | hoch [F] |
| 3 | Voice + ERP End-to-End | halbe Lücke, wird geschlossen | hoch [F] |
| 4 | Wartungsvertrags-Betriebssystem | **ECHT** | mittel — Legacy-ERPs ungeprüft |
| 5 | Compliance-Monitoring mit Sensorik | **ungeprüft** | keine — Prüfauftrag |
| 6 | Pay-per-Outcome | **ECHT in DACH** | mittel [F] |
| 7 | DSGVO als Kern | **FRIEDHOF** | hoch [F] |
| 8 | Mehrsprachigkeit | **FRIEDHOF** (Feature) | hoch [F] |
| 9 | KI + Mensch hybrid in DACH | **ECHT** | hoch [F] |
| 10 | Mittelstandslücke 299 €–150k $ | ECHT, falscher Käufer | mittel [S] |

---

## 6. VERTEIDIGBARKEIT FÜR EINEN NEUEINSTEIGER

### 6.1 Funding-Übersicht (wer kann wie lange Verluste tragen)

| Anbieter | Feld | Kapital | Quelle |
|---|---|---|---|
| **Parloa** (DE) | A Enterprise | **> 560 Mio. USD**, Bewertung 3 Mrd. USD (01/2026) [F] | techcrunch.com |
| **Cognigy** (DE) | A Enterprise | **für 955 Mio. USD an NiCE verkauft** (09/2025); zuvor > 170 Mio. USD VC [F] | handelsblatt.com |
| **PolyAI** (UK) | A Enterprise | 86 Mio. USD Series D (12/2025), Bewertung 750 Mio. USD [F] | cloudtalk.io |
| **Bland AI** (US) | A Infra | 65 Mio. USD gesamt [F] | builts.ai |
| **Vapi** (US) | A Infra | ca. 72 Mio. USD (2,1 + 20 + 50) [S] | sovereignmagazine.com |
| **Synthflow** (DE/US) | A Infra | 20 Mio. USD Series A (Accel) [F] | retellai.com |
| **Retell AI** (US) | A Infra | nur 5,1 Mio. USD, behauptet 50 Mio. USD ARR [F] | tested.media |
| **plancraft** (DE) | B | **> 50 Mio. €**, davon 38 Mio. € Series B (08/2025) [F] | plancraft.com/presse |
| **Air.ai** (US) | A | **tot** — 18 Mio. USD FTC-Vergleich [F] | thoughtly.com |
| Telekom / Cisco (Placetel) / sipgate | A | Konzernbilanzen | — |

### 6.2 Verteidigbarkeitsurteil je Feld

**Feld A — Verteidigbarkeit: SEHR NIEDRIG (2/10).**
- Eintrittsbarriere technisch nahe null: Retell/Vapi/Bland liefern die Engine
  ab 0,11 USD/Min ohne Monatsminimum [F].
- Downstream-Bedrohung: Telcos bundeln (Placetel 9 €/Nr. [F], Telekom im Netz [F]).
- Upstream-Bedrohung: Modellanbieter integrieren vorwärts.
- Sideways-Bedrohung: Vertikale Plattformen absorbieren (Aaron→Doctolib [F],
  Label Software [F]).
- Kapitalasymmetrie: Parloa 3 Mrd. USD Bewertung [F].
- **Der einzige verteidigbare Graben in Feld A ist nicht die Technik, sondern
  der Vertriebszugang zu einer Kundengruppe, die ein Neueinsteiger schneller
  erreicht als die Konzerne.** Das ist ein Distributionsvorteil, kein
  Produktvorteil — und er ist nicht verkaufbar (Kriterium 8).

**Feld B — Verteidigbarkeit: NIEDRIG (3/10).**
Besetzt, VC-finanziert, konsolidierend, Preisband 15–250 € [F], erfordert
500–1.900 Kunden für die Zielgröße [S]. Ausnahme: die Wartungsvertrags-Nische
(Chance 4), die genau deshalb offen ist, weil sie für VC zu klein ist.

**Feld C — Verteidigbarkeit: vermutlich HOCH, aber unbelegt (? /10).**
Die Argumente (Pflichtkauf, Hardware im Objekt, Datenhistorie, hohe
Wechselkosten, wenige große Kunden) sind theoretisch stark und passen zu
Kriterium 8 (Unternehmenswert) und Kriterium 5. **Ohne Anbieter- und
Preisrecherche darf daraus keine Bewertungszahl abgeleitet werden.**

### 6.3 Die harte Gesamtaussage

Feld A ist der Bereich, in dem Nicos bestehende Assets (CallSuite, Twilio,
deutsche Rufnummer, Supabase-Datenmodell) den größten
Geschwindigkeitsvorteil geben — und zugleich der Bereich mit der **schlechtesten
Verteidigbarkeit und dem niedrigsten Preispunkt**. Nach Methodik-Regel 8
darf der Asset-Vorteil ausschließlich auf „Geschwindigkeit bis zum ersten
Umsatz" und „Startkapitalbedarf" wirken. Er darf **nicht** die Bewertung von
Wettbewerbsvorteil und Unternehmenswert heben. Genau das ist hier die
Versuchung, vor der Methodik-Regel 11 (Freedom-Inbound-Neutralität) warnt.

Die belegte Schlussfolgerung dieses Agenten lautet: **Voice ist ein
hervorragender Türöffner und eine schlechte Maschine A.** Der Wert entsteht
nicht dort, wo der Anruf angenommen wird, sondern dort, wo aus dem Anruf eine
wiederkehrende, nachweispflichtige, technisch verankerte Leistung wird.

---

## 7. NACHRECHERCHE-AUFTRAG (priorisiert)

**Priorität 1 — Feld C, vollständig (höchster Erkenntniswert je Suchanfrage):**
1. Trinkwasser-/Legionellen-Monitoring: Anbieter, Abo-Preise, Vertragslaufzeiten
   (Stichworte: Legionellenprüfung Abo, Trinkwasserhygiene Monitoring Preise,
   TrinkwV Betreiberpflicht Dienstleister)
2. Aufzugs-Fernüberwachung: KONE 24/7 Connected Services, Schindler Ahead,
   TK Elevator MAX — Preismodelle, ob als Zusatzabo verkauft
3. Kälte-/Klimatechnik-Fernüberwachung: Anbieter, Preis je Anlage/Monat
4. Brandschutz-Prüfabos und Wartungsverträge nach DIN 14675: Preisbildung
5. Energiemonitoring nach EnEfG: Schwellenwerte (7,5 GWh/a), Pflichtenumfang,
   Anbieterpreise
6. Ladeinfrastruktur CPO-as-a-Service: reev, chargecloud, has·to·be/Elli —
   Preis je Ladepunkt/Monat, Vertragsmodelle
7. **Friedhofsprüfung Predictive Maintenance:** Welche Industrie-4.0-Sensorik-
   Startups 2016–2022 sind gescheitert und warum? (Optimierungs- vs.
   Pflichtkauf-Hypothese aus §5, Chance 5)
8. **Rechtsprüfung:** Wo genau verläuft die Grenze zwischen akkreditierungs-
   pflichtiger Prüfleistung (K.-o. nach `01` §6.3) und freier
   Monitoring-/Nachweisdienstleistung?

**Priorität 2 — Feld B Lücken:**
9. ServiceTitan (Preis je Techniker/Monat, Umsatz, Börsengang), Jobber,
   Housecall Pro, simPRO — Preise und Kundenkritik
10. Streit V.1, Moser, Sander & Doll, 1Tool — **Kernfrage: Hat einer von ihnen
    Wartungsvertrags-/Prüffristenverwaltung als Kernobjekt?** Davon hängt
    Chance 4 ab.
11. Kundenkritik G2/Capterra/OMR zu ToolTime, plancraft, Craftnote — Churn-
    Gründe, Ablehnungsgründe

**Priorität 3 — Feld A Validierung:**
12. Primärquellen-Check aller [F]-Preise aus §1 (die Aggregatoren sind
    Wettbewerber, siehe §1.6)
13. Telekom Magenta AI Call Assistant: Rollout-Datum und Preis — der wichtigste
    Einzelwert für Chance 1
14. Zahlungsbereitschaft-Validierung: Zahlt ein deutscher Handwerksbetrieb
    2.000–3.000 €/Monat für irgendetwas? Wenn nein, ist die Arithmetik aus
    §2.3 auch für Feld A und die Chancen 2/4 tödlich.

---

## 8. QUELLENVERZEICHNIS

Alle Quellen sind Suchergebnis-Extrakte vom 2026-08-05. Direkter Seitenabruf
war technisch nicht möglich (§0).

**Feld A international:** cloudtalk.io/blog/goodcall-pricing · vida.io/blog/goodcall-pricing ·
serviceagent.ai/blogs/goodcall-pricing · synthflow.ai/blog/slang-ai-pricing ·
loman.ai/blog/slang-ai-reviews-pricing-alternatives · slang.ai ·
oncrew.ai/blog/rosie-ai-pricing-2026 · heyrosie.com/blog/answering-service-cost ·
oncrew.ai/blog/numa-pricing-2026 · serviceagent.ai/blogs/numa-pricing ·
fast.io/resources/smith-ai-review-2026 · cloudtalk.io/smith-ai-pricing ·
loman.ai/blog/smith-ai-pricing · ruby.com/plans-and-pricing ·
vida.io/blog/ruby-receptionists-pricing · vida.io/blog/answerconnect-pricing ·
serviceagent.ai/blogs/answerconnect-pricing · cloudtalk.io/poly-ai-pricing ·
nurix.ai/blogs/polyai-pricing-features-guide · thoughtly.com/blog/air-ai-review ·
trillet.ai/blogs/air-ai-ftc-lawsuit-status-2026 · serviceagent.ai/blogs/air-ai-review

**Feld A Infrastruktur:** medium.com/@automation.labs (Vapi vs Retell vs Bland) ·
cekura.ai/blogs/retell-ai-pricing-per-minute · builts.ai/blog/vapi-vs-bland-ai-vs-retell-ai ·
tested.media/retell-vs-vapi-vs-bland-vs-synthflow · retellai.com/blog/vapi-vs-synthflow ·
sovereignmagazine.com/article/vapi-ai-50m-series-b-voice-agents ·
techcrunch.com/2026/01/15 (Parloa) · vestbee.com/insights/articles/parloa-raises-350-m ·
siliconangle.com/2026/01/15 · handelsblatt.com (NiCE/Cognigy) ·
cognigy.com/de/news/nice-schließt-akquisition-von-cognigy-ab ·
business-punk.com (Cognigy-Exit)

**Feld A DACH:** fonio.ai/en/pricing · fonio.ai/de/news-cool-stuff/ki-telefonassistent-kosten-10-anbieter-im-vergleich-2025 ·
vokaro.net/kosten/ki-telefonassistent-kosten · vokaro.net/blog/beste-ki-telefonassistenten-deutschland-2026 ·
speakki.de/blog/ki-telefonassistent-kosten · zeeg.me/de/blog/content/aaron-telefonassistent ·
zeeg.me/de/blog/content/ki-telefonassistent-kosten · ordicall.ai/blog/ki-telefonassistent-arztpraxis-anbieter-vergleich ·
placetel.de/ratgeber/ki-telefonassistent · premium-electronics.eu (Placetel AI) ·
help.sipgate.de/cloud-telefonanlage/…/sipgate-ai-agents · handelsblatt.com/technik/it-internet/…/100204610.html (Telekom) ·
label-software.de/ki-in-handwerkersoftware/ki-telefonassistent · squt.de (VIER) ·
digital-affin.de/blog/voicebot-anbieter · ihretelefonzentrale.de/blog/ki-telefonassistent-kosten ·
telefonie-strategie.de/ratgeber/ki-telefonassistent-kosten · autarc.energy/global/knowledge/anbieter-voice-agent ·
omr.com/de/reviews/contenthub/ki-telefonassistent-handwerk

**Feld A Telefonservices DACH:** ebuero.de/preisverzeichnis/telefonsekretariat ·
telefon.services/anbieter · telefon.services/anbieter/ebuero · starbuero.de/preise ·
starbuero.de/handwerk · cloudsecretary.de/telefonservice-bueroservice-fuer-handwerker ·
phonea.de/telefonservice-tarife · bs-strate.de/pages/telefonservice-handwerk.php ·
mobile-office.de/telefonservice-preise

**Feld B:** trusted.de/tooltime-kosten · omr.com/en/reviews/product/tooltime/pricing ·
handwerk-digitalisieren.de/tooltime-handwerkersoftware · trusted.de/plancraft-kosten ·
flinki.ai/tools/plancraft · craftnote.de/preise · ki-syndikat.de/tools/craftnote ·
softwareabc24.de/handwerker-software/craftnote · plancraft.com/de-de/presse/38-millionen-fur-plancraft ·
eu-startups.com/2025/08 (plancraft €38M) · vc-magazin.de/blog/2025/08/13/plancraft-38-mio-series-b ·
blog.meisterwerk.app/handwerksunternehmer/handwerker-software-vergleich-6-anbieter ·
meisterox.app/blog/handwerker-software-vergleich · handwerkersoftware.pro

**Feld C:** keine.
