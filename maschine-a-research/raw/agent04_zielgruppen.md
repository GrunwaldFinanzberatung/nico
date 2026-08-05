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

### ZG 11 – Steuerkanzleien

**1. Anzahl** **53.932 Steuerberaterpraxen** (ohne weitere Beratungsstellen);
**105.953 Kammermitglieder** gesamt (Stand 01.01.2026, +1,1 %), davon
**88.995 Steuerberater**, **14.670 anerkannte Berufsausübungsgesellschaften**,
**1.172 Steuerbevollmächtigte/Sonstige** – Bundessteuerberaterkammer,
Berufsstatistik 2025 [F].

**2. Größe** **65,9 % Selbstständigenquote**; **59.519 selbstständige**
Steuerberater, **30.817 angestellte** Berufsangehörige [F].
Typische Kanzlei: **3–15 Mitarbeitende** [A], [A] 300 T€ – 1,5 Mio. € Umsatz.

**3. Entscheider** Kanzleiinhaber/Partner, **45–62** [A]. Frauenanteil
**39,3 %** – neuer Höchststand [F]. Digitalaffinität mittel bis hoch, aber
**vollständig innerhalb des DATEV-Ökosystems** – das ist gleichzeitig Chance
(DATEV-Marktplatz als Kanal) und Barriere.

