# Agent 10 – Geschäftsmodell-Kopier- und Verbesserungs-Scout

Stand: 2026-08-05 · Auftraggeber: Nico Grunwald · Arbeitsgrundlage: `01_nordstern_und_anforderungen.md`

**Auftrag:** Bewährte Geschäftsmodelle finden, die nicht neu erfunden, sondern nur besser
gemacht werden müssen. Nachfrage bewiesen, Anbieter veraltet, Kundenerfahrung schlecht,
Lösungen unvollständig, Inhaber-Nachfolgeproblem.

---

## 0. Methoden- und Transparenzhinweis (bitte zuerst lesen)

- **Zahlenkennzeichnung** nach Vorgabe: **[F]** Fakt aus benannter Quelle · **[S]** Schätzung
  mit offengelegtem Rechenweg · **[A]** Annahme, unsicher.
- **Recherche-Einschränkung, die offengelegt werden muss:** Es wurden **22 WebSearch-Anfragen**
  durchgeführt (Ziel waren ≥25). Danach war das **sessionweite Websuch-Budget von 200 Anfragen
  erschöpft** (geteilt über alle parallel laufenden Research-Agenten). Zusätzlich blockierte
  der Agent-Proxy ab diesem Zeitpunkt auch WebFetch-Verbindungen zu externen Hosts
  (`gateway answered 403 to CONNECT` u. a. für ebuero.de, trustpilot.com, omr.com,
  nexxt-change.org, certado.io, exit-coach.de).
- **Konsequenz für die Qualitätskontrolle:** Alle mit **[F]** markierten Zahlen stammen aus den
  22 tatsächlich durchgeführten Suchen und sind mit Quelle benannt. Alles, was ich nicht
  verifizieren konnte, ist konsequent **[A]** – auch dort, wo ich aus Branchenkenntnis eine
  plausible Zahl nennen könnte. **Jedes [A] in diesem Dokument ist ein offener Rechercheauftrag**,
  kein Beleg. Vor einer Investitionsentscheidung sind mindestens die [A]-Zahlen der Top-8-Modelle
  nachzurecherchieren.
- **Nicht belegte Belegkategorien:** Der Auftrag verlangte „BELEGE: Bewertungen, veraltete
  Websites, Preisintransparenz, Wartezeiten". Bewertungsportale (Trustpilot, OMR, Capterra)
  waren durch Proxy-Policy nicht direkt abrufbar. Wo Bewertungsinhalte auftauchen, stammen sie
  aus **Suchergebnis-Zusammenfassungen**, nicht aus dem Original – das ist jeweils gekennzeichnet
  und ist **Evidenzstufe 2**, nicht Stufe 1.

---

## 1. Die Kernthese dieses Agenten in vier Sätzen

