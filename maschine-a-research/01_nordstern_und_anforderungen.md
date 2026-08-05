# 01 – Nordstern, Persönlichkeitsprofil und Anforderungen an „Maschine A"

Stand: 2026-08-05 · Auftraggeber: Nico Grunwald · Status: Verbindliche Arbeitsgrundlage für alle Research-Agenten

---

## 1. Definition „Maschine A"

**Maschine A** ist das *eine* skalierbare Unternehmen, das:

1. hohen **wiederkehrenden Cashflow** erzeugt,
2. **echten, messbaren Wert** für zahlende Kunden liefert,
3. ein **starkes Team finanzieren** kann (nicht nur Nico ernährt),
4. langfristig **weitgehend ohne Nicos tägliche Anwesenheit** funktioniert,
5. **Unternehmenswert** aufbaut (verkaufbar, nicht nur ein gut bezahlter Job).

Maschine A ist ausdrücklich **kein** Leidenschaftsprojekt. Leidenschaftsprojekte
(Werkstatt, Fahrzeuge, Outdoor, Musik, Geschichte) werden **von** Maschine A
finanziert – sie sind nicht Maschine A selbst. Diese Trennung ist ein
Kernkriterium der gesamten Bewertung.

---

## 2. Nordstern (wörtlich)

> „Ich erschaffe ein freies und selbstbestimmtes Leben für mich und meine Familie.
> Ich baue Unternehmen, Systeme und Projekte, die echten Wert schaffen und auch
> dann weiterwirken, wenn ich nicht persönlich arbeite.
> Mein Unternehmen dient meinem Leben. Mein Leben dient nicht meinem Unternehmen.
> Ich möchte bauen, entwickeln, entdecken, reisen und Zeit mit meiner Familie verbringen.
> Meine Unternehmen schaffen Einkommen, Vermögen und Sicherheit für meine Familie.
> Meine Kinder sollen nicht bei null anfangen müssen.
> Geld ist für mich kein Selbstzweck, sondern Entscheidungsfreiheit.
> Ich möchte Wert liefern, ohne permanent persönlich anwesend sein zu müssen."

### Finanzielle Zielgrößen

| Ziel | Wert | Zeithorizont (Annahme) |
|---|---|---|
| Netto frei verfügbar für Familie | ≥ 30.000 €/Monat | 36–60 Monate |
| Unternehmensumsatz | ≥ 100.000 €/Monat (1,2 Mio €/Jahr) | 24–48 Monate |
| Wiederkehrender Anteil am Umsatz | ≥ 60 % MRR | ab Monat 18 |
| EBITDA-Marge | ≥ 30 % | ab Monat 24 |
| Abwesenheitsfähigkeit | mehrere Wochen bis Monate am Stück | ab Monat 24 |

**Rechnerische Konsequenz (Annahme, muss in 10_finanzmodelle geprüft werden):**
30.000 € netto/Monat privat erfordert bei deutscher GmbH-Besteuerung
(≈30 % KSt+GewSt, dann ≈26,4 % KapESt+Soli auf Ausschüttung, effektiv ≈48 %
Gesamtbelastung) einen **Vorsteuergewinn von ca. 57.000–60.000 €/Monat**
bzw. **ca. 690.000–720.000 €/Jahr**. Bei 30 % EBITDA-Marge entspricht das
**ca. 190.000–200.000 € Monatsumsatz** – also dem *Doppelten* des genannten
100.000-€-Ziels. Das 100.000-€-Ziel ist damit ein **Zwischenziel**, kein Endziel.
Diese Diskrepanz muss in jeder Empfehlung offengelegt werden.

---

## 3. Persönlichkeitsprofil

### Stärken
- Unternehmer und Builder; Unternehmens- und Produktarchitekt
- kreativer, technischer Problemlöser
- sehr vielseitig, schnell lernfähig
- verbindet unterschiedliche Domänen miteinander
- optimistisch, lösungsorientiert
- erkennt Schwächen bestehender Lösungen
- stark im Verkaufen, Präsentieren, Überzeugen
- bereit, in der Aufbauphase intensiv und operativ zu arbeiten

### Interessen
Technik, Maschinen, Motoren, Fahrzeuge, Outdoor, Reisen, Geschichte, Musik,
KI, Automatisierung, Unternehmen

