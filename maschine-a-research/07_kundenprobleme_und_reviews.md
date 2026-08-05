# 07 – Kundenprobleme und Kundensignale

Stand: 2026-08-05 · Quelle: Agent 11 (`raw/agent11_kundensignale.md`)

---

## 0. Ehrlichkeitsvermerk – bitte zuerst lesen

Der Auftrag verlangte **mindestens 40 wörtliche Kundenzitate**. Geliefert wurden
**null verifizierte Zitate**. Das ist kein Versäumnis des Agenten, sondern eine
technische Grenze der Umgebung:

| Kanal | Status |
|---|---|
| WebFetch | **vollständig blockiert** – HTTP 403 auf *jeden* Host, inkl. Wikipedia. Egress-Policy, kein Bot-Schutz. |
| Bash/curl | blockiert – `CONNECT tunnel failed, 403` für reddit.com, trustpilot.com, g2.com, omr.com, handwerk.com, provenexpert.com, ebuero.de |
| Reddit | zusätzlich hart gesperrt, auch über Spiegelinstanzen und `allowed_domains` |
| WebSearch | funktioniert, aber sessionweit geteiltes Budget |

**Der Agent hat korrekt gehandelt und keine Zitate erfunden.** Es wäre trivial
gewesen, 40 plausibel klingende Handwerkerzitate zu schreiben; sie hätten sich
bis in die Endempfehlung fortgepflanzt und wären nicht mehr rückverfolgbar
gewesen.

**Konsequenz für die Bewertung:** Aus diesem Dokument darf **kein Modell
Punkte** in den Kategorien „Reale, nachweisbare Nachfrage" (Kriterium 10) oder
„Klare Zahlungsbereitschaft" (Kriterium 11) beziehen. Für Voice-AI-Modelle ist
die Freedom-Inbound-Neutralität aus Methodik-Regel 11 nach diesem Lauf sogar
**strenger** anzuwenden: Die Arbeitshypothese hat *weniger* Belegunterstützung
als vorher, nicht mehr.

**Erfassungsgrad:** Voice AI ~35 % (ausschließlich US-Markt) · Handwerkersoftware
0 % · deutsche KMU-Schmerzpunkte 0 % · Wartungsverträge 0 %.

---

## 1. Der wichtigste Befund: Der Review-Korpus ist vergiftet

In allen Suchen zu KI-Telefonassistenten dominierten nicht Kundenstimmen,
sondern **„Review"-Artikel direkter Wettbewerber** — 13 identifizierte Fälle
(Synthflow bewertet Goodcall, Retell bewertet Synthflow, Thoughtly bewertet
Retell, ServiceAgent bewertet Smith.ai/Goodcall/Rosie usw.). Details in
`06_wettbewerbsanalyse.md` §4.

**Das ist selbst ein verwertbares Marktsignal, kein bloßes Ärgernis:**

Ein Handwerksmeister, der „KI Telefonassistent Erfahrungen" googelt, findet
ausschließlich Verkäufer, die sich gegenseitig schlechtschreiben. **In dieser
Kategorie ist Vertrauen der Engpass, nicht der Feature-Vergleich.** Nachweisbare
lokale Referenzen aus dem eigenen Gewerk wirken stärker als jedes
Produktargument. Das beeinflusst die Akquisestrategie mehr als das Produkt.

---

## 2. Musterbildung nach Methodik-Regel 4 (≥5 unabhängige Fundstellen)

### 2.1 Bestätigte Muster: **keine**

Es konnte keine Rezensionsseite geöffnet und daher keine Fundstelle gezählt
werden. Aggregatbehauptungen Dritter über ungesehene Fundstellen als „Muster"
zu deklarieren, würde die Bewertungsmatrix mit Scheinpräzision infizieren.

### 2.2 Sechs Musterverdachte (belegt, aber unter Schwelle)

