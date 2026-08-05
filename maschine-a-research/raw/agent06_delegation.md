# Agent 06 — Delegations- und Organisationsarchitektur

**Prüffrage:** Kommt Nico bei den TOP-8-Modellen (S01, S02, S03, S04, S05, S06, S08, S13)
in 24 Monaten zu mindestens 80 % aus dem Tagesgeschäft heraus?

Stand: 2026-08-05 · Grundlage: `01_nordstern_und_anforderungen.md`, `13_shortlist.md`
· Recherchebudget: 6 Websuchen (deutsche Gehaltsdaten + Lohnnebenkosten), alles Übrige modelliert.

---

## 0. Zusammenfassung vorab (der eine Befund)

> **Delegierbarkeit ist bei sieben von acht Modellen kein Struktur-, sondern ein Finanzierungsproblem.**
> Nico kommt nicht deshalb nicht raus, weil die Aufgaben an ihm kleben — sondern weil der
> Deckungsbeitrag in Monat 18 die Rollen nicht bezahlt, die ihn ersetzen würden.
> Die 80-%-Frage ist damit in Wahrheit die Frage: **Welches Modell erreicht bis Monat 20
> genug MRR, um 3–5 Vollzeitrollen zu tragen?**

Zweiter Befund, der jede Empfehlung prägt:

> **Der Ausstieg kostet immer dieselben ~26.000 €/Monat Personalvollkosten** (Ops-Lead + Koordination
> + Kundenbetreuung + Vertrieb + Backoffice) [S]. Bei 75 % Bruttomarge und der 45-%-Regel
> (siehe §1.3) entspricht das einer Umsatzschwelle von **~77.000 €/Monat** [S].
> Modelle mit ARPU unter ~800 €/Monat erreichen das in 24 Monaten praktisch nicht,
> weil sie dafür 100+ Kunden brauchen. **ARPU ist die versteckte Delegierbarkeitsvariable.**

---

## 1. Methodik und Rechenwerk

### 1.1 Was „80 % raus" hier heißt — harte, prüfbare Definition

Ein weiches Kriterium wäre wertlos. Ich messe zweistufig, **beide** Bedingungen müssen erfüllt sein:

| Test | Bedingung | Warum |
|---|---|---|
| **Relativtest** | Nicos operative Tagesgeschäftsstunden in Monat 25+ ≤ 20 % seiner Peak-Stunden (Monat 4–12) | die wörtliche Auftragsfrage |
| **Absoluttest** | Nicos operative Tagesgeschäftsstunden in Monat 25+ ≤ **8 h/Woche** | verhindert, dass ein absurd hoher Peak (70 h) die 20-%-Hürde künstlich leicht macht |
| **Abwesenheitstest** (Zusatz, Nordstern §2) | 6 Wochen Abwesenheit ohne Umsatzverlust, ohne Compliance-Bruch, ohne Kundenkündigung | Zielgröße „Abwesenheitsfähigkeit ab Monat 24" |

**„Tagesgeschäft"** = alles, was wiederkehrend anfällt und keine Neuschöpfung ist:
Kundenbetreuung, Support, Eskalation, Disposition, Fristenüberwachung, Abrechnung,
Personalführung im Alltag, einzelne Verkaufsabschlüsse, Lieferantenkoordination, Verwaltung.

**Nicht Tagesgeschäft** (= die erlaubten Reststunden, die *zusätzlich* zu den 8 h zulässig sind):
Vision, Produktarchitektur, Wettbewerbsanalyse, Angebotsentwicklung, strategische Partnerschaften,
Kultur, große Entscheidungen, Führungsteam-Austausch, Aufbau neuer Produkte/Systeme.
Nico darf ab Monat 25 gern 30 h/Woche arbeiten — solange 22 h davon Wunschtätigkeit sind.

### 1.2 Deutsche Personalvollkosten — Rechenweg offengelegt

**Arbeitgeberfaktor:**
Arbeitgeberanteil Sozialversicherung 2026 ≈ **20,5 %** des Bruttos (KV 7,3 % + ~0,9 % halber Zusatzbeitrag,
RV 9,3 %, ALV 1,3 %, PV 1,7 %) [F-sek, sevdesk/taxmaro/lohnklar 2026].
Zuzüglich Umlagen U1/U2/Insolvenzgeld und Berufsgenossenschaft: **2–4 %** [F-sek].
Gesamtband **21–25 %**; Beispielrechnung der Quellen: 4.000 € brutto → 4.970 € Arbeitgeberkosten
= **+24,2 %** [F-sek].
→ Für Büro-/Innendiensttätigkeiten (niedriger BG-Satz) rechne ich mit **Faktor 1,22** [S].

**Arbeitsplatzkosten** (keine belastbare Quelle in den 6 Suchen gefunden → [A]):
6.000 €/Jahr = 500 €/Monat je Kopf.
Rechenweg [A]: Hardware/Abschreibung 100 € + Software-/SaaS-Lizenzen 150 € + Telefonie/Mobil 40 €
+ Raum bzw. Remote-Pauschale 150 € + Weiterbildung/Sonstiges 60 €.
Bandbreite realistisch 4.000–9.000 €/Jahr.

**Einmalkosten Recruiting** (nicht in den Monatskosten enthalten, separat einzuplanen):
15–25 % des Jahresbruttos bei Personalberatung, 2.000–6.000 € bei Eigenrecruiting + Zeitaufwand [A].

**Vollkostentabelle (Grundlage aller Umsatzschwellen unten):**

| # | Rolle | Brutto p. a. | Herkunft der Gehaltszahl | ×1,22 | + AP 6.000 | **Vollkosten p. M.** |
|---|---|---|---|---|---|---|
| R0 | VA / Backoffice (50 %) | 24.000 € [S] | abgeleitet aus Innendienst-Einstieg | 29.280 € | 35.280 € | **2.940 €** |
| R1 | Terminierer / SDR | 42.000 € [S] | Vertriebsinnendienst 25. Perzentil 38.400 € [F-sek Glassdoor 2026] | 51.240 € | 57.240 € | **4.770 €** |
| R2 | Disponent / Koordinator | 45.000 € [S] | Disponent Ø 43.228 € [F-sek jobvector 2026] | 54.900 € | 60.900 € | **5.075 €** |
| R3 | Kundenbetreuer / CSM | 52.000 € [S] | CSM 48.664 € (Indeed) – 57.541 € (jobvector) [F-sek 2026] | 63.440 € | 69.440 € | **5.787 €** |
| R4 | Vertrieb / Closer (Fix) | 55.000 € [S] | Vertriebsinnendienst 75. Perzentil 55.000 € [F-sek Glassdoor 2026] | 67.100 € | 73.100 € | **6.092 €** + Provision |
| R5 | Technischer Innendienst / 2nd Level | 60.000 € [S] | Techn. Support Fachkraft 50.000–83.520 €, Ø 64.500 € [F-sek jobvector 2026] | 73.200 € | 79.200 € | **6.600 €** |
| R6 | Ops-Lead / Teamleiter | 65.000 € [S] | Führungskraft Disposition 61.000 €, Teamleiter Disposition 47.300 € [F-sek 2026] | 79.300 € | 85.300 € | **7.108 €** |
| R7 | Softwareentwickler (Mid/Senior) | 75.000 € [A] | nicht recherchiert, marktüblich DACH | 91.500 € | 99.500 € | **8.292 €** |
| R8 | COO / Betriebsleiter | 95.000 € [S] | Betriebsleiter Ø 57.900 €, oberes Band 69.500 €; GF Kleinunternehmen Ø 85.000 €; COO 144.000 € [F-sek StepStone/gehaltsreporter/Experteer 2026] → Ops-Chef eines 15-Kopf-Betriebs mittig angesetzt | 115.900 € | 123.900 € | **10.325 €** |

**Provision Vertrieb (R4):** zusätzlich 8–12 % des Jahresneuumsatzes bzw. 1,0–1,5 Monatsentgelte
je gewonnenem Jahresvertrag [A]. Nicht in der Fixkostentabelle, aber in der Marge zu berücksichtigen.

### 1.3 Umsatzschwellen-Formel

Eine Rolle ist **nachhaltig** finanziert, wenn die **kumulierten** Personalvollkosten
höchstens 45 % des Deckungsbeitrags I (= Umsatz × Bruttomarge) verbrauchen.
Die übrigen 55 % des DB decken Marketing/Vertriebskosten, Tools, Recht, Versicherung,
Steuerberatung, Risikopuffer und die Ziel-EBITDA-Marge von ≥ 30 %.

> **Umsatzschwelle = kumulierte Personalvollkosten ÷ (Bruttomarge × 0,45)**

Kontrollrechnung bei BM 75 %: Faktor = 1 / (0,75 × 0,45) = **2,96**.
Zum Vergleich: die reine Break-even-Schwelle (Rolle zahlt gerade ihre eigenen Kosten aus dem DB)
wäre Faktor 1,33 — das ist die Zahl, mit der Gründer sich regelmäßig überschätzen.
Ich weise beide aus, empfehle aber ausschließlich die 45-%-Schwelle.

### 1.4 Was in JEDEM Modell ab Tag 1 ausgelagert wird (Nicos Anti-Liste)

Nicos harte Abneigungen (Unterlagen prüfen, Buchhaltung, Excel, Fristen-Einzelfälle, Verwaltung)
dürfen **niemals** durch seine Hände laufen. Das ist keine Frage der Skalierung, sondern der Disziplin
ab Woche 1. Modellunabhängig auszulagern:

| Aufgabe | Auslagerung | Kosten [A] |
|---|---|---|
| Buchhaltung, Lohnabrechnung, Jahresabschluss | Steuerberater + Buchhaltungsservice | 350–800 €/M |
| Belegerfassung, Rechnungslauf, Mahnwesen | VA + automatisierte Rechnungsstellung | 300–600 €/M |
| AGB, AVV, Verträge, Datenschutzdoku | Fachanwalt (Erstellung einmalig, dann Vorlage) | 4.000–9.000 € einmalig |
| Website, Content, Grafik, Video | Freelancer | 800–2.000 €/M |
| Listenrecherche, Datenpflege, CRM-Hygiene | VA / Datenanbieter | 400–900 €/M |
| Softwareentwicklung vor der ersten Festanstellung | Nearshore-Team / Agentur | 6.000–15.000 €/M |
| Physische Logistik, Lager, Versand, RMA (S03/S05/S08) | 3PL-Fulfillment | 300 € + Stückkosten |
| 1st-Level-Telefonsupport in der Frühphase | Teleservice-Dienstleister | 400–1.200 €/M |

**Fixe Regel für alle acht Modelle:** VA/Backoffice (R0) ist die **erste** Einstellung — vor jeder
Fachrolle, ab ca. 8.000–10.000 €/M MRR. Rechenweg: 2.940 € ÷ (0,75 × 0,45) = **8.711 €/M** [S].
Sie kostet am wenigsten und entfernt exakt die Tätigkeiten, die Nico laut Profil am schnellsten auslaugen.

---

## 2. Modellanalysen

---

## S01 — Betreiberpflichten-Manager für Mittelstandsstandorte

**Bruttomarge Annahme: 75 %** (Koordinationsmarge 70–85 % laut Shortlist [S], konservativ).
**ARPU Annahme: 1.250 €/Monat je Standort** (= 15.000 €/Jahr, Mitte des Bandes 5.000–30.000 € [S]).

### 2.1.1 Aufgabenzerlegung

**a) NUR NICO — nicht delegierbar in 24 Monaten**

| Aufgabe | Warum nicht delegierbar | h/Woche Peak |
|---|---|---|
| **Architektur des Pflichten-Regelwerks** (Anlagentyp → Vorschrift → Turnus → Prüferqualifikation → Nachweisform) | Das *ist* das Produkt. Ohne dieses Regelwerk ist jeder Auftrag Handarbeit. Wunschtätigkeit. | 10 |
| Rahmenvertragsarchitektur mit Partnern (Preise, SLA, Pönalen, Haftungsabgrenzung) | Verhandlungsführung + juristische Grundsatzentscheidung; prägt die Marge auf Jahre | 6 |
| Erste 10–15 Referenzkunden auf GF-Ebene | GF-zu-GF-Verkauf ohne Referenzen; Nicos belegte Stärke | 12 |
| Definition der Haftungsgrenze („wir schulden Nachweisfähigkeit, nicht Pflichterfüllung") + Versicherungsdeckung | K.-o.-Kriterium 9; existenzielle Weichenstellung | 3 |
| Aufbau des Partnernetzes in **neuen Regionen** (Erstansprache, Vertrauen, Konditionen) | siehe Sonderprüfung §2.1.6 — teilweise klebrig | 8 |

**b) FRÜH DELEGIERBAR (Monat 1–6)**

