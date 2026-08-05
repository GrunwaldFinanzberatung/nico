# 08 – Erlösarchitekturen und wiederkehrender Umsatz

Stand: 2026-08-05 · Detailquelle: `raw/agent05_mrr.md`

---

## 1. Rangliste nach MRR-Qualität

Gewichtung: Monat-13-Begründung 30 % · Churn 20 % · Preispunkt-Arithmetik 20 % ·
Bruttomarge 15 % · Betreuungsaufwand je 1.000 € 10 % · Kriterium 18 5 %

| Rang | Modell | Score | ARPU [S] | Kunden für 190.000 € | Churn/Jahr [S] | Bruttomarge [S] |
|---|---|---|---|---|---|---|
| 1 | **S08** Monitoring B2B2B (HACCP) | 9,30 | 3.800 € | **50** | 4–7 % | 78,7 % |
| 2 | **S04** Aufschaltung/Leitstelle | 8,90 | 2.400 € | **80** | 3–6 % | **57,9 %** |
| 3 | **S06** Prüf-SaaS | 8,43 | 1.300 € | 147 | 5–8 % | 83,6 % |
| 4 | **S01** Betreiberpflichten | 7,78 | 1.150 € | 166 | 6–9 % | 87,4 % |
| 5 | **S02** Terminierungs-Abo | 7,53 | 1.200 € | 159 | 12–18 % | 86,5 % |
| 6 | **S05** Anlagen-IoT | 7,05 | 1.600 € | 119 | 7–11 % | 79,1 % |
| 7 | **S03** SHK-Sensorik | 6,03 | 680 € | 280 | 8–12 % | 77,1 % |
| 8 | **S13** Voice-Agent | 2,20 | 320 € | **594** | 25–40 % | **49,8 %** |

## 2. Die zentrale Erkenntnis zum Churn

**S02 hat die beste Einzelbegründung für die Monatsgebühr (10/10) und landet
trotzdem nur auf Platz 5** — wegen 12–18 % Churn. Daraus folgt der wichtigste Satz
dieser Analyse:

> **Messbarer Nutzen erzeugt keine Bindung. Er wird monatlich neu bewertet.
> Struktureller Zwang wird gar nicht bewertet.**

Ein Kunde, dem man jeden Monat vorrechnet, dass er 3.000 € Mehrumsatz für 500 €
Gebühr bekommt, rechnet jeden Monat mit. Ein Kunde, der ohne das System seine
gesetzliche Nachweispflicht nicht mehr erfüllen kann, rechnet nicht.

## 3. Die drei stärksten Monat-13-Begründungen

1. **S04** – Die Frage stellt sich strukturell gar nicht. Die Einrichtung war nie
   das Produkt; nachts um 3 sitzt jemand in der Leitstelle. Verstärkt durch
   gesetzliche Pflicht (EN 81-28, BetrSichV).
2. **S08** – Der Nutzen *steigt* mit der Vertragsdauer: Der Jahresvergleich der
   Kühlkettenabweichungen je Filiale existiert in Monat 1 nicht und in Monat 13
   zum ersten Mal. Plus Pflicht (IFS/BRC), plus ereignisbasierter Beleg je Alarm.
3. **S06** – Als einziges Modell mit **beidem**: Umsatzargument („34 Angebote
   angenommen, 6.120 € Volumen" — in der eigenen Buchhaltung des Kunden
   gegenprüfbar) und Pflichtargument.

## 4. Durchgefallen als MRR-Modell

**S13 Voice-Agent — klar durchgefallen.** Bruttomarge 49,8 % bei realistischer
Nutzung (950 Min), und sie **sinkt mit steigender Kundenzufriedenheit**: Das Modell
verdient nur an Kunden, die es nicht nutzen — belegt durch den fonio-Befund
(0,099 €/Min bei Vollausschöpfung gegen 0,10–0,12 € Plattformkosten). Churn 25–40 %,
null Wechselkosten, 594 Kunden für das Ziel. **Nur als Modul innerhalb anderer
Modelle sinnvoll.**

