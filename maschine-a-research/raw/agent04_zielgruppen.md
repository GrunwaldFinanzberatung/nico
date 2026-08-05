# Agent 04 – Zielgruppen- und Problemanalyse (Deutschland, B2B)

Stand: 2026-08-05 · Agent 4 · Status: Rohdaten für Konsolidierung
Kennzeichnung nach 01_nordstern: **[F]** Fakt (Quelle) · **[S]** Schätzung (Rechenweg offen) · **[A]** Annahme (unsicher, Bandbreite)

---

## 0. Methodenhinweis und Ehrlichkeitsvermerk (bitte zuerst lesen)

### 0.1 Recherche-Einschränkung dieser Session
Das Websuche-Kontingent der Session (200 Anfragen, sessionweit von allen 12 Agenten
geteilt) war nach meinen Suchläufen erschöpft; direkter HTTPS-Egress ist im Container
durch das Gateway gesperrt (CONNECT → 403 für alle getesteten Hosts). Deshalb gilt:

- Alle **[F]**-Zahlen unten stammen aus in dieser Session tatsächlich durchgeführten
  Suchen mit benannter Primär- oder Verbandsquelle.
- Wo eine Betriebszahl **nicht** in dieser Session verifiziert werden konnte, steht
  ausdrücklich **[A] – in dieser Session nicht verifiziert** mit Bandbreite. Diese
  Zahlen sind vor Verwendung in der Endempfehlung nachzuprüfen.
- Ich habe bewusst **keine** Zahl aus dem Gedächtnis als [F] ausgegeben.

### 0.2 Quellenkritik: „Verpasste Anrufe" ist ein vermintes Feld
Die kursierenden Zahlen („30 % aller Handwerker-Anrufe gehen verloren",
„40–60 % unbeantwortet", „62 % bei kleinen Dienstleistern", „80–85 % sprechen nicht
aufs Band", „bis zu 96.000 € Umsatzverlust/Jahr") stammen **ausschließlich von
Anbietern von KI-Telefonassistenten** (agentino.de, telewa.de, vokaro.net,
easy-kiagentur.de, klickautomation.com, digitalolymp.ch, servasbot.at) – also von
Parteien mit unmittelbarem Verkaufsinteresse. **Keine dieser Zahlen ist auf eine
Primärstudie, ein Institut oder einen Verband rückführbar.** Sie werden in diesem
Dokument **nicht** als [F] verwendet.

Konsequenz: Ich rechne durchgehend mit **konservativ halbierten Annahmen**
(Nichtannahmequote 15–25 % statt 30–60 %, Verlustquote 40–55 % statt 80–85 %).
Wer den Marktangriff plant, muss diese Quote **selbst messen** (Call-Tracking bei
5–10 Pilotbetrieben über 4 Wochen) – das ist der billigste und wichtigste
Validierungsschritt des gesamten Projekts.

Belastbar ist dagegen nur ein Datenpunkt aus dem Gesundheitsbereich: eine
Kleintierpraxis mit 2 Tierärzten erhält **60–120 Anrufe/Tag** [S, Branchenmedium],
und eine hausärztliche Praxis **100–200 Anrufe/Tag**, konzentriert auf die ersten
zwei Öffnungsstunden [S, Branchenmedium]. Das Anrufaufkommen selbst ist plausibel
belegt – die Verlustquote nicht.

### 0.3 Die vier Schadensmodelle
Alle Euro-Schäden unten folgen einem von vier offengelegten Modellen:

**M1 – Verpasste Erstanfrage (Umsatzverlust)**
```
Schaden = A × T × u × n × v × c × W
A = eingehende Anrufe je Arbeitstag
T = Arbeitstage/Jahr (220 Handwerk, 250 Handel/Service)
u = Anteil unbeantwortet
n = Anteil echte Neuanfragen an den unbeantworteten
v = Anteil, der endgültig verloren geht (kein Rückruf, Wettbewerber)
c = Abschlussquote auf qualifizierte Neuanfrage
W = durchschnittlicher Auftragswert (netto)
→ Ergebnis = entgangener Umsatz. Für den Gewinn: × Deckungsbeitragsquote DB
```

**M2 – Administrativer Zeitverlust (Kostenschaden)**
```
Schaden = h × T × K       h = Stunden/Tag unproduktive Admin-Arbeit
                          K = Vollkostensatz (Büro 40–48 €/h, Meister/Inhaber 75–95 €/h) [A]
```

**M3 – Terminausfall / No-Show (Deckungsbeitragsverlust)**
```
Schaden = Ausfälle/Woche × 46 × Ausfalldauer(h) × DB je Behandlungsstunde × (1 − Nachbelegungsquote)
```

**M4 – Nicht besetzbare Kapazität (entgangene Marge durch Personalmangel)**
```
Schaden = fehlende Vollzeitkraft × Umsatz je Kraft/Jahr × DB-Quote
```

