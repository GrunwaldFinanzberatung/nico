# Agent 05 – Wiederkehrender-Umsatz-Architekt

Stand: 2026-08-05 · Auftrag: Erlösarchitektur für die TOP 8 der Shortlist (S01, S02, S03, S04, S05, S06, S08, S13)
· Grundlage: `01_nordstern_und_anforderungen.md`, `13_shortlist.md`, Rohmaterial Welle 1
· Zusatzrecherche: 8 Web-Suchen (Budget ausgeschöpft), WebFetch in dieser Umgebung blockiert

---

## 0. Gemeinsame Rechengrundlagen (gelten für alle 8 Modelle)

Damit die acht Erlösarchitekturen vergleichbar sind, rechne ich überall mit denselben
Kostensätzen und Vertriebsannahmen. Wer eine Zahl bestreiten will, bestreitet sie hier
einmal statt achtmal.

### 0.1 Personalvollkosten

| Rolle | Bruttogehalt/Jahr [A] | + AG-Anteil 21 % | + Arbeitsplatz/Overhead 15 % | Vollkosten/Jahr | €/produktive Stunde [S] |
|---|---|---|---|---|---|
| Ops / Kundenerfolg | 45.000 € | 54.450 € | 62.600 € | 62.600 € | **35 €** |
| Fachkraft (Technik, Regelwerk, Koordination) | 62.000 € | 75.020 € | 86.300 € | 86.300 € | **48 €** |
| Ingenieur / Vertikal-Engineering | 80.000 € | 96.800 € | 111.300 € | 111.300 € | **62 €** (aufgerundet 65 €) |

Rechenweg Stundensatz: Vollkosten ÷ 12 ÷ 150 produktive Stunden/Monat [A].
Beispiel Ops: 62.600 ÷ 12 = 5.217 €/Monat ÷ 150 h = 34,78 € → **35 €/h** [S].

### 0.2 Definition Bruttomarge in diesem Dokument

Bruttomarge = (Umsatz − direkt kundenbezogene Kosten) ÷ Umsatz.
Direkt kundenbezogen = Hosting/Cloud je Kunde, SIM/Konnektivität, eingekaufte Fremdleistung,
Hardware-Abschreibung (nur bei Miete), laufende Betreuungsstunden, anteilige Fachkraft-Kosten
für Regelwerks-/Formularpflege.
**Nicht** enthalten: Vertrieb, Marketing, Produktentwicklung, Geschäftsführung, Verwaltung.
Diese Abgrenzung ist wichtig, weil Kriterium 2 (≥ 65 %) sich auf die Bruttomarge bezieht,
K.-o. 5 (< 45 %) ebenfalls, und die EBITDA-Marge von 30 % erst nach Abzug der übrigen Blöcke steht.

### 0.3 Vertriebskapazität in 24 Monaten (einheitliches Modell)

Unter Annahme A10 (kein Risikokapital) ist die Vertriebsmannschaft der harte Deckel.
Realistischer Aufbaupfad [A]:

| Zeitraum | Nico als Vertriebs-FTE | Angestellte AE | Summe FTE | FTE-Monate |
|---|---|---|---|---|
| Monat 1–6 | 0,5 | 0 | 0,5 | 3,0 |
| Monat 7–12 | 0,7 | 1 | 1,7 | 10,2 |
| Monat 13–18 | 0,5 | 2 | 2,5 | 15,0 |
| Monat 19–24 | 0,3 | 3 | 3,3 | 19,8 |
| **Summe** | | | | **48,0 FTE-Monate** [S] |

Je Modell nenne ich dann nur noch die Abschlussrate **je Vertriebs-FTE-Monat** [S] und
multipliziere mit 48. Von der Bruttozahl gehen Churn und – wo relevant – Nicht-Aktivierungen ab.
Zusätzliche Bremse in allen Modellen: die zuletzt gewonnenen Kunden tragen ihren vollen MRR
erst nach der Onboarding-Zeit; ich rechne das über einen pauschalen Abschlag mit.

### 0.4 Die Zielarithmetik (aus Befund 1, hier fortgeschrieben)

| Ziel | Bedeutung |
|---|---|
| 10.000 € MRR | Nico kann sich selbst bezahlen, erste Ops-Kraft finanzierbar |
| 30.000 € MRR | Kleines Team, Modell trägt sich |
| 100.000 €/Monat | **Zwischenziel** laut Nordstern |
| 190.000 €/Monat | **Echtes Ziel** – erst hier stehen 30.000 € netto privat |

Die Kundenzahl-Tabellen in diesem Dokument rechnen für 100.000 € und 190.000 €
**Monatsumsatz gesamt**, nicht nur MRR. Wo Setup-/Hardwareumsatz einen relevanten Anteil
stellt, weise ich ihn getrennt aus – sonst entsteht ein geschöntes Bild.

### 0.5 Preisanker, die in dieser Session neu belegt wurden

| Anker | Wert | Quelle |
|---|---|---|
| DGUV-V3-Prüfung ortsveränderliche Betriebsmittel | **3–6 €/Gerät**; Büroauftrag insgesamt 150–350 € | [F] gwi-mbh.de, inventory-one.com, gericks-prueftechnik.de, 2026-08 |
| Heizungswartungsvertrag DE (Endkunde) | **180–350 €/Jahr**; Einzelwartung 80–260 € | [F] badenova.de, energie-experten.org, my-hammer.de, 2026-08 |
| HACCP-Temperaturüberwachung je Messstelle | **4,95 €** (Sencono, inkl. Gerätemiete), **5,00 €** (DIE HACCP APP), **8,00 €** (PSsystec, nur Konnektivität) | [F] sencono.de, diehaccpapp.de, m2mgermany.de, 2026-08 |
| NSL-Einrichtungskosten | **89–150 €** einmalig (Leitstelle), zzgl. Errichterstunden 50–250 € | [F] stadtritter.de, livealarm.de, 2026-08 |
| Aufzugswartung DE | **500–1.500 €/Jahr** je Anlage; inkl. Betriebskosten 2.000–6.000 €/Jahr | [F] guede-aufzugtechnik.com, aszendio.com, 2026-08 |
| Betreiberpflichten-/Prüfsoftware DE | STREIT **145 / 375 / 725 €/Monat**; Wettbewerber 29 €/Named User; KEVOX Basic 83 €/Monat je Lizenz | [F] streit-software.de, kevox.de, 2026-08 |
| B2B-Terminvereinbarung durch Agentur | **150–400 € je qualifiziertem Termin**; interner SDR 80–200 €; 50–80 Anrufe je Termin (Terminquote 2–5 %) | [F] telefonakquise-agentur.de, callin.io, 2026-08 |
| DIN-Normnutzung in Software | Lizenzmodell existiert ausdrücklich, **nur Lesezugriff**, Jahreslizenz, Preis individuell kalkuliert, jährlich angepasst | [F] support.dinmedia.de, dinmedia.de-Preisliste, 2026-08 |
| Heizungs-Fernüberwachung für Fachbetriebe | Bosch **HomeCom Pro** und Vaillant bieten das bereits – **herstellergebunden**, Preise nicht veröffentlicht | [F] bosch/vaillant über energie-fachberater.de, 2026-08 |

Der letzte Eintrag ist ein **Warnbefund für S03** und wird dort behandelt.

---

## S01 — Betreiberpflichten-Manager für Mittelstandsstandorte

### 1. Erlösbausteine einzeln

| Baustein | Preis | Begründung / Anker |
|---|---|---|
| **Setup: Anlagen-Erstaufnahme** | **4.500 €** (bis 25 Anlagen), **7.900 €** (bis 60), **12.000 €** (bis 120) einmalig je Standort [S] | Der Markt für einmaligen Compliance-Aufsatz liegt in DE „ab 3.000 € Initialaufwand" [F, DSB-Segment, A01 Z. 535]. Ein Standort mit 40 prüfpflichtigen Anlagen ist erheblich aufwendiger als ein DSB-Aufsatz. Eigenkosten: 2 Tage Vor-Ort × 8 h × 48 € = 768 € + 12 h Backoffice × 35 € = 420 € + Reise 300 € = **1.488 €** [S] → 67 % Setup-Marge bei 4.500 € |
| **Monatsgrundgebühr je Standort** | **690 €/Monat** (Kataster, Fristenmotor, Portal, Auditakte, bis 25 Anlagen) [S] | Harter Anker: STREIT Premium **725 €/Monat** [F, 2026-08] ist der obere Rand für *reine* Betreiberpflichten-Software. Wir positionieren bei 690 € – nominell unter dem teuersten Softwareprodukt – liefern aber zusätzlich die Beschaffung der Prüfleistung. Das ist die Preisfigur: gleicher Preis, doppelte Leistung |
| **Nutzungsgebühr je Anlage** | **6 €/Anlage/Monat** ab Anlage 26 [S] | Grenzkostennah gestaffelt; bei 60 Anlagen: 690 + 35 × 6 = **900 €/Monat**. Die Staffel zwingt zur vollständigen Katastererfassung statt zur Auswahl der „wichtigen" Anlagen – und genau die Vollständigkeit ist das Produkt |
| **Vermittlungsmarge Prüfleistung** | **18–25 % Aufschlag** auf den Partnerpreis [S] | DGUV V3: 3–6 €/Gerät [F]. Ein Standort mit 800 ortsveränderlichen Geräten = 2.400–4.800 €/Jahr allein hier. Über 8–12 Pflichten hinweg: **12.000–35.000 € Prüfvolumen/Jahr je Standort** [S] × 20 % = 2.400–7.000 €/Jahr = **200–580 €/Monat Marge** |
| **Zusatzmodul Gefahrstoffkataster** | 149 €/Monat [S] | Eigenständige Pflicht (GefStoffV), eigenständiges Datenmodell, deshalb eigenständiger Preis |
| **Zusatzmodul Unterweisungen** | 4,50 €/Mitarbeiter/Monat [S] | Anker: Unterweisungen **ab 25 €/Mitarbeiter** einmalig [F, betriebsarzt.online]. Bei 3 Pflichtunterweisungen/Jahr zahlt der Kunde heute 75 €/MA/Jahr; unser Abo kostet 54 €/MA/Jahr – billiger für ihn, wiederkehrend für uns |
| **Zusatzmodul Fuhrpark (§ 21 StVG)** | 4,90 €/Fahrzeug/Monat [S] | Anker: Vimcar 4,90 €, Mobexo ab 6,90 €, CARMADA ab 19 € Grundgebühr [F, leasingengel.de-Vergleich] |
| **Premium-Support „Audit-Beistand"** | 250 €/Monat [S] | Rufbereitschaft bei BG-/Behördenprüfung, Aufbereitung der Auditakte, Teilnahme per Video. Wird in der Praxis 1–2 × jährlich abgerufen; der Kunde zahlt für Verfügbarkeit |
| **Hardware-Miete** | **keine** – bewusst | Kein Kapitalbedarf, kein Lager, keine Logistik. Befund 2 sagt: nicht selbst erbringen, nicht selbst bauen |
| **Erfolgsanteil** | **keiner** – bewusst | Der Nutzen ist ein *vermiedener* Schaden. Vermiedene Schäden lassen sich nicht abrechnen, weil sie nicht eintreten. Jeder Versuch eines Erfolgshonorars führt in eine Haftungsdiskussion und damit in Richtung K.-o. 9 |

**Ziel-ARPU je Standort:** 690 (Basis) + 210 (Anlagenstaffel Ø) + 250 (Support/Module Ø) = **1.150 €/Monat** [S].
Prüfvolumen-Marge kommt obendrauf, wird aber – siehe unten – **netto** ausgewiesen.

### 2. Preis-Logik: je Standort + je Anlage

Der Preis bemisst sich an **Standort × Anlagenzahl**. Begründung:

- Der **Standort** ist die Haftungseinheit. Betreiberverantwortung nach BetrSichV/ArbSchG/§ 130 OWiG
  hängt am Betreiber der Anlage an einem Ort. Der Kunde denkt in Standorten, weil sein Risiko
  in Standorten organisiert ist. Ein Mehrstandort-Konzern kauft dann *n*-mal dasselbe Produkt –
  Umsatzmultiplikation ohne Vertriebsmultiplikation.
- Die **Anlage** ist der Kostentreiber. Jede zusätzlich erfasste Anlage erzeugt Fristen,
  Beauftragungen, Protokolle, Nachweisprüfung. Die Staffel bildet das ab und hält die Marge
  bei jedem Kundenzuschnitt stabil.
- **Je Nutzer wäre falsch** und ist der Grund, warum die etablierten Anbieter bei 29–83 €
  hängen bleiben [F]. Bei Nutzerpreisen spart der Kunde Nutzer – er lässt Hausmeister und
  Standortleiter draußen, die Datenqualität sinkt, das Produkt versagt. Wir wollen das Gegenteil:
  möglichst viele Beteiligte im System, weil jeder Beteiligte eine Wechselhürde ist.
- **Je Nutzungsvorgang wäre falsch**, weil der Kunde dann Prüfungen aufschiebt, um zu sparen –
  ein Fehlanreiz direkt gegen den Produktzweck.

### 3. Der zentrale Punkt: Was rechtfertigt die Monatsgebühr in Monat 13?

**Antwort: Ja, überzeugend – aus drei belegbaren Quellen.**

**(a) Der Fristenstrom hört nie auf.** Ein Standort mit 60 prüfpflichtigen Anlagen erzeugt
**60–120 Fälligkeiten pro Jahr** [S] (viele Pflichten sind jährlich, einige halbjährlich,
DGUV V3 je nach Gefährdungsbeurteilung 6–48 Monate). In Monat 13 laufen exakt dieselben
Fälligkeiten wie in Monat 1 – nur diesmal ohne dass der Kunde etwas tut. Die Einrichtung war
das Kataster; das Produkt ist der Vollzug.

**(b) Das Kataster von Monat 1 ist in Monat 13 falsch.** Das ist das stärkste Argument und es
wird selten ausgesprochen: Anlagen kommen hinzu, werden stillgelegt, Gebäudeteile werden
umgenutzt, Mitarbeiterzahlen ändern die Pflichtenlage – **und die Vorschriften selbst ändern
sich**. Belegte Beispiele allein aus dem Zeitfenster dieser Recherche: F-Gase-Verordnung
EU 2024/573 mit neuen Betreiberpflichten [F, roter-kaeltetechnik.de], GEG-Heizungsprüfpflicht,
TrinkwV-Novellen. Der Kunde kauft nicht eine Liste – er kauft, dass jemand anderes die
Vorschriftenlage beobachtet und seine Liste danach korrigiert. Eine Software, die er einmalig
kauft, kann das nicht leisten; ein Beratungsprojekt, das er einmalig kauft, auch nicht.

**(c) Lückenlosigkeit ist ein Zustand, kein Ergebnis.** Die Auditakte hat nur dann Wert, wenn
sie *heute* vollständig ist. Ein 13 Monate alter Nachweis ist wertlos. Damit ist die
Zahlungsbereitschaft strukturell dauerhaft.

**Nachweisbarkeit (das ist die Pflicht, nicht die Kür):** monatlicher Compliance-Report
„X von Y Pflichten fristgerecht erfüllt, Z in Bearbeitung, 0 überfällig", Vorher-Nachher der
überfälligen Positionen aus dem Onboarding, Jahresauditreport auf Knopfdruck. Der Kunde kann
die Zahl gegen seine eigene Ordnerablage prüfen. Ohne diesen Report ist die Monatsgebühr in
Monat 13 nicht verteidigbar – **das ist eine Produktanforderung, keine Marketingaufgabe.**

### 4. Kündigungsrisiko: Was passiert am Tag danach?

Am Tag nach der Kündigung besitzt der Kunde: eine exportierte Anlagenliste und einen PDF-Stapel
Nachweise. Er besitzt **nicht**: die Partnerverträge (die liegen bei uns), den Fristenmotor,
die Terminkoordination, die Regelwerksbeobachtung, den Ansprechpartner. Er muss **8–12
Einzelverträge** neu schließen und intern jemanden benennen, der Fristen führt – die Rolle,
die er vor uns nicht besetzt hatte und deshalb bei uns gekauft hat.

**Aber:** Der Schmerz ist **verzögert**. Nichts bricht am nächsten Morgen zusammen. Er merkt es
bei der ersten verpassten Frist – im Schnitt 3–5 Monate später [S], im schlimmsten Fall erst
beim BG-Besuch. Diese Verzögerung ist die Schwäche des Modells: Ein Controller kann die
1.150 €/Monat streichen und erlebt zwei Quartale lang keine Konsequenz.

**Churn [S]: 6–9 %/Jahr.** Rechenweg der Schätzung: Gesetzliche Wiederkehr drückt den Churn
(Befund 3), fehlende Sofortkonsequenz hebt ihn. Vergleichsband: Compliance-SaaS mit
Jahresverträgen im DE-Mittelstand liegt typisch bei 5–12 % Logo-Churn/Jahr [A]. Mit
24-Monats-Erstlaufzeit (marktüblich in diesem Segment [A]) landet man am unteren Rand.
Hauptkündigungsanlässe: Standortschließung, Übernahme durch einen Konzern mit eigenem
FM-Vertrag, Wechsel des technischen Leiters.

