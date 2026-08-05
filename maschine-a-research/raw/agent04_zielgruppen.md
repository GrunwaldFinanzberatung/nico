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