| # | Musterverdacht | Belege | Produktchance | Reife |
|---|---|---|---|---|
| **MV-1** | **Abrechnungsüberraschung ist die Nr.-1-Beschwerde.** Zusatzgebühren je Anruf, Minutenabrechnung, unangekündigte Preiserhöhungen (Goodcall 59→99→130 $ ohne Ankündigung; Smith.ai Add-on-Stapelung; Ruby „frequent price increases") | 6 Belege, 3 Anbieter, 4 Plattformtypen | **Radikale Preisgarantie als Kernversprechen.** Festpreis, alles inklusive, schriftliche Garantie 24 Monate, Kündigung in einem Klick. Verkaufsargument ist die Rechnung, nicht die KI. | mittel |
| **MV-2** | Kündigung wird erschwert, Belastung läuft weiter | 3 Belege, 2 Anbieter | Kündigung als Feature. § 312k BGB (Kündigungsbutton) gilt für Verbraucher, bei B2B nicht zwingend — aber als Vertrauenssignal einsetzbar. | niedrig |
| **MV-3** | **Einrichtung dauert deutlich länger als beworben.** „Learning curve" ist der meistgenannte Contra-Punkt: **59 Nennungen bei Synthflow, 46 bei Retell** auf G2 = 105 aggregierte Nennungen. Produktionsreifer Einsatz: 8–20 Stunden statt „minutes". | **einziger Verdacht mit harten Zahlen** | **„Done-for-you"-Einrichtung als bezahlte Setup-Leistung** statt Self-Service. Der Kunde kauft das fertig eingerichtete Ergebnis, nicht ein Werkzeug. Deckt Kriterium 18. | **hoch** |
| **MV-4** | Support nicht erreichbar oder nur über Community-Discord | 4 Belege | Benannter Ansprechpartner, garantierte Reaktionszeit als Vertragsbestandteil. **Nordstern-Konflikt:** genau die Leistung, die Nico dauerhaft nicht erbringen will — nur zulässig, wenn ab Tag 1 als bezahlte Rolle geplant. | mittel |
| **MV-5** | **Die KI bricht außerhalb des Skripts zusammen**, Eskalation fehlt oder ist unsauber | 7 Belege | Hybridmodell mit sauberer Eskalation. Zugleich der teuerste Teil (Personalkosten) → wirkt direkt gegen das 65-%-Margenziel. | mittel |
| **MV-6** | **Es gibt praktisch keinen unabhängigen Review-Korpus** in dieser Kategorie | Strukturbeobachtung über alle Suchen | Vertrauen ist der Engpass. Lokale Referenzen im selben Gewerk schlagen Features. | **hoch** |

### 2.3 Einzelmeinungen (ausdrücklich getrennt geführt)

- **Bewertungsdivergenz Retell: G2 4,8/5 vs. Trustpilot 3,1/5** [F]. Analytisch
  das interessanteste Signal, weil es nicht auf Meinung beruht, sondern auf
  strukturellem Unterschied: G2 sammelt überwiegend kurz nach Kauf, Trustpilot
  nach dem Problem. 1,7 Punkte Spanne = **Zufriedenheit beim Kauf, Enttäuschung
  im Betrieb**. Aber: ein Anbieter, eine Beobachtung → **Hypothese über Churn,
  kein Nachweis von Churn.**
- Rosie: kein Outbound, kein menschlicher Fallback (Produktlücke eines Anbieters)
- Retell: Latenz teils 4–5 Sekunden statt 800 ms; häufige Breaking Changes an der API
- PR-dokumentierter Einzelfall 03/2026: KI-Agent behauptete, ein Mensch zu sein,
  unterbrach, sprach die Kundin mit falschem Geschlecht an — **PR-Meldung eines
  interessierten Absenders** (menschlicher Antwortdienst), entsprechend zu gewichten
- „78 % bevorzugen Menschen" — Quelle ist der Blog eines KI-Empfangsanbieters
  ohne Erhebungsmethode. **Nicht verwendbar.**

---

## 3. Gegensignale: wo Kunden zufrieden sind

Auftragsgemäß gesucht, weil gelöste Probleme schlechte Marktlücken sind.

- Smith.ai: **4,7/5 auf G2** [F]; 332 Trustpilot-Bewertungen mit vielen 5-Sterne-Wertungen von Kleinunternehmen
- Retell AI: **4,8/5 auf G2** [F]
- Quellenübergreifend am häufigsten gelobt: **24/7-Verfügbarkeit zu einem Preis,
  den ein Kleinbetrieb für Personal nie zahlen könnte**
- Rosie: Flatrate ohne Minutenzuschläge (49/149/299 $) wird ausdrücklich positiv
  hervorgehoben — erkennbar als Gegenposition zu den Abrechnungsbeschwerden

---

## 4. Die strategische Kernaussage

> **Die Zufriedenheit liegt fast vollständig auf der technischen Ebene.
> Die Unzufriedenheit fast vollständig auf der kommerziell-operativen Ebene.**

Zufrieden: „Anruf wird angenommen, 24/7, billiger als Personal."
Unzufrieden: Abrechnung, Preiserhöhungen, Kündigung, Support, Einrichtungsaufwand,
Verhalten außerhalb des Skripts.

**Daraus folgen zwei unbequeme Konsequenzen:**

1. **Ein Modell, das über „bessere KI" gewinnen will, greift den bereits
   gelösten Teil des Marktes an.** Es ist nach Kriterium 24 („Wettbewerber über
   bessere Gesamtleistung schlagen") schwach positioniert.
2. **Ein Modell, das über faire Abrechnung, echten Support, garantierte
   Einrichtung und sauberes Kündigungsverhalten gewinnt, greift den ungelösten
   Teil an** — aber das ist ein **Service- und Prozessvorsprung, kein
   Technologievorsprung**. Er ist kopierbar und baut kein IP auf, was direkt
   gegen Kriterium 8 (verkaufbarer Unternehmenswert) und die Kategorie
   „Wettbewerbsvorteil" wirkt.

Die daraus folgende Red-Team-Frage lautet: *Was hindert Smith.ai oder Goodcall
daran, morgen eine Preisgarantie einzuführen und den einzigen Vorteil zu
neutralisieren?*

---

## 5. Branchenkontext KI-Agenten – mit Zirkelschluss-Warnung

| Befund | Stufe |
|---|---|
| Umfrage 03/2026 unter 650 Enterprise-Technologieverantwortlichen: 78 % betreiben mindestens einen KI-Agenten-Piloten, aber nur **14 %** haben organisationsweit skaliert | [S] – Primärstudie nicht verifiziert |
| „88 % der KI-Agenten-Piloten erreichen nie die Produktion" | **[A]** – Quelle ist ein Anbieterblog |
| Gartner 2026: 57 % gescheiterter KI-Initiativen durch unrealistische Erwartungen, 38 % durch Datenqualität | [S] – Zuschreibung über Drittseite |
| Fünf dominante Fehlermodi im Voice-Produktionsbetrieb: Speech Hallucination, Persona Drift, Akzent-/Dialektbias, Sicherheitsbedrohungen, Eskalationsversagen | [P] |

**Zirkelschluss-Warnung:** Diese Zahlen betreffen *Enterprise*-KI-Agenten, nicht
KMU-Telefonassistenten. Ein 5-Mitarbeiter-Sanitärbetrieb hat weder
Governance-Reibung noch Mehrsystem-Integration — die beiden Hauptursachen
entfallen dort teilweise. Nicht ungeprüft übertragen.

---

## 6. Was aus diesem Dokument NICHT abgeleitet werden darf

- Keine Aussage über den **deutschen** Markt. Null Datenpunkte aus dem
  deutschsprachigen Raum. In den USA sind „answering services" eine seit
  Jahrzehnten etablierte Kategorie mit hoher Zahlungsbereitschaft — in
  Deutschland ist selbst die Kategorieakzeptanz ungeklärt.
- Keine hochgerechneten Häufigkeiten („Beschwerde X bei drei Anbietern, also
  60 % des Marktes").
- Keine Verwendung der Marketingzahlen 27 % / 1.200 $ / 85 %.

---

## 7. Die bessere Alternative zur Sekundärrecherche

Für den deutschen Markt liefert Sekundärresearch ohnehin dünne Daten. Die
belastbarere Option kostet ~0 € und zwei Wochen:

1. **Erreichbarkeitstest:** 50 Betriebe der Zielgruppe außerhalb der Kernzeit
   anrufen und messen, wie viele erreichbar sind. Ersetzt die unbrauchbare
   27-%-Marketingzahl durch eine eigene **[F]**-Zahl für exakt den Zielmarkt.
2. **20 Inhaberinterviews** zu Problem, bestehender Lösung und Kosten.
3. **Zahlungsbereitschaftstest** mit konkretem Preisangebot.

Das beantwortet Leitfrage 8 direkt, passt zu Nicos Stärkenprofil (Telefonieren,
Verkaufen, Zuhören) und nutzt seinen vorhandenen Stack. **Diese Erhebung ist in
den 100-Tage-Plan aufgenommen (siehe `17_100_tage_plan.md`).**
