# 02 – Research-Methodik

Stand: 2026-08-05

---

## 1. Agentenstruktur

12 spezialisierte Agenten in 2 Wellen. Welle 2 baut auf den Ergebnissen von
Welle 1 auf – ohne Marktdaten sind Finanz-, Delegations- und Risikomodelle
wertlos.

### Welle 1 – Entdeckung (parallel, unabhängig)

| Agent | Rolle | Kernfrage | Output |
|---|---|---|---|
| 1 | Markt-Scout Deutschland | Welche Modelle mit MRR funktionieren im DACH-Mittelstand bereits? | `raw/agent01_markt_de.md` |
| 2 | Internationaler Scout | Welche funktionierenden Auslandsmodelle fehlen in DE noch? | `raw/agent02_markt_international.md` |
| 3 | Wettbewerbs- & Produktanalyse | Wer bietet was zu welchem Preis – und welche Kombination bietet niemand? | `raw/agent03_wettbewerb.md` |
| 4 | Zielgruppen- & Problemanalyse | Wer hat teure, wiederkehrende Probleme und Budget? | `raw/agent04_zielgruppen.md` |
| 10 | Kopier- & Verbesserungs-Scout | Welche bewährten Modelle sind schlecht umgesetzt? Ist Nachfolge/ETA eine Abkürzung? | `raw/agent10_copy_improve.md` |
| 11 | Kundensignal- & Review-Analyst | Was sagen echte Kunden – vor allem: woran scheitern bestehende Lösungen? | `raw/agent11_kundensignale.md` |

### Zwischenschritt – Konsolidierung durch den Orchestrator
Dedupliziere Modelle, wende die 10 K.-o.-Kriterien an, bilde Longlist (≥ 50)
und Shortlist (15).

### Welle 2 – Bewertung (parallel, auf Shortlist)

| Agent | Rolle | Kernfrage | Output |
|---|---|---|---|
| 5 | Wiederkehrender-Umsatz-Architekt | Woraus entsteht MRR konkret, und was rechtfertigt sie dauerhaft? | `raw/agent05_mrr.md` |
| 6 | Delegations- & Organisationsarchitekt | Kommt Nico in 24 Monaten zu 80 % raus – und wann finanziert der Umsatz welche Rolle? | `raw/agent06_delegation.md` |
| 7 | Finanz- & Skalierungsanalyst | Rechnet sich das konservativ – Break-even, Kapitalbedarf, Sensitivität? | `raw/agent07_finanzen.md` |
| 8 | Risiko- & Regulierungsprüfer | Was kann rechtlich, technisch, personell töten? | `raw/agent08_risiko.md` |
| 9 | Gründer-Persönlichkeits-Fit | Laugt das Modell Nico wieder aus? | `raw/agent09_fit.md` |
| 12 | Gegenanwalt / Red Team | Warum scheitert jede Top-Idee? | `raw/agent12_redteam.md` |

### Welle 3 – Synthese durch den Orchestrator
Bewertungsmatrix, Score nach Red Team korrigieren, Top 5 → Top 3 → Sieger,
MVP-Pläne, 100-Tage-Plan, Management Summary.

---

## 2. Research-Regeln (verbindlich)

1. **Nur belegte Anbieter.** Jedes Modell braucht mindestens einen real
   existierenden Anbieter mit URL. Ein Modell ohne Anbieter ist eine Idee,
   keine Erkenntnis, und fliegt aus der Longlist.
2. **Keine erfundenen Zahlen.** Jede Zahl trägt [F] Fakt (Quelle + URL + Datum),
   [S] Schätzung (Rechenweg sichtbar) oder [A] Annahme (Bandbreite, explizit
   unsicher). Zahlen ohne Kennung sind ungültig.
3. **Preise bevorzugt aus öffentlichen Preisseiten.** „Preis auf Anfrage" wird
   als solcher dokumentiert, nicht geschätzt-und-verschwiegen.
4. **Muster vs. Einzelmeinung.** Kundenaussagen zählen erst ab 5 unabhängigen
   Fundstellen als Muster. Alles darunter wird getrennt als Einzelmeinung
   ausgewiesen.
5. **Friedhofsprüfung.** Zu jeder erkannten „Marktlücke" wird geprüft, ob sie
   eine echte Lücke oder ein Friedhof ist (jemand hat es versucht und ist
   gescheitert). Unbeantwortete Friedhofsfrage = Warnhinweis in der Bewertung.
6. **Getrennte Prüfung.** Markt, Wettbewerb, Zahlungsbereitschaft und
   Delegierbarkeit werden unabhängig voneinander bewertet. Ein starker Markt
   heilt keine schlechte Delegierbarkeit.
7. **Keine Trendbegründungen.** „Weil KI gerade groß ist" ist kein Argument.
   Das Argument muss lauten: Kunde X zahlt heute Y € für Z, weil ihn das
   Problem A jährlich B € kostet.
8. **Kein Bonus für Vorhandenes.** Nicos CallSuite-Assets verbessern
   ausschließlich „Geschwindigkeit bis zum ersten Umsatz" und
   „Startkapitalbedarf" – nie Persönlichkeits-Fit oder Delegierbarkeit.
9. **Ausgeschlossene Modellklassen:** persönliche Reichweite/Influencer/
   tägliche Contentproduktion; stark regulierte Finanz-/Versicherungsmodelle
   als Hauptempfehlung; Modelle mit Nico als dauerhaftem Hauptleistungserbringer.
10. **Generische Listen sind verboten.** „Dropshipping, Amazon FBA, Coaching,
    SaaS" ohne belastbare Analyse zählt nicht.