1. In Deutschland existiert ein sehr großes, gesetzlich erzwungenes Ausgabenfeld
   („wiederkehrende Prüf-, Wartungs- und Nachweispflichten"), in dem der Kunde **nicht wählen
   kann, ob er zahlt** – nur bei wem.
2. Die Anbieterlandschaft dort ist extrem fragmentiert, technisch rückständig und
   preisintransparent – genau das Profil, das der Auftrag sucht.
3. Der eigentliche Kundenschmerz ist **nicht die Prüfung selbst**, sondern die **Koordination**
   (wer prüft was, wann, mit welchem Nachweis, wo liegt das Protokoll, wer erinnert mich) –
   und genau diese Koordination verkauft heute fast niemand als eigenständiges Produkt.
4. Die Kombination **„gesetzliche Prüfpflicht + Software + KI-Terminierung"** existiert in
   Teilen, aber **nicht als integriertes Kundenprodukt** – die Marktlücke ist real
   (Detailanalyse in Abschnitt 3).

---

## 2. Der Bewertungsfilter, den ich angelegt habe

Jedes Modell wurde gegen Nicos harte K.-o.-Kriterien geprüft. Zwei davon sind für dieses
Themenfeld besonders scharf:

| K.-o. | Bedeutung für Prüf-/Wartungsmodelle |
|---|---|
| **#3 stark reguliert als Kern** | Wer die Prüfung **selbst** erbringt, braucht „befähigte Personen" nach TRBS 1203, teils VdS-/ZÜS-Anerkennung. Das ist **keine BaFin-Erlaubnis**, aber es ist Qualifikationszwang mit Haftung. → Modelle, in denen Nicos Firma **koordiniert und dokumentiert** statt selbst prüft, sind strukturell besser. |
| **#10 ungeliebte Tätigkeiten als Kern** | Nicos Anti-Liste enthält wörtlich „Unterlagen prüfen, Dokumente sortieren" und „Fristen und Einzelfälle verwalten". **Das ist exakt der Inhalt eines Prüffristen-Geschäfts.** → Solche Modelle sind nur zulässig, wenn Fristenverwaltung **Softwarefunktion** ist, die der Kunde bzw. das System erledigt – nicht Handarbeit im Backoffice. Dieser Punkt ist der wichtigste Filter des gesamten Dokuments und wird bei jedem Modell unter Punkt 9 „Delegierbarkeit" bewertet. |

**Regulatorik-Ampel-Legende:**
- 🟢 **Grün** – keine Erlaubnis nötig, Haftung vertraglich begrenzbar
- 🟡 **Gelb** – Qualifikationsnachweise/Zertifizierungen für Mitarbeiter nötig, Haftung real aber versicherbar
- 🔴 **Rot** – Zulassung/Akkreditierung als Geschäftsvoraussetzung → nach Nicos K.-o. #3 auszuschließen oder nur als Partnerleistung zulässig

---

## 3. SONDERPRÜFUNG: „Gesetzliche Prüfpflicht + Software + KI-Terminierung" – gibt es das schon?

Der Auftrag verlangt eine explizite Antwort. Hier ist sie.

### 3.1 Was heute existiert – drei getrennte Lager

**Lager A – Prüffristen-/Wartungssoftware (alt, on-premise-geprägt, verwalterzentriert)**

| Anbieter | URL | Beobachtung |
|---|---|---|
| HOPPE „Wartungsplaner" / „Prüfplaner" | wartungsplaner.de, hoppe-net.de | Seit Jahrzehnten am Markt, klassische Windows-Software-Anmutung, Produktseiten im Stil der frühen 2000er [F: eigene Sichtung der Suchergebnis-Titel/Snippets „Software 195 Behalten Sie Ihre Prüfungen im Griff", 2026-08-05] |
| RISK-Project „SERVO" | risk-project.de | Arbeitsmittel-/Prüfwesen-Modul innerhalb einer EHS-Suite |
| Fraunhofer IFF „ELISA" | iff.fraunhofer.de | Client-Server-Lösung, papierlose Prüfdokumentation, Forschungsherkunft |
| mybuilding24 | mybuilding24.com | Betreiberpflichten-Plattform, betreibt selbst Vergleichsinhalte („Software für Prüfpflichten im Vergleich") |
| Cloudbrixx | cloudbrixx.de | Immobilien-/FM-Plattform, publiziert RWA-Prüfpflicht-Content |
| Planon | planonsoftware.com | Großer internationaler CAFM-/FM-Anbieter, Enterprise-Preisklasse |

**Charakteristik Lager A:** Verwaltet **Fristen**. Verkauft an den **Betreiber**. Löst
Dokumentation. **Löst nicht**, wer die Prüfung tatsächlich durchführt und wann der Termin steht.

**Lager B – ERP/Field-Service-Software für Prüfdienstleister (Anbieterseite)**

| Anbieter | URL | Funktionsumfang laut eigener Darstellung |
|---|---|---|
| Certado Suite | certado.io | „erstellt DGUV-konforme Protokolle automatisch", „mobile Prüfungen direkt beim Kunden ohne Zettelwirtschaft", „zeigt automatisch, welcher Kunde wann fällig ist", „überwacht Prüffristen automatisch mit automatisch versandten Erinnerungen" [F: Suchergebnis-Snippet certado.io, 2026-08-05] |
| Vemas (MS Consulting) | msconsulting.de/branchenloesungen/pruefdienstleister | „optimiert Termine, Touren und Ressourcen automatisch", Echtzeit-Einsatzsteuerung für Techniker [F: Suchergebnis-Snippet, 2026-08-05] |
| firstaudit | firstaudit.de | „Digitale Prüfprotokolle – KI-Software für mehr Rechtssicherheit" [F: Suchergebnis-Titel, 2026-08-05] |

**Charakteristik Lager B:** Verkauft an den **Prüfdienstleister**, nicht an den Endkunden. Hat
bereits Fälligkeits-Erinnerung und Tourenoptimierung. **Hat keinen KI-Sprachkanal** und
verkauft keine Terminvereinbarung als Leistung.

**Lager C – KI-Telefonassistenten (neu, branchenoffen, inbound-fokussiert)**

| Anbieter | URL | Beobachtung |
|---|---|---|
| HalloPetra GmbH (Berlin) | hallopetra.de | Spezialisiert auf Handwerk **SHK, Elektro, Kälte/Klima**; „über 1.000 Betriebe nutzen nach eigenen Angaben Petra" [F: Suchergebnis-Zusammenfassung, 2026-08-05 – Anbieterangabe, nicht unabhängig geprüft] |
| PORTA | – | „ausschließlich Handwerksbetriebe wie Elektriker, Maler, Tischler", legt Anrufinfos automatisch in Datenbank ab [F: Suchergebnis-Zusammenfassung] |
| voiceOne (OneAI UG, Bamberg) | – | KMU mit hohem Telefonaufkommen, Terminbuchung direkt im Kalender [F: Suchergebnis-Zusammenfassung] |
| Vokaro | vokaro.net | Handwerks-Templates mit Notfall-Erkennung, automatischer Terminbuchung, Branchen-FAQ [F: Suchergebnis-Zusammenfassung] |
| ruflab | ruflab.com | Publiziert „KI-Telefonassistent Made in Germany: Vergleich 2026" – d. h. Markt ist bereits vergleichsreif [F] |

**Charakteristik Lager C:** **Inbound.** Nimmt Anrufe an, die ohnehin kommen. **Kein Anbieter
in den Ergebnissen macht systematisch Outbound-Terminierung gegen eine Fälligkeitsliste.**

### 3.2 Die Antwort auf die Auftragsfrage

**Nein – die Dreier-Kombination existiert nicht als integriertes Produkt.**

Was existiert:
- Prüfpflicht + Software → **ja, gut abgedeckt** (Lager A und B, teils seit 20+ Jahren)
- Software + KI-Telefonie → **ja, entstehend** (Lager C, aber inbound und branchenoffen)
- Prüfpflicht + KI-**Outbound**-Terminierung → **hier ist die Lücke** [S: abgeleitet aus dem
  Fehlen jedes entsprechenden Anbieters in 3 gezielten Suchen zu Prüfsoftware, Prüfdienstleister-
  Software und KI-Telefonassistenten, 2026-08-05. Negativbefund aus 3 Suchen ist ein **schwacher
  Beleg** – vor einer Entscheidung mit mind. 10 weiteren Suchen zu härten.]

**Warum die Lücke ökonomisch sinnvoll ist – und warum sie trotzdem offen ist:**

Der Engpass eines Prüfdienstleisters ist nicht das Prüfen. Es ist, dass er
- eine Kundenliste mit Fälligkeiten hat (die Software kennt sie – siehe Certado-Zitat oben),
- aber niemanden, der 400 Kunden anruft und Termine so legt, dass die Tour dicht ist.

Die heutige Lösung ist **eine Bürokraft, die telefoniert** – oder eine E-Mail-Erinnerung, die
zu 70–85 % ignoriert wird [A: nicht belegt, Erfahrungswert-Bandbreite, **muss geprüft werden**].
Genau dieser Schritt – Fälligkeit → Anruf → bestätigter Termin im Techniker-Kalender – ist
- vollständig standardisierbar,
- sprachlich simpel (ein Terminvorschlag, zwei Alternativen, Bestätigung),
- und **exakt das, was Nicos vorhandener Twilio-/CallSuite-Stack technisch schon kann**
  (`api/call.js`, `api/twilio-token.js`, deutsche Rufnummer produktiv, `cs_listen` als
  Listenmodell, `cs_arbeitszeit` als KPI-Tracking – Beleg: Nordstern-Dokument Abschnitt 4).

**Warum es trotzdem niemand macht (ehrliche Gegenrede):**
- Der Prüfdienstleistermarkt ist kleinteilig und schwer zu erreichen; Software-Vertrieb dorthin
  ist teuer [A].
- Die vorhandenen ERP-Anbieter (Certado, Vemas) können die Funktion **nachbauen** – sie sitzen
  bereits auf den Fälligkeitsdaten. Das ist das größte Wettbewerbsrisiko dieses Modells.
- Sprach-KI auf Deutsch mit Terminlogik war bis vor ~2 Jahren nicht zuverlässig genug [A].

**Bewertung:** Die Lücke ist real, aber **kein Burggraben aus Technik** – der Burggraben müsste
aus Vertriebsgeschwindigkeit, Datenzugang und Vertragsbindung kommen. Das ist in Abschnitt 4
bei Modell 12 durchgerechnet.

---

## 4. Die Modelle

Format je Modell: 10 Pflichtpunkte laut Auftrag.

---

### Modell 1 – Prüfpflicht-Betriebssystem für Gewerbeimmobilien („Compliance-Cockpit als Abo")

**1. Modellname + realer Anbieter + URL**
Betreiberpflichten-Management als SaaS. Reale Anbieter: mybuilding24 (mybuilding24.com),
Cloudbrixx (cloudbrixx.de), Planon (planonsoftware.com), HOPPE Wartungsplaner
(wartungsplaner.de), Fraunhofer ELISA (iff.fraunhofer.de).

**2. Beweis der Nachfrage**
- GEFMA 190 „Betreiberverantwortung 2.0 im Facility Management" wurde neu aufgelegt und ist
  „das Standardwerk für Eigentümer und Betreiber von baulichen Anlagen in Deutschland" [F:
  gefma.de / facility-management.de, abgerufen 2026-08-05].
- Kernaussage der Richtlinie: Betreiberpflichten sind delegierbar, **die Haftung bleibt beim
  Betreiber** [F: gefma.de-Zusammenfassung]. Das erzeugt strukturelle Zahlungsbereitschaft für
  Nachweisführung.
- Mindestens 6 Anbieter mit eigenständigen Produkten in diesem Segment allein aus einer
  einzigen Suchabfrage → Markt ist bewiesen besetzt [F].
- Marktvolumen Deutschland: **[A] nicht ermittelt.** Offener Rechercheauftrag.

**3. Was ist heute schlecht? (Belege)**
- Produktsprache und Seitenaufbau der etablierten Anbieter sind erkennbar aus der
  Vor-Cloud-Ära (HOPPE-Seitentitel: „Prüfmanager erinnert Sie an die Prüftermine. Software 195
  Behalten Sie Ihre Prüfungen im Griff." – ein Seitentitel dieser Form ist ein Indikator für
  nicht überarbeitete Legacy-Webpräsenz) [F: Suchergebnis-Titel, 2026-08-05].
- **Keine öffentlichen Preise** bei den gesichteten Prüfmanagement-Anbietern. Preisintransparenz
  ist in diesem Segment die Regel [F: keine der 6 gesichteten Anbieterseiten führte in den
  Suchergebnissen einen Preis].
- Die Kategorie erzeugt eigenen Vergleichsjournalismus („Software für Prüfpflichten im
  Vergleich", „Beste Software für Betreiberpflichten finden" – beides von mybuilding24 selbst)
  [F] → Zeichen für Unübersichtlichkeit und Kaufunsicherheit.
- Strukturelle Unvollständigkeit: Die Software sagt dem Kunden, **dass** etwas fällig ist. Sie
  besorgt ihm **nicht** den Prüfer. Der Kunde braucht danach weiterhin 3–8 Einzeldienstleister.

**4. Was übernehmen wir?**
Das Kernversprechen „lückenloser Nachweis der Betreiberpflichten, gerichtsfest dokumentiert" und
die Objekt-/Anlagen-/Fristen-Datenstruktur. Das ist erprobt, funktioniert und muss nicht neu
erfunden werden.

**5. Was verbessern wir?**
- Öffentliche, gestaffelte Preisliste (pro Objekt/pro Anlage) – bricht mit der Branchennorm.
- Onboarding als Produkt: Anlagen-Erstaufnahme vor Ort in 1 Tag statt monatelanger Datenpflege
  durch den Kunden. Das ist der eigentliche Grund, warum solche Systeme scheitern [A].
- Mobil-first Prüfprotokoll mit Foto/Zeitstempel statt PDF-Ablage.

**6. Was kombinieren wir neu?**
Software **plus** Beschaffung der Prüfleistung: Das System kennt die Fälligkeit, beauftragt aus
einem kuratierten Partnerpool, terminiert automatisch, holt das Protokoll ab und legt es ab.
Der Kunde bekommt **eine Rechnung** statt acht.

**7. Warum wechselt ein Kunde zu uns? (konkreter Wechselgrund)**
Nicht „bessere Software". Sondern: *„Sie zahlen heute für ein Programm, das Ihnen sagt, dass
Ihr Rolltor fällig ist – und rufen den Prüfer trotzdem selbst an. Bei uns steht der Termin im
Kalender, ohne dass Sie etwas tun. Wenn kein Prüfer kommt, ist das unser Problem, nicht Ihres."*
Der Wechselgrund ist **Arbeitswegfall beim Objektverwalter**, messbar in Stunden/Monat.

**8. Wiederkehrender Umsatz: woher genau**
Monatliche Objektgebühr (Grundgebühr je Liegenschaft) + Staffel je erfasster prüfpflichtiger
Anlage. Zusätzlich Marge auf die vermittelte Prüfleistung. Vertragslaufzeit 24–36 Monate ist in
diesem Segment marktüblich [A].

**9. Delegierbarkeit**
**Kritisch – hier liegt Nicos K.-o. #10.** Die Leistung ist im Kern Fristenverwaltung. Das darf
**niemals Handarbeit** sein, sonst ist es genau die Tätigkeit, die Nico dauerhaft ablehnt. Nur
zulässig, wenn Fristenlogik zu ≥95 % Software ist und Menschen nur Ausnahmen bearbeiten.
Ergebnis dann: sehr gut delegierbar (Ops-Team + Partnernetz).

**10. Regulatorik-Ampel**
🟢 **Grün** – solange die eigentliche Prüfung durch qualifizierte Partner erfolgt. Haftungsrisiko
liegt in der Nachweisführung; über Vertragsgestaltung (Vermittlung statt Erfüllung) und
Vermögensschadenhaftpflicht beherrschbar. **Wird 🟡, sobald wir eigene Prüfer beschäftigen.**

---

### Modell 2 – DGUV-V3-Elektroprüfung als Abo statt als Einzelauftrag

**1. Modellname + realer Anbieter + URL**
Wiederkehrende Prüfung ortsveränderlicher/ortsfester elektrischer Betriebsmittel nach
DGUV Vorschrift 3. Anbieter: GP Prüfservice (gp-pruefservice.de), Deutscher Prüfservice /
DGUV-V3.GmbH (deutscher-pruefservice.de), ESG (esg-gesellschaft.de), KFK Konrad
(pruefservice-kfk.de), Piepenbrock (piepenbrock.de), Deutscher Prüfdienst
(deutscher-pruefdienst.de), elektropruefung.guru, elektropruefungen.info.

**2. Beweis der Nachfrage**
- Gesetzliche Wiederkehrpflicht: DGUV V3 (vormals BGV A3) verpflichtet **alle** Unternehmen mit
  elektrischen Betriebsmitteln zur wiederkehrenden Prüfung [F: mehrere Anbieterquellen,
  2026-08-05].
- Anbieterdichte als Nachfragebeweis: Allein eine Suche brachte **8 verschiedene bundesweite
  Anbieter** – darunter KFK Konrad mit „rund 100 Mitarbeitern deutschlandweit" und ESG mit
  „über 2.000 betreuten Unternehmen in über 20 Jahren" [F: Anbieterangaben, 2026-08-05].
- Marktvolumen: **[A] nicht ermittelt** – die Suche nach Marktgröße/Umsatz lieferte
  ausdrücklich keine Zahlen. Offener Rechercheauftrag.

**3. Was ist heute schlecht?**
- Domains wie `elektropruefung.guru` und `elektropruefungen.info` signalisieren
  SEO-getriebene Kleinanbieter ohne Markenaufbau [F: Domainnamen aus Suchergebnis].
- Preise werden weit überwiegend nur „auf Anfrage" genannt; wo Preise existieren, sind sie
  Stückpreise pro Gerät, die der Kunde nicht in Jahreskosten übersetzen kann [F: nur eine der
  gesichteten Seiten führte überhaupt eine Preisseite].
- Das Produkt ist **transaktional**: Der Prüfer kommt, prüft, geht, schickt PDF. Im Folgejahr
  muss der Kunde daran denken. Der Anbieter verliert den Kunden regelmäßig an den nächsten
  Billiganbieter, weil nichts bindet.
- Der Kunde braucht typischerweise **mehrere Anbieter parallel** (Elektro, Leitern, Regale,
  Tore, Feuerlöscher) – jeder mit eigener Rechnung, eigenem Portal, eigenem PDF-Format.

**4. Was übernehmen wir?**
Die Prüfleistung selbst inkl. Prüfplakette und Protokoll – ein vollständig standardisierter,
geschulter Arbeitsablauf, der sich in 4–8 Wochen an neue Mitarbeiter übertragen lässt [A].

**5. Was verbessern wir?**
- **Festpreis-Abo pro Standort und Monat** statt Stückpreis pro Gerät. Der Kunde kann budgetieren.
- Prüfergebnisse live im Kundenportal, nicht als PDF-Anhang.
- Automatische Wiedervorlage im Folgejahr **ohne Zutun des Kunden** – Terminvorschlag kommt
  von uns.

**6. Was kombinieren wir neu?**
DGUV V3 als **Anker** für ein Bündel: Elektro + Leitern/Tritte + Regale (DIN EN 15635) +
Tore (ASR A1.7) + Feuerlöscher – alles in einem Vertrag, einem Portal, einer Rechnung, möglichst
an **einem** Vor-Ort-Tag. Genau diese Bündelung fehlt heute (siehe Modelle 3, 4, 5).

**7. Warum wechselt ein Kunde zu uns?**
*„Sie haben für Elektro, Regale, Tore und Feuerlöscher vier Firmen, vier Termine, vier
Rechnungen und vier Aktenordner. Wir machen das an einem Tag im Jahr, zu einem Monatspreis, und
Sie sehen jederzeit online, was geprüft ist und was ansteht. Wenn die Berufsgenossenschaft
fragt, drucken Sie einen Bericht."*
Der Wechselgrund ist **Reduktion von vier Lieferanten auf einen** – nicht der Preis.

**8. Wiederkehrender Umsatz: woher genau**
Monatliches Prüf-Abo je Standort (Preis nach Gerätezahl/Fläche gestaffelt), 24–36 Monate
Laufzeit mit automatischer Verlängerung. Zusatzumsatz: Mängelbeseitigung, Nachprüfungen,
Neugeräte-Ersterfassung.

**9. Delegierbarkeit**
**Hoch.** Prüfer sind angestellte Techniker mit definiertem Tagesablauf; Disposition ist
Software. Nico ist nach der Aufbauphase in Vertrieb/Produkt, nicht in der Leistung.
Einschränkung: Rekrutierung qualifizierter Elektrofachkräfte ist der reale Engpass [A].

**10. Regulatorik-Ampel**
🟡 **Gelb** – keine Erlaubnispflicht, aber die Prüfung darf nur durch Elektrofachkräfte bzw.
„befähigte Personen" nach TRBS 1203 erfolgen. Haftung bei Fehlprüfung ist real (Personenschaden),
aber über Betriebs-/Vermögensschadenhaftpflicht versicherbar. **Kein K.-o. nach Nicos Kriterium
#3**, da keine staatliche Zulassung des Unternehmens erforderlich ist – aber deutlich näher an
der Grenze als ein reines Softwaremodell.

---

### Modell 3 – Regalprüfung / Lagersicherheit nach DIN EN 15635

**1. Modellname + realer Anbieter + URL**
Jährliche Regalinspektion. Anbieter: 123ingenieure (123ingenieure.de/regalpruefung/),
regalprofi24 (regalprofi24.de), Bonnema (bonnema.de), SW-Direkt (swdirekt.de),
arbeitssicherheit-fachkraft.de, arbeitssicherheit.gmbh, fachkraft-arbeitssicherheit.com.

**2. Beweis der Nachfrage**
- Pflicht: Betreiber müssen Lagereinrichtungen „in Zeitabständen von höchstens 12 Monaten" durch
  eine befähigte Person prüfen lassen (BetrSichV i. V. m. DIN EN 15635, DGUV 208-061) [F:
  mehrere Anbieterquellen, 2026-08-05].
- **Belegte Preise** (selten in dieser Branche!): 2,50–7,00 € pro laufendem Meter im Schnitt;
  Einstiegsangebote ab 2,49 €/lfm; Bonnema ab 2,00 € pro Regalfeld [F: Anbieterangaben,
  2026-08-05].
- Betroffen ist jedes Lager mit Palettenregalen – Logistik, Produktion, Handel, Handwerk.
  Anzahl betroffener Betriebe in DE: **[A] nicht ermittelt.**

**3. Was ist heute schlecht?**
- Der Markt ist ein **Preis-pro-Meter-Wettbewerb** – „sofort günstig!" steht wörtlich im
  Seitentitel eines Anbieters („Regalprüfung nach DIN EN 15635 und DGUV sofort günstig!")
  [F: Suchergebnis-Titel]. Das ist nach Nicos K.-o. #6 („gewinnt nur über niedrige Preise")
  eine **Warnung**, wenn man das Modell 1:1 kopiert.
- Mehrere Anbieter sind erkennbar Nebenprodukt einer Arbeitssicherheits-Beratung
  (arbeitssicherheit-fachkraft.de, fachkraft-arbeitssicherheit.com, arbeitssicherheit.gmbh –
  drei fast identische Domains, vermutlich derselben Gruppe) [F: Domainmuster].
- Preis „auf Anfrage" bei einem der größeren Anbieter (SW-Direkt) trotz existierender
  Marktpreise [F].

**4. Was übernehmen wir?**
Die Prüfsystematik (Schadenskategorien grün/gelb/rot nach DIN EN 15635) und die
Regalprüfer-Qualifikation.

**5. Was verbessern wir?**
- Weg vom Meterpreis: Verkauf als **Standortpauschale im Jahres-Abo**, inklusive der
  gesetzlich ebenfalls geforderten wöchentlichen Sichtkontrolle durch den „Regalverantwortlichen"
  (den wir schulen und mit einer App ausstatten).
- Sofortiger digitaler Mängelbericht mit Foto und Reparaturangebot am selben Tag.

**6. Was kombinieren wir neu?**
Regalprüfung + Reparaturteile-Lieferung + Schulung des internen Regalverantwortlichen +
Sichtkontroll-App. Der Mangelbefund erzeugt direkt Folgeumsatz (Traversenschutz, Anfahrschutz,
Ersatzstützen) – heute ein separater Handelsvorgang.

**7. Warum wechselt ein Kunde zu uns?**
*„Ihr aktueller Prüfer schreibt Ihnen 40 rote Mängel auf und fährt weg. Sie müssen dann selbst
Teile bestellen, Monteure suchen und die Nachkontrolle organisieren. Wir liefern den Mangel
inklusive Behebung und Nachweis – und Ihre wöchentliche Sichtkontrolle läuft über eine App, die
Ihr Lagerleiter in zwei Minuten erledigt."*
Wechselgrund: **Der Mangelbericht ist heute ein Problem, das der Kunde erbt. Bei uns ist er
erledigt.**

**8. Wiederkehrender Umsatz: woher genau**
Jahres-/Monatsabo Standortpauschale + Sichtkontroll-App-Lizenz + wiederkehrender Teileumsatz.

**9. Delegierbarkeit**
**Hoch.** Regalinspekteur ist eine Schulungsqualifikation, kein Studium. Sehr gut skalierbar
über angestellte Prüfer.

**10. Regulatorik-Ampel**
🟡 **Gelb** – befähigte Person nach DIN EN 15635/DGUV 208-061 erforderlich; Haftung bei
Regaleinsturz erheblich, aber versicherbar.

---

### Modell 4 – Tor-, Rolltor- und Türprüfung nach ASR A1.7

**1. Modellname + realer Anbieter + URL**
Jährliche Prüfung und Wartung kraftbetätigter Türen und Tore. Anbieter: PrüfAssist
(prüfassist.de), APS Prüfdienste (aps-pruefdienste.de), Kohlhauer Tore (kohlhauertore.de),
itore.de, Fox Tortechnik (fox-tortechnik.de), PROTEC-24 (protec-24.com), GWI (gwi-mbh.de).

**2. Beweis der Nachfrage**
- Pflicht: Rolltore, Sektionaltore, Schiebetore und andere kraftbetätigte Toranlagen müssen
  **mindestens einmal jährlich** durch eine befähigte Person geprüft werden [F: mehrere
  Anbieterquellen, 2026-08-05].
- Prüfer müssen nach TRBS 1203 qualifiziert sein [F].
- Betroffen: praktisch jede Halle, jeder Logistikstandort, jede Tiefgarage, jede Werkstatt.
  Anlagenzahl DE: **[A] nicht ermittelt.**

**3. Was ist heute schlecht?**
- Ein Anbieter betreibt noch eine **HTTP-Seite ohne TLS** mit URL-Struktur aus der Frühzeit des
  Web: `http://www.fox-tortechnik.de/info%20uvv%20pruefung%20und%20wartung%20bgr232,asr%20a1.htm`
  – Leerzeichen in Dateinamen, `.htm`-Endung, kein HTTPS [F: URL aus Suchergebnis, 2026-08-05].
  **Das ist der härteste einzelne Digitalisierungs-Beleg in diesem gesamten Dokument.**
- Die Anbieter sind fast durchweg **Tor-Errichter mit angehängtem Prüfservice**, nicht
  Prüfdienstleister. Die Prüfung ist für sie Beiwerk zum Anlagenverkauf → schlechte
  Terminverfügbarkeit, lange Wartezeiten [A – plausibel, aber nicht belegt].
- Keine Preistransparenz bei allen 7 gesichteten Anbietern [F].

**4. Was übernehmen wir?**
Prüfumfang und Prüfsystematik nach ASR A1.7 / DGUV / DIN EN 12635.

**5. Was verbessern wir?**
Reine Spezialisierung auf Prüfung + Kleinreparatur, unabhängig vom Torhersteller. Feste
Termin-Slots, Online-Buchung, Preisliste öffentlich.

**6. Was kombinieren wir neu?**
Tore sind ein idealer **Bündelpartner** zu DGUV V3 (Modell 2): Beide Prüfungen betreffen
denselben Standort, denselben Ansprechpartner, denselben Jahresrhythmus.

**7. Warum wechselt ein Kunde zu uns?**
*„Ihr Torbauer prüft Sie, wenn er gerade Zeit hat – meist im Herbst, meist mit vier Wochen
Vorlauf. Wir kommen zu einem festen Termin, den Sie im Januar für das ganze Jahr sehen, und
prüfen gleich Ihre Elektrik mit."*
Wechselgrund: **Terminsicherheit und Bündelung**, nicht Preis.

**8. Wiederkehrender Umsatz: woher genau**
Jahresvertrag je Toranlage, monatlich abgerechnet. Zusatz: Verschleißteile, Nachrüstung
Lichtschranken/Schließkantensicherung (häufigster Mangel) [A].

**9. Delegierbarkeit** Hoch – klar definierter Prüfablauf.

**10. Regulatorik-Ampel** 🟡 **Gelb** – befähigte Person nach TRBS 1203.

---

### Modell 5 – Brandschutz-Rundum-Abo (Feuerlöscher, RWA, Brandschutztüren, Unterweisung)

**1. Modellname + realer Anbieter + URL**
Brandschutz-Instandhaltung. Anbieter: Minimax Mobile (minimax-mobile.com), Jockel Brandschutz
(jockel-brandschutz.de), SFC Group (sfc-group.de), Maack Feuerschutz (maack-feuerschutz.de),
brandschutz-kundk.de, Herbach (herbach.de), Sela Brandschutz (sela-brandschutz.de),
Juschka (juschka-brandschutz.de), Indu-Light (indu-light.com). Verband: bvbf
(bvbf-brandschutz.de).

**2. Beweis der Nachfrage**
- Feuerlöscher: Prüfung nach DIN 14406-4 **mindestens alle 2 Jahre** durch einen Sachkundigen
  [F: mehrere Quellen, 2026-08-05].
- RWA-Anlagen: Wartung **mindestens jährlich** nach DIN 18232-2, VdS 2098 und Landesbauordnungen
  [F].
- **Belegte RWA-Preise:** 300 € (kleine Treppenhaus-RWA) bis 1.500 € (große Industrieanlage) pro
  Jahr; Batteriewechsel alle 3–4 Jahre zusätzlich 150–600 € [F: brandschutzfinder.de, 2026-08-05].
- Es existiert ein eigener Bundesverband der Brandschutz-Fachbetriebe (bvbf) → Branche ist groß
  genug für Verbandsstruktur [F].

**3. Was ist heute schlecht?**
- Extreme Fragmentierung: Die Suche lieferte fast ausschließlich **lokale Einzelbetriebe**
  („Feuerlöscher Wartung Hamburg", „Maack Feuerschutz – Hamburg") neben einem Konzern (Minimax)
  [F].
- **Klassisches Inhaber-Nachfolgeproblem:** Feuerlöscher-Wartungsbetriebe sind typische
  1–5-Personen-Familienbetriebe mit langjährigen Kundenlisten [A – plausibel aus dem
  Anbieterbild, nicht mit Altersstatistik belegt]. → Direkter Roll-up-Kandidat (siehe Modell 21).
- Preisintransparenz und Zusatzkosten-Praxis: Der Kunde bestellt eine „Wartung" und bekommt eine
  Rechnung mit Löschmittelaustausch, Ersatzteilen und Anfahrt, die das Doppelte des erwarteten
  Betrags ausmacht [A – häufige Klage, in dieser Recherche **nicht belegbar** gewesen; offener
  Rechercheauftrag: Bewertungsportale zu Feuerlöscherwartung auswerten].

**4. Was übernehmen wir?**
Die Wartungssystematik und den 2-Jahres-Rhythmus als Umsatzmotor.

**5. Was verbessern wir?**
- **All-inclusive-Monatspreis pro Löscher/Anlage** – Löschmittel, Ersatzteile, Anfahrt inklusive.
  Das beseitigt exakt den größten Ärgerpunkt der Branche.
- Digitale Standortkarte aller Löscher/RWA mit Fälligkeitsampel.

**6. Was kombinieren wir neu?**
Brandschutz-Hardware-Wartung + Brandschutzhelfer-/Brandschutzunterweisung als E-Learning
(Modell 15) + Flucht-/Rettungsplan-Aktualisierung. Heute drei getrennte Einkäufe.

**7. Warum wechselt ein Kunde zu uns?**
*„Sie haben letztes Jahr 340 € für die Wartung geplant und 780 € bezahlt, weil Löschmittel
fällig war. Bei uns zahlen Sie 9 € pro Löscher pro Monat – alles drin, auch der Austausch. Keine
Überraschungsrechnung mehr."* [Preis 9 €: **[A]** Illustration, nicht kalkuliert]
Wechselgrund: **Ende der Überraschungsrechnung.**

**8. Wiederkehrender Umsatz: woher genau**
Echtes Abo pro Gerät/Anlage. Das ist eines der saubersten MRR-Modelle in diesem Dokument, weil
das Asset physisch beim Kunden steht und gezählt werden kann.

**9. Delegierbarkeit** Hoch (Sachkundigen-Schulung), Disposition per Software.

**10. Regulatorik-Ampel**
🟡 **Gelb**, bei RWA tendenziell 🔴 **Rot-nah**: Minimax verweist darauf, dass es VdS-Anerkennung
als Errichter/Instandhalter für RWA gibt und „nur wenige Unternehmen am deutschen RWA-Markt eine
solche Qualität nachweisen" [F: minimax-mobile.com, 2026-08-05]. → RWA nur mit Partner oder nach
Zukauf eines anerkannten Betriebs. Feuerlöscher allein: 🟡.

---

### Modell 6 – Trinkwasser-/Legionellenprüfung als Verwaltungs-Abo

**1. Modellname + realer Anbieter + URL**
Legionellenuntersuchung nach TrinkwV. Anbieter: ista (ista.com), Techem (techem.com),
EAD Heizkostenabrechnung (ead-heizkostenabrechnung.de), Eurofins Umwelt (eurofins.de),
TÜV SÜD (tuvsud.com), legionellen-zentrum.de.

**2. Beweis der Nachfrage**
- Pflicht: Bei gewerblicher Vermietung bzw. Großanlagen zur Trinkwassererwärmung ist die
  Untersuchung **alle 3 Jahre** vorgeschrieben; betroffen sind u. a. Mehrfamilienhäuser mit mehr
  als zwei Wohneinheiten und gewerblich/öffentlich genutzte Warmwasseranlagen [F:
  Bundesgesundheitsministerium / TrinkwV, mehrere Anbieterquellen, 2026-08-05].
- Probenahme an **mindestens drei Stellen** je Gebäude; nur **akkreditierte** Labore dürfen
  untersuchen [F].
- Dass ista und Techem – zwei Milliarden-Konzerne der Heizkostenabrechnung – das als
  Standardprodukt führen, ist der stärkste Nachfragebeweis in diesem Dokument [F].

**3. Was ist heute schlecht?**
- Der Markt ist von den **Abrechnungskonzernen** besetzt, die Legionellenprüfung als
  Cross-Selling an ihre Zählerbestände verkaufen. Für kleine und mittlere Hausverwaltungen
  bedeutet das: Sie sind an ihren Abrechner gebunden und zahlen dessen Preis [A].
- Preise: **[A] nicht ermittelt** – keine der gesichteten Seiten nannte Preise.

**4. Was übernehmen wir?** Nichts an der Laborleistung (akkreditierungspflichtig).

**5. Was verbessern wir?** Die **Probenahme-Logistik**: Terminvereinbarung mit Mietern ist der
eigentliche Engpass (Zugang zu drei Entnahmestellen in bewohnten Einheiten).

**6. Was kombinieren wir neu?**
Probenahme-Koordination + Mieterterminierung per KI-Telefonie + Partnerlabor + Nachweisablage.

**7. Warum wechselt ein Kunde zu uns?**
*„Ihre Hausverwaltung verbrennt pro Objekt einen halben Tag damit, drei Mieter zu erreichen, die
zur Probenahme zuhause sein müssen. Wir übernehmen die Mieterterminierung komplett – Sie
bekommen nur noch den Befund."*
Wechselgrund: **Wegfall der Mieterterminierung** – ein echter, benennbarer Zeitfresser.

**8. Wiederkehrender Umsatz** Schwach: 3-Jahres-Zyklus. **Nur als Zusatzmodul** in einem
Immobilien-Compliance-Abo sinnvoll, nicht als eigenständiges Modell.

**9. Delegierbarkeit** Hoch.

**10. Regulatorik-Ampel** 🔴 **Rot für die Laborleistung** (Akkreditierungspflicht – nach Nicos
K.-o. #3 auszuschließen). 🟢 **Grün für die Koordinationsleistung.**
→ **Nur als Koordinationsmodell verfolgbar.**

---

### Modell 7 – Klimaanlagen-Inspektion (GEG §74) + F-Gase-Dichtheitsprüfung als Bündel

**1. Modellname + realer Anbieter + URL**
Energetische Inspektion nach §§74–78 GEG. Anbieter: encadi (encadi.de),
TGA Effizienz (tga-effizienz.de), Energieaudit365 (energieaudit365.de).
F-Gase: Infraserv (infraserv.com), Roter Kältetechnik (roter-kaeltetechnik.de),
Deutsche Thermo (deutsche-thermo.de), BFS Kälte-Klima (bfs-kaelte-klima.de).

**2. Beweis der Nachfrage**
- GEG §74: Betreiber von Klimaanlagen bzw. kombinierten Klima-/Lüftungsanlagen mit
  **Kältenennleistung > 12 kW** müssen energetische Inspektionen durchführen lassen [F:
  gesetze-im-internet.de/geg/__74.html, BBSR-GEG-Portal, 2026-08-05].
- Stichprobenregel bei Betreibern mit >10 Anlagen: jede 10. Anlage (bis 200 Anlagen), jede 20.
  (über 200) [F].
- F-Gase-VO **(EU) 2024/573**, in Kraft seit **11.03.2024**: Betreiber stationärer Klima-, Kälte-
  und Wärmepumpenanlagen müssen regelmäßige Dichtheitsprüfungen durch ein **zertifiziertes
  Unternehmen** durchführen und dokumentieren lassen; Prüfhäufigkeit nach CO₂-Äquivalent-Schwellen
  **5 / 10 / 50 / 500 t** [F: bfs-kaelte-klima.de, roter-kaeltetechnik.de, 2026-08-05].
- **Neu und wichtig:** Mit der Novelle fallen auch HFO-Kältemittel wie **R1234yf** unter die
  Dichtheitsprüfpflicht – das **erweitert den Prüfmarkt aktiv** [F: roter-kaeltetechnik.de].
- Anzahl betroffener Anlagen in DE: **[A] nicht ermittelt.**

**3. Was ist heute schlecht?**
- Das Feld ist **Ingenieurbüro-Territorium** – Einzelpersonen und Kleinstbüros
  (tga-effizienz.de, encadi, energieaudit365) mit Beratungs-Websites, ohne Produktcharakter,
  ohne Preise [F].
- Der Betreiber muss **zwei völlig getrennte Pflichten** erfüllen (GEG-Inspektion durch
  Energieberater, F-Gase-Dichtheitsprüfung durch zertifizierten Kältebetrieb) an **derselben
  Anlage** – und beauftragt dafür zwei Firmen.
- Die Ausnahme für gebäudeautomatisierte Nichtwohngebäude [F] macht die Rechtslage für Betreiber
  unübersichtlich → Beratungsbedarf, den heute niemand als Produkt verkauft.

**4. Was übernehmen wir?** Den Pflicht-Rhythmus als Umsatzbasis.

**5. Was verbessern wir?** Anlagen-Kataster mit automatischer Ermittlung, **welche** Pflicht für
**welche** Anlage greift (kW-Grenze, CO₂e-Schwelle, LES vorhanden ja/nein) – das ist heute
Handarbeit im Ingenieurbüro und ideal für Software.

**6. Was kombinieren wir neu?** GEG-Inspektion + F-Gase-Dichtheitsprüfung + Kältemittel-Logbuch
in einem Vertrag. Das Logbuch ist gesetzlich zu führen und liegt heute meist in Papier oder Excel.

**7. Warum wechselt ein Kunde zu uns?**
*„Sie wissen nicht sicher, welche Ihrer 23 Anlagen unter die neue F-Gase-Verordnung fällt und
welche unter §74 GEG – und Ihr Kältebetrieb weiß es auch nicht. Wir erfassen den Bestand einmal,
und danach sagt Ihnen das System für jede Anlage Pflicht, Intervall und nächsten Termin. Das
Logbuch führt sich selbst."*
Wechselgrund: **Rechtsunsicherheit bei geänderter Verordnung** – ein akuter, datierbarer Anlass
(11.03.2024) mit langem Nachlauf.

**8. Wiederkehrender Umsatz** Kataster-/Logbuch-Abo monatlich + Prüfaufträge im Zyklus.

**9. Delegierbarkeit** Mittel – die Bestandsbewertung erfordert Fachwissen; die laufende Führung
ist Software.

**10. Regulatorik-Ampel** 🟡 **Gelb** (Zertifizierungspflicht für die Dichtheitsprüfung selbst →
Partnermodell), 🟢 **Grün** für Kataster/Logbuch/Koordination.

---

### Modell 8 – Herstellerunabhängige Aufzugs-Betreuung (Wartung + Notruf + ZÜS-Koordination)

**1. Modellname + realer Anbieter + URL**
Aufzugswartung und -prüfung. Anbieter: TK Elevator (tkelevator.com), Schaufler Liftservice
(schaufler-liftservice.de), Güde Aufzugtechnik (guede-aufzugtechnik.com), aufzug24.net,
SVEAG Facility Management (sveag.de), personenaufzuege.com, Held Heimlift (held-heimlift.de).

**2. Beweis der Nachfrage**
- **Wiederkehrende Prüfung alle 2 Jahre durch eine ZÜS** (z. B. TÜV SÜD) ist durch die
  Betriebssicherheitsverordnung (BetrSichV) für **alle** Aufzugsanlagen vorgeschrieben,
  unabhängig von Nutzungsart [F: mehrere Quellen, 2026-08-05].
- Konsequenzen bei Nichteinhaltung: **Bußgelder, Stilllegung des Aufzugs, Verlust des
  Versicherungsschutzes, zivilrechtliche Haftungsansprüche** [F: sveag.de, 2026-08-05]. Das ist
  eine der schärfsten belegten Sanktionsketten in diesem Dokument → maximale Zahlungsbereitschaft.
- Wartung und Prüfung sind **strikt getrennt**: Wartung durch Aufzugsfirma, Prüfung durch
  unabhängige ZÜS; die Prüfung ersetzt die Wartung nicht [F].
- Anzahl Aufzüge in DE: **[A] nicht ermittelt** (Suche lieferte ausdrücklich keine Zahl).

**3. Was ist heute schlecht?**
- **Oligopol mit bekanntem Verhalten:** Der Markt wird von wenigen Konzernen dominiert; Kunden
  klagen über lange Reaktionszeiten und Bindung an den Hersteller über proprietäre Steuerungen
  [A – **nicht belegt in dieser Recherche**, aber gut dokumentiert in EU-Kartellverfahren der
  Vergangenheit; offener Rechercheauftrag].
- „Vollwartungsverträge" sind Blackbox-Verträge: Der Kunde weiß nicht, was enthalten ist [F: die
  Quellen unterscheiden lediglich zwischen Voll- und Teilwartung, ohne Preistransparenz].
- Hausverwaltungen müssen **Wartungsfirma, ZÜS-Prüftermin und Notrufaufschaltung getrennt**
  organisieren.

**4. Was übernehmen wir?** Nichts an der Wartung selbst (Spezialistenmarkt, hoher Kapitalbedarf).

**5. Was verbessern wir?** Die **Betreiberrolle**: transparente Vertragsprüfung, Terminsteuerung,
Mängelnachverfolgung nach ZÜS-Prüfung.

**6. Was kombinieren wir neu?**
Aufzugs-Compliance-Abo: ZÜS-Termin + Wartungsüberwachung + Notrufaufschaltung (Modell 9) +
Prüfbuch digital. Der Verwalter hat einen Ansprechpartner statt drei.

**7. Warum wechselt ein Kunde zu uns?**
*„Wenn die ZÜS-Prüfung überzogen wird, kann Ihr Aufzug stillgelegt werden und Ihre Versicherung
zahlt im Schadensfall nicht. Wir garantieren vertraglich, dass kein Prüftermin überzogen wird –
und wir verfolgen die Mängel aus dem Prüfbericht bis zur Erledigung nach."*
Wechselgrund: **Haftungsübernahme für Terminversäumnis** – ein Versprechen, das heute niemand gibt.

**8. Wiederkehrender Umsatz** Monatliche Gebühr pro Aufzug.

**9. Delegierbarkeit** Sehr hoch (reine Koordination). **Aber:** siehe K.-o. #10-Warnung –
Terminverfolgung muss Software sein.

**10. Regulatorik-Ampel** 🟢 **Grün** (Koordination) / 🔴 **Rot** (ZÜS-Prüfung selbst –
akkreditierungspflichtig, ausgeschlossen).

---

### Modell 9 – Notruf-/Alarmaufschaltung als Reseller-Abo (NSL)

**1. Modellname + realer Anbieter + URL**
Aufschaltung auf Notruf- und Serviceleitstelle. Anbieter/Vermittler: Notrufe24 (notrufe24.de),
ACC Sicherheitstechnik (accsicherheitstechnik.de), Secplan (secplan.de), Stadtritter
(stadtritter.de), WAB Security (wab-security.de).

**2. Beweis der Nachfrage**
- **Belegte Preise:** monatliche Aufschaltgebühren **20–50 €** bzw. **20–80 €** je nach Objekt
  und Leistungsumfang; Standardaufschaltung typisch **20–60 €/Monat**; NSL-Aufschaltung „ca.
  35 €/Monat"; Privatobjekte 59–79 €/Monat; Bandbreite gesamt 19–250 €/Monat [F: mehrere
  Anbieterquellen, 2026-08-05].
- Einmalige Einrichtungskosten **150–600 €** [F].
- Private Leitstellen können sich nach ISO 9001 und VdS-Richtlinien prüfen lassen [F].
- Anzahl NSL-Anbieter/Marktgröße DE: **[A] nicht ermittelt.**

**3. Was ist heute schlecht?**
- Extreme Preisspreizung bei nahezu identischer Leistung (19 € bis 250 €/Monat) [F] → klassisches
  Zeichen für **Preisintransparenz und schwachen Kundenvergleich**.
- Die Aufschaltung wird meist vom Errichter der Alarmanlage mitverkauft – der Kunde vergleicht nie.
- Kunden zahlen jahrelang, ohne je einen Alarm auszulösen → sehr hohe Marge, sehr geringe
  Wechselaktivität.

**4. Was übernehmen wir?** Das Abo-Modell selbst – es ist eines der reinsten MRR-Modelle im
deutschen Mittelstand.

**5. Was verbessern wir?** Öffentlicher Festpreis, Selbstservice-Portal (Alarmhistorie,
Kontaktketten, Scharfschaltzeiten selbst pflegen – heute ein Telefonat mit der Leitstelle).

**6. Was kombinieren wir neu?**
Aufschaltung + Aufzugsnotruf + Brandmeldeanlagen-Aufschaltung + technische Störmeldung
(Kühlraum, Heizung, Serverraum) in einem Vertrag.

**7. Warum wechselt ein Kunde zu uns?**
*„Sie zahlen 79 € im Monat für die Aufschaltung Ihrer Alarmanlage, 45 € für den Aufzugsnotruf
und 60 € für die Brandmeldeanlage – an drei verschiedene Leitstellen. Wir machen alles für 99 €,
mit einer Rufnummernliste, die Sie selbst online ändern können."*
Wechselgrund: **Bündelpreis + Selbstverwaltung der Kontaktkette.**

**8. Wiederkehrender Umsatz** 100 % Abo. Bestes MRR-Profil aller Modelle hier.

**9. Delegierbarkeit** Hoch – die Leitstelle selbst wird **eingekauft** (Wholesale), nicht betrieben.

**10. Regulatorik-Ampel**
🟢 **Grün als Reseller/Vermittler.** 🔴 **Rot als Leitstellenbetreiber** – 24/7-Personalbetrieb
verstößt zudem gegen Nicos K.-o. #7/#8, wenn er selbst betrieben würde. **Nur Reseller-Variante
zulässig.**

---

### Modell 10 – KI-Telefonassistent für technische Dienstleister (ebuero-Ablösung)

**1. Modellname + realer Anbieter + URL**
KI-gestützte Anrufannahme. Klassische Anbieter: ebuero AG (ebuero.de), Starbüro
(starbuero.de), Sekretaria. KI-Anbieter: HalloPetra (hallopetra.de), PORTA, voiceOne (OneAI UG),
Vokaro (vokaro.net), ruflab (ruflab.com).

**2. Beweis der Nachfrage**
- **Belegte Preise ebuero:** Grundgebühr **59,90 € (Einsteiger) / 99,90 € (Standard) /
  179,90–189,90 € (Profi)** pro Monat [F: ebuero.de-Preisverzeichnis und telefon.services,
  Stand 2026-08-05].
- ebuero ist 365 Tage/24 h erreichbar, meldet sich mit dem Firmennamen des Kunden, nimmt Name
  und Nummer auf und schickt eine E-Mail [F].
- KI-Seite: HalloPetra gibt **über 1.000 nutzende Handwerksbetriebe** an (SHK, Elektro,
  Kälte/Klima) [F: Anbieterangabe via Suchergebnis-Zusammenfassung, **nicht unabhängig geprüft**].
- Der Markt ist so weit entwickelt, dass **Vergleichsartikel mit „Top 7 / Top 9 / Top 12 / Top 15
  Anbietern"** existieren (Superchat, Placetel, Zeeg, ruflab, Vokaro) [F] → Nachfrage bewiesen,
  aber **auch: Markt bereits überfüllt.**

**3. Was ist heute schlecht?**
- **Bei den Alt-Anbietern:** Kritische Bewertungen beschreiben „sehr fragwürdige Methoden der
  Verkäufer" und dass „andere Kosten abgerechnet werden als vereinbart" [F: Trustpilot-Bewertungen
  zu ebuero.de, wiedergegeben in Suchergebnis-Zusammenfassung, 2026-08-05 – **Evidenzstufe 2**,
  Original war durch Proxy-Policy nicht abrufbar].
- Das Leistungsversprechen der Alt-Anbieter endet bei „Notiz per E-Mail". Der Kunde muss immer
  noch zurückrufen. **Das Problem ist nicht gelöst, nur verschoben.**
- **Bei den KI-Anbietern:** Alle sichtbaren Anbieter sind **inbound-only** und branchenoffen mit
  Templates. Kein Anbieter übernimmt Verantwortung für ein Geschäftsergebnis.

**4. Was übernehmen wir?** Das Preismodell (Monatsgebühr + Volumenstaffel) und die
Positionierung „Sie verpassen keinen Anruf mehr".

**5. Was verbessern wir?** Nicht „bessere KI" – das ist eine Commodity und in 12 Monaten
eingeholt. Sondern: **Ergebnisverantwortung** – nicht Anruf angenommen, sondern **Termin steht
im Kalender des Monteurs**.

**6. Was kombinieren wir neu?** Inbound-KI + **Outbound-Terminierung** (→ Modell 12) im selben
Vertrag. Der Assistent nimmt nicht nur an, er ruft auch raus.

**7. Warum wechselt ein Kunde zu uns?**
*„Ihr Telefonservice schickt Ihnen 14 E-Mails am Tag mit Namen und Nummern. Sie rufen abends
zurück, erreichen die Hälfte nicht. Bei uns steht am Abend nicht eine Notiz im Postfach, sondern
ein bestätigter Termin im Kalender – und wir rufen die anderen sieben von uns aus nochmal an."*
Wechselgrund: **E-Mail-Notiz vs. bestätigter Termin.**

**8. Wiederkehrender Umsatz** Monatliche Grundgebühr + Preis pro vereinbartem Termin
(erfolgsabhängige Komponente).

**9. Delegierbarkeit** Sehr hoch (Software + kleines Ops-Team).

**10. Regulatorik-Ampel**
🟡 **Gelb.** Zwei reale Themen: (a) **DSGVO** – Sprachaufzeichnung und Verarbeitung, AV-Verträge,
Hosting in DE (die deutschen Anbieter werben genau damit: „Made & hosted in Germany" [F]);
(b) **UWG §7** – Outbound-Anrufe brauchen Einwilligung. Bei **Bestandskunden-Terminierung im
Rahmen eines Wartungsvertrags** ist das unproblematisch, bei Kaltakquise nicht. **Diese Grenze
ist geschäftsentscheidend und muss anwaltlich geklärt werden.**

**Wettbewerbswarnung:** Dies ist das am dichtesten besetzte Feld im ganzen Dokument
(≥5 deutsche Anbieter, Vergleichsartikel mit bis zu 15 Anbietern [F]). Reines
„KI-Telefonassistent"-Angebot ist **kein** tragfähiges Maschine-A-Modell mehr. Nur die
Nischen-/Outbound-Variante (Modell 12) ist noch offen.

---

### Modell 11 – Büroservice neu gedacht: „Auftragsannahme als Ergebnis" für Handwerk

**1. Modellname + realer Anbieter + URL**
Telefon-/Büroservice. Anbieter: ebuero (ebuero.de), Starbüro (starbuero.de, betreibt eine
eigene Preisvergleichsseite gegen Wettbewerber [F]), sekretariatsservices.vergleichhoch2.de.

**2. Beweis der Nachfrage**
- Preise 59,90–189,90 €/Monat bei ebuero [F, siehe Modell 10].
- Dass ein Anbieter (Starbüro) eine eigene **Preisvergleichsseite gegen Wettbewerber** betreibt
  [F: starbuero.de/preisvergleich], zeigt: Der Markt ist preisumkämpft und der Kunde vergleicht
  aktiv → Nachfrage vorhanden, Differenzierung schwach.
- Ein Fachportal (legal-tech.de) hat einen **Selbsttest externer Telefonservices** publiziert
  [F] → das Thema hat genug Relevanz für redaktionelle Auseinandersetzung.

**3. Was ist heute schlecht?**
- Die Leistung ist seit 20 Jahren identisch: annehmen, notieren, mailen.
- Bewertungskritik (siehe Modell 10): Vertriebsmethoden und Abrechnung abweichend von der
  Vereinbarung [F, Evidenzstufe 2].
- Volumenstaffeln machen die Kosten unvorhersehbar – der Kunde weiß nicht, was der Monat kostet.

**4. Was übernehmen wir?** Nichts vom Kern – dieses Modell ist **die Vorlage, die wir ablösen**,
nicht die, die wir kopieren. Übernommen wird nur die Erkenntnis: **KMU zahlen monatlich für
Erreichbarkeit.**

**5. Was verbessern wir?** Flatrate statt Volumenstaffel.

**6. Was kombinieren wir neu?** Siehe Modell 12.

**7. Warum wechselt ein Kunde zu uns?** Siehe Modell 10.

**8. Wiederkehrender Umsatz** Monatsflatrate.

**9. Delegierbarkeit** Hoch, wenn KI-basiert; **niedrig und personalintensiv**, wenn menschliche
Agenten (das klassische Modell ist ein Callcenter – nach Nicos Profil unattraktiv).

**10. Regulatorik-Ampel** 🟡 Gelb (DSGVO).

**Einstufung: Ablösekandidat, nicht Kopiervorlage.**

---

### Modell 12 – ⭐ Terminierungs-Abo für Prüf- und Wartungsdienstleister („Umsatz aus der eigenen Kundenliste")

**Dies ist das Modell, das die Sonderprüfung aus Abschnitt 3 in ein Produkt übersetzt.**

**1. Modellname + realer Anbieter + URL**
Vergleichbare Bausteine, aber **kein integrierter Anbieter gefunden**:
Certado (certado.io – kennt die Fälligkeiten, terminiert aber nicht aktiv), Vemas
(msconsulting.de – optimiert Touren, akquiriert aber keine Termine), HalloPetra/voiceOne/Vokaro
(KI-Telefonie, aber inbound und ohne Fälligkeitsdatenbank).

**2. Beweis der Nachfrage**
- **Indirekt, aber stark:** Prüfdienstleister-Software wirbt explizit mit „zeigt automatisch,
  welcher Kunde wann fällig ist" und „automatisch versandte Erinnerungen" [F: certado.io].
  Wenn Erinnerungen ein verkaufbares Feature sind, ist das dahinterliegende Problem
  (Kunden verlängern nicht von allein) bewiesen.
- Vemas verkauft „optimiert Termine, Touren und Ressourcen automatisch" [F] – die **Auslastung
  des Technikers** ist also der anerkannte Engpass der Branche.
- Anbieterzahl im Zielmarkt: allein aus zwei Suchen ≥15 bundesweite Prüfdienstleister
  identifiziert [F]; Gesamtzahl Prüf-/Wartungsbetriebe in DE: **[A] nicht ermittelt.**
- **Warnung:** Die Nachfrage ist hier **abgeleitet, nicht direkt belegt.** Kein einziger
  gefundener Anbieter verkauft dieses Produkt – das kann Marktlücke **oder** Marktversagen
  bedeuten. Vor jedem Aufbau: 20 Prüfdienstleister anrufen und fragen, was ein bestätigter
  Termin ihnen wert ist. **Das ist der erste Schritt, nicht der Produktbau.**

**3. Was ist heute schlecht?**
- Der Prüfdienstleister hat 400 Kunden mit Jahresfälligkeit und **eine Bürokraft**, die
  telefoniert.
- E-Mail-Erinnerungen haben schlechte Rücklaufquoten [A – **nicht belegt**, muss gemessen werden].
- Die Folge: Techniker-Auslastung schwankt, Kunden fallen still ab, Wettbewerber übernimmt.

**4. Was übernehmen wir?** Das Terminierungs-Handwerk aus dem Callcenter – ein Bereich, in dem
Nico nachweislich Erfahrung hat (Nordstern Abschnitt 4: „Nico kennt Lead-Ökonomie und
Terminierung aus der Praxis").

**5. Was verbessern wir?** Menschliche Terminierung kostet ~15–35 € pro erreichtem Termin
[A – Erfahrungsbandbreite, nicht belegt]. KI-Terminierung senkt die Grenzkosten drastisch und
skaliert nachts und am Wochenende.

**6. Was kombinieren wir neu?**
**Fälligkeitsdatenbank + KI-Outbound + Kalender-Rückschreibung + Tourenlogik.** Der Kunde des
Prüfdienstleisters wird angerufen, bekommt zwei Terminvorschläge, die **geografisch zur Tour
passen**, bestätigt, und der Termin landet im Dispositionssystem.

**7. Warum wechselt ein Kunde zu uns?**
*„Ihre Frau Meier telefoniert drei Tage im Monat Ihre Fälligkeitsliste ab und schafft 60 Kunden.
Wir rufen alle 400 an, in einer Woche, auch abends – und legen die Termine so, dass Ihr Monteur
nicht quer durch den Landkreis fährt. Sie zahlen pro bestätigtem Termin, nicht pro Anruf."*
Wechselgrund: **Auslastung des Technikers und Rettung der Bestandskunden** – direkt in Euro
messbar, weil der Kunde weiß, was ein Prüfauftrag wert ist.

**8. Wiederkehrender Umsatz: woher genau**
Monatliche Plattformgebühr (Fälligkeitsdatenbank + Anbindung) + Preis pro bestätigtem Termin.
Der wiederkehrende Anteil kommt daher, dass **Fälligkeiten jedes Jahr wiederkommen** – der
Kunde kann nicht aussteigen, ohne sein Terminproblem zurückzubekommen.

**9. Delegierbarkeit** Sehr hoch – nach dem Aufbau ist es Software plus ein kleines
Kundenerfolgsteam.

**10. Regulatorik-Ampel**
🟡 **Gelb.** (a) **UWG §7:** Anrufe bei **Bestandskunden des Auftraggebers zur Erfüllung eines
bestehenden Wartungs-/Prüfverhältnisses** sind rechtlich anders zu bewerten als Kaltakquise –
das ist der tragende Rechtsgedanke des ganzen Modells und **muss vor dem ersten Euro anwaltlich
abgesichert werden.** (b) DSGVO: Auftragsverarbeitung, Kundendaten des Auftraggebers.
(c) KI-Transparenz: Anrufer muss erkennen können, dass er mit einem System spricht (EU AI Act,
Transparenzpflichten) [A – konkrete Anwendbarkeit auf diesen Fall nicht geprüft].

**Asset-Passung:** Höchste im gesamten Dokument. Twilio-Stack produktiv, deutsche Rufnummer
vorhanden, Listenmodell (`cs_listen`), Terminstatus-Tracking (`cs_arbeitszeit`),
Partner-Webhook-Ingest – alles laut Nordstern Abschnitt 4 belegt vorhanden.

**Ehrliche Gegenrede:** Der Burggraben ist dünn. Certado und Vemas sitzen auf den Daten und
können das Feature bauen. Wer hier gewinnt, gewinnt über Geschwindigkeit und Vertragsbindung,
nicht über Technik.

---

### Modell 13 – Arbeitssicherheits-Betreuung (Sifa) als Produkt-Abo

**1. Modellname + realer Anbieter + URL**
Sicherheitstechnische Betreuung nach ASiG/DGUV V2. Anbieter: 123ingenieure (123ingenieure.de),
arbeitssicherheit-fachkraft.de, fachkraft-arbeitssicherheit.com, arbeitssicherheit-deutschland.de,
Ullertec (ullertec.de), ABEMA (abema-bg.de), ProSafeCon, safest (safest.gmbh).

**2. Beweis der Nachfrage**
- **Belegte Preise:** Betreuung **ab 49 €/Monat**; ProSafeCon ab **98 €/Monat**; Stundensätze
  **75–130 €**, teils **80–200 €**; Sanitätswerk Lübke 80–150 €/h [F: mehrere Anbieterquellen,
  2026-08-05].
- **Anbieterdichte belegt:** safest.gmbh listet „über 643 Anbieter mit Bewertungen von 4,5 oder
  höher" [F: safest.gmbh, 2026-08-05]. → Das ist die **härteste Anbieterzahl** in diesem Dokument
  und beweist einen großen, funktionierenden Markt.
- Gesetzliche Pflicht: Jeder Betrieb mit mindestens einem Beschäftigten braucht
  sicherheitstechnische Betreuung [A – die genaue Schwelle je nach DGUV V2 Betreuungsmodell
  nicht in dieser Recherche belegt].

**3. Was ist heute schlecht?**
- **Domain-Kannibalismus als Symptom:** `arbeitssicherheit-fachkraft.de`,
  `fachkraft-arbeitssicherheit.com`, `arbeitssicherheit-deutschland.de`,
  `arbeitssicherheit.gmbh`, `123ingenieure.de` – mehrere fast identische Angebote, alle mit
  „Nr. 1"-Claim im Seitentitel („Sicherheitstechnische Betreuung jetzt bei Deutschlands Nr. 1",
  „Fachkraft für Arbeitssicherheit sofort bei der Nr.1") [F: Suchergebnis-Titel, 2026-08-05].
  Wenn vier Anbieter gleichzeitig „Nr. 1" sind, ist die Kategorie **markenlos**.
- Preisspreizung 49 €/Monat bis 200 €/Stunde für nominell dieselbe Rolle [F] → maximale
  Preisintransparenz.
- Die Leistung wird als **Stunden** verkauft (ein K.-o. nach Nicos Kriterium #16, wenn 1:1 kopiert).

**4. Was übernehmen wir?** Die gesetzliche Pflicht als Umsatzanker und das Monatsabo-Preisschema
(49–150 €/Monat/Betrieb).

**5. Was verbessern wir?** Weg von Stunden, hin zu **Ergebnis-Paketen**:
Gefährdungsbeurteilung + Unterweisungen + Begehung + Dokumentenablage als definierter Jahresumfang
zum Festpreis.

**6. Was kombinieren wir neu?** Sifa-Betreuung **plus** die physischen Prüfungen (Modelle 2–5)
plus E-Learning-Unterweisung (Modell 15). Heute kauft der Betrieb das bei drei bis fünf Firmen –
obwohl es **dieselbe Compliance-Akte** betrifft.

**7. Warum wechselt ein Kunde zu uns?**
*„Ihre Sifa kommt zweimal im Jahr, macht eine Begehung und schickt ein Protokoll. Die Prüfung
Ihrer Geräte, Ihrer Regale und Ihrer Tore und die Unterweisung Ihrer Leute organisieren Sie
trotzdem selbst. Bei uns ist die Sifa der Kopf, und wir bringen die Prüfer und die Schulungen
gleich mit – ein Vertrag, eine Akte, ein Ansprechpartner."*
Wechselgrund: **Die Sifa wird vom Berater zum Generalunternehmer der Arbeitssicherheit.**

**8. Wiederkehrender Umsatz** Monatsabo je Betrieb, gestaffelt nach Mitarbeiterzahl.

**9. Delegierbarkeit** Mittel bis hoch – Sifa-Qualifikation ist eine mehrmonatige Ausbildung, das
begrenzt die Rekrutierungsgeschwindigkeit. **Aber:** Der Nordstern verlangt „wenige hochwertige
Kunden statt hunderte Kleinkunden" (Kriterium #5) – dieses Modell tendiert zu vielen Kleinkunden
à 49–150 €. Bei 100.000 €/Monat wären das **bei 120 €/Monat ca. 830 Kunden [S: 100.000 / 120]**.
Das ist ein **ernstes Strukturproblem** und spricht gegen das Modell als Alleinstellung.

**10. Regulatorik-Ampel** 🟡 **Gelb** – Sifa-Qualifikation nach ASiG erforderlich, Haftung real.

---

### Modell 14 – Externer Datenschutzbeauftragter als Software-first-Abo

**1. Modellname + realer Anbieter + URL**
Externer DSB. Anbieter: eDSB-Deutschland (edsb-deutschland.de), PRICOM (pri-com.de),
Cortina Consult (cortina-consult.com), gesellschaft-datenschutz.de, keyed (keyed.de),
BullProtect (bullprotect.de), fraghugo (fraghugo.de).

**2. Beweis der Nachfrage**
- Pflicht nach **Art. 37 DSGVO** bei Behörden, umfangreicher regelmäßiger Überwachung oder
  Verarbeitung besonderer Kategorien (Art. 9–10) [F].
- **Belegte Preise:** **98–490 €/Monat** Bandbreite; Einstiegsangebote ab **99 €**, **125 €**,
  **149 €**, **250 €**/Monat; KMU typisch **500–1.200 €/Monat**; Stundenmodelle 120–200 €/h
  [F: mehrere Anbieterquellen, 2026-08-05].
- **Zusätzlicher, sehr wichtiger Nachfragetreiber:** „Auch ohne gesetzliche Pflicht bestellen
  viele KMU freiwillig einen externen DSB, weil Geschäftspartner oder Auftraggeber dies in
  Vergabeprozessen fordern" [F: fraghugo.de-Zusammenfassung, 2026-08-05]. → Nachfrage entsteht
  aus **Lieferkettendruck**, nicht nur aus Gesetz. Das ist ein sehr robuster Treiber.

**3. Was ist heute schlecht?**
- Preisspreizung 99 € bis 1.200 €/Monat für dieselbe Rolle [F].
- Der Markt zerfällt in „Kanzlei mit Beratung", „reine Softwarelösung" und „Hybrid" [F:
  keyed.de-Zusammenfassung] – der Kunde kann die Kategorien nicht unterscheiden.
- Vergleichsportale (fraghugo.de mit „Die 10 besten Anbieter 2026") existieren [F] → Zeichen für
  Unübersichtlichkeit.

**4. Was übernehmen wir?** Das Abo-Preisschema.

**5. Was verbessern wir?** Nichts Substanzielles – **und das ist die ehrliche Bewertung**.

**6. Was kombinieren wir neu?** Datenschutz + IT-Sicherheit (NIS2) + Compliance-Schulung.

**7. Warum wechselt ein Kunde zu uns?** **Kein überzeugender Wechselgrund gefunden.**
Der Markt ist bereits Software-first, bereits preisaggressiv, bereits abo-basiert.

**8. Wiederkehrender Umsatz** Gut (Monatsabo).

**9. Delegierbarkeit** Hoch.

**10. Regulatorik-Ampel** 🟡 Gelb.

**Einstufung: AUSSCHEIDEN.** Nachfrage belegt, aber die Kriterien „Anbieter veraltet" und
„Kundenerfahrung erwiesenermaßen schlecht" sind **nicht erfüllt**. Der Markt hat sich bereits
selbst modernisiert. Wird hier dokumentiert, damit dieser Weg nicht doppelt geprüft wird.

---

### Modell 15 – Unterweisungs-/Pflichtschulungs-Abo (E-Learning) als Anhängsel-Produkt

**1. Modellname + realer Anbieter + URL**
Pflichtunterweisung nach §12 ArbSchG / DGUV V1 als E-Learning. Anbieter: WEKA
(weka-elearning.de), VINYA (vinya.io), thinkmedia (thinkmedia.de), IMS-Schulung
(ims-schulung.de), EASI Control.

**2. Beweis der Nachfrage**
- Jährliche Unterweisungspflicht nach §12 ArbSchG und DGUV V1 [F].
- WEKA bietet **über 70 Kurse** aus Arbeitsschutz, Brandschutz, Compliance, Datenschutz im
  SaaS-Modell an [F: weka-elearning.de, 2026-08-05].
- **Belegte Preise:** IMS-Schulung 22,50–75,00 € netto je nach Teilnehmerzahl [F].

**3. Was ist heute schlecht?**
- Preise sind „konfigurierbar" und schwer vergleichbar [F].
- Es existiert eigener Vergleichsjournalismus („Unterweisungsmanager im Vergleich: So findest du
  den besten!" – digital-affin.de) [F].
- Der eigentliche Schmerz ist nicht der Kurs, sondern **der Nachweis, dass alle 47 Mitarbeiter
  ihn gemacht haben** – und das Nachhalten der 6 Nachzügler.

**4. Was übernehmen wir?** Den Kurskatalog (zukaufbar/lizenzierbar – nicht selbst produzieren).

**5. Was verbessern wir?** Automatische Nachverfolgung der Nachzügler über denselben
KI-Telefon-/SMS-Kanal wie Modell 12.

**6. Was kombinieren wir neu?** Unterweisung als **Zusatzmodul** im Prüf-Abo (Modelle 2–5, 13) –
gleicher Kunde, gleicher Ansprechpartner, gleiche Compliance-Akte, Grenzkosten nahe null.

**7. Warum wechselt ein Kunde zu uns?**
*„Sie haben die Kurse schon. Was Sie nicht haben: eine Liste, wer sie noch nicht gemacht hat,
und jemanden, der die sechs Nachzügler daran erinnert. Das machen wir – und es steht in derselben
Akte wie Ihre Geräteprüfung."*

**8. Wiederkehrender Umsatz** Pro Mitarbeiter pro Jahr – skaliert automatisch mit dem Kunden.

**9. Delegierbarkeit** Sehr hoch (reines Softwareprodukt).

**10. Regulatorik-Ampel** 🟢 **Grün.**

**Einstufung: Kein eigenständiges Modell, aber ein exzellenter Margen-Aufsatz.** Bruttomarge in
diesem Baustein deutlich über 80 % [A].

---

### Modell 16 – Equipment-as-a-Service nach Hilti-Vorbild (Nischen-Flottenmodell)

**1. Modellname + realer Anbieter + URL**
Hilti Fleet Management (hilti.group/.../fleet-management).

**2. Beweis der Nachfrage – das am besten belegte Modell im Dokument**
- Hilti stellte 1999 vom Werkzeugverkauf auf Werkzeug-Miete mit Monatsgebühr um; enthalten sind
  Gerätetausch auf neuere Modelle, Service und Wartung [F: HBS-/BMI-Fallstudien, hilti.group].
- **Kundenbindung fünfmal höher** als im vorherigen Geschäftsmodell; überproportionaler
  Ergebnisbeitrag [F: Business Model Navigator, HBS-Fallstudie].
- **1,5 Mio. Werkzeuge unter Fleet-Verträgen in 40 Ländern, Vertragswert über 1,2 Mrd. CHF
  (Stand 2015)** [F].
- Hiltis CTO nannte es „die wichtigste Innovation der Firmengeschichte" [F].
- Das Modell ist **akademisch dokumentiert** (Harvard Business School, mehrere Fallstudien) –
  stärkere Validierung gibt es für kein anderes Modell in diesem Dokument.

**3. Was ist heute schlecht?**
- Das Modell ist **außerhalb von Hilti kaum kopiert worden** – die Suche fand explizit keine
  Nachahmer [F: „the search results do not contain specific information about competitors or
  imitators"]. In Nischen (Messtechnik, Prüfgeräte, Vermessung, Akkusysteme, Gartentechnik im
  GaLaBau, Reinigungstechnik) gibt es überwiegend **klassische Miete oder klassischen Verkauf**,
  nicht das Flottenmodell mit Tausch, Wartung und Diebstahlschutz [A – nicht systematisch geprüft].

**4. Was übernehmen wir?** Die vollständige Modelllogik: Monatsgebühr, Tausch, Reparatur,
Verlustabsicherung, definierte Gerätezahl, Vertragslaufzeit.

**5. Was verbessern wir?** Reservierung/Tausch per App statt per Außendienst.

**6. Was kombinieren wir neu?**
**Flottenmodell + gesetzliche Prüfung.** Beispiel: elektrische Prüfgeräte, Messgeräte, Leitern,
Hebezeuge – Geräte, die **selbst prüfpflichtig** sind. Wer sie vermietet, kann die Prüfung
gleich mitliefern. Der Kunde hat dann per Definition nie ein ungeprüftes Gerät im Einsatz.
**Das ist ein echter, neuer Kombinationsgedanke** und mit keinem gefundenen Anbieter besetzt [A].

**7. Warum wechselt ein Kunde zu uns?**
*„Ihre 40 Leitern und 12 Hebezeuge müssen jährlich geprüft werden – Sie wissen nicht mehr genau,
welche wo steht und welche fällig ist. Bei uns mieten Sie sie zum Monatspreis, und was fällig
ist, tauschen wir aus. Sie haben nie wieder ein ungeprüftes Gerät auf der Baustelle."*
Wechselgrund: **Prüfpflicht verschwindet vom Kunden zum Vermieter.**

**8. Wiederkehrender Umsatz** 100 % Abo.

**9. Delegierbarkeit** Hoch, aber operativ logistiklastig.

**10. Regulatorik-Ampel** 🟢 **Grün.**

**Warnung – der Grund, warum das nicht Platz 1 ist:** **Kapitalintensität.** Das Modell
verlangt, den Gerätepark vorzufinanzieren. Nach Nicos Zusatzkategorie „Startkapitalbedarf" ist
das der schlechteste Wert im Dokument. Machbar nur mit Leasingpartner oder Herstellerfinanzierung.

---

### Modell 17 – Rundenservice-Modell nach MEWA/CWS-Vorbild in einer Nische

**1. Modellname + realer Anbieter + URL**
MEWA Textil-Service (mewa.de), CWS Hygiene Deutschland (cws.com), Hagleitner (hagleitner.com).

**2. Beweis der Nachfrage – zweitbeste Belegqualität im Dokument**
- **MEWA Umsatz 2024: rund 938 Mio. €** [F: northdata/Unternehmensangaben via Suche, 2026-08-05].
- **Marktanteil 35 % in Deutschland, 11 % in Europa** [F].
- **Über 200.000 B2B-Kunden, 53 Standorte, über 6.000 Mitarbeiter** [F].
- Gegründet 1908 [F] – das Modell trägt seit über 100 Jahren.
- CWS bündelte 2021 vier Gesellschaften zu CWS Hygiene Deutschland [F] → aktive Konsolidierung.
- Hagleitner: Direktvertrieb in 12 Ländern, Handelspartner in über 60 Ländern [F].

**3. Was ist heute schlecht?**
- Das Modell selbst funktioniert hervorragend – **hier ist nichts kaputt.** Was fehlt, sind
  **Nischen**, in denen es noch nicht angewendet wird.
- MEWA hat 35 % Marktanteil – 65 % liegen bei kleineren, schlechter organisierten Anbietern [S:
  100 % − 35 %].

**4. Was übernehmen wir?** Die Mechanik: Der Kunde besitzt nichts, zahlt monatlich, der
Dienstleister kommt in festen Runden, tauscht Verbrauchtes gegen Frisches, rechnet pauschal ab.
Kündigungsquote gegen null, weil der Ersatz Aufwand bedeutet.

**5. Was verbessern wir?** Verbrauchstransparenz (der Kunde weiß nie, ob er zu viel zahlt) und
Online-Anpassung der Liefermengen.

**6. Was kombinieren wir neu?** Rundenservice **+ Prüfleistung auf derselben Fahrt.**
Wer ohnehin monatlich zum Kunden fährt, kann Feuerlöscher-Sichtkontrolle, Erste-Hilfe-Auffüllung
und Prüfplaketten-Kontrolle im selben Besuch erledigen. **Die Fahrt ist bezahlt – die
Zusatzleistung ist fast reine Marge.**

**7. Warum wechselt ein Kunde zu uns?**
*„Bei Ihnen kommt einmal im Monat der Mattenservice, zweimal im Jahr der Feuerlöscherprüfer,
einmal die Erste-Hilfe-Auffüllung und einmal die Handtuchspender-Wartung. Vier Firmen, vier
Termine, vier Rechnungen. Wir kommen einmal im Monat und machen alles."*
Wechselgrund: **Vier Besuche werden einer.**

**8. Wiederkehrender Umsatz** 100 % Abo. Historisch bewiesen über >100 Jahre [F].

**9. Delegierbarkeit** Sehr hoch – Fahrer/Servicetechniker mit fester Route ist die am besten
delegierbare Tätigkeit im Dokument.

**10. Regulatorik-Ampel** 🟢 **Grün.**

**Warnung:** Logistik- und Kapitalintensität (Fahrzeuge, Lager, Textilbestand). Bruttomarge in
Wäschereimodellen liegt deutlich unter Nicos 65-%-Ziel [A – nicht belegt, aber
Industriewäscherei ist strukturell margenschwächer]. **Der Kombinationsgedanke (Prüfung auf der
bezahlten Fahrt) ist der eigentliche Wert dieses Modells, nicht das Textilgeschäft.**

---

### Modell 18 – Waschraum-/Hygieneservice-Abo in unterversorgter Nische

**1. Modellname + realer Anbieter + URL**
CWS Hygiene (cws.com/de-DE/hygiene), Hagleitner Hygiene Deutschland (hagleitner.com).

**2. Beweis der Nachfrage**
- CWS bündelte zum 01.01.2021 die Hygieneaktivitäten von CWS-boco Deutschland, Service to go,
  Initial Hygieneservice und Initial Textil Service in eine Gesellschaft [F: cws.com] → Der Markt
  ist groß genug für Vierfach-Konsolidierung.
- Hagleitner betreibt Standorte in Frankfurt, Sauerlach, Kirchheim/Teck, Nürnberg, Greven, Berlin
  [F] → flächendeckende Direktvertriebsstruktur lohnt sich.
- Marktgröße/Umsatz: **[A] nicht ermittelt.**

**3. Was ist heute schlecht?** Zwei große Anbieter dominieren; kleine und mittlere Kunden
(Handwerksbetriebe, Autohäuser, Arztpraxen) sind für deren Außendienst unattraktiv [A].

**4.–10.** Strukturell identisch zu Modell 17.
**Regulatorik: 🟢 Grün. Delegierbarkeit: sehr hoch.**

**Einstufung: Variante von Modell 17, kein eigenständiger Top-Kandidat.**

---

### Modell 19 – PV-Betriebsführung (O&M) für Gewerbedächer als Abo

**1. Modellname + realer Anbieter + URL**
Cleanwatt (cleanwatt.de/servicevertrag-fuer-photovoltaikanlagen/), PV-Service GmbH
(pv-service-gmbh.com), pv-montagefirmen.de, solaranlage-ratgeber.de.

**2. Beweis der Nachfrage**
- **Belegte Preise:** Pauschalwartung 120–300 €/Jahr (EFH); leistungsbezogen **18 €/kWp bei
  11–20 kWp**, **14 €/kWp bei 100 kWp**; Servicepakete 150 € (Basis) bis 500 € (Vollservice) pro
  Jahr [F: solaranlage-ratgeber.de, pv-montagefirmen.de, 2026-08-05].
- **Monitoring ist 30–40 % billiger als Vor-Ort-Wartung** [F] → Fernüberwachung ist die
  margenstarke Variante.
- Im gewerblichen Bereich ist der **E-Check PV vorgeschrieben** (privat alle 4 Jahre empfohlen)
  [F: solaranlage-ratgeber.de] → gesetzlicher Anker im B2B-Segment vorhanden.

**3. Was ist heute schlecht?**
- Wartungsverträge werden **vom Installateur** mitverkauft – ein Bauunternehmen, das kein
  Interesse an laufendem Service hat [A].
- Es gibt Vertragsmuster von Anwaltskanzleien im freien Umlauf (liesegang-partner.de,
  phasenwerk.de) [F] → Zeichen dafür, dass die Branche **noch keine standardisierten
  Produktverträge** hat, sondern jeder selbst bastelt.
- Bei Monitoring-Abos ist unklar, ob die App kostenlos oder kostenpflichtig ist [F: explizite
  Warnung auf pv-montagefirmen.de] → Preisintransparenz belegt.

**4. Was übernehmen wir?** Das leistungsbezogene Preisschema (€/kWp/Jahr) – es skaliert
automatisch mit der Anlagengröße.

**5. Was verbessern wir?** Ertragsgarantie statt Wartungsversprechen: Wir überwachen und melden
Ertragsabweichungen innerhalb von 48 Stunden.

**6. Was kombinieren wir neu?** PV-Monitoring + E-Check PV + DGUV V3 des Betriebs +
Wallbox-/Ladeinfrastrukturwartung. Alles Elektro, alles derselbe Standort, alles derselbe Prüfer.

**7. Warum wechselt ein Kunde zu uns?**
*„Ihre 300-kWp-Anlage läuft seit vier Monaten mit einem defekten String und niemand hat es
gemerkt – Ihr Installateur schaut nicht drauf. Bei uns sehen wir das am nächsten Tag und melden
uns bei Ihnen, bevor Sie es in der Abrechnung sehen."*
Wechselgrund: **Entgangener Ertrag ist in Euro rechenbar** – das ist der stärkste rein
wirtschaftliche Wechselgrund im ganzen Dokument (kein Compliance-Argument nötig).

**8. Wiederkehrender Umsatz** €/kWp/Jahr, monatlich abgerechnet.

**9. Delegierbarkeit** Hoch – Monitoring ist Software, Vor-Ort nur bei Störung.

**10. Regulatorik-Ampel** 🟡 **Gelb** – Arbeiten an der Anlage erfordern Elektrofachkraft;
Ertragsgarantien erzeugen Haftungsrisiko und müssen sorgfältig formuliert werden.

---

### Modell 20 – Ablösung veralteter Branchensoftware (Vertical SaaS)

**1. Modellname + realer Anbieter + URL**
Beispielhaft belegt an Handwerkersoftware: Streit Software, Sander & Doll
(capterra.com.de/software/201513/), Hero, BauFaktura, ServiceTitan (US).
Im Prüfdienstleister-Segment: HOPPE Wartungsplaner (wartungsplaner.de), Certado (certado.io),
Vemas (msconsulting.de).

**2. Beweis der Nachfrage**
- Es existieren mindestens **24 bewertete Handwerkersoftware-Anbieter** in Vergleichsportalen
  [F: handwerker-software.org, „24 Anbieter bewertet mit echten Nutzerstimmen", 2026-08-05];
  weitere Portale vergleichen 13 bzw. 10 Anbieter [F: fuer-gruender.de, softwareabc24.de].
- Capterra Deutschland führt eine eigene Kategorie mit Preisvergleich [F].
- **Software erzielt die höchsten Bewertungsmultiples aller Branchen: bis 10,4x EBITDA bei großen
  Software-Unternehmen, gegenüber 2,4x bei kleinen Konsumgüterbetrieben** [F: DUB-/Exit-Coach-
  Multiples Q1/2026]. → Für Nicos Kriterium #8 „verkaufbarer Unternehmenswert" ist Software die
  mit Abstand beste Assetklasse.

**3. Was ist heute schlecht? (bester Beleg im Dokument für „veralteter Anbieter")**
- **Streit Software** wird kritisiert für „veraltete Benutzeroberfläche, verschachtelte
  Menüführung, lange Ladezeiten und Übertragungsfehler"; der Anbieter ist „seit über 40 Jahren
  am Markt, was erklärt, warum die Software als veraltet wahrgenommen wird" [F:
  Nutzerbewertungen via Suchergebnis-Zusammenfassung, 2026-08-05 – **Evidenzstufe 2**].
- Der Markt hat „sich in den vergangenen Jahren einem starken Wandel unterzogen" [F] → das
  Zeitfenster ist offen, aber es schließt sich.

**4. Was übernehmen wir?** Den Funktionsumfang, den die Branche seit 20 Jahren akzeptiert hat –
er ist ausdefiniert und muss nicht erfunden werden.

**5. Was verbessern wir?** Cloud, mobil, Preis öffentlich, Migration aus dem Altsystem als
Dienstleistung (der eigentliche Wechselblocker).

**6. Was kombinieren wir neu?** Software **+ betriebene Dienstleistung** (Terminierung aus
Modell 12, Prüfkoordination aus Modell 1). Reine Software ist ein harter Wettbewerb; Software mit
angehängter Leistung ist verteidigbar.

**7. Warum wechselt ein Kunde zu uns?**
*„Sie wechseln nicht wegen Funktionen – Sie haben alle. Sie wechseln, weil Ihr Meister zwei
Minuten pro Auftrag im Menü sucht und weil wir Ihre 8.000 Altdatensätze migrieren, ohne dass Sie
einen Finger rühren. Und weil Sie bei uns nicht nur die Software bekommen, sondern auch die
Leute, die Ihre Termine machen."*
Wechselgrund: **Migration wird uns überlassen + Software ist nicht das ganze Angebot.**

**8. Wiederkehrender Umsatz** SaaS-Abo pro Nutzer/Monat.

**9. Delegierbarkeit** Sehr hoch nach dem Produktaufbau; **niedrig davor** – Nico wäre 12–24
Monate Produktarchitekt. Das passt zu seiner „idealen Langfristrolle" (Nordstern Abschnitt 3),
kollidiert aber mit „Geschwindigkeit bis zum ersten Umsatz".

**10. Regulatorik-Ampel** 🟢 **Grün.**

**Warnung:** ≥24 Wettbewerber allein im Handwerkssegment [F]. Nur in einer **engen Nische**
(z. B. ausschließlich Prüfdienstleister) sinnvoll, nicht in der Breite.

---

### Modell 21 – Roll-up / Buy-and-Build von Prüf- und Wartungsbetrieben

**1. Modellname + realer Anbieter + URL**
Weber Building Group (Waterland-Portfolio, Berlin), Haustec Group (Findos Investor / Auctus
Capital Partners), E.GRUPPE (GIMV-Plattform), LET Group.
Quellen: heuking.de, dhi.zdh.de (Deutsches Handwerksinstitut, „Private Equity im deutschen
Handwerk"), mind-partners.com, deutsche-startups.de.

**2. Beweis der Nachfrage – sehr gut belegt**
- **Weber Building Group: rund 30 Add-on-Akquisitionen zwischen 2022 und 2025** [F:
  mind-partners.com, 2026-08-05].
- **E.GRUPPE konsolidiert seit 2021 systematisch Elektrotechnikunternehmen im DACH-Raum**,
  übernahm 2025 die LET Group [F].
- **Bewertungs-Multiples Handwerk SHK/Elektro im Roll-up: 5,0–7,0x**, mit einer **Prämie von
  ca. 1x, wenn wiederkehrende Wartungsumsätze über 30 % liegen** [F: mind-partners.com,
  2026-08-05]. **Diese Zahl ist strategisch die wichtigste im ganzen Dokument:** Der Markt zahlt
  messbar dafür, dass ein Handwerksbetrieb Wartungsverträge hat.
- „Buy-and-Build und Roll-up-Strategien haben 2025 den deutschen Transaktionsmarkt dominiert"
  [F: heuking.de].
- Das Deutsche Handwerksinstitut hat eine eigene Publikation zu Private Equity im Handwerk [F]
  → Phänomen ist institutionell anerkannt.

**3. Was ist heute schlecht?**
- Die Käufer sind **Finanzinvestoren**, die Betriebe kaufen und danach oft wenig verändern
  außer Einkauf und Buchhaltung [A].
- Kleinstbetriebe unter ~1 Mio. € Umsatz fallen durch das PE-Raster – **genau dort ist das
  Nachfolgeproblem am größten und der Wettbewerb um Zielunternehmen am geringsten** [S:
  abgeleitet aus den Search-Fund-Zielgrößen 5–50 Mio. € Umsatz [F] – alles darunter ist
  unbesetzt].

**4. Was übernehmen wir?** Die Roll-up-Mechanik: Plattform kaufen, Add-ons anhängen,
Zentralfunktionen (Vertrieb, Disposition, Software, Einkauf) bündeln, Multiple-Arbitrage
realisieren.

**5. Was verbessern wir?** Statt nur Einkauf und Buchhaltung zu zentralisieren:
**Die zugekauften Betriebe auf Abo-Wartungsverträge umstellen** – das hebt laut belegter Zahl
das Multiple um ca. 1x [F].

**6. Was kombinieren wir neu?** Roll-up **+ die Terminierungsmaschine aus Modell 12.**
Wer 6 Prüfbetriebe kauft und deren gemeinsame Fälligkeitsliste über eine zentrale
KI-Terminierung fährt, hebt die Technikerauslastung aller sechs gleichzeitig.

**7. Warum „wechselt" hier jemand?** Anderer Mechanismus: Der **Verkäufer** wechselt, nicht der
Kunde. Wechselgrund des Verkäufers: *„Sie sind 63, haben keinen Nachfolger, Ihre 180 Kunden
kennen Sie persönlich, und Sie wollen nicht, dass daraus nichts wird. Wir übernehmen den Betrieb,
behalten Ihre Leute und Ihre Marke, und Sie bleiben ein Jahr als Berater."*

**8. Wiederkehrender Umsatz** Kommt mit dem gekauften Betrieb sofort mit – **das ist der
entscheidende Vorteil gegenüber jedem Neuaufbau.**

**9. Delegierbarkeit** Hoch, wenn die gekauften Betriebe funktionierende Betriebsleiter haben –
und das ist bei Nachfolgesituationen oft **nicht** der Fall (der Inhaber **war** der Betrieb).
**Das ist das Kernrisiko: Man kauft nicht selten einen gut bezahlten Job – exakt das, was Nicos
Nordstern ausschließt (Punkt 5: „verkaufbar, nicht nur ein gut bezahlter Job").**

**10. Regulatorik-Ampel** 🟡 **Gelb** – erbt die Regulatorik der gekauften Betriebe
(Meisterpflicht in Anlage-A-Gewerken, Qualifikationsnachweise, ggf. VdS/ZÜS).
**Achtung Meisterpflicht:** In zulassungspflichtigen Handwerken (HwO Anlage A) braucht der
Betrieb einen eingetragenen Meister – der kann angestellt sein, muss aber vorhanden sein.

---

### Modell 22 – Franchise-/Lizenzsystem für Prüfdienstleistungen

**1. Modellname + realer Anbieter + URL**
In der Recherche **kein etabliertes Franchise-System für DGUV-V3-/Prüfdienstleistungen
gefunden** [F: gezielte Suche nach „Prüfdienstleister Franchise Lizenzsystem Partner werden"
lieferte ausschließlich normale Dienstleister, kein Franchise – „the search results do not
contain specific information about a franchise or licensing system"]. Gefundene Anbieter sind
klassische Unternehmen: GP Prüfservice, ESG (über 2.000 Kunden in 20+ Jahren [F]),
KFK Konrad (~100 Mitarbeiter bundesweit [F]), Piepenbrock, DGUV-V3.GmbH.

**2. Beweis der Nachfrage** Indirekt: Die Leistung ist bundesweit nachgefragt (siehe Modell 2),
aber die Erbringung ist **regional gebunden** (jemand muss hinfahren). Genau diese Konstellation
– bundesweite Nachfrage, lokale Erbringung, standardisierbare Leistung – ist die klassische
Franchise-Konstellation.

**3. Was ist heute schlecht?** Der Markt besteht aus Einzelkämpfern mit SEO-Domains, die jeweils
selbst Marketing, Software, Einkauf und Kalibrierung organisieren müssen.

**4. Was übernehmen wir?** Franchise-Mechanik aus anderen technischen Branchen.

**5. Was verbessern wir?** Der Partner bekommt: Marke, Leads, Software, Prüfgeräte im
Flottenmodell (Modell 16), Terminierung (Modell 12), Kalibrierungsservice. Er bringt: Fahrzeug,
Qualifikation, Arbeitszeit.

**6. Was kombinieren wir neu?** Franchise + zentrale KI-Terminierung + Geräte-Flotte. Die
Zentrale verkauft, der Partner erbringt.

**7. Warum wechselt jemand zu uns?** Zielgruppe ist der **Ein-Mann-Prüfdienstleister**:
*„Sie sind ein guter Prüfer und ein schlechter Verkäufer. Sie fahren 60 % Ihrer Zeit oder suchen
Kunden. Wir füllen Ihren Kalender und Sie zahlen uns einen Anteil vom Umsatz."*

**8. Wiederkehrender Umsatz** Lizenzgebühr + Umsatzanteil + Softwaremiete + Gerätemiete –
**vier wiederkehrende Ströme aus einem Partner.**

**9. Delegierbarkeit** Sehr hoch – die Zentrale hat keine Leistungserbringung, nur System.
**Das ist strukturell das am besten zu Nicos Nordstern passende Modell im Dokument**
(Kriterium #6, #7, #9: Marke, Prozesse, Lizenzen als Asset).

**10. Regulatorik-Ampel**
🟢 **Grün für die Zentrale** (keine Prüfqualifikation nötig, die hat der Partner).
🟡 **Gelb** wegen Franchiserecht: vorvertragliche Aufklärungspflicht, Scheinselbstständigkeits-
risiko bei zu enger Steuerung des Partners. Beides beherrschbar, aber anwaltlich zu gestalten.

**Warnung:** Franchise verkauft sich erst, wenn das System **bewiesen** ist. Man braucht 2–3
eigene, profitable Pilotbetriebe, bevor der erste Partner unterschreibt. Das ist ein
**Stufe-2-Modell**, kein Startpunkt.

---

## 5. Ausgeschiedene und abgewertete Kandidaten (Vollständigkeit)

| Modell | Grund für Abwertung |
|---|---|
| **14 – Externer Datenschutzbeauftragter** | Markt bereits software-first und preisaggressiv; Kriterium „Anbieter veraltet" nicht erfüllt |
| **11 – Klassischer Büroservice** | Personalintensives Callcenter; Kriterium #16 (Stunden gegen Geld) verletzt, wenn menschlich betrieben |
| **6 – Legionellenprüfung** | 3-Jahres-Zyklus zu schwach für MRR; Laborleistung akkreditierungspflichtig (🔴) |
| **18 – Hygieneservice** | Strukturell identisch zu Modell 17, keine eigenständige These |
| **8 – Aufzugswartung (Leistung selbst)** | Kapitalintensiv, Spezialistenmarkt, ZÜS-Prüfung 🔴 – nur Koordinationsvariante tragfähig |
| **Leitstellenbetrieb (in Modell 9)** | 24/7-Personalbetrieb; verletzt Nicos K.-o. #7/#8 – nur Reseller-Variante zulässig |

---

## 6. Sonderauftrag: Funktioniert der deutsche ETA-/Nachfolgemarkt?

### 6.1 Die belegten Zahlen

**Marktgröße des Problems**
- **ca. 186.000 Unternehmen** in Deutschland suchen im Zeitraum **2026–2030** eine Nachfolge
  [F: IfM Bonn, zitiert über nordvisory.de / newmittelstand.org, abgerufen 2026-08-05].

**Wie gut funktioniert der ETA-Kanal tatsächlich?**
- **ca. 10–15 neue Search Funds pro Jahr** in Deutschland; **44 europäische Akquisitionen**
  insgesamt [F: newmittelstand.org / ostreum.com, 2026-08-05].
- **Stanford-Studie:** In Deutschland wurden **bislang nur 10** Unternehmensnachfolgen über
  Search Funds realisiert – **Frankreich 15, Spanien 32** [F: zitiert über
  unternehmeredition.de / newmittelstand.org, 2026-08-05].
- 2025 wird als „Durchbruchsjahr" bezeichnet [F: newmittelstand.org] – **das ist
  Anbieter-Marketingsprache**, nicht Statistik. **10 Transaktionen kumuliert bei 186.000
  Nachfolgefällen sind kein funktionierender Markt, sondern eine Nische.** [S: 10 / 186.000
  ≈ 0,005 %]
- Ostreum listet **12 Unternehmer**, die 2025 auf das traditionelle Search-Fund-Modell setzen
  [F: ostreum.com, DACH-Raum].

**Typische Zielunternehmen im Search-Fund-Modell**
- **Umsatz 5–50 Mio. €, EBIT 1,5–5 Mio. €** [F: newmittelstand.org, 2026-08-05].
- **→ Das ist deutlich oberhalb dessen, was Nico ohne institutionelle Investoren finanzieren
  kann.** Bei 5x EBIT auf 1,5 Mio. € EBIT liegt der Kaufpreis bei **7,5 Mio. €** [S].

**Plattformen**
- **nexxt-change** (nexxt-change.org): größte deutsche Nachfolgebörse, **732 Regionalpartner**,
  **über 10.000 laufend aktualisierte Inserate**, **ca. 1.000 Vermittlungserfolge pro Jahr**,
  **19.000 erfolgreiche Vermittlungen seit 2006**; Registrierung kostenlos; getragen von DIHK,
  ZDH und KfW [F: nexxt-change.org / dihk.de / ihk.de, abgerufen 2026-08-05].
- **Bewertung:** 1.000 Vermittlungen bei über 10.000 Inseraten = **Erfolgsquote ca. 10 % pro
  Jahr** [S: 1.000 / 10.000]. Das ist ein **realer, funktionierender Kanal** – aber überwiegend
  für Kleinstbetriebe, nicht für Search-Fund-Größen.
- Weitere: DUB (Deutsche Unternehmerbörse, liefert die zitierten Multiples), firmenzukaufen.de,
  meetadam.io.

**Preise und Multiples (Micro-Cap, also Nicos realistisches Segment)**
- **Micro-Cap-Multiples im Schnitt über 20 DUB-Branchen: 4,1x–5,7x EBITDA** [F: exit-coach.de /
  DUB, Q1/2026].
- Gesamtspanne Q1/2026: **2,4x** (kleine Konsumgüterbetriebe) bis **10,4x** (große
  Softwareunternehmen) [F].
- **Handwerk SHK/Elektro im Roll-up: 5,0–7,0x, plus ca. 1x Prämie bei >30 % wiederkehrenden
  Wartungsumsätzen** [F: mind-partners.com].
- **Durchschnittlicher Kaufpreiswunsch im deutschen Mittelstand 2025: 499.000 €** (vor sechs
  Jahren 372.000 €, +34 % nominal) [F: zitiert über wassermann-nachfolge.com / exit-coach.de].
  **→ Diese Zahl ist für Nico die wichtigste des Abschnitts: Der typische deutsche
  Nachfolgebetrieb kostet rund eine halbe Million, nicht sieben Millionen.**

**Finanzierbarkeit**
- **KfW ERP-Förderkredit Gründung und Nachfolge (077)** [F: kfw.de]; **ERP-Kapital für Gründung
  bis 500.000 €**; ERP-Gründerkredit für Volumina über 500.000 € [F].
- KfW fördert Gründer, Nachfolger und Jungunternehmer, die **weniger als 5 Jahre** unternehmerisch
  tätig sind [F: kfw.de]. **Achtung: Nico führt bereits die Grunwald Finanzberatung – ob er die
  5-Jahres-Grenze erfüllt, ist offen und muss geprüft werden. [A]**
- **Belegter Finanzierungsmix:** Eigenkapital **10–30 %**, Bankdarlehen **50–70 %**,
  Verkäuferdarlehen **10–30 %**, plus Fördermittel (KfW, Bürgschaftsbank) und Earn-out
  [F: firmenzukaufen.de / hoeflmayr.de, 2026-08-05].

### 6.2 Rechnung: Ist das für Nico eine Abkürzung zu 100.000 €/Monat Umsatz?

**Szenario A – Ein Betrieb, gekauft**

Ziel: **1,2 Mio. € Jahresumsatz** (= 100.000 €/Monat, Nordstern-Zwischenziel).

| Position | Wert | Kennung |
|---|---|---|
| Zielumsatz | 1.200.000 €/Jahr | [F: Nordstern] |
| Realistische EBIT-Marge Prüf-/Wartungsbetrieb | 10–15 % | [A] |
| Daraus EBIT | 120.000–180.000 €/Jahr | [S] |
| Multiple Micro-Cap | 4,1–5,7x EBITDA | [F: DUB Q1/2026] |
| **Kaufpreis** | **ca. 500.000–1.000.000 €** | [S: 120–180 T€ × 4,1–5,7] |
| Eigenkapitalanteil 10–30 % | **50.000–300.000 €** | [S: aus belegtem Mix] |
| Verkäuferdarlehen 10–30 % | 50.000–300.000 € | [F: Mix] |
| Bank/KfW 50–70 % | 250.000–700.000 € | [F: Mix] |

**Plausibilitätsprüfung gegen den Markt:** Der durchschnittliche Kaufpreiswunsch von **499.000 €**
[F] liegt exakt in dieser Spanne. Die Rechnung ist konsistent.

**Ergebnis Szenario A:** Ein Betrieb mit 1,2 Mio. € Umsatz ist für **ca. 50.000–300.000 €
Eigenkapital** erreichbar. Das 100.000-€-Umsatzziel wäre am **Tag des Closings** erreicht statt
in 24–48 Monaten.

**ABER – die drei Haken, die diese Rechnung entwerten:**

1. **Der Gewinn reicht nicht.** Das Nordstern-Dokument rechnet vor: 30.000 €/Monat netto privat
   erfordern **ca. 690.000–720.000 € Vorsteuergewinn pro Jahr** [F: Nordstern Abschnitt 2]. Ein
   gekaufter 1,2-Mio-€-Betrieb liefert 120.000–180.000 € EBIT [S] – **davon geht zunächst der
   Kapitaldienst ab.** Bei 700.000 € Fremdkapital, 5 % Zins und 8 Jahren Tilgung sind das
   **ca. 105.000 €/Jahr Kapitaldienst [S: 700.000/8 + 700.000×0,05×0,5 ≈ 87.500 + 17.500]**.
   **Es bleibt praktisch nichts.** Der Kauf bringt Umsatz, aber **kein ausschüttbares Einkommen**
   in den ersten Jahren.
2. **Man kauft oft den Job des Vorgängers.** In Betrieben dieser Größe **ist der Inhaber der
   Betrieb**: Er hat die Kundenbeziehungen, er kalkuliert, er führt. Genau das verletzt Nicos
   K.-o. #1 („Nico muss nach 24 Monaten noch zwingend Hauptleistungserbringer sein") und den
   Nordstern-Punkt 5.
3. **Nicos Anti-Liste kollidiert frontal mit dem Alltag eines Kleinbetriebs:** „bei jedem
   Mitarbeiterproblem eingebunden sein", „operatives Tagesgeschäft persönlich kontrollieren"
   – das **ist** die Arbeit eines neuen Inhabers eines 10-Mann-Betriebs in den ersten zwei Jahren.

**Szenario B – Search Fund mit Investoren**

Zielgröße 5–50 Mio. € Umsatz [F], Kaufpreise im einstelligen Millionenbereich, finanziert durch
ein Investorenkonsortium. **Realistisch für Nico? Nein, jedenfalls nicht kurzfristig.**
Search-Fund-Investoren finanzieren typischerweise Absolventen von Top-MBA-Programmen mit
strukturiertem Suchprozess und 18–24 Monaten Vollzeit-Suche ohne Einkommen [A – Kernmechanik des
Modells, in dieser Recherche nicht im Detail belegt]. Bei **kumuliert 10 realisierten
Transaktionen in Deutschland** [F] ist der Kanal zudem schlicht zu dünn, um darauf zu planen.

**Szenario C – Der Hybrid (die eigentliche Empfehlung)**

Nicht „bauen ODER kaufen", sondern: **klein kaufen, um Zugang zu kaufen.**

Ein **Kleinstbetrieb mit 300.000–600.000 € Umsatz** (z. B. ein Feuerlöscher-/Prüfbetrieb mit
180 Bestandskunden und Inhaber kurz vor Rente) kostet nach Micro-Cap-Multiples und dem belegten
durchschnittlichen Kaufpreiswunsch **ca. 100.000–250.000 €** [S: abgeleitet aus 4,1–5,7x auf
30–50 T€ EBIT, plausibilisiert am 499.000-€-Durchschnitt für größere Fälle].

Was man dafür bekommt:
- eine **bestehende Kundenliste mit gesetzlich wiederkehrenden Fälligkeiten** – der teuerste und
  langsamste Teil jedes Neuaufbaus,
- die **Qualifikationen/Zulassungen** im Betrieb (löst die 🟡-Ampeln der Modelle 2–5 durch Zukauf
  statt durch Aufbau),
- sofortigen Cashflow ab Monat 1.

Und darauf setzt man die **eigene Maschine** (Modelle 1, 12, 22): Software, KI-Terminierung,
Bündelung, dann Franchise oder weitere Zukäufe.

**Das ist die einzige Konstellation, in der der ETA-Weg Nicos Nordstern dient statt ihm zu
widersprechen** – weil das gekaufte Unternehmen nicht das Ziel ist, sondern der **Rohstoff**.

---

## 7. Wichtigste offene Rechercheaufträge (Priorität für Folgeagenten)

1. **Marktgrößen fehlen durchgehend.** Für DGUV V3, Regalprüfung, Torprüfung, Brandschutz und
   Prüfsoftware konnte **keine einzige Marktvolumen-Zahl** verifiziert werden. Ohne diese Zahlen
   ist keine Aussage über die Erreichbarkeit von 1,2 Mio. €/Jahr möglich.
2. **Bewertungsbelege fehlen (Evidenzstufe 1).** Trustpilot, OMR, Capterra, Google Reviews waren
   nicht direkt abrufbar. Die Aussagen zu ebuero und Streit Software sind Zweithand.
3. **Modell-12-Nachfrage ist nur abgeleitet.** Vor jeder Investition: 20 Prüfdienstleister
   telefonisch befragen (Nico kann das selbst, mit seinem eigenen Stack).
4. **UWG-§7-Frage für Bestandskunden-Terminierung** – anwaltlich klären, geschäftsentscheidend.
5. **KfW-5-Jahres-Grenze** für Nico prüfen (bestehende Unternehmertätigkeit).
6. **Negativbefund härten:** Dass die Kombination „Prüfpflicht + Software + KI-Outbound" nicht
   existiert, beruht auf 3 Suchen. Mit 10+ weiteren Suchen absichern, bevor darauf gebaut wird.

---

## 8. Quellenverzeichnis

**Telefon-/Büroservice und KI-Telefonie**
- [ebuero Preisverzeichnis Telefonsekretariat](https://www.ebuero.de/preisverzeichnis/telefonsekretariat)
- [ebuero Test 2026: Preise & Erfahrungen (telefon.services)](https://telefon.services/ebuero/)
- [Bewertungen zu ebuero AG (Trustpilot)](https://de.trustpilot.com/review/ebuero.de)
- [Starbüro Telefonservice Preisvergleich](https://www.starbuero.de/preisvergleich)
- [Externer Telefonservice im Selbsttest (legal-tech.de)](https://legal-tech.de/externer-telefonservice-im-selbsttest/)
- [KI Telefonassistent: Die 12 besten Anbieter (Superchat)](https://www.superchat.de/blog/bester-ki-telefonassistent-preise-funktionen)
- [KI-Telefonassistent Made in Germany: Vergleich 2026 (ruflab)](https://www.ruflab.com/blog/ki-telefonassistent-made-in-germany-anbieter-vergleich-2026)
- [Beste KI-Telefonassistenten 2026 (Vokaro)](https://vokaro.net/blog/beste-ki-telefonassistenten-deutschland-2026)
- [KI Telefonassistent Vergleich (Placetel)](https://www.placetel.de/ratgeber/ki-telefonassistent)

**Prüf- und Wartungspflichten**
- [DGUV V3 – Deutscher Prüfdienst](https://www.deutscher-pruefdienst.de/dguv-v3/)
- [GP Prüfservice DGUV V3](https://www.gp-pruefservice.de/leistungen/dguv-v3-pruefung)
- [ESG Gesellschaft DGUV V3](https://www.esg-gesellschaft.de/)
- [KFK Konrad Elektroprüfungen](https://www.pruefservice-kfk.de/dienstleistungen-pruefungen/elektropruefungen/elektropruefungen-europaweit/)
- [Deutscher Prüfservice / DGUV-V3.GmbH](https://deutscher-pruefservice.de/)
- [Regalprüfung nach DIN EN 15635 (123ingenieure)](https://123ingenieure.de/regalpruefung/)
- [Regalprüfung Bonnema](https://bonnema.de/dienstleistungen/regalpruefung)
- [Rolltore & Türen Prüfung nach ASR A1.7 (PrüfAssist)](https://www.xn--prfassist-r9a.de/leistungen/rolltore-tueren-pruefung)
- [Fox Tortechnik – UVV/BGR232/ASR A1.7 (HTTP-Seite)](http://www.fox-tortechnik.de/info%20uvv%20pruefung%20und%20wartung%20bgr232,asr%20a1.htm)
- [APS Prüfdienste – kraftbetätigte Türen und Tore](https://www.aps-pruefdienste.de/sicherheit-und-wartung-von-kraftbetatigten-turen-und-toren-gemass-asr-a1-7)
- [Feuerlöscher Wartung DIN 14406 (Jockel)](https://www.jockel-brandschutz.de/tragbare-feuerloescher)
- [bvbf – Instandhaltung und Prüfung](https://www.bvbf-brandschutz.de/brandschutz-unternehmen/asr-a2-2-massnahmen-gegen-braende/wartung-und-pruefung-1/arbeitsstaettenregel-asr-a2-2-wartung-und-pruefung)
- [RWA-Anlage Wartung: Kosten & Fristen 2026 (brandschutzfinder)](https://brandschutzfinder.de/ratgeber/rwa-anlage-wartung/)
- [Minimax Mobile – Wartung RWA](https://www.minimax-mobile.com/dienstleistungen-produkte/dienstleistungen/instandhaltung-service/wartung-rauch-und-waermeabzuege/)
- [RWA-Prüfpflichten (Cloudbrixx)](https://cloudbrixx.de/rauch-und-waermeabzugsanlage-rwa-pruefpflichten/)
- [Aufzug TÜV Prüfung Kosten & Pflichten (SVEAG)](https://www.sveag.de/news/aufzug-tuev-pruefung-kosten-pflichten-fristen-hausverwaltungen)
- [TK Elevator – Wartungsintervalle](https://www.tkelevator.com/de-de/blog/wie-oft-muss-ein-aufzug-gewartet-werden.html)
- [§ 74 GEG – gesetze-im-internet.de](https://www.gesetze-im-internet.de/geg/__74.html)
- [BBSR GEG-Infoportal – Inspektion von Klimaanlagen](https://www.bbsr-geg.bund.de/GEGPortal/DE/Archiv/GEG/GEG2020/InspektionVon/Klimaanlagen-node.html)
- [Die novellierte F-Gase-Verordnung (BFS Kälte-Klima, PDF)](https://www.bfs-kaelte-klima.de/fileadmin/DATEIEN/Download/Merkblaetter/Die_novellierte_F-Gase-Verordnung-12-24.pdf)
- [F-Gase-Verordnung EU 2024/573 – neue Betreiberpflichten (Roter Kältetechnik)](https://www.roter-kaeltetechnik.de/f-gase-verordnung-eu2024573-neu-betreiberpflichten/)
- [Trinkwasserverordnung und Legionellen (BMG, PDF)](https://www.bundesgesundheitsministerium.de/fileadmin/Dateien/3_Downloads/T/Trinkwasserverordnung/Stammtext_TrinkwV_und_Legionellen.pdf)
- [Legionellenprüfung (Techem)](https://www.techem.com/de/de/immobilienservices/legionellenpruefung)
- [Trinkwasseranalyse (TÜV SÜD)](https://www.tuvsud.com/de-de/branchen/gesundheit-und-medizintechnik/arbeits-gesundheitsschutz/mikrobiologisches-monitoring-firmenkunden/trinkwasseranalyse)

**Software / Betreiberpflichten**
- [HOPPE Prüfplaner](https://www.hoppe-net.de/Pruefplaner.htm)
- [Wartungsplaner – Prüfmanager](https://www.wartungsplaner.de/details/Pruefmanager.htm)
- [Software für Prüfpflichten im Vergleich (mybuilding24)](https://mybuilding24.com/software-fuer-pruefpflichten-im-vergleich/)
- [Fraunhofer IFF – Prüf-App ELISA](https://www.iff.fraunhofer.de/de/geschaeftsbereiche/logistik-fabriksysteme/pruef-app-elisa.html)
- [RISK-Project SERVO](https://www.risk-project.de/servo-wartung-und-pruefwesen)
- [Certado Suite für Prüfdienstleister](https://www.certado.io/pruefdienstleister/)
- [MS Consulting – ERP für Prüfdienstleister (Vemas)](https://msconsulting.de/branchenloesungen/pruefdienstleister)
- [firstaudit – digitale Prüfprotokolle](https://www.firstaudit.de/digitale-pruefprotokolle/)
- [GEFMA 190 Betreiberverantwortung 2.0](https://www.gefma.de/positionieren/news-aus-dem-fm/news-detailansicht/neuauflage-der-gefma-190-betreiberverantwortung)
- [Betreiberverantwortung im FM (Planon)](https://planonsoftware.com/de/glossar/betreiberverantwortung-facility-management/)
- [Handwerkersoftware Vergleich – 24 Anbieter](https://handwerker-software.org/article/08-erfahrungen-mittelstand)
- [Handwerkersoftware bei Capterra Deutschland](https://www.capterra.com.de/directory/31305/handyman/software)

**Arbeitssicherheit / Datenschutz / Unterweisung**
- [Kosten externe Fachkraft für Arbeitssicherheit (123ingenieure)](https://123ingenieure.de/arbeitssicherheit/fachkraft-fuer-arbeitssicherheit/)
- [Externe Fachkraft für Arbeitssicherheit finden & vergleichen (safest)](https://safest.gmbh/fachkraft-arbeitssicherheit)
- [Sicherheitstechnische Betreuung (arbeitssicherheit-fachkraft.de)](https://arbeitssicherheit-fachkraft.de/sicherheitstechnische-betreuung/)
- [Externer Datenschutzbeauftragter Kosten (keyed)](https://keyed.de/blog/datenschutzbeauftragter-kosten/)
- [Externer Datenschutzbeauftragter Kosten (fraghugo)](https://www.fraghugo.de/externer-datenschutzbeauftragter-kosten/)
- [WEKA E-Learning Arbeitsschutz-Unterweisungen](https://www.weka-elearning.de/betriebliche-unterweisungen/arbeitsschutz/)
- [Unterweisungsmanager im Vergleich (digital-affin)](https://www.digital-affin.de/blog/unterweisungsmanager-vergleich/)

**Abo-/Servicemodelle**
- [Hilti Fleet Management](https://www.hilti.group/content/hilti/CP/XX/en/services/tool-services/fleet-management.html)
- [Hilti Fleet Management (A) – Harvard Business School](https://www.hbs.edu/faculty/Pages/item.aspx?num=52550)
- [Hilti Business Model Navigator](https://businessmodelnavigator.com/case-firm?id=45)
- [MEWA Textil-Service SE – Northdata](https://www.northdata.com/MEWA%20Textil-Service%20SE,%20Wiesbaden/HRB%2033491)
- [CWS Hygiene Deutschland](https://www.cws.com/de-DE/hygiene/ueber-uns/cws-hygiene-deutschland-gmbh-co-kg)
- [Hagleitner Hygiene Deutschland](https://www.wer-zu-wem.de/firma/hagleitner-de.html)
- [Alarmaufschaltung Leitstelle – Kosten (Secplan)](https://www.secplan.de/blog/alarmaufschaltung-mehr-sicherheit-durch-den-anschluss-an-eine-leitstelle)
- [Kosten der Aufschaltung zur Leitstelle 2026 (ACC)](https://accsicherheitstechnik.de/wie-hoch-sind-kosten-der-aufschaltung-zur-leitstelle-2026/)
- [Notrufe24 – Leistungen und Preise](https://www.notrufe24.de/leistungen-preise)
- [Photovoltaik Wartung Kosten (solaranlage-ratgeber)](https://www.solaranlage-ratgeber.de/photovoltaik/photovoltaik-wartung/photovoltaik-wartung-kosten)
- [PV Wartungsvertrag Vergleich (pv-montagefirmen)](https://pv-montagefirmen.de/ratgeber/langfristige-betreuung-wartung/pv-wartungsvertrag-vergleich/)
- [Cleanwatt Servicevertrag PV](https://cleanwatt.de/servicevertrag-fuer-photovoltaikanlagen/)

**ETA / Nachfolge / M&A**
- [nexxt-change – Über die Börse](https://www.nexxt-change.org/DE/Service/Ueber-die-Boerse/ueber-die-Boerse)
- [DIHK – Unternehmensbörse nexxt-change](https://www.dihk.de/de/themenfelder/unternehmensentwicklung/unternehmensnachfolge-finden-oder-anbieten-die-unternehmensboerse-nexxt-change-159682)
- [Unternehmen kaufen statt gründen: Search Fund & ETA (New Mittelstand)](https://www.newmittelstand.org/unternehmen-kaufen-statt-grunden)
- [Search Fund Übersicht 2025 DACH (Ostreum)](https://www.ostreum.com/blog/traditionelle-search-funds-in-deutschland-osterreich-schweiz)
- [Search Funds als Nachfolgelösung im Mittelstand (Unternehmeredition)](https://www.unternehmeredition.de/search-funds-als-nachfolgeloesung-im-mittelstand/)
- [Entrepreneurship Through Acquisition (Everest-X)](https://everest-x.de/empower-blog/eta/)
- [Unternehmensnachfolge im Mittelstand (Nordvisory)](https://www.nordvisory.de/insights/unternehmensnachfolge-mittelstand)
- [EBITDA Multiples 2026 nach Branche & Größe (Exit Coach)](https://exit-coach.de/ebitda-multiples/)
- [KMU-Multiples 2025-Q1 (Wassermann Nachfolge)](https://www.wassermann-nachfolge.com/post/kmu-multiples-2025-q1)
- [EBIT Multiples Benchmarks (meetadam.io)](https://meetadam.io/benchmarks/ebit-multiples/)
- [KfW ERP-Förderkredit Gründung und Nachfolge (077)](https://www.kfw.de/inlandsfoerderung/Unternehmen/Gr%C3%BCndung-und-Nachfolge/F%C3%B6rderprodukte/ERP-F%C3%B6rderkredit-Gr%C3%BCndung-und-Nachfolge-(077)/)
- [Firma kaufen mit wenig Eigenkapital (Firmenzukaufen)](https://www.firmenzukaufen.de/blog/firma-kaufen-mit-wenig-eigenkapital-finanzierungsstrategien)
- [Nachfolge finanzieren: KfW, Bank, Eigenkapital, Verkäuferdarlehen (Höflmayr)](https://hoeflmayr.de/nachfolge-finanzieren-kfw-bank-eigenkapital)
- [Buy-and-Build / Roll-ups (Heuking)](https://www.heuking.de/en/news-events/newsletter-articles/detail/buy-and-build-roll-ups.html)
- [Private Equity im deutschen Handwerk (Deutsches Handwerksinstitut)](https://dhi.zdh.de/dhi-news/aktuelle-veroeffentlichungen/private-equity-im-deutschen-handwerk/)
- [Elektrotechnik & M&A: Multiples und Roll-ups (MIND Partners)](https://www.mind-partners.com/market-insights/elektrotechnik-im-mittelstand-m-a-trends-fur-schaltanlagenbauer-und-elektroinstallationsbetriebe)
- [Roll-ups – die neue Goldgrube der Startup-Szene (deutsche-startups.de)](https://www.deutsche-startups.de/2026/05/18/roll-ups-die-neue-goldgrube-der-startup-szene/)
