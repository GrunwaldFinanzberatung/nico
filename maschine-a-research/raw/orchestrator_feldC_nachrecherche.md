# Nachrecherche Feld C durch den Orchestrator

Anlass: Agent 03 konnte Feld C (Monitoring/Wartung/Compliance) mangels Suchbudget
nicht recherchieren und hat es als „strukturell bester Fit, keine Daten"
übergeben. Diese Lücke habe ich selbst geschlossen. Stand: 2026-08-05.

**Methodenhinweis:** Alle Angaben stammen aus WebSearch-Synthesen. WebFetch ist
in dieser Umgebung durch die Egress-Policy blockiert (HTTP 403 auf jedem Host),
Anbieter-Preisseiten konnten daher nicht direkt gelesen werden. Preise sind
[F] mit Einschränkung: belegt über Suchsynthese, nicht an der Primärquelle
verifiziert.

---

## 1. Das wichtigste Ergebnis: Feld C ist NICHT unbesetzt

Agent 03 vermutete in „Wartungsvertrags-Betriebssystem" (Chance 4) und
„Compliance-Monitoring" (Chance 5) offene Lücken. **Diese Vermutung ist in
dieser Allgemeinheit widerlegt.** Es existiert eine etablierte, dichte
Anbieterlandschaft:

### 1.1 Betreiberverantwortung / Prüffristenmanagement (Software)

| Anbieter | Positionierung | Beleg |
|---|---|---|
| **Maqsima** (Sulzbach) | `myFM`-Portal + TMS für Betreiberverantwortung nach ArbSchG, BetrSichV, GefStoffV | facility-manager.de |
| **Prüfpilot / Cloudbrixx** | **über 2.000 hinterlegte Prüfregeln** | cloudbrixx.de/pruefpilot |
| **mybuilding24** | Wartungsplanung, Doku, Inventar, Ticketing, Nachweise in einem | mybuilding24.com |
| **Prüfplaner / Wartungsplaner** | Prüfterminplanung im Betrieb | wartungsplaner.de |
| **ELISA (Fraunhofer IFF)** | Prüf-App für wiederkehrende Prüfungen, revisionssichere Doku | iff.fraunhofer.de |
| **waveware** | Regelwerke, Prüfwerte, Maßnahmen | — |
| **loyhutz CARE** | CAFM-Paket „Betreiberverantwortung" | loyhutz.de |
| **TOL GmbH**, **PwC IWMS** | CAFM- bzw. IWMS-Module Betreiberverantwortung | tol.info, pwc.de |

### 1.2 Kälte-/Klimatechnik F-Gase (Anlagenbuch)

| Anbieter | Beleg |
|---|---|
| **SHKwin**, **KaltimaCheck**, **RefrigerantTracker**, **ServicePilot** | industrie-fachwissen.de |
| **KlimaCraft** – „Digitales Anlagenbuch für Kälteanlagen" | klimacraft.de/digitales-anlagenbuch |

**Konsequenz:** Die Aussage „Kein Anbieter führt Wartungsvertrag, Prüffrist,
Anlagenstammdaten und Nachweisakte als Kernobjekte" gilt **nicht** für den
CAFM-/Betreiberverantwortungs-Markt. Sie gilt allenfalls für die
*Handwerkersoftware* (ToolTime, plancraft, Craftnote) — dort ist der Befund
weiterhin korrekt.

**Die verbleibende, präzisere Lücke** liegt damit nicht bei der Software an
sich, sondern an der Nahtstelle: Die CAFM-Systeme sitzen beim **Betreiber**
(Immobilie, Industrie, Facility Manager). Die Handwerkersoftware sitzt beim
**ausführenden Betrieb**. Kein untersuchtes System bedient den
*wartungsvertragsgetriebenen Fachbetrieb* (Kälte, Tor, Brandschutz,
Ladeinfrastruktur) mit Anlagenstammdaten, Prüffristen, Disposition und
Nachweis in einem Werkzeug. Das ist eine **engere, aber belegbarere Lücke**
als von Agent 03 formuliert — und sie muss vor jeder Empfehlung gegen die
Legacy-ERPs (Streit, Moser, Sander & Doll) geprüft werden, die genau dieses
Segment historisch bedienen.

---

## 2. Belegte Preisanker Feld C

Diese Zahlen fehlten Agent 03 vollständig und sind für die MRR-Modellierung
zentral.

