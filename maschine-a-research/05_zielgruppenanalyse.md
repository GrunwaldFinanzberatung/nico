# 05 – Zielgruppen- und Problemanalyse

Stand: 2026-08-05 · Detailquelle: `raw/agent04_zielgruppen.md` (22 Zielgruppen, 132×[F], 189×[S], 140×[A])

---

## 1. Der wichtigste Befund: Die kursierenden Zahlen sind unbrauchbar

Sämtliche verbreiteten Angaben zu verpassten Anrufen — „30 % aller
Handwerker-Anrufe gehen verloren", „40–60 % unbeantwortet", „62 % bei kleinen
Dienstleistern", „80–85 % sprechen nicht aufs Band", „bis zu 96.000 €
Umsatzverlust/Jahr" — stammen **ausschließlich von Anbietern von
KI-Telefonassistenten** (agentino.de, telewa.de, vokaro.net, easy-kiagentur.de,
klickautomation.com, digitalolymp.ch, servasbot.at).

**Keine dieser Zahlen ist auf eine Primärstudie, ein Institut oder einen Verband
rückführbar.** Sie sind in dieser Analyse verworfen; gerechnet wurde mit
**konservativ halbierten Annahmen** (Nichtannahmequote 15–25 % statt 30–60 %,
Verlustquote 40–55 % statt 80–85 %).

**Die reale Nichtannahmequote muss im Pilot gemessen werden.** Call-Tracking bei
5–10 Betrieben über 4 Wochen ist der billigste und wichtigste Validierungsschritt
des gesamten Projekts.

---

## 2. Die belegte Obergrenze der Zahlungsbereitschaft im Handwerk

| Kennzahl | Wert | Quelle |
|---|---|---|
| KI-Einsatz im Handwerk | **4 %** (9 % geplant) | [F] Bitkom/ZDH 2025, n=504 |
| Nennen hohe Investitionen als Hemmnis | **69 %** | [F] ebd. |
| Digitalisierungs-Selbstnote | **3,0** | [F] ebd. |
| Kleinstbetriebe: Anteil Digitalisierer / Anteil Ausgaben | **73 % / 24 %** | [F] KfW-Digitalisierungsbericht 2025 |
| **Abgeleitetes Gesamtbudget für ALLE Digitalthemen** | **430–680 €/Monat** | [S] |

Marktpreisanker zum Vergleich: Handwerkersoftware 15–120 €/Nutzer,
Telefonsekretariat 50–250 €/Monat.

**Konsequenz:** Jedes Modell, das von einem Handwerksbetrieb mehr als ~400 €/Monat
für ein einzelnes Thema erwartet, rechnet gegen belegte Daten.

---

## 3. Top 6 Zielgruppen

| # | Zielgruppe | Problem | Schaden/Jahr [S] | Zahlungsbereitschaft/Monat [S] | Kunden für 100k | Größter Einwand |
|---|---|---|---|---|---|---|
| 1 | **Immobilien-/Hausverwaltungen** | 70 % überlastet, 57 % geben Mandate ab, 14 % Aufnahmestopp [F, VDIV] | ~43 T€ direkt + 151 T€ blockiertes Wachstum | **500–1.500 €** (0,30–0,80 €/Einheit) | **100** (0,45 % Marktanteil) | „Muss in Haufe/DOMUS rein, sonst doppelte Pflege" + gedeckelte Verwaltervergütung |
| 2 | **Autohäuser** | Serviceannahme + Lead-Nachverfolgung, 100+ Anrufe/Tag | ~110 T€ DB je Standort | **800–2.500 €** | **83** (0,6 %) | „Der Hersteller schreibt uns die Systeme vor" — **Nicos Anti-Kriterium Konzernabhängigkeit** |
| 3 | **Freie Kfz-Werkstätten** | Verderbliche Hebebühnen-Kapazität, HU-Recall ungenutzt | ~56 T€ DB | 200–450 € | 286 (1,3 %) | „Meine Stammkunden rufen wieder an" + DMS-Integrationspflicht |
| 4 | **SHK-Betriebe** | Kein Innendienst, Umsatz −4 % [F, ZVSHK] | ~32 T€ | 180–350 € | 400 (0,83 %) | „Wir haben genug Arbeit" + extreme Preissensibilität |
| 5 | **Zahnarztpraxen/MVZ** | Neupatienten, No-Shows, Recall | ~74 T€ Umsatz / 48 T€ Gewinn (11 % von 677 T€ [F, KZBV]) | 350–900 € / MVZ 2–8 T€ | 128 (0,3 %) | Art. 9 DSGVO + § 203 StGB |
| 6 | **Steuerkanzleien** | Belegnachlauf, Nachwuchsengpass [F, BStBK] | ~106 T€ | 400–1.500 € | 125 (0,23 %) | „Muss DATEV-kompatibel sein" + Verschwiegenheitspflicht |