### 5. Wechselkosten und Bindung

| Dimension | Stärke | Konkret |
|---|---|---|
| Daten | **hoch** | 2 Jahre Prüfhistorie, Mängelverfolgung, Fotodokumentation mit Zeitstempel. Exportierbar als PDF – aber als PDF unbrauchbar |
| Hardware | keine | bewusster Verzicht, kostet Bindung |
| Verträge | **hoch** | Die Rahmenverträge mit 8–12 Prüfpartnern liegen bei uns, nicht beim Kunden. Er müsste sie alle neu verhandeln, zu schlechteren Konditionen (er ist ein Standort, wir sind ein Bündel) |
| Prozessintegration | **mittel-hoch** | Hausmeister, Standortleiter, Einkauf und externe Prüfer arbeiten im Portal. Jeder Beteiligte ist eine Hürde |
| Historie | **hoch** | Die Beweiskraft der Akte steigt mit ihrer Länge. Eine 3-jährige lückenlose Akte ist im Haftungsfall bares Geld |

### 6. Bruttomarge mit Rechenweg

Basis: ein Standort mit 60 Anlagen, ARPU 1.150 €/Monat.

| Kostenposition je Kunde/Monat | Betrag | Herleitung |
|---|---|---|
| Plattform/Hosting | 12 € | [S] Multi-Tenant-SaaS, Dokumentenspeicher |
| Ops-Betreuung (Beauftragung, Nachverfolgung) | 63 € | 1,8 h × 35 € [S] |
| Regelwerkspflege anteilig | 40 € | 1 Fachkraft 86.300 €/Jahr ÷ 12 = 7.192 € ÷ 180 Kunden = 40 € [S] |
| Partner-Koordination | 19 € | 0,4 h × 48 € [S] |
| Nachweis-Qualitätssicherung | 10,50 € | 0,3 h × 35 € [S] |
| **Summe** | **144,50 €** | |

**Bruttomarge = (1.150 − 144,50) ÷ 1.150 = 87,4 %** [S].
Konservativ mit Ausnahmefällen, Nacharbeit und Partnerausfällen: **78–85 %** [S].

**Zwei kritische Sensitivitäten, die offen benannt werden müssen:**

1. **Die Durchleitungsfalle.** Wenn das Prüfvolumen brutto durch die eigene Rechnung läuft
   (+1.800 €/Monat Volumen bei 20 % Aufschlag), steigt der Umsatz auf 2.950 € und die Kosten um
   1.500 € → **Bruttomarge fällt auf 44,2 %** [S] und verletzt K.-o. 5.
   **Architekturentscheidung: Netto-Ausweis (Agenturmodell).** Der Prüfpartner rechnet direkt
   mit dem Kunden ab, wir stellen die Vermittlungsmarge separat. Kosten: das 190.000-€-Ziel
   wird später erreicht. Nutzen: die Marge bleibt bei 78–87 % und Kriterium 2 ist erfüllt.
2. **Die Handarbeitsfalle.** Die 1,8 h Ops-Betreuung setzen voraus, dass der Fristenmotor zu
   ≥ 95 % Software ist. Ist die Fristenlogik Handarbeit, sind es 8–12 h/Kunde/Monat →
   Kosten 380–500 € → **Bruttomarge 57–67 %** [S], und Nico landet in genau der Tätigkeit,
   die auf seiner Anti-Liste steht. Das ist die Frage, die Agent 09 beantworten muss; für die
   Erlösarchitektur gilt: **ohne Softwarisierung der Fristenlogik trägt das Preismodell nicht.**

### 7. Monatlicher Betreuungsaufwand je Kunde

**2,5 h/Kunde/Monat [S]** im eingeschwungenen Zustand (1,8 h Ops + 0,4 h Koordination + 0,3 h QS).
In den ersten drei Monaten nach Onboarding: **8–14 h/Monat** [S].
Je 1.000 € Umsatz: **2,17 h** [S].

### 8. Kundenzahl-Tabelle

| Ziel | Standorte bei 1.150 € ARPU | Verträge (Ø 2,2 Standorte/Kunde [A]) |
|---|---|---|
| 10.000 € MRR | **9** [S] | 4 |
| 30.000 € MRR | **26** [S] | 12 |
| 100.000 €/Monat | **87** [S] | 40 |
| 190.000 €/Monat | **166** [S] | **76** |

Setup-Umsatz kommt hinzu und ist **kein MRR**: bei 6 Neustandorten/Monat × 4.500 € =
27.000 €/Monat Zusatzumsatz [S], der beim Erreichen der Zielgröße wegbricht, wenn das Wachstum
stoppt. Ehrliche Lesart: Von 190.000 € Monatsumsatz sind bei laufendem Wachstum ca. 155.000 €
MRR und 35.000 € Setup [S] → MRR-Quote 82 %, Kriterium „≥ 60 % MRR" klar erfüllt.

### 9. In 24 Monaten akquirierbar?

Annahmen: Ticket 1.150 € MRR + 4.500–7.900 € Setup. Entscheider: Geschäftsführung oder
technische Leitung. Verkaufszyklus 3–6 Monate [S] (Haftungsargument beschleunigt, Budgetierung
bremst). Abschlussrate **1,2 Verträge je Vertriebs-FTE-Monat** [S].

- 48 FTE-Monate × 1,2 = **58 Verträge** brutto
- × 2,2 Standorte = 127 Standorte
- − Churn (kumuliert ca. 8 % auf den durchschnittlichen Bestand) = −10
- − Ramp-Abschlag (die letzten 3 Monate tragen nur teilweise) = −12
- = **~105 aktive Standorte in Monat 24 → 120.750 € MRR** [S]

**100.000 €: JA** – erreichbar in Monat 21–23 [S].
**190.000 €: NEIN in 24 Monaten.** Bei fortgesetzter Vertriebsskalierung (5–6 AE) erreichbar in
**Monat 32–38** [S].

Zweiter Engpass, der geprüft werden muss: 127 Standorte × 2 Vor-Ort-Tage Erstaufnahme =
254 Auditorentage über 24 Monate = 11 Tage/Monat = **0,7 FTE Auditor** [S]. Beherrschbar.

---

## S02 — Terminierungs-Abo für Prüf- und Wartungsdienstleister

### 1. Erlösbausteine einzeln

| Baustein | Preis | Begründung / Anker |
|---|---|---|
| **Setup / Anbindung** | **2.900 €** einmalig [S] | Fälligkeitsdaten-Anbindung (Certado/Vemas/Excel), Gesprächsleitfaden, Stimm- und Skript-Tuning, Testkampagne, UWG-konforme Einwilligungsprüfung. Anker: **FoxifAI 1.920 € Setup** [F-sek] belegt, dass deutsche KMU vierstellige Setups für Voice-Produkte akzeptieren. Hier kommt die Datenanbindung dazu → 2.900 € begründbar. Eigenkosten: 22 h × 62 € = 1.364 € [S] → 53 % Setup-Marge |
| **Monatsgrundgebühr je Betrieb** | **449 €** (bis 600 Bestandskunden), **749 €** (bis 1.500), **1.190 €** (bis 3.000) [S] | Muss unter dem entfallenden Personalkostenanteil liegen: eine Bürokraft, die 3 Tage/Monat telefoniert = 24 h × 30 € Vollkosten = **720 €/Monat** [S]. 449 € liegt deutlich darunter → einfache Ja-Entscheidung. Gleichzeitig weit über dem 29–299-€-Voice-Band [F], weil es kein Voice-Produkt ist, sondern ein Terminprodukt |
| **Nutzungsgebühr je bestätigtem Termin** | **12 €** [S] | Der wichtigste Preis des Modells. Anker: Agentur-Terminierung B2B kostet **150–400 € je qualifiziertem Termin** [F, 2026-08], interner SDR 80–200 € [F] – das sind Kaltakquisepreise bei 2–5 % Terminquote [F]. Hier: **Bestandskunde mit gesetzlicher Fälligkeit**, erwartete Terminquote 35–55 % [A, muss gemessen werden]. Wert je Termin für den Kunden = Auftragswert, belegt **150–350 € bei einem Büro-DGUV-V3-Auftrag** [F], bei Industriekunden 800–3.000 € [A]. 12 € = **3,4–8 % des Auftragswerts** – unterhalb jeder Provisionsschwelle und damit ein Ja-Preis. Bei 30 € würde der Kunde anfangen zu rechnen, ob Frau Meier billiger ist |
| **Reaktivierungstermin** | **25 €** [S] | Bestandskunde, der seit > 18 Monaten keinen Auftrag erteilt hat. Das ist echter Neuumsatz und für den Kunden das Dreifache wert. Preisdifferenzierung nach Nutzenhöhe, nicht nach Aufwand |
| **Zusatzmodul Tourenoptimierung** | 199 €/Monat [S] | Vemas verkauft „optimiert Termine, Touren und Ressourcen automatisch" als Kernfeature [F] – der Markt hat den Nutzen bereits bepreist |
| **Zusatzmodul Angebots-Nachfassung** | 249 €/Monat [S] | Mangel → Angebot → Nachfassanruf. Direkte Übernahme des Inspect-Point-Prinzips [F-sek] |
| **Zusatzmodul SMS/WhatsApp-Bestätigung** | 99 €/Monat [S] | Anker: fonio verlangt 79 €/Monat für WhatsApp als Zusatzfeature [F] |
| **Zusatzmodul Mahnanruf** | 149 €/Monat [S] | Gleiche Infrastruktur, anderer Anlass, hoher wahrgenommener Wert |
| **Premium-Support „Managed Campaign"** | **299 €/Monat** [S] | Ein Kundenerfolgsmanager fährt die Kampagne monatlich, statt dass der Kunde Listen selbst auswählt. **Bei dieser Zielgruppe (5–40 MA, geringe Softwareaffinität) ist das die realistische Standardvariante, nicht die Ausnahme** – entsprechend hoch die Anschlussquote |
| **Hardware-Miete** | keine | reine Software/Telefonie |
| **Erfolgsanteil** | **verworfen** | Ein Umsatzanteil (z. B. 3 % des terminierten Auftragswerts) wäre wertgerecht, setzt aber voraus, dass der Betrieb uns seine Auftragswerte offenlegt. Das tut kein Mittelständler. Die Termingebühr ist der praktikable Ersatz |

**Ziel-ARPU [S]:** Betrieb mit 800 Bestandskunden ≈ 67 Fälligkeiten/Monat, davon 40 terminiert.
449 (Grund) + 480 (40 × 12 €) + 299 (Managed) + 199 (ein Modul) = **1.427 €/Monat**.
Konservativer Planwert für alle Rechnungen: **1.200 €/Monat** [S].

### 2. Preis-Logik: je Betrieb (Sockel) + je bestätigtem Termin (Nutzung)

- **Je Termin ist die überlegene Nutzungsmetrik**, weil sie die einzige Größe ist, die der
  Kunde selbst in Euro umrechnen kann. Er weiß, was ein Prüfauftrag wert ist. Ein Minutenpreis
  oder ein Anrufpreis würde ihn zwingen, unser Kostenmodell zu bewerten – das will er nicht und
  kann er nicht.
- **Der Sockel ist notwendig**, weil das Terminvolumen saisonal schwankt und die
  Fälligkeitsdatenbank ganzjährig gepflegt werden muss. Ohne Sockel hätten wir Monate mit
  Deckungsbeitrag null.
- **Je Nutzer wäre absurd** – der Betrieb hat eine Bürokraft.
- **Je Bestandskunde in der Datenbank** (statt je Termin) wurde geprüft und verworfen: Es
  bestraft den Kunden dafür, dass er seine Karteileichen hochlädt – und genau die sollen wir
  reaktivieren.

### 3. Der zentrale Punkt: Monat 13

**Antwort: Ja – die stärkste Monat-13-Begründung im gesamten Feld.**

Der Nutzen ist kein Zustand, sondern ein **Strom**. In Monat 13 liefert das System dieselben
40 Termine wie in Monat 1, und jeder einzelne ist in Euro bewertbar. Es gibt keinen
„Einrichtung ist erledigt"-Moment, weil die Einrichtung nie das Produkt war – die Fälligkeiten
laufen jedes Jahr neu auf. Das ist der Kern von Befund 3 in Reinform: **Der Kunde kann den
Anbieter wechseln, aber nicht die Fälligkeit.**

Zusätzlich schlägt in Monat 13 zum ersten Mal die vollständige Jahreswelle durch: Der Betrieb
sieht den Jahresvergleich seiner Reaktivierungsquote und seiner Technikerauslastung.

**Nachweisbarkeit: die beste der acht Modelle.** Monatsreport: „X Termine bestätigt,
Y Bestandskunden reaktiviert, Z € Auftragsvolumen daraus." Der Kunde kann jede Zahl in seinem
eigenen ERP gegenprüfen. Wir behaupten nichts, was er nicht selbst nachzählen kann.

**Die Kehrseite, die ausgesprochen gehört:** Messbarer Nutzen ist auch messbar *negativ*. Ein
schwacher Monat erzeugt sofort eine Kündigungsdiskussion. Modelle mit unsichtbarem Nutzen
(S01) werden nie hinterfragt; Modelle mit sichtbarem Nutzen werden jeden Monat neu bewertet.

### 4. Kündigungsrisiko: Was passiert am Tag danach?

Die Fälligkeitsliste läuft weiter – aber niemand ruft an. Innerhalb von **4–8 Wochen** [S]
fällt die Technikerauslastung sichtbar; die Lücken im Dispositionskalender sind physisch
sichtbar. Frau Meier müsste zurück ans Telefon und schafft 60 statt 400 Kunden [aus A10 Modell 12].
Der Schmerz tritt **schnell** ein und ist **in Euro sichtbar** – die beste Schmerzkurve der Liste.

**Aber – und das ist die ehrliche Gegenrede:** Es gibt **keine harten Wechselkosten**. Die
Fälligkeitsdaten gehören dem Kunden und liegen in seinem ERP. Er kann jederzeit zurück zur
Bürokraft oder zu einem Wettbewerber. Und Certado/Vemas sitzen bereits auf den Daten und
könnten das Feature bauen [aus 13_shortlist, offene Flanke].

**Churn [S]: 12–18 %/Jahr.** Rechenweg: Der Kündigungsschmerz ist hoch (drückt), die
Wechselhürde ist niedrig (hebt), die Leistung ist monatlich messbar und damit monatlich
angreifbar (hebt). Vergleichsband: ergebnisbasierte B2B-Dienstleistungen ohne Datenbindung
liegen typisch bei 15–25 %/Jahr [A]; die gesetzliche Fälligkeitsbasis drückt das nach unten.
**Gegenmittel: 24-Monats-Erstlaufzeit gegen 50 % Setup-Rabatt** – das ist der wirksamste
Einzelhebel im ganzen Modell.

### 5. Wechselkosten und Bindung

| Dimension | Stärke | Konkret |
|---|---|---|
| Daten | **niedrig** | Die Fälligkeitsdaten sind seine, nicht unsere |
| Hardware | keine | — |
| Verträge | **mittel** | Nur so stark wie die Erstlaufzeit; muss vertraglich erzwungen werden, weil es strukturell nicht entsteht |
| Prozessintegration | **mittel-hoch** | Kalender- und ERP-Rückschreibung: die Termine landen direkt in seiner Disposition. Wer das abschaltet, muss seine Disposition umbauen |
| Historie | **mittel-hoch, unterschätzt** | Nach 24 Monaten weiß das System, dass Kunde Müller nur dienstags vormittags kann, Kunde Schmidt zweimal angerufen werden muss und Kunde Weber nur per WhatsApp reagiert. **Diese Präferenzhistorie liegt in unseren Gesprächsprotokollen, nicht in seinem ERP.** Das ist das einzige echte Datenkapital des Modells – es muss bewusst aufgebaut und im Vertrag als unser Betriebsgeheimnis verankert werden |

### 6. Bruttomarge mit Rechenweg

Basis: ARPU 1.200 €/Monat, 40 bestätigte Termine.

| Kostenposition je Kunde/Monat | Betrag | Herleitung |
|---|---|---|
| KI-Telefonieminuten | 24 € | 40 Termine ⇒ ~110 Anrufversuche × 1,8 Min = 198 Min × 0,12 €/Min [F-Band fonio 0,12–0,15; Vollkosten 0,10–0,12 [S]] |
| Rufnummern/Trunk | 15 € | [S] |
| Plattform/Hosting | 18 € | [S] |
| Managed-Campaign-Betreuung | 87,50 € | 2,5 h × 35 € [S] |
| Ausnahmen/Beschwerden | 17,50 € | 0,5 h × 35 € [S] |
| **Summe** | **162 €** | |

**Bruttomarge = (1.200 − 162) ÷ 1.200 = 86,5 %** [S].
Konservativ bei 4 h Kampagnensteuerung statt 2,5 h: **79–86 %** [S].

Anzumerken: Die Telefoniekosten sind **nicht** der Engpass (24 € von 1.200 €). Der Engpass ist
die Kampagnensteuerung durch Menschen. Wer die nicht automatisiert, hat kein Softwaregeschäft,
sondern ein Callcenter mit besserem Werkzeug.

