# 16 – MVP-Pläne für die Top 3

Stand: 2026-08-05

Alle drei MVPs sind so geschnitten, dass sie **innerhalb der 30-Tage-Messung aus
`17_100_tage_plan.md` laufen** und mit vorhandenen Mitteln bezahlbar sind. Keiner
verlangt ein fertiges Produkt.

---

## MVP 1 — Die Sequenz: Terminierungsdienst als Türöffner und Deal-Sourcing

### Erstes konkretes Produkt
Ein **bezahlter Terminierungsdienst** für einen einzigen Prüfdienstleister.
Kein Produkt, kein Login, keine Software für den Kunden — eine Dienstleistung,
erbracht mit dem vorhandenen CallSuite-/Twilio-Stack.

### Genaue Zielgruppe
Ein Prüf- oder Wartungsbetrieb mit **200–600 Bestandskunden** und gesetzlich
wiederkehrenden Fälligkeiten (DGUV V3, Brandschutz, Tore, Regale), im Umkreis
von 150 km, mit einem Inhaber, der telefonisch erreichbar ist.

### Akutes Kundenproblem
Die Bürokraft telefoniert drei Tage im Monat die Fälligkeitsliste ab und schafft
60 Kunden. Der Rest fällt still ab. Die Techniker fahren quer durch den Landkreis,
weil Termine nach Eingang statt nach Route gelegt werden.

### Nutzenversprechen
> „Wir rufen alle 400 an, in einer Woche, auch abends — und legen die Termine so,
> dass Ihr Monteur nicht quer durch den Landkreis fährt. Sie zahlen pro
> bestätigtem Termin, nicht pro Anruf."

### Preis
- **Pilotpreis:** 0 € Setup, **12–18 € je bestätigtem Termin**, Abrechnung nach Erfolg
- **Monatliche Gebühr:** im Pilot **keine.** Erst nach dem Pilot: 250 €/Monat
  Plattformgebühr + 12 € je Termin
- Begründung für Erfolgsvergütung: Sie senkt die Kaufhürde beim misstrauischen
  Betriebsinhaber radikal. Sie ist ausdrücklich **kein Dauermodell** — sie ist die
  Einstiegsmechanik in einen Abovertrag (erfolgsabhängig ≠ planbarer MRR)

### Leistungsumfang
200 Bestandskundenanrufe gegen die Fälligkeitsliste · zwei Terminvorschläge je
Anruf, geografisch zur Tour passend · Rückschreibung in eine Liste, die der Kunde
in seine Disposition übernimmt · Tagesreport

### Was ausdrücklich NICHT enthalten ist
Keine Integration in die Software des Kunden · keine Anrufe bei Nicht-Kunden
(**UWG-Grenze**) · keine Angebote oder Upsells im Gespräch (kippt Fall A in
Werbung) · keine Privatkunden im ersten Durchlauf · kein Audio-Rohmitschnitt,
nur Transkript (§ 201 StGB) · keine Zusage einer Terminquote

### 30-Tage-Validierung
Woche 1: Auftraggeber gewinnen (5 Ansprachen) · Woche 2: Liste, Skript, KI-Ansage,
A/B-Aufbau · Woche 3–4: 200 Anrufe, davon 100 mit und 100 ohne KI-Ansage

### Zahlen
| Größe | Ziel |
|---|---|
| Potenzielle Kundenkontakte (Auftraggeber) | 15 Prüfdienstleister |
| Gesprächsziel | 8 Erstgespräche |
| Abschlussziel | **1 bezahlter Pilot** |
| Endkundenanrufe im Pilot | 200 |

### Abbruchkriterien
- Vollkosten je Termin > 40 % des erzielbaren Preises
- **KI-Ansage senkt die Abschlussquote um mehr als 30 %**
- 0 von 15 Prüfdienstleistern unterschreibt

### Benötigte Tools
Vorhanden: CallSuite, Twilio, deutsche Rufnummer, Supabase (`cs_listen`,
`cs_arbeitszeit`). Neu: Voice-Layer (Retell oder Vapi, 0,11–0,31 USD/Min
Vollkosten), ein Transkript-Store. **Kein CRM, kein Frontend.**

### Benötigte Partner
Fachanwalt für Wettbewerbsrecht (UWG-Freigabe des Skripts, ~1.500 €) —
**vor dem ersten Anruf, nicht danach.**

