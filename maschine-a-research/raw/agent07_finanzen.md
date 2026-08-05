# Agent 07 – Finanz- und Skalierungsanalyse

Stand: 2026-08-05 · Auftrag: Welle 2, Leitfrage „Rechnet sich das konservativ – Break-even,
Kapitalbedarf, Sensitivität?" · Gegenstand: S01, S02, S03, S04, S13
· Datenausgabe: `10_finanzmodelle.csv` (375 Datenzeilen, 15 Modell-Szenario-Kombinationen × Monat 0–24)

---

## 0. Das Ergebnis in sieben Sätzen

1. **Kein einziges Modell erreicht im realistischen Szenario 30.000 € netto privat innerhalb von 24 Monaten** – die schnellsten (S04, S13) brauchen 36–37 Monate, S01 47 Monate, S02 50 Monate, S03 60 Monate.
2. **In allen fünf konservativen Szenarien scheitert das Vorhaben** – drei erreichen nie einen Break-even (S02, S03, S13), zwei erst in Monat 52–54 (S01, S04). Das konservative Szenario ist kein Puffer, es ist ein Abbruchszenario.
3. **Annahme A1 (20.000–60.000 € Startkapital) trägt kein realistisches Szenario.** Nur die *absoluten* Kapitaluntergrenzen von S13 (33.600 €) und S02 (46.300 €) liegen innerhalb von A1 – und zwar ohne jeden Puffer, d. h. bei exakter Planerfüllung.
4. **Der tödlichste Hebel ist in vier von fünf Modellen der CAC, nicht der Churn.** CAC +100 % verdreifacht bis vervierfacht den Kapitalbedarf und verschiebt den Break-even um 13–25 Monate. Churn +50 % kostet dagegen selten mehr als 3 Monate.
5. **Der zweittödlichste Hebel ist der Vertriebszyklus.** Verdoppelt er sich, verschiebt sich das 100.000-€-Ziel um 14–20 Monate – bei praktisch unverändertem Deckungsbeitrag. Zeit ist in diesen Modellen teurer als Marge.
6. **S03 in der Hardware-Mietvariante ist mit 2,04 Mio. € Kapitalbedarf strukturell nicht finanzierbar** und muss zwingend als Hardware-*Verkauf* strukturiert werden, sonst fällt das Modell aus.
7. **Kapitaleffizientestes Modell ist S02 (Terminierungs-Abo)**, gefolgt von S13. S03 ist das kapitalineffizienteste und in jeder Variante das teuerste.

---

## 1. Gemeinsame Rechengrundlagen

### 1.1 Steuerrechnung – die Nordstern-Diskrepanz nachgerechnet

Standort Oldenburg / Nordwest-Niedersachsen (Annahme A3).

| Position | Satz | Kennung | Rechenweg |
|---|---|---|---|
| Gewerbesteuer-Hebesatz Oldenburg | 439 % | [F] IHK-Übersicht Hebesätze, Stand 06/2025 | – |
| Gewerbesteuer effektiv | 15,365 % | [S] | 3,5 % Messzahl × 4,39 |
| Körperschaftsteuer + SolZ | 15,825 % | [F] | 15 % × 1,055 |
| **Belastung thesauriert** | **31,19 %** | [S] | 15,365 + 15,825 |
| Kapitalertragsteuer + SolZ auf Ausschüttung | 26,375 % | [F] | 25 % × 1,055 |
| **Gesamtbelastung bei Vollausschüttung** | **49,34 %** | [S] | 1 − (1−0,3119) × (1−0,26375) |

**Ergebnis:** Für **30.000 € netto/Monat privat** braucht die GmbH einen
**Vorsteuergewinn von 59.217 €/Monat** = **710.600 €/Jahr** [S].

Das bestätigt die Rechnung aus `01_nordstern_und_anforderungen.md` (dort 57.000–60.000 €)
punktgenau. Bei einer EBITDA-Marge von 30 % entspricht das **197.400 € Monatsumsatz** [S] –
also erneut dem Doppelten des 100.000-€-Zwischenziels.

**Zwei Präzisierungen, die die Ausgangsrechnung nicht enthält:**

- **Kirchensteuer ist nicht eingerechnet.** Bei Kirchensteuerpflicht steigt die Belastung auf der Ausschüttung auf ca. 27,8 % und die Gesamtbelastung auf **50,4 %** → EBT-Bedarf **60.500 €/Monat** [S].
- **Der Auszahlungsweg ist nicht neutral.** Ein Geschäftsführergehalt ist Betriebsausgabe und mindert GewSt+KSt; die Belastung liegt dann bei der Einkommensteuer (Spitzensatz 45 % + SolZ, Durchschnittsbelastung bei ~700 k € Bruttobezug ca. 44–46 % [S]). Ein optimierter Mix aus GF-Gehalt und Ausschüttung senkt die Gesamtbelastung realistisch auf **46–48 %** [S] → EBT-Bedarf **57.700–59.200 €/Monat**. Die Bandbreite ist so schmal, dass sie an keiner Modellbewertung etwas ändert. **Ich rechne durchgehend mit 59.217 €.**

Wenn man einen Hebesatz von 350 % annimmt (Umlandgemeinden wie Wardenburg/Hatten), sinkt die
Gesamtbelastung auf 47,1 % und der EBT-Bedarf auf 56.700 €/Monat [S] – ein Standortvorteil von
ca. **2.500 € EBT/Monat**, nicht mehr. **Steuergestaltung löst dieses Problem nicht. Nur Umsatz löst es.**

### 1.2 Fixkostenbaukasten (monatlich, ohne Personal)

| Position | Betrag M1–12 | Quelle / Kennung |
|---|---|---|
| Steuerberater-Flatrate (lfd. Buchhaltung, Lohn, Beratung) | 380 € | [F] Flatrate-Kanzleien 299–449 €/Monat |
| Rückstellung Jahresabschluss + Steuererklärungen | 250 € | [S] aus [F] 2.000–7.000 €/Jahr, konservativ 3.000 € |
| Betriebs- + Vermögensschadenhaftpflicht, Cyber | 150 € | [S] aus [F] Solo-IT ab 12 €/Monat; mit VSH+Cyber und höheren Deckungssummen 1.200–2.400 €/Jahr |
| Laufende Rechtsberatung (Verträge, AVV, AGB) | 300 € | [A] |
| Büro / Coworking Region Oldenburg | 250 € | [A] |
| Software-Grundstack (Workspace, CRM, Buchhaltung, Vertragstool) | 300 € | [A] |
| Hosting / Infrastruktur (Supabase, Vercel, Monitoring, Twilio-Grundlast) | 150 € | [A] |
| IHK, Bank, Domains, Sonstiges | 100 € | [A] |
| **Summe** | **1.880 €** | |

**Im Modell angesetzt:** M1–6 **1.800 €**, M7–12 **2.200 €**, M13–18 **3.000 €**,
M19–24 **3.800 €**, ab M25 **4.200 €**, zzgl. **150 €/Kopf** ab dem 4. Mitarbeiter (Arbeitsplatz, Lizenzen).

### 1.3 Personalkosten (Arbeitgeber-Vollkosten)

Lohnnebenkosten 2026: **21–25 %** des Bruttogehalts [F]. Angesetzt: **+23 %**.

| Rolle | Brutto p. a. | Vollkosten/Monat | Kennung |
|---|---|---|---|
| Nico als GF (bewusst niedrig, A2) | 36.000 € | **3.700 €** | [A] – erst ab Monat 13 |
| Ops / Customer Success (angelernt) | 38.000 € | **3.900 €** | [S] |
| Vertrieb (Fixum + Provision) | 45.000 € + Prov. | **5.500 €** | [S] aus [F] SDR-Median DE 53.100 €/Jahr |
| Entwicklung (Freelance Teilzeit → Vollzeit) | – | **2.500 → 7.000 €** | [A] |

**Einstellungsregel im Modell (umsatzgetriggert, nicht plangetrieben):**

| Auslöser (MRR) | Neue Rolle |
|---|---|
| ab Monat 4 | Entwicklung Teilzeit (2.500 €) |
| 8.000 € | Ops #1 |
| 15.000 € | Vertrieb #1 |
| 25.000 € | Ops #2 · Entwicklung auf Vollzeit (7.000 €) |
| 35.000 € | Vertrieb #2 |
| 45.000 / 70.000 / 100.000 / 140.000 / 180.000 € | Ops #3–#7 |
| 60.000 / 90.000 / 120.000 / 160.000 / 200.000 € | Vertrieb #3–#7 |

### 1.4 Vertriebskosten – warum ich CAC zweifach ausweise

Der geladene CAC (`cac_loaded` in den Annahmetabellen) ist die **Benchmark-Größe** für
Payback und LTV/CAC. Im Cashflow buche ich dagegen **getrennt**:

- **Vertriebspersonal** als Fixkostenblock (siehe 1.3), sobald die MRR-Schwelle erreicht ist
- **direkte Akquiseausgaben je Neukunde** (Leadlisten, Messen, Fahrten, Pilotrabatte, Ads) als variable Kosten

Sonst wäre die Vertriebsperson doppelt gebucht. **Folge:** In Jahr 1 verkauft Nico selbst –
der *bare* CAC ist dann nur die direkte Akquiseausgabe (350–1.200 €), der *geladene* CAC
(700–6.000 €) enthält den kalkulatorischen Wert von Nicos Zeit. Beide Zahlen stehen in jeder
Annahmetabelle. Der geladene CAC ist die ehrlichere Zahl für Payback-Betrachtungen, der bare
CAC die ehrlichere für den Kapitalbedarf.

**Benchmark zur Kalibrierung** [F, DACH-B2B-SaaS 2026]: CAC-Payback 12–18 Monate
(US-Vergleich 8–12), Bruttomarge 75–82 %, Brutto-Churn 5–8 % p. a. im Mittelstandssegment,
NRR 105–115 %, durchschnittlicher B2B-Kaufzyklus 4,6 Monate.
CAC-Bandbreite Small/Mid-Market B2B-SaaS 300–5.000 USD.

**Anmerkung zur Kalibrierung meiner Churn-Annahmen:** Ich rechne durchgehend *deutlich
schlechter* als der DACH-Benchmark – 12 % bis 60 % p. a. statt 5–8 %. Begründung: Der
Benchmark misst etablierte Anbieter mit Referenzen und Produktreife. Ein Erstanbieter ohne
Referenzkunden verliert die ersten Kohorten überproportional.

### 1.5 Definition der Kapitalgrößen

| Größe | Formel | Bedeutung |
|---|---|---|
| **Tiefpunkt** | Minimum des kumulierten Cashflows (inkl. Einmalkosten in Monat 0) | absolute Kapitaluntergrenze bei **exakter** Planerfüllung |
| **Kapitalbedarf (Planungsgröße)** | \|Tiefpunkt\| + 3 Monatsfixkosten im Tiefpunktmonat + 0,5 Monatsumsatz Working Capital | die Zahl, mit der man plant |
| **Kapitalbedarf bis 100 k €/Monat** | wie oben, Tiefpunkt und WC bezogen auf den Monat des 100-k-Durchbruchs | Wachstumsfinanzierung |

Working Capital 0,5 Monatsumsatz: Abo-Rechnungen werden überwiegend vorschüssig gestellt,
Setup- und Durchleitungspositionen laufen mit 30 Tagen Zahlungsziel [A].

### 1.6 Finanzierungsrahmen unter A1 + A10

| Quelle | Betrag | Kennung |
|---|---|---|
| Eigenkapital laut A1 | 20.000–60.000 € | [A] |
| KfW ERP-Gründerkredit StartGeld (067) | bis **200.000 €** gesamt, davon max. **80.000 € Betriebsmittel**; seit 01.12.2025 angehoben von 125.000/50.000 €; 10 Jahre Laufzeit, 2 tilgungsfrei, KfW übernimmt 80 % des Ausfallrisikos | [F] KfW |
| **Praktische Obergrenze für ein Software-/Servicemodell** | **≈ 140.000 €** (60 k EK + 80 k Betriebsmittel) | [S] |