**S03 SHK-Sensorik — Grenzfall.** Der deutsche Heizungswartungsvertrag kostet
**180–350 €/Jahr** [F, neu belegt] statt der US-typischen ~1.000 $. ROI-Faktor beim
Kunden nur ~2,05 statt 6–8. Bei Faktor 2 wird jede Preisrunde zur
Kündigungsdiskussion.

## 5. Drei Modelle mit MRR-Tarnung

Hier sieht der Umsatz wiederkehrend aus, ist es aber nur teilweise. Muss aktiv
verhindert werden:

| Modell | Getarnter Einmalanteil | Wirkung |
|---|---|---|
| **S01** | Prüfvolumen-Durchleitung | senkt die Marge von 87 % auf **44 %** |
| **S05** | Hardware-Verkauf | ~20.280 € je Neukunde |
| **S08** | Setup + Hardware | 48.540 € je Neukunde |
| **S06** | (kein Projektgeschäft, aber) verkapptes Softwareentwicklungsvorhaben | 450.000–900.000 € Vorleistung, 12–18 Monate |

## 6. Zwei Korrekturen an der Shortlist

- **S04:** Die 75–90 % Bruttomarge gelten nur bei **eigener** Leitstelle. Bei
  White-Label-Einkauf sind es **57,9 %** — man kauft Kapitalfreiheit mit rund
  20 Margenpunkten und liegt damit **unter Pflichtkriterium 2**.
- **S03:** Die Rechnung „200 Betriebe × 500 €" hält der deutschen
  Endkundenökonomie nicht stand. Korrigiert: 148 Betriebe bei 680 € ARPU,
  **280 für das echte Ziel**.

## 7. Die überlegene Preis-Logik

**Je Objekteinheit (Aufschaltpunkt, Messstelle), gestaffelt, gegenüber einem Zahler
mit vielen Einheiten** — plus Vertragssockel plus margenstarkes Servicemodul.

Sie löst die Preispunkt-Arithmetik nicht durch Preiserhöhung, sondern durch
**Zählerwechsel**: S08 erreicht 3.800 € ARPU mit 7,90 € je Einheit. Sie multipliziert
ohne Neuverkauf, hält die Marge bei jeder Kundengröße stabil und ist prüfbar — also
unstrittig, was direkt auf den Churn wirkt.

## 8. Setup-Gebühren (Kriterium 18)

Alle acht Modelle sind kombinierbar, aber nur zwei Setup-Gebühren sind im deutschen
Markt hart belegt: **NSL-Einrichtung 150–600 €** (S04) [F] und **FoxifAI 1.920 €**
(S13) [F-sek].

Beste Struktur: **mengenabhängig.** S04: 249 € × Objektzahl = 34.860 € bei
140 Objekten = 14,5× Monats-ARPU. Setup-Marge bewusst auf 35–55 % begrenzen —
sonst optimiert der Vertrieb auf Setups statt auf Bestand.

## 9. Der unbequeme Gesamtbefund

**Kein einziges der acht Modelle erreicht 190.000 €/Monat in 24 Monaten.**
Nur S01 (Monat 21–23) und S02 (Monat 20–22) erreichen überhaupt das
100.000-€-Zwischenziel in diesem Zeitraum.

**Ausnahme von dieser Logik:** Bei S08 und S04 hängt das Ergebnis nicht an der
Vertriebsmenge, sondern an **2–3 Großabschlüssen**. Eine Kooperation mit 600
Filialen bedeutet 38.400 €/Monat aus einem einzigen Vertrag. Dieses Vertriebsspiel
passt zu Nicos Stärkenprofil (verkaufen, präsentieren, überzeugen), während die
Inside-Sales-Alternative unter Annahme A10 ohnehin ausgeschlossen ist.
