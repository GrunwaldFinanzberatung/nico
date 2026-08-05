# 06 – Wettbewerbsanalyse

Stand: 2026-08-05 · Quelle: Agent 03 (`raw/agent03_wettbewerb.md`), ergänzt um
Orchestrator-Nachrecherche (`raw/orchestrator_feldC_nachrecherche.md`) und
Agent 01/02/10.

**Belegqualität:** WebFetch war in dieser Umgebung durchgängig blockiert
(HTTP 403, Egress-Policy). **Keine Anbieter-Preisseite konnte direkt gelesen
werden.** Alle Preise stammen aus Suchergebnis-Extrakten. Sie sind mit **[F]**
gekennzeichnet, weil sie belegt sind — aber die Quelle ist in vielen Fällen ein
Aggregator, nicht der Anbieter. Vor jeder Entscheidung an der Primärquelle
prüfen. Siehe dazu die Quellenkritik in §4.

---

## 1. Feld A – KI-Telefonie und Telefonservice

### 1.1 DACH – KI-Telefonassistenten

| Anbieter | Land | Zielgruppe | Setup | Monatlich | Nutzung | Schwäche |
|---|---|---|---|---|---|---|
| **fonio.ai** | AT | KMU, Handwerk, Kanzleien | k. A. | Solo 99 € · Team 299 € [F] | 1.000 bzw. 3.000 Min inkl., danach 0,12–0,15 €/Min [F] | Feature-Entbündelung (Zusatznummer 7 €, WhatsApp 79 €) treibt Effektivpreis |
| **Vokaro** | DE | KMU, Gesundheit, Handwerk | Aktion: 0 € [F] | 99 € regulär, 69 € Aktion [F] | k. A. | Rabattgetriebene Positionierung, sehr kleine Firma |
| **SpeakKI** | DE | KMU | 0 €, monatlich kündbar [F] | nicht auffindbar | 50 Freiminuten [F] | Preise nicht öffentlich |
| **Aaron.ai** | DE | Arztpraxen | k. A. | ab 119 €/Behandler [F] | k. A. | **Seit 2024 in Doctolib aufgegangen, separat nicht mehr buchbar** [F] |
| **Placetel AI** | DE | eigene TK-Bestandskunden | k. A. | **+9 €/Monat je KI-Rufnummer** [F] | Minutenpakete | nur für Placetel-Kunden — genau das ist die Waffe |
| **sipgate AI Agents** | DE | eigene Bestandskunden | k. A. | Freiminutenpakete [F] | — | nur für sipgate-Kunden |
| **Telekom Magenta AI Call Assistant** | DE | Massenmarkt | — | **Preis offen, evtl. inklusive** [F] | — | **wird ins Netz integriert** — größte strukturelle Bedrohung des Feldes |
| **HalloPetra** | DE | SHK, Elektro, Kälte | k. A. | k. A. | k. A. | >1.000 Betriebe laut Eigenangabe [F, ungeprüft] |
| **FoxifAI** | DE | KMU | **1.920 € Setup** [F-sek] | ab 100 € [F-sek] | — | belegt: deutsche KMU akzeptieren Setup-Gebühren |
| **Label Software** | DE | Handwerk | — | — | — | **Handwerker-ERP mit integriertem KI-Telefonassistenten** [F] |

### 1.2 DACH – menschliche Telefonservices (die Bestandsindustrie)

| Anbieter | Grundgebühr | Nutzungspreis |
|---|---|---|
| **ebuero AG** (Marktführer) | 59,90 / 99,90 / 179,90 € [F] | **1,04–1,39 €/Min** [F]; +19,90 € für 24/7 |
| **starbuero.de** | 0 € [F] | **0,49 €/Bearbeitungsminute** [F] |
| **Cloudsecretary** | 0 € | **ab 0,99 € je angenommenem Anruf** [F] |
| **phonea** | 0 € | **1,70 € je Anruf** (Handwerkertarif) [F] |
| **Büroservice Strate** | — | 0,65 €/Min + 0,99 €/Anruf [F] |
| Marktbreite | **über 40 deutsche Anbieter im Vergleichstest gelistet** [F] |

### 1.3 International

