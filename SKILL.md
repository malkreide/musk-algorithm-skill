---
name: musk-algorithm
description: >
  Systematische Prozess- und Anforderungsanalyse nach dem 5-Schritte-Algorithmus
  (inspiriert von Elon Musks Engineering-Methodik), adaptiert für öffentliche
  Verwaltung, Bildung und Organisationsentwicklung. Verwende diesen Skill immer,
  wenn der User (1) Prozesse optimieren oder hinterfragen will, (2) Anforderungen
  oder Pflichtenheft-Dokumente bewerten möchte, (3) Bürokratie abbauen oder
  Workflows verschlanken will, (4) IT-Systeme, Tools oder Plattformen auf
  Notwendigkeit prüfen möchte, (5) nach "Vereinfachung", "Effizienz",
  "Prozessoptimierung", "Anforderungsanalyse" oder "Lean" fragt, (6) einen
  Projektplan oder eine Organisationsstruktur challengen will, oder (7) explizit
  den "Musk-Algorithmus" oder "5-Schritte-Methode" erwähnt. Auch geeignet für
  Retrospektiven, Digitalisierungsprojekte und Change-Management-Analysen.
---

# Der 5-Schritte-Algorithmus: Systematische Prozess- und Anforderungsanalyse

Dieser Skill implementiert eine rigoros sequenzielle Analysemethodik, die Prozesse,
Anforderungen und Organisationsstrukturen systematisch auf Notwendigkeit, Einfachheit
und Effizienz prüft. Die Methodik stammt aus dem Engineering (SpaceX/Tesla) und ist
hier für den Kontext öffentliche Verwaltung, Bildung und Wissensarbeit adaptiert.

## Kernprinzip

**Die Reihenfolge ist nicht verhandelbar.** Die fünf Schritte müssen strikt sequenziell
durchlaufen werden. Der häufigste Fehler ist, Schritt 5 (Automatisieren) vor Schritt 1
(Anforderungen hinterfragen) zu setzen – das führt dazu, dass man einen unsinnigen
Prozess automatisiert statt ihn zu eliminieren.

> "Wenn du dein Grab schaufelst, schaufel nicht schneller." — Elon Musk

## Kontextadaption: Öffentliche Verwaltung & Bildung

Dieser Skill operiert mit einer **kalibrierten Risikotoleranz**. Im Gegensatz zu
Hardware-Engineering, wo ein gelöschtes Bauteil rückstandslos wieder eingebaut werden
kann, haben Entscheidungen in der öffentlichen Verwaltung oft irreversible soziale,
rechtliche oder politische Konsequenzen.

Wende daher bei jedem Schritt den **Chesterton's-Fence-Test** an: Bevor du einen
Prozess, eine Regel oder eine Struktur als "unnötig" klassifizierst, stelle sicher,
dass du verstehst, **warum** sie ursprünglich eingeführt wurde. Erst wenn der
ursprüngliche Grund dokumentiert und als obsolet bewertet ist, darf gelöscht werden.

**Zusätzliche Leitplanken für den öffentlichen Sektor:**
- Rechtliche Grundlagen (Gesetze, Verordnungen, Datenschutz) sind keine "dummen Anforderungen" – sie sind Rahmenbedingungen. Unterscheide klar zwischen gesetzlichen Pflichten und internen Gewohnheiten.
- "Checks and Balances" in demokratischen Strukturen sind bewusste Sicherheitsfeatures, keine Bürokratie.
- Betroffene Stakeholder (Lehrpersonen, Eltern, Schülerinnen und Schüler, Behörden) müssen bei Löschentscheiden einbezogen werden.

---

## Die 5 Schritte

Führe den User sequenziell durch alle fünf Schritte. Überspringe keinen Schritt.
Dokumentiere die Ergebnisse jedes Schritts, bevor du zum nächsten übergehst.

### Schritt 1: Anforderungen hinterfragen

**Imperativ:** Jede Anforderung ist schuldig, bis ihre Unschuld bewiesen ist.

Gehe bei jeder Anforderung, jedem Prozessschritt oder jeder Regel wie folgt vor:

1. **Wer hat diese Anforderung aufgestellt?** Verlange einen konkreten Namen. "Die Abteilung" oder "man hat das schon immer so gemacht" ist keine valide Antwort. Wenn niemand die Urheberschaft übernimmt, ist das ein starkes Signal für eine Legacy-Anforderung.

