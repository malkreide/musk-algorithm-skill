# Installation und Einrichtung

## Übersicht

Der Musk-Algorithmus Skill kann auf verschiedene Arten in Claude integriert werden. Diese Anleitung deckt alle gängigen Szenarien ab.

---

## Option 1: Claude.ai (Web, Desktop, Mobile)

### Voraussetzungen
- Claude.ai Account (kostenlos oder Pro/Team)
- Zugriff auf die Skills-Funktion

### Schritt-für-Schritt-Anleitung

1. **Skill-Datei herunterladen**
   ```bash
   # Via Browser: Lade SKILL.md von GitHub herunter
   # Via Terminal:
   curl -O https://raw.githubusercontent.com/[dein-username]/musk-algorithm-skill/main/SKILL.md
   ```

2. **In Claude.ai importieren**
   - Öffne [claude.ai](https://claude.ai)
   - Klicke auf dein Profilbild (unten links)
   - Wähle **Einstellungen**
   - Navigiere zu **Skills**
   - Klicke auf **+ Skill hinzufügen**
   - Wähle **Von Datei hochladen**
   - Wähle die heruntergeladene `SKILL.md` Datei
   - Klicke **Speichern**

3. **Skill aktivieren**
   - Der Skill ist jetzt in deiner Skill-Bibliothek
   - Aktiviere ihn global oder nur für bestimmte Projekte

### Verifizierung

Teste den Skill mit:
```
Kannst du mir den Musk-Algorithmus erklären?
```

Claude sollte die 5 Schritte sequenziell erklären.

---

## Option 2: Claude API (Programmgesteuert)

### Voraussetzungen
- Anthropic API Key
- Python 3.8+ oder Node.js 16+

### Python-Beispiel

```python
import anthropic

# Skill-Inhalt laden
with open("SKILL.md", "r") as f:
    skill_content = f.read()

client = anthropic.Anthropic(api_key="your-api-key")

message = client.messages.create(
    model="claude-sonnet-4-20250514",
    max_tokens=4096,
    system=skill_content,  # Skill als System-Prompt
    messages=[
        {
            "role": "user", 
            "content": "Analysiere den Prozess für Beschaffungen."
        }
    ]
)

print(message.content)
```

### Node.js-Beispiel

```javascript
import Anthropic from "@anthropic-ai/sdk";
import fs from "fs";

// Skill-Inhalt laden
const skillContent = fs.readFileSync("SKILL.md", "utf8");

const client = new Anthropic({
  apiKey: process.env.ANTHROPIC_API_KEY,
});

const message = await client.messages.create({
  model: "claude-sonnet-4-20250514",
  max_tokens: 4096,
  system: skillContent,
  messages: [
    {
      role: "user",
      content: "Analysiere den Prozess für Beschaffungen.",
    },
  ],
});

console.log(message.content);
```

---

## Option 3: MCP Server (Model Context Protocol)

### Voraussetzungen
- MCP-Server-Setup (siehe [MCP Docs](https://modelcontextprotocol.io))
- Claude Desktop App oder kompatibles Tool

### Schritt 1: MCP-Resource erstellen

Erstelle eine `mcp_server.py`:

```python
from mcp.server import Server
from mcp.types import Resource
import asyncio

server = Server("musk-algorithm-skill")

@server.list_resources()
async def list_resources() -> list[Resource]:
    return [
        Resource(
            uri="skill://musk-algorithm",
            name="Musk-Algorithmus",
            mimeType="text/markdown",
            description="5-Schritte-Prozessanalyse für öffentliche Verwaltung"
        )
    ]

@server.read_resource()
async def read_resource(uri: str) -> str:
    if uri == "skill://musk-algorithm":
        with open("SKILL.md", "r") as f:
            return f.read()
    raise ValueError(f"Unknown resource: {uri}")

async def main():
    async with server.start():
        await asyncio.Event().wait()

if __name__ == "__main__":
    asyncio.run(main())
```

### Schritt 2: MCP-Server in Claude Desktop registrieren

Füge in `~/Library/Application Support/Claude/claude_desktop_config.json` hinzu:

```json
{
  "mcpServers": {
    "musk-algorithm": {
      "command": "python",
      "args": ["/pfad/zu/mcp_server.py"]
    }
  }
}
```

### Schritt 3: Claude Desktop neu starten

Der Skill steht jetzt als Resource zur Verfügung.

---

## Option 4: Lokale Datei-Referenz (Schnelltest)

Für schnelles Testen ohne dauerhafte Installation:

1. Lade `SKILL.md` herunter
2. In Claude.ai: Lade die Datei in einen Chat hoch
3. Schreibe: "Verwende die Methodik aus dieser Datei für folgende Analyse: [dein Prozess]"

**Nachteil:** Funktioniert nur für den aktuellen Chat, nicht persistent.

---

## Troubleshooting

### "Skill nicht gefunden"
- Stelle sicher, dass die Datei korrekt hochgeladen wurde
- Prüfe, ob der Skill in den Einstellungen aktiviert ist

### "Skill funktioniert nicht wie erwartet"
- Stelle sicher, dass du die aktuellste Version der `SKILL.md` verwendest
- Prüfe, ob der Skill-Inhalt vollständig ist (15 KB Grösse)

### API-Integration: "System Prompt zu lang"
- Der Skill ist ca. 15 KB gross – verwende ein Modell mit grossem Context Window (z.B. Claude Sonnet 4)
- Alternativ: Komprimiere den Skill auf die Kernschritte

---

## Best Practices

1. **Projekt-spezifische Aktivierung**: Aktiviere den Skill nur in Projekten, wo Prozessoptimierung relevant ist
2. **Kombination mit anderen Skills**: Der Musk-Algorithmus lässt sich gut kombinieren mit:
   - Dokumenten-Erstellungs-Skills (für Berichte)
   - Datenanalyse-Skills (für Kennzahlen)
3. **Regelmässige Updates**: Prüfe monatlich auf neue Versionen im GitHub-Repo

---

## Support

Bei Fragen oder Problemen:
- Öffne ein [GitHub Issue](https://github.com/[dein-username]/musk-algorithm-skill/issues)
- Kontaktiere: [deine-email@example.com]