11. **Freedom-Inbound-Neutralität.** Die Arbeitshypothese „KI-Inbound" erhält
    keinen Startvorteil. Sie muss sich gegen alle anderen Modelle durchsetzen
    oder verlieren.

---

## 3. Research-Fragen (die 12 Leitfragen)

1. Welche B2B-Leistungen in DACH werden heute schon dauerhaft monatlich bezahlt – und warum kündigt niemand?
2. Wo entsteht wiederkehrender Umsatz aus einer *Pflicht* (Gesetz, Norm, Versicherung) statt aus Überzeugung?
3. Welche Zielgruppe hat ein Problem, das sie jährlich fünfstellig kostet, und ein Budget dafür?
4. Wo ist die Leistungserbringung standardisierbar genug, dass eine angelernte Kraft sie in ≤ 6 Wochen übernehmen kann?
5. Welche Kombination aus Leistungen bietet heute niemand vollständig an – und warum nicht?
6. Woran scheitern bestehende Anbieter aus Kundensicht messbar (Churn, Reviews, Beschwerden)?
7. Welche funktionierenden Auslandsmodelle sind in DE noch unbesetzt – und was blockiert den Import (DSGVO, TKG, Kultur, Sprache)?
8. Wie hoch ist die realistische Zahlungsbereitschaft deutscher KMU – belegt, nicht erhofft?
9. Wie viele Kunden braucht das Modell für 10k / 30k / 100k € Monatsumsatz, und ist diese Kundenzahl akquirierbar?
10. Welcher fortlaufende, nachweisbare Nutzen rechtfertigt die Monatsgebühr in Monat 13?
11. Wo entsteht Unternehmenswert (IP, Daten, Verträge, Marke) statt nur Cashflow?
12. Welches Modell hält Nico auch in Jahr 4 noch für interessant?

---

## 4. Offene Annahmen (müssen vom Auftraggeber bestätigt oder korrigiert werden)

Diese Annahmen wurden für die Modellierung gesetzt, weil der Auftrag sie nicht
festlegt. Sie sind **entscheidungsrelevant** – wenn eine falsch ist, ändert
sich das Ergebnis.

| # | Annahme | Wirkung, wenn falsch |
|---|---|---|
| A1 | Verfügbares Startkapital: 20.000–60.000 € [A] | Hardware-/Bestandskaufmodelle fallen bei weniger Kapital raus; ETA/Nachfolge wird bei deutlich mehr Kapital attraktiver |
| A2 | Nico kann 12–24 Monate ohne volle Gehaltsentnahme durchhalten (Grundeinkommen aus bestehender Tätigkeit) | Ohne Puffer sind nur Modelle mit Cash in ≤ 90 Tagen zulässig |
| A3 | Standort: Nordwestdeutschland (abgeleitet aus Vorwahl 04488 / Region Oldenburg) [S] | Regionale Vor-Ort-Modelle (Technik/Wartung) hängen an Bevölkerungs- und Betriebsdichte |
| A4 | Rechtsform GmbH oder UG, keine bestehende Haftungsbeschränkung wird vorausgesetzt | Haftungsbewertung ändert sich |
| A5 | Kein Kompagnon/Mitgründer vorhanden, aber grundsätzlich gewinnbar | Modelle mit zwingend zweitem Gründer (z. B. Technik-Partner) verschieben sich |
| A6 | Die bestehende Finanzberatungs-Tätigkeit läuft weiter und darf **nicht** Maschine A sein | Wenn sie beendet wird, steigt Zeitbudget, sinkt Einkommenspuffer |
| A7 | Zielgruppe ist deutschsprachig; Internationalisierung erst ab Jahr 3 | Bewertung „internationale Erweiterbarkeit" bleibt niedrig gewichtet |
| A8 | Nico ist bereit, Menschen zu führen (5–15 Mitarbeitende) | Ohne Führungsbereitschaft scheiden alle personalintensiven Servicemodelle aus |
| A9 | „30.000 € netto/Monat" bedeutet frei verfügbar nach Steuern für die Familie | Siehe Rechnung in 01 – das erfordert ca. 190k Monatsumsatz, nicht 100k |
| A10 | Kein Interesse an Fremdkapital/VC; Finanzierung aus Cashflow + ggf. Bankdarlehen | VC-Modelle (schnelles SaaS-Scaling) werden abgewertet |

**Verfahren:** Alle Ergebnisse werden unter diesen Annahmen erstellt und sind
gültig, solange die Annahmen halten. Abweichungen sind in
`20_management_summary.md` gesondert ausgewiesen.

---

## 5. Qualitätskontrolle (Checkliste vor Abschluss)

- [ ] Jede Top-Idee durch mindestens 2 reale Anbieter oder harte Marktsignale belegt
- [ ] Wiederkehrender Umsatz je Finalist konkret hergeleitet (nicht behauptet)
- [ ] Delegationspfad je Finalist mit Rollen und Umsatzschwellen
- [ ] Operative Belastung ehrlich beziffert (Stunden/Woche, nicht „gering")
- [ ] Kundenakquise realistisch (Kanal, Kontaktzahl, Conversion, Zykluslänge)
- [ ] Risiken nicht kleingeredet, Eintrittswahrscheinlichkeit × Schaden bewertet
- [ ] Alle Zahlen als [F]/[S]/[A] gekennzeichnet
- [ ] KI-Inbound erhielt keinen Vorzug – Begründung dokumentiert
- [ ] Technische und hybride Modelle gleichgewichtig untersucht
- [ ] Nicos Wunsch nach praktisch-technischer Arbeit berücksichtigt
- [ ] Freiheitsmaschine vs. Leidenschaftsprojekt sauber getrennt
- [ ] Endempfehlung ist entscheidungsfähig (eine Nummer 1, mit Begründung und Abbruchkriterien)