- Fristenüberwachung und Vorlauf-Eskalation (T-90/T-60/T-30/T-14) → **Software + R0/R2**
- Terminvereinbarung Standort × Partner → R2 Koordinator
- Auftragsauslösung, Bestellung, Rechnungsprüfung Partner → R0
- Auditakten-Erzeugung, Dokumenten-Upload, Prüfberichts-Ablage → R0 + Software
- Kundenreporting / Monatsstatus → automatisiert + R0
- Ersterfassung/Kataster vor Ort → **Freelance-Ingenieur oder als Erstauftrag an den Partner vergeben**

**c) MITTEL DELEGIERBAR (Monat 7–18)**

- Laufende Partnersteuerung inkl. Qualitätsbeanstandungen → R6 Ops-Lead
- Mängelverfolgung und Nachprüfungslogik (der wertschöpfende Teil!) → R2/R6
- Kundenbetreuung, QBR, Vertragsverlängerung, Upsell weiterer Standorte → R3 CSM
- Neukundenabschluss unterhalb Konzerngröße → R4 Closer
- Normen-/Verordnungs-Monitoring (Änderungen im Regelwerk pflegen) → Fachredaktion, extern oder R5
- Einkaufsverhandlung mit Bestandspartnern → R6

**d) SOFORT AUSLAGERBAR (ab Tag 1)**

Buchhaltung, Verträge, Portal-Entwicklung (Nearshore), Kataster-Begehungen (Freelance-Ingenieur
oder TÜV-nahe Einzelprüfer, 400–800 €/Tag [A]), Marketing/Content, Datenschutz-Dokumentation.

### 2.1.2 Nicos Stundeneinsatz

| Phase | Tagesgeschäft h/Wo | Aufbau-/Wunschtätigkeit h/Wo | Summe | Kommentar |
|---|---|---|---|---|
| Monat 1–3 | 32 [S] | 28 [S] | 60 | Nico ist Vertrieb + Koordinator + Produktarchitekt |
| Monat 4–12 | **38 [S] (Peak)** | 17 [S] | 55 | Peak, weil erste Kunden live gehen und noch keine Ops-Rolle da ist |
| Monat 13–24 | 14 [S] | 20 [S] | 34 | nach R2 + R3, vor bzw. mit R6 |
| ab Monat 25 | **7 [S]** | 24 [S] | 31 | Rest: Partner-Eskalation, Großkunden-QBR, Grundsatzentscheidungen |

Relativtest: 7 ÷ 38 = **18,4 %** ✔ · Absoluttest: 7 ≤ 8 ✔

### 2.1.3 Rollen, Reihenfolge, Umsatzschwellen

Faktor bei BM 75 %: Umsatzschwelle = kumulierte Vollkosten × 2,96.

| # | Monat [S] | Rolle | Vollkosten p. M. | Kumuliert | **Umsatzschwelle MRR** | Kunden à 1.250 € |
|---|---|---|---|---|---|---|
| 1 | 3–5 | R0 VA/Backoffice (50 %) | 2.940 € | 2.940 € | **8.700 €** | 7 |
| 2 | 6–9 | **R2 Koordinator (erste Vollzeitkraft)** | 5.075 € | 8.015 € | **23.700 €** | 19 |
| 3 | 10–14 | R3 Kundenbetreuer / CSM | 5.787 € | 13.802 € | **40.900 €** | 33 |
| 4 | 13–16 | R4 Vertrieb / Closer | 6.092 € | 19.894 € | **58.900 €** | 47 |
| 5 | 17–21 | **R6 Ops-Lead** ← *der Rolle, die Nico rausholt* | 7.108 € | 27.002 € | **80.000 €** | 64 |
| 6 | 22–26 | R2b zweiter Koordinator | 5.075 € | 32.077 € | **95.000 €** | 76 |
| 7 | 28+ | R8 COO | 10.325 € | 42.402 € | **125.600 €** | 100 |

**Erste Vollzeitkraft: Koordinator (R2), Umsatzschwelle 23.700 €/Monat MRR** [S].
Alternativ-Lesart (Break-even statt 45-%-Regel): 6.767 €/M — bewusst nicht empfohlen.

**MRR_80** (Schwelle, ab der die 80-%-Struktur steht) = **80.000 €/Monat** = 64 Standorte.

### 2.1.4 Organigramm Monat 24 (bei ~65.000 €/M MRR, Basisszenario)

```
                         NICO (Geschäftsführer)
                         Vision · Produkt/Regelwerk · Partner-Grundsatz
                         Großkunden · Preisarchitektur
                                    │
        ┌───────────────┬───────────┴───────────┬────────────────┐
        │               │                       │                │
   R6 OPS-LEAD      R4 VERTRIEB            R3 CSM            extern
   (ab M17-21)      Closer KMU          Bestandskunden    · Steuerberater
        │           + Nico bei GF-        QBR/Upsell       · Anwalt
        │             Großkunden                           · Dev-Team
   ┌────┴────┐                                             · Kataster-
   │         │                                               Ingenieure
  R2        R0                                             · 250+ Prüf-
Koordinator  VA/Backoffice                                   partner
Fristen    Rechnungen                                       (Vertrags-
Termine    Auditakten                                        partner,
Partner-   Doku-Ablage                                       keine MA)
disposition
```

Kopfzahl intern Monat 24: **5 + Nico** (R0, R2, R3, R4, R6) [S].

### 2.1.5 Kritische Abhängigkeiten

| Risiko | Schwere | Beschreibung | Gegenmaßnahme |
|---|---|---|---|
| **R6 Ops-Lead** | **hoch** | Kennt alle Fristen, alle Partner, alle Sonderfälle. Geht er, bricht die Nachweisfähigkeit — das einzige Produktversprechen. | Regelwerk und Partnerkonditionen **in der Software**, nie im Kopf. Zwei-Personen-Prinzip bei Fristen ab 40 Standorten. Doppelbesetzung R2/R6 ab MRR 95 k. |
| **Einzelner Prüfpartner mit Regionalmonopol** | mittel-hoch | In dünn besetzten Regionen (Kranprüfung, Aufzug) gibt es 1–2 Anbieter. Deren Preis- oder Terminmacht schlägt direkt auf Marge und SLA durch. | Mindestens 2 Partner je Gewerk je Region als Zielbild; Vertragsklausel Preisanpassung max. Index. |
| **Nico selbst bis Monat 17** | hoch | Vor R6 ist Nico die Eskalationsinstanz und der Partnermanager. Ein 6-Wochen-Ausfall in Monat 12 reißt Fristen. | R2 früher einstellen, notfalls unter der Schwelle mit Puffer. |
| **Fristriss durch Partner** | hoch (siehe unten) | siehe Sonderprüfung | |

### 2.1.6 SONDERPRÜFUNG: Ist Partnernetz-Steuerung delegierbar? Wer haftet intern bei Fristriss?

**Delegierbarkeit — differenziert. Die Antwort ist nicht „ja" und nicht „nein":**

| Teilaufgabe | Delegierbar? | Ab wann |
|---|---|---|
| Beauftragung, Terminierung, Nachhalten, Rechnungsprüfung | **ja, vollständig** | Monat 4–6, an R2 |
| Qualitätsbeanstandung, Nacharbeit einfordern | **ja** | Monat 10–14, an R6 |
| Jährliche Konditionsverhandlung mit **Bestandspartnern** | **ja** | Monat 16–20, an R6 |
| **Erstakquise eines Partners in neuer Region / neuem Gewerk** | **teilweise nein** | bleibt bis Monat 24 zu ~50 % bei Nico |
| **Konflikt mit Partner (Preisdiktat, Qualitätsbruch, Abwerbeversuch beim Endkunden)** | **nein** | Chefsache, dauerhaft ~1–2 h/Woche |

Der klebrige Teil ist die **Erstakquise und die Konfliktlösung**, nicht die laufende Steuerung.
Grund: Ein Prüfpartner gibt einen Teil seiner Kundenbeziehung ab und muss überzeugt werden,
dass Nicos Firma ihn nicht ersetzt, sondern auslastet. Das ist ein Vertrauens- und
Geschäftsmodellgespräch, kein Einkaufsvorgang. Es ist an eine **Rolle** delegierbar
(Partner-/Einkaufsmanager), aber realistisch erst ab MRR ~95.000 €.
→ **Für Monat 24 heißt das: ca. 3 h/Woche Partnerarbeit bleiben bei Nico.**
Das ist innerhalb des 7-h-Budgets, aber es ist der größte Einzelposten.

**Interne Haftung bei Fristriss — die ehrliche Kette:**

1. **Nach außen (gegenüber Behörde/BG):** Nicos Firma haftet **nicht** für die Betreiberpflicht.
   Die Gesamtverantwortung bleibt beim Betreiber [F, laut Shortlist §S01]. Das ist die Basis
   dafür, dass K.-o. 3 nicht verletzt wird — sie darf niemals verwässert werden.
2. **Nach außen (zivilrechtlich gegenüber dem Kunden):** Nicos Firma schuldet aus dem Dienstvertrag
   die **rechtzeitige Veranlassung und Nachweisführung**. Reißt eine Frist, weil die Koordination
   versagt hat, ist das eine Pflichtverletzung nach § 280 BGB [A — von Agent 08 zu verifizieren].
   Typische Folgeschäden: Bußgeld, Betriebsunterbrechung, Versicherungsstreit.
   → **Vermögensschaden-Haftpflicht mit ausdrücklichem Einschluss von Koordinations- und
   Fristversäumnisschäden ist keine Option, sondern Startvoraussetzung.**
3. **Nach innen (Firma ↔ Partner):** Der Partner muss vertraglich für den von ihm verursachten
   Terminverzug einstehen (Pönale, Regress, Deckungsanzeige). Ohne diese Klausel bleibt der
   Schaden vollständig bei Nicos Firma — und die Koordinationsmarge von 75 % wird von einem
   einzigen Vorfall aufgezehrt.
4. **Nach innen (Firma ↔ Mitarbeiter):** Nach deutscher Arbeitnehmerhaftung ist der Koordinator
   bei normaler Fahrlässigkeit praktisch nicht in Regress zu nehmen [A]. **Das Fristenrisiko
   ist also strukturell ein Unternehmerrisiko und muss durch Systemgestaltung, nicht durch
   Personalverantwortung getragen werden.**

**Konsequenz für die Organisation:** Die Fristenüberwachung darf **nie** eine Personenaufgabe
sein. Sie muss eine Maschine sein, die einen Menschen anstößt: automatische Eskalationsstufen,
Zwangsbestätigung, Vier-Augen-Freigabe vor T-30, monatlicher Fristen-Review im Führungsteam.
Wenn das nicht steht, ist S01 kein delegierbares Geschäft, sondern eine tickende Uhr an Nicos Arm.

### 2.1.7 DIE HARTE FRAGE

**JA — aber nur, wenn der Umsatz mitzieht. Im Basisszenario: knapp verfehlt, Ziel Monat 28–30.**

- Strukturell ist S01 hoch delegierbar: das Kerngeschäft *ist* Koordination, und Koordination
  ist eine am Markt gut besetzbare Rolle (Facility-Compliance-Manager, Serviceleiter, Disponent).
- Der Blocker ist arithmetisch: MRR_80 = 80.000 €/M = **64 Standorte**. Bei GF-Ebene-Verkauf mit
  Sales Cycle 4–9 Monaten [A] und Kaltstart ohne Referenzen ist ein Basisszenario von
  **45.000–70.000 €/M in Monat 24** [S] realistisch, also 36–56 Standorte.
- **Was genau blockiert:** die Finanzierbarkeit des Ops-Leads (R6) bei ~80.000 € MRR.
  Ohne R6 bleibt Nico Partnermanager und Eskalationsinstanz → 14–18 h/Woche statt 7.
- Zweiter, kleinerer Blocker: Partner-Erstakquise in neuen Regionen. Der lässt sich durch
  geografische Fokussierung (2–3 Bundesländer statt bundesweit) fast vollständig entschärfen.

**Hebel, der S01 auf JA bringt:** Ops-Lead **vorziehen** auf Monat 14–16 und aus dem Kapitalpuffer
statt aus dem Cashflow finanzieren (6 Monate × 7.108 € = **42.648 € Vorfinanzierung** [S]).
Das ist die wirtschaftlichste Einzelinvestition in Nicos Freiheit im gesamten Projekt.

### 2.1.8 Sind die verbleibenden 20 % Wunsch oder Restmüll?

| Resttätigkeit ab M25 | h/Wo | Wunsch | Restmüll |
|---|---|---|---|
| Partner-Grundsatzverhandlung, neue Gewerke/Regionen | 3 | ✔ (Partnerschaften) | |
| Großkunden-QBR (Konzernstandorte) | 1,5 | ✔ (Präsentieren, Stärke) | |
| Regelwerk-Weiterentwicklung bei Gesetzesänderungen | 1 | ✔ (Produkt) | |
| Eskalation Fristriss / Kundenbeschwerde | 1,5 | | ✘ |

**Urteil: ~78 % Wunschtätigkeit, 22 % Restmüll.** Der Restmüll ist genau das Eskalationsrisiko —
kalkulierbar und über SLA-Automatik weiter reduzierbar. **Gute Restqualität.**

---