### 7. Monatlicher Betreuungsaufwand je Kunde

**3,0 h/Kunde/Monat [S]**. Je 1.000 € Umsatz: **2,50 h** [S].
Bei 100 Kunden = 300 h/Monat = **2,0 FTE**. Das ist der wunde Punkt des Modells.

### 8. Kundenzahl-Tabelle

| Ziel | Betriebe bei 1.200 € ARPU |
|---|---|
| 10.000 € MRR | **9** [S] |
| 30.000 € MRR | **25** [S] |
| 100.000 €/Monat | **84** [S] |
| 190.000 €/Monat | **159** [S] |

MRR-Struktur: Grundgebühr + Managed + Module = 947 € (79 %) sind vertraglich fix; 480 € (34 %
des Bruttos, hier überlappend gerechnet) sind volumenabhängig. Für die 60-%-MRR-Quote unkritisch.

### 9. In 24 Monaten akquirierbar?

Entscheider: Inhaber, allein entscheidungsbefugt. Verkaufszyklus **3–8 Wochen** [S] – der
kürzeste der acht Modelle, weil das Angebot einen Euro-Nutzen hat und keine Gremien braucht.
Abschlussrate **2,5 je Vertriebs-FTE-Monat** [S].

- 48 × 2,5 = **120 Abschlüsse** brutto
- − Churn (15 % auf durchschnittlichen Bestand über 24 Monate) = −16
- − Ramp-Abschlag = −8
- = **~96 aktive Kunden in Monat 24 → 115.200 € MRR** [S]

**100.000 €: JA** – erreichbar in Monat 20–22 [S].
**190.000 €: NEIN in 24 Monaten** – bei fortgesetzter Skalierung Monat 30–34 [S].

**Zwei Vorbehalte, die vor jedem Vertriebsaufbau geklärt sein müssen:**
1. **UWG § 7** bei Anrufen an Bestandskunden des Auftraggebers – anwaltlich, vor dem ersten Euro
   (Auftrag an Agent 08).
2. **Betreuungskapazität**: 96 Kunden × 3 h = 288 h/Monat. Ohne Automatisierung der
   Kampagnensteuerung ist bei ~60 Kunden Schluss.

---

## S03 — Sensor-Monitoring als Motor für Wartungs-Mitgliedschaften (SHK)

### 0. Vorbemerkung: eine notwendige Korrektur an der Shortlist

Die Shortlist rechnet mit **200 Betriebe × 500 €/Monat = 100.000 €/Monat** [S] und stützt die
Zahlungsbereitschaft auf die US-Ökonomie von SmartAC: **~1.000 $/Jahr je Endkunden-Mitgliedschaft**
und Retentionssprung von 70 % auf 97 % [F-sek].

**Diese Übertragung hält der deutschen Preisrealität nicht stand.** Neu belegt in dieser Session:
Ein deutscher Heizungswartungsvertrag kostet den Endkunden **180–350 €/Jahr**, eine Einzelwartung
80–260 € [F, badenova.de / energie-experten.org / my-hammer.de, 2026-08]. Das ist **Faktor 3–5
kleiner** als die amerikanische Membership.

Konsequenz für die Erlösarchitektur: Der Retentionsgewinn je Endkunde beträgt in DE
**250 € × 0,27 = 67,50 €/Jahr** [S] statt ~270 $. Der gesamte Preisspielraum schrumpft
entsprechend. Jede Preisfestlegung unten trägt diese Korrektur.

Zweiter neuer Warnbefund: **Bosch HomeCom Pro und Vaillant bieten Fachbetrieben die
Fernüberwachung bereits an** [F, energie-fachberater.de / vaillant.de, 2026-08] – herstellergebunden,
Preise nicht veröffentlicht. Die Lücke (Mischbestand, herstellerunabhängig) besteht damit
weiterhin, aber der Betrieb hat für seine Marken-Neuanlagen bereits eine kostenlose oder
gebündelte Lösung. **Wir konkurrieren nicht gegen nichts, sondern gegen null Euro.**

### 1. Erlösbausteine einzeln

| Baustein | Preis | Begründung / Anker |
|---|---|---|
| **Setup / Onboarding** | **1.500 €** einmalig je Betrieb [S] | Contractor-Dashboard, gebrandete Endkunden-App, Schulung des Verkaufsteams, 3 begleitete Musterinstallationen. Bewusst **unter** dem FoxifAI-Anker (1.920 € [F-sek]), weil hier die Adoption über allem steht: ein Betrieb, der nicht ausrollt, zahlt nie eine Nutzungsgebühr |
| **Monatsgrundgebühr je Betrieb** | **249 €/Monat** (Dashboard, App, bis 25 Anlagen inkl.) [S] | Anker: Handwerkersoftware 15–120 €/Nutzer, Core-Version 59 €/Nutzer [F]. Ein 8-Nutzer-SHK-Betrieb zahlt heute 320–470 €/Monat für sein ERP. 249 € als **Zweitsystem** ist die Obergrenze des Erträglichen |
| **Nutzungsgebühr je aktiver Anlage** | **2,20 €/Monat** ab Anlage 26 [S] | Harte Obergrenze aus der Endkundenrechnung: Der Wartungsvertrag bringt dem Betrieb 250 €/Jahr = 20,83 €/Monat, davon vielleicht 40 % Deckungsbeitrag = 8,33 €/Monat [S]. Mehr als ~25 % dieses Deckungsbeitrags kann unsere Gebühr nicht sein → 2,20 €. Zum Vergleich: der HACCP-Markt trägt 4,95–8,00 €/Messstelle [F] – dort ist die Überwachung aber Pflicht, hier ist sie Kür |
| **Hardware** | Sensorkit **149 € Verkauf** je Anlage (Einkauf 89 € [A]) | **Verkauf statt Miete – bewusste Architekturentscheidung.** Miete zu 4,90 €/Monat über 36 Monate ergäbe 176 € und stärkere Bindung, bindet aber Kapital: 89 € × 5.000 Anlagen = **445.000 €** [S]. Unter Annahme A10 (kein VC) nicht darstellbar |
| **Zusatzmodul „Mitgliedschafts-Verkaufsmaschine"** | **299 €/Monat** [S] | Anomalie erkannt → automatisches Angebot → Endkunden-Anruf durch unseren Voice-Agent. **Das ist die CallSuite-Verbindung und der eigentliche Wert des Modells** – hier wird aus Monitoring Umsatz. Preis orientiert sich am Managed-Campaign-Baustein aus S02 |
| **Premium-Support „Alarm-Triage"** | 199 €/Monat [S] | Vorqualifizierung der Meldungen, damit der Betrieb nicht 200 Fehlalarme sichtet. Ohne diesen Baustein scheitert die Adoption – deshalb faktisch Pflichtmodul |
| **Erfolgsanteil** | 12 € je verkaufter Endkunden-Mitgliedschaft [S] – **nur optional** | Reizvoll, aber schwer prüfbar: der Betrieb kann Abschlüsse verschweigen. Nur durchsetzbar, wenn der Abschluss im Dashboard erfasst wird, was wiederum Adoption voraussetzt. Als Nice-to-have führen, nicht als Planposition |

**Ziel-ARPU [S]:** Betrieb mit 60 aktiven Anlagen: 249 + (35 × 2,20 = 77) + 299 + 199 =
**824 €/Monat**. Konservativer Planwert wegen Modul-Anschlussquote < 100 %: **680 €/Monat** [S].

Damit ist die Shortlist-Annahme von 500 €/Monat nach oben korrigiert – aber nur, weil die
margenstarken Module mitgerechnet sind. **Ohne die Verkaufsmaschine liegt der ARPU bei ~330 €**
und das Modell fällt unter die 400-€-Filterregel aus Befund 1.

### 2. Preis-Logik: je Betrieb (Sockel) + je aktiver Anlage

- **Je aktiver Anlage** ist zwingend, weil der Nutzen des Betriebs mit der Zahl seiner
  Mitgliedschaften skaliert. Eine Pauschale je Betrieb würde die gesamte Skalierung an den
  erfolgreichsten Kunden verschenken – und genau die erfolgreichen Kunden sind die, die man
  behalten will.
- **„Aktiv" statt „installiert"** ist die entscheidende Definition: Nur Anlagen, die im
  Berichtsmonat Daten geliefert haben, werden berechnet. Das nimmt dem Kunden das Risiko und
  zwingt uns zur Datenqualität.
- **Je Endkunde wäre falsch**, weil wir keine Vertragsbeziehung zum Endkunden haben und nicht
  wissen dürfen, was der Betrieb ihm berechnet.
- **Je Nutzer wäre falsch** – dieselbe Begründung wie bei S01.

### 3. Der zentrale Punkt: Monat 13

**Antwort: Ja, aber mit spürbar dünnerem Polster als S01/S02/S04.**

Der laufende Nutzen ist real und täglich: Anomalien werden erkannt, bevor der Endkunde anruft.
Die belegte Retentionswirkung (70 % → 97 % [F-sek]) ist eine **laufende** Wirkung, keine
einmalige – solange die Sensoren melden, hält die Mitgliedschaft.

**Die Rechnung in Monat 13, ehrlich aufgemacht [S]:**
Betrieb mit 300 Endkunden-Mitgliedschaften à 250 €/Jahr:
- Retentionsgewinn: 300 × 250 € × (0,97 − 0,70) = **20.250 €/Jahr Mehrertrag**
- Unsere Gebühr: 824 € × 12 = **9.888 €/Jahr**
- **Faktor 2,05**

Bei Faktor 2 verhandelt der Kunde. Bei Faktor 5 nicht. Zum Vergleich: In den USA liegt derselbe
Faktor bei ~6–8, weil die Membership viermal so teuer ist. **Das ist der Grund, warum S03 in
Deutschland ein schwächeres Modell ist als in seinem Ursprungsmarkt – und dieser Unterschied
ist nicht durch bessere Ausführung heilbar.**

Zusätzlich muss die 97-%-Zahl relativiert werden: sie stammt aus **Anbieter-PR** [F-sek] und ist
nicht unabhängig verifiziert.

### 4. Kündigungsrisiko: Was passiert am Tag danach?

**Hier ist S03 stark.** Die Sensoren hören auf zu senden. 300 Endkunden, denen der Betrieb eine
„Premium-Mitgliedschaft mit Fernüberwachung" verkauft hat, bekommen keine Meldungen mehr – und
zahlen weiter. Der Betrieb steht vor **seinen eigenen Kunden** mit einem Leistungsversprechen,
das er nicht mehr erfüllen kann. Das ist rechtlich (Minderung, Kündigung der Mitgliedschaft)
und geschäftlich (Vertrauensverlust) ein sofortiges Problem.

**B2B2C-Weiterverkauf ist die härteste Bindungsform, die es gibt** – der Kunde hat unsere
Leistung an seine Kunden weitergegeben und kann sie nicht einseitig zurücknehmen.

**Churn [S]: 8–12 %/Jahr – aber mit einer wichtigen Struktur:**
Der Hauptchurn ist **kein Wert-Churn, sondern Adoptions-Churn** und fällt in **Monat 4–9**. Ein
Betrieb, der nach sechs Monaten erst 8 Sensoren ausgerollt hat, kündigt – nicht weil das Produkt
schlecht ist, sondern weil er es nie benutzt hat. Nach erfolgreicher Ausrollung (> 40 Anlagen)
liegt der Churn bei **3–5 %/Jahr** [S], weil die Hardware physisch in fremden Kellern hängt.
**Architekturkonsequenz: Das Setup muss 25 garantierte Installationen enthalten**, sonst
verkauft man Kündigungen im Voraus.

### 5. Wechselkosten und Bindung

| Dimension | Stärke | Konkret |
|---|---|---|
| Daten | mittel | Anlagenhistorie, Anomaliemuster – wertvoll, aber ersetzbar |
| Hardware | **sehr hoch nach Ausrollung** | 300 Sensoren in 300 fremden Kellern. Ein Wechsel bedeutet 300 Hausbesuche bei Privatkunden, die dafür Termine geben müssen. Praktisch prohibitiv |
| Verträge | mittel | 24-Monats-Laufzeit üblich |
| Prozessintegration | mittel-hoch | Dashboard im Tagesbetrieb der Disposition |
| Historie | **hoch, mittelbar** | Die Endkunden-Mitgliedschaftsbeziehung basiert auf unserer App |

### 6. Bruttomarge mit Rechenweg

Basis: 60 aktive Anlagen, ARPU 680 €/Monat, Hardware **verkauft** (nicht in COGS des Abos).

| Kostenposition je Kunde/Monat | Betrag | Herleitung |
|---|---|---|
| SIM/Konnektivität | 27 € | 60 × 0,45 € [S, Anker: NB-IoT-SIM 0,5–1,5 € [A], Mengenrabatt] |
| Cloud/Datenhaltung | 15 € | 60 × 0,25 € [S] |
| Dashboard-Hosting je Betrieb | 8 € | [S] |
| Alarm-Triage | 42 € | 1,2 h × 35 € [S] |
| Voice-Minuten Endkundenanrufe | 11 € | 60 Anrufe × 1,5 Min × 0,12 € [S] |
| Betriebsbetreuung | 52,50 € | 1,5 h × 35 € [S] |
| **Summe** | **155,50 €** | |

**Bruttomarge = (680 − 155,50) ÷ 680 = 77,1 %** [S]. Konservativ **70–77 %** [S].

**Sensitivität Hardware-Miete:** bei Miete statt Verkauf +60 × (89 € ÷ 36) = **+148 €** →
Bruttomarge **55,1 %** [S]. Miete kostet also **22 Margenpunkte plus 445.000 € Kapital**.
Klare Empfehlung: Verkauf.

### 7. Monatlicher Betreuungsaufwand je Kunde

**2,7 h/Kunde/Monat [S]**. Je 1.000 € Umsatz: **3,97 h** [S] – der zweitschlechteste Wert der Liste.

### 8. Kundenzahl-Tabelle

| Ziel | SHK-Betriebe bei 680 € ARPU |
|---|---|
| 10.000 € MRR | **15** [S] |
| 30.000 € MRR | **45** [S] |
| 100.000 €/Monat | **148** [S] |
| 190.000 €/Monat | **280** [S] |

Zum Vergleich: Die Shortlist nennt 200 Betriebe für 100.000 € – korrigiert sind es **148 bei
680 € ARPU** bzw. **200 bei 500 €**. Für das *echte* Ziel von 190.000 € sind es **280 Betriebe**
= ca. 0,56 % aller ~50.000 SHK-Betriebe in DE [A].

Hardware-Umsatz kommt hinzu und ist **kein MRR**: 60 € Marge × 60 Anlagen je Neukunde. Bei 6
Neukunden/Monat = 21.600 €/Monat [S]. Diese Zahl ist gefährlich, weil sie das Modell größer
aussehen lässt, als es wiederkehrend ist.

### 9. In 24 Monaten akquirierbar?

Abschlussrate **3,0 je Vertriebs-FTE-Monat** [S] – leichter zu verkaufen als S01, weil kleineres
Ticket und Inhaberentscheidung, Zyklus 4–10 Wochen.

- 48 × 3,0 = **144 Abschlüsse** brutto
- − 20 % Nicht-Ausrollung (Adoptions-Churn) = −29
- − 10 % Wert-Churn = −12
- − Ramp-Abschlag = −8
- = **~95 aktive Betriebe in Monat 24 → 64.600 € MRR** [S]

**100.000 €: NEIN in 24 Monaten** – erreichbar in **Monat 30–33** [S].
**190.000 €: NEIN** – **Monat 44+** [S].

Der Grund ist ausschließlich die Preispunkt-Arithmetik aus Befund 1: **680 € ARPU liegt unter
der Schwelle, ab der 24 Monate reichen.** Das Modell ist nicht schlecht – es ist zu klein bepreist,
und der deutsche Endkundenpreis lässt keinen höheren Preis zu.

---

## S04 — Aufschalt- und Leitstellen-Modell für Gebäudetechnik

### 1. Erlösbausteine einzeln

