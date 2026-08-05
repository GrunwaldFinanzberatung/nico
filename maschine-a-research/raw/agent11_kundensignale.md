# Agent 11 – Kundensignal- und Review-Analyst

Stand: 2026-08-05 · Status: **UNVOLLSTÄNDIG – Auftrag konnte nicht erfüllt werden**
Zuordnung: Welle 1, `raw/agent11_kundensignale.md`

---

## 0. ZUERST LESEN: Methodischer Abbruch und Beleglage

### 0.1 Was passiert ist

Der Auftrag verlangte **mindestens 40 wörtliche Kundenzitate** aus mindestens
30 WebSearch-Anfragen plus WebFetch auf Reddit, G2, Capterra, Trustpilot,
ProvenExpert und deutschen Foren. **Beides war in dieser Session technisch
nicht möglich.** Belegte Ursachen:

| Werkzeug | Status | Beleg |
|---|---|---|
| **WebFetch** | vollständig blockiert | HTTP 403 auf *jeden* Host, inkl. `en.wikipedia.org` und `news.ycombinator.com`. Kein Site-Bot-Schutz, sondern die Egress-Policy der Session. |
| **Bash/curl** | vollständig blockiert | `CONNECT tunnel failed, response 403`. Proxy-Statusendpunkt protokolliert `connect_rejected … policy denial` für `reddit.com`, `trustpilot.com`, `omr.com`, `handwerk.com`, `wer-weiss-was.de`, `provenexpert.com`, `ebuero.de`. |
| **Reddit (alle Wege)** | zusätzlich hart blockiert | WebFetch meldet gesondert „Claude Code is unable to fetch from www.reddit.com". `WebSearch` mit `allowed_domains:["reddit.com"]` liefert API-Fehler 400: Domain für den User-Agent nicht zugänglich. Auch Spiegel-Instanzen (redlib, safereddit) → 403. |
| **WebSearch** | nach 8 Anfragen erschöpft | Session-Budget 200/200 aufgebraucht (geteiltes Budget über alle 12 Agenten; bei meinem Start waren bereits ~192 verbraucht). |

**Konsequenz:** Ich habe **8 von 30+ geplanten Suchanfragen** durchgebracht und
**null direkte Seitenabrufe**. Alles Folgende stammt aus den Trefferlisten und
Synthesen dieser 8 Suchanfragen.

### 0.2 Warum hier fast keine echten Zitate stehen

Der Auftrag ist an dieser Stelle eindeutig:

> „Falls du ein Zitat nicht wörtlich belegen kannst, schreibe es NICHT als
> Zitat, sondern als paraphrasierte Beobachtung mit Quellenangabe."

Da ich **keine einzige Reviewseite direkt öffnen konnte**, habe ich für keine
Aussage die Originalformulierung gesehen. Was ich habe, ist die Zusammenfassung
eines Suchwerkzeugs über Seiten, die ich nicht gelesen habe. Ich schreibe daher
**keine 40 Zitate**, sondern führe konsequent drei Belegstufen:

| Kennung | Bedeutung |
|---|---|
| **[Z?]** | Wortfragment, das das Suchwerkzeug ausdrücklich in Anführungszeichen gesetzt hat. Wahrscheinlich Originalwortlaut, **aber nicht am Original verifiziert.** Nicht als verifiziertes Zitat verwendbar. |
| **[P]** | Paraphrase aus der Suchsynthese. Kein Zitat. |
| **[F]/[S]/[A]** | Zahlenkennung nach `02_research_methodik.md` §2.2. |

Zusätzlich bewerte ich jede Quelle nach Unabhängigkeit (siehe 0.3), weil das
im Ergebnis die wichtigste Erkenntnis dieses Agentenlaufs ist.

### 0.3 Wichtigste methodische Erkenntnis: Der Review-Korpus ist vergiftet

Das ist **kein Nebenbefund, sondern ein verwertbares Marktsignal.**

In allen 8 Suchanfragen zu KI-Telefonassistenten dominierten die Trefferlisten
nicht Kundenstimmen, sondern **„Review"-Artikel von direkten Wettbewerbern**:

| „Review"-Seite | Betreibt tatsächlich | Bewertet in den Treffern |
|---|---|---|
| `synthflow.ai/blog/goodcall-review` | Synthflow (Konkurrent) | Goodcall |
| `retellai.com/blog/synhtflow-ai-review` | Retell (Konkurrent) | Synthflow |
| `thoughtly.com/blog/retell-ai-review` | Thoughtly (Konkurrent) | Retell |
| `serviceagent.ai/blogs/…` | ServiceAgent (Konkurrent) | Smith.ai, Goodcall, Rosie |
| `dialora.ai/blog/…` | Dialora (Konkurrent) | Smith.ai, Synthflow, Goodcall |
| `myaifrontdesk.com/blogs/…` | My AI Front Desk (Konkurrent) | Rosie |
| `ainora.lt`, `oncrew.ai`, `vertexhub.app`, `botphonic.ai`, `squawkvoice.ai`, `open.cx`, `eesel.ai`, `contractortoolstack.com` | Anbieter bzw. Affiliate-Funnels | jeweils fremde Produkte |

Dazu kam bei HVAC-/Plumbing-Suchen eine Trefferliste, die **fast vollständig
aus GoHighLevel-Landingpages** bestand (`app.gohighlevel.com/v2/preview/…`) –
also aus White-Label-Funnels von Agenturen, nicht aus Kundenstimmen.

**Ableitungen für Maschine A:**

1. **Kaufentscheidung ist für den Kunden nicht rational treffbar.** Ein
   Handwerksmeister, der „KI Telefonassistent Erfahrungen" googelt, findet
   ausschließlich Verkäufer, die sich gegenseitig schlechtschreiben. Das
   erklärt, warum in dieser Kategorie **Vertrauen, nicht Feature-Vergleich,
   der Engpass ist** – und warum Referenzen aus der eigenen Region/Gewerk
   wahrscheinlich stärker wirken als jedes Produktargument.