## S02 — Terminierungs-Abo für Prüf- und Wartungsdienstleister

**Bruttomarge Annahme: 78 %** (Software + variable Telefoniekosten 0,10–0,12 €/Min [S laut A03]).
**ARPU Annahme: 1.300 €/Monat** (Plattform 500 € + ~67 bestätigte Termine × 12 € [S]).

### 2.2.1 Aufgabenzerlegung

**a) NUR NICO**

| Aufgabe | Warum | h/Wo Peak |
|---|---|---|
| Produktarchitektur des Terminierungs-Stacks (CallSuite-Weiterbau, Tourenlogik, Kalender-Rückschreibung) | Nicos Asset, Nicos Domänenwissen aus der Lead-Ökonomie | 12 |
| Die **Gesprächs-Ökonomie**: Was ist ein „bestätigter Termin", wann wird abgerechnet, wie wird No-Show behandelt | Bestimmt Preismodell und Marge; kann kein Angestellter entscheiden | 4 |
| UWG-Grundsatzklärung + Einwilligungsarchitektur mit Anwalt | Existenzielle Weichenstellung, einmalig | 2 |
| Erste 10 Kunden + Referenzfall mit belegbarer Auslastungssteigerung | Beweislast liegt beim Anbieter | 10 |
| Verhandlung mit den ERP-Herstellern (Certado, Vemas u. a.): Integration oder Konfrontation | Strategische Grundsatzfrage, siehe Burggraben-Flanke | 3 |

**b) FRÜH DELEGIERBAR (Monat 1–6)**

- Datenimport/Fälligkeitsmigration je Neukunde (CSV/Excel/API) → R0 + Skript
- Kampagnen-Ausspielung, Anrufplanung, Wiedervorlagen → automatisiert + R0
- Terminqualitätsprüfung (Stichproben Transkripte) → R0/Werkstudent
- Abrechnung je bestätigtem Termin → automatisiert
- 1st-Level-Support des Kunden („Warum wurde Herr X nicht erreicht?") → externer Teleservice oder R0

**c) MITTEL DELEGIERBAR (Monat 7–18)**

- **Prompt-/Gesprächsleitfaden-Pflege** → siehe Sonderprüfung §2.2.6, Rolle „Voice-Ops"
- Onboarding neuer Kunden komplett → R2/Implementation
- Beschwerdemanagement 2nd Level → R3 CSM
- Neukundenverkauf an KMU-Prüfdienstleister → R4 Closer
- Telefonie-Betrieb (Nummernpool, Reputationsüberwachung, Carrier) → R5 technischer Innendienst

**d) SOFORT AUSLAGERBAR**

Entwicklung (Nearshore), Buchhaltung, Rechtstexte, Transkript-Auswertung (VA),
Lead-Recherche für den eigenen Vertrieb (VA), Website/Content.

### 2.2.2 Nicos Stundeneinsatz

| Phase | Tagesgeschäft h/Wo | Aufbau/Wunsch h/Wo | Summe |
|---|---|---|---|
| Monat 1–3 | 30 [S] | 35 [S] | 65 |
| Monat 4–12 | **34 [S] (Peak)** | 18 [S] | 52 |
| Monat 13–24 | 11 [S] | 21 [S] | 32 |
| ab Monat 25 | **5 [S]** | 25 [S] | 30 |

Relativtest: 5 ÷ 34 = **14,7 %** ✔ · Absoluttest ✔ — **bester Wert nach S04.**

### 2.2.3 Rollen, Reihenfolge, Umsatzschwellen

Faktor bei BM 78 %: Umsatzschwelle = kumulierte Vollkosten ÷ (0,78 × 0,45) = × **2,85**.

| # | Monat [S] | Rolle | Vollkosten | Kumuliert | **Umsatzschwelle** | Kunden à 1.300 € |
|---|---|---|---|---|---|---|
| 1 | 3–5 | R0 VA/Backoffice | 2.940 € | 2.940 € | **8.400 €** | 6 |
| 2 | 6–8 | **R2 Onboarding/Voice-Ops (erste Vollzeitkraft)** | 5.075 € | 8.015 € | **22.800 €** | 18 |
| 3 | 9–13 | R4 Vertrieb / Closer | 6.092 € | 14.107 € | **40.200 €** | 31 |
| 4 | 12–16 | R5 Technischer Innendienst (Telefonie/Stack) | 6.600 € | 20.707 € | **59.000 €** | 45 |
| 5 | 15–19 | R3 CSM / Kundenbetreuung | 5.787 € | 26.494 € | **75.500 €** | 58 |
| 6 | 18–22 | **R6 Ops-Lead** | 7.108 € | 33.602 € | **95.700 €** | 74 |
| 7 | 26+ | R7 fest angestellter Entwickler (statt Agentur) | 8.292 € | 41.894 € | **119.400 €** | 92 |

**Erste Vollzeitkraft: Onboarding-/Voice-Ops (R2), Umsatzschwelle 22.800 €/Monat** [S].

**MRR_80 = 75.500 €/M** — und zwar bereits **vor** dem Ops-Lead, weil bei S02 die Leistung Software ist:
R2 + R5 + R3 zusammen decken den Alltag. R6 verbessert, ist aber nicht Bedingung.
Konservativ mit R6: 95.700 €.

### 2.2.4 Organigramm Monat 24 (bei ~70.000 €/M MRR)

```
                        NICO
                 Produkt · Preis · ERP-Partnerschaften
                 Neue Vertikalen · Großkunden
                             │
     ┌─────────────┬─────────┴─────────┬──────────────┐
     │             │                   │              │
 R5 TECH-OPS   R2 VOICE-OPS/        R4 VERTRIEB    R3 CSM
 Telefonie     ONBOARDING           Closer KMU     Bestand
 Nummernpool   Prompt-Bibliothek                   Churn
 Stack         Kundeneinrichtung                   Upsell
 Integrationen A/B-Tests
     │             │
     └──────┬──────┘
            │
        R0 VA/Backoffice
      Datenimport · Abrechnung · Stichproben
                    │
              extern: Nearshore-Dev (2 FTE) · Teleservice 1st-Level
```

Kopfzahl intern Monat 24: **5 + Nico** [S].

### 2.2.5 Kritische Abhängigkeiten

| Risiko | Schwere | Beschreibung | Gegenmaßnahme |
|---|---|---|---|
| **R5 Tech-Ops (Telefonie-Stack)** | **sehr hoch** | Einzige Person, die Nummernpool, Carrier-Beziehung, Spam-Reputation, Twilio-Konfiguration beherrscht. Fällt sie aus, telefoniert das Produkt nach 2–3 Wochen schlechter, ohne dass jemand versteht warum. **Größtes Schlüsselpersonenrisiko aller acht Modelle.** | Runbooks erzwingen, Konfiguration als Code, zweiter Kopf ab MRR 90 k, Managed-Telefonie-Dienstleister als Rückfallebene. |
| **Rufnummern-Reputation** | hoch | Kein Mensch, sondern ein Systemzustand. Werden Nummern als Spam gelabelt, sinkt die Erreichbarkeit modellweit. | Nummernrotation, Anrufer-Identifikation (CNAM/Branding), strikte Anrufzeitfenster, Opt-out-Automatik. |
| **ERP-Anbieter (Certado, Vemas)** | hoch | Sitzen auf den Fälligkeitsdaten. Bauen sie nach oder sperren die Schnittstelle, verschwindet der Zugang. | Frühe Partnerschaft statt Konfrontation; eigener Fälligkeitsimport ohne API (CSV/Screen) als Rückfall. |
| **Nico bis Monat 8** | hoch | Vor R2 hängt jedes Onboarding an ihm. | R2 als allererste Fachrolle, notfalls Teilzeit ab MRR 15 k. |

### 2.2.6 SONDERPRÜFUNG: Wer betreut die KI-Prompts? Wer klärt Beschwerden über Anrufe?

**Prompts — die Frage entscheidet, ob S02 ein Produkt oder eine Agentur ist.**

Es gibt genau zwei mögliche Architekturen:

| Architektur | Konsequenz |
|---|---|
| **A) Prompt je Kunde individuell** | 5–8 h Tuning pro Kunde und Dauerpflege. Bei 60 Kunden = 1,5 FTE nur Prompt-Pflege. **Das ist verkapptes Projektgeschäft → K.-o. 17.** |
| **B) Prompt-Bibliothek je Prüfvertikale** (DGUV V3, Aufzug, Kälte/F-Gase, Brandschutz, Tor/Rolltor, Leiter/Regal), Kunde konfiguriert nur Variablen (Firmenname, Terminfenster, Tourenraster, Ausnahmen) | Onboarding sinkt auf 2–4 h. Pflege ist zentral: 6 Vertikalen statt 60 Kunden. **Eine Rolle reicht bis ~150 Kunden.** |

**Zwingende Vorgabe: Architektur B ab Kunde 1.** Wenn Kunde 3 einen Sonderprompt bekommt, ist
das Modell für Nicos Zwecke tot. Die Prompt-Bibliothek ist ein **Produkt-Asset** (Kriterium 9)
und gehört in Nicos Wunschbereich — die *Pflege* gehört ab Monat 7 zur Rolle R2 „Voice-Ops".

**Ist Prompt-Tuning delegierbar? Ja, deutlich besser als sein Ruf.**
Es ist Textarbeit plus A/B-Auswertung von Transkripten, kein Entwicklerhandwerk. Passende Profile:
Callcenter-Teamleiter, Vertriebstrainer, Conversation Designer. Gehaltsband entspricht R2/R3
(45.000–52.000 € brutto [S]). **Nicos Rolle dabei ab Monat 12: Zielvorgabe (Terminquote,
Gesprächsdauer, Beschwerdequote), nicht Textredaktion.**

**Beschwerden — drei getrennte Kanäle, drei getrennte Eigentümer:**

| Kanal | Wer beschwert sich | Wer klärt | Ab wann delegiert |
|---|---|---|---|
| **1. Endkunde → Prüfdienstleister** („Ihr Roboter hat mich angerufen") | Endkunde des Kunden | **der Kunde selbst**, mit von Nico gelieferten Textbausteinen und Opt-out-Link | ab Tag 1 vertraglich zugewiesen |
| **2. Kunde → Nicos Firma** („Terminqualität schlecht", „falsche Zeit gebucht") | Prüfdienstleister | R0 (1st Level) → R3 CSM (2nd Level) → R2 Voice-Ops (Ursache) | R0 ab M3, R3 ab M15 |
| **3. Abmahnung / UWG-Beschwerde / BNetzA** | Anwalt der Gegenseite, Behörde | **Nico + Fachanwalt — nicht delegierbar** | dauerhaft, aber selten (< 3 Vorfälle/Jahr erwartet [A]) |

Kanal 1 ist der wichtigste und wird meist übersehen: **Die Beschwerdehoheit gegenüber dem
Endverbraucher muss vertraglich beim Auftraggeber liegen.** Sonst baut Nico ungewollt einen
B2C-Support auf — direkt auf seiner Anti-Liste. Werkzeug dafür: Anrufe erfolgen unter der
Rufnummer und im Namen des Prüfdienstleisters (White-Label), nicht unter Nicos Marke.
Zusatzeffekt: löst gleichzeitig die UWG-Frage teilweise (Bestandskunden-Kontakt zur
Vertragsdurchführung durch den Vertragspartner selbst) — **von Agent 08 zu verifizieren**.

### 2.2.7 DIE HARTE FRAGE

**JA.** S02 ist das Modell mit dem klarsten Ausstiegspfad.

Begründung:
- Die Leistung ist **Software plus Telefonie**, nicht Koordination Dritter und nicht Hardware.
  Es gibt keine physische Welt, in der etwas schiefgehen kann.
- Alle Rollen sind Standardprofile am deutschen Arbeitsmarkt (Onboarding, Support, Vertrieb,
  Telefonie-Technik) — kein Spezialistenmangel.
- **Das Asset senkt die Peak-Belastung real**: CallSuite existiert produktiv, Twilio läuft,
  deutsche Rufnummer vorhanden. Nico startet nicht bei null, sondern bei ~40 % Produkt.
- MRR_80 = 75.500 € = **58 Kunden**. Bei KMU-Inhabern als Käufer (kurzer Cycle, ROI in Euro
  belegbar: mehr Techniker-Auslastung) sind 50–90 Kunden in 24 Monaten realistisch [S].
  **Das ist das einzige Modell, bei dem MRR_24 die Schwelle MRR_80 im Basisszenario überschreitet.**

**Der Rest-Blocker, ehrlich benannt:** die Abhängigkeit von R5. Bis eine zweite technische Person
da ist (MRR ~90 k), springt Nico bei Telefonie-Störungen ein — geschätzt 6–10 Vorfälle im Jahr
à 3–6 h [A]. Das sind im Mittel 0,7 h/Woche und im 5-h-Budget enthalten, kann aber in einer
schlechten Woche 15 h fressen. **Runbook-Pflicht ab Tag 1.**

### 2.2.8 Wunsch oder Restmüll?

| Resttätigkeit ab M25 | h/Wo | Wunsch | Restmüll |
|---|---|---|---|
| Neue Prüfvertikalen definieren (Produkt) | 1,5 | ✔ | |
| ERP-/Verband-Partnerschaften | 1,5 | ✔ | |
| Führungsteam-Review, Zielvorgaben Gesprächsqualität | 1 | ✔ | |
| Telefonie-Störung, UWG-Einzelfall | 1 | | ✘ |

**Urteil: ~80 % Wunschtätigkeit. Beste Restqualität im Feld.**

---

## S03 — Sensor-Monitoring als Motor für Wartungs-Mitgliedschaften

**Bruttomarge Annahme: 68 %** (Sensorik-Zukauf amortisiert, Konnektivität laufend [S]).
**ARPU Annahme: 500 €/Monat je SHK-Betrieb** (laut Shortlist-Rechnung).

### 2.3.1 Aufgabenzerlegung

**a) NUR NICO**
- Produkt- und Geschäftsmodellarchitektur: Was genau kauft der SHK-Betrieb? (Antwort muss
  „Mehrumsatz" sein, nicht „Sensoren") — 8 h/Wo