Das ist die entscheidende Nebenbedingung: Anlaufverluste eines Software-/Servicemodells sind
fast vollständig **Betriebsmittel**, nicht Investitionen. Die 200.000-€-Schlagzeile des
StartGeld hilft nur einem Modell mit echtem Investitionsanteil (S03 Hardware) – und ausgerechnet
dort reicht sie hinten und vorne nicht.

**Jedes Modell mit einem Kapitalbedarf über 140.000 € verletzt entweder A1 oder A10.**

---

## 2. S01 – Betreiberpflichten-Manager für Mittelstandsstandorte

### 2.1 Annahmetabelle

| Annahme | konservativ | realistisch | ambitioniert | Kennung / Herleitung |
|---|---|---|---|---|
| Plattform-/Koordinationsgebühr je Standort/Monat | 500 € | 800 € | 1.200 € | [S] aus [F-Band] 5.000–30.000 €/Standort/Jahr, davon Koordinationsanteil |
| Setup-Gebühr (Kataster-Erstaufnahme) | 2.500 € | 4.000 € | 6.000 € | [A] |
| Durchleitungsvolumen (eingekaufte Prüfleistung) je Kunde/Monat | 800 € | 1.500 € | 2.500 € | [A] |
| Anteil Kunden, die Beschaffung abgeben | 25 % | 40 % | 60 % | [A] |
| Aufschlag auf Durchleitung | 15 % | 18 % | 20 % | [S] – Koordinationsaufschlag, keine Servicemarge |
| **ARPU (Tenure ≥ 4 Mon.)** | **700 €** | **1.400 €** | **2.700 €** | [S] |
| Churn/Monat | 1,5 % (16,6 % p. a.) | 1,0 % (11,4 % p. a.) | 0,7 % (8,1 % p. a.) | [A] – gesetzliche Wiederkehr senkt Churn (Befund 3 der Shortlist) |
| CAC (voll geladen) | 6.000 € | 5.000 € | 4.500 € | [A] – Multi-Stakeholder-Verkauf an GF + Technische Leitung |
| direkte Akquiseausgabe je Neukunde (bar) | 1.200 € | 1.200 € | 1.200 € | [A] |
| Vertriebszyklus | 6 Monate | 5 Monate | 4 Monate | [A]; [F]-Benchmark B2B 4,6 Monate |
| Conversion (qualifizierter Erstkontakt → Vertrag) | 3 % | 5 % | 7 % | [A] |
| Onboardingdauer | 8 Wochen | 6 Wochen | 5 Wochen | [A] |
| Onboardingkosten je Kunde (bar) | 1.800 € | 1.800 € | 1.800 € | [S] – ca. 25 h Kataster-Erstaufnahme |
| variable Kosten je Kunde/Monat (Software, Betreuung, Katasterpflege) | 120 € | 130 € | 140 € | [A] |
| Einmalkosten Monat 0 | 42.500 € | 36.000 € | 30.000 € | siehe 2.2 |

### 2.2 Einmalkosten Monat 0 (realistisch: 36.000 €)

| Position | Betrag | Kennung |
|---|---|---|
| GmbH-Gründung (Notar, HR, Beratung) | 1.500 € | [S] |
| Marke, Website, CI | 3.000 € | [A] |
| juristisches Vertragswerk Delegation (Schriftform, Eignungsprüfung, Gegenzeichnung – belegt formalisiert [F]) | 6.000 € | [A] |
| MVP Kataster + Fristenkalender + Portal (extern zugekauft) | 21.500 € | [A] |
| Aufbau Partnernetz (Rahmenverträge, Qualifikationsprüfung) | 4.000 € | [A] |

Nicht enthalten: Stammkapital 25.000 € (gebundenes Arbeitskapital, kein Aufwand).

### 2.3 Unit Economics

| Kennzahl | konservativ | realistisch | ambitioniert |
|---|---|---|---|
| Umsatz je Kunde/Monat | 700 € | 1.400 € | 2.700 € |
| variable Kosten je Kunde/Monat | 290 € | 622 € | 1.340 € |
| **Deckungsbeitrag je Kunde/Monat** | **410 €** | **778 €** | **1.360 €** |
| **Bruttomarge** | **58,6 %** | **55,6 %** | **50,4 %** |
| CAC-Payback (geladener CAC) | 14,6 Monate | 6,4 Monate | 3,3 Monate |
| LTV (DB/Churn) | 27.333 € | 77.800 € | 194.286 € |
| LTV/CAC | 4,6 | 15,6 | 43,2 |

**Der wichtigste Befund zu S01 – die Mischmarge täuscht:**

| Erlösstrom (realistisch) | Umsatz | DB | Marge |
|---|---|---|---|
| Plattform / Koordination | 800 € | 670 € | **83,8 %** |
| Durchgeleitete Prüfleistung | 600 € | 108 € | **18,0 %** |
| **Mischung** | **1.400 €** | **778 €** | **55,6 %** |

Die 70–85 % Koordinationsmarge aus der Shortlist ist **korrekt – aber nur für die
Koordinationsschicht.** Sobald man Prüfleistungen im eigenen Namen weiterberechnet, sinkt die
ausgewiesene Bruttomarge unter das Pflichtkriterium 2 (≥ 65 %) und in Richtung der
K.-o.-5-Schwelle (45 %). Das ist kein Rechenfehler, sondern eine **Strukturentscheidung**:

- **Variante A (Netto/Vermittlung):** Der Prüfdienstleister stellt dem Kunden direkt Rechnung, S01 berechnet nur die Koordination. Bruttomarge **84 %**, Umsatz je Kunde 800 €, aber **75 Kunden für 60.000 € MRR**.
- **Variante B (Brutto/Generalunternehmer):** S01 kauft ein und berechnet weiter. Bruttomarge **56 %**, Umsatz je Kunde 1.400 €, **43 Kunden für 60.000 € MRR** – aber Erfüllungshaftung für die eingekaufte Leistung und höherer Working-Capital-Bedarf.

**Empfehlung:** Variante A für die Bewertung ansetzen, Variante B nur bei Kunden, die die
Bündelrechnung ausdrücklich verlangen. Ich habe im Modell die gemischte Form gerechnet
(konservativer als A bei der Marge, konservativer als B beim Umsatz).

### 2.4 12- und 24-Monats-Modell (realistisch)

| Monat | Neu | Kunden | MRR | Umsatz | Fixkosten | Personal | Var. Kosten | Ergebnis v. St. | Kum. CF | Köpfe |
|---|---|---|---|---|---|---|---|---|---|---|
| 0 | – | 0 | 0 | 0 | – | – | 36.000 | −36.000 | −36.000 | 1 |
| 1 | 0 | 0 | 0 | 0 | 1.800 | 0 | 0 | −1.800 | −37.800 | 1 |
| 2 | 0 | 0 | 0 | 0 | 1.800 | 0 | 0 | −1.800 | −39.600 | 1 |
| 3 | 0 | 0 | 0 | 0 | 1.800 | 0 | 0 | −1.800 | −41.400 | 1 |
| 4 | 0 | 0 | 0 | 0 | 1.800 | 2.500 | 0 | −4.300 | −45.700 | 2 |
| 5 | 1 | 1 | 800 | 4.800 | 1.800 | 2.500 | 3.130 | −2.630 | −48.330 | 2 |
| 6 | 1 | 2 | 1.592 | 5.592 | 1.800 | 2.500 | 3.259 | −1.967 | −50.297 | 2 |
| 7 | 1 | 3 | 2.376 | 6.376 | 2.200 | 2.500 | 3.386 | −1.710 | −52.007 | 2 |
| 8 | 1 | 4 | 3.734 | 7.734 | 2.200 | 2.500 | 3.990 | −955 | −52.962 | 2 |
| 9 | 1 | 5 | 5.079 | 9.079 | 2.200 | 2.500 | 4.587 | −208 | −53.170 | 2 |
| 10 | 2 | 7 | 7.211 | 15.211 | 2.200 | 2.500 | 8.309 | +2.202 | −50.968 | 2 |
| 11 | 2 | 9 | 9.321 | 17.321 | 2.200 | 6.400 | 9.023 | −302 | −51.270 | 3 |
| **12** | 2 | **11** | **11.410** | **19.410** | 2.200 | 6.400 | 9.730 | **+1.080** | **−50.190** | 3 |
| 15 | 2 | 16 | 19.281 | 27.281 | 3.150 | 15.600 | 13.227 | −4.696 | −62.973 | 4 |
| 18 | 3 | 25 | 29.295 | 41.295 | 3.300 | 24.000 | 20.007 | −6.012 | −78.651 | 5 |
| 21 | 4 | 34 | 41.541 | 57.541 | 4.250 | 29.500 | 28.222 | −4.431 | −95.952 | 6 |
| **24** | 4 | **45** | **55.581** | **71.581** | 4.400 | 33.400 | 34.016 | **−235** | **−104.953** | 7 |

Quartalssummen und alle Monate für alle drei Szenarien: `10_finanzmodelle.csv`.

### 2.5 Zusammenfassung S01

| Kennzahl | konservativ | realistisch | ambitioniert |
|---|---|---|---|
| Break-even (dauerhaft positives Monatsergebnis) | **Monat 54** | **Monat 26** | Monat 4 |
| Kumulierter Cashflow > 0 | nie (in 72 Mon.) | Monat 35 | Monat 9 |
| Tiefpunkt kum. Cashflow | −403.527 € | **−105.134 €** | −35.400 € |
| **Kapitalbedarf (Planungsgröße)** | **596.253 €** | **279.761 €** | **40.800 €** |
| Kapitalbedarf bis 100 k €/Monat | 597.608 € | 290.007 € | 91.495 € |
| Gewinn v. St. Monat 12 | −2.919 € | **+1.080 €** | +7.058 € |
| Gewinn v. St. Monat 24 | −7.902 € | **−235 €** | +37.981 € |
| MRR Monat 24 | 21.128 € | 55.581 € | 167.536 € |
| 100.000 € Monatsumsatz erreicht | Monat 51 | **Monat 28** | Monat 16 |
| 190.000 € Monatsumsatz erreicht | Monat 93 | Monat 39 | Monat 24 |
| **EBT ≥ 59.217 € (= 30 k netto)** | **nie** | **Monat 47** | Monat 27 |
| Personal Monat 12 / 24 | 2 / 4 | 3 / 7 | 6 / 14 |
| **A1-Test (20–60 k €)** | 🔴 **NICHT FINANZIERBAR** | 🔴 **NICHT FINANZIERBAR** | 🟡 grenzwertig finanzierbar (40.800 €) |

**Personalbedarf im Zeitverlauf (realistisch):** M1–3 nur Nico · M4 Entwickler (Teilzeit)
· M11 Ops #1 · M14 Vertrieb #1 · M17 Ops #2 + Entwickler Vollzeit · M20 Vertrieb #2
· M22 Ops #3 · M28 Vertrieb #3.

---

## 3. S02 – Terminierungs-Abo für Prüf- und Wartungsdienstleister

### 3.1 Annahmetabelle