---

## 4. Die drei Befunde, die die Modellwahl verändern

### 4.1 Problemgröße und Zahlungsbereitschaft sind negativ korreliert

**Dachdecker haben den höchsten relativen Schaden (13,5 % des Umsatzes) und die
niedrigste Zahlungsbereitschaft (150–300 €/Monat).** Wer dem Schmerz folgt, landet
bei 400–700 Kleinkunden — genau das Modell, das Pflichtkriterium 5 und Nicos
Anti-Kriterien ausschließen.

### 4.2 Weitergebbarkeit der Kosten schlägt Problemstärke

Hausverwaltungen (+12 % Preisanpassung geplant [F]) und Selbstzahlerpraxen können
Kosten durchreichen. SHK, Pflege und GKV-Praxen können es nicht.

**Bei GKV-Arztpraxen greift das Umsatzmodell sogar grundsätzlich nicht:**
budgetiert — mehr Patienten bedeutet mehr Arbeit ohne mehr Geld.
Tiermedizin ist ökonomisch attraktiver als Humanmedizin.

### 4.3 Zwei-Segment-Architektur statt einer Zielgruppe

| Segment | Kunden | ARPU | MRR | Kanal |
|---|---|---|---|---|
| **Ankerkunden** | 70 | 1.400 € | 98.000 € | Direktvertrieb: Verwaltungen, Autohäuser, Kanzleien |
| **Volumenkunden** | 180 | 350 € | 63.000 € | **ausschließlich über Multiplikatoren**: Werkstattkonzepte, SHK-Großhandel, Innungen |
| **Summe** | **250** | | **161.000 €** | |

Das erreicht die korrigierte Zielgröße näherungsweise und respektiert Kriterium 5,
weil die 180 Volumenkunden nicht einzeln verkauft, sondern über eine Handvoll
Multiplikatorverträge gewonnen werden.

---

## 5. Zwei ausdrückliche Abwertungen

- **PV-Installateure:** falsches Problem — die Nachfrage bricht ein, nicht die
  Annahme; plus laufende Insolvenzwelle.
- **Pflegedienste:** SGB-XI-gedeckelte Refinanzierung, Art. 9 DSGVO, hohe Kundenzahl.

## 6. Belegte Anrufvolumina (die einzigen harten Zahlen dieser Art)

- Kleintierpraxis mit 2 Tierärzten: **60–120 Anrufe/Tag** [S, Branchenmedium]
- Hausärztliche Praxis: **100–200 Anrufe/Tag**, konzentriert auf die ersten
  Vormittagsstunden

## 7. Nicht verifiziert

Verbandszahlen für Maler, Bauhauptgewerbe, Metallbau, Küchenstudios, Fensterbauer,
Immobilienverwaltungen (Betriebszahl), Arzt-/Zahnarztpraxen und Energieberater sind
als **[A] – nicht verifiziert** markiert und müssen nachgeprüft werden.
Ursache: erschöpftes Suchkontingent und blockierter Egress.