- **Das Verkaufs-Enablement-Programm** für den SHK-Betrieb (Playbook: wie verkauft er
  Mitgliedschaften an Endkunden). Das ist der eigentliche Wert. Nicos Vertriebsstärke — 8 h/Wo
- Lieferantenauswahl und -verhandlung Sensorik (Stückpreis entscheidet die Marge) — 4 h/Wo
- Erste 15 Referenzbetriebe mit belegter Retentionssteigerung — 10 h/Wo
- Grundsatzentscheidung Herstellerschnittstellen (Vaillant/Viessmann/Bosch): kooperieren oder umgehen — 3 h/Wo

**b) FRÜH DELEGIERBAR (M1–6)**
Bestellabwicklung, Versand, Retouren (→ 3PL), Aktivierung/Provisionierung neuer Sensoren,
Rechnungsstellung, Schulungsvideo-Produktion, Datenpflege.

**c) MITTEL DELEGIERBAR (M7–18)**
Onboarding + Schulung neuer Betriebe (→ R3 CSM), Alarmregel-Tuning je Anlagentyp (→ R5),
2nd-Level-Technik (Konnektivität, Batterie, Fehlalarme) (→ R5), Neukundenvertrieb (→ R4),
**laufendes Enablement-Coaching** (→ R3, nach Playbook-Standardisierung),
Lieferantenbestellwesen (→ R6).

**d) SOFORT AUSLAGERBAR**
Fulfillment/Lager/RMA (3PL), Firmware/App-Entwicklung (Nearshore oder Sensorhersteller),
Buchhaltung, Zertifizierungsberatung (CE/Funk), Content.

### 2.3.2 Nicos Stundeneinsatz

| Phase | Tagesgeschäft | Aufbau/Wunsch | Summe |
|---|---|---|---|
| Monat 1–3 | 30 [S] | 35 [S] | 65 |
| Monat 4–12 | **38 [S] (Peak)** | 17 [S] | 55 |
| Monat 13–24 | 17 [S] | 18 [S] | 35 |
| ab Monat 25 | **10 [S]** | 22 [S] | 32 |

Relativtest: 10 ÷ 38 = 26,3 % ✘ · Absoluttest: 10 > 8 ✘ — **Hürde gerissen.**

### 2.3.3 Rollen und Umsatzschwellen

Faktor bei BM 68 %: × **3,27**.

| # | Monat | Rolle | Vollkosten | Kumuliert | **Umsatzschwelle** | Betriebe à 500 € |
|---|---|---|---|---|---|---|
| 1 | 4–6 | R0 VA/Backoffice | 2.940 € | 2.940 € | **9.600 €** | 19 |
| 2 | 7–10 | **R3 CSM/Enablement (erste Vollzeitkraft)** | 5.787 € | 8.727 € | **28.500 €** | 57 |
| 3 | 11–15 | R5 Technischer Innendienst | 6.600 € | 15.327 € | **50.100 €** | 100 |
| 4 | 14–18 | R4 Vertrieb | 6.092 € | 21.419 € | **70.000 €** | 140 |
| 5 | 18–24 | R3b zweiter CSM | 5.787 € | 27.206 € | **89.000 €** | 178 |
| 6 | 26+ | R6 Ops-Lead | 7.108 € | 34.314 € | **112.200 €** | 224 |

**Erste Vollzeitkraft: CSM/Enablement (R3), Umsatzschwelle 28.500 €/Monat = 57 Betriebe** [S].
**MRR_80 = 112.200 €/M = 224 Betriebe** — mehr als die Shortlist-Zielrechnung (200 Betriebe = 100 k).

### 2.3.4 Organigramm Monat 24 (bei ~50.000 €/M MRR)

```
                      NICO
        Produkt · Sensorlieferant · Hersteller-Politik
        Enablement-Methodik · Großkunden (Verbünde/Kooperationen)
                          │
        ┌─────────────────┼─────────────────┐
        │                 │                 │
   R3 CSM/           R5 TECH-             R4 VERTRIEB
   ENABLEMENT        INNENDIENST          Neukunden SHK
   Onboarding        Konnektivität
   Coaching          Alarmregeln
   Retention         2nd Level
        │                 │
        └────────┬────────┘
                 │
            R0 VA/Backoffice
                 │
   extern: 3PL-Fulfillment · Firmware-Dev · Sensorhersteller (1 Quelle!)
```

### 2.3.5 Kritische Abhängigkeiten

| Risiko | Schwere | Beschreibung |
|---|---|---|
| **Sensorlieferant (kein Mensch, ein Vertrag)** | **sehr hoch** | Ein Hersteller = ein Single Point of Failure für Lieferzeit, Preis, Firmware, Zertifizierung. Bei Chargenfehler steht das ganze Modell. Zweitquelle vor Kunde 50 zwingend. |
| **Heizungshersteller schließt Schnittstelle** | hoch | Aus der Shortlist bekannt. Nicht durch Personal lösbar — nur durch reine Nachrüstsensorik ohne Herstellerabhängigkeit. |
| **R3 Enablement-Person** | hoch | Wenn der SHK-Betrieb nicht verkauft, kündigt er. Die Person, die Betriebe zum Verkaufen bringt, hält den Umsatz. |
| **Nico als Coach** | hoch bis M15 | Das Enablement ist zunächst Nicos persönliche Verkaufskompetenz. Bis daraus ein Playbook wird, ist er der Träger. |

### 2.3.6 DIE HARTE FRAGE

**NEIN — knapp, aber klar. Realistisch Monat 30–36.**

Was genau blockiert (drei Dinge, in dieser Reihenfolge):

1. **Hardware erzeugt einen nie versiegenden Ausnahmestrom.** Lieferengpässe, Chargenfehler,
   Funkabdeckungsprobleme, Batteriewellen, Zollthemen, CE-/Funkzulassungsfragen. Jede einzelne
   Ausnahme ist delegierbar, aber die **Lieferantenbeziehung** ist Chefsache und bleibt bei Nico.
   Geschätzt 3–4 h/Woche dauerhaft [S].
2. **ARPU 500 € gegen MRR_80 von 112.200 €** heißt 224 Betriebe. Bei einer Vertriebsleistung
   von realistisch 6–10 Neubetrieben/Monat ab Monat 12 [A] steht Monat 24 bei 90–150 Betrieben
   = **45.000–75.000 €/M** [S]. Die 80-%-Struktur ist schlicht unbezahlt.
3. **Enablement ist Beratung.** Solange der Kunde nur zahlt, wenn *er* erfolgreich verkauft,
   ist Nicos Firma faktisch in der Vertriebsberatung — mit hoher Betreuungsintensität
   (1 CSM je 50–70 Betriebe [A], das ist eine schlechte Quote) und dauerhaftem Nachjustieren.

**Hebel, die S03 auf JA bringen könnten:** ARPU verdoppeln (Sensor-Miete + Erfolgsanteil an
Mitgliedschaften statt Flat 500 €) → MRR_80 bei 112 Betrieben statt 224 → dann JA.
Oder: Verkauf an SHK-**Verbünde/Kooperationen** statt Einzelbetriebe (Kriterium 5).

### 2.3.7 Wunsch oder Restmüll?

Rest ab M25 (10 h): Lieferantensteuerung 3,5 h (halb Wunsch: technisch/Produkt), Hersteller-Politik
1,5 h (Wunsch), Produktentwicklung 2 h (Wunsch), Eskalationen Betriebe/Retouren 3 h (**Restmüll**).
**Urteil: ~70 % Wunsch, 30 % Restmüll.** Der Hardware-Anteil zieht die Qualität messbar nach unten.

---

## S04 — Aufschalt- und Leitstellen-Modell für Gebäudetechnik

**Bruttomarge Annahme: 80 %** (Grenzkosten 2–5 €/Objekt gegen 20–60 € Erlös [F/S laut Shortlist]).
**ARPU Annahme: 35 €/Objekt/Monat**; **Kunde = Verwalter mit 30–80 Objekten → 1.050–2.800 €/M je Kunde.**

### 2.4.1 Aufgabenzerlegung

**a) NUR NICO**
- Auswahl und Vertrag mit der White-Label-Leitstelle (VdS/DIN EN 50518) — **die eine Entscheidung,
  die alles trägt** — 5 h/Wo in M1–4, danach 1 h
- Aufbau des Interventions-/Befreiungspartnernetzes (Aufzugbefreiung, Havariedienst) je Region — 8 h/Wo
- Preis- und Paketarchitektur (Aufschaltgebühr, Monatspreis, Interventionspauschale) — 3 h/Wo
- Erste 8–12 Verwaltungskunden (Portfolio-Verkauf) — 12 h/Wo
- Rechtsrahmen § 34a GewO / DIN EN 50518 / Notrufkette klären — 2 h/Wo einmalig

**b) FRÜH DELEGIERBAR (M1–6)**
Objekt-Stammdatenpflege, Alarmierungskette je Objekt konfigurieren, Aufschaltungs-Terminierung
mit dem Techniker, Rechnungsstellung je Objekt, Störungsticket-Ersterfassung, Doku nach BetrSichV.

**c) MITTEL DELEGIERBAR (M7–18)**
Objekt-Onboarding komplett inkl. Technikkoordination (→ R2), Fehlalarm-Analyse und Nachjustierung
(→ R2/R5), Verwalter-Betreuung und Portfolioerweiterung (→ R3), Neukundenverkauf (→ R4),
laufende Steuerung der Interventionspartner (→ R6), Leitstellen-SLA-Review (→ R6).

**d) SOFORT AUSLAGERBAR**
**Die gesamte 24/7-Leitstelle (White-Label)**, Gateway-/Router-Montage (Elektro-Partner),
Entwicklung des Kundenportals, Buchhaltung, Recht.

### 2.4.2 Nicos Stundeneinsatz

| Phase | Tagesgeschäft | Aufbau/Wunsch | Summe |
|---|---|---|---|
| Monat 1–3 | 26 [S] | 29 [S] | 55 |
| Monat 4–12 | **30 [S] (Peak)** | 16 [S] | 46 |
| Monat 13–24 | 10 [S] | 18 [S] | 28 |
| ab Monat 25 | **4 [S]** | 22 [S] | 26 |

Relativtest: 4 ÷ 30 = **13,3 %** ✔✔ · Absoluttest ✔ — **bester Wert im gesamten Feld.**

### 2.4.3 Rollen und Umsatzschwellen

Faktor bei BM 80 %: × **2,78**.

| # | Monat | Rolle | Vollkosten | Kumuliert | **Umsatzschwelle** | Objekte à 35 € |
|---|---|---|---|---|---|---|
| 1 | 3–5 | R0 VA/Backoffice | 2.940 € | 2.940 € | **8.200 €** | 234 |
| 2 | 6–9 | **R2 Objekt-Koordinator (erste Vollzeitkraft)** | 5.075 € | 8.015 € | **22.300 €** | 637 |
| 3 | 10–14 | R4 Vertrieb (Verwalter/Portfolios) | 6.092 € | 14.107 € | **39.200 €** | 1.120 |
| 4 | 14–19 | R3 CSM Verwalterbetreuung | 5.787 € | 19.894 € | **55.300 €** | 1.580 |
| 5 | 18–24 | **R6 Ops-Lead** | 7.108 € | 27.002 € | **75.100 €** | 2.146 |
| 6 | 26+ | R2b zweiter Koordinator | 5.075 € | 32.077 € | **89.200 €** | 2.548 |

**Erste Vollzeitkraft: Objekt-Koordinator (R2), Umsatzschwelle 22.300 €/Monat** [S].
**MRR_80 = 55.300 €** (R6 verbessert, ist aber wegen der eingekauften Leistungserbringung
nicht Voraussetzung) — die schlankste Struktur aller acht Modelle.

### 2.4.4 Organigramm Monat 24 (bei ~45.000 €/M MRR ≈ 1.290 Objekte)

