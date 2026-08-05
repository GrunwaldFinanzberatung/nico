# Agent 12 — Gegenanwalt / Red Team

Stand: 2026-08-05 · Auftrag: Angriff auf S01, S02, S03, S04, S05, S13
· Ziel: nicht Ideen entwerten, sondern falsche Euphorie verhindern

---

## 0. Methodik und Selbstbeschränkung

**Suchbudget:** 11 WebSearch-Anfragen (eine ohne Ertrag — englischsprachige
Wikipedia-Treffer statt deutscher Anbieter). WebFetch weiterhin 403, **keine
einzige Anbieter-Preisseite direkt geöffnet**. Das gilt für Welle 1 und für mich.
Meine Gegenbelege sind Suchsynthesen, also **[F-sek]**, nicht primärverifiziert.

**Wichtiger Befund vorab, methodisch:** Ich habe pro Modell im Schnitt *eine*
Suche gebraucht, um den zentralen Negativbefund der Shortlist zu erschüttern.
In vier von sechs Fällen ist das gelungen. Das ist das eigentliche Alarmsignal
dieses Berichts — nicht ein einzelnes Modell, sondern die **Trefferquote der
Gegenrecherche**. Wenn eine einzelne Suche reicht, um „das bietet niemand an"
zu kippen, liegt der Fehler in der Methode, nicht im Ergebnis.

**Was ich ausdrücklich NICHT angreife**, weil es der stärkste Teil des Projekts ist:
- **Befund 1 (Preispunkt-Arithmetik).** Der ist richtig, quantitativ sauber und
  unbequem. Er verurteilt allerdings mehr Shortlist-Modelle, als die Shortlist
  zugibt — dazu Angriff 5.
- **Die Ableitung der Orchestrator-Nachrecherche §5**, dass die Kundenzahl-
  Arithmetik sich nur durch **Zielgruppenwechsel zum Betreiber mit
  Anlagenbestand und Haftungsrisiko** löst. Das ist der beste Satz im gesamten
  Korpus. Er wird in der Shortlist zitiert, aber nicht konsequent angewandt:
  S02, S03 und S05 verkaufen weiterhin an den **ausführenden Betrieb**.

---

## 1. Angriffsprotokoll je Modell

Urteilsskala: **überlebt** (Kernthese hält, Details korrigieren) ·
**angeschlagen** (Kernthese hält nur unter zusätzlichen Bedingungen, Bewertung
muss runter) · **widerlegt** (Kernthese hält in der vorliegenden Form nicht).

---

### S01 — Betreiberpflichten-Manager · Urteil: **ANGESCHLAGEN**

**1. Versteckte operative Belastung.**
Das Produkt *ist* Fristenverwaltung und Einzelfallbearbeitung. Nicos Anti-Liste,
Positionen 1 und 2, lauten wörtlich: „Unterlagen prüfen, Dokumente sortieren"
und „Fristen und Einzelfälle verwalten". Die Shortlist behandelt das als
Softwareproblem. Es ist keins.

Ein schlechter Dienstag in Monat 20 bei 60 Standorten: Die Elektrofachkraft des
Partners in Ostwestfalen fällt aus, drei Standorte müssen umgeplant werden, aber
zwei davon haben Schichtbetrieb und lassen Prüfungen nur im Werksurlaub zu. Ein
Kunde hat Freitag ein Kundenaudit und in der Akte fehlen vier Nachweise, weil ein
Partner seine Berichte als abfotografierte PDFs mit falschen Anlagennummern
geschickt hat. Ein anderer Partner hat drei Positionen doppelt fakturiert, der
Kunde hat es gemerkt und fragt, wofür er die Koordinationsgebühr zahlt. Parallel
meldet ein Prüfbericht 14 Mängel — jemand muss entscheiden, ob das
Instandsetzungsangebot beauftragt wird, und das ist keine Softwarefrage, sondern
ein Telefonat mit einem Werkleiter, der kein Budget hat.

Das ist **Disposition und Reklamationsbearbeitung**. Disposition skaliert mit
Köpfen, nicht mit Code.

**2. Margenrealität — hier steckt ein Rechenfehler.**
Die Shortlist nennt „5.000–30.000 €/Standort/Jahr" Erlös **und** „Koordinations-
marge 70–85 %". Beides zusammen geht nicht. Die 5.000–30.000 € sind das
geschätzte **Prüfvolumen** des Standorts, also überwiegend durchgereichte
Partnerleistung. Darauf sind 70–85 % Marge unmöglich; realistisch sind
15–30 % Aufschlag auf Fremdleistung.

Zwei saubere Alternativen, die die Shortlist nicht trennt:
- **Modell A (Durchleitung):** Umsatz 5.000–30.000 €/Standort/Jahr,
  Bruttomarge **20–35 %**. Verletzt Kriterium 2 (≥ 65 %) und nähert sich K.-o. 5.
- **Modell B (reine Koordinationsgebühr):** Umsatz 500–1.500 €/Monat/Standort,
  Bruttomarge vor Personal 70–80 %, **aber** nach den 8–20 Koordinationsstunden
  je Standort und Jahr (Schätzung [A], à 45 € Vollkosten = 360–900 €/Jahr)
  landet man bei **50–65 %**. Und der Umsatz je Kunde ist ein Zehntel der
  genannten Zahl.

Zusätzlich unbepreist: die **Katasteraufnahme**. Ein Kataster über 15–18 Gewerke
entsteht nicht am Schreibtisch, sondern durch eine Begehung von 1–3 Tagen je
Standort mit Anfahrt. Bei 130+ Standorten ist das ein eigener Kostenblock, der in
keinem der drei Dokumente vorkommt.

**3. Warum Kunden wirklich kündigen.** Nicht wegen Unzufriedenheit — wegen
Preistransparenz. Jeder Partner rechnet dem Kunden irgendwann direkt vor, was
die Prüfung „eigentlich" kostet. Sobald der Kunde die Marge sieht und das Kataster
einmal existiert (er hat es ja bezahlt), ist der Rückweg zur Direktbeauftragung
billig. Weitere Treiber: neuer technischer Leiter bringt seine Anbieter mit;
Konzernmutter zentralisiert auf Apleona/Wisag; ein einziger gerissener Termin.

**4. Abhängigkeit von Nico.** Hoch und länger als 24 Monate. Verkauft wird
Haftungsberuhigung an einen Geschäftsführer. Das ist Vertrauensverkauf und exakt
Nicos Stärke — deshalb klebt es an ihm. Ein angestellter Verkäufer ohne 20
belastbare Referenzen verkauft das nicht. Realistisch delegierbar ab Jahr 3–4,
nicht ab Monat 24.

**5. Erstverkauf — schwerer als dargestellt.** Entscheider ist nicht einer,
sondern vier: Geschäftsführung (unterschreibt), technischer Leiter (verliert
Kontrolle), Fachkraft für Arbeitssicherheit (das ist *ihr* Job — der strukturelle
Blocker), Einkauf (will drei Angebote und kündigt bestehende Rahmenverträge
nicht gern). Realistischer Zyklus: 4–9 Monate bis zum Pilotstandort, danach
6–12 Monate bis zum Rollout. **Erste Rechnung frühestens Monat 6.**