| Annahme | konservativ | realistisch | ambitioniert | Kennung / Herleitung |
|---|---|---|---|---|
| Plattformgebühr/Monat | 249 € | 399 € | 599 € | [A] |
| bestätigte Termine je Kunde/Monat | 20 | 43 | 70 | [S]: 400 / 800 / 1.300 Bestandskunden × 60–65 % Terminierungsquote ÷ 12 |
| Preis je bestätigtem Termin | 9 € | 10 € | 11 € | [S] gegen [A]-Benchmark menschliche Terminierung 15–35 €/Termin |
| **ARPU** | **429 €** | **829 €** | **1.369 €** | [S] |
| variable Kosten je bestätigtem Termin | 2,00 € | 2,00 € | 1,80 € | [S] – siehe 3.2 |
| Setup-Gebühr | 1.500 € | 2.500 € | 3.500 € | [A] |
| Churn/Monat | 2,5 % (26,2 % p. a.) | 1,8 % (19,6 % p. a.) | 1,2 % (13,5 % p. a.) | [A] – höher als S01: Burggraben dünn, Pay-per-Outcome jederzeit abschaltbar |
| CAC (voll geladen) | 2.500 € | 2.000 € | 1.500 € | [A] – Inhaber-geführter Mittelstand, telefonisch erreichbar |
| direkte Akquiseausgabe je Neukunde (bar) | 700 € | 700 € | 700 € | [A] |
| Vertriebszyklus | 3 Monate | 2 Monate | 1,5 Monate | [A] |
| Conversion | 6 % | 9 % | 12 % | [A] |
| Onboardingdauer | 4 Wochen | 3 Wochen | 2 Wochen | [A] – Engpass ist die ERP-Datenintegration, nicht die Schulung |
| Onboardingkosten je Kunde (bar) | 2.000 € | 2.000 € | 2.000 € | [S] – Integration in Certado/Vemas/Fremdsysteme |
| Plattform-Grundkosten je Kunde/Monat | 40 € | 45 € | 50 € | [A] |
| Einmalkosten Monat 0 | 38.500 € | 30.000 € | 24.000 € | siehe 3.3 |

### 3.2 Herleitung der variablen Kosten je Termin (der Kern der Marge)

| Schritt | Wert | Kennung |
|---|---|---|
| KI-Voice-Vollkosten | 0,10–0,12 €/Min | [S] aus [F] Vapi/Retell 0,10–0,31 USD/Min all-in, fonio Überminuten 0,12–0,15 €/Min |
| Kontaktversuche je bestätigtem Termin | 5 | [A] |
| Gesprächsdauer je Versuch | 1,5 Min | [A] |
| Rohkosten Telefonie | 7,5 Min × 0,11 € = **0,83 €** | [S] |
| menschliche Nachbearbeitung bei 15 % der Fälle (2 Min à 25 €/h) | 0,12 € | [S] |
| Puffer Rufnummer, Trunk, Fehlversuche, Support | 1,05 € | [A] |
| **Summe** | **2,00 €** | [S] |

**Bruttomarge auf den Terminanteil: 80 %.** Zum Vergleich der Arbitrage-Beleg aus der
Wettbewerbsanalyse: menschlicher Telefonservice DACH 0,49–1,70 € je Minute bzw. Anruf [F],
ebuero 1,04–1,39 €/Min [F] → **Faktor 9–13** Kostenvorteil [S]. Selbst bei einer Verdreifachung
meiner Kostenannahme (6,00 €/Termin) bleibt der Terminpreis von 10 € auskömmlich.

### 3.3 Einmalkosten Monat 0 (realistisch: 30.000 €)

| Position | Betrag | Kennung |
|---|---|---|
| GmbH-Gründung, Marke, Website | 4.500 € | [S] |
| **UWG-§-7- und DSGVO-Gutachten (Pflicht vor dem ersten Euro)** | 6.000 € | [A] – die Shortlist nennt das ausdrücklich als Bedingung |
| Plattform-Ausbau auf CallSuite-Basis (Twilio produktiv, `cs_listen`, `cs_arbeitszeit` vorhanden [F]) | 11.500 € | [A] |
| Schnittstellen zu Fremd-ERP (Certado, Vemas, generischer CSV/API-Ingest) | 8.000 € | [A] |

**Der Asset-Vorteil ist hier bezifferbar:** Ohne den bestehenden Twilio-/Supabase-Stack läge der
Plattform-Ausbau bei geschätzt 30.000–40.000 € [A]. Der Vorsprung beträgt also
**ca. 20.000–28.000 € Einmalkosten und 3–4 Monate Zeit** [S] – exakt die beiden Kategorien,
für die Methodik-Regel 8 einen Bonus zulässt.

### 3.4 Unit Economics

| Kennzahl | konservativ | realistisch | ambitioniert |
|---|---|---|---|
| Umsatz je Kunde/Monat | 429 € | 829 € | 1.369 € |
| variable Kosten je Kunde/Monat | 80 € | 131 € | 176 € |
| **Deckungsbeitrag je Kunde/Monat** | **349 €** | **698 €** | **1.193 €** |
| **Bruttomarge** | **81,4 %** | **84,2 %** | **87,1 %** |
| CAC-Payback | 7,2 Monate | **2,9 Monate** | 1,3 Monate |
| LTV | 13.960 € | 38.778 € | 99.417 € |
| LTV/CAC | 5,6 | 19,4 | 66,3 |

**S02 hat die beste Bruttomarge der fünf Modelle** – und als einziges eine, die im
*konservativen* Szenario noch über dem Pflichtkriterium 2 (≥ 65 %) liegt.

### 3.5 12- und 24-Monats-Modell (realistisch)

| Monat | Neu | Kunden | MRR | Umsatz | Fixkosten | Personal | Var. Kosten | Ergebnis v. St. | Kum. CF | Köpfe |
|---|---|---|---|---|---|---|---|---|---|---|
| 0 | – | 0 | 0 | 0 | – | – | 30.000 | −30.000 | −30.000 | 1 |
| 1–2 | 0 | 0 | 0 | 0 | 1.800 | 0 | 0 | −1.800 | −33.600 | 1 |
| 3 | 2 | 2 | 1.658 | 6.658 | 1.800 | 0 | 5.662 | −804 | −34.404 | 1 |
| 4 | 2 | 4 | 3.286 | 8.286 | 1.800 | 2.500 | 5.919 | −1.933 | −36.337 | 2 |
| 5 | 2 | 6 | 4.885 | 9.885 | 1.800 | 2.500 | 6.172 | −587 | −36.924 | 2 |
| 6 | 2 | 8 | 6.455 | 11.455 | 1.800 | 2.500 | 6.420 | **+735** | −36.189 | 2 |
| 7 | 2 | 10 | 7.997 | 12.997 | 2.200 | 2.500 | 6.664 | +1.633 | −34.556 | 2 |
| 8 | 2 | 11 | 9.511 | 14.511 | 2.200 | 6.400 | 6.903 | −992 | −35.548 | 3 |
| 9 | 3 | 14 | 11.827 | 19.327 | 2.200 | 6.400 | 9.969 | +758 | −34.790 | 3 |
| 10 | 3 | 17 | 14.101 | 21.601 | 2.200 | 6.400 | 10.328 | +2.673 | −32.117 | 3 |
| 11 | 3 | 20 | 16.334 | 23.834 | 2.350 | 11.900 | 10.681 | −1.097 | −33.214 | 4 |
| **12** | 3 | **22** | **18.527** | **26.027** | 2.350 | 11.900 | 11.028 | **+749** | **−32.465** | 4 |
| 15 | 3 | 30 | 24.872 | 32.372 | 3.150 | 15.600 | 12.030 | +1.592 | −32.968 | 4 |
| 18 | 4 | 40 | 33.323 | 43.323 | 3.300 | 24.000 | 16.066 | −43 | −40.125 | 5 |
| 21 | 4 | 50 | 41.326 | 51.326 | 4.250 | 29.500 | 17.330 | +245 | −46.046 | 6 |
| **24** | 4 | **59** | **48.904** | **58.904** | 4.400 | 33.400 | 18.528 | **+2.576** | **−40.571** | 7 |

### 3.6 Zusammenfassung S02

| Kennzahl | konservativ | realistisch | ambitioniert |
|---|---|---|---|
| Break-even (dauerhaft) | **nie** | **Monat 21** | Monat 3 |
| Kumulierter Cashflow > 0 | nie | Monat 29 | Monat 9 |
| Tiefpunkt kum. Cashflow | −417.366 € | **−46.291 €** | −27.600 € |
| **Kapitalbedarf (Planungsgröße)** | **562.571 €** | **171.895 €** | **33.000 €** |
| Kapitalbedarf bis 100 k €/Monat | – (nie erreicht) | 198.381 € | 86.328 € |
| Gewinn v. St. Monat 12 | −3.234 € | **+749 €** | +17.065 € |
| Gewinn v. St. Monat 24 | −10.138 € | **+2.576 €** | +67.771 € |
| MRR Monat 24 | 15.995 € | 48.904 € | 148.113 € |
| 100.000 € Monatsumsatz | nie | Monat 34 | Monat 16 |
| 190.000 € Monatsumsatz | nie | Monat 54 | Monat 25 |
| **EBT ≥ 59.217 €** | **nie** | **Monat 50** | Monat 23 |
| Personal Monat 12 / 24 | 2 / 4 | 4 / 7 | 7 / 13 |
| **A1-Test** | 🔴 **NICHT FINANZIERBAR** | 🟡 Tiefpunkt 46.291 € **liegt in A1**, Planungsgröße nicht | 🟢 **finanzierbar** (33.000 €) |

**Der bemerkenswerte Befund:** S02 realistisch hat mit **−46.291 €** den zweitniedrigsten
Kapitaltiefpunkt aller fünfzehn Kombinationen – und ist damit das einzige Modell außer S13,
dessen absolute Untergrenze unter A1 liegt. Die Differenz zwischen Tiefpunkt (46 k) und
Planungsgröße (172 k) ist reiner Sicherheitspuffer. **S02 ist das Modell, bei dem die
Kapitalfrage am ehesten lösbar ist.**

**Personalbedarf (realistisch):** M1–3 Nico allein · M4 Entwickler Teilzeit · M8 Ops #1
· M11 Vertrieb #1 · M16 Ops #2 + Entwickler Vollzeit · M19 Vertrieb #2 · M23 Ops #3.

---

## 4. S03 – Sensor-Monitoring als Motor für Wartungs-Mitgliedschaften (SHK)

### 4.1 Die Strukturentscheidung, die über Leben und Tod entscheidet

Die Sensorik kann an den SHK-Betrieb **verkauft** oder an ihn **vermietet** werden.
Das ist keine Preisfrage, sondern die Kapitalfrage des gesamten Modells.

| Variante | Bruttomarge | Break-even | Kapitalbedarf | 100 k €/Monat |
|---|---|---|---|---|
| **Hardware-Verkauf** (189 € VK / 110 € EK, Vorkasse) | 75,2 % | Monat 28 | **438.916 €** | Monat 25 |
| Hardware-Verkauf, EK +30 % (143 €) | 75,2 % | Monat 35 | 736.137 € | Monat 25 |
| **Hardware-Miete** (kein HW-Umsatz, 110 € Vorfinanzierung je Anlage) | 75,2 % | **nie** | **2.039.487 €** | Monat 40 |

**Gegenprobe im Endzustand:** Für 100.000 € MRR aus dem Sensorstrom bräuchte man bei
6 €/Anlage/Monat rund **14.000 Anlagen** [S]. Bei 110 € Einkauf sind das
**1,54 Mio. € Hardware-Vorfinanzierung** [S] – zuzüglich Ausfall und Rückläufer.

> **Die Mietvariante von S03 ist unter A1 und A10 nicht finanzierbar und muss aus der
> Bewertung ausscheiden. Bewertbar ist nur die Verkaufsvariante mit Vorkasse.**
> Damit entfällt zugleich ein Teil des Bindungseffekts (der Betrieb, dem die Hardware gehört,
> kann den Anbieter leichter wechseln) – ein Argument, das an Agent 12 gehört.

Alle folgenden Zahlen betreffen die **Verkaufsvariante**.

### 4.2 Annahmetabelle