```
                       NICO
       Leitstellenvertrag · Interventionspartner-Grundsatz
       Preisarchitektur · Verwalter-Ketten/Verbände · Produkt
                           │
         ┌─────────────────┼─────────────────┐
         │                 │                 │
    R2 OBJEKT-        R4 VERTRIEB        R3 CSM
    KOORDINATOR       Verwalter,         Portfolio-
    Aufschaltung      Genossenschaften   erweiterung
    Alarmketten                          Beschwerden
    Fehlalarm-Analyse
         │
    R0 VA/Backoffice
    Abrechnung je Objekt · Stammdaten · BetrSichV-Doku
         │
  ══════ EXTERN, VERTRAGLICH GEBUNDEN ══════
  · White-Label-Leitstelle 24/7 (VdS/DIN EN 50518)  ← die Leistung
  · Interventions-/Befreiungspartner je Region      ← die Hände
  · Elektro-Montagepartner (Gateways)
  · Portal-Entwicklung
```

Kopfzahl intern Monat 24: **4 + Nico** [S]. **Kein einziger Mitarbeiter im Nachtdienst.**

### 2.4.5 SONDERPRÜFUNG: Schichtbetrieb mit Nachtdienst — wer führt das Team? Verstößt das gegen Nicos Kriterien?

**Die Frage ist die wichtigste des Modells, und sie hat eine eindeutige Antwort:
Nicos Firma darf die Leitstelle NICHT selbst betreiben. Weder in Monat 1 noch in Monat 24.**

**Warum, in Zahlen:**

Eigenbetrieb einer 24/7-Leitstelle erfordert durchgehende Besetzung: 168 h/Woche.
Bei 38 h Wochenarbeitszeit, Urlaub (30 Tage), Krankheit (ca. 6 %), Fortbildung und
Doppelbesetzung in Spitzenzeiten ergibt das **5,5–6,5 FTE nur für die Grundbesetzung** [S].
Rechenweg: 168 ÷ 38 = 4,42 Schicht-FTE; × 1,25 Ausfallfaktor (Urlaub/Krankheit/Schulung) = 5,53.

Kosten: 6 FTE Disponent (R2) × 5.075 € = **30.450 €/Monat**, zuzüglich Nacht-/Sonntagszuschläge
(steuerfrei bis 25 % nachts, 50 % sonntags — für den Arbeitgeber trotzdem Kosten) rund
+12 % [A] → **~34.100 €/Monat**, plus Schichtleitung (R6) 7.108 € → **~41.200 €/Monat** [S].
Plus VdS-/DIN-EN-50518-Zertifizierung, Redundanz-Rechenzentrum, Notstrom, Alarmempfangs-Technik:
einmalig 150.000–400.000 € [A].

Umsatzschwelle für den Eigenbetrieb bei BM-Verschlechterung: **~140.000 €/Monat = 4.000 Objekte** [S].
Das ist jenseits des 24-Monats-Horizonts.

**Warum es Nicos Kriterien verletzen würde (unabhängig vom Geld):**

| Nicos Kriterium | Verletzung durch Eigenbetrieb |
|---|---|
| „nicht bei jedem Mitarbeiterproblem eingebunden sein" | Schichtbetrieb hat die höchste Fluktuation und die meisten Personalkonflikte aller Betriebsformen (Dienstplan, Tauschwünsche, Krankmeldungen um 3 Uhr). |
| „operatives Tagesgeschäft nicht persönlich kontrollieren" | Bis ein Leitstellenleiter finanziert ist (MRR ~75 k), ist Nico faktisch der Dienstplaner. |
| „keine permanente Wochenend-/Notfallarbeit" (K.-o. 7) | Betrifft formal nur Nico — aber die Eskalationsspitze eines 24/7-Betriebs endet in Monat 1–18 immer beim Inhaber. |
| „lockere, bodenständige Kultur" (Kriterium 25) | Ein zertifizierter Alarmbetrieb ist prozessual streng, dokumentationspflichtig und auditiert. Kulturell das Gegenteil. |

**Verdikt:** Als **White-Label-Modell** ist S04 das delegierbarste Modell des gesamten Projekts —
weil die einzige nicht delegierbare Leistung (der Nachtdienst) per Vertrag gar nicht erst
ins Haus kommt. Als **Eigenbetrieb** ist es ein K.-o.-Kandidat.

**Preis dieser Entscheidung, ehrlich:** Die Leitstelle kostet 8–15 €/Objekt/Monat im Einkauf [A].
Bei 35 € Erlös bleiben 20–27 € — die 80 % Bruttomarge halten, aber der Lieferant hält den
Hebel. Zweite Leitstelle als Rückfallebene ist **Pflicht**, nicht Kür.

### 2.4.6 Kritische Abhängigkeiten

| Risiko | Schwere | Beschreibung |
|---|---|---|
| **White-Label-Leitstelle (Lieferantenmonopol)** | **sehr hoch** | Das größte Einzelrisiko des Modells ist kein Mensch, sondern ein Vertrag. Kündigung, Preiserhöhung oder Direktvertrieb des Leitstellenbetreibers an Nicos Kunden zerstört das Modell. Gegenmaßnahmen: mehrjähriger Vertrag mit Kundenschutzklausel, zweite zertifizierte Leitstelle ab 800 Objekten, Alarmempfang technisch abstrahieren (eigene Middleware zwischen Objekt und Leitstelle). |
| **R2 Objekt-Koordinator** | mittel | Kennt die Alarmketten. Aber: die Konfiguration liegt im System, nicht im Kopf → gut ersetzbar. |
| **Interventionspartner je Region** | mittel | Aufzugbefreiung binnen 30 min ist regional; Ausfall = SLA-Bruch. Zwei Partner je Region. |
| **Nico** | niedrig ab M18 | Geringste Personenabhängigkeit aller acht Modelle. |

### 2.4.7 DIE HARTE FRAGE

**JA — strukturell der klarste Ausstieg. Mit einem Vorbehalt beim Umsatztempo.**

- MRR_80 = 55.300 € = **1.580 Objekte** = 25–50 Verwaltungskunden.
- Realistisch Monat 24: **30.000–60.000 €/M** [S] (860–1.700 Objekte). Der Median liegt
  ziemlich genau auf der Schwelle.
- **Was blockieren kann:** nicht die Delegierbarkeit, sondern die Objektakquise. Der ARPU je
  Objekt ist niedrig; jede Wachstumsstufe braucht viele Objekte. Der Ausweg ist strikt der
  Portfolio-Verkauf an Verwalter, Wohnungsgenossenschaften und Facility-Dienstleister — nie
  an Einzeleigentümer. Bei Einzelobjektverkauf bricht das Modell an der Vertriebsökonomie,
  nicht an der Organisation.

### 2.4.8 Wunsch oder Restmüll?

Rest ab M25 (4 h): Leitstellen-/Partner-Grundsatz 1,5 h (Wunsch: Partnerschaften),
Produkt/neue Anlagenklassen 1,5 h (Wunsch), Großkundengespräche 0,5 h (Wunsch),
SLA-Eskalation 0,5 h (Restmüll).
**Urteil: ~88 % Wunschtätigkeit. Bestes Verhältnis im Feld.**

---

## S05 — Herstellerunabhängiges Anlagen-IoT für freie Servicebetriebe

**Bruttomarge Annahme: 70 %** [S]. **ARPU Annahme: 700 €/Monat je Servicebetrieb** [A].

### 2.5.1 Aufgabenzerlegung

**a) NUR NICO**
- Produktarchitektur und **Integrationsstrategie**: Welche Anlagenklassen, welche Protokolle,
  welche Tiefe? — 12 h/Wo
- Auswahl Sensorik-/Gateway-Lieferanten — 4 h/Wo
- Rechtsgrenze „nur auslesend, nie steuernd" durchsetzen (Konformitätsbewertung vermeiden) — 2 h/Wo
- Erste 10 Referenzbetriebe — 10 h/Wo
- **Der Entscheid, welche Kundenanfrage zur Produkt-Roadmap wird und welche abgelehnt wird** —
  die entscheidende Anti-Projektgeschäfts-Grenze — 4 h/Wo, dauerhaft

**b) FRÜH DELEGIERBAR (M1–6)**
Bestellwesen, Gerätelogistik, Abrechnung, Datenpflege, Dokumentation, Testprotokolle.

**c) MITTEL DELEGIERBAR (M7–18)**
Kunden-Onboarding und Inbetriebnahmebegleitung (→ R2), 2nd-Level-Technik (→ R5),
Standard-Integrationen nach Bibliotheksmuster (→ R7 Entwickler), Vertrieb (→ R4),
Betreuung/Retention (→ R3).

**d) SOFORT AUSLAGERBAR**
Plattform-/Firmware-Entwicklung (Nearshore-Team, 2–3 FTE, 8.000–15.000 €/M [A]),
Fulfillment, Buchhaltung, Recht, Zertifizierungsberatung.

### 2.5.2 Nicos Stundeneinsatz

| Phase | Tagesgeschäft | Aufbau/Wunsch | Summe |
|---|---|---|---|
| Monat 1–3 | 28 [S] | 37 [S] | 65 |
| Monat 4–12 | **36 [S] (Peak)** | 20 [S] | 56 |
| Monat 13–24 | 20 [S] | 18 [S] | 38 |
| ab Monat 25 | **12 [S]** | 20 [S] | 32 |

Relativtest: 12 ÷ 36 = 33,3 % ✘ · Absoluttest ✘ — **deutlich gerissen.**

### 2.5.3 Rollen und Umsatzschwellen

Faktor bei BM 70 %: × **3,17**.

| # | Monat | Rolle | Vollkosten | Kumuliert | **Umsatzschwelle** | Betriebe à 700 € |
|---|---|---|---|---|---|---|
| 1 | 4–6 | R0 VA/Backoffice | 2.940 € | 2.940 € | **9.300 €** | 13 |
| 2 | 7–11 | **R7 Entwickler/Applikationsingenieur (erste Vollzeitkraft)** | 8.292 € | 11.232 € | **35.600 €** | 51 |
| 3 | 12–16 | R5 Technischer Innendienst | 6.600 € | 17.832 € | **56.500 €** | 81 |
| 4 | 15–20 | R4 Vertrieb | 6.092 € | 23.924 € | **75.800 €** | 108 |
| 5 | 20–26 | R3 CSM | 5.787 € | 29.711 € | **94.200 €** | 135 |
| 6 | 28+ | R7b zweiter Entwickler + R6 Ops-Lead | 15.400 € | 45.111 € | **143.000 €** | 204 |

**Erste Vollzeitkraft: Entwickler/Applikationsingenieur (R7), Umsatzschwelle 35.600 €/Monat** [S]
— **die teuerste erste Vollzeitkraft aller acht Modelle.** Das ist der Kern des Problems.

**MRR_80 = ~94.200 €** (und selbst dann bleibt Nico Produkt-Gatekeeper).

### 2.5.4 Organigramm Monat 24 (bei ~40.000 €/M MRR)

```
                        NICO
      Produktarchitektur · Integrations-Roadmap (Gatekeeper!)
      Lieferanten · Erste Kunden neuer Anlagenklassen
                            │
            ┌───────────────┼───────────────┐
            │               │               │
      R7 ENTWICKLER    R5 TECH-        R4 VERTRIEB
      Integrationen    INNENDIENST     (ab M15-20)
      Plattform        Support 2nd
            │          Inbetriebnahme
            └───────┬───────┘
                    │
              R0 VA/Backoffice
                    │
        extern: Nearshore-Dev · Sensorlieferanten · 3PL
```

### 2.5.5 Kritische Abhängigkeiten

| Risiko | Schwere | Beschreibung |
|---|---|---|
| **R7 Entwickler / technischer Kopf** | **sehr hoch** | Bei einem Integrationsprodukt sitzt das Wissen im Code und im Kopf. Ein Abgang wirft die Roadmap um 4–6 Monate zurück. Und: Nico ist kein Entwickler — er kann die Person weder fachlich prüfen noch ersetzen. |
| **Integrationsvielfalt (Systemrisiko)** | **sehr hoch** | Jeder neue Anlagentyp eines neuen Kunden ist potenziell Sonderarbeit → schleichender Weg in K.-o. 4 (Sonderanfertigung je Kunde). |
| **Nearshore-Agentur** | hoch | In der Frühphase liegt das Produkt bei einem externen Team ohne Bindung. |
| **Nico als Gatekeeper** | hoch, dauerhaft | Die Entscheidung „das bauen wir / das bauen wir nicht" ist die Überlebensfrage des Modells und delegiert er zuletzt. |

### 2.5.6 DIE HARTE FRAGE

**NEIN. Der Blocker ist strukturell, nicht nur finanziell.**

Drei Blocker:

1. **Die Integrationsvielfalt erzeugt permanente Engineering-Nachfrage.** Ein freier Servicebetrieb
   mit Mischbestand hat per Definition heterogene Anlagen. Jeder Neukunde bringt 1–3 unbekannte
   Anlagentypen mit. Ohne eine harte Produktgrenze („wir unterstützen genau diese 12 Typen")
   wird S05 zum Projektgeschäft — und **mit** dieser Grenze schrumpft der adressierbare Markt.
   Das ist ein echter Zielkonflikt, kein Organisationsproblem.
2. **Die teuerste erste Vollzeitkraft.** 35.600 € MRR Schwelle bedeutet: bis dahin hängt die
   Technik entweder an Nico (der es nicht kann) oder an einer Agentur (die ihn abhängig macht).
   In beiden Fällen ist Monat 1–14 fremdbestimmt.
3. **Nicos Rolle als Produkt-Gatekeeper ist nicht delegierbar** — und sie ist bei diesem Modell
   kein 1-h-Job, sondern eine wöchentliche Priorisierungsschlacht mit Vertrieb und Kunden.

**Was S05 auf JA bringen könnte:** radikale Verengung auf **eine** Anlagenklasse mit
standardisiertem Protokoll (z. B. nur Tankfüllstände, nur Kälteanlagen). Dann konvergiert
S05 gegen S08 — und S08 ist die bessere Version derselben Idee.

### 2.5.7 Wunsch oder Restmüll?

Rest ab M25 (12 h): Produkt/Roadmap 5 h (Wunsch), Lieferanten 2 h (halb Wunsch),
technische Eskalationen und Kundenpriorisierungsstreit 5 h (**Restmüll**).
**Urteil: ~55 % Wunsch, 45 % Restmüll.** Schlechtestes Verhältnis nach S06.

---

## S06 — Prüf-SaaS, das aus dem Mangel ein Angebot macht

**Bruttomarge Annahme: 82 %** (reines SaaS, nach Normlizenzkosten [S]).
**ARPU Annahme: 900 €/Monat je Dienstleister** (Team-Lizenz, 8–15 Techniker) [A].

### 2.6.1 Aufgabenzerlegung

**a) NUR NICO**
- Produktkonzeption: die Mangel-zu-Angebot-Mechanik — das ist der ganze Wettbewerbsvorteil,
  laut Shortlist konzeptionell, nicht technisch — 14 h/Wo
- Normtext-Lizenzverhandlung (DIN/VDE/Beuth) — kostenkritisch und existenziell — 4 h/Wo
- Prüfkatalog-Struktur (welche Norm → welche Prüfpunkte → welches Mangelbild → welches Angebot) — 8 h/Wo
- Erste 10 Design-Partner-Kunden — 10 h/Wo
- Priorisierung der Roadmap — 5 h/Wo dauerhaft

**b) FRÜH DELEGIERBAR (M1–6)**
Buchhaltung, Marketing-Content, Testing, Support-Ticket-Ersterfassung, Datenmigration nach Skript.

**c) MITTEL DELEGIERBAR (M7–18)**
Onboarding/Datenmigration je Kunde (→ R2), Anwenderschulung Techniker (→ R3),
Support 1st/2nd Level (→ R0/R5), Prüfkatalog-Pflege bei Normänderungen (→ Fachredaktion extern
oder R5), Vertrieb (→ R4).

**d) SOFORT AUSLAGERBAR**
Gesamte Softwareentwicklung (Nearshore-Team, 3–4 FTE, 12.000–20.000 €/M [A]),
UX-Design, Fachredaktion Normtexte (freier Sicherheitsingenieur), Recht, Buchhaltung.

### 2.6.2 Nicos Stundeneinsatz

| Phase | Tagesgeschäft | Aufbau/Wunsch | Summe |
|---|---|---|---|
| Monat 1–3 | 20 [S] | 45 [S] | 65 |
| Monat 4–12 | **32 [S] (Peak)** | 28 [S] | 60 |
| Monat 13–24 | 26 [S] | 22 [S] | 48 |
| ab Monat 25 | **15 [S]** | 22 [S] | 37 |

Relativtest: 15 ÷ 32 = 46,9 % ✘✘ · Absoluttest ✘✘ — **klar gerissen.**

### 2.6.3 Rollen und Umsatzschwellen

Faktor bei BM 82 %: × **2,71**.

| # | Monat | Rolle | Vollkosten | Kumuliert | **Umsatzschwelle** | Kunden à 900 € |
|---|---|---|---|---|---|---|
| 1 | 6–9 | R0 VA/Backoffice | 2.940 € | 2.940 € | **8.000 €** | 9 |
| 2 | 10–14 | **R7 Entwickler (erste Vollzeitkraft)** | 8.292 € | 11.232 € | **30.400 €** | 34 |
| 3 | 14–18 | R2 Onboarding/Implementation | 5.075 € | 16.307 € | **44.200 €** | 49 |
| 4 | 18–24 | R4 Vertrieb | 6.092 € | 22.399 € | **60.700 €** | 67 |
| 5 | 24–30 | R3 CSM + R5 Support | 12.387 € | 34.786 € | **94.300 €** | 105 |
| 6 | 32+ | R7b + R6 | 15.400 € | 50.186 € | **136.000 €** | 151 |

**Erste Vollzeitkraft: Entwickler (R7), Umsatzschwelle 30.400 €/Monat** [S].
**MRR_80 ≈ 94.300 €** — plus die Voraussetzung eines fertigen Produkts.

### 2.6.4 Organigramm Monat 24 (bei ~30.000 €/M MRR — Realität, nicht Wunsch)

```
                        NICO
    Produkt (operativ!) · Normlizenzen · Roadmap · Vertrieb bei Großkunden
    → faktisch Head of Product + Head of Sales in Personalunion
                            │
            ┌───────────────┼───────────────┐
            │               │               │
      R7 ENTWICKLER   R2 ONBOARDING    R0 VA/BACKOFFICE
                      Migration
                      Schulung
                            │
   extern: Nearshore-Dev-Team (3 FTE) · Fachredaktion Normen · Recht
```

Kopfzahl intern Monat 24: **3 + Nico** [S] — und Nico ist Vollzeit im Produktbetrieb.

### 2.6.5 Kritische Abhängigkeiten

| Risiko | Schwere | Beschreibung |
|---|---|---|
| **Nico selbst** | **sehr hoch, dauerhaft** | Bei einem konzeptionell (nicht technisch) differenzierten Produkt ist der Konzeptgeber der Engpass. Genau der Fall, den K.-o. 1 verbietet. |
| **Normlizenzgeber (DIN/Beuth)** | hoch | Ohne Lizenz kein Produkt [laut Shortlist]. Kosten unbekannt, Verhandlungsposition schwach. |
| **Entwicklungsteam** | hoch | 12–18 Monate Vorleistung ohne Umsatz. |
| **Adoptionsrisiko in der Fläche** | hoch | Der Prüftechniker in der Halle muss die App wirklich nutzen. Scheitert die Adoption, hilft kein CSM. |

### 2.6.6 DIE HARTE FRAGE

**NEIN — und zwar am deutlichsten von allen acht.**

Was genau blockiert:

1. **Time-to-Product.** Eine Prüf-App mit Offline-Fähigkeit, Mobilerfassung, Normlogik,
   Mangelkatalog, Angebotsgenerator und ERP-Anbindung ist 12–18 Monate Entwicklung [A].
   In Monat 18 hat S06 typischerweise 15–35 Kunden und 15.000–30.000 € MRR [S].
   **Auf diesem Niveau ist keine einzige Entlastungsrolle finanziert außer R0 und R7.**
2. **Nico bleibt Produkt-Operator, nicht Produkt-Visionär.** Der Unterschied ist entscheidend:
   Produktarchitektur ist Wunschtätigkeit; tägliche Spec-Klärung, Bug-Triage, Kundenfeedback-Schleife
   und Release-Koordination sind Tagesgeschäft. In Monat 13–24 dominiert Letzteres.
3. **Der Wettbewerbsvorteil ist konzeptionell** — er lässt sich schlecht in eine Rollenbeschreibung
   schreiben. Was Nico „sieht", sieht ein angestellter Product Owner nicht automatisch.

**S06 ist nicht schlecht — es ist zu langsam für den 24-Monats-Test.** Bei einem 36-Monats-Horizont
kippt das Urteil auf JA (dann ~90.000 € MRR erreichbar und alle Rollen finanziert).
Als **Maschine A unter der 24-Monats-Bedingung: durchgefallen.**

### 2.6.7 Wunsch oder Restmüll?

Rest ab M25 (15 h): Produktvision/Roadmap 5 h (Wunsch), Normlizenzen/Recht 1 h (Restmüll),
Release-/Spec-/Bug-Triage 5 h (**Restmüll, als Produktarbeit getarnt**),
Großkundenvertrieb 2 h (Wunsch), Eskalationen 2 h (Restmüll).
**Urteil: ~47 % Wunsch, 53 % Restmüll.** Schlechtestes Verhältnis im Feld — und das gefährlichste,
weil es sich für Nico anfühlen wird wie Produktarbeit.

---

## S08 — Monitoring-as-a-Service mit B2B2B-Zahler (HACCP / Kühlkette / Silo)

**Bruttomarge Annahme: 75 %** (70–85 % nach Amortisation [S], konservativ).
**ARPU Annahme: 3.200 €/Monat je Kette** (100 Filialen × 4 Sensoren × 8 €/M [S]).

### 2.8.1 Aufgabenzerlegung

**a) NUR NICO**
- Produkt- und Preisarchitektur inkl. Zahlerlogik (Zentrale zahlt, Filiale nutzt) — 6 h/Wo
- Sensor- und Konnektivitätslieferant, Rahmenvertrag mit Mengenstaffel — 4 h/Wo
- Erste 3–5 Ketten (Enterprise-Verkauf, lange Zyklen, Pilot → Rollout) — 14 h/Wo
- Positionierung gegen bestehende Anbieter (Sencono u. a.) und Preisverteidigung — 3 h/Wo
- **Der Alarm-per-Anruf-Differenzierer** (Asset-Verbindung zu CallSuite) als Produktmerkmal — 3 h/Wo

**b) FRÜH DELEGIERBAR (M1–6)**
Geräteversand und Aktivierung, Filial-Stammdatenpflege, Abrechnung, Doku/HACCP-Berichte,
Batteriewechsel-Kampagnenplanung, Ticket-Ersterfassung.

**c) MITTEL DELEGIERBAR (M7–18)**
**Rollout-Projektmanagement je Kette** (die wichtigste Rolle: 100 Filialen in Wellen ausrollen)
(→ R2), Filial-Support 1st/2nd Level (→ R0/R5), Alarm-Schwellwert-Tuning je Warengruppe (→ R5),
Zentralen-Betreuung, QBR, Erweiterung auf weitere Standorte/Sensortypen (→ R3),
Neukunden-Ketten unterhalb Top-Segment (→ R4).

**d) SOFORT AUSLAGERBAR**
3PL-Fulfillment und Batterielogistik, Plattformentwicklung (Nearshore),
Filial-Installation (Elektro-/Servicepartner oder Filialpersonal nach Anleitung),
Kalibriernachweise (akkreditiertes Labor), Buchhaltung, Recht.

### 2.8.2 Nicos Stundeneinsatz

| Phase | Tagesgeschäft | Aufbau/Wunsch | Summe |
|---|---|---|---|
| Monat 1–3 | 28 [S] | 32 [S] | 60 |
| Monat 4–12 | **33 [S] (Peak)** | 18 [S] | 51 |
| Monat 13–24 | 13 [S] | 19 [S] | 32 |
| ab Monat 25 | **6 [S]** | 23 [S] | 29 |

Relativtest: 6 ÷ 33 = **18,2 %** ✔ · Absoluttest ✔

### 2.8.3 Rollen und Umsatzschwellen

Faktor bei BM 75 %: × **2,96**.

| # | Monat | Rolle | Vollkosten | Kumuliert | **Umsatzschwelle** | Ketten à 3.200 € |
|---|---|---|---|---|---|---|
| 1 | 4–6 | R0 VA/Backoffice | 2.940 € | 2.940 € | **8.700 €** | 3 |
| 2 | 7–10 | **R2 Rollout-Projektmanager (erste Vollzeitkraft)** | 5.075 € | 8.015 € | **23.700 €** | 8 |
| 3 | 11–15 | R5 Technischer Innendienst / Support | 6.600 € | 14.615 € | **43.300 €** | 14 |
| 4 | 14–18 | R3 Key-Account / CSM Zentralen | 5.787 € | 20.402 € | **60.400 €** | 19 |
| 5 | 18–23 | R4 Vertrieb Ketten | 6.092 € | 26.494 € | **78.400 €** | 25 |
| 6 | 24–30 | R6 Ops-Lead | 7.108 € | 33.602 € | **99.500 €** | 31 |

**Erste Vollzeitkraft: Rollout-Projektmanager (R2), Umsatzschwelle 23.700 €/Monat = 8 Ketten** [S].
**MRR_80 = 78.400 € = 25 Ketten.**

### 2.8.4 Organigramm Monat 24 (bei ~60.000 €/M MRR ≈ 19 Ketten)