2. **Warnung an den Orchestrator und an Agent 03:** Preis- und Feature-Angaben
   zu Voice-AI-Produkten, die aus diesen Quellen stammen, sind
   **wettbewerbsgefärbt**. Sie gehören nach `02_research_methodik.md` §2.3
   zwingend gegen die **öffentlichen Preisseiten der Anbieter selbst**
   geprüft, bevor sie in die Bewertungsmatrix einfließen.
3. **Marketingzahlen aus Anbieter-Landingpages sind hier unbrauchbar.**
   Konkret die in den Trefferlisten wiederholt auftauchenden Angaben
   „27 % der Anrufe unbeantwortet", „1.200 $ Verlust je verpasstem Anruf",
   „85 % hinterlassen keine Mailbox-Nachricht" stammen ausschließlich aus
   GoHighLevel-Verkaufsseiten ohne Primärquelle. **[A] – nicht als Fakt
   verwenden.** Wenn Maschine A auf dieser These aufbaut, muss die Zahl aus
   einer Primärstudie kommen (Vorschlag: eigene Messung mit Testanrufen bei
   50 Betrieben – siehe 6.2).

---

## 1. Was tatsächlich belegt gefunden wurde

Geordnet nach Beweiskraft, nicht nach Auftragsstruktur. Jede Zeile mit Quelle.
**Keine dieser Fundstellen erreicht allein die Musterschwelle von 5 unabhängigen
Belegen aus `02_research_methodik.md` §2.4.**

### 1.1 Abrechnung, Preissprünge und Kündigungsprobleme (Bereich A)