**6. Zahlungsbereitschaft: erhofft, nicht belegt.** Belegt ist, dass Standorte
Prüfleistung einkaufen. Unbelegt ist, dass jemand für die **Koordinationsschicht
separat** zahlt. Die Nachrecherche listet das selbst als offenen Punkt
(Preise Maqsima, Prüfpilot, mybuilding24 „nicht ermittelt"). Gegenanker: CAFM-
Software kostet ein paar hundert Euro im Monat, FM startet bei 1,50 €/m². Der
Preiskorridor 300–1.000 €/Monat ist plausibel, 2.500 € sind es nicht.

**7. Kopierbarkeit — der Negativbefund ist schwächer geworden.**
Meine Suche zeigt eine Schicht, die in der Friedhofsprüfung (§6 der Nachrecherche)
komplett fehlt: **bundesweite Prüfservice-Firmen mit Multi-Gewerke-Portfolio**.
KFK Torservice & Safety Prüfservice und KFK Konrad bieten Brandschutztore,
Brandschutztüren, Feststellanlagen, Elektroprüfung nach DGUV V3/V4, Maschinen-
und Anlagenprüfung sowie Leitern und Tritte — bundesweit, ISO 9001, seit über
30 Jahren, mit „ein Ansprechpartner"-Versprechen [F-sek]. Ebenso SI Prüfservice
und AB Prüfservice.

Die Friedhofsprüfung hat nur nach oben geschaut (TÜV, DEKRA, IFM-Konzerne) und
dort korrekt festgestellt: Software, Schulung, Großkunden. Sie hat **nicht nach
unten geschaut**. Dort sitzt der eigentliche Wettbewerber — und der hat bereits
Kunden, Prüfer, Fahrzeuge und Zertifizierung. Für ihn ist Nicos Modell die
Erweiterung des Gewerkeportfolios über Subunternehmer plus ein Portal. Das ist
ein 12-Monats-Projekt für ihn und ein 36-Monats-Projekt für Nico.

**Ehrliche Neubewertung des Negativbefunds:** von „plausibel, mittelstark belegt"
auf **„die Lücke ist enger als beschrieben und wird von unten angegriffen"**.

**8. Technologische Überholung.** Mittel — LLM-Agenten verbilligen Katasteraufnahme
und Fristenlogik. Für alle gleichermaßen. Kein Vorteil, eher Erosion des
Differenzierers.

**9. Regulierung.** K.-o. 3 ist korrekt nicht verletzt, solange nicht selbst
geprüft wird. Aber: Sobald der Personalengpass „Prüfung darf nur eine
Elektrofachkraft durchführen" zur eigenen Einstellung führt, kippt das. Weiter:
Gefährdungsbeurteilungen berühren BetrVG-Mitbestimmung, Nachweise enthalten
personenbezogene Daten.

**10. Personalintensität.** Hoch und früh: Koordinatoren, nicht Entwickler. Bei
130 Standorten schätze ich 8–15 Koordinatoren plus 4–6 Vertriebler [A]. Das ist
ein Dienstleistungsbetrieb mit Softwarelack, kein Softwaregeschäft.

---

### S02 — Terminierungs-Abo für Prüf- und Wartungsdienstleister · Urteil: **WIDERLEGT in der vorliegenden Form**

Ausführlich in Angriff 1. Hier die Punkte 1–10 kompakt.

**1. Operative Belastung.** Der Kunde liefert eine Excel mit 400 Zeilen: halb
veraltete Rufnummern, gewechselte Ansprechpartner, Fälligkeiten aus dem
Gedächtnis. Datenmigration ist je Kunde ein Projekt, nicht ein Import.
Tourenlogik braucht Technikerskills, Fahrzeugbeladung, Ersatzteilverfügbarkeit —
die stecken im ERP des Kunden. Schlechter Dienstag: Der Voice-Provider hat
Latenzprobleme, 60 Anrufe misslingen, ein Endkunde beschwert sich beim
Prüfdienstleister über den „Roboteranruf", dessen Inhaber ruft Nico persönlich an,
und gleichzeitig hat die KI acht Termine in ein Zeitfenster gelegt, das die
Disposition nicht halten kann.

**2. Margenrealität.** Bei 0,10–0,12 €/Min Voice-Vollkosten [S, aus S14] und
realistisch 2–4 Wählversuchen bei 30–40 % Privatkunden-Erreichbarkeit fallen je
**bestätigtem** Termin 6–12 Gesprächs- und Wählminuten an → 0,60–1,50 € reine
Telefoniekosten. Hinzu kommt die Fallback-Quote: 20–30 % der Angerufenen wollen
nicht mit einer KI sprechen [A] — diese Fälle laufen über einen Menschen, à 3–6 €.
Mischkalkulation: **1,50–3,00 € Kosten je Termin**. Bei 10–15 € Preis sind das
70–80 % Bruttomarge — aber erst nach dem Onboarding, das im ersten Jahr das
Ergebnis auffrisst.

**3. Kündigung.** Der Killer ist nicht Unzufriedenheit, sondern Bündelung: Der
Kunde erneuert sein ERP und die Funktion ist inklusive. Zweitens die Bürokraft,
deren Aufgabe wegautomatisiert wird und die im Betrieb bleibt — sie verteidigt
ihren Job und findet Fehler. Drittens Endkunden-Beschwerden: der Prüfdienstleister
riskiert seine Kundenbeziehung, Nico riskiert nur einen Vertrag. Asymmetrisches
Risiko zulasten des Kunden = hoher Churn.

**4. Nico-Abhängigkeit.** Anfangs baut und tunt er die Gesprächsleitfäden je
Kunde. Wenn jeder Kunde sein eigenes Skript, seine eigene Fälligkeitslogik und
seine eigene ERP-Schnittstelle braucht, streift das **K.-o. 4** (jeder Kunde eine
Sonderanfertigung).

**5. Erstverkauf — der beste unter den sechs.** Ein Entscheider (Inhaber),
Zyklus 4–10 Wochen. Blocker: Disponentin, Datenschutzbedenken, „meine Kunden
wollen keinen Roboter". Das ist real machbar. Es ist die einzige Stärke dieses
Modells, die die Prüfung überlebt.

**6. Zahlungsbereitschaft — falscher Anker in der Shortlist.**
Belegt sind **300 €+ je qualifiziertem B2B-Termin** und Retainer von
2.500–7.000 €/Monat im DACH-Raum [F-sek, dievertriebswikinger.de,
callcenterdirect.de]. Das ist **Kaltakquise-Neukundenterminierung** und ein
völlig anderes Gut. Ein Bestandskunden-Wartungstermin mit 200–600 € Auftragswert
[F, Nachrecherche] trägt bei etwa 50 % Deckungsbeitrag 100–300 € DB. Davon zahlt
niemand 300 €. Realistisch 5–20 € je Termin.

**Damit bricht die Arithmetik:** Prüfdienstleister mit 400 Bestandskunden =
400 Termine/Jahr × 15 € = 6.000 €/Jahr = **500 €/Monat ARPU**. Selbst mit
Plattformgebühr 250 €/Monat landet man bei 700–900 €. Für 190.000 €/Monat
braucht es **210–380 Kunden**. Das ist exakt das Szenario, das **Befund 1 der
eigenen Shortlist** als nicht finanzierbar ausschließt: Inside-Sales-Organisation
mit 10–20 Köpfen. S02 verstößt gegen die Filterregel des Projekts und ist trotzdem
auf Platz 2 gelandet.

**7./8. Kopierbarkeit und Überholung.** Siehe Angriff 1 — bereits geschehen.

**9. Regulierung — schärfer als notiert.** Die Shortlist nennt UWG § 7. Zwei
Ebenen, die fehlen:
- Ein Anruf zur Terminierung einer **vertraglich geschuldeten** Wartung ist
  Vertragsabwicklung, wahrscheinlich zulässig. Ein Anruf zur Terminierung einer
  **nicht** geschuldeten Prüfung ist Werbung → § 7 Abs. 2 Nr. 1 UWG, Einwilligung
  erforderlich, Bußgeldrahmen bis 300.000 €. Die Grenze verläuft mitten durch das
  Produkt und ist im Massenbetrieb schwer sauber zu halten.
- **KI-Transparenzpflicht.** Der Angerufene muss erfahren, dass er mit einer KI
  spricht. Eine Ansage „Sie sprechen mit einem KI-Assistenten" senkt die
  Abschlussquote messbar [A] — und niemand hat diese Quote gemessen. Sie ist die
  ökonomisch wichtigste unbekannte Zahl des Modells.

**10. Personalintensität.** Mittel, aber onboarding-lastig und damit im
Wachstum unangenehm: jeder Neukunde bindet Wochen.

---

### S03 — Sensor-Monitoring als Motor für Wartungs-Mitgliedschaften · Urteil: **WIDERLEGT in der vorliegenden Form**

**Der zentrale Gegenbeleg:** Die Hersteller sind bereits da, und zwar mit genau
diesem Angebot. **Vaillant aroTHERM COMFORT: Fernüberwachung ab 47 €/Monat mit
proaktiver Störungserkennung. Viessmann Vitocal mit ViCare und Predictive
Maintenance. Bosch/Buderus Compress Connected Comfort** [F-sek]. Dazu
Partnerprogramme, die dem SHK-Betrieb Fernüberwachung, 24/7-Monitoring und
KI-Steuerung als Teil des Herstellerpakets liefern (AF Wärme, Tecalor
Digitalisierungspartnerschaft) [F-sek]. Und digimax verkauft dem SHK-Handwerk
bereits eine „Wartungs-Plattform" samt Monteur-App und BEG/BAFA-Logik [F-sek].

Die Shortlist nennt genau diese Prüfung als „Offene Flanke (P1, sehr hoch)". Sie
ist jetzt geprüft. **Ergebnis: negativ für das Modell.** Der SHK-Betrieb bekommt
Monitoring vom Hersteller praktisch geschenkt, weil es für den Hersteller ein
Bindungsinstrument ist, kein Produkt. Gegen „geschenkt" verkauft man kein
500-€-Abo.

**Die verbleibende Nische** ist der **Mischbestand ohne Herstellerkonnektivität** —
also alte Gaskessel. Genau dieser Bestand wird durch GEG und Förderung gerade
ersetzt. Das Modell adressiert einen **schrumpfenden Bestand mit ablaufendem
Zeitfenster**.

**Weitere Punkte:**
- **Operativ:** Hardware bleibt Hardware, auch zugekauft: Lager, Seriennummern,
  RMA, Firmware, SIM-Verträge, Funklöcher im Heizungskeller. Schlechter Dienstag:
  LTE-Störung, 800 Sensoren offline, 40 Betriebe rufen an, keiner glaubt „liegt
  am Netz".
- **Marge/Kapital:** 80–250 € Hardware je Anlage plus 1–3 €/Monat Konnektivität,
  amortisiert über 24–36 Monate. Die Shortlist weist dafür **keinen
  Kapitalbedarf** aus. Bei 200 Betrieben × 40 Anlagen = 8.000 Sensoren ×
  150 € = **1,2 Mio. € Vorfinanzierung**. Das ist ein anderes Geschäft als
  beschrieben.
- **Kündigungsgrund, strukturell:** Das Modell setzt voraus, dass der SHK-Betrieb
  ein **Vertriebsprogramm** für Mitgliedschaften fährt. Deutsche SHK-Betriebe
  sind seit Jahren ausgelastet und lehnen Aufträge ab. Sie brauchen keinen
  Mehrumsatz, sie brauchen Monteure. **Befund 4 („das Ausland verkauft Umsatz")
  trifft auf einen Markt, dessen Engpass nicht Nachfrage, sondern Kapazität ist.**
  Das ist der schwerwiegendste konzeptionelle Einwand gegen Befund 4 insgesamt.
- **SmartAC-Transfer:** US-Klimaanlage bei 40 °C = Notfallgut mit hoher
  Zahlungsbereitschaft des Endkunden. Deutsche Gasheizung = robustes Gut mit
  20 Jahren Lebensdauer. Die 70 %→97 %-Retention ist nicht übertragbar.

---

### S04 — Aufschalt- und Leitstellen-Modell · Urteil: **ANGESCHLAGEN, Marge halbiert**

**2. Margenrealität — zweiter handfester Rechenfehler.**
Die 20–60 €/Monat je Aufschaltung sind bestätigt [F-sek, accsicherheitstechnik.de],
zuzüglich 150–600 € einmalig für Einrichtung, Parametrierung und Test. **Aber das
ist der Endkundenpreis.** Die Shortlist rechnet mit „Grenzkosten 2–5 €/Monat je
Objekt" → 75–90 % Marge. Diese Grenzkosten gelten für den **Betreiber der
Leitstelle**. Nico ist bei White-Label der **Wiederverkäufer** und zahlt einen
Einkaufspreis, nicht Grenzkosten. Realistischer EK: 8–20 €/Monat [A, ungeprüft] →
**Bruttomarge 45–60 %**, nicht 75–90 %. Bei 45 % greift **K.-o. 5**.

Das ist die wichtigste einzelne Zahl, die in 30 Tagen mit drei Telefonaten
klärbar ist — und sie entscheidet über das Modell.

**7. Kopierbarkeit: praktisch null Schutz.** Securitas betreut **über 78.000
aktive Aufschaltungen** mit drei VdS-zertifizierten Leitstellen und eigenem
Vertrieb, inklusive Aufzugsnotruf und Personenbefreiung [F-sek]. Die Leitstellen
verkaufen direkt. Jeder Elektro- und Sicherheitsbetrieb vermittelt Aufschaltungen
nebenbei. Nicos Differenzierung wäre — was genau? Wenn die Antwort „Preis" ist,
greift **K.-o. 6**.

**5. Erstverkauf, übersehener Blocker:** Zielkunde ist der Verwalter mit vielen
Objekten. Im WEG-Kontext kann der Verwalter eine **neue dauerhafte Kostenposition
nicht allein beschließen** — es braucht einen Beschluss der Eigentümerversammlung.
Die tagt einmal im Jahr. Damit hat dieses Modell einen **Entscheidungstakt von bis
zu zwölf Monaten** je Kunde. Das steht in keinem der Dokumente. Bei Gewerbe-
verwaltern und Einzeleigentümern gilt es nicht — was die Zielgruppe deutlich
verengt.

**1. Operativ:** Aufschaltung ist Projektgeschäft je Objekt: Übertragungsgerät,
SIM, IP-Weg, Testalarm, Parametrierung, Objektdatenblatt, Interventions- und
Befreiungsliste, Schlüsselverwaltung. Bei 5.000 Objekten ist die Pflege der
Objekt- und Kontaktdaten ein mehrköpfiger Vollzeitjob — und exakt Nicos
Anti-Liste. Schlechter Dienstag: eingeschlossene Person im Aufzug um 23 Uhr, der
Befreiungsdienst kommt nicht, formal haftet der White-Label-Partner, angerufen
wird Nico.

**3./9./10.** Churn tatsächlich niedrig (echte Stärke). § 34a GewO nur bei
eigener Intervention. Personalintensität mittel, aber verwaltungslastig.

**Was S04 rettet, falls es zu retten ist:** nicht die Aufschaltung, sondern die
**Nachweis- und Abrechnungsschicht darüber** (BetrSichV-Dokumentation,
Ereignisprotokoll, Verwalter-Reporting über hunderte Objekte). Dann ist es aber
ein Softwareprodukt mit Entwicklungsaufwand, nicht ein margenstarker
Weiterverkauf ohne Kapitalbedarf.

---

### S05 — Herstellerunabhängiges Anlagen-IoT für freie Servicebetriebe · Urteil: **ANGESCHLAGEN, kein eigenständiger Kandidat**

**7. Der Markt ist besetzt, nur fragmentiert.** Bereits in einer Suche gefunden:
**Tecson** (Tanks, Füllstände, Industrieanlagen über NB-IoT/LTE/LoRaWAN),
**HMS** (IoT-Gateways für Bestandsanlagen ohne Eingriff in vorhandene Steuerung,
plus Partnernetz für Komplettlösungen), **deltaheat** (herstellerunabhängiges
Retrofit-Monitoring Heizungskeller), **Pexon Consulting** (IoT-Retrofit
herstellerunabhängig, ohne Vendor-Lock-in), **wz-it** (Retrofit für
Bestandsanlagen Industrie) [alle F-sek]. Der Befund „der Servicebetrieb mit
gemischtem Bestand bleibt blind" ist nicht falsch, aber die Antwort darauf wird
bereits von mehreren Seiten verkauft — nur ohne dominanten Anbieter.

**Der Beleg für das Modell ist in Wahrheit ein Warnsignal.** „uptime.ac > 200
Unternehmen in Europa" wird als Stärke geführt. Ohne ARPU ist das eine
bedeutungslose Zahl — und 200 Kunden nach mehreren Jahren europaweiter Präsenz
deutet auf einen **langsamen, beratungsintensiven Verkauf**, nicht auf ein
skalierendes Abo.

**1./4. Sonderanfertigungsrisiko.** „Kunde installiert selbst" ist Wunschdenken.
Der erste Sensor an einem Kältesatz von 1998 ist ein Ingenieursprojekt: Modbus,
analoge Fühler, Klemmenpläne, Potentialfreiheit. Jede neue Anlagenfamilie
erfordert eine Adaption → **K.-o.-Kriterium 4 in Reichweite**.

**2. Marge.** Otodatas 67 % ist eine Hardware-Handelsspanne, kein EBITDA. Nach
Konnektivität, Cloud, Support und Adaptionsarbeit bleibt weniger.

**3. Kündigung, identische Struktur wie S03:** Wenn der Servicebetrieb aus den
Daten keine bezahlten Einsätze macht, ist Monitoring ein Kostenposten. Und Daten
in Aufträge zu verwandeln erfordert wieder Vertrieb, den der Betrieb nicht hat.

**Ehrliche Einordnung:** S05 ist S03 mit anderem Anlagentyp und denselben
Schwächen. Die Shortlist führt beide getrennt und erzeugt damit den Eindruck von
zwei unabhängigen Kandidaten. Es ist einer, und er ist schwach.

---

### S13 — Vertikaler Voice-Agent · Urteil: **WIDERLEGT als eigenständiges Geschäft**

Ausführlich in Angriff 4.

Kurz die neuen Belege: **Placetel — eine Telekom-Tochter — schreibt selbst den
Ratgeber „KI Telefonassistent: Die 7 besten Anbieter 2026" und verkauft parallel
einen „KI-Telefonassistent für Handwerker"** [F-sek]. **Superchat listet „die 12
besten Anbieter (2026)" mit Preisen** [F-sek]. Dazu in einer einzigen Suche
sichtbar: voiceOne, Vokaro, Voisa, Agentino, malma.ai, skill-sprinters,
ki-telefonassistent-handwerk.de — plus **plancraft PORTA**.

Ein Markt, in dem Vergleichslisten mit öffentlichen Preisen das dominante
Content-Format sind, ist nach **Befund 3 des Projekts selbst** ein Preiskampfmarkt.
Das Projekt hat die Regel formuliert und wendet sie hier nicht an.

Und: Marktschreiber ist die Telko. Wenn der Anschlussanbieter den Ratgeber
schreibt, in dem er selbst Platz 1 belegt, ist die Kategorie kein Markt mehr,
sondern ein Tarifmerkmal.

---

## 2. Die sechs geforderten Angriffe

### ANGRIFF 1 — Was hindert Certado oder Vemas daran, die Outbound-Terminierung morgen nachzubauen?

**Ehrliche Antwort: nichts. Und im Nachbarsegment ist es bereits passiert.**

Drei Belege, jeder für sich ausreichend:

**a) Certado sitzt nicht nur auf den Fälligkeitsdaten — es benachrichtigt bereits
automatisch.** Certado wirbt damit, dass die Software zeigt, „welcher Kunde wann
fällig ist", dass **Prüffristen automatisch überwacht und Erinnerungen automatisch
versendet werden**, mit getrennten Mandantenbereichen je Kunde und automatischem
Protokollversand [F-sek, certado.io]. Der Terminierungs-Workflow existiert also
schon — als E-Mail statt als Anruf. Der Unterschied zwischen Nicos Produkt und
Certados heutigem Stand ist **ein Kanal**, nicht eine Fähigkeit. Und der Kanal ist
über Retell, Vapi, ElevenLabs oder Twilio ConversationRelay in Wochen eingebaut.

**b) Der Präzedenzfall existiert und ist Monate alt: plancraft PORTA.**
plancraft — die mit 50 Mio. € finanzierte Handwerkersoftware, die die Shortlist
selbst als übermächtigen Gegner in einem *anderen* Segment führt — hat mit
**PORTA einen eigenen KI-Telefonassistenten** gestartet: nimmt Anrufe an, führt
natürliche Gespräche, **erkennt Bestandskunden automatisch**, transkribiert,
nutzbar **eigenständig oder integriert in plancraft**. Auf der Roadmap:
**Terminabstimmung**, E-Mail, WhatsApp [F-sek, plancraft.com, bau.bi]. Das ist
exakt Nicos Modell, gebaut vom Software-Inhaber der Kundenbeziehung, mit
VC-Rückendeckung, in einem Nachbarvertikal.

