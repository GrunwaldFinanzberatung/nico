# 19 – Red-Team-Analyse

Stand: 2026-08-05 · Detailquelle: `raw/agent12_redteam.md` (inkl. Nachtrag zu S08 und zur Kombination)

---

## 1. Überlebensurteil je Modell

| Modell | Urteil | Kern des Angriffs |
|---|---|---|
| **S01** Betreiberpflichten | **angeschlagen** | Margen-Doppelzählung (Durchleitung + 70–85 % geht nicht) · Kern = Fristen/Einzelfälle = Anti-Liste 1+2 · Verkaufszyklus 4–9 Monate · **Angriff von unten** durch bundesweite Multi-Gewerke-Prüfservices (KFK, SI Prüfservice, AB Prüfservice) — die Friedhofsprüfung hatte nur nach oben geschaut |
| **S02** Terminierung | **widerlegt in dieser Form** | kein Burggraben · ARPU real 500–900 € → 210–380 Kunden → verstößt gegen die eigene Filterregel |
| **S03** Sensor-SHK | **widerlegt** | Vaillant 47 €/Monat, Viessmann ViCare, Bosch, Tecalor-Partnerprogramme · SHK-Engpass ist **Kapazität, nicht Nachfrage** · ~1,2 Mio. € Hardwarevorfinanzierung nicht ausgewiesen |
| **S04** Leitstelle | **angeschlagen** | 75–90 % Marge ist ein Rechenfehler (Grenzkosten ≠ Einkaufspreis) → real 45–60 % · Securitas 78.000 Aufschaltungen · WEG-Beschluss = bis 12 Monate |
| **S05** Anlagen-IoT | **angeschlagen/redundant** | strukturgleich mit S03 · Markt besetzt (Tecson, HMS, deltaheat, Pexon) · „> 200 Kunden" ohne ARPU ist ein Warnsignal, kein Beleg |
| **S08** Monitoring B2B2B | **widerlegt (Kühlkette), angeschlagen (Tank/Silo)** | siehe § 3 |
| **S13** Voice-Agent | **widerlegt als eigenständiges Geschäft** | siehe § 2.2 |

---

## 2. Die sechs Angriffe

### 2.1 Angriff 1 — Was hindert Certado oder Vemas am Nachbau?

**Nichts. Und im Nachbarsegment ist es bereits passiert.**

Certado wirbt heute schon damit, dass Prüffristen automatisch überwacht und
**Erinnerungen automatisch versendet** werden — der Unterschied zu Nicos Produkt ist
**ein Kanal, keine Fähigkeit**.

Der Präzedenzfall: **plancraft PORTA** — eigener KI-Telefonassistent, erkennt
Bestandskunden automatisch, standalone oder integriert, **Terminabstimmung auf der
Roadmap**, gebaut vom Software-Inhaber der Kundenbeziehung mit 50 Mio. € im Rücken.
Voisa bietet bereits Schnittstellen zu gängiger Handwerkersoftware.

**Der Satz „Prüfpflicht + KI-Outbound existiert nicht" ist nicht mehr haltbar.**
Vorsprung: 12–18 Monate. Das ist ein Zeitvorsprung, kein Burggraben.

### 2.2 Angriff 4 — Gibt es ein Rettungsargument für S13?

**Nein.** Vier geprüft, alle gefallen:
- „vertikal + tief integriert" → tief integrieren kann, wem die Vertikalsoftware gehört
- „Outbound statt Inbound" → 6–12 Monate Halbwertszeit
- „Pay-per-Outcome" → ein Preismodell, kopierbar in einer Preisliste
- „DSGVO + deutsche Sprachqualität" → war 2024 ein Argument

Placetel, eine Telekom-Tochter, schreibt selbst den Anbietervergleich, in dem es
sich listet. **Die Kategorie ist ein Tarifmerkmal geworden.**

**Die ehrliche Rolle von Voice:** Werkzeug innerhalb eines Modells, in dem Nico die
Kundenbeziehung besitzt — dort ein dauerhafter Kostenvorteil (Cent-Grenzkosten gegen
die Bürokraft des Wettbewerbs), **nutzbar statt verkäuflich**.

### 2.3 Angriff 5 — Erreichen die Modelle 190.000 €/Monat?

