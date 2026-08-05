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