### 0.4 Der wichtigste Befund vorweg: das Konzentrationsproblem
Bei realistischen Handwerks-ARPUs von 200–350 €/Monat braucht Maschine A für
**100.000 € MRR zwischen 285 und 500 Kunden** [S]. Das kollidiert frontal mit
Pflichtkriterium 5 („wenige hochwertige Kunden statt hunderte Kleinkunden") und
mit Nicos Anti-Kriterien (täglicher Kundensupport, ständige Kundenberatung).
Zielgruppen mit ARPU ≥ 800 €/Monat (Autohäuser, Hausverwaltungen, Kanzleien,
Speditionen, FM-Dienstleister, Dentalgruppen) erreichen dasselbe Ziel mit
**60–125 Kunden**. Diese Unterscheidung dominiert das Ranking in Abschnitt 3
stärker als die reine Problemstärke.

---

## 1. Belegte Rahmendaten zur Zahlungsbereitschaft (kritischer Teil)

Der Auftrag verlangt ausdrücklich Belege **für oder gegen** die These
„deutsche Handwerksbetriebe sind preissensibel und digital zurückhaltend".
Ergebnis: **Die These wird durch die Daten überwiegend bestätigt.**

### 1.1 Belege GEGEN hohe Zahlungsbereitschaft im Handwerk

| Befund | Wert | Quelle |
|---|---|---|
| KI wird im Handwerk eingesetzt | **4 %** der Betriebe | Bitkom/ZDH-Studie 2025, n=504 Betriebe ab 1 Beschäftigten, telefonisch, KW 23–29/2025 [F] |
| KI konkret geplant | **9 %** | ebd. [F] |
| Betriebe mit Mitarbeitenden, die mit KI umgehen können | **29 %** | ebd. [F] |
| „Hohe Investitionen schrecken ab" | **69 %** | ebd. [F] |
| Sorge: „KI/Software gibt bald vor, wie wir arbeiten müssen" | **52 %** | ebd. [F] |
| Selbsteingeschätzter Digitalisierungsgrad | Schulnote **3,0** | ebd. [F] |
| Digitalisierungsausgaben des Mittelstands gesamt 2024 | **23,8 Mrd. €** | KfW-Digitalisierungsbericht Mittelstand 2025 [F] |
| Anteil Kleinstunternehmen (< 5 Besch.) an den Digitalisierern | **73 %** | ebd. [F] |
| … deren Anteil an den Digitalisierungs**ausgaben** | nur **24 %** | ebd. [F] |
| Anteil großer Mittelständler (≥ 50 Besch.) an Unternehmen / an Ausgaben | **2 % / 41 %** (9,2 Mrd. €) | ebd. [F] |
| Trend: Ausgabenanteil der Kleinen | 2016 noch 31 % → 2024 nur 24 % | ebd. [F] – die Schere **öffnet** sich |

**Ableitung [S]:** 24 % von 23,8 Mrd. € = 5,71 Mrd. € entfallen auf Kleinstbetriebe.
Nimmt man an, dass rund 900.000 Kleinstunternehmen Digitalisierungsprojekte
durchführen [A, Bandbreite 700.000–1.100.000], ergibt sich ein
**Digitalisierungsbudget von ca. 5.200–8.200 € pro Kleinstbetrieb und Jahr,
also 430–680 €/Monat – für ALLES zusammen**: Hardware, Website, Warenwirtschaft,
Handwerkersoftware, IT-Dienstleister, Schulung.

Das ist die harte Grenze. Ein einzelner Anbieter, der 500 €/Monat verlangt, fordert
das **gesamte** Digitalisierungsbudget eines Kleinstbetriebs. Realistisch abschöpfbar
sind **10–30 % dieses Budgets**, also **45–200 €/Monat bei Betrieben < 5 Mitarbeitern**
und – über Personalkostenersparnis argumentiert – **200–450 €/Monat bei Betrieben
mit 10–50 Mitarbeitern** [S].

### 1.2 Belege FÜR eine vorhandene, aber gedeckelte Zahlungsbereitschaft

Betriebe zahlen bereits heute monatlich – die Preisanker sind öffentlich und niedrig:

| Kategorie | Belegte Marktpreise | Quelle |
|---|---|---|
| Handwerkersoftware allgemein | **15–120 € pro Nutzer/Monat** | Marktvergleiche 2026 (trusted.de, gruenderkueche.de) [F] |
| HERO Starter / Pro | 29 € / 39 € netto pro Nutzer/Monat | Anbieterpreise [F] |
| Meisterwerk | ab 15 € pro Nutzer/Monat | Anbieterpreise [F] |
| Lexware Handwerk | 26,40 € – 66,90 €/Monat | Anbieterpreise [F] |
| Bosch OfficeOn | ab 49,99 €/Monat | Anbieterpreise [F] |
| Telefonsekretariat, typische Monatsrechnung | **50–250 €/Monat** | Marktübersicht [F] |
| phonea (Handwerkertarif) | 1,70 €/Anruf; 1,40 € bei fester Abnahme | Anbieterpreisseite [F] |
| phonea 24/7-Aufpreis | **29,50 €/Monat** | Anbieterpreisseite [F] |
| Mobile Office | 79 € (Business) / 99 € (Professional) + 1,09–1,29 €/Min | Anbieterpreisseite [F] |
| officehelden | 0,54 € pro Bearbeitungsminute | Anbieterpreisseite [F] |
| cloudsecretary | ab 0,99 € pro angenommenem Anruf | Anbieterpreisseite [F] |

**Interpretation:** Es existiert ein funktionierender Markt für ausgelagerte
Anrufannahme im Handwerk – aber zu **Preisen von 50–250 €/Monat**. Das ist der
Referenzpreis, an dem jedes neue Angebot gemessen wird. Ein Preis von 500 €/Monat
muss gegen einen etablierten 99-€-Anker verteidigt werden. Das geht nur mit
Leistungen, die das Telefonsekretariat **nicht** kann (Kalendereinsteuerung in die
Einsatzplanung, Angebots-/Auftragsanlage im Fachsystem, Rückrufkampagnen,
Bestandskunden-Reaktivierung, Wartungsvertrags-Verkauf) – nicht mit „aber unseres
ist KI".

### 1.3 Belege für die Gegenrichtung: wo Budget nachweislich da ist

| Befund | Wert | Quelle |
|---|---|---|
| Immobilienverwaltungen, die hohe Mittel in Automatisierung stecken | **knapp 80 %**, KI „ganz oben auf der Agenda" | VDIV Branchenbarometer 2025 [F] |
| Geplante Preisanpassungen der WEG-Verwaltungen 2025 | **+ ca. 12 %**, kleine Objekte bis **+17 %** | ebd. [F] – Kostensteigerungen sind **weitergebbar** |
| Erwartetes Umsatzplus der Verwaltungen bis Ende 2025 | **+7,8 %** | ebd. [F] |
| Arztpraxen mit Online-Terminvereinbarung | **40 %** | KBV/IGES PraxisBarometer Digitalisierung 2025, n=1.700 [F] |
| Arztpraxen mit Online-Rezeptbestellung | **45 %** | ebd. [F] |
| Zufriedenheit eRezept / eAU (Anstieg) | 63 → **77 %** / 69 → **78 %** | ebd. [F] |

**Kernunterschied:** Immobilienverwaltungen und Praxen können Kostensteigerungen
**an Dritte weiterreichen** (Eigentümergemeinschaft, Selbstzahlerleistungen) oder
haben sie bereits eingepreist. Der SHK-Meister kann das nicht – er konkurriert im
Stundensatz. **Weitergebbarkeit der Kosten ist der beste Einzelprädiktor für
Zahlungsbereitschaft** und schlägt Problemstärke.

### 1.4 Timing-Signal 2025/26: das Fenster öffnet sich gerade
Bis 2023 war das Problem der Handwerksbetriebe „zu viele Anfragen" – da war ein
verpasster Anruf eine Erleichterung, kein Schaden. Diese Lage hat sich gedreht:

| Branche | Entwicklung | Quelle |
|---|---|---|
| SHK-Handwerk | Umsatz **−4 %** 2024 (61,9 → 59,12 Mrd. €), 2025 ca. −1 % nominal erwartet; „spürbare Abkühlung, rückläufige Aufträge, sinkende Kapazitätsauslastung" | ZVSHK [F] |
| E-Handwerke | **−4 %** Umsatz 2024; 2025 „Jahr der Stagnation" | ZVEH [F] |
| Dachdeckerhandwerk | Umsatz 2025 **13,5 Mrd. € (0,0 %)** bei ca. **+4,5 %** Preissteigerung → **real negativ** | ZVDH [F] |
| PV-Installateure | „Volle Auftragsbücher aus dem Boomjahr 2023 abgearbeitet – Nachfrage nach Neuaufträgen bleibt aus" | Branchenmonitor 2025 [F] |
| GaLaBau | **+4,3 %** auf 11,11 Mrd. €, 16. Wachstumsjahr in Folge | BGL [F] – **Gegenbeispiel** |

**Konsequenz:** Ein „Wir verlieren keine Anfrage mehr"-Angebot ist 2026 verkaufbar,
war es 2022 nicht. Umgekehrt sinkt in einer Abschwungphase die Investitionsneigung.
Das ist ein **Zielkonflikt**, kein reiner Rückenwind – und ein Grund, den Pitch auf
**Personalkostenersparnis** (funktioniert in beiden Konjunkturlagen) statt auf
Umsatzsteigerung zu stellen.

---

## 2. Zielgruppenanalyse (22 Zielgruppen)

Gesamtrahmen: **1.038.126 Betriebe** in Handwerksrolle und Verzeichnis
handwerksähnlicher Gewerbe, **783,2 Mrd. € Umsatz 2025** (ohne USt.)
– ZDH, Kennzahlen des Handwerks 2025 [F].

---

### ZG 01 – SHK-Betriebe (Sanitär, Heizung, Klima)

**1. Branche + Anzahl**
**48.050 Betriebe** (2024, leichter Rückgang von 48.300) – ZVSHK-Jahresbilanz [F].
Für 2025 nennt der ZVSHK „rund 48.000 Betriebe" [F].

**2. Größe / Umsatz / Mitarbeiter**
Branchenumsatz **59,12 Mrd. €** (2024, −4 %), **390.000 Beschäftigte** – ZVSHK [F].
Rechnerisch: **1,23 Mio. € Umsatz je Betrieb**, **8,1 Mitarbeiter je Betrieb** [S].
Der Median liegt deutlich darunter – die Verteilung ist rechtsschief; typischer
Zielkunde: **5–25 Mitarbeiter, 600 T€ – 3 Mio. € Umsatz** [A].

**3. Entscheider**
Inhaber/Handwerksmeister, Alter **48–60** [A], entscheidet allein und schnell,
oft abends nach der Baustelle. Digitalaffinität niedrig bis mittel: Handwerk gesamt
gibt sich Note **3,0**, KI-Einsatz **4 %** – Bitkom/ZDH 2025 [F]. Zweitentscheider:
Ehepartnerin/Bürokraft im Innendienst – **oft der eigentliche Türöffner und zugleich
der größte Widerstand** (Angst vor Ersetzung).

**4. Konkretes Problem**
Alle produktiven Kräfte sind auf Baustellen; das Büro ist mit 0,5–1,5 Personen
besetzt und gleichzeitig für Telefon, Angebote, Bestellung, Rechnung, Terminierung
zuständig. Anrufspitzen (Heizungsausfall im Winter) treffen auf minimale
Innendienstkapazität. Wartungs- und Serviceverträge werden nicht systematisch
verkauft, obwohl sie die margenstärkste Leistung sind.

**5. Wirtschaftlicher Schaden [S] – Modell M1**
Annahmen (konservativ, jeweils rund halbiert gegenüber Anbieterangaben):
A = 25 Anrufe/Tag · T = 220 · u = 20 % · n = 25 % · v = 50 % · c = 30 %
· W = 1.500 € (Mischung Kleinreparatur 300–800 € und Anlagenerneuerung 12–20 T€) [A]
```
25 × 220              = 5.500 Anrufe/Jahr
× 0,20 unbeantwortet  = 1.100
× 0,25 Neuanfragen    =   275
× 0,50 endgültig weg  =   137
× 0,30 Abschluss      =    41 verlorene Aufträge
× 1.500 €             = 61.700 € entgangener Umsatz/Jahr [S]
× 30 % Deckungsbeitrag= 18.500 € entgangener DB/Jahr [S]
```
Zweitschaden M2 (Innendienst-Zeitverlust durch Rückrufschleifen, Terminverschieben,
Nachfassen): 1,5 h/Tag × 220 × 42 €/h = **13.900 €/Jahr** [S].
**Gesamtschaden ca. 32.000 €/Jahr, Bandbreite 15.000–70.000 €** [S].

**6. Bestehende Lösung heute**
Anrufbeantworter, Mobilnummer des Chefs, Bürokraft in Teilzeit, gelegentlich
klassisches Telefonsekretariat (50–250 €/Monat [F]); Handwerkersoftware
(pds, Label, Streit V.1, Sander, plancraft, HERO, ToolTime) für Angebot/Rechnung,
aber ohne Anrufanbindung.

**7. Unzufriedenheit**
Belegt: **69 %** nennen hohe Investitionen als Hemmnis, **63 %** den digitalen
Rückstand der Behörden – Bitkom/ZDH 2025 [F]. Zugleich sehen **76 %** Zeitersparnis
als Hauptvorteil der Digitalisierung [F] – das Problembewusstsein ist da, die
Umsetzung nicht. Für Telefonsekretariate liegt in dieser Session **kein**
belastbares Zufriedenheitsdatum vor – **offene Frage, muss in Agent 11 geklärt
werden**: warum kündigen Handwerksbetriebe ihr Telefonsekretariat?

**8. Zahlungsbereitschaft [S]**
**180–350 €/Monat** für Betriebe mit 5–25 Mitarbeitern; **400–650 €/Monat** nur bei
Betrieben > 25 Mitarbeiter oder mit Notdienst. Begründung: Referenzpreis
Telefonsekretariat 50–250 €/Monat [F]; Handwerkersoftware 15–120 €/Nutzer [F];
Digitalisierungsgesamtbudget Kleinstbetrieb 430–680 €/Monat [S]. Setup-Gebühr
**500–1.500 € einmalig** ist durchsetzbar, wenn sie als „Einrichtung + Einweisung"
verkauft wird [A].
**Kritisch:** Wer hier 600–900 €/Monat plant, plant an der Datenlage vorbei.

**9. Vertriebskanäle**
ZVSHK + 17 Landes-/Fachverbände SHK; SHK-Innungen (Innungsversammlungen als
Vortragsbühne); Messen **ISH Frankfurt** (2027) und **SHK Essen** (2026);
Fachmedien **SBZ**, **IKZ-Haustechnik**, **TGA Fachplaner**, **si-shk.de**;
**Großhandel als stärkster Partnerkanal** (GC-Gruppe, Richter+Frenzel,
Sanitär-Heinze, ELEMENTS-Verbund) – dort liegen Kundenlisten und Vertrauen;
Herstellerpartnerprogramme (Viessmann, Vaillant, Bosch/Buderus, Geberit);
Handwerkskammern/Betriebsberatung; Kaltakquise funktioniert (Inhaber geht selbst ans
Telefon), aber nur mit konkretem Zahlenaufhänger.

**10. Verkaufszyklus**
**14–45 Tage** [A]. Inhaberentscheidung, kein Gremium. Beschleuniger: kostenloser
4-Wochen-Anruf-Report („Sie haben 218 Anrufe nicht angenommen").

**11. Einwände / Wechselbarrieren**
- „Wir haben genug Arbeit, wir können gar nicht mehr annehmen" (trotz −4 % Umsatz [F])
- „Meine Kunden wollen mit einem Menschen sprechen, nicht mit einem Computer"
- „Meine Frau macht das Büro" (persönliche Kränkung als echte Barriere)
- „Was kostet das im Jahr?" – Fokussierung auf Kosten statt Ertrag
- Wechselbarriere technisch **niedrig** (Rufumleitung), emotional **hoch**
- Datenschutz/Mitschnitt-Thema bei Aufzeichnung von Anrufen (TDDDG/DSGVO)

**12. Konzentration für 100.000 € MRR**
Bei 250 €/Monat: **400 Kunden** = **0,83 %** aller SHK-Betriebe [S].
Bei 350 €/Monat: **286 Kunden** = 0,60 % [S].
Marktanteil ist erreichbar, **Kundenzahl ist das Problem** (Support, Onboarding,
Churn-Management bei 400 Kleinkunden). Verstößt gegen Pflichtkriterium 5.

---

### ZG 02 – Elektro- und informationstechnische Handwerke

**1. Anzahl** **49.113 Unternehmen** (Elektrotechnik, Informationstechnik,
Elektromaschinenbau), +0,5 % – ZVEH-Branchenkennzahlen [F].

**2. Größe** Umsatz **88,2 Mrd. €** (2024, −4 %), **451.050 sozialversicherungs-
pflichtig Beschäftigte** davon **46.403 Auszubildende** (−1,2 %) – ZVEH [F].
Rechnerisch **1,80 Mio. € je Betrieb**, **9,2 Beschäftigte je Betrieb** [S].
2025: „Jahr der Stagnation" [F].

**3. Entscheider** Elektromeister/Inhaber, 45–58 [A]. **Höhere technische
Affinität als SHK** (Gebäudeautomation, KNX, Ladeinfrastruktur, PV-Speicher) –
das senkt die Erklärungshürde für Software, erhöht aber den Anspruch
(„das könnte ich mir selbst bauen") und die Kritikfähigkeit.

**4. Problem** Gleiches Grundmuster wie SHK plus: hoher Anteil an
Kleinstaufträgen und Serviceanfragen (Störung, E-Check, Wallbox), die telefonisch
kommen und einzeln wenig wert, in Summe aber margenstark sind. Zusätzlich:
**wiederkehrende Prüfpflichten (DGUV V3, E-Check) werden nicht systematisch
nachverfolgt** – das ist der eigentlich attraktive Hebel, weil Pflichtwiederholung
= planbarer Umsatz.

**5. Schaden [S] – M1 + Pflichtprüfungs-Verlust**
A = 20 · T = 220 · u = 20 % · n = 25 % · v = 50 % · c = 30 % · W = 2.000 € [A]
```
20 × 220 = 4.400 → ×0,20 = 880 → ×0,25 = 220 → ×0,50 = 110 → ×0,30 = 33 Aufträge
33 × 2.000 € = 66.000 € entgangener Umsatz/Jahr [S] · DB 30 % = 19.800 € [S]
```
Zusatz: 300 Bestandskunden mit DGUV-V3-Prüfpflicht, 35 % werden nicht
nachverfolgt = 105 × 450 € Prüfauftrag = **47.250 € nicht abgerufener
Wiederholungsumsatz/Jahr** [S, A stark].
**Gesamt ca. 60.000–115.000 €/Jahr** [S].

**6. Heute** Bürokraft, Handwerkersoftware (pds, Streit, Label, mobile
Zeiterfassung), Großhandelsportale; Prüfnachverfolgung meist per Excel oder gar nicht.

**7. Unzufriedenheit** Gleiche Bitkom/ZDH-Datenlage wie ZG 01 [F].
Zusätzliches Signal: Beschäftigtenrückgang −1,2 % bei gleichzeitig 46.403 Azubis
zeigt Demografie-Druck [F] → Automatisierungsdruck steigt strukturell.

**8. Zahlungsbereitschaft [S]** **200–400 €/Monat**, bei Betrieben mit
Wartungs-/Prüfvertragsgeschäft **450–800 €/Monat**, weil hier direkt zurechenbarer
Zusatzumsatz entsteht (ROI-Rechnung 47 T€ vs. 6 T€ Jahreskosten ist verkaufbar).
Etwas höher als SHK, weil Auftragswerte und technische Affinität höher sind.

**9. Kanäle** ZVEH + 12 Landesinnungsverbände; **E-Marke**-Partnerprogramm;
Innungen; Messen **eltefa Stuttgart**, **Light+Building Frankfurt**;
Fachmedien **de – das elektrohandwerk (elektro.net)**, **ep ElektroPraktiker**,
**elektrowirtschaft.de**; Elektrogroßhandel **Sonepar, Rexel, FEGA & Schmitt,
Wilhelm Mayer**; Hersteller (Hager, ABB/Busch-Jaeger, Siemens, Gira).

**10. Zyklus** **21–50 Tage** [A].

**11. Einwände** „Das kann meine Software auch" (stimmt selten, klingt aber
plausibel); „Ich baue mir das selbst"; Preisvergleich mit 29-€-Softwaretarifen;
Skepsis gegenüber Sprach-KI im technischen Störungsgespräch.

**12. 100k MRR** Bei 300 €: **333 Kunden** = 0,68 % des Marktes [S].
Bei 550 € (Wartungsvertragsmodul): **182 Kunden** = 0,37 % [S].

---

### ZG 03 – Dachdeckerbetriebe

**1. Anzahl** **15.241 Betriebe** (Stichtag 31.12.2025, tarifliche Sozialkasse) –
ZVDH [F]. **78 % beschäftigen weniger als zehn Arbeitnehmende** [F].

**2. Größe** Umsatz **13,5 Mrd. €** (2025, ±0,0 % nominal, bei ca. **+4,5 %**
Preissteigerung also **real negativ**); **61.723 gewerbliche Arbeitnehmende**
(−1,0 %) – ZVDH [F]. Rechnerisch **886.000 € Umsatz je Betrieb**, **4,1 gewerbliche
AN je Betrieb** [S]. Nachfragetreiber: Sanierung, Photovoltaik, Dachbegrünung [F].

**3. Entscheider** Inhaber, 45–58 [A], **selbst auf dem Dach** – die
Erreichbarkeitslücke ist hier physisch am größten und am leichtesten zu belegen.
Digitalaffinität niedrig.

**4. Problem** Betrieb mit 4–8 Leuten hat **keinen** Innendienst. Anrufe laufen auf
das Handy des Chefs, der auf dem Dach steht, im Lärm arbeitet oder Absturzsicherung
trägt. Hohe Auftragswerte machen jeden verlorenen Erstkontakt teuer. Zusätzlich:
Sturmschaden-Peaks (nach Unwetter 5–10-faches Anrufaufkommen an einem Tag) –
genau dann wird nichts angenommen und genau dann ist die Zahlungsbereitschaft
der Endkunden am höchsten.

**5. Schaden [S] – M1, angepasst an kleine Betriebe / hohe Auftragswerte**
A = 12 · T = 220 · u = 25 % (kein Innendienst) · n = 20 % · v = 55 % · c = 20 %
· W = 8.000 € (Mischung Reparatur 800–2.500 € / Sanierung 15–40 T€) [A]
```
12 × 220 = 2.640 → ×0,25 = 660 → ×0,20 = 132 → ×0,55 = 73 → ×0,20 = 15 Aufträge
15 × 8.000 € = 120.000 € entgangener Umsatz/Jahr [S] · DB 25 % = 30.000 € [S]
```
**Höchster relativer Schaden aller Handwerks-Zielgruppen** (13,5 % des
Betriebsumsatzes von 886 T€) – weil Auftragswert hoch und Innendienst null.
Bandbreite konservativ **50.000–160.000 € Umsatz** bzw. 12.500–40.000 € DB [S].

**6. Heute** Mobiltelefon, Mailbox, Ehepartnerin, teils Anrufweiterleitung an
Kollegen; Software (Dachdecker-spezifisch: Sander, DACHDECKER-Software,
allgemeine Handwerkersoftware).

**7. Unzufriedenheit** Kein spezifisches Zufriedenheitsdatum in dieser Session
belegbar – **Lücke**. Indirektes Signal: „Weniger Betriebe verdienen mehr Geld"
(Branchenmedium dach.live) [F-schwach] deutet auf Konsolidierung und damit
professioneller werdende Betriebsführung.

**8. Zahlungsbereitschaft [S]** **150–300 €/Monat**. Trotz des höchsten Schadens
die **niedrigste** Zahlungsbereitschaft der Gruppe, weil Betriebe klein sind
(78 % < 10 AN [F]) und Ein-Mann-/Kleinbetriebe strukturell keine Monatsabos
akzeptieren. **Warnung: hoher Schaden ≠ hohe Zahlungsbereitschaft.**
Wer hier verkaufen will, braucht ein erfolgsabhängiges Modell
(z. B. Grundgebühr 99 € + 25 € je vermitteltem Vor-Ort-Termin) [A].

**9. Kanäle** ZVDH + Landesinnungsverbände; Messe **DACH+HOLZ International**;
Fachmedien **DDH – Das Dachdecker-Handwerk**, **dach.live**; Baustoffhandel und
Hersteller (Braas/Monier BMI, Creaton, Velux, Bauder, Rheinzink);
Sozialkasse SOKA-DACH als Adressquelle.

**10. Zyklus** **10–30 Tage** [A] – kürzester Zyklus, weil Einzelentscheider und
akuter Leidensdruck; aber auch kürzeste Kündigungstreue.

**11. Einwände** „Im Winter habe ich sowieso nichts zu tun" (Saisonalität →
Kündigungsrisiko Nov–Feb); „Meine Kunden sind Stammkunden"; extreme Preissensibilität.
**Saisonalität ist hier ein MRR-Killer** – Vertragslaufzeit 12 Monate zwingend.

**12. 100k MRR** Bei 220 €/Monat: **455 Kunden** = **3,0 %** aller
Dachdeckerbetriebe Deutschlands [S]. **Marktanteil zu hoch, Kundenzahl zu groß –
als alleinige Zielgruppe ungeeignet.** Nur als Zusatzsegment sinnvoll.

---

### ZG 04 – Maler- und Lackiererbetriebe

**1. Anzahl** **[A] ca. 38.000–42.000 Betriebe – in dieser Session nicht
verifiziert.** Zu prüfen über ZDH-Statistikdatenbank (zdh-statistik.de,
Gewerbegruppe Ausbaugewerbe) und Bundesverband Farbe Gestaltung Bautenschutz.

**2. Größe** [A] Ø 350.000–500.000 € Umsatz, 4–7 Mitarbeitende – nicht verifiziert.

**3. Entscheider** Inhaber/Malermeister, 42–58 [A], niedrige Digitalaffinität,
sehr preissensibel (Gewerk mit hohem Wettbewerbsdruck und niedrigen
Eintrittsbarrieren).

**4. Problem** Sehr viele kleine Anfragen mit niedrigem Auftragswert; hoher
Aufwand für Ortstermine/Aufmaß, die häufig nicht zum Auftrag führen; kaum
Innendienst. Angebotsnachverfolgung („Haben Sie mein Angebot erhalten?") findet
faktisch nicht statt.

**5. Schaden [S]** M1 mit A = 12 · u = 25 % · n = 25 % · v = 50 % · c = 25 %
· W = 3.000 € [A]:
```
12 × 220 = 2.640 → 660 → 165 → 82 → 21 Aufträge × 3.000 € = 62.000 € Umsatz [S]
DB 30 % = 18.600 €/Jahr [S]
```
Zusatz M2: unbeantwortete Angebote. 120 Angebote/Jahr [A], 40 % ohne Nachfassen,
davon 15 % wären bei Nachfassen doch gekommen = 7 Aufträge × 3.000 € =
**21.600 €/Jahr** [S].

**6. Heute** Handy, Mailbox, Papier-Aufmaß, Handwerkersoftware selten.

**7. Unzufriedenheit** Nicht belegt – **Lücke**.

**8. Zahlungsbereitschaft [S]** **99–200 €/Monat.** Niedrigste der gesamten
Analyse. Begründung: kleinste Betriebsgröße, niedrigster Auftragswert, höchster
Preiswettbewerb im Gewerk.

**9. Kanäle** Bundesverband Farbe Gestaltung Bautenschutz + Landesinnungsverbände;
Fachmedien **Mappe**, **Malerblatt**; Großhandel (Brillux, Caparol/DAW-Partnerprogramme,
Sto) – Herstellerpartnerprogramme sind hier der einzige effiziente Kanal.

**10. Zyklus** **7–21 Tage** [A].

**11. Einwände** Preis, Preis, Preis. Zusätzlich: „Ich habe die Kunden aus der
Nachbarschaft."

**12. 100k MRR** Bei 150 €: **667 Kunden** = ca. 1,7 % des Marktes [S].
**Ausschluss als Kernzielgruppe** – Kundenzahl unvereinbar mit Pflichtkriterium 5
und mit Nicos Anti-Kriterium „täglicher Kundensupport".

---

### ZG 05 – Bauunternehmen (Bauhauptgewerbe, Hoch- und Tiefbau)

**1. Anzahl** **[A] ca. 75.000–85.000 Betriebe im Bauhauptgewerbe – in dieser
Session nicht verifiziert.** Zu prüfen: Destatis Fachserie 4 / Hauptverband der
Deutschen Bauindustrie / ZDB.

**2. Größe** [A] Sehr heterogen: vom 5-Mann-Maurerbetrieb bis zum
mittelständischen GU mit 200 Mitarbeitenden. Zielsegment wären GU/Ausbau-Firmen
mit **20–150 Mitarbeitenden, 5–40 Mio. € Umsatz** [A].

**3. Entscheider** Geschäftsführer / kaufmännischer Leiter / Bauleiter.
Bei > 30 Mitarbeitenden **mehrstufige Entscheidung** → längerer Zyklus,
aber höheres Budget.

**4. Problem** Nicht Telefonannahme, sondern **Nachtragsmanagement,
Bautagebuch, Aufmaß-Dokumentation, Mängelverfolgung, Subunternehmer-Koordination**.
Nicht dokumentierte Nachträge sind der klassische Margenkiller. Zusätzlich:
Ausschreibungsflut – Angebote werden aus Kapazitätsgründen nicht abgegeben.

**5. Schaden [S] – abweichendes Modell (Nachtragsverlust)**
Bauunternehmen 12 Mio. € Umsatz [A]. Nachtragsvolumen typ. 6 % = 720.000 €;
davon 25 % nicht durchsetzbar mangels Dokumentation = **180.000 €/Jahr
entgangener Umsatz** [S, Annahmen stark]. Bei DB 12 % (Bau ist margenschwach)
= 21.600 € Gewinn [S].
Zweitschaden: nicht abgegebene Angebote. 200 Ausschreibungen/Jahr, 30 % nicht
bearbeitet = 60 × 8 % Zuschlagsquote = 4,8 Aufträge × 250.000 € = **1,2 Mio. €
Umsatz** [S] – aber bei 12 % DB nur 144.000 € Marge, und der Kapazitätsengpass
bleibt real.

**6. Heute** Bau-ERP (Nevaris, BRZ, iTWO, Bau-SU), Excel, WhatsApp-Gruppen,
Papier-Bautagebuch.

**7. Unzufriedenheit** Nicht belegt – **Lücke**. Bekannt: hoher
Insolvenzdruck im Bau 2024/25 → **Debitorenrisiko**.

**8. Zahlungsbereitschaft [S]** **500–2.000 €/Monat** bei 20–150 Mitarbeitenden.
Deutlich höher als im Ausbauhandwerk, weil das Problem sechsstellig ist und der
Käufer kaufmännisch denkt. **Aber:** hohe Anforderungen an Integration in
bestehendes Bau-ERP → Sonderanfertigungsrisiko (K.-o.-Kriterium 4!).

**9. Kanäle** ZDB, Hauptverband der Deutschen Bauindustrie, Landesverbände;
Messe **bauma** (München, alle 3 Jahre), **BAU München**; Fachmedien
**Deutsches Baublatt**, **bauhandwerk**, **tHIS**; Bau-ERP-Anbieter als Partner.

**10. Zyklus** **90–180 Tage** [A] – Gremienentscheidung, IT-Beteiligung.

**11. Einwände** „Wir haben Nevaris/BRZ, da muss das rein"; Datenhoheit;
„Unsere Bauleiter machen da nicht mit" (Adoptionsrisiko in der Fläche);
Insolvenz-/Zahlungsrisiko der Branche.

**12. 100k MRR** Bei 900 €/Monat: **111 Kunden** [S] – **gute Konzentration**.
Aber Standardisierbarkeit schwach und Verkaufszyklus lang. Nachrangig.

---

### ZG 06 – Freie Kfz-Werkstätten und freie Händler

**1. Anzahl** **22.050 freie Werkstätten und Händler** (Teil von insgesamt
**36.170** Kfz-Betrieben) – ZDK-Jahresbilanz, Stand 2023, −0,4 % [F].

**2. Größe** Gesamtes Kfz-Gewerbe: **207,3 Mrd. €** Umsatz (2024, +11,9 %),
für 2025 **210,8 Mrd. €**; **428.000 Beschäftigte** (2024, −0,5 %) – ZDK [F].
Rechnerisch über alle Betriebe **5,73 Mio. € je Betrieb** [S] – für freie
Werkstätten aber deutlich niedriger, realistisch **400 T€ – 1,5 Mio. €** bei
**4–12 Mitarbeitenden** [A], da der Umsatz stark vom Neuwagenhandel der
fabrikatsgebundenen Betriebe dominiert wird.

**3. Entscheider** Inhaber/Kfz-Meister, **45–60** [A]. Digitalaffinität mittel:
Werkstätten arbeiten seit Jahren mit Diagnose-, Teilekatalog- und
DMS-Systemen (Werbas, CarIT, AutoPlus, TopMotive/TecDoc) – **Software ist hier
kulturell normal**, anders als beim Dachdecker. Das ist ein unterschätzter Vorteil.

**4. Konkretes Problem**
Die Werkstattkapazität ist ein **verderbliches Gut**: eine nicht belegte Hebebühne
ist am Abend endgültig verloren. Gleichzeitig ist die Serviceannahme die
personelle Engstelle – der Serviceberater steht am Fahrzeug, am Tresen und am
Telefon gleichzeitig. Typische Folge: Anrufe zwischen 8 und 10 Uhr laufen ins
Leere, Kunden gehen zur nächsten Werkstatt. Zusätzlich: **HU/AU-Fälligkeiten und
Serviceintervalle werden nicht systematisch nachverfolgt** – der planbarste
Umsatz der Branche wird verschenkt.

**5. Schaden [S] – M1 + Wiedereinbestellungsverlust**
A = 30 · T = 250 · u = 25 % · n = 30 % · v = 40 % · c = 60 %
· W = 450 € (Inspektion/Reparatur, Lohn + Teile) [A]
```
30 × 250 = 7.500 → ×0,25 = 1.875 → ×0,30 = 562 → ×0,40 = 225 → ×0,60 = 135 Aufträge
135 × 450 € = 60.750 € entgangener Umsatz/Jahr [S]
× DB 55 % (Service ist margenstark: Lohn ~70 %, Teile ~25 %) = 33.400 €/Jahr [S]
```
Zusatz: 1.200 Bestandsfahrzeuge in der Kartei [A]; 30 % erscheinen nicht zur
fälligen HU/Inspektion, weil niemand erinnert = 360 Fahrzeuge; 25 % davon wären
mit aktiver Ansprache gekommen = 90 × 450 € = **40.500 € Umsatz**, DB 55 % =
**22.300 €/Jahr** [S].
**Gesamt ca. 55.700 € entgangener Deckungsbeitrag pro Jahr** [S] – bei einem
Betrieb mit vielleicht 80–150 T€ Jahresgewinn ein **Drittel bis die Hälfte des
Gewinns**. Das ist die stärkste ROI-Story im Handwerk.

**6. Bestehende Lösung** DMS/Werkstattsoftware (Werbas, ADIS, AutoPlus, Loco-Soft
auch bei freien), Terminbuch auf Papier oder im DMS, Anrufbeantworter;
Online-Terminbuchung meist über das Werkstattkonzept (z. B. Bosch Car Service
Portal) oder Plattformen (FairGarage, Autobutler, caroobi/Repareo – teils
gescheitert, siehe Friedhofsprüfung).

**7. Unzufriedenheit** In dieser Session nicht direkt belegt – **Lücke, an Agent 11
zu übergeben.** Indirekt: Beschäftigtenrückgang −0,5 % bei steigendem Umsatz [F]
= Produktivitätsdruck. **Friedhofswarnung:** Werkstatt-Vermittlungsplattformen
(Repareo, caroobi, Autobutler DE) sind in Deutschland weitgehend gescheitert.
Ein *Vermittlungs*modell ist dort ein Friedhof; ein *Betriebsassistenz*modell
(der Betrieb bleibt Absender) ist es nicht – diese Unterscheidung ist
entscheidend und muss in der Endempfehlung stehen.

**8. Zahlungsbereitschaft [S]** **200–450 €/Monat**, mit HU-/Serviceerinnerungs-
Modul **350–600 €/Monat**. Begründung: Der ROI ist mit 55 T€ DB gegen 4,2–7,2 T€
Jahreskosten außergewöhnlich klar rechenbar; Werkstätten zahlen bereits
DMS-Gebühren und Konzeptgebühren (Werkstattkonzepte kosten typ. mehrere hundert
Euro monatlich [A]) – die **Zahlungsgewohnheit für monatliche Systemgebühren
existiert bereits**. Das ist ein struktureller Vorteil gegenüber SHK/Dachdecker.

**9. Vertriebskanäle – der stärkste Partnerkanal der gesamten Analyse**
- **Werkstattkonzepte als Multiplikator**: Bosch Car Service, AutoCrew,
  1a autoservice, Meisterhaft, ATU, Premio, point S, Euro Garant, AutoFit.
  Ein einziger Konzeptvertrag erschließt 500–1.500 Betriebe auf einmal.
- **Teilegroßhandelsverbünde**: ATR, Carat, Coparts, Global Automotive/Select AG,
  Wessels+Müller, Stahlgruber/LKQ, TROST.
- ZDK + Landesverbände + Kfz-Innungen.
- Messen: **Automechanika Frankfurt** (2026), Automechanika-Regionalmessen.
- Fachmedien: **kfz-betrieb**, **amz**, **Krafthand**, **asp AutoServicePraxis**,
  **autohaus.de**.
- Kaltakquise sehr gut möglich (klare Rufnummern, Inhaber greifbar).

**10. Verkaufszyklus** **21–45 Tage** direkt [A]; über Werkstattkonzept
**120–270 Tage** für den Rahmenvertrag, danach aber Rollout mit sehr niedrigen
Stückkosten [A].

**11. Einwände / Wechselbarrieren**
- „Meine Stammkunden rufen wieder an" (bei Werkstätten teilweise berechtigt –
  Bindung ist höher als bei SHK; deshalb liegt der Hebel eher bei
  **Wiedereinbestellung** als bei Neukunden)
- „Das muss in mein DMS (Werbas/AutoPlus) rein" – **Integrationsanforderung ist
  der reale Blocker**, nicht der Preis
- Konzeptvorgaben: manche Betriebe dürfen nur konzeptzertifizierte Tools nutzen
- Preisvergleich mit dem 99-€-Telefonservice

**12. 100k MRR** Bei 350 €/Monat: **286 Kunden** = **1,3 %** der freien Betriebe [S].
Bei 500 €/Monat: **200 Kunden** = 0,9 % [S]. Über zwei Werkstattkonzepte
realistisch erreichbar – **Kanalkonzentration macht diese Zielgruppe
delegierbar und skalierbar**.

---

### ZG 07 – Autohäuser (fabrikatsgebunden)

**1. Anzahl** **14.120 fabrikatsgebundene Betriebe** (2023, −1,2 %) – ZDK [F].

**2. Größe** Deutlich größer als freie Werkstätten. Über alle 36.170 Kfz-Betriebe
verteilt sich ein Umsatz von 207,3 Mrd. € = **5,73 Mio. € je Betrieb** [S];
da Neu- und Gebrauchtwagengeschäft fast vollständig bei den fabrikatsgebundenen
Betrieben liegt, ist deren Durchschnitt realistisch bei **8–15 Mio. €** und
**25–80 Mitarbeitenden** [A]. Drei Geschäftsbereiche: Neuwagen, Gebrauchtwagen,
Service [F].

**3. Entscheider** Geschäftsführer / Serviceleiter / Marketingleiter;
bei Händlergruppen (Emil Frey, AVAG, Wellergruppe, Dello, Hedin) zentrale
IT-/Prozessverantwortliche. Alter 38–55 [A], **kaufmännisch, KPI-getrieben,
gewohnt an Systemkosten** – der professionellste Einkäufer im gesamten Feld.
Digitalaffinität mittel bis hoch.

**4. Konkretes Problem**
Zwei getrennte, jeweils teure Probleme:
(a) **Serviceannahme**: 80–150 eingehende Anrufe/Tag [A], Spitzen morgens; die
Serviceassistenz ist gleichzeitig Empfang, Kassierer und Telefonzentrale.
(b) **Lead-Nachverfolgung im Verkauf**: Online-Leads (Herstellerportal,
mobile.de, AutoScout24) werden nicht innerhalb der kritischen Reaktionszeit
bearbeitet; abends und samstags läuft niemand ans Telefon, obwohl genau dann
Privatkunden anrufen.

**5. Schaden [S] – zwei Modelle**
(a) Service, M1: A = 100 · T = 250 · u = 20 % · n = 25 % · v = 35 % · c = 65 %
· W = 550 € [A]
```
100 × 250 = 25.000 → ×0,20 = 5.000 → ×0,25 = 1.250 → ×0,35 = 437 → ×0,65 = 284
284 × 550 € = 156.200 € entgangener Serviceumsatz/Jahr [S] · DB 55 % = 85.900 € [S]
```
(b) Verkauf, M1 mit hohem W: 900 Leads/Jahr [A]; 20 % nicht oder zu spät
kontaktiert = 180; davon 50 % endgültig verloren = 90; Abschlussquote 12 % =
11 Fahrzeuge × **2.200 € Bruttoertrag je Einheit** [A] = **23.800 €/Jahr** [S]
(plus Folge-Serviceumsatz über die Haltedauer).
**Gesamt ca. 110.000 € entgangener Deckungsbeitrag pro Jahr und Standort** [S].
Das ist der **höchste absolute Schaden je Einzelbetrieb** in dieser Analyse –
und er trifft einen Käufer, der ihn selbst nachrechnen kann.

**6. Heute** DMS (Loco-Soft, CROSS/Vector, CDK/Keyloop, AutoPlus, ADP),
herstellerseitige CRM-/Leadsysteme (verpflichtend!), Call-Center-Lösungen
großer Gruppen, teils externe Terminvereinbarungs-Dienstleister
(z. B. für Serviceaktionen/Rückrufe – ein bereits **bezahlter** Vergleichsmarkt).

**7. Unzufriedenheit** Nicht direkt belegt – **Lücke**. Indirekt: „Trübe Aussichten
nach Rekorderlösen" (ZDK-Jahrespressekonferenz) [F] und rückläufige
Betriebszahlen (−1,2 %) [F] → Konsolidierung, Kostendruck, Professionalisierung.
In der Konsolidierung steigt die Bereitschaft, Personalkosten durch Systeme zu
ersetzen.

**8. Zahlungsbereitschaft [S]** **800–2.500 €/Monat je Standort**, bei
Händlergruppen **3.000–15.000 €/Monat** für Mehrstandort-Verträge.
Begründung: Der Schaden ist sechsstellig je Standort [S]; Autohäuser zahlen
bereits vier- bis fünfstellige Monatsbeträge für DMS, Werksvorgaben und
Marketing; der Einkäufer denkt in „Kosten je Serviceauftrag", nicht in
„Was kostet das im Monat". **Höchste belastbare Zahlungsbereitschaft der Analyse.**

**9. Vertriebskanäle**
Markenhändlerverbände (z. B. Verband der Mercedes-Benz-Partner, VDVA, Händlerbeiräte);
Händlergruppen zentral ansprechen (Emil Frey, AVAG, Weller, Hedin, Dello,
Schwabengarage) – **wenige Anrufe, viele Standorte**; Messen **Automechanika**,
**AUTOHAUS-Kongresse**, **Autohaus digital**; Fachmedien **AUTOHAUS (Springer)**,
**Automobilwoche**, **kfz-betrieb**; **DMS-Anbieter als Integrationspartner**
(Loco-Soft, Vector/CROSS – dort liegt die Verteilungsmacht).

**10. Verkaufszyklus** **60–150 Tage** je Einzelstandort [A];
**180–360 Tage** für Gruppenverträge [A]. Deutlich länger als Handwerk,
aber Vertragswert 5–20× höher.

**11. Einwände / Wechselbarrieren**
- **„Der Hersteller schreibt uns die Systeme vor"** – der schwerste Einwand.
  Werksvorgaben zu CRM, Leadmanagement und Datenflüssen sind bindend; ein
  Zusatzsystem muss sich der Werkslogik unterordnen. Das ist zugleich Nicos
  Anti-Kriterium „Abhängigkeit von Konzernen" – **Warnsignal**.
- „Wir haben ein eigenes Callcenter in der Gruppe"
- Datenschutz und Werks-IT-Freigaben verlängern jede Einführung
- DMS-Integration ist Pflicht, nicht Kür → Entwicklungsaufwand

**12. 100k MRR** Bei 1.200 €/Monat: **83 Kunden** = **0,6 %** der
fabrikatsgebundenen Betriebe [S]. Bei 2.000 €: **50 Kunden** [S].
**Beste Konzentration aller Handwerks-/Gewerbe-Zielgruppen** und vereinbar mit
Pflichtkriterium 5.

---

### ZG 08 – Zahnarztpraxen und Dental-MVZ

**1. Anzahl** **[A] ca. 40.000–43.000 Zahnarztpraxen – in dieser Session nicht
verifiziert** (zu prüfen über KZBV-Jahrbuch 2025 / BZÄK „Nachgezählt").
Belegt ist der Gesamtumsatz: **Zahnarztpraxen erwirtschaften 30,0 Mrd. €** [F, KZBV].

**2. Größe** **Ø 677.000 € Jahresumsatz je Einzelpraxis mit einem Inhaber**
(2023, abzüglich Fremdlabor; 2022 noch 625.800 €) – KZBV-Jahrbuch 2025 [F].
Typisch 1–3 Behandler, **4–12 Mitarbeitende** (ZFA, Prophylaxe, Verwaltung) [A].
Erhebliche regionale Spreizung (alte Bundesländer deutlich höher) [F].

**3. Entscheider** Praxisinhaber (Zahnarzt), **38–58** [A]; zunehmend
**Praxismanager/-in** als operative Entscheiderin. Bei MVZ-Ketten
(zahneins, Colosseum Dental, dentalgroup, Acura) zentrale Prozessverantwortliche –
**dort liegt der Mehrstandort-Hebel**. Digitalaffinität mittel bis hoch,
Investitionsbereitschaft in Praxisausstattung traditionell hoch
(ein Behandlungsstuhl kostet fünfstellig – die Preisanker sind ganz andere als
im Handwerk).

**4. Konkretes Problem**
(a) Der Empfang ist gleichzeitig Telefonzentrale, Terminvergabe, Abrechnung und
Patientenaufnahme. Neupatientenanrufe gehen in der Stoßzeit verloren.
(b) **No-Shows**: nicht erschienene Patienten blockieren Behandlerzeit, die
nicht nachbelegt werden kann – der teuerste Einzelposten.
(c) Recall/Prophylaxe-Nachverfolgung (halbjährliche PZR) läuft manuell.

**5. Schaden [S] – M1 + M3**
(a) Neupatienten, M1: A = 60 · T = 220 · u = 30 % · n = 8 % · v = 60 % · c = 50 %
```
60 × 220 = 13.200 → ×0,30 = 3.960 → ×0,08 = 317 → ×0,60 = 190 → ×0,50 = 95 Neupatienten
95 × 400 € Erstjahresumsatz [A] = 38.000 €/Jahr [S]
(mehrjährig, LTV 1.500 € über 5 Jahre [A] → 142.500 € entgangener Lebenswert [S])
```
(b) No-Shows, M3: 6 Ausfälle/Woche × 46 Wochen × 0,5 h = 138 Ausfallstunden;
Umsatz je Behandlungsstunde 300 € [A]; Nachbelegungsquote 50 % [A]
```
138 × 300 € × 0,50 = 20.700 €/Jahr [S]
```
(c) Recall: 1.500 Prophylaxe-berechtigte Patienten [A]; 35 % ohne Erinnerung
nicht erschienen = 525; 30 % wären mit Erinnerung gekommen = 157 × 95 € PZR
= **14.900 €/Jahr** [S].
**Gesamt ca. 73.600 €/Jahr entgangener Umsatz** = **10,9 % des Praxisumsatzes
von 677 T€** [S]. Bei Praxis-DB ca. 65 % (Personal- und Raumkosten laufen
ohnehin) sind das **ca. 47.800 € Gewinn/Jahr** [S].

**6. Heute** Praxisverwaltungssystem (CHARLY, DAMPSOFT, Dentalsoft, evident,
Z1/CGM), Terminbuch im PVS, Anrufbeantworter über Mittag, teils Doctolib
(Terminplattform, kostenpflichtig – belegt zahlungsfähiger Vergleichsmarkt),
teils externe „Telefonannahme für Praxen".

**7. Unzufriedenheit** Für Zahnärzte in dieser Session nicht direkt belegt.
Belegt für den Praxissektor allgemein: **40 %** haben Online-Terminvereinbarung,
**45 %** Online-Rezeptbestellung, Zufriedenheit mit digitalen Kernanwendungen
deutlich gestiegen (eRezept 63 → 77 %) – KBV/IGES PraxisBarometer 2025, n=1.700 [F].
Das heißt: **60 % haben noch keine Online-Terminvereinbarung** – ein
Adressierbarkeitsargument [S].

**8. Zahlungsbereitschaft [S]** **350–900 €/Monat je Praxis**;
**2.000–8.000 €/Monat** bei MVZ-Gruppen mit 5–30 Standorten.
Begründung: Praxisumsatz 677 T€ [F], Schaden ~48 T€ Gewinn [S], gewohnte
Systemkosten (PVS, Röntgen-Software, Terminplattform) im drei- bis vierstelligen
Monatsbereich [A]; die Praxis kann Kosten teilweise über Selbstzahlerleistungen
weitergeben. **Deutlich höher als jedes Handwerk.**

**9. Vertriebskanäle** **Dentaldepots als Multiplikator** (Pluradent,
Henry Schein, NWD, Dental Union) – sie sind bei jeder Praxis regelmäßig vor Ort;
Messe **IDS Köln** (2027) – die weltgrößte Dentalmesse, Pflichttermin;
Fachmedien **zm (zahnärztliche mitteilungen)**, **DZW**, **ZWP online**,
**dental barometer**; Praxisberater/Steuerberater mit Dentalfokus;
MVZ-Gruppen zentral; Kammern nur eingeschränkt (Werbebeschränkungen).

**10. Verkaufszyklus** **21–60 Tage** Einzelpraxis [A]; **120–240 Tage** MVZ-Gruppe [A].

**11. Einwände / Wechselbarrieren**
- **Datenschutz**: Patientendaten sind Gesundheitsdaten nach **Art. 9 DSGVO**;
  zusätzlich **§ 203 StGB** (Berufsgeheimnis) – Auftragsverarbeitungsvertrag und
  Verpflichtung „mitwirkender Personen" nach § 203 Abs. 3 StGB sind zwingend.
  Machbar, aber ein echter Vertriebswiderstand und Aufwand.
  **Bewertungsrelevanz:** kein K.-o. nach Kriterium 3 (keine Erlaubnispflicht,
  keine BaFin/MPDR), aber ein Abschlag bei Kriterium 14 „niedriger
  regulatorischer Aufwand".
- „Meine Helferinnen machen das doch"
- PVS-Integration (CHARLY/DAMPSOFT) als technische Hürde
- Standesrechtliche Empfindlichkeit gegenüber „Vertrieblichkeit"

**12. 100k MRR** Bei 550 €/Monat: **182 Praxen** = ca. 0,44 % [S].
Bei Mischung aus 120 Einzelpraxen (550 €) + 8 MVZ-Gruppen (4.200 €):
66.000 + 33.600 = **99.600 € MRR mit 128 Kunden** [S]. Gute Struktur.

---

### ZG 09 – Arztpraxen (Haus- und Fachärzte)

**1. Anzahl** **[A] ca. 50.000–55.000 vertragsärztliche Praxen – in dieser Session
nicht verifiziert** (zu prüfen über KBV-Gesundheitsdaten/Bundesarztregister).

**2. Größe** [A] Einzelpraxis bis Gemeinschaftspraxis/MVZ, 3–20 Mitarbeitende.

**3. Entscheider** Praxisinhaber (Arzt), 45–62 [A]; MFA-Leitung operativ.
Digitalaffinität laut KBV **überdurchschnittlich**: „Niedergelassene bleiben
Vorreiter in Sachen Digitalisierung"; 87 % nutzen den eArztbrief, 65 % versenden
ihn regelmäßig; Zufriedenheit eAU 69 → 78 % – KBV/IGES PraxisBarometer 2025,
n=1.700 [F].

**4. Problem** **100–200 Anrufe/Tag** in einer hausärztlichen Praxis, konzentriert
auf die ersten zwei Öffnungsstunden [S, Branchenmedium]; häufig nur eine MFA für
100+ Anrufe [S]. Ergebnis: Dauerbesetzt, entnervte Patienten, MFA im
Dauerstress → Fluktuation. Der Springer-Fachdiskurs „Arztpraxis ohne Telefon –
kann das funktionieren?" (MMW – Fortschritte der Medizin, 2025;
ästhetische dermatologie & kosmetologie, 2025) zeigt, dass das Thema in der
**Fachliteratur** angekommen ist [F] – ein seltenes, belastbares Nachfragesignal.

**5. Schaden – WICHTIGE EINSCHRÄNKUNG [S]**
**Bei GKV-Praxen greift Modell M1 nicht.** Die vertragsärztliche Vergütung ist
budgetiert/gedeckelt – mehr Patienten bedeuten **mehr Arbeit, nicht mehr Geld**.
Der Umsatzverlust-Pitch ist hier ökonomisch falsch und wird vom Arzt sofort
durchschaut. Es bleibt **M2/M4**:
```
Entlastung MFA: 2,5 h/Tag Telefonzeit einsparen × 220 Tage × 32 €/h Vollkosten [A]
= 17.600 €/Jahr [S]
Fluktuationskosten: 1 MFA-Neubesetzung alle 2 Jahre à 8.000 € [A] → 4.000 €/Jahr [S]
Selbstzahler-/IGeL- und Privatpatientenanteil: nur hier greift M1.
Bei 15 % Privatanteil und 40 verlorenen Privatterminen/Jahr × 180 € = 7.200 € [S]
```
**Gesamt ca. 28.800 €/Jahr** [S] – **weniger als ein Drittel des Zahnarzt-Schadens**,
obwohl das Anrufaufkommen doppelt so hoch ist. Das ist der wichtigste
Einzelbefund dieser Zielgruppe.

**6. Heute** PVS (CGM Medistar/Turbomed, medatixx, Duria, T2med),
Telefonanlage mit Warteschleife, Doctolib/samedi/Dr. Flex (Terminplattformen),
teils „Telefonzeiten" mit bewusster Nichterreichbarkeit.

**7. Unzufriedenheit** Belegt: Nachholbedarf bei **technischer Stabilität** und
**sektorenübergreifender Nutzung** – KBV 2025 [F]. Für Telefonie kein
belastbares Zufriedenheitsdatum in dieser Session – **Lücke**.

**8. Zahlungsbereitschaft [S]** **250–600 €/Monat**. Deutlich unter Zahnarzt,
weil der Nutzen Kostenersparnis statt Umsatz ist und die Praxis budgetiert ist.
Ausnahme: **reine Privat-/Selbstzahlerpraxen** (Ästhetik, Dermatologie,
Orthopädie-IGeL, Kinderwunsch, Augenlaser) – dort **600–1.500 €/Monat** [S],
weil dort jeder Neupatient direkter Umsatz ist.
**Strategische Konsequenz: nicht „Arztpraxen" ansprechen, sondern
„Selbstzahler-Praxen".**

**9. Kanäle** PVS-Anbieter als Partner (CGM, medatixx – große Verteilmacht);
Messen **DMEA Berlin** (Digital Health), **MEDICA Düsseldorf**;
Fachmedien **Deutsches Ärzteblatt**, **Der Hausarzt**, **MMW**,
**Ärzte Zeitung**; Praxisberater und Steuerberater mit Heilberufe-Fokus;
Ärztekammern nur eingeschränkt (Werberecht); MVZ-Träger zentral.

**10. Zyklus** **30–90 Tage** [A].

**11. Einwände** „Datenschutz"; „Meine Patienten sind alt und wollen einen
Menschen"; „Ich bekomme dafür kein Geld von der Kasse" (der ökonomisch
korrekte und schwerste Einwand); PVS-Integration; TI-Anbindung.

**12. 100k MRR** Bei 400 €/Monat: **250 Praxen** [S] – zu viele.
Über Selbstzahlerpraxen bei 900 €: **111 Praxen** [S] – tragfähig,
aber der adressierbare Teilmarkt ist erheblich kleiner und nicht quantifiziert
(**Lücke**).

---

### ZG 10 – Tierarztpraxen und Tierkliniken

**1. Anzahl** **46.089 approbierte Tierärzte** Ende 2025 (+444), davon nur
**34.476 tierärztlich tätig** – Bundestierärztekammer, Tierärztestatistik 2025 [F].
Anzahl Praxen: **[A] ca. 9.000–11.000 – nicht verifiziert**; belegt ist, dass
**in der Mehrzahl der Kammerbereiche die Zahl der Tierarztpraxen 2025 rückläufig
war** [F] und der Anteil Selbstständiger sinkt [F].

**2. Größe** Typische Kleintierpraxis: **2 Tierärzte + 2–3 TFA** [S];
[A] Umsatz 400.000–900.000 €.

**3. Entscheider** Praxisinhaber/-in, **35–55**, hoher Frauenanteil,
digital aufgeschlossen; zunehmend **Ketten** (AniCura/Mars, IVC Evidensia,
Evidensia Deutschland) mit zentralem Einkauf – **Mehrstandort-Hebel wie im Dental**.

**4. Konkretes Problem – das belegteste Telefonproblem der ganzen Analyse**
Eine durchschnittliche Kleintierpraxis erhält **60–120 Anrufe/Tag** bei einer
**Gesprächsdauer von 3–5 Minuten** – deutlich länger als in anderen Branchen
[S, Branchenmedium]. Rechnung: 90 Anrufe × 4 Min = **6 Stunden reine Telefonzeit
pro Tag** [S] – das ist eine volle Stelle, die faktisch nicht existiert.
Belegt: „Am Empfang steht häufig nur eine TFA, die gleichzeitig telefoniert,
Patienten empfängt, Rechnungen erstellt und dem Tierarzt assistiert" [S].
Der TFA-Fachkräftemangel ist laut Bundestierärztekammer bundesweit
vierstellig-fehlend [F-schwach, Verbandsaussage].

**5. Schaden [S] – M1 + M2**
M1: A = 90 · T = 250 · u = 30 % · n = 15 % · v = 50 % · c = 60 % · W = 120 € [A]
```
90 × 250 = 22.500 → ×0,30 = 6.750 → ×0,15 = 1.012 → ×0,50 = 506 → ×0,60 = 304
304 × 120 € = 36.500 € entgangener Umsatz/Jahr [S]
```
M2: 6 h/Tag Telefonzeit; 40 % davon (Terminvergabe, Öffnungszeiten,
Preisauskunft, Rezeptnachbestellung) sind vollständig automatisierbar [A]
= 2,4 h/Tag × 250 × 34 €/h TFA-Vollkosten = **20.400 €/Jahr** [S].
**Gesamt ca. 56.900 €/Jahr** [S] – bei 600 T€ Praxisumsatz **9,5 %**.
Zusatznutzen ohne Euro-Wert: Reduktion der TFA-Fluktuation, die in dieser
Branche existenzbedrohend ist.

**6. Heute** Praxissoftware (easyVET, Vetera, animal office, VetZ),
Anrufbeantworter, Notdienst-Weiterleitung, teils „Telefonzeiten".

**7. Unzufriedenheit** Belegt als struktureller Befund: „Tierarztpraxen im
Spannungsfeld zwischen steigenden Personal-, Energie- und Investitionskosten,
Fachkräftemangel und dem Anspruch bezahlbarer Versorgung" – BTK [F].
Rückläufige Praxiszahlen und sinkende Selbstständigenquote [F] = ökonomischer
Druck.

**8. Zahlungsbereitschaft [S]** **300–700 €/Monat** Einzelpraxis;
**2.500–10.000 €/Monat** bei Ketten (AniCura, IVC Evidensia) mit
50–200 Standorten. Begründung: Praxis ist **privatwirtschaftlich, nicht
budgetiert** (Tierhalter zahlen selbst nach GOT) – jeder gewonnene Termin ist
echter Umsatz, anders als bei GKV-Arztpraxen. **Das macht Tiermedizin
ökonomisch attraktiver als Humanmedizin (GKV).**
Zusätzlich: die **GOT-Novelle 2022** hat die Preise deutlich angehoben →
höhere Erlöse je Behandlung.

**9. Kanäle** Bundestierärztekammer/Landestierärztekammern (eingeschränkt);
**bpt (Bundesverband Praktizierender Tierärzte)** – der praxisnahe Verband;
Kongresse: **bpt-Kongress**, **Leipziger Tierärztekongress**, **VetMedica**;
Fachmedien **Deutsches Tierärzteblatt**, **team.konkret**, **hundkatzepferd**;
Praxissoftware-Anbieter (VetZ/easyVET) als Integrationspartner;
**Ketten zentral** – wenige Gespräche, viele Standorte;
Veterinärgroßhandel (Henry Schein Vet, WDT, CP-Pharma).

**10. Zyklus** **21–60 Tage** Einzelpraxis [A]; **150–300 Tage** Kette [A].

**11. Einwände** „Bei uns ist jeder Anruf ein Notfall, das kann keine Maschine
beurteilen" – **der stärkste und fachlich berechtigte Einwand**; die Lösung muss
Triage sicher an Menschen übergeben, sonst Haftungsthema.
Weiter: Datenschutz (unkritischer als Humanmedizin – **keine Gesundheitsdaten
nach Art. 9 DSGVO**, da Tierdaten; das ist ein echter regulatorischer Vorteil),
Praxissoftware-Integration, emotionale Bindung der Tierhalter an bekannte Stimmen.

**12. 100k MRR** Bei 450 €/Monat: **222 Praxen** = ca. 2,2 % [S] – zu viele
bei kleinem Markt. Mit Kettenanteil (5 Ketten à 6.000 € + 155 Einzelpraxen
à 450 €) = 30.000 + 69.750 = **99.750 € mit 160 Kunden** [S].
**Konzentrationsrisiko: der Markt ist mit ~10.000 Praxen klein**, ein
Marktanteil von 2 % ist nötig – machbar, aber wenig Puffer.

---
