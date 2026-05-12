# Macrobond Plugin for Claude Code

Query economic and financial time-series data from [Macrobond](https://www.macrobond.com/) directly in Claude Code.

## Features

- **Search** for economic indicators (CPI, GDP, unemployment, yields, FX, commodities)
- **Fetch** time series with metadata and observations
- **Revision history** — query point-in-time data, track how statistics were revised
- **Cross-country sets** — build comparable datasets across regions
- **MCP Server** — automatically configured when you install the plugin

## Installation

### Option 1: Install from GitHub

```bash
claude /plugins install mb-ne/claude-plugin
```

### Option 2: Manual Clone

```bash
git clone https://github.com/mb-ne/claude-plugin.git
claude --plugin-dir ./claude-plugin
```

## Configuration

Set these environment variables before using the plugin:

```bash
export MACROBOND_MCP_URL=https://mcp.macrobond.com/sse
export MACROBOND_API_KEY=your_api_key_here
```

Add them to your shell profile (`~/.bashrc`, `~/.zshrc`, etc.) to persist across sessions.

## Usage

Invoke with: `/macrobond:macrobond`

Example queries:
- "Get US CPI year-over-year data"
- "Find German unemployment rate monthly"
- "Build a G7 inflation comparison"
- "What was US GDP as known on 2020-01-01?"

## Plugin Structure

```
claude-plugin/
├── .claude-plugin/
│   └── plugin.json              # Plugin manifest
├── .mcp.json                    # MCP server config
├── skills/
│   └── macrobond/
│       ├── SKILL.md             # Skill instructions
│       └── references/
│           ├── domain_knowledge.md
│           └── metadata_guide.md
└── LICENCE
```

## Requirements

- [Macrobond](https://www.macrobond.com/) account with API access
- Claude Code

## License

Proprietary - Macrobond Financial AB — see [LICENCE](LICENCE)