### Erstes Personal
Keines. Nico führt die Akquise selbst; das ist seine Stärke und liefert
gleichzeitig das Deal-Sourcing für den Zukauf.

### Budget
| Position | Betrag |
|---|---|
| Voice-Layer 200 Anrufe à ~3 Min | ~200 € |
| Anwalt UWG + AI-Act-Ansage | 1.500 € |
| Fahrtkosten Erstgespräche | 300 € |
| **Summe** | **~2.000 €** |

### Der eigentliche Zweck
Dieser MVP verkauft nicht nur eine Leistung. Er misst Marge, technische
Machbarkeit, AI-Act-Effekt und Zahlungsbereitschaft in einem Vorgang — **und der
Auftraggeber ist ein qualifizierter Kaufkandidat.**

---

## MVP 2 — S04: Aufschaltung für Hausverwaltungen

### Erstes konkretes Produkt
Aufschaltung der **Aufzugsnotrufe** einer Hausverwaltung auf eine
White-Label-Leitstelle, plus monatlicher Nachweisreport nach BetrSichV.
Nur Aufzüge — kein zweites Gewerk im MVP.

### Genaue Zielgruppe
Hausverwaltung mit **50–300 verwalteten Einheiten** und mindestens 8 Aufzügen im
Bestand. Region Nordwest. Entscheider: Inhaber oder technischer Leiter.

**Warum diese Zielgruppe:** 70 % der Verwaltungen sind überlastet, 57 % geben
Mandate ab, 14 % haben einen Aufnahmestopp [F, VDIV]. Und sie können die Kosten
weiterreichen (+12 % Preisanpassung geplant [F]) — das ist der Befund, der
Problemstärke schlägt.

### Akutes Kundenproblem
BetrSichV verlangt Zweiwege-Notruf und regelmäßige Inaugenscheinnahme. Der
Verwalter hat pro Objekt einen anderen Aufzugsbauer, keinen Gesamtüberblick und
keinen Nachweis auf Knopfdruck — bei persönlicher Verantwortung.

### Nutzenversprechen
> „Alle Ihre Aufzüge auf einer Leitstelle, ein Report, eine Rechnung. Und wenn
> die Behörde fragt, drucken Sie den Nachweis aus, statt zwölf Firmen anzurufen."

### Preis
- **Setup:** 249 € je Objekt (mengenabhängig — bei 12 Aufzügen 2.988 €).
  Das ist der Hebel, der S04 überhaupt finanzierbar macht
- **Monatlich:** 35 € je Aufschaltung
- **Pilotpreis:** Setup halbiert für die ersten drei Kunden, Monatspreis regulär

### Was ausdrücklich NICHT enthalten ist
**Keine Befreiungsorganisation** und keine Intervention (das ist die
§ 34a-Grenze — reine Alarmweiterleitung ist erlaubnisfrei) · keine Wartung ·
keine anderen Gewerke im MVP · keine Haftungsübernahme für die Betreiberpflicht

### 30-Tage-Validierung
Vorgelagert und zwingend: **Einkaufspreis bei drei VdS-Leitstellen erfragen.**
Liegt er über 15 €/Aufschaltung, ist die Marge unter 60 % und das Modell muss neu
gerechnet werden — dann keine Kundenansprache.

### Zahlen
| Größe | Ziel |
|---|---|
| Potenzielle Kundenkontakte | 40 Hausverwaltungen |
| Gesprächsziel | 12 Erstgespräche |
| Abschlussziel | **2 Piloten mit je ≥ 8 Objekten** |

### Abbruchkriterien
- Einkaufspreis Leitstelle > 15 €/Objekt/Monat
- Weniger als 2 von 5 Verwaltern können ohne ETV-Beschluss entscheiden
- 0 Abschlüsse aus 12 Gesprächen

### Benötigte Partner
**VdS-zertifizierte Leitstelle als White-Label-Lieferant.** Das ist der kritische
Pfad — ohne diesen Partner existiert das Modell nicht.

### Budget
| Position | Betrag |
|---|---|
| Aufschaltgeräte 2 Piloten × 10 Objekte | ~4.000 € (vorfinanziert, über Setup gedeckt) |
| Rechtsprüfung § 34a / VdS-Kette | 1.000 € |
| Vertrieb | 500 € |
| **Summe** | **~5.500 €** |

---

## MVP 3 — S01: Betreiberpflichten-Overlay