| # | Befund | Stufe | Quelle |
|---|---|---|---|
| A1 | Kundin/Kunde kündigte Goodcall im Okt. 2025; Karte wurde trotz mehrfacher schriftlicher Aufforderung monatelang weiterbelastet, bis die Karte im Feb. 2026 gesperrt und ersetzt wurde; keine Rückerstattung. | [P] | Trustpilot-Rezension, wiedergegeben über Suche → `trustpilot.com/review/goodcall.com` (Vorgang datiert 10/2025–02/2026) |
| A2 | Stand Mai 2026 versuche Goodcall weiterhin, Karten von seit Monaten gekündigten Konten zu belasten. | [P] | ebd. |
| A3 | Preis stieg ohne Ankündigung von 59 $ auf 99 $ auf 130 $/Monat; Anfragen zum Abrechnungsstreit blieben unbeantwortet. | [P] | ebd. |
| A4 | 1-Stern-Rezension: Anruf beim Kundenservice beginne sofort mit Upselling, kein Dialog, nur Verkaufsdruck; am Ende werde man an eine andere Nummer verwiesen und der Vorgang beginne von vorn. | [P], Teilfragmente [Z?] | ebd. |
| A5 | Bei Smith.ai treten drei Beschwerdemuster **unabhängig auf vier Plattformen** auf – Trustpilot, G2, Clutch, BBB: (a) Rechnungsüberraschungen durch gestapelte Zusatzgebühren, (b) Weiterleitung an menschliche Agenten **ohne Freigabe des Kunden**, (c) Weiterbelastung nach Kündigung. | [P] | Sekundärauswertung `serviceagent.ai/blogs/smith-ai-pricing/` – **Achtung: Wettbewerber-Quelle**, nur als Hypothese verwendbar |
| A6 | Rechnungsüberraschungen seien die häufigste Beschwerde über Smith.ai auf Trustpilot. | [P] | ebd. |
| A7 | Ruby: wiederkehrende Beschwerden sind hoher Preis, **häufige Preiserhöhungen** [Z?: „frequent price increases"] und Minutenabrechnungs-Überraschungen. | [P] + [Z?] | ConsumerAffairs, wiedergegeben über Suche → `consumeraffairs.com/business/ruby-receptionists.html` |
| A8 | Ruby rechnet **pro Minute statt pro Anruf** ab; ein 5-Minuten-Anruf kostet das Fünffache eines 1-Minuten-Anrufs, Monatsrechnungen schwanken entsprechend stark. Überminutenpreise werden auf der Preisseite nicht veröffentlicht. | [P]; Preis 4,75–5,90 $/Zusatzminute **[S]** (Schätzung von Fit Small Business, nicht Ruby) | `fitsmallbusiness.com/ruby-receptionist-review/` |
| A9 | Fit Small Business vergibt für Rubys Preisgestaltung **1,75 von 5** und nennt sie [Z?] „well above industry average". | [F] Score 1,75/5 (Bewertung des Portals, nicht Messwert) | ebd. |
| A10 | Smith.ai-Zusatzgebühren je Anruf: Terminbuchung +1,50 $, Aufzeichnung +0,25 $, SMS-/Slack-Benachrichtigung +0,50 $, Spanisch +1,00 $, Zahlungsabwicklung +1,00 $, Live-Weiterleitung +3,00 $/Transfer; Hybridtarif 292,50–585 $/Monat. | **[S]** – Wettbewerber-Quelle, **muss gegen smith.ai/pricing geprüft werden** | `serviceagent.ai/blogs/smith-ai-pricing/` |

**Bewertung:** Das ist die belegstärkste Gruppe. A1–A4 betreffen **einen**
Anbieter, A5–A6 einen zweiten, A7–A9 einen dritten. Damit liegen Hinweise aus
**drei Anbietern und mindestens vier Plattformtypen** vor – das reicht für
einen begründeten Musterverdacht, aber **nicht** für ein bestätigtes Muster
nach §2.4, weil ich die Einzelrezensionen nicht zählen konnte.

### 1.2 Produktqualität und Scheitern im Betrieb (Bereich A, Churn-relevant)

| # | Befund | Stufe | Quelle |
|---|---|---|---|
| B1 | Goodcall: Der Dienst habe wenig Wert geliefert und nicht die erwarteten Ergebnisse gebracht; Unfähigkeit, komplexe, nicht-lineare Gespräche zu führen, führe zu [Z?] „broken promises" in Nutzerforen; Leistung breche ein, sobald das Gespräch vom Skript abweiche. | [P] + [Z?] | Suchsynthese über mehrere Goodcall-Review-Seiten – **überwiegend Wettbewerber-Quellen** |
| B2 | Rosie: **kein Outbound-Calling, kein menschlicher Fallback**, Wissen begrenzt auf das, was von der eigenen Website gezogen werden kann. Strukturelle Grenze für Betriebe, die Angebote nachfassen oder Termine am Vortag bestätigen wollen. | [P] | Suchsynthese, u. a. `serviceagent.ai/blogs/rosie-ai-pricing/`, `prospeo.io` |
| B3 | Rosie: [Z?] „there's almost no independent review data to lean on" – es gibt praktisch keine unabhängigen Bewertungsdaten. | [Z?] | ebd. – deckt sich mit Befund 0.3 |
| B4 | Retell AI: Support werde häufig als [Z?] „non-existent" beschrieben; primärer Supportkanal sei ein Community-Discord, was für dringende Geschäftsvorfälle ungeeignet sei. Weitere Nennungen: fehlender visueller Builder, **häufige Breaking Changes an der API**. | [P] + [Z?] | G2-Auswertung, wiedergegeben über Suche → `g2.com/products/retell-ai/reviews?qs=pros-and-cons` |
| B5 | Retell AI: Latenz schwanke – teils 800–1000 ms, teils **4–5 Sekunden**. | [P], Zahlen [F] laut G2-Rezension | ebd. |
| B6 | Retell AI: Top-Beschwerden mit Nennungszahlen – begrenzte Stimmauswahl für internationale Nutzung **67 Nennungen**, steile Lernkurve **46 Nennungen**, Preiskomplexität/Kosten für kleine Teams **41 Nennungen**. | **[F]** (G2-Aggregat) | ebd. |
| B7 | **Bewertungs-Divergenz Retell: G2 4,8/5 – Trustpilot 3,1/5.** | **[F]** | `g2.com/products/retell-ai/reviews`, `trustpilot.com/review/retellai.com` |
| B8 | Synthflow: [Z?] „learning curve" wird in **59 G2-Rezensionen** als Contra genannt. | **[F]** | `g2.com/products/synthflow/reviews?qs=pros-and-cons` |
| B9 | Synthflow: Tutorials bilden die aktuelle Oberfläche nicht ab; das Einrichten einer Custom Action mit cal.com sei schwierig gewesen. | [P] | ebd. |
| B10 | Synthflow: Produktionsreifer Einsatz koste **8–20 Stunden** für eine technikaffine Person – nicht die beworbenen [Z?] „minutes". | **[S]** (Einschätzung der auswertenden Seite) | Suchsynthese; **Wettbewerber-Quelle (Retell-Blog) beteiligt** |
| B11 | Synthflow: Latenzspitzen und Schwierigkeiten mit Barge-in (Unterbrechen des Bots) bei mehrdeutigen Anfragen. | [P] | ebd. |
| B12 | Dokumentierter Praxisfall (März 2026): Ein KI-Agent im Kundenservice **behauptete, ein Mensch zu sein**, unterbrach, wiederholte sich, konnte dem Gespräch nicht folgen und sprach die Kundin mit falschem Geschlecht an. | [P] | PR-Newswire-Meldung, März 2026 → `prnewswire.com/news-releases/ai-customer-service-fail-real-call-reveals-why-businesses-should-keep-humans-on-the-line-302703890.html` – **PR-Meldung eines interessierten Absenders (menschlicher Antwortdienst), entsprechend zu gewichten** |

**Bewertung Churn:** B1, B4, B5, B7, B10, B12 sind die härtesten
Scheiter-Indizien, die diese Session hergibt. Die Divergenz **G2 4,8 vs.
Trustpilot 3,1 (B7)** ist das analytisch wertvollste Einzelsignal, weil es
nicht auf Meinung, sondern auf strukturellem Unterschied beruht: G2-Bewertungen
werden überwiegend über Anreizkampagnen kurz nach Kauf eingesammelt,
Trustpilot-Bewertungen entstehen typischerweise **nach** dem Problem. Eine
Spanne von 1,7 Punkten ist ein starkes Indiz für **Zufriedenheit beim Kauf,
Enttäuschung im Betrieb** – also genau das Churn-Profil, nach dem der Auftrag
fragt. Das ist eine **Hypothese mit einem Beleg**, kein Muster.

### 1.3 Branchenweite Scheiterquoten KI-Agenten (Bereich A, Kontext)

| # | Befund | Stufe | Quelle |
|---|---|---|---|
| C1 | Umfrage März 2026 unter **650 Enterprise-Technologieverantwortlichen**: 78 % betreiben mindestens einen KI-Agenten-Piloten, aber nur **14 %** haben einen Agenten organisationsweit skaliert. | **[F]** wenn Primärstudie auffindbar – hier nur über `zenvanriel.com` referiert, **Primärquelle nicht verifiziert → aktuell [S]** | `zenvanriel.com/ai-engineer-blog/ai-agent-scaling-gap-pilot-production-2026/` |
| C2 | „88 % der KI-Agenten-Piloten erreichen nie die Produktion." | **[A]** – Quelle ist ein Anbieterblog (Haptik), keine Primärstudie | `haptik.ai/blog/why-ai-agents-dont-reach-production-…` |
| C3 | Gartner 2026: **57 %** gescheiterter KI-Initiativen gehen auf unrealistische Erwartungen zurück, **38 %** auf schlechte Datenqualität. | **[S]** – Gartner-Zuschreibung über Drittseite, Originalstudie nicht geprüft | Suchsynthese |
| C4 | Fünf Fehlermodi dominieren den Produktionsbetrieb von Voice AI: **Speech Hallucination, Persona Drift, Akzent-/Dialekt-Erkennungsbias, Sicherheitsbedrohungen, Eskalationsversagen.** | [P] | `agxntsix.ai/blog/voice-ai-pilot-to-production-failure-modes` |
| C5 | Voice AI hat eine **größere Demo-zu-Produktion-Lücke als Text-KI** – Ursachen: Hintergrundgeräusche, Akzente, Latenzanforderungen, tiefe Mehrsystem-Integration. | [P] | ebd. + `autointerviewai.com` |

**Achtung – Zirkelschluss-Warnung:** C1–C3 sind Zahlen über
*Enterprise*-KI-Agenten allgemein, **nicht** über KMU-Telefonassistenten. Sie
dürfen nicht ungeprüft auf das Handwerker-Segment übertragen werden. Ein
5-Mitarbeiter-Sanitärbetrieb hat weder Governance-Reibung noch
Mehrsystem-Integration – die beiden Hauptursachen in C4/C5 entfallen dort
teilweise. Die Übertragbarkeit gehört von **Agent 12 (Red Team)** geprüft.

### 1.4 Gegensignale – wo Kunden zufrieden sind

Auftragsgemäß gesucht, weil gelöste Probleme schlechte Marktlücken sind.

| # | Befund | Stufe | Quelle |
|---|---|---|---|
| D1 | Smith.ai: **4,7/5 auf G2**; auf Trustpilot 332 Bewertungen mit mehreren 5-Sterne-Wertungen von Kleinunternehmen. | **[F]** | `g2.com/products/smith-ai-ai-receptionist/pricing`, `ie.trustpilot.com/review/smith.ai` |
| D2 | Retell AI: **4,8/5 auf G2** (Angaben zur Anzahl schwanken quellenabhängig zwischen 781, 1.755 und 2.200 Rezensionen – **Inkonsistenz, ungeklärt**). | [F] Score, [A] Anzahl | `g2.com/products/retell-ai/reviews` |
| D3 | Wiederkehrend positiv genannt: **24/7-Verfügbarkeit zu einem Preis, den ein Kleinbetrieb für Personal nie zahlen könnte** – das ist quellenübergreifend der am häufigsten gelobte Punkt. | [P] | mehrere Trefferlisten |
| D4 | Rosie: **Flatrate-Preise ohne Minutenzuschläge** (49 $ / 149 $ / 299 $ pro Monat) werden ausdrücklich positiv hervorgehoben – erkennbar als Gegenposition zu den Abrechnungsbeschwerden aus 1.1. | [F] Preise laut mehreren Quellen; **gegen rosie-Preisseite zu prüfen** | `prospeo.io/s/rosie-pricing-reviews-pros-and-cons` |
| D5 | Retell: Berichte über minimale Bugs und geringe Latenz stärken das Vertrauen in die technische Basis. | [P] | Suchsynthese |

**Interpretation – das ist die wichtigste strategische Lesart dieses Laufs:**

Die Zufriedenheit liegt fast vollständig auf der **Funktionsebene**
(„Anruf wird angenommen, 24/7, billiger als Personal") – die Unzufriedenheit
fast vollständig auf der **Betreiberebene** (Abrechnung, Preiserhöhungen,
Kündigung, Support, Einrichtungsaufwand, Verhalten außerhalb des Skripts).

Daraus folgt eine unbequeme, aber entscheidungsrelevante Aussage:

> **Die Technologie ist nicht die Lücke. Die Lücke ist Betreiberdisziplin.**

Für Maschine A heißt das: Ein Modell, das über *bessere KI* gewinnen will,
greift den zufriedenen Teil des Marktes an (D1–D5) und ist nach
`01_nordstern…` §7 Kriterium 24 („Wettbewerber über bessere Gesamtleistung
schlagbar") schwach positioniert. Ein Modell, das über **faire, vorhersehbare
Abrechnung, echten Support, garantierte Einrichtung und sauberes
Kündigungsverhalten** gewinnt, greift den unzufriedenen Teil an. Das ist
allerdings ein **Service- und Prozessvorsprung, kein Technologievorsprung** –
mit den entsprechenden Folgen für Kriterium 8 (Verkaufbarkeit) und Kategorie
„Wettbewerbsvorteil", weil er kopierbar ist.

### 1.5 Kundenpräferenz Mensch vs. KI

| # | Befund | Stufe | Quelle |
|---|---|---|---|
| E1 | 78 % der Befragten würden ein Unternehmen mit menschlicher Empfangskraft einem mit KI vorziehen; 70 % sagen, Menschen zeigten Empathie. | **[A] – unbrauchbar als Fakt.** Quelle ist der Blog eines KI-Empfangsanbieters (thanksava.com), Primärerhebung nicht benannt. | `thanksava.com/post/how-ai-receptionists-handle-angry-difficult-callers` |
| E2 | Wiederkehrende Kritik an KI im Kundenservice: versteht die Absicht nicht, gibt falsche oder themenfremde Antworten, bricht außerhalb des Skripts zusammen, kann keine Empathie zeigen. | [P] | Suchsynthese, mehrere Anbieterblogs |
| E3 | Eine kleine Zahl von Anrufern ist irritiert, wenn sie merkt, dass eine KI den Anruf bearbeitet. | [P] | Suchsynthese |

E1 ist bewusst als unbrauchbar markiert: Die Zahl stammt von einer Partei mit
Interesse an genau diesem Ergebnis und wird ohne Erhebungsmethode genannt.

---

## 2. Musterbildung nach §2.4 – ehrliche Auswertung

Regel: **≥ 5 unabhängige Fundstellen = Muster. Weniger = Einzelmeinung.**

### 2.1 Bestätigte Muster

**Keine.**

Ich kann kein einziges Muster regelkonform ausweisen. Grund: Ich konnte keine
Rezensionsseite öffnen und daher keine Fundstellen zählen. Was ich habe, sind
Aggregatbehauptungen Dritter über Fundstellen, die ich nicht gesehen habe. Das
als „Muster" zu deklarieren wäre ein Verstoß gegen §2.2 und §2.4 und würde die
gesamte Bewertungsmatrix mit Scheinpräzision infizieren.

### 2.2 Musterverdachte (belegt, aber unter Schwelle)

Diese sechs Verdachte sind stark genug, um sie weiterzuverfolgen, und schwach
genug, dass **keine Bewertungsentscheidung** auf ihnen ruhen darf.

| # | Musterverdacht | Belegstellen | Unabh. Quellenarten | Abgeleitete Produktchance | Reife |
|---|---|---|---|---|---|
| **MV-1** | **Abrechnungsüberraschung ist die Nr.-1-Beschwerde bei Telefon-Diensten.** Zusatzgebühren pro Anruf, Minutenabrechnung, unangekündigte Preiserhöhungen. | A3, A5, A6, A7, A8, A10 (6 Belege, 3 Anbieter) | Trustpilot, ConsumerAffairs, Fit Small Business, (Sekundär: G2/BBB/Clutch) | **Radikale Preisgarantie als Kernversprechen:** Festpreis je Betrieb, alle Funktionen inklusive, schriftliche Preisgarantie 24 Monate, Kündigung online in einem Klick. Verkaufsargument ist nicht die KI, sondern die Rechnung. | mittel |
| **MV-2** | **Kündigung wird aktiv erschwert; Belastung läuft weiter.** | A1, A2, A5 (3 Belege, 2 Anbieter) | Trustpilot, (Sekundär: BBB) | Kündigung als Feature vermarkten. In DE ohnehin Pflicht (**Kündigungsbutton nach § 312k BGB seit 01.07.2022** – gilt für Verbraucher; bei B2B nicht zwingend, aber als Vertrauenssignal einsetzbar). Zu prüfen von Agent 08. | niedrig |
| **MV-3** | **Einrichtung dauert deutlich länger als beworben; Lernkurve ist der meistgenannte Contra-Punkt.** | B6 (46 G2-Nennungen), B8 (59 G2-Nennungen), B9, B10, B11 | G2 (2 Produkte, 105 aggregierte Nennungen), Anbieterauswertungen | **„Done-for-you"-Einrichtung als bezahlte Setup-Leistung**, nicht als Self-Service. Deckt sich exakt mit Kriterium 18 („Setup-Gebühr + Monatsvertrag"). Der Kunde kauft **das fertig eingerichtete Ergebnis**, nicht ein Werkzeug. Das ist der einzige Musterverdacht mit belastbaren Nennungszahlen. | **hoch** |
| **MV-4** | **Support ist nicht erreichbar oder nur über Community-Kanäle.** | B4, A4, A3, (B6 indirekt) | G2, Trustpilot | Benannter Ansprechpartner, garantierte Reaktionszeit als Vertragsbestandteil. **Achtung Nordstern-Konflikt:** Dies ist genau die Leistung, die Nico laut `01_nordstern…` §3 dauerhaft nicht erbringen will („täglicher Kundensupport, 24/7-Erreichbarkeit"). Nur zulässig, wenn ab Tag 1 als bezahlte Rolle geplant. → Agent 06. | mittel |
| **MV-5** | **Die KI bricht außerhalb des Skripts zusammen; Eskalation an Menschen fehlt oder ist unsauber.** | B1, B2, B5, B11, B12, C4, E2 (7 Belege) | G2, PR-Meldung, Fachanalysen, Anbieterauswertungen | **Hybridmodell mit sauberer Eskalation** als Produktkern: KI übernimmt das Standardaufkommen, ein definierter menschlicher Pfad übernimmt alles andere – transparent, ohne den Anrufer zu täuschen. Zugleich der teuerste Teil des Modells (Personalkosten) → wirkt direkt auf Kriterium „Bruttomarge ≥ 65 %". | mittel |
| **MV-6** | **Es gibt praktisch keine unabhängigen Bewertungsdaten in dieser Kategorie.** | 0.3 (13 Wettbewerber-„Review"-Seiten), B3 | Strukturbeobachtung über alle 8 Suchen | Vertrauen ist der Engpass, nicht Funktion. **Nachweisbare lokale Referenzen im selben Gewerk** schlagen jedes Feature-Argument. Beeinflusst die Akquisestrategie stärker als das Produkt. | **hoch** |

### 2.3 Einzelmeinungen (ausdrücklich getrennt)

Nach §2.4 als Einzelmeinung geführt, **nicht** in Musterbildung eingerechnet:

- **B7** – Bewertungsdivergenz G2 4,8 vs. Trustpilot 3,1 bei Retell. Analytisch
  das interessanteste Signal, aber **ein einziger Anbieter, eine Beobachtung.**
  Es ist eine Hypothese über Churn, kein Nachweis von Churn.
- **B2** – fehlendes Outbound bei Rosie. Produktlücke eines Anbieters.
- **B12** – der PR-dokumentierte Einzelfall. Ein Anruf, von einer interessierten
  Partei veröffentlicht.
- **E1** – „78 % bevorzugen Menschen". Eine Zahl, interessierte Quelle,
  keine Methode. Nicht verwendbar.
- **D4** – Rosies Flatrate-Preismodell als positive Ausnahme.

---

## 3. Was der Auftrag verlangte und was fehlt

Vollständigkeitsbilanz, damit der Orchestrator die Lücke exakt kennt:

| Auftragsteil | Status | Fehlt |
|---|---|---|
| **A) KI-Telefonassistenten / Voice AI** | teilweise, ~35 % | Reddit vollständig (r/smallbusiness, r/HVAC, r/Plumbing, r/msp, r/Entrepreneur, r/SaaS); Capterra, TrustRadius, BBB im Original; Smith.ai-, Ruby-, AnswerConnect-Rezensionen im Volltext |
| **B) Handwerker-/KMU-Software** | **0 %** | **Komplett offen.** Keine einzige Suche zu ToolTime, Craftnote, plancraft, ServiceTitan, Jobber, Housecall Pro durchgekommen |
| **C) Deutsche KMU-Schmerzpunkte** | **0 %** | **Komplett offen.** Keine einzige deutschsprachige Quelle erreicht. Alle Befunde oben sind aus dem **US-Markt** – WebSearch ist laut Werkzeugbeschreibung „US-only". |
| **D) Managed Services / Wartungsverträge** | **0 %** | **Komplett offen.** |
| **≥ 40 wörtliche Zitate** | **0 verifizierte Zitate** | Alle 40. Verfügbar: 8 unverifizierte Wortfragmente [Z?]. |
| **Muster ab 5 Nennungen** | 0 bestätigt, 6 Verdachte | Zählbare Fundstellen |
| **Churn-/Scheiter-Belege** | schwach | Echte Kündigungsberichte von Betreibern; Retention-/Churn-Zahlen von Anbietern |
| **Gegensignale** | teilweise | reicht für erste Interpretation (1.4) |