### Harte Abneigungen (Anti-Kriterien)
Nico will **dauerhaft nicht**:
- Unterlagen prüfen, Dokumente sortieren, Buchhaltung, Excel-Pflege
- Fristen und Einzelfälle verwalten
- täglicher Kundensupport, 24/7-Erreichbarkeit
- ständige Kundenberatung, immer dieselbe Standardleistung selbst erbringen
- stark regulierte Branche
- Abhängigkeit von Konzernen, Produktgebern, HGB-Strukturen
- steifes Anzug-Business
- operatives Tagesgeschäft persönlich kontrollieren
- bei jedem Mitarbeiterproblem eingebunden sein
- jeden Verkauf selbst abschließen
- ein Unternehmen besitzen, das ohne ihn stehen bleibt

### Ideale Langfristrolle
Vision · Produktentwicklung · Konkurrenzanalyse · Angebotsentwicklung ·
Innovation · Prozess- und Produktverbesserung · Firmenkultur ·
strategische Partnerschaften · große Entscheidungen · Austausch mit
Führungsteam · Erkennen von Engpässen · Aufbau neuer Unternehmen/Produkte/Systeme

### Motivationstreiber
Sichtbares Ergebnis · Verbesserung · Erschaffen · technisch/kreativ ·
Problemlösung · Abwechslung · Entwicklung

---

## 4. Bekannte Assets (Ausgangslage, kein Wunschdenken)

Belegt aus dem Repository `GrunwaldFinanzberatung/callsuite-backend`
(Stand 2026-08-05):

| Asset | Beleg | Relevanz |
|---|---|---|
| **CallSuite** – eigene Calling-/Lead-Software | `api/call.js`, `api/call-status.js`, `api/twilio-token.js` | Funktionierende Outbound-Telefonie im Browser (Twilio Voice SDK) |
| Twilio-Infrastruktur inkl. deutscher Rufnummer | `TWILIO_FROM_NUMBER=+4944885949019` | Telefonie-Stack produktiv, nicht Theorie |
| Supabase-Datenmodell | `cs_listen`, `cs_berater`, `cs_webhooks`, `cs_sheets_sync`, `cs_arbeitszeit` | Lead-Listen, Berater-Zuordnung, Arbeitszeit-/KPI-Tracking vorhanden |
| Partner-Webhook-Ingest | `api/webhook.js` + `formular.html` | Lead-Zufluss von Drittpartnern (z. B. Maklern) technisch gelöst |
| Google-Sheets-Auto-Sync | `api/sheets-sync.js`, 2-h-Intervall | Import aus Fremdquellen (z. B. ImmoScout-Leads) |
| Agenten-/Arbeitszeit-Tracking | `cs_arbeitszeit` (Anrufe, Erreicht, Termine) | Vorstufe eines Callcenter-Steuerungssystems |
| Vertriebs-/Telefonie-Erfahrung | Firmenkontext Grunwald Finanzberatung | Nico kennt Lead-Ökonomie und Terminierung aus der Praxis |

**Bewertungsrelevanz:** Modelle, die auf diesen Assets aufsetzen, erhalten in
„Geschwindigkeit bis zum ersten Umsatz" und „Startkapitalbedarf" einen
belegbaren Vorteil. Sie erhalten **keinen** Bonus in Persönlichkeits-Fit oder
Delegierbarkeit – diese müssen eigenständig verdient werden.

**Warnung (Red-Team-Vorgriff):** Der bestehende Kontext ist Finanzberatung/
Immobilienfinanzierung. Genau diese Branche steht auf Nicos Ausschlussliste
(stark reguliert, Produktgeber-Abhängigkeit, Anzug-Business). Die Assets sind
wertvoll – die *Branche* darum herum ist es für Maschine A nicht. Jede
Empfehlung muss diese Trennung sauber ziehen.

---

## 5. Pflichtkriterien (30)