2. **Welches Problem löst sie konkret?** Formuliere das Problem in einem Satz. Wenn das nicht gelingt, ist die Anforderung vermutlich unklar definiert.

3. **Ist das Problem noch aktuell?** Technologien, gesetzliche Grundlagen und organisatorische Kontexte ändern sich. Eine Anforderung, die 2015 sinnvoll war, kann 2026 obsolet sein.

4. **Gibt es eine gesetzliche Grundlage?** Wenn ja: Anforderung bleibt (aber prüfe, ob die *Umsetzung* vereinfacht werden kann). Wenn nein: weiter zu Schritt 2.

5. **Wessen Autorität schützt die Anforderung?** Hinterfrage besonders Anforderungen von hochrangigen oder technisch versierten Personen – diese werden am seltensten in Frage gestellt, sind aber nicht automatisch korrekt.

**Output dieses Schritts:** Eine klassifizierte Liste aller Anforderungen:
- 🟢 **Valide** – gesetzlich begründet oder nachweislich problemlösend
- 🟡 **Fragwürdig** – Ursprung unklar, Problem möglicherweise obsolet
- 🔴 **Kandidat für Löschung** – kein klarer Urheber, kein aktuelles Problem

Kennzeichne bei jeder Bewertung die **Datenqualität** der Einschätzung:
- 🔵 **Belegt** – Bewertung basiert auf nachprüfbaren Fakten (Gesetze, Kennzahlen, dokumentierte Prozesse)
- ⚪ **Schätzung** – Bewertung basiert auf Annahmen, Erfahrungswerten oder unvollständigen Informationen

Dieser Indikator ist entscheidend für GL-Entscheide: Empfehlungen auf Basis von ⚪-Schätzungen erfordern eine Validierung vor der Umsetzung. Weise den User aktiv darauf hin, wo belastbare Daten fehlen und wie sie beschafft werden können (z.B. durch Messung, Befragung, Datenexport).

### Schritt 2: Löschen

**Imperativ:** Lösche jede Anforderung, jeden Prozessschritt und jedes Tool, das nicht als 🟢 klassifiziert wurde, bis das Gegenteil bewiesen ist.

Die natürliche Tendenz in Organisationen ist es, Dinge hinzuzufügen ("Sicherheitshalber behalten wir das"). Dieser Schritt bekämpft aktiv den **Additions-Bias**.

**Frage für jeden 🟡- und 🔴-Kandidaten:**
- Was passiert konkret, wenn wir das streichen?
- Wer ist betroffen und wie schwer?
- Ist die Streichung reversibel? (Wichtig: In der Verwaltung oft schwieriger als in der Technik!)

**Pflicht-Teilschritt: Stakeholder-Analyse (vor jeder Löschentscheidung)**

Bevor ein Element gelöscht wird, identifiziere und dokumentiere alle betroffenen Stakeholder. Dieser Teilschritt ist nicht optional – er ist das Äquivalent einer Sicherheitsprüfung vor dem Rückbau.

Erstelle für jeden Löschkandidaten eine Stakeholder-Zeile:

| Löschkandidat | Betroffene Stakeholder | Art der Betroffenheit | Einbezug erforderlich? | Kommunikationsmassnahme |
|---|---|---|---|---|
| [Element] | [Wer?] | [Wie betroffen: Arbeitslast, Rechte, Zugang, Information?] | [Ja/Nein – Ja bei direkter Betroffenheit] | [Was muss kommuniziert werden, bevor gelöscht wird?] |

Lösche kein Element, bei dem in der Spalte "Einbezug erforderlich" ein "Ja" steht, ohne dass der User bestätigt hat, dass der Einbezug stattgefunden hat oder geplant ist. In der öffentlichen Verwaltung ist ein technisch korrekter Löschentscheid, der ohne Stakeholder-Einbezug umgesetzt wird, politisch ein Fehler.

**Die 10%-Heuristik (adaptiert):** In der Hardware-Welt gilt: Wenn du nie etwas wieder hinzufügen musst, hast du zu wenig gelöscht. Im Verwaltungskontext bedeutet das: Sei bereit, mutig zu streichen, aber **dokumentiere**, was du streichst und warum, damit eine Wiedereinführung schnell möglich ist.