### 3.1 Besonders schwerwiegend: Der deutsche Markt fehlt vollständig

Maschine A zielt laut `02_research_methodik.md` §4/A7 auf eine
**deutschsprachige Zielgruppe**. Dieser Agentenlauf enthält **null Datenpunkte
aus dem deutschsprachigen Raum**. Alle Preise, Beschwerden und
Zufriedenheitsmuster oben stammen aus dem US-Markt, wo Antwortdienste
(„answering services") eine seit Jahrzehnten etablierte, verbreitete Kategorie
mit hoher Zahlungsbereitschaft sind.

**Diese Übertragung ist nicht zulässig.** Konkret ungeklärt bleibt:

1. Ist die Kategorie „Telefonservice" im deutschen Handwerk überhaupt bekannt
   und akzeptiert? (US: ja, seit Jahrzehnten. DE: unklar.)
2. Wie hoch ist die deutsche Zahlungsbereitschaft wirklich? Leitfrage 8 aus
   §3 der Methodik ist damit für diesen Bereich **unbeantwortet**.
3. Blockiert DSGVO/TKG die Aufzeichnung und KI-Verarbeitung von
   Telefongesprächen in einer Weise, die das US-Modell hier teurer macht?
   → zwingend an **Agent 08** (Risiko/Regulierung).
4. Deutsche Wettbewerber (ebuero, eGain-artige Dienste, Sekretariatsservices)
   wurden gar nicht erfasst. Der Versuch, `ebuero.de` abzurufen, ist als
   erster Proxy-Fehler protokolliert.

Bis das geklärt ist, darf **kein Voice-AI-Modell** allein auf Basis dieses
Dokuments in der Bewertungsmatrix Punkte für „Reale, nachweisbare Nachfrage"
(Kriterium 10) oder „Klare Zahlungsbereitschaft" (Kriterium 11) erhalten.

---

## 4. Vorläufige Antwort auf Leitfrage 6 der Methodik

> „Woran scheitern bestehende Anbieter aus Kundensicht messbar (Churn, Reviews,
> Beschwerden)?"

**Soweit belegt, und ausdrücklich nur für den US-Markt:**

Bestehende Anbieter scheitern **nicht an der Sprachtechnologie**, sondern an
vier kommerziellen und operativen Punkten:

1. **Rechnung** – unvorhersehbar, Zusatzgebühren, unangekündigte Erhöhungen (MV-1)
2. **Vertragsaustritt** – erschwert, Weiterbelastung nach Kündigung (MV-2)
3. **Inbetriebnahme** – Wochen statt Minuten, Lernkurve als meistgenannter
   Contra-Punkt (MV-3, mit 105 aggregierten G2-Nennungen der belegstärkste Punkt)
4. **Support und Eskalation** – nicht erreichbar; KI bricht außerhalb des
   Skripts zusammen, ohne sauberen Übergang zum Menschen (MV-4, MV-5)

Die Sprachqualität selbst wird überwiegend **positiv** bewertet (D1, D2, D5).

**Strategische Konsequenz, die der Orchestrator kennen muss:** Wenn die vier
Schwachpunkte kommerziell-operativ und nicht technisch sind, dann ist der
Vorsprung eines besseren Anbieters **operativ und damit kopierbar**. Das drückt
die ungewichtete Kategorie „Wettbewerbsvorteil" und Kriterium 8
(„Verkaufbarer Unternehmenswert"), weil kein technisches IP entsteht. Genau
diese Frage gehört an **Agent 12 (Red Team)** – Formulierung des Angriffs:
*„Was hindert Smith.ai oder Goodcall daran, morgen eine Preisgarantie
einzuführen und Maschine As einzigen Vorteil zu neutralisieren?"*

Gegenläufig zu bedenken: Nicos bestehende Twilio-/CallSuite-Assets
(`01_nordstern…` §4) beschleunigen zwar den Start, liefern aber nach §2.8 der
Methodik **keinen** Bonus auf Fit oder Delegierbarkeit – und, nach dem Befund
dieses Agenten, auch keinen Wettbewerbsvorteil, weil die Telefonietechnik nicht
der Engpass ist.

---

## 5. Was NICHT in diesem Dokument steht (und warum)

Zur Absicherung gegen spätere Fehlnutzung:

- **Keine erfundenen Zitate.** Es wäre trivial gewesen, 40 plausibel klingende
  Handwerkerzitate zu schreiben. Sie hätten sich durch das gesamte Projekt bis
  in die Endempfehlung fortgepflanzt und wären nicht mehr rückverfolgbar
  gewesen. Nach §2.2 sind unbelegte Angaben ungültig.
- **Keine hochgerechneten Häufigkeiten.** „Beschwerde X taucht bei drei
  Anbietern auf, also betrifft sie 60 % des Marktes" – nicht zulässig.
- **Keine Übertragung US → DE.** Siehe 3.1.
- **Keine Verwendung der GoHighLevel-Marketingzahlen** (27 % / 1.200 $ / 85 %)
  als Fakten. Siehe 0.3.

---

## 6. Wiederaufnahme – konkreter Plan

### 6.1 Voraussetzung

Mindestens eine der beiden Sperren muss aufgehoben werden:

- **Suchbudget:** `CLAUDE_CODE_MAX_WEB_SEARCHES_PER_SESSION` erhöhen
  (Bedarf: **~45 Anfragen** allein für Agent 11), **oder** Agent 11 in einer
  eigenen Session mit frischem Budget starten.
- **Egress-Policy:** Freigabe für `reddit.com`, `trustpilot.com`, `g2.com`,
  `capterra.com`, `omr.com`, `provenexpert.com`, `handwerk.com`,
  `wer-weiss-was.de`, `ebuero.de`. Ohne diese Freigabe bleiben wörtliche Zitate
  **prinzipiell unmöglich** – dann muss der Auftrag von „40 Zitaten" auf
  „belegte Beobachtungen" umformuliert werden.

**Empfehlung:** Agent 11 in eigener Session neu starten und **vor allen anderen
Agenten** laufen lassen, da er das Suchbudget am stärksten benötigt.

### 6.2 Alternative ohne Websperren – und die inhaltlich bessere Option

Falls die Sperren bestehen bleiben, liefert Sekundärresearch für den deutschen
Markt ohnehin schwache Daten. Die belastbarere Alternative:

**Primärerhebung, 2 Wochen, Kosten ~0 €:**

1. **Erreichbarkeitstest:** 50 Handwerksbetriebe in der Region
   Oldenburg/Nordwest (A3) außerhalb der Kernzeit anrufen. Messen: Wie viele
   nehmen ab, wie viele Mailbox, wie viele klingeln ins Leere, wie viele rufen
   binnen 24 h zurück. Das ersetzt die unbrauchbare 27-%-Marketingzahl durch
   eine **eigene, belastbare [F]-Zahl für genau den Zielmarkt**.
2. **20 Kurzinterviews** mit Inhabern zu: Wer nimmt heute ab? Was kostet das?
   Was passiert mit Anfragen nach 17 Uhr?
3. **Zahlungsbereitschaftstest:** konkretes Angebot an 20 Betriebe, Reaktion messen.

Das beantwortet Leitfrage 8 („belegt, nicht erhofft") direkt – und liefert
Nachweise, die kein Wettbewerber hat. Es passt zudem zu Nicos Stärkenprofil
(§3: Verkaufen, Präsentieren, Überzeugen) und ist genau die Arbeit, die in
`01_nordstern…` §5 Kriterium 27 als zulässig arbeitsintensive Aufbauphase
vorgesehen ist.

### 6.3 Vorbereitete Suchanfragen für den Neustart

Nach Priorität. Bereich C und D zuerst, weil dort 0 % Abdeckung besteht **und**
weil dort der Zielmarkt liegt.

**Priorität 1 – Deutschland (Bereich C), 12 Anfragen:**
1. Handwerksbetrieb Telefon klingelt ständig Störung Büroarbeit Erfahrungen
2. Handwerker keine Zeit Angebote schreiben Nachfassen verlorene Aufträge
3. Handwerk Anfragen verlieren telefonisch nicht erreichbar Studie ZDH
4. Fachkräftemangel Handwerk Büro Verwaltung Bürokratie Belastung Umfrage
5. Telefonservice Handwerk Erfahrungen Sekretariatsservice Kosten
6. ebuero Erfahrungen Kritik Bewertung
7. Handwerk Digitalisierung Skepsis Software Erfahrungen Forum
8. Handwerkerforum Büroorganisation Telefon Chaos
9. KI Telefonassistent Handwerk Erfahrungen Deutschland
10. Handwerksbetrieb Notdienst Telefon Wochenende Belastung
11. wer-weiss-was Handwerker Anrufe Kunden erreichen
12. ZDH Konjunkturumfrage Bürokratiebelastung Stunden pro Woche

**Priorität 2 – Handwerkersoftware (Bereich B), 10 Anfragen:**
13. ToolTime Erfahrungen Kritik Handwerker
14. Craftnote Kritik Erfahrungen Bewertung
15. plancraft Bewertung Erfahrungen Nachteile
16. Handwerkersoftware Erfahrungen Forum zu teuer kompliziert
17. Handwerkersoftware Einrichtung Datenübernahme Probleme
18. ServiceTitan complaints expensive contract lock-in
19. Jobber pricing complaints reviews cons
20. Housecall Pro review problems complaints cancel
21. field service software "too many tools" integration complaint
22. Handwerkssoftware Wechsel Erfahrungen gekündigt

**Priorität 3 – Wartungsverträge (Bereich D), 6 Anfragen:**
23. Wartungsvertrag Ärger Kunden Beschwerden Leistung nicht erbracht
24. Wartungsvertrag Heizung Kunden unzufrieden kündigen
25. managed services contract clients "not getting value" renewal
26. MSP clients complain monthly fee what am I paying for
27. Wartungsvertrag automatische Verlängerung Ärger
28. Servicevertrag Reaktionszeit nicht eingehalten Beschwerde

**Priorität 4 – Voice AI Churn vertiefen (Bereich A), 10 Anfragen:**
29. "we cancelled" AI receptionist "back to" answering service
30. AI receptionist booked wrong appointment customer complaint
31. AI phone agent customers hang up when they realize it's AI
32. Smith.ai BBB complaints billing after cancellation
33. AnswerConnect complaints reviews cancel
34. AI receptionist "setup took" weeks complicated onboarding
35. voice AI agency churn rate clients leaving after 3 months
36. AI receptionist trial cancelled did not book any jobs
37. Trustpilot retellai.com 1 star reviews
38. AI answering service accent dialect could not understand complaint

**Priorität 5 – Gegensignale (7 Anfragen):**
39. AI receptionist "paid for itself" ROI happy contractor review
40. Jobber reviews customers love simple easy
41. answering service customers stayed for years satisfied
42. what AI receptionists do well 2026 verified reviews
43. Handwerkersoftware Erfahrungen positiv zufrieden empfehlen
44. virtual receptionist retention rate customers stay
45. AI receptionist small business "best decision" review

---

## 7. Übergabe an den Orchestrator – die vier Sätze, die zählen

1. **Dieses Dokument enthält keine bestätigten Muster und keine verifizierten
   Zitate.** Es darf keine Bewertungspunkte in der Matrix begründen.
2. **Sechs Musterverdachte** stehen bereit (MV-1 bis MV-6); die belegstärksten
   sind **MV-3 (Einrichtungsaufwand, 105 aggregierte G2-Nennungen)** und
   **MV-6 (kein unabhängiger Review-Korpus, damit Vertrauen als Engpass)**.
3. **Der einzige inhaltlich harte Befund lautet:** Die Beschwerden liegen auf
   der kommerziell-operativen Ebene (Abrechnung, Kündigung, Setup, Support),
   die Zufriedenheit auf der technischen Ebene. Ein Angriff über „bessere KI"
   zielt auf den gelösten Teil des Marktes. Ein Angriff über Betreiberdisziplin
   zielt auf den ungelösten Teil – ist aber kopierbar und baut kein IP auf.
   → Zwingend an **Agent 12** zur Gegenprüfung.
4. **Der deutsche Markt ist in diesem Lauf zu 0 % erfasst.** Solange das so
   ist, bleibt Kriterium 10 („Reale, nachweisbare Nachfrage") und Kriterium 11
   („Klare Zahlungsbereitschaft") für alle Voice-AI-Modelle **unbelegt** – und
   die Freedom-Inbound-Neutralität aus §2.11 der Methodik ist damit sogar
   *strenger* anzuwenden als bisher: Die Arbeitshypothese hat nach diesem Lauf
   **weniger** Belegunterstützung, nicht mehr.

---

## Quellenverzeichnis (alle in diesem Dokument referenzierten URLs)

Alle über WebSearch-Trefferlisten identifiziert. **Keine wurde direkt
abgerufen** – Abrufversuche scheiterten mit HTTP 403 (siehe 0.1).

**Bewertungsplattformen (unabhängig, höchste Priorität für Nachprüfung):**
- https://www.trustpilot.com/review/goodcall.com
- https://ie.trustpilot.com/review/smith.ai · https://uk.trustpilot.com/review/goodcall.com
- https://www.trustpilot.com/review/retellai.com
- https://www.g2.com/products/retell-ai/reviews?qs=pros-and-cons
- https://www.g2.com/products/synthflow/reviews?qs=pros-and-cons
- https://www.g2.com/products/smith-ai-ai-receptionist/pricing
- https://www.capterra.com/p/186839/Ruby-Receptionists-Virtual-Receptionist-and-Chat-Services/reviews/
- https://www.consumeraffairs.com/business/ruby-receptionists.html

**Fachportale (unabhängig, mittlere Priorität):**
- https://fitsmallbusiness.com/ruby-receptionist-review/
- https://slashdot.org/software/p/Rosie-AI/

**Analysen / Studien (Primärquellen nicht verifiziert):**
- https://agxntsix.ai/blog/voice-ai-pilot-to-production-failure-modes
- https://zenvanriel.com/ai-engineer-blog/ai-agent-scaling-gap-pilot-production-2026/
- https://www.haptik.ai/blog/why-ai-agents-dont-reach-production-and-how-voice-ai-breaks-the-pattern
- https://www.autointerviewai.com/blog/ai-voice-agent-demo-production-gap-failure-modes-2026
- https://www.digitalapplied.com/blog/customer-service-ai-agent-statistics-2026-data
- https://www.prnewswire.com/news-releases/ai-customer-service-fail-real-call-reveals-why-businesses-should-keep-humans-on-the-line-302703890.html (PR eines interessierten Absenders)

**Wettbewerber-„Reviews" – NUR als Hypothesenquelle, nie als Beleg:**
- https://serviceagent.ai/blogs/smith-ai-pricing/ · /blogs/goodcall-review/ · /blogs/rosie-ai-pricing/ · /blogs/goodcall-pricing/
- https://synthflow.ai/blog/goodcall-review · https://www.retellai.com/blog/synhtflow-ai-review
- https://thoughtly.com/blog/retell-ai-review · https://www.dialora.ai/blog/synthflow-ai-reviews · /blog/smith-ai-reviews · /blog/goodcall-reviews
- https://www.myaifrontdesk.com/blogs/rosie-ai-answering-service-reviews-…
- https://ainora.lt/blog/goodcall-ai-review-alternatives-2026 · /blog/rosie-ai-review-alternatives-2026
- https://oncrew.ai/blog/ruby-receptionist-alternatives-2026 · https://vertexhub.app/blog/ruby-receptionist-alternative.html
- https://thanksava.com/post/how-ai-receptionists-handle-angry-difficult-callers
- https://prospeo.io/s/rosie-pricing-reviews-pros-and-cons · /s/smithai-pricing-reviews-pros-and-cons
- https://www.eesel.ai/blog/retell-ai-reviews · https://www.cloudtalk.io/blog/retell-ai-review/ · https://zeeg.me/en/blog/post/synthflow-ai
- https://contractortoolstack.com/software/smith-ai/ · /software/synthflow/