| Baustein | Preis | Begründung / Anker |
|---|---|---|
| **Setup / Aufschaltgebühr je Objekt** | **249 €** einmalig je Aufschaltpunkt [S] | Anker: „Einrichtung **150–600 €** einmalig" [F, notrufexperten.de/accsicherheitstechnik.de]; NSL-Setup beim Leitstellenbetreiber **89–150 €** [F, 2026-08]. Einkauf ~120 € [S] → **52 % Setup-Marge**. Bei einem Portfoliokunden mit 140 Objekten = **34.860 € Setup bei Vertragsschluss** – das deckt die Kundenakquisitionskosten um ein Vielfaches. **Kriterium 18 in Reinform, und zwar belegt** |
| **Monatsgrundgebühr je Kundenkonto** | **149 €/Monat** [S] | Portal, Objektstammdaten, BetrSichV-Nachweise, Alarmhistorie, Reporting. Anker: CAFM-Cloud ab 195 €/Monat, VISA-FM Raumbuch 250 €/Monat [F, A01]. Wir liegen bewusst darunter, weil das Portal Beiwerk ist. Zweck des Sockels: verhindern, dass ein 8-Objekte-Kunde unter die Deckungsgrenze fällt |
| **Nutzungsgebühr je Aufschaltpunkt** | **44 €** (1–24 Objekte) / **38 €** (25–99) / **32 €** (100–499) / **27 €** (ab 500) pro Monat [S] | Anker: „Standardaufschaltungen üblicherweise **20–60 €/Monat**", „ab 24,95 €", „ab 29,95 €" [F, A01 Z. 273]. Wir positionieren im **oberen Drittel**, weil wir Multi-Gewerk, Nachweisführung und Portal liefern, nicht nur die reine Aufschaltung. Einkauf White-Label: **14–18 €/Punkt/Monat** [S, abgeleitet aus A01 Z. 277: „15–20 € Einkauf gegen 35–50 € Verkauf"] |
| **Zusatzmodul Aufzugswärter-Koordination** | 12 €/Aufzug/Monat [S] | Anker: Aufzugswärter-Service 200–600 €/Jahr [A, A01] = 17–50 €/Monat für die *Leistung*; wir koordinieren nur und nehmen ein Viertel |
| **Zusatzmodul Interventionsdisposition** | 9 €/Objekt/Monat [S] | Die Intervention selbst wird durchgereicht (§ 34a GewO bleibt beim Sicherheitsdienst – wichtig für K.-o. 3) |
| **Zusatzmodul BetrSichV-Nachweisakte** | 4 €/Objekt/Monat [S] | Reine Software, ~95 % Marge, hebt den Mischpreis |
| **Premium-Support „Störungsmanagement"** | **690 €/Monat** je Portfoliokunde [S] | Wir nehmen die Störung an, disponieren den Wartungspartner, verfolgen bis Abschluss. **Das ist der Baustein, der aus 38 € Aufschaltung ein Servicegeschäft macht** – und der Baustein mit der höchsten Eigenmarge |
| **Hardware-Miete** | Kommunikationsmodul/Router **6,90 €/Objekt/Monat** [S], nur wo nötig | Einkauf 110–160 € [A] → Amortisation in 16–23 Monaten. Bewusst optional, um Kapitalbindung zu begrenzen |
| **Erfolgsanteil** | keiner | Nicht darstellbar; die Leistung ist Verfügbarkeit |

**Beispielkunde (Hausverwaltung, 140 Objekte):**
149 + (140 × 38 = 5.320) + (140 × 4 = 560) + 690 = **6.719 €/Monat** [S].
**Kleinkunde (12 Objekte):** 149 + (12 × 44) = **677 €/Monat**.
**Ziel-ARPU über den Mix (Ø 55 Objekte): 2.400 €/Monat** [S].

### 2. Preis-Logik: je Aufschaltpunkt, gestaffelt, an einen Portfolio-Zahler

Das ist die **überlegene Preislogik der gesamten Liste** und der Grund, warum S04 arithmetisch
funktioniert:

- Der Aufschaltpunkt ist **Branchenstandard** – der Kunde muss nichts Neues lernen, kein Anbieter
  kann behaupten, wir würden anders rechnen.
- Er entspricht **exakt der Kostenstruktur**: jeder zusätzliche Punkt kostet uns 14–18 € Einkauf.
  Die Marge ist damit bei jeder Kundengröße stabil.
- Er ist **prüfbar**: der Kunde kann seine Objekte zählen. Keine Wertdiskussion.
- Er **wächst mit dem Kunden ohne Neuverkauf**: Kauft die Hausverwaltung 30 Objekte dazu, steigt
  unser Umsatz um 1.140 €/Monat, ohne dass ein Vertriebler tätig wird. Das ist der Land-and-Expand-
  Effekt, den keine der anderen sieben Preislogiken in dieser Stärke hat.
- **Je Standort wäre falsch**, weil ein Standort 1 oder 40 Aufschaltpunkte haben kann.

Die **Staffel** ist notwendig und nicht optional: Ohne sie kauft ein 500-Objekte-Kunde nicht,
weil 44 € × 500 = 22.000 €/Monat jenseits seiner Vorstellung liegt. Mit der Staffel zahlt er
27 € × 500 = 13.500 € – und wir verdienen an ihm absolut mehr als an 20 Kleinkunden bei
geringerem Betreuungsaufwand.

### 3. Der zentrale Punkt: Monat 13

**Antwort: Ja – der einzige der acht Bausteine, bei dem die Frage strukturell gar nicht
gestellt werden muss.**

Die Leistung *ist* die laufende Leistung. In Monat 13 sitzt nachts um 3 Uhr ein Disponent in der
Leitstelle, wenn im Aufzug jemand eingeschlossen ist. Es gibt keinen „Einrichtung ist erledigt"-
Moment, weil die Einrichtung nie das Produkt war – sie war die Voraussetzung dafür, das Produkt
zu erhalten.

Verstärkend: Die Aufschaltung erfüllt eine **gesetzliche Pflicht** (Zwei-Wege-Notrufsystem nach
BetrSichV / EN 81-28 für Aufzüge; Auflagen der Sachversicherer bei Brandmelde- und Einbruchmeldeanlagen).
Der Kunde zahlt nicht für einen Nutzen, den er abwägen kann, sondern für einen Zustand, den er
haben muss.

**Nachweisbarkeit:** vollständig auditierbar – Alarmprotokoll mit Zeitstempel, Reaktionszeiten,
Befreiungsdauern, Verfügbarkeitsstatistik, BetrSichV-Nachweis für die ZÜS-Prüfung. Jede Zahl
gerichtsfest.

### 4. Kündigungsrisiko: Was passiert am Tag danach?

**Der härteste Kündigungsschmerz der gesamten Liste.**

Am Tag nach der Kündigung sind die Aufzüge im Rechtssinne nicht mehr betriebsfähig – ohne
aufgeschaltetes Notrufsystem darf der Betreiber sie nicht betreiben. Er muss sie stilllegen oder
er handelt ordnungswidrig, bei einem Personenschaden haftet er persönlich. Das gilt **sofort**,
nicht in drei Monaten.

Er kann also nicht zu „nichts" wechseln, nur zu einem anderen Anbieter. Und dieser Wechsel
bedeutet: **140 Objekte umkonfigurieren** – jedes Notrufgerät muss auf die neue NSL-Rufnummer
umprogrammiert werden, teils vor Ort, teils per Fernkonfiguration, jedes mit Funktionstest und
Protokoll. Bei 140 Objekten sind das 140 Einsätze über 6–12 Wochen [S].

**Churn [S]: 3–6 %/Jahr – der niedrigste der acht Modelle.**
Rechenweg: gesetzliche Pflicht (drückt stark) + physischer Umkonfigurationsaufwand (drückt stark)
+ Versicherungsauflagen (drückt) + 24–36-Monats-Verträge als Branchenstandard [A] (drückt).
Gegenläufig nur: Objektverkäufe und Verwalterwechsel – das sind die realistischen
Kündigungsanlässe, und sie treffen einzelne Objekte, nicht ganze Verträge.

### 5. Wechselkosten und Bindung

| Dimension | Stärke | Konkret |
|---|---|---|
| Daten | mittel-hoch | Alarmhistorie, Nachweisakte über Jahre |
| Hardware | **hoch** | Kommunikationsmodule vor Ort; bei Miete zusätzlich Rückgabelogistik |
| Verträge | **hoch** | 24–36 Monate Branchenstandard, teils an Versicherungspolicen gekoppelt |
| Prozessintegration | **sehr hoch** | Die Eskalationskette ist im Notfallhandbuch des Kunden dokumentiert; Hausmeister, Techniker, Bereitschaft und Versicherer kennen unsere Nummer |
| Historie | hoch | Verfügbarkeitsnachweise gegenüber Eigentümern und ZÜS |

### 6. Bruttomarge mit Rechenweg — **hier steht der wichtigste Korrekturbefund zu S04**

Basis: Beispielkunde 140 Objekte, Umsatz 6.719 €/Monat, Leitstelle **White-Label eingekauft**.

| Kostenposition je Kunde/Monat | Betrag | Herleitung |
|---|---|---|
| NSL-Einkauf White-Label | 2.240 € | 140 × 16 € [S] |
| Portal/Hosting | 45 € | [S] |
| SIM je Objekt (wo eigenes Modul) | 112 € | 140 × 0,80 € [S] |
| Störungsdisposition | 288 € | 6 h × 48 € [S] |
| Kundenbetreuung | 90 € | 2 h × 45 € [S] |
| Stammdatenpflege | 52,50 € | 1,5 h × 35 € [S] |
| **Summe** | **2.827,50 €** | |

**Bruttomarge = (6.719 − 2.827,50) ÷ 6.719 = 57,9 %** [S].

**Das ist der entscheidende Befund zu S04 und er widerspricht der Shortlist.**
Die dort genannten **75–90 %** [S] gelten nur, wenn man die Leitstelle **selbst betreibt** –
dann sind die Grenzkosten je Punkt tatsächlich 2–6 € [A, A01 Z. 275]. Beim White-Label-Einkauf,
den dieselbe Shortlist zu Recht empfiehlt (kein Kapitalbedarf, keine VdS-Zertifizierung, kein
§ 34a), nimmt der Leitstellenbetreiber exakt die Marge, die man nicht selbst verdient.
**Man kauft Kapitalfreiheit mit rund 20 Margenpunkten.**

Zwei zulässige Lesarten, die getrennt gehalten werden müssen:

| Betrachtung | Rechnung | Marge |
|---|---|---|
| **Vollkonsolidiert** (NSL-Einkauf als COGS) | (6.719 − 2.827,50) ÷ 6.719 | **57,9 %** [S] |
| **Eigenleistungsbezogen** (NSL als durchlaufender Posten) | (6.719 − 2.240 − 587,50) ÷ (6.719 − 2.240) | **86,9 %** [S] |

Beide sind gültig; welche gilt, entscheidet die Vertragsgestaltung (Eigengeschäft vs. Vermittlung).
**Realistische Bandbreite bei White-Label: 55–66 %** [S] – über K.-o. 5 (45 %), aber **unter
Kriterium 2 (≥ 65 %)**. Hebel zur Verbesserung, in dieser Reihenfolge:
1. Anteil der reinen Softwaremodule erhöhen (Nachweisakte 4 €/Objekt, Portal, Reporting) – sie
   sind zu ~95 % Marge und heben den Mischsatz.
2. Mengenrabatt beim Leitstellenpartner (ab 2.000 Punkten realistisch 11–13 € statt 16 € [A])
   → Marge 63–68 %.
3. Ab ~3.000–5.000 Aufschaltpunkten eigene Leitstelle [A, A01 Z. 276] → 78–86 % [S], dann aber
   Kapitalbedarf, DIN EN 50518, VdS-Zertifizierung und 24/7-Personal.
   **Das ist eine Stufe-2-Entscheidung, kein Startpunkt.**

### 7. Monatlicher Betreuungsaufwand je Kunde

**9,5 h/Kunde/Monat [S]** – absolut der höchste Wert der Liste, aber es ist ein 6.719-€-Kunde.
Je 1.000 € Umsatz: **1,41 h** [S] – der zweitbeste Wert der Liste.
**Das ist die Kennzahl, auf die es ankommt**, und sie zeigt, warum Portfolio-Zahler strukturell
überlegen sind.

### 8. Kundenzahl-Tabelle

| Ziel | Vertragskunden bei 2.400 € ARPU | Aufschaltpunkte gesamt [S] |
|---|---|---|
| 10.000 € MRR | **5** [S] | ~240 |
| 30.000 € MRR | **13** [S] | ~710 |
| 100.000 €/Monat | **42** [S] | ~2.400 |
| 190.000 €/Monat | **80** [S] | **~4.500** |

Setup-Umsatz zusätzlich und **kein MRR**: bei 2 Neukunden/Monat × 55 Objekte × 249 € =
27.390 €/Monat [S].

### 9. In 24 Monaten akquirierbar?

Bremse: Der Zielkunde hat bereits eine Aufschaltung mit 24–36 Monaten Laufzeit. **Man kann ihn
nur zum Verlängerungszeitpunkt gewinnen** – in jedem Jahr ist also nur ein Drittel bis die Hälfte
des Marktes überhaupt ansprechbar. Verkaufszyklus 4–9 Monate [S].
Abschlussrate **0,8 je Vertriebs-FTE-Monat** [S].

- 48 × 0,8 = **38 Kunden** brutto
- − Churn (5 %) = −2
- − Ramp-Abschlag = −4
- = **~32 aktive Kunden in Monat 24 → 76.800 € MRR** [S]

**100.000 €: KNAPP NEIN in 24 Monaten** – erreichbar in **Monat 27–29** [S].
**190.000 €: NEIN** – **Monat 40–46** [S].

**Aber: S04 hat die höchste Varianz nach oben von allen acht.** Ein einziger Großkunde – eine
kommunale Wohnungsgesellschaft mit 1.200 Aufzügen – bringt bei 32 €/Punkt **38.400 €/Monat aus
einem Abschluss** [S] plus 298.800 € Setup. Zwei solche Logos verändern die 24-Monats-Antwort
komplett. Das ist ein Vertriebsspiel, das zu Nicos Stärkenprofil passt (verkaufen, präsentieren,
überzeugen) und nicht zu einer Inside-Sales-Organisation.

---

## S05 — Herstellerunabhängiges Anlagen-IoT für freie Servicebetriebe

### 1. Erlösbausteine einzeln

| Baustein | Preis | Begründung / Anker |
|---|---|---|
| **Setup / Flotten-Onboarding** | **3.900 €** einmalig je Servicebetrieb [S] | Bestandsaufnahme der Mischflotte, Sensor-Mapping je Fabrikat (Otis, Schindler, Kone, TK + Fremdfabrikate), Techniker-Schulung, 10 begleitete Musterinstallationen. Deutlich höher als S03, weil die **Fabrikatsvielfalt echten Engineering-Aufwand** erzeugt. Eigenkosten: 4 Tage × 8 h × 65 € = 2.080 € + Reise 400 € = **2.480 €** [S] → nur **36 % Setup-Marge**. Bewusst nahe an Selbstkosten: das Setup ist Adoptionshebel, kein Gewinnbringer |
| **Monatsgrundgebühr je Betrieb** | **390 €/Monat** (Plattform, bis 15 Anlagen inkl.) [S] | Höher als S03 (249 €), weil die Zielgruppe größer und die betreute Anlage wertvoller ist |
| **Nutzungsgebühr je Anlage** | **8,90 €/Monat** (1–99), **6,90 €** (100–399), **5,40 €** (ab 400) [S] | Anker: Marktband für Anlagen-Fernüberwachung **8–15 €/Sensor/Monat** [S/A, A01 Z. 243]; HACCP real 4,95–8,00 € [F]. Gegenrechnung für den Kunden: 8,90 € = **107 €/Jahr** gegen **500–1.500 €/Jahr Wartungsertrag je Aufzug** [F, 2026-08] = 7–21 %. Das ist zu viel für reine Information und angemessen, wenn ein Störungseinsatz gespart wird: **ein eingesparter Einsatz (150–350 € [A]) je Anlage und Jahr trägt die Gebühr allein** |
| **Hardware** | Sensor-/Gateway-Kit **349 € Verkauf** je Anlage (Einkauf 180 € [A]) | Gleiche Logik wie S03: Miete zu 12,90 €/Monat wäre bindender, bindet aber **540.000 € Kapital bei 3.000 Anlagen** [S]. Ohne VC → Verkauf |
| **Zusatzmodul Predictive** | 2,90 €/Anlage/Monat [S] | Ausfallvorhersage statt Zustandsanzeige – separate Wertstufe, separater Preis |
| **Zusatzmodul ZÜS-Prüfvorbereitungsakte** | 1,90 €/Anlage/Monat [S] | Die Monitoringdaten reduzieren den Prüfvorbereitungsaufwand vor der BetrSichV-Prüfung [aus A02 Modell 27]. Reine Software, ~97 % Marge |
| **Zusatzmodul White-Label-Endkundenportal** | **249 €/Monat** [S] | Der Servicebetrieb gibt seinen Objektbetreibern Zugang. **Der wichtigste Baustein des Modells** – er erzeugt die B2B2B-Weiterverkaufsbindung, die S05 sonst fehlt (siehe Churn) |
| **Premium-Support Alarm-Triage 24/7** | 690 €/Monat je Betrieb [S] | Bezahltes Team, K.-o. 8 betrifft nur Nico |
| **Erfolgsanteil** | keiner | nicht messbar zuordenbar |

**Ziel-ARPU [S]:** Betrieb mit 120 Anlagen: 390 + (105 × 8,90 = 934) + Predictive 348 +
Endkundenportal 249 = **1.921 €/Monat**. Konservativer Planwert: **1.600 €/Monat** [S].

### 2. Preis-Logik: je überwachter Anlage + Plattformsockel

