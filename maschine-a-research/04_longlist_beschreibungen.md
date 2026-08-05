# 04 – Longlist: Beschreibungen und Ausschlussbegründungen

Stand: 2026-08-05 · Strukturierte Fassung: `03_longlist.csv` (62 Modelle)

---

## 1. Wie die Longlist entstanden ist

| Schritt | Anzahl |
|---|---|
| Rohmodelle aus Welle 1 (A01: 41 DACH, A02: 36 international, A10: 22 Copy-and-Improve) | **99** |
| nach Deduplizierung (viele Doppelungen DE/international) | **62** |
| nach Anwendung der 10 K.-o.-Kriterien | 31 |
| nach Konvergenzprüfung → Shortlist | **16** |

**Regel 1 der Methodik wurde durchgehend eingehalten:** Jedes Longlist-Modell nennt
mindestens einen real existierenden Anbieter mit URL. Modelle ohne Anbieter sind
Ideen, keine Erkenntnisse, und wurden verworfen.

Die vollständigen Steckbriefe je Modell — mit Anbieter, Preisen, Schwächen,
Verbesserungsansatz, Delegierbarkeit und Regulatorik-Ampel — stehen in den
Rohberichten:

| Quelle | Umfang |
|---|---|
| `raw/agent01_markt_de.md` | 41 DACH-Modelle, je 11 Pflichtfelder |
| `raw/agent02_markt_international.md` | 36 internationale Modelle, je 12 Pflichtfelder |
| `raw/agent10_copy_improve.md` | 22 Copy-and-Improve-Modelle, je 10 Pflichtfelder, plus ETA-Analyse |
| `raw/orchestrator_feldC_nachrecherche.md` | Feld C (Betreiberverantwortung, Wartung, CPO) |

---

## 2. Die fünf Muster über alle Modelle

**Muster 1 — „Plattform über fragmentiertem Handwerk" ist das dominierende
Margen-Muster.** Die physische Leistung ist regional zersplittert, margenschwach und
personalabhängig. Die Fristen-, Dokumentations- und Koordinationsschicht darüber ist
bundesweit skalierbar mit kaum Grenzkosten.
→ **Wer die Leistung erbringt, verdient 45–60 %. Wer die Compliance zusagt und die
Erbringung einkauft, verdient 75–90 % und ist delegierbar.**

**Muster 2 — Der Zahler ist oft nicht der Nutzer.** Silotelemetrie, Agrar,
HACCP-Filialisten werden erst wirtschaftlich, wenn Lieferant, Abnehmer oder Zentrale
zahlt. Das löst gleichzeitig Kriterium 5.

**Muster 3 — Gesetzliche Wiederkehr schlägt vertragliche Wiederkehr.** Modelle mit
Turnus aus einer Verordnung (DGUV V3, DIN EN 15635, TrinkwV, F-Gase-VO, DIN 14676,
§ 146a AO, § 21 StVG) haben strukturell niedrigeren Churn. Der Kunde kann den
Anbieter wechseln, aber nicht die Pflicht.

**Muster 4 — Preistransparenz ist ein Indikator für Preisdruck.** Wo Preise offen
stehen (Handwerker-SaaS 15–120 €, Fuhrpark 4,90 €, Voice-KI ab 29 €, FaSi ab
29,99 €, DSB ab 79 €), herrscht Preiskampf. Wo niemand Preise veröffentlicht
(Entsorger-ERP, After-Sales-Portale, Gefahrstoff-SaaS, Kältetechnik,
Schädlingsmonitoring), sind Margen und Ticketgrößen höher.
**Achtung — das Red Team widerspricht:** Die Umkehrung ist genauso plausibel
(Preisintransparenz = Einzelfallgeschäft = K.-o. 4). Diese Heuristik hat die
Rangfolge mitgeprägt und ist **nicht validiert**.

**Muster 5 — Der Fachkräftemangel ist Risiko und Geschäftsmodell zugleich.**
Modelle, die den Engpass durch Fernüberwachung oder Automatisierung reduzieren
(Leckage-Erkennung halbiert Prüfintervalle, Fernüberwachung reduziert
Aufzugswärter-Turnus, Sensorik ersetzt Kontrollgänge), haben den stärksten
Wertbeitrag.

---

## 3. Ausschlüsse mit Begründung

| Modell | K.-o. / Grund |
|---|---|
| Handwerker-ERP als Standalone-SaaS | Kriterium 5: 500–1.900 Kunden nötig; plancraft mit > 50 Mio. € finanziert |
| Baustellen-Zeiterfassung, Werkstatt-SaaS, Fuhrpark-SaaS | ARPU 5–50 € → Kriterium 5 |
| KI-Automatisierungsagentur / Retainer | **K.-o. 17** — Projektgeschäft ohne Standardisierung |
| Externer Datenschutzbeauftragter | **K.-o. 10** — Kern ist wörtlich Nicos Anti-Liste |
| F-Gase-Prüfung, Kranprüfung (selbst erbringen) | **K.-o. 3** — Zertifizierung als Kern |
| Managed Print | schrumpfender Markt, 35–55 % Marge, Konzernabhängigkeit |
| Kassensystem/TSE | Payment ist BaFin-reguliert, Markt wird von Payment-Anbietern aufgerollt |
| Equipment-as-a-Service Baumaschinen | **K.-o. 5** — Kapitalintensität, 45–65 % Marge |
| Reine Routengeschäfte (Textil, Aktenvernichtung) | **K.-o. 5** — 40–51 % Marge selbst beim Weltklasse-Benchmark Cintas |
| Vertikaler MSP (Dental/Veterinär) | Bruttomarge 45–60 %, Helpdesk ab Tag 1, § 203 StGB |
| Micro Markets / Unattended Retail | Verwaltungslast kollidiert mit Anti-Kriterien |
| Resident Benefits Package | **Rechtsschranke** BetrKV / § 307 BGB — keine Lücke |
| MDU-/Bulk-Internet | **Rechtsschranke** TKG |
| Dashcam-Innenraumaufnahme | **Rechtsschranke** BetrVG / DSGVO |
| Search Fund im klassischen Sinn | Kanal existiert in DE praktisch nicht — **10 Transaktionen kumuliert** bei 186.000 Nachfolgefällen |
| CAFM-Software | Markt besetzt (Planon, Maqsima, Cloudbrixx), Enterprise-Vertrieb = Anzug-Business |
| Mobile Inspektionsplattform horizontal | horizontal, Marktführer SafetyCulture etabliert |
| Lone-Worker-Hardware | Blackline Safety: **4,1 % EBITDA** — Hardware-Eigenentwicklung zerstört die Marge |
| Voice-AI für Restaurants | enge Vertikale, niedriger deutscher Preispunkt |

**Nicht als Modelle geführt, sondern als übertragbare Mechaniken:**
Volumen- statt Sitzplatzpreis (ServiceM8) · netto-positive Preisgestaltung
(BrainBox AI) · Pay-per-Outcome (Numa) · Mindestumsatz-Offset (Vendasta) ·
Miete statt Verkauf (LVT) · Weiterverkaufsmarge auf fremder Sensorik (Otodata) ·
Setup-Gebühr plus Monatsgebühr (FoxifAI, im DE-Markt belegt).