| Anbieter | Land | Monatlich | Nutzung |
|---|---|---|---|
| Goodcall | US | 79 / 129 / 249 USD **je Agent** [F] | 0,50 USD je Unique Caller über Kontingent [F] |
| Rosie | US | 49 / 149 / 299 USD [F], **kein Setup** | 250/1.000/2.000 Min inkl. |
| Slang.ai | US | 399 / 599 USD **je Standort** [F] | unlimitiert |
| Numa | US | Quote-only, ~149 USD/User [F] | teils **pay-per-booked-appointment** [F] |
| Smith.ai | US | Human ab 292,50 USD/30 Calls; AI ab 95 USD [F] | Overage 9,75–10,50 USD **je Anruf** [F] |
| Ruby | US | 245–1.725 USD [F] | **3,53–4,90 USD/Min** [F] |
| AnswerConnect | US | 179–575 USD [F], Setup 75 USD | 1,75–2,25 USD/Min [F]; wirbt mit **„no AI, no bots"** |
| PolyAI | UK | kein öffentlicher Preis | Verträge **ab ~150.000 USD/Jahr** [F, Drittschätzung] |
| **Air.ai** | US | 25.000–100.000 USD Vorablizenz [F] | **TOT** – FTC-Klage 08/2025, 18 Mio. USD Vergleich 03/2026, Vermarktungsverbot [F] |

### 1.4 Infrastruktur-Layer

| Anbieter | Beworben | **Reale Vollkosten** | Funding |
|---|---|---|---|
| Vapi | 0,05 USD/Min [F] | **0,10–0,30 USD/Min** [F] | ~72 Mio. USD [S] |
| Retell AI | 0,07 USD/Min [F] | **0,11–0,31 USD/Min** [F] | 5,1 Mio. USD offengelegt, behauptet 50 Mio. USD ARR [F] |
| Bland AI | 0,11–0,14 USD/Min [F] | wie gelistet | 65 Mio. USD [F] |
| Synthflow | DE/US, White-Label | k. A. | 20 Mio. USD Series A (Accel) [F] |
| **Parloa** | DE, Enterprise | k. A. | **>560 Mio. USD, Bewertung 3 Mrd. USD** (01/2026) [F] |
| **Cognigy** | DE, Enterprise | k. A. | **für 955 Mio. USD an NiCE verkauft** (09/2025) [F] |

> **Der wichtigste Einzelbefund des Feldes:** Beworbener Minutenpreis
> (0,05–0,07 USD) und realer Vollkostenpreis (0,10–0,31 USD) liegen um
> **Faktor 2–5** auseinander, weil LLM-Token, Premium-Stimmen und Telefonie
> nicht enthalten sind [F]. **Jede Kalkulation mit dem Listenpreis ist falsch.**

### 1.5 Die Arbitrage – und warum sie sich schließt

- Menschlich DACH: **1,04–1,39 €/Min** (ebuero) [F]
- KI-Vollkosten: **ca. 0,10–0,12 €/Min** [S]
- → **Faktor 9–13** Kostenvorteil [S]; gegen Ruby sogar Faktor 30–45 [S]

**Aber:** fonio Solo = 99 € für 1.000 Freiminuten = **0,099 €/Min bei
Vollausschöpfung** [S] — das liegt **unter** den eigenen Plattform-Vollkosten.
Die Marge dieses Marktes kommt aus **Unterauslastung, nicht aus Wertschöpfung**.
Das ist ein instabiles Preisgleichgewicht.

---

## 2. Feld B – Vertikale Software für deutsches Handwerk

| Anbieter | Monatlich | Je weiterem Nutzer | Bindung |
|---|---|---|---|
| **ToolTime** | SOLO 79 € · TEAM 149 € · MAX ab 220 € [F] | 22 € (Jahres-VZ) / 34 € (monatlich) [F] | 1 oder 12 Monate [F] |
| **plancraft** | Business 74,90 € · Pro 139,90 € · Premium 249,90 € [F] | Büro-User 39,92–59,90 €; mobil 15,92–24,90 € [F] | Listenpreis nur bei 2 Jahren [F] |
| **Craftnote** | Baustelle 14,90 € · Fahrzeug 24,90 € · Büro 29,90 € · Büro Plus 49,90 € je Nutzer [F] | — | jährliche Abrechnung; **kein Gratisplan mehr** [F] |

**Gesamtband: 15–250 €/Monat je Betrieb bzw. Nutzer** [F].

**Strukturbefund:** Der Markt ist besetzt, VC-finanziert und konsolidiert.
plancraft: **38 Mio. € Series B (08/2025)**, Gesamtfinanzierung > 50 Mio. €,
**> 20.000 Kunden in 11 Ländern**, Mittel explizit für KI-Features [F].
Es existiert bereits eine Vermittlungsschicht (handwerkersoftware.pro) —
ein Zeichen für Marktreife, nicht für eine Lücke.

---

## 3. Feld C – Betreiberverantwortung, Wartung, Monitoring

Dieses Feld war bei Agent 03 datenleer und wurde vom Orchestrator nachrecherchiert.

### 3.1 Anbieterlandschaft (existiert, entgegen ursprünglicher Annahme)

**Prüffristen-/Betreiberverantwortungs-Software:** Maqsima (myFM, TMS) ·
Prüfpilot/Cloudbrixx (>2.000 Prüfregeln) · mybuilding24 · HOPPE Wartungsplaner/
Prüfplaner · ELISA (Fraunhofer IFF) · waveware · loyhutz CARE · TOL · Planon ·
PwC IWMS · **TÜV SÜD netinform.RE** · TÜV Rheinland „Roter Faden"