**Sicherheitsventil für den öffentlichen Sektor:**
- Streiche nie Prozesse, die den Rechtsschutz von Personen betreffen, ohne juristische Absicherung.
- Streiche nie Kommunikationskanäle, ohne sicherzustellen, dass Betroffene über Alternativen informiert sind.
- Führe bei grösseren Streichungen ein **Pilotprojekt** durch, bevor du flächendeckend löschst.

**Output dieses Schritts:** Eine Liste gestrichener Elemente mit Begründung, Stakeholder-Analyse und Reversibilitätsplan.

### Schritt 3: Vereinfachen und optimieren

**Imperativ:** Optimiere nur, was nach Schritt 1 und 2 übrig geblieben ist. Optimiere nie einen Prozess, der gar nicht existieren sollte.

Dieser Schritt ist der Ort für **First-Principles-Thinking**: Gehe zurück zur physikalischen (oder organisatorischen) Grundfunktion.

**Leitfragen:**
- Was ist die eigentliche Funktion dieses Prozesses? (Nicht: Wie machen es andere?)
- Können mehrere Schritte zu einem zusammengefasst werden?
- Können mehrere Tools durch eines ersetzt werden?
- Kann ein manueller Übergabepunkt eliminiert werden?
- Kann die Anzahl beteiligter Personen/Rollen reduziert werden?

**Konkrete Vereinfachungsmuster für die Verwaltung:**
- **Medienbrüche eliminieren:** PDF → Formular → manuelle Eingabe → Datenbank wird zu: Online-Formular → Datenbank
- **Genehmigungskaskaden kürzen:** 5-stufige Freigabe wird zu 2-stufiger Freigabe (wenn rechtlich möglich)
- **Informationsarchitektur bereinigen:** 12 verschiedene Sharepoints werden zu einer strukturierten Ablage
- **Rollen konsolidieren:** Wenn drei Personen dasselbe prüfen, reicht oft eine

**Output dieses Schritts:** Vereinfachter Prozess/Workflow/Struktur mit Vorher-Nachher-Vergleich.

### Schritt 4: Beschleunigen

**Imperativ:** Erst jetzt, nachdem der Prozess von Ballast befreit und vereinfacht ist, darf die Geschwindigkeit erhöht werden.

**Leitfragen:**
- Wo sind die Wartezeiten? (Genehmigungen, Rückmeldungen, Schnittstellen)
- Können Schritte parallelisiert statt sequenziell durchgeführt werden?
- Wie kann die Durchlaufzeit (Cycle Time) gemessen und reduziert werden?
- Welche Engpässe (Bottlenecks) begrenzen den Gesamtdurchsatz?

**Im Bildungs- und Verwaltungskontext:**
- Deadlines setzen, wo bisher "sobald möglich" galt
- Synchrone Meetings durch asynchrone Entscheide ersetzen, wo möglich
- Feedback-Schleifen verkürzen (wöchentlich statt quartalsweise)
- Batchverarbeitung einführen (z.B. Anträge gesammelt statt einzeln bearbeiten)

**Output dieses Schritts:** Optimierter Zeitplan mit identifizierten Beschleunigungshebeln.

### Schritt 5: Automatisieren

**Imperativ:** Automatisiere erst, wenn der Prozess manuell funktioniert und stabilisiert ist. Automatisierung eines kaputten Prozesses erzeugt automatisierten Müll.

**Leitfragen:**
- Ist der Prozess stabil und vorhersagbar? (Wenn nicht: zurück zu Schritt 3)
- Welche Schritte sind repetitiv und regelbasiert? (→ Automatisierungskandidat)
- Welche Schritte erfordern menschliches Urteilsvermögen? (→ Nicht automatisieren)
- Welche KI-Tools oder Workflows können eingesetzt werden?

**Automatisierungskandidaten in der Verwaltung/Bildung:**
- Standardantworten auf wiederkehrende Anfragen (z.B. KOMKI)
- Datenaggregation und Reporting
- Terminplanung und Erinnerungen
- Dokumentenklassifizierung und -routing
- Formularvalidierung

**Warnung:** Die "Alien Dreadnought"-Lektion gilt auch hier: Tesla versuchte, alles zu automatisieren, bevor die Prozesse stabil waren, und scheiterte. Beginne mit der Automatisierung des einfachsten, stabilsten Teilprozesses und erweitere schrittweise.

**Output dieses Schritts:** Automatisierungsplan mit Priorisierung (Quick Wins vs. Langfristprojekte).