| # | Kriterium | Typ |
|---|---|---|
| 1 | Wiederkehrende Einnahmen | Muss |
| 2 | Hohe Bruttomarge (Ziel ≥ 65 %) | Muss |
| 3 | Standardisierbare Leistung | Muss |
| 4 | Delegierbare Leistungserbringung | Muss |
| 5 | Wenige hochwertige Kunden statt hunderte Kleinkunden | Soll |
| 6 | Keine dauerhafte Abhängigkeit von Nico | Muss |
| 7 | ≥ 80 % Tagesgeschäft in 24 Monaten abgebbar | Muss |
| 8 | Verkaufbarer Unternehmenswert | Muss |
| 9 | Aufbau von Marke, Prozessen, Kundendaten, IP, Lizenzen oder Software | Soll |
| 10 | Reale, nachweisbare Nachfrage | Muss |
| 11 | Klare Zahlungsbereitschaft | Muss |
| 12 | Geschäftskritisches Problem | Muss |
| 13 | Messbarer Kundennutzen | Muss |
| 14 | Niedriger regulatorischer Aufwand | Soll |
| 15 | Kein stark reguliertes Finanz-/Versicherungsmodell | Muss |
| 16 | Kein reines Stunden-gegen-Geld-Modell | Muss |
| 17 | Kein dauerhaftes Projektgeschäft ohne Standardisierung | Muss |
| 18 | Setup-Gebühr + Monatsvertrag möglich | Soll |
| 19 | Lizenz-/Service-/Wartungs-/Nutzungsgebühren möglich | Soll |
| 20 | Skalierbar auf ≥ 100.000 €/Monat | Muss |
| 21 | Internationalisierbar | Kann |
| 22 | Technische, praktische oder systemische Komponente | Soll |
| 23 | Bestehende Lösungen deutlich verbesserbar | Soll |
| 24 | Wettbewerber über bessere Gesamtleistung schlagbar | Soll |
| 25 | Passend zu lockerer, bodenständiger Kultur | Soll |
| 26 | Aufbau mit Partner/COO/Assistenz möglich | Soll |
| 27 | Aufbauphase darf arbeitsintensiv sein | Rahmen |
| 28 | Aufbauarbeit passt zu Nicos Stärken | Muss |
| 29 | Administrative Arbeit früh delegierbar | Muss |
| 30 | Finanziert langfristig die Builder-Welt | Muss |

---

## 6. Harte Ausschlusskriterien (K.-o.)

Ein Modell wird **ohne Bewertung ausgeschlossen**, wenn mindestens eines zutrifft:

1. Nico muss nach 24 Monaten noch zwingend Hauptleistungserbringer sein.
2. Kein sinnvoller wiederkehrender Umsatz möglich.
3. Modell ist stark reguliert (Erlaubnispflicht §34c/d/f/i GewO, BaFin, MPDR, TÜV-Zulassung o. ä. als Kern).
4. Jeder Kunde benötigt eine vollständige Sonderanfertigung.
5. Bruttomarge dauerhaft zu niedrig, um Personal zu finanzieren (< 45 %).
6. Das Modell gewinnt nur über niedrige Preise.
7. Permanente Wochenend- oder Notfallarbeit notwendig.
8. 24/7-Erreichbarkeit wird erwartet (durch *Nico*; ein bezahltes 24/7-Team ist zulässig).
9. Hohe persönliche Haftung ohne beherrschbare Absicherung.
10. Nicos ungeliebte Tätigkeiten sind der Kern der Arbeit.

---

## 7. Bewertungsmatrix – Kategorien und Gewichte

20 Kategorien, jeweils 0–10 Punkte. Gewichtung laut Auftrag (Summe 100 %):

| Gewicht | Kategorie(n) | Anmerkung |
|---|---|---|
| 12 % | Persönlichkeits-Fit | |
| 12 % | Nordstern-Fit | |
| 10 % | Wiederkehrender Umsatz | |
| 10 % | Delegierbarkeit | |
| 10 % | Persönliche Unabhängigkeit von Nico | invertiert bewertet: 10 = maximal unabhängig |
| 8 % | Stärke des Kundenproblems | |
| 7 % | Zahlungsbereitschaft | |
| 7 % | Bruttomarge | |
| 6 % | Standardisierbarkeit | |
| 6 % | Skalierbarkeit | |
| 5 % | Geschwindigkeit bis zum ersten Umsatz | |
| 4 % | Regulatorisches + Haftungsrisiko (je 2 %) | invertiert: 10 = risikoarm |
| 3 % | Unternehmenswert | |
| **100 %** | | |

**Ungewichtete Zusatzkategorien** (werden erhoben und ausgewiesen, fließen aber
nicht in den Score ein, da der Auftrag ihnen kein Gewicht zuweist – sie dienen
als Tiebreaker und Warnsignale):

- Startkapitalbedarf (10 = sehr gering)
- Marktgröße
- Wettbewerbsvorteil
- Möglichkeit zur Produktverbesserung
- Internationale Erweiterbarkeit
- Langfristige Neugier für Nico

**Tiebreaker-Regel:** Bei Score-Differenz < 0,3 Punkten entscheidet in dieser
Reihenfolge: (1) Langfristige Neugier, (2) Startkapitalbedarf, (3) Wettbewerbsvorteil.

---

## 8. Kennzeichnung von Zahlen

Jede Zahl in diesem Projekt trägt eine Kennung:

- **[F]** Fakt – aus benannter, überprüfbarer Quelle, mit Datum
- **[S]** Schätzung – abgeleitet aus Fakten, Rechenweg offengelegt
- **[A]** Annahme – nicht belegt, plausible Bandbreite, explizit als unsicher markiert

Nicht gekennzeichnete Zahlen sind ungültig und müssen in der Qualitätskontrolle
beanstandet werden.