Identische Struktur wie S03, aber mit einem **3–4× höheren zulässigen Preis je Anlage**.
Begründung, und sie ist rein rechnerisch: Ein Aufzug kostet 500–1.500 €/Jahr Wartung [F], eine
Heizung 180–350 €/Jahr [F]. Der Wert der überwachten Einheit bestimmt den Preis der Überwachung –
nicht die Technik, die in beiden Fällen fast identisch ist. **Das ist die wichtigste Einsicht
aus dem Vergleich S03/S05: Dieselbe Technologie ist im wertvolleren Vertikal viermal so viel wert.**

Die Staffelung ab 100 bzw. 400 Anlagen ist notwendig, weil die Zielgruppe stark
größenheterogen ist (10 bis 800 Anlagen je Betrieb).

### 3. Der zentrale Punkt: Monat 13

**Antwort: Ja – aber mit der schwächsten Beweisführung unter den vier starken Modellen.**

Der laufende Nutzen ist real: jeden Monat werden Störungen erkannt, bevor die Anlage steht.
Aber – und das trennt S05 von S04 – der Nutzen ist eine **Effizienzverbesserung, keine
Pflichterfüllung**. In Monat 13 fragt der Betriebsleiter: *„Wie viele Ausfälle haben wir wirklich
verhindert?"* Das ist eine kontrafaktische Frage und deshalb strukturell schwer zu beantworten.
Man kann nicht zeigen, was nicht passiert ist.

**Die einzige belastbare Antwort ist eine Produktanforderung, keine Verkaufsformulierung:**
Im Onboarding muss eine **Baseline** erhoben werden – Störungseinsätze je Anlage und Jahr,
Erstlösungsquote, mittlere Stillstandszeit, Anteil Notfalleinsätze außerhalb der Regelzeit. Wer
diese Baseline nicht hat, kann Monat 13 nicht gewinnen und wird über den Preis verhandeln müssen.
Mit Baseline lautet der Monatsreport: „Störungseinsätze je Anlage 2,3 → 1,4; Anteil Notfälle
außerhalb Regelzeit 31 % → 12 %." Das ist verteidigbar.

**Der stärkere Monat-13-Anker ist das Endkunden-Portal**, weil der Servicebetrieb es an seine
Objektbetreiber weiterverkauft hat – siehe Kündigungsrisiko.

### 4. Kündigungsrisiko: Was passiert am Tag danach?

**Mit Endkunden-Portal:** Die Objektbetreiber, denen der Servicebetrieb einen „Wartungsvertrag
Premium mit Fernüberwachung und Portalzugang" verkauft hat, verlieren am nächsten Tag ihren
Zugang. Der Servicebetrieb muss 40 Hausverwaltungen erklären, warum die zugesagte Leistung
entfällt. Harter, sofortiger Schmerz.

**Ohne Endkunden-Portal:** Die Sensorik verstummt, der Betrieb fällt auf Reaktivbetrieb zurück.
Unangenehm, aber intern – niemand außerhalb merkt es. Mittlerer Schmerz.

**Churn [S]: 7–11 %/Jahr im Mittel** – mit Endkunden-Portal **5–8 %**, ohne **12–16 %**.
Rechenweg: Der Basis-Churn eines B2B-SaaS mit physischer Hardware liegt niedrig; das
Weiterverkaufsmodul halbiert ihn nochmals. **Architekturkonsequenz: Das Endkunden-Portal darf
kein optionales Modul sein, sondern gehört in jedes Paket ab dem ersten Tag** – notfalls
kostenlos, weil sein Beitrag zur Bindung den Modulpreis übersteigt.

### 5. Wechselkosten und Bindung

| Dimension | Stärke | Konkret |
|---|---|---|
| Daten | hoch | Anlagenhistorie über Fabrikatsgrenzen hinweg – das ist gerade das Alleinstellungsmerkmal |
| Hardware | **hoch, aber mit Einschränkung** | 120 Sensoren in Aufzugsschächten. **Aber der Kunde hat sie gekauft.** Ist die Hardware herstelleroffen, kann ein Wettbewerber sie übernehmen. **Gegenmittel: proprietäre Datenaufbereitung, nicht proprietäre Hardware** – der Wert liegt im Modell, nicht im Sensor |
| Verträge | mittel | 24 Monate |
| Prozessintegration | hoch | Disposition und Technikerplanung arbeiten mit den Meldungen |
| Historie | hoch | ZÜS-Prüfvorbereitung greift auf mehrjährige Daten zu |

### 6. Bruttomarge mit Rechenweg

Basis: 120 Anlagen, ARPU 1.600 €/Monat, Hardware verkauft.

| Kostenposition je Kunde/Monat | Betrag | Herleitung |
|---|---|---|
| SIM/Konnektivität | 72 € | 120 × 0,60 € [S] |
| Cloud/Datenverarbeitung | 42 € | 120 × 0,35 € [S] |
| Plattform je Betrieb | 20 € | [S] |
| Alarm-Triage | 70 € | 2 h × 35 € [S] |
| Fabrikats-/Engineering-Support | 78 € | 1,2 h × 65 € [S] |
| Kundenbetreuung | 52,50 € | 1,5 h × 35 € [S] |
| **Summe** | **334,50 €** | |

**Bruttomarge = (1.600 − 334,50) ÷ 1.600 = 79,1 %** [S]. Konservativ **72–80 %** [S].

Der Posten „Fabrikats-Support" ist die Risikoposition: Jedes neue Fabrikat erzeugt
Engineering-Aufwand, der nicht mit der Kundenzahl skaliert, sondern mit der Fabrikatsvielfalt.
Bei drei Vertikalen (Aufzug, Kälte, Tank) verdreifacht er sich, ohne dass der Umsatz sich
verdreifacht.

### 7. Monatlicher Betreuungsaufwand je Kunde

**4,7 h/Kunde/Monat [S]**. Je 1.000 € Umsatz: **2,94 h** [S].

### 8. Kundenzahl-Tabelle

| Ziel | Servicebetriebe bei 1.600 € ARPU |
|---|---|
| 10.000 € MRR | **7** [S] |
| 30.000 € MRR | **19** [S] |
| 100.000 €/Monat | **63** [S] |
| 190.000 €/Monat | **119** [S] |

Hardware-Umsatz zusätzlich, **kein MRR**: 169 € Marge × 120 Anlagen = 20.280 € je Neukunde
einmalig [S]. Bei 3 Neukunden/Monat = 60.840 €/Monat – **dieser Posten ist gefährlich groß.**
Bei unsauberer Darstellung sähe S05 in Monat 24 nach 150.000 €/Monat aus, wovon 40 % einmaliger
Hardwareumsatz wäre. Die MRR-Quote muss getrennt ausgewiesen werden, sonst verletzt das Modell
faktisch die 60-%-Vorgabe, während es sie auf dem Papier erfüllt.

### 9. In 24 Monaten akquirierbar?

Abschlussrate **1,3 je Vertriebs-FTE-Monat** [S] – technischer Verkauf, Pilotphase mit 10 Anlagen
üblich, Zyklus 3–6 Monate.

- 48 × 1,3 = **62 Abschlüsse** brutto
- − Churn (9 %) = −5
- − Ramp-Abschlag = −6
- = **~51 aktive Kunden in Monat 24 → 81.600 € MRR** [S]

**100.000 €: KNAPP NEIN in 24 Monaten** – **Monat 27–30** [S].
**190.000 €: NEIN** – **Monat 40+** [S].

**Ungelöste Spannung im Modell, die die Erlösarchitektur betrifft:** Aufzug, Kälte und Tank sind
drei verschiedene Verkaufsprozesse mit drei verschiedenen Sensorik-Stacks und drei verschiedenen
Normwelten. **Ein Vertikal allein hat in DE zu wenige Kunden** (freie Aufzugswartung: einige
hundert Betriebe [A]), **drei Vertikale kosten dreifachen Engineering-Aufwand** und drücken die
Marge über den Fabrikats-Support-Posten. Diese Frage muss vor dem Preismodell entschieden werden,
nicht danach.

---

## S06 — Prüf-SaaS, das aus dem Mangel ein Angebot macht

### 1. Erlösbausteine einzeln

| Baustein | Preis | Begründung / Anker |
|---|---|---|
| **Setup / Implementierung** | **4.900 €** einmalig [S] | Prüfformular-Konfiguration je Gewerk, Stammdatenmigration, Angebotsvorlagen, Artikelstammverknüpfung, Schulung. Anker: DSB-Markt „ab 3.000 € Initialaufwand" [F]; FoxifAI 1.920 € [F-sek]. Hier höher, weil Formular- und Artikelstammarbeit real **40–60 h** ist [S]: 50 h × 55 € = 2.750 € → **44 % Setup-Marge** |
| **Monatsgrundgebühr je Mandant** | **349 €/Monat** (Backoffice-Nutzer unbegrenzt) [S] | Bewusst unbegrenzte Büronutzer – wir wollen, dass Disposition, Buchhaltung und Vertrieb im System arbeiten, weil jeder eine Wechselhürde ist |
| **Nutzungsgebühr je Prüfer/Techniker** | **129 €/Prüfer/Monat** [S] | Der Kernpreis. Anker: **Rilla 199–349 $/Rep/Monat** [F-sek] ≈ 183–321 € – der internationale Beleg, dass ein Außendienst-Kopfpreis in dieser Höhe zahlbar ist, **wenn er Umsatz erzeugt**. Deutsche Handwerkersoftware liegt bei 15–120 €/Nutzer [F]. 129 € liegt oberhalb des deutschen Bandes und deutlich unter Rilla. Kundenrechnung: ein Prüfer erzeugt bei 15 Prüfungen/Woche und 2,3 Mängeln je Prüfung ≈ **150 Mängel/Monat**; bei 25 % Angebotskonversion und 180 € Ø-Auftragswert [S, abgeleitet aus DGUV-V3-Band 150–350 € [F]] = **6.750 €/Monat Zusatzumsatz**. 129 € = **1,9 % davon** |
| **Zusatzmodul Angebotsversand + Nachfassanruf** | 199 €/Monat [S] | Der CallSuite-Anschluss: das automatisch erzeugte Angebot wird nachtelefoniert. Genau der Schritt, der die Konversion von 25 % auf 35–40 % hebt [A] |
| **Zusatzmodul Kundenportal für Objektbetreiber** | 149 €/Monat [S] | B2B2B-Weiterverkauf, gleiche Bindungslogik wie S05 |
| **Zusatzmodul Fälligkeits-/Terminierung** | **449 €/Monat** [S] | **Das ist S02 als Modul.** Wichtigster struktureller Befund zur Erlösarchitektur: S02 und S06 verkaufen an dieselbe Zielgruppe und lassen sich zu einem Produkt mit zwei Einstiegspunkten bündeln |
| **Zusatzmodul Normtext-Bibliothek** | 99 €/Monat [S] | Weiterverrechnung der DIN-Lizenz mit Aufschlag |
| **Premium-Support** | 249 €/Monat [S] | |
| **Hardware** | keine (BYOD-Tablets) | bewusst |
| **Erfolgsanteil** | **1,5 %** des über die Plattform angenommenen Mängelauftragsvolumens [S] – **nur als Alternative** zum Prüferpreis, nie zusätzlich | Argument: risikofrei für den Kunden, gut als Einstiegsvariante in den ersten 6 Monaten. Nachteil: Abrechnungstransparenz nötig, Umsatzvolatilität, und der Kunde lernt, seine Aufträge am System vorbeizuführen. Danach Umstellung auf Kopfpreis |

**Ziel-ARPU [S]:** Betrieb mit 6 Prüfern: 349 + (6 × 129 = 774) + 199 + 99 = **1.421 €/Monat**.
Konservativer Planwert: **1.300 €/Monat** [S]. Mit Terminierungsmodul: 1.870 €.

### 2. Preis-Logik: je Prüfer im Außendienst

- **Je Prüfer** ist die richtige Metrik, weil sie **mit dem Nutzen skaliert**: mehr Prüfer =
  mehr Prüfungen = mehr Mängel = mehr Angebote = mehr Zusatzumsatz. Der Kunde bezahlt genau in
  der Währung, in der er profitiert.
- Sie ist **marktbelegt** – Rilla verkauft exakt so [F-sek] und erreicht damit 51 Mio. $ ARR bei
  NRR > 115 % [F-sek]. Die Kopfpreis-Logik ist der Grund für die NRR über 100 %: Stellt der
  Kunde einen Prüfer ein, wächst unser Umsatz automatisch.
- **Je Objekt wäre falsch**, weil der Prüfdienstleister die Objekte nicht besitzt und ihre Zahl
  nicht steuert.
- **Je Prüfung wäre falsch**, weil es die Nutzung des Systems bestraft – Prüfer würden
  Prüfungen außerhalb des Systems dokumentieren.
- **Die unbegrenzten Büronutzer sind kein Verschenken, sondern Strategie**: Sie erzeugen
  Wechselhürden zum Nulltarif.

### 3. Der zentrale Punkt: Monat 13

**Antwort: Ja – die zweitstärkste Begründung der Liste, aus zwei sich verstärkenden Quellen.**

**(a) Der Umsatzstrom.** Monatsreport: „148 Mängel dokumentiert, 122 Angebote automatisch erzeugt,
34 angenommen, 6.120 € Auftragsvolumen." Diese Zahl kann der Betrieb in seiner eigenen
Buchhaltung nachvollziehen. Sie fällt in Monat 13 nicht weg – sie ist der Regelbetrieb. Das ist
Befund 4 in Reinform: **wir verkaufen Mehrumsatz, nicht gesparte Bürostunden.**

**(b) Systemsoftware-Charakter.** Nach 13 Monaten liegt die gesamte Prüfhistorie im System. Die
gesetzlichen Nachweispflichten des Betriebs (DIN 14675, DGUV V3, PrüfVO der Länder) sind ohne
das System nicht mehr erfüllbar, weil die Vorprüfungen dort dokumentiert sind. Der Betrieb kann
nicht aufhören zu zahlen und weiterarbeiten.

Diese Kombination – **Umsatzargument plus Pflichtargument** – hat kein anderes der acht Modelle
in dieser Stärke.

### 4. Kündigungsrisiko: Was passiert am Tag danach?

Am nächsten Morgen haben 6 Prüfer kein Formular mehr auf dem Tablet. Sie fahren mit Papier los.
Die Angebotsmaschine steht. Die Prüfhistorie der letzten 13 Monate ist exportierbar – aber als
PDF-Stapel unbrauchbar, weil nicht durchsuchbar und nicht an Objekte gebunden.
**Sofortiger operativer Stillstand im Kerngeschäft.** Der härteste Schmerz nach S04, und im
Gegensatz zu S04 ohne Ausweichmöglichkeit auf einen gleichwertigen Anbieter, weil das Produkt
in DE so nicht existiert.

**Churn [S]: 5–8 %/Jahr.** Rechenweg: Systemsoftware im B2B-Mittelstand liegt typisch bei
4–8 %/Jahr Logo-Churn [A]; das Umsatzargument drückt zusätzlich. Vergleichsanker: Rilla erreicht
**NRR > 115 %** [F-sek] – in derselben Produktkategorie expandiert der Bestand sogar, statt zu
schrumpfen. Realistische Kündigungsanlässe: Betriebsaufgabe, Übernahme, Insolvenz.

### 5. Wechselkosten und Bindung

| Dimension | Stärke | Konkret |
|---|---|---|
| Daten | **sehr hoch** | Objektstamm, Prüfhistorie, Mängelverfolgung, Artikelstamm, Angebotsvorlagen |
| Hardware | keine | — |
| Verträge | hoch | 24–36 Monate bei Systemsoftware üblich |
| Prozessintegration | **sehr hoch** | Der gesamte Auftragsdurchlauf – Prüfung, Mangel, Angebot, Rechnung – läuft durch das System |
| Historie | **sehr hoch** | Migration realistisch **12–20 Wochen** [S], inklusive Neuschulung von 6–40 Prüfern |

### 6. Bruttomarge mit Rechenweg

Basis: ARPU 1.300 €/Monat, 80 Kunden im Bestand.

| Kostenposition je Kunde/Monat | Betrag | Herleitung |
|---|---|---|
| Hosting / Mobile-Backend | 22 € | [S] |
| DIN-/VDE-Normlizenz anteilig | 45 € | **[A] – der Unsicherheitsposten.** Belegt ist: DIN Media lizenziert Normen für Softwareimplementierung ausdrücklich, nur Lesezugriff, Jahreslizenz, Preis individuell kalkuliert und jährlich angepasst [F, support.dinmedia.de / dinmedia.de-Preisliste, 2026-08]. Angenommene Grundlizenz 25.000–60.000 €/Jahr ÷ 80 Kunden ÷ 12 = 26–63 €; Mittelwert 45 € |
| Support / Kundenerfolg | 56 € | 1,6 h × 35 € [S] |
| Formularpflege bei Normänderungen | 90 € | 1 Fachkraft 86.300 €/Jahr ÷ 12 = 7.192 € ÷ 80 Kunden [S] |
| **Summe** | **213 €** | |

**Bruttomarge = (1.300 − 213) ÷ 1.300 = 83,6 %** [S].
Sensitivität bei doppelter DIN-Lizenz (90 €/Kunde): **80,1 %** [S]. Auch im ungünstigen Fall
komfortabel über Kriterium 2.