**Kein einziges der sechs Modelle erreicht das Ziel mit über 20 % Wahrscheinlichkeit
in 60 Monaten.** Der größte Hebel ist deshalb nicht die Modellwahl, sondern die
**Zielformulierung**: 30 k € *entnommen* verlangt 175–273 k € Umsatz;
Lebensstandard plus Thesaurierung senkt den nötigen Umsatz auf **110–130 k €**.

### 2.4 Angriff 6 — Selbstkritik: die drei riskantesten Annahmen

1. **„Koordinationsmarge 70–90 %"** — belegt nur durch drei Analogien, von denen
   keine ein deutsches Koordinationsgeschäft ist. Bei S01 Doppelzählung, bei S04
   Verwechslung von Grenzkosten mit Einkaufspreis. Bei real 40–55 % verletzen beide
   Spitzenmodelle Kriterium 2. *Irrtumskosten: das Geschäftsmodell. Prüfkosten: drei Telefonate.*
2. **„Preisintransparenz ist ein positives Signal"** — die Umkehrung ist genauso
   plausibel (Einzelfallgeschäft → K.-o. 4). Diese Heuristik hat die gesamte
   Rangfolge erzeugt, in einer Umgebung, in der **keine Anbieterseite lesbar war**.
   Unwissen wird in Attraktivität übersetzt.
3. **„Was wir nicht gefunden haben, existiert nicht"** — die Gegenrecherche hat in
   **4 von 6 Fällen mit je einer Suche** Gegenbelege gefunden. Bei dieser
   Trefferquote liegt die Wahrscheinlichkeit über 80 %, dass zehn weitere Suchen je
   Modell mindestens einen weiteren relevanten Wettbewerber finden.
4. **(Nachtrag) „Die Matrix misst Modellqualität"** — sie misst teilweise
   **Rechercheintensität**. S08 stand oben, weil es unbeschossen war.

---

## 3. Der Nachtrag: S08 und die Kombination

### 3.1 S08 — der vorläufige Sieger, dreifach widerlegt

**Der Markt ist besetzt, in drei Schichten:**
- **Testo Saveris 2/3** — deutscher Messtechnikkonzern, explizit Lebensmittelmärkte,
  Cloud, Multi-Standort, HACCP-Doku, Alarm per SMS/Push
- **Danfoss Alsense** (> 50.000 Food-Retail-Installationen) und **Wurm** (Remscheid,
  W-LINKpro, eigener HACCP-Flyer) **besitzen bereits den Kälteregler in jedem
  Kühlmöbel** — für sie ist HACCP-Doku ein Softwaremodul, für einen Neueinsteiger
  ein Hardware-Rollout
- **TEMPASCAN ab 39 €/Monat** inklusive Sensoren, Gateway, Lizenz und allen
  Behördenberichten → **K.-o. 6 greift**

**Kapitalbedarf, gerechnet:** 8 Messpunkte à 40–80 € + Gateway 150–400 € +
Installation ≈ **900 € je Standort**. 100 k MRR (1.000 Standorte) = **0,9 Mio. €**;
190 k MRR = **1,7 Mio. €** vorfinanzierte Hardware. Payback 12–14 Monate vor CAC.

**Entscheidend ist das Vorzeichen, nicht die Marge:** Bei 50 Neustandorten/Monat
fließen 45.000 € ab und 5.000 € MRR zu. **Ein wachsendes S08 ist operativ dauerhaft
cashflownegativ** — ein Vermietungsgeschäft, das Gegenteil dessen, was der Nordstern
verlangt. Reale Bruttomarge über den Lebenszyklus: **45–60 %**.

**Und das Kernargument kippt:** Die Zentrale kauft zentral — deshalb ist es ein
**12–24-Monats-Ausschreibungsverkauf** mit Präqualifikation, Lastenheft, Pilot,
IT-Freigabe und Einkaufsabteilung. Also exakt „steifes Anzug-Business" und
„Abhängigkeit von Konzernen".

**Querschnittsbefund, der für alle Modelle gilt:** Kriterium 5 und Kriterium 8
stehen **in Spannung**. Unter ~25 Kunden wird Kundenkonzentration beim
Unternehmensverkauf zum **Bewertungsabschlag**, nicht zur Prämie.

### 3.2 Die Kombination — kohärent, aber teuer

**Urteil: kohärent, kein Bastelwerk — eine Sequenz mit hohem Preis.**