**c) Die Integration ist kein Burggraben, sie ist ein Feature.** Voisa wirbt
bereits mit „Schnittstellen zu vielen gängigen Handwerkersoftware-Lösungen und
Kalendersystemen" [F-sek]. Und mehrere Anbieter werben bereits mit proaktivem
Outbound: der Assistent ruft 24–48 Stunden vor dem Termin an, erinnert und lässt
verschieben oder absagen [F-sek]. **Der Satz der Shortlist „Prüfpflicht +
KI-Outbound existiert nicht" ist damit nicht mehr haltbar.** Er stimmte
vielleicht für die exakte Kombination „gesetzliche Fälligkeit + Tourenlogik" —
aber das ist eine Feature-Nuance, kein Markt.

**Warum es Certado/Vemas trotzdem vielleicht nicht sofort tun:** Sie sind kleine
deutsche Softwarehäuser mit begrenzter Entwicklungskapazität, ihr Vertrieb ist
langsam, und Telefonie ist ihnen kulturell fremd. Das kauft **12–18 Monate**,
nicht mehr. Es ist ein Zeitvorsprung, kein Burggraben. Und ein Zeitvorsprung
rechtfertigt keinen Platz 2 auf einer Shortlist, deren Zielhorizont 60 Monate ist.

**Konsequenz:** S02 ist als eigenständiges Abo-Geschäft nicht verteidigbar. Es ist
verteidigbar als **Mechanik innerhalb eines Modells, in dem Nico die
Kundenbeziehung besitzt** (S01, S15, oder ein zugekaufter Betrieb nach S16) —
dann ist die Terminierung kein Produkt, das man verkaufen und verteidigen muss,
sondern ein Kostenvorteil, den man nicht offenlegen muss.

---

### ANGRIFF 2 — Ist S01 ein Koordinationsgeschäft oder eine unversicherbare Haftungsfalle? Und warum sollte ein GF 15 funktionierende Verträge kündigen?

**Teil 1: Haftung.**

Die juristische Konstruktion der Shortlist ist korrekt und wichtig: Verkauft wird
**Nachweisfähigkeit**, nicht Haftungsübernahme; die Gesamtverantwortung bleibt
beim Betreiber; die Kontrollpflicht über delegierte Pflichten ist nach den
Suchbefunden **nicht übertragbar** [F-sek, TÜV NORD]. K.-o. 3 ist nicht verletzt.

Das löst aber nur die **öffentlich-rechtliche** Frage. Die gefährliche Ebene ist
die **zivilrechtliche**, und die ist in allen drei Dokumenten unbehandelt:

Nach einem Arbeitsunfall mit fehlendem Prüfnachweis passiert real Folgendes: Die
Berufsgenossenschaft nimmt beim Unternehmer Regress. Die Staatsanwaltschaft prüft
§ 222 StGB gegen die Geschäftsführung. Und die Geschäftsführung sucht denjenigen,
der vertraglich zugesagt hat, dass die Frist überwacht wird. Das ist Nicos GmbH.
Es geht dann nicht darum, ob sie öffentlich-rechtlich verantwortlich war, sondern
ob sie eine **vertragliche Nebenpflicht verletzt** hat. Das ist ein
Vermögensschaden — und wenn ein Personenschaden dranhängt, ein Bereich, den die
**Vermögensschadenhaftpflicht typischerweise gerade nicht deckt** (sie deckt
*echte* Vermögensschäden, nicht Personen- und Sachschadenfolgen) [F-sek]. Die
Betriebshaftpflicht deckt Personenschäden, aber nicht reine
Organisationsverschulden-Ketten.

**Damit entsteht genau in der Mitte eine Deckungslücke** — und diese Lücke ist
das Produkt. Fristversäumnis wird in der Branche zwar als klassischer
VSH-Schadenfall geführt (Notare, Steuerberater) [F-sek], aber „übersehene
Prüffrist mit Personenschadenfolge" ist ein anderes Risikoprofil und wird von
Versicherern erfahrungsgemäß mit Ausschlüssen oder gar nicht gezeichnet.

**Urteil:** Es ist **kein K.-o. nach Kriterium 9** — aber nur, wenn drei
Bedingungen erfüllt sind, die in der Shortlist fehlen:
1. Die Leistungsbeschreibung sagt „wir stellen Kataster, Terminplanung und
   Dokumentation bereit", **nicht** „wir stellen sicher, dass". Das Wort
   „sicherstellen" im Zitat der Nachrecherche (§6.2) ist bereits zu viel.
2. Haftungsbegrenzung auf die Jahresvergütung, AGB-fest formuliert (und das ist
   bei Kardinalpflichten in AGB nach § 307 BGB nicht trivial).
3. Ein schriftlich vorliegendes Versicherungsangebot **vor** dem ersten Vertrag.

Ohne 1–3 ist es tatsächlich eine Haftungsfalle. Mit 1–3 ist es ein Geschäft —
aber ein Geschäft, dessen Nutzenversprechen durch die eigene
Haftungsbegrenzung geschwächt wird, und genau darauf werden Kunden ihre
Einkaufsjuristen ansetzen.

**Teil 2: Warum kündigt ein GF 15 funktionierende Verträge?**

Er tut es nicht. Das ist der stärkste Einwand gegen S01, und er ist stärker als
der Haftungseinwand.

Die 15–18 Verträge sind nicht kaputt. Jeder Einzelne funktioniert; der
Elektroprüfer kommt seit neun Jahren, der Torservice kennt den Hausmeister. Was
nicht funktioniert, ist die **Gesamtsicht** — und die schmerzt exakt zweimal:
beim Audit und nach einem Vorfall. An 363 Tagen im Jahr schmerzt sie nicht.

Ein Wechsel bedeutet für den GF: alle Verträge kündigen (mit Fristen von 3–12
Monaten und teils automatischer Verlängerung), einen Neuling ohne Referenz
zwischen sich und seine Haftung schieben, den internen technischen Leiter und die
FaSi düpieren, und im ersten Jahr mehr Aufwand haben statt weniger. Der
rationale Ertrag: Übersicht. Das ist kein ausreichender Anreiz für einen
Vollwechsel.

**Was tatsächlich verkäuflich ist — und das ist der konstruktive Teil:**
nicht der Vollwechsel, sondern die **Overlay-Variante**. Die bestehenden 15
Verträge bleiben, wo sie sind. Nico verkauft Kataster, Fristenüberwachung,
Nachweiseinsammlung und Auditakte **über** die bestehenden Verträge. Preis
300–800 €/Monat, Entscheidung unterhalb der Einkaufsschwelle, kein Kündigungs-
schmerz, kein interner Feind (die FaSi wird entlastet statt ersetzt). Erst wenn
das läuft, wandern Gewerke einzeln in die Beschaffung über Nicos Partnernetz —
bei jedem Vertragsende eins.

Das ist ein deutlich langsamerer, aber realistischer Pfad. Es bedeutet aber auch:
Der ARPU startet bei 300–800 €, nicht bei 2.500 €, und die margenstarke
Koordinationsschicht kommt erst in Jahr 2–4 je Kunde. **Jede Finanzplanung für
S01, die mit sofortiger Vollbündelung rechnet, ist zu optimistisch.**

---

### ANGRIFF 3 — Kaltstart: Wie viele Monate bis zum ersten Euro?

Das Henne-Ei-Problem ist bei den dreien unterschiedlich schwer. Die Shortlist
behandelt es gar nicht.

**S01 — echtes Zwei-Seiten-Problem, aber lösbar.**
Man braucht Partner in 15–18 Gewerken × Region. Die gute Nachricht: Partner sind
billig zu gewinnen, weil sie **Aufträge ohne Akquise** bekommen — das ist ein
Angebot, das ein Prüfbetrieb annimmt, ohne exklusiv zu werden. Man braucht keine
Verträge, nur Zusagen. Die schlechte: In der Fläche (Kunde hat drei Standorte in
drei Bundesländern) braucht man dasselbe Netz dreimal.
**Realistische Zeitachse:** Monat 0–2 Angebotsdesign und 20 Partnergespräche ·
Monat 2–6 erste Verkaufsgespräche · Monat 4–9 erster bezahlter Pilotstandort
(wahrscheinlich Katasteraufnahme gegen Einmalhonorar) · **erster MRR-Euro Monat
6–10** · erster Standort im Vollbetrieb Monat 9–14.

**S02 — kein Netzwerkproblem, sondern ein Datenproblem.**
Es gibt keine zweite Marktseite. Der Prüfdienstleister bringt seine eigenen
Endkunden mit. Das ist der Grund, warum S02 die schnellste Zeit bis zum ersten
Euro hat.
**Realistische Zeitachse:** Monat 0–1 Voice-Agent auf CallSuite/Twilio aufsetzen ·
Monat 1–2 erster Pilot gegen Erfolgshonorar · **erster Euro Monat 2–3** · erster
echter Abovertrag Monat 4–6. Das ist real und der einzige belastbare
Geschwindigkeitsvorteil im gesamten Projekt.

**S03 — das schwerste Kaltstartproblem, und es wird unterschätzt.**
Drei Seiten statt zwei: Sensorlieferant (Mindestabnahme!), SHK-Betrieb, und
dessen Endkunde, der die Mitgliedschaft kaufen muss. Nico kontrolliert die
dritte Seite nicht einmal indirekt. Bevor der erste Betrieb zahlt, will er einen
Referenzbetrieb sehen, der damit tatsächlich Mitgliedschaften verkauft hat — und
den gibt es in Deutschland nicht.
**Realistische Zeitachse:** Monat 0–3 Hardwareauswahl und Vorfinanzierung ·
Monat 3–6 Pilotbetrieb, wahrscheinlich kostenlos · Monat 6–12 Nachweis, dass der
Pilot Mitgliedschaften verkauft (oder eben nicht) · **erster belastbarer MRR-Euro
Monat 12–18**, mit hoher Wahrscheinlichkeit gar nicht.