**Die DIN-Lizenz ist der einzige echte Margen-Unsicherheitsfaktor – und gleichzeitig der
Burggraben.** Sie muss **vor** dem Produktbau als konkretes Angebot eingeholt werden. Wer sie
hat, hat ein Produkt, das ohne Lizenz nicht kopierbar ist.

### 7. Monatlicher Betreuungsaufwand je Kunde

**2,2 h/Kunde/Monat [S]**. Je 1.000 € Umsatz: **1,69 h** [S] – der drittbeste Wert.

### 8. Kundenzahl-Tabelle

| Ziel | Prüfbetriebe bei 1.300 € ARPU | mit Terminierungsmodul (1.870 €) |
|---|---|---|
| 10.000 € MRR | **8** [S] | 6 |
| 30.000 € MRR | **24** [S] | 17 |
| 100.000 €/Monat | **77** [S] | 54 |
| 190.000 €/Monat | **147** [S] | **102** |

Der Sprung von 147 auf 102 durch ein einziges Modul zeigt, wie stark die Bündelung von S02 und
S06 wirkt. Das ist der wichtigste Hebel im ganzen Dokument.

### 9. In 24 Monaten akquirierbar?

**Hier fällt S06 durch – aber nicht am Vertrieb.**

Vertriebsseite: Systemsoftware-Wechsel ist ein Entscheidungsprozess von **4–9 Monaten** [S], und
der Betrieb wechselt nur, wenn sein Altsystem schmerzt. Abschlussrate **1,0 je Vertriebs-FTE-Monat** [S].
48 × 1,0 = 48 Kunden − Churn − Ramp = **~42 aktive → 54.600 € MRR in Monat 24** [S].

**Der eigentliche K.-o. steht davor:** Eine Prüf-Systemsoftware mit Mobil-App, Formularmotor,
Angebotsmaschine, Artikelstamm und ERP-Schnittstellen ist ein **12–18-Monats-Bauvorhaben mit
3–5 Entwicklern** [S] = **450.000–900.000 € Vorleistung**, bevor der erste Euro fließt. Unter
Annahme A10 (kein VC) ist das nur aus dem Cashflow eines anderen Modells finanzierbar.

**100.000 €: NEIN in 24 Monaten** – realistisch **Monat 34–40** [S], gerechnet ab Bauentscheidung.
**190.000 €: NEIN** – Monat 48+ [S].

**Ehrliches Gesamturteil zu S06: das beste Modell dieser Liste auf Sicht von 48 Monaten und das
schlechteste auf Sicht von 24.** Es ist der klassische Fall, in dem ein Modell nicht wegen
seiner Erlösarchitektur scheitert, sondern wegen ihrer Anlaufzeit.

---

## S08 — Monitoring-as-a-Service mit B2B2B-Zahler (HACCP / Kühlkette / Silo)

### 1. Erlösbausteine einzeln

| Baustein | Preis | Begründung / Anker |
|---|---|---|
| **Setup Rahmenvertrag** | **3.500 €** einmalig je Kettenkunde [S] | Alarmierungsmatrix, Eskalationsketten, Schnittstelle zur QM-Software der Zentrale, Schulung der Regionalleiter |
| **Setup je Standort** | **149 €** einmalig [S] | Anker: NSL-Einrichtung 89–150 € je Aufschaltpunkt [F, 2026-08] – vergleichbarer Vorgang. Bei 80 Filialen = 11.920 € plus 3.500 € = **15.420 € Setup bei Vertragsschluss** |
| **Monatsgrundgebühr je Rahmenvertrag** | **490 €/Monat** [S] | Zentral-Dashboard, Filialvergleich, Auditreport, QM-Export. **Diesen Baustein haben die Wettbewerber nicht** – Sencono, DIE HACCP APP und PSsystec verkaufen je Sensor an den Einzelstandort und haben kein Zentralprodukt [F, 2026-08] |
| **Nutzungsgebühr je Messstelle** | **7,90 €/Monat** inkl. Hardware-Nutzung [S] | Anker, alle neu belegt 2026-08: **Sencono 4,95 €** Full-Service-Flatrate inkl. Gerätemiete [F], **DIE HACCP APP 5,00 €** [F], **PSsystec 8,00 €** nur Konnektivität [F]. Wir liegen **60 % über Sencono** – das muss hart gerechtfertigt sein: (a) **Alarm per Anruf statt E-Mail**, (b) Zentral-Reporting über alle Filialen, (c) Eskalationskette mit Quittierungspflicht, (d) automatischer IFS/BRC-Auditbericht. **Ehrlicher Hinweis: Wer nur Temperaturkurven will, kauft für 4,95 €. Unser Produkt muss die Alarmkette sein, nicht der Sensor** |
| **Zusatzmodul Sprachalarm-Eskalation** | 1,90 €/Messstelle/Monat [S] | Der CallSuite-Differenzierer aus der Shortlist, separat bepreist und damit verkaufbar |
| **Zusatzmodul Tür/Feuchte/CO₂** | 4,90 €/Messstelle/Monat [S] | zusätzliche Sensorik, zusätzlicher Wert |
| **Zusatzmodul Reinigungs-/Checklisten** | 29 €/Standort/Monat [S] | HACCP-Eigenkontrolle ist mehr als Temperatur |
| **Zusatzmodul IFS/BRC-Auditpaket** | 199 €/Monat je Rahmenvertrag [S] | reine Software, ~97 % Marge |
| **Premium-Support 24/7-Alarmhotline mit Erstintervention** | **890 €/Monat** je Rahmenvertrag [S] | Wir nehmen den Alarm nachts an, arbeiten die Eskalationskette ab, dokumentieren. Margenstärkster Baustein, braucht ein bezahltes Team – K.-o. 8 betrifft nur Nico |
| **Hardware** | **Verkauf an die Zentrale: 129 €** je Messstelle (Einkauf 60 € [A]) + Gateway 249 € je Standort | **Architekturentscheidung mit Rechenweg:** Bei Miete nach Sencono-Vorbild bindet eine Kette mit 80 Filialen à 6 Messstellen 480 × 60 € + 80 × 120 € = **38.400 € Kapital**. Bei 20 Kettenkunden = **768.000 €** [S]. Unter Annahme A10 nicht darstellbar → Verkauf, dafür reduzierte Servicegebühr **5,90 €** statt 7,90 € wählbar |
| **Erfolgsanteil** | keiner | |

**Beispielkunde (Kette, 80 Filialen × 6 Messstellen = 480):**
490 + (480 × 7,90 = 3.792) + Sprachalarm (480 × 1,90 = 912) + Auditpaket 199 + 24/7 890 =
**6.283 €/Monat** [S].
**Ziel-ARPU über den Mix (Ø 55 Filialen): 3.800 €/Monat je Rahmenvertrag** [S].

### 2. Preis-Logik: je Messstelle, abgerechnet gegen die Zentrale

Das ist – zusammen mit S04 – die überlegene Preislogik, und aus denselben Gründen:

- **Branchennorm**: Der gesamte Markt rechnet je Messstelle ab [F: Sencono, DIE HACCP APP,
  PSsystec, alle 2026-08]. Wir müssen die Einheit nicht erklären.
- **Kostenkongruent**: jede Messstelle kostet SIM, Cloud, Gerätevorhaltung.
- **Multiplikationsfähig beim Zahler**: Die Zentrale hat 80 Filialen. Eine Verhandlung erzeugt
  480 Abrechnungseinheiten. **Das ist Muster 2 aus A01 – der Zahler ist nicht der Nutzer – und
  es löst Kriterium 5 strukturell**, nicht durch Preiserhöhung, sondern durch Zählerwechsel.
- **Wächst ohne Neuverkauf**: Eröffnet die Kette 12 neue Filialen, steigt unser Umsatz um
  ~570 €/Monat, ohne dass ein Vertriebler tätig wird.
- **Je Standort wäre gröber** und würde bei Filialen mit 2 Kühlstellen zu teuer und bei 20 zu
  billig sein – man verlöre entweder die kleinen oder die großen Standorte.

### 3. Der zentrale Punkt: Monat 13

**Antwort: Ja – aus drei unabhängigen Quellen, damit die belastbarste Begründung nach S04.**

**(a) Pflicht.** HACCP verlangt lückenlose Temperaturdokumentation; IFS/BRC-Audits prüfen sie
jährlich. Ein Monat ohne Aufzeichnung ist ein Auditbefund. Diese Pflicht besteht in Monat 13
unverändert.

**(b) Verderbschaden, laufend.** Ein nicht bemerkter Kühlausfall über Nacht kostet in einer
Filiale **3.000–15.000 € Warenwert** [A]. Bei 80 Filialen ist das statistisch mehrfach im Jahr.
Gegenrechnung: 6.283 €/Monat = **75.400 €/Jahr** gegen 10–25 verhinderte Ausfälle à 3.000–15.000 €
= **30.000–375.000 €** [S]. Das ist eine Rechnung, die der Einkauf der Zentrale selbst aufmacht.

**(c) Das Steuerungsinstrument wird mit der Zeit wertvoller, nicht weniger.** In Monat 13 sieht
die Zentrale zum ersten Mal einen **Jahresvergleich der Kühlkettenabweichungen je Filiale** –
welche Filiale hat systematisch Probleme, welches Gerät fällt wiederholt aus, welcher
Regionalleiter reagiert langsam. Diese Auswertung existiert in Monat 1 nicht und in Monat 13
zum ersten Mal. **Der Nutzen steigt mit der Vertragsdauer** – das ist die stärkste denkbare
Form der Monat-13-Begründung.

**Nachweisbarkeit: sehr hoch, weil ereignisbasiert.** „Am 14.03. um 02:41 Uhr Alarm Filiale
Bremen-Nord, um 02:44 Uhr Anruf Marktleiter, um 03:12 Uhr Techniker vor Ort, Ware gerettet,
geschätzter Warenwert 6.400 €." Das ist ein Beleg, kein Versprechen.

### 4. Kündigungsrisiko: Was passiert am Tag danach?

Die Kühlkettendokumentation bricht ab. Beim nächsten IFS-/BRC-Audit fehlen Aufzeichnungen →
Abwertung oder Zertifikatsverlust → der Handelspartner listet aus. Für einen Lieferanten oder
eine Kette ist das ein **existenzielles** Risiko, kein betriebswirtschaftliches.

Der Schmerz ist allerdings **verzögert** (bis zum Jahresaudit) – das ist die einzige Schwäche
in dieser Position. Kompensiert wird sie durch den physischen Aufwand: Ein Wechsel bedeutet, in
**80 Filialen** Hardware abzubauen und neue zu installieren, die Alarmierungsmatrix neu
aufzubauen und 80 Filialleiter neu zu schulen – ein Rollout-Projekt von 4–8 Monaten [S].

**Churn [S]: 4–7 %/Jahr.** Rechenweg: Rahmenverträge mit Ketten laufen 36 Monate [A]; der
Wechselaufwand ist ein Filialrollout; die Pflicht besteht unabhängig vom Anbieter (Befund 3).
Gegenläufig: Preisdruck durch den 4,95-€-Wettbewerb bei Vertragsverlängerung – das ist der
realistische Kündigungsanlass und der Grund, warum die margenstarken Zentralmodule nicht
verzichtbar sind.

### 5. Wechselkosten und Bindung

| Dimension | Stärke | Konkret |
|---|---|---|
| Daten | **sehr hoch** | Mehrjährige Temperaturhistorie ist Auditmaterial; sie muss aufbewahrt werden und ist nur in unserem System auswertbar |
| Hardware | **sehr hoch** | 480 Geräte in 80 Filialen |
| Verträge | **sehr hoch** | 36-Monats-Rahmenverträge, oft an Lieferantenauflagen gekoppelt |
| Prozessintegration | **sehr hoch** | Alarmierungsmatrix und Eskalationskette sind in der QM-Dokumentation der Kette verankert; Schnittstelle zur QM-Software der Zentrale |
| Historie | **sehr hoch** | Der Filialvergleich über Jahre ist ein Steuerungsinstrument, das nicht mitgenommen werden kann |

### 6. Bruttomarge mit Rechenweg

Basis: 480 Messstellen, Umsatz 6.283 €/Monat, Hardware **verkauft**.

| Kostenposition je Kunde/Monat | Betrag | Herleitung |
|---|---|---|
| SIM/Konnektivität | 264 € | 480 × 0,55 € [S] |
| Cloud/Datenhaltung | 96 € | 480 × 0,20 € [S] |
| Zentral-Dashboard | 35 € | [S] |
| Sprachalarm-Minuten | 14 € | ~40 Alarme × 3 Min × 0,12 € [S] |
| 24/7-Alarmdienst anteilig | 720 € | 3-Personen-Schichtteam 18.000 €/Monat ÷ 25 Rahmenverträge [S] |
| Kundenbetreuung | 140 € | 4 h × 35 € [S] |
| Ersatzgeräte / Ausfallquote | 72 € | 3 %/Jahr × 480 × 60 € ÷ 12 [S] |
| **Summe** | **1.341 €** | |

**Bruttomarge = (6.283 − 1.341) ÷ 6.283 = 78,7 %** [S].
**Sensitivität Hardware-Miete:** +480 × (60 € ÷ 36) = +800 € → **66,0 %** [S]. Miete kostet
**13 Margenpunkte plus 768.000 € Kapital** – die Verkaufsvariante ist damit ohne Alternative.

### 7. Monatlicher Betreuungsaufwand je Kunde

**4,0 h/Rahmenvertrag/Monat [S]** aktive Betreuung (der 24/7-Dienst ist separat als Kostenposition
kalkuliert). Je 1.000 € Umsatz: **1,05 h** [S] – **der beste Wert der gesamten Liste.**

### 8. Kundenzahl-Tabelle

| Ziel | Rahmenverträge bei 3.800 € ARPU | Messstellen gesamt [S] |
|---|---|---|
| 10.000 € MRR | **3** [S] | ~1.300 |
| 30.000 € MRR | **8** [S] | ~3.800 |
| 100.000 €/Monat | **27** [S] | ~12.700 |
| 190.000 €/Monat | **50** [S] | **~24.000** |

**Das ist die beste Zahl des gesamten Dokuments: 50 Kunden für das echte Ziel.**
Zum Vergleich: S13 braucht 594, S03 braucht 280.

Setup- und Hardwareumsatz zusätzlich, **kein MRR**: je Neukunde 15.420 € Setup + (480 × 69 € =
33.120 €) Hardwaremarge = **48.540 € einmalig** [S]. Bei 1 Neukunde/Monat sind das 48.540 €/Monat
zusätzlicher Umsatz – der bei Wachstumsstopp wegfällt und getrennt ausgewiesen werden muss.

### 9. In 24 Monaten akquirierbar?

Zielkunden: Filialisten – Bäckerei- und Metzgereiketten, Supermarktkooperationen,
Systemgastronomie, Pharmagroßhandel, Lebensmittellogistiker, Lieferanten mit Auflagen gegenüber
dem Handel.
Verkaufszyklus an eine Zentrale: **6–14 Monate** [S]. Entscheidergremium aus QM-Leitung, Einkauf
und IT. Pilotphase mit 5 Filialen üblich. Abschlussrate **0,45 je Vertriebs-FTE-Monat** [S] –
die niedrigste der acht Modelle.

- 48 × 0,45 = **21,6 Rahmenverträge** brutto
- − Churn (5 %) = −1
- − Ramp-Abschlag = −3
- = **~18 aktive Rahmenverträge in Monat 24 → 68.400 € MRR** [S]

**100.000 €: KNAPP NEIN in 24 Monaten** – **Monat 28–31** [S].
**190.000 €: NEIN** – **Monat 40–46** [S].

**Aber – und das ist bei S08 wichtiger als bei jedem anderen Modell – die Varianz nach oben ist
gewaltig.** Eine einzige Supermarktkooperation mit 600 Filialen à 8 Messstellen = 4.800
Messstellen = **38.400 €/Monat aus einem einzigen Abschluss** [S], plus ~420.000 € Setup und
Hardware. Zwei bis drei solche Logos erreichen das 100.000-€-Ziel allein.

**Bei S08 entscheidet nicht die Vertriebsmenge, sondern ob 2–3 große Logos gewonnen werden.**
Das ist ein anderes Vertriebsspiel als bei allen anderen Modellen – und es ist genau das Spiel,
das zu Nicos belegtem Stärkenprofil passt (verkaufen, präsentieren, überzeugen, große
Entscheidungen), statt zu einer Inside-Sales-Organisation, die Befund 1 ausschließt.

---

## S13 — Vertikaler Voice-Agent mit Tiefenintegration

### 1. Erlösbausteine einzeln

