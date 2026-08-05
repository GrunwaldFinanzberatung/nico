# 11 – Risiko- und Regulierungsanalyse

Stand: 2026-08-05 · Detailquelle: `raw/agent08_risiko.md`
**Hinweis:** Keine anwaltliche Beratung. Wo anwaltliche Prüfung zwingend ist, steht es dort.

---

## 1. Gesamtrisiko-Ranking (niedrig → hoch)

**S05 → S08 → S03 → S06 → S01 → S02 → S04 → S13**

> **Der unbequeme Befund: Das Ranking korreliert NEGATIV mit der Asset-Passung.
> S02 und S13 nutzen CallSuite am besten und sind die riskantesten Modelle.**

## 2. Die fünf geschäftsentscheidenden Rechtsfragen

### 2.1 UWG § 7 bei Outbound-Terminierung — schneidet den halben Nutzenkern weg

| Fall | Bewertung | Risiko |
|---|---|---|
| **A** Terminfindung innerhalb eines *laufenden* Wartungsvertrags, ohne jedes Angebot | **keine Werbung**, § 7 greift nicht | niedrig |
| **B** Erinnerung an eine Prüfpflicht **ohne** laufenden Vertrag | **ist Werbung.** B2B über mutmaßliche Einwilligung gut vertretbar (konkrete Vorgeschichte nötig, nicht bloß „allgemeiner sachlicher Zusammenhang"). **B2C verboten** | bis **300.000 €** Bußgeld |
| **C** Terminanruf **mit Upsell** | kippt selbst Fall A in Werbung | hoch |

Belegt und zentral: Die Rechtsprechung stuft „Service-Calls" bei Bestandskunden,
die *auch* der Absatzförderung dienen, als Werbung ein. **Der Name ändert nichts.**
Der Shortlist-Pitch „Bestandskunden fallen still ab, wir reaktivieren sie" ist genau
Fall B und bei Privatkunden unzulässig.

**Klumpenrisiko:** § 8 Abs. 2 UWG rechnet den Verstoß dem **Auftraggeber** zu.
Gleiches Skript × 40 Kunden × alle bisherigen Anrufe verwandelt die eigene
Kundenbasis in Regressgläubiger. Kein Einzelschaden — ein korreliertes Risiko.
Beherrschbarkeit: **schlecht.**

### 2.2 EU AI Act — gilt seit dem 2. August 2026

Art. 50 Abs. 1 KI-VO: **Ansage am Gesprächsanfang ist Pflicht**; bei Telefon greift
die Offensichtlichkeits-Ausnahme nie. Sanktion bis 15 Mio. €/3 % (bei KMU der
niedrigere Wert). Niedrigste Regulierungsstufe, kein Zulassungsverfahren, keine
CE-Kennzeichnung. **Compliance kostet ~0 € — aber alle Conversion-Benchmarks dieses
Projekts stammen aus der Zeit davor.**

### 2.3 S01-Haftung — versicherbar ja, per AGB begrenzbar kaum

- VSH deckt Fristversäumnis ausdrücklich als Standard-Schadenbild. Empfohlene
  Deckung 1 Mio. €, für S01 **3 Mio. €**. Prämie ohne Maklerangebot nicht
  ermittelbar ([A] 4.000–10.000 €/Jahr).
- **Drei Deckungslücken:** Bußgelder · Personenschäden (kein Vermögensschaden) ·
  Erfüllungsschäden.
- **AGB-seitig:** Vorsatz und grobe Fahrlässigkeit sind nicht ausschließbar, ein
  Kardinalpflicht-Ausschluss ist unwirksam — **und die Fristenüberwachung IST die
  Kardinalpflicht.**
- **Wirksame Hebel stattdessen:** Individualvereinbarung statt AGB · Leistung
  beschreiben als „Nachweisfähigkeit" statt „sicherstellen" · Gegenzeichnung ·
  Mitwirkungspflichten des Kunden.

### 2.4 S04 Leitstelle — die Abgrenzung trifft den Produktkern

Reine Entgegennahme und Weiterleitung von Alarmen ist ausdrücklich
**erlaubnisfrei**. Erlaubnispflichtig wird es, „sobald Notrufe durch Personen
aufgenommen werden, von denen in Krisensituationen **Aktivitäten erwartet** werden"
— die versprochene **Befreiungsorganisation** fällt darunter. Dazu ist VdS 3138 eine
**Kettenzertifizierung**, die Nicos Glied miterfasst. **White-Label löst das nicht
vollständig.**

### 2.5 DSGVO und § 201 StGB

Aufzeichnung nur mit Einwilligung; **eine Opt-out-Ansage ist laut DSK keine
wirksame Einwilligung** — es braucht aktive Zustimmung. KI-Auswertung ist eine
eigene Verarbeitung, bei Stimmerkennung Art. 9 DSGVO. § 201 StGB trifft den
Geschäftsführer **persönlich** und ist **nicht versicherbar** — aber vollständig
vermeidbar durch die Architekturentscheidung **„kein Audio-Rohmitschnitt, nur
Transkript"**.

## 3. K.-o.-Verstöße

| Modell | Befund |
|---|---|
| **S04** | **K.-o. 3 bedingt VERLETZT.** Zulassung ist der Marktzugang, Zertifikat ist das Produkt. Rettung nur durch Amputation auf rein technische Aufschaltung — dann deutlich schwächer. Zusätzlich K.-o.-5-Verdacht: 75–90 % Marge nicht haltbar, realistisch 45–65 % |
| **S01** | **K.-o. 9 bedingt.** Nicht verletzt, aber **nur** mit GmbH + kombinierter BHV/VSH ≥ 3 Mio. + individuell ausgehandelter Obergrenze + Gegenzeichnung. Ohne alle vier: verletzt, und nicht nachrüstbar. Zusätzlich **K.-o. 10 ernsthaft gefährdet** |
| alle übrigen | kein K.-o.; S13 scheitert nicht am Recht, sondern strategisch |

## 4. Die drei gefährlichsten unbeachteten Risiken

**1. Der Vier-Hürden-Gesprächseinstieg.** KI-Ansage + Art.-14-Information +
ggf. Einwilligung + Rechtsgrundlagenprüfung. Ein *ökonomisches* Risiko aus einer
*Rechtspflicht* — es fällt zwischen Finanz- und Risikoanalyse hindurch. Fällt die
Terminquote von 25 % auf 12 %, kippt jedes Pay-per-Outcome-Modell.
**Billigstes entscheidungsrelevantes Experiment des Projekts: 200 A/B-Testanrufe
über die vorhandene CallSuite, zwei Wochen.**

**2. Carrier-Sperrschalter.** Twilio wird als Asset geführt; es ist zugleich ein
Single Point of Failure, den ein Dritter per Policy abschalten kann — dann sind alle
Kunden gleichzeitig offline. Nur mit Vorlauf beherrschbar: Zweitcarrier, getrennte
Sub-Accounts je Kunde.

**3. Korrelierte UWG-Regresskette bei S02.** Siehe 2.1. Beherrschbarkeit: schlecht.

## 5. Notwendige Absicherungen

| Maßnahme | Betrifft | Kosten [A] |
|---|---|---|
| GmbH statt Einzelunternehmen | alle | 25.000 € Stammkapital (12.500 € eingezahlt), ~1.000 € Gründung |
| Kombinierte BHV/VSH ≥ 3 Mio., Einschluss Koordinationsfehler | S01, S04 | 4.000–10.000 €/Jahr |
| Individualvereinbarung statt AGB | S01 | einmalig 2.000–4.000 € Anwalt |
| Zweitcarrier + Sub-Accounts je Kunde | S02, S13 | technischer Aufwand |
| Architektur „kein Rohmitschnitt, nur Transkript" | S02, S13, S06 | Designentscheidung, 0 € |
| Anwaltliche UWG-Prüfung vor dem ersten Euro | S02 | 1.500 € |

## 6. Offene Punkte

Konkrete Versicherungsprämien (kein Anbieter nennt sie ohne Risikoerfassung) ·
DIN-Media-Lizenzkosten für S06 (individuell verhandelt — **Existenzfrage des
Modells**, mit zwei Telefonaten klärbar) · § 34a-Subsumtion des
White-Label-Konstrukts · Eichrecht bei S08 und CPO-Modellen.