**Zusammengefasst:** Der einzige der drei mit einem verteidigten Kaltstart ist
ausgerechnet der, dessen Burggraben nicht existiert. Das ist die zentrale
Spannung dieses Projekts, und sie deutet auf die Lösung: **die schnelle Mechanik
(S02) in das langsame, verteidigbare Geschäft (S01) einbauen** — nicht beide als
Alternativen behandeln.

---

### ANGRIFF 4 — Gibt es irgendein Argument, das S13 rettet?

**Nein. Die ehrliche Rolle von Voice ist die eines Werkzeugs innerhalb eines
anderen Modells.**

Ich habe vier mögliche Rettungsargumente geprüft:

**Rettung 1: „Vertikal und tief integriert schlägt horizontal."**
Widerlegt durch plancraft PORTA. Wer tief in einen Vertikal integrieren kann, ist
der, dem die Vertikalsoftware gehört. Nico gehört keine. Er müsste tiefer
integrieren als der Eigentümer der Datenbank — strukturell unmöglich.

**Rettung 2: „Outbound statt Inbound ist unbesetzt."**
Teilweise richtig — der sichtbare Markt ist Empfang und Anrufannahme. Aber
Terminerinnerung mit Verschiebeoption wird bereits beworben [F-sek], und
Outbound ist technisch derselbe Stack mit anderem Trigger. Halbwertszeit dieses
Vorsprungs: 6–12 Monate.

**Rettung 3: „Bezahlung nach Ergebnis statt nach Minute."**
Das ist ein Preismodell, kein Geschäftsmodell. Es lässt sich in einer
Preisliste kopieren. Und es verschiebt Risiko zu Nico, was in einem Markt mit
fallenden Preisen die Marge zusätzlich drückt.

**Rettung 4: „DSGVO/deutsche Sprachqualität als Graben."**
Das war 2024 ein Argument. 2026 hosten alle in der EU und sprechen gutes Deutsch.

**Der einzig belastbare Rest:** Voice ist für Nico ein **Kostenvorteil und ein
Beschleuniger**, kein Produkt. In jedem Modell, in dem er die Kundenbeziehung
besitzt, kann er Kontaktaufnahme, Terminierung, Erinnerung, Nachfassen und
Mängelabfrage zu Grenzkosten von Cent-Beträgen betreiben, während der Wettbewerb
eine Bürokraft dafür bezahlt. Das ist ein realer, dauerhafter Vorteil — er ist
nur nicht verkäuflich, sondern nutzbar.

**Konkreter Vorschlag:** S13 aus der Shortlist streichen und stattdessen eine
Querschnittsnotiz „Voice als interne Fähigkeit" führen, die bei S01, S02, S07 und
S15 als Margenhebel eingerechnet wird. Damit verschwindet ein schwacher Kandidat
und ein starkes Asset bleibt sichtbar. S14 (White-Label-Motor für Telefonservices)
ist übrigens die einzige Voice-Variante mit einem echten strukturellen Argument
(40 Kunden statt 4.000) — und die Shortlist sagt selbst, dass sie als Maschine A
nicht reicht. Das ist konsistent.

---

### ANGRIFF 5 — Erreichen die Modelle 190.000 €/Monat? Brutal.

Zur Erinnerung: 30.000 € netto privat pro Monat ≈ 57.000–60.000 € Vorsteuergewinn
pro Monat ≈ bei 30 % EBITDA **190.000–200.000 € Monatsumsatz**. Bei niedrigerer
Marge entsprechend mehr.

| Modell | Realistischer ARPU/Monat [A] | Kunden für 190 k € | Realistische EBITDA-Marge | Umsatz, der 57 k € Gewinn trägt | Wahrscheinlichkeit in 60 Monaten |
|---|---|---|---|---|---|
| **S01** Overlay-Start | 800–1.500 € | 130–240 Standorte | 15–25 % | **230–380 k €** | **15–20 %** |
| **S01** Vollbündelung | 2.000–2.500 € (davon 70 % Durchleitung) | 76–95 | 8–15 % | **380–700 k €** | **< 10 %** |
| **S02** | 500–900 € | 210–380 Dienstleister | 20–30 % | 190–285 k € | **< 10 %** |
| **S03** | 500 € (unbelegt) | 380 SHK-Betriebe | 15–25 % | 230–380 k € | **< 5 %** |
| **S04** | 35 € je Aufschaltung | **5.400 Objekte** | 15–25 % | 230–380 k € | **10–15 %** |
| **S05** | 400–800 € | 240–475 Betriebe | 20–30 % | 190–285 k € | **< 10 %** |
| **S13** | 150–300 €, fallend | 630–1.270 | 10–20 % | 285–570 k € | **~ 0 %** |

**Die unbequeme Gesamtaussage:** Kein einziges der sechs Modelle erreicht das
Nordstern-Ziel mit einer Wahrscheinlichkeit über 20 %. Die Analyse verkauft
tatsächlich ein 100-k-Zwischenziel als Erfolg — und selbst das 100-k-Ziel
erreichen nur S01 und S04 mit nennenswerter Wahrscheinlichkeit, weil nur diese
beiden einen ARPU über der Filterregel von Befund 1 haben.

**Drei ehrliche Konsequenzen:**

1. **Der Zeithorizont ist falsch, nicht die Modelle.** Ein Koordinations- oder
   Plattformgeschäft mit 130–240 Firmenkunden aufzubauen ist ein **7–10-Jahres-
   Projekt** mit organischem Kapital, kein 5-Jahres-Projekt. 36–60 Monate sind
   im Nordstern als „Annahme" markiert. Diese Annahme sollte revidiert werden,
   bevor Modelle daran gemessen werden.

2. **Ein Modell allein reicht nicht — und das ist keine Ausrede, sondern eine
   Strukturaussage.** Die Kombination aus einem koordinierenden Kerngeschäft
   (S01), einem Kostenvorteil daraus (Voice/S02-Mechanik), einem Zukauf als
   Startrampe (S16) und später Lizenzierung (S15) kommt in Summe eher an das
   Ziel als jedes einzelne. Genau diesen Weg beschreibt S16 bereits, wird aber
   als „Markteintrittsstrategie" abgetan statt als Kern.

3. **Die Zielgröße selbst gehört auf den Prüfstand — das ist der größte Hebel
   im ganzen Projekt.** „30.000 € netto **privat entnommen** jeden Monat" ist die
   teuerste denkbare Formulierung des Nordsterns, weil sie doppelt besteuert
   wird (≈ 48 % effektiv). Der Nordstern sagt aber wörtlich: „Geld ist für mich
   kein Selbstzweck, sondern Entscheidungsfreiheit" und „Meine Kinder sollen
   nicht bei null anfangen müssen". Das ist eine **Vermögens**aussage, keine
   Entnahmeaussage. Bei 12.000–15.000 € privater Entnahme plus Thesaurierung und
   Vermögensaufbau in der Holding reicht ein Unternehmensumsatz von
   **110–130 k €/Monat** — und der ist bei S01 und S04 in 5 Jahren erreichbar.
   Die Differenz zwischen diesen beiden Zielformulierungen entscheidet über die
   Machbarkeit des gesamten Vorhabens und ist bisher nirgends diskutiert.
   **Empfehlung: Vor Welle 3 mit einem Steuerberater rechnen lassen. Diese eine
   Stunde ist mehr wert als drei weitere Recherche-Agenten.**

---

### ANGRIFF 6 — Selbstkritik der Recherche

**Die anfälligste Schlussfolgerung des Projekts** ist nicht ein einzelner
Negativbefund, sondern die **Rangfolge selbst**. Sie ist maßgeblich durch die
Heuristik „wo keine Preise stehen, sind die Margen hoch" (Befund 3, zweiter Teil)
erzeugt worden. Diese Heuristik hat systematisch alles abgewertet, was
recherchierbar war, und alles aufgewertet, was nicht recherchierbar war — in
einer Umgebung, in der **kein einziger Anbieter direkt gelesen werden konnte**.
Das ist ein Bewertungsverfahren, das Unwissen in Attraktivität übersetzt.

#### Die drei riskantesten Annahmen

**Annahme 1 — „Die Koordinationsmarge beträgt 70–90 %."**
Trägt S01, S04 und die gesamte Filterregel aus Befund 2. Belegt ist sie durch
drei Analogien, von denen **keine ein deutsches Koordinationsgeschäft** ist:
Otodata (US-Hardwarehandel), Aktenvernichtung (Routenlogistik), Blackline
(Hardwarehersteller). Meine Prüfung zeigt bei S01 eine Doppelzählung von
Durchleitungsumsatz und Marge, bei S04 eine Verwechslung von Grenzkosten des
Leitstellenbetreibers mit dem Einkaufspreis des Wiederverkäufers. Wenn die echte
Koordinationsmarge bei 40–55 % liegt, verletzen **beide Spitzenmodelle
Kriterium 2** und nähern sich K.-o. 5. **Kosten eines Irrtums: das gesamte
Geschäftsmodell.** Kosten der Prüfung: drei Telefonate.

**Annahme 2 — „Preisintransparenz ist ein positives Signal."**
Die Umkehrung ist mindestens genauso plausibel: Preisintransparenz bedeutet oft,
dass **jedes Geschäft ein Einzelfall** ist (→ K.-o. 4, keine Standardisierbarkeit),
dass Verkaufszyklen lang sind, oder dass es zu wenige Abschlüsse für eine
Preisliste gibt. KONE veröffentlicht keine Preise, weil jede Anlage anders ist —
nicht weil die Marge fett ist. Diese Annahme hat S13 nach unten und S01/S03/S05
nach oben sortiert. Wenn sie falschherum ist, ist die Reihenfolge falschherum.

**Annahme 3 — „Was wir nicht gefunden haben, existiert nicht."**
Alle sechs Modelle ruhen auf Negativbefunden aus 2–3 Suchen ohne eine einzige
geöffnete Anbieterseite. Meine Gegenrecherche hat in **vier von sechs Fällen** mit
je einer Suche Gegenbelege gefunden: Certado versendet Fälligkeitserinnerungen
bereits automatisch; plancraft PORTA existiert; Vaillant verkauft Fernüberwachung
ab 47 €/Monat; bundesweite Prüfservices decken bereits mehrere Gewerke unter
einem Ansprechpartner ab; der Retrofit-IoT-Markt ist dicht besetzt. Bei dieser
Trefferquote ist die Erwartung, dass **weitere 10 Suchen je Modell mindestens
einen weiteren relevanten Wettbewerber finden**, größer als 80 %.

**Zusatzannahme (Nummer 3b, weil sie emotional die gefährlichste ist) —
„CallSuite ist ein Vorsprung."**
CallSuite ist ein browserbasierter Dialer auf Twilio Voice SDK mit Listen- und
Arbeitszeitverwaltung. Ein KI-Voice-Agent mit Barge-in, Turn-Taking,
Funktionsaufrufen und Kalenderrückschreibung ist ein anderes Produkt. Der Abstand
zwischen CallSuite und einem Retell-/Vapi-Stack ist **nicht positiv**. Der echte
Vorsprung liegt woanders und ist wertvoller: Nico kennt die Ökonomie von
Erreichbarkeitsquoten, Wählversuchen und Terminkosten aus der Praxis. Das ist
Domänenwissen, kein Code — und es sollte als solches bewertet werden.

---

## 3. Korrekturvorschläge — was muss nach unten