| Annahme | konservativ | realistisch | ambitioniert | Kennung / Herleitung |
|---|---|---|---|---|
| Grundgebühr je SHK-Betrieb/Monat | 199 € | 299 € | 399 € | [A] |
| Preis je überwachter Anlage/Monat | 6 € | 6 € | 7 € | [A] |
| Zielzahl Anlagen je Betrieb nach 12 Mon. | 40 | 80 | 150 | [S] aus [F-sek] SmartAC: 20 % Abschlussquote beim Endkunden |
| Rampendauer je Betrieb | 12 Monate | 12 Monate | 12 Monate | [A] |
| **ARPU im Endzustand** | **439 €** | **779 €** | **1.449 €** | [S] · Shortlist-Rechnung „200 Betriebe × 500 €" liegt zwischen kons. und real. |
| Sensor-Kit Verkaufspreis / Einkauf | 199 / 140 € | 189 / 110 € | 179 / 90 € | [S] aus [F-Band] Sensor 40–90 €, Sensorkit 300–900 €/Maschine, onsenso-Startset 432,68 € inkl. 3 J. |
| variable Kosten je Anlage/Monat (SIM, Cloud, Inferenz, Supportanteil) | 1,80 € | 1,60 € | 1,40 € | [S] aus [F] NB-IoT-SIM 0,5–1,5 €/Monat |
| Plattformkosten je Betrieb/Monat | 60 € | 65 € | 70 € | [A] |
| Setup-Gebühr je Betrieb | 1.500 € | 2.500 € | 3.500 € | [A] |
| Churn/Monat | 3,0 % (30,6 % p. a.) | 2,0 % (21,5 % p. a.) | 1,2 % (13,5 % p. a.) | [A] – **Warnung:** die belegten 97 % Retention gelten für **Endkunden** [F-sek], nicht für Betriebe. Der Betrieb, der die Rampe nicht schafft, kündigt. |
| CAC (voll geladen) | 4.000 € | 3.000 € | 2.200 € | [A] – Innungs-/Messevertrieb |
| direkte Akquiseausgabe je Neukunde (bar) | 900 € | 900 € | 900 € | [A] |
| Vertriebszyklus | 4 Monate | 3 Monate | 2 Monate | [A] – der Betrieb muss sein Endkundengeschäft umbauen, nicht nur eine Software einführen |
| Conversion | 4 % | 6 % | 9 % | [A] |
| Onboardingdauer / -kosten (bar) | 6 Wo / 1.800 € | 5 Wo / 1.800 € | 4 Wo / 1.800 € | [A] |
| Einmalkosten Monat 0 | 72.500 € | 55.000 € | 42.500 € | siehe 4.3 |

### 4.3 Einmalkosten Monat 0 (realistisch: 55.000 €)

| Position | Betrag | Kennung |
|---|---|---|
| GmbH-Gründung, Marke, Website | 4.500 € | [S] |
| Firmware, Cloud-Plattform, Betriebs-Dashboard, White-Label-Endkunden-App | 22.000 € | [A] |
| **Hardware-Erstbevorratung** (150 Kits × 110 €) | 16.500 € | [S] |
| CE-/Funk-Konformitätsbewertung Gesamtkit | 8.000 € | [A] – entfällt nur bei reinem Weiterverkauf vollzertifizierter Ware |
| DSGVO-Konstruktion (Endkundeneinwilligung, AV-Vertrag, EU-Hosting) | 4.000 € | [A] |

**Bereits die Einmalkosten im konservativen Szenario (72.500 €) sprengen A1.**
S03 ist das einzige Modell, bei dem das der Fall ist.

### 4.4 Unit Economics (Endzustand, Verkaufsvariante)

| Kennzahl | konservativ | realistisch | ambitioniert |
|---|---|---|---|
| Umsatz je Betrieb/Monat | 439 € | 779 € | 1.449 € |
| variable Kosten je Betrieb/Monat | 132 € | 193 € | 280 € |
| **Deckungsbeitrag je Betrieb/Monat** | **307 €** | **586 €** | **1.169 €** |
| **Bruttomarge** | **69,9 %** | **75,2 %** | **80,7 %** |
| CAC-Payback | 13,0 Monate | 5,1 Monate | 1,9 Monate |
| LTV | 10.233 € | 29.300 € | 97.417 € |
| **LTV/CAC** | **2,6** | 9,8 | 44,3 |

LTV/CAC von **2,6** im konservativen Szenario ist der schlechteste Wert nach S13 und liegt
unter der üblichen Investitionsschwelle von 3,0.

### 4.5 12- und 24-Monats-Modell (realistisch)

| Monat | Neu | Betriebe | MRR | Umsatz | Fixkosten | Personal | Var. Kosten | Ergebnis v. St. | Kum. CF | Köpfe |
|---|---|---|---|---|---|---|---|---|---|---|
| 0 | – | 0 | 0 | 0 | – | – | 55.000 | −55.000 | −55.000 | 1 |
| 1–3 | 0 | 0 | 0 | 0 | 1.800 | 0 | 0 | −1.800 | −60.400 | 1 |
| 4 | 2 | 2 | 3.198 | 8.198 | 1.800 | 2.500 | 7.018 | −3.120 | −63.520 | 2 |
| 6 | 2 | 6 | 9.635 | 14.635 | 1.800 | 6.400 | 10.219 | −3.784 | −68.818 | 3 |
| 8 | 2 | 10 | 16.116 | 21.116 | 2.350 | 11.900 | 13.374 | −6.507 | −77.857 | 4 |
| 10 | 3 | 14 | 24.226 | 31.726 | 2.350 | 11.900 | 19.988 | −2.513 | −85.184 | 4 |
| **12** | 3 | **20** | **33.972** | **41.472** | 2.500 | 20.300 | 24.645 | **−5.973** | **−99.688** | 5 |
| 15 | 3 | 27 | 48.637 | 56.137 | 3.600 | 33.400 | 31.490 | −12.353 | −136.513 | 7 |
| 18 | 4 | 37 | 61.943 | 71.943 | 3.750 | 38.900 | 39.792 | −10.500 | −164.420 | 8 |
| 21 | 4 | 47 | 75.092 | 85.092 | 4.700 | 42.800 | 45.231 | −7.639 | −190.996 | 9 |
| **24** | 4 | **56** | **84.967** | **94.967** | 4.700 | 42.800 | 48.767 | **−1.300** | **−201.202** | 9 |

### 4.6 Zusammenfassung S03

| Kennzahl | konservativ | realistisch | ambitioniert |
|---|---|---|---|
| Break-even (dauerhaft) | **nie** | **Monat 28** | Monat 9 |
| Kumulierter Cashflow > 0 | nie | Monat 42 | Monat 14 |
| Tiefpunkt kum. Cashflow | −919.008 € | **−206.521 €** | −48.018 € |
| **Kapitalbedarf (Planungsgröße)** | **1.106.167 €** | **438.916 €** | **176.444 €** |
| Kapitalbedarf bis 100 k €/Monat | 1.382.633 € | 438.916 € | 196.155 € |
| Gewinn v. St. Monat 12 | −7.440 € | −5.973 € | +13.427 € |
| Gewinn v. St. Monat 24 | −18.282 € | **−1.300 €** | +74.569 € |
| MRR Monat 24 | 29.744 € | 84.967 € | 243.021 € |
| 100.000 € Monatsumsatz | Monat 91 | Monat 25 | Monat 11 |
| **EBT ≥ 59.217 €** | **nie** | **Monat 60** | Monat 22 |
| Personal Monat 12 / 24 | 3 / 5 | 5 / 9 | 10 / 16 |
| **A1-Test** | 🔴 **NICHT FINANZIERBAR** (schon die Einmalkosten) | 🔴 **NICHT FINANZIERBAR** | 🔴 **NICHT FINANZIERBAR** (176.444 €) |

> **S03 ist in allen drei Szenarien nicht unter A1 finanzierbar.** Es ist das einzige Modell,
> für das das gilt. Ursache ist nicht die Marge (75 % ist gut), sondern die Kombination aus
> Hardware-Vorfinanzierung, hohen Einmalkosten (CE, Firmware, Bevorratung), langem
> Vertriebszyklus und der 12-Monats-Rampe je Kunde: Ein gewonnener Betrieb liefert erst nach
> einem Jahr seinen vollen Deckungsbeitrag, verursacht aber CAC und Onboarding sofort.

---

## 5. S04 – Aufschalt- und Leitstellen-Modell (White-Label-Reseller)

### 5.1 Annahmetabelle

