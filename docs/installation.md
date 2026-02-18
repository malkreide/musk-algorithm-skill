# Installation and Setup

🌐 **Language / Sprache:** [English](installation.md) | [Deutsch](installation.de.md)

## Overview

The 5-Step Algorithm Skill can be integrated into Claude in several ways. This guide covers all common scenarios.

---

## Option 1: Claude.ai (Web, Desktop, Mobile)

### Prerequisites
- Claude.ai account (free or Pro/Team)
- Access to the Skills feature

### Step-by-Step Guide

1. **Download the skill file**
   ```bash
   # Via browser: Download SKILL.md from GitHub
   # Via terminal:
   curl -O https://raw.githubusercontent.com/malkreide/musk-algorithm-skill/main/SKILL.md
   ```

2. **Import into Claude.ai**
   - Open [claude.ai](https://claude.ai)
   - Click on your profile picture (bottom left)
   - Select **Settings**
   - Navigate to **Skills**
   - Click **+ Add Skill**
   - Select **Upload from file**
   - Choose the downloaded `SKILL.md` file
   - Click **Save**

3. **Activate the skill**
   - The skill is now in your skill library
   - Activate it globally or only for specific projects

### Verification

Test the skill with:
```
Can you explain the Musk Algorithm to me?
```

Claude should explain the 5 steps sequentially.

---

## Option 2: Claude API (Programmatic)

### Prerequisites
- Anthropic API Key
- Python 3.8+ or Node.js 16+

### Python Example

```python
import anthropic

# Load skill content
with open("SKILL.md", "r") as f:
    skill_content = f.read()

client = anthropic.Anthropic(api_key="your-api-key")

message = client.messages.create(
    model="claude-sonnet-4-20250514",
    max_tokens=4096,
    system=skill_content,  # Skill as system prompt
    messages=[
        {
            "role": "user",
            "content": "Analyze the procurement process."
        }
    ]
)

print(message.content)
```

### Node.js Example

```javascript
import Anthropic from "@anthropic-ai/sdk";
import fs from "fs";

// Load skill content
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
      content: "Analyze the procurement process.",
    },
  ],
});

console.log(message.content);
```

---

## Option 3: MCP Server (Model Context Protocol)

### Prerequisites
- MCP server setup (see [MCP Docs](https://modelcontextprotocol.io))
- Claude Desktop App or compatible tool

### Step 1: Create MCP Resource

Create a `mcp_server.py`:

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
            name="5-Step Algorithm",
            mimeType="text/markdown",
            description="5-step process analysis for public administration"
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

### Step 2: Register MCP Server in Claude Desktop

Add to `~/Library/Application Support/Claude/claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "musk-algorithm": {
      "command": "python",
      "args": ["/path/to/mcp_server.py"]
    }
  }
}
```

### Step 3: Restart Claude Desktop

The skill is now available as a resource.

---

## Option 4: Local File Reference (Quick Test)

For quick testing without permanent installation:

1. Download `SKILL.md`
2. In Claude.ai: Upload the file to a chat
3. Write: "Use the methodology from this file for the following analysis: [your process]"

**Drawback:** Works only for the current chat, not persistent.

---

## Troubleshooting

### "Skill not found"
- Ensure the file was uploaded correctly
- Check whether the skill is activated in settings

### "Skill doesn't work as expected"
- Ensure you're using the latest version of `SKILL.md`
- Check whether the skill content is complete (~15 KB file size)

### API Integration: "System prompt too long"
- The skill is approximately 15 KB — use a model with a large context window (e.g., Claude Sonnet 4)
- Alternatively: Compress the skill to its core steps

---

## Best Practices

1. **Project-specific activation**: Only activate the skill in projects where process optimization is relevant
2. **Combination with other skills**: The 5-Step Algorithm works well combined with:
   - Document creation skills (for reports)
   - Data analysis skills (for metrics)
3. **Regular updates**: Check monthly for new versions in the GitHub repo

---

## Support

For questions or issues:
- Open a [GitHub Issue](https://github.com/malkreide/musk-algorithm-skill/issues)
