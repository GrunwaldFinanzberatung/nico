# 13 – Shortlist: die 16 Modelle, die in die Tiefenbewertung gehen

Stand: 2026-08-05 · Grundlage: Welle 1 (Agenten 01, 02, 03, 10, 11 + Orchestrator-Nachrecherche)
· Rohmaterial: 99 dokumentierte Modelle → dedupliziert → K.-o.-Filter → 16

---

## 0. Wie diese Liste entstanden ist

| Schritt | Anzahl |
|---|---|
| Rohmodelle aus Welle 1 (A01: 41, A02: 36, A10: 22) | 99 |
| nach Deduplizierung (viele Doppelungen DE/international) | 62 |
| nach Anwendung der 10 K.-o.-Kriterien | 31 |
| nach Konvergenzprüfung (von ≥2 Agenten unabhängig gefunden **oder** außergewöhnlich starker Einzelbefund) | **16** |

Die vollständige Longlist mit allen 62 Modellen liegt in `03_longlist.csv` und
`04_longlist_beschreibungen.md`. Die Ausschlussbegründungen stehen dort.

---

## 1. Die vier Befunde, die diese Shortlist prägen

Diese Erkenntnisse gelten **modellübergreifend** und sind das eigentliche
Ergebnis von Welle 1. Sie sind wichtiger als jedes einzelne Modell.

### Befund 1 — Die Preispunkt-Arithmetik entscheidet vor jeder Produktfrage

| Preis je Kunde/Monat | Kunden für 100.000 €/Monat | Kunden für 190.000 €/Monat (echtes Ziel) |
|---|---|---|
| 99 € | 1.010 [S] | 1.919 [S] |
| 199 € | 503 [S] | 955 [S] |
| 500 € | 200 [S] | 380 [S] |
| 2.500 € | **40** [S] | **76** [S] |