| Baustein | Preis | Begründung / Anker |
|---|---|---|
| **Setup / Vertikalintegration** | **2.400 €** einmalig [S] | Anker: **FoxifAI 1.920 € Setup + ab 100 €/Monat** [F-sek] – der einzige belegte Beweis, dass deutsche KMU eine vierstellige Setup-Gebühr für Voice akzeptieren. 2.400 € für tiefere Integration (Kalender, ERP, Warenwirtschaft, branchenspezifische Gesprächslogik) |
| **Monatsgrundgebühr** | **249 €/Monat** je Standort inkl. 750 Minuten [S] | Anker: DACH-Band **29–299 €**, Kernband 69–199 €, Ausreißer bis 499 € [F]; fonio Team 299 € [F]; Superchat Professional 129 € [F]. **249 € liegt bereits am oberen Rand des existierenden Bandes** – viel Luft nach oben gibt es nicht |
| **Nutzungsgebühr** | 0,29 €/Min über Kontingent [S] | Anker: Markt 0,10–0,28 €/Min [F], fonio konkret 0,12–0,15 € [F], KI-Vollkosten 0,10–0,12 € [S]. Bei 0,29 € läge die Marge auf der Zusatzminute bei 59–66 % |
| **Zusatzmodule** | zusätzliche Rufnummer 7 €, WhatsApp 79 €, Outbound-Terminierung 199 €, CRM-Rückschreibung 99 € [S] | Direkt von fonio übernommen: „Zusatzfeatures 5–79 €/Feature/Monat, zusätzliche Rufnummer 7 €, WhatsApp 79 €" [F]. **Die Übernahme fremder Modulpreise ist selbst ein Warnsignal: Es gibt in dieser Kategorie keine eigene Preissetzungsmacht** |
| **Premium-Support** | 149 €/Monat [S] | |
| **Hardware** | keine | |
| **Erfolgsanteil** | **4,90 € je gebuchtem Termin** [S] | Der einzige Baustein, der die Preisvergleichbarkeit durchbricht – und deshalb der einzige, der überhaupt verteidigt werden kann |

**Ziel-ARPU:** rechnerisch 249 + 58 (200 Zusatzminuten) + 199 (ein Modul) = 506 €/Monat.
**Realistisch im DACH-Markt nach Rabattierung: 320 €/Monat** [S]. Belegter Kontext:
„DACH-Preisband bereits 29–299 € mit Rabattschlacht" [aus 13_shortlist].

### 2. Preis-Logik: je Rufnummer/Standort + Minutenpaket

**Das ist die Branchenlogik und genau das Problem.** Sie ist vollständig vergleichbar: Jeder
Interessent kann drei Angebote nebeneinanderlegen und Minutenpreise dividieren. In einer
Kategorie mit über einem Dutzend Anbietern, Telko-Bundling (Telekom integriert den Assistenten
ins Netz, Placetel verkauft die KI-Rufnummer für 9 €/Monat [F]) und ERP-Bundling (Label Software
liefert den Assistenten mit [F]) führt vollständige Vergleichbarkeit in genau eine Richtung.

Die **einzige Rettung wäre die Umstellung auf Outcome-Abrechnung** – je terminiertem Vorgang
statt je Minute. Damit wäre S13 aber kein eigenes Modell mehr, sondern S02.

### 3. Der zentrale Punkt: Monat 13

**Antwort: Ja, der Nutzen existiert – aber die Antwort hilft nicht, und das ist ein qualitativ
anderer Befund als bei den übrigen sieben.**

Der Agent nimmt in Monat 13 Anrufe an wie in Monat 1. Es gibt kein Nutzenproblem.
**S13 hat ein Preisproblem, kein Nutzenproblem** – und für die Erlösarchitektur ist das genauso
tödlich.

In Monat 13 bekommt der Kunde ein Angebot über 79 €/Monat für dieselbe Leistung, oder seine
Telefonanlage liefert sie mit. Der Nutzen rechtfertigt **eine** Monatsgebühr – aber nicht
**diese** Monatsgebühr. Bei jeder Verlängerung wird neu verhandelt, und die Richtung steht fest.

**Die einzige Konstellation, in der S13 in Monat 13 verteidigbar ist:** wenn der Agent so tief
in ein Vertikal-ERP integriert ist, dass er **Aufträge auslöst** statt Nachrichten aufzunehmen –
Termin im Dispositionssystem, Auftrag im Warenwirtschaftssystem, Rückfrage an den richtigen
Techniker. Dann wird er Systemsoftware, die Preisvergleichbarkeit bricht, und der Churn fällt.
**Aber dann ist S13 kein eigenständiges Modell mehr, sondern ein Modul von S02 oder S06** – und
genau so sollte es behandelt werden.

### 4. Kündigungsrisiko: Was passiert am Tag danach?

Die Anrufe gehen wieder an den Anrufbeantworter oder klingeln durch. Unangenehm – aber ohne
Substanzverlust. Der Zustand von vor 13 Monaten kehrt zurück, und der war erträglich, sonst
hätte der Kunde nicht 13 Monate ohne Assistenten überlebt. Er verliert **keine** Daten, **keine**
Historie von Wert, **keine** Pflichterfüllung, **keine** Zusage gegenüber seinen eigenen Kunden.
Die Rufnummer gehört ihm.

**Das ist der schwächste Kündigungsschmerz der acht Modelle – mit Abstand.**

**Churn [S]: 25–40 %/Jahr.** Rechenweg: Horizontales KMU-SaaS unter 300 € ARPU liegt typisch bei
2–4 % Logo-Churn pro **Monat** [A] = 22–39 %/Jahr. Hinzu kommen hier Preisdruck von unten
(Placetel 9 €/Monat [F]) und Bundling von oben (Telekom im Netz, ERP-Hersteller inklusive [F]).
Bei 30 % Jahres-Churn muss jährlich ein Drittel des Bestands neu verkauft werden, **nur um
stillzustehen**.

### 5. Wechselkosten und Bindung

| Dimension | Stärke |
|---|---|
| Daten | **sehr niedrig** – Gesprächsprotokolle ohne Weiterverwendungswert |
| Hardware | keine |
| Verträge | niedrig – Monats- bis 12-Monats-Laufzeiten sind Marktstandard in dieser Kategorie [F-Kontext] |
| Prozessintegration | niedrig in der Basisvariante |
| Historie | **keine** |

Einziger Aufwand beim Wechsel: Rufnummernportierung – und die ist gesetzlich erleichtert.

### 6. Bruttomarge mit Rechenweg — **der harte Befund**

Basis: ARPU 320 €/Monat, tatsächliche Nutzung 950 Minuten.

| Kostenposition je Kunde/Monat | Betrag | Herleitung |
|---|---|---|
| Voice-Plattform (LLM + TTS + STT + Telefonie) | 104,50 € | 950 Min × 0,11 € [S; Vollkosten belegt 0,10–0,12 €/Min] |
| Rufnummer/Trunk | 3 € | [S] |
| Hosting/Orchestrierung | 6 € | [S] |
| Support | 28 € | 0,8 h × 35 € [S] |
| Prompt-/Skriptpflege | 19,20 € | 0,4 h × 48 € [S] |
| **Summe** | **160,70 €** | |

**Bruttomarge = (320 − 160,70) ÷ 320 = 49,8 %** [S].

**Das ist der entscheidende Befund zu S13 und er korrigiert die Shortlist.** Dort stehen
60–80 % – diese gelten nur bei **geringer** Minutennutzung. Genau das ist der belegte
fonio-Befund: „verkauft bei Vollausschöpfung **unter** den eigenen Plattformkosten" [F];
fonio Solo = 0,099 €/Min bei Vollausschöpfung gegen 0,10–0,12 € Vollkosten [S].

**Das Modell verdient nur an Kunden, die es nicht nutzen.** Das ist strukturell instabil, weil
genau diese Kunden kündigen – sie sehen keinen Nutzen. Die Kunden, die bleiben, sind die
unprofitablen. Eine Erlösarchitektur, deren Deckungsbeitrag negativ mit der Kundenzufriedenheit
korreliert, ist keine Erlösarchitektur.

Bei 49,8 % liegt S13 nur knapp über K.-o. 5 (< 45 %) und weit unter Kriterium 2 (≥ 65 %).

### 7. Monatlicher Betreuungsaufwand je Kunde

**1,2 h/Kunde/Monat [S]** – absolut der niedrigste Wert.
Je 1.000 € Umsatz: **3,75 h** [S] – **der schlechteste Wert der Liste**, weil der Umsatz so klein ist.

### 8. Kundenzahl-Tabelle

| Ziel | Kunden bei 320 € ARPU | zu verkaufen bei 30 % Churn (24 Monate) |
|---|---|---|
| 10.000 € MRR | **32** [S] | ~42 |
| 30.000 € MRR | **94** [S] | ~125 |
| 100.000 €/Monat | **313** [S] | **~415** |
| 190.000 €/Monat | **594** [S] | **~790** |

### 9. In 24 Monaten akquirierbar?

Um 313 aktive Kunden zu halten, müssen bei 30 % Churn in 24 Monaten **~415 verkauft** werden.
Bei 48 Vertriebs-FTE-Monaten entspricht das **8,6 Abschlüssen je FTE-Monat** bei einem
320-€-Ticket mit 2.400 € Setup.

Das ist für einen beratenden Verkauf mit Integrationsaufwand unrealistisch. Es funktioniert nur
mit Self-Service/Product-Led-Growth (dann fällt aber die Setup-Gebühr weg, und damit die
Deckung der Akquisekosten) oder mit einem **10–20-köpfigen Inside-Sales-Team** – exakt die
Struktur, die Befund 1 unter Annahme A10 ausschließt und für die plancraft 50 Mio. € eingesammelt hat.

**100.000 €: NEIN. 190.000 €: NEIN.** Unter Annahme A10 in keinem Zeithorizont mit dieser
Erlösarchitektur erreichbar.

---

# QUERAUSWERTUNG

## Q1. Rangliste der 8 Modelle nach Qualität der Erlösarchitektur

Bewertet werden **ausschließlich Eigenschaften der Erlösarchitektur** – nicht Persönlichkeits-Fit,
nicht Marktgröße, nicht Regulatorik. Gewichtung:

| Dimension | Gewicht | Warum |
|---|---|---|
| Monat-13-Begründung | 30 % | Die Kernfrage des Auftrags |
| Churn-Struktur / Kündigungsschmerz | 20 % | Bestimmt, ob MRR hält |
| Preispunkt-Arithmetik (Kunden für 190.000 €) | 20 % | Befund 1: entscheidet vor jeder Produktfrage |
| Bruttomarge | 15 % | Kriterium 2 / K.-o. 5 |
| Betreuungsstunden je 1.000 € Umsatz | 10 % | Bestimmt Teamgröße und Delegierbarkeit |
| Kriterium 18 (Setup + Monatsvertrag) | 5 % | Soll-Kriterium, deckt CAC |

| Rang | Modell | M13 | Churn | Arithm. | Marge | Aufwand | K18 | **Score** |
|---|---|---|---|---|---|---|---|---|
| **1** | **S08** Monitoring B2B2B (HACCP) | 9 | 9,5 | 10 | 8 | 10 | 10 | **9,30** |
| **2** | **S04** Aufschaltung/Leitstelle | 10 | 10 | 8,5 | 5 | 9,5 | 10 | **8,90** |
| **3** | **S06** Prüf-SaaS (Mangel → Angebot) | 9 | 9 | 6,5 | 8,5 | 8,5 | 10 | **8,43** |
| **4** | **S01** Betreiberpflichten-Manager | 8 | 8 | 6 | 8,5 | 8 | 10 | **7,78** |
| **5** | **S02** Terminierungs-Abo | 10 | 5 | 6 | 8,5 | 6 | 9 | **7,53** |
| **6** | **S05** Anlagen-IoT freie Servicebetriebe | 7 | 7 | 7 | 8 | 5,5 | 8 | **7,05** |
| **7** | **S03** Sensor-Monitoring SHK | 6,5 | 7 | 3 | 7,5 | 6 | 7 | **6,03** |
| **8** | **S13** Vertikaler Voice-Agent | 3 | 1,5 | 1 | 2 | 1 | 8 | **2,20** |

Rechenbeispiel S08: 9 × 0,30 + 9,5 × 0,20 + 10 × 0,20 + 8 × 0,15 + 10 × 0,10 + 10 × 0,05
= 2,70 + 1,90 + 2,00 + 1,20 + 1,00 + 0,50 = **9,30**.

**Die drei Kernaussagen der Rangliste:**

1. **Oben stehen die Modelle mit Portfolio-Zahler** (S08, S04). Nicht weil sie das beste Produkt
   haben, sondern weil ihre Abrechnungseinheit sich beim Kunden multipliziert.
2. **S02 hat die beste Monat-13-Begründung der ganzen Liste (10/10) und landet trotzdem nur auf
   Platz 5.** Grund: Churn 5/10. Das ist die wichtigste Einzelerkenntnis dieses Dokuments —
   *messbarer Nutzen allein erzeugt keine Bindung.* Messbarer Nutzen wird monatlich neu bewertet;
   struktureller Zwang wird gar nicht bewertet.
3. **S13 fällt nicht knapp durch, sondern in jeder einzelnen Dimension.** 2,20 gegen 6,03 für
   das nächstschwächste Modell.

## Q2. Welche Modelle sind in Wahrheit KEINE MRR-Modelle?

### Klarer Durchfaller: S13

**S13 ist formal ein Abo und materiell ein Verbrauchsgut ohne Preissetzungsmacht.** Die drei
Gründe, jeder für sich ausreichend:
- Bruttomarge 49,8 % [S] bei realistischer Nutzung, und sie **fällt mit steigender
  Kundenzufriedenheit** – belegt durch den fonio-Befund [F].
- Churn 25–40 %/Jahr [S]: ein Drittel Neuverkauf jährlich nur zum Stillstand.
- Null Wechselkosten. Es gibt kein einziges Element, das den Kunden hält.