### Erstes konkretes Produkt
**Ein Kataster, kein Portal.** Aufnahme aller prüfpflichtigen Anlagen eines
Standorts, Fristenkalender, Nachweisakte — geliefert als strukturierte Datei plus
monatliche Fristenmeldung. Software kommt später, wenn drei Kunden zahlen.

### Genaue Zielgruppe
Betriebsstätte mit **50–500 Mitarbeitern**, eine Halle plus Verwaltung.
Entscheider: technischer Leiter oder Geschäftsführer.

### Akutes Kundenproblem
15–18 separate Verträge, 15–18 Fristensysteme, kein Gesamtnachweis — bei
persönlicher Haftung der Geschäftsführung. Über 50 Pflichtvorschriften allein vom
Gesetzgeber [F].

### Nutzenversprechen
> „Sie zahlen heute für ein Programm, das Ihnen sagt, dass Ihr Rolltor fällig ist —
> und rufen den Prüfer trotzdem selbst an. Bei uns steht der Termin im Kalender.
> Und wenn die Behörde kommt, liegt die Akte auf Knopfdruck vor."

### Preis
- **Setup (Standortaufnahme):** 1.500–3.500 € je Standort, mengenabhängig
- **Monatlich:** 300–800 € je Standort (Overlay über bestehende Verträge)
- **Bewusst nicht:** 5.000–30.000 €/Jahr Vollpaket mit Durchleitung des
  Prüfvolumens — das senkt die Marge von 87 % auf 44 % und macht aus einem
  Koordinationsgeschäft ein Durchleitungsgeschäft

### Was ausdrücklich NICHT enthalten ist
**Keine Haftungsübernahme** — die Gesamtverantwortung bleibt beim Betreiber [F],
verkauft wird **Nachweisfähigkeit** · keine eigene Prüfleistung (K.-o. 3) ·
keine Kündigung bestehender Verträge im ersten Jahr · keine Zusage, dass keine
Frist gerissen wird

### 30-Tage-Validierung
20 Anrufe bei technischen Leitern. Frage: *„Wer koordiniert Ihre Prüfungen heute,
mit welchem Werkzeug, und was kostet Sie das intern?"* — **nicht** „hätten Sie
Interesse".

### Zahlen
| Größe | Ziel |
|---|---|
| Potenzielle Kundenkontakte | 20 technische Leiter |
| Gesprächsziel | 20 geführte Gespräche mit konkreter Zahl |
| Abschlussziel | **1 bezahlte Standortaufnahme** (Setup allein, ohne Abo) |

### Abbruchkriterien
- Weniger als 3 von 20 nennen eine konkrete Zahl über 500 €/Monat
- Kein Versicherungsangebot für „Koordination gesetzlicher Prüfpflichten" oder
  Ausschluss der Kernleistung
- Mindestens 5 Anbieter bieten bereits Koordination fremder Gewerke an

### Benötigte Partner
Zwei bis drei Prüfdienstleister je Gewerk als Erbringungspartner ·
Gewerbeversicherungsmakler · Fachanwalt für die Individualvereinbarung

### Erstes Personal
**Ops-/Compliance-Koordinator unter den ersten drei Einstellungen** — nicht der
zehnten. Das ist keine Formalie, sondern die Bedingung, unter der dieses Modell
für Nico überhaupt zulässig ist.

### Budget
| Position | Betrag |
|---|---|
| Anwalt Individualvereinbarung | 3.000 € |
| Versicherungsmakler / Erstprämie anteilig | 1.000 € |
| Vertrieb und Fahrten | 800 € |
| **Summe** | **~4.800 €** |

---

## Was alle drei MVPs gemeinsam haben

1. **Kein Produktbau vor dem ersten bezahlten Kunden.** In allen drei Fällen wird
   eine Dienstleistung verkauft, die Nico manuell erbringen kann. Software entsteht
   erst, wenn dreimal jemand bezahlt hat.
2. **Der Preis wird genannt, nicht erfragt.** „Hätten Sie Interesse" ist keine
   Messung. Eine Unterschrift ist eine.
3. **Rechtliche Freigabe vor dem ersten Kundenkontakt**, nicht danach — UWG bei
   MVP 1, § 34a bei MVP 2, Haftungsbegrenzung bei MVP 3.
4. **Gesamtbudget aller drei MVPs: ~12.300 €** — innerhalb von Annahme A1, selbst
   wenn alle drei parallel getestet werden. Empfohlen wird das nicht: MVP 1 zuerst,
   weil er zugleich Deal-Sourcing liefert.