**ERP für Prüfdienstleister:** Certado Suite („zeigt automatisch, welcher Kunde
wann fällig ist", automatische Erinnerungen) · Vemas (Termin-/Tour-/
Ressourcenoptimierung) · firstaudit

**Kälte/F-Gase-Anlagenbuch:** SHKwin · KaltimaCheck · RefrigerantTracker ·
ServicePilot · KlimaCraft

### 3.2 Belegte Preisanker

| Leistung | Preis | Takt |
|---|---|---|
| DGUV V3, ortsveränderliche Geräte | **3–8 €/Gerät** [F] | 6–24 Monate |
| DGUV V3, ortsfeste Anlagen | **50–150 €/Anlage** [F] | 4 Jahre |
| Wartungsvertrag Gewerbe-Klimaanlage | **200–600 €/Anlage/Jahr** [F] | jährlich |
| Aufzugswartungsvertrag | **1.500–3.000 €/Jahr je Anlage** [F] | laufend |
| Aszendio (nutzungsbasiert) | **ab 930 €/Jahr (77,50 €/Monat)** + variabel [F] | laufend |
| Objektaufschaltung Leitstelle | **20–60 €/Monat je Objekt** [F] | laufend |
| Facility Management (München) | **1,50–6,00 €/m²/Monat** [F] | laufend |
| Legionellen-Gefährdungsanalyse | 390 € (≤10 WE) / 890 € (≤50) / 3.350 € (≤100) [F] | anlassbezogen |
| PV-Betriebsführung | **8–15 €/kWp/Jahr** [F] | 20–30 Jahre |

### 3.3 Gesetzliche Takte (der ökonomische Kern)

| Pflicht | Grundlage | Takt |
|---|---|---|
| Dichtheitsprüfung Kälte/Klima/WP | **F-Gase-VO (EU) 2024/573** | 3/6/12 Monate je CO₂-Äq.; ≤30 kW jährlich, >30 kW halbjährlich [F] |
| Elektrische Betriebsmittel | DGUV V3 / § 3 BetrSichV | 6–24 Monate [F] |
| Ortsfeste Elektroanlagen | DGUV V3 | 4 Jahre [F] |
| Betreiberpflichten gesamt | Bund + Länder | **über 50 verschiedene Pflichtvorschriften** [F] |

### 3.4 Die Rechtsschranke, die das Produkt formt

Betreiberpflichten **können delegiert werden**, aber die **Gesamtverantwortung
bleibt beim Betreiber/Eigentümer** [F]. Die Delegation verlangt: sorgfältige
Auswahl und Eignungsprüfung, klare Definition der Pflichten, **Schriftform mit
Gegenzeichnung**, Bereitstellung aller Mittel [F].

→ Ein Produkt darf **nicht** „wir übernehmen Ihre Haftung" versprechen. Es muss
**Nachweisfähigkeit** verkaufen. Damit ist K.-o.-Kriterium 3 nicht verletzt,
solange die prüfpflichtige Leistung bei qualifizierten Partnern eingekauft und
deren Eignung dokumentiert wird.

---

## 4. Quellenkritik – der Review-Korpus ist wettbewerbsgefärbt

Auffällig viele auffindbare „Anbietervergleiche" und „Pricing Guides" werden von
**direkten Wettbewerbern** betrieben:

| „Review"-Seite | Betreibt | Bewertet |
|---|---|---|
| synthflow.ai/blog/goodcall-review | Synthflow | Goodcall |
| retellai.com/blog/…synthflow… | Retell | Synthflow |
| thoughtly.com/blog/retell-ai-review | Thoughtly | Retell |
| serviceagent.ai/blogs/… | ServiceAgent | Smith.ai, Goodcall, Rosie |
| dialora.ai/blog/… | Dialora | Smith.ai, Synthflow, Goodcall |
| myaifrontdesk.com/blogs/… | My AI Front Desk | Rosie |
| cloudtalk.io, vokaro.net, fonio.ai/…/vergleich | jeweils Anbieter | alle anderen |

Bei HVAC-/Plumbing-Suchen bestand die Trefferliste zusätzlich fast vollständig
aus **GoHighLevel-White-Label-Funnels** (`app.gohighlevel.com/v2/preview/…`).

**Zwei Folgerungen:**

1. Alle Fremdpreise sind vor einer Entscheidung an der Primärquelle zu prüfen.
2. Dass praktisch jeder Anbieter dieses SEO-Spiel spielt, ist selbst ein
   Marktsignal: **Die Kundenakquise läuft über Preisvergleiche — der Markt ist
   in der Preiskampfphase**, typisch für einen Markt kurz vor der
   Kommoditisierung, nicht für einen frühen Markt.