Verwendung, in der S13 sinnvoll bleibt: **als Modul innerhalb von S02, S03, S06 oder S08** –
dort erzeugt es Differenzierung („Alarm per Anruf", „Nachfassanruf zum Angebot", „Termin­bestätigung
per Anruf") und wird durch die Bindung des Trägermodells geschützt. Als eigenständiges Modell:
durchgefallen.

### Grenzfall: S03

Kein verkapptes Projektgeschäft, aber ein **strukturell zu dünnes MRR-Modell für den deutschen
Markt**. Der ROI-Faktor beim Kunden liegt bei ~2,05 [S] statt bei den US-typischen 6–8, weil der
deutsche Heizungswartungsvertrag 180–350 €/Jahr kostet statt ~1.000 $ [F, beide 2026-08]. Bei
Faktor 2 wird jede Preiserhöhung zur Kündigungsdiskussion. Zusätzlich liegt der ARPU (680 €) so
niedrig, dass 280 Kunden für das echte Ziel nötig sind. Das MRR ist echt – es ist nur zu klein
und zu verhandelbar.

### Drei Modelle mit MRR-Tarnung, die aktiv verhindert werden muss

Diese drei sind echte MRR-Modelle, **erzeugen aber Umsatzbestandteile, die wie MRR aussehen und
keiner sind.** Wer sie nicht getrennt ausweist, täuscht sich selbst:

| Modell | Tarnung | Größenordnung | Gegenmittel |
|---|---|---|---|
| **S01** | **Durchleitung der Prüfleistung.** 12.000–35.000 €/Jahr Prüfvolumen je Standort können brutto durch die eigene Rechnung laufen | Umsatz +156 %, **Bruttomarge fällt von 87 % auf 44 %** [S] → K.-o. 5 verletzt | **Netto-Ausweis (Agenturmodell)**: Partner rechnet direkt mit dem Kunden ab, wir stellen nur die Vermittlungsmarge |
| **S05** | **Hardware-Verkauf.** 169 € Marge × 120 Anlagen = 20.280 € je Neukunde einmalig | Bei 3 Neukunden/Monat 60.840 €/Monat – bis zu 40 % des Gesamtumsatzes wäre einmalig | Hardwareumsatz in jeder Planung als separate Zeile; MRR-Quote monatlich berichten |
| **S08** | **Setup + Hardware.** 48.540 € je Neukunde einmalig [S] | Bei 1 Neukunde/Monat 48.540 €/Monat | dito |

Ein viertes, subtileres Risiko: **S06 ist kein verkapptes Projektgeschäft, aber ein verkapptes
Softwareentwicklungsvorhaben** – 450.000–900.000 € Vorleistung über 12–18 Monate [S], bevor die
Erlösarchitektur überhaupt greift. Die Architektur ist exzellent, sie ist nur nicht in 24
Monaten zugänglich.

### Was überraschend NICHT durchfällt

**S02** ist trotz seines Nutzungsanteils (34 % der Erlöse sind volumenabhängig) ein echtes
MRR-Modell, weil die zugrunde liegenden Fälligkeiten gesetzlich wiederkehren (Befund 3). Der
Nutzungsanteil schwankt saisonal, verschwindet aber nicht. Das Risiko bei S02 ist Churn, nicht
Wiederkehr.

## Q3. Welche Preis-Logik ist die überlegene – und warum?

**Antwort: Preis je Objekteinheit (Aufschaltpunkt, Messstelle, Anlage), gestaffelt, abgerechnet
gegenüber einem Zahler, der viele Einheiten besitzt – kombiniert mit einem Vertragssockel und
mindestens einem margenstarken Servicemodul.**

Die Rangfolge aller in diesem Dokument geprüften Preislogiken:

| Rang | Preis-Logik | Modelle | Bewertung |
|---|---|---|---|
| **1** | **Je Objekteinheit bei Multiplikator-Zahler** | S04, S08 | Überlegen in allen fünf Prüfdimensionen |
| **2** | **Je Objekteinheit bei Einzelzahler** | S01, S05 | Gute Skalierung, aber der Zahler hat nur begrenzt viele Einheiten |
| **3** | **Je Außendienst-Kopf** | S06 | Skaliert mit dem Nutzen, marktbelegt (Rilla [F-sek]), aber gedeckelt durch die Betriebsgröße |
| **4** | **Je Ergebnis (bestätigter Termin)** | S02 | Beste Nutzenkommunikation, schlechteste Bindung |
| **5** | **Je Anlage bei zu niedrigem Einheitenwert** | S03 | Richtige Logik, falsches Vertikal |
| **6** | **Je Rufnummer + Minute** | S13 | Vollständig vergleichbar → Preisverfall |

**Die fünf Gründe, warum Logik 1 gewinnt:**

1. **Sie multipliziert ohne Neuverkauf.** Eine Verhandlung mit einer Kette erzeugt 480
   Abrechnungseinheiten; kauft die Hausverwaltung 30 Objekte dazu, steigt der Umsatz um
   1.140 €/Monat ohne Vertriebsaufwand. Das ist der einzige Mechanismus in diesem gesamten
   Dokument, der Umsatzwachstum von Vertriebswachstum entkoppelt.
2. **Sie löst Befund 1 arithmetisch statt durch Preiserhöhung.** Nicht „wir nehmen mehr Geld je
   Kunde", sondern „wir zählen anders". S08 erreicht 3.800 € ARPU mit einem Einheitenpreis von
   7,90 € – niedriger als der Wettbewerb es je Einheit könnte, und trotzdem der höchste ARPU der
   Liste. **Das ist die eigentliche Auflösung des Preispunkt-Problems.**
3. **Die Bruttomarge bleibt bei jeder Kundengröße stabil**, weil Preis und Grenzkosten dieselbe
   Bezugsgröße haben. Bei Kopf- oder Pauschalpreisen driften sie auseinander.
4. **Sie ist prüfbar und damit unstrittig.** Der Kunde zählt seine Objekte. Es gibt keine
   Wertdiskussion, keinen jährlichen Rechtfertigungszwang – und damit keine jährliche
   Kündigungsdiskussion. Das ist ein direkter Churn-Vorteil.
5. **Sie entspricht der Branchennorm** in beiden Fällen (Aufschaltpunkt [F], Messstelle [F]).
   Man muss die Einheit nicht erklären, nur den Preis.

**Warum die Alternativen verlieren:**
- **Je Nutzer** ist die häufigste und schädlichste Wahl im deutschen Mittelstandsmarkt: Sie
  deckelt den ARPU bei 29–129 € [F], erzeugt den Fehlanreiz, Nutzer wegzulassen, und reduziert
  damit genau die Prozessverankerung, die Bindung erzeugt.
- **Je Minute** ist der Sonderfall vollständiger Vergleichbarkeit und führt zwingend zum
  Preisverfall (S13, belegt).
- **Je Ergebnis** kommuniziert den Nutzen am besten und bindet am schlechtesten – der Kunde
  bewertet jeden Monat neu.
- **Pauschale je Standort/Betrieb** ist kostenkongruent falsch und verschenkt die Skalierung an
  den erfolgreichen Kunden.

**Die vollständige überlegene Struktur besteht aus drei Teilen, nicht einem:**

| Teil | Funktion | Beispiel S08 |
|---|---|---|
| **Sockel je Vertrag** | deckt die Fixkosten der Betreuung, verhindert unprofitable Kleinkunden | 490 €/Monat |
| **Staffelpreis je Einheit** | skaliert mit dem Kunden, kostenkongruent, prüfbar | 7,90 €/Messstelle |
| **Margenstarkes Servicemodul** | hebt den Mischsatz und differenziert gegen Billiganbieter | 24/7-Alarmdienst 890 €, Auditpaket 199 € |

Alle drei Teile finden sich in S04, S08 und S01. In S13 fehlt der dritte vollständig – und das
ist der Grund, warum S13 gegen 9-€-Wettbewerber nichts entgegenzusetzen hat.

## Q4. Wo lässt sich Setup-Gebühr + Monatsvertrag kombinieren (Kriterium 18)?

**Bei allen acht – aber in sehr unterschiedlicher Qualität.** Entscheidend ist nicht, *ob* eine
Setup-Gebühr durchsetzbar ist, sondern **ob sie die Kundenakquisitionskosten deckt**.

| Modell | Setup-Gebühr | Setup-Marge | Setup ÷ Monats-ARPU | Belegqualität | Deckt Setup die CAC? |
|---|---|---|---|---|---|
| **S04** | 249 € × Objektzahl (140 Objekte = **34.860 €**) | 52 % | **14,5×** | **[F]** – „Einrichtung 150–600 € einmalig" [notrufexperten.de/acc, 2026-08]; NSL-Setup 89–150 € [F] | **Mehrfach** |
| **S08** | 3.500 € + 149 €/Standort (80 Filialen = **15.420 €**) | ~55 % [S] | **4,1×** | [S], gestützt auf NSL-Setup-Anker [F] | **Mehrfach** |
| **S06** | **4.900 €** | 44 % | 3,8× | [S], gestützt auf DSB „ab 3.000 € Initialaufwand" [F] | Ja |
| **S05** | **3.900 €** | 36 % | 2,4× | [S] | Knapp |
| **S01** | **4.500–12.000 €** | 67 % | 3,9× (bei 4.500 €) | [S], gestützt auf DSB-Anker [F] | Ja |
| **S02** | **2.900 €** | 53 % | 2,4× | [S], gestützt auf **FoxifAI 1.920 €** [F-sek] | Ja |
| **S13** | **2.400 €** | ~60 % [S] | **7,5×** | **[F-sek]** – FoxifAI **1.920 € + ab 100 €/Monat**, der einzige direkte Marktbeleg | Ja – **aber der Kunde churnt, bevor sich das MRR aufbaut** |
| **S03** | **1.500 €** | ~40 % [S] | 2,2× | [S] | Knapp |

**Die vier Erkenntnisse zu Kriterium 18:**

1. **Nur zwei Setup-Gebühren sind im deutschen Markt hart belegt:** die NSL-Einrichtung
   (150–600 €, S04) [F] und FoxifAI (1.920 €, S13) [F-sek]. Alle übrigen sind begründete
   Schätzungen mit Anker. Bemerkenswert: Ausgerechnet das schwächste Modell liefert den besten
   Setup-Beleg – ein Hinweis darauf, dass eine hohe Setup-Gebühr kein Qualitätssignal ist,
   sondern oft ein Kompensationsversuch für schwaches MRR.
2. **Die überlegene Setup-Struktur ist die mengenabhängige** (S04: 249 € × Objektzahl; S08:
   Grundbetrag + je Standort). Sie skaliert mit dem realen Onboarding-Aufwand, ist gegenüber
   dem Kunden trivial zu begründen und erzeugt bei Portfoliokunden fünfstellige Beträge bei
   Vertragsschluss. **Eine Pauschale wie „4.900 €" ist bei einem 40-Prüfer-Betrieb zu billig und
   bei einem 3-Prüfer-Betrieb zu teuer.**
3. **Die Setup-Marge sollte bewusst niedrig gehalten werden – 35–55 %, nicht 70 %.** Begründung:
   Wenn Setups profitabler sind als MRR-Monate, optimiert das Vertriebsteam auf Setups statt auf
   Bestandskunden, und die Provisionierung folgt. S01 mit 67 % Setup-Marge ist hier bereits an
   der Grenze. **Die Setup-Gebühr hat genau eine Aufgabe: die CAC decken, damit das MRR ab Monat 1
   Deckungsbeitrag ist.**
4. **Setup-Gebühr als Bindungsinstrument nutzen, nicht nur als Einnahme:** 50 % Setup-Rabatt
   gegen 24 Monate Erstlaufzeit ist bei **S02** (Churn 12–18 %) und **S03** (Adoptions-Churn in
   Monat 4–9) der wirksamste verfügbare Einzelhebel – wirksamer als jede Produktverbesserung.

## Q5. Drei modellübergreifende Befunde, die aus der Gesamtschau folgen

### Befund A — Kein einziges der acht Modelle erreicht 190.000 €/Monat in 24 Monaten

| Modell | MRR Monat 24 [S] | 100.000 € erreicht in | 190.000 € erreicht in |
|---|---|---|---|
| S02 | 115.200 € | **Monat 20–22** | Monat 30–34 |
| S01 | 120.750 € | **Monat 21–23** | Monat 32–38 |
| S05 | 81.600 € | Monat 27–30 | Monat 40+ |
| S04 | 76.800 € | Monat 27–29 | Monat 40–46 |
| S08 | 68.400 € | Monat 28–31 | Monat 40–46 |
| S03 | 64.600 € | Monat 30–33 | Monat 44+ |
| S06 | 54.600 € | Monat 34–40 | Monat 48+ |
| S13 | — | nie (unter A10) | nie (unter A10) |

Nur **S01 und S02** erreichen das 100.000-€-Zwischenziel innerhalb von 24 Monaten. Das echte
Ziel von 190.000 € liegt bei jedem Modell jenseits von Monat 30. **Diese Diskrepanz muss in der
Endempfehlung offengelegt werden** – sie ist keine Schwäche der einzelnen Modelle, sondern eine
Folge der Vertriebskapazität unter Annahme A10.

Die einzige Ausnahme von dieser Logik ist **S08** (und abgeschwächt S04): Dort hängt das Ergebnis
nicht an der Vertriebsmenge, sondern an 2–3 Großabschlüssen. Eine Supermarktkooperation mit 600
Filialen bringt allein 38.400 €/Monat. **Bei S08 ist die 24-Monats-Antwort keine Rechenaufgabe,
sondern eine Wette auf drei Logos** – und diese Wette passt zu Nicos Profil.

### Befund B — Die Kennzahl, die über die Delegierbarkeit entscheidet, ist Betreuungsstunden je 1.000 € Umsatz

| Modell | h/Kunde/Monat | ARPU | **h je 1.000 €** | Ops-FTE bei 190.000 €/Monat [S] |
|---|---|---|---|---|
| S08 | 4,0 | 3.800 € | **1,05** | **1,3** |
| S04 | 9,5 | 6.719 € | **1,41** | **1,8** |
| S06 | 2,2 | 1.300 € | **1,69** | 2,1 |
| S01 | 2,5 | 1.150 € | **2,17** | 2,7 |
| S02 | 3,0 | 1.200 € | **2,50** | 3,2 |
| S05 | 4,7 | 1.600 € | **2,94** | 3,7 |
| S13 | 1,2 | 320 € | **3,75** | 4,8 |
| S03 | 2,7 | 680 € | **3,97** | 5,0 |

Rechenweg Spalte 5: 190 × (h je 1.000 €) ÷ 150 produktive Stunden je FTE-Monat [A].

Die absoluten Stunden je Kunde täuschen: **S04 hat mit 9,5 h den höchsten Aufwand je Kunde und
braucht bei 190.000 € trotzdem nur 1,8 Ops-Kräfte** – S03 braucht mit 2,7 h je Kunde ganze 5,0.
Für Kriterium 4 (Delegierbarkeit), Kriterium 7 (80 % abgebbar) und die EBITDA-Marge von 30 % ist
allein die relative Kennzahl maßgeblich.

### Befund C — Die drei stärksten Monat-13-Begründungen folgen alle demselben Muster

Die überzeugendsten Antworten auf „warum zahlt der Kunde in Monat 13?" haben **nichts mit
Produktqualität zu tun**. Sie haben eine von drei Strukturen:

| Struktur | Modelle | Warum sie trägt |
|---|---|---|
| **Die Leistung ist die laufende Leistung** | S04 | Es gibt keinen Einrichtungszustand. Nachts um 3 sitzt jemand in der Leitstelle |
| **Der Nutzen steigt mit der Vertragsdauer** | S08 | Der Jahresvergleich der Filialen existiert in Monat 1 nicht und in Monat 13 zum ersten Mal |
| **Der Kunde hat die Leistung weiterverkauft** | S03, S05 (mit Portal), S08 | Er kann nicht kündigen, ohne sein eigenes Versprechen zu brechen |
| **Monatlicher Euro-Strom, gegenprüfbar** | S02, S06 | Der Kunde zählt die Termine bzw. die angenommenen Angebote in seinem eigenen System nach |

Die **schwächste** Struktur ist die, bei der der Nutzen ein *vermiedener* Schaden ist (S01) oder
ein *kontrafaktischer* Effizienzgewinn (S05 ohne Baseline) – beide sind real, aber nicht zeigbar.
Für beide gilt dieselbe Konsequenz: **Ohne eine im Onboarding erhobene Baseline und einen
monatlichen Report ist die Monat-13-Frage nicht gewinnbar.** Das ist eine Produktanforderung, die
in die Roadmap gehört, nicht in die Verkaufsschulung.

---

## Anhang: Quellen der in dieser Session neu erhobenen Zahlen

- DGUV-V3-Kosten je Gerät: [gwi-mbh.de](https://www.gwi-mbh.de/dguv-v3-pruefung-kosten-pro-geraet/), [inventory-one.com](https://inventory-one.com/2026/06/29/dguv-v3-pruefung-kosten/), [gericks-prueftechnik.de](https://www.gericks-prueftechnik.de/ratgeber/dguv-v3-kosten/)
- Heizungswartungsvertrag DE: [badenova.de](https://www.badenova.de/blog/heizungswartung/), [energie-experten.org](https://www.energie-experten.org/heizung/heizung-kaufen/wartungsvertrag), [my-hammer.de](https://www.my-hammer.de/heizung/preisradar/was-kostet-heizung-warten)
- HACCP-Sensorpreise: [sencono.de](https://www.sencono.de/), [diehaccpapp.de](https://diehaccpapp.de/haccp-temperaturueberwachung), [m2mgermany.de (PSsystec)](https://www.m2mgermany.de/shop/produkt/smarttempmonitor-wireless-iot-paket-haccp-temperaturkontrolle)
- NSL-Einrichtungskosten: [stadtritter.de](https://stadtritter.de/nsl-notrufleitstelle/), [livealarm.de](https://www.livealarm.de/blog/was-kostet-ein-polizeialarm/)
- Aufzugswartungskosten: [guede-aufzugtechnik.com](https://guede-aufzugtechnik.com/blog/aufzugswartung-kosten/), [aszendio.com](https://aszendio.com/kosten-fuer-die-aufzugswartung-im-ueberblick-was-betreiber-wissen-sollten/)
- Betreiberpflichten-/Prüfsoftware-Preise: [streit-software.de](https://www.streit-software.de/wissen/wartungsplaner-software), [kevox.de](https://kevox.de/software/brandschutzsoftware/)
- B2B-Terminvereinbarung Preise: [telefonakquise-agentur.de](https://telefonakquise-agentur.de/call-center-terminvereinbarung/), [callin.io](https://callin.io/de/best-b2b-appointment-setting-services/)
- DIN-Normlizenzierung in Software: [support.dinmedia.de](https://support.dinmedia.de/de/support/solutions/articles/80001166273-kann-ich-eine-norm-in-meiner-software-verwenden-), [dinmedia.de Preisliste](https://www.dinmedia.de/resource/blob/1057654/dc051e80a1f72d75254a29afa893ab63/preisliste-din-regelwerk-data.pdf)
- Herstellergebundene Heizungs-Fernüberwachung: [energie-fachberater.de](https://www.energie-fachberater.de/strom-solar/smarthome-haustechnik/profi-portal-zur-heizungsueberwachung.php), [vaillant.de](https://www.vaillant.de/heizung/heizung-verstehen/heiztechniklexikon/begriffe-c-f/fernuberwachung/)

### Offene Punkte für Welle 3

1. **S06 – DIN-Lizenzkosten konkret einholen.** Der einzige Margenposten, der zwischen 26 € und
   > 100 € je Kunde/Monat schwanken kann. Angebot bei DIN Media anfordern, bevor gebaut wird.
2. **S04 – White-Label-Einkaufspreis je Aufschaltpunkt verhandeln.** Die Annahme 14–18 € [S]
   entscheidet über 58 % oder 68 % Bruttomarge. Drei Leitstellenbetreiber anfragen.
3. **S02 – Terminquote bei Bestandskunden messen.** Die Annahme 35–55 % [A] trägt ein Drittel des
   ARPU. 20 Prüfdienstleister anrufen (der erste Schritt laut A10, nicht der Produktbau).
4. **S08 – Verderbschadenshöhe je Filiale belegen.** Die 3.000–15.000 € [A] sind das Kernargument
   der Monat-13-Begründung und derzeit unbelegt.
5. **S03 – Preise von Bosch HomeCom Pro und Vaillant für Fachbetriebe ermitteln.** Wir konkurrieren
   möglicherweise gegen null Euro.