| Position | Bisher | Vorschlag | Begründung |
|---|---|---|---|
| S01 Bruttomarge | 70–85 % | **35–55 %** (Durchleitung) bzw. Umsatzdefinition auf reine Koordinationsfee umstellen | Doppelzählung Fremdleistung/Marge |
| S01 Erlös je Standort | 5.000–30.000 €/Jahr | **3.600–18.000 €/Jahr** Koordinationsfee, getrennt vom Prüfvolumen ausweisen | Overlay-Realität, Angriff 2 |
| S01 Persönlichkeits-Fit | — | **deutlich runter** | Kern ist Fristen- und Einzelfallverwaltung = Anti-Liste 1+2 |
| S01 Unabhängigkeit von Nico | — | **runter** | Vertrauensverkauf, delegierbar erst Jahr 3–4 |
| S01 Wettbewerbsvorteil | „Lücke plausibel" | **„Lücke enger, Angriff von unten belegt"** | KFK, SI Prüfservice, AB Prüfservice |
| S02 Verteidigbarkeit | „Burggraben dünn" | **„kein Burggraben"** | plancraft PORTA, Certado-Automatik, Voisa-Schnittstellen |
| S02 Zahlungsbereitschaft | implizit hoch | **runter, Anker korrigieren** | 300 €/Termin gilt für Kaltakquise, nicht Bestandstermine |
| S02 Shortlist-Rang | Platz 2 | **kein eigenständiges Modell; Mechanik innerhalb S01/S15/S16** | Verstößt gegen die eigene Filterregel aus Befund 1 |
| S03 Beleg-Status | „[F-sek] Retention 70→97 %" | **„US-Kontext, nicht übertragbar"** | Gasheizung ≠ US-Klimaanlage; Kapazitäts- statt Nachfrageengpass |
| S03 offene Flanke P1 | „ungeprüft" | **„geprüft, negativ"** | Vaillant 47 €/Monat, Viessmann, Bosch, Tecalor-Partnerprogramme |
| S03 Kapitalbedarf | nicht ausgewiesen | **~1,2 Mio. € Hardwarevorfinanzierung bei Zielgröße** | 8.000 Sensoren × ~150 € |
| S04 Bruttomarge | 75–90 % | **45–60 %** | Grenzkosten ≠ White-Label-Einkaufspreis |
| S04 Verkaufszyklus | nicht ausgewiesen | **bis 12 Monate bei WEG-Verwaltern** | Beschluss der Eigentümerversammlung nötig |
| S04 Wettbewerbsvorteil | — | **runter** | Securitas 78.000 Aufschaltungen, Direktvertrieb der Leitstellen |
| S05 | Shortlist-Platz 5 | **mit S03 zusammenlegen, gemeinsam auf Beobachtung** | identische Struktur, identische Schwächen, besetzter Markt |
| S13 | Shortlist-Platz 13 | **streichen; als Querschnittsfähigkeit „Voice intern" führen** | Angriff 4 |
| Alle: Skalierbarkeit | „erreicht 100 k" | **Wahrscheinlichkeit ausweisen, nicht Möglichkeit** | Angriff 5 |
| Nordstern-Zielgröße | 190–200 k € Umsatz | **Entnahme- vs. Thesaurierungsszenario rechnen lassen** | Größter Einzelhebel des Projekts |

---

## 4. Was in 30 Tagen gemessen werden muss

Sieben Messungen, jede mit Abbruchschwelle. Zusammen unter 2.000 € und etwa
15 Arbeitstage. Sie ersetzen eine komplette weitere Recherchewelle.