Sie ist genau dann ein Unternehmen, wenn die Kundenliste des gekauften Betriebs die
Overlay-Zielgruppe ist. Dann wird das Overlay zum **Upsell an Bestandskunden** — und
entschärft den Einwand, der S01 am härtesten traf („warum vertraut ein
Geschäftsführer einem Neuling?"). Er tut es nicht; er tut es dem Betrieb, der seit
elf Jahren seine Elektroprüfung macht.

**K.-o. 1 ist formal nicht verletzt** (die Elektrofachkraft erbringt die Leistung).
Die Warnung „der Inhaber ist der Betrieb" gilt unter ~5 Mitarbeitern, ab 6–12 mit
angestelltem Meister nicht mehr.

**Verletzt wird stattdessen die Anti-Liste — in den ersten 9–15 Monaten
vollständig, alle zehn Punkte gleichzeitig.**

> **Die ehrliche Formel: Der Zukauf tauscht ein Risiko gegen eine Belastung.**

Mittelfristig löst er das Fit-Problem trotzdem besser als alles andere, weil er als
einziger Pfad die Verwaltungsarbeit **finanzierbar** macht.
Das Bindungsproblem hat eine belegte Lösung: **Das Verkäuferdarlehen (10–30 %) ist
nicht nur Finanzierung, es ist das Bindungsinstrument.**

Zeit vom Kauf zum Plattformbetrieb: **5–7 Jahre.** Ergebnis nach 60 Monaten:
**25–50 k €/Monat Vorsteuergewinn plus 1,5–4 Mio. € Unternehmenswert** [S].

### 3.3 Die ehrlichste Empfehlung

**(b) Zukauf als Startrampe, mit hartem Entscheidungspunkt nach 90 Tagen und
(a) Zielsenkung als benanntem Rückfallpfad.**

(a) allein weicht aus: Ein gesenktes Ziel macht ein unbelegtes Modell nicht
belegter. (b) kauft die drei Dinge, die keine Recherchewelle erzeugen kann:
**Cashflow ab Monat 1, Referenz und Zutritt, Kundenliste mit gesetzlichen
Fälligkeiten.**

**(c′) Buy-and-Build aus 4–6 Betrieben** mit gemeinsamer Steuerungsschicht ist
rechnerisch der **einzige Pfad, der 190 k €/Monat mit über 50 % Wahrscheinlichkeit
erreicht** — gehört aber als Zielbild ab Jahr 4 in die Planung, nicht als Einstieg.

---

## 4. Korrekturvorschläge — was nach unten musste

| Position | Bisher | Korrigiert |
|---|---|---|
| S01 Bruttomarge | 70–85 % | **35–56 %** (Durchleitung) |
| S01 Erlös je Standort | 5.000–30.000 €/Jahr | **3.600–18.000 €** Koordinationsfee, getrennt ausweisen |
| S02 Verteidigbarkeit | „Burggraben dünn" | **„kein Burggraben"** |
| S02 Rang | Platz 2 | **kein eigenständiges Modell; Mechanik** |
| S03 Beleg-Status | „Retention 70→97 %" | **„US-Kontext, nicht übertragbar"** |
| S03 offene Flanke P1 | „ungeprüft" | **„geprüft, negativ"** |
| S04 Bruttomarge | 75–90 % | **45–60 %** |
| S05 | Platz 5 | **mit S03 zusammenlegen, auf Beobachtung** |
| S08 Bruttomarge | 70–85 % | **45–60 %** über den Lebenszyklus |
| S13 | Platz 13 | **streichen; als Querschnittsfähigkeit führen** |
| Alle: Skalierbarkeit | „erreicht 100 k" | **Wahrscheinlichkeit ausweisen, nicht Möglichkeit** |
| Nordstern-Zielgröße | 190–200 k € | **Entnahme- vs. Thesaurierungsszenario rechnen** |

---

## 5. Die Falsifikationsbedingungen der Endempfehlung

Nach Wahrscheinlichkeit geordnet:

1. **Nicos „bereit, operativ zu arbeiten" schließt Personalführung nicht ein.**
   Dann ist die Sequenz falsch, egal wie gut die Rechnung aussieht.
   *Testbar für zwei Tage bei einem befreundeten Betriebsinhaber, bevor eine Due
   Diligence Geld kostet.*
2. **Kapital ist doch verfügbar (> 200 k €).** Dann ist (c′) von Anfang an überlegen.
3. **Die KI-Transparenzansage senkt die Abschlussquote um mehr als ein Drittel.**
   Dann fällt der Kostenvorteil weg, der die Kombination zusammenhält, und (b)
   reduziert sich auf „Nico kauft einen Handwerksbetrieb".