| Leistung | Preis | Rhythmus | Quelle |
|---|---|---|---|
| **DGUV V3, ortsveränderliche Geräte** | **3–8 €/Gerät** [F] | alle 6–24 Monate (Gefährdungsbeurteilung, § 3 BetrSichV) | gwi-mbh.de, ama-systems.eu |
| **DGUV V3, ortsfeste Anlagen** | **50–150 €/Anlage** [F] | i. d. R. alle 4 Jahre | gwi-mbh.de |
| **DGUV V3, typisches Büro** | 150–350 € je Durchgang [F] | | ama-systems.eu |
| **Wartungsvertrag Gewerbe-Klimaanlage** | **200–600 €/Anlage/Jahr** [F], je nach Größe und SLA | jährlich | klimavergleich.at |
| **Legionellen-Gefährdungsanalyse**, bis 10 WE | ab 390 € netto [F] | anlassbezogen | hms-tec.de |
| … bis 50 WE | ab 890 € netto [F] | | ebd. |
| … bis 100 WE | ab 3.350 € netto [F] | | ebd. |

### Gesetzliche Wiederkehr-Taktung (der eigentliche Wert)

| Pflicht | Rechtsgrundlage | Takt |
|---|---|---|
| Dichtheitsprüfung Kälte-/Klimaanlagen/Wärmepumpen | **F-Gase-VO (EU) 2024/573** | alle 3, 6 oder 12 Monate je CO₂-Äquivalent [F]; ≤ 30 kW jährlich, > 30 kW halbjährlich [F] |
| Elektrische Betriebsmittel | DGUV V3 / BetrSichV § 3 | 6–24 Monate [F] |
| Ortsfeste elektrische Anlagen | DGUV V3 | 4 Jahre [F] |

**Das ist der ökonomische Kern von Feld C:** Der Kauf entsteht aus einer
Rechtspflicht mit festem Takt, nicht aus Überzeugung. Genau die Eigenschaft,
die Feld A (Voice) und Feld B (Handwerk-SaaS) fehlt und die deren Preisverfall
erklärt.

---

## 3. Ladeinfrastruktur-Betrieb (CPO-as-a-Service) — eigenständiger Kandidat

Aus der Recherche als **zusätzlicher Longlist-Kandidat** aufgenommen, den kein
Agent bisher hatte:

- **Rolle:** Der CPO (Charge Point Operator) betreibt Ladepunkte für Dritte:
  Stromeinkauf, Monitoring, Wartung, Instandsetzung, **Abrechnung der
  Ladevorgänge** und Erstattungen [F].
- **Erlösform:** Die Wohnungswirtschaft bzw. der Objekteigentümer zahlt eine
  **monatliche Gebühr je Ladepunkt** für Betrieb und Abrechnung [F]. Konkrete
  Preisspanne nicht ermittelt — offener Punkt.
- **Regulatorischer Rückenwind mit Datum:** Zum **01.01.2026** entfallen die
  bisher zulässigen **monatlichen Pauschalen für das Laden von Dienstwagen zu
  Hause**; eine pauschale Erstattung ohne tatsächlichen Verbrauchsnachweis ist
  nicht mehr zulässig [F]. Das erzwingt **eichrechtskonforme
  Verbrauchsmessung und Einzelabrechnung** bei jedem Arbeitgeber mit
  Dienstwagenflotte und Heimladung — ein Stichtag, der Nachfrage erzeugt.
- **Marktstruktur:** Es gibt viele Anbieter mit **erheblichen Preisunterschieden**
  [F]; Vergleichsstudien zur Wallbox-Abrechnung existieren bereits
  (thechargingproject.com), ebenso Warnungen vor intransparenten Betriebskosten
  (clean-charge.de). Das deutet auf **einen unreifen, intransparenten, aber
  bereits zahlenden Markt** — die Konstellation, die Agent 10 sucht.
- **Fit-Vorprüfung:** hybrid (Hardware + Software + Service), wiederkehrend,
  technisch, delegierbar; Regulatorik = Eichrecht/Messstellenbetrieb, **muss
  von Agent 08 geprüft werden** (mögliches K.-o. nach Kriterium 3).

---

## 4. Offene Prüfaufträge aus dieser Nachrecherche

1. **Preise der Betreiberverantwortungs-Software** (Maqsima, Prüfpilot,
   mybuilding24) — nicht ermittelt. Entscheidet, ob dort Preispunkte über dem
   Handwerk-SaaS-Band von 15–250 € erzielbar sind.
2. **Legacy-ERPs Streit V.1, Moser, Sander & Doll** — decken sie den
   Wartungsvertragsbetrieb bereits ab? Entscheidet über Chance 4.
