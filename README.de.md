# Der 5-Schritte-Algorithmus Skill für Claude

🌐 **Language / Sprache:** [English](README.md) | [Deutsch](README.de.md)

Ein Claude Skill, der systematische Prozess- und Anforderungsanalyse nach dem 5-Schritte-Algorithmus (inspiriert von Elon Musks Engineering-Methodik) implementiert, adaptiert für öffentliche Verwaltung, Bildung und Organisationsentwicklung.

## Überblick

Dieser Skill leitet Claude durch eine rigoros sequenzielle Analysemethodik, die Prozesse, Anforderungen und Organisationsstrukturen systematisch auf Notwendigkeit, Einfachheit und Effizienz prüft. Ursprünglich für Hardware-Engineering bei SpaceX/Tesla entwickelt, wurde die Methodik sorgfältig für Wissensarbeit im öffentlichen Sektor adaptiert — mit zusätzlichen Leitplanken für Rechtskonformität, Stakeholder-Einbezug und demokratische Rechenschaftspflicht.

## Die 5 Schritte

Die Reihenfolge ist nicht verhandelbar. Jeder Schritt muss abgeschlossen werden, bevor zum nächsten übergegangen wird.

1. **Anforderungen hinterfragen** — Jede Anforderung ist schuldig, bis ihre Unschuld bewiesen ist. Identifiziere, wer sie aufgestellt hat, welches Problem sie löst und ob dieses Problem noch existiert.

2. **Löschen** — Entferne alles, was nicht als valide klassifiziert wurde. Bekämpfe den Additions-Bias. Führe vor jeder Löschung eine obligatorische Stakeholder-Analyse durch.

3. **Vereinfachen und optimieren** — Optimiere nur, was übrig bleibt. Wende First-Principles-Thinking an. Eliminiere Medienbrüche, kürze Genehmigungskaskaden, konsolidiere Rollen.

4. **Beschleunigen** — Erhöhe die Geschwindigkeit erst nach der Vereinfachung. Finde Engpässe, parallelisiere Schritte, verkürze Feedback-Schleifen.

5. **Automatisieren** — Automatisiere zuletzt, nie zuerst. Automatisiere nur stabile, vorhersagbare, regelbasierte Prozesse.

## Schlüssel-Adaptionen für die öffentliche Verwaltung

Im Gegensatz zum ursprünglichen Engineering-Kontext enthält diese Adaption:

- **Chesterton's-Fence-Test** — Verstehe, warum eine Regel existiert, bevor du sie entfernst
- **Obligatorische Stakeholder-Analyse** — Vor jeder Löschentscheidung
- **Datenqualitäts-Indikatoren** — 🔵 Belegt vs. ⚪ Schätzung für GL-Entscheide
- **Bewusstsein für rechtliche Rahmenbedingungen** — Unterscheide gesetzliche Pflichten von internen Gewohnheiten
- **Reversibilitätsplanung** — Dokumentiere Löschungen für schnelle Wiedereinsetzung
- **Pilotprojekte** — Teste vor der organisationsweiten Einführung

## Anwendungsfälle

Dieser Skill aktiviert sich, wenn Nutzende:
- Prozesse optimieren oder hinterfragen wollen
- Anforderungen oder Pflichtenheft-Dokumente bewerten möchten
- Bürokratie abbauen oder Workflows verschlanken wollen
- IT-Systeme, Tools oder Plattformen auf Notwendigkeit prüfen möchten
- Nach «Vereinfachung», «Effizienz», «Prozessoptimierung» oder «Lean» fragen
- Einen Projektplan oder eine Organisationsstruktur challengen wollen
- Den «Musk-Algorithmus» oder die «5-Schritte-Methode» erwähnen

## Installation

### Für Claude.ai Projekte (Empfohlen)

1. Lade die Datei `SKILL.de.md` aus diesem Repository herunter
2. Gehe in deinem Claude.ai Projekt zu Projekteinstellungen → Skills
3. Lade die Datei hoch oder erstelle einen neuen benutzerdefinierten Skill
4. Der Skill wird automatisch basierend auf Nutzerinteraktionsmustern aktiviert

### Für Claude Desktop / API

Füge den Skill-Inhalt in deine System-Prompts oder benutzerdefinierten Anweisungen ein.