Nicos Soll-Kriterium 5 („wenige hochwertige Kunden") ist damit **keine
Präferenz, sondern eine rechnerische Notwendigkeit**. Jedes Modell im
29–299-€-Band verlangt eine Inside-Sales-Organisation mit 10–20 Köpfen —
genau das, wofür plancraft 50 Mio. € eingesammelt hat, und unter Annahme A10
(kein VC) nicht finanzierbar.

**Filterregel:** Modelle mit ARPU < 400 €/Monat kommen nur in die Shortlist,
wenn der Zahler ein Multiplikator ist (Kette, Verband, Partner, Betrieb mit
vielen Endkunden) — nicht der Einzelkunde.

### Befund 2 — Die Marge sitzt in der Koordination, nicht in der Ausführung

> „Wer die Leistung erbringt, verdient 45–60 %. Wer die Compliance zusagt und
> die Erbringung einkauft, verdient 75–90 % und ist delegierbar."
> — Agent 01, Muster 1

Bestätigt durch drei unabhängige Gegenproben:
- Aktenvernichtung: ~40 % Bruttomarge [F-sek]; Cintas als Weltklasse-Benchmark: 51 % [F-sek]
- Blackline Safety (Hardware-Eigenentwicklung): **4,1 % EBITDA** bei 150,5 Mio. $ Umsatz [S aus F]
- Otodata (fremde Sensorik weiterverkauft): 1,50 $ Einkauf gegen 26–54 $ Marktpreis ≈ 67 % Marge [S]

**Filterregel:** Kein Modell, in dem Nicos Firma die physische Leistung selbst
erbringt oder Hardware selbst entwickelt. Ausführung wird eingekauft,
Hardware wird zugekauft.

### Befund 3 — Gesetzliche Wiederkehr schlägt vertragliche Wiederkehr

Modelle mit Turnus aus einer Verordnung (DGUV V3, DIN EN 15635, TrinkwV,
F-Gase-VO 2024/573, DIN 14676, § 21 StVG, NIS2) haben strukturell niedrigeren
Churn als Modelle, die ein Nutzenversprechen verkaufen. **Der Kunde kann den
Anbieter wechseln, aber nicht die Pflicht.**

Gegenprobe im Preisverhalten: Wo Preise offen im Netz stehen (Handwerker-SaaS
15–120 €, Voice-KI ab 29 €, FaSi ab 29,99 €, DSB ab 79 €), herrscht Preiskampf.
Wo niemand Preise veröffentlicht (Entsorger-ERP, After-Sales-Portale,
Gefahrstoff-SaaS, Kältetechnik, Schädlingsmonitoring), sind Margen und
Ticketgrößen deutlich höher. **Preisintransparenz ist hier ein positives Signal.**

### Befund 4 — Deutschland verkauft dem Handwerk Verwaltung, das Ausland verkauft ihm Umsatz

> „In Deutschland existiert praktisch kein Anbieter, der dem Handwerksbetrieb
> ein Produkt verkauft, dessen ROI in Euro **Mehrumsatz** statt in gesparten
> Bürostunden gemessen wird." — Agent 02, Lücke 1

Belege: SmartAC verkauft Wartungs-Mitgliedschaften (~1.000 $/Jahr je Endkunde,
Retention von 70 % auf **97 %** [F-sek]) · Rilla verkauft Abschlussquote
(199–349 $/Rep/Monat, 51 Mio. $ ARR, NRR > 115 % [F-sek]) · Inspect Point
verwandelt jeden Prüfmangel automatisch in ein Angebot · Payaca verkauft die
Förderbürokratie weg.

**Das ist die Auflösung des Zahlungsbereitschafts-Problems.** Ein Betrieb, der
500 €/Monat zahlt und 3.000 €/Monat Mehrumsatz sieht, kündigt nicht — und
verhandelt nicht über 50 €.

---

## 2. Die Shortlist

Legende Konvergenz: ⬤⬤⬤ = von 3+ Agenten unabhängig gefunden · ⬤⬤ = von 2 ·
⬤ = starker Einzelbefund

### S01 — Betreiberpflichten-Manager für Mittelstandsstandorte ⬤⬤⬤
**Quelle:** A01 Modell F.2/Synthese · A10 Modell 1 · Orchestrator §6
**Angebot:** Kataster aller prüfpflichtigen Anlagen eines Standorts, Fristenkalender,
Durchführung über geprüftes Partnernetz, Auditakte auf Knopfdruck, **ein Vertrag,
eine Rechnung, ein Portal**.
**Zielgruppe:** Betriebsstätten mit 50–500 Mitarbeitern (Produktion, Logistik, Handel).
**Problem:** Heute 15–18 separate Verträge, 15–18 Fristensysteme, null Gesamtnachweis —
bei persönlicher Haftung der Geschäftsführung. Über 50 Pflichtvorschriften allein
vom Gesetzgeber [F].
**Erlös:** 5.000–30.000 €/Standort/Jahr [S, unverifiziert] · Koordinationsmarge 70–85 % [S]
**Rechtsrahmen (belegt):** Delegation ist zulässig und formalisiert (Schriftform,
Eignungsprüfung, Gegenzeichnung), **Gesamtverantwortung bleibt beim Betreiber** [F].
→ Produkt ist **Nachweisfähigkeit**, nicht Haftungsübernahme. K.-o. 3 damit nicht verletzt.
**Offene Flanke:** Negativbefund nur mittelstark (2 Suchen). TÜVs verkaufen Software
und Schulung, IFM-Konzerne nur Großportfolios — aber nicht systematisch geprüft.

### S02 — Terminierungs-Abo für Prüf- und Wartungsdienstleister ⬤⬤
**Quelle:** A10 Modell 12 ⭐ · A03 Chance 6 (Pay-per-Outcome)
**Angebot:** Fälligkeitsdatenbank + KI-Outbound + Kalenderrückschreibung + Tourenlogik.
Der Kunde des Prüfdienstleisters wird angerufen, bekommt zwei geografisch zur Tour
passende Terminvorschläge, bestätigt, Termin landet in der Disposition.
**Zielgruppe:** Prüf- und Wartungsdienstleister mit 200–2.000 Bestandskunden.
**Problem:** Der Betrieb hat 400 Kunden mit Jahresfälligkeit und eine Bürokraft,
die telefoniert. Techniker-Auslastung schwankt, Bestandskunden fallen still ab.
**Erlös:** Monatliche Plattformgebühr + Preis je bestätigtem Termin.
**Asset-Passung: höchste im gesamten Projekt.** CallSuite ist bereits ein
Outbound-Terminierungssystem gegen Listen (`cs_listen`, `cs_arbeitszeit`, Twilio
produktiv, deutsche Rufnummer).
**Belegte Lücke:** Lager A (Prüfsoftware), Lager B (Dienstleister-ERP) und Lager C
(KI-Telefonie, **inbound-only**) existieren getrennt. Prüfpflicht + KI-**Outbound**
existiert nicht. Negativbefund aus 3 Suchen = **schwach**, muss gehärtet werden.
**Offene Flanke:** Burggraben dünn — Certado und Vemas sitzen auf den Fälligkeitsdaten.
UWG § 7 muss anwaltlich geklärt werden (Bestandskunden des Auftraggebers ≠ Kaltakquise).

### S03 — Sensor-Monitoring als Motor für Wartungs-Mitgliedschaften ⬤⬤
**Quelle:** A02 Modell 22 ⭐ (SmartAC.com) · A01 Modell 13
**Angebot:** Herstellerunabhängige Nachrüstsensorik an Heizung/Wärmepumpe/Klima,
verkauft **an den SHK-Betrieb**, der damit seinen Endkunden Wartungs-Mitgliedschaften
verkauft und sie sichtbar macht.
**Zielgruppe:** SHK-/Kälte-Betriebe (nicht deren Endkunden).
**Beleg:** Retention der Mitgliedschaften steigt von 70 % auf **97 %** [F-sek];
~1.000 $/Jahr je Endkunden-Mitgliedschaft.
**Rechnung:** 200 Betriebe × 500 €/Monat = 100.000 €/Monat [S].
**Passt zu Befund 4:** verkauft Mehrumsatz, nicht gesparte Bürostunden.
**Offene Flanke (P1, sehr hoch):** Existiert in DE bereits ein Anbieter, der an
SHK-Betriebe verkauft? Gegen Vaillant, Viessmann, Bosch, 1Komma5Grad, thermondo prüfen.
Risiko: Heizungshersteller schließen die Schnittstelle.

### S04 — Aufschalt- und Leitstellen-Modell für Gebäudetechnik ⬤⬤
**Quelle:** A01 Modelle 10 + 16 · A10 Modell 9
**Angebot:** 24/7-Aufschaltung von Aufzügen, Toren, Heizung, Kälte, Pumpen,
Brandmeldern auf eine Leitstelle; Notruf, Befreiungsorganisation, Dokumentation
nach BetrSichV. Leitstelle **White-Label eingekauft**, nicht selbst gebaut.
**Erlös:** 20–60 €/Monat je Aufschaltung [F] · Bruttomarge 75–90 % [S]
(Grenzkosten je zusätzlichem Objekt 2–5 €/Monat).
**Warum stark:** Klassische Plattformökonomie, extrem niedriger Churn, kein
Kapitalbedarf bei White-Label, 24/7 über bezahltes Team (K.-o. 8 betrifft nur Nico).
**Offene Flanke:** ARPU niedrig → braucht viele Objekte; Zielkunde muss der
Verwalter mit vielen Objekten sein, nicht der Einzeleigentümer. § 34a GewO prüfen,
falls Intervention dazukommt. DIN EN 50518 / VdS-Zertifizierung der Leitstelle.

### S05 — Herstellerunabhängiges Anlagen-IoT für freie Servicebetriebe ⬤⬤
**Quelle:** A02 Modell 27 (uptime.ac) · A02 Lücke 2 · A01 Modell 13
**Angebot:** Nachrüstsensorik + Auswerteplattform für **freie Wartungsfirmen mit
Mischbestand** (Aufzüge, Tanks, Kälte). Kunde installiert selbst.
**Beleg:** uptime.ac > 200 Unternehmen in Europa [F-sek]. Otodata: 1,50 $ Einkauf
gegen 26–54 $ Marktpreis ≈ 67 % Marge [S].
**Kern der Lücke:** Der Anlagenhersteller vernetzt nur eigene Geräte. Der
Servicebetrieb mit gemischtem Bestand bleibt blind. Deutschland ist ein
Bestandsanlagen-Land.
**Rechtsgrenze:** nur **auslesend**, nie steuernd — sonst Konformitätsbewertung.

### S06 — Prüf-SaaS, das aus dem Mangel ein Angebot macht ⬤⬤
**Quelle:** A02 Modell 8 (Inspect Point) ⭐ · A02 Lücke 3 · A10 Modell 3
**Angebot:** Prüfsoftware für Brandschutz-/Sicherheitsdienstleister, bei der jeder
dokumentierte Mangel **automatisch zum Angebot** wird.
**Der konzeptionelle Unterschied:** Deutsche Anbieter bauen Dokumentationswerkzeuge,
angelsächsische bauen Vertriebssysteme. Nicht technisch, sondern konzeptionell —
deshalb ohne Kapitalwettlauf kopierbar.
**Offene Flanke:** DIN-/VDE-Normtexte sind lizenzpflichtig. Ohne Lizenz kein Produkt,
mit Lizenz ein Burggraben. Kosten unbekannt.

### S07 — Halterhaftungs-Compliance für KMU-Fuhrparks ⬤
**Quelle:** A01 Modell 26
**Angebot:** Führerscheinkontrolle, UVV-Fahrzeugprüfung, Fahrerunterweisung,
Nachweisführung nach § 21 StVG.
**Kaufmotiv:** persönliche Geschäftsführerhaftung. Marge 80–90 % [S], rein softwarebasiert.
**Passung zum Asset:** Der bekannte Engpass „Fahrer machen nicht mit" wird exakt
durch Outbound-Telefonie gelöst — dieselbe Mechanik wie S02.
**Offene Flanke:** LapID dominiert das obere Segment; ARPU im KMU-Segment unklar.

### S08 — Monitoring-as-a-Service mit B2B2B-Zahler (HACCP / Kühlkette / Silo) ⬤⬤
**Quelle:** A01 Modelle 11 + 14 · A02 Modell 25
**Angebot:** Sensorik + Cloud-Doku + Alarm; verkauft an **Filialzentrale, Lieferant
oder Abnehmer**, nicht an den Einzelstandort.
**Warum das zählt:** Muster 2 aus A01 — der Zahler ist nicht der Nutzer. Löst
Kriterium 5 strukturell.
**Marge:** 70–85 % nach Amortisation [S]. Sencono beweist reine Gerätemiete im
deutschen Markt [F].
**Differenzierer mit vorhandenem Asset:** Alarm per **Anruf** statt E-Mail, die
nachts niemand liest.

### S09 — PV-Betriebsführung (O&M) im Segment 100–750 kWp ⬤⬤
**Quelle:** A01 Modell 38 · A10 Modell 19
**Beleg:** 8–15 €/kWp/Jahr [F], Vertragslaufzeiten 20–30 Jahre, von Banken erzwungen,
95 % fernbetrieblich, Vor-Ort über Partnernetz.
**Segmentlücke:** zu klein für Fonds-Dienstleister, zu groß für den Installateur.
**Rechnung:** 100.000 €/Monat = 1,2 Mio. €/Jahr ÷ 10 €/kWp ≈ **120 MWp** betreute
Leistung [S] — erreichbar nur über Portfoliokunden, nicht über Einzelanlagen.
**Einziger Kandidat mit rein wirtschaftlichem Wechselgrund** (Ertragsausfall in Euro),
ohne Compliance-Argument.

### S10 — Compliance-/Förder-SaaS für Wärmepumpen-, PV- und Wallbox-Installateure ⬤
**Quelle:** A02 Modell 7 (Payaca, UK) ⭐
**Angebot:** BEG/BAFA/KfW/GEG/VDE-Anmeldung als geführter Prozess im Auftragsfluss.
**These:** Deutschland hat einen deutlich komplexeren Förder- und Nachweisstack als UK,
die deutsche Handwerkersoftware ist aber durchweg generalistisch.
**Burggraben:** Förderrecht ändert sich ständig — das ist zugleich Last und Graben.
**Offene Flanke (P2, sehr hoch):** Gegen plancraft, HERO, ToolTime, enerchart prüfen.

### S11 — NIS2-/vCISO-Plattform für Dienstleister ⬤
**Quelle:** A02 Modell 13 (Cynomi, 37 Mio. $ Series B [F])
**Angebot:** Plattform, mit der IT-Dienstleister ihren Kunden NIS2-Compliance liefern.
**Bester Delegationshebel im gesamten Projekt:** Verkauf an MSPs — ein Gespräch =
30 Endkunden, und der Endkundensupport liegt **strukturell beim Partner**.
**Timing:** NIS2-Umsetzungspflicht greift jetzt.
**Harte Grenze:** Sobald man selbst vCISO ist, entsteht Haftung → K.-o. 9.
Strikt Plattform bleiben.

### S12 — Bauprojekt- und Ausschreibungsdaten mit KI-Erhebung ⬤
**Quelle:** A01 Modell 34
**Angebot:** Reines Datenprodukt. Die Platzhirsche (ibau, B_I, greenprofi)
recherchieren bis heute **manuell** aus öffentlichen Quellen.
**Warum jetzt:** Diese Flanke existierte vor LLMs nicht.
**Marge:** 65–80 % mit steigender Grenzmarge, keine Leistungserbringung vor Ort,
keine Personalabhängigkeit, international übertragbar.

### S13 — Vertikaler Voice-Agent mit Tiefenintegration (Arbeitshypothese A) ⬤⬤⬤
**Quelle:** A01 Modell 35 · A03 Feld A · A02 Modell 1 · A11
**Status: bewusst in der Shortlist, obwohl Welle 1 überwiegend dagegen spricht.**
Aufgenommen, weil die Asset-Passung real ist und Methodik-Regel 11 verlangt, dass
die Hypothese fair geprüft und nicht vorab entsorgt wird.
**Gegen das Modell (belegt):** Telekom integriert den Assistenten **ins Netz**;
Placetel verkauft die KI-Rufnummer für 9 €/Monat; Aaron.ai ist in Doctolib
aufgegangen und separat nicht mehr buchbar; Label Software liefert den Assistenten
im eigenen ERP mit; DACH-Preisband bereits 29–299 € mit Rabattschlacht;
fonio verkauft bei Vollausschöpfung **unter** den eigenen Plattformkosten;
Verteidigbarkeit 2/10; Air.ai als Vertrauensschaden der Kategorie.
**Für das Modell:** Wochen statt Monate bis zum ersten Umsatz; 60–80 % Marge;
keine Vor-Ort-Leistung; FoxifAI belegt, dass deutsche KMU **1.920 € Setup +
ab 100 €/Monat** akzeptieren [F-sek] → Kriterium 18 erfüllt.
**Bedingung, unter der es überhaupt bewertbar bleibt:** vertikal und tief
integriert. Der horizontale 49-€-Markt ist tot.

### S14 — White-Label-Voice-Motor für die 40+ deutschen Telefonservice-Anbieter ⬤
**Quelle:** A03 Chance 2
**Angebot:** DSGVO-konforme Voice-Engine mit deutscher Sprachqualität, die
bestehende Telefonservices unter eigenem Namen betreiben.
**Arbitrage:** Diese Anbieter rechnen mit 0,49–1,70 €/Min bzw. je Anruf ab [F];
KI-Vollkosten 0,10–0,12 €/Min [S] → **Faktor 9–13**.
**Erfüllt Kriterium 5 perfekt:** 40 mögliche B2B2B-Kunden statt tausender KMU.
**Aber:** 40 × 2.500 € = 100.000 € theoretisch, realistisch 30–50 % Durchdringung
→ 30.000–50.000 €/Monat [S]. **Reicht als Maschine A allein nicht.**
**Hauptrisiko:** Kannibalisierungsverweigerung — AnswerConnect wirbt in den USA
explizit mit „no AI, no bots" [F]. Zeitfenster geschätzt 18–30 Monate [A].

### S15 — Franchise-/Lizenzsystem für Prüfdienstleistungen ⬤
**Quelle:** A10 Modell 22
**Angebot:** Zentrale liefert Marke, Software, Terminierung, Einkauf, Schulung;
Partnerbetriebe erbringen die Prüfleistung und zahlen Eintritt plus Umsatzanteil.
**Warum strukturell stark:** Die Zentrale erbringt **keine Leistung** — das ist die
sauberste Nordstern-Passung im gesamten Projekt, mit vier MRR-Strömen.
**Warum nicht Startpunkt:** Stufe-2-Modell. Braucht erst 2–3 profitable Pilotbetriebe,
sonst gibt es nichts zu lizenzieren.

### S16 — Micro-ETA-Hybrid: Kleinstbetrieb kaufen, Maschine daraufsetzen ⬤
**Quelle:** A10 Abschnitt 6, Szenario C
**Angebot:** Kein eigenständiges Geschäftsmodell, sondern eine **Markteintritts-
strategie** für S01/S02/S15.
**Beleg:** Search Funds sind in DE kein Kanal (kumuliert **10 Transaktionen** bei
186.000 Nachfolgefällen 2026–2030 [F/S]). nexxt-change funktioniert dagegen:
~1.000 Vermittlungen/Jahr bei > 10.000 Inseraten [F]. Durchschnittlicher
Kaufpreiswunsch **499.000 €** [F]. Micro-Cap-Multiples **4,1–5,7× EBITDA** [F].
Finanzierungsmix EK 10–30 %, Bank/KfW 50–70 %, Verkäuferdarlehen 10–30 % [F].
**Was man kauft:** Kundenliste mit gesetzlichen Fälligkeiten, mitgekaufte
Qualifikationen (löst die Regulatorik-Ampeln durch Zukauf statt Aufbau),
Cashflow ab Monat 1. Kaufpreis Kleinstbetrieb 100.000–250.000 € [S].
**Belegter Hebel:** **+1× Multiple-Prämie**, sobald wiederkehrende Wartungsumsätze
über 30 % liegen [F].
**Harte Warnung:** Als *alleiniger* Weg verletzt der Kauf K.-o. 1 — in dieser
Betriebsgröße **ist der Inhaber der Betrieb**. Nur zulässig, wenn der Betrieb
**Rohstoff** ist, nicht Ziel.

---

## 3. Ausgeschlossen mit Begründung (Auswahl der wichtigsten)

| Modell | K.-o. / Grund |
|---|---|
| Standalone KI-Telefonassistent, horizontal | K.-o. 6 (gewinnt nur über Preis) — DACH 29–299 €, Telko-Bundling, Marge rechnerisch weg |
| Handwerker-ERP als Standalone-SaaS | Kriterium 5 + A10: 500–1.900 Kunden nötig, VC-finanzierter Gegner mit 50 Mio. € |
| KI-Automatisierungsagentur / Retainer | K.-o. 17 (Projektgeschäft ohne Standardisierung) |
| Externer Datenschutzbeauftragter | K.-o. 10 (Kern = Dokumente, Fristen, Einzelfälle = Nicos Anti-Liste) |
| F-Gase-Prüfung / Kranprüfung selbst erbringen | K.-o. 3 (Zertifizierung als Kern) |
| Managed Print, Kassensysteme/TSE | schrumpfender Markt bzw. Payment ist BaFin-reguliert |
| Equipment-as-a-Service Baumaschinen | Kapitalintensität + 45–65 % Marge → K.-o. 5 |
| Reine Routengeschäfte (Textil, Aktenvernichtung) | Bruttomarge 40–51 % selbst beim Weltklasse-Benchmark → K.-o. 5 |
| Resident Benefits Package, MDU-Internet, Dashcam-Innenraum | Rechtsschranken (BetrKV/§ 307 BGB, TKG, BetrVG/DSGVO) — keine Lücken |
| Vertikaler MSP (Dental/Veterinär) | Bruttomarge 45–60 % unter Ziel; Helpdesk ab Tag 1; § 203 StGB |
| Micro Markets / Unattended Retail | Verwaltungslast kollidiert mit Anti-Kriterien |
| Search Fund im klassischen Sinn | Kanal existiert in DE praktisch nicht (10 Transaktionen kumuliert) |

---

## 4. Was Welle 2 klären muss

| Frage | Betrifft | Agent |
|---|---|---|
| Woraus entsteht MRR konkret, was rechtfertigt sie in Monat 13? | alle | 05 |
| Kommt Nico in 24 Monaten zu 80 % raus? Wann finanziert der Umsatz welche Rolle? | alle | 06 |
| Break-even, Kapitalbedarf, Sensitivität, drei Szenarien | S01–S05, S13 | 07 |
| UWG § 7 bei Bestandskunden-Terminierung; Delegationsrecht; Eichrecht; § 201 StGB; NIS2-Haftung; Versicherbarkeit von Koordinationsfehlern | S01, S02, S07, S11 | 08 |
| Laugt das Modell Nico wieder aus? Besonders: Ist Fristenverwaltung Software oder Handarbeit? | alle | 09 |
| Warum scheitert jedes Top-Modell? Kernfrage: Was hindert Certado/Vemas daran, S02 nachzubauen? | Top 5 | 12 |