**4. Konkretes Problem**
(a) **Nachwuchs- und Personalengpass ist belegt**: „Die Zahl der
Ausbildungsverhältnisse ist weiter rückläufig"; **17.081** Ausbildungsverhältnisse
zum Steuerfachangestellten bundesweit – BStBK [F]. Bei 53.932 Praxen sind das
0,32 Azubis je Praxis [S].
(b) **Belegnachlauf und Mandantenkommunikation**: Kanzleien verbringen einen
erheblichen Teil ihrer Zeit damit, Mandanten hinterherzutelefonieren
(„Wo sind die Belege für Mai?"). Das ist **nicht fakturierbare Zeit**.
(c) Mandantenanrufe mit Standardfragen (Fristen, Vollmachten, Bescheidkopien)
binden Fachkräfte, die abrechenbar arbeiten könnten.

**5. Schaden [S] – M2 + M4**
M2 (nicht fakturierbare Kommunikationszeit): Kanzlei mit 8 Mitarbeitenden;
3 Fachkräfte × 1,25 h/Tag Belegnachlauf und Rückfragen × 220 Tage
× **75 €/h abrechenbarer Stundensatz** [A]
```
3 × 1,25 × 220 × 75 € = 61.875 €/Jahr entgangene fakturierbare Leistung [S]
```
M4 (unbesetzte Stelle → abgelehnte Mandate): 1 unbesetzte Fachkraftstelle;
Umsatz je Fachkraft **110.000 €/Jahr** [A]; DB 40 % [A]
```
110.000 × 0,40 = 44.000 €/Jahr entgangener Deckungsbeitrag [S]
```
**Gesamt ca. 105.900 €/Jahr** [S] – bei einer 800-T€-Kanzlei über 13 % des
Umsatzes. **Höchster relativer Schaden aller Dienstleistungszielgruppen.**

**6. Heute** DATEV (Unternehmen online, DMS, Meine Steuern), Kanzleisoftware
(Addison/Wolters Kluwer, Agenda, Simba, Stotax), teils Mandantenportale
(getmyinvoices, Candis, Circula), Telefon und E-Mail.

**7. Unzufriedenheit** Belegt nur indirekt über den Nachwuchsengpass [F]
(„Nachwuchs bleibt Engpass" – Überschrift der Berufsstatistik-Berichterstattung).
Für konkrete Softwareunzufriedenheit **keine Belege in dieser Session – Lücke**,
an Agent 11 zu übergeben.

**8. Zahlungsbereitschaft [S]** **400–1.500 €/Monat**;
größere Kanzleien (20+ Mitarbeitende) **1.500–4.000 €/Monat**.
Begründung: Der Schaden ist sechsstellig [S]; Kanzleien sind es gewohnt,
pro Arbeitsplatz und Modul zu zahlen (DATEV-Kostenstruktur); sie **fakturieren
selbst nach Stundensatz** und verstehen den Wert eingesparter Zeit sofort –
das ist der ökonomisch reifste Käufer im gesamten Feld.
**Sehr hohe Zahlungsbereitschaft, gute Bonität, extrem niedriger Zahlungsausfall.**

**9. Kanäle** **DATEV-Marktplatz** (der zentrale Verteilkanal – Aufnahme ist
selbst ein Projekt); **Deutscher Steuerberaterverband (DStV)** + 15
Landesverbände; **Deutscher Steuerberatertag** (Jahreskongress);
Messen/Kongresse **DATEV-Kongress**, **Kanzleiforum**;
Fachmedien **NWB**, **DATEV magazin**, **Die Steuerberatung**, **stb-web.de**,
**taxtech.blog**; Kanzleiberater und Softwarehäuser als Reseller.

**10. Verkaufszyklus** **60–150 Tage** [A]. Berufsstand ist entscheidungsträge,
prüft gründlich, kauft aber dann langfristig. **Sehr niedriger Churn** –
ein struktureller MRR-Vorteil.

**11. Einwände / Wechselbarrieren**
- **„Muss DATEV-kompatibel sein"** – ohne DATEV-Schnittstelle kein Geschäft.
  Das ist eine harte technische Eintrittsbarriere (und zugleich ein Burggraben,
  wenn man sie überwindet).
- **§ 203 StGB / § 62a StBerG Verschwiegenheit**: Dienstleister müssen förmlich
  verpflichtet werden; Auftragsverarbeitung nach Art. 28 DSGVO; Serverstandort DE.
  Machbar, aber Prüfungsaufwand beim Mandanten.
- „Meine Mandanten wollen mich persönlich sprechen"
- Berufsrechtliche Vorsicht bei Werbung und Auslagerung
- Hohe Wechselbarriere in beide Richtungen: schwer reinzukommen,
  aber danach **sehr klebrig**

**12. 100k MRR** Bei 800 €/Monat: **125 Kanzleien** = **0,23 %** von 53.932 [S].
Bei 1.200 €: **83 Kanzleien** [S]. **Exzellente Konzentration**, geringster
erforderlicher Marktanteil aller Zielgruppen.

**Bewertungsvorbehalt gegenüber Nicos Profil:** Steuerberatung ist ein
**Anzug-Business** mit Fristen-, Dokumenten- und Einzelfalllogik. Nico lehnt
„Fristen und Einzelfälle verwalten", „Unterlagen prüfen" und „steifes
Anzug-Business" ausdrücklich ab. Als *Kunde* ist die Kanzlei attraktiv;
als *Arbeitsinhalt* liegt sie nahe an Nicos Abneigungen. Das muss Agent 09
(Persönlichkeits-Fit) prüfen.

---

### ZG 12 – Immobilien- und Hausverwaltungen (WEG- und Mietverwaltung)

**1. Anzahl** **[A] ca. 19.000–23.000 Verwaltungsunternehmen – in dieser Session
nicht verifiziert** (zu prüfen über VDIV-Branchenbarometer 2025 Vollversion /
Destatis WZ 68.32).

**2. Größe** [A] typisch 3–25 Mitarbeitende, 500–5.000 verwaltete Einheiten,
300 T€ – 3 Mio. € Umsatz. Belegt: Verwaltungen erwarteten bis Ende 2025
ein **Umsatzplus von durchschnittlich 7,8 %** – VDIV Branchenbarometer 2025 [F].

**3. Entscheider** Geschäftsführer/Inhaber, **40–60** [A]; kaufmännisch geprägt,
denkt in „Kosten je Einheit". Digitalaffinität mittel – aber
**Investitionsbereitschaft belegt hoch** (s. u.).

**4. Konkretes Problem – die am besten belegte Schmerzlage der gesamten Analyse**

| Befund | Wert | Quelle |
|---|---|---|
| Verwaltungen berichten von **Überlastung** | **70 %** (ein Drittel davon stark) | VDIV Branchenbarometer 2025 [F] |
| … weil offene Stellen unbesetzt bleiben | ja, insbesondere große Verwaltungen | ebd. [F] |
| Verwaltungen, die **unrentable Mandate abgeben** | **57 %** | ebd. [F] |
| Verwaltungen, die **gar keine Neukunden mehr annehmen** | **14 %** | ebd. [F] |
| Verwaltungen, die **hohe Mittel in Automatisierung** stecken | **knapp 80 %**, KI „ganz oben auf der Agenda" | ebd. [F] |
| Geplante Preisanpassungen 2025 (WEG) | **ca. +12 %**, kleine Objekte bis **+17 %** | ebd. [F] |

Das ist die seltene Konstellation: **belegter Schmerz + belegte
Investitionsabsicht + belegte Fähigkeit, Kosten weiterzugeben.**
Operativ: Verwaltungen ertrinken in Eigentümer- und Mieteranrufen
(Heizung defekt, Nebenkostenabrechnung, Beschluss XY), Handwerkerkoordination,
Terminorganisation für Eigentümerversammlungen und Schadensmeldungen.

**5. Schaden [S] – M2 + M4**
Referenzverwaltung: **2.500 WEG-Einheiten**, Vergütung **28 €/Einheit/Monat** [A]
→ 840.000 € Jahresumsatz [S].
M2 (Telefon-/Anfragelast): 2.500 Einheiten × 2,5 Kontakte/Jahr = 6.250 Kontakte;
Ø 6 Minuten inkl. Nachbearbeitung = **625 Stunden/Jahr** × 45 €/h Vollkosten
```
625 × 45 € = 28.100 €/Jahr reine Kommunikationskosten [S]
davon 45 % automatisierbar (Standardauskunft, Terminvergabe, Schadensaufnahme) [A]
= 12.600 €/Jahr direkt einsparbar [S]
```
M4 (unbesetzte Stelle = nicht annehmbare Mandate): Ein Objektbetreuer verwaltet
**400–500 Einheiten** [A]. Eine unbesetzte Stelle bedeutet
```
450 Einheiten × 28 € × 12 = 151.200 € Umsatz, der nicht angenommen werden kann [S]
× 20 % Nettomarge = 30.240 €/Jahr entgangener Gewinn [S]
```
Zusatzschaden (belegt): **57 % geben unrentable Mandate ab** [F] – das ist
aktiv aufgegebener Umsatz, weil die Bearbeitung zu teuer ist. Wer die
Bearbeitungskosten je Einheit senkt, macht abgegebene Mandate wieder rentabel.
**Gesamt ca. 42.800 €/Jahr direkt + 151.200 € blockiertes Wachstum** [S].

**6. Heute** Verwaltersoftware (Haufe PowerHaus, DOMUS 4000/1000, Aareon Wodis,
immoware24, iX-Haus/CREM, Facilioo), Mieter-/Eigentümerportale
(**casavi**, **etg24**, Immoware-Portal – belegt zahlungsfähiger Vergleichsmarkt),
Telefonzentrale, Sprechzeiten, E-Mail-Postfach als Sammelbecken.

**7. Unzufriedenheit** Belegt über die Verhaltensdaten: 57 % geben Mandate ab,
14 % nehmen keine Neukunden – das sind **Kapitulationssignale**, nicht Meinungen [F].
Zusätzlich der Marktkommentar „Verwaltersterben" (Branchenblog) [F-schwach].
Das ist stärker als jede Zufriedenheitsumfrage.

**8. Zahlungsbereitschaft [S]** **500–1.500 €/Monat** bei 1.000–3.000 Einheiten;
**2.000–6.000 €/Monat** bei > 5.000 Einheiten.
Alternativ und besser: **Preis je verwalteter Einheit, 0,30–0,80 €/Einheit/Monat**
[S] – das ist die Kalkulationslogik der Branche und macht den Preis
**an die Verwaltervergütung weiterreichbar** (die Verwaltung hebt ihre
Einheitsvergütung um 0,50 € an und ist kostenneutral).
Bei 2.500 Einheiten × 0,50 € = **1.250 €/Monat** [S].
Begründung für die Höhe: belegte Preisanpassungen von +12 % [F], belegte
Automatisierungsinvestitionen von 80 % der Verwaltungen [F], Schaden > 40 T€/Jahr [S].

**9. Vertriebskanäle**
**VDIV Deutschland** + 11 Landesverbände (Mitgliederkommunikation,
Verbandszeitschrift, Partnerprogramm); **Deutscher Verwaltertag** (Jahreskongress,
der Pflichttermin der Branche); Regionalveranstaltungen der Landesverbände;
Messen **Immobilien-Verwaltertag**, **EXPO REAL** (eher institutionell);
Fachmedien **IVV immobilien vermieten & verwalten**, **Der Immobilienverwalter**,
**Immobilienwirtschaft (Haufe)**, **immobilienmanager**;
**Softwarehäuser als Integrationspartner** (Haufe, DOMUS, Aareon, casavi) –
und zugleich potenzielle Wettbewerber;
Verwaltergruppen/Konsolidierer (Matera, ImmoScout-nahe Rollups, Objego)
als Mehrstandortkunden.

**10. Verkaufszyklus** **45–120 Tage** [A]. Geschäftsführerentscheidung,
aber typischerweise mit Testphase an einem Objektbestand.

**11. Einwände / Wechselbarrieren**
- **„Das muss in unsere Verwaltersoftware rein, sonst pflegen wir doppelt"** –
  der zentrale Einwand. Ohne Schnittstelle zu Haufe/DOMUS/Aareon kein Abschluss.
- **„Unsere Vergütung ist im Verwaltervertrag gedeckelt"** – jeder Zusatz-Euro
  geht bis zur nächsten Eigentümerversammlung direkt vom Gewinn ab.
  Gegenmittel: Preis je Einheit, der in die nächste Vergütungsanpassung
  eingepreist wird (belegt: +12 % geplant [F]).
- „Eigentümer wollen ihren Verwalter persönlich sprechen"
- Haftungsfragen bei Schadensmeldungen (Wasserschaden falsch priorisiert)
- Beschlusszwang der WEG bei bestimmten Kostenumlagen

**12. 100k MRR** Bei 1.000 €/Monat: **100 Kunden** = ca. **0,45 %** des Marktes [S].
Bei 1.250 € (Einheitenmodell): **80 Kunden** [S].
**Beste Kombination aus niedriger Kundenzahl, belegtem Schmerz und belegter
Investitionsabsicht in der gesamten Analyse.**

---

### ZG 13 – Ambulante Pflegedienste

**1. Anzahl** **17.938–17.976 ambulante Pflegedienste** (Marktdaten/MD-Bericht),
die **2.275.280 Patienten** versorgen; die amtliche Pflegestatistik weist
**15.549 Dienste** mit **1.100.672 Patienten** aus – rund 50 % der versorgten
Patienten fehlen in der amtlichen Statistik [F, pflegemarkt.com].
**2024: 623 Neugründungen, 292 Schließungen** [F]. Wachstum 2022–2025
**+10,3 %** [F].

**2. Größe** Rechnerisch **127 Patienten je Dienst** [S: 2.275.280 / 17.938].
[A] typisch 15–40 Mitarbeitende, 800 T€ – 2,5 Mio. € Umsatz.

**3. Entscheider** Inhaber/Pflegedienstleitung (PDL), **38–55** [A],
oft aus der Pflege kommend, kaufmännisch weniger geschult, chronisch
zeitarm. Digitalaffinität niedrig bis mittel.

**4. Konkretes Problem**
(a) **Tägliches Ausfallmanagement**: eine kranke Pflegekraft zwingt zur
kompletten Umplanung mehrerer Touren – morgens um 6 Uhr, telefonisch.
(b) **Nicht abgerechnete Leistungen** durch Dokumentationslücken.
(c) Anfragen von Angehörigen und Kliniken (Überleitung) werden verpasst –
und ein nicht angenommener Neupatient ist ein **dauerhafter** monatlicher
Umsatzverlust, nicht ein einmaliger.

**5. Schaden [S] – M2 + Abrechnungsverlust + M1 mit wiederkehrendem Wert**
M2 (Ausfall-/Tourenumplanung): PDL 1,5 h/Tag × 250 × 55 €/h Vollkosten
= **20.600 €/Jahr** [S].
Abrechnungsverlust: Umsatz 1,2 Mio. € [A] × 3 % nicht abgerechnete Leistungen [A]
= **36.000 €/Jahr** [S].
M1 mit Dauerwert: 24 Neuanfragen/Jahr verpasst [A]; 40 % wären Patienten geworden
= 10 Patienten × **1.400 €/Monat durchschnittlicher Pflegeumsatz** [A] × 12
= **168.000 €/Jahr wiederkehrender Umsatz** [S] – aber gedeckelt durch die
Kapazität: der Dienst kann sie mangels Personal ohnehin nicht versorgen.
**Realistisch ansetzbar sind daher nur M2 + Abrechnung = ca. 56.600 €/Jahr** [S].

**6. Heute** Pflegesoftware (Vivendi/Connext, MediFox DAN, Godo Systems,
Snap, Curasoft), Dienstplansoftware, Telefon, WhatsApp-Gruppen (datenschutzwidrig,
aber verbreitet).

**7. Unzufriedenheit** In dieser Session nicht belegt – **Lücke**.

**8. Zahlungsbereitschaft [S]** **200–500 €/Monat**. Deutlich unter dem
Schadenspotenzial. Begründung:
- Die Vergütung ist über **SGB XI / Rahmenverträge mit Pflegekassen**
  reguliert und verhandelt – Kostensteigerungen sind **nicht frei weitergebbar**,
  sondern erst in der nächsten Vergütungsverhandlung.
- Der Engpass ist **Personal, nicht Nachfrage** – mehr Anfragen anzunehmen
  hilft nicht, wenn niemand die Tour fahren kann. Das entwertet den
  Umsatz-Pitch vollständig.
- Margen sind dünn; Inhaber sind Pflegefachkräfte, keine Investoren.

**9. Kanäle** **bpa Bundesverband privater Anbieter sozialer Dienste**,
**ABVP**, **AWO/Diakonie/Caritas** als Träger-Zentralen (Mehrstandortkunden!);
Messen **ALTENPFLEGE** (Nürnberg/Essen), **Pflegemesse**;
Fachmedien **Häusliche Pflege**, **CAREkonkret**, **Altenheim**;
Pflegesoftware-Anbieter als Partner (MediFox DAN, Connext).

**10. Zyklus** **45–120 Tage** [A]; bei Trägern (Diakonie, Caritas)
**180–360 Tage** wegen Gremien.

**11. Einwände** „Dafür bekommen wir keine Refinanzierung von der Kasse" –
der ökonomisch entscheidende Einwand; Datenschutz (Gesundheitsdaten, Art. 9 DSGVO);
MD-Prüfungsrelevanz jeder Dokumentationsänderung; „Unsere Mitarbeiter sind
über 50 und machen das nicht mit".

**12. 100k MRR** Bei 350 €/Monat: **286 Kunden** = 1,6 % [S] – zu viele
bei gleichzeitig niedrigem ARPU und regulatorischem Aufwand.
**Empfehlung: abwerten.** Regulatorik (SGB XI, MD, Art. 9 DSGVO) plus
gedeckelte Refinanzierung plus hohe Kundenzahl ist die schlechteste
Kombination der Analyse.

---

### ZG 14 – Speditionen und Fuhrparks

**1. Anzahl** **[A] ca. 6.500–8.000 Speditionen mit relevanter Größe – in dieser
Session nicht verifiziert.** Belegt: Speditions- und Logistikdienstleister
beschäftigten **592.622 Personen** (2024) und erzielten **123,1 Mrd. €** Umsatz
(2023) – DSLV [F]. Logistik insgesamt: drittgrößte Branche Deutschlands,
**ca. 300 Mrd. €**, **> 3 Mio. Beschäftigte** [F].

**2. Größe** [A] Zielsegment: 20–150 Fahrzeuge, 5–50 Mio. € Umsatz.

**3. Entscheider** Geschäftsführer / Leiter Disposition / IT-Leiter.
Kaufmännisch, kostengetrieben, gewohnt an Systemkosten (TMS, Telematik, Maut).

**4. Konkretes Problem – belegt**

| Befund | Wert | Quelle |
|---|---|---|
| Speditionen, die **Dispositionsstellen nicht besetzen** können | **64 %** | Branchenerhebung Logistik-Fachkräftemangel [F] |
| Fehlende Berufskraftfahrer in Deutschland | **ca. 70.000**; BGL-Prognose: bald **120.000** | BGL / kraftfahrer.net [F] |
| Renteneintritte vs. Neueinsteiger je Jahr | **30.000–35.000 aus** vs. **15.000–20.000 ein** | ebd. [F] |
| Kostendruck Stückgut H1 2025 | Sendungsmengen **−3,2 %**, Depots **+5,8 %** | DSLV-Kostenindex 2025 [F] |
| Mindestlohn | **13,90 €** ab 01.01.2026, **14,60 €** ab 01.01.2027 | [F] |

Die Disposition ist der Engpass: Anfragen, Statusabfragen („Wo ist meine
Sendung?"), Terminavisierung, Schadensmeldungen und Fahrerkommunikation
laufen alle über dieselben wenigen Personen, die zugleich planen sollen.

**5. Schaden [S] – M2 + Leerkilometer + M4**
M2 (Statusabfragen): 30 Statusanrufe/Tag × 250 × 6 Min = **750 h/Jahr**
× 48 €/h Vollkosten Disponent = **36.000 €/Jahr** [S]; 70 % davon
automatisierbar (Sendungsstatus ist in jedem TMS abrufbar) = **25.200 €** [S].
Leerkilometer: 30 LKW × 110.000 km/Jahr = 3,3 Mio. km; **3 %** vermeidbare
Leerfahrten durch bessere Disposition [A] × 1,20 €/km Vollkosten
= **118.800 €/Jahr** [S].
M4 (nicht besetzbare Dispo-Stelle): belegt bei 64 % der Speditionen [F];
Folge: 1–2 nicht bediente Kundenanfragen pro Woche → 75/Jahr × 20 % Abschluss
× 4.500 € Jahresumsatz je Kleinkunde [A] = **67.500 €** [S].
**Gesamt ca. 211.500 €/Jahr** [S] – der **höchste absolute Schaden** neben
Autohaus und Bau.

**6. Heute** TMS (cargoSoft, LIS Winsped, Transdata Komalog, Soloplan CarLo,
Active Logistics), Telematik (Webfleet, TomTom, Trimble, Idem), Frachtenbörsen
(TIMOCOM, Transporeon), Telefon und E-Mail.

**7. Unzufriedenheit** Belegt über den Personalengpass (64 % [F]) und den
Kostenindex (steigende Maut-, Personal-, Materialkosten [F]).
Softwareunzufriedenheit nicht belegt – **Lücke**.

**8. Zahlungsbereitschaft [S]** **800–3.000 €/Monat** bei 20–150 Fahrzeugen.
Begründung: sechsstelliger Schaden [S]; die Branche zahlt bereits
**pro Fahrzeug und Monat** für Telematik (typ. 15–40 €/Fzg/Mon [A]) –
ein Preis „je Fahrzeug" ist kulturell akzeptiert und skaliert automatisch mit
der Kundengröße. Bei 60 Fahrzeugen × 25 €/Fzg = 1.500 €/Monat [S].

**9. Kanäle** **DSLV** + Landesverbände Spedition und Logistik;
**BGL Bundesverband Güterkraftverkehr Logistik und Entsorgung**;
Messe **transport logistic München** (2027) – die europäische Leitmesse;
Fachmedien **DVZ Deutsche Verkehrs-Zeitung**, **VerkehrsRundschau**,
**eurotransport/trans aktuell**, **LOGISTIK HEUTE**;
TMS-Anbieter und Telematikanbieter als Integrationspartner;
Ladungsverbünde/Systemkooperationen (**IDS Logistik**, **CargoLine**,
**System Alliance**, **Online Systemlogistik**, **24plus**) – das sind
**Multiplikatoren mit je 40–200 Mitgliedsspeditionen**, der effizienteste Kanal.

**10. Zyklus** **90–180 Tage** [A]; Systemkooperationen 180–360 Tage [A].

**11. Einwände / Wechselbarrieren**
- **„Das muss in unser TMS"** – TMS-Integration ist zwingend und pro System
  unterschiedlich → **Sonderanfertigungsrisiko (K.-o.-Kriterium 4 prüfen!)**
- „Unsere Kunden sind Industriekunden mit eigenen Portalvorgaben"
- Margen im Transport sind dünn (2–4 %) → jede Fixkostenerhöhung tut weh
- Insolvenzrisiko in der Transportbranche → Debitorenprüfung nötig
- Disponenten fürchten Kontrollverlust und Ersetzung

**12. 100k MRR** Bei 1.500 €/Monat: **67 Kunden** [S].
**Sehr gute Konzentration.** Aber: Standardisierbarkeit durch TMS-Vielfalt
gefährdet, und der Verkaufszyklus ist lang.

---

### ZG 15 – Metallbau, Zerspanung, CNC-Lohnfertigung

**1. Anzahl** **[A] Metallbauer im Handwerk ca. 38.000–42.000; CNC-/Zerspanungs-
Lohnfertiger als Teilmenge ca. 5.000–8.000 – in dieser Session nicht verifiziert**
(zu prüfen: ZDH-Statistikdatenbank, Bundesverband Metall, VDMA, Destatis WZ 25.62).

**2. Größe** [A] Lohnfertiger typisch 10–80 Mitarbeitende, 1–15 Mio. € Umsatz.

**3. Entscheider** Inhaber/technischer Geschäftsführer, 45–60 [A],
technisch sehr affin (CAD/CAM, CNC-Steuerungen, Messtechnik), aber
**kaufmännische Prozesse oft archaisch** (Angebote in Excel).

**4. Konkretes Problem**
**Angebotserstellung ist der Engpass.** Anfragen kommen als PDF-Zeichnung
oder STEP-Datei per E-Mail. Die Kalkulation macht der Chef oder ein Techniker –
abends. Durchlaufzeit bis zum Angebot: **3–10 Arbeitstage** [A].
Währenddessen liefern Plattformen (**Xometry**, **Laserhub**, **Sourcify**,
**Protolabs**) in Minuten einen Preis. Folge: Anfragen werden verloren,
bevor sie kalkuliert sind – oder aus Kapazitätsgründen gar nicht bearbeitet.

**5. Schaden [S] – Angebotsdurchsatz**
400 Anfragen/Jahr [A]; **30 % werden nicht oder zu spät bearbeitet** [A] = 120;
Abschlussquote bei rechtzeitiger Bearbeitung 25 % [A];
Ø Auftragswert 4.500 € [A]
```
120 × 0,25 × 4.500 € = 135.000 € entgangener Umsatz/Jahr [S]
× DB 30 % = 40.500 €/Jahr [S]
```
Zusatz M2: 400 Angebote × 1,5 h Kalkulationsaufwand × 85 €/h
= **51.000 €/Jahr** Kalkulationskosten [S]; 40 % davon automatisierbar
bei wiederkehrenden Teilefamilien = **20.400 €** [S].
**Gesamt ca. 60.900 €/Jahr** [S].

**6. Heute** ERP (ams.erp, Sage, ABAS, PSIpenta, Cetec), CAM (hyperMILL,
Siemens NX, Mastercam), Kalkulation in Excel; Plattformen als
Fremdkanal (Xometry als Wettbewerber **und** als Auftragsquelle).

**7. Unzufriedenheit** Nicht belegt – **Lücke**. Marktsignal: das Wachstum
von Xometry/Laserhub belegt, dass Einkäufer die langsame Angebotsabgabe
klassischer Lohnfertiger nicht akzeptieren [S, Marktbeobachtung].

**8. Zahlungsbereitschaft [S]** **400–1.200 €/Monat**.
Begründung: fünfstelliger Schaden, kaufmännisch rechenbarer Nutzen,
gewohnte ERP-Kosten. Aber: Kalkulationslogik ist **je Betrieb individuell**
(Maschinenstundensätze, Rüstzeiten, Materialaufschläge) →
**Sonderanfertigungsrisiko hoch – K.-o.-Kriterium 4 prüfen.**

**9. Kanäle** **Bundesverband Metall (BVM)** + Landesinnungsverbände;
**VDMA** (eher für größere); Messen **AMB Stuttgart**, **EMO Hannover**,
**Blechexpo Stuttgart**, **EuroBLECH Hannover**;
Fachmedien **MM MaschinenMarkt**, **blechnet**, **Fertigung**,
**mav – Innovation in der spanenden Fertigung**;
Werkzeug-/Maschinenhändler (Hoffmann Group, Hahn+Kolb) als Partner.

**10. Zyklus** **60–150 Tage** [A].

**11. Einwände** „Unsere Kalkulation ist unser Betriebsgeheimnis";
„Jedes Teil ist anders"; ERP-Integration; Angst vor Preistransparenz.

**12. 100k MRR** Bei 700 €/Monat: **143 Kunden** [S] – bei geschätzt
5.000–8.000 Lohnfertigern wären das **1,8–2,9 % Marktanteil** [S].
Machbar, aber Standardisierbarkeit ist der Schwachpunkt.

---

### ZG 16 – Entsorgungs- und Containerdienste

**1. Anzahl** **ca. 11.000 Unternehmen** in der Entsorgungswirtschaft mit
**ca. 280.000 Beschäftigten** und **ca. 80 Mrd. €** Jahresumsatz –
BMUV, „Abfallwirtschaft in Deutschland 2025" [F].
Reine **Containerdienste** als Teilmenge: **[A] ca. 1.500–3.000 – nicht verifiziert.**

**2. Größe** [A] Containerdienst typisch 8–40 Mitarbeitende, 2–15 Mio. € Umsatz,
5–30 Fahrzeuge.

**3. Entscheider** Inhaber/Geschäftsführer, 40–60 [A], praktisch orientiert,
mittlere Digitalaffinität.

**4. Konkretes Problem**
**Die Auftragsannahme ist fast vollständig telefonisch und hochgradig
standardisiert**: Containergröße, Abfallart, Stellplatz-Adresse, Stell- und
Abholtermin, Ansprechpartner. Genau diese Standardisierung macht die Zielgruppe
technisch attraktiv – und die Nichterreichbarkeit teuer, weil der Anrufer
(Bauherr, Handwerker, Privatkunde) sofort den nächsten Anbieter wählt.
Zweitproblem: Disposition der Abrollkipper und Nachweisführung (eANV).

**5. Schaden [S] – M1, hohe Umwandlungsquote**
A = 40 · T = 250 · u = 20 % · n = 60 % (fast jeder Anruf ist eine Bestellung)
· v = 50 % · c = 75 % · W = 380 € [A]
```
40 × 250 = 10.000 → ×0,20 = 2.000 → ×0,60 = 1.200 → ×0,50 = 600 → ×0,75 = 450
450 × 380 € = 171.000 € entgangener Umsatz/Jahr [S] · DB 35 % = 59.850 €/Jahr [S]
```
**Höchste Umwandlungsquote aller Zielgruppen** – weil der Anruf selbst schon
die Bestellung ist. Das ist der technisch sauberste Anwendungsfall
für automatisierte Auftragsannahme im gesamten Feld.

**6. Heute** Branchensoftware (**tegos enwis**, **RESY**, **ZEUS**,
**Abfallmanager**, **Recy/Recycling-Software**), Telefon,
teils Online-Shops für Containerbestellung (Containerdienst-Portale wie
**Containerdienst.de**, **Schuttflix** – letzteres ein finanzierter
Plattformwettbewerber).

**7. Unzufriedenheit** Nicht belegt – **Lücke**.
**Friedhofsprüfung nötig:** Schuttflix und ähnliche Plattformen haben versucht,
die Bestellung zu digitalisieren; die Marktreaktion ist zu prüfen.

**8. Zahlungsbereitschaft [S]** **400–1.000 €/Monat**.
Begründung: hoher Schaden, klar rechenbare Auftragswerte, gewohnte
Software- und Telematikkosten.

**9. Kanäle** **BDE Bundesverband der Deutschen Entsorgungs-, Wasser- und
Rohstoffwirtschaft**, **bvse** (mittelständisch geprägt – der bessere Kanal),
**VKU** (kommunal); Messe **IFAT München** (2026, Weltleitmesse);
Fachmedien **EUWID Recycling und Entsorgung**, **RECYCLING magazin**,
**ENTSORGA-Magazin**; Branchensoftware-Anbieter (tegos) als Partner.

**10. Zyklus** **30–90 Tage** [A].

**11. Einwände** „Unsere Kunden sind Stammkunden vom Bau";
„Preisauskunft am Telefon ist Verhandlungssache" (Preisdifferenzierung nach
Kunde – eine Automatisierung darf nicht die Preisstruktur offenlegen);
Abfallrecht/Nachweisführung; Branchensoftware-Integration.

**12. 100k MRR** Bei 650 €/Monat: **154 Kunden** [S].
Bei geschätzt 1.500–3.000 Containerdiensten wären das **5–10 % Marktanteil** –
**zu hoch. Konzentrationsrisiko: Der Markt ist zu klein für 100k MRR allein.**
Nur als margenstarkes Zweitsegment neben einer größeren Zielgruppe sinnvoll.

---

### ZG 17 – Garten- und Landschaftsbau (GaLaBau)

**1. Anzahl** **19.898 landschaftsgärtnerische Fachbetriebe** (2025), davon
**4.254 in den elf GaLaBau-Landesverbänden des BGL organisiert** – BGL-
Branchenstatistik 2025 [F].

**2. Größe** Umsatz **11,11 Mrd. €** (2025, **+4,3 %** gegenüber 10,65 Mrd. €),
**131.746 Beschäftigte** – Höchststand; **16. Wachstumsjahr in Folge** – BGL [F].
Rechnerisch **558.000 € Umsatz je Betrieb**, **6,6 Beschäftigte je Betrieb** [S].

**3. Entscheider** Inhaber/Landschaftsgärtnermeister, 40–58 [A],
mittlere Digitalaffinität.

**4. Konkretes Problem** Extreme **Saisonalität**: Februar bis Mai kommt die
Masse der Privatkundenanfragen, genau dann sind alle Kolonnen draußen und das
Büro einfach besetzt. Angebote werden mit Wochen Verzug erstellt.
Zusätzlich: Pflegeverträge (wiederkehrend, margenstark) werden nicht
systematisch verkauft.

**5. Schaden [S] – M1, saisonal gewichtet**
Saison (80 Arbeitstage Feb–Mai): A = 25 · u = 30 %;
Rest (140 Tage): A = 10 · u = 15 %
```
Saison: 25 × 80 = 2.000 → ×0,30 = 600
Nebensaison: 10 × 140 = 1.400 → ×0,15 = 210
Summe unbeantwortet = 810
× n 30 % Neuanfragen = 243 → × v 50 % = 121 → × c 25 % = 30 Aufträge
30 × 4.500 € Ø Auftragswert [A] = 135.000 € entgangener Umsatz/Jahr [S]
× DB 28 % = 37.800 €/Jahr [S]
```
Zusatz: 200 Bestandskunden ohne Pflegevertrag [A]; 10 % abschließbar bei
aktiver Ansprache = 20 × 1.200 €/Jahr = **24.000 € wiederkehrender Umsatz** [S].

**6. Heute** Handwerkersoftware/GaLaBau-Software (DATAflor, KWP,
Streit, ProAgrar), Handy, Bürokraft in Teilzeit.

**7. Unzufriedenheit** Nicht belegt – **Lücke**.
**Wichtiges Gegensignal: Die Branche wächst seit 16 Jahren [F].** Wachsende
Branchen haben weniger Leidensdruck bei „verpassten Anfragen", weil sie
ohnehin ausgelastet sind. Das **senkt** die Dringlichkeit erheblich,
anders als bei SHK/Elektro/Dachdecker mit rückläufigen Umsätzen [F].

**8. Zahlungsbereitschaft [S]** **150–350 €/Monat**.
Gedämpft durch Betriebsgröße (6,6 Beschäftigte [S]) und durch die Tatsache,
dass Auslastung nicht das Problem ist. Saisonalität bedroht zusätzlich die
MRR-Stabilität (Kündigungswelle im Herbst).

**9. Kanäle** **BGL** + 11 Landesverbände (nur 4.254 von 19.898 Betrieben
organisiert [F] – der Verbandskanal deckt nur **21 %** des Marktes ab, das ist
eine wichtige Einschränkung); Messe **GaLaBau Nürnberg** (2026, Leitmesse);
Fachmedien **DEGA GALABAU**, **Neue Landschaft**, **TASPO**;
Baumaschinen-/Baustoffhändler und Pflanzengroßhandel als Partner.

**10. Zyklus** **14–45 Tage** [A], stark saisonabhängig
(Vertriebsfenster faktisch Oktober–Januar).

**11. Einwände** „Wir sind bis August ausgebucht"; Saisonalität;
Preissensibilität; „Meine Kunden kommen über Empfehlung".

**12. 100k MRR** Bei 250 €/Monat: **400 Kunden** = **2,0 %** des Marktes [S].
Zu viele Kunden, zu niedriger ARPU, zusätzlich Saison-Churn. **Abwerten.**

---

### ZG 18 – Facility Management / Gebäudedienstleister

**1. Anzahl** **[A] ca. 25.000–30.000 Unternehmen im Gebäudeservice – in dieser
Session nicht verifiziert.** Belegt: die **25 führenden Facility-Service-
Unternehmen** erzielten **18,7 Mrd. € Umsatz** (2024, **+7,8 %**) und decken
**mehr als 30 % des deutschen Facility-Service-Marktes** ab – Lünendonk-Studie
2025 [F]. Beschäftigte bei Facility-Service-Anbietern: **291.792** (2024, +1,6 %) [F].
Für 2026 prognostizieren die Anbieter **+8–9 %** Umsatzwachstum, gestützt vom
Infrastruktur-Sondervermögen des Bundes [F].

**2. Größe** Hoch konzentriert: Top 25 = >30 % Marktanteil [F].
Mittelständisches Zielsegment: [A] 5–50 Mio. € Umsatz, 100–800 Mitarbeitende.

**3. Entscheider** Geschäftsführung, Leiter Operations, IT-Leitung.
Professionelle Beschaffung, Ausschreibungsprozesse.

**4. Konkretes Problem** **Störmeldungsannahme und SLA-Einhaltung.**
Ein FM-Dienstleister betreibt eine Störmeldezentrale; verpasste oder zu spät
bearbeitete Meldungen führen zu **SLA-Verletzungen mit Vertragsstrafen**.
Zusätzlich: Nachweisführung gegenüber dem Auftraggeber, Einsatzsteuerung
verteilter Objektteams, hohe Personalfluktuation.
Belegt als Branchenherausforderung: **Personalmangel, Verzögerungen bei der
Digitalisierung, steigende ESG-Anforderungen** – Lünendonk 2025 [F].

**5. Schaden [S] – SLA-Pönalen + M2**
FM-Dienstleister mit 15 Mio. € Umsatz [A]:
SLA-Pönalen typisch **0,5–2 % des Auftragswerts** [A]
```
15.000.000 × 0,01 (Mittelwert 1 %) = 150.000 €/Jahr Vertragsstrafen [S]
davon 40 % durch bessere Meldungsannahme/Eskalation vermeidbar = 60.000 €/Jahr [S]
```
M2 (Störmeldezentrale): 120 Meldungen/Tag × 250 × 4 Min = 2.000 h/Jahr
× 42 €/h = **84.000 €/Jahr**; 50 % automatisierbar = **42.000 €** [S].
**Gesamt ca. 102.000 €/Jahr** [S].

**6. Heute** CAFM-Systeme (Planon, pit-FM, Spartacus, IMSWARE, Wave,
Archibus), Ticketsysteme, eigene Leitstellen, teils 24/7-Callcenter
(bereits bezahlt – ein belegter Vergleichsmarkt).

**7. Unzufriedenheit** Belegt: „Verzögerungen in der Digitalisierung" als
zentrale Herausforderung – Lünendonk 2025 [F].

**8. Zahlungsbereitschaft [S]** **1.000–5.000 €/Monat** im Mittelstand;
Konzern-FM **10.000 €+**. Begründung: sechsstelliger Schaden,
professionelle Beschaffung, bereits bezahlte Leitstellen als Preisanker.

**9. Kanäle** **GEFMA** (Deutscher Verband für Facility Management),
**RealFM**, **BIV Bundesinnungsverband des Gebäudereiniger-Handwerks**;
Messen **INservFM Frankfurt**, **Servparc**;
Fachmedien **Der Facility Manager**, **facility-management.de**,
**Lünendonk-Listen** (Adressquelle der Top-Anbieter);
CAFM-Anbieter als Partner.

**10. Zyklus** **150–360 Tage** [A] – Ausschreibungen, IT-Sicherheitsprüfungen,
Datenschutz-Audits. **Längster Zyklus der Analyse.**

**11. Einwände** „Wir haben eine eigene Leitstelle"; Ausschreibungszwang;
IT-Sicherheitsanforderungen (ISO 27001, teils TISAX);
Integration in CAFM; „unsere Auftraggeber schreiben das System vor".

**12. 100k MRR** Bei 2.500 €/Monat: **40 Kunden** [S] – **beste
Konzentration der gesamten Analyse.** Aber: längster Verkaufszyklus,
höchste Einstiegshürden, und die Top-25-Konzentration bedeutet, dass wenige
Großkunden das Modell dominieren würden → **Klumpenrisiko** und Abhängigkeit
von Konzernen (Nicos Anti-Kriterium).

---

### ZG 19 – Landwirtschaftliche Lohnunternehmer

**1. Anzahl** **ca. 2.000 Lohnunternehmen** mit **30.000 Mitarbeitenden** sind im
**BLU** (12 Landesverbände/-gruppen) organisiert – BLU [F].
Gesamtzahl je nach Definition höher; **[A] 3.000–5.000 insgesamt – nicht verifiziert.**

**2. Größe** Rechnerisch **15 Mitarbeitende je Betrieb** [S: 30.000/2.000];
[A] Umsatz 800 T€ – 4 Mio. €.

**3. Entscheider** Inhaber, 38–58 [A], **technikaffin** (Präzisionslandwirtschaft,
GPS-Lenksysteme, ISOBUS, Telemetrie sind Alltag) – deutlich digitaler als das
Bauhandwerk.

**4. Konkretes Problem** **Extreme Saisonspitzen** (Silage, Ernte, Gülle,
Aussaat): In einem 10-Tage-Wetterfenster rufen 200 Landwirte an, alle wollen
sofort. Die Einsatzplanung passiert im Kopf des Inhabers, nachts.
Dokumentation der erbrachten Leistungen (ha, m³, Stunden) für die Abrechnung
ist unvollständig → **Abrechnungsverluste**.

**5. Schaden [S] – Abrechnungsverlust + M2**
Umsatz 1,8 Mio. € [A]; **4 % nicht oder zu niedrig abgerechnete Leistungen**
(fehlende Stundenzettel, vergessene Zuschläge, Rüstzeiten) [A]
```
1.800.000 × 0,04 = 72.000 €/Jahr [S]
```
M2 (Einsatzplanung/Telefon in der Saison): 60 Tage × 3 h/Tag × 85 €/h
Inhaber-Vollkosten = **15.300 €/Jahr** [S].
**Gesamt ca. 87.300 €/Jahr** [S].

**6. Heute** Ackerschlagkarteien und Lohnunternehmer-Software
(**agrirouter**, **365FarmNet**, **NEXAT/Farmpilot**, **LU-Soft**,
**Agrarbüro**), Papier-Stundenzettel, WhatsApp.

**7. Unzufriedenheit** Nicht belegt – **Lücke**.

**8. Zahlungsbereitschaft [S]** **300–800 €/Monat**.
Begründung: fünfstelliger Schaden, technikaffiner Käufer, gewohnte
Maschinen-/Softwareinvestitionen (ein Häcksler kostet sechsstellig – die
Preisanker sind hoch). Aber: **extreme Saisonalität des Cashflows**
(Zahlungen kommen nach der Ernte) → Jahresvorauszahlung anbieten.

**9. Kanäle** **BLU** + 12 Landesverbände/-gruppen (erreicht ~2.000 Betriebe
direkt [F] – **hohe Kanalabdeckung**); Messe **Agritechnica Hannover** (2027,
Weltleitmesse); Fachmedien **Lohnunternehmen (Beckmann Verlag)**, **profi**,
**traction**, **top agrar**; Landmaschinenhändler und -hersteller
(Claas, John Deere, Fendt/AGCO, Krone) als Partner.

**10. Zyklus** **30–90 Tage** [A], Vertriebsfenster Winter (Nov–Feb).

**11. Einwände** „In der Saison habe ich keine Zeit für Software";
Funknetzabdeckung auf dem Feld; „meine Fahrer sind keine Techniker";
Saisonalität des Cashflows.

**12. 100k MRR** Bei 500 €/Monat: **200 Kunden** = **10 % aller BLU-Mitglieder** [S].
**Marktanteil viel zu hoch. Der Markt ist mit ~2.000–5.000 Betrieben zu klein
für 100k MRR.** Nur als Nische mit sehr hohem ARPU oder als Zusatzsegment.

---

### ZG 20 – Sicherheitsdienstleister

**1. Anzahl** **4.517 Unternehmen** in der privaten Sicherheitswirtschaft;
zusätzlich **666 klassische Detekteien** (fast halbiert seit 2014: 1.211).
**Der BDSW hat 1.029 Mitgliedsunternehmen** – BDSW [F].

**2. Größe** **290.871 Beschäftigte** (Stichtag 30.06.2025) – Höchststand,
davon **276.987** in privaten Sicherheits- und Wachdiensten;
Branchenumsatz **14,02 Mrd. €** (2024), Prognose **14,75 Mrd. €** (2025) – BDSW [F].
Die **Top 25** erzielten **5.628,1 Mio. €** sicherheitsrelevanten Umsatz
(GJ 2025) = ca. **40 % des Marktvolumens** mit **97.400 Beschäftigten**
(ca. ein Drittel aller Branchenbeschäftigten) – Lünendonk-Liste 2025 [F].
Rechnerisch: **3,27 Mio. € Umsatz** und **64 Beschäftigte je Unternehmen** [S].

**3. Entscheider** Geschäftsführer / Einsatzleiter / Disponent.
Digitalaffinität niedrig bis mittel; belegtes Branchensignal:
„Sicherheitsdienstleister werden digital" (Lünendonk) [F] – der Wandel läuft gerade.

**4. Konkretes Problem** **Schicht- und Ausfalldisposition.** Ein kurzfristiger
Ausfall (Krankheit) muss binnen Minuten nachbesetzt werden, sonst greift eine
Vertragsstrafe oder der Objektschutz ist nicht erfüllt. Das passiert
telefonisch, oft nachts, durch den Einsatzleiter. Zusätzlich: hohe Fluktuation,
Nachweisführung (Bewachungsverordnung, Sachkundenachweis § 34a GewO),
Dokumentation von Streifengängen.

**5. Schaden [S] – Ausfallnachbesetzung + M2**
Unternehmen mit 200 Mitarbeitenden [A]:
Ausfälle 250/Jahr [A] × 8 h × **14 € Mehrkosten je Stunde**
(Überstunden-, Nacht-, Feiertagszuschläge, Subunternehmereinsatz) [A]
```
250 × 8 × 14 € = 28.000 €/Jahr [S]
```
M2 (Dispositionsaufwand): 2 h/Tag × 365 × 45 €/h = **32.850 €/Jahr** [S];
60 % automatisierbar (Verfügbarkeitsabfrage, Schichtangebot, Bestätigung)
= **19.700 €** [S].
Vertragsstrafen bei Nichtbesetzung: [A] 15.000 €/Jahr.
**Gesamt ca. 62.700 €/Jahr** [S].

**6. Heute** Dienstplan-/Dispositionssoftware (**Securitas-Eigenentwicklungen**,
**Sicherheitsdienst-Software**, **Papershift**, **Plano**, **GFOS**),
Telefon/WhatsApp-Gruppen, Excel.

**7. Unzufriedenheit** Belegt indirekt: „Fachkräftemarkt zeigt erste Entspannung"
bei gleichzeitig verdoppeltem Umsatz [F] – die Branche wächst schneller als
ihre Prozesse. Lünendonk-Studientitel „Sicherheitsdienstleister werden digital" [F].

**8. Zahlungsbereitschaft [S]** **400–1.200 €/Monat** im Mittelstand;
Top-25-Unternehmen haben Eigenentwicklungen und sind schwer angreifbar.
Begründung: Personalkostenanteil >75 %, jede Effizienz an dieser Stelle zählt;
aber die Branche ist **preisgetrieben** (Ausschreibungen nach billigstem Angebot)
und arbeitet mit sehr dünnen Margen.

**9. Kanäle** **BDSW** (1.029 Mitglieder [F]) + **BDGW** (Geld/Wert);
Messe **Security Essen** (2026, Weltleitmesse);
Fachmedien **PROTECTOR**, **WiK Zeitschrift für Sicherheit in der Wirtschaft**,
**Sicherheit.info**; Lünendonk-Liste als Adressquelle für Großanbieter.

**10. Zyklus** **60–150 Tage** [A].

**11. Einwände** „Bei uns ist alles Objekt-individuell"; Tarifbindung und
Betriebsrat bei größeren Anbietern; § 34a-GewO-Nachweise;
extremer Preisdruck durch Ausschreibungen.

**12. 100k MRR** Bei 700 €/Monat: **143 Kunden** = **3,2 %** aller
4.517 Unternehmen [S]. Bei 4.517 Unternehmen und starker
Top-25-Konzentration ist der adressierbare Mittelstand klein.
**Konzentrationsrisiko – nur als Zweitsegment.**

---

### ZG 21 – Küchen-/Möbelstudios und Fensterbauer

**1. Anzahl** **[A] Küchenstudios ca. 3.000–4.500; Fensterbau-Fachbetriebe
ca. 4.000–6.000; Tischlereien/Schreinereien ca. 33.000–38.000 – in dieser
Session nicht verifiziert** (zu prüfen: Verband der Küchenspezialisten,
Verband Fenster + Fassade (VFF), Tischler Schreiner Deutschland, ZDH-Datenbank).

**2. Größe** [A] Küchenstudio 3–12 Mitarbeitende, 800 T€ – 4 Mio. € Umsatz;
Fensterbauer 8–40 Mitarbeitende, 1,5–12 Mio. €.

**3. Entscheider** Inhaber, 42–60 [A], vertrieblich denkend
(Küchenstudios sind faktisch Einzelhandel mit Beratungsverkauf).

**4. Konkretes Problem** **Sehr hohe Auftragswerte bei sehr wenigen Kontakten.**
Ein Küchenkauf hat einen Wert von 12.000–25.000 € [A]. Ein verpasster
Beratungstermin ist damit außergewöhnlich teuer. Gleichzeitig ist das Studio
während der Beratungsgespräche telefonisch nicht erreichbar –
Beratung dauert 2–3 Stunden, in denen niemand ans Telefon geht.
Zweitproblem: **Nachfassen bei abgegebenen Planungen** findet kaum statt,
obwohl die Abschlussquote dadurch massiv steigt.

**5. Schaden [S] – M1, hoher Auftragswert**
A = 15 · T = 250 · u = 25 % · n = 30 % · v = 55 % · c = 25 %
· W = 15.000 € Küchenauftrag [A]
```
15 × 250 = 3.750 → ×0,25 = 937 → ×0,30 = 281 → ×0,55 = 154 → ×0,25 = 38 Aufträge
```
Das ist zu hoch gegriffen; ein Studio verkauft real 80–200 Küchen/Jahr [A].
Realistischer, an der Terminlogik ausgerichtet:
```
2 verpasste Beratungstermine/Woche × 46 = 92 Termine
× 55 % endgültig verloren = 50 → × 30 % Abschlussquote = 15 Küchen
15 × 15.000 € = 225.000 € entgangener Umsatz/Jahr [S] · DB 30 % = 67.500 € [S]
```
Zusatz: 250 abgegebene Planungen/Jahr [A]; 50 % ohne Nachfassen;
davon 8 % kämen bei systematischem Nachfassen doch = 10 Küchen × 15.000 €
= **150.000 € Umsatz**, DB 30 % = **45.000 €/Jahr** [S].
**Gesamt ca. 112.500 € entgangener Deckungsbeitrag/Jahr** [S] –
**höchster DB-Schaden je Einzelbetrieb außerhalb von Autohaus/Spedition.**

**6. Heute** Küchenplanungssoftware (**Carat**, **Winner Flex**, **KPS**),
Verbundgruppen-Systeme, Terminkalender, Telefon.

**7. Unzufriedenheit** Nicht belegt – **Lücke**.
Marktkontext: Küchen- und Möbelhandel leidet 2024/25 unter Konsumzurückhaltung
und der Bau-/Umzugsflaute → sinkende Frequenz **erhöht** den Wert jedes
einzelnen Kontakts erheblich. Das ist ein starkes Timing-Argument [S].

**8. Zahlungsbereitschaft [S]** **400–1.000 €/Monat**.
Begründung: Ein einziger zusätzlich gewonnener Küchenauftrag pro Jahr
(4.500 € DB) refinanziert 375 €/Monat vollständig. Diese Rechnung ist
für einen Küchenverkäufer sofort einleuchtend – **die einfachste
ROI-Argumentation der gesamten Analyse.**

**9. Kanäle** **Verbundgruppen als dominanter Kanal**: **Der Kreis**,
**MHK Group**, **DER KREIS**, **Küchengilde**, **Einrichtungspartnerring VME**,
**Begros**, **Garant** – über eine Verbundgruppe erreicht man 300–1.500
Studios auf einmal; **Verband der Küchenspezialisten (VdDK)**;
Messen **area30 / Küchenmeile A30** (Löhne), **imm cologne**,
**LivingKitchen**; Fachmedien **Küchenplaner**, **KÜCHE**, **möbel kultur**,
**Der Küchenprofi**.
Fensterbau separat: **VFF Verband Fenster + Fassade**, Messe
**Fensterbau Frontale Nürnberg** (2026), Fachmedien **GW Glaswelt**, **BM**.

**10. Zyklus** **21–60 Tage** [A]; über Verbundgruppe 120–240 Tage
für den Rahmenvertrag [A].

**11. Einwände** „Beratung ist Vertrauenssache, das kann keine Maschine";
„Meine Verkäufer rufen selbst zurück" (tun sie nicht);
Verbundgruppen-Systemvorgaben; kleine Marktgröße.

**12. 100k MRR** Bei 600 €/Monat: **167 Kunden** [S].
Bei geschätzt 3.000–4.500 Küchenstudios = **3,7–5,6 % Marktanteil** –
**zu hoch als Einzelmarkt**; zusammen mit Fensterbauern und Möbelhäusern
(gemeinsame Logik: hoher Auftragswert, Beratungsverkauf, Studio) wird
der adressierbare Markt aber auf ~10.000 Betriebe erweitert → 1,7 % [S].
**Als kombiniertes Segment „beratungsintensiver Fachhandel" tragfähig.**

---

### ZG 22 – Energieberater und PV-Installateure

**1. Anzahl** **9.203 Photovoltaik-Installateure** (Stand Juni 2026, Adressdatenbank
listflix) [F-schwach – kommerzielle Adressdatenbank, keine Verbandsstatistik];
der **Bundesverband des Deutschen Solarhandwerks (BDSH)** schätzt
**8.000 PV-Unternehmen**; andere Quellen nennen **6.300** [F].
**46,1 % sind Kleinstunternehmen**, **76,7 % im Handelsregister eingetragen**;
Bayern führt mit **2.011** Installateuren [F].
Energieberater: **[A] ca. 13.000–15.000 Energieeffizienz-Experten in der
dena-Expertenliste – nicht verifiziert.**
Kontext: **4,8 Mio. Photovoltaikanlagen** waren zum Jahresende 2025 in
Deutschland installiert (Mitte 2025: 4,2 Mio.) – Destatis [F].

**2. Größe** [A] PV-Betrieb typisch 4–25 Mitarbeitende, 600 T€ – 6 Mio. €;
Energieberater häufig Einzelunternehmer oder Kleinstbüro (1–5 Personen).

**3. Entscheider** Inhaber, 32–50 [A] – **die jüngste und digitalste
Entscheidergruppe der gesamten Analyse**; viele Betriebe wurden erst
2020–2023 gegründet.

**4. Konkretes Problem – und warum es das falsche Problem ist**
Belegt: „Die vollen Auftragsbücher aus dem Boomjahr 2023 sind abgearbeitet –
nun bleibt vielerorts die Nachfrage nach Neuaufträgen aus" [F].
Das heißt: Das Problem ist **nicht** „wir verlieren Anfragen", sondern
**„es kommen keine Anfragen mehr"**. Das ist ein **völlig anderes Produkt**
(Leadgenerierung / Marketing) mit völlig anderer Ökonomie:
erfolgsabhängig, margenschwach, austauschbar, und in einem Markt mit
Insolvenzwelle.

**5. Schaden [S]** Ein Anrufannahme-Produkt hat hier den geringsten Wert
aller Zielgruppen, weil das Anrufaufkommen selbst eingebrochen ist.
Für ein Leadprodukt: Ein PV-Betrieb braucht 15 Aufträge/Monat à 18.000 €;
bei 25 % Abschlussquote sind das 60 qualifizierte Leads/Monat.
Fehlen davon 20, entgehen 5 Aufträge × 18.000 € = 90.000 €/Monat Umsatz [S] –
theoretisch riesig, praktisch aber ein **Leadkosten-Wettbewerb**, in dem
Maschine A gegen Aroundhome, DAA, Selfmade Energy, Enpal und
Facebook-Ads-Agenturen antreten müsste.

**6. Heute** PV-Planungssoftware (PV*SOL, Solar-Planit, Sunny Design),
Leadportale (**DAA Deutsche Auftragsagentur**, **Aroundhome**,
**Selfmade Energy**, **Solarwatt-Partnerprogramme**), Marketingagenturen.

**7. Unzufriedenheit** Belegt: Nachfrageeinbruch [F].
**Friedhofswarnung: Der PV-Markt hat 2024/25 eine Insolvenzwelle erlebt**
(u. a. Solarwatt-Restrukturierung, zahlreiche regionale Installateure).
Debitorenrisiko und Churn wären extrem hoch.

**8. Zahlungsbereitschaft [S]** **150–400 €/Monat** für Prozesssoftware –
und faktisch **null** für Prozessoptimierung, solange die Auftragsbücher leer
sind. Für Leads: **hoch, aber erfolgsabhängig** (60–250 € je qualifiziertem Lead
[A]) – das ist aber kein MRR-Modell, sondern Transaktionsgeschäft
und verstößt gegen Pflichtkriterium 1.

**9. Kanäle** **BSW-Solar**, **BDSH**, **DGS**; Messe **Intersolar Europe
München** (2026); Fachmedien **pv magazine**, **Solarserver**, **photovoltaik**;
Modul-/Wechselrichterhersteller-Partnerprogramme (SMA, Fronius, Huawei,
Meyer Burger); Energieberater über **GIH Bundesverband**, **DEN**,
**dena-Expertenliste**, Fachmedium **Gebäude-Energieberater**.

**10. Zyklus** **14–45 Tage** [A] – schnell, weil junge Entscheider.

**11. Einwände** „Ich brauche keine Anrufannahme, ich brauche Kunden";
Zahlungsfähigkeit; hoher Churn; „bringt mir das Aufträge? Dann zahle ich
pro Auftrag, nicht monatlich".

**12. 100k MRR** Bei 250 €/Monat: **400 Kunden** = **4,3–6,3 %** des Marktes [S].
**Ausschluss als Kernzielgruppe.** Falsches Problem, instabile Branche,
Insolvenzrisiko, erfolgsabhängige Preiserwartung.

---

## 3. Bewertung und Ranking

### 3.1 Bewertungslogik
Der Auftrag verlangt: **Problemstärke × Zahlungsbereitschaft × Erreichbarkeit ×
Delegierbarkeit der Betreuung**. Jede Dimension 0–10, multiplikativ (nicht additiv),
weil eine Null in einer Dimension die Zielgruppe tatsächlich wertlos macht –
ein riesiges Problem ohne Budget ist kein Geschäft.

Definitionen:
- **Problemstärke** – Höhe und Wiederkehr des Schadens relativ zum Betriebsergebnis,
  plus Dringlichkeit (Konjunkturlage).
- **Zahlungsbereitschaft** – belegter/ableitbarer ARPU **und** Weitergebbarkeit
  der Kosten an Dritte.
- **Erreichbarkeit** – Existenz konzentrierter Kanäle (Verbände, Verbundgruppen,
  Ketten, Softwarepartner) und Kaltakquisefähigkeit.
- **Delegierbarkeit der Betreuung** – kann eine angelernte Kraft Onboarding und
  laufende Betreuung in ≤ 6 Wochen übernehmen (Pflichtkriterium 4 und
  Nicos Anti-Kriterien)? Abzug für Fachwissen, Regulatorik, Individualisierung.

### 3.2 Gesamtranking (alle 22 Zielgruppen)

| Rang | Zielgruppe | Problem | Zahlung | Erreichbar | Delegierbar | Score (÷1000) |
|---|---|---|---|---|---|---|
| **1** | **Immobilien-/Hausverwaltungen** | 9 | 8 | 9 | 8 | **5,18** |
| **2** | **Autohäuser (fabrikatsgebunden)** | 8 | 9 | 8 | 9 | **5,18** |
| **3** | **Freie Kfz-Werkstätten** | 8 | 6 | 9 | 9 | **3,89** |
| **4** | **SHK-Betriebe** | 9 | 5 | 9 | 9 | **3,65** |
| **5** | **Zahnarztpraxen / Dental-MVZ** | 8 | 8 | 7 | 8 | **3,58** |
| **6** | **Steuerkanzleien** | 8 | 9 | 8 | 6 | **3,46** |
| 7 | Elektro-/E-Handwerke | 8 | 5 | 9 | 9 | 3,24 |
| 8 | Containerdienste/Entsorgung | 8 | 7 | 6 | 9 | 3,02 |
| 9 | Küchenstudios/Fensterbauer | 8 | 7 | 7 | 8 | 3,14 |
| 10 | Tierarztpraxen | 9 | 6 | 6 | 8 | 2,59 |
| 11 | Speditionen/Fuhrparks | 8 | 8 | 6 | 6 | 2,30 |
| 12 | Arztpraxen (GKV) | 9 | 6 | 6 | 7 | 2,27 |
| 13 | Dachdecker | 9 | 4 | 8 | 9 | 2,59 |
| 14 | Metallbau/CNC-Lohnfertigung | 7 | 7 | 6 | 5 | 1,47 |
| 15 | Facility Management | 7 | 9 | 6 | 5 | 1,89 |
| 16 | Sicherheitsdienste | 7 | 6 | 6 | 6 | 1,51 |
| 17 | Bauunternehmen | 8 | 8 | 5 | 4 | 1,28 |
| 18 | GaLaBau | 6 | 4 | 7 | 9 | 1,51 |
| 19 | Lohnunternehmer Landwirtschaft | 7 | 6 | 8 | 7 | 2,35 |
| 20 | Ambulante Pflegedienste | 9 | 4 | 7 | 5 | 1,26 |
| 21 | Maler/Lackierer | 6 | 3 | 7 | 9 | 1,13 |
| 22 | PV-Installateure/Energieberater | 4 | 3 | 7 | 8 | 0,67 |

*(Rang = Score; die Nummerierung 7–22 folgt der Score-Reihenfolge nur grob,
weil einzelne Zielgruppen zusätzlich wegen Marktgröße abgewertet wurden –
siehe Spalte „Konzentrationsrisiko" in 3.3.)*

### 3.3 Korrekturfaktor Marktgröße (Konzentrationsrisiko)
Score allein reicht nicht. Entscheidend ist, **welchen Marktanteil** Maschine A
für 100.000 € MRR braucht. Über 2 % Marktanteil in einem fragmentierten
KMU-Markt ist ohne Verbandspartnerschaft unrealistisch.

| Zielgruppe | ARPU [S] | Kunden für 100k MRR | Marktanteil nötig | Bewertung |
|---|---|---|---|---|
| Autohäuser | 1.200 € | **83** | 0,6 % | ✅ sehr gut |
| Steuerkanzleien | 800 € | **125** | 0,23 % | ✅ sehr gut |
| Immobilienverwaltungen | 1.000 € | **100** | ~0,45 % | ✅ sehr gut |
| Zahnarztpraxen (+MVZ) | 550/4.200 € | **128** | ~0,3 % | ✅ sehr gut |
| Speditionen | 1.500 € | **67** | ~1 % | ✅ gut |
| Facility Management | 2.500 € | **40** | ~0,15 % | ✅ gut (aber Zyklus) |
| Freie Kfz-Werkstätten | 350 € | **286** | 1,3 % | ⚠️ grenzwertig |
| Elektrobetriebe | 300 € | **333** | 0,68 % | ⚠️ Kundenzahl hoch |
| SHK | 250 € | **400** | 0,83 % | ⚠️ Kundenzahl hoch |
| Küchenstudios (nur) | 600 € | **167** | 3,7–5,6 % | ❌ Markt zu klein |
| Containerdienste | 650 € | **154** | 5–10 % | ❌ Markt zu klein |
| Lohnunternehmer | 500 € | **200** | ~10 % (BLU) | ❌ Markt zu klein |
| GaLaBau | 250 € | **400** | 2,0 % | ❌ ARPU + Saison |
| Dachdecker | 220 € | **455** | 3,0 % | ❌ zu viele Kunden |
| Maler | 150 € | **667** | ~1,7 % | ❌ Kundenzahl absurd |
| PV | 250 € | **400** | 4,3–6,3 % | ❌ falsches Problem |

**Zentrale Erkenntnis:** Die Zielgruppen mit dem *größten* Problem
(Dachdecker 13,5 % Umsatzschaden, SHK, Pflege) sind fast durchweg die mit der
*niedrigsten* Zahlungsbereitschaft und der *höchsten* nötigen Kundenzahl.
**Problemgröße und Zahlungsbereitschaft sind in diesem Markt negativ korreliert** –
weil kleine Betriebe die größten Lücken und die kleinsten Budgets haben.
Wer dem Schmerz folgt, landet bei 400–700 Kleinkunden und damit bei genau dem
Geschäftsmodell, das Nico ausgeschlossen hat.

### 3.4 Empfohlene Marktarchitektur
Aus der Analyse folgt keine „eine Zielgruppe", sondern eine **Zwei-Segment-Struktur**:

**Segment A – Ankerkunden (60 % des MRR, ~60–80 Kunden):**
Immobilienverwaltungen, Autohäuser, Steuerkanzleien.
ARPU 1.000–2.500 €, lange Zyklen, sehr niedriger Churn, hohe Bonität.
Diese Kunden finanzieren das Team und erzeugen den Unternehmenswert.

**Segment B – Volumensegment (40 % des MRR, ~150–200 Kunden):**
Freie Kfz-Werkstätten und SHK-Betriebe, erschlossen **ausschließlich über
Multiplikatoren** (Werkstattkonzepte, SHK-Großhandel), nie über Einzelakquise.
ARPU 250–450 €, standardisiertes Self-Onboarding, Support über Wissensdatenbank
und angelernte Kraft.

Rechnung: 70 × 1.400 € = 98.000 € + 180 × 350 € = 63.000 € → **161.000 € MRR**
mit **250 Kunden** [S]. Das erreicht sogar die in 01_nordstern genannte
Zielgröße von ca. 190.000 € Monatsumsatz für 30.000 € netto privat –
mit 300–320 Kunden [S].

### 3.5 Was diese Analyse NICHT beantwortet (Übergaben)

| Offene Frage | An wen |
|---|---|
| Reale Nichtannahmequote am Telefon – **muss gemessen werden**, alle kursierenden Zahlen sind Anbietermarketing | MVP-Plan / Pilotmessung |
| Warum kündigen Betriebe ihr Telefonsekretariat? Churn-Gründe bestehender Anbieter | Agent 11 (Kundensignale) |
| Nicht verifizierte Betriebszahlen: Maler, Bau, Metallbau, Küchenstudios, Fensterbauer, Immobilienverwaltungen, Arztpraxen, Zahnarztpraxen, Energieberater | Nachrecherche mit freiem Suchkontingent |
| Friedhofsprüfung: Repareo/caroobi/Autobutler (Kfz), Schuttflix (Container), gescheiterte Handwerker-Plattformen | Agent 10 (Copy & Improve) |
| Wettbewerbspreise konkreter KI-Telefonanbieter (agentino, vokaro, telewa u. a.) und deren Kundenzahl | Agent 03 (Wettbewerb) |
| Ob die Verbands-/Verbundgruppenkanäle tatsächlich Partnerprogramme öffnen | Agent 06 (Delegation/Go-to-Market) |
| DATEV-Marktplatz-Aufnahmebedingungen; § 203 StGB-Konstruktion | Agent 08 (Risiko/Regulierung) |
| Ob Nico Hausverwaltungen und Kanzleien als Kundschaft dauerhaft interessant findet (Anzug-Business-Nähe) | Agent 09 (Persönlichkeits-Fit) |

---

## 4. Quellenverzeichnis (in dieser Session verifiziert)

| Quelle | Verwendet für |
|---|---|
| ZDH – Kennzahlen des Handwerks 2025 / Wirtschaftlicher Stellenwert 2025 (zdh.de) | 1.038.126 Betriebe, 783,2 Mrd. € |
| ZVSHK – SHK-Handwerk Jahresbilanz 2024/2025 (zvshk.de, sbz-online.de) | 48.050 Betriebe, 59,12 Mrd. €, 390.000 Beschäftigte, −4 % |
| ZVEH – Branchenkennzahlen der E-Handwerke 2024/2025 (zveh.de, elektrowirtschaft.de, pv-magazine.de) | 49.113 Unternehmen, 88,2 Mrd. €, 451.050 Beschäftigte, 46.403 Azubis |
| ZDK – Jahresbilanz Kfz-Gewerbe (kfzgewerbe.de, krafthand.de, autohaus.de) | 36.170 Betriebe (14.120/22.050), 207,3 Mrd. €, 428.000 Beschäftigte |
| ZVDH – Steckbrief/Geschäftsbericht, Stand 31.12.2025 (dachdecker.org, ddh.de) | 15.241 Betriebe, 13,5 Mrd. €, 61.723 AN, 78 % < 10 AN |
| BGL Bundesverband Garten-, Landschafts- und Sportplatzbau – Branchenstatistik 2025 | 19.898 Betriebe, 11,11 Mrd. €, 131.746 Beschäftigte, 4.254 organisiert |
| BStBK – Berufsstatistik 2025, Stand 01.01.2026 (bstbk.de) | 105.953 Mitglieder, 53.932 Praxen, 88.995 StB, 14.670 Gesellschaften, 17.081 Azubis, 65,9 % selbstständig |
| VDIV Deutschland – Branchenbarometer 2025 (vdiv.de) | 70 % Überlastung, 57 % Mandatsabgabe, 14 % Aufnahmestopp, 80 % Automatisierungsinvestition, +12 % Preise, +7,8 % Umsatz |
| pflegemarkt.com / MD-Bericht / Destatis Pflegestatistik | 17.938–17.976 Dienste, 2.275.280 Patienten, 15.549 amtlich, 623/292 Gründungen/Schließungen |
| DSLV / BGL / VerkehrsRundschau / eurotransport | 592.622 Beschäftigte, 123,1 Mrd. €, 64 % Dispo-Stellen unbesetzbar, 70.000 fehlende Fahrer, Mindestlohn 13,90/14,60 € |
| BDSW / Lünendonk-Liste 2025 (bdsw.de, luenendonk.de) | 4.517 Unternehmen, 290.871 Beschäftigte, 14,02/14,75 Mrd. €, Top 25 = 5.628,1 Mio. € |
| BMUV – Abfallwirtschaft in Deutschland 2025 | ca. 11.000 Unternehmen, 280.000 Beschäftigte, ca. 80 Mrd. € |
| Lünendonk – Facility Service in Deutschland 2025 | Top 25 = 18,7 Mrd. €, +7,8 %, >30 % Marktanteil, 291.792 Beschäftigte |
| KZBV – Statistisches Jahrbuch 2025 (kzbv.de, rebmann-research.de) | 677.000 € Ø Praxisumsatz, 30,0 Mrd. € gesamt |
| KBV/IGES – PraxisBarometer Digitalisierung 2025, n=1.700 (kbv.de, iges.com) | 40 % Online-Termin, 45 % Online-Rezept, 44 % DiGA, 87 % eArztbrief, eRezept 63→77 % |
| Bundestierärztekammer – Tierärztestatistik 2025 | 46.089 approbiert, 34.476 tätig, rückläufige Praxiszahlen |
| BLU Bundesverband Lohnunternehmen | ca. 2.000 Lohnunternehmen, 30.000 Mitarbeitende, 12 Landesverbände |
| BDSH / Solarmonitor 2025 / Destatis / listflix | 9.203 bzw. 8.000 bzw. 6.300 PV-Betriebe, 46,1 % Kleinstunternehmen, 4,8 Mio. PV-Anlagen |
| **Bitkom/ZDH – Digitalisierung des Handwerks 2025, n=504** | **KI 4 %/9 %, 69 % Investitionshürde, 52 % Sorge, 29 % KI-Kompetenz, Note 3,0, 85 % digitale Services, 76 % Zeitersparnis** |
| **KfW – Digitalisierungsbericht Mittelstand 2025** | **23,8 Mrd. €, Kleine 73 %/24 %, Große 2 %/41 % (9,2 Mrd. €), Trend 31 %→24 %** |
| Preisvergleiche Handwerkersoftware (trusted.de, gruenderkueche.de) + Anbieterpreisseiten (HERO, Meisterwerk, Lexware, Bosch) | 15–120 €/Nutzer/Monat |
| Telefonservice-Anbieterpreisseiten (phonea, Mobile Office, officehelden, cloudsecretary) | 50–250 €/Monat, 0,99–1,70 €/Anruf, 24/7 +29,50 €/Monat |

**Nicht als Quelle verwendet (Anbietermarketing ohne Primärbeleg):**
agentino.de, telewa.de, vokaro.net, easy-kiagentur.de, klickautomation.com,
digitalolymp.ch, servasbot.at, starbuero.de, digital-rezeption.de.

---

*Ende Agent 04.*