3. **CPO-Monatsgebühr je Ladepunkt** — nicht ermittelt.
4. **Eichrecht/Messstellenbetriebsgesetz** — K.-o.-Prüfung für das CPO-Modell.
5. **DGUV-V3-Dienstleistermarkt** — Konsolidierungsgrad, Margen, ob Software
   oder Prüfleistung das Geschäft trägt. Achtung: Die Prüfung selbst darf nur
   eine **Elektrofachkraft** durchführen [F] — das ist eine
   Qualifikationsbindung, kein Verbot, aber ein Personalengpass.

---

## 5. Nachtrag: Preisanker Wartung/FM und ein belegter Angreifer

| Leistung | Preis | Quelle |
|---|---|---|
| **Aufzugswartungsvertrag** | **1.500–3.000 €/Jahr je Anlage** [F] = 125–250 €/Monat | personenaufzuege.com, aufzug24.net |
| **Aszendio** – nutzungsbasierte Aufzugswartung | **ab 930 €/Jahr Basispreis (77,50 €/Monat)** + variabler Wartungseinsatz [F] | aszendio.com |
| **Facility Management (München, je Leistungsumfang)** | **1,50–6,00 €/m²/Monat** [F] | falke-fm.com |
| KONE / TK Elevator | kein öffentlicher Preis, individuelle Bewertung je Anlage [F] | kone.de, tkelevator.com |

### Warum Aszendio wichtig ist

Aszendio ist ein **belegtes Praxisbeispiel für genau das Muster, das Agent 10
sucht**: eine Legacy-Branche mit Oligopol (KONE, Schindler, TK Elevator, Otto),
intransparenter Preisbildung („individuelles Angebot je Anlage") und
unzufriedenen Kunden wird von einem Angreifer mit **transparentem,
nutzungsbasiertem Preismodell** attackiert. Das Wechselargument ist nicht
Technik, sondern **Preistransparenz und Fairness** — dieselbe Struktur, die
Agent 11 im Voice-Markt gefunden hat (MV-1: Abrechnung ist die Nr.-1-Beschwerde).

**Verallgemeinerbare These für die Longlist [S]:** In deutschen
Wartungsmärkten mit Herstelleroligopol und Preisintransparenz ist
„transparente, nutzungsbasierte Abrechnung + digitaler Nachweis" ein
tragfähiger Angriffsvektor. Zu prüfen für: Aufzüge, Brandmeldeanlagen,
Torantriebe, Kälte/Klima, Ladeinfrastruktur.

**Gegenprobe an Nicos Kriterien:** Dieses Muster erfordert die
**Leistungserbringung selbst** (Monteure, Fahrzeuge, Ersatzteile) — also ein
personalintensives Servicegeschäft mit Bruttomargen deutlich unter 65 %.
Es kollidiert mit Kriterium 2 und ist nur dann interessant, wenn Nico die
**Steuerungsschicht** (Software, Disposition, Nachweis, Abrechnung) verkauft
und die Ausführung bei bestehenden Fachbetrieben belässt. Diese Unterscheidung
ist für die Bewertung entscheidend und muss in der Shortlist sauber gezogen
werden.

### Antwort auf Agent 03s kritischste Frage (§7, Punkt 14)

> „Zahlt ein deutscher Betrieb 2.000–3.000 €/Monat für irgendetwas?"

**Ja — aber nicht der 5-Mann-Handwerksbetrieb.** Belegt zahlen in dieser
Größenordnung:
- **Objekt-/Anlagenbetreiber** (Wohnungswirtschaft, Industrie, öffentliche
  Hand): FM ab 1,50 €/m²/Monat bedeutet bei 2.000 m² bereits 3.000 €/Monat [S].
- **Betreiber mit mehreren Anlagen**: 20 Aufzüge × 125–250 €/Monat =
  2.500–5.000 €/Monat [S].

**Konsequenz für die Zielgruppenwahl:** Die Kundenzahl-Arithmetik aus Agent 03
§2.3 (500–1.900 Kunden nötig) löst sich **nicht** durch ein besseres Produkt
für Handwerksbetriebe, sondern **nur durch einen Zielgruppenwechsel** — weg vom
ausführenden Kleinbetrieb, hin zum **Betreiber mit Anlagenbestand und
Haftungsrisiko**. Das ist die wichtigste strategische Ableitung dieser
Nachrecherche und muss in die Bewertung aller Modelle einfließen.
