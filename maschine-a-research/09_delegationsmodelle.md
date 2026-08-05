# 09 – Delegations- und Organisationsmodelle

Stand: 2026-08-05 · Detailquelle: `raw/agent06_delegation.md`

---

## 1. Der Kernbefund

**Delegierbarkeit ist bei 7 von 8 Modellen kein Struktur-, sondern ein
Finanzierungsproblem.** Nico kommt nicht deshalb nicht heraus, weil Aufgaben an ihm
kleben, sondern weil der Deckungsbeitrag in Monat 18 die Rollen nicht bezahlt, die
ihn ersetzen.

Der Ausstieg kostet immer dieselben **~26.000 €/Monat Personalvollkosten** [S] →
bei 75 % Bruttomarge eine Schwelle von **~77.000 €/Monat MRR**.

> **ARPU ist die versteckte Delegierbarkeitsvariable. Jedes Modell mit ARPU unter
> 800 €/Monat reißt die 80-%-Hürde.**

## 2. Prüfdefinition (hart)

Relativtest ≤ 20 % der Peak-Stunden (Monat 4–12) **und** Absoluttest ≤ 8 h/Woche
ab Monat 25. **Beides** muss gelten.

## 3. Rangliste

| Rang | Modell | h/Woche ab M25 | % Peak | Wunschanteil im Rest | 80 % erreicht? |
|---|---|---|---|---|---|
| 1 | **S04** Leitstelle (White-Label) | 4 | 13,3 % | 88 % | **JA** |
| 2 | **S02** Terminierungs-Abo | 5 | 14,7 % | 80 % | **JA** |
| 3 | **S08** Monitoring B2B2B | 6 | 18,2 % | 80 % | **JA** |
| 4 | **S01** Betreiberpflichten | 7 | 18,4 % | 78 % | JA, umsatzabhängig (Median M28–30) |
| 5 | S03 Sensor → Mitgliedschaft | 10 | 26,3 % | 70 % | **NEIN** |
| 6 | S05 Anlagen-IoT | 12 | 33,3 % | 55 % | **NEIN** |
| 7 | S13 Voice-Agent | 12 | 35,3 % | 38 % | **NEIN** |
| 8 | S06 Prüf-SaaS | 15 | 46,9 % | 47 % | **NEIN** |

**Warum die vier scheitern:** S03 und S13 am ARPU (heilbar über das Preismodell) ·
S05 an der Integrationsvielfalt (heilbar nur durch Verengung — dann wird daraus
S08) · S06 an der Time-to-Product (in 24 Monaten nicht heilbar; bei 36 Monaten ja).

## 4. Umsatzschwelle für die erste Vollzeitkraft

Formel: kumulierte Vollkosten ÷ (Bruttomarge × 0,45).
Vollkosten = Bruttogehalt × 1,22 [F-sek: AG-SV 20,5 % + Umlagen/BG] + 6.000 €/Jahr
Arbeitsplatz [A].

| Modell | Erste Vollzeitkraft | Schwelle MRR |
|---|---|---|
| S04 | Objekt-Koordinator | **22.300 €** |
| S02 | Onboarding/Voice-Ops | **22.800 €** |
| S01 / S08 | Compliance-Koordinator / Rollout-PM | **23.700 €** |
| S13 | Implementation Specialist | 26.200 € |
| S03 | CSM/Enablement | 28.500 € |
| S06 | Entwickler | 30.400 € |
| S05 | Applikationsingenieur | 35.600 € |

**Vorgelagert in allen Modellen:** VA/Backoffice 50 % ab **8.000–9.600 € MRR**.
Nicht optional — diese Rolle hält Nicos Anti-Liste von ihm fern und ist der
billigste Delegationshebel überhaupt.

## 5. Die vier Sonderprüfungen

**S01 Partnernetz.** Delegierbar sind Beauftragung, Terminierung,
Qualitätsbeanstandung und Konditionsverhandlung mit Bestandspartnern.
**Klebrig bleiben Erstakquise in neuen Regionen und Partnerkonflikte —
~3 h/Woche dauerhaft.** Bei Fristriss haftet Nicos Firma nicht für die
Betreiberpflicht (die bleibt beim Betreiber), aber zivilrechtlich aus § 280 BGB für
die Koordination. Arbeitnehmerhaftung greift praktisch nicht → **das Fristenrisiko
ist strukturell Unternehmerrisiko und muss durch die Maschine gelöst werden, nicht
durch Personalverantwortung.**

**S02 Prompts und Beschwerden.** Prompt-Bibliothek je Prüfvertikale (6 Templates),
**niemals kundenindividuelle Prompts** — sonst K.-o. 17. Pflege ist Textarbeit plus
A/B-Auswertung, delegierbar an ein Callcenter-Teamleiter-Profil ab Monat 7.
Beschwerden in drei getrennten Kanälen: Endkunde → **vertraglich beim Kunden**
(Anruf unter dessen Rufnummer, White-Label) · Kunde → Kundenbetreuung ·
UWG/Behörde → Nico plus Anwalt, selten.

**S04 Nachtdienst.** Eigenbetrieb erfordert 5,5–6,5 FTE Grundbesetzung
(168 h ÷ 38 h × 1,25 Ausfallfaktor) ≈ **41.200 €/Monat** plus 150.000–400.000 €
Zertifizierung [S/A] → rechnet sich erst ab ~140.000 €/Monat MRR. **Und verletzt
vier von Nicos Kriterien direkt.** Verdikt: **White-Label ist Bedingung, nicht
Option.** Dann ist S04 das delegierbarste Modell überhaupt — und das Hauptrisiko
ist kein Mensch, sondern ein Vertrag (Zweitleitstelle wird ab ~800 Objekten Pflicht).

**S13 Onboarding.** 17–28 h je Kunde initial, 4,5–8,5 h nach Templatisierung [S].
Bei internem Satz 60 €/h deckt das Setup von 1.920 € beides. **Onboarding skaliert —
aber nur bei EINER Vertikale und EINEM Ziel-ERP.** Kein verkapptes Projektgeschäft,
aber haarscharf: Drei Grenzen (mehr als 2 ERPs, Kundenprompts,
Sonderintegrationszusagen) werden unter Umsatzdruck typischerweise überschritten.
Der eigentliche Killer bleibt der ARPU: 229 Kunden à 450 € für den 80-%-Punkt.

## 6. Der universelle Hebel

**Ops-Lead 4–6 Monate vor der rechnerischen Schwelle einstellen, aus Kapital statt
aus Cashflow.** 42.648 € Vorfinanzierung verschieben Nicos 80-%-Punkt um
**4–8 Monate** nach vorn.

Entscheidend für S01, S04 und S08. **Nutzlos für S03, S05, S06 und S13** — dort
fehlt nicht Führung, sondern Umsatz.