| # | Messung | Vorgehen | Kennzahl | Abbruchschwelle |
|---|---|---|---|---|
| 1 | **Koordinationsmarge S04** (billigste, härteste Zahl im Projekt) | 3 VdS-Leitstellen als potenzieller Wiederverkäufer anfragen | Einkaufspreis je Aufschaltung/Monat | > 15 € bei 35 € Marktpreis → S04 auf < 60 % Marge korrigieren |
| 2 | **Wettbewerbshärtung von Hand** | Ein Mensch (nicht WebFetch) öffnet 30 Seiten: Maqsima, Prüfpilot, mybuilding24, netinform.RE, Certado, Vemas, KFK, SI/AB Prüfservice, 5 IFM-Mittelstandsangebote, 5 Voice-Anbieter | Anzahl Anbieter, die **Koordination fremder Gewerke** anbieten | ≥ 5 → S01-Positionierung neu schneiden |
| 3 | **Zahlungsbereitschaft S01** | 20 Anrufe bei technischen Leitern (50–500 MA). Frage: „Wer koordiniert Ihre Prüfungen heute, mit welchem Werkzeug, und was kostet Sie das intern?" — **nicht** „hätten Sie Interesse" | Anteil mit konkreter Zahl > 500 €/Monat · Anteil, der eine interne Person namentlich nennt (= der Blocker) | < 3 von 20 mit Zahl → Preispunkt auf 300–600 € korrigieren |
| 4 | **Der eine echte Feldtest** | Nico terminiert mit CallSuite + Voice-Layer für **einen** Prüfdienstleister 200 Bestandskunden gegen Erfolgshonorar | Erreichbarkeit · Termine je 100 Anrufe · Minuten je Termin · Vollkosten je Termin · Beschwerdequote · **Abschlussquote mit vs. ohne KI-Ansage** | Vollkosten > 40 % des erzielbaren Preises **oder** KI-Ansage senkt Quote > 30 % → S02-Mechanik neu bewerten |
| 5 | **Preisprobe S02** | 15 Prüfdienstleistern eine konkrete Zahl nennen: 250 €/Monat + 12 € je bestätigtem Termin | Anzahl **unterschriebener** bezahlter Piloten (nicht „interessant") | 0 von 15 → S02 endgültig streichen |
| 6 | **Versicherbarkeit S01** | 2 Gewerbemakler: Vermögensschadenhaftpflicht für „Koordination gesetzlicher Prüfpflichten" | Prämie · Deckungssumme · **Ausschlussliste** (insbesondere Personenschadenfolge) | kein Angebot oder Ausschluss der Kernleistung → Leistungsbeschreibung radikal verengen |
| 7 | **Entscheidungstakt S04** | 5 Verwalter fragen: neue monatliche Position ohne ETV-Beschluss möglich? | Anteil „ja" | < 2 von 5 → Zielgruppe auf Gewerbe/Eigentümer verengen, Marktgröße neu rechnen |

**Die wichtigste davon ist Nummer 4.** Sie testet in einem einzigen Experiment
gleichzeitig Marge, technische Machbarkeit, Regulatorik-Reibung,
Zahlungsbereitschaft und Nicos eigenes Empfinden bei der Arbeit — und sie kostet
nichts außer Zeit, weil das Asset existiert. Jede weitere Woche Schreibtisch-
recherche vor diesem Test ist verlorene Zeit.

---

## 5. Was nach dem Angriff steht

Damit dieser Bericht nicht nur abräumt:

- **Überlebt mit Korrekturen:** S01, aber als **Overlay** (Kataster, Fristen,
  Nachweisakte über bestehende Verträge, 300–800 €/Monat), mit schrittweiser
  Migration der Gewerke, harter Haftungsbegrenzung und der ehrlichen Ansage, dass
  es ein Dienstleistungsbetrieb mit Softwarelack ist. Und S04, aber erst nach
  Messung 1.
- **Überlebt nur als Werkzeug:** die S02-Mechanik und S13. Beide gehören in ein
  Modell, in dem Nico die Kundenbeziehung besitzt — dort sind sie ein
  dauerhafter Kostenvorteil statt ein unverteidigbares Produkt.
- **Sollten die Shortlist verlassen:** S03 und S05 in der vorliegenden Form.
- **Verdient mehr Aufmerksamkeit, als es bekommt:** S16 (Zukauf als Startrampe).
  Es löst genau die drei Probleme, an denen alle sechs Topmodelle kranken —
  Kaltstart, fehlende Referenz, fehlender Cashflow in Monat 1 — und es ist das
  einzige Modell, dessen Kritikpunkt (K.-o. 1) durch Struktur statt durch Glück
  auflösbar ist. Der Satz der Shortlist „nur zulässig, wenn der Betrieb Rohstoff
  ist" ist richtig und sollte zum Ausgangspunkt gemacht werden, nicht zur Fußnote.

---

## Quellen (alle [F-sek], Suchsynthese, keine Primärseite geöffnet)

- [Certado Suite – Prüfdienstleister](https://www.certado.io/pruefdienstleister/) · [Prüffristen verwalten](https://www.certado.io/funktionen/prueffristen/)
- [plancraft PORTA – KI-Telefonassistent](https://plancraft.com/de-de/porta/ki-telefonassistent) · [bau.bi zu PORTA](https://bau.bi/baumagazin/betriebsfuehrung/digitalisierung-porta-ki-front-office-soll-handwerksbetriebe-entlasten-b21395)
- [Voisa – KI-Telefonassistent Handwerker](https://www.voisa.ai/ki-telefonassistent/handwerker) · [Agentino – Terminplanung Handwerker](https://agentino.de/blog/terminplanung-handwerker-tools-apps/)
- [Placetel – KI Telefonassistent Vergleich 2026](https://www.placetel.de/ratgeber/ki-telefonassistent) · [Superchat – 12 beste Anbieter](https://www.superchat.de/blog/bester-ki-telefonassistent-preise-funktionen)
- [ACC Sicherheitstechnik – Kosten Aufschaltung 2026](https://accsicherheitstechnik.de/wie-hoch-sind-kosten-der-aufschaltung-zur-leitstelle-2026/) · [Securitas NSL](https://www.securitas.de/services/remote/notruf-und-serviceleitstelle/)
- [KFK Torservice & Safety Prüfservice](https://www.torservice-deutschlandweit-kfk.de/) · [KFK Konrad Elektroprüfungen](https://www.pruefservice-kfk.de/) · [SI Prüfservice](https://www.si-pruefservice.de/) · [AB Prüfservice](https://abpruefservice.de/)
- [TÜV NORD – Betreiberpflichten wahrnehmen und delegieren](https://www.tuev-nord.de/de/unternehmen/bildung/wissen-kompakt/betreiberpflichten-wahrnehmen-und-delegieren-so-vermeiden-unternehmen-rechtsfolgen/) · [TÜV SÜD netinform.RE](https://www.tuvsud.com/de-de/branchen/real-estate/technische-gebaeudeausruestung-und-aufzuege/betreiberverantwortung-netinform-re)
- [tga-fachplaner – digitale Wärmepumpen-Überwachung](https://www.tga-fachplaner.de/meldungen/wartung-verbraucher-wollen-digitale-waermepumpen-ueberwachung) · [digimax SHK-Handwerk](https://digimax.de/branchen/shk-handwerk) · [IKZ – Lizenzmodell fürs SHK-Handwerk](https://www.ikz.de/detail/news/detail/pellet-waermepumpen-hybridheizung-neues-lizenzmodell-fuers-shk-handwerk/)
- [Tecson IoT](https://iot.tecson.de/) · [deltaheat Retrofit Monitoring](https://www.deltaheat.de/digitalisierung-heizungskeller/heizungsanlage-digitalisieren-mit-retrofit-monitoring/) · [Pexon IoT-Retrofit](https://pexon-consulting.de/ki-beratung/ai-agent/ki-retrofit-industrie-4-0/)
- [dievertriebswikinger – Kaltakquise outsourcen Kosten 2026](https://dievertriebswikinger.de/kaltakquise-outsourcen-kosten/) · [callcenterdirect – B2B Preise](https://www.callcenterdirect.de/call-center-b2b-preise-vergleichen)
- [Württembergische – Vermögensschadenhaftpflicht](https://www.wuerttembergische.de/geschaeftskunden/vermoegensschadenhaftpflichtversicherung/) · [für-gründer – VSH prüfen](https://www.fuer-gruender.de/wissen/unternehmen-gruenden/versicherung/gewerbliche-haftpflichtversicherung/vermoegensschadenhaftpflicht/)

---
---

# NACHTRAG (Abschnitte 6–8)

Anlass: S08 wurde in Welle 2 nie angegriffen und wäre allein deshalb Sieger
geworden. Zusätzlich: Angriff auf die Kombination, die sich aus meinem eigenen
Abschnitt 5 ergibt, und eine Empfehlungsfrage.
Suchbudget Nachtrag: 6 WebSearch-Anfragen, davon zwei mit schwachem Ertrag
(Danfoss statt Wurm/Eckelmann; Zentraleinkauf nur generisch). WebFetch weiter 403.

---

## 6. S08 — Monitoring-as-a-Service mit B2B2B-Zahler · Urteil: **WIDERLEGT im Kühlketten-Zweig, ANGESCHLAGEN im Tank-/Silo-Zweig**

### 6.0 Vorbemerkung: das natürliche Experiment

S08 stand bei Agent 09 auf Fit-Platz 5 (7,0) und bei Agent 06 auf
Delegierbarkeits-Platz 3. Es hatte grüne Ampeln in Regulatorik, Marge und
Kriterium 5. Es hatte diese Ampeln, weil **niemand hingesehen hat**. Sechs
Suchen später steht davon wenig. Das ist kein Vorwurf an einen einzelnen
Agenten — es ist der Beweis für Annahme 3 aus Abschnitt 2 in Reinform:
**Die Rangfolge dieses Projekts korreliert mit Rechercheintensität, nicht mit
Modellqualität.** S08 ist der Kontrollversuch, der das zeigt.

### 6.1 Ist der Markt besetzt? — Ja, dreifach, und Testo macht es tatsächlich schon

**Schicht 1 — der Messtechnik-Konzern.** Testo verkauft mit **Saveris 2 und
Saveris 3** exakt das beschriebene Produkt: Funk-Datenlogger in Kühlmöbeln,
Kühlräumen und Lagern, automatische Cloud-Übertragung, HACCP-konforme
Dokumentation, Alarm per E-Mail, SMS und Push, Multi-Standort-Überwachung über
Filialen hinweg, eigene Anwendungsseite „Automatische Temperaturüberwachung in
Lebensmittelmärkten", Referenzen im deutschen LEH [F-sek, testo.com]. Testo ist
kein Startup, sondern ein deutscher Messtechnikkonzern mit Kalibrierlaboren,
Außendienst und Konzerneinkaufszugang. **Die Antwort auf „macht der das schon?"
lautet: ja, seit Jahren, produktisiert, mit eigener Cloud.**

**Schicht 2 — die Kältetechnik-Regelung, und die ist gefährlicher.**
Danfoss betreibt mit **Alsense** eine Cloud für Food Retail mit
Alarmmanagement, 24/7-Monitoring-Integration und Performance-Tracking, bei über
**50.000 Food-Retail-Installationen weltweit** [F-sek, danfoss.com]. Im
deutschen Markt kommt **Wurm** (Remscheid) dazu, mit eigenem Funksensor
`W-LINKpro` und einem Flyer, der wörtlich „HACCP-konformes Temperaturmonitoring"
überschrieben ist [F-sek, wurm.de].

Das ist die S08-Version des Certado-Problems aus Angriff 1: **Diese Anbieter
besitzen bereits den Kälteregler in jedem Kühlmöbel.** Die Temperaturdaten
entstehen ohnehin in ihrer Hardware. HACCP-Dokumentation ist für sie ein
Softwaremodul auf vorhandener Sensorik, für Nico ist es ein Hardware-Rollout.
Der Grenzkostenunterschied ist nicht knapp, er ist strukturell.

**Schicht 3 — die Preisbrecher, und die entscheiden die Sache.**
**TEMPASCAN: ab 39 €/Monat inklusive Sensoren, Gateway, Lizenz, Checklistenmodul
und allen Berichten für die Behörde** [F-sek, tempascan.com]. Dazu Sencono
(„günstig & smart", ausschließlich Miete), COMOTIX (4G/5G-Fernüberwachung
Lebensmittel/Gastro), ELPRO, ebro, LineMetrics, Plug and Track.

**Damit greift Befund 3 des Projekts gegen S08, nicht für es.** Der Preis steht
öffentlich im Netz, mit Hardware inklusive, ab 39 €. Nach der eigenen Heuristik
des Projekts ist das ein Preiskampfmarkt. Die Shortlist führt stattdessen
„Sencono beweist reine Gerätemiete im deutschen Markt [F]" als Stärke. Die
umgekehrte Lesart ist die richtige: **Sencono vermietet ausschließlich, weil der
Kunde die Hardware nicht kaufen will.** Das ist kein Margenbeleg, das ist ein
Kapitalbindungsbeleg.

**Der Schädlings-Zweig ist am härtesten besetzt.** Anticimex ist ein
schwedischer Konzern von 1934 mit europäischer Konsolidierungsmaschine und
vermarktet **SMART / Smart Connect** als permanentes, digitales
24/7-Schädlingsmonitoring für Lebensmittelindustrie und Handel, mit dem Argument
**„bis zu 70 % weniger Technikerbesuche"** [F-sek, anticimex.de]. Das ist
dasselbe Nutzenversprechen wie S08 — von einem Anbieter, der die Ausführung
gleich mitliefert und Betriebe aufkauft.

### 6.2 Hält die Marge? — Die Kapitalrechnung, die in der Shortlist fehlt

Die Shortlist sagt „70–85 % nach Amortisation [S]". Der Halbsatz „nach
Amortisation" trägt das ganze Gewicht und wird nirgends beziffert. Hier ist die
Rechnung.

**Annahmen [A], jeweils Bandbreite:**
- ARPU je Standort: 100 €/Monat (zwischen TEMPASCAN 39 € und einem Premium-Paket
  von 150–250 €)
- Messpunkte je Standort: 8 (Bäckerei-/Gastrofiliale 4–8, Supermarkt 15–30)
- Sensorstückpreis: 40–80 € (einfache LoRaWAN-Sensoren 30–70 € [F-sek]; mit
  Lebensmittelsonde und Kalibriernachweis am oberen Rand)
- Gateway/Router je Standort: 150–400 €
- Installation/Inbetriebnahme: 100–300 €

| Position | je Standort |
|---|---|
| 8 Sensoren | 320–640 € |
| Gateway | 150–400 € |
| Installation | 100–300 € |
| **Summe Hardware + Setup** | **570–1.340 €, Mittel ≈ 900 €** |

| Zielgröße | Standorte | **Vorfinanzierte Hardware** |
|---|---|---|
| 100.000 € MRR | 1.000 | **0,57–1,34 Mio. €, Mittel ≈ 0,9 Mio. €** |
| 190.000 € MRR | 1.900 | **1,1–2,5 Mio. €, Mittel ≈ 1,7 Mio. €** |

**Payback je Standort:** 900 € Hardware gegen 100 € Umsatz abzüglich
Konnektivität (2–4 €), Cloud (5–10 €), Support/Alarmbearbeitung (10–20 €) →
Deckungsbeitrag 65–80 €/Monat → **12–14 Monate reiner Hardware-Payback, vor
Kundenakquisitionskosten.** Mit CAC eher 18–24 Monate.

**Die eigentliche Konsequenz ist nicht die Marge, sondern das Vorzeichen des
Cashflows.** Bei 50 neuen Standorten pro Monat fließen ~45.000 € Hardware ab und
5.000 € neuer MRR zu. **Ein wachsendes S08 ist operativ dauerhaft
cashflownegativ**, bis das Wachstum aufhört. Das ist die Definition eines
Vermietungsgeschäfts, und es ist das exakte Gegenteil dessen, was der Nordstern
verlangt („hoher wiederkehrender Cashflow", „Entnahmen für die Familie"). Ein
Unternehmen mit 190 k € MRR und 1,7 Mio. € Hardware im Feld schüttet keine
57 k €/Monat aus — es finanziert.

Drei Auswege, alle mit Preis:
1. **Kunde kauft die Hardware** → kein Abo mehr, sondern Handelsgeschäft mit
   20–30 % Handelsspanne plus kleinem Lizenzabo. Kriterium 2 verletzt.
2. **Leasing/Mietkauf über Dritte** → Kapitalproblem gelöst, aber der
   Leasinggeber nimmt seine Marge; realistisch bleiben 45–55 %. Nähe zu K.-o. 5.
3. **Bei 39 € Marktpreis mitgehen** → Payback über 24 Monate, K.-o. 6.

**Urteil zur Marge:** Die 70–85 % beschreiben Jahr 3+ *eines einzelnen
Bestandskunden*, nicht das Unternehmen. Als Unternehmenskennzahl im Wachstum
sind sie **irreführend**. Realistische Bruttomarge über den Lebenszyklus
inklusive Hardwareabschreibung: **45–60 %**.

### 6.3 Der B2B2B-Zahler — das Kernargument, und es kippt

Die Shortlist feiert den zentralen Einkauf als strukturelle Lösung von
Kriterium 5. **Er ist gleichzeitig die strukturelle Verletzung von drei anderen
Kriterien.** Die Frage des Koordinators ist genau richtig gestellt: Ja, eine
Filialzentrale kauft zentral ein — und *deshalb* ist es ein Problem.

**Was ein Zentraleinkauf real bedeutet:** Lieferantenregistrierung,
Präqualifikation (Bonität, Versicherungssummen, Zertifikate, oft
Mindestumsatz und Referenzen vergleichbarer Größe — ein Zweijahresunternehmen
erfüllt das nicht), Lastenheft, Pilot in 3–5 Filialen, Bewertungsmatrix,
Preisverhandlung, Rahmenvertrag, Rollout-Planung. Mitentscheider: Facility-/
Category-Einkauf, QM bzw. Lebensmittelsicherheit, **IT** (Sensoren im Filialnetz
sind ein Security- und Netzfreigabethema — der stille Projektkiller), Technik/
Kältetechnik (die haben Danfoss oder Wurm und fragen, wozu ein zweites System),
Datenschutz, ggf. Betriebsrat. **Realistische Dauer Erstkontakt bis Rollout:
12–24 Monate [A], plus 6–12 Monate Rollout.**

**Und jetzt der Abgleich mit Nicos Anti-Liste.** Das ist Verkauf an
Konzerneinkauf mit Lastenheften, Jahresgesprächen, Preisrunden und
Ausschreibungswiederholung alle 3 Jahre. Es ist damit:
- „steifes Anzug-Business" — Anti-Liste, wörtlich
- „Abhängigkeit von Konzernen" — Anti-Liste, wörtlich
- strukturell dasselbe Muster, das ihn in der Finanzberatung stört, nur mit
  anderem Gegenüber

**Zusätzlich ein Risiko, das die Shortlist nirgends bewertet: Klumpenrisiko.**
Wenn 10 Kunden 100 k € MRR tragen, ist jede Kündigung ein Umsatzeinbruch von
10 % über Nacht — und beim Unternehmensverkauf bewertet ein Käufer
Kundenkonzentration mit **Abschlag**, nicht mit Prämie. Damit stehen
**Kriterium 5 („wenige hochwertige Kunden") und Kriterium 8 („verkaufbarer
Unternehmenswert") in direkter Spannung.** Das gilt über S08 hinaus für S14 und
für jedes B2B2B-Modell im Projekt und sollte als Querschnittsbefund geführt
werden. Faustregel: unterhalb von ~25 Kunden wird Kriterium 5 zur Gefahr für
Kriterium 8.

**Marktgröße, ehrlich:** Deutsche Filialketten mit 200+ kühlpflichtigen
Standorten sind EDEKA, REWE, Aldi, Lidl, Kaufland, Netto, Penny, Norma und die
Drogerieketten — sie sind **alle bereits ausgestattet** (Testo, Wurm, Danfoss).
Das adressierbare Segment sind mittelgroße Ketten mit 30–80 Standorten:
3.000–8.000 €/Monat je Kunde, also **25–60 solcher Ketten für 190 k €**. Das ist
rechnerisch nicht absurd — aber 25–60 gewonnene Ausschreibungen in 60 Monaten
bedeutet einen Gewinn *pro Monat*, dauerhaft, bei 12–24 Monaten Zykluszeit. Das
verlangt eine Pipeline von 150–300 laufenden Vorgängen und ein Key-Account-Team.

### 6.4 Wechselaufwand und der erste Kunde

Die Shortlist führt „extrem niedriger Churn durch verbaute Hardware" als Stärke.
**Das ist symmetrisch — und asymmetrisch zu Nicos Nachteil.** Ein Markt mit hohen
Wechselkosten ist für den Bestandsanbieter ein Burggraben und für den Angreifer
die schlechteste denkbare Ausgangslage. Nico ist der Angreifer.

Wie gewinnt man den ersten Kunden gegen einen Bestandsanbieter mit verbauter
Hardware? Nur über einen von vier Wegen:
1. **Migrationsanlass** (Systemabkündigung, Filialumbau, neue Kälteanlage,
   Kettenübernahme) — Timing-Geschäft mit Zufallskomponente, nicht planbar
2. **Vorfall** (Behördenbeanstandung, Warenverlust, Bußgeld) — nicht planbar
3. **Preis** — K.-o. 6, und gegen 39 € kaum unterbietbar
4. **Hardware kostenlos stellen und nur Lizenz berechnen** — verdoppelt den
   ohnehin nicht ausgewiesenen Kapitalbedarf

**Keiner dieser vier Wege ist ein Vertriebsprozess.** Drei davon sind Warten.

### 6.5 Wer baut es in 6 Monaten nach?

Falsche Frage. **Es ist gebaut.** Testo, Danfoss Alsense, Wurm, TEMPASCAN,
Sencono, COMOTIX, LineMetrics, ELPRO, ebro, Plug and Track, Anticimex im
Schädlingszweig, Otodata und Tecson im Tankzweig. Der einzige unbesetzte Winkel
ist der, den die Shortlist selbst nennt: **„Alarm per Anruf statt E-Mail, die
nachts niemand liest."** Das ist ein starker Gedanke — und ein Feature, das in
einer Sprintwoche nachgebaut ist. Es ist derselbe Differenzierer wie bei S02 und
S13, und er ist zum dritten Mal keine Verteidigungslinie, sondern ein Werkzeug.

### 6.6 Die restlichen Prüfpunkte

**Regulatorik ist nicht grün, sondern gelb.** HACCP-Dokumentation ist
beweiserheblich gegenüber der Lebensmittelüberwachung. Fällt sie aus und der
Betrieb kassiert eine Beanstandung oder kann eine Charge nicht freigeben, ist
das ein Vermögensschaden mit derselben Deckungslücke wie bei S01. Zusätzlich:
HACCP-relevante Messmittel unterliegen Kalibrier- und Rückführbarkeits-
anforderungen — ein wiederkehrender, nachweispflichtiger Prozess, den Testo als
Messtechnikkonzern nebenbei mitliefert und den Nico einkaufen müsste.
Kühlraumdaten (Tür offen, wann, wie lange) berühren im Zweifel
Leistungs- und Verhaltenskontrolle → BetrVG § 87.

**Delegierbarkeit (Agent 06, Platz 3) — formal richtig, ökonomisch teuer.**
1.900 Standorte im Feld bedeuten: RMA, Fehlalarmbearbeitung, Gateway-Ausfälle,
Netzumstellungen, Kalibrierzyklen — und **Batteriewechsel**. Bei 2–5 Jahren
Batterielaufzeit und ~15.000 Sensoren sind das **3.000–7.500 Batteriewechsel pro
Jahr**, also ein eigener Außendienst- oder Versandprozess. Ja, das ist
delegierbar. Delegierbar heißt aber nicht margenneutral: Es ist genau die
Kostenschicht, die die 70–85 % auf 45–60 % drückt. Ich senke nicht die
Delegierbarkeit, ich senke die Marge, aus der delegiert wird.

**Nico-Abhängigkeit:** niedriger als bei S01 — der einzige Punkt, an dem S08
tatsächlich gut abschneidet. Ausschreibungsverkauf ist delegierbar an einen
Key-Account-Manager, sobald Referenzen existieren.

**Der einzige Teil von S08, der weiter geprüft gehört:** der **Tank-/Silo-Zweig**.
Dort ist der Zahler der **Lieferant** (Heizöl, Flüssiggas, Futtermittel,
Schmierstoffe), und sein ROI ist keine Compliance, sondern **eingesparte
Leerfahrten** — ein echter Euro-ROI im Sinne von Befund 4, den der Kühlketten-
Zweig nicht hat. Otodata und Tecson besetzen ihn, das Klumpenrisiko bleibt, und
die Kapitalrechnung gilt unverändert. Aber es ist die einzige S08-Variante, die
nicht an der Zahlungsbereitschaft scheitert.

### 6.7 Korrekturvorschlag S08

| Position | Bisher | Vorschlag |
|---|---|---|
| Bruttomarge | 70–85 % | **45–60 %** über Lebenszyklus inkl. Hardware |
| Kapitalbedarf | nicht ausgewiesen | **0,9 Mio. € für 100 k MRR · 1,7 Mio. € für 190 k MRR** |
| Cashflow-Profil | implizit positiv | **im Wachstum negativ** — Widerspruch zum Nordstern |
| Regulatorik | grün | **gelb** (Beweiserheblichkeit, Kalibrierung, BetrVG) |
| Kriterium 5 gelöst | ja | **ja, erzeugt aber Klumpenrisiko gegen Kriterium 8** |
| Persönlichkeits-Fit | Platz 5 (7,0) | **deutlich runter** — Konzerneinkauf = Anti-Liste „Anzug-Business", „Konzernabhängigkeit" |
| Verkaufszyklus | nicht ausgewiesen | **12–24 Monate** bis Rahmenvertrag |
| Wettbewerb | „Sencono beweist Gerätemiete" | **dicht besetzt: Testo, Danfoss Alsense, Wurm, TEMPASCAN ab 39 € inkl. Hardware** |
| Shortlist-Rang | Anwärter auf Platz 1 | **Kühlkette streichen · Tank/Silo als eigener Kandidat weiterführen** |

**S08 wäre nicht Sieger geworden. Es war nur unbeschossen.**

---

## 7. Angriff auf die Kombination: S16-Zukauf + S01-Overlay + Voice als Werkzeug

### 7.1 Kohärentes Unternehmen oder Bastelwerk aus drei Halbmodellen?

Der Test, den ich anlege: Gibt es **einen** Kunden, **ein** Nutzenversprechen und
**eine** Erlöslogik, oder werden drei Geschäfte nebeneinander betrieben?

Aufgeschlüsselt:
- **Gekaufter Prüfbetrieb:** Kunde = Gewerbestandort mit Prüfpflicht.
  Erlös = Prüfleistung je Stück/Einsatz. Marge 45–60 %.
- **S01-Overlay:** Kunde = **derselbe Standort**, aber ein anderer Käufer im
  Haus (GF/HSE statt Technik/Einkauf). Erlös = Abo 300–800 €/Monat.
- **Voice:** kein Kunde, kein Erlös — interner Kostenvorteil in Terminierung,
  Erinnerung, Nachfassen, Mängelabfrage.

**Urteil: kohärent, kein Bastelwerk — aber nur unter einer scharfen Bedingung.**
Es ist genau dann ein Unternehmen, wenn die Kundenliste des gekauften Betriebs
**die Zielgruppe des Overlays ist**. Dann ist die Sequenz sauber: Der Betrieb
liefert Zutritt und Vertrauen, das Overlay liefert MRR und Marge, Voice liefert
den Kostenvorteil, mit dem beides billiger läuft als beim Wettbewerb. Das
Overlay wird dann **kein Kaltverkauf mehr, sondern ein Upsell an Bestandskunden**
— und damit ist genau der Einwand entschärft, der in Angriff 2 S01 am härtesten
getroffen hat: „Warum sollte ein GF einem Neuling ohne Referenz vertrauen?"
Er tut es nicht. Er tut es dem Betrieb, der seit elf Jahren seine Elektroprüfung
macht.

Das ist der stärkste strukturelle Gedanke, der in diesem Projekt bisher
aufgetaucht ist, und er steht in der Shortlist nur als Fußnote (S16 als
„Markteintrittsstrategie").

**Die Bedingung ist aber eng und verknappt das Suchprofil drastisch:** Der
Kaufkandidat muss (a) viele kleine Gewerbekunden haben statt weniger
Großaufträge, (b) gesetzlich getaktete Wiederkehr, (c) eine bedienbare Region,
(d) übertragbare Qualifikation im Haus. Bei ~1.000 Vermittlungen/Jahr über
nexxt-change [F] passen davon vielleicht **5–20 pro Jahr bundesweit [A]**. Das
ist ein **Suchprozess von 12–24 Monaten**, kein Einkauf. Wer das unterschätzt,
kauft aus Ungeduld den falschen Betrieb — und der falsche Betrieb ist keine
Rampe, sondern ein Job.

### 7.2 Widerspricht der Kauf K.-o. 1? — Nein formal, ja praktisch

**Formal nicht.** K.-o. 1 lautet: „Nico muss nach 24 Monaten noch zwingend
**Hauptleistungserbringer** sein." Bei einem Prüfbetrieb erbringt die
Elektrofachkraft die Leistung, nicht der Inhaber. Nico wäre Eigentümer und
Geschäftsführer, nicht Leistungserbringer. Die Unterscheidung ist echt und
rettet das Kriterium — im Gegensatz zu einem gekauften Ein-Mann-Betrieb, wo der
Inhaber tatsächlich der Betrieb ist. Das ist auch die Präzisierung, die die
Shortlist-Warnung („in dieser Betriebsgröße ist der Inhaber der Betrieb")
braucht: **Sie gilt unter ~5 Mitarbeitern. Ab 6–12 Mitarbeitern mit angestelltem
Meister gilt sie nicht mehr.** Die Untergrenze der Betriebsgröße ist damit ein
K.-o.-Kriterium des Kaufprofils, keine Preisfrage.

**Praktisch aber trifft es ein anderes Kriterium, härter.** Verletzt wird nicht
K.-o. 1, sondern die Anti-Liste: „bei jedem Mitarbeiterproblem eingebunden sein",
„operatives Tagesgeschäft persönlich kontrollieren", „Buchhaltung", „Fristen und
Einzelfälle verwalten". Bei einem 6–12-Mann-Betrieb ist der Inhaber in den
ersten Monaten Personalchef, Disponent, Reklamationsstelle und
Buchhaltungsaufsicht **gleichzeitig**.

**Wie wird der Betrieb wirklich „Rohstoff statt Ziel"?** Vier prüfbare
Testfragen, alle **vor** dem Kauf beantwortbar:
1. **Finanziert sein Cashflow die Plattform, oder ersetzt er sie?** Wenn Nico
   nach 24 Monaten immer noch überwiegend Prüfumsatz macht, war der Betrieb das
   Ziel. Messgröße: Anteil Overlay-MRR am Gesamtumsatz in Monat 24. Zielwert
   ≥ 20 %.
2. **Passt die Kundenliste zur Overlay-Zielgruppe?** Messgröße: Anzahl Kunden mit
   50–500 Mitarbeitern. Zielwert ≥ 80.
3. **Ist die Leistung über die eigene Kapazität hinaus skalierbar?** Also: Kann
   ein Partnerbetrieb sie mit erbringen, ohne dass der Kunde es merkt? Wenn nein,
   ist die Wachstumsgrenze die Personalgrenze.
4. **Ist Nico sein Vertriebsmotor?** Wenn der Betrieb ohne Inhaberverkauf keine
   Neukunden gewinnt, kauft man eine Abhängigkeit.

**Und das Bindungsproblem hat eine belegte Lösung, die die Shortlist bereits
enthält, ohne sie als solche zu erkennen:** Der Finanzierungsmix mit
**10–30 % Verkäuferdarlehen** [F] ist nicht nur Finanzierung, er ist das
**Bindungsinstrument**. Ein Verkäufer mit ausstehendem Darlehen und Earn-out
bleibt 12–24 Monate erreichbar und übergabewillig. Alternative: nur Betriebe
kaufen, die bereits einen **angestellten Meister/Betriebsleiter** haben. Beides
verteuert und verknappt — und beides muss in den Kaufpreis, nicht in die
Hoffnung. Konkret: eine kaufmännische Leitung ab Monat 1 kostet 60–80 k €/Jahr
und senkt den maximal tragbaren Kaufpreis um rund **ein Multiple**.

### 7.3 Löst der Zukauf das Fit-Problem oder verschärft er es?

**Kurzfristig verschärft er es massiv, und das muss so gesagt werden.**

Agent 09 warnt, dass Fristen- und Einzelfallverwaltung Nico auslaugt. Ein
gekaufter Prüfbetrieb ist exakt das — plus Lohnbuchhaltung, plus Fuhrpark, plus
Krankmeldungen. In den ersten 9–15 Monaten trifft Nicos Alltag **alle zehn
Punkte der Anti-Liste gleichzeitig**. Das ist kein Nebeneffekt, das ist der
Kaufgegenstand.

Die ehrliche Formulierung lautet:

> **Der Zukauf tauscht ein Risiko gegen eine Belastung.**
> Greenfield: geringe Belastung, hohes Scheiterrisiko — kein Kunde, kein
> Cashflow, 6–12 Monate bis zum ersten Euro, unbelegte Zahlungsbereitschaft,
> Verteidigbarkeit, die bei einer einzigen Suche gerissen ist.
> Zukauf: Cashflow und Referenz ab Monat 1, dafür 12–24 Monate Anti-Liste-Alltag.

**Damit ist die Wahl keine analytische Frage mehr, sondern eine Charakterfrage.**
Die Analyse sollte sie offenlegen statt sie wegzurechnen. Nicos Profil sagt
„bereit, in der Aufbauphase intensiv und operativ zu arbeiten" — aber bei ihm
heißt operativ *bauen und verkaufen*, nicht Urlaubsanträge genehmigen und
Krankmeldungen umdisponieren. Genau hier kollidiert das Persönlichkeitsprofil
mit dem Kaufpfad, und es ist die wichtigste Information, die Nico für seine
Entscheidung braucht.

**Mittelfristig löst der Zukauf das Fit-Problem allerdings besser als jede
Alternative** — weil er derjenige Pfad ist, der die Verwaltungsarbeit
**finanzierbar** macht. Ein Betrieb mit 800 k–1,5 Mio. € Umsatz trägt ab Tag 1
eine Bürokraft, einen Disponenten und später eine kaufmännische Leitung. Ein
Greenfield-Startup mit 4 k € MRR in Monat 9 trägt niemanden — dort macht Nico
die Verwaltung selbst, nur unbezahlt und länger.

### 7.4 Was kostet der Umbau zum Plattformbetrieb an Zeit? — Ehrlich: 5–7 Jahre

| Phase | Monate | Inhalt | Nicos Rolle |
|---|---|---|---|
| Suche & Kauf | 0–12 | nexxt-change/Vermittler, Due Diligence, KfW/Bank/Verkäuferdarlehen, Übergabe | Käufer, Verhandler — passt gut |
| Stabilisierung | 12–24 | **nichts umbauen außer den eigenen Prozessen**: Kundenstamm, Fälligkeiten, Prüfdaten sauber digitalisieren. Voice-Terminierung **intern** einführen — hier zahlt das Asset zum ersten Mal, weil es keinen Verkauf braucht, nur eine Entscheidung. Messgröße: Auslastung der Prüfer | Betriebsleiter wider Willen — passt schlecht |
| Overlay | 24–36 | Kataster/Fristen/Nachweisakte an Bestandskunden verkaufen, erste Fremdgewerke über Partner. Erster plattformartiger MRR | Verkäufer, Produktarchitekt — passt sehr gut |
| Fläche | 36–60 | zweiter Betrieb oder Partnernetz, Software produktisieren, ggf. Lizenzierung (S15) | Unternehmensarchitekt — passt ideal |

**Realistisches Ergebnis nach 60 Monaten [S]:** 2–4 Mio. € Umsatz, 15–25 %
EBITDA → 300–600 k € Gewinn/Jahr = **25–50 k €/Monat vor Steuern**, davon
40–50 % wiederkehrend. Unternehmenswert bei 4,1–5,7× EBITDA plus der belegten
**+1× Multiple-Prämie ab 30 % wiederkehrenden Umsätzen** [F]: grob 1,5–4 Mio. €.

Das liegt **unter** dem Nordstern-Ziel von 57 k €/Monat Vorsteuergewinn — aber es
ist die höchste Zahl, die ich in diesem gesamten Projekt für einen Pfad mit
Wahrscheinlichkeit über 30 % ausrechnen kann. Und es baut nebenbei einen
verkaufbaren Unternehmenswert auf, was fünf der sechs Topmodelle in 60 Monaten
nicht tun.

### 7.5 Urteil zur Kombination

**Kein Bastelwerk — eine Sequenz.** Sie ist die einzige Struktur im Projekt, die
Kaltstart, fehlende Referenz und fehlenden Cashflow **gleichzeitig** löst, und
die einzige, in der Nicos zwei echte Assets (Verkaufsfähigkeit,
Telefonie-Ökonomie) ab Monat 1 wirken statt nach einem neunmonatigen Produktbau.

Preis: 12–24 Monate Anti-Liste-Alltag, ein 5–7-Jahres-Horizont, ein
12–24-monatiger Suchprozess mit engem Profil, und ein Kaufpreis, der eine
kaufmännische Leitung mit einpreisen muss.

Sie kippt, wenn eine der vier Bedingungen aus 7.2 nicht erfüllbar ist — vor
allem, wenn kein Betrieb mit angestelltem Meister und passender Kundenliste
gefunden wird. Dann ist der Kauf keine Rampe, sondern ein gut bezahlter Job mit
Kredit.

---

## 8. Auftrag 3 — Die ehrlichste Empfehlung

### 8.1 Zuerst: Option (c) ehrlich geprüft

Nach 17 Suchen und 99 gesichteten Modellen zu behaupten, es gebe „etwas ganz
anderes", wäre unseriös. Eine **Klasse** fehlt aber tatsächlich als eigene,
benannte Option — sie steckt halb in S16 und halb in S15, ohne je zusammengeführt
worden zu sein:

> **(c′) Buy-and-Build: 4–6 Prüf-/Wartungsbetriebe derselben Nische mit
> gemeinsamer Steuerungsschicht.** Nicht ein Betrieb als Rampe, sondern eine
> Holding mit gemeinsamer Disposition, Terminierung, Nachweis-Software, Einkauf
> und Marke. Genau dort wirkt der belegte Hebel „+1× Multiple-Prämie ab 30 %
> wiederkehrenden Wartungsumsätzen" [F] — auf einer größeren Basis, und die
> Steuerungsschicht wird zum Margenhebel über alle Betriebe hinweg.

Rechnerisch ist das **der einzige Pfad im gesamten Projekt, der 190 k €/Monat
mit über 50 % Wahrscheinlichkeit erreicht**: 5 Betriebe à 1,5 Mio. € Umsatz sind
7,5 Mio. €/Jahr = 625 k €/Monat, bei 12–18 % EBITDA also 75–110 k €/Monat
Gewinn — deutlich über dem Ziel. Kapitalbedarf 1,5–3 Mio. €, Finanzierung über
den belegten Mix (EK 10–30 %, Bank/KfW 50–70 %, Verkäuferdarlehen 10–30 %).

**Ich empfehle es trotzdem nicht als Einstieg** — weil es Nicos Anti-Liste am
härtesten verletzt (60–100 Mitarbeiter, mehrere Standorte, Personalführung als
Kerngeschäft), einen COO ab Tag 1 zwingend voraussetzt und der zweite Zukauf ohne
einen erfolgreich integrierten ersten reines Glücksspiel ist. Es gehört aber als
**Zielbild ab Jahr 4** in die Planung, nicht als vergessene Option. Und es
verändert die Bewertung des ersten Kaufs: Man kauft dann nicht irgendeinen
Betrieb, sondern den ersten von fünf — mit entsprechenden Anforderungen an
Nische, Prozessähnlichkeit und Übertragbarkeit.

### 8.2 Die Empfehlung

**(b), aber mit einem harten Entscheidungspunkt nach 90 Tagen — und (a) als
benannter Rückfallpfad, nicht als Trostpreis.**

Warum nicht (a) allein: Ein gesenktes Ziel macht ein unbelegtes Modell nicht
belegter. Das Kernproblem der sechs Topmodelle ist nicht die Zielhöhe, sondern
dass in **vier von sechs Fällen eine einzige Suche den Burggraben gerissen hat**
und dass in **keinem** Fall die Zahlungsbereitschaft für die eigentliche
Leistungsschicht belegt ist. Das ändert sich nicht, wenn man die Latte tiefer
hängt.

Warum (b): Es kauft exakt die drei Dinge, die allen sechs Modellen fehlen und die
durch keine weitere Recherchewelle entstehen können — **Cashflow ab Monat 1,
Referenz und Zutritt, eine Kundenliste mit gesetzlichen Fälligkeiten**. Und es ist
das einzige Konstrukt, in dem Nicos Verkaufsstärke sofort auf echte Kunden trifft
statt auf eine Landingpage.

**Konkret, die nächsten 90 Tage — zwei Spuren parallel:**

**Spur 1 (kostet Zeit, kein Geld): Der Feldtest.** Nico terminiert mit CallSuite
plus Voice-Layer für **einen echten Prüfbetrieb** 200 Bestandskunden gegen
Erfolgshonorar. Das liefert drei Dinge auf einmal:
- harte Zahlen (Erreichbarkeit, Kosten je Termin, Effekt der KI-Transparenzansage
  auf die Abschlussquote) — die Messung 4 aus Abschnitt 4
- ersten Umsatz
- **Deal-Sourcing**: Der Inhaber, für den er terminiert, ist entweder selbst
  Kaufkandidat, kennt einen, oder wird der erste Overlay-Kunde. Ein
  Betriebsinhaber, der gesehen hat, dass Nico ihm Termine bringt, ist der beste
  denkbare Türöffner in eine Branche, in die man sonst nicht hineinkommt.

**Spur 2 (kostet wenig Geld): Das Suchprofil.** nexxt-change und 2–3
M&A-Vermittler mit einem scharfen Profil bespielen (Prüf-/Wartungsbetrieb,
6–15 Mitarbeiter, ≥ 80 Gewerbekunden mit 50–500 MA, gesetzlich getaktete
Wiederkehr, **angestellter Meister vorhanden**, Verkäufer bereit zu 24 Monaten
Übergabe mit Verkäuferdarlehen). Parallel die Messungen 1, 3 und 6 aus
Abschnitt 4.

**Entscheidung nach 90 Tagen:**

| Spur 1 | Spur 2 | Entscheidung |
|---|---|---|
| funktioniert | ≥ 3 passende Kandidaten | **(b)** — Kauf verfolgen, Overlay als Phase 2 |
| funktioniert | keine Kandidaten | **(a)** — S01-Overlay greenfield, gestartet aus den Kontakten aus Spur 1, Ziel auf 110–130 k €/Monat Umsatz gesenkt |
| funktioniert nicht | egal | **Stopp und Neubewertung** — dann ist das Voice-Asset kein Asset, und die halbe Bewertungslogik dieses Projekts steht auf Sand |

Und in jedem Fall, unabhängig vom Ausgang: **die Steuerberater-Stunde aus
Angriff 5.** Entnahme- gegen Thesaurierungsszenario. Sie kann das Zielniveau um
40 % senken, ohne dass Nico auf irgendetwas verzichtet, und ist damit der
billigste Hebel im gesamten Projekt.

### 8.3 Die Bedingung, unter der meine Empfehlung falsch ist

Drei Falsifikationsbedingungen, nach Wahrscheinlichkeit geordnet:

**1. (wahrscheinlichste) Nicos „bereit, operativ zu arbeiten" schließt
Personalführung nicht ein.** Wenn er nach 9 Monaten als Inhaber eines
12-Mann-Betriebs mit Krankmeldungen, Lohnabrechnung und Kundenreklamationen
erschöpft und desinteressiert ist, ist (b) falsch — unabhängig davon, wie gut die
Rechnung aussieht. **Ein analytisch schwächeres Modell, das er durchhält, schlägt
jedes stärkere, das er nicht durchhält.** Dann ist (a) richtig, auch wenn (a) das
Ziel verfehlt. Diese Frage kann kein Research-Agent beantworten, nur Nico selbst
— und er sollte sie beantworten, **bevor** eine Due Diligence Geld kostet. Der
ehrlichste Test dafür ist billig: zwei Tage bei einem befreundeten Betriebsinhaber
mitlaufen, an einem normalen Dienstag.

**2. Kapital ist verfügbar oder aufnehmbar.** Die gesamte Analyse arbeitet unter
Annahme A10 („kein VC"). Mit 1–2 Mio. € Eigenkapital ist meine Empfehlung zu
kleinteilig — dann ist (c′) der Buy-and-Build von Anfang an überlegen, weil er
als einziger die Nordstern-Zahl tatsächlich erreicht und weil bei diesem
Kapitaleinsatz ein COO ab Tag 1 finanzierbar ist.

**3. Der Feldtest scheitert an der KI-Transparenzpflicht.** Wenn die Ansage
„Sie sprechen mit einem KI-Assistenten" die Abschlussquote um mehr als ein
Drittel senkt, fällt der Kostenvorteil weg, der die ganze Kombination
zusammenhält. Dann reduziert sich (b) auf „Nico kauft einen Handwerksbetrieb" —
ein solides Mittelstandsleben, aber kein Maschine-A-Pfad. Das ist die einzige der
drei Bedingungen, die in 30 Tagen messbar ist, und deshalb steht sie an erster
Stelle des Programms.

### 8.4 Nachtrag zur Annahmenliste aus Abschnitt 2

Aus dem S08-Kontrollversuch folgt eine vierte riskante Annahme, jetzt belegt:

**Annahme 4 — „Die Bewertungsmatrix misst Modellqualität."**
Sie misst teilweise Rechercheintensität. S08 hatte grüne Ampeln, weil es
unbeschossen war; sechs Suchen haben Marge, Regulatorik, Persönlichkeits-Fit und
Wettbewerbslage gleichzeitig nach unten korrigiert. Solange nicht **jedes**
Shortlist-Modell mit vergleichbarer Härte geprüft ist, ist jeder Vergleich
zwischen ihnen ungültig. Praktische Konsequenz für Welle 3: **kein Ranking
veröffentlichen, bevor S06, S07, S09–S12 und S14–S16 dieselbe Behandlung
bekommen haben** — oder das Ranking ausdrücklich auf die geprüften Modelle
beschränken.

---

## Quellen Nachtrag (alle [F-sek], Suchsynthese)

- [Testo Saveris 2 – Lebensmittelmärkte](https://www.testo.com/de-CH/anwendungen/food-supermarkets-saveris-2) · [Testo Saveris Food Safety](https://www.testo.com/de-DE/saveris/food/foodsafety) · [Testo Lebensmitteleinzelhandel](https://www.testo.com/de-AT/solutions/lebensmitteleinzelhandel)
- [Danfoss – Monitoring & Management Supermärkte (Alsense)](https://www.danfoss.com/en/markets/food-and-beverage/dcs/monitoring-and-management/) · [Danfoss Food Retail](https://www.danfoss.com/en-us/markets/food-and-beverage/dcs/food-retail/)
- [Wurm – HACCP-konformes Temperaturmonitoring (PDF)](https://www.wurm.de/sites/default/files/public/download/Flyer_HACCP_0.pdf)
- [TEMPASCAN – HACCP-Preise ab 39 €/Monat inkl. Hardware](https://tempascan.com/wissenswertes/temperaturueberwachung-haccp-preise-ab-39-e-monatlich-inklusive-hardware/) · [Sencono](https://www.sencono.de/) · [COMOTIX Lebensmittel/Gastro](https://www.comotix.com/de/anwendungen/temperaturueberwachung/lebensmittel-gastronomie-haccp-12487152/)
- [Anticimex SMART Connect](https://www.anticimex.de/smart/smart-connect/) · [Anticimex SMART Lebensmittelindustrie](https://www.anticimex.de/schaedlingsbekaempfung/lebensmittelindustrie/smart-pest-control/)
- [Pallax – LoRaWAN-Sensoren Preisguide](https://pallax.io/blog/lorawan-sensoren-der-ultimative-guide-fuer-typen-anwendungsfaelle-und-auswahl/) · [m2mGermany LoRaWAN-Sensoren](https://www.m2mgermany.de/shop/produkte/lorawan-sensoren/)