| Annahme | konservativ | realistisch | ambitioniert | Kennung / Herleitung |
|---|---|---|---|---|
| Preis je Aufschaltung/Monat | 39 € | 45 € | 49 € | [F] belegtes Band 20–60 €/Monat Standardaufschaltung; Gesamtspanne 19–250 € |
| White-Label-Einkauf je Aufschaltung/Monat | 18 € | 15 € | 12 € | [S] aus Agent 01 Modell 16 („15–20 € Einkauf gegen 35–50 € Verkauf") |
| Portalgebühr je Verwalter/Monat | 99 € | 149 € | 199 € | [A] |
| Objekte je Verwalter nach 12 Mon. | 25 | 40 | 70 | [A] |
| **ARPU im Endzustand** | **1.074 €** | **1.949 €** | **3.629 €** | [S] |
| Einrichtungsgebühr je Objekt (einmalig) | 199 € | 249 € | 299 € | [F] belegtes Band 150–600 € |
| Übertragungsgerät je Objekt (Einkauf) | 120 € | 115 € | 110 € | [A] |
| Plattformkosten je Verwalter/Monat | 40 € | 45 € | 50 € | [A] |
| Churn/Monat (Verwalter) | 1,0 % | 0,7 % (8,1 % p. a.) | 0,4 % (4,7 % p. a.) | [S] – niedrigster Churn im Feld: Dauerschuldverhältnis, Versicherungsauflage, Kunde vergleicht nie [F] |
| CAC (voll geladen) | 3.500 € | 2.800 € | 2.200 € | [A] |
| direkte Akquiseausgabe je Neukunde (bar) | 700 € | 700 € | 700 € | [A] |
| Vertriebszyklus | 5 Monate | 4 Monate | 3 Monate | [A] – Immobilienverwaltung, Gremien |
| Conversion | 5 % | 7 % | 10 % | [A] |
| Onboardingdauer / -kosten (bar) | 4 Wo / 900 € | 3 Wo / 900 € | 2 Wo / 900 € | [A] |
| Einmalkosten Monat 0 | 29.500 € | 25.000 € | 21.000 € | siehe 5.2 |

### 5.2 Einmalkosten Monat 0 (realistisch: 25.000 €)

| Position | Betrag | Kennung |
|---|---|---|
| GmbH-Gründung, Marke, Website | 4.500 € | [S] |
| Selbstservice-Portal (Alarmhistorie, Kontaktketten, Scharfschaltzeiten) | 12.000 € | [A] |
| NSL-Rahmenvertrag, Verträge, § 34a-GewO-Prüfung | 4.000 € | [A] |
| Erstbevorratung Übertragungsgeräte (40 × 115 €) | 4.500 € | [S] |

**S04 hat die niedrigsten Einmalkosten aller fünf Modelle** – es wird nichts entwickelt
außer einem Portal, die Leistung selbst wird eingekauft.

### 5.3 Die Einkaufspreis-Sensitivität – der wunde Punkt von S04

| Einkauf je Aufschaltung | Bruttomarge | DB je Kunde | Break-even | Kapitalbedarf | Ergebnis M24 |
|---|---|---|---|---|---|
| 15 € (Basis realistisch) | **66,9 %** | 1.304 € | Monat 21 | 341.861 € | +6.594 € |
| 19,50 € (+30 %) | **57,7 %** | 1.124 € | Monat 26 | 511.775 € | −176 € |
| 24,00 € (+60 %) | **48,4 %** | 944 € | Monat 30 | 650.962 € | −6.946 € |
| 18 € (konservativ, bei 39 € VK) | **54,4 %** | 584 € | Monat 52 | 839.562 € | −20.397 € |

Das ist die strukturelle Schwäche des Reseller-Modells: **S04 besitzt seinen Wareneinsatz
nicht.** Der Bruttomargenkorridor liegt zwischen 54 % und 76 % – im konservativen Fall unter
Pflichtkriterium 2 (65 %) und nur 9 Prozentpunkte über der K.-o.-5-Schwelle. Eine
Preiserhöhung der Partner-NSL um 60 % würde S04 auf 48 % drücken und damit an die
Ausschlussgrenze. Die belegte Preisspreizung im Markt (19–250 €/Monat bei nahezu identischer
Leistung [F]) zeigt zugleich, dass Preiserhöhungen zum Kunden hin durchsetzbar sind – aber nur
solange der Kunde nicht vergleicht.

**Gegenmaßnahme (nicht modelliert, gehört in den MVP-Plan):** Mengenstaffel mit zwei
NSL-Partnern und Wechselklausel im Rahmenvertrag verhandeln, bevor der erste Kunde da ist.

### 5.4 Unit Economics

| Kennzahl | konservativ | realistisch | ambitioniert |
|---|---|---|---|
| Umsatz je Kunde/Monat | 1.074 € | 1.949 € | 3.629 € |
| variable Kosten je Kunde/Monat | 490 € | 645 € | 890 € |
| **Deckungsbeitrag je Kunde/Monat** | **584 €** | **1.304 €** | **2.739 €** |
| **Bruttomarge** | **54,4 %** | **66,9 %** | **75,5 %** |
| CAC-Payback | 6,0 Monate | **2,1 Monate** | 0,8 Monate |
| LTV | 58.400 € | 186.286 € | 684.750 € |
| **LTV/CAC** | 16,7 | **66,5** | 311,2 |

**S04 hat die mit Abstand besten Unit Economics des Feldes** – Folge des extrem niedrigen
Churns. Ein einmal gewonnener Verwalter mit 40 Objekten trägt über 11 Jahre.

### 5.5 12- und 24-Monats-Modell (realistisch)

| Monat | Neu | Verwalter | Objekte ca. | MRR | Fixkosten | Personal | Var. Kosten | Ergebnis v. St. | Kum. CF | Köpfe |
|---|---|---|---|---|---|---|---|---|---|---|
| 0 | – | 0 | 0 | 0 | – | – | 25.000 | −25.000 | −25.000 | 1 |
| 1–4 | 0 | 0 | 0 | 0 | 1.800 | 0–2.500 | 0 | −1.800/−4.300 | −34.700 | 1–2 |
| 5 | 2 | 2 | 7 | 2.258 | 1.800 | 2.500 | 4.157 | −6.199 | −40.899 | 2 |
| 7 | 2 | 6 | 33 | 7.616 | 2.200 | 2.500 | 6.346 | −3.430 | −49.037 | 2 |
| 9 | 2 | 10 | 77 | 14.071 | 2.200 | 6.400 | 8.896 | −3.425 | −57.931 | 3 |
| 11 | 3 | 15 | 140 | 22.718 | 2.350 | 11.900 | 13.873 | −5.405 | −70.189 | 4 |
| **12** | 3 | **18** | **180** | **28.137** | 2.500 | 20.300 | 15.975 | **−10.638** | **−80.827** | 5 |
| 15 | 3 | 26 | 320 | 46.733 | 3.600 | 33.400 | 23.048 | −13.315 | −119.062 | 7 |
| 18 | 4 | 37 | 490 | 67.251 | 3.750 | 38.900 | 32.155 | −7.554 | −147.545 | 8 |
| 21 | 4 | 48 | 680 | 89.391 | 4.700 | 42.800 | 40.097 | **+1.794** | −156.679 | 9 |
| **24** | 4 | **59** | **880** | **111.673** | 5.000 | 52.200 | 47.879 | **+6.594** | **−147.059** | 11 |

Objektzahl [S] = Summe der Kohorten-Rampen; sie ist die operative Steuergröße, nicht die Kundenzahl.

### 5.6 Zusammenfassung S04

| Kennzahl | konservativ | realistisch | ambitioniert |
|---|---|---|---|
| Break-even (dauerhaft) | **Monat 52** | **Monat 21** | Monat 10 |
| Kumulierter Cashflow > 0 | nie | Monat 32 | Monat 14 |
| Tiefpunkt kum. Cashflow | −565.380 € | **−158.473 €** | −51.080 € |
| **Kapitalbedarf (Planungsgröße)** | **839.562 €** | **341.861 €** | **174.779 €** |
| Kapitalbedarf bis 100 k €/Monat | 839.562 € | 353.177 € | 200.795 € |
| Gewinn v. St. Monat 12 | −4.937 € | −10.638 € | +11.932 € |
| Gewinn v. St. Monat 24 | −20.397 € | **+6.594 €** | +187.900 € |
| MRR Monat 24 | 36.544 € | 111.673 € | 394.487 € |
| 100.000 € Monatsumsatz | Monat 41 | **Monat 23** | Monat 12 |
| 190.000 € Monatsumsatz | Monat 64 | Monat 32 | Monat 16 |
| **EBT ≥ 59.217 €** | Monat 95 | **Monat 36** | Monat 18 |
| Personal Monat 12 / 24 | 2 / 6 | 5 / 11 | 11 / 16 |
| **A1-Test** | 🔴 **NICHT FINANZIERBAR** | 🔴 **NICHT FINANZIERBAR** | 🔴 **NICHT FINANZIERBAR** |

**S04 ist das Modell mit dem schnellsten Weg zu 30.000 € netto (Monat 36 realistisch) – und
zugleich das mit dem zweithöchsten Kapitalbedarf.** Ursache: 100 % MRR ohne Setup-Erlöse
(die Einrichtungsgebühr deckt gerade das Gerät), 12-Monats-Objektrampe je Kunde und ein
Vertriebszyklus von 4 Monaten. S04 verdient hervorragend – aber erst spät, und die Zeit
davor muss finanziert werden.

---

## 6. S13 – Vertikaler Voice-Agent mit Tiefenintegration

### 6.1 Annahmetabelle

| Annahme | konservativ | realistisch | ambitioniert | Kennung / Herleitung |
|---|---|---|---|---|
| MRR je Kunde (inkl. Überminuten) | 303 € | 520 € | 900 € | [S]; [F] DACH-Kernband 69–199 €, Ausreißer bis 499 €; [F-sek] FoxifAI ab 100 €/Monat |
| Setup-Gebühr | 1.500 € | 1.920 € | 2.500 € | [F-sek] FoxifAI 1.920 € Setup – belegt, dass dt. KMU das akzeptieren |
| Minutenvolumen je Kunde/Monat | 800 | 1.200 | 1.800 | [A] |
| Minuten-Einkauf (Vollkosten) | 0,11 € | 0,11 € | 0,10 € | [S] aus [F] Vapi/Retell 0,10–0,31 USD/Min all-in; fonio Überminuten 0,12–0,15 € |
| Supportkosten je Kunde/Monat | 55 € | 45 € | 40 € | [A] – KMU-Support ist der teuerste Posten des Modells |
| Hosting/Rufnummer je Kunde/Monat | 15 € | 15 € | 20 € | [A] |
| **Churn/Monat** | **5,0 % (46 % p. a.)** | **3,5 % (35 % p. a.)** | **2,0 % (21,5 % p. a.)** | [A] – höchster Churn im Feld: monatlich kündbar [F], Telekom-Netzintegration, Placetel 9 €/Monat je KI-Rufnummer [F] |
| CAC (voll geladen) | 1.400 € | 1.000 € | 700 € | [A] – niedrigster CAC des Feldes |
| direkte Akquiseausgabe je Neukunde (bar) | 350 € | 350 € | 350 € | [A] |
| Vertriebszyklus | 1,5 Monate | 1 Monat | 0,75 Monate | [A] |
| Conversion | 8 % | 12 % | 16 % | [A] |
| Onboardingdauer / -kosten (bar) | 2 Wo / 1.300 € | 1,5 Wo / 1.300 € | 1 Wo / 1.300 € | [S] – Prompt-Engineering, ERP-Integration, Testschleifen |
| Einmalkosten Monat 0 | 28.500 € | 24.000 € | 20.000 € | GmbH/Marke 4.500 € + vertikale Integration 16.500 € + Recht (AI-Act-Transparenz, TKG, DSGVO) 3.000 € |

### 6.2 Unit Economics – hier liegt der Befund

| Kennzahl | konservativ | realistisch | ambitioniert |
|---|---|---|---|
| Umsatz je Kunde/Monat | 303 € | 520 € | 900 € |
| variable Kosten je Kunde/Monat | 158 € | 192 € | 240 € |
| **Deckungsbeitrag je Kunde/Monat** | **145 €** | **328 €** | **660 €** |
| **Bruttomarge** | **47,9 %** | **63,1 %** | **73,3 %** |
| CAC-Payback | 9,7 Monate | 3,0 Monate | 1,1 Monate |
| LTV | 2.900 € | 9.371 € | 33.000 € |
| **LTV/CAC** | **2,1** | 9,4 | 47,1 |

> **Die konservative Bruttomarge von S13 liegt bei 47,9 % – 2,9 Prozentpunkte über der
> K.-o.-5-Schwelle von 45 %.** Und sie liegt unter Pflichtkriterium 2 (65 %) sowohl im
> konservativen als auch im realistischen Szenario. Das ist die rechnerische Bestätigung des
> Shortlist-Befunds „fonio verkauft bei Vollausschöpfung unter den eigenen Plattformkosten".
>
> Bei 303 € MRR und 800 Minuten kostet allein die Telefonie 88 €. Der teuerste Posten ist
> aber nicht die KI, sondern der **KMU-Support mit 55 €** – der Posten, der nach Nicos
> Anti-Kriterienliste („täglicher Kundensupport") ohnehin ausgelagert werden müsste, was ihn
> nicht billiger macht.

### 6.3 Die Kundenzahl-Arithmetik – das eigentliche S13-Problem

| Ziel | konservativ (303 €) | realistisch (520 €) | ambitioniert (900 €) |
|---|---|---|---|
| Kunden für 100.000 € MRR | **330** | 192 | 111 |
| Kunden für 190.000 € MRR | **627** | 365 | 211 |
| Neukunden/Monat nur zum **Halten** von 100 k MRR | **16,5** | 6,7 | 2,2 |
| Neukunden/Monat nur zum **Halten** von 190 k MRR | **31,4** | 12,8 | 4,2 |

**Zum Vergleich – dieselbe Rechnung für die anderen Modelle (realistisch):**

| Modell | ARPU | Kunden für 100 k MRR | Ersatzbedarf/Monat | bei Churn +50 % |
|---|---|---|---|---|
| S01 | 1.400 € | 71 | **0,7** | 1,1 |
| S02 | 829 € | 121 | 2,2 | 3,3 |
| S03 | 779 € | 128 | 2,6 | 3,9 |
| **S04** | **1.949 €** | **51** | **0,4** | **0,5** |
| **S13** | **520 €** | **192** | **6,7** | **10,1** |

Das ist Befund 1 der Shortlist („die Preispunkt-Arithmetik entscheidet vor jeder
Produktfrage") in Zahlen. S13 im konservativen Szenario braucht **16,5 Neuabschlüsse pro
Monat**, nur um nicht zu schrumpfen – das entspricht bei 12 % Conversion **138 qualifizierten
Erstgesprächen im Monat, dauerhaft, nur für den Erhalt**. Das ist eine Inside-Sales-Organisation
von 3–4 Köpfen, die keinerlei Wachstum erzeugt.

### 6.4 12- und 24-Monats-Modell (realistisch)

| Monat | Neu | Kunden | MRR | Umsatz | Fixkosten | Personal | Var. Kosten | Ergebnis v. St. | Kum. CF | Köpfe |
|---|---|---|---|---|---|---|---|---|---|---|
| 0 | – | 0 | 0 | 0 | – | – | 24.000 | −24.000 | −24.000 | 1 |
| 1–2 | 0 | 0 | 0 | 0 | 1.800 | 0 | 0 | −1.800 | −27.600 | 1 |
| 3 | 5 | 5 | 2.600 | 12.200 | 1.800 | 0 | 9.210 | **+1.190** | −26.410 | 1 |
| 6 | 5 | 19 | 9.867 | 19.467 | 1.800 | 6.400 | 11.893 | −626 | −24.964 | 3 |
| 9 | 9 | 43 | 22.421 | 39.701 | 2.350 | 11.900 | 23.128 | +2.322 | −20.078 | 4 |
| **12** | 9 | **65** | **33.702** | **50.982** | 2.500 | 20.300 | 27.294 | **+888** | **−24.360** | 5 |
| 15 | 14 | 99 | 51.371 | 78.251 | 3.600 | 33.400 | 42.068 | −817 | −33.641 | 7 |
| 18 | 14 | 129 | 67.248 | 94.128 | 3.750 | 38.900 | 47.930 | +3.548 | −27.124 | 8 |
| 21 | 20 | 174 | 90.552 | 128.952 | 4.850 | 48.300 | 66.434 | +9.367 | −2.073 | 10 |
| **24** | 20 | **214** | **111.493** | **149.893** | 5.000 | 52.200 | 74.167 | **+18.527** | **+44.661** | 11 |

### 6.5 Zusammenfassung S13

| Kennzahl | konservativ | realistisch | ambitioniert |
|---|---|---|---|
| Break-even (dauerhaft) | **nie** | **Monat 16** | Monat 3 |
| Kumulierter Cashflow > 0 | nie | **Monat 22** | Monat 5 |
| Tiefpunkt kum. Cashflow | −659.220 € | **−33.641 €** | −23.600 € |
| **Kapitalbedarf (Planungsgröße)** | **906.256 €** | **183.766 €** | **29.000 €** |
| Kapitalbedarf bis 100 k €/Monat | 906.256 € | 201.488 € | 83.843 € |
| Gewinn v. St. Monat 12 | −3.704 € | **+888 €** | +34.946 € |
| Gewinn v. St. Monat 24 | −16.316 € | **+18.527 €** | +185.317 € |
| MRR Monat 24 | 40.820 € | 111.493 € | 330.091 € |
| 100.000 € Monatsumsatz | Monat 37 | **Monat 19** | Monat 10 |
| **EBT ≥ 59.217 €** | **nie** | **Monat 37** | Monat 15 |
| Kunden Monat 24 | 135 | **214** | 367 |
| Personal Monat 12 / 24 | 3 / 6 | 5 / 11 | 10 / 16 |
| **A1-Test** | 🔴 **NICHT FINANZIERBAR** | 🟡 Tiefpunkt 33.641 € **liegt in A1**, Planungsgröße nicht | 🟢 **finanzierbar** (29.000 €) |

**S13 ist rechnerisch das schnellste und kapitalleichteste Modell – und zugleich das
fragilste.** Es erreicht im realistischen Szenario als einziges einen positiven kumulierten
Cashflow innerhalb von 24 Monaten (Monat 22). Es bricht aber im konservativen Szenario
vollständig zusammen, und der Abstand zwischen „schnellstem Modell" und „totem Modell" ist
nur die Differenz zwischen 3,5 % und 5,0 % Monatschurn bei gleichzeitig 20 % niedrigerem Preis.

**Zusätzlich – und das trifft nur S13:** Es ist das einzige Modell, dessen Kundenzahl in
Monat 24 (214 realistisch, 367 ambitioniert) das Soll-Kriterium 5 („wenige hochwertige Kunden
statt hunderte Kleinkunden") **direkt verletzt**.

---

## 7. Sensitivitätsanalyse

Basis ist jeweils das **realistische** Szenario. Vier Einzelschocks und ein kombinierter Schock.
„CAC +100 %" bedeutet: doppelte direkte Akquiseausgaben **und** doppelte Vertriebsmannschaft für
dieselbe Neukundenzahl. „Vertriebszyklus × 2" bedeutet: Verzögerung um die ursprüngliche
Zykluslänge **und** halbierte Rampengeschwindigkeit.

### 7.1 Vollständige Sensitivitätsmatrix

| Modell | Variante | Break-even | Kum. CF > 0 | Kapitalbedarf | Ergebnis M24 | MRR M24 | 100 k erreicht | LTV/CAC | Payback |
|---|---|---|---|---|---|---|---|---|---|
| **S01** | Basis realistisch | M26 | M35 | 279.761 € | −235 € | 55.581 € | M28 | 15,6 | 6,4 |
| S01 | Churn +50 % | M25 | M36 | 258.944 € | −1.387 € | 53.532 € | M28 | 10,4 | 6,4 |
| S01 | **Preis −20 %** | M39 | M56 | 555.964 € | −10.501 € | 44.465 € | M31 | 10,0 | 10,0 |
| S01 | **CAC +100 %** | **M45** | M59 | **1.063.964 €** | −16.335 € | 55.581 € | M28 | 7,8 | 12,9 |
| S01 | **Zyklus × 2** | **M46** | M63 | 493.727 € | −3.408 € | **13.671 €** | **M48** | 15,6 | 6,4 |
| S01 | alle vier zugleich | **nie** | nie | 1.494.663 € | −10.269 € | 10.658 € | M54 | 3,3 | 20,1 |
| **S02** | Basis realistisch | M21 | M29 | 171.895 € | +2.576 € | 48.904 € | M34 | 19,4 | 2,9 |
| S02 | Churn +50 % | M25 | M31 | 186.209 € | −398 € | 45.372 € | M37 | 12,9 | 2,9 |
| S02 | Preis −20 % | M29 | M43 | 293.775 € | −5.155 € | 39.123 € | M39 | 14,8 | 3,8 |
| S02 | **CAC +100 %** | **M39** | M54 | **617.945 €** | −11.524 € | 48.904 € | M34 | 9,7 | 5,7 |
| S02 | **Zyklus × 2** | M33 | M45 | 240.983 € | −3.067 € | **30.444 €** | **M51** | 19,4 | 2,9 |
| S02 | alle vier zugleich | **nie** | nie | 981.106 € | −11.079 € | 22.831 € | M65 | 4,9 | 7,5 |
| **S03** | Basis realistisch | M28 | M42 | 438.916 € | −1.300 € | 84.967 € | M25 | 9,8 | 5,1 |
| S03 | Churn +50 % | M29 | M45 | 456.404 € | −4.613 € | 79.453 € | M25 | 6,5 | 5,1 |
| S03 | **Preis −20 %** | M44 | **nie** | 866.256 € | −16.244 € | 67.973 € | M29 | 7,2 | 7,0 |
| S03 | **CAC +100 %** | **M53** | **nie** | **1.457.487 €** | −21.850 € | 84.967 € | M25 | 4,9 | 10,2 |
| S03 | Zyklus × 2 | M41 | M64 | 570.194 € | −12.959 € | 47.366 € | M39 | 9,8 | 5,1 |
| S03 | alle vier zugleich | **nie** | nie | **1.938.352 €** | −34.849 € | 35.797 € | M52 | 2,4 | 13,9 |
| **S04** | Basis realistisch | M21 | M32 | 341.861 € | +6.594 € | 111.673 € | M23 | 66,5 | 2,1 |
| S04 | Churn +50 % | M24 | M33 | 386.849 € | +4.466 € | 108.372 € | M23 | 44,4 | 2,1 |
| S04 | Preis −20 % | M30 | M44 | 575.725 € | −6.041 € | 89.338 € | M26 | 46,6 | 3,1 |
| S04 | **CAC +100 %** | **M34** | M46 | **1.048.283 €** | −18.806 € | 111.673 € | M23 | 33,3 | 4,3 |
| S04 | **Zyklus × 2** | M34 | M48 | 450.803 € | −9.411 € | **44.842 €** | **M35** | 66,5 | 2,1 |
| S04 | alle vier zugleich | **nie** | nie | **1.777.660 €** | −31.497 € | 35.082 € | M40 | 15,5 | 6,1 |
| **S13** | Basis realistisch | M16 | M22 | 183.766 € | +18.527 € | 111.493 € | M19 | 9,4 | 3,0 |
| S13 | Churn +50 % | M19 | M23 | 190.372 € | +14.721 € | 99.039 € | M19 | 6,2 | 3,0 |
| S13 | **Preis −20 %** | **M28** | M42 | 471.674 € | −1.752 € | 89.195 € | M21 | 6,4 | 4,5 |
| S13 | **CAC +100 %** | **M32** | M46 | **825.238 €** | −11.073 € | 111.493 € | M19 | 4,7 | 6,1 |
| S13 | Zyklus × 2 | M25 | M37 | 261.229 € | −171 € | 55.803 € | M28 | 9,4 | 3,0 |
| S13 | alle vier zugleich | **nie** | nie | **1.851.229 €** | −27.913 € | 39.581 € | M38 | 2,1 | 8,9 |

### 7.2 Welche Variable tötet welches Modell?

| Modell | tödlichste Variable | Wirkung | zweittödlichste | Warum |
|---|---|---|---|---|
| **S01** | **CAC +100 %** | Break-even M26 → **M45**, Kapitalbedarf ×3,8 auf 1,06 Mio. € | Zyklus × 2 (100 k von M28 auf M48) | S01 hat den höchsten CAC absolut (5.000 €) bei nur 4 Neukunden/Monat in M24. Jeder Euro CAC schlägt mit dem 4-fachen auf den Monatscashflow durch. |
| **S02** | **CAC +100 %** | BE M21 → **M39**, Kapital ×3,6 auf 618 k € | Zyklus × 2 (100 k von M34 auf M51) | Gleiche Mechanik, aber gedämpft durch 84 % Bruttomarge. **S02 ist gegen Churn und Preis am robustesten:** Preis −20 % verschiebt den BE nur um 8 Monate. |
| **S03** | **CAC +100 %** | BE M28 → **M53**, Kapital ×3,3 auf 1,46 Mio. €, **kein kumulierter BE mehr** | **Preis −20 %** (866 k €, kein kum. BE) | S03 ist doppelt exponiert: Hardware-Einstandskosten sind fix und skalieren nicht mit dem Preis. Preis −20 % bei unveränderten 110 € Sensorkosten frisst die halbe Marge. |
| **S04** | **CAC +100 %** | BE M21 → M34, Kapital ×3,1 auf 1,05 Mio. € | **Einkaufspreis der Partner-NSL +60 %** (Marge 67 % → 48 %) | S04 verträgt Churn und Preis besser als jedes andere Modell (LTV/CAC bleibt selbst bei Churn +50 % bei 44). Der wunde Punkt ist die **Fremdabhängigkeit im Wareneinsatz** – die einzige Variable, die S04 aus dem Nichts treffen kann. |
| **S13** | **Preis −20 %** | BE M16 → **M28**, Kapital ×2,6 auf 472 k € | CAC +100 % (825 k €) | Als einziges Modell ist S13 preis- und nicht CAC-getrieben. Grund: Bruttomarge nur 63 %, variable Kosten (Minuten + Support) sind preisunabhängig. **Und genau Preisdruck ist im S13-Markt belegt** – Placetel 9 €/Monat, Telekom-Netzintegration, fonio-Rabattschlacht [F]. Der wahrscheinlichste Schock ist gleichzeitig der tödlichste. |

### 7.3 Drei querliegende Befunde aus der Sensitivität

**1. Churn ist überall der harmloseste der vier Schocks – aber das ist ein Messartefakt, das
man verstehen muss.** Bei +50 % Churn steigt der Kapitalbedarf nirgends um mehr als 13 %, und
bei S01 sinkt er sogar (weniger Kunden = weniger CAC und weniger variable Kosten in der
Verlustphase). Churn wirkt nicht auf den Kapitalbedarf, sondern auf die **Endhöhe**: Er
bestimmt, bei welcher MRR das Wachstum stehenbleibt. Die richtige Churn-Kennzahl ist nicht der
Break-even, sondern der **Deckel** aus Abschnitt 6.3 – und dort ist die Streuung extrem:
S04 könnte bei seinem M24-Vertriebstempo theoretisch bis 1,11 Mio. € MRR wachsen, S03 nur bis
156 k €, S13 bis 297 k € (realistisch) bzw. 121 k € (konservativ).

**2. CAC schlägt in vier von fünf Modellen am härtesten durch, weil der CAC in diesen
Modellen sofort bar wird, der Deckungsbeitrag aber über 2–15 Monate zurückfließt.** Das ist
kein Margenproblem, sondern ein Timing-Problem. Konsequenz für die Umsetzung: **Jeder Euro
Setup-Gebühr, der den CAC im Abschlussmonat kompensiert, ist mehr wert als drei Euro MRR.**
S04 ist das einzige Modell ohne echte Setup-Gebühr (die Einrichtungsgebühr deckt nur das
Gerät) – und hat deshalb den zweithöchsten Kapitalbedarf trotz der besten Unit Economics.

**3. Der kombinierte Schock tötet alle fünf Modelle.** Bei Churn +50 %, Preis −20 %,
CAC +100 % und doppeltem Vertriebszyklus erreicht **kein einziges Modell** einen Break-even
innerhalb von 60 Monaten; der Kapitalbedarf liegt zwischen 981 k € (S02) und 1,94 Mio. € (S03).
Das ist keine akademische Übung: Die vier Schocks sind **korreliert**. Ein Wettbewerber, der
in den Markt eintritt, senkt gleichzeitig den erzielbaren Preis, erhöht den CAC, verlängert
den Zyklus (der Kunde vergleicht jetzt) und erhöht den Churn. **Die relevante Frage an
Agent 12 lautet daher nicht „welcher Schock tritt ein", sondern „wie wahrscheinlich ist der
Markteintritt eines ernsthaften Wettbewerbers je Modell".**

---

## 8. Die Antwort auf die Nordstern-Frage

### 8.1 Die Zielgröße

**30.000 € netto/Monat privat = 59.217 € Gewinn vor Steuern/Monat = 710.600 € p. a.**
(GmbH, Hebesatz 439 % Oldenburg, Vollausschüttung, ohne Kirchensteuer) [S]

### 8.2 Wann erreicht welches Modell dieses Ziel?

| Modell | konservativ | **realistisch** | ambitioniert | Umsatz im Zielmonat (realistisch) |
|---|---|---|---|---|
| **S04 Leitstelle** | Monat 95 | **Monat 36** | Monat 18 | ca. 240.000 €/Monat |
| **S13 Voice-Agent** | **nie** | **Monat 37** | Monat 15 | ca. 262.000 €/Monat |
| **S01 Betreiberpflichten** | **nie** | **Monat 47** | Monat 27 | ca. 273.000 €/Monat |
| **S02 Terminierung** | **nie** | **Monat 50** | Monat 23 | ca. 175.000 €/Monat |
| **S03 Sensor-SHK** | **nie** | **Monat 60** | Monat 22 | ca. 252.000 €/Monat |

### 8.3 Die Antwort in Klartext

**Ja – zwei Modelle erreichen 30.000 € netto privat innerhalb von fünf Jahren, wenn das
realistische Szenario eintritt: S04 (Monat 36) und S13 (Monat 37). Alle fünf schaffen es im
realistischen Szenario innerhalb von 60 Monaten. Kein einziges schafft es im konservativen
Szenario – vier davon nie.**

Damit sind vier Feststellungen unabweisbar:

**1. Das 36-Monats-Ziel aus dem Nordstern ist nur im besten Fall erreichbar.**
Die Zielgröße „30.000 € netto in 36–60 Monaten" ist im *oberen* Teil ihrer eigenen Bandbreite
realistisch (47–60 Monate für S01/S02/S03), im unteren Teil (36 Monate) nur für S04 und S13 –
und nur, wenn nichts schiefgeht.

**2. Die Diskrepanz aus `01_nordstern_und_anforderungen.md` bestätigt sich exakt und wird
sogar noch schärfer.** Der Umsatz im Zielmonat liegt bei allen Modellen zwischen **175.000 und
273.000 €/Monat** – nicht bei 190.000 €, wie die 30-%-EBITDA-Annahme nahelegt. Grund: In den
Modellen, die *vor* Monat 40 dort ankommen, ist die EBITDA-Marge zu diesem Zeitpunkt noch
nicht bei 30 %, sondern bei 20–25 % (S04: 25 %, S13: 21 %). **Das 100.000-€-Ziel ist nicht
nur ein Zwischenziel – es ist knapp die Hälfte des Weges.**

**3. Der Engpass ist nie die Marge, sondern immer die Zeit und das Kapital dazwischen.**
Alle fünf Modelle haben ausreichende Deckungsbeiträge. Vier von fünf haben LTV/CAC über 9 im
realistischen Fall. Was sie scheitern lässt, ist der Zeitraum von 16–28 Monaten bis zum
operativen Break-even, den jemand finanzieren muss.

**4. Der ehrliche Erwartungswert liegt zwischen realistisch und konservativ.**
Nimmt man an, dass die Wahrheit im Mittel zwischen konservativem und realistischem Szenario
liegt – was bei Erstgründungen in einem unbelegten Markt die verteidigbarere Annahme ist –
dann erreicht **keines der fünf Modelle 30.000 € netto in 60 Monaten**. Das muss in der
Endempfehlung stehen.

### 8.4 Was das für die Erwartungssteuerung bedeutet

| Realistisch erreichbar (realistisches Szenario) | Zeitpunkt | Modelle |
|---|---|---|
| erster Euro Umsatz | Monat 3–5 | alle |
| operativer Break-even | Monat 16–28 | alle |
| 100.000 € Monatsumsatz (Zwischenziel Nordstern) | Monat 19–34 | alle |
| **10.000 € netto/Monat privat** (EBT 19.700 €) | **Monat 22–31** | alle |
| **20.000 € netto/Monat privat** (EBT 39.500 €) | Monat 28–45 | alle |
| **30.000 € netto/Monat privat** (EBT 59.200 €) | **Monat 36–60** | alle |

Der Sprung von 10.000 € auf 30.000 € netto dauert länger als der gesamte Weg von null auf
10.000 €. Das ist die wichtigste Erwartung, die zu setzen ist.

---

## 9. Ranking nach Kapitaleffizienz

**Metrik:** Euro Startkapital (Planungsgröße bis Break-even) je Euro MRR in Monat 24.
Niedriger ist besser.

### 9.1 Alle fünfzehn Kombinationen

| Rang | Modell | Szenario | Kapitalbedarf | MRR Monat 24 | **€ Kapital je € MRR** |
|---|---|---|---|---|---|
| 1 | **S13** | ambitioniert | 29.000 € | 330.091 € | **0,09** |
| 2 | **S02** | ambitioniert | 33.000 € | 148.113 € | **0,22** |
| 3 | **S01** | ambitioniert | 40.800 € | 167.536 € | **0,24** |
| 4 | S04 | ambitioniert | 174.779 € | 394.487 € | 0,44 |
| 5 | S03 | ambitioniert | 176.444 € | 243.021 € | 0,73 |
| 6 | **S13** | **realistisch** | 183.766 € | 111.493 € | **1,65** |
| 7 | **S04** | **realistisch** | 341.861 € | 111.673 € | **3,06** |
| 8 | **S02** | **realistisch** | 171.895 € | 48.904 € | **3,51** |
| 9 | **S01** | **realistisch** | 279.761 € | 55.581 € | **5,03** |
| 10 | **S03** | **realistisch** | 438.916 € | 84.967 € | **5,17** |
| 11 | S04 | konservativ | 839.562 € | 36.544 € | 22,97 |
| 12 | S13 | konservativ | 906.256 € | 40.820 € | 22,20 |
| 13 | S01 | konservativ | 596.253 € | 21.128 € | 28,22 |
| 14 | S02 | konservativ | 562.571 € | 15.995 € | 35,17 |
| 15 | S03 | konservativ | 1.106.167 € | 29.744 € | 37,19 |

### 9.2 Ranking über alle drei Szenarien (der belastbare Vergleich)

Ein Ranking, das nur ein Szenario ansieht, belohnt Optimismus. Der folgende Vergleich mittelt
über alle drei Szenarien und zieht zusätzlich die absolute Kapitaluntergrenze heran.

| Rang | Modell | Ø € Kapital / € MRR über 3 Szenarien | Tiefpunkt realistisch (absolute Untergrenze) | Einmalkosten realistisch | Urteil |
|---|---|---|---|---|---|
| **1** | **S02 Terminierungs-Abo** | **12,97** | **−46.291 €** ✅ in A1 | 30.000 € | **kapitaleffizientestes Modell** – niedrigster Tiefpunkt bei substanziellem Geschäft, beste Bruttomarge (84 %), robusteste Sensitivität |
| 2 | S13 Voice-Agent | 7,98 (aber Ø verzerrt durch Ausreißer) | **−33.641 €** ✅ in A1 | 24.000 € | niedrigster Tiefpunkt überhaupt, aber konservatives Szenario ist ein Totalausfall (906 k €) |
| 3 | S01 Betreiberpflichten | 11,16 | −105.134 € ❌ | 36.000 € | solide, aber langsam; höchster CAC |
| 4 | S04 Leitstelle | 8,82 | −158.473 € ❌ | 25.000 € | beste Unit Economics des Feldes, aber teuerster Weg dorthin |
| 5 | S03 Sensor-SHK | 14,36 | −206.521 € ❌ | 55.000 € | **kapitalineffizientestes Modell** in jeder Betrachtung |

**Der Ø-Wert ist bewusst mit Vorsicht zu lesen** – er wird von den konservativen Szenarien
dominiert, in denen der Nenner (MRR M24) zusammenbricht. Aussagekräftiger sind die beiden
rechten Spalten. Nach beiden gilt dieselbe Reihenfolge:

> **S02 und S13 sind die einzigen beiden Modelle, deren absolute Kapitaluntergrenze im
> realistischen Szenario innerhalb von A1 (20.000–60.000 €) liegt.**
> **S03 ist in jeder Betrachtung und jedem Szenario das teuerste.**

### 9.3 Kapitalbedarf für Wachstum bis 100.000 €/Monat

| Modell | konservativ | realistisch | ambitioniert |
|---|---|---|---|
| S01 | 597.608 € (M51) | **290.007 € (M28)** | 91.495 € (M16) |
| S02 | nie erreicht | **198.381 € (M34)** | 86.328 € (M16) |
| S03 | 1.382.633 € (M91) | **438.916 € (M25)** | 196.155 € (M11) |
| S04 | 839.562 € (M41) | **353.177 € (M23)** | 200.795 € (M12) |
| S13 | 906.256 € (M37) | **201.488 € (M19)** | 83.843 € (M10) |

Bemerkenswert: Bei S02, S03 und S13 ist der Kapitalbedarf bis 100 k €/Monat **fast identisch**
mit dem Kapitalbedarf bis Break-even. Sobald diese Modelle profitabel sind, finanzieren sie
ihr Wachstum selbst. Bei S01 und S04 klafft eine Lücke – dort ist das Wachstum nach dem
Break-even weiterhin cash-negativ, weil jeder Neukunde CAC und Onboarding vorstreckt, bevor
die 12-Monats-Rampe greift.

---

## 10. A1-Test: Welche Modelle sind unter 20.000–60.000 € Startkapital finanzierbar?

### 10.1 Ampeltabelle

| Modell | Szenario | Einmalkosten M0 | Tiefpunkt (Untergrenze) | Kapitalbedarf (Planung) | A1-Urteil |
|---|---|---|---|---|---|
| S01 | konservativ | 42.500 € | −403.527 € | 596.253 € | 🔴 **NICHT FINANZIERBAR** |
| S01 | realistisch | 36.000 € | −105.134 € | 279.761 € | 🔴 **NICHT FINANZIERBAR** |
| S01 | ambitioniert | 30.000 € | −35.400 € | 40.800 € | 🟢 finanzierbar |
| S02 | konservativ | 38.500 € | −417.366 € | 562.571 € | 🔴 **NICHT FINANZIERBAR** |
| S02 | realistisch | 30.000 € | **−46.291 €** | 171.895 € | 🟡 nur ohne Puffer (Untergrenze in A1) |
| S02 | ambitioniert | 24.000 € | −27.600 € | 33.000 € | 🟢 finanzierbar |
| S03 | konservativ | **72.500 €** | −919.008 € | 1.106.167 € | 🔴 **NICHT FINANZIERBAR** – schon M0 sprengt A1 |
| S03 | realistisch | 55.000 € | −206.521 € | 438.916 € | 🔴 **NICHT FINANZIERBAR** |
| S03 | ambitioniert | 42.500 € | −48.018 € | 176.444 € | 🔴 **NICHT FINANZIERBAR** |
| S03 | *Mietvariante* | 55.000 € | – | **2.039.487 €** | 🔴 **STRUKTURELL NICHT FINANZIERBAR** |
| S04 | konservativ | 29.500 € | −565.380 € | 839.562 € | 🔴 **NICHT FINANZIERBAR** |
| S04 | realistisch | 25.000 € | −158.473 € | 341.861 € | 🔴 **NICHT FINANZIERBAR** |
| S04 | ambitioniert | 21.000 € | −51.080 € | 174.779 € | 🔴 **NICHT FINANZIERBAR** |
| S13 | konservativ | 28.500 € | −659.220 € | 906.256 € | 🔴 **NICHT FINANZIERBAR** |
| S13 | realistisch | 24.000 € | **−33.641 €** | 183.766 € | 🟡 nur ohne Puffer (Untergrenze in A1) |
| S13 | ambitioniert | 20.000 € | −23.600 € | 29.000 € | 🟢 finanzierbar |

**Bilanz: 11 von 16 Kombinationen sind unter A1 nicht finanzierbar. Kein einziges realistisches
Szenario ist es mit Puffer.**

### 10.2 Was A1 tatsächlich reicht – und was nicht

Mit dem erweiterten Rahmen aus 1.6 (**60.000 € Eigenkapital + 80.000 € KfW-Betriebsmittel
≈ 140.000 €** [S]) ergibt sich:

| Modell (realistisch) | Kapitalbedarf | mit KfW gedeckt? |
|---|---|---|
| S13 | 183.766 € | ⚠️ knapp verfehlt (−44 k €) |
| S02 | 171.895 € | ⚠️ knapp verfehlt (−32 k €) |
| S01 | 279.761 € | ❌ nein |
| S04 | 341.861 € | ❌ nein |
| S03 | 438.916 € | ❌ nein |

**S02 und S13 sind mit 32.000 bzw. 44.000 € Nachschärfung erreichbar.** Die drei realistischen
Stellhebel dafür – jeder für sich reicht nicht, in Kombination reichen sie:

| Hebel | Wirkung auf den Kapitalbedarf | Preis |
|---|---|---|
| Setup-Gebühr erhöhen (S02: 2.500 → 4.000 €) | ca. −25.000 € über 24 Monate [S] | schwerer verkäuflich, längerer Zyklus |
| Vertriebstempo in M1–12 halbieren, dafür Break-even früher | −20.000 bis −40.000 € [S] | 100-k-Ziel um 8–12 Monate später |
| Nico-Gehalt bis Monat 24 aussetzen (statt ab M13) | **−44.400 €** [S] (12 × 3.700 €) | verlangt A2 über volle 24 statt 12–24 Monate |
| Onboardingkosten senken (Self-Service-Integration statt Handarbeit) | S02: −1.000 €/Kunde ≈ −35.000 € [S] | Entwicklungsaufwand +8.000 € einmalig |

**Die vierte Zeile ist die wichtigste und die unbequemste:** Der Verzicht auf Nicos Gehalt in
Monat 13–24 ist der einzige Einzelhebel, der die Lücke bei S02 und S13 allein schließt. Er
verschärft aber A2 von „12–24 Monate" auf „24 Monate ohne volle Entnahme" – und das ist eine
Aussage, die der Auftraggeber bestätigen muss, nicht ich.

### 10.3 Was aus dem A1-Befund für die Endempfehlung folgt

1. **S03 ist unter A1/A10 kein Kandidat.** Nicht wegen schwacher Ökonomie – die Marge ist gut –, sondern weil Hardware-Bevorratung, CE-Bewertung und 12-Monats-Rampe eine Kapitalklasse verlangen, die im Auftrag ausgeschlossen ist. Sollte A1 nach oben korrigiert werden (> 200.000 €), ändert sich diese Bewertung.
2. **S04 hat die besten Unit Economics des Feldes und ist trotzdem nur schwer finanzierbar.** Grund ist ausschließlich das Fehlen einer echten Setup-Gebühr. Wird das Erlösmodell um eine **Projektierungs-/Aufschaltpauschale von 500–1.000 € je Kunde (nicht je Objekt)** ergänzt, sinkt der Kapitalbedarf spürbar. Das ist eine Produktentscheidung, keine Marktbedingung – und sie sollte vor jeder Bewertung getroffen werden.
3. **S02 und S13 sind die einzigen unter A1 startbaren Modelle** – S02 wegen der höchsten Bruttomarge und des CallSuite-Assetvorsprungs (20–28 k € und 3–4 Monate [S]), S13 wegen des niedrigsten Kapitaltiefpunkts überhaupt.
4. **S13 ist gleichzeitig das Modell mit dem höchsten Totalausfallrisiko.** Sein konservatives Szenario ist kein gedämpfter, sondern ein vollständiger Fehlschlag: 47,9 % Bruttomarge (knapp über K.-o. 5), LTV/CAC 2,1, kein Break-even. Und der Schock, der es dorthin bringt – Preisverfall –, ist im Markt bereits belegt.

---

## 11. Offene Punkte und Grenzen dieser Analyse

1. **Preise für S01, S02 und S03 sind nicht belegt, sondern abgeleitet.** Für S04 und S13 existieren öffentliche Preisbänder [F]. Für S01 (5.000–30.000 €/Standort/Jahr) und S02 (kein Anbieter existiert) sind alle Preisannahmen [A]/[S]. Die Sensitivität „Preis −20 %" ist damit für S01/S02/S03 kein Stresstest, sondern eine plausible Alternativrealität. **Empfehlung: 20 Preisgespräche vor jedem Produktbau** – für S02 fordert das die Shortlist bereits ausdrücklich.
2. **Die Neukundenzahlen sind exogen gesetzt, nicht aus Vertriebskapazität abgeleitet.** Ich habe sie an der Zykluslänge, der Conversion und Nicos Alleinarbeit in Jahr 1 kalibriert und mit einem Floor „kein Neukunde vor Monat 3" versehen. Sie sind trotzdem die weichste Annahme des Modells.
3. **Die ambitionierten Szenarien sind keine Prognosen.** Sie zeigen, was wahr sein müsste, damit die Modelle unter A1 funktionieren – z. B. dass Nico in S13 ab Monat 3 acht Abschlüsse pro Monat allein erzielt. Sie gehören in die Bewertung als Obergrenze, nicht als Erwartung.
4. **Umsatzsteuer ist durchgehend ausgeklammert** (durchlaufender Posten im B2B). Working-Capital-Effekte aus der USt-Voranmeldung sind im 0,5-Monats-WC-Puffer grob enthalten.
5. **Nicht modelliert:** Forderungsausfälle (bei Handwerks-/Verwalterkundschaft ansetzbar mit 1–2 % des Umsatzes [A]), Wechselkursrisiko bei USD-denominierten KI-Plattformkosten (betrifft S02 und S13), Rechtsstreitkosten.
6. **Der Zusammenhang zwischen Churn und Sättigungs-MRR (Abschnitt 6.3) ist die wichtigste Kennzahl, die in keiner Standard-Break-even-Rechnung auftaucht** – und sie schlägt S13 und S03 deutlicher als jede Kapitalbedarfszahl.

---

## Anhang: Quellen der [F]-Zahlen dieser Analyse

| Zahl | Wert | Quelle |
|---|---|---|
| Gewerbesteuer-Hebesatz Oldenburg | 439 % | IHK-Übersicht Gewerbesteuer-Hebesätze, Stand 06/2025 – ihk.de |
| KSt + SolZ / KapESt + SolZ | 15,825 % / 26,375 % | gesetzlich |
| KfW ERP-Gründerkredit StartGeld (067) | bis 200.000 € (ab 01.12.2025, zuvor 125.000 €), davon max. 80.000 € Betriebsmittel (zuvor 50.000 €); 10 J. Laufzeit, 2 J. tilgungsfrei; KfW trägt 80 % des Ausfallrisikos | kfw.de – Förderprodukt 067 + KfW-Pressemitteilung |
| Lohnnebenkosten Arbeitgeber 2026 | 21–25 % des Bruttos (SV ~21 %, Umlagen/BG 2–4 %) | lohnklar.de, zep.de, sevdesk.de |
| Beitragsbemessungsgrenzen 2026 | 69.750 € (KV/PV), 101.400 € (RV/AV) | lohnklar.de |
| SDR-Gehalt Deutschland | Ø 53.100 €/Jahr; 41.000 € (25. Perz.) bis 71.625 € (75. Perz.) | Glassdoor DE, Stand 01/2026 |
| Steuerberater kleine GmbH | Flatrate 299–449 €/Monat; klassische Kanzlei 580–1.000 €/Monat; Jahresabschluss 1.500–5.000 €/Jahr | onlinebilanz.de, bsteuern.com, norman.finance |
| Betriebs-/Vermögensschadenhaftpflicht IT | Solo-IT-Schutz ab ca. 12 €/Monat; Betriebshaftpflicht-Anteil 100–250 €/Jahr | versicherungsriese.de, betriebshaftpflicht24.de |
| DACH-B2B-SaaS-Benchmarks 2026 | CAC-Payback 12–18 Mon.; Bruttomarge 75–82 %; Brutto-Churn 5–8 % p. a.; NRR 105–115 % | saaswelt.de |
| B2B-Kaufzyklus | Ø 4,6 Monate über sieben Kanäle | gtm8020.com |
| B2B-SaaS-CAC Small/Mid-Market | 300–5.000 USD; Baseline Ø 702 USD | userpilot.com, gtm8020.com |
| Aufschaltgebühr NSL (S04) | 20–60 €/Monat Standard; Gesamtspanne 19–250 €; Einrichtung 150–600 € | Agent 01 Modell 16 / Agent 10 Modell 9 – notrufexperten.de, accsicherheitstechnik.de, Piepenbrock-Preisliste |
| KI-Voice-Vollkosten (S02, S13) | 0,10–0,31 USD/Min all-in (beworben 0,05–0,07); fonio Überminuten 0,12–0,15 €/Min | Agent 03 §1.2/1.3 – cekura.ai, fonio.ai |
| Menschlicher Telefonservice DACH | ebuero 1,04–1,39 €/Min; starbuero 0,49 €/Min; phonea 1,70 €/Anruf | Agent 03 §1.4 |
| DACH-Preisband KI-Telefonassistent | 29–299 €/Monat, Kernband 69–199 € | Agent 03 §1.5 |
| FoxifAI (S13-Referenz) | 1.920 € Setup + ab 100 €/Monat | Agent 02, [F-sek] |
| SmartAC (S03-Referenz) | 20 % Abschlussquote Endkunden; Retention 70 % → 97 %; ~1.000 $/Jahr je Mitgliedschaft | Agent 02 Modell 22, [F-sek] |
| Sensorkosten (S03) | Sensor 40–90 €; Sensorkit 300–900 €/Maschine; onsenso-Startset 432,68 € inkl. 3 J.; NB-IoT-SIM 0,5–1,5 €/Monat | Agent 01 Modelle 11/13/14 |

---

*Ende Agent 07. Datenausgabe: `10_finanzmodelle.csv` – Spalten: Modell; Szenario; Monat;
Kunden; Umsatz; Fixkosten (inkl. Personal); Variable_Kosten (inkl. Onboarding und direkter
Akquiseausgaben); Ergebnis_vor_Steuern; Kumulierter_Cashflow. Monat 0 enthält die Einmalkosten.
Trennzeichen: Semikolon.*
