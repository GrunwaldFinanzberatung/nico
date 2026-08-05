# 14 – Top 5 Deep Dive

Stand: 2026-08-05 · Alle Werte nach Red-Team-Korrektur
· Zahlenquellen: `08_mrr_modelle.md`, `09_delegationsmodelle.md`, `10_finanzmodelle.csv`, `11_risikoanalyse.md`, `19_red_team_analyse.md`

---

## Übersichtstabelle

| | **S04** Leitstelle | **S01** Betreiberpflichten | **S08** Monitoring B2B2B | **S02** Terminierung | **S13** Voice-Agent |
|---|---|---|---|---|---|
| ARPU [S] | 2.400 € | 1.150 € | 3.800 € | 1.200 € | 320 € |
| Kunden für 190.000 € | **80** | 166 | **50** | 159 | 594 |
| Bruttomarge (korrigiert) | **45–60 %** | **35–56 %** | **45–60 %** | 86,5 % | **49,8 %** |
| Churn/Jahr [S] | **3–6 %** | 6–9 % | 4–7 % | **12–18 %** | **25–40 %** |
| Break-even (realistisch) | M21 | M26 | n. m. | M21 | M16 |
| Kapitalbedarf (realistisch) | 342 k € | 280 k € | n. m. (0,9–1,7 Mio. € HW) | 172 k € | 184 k € |
| Unter A1 finanzierbar | **nein** | **nein** | **nein** | grenzwertig | grenzwertig |
| 80 % Ausstieg in 24 M | **JA** (4 h/Wo) | JA ab M28–30 | JA (6 h/Wo) | JA (5 h/Wo) | **NEIN** (12 h/Wo) |
| Erste Vollzeitkraft ab MRR | 22.300 € | 23.700 € | 23.700 € | 22.800 € | 26.200 € |
| Persönlichkeits-Fit | 5,2 | **4,8** | 7,0 | 6,9 | 6,7 |
| Risikorang (1 = niedrig) | 7 | 5 | **2** | 6 | **8** |
| K.-o.-Verstoß | **K.-o. 3 bedingt** | K.-o. 9 bedingt, K.-o. 10 gefährdet | keiner | keiner | keiner |
| Red-Team-Urteil | angeschlagen | angeschlagen | widerlegt (Kühlkette) | widerlegt (Standalone) | widerlegt |
| 30 k netto erreicht | **M36** | M47 | n. m. | M50 | M37 |

---

## 1. S04 — Aufschalt- und Leitstellenmodell

**Angebot:** 24/7-Aufschaltung von Aufzügen, Toren, Heizung, Kälte, Pumpen,
Brandmeldern auf eine White-Label eingekaufte Leitstelle. Notruf, Dokumentation
nach BetrSichV.
**Zielgruppe:** Hausverwaltungen (50–300 Einheiten), Wohnungsunternehmen, Kliniken,
Kommunen, Gewerbeimmobilien.
**Preis:** 20–60 €/Monat je Aufschaltung [F] · Setup mengenabhängig 249 €/Objekt
(bei 140 Objekten 34.860 € = 14,5× Monats-ARPU).
**Wiederkehrender Umsatz:** Die Monat-13-Frage stellt sich strukturell nicht —
nachts um 3 sitzt jemand in der Leitstelle. Gesetzlich verstärkt (EN 81-28, BetrSichV).
**Mitarbeiter:** Objekt-Koordinator ab 22.300 € MRR. **Kein eigenes Leitstellenteam**
— Eigenbetrieb bräuchte 5,5–6,5 FTE und rechnet sich erst ab ~140.000 € MRR.
**Nicos Rolle:** Vertrieb an Verwalter, Partnerverhandlung mit der Leitstelle,
Produktschnitt. Ab Monat 25: 4 h/Woche, davon 88 % Wunschtätigkeit.
**Umsatzpotenzial:** 80 Kunden für 190.000 €. Bei S04 hängt das Ergebnis an
2–3 Großabschlüssen, nicht an Vertriebsmenge — das passt zu Nicos Stärkenprofil.
**Startaufwand:** ~5.500 € MVP. Kapitalbedarf bis Break-even 342 k € — behebbar
über die Setup-Gebühr.
**Markteintritt:** 40 Hausverwaltungen ansprechen, 12 Erstgespräche, 2 Piloten.
**Kritischer Pfad:** VdS-Leitstelle als White-Label-Lieferant. Ohne diesen Partner
existiert das Modell nicht.
**Größte Gefahr:** K.-o. 3. Befreiungsorganisation ist erlaubnispflichtig;
VdS 3138 ist eine Kettenzertifizierung, die Nicos Glied miterfasst.

## 2. S01 — Betreiberpflichten-Manager (als Overlay)