```
                        NICO
      Produkt · Sensorlieferant · Enterprise-Erstgespräche
      Preisarchitektur · neue Vertikalen (Apotheke, Labor, Pharma-Logistik)
                            │
        ┌───────────────┬───┴───────────┬────────────────┐
        │               │               │                │
   R2 ROLLOUT-      R5 TECH-       R3 KEY-ACCOUNT    R4 VERTRIEB
   PROJEKTMGMT      SUPPORT        Zentralen          (ab M18)
   Wellenplanung    Schwellwerte   QBR
   Filialtermine    Filial-2nd     Ausrollung
        │           Level          weiterer Standorte
        └───────┬───────┘
                │
          R0 VA/Backoffice
   Versand · Abrechnung · HACCP-Berichte · Batteriekampagnen
                │
  extern: 3PL · Nearshore-Dev · Installationspartner · Kalibrierlabor
```

Kopfzahl intern Monat 24: **5 + Nico** [S].

### 2.8.5 Kritische Abhängigkeiten

| Risiko | Schwere | Beschreibung |
|---|---|---|
| **Kundenkonzentration** | **sehr hoch** | 19 Ketten in Monat 24 heißt: der größte Kunde ist 15–25 % des Umsatzes. Ein Verlust ist existenziell. **Das ist bei S08 das größte Risiko — größer als jedes Personenrisiko.** Gegenmaßnahme: mehrjährige Verträge mit Kündigungsfrist ≥ 6 Monaten, kein Kunde > 20 % Umsatz ab Monat 30. |
| **R2 Rollout-PM** | hoch | Hält 3–5 parallele Filial-Rollouts. Ausfall verzögert Umsatzstart neuer Ketten um Monate. |
| **Sensorlieferant** | hoch | wie S03: eine Quelle = ein Ausfallpunkt. Vorteil gegenüber S03: **nur eine Sensorklasse (Temperatur/Feuchte)** → Zweitquelle leicht zu finden. |
| **Filial-Support-Flut** | mittel-hoch | 19 Ketten × 100 Filialen = 1.900 potenzielle Anrufer. Muss vertraglich zur Zentrale/deren 1st-Level geschoben werden, sonst frisst der Helpdesk die Marge. |

### 2.8.6 DIE HARTE FRAGE

**JA — mit dem stärksten strukturellen Argument aller Sensormodelle.**

Warum S08 dort funktioniert, wo S03 und S05 scheitern:

| | S03 | S05 | **S08** |
|---|---|---|---|
| Sensorklassen | 3–5 | 8–15 | **1–2** |
| Kunden für MRR_80 | 224 | 135 | **25** |
| Onboarding-Typ | je Betrieb neu | je Anlage neu | **Wellen-Rollout nach Schema** |
| Zahler = Nutzer? | ja | ja | **nein (Zentrale zahlt)** |
| Nicos Rest h/Wo | 10 | 12 | **6** |

Die Homogenität ist der Delegationshebel: Ein Rollout-Projektmanager, der Kette 5 ausrollt,
macht exakt dasselbe wie bei Kette 4. Das ist eine echte Rolle mit einer echten Checkliste.

**Was blockieren kann:** der Vertriebszyklus. Enterprise-Verkauf an Filialzentralen dauert
6–12 Monate von Erstkontakt über Pilot bis Rollout [A]. Nico muss die ersten 3–5 Ketten selbst
holen, und diese Zeit ist Tagesgeschäft im schlechten Sinn (Ausschreibungsunterlagen,
Lieferantenfragebögen, Sicherheitsaudits — Nicos Anti-Liste). Realistisch Monat 24:
**40.000–80.000 €/M** [S], Median über MRR_80.

### 2.8.7 Wunsch oder Restmüll?

Rest ab M25 (6 h): neue Vertikalen und Produkt 2,5 h (Wunsch), Sensorlieferanten 1 h
(halb Wunsch), Enterprise-Erstgespräche/Verbände 1,5 h (Wunsch), Kundenkonzentrations-Management
und Vertragsverhandlungen 1 h (Restmüll).
**Urteil: ~80 % Wunsch.** Gut.

---

## S13 — Vertikaler Voice-Agent mit Tiefenintegration

**Bruttomarge Annahme: 68 %** (60–80 % laut Shortlist, Modellkosten steigen mit Nutzung [S]).
**ARPU Annahme: 450 €/Monat** (FoxifAI-Beleg: 1.920 € Setup + ab 100 €/M [F-sek]; für eine
tief integrierte Vertikallösung realistisch 300–800 €, Mitte 450 €) [S].

### 2.13.1 Aufgabenzerlegung

**a) NUR NICO**
- Wahl und Verteidigung der Vertikalen (welche Branche, welches ERP) — die Überlebensfrage — 6 h/Wo
- Tiefenintegration-Architektur (ein ERP tief statt zehn flach) — 8 h/Wo
- Preisverteidigung gegen den 29-€-Markt: Verpackung, Setup-Gebühr, ROI-Nachweis — 5 h/Wo
- Erste 15 Kunden und der Referenz-Case — 12 h/Wo
- Verhandlung mit dem ERP-/Branchensoftwarehersteller (Partnerschaft oder Verdrängung) — 4 h/Wo

**b) FRÜH DELEGIERBAR (M1–6)**
Rufnummernportierung/SIP-Einrichtung, Wissensbasis-Befüllung nach Fragebogen,
Testanrufe und Protokollierung, Abrechnung, Ticket-Ersterfassung.

**c) MITTEL DELEGIERBAR (M7–18)**
Komplettes Kunden-Onboarding (→ R2 Implementation Specialist),
Prompt-/Gesprächsführungs-Tuning nach Bibliothek (→ R2),
Beschwerde-/Qualitätsfälle (→ R3), Neukundenvertrieb (→ R4),
Telefonie-/Stack-Betrieb (→ R5), Modellwechsel-Regressionstests (→ R5/R7).

**d) SOFORT AUSLAGERBAR**
Entwicklung, Buchhaltung, Recht, Marketing, Transkript-Auswertung (VA).

### 2.13.2 Nicos Stundeneinsatz

| Phase | Tagesgeschäft | Aufbau/Wunsch | Summe |
|---|---|---|---|
| Monat 1–3 | 30 [S] | 32 [S] | 62 |
| Monat 4–12 | **34 [S] (Peak)** | 18 [S] | 52 |
| Monat 13–24 | 22 [S] | 16 [S] | 38 |
| ab Monat 25 | **12 [S]** | 18 [S] | 30 |

Relativtest: 12 ÷ 34 = 35,3 % ✘ · Absoluttest ✘ — **gerissen.**

### 2.13.3 Rollen und Umsatzschwellen

Faktor bei BM 68 %: × **3,27**.

| # | Monat | Rolle | Vollkosten | Kumuliert | **Umsatzschwelle** | Kunden à 450 € |
|---|---|---|---|---|---|---|
| 1 | 3–5 | R0 VA/Backoffice | 2.940 € | 2.940 € | **9.600 €** | 21 |
| 2 | 6–9 | **R2 Implementation Specialist (erste Vollzeitkraft)** | 5.075 € | 8.015 € | **26.200 €** | 58 |
| 3 | 9–13 | R4 Vertrieb | 6.092 € | 14.107 € | **46.100 €** | 102 |
| 4 | 12–17 | R5 Tech-Ops Telefonie/Stack | 6.600 € | 20.707 € | **67.700 €** | 150 |
| 5 | 16–22 | R2b zweiter Implementation Specialist | 5.075 € | 25.782 € | **84.300 €** | 187 |
| 6 | 20–26 | R3 CSM / Churn-Bekämpfung | 5.787 € | 31.569 € | **103.200 €** | 229 |
| 7 | 28+ | R6 Ops-Lead | 7.108 € | 38.677 € | **126.500 €** | 281 |

**Erste Vollzeitkraft: Implementation Specialist (R2), Umsatzschwelle 26.200 €/Monat = 58 Kunden** [S].
**MRR_80 ≈ 103.200 € = 229 Kunden.**

### 2.13.4 SONDERPRÜFUNG: Wer macht Onboarding und Prompt-Tuning je Kunde? Skaliert das, oder ist es verkapptes Projektgeschäft?

**Der Onboarding-Aufwand, aufgeschlüsselt** [S, keine Primärquelle — Modellrechnung]:

| Schritt | Erste 12 Kunden | Nach Templatisierung |
|---|---|---|
| Rufnummer/SIP, Weiterleitungslogik | 2–3 h | 0,5–1 h |
| Anbindung ERP/Kalender/Warenwirtschaft | 4–8 h | 1–2 h (bei *derselben* Vertikale) |
| Wissensbasis (Leistungen, Preise, Zeiten, Ausnahmen) | 3–5 h | 1–2 h (Fragebogen + Import) |
| Gesprächsführungs-Tuning | 4–6 h | 1–1,5 h |
| Testphase mit echten Anrufen + Nachjustierung (4–8 Wochen) | 4–6 h | 1–2 h |
| **Summe** | **17–28 h** | **4,5–8,5 h** |

**Deckt der Preis das?** Setup 1.920 € [F-sek] ÷ interner Vollkostensatz eines Implementation
Specialists. Rechenweg: 5.075 €/M ÷ (4,33 Wochen × 38 h × 0,7 Auslastung) = **44 €/h Vollkosten** [S];
mit Zuschlag für Führung/Overhead **60 €/h** [S].
- Erste Kunden: 22 h × 60 € = **1.320 €** → Setup deckt es, dünn.
- Nach Templatisierung: 6,5 h × 60 € = **390 €** → Setup deckt es klar.
→ **Onboarding skaliert — unter einer harten Bedingung: EINE Vertikale, EIN Ziel-ERP.**
Sobald der zweite ERP-Typ dazukommt, springt der Aufwand zurück auf 17–28 h, und die
Templatisierung beginnt von vorn.

**Prompt-Tuning je Kunde: skaliert nur als Bibliothek.** Wie bei S02 gilt: Vertikale Templates
mit Kundenvariablen — nicht Kundenprompts. Zusätzliches Problem, das S02 nicht hat:
**Modellwechsel.** Ändert der Modellanbieter Version oder Verhalten, muss die gesamte
Bibliothek regressionsgetestet werden. Bei 6 Templates ist das ein Zwei-Tage-Job; bei
200 Kundenprompts ist es unmöglich. Das ist der stärkste Grund für die Bibliotheksarchitektur.

**Ist es verkapptes Projektgeschäft (K.-o. 17)?**
**Nein — aber nur haarscharf, und nur bei strikter Vertikalisierung.** Das Urteil kippt zu „ja",
sobald eine der drei Grenzen überschritten wird:
1. mehr als 2 Ziel-ERPs,
2. individuelle Prompts statt Bibliothek,
3. Zusagen für Sonderintegrationen im Verkaufsgespräch.
Alle drei Grenzen werden unter Umsatzdruck typischerweise überschritten. **Das ist ein
Disziplinrisiko, kein Modellrisiko — aber es ist real.**

### 2.13.5 Organigramm Monat 24 (bei ~35.000 €/M MRR ≈ 78 Kunden)

```
                        NICO
      Vertikalen-Strategie · Preisverteidigung · ERP-Partnerschaft
      + faktisch: Eskalationen, Churn-Gespräche, Modellwechsel-Entscheidungen
                            │
            ┌───────────────┼───────────────┐
            │               │               │
   R2 IMPLEMENTATION   R4 VERTRIEB     R0 VA/BACKOFFICE
   Onboarding                          Abrechnung
   Prompt-Bibliothek                   Testanrufe
   Tuning
            │
   extern: Nearshore-Dev · Telefonie-Provider · Modellanbieter
   ⚠ R5 Tech-Ops erst ab MRR 67.700 € → bis dahin bei Nico oder extern
```

### 2.13.6 Kritische Abhängigkeiten

| Risiko | Schwere | Beschreibung |
|---|---|---|
| **Preisverfall (kein Mensch, ein Markt)** | **sehr hoch** | Telekom im Netz, Placetel 9 €/M, ERP-Hersteller bundeln [laut Shortlist]. Sinkt der ARPU von 450 € auf 250 €, verdoppelt sich die Kundenzahl für jede Rollenschwelle — und Nico kommt nie raus. |
| **Modellanbieter** | hoch | Versionswechsel, Preisänderung, Verhaltensänderung. Nicht steuerbar, nur abfederbar (Abstraktionsschicht, zwei Anbieter). |
| **R2 Implementation Specialist** | hoch | Bei 78 Kunden und einer Person: Urlaub, Krankheit oder Kündigung stoppt jedes Neugeschäft. |
| **Qualitätshaftung für Gesagtes** | mittel-hoch | Sagt die KI einem Endkunden einen falschen Preis oder Termin zu, entsteht beim Kunden Schaden. Vertragliche Haftungsbegrenzung zwingend; die Eskalation landet bis Monat 20 bei Nico. |

### 2.13.7 DIE HARTE FRAGE

**NEIN.**

Was genau blockiert — und es ist nicht die Delegierbarkeit der Aufgaben:

1. **Der ARPU.** Bei 450 €/Monat braucht MRR_80 **229 Kunden**. Selbst bei sehr gutem
   Vertrieb (8–12 Neukunden/Monat ab Monat 10 [A]) und 15 % Jahres-Churn steht Monat 24 bei
   **60–110 Kunden = 27.000–50.000 €/M** [S]. Die entlastenden Rollen 4–6 sind schlicht unbezahlt.
   **Das ist Befund 1 der Shortlist, angewendet auf die Organisationsfrage: Niedriger ARPU
   ist gleichbedeutend mit später Delegierbarkeit.**
2. **Die Rollenanzahl ist bei S13 höher als bei jedem anderen Modell relativ zum Umsatz.**
   Voice braucht gleichzeitig Implementation, Tech-Ops, Vertrieb *und* CSM (weil Churn hoch ist)
   — vier Funktionen, finanziert aus einem der niedrigsten ARPUs im Feld.
3. **Der Churn zwingt Nico ins Kundengespräch.** Bei einem austauschbaren Produkt in einem
   Preiskampf ist der Inhaber das Rückhalteargument. Das ist Tagesgeschäft, das mit der
   Kundenzahl wächst statt zu sinken.

**Was S13 auf JA bringen würde:** ARPU ≥ 900 €/Monat durch echte Tiefenintegration mit
messbarem Umsatzeffekt (Befund 4 der Shortlist) statt Anrufannahme. Dann MRR_80 bei
115 Kunden — grenzwertig machbar. **Unter 900 € ARPU ist S13 organisatorisch nicht zu retten.**

### 2.13.8 Wunsch oder Restmüll?

Rest ab M25 (12 h): Vertikalen-/Produktstrategie 3 h (Wunsch), ERP-Partnerschaft 1,5 h (Wunsch),
Preis-/Churn-Gespräche mit Kunden 4 h (**Restmüll**), technische Eskalation und Modellwechsel 2 h
(**Restmüll**), Beschwerden 1,5 h (**Restmüll**).
**Urteil: ~38 % Wunsch, 62 % Restmüll.** Der schlechteste Wert im Feld — Nico bliebe
Retention-Manager eines Preiskampfprodukts.

---

## 3. Quervergleich

### 3.1 Rangliste nach Delegierbarkeit

| Rang | Modell | Nico h/Wo ab M25 | % vom Peak | Absoluttest ≤ 8 h | Wunschanteil im Rest | **80 % erreicht?** |
|---|---|---|---|---|---|---|
| **1** | **S04** Leitstelle (White-Label) | **4** | 13,3 % | ✔ | 88 % | **JA** |
| **2** | **S02** Terminierungs-Abo | **5** | 14,7 % | ✔ | 80 % | **JA** |
| **3** | **S08** Monitoring B2B2B | **6** | 18,2 % | ✔ | 80 % | **JA** |
| **4** | **S01** Betreiberpflichten-Manager | **7** | 18,4 % | ✔ | 78 % | **JA, aber umsatzabhängig** |
| 5 | S03 Sensor→Wartungs-Mitgliedschaft | 10 | 26,3 % | ✘ | 70 % | **NEIN** |
| 6 | S05 Anlagen-IoT freie Servicebetriebe | 12 | 33,3 % | ✘ | 55 % | **NEIN** |
| 7 | S13 Vertikaler Voice-Agent | 12 | 35,3 % | ✘ | 38 % | **NEIN** |
| 8 | S06 Prüf-SaaS Mangel→Angebot | 15 | 46,9 % | ✘ | 47 % | **NEIN** |

### 3.2 Der zweite, entscheidende Test: Trägt der Umsatz die Struktur?

Delegierbarkeit auf dem Papier ist wertlos, wenn die Rollen nicht bezahlt sind.
**MRR_80** = Umsatz, ab dem die für 80 % nötige Rollenstruktur nach der 45-%-Regel finanziert ist.
**MRR_24** = realistisch erreichbarer MRR in Monat 24 [S, Basisszenario].

| Modell | ARPU/M | Kunden für MRR_80 | **MRR_80** | **MRR_24 (Band)** | Trägt? |
|---|---|---|---|---|---|
| S02 | 1.300 € | 58 | 75.500 € | **50.000–90.000 €** | **ja, Median trifft** |
| S08 | 3.200 € | 25 | 78.400 € | **40.000–80.000 €** | **knapp, oberes Band** |
| S04 | 1.400 €/Verwalter | ~35 Verwalter (1.580 Objekte) | 55.300 € | **30.000–60.000 €** | **knapp, Median trifft** |
| S01 | 1.250 € | 64 | 80.000 € | **45.000–70.000 €** | **nein im Median → M28–30** |
| S03 | 500 € | 224 | 112.200 € | 35.000–60.000 € | nein |
| S13 | 450 € | 229 | 103.200 € | 27.000–50.000 € | nein |
| S05 | 700 € | 135 | 94.200 € | 25.000–50.000 € | nein |
| S06 | 900 € | 105 | 94.300 € | 20.000–45.000 € | nein |

**Die Korrelation ist fast perfekt:** Jedes Modell mit ARPU < 800 €/Monat scheitert an der
80-%-Hürde — nicht wegen klebriger Aufgaben, sondern weil es zu viele Kunden braucht,
um die entlastenden Rollen zu bezahlen. Das validiert Befund 1 der Shortlist aus einer
völlig anderen Richtung.

### 3.3 Umsatzschwelle für die erste Vollzeitkraft (Kernantwort)

| Modell | Erste Vollzeitkraft | Vollkosten p. M. | **Umsatzschwelle** | in Kunden |
|---|---|---|---|---|
| S06 | Entwickler (R7) | 8.292 € | **30.400 €** | 34 |
| S05 | Applikationsingenieur/Entwickler (R7) | 8.292 € | **35.600 €** | 51 |
| S03 | CSM/Enablement (R3) | 5.787 € | **28.500 €** | 57 |
| S13 | Implementation Specialist (R2) | 5.075 € | **26.200 €** | 58 |
| S08 | Rollout-Projektmanager (R2) | 5.075 € | **23.700 €** | 8 Ketten |
| S01 | Compliance-Koordinator (R2) | 5.075 € | **23.700 €** | 19 Standorte |
| S02 | Onboarding/Voice-Ops (R2) | 5.075 € | **22.800 €** | 18 |
| S04 | Objekt-Koordinator (R2) | 5.075 € | **22.300 €** | 637 Objekte / ~12 Verwalter |

Vorgelagert in **allen** Modellen: **VA/Backoffice (50 %) ab 8.000–9.600 €/M MRR**.
Diese Einstellung ist nicht optional — sie hält Nicos Anti-Liste von ihm fern.

### 3.4 Schlüsselpersonenrisiko im Vergleich

| Modell | Wer/was kann das Unternehmen lahmlegen | Typ |
|---|---|---|
| S01 | Ops-Lead (Fristen- und Partnerwissen) | Person |
| S02 | **Tech-Ops Telefonie** (Nummernreputation, Carrier, Stack) | **Person — höchstes Personenrisiko im Feld** |
| S03 | Sensorlieferant (eine Quelle) | Lieferant |
| S04 | **White-Label-Leitstelle** (Vertrag, nicht Mensch) | **Lieferant — höchstes Vertragsrisiko im Feld** |
| S05 | Entwickler + Integrationswissen | Person + System |
| S06 | **Nico selbst** (konzeptioneller Produktvorteil) | **Inhaber → K.-o.-1-Nähe** |
| S08 | Kundenkonzentration (Top-Kunde 15–25 % Umsatz) | Markt |
| S13 | Preisniveau des Marktes + Modellanbieter | Markt + Lieferant |

Bemerkenswert: **Bei den vier bestbewerteten Modellen ist das Hauptrisiko kein Mensch,
sondern ein Vertrag oder eine Kundenstruktur.** Beides ist durch Zweitquellen und
Vertragsgestaltung beherrschbar. Bei den vier schlechteren ist es eine Person oder Nico selbst.

### 3.5 Der universelle Beschleuniger

Über alle acht Modelle hinweg gilt derselbe Hebel:

> **Die entlastende Führungsrolle (Ops-Lead R6) 4–6 Monate VOR der rechnerischen Schwelle
> einstellen und aus Kapital statt Cashflow vorfinanzieren.**
> Kosten: 6 × 7.108 € = **42.648 €** [S].
> Wirkung: verschiebt Nicos 80-%-Punkt um 4–8 Monate nach vorn.

Für S01, S04 und S08 ist das der Unterschied zwischen „Monat 24" und „Monat 30".
Für S03, S05, S06 und S13 reicht es nicht — dort fehlt nicht die Führung, sondern der Umsatz.

---

## 4. Empfehlung aus reiner Delegationssicht

1. **S02** — bester Gesamtausgleich aus Delegierbarkeit (Rang 2), Umsatztempo (einziges Modell,
   dessen Median-MRR_24 über MRR_80 liegt), Asset-Passung und Restqualität (80 % Wunsch).
2. **S04** — höchste strukturelle Delegierbarkeit überhaupt, **unter der zwingenden Bedingung
   White-Label**. Eigenbetrieb der Leitstelle ist ein K.-o.-Kandidat gegen Nicos Kriterien.
3. **S08** — bester Kompromiss aus wenigen großen Kunden und homogener, delegierbarer Leistung.
   Hauptaufgabe: Kundenkonzentration vertraglich absichern.
4. **S01** — strukturell stark, scheitert am Umsatztempo. Wird JA, wenn der Ops-Lead vorfinanziert
   und geografisch fokussiert gestartet wird.
5.–8. **S03, S05, S13, S06** reißen die Hürde. Bei S03 und S13 liegt es am ARPU (heilbar durch
   Preismodell), bei S05 an der Integrationsvielfalt (heilbar nur durch Verengung → wird zu S08),
   bei S06 an der Time-to-Product (nicht heilbar innerhalb von 24 Monaten).

**Warnung an den Orchestrator:** Diese Rangliste bewertet ausschließlich Delegierbarkeit und
Organisationsökonomie (Gewichte 10 % Delegierbarkeit + 10 % Unabhängigkeit von Nico = 20 %
der Gesamtmatrix). Sie ersetzt keine Markt-, Wettbewerbs- oder Finanzbewertung.
Insbesondere sind alle MRR_24-Bänder **[S] ohne Primärquelle** und müssen gegen Agent 07
(Finanzmodell) und Agent 12 (Red Team) gespiegelt werden.

---

## 5. Quellen der Gehaltsdaten

- Vertriebsinnendienst Ø 46.500 €/Jahr, Spanne 38.400–55.000 € — [Glassdoor 2026](https://www.glassdoor.de/Salaries/germany-vertrieb-innendienst-salary-SRCH_IL.0,7_IN96_KO8,28.htm), [jobvector 2026](https://www.jobvector.de/gehalt/vertriebsinnendienst/)
- Customer Success Manager 48.664 €–57.541 €/Jahr — [jobvector 2026](https://www.jobvector.de/gehalt/customer+success+manager/), [Indeed 2026](https://de.indeed.com/career/customer-success-manager/salaries)
- Disponent Ø 43.228 €/Jahr; Führungskraft Disposition 61.000 €; Teamleiter Disposition 47.300 € — [jobvector 2026](https://www.jobvector.de/gehalt/disponent/), [StepStone 2026](https://www.stepstone.de/gehalt/Teamleiter-in-Disposition.html)
- Betriebsleiter Ø 57.900 €, oberes Band 69.500 €; Geschäftsführer Kleinunternehmen Ø 85.000 €; COO Ø 144.000 € — [StepStone 2026](https://www.stepstone.de/gehalt/Betriebsleiter-in.html), [gehaltsreporter 2026](https://gehaltsreporter.de/gehaelter-von-a-bis-z/management-consulting-stabsfunktion/geschaeftsfuehrer), [Experteer 2026](https://www.experteer.de/career/salaries/coo-deutschland)
- Technischer Support Ø 64.500 €/Jahr, Fachkraft 50.000–83.520 €; Servicetechniker Einstieg 39.672 € — [jobvector 2026](https://www.jobvector.de/gehalt/technischer+support/)
- Lohnnebenkosten AG 2026: SV-Anteil ~20,5 %, gesamt 21–25 %; Beispiel 4.000 € brutto → 4.970 € Arbeitgeberkosten (+24,2 %) — [sevdesk 2026](https://sevdesk.de/ratgeber/buchhaltung-finanzen/lohnbuchhaltung/lohnnebenkosten/), [taxmaro 2026](https://www.taxmaro.com/post/lohnnebenkosten-arbeitgeber-2026), [lohnklar 2026](https://lohnklar.de/blog/lohnnebenkosten-2026)

**Nicht recherchiert und daher [A]:** Arbeitsplatzkosten pro Kopf, Entwicklergehälter,
Recruiting-Kosten, VA-Freelancer-Stundensätze, Leitstellen-Einkaufspreise, Sales-Cycle-Längen,
alle MRR_24-Bänder.