**Nicht verwendbare Zahlen:** Die überall zitierten Angaben „27 % der Anrufe
unbeantwortet", „1.200 $ Verlust je verpasstem Anruf", „85 % hinterlassen keine
Nachricht" stammen ausschließlich aus GoHighLevel-Verkaufsseiten ohne
Primärquelle. **[A] – nicht als Fakt verwenden.**

---

## 5. Verteidigbarkeit für einen Neueinsteiger

| Feld | Note | Begründung |
|---|---|---|
| **A – Voice** | **2/10** | Engine ab 0,11 USD/Min ohne Monatsminimum verfügbar; Telcos bundeln downstream (Placetel 9 €, Telekom im Netz); Modellanbieter integrieren upstream; Vertikalplattformen absorbieren sideways (Aaron→Doctolib, Label Software); Kapitalasymmetrie (Parloa 3 Mrd. USD). Der einzige Graben ist Vertriebszugang — ein Distributionsvorteil, kein Produktvorteil, und **nicht verkaufbar**. |
| **B – Handwerk-SaaS** | **3/10** | Besetzt, VC-finanziert, konsolidierend; 500–1.900 Kunden für die Zielgröße nötig. Ausnahme: die Wartungsvertrags-Nische, offen genau weil sie für VC zu klein ist. |
| **C – Betreiberpflichten/Monitoring** | **vermutlich hoch, teilbelegt** | Pflichtkauf, Hardware im Objekt, Datenhistorie, hohe Wechselkosten, wenige große Kunden. Software-Schicht ist besetzt; die **Managed-Service-Schicht für 50–500-MA-Standorte** ist es nach zwei Suchen nicht — Negativbefund muss gehärtet werden. |

---

## 6. Die zehn geprüften Chancen mit Friedhofsurteil

| # | Chance | Urteil | Belegqualität |
|---|---|---|---|
| 1 | Standalone KI-Telefonassistent DACH | **FRIEDHOF im Entstehen** | hoch – 5 unabhängige Signale [F] |
| 2 | White-Label-Voice für 40+ Telefonservices | **ECHT**, Fenster 18–30 Monate [A] | hoch [F] |
| 3 | Voice + ERP End-to-End | halbe Lücke, wird geschlossen | hoch [F] |
| 4 | Wartungsvertrags-Betriebssystem | **ECHT** (enger gefasst als ursprünglich) | mittel – Legacy-ERPs ungeprüft |
| 5 | Compliance-Monitoring mit Sensorik | **teilweise besetzt** (siehe §3.1) | mittel nach Nachrecherche |
| 6 | Pay-per-Outcome | **ECHT in DACH** (nur Numa/US macht es) | mittel [F] |
| 7 | DSGVO als Kern | **FRIEDHOF** – 5 von 5 DACH-Anbietern führen dasselbe Argument | hoch [F] |
| 8 | Mehrsprachigkeit | **FRIEDHOF** – bei Ruby/AnswerConnect in jedem Tarif inklusive | hoch [F] |
| 9 | KI + Mensch hybrid in DACH | **ECHT** – nur Smith.ai (US) kombiniert beides | hoch [F] |
| 10 | Mittelstandslücke 299 €–150k $ | ECHT, aber falscher Käufer (Anzug-Business) | mittel [S] |

---

## 7. Die Feature-Lücken, die niemand schließt

**Lücke I – „Vom Anruf bis zum abgerechneten Auftrag" in einem Vertrag.**
Voice-Anbieter enden beim Kalendereintrag. ERP-Anbieter beginnen beim Auftrag.
Dazwischen liegt eine Bruchkante, die kein untersuchter Anbieter überbrückt.
Label Software greift als einziger von der ERP-Seite aus in Richtung Telefonie —
das zeigt, wohin die Konsolidierung läuft.

**Lücke II – „Wartungsvertrag" statt „Projekt" als Datenmodell.**
Die gesamte deutsche Handwerkersoftware ist projekt- und angebotszentriert.
Kein untersuchter Anbieter führt Anlage, Wartungszyklus, Prüffrist und
Nachweispflicht als First-Class-Objekte. Für Betriebe, deren Umsatz aus
*wiederkehrenden Wartungsverträgen* stammt, ist die vorhandene Software
strukturell falsch gebaut.

**Lücke III – Prüfpflicht + KI-Outbound-Terminierung.**
Drei Lager existieren getrennt: Prüfsoftware (kennt die Fälligkeiten),
Dienstleister-ERP (optimiert Touren), KI-Telefonie (**inbound-only**).
**Kein Anbieter ruft systematisch gegen eine Fälligkeitsliste an.**
Negativbefund aus 3 Suchen — schwach, muss gehärtet werden.