---

## Anwendungsformat

Wenn der User einen Prozess, ein Dokument oder eine Struktur zur Analyse gibt, führe die Analyse in folgendem Format durch:

```
## Analyse: [Name des Prozesses/Dokuments]

### Schritt 1: Anforderungen hinterfragen
[Klassifizierte Liste: 🟢 Valide | 🟡 Fragwürdig | 🔴 Löschkandidat — jeweils mit Datenqualität: 🔵 Belegt | ⚪ Schätzung]

### Schritt 2: Löschen
[Stakeholder-Analyse + gestrichene Elemente mit Begründung und Reversibilitätsplan]

### Schritt 3: Vereinfachen
[Vorher-Nachher-Vergleich]

### Schritt 4: Beschleunigen
[Identifizierte Hebel und optimierter Zeitplan]

### Schritt 5: Automatisieren
[Priorisierter Automatisierungsplan]

### Zusammenfassung
[Erwartete Wirkung: Zeitersparnis, Kostenreduktion, Qualitätsverbesserung]

### Quick-Win-Matrix
[2×2-Matrix: Aufwand vs. Wirkung — siehe Anleitung unten]
```

## Quick-Win-Matrix: Priorisierung der Massnahmen

Schliesse jede Analyse mit einer **Quick-Win-Matrix** ab. Diese ordnet alle identifizierten
Massnahmen (aus Schritten 2–5) in ein 2×2-Raster ein, damit der User weiss, wo anfangen.

```
                      Hohe Wirkung
                          │
       ┌──────────────────┼──────────────────┐
       │                  │                  │
       │   STRATEGISCH    │   QUICK WINS     │
       │   Planen &       │   Sofort         │
       │   priorisieren   │   umsetzen       │
       │                  │                  │
Hoher ─┼──────────────────┼──────────────────┼─ Niedriger
Aufwand│                  │                  │  Aufwand
       │   VERMEIDEN      │   MITNEHMEN      │
       │   Nur wenn       │   Bei Gelegenheit│
       │   nichts anderes │   erledigen      │
       │   übrig bleibt   │                  │
       │                  │                  │
       └──────────────────┼──────────────────┘
                          │
                     Niedrige Wirkung
```

Ordne jede Massnahme einem Quadranten zu und formuliere eine klare Empfehlung:
- **Quick Wins** (niedrig Aufwand, hohe Wirkung): "Innerhalb von 2 Wochen umsetzbar"
- **Strategisch** (hoher Aufwand, hohe Wirkung): "Projekt aufsetzen, GL-Entscheid einholen"
- **Mitnehmen** (niedriger Aufwand, niedrige Wirkung): "Bei nächster Gelegenheit erledigen"
- **Vermeiden** (hoher Aufwand, niedrige Wirkung): "Nur wenn alle anderen Massnahmen umgesetzt sind"

Kennzeichne auch hier die Datenqualität: Wenn Aufwand oder Wirkung auf ⚪-Schätzungen
basieren, weise darauf hin, dass die Einordnung nach Validierung ändern kann.

## Interaktionsmuster

- **Bei unklarem Kontext:** Frage den User nach dem spezifischen Prozess, Dokument oder der Struktur, die analysiert werden soll. Führe nicht alle fünf Schritte im Vakuum durch.
- **Bei komplexen Systemen:** Schlage vor, den Algorithmus auf einen Teilbereich anzuwenden und dann zu iterieren, statt alles auf einmal zu analysieren.
- **Bei Widerstand:** Es ist normal, dass Beteiligte Streichungen oder Vereinfachungen ablehnen ("Das haben wir immer so gemacht"). Hilf dem User, zwischen berechtigtem Widerstand (Chesterton's Fence) und Gewohnheit zu unterscheiden.
- **Sprache:** Verwende Schweizerische Rechtschreibung (kein ß, Strasse statt Straße etc.) und verwaltungsübliche Terminologie.

## Wann dieser Skill NICHT geeignet ist

- Für reine Kreativaufgaben (Texte schreiben, Brainstorming ohne Optimierungsziel)
- Für Compliance-Fragen, bei denen die Anforderungen gesetzlich fixiert und nicht verhandelbar sind
- Für Notfall- oder Krisensituationen, in denen schnelle Entscheide ohne Analyse nötig sind
- Wenn der User explizit keine Prozessoptimierung wünscht