Detaillierte Installationsanweisungen (inkl. API und MCP-Server) findest du im [Installationsleitfaden](docs/installation.de.md).

## Beispiel: Schulanmeldungs-Prozess

Das Repository enthält ein [vollständiges Anwendungsbeispiel](examples/example-1-schulanmeldungen.de.md), das einen Schulanmeldungs-Prozess analysiert, der von 12 auf 5 Schritte reduziert wurde — mit einer Verkürzung der Bearbeitungszeit von 6 Wochen auf unter 24 Stunden.

**Kernergebnisse aus dem Beispiel:**
- **Zeitersparnis (Sekretariat):** ~80%
- **Zeitersparnis (Eltern):** 6 Wochen → 24 Stunden
- **Fehlerreduktion:** ~90%
- **Kostenreduktion:** ~CHF 12'000/Jahr

## Ausgabeformat

Jede Analyse liefert:
- Klassifizierte Anforderungsliste (🟢 Valide | 🟡 Fragwürdig | 🔴 Löschkandidat)
- Stakeholder-Analyse mit Reversibilitätsplan
- Vorher-Nachher-Prozessvergleich
- Beschleunigungshebel und optimierter Zeitplan
- Priorisierter Automatisierungsplan
- **Quick-Win-Matrix** (2×2: Aufwand vs. Wirkung)

## Theoretische Fundierung

Der Skill integriert Konzepte aus:
- **Lean Manufacturing** (Toyota Production System) — Verschwendungselimination
- **First Principles Thinking** — Konventionen hinterfragen, zu Grundlagen zurückkehren
- **Theory of Constraints** (Goldratt) — Engpässe identifizieren und optimieren
- **Chesterton's Fence** — Verstehen vor dem Entfernen
- **Additions-Bias-Forschung** (Nature, 2021) — Menschen bevorzugen Hinzufügen vor Weglassen

Den vollständigen theoretischen Hintergrund findest du unter [Hintergrund](docs/background.de.md).

## Repository-Struktur

```
musk-algorithm-skill/
├── SKILL.md                    # Der Skill (Englisch)
├── SKILL.de.md                 # Der Skill (Deutsch)
├── README.md                   # Dokumentation (Englisch)
├── README.de.md                # Dokumentation (Deutsch)
├── LICENSE                     # MIT-Lizenz
├── CONTRIBUTING.md             # Beitragsrichtlinien (Englisch)
├── CONTRIBUTING.de.md          # Beitragsrichtlinien (Deutsch)
├── CHANGELOG.md                # Änderungsprotokoll
├── docs/
│   ├── installation.md         # Installationsleitfaden (Englisch)
│   ├── installation.de.md      # Installationsleitfaden (Deutsch)
│   ├── background.md           # Theoretischer Hintergrund (Englisch)
│   └── background.de.md        # Theoretischer Hintergrund (Deutsch)
└── examples/
    ├── example-1-school-enrollment.md    # Anwendungsbeispiel (Englisch)
    └── example-1-schulanmeldungen.de.md  # Anwendungsbeispiel (Deutsch)
```

## Mitwirken

Beiträge sind willkommen! Siehe [CONTRIBUTING.de.md](CONTRIBUTING.de.md) für Richtlinien.

## Lizenz

MIT License — siehe [LICENSE](LICENSE) Datei für Details.

## Autor

**Hayal Oezkan**  
Marketing und Kommunikation / KI-Fachgruppe Stadtverwaltung Zürich

GitHub: [@malkreide](https://github.com/malkreide)

## Danksagungen

Basierend auf Elon Musks 5-Schritte-Algorithmus, dokumentiert in Walter Isaacsons Biografie *Elon Musk* (2023), mit Adaptionen aus:
- Lean Manufacturing (Toyota Production System)
- Theory of Constraints (Eliyahu Goldratt)
- Chesterton's Fence (G.K. Chesterton)
- Additions-Bias-Forschung (Adams et al., Nature 2021)

---

> *«Wenn du nicht gelegentlich etwas wieder hinzufügen musst, hast du nicht genug gelöscht.»* — Elon Musk

---

<div align="center">

**Made with ❤️ in Zürich**

[LinkedIn](https://www.linkedin.com/in/hayaloezkan/) • [Dokumentation](docs/) • [Mitwirken](CONTRIBUTING.de.md)

</div>
