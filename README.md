# Musk-Algorithmus Skill für Claude

Ein systematischer 5-Schritte-Ansatz zur Prozess- und Anforderungsanalyse, adaptiert für öffentliche Verwaltung, Bildung und Organisationsentwicklung.

## Übersicht

Dieser Claude Skill implementiert eine rigoros sequenzielle Analysemethodik, die Prozesse, Anforderungen und Organisationsstrukturen systematisch auf **Notwendigkeit**, **Einfachheit** und **Effizienz** prüft. Die Methodik stammt aus dem Engineering (SpaceX/Tesla) und ist hier speziell für den Kontext der öffentlichen Verwaltung und des Bildungswesens adaptiert.

### Kernprinzip: Die richtige Reihenfolge

Die fünf Schritte müssen **strikt sequenziell** durchlaufen werden:

1. **Anforderungen hinterfragen** – Ist das überhaupt nötig?
2. **Löschen** – Entferne alles Unnötige
3. **Vereinfachen** – Optimiere nur, was bleibt
4. **Beschleunigen** – Mache es schneller
5. **Automatisieren** – Erst jetzt: Technologie einsetzen

> "Wenn du dein Grab schaufelst, schaufel nicht schneller." – Elon Musk

Der häufigste Fehler ist, Schritt 5 (Automatisieren) vor Schritt 1 (Hinterfragen) zu setzen – das führt dazu, dass man einen unsinnigen Prozess automatisiert, statt ihn zu eliminieren.

## Einsatzgebiete

Verwende diesen Skill, wenn du:

- ✅ Prozesse optimieren oder hinterfragen willst
- ✅ Anforderungen oder Pflichtenhefte bewerten möchtest
- ✅ Bürokratie abbauen oder Workflows verschlanken willst
- ✅ IT-Systeme, Tools oder Plattformen auf Notwendigkeit prüfen möchtest
- ✅ Einen Projektplan oder eine Organisationsstruktur challengen willst
- ✅ Retrospektiven, Digitalisierungsprojekte oder Change-Management-Analysen durchführst

## Installation

### Für Claude.ai (Web/Desktop/Mobile)

1. Öffne [Claude.ai](https://claude.ai)
2. Gehe zu **Einstellungen** → **Skills**
3. Klicke auf **Skill hinzufügen**
4. Wähle **Von Datei importieren**
5. Lade die `SKILL.md` Datei hoch

### Für Claude API / MCP

```bash
# Skill-Datei herunterladen
curl -O https://raw.githubusercontent.com/[dein-username]/musk-algorithm-skill/main/SKILL.md

# In deinem MCP-Server als Resource einbinden
```

## Verwendung

### Grundlegendes Beispiel

```
User: Ich habe einen Prozess für die Verwaltung von Schulanmeldungen. 
Können wir den mit dem Musk-Algorithmus analysieren?

Claude: [Führt sequenziell durch alle 5 Schritte und liefert:]
- Klassifizierte Anforderungsliste (🟢 Valide | 🟡 Fragwürdig | 🔴 Löschkandidat)
- Stakeholder-Analyse für Streichungen
- Vereinfachten Prozess (Vorher-Nachher)
- Beschleunigungshebel
- Automatisierungsplan
- Quick-Win-Matrix zur Priorisierung
```

### Mehr Beispiele

Siehe [`examples/`](examples/) Verzeichnis für vollständige Anwendungsbeispiele:
- Prozessanalyse: Schulanmeldungen
- Anforderungsdokument-Audit: IT-Beschaffung
- IT-System-Bewertung: Tool-Konsolidierung

## Besonderheiten für öffentliche Verwaltung

Dieser Skill operiert mit **kalibrierter Risikotoleranz** und berücksichtigt:

- **Rechtliche Grundlagen** (Gesetze, Verordnungen, Datenschutz) als unverrückbare Rahmenbedingungen
- **Chesterton's Fence**: Verstehe den ursprünglichen Grund, bevor du etwas löschst
- **Stakeholder-Einbezug**: Pflicht-Analyse vor jeder Löschentscheidung
- **Checks and Balances** in demokratischen Strukturen als bewusste Sicherheitsfeatures

## Quick-Win-Matrix

Jede Analyse endet mit einer Priorisierungsmatrix:

```
                    Hohe Wirkung
       ┌────────────────┬────────────────┐
       │  STRATEGISCH   │   QUICK WINS   │
       │  Planen        │   Sofort       │
Hoher ─┼────────────────┼────────────────┼─ Niedriger
Aufwand│  VERMEIDEN     │   MITNEHMEN    │  Aufwand
       │  Nur wenn nötig│   Bei Gelegenheit│
       └────────────────┴────────────────┘
                    Niedrige Wirkung
```

## Technische Details

- **Format**: Markdown-basierter Claude Skill
- **Sprache**: Deutsch (Schweizer Rechtschreibung)
- **Zielgruppe**: Öffentliche Verwaltung, Bildungseinrichtungen, Nonprofit-Organisationen
- **Methodischer Ursprung**: Elon Musk's 5-Step Algorithm (adaptiert)

## Lizenz

[MIT License](LICENSE) – Frei verwendbar für öffentliche und private Zwecke.

## Credits

- **Entwickelt von**: Hayal Oezkan
- **Methodischer Ursprung**: Elon Musk's 5-Step Algorithm (SpaceX/Tesla)
- **Adaptation**: Speziell angepasst für öffentliche Verwaltung und Bildung

## Beiträge

Verbesserungsvorschläge, Beispiele oder Fehlerberichte sind willkommen! Bitte erstelle ein Issue oder einen Pull Request.

## Weiterführende Ressourcen

- [Original-Quelle: Walter Isaacson – Elon Musk Biografie](https://www.simonandschuster.com/books/Elon-Musk/Walter-Isaacson/9781982181284)
- [Chesterton's Fence Principle](https://fs.blog/chestertons-fence/)
- [First Principles Thinking](https://jamesclear.com/first-principles)

---

**Hinweis**: Dieser Skill ersetzt keine professionelle Beratung in rechtlichen, finanziellen oder sicherheitsrelevanten Fragen. Bei Unsicherheit konsultiere Fachpersonen.

---

<div align="center">

**Made with ❤️ in Zürich**

[LinkedIn](https://www.linkedin.com/in/hayaloezkan/) • [Documentation](docs/) • [Contributing](CONTRIBUTING.md)

</div>