**Angebot:** Kataster aller prüfpflichtigen Anlagen, Fristenkalender, Nachweisakte
— als **Overlay über bestehende Verträge**, nicht als Vollpaket mit Durchleitung.
**Zielgruppe:** Betriebsstätten 50–500 Mitarbeiter.
**Preis:** Setup 1.500–3.500 €/Standort · monatlich **300–800 €/Standort**.
Ausdrücklich **nicht** 5.000–30.000 €/Jahr mit Durchleitung — das senkt die Marge
von 87 % auf 44 %.
**Wiederkehrender Umsatz:** Über 50 Pflichtvorschriften allein vom Gesetzgeber [F].
Der Kunde kann den Anbieter wechseln, nicht die Pflicht.
**Mitarbeiter:** **Ops-/Compliance-Leiter unter den ersten drei Einstellungen** —
das ist die Bedingung, unter der das Modell zulässig ist, keine Formalie.
**Nicos Rolle:** Vertrieb und Produktarchitektur — ausdrücklich **nicht** die des
Garanten. Ab Monat 28–30: 7 h/Woche.
**Umsatzpotenzial:** 166 Kunden für 190.000 €.
**Markteintritt:** 20 Anrufe bei technischen Leitern mit der Frage nach den heutigen
internen Kosten, nicht nach Interesse.
**Größte Gefahr:** Nicht die Ökonomie, sondern der Fit. 450–540 parallele Fristen
bei 30 Standorten, dauerhaft 22–27 gleichzeitige Einzelfälle. Der Verkaufserfolg
erzeugt die Last, die vom Verkaufen abhält.
**Zwingende Absicherung:** Individualvereinbarung statt AGB (die Fristenüberwachung
ist die Kardinalpflicht) · kombinierte BHV/VSH ≥ 3 Mio. mit Einschluss von
Koordinationsfehlern.

## 3. S08 — Monitoring-as-a-Service mit B2B2B-Zahler

**Angebot:** Sensorik, Cloud-Dokumentation und Alarmierung, verkauft an
Filialzentrale, Lieferant oder Verband.
**Beste MRR-Qualität im Feld (Score 9,30):** höchster ARPU (3.800 €), nur
**50 Kunden** für 190.000 €, Churn 4–7 %, und der Nutzen **steigt** mit der
Vertragsdauer — der Jahresvergleich der Abweichungen je Filiale existiert in
Monat 13 zum ersten Mal.
**Warum es trotzdem fällt:** Markt dreifach besetzt (Testo Saveris, Danfoss Alsense
mit > 50.000 Installationen, Wurm; TEMPASCAN ab 39 €/Monat all-inclusive) ·
0,9–1,7 Mio. € Hardwarevorfinanzierung · **operativ dauerhaft cashflownegativ im
Wachstum** (bei 50 Neustandorten/Monat: 45.000 € raus, 5.000 € MRR rein) ·
B2B2B bedeutet 12–24-Monats-Ausschreibungsverkauf mit Einkaufsabteilung.
**Was bleibt:** Der Tank-/Silo-Zweig ist nur angeschlagen, nicht widerlegt — und
der Alarm per Anruf bleibt ein echter Differenzierer.

## 4. S02 — Terminierungs-Abo (als Mechanik, nicht als Unternehmen)

**Beste Monat-13-Begründung des gesamten Feldes (10/10)** und höchste Bruttomarge
(86,5 %) — und trotzdem nur MRR-Rang 5, wegen 12–18 % Churn.

> **Messbarer Nutzen erzeugt keine Bindung. Er wird monatlich neu bewertet.
> Struktureller Zwang wird gar nicht bewertet.**

**Warum widerlegt:** plancraft PORTA existiert mit Terminabstimmung auf der Roadmap ·
Certado wirbt schon mit automatischen Erinnerungen (Unterschied = ein Kanal) ·
UWG § 7 verbietet die Reaktivierung bei Privatkunden · § 8 Abs. 2 UWG macht die
eigene Kundenbasis zu Regressgläubigern.
**Was bleibt:** die Mechanik als **interner Kostenvorteil** in einem Modell, in dem
Nico die Kundenbeziehung besitzt. Dort schlägt sie die Bürokraft des Wettbewerbers
um Größenordnungen.

## 5. S13 — Vertikaler Voice-Agent

**Als MRR-Modell klar durchgefallen (Score 2,20).** Bruttomarge 49,8 % bei
realistischer Nutzung — und sie **sinkt mit steigender Kundenzufriedenheit**: Das
Modell verdient nur an Kunden, die es nicht nutzen (fonio: 0,099 €/Min bei
Vollausschöpfung gegen 0,10–0,12 € Plattformkosten). Churn 25–40 %, null
Wechselkosten, **594 Kunden** für das Ziel, Verteidigbarkeit 2/10, höchstes
Risikoranking, reißt die Delegationshürde.

Dazu die Marktlage: Telekom integriert ins Netz, Placetel 9 €/Monat,
Aaron.ai in Doctolib aufgegangen, Air.ai mit 18-Mio.-$-FTC-Vergleich beendet.
Und seit dem 2. August 2026 gilt die AI-Act-Ansagepflicht, deren Wirkung auf die
Conversion niemand kennt.

**Einzige zulässige Rolle: Modul innerhalb eines anderen Modells.**
